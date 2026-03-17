## `neurodebian:noble`

```console
$ docker pull neurodebian@sha256:79adb5f98a71a6159946a6b681f15fcd57fb27c6daec32e7f1b6a1d94aa61f23
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:noble` - linux; amd64

```console
$ docker pull neurodebian@sha256:99cec198c10241708cc74ddb9badc7f61579e15770743a61cb7a76020efeb381
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33403846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:698c47689ccd15da9af1cd464a050999d7f1ad7c080c757055ffc9ac0ab58c33`
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
# Tue, 17 Mar 2026 01:43:40 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:43:41 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Mar 2026 01:43:41 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian noble main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 17 Mar 2026 01:43:48 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:817807f3c64e0b90b66edc7d90297f121cad2a7c2a3ee05a731557762f91e6c7`  
		Last Modified: Mon, 23 Feb 2026 17:51:17 GMT  
		Size: 29.7 MB (29731993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cd2ec225ec2a9033fe4348f140a3f8ec348f417e5042ceb69ebada72bd674db`  
		Last Modified: Tue, 17 Mar 2026 01:43:55 GMT  
		Size: 3.6 MB (3564564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ef17f483be9c2ebf11f63f4d9f74a665b3c6fae30c0fdcb26137614861b95f2`  
		Last Modified: Tue, 17 Mar 2026 01:43:55 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6feceec3641c1de79bdd0dcd16ec89f8c37f2277b29391fae5a9f0d01a48ba93`  
		Last Modified: Tue, 17 Mar 2026 01:43:54 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cc4e2ec377246875f841ab25ba7e5975732e41e87749f28aeba3921aeb5bb52`  
		Last Modified: Tue, 17 Mar 2026 01:43:55 GMT  
		Size: 104.4 KB (104379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble` - unknown; unknown

```console
$ docker pull neurodebian@sha256:fbb5db8c0e09cdff64b8f32319be07af9b6a1bbdfa7c34e6384d41d6d8452fdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2134822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d841613d66ed32fe559043280b70d9e9b66e1909b225de45872710f62ed7bac`

```dockerfile
```

-	Layers:
	-	`sha256:b7ca2ca4ec1655009f26991208d8dcfc04bb060bf3089f4880cff7c384169354`  
		Last Modified: Tue, 17 Mar 2026 01:43:55 GMT  
		Size: 2.1 MB (2120889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cea1bf48e4d857192c9e8234db2505ace1be473b7074ad2e5f898bde4798f908`  
		Last Modified: Tue, 17 Mar 2026 01:43:54 GMT  
		Size: 13.9 KB (13933 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:noble` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:f245aafa6ac8f69e6188bebb3508fdad80fbdd1fb625fd621adb8a081b73a203
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32539513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13c56ee68d80089c3f0925d8e58f1aadbf3c27908dd7512fc85c2c23e22163e2`
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
# Tue, 17 Mar 2026 01:45:26 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:45:26 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Mar 2026 01:45:26 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian noble main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 17 Mar 2026 01:45:35 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:86790fc5660dcd86928b849ae0826aba701bf9e005e92c8f9e06c917e82c87f7`  
		Last Modified: Mon, 23 Feb 2026 17:51:24 GMT  
		Size: 28.9 MB (28869709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:533c5edf582f6c749ef6a1c980c83140c19790fba01e023270d953596d6728eb`  
		Last Modified: Tue, 17 Mar 2026 01:45:42 GMT  
		Size: 3.6 MB (3561698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58e00b53b8e4686217ad4464335977ad206a0b44b2c815209a57b92579deb2c3`  
		Last Modified: Tue, 17 Mar 2026 01:45:42 GMT  
		Size: 2.6 KB (2638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4150071e6c680a3e30636e054b5eb864727fe3c9b6bc8e4e894a63bb147d2e8`  
		Last Modified: Tue, 17 Mar 2026 01:45:42 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcf622f6ce748df581fde435236c4025fce1294e846eb31a4c2bb114ad60de5e`  
		Last Modified: Tue, 17 Mar 2026 01:45:42 GMT  
		Size: 105.2 KB (105195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble` - unknown; unknown

```console
$ docker pull neurodebian@sha256:345880f970f78bca78609af939641e1ee75bb8f43c66a887fa2d8ee357bf4356
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2135992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33261a958005f1391a059daad1bcaac28d5b8b86b44eabd34be6e413a13c46d1`

```dockerfile
```

-	Layers:
	-	`sha256:4bcad4951b4567ba4ce52d8f30dd9930b9a357da1219bb3fbdc23e3ae7caab35`  
		Last Modified: Tue, 17 Mar 2026 01:45:42 GMT  
		Size: 2.1 MB (2121934 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:506182a496a21e1b4cab38177081115a703e24a5ca3745eda65191d95f3a7545`  
		Last Modified: Tue, 17 Mar 2026 01:45:42 GMT  
		Size: 14.1 KB (14058 bytes)  
		MIME: application/vnd.in-toto+json
