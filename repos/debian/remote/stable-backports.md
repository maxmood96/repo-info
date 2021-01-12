## `debian:stable-backports`

```console
$ docker pull debian@sha256:96e45013b9eb742e3c6d1336d2bc3f92afe8669e0e7bda593aae308bc5bf11d0
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
$ docker pull debian@sha256:ff30ab8c393dcb0de4004336aed411ff87d5f2c3bd6fd0a1f514bfa4e9188acc
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50399411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bd738c4c27dab38695e5a1f9217000572439555c8fa2909886619652e1ac879`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:34:38 GMT
ADD file:9d0a58453be7f2305b2b3bb38c88debac1b3475268a9c5eb0053855d27436446 in / 
# Tue, 12 Jan 2021 00:34:39 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 00:34:44 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:62dfdff96a793026fa2612dccf8d383ac2199cc59f95c819faeadfda5348b4e9`  
		Last Modified: Tue, 12 Jan 2021 00:42:24 GMT  
		Size: 50.4 MB (50399184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfa5c2cdcfb19b540afd822cd9e62513daa28c2ce5cb7d15a4ae063274284bc1`  
		Last Modified: Tue, 12 Jan 2021 00:42:31 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:8e1168c71a571321a3ccf24b4bfca520ca5b14b3f4e226b8cd4ea22a3a714698
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 MB (48112858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f2dfc0d62a94e7d34bdf3ccde4d8a3ab522ef9b8ac3eda30a9ab9b8eb111a08`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:54:36 GMT
ADD file:6a6965267a88ce5422108f44396b7f0f6c617671119df23fd6f96145881719f5 in / 
# Tue, 12 Jan 2021 00:54:37 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 00:54:44 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:043f335bc88804fe97c0ac574ecfcc3ba7be42c7a37171796ab7c701af0b32ad`  
		Last Modified: Tue, 12 Jan 2021 01:04:01 GMT  
		Size: 48.1 MB (48112632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c092f833eb1a784cce849cd08b82501a34ee885c8a00dfac7b0343880a871db1`  
		Last Modified: Tue, 12 Jan 2021 01:04:09 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:52c497ece1bd7eb1cc112fabbadfcfac9ed5aa7e873e22c122a6e40ac6f57e29
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45870295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:111f03f7a7cf2b596ee72b6886c03e8db3e367b383063f610b9c33fef9af13b0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:04:35 GMT
ADD file:6ddc40e064f2939859a1303487f6b3effe8fb8b622be9c32a52486c9b23c9295 in / 
# Tue, 12 Jan 2021 00:04:38 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 00:04:47 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:542e59a2937340a22ccbc38528f6b1b7a2d0e2d0acccf1dd366644de4af25cf3`  
		Last Modified: Tue, 12 Jan 2021 00:14:28 GMT  
		Size: 45.9 MB (45870070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6e0013f1c03400edd7f4704526ffd52cd1f22c2954e14d42e02179485a662c2`  
		Last Modified: Tue, 12 Jan 2021 00:14:42 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:026dd51a59fe6b49a6b649840dde0f4566bc5a90afcc7b4ad2fe9ddbe53415b3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49183860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3255a88fcf293bcd35ccd4de0488dc0ee864a2c568563dba8bc6bf061186a041`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:43:14 GMT
ADD file:22b52ec13aa24856e290d74e9de91969b609ddaf42d30e2f6f269a8d1c7656e0 in / 
# Tue, 12 Jan 2021 00:43:39 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 00:44:28 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:5876335f48bbf0bd42a1da148c055c378edd1eff18168b4c4a4c8d62cb3262a0`  
		Last Modified: Tue, 12 Jan 2021 00:53:57 GMT  
		Size: 49.2 MB (49183634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e480fe71038f8b0fc148cdf9458a8febd09231378fd288b70d9f5fc11bb4e45`  
		Last Modified: Tue, 12 Jan 2021 00:54:11 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; 386

```console
$ docker pull debian@sha256:60cf937b7ebe8732eed7d5961dfef0a95461bd1ce73de8d7b26bc52b888aab8b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.2 MB (51163862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa7bbb0e9054a384f54e135796ff1c8d15af2b6955d96e85af36acd3a8d5f023`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:41:33 GMT
ADD file:0556b58fe3e2c4da8516dec06a9807766ad013285965d896a56d66791d504a27 in / 
# Tue, 12 Jan 2021 00:41:33 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 00:41:39 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:c4bbd9d867f356ba4c4d12dbd3169d2ab0f4217d3e949d8adf034ebd6fed2a26`  
		Last Modified: Tue, 12 Jan 2021 00:49:49 GMT  
		Size: 51.2 MB (51163640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdb442e675cb2de5de4bfeb2873a01b6365a50e388dda6012e0712ddb524b5c1`  
		Last Modified: Tue, 12 Jan 2021 00:49:56 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; mips64le

```console
$ docker pull debian@sha256:a3608e0f9b31bbe89d31133fd4105b46bd148d94b9071aa73661de1e65a42a42
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (49022819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9d68f3dc3636966f11a9b026a5b22c344f96df47fd54942a8b02e6a5138c221`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 11 Dec 2020 02:04:38 GMT
ADD file:aed8f53e57fbd49d05b28154d4973621e5dec28eb9a084dd5d87df879deca96b in / 
# Fri, 11 Dec 2020 02:04:39 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 02:04:46 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:e10b6267b593dd71c8007099359a7a115b3120e34f5e80e55282f361f252cccb`  
		Last Modified: Fri, 11 Dec 2020 02:12:19 GMT  
		Size: 49.0 MB (49022594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1991be1b840df49c513058cb44c0c2463b2ef05541d57562b6f4a80457375991`  
		Last Modified: Fri, 11 Dec 2020 02:12:34 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:33bbd1b384c240e2d6e9ece7633db8292555210192d194614af0aeca81e128cf
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.1 MB (54144945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d72381f51b019c1426bcf51a5f0693988b17fe82c50242ba93ab68af894edd05`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:26:52 GMT
ADD file:dd188822f88de611569750cc3021f23a507f06e7d1d0437346848d554d939cd1 in / 
# Tue, 12 Jan 2021 00:27:00 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 00:27:26 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:76c3a2548b37dbf45f7e93753542dc9b4c651cb8c335873d2b2aac22c3701d18`  
		Last Modified: Tue, 12 Jan 2021 00:35:37 GMT  
		Size: 54.1 MB (54144720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fadd23a859e2be1aa2a94c5c17a97b37aa08318809460c637c84f445d71f782`  
		Last Modified: Tue, 12 Jan 2021 00:35:51 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; s390x

```console
$ docker pull debian@sha256:f4b44f70c4ad8d13cd4676a45c33e93a9a58195f5e3899f716d135d017b2fc71
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (48970745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:309767a678fea8ded63773b5d936e0092c2fbd3ba2f3b4307005a2e49001760f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:42:56 GMT
ADD file:3e938cd6f055ceb3b5272786899f974036a2f2e8be5146c9a66e7a94e77e386a in / 
# Tue, 12 Jan 2021 00:42:58 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 00:43:04 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:ce69d88400d4583b3741626f7c2c2d870fea78a646a6bbd860a7c759cec08544`  
		Last Modified: Tue, 12 Jan 2021 00:57:30 GMT  
		Size: 49.0 MB (48970523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d27798324f69b740c43c4b502979a4eeb2c6cf57e33d9dddc874d7eccd8b5de0`  
		Last Modified: Tue, 12 Jan 2021 00:58:49 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
