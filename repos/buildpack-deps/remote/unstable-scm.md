## `buildpack-deps:unstable-scm`

```console
$ docker pull buildpack-deps@sha256:69813fa6c0df33b899aa2566c77effa517ebc79aeaf50ed536ad5da93761ebba
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 18
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
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:unstable-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:341a0b57d2b16179f0dd59ae8b0fd66545a0766d6435bade43642063df056ac5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.1 MB (143095957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:234e297b09eb1b7340d85e8ad8cf502b18e8c565140478ebad7defafeecb32fe`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1751241600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:603de70df79137e44ed9b8e9d2eec3a1b8eb889b8a8650df1a6bfc2ba9798f72`  
		Last Modified: Tue, 01 Jul 2025 01:14:45 GMT  
		Size: 49.3 MB (49267699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b752883ea09044589f48c52df49289712f416806e7b67e6d3b283e6c96ac266`  
		Last Modified: Tue, 01 Jul 2025 02:25:34 GMT  
		Size: 25.6 MB (25619155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb14a16253ea0df4ebeb77b1db25ac37e73812925ccf4de831d1f7bc411f2c38`  
		Last Modified: Tue, 01 Jul 2025 04:11:59 GMT  
		Size: 68.2 MB (68209103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9f33435c6ebce0f65890ce6e2c0cd5afabf06db7f0792bcf0df87801373fd678
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7785960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a296c583045141ecf21098993f50a2d21de384a36f7a83ab0429f9c41ea78c1`

```dockerfile
```

-	Layers:
	-	`sha256:f905e0475b1abdfbb452be9d28bc18875a564d7d54439a1393fc224120d8ce21`  
		Last Modified: Tue, 01 Jul 2025 04:20:59 GMT  
		Size: 7.8 MB (7778664 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b04e3e8108bf5c459285697f1c4c21463bced81f3f67c073d47063bac5e950b4`  
		Last Modified: Tue, 01 Jul 2025 04:21:00 GMT  
		Size: 7.3 KB (7296 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:7d461e7f0494157983e05bb249237790d3f8f7f517684e28f87da406d3571c05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.5 MB (137518143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e136b3ec4cbca3e7e8a75b90147c54ee66a6f97be08cc5b31c77153313d2f178`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armel' out/ 'sid' '@1751241600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:fd39e087bd20994f06786e43ae83cecd3968cf0c8e31fda1f457b3222b6b6540`  
		Last Modified: Tue, 01 Jul 2025 01:15:07 GMT  
		Size: 47.4 MB (47440208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4cf909077bd520f713ad0bb67e6ba6cb18dc45cf617fb6f8d5e7a63b048c164`  
		Last Modified: Tue, 01 Jul 2025 06:08:19 GMT  
		Size: 24.3 MB (24345967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8df6e38020028956bdeaa81464be7d4bdbf7dcfe67640edf45bca2f56aea465c`  
		Last Modified: Tue, 08 Jul 2025 01:33:02 GMT  
		Size: 65.7 MB (65731968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:43ae152200bbf941251fa8684a92af70b73ae8b4ca7b2e5765157f49ffecc262
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7796304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:713ea99029bd6456512e011cf12bca2140450147166c3f711a7e5af4a6b6f0be`

```dockerfile
```

-	Layers:
	-	`sha256:c9f7f56ab6cb05947c4b681a1c97315b4ded0dadfa770734da60b19c7d2b53eb`  
		Last Modified: Tue, 01 Jul 2025 13:20:57 GMT  
		Size: 7.8 MB (7788947 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ef19f6766ef52ab2ff72505547befb66db990a0cc8f793bb7cb79e4141d81de`  
		Last Modified: Tue, 01 Jul 2025 13:20:58 GMT  
		Size: 7.4 KB (7357 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:7435fb673ca53c1fee6f5aab684641012b2cb973307bc7fa33e2cda53fb3519f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.5 MB (132480868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b6b1db1fff9250a525358b6e937e537e0c494a3de7c01356988aa8a95546798`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armhf' out/ 'sid' '@1751241600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:c9f75345f8518e5dbbf40af904c00f3e014f0846ed6946f7fe425ac03a8e75b1`  
		Last Modified: Tue, 01 Jul 2025 01:16:26 GMT  
		Size: 45.7 MB (45709047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f7f9ff4c752d1f9e8936db04d44226667ece5c3bad3798a0f88a5404d9f206`  
		Last Modified: Tue, 01 Jul 2025 08:59:49 GMT  
		Size: 23.6 MB (23618470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59681cc62ca4eb6c592f99e5bde64f4b1fc54a1a76864ebda73f827aa1b4361a`  
		Last Modified: Tue, 01 Jul 2025 18:31:01 GMT  
		Size: 63.2 MB (63153351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d11a2e033b58fc758fe022cc44264b005cfb7c239298a698dac6a58c92a9258f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7786520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31c8a7cd7a0597b499851ba66172648630eefd86782a34fdc1958c61cf76b10a`

```dockerfile
```

-	Layers:
	-	`sha256:9782665d338bf9b8b58071126ce7f6241fa5d441b9efe7f4ca0af3144eccc5fa`  
		Last Modified: Tue, 01 Jul 2025 19:20:55 GMT  
		Size: 7.8 MB (7779163 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ecf7988dd621e09b709e47ec76ef49e2a74d9dbf206e9dcb084a967b581f1f8`  
		Last Modified: Tue, 01 Jul 2025 19:20:56 GMT  
		Size: 7.4 KB (7357 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:cfc20510317ad260a63fc09dace011550e991013f9afa313ac8ade0c9b64e15f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.6 MB (142629455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:879f752558200522c202c9795a2778c787b212e483807d364ee1a313439a1b7c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1751241600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:22b8dcea0b04f0cc6c2f22278513a305f4657bbd6ff8b7b3b8d205b40cebc22e`  
		Last Modified: Tue, 01 Jul 2025 01:16:26 GMT  
		Size: 49.6 MB (49633737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cba22b3a401d582005c703416897d35ba010c24db8d110f9011886e05173de3`  
		Last Modified: Tue, 01 Jul 2025 06:52:58 GMT  
		Size: 25.0 MB (25009526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b35fdfd4f8345d7a21ff603855a2ab09ed78a0c3589580e64572c63d5d766676`  
		Last Modified: Tue, 01 Jul 2025 13:30:24 GMT  
		Size: 68.0 MB (67986192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1341754bb133074aec38f1655feb49fecff9189fbe8bb490a76cd94edbb8e90e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7793704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:789ce837d62caa7c18c74e1b10bcbbce0da9b27cce68601400032e6ee91e711a`

```dockerfile
```

-	Layers:
	-	`sha256:16275b868581630d0e24f198ec7a9a8d62405b412bb546e8b44fce2c1e34205d`  
		Last Modified: Tue, 01 Jul 2025 16:20:44 GMT  
		Size: 7.8 MB (7786327 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29f6667ebd72980b53e528c9837432e04bac7dc65111250d4ac7ddb2c46e1bad`  
		Last Modified: Tue, 01 Jul 2025 16:20:44 GMT  
		Size: 7.4 KB (7377 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:12a8b731a15ac989d4c0ecf58c8cf4b2ca697328589ecc69e4d8c96899101b60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.9 MB (147850682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bda7f13a0d9e866ae46b8c46d1bda7606e312ab066fdf3f1cca24606d24ac45b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1751241600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:41ea081e29dc4034ec31a49ac48ddbf738b840fd4d226f5678cb63f00b10ab33`  
		Last Modified: Tue, 01 Jul 2025 01:15:01 GMT  
		Size: 50.8 MB (50790707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d224078a83c5498b9115edbeec34eecaddc04a9e2e47f0e71d34a7e780a2059`  
		Last Modified: Tue, 01 Jul 2025 02:24:36 GMT  
		Size: 26.8 MB (26773974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be6014d1af113edbca3a63a8a8aff65bf03bbb831dcab023e346303a638c1250`  
		Last Modified: Tue, 01 Jul 2025 03:19:59 GMT  
		Size: 70.3 MB (70286001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:14b6a8a1fae7a389dbdd32b73a894bb37ea966361e77e6f44cba3331598a882a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7782080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:864bcd851bf1d378f5d1ff51f1ef08c35a956f5f5e5bcc43828fd3f3a0cb8d98`

```dockerfile
```

-	Layers:
	-	`sha256:b0e58f4e950070edd432fd0116f2c307f5f9e9e15321ba71b4c276cae598c7b1`  
		Last Modified: Tue, 01 Jul 2025 04:21:27 GMT  
		Size: 7.8 MB (7774805 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ef0e6d7e7f58f927fcd2f1851077fd2e32f8b35023908f287dde95946d1463b`  
		Last Modified: Tue, 01 Jul 2025 04:21:28 GMT  
		Size: 7.3 KB (7275 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:f132010f2ea7299b6f0ef6a0cbcecbc6f142abe32289dab725cdd2365cd53ecf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.4 MB (142391349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ac25c33aac79792a6d5ba0688d7b8b85ff83aa7f8e89cdd8ae8e7c9be33c502`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'mips64el' out/ 'sid' '@1751241600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:ad926ea8e83c042a73d78f88f96eb49414795f66dcc267a85d9852f179b0c83d`  
		Last Modified: Tue, 01 Jul 2025 01:15:27 GMT  
		Size: 49.6 MB (49558347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a0e25832798c28ea6fed5958b87a1275a2e1ec0ae14c386fa13a9161bf99712`  
		Last Modified: Tue, 01 Jul 2025 18:51:13 GMT  
		Size: 25.7 MB (25668967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:824e711c89c1d7fca8a8e6f46101a0bc67d6013a4eb73fe9d978a3b132d0356d`  
		Last Modified: Wed, 02 Jul 2025 03:06:26 GMT  
		Size: 67.2 MB (67164035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ca12fbaa4e8f2d9bed53a0b7ab9abaf74c81a73db81e225f21cd98e8e4aaa4f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 KB (7130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3f0c1935f14221ca3ddcd40e242deab1d18c26e4041a987a26d18d85cc5947a`

```dockerfile
```

-	Layers:
	-	`sha256:5631503abf79e906b979a8bbc17a600ff053877d6bb9a71cfd56355f31313acb`  
		Last Modified: Wed, 02 Jul 2025 04:21:21 GMT  
		Size: 7.1 KB (7130 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:6abcdc295cfec7d85c94d2ff546eeff233a2474fcee24f95511f9814056650c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.6 MB (153582244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea757ff976c8049eb0ae6a34f9576bd2a9cd7afa6d89446203585fb8a3f3297b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'sid' '@1751241600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:ffa7252988b58d241b86b58e553a13c9ab6ded3d6fbdc73ace28ee71d043ceae`  
		Last Modified: Tue, 01 Jul 2025 01:15:58 GMT  
		Size: 53.1 MB (53101309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:770aa93e38d20512e91dacc6e2f7a3a7358bc81f356fbf0317b659cafa8ac481`  
		Last Modified: Tue, 01 Jul 2025 05:07:54 GMT  
		Size: 27.0 MB (27003579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02be88bce329950d3d92db09ce4cf3130958aaf32bd985856e638aa08ff050d4`  
		Last Modified: Tue, 01 Jul 2025 10:11:01 GMT  
		Size: 73.5 MB (73477356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:526c64bc52922586ff351993ec8a18ef2a6c1531fad64b44509e0964fa1f34b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7802361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19ac18d9f86d1618c121be89db30f758c7ca59818dce55e3597d5b8874bbbc66`

```dockerfile
```

-	Layers:
	-	`sha256:b2c1d4de617c20310509cfeb2c38c127035b190fcf79793ad516dc98c1c0d658`  
		Last Modified: Tue, 01 Jul 2025 13:21:22 GMT  
		Size: 7.8 MB (7795032 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4254944c48f71fd2095b0df80a4de6f35fe271618c319c3b4ed15cd71b730d84`  
		Last Modified: Tue, 01 Jul 2025 13:21:22 GMT  
		Size: 7.3 KB (7329 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:c943f0df1229a3e28ac477d138c40fd08872d11f7de222ad53ddaa72e6f05986
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.8 MB (139802594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce16ffb167865e6220ea2272051deb55f210901f0990bc336d1b99fa5adc706c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1751241600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:42f7c08d656e09c01f14d35a847143f84e881d1ac3f16f3ba511348bbbaa7d82`  
		Last Modified: Tue, 01 Jul 2025 03:27:03 GMT  
		Size: 47.8 MB (47756066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17a4ef3bea202b6f661456b37f5106a6a6e0acda6439394bd6618c6150a35c24`  
		Last Modified: Tue, 01 Jul 2025 02:22:42 GMT  
		Size: 25.0 MB (24954336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89f59f94fee11898b889be78db1b26357b77690be8753df91b533098e18b75eb`  
		Last Modified: Tue, 01 Jul 2025 03:58:27 GMT  
		Size: 67.1 MB (67092192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:65c3595b06707ef5426bca16f71cb4f66d35ec7e0ae4f3907b151a328ffa218a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7775820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09b53efe2f6dfcc9c74753e064965dd8b027f962c71270fd3457baea55453523`

```dockerfile
```

-	Layers:
	-	`sha256:9dd4435e2ee2298f9a1bc1df11cc151392ee318da2a40204a523df4a3283f0fe`  
		Last Modified: Tue, 01 Jul 2025 04:21:47 GMT  
		Size: 7.8 MB (7768492 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:520805d6dc202af83c93803382120eb09227a998e179b4c9256ddfe72c8a9017`  
		Last Modified: Tue, 01 Jul 2025 04:21:48 GMT  
		Size: 7.3 KB (7328 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:f6304f4124c45e010879ecc9dbe6745152bbd2d30b3f0a56aa9183e0cb811fec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.2 MB (145183359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0d20c38b07b996dfbc65590d82786b74de9bafd981262350948cfedbf84677c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 's390x' out/ 'sid' '@1751241600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:4acd445fdd6fc8a863e2e2fbc1f6d0dd614a42ad5a89118b6cd287f18c027f79`  
		Last Modified: Tue, 01 Jul 2025 01:16:17 GMT  
		Size: 49.3 MB (49346648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4d516536545f6fd66256972b93b51614ab1c9f96883e1f5c8990597ce59c040`  
		Last Modified: Tue, 01 Jul 2025 05:31:15 GMT  
		Size: 26.8 MB (26786410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ca1529b246d5d5bf9d3254f1e2eb47235c74e91731ad440f78e506bbce83b45`  
		Last Modified: Tue, 01 Jul 2025 08:57:01 GMT  
		Size: 69.1 MB (69050301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7cb229de4961437de09372793647efe225f49ff689b3b532cc3079ed1aec7c27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7796127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e031870ba8ee01ee180569687a2289a1adbcd3bfed2c1cd756fef7ee6017c75a`

```dockerfile
```

-	Layers:
	-	`sha256:02cf29dfba17a257dac937ad808c8f9f80df511c58940f19df57322de5643daa`  
		Last Modified: Tue, 01 Jul 2025 10:21:04 GMT  
		Size: 7.8 MB (7788830 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a39d99a1b7c617975bea309d04115a94e9519bd2ff331eaf55bd4287987839d`  
		Last Modified: Tue, 01 Jul 2025 10:21:05 GMT  
		Size: 7.3 KB (7297 bytes)  
		MIME: application/vnd.in-toto+json
