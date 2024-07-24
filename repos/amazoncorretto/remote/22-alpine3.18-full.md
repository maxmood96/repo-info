## `amazoncorretto:22-alpine3.18-full`

```console
$ docker pull amazoncorretto@sha256:feaef76ec43395973ca9138677699de405033708d94dd7b01c69297bf1dcb3c7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:22-alpine3.18-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:1ab3bac67472328486c56018ec1311fd3d83b50a459b0ac5c720387d456a29c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.0 MB (161011676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:662ad037f6cf29b99865c947a9c9d1af7380db244d8cc61fceba54bd1b92f83a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
ADD file:5851aef23205a072ef361dd412a73a39a1ada75e19a207a392bb7ec9b8556e11 in / 
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/sh"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=22.0.2.9.1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=22.0.2.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-22=$version-r0 &&     rm -rf /usr/lib/jvm/java-22-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 16 Jul 2024 22:56:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:930bdd4d222e2e63c22bd9e88d29b3c5ddd3d8a9d8fb93cf8324f4e7b9577cfb`  
		Last Modified: Mon, 22 Jul 2024 22:27:34 GMT  
		Size: 3.4 MB (3415640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b23d7ff48c088848fe7dddc60667dd1b7e267effc0a440421677ed091efbf34b`  
		Last Modified: Mon, 22 Jul 2024 23:06:53 GMT  
		Size: 157.6 MB (157596036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:22-alpine3.18-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:c8f9967bde1aa30a7268d7e01443c5c648845d35e7c0476002060cd73e855b6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **390.4 KB (390415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:572bc1205090db9bb9b7df2e66584f77dbe8bfbef787669b727fd1578a2b0bf3`

```dockerfile
```

-	Layers:
	-	`sha256:6485412a62b97aa95d57c06c784df4c748940328dff42426dbba629b90375e2b`  
		Last Modified: Mon, 22 Jul 2024 23:06:49 GMT  
		Size: 381.2 KB (381246 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5dc6ba27d32db146d6253ca7dc52f1ebb048c32226e5d67c25c8c25f1fcc620f`  
		Last Modified: Mon, 22 Jul 2024 23:06:49 GMT  
		Size: 9.2 KB (9169 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:22-alpine3.18-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:a5751af93cb144fd8e49b828eab0fe3d620a296729f88a9d6285fbf443c84ac0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.5 MB (158534206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d71bb8b56bd393ed299b24f4cf6915c91ab4713d52c19473c65470d01cd6bac1`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
ADD file:4a10978248445fe045fc2859ce867988ab71bd2281ad7d88b62597252642a56b in / 
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/sh"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=22.0.2.9.1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=22.0.2.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-22=$version-r0 &&     rm -rf /usr/lib/jvm/java-22-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 16 Jul 2024 22:56:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:4983c3fe2029a430985943e6d87b35248366efd28cee655acc3ebff5daf703fa`  
		Last Modified: Mon, 22 Jul 2024 21:44:57 GMT  
		Size: 3.3 MB (3339494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24caf9c515c953c92c2982a6c284b78d53e56054cde93c88fde8ee390fe9fd70`  
		Last Modified: Wed, 24 Jul 2024 10:47:32 GMT  
		Size: 155.2 MB (155194712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:22-alpine3.18-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:65b925cd044207a4a6b0c9e6320acb562aea785acc9917285cf6c21f5937b33d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.5 KB (389492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26cf4a59211c7a9624ce955760e04b3ea2b758258bf755afabf9bab559fce575`

```dockerfile
```

-	Layers:
	-	`sha256:97fa1e71cc31ea846bdaca09b38183dfe0c30eacdc9e34a18052054564981a36`  
		Last Modified: Wed, 24 Jul 2024 10:47:29 GMT  
		Size: 380.0 KB (380023 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d5f75a1081d6de7178bf721d9f89e18d5ff77f580791380c4e5fcad2177f65c`  
		Last Modified: Wed, 24 Jul 2024 10:47:28 GMT  
		Size: 9.5 KB (9469 bytes)  
		MIME: application/vnd.in-toto+json
