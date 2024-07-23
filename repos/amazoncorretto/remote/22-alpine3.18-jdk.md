## `amazoncorretto:22-alpine3.18-jdk`

```console
$ docker pull amazoncorretto@sha256:6263f8dd86aa1b46ce507e3a11db0727ea8104bc30bc6d49f65f008ebace3bd0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:22-alpine3.18-jdk` - linux; amd64

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

### `amazoncorretto:22-alpine3.18-jdk` - unknown; unknown

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

### `amazoncorretto:22-alpine3.18-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:098a313fdd8abeafd96ad1eb32333f0a805f0bc4480ce66e778c7e8e17ab09e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.5 MB (158532602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e46f69209d58678890a43cb5d0c9324694519e19a30cb4596e995b98717da758`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:41 GMT
ADD file:4f760ede9d48d6073317cae6d632deaab101f337e09c56a7f9b8847ed99de3e8 in / 
# Thu, 20 Jun 2024 17:40:42 GMT
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
	-	`sha256:5c905c7ebe2fecec0b1115f145c0ea74b3233aa25d8239903194f6b4424044ce`  
		Last Modified: Thu, 20 Jun 2024 17:41:31 GMT  
		Size: 3.3 MB (3337949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:796cf498de94a64529afbb555d2b35f784240369fda345d6654c4fee91087337`  
		Last Modified: Thu, 18 Jul 2024 01:29:23 GMT  
		Size: 155.2 MB (155194653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:22-alpine3.18-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:606d623ec3b0b384e5568e3b3306b29f13d4bb33a802c6c5fb00c72073038695
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.5 KB (389492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:163ce0b81e013bd6e4c0b8159f2950882c0e959666bb119cf6f91ae41b858b47`

```dockerfile
```

-	Layers:
	-	`sha256:42d9219874226c8f4ae5d2b17f53341fad24b84557092a93dcb68214aef98157`  
		Last Modified: Thu, 18 Jul 2024 01:29:19 GMT  
		Size: 380.0 KB (380023 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17fb05fda2364df2d4628eab358f8fa986f416e3ac2dd409c8c972db588f6ec7`  
		Last Modified: Thu, 18 Jul 2024 01:29:19 GMT  
		Size: 9.5 KB (9469 bytes)  
		MIME: application/vnd.in-toto+json
