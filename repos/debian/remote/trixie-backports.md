## `debian:trixie-backports`

```console
$ docker pull debian@sha256:14e9e3d0c23c05c12175a863516e896418ae86d981436a20eb023ae84a750654
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
$ docker pull debian@sha256:544b0da0f58a85464355a374791306a786ebfe3c67ec85b47692646408cd5d25
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.8 MB (52821432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:875af3078eb1c8adfa61705fb0c573efb755804bba9de7fab666075bad88651d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 05:26:17 GMT
ADD file:aeee476035b2ce2f3c795377011e41eae116861792cc7c02090d8c6e0e5b40e9 in / 
# Tue, 23 Jul 2024 05:26:17 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 05:26:22 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:2c622000fb34abccd4a19243f49979fc534d754c97f8e18457162c25dfabe489`  
		Last Modified: Tue, 23 Jul 2024 05:30:46 GMT  
		Size: 52.8 MB (52821206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6ea93c926a5b98ae4bfd648f517f56301330b3d764ade5855eb156d9ca24188`  
		Last Modified: Tue, 23 Jul 2024 05:30:54 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:trixie-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:d670980a816d41e67884e2e6362d7ecf13974d180dfbe616080b4612572d1aee
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.8 MB (49808014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a339cca91f54a55abd22031c0c2276230da32dbb95272337589a80c8a525bf6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 22 Jul 2024 23:59:14 GMT
ADD file:03b45e1df3fc6931a8ddcada5ff0a44361f55a5f77b85b332a37efac67af70c7 in / 
# Mon, 22 Jul 2024 23:59:15 GMT
CMD ["bash"]
# Mon, 22 Jul 2024 23:59:19 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:7c6b0161e34fdad02b8c4ce71aed07442e95f3916056ffa8fc8957d554429aa6`  
		Last Modified: Tue, 23 Jul 2024 00:04:42 GMT  
		Size: 49.8 MB (49807789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7046a408a813975b8617ef7b12c2cbfcc82c574869e592efb7277e67ad4974d`  
		Last Modified: Tue, 23 Jul 2024 00:04:50 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:trixie-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:2290e885f6f19bb38c67fe028042d15feeaa781bea3d93a4551251bc5c36bbcb
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47313668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8da24eb64ffd60de393f35f309132273397b8c760a14657709ed65e453197994`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 03:05:07 GMT
ADD file:b71b90e852d24ff72e11c891781becf7dff5c6b7913fe6f75d4afaaf9dd0fb77 in / 
# Tue, 23 Jul 2024 03:05:09 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:05:14 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:6a5c1f2df69e68e08287b3688c735ace9ad27b45503738288df9d10ef7066ce1`  
		Last Modified: Tue, 23 Jul 2024 03:10:02 GMT  
		Size: 47.3 MB (47313443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eae643c601e7173c20384bb5c60091cbc879c5d8052eaedc6f804a93d633e6a9`  
		Last Modified: Tue, 23 Jul 2024 03:10:10 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:trixie-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:4758b7440faa2a10bcf78fe12c7dc27addbda3a7baf46e4eedeacdab5a3eede5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.0 MB (53026546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28148e2b0e1ee6d334732745d16398405f258eb999c6fa3a5826e41e0469c064`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 04:19:11 GMT
ADD file:36c12887052d1b06bbaec01740a2cd1b9dab4bc7827e406c3311158554478418 in / 
# Tue, 23 Jul 2024 04:19:11 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 04:19:14 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:493524e4a43f41421b39cb784ceebfde54145b94187eac6910c35f8178b410da`  
		Last Modified: Tue, 23 Jul 2024 04:23:05 GMT  
		Size: 53.0 MB (53026321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2469f1cc9375e6b2c7625cccab0071ee8da7da45316f8543b0815557750c5e3c`  
		Last Modified: Tue, 23 Jul 2024 04:24:15 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:trixie-backports` - linux; 386

```console
$ docker pull debian@sha256:113a2d52edca8eb9a086b23574bafa33c02597a7ecc612b4adf00cf5a5a15ae9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53681472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ba4edc12c553a6a7fb3701f52d4e85b9d476d9518bbf7b4b92b284180d15e90`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 03:56:12 GMT
ADD file:01a40f7b1e06135068b561ea73bceefb80384e78cf04f7afc30b29280b89be42 in / 
# Tue, 23 Jul 2024 03:56:13 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:56:16 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:603ccf6e4399370cd3c9b421529967f58d124fe253b75b4d92b2e58cf112fdbb`  
		Last Modified: Tue, 23 Jul 2024 04:01:16 GMT  
		Size: 53.7 MB (53681250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a21b617a8653369afcbe6261e920cee6a69a6c51b9b27a05a2506fccee3f5b8c`  
		Last Modified: Tue, 23 Jul 2024 04:01:24 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:trixie-backports` - linux; mips64le

```console
$ docker pull debian@sha256:1ba1ca654640e33bc718bf00f610e4fd7b1952905f2bc24fef32a936ce06c1c3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51636377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:989a159a7170837719551d5369504afec38a26d0200872626ed943136dd7bfe3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 00:44:48 GMT
ADD file:392fc10c04bd3df02b9ce57b447e54a4d1bcdfb0ec61a622808e7db6f2f1914f in / 
# Tue, 23 Jul 2024 00:44:54 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 00:45:08 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:4c50956a8a7195506ef530c7c5f445057322dc9fe660c45a79ea6c6084874804`  
		Last Modified: Tue, 23 Jul 2024 00:56:14 GMT  
		Size: 51.6 MB (51636151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb344e61ca4b1920ded001ec4d3c85696d2437f9502f1da860ce08669a12dd86`  
		Last Modified: Tue, 23 Jul 2024 00:56:24 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:trixie-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:bcd838d80d52bf52640b6b0dd858d4a33d962cdcbab35b868d06077f2d3ab2ad
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.7 MB (56722294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1d8bbfb73bc4819bc518162c6c378a4689960e8270dbb9a7342d88eef682e5e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 01:29:19 GMT
ADD file:3a2bd17a40219dbb040555571523f8df1fea9b1d1a82249388c40cefedfa6de9 in / 
# Tue, 23 Jul 2024 01:29:22 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 01:29:26 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:ef086634154fd58171058df19eb35df551381968a0480be4625baa26e8bd8a54`  
		Last Modified: Tue, 23 Jul 2024 01:34:29 GMT  
		Size: 56.7 MB (56722073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:966b7286c6844b090752a2bf1284668f5882254c8ee8655f67ba81e22eade8a9`  
		Last Modified: Tue, 23 Jul 2024 01:34:37 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:trixie-backports` - linux; riscv64

```console
$ docker pull debian@sha256:a812c3bcae61f3700d231d79a0679b69c16962ece3df7dd03a8fb1e0d3d93f1b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51127453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adfc1bb2a312815637f12f02afb703303293e014a146b690c7e09dbe8bd949d2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:13:20 GMT
ADD file:83cbcb6055e53dd5bbbdb284d5c1129bd8ef0b02c2f174e4bad8a86a9a470700 in / 
# Tue, 13 Aug 2024 00:13:22 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 00:13:31 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:664f4e8f311a644728086c0fb1ccd2a113bc5c8af1174d6b42e68ae243e81646`  
		Last Modified: Tue, 13 Aug 2024 00:18:53 GMT  
		Size: 51.1 MB (51127228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:758427a149e223d282ca6a4fc1598c1b14113db8e71e801e1bd2642cbf03596a`  
		Last Modified: Tue, 13 Aug 2024 00:19:03 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:trixie-backports` - linux; s390x

```console
$ docker pull debian@sha256:5b905b6ed3bf9f169dd7abd2100ed17921ae71f3c2807b810c933db75b7e5737
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.4 MB (52414463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee6afbbdac07c82a37b36db2ac9a728882bef68edd337f4c44c086d9f763c613`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 02:30:46 GMT
ADD file:5991487b53c92b85f56a9cb6ec51789428cf5b58777f5dee12014b0223fc1434 in / 
# Tue, 23 Jul 2024 02:30:48 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 02:30:56 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:6deaf86d1b7bfd5bc637ea83983f978199741e71e1597a41b9ad7983be78ad34`  
		Last Modified: Tue, 23 Jul 2024 02:35:01 GMT  
		Size: 52.4 MB (52414237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccb1f82a3ea59b1c2ade78c257ae6f044831c77125ce9ca7c8c2b9ccd5df00ff`  
		Last Modified: Tue, 23 Jul 2024 02:35:07 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
