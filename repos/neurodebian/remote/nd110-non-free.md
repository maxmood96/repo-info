## `neurodebian:nd110-non-free`

```console
$ docker pull neurodebian@sha256:6d2974fe43af719acd5fe2f15ed2b7ea3cefc0e1a0fadc31ccbb1fafd1ae2b7d
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
$ docker pull neurodebian@sha256:37742f33147749a7cf8493b1c57e513137caf3a39237ff5fd69d05e9741843d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66289886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:198e3b59f16736e7d1b4a215fb775f60a8db597df22072c3d4e56b031dbb14cb`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:e1bdcceaa316a43ad58ce8cf054a8e89ecf5a0dbae8125eb85e9b26fdb2fca2b in / 
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
	-	`sha256:ba83bbfca9443648a883d1404b33faa0f5e096a99a2b683e3bbaee8912bca845`  
		Last Modified: Wed, 04 Sep 2024 22:34:34 GMT  
		Size: 55.1 MB (55081329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:498f1488fe0ce4f68ba65588e42a509359c780aa37830c58b5bc532049f3df06`  
		Last Modified: Wed, 04 Sep 2024 23:10:31 GMT  
		Size: 11.1 MB (11105001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48078c64027e315d16c3372a517ad0c996c3cf427cc76e93e09b8930683d4a89`  
		Last Modified: Wed, 04 Sep 2024 23:10:31 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f6ab9cca1215b9e090b5fd61f543c95516ad130be26f239a6350ddcbcb06643`  
		Last Modified: Wed, 04 Sep 2024 23:10:31 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a912325e1f8f7ad2107b3ed37ccfb31fd6cf24f60f829b87f710ce0e7285083`  
		Last Modified: Wed, 04 Sep 2024 23:10:31 GMT  
		Size: 101.2 KB (101204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1377c99ace9afbc4b630d2ad13a2ad54f2797a1ad5b02d255712c5274cabbfc`  
		Last Modified: Wed, 04 Sep 2024 23:10:32 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:02560e1e69409480316a22e0c128252d8158e8447af63065e8ba0dc7661e4c39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4239252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeb3a370621af6b03463d135102fdc5b70dd52233d202435895b030bfad0fd63`

```dockerfile
```

-	Layers:
	-	`sha256:fb9f5d0bf90cf2c36528627b064a061e2884c4b8ce20b8725eca76988de7c219`  
		Last Modified: Wed, 04 Sep 2024 23:10:31 GMT  
		Size: 4.2 MB (4223740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ccc908c641f6d66494192e645327f8e109f089102893e1f99551a0b8a7cb6b20`  
		Last Modified: Wed, 04 Sep 2024 23:10:31 GMT  
		Size: 15.5 KB (15512 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110-non-free` - linux; arm64 variant v8

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

### `neurodebian:nd110-non-free` - unknown; unknown

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

### `neurodebian:nd110-non-free` - linux; 386

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

### `neurodebian:nd110-non-free` - unknown; unknown

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
