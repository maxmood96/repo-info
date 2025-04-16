## `amazoncorretto:24-alpine3.20`

```console
$ docker pull amazoncorretto@sha256:875484ee266b3aa0e5e29fa6cb46adeab355a6d082a9401bf627473ae20da72c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:24-alpine3.20` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:46d7c6977873e5b352f15eb8a83f133777293c06b9fa643404e0f198e9597dc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.2 MB (180229775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27a1d00dc9e804bc052fbaad5f39d6fc8c3621b67304eee80f2f501bade9816d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Tue, 15 Apr 2025 21:50:45 GMT
ARG version=24.0.1.9.1
# Tue, 15 Apr 2025 21:50:45 GMT
# ARGS: version=24.0.1.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-24=$version-r0 &&     rm -rf /usr/lib/jvm/java-24-amazon-corretto/lib/src.zip # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
ENV LANG=C.UTF-8
# Tue, 15 Apr 2025 21:50:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 15 Apr 2025 21:50:45 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 12:05:36 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06180867a04566e5966773f240622100a492f334647073fc84c5e82cff04dd14`  
		Last Modified: Tue, 15 Apr 2025 23:56:03 GMT  
		Size: 176.6 MB (176602878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:24-alpine3.20` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:1e30226be59eebcea1cd3965bb85b38a38c209ef7960b9566d85d089335dd49b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **395.1 KB (395066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc03760fa9ba0644603ac43dfb2a4d7b029b9a46a99652a624fb6d2356d26cea`

```dockerfile
```

-	Layers:
	-	`sha256:4d5fcef5e2b93d8403d53037fcff73a449f987bb7a2752ea3ce8c2bf46278c68`  
		Last Modified: Tue, 15 Apr 2025 23:56:00 GMT  
		Size: 385.7 KB (385652 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ff094289dff3f143e25f3e6796a8e9c4697543a2ee9292ab1ad6641c6fe6334`  
		Last Modified: Tue, 15 Apr 2025 23:56:00 GMT  
		Size: 9.4 KB (9414 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:24-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:46b3fd9d77d7c532f4028ca8fcd18acde9e0b292a9a74f7bcb13d22257d4f020
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.4 MB (178386972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f5239b214cc44661269e4429d75cd4625199615037479f2a1ee1f0632c652df`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Fri, 21 Mar 2025 22:11:14 GMT
ARG version=24.0.0.36.2
# Fri, 21 Mar 2025 22:11:14 GMT
# ARGS: version=24.0.0.36.2
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-24=$version-r0 &&     rm -rf /usr/lib/jvm/java-24-amazon-corretto/lib/src.zip # buildkit
# Fri, 21 Mar 2025 22:11:14 GMT
ENV LANG=C.UTF-8
# Fri, 21 Mar 2025 22:11:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 21 Mar 2025 22:11:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:94e9d8af22013aabf0edcaf42950c88b0a1350c3a9ce076d61b98a535a673dd9`  
		Last Modified: Fri, 14 Feb 2025 12:05:38 GMT  
		Size: 4.1 MB (4091165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:574f8df7517930845e7be43ad15c7a87e46a67888cc5c53c011f043e7044bc3b`  
		Last Modified: Mon, 24 Mar 2025 17:37:03 GMT  
		Size: 174.3 MB (174295807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:24-alpine3.20` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:503473164a287d36d7400f4f532d4bf3d6ee3d6ff5a22a2788c0a2ade712ff69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **394.6 KB (394581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1482293566ce93dc6236bcdc84479678054752fbb7e86f7a02bf022789b14428`

```dockerfile
```

-	Layers:
	-	`sha256:01c0a4e0bc3e34de7eb4b936f9a5c85f3acc6d74838dc4cf662e9ccc9574e41b`  
		Last Modified: Mon, 24 Mar 2025 17:36:59 GMT  
		Size: 385.1 KB (385062 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f57c7ec145f8ddbe2ec69cc996a3dd1afedca869bee800753b7662fa5016cb91`  
		Last Modified: Mon, 24 Mar 2025 17:36:59 GMT  
		Size: 9.5 KB (9519 bytes)  
		MIME: application/vnd.in-toto+json
