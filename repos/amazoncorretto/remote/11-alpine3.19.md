## `amazoncorretto:11-alpine3.19`

```console
$ docker pull amazoncorretto@sha256:ad23a5b855435280d38953458a3311d02b25d36ef04bf32c012e47c063428e9e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-alpine3.19` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:f8aad5c408aa8a19d738668c9ce16a4c99e35d0d5b599bf3558ea80e85d7857d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.3 MB (145323428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:306e0d9049d4f96525a136931ba8861923defdf960324daaeece803cb61d4b78`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
ADD alpine-minirootfs-3.19.5-x86_64.tar.gz / # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 23:01:14 GMT
ARG version=11.0.25.9.1
# Fri, 13 Dec 2024 23:01:14 GMT
# ARGS: version=11.0.25.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 23:01:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 13 Dec 2024 23:01:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:eb002c13a70b63d5677b5a03f11b7b8b60f7d62f296fbb7475169a617500d3cb`  
		Last Modified: Tue, 07 Jan 2025 02:28:43 GMT  
		Size: 3.4 MB (3413271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb24def776b0b83eea781a9f5fd19beff4c8c741703f9e9b72c660b844b4d479`  
		Last Modified: Tue, 07 Jan 2025 03:29:23 GMT  
		Size: 141.9 MB (141910157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.19` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:9ff6c6189df108df9d95124e36e441cd4976ff885d532dd2019d918137eea116
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **397.1 KB (397109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:154b6b5f275038421b3048552e62b1dbbcfbfc49caa59b55c425fc695d0b2508`

```dockerfile
```

-	Layers:
	-	`sha256:ef8d8813f2197f1f53dd10eb7b1776e0e501be28a5c0fb41b8550f2bf9a7f1dd`  
		Last Modified: Tue, 07 Jan 2025 03:29:21 GMT  
		Size: 387.7 KB (387693 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1ae66a1709bd8be6fa85b6fae625d902fce349de7fb59a068a854e10c77529f`  
		Last Modified: Tue, 07 Jan 2025 03:29:21 GMT  
		Size: 9.4 KB (9416 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:98886f91e201472356084910aa883868b84ec0a8f4be63613134ade25b60b22c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.4 MB (143390457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac9bbcb8b355ab4ade3b4b4eac65315cf200ba5e2e678e1b3436cad1e7553743`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=11.0.25.9.1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=11.0.25.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 16 Oct 2024 02:18:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:6c9d4d66fb4987fcd48c673e8b29bb504a3cfb33f10b97cbcea126aa3b8b59fd`  
		Last Modified: Mon, 09 Sep 2024 07:03:21 GMT  
		Size: 3.4 MB (3359246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2da3eda2dd8abdaef10b65d8a6edd96bffb48dd5d1f5532205bf1a801c742f57`  
		Last Modified: Tue, 12 Nov 2024 11:07:38 GMT  
		Size: 140.0 MB (140031211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.19` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:61644ff456a40f78bd7786733656ad3cbda607071ad99189bafacd7b59cc83ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **397.9 KB (397907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e117cb784d19041a0cc1c31166a5790fbe7d4d41f305e8cd963c72c9fc422052`

```dockerfile
```

-	Layers:
	-	`sha256:fd2ac91041256620677726cd526fad17ef1a32722fab8cbd89420a19ed20e90d`  
		Last Modified: Tue, 12 Nov 2024 11:07:35 GMT  
		Size: 388.4 KB (388386 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f43e284ecb72d0d8aa2958a68487adffdf36a67874d886d7a4ae8a11b7474021`  
		Last Modified: Tue, 12 Nov 2024 11:07:34 GMT  
		Size: 9.5 KB (9521 bytes)  
		MIME: application/vnd.in-toto+json
