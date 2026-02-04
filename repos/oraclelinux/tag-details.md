<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `oraclelinux`

-	[`oraclelinux:10`](#oraclelinux10)
-	[`oraclelinux:10-slim`](#oraclelinux10-slim)
-	[`oraclelinux:7`](#oraclelinux7)
-	[`oraclelinux:7-slim`](#oraclelinux7-slim)
-	[`oraclelinux:7-slim-fips`](#oraclelinux7-slim-fips)
-	[`oraclelinux:7.9`](#oraclelinux79)
-	[`oraclelinux:8`](#oraclelinux8)
-	[`oraclelinux:8-slim`](#oraclelinux8-slim)
-	[`oraclelinux:8-slim-fips`](#oraclelinux8-slim-fips)
-	[`oraclelinux:8.10`](#oraclelinux810)
-	[`oraclelinux:9`](#oraclelinux9)
-	[`oraclelinux:9-slim`](#oraclelinux9-slim)
-	[`oraclelinux:9-slim-fips`](#oraclelinux9-slim-fips)

## `oraclelinux:10`

```console
$ docker pull oraclelinux@sha256:70e74281db6949cf1e4a1ee20b4808f038f9365f23b97bf73841acfec78b2164
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `oraclelinux:10` - linux; amd64

```console
$ docker pull oraclelinux@sha256:6adaf30323be88917cd583eb6c9d4b5de1432b93c87afc9725c4c9a15315f792
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.1 MB (95076852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b06df90b88eabeec9249b9da512af6c298696ad9f81282af47a55fee9fb4c8c9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 04 Feb 2026 00:25:01 GMT
ADD oraclelinux-10-amd64-rootfs.tar.xz / # buildkit
# Wed, 04 Feb 2026 00:25:01 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:3b56ffef683fab780f6a81fc6ef428658356d0a3dc55b625d5bd826a9f4d1b7e`  
		Last Modified: Wed, 04 Feb 2026 00:25:21 GMT  
		Size: 95.1 MB (95076852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `oraclelinux:10` - unknown; unknown

```console
$ docker pull oraclelinux@sha256:e441d5d5739930e62ec5ec5c093ecb91691adfc04eea6195d0587ab7b780b4c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5544103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57f9ab2bb66ce6850864c1abe0d2c1c8d7d1b6c3ebb37a118d2fa5979258fd88`

```dockerfile
```

-	Layers:
	-	`sha256:e8f26da51a10833827e3ce9deb9f230e7c018ec6c14785144052b52660237448`  
		Last Modified: Wed, 04 Feb 2026 00:25:19 GMT  
		Size: 5.5 MB (5539293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa156e7350d061ea1e2b37bf689a515c93c39f677c9954b69aab4072ab9a634d`  
		Last Modified: Wed, 04 Feb 2026 00:25:18 GMT  
		Size: 4.8 KB (4810 bytes)  
		MIME: application/vnd.in-toto+json

### `oraclelinux:10` - linux; arm64 variant v8

```console
$ docker pull oraclelinux@sha256:1e5ed68866985117b56ce403e65befc60eb3f96dabc6d92ab00dbdb595b6f7f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.2 MB (93170101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:438c9f1c8ac78e162c62279f814551b1d8545a95e1d738f43e5cd8e9393c6b32`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 04 Feb 2026 00:24:02 GMT
ADD oraclelinux-10-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 04 Feb 2026 00:24:02 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:968729e60a06cef6e4ebc8fc12d991a466562e25c9828980515ee0711b6915be`  
		Last Modified: Wed, 04 Feb 2026 00:24:26 GMT  
		Size: 93.2 MB (93170101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `oraclelinux:10` - unknown; unknown

```console
$ docker pull oraclelinux@sha256:43ab8e56cdbc7dd9c2c6b2dd788211865da7ecaac49f7efb0fd33be8a17e8a56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5544225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7290c8991246a4e58dac7562d6597ffc44b6a6f632563213bee9173695dc96c`

```dockerfile
```

-	Layers:
	-	`sha256:08e336b7d8a7a9aa6494ecf27b23efc3cd7df706260a145e0e9041a1bb57b182`  
		Last Modified: Wed, 04 Feb 2026 00:24:22 GMT  
		Size: 5.5 MB (5539382 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:263c302e7b22db9c0871a52b7761bcb6a0d3452e69f95f95391b8faa7bbffb53`  
		Last Modified: Wed, 04 Feb 2026 00:24:23 GMT  
		Size: 4.8 KB (4843 bytes)  
		MIME: application/vnd.in-toto+json

## `oraclelinux:10-slim`

```console
$ docker pull oraclelinux@sha256:e7dcfab74f0cf104d08a345a3c9e9af011d53da3c0dfa4f3394821ed87ee11ed
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `oraclelinux:10-slim` - linux; amd64

```console
$ docker pull oraclelinux@sha256:f45abc686f31de0133a414963c3f4f6ac0062141e08e152fcc494a7aaaeafc6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.0 MB (43030480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfd8fc9300858c7a934f53387f185f5efebea8690b99dbf0a9c965f1f3f59fec`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 04 Feb 2026 00:25:41 GMT
ADD oraclelinux-10-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 04 Feb 2026 00:25:41 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:b54068dedc8837199fe2dae68343f5ee21898a08b026620fcc9a73c0f5f736de`  
		Last Modified: Wed, 04 Feb 2026 00:25:51 GMT  
		Size: 43.0 MB (43030480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `oraclelinux:10-slim` - unknown; unknown

```console
$ docker pull oraclelinux@sha256:3c21b66888190fa6a705bda9b53ed7c8296bd82e7c1039c08910131ed65d7b9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1017451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4e770270f16d871f21e06f6824dc2b31135befddf99afda89428bbce9fcc115`

```dockerfile
```

-	Layers:
	-	`sha256:af28d63312d6b693d035636098dec4c9367ab182bf63a86cc01cda9019a16235`  
		Last Modified: Wed, 04 Feb 2026 00:25:50 GMT  
		Size: 1.0 MB (1012605 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fecd163d61160cc8df55ad772e5d1815b2fb433cf2f5fe09e1cab487d0df89e9`  
		Last Modified: Wed, 04 Feb 2026 00:25:50 GMT  
		Size: 4.8 KB (4846 bytes)  
		MIME: application/vnd.in-toto+json

### `oraclelinux:10-slim` - linux; arm64 variant v8

```console
$ docker pull oraclelinux@sha256:b453a0047b713abea651eb9aa0fb10773c3e57bd928839196854d5ec365a4707
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.4 MB (41440840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e04657b6c1c38f1aad34da7ebc4eb92f41015f4cc5c0abc84344890ee5eaa268`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 04 Feb 2026 00:25:11 GMT
ADD oraclelinux-10-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 04 Feb 2026 00:25:11 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:b1c04f18254162ff5a3c45d97c70abfb61551be624bc44f3ddf318c0b14a8c28`  
		Last Modified: Wed, 04 Feb 2026 00:25:22 GMT  
		Size: 41.4 MB (41440840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `oraclelinux:10-slim` - unknown; unknown

```console
$ docker pull oraclelinux@sha256:67b34ae0028580e7c23cb897e65fd4d6f82dfe4ef9e46d7f873b0ec712b032cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1017501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ebb2b2ad9569e8b631e5134009acee721839be61ea103512419e7968cd0c735`

```dockerfile
```

-	Layers:
	-	`sha256:7cd0681727e28ba4e3d12f96bc5d4d6f099ec1372355cb945a870e039efd599b`  
		Last Modified: Wed, 04 Feb 2026 00:25:20 GMT  
		Size: 1.0 MB (1012625 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48a705f01a2235a47e40658e4a30febcd2a7c569705fe51bf286b284aeb50d0c`  
		Last Modified: Wed, 04 Feb 2026 00:25:20 GMT  
		Size: 4.9 KB (4876 bytes)  
		MIME: application/vnd.in-toto+json

## `oraclelinux:7`

```console
$ docker pull oraclelinux@sha256:767c93c07b1fa621ae56d1f5f090e8c0dce7eb452e7dda1e74bbe7546504d63f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `oraclelinux:7` - linux; amd64

```console
$ docker pull oraclelinux@sha256:7bd67d839b5296423b49806513e985d1440c1666732bdab49d8fe4f2eaa8882e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.4 MB (95379377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27eb3f6a5a2ea765d10a69fcc8cdf5e8d551d46aad900344db5a30bc2790f925`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 10 Dec 2024 23:51:26 GMT
ADD oraclelinux-7-amd64-rootfs.tar.xz / # buildkit
# Tue, 10 Dec 2024 23:51:26 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:7e97d888e3ce798d1fd4f6290ab2faa2e76d131b997de8abd0073b19ce89ff9e`  
		Last Modified: Wed, 11 Dec 2024 20:29:27 GMT  
		Size: 95.4 MB (95379377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `oraclelinux:7` - unknown; unknown

```console
$ docker pull oraclelinux@sha256:48cbf9d2b2eb4e8b49abbc4a5ee884bbd4e38d9a7775f32d23521d4cb4ec9334
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5986658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca2d2f842db34aaa9439decd84f84e8cdd5677d3ec53e95365d21157d33f121f`

```dockerfile
```

-	Layers:
	-	`sha256:27e4fd6dc2a746095a9d3bda1f23775ebdee67e2f23c01fdc355d4073032ea97`  
		Last Modified: Wed, 11 Dec 2024 20:29:26 GMT  
		Size: 6.0 MB (5981509 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c096aa08ec8ef96172085216ad2f1438f843a0454bec76e639965c1886237f5d`  
		Last Modified: Wed, 11 Dec 2024 20:29:26 GMT  
		Size: 5.1 KB (5149 bytes)  
		MIME: application/vnd.in-toto+json

### `oraclelinux:7` - linux; arm64 variant v8

```console
$ docker pull oraclelinux@sha256:fa93b39b22ba5975b662591e71d508b060c06a60b0dd149aedd57e8832dee1bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.3 MB (97327013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1819ead03a2e5166f44a38f549f069a3b0a7d2987fb565b8c5165cf40e5bf2f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 10 Dec 2024 23:52:16 GMT
ADD oraclelinux-7-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 10 Dec 2024 23:52:16 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:9d7edc91d9d8dde556a51cc4cb7cfc1cfea1a0c15f6388ab6c8b583c8f8c42c8`  
		Last Modified: Wed, 11 Dec 2024 20:30:26 GMT  
		Size: 97.3 MB (97327013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `oraclelinux:7` - unknown; unknown

```console
$ docker pull oraclelinux@sha256:382ad209af84477ee4b3dc4bcfee2f50041252a10cf71d5e0499285ae44489b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5980190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b4bf0b4acbd52c5c2c36018b0f5310d7d7d5d8905633d958151bfdf0286fe62`

```dockerfile
```

-	Layers:
	-	`sha256:808b3b6e809d50e57eab82cabcc5d37acf7266bcdf087589d1ad337a77ffd5d5`  
		Last Modified: Wed, 11 Dec 2024 20:30:24 GMT  
		Size: 6.0 MB (5975000 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa0fb3a85603ebc1f4a6e7cb274bcb060fdd154bd987a2f2ee1d7d3022548e50`  
		Last Modified: Wed, 11 Dec 2024 20:30:23 GMT  
		Size: 5.2 KB (5190 bytes)  
		MIME: application/vnd.in-toto+json

## `oraclelinux:7-slim`

```console
$ docker pull oraclelinux@sha256:1add6ed8602ea996528110fe75f4b03c2ca7ffdbe9497148dbb46c3cc9ce6acd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `oraclelinux:7-slim` - linux; amd64

```console
$ docker pull oraclelinux@sha256:645371a66c08ed18b7aacf217c964f0db70c26ac87f3d8816d7ae24160f178e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50488860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05211a081d592eb56daf16b0651eb55b233a65466492b28345804309b45caf21`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 10 Dec 2024 23:51:26 GMT
ADD oraclelinux-7-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 10 Dec 2024 23:51:26 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:38299ae2e819f6ec4befee45312f809ca241167aa554dd79e0a4baf505b88d21`  
		Last Modified: Wed, 11 Dec 2024 20:29:22 GMT  
		Size: 50.5 MB (50488860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `oraclelinux:7-slim` - unknown; unknown

```console
$ docker pull oraclelinux@sha256:3e60616703d321b4c868bf296f2fd6c8c6c5539d7252f553a29a38d9c7e381b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4265757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3719d88423e8ac803d456c5577f5999495b77126402be43cca2ffafe64bc5cdf`

```dockerfile
```

-	Layers:
	-	`sha256:93bca7b03d35bd2fefaf75af27762097b46af67876bee548d64a9b6b6006d9a3`  
		Last Modified: Wed, 11 Dec 2024 20:29:21 GMT  
		Size: 4.3 MB (4260876 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e4ba8e10b3db73de89af88b81958d66dc02f595d255183dc19952eb0ce4e621`  
		Last Modified: Wed, 11 Dec 2024 20:29:21 GMT  
		Size: 4.9 KB (4881 bytes)  
		MIME: application/vnd.in-toto+json

### `oraclelinux:7-slim` - linux; arm64 variant v8

```console
$ docker pull oraclelinux@sha256:c076be2394491ba6ee7e1c181bba19f7fb14b9b7a3d02a587e39990095e1f33b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51085581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f06f30900e46d5c64d59c1d25d8ab52556276be4385ec1a0390fb904c5264e01`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 10 Dec 2024 23:52:16 GMT
ADD oraclelinux-7-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 10 Dec 2024 23:52:16 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:7f916988e24d766c1f69587f05a2bec5c9eaa3b83215ef893b0a1c187a4080e2`  
		Last Modified: Wed, 11 Dec 2024 20:30:50 GMT  
		Size: 51.1 MB (51085581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `oraclelinux:7-slim` - unknown; unknown

```console
$ docker pull oraclelinux@sha256:5b1dc952926404e7492092f571e5821751c628902e657ba855a481ed94018fa2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4261981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c0d1dae38824c867305a6a9860f9e0aaa76d28518ec25c93b6e7e70a102f95c`

```dockerfile
```

-	Layers:
	-	`sha256:65358737d3c6c3d7c88bcc5babcc796654b2ea32bf52846e7df42a2576ecf66b`  
		Last Modified: Wed, 11 Dec 2024 20:30:49 GMT  
		Size: 4.3 MB (4257067 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5767786f31b0ec8711c380c8c59ed27febec722831f991be9790f1ba558d597b`  
		Last Modified: Wed, 11 Dec 2024 20:30:48 GMT  
		Size: 4.9 KB (4914 bytes)  
		MIME: application/vnd.in-toto+json

## `oraclelinux:7-slim-fips`

```console
$ docker pull oraclelinux@sha256:412c63a1a077bf720cb5371c81e8b3ff223068a81502115b5c16c6a8e0b47d06
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `oraclelinux:7-slim-fips` - linux; amd64

```console
$ docker pull oraclelinux@sha256:12ac0df82f5a3f2f09ecad7854ea4444fc1b708ef411c1e2f24d6f25d4245ab4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.4 MB (76371715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50463282112b0271e86226490f8f265a25803e9027da5110791e968ef330fe1f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 10 Dec 2024 23:51:26 GMT
ADD oraclelinux-7-slim-fips-amd64-rootfs.tar.xz / # buildkit
# Tue, 10 Dec 2024 23:51:26 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:9e381a889e7f7459c839feb62226085f5b7525448d0f6680fac53900ab4ba12d`  
		Last Modified: Wed, 11 Dec 2024 20:29:52 GMT  
		Size: 76.4 MB (76371715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `oraclelinux:7-slim-fips` - unknown; unknown

```console
$ docker pull oraclelinux@sha256:3fac3d84b86523a883865ed8f2af0be8356d4aa35e684adae0a4479919f2f56c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5126535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dc0605a6d6bf225b94244189b2b8e89c5beede52a9b7cad51d157f3989a9f2d`

```dockerfile
```

-	Layers:
	-	`sha256:4f9cbc8a8c05259ded9bf3516634c155287aff566191d9c0da39f98bfc94f423`  
		Last Modified: Wed, 11 Dec 2024 20:29:50 GMT  
		Size: 5.1 MB (5121617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77d014e356117e170e2658308a622945cc432eeaeb8dae01189679438180047e`  
		Last Modified: Wed, 11 Dec 2024 20:29:49 GMT  
		Size: 4.9 KB (4918 bytes)  
		MIME: application/vnd.in-toto+json

### `oraclelinux:7-slim-fips` - linux; arm64 variant v8

```console
$ docker pull oraclelinux@sha256:4b254a0e1369e408b33ec9790d2467649b6664dfddf2fcbea700d910d055e7b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.0 MB (77985183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ede26b130cea5ed695383e2c7010bd152ff5f8ded3a7930551fd9370ce53b30`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 10 Dec 2024 23:52:16 GMT
ADD oraclelinux-7-slim-fips-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 10 Dec 2024 23:52:16 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:b50bd403ff40f287f6fc609d6d2c609ee8eb561a4fa13293b9c6b686bd8f7cff`  
		Last Modified: Wed, 11 Dec 2024 20:31:21 GMT  
		Size: 78.0 MB (77985183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `oraclelinux:7-slim-fips` - unknown; unknown

```console
$ docker pull oraclelinux@sha256:a168426b3c9391aa341551993a6681b05a63b3495ca97b187e8d66a81d4bf375
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5122760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce130b99a71cc90c5ba4b4114df2a09f196d1985957304e529b7372e3531ff3b`

```dockerfile
```

-	Layers:
	-	`sha256:15a9e031bceed3e015eb997b73961b66e8704e7256dfcd494c2cc941ddd68762`  
		Last Modified: Wed, 11 Dec 2024 20:31:19 GMT  
		Size: 5.1 MB (5117808 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:daf49abd27521aa834ddfe1bf3fd10cf25d974c06de2eccc4319593d0f5375cf`  
		Last Modified: Wed, 11 Dec 2024 20:31:18 GMT  
		Size: 5.0 KB (4952 bytes)  
		MIME: application/vnd.in-toto+json

## `oraclelinux:7.9`

```console
$ docker pull oraclelinux@sha256:767c93c07b1fa621ae56d1f5f090e8c0dce7eb452e7dda1e74bbe7546504d63f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `oraclelinux:7.9` - linux; amd64

```console
$ docker pull oraclelinux@sha256:7bd67d839b5296423b49806513e985d1440c1666732bdab49d8fe4f2eaa8882e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.4 MB (95379377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27eb3f6a5a2ea765d10a69fcc8cdf5e8d551d46aad900344db5a30bc2790f925`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 10 Dec 2024 23:51:26 GMT
ADD oraclelinux-7-amd64-rootfs.tar.xz / # buildkit
# Tue, 10 Dec 2024 23:51:26 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:7e97d888e3ce798d1fd4f6290ab2faa2e76d131b997de8abd0073b19ce89ff9e`  
		Last Modified: Wed, 11 Dec 2024 20:29:27 GMT  
		Size: 95.4 MB (95379377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `oraclelinux:7.9` - unknown; unknown

```console
$ docker pull oraclelinux@sha256:48cbf9d2b2eb4e8b49abbc4a5ee884bbd4e38d9a7775f32d23521d4cb4ec9334
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5986658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca2d2f842db34aaa9439decd84f84e8cdd5677d3ec53e95365d21157d33f121f`

```dockerfile
```

-	Layers:
	-	`sha256:27e4fd6dc2a746095a9d3bda1f23775ebdee67e2f23c01fdc355d4073032ea97`  
		Last Modified: Wed, 11 Dec 2024 20:29:26 GMT  
		Size: 6.0 MB (5981509 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c096aa08ec8ef96172085216ad2f1438f843a0454bec76e639965c1886237f5d`  
		Last Modified: Wed, 11 Dec 2024 20:29:26 GMT  
		Size: 5.1 KB (5149 bytes)  
		MIME: application/vnd.in-toto+json

### `oraclelinux:7.9` - linux; arm64 variant v8

```console
$ docker pull oraclelinux@sha256:fa93b39b22ba5975b662591e71d508b060c06a60b0dd149aedd57e8832dee1bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.3 MB (97327013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1819ead03a2e5166f44a38f549f069a3b0a7d2987fb565b8c5165cf40e5bf2f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 10 Dec 2024 23:52:16 GMT
ADD oraclelinux-7-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 10 Dec 2024 23:52:16 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:9d7edc91d9d8dde556a51cc4cb7cfc1cfea1a0c15f6388ab6c8b583c8f8c42c8`  
		Last Modified: Wed, 11 Dec 2024 20:30:26 GMT  
		Size: 97.3 MB (97327013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `oraclelinux:7.9` - unknown; unknown

```console
$ docker pull oraclelinux@sha256:382ad209af84477ee4b3dc4bcfee2f50041252a10cf71d5e0499285ae44489b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5980190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b4bf0b4acbd52c5c2c36018b0f5310d7d7d5d8905633d958151bfdf0286fe62`

```dockerfile
```

-	Layers:
	-	`sha256:808b3b6e809d50e57eab82cabcc5d37acf7266bcdf087589d1ad337a77ffd5d5`  
		Last Modified: Wed, 11 Dec 2024 20:30:24 GMT  
		Size: 6.0 MB (5975000 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa0fb3a85603ebc1f4a6e7cb274bcb060fdd154bd987a2f2ee1d7d3022548e50`  
		Last Modified: Wed, 11 Dec 2024 20:30:23 GMT  
		Size: 5.2 KB (5190 bytes)  
		MIME: application/vnd.in-toto+json

## `oraclelinux:8`

```console
$ docker pull oraclelinux@sha256:f3759153ce4cef654e67bf179b8dfdab460f2461069f4c1e08df9b79b108988a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `oraclelinux:8` - linux; amd64

```console
$ docker pull oraclelinux@sha256:3366ea7c43d66d9db1bf44f30b6965cf185932d4900497490c69b83771b65851
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.0 MB (101003699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aace8e4fc9e3b84c52d09d21f81443ae0e7a9adeaf087b8f80aba01cefb18d51`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 04 Feb 2026 00:25:30 GMT
ADD oraclelinux-8-amd64-rootfs.tar.xz / # buildkit
# Wed, 04 Feb 2026 00:25:30 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:01bf239208e3dcdfa794ce14fbcbf507c545cc8939114de02a7d3d3572955951`  
		Last Modified: Wed, 04 Feb 2026 00:25:51 GMT  
		Size: 101.0 MB (101003699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `oraclelinux:8` - unknown; unknown

```console
$ docker pull oraclelinux@sha256:dba783cf03a889d89a37eb3ac4ff7abcfd9a735b3402e119112c7263bbc02289
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6147528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f52849f09384bc35f28a8fdce949e43f8f4ed29d134b3fdf12844664e52969f0`

```dockerfile
```

-	Layers:
	-	`sha256:74e7ab8de79e47162706b34d14b15a1917503b0d513c75ba7223c437b13b25ab`  
		Last Modified: Wed, 04 Feb 2026 00:25:49 GMT  
		Size: 6.1 MB (6142419 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0777887935d0ceee772af154ec4697b6c2d9c4549dbef8cff42ad232f625256`  
		Last Modified: Wed, 04 Feb 2026 00:25:48 GMT  
		Size: 5.1 KB (5109 bytes)  
		MIME: application/vnd.in-toto+json

### `oraclelinux:8` - linux; arm64 variant v8

```console
$ docker pull oraclelinux@sha256:f41d7a939cea930d9b8dcbd156cfb239b4f2694d85c10340b5d80a27541d304c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.9 MB (99897033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0be70e54e93cb0e1736d5c9de74943e890ba2e680427709e810a3295398809f4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 04 Feb 2026 00:24:36 GMT
ADD oraclelinux-8-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 04 Feb 2026 00:24:36 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f7746540d69ea689934b73e1d70007e8e5be184547e6705477f2c5aacee9a1d5`  
		Last Modified: Wed, 04 Feb 2026 00:24:57 GMT  
		Size: 99.9 MB (99897033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `oraclelinux:8` - unknown; unknown

```console
$ docker pull oraclelinux@sha256:348844ca7c81dde3e4f0be1a8c5fb9c765bf7a3b439551da0fe89c62eb8c954e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6148349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fc5e2d80233f4a8527f043d42fac1c22672f9e1121031634bf8234195086696`

```dockerfile
```

-	Layers:
	-	`sha256:15a0b6b3c87ab7e38cbbb31a6b8f755c0b54eec1b420a9e6c26954f6c6f185c2`  
		Last Modified: Wed, 04 Feb 2026 00:24:56 GMT  
		Size: 6.1 MB (6143200 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c3219042fa2f96d6bf3f8c022bf10ab8b83936b7baf19f73de917d0fd5a0043`  
		Last Modified: Wed, 04 Feb 2026 00:24:55 GMT  
		Size: 5.1 KB (5149 bytes)  
		MIME: application/vnd.in-toto+json

## `oraclelinux:8-slim`

```console
$ docker pull oraclelinux@sha256:eebba903b134f493390e8f41c0bc90e8a8bb4c3ddd24f9cbbc2281d5a02bd113
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `oraclelinux:8-slim` - linux; amd64

```console
$ docker pull oraclelinux@sha256:4fdec3a94a1942d25c4568ac84a57f0c58176fbf4fc6a2d172ecb976c18ff507
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.5 MB (51467065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b90dbca955c063e0ad0d5166af14307deda903a698a91f91e6f091c965435b4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 26 Jan 2026 22:04:10 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 26 Jan 2026 22:04:10 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:70f5c9ee868f124c508277177dfd78acddb8ada1f704dc8be2b2cdd99836131c`  
		Last Modified: Mon, 26 Jan 2026 22:04:22 GMT  
		Size: 51.5 MB (51467065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `oraclelinux:8-slim` - unknown; unknown

```console
$ docker pull oraclelinux@sha256:7d9d9dfe2af498c517c35c621ef362217386ac84f1252d281aaf7c8757dccb9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2089642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24e0ad55da7c274a75b171f4265d4d08022597dc9ac1fbdd49e82a2895509ec3`

```dockerfile
```

-	Layers:
	-	`sha256:de410bd515ec9c945aa60a46ce469064d42f4b881fe921b7b13d41acddeb1c8f`  
		Last Modified: Mon, 26 Jan 2026 22:04:20 GMT  
		Size: 2.1 MB (2084804 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a9aa0eb686c9c200f18c4628f95d73d4099a99aa906793b3fd45dd96b0bad03`  
		Last Modified: Mon, 26 Jan 2026 22:04:20 GMT  
		Size: 4.8 KB (4838 bytes)  
		MIME: application/vnd.in-toto+json

### `oraclelinux:8-slim` - linux; arm64 variant v8

```console
$ docker pull oraclelinux@sha256:40df698cb4f0424fe0b2167f8fae60d19b3a7e79f68da8a506fa6b07d0f2ba4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 MB (50197120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cfb87964bcfd3bcae679762fed0c53161260f747c489ac740b3e8ca5aa3e1a8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 26 Jan 2026 22:07:11 GMT
ADD oraclelinux-8-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 26 Jan 2026 22:07:11 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:3e76a047bd66be5e3e8818d893725279bf9a5b8a583db4b258f0d16df8850a42`  
		Last Modified: Mon, 26 Jan 2026 22:07:23 GMT  
		Size: 50.2 MB (50197120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `oraclelinux:8-slim` - unknown; unknown

```console
$ docker pull oraclelinux@sha256:f4a2ce31a4ac670989fc55b790c65e4a19f0f95eea5af271dedd039f907cd3bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2089072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b390ca48e4a8fb4d166f42f50249ceb23abaa0401dbf8e23b5d67ee8028f4944`

```dockerfile
```

-	Layers:
	-	`sha256:83b2b1222d4bf71093921ee3acb1d12984310fb664b9b8902a6c388b9180b75b`  
		Last Modified: Mon, 26 Jan 2026 22:07:21 GMT  
		Size: 2.1 MB (2084202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:187f542e6c5b1bb4bb19f253097e67f68c6c23834055f0b4c53866a27bac90c4`  
		Last Modified: Mon, 26 Jan 2026 22:07:21 GMT  
		Size: 4.9 KB (4870 bytes)  
		MIME: application/vnd.in-toto+json

## `oraclelinux:8-slim-fips`

```console
$ docker pull oraclelinux@sha256:c2ef6db63d63f65a9afb45c113d3804353db87964bf346c3d87c8eaac05c7e14
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `oraclelinux:8-slim-fips` - linux; amd64

```console
$ docker pull oraclelinux@sha256:872622b8330a0023cea91e7e1910111300c1ff89a5a4c4da226e3279b6df4311
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.5 MB (51468156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d26e9fae7d9d1e34c5c28c275d1182bb819f1ece79679d1d706c4f43617a4f7a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 26 Jan 2026 22:08:15 GMT
ADD oraclelinux-8-slim-fips-amd64-rootfs.tar.xz / # buildkit
# Mon, 26 Jan 2026 22:08:15 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:c1dc5cd9894a0b69e84f4529f740257009af0dd3cd163581205f60e9de47965a`  
		Last Modified: Mon, 26 Jan 2026 22:08:27 GMT  
		Size: 51.5 MB (51468156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `oraclelinux:8-slim-fips` - unknown; unknown

```console
$ docker pull oraclelinux@sha256:d2f678e23e38b2be9f510698bb6b1f1fcb7ed8a57a44baec9253b00d24368982
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2096018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:627a2d8c906cf873e0cd524973f83a3101ef4cc669ee32bb51e15d3adb5f090a`

```dockerfile
```

-	Layers:
	-	`sha256:0cdeefb03363c9abfe53565312e9a54108729bfef36be8f187460bbe4a0dc530`  
		Last Modified: Mon, 26 Jan 2026 22:08:26 GMT  
		Size: 2.1 MB (2091142 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c1c05b071a55cb1e32029a242b1649d084e563e283d50ee1239355888aba167`  
		Last Modified: Mon, 26 Jan 2026 22:08:25 GMT  
		Size: 4.9 KB (4876 bytes)  
		MIME: application/vnd.in-toto+json

### `oraclelinux:8-slim-fips` - linux; arm64 variant v8

```console
$ docker pull oraclelinux@sha256:0cf7a76b90d9c6c42a4d65af5c74c9996fdaa028de8915be1e10e0462bf56fac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 MB (50196287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5daae860c658583cb0b00e136c9652920e1bcc56c5c568a702300a1e5f712e7c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 26 Jan 2026 22:05:16 GMT
ADD oraclelinux-8-slim-fips-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 26 Jan 2026 22:05:16 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:83b1ff1c7b4492d99ad00d343220ed4581711569b62bcc3b79908f007e1bb390`  
		Last Modified: Mon, 26 Jan 2026 22:05:28 GMT  
		Size: 50.2 MB (50196287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `oraclelinux:8-slim-fips` - unknown; unknown

```console
$ docker pull oraclelinux@sha256:459494727256cb7dd370e9704f7dd037b5f7098b53f0385a7e4716f2092083a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2095449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95b1f440777133fc9296559e71fa47a16e04c07806eb8a2708bd9b6f069aee97`

```dockerfile
```

-	Layers:
	-	`sha256:bb5d1e0d9b3ebd736084c464aa746082f34c7db5438a875bd16147deed54e8f6`  
		Last Modified: Mon, 26 Jan 2026 22:05:26 GMT  
		Size: 2.1 MB (2090540 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:501c910f29e37113c3162cc283d6e9ac5c0f33ab524580e37f0dd6a21d55e0a7`  
		Last Modified: Mon, 26 Jan 2026 22:05:26 GMT  
		Size: 4.9 KB (4909 bytes)  
		MIME: application/vnd.in-toto+json

## `oraclelinux:8.10`

```console
$ docker pull oraclelinux@sha256:f3759153ce4cef654e67bf179b8dfdab460f2461069f4c1e08df9b79b108988a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `oraclelinux:8.10` - linux; amd64

```console
$ docker pull oraclelinux@sha256:3366ea7c43d66d9db1bf44f30b6965cf185932d4900497490c69b83771b65851
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.0 MB (101003699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aace8e4fc9e3b84c52d09d21f81443ae0e7a9adeaf087b8f80aba01cefb18d51`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 04 Feb 2026 00:25:30 GMT
ADD oraclelinux-8-amd64-rootfs.tar.xz / # buildkit
# Wed, 04 Feb 2026 00:25:30 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:01bf239208e3dcdfa794ce14fbcbf507c545cc8939114de02a7d3d3572955951`  
		Last Modified: Wed, 04 Feb 2026 00:25:51 GMT  
		Size: 101.0 MB (101003699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `oraclelinux:8.10` - unknown; unknown

```console
$ docker pull oraclelinux@sha256:dba783cf03a889d89a37eb3ac4ff7abcfd9a735b3402e119112c7263bbc02289
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6147528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f52849f09384bc35f28a8fdce949e43f8f4ed29d134b3fdf12844664e52969f0`

```dockerfile
```

-	Layers:
	-	`sha256:74e7ab8de79e47162706b34d14b15a1917503b0d513c75ba7223c437b13b25ab`  
		Last Modified: Wed, 04 Feb 2026 00:25:49 GMT  
		Size: 6.1 MB (6142419 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0777887935d0ceee772af154ec4697b6c2d9c4549dbef8cff42ad232f625256`  
		Last Modified: Wed, 04 Feb 2026 00:25:48 GMT  
		Size: 5.1 KB (5109 bytes)  
		MIME: application/vnd.in-toto+json

### `oraclelinux:8.10` - linux; arm64 variant v8

```console
$ docker pull oraclelinux@sha256:f41d7a939cea930d9b8dcbd156cfb239b4f2694d85c10340b5d80a27541d304c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.9 MB (99897033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0be70e54e93cb0e1736d5c9de74943e890ba2e680427709e810a3295398809f4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 04 Feb 2026 00:24:36 GMT
ADD oraclelinux-8-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 04 Feb 2026 00:24:36 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f7746540d69ea689934b73e1d70007e8e5be184547e6705477f2c5aacee9a1d5`  
		Last Modified: Wed, 04 Feb 2026 00:24:57 GMT  
		Size: 99.9 MB (99897033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `oraclelinux:8.10` - unknown; unknown

```console
$ docker pull oraclelinux@sha256:348844ca7c81dde3e4f0be1a8c5fb9c765bf7a3b439551da0fe89c62eb8c954e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6148349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fc5e2d80233f4a8527f043d42fac1c22672f9e1121031634bf8234195086696`

```dockerfile
```

-	Layers:
	-	`sha256:15a0b6b3c87ab7e38cbbb31a6b8f755c0b54eec1b420a9e6c26954f6c6f185c2`  
		Last Modified: Wed, 04 Feb 2026 00:24:56 GMT  
		Size: 6.1 MB (6143200 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c3219042fa2f96d6bf3f8c022bf10ab8b83936b7baf19f73de917d0fd5a0043`  
		Last Modified: Wed, 04 Feb 2026 00:24:55 GMT  
		Size: 5.1 KB (5149 bytes)  
		MIME: application/vnd.in-toto+json

## `oraclelinux:9`

```console
$ docker pull oraclelinux@sha256:895f1dd2a54d3b1aebe86b4a87c19de0d42c7892157872275acd483c8358318a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `oraclelinux:9` - linux; amd64

```console
$ docker pull oraclelinux@sha256:49f6b565ac40902f723a4c9a4b6a50cacaea91ab6efd827331ebcd17bccef6a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.0 MB (94040168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cbc06bef2da2d9443d6ba0c840de2a70088ac06383215de4a1a8af366b4a2f5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 30 Jan 2026 23:39:03 GMT
ADD oraclelinux-9-amd64-rootfs.tar.xz / # buildkit
# Fri, 30 Jan 2026 23:39:03 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:97c90c85b2190f1e0dd01947c704916c52dd5d174f3afbbc332a2d7937eb194d`  
		Last Modified: Fri, 30 Jan 2026 23:39:22 GMT  
		Size: 94.0 MB (94040168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `oraclelinux:9` - unknown; unknown

```console
$ docker pull oraclelinux@sha256:70fdb092f161b0cd43c33fe07d70adae5e575a9787bd1c96889ebd33f547cd93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5743669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bbd1946861eb971dd3f672dcddc10922074a2b226913165c47c916f73e5f318`

```dockerfile
```

-	Layers:
	-	`sha256:9fe1d5c0cbcbbdef2b23f9e7ad66b5a1f9dfd40b80eb724705f8e3d990554075`  
		Last Modified: Fri, 30 Jan 2026 23:39:19 GMT  
		Size: 5.7 MB (5738865 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6bff378d795bd5e6f1d47a0aac683c46db40e92bae47be77fb6e161dd2f78be`  
		Last Modified: Fri, 30 Jan 2026 23:39:19 GMT  
		Size: 4.8 KB (4804 bytes)  
		MIME: application/vnd.in-toto+json

### `oraclelinux:9` - linux; arm64 variant v8

```console
$ docker pull oraclelinux@sha256:cb157c68b5700c7ddf257d59f296ed947ff06d9d851dad400dc6035d0eec157f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.4 MB (92431451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa81f7d2421c00ef9a96348a704a7cb3f9fe297b299f34d4a3464181c117af2d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 30 Jan 2026 23:38:54 GMT
ADD oraclelinux-9-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 30 Jan 2026 23:38:54 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:80c7dde0e69e83cb4f813db5665cd45c9bc56d95d6c92c9966d9e8421dd06b80`  
		Last Modified: Fri, 30 Jan 2026 23:39:15 GMT  
		Size: 92.4 MB (92431451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `oraclelinux:9` - unknown; unknown

```console
$ docker pull oraclelinux@sha256:b01f3d515b668f5884e3fc952ccac92e43a22494f3817a6117762ae9124ff111
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5743242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baf9764930b5096d643dad54331fc576755ecdfd6dd7b8eceb9d46a204a22a5b`

```dockerfile
```

-	Layers:
	-	`sha256:7261ec448abc3f3b1dfd6258e30b07cdde02cf3aa9c61745bc02e3abefa3c5b7`  
		Last Modified: Fri, 30 Jan 2026 23:39:13 GMT  
		Size: 5.7 MB (5738409 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:105524e7de17da94ab2b5e1159bad83256104b57043a432315f26eddc008be4f`  
		Last Modified: Fri, 30 Jan 2026 23:39:12 GMT  
		Size: 4.8 KB (4833 bytes)  
		MIME: application/vnd.in-toto+json

## `oraclelinux:9-slim`

```console
$ docker pull oraclelinux@sha256:cf3e70b1e12805e0888b95914d6deeb1fb6cc232093f91928a853bca5702a166
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `oraclelinux:9-slim` - linux; amd64

```console
$ docker pull oraclelinux@sha256:54903c4e02e29aea64e0bad16366cdfaa0f1734ecf720f22a7db25d76fabe217
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47313808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d8a664bc89c616374f6a9d4b1d9708a6d750ad8a50e050a503a3d3e1a2ec84e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 30 Jan 2026 23:39:45 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 30 Jan 2026 23:39:45 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:c21bb7e51cd3b6a6786c5cece22bd0b261e4bf013a53ecb6f4dce35d38c40f23`  
		Last Modified: Fri, 30 Jan 2026 23:39:56 GMT  
		Size: 47.3 MB (47313808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `oraclelinux:9-slim` - unknown; unknown

```console
$ docker pull oraclelinux@sha256:60e12afff164e25fd9a18742138dc0a649a1f8b9d2a92fb6defed54f4677661d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2205486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6590451725b8942a6fa0174678710f92a1f4d420f6b40fdbb63d53f58b62437`

```dockerfile
```

-	Layers:
	-	`sha256:d6d24d9f132c26fcd66995e4323843ecedb3cb6c272f36014ba18d919d69c08f`  
		Last Modified: Fri, 30 Jan 2026 23:39:55 GMT  
		Size: 2.2 MB (2200649 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e6dc495316399e774627c69828eea9e22e55c4e9be26d927ea2d19109ea8ac2`  
		Last Modified: Fri, 30 Jan 2026 23:39:54 GMT  
		Size: 4.8 KB (4837 bytes)  
		MIME: application/vnd.in-toto+json

### `oraclelinux:9-slim` - linux; arm64 variant v8

```console
$ docker pull oraclelinux@sha256:96b30073e369c323e2cbf210056a1193949072b3d9bffe438bcca93fff3d1496
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45901641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7cda3de68f5e1b5be34046143fc61465411351ec80891346967108765a996e1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 30 Jan 2026 23:39:10 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 30 Jan 2026 23:39:10 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:9490d79385bda9b2c792f8c72c8b1a55f5d14188d676eda2ed07199c47f59396`  
		Last Modified: Fri, 30 Jan 2026 23:39:22 GMT  
		Size: 45.9 MB (45901641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `oraclelinux:9-slim` - unknown; unknown

```console
$ docker pull oraclelinux@sha256:55835a7b8e97268fd700217278523fe50988249df49b72439368021ec199bce4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2204932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb27c927ab078fc6e427eacfcd947157c18615231b58541c8e9e01e512e7026b`

```dockerfile
```

-	Layers:
	-	`sha256:93192bcd5ac0b42fbcef0d9a36ae53c5eee574bcd2911ddf01c9e83530139eda`  
		Last Modified: Fri, 30 Jan 2026 23:39:21 GMT  
		Size: 2.2 MB (2200061 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f1c16fb980fd96f15611fff92feda274584240bb0f461448aa6f33de45c9fdb`  
		Last Modified: Fri, 30 Jan 2026 23:39:21 GMT  
		Size: 4.9 KB (4871 bytes)  
		MIME: application/vnd.in-toto+json

## `oraclelinux:9-slim-fips`

```console
$ docker pull oraclelinux@sha256:355434168dfc9c72d4b29f7aec7479f1d2723b4030bd51793f113c2331b79d4c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `oraclelinux:9-slim-fips` - linux; amd64

```console
$ docker pull oraclelinux@sha256:1bd3299b220700a8cd76730e56d6a7790281e02fc5f0c64dcd0b132090656c77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49467989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6480aa4b3c9449faf5f3a4068e3acbe5de4951776fcae4e633641be71ad7dbf6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 30 Jan 2026 23:39:58 GMT
ADD oraclelinux-9-slim-fips-amd64-rootfs.tar.xz / # buildkit
# Fri, 30 Jan 2026 23:39:58 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:8be0bee6ceccad5f1ea9b494c5accc00e2023fe54cc96a7afa93f0aab1dc56e6`  
		Last Modified: Fri, 30 Jan 2026 23:40:09 GMT  
		Size: 49.5 MB (49467989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `oraclelinux:9-slim-fips` - unknown; unknown

```console
$ docker pull oraclelinux@sha256:f57eda560c3efc305ca6beeed4a305802018ea969a9a7f73d460e691c3c5c9fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2213278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:083eeadac5f05242f7df979722ae3b5f5eb33e58a1002710b339abbb0478a1f4`

```dockerfile
```

-	Layers:
	-	`sha256:7b4399711ccebca5d00279620f03159b16dace0e69845344151093f89c491e3f`  
		Last Modified: Fri, 30 Jan 2026 23:40:08 GMT  
		Size: 2.2 MB (2208402 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83936fc801b3f96f54c53821bac3ae608c86e0a8aa1a4d4a83ee8923f76c7d05`  
		Last Modified: Fri, 30 Jan 2026 23:40:08 GMT  
		Size: 4.9 KB (4876 bytes)  
		MIME: application/vnd.in-toto+json

### `oraclelinux:9-slim-fips` - linux; arm64 variant v8

```console
$ docker pull oraclelinux@sha256:11b59b04f5bf4bdd7546b8da7050c5f91c3f4fd9d0c5db5aeb21a351bbb5890a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.9 MB (47942661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd8534c9e309fbda562bf2efa21e5fd37f789fa46e64caf0c8811b69678bb4d7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 30 Jan 2026 23:39:22 GMT
ADD oraclelinux-9-slim-fips-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 30 Jan 2026 23:39:22 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:db7d0d9e9d7d6b9f5c3184bdae59d76d30099228e376cb9c9c2b3d38adf00045`  
		Last Modified: Fri, 30 Jan 2026 23:39:33 GMT  
		Size: 47.9 MB (47942661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `oraclelinux:9-slim-fips` - unknown; unknown

```console
$ docker pull oraclelinux@sha256:f2795d9c71e44041f0b11d632c27c7c9c32fbc801b30180a3f335930e02398c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2212723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:487d40bf3e8e592a6fab15fe907b7e1309d454253a795cc6fbb116ef437e2280`

```dockerfile
```

-	Layers:
	-	`sha256:098b57abe598e67787c3ad1ce2acea0a434ab21b4510114b3e6aeacdb9cd0d4e`  
		Last Modified: Fri, 30 Jan 2026 23:39:32 GMT  
		Size: 2.2 MB (2207814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40dfd423cb059f6cf2163b28edfbc6e4c7401c7ae68eced26df24edff34a7438`  
		Last Modified: Fri, 30 Jan 2026 23:39:32 GMT  
		Size: 4.9 KB (4909 bytes)  
		MIME: application/vnd.in-toto+json
