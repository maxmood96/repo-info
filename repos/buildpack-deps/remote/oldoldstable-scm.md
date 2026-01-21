## `buildpack-deps:oldoldstable-scm`

```console
$ docker pull buildpack-deps@sha256:0e4a04d2d4900df121644684d7aa62372b80c0d5ab61c12994d65e2eb57dc8da
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
$ docker pull buildpack-deps@sha256:15b3ed46d832d50bb92c59548f15e15042bcc7dc082e1627829e1e893fbfe87a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124276595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5c9272403626fb0f9ab88a76e8418ecab2681ed3e860ea7996f11968abe4698`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1768176000'
# Tue, 13 Jan 2026 02:09:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 03:53:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:fccfc62cb15165379a658b98df1680b95e3908f69adc8e7176a095a7b4cf2106`  
		Last Modified: Tue, 13 Jan 2026 00:41:25 GMT  
		Size: 53.8 MB (53756446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24af405f2300f6988a2a2eaae4ec7393c0f9119fea3a400a1864fa5905a9bb66`  
		Last Modified: Tue, 13 Jan 2026 02:09:22 GMT  
		Size: 15.8 MB (15764316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e91529b594c86b803d1ccddf4f9d27516e8577c5b27e466be4f89f3a15da8944`  
		Last Modified: Tue, 13 Jan 2026 03:53:27 GMT  
		Size: 54.8 MB (54755833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldoldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c11c2888fd697f4c5f502b7141bca18c4307d581c04158c7f94b746b1e61eb1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7919475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac8b4f059a38d21744eadcf77c87766ececd6fc606ad6421b84666024fc62505`

```dockerfile
```

-	Layers:
	-	`sha256:f20e23abc33f75f0275b6b7f443129bf9db177f60aae35cbc8cd7bd4ffa39bd6`  
		Last Modified: Tue, 13 Jan 2026 07:43:43 GMT  
		Size: 7.9 MB (7912160 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a44031bd15a82ab9e2b5fad9d2cbaaa3abbb6432c0bc53dc0541a9d17ce0c307`  
		Last Modified: Tue, 13 Jan 2026 03:53:25 GMT  
		Size: 7.3 KB (7315 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldoldstable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:87793da8ee908c38b0913941d3c269833eae899940cdd7089c8001cbcbfea4b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.6 MB (114556682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d29fbdea33d157bb709828e150d60ce504a380e25e1faccd274e13fe54474cb0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1768176000'
# Tue, 13 Jan 2026 02:57:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:24:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:5d86a038b54ede2ada385178a3a13e9fc7833f9952c07b251c404c3aa117dcd4`  
		Last Modified: Tue, 13 Jan 2026 00:41:09 GMT  
		Size: 49.0 MB (49046458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd38532089c34c92931050565b084061d36d5f2907633b524122c2d6f089b42a`  
		Last Modified: Tue, 13 Jan 2026 02:57:41 GMT  
		Size: 14.9 MB (14879656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e704ca674385fc92cb2832f27a6cfada2b1b4e440bed4c77bded017641bb11e1`  
		Last Modified: Tue, 13 Jan 2026 04:25:02 GMT  
		Size: 50.6 MB (50630568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldoldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ff211456fba12d0ff4757864bd26168fa6ef5327c4e11c22d0e6bd2c865f7659
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7920942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd55d1a8c510aaea6b2b1885e266a3c6d6bbe0dacd1aff156f625df456692f9e`

```dockerfile
```

-	Layers:
	-	`sha256:ba921e5bc3fb5d6d95c640db3844dc2de451131e6a6580241e33bb568947c6b5`  
		Last Modified: Tue, 13 Jan 2026 05:22:36 GMT  
		Size: 7.9 MB (7913562 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:742ede317503edb057f1eb2db9eb03ca0099af02f3f89e3b10830c9f73234459`  
		Last Modified: Tue, 13 Jan 2026 05:22:37 GMT  
		Size: 7.4 KB (7380 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldoldstable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:9d29960c807c5367b1d23439099347ed9708dd65f228add5672f61205a083f3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.9 MB (122870944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d3cff96c2b3a9f201e8bd4f95126989cc5e730cfb281de984b16047e5a11113`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1768176000'
# Tue, 13 Jan 2026 02:13:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 03:56:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:0c9029c19a9aa67ff2b1313f591bcb473f0522775cc5a54491b5f7754253c547`  
		Last Modified: Tue, 13 Jan 2026 00:41:52 GMT  
		Size: 52.3 MB (52257769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee6280b099c5251ca1a2b55e8af5af4da252bad1f89325ba7a8344f2dea14e67`  
		Last Modified: Tue, 13 Jan 2026 02:13:33 GMT  
		Size: 15.7 MB (15749667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:735b68aa807ef231d58e7459ca83cac377da9d7f71d24a498190598a342d5bac`  
		Last Modified: Tue, 13 Jan 2026 03:57:02 GMT  
		Size: 54.9 MB (54863508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldoldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f99ee06af9cb5218e94995b8007b3bc70019cffe7e93f06590128c1956d5cb7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7925290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82190d0255124e808b759b6bf3818054a7ba77339fea848d71fb4c6304c4e2fa`

```dockerfile
```

-	Layers:
	-	`sha256:04d891f3d54031dc013d20d7a5bdb3f856299e0122af2e67d85ba4c8479f79dc`  
		Last Modified: Tue, 13 Jan 2026 08:20:33 GMT  
		Size: 7.9 MB (7917894 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4efb96d16ee9b1a172e2cacd182979ea3041ae8e78f631c36a7df504c3487bed`  
		Last Modified: Tue, 13 Jan 2026 08:20:33 GMT  
		Size: 7.4 KB (7396 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldoldstable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:0e04a269d1cf6637725e5582260dc05b310aa284c56387dbebda68421168082a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.0 MB (127016325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6815b3aa6aefdecafba8f575089d8a83dfdd146184e942df2a22a45e16148c99`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1768176000'
# Tue, 13 Jan 2026 02:02:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 03:03:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7e115d265636fc6da528c1f4977e22baefb0bae7061ada6dba677a290e83b246`  
		Last Modified: Tue, 13 Jan 2026 00:41:26 GMT  
		Size: 54.7 MB (54699638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6ed43d5d71f701abde2a62df95258edf0ac9ef3046d49ca25c0f30e57af2985`  
		Last Modified: Tue, 13 Jan 2026 02:02:38 GMT  
		Size: 16.3 MB (16267780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50309e354294a6f81ebf1bf80c4203a79bc9374449993f7fb52ebf0640408262`  
		Last Modified: Tue, 13 Jan 2026 03:03:46 GMT  
		Size: 56.0 MB (56048907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldoldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f8303881651568734528b2aafcc346741530e1ef6b30aab5e6d4f31b4386a200
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7915024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc4ce379914825c166bf748763fe890f79b09b2e6607a7fb877de27989e3617a`

```dockerfile
```

-	Layers:
	-	`sha256:556d9759865dd27bdc48a52582a15d487b8232b3887e437c862374fd4b1f2a60`  
		Last Modified: Tue, 13 Jan 2026 05:22:52 GMT  
		Size: 7.9 MB (7907730 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d6a87fb67cb5fb02545d66a5a65fc3906d2174c13247c97c0df0c375a241b26`  
		Last Modified: Tue, 13 Jan 2026 03:03:35 GMT  
		Size: 7.3 KB (7294 bytes)  
		MIME: application/vnd.in-toto+json
