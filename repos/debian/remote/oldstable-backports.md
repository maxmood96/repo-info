## `debian:oldstable-backports`

```console
$ docker pull debian@sha256:b88383bcf38b848f1f12cb99f70d495f4cb21334fa480db7565d9e78c5cdc45f
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
$ docker pull debian@sha256:8817f7e9169adcb1550c73d2a6b4964fbff6adafefa28debbecbaa6bdf144867
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50437367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cea87495549a449977780cf8d5554883ce35913905076150aa73c39d9b032901`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 01:23:33 GMT
ADD file:01d4d39be06fbf95ae81fff0a269566102be821560c2b09c91a1d7ad09c03d20 in / 
# Tue, 21 Dec 2021 01:23:34 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 01:23:37 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:77245358ecd9717f050393dfd48400a8fd0cb71a4527fae22c5b0229b02107f5`  
		Last Modified: Tue, 21 Dec 2021 01:29:29 GMT  
		Size: 50.4 MB (50437142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7abe1f9f8eb3d1536cf3d71c1bee0848ab65d4921371953529e282c8d0ed9b5`  
		Last Modified: Tue, 21 Dec 2021 01:29:39 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:adaf728b2bb83375529e1baaaea180a9345f2ed775ee259eb3e5076454972d85
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.2 MB (48154554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b47f338d5d6d55b5518d91bf56c62bb939ec4328f90b05c48f092c0ab408e3cc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 01:52:54 GMT
ADD file:1a710ea282cd5d0c3a4a9b8f78a2236a123395bab356c5a373ee20a7eb2520b0 in / 
# Tue, 21 Dec 2021 01:52:54 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 01:53:07 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:f7d4ff054d0270c117d279bddbaff9d319a0c080451130e6a174edfb798faed4`  
		Last Modified: Tue, 21 Dec 2021 02:09:19 GMT  
		Size: 48.2 MB (48154329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:371a903f7a90359a8d769ac14ffd9ed2b8bf9f74ec3e423af84fb3f5d650483b`  
		Last Modified: Tue, 21 Dec 2021 02:09:30 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:fdba432ccf830a02649a5eed96d68388c0bddef4c517d289c52d97ff3037198d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45918323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5553c66e7d1014d4d615f3f2f0051bd63681927f7bab58355061b82d4b7f307f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 02:02:18 GMT
ADD file:d675ac7d57eb4e13f34c78ce240394d217aa5fc0a9704c76ff0a0452ac591b17 in / 
# Tue, 21 Dec 2021 02:02:19 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 02:02:32 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:7f8219fe81c8db60df861ca59b9b4ddd5519cce72065aa144ec7caa59145d5bf`  
		Last Modified: Tue, 21 Dec 2021 02:18:41 GMT  
		Size: 45.9 MB (45918095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b72e4d6b7c4157abd2cde53900475018b3977489823eada064cd5f4254934145`  
		Last Modified: Tue, 21 Dec 2021 02:18:53 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:5276b6a3fd2821d852037235114c9c68540791ef9205aae1f5a415f7a4695b4d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49223349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7fd50a47136fc62d18384558caa49e3e45cac6203622792c97016543ff0f560`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 01:43:21 GMT
ADD file:da55f63309c3e3eeaf9b6d9ab141fe3fea1750a44e59e739a5683fb985bd90fc in / 
# Tue, 21 Dec 2021 01:43:22 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 01:43:28 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:aed84f893300b9a43b86015ddd8e76ed296f1643ad906676e325a0b1169aa37f`  
		Last Modified: Tue, 21 Dec 2021 01:50:44 GMT  
		Size: 49.2 MB (49223123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8629043442ccc1e328225297f392a8e80332ceab99894e5288906a24dbb5d9a2`  
		Last Modified: Tue, 21 Dec 2021 01:50:54 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; 386

```console
$ docker pull debian@sha256:55044506e23b45c1cdf7ef0a0287edd6fa344dd5979f6c5dffcc0a2ba017f043
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.2 MB (51208019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa00f0ebd9a7830235fcde073a628c264eb57bd7f41cc4ea80a72018ca45d35b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 01:41:32 GMT
ADD file:67c4844a5e7d215e401cb1a526e7d1849ef0215091cc28f1f932585a50711b2e in / 
# Tue, 21 Dec 2021 01:41:33 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 01:41:40 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:06055311534f5eb75b41b08fdde9cc4d677943a7aba8f14d611b02ed14a127ca`  
		Last Modified: Tue, 21 Dec 2021 01:51:00 GMT  
		Size: 51.2 MB (51207794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b0cdb00242e44bb1226d001fb657ffbd513e650fd44a73095cc1736090b1a43`  
		Last Modified: Tue, 21 Dec 2021 01:51:14 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; mips64le

```console
$ docker pull debian@sha256:c8b0bdeb64ff5a5d0e774f9ed69eab52f0395220072585aad29a36870b9b4704
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49079885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22935a1f459bedabef745095fec7ea6f172fbbec00ecc211dbe1edfd6ffbae60`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 02:10:27 GMT
ADD file:8bd50c7db508e7ce000241707a9634d1d149986edc86a1833aeb023eb551e3ec in / 
# Tue, 21 Dec 2021 02:10:28 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 02:10:37 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:c314eb3e020dc848d94f20d859068dd62237b91ed8282d4db8801ef6e15a971d`  
		Last Modified: Tue, 21 Dec 2021 02:20:39 GMT  
		Size: 49.1 MB (49079658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:723c734a2bafd122e43031342183424efb7152db03d14410058d59120856665e`  
		Last Modified: Tue, 21 Dec 2021 02:20:49 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:922132139078117fa897674b0135739c6b76452412df02e0eed07b33285626fe
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.2 MB (54183960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22cc36d26f5f300c9efa8da435e2344ec3887478831b2363e2262613e435e55c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 02:21:27 GMT
ADD file:3150b5e1f83ba745bf045d86dcc3a0c63af07d9dcad02124696f44e81c1b6fd5 in / 
# Tue, 21 Dec 2021 02:21:34 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 02:21:44 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:19b4c40593c00102512273ff921b6a738f9fffa7aef82e6f7a78fddfd36d3f25`  
		Last Modified: Tue, 21 Dec 2021 02:30:46 GMT  
		Size: 54.2 MB (54183731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e76164efce84da021af5c3cfe66bd9a1545b648fdbec3c5bb77a420333ddf7d`  
		Last Modified: Tue, 21 Dec 2021 02:30:58 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; s390x

```console
$ docker pull debian@sha256:366ebc9a46114249e29c2727c6d15ec3be4822db45843aa4ac0591828ed90a57
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (49005678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:214f1025f83080afdb4f42af7d8204fdf62807cc086c0f1a983deb2eef874e07`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 01:43:09 GMT
ADD file:37e3ccece672e6c0ba669033fc5d6a331e6c60cb93bd1100e2a98a24a8cbd364 in / 
# Tue, 21 Dec 2021 01:43:11 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 01:43:18 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:c479c9091d0265cf5a542e1317d5c169672f55acab6d6d1ddc52e016192e8a1d`  
		Last Modified: Tue, 21 Dec 2021 01:49:07 GMT  
		Size: 49.0 MB (49005452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac8cf4897c440fba4e9f046ce602e341c23bce7faf0dbcea9e70f109f029474a`  
		Last Modified: Tue, 21 Dec 2021 01:49:14 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
