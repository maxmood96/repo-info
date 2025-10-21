## `buildpack-deps:oldstable-curl`

```console
$ docker pull buildpack-deps@sha256:4166163a83d62f9f3e34a8def07af72bb18cf131006a93f31b86b8754388c596
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
$ docker pull buildpack-deps@sha256:6ec1dd23708af3116dc8086bf7dc0152b6833523c9014f8ac1da7fe1847b2aa6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72506433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6939b87d539c5c2ac6629f088105904730a2717c247bbbbc83b8eca59de8e436`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1759104000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c6b11972fd12973831818babf60f1ffc1c4047507943d132dffc612884022858`  
		Last Modified: Mon, 29 Sep 2025 23:34:14 GMT  
		Size: 48.5 MB (48480557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db3dba6026a3c551d6b8e98308c073fff4fd569fd2fc61f21384cb996da82c9e`  
		Last Modified: Tue, 30 Sep 2025 01:43:53 GMT  
		Size: 24.0 MB (24025876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ad4bd9c2bb1006c1225d6c747476113ab849d8fccc5938197536cc239dba2381
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4520551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0fda2f069101276551971073f6ff29807676c93e1b8207b7026fceaf65a4858`

```dockerfile
```

-	Layers:
	-	`sha256:e5fd547211fc26939343b0587f8aa8549e4e3aac993197805ad52d740df02cad`  
		Last Modified: Tue, 30 Sep 2025 01:19:34 GMT  
		Size: 4.5 MB (4513691 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbe64c14a6059e5af61f211fdcca41ee3b7b9e6bad3aeab372d58f700cf6bef9`  
		Last Modified: Tue, 30 Sep 2025 01:19:35 GMT  
		Size: 6.9 KB (6860 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:792fa54013af03edd3250bd3787252df7a5792d31f1bd70756049cee1dedda7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.7 MB (68720852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bc0d60e010e8906921c5abde44f754f08f6e85843a747115cab83d6220bc9d7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1760918400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d6b0ca95b13ee68ac33e867e046c01d5a40daee1d76922dab47dd1edf2533e94`  
		Last Modified: Tue, 21 Oct 2025 00:19:45 GMT  
		Size: 46.0 MB (46015580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f052363c254a265c1c1981af32f1173b8e1aaed39bd939fefe1c6df9415293e8`  
		Last Modified: Tue, 21 Oct 2025 02:31:20 GMT  
		Size: 22.7 MB (22705272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b0c9eeb081f1fd65b88e5b03b5ac518a4b09d83636f9c79d2515697c79fe16c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4524431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b134f3b4f4466bbcdad07d9d02943837c44e2ad8470f6cc02de518094a7676b9`

```dockerfile
```

-	Layers:
	-	`sha256:df2e01261dbd277a9e088676f18f534e7eeac9c3e84ac7ba363e6ee7af9b6057`  
		Last Modified: Tue, 21 Oct 2025 06:21:21 GMT  
		Size: 4.5 MB (4517507 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eda1152c0400f5a539f5cc58cc5f9fb6347e7917bb6d8c311532a3e9baca90fb`  
		Last Modified: Tue, 21 Oct 2025 06:21:21 GMT  
		Size: 6.9 KB (6924 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:0ee6c37ad86b1ebe3118e4e93f814da9ea7b9c2bb25c1bd90feb6036da703167
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.1 MB (66130415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6ccccb0e64d87419ee311dcd8c1243f1b9e16d77c2dfa98cd474f2d933ef8f7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1760918400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:5dbe800c0d6104b6df988b153994b0d1b5c022197b54cf928820e3c23d00c7eb`  
		Last Modified: Tue, 21 Oct 2025 01:16:21 GMT  
		Size: 44.2 MB (44195910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:178651637d26f6ae6fc6c2a3297b37f8bbef12e80d822930b05b14f51a262382`  
		Last Modified: Tue, 21 Oct 2025 02:43:48 GMT  
		Size: 21.9 MB (21934505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7dbfb28a8f384a49e792c3f6d5886b853c4b3a16b26585c10c85fe20f66660af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4522904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d72cc04e3ee2e3efcb51f7fdded945f2c48dbe09b214bc1b0809654bc12f322e`

```dockerfile
```

-	Layers:
	-	`sha256:dabc53146799a2fbeae743d4d9972c378416f5bed5b7fa422d43ecb99fc944c4`  
		Last Modified: Tue, 21 Oct 2025 07:19:47 GMT  
		Size: 4.5 MB (4515980 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43bbc4bfabe5545c9c7f8f91515896e75d25e2b60813e67c42f723b2511760ad`  
		Last Modified: Tue, 21 Oct 2025 07:19:48 GMT  
		Size: 6.9 KB (6924 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:0c1773b9fe47ddf87f7ad6f73d8e5aa79641b755aead13aa020f943b77365b53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.0 MB (71953649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c31307e8d879112e29874d657d5df59a35bd635a121dcb5cd02ad7d59ebce141`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1759104000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:f7b43f0d0a8b99591b27457b368e70a582002600d32503fd07798c1bee7cd134`  
		Last Modified: Mon, 29 Sep 2025 23:34:16 GMT  
		Size: 48.4 MB (48358915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b261306f7eb1436ff95e3b9d948f5373b0dcf6ca1223aaa4c2fb303b03e744c`  
		Last Modified: Tue, 30 Sep 2025 00:56:21 GMT  
		Size: 23.6 MB (23594734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:003bb6c21a37351cf6d3fbf6085240f0b4f77cac3a54782c57356c390233ff55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4520892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6982b9b0b004c0b6f328d9c33328c1e0351ed4ad3b32f36ea5e9e518c001b3a`

```dockerfile
```

-	Layers:
	-	`sha256:14a3c9ded366b58d40fefce68649c425b34725a5300389f8f67608d18efbb263`  
		Last Modified: Tue, 30 Sep 2025 12:02:04 GMT  
		Size: 4.5 MB (4513952 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e50f10fd5567209ea99fd2558c02d23073a8cd7b52e8c90567785536c1b341c`  
		Last Modified: Tue, 30 Sep 2025 12:02:03 GMT  
		Size: 6.9 KB (6940 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:84484e87b2e152be1d9c0d5616378b02bfa1d1f36c2d91c1aace20d3dbd4e64f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.3 MB (74327286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a178cc29d7d734768bd05050bb2bb8d5303c245f2d0877f7f1c0ee23805c3fd5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1759104000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:2212ccc79525753c3f36994bd936e194dcec09d69b21786be4caa60f697693d8`  
		Last Modified: Mon, 29 Sep 2025 23:34:26 GMT  
		Size: 49.5 MB (49466651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:304a8a7ec291d92cb9effbdbbb7bb5864ca1d87b5e149ee45db584ed39cfc4eb`  
		Last Modified: Tue, 30 Sep 2025 00:20:19 GMT  
		Size: 24.9 MB (24860635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5d03a7e00d48dc3acfb81209a42568054a59dae37d3f32c75e7d896ab1122bc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4517648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f0431b13f52f8619489aaee91a13af5595c71e034da2a10ee925e630123c190`

```dockerfile
```

-	Layers:
	-	`sha256:912bb1842c23af498b00d1d7530d4107095a7791309b3a37ca379ca9816747fc`  
		Last Modified: Tue, 30 Sep 2025 15:25:51 GMT  
		Size: 4.5 MB (4510811 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9635f859e2916ae9c9f91429999974e38a687ac22ac9230998bce22ace02e2aa`  
		Last Modified: Tue, 30 Sep 2025 15:25:52 GMT  
		Size: 6.8 KB (6837 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:4014de4b243442183f70b799bab7fa582f91aa5519e13033bc90ab4e44a290a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.4 MB (72371952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c3d945bdb4378f0c49460c47dc6e4e88a71d90284ef36804f6ca33c431751fb`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1759104000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7eacf7da1d9ca68e46013f3f56395614b995d68904a39e73d4a5bad90579014f`  
		Last Modified: Mon, 29 Sep 2025 23:33:18 GMT  
		Size: 48.8 MB (48760734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:300a1eca9595b83f733381d5f5c6ca135b5d5a79fcdb8204a00ace454f493a78`  
		Last Modified: Tue, 30 Sep 2025 16:39:43 GMT  
		Size: 23.6 MB (23611218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9f7351f5c1f3fa67d4db7c67792cf18bf22c984fb9b6ea94be20ae3fff067b40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 KB (6691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8985acdb0cf29ca1050a8fd24b32126772b8007e7333abbab18509d4946a9fb6`

```dockerfile
```

-	Layers:
	-	`sha256:0d07db8624dcfd2ae36069fab0e972c820428fb0466018ac21523c36baa98e84`  
		Last Modified: Tue, 30 Sep 2025 19:19:51 GMT  
		Size: 6.7 KB (6691 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:f134359dbe48211697d8d6fb4e57af795248f0b619a86d66493ce0dc5a497ca6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.0 MB (77995683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f674d670a7412a865931066d5e370831eb5f3d4de9e67d31d662027e769abdb`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1759104000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:812b25f785969d275d8c3962568c03f83ccc4df31b95f01c0646d79d6d5069f3`  
		Last Modified: Mon, 29 Sep 2025 23:33:30 GMT  
		Size: 52.3 MB (52326764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7f96d9492071bbcb8f94f1c41ed34bb1a985729d6a6ad6f8a6d10f9bd6e3f16`  
		Last Modified: Tue, 30 Sep 2025 02:24:29 GMT  
		Size: 25.7 MB (25668919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e24e8961eecb7dc76bf098555618d2972a3e911aaa73936b56aa0f984c626912
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4525206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78583a1377e800a1d985f8e3877d10e5f4275139b4242d1ba67c16231cf8e286`

```dockerfile
```

-	Layers:
	-	`sha256:478e9bfe169222e8f58b47b3505f0f49170364e7d4628997c9f0973ea00c5561`  
		Last Modified: Wed, 01 Oct 2025 22:03:40 GMT  
		Size: 4.5 MB (4518315 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c971296ef78ecb0af00f14851a6291e2f8e678b4436243a4005f5fdd0443f47f`  
		Last Modified: Wed, 01 Oct 2025 22:03:41 GMT  
		Size: 6.9 KB (6891 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:74a09739c4cf6faa35444fffc3ea17963a7eaff09b11cda2285e52e752e158fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 MB (71161162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9cec9f767a8122d0f042f74a1a8275bbbd525f2ecf9314a682368a1f0196bf5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1759104000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:87d1bec83b35277b636c6e05b9418301b2f025752d7539cecae442f0b94d8fbe`  
		Last Modified: Mon, 29 Sep 2025 23:33:26 GMT  
		Size: 47.1 MB (47137446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa2365377a8d4ecfdf70b8afc073fddfe487283a41bc28927b47a4757047f66c`  
		Last Modified: Tue, 30 Sep 2025 03:09:03 GMT  
		Size: 24.0 MB (24023716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:dace99948766353728ecde9993364acbfc4417f87feb565035c30d8909871e46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4517355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a227a746758e36830eb5cf4545241f4df0492172b2be6d02cd19e6bfab5fe86`

```dockerfile
```

-	Layers:
	-	`sha256:7e3d4c7549befb40b9b0bb755cd56b09993334410370e2a39e5d3414fdc84759`  
		Last Modified: Wed, 01 Oct 2025 02:01:19 GMT  
		Size: 4.5 MB (4510495 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e20ccdd8cb7156eb5e55181aa2947c66a26af217e19b6ab51863909c8ad08bf4`  
		Last Modified: Wed, 01 Oct 2025 02:01:19 GMT  
		Size: 6.9 KB (6860 bytes)  
		MIME: application/vnd.in-toto+json
