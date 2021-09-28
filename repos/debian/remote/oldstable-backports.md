## `debian:oldstable-backports`

```console
$ docker pull debian@sha256:6e28d036e8d521a42a61eb1f33522add637fff279f177759077e8dcb27382308
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

### `debian:oldstable-backports` - linux; amd64

```console
$ docker pull debian@sha256:7ddb3af78391c17600c96efd07940ff65694a350e03183c9fc394268d0fe88b6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50436477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8547007c1afefa659b51c5f7837220d252e27d6ad35adaf9435269154ee4ced`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 28 Sep 2021 01:23:50 GMT
ADD file:2e534cb29f7663d54796547961291dc2ed68f76acfea9b1230e9e8435756292d in / 
# Tue, 28 Sep 2021 01:23:51 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 01:23:54 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:76faeef923bde74843eb96e7128eeef07c2b3e730a26cd6e30279560f8fc29ee`  
		Last Modified: Tue, 28 Sep 2021 01:30:41 GMT  
		Size: 50.4 MB (50436254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5042c161e99ca7f57b845de0fbf43c1faeb378b6ba0e1476b886d922cfca1e3e`  
		Last Modified: Tue, 28 Sep 2021 01:30:50 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:11c3fda81bd459a94fb9a7a04bfebe6ad268538e4c8c428110818d3164909212
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.2 MB (48153975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5492d44a679b2f402b227f113750d1086d6e6455b3f7d1f8750882a7e757395e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 28 Sep 2021 01:53:13 GMT
ADD file:74438a9206fc0547d98056e300568c95fefdebb549ab0e1511ac530413e3c785 in / 
# Tue, 28 Sep 2021 01:53:14 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 01:53:27 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:4fbdce7b75f5a51e079e0306750abf59caa73269c6e1a08c4169a11203d26634`  
		Last Modified: Tue, 28 Sep 2021 02:10:04 GMT  
		Size: 48.2 MB (48153749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b2b438fb0de66eba70315e14331e7da4873edd6568d4f87c1fc62b8e45e7b38`  
		Last Modified: Tue, 28 Sep 2021 02:10:16 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:99f391502886301f61578614fa6dcaa6c069572782a880d5be144ff7e5eed1b6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45917738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f173d1a975136aaa084de340f475c8aa38ba315a4078cbfc487112617fd2d5e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Sep 2021 01:02:03 GMT
ADD file:17995ec5935167f8cfb9f959ee5e14c9dd7f7e9671a65abe443b39988934dce3 in / 
# Fri, 03 Sep 2021 01:02:04 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 01:02:16 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:4583284ddbf17c7cc8c8ad1fdfc30f52eeda1a4f6dc7644108c26362263af3cc`  
		Last Modified: Fri, 03 Sep 2021 01:18:24 GMT  
		Size: 45.9 MB (45917513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:575de22dab8f7438143877309c351c5e95ef038f4848e14472caa1e96822d5c9`  
		Last Modified: Fri, 03 Sep 2021 01:18:36 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:df0557f2a8580f2319383d445a9ef6bc343a3c6e3daa1ce4d09142b18707e606
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49222574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fbe2ae784359bbf65a0ce4436452aefd7c4b30f391a6a86222c547b220f22f5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 28 Sep 2021 01:41:52 GMT
ADD file:1e53836266c94bb5380ad8ddd081de2f0edba1c25bb2cf0c923ab2664ecbbf9f in / 
# Tue, 28 Sep 2021 01:41:53 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 01:41:59 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:5c94be4fbb653265cbca3b3228fb23214358d4bcc2772cfad97594b9c0a92169`  
		Last Modified: Tue, 28 Sep 2021 01:50:24 GMT  
		Size: 49.2 MB (49222351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2830fd0260a2dc443d2ffd88efb9da6cbe1402d1b1c088128cb25ed0ffafc26c`  
		Last Modified: Tue, 28 Sep 2021 01:50:35 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; 386

```console
$ docker pull debian@sha256:7a7f91ca80dcb00e48c7f28eff785601d776c2ed1c69def15b600dfa69c66a4b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.2 MB (51207639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a685397227450ec33cfb4bcfaa5ae6b1298b313cbcb96a91aa000ff6a672caaf`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 28 Sep 2021 01:41:42 GMT
ADD file:9a052d104d56e0b9d847870a89ca0dbf3ea5d5c9cef3be65b5299ced7cbfe137 in / 
# Tue, 28 Sep 2021 01:41:43 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 01:41:49 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:5d52f24f8631fecfa6ece230564add5d46cf4edc834f3fdf1a8891f57fd71d50`  
		Last Modified: Tue, 28 Sep 2021 01:51:18 GMT  
		Size: 51.2 MB (51207413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fba8a803a1b9002e46f41d2f10a4e64c19c8e03fe0099a88921b917234330506`  
		Last Modified: Tue, 28 Sep 2021 01:51:29 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; mips64le

```console
$ docker pull debian@sha256:637049b05671854ff622e4f40642eb415590f79796c46f9a4c9bfadc06abb231
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49080304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdf836854d4fde3ce13cfa07208cce9578b2f105f72691ba9518ab92f9675771`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Sep 2021 01:11:14 GMT
ADD file:b3a0336c03cde91518be1189cdca3185276e9c9e965d5e123b766b8399bd3e1d in / 
# Fri, 03 Sep 2021 01:11:15 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 01:11:21 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:91339a4d49208e09b5b1324d90f5dc6104bb35ccb61135662b98533970c514f2`  
		Last Modified: Fri, 03 Sep 2021 01:20:36 GMT  
		Size: 49.1 MB (49080080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae91dc7b06123ad83c662741d20d8b890516ca85ed88ba4aa2c0432d3f0a3dc8`  
		Last Modified: Fri, 03 Sep 2021 01:20:46 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:44b40ab18a1b025c71b6b25c8daeba2a7ed29edce0657d436b1c6377ed754c94
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.2 MB (54182888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c694c2b9723790899a70fb6d7866e97109b7a9393dd14f0267abdf2b94d62fc`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Sep 2021 01:25:01 GMT
ADD file:0de8dbd369ea8a734934d859b2127ac2d170c7c67ed97b1969a240f3a20f0806 in / 
# Fri, 03 Sep 2021 01:25:14 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 01:25:35 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:5ec7b038dfffa75a312736217d90bbf467ce4af7129e08320361872aa43b27d4`  
		Last Modified: Fri, 03 Sep 2021 01:40:50 GMT  
		Size: 54.2 MB (54182660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84d84750a2ec9d770a90f06a4971a6c6d26e845860843dad9ca2f724556fc877`  
		Last Modified: Fri, 03 Sep 2021 01:41:04 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; s390x

```console
$ docker pull debian@sha256:685f06c5b541c1c506804fdb237c7f8e272f28eac267bb6d4cfb5b33ddb57aa0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (49004533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d113dd593f13b947bdd4495621dbaaf1311600d7c82552af932ee7e3a4a3995`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 28 Sep 2021 01:43:42 GMT
ADD file:0d48c6cfa43326752a72a81e480683e805db4db24c44de2528d026c30fae4662 in / 
# Tue, 28 Sep 2021 01:43:44 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 01:43:51 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:c774ab9b5b870bdae66a7cb4897b04a09bc8a32b6b1b48b388d308fd37c9bcce`  
		Last Modified: Tue, 28 Sep 2021 01:49:52 GMT  
		Size: 49.0 MB (49004310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd3fdeaf46f1dea9263881541454bd94af8d0440038982aed0e06c4b5ef0fc2`  
		Last Modified: Tue, 28 Sep 2021 01:49:59 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
