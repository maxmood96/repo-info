## `amazoncorretto:24-alpine3.20-jdk`

```console
$ docker pull amazoncorretto@sha256:2902591b50bd26dc6ff91a6bea3222439bd4a06ac2be75c79a5987034d661cad
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:24-alpine3.20-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:199b4114c32c46e726f84523e68c77e45369df90669654e6c2b58bf467f79cc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.4 MB (180391163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92b266f67d700074e6c1d4316da1c6a2a3a7294faf8f57632b834333f2d0bd7d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:31:35 GMT
ADD alpine-minirootfs-3.20.7-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:31:35 GMT
CMD ["/bin/sh"]
# Wed, 16 Jul 2025 19:33:24 GMT
ARG version=24.0.2.12.1
# Wed, 16 Jul 2025 19:33:24 GMT
# ARGS: version=24.0.2.12.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-24=$version-r0 &&     rm -rf /usr/lib/jvm/java-24-amazon-corretto/lib/src.zip # buildkit
# Wed, 16 Jul 2025 19:33:24 GMT
ENV LANG=C.UTF-8
# Wed, 16 Jul 2025 19:33:24 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 16 Jul 2025 19:33:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:01d036902a3ca86e8793073c8094cba44d83a38953a489ac0641f3de017fe2d2`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3620477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a132c25f58c5fba11883b48fca8a520856b027517440cfd33b187c00bd96acfa`  
		Last Modified: Wed, 16 Jul 2025 22:24:01 GMT  
		Size: 176.8 MB (176770686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:24-alpine3.20-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:5818890028cb38e7f14f08019c8a7b5ddc3efa8dcd0d42a480992f391e95db35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.5 KB (396485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cb5a86f57a26498fe8e6f09cd78a387acdef660be7e32a8d6e1c14044f99e71`

```dockerfile
```

-	Layers:
	-	`sha256:54bc35500af59363d3e9ab3dd726bfda9244f0f67ab4871ebe8528d6b7a4c774`  
		Last Modified: Wed, 16 Jul 2025 21:50:41 GMT  
		Size: 387.1 KB (387070 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac4786ffda1b2286c58787a37f9daccf632c295a5f95831fbe0832a34422ecb7`  
		Last Modified: Wed, 16 Jul 2025 21:50:42 GMT  
		Size: 9.4 KB (9415 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:24-alpine3.20-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:6ce473a59e4170f424a6748b3a2dd31da733f360c07c7faf5f918a9a7e032d0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.6 MB (178606396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c579d7bfc09f8cdfdbd1eb66d1510db9be078f5172607bcde450672f4619f6b5`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:31:35 GMT
ADD alpine-minirootfs-3.20.7-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:31:35 GMT
CMD ["/bin/sh"]
# Wed, 16 Jul 2025 19:33:24 GMT
ARG version=24.0.2.12.1
# Wed, 16 Jul 2025 19:33:24 GMT
# ARGS: version=24.0.2.12.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-24=$version-r0 &&     rm -rf /usr/lib/jvm/java-24-amazon-corretto/lib/src.zip # buildkit
# Wed, 16 Jul 2025 19:33:24 GMT
ENV LANG=C.UTF-8
# Wed, 16 Jul 2025 19:33:24 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 16 Jul 2025 19:33:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:13e713f825654e9e4f57146ec84918d478434f708d4d3d9d18d0e7ba2be56801`  
		Last Modified: Tue, 15 Jul 2025 19:00:10 GMT  
		Size: 4.1 MB (4088368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86dc9fe62a38003a1eb78893649b71e0706c2195386b263cb643e7ceb319ed36`  
		Last Modified: Thu, 17 Jul 2025 20:11:51 GMT  
		Size: 174.5 MB (174518028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:24-alpine3.20-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:19e3516ed7e04c74be18d765a1f03510a9521cb9220bdd48abf302086c2b506d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.0 KB (396005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:785b0febb98f1895bab116c9e321dff8a710297d7ac1d6dbb352eb7b24aed838`

```dockerfile
```

-	Layers:
	-	`sha256:9e6ccb1741bb08a8d4b3a16399185eb6ce000ccac6dec6a6c4aa8fa22c3178e1`  
		Last Modified: Thu, 17 Jul 2025 03:50:35 GMT  
		Size: 386.5 KB (386486 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a8604a1f8cc2a93c200cc2d843ab3872660fe60889abd8fc4f76621c72fc2e2`  
		Last Modified: Thu, 17 Jul 2025 03:50:36 GMT  
		Size: 9.5 KB (9519 bytes)  
		MIME: application/vnd.in-toto+json
