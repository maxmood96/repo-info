## `debian:forky-backports`

```console
$ docker pull debian@sha256:7c3df866484cd4e88e2cb9dc47a626b41f4215d06eae06fa435a948462b54c28
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

### `debian:forky-backports` - linux; amd64

```console
$ docker pull debian@sha256:13b23b107658485d66a0bbcc62397243dfb2e39adfaa3b1c77bb9f8695d33b29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49575258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba05d9fc60f3abc7f1dcb9adda86e16d4066cf7a638ad6db840ae17045b4f6fd`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1757289600'
# Mon, 08 Sep 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:92b4a1a651b0c3628297f7472014e3ecb5580ebbd73dd0616ae4e5d399ff0831`  
		Last Modified: Mon, 08 Sep 2025 21:12:37 GMT  
		Size: 49.6 MB (49575035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b2aea742f396ebb88d278d2eaad024001fc4c94b364c30d4d7bd4e9f5aaf44f`  
		Last Modified: Mon, 08 Sep 2025 22:15:44 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:ce848bbd8565430ab21c675501a8f82b2399de04110135709fb35566f9a9b8eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3176575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef35832649c6f9c6bb6344e46808baef36d2c7fe030d40ffc37bd29856bf857e`

```dockerfile
```

-	Layers:
	-	`sha256:072190e6707abe09a88be7891af61b7c1eefb40d29626a93bfb635cfa7966264`  
		Last Modified: Tue, 09 Sep 2025 00:25:06 GMT  
		Size: 3.2 MB (3170755 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b93b311646627dd26f198f677bbe3bd4f9c67b1cf3a8db7af35eeafb9c6898d2`  
		Last Modified: Tue, 09 Sep 2025 00:25:07 GMT  
		Size: 5.8 KB (5820 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:forky-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:941e7c7fe985b48ada5a361787b8d14c52a0135a596b5c6440cca5af4ad0ac21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45943444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d13a6f75d9560884d4859c23264785f1016dc42376034598aa1041402ab03174`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'forky' '@1757289600'
# Mon, 08 Sep 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:37213742d2f58ba09fd9f68c8a57d0aed21f04fbd865207a40734ff3e6e7a8c6`  
		Last Modified: Mon, 08 Sep 2025 21:14:40 GMT  
		Size: 45.9 MB (45943220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb186f1a7cbc17e9da5e9e1a76412c6910fb0926a4154ffad5918ef0189ab5e6`  
		Last Modified: Mon, 08 Sep 2025 21:54:51 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:d8f251922ae9008ed2e28f94419e43cd7055d3cca66a5ddf4948a6193ecd38c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3178005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8858d881a449068aad61174ca6ef958158a025fe76a7f147d6d4e8c5420a1339`

```dockerfile
```

-	Layers:
	-	`sha256:a540ead0d65199e0b8dee73b7a26730529d6a45018663c94ee0a6c29916af70a`  
		Last Modified: Tue, 09 Sep 2025 00:25:12 GMT  
		Size: 3.2 MB (3172129 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:557d91bd618feccbfdf0494289c4a164bc9ded29e2232169b6c1b8cedb8242dc`  
		Last Modified: Tue, 09 Sep 2025 00:25:13 GMT  
		Size: 5.9 KB (5876 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:forky-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:ce5ba8a11cd869f32b2ab18e26c5098f0d506bc3b947f9c008d4a23045106782
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.9 MB (49863719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d677810d171e68754bded2d9dec5cd3ba23523b2ac2983d2af6838a8ff442bf`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1757289600'
# Mon, 08 Sep 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:43c9f83b4c0cbba0c49dce5bbb999963ed78f9198001feb88e7464916cedc070`  
		Last Modified: Mon, 08 Sep 2025 21:14:38 GMT  
		Size: 49.9 MB (49863496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3f1d56054cdfe7adfa33ce323a116296d382d770333d145b7f52533899aa2e1`  
		Last Modified: Mon, 08 Sep 2025 22:01:45 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:6c044b7aa567bae99548922972d8d32cee832f3a9778e7a5e7ef969955bb80ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3178125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45576535a0a83d115bdb7314f73bdac1e139437dd3ab9ea4ed0f42a460a3c0d4`

```dockerfile
```

-	Layers:
	-	`sha256:eef3fce2dab14cae59c542c316e64fb8f4442b8ffee115386fa1f9a8e04e231e`  
		Last Modified: Tue, 09 Sep 2025 00:25:18 GMT  
		Size: 3.2 MB (3172236 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e067c0fda39401b2045d4853a0baf7c8894f80c432449f8c109688a55c4eb9c`  
		Last Modified: Tue, 09 Sep 2025 00:25:19 GMT  
		Size: 5.9 KB (5889 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:forky-backports` - linux; 386

```console
$ docker pull debian@sha256:960169267144a63601a60aa9015433d2841f31f30e8f84c22ce9bc5a98447970
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51050033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01b60bbb8d1a9efb7a443442af3bc1103c1d6418283e20f7848cffd2e439a6d6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1757289600'
# Mon, 08 Sep 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:e46ba83d4247b0505c7b4e05b89ae8056e10eb07f4e445e17e2dc44b8c60b063`  
		Last Modified: Mon, 08 Sep 2025 21:12:21 GMT  
		Size: 51.0 MB (51049810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f1f1096354ad2648e31c84464d2fe25c2ecb59bbcc7e55c8330b5baa17caa56`  
		Last Modified: Mon, 08 Sep 2025 21:52:48 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:7a1563f6932a9d74b336da3650318704047281d56efe50feaefe669b5fbdb31d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3173763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22c0b71f007962f16d75bafefc6e1f2fe95b40286b2a89eedbefca3114e3c4c9`

```dockerfile
```

-	Layers:
	-	`sha256:73e466959f15884b1aab7252cb68a1e94cdabcf435feb25dafaff5150664eb8f`  
		Last Modified: Tue, 09 Sep 2025 00:25:23 GMT  
		Size: 3.2 MB (3167959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddca23fed74e3cbe4e685eb04c5aa00576619959cd2c014fa87c0776b6665a62`  
		Last Modified: Tue, 09 Sep 2025 00:25:24 GMT  
		Size: 5.8 KB (5804 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:forky-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:3c4ff0b3b84882f88eba08e59dd03bec49c116608a58068aacc6769e3c526144
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.4 MB (53391921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90a8850f5ba8c21d16c4f51df78a91db81d49bc468f53ff0a505c263484013b6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'forky' '@1757289600'
# Mon, 08 Sep 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:e4e4a2bdd2295cd2a4f3315805533676c7f12dc54b360ff3c285c5614051d45d`  
		Last Modified: Tue, 09 Sep 2025 02:16:14 GMT  
		Size: 53.4 MB (53391698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fec2d8ac06ab057cd3d0694f08a976aa731dea7b88178e715e4786b435880827`  
		Last Modified: Mon, 08 Sep 2025 21:58:36 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:feee76e19bd91f9bebffa9a7089ed06144089c26733adace51e510e1cba379bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3180111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33198e597ebfe837264dfe3295f3906e1478e0efe7aa9377ae3e777c709499d9`

```dockerfile
```

-	Layers:
	-	`sha256:a017c8db94c2969840298839f015b599906525630943833ade835991ce1446cf`  
		Last Modified: Tue, 09 Sep 2025 00:25:29 GMT  
		Size: 3.2 MB (3174264 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f64ef89bc84e9c60ed0f0439e2082523341c356b6f9bc3646007cfebc384d3a4`  
		Last Modified: Tue, 09 Sep 2025 00:25:30 GMT  
		Size: 5.8 KB (5847 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:forky-backports` - linux; riscv64

```console
$ docker pull debian@sha256:7e1057262bb858b6e42051682bfd6b2a473d31d3771f917b357e5afd712090d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (47991106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ec35599b0643e0df455e62df0739d305afc27dec957b2f27dd58320c7deca6b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'forky' '@1757289600'
# Mon, 08 Sep 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:b69968429eb7c4ddc55330629f921afc4125b1edb6cd3eb02edfe67c09cb248f`  
		Last Modified: Mon, 08 Sep 2025 22:03:44 GMT  
		Size: 48.0 MB (47990884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:181fa79b752f94a95979ccd007cabb94fecac472f3f0271ba7fc2118658572c0`  
		Last Modified: Mon, 08 Sep 2025 21:59:38 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:061853811eb3a66d2abfbeee30d0d4dbbd6ea17755ea07b383627d97fa449fb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3168913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f51de7266fa9b8cb94f21e22250a806650736a99954c544ce675d2fd6166eb39`

```dockerfile
```

-	Layers:
	-	`sha256:c1af402d295548d8fc47925fa94aae6bcd25da6224ecf5e805e6bcdb4280cb9e`  
		Last Modified: Tue, 09 Sep 2025 00:25:35 GMT  
		Size: 3.2 MB (3163066 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88be3c7a4710ff9dae4be3c21d0f144ae2077c2eeb715c2c9def73aa7e5faa83`  
		Last Modified: Tue, 09 Sep 2025 00:25:36 GMT  
		Size: 5.8 KB (5847 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:forky-backports` - linux; s390x

```console
$ docker pull debian@sha256:f263702783a95aba89f4112be634c34e73365fcd171471dd2406f4497308f610
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49583405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db58162762d18965e2405d0ce8cbcf83b8914a4b3adaddc3c0a8201773cb7441`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'forky' '@1757289600'
# Mon, 08 Sep 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:d70c4639b1bb56ca2bfa88a8dedfb6d14d5f6a857613b672fef601229bcd766f`  
		Last Modified: Tue, 09 Sep 2025 10:20:05 GMT  
		Size: 49.6 MB (49583182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09cb8312de69639c432b68549367b93a08169c7270fba65b8214dadc239081f7`  
		Last Modified: Mon, 08 Sep 2025 21:58:44 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:08d89eeaa2c3746040adb7b960c20efec5affaf3e2633a3efbad409d82540b80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3178022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cc7e310325f6bd6bcb02811e8e9109ae038d4d54df45967b9a3af464c7d956e`

```dockerfile
```

-	Layers:
	-	`sha256:a56e1601e183514ba20674d2f30bbfa6297128215b5ba2c66c586fe28466db77`  
		Last Modified: Tue, 09 Sep 2025 00:25:41 GMT  
		Size: 3.2 MB (3172202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:219ec4879fc4a1af6e8206a857bdd369afff6cba60881da56751dd4517915af6`  
		Last Modified: Tue, 09 Sep 2025 00:25:42 GMT  
		Size: 5.8 KB (5820 bytes)  
		MIME: application/vnd.in-toto+json
