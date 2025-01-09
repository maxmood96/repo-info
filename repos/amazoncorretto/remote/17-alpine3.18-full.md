## `amazoncorretto:17-alpine3.18-full`

```console
$ docker pull amazoncorretto@sha256:258ba7ea5f779489b2e5b4612e01037bcb6abd87d7ee2e200249bafe5c69b9bb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-alpine3.18-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:98feeb90aec2b6ed260a9d850c540487a4691e98e77c4118065b45a64ae9d5ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.1 MB (149067637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a97b1dd3691dd7b514fc564ff74846d09f9458a6a1b32e5c1802136efff9338`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
ADD alpine-minirootfs-3.18.11-x86_64.tar.gz / # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 23:01:14 GMT
ARG version=17.0.13.11.1
# Fri, 13 Dec 2024 23:01:14 GMT
# ARGS: version=17.0.13.11.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 23:01:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 13 Dec 2024 23:01:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:f54a5150a7602eaef3169b83e73d5927b20aef2fcaefcba18b532bd63b328fff`  
		Last Modified: Wed, 08 Jan 2025 17:23:37 GMT  
		Size: 3.4 MB (3417974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c535ab4b355c3ef1064bc0a1166fff944dfa977ff757054366a1536815d2862b`  
		Last Modified: Wed, 08 Jan 2025 18:11:25 GMT  
		Size: 145.6 MB (145649663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.18-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:5a68fa6a05034b54d66c7a21dcd34f0b9d238d52bb5ac0e172eef5c0f8741014
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.7 KB (389658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abcf83ededf7f15b2dd879554efd22657536cd645b7d77e051556ae1caa11a60`

```dockerfile
```

-	Layers:
	-	`sha256:2e1f9c6538547f91c55df83a118395fe66c727a7c8e85b9a1a815ee5931335b3`  
		Last Modified: Wed, 08 Jan 2025 18:11:23 GMT  
		Size: 380.2 KB (380236 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee69504b4f2ee0e0ebabf480b83b8538b7d45f99cf234c001a8f4faf8817eb76`  
		Last Modified: Wed, 08 Jan 2025 18:11:23 GMT  
		Size: 9.4 KB (9422 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-alpine3.18-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:94ac2b62e44e3e6894e768a70e9d65cf8e91c82d351f5e23fa147ef6ef52a29a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.3 MB (147272443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d37406342095f6dde08fbc6a983a10d651c083929f989bca869aae0240419fbd`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
ADD alpine-minirootfs-3.18.10-aarch64.tar.gz / # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 23:01:14 GMT
ARG version=17.0.13.11.1
# Fri, 13 Dec 2024 23:01:14 GMT
# ARGS: version=17.0.13.11.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 23:01:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 13 Dec 2024 23:01:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:fb3f1f9d2d6533828602bbf29a9a8cc07ae4a2a3e88846100e68ce43a16d2932`  
		Last Modified: Tue, 07 Jan 2025 03:03:28 GMT  
		Size: 3.3 MB (3337435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37cc44348b713b011df0252765b9d6f82671c6ed492c3aa2653ff5224e6fe826`  
		Last Modified: Tue, 07 Jan 2025 07:23:11 GMT  
		Size: 143.9 MB (143935008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.18-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:c0e50973a10bd7c70352008c528f10bb9fe1e8536aa80d0c6210b25df0c7f893
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.2 KB (389181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeb657b8139a01a665e748793adf5ba0c2bc114920ae7cd1d68e8f1273b181ff`

```dockerfile
```

-	Layers:
	-	`sha256:5b7590d758bbb5ab417998e92ef79936e983e56da4e744ed9c53624863d354f4`  
		Last Modified: Tue, 07 Jan 2025 07:23:08 GMT  
		Size: 379.7 KB (379655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec7595f6a3d99f4063f69cfc9550781f7190775d02261ab5457fd6537440d95f`  
		Last Modified: Tue, 07 Jan 2025 07:23:08 GMT  
		Size: 9.5 KB (9526 bytes)  
		MIME: application/vnd.in-toto+json
