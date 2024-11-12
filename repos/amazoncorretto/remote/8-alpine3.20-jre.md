## `amazoncorretto:8-alpine3.20-jre`

```console
$ docker pull amazoncorretto@sha256:e3bcf835fb6ab5e51ab2fdc2df8f7c3b178551f46d404c59b5a9fe8947f26e7c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-alpine3.20-jre` - linux; amd64

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

### `amazoncorretto:8-alpine3.20-jre` - unknown; unknown

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

### `amazoncorretto:8-alpine3.20-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:bc5cd20ad91e6af32503dd301ae6c2c63e2384d60919fa845378dc2cc6450021
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45445872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fdf85141bde86d0d47f78c752bf7129ab06472a8461dd91961ab2f3341b4a14`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
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
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84d21706bd8ec37e9bf81ab2bce32aabc59e2bef2883f768c342b5916c856c6d`  
		Last Modified: Wed, 16 Oct 2024 18:10:54 GMT  
		Size: 41.4 MB (41358226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.20-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:fb7b17d9e7d4b79a28afefde3bd6a288f9bbc4be3b2cfa7babce22a55f98d024
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.2 KB (191238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81d7cdd601c568ca3b24bd8fd7a2c9b015ca00145c43763eafacd1f4feb6a3f4`

```dockerfile
```

-	Layers:
	-	`sha256:c5993914b28afbe14c0341136fd02466a018b7db6c01b61b755d5b7f20a69f78`  
		Last Modified: Wed, 16 Oct 2024 18:10:53 GMT  
		Size: 182.0 KB (181988 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3963b89a8cdf51dc4734b311fde7b833d399f0871fcf2775c7b3ec4d7317858d`  
		Last Modified: Wed, 16 Oct 2024 18:10:53 GMT  
		Size: 9.2 KB (9250 bytes)  
		MIME: application/vnd.in-toto+json
