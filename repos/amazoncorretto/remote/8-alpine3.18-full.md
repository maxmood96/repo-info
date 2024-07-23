## `amazoncorretto:8-alpine3.18-full`

```console
$ docker pull amazoncorretto@sha256:2627aeffc21d4a14e1bd76f7986e233ce4c77499a38c36f977f2b45bf0d58ff6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-alpine3.18-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:76d56c0616d5940859d242357a7a421b26d4d8eaefe5babfac5fdf0c9fc4c941
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.5 MB (103539380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c403c0e785e22ca87c8930fd308b1e84854022d90738bd00d983c447b1ca6032`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
ADD file:5851aef23205a072ef361dd412a73a39a1ada75e19a207a392bb7ec9b8556e11 in / 
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/sh"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=8.422.05.1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=8.422.05.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
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
	-	`sha256:8990b85602c9da3cabeb1d1f5ce449a184f9e5c23a1a35cabb12e0af22367d8b`  
		Last Modified: Mon, 22 Jul 2024 23:04:28 GMT  
		Size: 100.1 MB (100123740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.18-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:530a6b52f98dab20964d3ede202cf302d7d0e31b60b5d3ae9989d170632e57e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.2 KB (254228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16c5980b47c1d2fae16abbc5c2ff1d8898f4003c9e23f4ddc41d3210eea28ae2`

```dockerfile
```

-	Layers:
	-	`sha256:85909688b4e7f2505d835fd22cbf510e72870ff43b992624af8f05c67ed079e6`  
		Last Modified: Mon, 22 Jul 2024 23:04:25 GMT  
		Size: 245.1 KB (245075 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:523e21ebacbb9bc3a69b12fadd9ee1c581b9bdaee77b7dab066a60cc9020fcdc`  
		Last Modified: Mon, 22 Jul 2024 23:04:25 GMT  
		Size: 9.2 KB (9153 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-alpine3.18-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:dd8ccef4d6b11834ca7e2fcee22e9e8e68cc2a0d4602e4d2afc0b7e6d8cdafee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.2 MB (103173941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5621346e21991e17fc40bb2ca0c0be479bb53ccc5a4044e11209a502a98d380c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:41 GMT
ADD file:4f760ede9d48d6073317cae6d632deaab101f337e09c56a7f9b8847ed99de3e8 in / 
# Thu, 20 Jun 2024 17:40:42 GMT
CMD ["/bin/sh"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=8.422.05.1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=8.422.05.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
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
	-	`sha256:9c04b30fdfb8a5255460d6460daf4c158b9475d10c9984ac2c27ba122288c493`  
		Last Modified: Thu, 18 Jul 2024 00:59:33 GMT  
		Size: 99.8 MB (99835992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.18-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:e2b9bf2bea95157d02935c597d3ec8889cc107b97c7a8e3c50a1fd2756db6522
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.7 KB (254658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d40003049117436760222466945828014dfec178f9d0c66815d52332d2ac023f`

```dockerfile
```

-	Layers:
	-	`sha256:ffae89ce09131de33b80f9bc0464e730a64b0349082171a4d580eca52f94135e`  
		Last Modified: Thu, 18 Jul 2024 00:59:30 GMT  
		Size: 245.2 KB (245207 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7befc2a83a7371f9b8976247ea52392046b4ac34551cba3251f7532e04be242`  
		Last Modified: Thu, 18 Jul 2024 00:59:30 GMT  
		Size: 9.5 KB (9451 bytes)  
		MIME: application/vnd.in-toto+json
