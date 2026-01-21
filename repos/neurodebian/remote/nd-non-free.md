## `neurodebian:nd-non-free`

```console
$ docker pull neurodebian@sha256:0b630c00c5070bf23631871f269b8293c6027e2f30a895ea73746f2ed9b4b936
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:nd-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:883eb0b954b83d7480c8a3678cbc8ae5d0acb09156daa78de63f88d0c7be2215
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.6 MB (60567727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f103c35caa70fa2e598bbf9b8e5d389f44a144527d5ae15a2ec8e3bbc2b1be6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1768176000'
# Tue, 13 Jan 2026 02:35:36 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:35:36 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 13 Jan 2026 02:35:36 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 13 Jan 2026 02:35:40 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:35:40 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:b2184fb6462644b6acf50283df065d3d00ff827c80b1fe7de520944b5c1333b4`  
		Last Modified: Tue, 13 Jan 2026 00:42:32 GMT  
		Size: 48.8 MB (48841950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa19ca8127c7609765102d825c06a722be6aa2a704ad10ba538de570a72b6c7e`  
		Last Modified: Tue, 13 Jan 2026 02:35:54 GMT  
		Size: 11.6 MB (11632256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c78ad8f8ce96a8a0161687f8d72d7ce31047f9e79c01cc6d465e0f2520459fd7`  
		Last Modified: Tue, 13 Jan 2026 02:35:48 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2174da5053e56df9335e9b85f225136e8dc9397d0594a3c1fd6850ee2f8bbb7`  
		Last Modified: Tue, 13 Jan 2026 02:35:53 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:220bbb1b36941bb7f746471dbd6af8c3dd4662bade8d99d05f24f13912b51c8f`  
		Last Modified: Tue, 13 Jan 2026 02:35:53 GMT  
		Size: 90.2 KB (90201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:181a2da67b8e3991dcb1f417001cfa2694d49106dcc0c91c375c094c1af0bc27`  
		Last Modified: Tue, 13 Jan 2026 02:35:53 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:4ceb7efd5cc791e93223c656e87687a09bb780e06359f7b203d71b3883af59a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3609160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4898b9290d6b9bc8ce40cdde772e085e81442a757a7a24bab3635b2cd8aa9744`

```dockerfile
```

-	Layers:
	-	`sha256:86e4d90f97512714d41888dd2c03de4c8d3dfe00af68c592810d378d4c23225d`  
		Last Modified: Tue, 13 Jan 2026 02:35:48 GMT  
		Size: 3.6 MB (3593229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25234269e6f4b00858be9f4f0c989c43f66a8e3594d8bc59f42bf51e559e473c`  
		Last Modified: Tue, 13 Jan 2026 05:09:23 GMT  
		Size: 15.9 KB (15931 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:0c396589891d3c617ca0410ea2ff3ef8c48ab233cd8826d253a933bd2501b5b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60202796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:427aa2ced9486bd12be502f9419345de174c5654292a3ce2ff4d35ea097d7a95`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1768176000'
# Tue, 13 Jan 2026 02:38:40 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:38:40 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 13 Jan 2026 02:38:40 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 13 Jan 2026 02:38:44 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:38:44 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:6d947e77c03f512510d8bed1eff4f80727f54732f6ae212199524bdf89493609`  
		Last Modified: Tue, 13 Jan 2026 00:42:16 GMT  
		Size: 48.8 MB (48824718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c9a5edd52237009e0cac583b17514f638b5d8f08eedc3930a2e812e893bd6c7`  
		Last Modified: Tue, 13 Jan 2026 02:39:00 GMT  
		Size: 11.3 MB (11283894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abc58c09ec95440415b943959da0113ae578e6d378ab910c68074397ee96024d`  
		Last Modified: Tue, 13 Jan 2026 02:38:58 GMT  
		Size: 2.6 KB (2631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e3e2db745e5179dd8918931028318ac50146b5c7f4ed70102c02afdf323fabe`  
		Last Modified: Tue, 13 Jan 2026 02:38:58 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43d8c2ee79391cf1b2076de818d699484239f70dab0332479d0eb6876eb76d24`  
		Last Modified: Tue, 13 Jan 2026 02:38:52 GMT  
		Size: 90.9 KB (90868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7407bf616dbd5929f5d38b6b8161c64ea318bef988d826e2db12e1c7bdfa6b3b`  
		Last Modified: Tue, 13 Jan 2026 02:38:53 GMT  
		Size: 417.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:c40f5ce3cfbbb278253579b56d9308fe52a4d1238982cb42d68d999e8e92b88a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3610176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62d60536309a11b855e32b84990e0453efdfe7827f3a33e9562615a2ea3d04f5`

```dockerfile
```

-	Layers:
	-	`sha256:9690eb218fc781102f03827a207ea0cff9fff756f8122a35552468f93250a736`  
		Last Modified: Tue, 13 Jan 2026 05:09:28 GMT  
		Size: 3.6 MB (3594105 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9fdaae74eb9cff639961a564fad50873ac2bf56d2c0ea39128352527d6b9e666`  
		Last Modified: Tue, 13 Jan 2026 05:09:35 GMT  
		Size: 16.1 KB (16071 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:29c6f2d2701bc0d15ab7aecb27bd6a46db79c8e5a7816d1289882bfa328a0cc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.8 MB (61815677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c093d6a9a0e2ddba9eb0857a20960b123f24417c1896d87284b76f837efa073`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1768176000'
# Tue, 13 Jan 2026 02:15:22 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:15:23 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 13 Jan 2026 02:15:23 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 13 Jan 2026 02:15:27 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:15:27 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:621ee2827046628793df0c5176988fc0eef90eb94ab1b862f17e074ba6064e3d`  
		Last Modified: Tue, 13 Jan 2026 00:42:41 GMT  
		Size: 49.9 MB (49943816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca115bc00d353cad320bbfd72a4e71bd2d894f06113dcb9a17030fb18e14aa4`  
		Last Modified: Tue, 13 Jan 2026 02:15:43 GMT  
		Size: 11.8 MB (11777974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:109172636f5d8d15495a86c47640b8833da31afa49dac51dc788d331d51b4194`  
		Last Modified: Tue, 13 Jan 2026 02:15:35 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cabaf41752bbfa6fc79aa7258daafcea5cd5ad20b4ad9da0d86b1e88d1a8bedb`  
		Last Modified: Tue, 13 Jan 2026 02:15:35 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c2d143b59110518f6bd31d6dd22cb9813ce4fcc6f91f1241d926ef3b57c95d4`  
		Last Modified: Tue, 13 Jan 2026 02:15:35 GMT  
		Size: 90.6 KB (90564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09d2cf67c8b76bf197f0430f4758d401b3dce448aa47698c1733eaf18167b00e`  
		Last Modified: Tue, 13 Jan 2026 02:15:42 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:304666b92baad6e4035e011a329a7d8bbd4352a94a1bbb7dddd27d4dceb391f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3607088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c456b6dd20574b34e286d508e125f0c53668b0932f7c6882109698912166b43`

```dockerfile
```

-	Layers:
	-	`sha256:0a44ae40c2d9af50ce8fb40c7a0100941164bfd8490f4e7115b2766a546e667a`  
		Last Modified: Tue, 13 Jan 2026 05:09:39 GMT  
		Size: 3.6 MB (3591187 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3c08d2228b8f636f2a594f5106ad6f754469e440be86a8eb81b47366aad1557`  
		Last Modified: Tue, 13 Jan 2026 02:15:35 GMT  
		Size: 15.9 KB (15901 bytes)  
		MIME: application/vnd.in-toto+json
