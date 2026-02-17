## `sapmachine:17-jre-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:74f1ec52eb053a1f32f0731347f181be6e1e6623c3191469b6c356958ad58a3b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jre-ubuntu-noble` - linux; amd64

```console
$ docker pull sapmachine@sha256:b4e8b6d5a6d69553acdc1873ff0c42049bdf2462f2852fad33fcb15983b39dba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.5 MB (84497535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4ce5b3a9040fdc7a940b264150cf58d0478d2b5239223e60aa9032960604fe3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Feb 2026 16:49:54 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:49:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:49:56 GMT
ADD file:1ae27d2ef4369361104b699712f3897141e394785df5d193d67b44626f57eb87 in / 
# Tue, 10 Feb 2026 16:49:57 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:35:12 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.18 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:35:12 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 17 Feb 2026 20:35:12 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:01d7766a2e4a62b74e0bebf2cd12c47e675e9221174f6570854203e84ffe68b0`  
		Last Modified: Tue, 10 Feb 2026 17:41:34 GMT  
		Size: 29.7 MB (29727611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b139a015fc188fbcc9c6806e276c23e7e5343130f633494333c5dc380167a90`  
		Last Modified: Tue, 17 Feb 2026 20:35:25 GMT  
		Size: 54.8 MB (54769924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:0b2f05e6d01f71180a86cbb438db7b4f5d260a131a8c172bf187b4c54b55ef8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2529808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d90f6266b071288ba7da3f4d9c9c179f7d1031086cbefdc09390d698a6d60378`

```dockerfile
```

-	Layers:
	-	`sha256:683143fd7b9dc0822574ea5f6727d8ed0c46ea3465e3c80cc56338c26982baee`  
		Last Modified: Tue, 17 Feb 2026 20:35:24 GMT  
		Size: 2.5 MB (2519762 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8cb284b1e59434f65d38da3443f782bd85315d806a579561e87e6fad935f6f6`  
		Last Modified: Tue, 17 Feb 2026 20:35:24 GMT  
		Size: 10.0 KB (10046 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-ubuntu-noble` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:02c1b19279e4d6661bf0b2567fc25a622043ed8753cf796399d561981d831672
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.1 MB (83067106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c82a21286eaa0350c64f67473b6c0abc653825fccda920f412c907ba7e9c063`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Feb 2026 16:52:26 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:52:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:52:29 GMT
ADD file:25d708bf0b30ddee20c0b2764034e065aca922cafd48eb9c662e35ba02ccf1de in / 
# Tue, 10 Feb 2026 16:52:29 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:34:14 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.18 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:34:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 17 Feb 2026 20:34:14 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:66a4bbbfab887561d75f1fdb3c6221c974346f82c9229f5ef99f96b7e6c25704`  
		Last Modified: Tue, 10 Feb 2026 17:41:42 GMT  
		Size: 28.9 MB (28865120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9644fa59bd47c047ada9c0179e6771ba5606ea95e3599db48c00dac3601e2dd6`  
		Last Modified: Tue, 17 Feb 2026 20:34:27 GMT  
		Size: 54.2 MB (54201986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:c80879c420c49df3aa0b6bb881e7378a8c63f7b1620cf5f2dca445e1115f46d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2530476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b4c07fcbe1e5ae9ccd3be3093c7f4d7352ee6c5e2ed174e40cedf8c4533a97c`

```dockerfile
```

-	Layers:
	-	`sha256:c1a0ac2c4525565dca11da7dfd45d4b8757d3d2ef1c7b5fc93ba9223d9f27136`  
		Last Modified: Tue, 17 Feb 2026 20:34:25 GMT  
		Size: 2.5 MB (2520278 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a66481a0dc5ce5e646aad47d49920c9ab47344a6070004760933ce540544865c`  
		Last Modified: Tue, 17 Feb 2026 20:34:25 GMT  
		Size: 10.2 KB (10198 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-ubuntu-noble` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:5d30747f02737ceb53e517ed21ed31b2214b3e3a38b1238ec064f45166cfbaaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.4 MB (90379288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd277193684a641ab6706366143458fa10d1cc04e928d0663793a0cd0b8f9887`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Feb 2026 16:50:31 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:50:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:50:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:50:31 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:50:35 GMT
ADD file:993db8d05f03953198d71fcb66f9a9dca68dcfd7ca7b3e4a866954aa297b35ce in / 
# Tue, 10 Feb 2026 16:50:35 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 21:36:07 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.18 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:36:07 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 17 Feb 2026 21:36:07 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:de86bbb8cdc5c52dc9167f3fab22b2f39424ccbfd06ab6c7b34bb3456cf0ad43`  
		Last Modified: Tue, 10 Feb 2026 17:41:57 GMT  
		Size: 34.3 MB (34306906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5bd219eca1947f6ae5437f10567d75741584d4c0bae306d0f6249c27b36a5b2`  
		Last Modified: Tue, 17 Feb 2026 21:36:40 GMT  
		Size: 56.1 MB (56072382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:d01648edcb9e0bdfc30f6f106644e420c24a1a514bd16fc2c550665ee480a372
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2529374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ece7b44d693c2f94f8c2305f02bf0749a20f56438b03079c51f143c0c5ca6ae`

```dockerfile
```

-	Layers:
	-	`sha256:39c9ef8c95964897bae577be04f1a462eca5bcb4c63222b36f13524edcae8ab2`  
		Last Modified: Tue, 17 Feb 2026 21:36:38 GMT  
		Size: 2.5 MB (2519260 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08b38ba7f47b6218981520a2fff43f3438960310ff6638155bdf583a4e7add8d`  
		Last Modified: Tue, 17 Feb 2026 21:36:37 GMT  
		Size: 10.1 KB (10114 bytes)  
		MIME: application/vnd.in-toto+json
