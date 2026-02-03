## `buildpack-deps:unstable-curl`

```console
$ docker pull buildpack-deps@sha256:aa95c042970383b41cfb941127e6a48fa1c967e871bfc4385a65aa32927959a8
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
$ docker pull buildpack-deps@sha256:058997fc85e08e5d1ecdd9b15f230c63f29c2699c7097612e63d72faef4ff8a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75880819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cb59c1e7b53870c496f4bbbacd038ba73caf4aa9242460ac46ee7cd2ff5cb6f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1769990400'
# Tue, 03 Feb 2026 02:42:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e5dc831051d738f5c1db4254dde56feb7c9e75e136e23995d896f1b6e1ba752f`  
		Last Modified: Tue, 03 Feb 2026 01:15:47 GMT  
		Size: 48.7 MB (48654703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7215d01a65c1956de10f370e9c70556dc553159f6db5154f95cf3f4792912cc`  
		Last Modified: Tue, 03 Feb 2026 02:43:08 GMT  
		Size: 27.2 MB (27226116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:445d9597d3492dbc7608a69f67a419bac209655f02e7993725e8e6d8ff93ca4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4136946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc204aa30611f82461ac3dfec5ae4a8bcdb29670ab19f3d75aeee71eef5cd440`

```dockerfile
```

-	Layers:
	-	`sha256:57b732576ea84c995e92599beb0731e76199e53e4192b8a7ebe464e527f372a0`  
		Last Modified: Tue, 03 Feb 2026 02:43:07 GMT  
		Size: 4.1 MB (4130185 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21b1564573094c103a4428d42a6c165175e92fb6c6a18377857a8ad4e2892f9a`  
		Last Modified: Tue, 03 Feb 2026 02:43:07 GMT  
		Size: 6.8 KB (6761 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:7967103d176625c3a543011976cfcbbf6cf142b1ce572ef4e999ce98de43e979
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (70027078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e6cb3fec0e7ab90137eba73184e99c179d01dd302d4d500b9a8a7c7b4c6e365`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'sid' '@1768176000'
# Tue, 13 Jan 2026 02:58:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:8b7f582255e583d8176a24d49b58b25ef2ab11e30f1f26c271dc02b42befa1ec`  
		Last Modified: Tue, 13 Jan 2026 00:42:25 GMT  
		Size: 45.1 MB (45124955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f363fb6b9543f81f86efd0aecc6d9e12898921b7bd5ed58e85c04a1426057dd9`  
		Last Modified: Tue, 13 Jan 2026 02:58:25 GMT  
		Size: 24.9 MB (24902123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6b17c2a149937d82f5d6d8630b53a75563d8b2ce7b84c0602455ff0e6bff1621
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4122411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85d5f34b7769145a9bedc0892adc8dc1be51eccb658af5560a7410b6d41432c1`

```dockerfile
```

-	Layers:
	-	`sha256:1d3ae6ed7a776e2c49e6a37670219908d8f9eeb23803022aac297fb7c4e053d0`  
		Last Modified: Tue, 13 Jan 2026 02:58:24 GMT  
		Size: 4.1 MB (4115587 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f45da1c0e5b432120b875c0b22a52b98452e09910c39a048a10fb7b5bdfe2a95`  
		Last Modified: Tue, 13 Jan 2026 02:58:24 GMT  
		Size: 6.8 KB (6824 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:6a4cad6c54d5fdc67ca7f86bc99d2266e34369b83273585f36119b712f66a212
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75377442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dbe8457dee6e50f0194d44cdcf4d3f1b307ba2c30c4a616633cdfb13659cb4e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1768176000'
# Tue, 13 Jan 2026 02:14:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:6d947e77c03f512510d8bed1eff4f80727f54732f6ae212199524bdf89493609`  
		Last Modified: Tue, 13 Jan 2026 00:42:02 GMT  
		Size: 48.8 MB (48824718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23d83fa1af402d6122143d9e5834df76a1ce4536b0e53fa05dd6ae332f4c77b6`  
		Last Modified: Tue, 13 Jan 2026 02:15:03 GMT  
		Size: 26.6 MB (26552724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:93420b48cbfc249b51124d501d31421d656b365b663219555c043821d7221cb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4121825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bd540dd4023402b21a836cb8c008b62ec3c2168653b72aec3b9b274a9c359a9`

```dockerfile
```

-	Layers:
	-	`sha256:2e0c476488926d4087b162f0a8f9e95888f394afc45f56f485693d31819c23e2`  
		Last Modified: Tue, 13 Jan 2026 02:15:03 GMT  
		Size: 4.1 MB (4114984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b354444a9ce93fcad3c5c0795594dd8cdaa120f73f0a68d25f4a973f756b64c`  
		Last Modified: Tue, 13 Jan 2026 02:15:03 GMT  
		Size: 6.8 KB (6841 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:e384e2230154686142f53ca72493a18d49803169f475fe8afca5a2b2bd6547b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.4 MB (78418470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed78c757db10ddb1c7603df0201914cfe30eee9f205d652b4277aec6ff5ba40d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1768176000'
# Tue, 13 Jan 2026 02:02:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:621ee2827046628793df0c5176988fc0eef90eb94ab1b862f17e074ba6064e3d`  
		Last Modified: Tue, 13 Jan 2026 00:42:41 GMT  
		Size: 49.9 MB (49943816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82ebc798fc10f8015cd27d3c8885c010f05e57b86cddfc6e327bc7f746362b1e`  
		Last Modified: Tue, 13 Jan 2026 02:02:58 GMT  
		Size: 28.5 MB (28474654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:346e67b76f430cbcb1c8c5b35c41ab9101f6ba2a9aef7471241310bd04a26972
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4117944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec905e2f147f2cb763b076e4b3f304892c351d98540b72ed076f4d647dd1f5fd`

```dockerfile
```

-	Layers:
	-	`sha256:43ea74d05127301ebbef6d74988b833530d4508d106e09b8569fc9f5e34e798f`  
		Last Modified: Tue, 13 Jan 2026 02:02:57 GMT  
		Size: 4.1 MB (4111205 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f4b0cfec9b6e2424591b0ed8c10274cbcfb171d07c12a065c52c9d3fe60fc71`  
		Last Modified: Tue, 13 Jan 2026 02:02:57 GMT  
		Size: 6.7 KB (6739 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:8e7325351670868f59e836788769d4b945310451cd4d1a61a0d8c8727c55334b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.0 MB (82959327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38e9309b1670b1d151a5d688e77e80de2061e89c35c99e4f7ddf396ba7268980`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'sid' '@1768176000'
# Wed, 14 Jan 2026 00:58:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:3fc9cd4fe16c3d17cfa9014c31678a58aad75101c0db66189ea08efe999c1a84`  
		Last Modified: Tue, 13 Jan 2026 23:17:49 GMT  
		Size: 53.5 MB (53525434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a197399fa4447d8fa115804ab3b4e02dac8c91312a2de42315098f7ba5379933`  
		Last Modified: Wed, 14 Jan 2026 00:59:10 GMT  
		Size: 29.4 MB (29433893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c460d945c3e90cfef32e96d57ad0e69091e980eceb07e761d45941148148f42f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4124731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a450f58214d7be8b5fd332925d697a44822aaf2b398b538a91683bd7de21a0c0`

```dockerfile
```

-	Layers:
	-	`sha256:80a79e9d5eff48974fa8e9ef016132bcbd529ec7fb97c8e2d550416aea98197c`  
		Last Modified: Wed, 14 Jan 2026 00:59:10 GMT  
		Size: 4.1 MB (4117938 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:238e539ccca31ba27c3f6f69ea1a285eecc588f19fcecebb7a3a9f9fd1275f1c`  
		Last Modified: Wed, 14 Jan 2026 00:59:09 GMT  
		Size: 6.8 KB (6793 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:13175392da6a3a9c8dd4577e73ea51664db1f26abcd7dcaf13ef3b64ca3d8f84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.6 MB (73596037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a42e59fa05e2ab3bf7545722004bbbfe43fa8f3e8c6327667e3b7428b2ca6b6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1768176000'
# Fri, 16 Jan 2026 06:44:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:3f1a05ef5786076b47fcd681b3f4ff2ab26c932b463a6ab7c885cf7684b1355a`  
		Last Modified: Tue, 13 Jan 2026 00:55:56 GMT  
		Size: 46.9 MB (46856753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2839eb91239c64d14daceac3c851cd6aded1a2915fa193b50025c045cf501598`  
		Last Modified: Fri, 16 Jan 2026 06:45:41 GMT  
		Size: 26.7 MB (26739284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:281f3df94de125a7d6ea37b2d0352da590c45c86dfa819cc1b7d9cab78a67f50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4112566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7fa41d37633ad8cc11fdf06b05c5f1c250378af7119b5b8bb4c09b0bf709b12`

```dockerfile
```

-	Layers:
	-	`sha256:99a207a91a3ce372d3008711036e005a7d6e1a2bfc5f66ddba5ce8e099cb5f0a`  
		Last Modified: Fri, 16 Jan 2026 06:45:38 GMT  
		Size: 4.1 MB (4105773 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e20a036e05bf60ff268c23de6755cb85cc8d54c685cb36e18ffc1fcc24871850`  
		Last Modified: Fri, 16 Jan 2026 06:45:37 GMT  
		Size: 6.8 KB (6793 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:c532d734f7e844c56d0c6e6f5d53acb790432e66fadee6fbe8d7a978af03566b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75420929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:378396a9415899ad961de5438c029b55a6a4b8bf1df6a33f841fc0bb67fba1d2`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'sid' '@1769990400'
# Tue, 03 Feb 2026 03:45:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:3bfb68c2648b1088debcce6bc605d7ea6709b6f129c9ce647bf0a7c385d8350b`  
		Last Modified: Tue, 03 Feb 2026 01:13:18 GMT  
		Size: 48.4 MB (48421195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bd1e07a5a5c7ee531c5adb5cc340d101adfb8e3eab835cd2272f521de25591b`  
		Last Modified: Tue, 03 Feb 2026 03:45:17 GMT  
		Size: 27.0 MB (26999734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:46286f97eba09e863a0ccec9f17a649047ac7f17e491ef752ed7057684c42f9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4138354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c5cb175477d1fc2aba2b8934c1505a564b15c1566ea121aff9c199fa46e53c6`

```dockerfile
```

-	Layers:
	-	`sha256:7ba9aa61d7cfa2f1f0ae0c0332283150ddb2a7586b55423df8b5edcb27b0bd03`  
		Last Modified: Tue, 03 Feb 2026 03:45:17 GMT  
		Size: 4.1 MB (4131594 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d2144c3bc71583a20e050158472bd6d8259abb35cd26e573d75b406334b1ca1`  
		Last Modified: Tue, 03 Feb 2026 03:45:17 GMT  
		Size: 6.8 KB (6760 bytes)  
		MIME: application/vnd.in-toto+json
