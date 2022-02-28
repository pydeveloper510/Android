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
12 .Get Macaddress and IpAddress phone number
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
