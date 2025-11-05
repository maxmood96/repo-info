## `amazoncorretto:21-alpine3.21-jdk`

```console
$ docker pull amazoncorretto@sha256:d0abd1f4a1c98c593babb97fec6e64438acea8e1c209858f4f417f5174099bec
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-alpine3.21-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:5c5be512a155ea11feee4afb2109a20b86afbc6c2ce21c95d1d89546d62f714b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.2 MB (165214278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6070470f5c3884e7a91e9f6e22f2b248264b63d9fa1776932909fe5cdade24f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
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
	-	`sha256:f637881d1138581d892d9eb942c56e0ccc7758fe3bdc0f1e6cd66059fdfd8185`  
		Last Modified: Wed, 08 Oct 2025 12:54:09 GMT  
		Size: 3.6 MB (3642569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6197df07efde7daafe29916f7f56eda3d774aa1f4a1a2f437f8e0ae2cca4a9f`  
		Last Modified: Wed, 22 Oct 2025 01:01:15 GMT  
		Size: 161.6 MB (161571709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.21-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:0c71cad933640542bd0dc7f8f009c752da95884a013405546585dac90a402d05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **595.9 KB (595873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a413ba350ba87255d4152fb5adba9b8579dd6a8c0d2c9fef844d11010fe7aa1`

```dockerfile
```

-	Layers:
	-	`sha256:7f22932841c52c8be216d33187b6aee80b21f62227a26c9cf894060355c6d925`  
		Last Modified: Wed, 22 Oct 2025 00:52:36 GMT  
		Size: 586.5 KB (586458 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4b0887108ede57a94661f2ce1e10605ae1ef38e53786f9448271d9ddd17145f`  
		Last Modified: Wed, 22 Oct 2025 00:52:37 GMT  
		Size: 9.4 KB (9415 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-alpine3.21-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:fce4ecb4d28ebe2c930232704f83933a05730dd692017e1cec84ca6a11973d13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.6 MB (163574147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ee6dec2fd00a35af546e4074007ed66e21c6a2e9eeb5a414cdbd72a535deb15`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Tue, 04 Nov 2025 23:16:20 GMT
ARG version=21.0.9.11.1
# Tue, 04 Nov 2025 23:16:20 GMT
# ARGS: version=21.0.9.11.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Tue, 04 Nov 2025 23:16:20 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 23:16:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 04 Nov 2025 23:16:20 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:c2fe130f4aabc917e559e7eed7d37b0e21ba13b44520101696887ca892e8c63f`  
		Last Modified: Wed, 08 Oct 2025 16:24:46 GMT  
		Size: 4.0 MB (3992353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64b3a14b59a66bd18cc414432756e3cf15f091bd7d40e951dabc60b97aa88fc6`  
		Last Modified: Wed, 05 Nov 2025 01:52:47 GMT  
		Size: 159.6 MB (159581794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.21-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:f3bf3b5ed72fc933f84ee7b98105ad248d4e163c70740a8461661df80a2f71c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **595.4 KB (595352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:841b9c1236d76fa273070de7ce0dc5b5df7520ccb5afffe89f755c5bc52ffb97`

```dockerfile
```

-	Layers:
	-	`sha256:39f0dab4f3c01d96dec796bf70c51c14fb4e219d748fe2364dd2c8a18a87be62`  
		Last Modified: Wed, 05 Nov 2025 01:48:56 GMT  
		Size: 585.9 KB (585877 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d9ac3959ad64f9e80a00a972351d2a4b5294dcffc29042a992d54fec441a814`  
		Last Modified: Wed, 05 Nov 2025 01:48:57 GMT  
		Size: 9.5 KB (9475 bytes)  
		MIME: application/vnd.in-toto+json
