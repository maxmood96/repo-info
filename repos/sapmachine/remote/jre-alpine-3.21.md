## `sapmachine:jre-alpine-3.21`

```console
$ docker pull sapmachine@sha256:268cc0293abfc3483f1a23db27ebefcda9ee2427c1d1faa8e2f2ee6421ee5b52
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:jre-alpine-3.21` - linux; amd64

```console
$ docker pull sapmachine@sha256:8a4b4e5706dd7c060e69af5c97b27b949ad2e34d0a7213738b8db6d89759321e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.6 MB (72643282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:686bdc50115f59babae50c7e828797726916e5d57265b3c31f9dd19e2e260dc5`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Wed, 17 Sep 2025 04:28:56 GMT
RUN wget -qO /etc/apk/keys/sapmachine-apk.rsa.pub https://dist.sapmachine.io/alpine/sapmachine-apk.rsa.pub &&     echo "4444e47cabf35695f9406692848de191d3b7cbd47dcdc1ffb62f4f70aea06e89 /etc/apk/keys/sapmachine-apk.rsa.pub" | sha256sum -c - &&     echo "https://dist.sapmachine.io/alpine" >> /etc/apk/repositories &&     apk add sapmachine-25-jre=25-r0 # buildkit
# Wed, 17 Sep 2025 04:28:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-sapmachine-jre
# Wed, 17 Sep 2025 04:28:56 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:0368fd46e3c6d237d81390ff086f93aee216df5cfa814041a491453fb0932a12`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3637570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afcbbaca664060cb0925ce29dee8eba8cbab70cfec1b447c3e1955860db32967`  
		Last Modified: Wed, 17 Sep 2025 17:37:51 GMT  
		Size: 69.0 MB (69005712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-alpine-3.21` - unknown; unknown

```console
$ docker pull sapmachine@sha256:5f95153106828697f0f9e068dfe1bebf3eff6f8d12e0b8065fb6ce026301f658
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **437.8 KB (437830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2f6353db4197ff40f971857eda784c6cd0ffdacd8a1e8bf34efc5068d3a33ec`

```dockerfile
```

-	Layers:
	-	`sha256:723bbee434f8ccbdce9a6bc5e93df6d44ac586a233a654ea94de8675b0074a65`  
		Last Modified: Wed, 17 Sep 2025 21:11:33 GMT  
		Size: 430.5 KB (430520 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1cee29318b891871d066a3cd325ef89a4bae3e3515262f4e7ceec4a030e1e323`  
		Last Modified: Wed, 17 Sep 2025 21:11:34 GMT  
		Size: 7.3 KB (7310 bytes)  
		MIME: application/vnd.in-toto+json
