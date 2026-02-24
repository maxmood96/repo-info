## `buildpack-deps:oldstable-curl`

```console
$ docker pull buildpack-deps@sha256:8a6a22d2cad4eb6a80072948d96c30933624b2b7f0ddf17a27f5a500eef270e8
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

### `buildpack-deps:oldstable-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:a12fc26467ebb4b039417912af5b75be98731aeaac7b2e3ad467ce25e7a36576
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72527227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c03f7170e0c39afdcd1d2de66b723e9d62eb84dbce4cc0292fcd688699326ee`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:18:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:6a7e0620566c7dfbe5d3c9a7601d116556ec17a021b3e824f8ab09d12b0c25c6`  
		Last Modified: Tue, 24 Feb 2026 18:42:43 GMT  
		Size: 48.5 MB (48488777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab3b37e4807fe48145826511e16a527bbc4695222ceb966669a4d16729b3b94`  
		Last Modified: Tue, 24 Feb 2026 19:18:52 GMT  
		Size: 24.0 MB (24038450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d15e42c24c3436dd5c7b248c7d451848d306e9224fb42b81988f7421bc58546e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4521151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39fe83ea6cb2710e0f3d2397a4d68220001886cf9c461036fb063d12cd131932`

```dockerfile
```

-	Layers:
	-	`sha256:2720e12fdb8176197169620b0f17e9ad73b940e193405f4a8440d6312f99a53f`  
		Last Modified: Tue, 24 Feb 2026 19:18:51 GMT  
		Size: 4.5 MB (4514334 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1203ca760ee34017448452232f5cebd57fb4762bc70b60e82da98d7bb001b831`  
		Last Modified: Tue, 24 Feb 2026 19:18:51 GMT  
		Size: 6.8 KB (6817 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:2b6395a53f5817e7de239a73f721b54dff2120dd3589cb809595d4757fc08d4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.7 MB (68735481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80358dad00e8949f9970a573deace556e183453a84142e4aaf791da3c0f32bd9`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:55:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:e6dff74bad3c0a4d20c6ddf48bb9ccf82f570d23f324336b4a4e2168c71b093e`  
		Last Modified: Tue, 24 Feb 2026 18:41:45 GMT  
		Size: 46.0 MB (46021660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26d656499e87502826ec64f9b609b22ebce144a3b7eed7bbe76030f651d2bca9`  
		Last Modified: Tue, 24 Feb 2026 19:55:36 GMT  
		Size: 22.7 MB (22713821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:360d401323c5477b0f30647ef8f38a8a4bd7323b96f33aa866c52677d011b8d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4525031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23ca9d7e5431556e6699cc52107310115b431999b712c90a8950ff51c483fda9`

```dockerfile
```

-	Layers:
	-	`sha256:489315edc48d8b192755d5927904839e27d94a7c2f10fbc58c56346ceb5951b1`  
		Last Modified: Tue, 24 Feb 2026 19:55:36 GMT  
		Size: 4.5 MB (4518150 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d27363d18cb3044631bfdf79298a8cd26dfd3ddb22f2306cc217aab43cf2e265`  
		Last Modified: Tue, 24 Feb 2026 19:55:35 GMT  
		Size: 6.9 KB (6881 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:4ab5eba144ea54e77571f7d080302ccdc744a7f5c7ffee354ffc4c7adbc1c8a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.1 MB (66149902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e9f06ffa497387bf1dcab1c72c50f499d8d8ec2f712918ab275b3c6bc698bf2`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 20:01:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:510542cb38bcb0c99cf41f8715bc80ae2e63df19b8399efbb11254ee0ddd4299`  
		Last Modified: Tue, 24 Feb 2026 18:41:53 GMT  
		Size: 44.2 MB (44207818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:122a79376a0d51f606a8d45c17043adef288961e7b30a2332c485fac0427d825`  
		Last Modified: Tue, 24 Feb 2026 20:01:59 GMT  
		Size: 21.9 MB (21942084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:857c29e6e25157da9322295da0f306ed0d3531bd12ddb3f2e57f4826c9d5c729
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4523504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96b3c70966c3316b859e1639ed3201218d13a32d6dcd912b798cb7930bc2c786`

```dockerfile
```

-	Layers:
	-	`sha256:93539304e38b96318810af2fe070aeb1dfc29179bcb9b1959d5ed804914b4855`  
		Last Modified: Tue, 24 Feb 2026 20:01:59 GMT  
		Size: 4.5 MB (4516623 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b74d3dc4c9de2102f57145cc92d8008e0ef17694ec6539c21c8df2c8cb3d112`  
		Last Modified: Tue, 24 Feb 2026 20:01:59 GMT  
		Size: 6.9 KB (6881 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:e6f61b25778a2336e3b3035607ae680add9464ea97b01f0cc73c69a005022814
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.0 MB (71977946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80cc405bac28ee2e5c047dcd1cd52703d8f6939f7816a36776a9a3895a0992ea`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:24:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:8578011282ae3fef36307f7e3afb2265a96bada1a57648f07bea9cc1a11e7b7b`  
		Last Modified: Tue, 24 Feb 2026 18:42:06 GMT  
		Size: 48.4 MB (48373210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:443d4217b87aad21c6acb58313c9038eb24571a4e9f81de2463aaf19d403a640`  
		Last Modified: Tue, 24 Feb 2026 19:24:13 GMT  
		Size: 23.6 MB (23604736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a6e72f7e872d0ab79c9b9c55a812026defd3efa2b1ad313a4753f5276f63fb84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4521492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce1e6865227d361e9589aa73e8b5aa6912698c9618f60d25fdef7494126702c4`

```dockerfile
```

-	Layers:
	-	`sha256:1953767858bec939ca4d490534f571b3164b6d124c5c30a784eacb79702bba44`  
		Last Modified: Tue, 24 Feb 2026 19:24:13 GMT  
		Size: 4.5 MB (4514595 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57fd97baa41688eaba72f20e63a0a7e15a6f0c81989e733060399ff387ea1eac`  
		Last Modified: Tue, 24 Feb 2026 19:24:13 GMT  
		Size: 6.9 KB (6897 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:a1e596aa0c6fe835628e0ec5dd31dbc42b2082a0a9b1aba4be197cc4ec107f3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.3 MB (74349959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c27ba496628b52acb36db23f39742cb9abb35b94f2f987c0e8595c099be0e759`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:24:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:443394a7d911f581670ce4df7959c82f7e8f0be02b5a7ba3c71bc5958012963d`  
		Last Modified: Tue, 24 Feb 2026 18:41:48 GMT  
		Size: 49.5 MB (49477853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e31e1fab6283d72f6ce2de137bc123a8ab89a85f0baa0b6c11c2c6d28c359a32`  
		Last Modified: Tue, 24 Feb 2026 19:24:43 GMT  
		Size: 24.9 MB (24872106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8f55dd6a57453dc369234d8a683d9b877ba1e860e6f24303cdeab7881844bd89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4518247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e721bca8bd0559cf25f004e22c6ec3833b969e6115b47516a5f8d9ecfb9a8368`

```dockerfile
```

-	Layers:
	-	`sha256:532b5643bab03265a29a2746a7235c6a8dddc9455594498a1e753f1b57b7465d`  
		Last Modified: Tue, 24 Feb 2026 19:24:43 GMT  
		Size: 4.5 MB (4511453 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a766bb61d9f4472ae2dc39e90383ebd0ac1dd8fa1492c019a95477199206fd0`  
		Last Modified: Tue, 24 Feb 2026 19:24:42 GMT  
		Size: 6.8 KB (6794 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:1bb6ae512bc58c1894aa2eb1a19f41d084f554a08f953b57da57b5f7a8747295
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.4 MB (72378655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e31eebd11734b71a415b94112964cd9dcb13d72f327c5fe6445047b21692612`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 16:06:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:001d31ce76be3df3174382025b0b9e2985ddc96d785143497e14a46cdcdcf951`  
		Last Modified: Tue, 03 Feb 2026 01:12:32 GMT  
		Size: 48.8 MB (48763257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e910e12f1ba466db5d640f799037fd1161885165d6ef1a46de53b55b08cfb02`  
		Last Modified: Tue, 03 Feb 2026 16:07:24 GMT  
		Size: 23.6 MB (23615398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d570cc7455bee8daa96486154b351200f2b9ec8869f641e438e38e932286e7b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 KB (6650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12a3469add188589ccb7210aac67297261dbfa41ff2b86aefea2af19ebe1b255`

```dockerfile
```

-	Layers:
	-	`sha256:5ee8115be9c0c4dac925d30b372f68f01b467237e1939f379d9a27ce0795e431`  
		Last Modified: Tue, 03 Feb 2026 16:07:22 GMT  
		Size: 6.7 KB (6650 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:60cd2ace15854048bcea8b8d7dce6c6050a61ac2178fdc033f596989d6f6b563
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.0 MB (77998632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d35e3c08d4a980488642dbfac556bd0704d122d3dac918a3c28a9338cf0e5b30`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 05:22:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:5e189aacb842725e8d1d9877c9ab9af09e14901412b6665e179393112b5bca51`  
		Last Modified: Tue, 03 Feb 2026 01:12:57 GMT  
		Size: 52.3 MB (52327289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a1311f6670d65067c1adb8d518ab8836a9d3d42058afdd776824845f91935c9`  
		Last Modified: Tue, 03 Feb 2026 05:22:25 GMT  
		Size: 25.7 MB (25671343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7243c4f1edf7dd4847ca8c3b4eda8b6dc2ca6ed954e328da89ce128b580d5c6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4525809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6b9f18a4d6e8ec3e2ebd5c35992b40eb6c176feb47e499d5b54debbb5225fba`

```dockerfile
```

-	Layers:
	-	`sha256:b56c04fa2553097bbd8bf48b766a006f1d18464c21923ef2135a6cec87288e8c`  
		Last Modified: Tue, 03 Feb 2026 05:22:24 GMT  
		Size: 4.5 MB (4518960 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0292e20d9ba5a3186c9f9bded2bf5836dc4d49527456be0af6da05f7e2d1ab31`  
		Last Modified: Tue, 03 Feb 2026 05:22:24 GMT  
		Size: 6.8 KB (6849 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:2786dd900ac737af64b29b0a0ded45c92d24163ced2a5511846b86edf6d672ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 MB (71181961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb415b89047d95e18ed4647c6844abc5fb59fac43fa40d9930846cac52c2be76`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 20:56:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:00b1871f38dea81b1982e306480bd9f97cedf7b0cb3342e4bc84925e6082ade8`  
		Last Modified: Tue, 24 Feb 2026 18:41:26 GMT  
		Size: 47.1 MB (47148087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1490eda04f0dc8144e02f684cac28c2862b3a584dd3e8ad7e22b96b35409c89`  
		Last Modified: Tue, 24 Feb 2026 20:56:37 GMT  
		Size: 24.0 MB (24033874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e5a7e521c94b254e246ec1a4f1f50308ffd42a7976c3eb25de6c6b4318780b2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4517955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b443c83bd63911336cf8aba3251ad7740677269197a9abb8589d2cba904d8115`

```dockerfile
```

-	Layers:
	-	`sha256:8731012872d0007add5e4b16492d3b4d06a71a97b22177ad0bcbae321440536b`  
		Last Modified: Tue, 24 Feb 2026 20:56:36 GMT  
		Size: 4.5 MB (4511138 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8cd8d36777eb75f6d2e81e58b64960764d2f7f3928c4e695a57c2ba974324f02`  
		Last Modified: Tue, 24 Feb 2026 20:56:36 GMT  
		Size: 6.8 KB (6817 bytes)  
		MIME: application/vnd.in-toto+json
