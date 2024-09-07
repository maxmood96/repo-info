## `amazoncorretto:11-alpine-jdk`

```console
$ docker pull amazoncorretto@sha256:febe651d752fcdb38347e1bd0531005b9f166fce3738e37368de94e60bb18f0b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-alpine-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:de839c45ea701ab29756831adc5b26b1942d18309d868a8e571914a510c5e0f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.4 MB (145433277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38cff08b235c240e61d2eb9ced9a689f4058601cfee9e7c3c1ff7f072721444c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/sh"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=11.0.24.8.1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=11.0.24.8.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 16 Jul 2024 22:56:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec99fb94b338a07553936ce87876960f5b902aab07a49c4fd285815962a554d2`  
		Last Modified: Fri, 06 Sep 2024 23:17:36 GMT  
		Size: 141.8 MB (141809470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:32fe8bbe80d2698c0a84a6b8795f875ab152f10326dfd50d60e201ef335d958b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **395.8 KB (395777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ef68bf3c618c33c1b124e013e3009b0477be736350a730776a334882a179da0`

```dockerfile
```

-	Layers:
	-	`sha256:04a4cb118b1045973c2f65dca2ca041867bdaad06d6bc766a7d51770762ac517`  
		Last Modified: Fri, 06 Sep 2024 23:17:34 GMT  
		Size: 385.3 KB (385297 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7998a6fd2eb58a8bb256f4503011a3a6f2f14677065e12a52227f07a8c974c17`  
		Last Modified: Fri, 06 Sep 2024 23:17:34 GMT  
		Size: 10.5 KB (10480 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-alpine-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:f034e0373f4794367f6a122732866204a4cd4f417056f93050fd4b2c0b15f0b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.0 MB (144046665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8443866afadc2eadc3b930e9ed1c500238aa4adc097e43be4ab59f0305ec8188`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/sh"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=11.0.24.8.1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=11.0.24.8.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 16 Jul 2024 22:56:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f61e4d063d408aaa3bd545c1353b34fc7e9cf477360f91a0948870c1712e9f16`  
		Last Modified: Wed, 24 Jul 2024 10:41:50 GMT  
		Size: 140.0 MB (139959731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:1df7349a9f3be91b0eb2a97fda4f240b25a6a45aeb8b50927209123ab7cf494c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.2 KB (396227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83d311134f8f7b55657f8db5272d2f703005fcfaf60bb3e2b908cd5730316122`

```dockerfile
```

-	Layers:
	-	`sha256:71ba6227018bfc7d05fa632ddd487b57b9fb52445bf228763ea9ba24b9418971`  
		Last Modified: Wed, 24 Jul 2024 10:41:47 GMT  
		Size: 385.4 KB (385401 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0e2d972becb8530f9274a6ffcf3472c5b5340bbcea6901d01c278889d4a926b`  
		Last Modified: Wed, 24 Jul 2024 10:41:46 GMT  
		Size: 10.8 KB (10826 bytes)  
		MIME: application/vnd.in-toto+json
