## `amazoncorretto:8u412-alpine3.18-jre`

```console
$ docker pull amazoncorretto@sha256:a15fab65baf39dc2beedd118c97a1e932876dfff0b172a6fb48bff1df04b8181
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u412-alpine3.18-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:f7b486f77c80db5e0572c8ffd9eafef5ddc20460be6fa118dffe9d3d7978a6ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.1 MB (45061352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29e0bfb070d7fc78bac1df46a192851fbbf4b7e2a616bbc8c59317505d108364`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Apr 2024 21:21:40 GMT
ADD file:aa183dc07d0f6a47c02f7f1388fa0ce4639ad328111172149be7c7c65d634ded in / 
# Tue, 16 Apr 2024 21:21:40 GMT
CMD ["/bin/sh"]
# Tue, 16 Apr 2024 21:21:40 GMT
ARG version=8.412.08.1
# Tue, 16 Apr 2024 21:21:40 GMT
# ARGS: version=8.412.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Apr 2024 21:21:40 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 21:21:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:73baa7ef167e70f1c0233fe09e741780d780ea16e78b3c1b6f4216e2afbbd03e`  
		Last Modified: Thu, 20 Jun 2024 20:17:53 GMT  
		Size: 3.4 MB (3413894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b0d93262c1d13bd76bf71a6bb3ded38a4f16240b3316d2609445e6ddb06931a`  
		Last Modified: Fri, 05 Jul 2024 19:55:59 GMT  
		Size: 41.6 MB (41647458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u412-alpine3.18-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:a2c9bb9d8f69fdd75bbccf75c0a875efb0733f1ee36cc1670018d6646db8cbbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.2 KB (187232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08e87ee352ff141e0bdc22cf9b9490dbd6f2f1b6654805551d25d96a8525f55b`

```dockerfile
```

-	Layers:
	-	`sha256:cc7512ca734dd9a7f3e0689f12c1d1497b42337de780f28a988fdeed126754a2`  
		Last Modified: Fri, 05 Jul 2024 19:55:58 GMT  
		Size: 178.8 KB (178778 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb9cea0cdf68173f52ef51ecb2866c65cae336ba805d916e4c541d4f43947f44`  
		Last Modified: Fri, 05 Jul 2024 19:55:58 GMT  
		Size: 8.5 KB (8454 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u412-alpine3.18-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:bc516b9199489dbc79e4e5c7dbe4cc0ef74a015a994dcae3be6f0cf57549dd5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.6 MB (44637794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:404a2c1a9594fa07c0fa4bd77a1ce8558dcd5ed6110254c365f32de2cc5952d8`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Apr 2024 21:21:40 GMT
ADD file:4f760ede9d48d6073317cae6d632deaab101f337e09c56a7f9b8847ed99de3e8 in / 
# Tue, 16 Apr 2024 21:21:40 GMT
CMD ["/bin/sh"]
# Tue, 16 Apr 2024 21:21:40 GMT
ARG version=8.412.08.1
# Tue, 16 Apr 2024 21:21:40 GMT
# ARGS: version=8.412.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Apr 2024 21:21:40 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 21:21:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:5c905c7ebe2fecec0b1115f145c0ea74b3233aa25d8239903194f6b4424044ce`  
		Last Modified: Thu, 20 Jun 2024 17:41:31 GMT  
		Size: 3.3 MB (3337949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b832afec1943343ea65b13897a5214eb5d11d5aead71ca10fe4504f11e4337`  
		Last Modified: Fri, 05 Jul 2024 20:01:39 GMT  
		Size: 41.3 MB (41299845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u412-alpine3.18-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:2437134d70873aaa7f318e7e7c1d4edd18e0e5af81ca69c0ff99e47da85c6ba5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.6 KB (187616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e72da7a2b918f708ff8b64077931cc558928ac3c5b1794ea4e3b81355034b008`

```dockerfile
```

-	Layers:
	-	`sha256:ec09ca2ea824bf0cde2d37584f5e2f7f140ee10afcd78371bb2b82585ca2eac8`  
		Last Modified: Fri, 05 Jul 2024 20:01:38 GMT  
		Size: 178.9 KB (178886 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb02cd6434d39ff531d680eb2c7df9b02632a9e393a4a34c8167df0a49227754`  
		Last Modified: Fri, 05 Jul 2024 20:01:38 GMT  
		Size: 8.7 KB (8730 bytes)  
		MIME: application/vnd.in-toto+json
