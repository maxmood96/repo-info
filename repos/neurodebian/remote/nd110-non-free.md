## `neurodebian:nd110-non-free`

```console
$ docker pull neurodebian@sha256:d5ef72e0ead2636cc454167d982022a272b84411056597e8ee3b213154867189
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
$ docker pull neurodebian@sha256:126a9c6f63443f25bb6a1fa8ba12dce607b5f7c9ba0ccf75f419aa392733b4f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.9 MB (64947801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e84d63926e49213c6ae43aebed55881dd093f6699c825ae811680c1e019c5bf`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1736726400'
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
	-	`sha256:de97e8062e06250e3c3cef0d40cfe62111bb4b74bcf6221e25a06452dacffcf6`  
		Last Modified: Tue, 14 Jan 2025 01:33:36 GMT  
		Size: 53.7 MB (53739164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0cf63ca12518155ae5de9de65a484934fd44571aca70148fb813b2e769d5fe0`  
		Last Modified: Tue, 14 Jan 2025 02:35:05 GMT  
		Size: 11.1 MB (11105084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90cdf1b10154a8694dc9e1e80207b0645963f760016e0ea00bd64ae0abdb27b5`  
		Last Modified: Tue, 14 Jan 2025 02:35:04 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af00d05f7027b7accf9b9f5af3300fa1112f644660108b985eed73a98894f7a1`  
		Last Modified: Tue, 14 Jan 2025 02:35:04 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf14d73e93cda3ec35b9666d7806de3cd28fd16dd972445bd652189c2d7e8963`  
		Last Modified: Tue, 14 Jan 2025 02:35:05 GMT  
		Size: 101.2 KB (101202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d95edef1b774ba0ecebbc584f45789965a8fb6a8974670ce37b71078652c0bb1`  
		Last Modified: Tue, 14 Jan 2025 02:35:05 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:6998eb4b22a2f5e49220a52eed20c499c767a1b2cb6416699c68fa2ac727b1f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4248552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06f5f792f9285e748d19c784e4eeca5bed4c7b9579c9f5595d97c01276a2b536`

```dockerfile
```

-	Layers:
	-	`sha256:d108705f064f5fafccc60c5ac7b967efa2d40789ae931c87e4e7fba5d00c4718`  
		Last Modified: Tue, 14 Jan 2025 02:35:05 GMT  
		Size: 4.2 MB (4232832 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a3092cdd3bf27c62cc11e1e8a0a8d9d30e81f19f1caa0bae26a81b49bf668a6`  
		Last Modified: Tue, 14 Jan 2025 02:35:04 GMT  
		Size: 15.7 KB (15720 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:535963c32fcf93d0b7e6b596c82ad6961c27b36a7e41ff685482c464957d071f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63455076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:362a4108e7a83cedf833a545ff08b6207e7ba08b6a3a0812d115741b25ec5c3b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1734912000'
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
	-	`sha256:447d428f9ffe60c6c8cc59e00901cd865a36737372ba05710598d7eaf0a1144d`  
		Last Modified: Tue, 24 Dec 2024 21:34:37 GMT  
		Size: 52.2 MB (52245698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be3fd91d26138d9aaab80f425987de57628c24f81aca2727bcbbe870f7dd5c3a`  
		Last Modified: Wed, 25 Dec 2024 02:19:02 GMT  
		Size: 11.1 MB (11105941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05d41e172cd8c296857603d6eec38de1b1fcad65483cb5e3a5c165772ebbc188`  
		Last Modified: Wed, 25 Dec 2024 02:19:02 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:583285aa42d4ba42549ac2e4ea57d0849fc285d04fffe2155b702638dfda9ade`  
		Last Modified: Wed, 25 Dec 2024 02:19:02 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a2a8e49cbdd987bb7224891093e38a2baa58d5a5b27980b70b0c710e3e4f973`  
		Last Modified: Wed, 25 Dec 2024 02:19:02 GMT  
		Size: 101.1 KB (101090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b911fff051384026d3a1ce7b93df92d04591d621e7a848ece543384bb43066a`  
		Last Modified: Wed, 25 Dec 2024 02:19:15 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:35f38aead4bfd0e832e06598f24f6017efb0e74754e494b9991587ded171bfae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4248299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6843c473007509fab0df0a75cfef7c88886f907a7d220eb6eb6f9822e16a0c8`

```dockerfile
```

-	Layers:
	-	`sha256:0c3a437b2e81c9a759dc43a0fc0f0e1afa5ff8144b82fb661cb368f505d8edfd`  
		Last Modified: Wed, 25 Dec 2024 02:19:16 GMT  
		Size: 4.2 MB (4232439 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e5539bdd889e22e995e7c9aef5cc6581e5a103abc9a7919ac5176c493a543ae`  
		Last Modified: Wed, 25 Dec 2024 02:19:15 GMT  
		Size: 15.9 KB (15860 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:015a7dd803edcdc7484a798a88b3b765b810487a802bff5aebbbc0901cc96dd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66280132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69f78c021a761771a4418b984f05cc74f31b740833c7f9730a39c9e459d3d039`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1736726400'
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
	-	`sha256:b72c0b254e0d45985d121f47650a88f2ee35fbb4ff596c396ee98094e0a26d1b`  
		Last Modified: Tue, 14 Jan 2025 01:33:19 GMT  
		Size: 54.7 MB (54676276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad941907de38852fe321944a1379f7aec8d0a718b1959b442713da9a8da7b4b3`  
		Last Modified: Tue, 14 Jan 2025 02:17:36 GMT  
		Size: 11.5 MB (11500377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58d840dc63356d47b24541755231db1cf532c8d9b8ffb8ebc8c1c5eb27a0c025`  
		Last Modified: Tue, 14 Jan 2025 02:17:36 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:010a2f58af9ba9f8b54795fcb5f760c32de75b6688b50f66520e9eea0ddde850`  
		Last Modified: Tue, 14 Jan 2025 02:17:36 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bf318f9ef815963883d16998eda644d713cd8994624c9daa4b7a9797116f8be`  
		Last Modified: Tue, 14 Jan 2025 02:17:36 GMT  
		Size: 101.1 KB (101133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8870f49d0c375b65be9505532f629d6489e4b51915d11b303b4a524f1b434c8`  
		Last Modified: Tue, 14 Jan 2025 02:17:37 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:e2181fd46b08d6b841f4b0e9eb88fe541c7f13d71828622eafcb1034b818d64f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4244985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0c8ff57d5b1699c7a3c34b4ac820127284568aacf5b22dc8f47b927e86bf585`

```dockerfile
```

-	Layers:
	-	`sha256:eeb99a7e66f04886b3dd493a01c4bab5ee498d9c33a43164d8815f03a193a5ac`  
		Last Modified: Tue, 14 Jan 2025 02:17:36 GMT  
		Size: 4.2 MB (4229294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ad80cea47c04a2da438ad63f8525ac0aeb17d3dde32649fde8975ffdc09a63a`  
		Last Modified: Tue, 14 Jan 2025 02:17:36 GMT  
		Size: 15.7 KB (15691 bytes)  
		MIME: application/vnd.in-toto+json
