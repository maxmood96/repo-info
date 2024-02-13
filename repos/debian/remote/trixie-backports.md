## `debian:trixie-backports`

```console
$ docker pull debian@sha256:3d32d1ca835e849294ce77288e212251cac536cbd71cff601e81cd769030761a
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

### `debian:trixie-backports` - linux; amd64

```console
$ docker pull debian@sha256:5f54c6f78aa4878d5ec65af57b638b2641f46738fbefb5aa13c317c2dcef04cd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52331794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de6bdca3459e8fc60e099f18db15789905e60b39c5e969f9811dd4e4b8434ddc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:40:05 GMT
ADD file:fdbc095d632d315bfdea7b6a7cb53bfc7d32b5f6d604481cc9ff350c6ee09e3a in / 
# Tue, 13 Feb 2024 00:40:05 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 00:40:10 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:02ffa0574dfa0456dc05b0e175a93781ebc31447cddca3de402d11ac2734c97a`  
		Last Modified: Tue, 13 Feb 2024 00:46:31 GMT  
		Size: 52.3 MB (52331572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87d58bec1eb8de1ee0650462f8c79f2f6de71842cb9b09077273539f6ee671e3`  
		Last Modified: Tue, 13 Feb 2024 00:46:39 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:trixie-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:9a8d0faef499376ef279151bf2ecd3a56740b78edf70f362043cc21257a86606
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49418621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:376714c0a6436d6b565ca277cc2370be995e08d09b75503ec640fef3c7f62924`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:11:00 GMT
ADD file:8084501970c8177779352fb042faf935926737abda51187262ee0b2cabb246de in / 
# Tue, 13 Feb 2024 01:11:00 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:11:06 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:6eafce9f3c4ac029ffad9441b0ad63ffd00fa23ea2ac500527ce7dcf6ceec0f3`  
		Last Modified: Tue, 13 Feb 2024 01:17:23 GMT  
		Size: 49.4 MB (49418395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4adf010bef537a54714e11835bb8471bed25a8ad94819ccd5a7d1bc3fc16ed89`  
		Last Modified: Tue, 13 Feb 2024 01:17:38 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:trixie-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:dc82fa1e23d25a71353dd5ad88f67227c66bfc40848419a4b896e45bff316a81
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46892827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d1c4d30c189bb216ee322800377ee7c02f43fee386dafef11df4ae01495c5f8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:47:01 GMT
ADD file:313528f956e019639cb41933c0f6d14e7dca01353fe4ca789d7ac69e4c131ccd in / 
# Wed, 31 Jan 2024 22:47:01 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 22:47:05 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:30dca4c17f72b09129956e26ae0841f8c684bf0810e63983ab453762044c668b`  
		Last Modified: Wed, 31 Jan 2024 22:53:21 GMT  
		Size: 46.9 MB (46892605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:434b08e89e771657d8ae72e30f317dbbdb7dcc5e52032ac81fff933feed355bd`  
		Last Modified: Wed, 31 Jan 2024 22:53:30 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:trixie-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:d8b63208495d3ae41110499acae03c66aaf3a1f5bec9ebb7090b24d3bab015f6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52194335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18a0d2ce915173d77c2ba162d754a57ecd188ca2aba81c272e75a462a6e35b85`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:43:09 GMT
ADD file:b40105fd74cc055edd0e68436fc1b45799a62376b3530660f3a93d3c606cb590 in / 
# Tue, 13 Feb 2024 00:43:09 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 00:43:12 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:bcbaf42bd4ac1f9cb9ae9a8d53c22847171447fef1719f5037eaeed94f945284`  
		Last Modified: Tue, 13 Feb 2024 00:49:06 GMT  
		Size: 52.2 MB (52194112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91300bb706094513b14feca0696a64b3360c1c698d7083c7614d69a186006c11`  
		Last Modified: Tue, 13 Feb 2024 00:49:15 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:trixie-backports` - linux; 386

```console
$ docker pull debian@sha256:183e29f84b0925073c33e7ce268a63ba4b0a7fd409bc807103a4eb951902b8d0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53167199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eed4be4aad89b356de636cd0d153fb3453eda1c3fd3e66a1ae325ba240cb9ab4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:45 GMT
ADD file:48adfe9ef1da0d6e87fe297dd6cf8e9e117db33c490c41c77b6f2aadda29a275 in / 
# Tue, 13 Feb 2024 00:41:46 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 00:41:49 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:b1a72a4bdfc8e16b8965d5db9e85a05a0f23a851b8b45d3b9e7376d79f2f223b`  
		Last Modified: Tue, 13 Feb 2024 00:49:03 GMT  
		Size: 53.2 MB (53166976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c7f4b137577e35c099d34d258eb32d094487d3ab610e3ace42138ecd437bff6`  
		Last Modified: Tue, 13 Feb 2024 00:49:12 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:trixie-backports` - linux; mips64le

```console
$ docker pull debian@sha256:e16cae5c31f03f61ce53c7b1e73aca53273dd9270d7031ab7d24e0d68312a7ba
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.4 MB (51373979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a6b1d1627cb5b34e92bbc5397b98d8726a60488b46e88dac9db4a92fb3c7588`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:34:03 GMT
ADD file:534203d126346e48b8c0d0430dcecaa093294a7a3c98d571701aab3e6c36d391 in / 
# Wed, 31 Jan 2024 22:34:09 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 22:34:21 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:b3d1be35073c977f0bb775d26df73db32aabd06a76b52f045f43c249f737a518`  
		Last Modified: Wed, 31 Jan 2024 22:45:28 GMT  
		Size: 51.4 MB (51373756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65a7e48336abf84a52286d5568ffe6764283cb68c689a45d3ea6682d50aa581d`  
		Last Modified: Wed, 31 Jan 2024 22:45:38 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:trixie-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:e4bb22830ef2f502484534ca9e583d912a363a1653d9e6e9811738f444f44902
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.2 MB (56235062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:634d026a83dc95fe26bfd292b7f3d50512e65570acf3aea744f15fbcb80a40b7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:36 GMT
ADD file:20495ab1a5b590f87307401881c4392d68c4ae3aee17cd89e2196908d9ee5c75 in / 
# Tue, 13 Feb 2024 00:41:39 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 00:41:44 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:f12da478bcef0b5e264ca4e1bc3288008557f76cc25c8a87e714181c7f30ac36`  
		Last Modified: Tue, 13 Feb 2024 00:47:57 GMT  
		Size: 56.2 MB (56234839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba3431686f1ab8fb8a4d03aab8bc40794dfdef1202825159304c50e621319632`  
		Last Modified: Tue, 13 Feb 2024 00:48:06 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:trixie-backports` - linux; s390x

```console
$ docker pull debian@sha256:5594dc31fb49a3e528578c298ad248f1c359921b6977470e7cb65db823d479fb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51697994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1587fb746546fe1d71ba9971ab4e3d1c722eba79711434570f1f0a78fc6dd2a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:18:29 GMT
ADD file:3b31c2bd33a3d7e6352823413292afa26a09dbcdbc56396202701f16e609204c in / 
# Wed, 31 Jan 2024 23:18:33 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:19:49 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:651c4bce8b545a7028c9eea81f8b25dae93c9bf0073fff7020f5784448310184`  
		Last Modified: Wed, 31 Jan 2024 23:31:42 GMT  
		Size: 51.7 MB (51697772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05fa75ae686ff303ba389c898a7e52b57ecdb01ac51969b8319d8b7ff2b53949`  
		Last Modified: Wed, 31 Jan 2024 23:31:48 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
