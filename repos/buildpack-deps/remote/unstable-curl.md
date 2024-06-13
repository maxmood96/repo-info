## `buildpack-deps:unstable-curl`

```console
$ docker pull buildpack-deps@sha256:85161cffbcde764ef4f69f3d6012adfe0ffacbf68e96dace39605c9a19e19e1e
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
$ docker pull buildpack-deps@sha256:c2464e7c70ad5f869976e4b6283f5942883eff2ccff1bedf3049a2d22dfbfa41
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.5 MB (71462892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be7ffce092a3fef9ae8b08fb03c65caeca5ed4667492a96a1da28d830862f089`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 01:22:28 GMT
ADD file:06cf5b56eee98058acc2138b22939b094380deece3b7569cb8f72001a1b1ae81 in / 
# Thu, 13 Jun 2024 01:22:29 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 03:44:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5d01f86c265bdcd9ad24686bfb950b1af7886771bc1e983efedb66d6751451de`  
		Last Modified: Thu, 13 Jun 2024 01:28:09 GMT  
		Size: 52.4 MB (52429606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f10c3634e4ea850e0332efdaef4da3bd69ad039d336a37c6df0056933e0e309c`  
		Last Modified: Thu, 13 Jun 2024 03:52:21 GMT  
		Size: 19.0 MB (19033286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; arm variant v5

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

### `buildpack-deps:unstable-curl` - linux; arm variant v7

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

### `buildpack-deps:unstable-curl` - linux; arm64 variant v8

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

### `buildpack-deps:unstable-curl` - linux; 386

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

### `buildpack-deps:unstable-curl` - linux; mips64le

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

### `buildpack-deps:unstable-curl` - linux; ppc64le

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

### `buildpack-deps:unstable-curl` - linux; riscv64

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

### `buildpack-deps:unstable-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:c217626be9440573d2d871bb5174b8cce0c1ac7ec4e7ae71d0d5f45268be0b3b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.3 MB (72270154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5d3fc177e626678307dcfca8ca78ee7638ff683e8fb20f9a3153fa84b0f012e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:44:00 GMT
ADD file:48df1edc9b73475781ccac0eb967ca97c87c5a3132a7c9058519fad686260867 in / 
# Thu, 13 Jun 2024 00:44:02 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 05:25:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:f539c970b22ae85b0b82128798f27249002cae24f6d005cd8df7e2098a346a0d`  
		Last Modified: Thu, 13 Jun 2024 00:48:56 GMT  
		Size: 52.1 MB (52054394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98301e222cdd3787932e298432980b45832dc8bafb525d89b9f56907acf79064`  
		Last Modified: Thu, 13 Jun 2024 05:32:33 GMT  
		Size: 20.2 MB (20215760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
