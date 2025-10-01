## `buildpack-deps:bullseye-scm`

```console
$ docker pull buildpack-deps@sha256:0579c3613f561ea5942225e8d87667cb07f9051967123a0d43d4ef7252be3255
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
$ docker pull buildpack-deps@sha256:e27c7e13f8a2d9189aa1bd2cef7659f1aff481cb5ba0832077d0bcdf5b5371fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124276170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0da68afeccb92d66cd47c8c33c0785d5dbc0435debe54329d39874439d96e67`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1759104000'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:10ffc47270cd106d2d04bc7ef4749d579620e45a84804ba3b18f0898fe5ecc64`  
		Last Modified: Mon, 29 Sep 2025 23:35:07 GMT  
		Size: 53.8 MB (53756064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:840feb027ec25230e94a2f7f4414d50952ed3e6c6fc69a711b34ce7938a2dcdb`  
		Last Modified: Tue, 30 Sep 2025 00:10:31 GMT  
		Size: 15.8 MB (15764102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aab467d29752c57d2c01fec39d489ac683e5cae8e5554713067baf3203fa856`  
		Last Modified: Tue, 30 Sep 2025 03:17:35 GMT  
		Size: 54.8 MB (54756004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c5b76d76159a5ed08c621f0c13ad7a4fcba36f2ce2c2015bd195ed363f80f3db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7919519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e80c7f6639ab6df70fb56b50752052f187f17f658664a1c7fcc59470f04b79a`

```dockerfile
```

-	Layers:
	-	`sha256:8ba8743d8e0d155cdd6bad076fe011f97ccc59a5b136f0e8a6468643e787652f`  
		Last Modified: Tue, 30 Sep 2025 22:35:12 GMT  
		Size: 7.9 MB (7912160 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c03ffa85cd87bb368f7a766df6ec7b016141d78143487660bf11a4ec6003467d`  
		Last Modified: Tue, 30 Sep 2025 22:35:13 GMT  
		Size: 7.4 KB (7359 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:fdb24a5b9482b34f4c5c96a24ac407f0c3ea1719b1f9e4162ad44f6454f04f76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.6 MB (114555505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ed989a670bd896b4979515178f18f59209752976d375f2b2dbd4077cb44b039`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1759104000'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:48c74e0c7f4820f85dd12f127039bbbc28eb9159c3b96ee4a97479e469ca271b`  
		Last Modified: Mon, 29 Sep 2025 23:34:24 GMT  
		Size: 49.0 MB (49046061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e17788e6ce4b362e582a71e64fdd7b6468048effec65882098d34fc7587c523`  
		Last Modified: Tue, 30 Sep 2025 01:07:06 GMT  
		Size: 14.9 MB (14879270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e8d3ca9464d084a846394ffb79d9843779d9cc36c2ef243753ca26993b52971`  
		Last Modified: Tue, 30 Sep 2025 02:39:12 GMT  
		Size: 50.6 MB (50630174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ab85fd44254484b9f0b99a59b3151a44f93adb29da88f71657fdb9e437b60b12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7920985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25ca02b4ffe236897195d3733c78140a0bcc6aa836bde2bef7196a88eeffebbd`

```dockerfile
```

-	Layers:
	-	`sha256:f2196c7d4ec459024e1b1c0233774faecd2a1ee8abe95f2efe804f214881c7a4`  
		Last Modified: Wed, 01 Oct 2025 20:46:57 GMT  
		Size: 7.9 MB (7913562 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f839280403604bdf677cb9652b0c2de254b24077f818869f3aabfefe08d115a`  
		Last Modified: Wed, 01 Oct 2025 20:46:58 GMT  
		Size: 7.4 KB (7423 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:fce412433f4bf3ffc12478bb316b52cee3dad82322a9c1c27f97ca270878968e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.9 MB (122860890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85acfa8a0d594520591f146156cb80385bcd9710594844c0e539c3ac7f3a78ad`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1759104000'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:9b16ae1bbd1ada84c12528379a10e280bd89e0d0332670c8487145eb77fe2fe1`  
		Last Modified: Mon, 29 Sep 2025 23:34:42 GMT  
		Size: 52.3 MB (52257414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed44f1c4305e990c6301b16db5ccb0849b5044d4eab021969a1274b1471f5cdc`  
		Last Modified: Tue, 30 Sep 2025 00:13:37 GMT  
		Size: 15.7 MB (15749303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d06d88b67dfc22f54e531fe9bee90e889b90f5349a5ac5473af85c6967813b62`  
		Last Modified: Tue, 30 Sep 2025 01:19:29 GMT  
		Size: 54.9 MB (54854173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2d581d4fabe344827f894eac558d7787dc1d9791c0c7ec8f1e9cd88a88b3798d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7925333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:623965615381bd563d61591e8700e9ad5c08c0e9805c065cdb95cc7c4adb1be4`

```dockerfile
```

-	Layers:
	-	`sha256:81492d54a954e00388f2dd1bceec82f9474c58577b7cc0f5c9eeeeb64fae7fba`  
		Last Modified: Tue, 30 Sep 2025 11:46:27 GMT  
		Size: 7.9 MB (7917894 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab30c971f448b08faaadb20a30bf78d8749d27fe9dffd7fe1661bda09f3f86ab`  
		Last Modified: Tue, 30 Sep 2025 11:46:28 GMT  
		Size: 7.4 KB (7439 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:f4ffbf85147d94ed443eaa8b4eeea21538d44d38621622557430be33e01a4974
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.0 MB (127015332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3762be4a16910da9dda2bb3582874074866cd941bdb04dbc32cdadc5a632e9c2`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1759104000'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:ceabdec1cb201cbc144cbbf99606ecccc3942e0acc3ede261d7cced4e3f632e8`  
		Last Modified: Mon, 29 Sep 2025 23:35:34 GMT  
		Size: 54.7 MB (54699245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3f70b590df86e9bb29cea47ff5206076a14d6ec7a2d599a47314d5c807427f8`  
		Last Modified: Tue, 30 Sep 2025 00:20:26 GMT  
		Size: 16.3 MB (16267769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49eba0f07bb8b54d93c18e8046612f1ea91d973cf657c81818dae53819cabca4`  
		Last Modified: Tue, 30 Sep 2025 01:19:09 GMT  
		Size: 56.0 MB (56048318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5d0c518aac2a7e79f185b5d2559294b35558110b393843dbce675482e812c75e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7915067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3959dd8ae6e2f0cdbd9103bc5363ca03322f362cc0b0b825af8be14304a9eb4d`

```dockerfile
```

-	Layers:
	-	`sha256:fe011be3c966d8384cda7345e2afa38a78a966fbd66d6a574906dd6bc9aaf673`  
		Last Modified: Tue, 30 Sep 2025 16:36:33 GMT  
		Size: 7.9 MB (7907730 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad6b7812f229df480b20a415c66759582c293c90e13500a6a974a56a74e0bf19`  
		Last Modified: Tue, 30 Sep 2025 16:36:34 GMT  
		Size: 7.3 KB (7337 bytes)  
		MIME: application/vnd.in-toto+json
