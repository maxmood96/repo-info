## `buildpack-deps:sid-curl`

```console
$ docker pull buildpack-deps@sha256:e66013cf9a798b56bd939a28daa9b16194483b066eb6538c852f5d9a03e2c23b
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

### `buildpack-deps:sid-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:654513afd24124c5268771565fd51383c1fd9c0f99418ed0d2edb95931800554
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.9 MB (74886854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77cdb0a9def6cb7b0386a8391ac13c5b122fc34dd110daeb4469148605a2e0f0`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1751241600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
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

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:45b2382862ae5fea93784e968e24b713b101ab3ed5c945358893c804e681177b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4123152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ba1b3c3e18944708504d4344276b111d2a6dde0df6e17fe396317d87c5b4f06`

```dockerfile
```

-	Layers:
	-	`sha256:562cf80b8109bd1774485edd87c58f7f8a7c689f665a42ff8c84ce566eb1f714`  
		Last Modified: Tue, 01 Jul 2025 04:20:48 GMT  
		Size: 4.1 MB (4116348 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28af60a53eca2b641a4e7099ac92c04cde933992f292ae4df4441de7c28da685`  
		Last Modified: Tue, 01 Jul 2025 04:20:49 GMT  
		Size: 6.8 KB (6804 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:630c0778a69fc1868f74cf35894c9cbe64255d2e8ec05dbffd1f0661a6841db3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.8 MB (71786175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87f475fe057a040310dfe20e2425f15d85993fc1ae95b4f1ff5d96d02fa4aff0`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armel' out/ 'sid' '@1751241600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
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

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:29a28eadad233807f16f815773b1458cf1cf6f9588a8e4b07b06c6887199a52a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4135447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbd4cbde955ced7a3fcef7079d76edc0c8e7324441eaf6323e7e5036cda290cc`

```dockerfile
```

-	Layers:
	-	`sha256:5bd4a2f12665468d354d70e0593c2ef2d8ebff0e71c3d6613d269021b681dfca`  
		Last Modified: Tue, 01 Jul 2025 07:21:10 GMT  
		Size: 4.1 MB (4128583 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11ca10edd7e6ee7cfc2cfb0632444f5c8312c52c7e8934facc5ffcfdb3c7721e`  
		Last Modified: Tue, 01 Jul 2025 07:21:10 GMT  
		Size: 6.9 KB (6864 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:d9cab4bae937e1a9a556cc1a2be131686d95d0595cffe70a7134db830ba6c010
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.3 MB (69327517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe1071b9e28b74204bf052d34ac7afbfd2d6902a40438875f4fd70107f9f7d12`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armhf' out/ 'sid' '@1751241600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
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

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e6a0fb9b465963c4b49f77fae203fda272cc7799b1caa43d567c2556830fc162
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4124705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bed24cc15142a1deecf9182c07bd53d0b75e02fe7ba93db1f3f9b349cc19b2cd`

```dockerfile
```

-	Layers:
	-	`sha256:73e49c594ee7f0804f1c4f24e0ad5ea8dd42d706ac778eee79f314f7e3319c28`  
		Last Modified: Tue, 01 Jul 2025 10:20:34 GMT  
		Size: 4.1 MB (4117841 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97d0c3e76fa6f618a44eeeb89e7cbc9bbf41a362625a217bd19f2105372703e1`  
		Last Modified: Tue, 01 Jul 2025 10:20:35 GMT  
		Size: 6.9 KB (6864 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:b20b44e51f48f8752bb4c1d6acea85bbd2c4e352e354708481301d5fc2dae829
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.6 MB (74643263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b8bd60c27d46a8f046bea2215343551122fc75d49074448b209e40d4ef3a2a9`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1751241600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
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

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:87e4daf789c55c1798a03813c878118a3624c6ceeabcefda36c0c32bb65f3252
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4124762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a42905f5297bb644e092245d20e43edc942e1c1c0856e3721c16c3de33357168`

```dockerfile
```

-	Layers:
	-	`sha256:0bed3745c261ef5806c0c4a78382d1af1b15754b04d465b8976c5ab72657b4c1`  
		Last Modified: Tue, 01 Jul 2025 07:21:19 GMT  
		Size: 4.1 MB (4117878 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0ccd434767c043b67820e4500995a05a329db18036975208cd0895729437901`  
		Last Modified: Tue, 01 Jul 2025 07:21:20 GMT  
		Size: 6.9 KB (6884 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:4848cb8958e59c8a99bac261484cac96913f11a63b6407b912418b851cca5a19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.6 MB (77564681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78f13fba4530d699681e350a1a6046a40b1734a761458d39fc34fee8a39e2a6f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1751241600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
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

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5ab817c95a9a87697518b7f53cc6d7b9eab350c517fc22d6e195563bd930bf27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4120244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54c4d23417ce2440b19b36f28dfcc8baec06b1517d5f9bd05fd8a728f0bf8807`

```dockerfile
```

-	Layers:
	-	`sha256:7db5376dca3bb6b0daed7846deacb032e32aa5501c1a7af5a30b436ab76fd363`  
		Last Modified: Tue, 01 Jul 2025 04:21:02 GMT  
		Size: 4.1 MB (4113462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa89909bfb0ee9f9f14e0ab57c5eec90906fc5bc279788fbde05eb1d31e7bdb9`  
		Last Modified: Tue, 01 Jul 2025 04:21:02 GMT  
		Size: 6.8 KB (6782 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:e2c805eb6f882372069e75e9c64f99160a769216e17e00d7e07bff601fb2e0ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.2 MB (75227314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdad3505afb3952378033d688512a061a7c5318bf6608fa7fa6e7447cb74df5c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'mips64el' out/ 'sid' '@1751241600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
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

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c11e4ccd966b2e70347bb4f156d87e7d0d0478003cc6280217acf9cb88c15a5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 KB (6636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61755fc1ffa6c0a3b661bac959c85c5b65c324cd9587734710ec3ee5e482e30f`

```dockerfile
```

-	Layers:
	-	`sha256:6099e5e0da142bc091c70501c2e2f017a0ca73c2c2a773e0739fa4d27457891c`  
		Last Modified: Tue, 01 Jul 2025 19:20:56 GMT  
		Size: 6.6 KB (6636 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:f878e5d283102a2e5f00d5c812985d13abf72a6ec93b8598b8bae9ec11bc518d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.1 MB (80104888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b876f4218fbf00f3d2c2d6b9e50be7eac4fe336f0a9b7244e358d04724e005e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'sid' '@1751241600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
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

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2dd56c3cc42cdd7b61f1aab9bb265fe1bc9e8a6d0144ec8e3083af926a9629bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4136275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aedf605e8ee2d24d3a9de2dc83618f16a1ced742fe6e635f653f68f81eb0228e`

```dockerfile
```

-	Layers:
	-	`sha256:b7ae15f8495923f2658ed6d11b6ba0b665b840bd4947e8fe0f62a9aa6c799006`  
		Last Modified: Tue, 01 Jul 2025 07:21:31 GMT  
		Size: 4.1 MB (4129439 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6a4dd0699f9b7553c3ba0ffeac2e05c1c2446c576fb35e6de4883ed4e22c66b`  
		Last Modified: Tue, 01 Jul 2025 07:21:31 GMT  
		Size: 6.8 KB (6836 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:d0634f4ca8ef432fe4e5a6f97834ef6566193409b32f7c3545333962aac7515c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72710402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f373cc57bcde4de73b79210120045874c92075ae5e2f932ef82dc84b996c4ec0`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1751241600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
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

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5497e20292f151afda9297e6e3184eaa7a156b1d6d42049ae82baf9cbc06f652
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4115685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00ac6cb738fc2a1e1dd7a3330ca224ad0b1bb727bbe6dd2198be9bf7f5b6875c`

```dockerfile
```

-	Layers:
	-	`sha256:e127e6ba2ee46cb75c1b7b09deabdaf0eafb2f8a6023c394dfa6064ede62ad3a`  
		Last Modified: Tue, 01 Jul 2025 04:21:11 GMT  
		Size: 4.1 MB (4108850 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9fa5889f086e2e9067b7dbe415cd146af117731cbaaff83543968cb5625cf1ae`  
		Last Modified: Tue, 01 Jul 2025 04:21:12 GMT  
		Size: 6.8 KB (6835 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:054cdbc61a4d612e7667eb6f8e1b3a2458324358365120dcad22c506b2900368
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76133058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcd226475c39a06ce23e09cc4ed17ee4a7d98dc4e0d8b696349fe3beea2f6956`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 's390x' out/ 'sid' '@1751241600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
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

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ae9515ce8e198c998d1677e974e23eb88161957573a699600ef78cf32ab99d1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4133815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6c77a14be69fb88dc0b2710d9a620a53abf002adbc8654f9bba18b67f5f67a9`

```dockerfile
```

-	Layers:
	-	`sha256:9a2f4740da0d036f138de61c45fa0f651de2e1dbc8facb1ccbd80659c379169c`  
		Last Modified: Tue, 01 Jul 2025 07:21:39 GMT  
		Size: 4.1 MB (4127011 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb1ca1d165afdef254c69b9c855d44f21b9f70bb5d69d9b9d444064fd8fc7116`  
		Last Modified: Tue, 01 Jul 2025 07:21:40 GMT  
		Size: 6.8 KB (6804 bytes)  
		MIME: application/vnd.in-toto+json
