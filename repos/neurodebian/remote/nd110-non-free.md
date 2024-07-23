## `neurodebian:nd110-non-free`

```console
$ docker pull neurodebian@sha256:6eb7047131d18122f0e2d754480629d1d823a544092c832286f32f954c70bfa2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:nd110-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:9169aca8765b26832244003e164111bddf36e9000b1216f8e7a03c7f96c4fe7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66292710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86de54931fdb819e97959ffdc98c5b1d5c1d95609b179fc3ac1fc802d33a8945`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:61c91b2a02e0d3deb2364da03241d137acf78345623ae188082e574b043032a0 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:73226dab8db5240a2ddbdbe2fb1f0949a911563a62a3d5de3c8669ae708e88de`  
		Last Modified: Tue, 23 Jul 2024 05:28:11 GMT  
		Size: 55.1 MB (55084578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4203d3e26932e117e5a08d861f59e1899dce1c005702276450b904177c19cb2a`  
		Last Modified: Tue, 23 Jul 2024 07:14:51 GMT  
		Size: 11.1 MB (11105032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3355d9bc6ce568013c3b0db91282f933798aa18867ab4c1c817007bb650d6eab`  
		Last Modified: Tue, 23 Jul 2024 07:14:50 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a8ac34ee9820db6d31a67aa65ff870c61daea5034053781f925a4158b91ad4d`  
		Last Modified: Tue, 23 Jul 2024 07:14:50 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf3a4495a6fb1dd49d4a821cf3976220e6395a9e8439809d8cbf021e645ce2f9`  
		Last Modified: Tue, 23 Jul 2024 07:14:51 GMT  
		Size: 100.8 KB (100750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:449f168b0c554b07cab2523e57a84d5385be3575dc1e6276859b3ed58065d1df`  
		Last Modified: Tue, 23 Jul 2024 07:14:51 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:a26ac99eecf184cfe3431360a0cd033220f702ca73fa56dfd59d33e0d3a50266
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4239252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e82637fa1391447c6d0544d010aeaa356a69a64427c058a9707be2176451d39e`

```dockerfile
```

-	Layers:
	-	`sha256:a4ab3b457787b5e3126ec0fac5720bf2c186fa30a8f8d0e6b17e5b1a3ce030fa`  
		Last Modified: Tue, 23 Jul 2024 07:14:51 GMT  
		Size: 4.2 MB (4223740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:943ae89fbf22535224d00ebcdef1727f67a52537b65d0abafa7a4070e6d3cf3a`  
		Last Modified: Tue, 23 Jul 2024 07:14:50 GMT  
		Size: 15.5 KB (15512 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:82bf4e5ed94becd63bc80613bbbfcab1117f3531cb3e6bdc4de8b91584390bbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.9 MB (64938791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d4fd46d859c6c291dfcc03a794a375e2419819290d85a5ac3be035574f3acee`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:bbd5c67ed8e7916601bc20e4ce4973720e715d9dcd892ccbd64c1d5de711a38d in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:2c9750102c61ce3f4a11c8776dfc892d41a6d4a662d2882e471664dbad58487e`  
		Last Modified: Tue, 23 Jul 2024 04:20:44 GMT  
		Size: 53.7 MB (53729987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2748620df5e1335ff4d2a1ff3d6b29fdcadb199a1da1c0f954ee400b0987da57`  
		Last Modified: Tue, 23 Jul 2024 18:34:49 GMT  
		Size: 11.1 MB (11105782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28772ec05400cd0f7075f13813c452cc315f7c87a3370a48753a5530b8c202b2`  
		Last Modified: Tue, 23 Jul 2024 18:34:49 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b74765cc784e39ab51976cb4f82860a87708d3a5f7bba696c461c07136ec85c5`  
		Last Modified: Tue, 23 Jul 2024 18:34:49 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c36deb65a886758fde62b0455cb2efcf0eba23ed9c43693d1ed048665413046`  
		Last Modified: Tue, 23 Jul 2024 18:34:49 GMT  
		Size: 100.7 KB (100677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb59aa94f3e9a771660b397dd7d1d9b5696b3825b0a79e545024cd1d2a0849d`  
		Last Modified: Tue, 23 Jul 2024 18:35:12 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f14d63d20d8059739706c1703eb4b34926365cd9a6f1cc608f90d03aa733da22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4239137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:668b5b5bd362e873dd3e0d4f8760bc5294fcdd2aab0ed043728a78c754145f9b`

```dockerfile
```

-	Layers:
	-	`sha256:e0a878916f8e961699113fb67ad468aea57e710c163490714237c67b508d9d2d`  
		Last Modified: Tue, 23 Jul 2024 18:35:12 GMT  
		Size: 4.2 MB (4223345 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5642cb35f6a21f1a43ec2b4c604519bb2ce12aca7fa740d57a0f0170b0ce26d`  
		Last Modified: Tue, 23 Jul 2024 18:35:12 GMT  
		Size: 15.8 KB (15792 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:f3bbd6cb40a972adad281c251a26b3849256f1d5e23eb4e46cf24bac38710bc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67677294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e8c3d85fb9747aab0f870841c258a2de0195db99c08ada430dff64008a85062`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:d1f79afb47e16fbf87d0a90342c567c752e14b1bf325fa45d6de69ea871b26df in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:35a8dcedb97fd8133fbcd18694f30c60eebc7e4f268630ab7b35eefe40254457`  
		Last Modified: Tue, 23 Jul 2024 03:58:11 GMT  
		Size: 56.1 MB (56074170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf6fbe20aa5b4a62df6fddf9098e73fcd193053f19ec4b96dcfc3980ed765b16`  
		Last Modified: Tue, 23 Jul 2024 06:16:21 GMT  
		Size: 11.5 MB (11500131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b939e2e66405723c6e381754628c666f4480cd54ce632d36b4f31128c4bf6cb9`  
		Last Modified: Tue, 23 Jul 2024 06:16:18 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d75cdda278d30c01a386f46a7403ae0ecf5bc79ede317554522d0468911dad85`  
		Last Modified: Tue, 23 Jul 2024 06:16:21 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9347731466fa755649ac3f9513a02e4212f1ee9d62296c50f43a8ad484c73bc1`  
		Last Modified: Tue, 23 Jul 2024 06:16:21 GMT  
		Size: 100.6 KB (100647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61e0e622a2c8fffcc48a2e8ef53ef03849e5267ecfda9859881263db6951d853`  
		Last Modified: Tue, 23 Jul 2024 06:16:21 GMT  
		Size: 359.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:09ea5537d94e7fc078811fd6a01bf389a0aa6cd17f4046584b89cfe35bb65dd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4235685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e13baaa881b84dc52642d868a8eeb129e242389e8bab71d8314fb60db018700`

```dockerfile
```

-	Layers:
	-	`sha256:8d3ad12904a82508081c67419c32149f22aaf2a3f750bb2caeae9248f030cc27`  
		Last Modified: Tue, 23 Jul 2024 06:16:21 GMT  
		Size: 4.2 MB (4220200 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69a91c6d7601c8ea9fdca46d69836734a4129a6c0d0471974d6b9221047fab40`  
		Last Modified: Tue, 23 Jul 2024 06:16:21 GMT  
		Size: 15.5 KB (15485 bytes)  
		MIME: application/vnd.in-toto+json
