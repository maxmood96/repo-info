## `sapmachine:25-alpine-3.21`

```console
$ docker pull sapmachine@sha256:72bf5ecee3b788ca5c96171d6e38b6ab17bd292710abd3c3ded6cffc1c1d3377
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:25-alpine-3.21` - linux; amd64

```console
$ docker pull sapmachine@sha256:17f01d0daf40630e16032634748ad33dfbd9a3d3bc7d5479d7430e429498be99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.3 MB (238334082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c3714a29c422fbe08b74bd89b4b203ac88e81311a95a7ab94a5147168813f2b`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Wed, 17 Sep 2025 04:28:56 GMT
RUN wget -qO /etc/apk/keys/sapmachine-apk.rsa.pub https://dist.sapmachine.io/alpine/sapmachine-apk.rsa.pub &&     echo "4444e47cabf35695f9406692848de191d3b7cbd47dcdc1ffb62f4f70aea06e89 /etc/apk/keys/sapmachine-apk.rsa.pub" | sha256sum -c - &&     echo "https://dist.sapmachine.io/alpine" >> /etc/apk/repositories &&     apk add sapmachine-25-jdk=25-r0 # buildkit
# Wed, 17 Sep 2025 04:28:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-sapmachine-jdk
# Wed, 17 Sep 2025 04:28:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0368fd46e3c6d237d81390ff086f93aee216df5cfa814041a491453fb0932a12`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3637570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4cd9f550d0336ba72d157b6a02ce46b05cdbd62ce8abcc6042eff006dca9fe0`  
		Last Modified: Wed, 17 Sep 2025 17:37:26 GMT  
		Size: 234.7 MB (234696512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:25-alpine-3.21` - unknown; unknown

```console
$ docker pull sapmachine@sha256:9f319f4317967547c81fba19eadd7145fa933629120393b56056b017682d8ec7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **511.1 KB (511067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dcefae7a3724237db322129a28864ed1af9282eb40a6afa73c4420a84949f9e`

```dockerfile
```

-	Layers:
	-	`sha256:af30917e3d09517bb82531885e109688d460bf876177007a5033385d5b6fe851`  
		Last Modified: Wed, 17 Sep 2025 21:10:21 GMT  
		Size: 502.8 KB (502792 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db2f3186c3685de752c89f4a1ad9347d75328b366f8b627aaa2430fdccfeeab5`  
		Last Modified: Wed, 17 Sep 2025 21:10:22 GMT  
		Size: 8.3 KB (8275 bytes)  
		MIME: application/vnd.in-toto+json
