## `amazoncorretto:17-alpine3.22-jdk`

```console
$ docker pull amazoncorretto@sha256:43c27577029a4447ca145be43698fbaa1e147070c5dad28b7180e6f95e4059a8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-alpine3.22-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:c59250561693605cd5cedd6d215308473d0846387a1011afc7b24edef77d8435
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.4 MB (152373841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08c27189dc04a40129030defc99751e9ee06ddced9991d52998aeb14115527aa`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:21 GMT
ADD alpine-minirootfs-3.22.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:21 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:53:56 GMT
ARG version=17.0.19.10.1
# Mon, 22 Jun 2026 19:53:56 GMT
# ARGS: version=17.0.19.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Mon, 22 Jun 2026 19:53:56 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 19:53:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Mon, 22 Jun 2026 19:53:56 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:f7ee36c9aa34bbb665f975c76e5c0d1607f0674b94c84cfb0061f87006ea5d10`  
		Last Modified: Mon, 22 Jun 2026 09:11:44 GMT  
		Size: 3.8 MB (3787595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f550678e13968b1f7e89d4d7bdfcf2e8287baa0d37e46d17bedc8e5fd8c82cdb`  
		Last Modified: Mon, 22 Jun 2026 19:54:13 GMT  
		Size: 148.6 MB (148586246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.22-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:c89518921d62d0393b37d72a0d4b3d8563a0feccc46155e87beac1d705a98765
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **593.2 KB (593166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40cd8c97c9e765624317eb4ae1e2fd1a8882ca319280485d7aabcf1edde85c90`

```dockerfile
```

-	Layers:
	-	`sha256:7e99d82c0a4c750a8e14f2d1618fd02bf1723fd67ec0b93231d73470333cd222`  
		Last Modified: Mon, 22 Jun 2026 19:54:10 GMT  
		Size: 583.8 KB (583787 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:407e8663b7f355769b2f0aa6f239de3dbf67f0020670339c75737fdc56eb9e4c`  
		Last Modified: Mon, 22 Jun 2026 19:54:10 GMT  
		Size: 9.4 KB (9379 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-alpine3.22-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:5ac4391887e59b755bb9443031dc4493be0ad57115e26bac98daa871f1d66769
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.1 MB (151056140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55e55f43140ab05f27194d5b23b52112b3183f83a05594f6af133449e23fd8b2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:11 GMT
ADD alpine-minirootfs-3.22.5-aarch64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:11 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:55:29 GMT
ARG version=17.0.19.10.1
# Mon, 22 Jun 2026 19:55:29 GMT
# ARGS: version=17.0.19.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Mon, 22 Jun 2026 19:55:29 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 19:55:29 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Mon, 22 Jun 2026 19:55:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:738128faa30f570583b0e57efd831e0e6a2a9aacf1be88c8f4c1ef8a5b7033cc`  
		Last Modified: Mon, 22 Jun 2026 09:11:35 GMT  
		Size: 4.1 MB (4120486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29b1eaf47c1f057b880b189fa447d8cf08b4412b1eb24cb6b1142a3e44186e90`  
		Last Modified: Mon, 22 Jun 2026 19:55:47 GMT  
		Size: 146.9 MB (146935654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.22-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:a7ba66333df1da0722055db4ab1968af9db266c63f184466e405bc100a1b8811
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **592.7 KB (592689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eed9519d22b37745c46fdbd2fd03b7fdfdd29846addaf5c24adcb4fc60ad9675`

```dockerfile
```

-	Layers:
	-	`sha256:54eb1b86a7613649feea9389c912db40f95b074d73fa6fad332c9b3c84c02014`  
		Last Modified: Mon, 22 Jun 2026 19:55:44 GMT  
		Size: 583.2 KB (583206 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:207750eafa39ead6988018445e5924909b5f64bb9ffece59d406b736c66aaba2`  
		Last Modified: Mon, 22 Jun 2026 19:55:44 GMT  
		Size: 9.5 KB (9483 bytes)  
		MIME: application/vnd.in-toto+json
