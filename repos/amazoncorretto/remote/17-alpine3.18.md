## `amazoncorretto:17-alpine3.18`

```console
$ docker pull amazoncorretto@sha256:27ce63e98b64a48f4d59798717cb227b3fc1b25f2ea041916cbf0ddc5fa3e751
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-alpine3.18` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:98feeb90aec2b6ed260a9d850c540487a4691e98e77c4118065b45a64ae9d5ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.1 MB (149067637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a97b1dd3691dd7b514fc564ff74846d09f9458a6a1b32e5c1802136efff9338`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
ADD alpine-minirootfs-3.18.11-x86_64.tar.gz / # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 23:01:14 GMT
ARG version=17.0.13.11.1
# Fri, 13 Dec 2024 23:01:14 GMT
# ARGS: version=17.0.13.11.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 23:01:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 13 Dec 2024 23:01:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:f54a5150a7602eaef3169b83e73d5927b20aef2fcaefcba18b532bd63b328fff`  
		Last Modified: Tue, 14 Jan 2025 20:33:01 GMT  
		Size: 3.4 MB (3417974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c535ab4b355c3ef1064bc0a1166fff944dfa977ff757054366a1536815d2862b`  
		Last Modified: Tue, 14 Jan 2025 20:36:32 GMT  
		Size: 145.6 MB (145649663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.18` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:5a68fa6a05034b54d66c7a21dcd34f0b9d238d52bb5ac0e172eef5c0f8741014
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.7 KB (389658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abcf83ededf7f15b2dd879554efd22657536cd645b7d77e051556ae1caa11a60`

```dockerfile
```

-	Layers:
	-	`sha256:2e1f9c6538547f91c55df83a118395fe66c727a7c8e85b9a1a815ee5931335b3`  
		Last Modified: Wed, 08 Jan 2025 18:11:23 GMT  
		Size: 380.2 KB (380236 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee69504b4f2ee0e0ebabf480b83b8538b7d45f99cf234c001a8f4faf8817eb76`  
		Last Modified: Wed, 08 Jan 2025 18:11:23 GMT  
		Size: 9.4 KB (9422 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:cd955603907ea487362869ab375e7e12d294602e7140dde0f75a1c59fa5d0ca6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.3 MB (147276910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34fb4d6fb1d248b4cba219e5970a5221683931c069ea1bae54f69f15afb35be9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
ADD alpine-minirootfs-3.18.11-aarch64.tar.gz / # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 23:01:14 GMT
ARG version=17.0.13.11.1
# Fri, 13 Dec 2024 23:01:14 GMT
# ARGS: version=17.0.13.11.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 23:01:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 13 Dec 2024 23:01:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:f6b431426dd566e612639f03cd46e521b3133a043bb6b60edeeeef80d513e870`  
		Last Modified: Tue, 14 Jan 2025 20:34:06 GMT  
		Size: 3.3 MB (3341861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d751a60c3c2aa17a9631876cab6feb1841f9521615571ffb41a0351760a037ee`  
		Last Modified: Wed, 08 Jan 2025 22:19:18 GMT  
		Size: 143.9 MB (143935049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.18` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:793f1dffee35d1af8baaa63706bf894dd2a6cc9f916bf6437ef7c46842248f73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.2 KB (389181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a30b1e5e8051fa4480d951d5176a26f0b89ebdca4b2a1d3730db9d151a75670`

```dockerfile
```

-	Layers:
	-	`sha256:6bb35372cfd6826903bde5d2932cfa46160eaca8129cf01edf6a200abf58a319`  
		Last Modified: Wed, 08 Jan 2025 22:19:14 GMT  
		Size: 379.7 KB (379655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7eadb83a2e5756a423ca4c9166dff2bcf2a915fad181893ef119891f86baf97c`  
		Last Modified: Wed, 08 Jan 2025 22:19:14 GMT  
		Size: 9.5 KB (9526 bytes)  
		MIME: application/vnd.in-toto+json
