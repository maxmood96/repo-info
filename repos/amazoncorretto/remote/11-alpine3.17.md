## `amazoncorretto:11-alpine3.17`

```console
$ docker pull amazoncorretto@sha256:d9aa1163ff74dc4b073bfcecaf7f294b6e81d97d6ca1c70b34fb25cb0767f1cc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-alpine3.17` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:619e3f39cbd9b62bbf505ab426056baaf06eb2a3d8014a17bbf4f45cc5d64645
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.2 MB (145233585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:807a82e350aced5ab8c7efe1cda2481ea6c570d29cf2496eff865050a0958bc2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Apr 2024 21:21:40 GMT
ADD file:cbcddefa487fb5085857fbba16854e06e53f93295bbf36ef1968a0b89835cad7 in / 
# Tue, 16 Apr 2024 21:21:40 GMT
CMD ["/bin/sh"]
# Tue, 16 Apr 2024 21:21:40 GMT
ARG version=11.0.23.9.1
# Tue, 16 Apr 2024 21:21:40 GMT
# ARGS: version=11.0.23.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Apr 2024 21:21:40 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 21:21:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 16 Apr 2024 21:21:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:f9202480295a4ef9cc62343dea568a5840b58bc68a1970045d30f3077a46a471`  
		Last Modified: Thu, 20 Jun 2024 20:18:01 GMT  
		Size: 3.4 MB (3389963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da1bc8b47f3043c933c63d3ba934ce660ea0746611755a756d2bc617c048974`  
		Last Modified: Fri, 05 Jul 2024 19:56:16 GMT  
		Size: 141.8 MB (141843622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.17` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:22690dd436c9ce786584377d9c2354652d3be5f8c2650d68ce6d9bc345955856
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **392.1 KB (392111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:431f5cddb29fc1856d556125613570dfeb4808caf858af343bcbfc6c71bdf0aa`

```dockerfile
```

-	Layers:
	-	`sha256:af4ef5b1ad75974002a5875eb3c4f05c8fbd7ef778168f6677da7e0f9abb107a`  
		Last Modified: Fri, 05 Jul 2024 19:56:13 GMT  
		Size: 382.9 KB (382939 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90be2f4f2bba575f68b039f128e9855a844410cef437758f90e6d090e6fe3194`  
		Last Modified: Fri, 05 Jul 2024 19:56:13 GMT  
		Size: 9.2 KB (9172 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-alpine3.17` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:4d03d35ea1a7be6c2fc6f63b8faf9fe46944b70dd9c786d9ce0bccb03202ea92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.2 MB (143205131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5169959338567a4ce1db5930d4719fc3a0e6b67f2e078ac40b089e14818045c1`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Apr 2024 21:21:40 GMT
ADD file:deb5b1c3cd4e7a5be179620c767b9d7bfac29f2544596a65b760460e7a645c51 in / 
# Tue, 16 Apr 2024 21:21:40 GMT
CMD ["/bin/sh"]
# Tue, 16 Apr 2024 21:21:40 GMT
ARG version=11.0.23.9.1
# Tue, 16 Apr 2024 21:21:40 GMT
# ARGS: version=11.0.23.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Apr 2024 21:21:40 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 21:21:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 16 Apr 2024 21:21:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:e45a60384f0269bd8514e16cf71591639353996e62a144763c5e519b386ac31c`  
		Last Modified: Thu, 20 Jun 2024 17:41:39 GMT  
		Size: 3.3 MB (3272586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:161b48cb8b5adf73aa97abdf66d479a94923c3b933dbe6720c57a96ad9cf8cfa`  
		Last Modified: Fri, 05 Jul 2024 20:09:21 GMT  
		Size: 139.9 MB (139932545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.17` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:a9c3447ae20b8aa2aec971553b8c4a3c3106d59f130a0fea2aaaf558dd5af1aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **392.5 KB (392466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e81a4c0ebbd2aeefb06935773019923ec0ff2aa3605abd8954fc8d2ae4bb9033`

```dockerfile
```

-	Layers:
	-	`sha256:dc5083b8e02395a3e4dc989be3b61739302771b221242c3eedcf3aa3844dea32`  
		Last Modified: Fri, 05 Jul 2024 20:09:18 GMT  
		Size: 383.0 KB (382995 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e1fb2cc5ec5c8634325a646393e4bf5229d26a850d828c3358c52fe9088ac94`  
		Last Modified: Fri, 05 Jul 2024 20:09:17 GMT  
		Size: 9.5 KB (9471 bytes)  
		MIME: application/vnd.in-toto+json
