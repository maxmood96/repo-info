## `amazoncorretto:8-alpine3.21-jdk`

```console
$ docker pull amazoncorretto@sha256:a696730db8e080253c7edafcc5f8c0414b5a0f90ad42f2a8935a968021a5f3b1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-alpine3.21-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:4abb80a44ec9e01c4d90e323661631d03b5c966604cce9826822f122a744b980
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.9 MB (103932960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82fdea60968bda7c0fc9363dcc2e0c3f82c0cc6402b805c5e6d3d4dfaa711d3c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Wed, 16 Jul 2025 19:33:24 GMT
ARG version=8.462.08.1
# Wed, 16 Jul 2025 19:33:24 GMT
# ARGS: version=8.462.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 16 Jul 2025 19:33:24 GMT
ENV LANG=C.UTF-8
# Wed, 16 Jul 2025 19:33:24 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 16 Jul 2025 19:33:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:0368fd46e3c6d237d81390ff086f93aee216df5cfa814041a491453fb0932a12`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3637570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff437e9f8d40b5789d591ce279a2d11438ad5828dd8c4d6dfb806d8be1f7c47f`  
		Last Modified: Wed, 16 Jul 2025 20:24:54 GMT  
		Size: 100.3 MB (100295390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.21-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:67b85620ed49b7a19471b63cd87f52e7f2f752d5970dfeb5181f25f3f3a985db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.9 KB (260892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dc18231cc83f7bca8e0b5f2b00792e33e524dd48b0f710af90ea2c768bcf9c9`

```dockerfile
```

-	Layers:
	-	`sha256:6e8f80143de9c05f01450cc08580b03f3e98102afa92647933f2395dda1d71c9`  
		Last Modified: Wed, 16 Jul 2025 21:51:22 GMT  
		Size: 250.2 KB (250196 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:667d21ab46721116e9bb60e6ec597501d03f264f9bcfc74d7de17ebfec622b3c`  
		Last Modified: Wed, 16 Jul 2025 21:51:22 GMT  
		Size: 10.7 KB (10696 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-alpine3.21-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:3433557c8104fbc1a17b04411d0f93a34297199113567cb3fd744cf9de7655f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.1 MB (104079077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53538b9c5ac3167cb0b6a619e545c7eafff817048e599dee3034481d561797f6`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Wed, 16 Jul 2025 19:33:24 GMT
ARG version=8.462.08.1
# Wed, 16 Jul 2025 19:33:24 GMT
# ARGS: version=8.462.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 16 Jul 2025 19:33:24 GMT
ENV LANG=C.UTF-8
# Wed, 16 Jul 2025 19:33:24 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 16 Jul 2025 19:33:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:d06c6b665c9b4c183a2e300b290a6b4b7db03f803122fe93d91e9178f425e488`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 4.0 MB (3986937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:171b7da45a838cb217cd89de9b17378196859b9c49fa77921a751c5ccf1e102b`  
		Last Modified: Thu, 17 Jul 2025 01:48:11 GMT  
		Size: 100.1 MB (100092140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.21-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:6df9d8f17cc6e4cc5450b7cae688873328dad4907d7841c35c52bd0b66f8a0a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.2 KB (261224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3111f6e888d848cc35a071c26bd811c3f5fa24e662d54233e5071da38d2c1845`

```dockerfile
```

-	Layers:
	-	`sha256:b30abe63ee3cb680c4a322899cc6a0456780764c252b332580b05aa8c27ffff6`  
		Last Modified: Thu, 17 Jul 2025 03:51:15 GMT  
		Size: 250.4 KB (250376 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c9babf8f218f81b37a2fce9fa4ea14368075ee3af0c3d5eb00968f70d1f50ac`  
		Last Modified: Thu, 17 Jul 2025 03:51:15 GMT  
		Size: 10.8 KB (10848 bytes)  
		MIME: application/vnd.in-toto+json
