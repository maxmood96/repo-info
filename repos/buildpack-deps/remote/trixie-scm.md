## `buildpack-deps:trixie-scm`

```console
$ docker pull buildpack-deps@sha256:aff8fb7c707292e464e199c3ff5839ec24cccc9b24e8d6f87125a399f8f7527f
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

### `buildpack-deps:trixie-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:7e93862223747cc5394f6eb431714def5e3f387d0ab679dcc30b9d4651943e23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.7 MB (142684385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fed493eede9d76a665504661cce3aafa0cd68c9c24a703adc1ad063d90396eb`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:cae3b572364a7d48f8485d67baee38e4e44e299b8c8c4d020ff7fb5fdd97f88c`  
		Last Modified: Mon, 29 Sep 2025 23:35:29 GMT  
		Size: 49.3 MB (49284626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd090f42c4b7844c5846f9b4c719994f496fac3befe1d30f0ff20794e742370a`  
		Last Modified: Tue, 30 Sep 2025 03:17:21 GMT  
		Size: 25.6 MB (25614810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0c9d6d993ac93f222ba87ca01097d40f632be9b48f6b5e399f2c5da1b3133d1`  
		Last Modified: Tue, 30 Sep 2025 03:18:12 GMT  
		Size: 67.8 MB (67784949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:dbf6823a4c93adc4b9b9e3856fef7fb964927ed82520fd5adaee3839de9f50a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7774616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3789f0b88a481a2e6c4ffee3328cd7f2e08c9289d82b03fdc1884110efd91353`

```dockerfile
```

-	Layers:
	-	`sha256:4341ee45c035c43a7a31e33bd90135e73670cafcd854cbc66a47fd3233d630dd`  
		Last Modified: Tue, 30 Sep 2025 20:48:18 GMT  
		Size: 7.8 MB (7766996 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b3fd5106d8b45aebef1e93f2fff9715d089ed2392665e1e8758b2b89c1aa0dc`  
		Last Modified: Tue, 30 Sep 2025 20:48:19 GMT  
		Size: 7.6 KB (7620 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:cbd2cb852c8704ddbc27bb17f6968c53082662372c6e0062189f5b125cc47945
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.1 MB (137116319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2547a50d76a19c51ffec12c90e749e9d0ca53c11e6aeb26853838e2b6876061`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1760918400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:36e1dd9ce5730c29e323bfee77881b6b709a9ef3833ed3a509dabd626e23ef19`  
		Last Modified: Tue, 21 Oct 2025 00:20:35 GMT  
		Size: 47.4 MB (47448771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc5aab8f083c99dfceb8649e1078e500b3226031e7fdab550eda596ce5b675db`  
		Last Modified: Tue, 21 Oct 2025 02:32:50 GMT  
		Size: 24.3 MB (24342547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93a322d2ac28a78c43ffaa81483b3e7182f4b364130ce74f60ef2317ccf71493`  
		Last Modified: Tue, 21 Oct 2025 03:57:05 GMT  
		Size: 65.3 MB (65325001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8c0d1701c51b62b7a69fb0ebcda37ca07bc2c53ace10badd5340a828b7632c6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7775780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0510ea83903a48f17de5e8f16e52f6b86706c77ea524b17ea70523755ed0cafd`

```dockerfile
```

-	Layers:
	-	`sha256:7222734efeba70bedc9938afa979584a5274cd74f4e80d78ee1cdacff8ebd544`  
		Last Modified: Tue, 21 Oct 2025 07:21:20 GMT  
		Size: 7.8 MB (7768088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:789438771b0cf9b890e11c19d61dddb83a3f4144f6fc0bcd600e39fbb9f1e6bd`  
		Last Modified: Tue, 21 Oct 2025 07:21:21 GMT  
		Size: 7.7 KB (7692 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:97ecafad04321113f2b7183396781824227d1b43994376917f6e08e480659c6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.0 MB (132046560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1a248340967c41d1a10d1b7dd5360541bffddab468081dbb97682ac05804053`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1760918400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:25723cf5ae8b10c461d8c699bc5f9e41058f8fd5113212d106848ebe89fc0ffc`  
		Last Modified: Tue, 21 Oct 2025 00:20:56 GMT  
		Size: 45.7 MB (45716494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:452a743b80bee0c18e49576c93efcfb6c736c07dbdda0e38658362cec14c6415`  
		Last Modified: Tue, 21 Oct 2025 02:45:21 GMT  
		Size: 23.6 MB (23616662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcfad6891ec6a8c0bc6bb36a13c5e7bc91999a0a3e69d53912de98fc37f3aa42`  
		Last Modified: Tue, 21 Oct 2025 04:11:23 GMT  
		Size: 62.7 MB (62713404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:efd7765e6822bb15378525628aa0b608eb21474f15252ee0d5f6811f0d9e6ca9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7775249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7fef0df682348cdfc0704cd24d12cda2c649acfcdf99db7ebec39870fbab81f`

```dockerfile
```

-	Layers:
	-	`sha256:257dbe6343766f84aa165040443c6d40d20ae809eef6bf73c3cf29d9d3de1f56`  
		Last Modified: Tue, 21 Oct 2025 07:21:27 GMT  
		Size: 7.8 MB (7767557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b2bd78e910f0ac470b6b1eac86c373f9250b52d8f35142e4a65ea709ea0dfde`  
		Last Modified: Tue, 21 Oct 2025 07:21:28 GMT  
		Size: 7.7 KB (7692 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:0190f69593fd4f12c3355e4a54c2e2add6bc7dfa57f0bac1bb142542b0970a33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.2 MB (142248042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49102b8007fbd8f0ea5953bc6649ab02c081a42aed19138e1af8b9fdf464dcd5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1759104000'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:28aec8b14b3eeacbf47ef38af72fab694b109fdcdf31581722750599baf1a932`  
		Last Modified: Mon, 29 Sep 2025 23:35:17 GMT  
		Size: 49.6 MB (49648695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:003e6ed58c0c6ddbc757cdcbd876d66b9b5eed39128088a0055c819ebe15d20d`  
		Last Modified: Tue, 30 Sep 2025 00:14:22 GMT  
		Size: 25.0 MB (25016370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:390c9631087ef516f060328537d417f223e1f264c968e39186895696e78090b7`  
		Last Modified: Tue, 30 Sep 2025 01:20:15 GMT  
		Size: 67.6 MB (67582977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:fd1e24cfa7af43aea04b01afcf8d3079ea46a16d66b640257f4f15967dd036a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7782383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:239de39a67ede0e016545d90fcab5af340671e442d33a9496f74af4dad721a08`

```dockerfile
```

-	Layers:
	-	`sha256:8098fb79c28dee28decbb7012dfe31d45d83bcade4dff4e5cd5b1f52016a716a`  
		Last Modified: Tue, 30 Sep 2025 11:48:09 GMT  
		Size: 7.8 MB (7774671 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:477514c19a8ba7b433c8952a625aba0c53fb98a673a0dc6f9a9b0236c466b2bd`  
		Last Modified: Tue, 30 Sep 2025 11:48:10 GMT  
		Size: 7.7 KB (7712 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:f22199875003e99268f914d659e35ba87a9a901da57a80f5168278f6937a2e8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.4 MB (147369373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad10eb619004c7af6df9553127320768a2a4c0bd9712e0e28c3dd69f9f8a67f2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1759104000'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f1c1f592b5569b5e2093c3107a48f2929b609f05af6d24c06d41a7ec1ae5e0e1`  
		Last Modified: Mon, 29 Sep 2025 23:35:36 GMT  
		Size: 50.8 MB (50800229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11e5d861644e3a43dbea9917a86fd0d6ccf184bc7514ee58118ffa521ac4bc61`  
		Last Modified: Tue, 30 Sep 2025 00:21:14 GMT  
		Size: 26.8 MB (26774670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acddf1ffebf58f05179a0e8a785ab62df40c7d1c75ee543282d404ca07d3ffec`  
		Last Modified: Tue, 30 Sep 2025 01:21:21 GMT  
		Size: 69.8 MB (69794474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e12a6306ef9b9d6e4f7b18923ee6148171e26586696e36388745b084f6df833b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7770724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca1a19ff1998b29ecc65f7f5b296dfb324f2b87478f360ffda24ebe5ff08a886`

```dockerfile
```

-	Layers:
	-	`sha256:94bc44f01cfdc0521448addbd13db72f015b0482ccff267919a84b8f1eead5a3`  
		Last Modified: Tue, 30 Sep 2025 15:25:35 GMT  
		Size: 7.8 MB (7763131 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84f068faf754ff36d1d3a7b9bc3c719a1046eeaf5434234b227d9f9b4042480a`  
		Last Modified: Tue, 30 Sep 2025 15:25:36 GMT  
		Size: 7.6 KB (7593 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:e1382ac2a9b49604394dd8b92ec149788808cd24f036b54f0ded295603031f99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.1 MB (153139349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdc793e6913e11d117be588fc6be78c2da85400928f4d7aed682a003d373f3d6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1759104000'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:71fbf24a239310917388930bb043e64907cb532b9ac8f265e44e032dc3bf4409`  
		Last Modified: Mon, 29 Sep 2025 23:41:05 GMT  
		Size: 53.1 MB (53109217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c97a0b9869d194af98b70e095598cab3ab85032828ead695d63f75204d7418fc`  
		Last Modified: Tue, 30 Sep 2025 09:24:30 GMT  
		Size: 27.0 MB (26995278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ed492992022fa9e4a253b427574c9ab21d82072f73e353ad6f09e1555a92cc4`  
		Last Modified: Wed, 01 Oct 2025 11:14:56 GMT  
		Size: 73.0 MB (73034854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:3a179807329b5e9c71bd791fa8cc5f13c32f988eb5a85db5fdb6da8f1506600c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7781776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:531950c2b540b6945808f21690d002304f7e8f11257e8d8d69cfaecca3084761`

```dockerfile
```

-	Layers:
	-	`sha256:98a4b1ddd04456eacb000e9a748fe8b29d370b59df873902f73ee90b859c7eb2`  
		Last Modified: Wed, 01 Oct 2025 20:24:20 GMT  
		Size: 7.8 MB (7774119 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd1336514fd7b720f846b3256e06eae5a480d4b3e4c89accfbd0dd379f49ed8a`  
		Last Modified: Wed, 01 Oct 2025 20:24:21 GMT  
		Size: 7.7 KB (7657 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:9a15dd54f2c50d819f7fc35eebe8f958caa134d46d98a15ffc346b7b0cf96431
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.4 MB (139382769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef33677fed2972028c281b22c29a2b92d78ac3a073cfdf00e48926690ed10c25`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1759104000'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:913254a25f5e448a50a1e74fa50f037e22f85cfe4d6a3c626f4b7405299b7c1b`  
		Last Modified: Tue, 30 Sep 2025 01:03:38 GMT  
		Size: 47.8 MB (47770009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8533144b875d90b1f9c5a4ecb4c26177d9b646c254cea7d68fd43c77c27f975`  
		Last Modified: Wed, 01 Oct 2025 10:56:05 GMT  
		Size: 25.0 MB (24952783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c645409e32b37950d400f06f75fff87e9a716322f248e5d01d290689226a51f`  
		Last Modified: Sat, 04 Oct 2025 03:44:05 GMT  
		Size: 66.7 MB (66659977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a033f3d9b18e7ce62351cadfd1b9397a8feded1ddc989d9077ebb15de0ac9988
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7764490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f926899775695ba13df134263c3b9d4786967b3f3c483ce3896975f32d8dae75`

```dockerfile
```

-	Layers:
	-	`sha256:bc3acfa405360a1c031a5cc2bff8df85021e0369abf7d7498a4575547404c3f8`  
		Last Modified: Sat, 04 Oct 2025 04:20:33 GMT  
		Size: 7.8 MB (7756832 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e864e2e85d52b577a0398aef460fa648c7b63a43f9b3dbba294e8d42f779e898`  
		Last Modified: Sat, 04 Oct 2025 04:20:34 GMT  
		Size: 7.7 KB (7658 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:b7dc0601a89c21b18a19e1a35fcf1e2dd805ddd542156da1e2cb23fbb0b10dd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.8 MB (144771525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc6d64edeed402e086840eec7ca22c8ad8cc37baa7741a5d22a7cf4d5bc9d963`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1759104000'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:024d6c344f0b9dbb2baf07e95dfd2abbfadc5c8262ca381f39f6489670cbaff5`  
		Last Modified: Mon, 29 Sep 2025 23:41:06 GMT  
		Size: 49.4 MB (49351442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae40148dca91a7d747a8331f403c812cb96e16b0e939c3f7e22eaed6bd4173a3`  
		Last Modified: Tue, 30 Sep 2025 09:36:14 GMT  
		Size: 26.8 MB (26782227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2360823d72f62f7ab99d1125b961476d915cd531da8e87d42d3767dfd3b86d6`  
		Last Modified: Tue, 30 Sep 2025 15:54:22 GMT  
		Size: 68.6 MB (68637856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f3b13075ea2a68a339d2a386b32be873c145e9b01faf4d96238fb9f64b7801e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7775529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec6a8bb20cbabf0377a1fbc35e8f8b0383926d5011f4e32435455dc1194379d3`

```dockerfile
```

-	Layers:
	-	`sha256:2b519a97c7099e62f8576aea41ef66f75657935a84b53b1a51af71eeeca550c0`  
		Last Modified: Wed, 01 Oct 2025 01:30:47 GMT  
		Size: 7.8 MB (7767909 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aed1a79c058bef0e348d5709ac3680e416152d5fa7c3709266050915f46c6611`  
		Last Modified: Wed, 01 Oct 2025 01:30:47 GMT  
		Size: 7.6 KB (7620 bytes)  
		MIME: application/vnd.in-toto+json
