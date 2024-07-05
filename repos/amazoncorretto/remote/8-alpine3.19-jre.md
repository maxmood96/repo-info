## `amazoncorretto:8-alpine3.19-jre`

```console
$ docker pull amazoncorretto@sha256:8d85aa73a633a063afb946451b5c2b95c67e0ca1587d82880847264577e40bd2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-alpine3.19-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:8f22ce2f4a86dec10683a953ac0d304c9ca55f5f3402f1698508cbc32941a0cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.1 MB (45064921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5a2e7821ab813f613fff0271a750353d011c551ec26b59db637756af51fc772`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Apr 2024 21:21:40 GMT
ADD file:fb066571462e703f86645131b43d211ff8531ffac77ea394456bfe569a6f17fe in / 
# Tue, 16 Apr 2024 21:21:40 GMT
CMD ["/bin/sh"]
# Tue, 16 Apr 2024 21:21:40 GMT
ARG version=8.412.08.1
# Tue, 16 Apr 2024 21:21:40 GMT
# ARGS: version=8.412.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Apr 2024 21:21:40 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 21:21:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:b84a74cde5af5c5199bfc2ce2a8c8951a29a7716d17327e923f1a14c870a858b`  
		Last Modified: Thu, 20 Jun 2024 20:17:43 GMT  
		Size: 3.4 MB (3417332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:196ea4f73002511493d0efe6b7df0a8eb4f0e9ed1be516008292f47001292b52`  
		Last Modified: Fri, 05 Jul 2024 19:56:10 GMT  
		Size: 41.6 MB (41647589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.19-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:6a93882f481aef5aed724bbacbfb25687ad70221153343c829f25d07c5680c61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.2 KB (189212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd3ad6fb1daaf41d9c32a3b6834ad3f93890dca538ac70fea8dc9cfb924a297d`

```dockerfile
```

-	Layers:
	-	`sha256:339216341706ccca6e7a482479f4a440f97403692fded6284567ed3f0c5eff5f`  
		Last Modified: Fri, 05 Jul 2024 19:56:08 GMT  
		Size: 180.1 KB (180098 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1edfc9c1b950867af36067f1a9c33e910965a3e4e3b37d1ad766bd50e046816f`  
		Last Modified: Fri, 05 Jul 2024 19:56:08 GMT  
		Size: 9.1 KB (9114 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-alpine3.19-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:6d1e116e341a2e1df522e6bfa93cc4ff81022eb97b6624d6b2550a8070f4aac4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.7 MB (44657300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89aa42509aad35399d2aeb8a0cfdfa767e4ad2df6ff047f4d3b79f013db7ecab`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Apr 2024 21:21:40 GMT
ADD file:f5632bd5469a9b26f7ff1739bb0b5dd166613259104f7bf76d587a8a428debcc in / 
# Tue, 16 Apr 2024 21:21:40 GMT
CMD ["/bin/sh"]
# Tue, 16 Apr 2024 21:21:40 GMT
ARG version=8.412.08.1
# Tue, 16 Apr 2024 21:21:40 GMT
# ARGS: version=8.412.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Apr 2024 21:21:40 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 21:21:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:d4f2d2bd5ed999e04bfbfb910f14154b488ad32abf053954bff805f47fc3ad1e`  
		Last Modified: Thu, 20 Jun 2024 17:41:12 GMT  
		Size: 3.4 MB (3357202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b50bb7a200bc3667411bd7fa5c8748dfc217210e6390da0e06d2b9b9c5ef38ac`  
		Last Modified: Fri, 05 Jul 2024 20:02:34 GMT  
		Size: 41.3 MB (41300098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.19-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:649ebbd18a7b98530719d7966769adcb6be52aefb9a55716cfc3026ba42e2674
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.6 KB (189644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f823a6fbcb0782c14ece42db9e01710a2435114f5fbab10f73e524586e500d1`

```dockerfile
```

-	Layers:
	-	`sha256:dd6b9bb49146df77e22e67e0fbbf7c35f609221496d2e6f4b5173bd85c820eaf`  
		Last Modified: Fri, 05 Jul 2024 20:02:33 GMT  
		Size: 180.2 KB (180230 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e8dea40826231d54f052a06339da496b7dbd9e280d0f9d31a50ce18866b2e8b`  
		Last Modified: Fri, 05 Jul 2024 20:02:33 GMT  
		Size: 9.4 KB (9414 bytes)  
		MIME: application/vnd.in-toto+json
