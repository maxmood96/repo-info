## `buildpack-deps:unstable-curl`

```console
$ docker pull buildpack-deps@sha256:7a283624f6a77601807336cd36f2ea7b9da03b06a75569787e55bbab6f256b91
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

### `buildpack-deps:unstable-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:4b3fc430baaca0553cca036f4c131c9a46ff947c7563acfceb67700f2f2c6cba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.6 MB (75570335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42c61dbadafad4dcc5deb1d3c156eb3690427d73f90a60a9fd08dbe8759a35a5`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1760918400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:767319f7ad72179f876946bf5b239f862d2d5ad761041b6e449acd3ce4c0bdde`  
		Last Modified: Tue, 21 Oct 2025 00:19:58 GMT  
		Size: 48.4 MB (48383307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0041865733f8eac4afbcf0e7351d1bf685e1d3b536723ebe09dcc7b7f34ad22f`  
		Last Modified: Tue, 21 Oct 2025 01:42:32 GMT  
		Size: 27.2 MB (27187028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c9231fe98928dae6b97894ddb8c5d6255a770e78c59bc6f3aedd010eb5f0c259
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4103683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:828cef8089209255b2dd84cdec096ee9701f61f4d0b588abd59ecfd41213302a`

```dockerfile
```

-	Layers:
	-	`sha256:700c25de9c3e523ab6bc9ddaf73d6dc2c8655af427ffa30ce6b9df6ff4dbee72`  
		Last Modified: Tue, 21 Oct 2025 10:22:15 GMT  
		Size: 4.1 MB (4096879 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f9cc81f9093a685676a4d9acb5ba224c26c49082187f926c2e43d5722ced1aa`  
		Last Modified: Tue, 21 Oct 2025 10:22:15 GMT  
		Size: 6.8 KB (6804 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:068db1fec5489c9944f06e7282d0cd1a056d3f97e9097dd1b42c53b4b40b6abc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.4 MB (72377971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3623360c6066dbe48c1fe5ea95814b380920f3b83d163eb85ade09f6cf1e63e6`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armel' out/ 'sid' '@1760918400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:204bc56c72452e737a2bccff3f4208682016048e825d5ac2bc52dc2c4d4649de`  
		Last Modified: Tue, 21 Oct 2025 00:20:34 GMT  
		Size: 46.6 MB (46593513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe3882f8d4f2701b8365480052f7e556ff8fd1101d8f1b72e8141c4360f1d695`  
		Last Modified: Tue, 21 Oct 2025 02:32:18 GMT  
		Size: 25.8 MB (25784458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a5eda31f68b8c2584e427f3fac9d361ba54579a99ef63371f4543583e3321285
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4106747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36b9870e6b12b9b69f115e2b11b128621776503ce95022bf1effafaa1d7c3c46`

```dockerfile
```

-	Layers:
	-	`sha256:48751e168c8b062053375e9cfde0774df682cb652b1b19b8c5a1772e667f8cae`  
		Last Modified: Tue, 21 Oct 2025 07:21:27 GMT  
		Size: 4.1 MB (4099879 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:659218159764db9e5bac6f2694772f0710f433e7bb76be9e8f40ecec836e6d18`  
		Last Modified: Tue, 21 Oct 2025 07:21:28 GMT  
		Size: 6.9 KB (6868 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:df25dc4bb17428df8fa2c56ba3858d6402249d9f1e62893eff4ded021b5c2736
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.8 MB (69833595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1376150b70c5a90c6cdbe2be2bb3f06a569479bef192ce15f2d60e47536989c9`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armhf' out/ 'sid' '@1760918400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:d46bd548fc78deefe00dfcd2b559377066496f2d6beb8d1543970d5a2164151e`  
		Last Modified: Tue, 21 Oct 2025 00:20:45 GMT  
		Size: 44.9 MB (44911556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6ca5d6a8872c7e1682c82eee718887aef134a416249261516f2ddbf348e5bb1`  
		Last Modified: Tue, 21 Oct 2025 02:45:21 GMT  
		Size: 24.9 MB (24922039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ea6a0f5b2553d7eccce7a3a28e00ab17ad69663d572a93137f3190a95b90a7ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4105243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5354c17408f28a041cc4a3154dfa50051145221883ed7a0534006d7c46bc3e2`

```dockerfile
```

-	Layers:
	-	`sha256:c35b2f2d9ed802624b1ed39860bc7e0997c6a74eeeeeb7928f49cad5af2e2453`  
		Last Modified: Tue, 21 Oct 2025 07:21:33 GMT  
		Size: 4.1 MB (4098375 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe42d786884a0b21a4f5df414fbd57b5931d30c58fd465baac5313836ee2306d`  
		Last Modified: Tue, 21 Oct 2025 07:21:33 GMT  
		Size: 6.9 KB (6868 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:5f0d6f8b7ced2af4b856ff1ad8312e56ef2ac5f6f132fb5827dc444eb0f63fff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.0 MB (75002492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b4184d756f28bdecd4c6288828612bde291ba0617c4de16d7ec62e39beca329`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1760918400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e43e2837b589215836966b2f88d71f57e2c4d5e8f8cb435d19f6ca010856531d`  
		Last Modified: Tue, 21 Oct 2025 00:21:19 GMT  
		Size: 48.5 MB (48506031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18d1d3885aec81341d6c3f13d004d1c421d5225a47b5dd56191da09737f82f78`  
		Last Modified: Tue, 21 Oct 2025 01:46:53 GMT  
		Size: 26.5 MB (26496461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:74df3fccefc45fa9faf825515b27fb40749ad6ffc34e57f7c3032f81c01b7230
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4104656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1da0025234a45902a6848eca7a21bc486669b0ac54039c64eee80c0fc52347b8`

```dockerfile
```

-	Layers:
	-	`sha256:617b71e2bea76daa2fcc9f4b4f4e5cf233bc737d7377ca1b6fcb87e1191ccccc`  
		Last Modified: Tue, 21 Oct 2025 10:22:25 GMT  
		Size: 4.1 MB (4097772 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b97909283a9aec5221c03c1dff59f86b8b4c6cc5d9f891b33edb3a77aa5ba79`  
		Last Modified: Tue, 21 Oct 2025 10:22:26 GMT  
		Size: 6.9 KB (6884 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:da7288ecfc54bb69f32586d359f77cb64b8363ff529de594b3483162753f9aea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.1 MB (78145801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3e832c4e7f9d6c5d131916809d06b045c6050eaad2f8f41afa4419f098c57d5`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1760918400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:c10cb3338a430a2ff28907bb8e87eec0d18b9eda310d3dbee0b9f6e1108bcaaa`  
		Last Modified: Tue, 21 Oct 2025 00:21:24 GMT  
		Size: 49.7 MB (49718167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fda6499db2a9a6f591335665b50167bb19c3bb91ebb991c34e464fc868a2cca0`  
		Last Modified: Tue, 21 Oct 2025 01:53:31 GMT  
		Size: 28.4 MB (28427634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ed9a5f260bc0be4a78de2ddefb745ec751d3cecabe751d95af1cdd67e3c16d96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4100780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9349671994e7445339ccc53337c58cc2fa4ceadb20c58624a4a4781a62462bea`

```dockerfile
```

-	Layers:
	-	`sha256:6cdcdc298e81f1562ddeb4f3831eb8a7ded451d1832196c5584f7a04dd2ad3e7`  
		Last Modified: Tue, 21 Oct 2025 10:22:30 GMT  
		Size: 4.1 MB (4093998 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c102de3f98680637093e802983a53df670b5e706a29abb4a455b09f66a9f1d5`  
		Last Modified: Tue, 21 Oct 2025 10:22:31 GMT  
		Size: 6.8 KB (6782 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:de97936871e93ce92b5e3e1dde0d5be94b1e943aeee4e714871f2855487cd450
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.7 MB (75723632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c589136d6397a3f111c9a0443365528f5245b47f338d20e64f280318ba56a96`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'mips64el' out/ 'sid' '@1760918400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:6dd82e8f3bb693d3ab0a24c9bfd56d40d1be2ec87a80a565bb29ebde51d7a8a9`  
		Last Modified: Tue, 21 Oct 2025 00:21:36 GMT  
		Size: 48.6 MB (48586528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09ece089fc78cd5e3356fd704455c8030636434bdf37dbc15a1b8e5f08d992f0`  
		Last Modified: Tue, 21 Oct 2025 17:28:53 GMT  
		Size: 27.1 MB (27137104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9cd388fbeb9bbccd8685767221c2b0fcdceb37efc44a4fcad17db4e12b035cd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 KB (6637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ada5a4ddae984b1b771af52145b2c967b05a17c1c058a81c315134d744036b11`

```dockerfile
```

-	Layers:
	-	`sha256:3ef99bea6360afe09cd28fefb0abaa579885f991c4ab83b0c08ab79b2df8ff5d`  
		Last Modified: Tue, 21 Oct 2025 19:20:41 GMT  
		Size: 6.6 KB (6637 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:e99dd0dd638c4788320db056ca139d5e09b6426a6036432065f1dd2bb3da7b69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.0 MB (81957633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41aa828b81bb7b9b11c75a2b4da74a1729f14b8d913f561dbf3b47ac7b9a2a74`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'sid' '@1760918400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:573dcf794048f7c1a04d7e5caace5a2fd1f7290004272bc4f3dfd960a096f8a9`  
		Last Modified: Tue, 21 Oct 2025 00:23:18 GMT  
		Size: 53.2 MB (53217563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4d66ae6d7a7d4ee86e6e6ff963fcaf8df404ad10cfa1d1fd6e312e128f220b4`  
		Last Modified: Tue, 21 Oct 2025 07:45:26 GMT  
		Size: 28.7 MB (28740070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1e511c058b0b370c4a62329904b9c7bd3297c8d3c59ba52e3076c0e75f32ff6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4107548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1ceb53cf51de1c1cc152337bac2b43d40455fd89cccfe9eb65607b4a31e88fb`

```dockerfile
```

-	Layers:
	-	`sha256:64d7356ed63440c591fccef0b73a849db914276828577ba4a381de52532cab24`  
		Last Modified: Tue, 21 Oct 2025 10:22:36 GMT  
		Size: 4.1 MB (4100712 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebadafb3b7a38542fd142c6b915ca4a7aba7b838731cdbd4f2587f63b524b63e`  
		Last Modified: Tue, 21 Oct 2025 10:22:37 GMT  
		Size: 6.8 KB (6836 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:d4e2e40c89e88a921a07200052f9fa01a11a2d52d74c1490fdfd6b8315bc731c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.0 MB (76015828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:759cd6ae890199fb8040deacc6e298266d44922211bc3a42c8304255d4646fa6`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1759104000'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5296fd171b043d9adeac427b668a2c333e09261704a2befe2a2593421c6da9fd`  
		Last Modified: Tue, 30 Sep 2025 00:53:09 GMT  
		Size: 46.7 MB (46680971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d995bc0710c59defc3b6e948b5fec04402ad900b4af1204d7420bb8e2736886a`  
		Last Modified: Wed, 01 Oct 2025 18:09:27 GMT  
		Size: 29.3 MB (29334857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:0fc10d8ea86b76cecffdd3f625918c5f61beb816e2a1f697a01612613bdfa7b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4079599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f70deb93b7affdf67c7a82b5ccdff0d09fb50c8dbba4c3516054708247ef40a5`

```dockerfile
```

-	Layers:
	-	`sha256:838b0399f001f860e3f07a1a286cdf6f5d00fd4ec10dde753e22b170d50263d6`  
		Last Modified: Wed, 01 Oct 2025 19:20:49 GMT  
		Size: 4.1 MB (4072763 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6241c0e3bc4f04ee754746ee799fdd95c43cb39c3bf4acbae894c9835f6f2808`  
		Last Modified: Wed, 01 Oct 2025 19:20:50 GMT  
		Size: 6.8 KB (6836 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:9098cc9666e579f422f80b051eba5f97a72a0aa06b05370db631399f0ccc4b58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.6 MB (76606103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:557c289db38a107ae56429d931cde4ede8e9c0e8981c13dd06e62bb9ee013cb3`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 's390x' out/ 'sid' '@1760918400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:bfcdf3c01297eb06b59232529bb37e83cf5e8225551f7278d0bbddf997984733`  
		Last Modified: Tue, 21 Oct 2025 00:24:47 GMT  
		Size: 48.3 MB (48267195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a93e1c83200c153fd9fe1cb55ab94175e48e69920e85393ca3619fdc448ac729`  
		Last Modified: Tue, 21 Oct 2025 12:40:44 GMT  
		Size: 28.3 MB (28338908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2b3f3cb93c2cdb27ab9ded3f0943dcc304d195ea5e7d77f5e2f265ef8526509d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4105092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e1241b907d03913f8dd201e5672e6a69fba496cc218c3b837fe4f09a08dff8c`

```dockerfile
```

-	Layers:
	-	`sha256:3b9a98511bb1447262afb684667c83355d737c3499dece3a9da9e8a641e5168e`  
		Last Modified: Tue, 21 Oct 2025 13:20:34 GMT  
		Size: 4.1 MB (4098288 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af6cfe703cec7359878aaab87d58cc4ef568db0806a37d143494627f0145ab67`  
		Last Modified: Tue, 21 Oct 2025 13:20:35 GMT  
		Size: 6.8 KB (6804 bytes)  
		MIME: application/vnd.in-toto+json
