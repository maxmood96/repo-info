## `buildpack-deps:testing-curl`

```console
$ docker pull buildpack-deps@sha256:bd44b1c92c80ab958e7f4ab7aa20cf8852f7dc1509b86bc30a243810267894a8
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

### `buildpack-deps:testing-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:329fc0881ca3ce9edb25230bbfe199cc68c98c5ed74cc0e4ab082559a3a7540e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.9 MB (73884877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6169a54b9e4c1e1771ca845cd6d60b8c02eadaa57f758aa051ebaf02a06c94a2`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 00:22:22 GMT
ADD file:1dbb9219e4db2c44c251f0ada692f495f60d7f7206c6921c094608440df579c0 in / 
# Thu, 17 Oct 2024 00:22:23 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 01:07:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:2d932a6262bf92703e4c318877f26c9f5817456038e35b8c537685fc2b40a29a`  
		Last Modified: Thu, 17 Oct 2024 00:26:49 GMT  
		Size: 53.2 MB (53238741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a3af942d5f32a53d271e49824c635bd83b9f44545e34efa1a534acbcd19cf8c`  
		Last Modified: Thu, 17 Oct 2024 01:12:47 GMT  
		Size: 20.6 MB (20646136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:58709926ec28b7598d8c8be1f1bfe83998d3f7b516d8b0ccf3ab1c475eab7885
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.8 MB (69790540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7764238980c92c8ef680edcdb7cbfe50bd21f2ac944b95e0f8a15eea026a675`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 00:55:50 GMT
ADD file:010709d78fdc05933a72549f7cb322633ad7dbe3d97bfcbda0aa10337118fb24 in / 
# Thu, 17 Oct 2024 00:55:51 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 01:32:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:f9250cc0718983393b852e9ddb20839b610fbab7fa648abee09b726c74343ff5`  
		Last Modified: Thu, 17 Oct 2024 00:59:25 GMT  
		Size: 50.1 MB (50146097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:881241cc914c17be2c506105e054bfcf46ca5dc3a2c61b399fb49563a725f97c`  
		Last Modified: Thu, 17 Oct 2024 01:37:57 GMT  
		Size: 19.6 MB (19644443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:98d0d2d989c716ceacab3193640a9356b37fa827f72314d00a0270c8006197f6
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66262823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e7602a452f4245dfc17d03f43f1bc3130eebba36523027d5e4c9116d704a13c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 05:15:43 GMT
ADD file:13242b1f67d07c997aa23e4b688f29c3a6c6dd2678f15f8738e88d4e66cd5ad8 in / 
# Fri, 27 Sep 2024 05:15:45 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 07:35:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:2e00dc0285e0f577d99c5fb34081dcf709cc26a9e85129b9e7bf7486f41e9f93`  
		Last Modified: Fri, 27 Sep 2024 05:20:03 GMT  
		Size: 47.6 MB (47633953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d39e04951abf97af56dedf87c98cd7cc72052708138c6c90da2eaa7628520ed6`  
		Last Modified: Fri, 27 Sep 2024 07:42:12 GMT  
		Size: 18.6 MB (18628870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:9aef11957c014ee01c467128ef31a08b32c6953f31ab48378266d1d08cfb0599
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.7 MB (73655342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:830955de46667fa98d512e386318f49ac6b2fe117dbdd5900d9bcc4c8945eefd`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 04:39:36 GMT
ADD file:6e593c1f521506b0f2af9a3f995a4a4355898a8de85014ead699072096977336 in / 
# Fri, 27 Sep 2024 04:39:37 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:22:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:789b7eaf9779c1b4818e6bfd3f071ee22446dc33481efffa3036978d098e31d7`  
		Last Modified: Fri, 27 Sep 2024 04:43:31 GMT  
		Size: 53.6 MB (53616601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56925e2753eebe331e1e7850cdb33fa7fabb783a0365763734fb7f7fa68594e0`  
		Last Modified: Fri, 27 Sep 2024 05:27:28 GMT  
		Size: 20.0 MB (20038741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:9a0b61de3c77cbd4f3951d1b86e89f18cebda6691e831e4aa5fbdccfebade913
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.8 MB (75834438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:344e608e55235f5addc0ddae1867daa1d6cd1b8fb3ce562a6c212b6ba100a304`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 00:40:55 GMT
ADD file:4d5beb040f172554a949bc99442605b682a56e62c519e97a7b25948e06a423c7 in / 
# Thu, 17 Oct 2024 00:40:56 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 01:07:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:33d5fa78ce89fa0c095775872e03741607d5e662aede62fa388ef8ad810ffa10`  
		Last Modified: Thu, 17 Oct 2024 00:45:54 GMT  
		Size: 54.1 MB (54077458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d8bca6b1029fb346ac8c3fd8fd0242c8617b39ff467401ae5be38d72823e794`  
		Last Modified: Thu, 17 Oct 2024 01:13:34 GMT  
		Size: 21.8 MB (21756980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:c5342c0c1be81fd113cf65c7d5b9d198b26f6a8124c06b1ab51d387092ea8b8f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.1 MB (73094133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd4e344522eedc9065a33ce8949aaf3b62495d9d21aa82313866cb04812d2792`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:13:57 GMT
ADD file:7540ed5b693bb419df5aaa69483f55c19bc0566d076c5e65757a0a6fe38375a3 in / 
# Thu, 17 Oct 2024 01:14:04 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 02:00:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:bd6795a0a311ac784071ff263d2b83d646956234334d40fe908b91a1dde11378`  
		Last Modified: Thu, 17 Oct 2024 01:22:22 GMT  
		Size: 52.1 MB (52128468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3136c2a952f0ce80aeca2b6928afe3f03863f57c7fa1a03ebd2f7c0be5923c8`  
		Last Modified: Thu, 17 Oct 2024 02:15:26 GMT  
		Size: 21.0 MB (20965665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:0f63d9df29082024122add44351a7612cf62614bfbfd771fb98129f5bc5f54f2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.4 MB (80442696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:176627dbf06b953e07fe806b048b4cec595be0b658120dc1d6eed93a6050b879`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:20:15 GMT
ADD file:7d34de8e15cda6686099080e64714532070b3d06a451fa9d77a5716745974490 in / 
# Thu, 17 Oct 2024 01:20:18 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 01:48:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:8299bac21377f71d4bbd00f3075290f241c45c39e6a9a76012dbff5b62d14e88`  
		Last Modified: Thu, 17 Oct 2024 01:23:55 GMT  
		Size: 57.1 MB (57126645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abbcab475561b983c55c4a069685bc4edb3857233ed2831996472141939c0d16`  
		Last Modified: Thu, 17 Oct 2024 01:53:43 GMT  
		Size: 23.3 MB (23316051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:d20086c9074077ff1ceee825964e0d6d0df947f49720c2c02541d21cf5e589a4
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.7 MB (71667847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca742519001d8918b315e8d5682c4a1bbce6d08bf830427b8d6e31d955f86fc5`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:11:34 GMT
ADD file:a39f1e594ed2d718a6cabab2e5ea2ce29b47a86f2d43588cafbf682ddc9af2ca in / 
# Thu, 17 Oct 2024 01:11:36 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 01:52:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5c18b80e18178230beda6e484fe9dcde3f9663fa4695718e63800e23f1c0399f`  
		Last Modified: Thu, 17 Oct 2024 01:17:23 GMT  
		Size: 51.5 MB (51529184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f253dcf9a8469b142e7d68b5d2a30f0a76ae88784e658243889a6156353191c7`  
		Last Modified: Thu, 17 Oct 2024 02:01:24 GMT  
		Size: 20.1 MB (20138663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:7a815adf7f34038e8af8937945bc9715fd6dd87d23264894e5b58ec62369aef2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.2 MB (74165458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab392593f47f6c95908f64b1886eabaf06a961df79034a9462742eeb8dfbaca8`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 02:45:24 GMT
ADD file:62bc4f2057452df8dde276d456f3954e7e27a723040dd9314069695b18b4c75a in / 
# Fri, 27 Sep 2024 02:45:26 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 03:16:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5d4e554dd357d755b1103e6fac1ca2fe641d4ec4ce0581cc222f4bffe8b54c0c`  
		Last Modified: Fri, 27 Sep 2024 02:48:50 GMT  
		Size: 52.8 MB (52771035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36f683d43e465332ea4b3a44a602cd96364371abbd8a8e9766b4a056ad242572`  
		Last Modified: Fri, 27 Sep 2024 03:22:02 GMT  
		Size: 21.4 MB (21394423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
