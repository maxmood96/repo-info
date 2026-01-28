## `amazoncorretto:17-alpine3.23-jdk`

```console
$ docker pull amazoncorretto@sha256:0357808d805ba2e70f8a7d009d8adba610dc95223fcba167bbc202880fa0ec31
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-alpine3.23-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:3230ae92320fe797d34d1a66e75c61e72b91544f022d3a68f479dc45601c6616
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.2 MB (152228982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed6ce254edd2795fce4dbb39f16cdbfcea78505c942629baa25bc706286ab2a4`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:48:03 GMT
ARG version=17.0.18.8.1
# Wed, 28 Jan 2026 02:48:03 GMT
# ARGS: version=17.0.18.8.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Wed, 28 Jan 2026 02:48:03 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:48:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 28 Jan 2026 02:48:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9ed859fda71dc33d0955acbbb721804c828661acbb1012ae01e3ff3c4843fff`  
		Last Modified: Wed, 28 Jan 2026 02:48:20 GMT  
		Size: 148.4 MB (148367161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.23-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:ca80031efa094f6467e7b4971d825581ee91a564359e6843f95ea346eb7f687d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **593.8 KB (593819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:228c591b6019238e60d383b99206464d98b3aca9782a7e627ea4180ed68515e3`

```dockerfile
```

-	Layers:
	-	`sha256:b9808bcaf5c2f92d966608bdfa6e1e418ad40ea386d64bce5e35ba8e37d48eb0`  
		Last Modified: Wed, 28 Jan 2026 02:48:17 GMT  
		Size: 583.1 KB (583137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d7a9ee6ecccb3ef547a44e60f94a732d8ae6d72b39f005a6169537dfa7a0a1c`  
		Last Modified: Wed, 28 Jan 2026 02:48:17 GMT  
		Size: 10.7 KB (10682 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-alpine3.23-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:65d14d92d293e9c24d473421bd3e485deca66f2ea7869f0cfe805aa63043a7b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.9 MB (150909871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfb2bbd625a47771ca65e9163ff359a6135c7cfc75c30ac57f4cd1765301dd42`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:49:18 GMT
ARG version=17.0.18.8.1
# Wed, 28 Jan 2026 02:49:18 GMT
# ARGS: version=17.0.18.8.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Wed, 28 Jan 2026 02:49:18 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:49:18 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 28 Jan 2026 02:49:18 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cd0167a09da280b97a0fb6dce8bd4a2fd4b5ad1e8a8869f0be19e804f371840`  
		Last Modified: Wed, 28 Jan 2026 02:49:36 GMT  
		Size: 146.7 MB (146712780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.23-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:3ff704a802a90ddbe1e336242d6ba00d5c2f95a63d1fa50767d3ad9100042fbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **592.8 KB (592788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:679c406141b7daf111b324d1c90694ecdc30f9681fe5a6a0ea58e0a30373487a`

```dockerfile
```

-	Layers:
	-	`sha256:d3dc8f6593b7c4a2ab6eeddd44088b0bde908383f3ee9740f79af23f1da43705`  
		Last Modified: Wed, 28 Jan 2026 02:49:33 GMT  
		Size: 582.0 KB (581954 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7df318d53aac7b6d748a63b5f4241c9a4fc039d3b00e0eb95bf0ed3b41099488`  
		Last Modified: Wed, 28 Jan 2026 02:49:33 GMT  
		Size: 10.8 KB (10834 bytes)  
		MIME: application/vnd.in-toto+json
