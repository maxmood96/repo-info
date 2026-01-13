## `buildpack-deps:bookworm-scm`

```console
$ docker pull buildpack-deps@sha256:c2cd1a7cbcb7fdf65b706bba275d3d6ba2c0b0a1754bbb09dcb48e52b9c94053
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
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:bookworm-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:8c0dcb9fbccb7b4f9ced24cf3b4810f85d3f53e622126491539932f337ff0b39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.9 MB (136906230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9e8915dae19b23f0ac6baa777d71de52fdaa21332bb1ba6c058ebfca55d9f68`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:44:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 01:22:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:32a5bf163bd75109aaa8d446f1570117432475cbb2df3fb6f89dd243bcedd1f3`  
		Last Modified: Mon, 29 Dec 2025 22:26:43 GMT  
		Size: 48.5 MB (48480796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16afb0fdc4694732853f4fbf5125c1dcb35f20cca5bec77a98d73d0d3124f855`  
		Last Modified: Mon, 29 Dec 2025 23:45:17 GMT  
		Size: 24.0 MB (24029344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a858b7813255a9cb57d05f02b50978e5b5965b0cfc040288fa29905cdc65ad9a`  
		Last Modified: Tue, 30 Dec 2025 01:22:58 GMT  
		Size: 64.4 MB (64396090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8e4eca8318f86aaa59f2c4b6460132fd18c72123832016e63189673c5270b753
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7972714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7334d0fc6e313a778639bd8441400104d74c5290c53c3fc189fecad7ee4e6c9`

```dockerfile
```

-	Layers:
	-	`sha256:2c66c297f77c26c5e4a5e60ed4c1ff2958bd7c9c4d33b645383d2efeca6ed515`  
		Last Modified: Tue, 30 Dec 2025 04:21:45 GMT  
		Size: 8.0 MB (7965405 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:70c101bb28e1ffd1cbdfa00ca49c144be850fbf065fd94591a349ec7ca9c84b6`  
		Last Modified: Tue, 30 Dec 2025 04:21:46 GMT  
		Size: 7.3 KB (7309 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:931e127a8271f72624d9f402ed8e9fdf57a4b86bfac66483fdeffdc1dd4eb324
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.7 MB (130738435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5103f8adfa028ca44607ec976c48a38139607d2056a1b338ad62126c45d3c704`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:28:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:07:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:3328d590af06d44e564f37191fbae5238775007425643c6f6e4f3136ae883b75`  
		Last Modified: Tue, 13 Jan 2026 00:41:51 GMT  
		Size: 46.0 MB (46016731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5bceff052bbfb51ccdda1b71d208734d7536dbc22a0d2c8310def26afcb3273`  
		Last Modified: Tue, 13 Jan 2026 02:28:56 GMT  
		Size: 22.7 MB (22712635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1e4250b4026270105a4d93c8bfb01a0581bf77b1bda3c2e5b6bd1ebd71b621f`  
		Last Modified: Tue, 13 Jan 2026 04:07:58 GMT  
		Size: 62.0 MB (62009069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f71c6f66ac76c922522b5aca515630d56e5a9d5b6cbee7bcf6287b6ee329dacb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7975280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18d908224c790b8fe10696779add37f4d31742d1efb85154dce3d9b5bd36cce1`

```dockerfile
```

-	Layers:
	-	`sha256:792e314aa279dfe5ef1641ee168033cdd09691d92cf192c5e741914571aa00bc`  
		Last Modified: Tue, 13 Jan 2026 05:22:12 GMT  
		Size: 8.0 MB (7967906 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2ea12985a31ac347a575063523dccdd7a765663915c31e77b5bfe0b421cd82d`  
		Last Modified: Tue, 13 Jan 2026 05:22:13 GMT  
		Size: 7.4 KB (7374 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:e032153db319fbd7ae52bdb7c262898d0b400e1e9e32d966e23052fdb3b004ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.8 MB (125792339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f59a8c52ebcc6ba0785e3e2d1900d9c2b8895d699113490aabaf7af41e4646e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:57:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:24:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d1f8df344790c402ed8a818bba76e9111f5e212418c662cf0574919edf68933b`  
		Last Modified: Tue, 13 Jan 2026 00:42:15 GMT  
		Size: 44.2 MB (44198845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b61baedfd715aa7493fd2550daee1914be821a60dd0067158988236109172a`  
		Last Modified: Tue, 13 Jan 2026 02:57:25 GMT  
		Size: 21.9 MB (21941488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a97f9f395cd1e9e02761196527b4253d5246be969781795c278996437891e5cf`  
		Last Modified: Tue, 13 Jan 2026 04:25:12 GMT  
		Size: 59.7 MB (59652006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6e332b7f913a1917da4a175f6bb19fddc02e372c8ad6908ea0f977ee02a92638
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7974699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa89959bc3868549edd0f071dd3bb424b3c1a1daa1606708b11aefa828d54356`

```dockerfile
```

-	Layers:
	-	`sha256:5812e6fd4aaf90367198484bb2695175c97d3297981166f3e4d4c52e226f3826`  
		Last Modified: Tue, 13 Jan 2026 05:22:21 GMT  
		Size: 8.0 MB (7967325 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f28cbeaa43a00e9c8d2c6b22f6819e2677caaa6729250d18a6e8821281d77f5`  
		Last Modified: Tue, 13 Jan 2026 05:22:22 GMT  
		Size: 7.4 KB (7374 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:23f3534866d0fadead49f3488bcdf663a332307681a315530cbb0a663b313454
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.3 MB (136328695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8209db6362cee8570b99b29ebba5bae041f83cfa2043a0782fb2bcccd7446470`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:45:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 01:24:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:bc82f51ad2e6d256131f87c3aebb045333f03c39e64a6b4985cc9e6ea5602d4d`  
		Last Modified: Mon, 29 Dec 2025 22:26:42 GMT  
		Size: 48.4 MB (48359147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b14a03c2e7665cfd5dcf91d78e753eaacbe124548ced748ccf44fdc600c28e4`  
		Last Modified: Mon, 29 Dec 2025 23:45:53 GMT  
		Size: 23.6 MB (23598380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:885a684c982cb8679ba82c9c939ec2b3cfe9c823a68d404ebbc3ac75d14830df`  
		Last Modified: Tue, 30 Dec 2025 01:25:21 GMT  
		Size: 64.4 MB (64371168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c6f1cc7065621bb3921a3ce6663ea1ec60706a11a565ef6afcb521b22f4e3d04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7979188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4af94e48b78678e127aaec4ac9cdc060a4d8aedf4891fbac05ecc5f24ad0bd31`

```dockerfile
```

-	Layers:
	-	`sha256:fbc5014ca112c5a8469dd8b7b6b588c8ea72d8359e0cad1a292169489c72f20a`  
		Last Modified: Tue, 30 Dec 2025 04:23:29 GMT  
		Size: 8.0 MB (7971798 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14a6046646aa6ad3cfc862381e876205963e0a85a67ca16d8bae0b1fc18cde08`  
		Last Modified: Tue, 30 Dec 2025 04:23:30 GMT  
		Size: 7.4 KB (7390 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:6c42a90c6d9fb3ce5043967a108731d0951d0e66f3ebb2324da51dce0a4b2009
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.6 MB (140574185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7b7689f912c52c7569e08086028c04a0ae1dd0913426410d792bad3b377ecad`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:02:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 03:03:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:2ec54d337d067729b748c8f421e417d2e02e79e9e0caf328deaa1b815a93c883`  
		Last Modified: Tue, 13 Jan 2026 00:42:07 GMT  
		Size: 49.5 MB (49468594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63ef3b5e8322d4c8e5ca6198e931fb91c384bac3ef8aafd81a71617e9534b7ab`  
		Last Modified: Tue, 13 Jan 2026 02:02:23 GMT  
		Size: 24.9 MB (24871330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20be0f262f5ef3547fc45c5726dd33bf707569fc1cceccb9f87c4f4965c4f9ed`  
		Last Modified: Tue, 13 Jan 2026 03:03:50 GMT  
		Size: 66.2 MB (66234261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:bb87ed36dc4b1d67774048748a454e64cf5873e2c8a58c7e81cd89c24b56c7fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7969494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53907d8e139384b6e35e0695ad4b6718128680d496987e98e8d75958308ce6fb`

```dockerfile
```

-	Layers:
	-	`sha256:bac890056e1e034b049f1d9a9e31dc2a11f21dfd1be266b64086d84703b6bbfe`  
		Last Modified: Tue, 13 Jan 2026 05:22:36 GMT  
		Size: 8.0 MB (7962206 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f084d150ea2e463a8b630941aff1282246154ba09e4ba4726522a0bffdb01dc`  
		Last Modified: Tue, 13 Jan 2026 05:22:37 GMT  
		Size: 7.3 KB (7288 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:fef74f7617cc0e34dd2af58c29a15786ae530addf25ca9f2ffd80f2c56fe688e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.7 MB (135684228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a52cc93ae2827f1e67b79ee69285b26e55911ebdff127192de95098a750320fe`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 11:49:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 17:13:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:6a43d59f754c088126249c7de1413be451574eda24274414bef9aea85a3ac886`  
		Last Modified: Mon, 29 Dec 2025 22:38:14 GMT  
		Size: 48.8 MB (48760925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ec26c7ec0c76b4716fe076707c8489ced71c06858c4f9f03f18c306cb4344cd`  
		Last Modified: Tue, 30 Dec 2025 11:50:06 GMT  
		Size: 23.6 MB (23613812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a2269474ce0b0fca7a225e6021a034ce6b526a7a59bdba22d740e8cee0614ec`  
		Last Modified: Tue, 30 Dec 2025 17:14:42 GMT  
		Size: 63.3 MB (63309491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:530a506bcd2813aeadf57b3354bbb304144def0031f0ba65b26ef6b8aa7791a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 KB (7143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc82d0a00a34492bccab3e43ea3352260af1c2205ac40f5a6a58493bbc79f656`

```dockerfile
```

-	Layers:
	-	`sha256:76e62f91044fe26a61d0cdeb7427b2a43b81690eafb6fdca3fbda6864c1c62bb`  
		Last Modified: Tue, 30 Dec 2025 20:20:11 GMT  
		Size: 7.1 KB (7143 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:3de4b01bb530b916875ad1feb067d361583f33b16fb1ed08d627a9f43b55abae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.8 MB (147844693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:647d518d6dba8be1ba9e63dcac76f7eb8769a7e55e64db7d3e408a274f186326`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 01:30:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 03:16:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:48e256c4119c0ad256492d6a930e99d2b2d7f8d7920d619aa2de4f616c37076e`  
		Last Modified: Mon, 29 Dec 2025 22:25:39 GMT  
		Size: 52.3 MB (52326998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7517c515ac5fd6799cec288b72512b8ea3fc54d2d37de5af54d06ba0ea2f21bf`  
		Last Modified: Tue, 30 Dec 2025 01:31:20 GMT  
		Size: 25.7 MB (25672165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f30ff2cfb691fedcba1692cb13fd0632001d1a876833f4cd2aa52eba87257a8f`  
		Last Modified: Tue, 30 Dec 2025 03:17:48 GMT  
		Size: 69.8 MB (69845530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:82612951063554984e4e00097959a6ffef3bbffa7a16a54f338b21ab0f662a0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7980615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fbc27abbc03e3ae006b3ea5043f7eaf96878e77bd091d1f745e1b663734040e`

```dockerfile
```

-	Layers:
	-	`sha256:220379fad1f73ca2cfa85573c9fbbcd46cfb7a0ef036838be873878a407dc8ef`  
		Last Modified: Tue, 30 Dec 2025 05:20:46 GMT  
		Size: 8.0 MB (7973276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba29cc6d4ca262543c9298380ca562ddca17693abb5c9beea5ce3ec4184c4de8`  
		Last Modified: Tue, 30 Dec 2025 05:20:47 GMT  
		Size: 7.3 KB (7339 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:0dc975b3b1b6bef64aa74fce3d06915ce03425937da29dd5cd97f7f6a505742b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 MB (134672197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3fd5ea1c8d24a8a8243bb5f0394e666b1e8f9b5c2a59d346313400b762216fd`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:09:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 03:14:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:533e1723f6efd3a2dac5ef2d710062f1e6292bf061b83d41b908fe862b8922dc`  
		Last Modified: Tue, 13 Jan 2026 00:40:26 GMT  
		Size: 47.1 MB (47138430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8133db08df54d1100dff2f0259f057251959db22c09d939ae558af001aa8088c`  
		Last Modified: Tue, 13 Jan 2026 02:10:04 GMT  
		Size: 24.0 MB (24032491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fb4cc23aeea1b258f198103e8c2d450f82da1d5de8a3eb227ed2969f60d97c4`  
		Last Modified: Tue, 13 Jan 2026 03:15:34 GMT  
		Size: 63.5 MB (63501276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:45377a2000d5817f0fc931e36841cfea7c4102e0f45495b58abbf7e9db8e41c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7969671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:449f3ba88c7e3f9774d1ac9bbdf4e2a41aae1f770f1fb8d99371b21b23332f7b`

```dockerfile
```

-	Layers:
	-	`sha256:6c358d26de9d1e16b089fbc55b0ea0c3324814ff88086e29a016a596b6c81321`  
		Last Modified: Tue, 13 Jan 2026 05:22:53 GMT  
		Size: 8.0 MB (7962361 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bbb4d5935cf2629d0aea1568243a59f6ce7e310a2c7c3399d7faf0bdc40a3ca`  
		Last Modified: Tue, 13 Jan 2026 05:22:54 GMT  
		Size: 7.3 KB (7310 bytes)  
		MIME: application/vnd.in-toto+json
