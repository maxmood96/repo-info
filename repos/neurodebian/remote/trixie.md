## `neurodebian:trixie`

```console
$ docker pull neurodebian@sha256:8cadca06c88fb1316bd4eba824a2d0cedde36346b2da7c0fb838226de770e49c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:trixie` - linux; amd64

```console
$ docker pull neurodebian@sha256:22ba4c69dfacb7993f7fcf3708c2ec38e7a15ed1bed206d226c5160e47273847
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.5 MB (58516023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6fd9c4b14dc331719047f53a409b7b3093d384a6ff135c95b14e664c6b43885`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1733097600'
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian trixie main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:e4743b5a77e386ff2c8b73b5f4786349b4c3b4a5bba77f60a49c3b94a3b29584`  
		Last Modified: Fri, 13 Dec 2024 15:34:48 GMT  
		Size: 52.1 MB (52113554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e31fa211153a834040c35ecc855708df74ae143e0f067f5f29d4299bec783171`  
		Last Modified: Fri, 03 Jan 2025 23:08:15 GMT  
		Size: 6.3 MB (6309046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:759be46808786c18908d758383834044fed05ddaf818585877931072aaa3bea3`  
		Last Modified: Tue, 07 Jan 2025 02:50:02 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47b9340f215c3f9e9497b17c7dcc21314a53d5553d70c1a45f9ecd9663aa523c`  
		Last Modified: Mon, 06 Jan 2025 19:56:38 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:809dd25b48752fba0eeac0fcf5c38a88f0e12b0db0b022acf82ae7fafd98800f`  
		Last Modified: Tue, 31 Dec 2024 09:25:24 GMT  
		Size: 91.4 KB (91435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie` - unknown; unknown

```console
$ docker pull neurodebian@sha256:6b22d1f83ebacbb4392e9e1ec31a9e0902f3f7a2cde703ee063fc39bfcd1b648
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3577932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b9d1493dabbbd58df5573fa3c3dc733bfb235815353be42c104a85da39f4758`

```dockerfile
```

-	Layers:
	-	`sha256:8cfad2f41e51e9ca8348d9d7852f9a0f81c5d0a482874503181c168442d46e8d`  
		Last Modified: Tue, 07 Jan 2025 00:52:57 GMT  
		Size: 3.6 MB (3564266 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:291ee8d275476a4f56b64a69bb3c484a527878d207b0f47533dc5df2c24f9458`  
		Last Modified: Tue, 07 Jan 2025 00:52:57 GMT  
		Size: 13.7 KB (13666 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie` - linux; arm64 variant v8

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

### `neurodebian:trixie` - unknown; unknown

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

### `neurodebian:trixie` - linux; 386

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

### `neurodebian:trixie` - unknown; unknown

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
