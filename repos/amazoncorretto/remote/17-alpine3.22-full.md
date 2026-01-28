## `amazoncorretto:17-alpine3.22-full`

```console
$ docker pull amazoncorretto@sha256:b28bb7fae0a3bca761045de00f4400068faccb8ab463356c5f1b0c644bec2bfc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-alpine3.22-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:11d30a24c48c44be64873ca9f076c6c5b8f33d3a2e2abe25822b70d2fa171f1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.2 MB (152173425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e749f90964e12fb2a06b6a244eddacbbfba86b9a7c0713d3c89ce29d66f2c6a3`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:47:40 GMT
ARG version=17.0.18.8.1
# Wed, 28 Jan 2026 02:47:40 GMT
# ARGS: version=17.0.18.8.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Wed, 28 Jan 2026 02:47:40 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:47:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 28 Jan 2026 02:47:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42553a5753a849b2187e2fe6d8199a6666cbf97cab10ed6414555b01a4a3764d`  
		Last Modified: Wed, 28 Jan 2026 02:47:57 GMT  
		Size: 148.4 MB (148368550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.22-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:f0d3f9f26da56922e7e89c91f2ee2e610cbf26f98a313361fb5d3be16b039f5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **592.5 KB (592510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f44120a187729e0a6417c6781aae9689dfa61e9a1cb2abace6ec1b62d3283a17`

```dockerfile
```

-	Layers:
	-	`sha256:6862a9b10a61a13b49779ef97bd3cef8ad9c867337959f67332b03e44aef477f`  
		Last Modified: Wed, 28 Jan 2026 02:47:53 GMT  
		Size: 583.1 KB (583136 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5e55ffd355e8e076f5a2511271ae963d75d05fe8aede4ccce38bec971fe5bec`  
		Last Modified: Wed, 28 Jan 2026 02:47:53 GMT  
		Size: 9.4 KB (9374 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-alpine3.22-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:5f5bb24fb23b893dd5684e1d766d89c7aa598e9c9da3ab14274dfd0f51d71ba5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.9 MB (150850221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4763b2f657f8bf6962cb1af717dacd84bd4b0062d4bd4e76b47c649e2f7a31f9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:48:33 GMT
ARG version=17.0.18.8.1
# Wed, 28 Jan 2026 02:48:33 GMT
# ARGS: version=17.0.18.8.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Wed, 28 Jan 2026 02:48:33 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:48:33 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 28 Jan 2026 02:48:33 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d425aa915701d560e60bbffb6d3889828b3237410852fb189aa2765d1c710829`  
		Last Modified: Wed, 28 Jan 2026 02:48:50 GMT  
		Size: 146.7 MB (146710702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.22-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:7a8c0b30ff530f6c380088e151f9220485f26a3fcef851d47cd4945d2299c040
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **592.0 KB (592033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c90ba4d62ec2927dd0691a6da39a02691a62191e0e9cb230a6020b8361ee69f`

```dockerfile
```

-	Layers:
	-	`sha256:cfcb5b9649b55d919206a13a83aad7084872377a687ffdfed75a5d01d02e0d2c`  
		Last Modified: Wed, 28 Jan 2026 02:48:47 GMT  
		Size: 582.6 KB (582555 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f07cda2c323f7904fc809804e3d17805245108d906a7fde6eb909974d91030b3`  
		Last Modified: Wed, 28 Jan 2026 02:48:47 GMT  
		Size: 9.5 KB (9478 bytes)  
		MIME: application/vnd.in-toto+json
