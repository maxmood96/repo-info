## `debian:bullseye-backports`

```console
$ docker pull debian@sha256:0b057267458f929226584aad055a9bed94f1d6c47c2063e97cce050c76344e79
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

### `debian:bullseye-backports` - linux; amd64

```console
$ docker pull debian@sha256:7d49de6012fa0f55dbf5e5b27ae88123013ba160576c2667fece43b02e1fa9e8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.0 MB (55010112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9e596cc0c7e25479ce915525305c1d8041ac523120bf00c1da3d291e20be5cd`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:20:16 GMT
ADD file:798015650079cb88614ff181a30f9c3d3fde8361c49ae2dec2058d5a3e61f5df in / 
# Thu, 23 Jun 2022 00:20:16 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 00:20:20 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:1339eaac5b67d16d6d9f41fb7a7b96f7cebf3ba4beab36cbb60935aa772af583`  
		Last Modified: Thu, 23 Jun 2022 00:24:48 GMT  
		Size: 55.0 MB (55009886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e9c2200a24a2127148874401443143b480b5f05b9edfe8fa33ed7020efd19b2`  
		Last Modified: Thu, 23 Jun 2022 00:25:06 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:494026e3aaa23b451ec44cec05a9ba5562fffa39ac6099e1f93541a5667f3195
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.5 MB (52541365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ab1f303cc9ff9f154ee7404531b70d185a4f24128f7cd014ec6ece1f72a2383`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:50:04 GMT
ADD file:a9a29412ef2a46df9ac08c0263e1fd3872777bcafdf6f172dae904af96ff7585 in / 
# Thu, 23 Jun 2022 00:50:04 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 00:50:20 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:6e4031f48ff7c3b7223afff91721ded4a4de5f7c666f84c58a5d8298dd0fe028`  
		Last Modified: Thu, 23 Jun 2022 01:04:50 GMT  
		Size: 52.5 MB (52541138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2062c297f6d64932c63cb4807f5582c5091e9efe57b8fa395c698fd9857c28c`  
		Last Modified: Thu, 23 Jun 2022 01:05:13 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:264641619204f4971f7745dcd867005bf1a064108cd572fd667bab1b1c0ed8a8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 MB (50199830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3736f5d745f57e18be9527085e0ed3d69c8b041cb5fd8ca0928e8e246066605b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:59:08 GMT
ADD file:59a6186285c4849971ea2d4801e6ebc1e4310f5e3dc0f87389f39d1fa8a63c58 in / 
# Thu, 23 Jun 2022 00:59:10 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 00:59:26 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:2147df557f50051066d8920b460727b890c1da5cb2c15b055c99ed8216b5528f`  
		Last Modified: Thu, 23 Jun 2022 01:14:34 GMT  
		Size: 50.2 MB (50199604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75ea65fb1da54e2e3a03aa0e2f3162eec817f0b56b0f1bf292104baec19a1eef`  
		Last Modified: Thu, 23 Jun 2022 01:14:58 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:14a9f440538a76845a018a8dc91278914c799060d3dc6176e22b250a2edaa03b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53697042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:563e7376ce6281be40fac9858c025be87622220928e5ecfb4b030fbf2d587063`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:40:28 GMT
ADD file:64c455af1bb18ff2c202a244e058b6e5ac147b89410ed36edc5e29f4b6f02c5d in / 
# Thu, 23 Jun 2022 00:40:29 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 00:40:36 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:f873dfbc59b181817d5bc2b9fc31d90d8f9139c8cabb2fa7264f9bd7b418b8d2`  
		Last Modified: Thu, 23 Jun 2022 00:46:51 GMT  
		Size: 53.7 MB (53696815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de4bc45539e1832890d5c882c75331a72635be14c171da0660ccd88be3712d38`  
		Last Modified: Thu, 23 Jun 2022 00:47:10 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; 386

```console
$ docker pull debian@sha256:72b21bf7a37343fbc05904f8d687b1390bc48aa049935d4405f16e26bbdd0d2f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.0 MB (56007747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49ba20f6e306588357563103fa72e13f8a1bdbcaf6c62ed33cc47866ea5fc9f0`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:39:17 GMT
ADD file:38ad8e7562f238cf436c2a32b21b397a0ad3dd5c8f68f29bc724458cad18a47e in / 
# Thu, 23 Jun 2022 00:39:18 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 00:39:26 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:8bfd9a7ec075cef3ff84a270710c704347f9a866aeb50e5a286491696168d5f5`  
		Last Modified: Thu, 23 Jun 2022 00:46:04 GMT  
		Size: 56.0 MB (56007522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89f548c92b2db7aeb44c40ac20f06778800fb59fa57ca8da6f5d595a3bfe6731`  
		Last Modified: Thu, 23 Jun 2022 00:46:27 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; mips64le

```console
$ docker pull debian@sha256:11e3724b74cc4b3867b88c8ed2c32d6f50f5ff8be5a1c858671c76e4cb7d511e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53272556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a56cb085c71b0cff7e4bf8deb90024e3105a8349da7427ecdf85217e498bf8d`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 01:10:35 GMT
ADD file:bf0066890c02fe9254ebe22df9f29cfa14ff8023e297cd8ce14c32d423c81099 in / 
# Sat, 28 May 2022 01:10:40 GMT
CMD ["bash"]
# Sat, 28 May 2022 01:10:53 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:e3c10d3d838c43f5c37f26af81b379c8e9fd26b58bb2a30e2b137934e2266ef1`  
		Last Modified: Sat, 28 May 2022 01:20:51 GMT  
		Size: 53.3 MB (53272327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e6b19c8cfd106f1136fadd6d865ca9f9e71f1cddeef4e3be86289687ae5488b`  
		Last Modified: Sat, 28 May 2022 01:21:08 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:3dea33bd7a464ad4757fb371bbd07d620826dec919b6a0ab6e381024eb2161ae
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.9 MB (58902885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cfba11e5670d9f960f63cc73278f88830d3417d21284d25d72bd9b432436dde`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 01:22:18 GMT
ADD file:0cf54bc63a3f2c0d5652c62456619ccdd983f64f718a89816c151963f108461f in / 
# Sat, 28 May 2022 01:22:26 GMT
CMD ["bash"]
# Sat, 28 May 2022 01:22:40 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:6a8d10cab014c8bb87d1db1758eacc9d3a16b40994eec1e70e2eef174276708c`  
		Last Modified: Sat, 28 May 2022 01:31:45 GMT  
		Size: 58.9 MB (58902658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18bbdb56286119c7b54a7d5d8f6c7a0359cf01f73fca76ce86169b503d620e40`  
		Last Modified: Sat, 28 May 2022 01:32:13 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; s390x

```console
$ docker pull debian@sha256:1a57e4d7c486e9513849268777a29be6ab1b6159842be94d9885f44edb1baf5a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53276999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dda92ea694cf4d6951697e1bae431ff541826b98392f35f7c770aa0f9ad2635`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:42:40 GMT
ADD file:80a08f446549ae1b71aaab0aada00625b804fd959e2a21a9c0747fb3cdb0afc0 in / 
# Thu, 23 Jun 2022 00:42:48 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 00:42:57 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:e92226c94dce8ebeb505bbbebdc70207295a4a602fc736044e4e69866dc05e58`  
		Last Modified: Thu, 23 Jun 2022 00:51:36 GMT  
		Size: 53.3 MB (53276772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7de0e353b33ceabed3477871a0d8fd538968c87db2186e1643637cdef60d7176`  
		Last Modified: Thu, 23 Jun 2022 00:51:50 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
