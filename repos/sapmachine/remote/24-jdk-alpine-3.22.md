## `sapmachine:24-jdk-alpine-3.22`

```console
$ docker pull sapmachine@sha256:8b65631e341d4a2b22828b301db19a8234084440b3cd43aa38f03f36173c0b39
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:24-jdk-alpine-3.22` - linux; amd64

```console
$ docker pull sapmachine@sha256:7dfff90f812a2cd44500f24b130888b1c0daebc460314929138bcffcc6a0ed6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.9 MB (236908168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91600070239e9891e727e78b73452586dc704be7964e7f7bff4f4a29f9478a69`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 04 Jul 2025 15:51:13 GMT
RUN wget -qO /etc/apk/keys/sapmachine-apk.rsa.pub https://dist.sapmachine.io/alpine/sapmachine-apk.rsa.pub &&     echo "4444e47cabf35695f9406692848de191d3b7cbd47dcdc1ffb62f4f70aea06e89 /etc/apk/keys/sapmachine-apk.rsa.pub" | sha256sum -c - &&     echo "https://dist.sapmachine.io/alpine" >> /etc/apk/repositories &&     apk add sapmachine-24-jdk=24.0.1-r0 # buildkit
# Fri, 04 Jul 2025 15:51:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-24-sapmachine-jdk
# Fri, 04 Jul 2025 15:51:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25c076a95d64db3fb32e83d7c7f08ea73173ed6598739dc49d5005ee84e4c6ce`  
		Last Modified: Mon, 07 Jul 2025 20:45:56 GMT  
		Size: 233.1 MB (233111322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:24-jdk-alpine-3.22` - unknown; unknown

```console
$ docker pull sapmachine@sha256:6cbf250a529f896f1efa3328eb2f811fad64ec55b3f6761ca00ac37916c4ddab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **515.7 KB (515685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d28cf3cc6305e52ae71f013d767cf3b95a7ad64fe563c510ed87a85db5ac4a72`

```dockerfile
```

-	Layers:
	-	`sha256:ff6431e9ba61bb3584402ef17606bc13b9680c1227c93195c5c736eed3a724c6`  
		Last Modified: Mon, 07 Jul 2025 21:06:41 GMT  
		Size: 505.5 KB (505488 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34a82df2e93cd96b4871e59c917a8d6f27a9d471fd899ba550c71a9f884c4d60`  
		Last Modified: Mon, 07 Jul 2025 21:06:42 GMT  
		Size: 10.2 KB (10197 bytes)  
		MIME: application/vnd.in-toto+json
