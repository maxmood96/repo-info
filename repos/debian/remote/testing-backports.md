## `debian:testing-backports`

```console
$ docker pull debian@sha256:312a614d8ef00e93fb75174f1b82fb3b53d7d9029ba4f8d4da791ace83cb80ec
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

### `debian:testing-backports` - linux; amd64

```console
$ docker pull debian@sha256:9b92c6113157096c3c47e52073f2654d6e82df2213fbd8c3c1aafd20a6991e46
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54909772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af5d54fa3254727cddcd1f6884772b524c49eeaca5367092837041f356391a41`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Aug 2021 01:26:21 GMT
ADD file:78a808c11f084f171360ce87535de573285eb3f06602698c86bc2007a307299e in / 
# Tue, 17 Aug 2021 01:26:21 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 01:26:26 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:a42321116e438acfff1628527f7ae9e433d1ece73a19aecf4b4642d110d317fd`  
		Last Modified: Tue, 17 Aug 2021 01:33:48 GMT  
		Size: 54.9 MB (54909547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8163ee8fa65060a1e23b5150adc9c5ef0919acce155aec1a9f4435452f3540ae`  
		Last Modified: Tue, 17 Aug 2021 01:33:58 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:643989834ca9fbc2ab3b834d034c6928ee41b195f23217847ac7557477727293
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.4 MB (52446702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3897ba186f63899ffadaefb9dab4b5e01e8b0411329d6d5dcdb75f681f8f75b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Aug 2021 02:01:50 GMT
ADD file:491a84a5ae48bcd2399e52d9a9a7f15369b963b0323b98dc1217a89cdca21ebe in / 
# Tue, 17 Aug 2021 02:01:51 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 02:02:03 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:63758c2a30f3f97256f945fe58e8f02a6db4bf3cf37e894450af7940fffdabe0`  
		Last Modified: Tue, 17 Aug 2021 02:20:16 GMT  
		Size: 52.4 MB (52446478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d00dde8a881704f7f5f02a07bacdfd61258a18acc5b9df474aeaaa5eeaa0a05`  
		Last Modified: Tue, 17 Aug 2021 02:20:28 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:9d9096775d6675ab6b58b452047ff99a036667e8bd68f09b11bc309d4b65c3a3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50113032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ef4af24b2976e2aec8e9c599b7104eb696c83e31e90a4816986936b83935123`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Aug 2021 02:20:09 GMT
ADD file:874bffeed2e5c0d6617cf96d64553936059d797aeb8958af5260b908ad0c2b53 in / 
# Tue, 17 Aug 2021 02:20:10 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 02:20:24 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:52226b9e985e60aa27152e8d2b5757735c276ea3a0f2d42cc78bbe4f289b90ba`  
		Last Modified: Tue, 17 Aug 2021 02:37:45 GMT  
		Size: 50.1 MB (50112808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb0d20808e984f7407a00033b704e010ae0bd96ad5a5a50a02af0057192449a9`  
		Last Modified: Tue, 17 Aug 2021 02:37:58 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:ba96b313cc8bd04a04eef70024bc8b926710d2bc6b85fa3b3bca90102811f638
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 MB (53595459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98dc2de27fb201e77b78941d15e2d981ec93f8c001b76147ad19bf335780895d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Aug 2021 01:48:44 GMT
ADD file:3893bd6ddc225c2b660af0396860193305baef444ab5aeb369ea28b0679c3a14 in / 
# Tue, 17 Aug 2021 01:48:44 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 01:48:50 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:20341cea39b7b052e8fa46c85b6e6d17dbd3830a13c140eb6d72f4dd6ec5b8e6`  
		Last Modified: Tue, 17 Aug 2021 01:58:25 GMT  
		Size: 53.6 MB (53595238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9bcaa33f97695db5022992cc5a17d37fd1d235e31e1736ab14df2c2523e0ad0`  
		Last Modified: Tue, 17 Aug 2021 01:58:36 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; 386

```console
$ docker pull debian@sha256:bfb42a1068582cbc838b712f268454ba5ad9a6b0ac50a360b8cf7f35e010f602
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.9 MB (55916971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec8bde8b99b226259d0764c9eb02b4f1de836db00cbcd098e8877fc2e23a512c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Aug 2021 01:44:22 GMT
ADD file:ffab122453062fedf7fb8552a0aaa4cf58f8acdf226e4c46b43f389b618991ed in / 
# Tue, 17 Aug 2021 01:44:22 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 01:44:28 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:4ec869f5a812521523d268b332053af7ad7bb42b210f18130827e444671149e0`  
		Last Modified: Tue, 17 Aug 2021 01:55:42 GMT  
		Size: 55.9 MB (55916749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2d9f3868eb1d49a72e03c160b83aff2cb642c060ac5adc52e0809726d09bd62`  
		Last Modified: Tue, 17 Aug 2021 01:55:55 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; mips64le

```console
$ docker pull debian@sha256:e61067015065d040b05c529414bf28f670b2199af572722f023144d79e10c4c9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53162176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95b06a04e07c69163a39ab5e8e874c316f0364848a09716d503739f54473d7be`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Aug 2021 01:15:31 GMT
ADD file:62e54467a10eee79414aff4cc5d6ef5d021414ee51f5639ebcc19417ee41a10d in / 
# Tue, 17 Aug 2021 01:15:32 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 01:15:41 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:503c3f99e2ad5387a582b3959e0db27a063dd2892d4bf3599d8d3e518d8f76a0`  
		Last Modified: Tue, 17 Aug 2021 01:26:22 GMT  
		Size: 53.2 MB (53161953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd42c0ccd5c848f07ca5e6a06846c1c2517cc5bf99c502e2663d5cda7fb749ee`  
		Last Modified: Tue, 17 Aug 2021 01:26:32 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:212774be5962f76c832e839a73a2679a1a3d55653eca403ec9aa55d36f151c3b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.8 MB (58811001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a53729f9b0e826655f5b71654e686074f2e96646e42025ddbddd300cf1b052a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Aug 2021 01:37:41 GMT
ADD file:1f0015936f61869d4be0802e8692d936b87b60ce9198abdeae9e7df07172a08f in / 
# Tue, 17 Aug 2021 01:37:49 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 01:38:12 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:2582c71fc0095399869e98ebc0072852aa8431fc7ead1a6a512085dfc17ff54f`  
		Last Modified: Tue, 17 Aug 2021 01:56:42 GMT  
		Size: 58.8 MB (58810778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80ffa4f346b427f7c8f9cd56cef8dafb1b666a53d35216c7b20c2f9e7ec7adbb`  
		Last Modified: Tue, 17 Aug 2021 01:56:54 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; s390x

```console
$ docker pull debian@sha256:0ea3f878c7f4da05b287696f86872deea20bafccc6c90839f7cddc1ca66851da
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53188776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c92bfcc2808bbc882f959958c2f4595ad4dbd475e6a3a7b773cbdda011cf9efe`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Aug 2021 01:52:42 GMT
ADD file:b26674f4981f5db4384da9469d05dea7bdf6bca5c09c954606849d005794f331 in / 
# Tue, 17 Aug 2021 01:52:50 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 01:52:58 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:9cb7e265bbdb4667aca5ec3384874eca1b6494c42d2489f1d0221adfd706bf9b`  
		Last Modified: Tue, 17 Aug 2021 02:00:01 GMT  
		Size: 53.2 MB (53188554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cd003cdd8c82a9f5b05c040826e4d810ba6a5580ba4b9b103d93f35636dbc23`  
		Last Modified: Tue, 17 Aug 2021 02:00:11 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
