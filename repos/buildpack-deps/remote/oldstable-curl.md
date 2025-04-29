## `buildpack-deps:oldstable-curl`

```console
$ docker pull buildpack-deps@sha256:536bb910d642d6a212d2b20d5dbee986f26b8d31f43b8e8d024757030a1a9dca
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

### `buildpack-deps:oldstable-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:d46f632af1ce957541db52d3193c01a847e6cf30f0389b6cb5d8dda63e4aecd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.5 MB (69511284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f6280c6ef0fc6fbceffeac71b7f184a68b7450ec4c72a7b31c20af1584cee5c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1745798400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:19f1f54854d69811b3745bdd374e863f2fc2dc765fe37d1a30df3e590273322b`  
		Last Modified: Mon, 28 Apr 2025 21:08:07 GMT  
		Size: 53.7 MB (53747740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ee1ef79bfdcd8777f441528bcffb7a16f7a3d0852661baef04456810160e792`  
		Last Modified: Mon, 28 Apr 2025 21:55:44 GMT  
		Size: 15.8 MB (15763544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6b9c730ffb87f6966054a3b363768cf2660eedf425fd4cc97470eeeb44da2983
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4494396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a49c675e28df764c09caada1b09d0be3cde221b0b5378d26480ddf9e37e77d71`

```dockerfile
```

-	Layers:
	-	`sha256:ce8e54447a965d6bb403a1e208edb6650e424c20e0d54b8258175b757c4f8557`  
		Last Modified: Mon, 28 Apr 2025 21:55:44 GMT  
		Size: 4.5 MB (4487595 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bbcfcd080b20d2c56bd4973791d006372665e89a766b1dac0156a55cdad65599`  
		Last Modified: Mon, 28 Apr 2025 21:55:43 GMT  
		Size: 6.8 KB (6801 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:0bc7c8622cd8c56e48874ac60e025120163b8040e967d2f4b49223b586900e47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.9 MB (63910162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f57adefe8be669da2dd0e065aa10a7ef4e46fe525416a9dccf8caf01455b53e1`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1743984000'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:8c2fc9e6d23f3debfa68416a2b96331b92d563b20272933315ecfbbada38e955`  
		Last Modified: Tue, 08 Apr 2025 00:23:35 GMT  
		Size: 49.0 MB (49031449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:525b68fed12d763a57f1b020aa1579673112de80a5b780b5ffaa045109c81f23`  
		Last Modified: Tue, 08 Apr 2025 07:38:26 GMT  
		Size: 14.9 MB (14878713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:74a2dc6b13d6a4245ced86bc9245eb06ec8b7886c73620d364aac822de60fee8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4496038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b87b3e511becb82558ce8158ceca3612127ae88e84065cbb0ba3ddea4c76c79b`

```dockerfile
```

-	Layers:
	-	`sha256:2b2158ca015230ceda97b3f0ea5d09f32c66171fcbce3eb8623ab1c8cac4c43b`  
		Last Modified: Tue, 08 Apr 2025 07:38:26 GMT  
		Size: 4.5 MB (4489177 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29d8384c0c4ddea09e556f2f25b5d4410eb4313f61dd5405ff7d5f056ed24dde`  
		Last Modified: Tue, 08 Apr 2025 07:38:25 GMT  
		Size: 6.9 KB (6861 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:c2d3bde12cb01b63210b0267c88042926cd3196127300b61b2402c59ea15998e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.0 MB (68003308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c1ef2ff53a579dbfa9e1235ab11f8348d841539ab9350b08ee7eecd67075997`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1743984000'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:75f90a7fcbe0fba15646899ff45dbbdeecc9661d3b9445f4ef346d30119fe345`  
		Last Modified: Tue, 08 Apr 2025 00:23:22 GMT  
		Size: 52.3 MB (52254222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9322dad1d7c942b6794e486e4e0b838c10dfb06247f1794d20cc703ddfee969f`  
		Last Modified: Tue, 08 Apr 2025 06:03:40 GMT  
		Size: 15.7 MB (15749086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:34a0e3d2f03c84c8659c79a0ccf799f7efd43965078580da2f079639edc23003
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4494036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3417529ebeef7d165205c013a7ce026626264d9bf6c18397f76fadc26018cd3b`

```dockerfile
```

-	Layers:
	-	`sha256:4e601ba990d7c970f12770b33aa3d11ef202e01db99a958eeafbc02b731a7eb0`  
		Last Modified: Tue, 08 Apr 2025 06:03:39 GMT  
		Size: 4.5 MB (4487155 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4caa97b0e18521b70bde8bf387af2f0fd929d793be3f3f54a11f9c4e66a561e8`  
		Last Modified: Tue, 08 Apr 2025 06:03:39 GMT  
		Size: 6.9 KB (6881 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:b1c0cfa8c32d56d8fab9743742ebd5184a5be165352f0d29bce30ed1401d9182
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (70950501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3ea7c3daa707cdf14a3ce4de2fae8455c730f1cf2e5307a1358bd0761cd0105`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1745798400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:4ef50a397f2c0106a3e44d1d1bae16cf52fb5e7e855c588f4098e281321c3e7b`  
		Last Modified: Mon, 28 Apr 2025 21:08:10 GMT  
		Size: 54.7 MB (54683102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cbb48ef4c334135b55fe5dd328911059bfd41eec15edf03ff0ab96ca44fb6a1`  
		Last Modified: Mon, 28 Apr 2025 21:53:52 GMT  
		Size: 16.3 MB (16267399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f56cc8c94d9a7f00f928dd03f18d8d39c453eb65398a61a3b1355f331beaab62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4490815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:304dc762690dd477bf58d270ec35ddfa3fb851cd33d18c371250eeb1f713dcee`

```dockerfile
```

-	Layers:
	-	`sha256:fbc6e7d5789639f0a02523cc743a26a849d781abaa63fc9d69c5e2e3a4086322`  
		Last Modified: Mon, 28 Apr 2025 21:53:52 GMT  
		Size: 4.5 MB (4484036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b63dfd5e44edaa04e3d1b82b9fc300099b24b1b51c58fe250491a799f3fd801a`  
		Last Modified: Mon, 28 Apr 2025 21:53:51 GMT  
		Size: 6.8 KB (6779 bytes)  
		MIME: application/vnd.in-toto+json
