[index.html](https://github.com/user-attachments/files/22633573/index.html)
<!DOCTYPE html>
<html lang="fa">
<head>
  <meta charset="UTF-8">
  <title>نوتیفیکیشن محصولات جدید</title>
</head>
<body>
  <!-- OneSignal Push Notification Button (Fancy Version, B Titr Font, Full Text) -->
  <div style="text-align:center; margin:20px;">
    <button id="notifyBtn" 
            style="font-family: 'B Titr', sans-serif; background-color:#1A237E; color:white; padding:12px 25px; border:none; border-radius:8px; font-size:16px; cursor:pointer; transition: 0.3s;">
      دریافت نوتیفیکیشن محصولات جدید
    </button>
  </div>

  <!-- Hover Effect -->
  <style>
    #notifyBtn:hover {
      background-color: #303F9F; /* کمی روشن‌تر از سرمه‌ای */
    }
  </style>

  <!-- OneSignal Script -->
  <script src="https://cdn.onesignal.com/sdks/OneSignalSDK.js" async=""></script>
  <script>
    var OneSignal = window.OneSignal || [];
    OneSignal.push(function() {
      OneSignal.init({
        appId: "a227d600-82ce-474e-801f-8eeb7847b803",
      });
    });

    document.getElementById("notifyBtn").addEventListener("click", function() {
      OneSignal.push(function() {
        OneSignal.registerForPushNotifications();
      });
    });
  </script>
</body>
</html>
