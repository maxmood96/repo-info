## `sapmachine:11-jre-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:0e381578e2cb3b74c13b3fb63e70b71edea16e8949f2877ed16f6d3fe06e5455
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:11-jre-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:6e8f231f0a94977f6bb298ade9ac88040f352d4d56d35cb1a2048c05f3a9f34f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.5 MB (79472447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4be5403ce8706e12c8dfbf79de55cbaf3f87e437c91725a84f4a18849947672`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:56 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:56 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 May 2024 10:06:56 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Mon, 13 May 2024 10:06:56 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:56 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jre=11.0.23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Mon, 13 May 2024 10:06:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:780924d290b34498ffb97bd726a45b75996fec5f9794a3f88dcaf57f2828e762`  
		Last Modified: Tue, 02 Jul 2024 03:32:09 GMT  
		Size: 49.9 MB (49938392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:8ca50e701967b65449e6a3cb97138ab5adc6f0ad4b983034d8b6ccdb2203b93f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2379333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58791fc6c47e9de57b6c29f8d732ed2645096aa2c6dbebd6ae698c5ba0b17256`

```dockerfile
```

-	Layers:
	-	`sha256:1c2fa3054860f4e312671af5ce21d2d0ac3ad951265c27f1e187f15ab7a06502`  
		Last Modified: Tue, 02 Jul 2024 03:32:09 GMT  
		Size: 2.4 MB (2370748 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4b0ae96738dfcb7883616bfbf938208641e274434cd1ee6fb08f977c28dd8a9`  
		Last Modified: Tue, 02 Jul 2024 03:32:09 GMT  
		Size: 8.6 KB (8585 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jre-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:4dc20586fb2bc413eb8ae3f228d2376c6d66d2cd7c1b125cc325b6d8c532664f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.6 MB (76578707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4297467ddd7fb8ebda009b7ba5cf6994f70b2da45b86680b2a93777ebe4f8389`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:56 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:56 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 May 2024 10:06:56 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Mon, 13 May 2024 10:06:56 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:56 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jre=11.0.23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Mon, 13 May 2024 10:06:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9b10a938e28486049341cb41134e8c0c141b2e25870896c597e2a54df471acbb`  
		Last Modified: Mon, 03 Jun 2024 10:46:52 GMT  
		Size: 27.4 MB (27361782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2c55f38a25d7ab87e33d7efd46c014cdb23761060e2de32af8e0ffe013e4be5`  
		Last Modified: Wed, 26 Jun 2024 00:33:55 GMT  
		Size: 49.2 MB (49216925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:a3ddace832a1e2f426d6c45cba2691b618fd4d1fcc934d79140abd36f7b8df4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2379942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f8f4cd408db35bc0e513b02870b1196a291f37701369262e26280f960b319a4`

```dockerfile
```

-	Layers:
	-	`sha256:44a5e741d94798f7967613e627aa285c8f95d7e01832223ae89002db2d52c193`  
		Last Modified: Wed, 26 Jun 2024 00:33:54 GMT  
		Size: 2.4 MB (2371056 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c861d42f3bd83f774f5154a329ff4719b54ebedffd21937c7b0c47130ae7c87`  
		Last Modified: Wed, 26 Jun 2024 00:33:53 GMT  
		Size: 8.9 KB (8886 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jre-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:f6c31eb3f10e1181258295f927b3d88a28ef5363c6ffdbf7f8236dc49e45d9a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.0 MB (83025500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bf87bb33449ce5523628cfec10580791322a12ea450aa714fa85901279bd630`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:56 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:56 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 May 2024 10:06:56 GMT
ADD file:e2e1e840070a30a93a9141ddf77b416d95fb822ac1f550f7162a64e18e0ade5b in / 
# Mon, 13 May 2024 10:06:56 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:56 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jre=11.0.23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Mon, 13 May 2024 10:06:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:dcb5d217f9f18d3486ceb1894319d66c6f49a84670fbf2ac2f4dd47935357bfc`  
		Last Modified: Thu, 27 Jun 2024 20:18:46 GMT  
		Size: 34.5 MB (34461081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e20722ab1b9610b0cf5951c817f767ae1ec98e508fffb05c8532c7d08a053ee1`  
		Last Modified: Tue, 02 Jul 2024 21:40:22 GMT  
		Size: 48.6 MB (48564419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:1e501a435fc371e5849705443bddbad4483b9c2004328c7000ba08726c0f4f43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2383356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d43de420f4577c1bdf412e822ca87727c2e7686c4915f2424d1580e956593c9`

```dockerfile
```

-	Layers:
	-	`sha256:077e42979f3f421b5cd54a2fd1cabb14c348bd1cff4a3de24aef3b12b32593a5`  
		Last Modified: Tue, 02 Jul 2024 21:40:21 GMT  
		Size: 2.4 MB (2374733 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af8bd5090202e16694d48de339f3b75e0bc369accdc259eb271abaa8e8aebbf6`  
		Last Modified: Tue, 02 Jul 2024 21:40:20 GMT  
		Size: 8.6 KB (8623 bytes)  
		MIME: application/vnd.in-toto+json
