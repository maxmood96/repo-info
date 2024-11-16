## `neurodebian:noble-non-free`

```console
$ docker pull neurodebian@sha256:7e1437687865294520ccdbd7c5c463babea5d73652986c21f575d20cb5f98225
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:noble-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:fecbf737e69bb6a7280a580f4a39f0893fb62f333727951d4366d1bb91d76367
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33414411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28a3f74a76e86e43681715ae7139cfc226f3642dd2d9a65306bbe3b8d9432f0b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ARG RELEASE
# Fri, 21 Jun 2024 21:57:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:a3272496fda5a8d021b94dccaa6baa685ded51e9d23edb05f0b30978a83c9fc2 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["/bin/bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian noble main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:afad30e59d72d5c8df4023014c983e457f21818971775c4224163595ec20b69f`  
		Last Modified: Wed, 16 Oct 2024 12:48:06 GMT  
		Size: 29.8 MB (29751784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69d38b8e8aef4d64c7ae344914f29a40650790b36ca4af904e3f9ed2de985476`  
		Last Modified: Sat, 16 Nov 2024 02:57:00 GMT  
		Size: 3.6 MB (3558751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d16b35ef360fa2983c365ebf28fe3e4d6dea08b178e8050b4a46f478a44f87f`  
		Last Modified: Sat, 16 Nov 2024 02:57:00 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e88aade09779dfa4c13efaaf96275542949d9c6540340a0b01dd9d671a8b919`  
		Last Modified: Sat, 16 Nov 2024 02:57:00 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d95da935f4fb7e0e90557addc25a2ddad11daec76acb4a6d5d696659b0586ee6`  
		Last Modified: Sat, 16 Nov 2024 02:57:00 GMT  
		Size: 101.5 KB (101484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17149c52c7bb0f4b4d6dafd08d3cb8ff441b98ec1b97e5b86ce2d422a493f481`  
		Last Modified: Sat, 16 Nov 2024 02:57:01 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:9b3146e161f3ce19f6e07ce945ebc7a43c30f49761e7fb6c57f819bd3e750dcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2003103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9100dbace151c02e6f4a60ce451a34763bf3ecd57bb4abc64d578aa922af3ffc`

```dockerfile
```

-	Layers:
	-	`sha256:9b01392fdf284c1a62db9958a609cc4a560d35ecf7f78ba48af30ff812066ce1`  
		Last Modified: Sat, 16 Nov 2024 02:57:00 GMT  
		Size: 2.0 MB (1987213 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df126d1669c6415286cc56056524dcd7e479d578a1c11f4c9d807f801a2bde79`  
		Last Modified: Sat, 16 Nov 2024 02:57:00 GMT  
		Size: 15.9 KB (15890 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:noble-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:53cac0b1df1cae57e55ac370115f26068e80c52188f8ce50be5ed3d844c4fa96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32554504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0eb969f64ea5c3d014d044f4992c56012a9b8a0356e7c8ca8ca2ccbd1bed4f30`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ARG RELEASE
# Fri, 21 Jun 2024 21:57:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:f45100f0b1cac298fb43b06ffef22e36a90991ee414d6dd825694bbea3365d40 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["/bin/bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian noble main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:e3366dd687552c0533285c7066bb8e937a5aaa2ff3a0c1c7f1305b3310399895`  
		Last Modified: Wed, 16 Oct 2024 12:48:12 GMT  
		Size: 28.9 MB (28892425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2730281b7aa2afc6f5415359b1e75ab20ffd63a9aeb9a6434ee4dd72ca91fa9`  
		Last Modified: Sat, 16 Nov 2024 03:19:07 GMT  
		Size: 3.6 MB (3557696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf185d2700eb1e11f3b9a77be6f31690a23dbb1d5a78b27b69393023b1abbb3`  
		Last Modified: Sat, 16 Nov 2024 03:19:06 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29bcc50f4e7e6bd421fe9ce745bcba73eee74e2e7816a4c1934614f7868a964f`  
		Last Modified: Sat, 16 Nov 2024 03:19:06 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7cb1aacd27b7dfc27830b6eeea54c14aceb3cba8d0e34c28d0c74b6b0c472c0`  
		Last Modified: Sat, 16 Nov 2024 03:19:07 GMT  
		Size: 102.0 KB (101983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bee28ffbafa489ac28fd8e18ea35adcb543ad84ee357a75f80ac8ef7aaa69eea`  
		Last Modified: Sat, 16 Nov 2024 03:19:25 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:a1cf199eb2c3f73236eab154bf58c1e4bff9c5ac8c29cf77537d9dff4f6640ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2004288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3ea1a0acbe9b173e127aea0f1504fb82854416e150246da15f0b6f53b6fb9dc`

```dockerfile
```

-	Layers:
	-	`sha256:4f591be482f23eebd2a681515139b503c698cb622ac37af35d8c69430cb98f32`  
		Last Modified: Sat, 16 Nov 2024 03:19:26 GMT  
		Size: 2.0 MB (1988258 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94a703cabb485d5e6cdbc0cf01bfbf655d0df04e4718faf6a7d729c55597a294`  
		Last Modified: Sat, 16 Nov 2024 03:19:25 GMT  
		Size: 16.0 KB (16030 bytes)  
		MIME: application/vnd.in-toto+json
