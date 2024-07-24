## `amazoncorretto:11-alpine3.20-jdk`

```console
$ docker pull amazoncorretto@sha256:057c1b725f9ce1e48422d58009ae7d779ac6db5d4c59d6584e241ee46431f3f6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-alpine3.20-jdk` - linux; amd64

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

### `amazoncorretto:11-alpine3.20-jdk` - unknown; unknown

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

### `amazoncorretto:11-alpine3.20-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:f034e0373f4794367f6a122732866204a4cd4f417056f93050fd4b2c0b15f0b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.0 MB (144046665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8443866afadc2eadc3b930e9ed1c500238aa4adc097e43be4ab59f0305ec8188`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
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
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f61e4d063d408aaa3bd545c1353b34fc7e9cf477360f91a0948870c1712e9f16`  
		Last Modified: Wed, 24 Jul 2024 10:41:50 GMT  
		Size: 140.0 MB (139959731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.20-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:1df7349a9f3be91b0eb2a97fda4f240b25a6a45aeb8b50927209123ab7cf494c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.2 KB (396227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83d311134f8f7b55657f8db5272d2f703005fcfaf60bb3e2b908cd5730316122`

```dockerfile
```

-	Layers:
	-	`sha256:71ba6227018bfc7d05fa632ddd487b57b9fb52445bf228763ea9ba24b9418971`  
		Last Modified: Wed, 24 Jul 2024 10:41:47 GMT  
		Size: 385.4 KB (385401 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0e2d972becb8530f9274a6ffcf3472c5b5340bbcea6901d01c278889d4a926b`  
		Last Modified: Wed, 24 Jul 2024 10:41:46 GMT  
		Size: 10.8 KB (10826 bytes)  
		MIME: application/vnd.in-toto+json
