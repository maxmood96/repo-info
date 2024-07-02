## `buildpack-deps:trixie-scm`

```console
$ docker pull buildpack-deps@sha256:4f54a3b9684fee92bc6e642dea456b335cf0dda1767f7a3d8c82f906fa9e79ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:trixie-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:4c42ecb88b3ec59ba808db443ec01f74f1564bfaa4bd090b6a3b203c3f5a5230
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.6 MB (137632404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6115d13d01ce8f5aeec86478625284c0f4440c8d246b6766e25e4d057ec88d30`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 01:26:59 GMT
ADD file:90c4ad8b280b16131f305780a1f2721616642bd4d5b4a26256c760cd8ae98f27 in / 
# Tue, 02 Jul 2024 01:27:00 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:54:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 02 Jul 2024 01:54:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:ca828e2fa86974a7bad5159e89a3c4f34921c624322a7fa71026f2a3933ab620`  
		Last Modified: Tue, 02 Jul 2024 01:31:45 GMT  
		Size: 52.5 MB (52458214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:687f3d296dd0e92cd772395160b84eeaffb55fa2ffce846bc61595e5e164a5e3`  
		Last Modified: Tue, 02 Jul 2024 02:03:19 GMT  
		Size: 19.0 MB (19021831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbb04f2f4343d6b362ed3e5d55a9e7736eacbe6aaa43d185b2b3e8af75e33528`  
		Last Modified: Tue, 02 Jul 2024 02:03:35 GMT  
		Size: 66.2 MB (66152359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:dc47173aea07707872c036356887da17032c30d9b6b0d9aba36aa72c7b720dca
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.4 MB (131366630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:168a405a841f90f0cdf45b6f3982ca100980d8a8a15a333dbc774579507fac71`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 00:49:52 GMT
ADD file:c318229166795e4eb716c1fa6af23bbb2d4ecba024b60f621a291810a3a401d4 in / 
# Tue, 02 Jul 2024 00:49:53 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:20:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 02 Jul 2024 01:21:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:000d0bc5723ca659fec8fc6ce252cb52307971eb476903fc3b9275de15df06e8`  
		Last Modified: Tue, 02 Jul 2024 00:54:39 GMT  
		Size: 49.5 MB (49521421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:736d7cf5b3e3c6cf6b2dca2768e87625a43b941f89b6406ba80bef82b5dcbee3`  
		Last Modified: Tue, 02 Jul 2024 01:25:57 GMT  
		Size: 18.0 MB (17968957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e085c26efcb68cf6283027c6da91a96cdc6853a2e46a54addc7366a9803c4bc`  
		Last Modified: Tue, 02 Jul 2024 01:26:15 GMT  
		Size: 63.9 MB (63876252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:5b878a5e4cc16c3999f4c28f96d369bfcc9085e6e721b77ec092fb3596face62
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125671112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:700d52f32920ec1796f3c7ef4154ce5845466c0b699dc2564b4a0bf8693fa775`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 01:01:43 GMT
ADD file:527e478975b1f859c9421d232809fcdad4ae845a2591655169c3c0cbd9556cb0 in / 
# Tue, 02 Jul 2024 01:01:43 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:30:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 02 Jul 2024 01:30:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:e4626e10f2b2fa1f8bd684a19417be06dce44506821e68c986c039ebcf444ea1`  
		Last Modified: Tue, 02 Jul 2024 01:06:18 GMT  
		Size: 47.0 MB (47028058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdca2198e49697301427c37393c92e7e2c23045ee43c3f521b70811fad9baacd`  
		Last Modified: Tue, 02 Jul 2024 01:42:27 GMT  
		Size: 17.4 MB (17362030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53904b9da40d410bed49b2fce148f70c4bb32e0d641635fda45634ed2b643633`  
		Last Modified: Tue, 02 Jul 2024 01:42:47 GMT  
		Size: 61.3 MB (61281024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:879cf292ca55f2dac3f60d1ae87c900d99a880b17f984e3cea0f803942fb91a8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.8 MB (137810832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8a97ec39812e39e1c687955dc4e4357d504033c6bc4b60b658da73fc4fb46db`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 00:40:56 GMT
ADD file:231a92f6a31914243d9c6358dbd08017ac703b3270465f6d231f3d178f7e783f in / 
# Tue, 02 Jul 2024 00:40:57 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 03:55:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 02 Jul 2024 03:56:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5bed35cfcfc0ac7f84b7a2c93f738e00119f31c9a82999f6fc0e8493ceff3010`  
		Last Modified: Tue, 02 Jul 2024 00:45:19 GMT  
		Size: 52.7 MB (52693320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9751e3702568b536545773c8a831b25db2876eb1b4d0823a3cfa663395793f96`  
		Last Modified: Tue, 02 Jul 2024 04:04:20 GMT  
		Size: 18.8 MB (18763001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b302bfdc7cbaed0a8ebc1a14e878b03d086764643d49d881cf50b66a5a851fc0`  
		Last Modified: Tue, 02 Jul 2024 04:04:35 GMT  
		Size: 66.4 MB (66354511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:14d77bec735b0db701c7b9e0db46afd5a4ce074230807fcd268fa53372e61370
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.3 MB (141269892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c56bedaaf854248b902da5dcd667e0b11fbfe42d0d418c0b22d4336e795486f6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 00:40:52 GMT
ADD file:2c79a29515e7dc495de2293d9b08d4b2ecee86e61c2d0adf1658f7b939d57c1c in / 
# Tue, 02 Jul 2024 00:40:53 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:12:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 02 Jul 2024 01:12:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:86c6de18cd170a5e610d31625f09596aeecc408fed7171fc8922ae0196331108`  
		Last Modified: Tue, 02 Jul 2024 00:46:09 GMT  
		Size: 53.3 MB (53333176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ed3a89daa70bb513739a2ade83fc5f0a43a784f37749e2584d3c335224ae6e7`  
		Last Modified: Tue, 02 Jul 2024 01:17:53 GMT  
		Size: 20.0 MB (20029610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3099c8c1942a3e6f5ac57d77a04b1e727414a9f58f935b9f5458db57884654a`  
		Last Modified: Tue, 02 Jul 2024 01:18:14 GMT  
		Size: 67.9 MB (67907106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:434ad09beeeaf63fdfe2af786c50af25111a4e0eaf5e04a3a7556d5e0ea44c19
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.0 MB (136008670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a1dd62f9d23abb8e3ebdfc8fa61452ab4d8aa73261e3fbd26e811b706c0c7ac`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 01:25:15 GMT
ADD file:3db649d00cbcab4f80ae59713bc5516d64748afefc7b50d6ec9b17f007a2d82a in / 
# Tue, 02 Jul 2024 01:25:20 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 02:21:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 02 Jul 2024 02:23:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:f6c6179e3393971283f4159a87b337ff64cbda1886dbd0e30fe99b15d1f2b7ec`  
		Last Modified: Tue, 02 Jul 2024 01:36:31 GMT  
		Size: 51.3 MB (51311657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8992fbd14e1b9fc5fdb381b9396a2ccb1f18397cae60807f219afbcf1579ac7b`  
		Last Modified: Tue, 02 Jul 2024 02:39:15 GMT  
		Size: 19.5 MB (19507340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f227430dafb09eb295efcfc652188f4b6892b99c5ccb986b8e11138216a465e0`  
		Last Modified: Tue, 02 Jul 2024 02:40:05 GMT  
		Size: 65.2 MB (65189673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:8032c73ca1f1c7cd286d0d6f865d0eeb17c76dc0717ee79096e04e15e9184918
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.0 MB (149042048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba8573b3ae401c599c87aed4660ba7e77be112cc47396d3f9eaa52e3cb36603b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 01:19:54 GMT
ADD file:2befd9889f7183dff7c3af514af787c529a360a9bdb089a9e9db6dafcd6001c6 in / 
# Tue, 02 Jul 2024 01:19:57 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:53:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 02 Jul 2024 01:54:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:1562048ab74aa86e6df4a38c0c8f568200759fc4f56abccc22d1df342f206dab`  
		Last Modified: Tue, 02 Jul 2024 01:25:27 GMT  
		Size: 56.3 MB (56345204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dea8d116669b7a9effcef7da51c6a3adb0b03e6013b8bdbdc06106781c822b6`  
		Last Modified: Tue, 02 Jul 2024 02:08:00 GMT  
		Size: 21.0 MB (20982544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf30d890983307c7c405d9221c5b4107daefd6f37bc649fd38c82720f869cfd8`  
		Last Modified: Tue, 02 Jul 2024 02:08:19 GMT  
		Size: 71.7 MB (71714300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:fae234826afee1e71edc720d3c0bfaa23265a3cd1d57286f65f60b7c37ee61d8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.7 MB (139747249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e27ea36bffa41715ad97f1d70f607d5ab936710dea1ad0bb75691a6bdf49c0ff`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 00:46:19 GMT
ADD file:8bed729fdb05f23c2c9685e4b49aca399cccb129d549ff0cd5178ece57a34073 in / 
# Tue, 02 Jul 2024 00:46:21 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 03:38:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 02 Jul 2024 03:38:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:7663a7e6ec84fcce1d022bfe86b7d77ebcf92e841e95456e76280883841e0985`  
		Last Modified: Tue, 02 Jul 2024 00:51:04 GMT  
		Size: 52.1 MB (52089479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbb594591801b3f0f0c97b7761fc4001fd8d788cd8eb1fac03442aa5ccbab471`  
		Last Modified: Tue, 02 Jul 2024 03:47:01 GMT  
		Size: 20.2 MB (20208262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c71f5b2f892fbc7bbfbf5e24b35413c82ba30845f64c37d9ec5bd2ca8a5cabfc`  
		Last Modified: Tue, 02 Jul 2024 03:47:15 GMT  
		Size: 67.4 MB (67449508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
