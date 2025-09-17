## `sapmachine:17-alpine-3.21`

```console
$ docker pull sapmachine@sha256:0eb9f8eea513961a837b284d36357964e623eddff8995021e23b71a503b6854f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:17-alpine-3.21` - linux; amd64

```console
$ docker pull sapmachine@sha256:be804494ef6a3c49e9d1008f7b4599647aab0d899a0ba59562165308ac2baca8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.6 MB (204578407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d3b9102f037cc96923500d9d8dcb7e7001c9c01a00567894719382c7d9d1467`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Mon, 11 Aug 2025 06:09:35 GMT
RUN wget -qO /etc/apk/keys/sapmachine-apk.rsa.pub https://dist.sapmachine.io/alpine/sapmachine-apk.rsa.pub &&     echo "4444e47cabf35695f9406692848de191d3b7cbd47dcdc1ffb62f4f70aea06e89 /etc/apk/keys/sapmachine-apk.rsa.pub" | sha256sum -c - &&     echo "https://dist.sapmachine.io/alpine" >> /etc/apk/repositories &&     apk add nss sapmachine-17-jdk=17.0.16-r0 # buildkit
# Mon, 11 Aug 2025 06:09:35 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-sapmachine-jdk
# Mon, 11 Aug 2025 06:09:35 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0368fd46e3c6d237d81390ff086f93aee216df5cfa814041a491453fb0932a12`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3637570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:663a634459f33d3594308a00f37e9225982a8368033190dbdb22f387413430e8`  
		Last Modified: Wed, 17 Sep 2025 17:41:32 GMT  
		Size: 200.9 MB (200940837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-alpine-3.21` - unknown; unknown

```console
$ docker pull sapmachine@sha256:afae22323f27464a6e5ff051d20d6bd90b576998309db55e4bf02c5484884516
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **517.4 KB (517363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26db50a1f1c986eb2184e7e1b856e00beea59cd489966035040c568b61d9589d`

```dockerfile
```

-	Layers:
	-	`sha256:72c5732ec9b177e614eb12dc7477895ac9162ef913e052b843e179536c44437f`  
		Last Modified: Wed, 17 Sep 2025 21:05:24 GMT  
		Size: 509.7 KB (509689 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2108724a5f4e57cdaa6d510ba06f7badce2d19dce4ef664b32349363b9f208c4`  
		Last Modified: Wed, 17 Sep 2025 21:05:25 GMT  
		Size: 7.7 KB (7674 bytes)  
		MIME: application/vnd.in-toto+json
