## `neurodebian:latest`

```console
$ docker pull neurodebian@sha256:593272b6e12292a86529e7cf49d9b14013978495950ec97d74773b64b662fa4c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:latest` - linux; amd64

```console
$ docker pull neurodebian@sha256:5a6560e98de0074d4f556e3a3d723a82ddaf0ae65f34cda741c0584e755c69fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59845610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80daaf772d06e04317a105c593b722bf4830f53083a1c3041236aa8f303df83d`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:8fb375ec14f3df8b31b70d0216508565ab7264a7e16cac4f8cc07f8eca22445f`  
		Last Modified: Mon, 08 Sep 2025 21:12:37 GMT  
		Size: 48.5 MB (48480610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cc68ad6246d17dbfc153a24bae65f1a5f73ff584955429a8236e563aa3d001f`  
		Last Modified: Mon, 08 Sep 2025 22:48:31 GMT  
		Size: 11.3 MB (11269479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76a1c1b4568c9392569145efa49e13b53064de29748b4330157f35fe17d3c28d`  
		Last Modified: Mon, 08 Sep 2025 21:42:51 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa576ad08b5522d438407cf741520c4be3638d6c6f66e9080164d0e470978c8e`  
		Last Modified: Mon, 08 Sep 2025 21:42:57 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d3c1b0722585c6a8c19c079e8987ed2951983f7aed063647f1b7f7fa3133937`  
		Last Modified: Mon, 08 Sep 2025 21:42:59 GMT  
		Size: 93.3 KB (93346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:latest` - unknown; unknown

```console
$ docker pull neurodebian@sha256:814f7556d4158f8a1e283388b3c402e0654227d8a269ee0ab181e6b21f434b69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4089860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2579c266cae1e084172b034d8c94e5fcdf1519765bb54f306e76f79b625b0dea`

```dockerfile
```

-	Layers:
	-	`sha256:4eb751fc0f69002c0dfaadfa36ab65ef9b01d64364167eb630243f00f1019f08`  
		Last Modified: Mon, 08 Sep 2025 22:07:34 GMT  
		Size: 4.1 MB (4075544 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea1205fd63d05f019c473c467d0b5d0792d62a875286ab84731f3f8b99040391`  
		Last Modified: Mon, 08 Sep 2025 22:07:35 GMT  
		Size: 14.3 KB (14316 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:latest` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:c21dbd0a1b16c4fb222391d8e8e637e2922cdaa24fe9ed526552317f113eec9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59810755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:008b6ced829a9d58058b2cbab03447436e078b2409fe75b5b1378777ba39b2ba`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:37b49b813d9cadbc816aea22a15ef76898c66b4db015fea88b8f15bf213d5004`  
		Last Modified: Mon, 08 Sep 2025 21:13:28 GMT  
		Size: 49.6 MB (49643746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d54f0a8b8cdeb016765b4421672e7132d34ac6b326223b731d5282d5c3ae095`  
		Last Modified: Tue, 23 Sep 2025 17:39:19 GMT  
		Size: 10.1 MB (10073260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96ca08b2ff60dcd56cef5ab73acd2c160b4e06751f62df7e0e95d1bcfd11d8d6`  
		Last Modified: Tue, 23 Sep 2025 17:39:18 GMT  
		Size: 2.6 KB (2638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e35bc05e600c15f0db597abe53e56f5133f1a07cef5ceef2dde74108818d40b`  
		Last Modified: Tue, 23 Sep 2025 17:39:18 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87503a3dead3a4605bff54bd22c67f01d31f31f6b7c17460c90ae59af2d30d76`  
		Last Modified: Tue, 23 Sep 2025 17:39:19 GMT  
		Size: 90.8 KB (90839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:latest` - unknown; unknown

```console
$ docker pull neurodebian@sha256:20da5439101ef73faac42cf32c8dacca771cdd9cdce9a342d0499874e2dfdc62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:000c048359af5327f48f359238ffbbbf20737b7e60535c97db620c1ebe6f0cab`

```dockerfile
```

-	Layers:
	-	`sha256:c8c473610319b2e88f677aca463db980bd056b2466974dfa73007cbbb5f01c33`  
		Last Modified: Tue, 23 Sep 2025 19:07:45 GMT  
		Size: 3.6 MB (3614508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6cb37a93695cd94314c8d98c7d617488ec6ee93baa6906bb6aa6804b7f9e796f`  
		Last Modified: Tue, 23 Sep 2025 19:07:46 GMT  
		Size: 14.4 KB (14431 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:latest` - linux; 386

```console
$ docker pull neurodebian@sha256:557a466129fe8cd12edbf882dc0ebf898652e8b101e0138a9fce8af68ef67f16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61351348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77e7b84e0788bd3a7eeacb70c4ab0929b84ccf10892c9650e34e5bec7ca21199`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1757289600'
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c9dedb413b4079d00183873186dd00dae4338c64e4152f334d39473e37deb8c5`  
		Last Modified: Mon, 08 Sep 2025 21:12:41 GMT  
		Size: 50.8 MB (50794950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:768b3fdcc0892aba7d97f3db5214e7a8724b3691fbe410f5aec7c9f7729c19e4`  
		Last Modified: Tue, 23 Sep 2025 17:34:19 GMT  
		Size: 10.5 MB (10462915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d13e953626a5863b8c7828fd4ed69028cf735723c389479008359be4d9edd990`  
		Last Modified: Tue, 23 Sep 2025 17:34:18 GMT  
		Size: 2.6 KB (2634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:980b88e4c67b14fb8d1d73a427f8fcdf3eb95789988d2d91ec6970cc6c22bd58`  
		Last Modified: Tue, 23 Sep 2025 17:34:19 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3482123fd30bdde26844e46aa5360dc605124e27e13b22a8e44866fbc344d156`  
		Last Modified: Tue, 23 Sep 2025 17:34:19 GMT  
		Size: 90.6 KB (90579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:latest` - unknown; unknown

```console
$ docker pull neurodebian@sha256:3b4d14f31a3774572ceef81ad84383cb0c1ae39ebd131510cfcda15a3630d172
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3625191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a86f3fa91eb5042a491e37386d2d34c7c933cc12376225de8f5eac7702a61a2f`

```dockerfile
```

-	Layers:
	-	`sha256:93eaec6d2f1f521fc263252d9ca16cb3a360a3af7531bb55ec9c8264df60460c`  
		Last Modified: Tue, 23 Sep 2025 19:07:51 GMT  
		Size: 3.6 MB (3610930 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d5f4614670f64ec9fb8c7b72d96283e5b91deb0d9f10815b2ac4881be86ae82`  
		Last Modified: Tue, 23 Sep 2025 19:07:53 GMT  
		Size: 14.3 KB (14261 bytes)  
		MIME: application/vnd.in-toto+json
