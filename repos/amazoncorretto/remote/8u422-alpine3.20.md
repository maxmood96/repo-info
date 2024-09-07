## `amazoncorretto:8u422-alpine3.20`

```console
$ docker pull amazoncorretto@sha256:e4120480e7570ce2d7a540fd497d60e9ba59a270f207c56192af72ea8479cae0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u422-alpine3.20` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:3bd5ac6209e70d59953dd15f496204c3016ae23a5c671e4531183d5de5074d90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.7 MB (103747598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87de4679254064d06d1b92661b4217f06803579db1ae6790790e25582ba96e46`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
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
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37acea8028a4fbb47d620368843704b3220d4e77d3859fd1ae39012514b5d4b4`  
		Last Modified: Fri, 06 Sep 2024 23:17:08 GMT  
		Size: 100.1 MB (100123791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u422-alpine3.20` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:544bd4ccfd438a4870a1617d98f887566f087cb91a30c4e940773216859b3fe2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.2 KB (253248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2afc9c1a28ba2af3962eb97c736cbbfa8fc38e03707400a3bbfff4fb6c7d0259`

```dockerfile
```

-	Layers:
	-	`sha256:fa2c3f67497c223113795b5a847f216ed958dfc3d8d6a69000f8c968f91ad0aa`  
		Last Modified: Fri, 06 Sep 2024 23:17:05 GMT  
		Size: 242.8 KB (242798 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3b07c3ba4fa594b2f43ca8e804fee1ba085bed0a5d8512edeb2b27ce201fc89`  
		Last Modified: Fri, 06 Sep 2024 23:17:05 GMT  
		Size: 10.4 KB (10450 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u422-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:6a05d74b96551dd2558bf1ae197529c333e5e1292d19e0864570f34085d48b40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.9 MB (103921748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ec016323c50d29cc34da9d04972cf5a570677529e73e74b1e641401014bc092`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
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
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14f0bc26a341945105003a0d32c6400f67ebb4815afe0b531e1a808bbc2b61c7`  
		Last Modified: Wed, 24 Jul 2024 16:29:28 GMT  
		Size: 99.8 MB (99834814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u422-alpine3.20` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:2d5a45dd19fa700f54f0cc3aab9589ea4a96a6b3a000fd223c2f9490a8dcd992
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.8 KB (253776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14d6ba57480146ede2f33e6f66435971dbcfcd3dcc35a272aed7e0b6408caa2b`

```dockerfile
```

-	Layers:
	-	`sha256:5d68bf2561d79d68c3a3ca581e760c0823a6cbcb508b3501c469facac8bc2108`  
		Last Modified: Wed, 24 Jul 2024 16:29:26 GMT  
		Size: 243.0 KB (242978 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81a18af9d6cf333fdb604f8a6c88e88b1556ea9fae5ec775895bbd689f53def2`  
		Last Modified: Wed, 24 Jul 2024 16:29:26 GMT  
		Size: 10.8 KB (10798 bytes)  
		MIME: application/vnd.in-toto+json
