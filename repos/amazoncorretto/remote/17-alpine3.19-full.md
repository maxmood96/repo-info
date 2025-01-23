## `amazoncorretto:17-alpine3.19-full`

```console
$ docker pull amazoncorretto@sha256:1a4369c3eac1dd9927b95e34d6a3198beab382312e12d351fcf044bdc55f121d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-alpine3.19-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:63d141d176e186719cdd207b2798edf3c338d3006e476a276b2b9d6907abbc84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.1 MB (149069629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5249495cb7e82701f9af101a91c48861f1313a737d2283e1549ab8c9a9bd79bc`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
ADD alpine-minirootfs-3.19.6-x86_64.tar.gz / # buildkit
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
	-	`sha256:861950bce9fa55e0462bb22503f61d8e7396f292af10969506b51e7bdb701d60`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.4 MB (3420242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba407145c9401126c3dec836fcba3e11997e54f81df4d4144407ff22c0aa6dd4`  
		Last Modified: Wed, 08 Jan 2025 18:13:20 GMT  
		Size: 145.6 MB (145649387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.19-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:e9085d81ff004710cf6f1c159eef2de0b3a6a71162711af07a9726746c5fe1a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **390.3 KB (390317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36b37bee8ff94e0be05d9a4ef67efbb2988fb8d235a30c208dfa91453ba02f72`

```dockerfile
```

-	Layers:
	-	`sha256:aaa7c501f2e149097506c74ca0c5965f2b943b00e2c5776d29ab24f9f19519e3`  
		Last Modified: Wed, 08 Jan 2025 18:13:18 GMT  
		Size: 380.9 KB (380895 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddd9feeff97d2f64327b0d31ba1df3339524e1d1d46db000aa58c63d0092edc4`  
		Last Modified: Wed, 08 Jan 2025 18:13:18 GMT  
		Size: 9.4 KB (9422 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-alpine3.19-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:27977af4513edf641a7d549e976a73aafabe032a9068680c92daa775d165cba3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.4 MB (147382386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9672a44fb8e730c7cc500e8dd28e2c31823d37784c49065c61206e0d92157ed9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:06:42 GMT
ADD alpine-minirootfs-3.19.6-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:06:42 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2025 01:09:23 GMT
ARG version=17.0.14.7.1
# Thu, 23 Jan 2025 01:09:23 GMT
# ARGS: version=17.0.14.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Thu, 23 Jan 2025 01:09:23 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jan 2025 01:09:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Thu, 23 Jan 2025 01:09:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:88b83b407e415cb5cb78776f0e83bf403b89f77eb02721ce6a3cbf1eba723438`  
		Last Modified: Wed, 08 Jan 2025 17:24:18 GMT  
		Size: 3.4 MB (3360532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4764cc5cfceb8f11be8768feb456ba10642f2ef3caef7921575286ca20551ef3`  
		Last Modified: Thu, 23 Jan 2025 18:48:13 GMT  
		Size: 144.0 MB (144021854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.19-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:6f94ca04c8f585fe6ecaf5fe4a6c7c27672739d2277fdcadf6e4eddf9986bbfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.8 KB (389833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71896a2fcce59365e5804c471d55549dbc7746bd620ad1f7add84cca30af4301`

```dockerfile
```

-	Layers:
	-	`sha256:4639c8de075d975362c9ef467312ab1add84d7ac7e5d885951a8f4140029228e`  
		Last Modified: Thu, 23 Jan 2025 18:48:10 GMT  
		Size: 380.3 KB (380312 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a85ae0245d32402bebbc106f2e3b129c176f8b94c8b5ed93ea33767a43677b2`  
		Last Modified: Thu, 23 Jan 2025 18:48:10 GMT  
		Size: 9.5 KB (9521 bytes)  
		MIME: application/vnd.in-toto+json
