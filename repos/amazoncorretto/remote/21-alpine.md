## `amazoncorretto:21-alpine`

```console
$ docker pull amazoncorretto@sha256:4cff3d338418faa41a20bf384c7ed67b8a6897ce5ce0e3fecd7ea08c5c7a2909
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-alpine` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:8ab4d20d92e79a31319e76c9fabe8c8ed8084368553799a9c67af7d7c2ffda16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.3 MB (163348502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5454b242ea7d4dc8dd18697f2de16714e8c582d0f77260ca632e034242b535e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/sh"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=21.0.4.7.1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=21.0.4.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 16 Jul 2024 22:56:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4df7fa76b697f54cfbf0defe76cd93473de2381bbe2ac80ec721a68cc052f862`  
		Last Modified: Mon, 22 Jul 2024 23:04:52 GMT  
		Size: 159.7 MB (159725610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:3d76a79ac806b8da4efcf94bd5b8e14dcd69cb0e42a30e9aabe49ff0cc1e9f69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **388.9 KB (388859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48b691b0c21691fe40a61af89bc1bcb89b35947c278551466a5ee874e463aaf1`

```dockerfile
```

-	Layers:
	-	`sha256:b1bd2cc813f17b328dae22f100c3c3770c7b1b79328966aab7c6a8379df0f5a4`  
		Last Modified: Mon, 22 Jul 2024 23:04:50 GMT  
		Size: 378.4 KB (378384 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1225e203a8706b8a1a3301d741e527bf31e4e3cf425165e24ec10865cb59bf2c`  
		Last Modified: Mon, 22 Jul 2024 23:04:49 GMT  
		Size: 10.5 KB (10475 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-alpine` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:eb70f499555922ea86da58e01cc655f920de6d6cb3e4de7a97661a895afd2d9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.6 MB (161568832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29a3e7dace234afe17cbac4be72b0264651597652de9f8fe893cd445dbdf29a4`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/sh"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=21.0.4.7.1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=21.0.4.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
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
	-	`sha256:5e7643ad6a283ce9aa47deec1fb3caa483a54533735f67fb3f6d2276e43ccc2d`  
		Last Modified: Wed, 24 Jul 2024 10:46:18 GMT  
		Size: 157.5 MB (157481898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:123c1e904f6bcf204c26a13cbd40ba1d67f3b80fe9cc7627d1de010e0f5fb0b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **388.7 KB (388673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e39ba8bd8ca44332ecc40c32f643da9656069b25fac9dee203d7f4ecfc8182e1`

```dockerfile
```

-	Layers:
	-	`sha256:7a7c7d91ce4b23b3da2fbfa01bac25abf8c5ff4d184715e614f8156d28388c46`  
		Last Modified: Wed, 24 Jul 2024 10:46:14 GMT  
		Size: 377.9 KB (377850 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1279d1924335d40dd5e79d7a7fcba4ab3ab537fc0bfd7f3a9a607c72dbc98987`  
		Last Modified: Wed, 24 Jul 2024 10:46:14 GMT  
		Size: 10.8 KB (10823 bytes)  
		MIME: application/vnd.in-toto+json
