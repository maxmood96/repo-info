## `amazoncorretto:17-alpine3.19-full`

```console
$ docker pull amazoncorretto@sha256:4530abf51f2a9ad2628bea27725a687168284879d8a09f42195e4e7469bd5650
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-alpine3.19-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:68f11f7c8b255fc38dd3e3fe75f065f5dc4a5b087129488122a422fc39716680
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.4 MB (149435399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a29b9b36234a4830fa4a1092d034f509901c5f684bfd37865d8dac2777c8885`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 20 Jun 2024 20:17:04 GMT
ADD file:fb066571462e703f86645131b43d211ff8531ffac77ea394456bfe569a6f17fe in / 
# Thu, 20 Jun 2024 20:17:04 GMT
CMD ["/bin/sh"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=17.0.12.7.1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=17.0.12.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 16 Jul 2024 22:56:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:b84a74cde5af5c5199bfc2ce2a8c8951a29a7716d17327e923f1a14c870a858b`  
		Last Modified: Thu, 20 Jun 2024 20:17:43 GMT  
		Size: 3.4 MB (3417332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34713cdaebac57a84a92063efda61430ff261066829485da248d1d74fdbd5f97`  
		Last Modified: Thu, 18 Jul 2024 00:55:56 GMT  
		Size: 146.0 MB (146018067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.19-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:39296f6a2ce2ec63f23a260730d049eecc5a9ce922e4da3bbd73b7b7cd97f72e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.9 KB (389935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c97143cac9e704fdbc9352ef720d8e8c51bbaba4ca5dfba3e25b5d7b05837a31`

```dockerfile
```

-	Layers:
	-	`sha256:0617600dcce287a2f34cd3cacaba7e17bd47b2a75fad48bd678517c55159a537`  
		Last Modified: Thu, 18 Jul 2024 00:55:53 GMT  
		Size: 380.8 KB (380763 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:805d3435790f76eea54b43d60f282115f7e9990f7b0fa214ce262f056a1f2be8`  
		Last Modified: Thu, 18 Jul 2024 00:55:52 GMT  
		Size: 9.2 KB (9172 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-alpine3.19-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:b5723e477abe7d6243853d7a9b9e800691ff9c743b42adeaf20a789224cc15b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.7 MB (147707956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93c9f82b0e8a92f40219145a967261b83ce485d4aaf15cfb511a7e3e1c1c5810`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:38 GMT
ADD file:f5632bd5469a9b26f7ff1739bb0b5dd166613259104f7bf76d587a8a428debcc in / 
# Thu, 20 Jun 2024 17:40:38 GMT
CMD ["/bin/sh"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=17.0.12.7.1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=17.0.12.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 16 Jul 2024 22:56:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:d4f2d2bd5ed999e04bfbfb910f14154b488ad32abf053954bff805f47fc3ad1e`  
		Last Modified: Thu, 20 Jun 2024 17:41:12 GMT  
		Size: 3.4 MB (3357202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b78f93404a7937c552ee4b89eaf805ea5e47d0425d072569573bd426fd17911e`  
		Last Modified: Thu, 18 Jul 2024 01:17:31 GMT  
		Size: 144.4 MB (144350754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.19-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:c8809d5b88c3e4d24289cb23d16dfcb2999b8fedc9b4403d50af4a604bd5b33a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.7 KB (389653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe04ad1df87956ceec0bd72322dcf7e7ad03a3f0b4c363bca3cc6e5ffb5a12f1`

```dockerfile
```

-	Layers:
	-	`sha256:915885e241d846a2cc4cfac72ea30eb9ef88b101949ec704d98b91235cbfbbea`  
		Last Modified: Thu, 18 Jul 2024 01:17:27 GMT  
		Size: 380.2 KB (380181 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1029adacc1b98b3b0880b27d4acaf4c0f4f5f3d70b0ffb40c3f6730ef5d9143d`  
		Last Modified: Thu, 18 Jul 2024 01:17:27 GMT  
		Size: 9.5 KB (9472 bytes)  
		MIME: application/vnd.in-toto+json
