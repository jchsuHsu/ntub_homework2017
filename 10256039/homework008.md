# 作業 008

1. 如果直接在發生失敗的時候 `redirect` 到 `new_candidate_path` 會無法保留使用者輸入的表單，解決方式：使用 `render`

2. 如果寫在前端的 js 當使用者關閉瀏覽器的 js 或是使用特殊方法發送請求時會無法驗證，如果寫在 Controller 裡面的話則是需要在每次都撰寫一次驗證，所以統一交給 Model 處理方便又簡單

3. N + 1 問題是指當有 10 比資料時需要撈 DB 11 次。
   比如說要列出所有 User 的購物紀錄，先從 User 資料表撈出所有 User 再跟據 User 去撈出所有的購物紀錄。
   在 Rails 中如果要解決可以使用 `includes()` 的語法
