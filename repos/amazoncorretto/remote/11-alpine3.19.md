## `amazoncorretto:11-alpine3.19`

```console
$ docker pull amazoncorretto@sha256:4f43b35144145251fb3c474bb9a600af2fbee7b51226cb2cf195c595fa90a0c9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-alpine3.19` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:347dfc696be5cbdb2aa743f7b8b6a17477391639f110f0b236cd79526a8c6042
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.2 MB (145228240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:365d787981181a3fc2ff990bbe201aabfdfde08d19dbb886e56007c11fd428b5`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 20 Jun 2024 20:17:04 GMT
ADD file:fb066571462e703f86645131b43d211ff8531ffac77ea394456bfe569a6f17fe in / 
# Thu, 20 Jun 2024 20:17:04 GMT
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
	-	`sha256:b84a74cde5af5c5199bfc2ce2a8c8951a29a7716d17327e923f1a14c870a858b`  
		Last Modified: Thu, 20 Jun 2024 20:17:43 GMT  
		Size: 3.4 MB (3417332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcf907c28030346c77f6ea15051539cef29c08f4631604fbf6b09ba7edf5ffe7`  
		Last Modified: Thu, 18 Jul 2024 00:55:49 GMT  
		Size: 141.8 MB (141810908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.19` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:5113ff1678a7c42cb111f23649df62bd8db238e4eb7e0e54491d0faaebdd669a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **397.4 KB (397396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8790b617eb080123ece8d9aeec18d18b54e4b456cf36d4d27e45fb257baf5ba8`

```dockerfile
```

-	Layers:
	-	`sha256:b78762ae36803d2a5798c2aefda3a612ae3d45e40b5be3117a721146bf989017`  
		Last Modified: Thu, 18 Jul 2024 00:55:45 GMT  
		Size: 388.2 KB (388224 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f4f4a86ab7c282756edb974319ea125ec1d95c1c2b4a3172c2016eabdafb449`  
		Last Modified: Thu, 18 Jul 2024 00:55:45 GMT  
		Size: 9.2 KB (9172 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:836df20a3d4e0c21379ba768d307aae54437dc8972fb94d569f0a448e573944e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.3 MB (143316042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:522ab9fda7f97cb9b06a5124a5328ee1897c99552a7d0c54682600a105ba29a8`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:38 GMT
ADD file:f5632bd5469a9b26f7ff1739bb0b5dd166613259104f7bf76d587a8a428debcc in / 
# Thu, 20 Jun 2024 17:40:38 GMT
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
	-	`sha256:d4f2d2bd5ed999e04bfbfb910f14154b488ad32abf053954bff805f47fc3ad1e`  
		Last Modified: Thu, 20 Jun 2024 17:41:12 GMT  
		Size: 3.4 MB (3357202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcca778f984f2205a165ed9e8e5933b21a4917e7454e01f38acbaf40035817a6`  
		Last Modified: Thu, 18 Jul 2024 01:09:06 GMT  
		Size: 140.0 MB (139958840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.19` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:785a38fdb0890db52766ae01e662351417f6d5fb2ac1e7502ca31e2dc8d35890
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **397.8 KB (397752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c99188f3e4ea42a92501fbc59dd9c102f53a83f40ea2a769807cef4346ef3a1c`

```dockerfile
```

-	Layers:
	-	`sha256:2a41a49e2dd0cdeb0affe68f7cfe97c3f0479bcf25783718319803f82f647f74`  
		Last Modified: Thu, 18 Jul 2024 01:09:02 GMT  
		Size: 388.3 KB (388280 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e5bf4c3b697a6a2ce381ea2e79691522c7c088899770d7190c440fb2df3827b`  
		Last Modified: Thu, 18 Jul 2024 01:09:02 GMT  
		Size: 9.5 KB (9472 bytes)  
		MIME: application/vnd.in-toto+json
