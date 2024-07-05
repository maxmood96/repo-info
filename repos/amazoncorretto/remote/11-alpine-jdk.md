## `amazoncorretto:11-alpine-jdk`

```console
$ docker pull amazoncorretto@sha256:7b73082757ac589cfeea9d09f2153bfe6036dd3069b5caec1ca861f800dbcbac
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-alpine-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:a2fb965dcf13a084bd6447ae42386a8c01804ceb054ef8880c1791168997a4a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.3 MB (145261035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1338334d327aa5cd9f9750dcce6f99a1b39703095d8dcae364e46fd048ea43c2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Apr 2024 21:21:40 GMT
ADD file:fb066571462e703f86645131b43d211ff8531ffac77ea394456bfe569a6f17fe in / 
# Tue, 16 Apr 2024 21:21:40 GMT
CMD ["/bin/sh"]
# Tue, 16 Apr 2024 21:21:40 GMT
ARG version=11.0.23.9.1
# Tue, 16 Apr 2024 21:21:40 GMT
# ARGS: version=11.0.23.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Apr 2024 21:21:40 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 21:21:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 16 Apr 2024 21:21:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:b84a74cde5af5c5199bfc2ce2a8c8951a29a7716d17327e923f1a14c870a858b`  
		Last Modified: Thu, 20 Jun 2024 20:17:43 GMT  
		Size: 3.4 MB (3417332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a49c3ad2f776c974fe33c6c46070af4ac6713c4b0bad6b66fa75ee5d54e861f2`  
		Last Modified: Fri, 05 Jul 2024 19:56:14 GMT  
		Size: 141.8 MB (141843703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:211ebd6c91d2799bcbe3dd41876de32f29197528b744afc70e3977215ca79e6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.0 KB (395988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6f8030a002df6965e0e4fe4338d5976552b08d950a8e9168e71f9f477f6af35`

```dockerfile
```

-	Layers:
	-	`sha256:e4b0e758626169886f5bcfab69d02e7bfef77d627a28fb7f62351c7789ae9adc`  
		Last Modified: Fri, 05 Jul 2024 19:56:12 GMT  
		Size: 385.5 KB (385509 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa5861cfd3a99165e6c0a09b955bd78c32c511abe82e274e858eea4aefd16baa`  
		Last Modified: Fri, 05 Jul 2024 19:56:12 GMT  
		Size: 10.5 KB (10479 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-alpine-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:a186c34de776362316027d22447e3fd9800a40760b1503d4ada66ca39afbd7fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.3 MB (143289846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:198e98879b9efcdd6b9fe25ec2c5bbe9697431c811a6a4b7907b22006a1c5bd6`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Apr 2024 21:21:40 GMT
ADD file:f5632bd5469a9b26f7ff1739bb0b5dd166613259104f7bf76d587a8a428debcc in / 
# Tue, 16 Apr 2024 21:21:40 GMT
CMD ["/bin/sh"]
# Tue, 16 Apr 2024 21:21:40 GMT
ARG version=11.0.23.9.1
# Tue, 16 Apr 2024 21:21:40 GMT
# ARGS: version=11.0.23.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Apr 2024 21:21:40 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 21:21:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 16 Apr 2024 21:21:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:d4f2d2bd5ed999e04bfbfb910f14154b488ad32abf053954bff805f47fc3ad1e`  
		Last Modified: Thu, 20 Jun 2024 17:41:12 GMT  
		Size: 3.4 MB (3357202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3e7735d7eb762adb6492954294b26915286c623f822e40bad06012ef796b329`  
		Last Modified: Fri, 05 Jul 2024 20:10:27 GMT  
		Size: 139.9 MB (139932644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:3f598a55a1bd46dd90c7ac11aa62e579324d4be97c6aff7ebf4ff34659c52296
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.4 KB (396441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd61c597689699341695318245126fa1ada9f521345e6f658b537ceaeac3222f`

```dockerfile
```

-	Layers:
	-	`sha256:fcc01622a3cd97fe7d583de51ecda2ee48a4f72380a7d8a8868401c425e2bd26`  
		Last Modified: Fri, 05 Jul 2024 20:10:23 GMT  
		Size: 385.6 KB (385613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97acf6fdf124d0d1eb5caf92769db4844ff8a1d1d594022985c7a7c1a927e32c`  
		Last Modified: Fri, 05 Jul 2024 20:10:23 GMT  
		Size: 10.8 KB (10828 bytes)  
		MIME: application/vnd.in-toto+json
