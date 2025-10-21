## `buildpack-deps:bullseye-scm`

```console
$ docker pull buildpack-deps@sha256:d47c15749df9dce9043afb9117061d3cb65ce798c53e1f8fd09a071da6894938
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
$ docker pull buildpack-deps@sha256:954bfe5953048ed118aa47068b46219507c3b887b199c21445b53b546494997e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.6 MB (114553880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86b8ba6f47973dbc8e6e2933dc94ecc887745f90d2b8d2bbce5e6091f32611af`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1760918400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:680ed921e0c94a719af1d242eac2d0c1be8482153680a3940f3435ee5598303a`  
		Last Modified: Tue, 21 Oct 2025 00:20:24 GMT  
		Size: 49.0 MB (49046121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30c68013a317d7d802bb25c57a724c8753caec2fc7f0e78fc13f9a38fd22ecd4`  
		Last Modified: Tue, 21 Oct 2025 02:44:25 GMT  
		Size: 14.9 MB (14879264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:895fddf2807e047e5b02e5418fd04d343d3e9b5b393b2f3f0cd6704cad44b8f0`  
		Last Modified: Tue, 21 Oct 2025 04:10:49 GMT  
		Size: 50.6 MB (50628495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:04a93d9f1422231f6d603d19e7a723508d2382a40b23215a91fd445786ab2b41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7920985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:681ab9e74ffe8e77beecbfe2e8c5c25126af9ed6e99864bfb9aad0d42154b23e`

```dockerfile
```

-	Layers:
	-	`sha256:8fa5a717aa2c037809fe9640d7c2c068ff19060bc513aeb41b5ba9b58a5dedb5`  
		Last Modified: Tue, 21 Oct 2025 07:20:10 GMT  
		Size: 7.9 MB (7913562 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3783405965009463f5747e6320466144b7fad44cce63bb9fa8aebe956f4e2758`  
		Last Modified: Tue, 21 Oct 2025 07:20:11 GMT  
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
