## `buildpack-deps:sid-curl`

```console
$ docker pull buildpack-deps@sha256:01d12c85fd6da77963877b9e4c1c0d3b6304e3931a7f0130e5388eb3dfa06ef4
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

### `buildpack-deps:sid-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:3bb61e843f0a31b78026b0a33f51d80f65a5ac4cf69aa54ecef34b5b4c550619
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.7 MB (75680909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11313e13ff03a9d76f8b033efdf39df00626dd48bfbe3047c5e2e4834de56e40`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1762202650'
# Tue, 04 Nov 2025 00:28:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:2e77f12282fcde2c6f54d54624e8a7eef59205bf9001d755b40c1e76ea8e3238`  
		Last Modified: Tue, 04 Nov 2025 00:13:00 GMT  
		Size: 48.5 MB (48485640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f19ac06db907fa72eecf21fa150fd26d99a092e409ed5349cff34755befbc8f`  
		Last Modified: Tue, 04 Nov 2025 00:28:38 GMT  
		Size: 27.2 MB (27195269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:eff5ea32912bbaf6b91d08991d640fbe2200cbc042b76026d5e0da6a04dab928
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4105070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7cd10be292cee079aff0a12ff59e4ca3a716a7336bc868699d3ab20d514a108`

```dockerfile
```

-	Layers:
	-	`sha256:f264082a290198bcffa1658c7f2d63f9e96943e95ad59ba5dd451363081f404b`  
		Last Modified: Tue, 04 Nov 2025 11:23:49 GMT  
		Size: 4.1 MB (4098309 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b730cde1d8ff99b6865f3303e3f744fa62e7a5bf773a11ea17475792e3b64d94`  
		Last Modified: Tue, 04 Nov 2025 11:23:50 GMT  
		Size: 6.8 KB (6761 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:36425b4377c67ac3b0f72acfe46d4b4ec20f9489d15f7b89d64a54edc4d497c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69920408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:829133095a83ca933728392dcb9a3b5028119a73e85ee8135da83748288d3010`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'sid' '@1762202650'
# Tue, 04 Nov 2025 02:18:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:4cf40c8870d4fc31c85e1981d6e2ac2787a589f1e553cccffe9aca41df353fd5`  
		Last Modified: Tue, 04 Nov 2025 00:13:33 GMT  
		Size: 45.0 MB (44990635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32fb447e96331843e57f9f8c2921b90731b9e4529a8a58e3def300ae395aa899`  
		Last Modified: Tue, 04 Nov 2025 02:19:17 GMT  
		Size: 24.9 MB (24929773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6c04ab9056c154e6ae42a55f73a33e281c526467c149b538193754811d6ecebe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4106630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd1a046366c62006c59dde5400fdeb5761813e1b40d6800151b42b3b26042ddd`

```dockerfile
```

-	Layers:
	-	`sha256:68bb49afbf85cf33005a503b845895fd81fe1c648df40c2bc7611e1d2792bf65`  
		Last Modified: Tue, 04 Nov 2025 11:23:55 GMT  
		Size: 4.1 MB (4099805 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb8997b693e7416258d5bf5ab5a9bf1c0c3b76a617db47bc25a7ac7a0e1b6c9f`  
		Last Modified: Tue, 04 Nov 2025 11:23:55 GMT  
		Size: 6.8 KB (6825 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:ce83312af6f68004bac915c3d3c72c207634f08b32e9512bae087b01bf0e0c92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.0 MB (75048290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa1646440c724bdd11aeb6d5b103008c248186c81c7f42235b5331624ca36f67`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1762202650'
# Tue, 04 Nov 2025 01:29:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e6429e9e41ca9e14d8856af7a396ce50bc2b9896b4f4cd83c36fd480cd4514de`  
		Last Modified: Tue, 04 Nov 2025 00:13:31 GMT  
		Size: 48.6 MB (48586018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdee2464e4f33b113343bb1ab557ca8f41d3b10032adfee93dfe6afa6fc0c4b0`  
		Last Modified: Tue, 04 Nov 2025 01:30:07 GMT  
		Size: 26.5 MB (26462272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:3981f029ca3741e9ac4cbadd283ef89ef4be5296e02ba168348dc04080638a04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4106042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e33ed55d2c17020d0a2d205647ca536a72f4f5d7a241cbb92fee73b24e9d8853`

```dockerfile
```

-	Layers:
	-	`sha256:4bd6d2041680a2b94026bc5f25caa1ee8743cde61eff6c7db0a1ae73d1d78d8e`  
		Last Modified: Tue, 04 Nov 2025 11:25:19 GMT  
		Size: 4.1 MB (4099202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:461a657b134af443b47df7b4e33bbac070c3169a66e1e48f335cc0d294ad7a00`  
		Last Modified: Tue, 04 Nov 2025 11:25:20 GMT  
		Size: 6.8 KB (6840 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:79a2380e227d14c9b39afcdcfbc368ba1442b59bbafee46e305690c99ea54c59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.2 MB (78245269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e08a154510ee0409bae9de68443ec7f5e0f647de8d57252b6b3141eb8eb5f621`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1762202650'
# Tue, 04 Nov 2025 01:31:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:37a822686dc57d9a439e8fe6f90a9020bbd58f684341d3cac6e3e13c68f3344e`  
		Last Modified: Tue, 04 Nov 2025 00:13:36 GMT  
		Size: 49.8 MB (49809007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e227b380623fcba2d9150034228fcc8257fa11236e7ccca0e2f9cad3a24c603a`  
		Last Modified: Tue, 04 Nov 2025 01:32:02 GMT  
		Size: 28.4 MB (28436262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:3359158ade2919ba1bfa4422606048466187dbdb83d3b7a3f0e3a483efd666fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4102167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3d12c47c8574b0fced89e97bc0e42099cc0d157d40b81dd1a894d97e04f7ceb`

```dockerfile
```

-	Layers:
	-	`sha256:cede792be9e65b125b1eb4219b8396e08ab3eec86a48712c67988a087df19604`  
		Last Modified: Tue, 04 Nov 2025 01:31:55 GMT  
		Size: 4.1 MB (4095428 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b672e78181943f1a3ecc6843b66387bd7599b3c7dc2acf0bb2f5874dc30f120`  
		Last Modified: Tue, 04 Nov 2025 01:31:54 GMT  
		Size: 6.7 KB (6739 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:8bf17c31458bc47015363d5531aea1dc0539fe6b09b8f88d0f2d9c34af1c3c32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.1 MB (82118901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d111c64fdcfffbae00d43a18e786260bd8426498fd6bdb484cdd1ae12f8ed072`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'sid' '@1762202650'
# Tue, 04 Nov 2025 06:27:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:030897837715e5a3cb573dbccbde37df9e71014e141907c9a871969c5845717b`  
		Last Modified: Tue, 04 Nov 2025 00:16:41 GMT  
		Size: 53.3 MB (53318000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e937e4e09e15f972661a8c6ed2f0ea78f89b82022e280a058f528fdf12a10ad9`  
		Last Modified: Tue, 04 Nov 2025 06:27:54 GMT  
		Size: 28.8 MB (28800901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:60ab809f4a0d995b7cd6ec4edf8540a54d8e5ecde9338bac07a0054a94e702f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4108935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01a726ccaada42b5885eac71e528e50161b9a525e6760420043eb4886047b5e6`

```dockerfile
```

-	Layers:
	-	`sha256:d3104c6c2e82cd47285e8c879f69c3f76a28c5a0e6c1ecb23f21041bf263d77a`  
		Last Modified: Tue, 04 Nov 2025 08:21:35 GMT  
		Size: 4.1 MB (4102142 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd5bd5db70bca5cef74ad36e64cb0c4ceb604c42ea32dc50c9598dc59c534b56`  
		Last Modified: Tue, 04 Nov 2025 08:21:35 GMT  
		Size: 6.8 KB (6793 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:51ea31613a6ac8b44b991da2f910506387ff8810691d2bdd30fcd1f314417c3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.1 MB (73112431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6511c7c071cfeb32be9916e5cf01c1204f8aa56410339a936457099a3ff5ceb1`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1760918400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:2be9bed11e9fd66165d84261d66ea19eb2c82eac8e67869aa7908bd19fd9be21`  
		Last Modified: Tue, 21 Oct 2025 00:25:21 GMT  
		Size: 46.7 MB (46705170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d36f6ee73a964ada5e4d7f0d2e62741259e488dac65675b450483b9da2f329e7`  
		Last Modified: Thu, 23 Oct 2025 03:09:49 GMT  
		Size: 26.4 MB (26407261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2440ebf922a59774446fb01be8e19abfca9a848c4a17b0e7988e3d5998acab87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4096198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:962fee51da12a0c9fc35d228345c255bd3f4abf25e6f0deefac8a7de4da01263`

```dockerfile
```

-	Layers:
	-	`sha256:46cee17684db2ab8d36b3b251340171a60b85027f77804558f5005a863ef1a34`  
		Last Modified: Wed, 22 Oct 2025 19:20:36 GMT  
		Size: 4.1 MB (4089362 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a45051579bc5b66c27327718c37971cb833de13b9e1d9946e8e61d93c4797aeb`  
		Last Modified: Wed, 22 Oct 2025 19:20:37 GMT  
		Size: 6.8 KB (6836 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:b08440e4441e615539fd10009f393eeb9421bf95104321a677cac89f7a4e98e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.7 MB (76670619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1ee15f0077c18fbbc1b199f5907073008c56876d04dbd11f371d613ac72b5ae`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'sid' '@1762202650'
# Tue, 04 Nov 2025 10:02:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:ee07654f71bb163a06c3532a844efe8d75683f4dd53a88a8109fd9ed1b66fc1f`  
		Last Modified: Tue, 04 Nov 2025 00:16:26 GMT  
		Size: 48.3 MB (48346444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14e24f5b3ee730a867fae54f44e0b43c0311d9bd66c565a7c2a2b0d7a887c220`  
		Last Modified: Tue, 04 Nov 2025 10:03:07 GMT  
		Size: 28.3 MB (28324175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:54b2df1bba47b42f223252bdf9378fa66b58168bcd454042a0d11f97cae4528b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4106479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:329c35f28f85075776312e50f17e864d83b5c0de55ce6d4e7f18e229cb08388a`

```dockerfile
```

-	Layers:
	-	`sha256:fc010c6b002fca2acb3f824b6865524d3910f8d5aba92807d630a4f028cb8458`  
		Last Modified: Tue, 04 Nov 2025 10:02:58 GMT  
		Size: 4.1 MB (4099718 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba9c88e8aeb2aed7f6df8210c94356176d31d89d2f67dc1d5d0a7ffe616d9654`  
		Last Modified: Tue, 04 Nov 2025 10:02:57 GMT  
		Size: 6.8 KB (6761 bytes)  
		MIME: application/vnd.in-toto+json
