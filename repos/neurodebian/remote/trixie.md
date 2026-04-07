## `neurodebian:trixie`

```console
$ docker pull neurodebian@sha256:2f4c470979405f043d5816a2dba54ca07331e342b4f9a7db2e47a6c3478f43ab
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
$ docker pull neurodebian@sha256:6c104489228738831d5ca33b6baf71ce5cfc18b9e9f7bc0d14ae6a445dfe0c60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59684086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36a3c00b85430bbc08735ae3ead27683573e91bf9af2e8f1dac4561f50996dc0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 02:01:06 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:01:07 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 02:01:07 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 07 Apr 2026 02:01:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a7730063fcfe708b222d34c4f07d633dfe087a28c05c4daaab2fa9943854c155`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 49.3 MB (49297833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:491dd2c1ce4a7e4b47bb0f8c8b741e73a78e971f2f0b5f576c0b20ea8c265992`  
		Last Modified: Tue, 07 Apr 2026 02:01:21 GMT  
		Size: 10.3 MB (10292926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5499acfb1e6832771a0807da2c835d40a0fcf56fa1e829aadeca0574f98e59cf`  
		Last Modified: Tue, 07 Apr 2026 02:01:21 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da3cda9db193172c74664130719db3132d8bbab1895244ff787f388fa27e8be9`  
		Last Modified: Tue, 07 Apr 2026 02:01:20 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa31249a55d68e978373b17a3a29045fda264a2f48ce4546b00e5c7df843de9e`  
		Last Modified: Tue, 07 Apr 2026 02:01:21 GMT  
		Size: 90.4 KB (90419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie` - unknown; unknown

```console
$ docker pull neurodebian@sha256:5013919ccc9ef92983a73ab94bea9b759b6e5d9bc0b349a0c5578a57eb01196d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e767760a21268d05f2acda8a74b7dec0ca65ac8ecab817a8234bb4383d5b57f2`

```dockerfile
```

-	Layers:
	-	`sha256:c537c6e052c78b4e59bd6777ddc6484a9a231f89d686f491afbc066bcf392bca`  
		Last Modified: Tue, 07 Apr 2026 02:01:21 GMT  
		Size: 3.6 MB (3614104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27f9d0e0748809704210bd279c94b612a1fc365276fff4575ac4651202720d38`  
		Last Modified: Tue, 07 Apr 2026 02:01:20 GMT  
		Size: 14.3 KB (14251 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:58d1bd7459c21ab1d7a283920ce3c6da18d960096352c0ccf2535b25d1a4250d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59837190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8775e554e09da19bca8c4c969d979b5900d0dfc4e5faddca26558b30c893ff2c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 02:04:03 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:04:04 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 02:04:04 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 07 Apr 2026 02:04:07 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:912041a7b9f63b6550d3a3949c43e45f74a36a2f80c727e70e41cbe851de2d20`  
		Last Modified: Tue, 07 Apr 2026 00:11:19 GMT  
		Size: 49.7 MB (49665256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9e31d89380ba732a0406195a80e8d1f3739c5ccfd5c102147c23a0a8f4708d7`  
		Last Modified: Tue, 07 Apr 2026 02:04:15 GMT  
		Size: 10.1 MB (10077988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2483c2d3147352a96a1061695bd50cecf1a77bf57f3a77aac478c02f0f67ef8f`  
		Last Modified: Tue, 07 Apr 2026 02:04:15 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e2751667ba5d31911e37cce1f7dfd23821525fb957928f5faa8a6cdd36d3b61`  
		Last Modified: Tue, 07 Apr 2026 02:04:15 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:420205519c6217769acfb298c60c3c469bdb5371378721822ef809caeae63ca7`  
		Last Modified: Tue, 07 Apr 2026 02:04:15 GMT  
		Size: 91.0 KB (91038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie` - unknown; unknown

```console
$ docker pull neurodebian@sha256:b30f0489d7276af845415c7260183e991fc4cd8e77740cce7ec7d7e141690b15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3630019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6f8839bd68e19d91358b5a5abd666a7a4e5fbd79c831055c5c36fe6db305ae5`

```dockerfile
```

-	Layers:
	-	`sha256:4ba20350eefa715ad7383f1264c935f46d9475f86c079fa66d4a2a7eb7cb8de7`  
		Last Modified: Tue, 07 Apr 2026 02:04:15 GMT  
		Size: 3.6 MB (3615631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1fbf8fad5f0b3b5169e280dc6798fe61163081b0b66a7b5f3e18062d3ca4f133`  
		Last Modified: Tue, 07 Apr 2026 02:04:15 GMT  
		Size: 14.4 KB (14388 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie` - linux; 386

```console
$ docker pull neurodebian@sha256:422c2755b2e1bb2cd368b83e6a6e2c89ab0a54fb5f4848d7e2e4f6a8f220e7ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61379806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:545007a21b6e79e48db521a82a8df542d7e10a15a63e5d34df7a68e6b0e17388`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:48:21 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:48:22 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 01:48:22 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 07 Apr 2026 01:48:26 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:cdc6802f3021d1c2b9488d1de8ce2706686229997f4dcbab2461da2a3a1f115f`  
		Last Modified: Tue, 07 Apr 2026 00:11:26 GMT  
		Size: 50.8 MB (50819088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aae1f0fbac6a88be9dcb23c571da82da088cadda19b034b842e84cfcaa28f452`  
		Last Modified: Tue, 07 Apr 2026 01:48:33 GMT  
		Size: 10.5 MB (10467068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:754115c41d1776cec3df85c51bf394a2902c4eb791f82968f19c476a4eb2c6ff`  
		Last Modified: Tue, 07 Apr 2026 01:48:33 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da0f12721908b18e9c6e9b6ceae633014052eeaecf3932e098fd33b5c039692a`  
		Last Modified: Tue, 07 Apr 2026 01:48:33 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a0d1e672a9c3716d3995031e1bccf1c7cdfc458eae2a4dc4586cdafed0da19`  
		Last Modified: Tue, 07 Apr 2026 01:48:33 GMT  
		Size: 90.7 KB (90742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ca41842e4de756490c8d6ea1114951e8a19bb5e3d1a854c8a444b58430791eb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3626270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ee0777bbabdcec9770ecc591bd196cf2bf6b83641b2694d4bb341221b144989`

```dockerfile
```

-	Layers:
	-	`sha256:df67e9a01457161fed449645509b7c5c64fcb4132915e5ad855cd6dfe596865a`  
		Last Modified: Tue, 07 Apr 2026 01:48:33 GMT  
		Size: 3.6 MB (3612052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c16755d7777b7d788fb820ba0fc72234a522326dbec9d099a8f50ae45927358`  
		Last Modified: Tue, 07 Apr 2026 01:48:33 GMT  
		Size: 14.2 KB (14218 bytes)  
		MIME: application/vnd.in-toto+json
