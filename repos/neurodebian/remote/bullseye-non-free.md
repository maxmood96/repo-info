## `neurodebian:bullseye-non-free`

```console
$ docker pull neurodebian@sha256:8199b61b1a417e7ed51ca8f80672a46e758a4c8ced47ee34c31aafbe6fb46d18
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:bullseye-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:ffc4b9f7508e242b9c69859a5d90b3cf612c06fc0ada1d8504b151d926aa7a8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66293237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cec37c6d3e31136d0c85bbcf9c097ffbd9779f27e708ee6c92d484ba1b1ccc5`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:6648a8158bbf4a36244eb9e936fbed4ea29f2f090fb0a97a6a737be2d85a5333 in / 
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
	-	`sha256:203e9cf21bd27322e5baf32653bf3314ccf688be497585240d18b9f0ca24f2ee`  
		Last Modified: Tue, 13 Aug 2024 00:24:05 GMT  
		Size: 55.1 MB (55084675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:302351d91a1231ecbae76cb5918e1b4cc192e39df948aca28a41606f1a06b4e0`  
		Last Modified: Tue, 13 Aug 2024 01:11:50 GMT  
		Size: 11.1 MB (11105040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbe9b6f0fef964119f9408e111e03d80dc922a3a345387da6b73d909fa80b92c`  
		Last Modified: Tue, 13 Aug 2024 01:11:49 GMT  
		Size: 1.7 KB (1739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb7445590a739b3a522581d8c7dc1ffaece3ac9e37098e8907cfb623047fa6d0`  
		Last Modified: Tue, 13 Aug 2024 01:11:49 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6518ed1b8e70b81cfcd4f0d725be2b0ea9493750e3a879f9c5e805fa8a0db623`  
		Last Modified: Tue, 13 Aug 2024 01:11:49 GMT  
		Size: 101.2 KB (101177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7335d3d5a67b1af26f9467d05864711f203d8717fdaf3b234633685a0d52763`  
		Last Modified: Tue, 13 Aug 2024 01:11:50 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:5dafc26cdfdbf6bd3b827334c33c1c51a3589aeb2d4cc8fdfdfad72ce91a969f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4239250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:583ecc2700e13b73ae9acf43a5cc50f26177d75c2925a95ecd587e6c3007edcd`

```dockerfile
```

-	Layers:
	-	`sha256:7646adb8bf076c6f9cf65585d8ac71b400a62b06deea134f022bc9665a48b1ba`  
		Last Modified: Tue, 13 Aug 2024 01:11:50 GMT  
		Size: 4.2 MB (4223740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4c1b77c2882e500f5c0a132939374d17c22a90124b059be85680374d5521d83`  
		Last Modified: Tue, 13 Aug 2024 01:11:49 GMT  
		Size: 15.5 KB (15510 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:76612f82bb19d492cda557ef4ca7e5e12aa89fe10533f9f802f660f932860e9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.9 MB (64939265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e19fcb6b90a409e53d91791ce566f2dbb2995ad53426d99769cad48f62dcdec0`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:4a2aa1b23402547c558d14f98384342f2e98460b659cd211609373f5408e83bc in / 
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
	-	`sha256:5d8903d6126c38fefcb1196b9998da0798f56cbdf18a91c00d822144c232af6b`  
		Last Modified: Tue, 13 Aug 2024 00:43:03 GMT  
		Size: 53.7 MB (53729921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:604c1837712cd740a7b87a314d41272c401ded8ce6df66684b504dd48894e92b`  
		Last Modified: Tue, 13 Aug 2024 07:39:38 GMT  
		Size: 11.1 MB (11105879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:300cf65bc9beca57bc7882230779a6aa040b842f40c72404d5c06e5dadf718f7`  
		Last Modified: Tue, 13 Aug 2024 07:39:37 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f3d9476d60842d9d913502642dcba44aa76828cfb14cbaecfb739e21aa465a0`  
		Last Modified: Tue, 13 Aug 2024 07:39:37 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75fb0f25f8fac8aa2b0b2671c3c902f209d41aa33455bb202bf968ebef99f92d`  
		Last Modified: Tue, 13 Aug 2024 07:39:37 GMT  
		Size: 101.1 KB (101121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba89ecc911f902ffdc68ce05b8a946d4c9dfe6834b0badbe843453dbe61e05c9`  
		Last Modified: Tue, 13 Aug 2024 07:39:57 GMT  
		Size: 359.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:0344d9075d2b5e7102ee9ba7d47f4389ccbb2dd959b2258492790012b7ea4849
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4239137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15ad05d8e8a9822138efd10511df029b10ff7963e2cfe6ff10fe1991e116738c`

```dockerfile
```

-	Layers:
	-	`sha256:3df23917d59aa302a0ed7bc885013174a9738e685b109c0cd41abf30d16a1398`  
		Last Modified: Tue, 13 Aug 2024 07:39:57 GMT  
		Size: 4.2 MB (4223345 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8386cba83bbea8f238f4918e8b5f8d5d1d74d9d730390b0e7bc812850de98719`  
		Last Modified: Tue, 13 Aug 2024 07:39:57 GMT  
		Size: 15.8 KB (15792 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:fc86b4be57cf117a0ca4558a7fb4b3dcaab78a2875da39c098636ce4d1fd6228
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67677653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e33961755717a6e4df1dccbf4721ed678520139dae487a163f29d22126c291cb`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:b4823f40fb9693690d7dfe07f6179ae1ea0a288d8912f4f8365d372e27134f0e in / 
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
	-	`sha256:c99355adbbcd3ac4e44cd6fb2596fed1658ea87be87df9894ec5aaf076a548b2`  
		Last Modified: Tue, 13 Aug 2024 00:42:55 GMT  
		Size: 56.1 MB (56074104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f49a32a7663886dda98b3e982992ab7412bbe79dc2e558114930a6f85414704f`  
		Last Modified: Tue, 13 Aug 2024 01:11:50 GMT  
		Size: 11.5 MB (11500159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e97530f82c868f8106a7554a67bb6753fe0c9c16b172aa5ecc328fbfd935fe9`  
		Last Modified: Tue, 13 Aug 2024 01:11:49 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb7445590a739b3a522581d8c7dc1ffaece3ac9e37098e8907cfb623047fa6d0`  
		Last Modified: Tue, 13 Aug 2024 01:11:49 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0630285d079475ca95c222ddec6d833d65d6eb2863881d078e45b8e086a19b1`  
		Last Modified: Tue, 13 Aug 2024 01:11:50 GMT  
		Size: 101.0 KB (101039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99ad846a8b84c1d32ae4fb5beb9b88fa142a72c6639a7ca617de7ac53da474f5`  
		Last Modified: Tue, 13 Aug 2024 01:11:50 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:0c0ac5f568dcc5d1672b7658c6b3217b4286fd142b6e8b1aabcb19f4c99d5f40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4235685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5804d6f0911db6c145a1be84d4149cdf5167f83f17d08b3c0ca9b1a4a57c0173`

```dockerfile
```

-	Layers:
	-	`sha256:54232af2ad07f640f95a2b03db33f7ad7c5507e91a07d9237d6e753d7d0f20a8`  
		Last Modified: Tue, 13 Aug 2024 01:11:50 GMT  
		Size: 4.2 MB (4220200 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a75c8cedde283c2362dcc1352ca8b9371bef2c1e4fda66ef1e0186d0a32eb5b`  
		Last Modified: Tue, 13 Aug 2024 01:11:49 GMT  
		Size: 15.5 KB (15485 bytes)  
		MIME: application/vnd.in-toto+json
