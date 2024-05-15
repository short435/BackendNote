# Status Code




## Introudcion

## Type

- 1xx (Informational)：表示接收的請求正在處理。
- 2xx (Success)：表示請求正常處理完畢。
- 3xx (Redirection)：表示需要後續操作才能完成這一請求。
- 4xx (Client Error)：表示客戶端錯誤導致服務器無法處理請求。
- 5xx (Server Error)：表示服務器處理請求出現錯誤。

### 1xx 訊息響應
- 100 Continue：客戶端應繼續其請求

### 2xx 成功
- 200 OK：請求成功，且伺服器返回所請求的資源。
- 201 Created：請求成功且伺服器創建了新的資源。

### 3xx Redirection
- 301 Moved Permanently：


### 4xx Client Error
- 400 Bad Request：服務器無法理解客戶端的請求，由於語法無效。
- 401 Unauthorized：請求需要用戶的身份驗證。如果請求已經包括了授權憑證，則表示服務器認證這些憑證失敗。
- 404 Not Found：請求失敗，請求所希望得到的資源未被在服務器上發現。沒有信息能告訴用戶這個情況到底是暫時的還是永久的。


### 5xx Server Error
- 500 Internal Server Error：服務器遇到了一個未曾預料的狀況，導致其無法完成對請求的處理。一般來說，這個問題都會在服務器的錯誤日誌中留下紀錄。