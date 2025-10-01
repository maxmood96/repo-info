## `buildpack-deps:oldoldstable-scm`

```console
$ docker pull buildpack-deps@sha256:bb9d696a6fe48b2ff9f75942721027ff1565f9395d54d8412be607a984d17080
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

### `buildpack-deps:oldoldstable-scm` - linux; amd64

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

### `buildpack-deps:oldoldstable-scm` - unknown; unknown

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

### `buildpack-deps:oldoldstable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:f9fbe19eae002e2d74ea1c47b92a51d60cf683c03b373f9fef27ff35a03fee6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.6 MB (114557856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:495105e91f6818415f88415923728c98a1c4327f0cba59b2e05519f1cc0737f1`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1757289600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:8274f5d2891e4b4a199e88ea54bf64be2b431cff01268ebaebfacd12519d655d`  
		Last Modified: Mon, 08 Sep 2025 21:14:50 GMT  
		Size: 49.0 MB (49044356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf7f7d1af869adfa648959578fb79545e78d3ad3763e029dfc7f93e144fcbcf1`  
		Last Modified: Tue, 09 Sep 2025 00:01:03 GMT  
		Size: 14.9 MB (14880715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68ecf2b4d23f0a78cb60113427441ac697a546595e8f7673028790822ce75517`  
		Last Modified: Tue, 09 Sep 2025 06:18:47 GMT  
		Size: 50.6 MB (50632785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldoldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:738040c96024651bc63346e82d0cbb9c0385456af0e4e448e01e37349155afc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7920983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38d5072c2b4d26fae4db32e24420daf5b5ed4db6525d0df2dfdded8a0971cb4d`

```dockerfile
```

-	Layers:
	-	`sha256:7ca8dc0c4be49a4377a4344974556aa5485c7cbe8d49295b3fe3a25c0f648632`  
		Last Modified: Tue, 09 Sep 2025 04:20:13 GMT  
		Size: 7.9 MB (7913562 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e4f675646f09b73564c098f968294c644a52b0d350727dadc511298ce9f8979`  
		Last Modified: Tue, 09 Sep 2025 04:20:14 GMT  
		Size: 7.4 KB (7421 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldoldstable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:2e29c80e6cea16c1b2958f17fb062e2238122226820ff7144c8e1a11a78ebf04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.9 MB (122854985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1922719ad5689353ac6886e441fa7262270b1f31f04fff21f177ae740de3000b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1757289600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7df02cb4a974a4e8a9eb65ffcff7274f9dca341d29aaa763294c42e49805ca19`  
		Last Modified: Mon, 08 Sep 2025 21:15:41 GMT  
		Size: 52.2 MB (52248370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32c26dea2f52a9cb0633591a828e9fd53a32d89290a8c2b4b5d5286f76f5332d`  
		Last Modified: Mon, 08 Sep 2025 22:20:05 GMT  
		Size: 15.8 MB (15750666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3b8f2ae237d2864fee9f12b950708d56b6e76bc6595e309bb307eade128f989`  
		Last Modified: Tue, 09 Sep 2025 02:13:06 GMT  
		Size: 54.9 MB (54855949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldoldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:4988d25af8fffc1d515cc5e0c7f8b3c4d1242fb4c8641ad572cacbcdeab946f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7925331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2921327097c576d6ca3c5c64a9c9382e9685455def8e626152196e6e9545dc9a`

```dockerfile
```

-	Layers:
	-	`sha256:747b6391bfb701e7411b72e15f80038d0236d37e3f84c0021ff48c9e54afc3ca`  
		Last Modified: Tue, 09 Sep 2025 04:20:24 GMT  
		Size: 7.9 MB (7917894 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9ed60bf54836bebbbdb1818354f03cd59c3ade6d79aa4282abcd781b9e51c42`  
		Last Modified: Tue, 09 Sep 2025 04:20:25 GMT  
		Size: 7.4 KB (7437 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldoldstable-scm` - linux; 386

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

### `buildpack-deps:oldoldstable-scm` - unknown; unknown

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
