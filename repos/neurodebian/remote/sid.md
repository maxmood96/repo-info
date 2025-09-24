## `neurodebian:sid`

```console
$ docker pull neurodebian@sha256:28ed00c3b99a93843498bcdf4dbb2e106a98bd6f09cb16cb0f429c7287b5b92d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:sid` - linux; amd64

```console
$ docker pull neurodebian@sha256:3a7c2310d559960aaf251bc55abe9a2ab7db5737be3afbf4fe917255a3297e94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60150107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:237a847b33b05b4e89235d3b6749d4840276b001e4738669e669a1a496565414`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1757289600'
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:8d64c6c7c21822ac171c4c396d70161707401d6d50d133075d661956f08dc756`  
		Last Modified: Mon, 08 Sep 2025 21:13:08 GMT  
		Size: 49.7 MB (49657990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d854924ae9b4b1288c9dfda064ea896d3981b318987c9c6ffe8efb82e63325d9`  
		Last Modified: Tue, 23 Sep 2025 19:50:14 GMT  
		Size: 10.4 MB (10399375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2e96eca8e251a3599c0646fff211e1ad902995d9c8f4cdcb9aea901bbe51fc8`  
		Last Modified: Tue, 23 Sep 2025 19:50:09 GMT  
		Size: 2.6 KB (2634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9b127e8318640efb0fdf4c7d5c155014b89218f931be0840c2468e892e0fe82`  
		Last Modified: Tue, 23 Sep 2025 19:50:11 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f94e92357646159f3de34f7a59b35af379809eb95e8ca6cdebfc80f6bf415b5`  
		Last Modified: Tue, 23 Sep 2025 19:50:11 GMT  
		Size: 89.8 KB (89839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:db93141dbaaab047d2c5961e0f3a40a490a3bc4c02858e362684aac66d8f11cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3623887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40ec5dfabfdd39f0aaf814e90273b851f03175e48b64cc6bdc82acd7e035dd64`

```dockerfile
```

-	Layers:
	-	`sha256:b3b0384cfc3d61d143a214949d2e595f859d287f885e4e4d78e634cc601b3ca2`  
		Last Modified: Tue, 23 Sep 2025 22:07:41 GMT  
		Size: 3.6 MB (3609940 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15b8bd663afd20bb3f9e9dd8d1902aa8ea08259a6ff7149fc262d1757f040bfb`  
		Last Modified: Tue, 23 Sep 2025 22:07:42 GMT  
		Size: 13.9 KB (13947 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:3473d74285345688dad026ef0917211d20aaac7a63891d8b253c51ac76c7f36c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60205188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3780f0e6abc99ad711f80a483189a852bc2a1d2bd2d9ce913bc7f0a749388490`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1757289600'
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:00e024daab2d43f36749bffb01f2b299b405cff0659a8e4f4f00bb468dd24c27`  
		Last Modified: Mon, 08 Sep 2025 21:14:58 GMT  
		Size: 49.9 MB (49934721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67162de59cae8432f37018bdfca1926d8d40b34084a6e6ca535064ebafd11af7`  
		Last Modified: Tue, 23 Sep 2025 17:39:57 GMT  
		Size: 10.2 MB (10177061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30bb81dbbd87423aed66a55483c3b6d0acb4129dabd3c0147e74c76b0addb550`  
		Last Modified: Tue, 23 Sep 2025 17:39:56 GMT  
		Size: 2.6 KB (2633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bba3ff27e7afe1dc3962ba33f3faa4fbaba125ab630cb86d1125223c943c68d6`  
		Last Modified: Tue, 23 Sep 2025 17:39:56 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a03b9f2f2b5433c7d521cd2962c537a2863678d15ff9ec8e3d1f7d6a4677c1ca`  
		Last Modified: Tue, 23 Sep 2025 17:39:56 GMT  
		Size: 90.5 KB (90502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:5f6b3b64165dd6cf8115298360e079d70eadbd2cb05021d0f0e61c82e695744f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3625527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:631b4c7bfa49457dfcdf6c8869cf60c5f244c01f22f3bab8aca7e9c5ff4d4d68`

```dockerfile
```

-	Layers:
	-	`sha256:7d39ac1ae9919d67a330944d83252b6fba745ae3f16dce0326e07afcfb619d25`  
		Last Modified: Tue, 23 Sep 2025 19:07:54 GMT  
		Size: 3.6 MB (3611455 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b646a4ca03999ebf0a0e86482bbb39a1c31c084ad7112cd593dc386c8241932f`  
		Last Modified: Tue, 23 Sep 2025 19:07:55 GMT  
		Size: 14.1 KB (14072 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid` - linux; 386

```console
$ docker pull neurodebian@sha256:087bfe5c7fe5a858c0dad888bdae06c7aa709dd89a70dfd28b9efb1eecb2a247
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.8 MB (61758851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c9911b404ee218bf7821aafaf7618a81634351f6f5577a865753205cecbce39`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1757289600'
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:eb039ce3bcf3fbed73729096e510ae45e98c7db73d412a09aa57aaad6f2f6267`  
		Last Modified: Mon, 08 Sep 2025 21:12:53 GMT  
		Size: 51.1 MB (51113613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fc41e7d47140b0d1fc4152bc7af8595e60e5b75abcc8d92b17c1e4bccdc2777`  
		Last Modified: Tue, 23 Sep 2025 17:35:59 GMT  
		Size: 10.6 MB (10552105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edeabcf2a16d8446d9f601b7a5f0e0dcc7eec713032a5af69f0e62133b4d0a5e`  
		Last Modified: Tue, 23 Sep 2025 17:35:57 GMT  
		Size: 2.6 KB (2634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62a81e3c095adac2afeafbb59a941a25173e7979c43c100a882514bea7877cf2`  
		Last Modified: Tue, 23 Sep 2025 17:36:00 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2a5f5e7ce5e4c5bd3868fbeb258a1b9acc9bf9658887f081960ec7b90b4c574`  
		Last Modified: Tue, 23 Sep 2025 17:35:57 GMT  
		Size: 90.2 KB (90230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2b4e860b4c2cf391bdc9ff71e490d986221996da51ec3a24f0cfd46a85c4480c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3621820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a62dabffd47060461fc93e44830dedddbd7576c04f5afea31f63b493c1da5551`

```dockerfile
```

-	Layers:
	-	`sha256:9896fe7c4d9ef11f9576f83857d7f2ba9fdadb7b07a9a04d20d5e2e494dd447f`  
		Last Modified: Tue, 23 Sep 2025 19:08:00 GMT  
		Size: 3.6 MB (3607901 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09cc604acd1809bed7d56e0d91d55d2eec5d7d859506811fc30bc2c91a6f86fc`  
		Last Modified: Tue, 23 Sep 2025 19:08:01 GMT  
		Size: 13.9 KB (13919 bytes)  
		MIME: application/vnd.in-toto+json
