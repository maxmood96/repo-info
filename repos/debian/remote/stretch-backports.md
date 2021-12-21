## `debian:stretch-backports`

```console
$ docker pull debian@sha256:0b6af83fd23c2998b72b257a8414e854e90c84141485d6f9456ee83713c76a99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `debian:stretch-backports` - linux; amd64

```console
$ docker pull debian@sha256:4f371368ef8998caa9899709bc4b550ee6502693346902faf6b99288f94c5387
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45381629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06eb38c3205c3bc50de9cca4148d3ecfec13f4e3307c0f1e1813d2c8e8aaa5c9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 01:24:31 GMT
ADD file:4937a62e9e92f367221357a58d7438d1f76546bf3669281431633aebcfd7839d in / 
# Tue, 21 Dec 2021 01:24:31 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 01:24:35 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:6a56b4def9c45045931a9cf99e9365b558347ae41ec8bfb104a7787e1c3129b0`  
		Last Modified: Tue, 21 Dec 2021 01:31:13 GMT  
		Size: 45.4 MB (45381404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa5e78e8babe0559c8a02feda106ce278095129b0a44392290d6b95da737882b`  
		Last Modified: Tue, 21 Dec 2021 01:31:27 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stretch-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:1cb4a2493829d59faf6700ac074c23262142ed8609f4fbf97f20d2f6bbfdbe8e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.1 MB (44092067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da0433ad4cc410c9739546c62a793453e1e8040078cfd5b1dfb2073c071bb535`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 01:55:32 GMT
ADD file:f4fd2295264880f83c7b33497cc2ca05b6182abc2a1b4cc745d8c9390418387e in / 
# Tue, 21 Dec 2021 01:55:33 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 01:55:48 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:dd6be4bbf248359401800a128efc91a8f8c27caaab1275a046d16ed2b44361cb`  
		Last Modified: Tue, 21 Dec 2021 02:13:02 GMT  
		Size: 44.1 MB (44091842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a33e0efc618c5b58b98d93eff2987994afa75418d43d526504260e87669e1116`  
		Last Modified: Tue, 21 Dec 2021 02:13:21 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stretch-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:b5fc9044df8a113097b56883753e9d5b2ecb7e50b3c17b5dfaed22f354ad0d85
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42117159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dde32170c2f7fce2db02cd96443f096a3ac1fcd0c44e87d8b0106757f80e47fc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 02:05:07 GMT
ADD file:60b016ba67df7136a5c9120c3bda872fe6fc9264670eaec4af04649094d2c53d in / 
# Tue, 21 Dec 2021 02:05:08 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 02:05:23 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:1680a7a0944ad84261b1979d7a37cbfaab55a5d7841917a0fb9a78ccc086ee83`  
		Last Modified: Tue, 21 Dec 2021 02:22:04 GMT  
		Size: 42.1 MB (42116934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c1d2f63e1bdeed52ea9bcbe0058f63be5dae368c93585cdedfbc138ebe93002`  
		Last Modified: Tue, 21 Dec 2021 02:22:24 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stretch-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:1b90ff4d0190faa30018be01bc7fa61ace0c4c02099f85ab7ddd27a861f7ea9c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.2 MB (43174003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c59cd822b5b23c191d9bcf4f0c50afe0a89db13248c76075179a8577e12326b5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 01:44:24 GMT
ADD file:a938be6f1e00e8fe4e0dde6657fcab5db99de34969d54368106a9334f67c1533 in / 
# Tue, 21 Dec 2021 01:44:25 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 01:44:32 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:d097540eada98ef0bee6e7283ee6a0fbe163c439c3543706a7fbf2f0158fd907`  
		Last Modified: Tue, 21 Dec 2021 01:52:36 GMT  
		Size: 43.2 MB (43173780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd926d1258197b4bfac3b4ea8273dc9d69e1ff00012feeedf1dd4404eb6c2698`  
		Last Modified: Tue, 21 Dec 2021 01:52:53 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stretch-backports` - linux; 386

```console
$ docker pull debian@sha256:9303dea4db77a3466b8cd1f52c25b81f64a2cfba3457681ce87911dc7313bb71
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.1 MB (46097933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1aeb57a083bff7ee8f98e10ede1d3506b03ff62f1a57847b35ded7295e69abc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 01:43:09 GMT
ADD file:55bfa1f20811d5ad7e0824cb8b85e2d7c75ed74ca2784dae41a80c54c2ee3ca8 in / 
# Tue, 21 Dec 2021 01:43:10 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 01:43:18 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:a33597723b77b33e69ce15c675459677dc40eb6b8b822c767d1d106fb2b0365e`  
		Last Modified: Tue, 21 Dec 2021 01:53:18 GMT  
		Size: 46.1 MB (46097707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d520502bc0a3ba1bb6debf3bb92da570f49f175fc992b674e6501748b34e65ea`  
		Last Modified: Tue, 21 Dec 2021 01:53:35 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
