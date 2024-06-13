## `buildpack-deps:sid-curl`

```console
$ docker pull buildpack-deps@sha256:6739be6cc5299a2a3becd3fc86ef85892c9a52acc3e6d950692a0102ec540c63
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

### `buildpack-deps:sid-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:d4940b76f809da1197d06e221d76a16f154fd99910005a1c2f7651772d7125a0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.5 MB (77459604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd0377e771a8165686d7b01131699352a03f3100e1b93531a23ed77ab1db9361`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:29:36 GMT
ADD file:b10a84e4e404c6ca6a1a6782f9040f24bb7bfbb95055e8cd39600ef22a4a9284 in / 
# Tue, 14 May 2024 01:29:36 GMT
CMD ["bash"]
# Tue, 14 May 2024 02:59:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:a79fdf356ad40501c2429368bf029e9f2414f18b03d6fa40ddac5cebf750f95c`  
		Last Modified: Tue, 14 May 2024 01:35:04 GMT  
		Size: 52.6 MB (52642897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfc1cdf2f53eab47078fb369ea2ed0807107650f4e0c9a7ff1cae9e9467eba2d`  
		Last Modified: Tue, 14 May 2024 03:07:13 GMT  
		Size: 24.8 MB (24816707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:2727b522581a0e9d7e257ccaa991834af6fad6e44209e8339342c595ccf11160
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.5 MB (67472237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:360d84e2c287393e6db6dfd2cb720264c45ee9f7f0d1c85135e8061dc40a060f`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:49:12 GMT
ADD file:53c5bacab4479c2281acdc8e18c636052e6d20212a45337d8a17b19319ec5ca7 in / 
# Thu, 13 Jun 2024 00:49:13 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:18:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:a884fb5df6a69e4609683ee45a6be09afed09564ce4f6b3902caeb9298054718`  
		Last Modified: Thu, 13 Jun 2024 00:53:18 GMT  
		Size: 49.5 MB (49497721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23a34ed06c08a0ade11823d7031f7d8e27822e2579c680e8f6960a126d5c3c1a`  
		Last Modified: Thu, 13 Jun 2024 01:26:23 GMT  
		Size: 18.0 MB (17974516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:bf257bbdb91866273bca56a40dd0290f25e4af8ac9569ecd3cb27493500f8ae4
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.4 MB (64377753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f69a19347af70abb5d47d8401477a141e4acdea8fb3a2f3ba8cf5937aa01c9b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:58:58 GMT
ADD file:447d578cf14b4a73088105e96e789b86c902fce17f3abdbe2d9af6404943e16d in / 
# Thu, 13 Jun 2024 00:58:58 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:28:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5ce389400ad34c3c307d0ed4f17eb1ab2ebf0cace811962fd7529ddeb931a8cb`  
		Last Modified: Thu, 13 Jun 2024 01:04:22 GMT  
		Size: 47.0 MB (47006979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:235b6587c5780c1c7e65c98dff1392373e5f0b3294f927a258767325ac74de69`  
		Last Modified: Thu, 13 Jun 2024 01:36:27 GMT  
		Size: 17.4 MB (17370774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:a6883eaf68d2b828459a2901d2a401218c8d59a3edb2ab487d374300230f9c8d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.5 MB (71454488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b86afd40412d2678262f0f1f6ac3dfd9c7d739dcdec42cdd722003f7119be699`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:40:53 GMT
ADD file:0df3518c1c665e2879ed3c7b7c5961b53fc28709cc135a245b209411a275c037 in / 
# Thu, 13 Jun 2024 00:40:54 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:25:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:844667f4b2125bd419ff2157667c09ca5b8d442b399e2db99e62277881555d82`  
		Last Modified: Thu, 13 Jun 2024 00:45:41 GMT  
		Size: 52.7 MB (52683111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de631d800a2d5597fbeefa6256f2a1b9ec1248adc1daeb69a836e05978fa6d5c`  
		Last Modified: Thu, 13 Jun 2024 01:32:52 GMT  
		Size: 18.8 MB (18771377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:a93d5eb754693132046b44e39b9895bf59057756f3d9d2afa9b661d0c3189d6c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.3 MB (73341776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:900a196239184de5dd85c9ddddbd7d4b87efe0349298cc554566130f3d778991`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:40:29 GMT
ADD file:8452dc45806912ac27c72fbde099f24d3385b2fe336f125781076ac8fada56f2 in / 
# Thu, 13 Jun 2024 00:40:30 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:13:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:892c6905b91a2725baf7261577bc387b671ddd2ecf5bba2922a38096ad8e5eae`  
		Last Modified: Thu, 13 Jun 2024 00:46:12 GMT  
		Size: 53.3 MB (53304297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5d90251148762e9b64a325035fd3aefcf26ce939ab1b44ed3e8097e28585f2b`  
		Last Modified: Thu, 13 Jun 2024 01:22:39 GMT  
		Size: 20.0 MB (20037479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:c73ec6fc8dd569ecd6a81939769429fcc3243c10e625619ffd1e7fcdf1732c74
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.8 MB (70792880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b1291d89c51713d502d831c481a696064d24c0ea1dd4e04343314cdd499aaf0`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 01:13:44 GMT
ADD file:bc1c5f4f7dc974780be655fc08cd2e36c5d04921a942dd0065534fe0f2520661 in / 
# Thu, 13 Jun 2024 01:13:50 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 02:17:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:371a3512d511da5522a67af4d5945c86f5bf5015bc3be3dfc08ea50797400367`  
		Last Modified: Thu, 13 Jun 2024 01:25:20 GMT  
		Size: 51.3 MB (51279195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52e19ab65511529aa4e809a989c916e7d1eea56540a36758da55666b6d063b69`  
		Last Modified: Thu, 13 Jun 2024 02:42:33 GMT  
		Size: 19.5 MB (19513685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:e5edca7fe593cb9d55f8f14bab112cbaa2779a97f0a6fefc177bcfdeee6939df
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.3 MB (77296247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c24257e6f9704ed4c61c4d43e85d492466bc297bf3fad9e01be24ba482b2f91`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 01:18:10 GMT
ADD file:17f3c29affbf057347abf006bc2aa243347ef42e5dcd37286af3c79f3fe983a4 in / 
# Thu, 13 Jun 2024 01:18:13 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:52:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:edab80a24633b63ae0ba8926dd3e7105717650d226694cdbfeaa41301a651162`  
		Last Modified: Thu, 13 Jun 2024 01:23:25 GMT  
		Size: 56.3 MB (56296967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa0cda58a29e7eca0ea797c77896694dad5c8ba0063d2386e0f1bcf721031263`  
		Last Modified: Thu, 13 Jun 2024 02:02:11 GMT  
		Size: 21.0 MB (20999280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:a5400bf2c9e5726109720d30527c96303f01fe54109ffcb1b08783471ee26ec3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.4 MB (69421620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0299e6f8b131914ed98855e3c32289e7c65840c305b555b6f722c760299539aa`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 01:31:50 GMT
ADD file:5f145818f2852834c826623d73119954ead96eb9bce2d43c78acb87643e22613 in / 
# Thu, 13 Jun 2024 01:31:53 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 02:02:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:6ac783982847dc2f82c444819c90a10bdd382db79de84981f527e1462e567adf`  
		Last Modified: Thu, 13 Jun 2024 01:36:23 GMT  
		Size: 50.7 MB (50715744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1659c611213bc35c1eb01ea12d4ad271643ffd53f1e2e2bc4b26608a2487a2b`  
		Last Modified: Thu, 13 Jun 2024 02:14:02 GMT  
		Size: 18.7 MB (18705876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:9d13b3b3fed7a5c88446c55e87f4cd26f81127cfada2b0a78434a934ed4c967e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.8 MB (77840902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd13938e979998201bdf409e7fd9c1432696ae28a2c50a7e76e28090a4625142`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 00:43:54 GMT
ADD file:34bf2264b5be5e585bc909c05f313cebb02329e956459b02e719a727804b5ef1 in / 
# Tue, 14 May 2024 00:43:57 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:23:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:d8beb42479d9c358247f3312313f4b01304d06a9f4350f46669bc0340b164395`  
		Last Modified: Tue, 14 May 2024 00:48:47 GMT  
		Size: 52.3 MB (52293312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe716d1139dcfb0e4a0ac4867ff5d98684c037b80d0741511a7238159f33b964`  
		Last Modified: Tue, 14 May 2024 01:31:04 GMT  
		Size: 25.5 MB (25547590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
