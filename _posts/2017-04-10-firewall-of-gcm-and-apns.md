---
layout: post
title: "APNS, GCM 방화벽 설정"
categories: memo
author: "indexall"
meta: "apns gcm firewall"
---

### 도메인으로 설정
#### APNS
- gateway.push.apple.com 2195
- feedback.push.apple.com 2196

#### GCM
- android.googleapis.com 443,5228,5229,5230

### IP로 설정
도메인으로 설정이 되면 좋겠지만 간혹 IP로 방화벽을 설정해야 할 때가 있음. 그럴때는 아래 스펙문서 링크를 참고

#### APNS
- https://support.apple.com/ko-kr/HT203609
> APNS 서버에서는 로드 밸런싱을 사용하기 때문에 사용자의 기기에서 알림을 보낼 때 항상 같은 공용 IP 주소에 연결되지 않습니다. 사용 중인 기기가 Apple에 할당된 전체 17.0.0.0/8 주소 블록에서 이러한 포트에 접근하는 것을 허용하는 것이 가장 좋습니다.

#### GCM
- https://developers.google.com/cloud-messaging/http
> If your organization has a firewall that restricts the traffic to or from the Internet, you need to configure it to allow connectivity with GCM in order for your GCM client apps to receive messages. The ports to open are: 5228, 5229, and 5230. GCM typically only uses 5228, but it sometimes uses 5229 and 5230. GCM doesn’t provide specific IPs, so you should allow your firewall to accept outgoing connections to all IP addresses contained in the IP blocks listed in Google’s ASN of 15169. 

Google’s ASN of 15169 참고 link : https://ipinfo.io/AS15169