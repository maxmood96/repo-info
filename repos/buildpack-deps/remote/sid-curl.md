## `buildpack-deps:sid-curl`

```console
$ docker pull buildpack-deps@sha256:ee29a3a2455b725daebc251785e8bb4d77c4c6b7abe7da9e2d0debaa3979696f
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

### `buildpack-deps:sid-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:283ed630da5a487390d1f83a93915bdb8a881a4d90328bb0d3d0789c830c800a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75930659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:744ca6c03ea9a34bdf6c699a8d28b3164702cacd5d7e2ca76ef6cd4099b2bbc2`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1771804800'
# Tue, 24 Feb 2026 19:19:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:d8aecb4bc7b9e58c615fe5a04f51a5710114ff668af7b4f56dd368d492375e7d`  
		Last Modified: Tue, 24 Feb 2026 18:43:47 GMT  
		Size: 48.7 MB (48666927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a5a3b9aa5dd67fed7efa597566954b806b6c17ff4757052490684a87ba9c100`  
		Last Modified: Tue, 24 Feb 2026 19:20:08 GMT  
		Size: 27.3 MB (27263732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1787b6e53ef92315a34964bb9644f0b6a314fc924d9dd7a8f943d32b437f14f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4130742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c097ccbeaaa34a7b371362ad436d8ad43ab8cf672d616afdd6c07ff37ee57354`

```dockerfile
```

-	Layers:
	-	`sha256:d6b65ec028ae414c853c228194d046e8d02f8cb9ff833bc08318ce12ae80f586`  
		Last Modified: Tue, 24 Feb 2026 19:20:08 GMT  
		Size: 4.1 MB (4123981 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6413b0e71b9eac2a557f4a8c01f84baeb3f0c8b55b54031ec3e85ea657517ee`  
		Last Modified: Tue, 24 Feb 2026 19:20:07 GMT  
		Size: 6.8 KB (6761 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:c17dbf8b6dea5906aebc86e5c914a109bcb848824c072716eed3ddef89084093
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.6 MB (70606201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8004339037f260c5541f6950bebfb31f02f2b68a85f9b07730b0a37522c42fc`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'sid' '@1771804800'
# Tue, 24 Feb 2026 20:04:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:97ecb7dc5149349428e562613e6adb43b3de4d352c854673428e628da358370f`  
		Last Modified: Tue, 24 Feb 2026 18:42:32 GMT  
		Size: 45.7 MB (45650224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09e80713e8851bb16d17addabd13dbf94a64b8f2f71fc35c153fe3f3d905e74e`  
		Last Modified: Tue, 24 Feb 2026 20:04:46 GMT  
		Size: 25.0 MB (24955977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b9e1421e61febbf7b93c8d24060f0f3297d8f8359b16ad6916a12cc33fd393fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4132302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77bdc333bdb8ae414cf4af75b188931a5392b588cbfb585cfd550a94693ca59c`

```dockerfile
```

-	Layers:
	-	`sha256:b0acba6f216c2d7073a9fabdb403178f893913a0f78cd90b8c9ddc23acdc6021`  
		Last Modified: Tue, 24 Feb 2026 20:04:46 GMT  
		Size: 4.1 MB (4125477 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:777db458a3802ba0167a230d8db9166411828bcad7f1b3cc9e068d4a28a49593`  
		Last Modified: Tue, 24 Feb 2026 20:04:45 GMT  
		Size: 6.8 KB (6825 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:15e8974db5422b5ca2eaa12bfaba1725a5a58cf8170e3c7f48d8e93e6f4487f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.3 MB (75267003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7e35cfe3e2429574d699964a3351f9f265421a017c1a562f07d9423c48bd4fc`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1771804800'
# Tue, 24 Feb 2026 19:24:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:61a95a2f6784ce634817550699b53ea6f85b093ca9ec55f99c5217b534acfb51`  
		Last Modified: Tue, 24 Feb 2026 18:42:36 GMT  
		Size: 48.7 MB (48709262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9febf2eebdcd541e5079a4d79c0089d659ae0df279b4c59ab388cf9f3a36d6a`  
		Last Modified: Tue, 24 Feb 2026 19:24:43 GMT  
		Size: 26.6 MB (26557741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:edeaab12d82ee1881b657158f0865bef3e47fac72c37b2e1fede6093eca9ea7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4139740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c4a5580edeac5c416bd65f39450a8e5f87b0ba51209842622f37aa22765a61c`

```dockerfile
```

-	Layers:
	-	`sha256:4786578ee9534f899faacf7a3fe0f555aa603223ad304b921e3cb57f7c52054f`  
		Last Modified: Tue, 24 Feb 2026 19:24:43 GMT  
		Size: 4.1 MB (4132899 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50f14d6be62b0f1ee3fd36dc7d04bf43d46d59e166bd74fef93d7dd98f08064b`  
		Last Modified: Tue, 24 Feb 2026 19:24:42 GMT  
		Size: 6.8 KB (6841 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:e4cc4ef66f2f1c24a87ccc306c316f4eab0e97386f850db61810599a9b620405
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.5 MB (78544561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5bcbfde0aa91c1cac9aedd8dc9ab9793a126e1e014966e8a48939cd80aebf59`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1771804800'
# Tue, 24 Feb 2026 19:24:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:def456773a4aeca49d4b978ec8b12f148f201cb7cf9c2174e05e9ced13435b6d`  
		Last Modified: Tue, 24 Feb 2026 18:42:59 GMT  
		Size: 50.0 MB (50022115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3559a7084ebe893d133871358dab0d079615e3eaacd04f900b699ede2f39f35d`  
		Last Modified: Tue, 24 Feb 2026 19:25:03 GMT  
		Size: 28.5 MB (28522446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1f9603c00f5bcc5f75b79403dd6ebf7663fbf8c3424856326c0c09e9227bd853
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4127820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:287795a55dc2ee2098e534b335d490307a80db9166fa9ff8e57dd05f9820824e`

```dockerfile
```

-	Layers:
	-	`sha256:9c07d85a8b6448b3b92fc057f097bd34ef7e91a4c48e92bf0d6921578908aaa0`  
		Last Modified: Tue, 24 Feb 2026 19:25:02 GMT  
		Size: 4.1 MB (4121081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1aa122251b251469f0455a3651cf45ebb2eb9cb21b27f4c2fc438399a736d4b3`  
		Last Modified: Tue, 24 Feb 2026 19:25:02 GMT  
		Size: 6.7 KB (6739 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:820c40589769232c721e4ff63828eb6e69904194d764fac09c3c3c9ff0acd6da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.2 MB (83218578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f649895638300b2ddd04c309e0940997f8bed273485988768a0f9ff5756075ab`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'sid' '@1771804800'
# Tue, 24 Feb 2026 21:21:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:98cf99f8e5f75111e243f4d3c092140d6c7618c5cce72eba92c5c2c4d8f97f2a`  
		Last Modified: Tue, 24 Feb 2026 18:43:36 GMT  
		Size: 53.7 MB (53670202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91c9c8da854a9fd9a96b0f203229509ae404e6f58b91c885234945a59771f957`  
		Last Modified: Tue, 24 Feb 2026 21:22:11 GMT  
		Size: 29.5 MB (29548376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:17f8aef41cb08316602a527774f261a5afd0805e40bd60f93fc239d3bbe3e089
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4134649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ab3150a32c194aaf60537454bad0faa84d1633b4d4f8978ac0dc7e8009ccb8a`

```dockerfile
```

-	Layers:
	-	`sha256:3f56b00fd40839c9deffc52b5240bd0917de28f3f4a590e9fd8f0b442a5b1d2b`  
		Last Modified: Tue, 24 Feb 2026 21:22:11 GMT  
		Size: 4.1 MB (4127856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9e3ca729cb83d6bfe72cf97b3453d380d07373e88c4e9c32606b87b928e5bda`  
		Last Modified: Tue, 24 Feb 2026 21:22:10 GMT  
		Size: 6.8 KB (6793 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:59cb1525940b3963768ce52a1cb788be6d354d45e149d105f1310a67073d3102
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.7 MB (73716271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1110561a43501db640decd8fa317a29eb52a7fa1e8873df88438a1271b762d7f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1771804800'
# Thu, 26 Feb 2026 21:40:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:8883acc64dfc3047a79b0cc247a530d5064df45ee191c83ce50326e6f5321005`  
		Last Modified: Tue, 24 Feb 2026 18:46:58 GMT  
		Size: 46.9 MB (46910148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:117b9883d58655e16546eb41ce58204eed0527238cddce201073b9d732ba7588`  
		Last Modified: Thu, 26 Feb 2026 21:41:52 GMT  
		Size: 26.8 MB (26806123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8537059217f174ae166d2f3227032a2ca859f90dccc79601c91e0f3ffe074044
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4122484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58d990b8129c405642e837ed7c00f880f281e665863946dcadbab11e967a7929`

```dockerfile
```

-	Layers:
	-	`sha256:763bb63661baca293202a91155d824d5eb280e1b103b42632544ac4b63282a83`  
		Last Modified: Thu, 26 Feb 2026 21:41:48 GMT  
		Size: 4.1 MB (4115691 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:022067c2e75c60854c172a972c5bb43e5ee188c84b2f729d59cb14a119742027`  
		Last Modified: Thu, 26 Feb 2026 21:41:47 GMT  
		Size: 6.8 KB (6793 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:f43d85e73f6ec029ea6b4d484ead89b6f4bf536633f9ec7ee06744f950777a9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75497831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a74f114769cdf6bcdc02f7b513a410a6de38fe6921520edd07e94edbf848b080`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'sid' '@1771804800'
# Tue, 24 Feb 2026 20:57:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:b79b6ca78edd108b2b500a1c2abe8a5f5b6dee5dce46c5bd663b643e7c568362`  
		Last Modified: Tue, 24 Feb 2026 18:42:12 GMT  
		Size: 48.4 MB (48447710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:694122fd04e83fa7d8372df97237755c6e7de35a0f627724e622c594e1610bc1`  
		Last Modified: Tue, 24 Feb 2026 20:58:22 GMT  
		Size: 27.1 MB (27050121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9a5e1f920730f165fd889d405c384cbebdc5f03b6378e401bae5bb3f69cd1435
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4132150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a4d18fbec994aed316f64df6e6e6bbcf7bb5ffa540440ebab8ea3b6c14dcc1c`

```dockerfile
```

-	Layers:
	-	`sha256:95f975649d9871890b84930c3ef64b462b47c1057f5c8ddfcf66636fdfab45fd`  
		Last Modified: Tue, 24 Feb 2026 20:58:22 GMT  
		Size: 4.1 MB (4125390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82b7eb85000f15cef803d0ff3acc4924a23150e7d955026c2320e0aabf9dca3f`  
		Last Modified: Tue, 24 Feb 2026 20:58:22 GMT  
		Size: 6.8 KB (6760 bytes)  
		MIME: application/vnd.in-toto+json
