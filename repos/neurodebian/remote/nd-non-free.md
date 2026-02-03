## `neurodebian:nd-non-free`

```console
$ docker pull neurodebian@sha256:3f7505cd2a98c7b65a1686ec9196357a8c77b8f9e87d476ac19a198abfe87cbd
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
$ docker pull neurodebian@sha256:a34bd5c63c5d4d902f50950efd6ce5dca64b1addf6060d5cb0d1249f0cbee543
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60288827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:308f8f8e8e8be830f406d62dc791fd094ace9d9714082e5a38b94de80c022113`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1769990400'
# Tue, 03 Feb 2026 02:49:08 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:49:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:49:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 03 Feb 2026 02:49:12 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:49:12 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:e5dc831051d738f5c1db4254dde56feb7c9e75e136e23995d896f1b6e1ba752f`  
		Last Modified: Tue, 03 Feb 2026 01:15:47 GMT  
		Size: 48.7 MB (48654703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce7002f3da964c57bd455c7ea9aea032a614f96ad162a44a4e3be7f438517c9a`  
		Last Modified: Tue, 03 Feb 2026 02:49:20 GMT  
		Size: 11.5 MB (11540369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:582397b9dc850b850ffd74061feea99dfb6b237c0192d6191177bd0a6cd86b64`  
		Last Modified: Tue, 03 Feb 2026 02:49:19 GMT  
		Size: 2.6 KB (2634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbfae06b9f53d369e6035db2bb25acc88db5141f15668b9c187df731a53d6330`  
		Last Modified: Tue, 03 Feb 2026 02:49:19 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae0675e38a13a9ae911bed6a859416965f3afb652c0c0bde63d3aa4b7c256fd8`  
		Last Modified: Tue, 03 Feb 2026 02:49:19 GMT  
		Size: 90.4 KB (90432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28a622e4dd49c0b33475fbc290bee154d0d2fa0f6b39499fc01581d935969bf0`  
		Last Modified: Tue, 03 Feb 2026 02:49:20 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:e40dd2e539b3db456883132b1b1edd605a481e44ded2b819881cb3566719049d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3623628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a040ca843f8191579ffafa4b24724273fd39a8d8db116dbf48cb294a674d25ac`

```dockerfile
```

-	Layers:
	-	`sha256:80d0cd2e330fc9bf7aa1ae15a2864ea8ed86232bb2bdabd6bdfc79ab09150396`  
		Last Modified: Tue, 03 Feb 2026 02:49:19 GMT  
		Size: 3.6 MB (3607697 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d44da38342d0de406e284f67ea9541752f7cdaec248b21cc9996fbba57ab3770`  
		Last Modified: Tue, 03 Feb 2026 02:49:19 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:42:02 GMT  
		Size: 48.8 MB (48824718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c9a5edd52237009e0cac583b17514f638b5d8f08eedc3930a2e812e893bd6c7`  
		Last Modified: Tue, 13 Jan 2026 02:38:53 GMT  
		Size: 11.3 MB (11283894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abc58c09ec95440415b943959da0113ae578e6d378ab910c68074397ee96024d`  
		Last Modified: Tue, 13 Jan 2026 02:38:52 GMT  
		Size: 2.6 KB (2631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e3e2db745e5179dd8918931028318ac50146b5c7f4ed70102c02afdf323fabe`  
		Last Modified: Tue, 13 Jan 2026 02:38:52 GMT  
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
		Last Modified: Tue, 13 Jan 2026 02:38:52 GMT  
		Size: 3.6 MB (3594105 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9fdaae74eb9cff639961a564fad50873ac2bf56d2c0ea39128352527d6b9e666`  
		Last Modified: Tue, 13 Jan 2026 02:38:52 GMT  
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
		Last Modified: Tue, 13 Jan 2026 02:15:35 GMT  
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
		Last Modified: Tue, 13 Jan 2026 02:15:36 GMT  
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
		Last Modified: Tue, 13 Jan 2026 02:15:35 GMT  
		Size: 3.6 MB (3591187 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3c08d2228b8f636f2a594f5106ad6f754469e440be86a8eb81b47366aad1557`  
		Last Modified: Tue, 13 Jan 2026 02:15:35 GMT  
		Size: 15.9 KB (15901 bytes)  
		MIME: application/vnd.in-toto+json
