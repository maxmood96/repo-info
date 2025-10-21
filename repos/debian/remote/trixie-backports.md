## `debian:trixie-backports`

```console
$ docker pull debian@sha256:d13dd042cce5b0ceac0e917d12718d2de973684d9cbf1d21e61ac3fe9934b423
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
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `debian:trixie-backports` - linux; amd64

```console
$ docker pull debian@sha256:2fa40b88a264a8b641a6c3fd412a5afc63189435e72d7bcfe13e3fa5b16afd46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49285193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a0d9645cd575fa08549eaef7f912ec05b93d1fcf7af909a59e7c7aeb0671bc6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1760918400'
# Mon, 20 Oct 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:795dbedde24d2c72dafd2b71fe36643552e56859c0e29cdb095ed54b825fbaa2`  
		Last Modified: Tue, 21 Oct 2025 00:20:33 GMT  
		Size: 49.3 MB (49284971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37a25ba7a779411b04b1fb3889ab8ab6b9094a5abfc7c8f9d1170d661d2c5abc`  
		Last Modified: Tue, 21 Oct 2025 01:16:44 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:c9fca72f05cf70a924f89ca43e051aad380f0881d1db616c908ae9cf2b5d9194
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3175850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc8122c24eb86598c3ba0afd8b776fba42bf5f35cad23129694c8ab9727ae401`

```dockerfile
```

-	Layers:
	-	`sha256:2d8cfbe23c42de41d75b6c4d225c904196be3a4e556bad48495be33e3d87f60e`  
		Last Modified: Tue, 21 Oct 2025 09:25:52 GMT  
		Size: 3.2 MB (3170024 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:429248c5d31fbe3f6e36606d3d6cb4d49dc4e5fe40aa6c412d02c3175a39b16c`  
		Last Modified: Tue, 21 Oct 2025 09:25:52 GMT  
		Size: 5.8 KB (5826 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:178230729bd5a0661e9387611565e7807c8463beb4965741367fb00bd7900b36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47448993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f965068a98e6760c9bca5f604ed144c7bcb1a8828a9fce4c80ad9802cd71d42`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1760918400'
# Mon, 20 Oct 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:36e1dd9ce5730c29e323bfee77881b6b709a9ef3833ed3a509dabd626e23ef19`  
		Last Modified: Tue, 21 Oct 2025 00:20:35 GMT  
		Size: 47.4 MB (47448771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5be1d42c9ba99d4e2bf224399b9871e5ccdfdbe5a8da90469ab3a242b2e31abe`  
		Last Modified: Tue, 21 Oct 2025 02:05:34 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:993e84693b5597510b707de9fcfa4168162d5b8a4bb349072cc431e1374e2f80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3178844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae3b815ba092f3ea9657f473ff66dd2d7bf2afedfaec5e1b844c1d97aaffd9c7`

```dockerfile
```

-	Layers:
	-	`sha256:ca5b91a7d3b031368da7e15a307a0005486e2e9ceea0b764c74cc005c4f24733`  
		Last Modified: Tue, 21 Oct 2025 06:25:12 GMT  
		Size: 3.2 MB (3172961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2cb16feecf88f4cc85230af7f6e3bdc5fdd674aeb3046e008587877fd99a650`  
		Last Modified: Tue, 21 Oct 2025 06:25:13 GMT  
		Size: 5.9 KB (5883 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:6a0eb536fc3bdaa193ddfeabe15d9edeebc283e467f22ebffae94db7da04e50f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45716715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:940959a16d98976a01745b774e57cd3ffa09f41f9b894d80c902e4e8c4ecff0b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1760918400'
# Mon, 20 Oct 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:25723cf5ae8b10c461d8c699bc5f9e41058f8fd5113212d106848ebe89fc0ffc`  
		Last Modified: Tue, 21 Oct 2025 00:20:56 GMT  
		Size: 45.7 MB (45716494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53827db731198ab7d1b942b2833a22e577589f5802210b7917b4b913b19386ea`  
		Last Modified: Tue, 21 Oct 2025 01:17:42 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:2c231d36857d96f7ae2dc3069531bdb12c9dff444d2b4014ad1de03859a106be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3177280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a785aa05287fa6a904ed9038f9c18393126b597c57c64044f0e28a142ced975`

```dockerfile
```

-	Layers:
	-	`sha256:a5a25e48fe25085fa02dc5657f73ba096b85d3562be3e8e88f710747ba9c5acc`  
		Last Modified: Tue, 21 Oct 2025 09:25:59 GMT  
		Size: 3.2 MB (3171398 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba840e2ca86d037e1fb926483cb7e295e41d966fee7a58d4a9d37597c768e80b`  
		Last Modified: Tue, 21 Oct 2025 09:26:00 GMT  
		Size: 5.9 KB (5882 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:f3e3ba70851549feb6a60fb181d2b2bde13c69a8362644259f64d37dbdb9e07b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49649964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43be5f5633abb875823486313899614ce9f3e2dfba9707ae27157638597fbe5c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1760918400'
# Mon, 20 Oct 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:2a101b2fcb53d61db540cb76da094137d4f0291a93fa41357ab70c3debf4d3c3`  
		Last Modified: Tue, 21 Oct 2025 00:22:57 GMT  
		Size: 49.6 MB (49649743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b75e0353c685136614933b10716f79bc4ac8d86af9bb583dc1049b61d58599fb`  
		Last Modified: Tue, 21 Oct 2025 01:16:53 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:0cf11bacdebfc590bd580cf806568fdcd663db500b14ff6519000b5aecb136ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3177400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:492374775aff86907037dd832c2b08018b86801b207fd49df1f071c6b8e8fb89`

```dockerfile
```

-	Layers:
	-	`sha256:4963da145f9cbe25e8032a4089133667f56bf9b805d139239fe54a96997723ee`  
		Last Modified: Tue, 21 Oct 2025 09:26:04 GMT  
		Size: 3.2 MB (3171505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9cbeac2b804cdf7a3d0d998b078de86bf40004ff20433b37ec3485a65581b0df`  
		Last Modified: Tue, 21 Oct 2025 09:26:05 GMT  
		Size: 5.9 KB (5895 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; 386

```console
$ docker pull debian@sha256:aaa0e6f22307928e1399319c82d54aa9f227ce1715762c2f43213cf2ce734f9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.8 MB (50800796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d925caf19a39f4c0d6b64d7e79b39baf7b84cbb764bea8e750d8b74365433943`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1760918400'
# Mon, 20 Oct 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:0c4647ea5bf10ee4302f28d7b05ac3b18ede5c510a3bb65671353e4dc5445f11`  
		Last Modified: Tue, 21 Oct 2025 00:20:56 GMT  
		Size: 50.8 MB (50800574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b279888b1f9d908ea6429ff41746045b023cd1171a3407e61ca980b0409d413`  
		Last Modified: Tue, 21 Oct 2025 01:17:28 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:b21c9cd4ca33db7d3115fe0a6eddbdfed210053a750c746d2ac4e45259b76638
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3173037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7f6e71194f83d73907e95e5b3f572d01c52b54e2f1d39350915cde265a5aca6`

```dockerfile
```

-	Layers:
	-	`sha256:6f6d18408f7df4348a713f82691962957e52a42aa741d70b678ee1204b25709f`  
		Last Modified: Tue, 21 Oct 2025 09:26:09 GMT  
		Size: 3.2 MB (3167227 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff698c057228713ad1955a8b6363ca4dc4fe7ec0b431707fd25d231022297fde`  
		Last Modified: Tue, 21 Oct 2025 09:26:10 GMT  
		Size: 5.8 KB (5810 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:f0749b9f09767fe9962e65248a300b291e18a85bece06816328bb92a1854946c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.1 MB (53109698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb77df218c9a280a27d0ddd89bdec90039b51e262a19bb26f413f430b8ff9b7c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1760918400'
# Mon, 20 Oct 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:047d1b265d8a7d20ef8b3ccb9f133c3c5f1e4f9c92089889756590b7f20452b5`  
		Last Modified: Tue, 21 Oct 2025 00:26:24 GMT  
		Size: 53.1 MB (53109476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71a97a59d13c31064f55f9380726bb3a16a87007ea2fe0993370dad2f3ae0ab9`  
		Last Modified: Tue, 21 Oct 2025 01:21:16 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:7e5be3ed000229503f8846d66ba09187f973db619b9baa216a213b2ad7683455
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3179388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f384a4979e92f5cca2f7818f6ee5fd33a2fea710089bd5d02863000f424b0e7f`

```dockerfile
```

-	Layers:
	-	`sha256:59b4902670d95a480ce3ac63437c00e3d61fb10afabfaaf264a0cb0c16f87978`  
		Last Modified: Tue, 21 Oct 2025 03:30:58 GMT  
		Size: 3.2 MB (3173535 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:060e198a91ec29ca1dd5d57eeb13dd2b4aee7b0b7ff4c27172223f34598faf63`  
		Last Modified: Tue, 21 Oct 2025 03:30:59 GMT  
		Size: 5.9 KB (5853 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; riscv64

```console
$ docker pull debian@sha256:2b2e7ac79b321ec799a59de333db3e76e6d7ba14b50e2629159731e8b98f8a8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47770529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32caeaa65eb10971bc53f69def6d8ecdfdf19c42cb093dabb8cc9a91a06c70f0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1760918400'
# Mon, 20 Oct 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:f99bc11a75f6f7a676f3f49bda98f8ef1b59f2c8ba74759e5fa155fda025bf88`  
		Last Modified: Tue, 21 Oct 2025 00:35:52 GMT  
		Size: 47.8 MB (47770306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3622645b89c381e5e3f4534ab6b1da9e6315cd9f125dbec5a92d5ae36efdf797`  
		Last Modified: Tue, 21 Oct 2025 01:22:52 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:fc0947d354bf61a68bd11f11e9472cbab31ee6250f5ac3b4cfbd47183ab788f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3168199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aff5f40fa9992b085fb2cb15afbcfa09809b7adeb2bba46f1c4a5b96cd599d9b`

```dockerfile
```

-	Layers:
	-	`sha256:695fe4e75552e7a37d9e9047f567475dac811a4815408f5f22c2402c0097a01f`  
		Last Modified: Tue, 21 Oct 2025 03:31:03 GMT  
		Size: 3.2 MB (3162347 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6063e95803761db13b93fa64b05823fe69b36f9c93d7ab29a91a5f1c17a4db8f`  
		Last Modified: Tue, 21 Oct 2025 03:31:03 GMT  
		Size: 5.9 KB (5852 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; s390x

```console
$ docker pull debian@sha256:8f12f2bf4552c81969b7b9683b34d4cd08cded335ec473b8eb3e338fcef5bcdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49351921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5e6f09e6aa520c0657d3abff62092c3c11b979622f97c096425f9319f5b0557`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1760918400'
# Mon, 20 Oct 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:be7c8533c3f8dfcf5ab5c0fd76b47a568dc971c853834a20808defd1e88a5ffe`  
		Last Modified: Tue, 21 Oct 2025 00:27:58 GMT  
		Size: 49.4 MB (49351699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7a7d49607018ddffbdba473375a205197327a8f9b34ee9200e14e47e212f41f`  
		Last Modified: Tue, 21 Oct 2025 01:21:29 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:5a0d3ba22aae96ca737a8db90879881c158cb151a896d03a0a1f2dc897704f7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3177298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bdcd099a9f63bcc44066d543d920574bb0609696649e8b7a17beb4b2cede444`

```dockerfile
```

-	Layers:
	-	`sha256:733aba472fa9c21d2695cf417119f4cc057f53a9066074d7e6dda41989f47105`  
		Last Modified: Tue, 21 Oct 2025 06:25:33 GMT  
		Size: 3.2 MB (3171471 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7c7b54a453761cc54b032b4af920e02ff6ae1113831c7049efda6425e3e8d31`  
		Last Modified: Tue, 21 Oct 2025 06:25:34 GMT  
		Size: 5.8 KB (5827 bytes)  
		MIME: application/vnd.in-toto+json
