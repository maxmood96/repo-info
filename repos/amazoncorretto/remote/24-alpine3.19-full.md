## `amazoncorretto:24-alpine3.19-full`

```console
$ docker pull amazoncorretto@sha256:0132a7898fff5edfd575e244269d838855fe0ad5aeebd8ff3e4019254c7dd8e6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:24-alpine3.19-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:6557cdb5d545e1d224d002a6a483cea3bde6e8906b25f88a383f35bd3141a33b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.0 MB (180024964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74141733f9e2f6e103beaedca15df1d0a1b0aba59c25ee3a0653ccc0d05bcb4a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:05:02 GMT
ADD alpine-minirootfs-3.19.7-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:05:02 GMT
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
	-	`sha256:83abf496f1b833f01c8f72695520b8975cc8b730d14a8ac270d6201bd0f1877e`  
		Last Modified: Fri, 14 Feb 2025 14:30:10 GMT  
		Size: 3.4 MB (3420868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bc235731fa69d232d460559bfdc28bf050b8e1482d61f14f30f4bab1beb8cc7`  
		Last Modified: Tue, 15 Apr 2025 23:56:05 GMT  
		Size: 176.6 MB (176604096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:24-alpine3.19-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:1b8c649b6642361ee91278f97ca64001788eefd0592cd59e422ef6ed26f4e2c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **399.3 KB (399296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e223bd2337c5993af85d531ca06088c555df679c306d0d8ef7b520288a1e1e6c`

```dockerfile
```

-	Layers:
	-	`sha256:3ca89f2dce50fe0f156c2e368f763608fb730ad7035c5640e9c7a44786c8fbec`  
		Last Modified: Tue, 15 Apr 2025 23:56:02 GMT  
		Size: 389.9 KB (389882 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:548d2dc2958f66ee9d1afc141ca5b8dc7725c405de0db97288436cab958030a0`  
		Last Modified: Tue, 15 Apr 2025 23:56:02 GMT  
		Size: 9.4 KB (9414 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:24-alpine3.19-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:7166fbe3ee90324d25ed0725d89f81df99c55da77d2ab133ea1e6ab77e62448f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.7 MB (177663501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ee9344306f7ea33c969e7a1545fca7d4c6395926140c8ca81ea4b74d254f8fa`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:05:02 GMT
ADD alpine-minirootfs-3.19.7-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:05:02 GMT
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
	-	`sha256:d13a3fff434d56c3504596695435266be8d07061a80359aa09366eea2e094aa0`  
		Last Modified: Fri, 14 Feb 2025 14:31:17 GMT  
		Size: 3.4 MB (3361424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d9296fec7f2b5a3e3f3a9135ba4cf56d4dfbe330b320a25f8a24c6131c359b5`  
		Last Modified: Wed, 16 Apr 2025 00:24:16 GMT  
		Size: 174.3 MB (174302077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:24-alpine3.19-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:5f5357439c550ae3eca58bb68e26e5428cb694d290ff4256e4fdf4f53f454310
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.8 KB (398816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9da562ae85f38be64a5b0fc6f1cfe1a77ac55fc1f4c121c1c769080b803a02f8`

```dockerfile
```

-	Layers:
	-	`sha256:efebb9b09d0e9435e52f842e673066ca439d20868440b5957e0e1957260a6049`  
		Last Modified: Wed, 16 Apr 2025 00:24:12 GMT  
		Size: 389.3 KB (389298 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9abb00209743794b7b6f99c8581c5ec645eb7d06993d90c3a2475f968a62f5a`  
		Last Modified: Wed, 16 Apr 2025 00:24:11 GMT  
		Size: 9.5 KB (9518 bytes)  
		MIME: application/vnd.in-toto+json
