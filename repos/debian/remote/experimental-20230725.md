## `debian:experimental-20230725`

```console
$ docker pull debian@sha256:c826285338d9d5922466321759653d069fd68d3a0dba67caf430074bbbb6f8f1
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

### `debian:experimental-20230725` - linux; amd64

```console
$ docker pull debian@sha256:d7d7b380cfc3a8478cffe49a2b4aea480fd473ecf0a49cf46b26de03e43c6c08
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49463171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff87772c806922ee2b2f01ca9f2fb2cdf80c12b02fa90a848072b356525f464f`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jul 2023 23:27:50 GMT
ADD file:e7cc602313479915aa6d96a8e0e8b26ef2e019e509dcb322fed784b25c0b1335 in / 
# Thu, 27 Jul 2023 23:27:51 GMT
CMD ["bash"]
# Thu, 27 Jul 2023 23:28:04 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:f56ab639b79f292f69be1679909a91e43b43f83d21562229738db9c77eec194d`  
		Last Modified: Thu, 27 Jul 2023 23:34:22 GMT  
		Size: 49.5 MB (49462949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:870c2f68348f0a94ebc02d093b01d02d7692a7211cabcf5c4e2217531e0dfc77`  
		Last Modified: Thu, 27 Jul 2023 23:34:43 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental-20230725` - linux; arm variant v5

```console
$ docker pull debian@sha256:25a6ce57c161fd2f6f0f84f4f920c9ab59148c80d2a00dafa160552ceb314c21
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47221588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11622f85bd423eca25e15aad328df0f552c8450aff755f5ed4bfaae0924d0d35`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jul 2023 23:50:12 GMT
ADD file:9279090ea7e122cc4f9e36d6bbaca5a3f1ac560e6f9ae9425ad4206f21e5420b in / 
# Thu, 27 Jul 2023 23:50:12 GMT
CMD ["bash"]
# Thu, 27 Jul 2023 23:50:21 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:4b16b677a781f60591648eab1255b4057b22039a7c01021a47fce85fd8f08227`  
		Last Modified: Thu, 27 Jul 2023 23:55:18 GMT  
		Size: 47.2 MB (47221365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d4efda160945eaf471823e30f8d4dcf5eb9f3141534d79c1b8ded342066ff83`  
		Last Modified: Thu, 27 Jul 2023 23:55:38 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental-20230725` - linux; arm variant v7

```console
$ docker pull debian@sha256:d35f5b149ae4cfa17dcf06b8e3a5c274b93572407bbdba1a08d85feea285581d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.0 MB (45003384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c87a63884390c1805cb35dbb81d35ddf27a1adcb15663adbcac61e01887e80e9`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Jul 2023 00:01:30 GMT
ADD file:652ffce7fe593ae68aba7b8332aaa48272777ef80579006c9f355bdeee79df59 in / 
# Fri, 28 Jul 2023 00:01:31 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 00:01:44 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:25a3838c8ceafc011502cc10603a83e9efcd0bbe84d3b44abe0303913fe91ba2`  
		Last Modified: Fri, 28 Jul 2023 00:08:22 GMT  
		Size: 45.0 MB (45003162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28104c321875eadd4ee2e29205314789abf108a704cb87d32a1963abae46ad2c`  
		Last Modified: Fri, 28 Jul 2023 00:08:43 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental-20230725` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:2092bd34ed5b7b3f468748079c96eb859ee93dd55caff76085e883f9a0897415
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49385996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbbd495ab9ccdde2203cab62db7f0f301fa489db42485a8c2cd5165b6f0b94df`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jul 2023 23:44:59 GMT
ADD file:5f562f9fc86457f5e36f1efc493d2e4c33b6bdaeb0647313f627da0e54668b20 in / 
# Thu, 27 Jul 2023 23:45:00 GMT
CMD ["bash"]
# Thu, 27 Jul 2023 23:45:08 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:bae2bcfb8a372803822a72bc86bf7d3a7e33f97c85fd34649af6c0a288fda396`  
		Last Modified: Thu, 27 Jul 2023 23:51:03 GMT  
		Size: 49.4 MB (49385774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1407f97334a8bed8e1300deccbf666ea3b8607990a283ad79da7e3585ae34100`  
		Last Modified: Thu, 27 Jul 2023 23:51:23 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental-20230725` - linux; 386

```console
$ docker pull debian@sha256:fc2bd253e9aa70a4faa294d509d0ca1114eac608c211aa3850cce0014e24e1bd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50473923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c94f153f19d6ee753fd6ca6a4e1ce1a93365754998b35718ef627b9561e26381`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jul 2023 23:41:47 GMT
ADD file:d100c670fbb7aaacaade7b8731acf0d966f044dc44ff9a0da83feb50a2fe4c77 in / 
# Thu, 27 Jul 2023 23:41:48 GMT
CMD ["bash"]
# Thu, 27 Jul 2023 23:41:58 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:7a25733f1b07b40e0ee2de9f5e846bc037209942ee787daf2ccbf38c86460592`  
		Last Modified: Thu, 27 Jul 2023 23:48:59 GMT  
		Size: 50.5 MB (50473699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1ad374e256593d205fb1ea38418f32a1118d36f4edb6935422e5404df6754aa`  
		Last Modified: Thu, 27 Jul 2023 23:49:21 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental-20230725` - linux; mips64le

```console
$ docker pull debian@sha256:c5cf5696902e77995fc2063acf30f4c0e0ed98134649ef03691ac3bd71116b00
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49334852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:365d1481aa4ce96e7d2a6607a335ee8f464d951081bd345e564fd78f3880d961`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jul 2023 23:19:19 GMT
ADD file:a9d0c06c56c9a5053b0f1e0e1e9c6d6441c7aeddcb2294a331574201f618cb10 in / 
# Thu, 27 Jul 2023 23:19:25 GMT
CMD ["bash"]
# Thu, 27 Jul 2023 23:20:06 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:88dcbf9b63cc9bafb470283f20b3def1f55fac5e40385d6bf3b8a32224cd16fb`  
		Last Modified: Thu, 27 Jul 2023 23:30:43 GMT  
		Size: 49.3 MB (49334627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4923beaa002e6f49bd2e09b0749f345dea7c5645d60455e3d8d8fc34e3eca6bb`  
		Last Modified: Thu, 27 Jul 2023 23:31:22 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental-20230725` - linux; ppc64le

```console
$ docker pull debian@sha256:dfcc752a41311c5d70ef85e4c8235226fcabe527c0088efa96fda9428e36dc5b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.4 MB (53379424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c5781c7bf4a19eca59a1e94044b3ee762ae877decb4d413400a69ba4ed4852b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jul 2023 23:26:55 GMT
ADD file:59bb239f6abc9448e67220f9536853f4d6440f41365514bee5457e8121a1e6c9 in / 
# Thu, 27 Jul 2023 23:26:58 GMT
CMD ["bash"]
# Thu, 27 Jul 2023 23:27:18 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:e9f31e6e72d4e39fd189243399633d40af3b328be33843dba86a632be7c63642`  
		Last Modified: Thu, 27 Jul 2023 23:35:19 GMT  
		Size: 53.4 MB (53379201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8938822d70b6af48ef340a5ef6e1446e6f5f9cb4aafef99aa813fedb26ecc36c`  
		Last Modified: Thu, 27 Jul 2023 23:35:52 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental-20230725` - linux; riscv64

```console
$ docker pull debian@sha256:221619f0d1fcbf09705c435a88d81c06a255f68eab2c9f54735ea874745f2a35
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45657174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f76c54b7f1b7b7b6081068311ca6305e3740f16a9db758f5c6b546504a4bfc1`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jul 2023 23:11:04 GMT
ADD file:64a64f7f9d3c1b069cedb0fd6808e4df4f1b5cf426db8d67146e596b67b66e0b in / 
# Thu, 27 Jul 2023 23:11:06 GMT
CMD ["bash"]
# Thu, 27 Jul 2023 23:11:42 GMT
RUN echo 'deb http://deb.debian.org/debian-ports experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:826a19f52873a2057b9a6bafcb19f07da36d3d39bdfe23edec86a6ea28bf4f72`  
		Last Modified: Thu, 27 Jul 2023 23:14:28 GMT  
		Size: 45.7 MB (45656945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce87ce3f0651366a0892e79a166d9b0ef65896955112e3719860aaabddf718d7`  
		Last Modified: Thu, 27 Jul 2023 23:15:16 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental-20230725` - linux; s390x

```console
$ docker pull debian@sha256:99bf5bc91d5d057327cae468175cdc87aca2480c424a4d33385985121a73b0c6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.9 MB (47858880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f291f67a322446915b94da0ed50bdb92c8ca6c7635f0a3a8af744bb05fa1ca06`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jul 2023 23:50:32 GMT
ADD file:17303e8f959bdac211b78c8e049d12c1507dfb79bcab51a7bad65915274950b9 in / 
# Thu, 27 Jul 2023 23:50:34 GMT
CMD ["bash"]
# Thu, 27 Jul 2023 23:50:51 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:11dddd102ef78c154129fcd2c46bd18efa2e5cfae8d3079dfebaac59f2b802a4`  
		Last Modified: Thu, 27 Jul 2023 23:55:06 GMT  
		Size: 47.9 MB (47858659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:703fbb8d1836584eabb56b1219f8e2cb48490feb1d8bdb8467f9e2daa4f714fb`  
		Last Modified: Thu, 27 Jul 2023 23:55:22 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
