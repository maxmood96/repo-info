## `neurodebian:nd110-non-free`

```console
$ docker pull neurodebian@sha256:bc55848d218147731968a7401d67e40f20830f8bb81eeb5d699dee57d2b8a2a0
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
$ docker pull neurodebian@sha256:433b10f63bc29bebf93cce594f70a709c333d58888f0c1dae59d8a38e917e917
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.9 MB (64930548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24e77dbdc7a26728e6fede307180c342d554ae1f60840118690b95095ce2d65b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:4e98397394fc6db8fa55fb21c15dab09007b6ba883cb193f3a53f94480fee872 in / 
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
	-	`sha256:a4cd3ad66f7873241881d2ddd4efa6521034245e95e2b0b4a059817345151048`  
		Last Modified: Tue, 02 Jul 2024 00:42:43 GMT  
		Size: 53.7 MB (53721653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68ea11fc4812146ee0406609bad9931ab449987942af4c11c63743088a1ed032`  
		Last Modified: Tue, 02 Jul 2024 16:00:10 GMT  
		Size: 11.1 MB (11105843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c6adaa472f44d4e0fde1bfb9b6682772843d66b15ef7598b4558b66db050d49`  
		Last Modified: Tue, 02 Jul 2024 16:00:09 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dff784185d6c577acbfea3c8f77c196ff0c53187329dfb35087fda392ed658b`  
		Last Modified: Tue, 02 Jul 2024 16:00:09 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f15342e6ff663e4aaa1146d7b0b3b61b678ae6c7a1195f429b23398d519ece0`  
		Last Modified: Tue, 02 Jul 2024 16:00:09 GMT  
		Size: 100.7 KB (100700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fb0059251eb4e037e9330a461857c1cc659f97435a2477d29e0dc2f647a50af`  
		Last Modified: Tue, 02 Jul 2024 16:00:29 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:65e2f672d7daed979af9224884286c87f5c60c11f2bf2509a68a7f504d7f3c7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4214170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d913103204b84b8f9c9dc416cc1b1b59951988f873b2d8a172a315104d520e10`

```dockerfile
```

-	Layers:
	-	`sha256:2617cd894e45708e8ee0010408f0f4692854f007e86dbcaa5e6f16e67176df27`  
		Last Modified: Tue, 02 Jul 2024 16:00:29 GMT  
		Size: 4.2 MB (4198378 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:817bfdfc005086a64389cd3a32b12a09ad41707adb504d8ccee86d41fa679320`  
		Last Modified: Tue, 02 Jul 2024 16:00:29 GMT  
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
