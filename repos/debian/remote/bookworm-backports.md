## `debian:bookworm-backports`

```console
$ docker pull debian@sha256:070132ccec90495957b49bdad98b63fc84227bfc6d85bd2d975fd8765a081f5e
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

### `debian:bookworm-backports` - linux; amd64

```console
$ docker pull debian@sha256:b464a0f624b0afc02688464434efa82c35ee2615a59659d60b95f29fb6352288
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49552828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74bf0291ccedba8a94a544fd4539285dc5321c0c8caf6fec91f0febef0440e08`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:09 GMT
ADD file:333b899a197a48b3333115a3b59efed559494808873943f606a9bc2b6e242c49 in / 
# Tue, 13 Feb 2024 00:37:10 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 00:37:14 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:7bb465c2914923b08ae03b7fc67b92a1ef9b09c4c1eb9d6711b22ee6bbb46a00`  
		Last Modified: Tue, 13 Feb 2024 00:41:39 GMT  
		Size: 49.6 MB (49552605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81a3652b1486a5636a12ef9cb968ddcc2ac31aa424f53485d4cab9346be77fa8`  
		Last Modified: Tue, 13 Feb 2024 00:41:53 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:1b28964cb2e529bb8fd686a961400af113a9ca4ac0752d9efbf5ee91dd1ec009
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47311996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:739ebf247670e4e92ada6a50da61565f3abc98826389d78d5891373bea9106af`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:08:03 GMT
ADD file:32a9c7aaf2ccd1a1e30b6cad6aff8691eb3b1405483450a082bc84962be78652 in / 
# Tue, 13 Feb 2024 01:08:03 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:08:11 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:96cfcfafa452979ace6d9825bfc1192c702df30f7cecf2ea7f7041de5d705416`  
		Last Modified: Tue, 13 Feb 2024 01:13:03 GMT  
		Size: 47.3 MB (47311769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:589778cd3c211c2354665ea31634a49082e4e721c5f98313640ef0eb74059899`  
		Last Modified: Tue, 13 Feb 2024 01:13:19 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:f95434e64eaac8bb1711e0a98ad3c4d22922937fb7cc145b8b4b9c0f1a858fb7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45178216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87bbdb43377ceae6dc934e44d24b53fefcf2b4860e738e23640caddcc125ac55`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:09 GMT
ADD file:24186d75daba80fe802230517bbb6b4e9d6c695398d1db98108b4487d27ebb43 in / 
# Wed, 31 Jan 2024 22:44:09 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 22:44:14 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:af02191d26cb0ab470ac42e81c677a72e87ee39e67a36576e102fffc8b1de4a7`  
		Last Modified: Wed, 31 Jan 2024 22:48:27 GMT  
		Size: 45.2 MB (45177992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6104ba7ce1f1c27010fc0a8337f59c51ad962ad13958b5cab0b37ce4fc4f0bb6`  
		Last Modified: Wed, 31 Jan 2024 22:48:41 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:1428629b4b9c530b1f899ae34c454128c5c6afeb7f3585a1b4ace70167e48430
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49591189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e3a40b7f1aa6590d65742892bc6d77515d17d31bc9768fcdac318ade2778d7c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:10 GMT
ADD file:73b36e8089732e9bb253d9a9db76cc1cf5c430bd49647849b77924cd5fdaf8ae in / 
# Tue, 13 Feb 2024 00:41:10 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 00:41:15 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:c2964e85ea54bbef26d274e85fa0a3fde68f074e0774d0729e6ebe341e24eee1`  
		Last Modified: Tue, 13 Feb 2024 00:44:29 GMT  
		Size: 49.6 MB (49590965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f90a471a29cc5c9a95396f0920b8dc1d1e6584e8712b851b14280ad69f59d11b`  
		Last Modified: Tue, 13 Feb 2024 00:44:45 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; 386

```console
$ docker pull debian@sha256:7e1848238a32fdf8a309bc8c9dac9cf85229c9407c8af738861be5944e9e7cd8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50582151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3ed7b4809370a67b4a745f79ac84b6ac23d991a05df754fb0d4cd73c6b0525d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:38:44 GMT
ADD file:e12b4798eb856f517a57dfe550811e57903589ffa74a09d47f7c0261e23ca645 in / 
# Tue, 13 Feb 2024 00:38:44 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 00:38:48 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:911275c2fc723590176bf48d32222d2b1299cd1a17294bdc4cebd96e25742b27`  
		Last Modified: Tue, 13 Feb 2024 00:43:21 GMT  
		Size: 50.6 MB (50581925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9025d716bcca304734c369e714cda4e46e98799b1d5de214bca7fd86f49cb867`  
		Last Modified: Tue, 13 Feb 2024 00:43:35 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; mips64le

```console
$ docker pull debian@sha256:9474ccc7d49afd24b52194780ffdc18331962c685afc01396eacae8c0f4423a6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49574287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:923c80e1297ab23bcdfe4ef84267e8732f935add8ba3ffb927a531eea3df1d63`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:26:24 GMT
ADD file:eee6c048a0eb51959b7cb7d3c4efc6652decf19517bcb25076f8ef9fc376ce48 in / 
# Wed, 31 Jan 2024 22:26:30 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 22:26:50 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:07a56ca79640510bd74a49ee96c70117fcef80d3a54a0b75ab30e3c06c58abff`  
		Last Modified: Wed, 31 Jan 2024 22:37:38 GMT  
		Size: 49.6 MB (49574061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d915eabf98877d8d84fd52e08bcb47dc70d8c2939ddcba0a3ae2685583aad25a`  
		Last Modified: Wed, 31 Jan 2024 22:37:55 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:f57ef18642ced7d71875c7fc421ea3e13775284fc8d1d7d0074428391fe370f5
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 MB (53556756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e09bd731b0531139b2e6470b2541458b2f3db42473a0dbfb9c3109a9d2ee41b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:38:43 GMT
ADD file:83b2c138b49e79b23d3462cb4b39f3f6f151b690a83c7b1ff169ae4590fa0b43 in / 
# Tue, 13 Feb 2024 00:38:45 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 00:38:56 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:79696cca44e9751723104a8e361568bddd373ed772da9f88250ba2947fbc6043`  
		Last Modified: Tue, 13 Feb 2024 00:43:22 GMT  
		Size: 53.6 MB (53556530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08d1829907f6114b54e7f625f1c43276e7c40dc746773f2d8663c67c51b4184b`  
		Last Modified: Tue, 13 Feb 2024 00:43:40 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; s390x

```console
$ docker pull debian@sha256:46393a06b91d99f96916b200818427f51d3b4a00ed08ed2c0ad22b7e78cc7cfc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.9 MB (47940991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65d137c8428ea29eaebff6a797fa87aa21c10bb05c9e83756609f3c1778c9ae6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:56:21 GMT
ADD file:b1c0200d0f8b6070dfcbbadb831cbd04bd8d1b15c3c1f8e6e13c467f6c3f2879 in / 
# Wed, 31 Jan 2024 22:56:23 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 22:57:36 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:0241650ae38ec8570f9718818b3b516c90697c5cd5686d5dd89306ae5f8e4657`  
		Last Modified: Wed, 31 Jan 2024 23:28:45 GMT  
		Size: 47.9 MB (47940767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26cde108783440c628dc7d747754980cd9f43a43224611bd8a61baa17ad82ea2`  
		Last Modified: Wed, 31 Jan 2024 23:29:01 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
