## `debian:experimental`

```console
$ docker pull debian@sha256:5fbaf548cc847fc74caa74b6a9d0c0cc3ff4e6eac863f980080bb1ae3a8c3d1b
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

### `debian:experimental` - linux; amd64

```console
$ docker pull debian@sha256:c34e1569aca56b9192091930a3ed888130d68a835bcf44eae46b64098be018a2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.8 MB (55758326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1155b79982f5cb3cb4ca852f8db318fe9657f4f255df38ab0a63558d2f4e4d51`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:23:08 GMT
ADD file:db09d197fcb0e66f610eb98b792583f6ec40f708cb0d0177e510c2a158f566fa in / 
# Wed, 17 Nov 2021 02:23:09 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 02:23:19 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:a6543f35db5e93a9d2a1ff8c5abaf275a6bfe30ceb4f008f8047cacfd2d0f324`  
		Last Modified: Wed, 17 Nov 2021 02:30:33 GMT  
		Size: 55.8 MB (55758105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:510e6744cd6ef82181b5126f01e80d20252c4fd4245ffa53d41ec779ee543d1c`  
		Last Modified: Wed, 17 Nov 2021 02:30:57 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; arm variant v5

```console
$ docker pull debian@sha256:f285fb4cba39f82f3e9edf346f1ebd8f747ab13a01a16053b90799ce9e2f7ddc
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53238960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e8987a7b943d00c071d485dd3af35769aa9ddd5c18b898cf56aaefd589346db`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:57:44 GMT
ADD file:4f7ce5598f98e9f01ec7174a57364d9d28802a554530db59c008960d0a40c239 in / 
# Wed, 17 Nov 2021 02:57:45 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 02:58:18 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:5c59a35f8148e14582e723208c2af72918650b046899af2d952e25ad86cc3dd2`  
		Last Modified: Wed, 17 Nov 2021 03:16:24 GMT  
		Size: 53.2 MB (53238737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10c4cb694ca349e0fcee01dce7cc639e0e468f453e3bc939a6128afdb7ab791b`  
		Last Modified: Wed, 17 Nov 2021 03:17:06 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; arm variant v7

```console
$ docker pull debian@sha256:045e674644b35bc4a2bf075445145fe9a410f7274f66d801bea71fb370dbc5c8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50860530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aec3c000773d608dd166eee6d899e220139f9c6f4ebd0fbaedf7ed5e65944cbd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:07:01 GMT
ADD file:930f169a86ba880df2aaea12f3e8598f194b73f18795a8cd70efcd27b241bda3 in / 
# Wed, 17 Nov 2021 02:07:02 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 02:07:35 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:61a45c58489b0c8e11c36c2b4e975b6bd6dd5cd0b16c91ccb452966e84c75021`  
		Last Modified: Wed, 17 Nov 2021 02:24:50 GMT  
		Size: 50.9 MB (50860307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8647d476eb9176d77a596dd5cef2be97e3386236a4e2f12e22d27fc8742d717a`  
		Last Modified: Wed, 17 Nov 2021 02:25:31 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:6460b222d57825e8dbba8071810b435418e8459e2fc5a4a9096ebb47a83c1874
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.8 MB (54767296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6157a41c40dfece8c9e8f4aeccfec249a4c19835344d6ce672af84d61aeae663`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:43:27 GMT
ADD file:44b7578caffebde5ddfd201775779df99cb1d525113ba58609f8cdf1f47092ce in / 
# Wed, 17 Nov 2021 02:43:27 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 02:43:43 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:af0aea1ea198f6a1207b9812f667f234e3ccf829e7b41959a314d3616636bc52`  
		Last Modified: Wed, 17 Nov 2021 02:52:44 GMT  
		Size: 54.8 MB (54767075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:419ceac417071c25631219677cdd697c6d7d12c3b7071efe3130a7a7bd6910b8`  
		Last Modified: Wed, 17 Nov 2021 02:53:10 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; 386

```console
$ docker pull debian@sha256:67e28b400930f0be61f9ac08fa63a6175f1e0b860fe342583c1300cc1ce6864d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.8 MB (56817061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05c0c534ca7cb93c07b3173e666f97d46b4c01e0e0a41c3d12bf4d7db871f3ff`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:43:20 GMT
ADD file:b1c54ba84e5f6c88c1f3a56a44deef95ed0ae707568246e0aad79bfb2ad13ff7 in / 
# Wed, 17 Nov 2021 02:43:20 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 02:43:36 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:5ae2b303578d13cb8c2bec7380b5933eb31c2dc36e90d6745fabbb1efa42d287`  
		Last Modified: Wed, 17 Nov 2021 02:54:04 GMT  
		Size: 56.8 MB (56816838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:156ce42d4e4e409da10973009e6fa0698ea418b75cc8adf3f94111a79431590d`  
		Last Modified: Wed, 17 Nov 2021 02:54:32 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; mips64le

```console
$ docker pull debian@sha256:3cb33f89962a7fbe0dd037c6db997b05501c3bd2864ef5522f34e47746355cbb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.4 MB (54365685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6baa4eb242aa136297ce4887ab58269c4f82464cfc3eb6d011e953052c1fc169`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:15:00 GMT
ADD file:65990c5fc1629d9c60c5eae96c8b5b16dc64c2e1e4d049da2d9d45ca8126a2b6 in / 
# Wed, 17 Nov 2021 02:15:01 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 02:15:28 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:a0ac2e403b44e2769c44c8edeefcb754cc01a8aed8345df0bc46cedfb659667e`  
		Last Modified: Wed, 17 Nov 2021 02:26:29 GMT  
		Size: 54.4 MB (54365461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bdc3e2e4c4165a83be05dc4ec812788c45f4bd9e9aa9ba661a73512081685e3`  
		Last Modified: Wed, 17 Nov 2021 02:27:11 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; ppc64le

```console
$ docker pull debian@sha256:682b290c786b2bea60bb40637a31e82c464b357185c85c39b88365e51f94a2d0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.0 MB (60045252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fedf50d85bd176395364a6f442d183c2fbfffbaf05c51965593223f886efa87c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 03:38:38 GMT
ADD file:f98cd5c0b6d1b0eca9c66a96528f16cee04c4c39c0099aeb696452eba40f7ce5 in / 
# Wed, 17 Nov 2021 03:38:55 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 03:40:33 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:20a855c65aabb17aca96cb4aba443be5ede8aeccac91e0e21c41cf07a4ae22c2`  
		Last Modified: Wed, 17 Nov 2021 04:17:17 GMT  
		Size: 60.0 MB (60045027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8329727e1f1f8d329e49169175a09e367d1cadc563448ad984132019f26b854c`  
		Last Modified: Wed, 17 Nov 2021 04:19:16 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; riscv64

```console
$ docker pull debian@sha256:9a4fd411b6cad4efff57b06e5d7c5247dc56614442f0a923f50fd0bf50c3d0cf
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.5 MB (51522622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6a90333fb1c00ce7d932c4281569862fd236fba77d8ef4ebe04691fc75841d1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:18:02 GMT
ADD file:0ec1f46a764439430fb9f09f4839b10976be8fc64fc12afa4c027f1c62f25260 in / 
# Wed, 17 Nov 2021 02:18:04 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 02:21:13 GMT
RUN echo 'deb http://deb.debian.org/debian-ports experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:2bc932115d57a62ccf3e02aa3e687abcf6d81b71a70bd56a6c3eef683ff58d23`  
		Last Modified: Wed, 17 Nov 2021 02:34:09 GMT  
		Size: 51.5 MB (51522393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e5161a894d80361fe39f50145322762014675b9abb46699d942082d90b4dfc4`  
		Last Modified: Wed, 17 Nov 2021 02:36:47 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; s390x

```console
$ docker pull debian@sha256:d73fa202edf98345edf9e6534f97065f21b1cec3046305536c1060c47d487150
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53965842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc8704ff4f7e75c9e0aa046a651029ee9276445f9942de9fcfc702e9355478b0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:45:12 GMT
ADD file:3e240d4862da4173e8dc2b043c11c59b5b8d8ea71c087729ecc0bcedf15bc5c2 in / 
# Wed, 17 Nov 2021 02:45:15 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 02:45:32 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:e50a73e9a583b8d41392e2bc8c7f048886a3cea5c4319e2b919dfbc1866d9e9f`  
		Last Modified: Wed, 17 Nov 2021 02:51:10 GMT  
		Size: 54.0 MB (53965621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c88b35c8c27cbb17920e80d41e0eb4913c843ef5a4f7985f320cfe0c2cd0230`  
		Last Modified: Wed, 17 Nov 2021 02:51:28 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
