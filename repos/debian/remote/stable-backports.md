## `debian:stable-backports`

```console
$ docker pull debian@sha256:c35b11e681773f020cb3095fae5e9c8edc25e75c4c43aec3d57554f00b99bb1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `debian:stable-backports` - linux; amd64

```console
$ docker pull debian@sha256:d9b0016263811dfa73b4ae79b9d566894dcbf186f35475c15113dfdbe9f98814
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50397970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c571d9c6c923699446793345910dac6dcdb8301c7f18e2744542149795c7cd8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:23:37 GMT
ADD file:08a62c04bdf7cd40093f5e87d04d397f66b2e391bd1799269a44feb32671e330 in / 
# Tue, 17 Nov 2020 20:23:37 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 20:23:44 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:4d05d207938b37e1d50ec2d32c55eb8f8609867826c2b0702cec8c933754d5ca`  
		Last Modified: Tue, 17 Nov 2020 20:29:41 GMT  
		Size: 50.4 MB (50397745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5343b9703bcbf8e040726ab6871eb4e2da5b8d65d2011d89a234eee50b38c41e`  
		Last Modified: Tue, 17 Nov 2020 20:29:46 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:46b276b54330bf59b4fec553a09975312b473e7f49b5f0ebca2a2bd2c5495e41
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 MB (48111346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1374b2c43ca16992c0efd8382222cca6d6d90ec309df38623f97300f5ca57e08`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:24:01 GMT
ADD file:f6905a639ee072ff905061d95f9e716ef9ecc00943c82b7e890142ea07d7106f in / 
# Tue, 17 Nov 2020 20:24:07 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 20:24:16 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:8baa9f629422057a2770fbb38fea8ce4edb6d0cd8a9f2bcc8c9364b0795936a9`  
		Last Modified: Tue, 17 Nov 2020 20:33:47 GMT  
		Size: 48.1 MB (48111123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3c24657f1244f84def2858aa92f839871290e177705b50d1cc2da4a2e1e35e3`  
		Last Modified: Tue, 17 Nov 2020 20:33:58 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:ce2cb325f4e6360287876ab4bc3482efe2a8f5e153e35100b20874c51421883a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45868448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3b1085462775dd88927f49442553c9c423d60ba9691d877fff498b4479cab27`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:25:06 GMT
ADD file:590d1a4d78cc71d95aef2c933f04a5b07f875721762d82ab945bfb3e2e0b2f6d in / 
# Tue, 17 Nov 2020 20:25:15 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 20:25:27 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:454e64d48702ef4c7a161cc4d0b01fb00731de78e148a6f6155393d391512d38`  
		Last Modified: Tue, 17 Nov 2020 20:34:45 GMT  
		Size: 45.9 MB (45868223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c5d57f5a67c6cd15e96289afac4ed8095ac72a655a13672ad8002aff501dc82`  
		Last Modified: Tue, 17 Nov 2020 20:34:54 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:a48c6156f78070379026bf6c4c04399f653f52d7d7b3da5c61daa657437078ca
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49179428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f57e3d186ba5e0ded53343836b9b9f13eb97ad965e1de5dc9421bbfed3c2593`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:25:56 GMT
ADD file:004f317c15cd7df0e244d8601a3b6e4ce4e80995663013f8ea89fb0eb0583a63 in / 
# Tue, 17 Nov 2020 20:25:59 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 20:26:51 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:5be914df7b5e6f9a6a7b3acedadc7b39e5d4c318d06369747c73aaf4301ec21a`  
		Last Modified: Tue, 17 Nov 2020 20:33:39 GMT  
		Size: 49.2 MB (49179202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:905810a4ebc30ac3a485600877827b8a04d76cc7c761e276cea8412ca0bf139d`  
		Last Modified: Tue, 17 Nov 2020 20:33:48 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; 386

```console
$ docker pull debian@sha256:6bef5dbdde3dc036a2a715a3a5c343ac1e175155e5e41d0a0197fb0b410a4c19
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.2 MB (51159720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48939bb2d5582a3003226f4cc907a3773190deb37112eeab683555b44df1d429`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:22:32 GMT
ADD file:e910e2e9880335222c7f2bd9042317980384dcf367c5b526738762eea6533009 in / 
# Tue, 17 Nov 2020 20:22:32 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 20:22:37 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:5dcf3acaf8974955fbb565b4543b4eff29052b960da144c1ab3bed0dce8c5a47`  
		Last Modified: Tue, 17 Nov 2020 20:29:29 GMT  
		Size: 51.2 MB (51159494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ef6f682cd10a881af22dbebd0a6fa456ba992c341d71faed65ce9d7e4772b50`  
		Last Modified: Tue, 17 Nov 2020 20:29:35 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; mips64le

```console
$ docker pull debian@sha256:2b5183f588bf0f3bff6c4931cc634f066690c9a2fa9460c988dbd3baeb6e4a88
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (49020531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88619a6b1c4a87e0b4442104ccfd8d3da2a5ad4aa74ae2226a5869431698798f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:20:44 GMT
ADD file:e1aa8561bbf81211e0fa8a391ccdb1c1a17b4c61c6598919ac94970828568af9 in / 
# Tue, 17 Nov 2020 20:20:45 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 20:20:52 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:005afbff6ce4e015faa00d2df67f7b2953d6a8513ef7682abce67147cad7c6ed`  
		Last Modified: Tue, 17 Nov 2020 20:28:39 GMT  
		Size: 49.0 MB (49020305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bb545e54c71fa4baffb8b1fa88868ec91646924525b1b8f9a7adbf187b4ad24`  
		Last Modified: Tue, 17 Nov 2020 20:28:51 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:292e3478b70d14c6e30c8584e599282e36db7ddd2da9637bc67ed1e305af7bde
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.1 MB (54143286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7b5993cfe249dc8e159b65dcec35e26f878316329ac89d49c8a29fe77aa1cc1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 23:24:20 GMT
ADD file:eb4c7def901bc2986e679334ee173b97affd3d52d7490e333efcad3803423f54 in / 
# Tue, 17 Nov 2020 23:24:30 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 23:24:43 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:f36467046d39e664c9f24108fe797b190b581fcd74fb7341ad681da46c89232d`  
		Last Modified: Tue, 17 Nov 2020 23:36:22 GMT  
		Size: 54.1 MB (54143060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dcbe1cacaf3f3917b5a2d38b946d9db6464df25ac744ac4363994b32861a943`  
		Last Modified: Tue, 17 Nov 2020 23:36:34 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; s390x

```console
$ docker pull debian@sha256:b482ce955006c87d681719b1ec705659209599b7a5611e36ac86777d92642f8d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (48968479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5c7774ffb4d4193866c30f8163cdb15540f1bd9225fc4c468107a1f0d263804`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:19:37 GMT
ADD file:6d4efeddf08e5a1ac91682e26b7c2b436e66281fb19aeb41765c1b27a4c7d0c4 in / 
# Tue, 17 Nov 2020 20:19:47 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 20:19:54 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:44d4fd8ecce2e5958ba48a4b1f42782c0c66a17312e5e3a781b7c78e97de453e`  
		Last Modified: Tue, 17 Nov 2020 20:24:30 GMT  
		Size: 49.0 MB (48968255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:901aa0d4c4427647e5303e2189b0233375e9f8bbd66f77acfd676687e4c00a8c`  
		Last Modified: Tue, 17 Nov 2020 20:24:38 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
