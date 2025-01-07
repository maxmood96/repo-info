## `amazoncorretto:23-alpine-jdk`

```console
$ docker pull amazoncorretto@sha256:41b2122d57e17486029368468308d39e8bdb1c567c8c31a19dee1b8935aab34f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:23-alpine-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:502904b518d1e08728ac1ba85de8e15caadf512edba0440006b104863df86467
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.3 MB (170272818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e45a794200b24c366e50a2fd6b97782b7ab9a1671cea81f98d00c190d38eaedc`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
ADD alpine-minirootfs-3.20.4-x86_64.tar.gz / # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 23:01:14 GMT
ARG version=23.0.1.8.1
# Fri, 13 Dec 2024 23:01:14 GMT
# ARGS: version=23.0.1.8.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-23=$version-r0 &&     rm -rf /usr/lib/jvm/java-23-amazon-corretto/lib/src.zip # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 23:01:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 13 Dec 2024 23:01:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:63b69af3dc5582ce6b63be03623e334ccd4e5cb4bde42702bbfc7a986a1bf432`  
		Last Modified: Tue, 07 Jan 2025 02:28:35 GMT  
		Size: 3.6 MB (3613999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94ad1e0bc1086a0d66015a8c5cb2b20b9b24a12d4c39311e4799c0d9b5940200`  
		Last Modified: Tue, 07 Jan 2025 03:31:12 GMT  
		Size: 166.7 MB (166658819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:23-alpine-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:48b31c296044bc9df85bed40c9cc9a1c4de6b15babf00e32786b1424d61cb495
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **390.5 KB (390532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50f73acff2e9b8b9b93cb58fb45516192ff75ec7cc5ff4adac23966100674e64`

```dockerfile
```

-	Layers:
	-	`sha256:05f7cc9ee9c3f2f8cbf9fa851aeae7b554b69659f48a5763b71452fc18c3c4fe`  
		Last Modified: Tue, 07 Jan 2025 03:31:10 GMT  
		Size: 379.8 KB (379813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:660d394f095be765305308e4c324fa632e2a8500a1cfe3a7ce12d21cd0ecca44`  
		Last Modified: Tue, 07 Jan 2025 03:31:10 GMT  
		Size: 10.7 KB (10719 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:23-alpine-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:fa493b893e361f55aa0d0c6e91481fd54d5c1b38338e4948583d313e2279dbba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.4 MB (168439982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5157a7c1d5b54faffe67fe0b26f319d054ec9605d371581ced2ccfd6be147f20`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=23.0.1.8.1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=23.0.1.8.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-23=$version-r0 &&     rm -rf /usr/lib/jvm/java-23-amazon-corretto/lib/src.zip # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 16 Oct 2024 02:18:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef1413bef328b2e591c8275ac22907ac0cec7bff979b30006b16e8a64026a130`  
		Last Modified: Wed, 13 Nov 2024 07:54:46 GMT  
		Size: 164.4 MB (164352256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:23-alpine-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:ab9ba1b53436e2cc5921b2001530e4bee15329c7dbd5c4833779f18d9af7532b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **390.1 KB (390137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cb54260ea1b34e617bced6fcd63d06524a4b38452fcbd60b13473fec15be611`

```dockerfile
```

-	Layers:
	-	`sha256:fc9479b61017acf02829141705a9465e1fb159c01b36ef141e10c9507d7be8b7`  
		Last Modified: Wed, 13 Nov 2024 07:54:42 GMT  
		Size: 379.3 KB (379265 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10f91a1c508498455801c403cb5136740168992a005faba92ee0044248888018`  
		Last Modified: Wed, 13 Nov 2024 07:54:42 GMT  
		Size: 10.9 KB (10872 bytes)  
		MIME: application/vnd.in-toto+json
