## `amazoncorretto:8u482-alpine3.22`

```console
$ docker pull amazoncorretto@sha256:3eb984d1d3dab74b9dcd27f60ce00553ae34d3ed9d08a096756cd1ed89d5eb4d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u482-alpine3.22` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:83906a8351178b068a88e2299da94291ac497a9c0d3f12b0d0a0da14c3cf7fa6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.6 MB (104577359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee5c5299012bb9dcf11876a2eb0c7ee9a392b044638df8f6dec27e18fe01d381`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 21 Jan 2026 18:59:32 GMT
ARG version=8.482.08.1
# Wed, 21 Jan 2026 18:59:32 GMT
# ARGS: version=8.482.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 21 Jan 2026 18:59:32 GMT
ENV LANG=C.UTF-8
# Wed, 21 Jan 2026 18:59:32 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 21 Jan 2026 18:59:32 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Sun, 07 Dec 2025 13:53:31 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:717ea002bc7fdb17f68ace861a1e05086b366b98dd432124b50e20735b584078`  
		Last Modified: Wed, 21 Jan 2026 18:59:46 GMT  
		Size: 100.8 MB (100774907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u482-alpine3.22` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:75bbba6f9d23ac7b16f3f80b33364bcbd846cf24d5bf8726698a16ffe2dc3211
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.0 KB (257029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2086e931ee41eef29f90842e72e869ee7d7d6f80d3cda78be7946b724c79d759`

```dockerfile
```

-	Layers:
	-	`sha256:27804ebb2d35240ef7d00ff848d71c13adac3177d920ae7cd97554f8736d25c7`  
		Last Modified: Wed, 21 Jan 2026 19:56:09 GMT  
		Size: 247.7 KB (247674 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ce534e7b953c8f710764e7981e37fe080f3c2f9ab8d142591675a1ed8d1011c`  
		Last Modified: Wed, 21 Jan 2026 19:56:10 GMT  
		Size: 9.4 KB (9355 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u482-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:416bfccc23ad4d5dbfbe451903e492daa03488820389fe08b6267373037c8fc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.7 MB (104699220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18b9ea395f6cf971084e8dd851e0a0f7b27b26059fc7e2b3f5caeaa6e9d26a18`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 21 Jan 2026 18:59:39 GMT
ARG version=8.482.08.1
# Wed, 21 Jan 2026 18:59:39 GMT
# ARGS: version=8.482.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 21 Jan 2026 18:59:39 GMT
ENV LANG=C.UTF-8
# Wed, 21 Jan 2026 18:59:39 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 21 Jan 2026 18:59:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:11 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e139de12827dca78824165f354dcc2173b3b0cc2fbe0c68732e30942e998149`  
		Last Modified: Wed, 21 Jan 2026 20:53:36 GMT  
		Size: 100.6 MB (100561151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u482-alpine3.22` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:6707e99630a58f7a2ec7b17831f695ff9005dc4ecf7ed684f9387743c35b16d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.3 KB (257265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09280a079079a2f9ae601f7310fbc465f52730add8158bd471ffec24439ec7b5`

```dockerfile
```

-	Layers:
	-	`sha256:6f3184d61bcdb9e568cf40653b3c09d9f41a8e17cbb7999fbc50e19a669e9128`  
		Last Modified: Wed, 21 Jan 2026 18:59:50 GMT  
		Size: 247.8 KB (247806 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e5e38eb321e9372defc2b7494ef1d6d92870c7ec9487cd490445b495d9b2bf8`  
		Last Modified: Wed, 21 Jan 2026 19:56:20 GMT  
		Size: 9.5 KB (9459 bytes)  
		MIME: application/vnd.in-toto+json
