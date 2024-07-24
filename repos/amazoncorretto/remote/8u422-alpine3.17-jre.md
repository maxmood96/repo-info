## `amazoncorretto:8u422-alpine3.17-jre`

```console
$ docker pull amazoncorretto@sha256:f6bb2758ac37c8ec68eeeea731d100f7dbc99aad1431a479bbb55a0363443b60
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u422-alpine3.17-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:bbac661707743546844df332a3996a3671edcb36534e04fddd7a7715cacb0308
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.0 MB (44991365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:233da5cd4232f5553619e24e5f37339109b6b5d71b5b92fd90283ba67ec7fd79`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
ADD file:ec892b6986dac395477ae6947272ea0913b711cda60bbd7d575b374ecfc4cee2 in / 
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/sh"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=8.422.05.1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=8.422.05.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:b99da37831f37d3f77de0ac7a864f9b69f1dbb4461e5ddfe5a3c2b7e2a3586c5`  
		Last Modified: Mon, 22 Jul 2024 22:27:42 GMT  
		Size: 3.4 MB (3391983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74ec8924afc6ffd5fdc2c2074136d72927592514dab5c0d02b9cd2ea10b75ca0`  
		Last Modified: Mon, 22 Jul 2024 23:04:23 GMT  
		Size: 41.6 MB (41599382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u422-alpine3.17-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:a3cf7d60e568bcc07285d83bb6dd3907588dbd4418f57e7e9d73ae1f0f1ae6df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.6 KB (192578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe098e9a4b6274a4289a520624bdea69ebbb8bc6a14a8623f5733d8d9e328951`

```dockerfile
```

-	Layers:
	-	`sha256:b2c1a3279bc1cb71a9f0fef4155033284ffb5250a4f641b5289fee8b07f83387`  
		Last Modified: Mon, 22 Jul 2024 23:04:23 GMT  
		Size: 184.1 KB (184124 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4f1f02b9ad3e2bab6f3bd0cf73803968137e2862ce055481c507d52b5999fa5`  
		Last Modified: Mon, 22 Jul 2024 23:04:23 GMT  
		Size: 8.5 KB (8454 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u422-alpine3.17-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:9e236acb9e4b8e2cf707ac3118c05f6e0a3105d096b90744630f62a40a0abd45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.6 MB (44580326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c8dc37c5cc3ac18800275047ecdc0cc25569e9237acac9a0598eccc61fcbbc5`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
ADD file:768e36150231c818b6707881e3060e9adfe496d4c48c00b59a05eecb16923c3d in / 
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/sh"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=8.422.05.1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=8.422.05.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:dba698d60556788613e51a85af8ac1331430729add60c326c10517189222232c`  
		Last Modified: Mon, 22 Jul 2024 21:45:05 GMT  
		Size: 3.3 MB (3274245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fa31a9ea9612de322ae4d1a329e36cd10d3b04855a66493f451182717ea570e`  
		Last Modified: Wed, 24 Jul 2024 10:37:15 GMT  
		Size: 41.3 MB (41306081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u422-alpine3.17-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:6aadaabe5d6dfc8f311160018821a6ccd9a1731ea015d43269e89cb00010045c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.0 KB (192961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbc96d53b1b8e7e2e5bac86ffc7a09d7f74ec4abbffb3d5225e9394aaeacfcd0`

```dockerfile
```

-	Layers:
	-	`sha256:32640e4fecab85ade108d9a3ec7a9ae7d2f32e02e3703dcf5ab7301092eb5280`  
		Last Modified: Wed, 24 Jul 2024 10:37:14 GMT  
		Size: 184.2 KB (184232 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8590465f6e94e7f13f8eff8cc12206a14d8fc0d627cb5a0eb52ff6a23f49f64`  
		Last Modified: Wed, 24 Jul 2024 10:37:14 GMT  
		Size: 8.7 KB (8729 bytes)  
		MIME: application/vnd.in-toto+json
