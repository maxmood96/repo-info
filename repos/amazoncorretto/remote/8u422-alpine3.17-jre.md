## `amazoncorretto:8u422-alpine3.17-jre`

```console
$ docker pull amazoncorretto@sha256:f7aeaeaf2811ed4c7ddc970409ea2b33de368007084af08d7cd68d0e32dbbe74
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u422-alpine3.17-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:729665f8e26af60540e8f84b7f4e8f7199568c0a1681113720f6f2c01b71e137
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.0 MB (44991614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:726f7705e4c8a8255c102f2b84f2a35f081699c198ae7770ba2a2be89b86c37b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
ADD file:8bf458f5fbed9f27c897506538c02fb5810b70aba850bb883d2120985fa15bac in / 
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
	-	`sha256:a0f4cbe03b6df9e61ce02b3c41bbc05481842858bd48d9687614abe719303b47`  
		Last Modified: Fri, 06 Sep 2024 22:21:07 GMT  
		Size: 3.4 MB (3392194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7ba0a91d42dd541325483d36a0605ecfcaffb51a2b0a5eb84e1a295de0c7453`  
		Last Modified: Fri, 06 Sep 2024 23:25:20 GMT  
		Size: 41.6 MB (41599420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u422-alpine3.17-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:033aa8cb4f449eee42ad159e5cea71c3be4c8063f7b9aa29baf757df31807b71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.6 KB (192578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e13a4a42b73f59028522609b37e16a69bda179471fc313339e9dd633d6180d0d`

```dockerfile
```

-	Layers:
	-	`sha256:0a9b2c9856b5ea22da2da46c4704166839af37d85de2d0578188e90cc322e503`  
		Last Modified: Fri, 06 Sep 2024 23:25:19 GMT  
		Size: 184.1 KB (184124 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8dbd4f56ec957737ff1f6f5c50cf55eca85a0662dd7508db72459fcd85d13c1e`  
		Last Modified: Fri, 06 Sep 2024 23:25:19 GMT  
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
