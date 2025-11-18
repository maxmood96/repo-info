## `buildpack-deps:unstable-curl`

```console
$ docker pull buildpack-deps@sha256:351df823ee04ff2d88be1a08a46ce814667c089dea05414703720c23a0b6b517
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
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

### `buildpack-deps:unstable-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:d7f677429ab7f29c7172201666e40593ef893c484b720846db041cd6fc471e36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.7 MB (75718626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c33355c77869dc8ca7a56cb08875dca141946d6573fa6838ad0e7bfb0a01f3e7`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1763337600'
# Tue, 18 Nov 2025 05:10:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:63fb544511bd02db3b85f4aa7407dbf6c6f5cd7cb1c0c1e65d055477ac245bcf`  
		Last Modified: Tue, 18 Nov 2025 02:31:43 GMT  
		Size: 48.5 MB (48500427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f587827fecd245749e6cb3adce116c1cb03e4aa424acd20250747a6b892e702f`  
		Last Modified: Tue, 18 Nov 2025 05:10:46 GMT  
		Size: 27.2 MB (27218199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:89f069c9246b36ab06e22524697c1a5d866df537a721f30ee890f74ef4e08b4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4105054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:057b329129032f8efbda70ba460bb481e855f84d3cff1eeece99fec2542449e9`

```dockerfile
```

-	Layers:
	-	`sha256:fdd5ecc9c275ce169abcab2d2ae9f40bbc5042a5e28e6e5bc0ab2064347ee732`  
		Last Modified: Tue, 18 Nov 2025 08:22:40 GMT  
		Size: 4.1 MB (4098293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0d7092f6c8ac1a7faf30e35511eea9fb26489fd3683653c8c0db6cbbc2748c0`  
		Last Modified: Tue, 18 Nov 2025 08:22:41 GMT  
		Size: 6.8 KB (6761 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:fa63ca466b8dc135a9e00180a9b917c0db2d617b134b370d95d1316d8bcdc487
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69949980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e46680c2c2fee7a0bd30dd92505600eb3a89092ffbc2afc2a11a0ef0ea7977a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'sid' '@1763337600'
# Tue, 18 Nov 2025 03:59:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:249f143dbba2558bd4f87316a884ba0d2b99358af5b3c63e9ac2b9640e6f9846`  
		Last Modified: Tue, 18 Nov 2025 01:12:47 GMT  
		Size: 45.0 MB (45003691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cdd7e51b270e55f3a7a9a2d43268061869ee4c4d0b6076dffdec9ff8ef06009`  
		Last Modified: Tue, 18 Nov 2025 03:59:26 GMT  
		Size: 24.9 MB (24946289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5745bad4520248694b5171631376fd1ba3b5565c1d3f5b1a54fa01b5815ccae3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4106614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba611c2c01125bf32b80c565d56f429277b833365f7765f2e424f4144a0b8a74`

```dockerfile
```

-	Layers:
	-	`sha256:3d492ff32c3f31ca656a13d707f3ca57365ff7ff307e1b6f6a4028fec3082980`  
		Last Modified: Tue, 18 Nov 2025 05:23:58 GMT  
		Size: 4.1 MB (4099789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ddaf0780eb5cf9fa13c210d6d9820738b41edbd4bc1f51f8d7fa5f5619d47de`  
		Last Modified: Tue, 18 Nov 2025 05:23:59 GMT  
		Size: 6.8 KB (6825 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:957678db45795afd681c523fb0ea959949865738adf09239dded4e00edba3376
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.0 MB (75036723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a90c58568a3624d6bc8a7bf98e0c82d6d3aa7976e18fa1731908fedb2420e3a8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1763337600'
# Tue, 18 Nov 2025 03:26:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:2b90f6fb16dc868101354a233036d6d70e13cd3477e4df5ab59f2ccc8607c1d4`  
		Last Modified: Tue, 18 Nov 2025 01:13:53 GMT  
		Size: 48.6 MB (48591389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:088f615e7cb4b13e78f79053e3ff3386cb79b093cd2d91fe819f692264eb1475`  
		Last Modified: Tue, 18 Nov 2025 03:26:37 GMT  
		Size: 26.4 MB (26445334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5494ea924406f74e9205719dd96fb5e4cf783bb15ec6efb93978e2ce8675eb5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4106027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:378cd5079d0e6609b9acd684a611086787dac69c8538b0532328c14c613bedd9`

```dockerfile
```

-	Layers:
	-	`sha256:5dd5adb497adb25730288e11101af4f6326da4fda1441d84c7d1911ea90d53e4`  
		Last Modified: Tue, 18 Nov 2025 05:24:03 GMT  
		Size: 4.1 MB (4099186 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8c6c722772edf62994414c8465b9ba4f75a04c3ead8226797c284babe1f5a8f`  
		Last Modified: Tue, 18 Nov 2025 05:24:04 GMT  
		Size: 6.8 KB (6841 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:b6209b8bc13627f9097cfcdcc0e6871c065b9f07274a814a35f749094013b190
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.3 MB (78278187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e8405219107f6470c1cec560e5def2e70f57c80a0d759ff48fde0d8810c3c5b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1763337600'
# Tue, 18 Nov 2025 02:57:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:b1df74e42eaae76d71bf2c2aa402328d711dcdb63b4080ae4e7050388c00bad0`  
		Last Modified: Tue, 18 Nov 2025 01:12:57 GMT  
		Size: 49.8 MB (49833161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55f52a4943d5de6ba698c20cbf767503261cc0eb7a108778d7a744e58da50d69`  
		Last Modified: Tue, 18 Nov 2025 02:57:26 GMT  
		Size: 28.4 MB (28445026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:20c36ff69d4f40b8a3a111525b6969461d2b87acd86e6b00d457d1f5303d4111
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4102151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd2b7b863a6a7e88551768d335f99848df65b797b0d1a9f765b534ae42a54074`

```dockerfile
```

-	Layers:
	-	`sha256:5b142cf1cb14364f872c8dcdbc66154545c9e83bd408fa9f09b3cb05823eb72d`  
		Last Modified: Tue, 18 Nov 2025 05:24:09 GMT  
		Size: 4.1 MB (4095412 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f84d12f9c81d484e78c384f534b332657068c73f44de4b0456a5735743057bb`  
		Last Modified: Tue, 18 Nov 2025 05:24:10 GMT  
		Size: 6.7 KB (6739 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:6ae27a6c1c837f7be35b1e374a46c4e28bfa87ac3a167ee726242a2aed25268e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.2 MB (82174106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b691d45cb15eb4f91794f2c1c6ad4f7b9c9283d8beeb0a06157333966d173a2`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'sid' '@1763337600'
# Tue, 18 Nov 2025 04:06:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:233726152393942e1ef6b4533705d6bb3e4142964e6e486a7902cf456eab5151`  
		Last Modified: Tue, 18 Nov 2025 01:56:30 GMT  
		Size: 53.3 MB (53335631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8247117b12d78345474708e2bcd8a4be4ebcad8965145f6ab351c359ba9869b`  
		Last Modified: Tue, 18 Nov 2025 04:07:17 GMT  
		Size: 28.8 MB (28838475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:19468b49819639df2fea9e77ba3be4fef71a5dc0042a4159304076b9257df2fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4108918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b34126a77958eb78b9920b1d1f18d3286573a2f1d0ecc24a694ec4845474eaf1`

```dockerfile
```

-	Layers:
	-	`sha256:40c6c42304740f2a8efb8a170ea9d38cfcc48e13c9c9d1b444909b64f927d6f3`  
		Last Modified: Tue, 18 Nov 2025 05:24:14 GMT  
		Size: 4.1 MB (4102126 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:721a2cd23ab3fdc705fe69c0fb33114f74243b71f8933379f914a9e8492a5e9f`  
		Last Modified: Tue, 18 Nov 2025 05:24:14 GMT  
		Size: 6.8 KB (6792 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:0da5d11bf957517b19507da6d28d9ff9adb08c8fe7329921431705c4dbe8e378
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73185118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d83bb69c97d797033968f95dfb7215719dde6bafccb2c9ca75b3ccafb4326af`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1762202650'
# Wed, 05 Nov 2025 11:59:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:0d83aab6f1b53b0725edaae6679e08548e39316074675f21600df7f5620f7fb5`  
		Last Modified: Tue, 04 Nov 2025 00:17:08 GMT  
		Size: 46.8 MB (46794261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:228cbd09f8069207ccfebd2b0e21dcb66c15200b5b8eab72b328a2c4f3d36206`  
		Last Modified: Wed, 05 Nov 2025 12:01:22 GMT  
		Size: 26.4 MB (26390857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:939263e03a26d15b08d06296ef74e26c674daad9fb2752f66e951f0e9765a1b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4097585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19d5f167577e02af5243686965b21aec4f9be239f1177d1d4fa9aeabfd3deace`

```dockerfile
```

-	Layers:
	-	`sha256:7b6416c844ee65a023940dde472eecc04dabd71f08eca4e171b1116be0db5a66`  
		Last Modified: Wed, 05 Nov 2025 14:28:05 GMT  
		Size: 4.1 MB (4090792 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5712e5c36033868e35f4b1cf5d92ad03802f374fd4c458bb62ba7e170cf7b02`  
		Last Modified: Wed, 05 Nov 2025 14:28:02 GMT  
		Size: 6.8 KB (6793 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:b08440e4441e615539fd10009f393eeb9421bf95104321a677cac89f7a4e98e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.7 MB (76670619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1ee15f0077c18fbbc1b199f5907073008c56876d04dbd11f371d613ac72b5ae`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'sid' '@1762202650'
# Tue, 04 Nov 2025 10:02:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:ee07654f71bb163a06c3532a844efe8d75683f4dd53a88a8109fd9ed1b66fc1f`  
		Last Modified: Tue, 04 Nov 2025 00:16:26 GMT  
		Size: 48.3 MB (48346444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14e24f5b3ee730a867fae54f44e0b43c0311d9bd66c565a7c2a2b0d7a887c220`  
		Last Modified: Tue, 04 Nov 2025 10:03:07 GMT  
		Size: 28.3 MB (28324175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:54b2df1bba47b42f223252bdf9378fa66b58168bcd454042a0d11f97cae4528b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4106479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:329c35f28f85075776312e50f17e864d83b5c0de55ce6d4e7f18e229cb08388a`

```dockerfile
```

-	Layers:
	-	`sha256:fc010c6b002fca2acb3f824b6865524d3910f8d5aba92807d630a4f028cb8458`  
		Last Modified: Tue, 04 Nov 2025 14:30:40 GMT  
		Size: 4.1 MB (4099718 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba9c88e8aeb2aed7f6df8210c94356176d31d89d2f67dc1d5d0a7ffe616d9654`  
		Last Modified: Tue, 04 Nov 2025 14:30:39 GMT  
		Size: 6.8 KB (6761 bytes)  
		MIME: application/vnd.in-toto+json
