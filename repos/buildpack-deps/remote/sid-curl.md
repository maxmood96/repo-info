## `buildpack-deps:sid-curl`

```console
$ docker pull buildpack-deps@sha256:90ba33d3d03eedb8292fb91f12568c4412f1628b0ad7c78c7d83982d754ea793
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
$ docker pull buildpack-deps@sha256:6943f938d9951b7d261762647568d3778d3ed55905019227091541b7889e9fa6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.2 MB (72178551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:654515af3131c5fcf8190e81562db736635066cccdbc3dac39e30ca8a39491ad`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 04:05:54 GMT
ADD file:20b1068c276c223839818edd0aca3981a1b8139130064d19f9ec38e26a94ff27 in / 
# Thu, 17 Mar 2022 04:05:54 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 06:33:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 06:33:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:ab40a96ab944197ee11d696f776db9c1130db9825e9996a5e8939611fcf5e470`  
		Last Modified: Thu, 17 Mar 2022 04:12:27 GMT  
		Size: 56.0 MB (55984715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:214f624759443498bdf804a19e1294b81976d28ed00d521e85a6ef33658ab378`  
		Last Modified: Fri, 18 Mar 2022 07:05:57 GMT  
		Size: 5.3 MB (5269458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e59203613ecfdfcaa48f715e4d48dfb31fde19bed9d8d6dd6886973ca3d859f7`  
		Last Modified: Fri, 18 Mar 2022 07:05:57 GMT  
		Size: 10.9 MB (10924378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:4bb272a6ebaaa0a79167b0b2ee6cbd8a7e70a9318992c7dd4cce7bbf43f6a2a7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.2 MB (69155478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49b65e3b02efe40bbefb5f21eee3ee01b5d1b4705371e621e152ca738f8dd885`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 05:23:03 GMT
ADD file:a9d4a5aa739c9c980a2e0b3342f616a0ef24327457038a7d2d1f054b47bb869d in / 
# Thu, 17 Mar 2022 05:23:04 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 19:24:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 19:24:54 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:c1b1560f4e7f4d5dc335516eb5f16007a5ba8efcbedcc5584f361684738e508d`  
		Last Modified: Thu, 17 Mar 2022 05:39:40 GMT  
		Size: 53.4 MB (53393523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d3688991f52d334055cd012a6287b39073e9b4ac6c7cd7012b2c8be6c4cf410`  
		Last Modified: Thu, 17 Mar 2022 19:44:30 GMT  
		Size: 5.2 MB (5164495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:247526418f56b9d635ff39e99bd9d2058cdf75fa52ee8a6fb0e2a007868a5e12`  
		Last Modified: Thu, 17 Mar 2022 19:44:32 GMT  
		Size: 10.6 MB (10597460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:fcb99ce3e04494216fd202644de8f8dd1076a25b12318ab6fb5279aed228f74d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66272565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f709c5b39e66bf76fae317ee39d2b2e26fc951c7ab758c004c2015ed29e98f1b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:06:51 GMT
ADD file:6d4b498179cf5ce76b5c392522e45f7c4c4d0d4bfecee20cf2e30c39ab2c209f in / 
# Tue, 01 Mar 2022 02:06:52 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 09:33:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 09:34:01 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:1c659af384e72219bee43c78d09cffa65613c854ea39a8d72326f2897f1c899d`  
		Last Modified: Tue, 01 Mar 2022 02:23:24 GMT  
		Size: 51.0 MB (50991190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e00022efa6a0aec733e4d12aa18f38e4a2938f4f051f6e9e8c3e2046f1ff2f9c`  
		Last Modified: Tue, 01 Mar 2022 09:56:41 GMT  
		Size: 5.0 MB (5035167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81db15ace667b6657bcdacc04d0531c5cd45fd704d5e17e4addddfa52a907051`  
		Last Modified: Tue, 01 Mar 2022 09:56:42 GMT  
		Size: 10.2 MB (10246208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:fe0129a4c5f9d9d223e94383888c344f377cd2762f33dc7accebefe230cc39bd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.9 MB (70865563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d077ad99748ee748b802513089e80e0d67ec10fa7b9b79135fda0bfa1481a294`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 03:23:19 GMT
ADD file:1d38d88879da25d9a1bc7a4c5e36bc54d45209f4c931e6da3f7a5121498cecf5 in / 
# Thu, 17 Mar 2022 03:23:20 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 22:13:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 22:13:54 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:d1bb23fb7eb3b065e76a0f28cfe8d85ecc762b7cff467fdbcda2f70363c88087`  
		Last Modified: Thu, 17 Mar 2022 03:31:11 GMT  
		Size: 54.9 MB (54916866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94c42e541f9a190ed5b1572f38d77d9a07c7899f7b9640e25460c12e849991f1`  
		Last Modified: Thu, 17 Mar 2022 22:23:20 GMT  
		Size: 5.3 MB (5255457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:556c64db2922b5a87b5591ed9b67221014a21677b094903b77fc24099a5a1f3c`  
		Last Modified: Thu, 17 Mar 2022 22:23:21 GMT  
		Size: 10.7 MB (10693240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:cf918a40def0ef2a54f8aa34f15c84c35383777e1fb1019b778d1c40ebb8130e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.7 MB (73736777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd9416a3cf6ac3af32a1df140b38f25850e253e092a6f07a6f0d40bff60603f1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:09:17 GMT
ADD file:cc05e2e409ddf6094d6143fb5d4b47dfb3390bc7281658217d6456c28a94c208 in / 
# Tue, 01 Mar 2022 02:09:17 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 05:44:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 05:44:39 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:fe6e66c27ed7931bded2ff21e1416e6590e3576bb223676ce7abc704e1326545`  
		Last Modified: Tue, 01 Mar 2022 02:18:48 GMT  
		Size: 57.0 MB (57009099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7111e6839c4aa2db70f0f1ec148e3436b2b0964e461965e85327ded44355cb32`  
		Last Modified: Tue, 01 Mar 2022 05:55:11 GMT  
		Size: 5.4 MB (5407372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31ee5a5a98edeffbc2270186d55a9d2f1ea5dea3a894a3a0b2cf2ed8cf132b99`  
		Last Modified: Tue, 01 Mar 2022 05:55:12 GMT  
		Size: 11.3 MB (11320306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:76e4ba4f0f4227dc356e98d2b19d6b38806c0bf8c7368b8952a7117bc4a746fe
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.5 MB (70532432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8df2597a07c8932d760644ad5adb1de05d3e26e7f9d1651f298de4c082fd05d1`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 08:55:47 GMT
ADD file:2015a98f802a1e28eca2c4eba0b574f58c2cd7844c0d94dbf0e29e8180aea210 in / 
# Thu, 17 Mar 2022 08:55:51 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 19:38:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 19:39:35 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:3d194d6caec7e92bc6e1448edd24c61790b7372a62bd6808d5cd0c5a6eda1736`  
		Last Modified: Thu, 17 Mar 2022 10:46:33 GMT  
		Size: 54.6 MB (54636832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c6d8d6c495a88dc95c7cdb4d3ae2e01617fbe355ec506b682a16ac6bd71546a`  
		Last Modified: Thu, 17 Mar 2022 19:57:08 GMT  
		Size: 5.2 MB (5222583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91053236c731557db21c8cae8dadcde7f25967ff5d460c9f67f4789ecb8b3be7`  
		Last Modified: Thu, 17 Mar 2022 19:57:10 GMT  
		Size: 10.7 MB (10673017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:513d32b1d653847f4f012a0d9227aab2d8186fde78d49220e81dd5838881dc35
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.6 MB (77636462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6d9f7706bd5f1dc2e9e2f17b934432b336e61682cd1b3370b1e378d0b3b4869`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:07:35 GMT
ADD file:b9f003037b742d278d03bf492fdacca507aed7e40b6e3727c8e5053d83d7d356 in / 
# Tue, 01 Mar 2022 02:07:43 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 07:30:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 07:30:38 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:071265fa048a30ea363f6d7ac648ffe04d00265431517a6f41931d6009cba801`  
		Last Modified: Tue, 01 Mar 2022 02:17:38 GMT  
		Size: 60.4 MB (60392664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78f2a2974e7f09a087305fde1cbea3479f9c172ddfb12eedebe53cd4ec065cd4`  
		Last Modified: Tue, 01 Mar 2022 07:45:03 GMT  
		Size: 5.5 MB (5543587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce69ed89337ee2d370f6c9b149d277c8c1c479029a4113ddbfaa0b6783949565`  
		Last Modified: Tue, 01 Mar 2022 07:45:04 GMT  
		Size: 11.7 MB (11700211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:c3980de3ed3b025c0d84d5e38516aaccca3a7acdeb4125424201686281a029b3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.1 MB (67060604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:650dfff09d8b84ea9c4bbf1943958bb863e0d56c07c84dfaeb67baf2ec1491a0`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 01:14:42 GMT
ADD file:a994e723b30499cbdba960284559bdde2e3abee2fdcb763fdd233da95dafe147 in / 
# Thu, 17 Mar 2022 01:14:44 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 02:01:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 02:02:50 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:271cb4a0cf55f464e243d145aec35f35f8228420ef9aefb2a52eaabc09bf5c50`  
		Last Modified: Thu, 17 Mar 2022 01:33:41 GMT  
		Size: 51.7 MB (51661116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cead6fedbff27583eae8cbd457b531667d28b94bafbb24b1402d794d4c55ec0`  
		Last Modified: Thu, 17 Mar 2022 02:34:04 GMT  
		Size: 5.1 MB (5077182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c8e5e53be16547420594001f871619cc0c003f8d23528375b0f6c4550aaa2f2`  
		Last Modified: Thu, 17 Mar 2022 02:34:07 GMT  
		Size: 10.3 MB (10322306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:71adb0264e2f56a313869a4d1c35ba7e8c550b5786fb9286fd6ae3cfd04bf22c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.3 MB (70312008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d276887bea2c86045740e207e7f8d0a86772f49f7531a5cb9a3872fe238c6125`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 03:08:11 GMT
ADD file:4a7b0c9e8bc60d35d06240af5417427853918fe6624688050d4aca10a22b433f in / 
# Thu, 17 Mar 2022 03:08:14 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 18:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 18:23:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:8e1d6cb1e553f745f248c4d7a409401acdb697f1bd597e8c1c08d6fcd5db0f2d`  
		Last Modified: Thu, 17 Mar 2022 03:13:59 GMT  
		Size: 54.2 MB (54246705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99267e3e8ccd599670f5059d59cf2f80cafc0773fc8b74ba953d5d5cb2189fed`  
		Last Modified: Thu, 17 Mar 2022 18:30:46 GMT  
		Size: 5.2 MB (5245707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3282440b854d7908290c041b1619604c86d6fb3ec5e2ed67356bbd4ef1847863`  
		Last Modified: Thu, 17 Mar 2022 18:30:47 GMT  
		Size: 10.8 MB (10819596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
