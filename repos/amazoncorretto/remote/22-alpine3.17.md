## `amazoncorretto:22-alpine3.17`

```console
$ docker pull amazoncorretto@sha256:3341aa92173a49743871a04f55fc48612f9614e439e4f836abe611ae020c3cf3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:22-alpine3.17` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:4a998972556938c6356d42a32d67d7d74fe773c4ca08d204c867fdf3e7530cf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.0 MB (160988490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53a62801a4561aabdfc09a385f1ba2427f46bdae2ec37176a185bc19e05c4786`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
ADD file:8bf458f5fbed9f27c897506538c02fb5810b70aba850bb883d2120985fa15bac in / 
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
	-	`sha256:a0f4cbe03b6df9e61ce02b3c41bbc05481842858bd48d9687614abe719303b47`  
		Last Modified: Fri, 06 Sep 2024 22:21:07 GMT  
		Size: 3.4 MB (3392194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2070609f4ddfba2339ca57ec7fac4081579674109d577d149046e5a034da929e`  
		Last Modified: Fri, 06 Sep 2024 23:18:04 GMT  
		Size: 157.6 MB (157596296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:22-alpine3.17` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:860c5417c6aa8baecd232912296055748ce19fe564524286e6833860f1f4f5ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.8 KB (389813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3cb39f2c84a0bb4234fad156e773270ef743c1b29b4d2a03d7da70bb7d5349c`

```dockerfile
```

-	Layers:
	-	`sha256:38c544710f0e4440d14b1425ad195b952bc96f92f0a8b8cef8aa2994b6d0c05a`  
		Last Modified: Fri, 06 Sep 2024 23:18:00 GMT  
		Size: 380.6 KB (380644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee7ba9c29ec44af9343ef6478cf541ed901b7c79a10bd4c9bead4639b7d31360`  
		Last Modified: Fri, 06 Sep 2024 23:18:00 GMT  
		Size: 9.2 KB (9169 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:22-alpine3.17` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:66bb320b05494ea19bdcca779e73808847d627b50f07c6a3474af10c2bc740f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.5 MB (158469115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9257eb18a017a7f9d31e3a5c3a3a7a06628686c16e2bd31ea233c0d9f1d43bd`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
ADD file:768e36150231c818b6707881e3060e9adfe496d4c48c00b59a05eecb16923c3d in / 
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
	-	`sha256:dba698d60556788613e51a85af8ac1331430729add60c326c10517189222232c`  
		Last Modified: Mon, 22 Jul 2024 21:45:05 GMT  
		Size: 3.3 MB (3274245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7359796ec1e1b3ece216367679f0bd764dd2f049fc6a150ea888707c1d7844b`  
		Last Modified: Wed, 24 Jul 2024 10:46:56 GMT  
		Size: 155.2 MB (155194870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:22-alpine3.17` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:4e5d007a1be191b34465d9a435b40d039a496e060554adf8cd9fae6353894798
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **388.9 KB (388889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a9b05521b7739abb7200ff741afee8dae68e6c568b5e69d3626d5d97db323c6`

```dockerfile
```

-	Layers:
	-	`sha256:912d0bb82c9505ff203eb95eb3886a91c5aed73733fa4526c4667c69e60785d2`  
		Last Modified: Wed, 24 Jul 2024 10:46:52 GMT  
		Size: 379.4 KB (379421 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:769e9b386ab5f5332565373dd70ecd6e879d2860e5b1fea7091c35090c8567c2`  
		Last Modified: Wed, 24 Jul 2024 10:46:52 GMT  
		Size: 9.5 KB (9468 bytes)  
		MIME: application/vnd.in-toto+json
