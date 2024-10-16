## `amazoncorretto:8-alpine3.18-jre`

```console
$ docker pull amazoncorretto@sha256:15b247f7d9ce381746483cfa8908b34716b247f45b92b4d84cf648ed5f0923e8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-alpine3.18-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:78b8b4600b54313e19fbcdb01ce48f61b861495bb31abe433cc9e2777f98c8ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.1 MB (45072312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20b009e88866795707783430371c34a4e020baa74932af8b7f15d4a5050a1c9f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:19 GMT
ADD file:5dd525c57625a3a84d57d435b3c255f417ad1722250faaf006c66b9090207f66 in / 
# Fri, 06 Sep 2024 22:20:19 GMT
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
	-	`sha256:1cc3d825d8b2468ef662a8b631220516f492e24232477209fe863836d2d2ed44`  
		Last Modified: Fri, 06 Sep 2024 22:20:59 GMT  
		Size: 3.4 MB (3416313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36fc06cef69c56908ad79db5e087ade937a1b6715723c6cdb5d5d0c7a6fc1744`  
		Last Modified: Wed, 16 Oct 2024 17:55:53 GMT  
		Size: 41.7 MB (41655999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.18-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:eba529c169c2a0467043959a6fd059655267f17d86d7857c6559939ac971c47f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.3 KB (193263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de5200117e0df43562758be8aa8be3fdf85cffbaa6db1213856840b9722ba5c5`

```dockerfile
```

-	Layers:
	-	`sha256:b6ecae0276ab646ad2349650c7a5a5b67504aae1266a5c45f2f7de0bc71c2645`  
		Last Modified: Wed, 16 Oct 2024 17:55:53 GMT  
		Size: 184.8 KB (184771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18368edda0bbe2116316d8f17be48d1b1840a75a9aae206d0fd18f043d60f5c4`  
		Last Modified: Wed, 16 Oct 2024 17:55:53 GMT  
		Size: 8.5 KB (8492 bytes)  
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
