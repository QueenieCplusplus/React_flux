# React flux
React 的單向資料流架構模式

# 3 Core Components

建議將這些元件關注在分離，可做單元測試。

* Model, store 儲存 (商業邏輯與資料的互動)

* Controller, dispatch 分配器為應用程式的中樞。算是種單例 Singleton。
 （利用 Action 介面定義分配器, Action 也可視為應用程式中的領域特定語言 domain-specific-language）

* View, view 視圖 (render 渲染應用程式的元件樹)


     
                                                                          
                                                                            
                                                                           
                  UI 的每一個動作會送到分配器。                          
                  它雖然不是核心元件，但構成分配器的                             分配器於資料儲存中，
                  領域定義語言。（使用者動作被翻譯成分配器動作）                   註冊回呼函式，
                  例如：新增、刪除、修改。                                     分配器也管理依賴。
            
                  
                              Action   ------>   Dispatcher   ------>   callbacl

                                |                                           |
                                |                                           V

        Web API ------>    Action Creator                                 Store    封裝商業邏輯與應用程式資料的互動，沒有 setter，新增通過資料儲存的變更事件送回應用程式，更新則通過分配器來到 store。

                                |                                           |
                                |                                           V

                               button                                    onChange(Event){
                               input     ------     Views      <------          
                                                                        return{};
                                                                        }
                                                                        
                                                                        
                                                                        
                                                                        
                                                                        
                                                                        
                                                                        
