## `buildpack-deps:unstable-curl`

```console
$ docker pull buildpack-deps@sha256:9d72ec118c208781fcfe6e5d86cf1de1456f6046593beff609a793575d0a8800
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 9
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:unstable-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:1444ecae199d3a84f514fffd3e96a07d956d068d696e22a6668f3a8b7b69bea0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.6 MB (73558597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3b07e6edfec497631a8a3716b0e973fce8f54eb68ded798958b4befa07050d2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jul 2023 01:21:50 GMT
ADD file:4bfda8f11e59383c37bfa6038bb5d22f58b9724d249a62568a2e7d2908821cd3 in / 
# Tue, 04 Jul 2023 01:21:50 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 03:34:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6efa412d16b908043ec01c4ac9ff7323c0f488dd5d7ea4b9b086f1e80350b9b3`  
		Last Modified: Tue, 04 Jul 2023 01:27:46 GMT  
		Size: 49.5 MB (49475944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cad8fa89586d6eb7c1bf3add3cde8c80b2da78794ef30be11a97f2dad784809a`  
		Last Modified: Tue, 04 Jul 2023 03:54:24 GMT  
		Size: 24.1 MB (24082653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:d1a9056c98835bada87f4138da4b902136cb795eca133e00ff0b1c407fb52bc1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70080759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a9b5fce7ee5621e0e2234d3e15d91216d47839ce7270d9e7ac54cf651eecc62`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jul 2023 00:49:11 GMT
ADD file:e6181e27889c016519d8d701345aafff7138df96a76fb6a29403c8a33a3365fe in / 
# Tue, 04 Jul 2023 00:49:11 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 04:27:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:667272d8fe1bc81ce33874dbc84976c86d6b95f50198465a6ab672c71d87f666`  
		Last Modified: Tue, 04 Jul 2023 00:53:33 GMT  
		Size: 47.3 MB (47322473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3b5934a15453e5e63936a0201a34b820f06d7c27f091dc017bac7d92e1e58d7`  
		Last Modified: Tue, 04 Jul 2023 04:30:42 GMT  
		Size: 22.8 MB (22758286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:59061e421f12529526dedfeedce5569a02e1b2a257e39132aaa33a404dee04a0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.2 MB (67157789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89568bc4d80f006e44d94b77ccd742ffd184dd2cb9930912b9cc360cf402b7ae`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jun 2023 00:00:33 GMT
ADD file:82567bde3caa9ad83c0c12c0525e6fd51cc833f0b29e733c2da572ed00150220 in / 
# Tue, 13 Jun 2023 00:00:39 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 05:00:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1d80e7ebc54969ad575378cf66dc58999cbf341e0d2a92c9ff0bfd5b3b9fb1c3`  
		Last Modified: Tue, 13 Jun 2023 00:06:30 GMT  
		Size: 45.2 MB (45234838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a26e461ec0e64583c2acfbef48942f57c9de9da65ff1a078a62e910baf3ce05`  
		Last Modified: Tue, 13 Jun 2023 05:05:32 GMT  
		Size: 21.9 MB (21922951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:0984fef26ca007b8361af058cc68e24c88364f04f39d1a5b9818a82efa2c8e30
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73150333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ceb08765561cdb51f4d0fbc0ce9566e0cb080c17279f33f10d5a5275dcd7962`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jun 2023 23:41:38 GMT
ADD file:94f1432513f9a03b38028af02b1d1720fb0558559faf3e7f9d7097cf6b962056 in / 
# Mon, 12 Jun 2023 23:41:39 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 03:05:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8ba9ab3e6f12b9702649c2e0c7d78e22ffb9183f68c288b9edef2387bd8d4efd`  
		Last Modified: Mon, 12 Jun 2023 23:46:36 GMT  
		Size: 49.6 MB (49592096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:393fb89bae1d5f0307a283cb7c3b5f54cc63fde2e90b7b65ceae29bcd27126f5`  
		Last Modified: Tue, 13 Jun 2023 03:10:09 GMT  
		Size: 23.6 MB (23558237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:555e0c926152f63f4be81642923a7d416a6db8de6cdeffaf232ce9a51950f704
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75427637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43878012a9d69af31988db85d06eed454cfed8f9f71f7baeaf892725ce675e3e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jul 2023 01:40:19 GMT
ADD file:565f8487c71b5de967f1bf16d4bd86291107b68f4152a61e35a8ab86e9f83b7b in / 
# Tue, 04 Jul 2023 01:40:20 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 05:37:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:46685592106ba6554716942e180f6b4cd8a73f1ec934554b40aee89b47118f5e`  
		Last Modified: Tue, 04 Jul 2023 01:46:32 GMT  
		Size: 50.5 MB (50505825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bf3084ac7ee091f26af470878c8197f67d44c09670c27921a26209c909a5c0b`  
		Last Modified: Tue, 04 Jul 2023 05:42:02 GMT  
		Size: 24.9 MB (24921812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:3c6d534b2bee072e65116be4c4db5f713b9559c66ddd9d00234f189d349f3917
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73167755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:870fbe68325b37a1adc7501ef4d15644fdf31b3fe699e4f855a737ebf9cfef52`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jun 2023 00:12:52 GMT
ADD file:b2a9cefcdd223b4cbf9b1abac81e8c0c158a24f9c272910a8822619ea9d55ae9 in / 
# Tue, 13 Jun 2023 00:12:57 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 02:12:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:65733d4f161a7d2fd9cef6d80eb7fe00897e936eb78d018361809f7384b08c28`  
		Last Modified: Tue, 13 Jun 2023 00:25:52 GMT  
		Size: 49.6 MB (49561285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8cac982d96cd0724a1a282faecd42ae997cf2e6c468441bdcf2ce718f092f4d`  
		Last Modified: Tue, 13 Jun 2023 02:26:09 GMT  
		Size: 23.6 MB (23606470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:a5807b1f6748c228dc4b2b9be5b8dd6d43925344484a7ac9794dd5a809331ce1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.2 MB (79206895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:985fda4e25a501fb5c76ae42a7c2ebc1fccc03a9dad9be7395da923cac261da5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jul 2023 01:19:33 GMT
ADD file:4c1d6f76704d32b9b503bd61c4b485555ec28037fb500403ffb5cbb102cf4509 in / 
# Tue, 04 Jul 2023 01:19:36 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 03:37:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3e4e6efa69b637e0e8ca00ddcae1aed23aef874a92a2904bdc6c9fa5b3212b8a`  
		Last Modified: Tue, 04 Jul 2023 01:27:02 GMT  
		Size: 53.5 MB (53474414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10b5bee4b9196ae6959902bca430113379429a2f075e1553977c6d0442f46233`  
		Last Modified: Tue, 04 Jul 2023 04:39:59 GMT  
		Size: 25.7 MB (25732481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:44d3a4e55beac77f423ed6b86a5ec1b7f0f8420391a51ef5818256b5db0eeda5
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.0 MB (67982840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb302f8c83e3c25737152a29d46030f5f78fa08610c71bf94fd362290d41d72d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jul 2023 01:09:05 GMT
ADD file:dc2a1586d12e833e5dc300033838059f3946ddddccde6c62d17cba40536ead15 in / 
# Tue, 04 Jul 2023 01:09:07 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 01:31:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d273b82777a979179469448ba9e255d7f7e1671f28d5610f47e8530093aaa04e`  
		Last Modified: Tue, 04 Jul 2023 01:12:27 GMT  
		Size: 45.7 MB (45695454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4f7ece03f0359914c61a65ea80744e3ec92ac1afbb1ddab79b6c7276dae0614`  
		Last Modified: Tue, 04 Jul 2023 01:43:00 GMT  
		Size: 22.3 MB (22287386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:8211e8f6c8723217137753ad27a4c9d54bf8a0981e5e1b88e21857c7284d7918
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.9 MB (71940987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d9c692d3c223e575d80944072e796dcd0b6ff99f060acdb6763914a505db111`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jun 2023 04:30:54 GMT
ADD file:7ea0e5c460c626891cd3fc90639d6bfb9a27beeb7f5c79fd9c348c5b6244bd0d in / 
# Tue, 13 Jun 2023 04:30:58 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 18:33:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a129144c9fdcf79f6394b7f7bfa3d7e6a0c8ebfd424dca918695356a1b3bf970`  
		Last Modified: Tue, 13 Jun 2023 04:35:27 GMT  
		Size: 47.9 MB (47920583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d42182bfe271810fa332f879c12433ca046660729997bdce646aa7157138984`  
		Last Modified: Tue, 13 Jun 2023 18:39:25 GMT  
		Size: 24.0 MB (24020404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
