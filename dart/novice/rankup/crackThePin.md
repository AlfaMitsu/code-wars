Crack the PIN

    import 'dart:convert';
    import 'package:crypto/crypto.dart';
    
    String crack(String hash) {
      for (int pin = 0; pin < 100000; pin++) {
        String pinStr = pin.toString().padLeft(5, '0');
        String pinHash = md5.convert(utf8.encode(pinStr)).toString();
        if (pinHash == hash) {
          return pinStr;
        }
      }
      return "PIN not found";
    }
