# React flux
React 的單向資料流架構模式

# 3 Core Components

建議將這些元件關注在分離，可做單元測試。

* Model, store 儲存 (商業邏輯與資料的互動)

* Controller, dispatch 分配器為應用程式的中樞。算是種單例 Singleton。
 （利用 Action 介面定義分配器, Action 也可視為應用程式中的領域特定語言 domain-specific-language）

* View, view 視圖 (render 渲染應用程式的元件樹)


                              Action   ------>   Dispatcher   ------>   callbacl

                                |                                           |
                                |                                           V

        Web API ------>    Action Creator                                 Store

                                |                                           |
                                |                                           V

                               button                                    onChange(Event){
                               input     ------     Views      <------          
                                                                          return{};
                                                                        }
                                                                        
                                                                        
                                                                        
                                                                        
