## `amazoncorretto:8u432-alpine3.18-jre`

```console
$ docker pull amazoncorretto@sha256:2e987ac35638d76563b068908e566603e295a5d5714dfe6e526dafedd6794ada
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u432-alpine3.18-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:eddddb43054c1b334b7e8c27f0e2a65f379dd7303c2b8b65281bd1d878a969c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.1 MB (45073905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e9ea8aa2c07e598d1d563666e247fcfea82155b1754bb60c49d4bdbf4ab0cb7`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
ADD alpine-minirootfs-3.18.11-x86_64.tar.gz / # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 23:01:14 GMT
ARG version=8.432.06.1
# Fri, 13 Dec 2024 23:01:14 GMT
# ARGS: version=8.432.06.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 23:01:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:f54a5150a7602eaef3169b83e73d5927b20aef2fcaefcba18b532bd63b328fff`  
		Last Modified: Wed, 08 Jan 2025 17:23:37 GMT  
		Size: 3.4 MB (3417974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9068ec254366c93ac680a0ec78689c76498a8c202b06a73f82e8e9f4b6c3f44c`  
		Last Modified: Wed, 08 Jan 2025 18:09:11 GMT  
		Size: 41.7 MB (41655931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u432-alpine3.18-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:9ed673d18e7a748509a7e06f59ced8306c3eb64ddcf10bf3905b16db8287c4ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.4 KB (193371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e198273a17510240e11c01357cb5645c58e3762ef92798f83672014c14302b3`

```dockerfile
```

-	Layers:
	-	`sha256:0794d4919e95c4ae6ce12bcafe7b9383c3ded31c9e8824225a51888c20d93543`  
		Last Modified: Wed, 08 Jan 2025 18:09:10 GMT  
		Size: 184.7 KB (184672 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c47461838e817c6d454974e4d1f407790cecb316d569c0e9c2b510a344b70e7`  
		Last Modified: Wed, 08 Jan 2025 18:09:10 GMT  
		Size: 8.7 KB (8699 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u432-alpine3.18-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:beeee777b4a523679f68037eea79ecdf74e10b1bb085da0a01d1b81f2e80c4e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.7 MB (44695749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2202faea9c6b070fc75e6ac9a22019f82738bc25b8ad7aafcc53752ebd6cdcc0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
ADD alpine-minirootfs-3.18.10-aarch64.tar.gz / # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 23:01:14 GMT
ARG version=8.432.06.1
# Fri, 13 Dec 2024 23:01:14 GMT
# ARGS: version=8.432.06.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 23:01:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:fb3f1f9d2d6533828602bbf29a9a8cc07ae4a2a3e88846100e68ce43a16d2932`  
		Last Modified: Tue, 07 Jan 2025 03:03:28 GMT  
		Size: 3.3 MB (3337435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fc8c5146f3ceaf4e1327bf197f506003cfb6dbbd7c6a7a227dd5a43076c03ba`  
		Last Modified: Tue, 07 Jan 2025 07:19:24 GMT  
		Size: 41.4 MB (41358314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u432-alpine3.18-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:2dc60183e5f9734e07b9e77117fdcf480862c26b68d59c86c4143e8d1cf33b7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.6 KB (193559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:978ef4105d5686963cfceb3701723bdef51de886f5a88f2c454e39ae5f4ac73e`

```dockerfile
```

-	Layers:
	-	`sha256:9e4df1f92daf4337a7cf1e0a90c5067e52da87b796ed4e27424ea38c20debb70`  
		Last Modified: Tue, 07 Jan 2025 07:19:22 GMT  
		Size: 184.8 KB (184780 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb62d355a2e418b6ce2f50d8ea6cd42b36c6e343ca04c568959baa554e81867b`  
		Last Modified: Tue, 07 Jan 2025 07:19:22 GMT  
		Size: 8.8 KB (8779 bytes)  
		MIME: application/vnd.in-toto+json
