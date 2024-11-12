## `amazoncorretto:8-alpine3.18-jre`

```console
$ docker pull amazoncorretto@sha256:3357e11c6800189bd0c4e559d84f3d9f1d32b123d033b917ba52b42b5a77b6b1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-alpine3.18-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:2245b8edbf3877f9f33467963b5c4674ec47c83a0d43b3c5bc7440c86df89144
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.1 MB (45072286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa12e385bfd54f883c5644588bf3b8461b4f3a54200c11fd25949febba948e88`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:03:22 GMT
ADD alpine-minirootfs-3.18.9-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:03:22 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=8.432.06.1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=8.432.06.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:dc0decf4841d19b14e836c2d82bd5cb9540fb5e0d1359549ca243f49036557e9`  
		Last Modified: Mon, 09 Sep 2024 07:02:43 GMT  
		Size: 3.4 MB (3416401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93fbb9a965d3205e852905aac174b5034d21ce0ee781f5b26488ea9edde1d75c`  
		Last Modified: Tue, 12 Nov 2024 02:11:40 GMT  
		Size: 41.7 MB (41655885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.18-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:fba302d3365f7fd6fc09075ea896193bb7ff4c43612b3fcbe5df0c3b64333c95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.6 KB (193563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8fba0ad168bba03a7921159d87df15688ddc074ebdee234fa5127ed8149d162`

```dockerfile
```

-	Layers:
	-	`sha256:a79f0bfcea4b0c166eabe5364e7d6102ebb63f0b34a27f222248687239d5aa27`  
		Last Modified: Tue, 12 Nov 2024 02:11:40 GMT  
		Size: 184.9 KB (184864 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d45459153e6edc35892ad380ae114b40158b0421498aea024d22237f3475d2c7`  
		Last Modified: Tue, 12 Nov 2024 02:11:40 GMT  
		Size: 8.7 KB (8699 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-alpine3.18-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:36997e877de7ea30afd13e3a37af6652726bdec6e2f9272c9661b4402d6f6e41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.7 MB (44698672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:236c7cbb94773a570fffb4c8c7a99f5372ee9ea7e0a84741837233b91ee9fd3c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:20 GMT
ADD file:c2dbff469fced00345f9627d1efd892f94d53dbb31a6485fa9411b2fb1b4840f in / 
# Fri, 06 Sep 2024 22:44:20 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=8.432.06.1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=8.432.06.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:720f3032cd1105e6311c8adee3ee0f3b6827bec2c48f1cfff486a347ad22f05c`  
		Last Modified: Fri, 06 Sep 2024 22:44:58 GMT  
		Size: 3.3 MB (3340347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1c5ba4148dc97cc30b29a16323a14d40c73e4474ac931db95df0361b521f552`  
		Last Modified: Wed, 16 Oct 2024 18:08:42 GMT  
		Size: 41.4 MB (41358325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.18-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:b2095cef6579ce1595015b4206fb30c67c77a648010e5ecd93d2f70b6f9f1b27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.4 KB (193445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c493b9d2c1bafdcf73b910f239ddeaf22b56bb9ce29acd652a9b8663e75dfec8`

```dockerfile
```

-	Layers:
	-	`sha256:2af83c5daccbdb7884a0a4709bc9d4e3ecf1a6057d2ed11ecabd17164f363f6a`  
		Last Modified: Wed, 16 Oct 2024 18:08:40 GMT  
		Size: 184.9 KB (184879 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bcb7fb4f37bb44e8be1d56b435653fbfa5653bb498320112431d21be773be46c`  
		Last Modified: Wed, 16 Oct 2024 18:08:40 GMT  
		Size: 8.6 KB (8566 bytes)  
		MIME: application/vnd.in-toto+json
