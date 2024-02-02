## `buildpack-deps:trixie-curl`

```console
$ docker pull buildpack-deps@sha256:9676f249efa277d6f658ace6f62655d6e6bd184e8a5ee19cfe40a17f20519919
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
$ docker pull buildpack-deps@sha256:84326e327314455c4bab2f12086f2976fad56f95d2c73b0e5dc8287b3d77dd01
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.6 MB (76623453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1876ac991c0d94e9d40ec790f81fac9d0192bced604cdcafc921362ff7692364`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:37:59 GMT
ADD file:8ad3e26aeda90bbd087b64f3a0110c8f2e520a774d62a26d5aeb7c5006e472ca in / 
# Wed, 31 Jan 2024 22:38:00 GMT
CMD ["bash"]
# Fri, 02 Feb 2024 06:00:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:a946c083680d9a81b8eb8383bbc21cd34444b1c5f3212c5d3fc463e0220d7b73`  
		Last Modified: Wed, 31 Jan 2024 22:44:39 GMT  
		Size: 52.3 MB (52283197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3989ddeeace463dca551e8958b92088c5e4b3d49b9ba7ca3579c7dbf9cd9af1`  
		Last Modified: Fri, 02 Feb 2024 06:21:45 GMT  
		Size: 24.3 MB (24340256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:1c1112adc813c8c551efa6a9791d7f9a7ad836aad790eb3c79664eafeead7660
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.2 MB (72192534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44dea16c77d1eae9cffc13842c542dd71f840b414ac3889cfc6943cea769cd77`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:46:08 GMT
ADD file:7144257253ce293f694d917fb06ea4d03cb3cffd94c432e47fa5a77e03a5a2f7 in / 
# Wed, 31 Jan 2024 22:46:09 GMT
CMD ["bash"]
# Fri, 02 Feb 2024 00:48:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:9be7d01dbe3e5ca74f21aad18f318e9da338902efa0bdf09221df8cf061d6b3a`  
		Last Modified: Wed, 31 Jan 2024 22:51:27 GMT  
		Size: 49.4 MB (49400791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd8e83ce6004aab85ee491973a0f9e3b97cfa5114d4dacf9858519bf7991608f`  
		Last Modified: Fri, 02 Feb 2024 00:52:46 GMT  
		Size: 22.8 MB (22791743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:198091b0bb21f5b70c09cfe4c9abf18a0caf90a2711ce5e11b8e0c7cea1df75a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.0 MB (69003325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5893a7a2f2dfaa3342ad12fcf0d5b2993b234942d22d770a6d0bfc8b697f842`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:47:01 GMT
ADD file:313528f956e019639cb41933c0f6d14e7dca01353fe4ca789d7ac69e4c131ccd in / 
# Wed, 31 Jan 2024 22:47:01 GMT
CMD ["bash"]
# Fri, 02 Feb 2024 02:25:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:30dca4c17f72b09129956e26ae0841f8c684bf0810e63983ab453762044c668b`  
		Last Modified: Wed, 31 Jan 2024 22:53:21 GMT  
		Size: 46.9 MB (46892605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e6a602f4bf46f38d84ca21598d3b5c8d8cd9291a8b80057f8063d0308237cf9`  
		Last Modified: Fri, 02 Feb 2024 02:29:52 GMT  
		Size: 22.1 MB (22110720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:9e3db3937a4305ab49d8eda5fd1e314e93e2c0f3ce2b42d445d85d32baa8e37c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.8 MB (75758002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9698bc796186610ee6dee8989c9eb771a9941c97cf3fdaa57fc9aca8f20ea3d8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:46:18 GMT
ADD file:22615a550fb316cdf09ee3c185139fbdb9bf6b776c7f96bba26ba5cc5b14fbb4 in / 
# Wed, 31 Jan 2024 22:46:19 GMT
CMD ["bash"]
# Fri, 02 Feb 2024 00:47:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:b24f8e2b921fe314282df3bbfa20988c1046ee499441de80fd5229551987d1eb`  
		Last Modified: Wed, 31 Jan 2024 22:52:31 GMT  
		Size: 52.2 MB (52161387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25c4512a32748f0e93f76775383772932810e78398b7fc5a25c81e38a202a60f`  
		Last Modified: Fri, 02 Feb 2024 01:06:57 GMT  
		Size: 23.6 MB (23596615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:6439562975c8cabcfdf34862ddc6d02f6bdcdeb17df571aa406a928d07a0bfec
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.1 MB (78071510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc88dafe8aed02987ad83dc9438108f74887677f82061f88ad2551cef6f889af`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:41:43 GMT
ADD file:443c10cf2bd14299f3b496a80df4429c5642d898fb2f3e8c184e8c4d58fb8cd2 in / 
# Wed, 31 Jan 2024 22:41:44 GMT
CMD ["bash"]
# Fri, 02 Feb 2024 00:38:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:c71e0026d29ede0429851d35323a9a769fb82ad7760740b559b172f3789ae3b7`  
		Last Modified: Wed, 31 Jan 2024 22:49:09 GMT  
		Size: 53.1 MB (53140039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84d65910f8e6ecd215a4cfaada6490da4c0f4366147a1cc7a5c79cab0ae7f7fd`  
		Last Modified: Fri, 02 Feb 2024 00:41:55 GMT  
		Size: 24.9 MB (24931471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:21ec5313fd1457ca59dcf375c12cafac4a4611ebe538337b6ff190e04df56ee9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.6 MB (75612218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61e6255bd7972476b0d526c4d9f9b54ebc1b4dd2ebffc4ff2655ca168442fa16`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:34:03 GMT
ADD file:534203d126346e48b8c0d0430dcecaa093294a7a3c98d571701aab3e6c36d391 in / 
# Wed, 31 Jan 2024 22:34:09 GMT
CMD ["bash"]
# Fri, 02 Feb 2024 01:06:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:b3d1be35073c977f0bb775d26df73db32aabd06a76b52f045f43c249f737a518`  
		Last Modified: Wed, 31 Jan 2024 22:45:28 GMT  
		Size: 51.4 MB (51373756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f66eaa0ef2d3a43d454ccecb5a8fe8fa3b404d14c1ba170162b92b5af9de940`  
		Last Modified: Fri, 02 Feb 2024 01:15:50 GMT  
		Size: 24.2 MB (24238462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:d59e4fac0b969781c28610b951bf8eb8a57c48d355e11d1b8887e98e8678b4a9
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.5 MB (82451067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60a4d9065304aed90b2672ecb6051043e0535de87a78930564cc8537b57b87d5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:32:14 GMT
ADD file:9862d7fda5f3fc5c48229d44a182f0619051f084c461b10ae5cd841f609dd876 in / 
# Wed, 31 Jan 2024 22:32:17 GMT
CMD ["bash"]
# Fri, 02 Feb 2024 01:52:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:fbf7f53bb9540a00260474ff7da2e470dc3eecfdc9849d2cfb73bb9e5f549622`  
		Last Modified: Wed, 31 Jan 2024 22:38:21 GMT  
		Size: 56.2 MB (56198785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92c66c2f24b74b885aed137e39b5414d66a8906b77e1d860f925d28c45bbbdbc`  
		Last Modified: Fri, 02 Feb 2024 02:30:49 GMT  
		Size: 26.3 MB (26252282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:ac91fe14bc5679daebfd5242044b3ab23d236734ed5b09d91fa090705e8339d5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.6 MB (76620308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c87c04436a08f3abb6c4a7e54ef408f89b2eef9dc20e929b6a0d56ca34d23f81`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:18:29 GMT
ADD file:3b31c2bd33a3d7e6352823413292afa26a09dbcdbc56396202701f16e609204c in / 
# Wed, 31 Jan 2024 23:18:33 GMT
CMD ["bash"]
# Fri, 02 Feb 2024 00:58:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:651c4bce8b545a7028c9eea81f8b25dae93c9bf0073fff7020f5784448310184`  
		Last Modified: Wed, 31 Jan 2024 23:31:42 GMT  
		Size: 51.7 MB (51697772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db85ac82864171f5b39a8cef06755753f3688ade2c0de1df1df59738ce25afd0`  
		Last Modified: Fri, 02 Feb 2024 01:32:15 GMT  
		Size: 24.9 MB (24922536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
