## `sapmachine:alpine-3.23`

```console
$ docker pull sapmachine@sha256:cccd9e9dbb5aed5f2fb580dfb868d41d0f2be93e564d5905f857e9dd42d8322e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:alpine-3.23` - linux; amd64

```console
$ docker pull sapmachine@sha256:0641dd38cb08c749c0977d8ea853f2216831c73395ac6f6269c44908e8620649
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.1 MB (232064506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d3b8e2039225223d018442d608675f91bf952a57320d3ea441193608c66d157`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Tue, 21 Apr 2026 23:02:30 GMT
RUN wget -qO /etc/apk/keys/sapmachine-apk.rsa.pub https://dist.sapmachine.io/alpine/sapmachine-apk.rsa.pub &&     echo "4444e47cabf35695f9406692848de191d3b7cbd47dcdc1ffb62f4f70aea06e89 /etc/apk/keys/sapmachine-apk.rsa.pub" | sha256sum -c - &&     echo "https://dist.sapmachine.io/alpine" >> /etc/apk/repositories &&     apk add sapmachine-26-jdk=26.0.1-r0 # buildkit
# Tue, 21 Apr 2026 23:02:30 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-26-sapmachine-jdk
# Tue, 21 Apr 2026 23:02:30 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ebc6ec15df582ae6133ed2d03dbe200dd4d18719af81f46a88ef434dac79f1`  
		Last Modified: Tue, 21 Apr 2026 23:02:53 GMT  
		Size: 228.2 MB (228200317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:alpine-3.23` - unknown; unknown

```console
$ docker pull sapmachine@sha256:9e9e7a989be21b384b9279db94f4280229cd1b24565fa9808b1207b7a57829de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **512.0 KB (512042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28f21a22bb71841316cd1cdae27709e3ceb038c9b3dc554d0559ef18b388af36`

```dockerfile
```

-	Layers:
	-	`sha256:9fca500e0133d5db2df6a65fd63b23e92226e7d6e8b4f8a56bdb535b20244bc4`  
		Last Modified: Tue, 21 Apr 2026 23:02:47 GMT  
		Size: 501.9 KB (501888 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:695f657a70b3f8600094f1d1fe4dbe812c624e3625566bfb2cc7b4ba370fe9ae`  
		Last Modified: Tue, 21 Apr 2026 23:02:47 GMT  
		Size: 10.2 KB (10154 bytes)  
		MIME: application/vnd.in-toto+json
