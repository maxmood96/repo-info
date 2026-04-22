## `buildpack-deps:bookworm-curl`

```console
$ docker pull buildpack-deps@sha256:3ec1f9e7d2e86e2f92cbf38bfc37431b9b9ccc7edf5c352b08d57404e7750e28
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

### `buildpack-deps:bookworm-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:019754b6772aa831b51b71eb9cc893dec19bb1ccdddba7968ab77c75cbb27d85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72530862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1ea9b9744ea9095e647f8785881c26403877d2b2f41571daa21364d730e1813`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 05:00:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:db53381ee51f9e43304e236099ba097ae1b33ae41a8007e0b6319992eb55fd00`  
		Last Modified: Wed, 22 Apr 2026 00:15:45 GMT  
		Size: 48.5 MB (48488628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5203b2bfeff92b72e816dc6cbb1f16856f0cd592e521e3c0cfa195a78fe180e`  
		Last Modified: Wed, 22 Apr 2026 05:01:15 GMT  
		Size: 24.0 MB (24042234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:aa7639c7ca20865bb3a70bd86db98f164cb1fcd471feef4eb365cd09c42419c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4521150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ffbd022d66e66ae51c3306de89248df4b03dba880ec218c14e5355926798db9`

```dockerfile
```

-	Layers:
	-	`sha256:a46cddaee8b107ca66c8d9dc25feb5b66d37fe81f277a77d98d535450d919bed`  
		Last Modified: Wed, 22 Apr 2026 05:01:06 GMT  
		Size: 4.5 MB (4514334 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58ef14e1babe048ed256b6b84eb7af5ab9069fc524afe0be24d1f1f882bd0b62`  
		Last Modified: Wed, 22 Apr 2026 05:01:05 GMT  
		Size: 6.8 KB (6816 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:bfb30825cd6f321ea1506388e2d9d974343ad4dac9f6e5fc290cd5a43d80187b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.7 MB (68735522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a2789e5895d93a7397da9c83cecab079256a15c0329ea35a9b56a841d4ba7f7`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 02:45:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c4564d3f444801f4c4ab3e01fd62e7dd3bd91054769ac22888b9bef61823a830`  
		Last Modified: Tue, 07 Apr 2026 00:10:20 GMT  
		Size: 46.0 MB (46021666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fccdf893742febb0a81a70ae87b43e8f63165210f89f5c68b785189d45a2427a`  
		Last Modified: Tue, 07 Apr 2026 02:45:21 GMT  
		Size: 22.7 MB (22713856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:aa35eb02005428c4a86f22e10592a31c9665a2c6271b47a76c82cbbd92be8994
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4525031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1748625dc80131d70ff6175bce0d4865c49ad28d01480d4d4e97521d25c42f4`

```dockerfile
```

-	Layers:
	-	`sha256:641be05edeead0a8d65283f30505d49d8bf78d2cb4681d369a8f9190c6d199c9`  
		Last Modified: Tue, 07 Apr 2026 02:45:20 GMT  
		Size: 4.5 MB (4518150 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a736332894c431cbdef8058a77543be067d15a2ce5d0d208258c8c7eb142923`  
		Last Modified: Tue, 07 Apr 2026 02:45:20 GMT  
		Size: 6.9 KB (6881 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:75b82df83fdc301f0382f24ec63b03385d697bc04965a482ef6d52dc4fa630de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66153995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0e4a065a25d2468c7d593558686d7af1bcc528e9bd65475bb1f3a728a742869`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 02:18:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a78e7b2123c5c35e65ee1cc17df0d11c1db8ab3c4fe80b457270c2d9ae5003b1`  
		Last Modified: Wed, 22 Apr 2026 00:16:29 GMT  
		Size: 44.2 MB (44207655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:218160481dc948cfbf943718a4363de6a3663997f19a965c7b86136ac3e28f30`  
		Last Modified: Wed, 22 Apr 2026 02:18:15 GMT  
		Size: 21.9 MB (21946340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:37b81509725954abc62dadf0563132020da2b226a8e6d8726039793c5b828303
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4523504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:240beceb031192c68028077e138831ec70e548c55c4b37b2a08fc843ee2d2a09`

```dockerfile
```

-	Layers:
	-	`sha256:4f9722a35424077a8395b7f9fcf41f1be0265df258323e27280514c7d31ae787`  
		Last Modified: Wed, 22 Apr 2026 02:18:14 GMT  
		Size: 4.5 MB (4516623 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b19cc59db80d51b09276485aa258a493f65633779dcbd37f035cb1dde3471e8`  
		Last Modified: Wed, 22 Apr 2026 02:18:14 GMT  
		Size: 6.9 KB (6881 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:30ef823c1033c660f83505327128878f738c121014404db5a16c9311a7a9528e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.0 MB (71982494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ac6f6e75f839cbb91bc96aba5b483bd6147c0bcc67db43c779589d7923b213e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:42:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:30de66f8fdafab67e88d876087f571a693a1a6c4cf0abc29efbf88ea878e0d29`  
		Last Modified: Wed, 22 Apr 2026 00:15:43 GMT  
		Size: 48.4 MB (48373071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bb7bd28fbdfe678a7f45878b7b1c07dbbc0fa7753b0312aa8fd049667a9e137`  
		Last Modified: Wed, 22 Apr 2026 01:43:06 GMT  
		Size: 23.6 MB (23609423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6cc95f0e6f404473e72a485f095eca6aeb894a75735687197e805a7d99f5473a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4521492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c132827ad90d3486798a5c093fc1379b24c580e78f435f87baa4b07511a23df`

```dockerfile
```

-	Layers:
	-	`sha256:c06cb72d19b41226e09a4cbf3efe63a52ccd1ea43a66fec2e7d58c50f11254bc`  
		Last Modified: Wed, 22 Apr 2026 01:43:06 GMT  
		Size: 4.5 MB (4514595 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20feba1fe8ba19f2281aacfcb4ae9941c491f9cf73d73ed2d7135cbd525faf0d`  
		Last Modified: Wed, 22 Apr 2026 01:43:05 GMT  
		Size: 6.9 KB (6897 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:c33c8cd14082f90636d0f0f946200a32a63a8639ee0c4ebb694d06f4f1690502
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.3 MB (74349888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f4bfc5bfc80bda6f0e9dd944ab5714a205727b729022527ce121baef45b5f3a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:45:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:6b838e591408b61fcf923bcc567649c4053d737a0dcf488cb215bcd633b7d70f`  
		Last Modified: Tue, 07 Apr 2026 00:10:40 GMT  
		Size: 49.5 MB (49477915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:240fa1f3927770a46d24419f7704239ba70e841afdde2d9e2629af344b11c262`  
		Last Modified: Tue, 07 Apr 2026 01:45:49 GMT  
		Size: 24.9 MB (24871973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:170ad219e0cdb2f888e214482dbbe76e20c3d88e6b4d1ca738be363c63dd6f91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4518248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:559672e0390f8677ca79c8a985a8267fd684258da8783bd74216522834afd76c`

```dockerfile
```

-	Layers:
	-	`sha256:0cb7087cd5727c9c1b746b598b153bba31640a3c5b07a17a3c58001e22c82ab7`  
		Last Modified: Tue, 07 Apr 2026 01:45:49 GMT  
		Size: 4.5 MB (4511453 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1268bd3fec73488cc30b510a28861c45d182780a17825243cda55dcba9df61e5`  
		Last Modified: Tue, 07 Apr 2026 01:45:48 GMT  
		Size: 6.8 KB (6795 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:b7a07c3396f4b0c8f3c20c7beb491de13cdbc262d797328f49aea208ab745e82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.4 MB (72397855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64ddf4b22426d41029801823e393f2391bab9469814dfd13fa67b374c89061fe`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 15:01:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7a9b4a7963b008240d9a254ca4fd1193c938bed0a9c6fe9c04630f13b1a17a44`  
		Last Modified: Tue, 07 Apr 2026 00:09:37 GMT  
		Size: 48.8 MB (48782593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5370b42611bdad35bb24b3e5a6a342f00eb8523dc8562b7babeca6f19608f4c`  
		Last Modified: Tue, 07 Apr 2026 15:01:37 GMT  
		Size: 23.6 MB (23615262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:0d3da12fb614dc3d5cf954a3c6d0a2a754ffcbd7fe3a115e495659ba8baf97d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 KB (6650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddc29fcf02bbf3ccfd66a4ede071c4968547af5260efcc91df236f9160cad628`

```dockerfile
```

-	Layers:
	-	`sha256:b5701e233a50ef324d460597e0b7a9064a17b40d17211b702d768af839e3a841`  
		Last Modified: Tue, 07 Apr 2026 15:01:34 GMT  
		Size: 6.7 KB (6650 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:04a6bc7e75f14374ce8e2aaade7772d143ad2877e219b6079d3fd052e2aa0b64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.0 MB (78008515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5c354d89ba22d3a9b6e2c44efbae0efb8a5f977551ee11b76d8f04421dca7f2`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 04:21:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:6b775f7ad22043f8bb75d535d8a1279e43453a08a4a9e6a0b48c020c9b387079`  
		Last Modified: Tue, 07 Apr 2026 00:09:43 GMT  
		Size: 52.3 MB (52336938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a522a501745b6503b15f6badc6170d6fa2321f26576c47b363acd8cb21b2ee`  
		Last Modified: Tue, 07 Apr 2026 04:21:54 GMT  
		Size: 25.7 MB (25671577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:3998bb20ab515ebdb115aa358a4fb6b284588d063c00f576551abdd57bc35768
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4525809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e4064c8a05050600b2799319bd0efaada4a72658264e2089c7d7b7f27e50de5`

```dockerfile
```

-	Layers:
	-	`sha256:8c050707dff502b9d779ca56bb19f45ae6520868d420ea384d0cb21bbf4d14b9`  
		Last Modified: Tue, 07 Apr 2026 04:21:53 GMT  
		Size: 4.5 MB (4518960 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ffe25b575a62a170708e763dab6b93874a984408f2fedc75b6a91df1b64dae72`  
		Last Modified: Tue, 07 Apr 2026 04:21:53 GMT  
		Size: 6.8 KB (6849 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:57fc1f40dde83132ce4676a662aeb225c62de7889da5e47c789e2e4df7535d60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 MB (71184333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07695240a43dcef4f344e886dfc6d0652eb0cce368ae4254baf5fc72ad9c1910`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 02:31:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:65a8acd2327b0f3316fe8707ebd5c99b15e79306d4eca71f3e635588795ae2bb`  
		Last Modified: Wed, 22 Apr 2026 00:15:31 GMT  
		Size: 47.1 MB (47147970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac385f32c2d6e9209dd9f8ada378863aba00921ac3815f399e84f802ea5ce36e`  
		Last Modified: Wed, 22 Apr 2026 02:32:03 GMT  
		Size: 24.0 MB (24036363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c2f82309e4ab8bde3a48f512099a19ae298f27b4c2b30af1f3c83fc1bddf23a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4517955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:093420b226a3827a6617cc61d00d5c5cb000c33169ce73ad460ab07b15177123`

```dockerfile
```

-	Layers:
	-	`sha256:85a33c90c8eb30dff9381213a1db3e2bab4c99a1d4aa3b0e3f9584f3c6339114`  
		Last Modified: Wed, 22 Apr 2026 02:32:03 GMT  
		Size: 4.5 MB (4511138 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8aed1fc73ae6f9fb6635ada6bd54b4938d11c070e91a4c327fb2e1895a5a3980`  
		Last Modified: Wed, 22 Apr 2026 02:32:02 GMT  
		Size: 6.8 KB (6817 bytes)  
		MIME: application/vnd.in-toto+json
