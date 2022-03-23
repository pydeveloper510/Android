# Android (JAVA)
android work
1. TextView
2. Button
3. EditText
4. Intent
5. Viewbinding (setting in gradle file)
6. ListView
7. Webview
8. RecycleView
9. Fragment
10. Log & comment
11. Thread & Handler
12. Get Macaddress and IpAddress phone number
```
public static String getLocalMacAddress() {
        String result = "";
        InetAddress ip;

        try {
            ip = InetAddress.getLocalHost();

            NetworkInterface network = NetworkInterface.getByInetAddress(ip);
            Log.e("아이피 확인1 : ", String.valueOf(network));

            byte[] mac = network.getHardwareAddress();

            String ipValue = ip.getHostAddress();
//            System.out.println("아이피 확인 : " + ipValue);
            Log.e("아이피 확인2 : ", ipValue);

            String ipValue2 = ip.getHostName();
//            System.out.println("아이피 확인 : " + ipValue2);
            Log.e("아이피 확인3 : ", ipValue2);



            StringBuilder sb = new StringBuilder();
            for (int i = 0; i < mac.length; i++) {
                sb.append(String.format("%02X%s", mac[i], (i < mac.length - 1) ? "-" : ""));
            }
            result = sb.toString();
            Log.e("Mac 주소: ", result);
        } catch (UnknownHostException e) {
            e.printStackTrace();
        } catch (SocketException e){
            e.printStackTrace();
        }

        return result;
    }
```
# adb restart 
android sdk>platform-tools>

adb kill-server

press enter

and again

adb start-server

press enter

# get sha1 key on android studio
Easiest way for getting SHA1 Key in android studio both (Debug and release Mode)

1.Open Android Studio
2.Open Your Project
3.Click on Gradle (From Right Side Panel, you will see Gradle Bar)
4.Click on Refresh (Click on Refresh from Gradle Bar , you will see List Gradle scripts of your Project)
5.Click on Your Project (Your Project Name form List)
6.Click on Tasks/Android
7.Double Click on signingReport (You will get SHA1 and MD5 in Run Bar)


