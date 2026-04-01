## `buildpack-deps:resolute-curl`

```console
$ docker pull buildpack-deps@sha256:aadfe6d2eb9061a64241ba3e189329fb9463dc7dffbde8792c0029f55dbc1479
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:resolute-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:82506146a40d1e7a14122946d81d35d994be95c137f1179c84c15f682b805f53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.1 MB (61071923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4bbda63097d3fae1baac493896581e2c5793d6797bafa4c91539b323c358737`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Apr 2026 04:01:06 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-2190cb971fd0e5f37eb1b492cbc3c1e3/images/ubuntu:rockcraft-base /home/buildd/rockcraft-ubuntu-2190cb971fd0e5f37eb1b492cbc3c1e3/images/.temp_layer.4425.tar --tag 26.04
# Wed, 01 Apr 2026 04:01:06 GMT
RUN umoci config
# Wed, 01 Apr 2026 04:01:06 GMT
RUN umoci config
# Wed, 01 Apr 2026 04:01:06 GMT
RUN umoci config
# Wed, 01 Apr 2026 04:01:06 GMT
RUN umoci config
# Wed, 01 Apr 2026 04:01:06 GMT
RUN umoci config
# Wed, 01 Apr 2026 04:01:06 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-2190cb971fd0e5f37eb1b492cbc3c1e3/images/ubuntu:26.04 /home/buildd/rockcraft-ubuntu-2190cb971fd0e5f37eb1b492cbc3c1e3/images/.temp_layer.control_data.4425.tar
# Wed, 01 Apr 2026 20:05:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:a028660a7b4f1b5217ef1f9e71530c04bb548e81d05a91dba1c14a136299f534`  
		Last Modified: Wed, 01 Apr 2026 05:09:39 GMT  
		Size: 41.6 MB (41551910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7f09f0d240e7d8cf10637b0dc107589f18f90d5d58b7a8d5d83253e788969e0`  
		Last Modified: Wed, 01 Apr 2026 05:09:42 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a5838583e0357c92d847bf5b230796d38f2e305482cb640ea0a33a08f78ea86`  
		Last Modified: Wed, 01 Apr 2026 20:05:47 GMT  
		Size: 19.5 MB (19519626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:resolute-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e6c4a19e4ecc2280b11598280eb9f2e341ada86779c63a62a0cb283e3dd72546
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4363475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc76ccefd38f74243cfd0215ad2f6cdde1179ccdffbc0f9c90d3976a33588dd0`

```dockerfile
```

-	Layers:
	-	`sha256:7e4d4ad35eb1366e554f0c7e4c6ea1e6c83ab6127f7d61410876ae16a02ca319`  
		Last Modified: Wed, 01 Apr 2026 20:05:46 GMT  
		Size: 4.4 MB (4356232 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9782a4438c2d6fdfedbc5574354d2a7a45c006a673e85d8d04949970c293c32a`  
		Last Modified: Wed, 01 Apr 2026 20:05:47 GMT  
		Size: 7.2 KB (7243 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:resolute-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:4348340c5e394deb96f6f7151ed4e4f606ebf2d39129d14a2f3dd54e5a100504
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.5 MB (56456210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb4065ac1aa4134e6935746cb396d39b1065a803e85e0eda990ed0f2aac8eaa0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Apr 2026 04:04:09 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-2190cb971fd0e5f37eb1b492cbc3c1e3/images/ubuntu:rockcraft-base /home/buildd/rockcraft-ubuntu-2190cb971fd0e5f37eb1b492cbc3c1e3/images/.temp_layer.4460.tar --tag 26.04
# Wed, 01 Apr 2026 04:04:10 GMT
RUN umoci config
# Wed, 01 Apr 2026 04:04:10 GMT
RUN umoci config
# Wed, 01 Apr 2026 04:04:10 GMT
RUN umoci config
# Wed, 01 Apr 2026 04:04:10 GMT
RUN umoci config
# Wed, 01 Apr 2026 04:04:10 GMT
RUN umoci config
# Wed, 01 Apr 2026 04:04:10 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-2190cb971fd0e5f37eb1b492cbc3c1e3/images/ubuntu:26.04 /home/buildd/rockcraft-ubuntu-2190cb971fd0e5f37eb1b492cbc3c1e3/images/.temp_layer.control_data.4460.tar
# Wed, 01 Apr 2026 20:07:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:b87bc5e9902cacc98659b7db3fea909a8ae8c0e207125762ba9f55078ffef605`  
		Last Modified: Wed, 01 Apr 2026 05:10:11 GMT  
		Size: 38.6 MB (38647549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90488af8b50823555c030ac051af6efa635ef247e7d4c3d8c7e9910c3755891f`  
		Last Modified: Wed, 01 Apr 2026 05:10:13 GMT  
		Size: 391.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46104cf503adc45c0cd7985b491e2cefa21745aaf0863b165b0c724dbbdff0c4`  
		Last Modified: Wed, 01 Apr 2026 20:07:52 GMT  
		Size: 17.8 MB (17808270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:resolute-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:bfd9a53e5f8b76c70b4643712568c435ba24b6632cfa9dedb4cb389a9a51dbac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4365041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3df399fd373e224c601ea51bc189febec0c3498b882196e5447391f39697cb4d`

```dockerfile
```

-	Layers:
	-	`sha256:b44a6da4f3e7d9fe4ec91e636abc258fc90015a8b0f7fae1394172ed1ca242a7`  
		Last Modified: Wed, 01 Apr 2026 20:07:51 GMT  
		Size: 4.4 MB (4357734 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42917803fe64145fa5ce1dae1561201eec4f7ac2f9026a327d78da26e918aa52`  
		Last Modified: Wed, 01 Apr 2026 20:07:51 GMT  
		Size: 7.3 KB (7307 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:resolute-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:d57dfb2beda8497a94686d6d0b1503159f4b6b577060a0bddd59a8fd32f017e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59789944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c9b9a13053459af4ef473f5686f560d549bddf44ceebb2ba67c43deb9878c34`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Apr 2026 04:03:15 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-2190cb971fd0e5f37eb1b492cbc3c1e3/images/ubuntu:rockcraft-base /home/buildd/rockcraft-ubuntu-2190cb971fd0e5f37eb1b492cbc3c1e3/images/.temp_layer.4502.tar --tag 26.04
# Wed, 01 Apr 2026 04:03:15 GMT
RUN umoci config
# Wed, 01 Apr 2026 04:03:15 GMT
RUN umoci config
# Wed, 01 Apr 2026 04:03:15 GMT
RUN umoci config
# Wed, 01 Apr 2026 04:03:15 GMT
RUN umoci config
# Wed, 01 Apr 2026 04:03:15 GMT
RUN umoci config
# Wed, 01 Apr 2026 04:03:15 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-2190cb971fd0e5f37eb1b492cbc3c1e3/images/ubuntu:26.04 /home/buildd/rockcraft-ubuntu-2190cb971fd0e5f37eb1b492cbc3c1e3/images/.temp_layer.control_data.4502.tar
# Wed, 01 Apr 2026 20:05:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e01771b74c5a1f96dc758c147c06fb46daa8f6142de3935a5b8ad25c5f395a90`  
		Last Modified: Wed, 01 Apr 2026 05:09:50 GMT  
		Size: 40.7 MB (40734995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59caf9e43b45d2a51ce8729f055a065c5081c6e9a3b145ea8f9b573f05936182`  
		Last Modified: Wed, 01 Apr 2026 05:09:53 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10e62c4f1f39ef342f5f9676dfc2e62081ae01b9edd9b110549359bbe5b9e84e`  
		Last Modified: Wed, 01 Apr 2026 20:05:55 GMT  
		Size: 19.1 MB (19054561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:resolute-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f2afcc493cdb5091a9d3348528ccc0721f52a1bc1bef6541c5a8bc614de5ec5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4363813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46e1e17c7ce283682d2cc044bf52d7f499275ddfe79594958fb68fbeea02a035`

```dockerfile
```

-	Layers:
	-	`sha256:34253c32ae5c538d835db8bb3e9a66aa58fb0be9cf80af9a7408accfb24eddc6`  
		Last Modified: Wed, 01 Apr 2026 20:05:54 GMT  
		Size: 4.4 MB (4356490 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:996d303489ae82a1d7f93c9fd9bd95d950402941ec2f7d8cd2fd50e1f6ce88d2`  
		Last Modified: Wed, 01 Apr 2026 20:05:54 GMT  
		Size: 7.3 KB (7323 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:resolute-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:27dcea4a3415d62dbe0eabc0e368871116a8c39deb3feb16af815c0dab6fb2fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.7 MB (68738631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4acdc408e27685a2a8f11430ee95dc0f10cbf94c551ee5ae29710c0e327e275f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Apr 2026 04:04:11 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-2190cb971fd0e5f37eb1b492cbc3c1e3/images/ubuntu:rockcraft-base /home/buildd/rockcraft-ubuntu-2190cb971fd0e5f37eb1b492cbc3c1e3/images/.temp_layer.4409.tar --tag 26.04
# Wed, 01 Apr 2026 04:04:11 GMT
RUN umoci config
# Wed, 01 Apr 2026 04:04:11 GMT
RUN umoci config
# Wed, 01 Apr 2026 04:04:11 GMT
RUN umoci config
# Wed, 01 Apr 2026 04:04:11 GMT
RUN umoci config
# Wed, 01 Apr 2026 04:04:11 GMT
RUN umoci config
# Wed, 01 Apr 2026 04:04:12 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-2190cb971fd0e5f37eb1b492cbc3c1e3/images/ubuntu:26.04 /home/buildd/rockcraft-ubuntu-2190cb971fd0e5f37eb1b492cbc3c1e3/images/.temp_layer.control_data.4409.tar
# Wed, 01 Apr 2026 20:17:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:2d29a67913207c73576260dcfc2f317ce8f370d2e6036a15cea1d4c50619f9e0`  
		Last Modified: Wed, 01 Apr 2026 05:10:00 GMT  
		Size: 46.7 MB (46747843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:632d8b198f2e7d6fc57ec36af12b5218cd6b2fdd0af240c60203b87363f9d140`  
		Last Modified: Wed, 01 Apr 2026 05:10:03 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a322216276af0165efcb8f7a01337a87030ed5621a502f99fe12e03f8972fa4`  
		Last Modified: Wed, 01 Apr 2026 20:17:58 GMT  
		Size: 22.0 MB (21990398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:resolute-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d80d27815332dbf2be245e0d56469361e4a493cddf97e07785ab0c1d98c6d9bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4367330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdeef8179458808e4c5e297d8942fa6f00474296ad50c74cf27bcf8148a8a175`

```dockerfile
```

-	Layers:
	-	`sha256:14dc203bd38022e398219d4ad5c606778be7a1ede87cc3f2bcfa65a0cd5f20b2`  
		Last Modified: Wed, 01 Apr 2026 20:17:58 GMT  
		Size: 4.4 MB (4360055 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:275ee2bdb17c1fa00a61021a37dacd152cb903295427e6cea79e5a8e4a218830`  
		Last Modified: Wed, 01 Apr 2026 20:17:58 GMT  
		Size: 7.3 KB (7275 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:resolute-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:ec90b1594568bcc4d786634942fe07c5ed4d2e6d7c185013a7b2c5ad6107017c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.1 MB (61115462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea198d9d5857e4f9437f94db7691ff23fc51f201a0f605b160bee427d660c677`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Apr 2026 04:04:25 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-2190cb971fd0e5f37eb1b492cbc3c1e3/images/ubuntu:rockcraft-base /home/buildd/rockcraft-ubuntu-2190cb971fd0e5f37eb1b492cbc3c1e3/images/.temp_layer.4471.tar --tag 26.04
# Wed, 01 Apr 2026 04:04:25 GMT
RUN umoci config
# Wed, 01 Apr 2026 04:04:25 GMT
RUN umoci config
# Wed, 01 Apr 2026 04:04:25 GMT
RUN umoci config
# Wed, 01 Apr 2026 04:04:25 GMT
RUN umoci config
# Wed, 01 Apr 2026 04:04:25 GMT
RUN umoci config
# Wed, 01 Apr 2026 04:04:25 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-2190cb971fd0e5f37eb1b492cbc3c1e3/images/ubuntu:26.04 /home/buildd/rockcraft-ubuntu-2190cb971fd0e5f37eb1b492cbc3c1e3/images/.temp_layer.control_data.4471.tar
# Wed, 01 Apr 2026 20:14:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:1ec23a920706567555cbde8fd1a678eb0fc884335da074568e17a20e5c82930e`  
		Last Modified: Wed, 01 Apr 2026 05:10:32 GMT  
		Size: 41.1 MB (41118651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7bdc07369a1ddaa6de066f70a0f9a108bb5825b1bd40d6d4f6597f005bc34d7`  
		Last Modified: Wed, 01 Apr 2026 05:10:34 GMT  
		Size: 389.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbc25a5beb15342c7e309bfdccb5203cbe47007ad1730733e60115e0d560df0a`  
		Last Modified: Wed, 01 Apr 2026 20:14:27 GMT  
		Size: 20.0 MB (19996422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:resolute-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5cf1be841ee60498966fc1dee7046072bfa4950be8e04a5ee61933dcf0a683ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4365506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e137ad94ff34b56714af44af3e186f72d66fbe1e99a7f17762a2e19389d75a9`

```dockerfile
```

-	Layers:
	-	`sha256:5ac04c707a315932b4e8d4046fa61bd99325eb4ddbcc7598fbecc21747965516`  
		Last Modified: Wed, 01 Apr 2026 20:14:27 GMT  
		Size: 4.4 MB (4358263 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:460c4cd00b01d7883f2ae8c8e81a86fd9ce1cb175e00493f073a4e105019c80a`  
		Last Modified: Wed, 01 Apr 2026 20:14:26 GMT  
		Size: 7.2 KB (7243 bytes)  
		MIME: application/vnd.in-toto+json
