## `neurodebian:plucky-non-free`

```console
$ docker pull neurodebian@sha256:9fd3465d53ebf5c8667e396345b5c07e0dd332eba99b8f89f1c1d73e0b8ad637
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:plucky-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:e7e12a8494e56c96b8e743d68b661259bd850d79cda5e240f678665dea664e21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 MB (34805176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f8a964bf53bf298b9fda4da6ee1cf2dfb78d231037035040a8e9e15837b3368`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 10 Sep 2025 05:07:41 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:07:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:07:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:07:41 GMT
LABEL org.opencontainers.image.version=25.04
# Wed, 10 Sep 2025 05:07:44 GMT
ADD file:1d0db44377aa33c495de438dd435408b4391cf11e887ef1a542a8ab49275c67c in / 
# Wed, 10 Sep 2025 05:07:44 GMT
CMD ["/bin/bash"]
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian plucky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel plucky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:47429ff9cdd3006afbf0a7a02f144b5a7444e546614a97a12fd567f7a4e3afdb`  
		Last Modified: Wed, 10 Sep 2025 15:57:53 GMT  
		Size: 28.3 MB (28305856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7422c772e4bebb82915c942d5d65cee5cb73f3fa9d071314036f12211bfbd35`  
		Last Modified: Tue, 23 Sep 2025 17:39:20 GMT  
		Size: 6.4 MB (6392080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2ab86a9a06680b71282957a516de592ec540d4a3a3085dd99770143b53ec4f8`  
		Last Modified: Tue, 23 Sep 2025 17:39:19 GMT  
		Size: 2.6 KB (2635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ad68505bcdededd57953f74dd00caa2c6585aae6568b7b50b821a33e1750a89`  
		Last Modified: Tue, 23 Sep 2025 17:39:19 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:578f665a5e0bc3591b4eceef30540c01829e4e5e22367f95b3d347ad70de0d96`  
		Last Modified: Tue, 23 Sep 2025 17:39:20 GMT  
		Size: 103.9 KB (103902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cea750d95d3d4c2c0c60e9495f5ca6be923d353c078878135a374eeb6fd688c`  
		Last Modified: Tue, 23 Sep 2025 17:39:20 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:plucky-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:777bfcf11ec281aab0a7a0452dc2ff515160a15fa2deb6b1350b7d86ad703933
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2145983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba055ad51cb0966bc47f359d61b9e7366de88d63000a6a4d0ba557ebd5ff739e`

```dockerfile
```

-	Layers:
	-	`sha256:c5eed7530f2fa3ee9c35819415fd3c037dd5b1b351f7bb24d980eefdf4ec16b1`  
		Last Modified: Tue, 23 Sep 2025 19:08:37 GMT  
		Size: 2.1 MB (2129627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aab62724697affbc8b975acf6239ccea91b8af0a438a9131fc842c9c82e1703a`  
		Last Modified: Tue, 23 Sep 2025 19:08:37 GMT  
		Size: 16.4 KB (16356 bytes)  
		MIME: application/vnd.in-toto+json
