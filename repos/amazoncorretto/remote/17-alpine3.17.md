## `amazoncorretto:17-alpine3.17`

```console
$ docker pull amazoncorretto@sha256:a95eb5c7b6768b3f55888917b2f2137a46d66da76d9f814673b42272316ccb52
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-alpine3.17` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:92837c93a246da15d87e755d186f4a6dca48573387800359f4b712864fa32ff7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.4 MB (149410083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78264e07206ed2affc57ffae5467bba54fc226fbfc4f0bfec3602def2bf566a5`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
ADD file:ec892b6986dac395477ae6947272ea0913b711cda60bbd7d575b374ecfc4cee2 in / 
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/sh"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=17.0.12.7.1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=17.0.12.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 16 Jul 2024 22:56:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:b99da37831f37d3f77de0ac7a864f9b69f1dbb4461e5ddfe5a3c2b7e2a3586c5`  
		Last Modified: Mon, 22 Jul 2024 22:27:42 GMT  
		Size: 3.4 MB (3391983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e198c571710c938bf0b2faf75109a974637790cd534f60ed8ab61cffdac00b70`  
		Last Modified: Mon, 22 Jul 2024 23:04:43 GMT  
		Size: 146.0 MB (146018100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.17` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:6d9490de5b88fda97e3461cbbd84a54eb64c780a4f2f020c18a44ca155750a98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **388.7 KB (388673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da6289208c0398b63d0215fc61f06f38ebb49b79ddd8eed29b064b1b51a48ab1`

```dockerfile
```

-	Layers:
	-	`sha256:533b55f51cf24a898908df4198c7961f852167ce0e2669522e9e9d8c97e6bcb1`  
		Last Modified: Mon, 22 Jul 2024 23:04:42 GMT  
		Size: 379.5 KB (379501 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff84d1b42c4c9c94fa4323ea2aad397666bb22096874e1b296dec81176dbdc1e`  
		Last Modified: Mon, 22 Jul 2024 23:04:41 GMT  
		Size: 9.2 KB (9172 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-alpine3.17` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:e3d70ce879996b01af72714190d02feea29adb40e38bad066ba70a38c1c55f7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.6 MB (147623511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7881df873c80f5991af8d8e9d6d89bf24e65c06e9a76b5eb9bbf3e6f647189eb`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:45 GMT
ADD file:deb5b1c3cd4e7a5be179620c767b9d7bfac29f2544596a65b760460e7a645c51 in / 
# Thu, 20 Jun 2024 17:40:45 GMT
CMD ["/bin/sh"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=17.0.12.7.1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=17.0.12.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 16 Jul 2024 22:56:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:e45a60384f0269bd8514e16cf71591639353996e62a144763c5e519b386ac31c`  
		Last Modified: Thu, 20 Jun 2024 17:41:39 GMT  
		Size: 3.3 MB (3272586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75035188f4768e3587991901f6eeb889b5d7f5fabb6016ea6d345358c93926da`  
		Last Modified: Thu, 18 Jul 2024 01:16:22 GMT  
		Size: 144.4 MB (144350925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.17` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:d0887cfc80b499f5b7ad36c857809ec6bd7c1b442dc4231bb069cdebfd4d1998
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **388.4 KB (388390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf8cbcc9cd056ca34e056beca90d6be439f196d1bbd5d1c59fb8db3832954951`

```dockerfile
```

-	Layers:
	-	`sha256:e464e80c91d8e7edd8e6d32fb4cf6bc6e11fdb7a33fa43651f7dbad4f7d0f244`  
		Last Modified: Thu, 18 Jul 2024 01:16:18 GMT  
		Size: 378.9 KB (378919 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:293b3050803a1f10b55cefaeec2ab35773e19e1a4b6a5e903fbb3e873d25e563`  
		Last Modified: Thu, 18 Jul 2024 01:16:18 GMT  
		Size: 9.5 KB (9471 bytes)  
		MIME: application/vnd.in-toto+json
