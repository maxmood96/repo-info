## `buildpack-deps:oldstable-scm`

```console
$ docker pull buildpack-deps@sha256:f8b44d871c904becd02992c1785520907b4166b7974db9aead2789ecbc5d00e0
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

### `buildpack-deps:oldstable-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:4814e93af668ad776156987b0a30c8b308b118e01fbbd17f741b791b8851bad8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.0 MB (124049061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e581d121fb96975fea39e8d8b79c9c4de4cb6ac154abf3542985c05e89625228`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1738540800'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:478cb73646107d7b3f891aa53abaed926667463844c07b1d924bd760ae03f38a`  
		Last Modified: Tue, 04 Feb 2025 01:36:37 GMT  
		Size: 53.7 MB (53738873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0388f0d5bf1adc15e551cceee5a85f21b1ebf5b13c380ee0e941c5d55013598`  
		Last Modified: Tue, 04 Feb 2025 04:37:42 GMT  
		Size: 15.6 MB (15558271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d473f760e53d3d50afd1cebc7113387023a04ff8ec34073c4412b465ccc2fc5`  
		Last Modified: Tue, 04 Feb 2025 05:19:08 GMT  
		Size: 54.8 MB (54751917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ef9e6950a308d27ad0fed70063500c67d5f94b60458bf35e69a461c78d601501
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7715539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2c9ec6144be5fdec793e06b9bfe76a1ab2b4f60224d307ec385d56b9d387f4a`

```dockerfile
```

-	Layers:
	-	`sha256:52a22ae317e2876eea325b36b2cc60b6f80c3cb88a7dbdba1853d7465f8d0e0b`  
		Last Modified: Tue, 04 Feb 2025 05:19:07 GMT  
		Size: 7.7 MB (7708186 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d5117857f7ca0d3e1bf3a461cdcb72b1ca27dbcbcf55684d0fb889d6ed4006b`  
		Last Modified: Tue, 04 Feb 2025 05:19:07 GMT  
		Size: 7.4 KB (7353 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:d774943785660ecc2de823027779a925c87651bd40f06fbc6b58b9de1c8bd809
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.3 MB (114339540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d5ee24dd46e5c5e26ee74d9f511fcc3735ef780de9003547e3a914b976008fd`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1736726400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:2d8b4e71b0057b288fa0b7cf9b1d15edc9bec9dc37df63d3463ce28e4f414dc9`  
		Last Modified: Tue, 14 Jan 2025 01:35:36 GMT  
		Size: 49.0 MB (49025062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7055bc7f040fce3e9b8f05fd7f56b8a568950e082ea8ea3aa96cf99f49523ca5`  
		Last Modified: Tue, 14 Jan 2025 08:58:39 GMT  
		Size: 14.7 MB (14673832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:681398f28ce19a7af317e3774529df465ed1770ca10164fdba3b20f23a5d8026`  
		Last Modified: Tue, 14 Jan 2025 16:16:27 GMT  
		Size: 50.6 MB (50640646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1c91b0f90f1ef91ce5f6c48aadb2477540546f65adf63b3d90982ec86f15a6be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7716983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d58caa9f61dfed2e570b426db1959ba75ae97217fa6a9a80716c68ee7e4355f`

```dockerfile
```

-	Layers:
	-	`sha256:d98b7e41b3cd63c512f218dfab9c9d65b81f3eea63c8b836f660301b020c5d66`  
		Last Modified: Tue, 14 Jan 2025 16:16:26 GMT  
		Size: 7.7 MB (7709570 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3bdd7383a4b1f4d3f50aaff18c4c7bc58547a6b215c9b01676e6337e8dfb72a`  
		Last Modified: Tue, 14 Jan 2025 16:16:25 GMT  
		Size: 7.4 KB (7413 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:7cd12446ba7224b5c2917b1c38ea6cc66ca5d1b816e2220b6746099844d83a02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.6 MB (122642755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c009330911b291df3f419696b4f356ad17a61817d491820586e38c2b0009d1bf`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:1270858b2b9cb5d47abd119b946534b70ff7d09f29c425fc07b280e5c28971c6`  
		Last Modified: Tue, 14 Jan 2025 01:36:12 GMT  
		Size: 52.2 MB (52246060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03dfd6b176342cb480b79cef9a7188364b0f5702ccc77422fcdb5d7d8f3f42c8`  
		Last Modified: Tue, 14 Jan 2025 07:00:18 GMT  
		Size: 15.5 MB (15544093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d23ac0e9b25076f1cc90469f31bffaae783c6a3a88272620af5e7dcbe0b8202`  
		Last Modified: Tue, 14 Jan 2025 13:31:46 GMT  
		Size: 54.9 MB (54852602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c15cf8ae3f7c2b7a8e902962590e6c9064ebc3de259521e75513e13f2e9583c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7721335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ea1bc11e1597522ba927e7cf032ac12c2f5c0b48f76688a2c41cc8df5ff6d4c`

```dockerfile
```

-	Layers:
	-	`sha256:cb5b7433e723b0023aeae558a9a132cd43f7fd43bf007e6f3bfc19ad25dd8b7c`  
		Last Modified: Tue, 14 Jan 2025 13:31:45 GMT  
		Size: 7.7 MB (7713902 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1092df41e57f424822625c9e363e68af5c5429b0bfca3a72c6d7952e77fbb0a`  
		Last Modified: Tue, 14 Jan 2025 13:31:44 GMT  
		Size: 7.4 KB (7433 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:9a62f978f5fdc58bc19fc0153c3642c7986206935c5123229b9400de09265b18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.8 MB (126767886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebb73a16d07dcda55523ead47dacd4d9749d94ac0ad37187950d43b0fdbab437`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1738540800'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c2b5327eac1fcd49233dc8f6e5417e7e2efeea16edfcbff9dd025f389e15b11e`  
		Last Modified: Tue, 04 Feb 2025 01:36:38 GMT  
		Size: 54.7 MB (54675956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40d372eab1872f98afed1da2c899af883a0b3a6e52e25e2690ed35b3d6f859e5`  
		Last Modified: Tue, 04 Feb 2025 04:23:38 GMT  
		Size: 16.1 MB (16062054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4520e7fd9b17628990db3e961c2d7570421849af1fe255937c0a9e48cf49a48f`  
		Last Modified: Tue, 04 Feb 2025 05:15:33 GMT  
		Size: 56.0 MB (56029876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:4c21667e744397eb3935c16797e52b0148b9d2656c9c5df160d776ef48f8019e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7711006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50bd9c61c42af2df265f3d3c98356591cf58dbc8635d76bca719e8339597bd94`

```dockerfile
```

-	Layers:
	-	`sha256:fcedc0c587cb91d36a7804b4632555da7225541fa346b9a49d88f2ea9ef0ba0d`  
		Last Modified: Tue, 04 Feb 2025 05:15:32 GMT  
		Size: 7.7 MB (7703676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23633969f8f239808620f33b97db5f047216cba12a362fa470b4395f1a8ed0b5`  
		Last Modified: Tue, 04 Feb 2025 05:15:32 GMT  
		Size: 7.3 KB (7330 bytes)  
		MIME: application/vnd.in-toto+json
