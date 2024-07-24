## `amazoncorretto:8-alpine3.19-jre`

```console
$ docker pull amazoncorretto@sha256:c14fcf3e23c5f9c2369ebe163ad425ab770b07a6efb5ab1a286c76a4c9879549
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-alpine3.19-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:ae72b90c40be91f72b800cff3f3e1e63bb260215d4d2fc58618cee1421eb999e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.0 MB (45018454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e7b464eff0b39f057b41fbc5f32d1e6502ca0c18cf123fb3aff4aedcc4c0184`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
ADD file:c644b15c170e2ca46176a566910d40a21dce66518ed8fdfd34ebcf0e9dc90c55 in / 
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
	-	`sha256:46b060cc26202cf98e28414d790b5cabd67094bba50315a1ae2e9daf913fca4f`  
		Last Modified: Mon, 22 Jul 2024 22:27:25 GMT  
		Size: 3.4 MB (3419040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da3e4b582d4020819801a28793afe31df4dce59e98a1ef117ec217374425f59c`  
		Last Modified: Mon, 22 Jul 2024 23:04:22 GMT  
		Size: 41.6 MB (41599414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.19-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:865d84cbb70ececddaf3802bd118ea9ea8ea96c3b3d4d5051619e16f1ca2c64b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.8 KB (193840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bffa37e2eb8ea44fc658fb6a6c7765e78ecea95d26c79ca99c426a3cb821f00a`

```dockerfile
```

-	Layers:
	-	`sha256:4e4f1fcc1607ee570a382374cefa3fac5d251b170a0a5f18dc32f21a80ae232c`  
		Last Modified: Mon, 22 Jul 2024 23:04:21 GMT  
		Size: 185.4 KB (185386 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32b96b50db4e43f087ae9c3c2b12efb6bc42f1c3d58b8769dfa0b2883411ab33`  
		Last Modified: Mon, 22 Jul 2024 23:04:21 GMT  
		Size: 8.5 KB (8454 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-alpine3.19-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:9538a2b793ee93f06c2799f4b2670764e6c3c437abda5bf5f04bccbfdb34ffc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.7 MB (44664813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be80675ea7802c0be6238bb31af322e6a87ecd733eed3653fcea58ceb0b18192`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
ADD file:7990c7edbcf2739c4b2df767635f403325689f42de6e05e9d81a79fc719930c5 in / 
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
	-	`sha256:119661e64d8d593a625274dd829d8550c61de6dd5631287dfea42e99c1c2c736`  
		Last Modified: Mon, 22 Jul 2024 21:44:49 GMT  
		Size: 3.4 MB (3358458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fa05f4653f562974719f7a494477ed9b48d6e584aaa7240780c5808b0b31e4c`  
		Last Modified: Wed, 24 Jul 2024 16:29:00 GMT  
		Size: 41.3 MB (41306355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.19-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:71988921a0d7d96b0c7245ee783627a533f037475014cc50d442dcf7ba1bbcb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.2 KB (194223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f30a788467cbcca9f479d7e44137ee12e5ab9964813180cb9fc542494636f532`

```dockerfile
```

-	Layers:
	-	`sha256:93fb06ca027b1d33b593f8fd32e6a409a06a3cda8a8f98f89a11f8d0d5173e8d`  
		Last Modified: Wed, 24 Jul 2024 16:28:58 GMT  
		Size: 185.5 KB (185494 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40e5c47f21fb8fb8c3c161a15aff969b7694ede48954bd48a48ee4f5c1cb2558`  
		Last Modified: Wed, 24 Jul 2024 16:28:58 GMT  
		Size: 8.7 KB (8729 bytes)  
		MIME: application/vnd.in-toto+json
