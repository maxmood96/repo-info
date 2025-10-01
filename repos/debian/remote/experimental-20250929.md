## `debian:experimental-20250929`

```console
$ docker pull debian@sha256:bb0a2172a5ad7f3a10e741da57c040ae98f3ddf09ad76f5e0b38704007869718
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
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
	-	linux; riscv64
	-	unknown; unknown

### `debian:experimental-20250929` - linux; amd64

```console
$ docker pull debian@sha256:187943a70d1d83ba8c21bbb2e712fe09af9b3e410bf221a561412cc33f520124
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48377192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0107e067f7ad862ed6e43246ac5afbcde0652813654efb1ab91cf99ffe3abef`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'unstable' '@1759104000'
# Mon, 29 Sep 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:2e268ef41e6726cf436878e5d758c3cf512eac396b4c66cf7cc4a3c6bca39ce7`  
		Last Modified: Mon, 29 Sep 2025 23:35:35 GMT  
		Size: 48.4 MB (48376972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74d5235f4f812c27f8a04cff1755c4265746565647f56568418e4ae002bbe41c`  
		Last Modified: Mon, 29 Sep 2025 23:48:05 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental-20250929` - unknown; unknown

```console
$ docker pull debian@sha256:c67739821711e99e2bc569a681c51668ba8d9b60bacf3bcae4c818ab4395cc18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3133799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26b1d9fc823632a5c1e4b91b5b9b5244678bd4abc70a0437ca34d888b4d57ff4`

```dockerfile
```

-	Layers:
	-	`sha256:778dbc71f41ba7d271d7d9c088d9af64deeb4db411528737f62decf51a44b859`  
		Last Modified: Tue, 30 Sep 2025 00:25:58 GMT  
		Size: 3.1 MB (3127655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de7fbcc8ab9f607f4fafa543c51411f2d7e183df3f5140ef859186ccad26b29d`  
		Last Modified: Tue, 30 Sep 2025 00:25:59 GMT  
		Size: 6.1 KB (6144 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental-20250929` - linux; arm variant v5

```console
$ docker pull debian@sha256:2d2918ef962eb204d71f88c5a7342e2573fb3d6d571f728af8964a6bd7d82f5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.5 MB (46536829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:866df0bb2a862dabb413cf27f8a330313346e1e7e0de553d7be404e4fc0ca003`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'unstable' '@1759104000'
# Mon, 29 Sep 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:42d2eb177161037e0cdbddbce89eefd965ff50b20fece708033603749bcb2ddc`  
		Last Modified: Mon, 29 Sep 2025 23:35:23 GMT  
		Size: 46.5 MB (46536609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6116c9c75597538317730c5f0287104c7071959b6ca655be4a6ed04e36c2a93a`  
		Last Modified: Mon, 29 Sep 2025 23:54:02 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental-20250929` - unknown; unknown

```console
$ docker pull debian@sha256:a158905ee9b6980b898a2f061948f3721074ec7667d3dc14295babed4cb19551
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3136823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:611e9df48caea2d11051028a17ab974bc273bc16f7da1e0fd8d993c836952ae6`

```dockerfile
```

-	Layers:
	-	`sha256:e58112a2c35aa42a4bf2effb26a8c4a7471d9c0906d218c64f48c6bfbc45bf56`  
		Last Modified: Tue, 30 Sep 2025 00:26:04 GMT  
		Size: 3.1 MB (3130615 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8728e9c23e8f0333025bcba49f7de4e0af3e438cb2ef83dc90449d9f72fe4d6`  
		Last Modified: Tue, 30 Sep 2025 00:26:04 GMT  
		Size: 6.2 KB (6208 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental-20250929` - linux; arm variant v7

```console
$ docker pull debian@sha256:6e5c660b2a5633ba47b903f60836d9fbfb14d6d3b0b6ae9cead5b056b1de32b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.9 MB (44859017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c2dc2ab36f0d7113f006ae9c7bebac9baf8450777d65cdd5d78ea3b9f195aa2`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'unstable' '@1759104000'
# Mon, 29 Sep 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:b2eed836a24562fe0aad0bca4413791f841f2a9774d8c56a8c1eec4c5a998775`  
		Last Modified: Mon, 29 Sep 2025 23:35:33 GMT  
		Size: 44.9 MB (44858802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b630f08bfed1b9d87a168bba6242f09cbc575efa12e028b0b2cf3161428d1eb2`  
		Last Modified: Mon, 29 Sep 2025 23:54:09 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental-20250929` - unknown; unknown

```console
$ docker pull debian@sha256:6d94e732ecb8ffb17369d10b29472922a968db010c88bde039948e6b4ac6af8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3135239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c5b537333f4df0584f321709a135d5b8daf9d60ca0640243a6417aff22f33b8`

```dockerfile
```

-	Layers:
	-	`sha256:1fafab4bbe98637064b504c8fb5f6e7e3d93a6cc1291bf077cad4a355642bcfc`  
		Last Modified: Tue, 30 Sep 2025 00:26:08 GMT  
		Size: 3.1 MB (3129031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08a10b80681ce2077858bc902e506c6b2a06dd8349a17110eb7580c6ffb9fac4`  
		Last Modified: Tue, 30 Sep 2025 00:26:09 GMT  
		Size: 6.2 KB (6208 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental-20250929` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:2dba54ca86d5200474271547dfb8fe2bfab6cfa99deadef9e5673ad3a1547c96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48488218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8168e1ce18d5df30628ebfd0ec798f48127de23d521d2db1ceb80cb627c9079`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'unstable' '@1759104000'
# Mon, 29 Sep 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:69805609f7e9ecc5161e34bd20abccabb4ffee21d6ab2248335a8a349dd1efef`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 48.5 MB (48487998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70ed9a2de812564c2a973860c48022441e538d86a48baf634a4d337a3c9e6d70`  
		Last Modified: Mon, 29 Sep 2025 23:48:32 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental-20250929` - unknown; unknown

```console
$ docker pull debian@sha256:5e01141b8c190a46001271c733625aee570b129f652436c68ee0fa7b3bb3eb51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3134732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a5ea4f723c22115bd84919c09861c107d02242052775aeb43e419ab96c1ba6b`

```dockerfile
```

-	Layers:
	-	`sha256:18a24a511329fcaceb2f831e4cbbf48bf5da223763d9f1ecf219807882ee9f22`  
		Last Modified: Tue, 30 Sep 2025 00:26:13 GMT  
		Size: 3.1 MB (3128508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b53a4fa51b7c8f539f3ed45916ee1cd85473f3bc68fc4606ac6820ff56c0f2bc`  
		Last Modified: Tue, 30 Sep 2025 00:26:14 GMT  
		Size: 6.2 KB (6224 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental-20250929` - linux; 386

```console
$ docker pull debian@sha256:bcf1e41cb805452a53f8b738216c7fe86b048ee5f3a85f5fc876f8da4a23eae0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49686398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97dc1efcf2f98027611584a5c0f08242281b9ffb405192c8112d6cf633ee2f0f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'unstable' '@1759104000'
# Mon, 29 Sep 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:5ee4cf48d82ee90d6d27587a7f7a8973d68eb3b04d974f0a2875d59665caabf0`  
		Last Modified: Mon, 29 Sep 2025 23:48:27 GMT  
		Size: 49.7 MB (49686178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af4f72281d4c063b3850bf1ce9ef9ae96801a18a610dc43302a37e645a0796be`  
		Last Modified: Tue, 30 Sep 2025 00:00:23 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental-20250929` - unknown; unknown

```console
$ docker pull debian@sha256:0832e7cacd4ccbc4197b2938fc72f00ebaa27c8c5816ac701ebf3e892c654ce1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3130981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8d06a670ae79c6967989d85415b1b1e42f558cf13a293ff8122d35e12638db7`

```dockerfile
```

-	Layers:
	-	`sha256:9d3c887841e64b29459e92a7874238368e837d815ef98cfa39e1165b40cdde15`  
		Last Modified: Tue, 30 Sep 2025 00:26:18 GMT  
		Size: 3.1 MB (3124859 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ac35469672841fdf39438fc4f877c59b278c1dd03b1777317fb6caf737c13cf`  
		Last Modified: Tue, 30 Sep 2025 00:26:19 GMT  
		Size: 6.1 KB (6122 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental-20250929` - linux; mips64le

```console
$ docker pull debian@sha256:aef25feb7fd42fc05e474e3656acbeb16f887e0aade00277969e4a4ba27a20de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48517295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e211af734d9108d540b4bf6a14896f412b5cbfb04063985619f81b86b41a4f4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'unstable' '@1759104000'
# Mon, 29 Sep 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:0061624ae5f0179085c630a23bbeb44b96a64b30d9a1f379a8f67c8f7619921f`  
		Last Modified: Mon, 29 Sep 2025 23:37:10 GMT  
		Size: 48.5 MB (48517075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d979516d09e9edbdbbfe2e92092282f1d9180d4334c7469d7d4d83ead588d339`  
		Last Modified: Tue, 30 Sep 2025 00:17:25 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental-20250929` - unknown; unknown

```console
$ docker pull debian@sha256:3ad1bf8902e345adf6d9134218bc0a8c4b95e2f7f3ad098f93c382986f8b16c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 KB (5977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f4033bfd9aaa29b205c9e79179f664a49036b7ec0781eb06a9bf32525557530`

```dockerfile
```

-	Layers:
	-	`sha256:94ff6b8e02dd7d2de52784001f4c18eb928251310bdc5dd49bb048507ec2bc89`  
		Last Modified: Tue, 30 Sep 2025 00:26:23 GMT  
		Size: 6.0 KB (5977 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental-20250929` - linux; riscv64

```console
$ docker pull debian@sha256:a1b8aed15ecbc25cb255d910d1b031e639d54cdbf37089288f22fad7e982faaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.7 MB (46681198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:574b76cadaa4310f24dbf048de2f561740e811018a85f6bc19e34374afd5f1c5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'unstable' '@1759104000'
# Mon, 29 Sep 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:4896a84f986a54e1b1410482cb14c14b79bad4d5764a0d23c342dc2b1db56b38`  
		Last Modified: Tue, 30 Sep 2025 01:07:35 GMT  
		Size: 46.7 MB (46680978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c34d87fb716daf97a23c75ea9655f5b4c9fb6f26601ff9847d1ab54b0f8d3f7b`  
		Last Modified: Tue, 30 Sep 2025 01:31:05 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental-20250929` - unknown; unknown

```console
$ docker pull debian@sha256:c8c93abae45220da5d4f287b9e4e3263f9c1d462694a6201ef1551cabd5014e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3126136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46c56a0f2e96b1b7ebbd4cf3e70b8d57eeacdcc0f045800eb7beca4d757ba443`

```dockerfile
```

-	Layers:
	-	`sha256:faec2b95684df49e79f140b13ae661e84e67cdc73051f3d49f40b07b0aa94661`  
		Last Modified: Tue, 30 Sep 2025 06:32:59 GMT  
		Size: 3.1 MB (3119960 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1e6ed884cf3a02d3b125636d798505e644cd487735bad800715ebfd9f8136a5`  
		Last Modified: Tue, 30 Sep 2025 06:32:59 GMT  
		Size: 6.2 KB (6176 bytes)  
		MIME: application/vnd.in-toto+json
