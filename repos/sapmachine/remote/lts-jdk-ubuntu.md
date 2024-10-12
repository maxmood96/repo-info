## `sapmachine:lts-jdk-ubuntu`

```console
$ docker pull sapmachine@sha256:81e5a6f660da06df42300b9c4413f8c614c0e18605cf9b2efa553e98f627fcd9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:lts-jdk-ubuntu` - linux; amd64

```console
$ docker pull sapmachine@sha256:ac5375bcda5c79fb787207e79ec59159f02ec97096878649d440b22bff459586
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.3 MB (245348883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7166c8e1e127b1daf19482c44efef13a97c670e856eb0b4f7136fde4023bdf48`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:16 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 18 Jul 2024 15:16:16 GMT
ADD file:f77876c7db6df55380fb32e200969af6e12f1e932f742c4a63bd9da235d83413 in / 
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d1fbec07a2e50e73803e0c9ea0fc8f9fb48ad1215583bb1bbb8852660f52abeb`  
		Last Modified: Thu, 10 Oct 2024 08:59:45 GMT  
		Size: 29.8 MB (29750457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb619f111cd9a79835f8ab624a1b4713d2326306477299d9d2eaab9daf2a4571`  
		Last Modified: Sat, 12 Oct 2024 00:01:24 GMT  
		Size: 215.6 MB (215598426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jdk-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:42ee0247575309d01901e88231544cec3b89c839823f911a9bcc7a8da8cceadf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2465918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb6cb3d3efe4069ec3f96b4f9186e262e251cf99ac7473c92a4c414bbadb3bf3`

```dockerfile
```

-	Layers:
	-	`sha256:19697f0d6ae85f115f9d64b9f47858e9931e0306721f1830cdfc99da970c257c`  
		Last Modified: Sat, 12 Oct 2024 00:01:21 GMT  
		Size: 2.5 MB (2452815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71b9fbe946a28e4e879106b1e1e0e240e950bf939f1934f76758b31362fae704`  
		Last Modified: Sat, 12 Oct 2024 00:01:21 GMT  
		Size: 13.1 KB (13103 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jdk-ubuntu` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:b939baf7cee801aa747a7a394430c9abd72e716ffc1398a635f9faca5cd67e8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.6 MB (242587260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b1210c13b9049853d4f61c4a50c3bcd4d5ca71f7cb7b8bb3dfc4faf2b375a84`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:16 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 18 Jul 2024 15:16:16 GMT
ADD file:9d8a15341d364d2508ffca0657b4cb175a35d2edbdb0cf2476f7c4fff4f6c66a in / 
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:25a614108e8d9c23a53cb3193f34ba623efe45c81ccaaa2281092b512ef7e07e`  
		Last Modified: Mon, 16 Sep 2024 07:36:32 GMT  
		Size: 28.9 MB (28885430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b6f410376e3ea641c8d322f9d6bcda25406671f32829386bd1c91c532d7254e`  
		Last Modified: Wed, 02 Oct 2024 03:49:37 GMT  
		Size: 213.7 MB (213701830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jdk-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:f393df2dff67988ace1a819bf39636388c5a9f346ba27e34155416282692960e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2466147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a028e97f3f8a0aa47ce2b9032eacae5423106a4d6363004c463c65d2e55369c`

```dockerfile
```

-	Layers:
	-	`sha256:f1ea0fb4fdb30bb44c536442841024f3bd6f729017b7c99f8649d4291e5e434c`  
		Last Modified: Wed, 02 Oct 2024 03:49:32 GMT  
		Size: 2.5 MB (2452811 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73d7e01a3274a73058b8dd8a88d3ee620ce91f07549b2ea32c80c945c2c6bd74`  
		Last Modified: Wed, 02 Oct 2024 03:49:32 GMT  
		Size: 13.3 KB (13336 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jdk-ubuntu` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:110de18da921da052de7071f3249eb893d634e9253074730b8d7e5a6fe22f5d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.4 MB (251439404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1dc65b84355d746e67e418b00535faa4d19728da897802b17c7af1d72ea6ea2`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:16 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 18 Jul 2024 15:16:16 GMT
ADD file:6ec0ebf9a019b7c00b0121b97e89fcad881460415f8dcb9bb94b1cc7f5d0a5bc in / 
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0e110547234fd795b1c6d90b50b5df43ec509107fdf663124acb5e3861c38ef9`  
		Last Modified: Thu, 10 Oct 2024 09:00:03 GMT  
		Size: 34.4 MB (34389412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76607ab912770cd1c8107e2e912004892a20dee96a6c30a216a1ddbc330274cb`  
		Last Modified: Sat, 12 Oct 2024 00:29:49 GMT  
		Size: 217.0 MB (217049992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jdk-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:c1e6b15c07befbb32181594c6be577de4777658d38da19849065c20918051de3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2468112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24a2b43d863ad88b5f13dbee42909bc5fdaa1a8c453ad1d91bf05124ff5fcaeb`

```dockerfile
```

-	Layers:
	-	`sha256:37e7e7740914d3f529f08d4c67488c1bd7f6d1b6de02958fa51818473204e443`  
		Last Modified: Sat, 12 Oct 2024 00:29:44 GMT  
		Size: 2.5 MB (2454887 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4928175bdba95860e95df731e231949baeb9336d53f707a61518ec990f227e4`  
		Last Modified: Sat, 12 Oct 2024 00:29:44 GMT  
		Size: 13.2 KB (13225 bytes)  
		MIME: application/vnd.in-toto+json
