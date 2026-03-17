## `neurodebian:noble-non-free`

```console
$ docker pull neurodebian@sha256:b289304036b43b2b6f3ad612027e6859c6bdccbb50f661e67b5eb10ec2b808dd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:noble-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:931939e21f3e8e404e747e12a162e3e7fad01b0a7d24e5f7c820c28ded17882e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33404197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aabccfb9217d8ed362278ad062b465ee927cff4c7c6caa1b3fd30e65de5a622d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 23 Feb 2026 17:17:53 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:17:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:17:55 GMT
ADD file:3f78aa860931e0853077f09eb31eddbeeef8a9dd70977305b4876aa176770721 in / 
# Mon, 23 Feb 2026 17:17:56 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:43:50 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:43:51 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Mar 2026 01:43:51 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian noble main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 17 Mar 2026 01:43:57 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:43:57 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:817807f3c64e0b90b66edc7d90297f121cad2a7c2a3ee05a731557762f91e6c7`  
		Last Modified: Mon, 23 Feb 2026 17:51:17 GMT  
		Size: 29.7 MB (29731993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e84ab0d452cb21362d5ba044daf5df99864fb25c5d08dd9d0bd97026143a048f`  
		Last Modified: Tue, 17 Mar 2026 01:44:04 GMT  
		Size: 3.6 MB (3564507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f3bc17860a6a5345cef1e7af56e1244e6f30c1dc558bc2838de57efbdada052`  
		Last Modified: Tue, 17 Mar 2026 01:44:04 GMT  
		Size: 2.6 KB (2639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b6e70019b132acc2d97fda51b094eb544fbc9a053297a2ea80c9eb960f58d13`  
		Last Modified: Tue, 17 Mar 2026 01:44:04 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:872ce36ff481a7c03cf8ac9e06c0bef6150a282c4d2b0d97482c9c27cb4a118f`  
		Last Modified: Tue, 17 Mar 2026 01:44:04 GMT  
		Size: 104.4 KB (104354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4696bcd872eb5237c46e9c3df9ea3ca46de979cb111fc0fb249860b8fc0138ed`  
		Last Modified: Tue, 17 Mar 2026 01:44:05 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:4b0d6c2c1629074abdf85b6f467a19fc0201a837bc4152db44603ddb186f5e05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2137087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e204b0a7b6f48e64159e1115dfb3ae2ba89f75a2a92602c952449e6619d0276`

```dockerfile
```

-	Layers:
	-	`sha256:78f99f9c44f6e8511253f8e60951ae0b4cddd44ce4e91ab1c92423423b1d12e8`  
		Last Modified: Tue, 17 Mar 2026 01:44:04 GMT  
		Size: 2.1 MB (2120925 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69daa31095a097290e3e9d7965de683252c5e8df8d9b4ee14d18750f5f82dab3`  
		Last Modified: Tue, 17 Mar 2026 01:44:04 GMT  
		Size: 16.2 KB (16162 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:noble-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:ce595481555f22799b23709984c63132aaf65f8173372b49dda0db288400aec9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32540013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed632cb3d5db47f8b17ff49beef3f5dce58045dcc0def9094fdf199bfd4b738c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 23 Feb 2026 17:19:30 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:19:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:19:32 GMT
ADD file:2763d61bc43bd178306ae0d4151c2477166ebf199b8d7294d9ea410f9891993f in / 
# Mon, 23 Feb 2026 17:19:33 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:45:27 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:45:28 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Mar 2026 01:45:28 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian noble main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 17 Mar 2026 01:45:37 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:45:37 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:86790fc5660dcd86928b849ae0826aba701bf9e005e92c8f9e06c917e82c87f7`  
		Last Modified: Mon, 23 Feb 2026 17:51:24 GMT  
		Size: 28.9 MB (28869709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48f6f623361c6efd56bb67aedc4f222717a42d17afef22ff4c5a31d7a7e256be`  
		Last Modified: Tue, 17 Mar 2026 01:45:43 GMT  
		Size: 3.6 MB (3561747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9723320ffa1c0b3494c2a8ed4ab8007e21efa59c99e44eddf2e3fc1fd2f829b4`  
		Last Modified: Tue, 17 Mar 2026 01:45:43 GMT  
		Size: 2.6 KB (2639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4229db03f200c816596816aa31c4b37e3fab83352edd9fdc7ad6907a0687515c`  
		Last Modified: Tue, 17 Mar 2026 01:45:43 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:693b4978166e3d1c2e71665356071e6072c778a9a42676165726a80bbe5319d7`  
		Last Modified: Tue, 17 Mar 2026 01:45:43 GMT  
		Size: 105.2 KB (105213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33985861acc8af083671e8a61968806b39e5ccf0edd830537a58a9e638ec9f91`  
		Last Modified: Tue, 17 Mar 2026 01:45:44 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:e6b7c55f14afc19e0caa0105bfd997392b6094d9e9c1ea96dcfd7971fccd8cee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2138273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0a0cb863feaf52e97c9de309a966eb0e954946a2ff81ba964c220e106cf4e3a`

```dockerfile
```

-	Layers:
	-	`sha256:7e7ce7ddccae0a2b981eb1811f66b4f82d041a4a40fc23f89cd5994f7ce03035`  
		Last Modified: Tue, 17 Mar 2026 01:45:43 GMT  
		Size: 2.1 MB (2121970 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e996bedf073e79f9ab5366cfff4022fadd40eedbc816b96d8629dc5984962a99`  
		Last Modified: Tue, 17 Mar 2026 01:45:43 GMT  
		Size: 16.3 KB (16303 bytes)  
		MIME: application/vnd.in-toto+json
