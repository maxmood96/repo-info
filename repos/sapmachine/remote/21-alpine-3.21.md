## `sapmachine:21-alpine-3.21`

```console
$ docker pull sapmachine@sha256:8ca2e2cf35efc8937f50f2470a9ca973acf3578fa41ccb124f08ffa57655cd94
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:21-alpine-3.21` - linux; amd64

```console
$ docker pull sapmachine@sha256:e78384d34c8a999b7d282ba3b18948988ff574acd6a0ddc92be78f62f92eebd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.8 MB (219797927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc5d5a18df28af5f918275226f2e74b2ae726ff7d19d90e143ca1b9c127fa32a`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Mon, 11 Aug 2025 06:09:32 GMT
RUN wget -qO /etc/apk/keys/sapmachine-apk.rsa.pub https://dist.sapmachine.io/alpine/sapmachine-apk.rsa.pub &&     echo "4444e47cabf35695f9406692848de191d3b7cbd47dcdc1ffb62f4f70aea06e89 /etc/apk/keys/sapmachine-apk.rsa.pub" | sha256sum -c - &&     echo "https://dist.sapmachine.io/alpine" >> /etc/apk/repositories &&     apk add nss sapmachine-21-jdk=21.0.8-r0 # buildkit
# Mon, 11 Aug 2025 06:09:32 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-sapmachine-jdk
# Mon, 11 Aug 2025 06:09:32 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0368fd46e3c6d237d81390ff086f93aee216df5cfa814041a491453fb0932a12`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3637570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f856ad3a6c1b78a04458c82a0a282d2227a9f2b3544b8f56513c7bc369a2185`  
		Last Modified: Wed, 17 Sep 2025 17:39:47 GMT  
		Size: 216.2 MB (216160357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-alpine-3.21` - unknown; unknown

```console
$ docker pull sapmachine@sha256:5f9f2a6e39d2cc5d5cc732c36edc50b445bf4c9e39504216e8a428c2c2f11ee1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **519.2 KB (519248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:945dc8c1fcfb4ab361c06b2dd9aab75045c356661e90dfe631f5fd41c05501e8`

```dockerfile
```

-	Layers:
	-	`sha256:ecf2bb4241867661cf8986011fe172639eee753953aec201fbef5910b784d999`  
		Last Modified: Wed, 17 Sep 2025 21:07:49 GMT  
		Size: 511.6 KB (511579 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a429e0f9c5b5292593e59c188e0068a2d91c32faa22ac326eb2665e7d9b98c3d`  
		Last Modified: Wed, 17 Sep 2025 21:07:50 GMT  
		Size: 7.7 KB (7669 bytes)  
		MIME: application/vnd.in-toto+json
