## `amazoncorretto:8u432-alpine-jre`

```console
$ docker pull amazoncorretto@sha256:39beeb7219ae755ec04107f01a288dad171458442b29cc903847a16c69741f48
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u432-alpine-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:54576276ae9fb8f5d86bbd3276157575c0d39affb133de2758192d36ae4f4af2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.3 MB (45280555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41694c7d3b1be508d78965f57ec8c2103fa8d8026c160a0b19af648485818f0c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=8.432.06.1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=8.432.06.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74aab8c00f2e6d68d1b07c353d1836dc51637418b77743173e6a391456ed4fb0`  
		Last Modified: Tue, 12 Nov 2024 02:11:56 GMT  
		Size: 41.7 MB (41656651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u432-alpine-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:3b8b7a0245b5c47d7bd0941166b11811f3c690c22999421f3ac251d5f8c7223b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.3 KB (191308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fefeb8c68dc5c4233535b0af7d0c3ab7303344a6a4563a6a07fc6b3e21dadf7`

```dockerfile
```

-	Layers:
	-	`sha256:759e745273d8e0a1fc421164f6d9db08bf49e48690d305d0e3bc4e8e038d4912`  
		Last Modified: Tue, 12 Nov 2024 02:11:55 GMT  
		Size: 181.9 KB (181949 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d514cb713473bfa5b73940e083519cfa977586c7d1432d44abd00359fb867f30`  
		Last Modified: Tue, 12 Nov 2024 02:11:55 GMT  
		Size: 9.4 KB (9359 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u432-alpine-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:fd033301f2b5203b4a3aa39ca3295b5f57203305a48bafd7aa575c502c2ec93f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45445768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e897325fd0d0639d090f158409810d743dbdfe75f51353423278e4199ae77f4f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=8.432.06.1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=8.432.06.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:714344b1e7aaa55a474e4cd0c0218363021b0c689041dc73be8432bc4600f3a3`  
		Last Modified: Tue, 12 Nov 2024 11:05:53 GMT  
		Size: 41.4 MB (41358042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u432-alpine-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:e8b72c7fd43d1122313aeaa8e6ef45e86654bb88957a45f15d1613530f88dd96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.5 KB (191543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6a72f30b49fa0f1843cddb79fa8e0d8ab46a87ceccc6a87ea20d31d996458c2`

```dockerfile
```

-	Layers:
	-	`sha256:b02ae8038e9cf782d0f63973d6c43a62d50707a7c7e74ef8b2f1d22fecb57675`  
		Last Modified: Tue, 12 Nov 2024 11:05:52 GMT  
		Size: 182.1 KB (182081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25f6f17be0df98960ec5ae9ac7484090e977c230f221737d44391e2f0f1c98d0`  
		Last Modified: Tue, 12 Nov 2024 11:05:52 GMT  
		Size: 9.5 KB (9462 bytes)  
		MIME: application/vnd.in-toto+json
