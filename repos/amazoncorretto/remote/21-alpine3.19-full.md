## `amazoncorretto:21-alpine3.19-full`

```console
$ docker pull amazoncorretto@sha256:11336bee541785bbd712cdf66b1e79a4f09921693c7365efe586ac0fd43ee525
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-alpine3.19-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:5f84f8374758f707021e153b7d892acd3c28e5a58b2952faefe120f00a10e7ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.0 MB (164986606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6a90accdcfca5a220a4e373e1027209055380118fd164a53b8c18537eddbaed`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:10:40 GMT
ADD alpine-minirootfs-3.19.9-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:10:40 GMT
CMD ["/bin/sh"]
# Tue, 21 Oct 2025 20:48:19 GMT
ARG version=21.0.9.10.1
# Tue, 21 Oct 2025 20:48:19 GMT
# ARGS: version=21.0.9.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Tue, 21 Oct 2025 20:48:19 GMT
ENV LANG=C.UTF-8
# Tue, 21 Oct 2025 20:48:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 21 Oct 2025 20:48:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:17a39c0ba978cc27001e9c56a480f98106e1ab74bd56eb302f9fd4cf758ea43f`  
		Last Modified: Wed, 08 Oct 2025 12:04:11 GMT  
		Size: 3.4 MB (3419815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b51528d40984545fc6adcac67d25d4f3c1750de4243649ca11bbaa90714ac17`  
		Last Modified: Wed, 22 Oct 2025 00:56:26 GMT  
		Size: 161.6 MB (161566791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.19-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:d9b648061d7a8a715827911ff0d848ccc487cc8554ba434c67f9a43c29565a28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **594.4 KB (594370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbc15e60977bdf60859803d8923545307f8bf1bc19af87f1a924a5f13975f1f6`

```dockerfile
```

-	Layers:
	-	`sha256:257cff0512e9b6771014b923f4e4d5ee9c6e745e5f7067139578a0da9b4b2ce9`  
		Last Modified: Wed, 22 Oct 2025 00:52:15 GMT  
		Size: 585.0 KB (584955 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4baf8b578ff2922aa1037b5c48b152ea48931bc19a00a9a58e008693b399ec50`  
		Last Modified: Wed, 22 Oct 2025 00:52:16 GMT  
		Size: 9.4 KB (9415 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-alpine3.19-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:0c05398b8e32eaffc903070793c2a6584b96e230564fa0acd61dee81058b3187
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.0 MB (162953340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51f3d6d30920147905fd3ea8968cc77c37b9decf909ce9f409ecbea5d9466c66`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:10:40 GMT
ADD alpine-minirootfs-3.19.9-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:10:40 GMT
CMD ["/bin/sh"]
# Tue, 04 Nov 2025 23:15:34 GMT
ARG version=21.0.9.11.1
# Tue, 04 Nov 2025 23:15:34 GMT
# ARGS: version=21.0.9.11.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Tue, 04 Nov 2025 23:15:34 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 23:15:34 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 04 Nov 2025 23:15:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:5711127a7748d32f5a69380c27daf1382f2c6674ea7a60d2a3e338818590fea1`  
		Last Modified: Wed, 08 Oct 2025 12:04:21 GMT  
		Size: 3.4 MB (3359301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa6f7f98c666e13541ae56951149fab7d14c234e262b3af8645858c363983310`  
		Last Modified: Wed, 05 Nov 2025 04:20:28 GMT  
		Size: 159.6 MB (159594039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.19-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:9eb87c24310db187eb3cc872a56ec2e56f39e3724d5459f05d71709485c3ce48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **593.8 KB (593847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5f369feb098a4409b75297a65a52ef0d2375ea963240f810ee9cba72370d32f`

```dockerfile
```

-	Layers:
	-	`sha256:d9dbc61c3e6c4a6c918a53b3ee51be010ec1a2ac328121b689cc9a25bb6e74a7`  
		Last Modified: Wed, 05 Nov 2025 01:48:39 GMT  
		Size: 584.4 KB (584374 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99cfb6c5dc7a88d9eb1d384ec98081532af3c2c936b3e73435598eabe6621b29`  
		Last Modified: Wed, 05 Nov 2025 01:48:40 GMT  
		Size: 9.5 KB (9473 bytes)  
		MIME: application/vnd.in-toto+json
