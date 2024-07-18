## `amazoncorretto:11-alpine3.18-full`

```console
$ docker pull amazoncorretto@sha256:e947153c36a65debf581d4e762b7d338ede452010cfa69f0f9183410e0065263
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-alpine3.18-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:ee4690dbe3d6cb73886511f510479076c419feb7d2e919a70911fa9ad3b9507f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.2 MB (145224749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af56d4465b2a622dd6fad52fddc73c42850f55fd5451f9eed92e68a51513ac18`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 20 Jun 2024 20:17:10 GMT
ADD file:aa183dc07d0f6a47c02f7f1388fa0ce4639ad328111172149be7c7c65d634ded in / 
# Thu, 20 Jun 2024 20:17:10 GMT
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
	-	`sha256:73baa7ef167e70f1c0233fe09e741780d780ea16e78b3c1b6f4216e2afbbd03e`  
		Last Modified: Thu, 20 Jun 2024 20:17:53 GMT  
		Size: 3.4 MB (3413894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00c986db3c69bd1a61740eb9c7784c9b0d4d7e132181aa15a193f45fda3e69d6`  
		Last Modified: Thu, 18 Jul 2024 00:55:54 GMT  
		Size: 141.8 MB (141810855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.18-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:7ec44b49222b7240b60fdb1827a169e495e87580c859312edbf48c20888ebd0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.7 KB (396736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3903940273af5d1b04cb69a3b091590c1689da5b9343dd7bf176fd266b7f8099`

```dockerfile
```

-	Layers:
	-	`sha256:5e346f40b1c9684cacf1e347e27053fd5cf1a25541471ee4e5b4483e5b2b9890`  
		Last Modified: Thu, 18 Jul 2024 00:55:51 GMT  
		Size: 387.6 KB (387564 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22c6ab526068585882bfca602f37aff01421cceea549d35a3c734b8bb5bb52a5`  
		Last Modified: Thu, 18 Jul 2024 00:55:51 GMT  
		Size: 9.2 KB (9172 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-alpine3.18-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:4373cf7885ea4594baca019f1df346859fd6a92c88d721068ad0555801106cb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.3 MB (143296619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8ef61a47b5ab53255ef7a1650e23392106cd1eda4d684ff16217b8b4752a6ef`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:41 GMT
ADD file:4f760ede9d48d6073317cae6d632deaab101f337e09c56a7f9b8847ed99de3e8 in / 
# Thu, 20 Jun 2024 17:40:42 GMT
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
	-	`sha256:5c905c7ebe2fecec0b1115f145c0ea74b3233aa25d8239903194f6b4424044ce`  
		Last Modified: Thu, 20 Jun 2024 17:41:31 GMT  
		Size: 3.3 MB (3337949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b7fa32e2951fc217b580e96c36ccbaecabf2fee82783d3a7dc2ebbf64b91e2`  
		Last Modified: Thu, 18 Jul 2024 01:08:32 GMT  
		Size: 140.0 MB (139958670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.18-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:a9367b255484e79d7460b8a27adc13f8e10537f02e2699cbac8c01578796d869
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **397.1 KB (397092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91402fcae7d08e56945b5e0bf745448ec6d9d20c9277b2c8086b94563787ec44`

```dockerfile
```

-	Layers:
	-	`sha256:433703e9c600285010ce840bceb7baa9afa5f5486cbc283f672dfac61d27d407`  
		Last Modified: Thu, 18 Jul 2024 01:08:29 GMT  
		Size: 387.6 KB (387620 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1c3c3de84a3d19db5b1002b1679c2a597b6087593c9abd8ed408a6f556affe6`  
		Last Modified: Thu, 18 Jul 2024 01:08:28 GMT  
		Size: 9.5 KB (9472 bytes)  
		MIME: application/vnd.in-toto+json
