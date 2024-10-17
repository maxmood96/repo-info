## `debian:trixie-backports`

```console
$ docker pull debian@sha256:e1855a1396f943a72d96ae7b1be87e328c0196e3973dbb3d740f3c29a7136df8
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

### `debian:trixie-backports` - linux; amd64

```console
$ docker pull debian@sha256:1267923c619ee5def03216507595480faca1092ebc1611d9bb477a78555d04af
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53238963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:655790310709c57765b72828f221283f692291a09fc4c7fca3cf5478d79ffa45`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 00:22:22 GMT
ADD file:1dbb9219e4db2c44c251f0ada692f495f60d7f7206c6921c094608440df579c0 in / 
# Thu, 17 Oct 2024 00:22:23 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 00:22:28 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:2d932a6262bf92703e4c318877f26c9f5817456038e35b8c537685fc2b40a29a`  
		Last Modified: Thu, 17 Oct 2024 00:26:49 GMT  
		Size: 53.2 MB (53238741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16e155fbbd3ef115cdc11a5fb249b55d7b70acc80f857011b5898b4624377121`  
		Last Modified: Thu, 17 Oct 2024 00:26:56 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:trixie-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:308845b62b86b5de23df1d2538783d211ffcdfd4a92a9c74dbffdf6d566f793f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50146321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce8b3092e25aac878b9bd42a956fc653967bb2a3a5cddb4d8dc79aadd6f9387a`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 00:55:50 GMT
ADD file:010709d78fdc05933a72549f7cb322633ad7dbe3d97bfcbda0aa10337118fb24 in / 
# Thu, 17 Oct 2024 00:55:51 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 00:55:56 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:f9250cc0718983393b852e9ddb20839b610fbab7fa648abee09b726c74343ff5`  
		Last Modified: Thu, 17 Oct 2024 00:59:25 GMT  
		Size: 50.1 MB (50146097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f80b98595d538eb16731477aabc364e7e2be206758e55234545bf718aefed64a`  
		Last Modified: Thu, 17 Oct 2024 00:59:34 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:trixie-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:e9fa3a7c9815885bea54de1ef8535aec61bb0b10a2299f3d5d6f73c1dbaa6c50
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47659865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60f5d75c76c36bc8bd7682d77a14c1f81388e73d7b80a5c72f1240784bd64eb6`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 03:05:25 GMT
ADD file:7b183110c42f24584c122a8e76db1e925d5fd8b3489ae273dbca0b0cc3bc0090 in / 
# Thu, 17 Oct 2024 03:05:26 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 03:05:30 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:a5589eaa1616610f1da5585cd04faf9e418fe913dd4e9ef827abdbe93f8caa5b`  
		Last Modified: Thu, 17 Oct 2024 03:10:29 GMT  
		Size: 47.7 MB (47659640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9b91211d7d8f544c2499de2337f3eeb25ac3db05fea31c54ce4e3b43288124f`  
		Last Modified: Thu, 17 Oct 2024 03:10:36 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:trixie-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:7592d15e0a4a0b2056bfdd99e0dc6a6591f7b44355a573a5ed2ba4425a903202
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 MB (53599946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d7056c13d9e2289f082545d0a43f1790048ea6ac6009506dfcba75499accce9`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:13:19 GMT
ADD file:5d91cfda460a83c91802e918bddf6951978599b67dbd5e3c0a492a53f20d6ad6 in / 
# Thu, 17 Oct 2024 01:13:19 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 01:13:22 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:6f4ac25c892a8a547634a70e67af9f356a5f2b1f34e7c78d52074f2a21999111`  
		Last Modified: Thu, 17 Oct 2024 01:17:18 GMT  
		Size: 53.6 MB (53599725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6d1731b934e4a91f798a1e036469ff4db5d894f8092b226eea25c9f31bf0406`  
		Last Modified: Thu, 17 Oct 2024 01:17:25 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:trixie-backports` - linux; 386

```console
$ docker pull debian@sha256:b1fe3d4f699162db4464e9b66ec419ae36c48c2432457538bbc7a734e1abf741
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.1 MB (54077679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bf2fc722e05e19c01e62861a880deaf956b9f7dace8315415660a2f7c6a9629`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 00:40:55 GMT
ADD file:4d5beb040f172554a949bc99442605b682a56e62c519e97a7b25948e06a423c7 in / 
# Thu, 17 Oct 2024 00:40:56 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 00:40:59 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:33d5fa78ce89fa0c095775872e03741607d5e662aede62fa388ef8ad810ffa10`  
		Last Modified: Thu, 17 Oct 2024 00:45:54 GMT  
		Size: 54.1 MB (54077458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24a59559521df839e245332d5a16e23ba795763959727cef4438da2596126781`  
		Last Modified: Thu, 17 Oct 2024 00:46:01 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:trixie-backports` - linux; mips64le

```console
$ docker pull debian@sha256:37b7b47b332a6953bc7de74fbe25f6b30f8d9c9cbf4edd5082a548c1e0ff827b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.1 MB (52128694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7ac076af85c0a64bc868d628a3454116567acab008aa9d5729da102f5a83126`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:13:57 GMT
ADD file:7540ed5b693bb419df5aaa69483f55c19bc0566d076c5e65757a0a6fe38375a3 in / 
# Thu, 17 Oct 2024 01:14:04 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 01:14:18 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:bd6795a0a311ac784071ff263d2b83d646956234334d40fe908b91a1dde11378`  
		Last Modified: Thu, 17 Oct 2024 01:22:22 GMT  
		Size: 52.1 MB (52128468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15331233c22c12b7ad1f183099509439c110eee20c7ad9fcd4c234d261ab9364`  
		Last Modified: Thu, 17 Oct 2024 01:22:31 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:trixie-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:9d388e16600960df8393471e3b601a3a9f32432c21b465a69bbe03aca0421a68
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.1 MB (57126867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8a2e73de73380816a0a4beb1bcc5b482d245347316cbb157f6f6dd6cb792736`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:20:15 GMT
ADD file:7d34de8e15cda6686099080e64714532070b3d06a451fa9d77a5716745974490 in / 
# Thu, 17 Oct 2024 01:20:18 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 01:20:23 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:8299bac21377f71d4bbd00f3075290f241c45c39e6a9a76012dbff5b62d14e88`  
		Last Modified: Thu, 17 Oct 2024 01:23:55 GMT  
		Size: 57.1 MB (57126645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc575560f5655a0e9ad5d7dd0a67078d0346512094472ab57bc0182e05bb2bcb`  
		Last Modified: Thu, 17 Oct 2024 01:24:03 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:trixie-backports` - linux; riscv64

```console
$ docker pull debian@sha256:ec82114c5aba4554e0c3d336568cac05b98ee76774254109f56cbb7997fdbbac
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.5 MB (51529408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae9b9222265ed582899c4af4ca3367c523d1290e48464a6c1e38d9b530cdb5b7`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:11:34 GMT
ADD file:a39f1e594ed2d718a6cabab2e5ea2ce29b47a86f2d43588cafbf682ddc9af2ca in / 
# Thu, 17 Oct 2024 01:11:36 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 01:11:50 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:5c18b80e18178230beda6e484fe9dcde3f9663fa4695718e63800e23f1c0399f`  
		Last Modified: Thu, 17 Oct 2024 01:17:23 GMT  
		Size: 51.5 MB (51529184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a36a458de58d650a9681e1f8dfafa76cfa85716df2c26ab009a22f84785ace78`  
		Last Modified: Thu, 17 Oct 2024 01:17:32 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:trixie-backports` - linux; s390x

```console
$ docker pull debian@sha256:604057248718d579732296d74a2a2b2c0379e58381af4f90745b148b065ee03c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.8 MB (52809065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1ac8b340865872098b08f01ebb8e9a7e97557172cc0e90791d0bb359ef95611`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:48:13 GMT
ADD file:fe7c88cb45fa7097d71f60ba00c0d6ad76dd030e8e34771e5ee3735b59a4d6e6 in / 
# Thu, 17 Oct 2024 01:48:15 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 01:48:24 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:53440987c87b8deb9090e5298bf822ffc945f186eb4c81cecc0ebf58717ca549`  
		Last Modified: Thu, 17 Oct 2024 01:51:55 GMT  
		Size: 52.8 MB (52808844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80f3df64a7055472506cfe7d911f4d6aae7fb17131f40b794f240aaea7432136`  
		Last Modified: Thu, 17 Oct 2024 01:52:00 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
