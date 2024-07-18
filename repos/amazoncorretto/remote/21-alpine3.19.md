## `amazoncorretto:21-alpine3.19`

```console
$ docker pull amazoncorretto@sha256:dc31a5672f862b5fc2cd54fc4ac76057e5867eb5e995abab3fc3a3dc2ddc0575
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-alpine3.19` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:b20ca1881635fca829474e2f7ab6b1be73c58217eba789232a8ffaae4e2cb4c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.1 MB (163143296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3d9221caefdcbaa32d9c0e9d3ed8e62abccc5750cee23f3e05fe6b76f689583`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 20 Jun 2024 20:17:04 GMT
ADD file:fb066571462e703f86645131b43d211ff8531ffac77ea394456bfe569a6f17fe in / 
# Thu, 20 Jun 2024 20:17:04 GMT
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
	-	`sha256:b84a74cde5af5c5199bfc2ce2a8c8951a29a7716d17327e923f1a14c870a858b`  
		Last Modified: Thu, 20 Jun 2024 20:17:43 GMT  
		Size: 3.4 MB (3417332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19830f1258e542f8262eeb32eac6af9d4df21f637a6a5e29cc1add035bb862a1`  
		Last Modified: Thu, 18 Jul 2024 00:56:10 GMT  
		Size: 159.7 MB (159725964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.19` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:60f24cf2d1b675d0185c2915208a215e1e0cf5591541becb21b000a662595fe4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **390.5 KB (390482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e99680c1d2b0915bf3920c65af4cee55e578be7fab62c48b7912a4f439017687`

```dockerfile
```

-	Layers:
	-	`sha256:8e9d4411447105fe7811aea815f569709d79319338ac40bcb0d0a500b02fe445`  
		Last Modified: Thu, 18 Jul 2024 00:56:06 GMT  
		Size: 381.3 KB (381313 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16554ebf11b9ead2af1b7b7bba7e5550224f14c5d9999ac8c75814eee1c93ceb`  
		Last Modified: Thu, 18 Jul 2024 00:56:05 GMT  
		Size: 9.2 KB (9169 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:08c4b81d35c3cab2882592b981c3cc30744cedabebdd1690fa417ca2c6e20eda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.8 MB (160838720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ea9fc07f68b7a6244a8c12d47b90366e68cc5d2984e4339e8f490a7106e7283`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:38 GMT
ADD file:f5632bd5469a9b26f7ff1739bb0b5dd166613259104f7bf76d587a8a428debcc in / 
# Thu, 20 Jun 2024 17:40:38 GMT
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
	-	`sha256:d4f2d2bd5ed999e04bfbfb910f14154b488ad32abf053954bff805f47fc3ad1e`  
		Last Modified: Thu, 20 Jun 2024 17:41:12 GMT  
		Size: 3.4 MB (3357202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3909d3a08ac7e7c9504b02289d97eb4ffc88bcaa132e0f6bb3a18151a685e372`  
		Last Modified: Thu, 18 Jul 2024 01:23:51 GMT  
		Size: 157.5 MB (157481518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.19` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:d60b67f79b1dc4ec2680b8e2202b7e3f36bfe47bac345d884b57545ecadc6acf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **390.2 KB (390200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac3369097b8f1f02399266bed9a60529fda4d0be343d0027b76d4b24e28a20c0`

```dockerfile
```

-	Layers:
	-	`sha256:9a1d26818aa178045db46f2a6e0a7f6290e589390d34b271df7ff844858b6a3e`  
		Last Modified: Thu, 18 Jul 2024 01:23:46 GMT  
		Size: 380.7 KB (380731 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:714e7d6370d6f4a495121aafd764eb0073a6406a7143595d89183a0be7b531ea`  
		Last Modified: Thu, 18 Jul 2024 01:23:45 GMT  
		Size: 9.5 KB (9469 bytes)  
		MIME: application/vnd.in-toto+json
