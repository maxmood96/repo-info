## `buildpack-deps:bookworm-scm`

```console
$ docker pull buildpack-deps@sha256:7166e54034b46b5acdf70aa0b5df7b6dafca628814cf3b98079ccf104a30d40e
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

### `buildpack-deps:bookworm-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:faa2673379ca1a7d13117355d28a8fb53549ccda673bd88394e40ea8de5ece19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.9 MB (136903521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aeb00390adcbeb390dc848137089fe2cac00c4efb1d6f18e50bc4edb5e43f74d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:8fb375ec14f3df8b31b70d0216508565ab7264a7e16cac4f8cc07f8eca22445f`  
		Last Modified: Mon, 08 Sep 2025 21:12:37 GMT  
		Size: 48.5 MB (48480610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccbbb2080a06a2888e44131965340c1eccd23f4d49efe72176246649abfbf9d9`  
		Last Modified: Mon, 08 Sep 2025 21:54:14 GMT  
		Size: 24.0 MB (24025996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d5073558d5a5274440fddfe987f56645dc90b8b84481e9e3dc858ac3311e33e`  
		Last Modified: Mon, 08 Sep 2025 22:13:51 GMT  
		Size: 64.4 MB (64396915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:4fe49946cedf832a907d5e4a81aea64b8ce2962debbcc2a8be5a6f5df85d6de1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7972758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:004735eeecc263b95767fd5dd88acb6fd2ef1823223a73334171e9f7e01d95b9`

```dockerfile
```

-	Layers:
	-	`sha256:28ae8cbd2a5bee47c911c2ae5d7d34643d29c79498ce5549c1f6a5ee10219f7c`  
		Last Modified: Tue, 09 Sep 2025 01:19:52 GMT  
		Size: 8.0 MB (7965405 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc58056c7ee16c94efcdfd37eb47b210f813ef87877b71816414a6ddd1f110d8`  
		Last Modified: Tue, 09 Sep 2025 01:19:53 GMT  
		Size: 7.4 KB (7353 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:0e490253b7c826bfe7f2b5b431610bbdcf3e417565554ee9098c2bb79f31b591
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.7 MB (130728774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c09587e8ade103b5cbf96e7d5ef40efd15cc7c8339aa57e700a1a7d596d3379e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1757289600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:cb78550743da54c438514c9643e672e9378df901e1cdbedec41078f3c369313d`  
		Last Modified: Mon, 08 Sep 2025 21:13:54 GMT  
		Size: 46.0 MB (46015690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:021282bc493daf4a7f690f4c5ff13dd6b9ca0b3670be69b20780afc009b935a3`  
		Last Modified: Tue, 09 Sep 2025 01:31:45 GMT  
		Size: 22.7 MB (22702497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c53fafdbc28fe332224708213002063b17ece9649ba71df33c9c82a8c3edd746`  
		Last Modified: Tue, 09 Sep 2025 05:05:26 GMT  
		Size: 62.0 MB (62010587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:957dee9c64060be18b35e072b6ef87ba6a4ead4484ced6aac81db26578437ccb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7974680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9510bd7cd5b77151594928ed21d04884c1e484c58825e43a69abc81e8676f330`

```dockerfile
```

-	Layers:
	-	`sha256:e44e5961d6b74861f4e11c9bd0886d2ff480aa3ac93c43b8109c1bace75c27e2`  
		Last Modified: Tue, 09 Sep 2025 04:19:58 GMT  
		Size: 8.0 MB (7967263 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8904882b6668c839393a7d5fc34743617067026b89003721ddeb6ace05b50cd`  
		Last Modified: Tue, 09 Sep 2025 04:19:59 GMT  
		Size: 7.4 KB (7417 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:d8df11df6854c43b861bdfa36cb2124117264827bedddd880dcc1e92fb7ea081
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.8 MB (125779903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24f3dae968e315a8a940efa8f741566d46e056fcca1d3b180693179fb32edc82`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1757289600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:66de9a3b6b96c15de3235377e1618295643161d16058e17bde51f54951c6ec21`  
		Last Modified: Mon, 08 Sep 2025 21:14:33 GMT  
		Size: 44.2 MB (44195998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0efd1e8889a5c39ed7ad3628cf08e3daff474f9ff5b33972b323c79f306440f8`  
		Last Modified: Mon, 08 Sep 2025 23:37:54 GMT  
		Size: 21.9 MB (21931079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1ad8fb006981127731180a5d548f700fd609cacd7e365cb66fbcaf2fd1e979c`  
		Last Modified: Tue, 09 Sep 2025 03:21:06 GMT  
		Size: 59.7 MB (59652826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6f6ca0e8e4f61bd9478c1cc65f638d43bef03eff1d16e4ccf4a2bab726670495
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7974099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e19a925cd8c53dbd4dece85c6c40bbbd20d6d5f7721d755cd594fbd41fe3f772`

```dockerfile
```

-	Layers:
	-	`sha256:afcc71167e78b9a200f06322f2d52a9850d9f18e22c82d38ecbff1ed946442ba`  
		Last Modified: Tue, 09 Sep 2025 04:20:10 GMT  
		Size: 8.0 MB (7966682 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a64743ce31fc24faf09fa2c47002f9b62a164073e56b2254f9706f990e3901f`  
		Last Modified: Tue, 09 Sep 2025 04:20:11 GMT  
		Size: 7.4 KB (7417 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:ec88ea0aca93d3ac133bb54a71b0dabd1f7c5552db50531c21878db58c9a195b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.3 MB (136324989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b29c50c493623ca519fbe0d366e283084a50a75e0306f09d261523212bee358b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1757289600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a9331b686701a987bcd276cc69a0f676d471ccda1aa353d2f7fad017f2894cd0`  
		Last Modified: Mon, 08 Sep 2025 21:14:32 GMT  
		Size: 48.4 MB (48359019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e108925666d6d84c8fa32751877e66a295ad55c9fbd10142325b99d60e786e17`  
		Last Modified: Mon, 08 Sep 2025 22:21:46 GMT  
		Size: 23.6 MB (23594789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:133142790bc081eb3e5455996df5c3f98df543c5a224c3643437a19d4d6a7d93`  
		Last Modified: Tue, 09 Sep 2025 02:12:12 GMT  
		Size: 64.4 MB (64371181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b60f2b79fd17243e29cf935a1ce6ba0f35235428254214dc24c2dfd80b5aa773
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7979231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a93f105fd01965ddbdff98de65656b7795fa60be69d0ad515c6275b197b74692`

```dockerfile
```

-	Layers:
	-	`sha256:c9d52a71027fa0499d68e558cbb62063fec26ef165f3c1ac191acdcceefa65d2`  
		Last Modified: Tue, 09 Sep 2025 03:24:04 GMT  
		Size: 8.0 MB (7971798 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:522c60f485463e79617a4fbf00432ee738843843cf7463fe9eecb39e47138a87`  
		Last Modified: Tue, 09 Sep 2025 03:24:05 GMT  
		Size: 7.4 KB (7433 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:3cdc8ae5ba6063f04faa3089a1bba0f962b397b7564261ef127cb36575fe53d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.6 MB (140560393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7be6e35262f00f1f795f78b9e296d7ebe8e8dc788bb0e07cb8aa1af3e8042c0f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1757289600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:5538e96bb7df1a7ef01bd7fcbf51f4cbc041246109c06cf661f7058c203851af`  
		Last Modified: Mon, 08 Sep 2025 21:12:26 GMT  
		Size: 49.5 MB (49466684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:822d7073f1bfbc05d754234ff0c82bf81a44dcb6b19979f28688d3054a71fa6a`  
		Last Modified: Mon, 08 Sep 2025 22:07:56 GMT  
		Size: 24.9 MB (24860658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2248c0dfdaafb69ef95f2c3162eb9698e04d446b6646131ff2e543b79a6f79f`  
		Last Modified: Mon, 08 Sep 2025 22:39:17 GMT  
		Size: 66.2 MB (66233051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e501e0328136415ea3c4ef29265d52cdb9ad7abc78123e0b88b55b139fae12a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7968894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e729c4b95ae4d55c1eb4f5ef75adb30a00b1a75d858a34daf5be98c9de0a5c6c`

```dockerfile
```

-	Layers:
	-	`sha256:a008b010ff09ee7b2c2e8bf9369789c31568130109cd844bf9f06161d6a4edc3`  
		Last Modified: Tue, 09 Sep 2025 01:20:18 GMT  
		Size: 8.0 MB (7961564 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:709e1b452449df1ed6908563962467b8554de55d0857133c8ee963f5f23afdbd`  
		Last Modified: Tue, 09 Sep 2025 01:20:20 GMT  
		Size: 7.3 KB (7330 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:0af539e8157ba279534e7ec40e53d946deb13bcc71bd18d618da8ebcf568ddfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.7 MB (135689031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86cbf13bd156ad443757ef41fa2e5723601c0acf3b00e39cf455cba7dcbedfa1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1754870400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:39ab9a968f454fda0ebffae415d31434cb4c4b3f4bb9da0e89f360bd60fa3275`  
		Last Modified: Tue, 12 Aug 2025 21:09:50 GMT  
		Size: 48.8 MB (48776657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd5bf976bc5466a2e4cdc6d87c28337bf663ea094da7d169694d61961d11248d`  
		Last Modified: Wed, 13 Aug 2025 06:38:46 GMT  
		Size: 23.6 MB (23603659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e53fb77ec58b351a832fef6343e52e81f478bfac5e6664210978fbb38a2cddf`  
		Last Modified: Wed, 13 Aug 2025 19:21:03 GMT  
		Size: 63.3 MB (63308715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ae767b3acea6b4e9df5e03f3262d18b389a0e72832b42a16f237ad22c502829b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 KB (7186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce5b83a8b3a5666d11c8ce30aaf9f9b7fec343019b3bf6b7dff3ede90a810a94`

```dockerfile
```

-	Layers:
	-	`sha256:3841e43b5793ce163b6086997052c6380227d18a667a5557e1744f8e1c878c38`  
		Last Modified: Wed, 13 Aug 2025 19:20:05 GMT  
		Size: 7.2 KB (7186 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:b72bba2182417f99a964bbf11d55bbb4b48f2cf2f918955c7a36a8947a363a67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.8 MB (147844082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e980f2e0e0ea9958a049fe4a14e100ffbfd14324231eeece6d7d59633ebc21ff`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1754870400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:33bc01697f2fcceb00fe53fe1bf433b48dc127c82c1555f61eeddeda9d72ff40`  
		Last Modified: Tue, 12 Aug 2025 23:05:53 GMT  
		Size: 52.3 MB (52338077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2f87ea767eb09118b3668a0dc44ddf5bf258db4f1bebc7989803cb1b75a66c9`  
		Last Modified: Wed, 13 Aug 2025 14:33:16 GMT  
		Size: 25.7 MB (25666039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddb09aa58684adf8f458ec24cfe46bcd658b8344a3c5c5ec70c88bbe9010b255`  
		Last Modified: Wed, 13 Aug 2025 22:43:40 GMT  
		Size: 69.8 MB (69839966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:201302114e7a81ebe245b77565e1f4799865a62503cd5b60683f7a310dfeda8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7973878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd3344f44cedea04699bf5575626cf58521d336b7a543eddfe2d113e1f69aa61`

```dockerfile
```

-	Layers:
	-	`sha256:57eb9b5adaa6a6a20a7ff447a9f921ccca850583aa272b3e3052696819624479`  
		Last Modified: Wed, 13 Aug 2025 22:20:07 GMT  
		Size: 8.0 MB (7966493 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62d8a05a38fee0f63b96a5cdbb5ba559563c0dc675a394d9a9fffe7bdf65d8e2`  
		Last Modified: Wed, 13 Aug 2025 22:20:08 GMT  
		Size: 7.4 KB (7385 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:5e2c358e028db9088572818d06e8c4af5b4662cac3fe551ad5f0b89614350444
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 MB (134667807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a8e846138286aa29e370eb2cf9935361974755ec4499a1053f68435bbfd98c2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1754870400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:635b31fd21bf059b6af0abf57b343066d0218ebb3e0b679927cc1752427a72da`  
		Last Modified: Tue, 12 Aug 2025 20:53:37 GMT  
		Size: 47.1 MB (47149866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af75c300f83884b3a2b4352096299334113ee00d6718ab116cdad0fd28ea4064`  
		Last Modified: Wed, 13 Aug 2025 03:14:49 GMT  
		Size: 24.0 MB (24020172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4afd6f1f2a58fa1289478b7c4157102354638b354f847958c5d7c5b4449c508e`  
		Last Modified: Wed, 13 Aug 2025 08:03:43 GMT  
		Size: 63.5 MB (63497769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b171f698ea0ba97e70a12cd9b93d1122c6a56b8f7377fe950d19c4b8a3ba8e1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7962298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe7763692578eeea1a8fbc54e46d731c8b4579c84a738667d553e076c1d8c36b`

```dockerfile
```

-	Layers:
	-	`sha256:de1f742393f65cda74f04421cc90ff14e440c56fa1ba180fafa2f161bde896e9`  
		Last Modified: Wed, 13 Aug 2025 10:20:07 GMT  
		Size: 8.0 MB (7954945 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48937b347e90baef8fa42146cc2347b827e69d378d41c8f3580686ad378a85cd`  
		Last Modified: Wed, 13 Aug 2025 10:20:08 GMT  
		Size: 7.4 KB (7353 bytes)  
		MIME: application/vnd.in-toto+json
