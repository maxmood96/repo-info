## `debian:stable-backports`

```console
$ docker pull debian@sha256:944ba29e5ba7a164e250394820f24fbe7010d9731cd479cc92980d42d75918d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `debian:stable-backports` - linux; amd64

```console
$ docker pull debian@sha256:13974285c0f6a42af48168dee4a740d522188a5d65aa7ec62b4c1f98a7d220cd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.0 MB (55010098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:507e89bdfe9c356ffc228ab3bcb4db70112f74ba00e0bdb431a884892a3ed792`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:21:51 GMT
ADD file:737a506e7ebc691df8a80d35c1cbb41c08ae5a5d845821fc5c8c20be3ebeca2e in / 
# Thu, 23 Jun 2022 00:21:51 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 00:21:54 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:2e28d2612399606ad88011a02d3461010a45bb18ee475e4046f6d089d07573c3`  
		Last Modified: Thu, 23 Jun 2022 00:29:00 GMT  
		Size: 55.0 MB (55009876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f6b2e249775b778ea4f5e30e5ee397d270e085c544977ee70a39b74fef92df1`  
		Last Modified: Thu, 23 Jun 2022 00:29:10 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:39c267946be7ea904aad0bd7991ec521456a7113681b1c666b34c7932ef51606
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.5 MB (52541355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58b3fcf1a03a6b40e2fbd1afc59f071d1d341df992e6b45aabf1ea324aae2f59`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:54:41 GMT
ADD file:30be18a2a0a287723b8e48a75c0582b899f1c3df76c8d5cb7ef570fa268d6ace in / 
# Thu, 23 Jun 2022 00:54:42 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 00:54:55 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:cd8ecb2c12f965efdd0de713f1390f9ef2626c397f479f546f503a6a2e49cf5b`  
		Last Modified: Thu, 23 Jun 2022 01:11:37 GMT  
		Size: 52.5 MB (52541132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05bd675c1b27bdd43c763623f2c498c8f09b21c657543c84ff0d4afac256c4d4`  
		Last Modified: Thu, 23 Jun 2022 01:11:48 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:99fa2729d3dfc25ac6879a50f9e99947a3852c1428d3d02946fb1284a134f6e7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 MB (50199589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51dd00a0cda3782d3eef4a8dbd7c5006a9c37e1d71baf067c6e39b1fb0aa97d8`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 01:04:16 GMT
ADD file:5996ca40b14395257ee9465f542e325742df193190697f32656a16f82ba8be0f in / 
# Sat, 28 May 2022 01:04:17 GMT
CMD ["bash"]
# Sat, 28 May 2022 01:04:29 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:a629aa7acf7526a04f6b205da1795f21b7636b731d96f0bdcce4354230cccd33`  
		Last Modified: Sat, 28 May 2022 01:20:42 GMT  
		Size: 50.2 MB (50199366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb3bac480179da16bbc4852ed461845f3656865dc30a91c0315a4b9fd3d95607`  
		Last Modified: Sat, 28 May 2022 01:20:53 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:8dc32c8a1f53251dc82c30425ff09b26ff0b506d860b16e04c2ab9bf052c0d08
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53697057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9e75edc44560ebd82f39213f43525dcd6fbc23d4faa1387591eb4670577258c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:42:21 GMT
ADD file:ddcae2c18fa8dd35f2057125dacd9932420163d1d4597d8a33a9f29d13f275de in / 
# Thu, 23 Jun 2022 00:42:22 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 00:42:28 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:a13be41bd2ad9b92c78cedeb166a2205e88427c96a52433fce09b95e29b46d82`  
		Last Modified: Thu, 23 Jun 2022 00:50:37 GMT  
		Size: 53.7 MB (53696835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d0e91ad6ab8b4623cb4f72efe4cd4c950c2ae71888cf79e1b6a35c3771954f0`  
		Last Modified: Thu, 23 Jun 2022 00:50:48 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; 386

```console
$ docker pull debian@sha256:375112b66186b011486a8b7a0a704c745eb4ed9dfe6badee6ec0bbcd7b716f22
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.0 MB (56007771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a6de90e454643c3f4b16b3a9ae2851dafb834ec5d860f301682262e57644d72`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:41:19 GMT
ADD file:ff4b29ac632aa6328e16072dfa0f3e7b66c56d1cecb34bfb18a1d1b95a2d691f in / 
# Thu, 23 Jun 2022 00:41:20 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 00:41:26 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:8058a8829a35e9a90cb4a6c94fcceaffeaf71b45fbdbb6cdc36cca7b6de6ab40`  
		Last Modified: Thu, 23 Jun 2022 00:50:07 GMT  
		Size: 56.0 MB (56007548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40c6ed653ebfcbef2541c92ddedbaac629a3b68a5bcc92f7b1115a595f62ef18`  
		Last Modified: Thu, 23 Jun 2022 00:50:19 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; mips64le

```console
$ docker pull debian@sha256:ccadc47d807376c3f29d38280dfc40f0f04ebca251304089cd056c0eda89a50d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53272554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27148cb154704afb08d7ac7ff72e0bb907a8bd300249bc09ae59d0d463728d84`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 01:15:08 GMT
ADD file:be557b3d74a39c8051f2c00e84687ab16ebd892b36e8082a5ea300cb6bb7ad14 in / 
# Sat, 28 May 2022 01:15:13 GMT
CMD ["bash"]
# Sat, 28 May 2022 01:15:26 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:5716b5cfdffd75127dbe0991eff876f003b4eed04041291b556b7b099c1e527d`  
		Last Modified: Sat, 28 May 2022 01:26:01 GMT  
		Size: 53.3 MB (53272331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c532bfb0596dc121c8b023756a1718ca8bb67e2b2e14482c44d28c2201de69b7`  
		Last Modified: Sat, 28 May 2022 01:26:13 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:5ffe7093ac4f95ac6b4f4c11e8f91941ed2e4f3e44d92aa1e64fb5585eaf836f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.9 MB (58902893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78302adefcb237675c0211213c66c5c50053d3c5d2c3cb91801d605eef8c2278`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 01:25:50 GMT
ADD file:7c27d3f8cd82082cd3b792b3650524a2c8adbc4494d9ad7e6d7ae79b0689ed10 in / 
# Sat, 28 May 2022 01:25:55 GMT
CMD ["bash"]
# Sat, 28 May 2022 01:26:08 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:7b10a36258949d27f558770f76e91c58abf97f000104d582f67fbd7d43aa89c0`  
		Last Modified: Sat, 28 May 2022 01:35:32 GMT  
		Size: 58.9 MB (58902668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:563df939dcf42236b7ccb739b48a87ed253fd8aa8bbe7914f395d86147cdaf13`  
		Last Modified: Sat, 28 May 2022 01:35:44 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; s390x

```console
$ docker pull debian@sha256:081ead2774ed562ab52227456b4f0eb41f27faeadef8cfbdc7720a7ecc7929d9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53277026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c2fd11b1a191a86b2235d221df773b228774b217940d42ac0116d1e1f9b8e97`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:46:00 GMT
ADD file:73c0b4e8a93d320e7beacb602bbd3be64261189e16d3534d40ec519b2acfbff8 in / 
# Thu, 23 Jun 2022 00:46:08 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 00:46:17 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:c20cf944d8c43a3b78c63ae1b46b6e5070946c86ef7ef98faee10dcde4b83bc5`  
		Last Modified: Thu, 23 Jun 2022 00:53:44 GMT  
		Size: 53.3 MB (53276802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e990b7d84256d6222cd0e345c5dc76b27475416a081d5c12ab020c57d37c7d7d`  
		Last Modified: Thu, 23 Jun 2022 00:53:51 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
