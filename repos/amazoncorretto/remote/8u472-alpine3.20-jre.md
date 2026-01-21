## `amazoncorretto:8u472-alpine3.20-jre`

```console
$ docker pull amazoncorretto@sha256:f49aba7c92a0ff4adbc1f6c6182d11525c8bd8846bdef3a0fd8a4cb3b780048e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u472-alpine3.20-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:4ba92ff7b31b2a201835b57f4e4794a9402311355986323aa02c710dfe88afa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45362022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd1e3efc66958f794a633f131e3ea732b25c1c4b7696b01570d7d37777fa88c0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:10:03 GMT
ADD alpine-minirootfs-3.20.8-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:10:03 GMT
CMD ["/bin/sh"]
# Tue, 21 Oct 2025 20:48:19 GMT
ARG version=8.472.08.1
# Tue, 21 Oct 2025 20:48:19 GMT
# ARGS: version=8.472.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Tue, 21 Oct 2025 20:48:19 GMT
ENV LANG=C.UTF-8
# Tue, 21 Oct 2025 20:48:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:5311e7f182d02360a7194aa2995849bcdf04795c39a0ffdcf413eae625865970`  
		Last Modified: Sun, 07 Dec 2025 13:54:16 GMT  
		Size: 3.6 MB (3627056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec4512409e8eaa64492f2c1e22c2aabf8538d1e0004f787996d83f4237087089`  
		Last Modified: Sun, 21 Dec 2025 02:19:56 GMT  
		Size: 41.7 MB (41734966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u472-alpine3.20-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:bb4a575739cbc3d3a44732de96487f700888cc8c0692e9a6dfe039cf6cfb9929
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.5 KB (191517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81cf69af65bfd2a23159977157e81b0668666f2fa66a0cb35e43f4f5b8bf360d`

```dockerfile
```

-	Layers:
	-	`sha256:45e222b8fe397501424d54215dde570d4c16c6654e48d83730145886dd170e2c`  
		Last Modified: Tue, 21 Oct 2025 23:25:20 GMT  
		Size: 182.8 KB (182818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2312540fc143ecb1ca9639475badea07e690c01678e210bd6101810202435280`  
		Last Modified: Tue, 13 Jan 2026 07:32:32 GMT  
		Size: 8.7 KB (8699 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u472-alpine3.20-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:e7112fd8250ab88f9e502f91601c962cbb9ccde31f7ddbd23c56364e48205a37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45521990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2c061d2f7cf361915f1a2ea95a756b20cdf3b4b9018f811502ef30cd9f13bd6`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:10:03 GMT
ADD alpine-minirootfs-3.20.8-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:10:03 GMT
CMD ["/bin/sh"]
# Tue, 21 Oct 2025 20:48:19 GMT
ARG version=8.472.08.1
# Tue, 21 Oct 2025 20:48:19 GMT
# ARGS: version=8.472.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Tue, 21 Oct 2025 20:48:19 GMT
ENV LANG=C.UTF-8
# Tue, 21 Oct 2025 20:48:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:c765ae84869fd59a62821873e5413a3e92e36bdc1ced8fab3520334863720a49`  
		Last Modified: Wed, 08 Oct 2025 12:02:47 GMT  
		Size: 4.1 MB (4089377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b59428824c36cb2497c8af24c3d86ae921626b910a8376a1ed8cf61bc30f37ae`  
		Last Modified: Sun, 21 Dec 2025 12:54:32 GMT  
		Size: 41.4 MB (41432613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u472-alpine3.20-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:4fd0ee2d574f62373fb2ced9d2b1d6f3ceee0b8636b4a8a59d78682ae6a10702
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.7 KB (191705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39132c1dd92d89f0703e0e9a3996f7c9334a97124e26cf1a8d5737f0ab482023`

```dockerfile
```

-	Layers:
	-	`sha256:9eb2cbe62c2d36f7cdd77604465078d7924394c15daeec6618b7a7c6ffeb7afd`  
		Last Modified: Tue, 21 Oct 2025 21:49:04 GMT  
		Size: 182.9 KB (182926 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74dcb309b123260f57a819f03784c47aae1783b8508d694b0d0b4a26591518fb`  
		Last Modified: Tue, 21 Oct 2025 21:49:04 GMT  
		Size: 8.8 KB (8779 bytes)  
		MIME: application/vnd.in-toto+json
