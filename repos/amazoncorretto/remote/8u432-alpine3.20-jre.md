## `amazoncorretto:8u432-alpine3.20-jre`

```console
$ docker pull amazoncorretto@sha256:00f86c215ae0d9a4f2ec67acd180101c200f55f877f408e30c5d88d02fad828c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u432-alpine3.20-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:9ddba547d843454e9838b8281a30503890e139fe98679c8e8f5ee8ce72263e6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.3 MB (45282863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52b133f2f7c2fda53e0cbdf7f5c91a23ff38f5c48b20bec8fc967f0ca6910884`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 23:01:14 GMT
ARG version=8.432.06.1
# Fri, 13 Dec 2024 23:01:14 GMT
# ARGS: version=8.432.06.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 23:01:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Wed, 08 Jan 2025 15:55:45 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b6e24abd82baadc2d15caebcc9e62612d96791128f05f9b569abbc2a22dbc2f`  
		Last Modified: Wed, 08 Jan 2025 18:09:58 GMT  
		Size: 41.7 MB (41656603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u432-alpine3.20-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:cb34eecaf4aec3180ab8af3ba5ec622e43912e032862c3ba5154e9a8eddb403a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.1 KB (191120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00d670eea7c669a022aa7f083db7c5ada97fec42d88a0a22a88a316aff29cd8d`

```dockerfile
```

-	Layers:
	-	`sha256:1527b4d22c79ffb4019b50c4328df6a90cf66f631033252513019ee0293edce0`  
		Last Modified: Wed, 08 Jan 2025 18:09:57 GMT  
		Size: 181.8 KB (181761 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4bddbf321971e2202b72e417e739c062fbf86da8ad178aac0ab5dd1ccc16a1a7`  
		Last Modified: Wed, 08 Jan 2025 18:09:56 GMT  
		Size: 9.4 KB (9359 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u432-alpine3.20-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:0fbeb4b9882ab3ddebadc23e23b6614492a613506dd8b2f733950ce8250b5cb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45444838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f84d7769b47723d929b9f4740dbcd5bf7a354c321ced1987cc1919eee4cabefe`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
ADD alpine-minirootfs-3.20.4-aarch64.tar.gz / # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 23:01:14 GMT
ARG version=8.432.06.1
# Fri, 13 Dec 2024 23:01:14 GMT
# ARGS: version=8.432.06.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 23:01:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:ef22e11fe7735044a1b56fc644666588aa863fb6abe827f676cb9d11ba34d993`  
		Last Modified: Tue, 07 Jan 2025 03:03:03 GMT  
		Size: 4.1 MB (4086686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb11b32f228dfe7054d12111ed17f86a606243e60b90fa23cd5e60f830417bce`  
		Last Modified: Tue, 07 Jan 2025 07:20:58 GMT  
		Size: 41.4 MB (41358152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u432-alpine3.20-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:6a72754cecd82a29743d9686aff6781036b1e7d189e5ad47d928625d56a335af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.4 KB (191355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:424b1929cc41c1877e3cc07ee5fd0be35041511506034758a22604b9e56f0869`

```dockerfile
```

-	Layers:
	-	`sha256:aa95375f2a611dd180cdfa394ed2c8c67624309ad228b62daa259a8daa549f30`  
		Last Modified: Tue, 07 Jan 2025 07:20:57 GMT  
		Size: 181.9 KB (181893 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:836e0c3d17591313eead4569eb23d30584397e02322f3d80bfe328b77077e17a`  
		Last Modified: Tue, 07 Jan 2025 07:20:57 GMT  
		Size: 9.5 KB (9462 bytes)  
		MIME: application/vnd.in-toto+json
