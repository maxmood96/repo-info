## `buildpack-deps:bookworm-curl`

```console
$ docker pull buildpack-deps@sha256:7b453573e5b0c4a61344ad032d332ed601879d009c96a7e1391afdf1fc6adae6
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

### `buildpack-deps:bookworm-curl` - linux; amd64

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

### `buildpack-deps:bookworm-curl` - unknown; unknown

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

### `buildpack-deps:bookworm-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:60633fe4ccea246f4f567f874511137c21fea99a8cad20bfecf9051626360e54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.7 MB (68718118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55229d29128de79a9cefad1969f9127d19c43f0721d31373d31f33e4f2e5f504`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1759104000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:8f9dd65d850ae18d5d5161e690c6c0b615e72aceac0e3bbc51ed315faf762f0a`  
		Last Modified: Mon, 29 Sep 2025 23:34:08 GMT  
		Size: 46.0 MB (46015582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:050a4079641da2be39571d354108d87d3709c848f35b60ff42118ae57f90dee2`  
		Last Modified: Tue, 30 Sep 2025 01:01:11 GMT  
		Size: 22.7 MB (22702536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:515dabc82cd5f42c8fb701f54f2cfc5399e469eb7d6a943d47d7f33e55a981eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4524431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c36da429de2be717929c4033da1b691dd9455c255cda7c5cba8fc7e03ccfb49`

```dockerfile
```

-	Layers:
	-	`sha256:c2bae0d57b9e5d3935926627c185795e49a8da1a035ac2c965ed85feeaa9c0a2`  
		Last Modified: Tue, 30 Sep 2025 06:35:36 GMT  
		Size: 4.5 MB (4517507 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e852a0d457db75449b6e2f049ac278be94f8626a8af05b011229a408f09c4f2b`  
		Last Modified: Tue, 30 Sep 2025 06:35:37 GMT  
		Size: 6.9 KB (6924 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:fdc9ef8112696d2c0db16d43add7e4c4c101e154b3ab2c4a48f7723b14098b4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.1 MB (66126633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbdb3f9624bc521bd6b1bf7d5f81556cede7658a827e1f04a453148312b0c3ee`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1759104000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:03e514ef7fa283c62434ceaa5569a1dfd7eb8f0bc5744761a741cccd05a62353`  
		Last Modified: Mon, 29 Sep 2025 23:34:15 GMT  
		Size: 44.2 MB (44195923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8de0c6a4c275fbc1127f1e13a9f6de6ca4fdc975838d76828750e675f4b1fd24`  
		Last Modified: Tue, 30 Sep 2025 01:05:07 GMT  
		Size: 21.9 MB (21930710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e4554f77efe736f5b73627663f730b7458837e703277493188182cf5ba027b75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4522904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96017f28d731bb152ebab316b39c38ac12bf6845bd79adf77105e0ee374cef14`

```dockerfile
```

-	Layers:
	-	`sha256:a65bccde503c95fb327363a047acdaa752b0a5275f0dd8e640cf8af8256c5e88`  
		Last Modified: Wed, 01 Oct 2025 19:53:25 GMT  
		Size: 4.5 MB (4515980 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:398fd2d4fb230227fe23d05518b0d57184d2cc3af4d80aaf0a479928e84ce23d`  
		Last Modified: Wed, 01 Oct 2025 19:53:27 GMT  
		Size: 6.9 KB (6924 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; arm64 variant v8

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

### `buildpack-deps:bookworm-curl` - unknown; unknown

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

### `buildpack-deps:bookworm-curl` - linux; 386

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

### `buildpack-deps:bookworm-curl` - unknown; unknown

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

### `buildpack-deps:bookworm-curl` - linux; mips64le

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

### `buildpack-deps:bookworm-curl` - unknown; unknown

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

### `buildpack-deps:bookworm-curl` - linux; ppc64le

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

### `buildpack-deps:bookworm-curl` - unknown; unknown

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

### `buildpack-deps:bookworm-curl` - linux; s390x

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

### `buildpack-deps:bookworm-curl` - unknown; unknown

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
