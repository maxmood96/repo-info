## `buildpack-deps:trixie-curl`

```console
$ docker pull buildpack-deps@sha256:9f3ec2c34f2a068d51874ada4553f6327d823ca332b29805ee6c674023ff561e
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

### `buildpack-deps:trixie-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:b5a2216ded3dfabaa523075f3d093e49651e32b4c676be578ce1d198001b5c9a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.2 MB (79181482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d5f0ef64f6edce5c0b648e714f12badae93d6c4ff5495129213ff569d07e79d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:40:05 GMT
ADD file:fdbc095d632d315bfdea7b6a7cb53bfc7d32b5f6d604481cc9ff350c6ee09e3a in / 
# Tue, 13 Feb 2024 00:40:05 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:28:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:02ffa0574dfa0456dc05b0e175a93781ebc31447cddca3de402d11ac2734c97a`  
		Last Modified: Tue, 13 Feb 2024 00:46:31 GMT  
		Size: 52.3 MB (52331572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee8b4acf3d75cdfabf855170e302e7faa684ea2ab5ed2c5f7ca4ab289f942ae3`  
		Last Modified: Tue, 13 Feb 2024 01:34:58 GMT  
		Size: 26.8 MB (26849910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:fd0a14ae856254c098859eec38bafaf87e9474e0d817958dc4b89726aa5aa0fb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72458820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:717c04e5eab3c7c08ebdbcddf4383b81f31a07eb15d7c81d1d2370a21b5aa91c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:49:56 GMT
ADD file:3e60918b2fc6eb291458158f2b94b782320f758effe373fd6d0a5c58dd3e2319 in / 
# Tue, 12 Mar 2024 00:49:56 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:39:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5d768e5bf180c947f8692477b575df3498b64f65e904bac933d0260cd957c8aa`  
		Last Modified: Tue, 12 Mar 2024 00:55:26 GMT  
		Size: 49.4 MB (49418029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deb2336dddcb338dd0f592faca75df5ec1dcd20bf4a99dac4ce09223036087fc`  
		Last Modified: Tue, 12 Mar 2024 01:45:26 GMT  
		Size: 23.0 MB (23040791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:7bd0fef0c15b6b22976187497f5fc8e60c1cb6fe6ad8dd9a9826aff2ecc2a69f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.3 MB (71336548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46cca5fd674f71a9a0e4010da408509d4d06da6a66ee88cb1749dedb163009ee`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:24:05 GMT
ADD file:f3b7f1f27caea165ab01da75acbaae7e03df94488e3cfefa977f306caf975209 in / 
# Tue, 13 Feb 2024 01:24:06 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 04:23:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:579ea7eccb92178525cb18bd8dc77986380b3f914f60227ce0c74c4ada08c61a`  
		Last Modified: Tue, 13 Feb 2024 01:31:46 GMT  
		Size: 46.9 MB (46914007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69ba2a252ec366e26c0dbd94c623c7e6c905afe0f198ac0d2cd9f018673abbf3`  
		Last Modified: Tue, 13 Feb 2024 04:32:13 GMT  
		Size: 24.4 MB (24422541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:64b7ff72b7d47330d2407edd07ee6ddd8762882093629c0ea442921448fc2ca9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76070350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03235140c06be132c58c0cdeadaa865e344ba6a78e9c1fc9243154a73c0b272d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:47:23 GMT
ADD file:822f8ebf81dcb8d0c3abe6092460eb4cd185e7a4b5b794a9ebc4221cc30518c9 in / 
# Tue, 12 Mar 2024 00:47:24 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:31:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:abb8ff6184544bf5d189fbbab4286e594f2b7adc7d1feb51af49c007cff0e2c6`  
		Last Modified: Tue, 12 Mar 2024 00:53:00 GMT  
		Size: 52.2 MB (52191351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28f6a2f77ef2eb04a7b071796c5ec48f48d3cc5f0577048728b1f064cfc42453`  
		Last Modified: Tue, 12 Mar 2024 01:38:42 GMT  
		Size: 23.9 MB (23878999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:dd0f8780a9e3a1427be04b729b628a6210f19daa6c147b10d71dd85511a17e52
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.1 MB (81053399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2cb4f729aa8bf435ec461964e478b611b67a629029a4e260fa8900bb4a8b6a7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:45 GMT
ADD file:48adfe9ef1da0d6e87fe297dd6cf8e9e117db33c490c41c77b6f2aadda29a275 in / 
# Tue, 13 Feb 2024 00:41:46 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:27:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:b1a72a4bdfc8e16b8965d5db9e85a05a0f23a851b8b45d3b9e7376d79f2f223b`  
		Last Modified: Tue, 13 Feb 2024 00:49:03 GMT  
		Size: 53.2 MB (53166976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52348cdaee951cfde5088d97935929bf6f09626868b2b48c50a688783d5fad8e`  
		Last Modified: Tue, 13 Feb 2024 01:35:17 GMT  
		Size: 27.9 MB (27886423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:b384349ee873c845d6846cc9daf33f3b3862a129b50d3cca6417f92d632223cc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.1 MB (78067182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f22cc52942ab8af399e083497fc46481bb88c01eb1c1a256f15e9bf165bd043`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 02:10:56 GMT
ADD file:9e81c7cdd0919c81ec6e4c8e7ef69562482e6c6184b0d333d4967432528f527e in / 
# Tue, 13 Feb 2024 02:11:01 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 04:11:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:9e34ce429d95dc24c45b2002b054092ba5fa55ce42b0cd3741fac5028688537e`  
		Last Modified: Tue, 13 Feb 2024 02:22:24 GMT  
		Size: 51.4 MB (51404528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9823263b2593dafa6b195b9b1d81ef1eb1be76f5ae911f0a51ed22fa2c480af`  
		Last Modified: Tue, 13 Feb 2024 04:31:05 GMT  
		Size: 26.7 MB (26662654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:462a72ba0fb0509281ec48005feee8849237e75e97b4f9473c101c91c8b2b032
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.3 MB (85282259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c40249fefed1d217df6b9b8c2575dbf6cdaf6e89168f22c2c96d4701e47c4e5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:36 GMT
ADD file:20495ab1a5b590f87307401881c4392d68c4ae3aee17cd89e2196908d9ee5c75 in / 
# Tue, 13 Feb 2024 00:41:39 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 07:32:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:f12da478bcef0b5e264ca4e1bc3288008557f76cc25c8a87e714181c7f30ac36`  
		Last Modified: Tue, 13 Feb 2024 00:47:57 GMT  
		Size: 56.2 MB (56234839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbb30d823a34f6274ec3b36fe7d62aea5946dc0fe6f3c2fbc9d8cb1574aa46cc`  
		Last Modified: Tue, 13 Feb 2024 07:39:58 GMT  
		Size: 29.0 MB (29047420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:ff0d1a140bae51964725cb9471d5a971ecf74e35f74d3c64234763ef4b503fee
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.4 MB (79396100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:883211e70ad6032fefbbac2065bff44d3cc98bef3a1c14cfcf6c1d800e8a1f07`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:21:00 GMT
ADD file:f20e5306e56598f8b82f84922c40c9e2f7e47e2a8c85bf30e7e3a6a9e21b9401 in / 
# Tue, 13 Feb 2024 01:21:03 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 02:37:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:3bf5d0a5ac97061d670703e5273b82b1ecbc5b9bf33962fb4024d89b066daf10`  
		Last Modified: Tue, 13 Feb 2024 01:32:45 GMT  
		Size: 51.7 MB (51742323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cb5ddb994c56eadc492865ce2e238a4c712cc671751f0a8231b33027bdaa2a3`  
		Last Modified: Tue, 13 Feb 2024 03:00:46 GMT  
		Size: 27.7 MB (27653777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
