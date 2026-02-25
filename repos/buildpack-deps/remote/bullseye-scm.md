## `buildpack-deps:bullseye-scm`

```console
$ docker pull buildpack-deps@sha256:d669e47167b042acf33f6b86f704a02699cf560cd0ba6f083f1cd8d392bfd4b2
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
$ docker pull buildpack-deps@sha256:46e10286a8d02a7bd307e18e9343429807b6d48872d1a2bd35bca84544818e0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124307642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0d44dfbc415fff5c1e9020aedceaa08af267a931f0b750375a1b199d44954f3`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1771804800'
# Tue, 24 Feb 2026 19:19:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:03:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:fd834ead99fe4ea0884686321217c38494a7a0c7327e2a5ed98d978011de7ddb`  
		Last Modified: Tue, 24 Feb 2026 18:43:07 GMT  
		Size: 53.8 MB (53756434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cfe71fa68737bfefafea69e4a0c5b69941285043380076279a4d65e82b5973e`  
		Last Modified: Tue, 24 Feb 2026 19:19:14 GMT  
		Size: 15.8 MB (15790747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cafa00cf3a9efb63d5aec84c5357f82990b3f70ca32d8a41f639c98f03b27f20`  
		Last Modified: Tue, 24 Feb 2026 20:04:11 GMT  
		Size: 54.8 MB (54760461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c4af5732edbc8a44c0e3a9a1b4461c3dade87082295e72210a49977f3b80d391
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7930317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f7deaec15b1260d8dc27071d87a9d0601df9a512cdf6c9981fedfb53e8ee91b`

```dockerfile
```

-	Layers:
	-	`sha256:f1dc0b1b944b228b0f637d149c0d52b291f23584b7e9a6475a78eecf644e9a79`  
		Last Modified: Tue, 24 Feb 2026 20:04:09 GMT  
		Size: 7.9 MB (7923001 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:780c9dc4ca5c84c0ec298a1282e366cc205dd39703c1b765c9f715c4bdec9db0`  
		Last Modified: Tue, 24 Feb 2026 20:04:09 GMT  
		Size: 7.3 KB (7316 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:fc304c58c9ffae2b957fba72da5e2d6b852112a5d04c5de705a88a5792d0d514
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.6 MB (114593654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:152da06e9aab8424d479ea62f8212ea2e698e47980aaf918ed5874cafbd99f2d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1771804800'
# Tue, 24 Feb 2026 20:02:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 21:34:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:dada255a3ad6614e8b2a389545f0625a8ca4a68f069cd24789cbdcf7a89bee05`  
		Last Modified: Tue, 24 Feb 2026 18:42:25 GMT  
		Size: 49.0 MB (49047560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd6350b59ed962425f695241e787bf8023af23ee4d06b078f82307ec998a697a`  
		Last Modified: Tue, 24 Feb 2026 20:02:14 GMT  
		Size: 14.9 MB (14905114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b78c92b47a812d57f4809800124de840b8b33ed15c020f80d518d0739cea99e`  
		Last Modified: Tue, 24 Feb 2026 21:34:53 GMT  
		Size: 50.6 MB (50640980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6d54ea77dd9a3d3ac4eb16039d7af1b06162b67a2e03eca65ed1ce19ff9fa019
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7931782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07d11726263d63a2aed74ab71938fb07ce3cb26003665a3ae54fdeee80c4e50e`

```dockerfile
```

-	Layers:
	-	`sha256:f02e78f3362da19635b983aed3c6e9fa55d91dd83b525a89257361498cf8d21c`  
		Last Modified: Tue, 24 Feb 2026 21:34:52 GMT  
		Size: 7.9 MB (7924403 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df31cdfdbf3507ebfec127bf28f22a568c1d3068dbb588c6a974a52c5dac115a`  
		Last Modified: Tue, 24 Feb 2026 21:34:52 GMT  
		Size: 7.4 KB (7379 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:d333e2a74e9d726c2014f433a416d7cda047e7a747c8c3360fbbe09fe65b487e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.9 MB (122908229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0465e5f0ac5ef777f278e9838c12590bff555a6110d369b32542d7d4fa6bbc8c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1771804800'
# Tue, 24 Feb 2026 19:24:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:14:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:0509053f2cf8072309184287dd2fd397e589dc5db17a1ddc469001be80ea07a3`  
		Last Modified: Tue, 24 Feb 2026 18:42:38 GMT  
		Size: 52.3 MB (52258392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e6dd0e9da832194c696500da7078d1cd12126c89f2a0283b7c424f7ffb55413`  
		Last Modified: Tue, 24 Feb 2026 19:24:15 GMT  
		Size: 15.8 MB (15774813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56f5bc11f4eeb73c577f8942878489898f3a73ef826300ec26a1880e09111671`  
		Last Modified: Tue, 24 Feb 2026 20:14:51 GMT  
		Size: 54.9 MB (54875024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b8eb2a8262d83aee511636f22dd3a4d18511a1b05996afa2f6be7ca71d4dd2d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7936131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9854703636e566e70f81af85c96eafaa59e4306e49025950300822f4b16ecf7`

```dockerfile
```

-	Layers:
	-	`sha256:dec45c6b380fe42b146eef4d9b31afb7025b3c758178daa02232d34cd6dd5c42`  
		Last Modified: Tue, 24 Feb 2026 20:14:50 GMT  
		Size: 7.9 MB (7928735 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4842a873f419714f533030a776e95ef399884a31ff300465b587b4727f06c3f`  
		Last Modified: Tue, 24 Feb 2026 20:14:50 GMT  
		Size: 7.4 KB (7396 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:358c7928a2f239f74bfeb9ee78eb5e0aaf3479113143d954e7f29d4013229fc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.1 MB (127054841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:672a15f2d1f20a860b2a25f82e7e441eb9a239825f429f81acf7f3116b0bc0d2`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1771804800'
# Tue, 24 Feb 2026 19:24:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:56:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:be7de57c5a292b6137b558f622789891088c38f02c67ce301a1559809fbe8ae2`  
		Last Modified: Tue, 24 Feb 2026 18:42:22 GMT  
		Size: 54.7 MB (54699784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d0ba919300e8846f159f61d3dad9bc45f102d2250de1dac9da8674f83e4e628`  
		Last Modified: Tue, 24 Feb 2026 19:24:44 GMT  
		Size: 16.3 MB (16295541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42c2152f88d25aaccd0c582b343220b4ec754827f272c5f5df677301ccd082aa`  
		Last Modified: Tue, 24 Feb 2026 19:57:01 GMT  
		Size: 56.1 MB (56059516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ae45dab5457fb439dd1698651e12ec2d16e81cd9787d29a326b718e681ec9c77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7925864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cec617fdf9f6c5fcf055704d5f510cb25f36cfe42b17c3d7e8c045f05f62393`

```dockerfile
```

-	Layers:
	-	`sha256:667c92486c4ccd0bbc4c047e608603b90dea34ce83b878c7bf708d708fe284f6`  
		Last Modified: Tue, 24 Feb 2026 19:57:00 GMT  
		Size: 7.9 MB (7918571 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed2768aabae5ea66dffe64b6b00d4005d37a8b58bd36e57aeb190a0e24efa6e1`  
		Last Modified: Tue, 24 Feb 2026 19:57:00 GMT  
		Size: 7.3 KB (7293 bytes)  
		MIME: application/vnd.in-toto+json
