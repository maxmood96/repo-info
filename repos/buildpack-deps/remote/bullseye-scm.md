## `buildpack-deps:bullseye-scm`

```console
$ docker pull buildpack-deps@sha256:ce9187824ef25a8fea2f3594609a64438a6ddbfa02abc27b324aa741030ff674
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `buildpack-deps:bullseye-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:bd73c1652d62f93e5372b9e7fd9f2fbda2b982921671adee3223fca21289c78b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.1 MB (124051950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c8c836a09f3c40fef1d7128da690478855525d53797ee2ee8149088b7947cd1`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1742169600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:8d1bfb80edb9306e3de72f4095daeae4c281712482255562f2e236ae85233e7d`  
		Last Modified: Mon, 17 Mar 2025 22:17:19 GMT  
		Size: 53.7 MB (53741275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aae550f4768ad83c7dcc1ef8de6de078a33effa152d846f4604ead4cbb1f414`  
		Last Modified: Mon, 17 Mar 2025 23:13:33 GMT  
		Size: 15.6 MB (15558355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a322d21cc1b9c3e86a0528fd885e7483a3b2497c1448256bf87a4493be665ab0`  
		Last Modified: Tue, 18 Mar 2025 00:18:59 GMT  
		Size: 54.8 MB (54752320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e3af98a4f7288e993cd06641e94b7694c368a698a5a8703f9b65a8193668a2df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7715538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51706afabcf3017516124b53ff13565f74d087cfabc195f504d0329d13afb2c6`

```dockerfile
```

-	Layers:
	-	`sha256:5f63239a24562358e316da634b5782c173c39c04cfd791b5b3e7e3a267f85d67`  
		Last Modified: Tue, 18 Mar 2025 00:18:58 GMT  
		Size: 7.7 MB (7708186 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0aed8044feecbc20f3de4da8410165c083ddd42da327870f84369f8c61396479`  
		Last Modified: Tue, 18 Mar 2025 00:18:57 GMT  
		Size: 7.4 KB (7352 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:10e160a2eb0a598ff915afbf442a63a6f15cd0eb86ecbed306258c7d18d6c8be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.3 MB (114340798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a12ad997df4877b7df4accab549c62377b24a1248240a97106692b881b09584c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1742169600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c0fd1793bf8bc1764ff6503ad6f86ae0f1151de2bd8b7285b28dc6f5cc6001c3`  
		Last Modified: Mon, 17 Mar 2025 22:19:04 GMT  
		Size: 49.0 MB (49026561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9fd5d78189f9a0219a8d445519fe59067dcfa82b8799cf047c0b783ffa33a78`  
		Last Modified: Tue, 18 Mar 2025 07:26:06 GMT  
		Size: 14.7 MB (14674012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d31183489ce2b77443c42eee08badb4a4fcf8ad4cef9299e71603f2239cb4064`  
		Last Modified: Tue, 18 Mar 2025 15:29:13 GMT  
		Size: 50.6 MB (50640225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:4b30558451369a042a41509e315b4af7bd6c5943c1b09d29728aa44a76085055
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7716999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49e54ca69d57410aa74b8c1aca0d2f60c77294d27773f85f62bed3c796932cef`

```dockerfile
```

-	Layers:
	-	`sha256:b78426ab7d42bf3b5e9816c311a81fc89a56c9c51738973b044c229460e106c9`  
		Last Modified: Tue, 18 Mar 2025 15:29:12 GMT  
		Size: 7.7 MB (7709588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07f9eb1ad504ac11b040e08db2d363b5b5033ef7a264fd77d27bb2f6b6ec07e5`  
		Last Modified: Tue, 18 Mar 2025 15:29:11 GMT  
		Size: 7.4 KB (7411 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:7f1026b07b63993af6f67082f1323e0483736116985768c6934becad68c06045
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.6 MB (122647827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:873909f1056dd5c37ea7f3cbcf0f9d97cb2d030699c3f32cc9053e360d4a6bb4`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1742169600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7d61d9dafd0c900d9eaa97f9411b10213d45699b9afb91aee676649c07fc4a51`  
		Last Modified: Mon, 17 Mar 2025 22:18:23 GMT  
		Size: 52.2 MB (52248394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:645bc92dcf4a3c806f112acf0724041051eab86b13816f8d7286950facb47ec3`  
		Last Modified: Tue, 18 Mar 2025 05:00:00 GMT  
		Size: 15.5 MB (15544004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a96fedce3b84d801b5eec66fa2ddb4a4653be64f8e04188e6e7ab37b6566bd34`  
		Last Modified: Tue, 18 Mar 2025 13:15:20 GMT  
		Size: 54.9 MB (54855429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8a203b452fdd6f02cb43402ca189d1b43834471c0f22fa9a48d96c4d7233492c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7721353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4548cd58ed0576a4e3cb1527072904171cbf4af08ecb051da0ace17926fd803`

```dockerfile
```

-	Layers:
	-	`sha256:32a8ace573f3e839059f8f6909ee3ffe11e85417b9240dd5a1480a7744511a85`  
		Last Modified: Tue, 18 Mar 2025 13:15:19 GMT  
		Size: 7.7 MB (7713920 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12001a112e798ec919e1451a40eace7cb3b85e59e85fd397db4a653a514d50c6`  
		Last Modified: Tue, 18 Mar 2025 13:15:18 GMT  
		Size: 7.4 KB (7433 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:7dfc091a89f87179f66cf3ef53909d34a792b8713e83d11c586f1621729539c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.8 MB (126770670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f39a9e57cdbaa07550e355aeb52c79cb7d676eac7864a5faca4e944d9371c01e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1742169600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b2bf052a55a1540734073d8a106c4845ec09ac4ac8cc46a275584d3eef876deb`  
		Last Modified: Mon, 17 Mar 2025 22:17:43 GMT  
		Size: 54.7 MB (54678617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e5503af74d5075005e8a2caef8b6b369ec49cf0d7a20dcdd1fe79d68aa4ba6c`  
		Last Modified: Mon, 17 Mar 2025 23:32:34 GMT  
		Size: 16.1 MB (16062045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cfffc7337857c58b61734136d663ca328549ab864bf18f3217e50e3fdc25680`  
		Last Modified: Tue, 18 Mar 2025 00:18:53 GMT  
		Size: 56.0 MB (56030008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:feaffbb25ac74d42bb1992c2e711f926232839809374b298c8463c92de37f215
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7711006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afeb46c188c98148928e4a8d4476e4cc1613b9dc387754983f430c34e6c6d81d`

```dockerfile
```

-	Layers:
	-	`sha256:202cad62c131e60480ad23efffe89b069f938bd646d56fa02e9fe8d6aa189254`  
		Last Modified: Tue, 18 Mar 2025 00:18:52 GMT  
		Size: 7.7 MB (7703676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e9bc2af8859be4a8c57dc9015df3a283f521ae4f10045330a8b6d47e39ead37`  
		Last Modified: Tue, 18 Mar 2025 00:18:52 GMT  
		Size: 7.3 KB (7330 bytes)  
		MIME: application/vnd.in-toto+json
