## `amazoncorretto:11-alpine3.20`

```console
$ docker pull amazoncorretto@sha256:0515e75e5b9435dfc58212694655e26739ba3eecbf8823e26b22718666e28962
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-alpine3.20` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:4e95e7e83380ec680c61aeb7008075c9a151b82bf6aa100f0a1e62e041852ecc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.4 MB (145432493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c643f30b390358850dd2f5cb64ae6de4227dd7c24923c449b47da9136ee6c453`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Tue, 16 Jul 2024 22:56:42 GMT
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
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d2b2662e959ba759e59184c77c32f8ed52b44dab2d990f5480eaa88b4683662`  
		Last Modified: Tue, 23 Jul 2024 00:07:17 GMT  
		Size: 141.8 MB (141809601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.20` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:c524ae4da72f144e5b0052f36b58880a8a1cfc80b8d5ff5ed4835fabed10752d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **395.8 KB (395776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:845ce2231b87280b5aa58d0169783276456029dde6e7f738507b0e08e069ea8e`

```dockerfile
```

-	Layers:
	-	`sha256:400a1fe98685b88ac2ebbf111ec2172c75573e7ae4a02d258086df3962b84c5d`  
		Last Modified: Tue, 23 Jul 2024 00:07:15 GMT  
		Size: 385.3 KB (385297 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b00183862884534c29828d677730f7dae089e42ca5dec917976af2f6e4d23974`  
		Last Modified: Tue, 23 Jul 2024 00:07:15 GMT  
		Size: 10.5 KB (10479 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:9b8cf9616307a0e55d4e97702c094f844cce870ee66e852b66750a887a9d7e33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.0 MB (144048563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8581aa95eb3842aab16f64b7e74cd1bdeb46c508eb5e0123032933114993b6e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:35 GMT
ADD file:033626ac44156f3d5800a602c46870486b1492b9ba26096eaa66cceb6fcead77 in / 
# Thu, 20 Jun 2024 17:40:35 GMT
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
	-	`sha256:a258b2a6b59a7aa244d8ceab095c7f8df726f27075a69fca7ad8490f3f63148a`  
		Last Modified: Thu, 20 Jun 2024 17:40:58 GMT  
		Size: 4.1 MB (4088800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b7f671662efdec07e12943e980d93c7cee9250d19994bcd3624da20d98633ae`  
		Last Modified: Thu, 18 Jul 2024 02:14:35 GMT  
		Size: 140.0 MB (139959763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.20` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:e74b9065b5631d206dd733047f067e070b5fdfb2ca3379b7bf5a9f4e3fc5f631
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.2 KB (396227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:895bb56e69cfd9e0efc55137297fdee80eb6108438e781f4ea42df5906aff5a5`

```dockerfile
```

-	Layers:
	-	`sha256:9ff6c00cae50fc3e071b8f5ae0eeaba70d48bacc1b1a9b74ffde7cdff54c3135`  
		Last Modified: Thu, 18 Jul 2024 02:14:31 GMT  
		Size: 385.4 KB (385401 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5ba023f75922b48fdd9fe5d04ab7a81f5675ba70289ac2e9835ee8032355e2c`  
		Last Modified: Thu, 18 Jul 2024 02:14:31 GMT  
		Size: 10.8 KB (10826 bytes)  
		MIME: application/vnd.in-toto+json
