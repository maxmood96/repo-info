## `amazoncorretto:8-alpine3.19-full`

```console
$ docker pull amazoncorretto@sha256:dc43d18c7f03d6a9b0c1773aebef361b9722b0146129c40d0ae4e06c56bfa9ca
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-alpine3.19-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:009ceeaf8052fb52017cd84c548721e8066983a442901a48c1993af7d525098f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.7 MB (103710632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d265270b376632a9e9da8fe7b5c54f6666e0c7be8c90afb6302989292a2eb7da`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:32:09 GMT
ADD alpine-minirootfs-3.19.8-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:32:09 GMT
CMD ["/bin/sh"]
# Wed, 16 Jul 2025 19:33:24 GMT
ARG version=8.462.08.1
# Wed, 16 Jul 2025 19:33:24 GMT
# ARGS: version=8.462.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 16 Jul 2025 19:33:24 GMT
ENV LANG=C.UTF-8
# Wed, 16 Jul 2025 19:33:24 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 16 Jul 2025 19:33:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:1747dece94917ce1b0256ecd60138ce4deaea1bd35dcb6b2e8afe697dd2f5b71`  
		Last Modified: Tue, 15 Jul 2025 18:59:51 GMT  
		Size: 3.4 MB (3415528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69dc2bcc1b62fa481f3e5bc75ce4a8403d1f93bbc7cc5ba51c58c9e12d9d05ce`  
		Last Modified: Wed, 16 Jul 2025 20:25:13 GMT  
		Size: 100.3 MB (100295104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.19-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:d0647acc6b2520f9d9ccb96bc4404edfeb8edcdd8e55692dc8de88abe5360aa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.8 KB (256800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2074eb4beddec869148ae9dc8c756925d2d33ca8265b0e277f5beb44185a9153`

```dockerfile
```

-	Layers:
	-	`sha256:9175b8032e6401da8f30eff74d9e14feda78b8088fbe8628f0e03266bd5da62d`  
		Last Modified: Wed, 16 Jul 2025 21:51:31 GMT  
		Size: 247.4 KB (247402 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53c483e56c9120967a0319ab94551e2298e0f119c7328bdefa037387fbf84fc5`  
		Last Modified: Wed, 16 Jul 2025 21:51:32 GMT  
		Size: 9.4 KB (9398 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-alpine3.19-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:d523ef052ab32efb18da918627759d106cec919f57352d57dc2f9e6bfdf0de4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.4 MB (103444741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78c0f7cad9d05c15ed618f70aac0d5cddde5cd54ebd24a2d2000cb26f7359225`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:32:09 GMT
ADD alpine-minirootfs-3.19.8-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:32:09 GMT
CMD ["/bin/sh"]
# Wed, 16 Jul 2025 19:33:24 GMT
ARG version=8.462.08.1
# Wed, 16 Jul 2025 19:33:24 GMT
# ARGS: version=8.462.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 16 Jul 2025 19:33:24 GMT
ENV LANG=C.UTF-8
# Wed, 16 Jul 2025 19:33:24 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 16 Jul 2025 19:33:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:07e9a47f0c334cceba1b05e86ef0150c84564a9b9e9d4ae9dc9a5ebc85ef2b7c`  
		Last Modified: Tue, 15 Jul 2025 19:00:19 GMT  
		Size: 3.4 MB (3353103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:654d45448034489b74e6de224b1a803684e465781ebc1c23c95f861b0663dffc`  
		Last Modified: Thu, 17 Jul 2025 01:47:01 GMT  
		Size: 100.1 MB (100091638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.19-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:829c919813111a49a98edb36c54a2d67dec803d06ad40a6be06c7232856ae544
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.0 KB (257036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f10af047cf671409bae7c6fab5a5a8bd859878800e130ce80157644c0c3e645`

```dockerfile
```

-	Layers:
	-	`sha256:9e3ec4fe7db6c284301871f66887ba350fd9036584e010cd2bc6c0d05ad5ffff`  
		Last Modified: Thu, 17 Jul 2025 03:51:22 GMT  
		Size: 247.5 KB (247534 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e370fce20f067498d627cd0f844cf902351f259e522c3df8bd89062390e1a1d`  
		Last Modified: Thu, 17 Jul 2025 03:51:22 GMT  
		Size: 9.5 KB (9502 bytes)  
		MIME: application/vnd.in-toto+json
