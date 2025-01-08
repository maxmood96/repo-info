## `amazoncorretto:23-alpine3.20-full`

```console
$ docker pull amazoncorretto@sha256:7d4affc68ccf4c2c788ad47904a11c7668ccaddc111980acdf40fb6f6c9fe485
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:23-alpine3.20-full` - linux; amd64

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

### `amazoncorretto:23-alpine3.20-full` - unknown; unknown

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

### `amazoncorretto:23-alpine3.20-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:a2f2cb8ce072f5ae6209c80c235147901951b68f44dffe9820ba3909951a7c37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.4 MB (168438960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ced379e72d52128b9a1a43ef27411034770835213aa2c6ef92e0ab7754ef9007`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
ADD alpine-minirootfs-3.20.4-aarch64.tar.gz / # buildkit
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
	-	`sha256:ef22e11fe7735044a1b56fc644666588aa863fb6abe827f676cb9d11ba34d993`  
		Last Modified: Tue, 07 Jan 2025 03:03:03 GMT  
		Size: 4.1 MB (4086686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70544c0c4b6a989283661f627440b537a03757649de4e8a27fe4683dae274906`  
		Last Modified: Tue, 07 Jan 2025 07:26:56 GMT  
		Size: 164.4 MB (164352274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:23-alpine3.20-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:95d2b7a28044388b4ea04d9721ccc31e558864ad532a0c82a228c477fa21b678
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.5 KB (389512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f59ec80ad00c90d37995ba2b697c33dd648d10802519dc1125488d28a2c97bc`

```dockerfile
```

-	Layers:
	-	`sha256:ef0e71f0a6cb94ba798a6cb139322ec46aac4141bd6f2d0bc774415bd78be004`  
		Last Modified: Tue, 07 Jan 2025 07:26:52 GMT  
		Size: 378.6 KB (378640 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65e7407e303ea1f0e46c47f14738fd9ac9bf16a272f64f5af192f96d6fe806e4`  
		Last Modified: Tue, 07 Jan 2025 07:26:52 GMT  
		Size: 10.9 KB (10872 bytes)  
		MIME: application/vnd.in-toto+json
