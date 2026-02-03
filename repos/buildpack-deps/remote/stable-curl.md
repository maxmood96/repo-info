## `buildpack-deps:stable-curl`

```console
$ docker pull buildpack-deps@sha256:b30263a7d9d1f1a9fa797335613ef1299ee9c130d1bed2d26e00b8e7332a4f34
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:stable-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:8b6b01787f039e30d884795211f4fdd8e23a0edae5f5797a22e754c38275a6df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.9 MB (74906962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c2b60a53190ce31b025e13e9dd83c27644fb5cc5eacb2225ccf5734403338c7`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:42:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:ef235bf1a09a237b896b69935c8c8d917c9c6a78b538724911414afc0a96763c`  
		Last Modified: Tue, 03 Feb 2026 01:16:00 GMT  
		Size: 49.3 MB (49292952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:954d6059ca7bdbb9ceb566ca2239e01ef312165659d656753d7dbace7771a591`  
		Last Modified: Tue, 03 Feb 2026 02:43:06 GMT  
		Size: 25.6 MB (25614010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c9ea60b555631b25158b68dcf03fabc67cf356f11a9754e3b36c5bc18051247f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4126999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4f8ccc2fec38c924ecadb39d686cf17b0b1e90cafb1a859cef55c26063dd1fe`

```dockerfile
```

-	Layers:
	-	`sha256:6f12ad5a5d6776035528e3a1c21247b9598145e0843e77b15cf4c2ccc3e0b47b`  
		Last Modified: Tue, 03 Feb 2026 02:43:06 GMT  
		Size: 4.1 MB (4119913 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7036b2df6461fe58796f9cbb14e35792a345472a815591af505bc80429b3bb5f`  
		Last Modified: Tue, 03 Feb 2026 02:43:06 GMT  
		Size: 7.1 KB (7086 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:e3f3aa945951224c54755f0426a81afc3b89ba04d8f46a24c787b016fb5a5edf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.8 MB (71809514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a2486eaa8e6dc97df15b060af079f25473a971352c712e077ab6ee4006ec11f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 03:26:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:ba31dc65cf53cae37b5517f251f4d408e91109de491cbd8816a9f21c33a05203`  
		Last Modified: Tue, 03 Feb 2026 01:14:09 GMT  
		Size: 47.5 MB (47453997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91afe525ee94a6eec8f0285b6d37bd019b53a0d3e972edf130127870dbcc171e`  
		Last Modified: Tue, 03 Feb 2026 03:26:40 GMT  
		Size: 24.4 MB (24355517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ca4b0e13585189f900aa4bbc5e0ab45863a35969553a8958aece3d83086dd365
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4130061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a4044e1201e16a9ead6a7f790c5efaa3a2f88c6fa0a83401bf048593181af77`

```dockerfile
```

-	Layers:
	-	`sha256:0464a7a869b77f0c23a35e5b8bbcfaa6544a405705a9547536199d1e9d125e67`  
		Last Modified: Tue, 03 Feb 2026 03:26:39 GMT  
		Size: 4.1 MB (4122903 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b302c0a65bb9e78e082dccb602bbea4d3e7858c95202336122e4cdba41b28041`  
		Last Modified: Tue, 03 Feb 2026 03:26:39 GMT  
		Size: 7.2 KB (7158 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:4f5b168407ab7579daa5195a0591566eb8c11d6953f2d840599df1f7c107400f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.3 MB (69344485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2e91e1e402006636869ea21d0ab21969368a18fa8f89bed5d76dec16da72dec`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:58:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:0f4296a8ece8abd5a409e5fbdb0cf93258815e4fec9dc768c39a63faf3c16052`  
		Last Modified: Tue, 13 Jan 2026 00:42:25 GMT  
		Size: 45.7 MB (45717820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a8e700e2f18987ab9f97abcd0497d5dfc1706a8c057e685438ce3b71d8067c0`  
		Last Modified: Tue, 13 Jan 2026 02:59:04 GMT  
		Size: 23.6 MB (23626665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a4022af9daab8fd128446e9b47577c5e05501df410609b93136282ae4910bc68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4128572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d25df1c361bc05fa243aca07409e8291bc836c1a1e61c29a535756819cb0a962`

```dockerfile
```

-	Layers:
	-	`sha256:d54ffcd94ada5d15233720a8c7468bb60f327c57b8184657eedf4e295eb849e4`  
		Last Modified: Tue, 13 Jan 2026 02:59:04 GMT  
		Size: 4.1 MB (4121414 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a3f9537cef0cd4a60c5af5d20f2e29b510bd5034bf03e4f3a2002d758d4089a`  
		Last Modified: Tue, 13 Jan 2026 02:59:03 GMT  
		Size: 7.2 KB (7158 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:ffa846549bbb651d58ec0fe396744675436cbb5046d281894edb320ec840d0bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74670719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2fe8c2ed96ba04cf6319393e8c29ff68c96d1c23523c46a4cfd9a1e086271cb`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:15:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5582010cab7f00a8f96e076b02666116eaa7e4af9a74eb44f2946a593b50294f`  
		Last Modified: Tue, 13 Jan 2026 00:42:42 GMT  
		Size: 49.6 MB (49648083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:599d5b6b6766fd729045e2e7d0396d1f61fe41c612d4aef6bb3bf5ea7db12ae2`  
		Last Modified: Tue, 13 Jan 2026 02:15:36 GMT  
		Size: 25.0 MB (25022636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6df3fcaf43359699105dd5e2720e0fc7e48c61ae4b58e6b34a8b41db8efcc593
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4128633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:766b5f17f38613bce07730dfaf3bfe8ef136fe7651f114c9c0d500a24dbcc348`

```dockerfile
```

-	Layers:
	-	`sha256:3e3619bd51407e3233d5fc9a1712d8d45d6262c1274ce286f79a79da52d84ece`  
		Last Modified: Tue, 13 Jan 2026 02:15:35 GMT  
		Size: 4.1 MB (4121455 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a017f18799b511939ea31ef74a3581f8f31fe33b9fc6e55164ed5e1fa76f9e0`  
		Last Modified: Tue, 13 Jan 2026 02:15:35 GMT  
		Size: 7.2 KB (7178 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:24088d6328926594d988210fae255478bbb6d3d69b3424a46de8f5a82d71773f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.6 MB (77577150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:861de31eb2bfcc3bd79a85e1757a273453fe03fa5220c0a5a94c0dd9d175ecc1`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:03:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:1f0b243ad587d8f60f107748ba9fe54e338921c7b90e6a5d26e1d50d32f7481b`  
		Last Modified: Tue, 13 Jan 2026 00:43:28 GMT  
		Size: 50.8 MB (50798876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef949cdbd6ae265d5239bd005e65c3d578de54ebe10474ccd2feb9708b6e1843`  
		Last Modified: Tue, 13 Jan 2026 02:03:36 GMT  
		Size: 26.8 MB (26778274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1c7588c780f957c00c72badc134ebcd9f717f2f9e39056c493bf2e617791f777
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4124079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e281f2ae5996307c77c9016ce53acf8aaae8be411573c1cfe5fe257efee98ef`

```dockerfile
```

-	Layers:
	-	`sha256:a02920076e353fdebcd8bfb2e5cd2f976f59957cc213e951fffa5d2fb49ac8a2`  
		Last Modified: Tue, 13 Jan 2026 02:03:36 GMT  
		Size: 4.1 MB (4117020 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad02a95157b3a4132ad12e70c7db8633c71a631d929fdd93ad218209cbb33fd3`  
		Last Modified: Tue, 13 Jan 2026 02:03:35 GMT  
		Size: 7.1 KB (7059 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:47d7c45dc4ae8b6277ef9ee08a7c69503b8c43441a303df703e62ee89601fad7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.1 MB (80105014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56737046c59ae7c848ea3299724d948db41113a449b5106e1bb2cf5e7d072895`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 09:15:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:6ff412c1efdf82a2030de7bb593b97f09e02e2b337f615eb1c3faedeef765d44`  
		Last Modified: Tue, 13 Jan 2026 08:45:48 GMT  
		Size: 53.1 MB (53106962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f21554c0ffe7aa9121703873815aca94dbbdf6352a46266dc923fc9e36d0d58a`  
		Last Modified: Tue, 13 Jan 2026 09:18:01 GMT  
		Size: 27.0 MB (26998052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b41bb47c086a9df336f7146e2b3c4d581690c4d493c2abb87406110dc01af896
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4130885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f7b47e80182fd7d452e326f93690472feeb200706ee885a221a76f9b7b6f7b5`

```dockerfile
```

-	Layers:
	-	`sha256:57fb69b9da141ebb54dba3ddc074fd4047a0f297688c5e200a0c7fed30995eb9`  
		Last Modified: Tue, 13 Jan 2026 09:16:44 GMT  
		Size: 4.1 MB (4123761 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:630080df278466ec098cf769c985da4b7ca0f0b1afb50df49d762370cde9a579`  
		Last Modified: Tue, 13 Jan 2026 09:16:26 GMT  
		Size: 7.1 KB (7124 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:953a04b991d3d7a0611fe965973cf3943b90400232dd97207e5e7cfbb496bb06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72723579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef7d71c6a4d4b2a66a9caa3a8fe4ecb87f80af742f20de94e5fba4c2d41cfc5d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1768176000'
# Fri, 16 Jan 2026 06:47:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:559020494fc8527e77b291bee49cdac1db6bca66f8926cda195e0e4ebe7d2d3d`  
		Last Modified: Tue, 13 Jan 2026 01:06:14 GMT  
		Size: 47.8 MB (47770843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f7f36a5fa281a3384abd9a90a26442f28edb507f1b9c537a07e1f5aaeb769a1`  
		Last Modified: Fri, 16 Jan 2026 06:49:07 GMT  
		Size: 25.0 MB (24952736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:970b78aeb305e78337b319a0880be9a023e77b0ed16ec19ce3a7ad7355190ad8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4119549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ba1c0e914965ebb49dafdbc315c3563c14d051e797e635e7afd854bdd7b61f8`

```dockerfile
```

-	Layers:
	-	`sha256:792dbab9a006e657d8bd23909e1b06c99e6b8a2347ee67d261ac404f58617137`  
		Last Modified: Fri, 16 Jan 2026 06:49:03 GMT  
		Size: 4.1 MB (4112425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff972c99913c6c88371cc6530c33f3f465080d896b017740658865328d3766ba`  
		Last Modified: Fri, 16 Jan 2026 06:49:02 GMT  
		Size: 7.1 KB (7124 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:1e03b09baffb0df719407f5bc5f6d3add3c0482645f4098af6cd9a5e27a65c48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76149095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d5eca0f9701b2e66def73f230a3325414ff1e9d8e50e55f9aa71803e9e6d3f9`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 03:45:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5578086c4ad67b3331d31c74c0b8aa3d13821b75ffa03070b0c1c80fdba7ceaa`  
		Last Modified: Tue, 03 Feb 2026 01:14:13 GMT  
		Size: 49.4 MB (49354378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef24c0cb82fa1ab6f1887f140586ec94ae060d22e6053b5747ce4acc96547b39`  
		Last Modified: Tue, 03 Feb 2026 03:45:31 GMT  
		Size: 26.8 MB (26794717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a336a411937a08cb16b99ec635388e0833eaed81799978417a1f0f94ecc226de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4128409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6c585fbe39522fd18aef158f685e58b58e40957669d80f6ac1fbb7e78579d80`

```dockerfile
```

-	Layers:
	-	`sha256:a0f18a17b103acaf9d6ccd5caefa44b15de350c0780ea1ff4bfc196842b64488`  
		Last Modified: Tue, 03 Feb 2026 03:45:31 GMT  
		Size: 4.1 MB (4121323 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3a540fa9f84d17350ce3eba9544c88bbb88d83584996e799e7c8849532af4a2`  
		Last Modified: Tue, 03 Feb 2026 03:45:30 GMT  
		Size: 7.1 KB (7086 bytes)  
		MIME: application/vnd.in-toto+json
