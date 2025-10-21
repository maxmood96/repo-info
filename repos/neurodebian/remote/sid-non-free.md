## `neurodebian:sid-non-free`

```console
$ docker pull neurodebian@sha256:9bd27c3bc7b5253f0c3226d2712e9b7f1ecd4ec5edaa11f03c6c863e4d6768da
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:sid-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:3a7b03eae23373adc7f4797d63972c0600ec9adbf050bc2f65020375d4fd72ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.0 MB (60030519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18a936f54e3e3fb9ed08a06d30adc731f696f07b9d62bfab0aba457cd08f66d6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1760918400'
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:767319f7ad72179f876946bf5b239f862d2d5ad761041b6e449acd3ce4c0bdde`  
		Last Modified: Tue, 21 Oct 2025 00:19:58 GMT  
		Size: 48.4 MB (48383307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ef0bd306c085e0d9172bf7465142fb444c97a324135965ce5f87bd943359a51`  
		Last Modified: Tue, 21 Oct 2025 01:48:20 GMT  
		Size: 11.6 MB (11554128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7db591813a3859f1c875db7d03736704beea3c0eafbf8fe46856a4c300570be`  
		Last Modified: Tue, 21 Oct 2025 01:48:18 GMT  
		Size: 2.6 KB (2634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ecfe9da75e8e5d505b08f0e5e108f3525d32ed146a4b61d464d459cae2c3033`  
		Last Modified: Tue, 21 Oct 2025 01:48:18 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:758f72300e0a26bae0fe567acaeaf7d1518ca74ba76f13595adf5e943960da31`  
		Last Modified: Tue, 21 Oct 2025 01:48:18 GMT  
		Size: 89.8 KB (89763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9599c70bb4ad4d506b83672510c05b33e76d4319cce66e73e216bc3aa6bf11c`  
		Last Modified: Tue, 21 Oct 2025 01:48:18 GMT  
		Size: 417.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f6e6d4473c60ac11fd516bfd50bb2347b953252fbd5a06dbc3778627f9d71183
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3591975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2be6f49cf6ea102f20699dc387e85ad4730aba76d5881c287eaa6d181cdbbc04`

```dockerfile
```

-	Layers:
	-	`sha256:642d6011514f28f40fee2f55d27a981db70fdea023345d962e9890fca8486a5c`  
		Last Modified: Tue, 21 Oct 2025 10:08:57 GMT  
		Size: 3.6 MB (3576001 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8e31c9c575de2ccb5e5b4910cecb45f70622cb53cb4c66aac58f235a56172de`  
		Last Modified: Tue, 21 Oct 2025 10:08:58 GMT  
		Size: 16.0 KB (15974 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:76dd51b7d628ebef8b0a046ac4395f348da3a39cfaafc4a534de8a1e293e89e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59891954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0d69a9f67c34b548f0606b6ba44ddc243d150da75f68289c41acb197cb0d8bd`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1760918400'
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:e43e2837b589215836966b2f88d71f57e2c4d5e8f8cb435d19f6ca010856531d`  
		Last Modified: Tue, 21 Oct 2025 00:21:19 GMT  
		Size: 48.5 MB (48506031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd67243de293f26b725ea615d2f0e15b929f581e1a5f0ce82e28978d04596bb5`  
		Last Modified: Tue, 21 Oct 2025 01:52:28 GMT  
		Size: 11.3 MB (11292178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa5c4a856701954dd67681ab2f54aa0b71579e52d83f1282d4768c500fc2aa4d`  
		Last Modified: Tue, 21 Oct 2025 01:52:27 GMT  
		Size: 2.6 KB (2630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb0427437bd76102aefdffcb59cf50392c2c15c276d2eb482d019df9c7718003`  
		Last Modified: Tue, 21 Oct 2025 01:52:27 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a962cafff807b0d481a181fef61ea8de5bb7a34103f3fbe094fbe20953c92663`  
		Last Modified: Tue, 21 Oct 2025 01:52:27 GMT  
		Size: 90.4 KB (90429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33671d4c3fab47b3ad0c11de0c9bfdef12fcafbcf84107da772bd4e8579b3800`  
		Last Modified: Tue, 21 Oct 2025 01:52:27 GMT  
		Size: 417.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:3a1413f605257adc6e875b122eee0550d79191a4244c06f0b59aeba49ea1c29c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3592991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a19d10f1a00e967892969d6ecd09a402a983ecb07c7749ad50190017c5efcc55`

```dockerfile
```

-	Layers:
	-	`sha256:3f4c472099e374cac91f770e1475881c2edb2a52b5bb930f06dd97f1fbdedda2`  
		Last Modified: Tue, 21 Oct 2025 10:09:02 GMT  
		Size: 3.6 MB (3576877 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f920c5892f08f55068e3862ed5afcecdf8941a4b6c6b4da17bc10a490311f012`  
		Last Modified: Tue, 21 Oct 2025 10:09:03 GMT  
		Size: 16.1 KB (16114 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:b8b04e408922e8e0037deb27e669fa92a4c2b3eb6f4d2779f391a03985bc0975
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61537589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d397abf3b90cabb0ac8ef969df0097a4a1d6ac4e9b46fc96fdafc5d76d6c72d1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1760918400'
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:c10cb3338a430a2ff28907bb8e87eec0d18b9eda310d3dbee0b9f6e1108bcaaa`  
		Last Modified: Tue, 21 Oct 2025 00:21:24 GMT  
		Size: 49.7 MB (49718167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6263729212fa24d688b0e089aa21d4d42b0a9b2eb0b8cba38c6c434a061b62c`  
		Last Modified: Tue, 21 Oct 2025 01:55:55 GMT  
		Size: 11.7 MB (11725976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dad57c5e770b81f2167932e7f4cc7b3d4ece39254ec42121687158f4534a767e`  
		Last Modified: Tue, 21 Oct 2025 01:55:52 GMT  
		Size: 2.6 KB (2631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bba61575e7e3a1bf2390add264c736dcc789bb14a4cb77113509efb1feba8feb`  
		Last Modified: Tue, 21 Oct 2025 01:55:52 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:681bf1529eccfb3133758475f67f0e4b7094045b95e354c391c2519d50e2bb4f`  
		Last Modified: Tue, 21 Oct 2025 01:55:52 GMT  
		Size: 90.1 KB (90130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a7d01f9f824f5e715767625a8168d13679c87e2bd7d639e1a1b6852c9d2026d`  
		Last Modified: Tue, 21 Oct 2025 01:55:52 GMT  
		Size: 417.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:5e449d2828e8db6082e96f0ba57918bbc73580a4eca072f7f3edece9e2c29422
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3589908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4765ab2c4299f54c8fa77010ba0d5108aeeb524477ae3dcd1b13f1ed45b8356e`

```dockerfile
```

-	Layers:
	-	`sha256:1169f578ae145181d478afad1410324050c505c2e9c5bbc69463e9524f227fbf`  
		Last Modified: Tue, 21 Oct 2025 10:09:07 GMT  
		Size: 3.6 MB (3573964 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:895fe37261301b538d481791ab9f9f065b91570d2ddf98845322619c922753e3`  
		Last Modified: Tue, 21 Oct 2025 10:09:08 GMT  
		Size: 15.9 KB (15944 bytes)  
		MIME: application/vnd.in-toto+json
