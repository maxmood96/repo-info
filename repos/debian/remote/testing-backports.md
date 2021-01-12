## `debian:testing-backports`

```console
$ docker pull debian@sha256:886a6fa12c41943e9ad9f66f9ebaa5c034cf6b9dc9c79ef84f4b2e2a6631fc63
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

### `debian:testing-backports` - linux; amd64

```console
$ docker pull debian@sha256:22ab239c5d592feabf6ccff383b4c99aa097c71063f2f71ffe33cfbf10092bd3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 MB (53566504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00f44bc88065b51564e56ebc2e237cba555311a6a8c5b1d7fcacaf55458f63a3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:35:33 GMT
ADD file:ec3a8744e6d19825f056cd444a8fc650e7f8f9a94a6c88884237da472b219fd6 in / 
# Tue, 12 Jan 2021 00:35:33 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 00:35:39 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:6699a6ece22e14f81c71026455810d95b56a6dd5c0812217320f30bf1b4bd75c`  
		Last Modified: Tue, 12 Jan 2021 00:43:46 GMT  
		Size: 53.6 MB (53566282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ad5227262e445f31d6d4a91119b4324e02ded95f5d5c672a1a46967a17d55d0`  
		Last Modified: Tue, 12 Jan 2021 00:43:56 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:26699a49585df161a3a7a854f9beb40ec7dee296bdb9c806e61fb5e81a9c12d4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.5 MB (51487723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1eb4158996ca7e781feb0931f1704eecdb22df9bc2c9809503a399cb85b455a0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:55:56 GMT
ADD file:df908d4fcbb50866c8b34d50f2ca9c346cd851984cefb8de7e9ff4a42b8d18cd in / 
# Tue, 12 Jan 2021 00:55:57 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 00:56:06 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:337c57196da6d476c6ded3fd827ec7ed76bd05a0715df687e55cbce054db13a3`  
		Last Modified: Tue, 12 Jan 2021 01:05:35 GMT  
		Size: 51.5 MB (51487498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bad7608bb43e5f16e78b59dc16bbaf50a3e8a639f98bd4f4f76986249c1690bf`  
		Last Modified: Tue, 12 Jan 2021 01:05:47 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:fbe7f9af69f408ac7882decb1493b3127e69cbdd69083c830c36906df5755bb2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49159881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f38c11f1d89d306cb45571cc568e2acf1cd56d797687c6d6f7e5fba0b824da8c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:06:07 GMT
ADD file:1e03ef832cd977f6b700aefac7b2c9f8b65cdcce6823c5b9301384eee68cb570 in / 
# Tue, 12 Jan 2021 00:06:13 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 00:06:24 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:2dca042368cf7a3c7ce407bdbbea6e89c6fb5a9c3f7180b18c3b453a02013e01`  
		Last Modified: Tue, 12 Jan 2021 00:16:26 GMT  
		Size: 49.2 MB (49159656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c1c88ec47c96322b2eb27d22f419486579571b3c6b43dfebccad9ccf1671ac4`  
		Last Modified: Tue, 12 Jan 2021 00:16:40 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:76ae359f42fb6d058c5978c3421a05cd0c6519f1c6a8c9d8853286074b715060
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.4 MB (52428611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dcea40929b119ab94d95a8985f9e9c29a96b139891d0f46e066eef1ad235b57`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:46:23 GMT
ADD file:48fbb35da8de6ff711480aa027f137139f79e852973afb58dea3460bf0283006 in / 
# Tue, 12 Jan 2021 00:46:35 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 00:46:50 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:f37f58c0cf881aabae111871e3d6ad56dbcda59b0d0d2705993a3166055432e2`  
		Last Modified: Tue, 12 Jan 2021 00:55:48 GMT  
		Size: 52.4 MB (52428385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:069b642df8274e95120471cdb207390ba3dd0da097113e50542a84d26f2c234c`  
		Last Modified: Tue, 12 Jan 2021 00:55:59 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; 386

```console
$ docker pull debian@sha256:e652016b78dbaf0e586ec0461b359ecaa0167eaea9c4a7874d453cad131b988a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.6 MB (54618229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23d37aff8efddf4f5fe4b9ce9f60b0b9cacb6a92e601ab80894767f9194da7cd`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:42:29 GMT
ADD file:e2124e8b9f04a77426ec6fa14a86b2780e54b2130a5b7c96b2798219d746b69d in / 
# Tue, 12 Jan 2021 00:42:29 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 00:42:34 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:c3b522b29620ce3663ffd1db4debfe8fd44660a857bbb165785817381de3b820`  
		Last Modified: Tue, 12 Jan 2021 00:51:25 GMT  
		Size: 54.6 MB (54618007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:967c044637cd76ddbbb06476d342d37f8c770d179ba709931118db98b8c4c2e9`  
		Last Modified: Tue, 12 Jan 2021 00:51:36 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; mips64le

```console
$ docker pull debian@sha256:a354a3fc5b979ffc3d2046cc1b986a6cf95c7c093e67581f2b6dd30e1acdbdbb
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51829755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7595f325f8e66d42962ae5af52a2a2742b688544efe0e3754c7dc91a6151aca5`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 11 Dec 2020 02:05:27 GMT
ADD file:a962c401561b0b9595070a2d02c8bf585824af3423727a8a42796baa7c28552d in / 
# Fri, 11 Dec 2020 02:05:28 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 02:05:34 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:b04f7c22a03dd463866bf347f62a9c1d60a806587b3be5d5548eca723f4990d2`  
		Last Modified: Fri, 11 Dec 2020 02:13:47 GMT  
		Size: 51.8 MB (51829531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fdf7ca5cdd26c73e638c843cdc6782dd060f357a470f7ddf46ca71c553a5a2b`  
		Last Modified: Fri, 11 Dec 2020 02:13:59 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:e675b33ce690f123daa9c9c33f876e69681f52173db1db397a3f61bfdd47bc1f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.6 MB (57562501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:806cf8e07c29c4f0a91333023a17417e42493749eb5c326b851d218d7f05a4ba`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:28:12 GMT
ADD file:7c5aef981ec69d203ed3041958d604b3c221d38286982325e933a4aea004fd00 in / 
# Tue, 12 Jan 2021 00:28:23 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 00:28:49 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:6168374c1cd1389f3d510ecd4c9bd0520534b68b8f0f32d0479e4fa2e3e9d69e`  
		Last Modified: Tue, 12 Jan 2021 00:36:39 GMT  
		Size: 57.6 MB (57562274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0fc83643253477a9fa9245becea3df9c5fbe292c9ae67e110393a90e11c3244`  
		Last Modified: Tue, 12 Jan 2021 00:36:54 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; s390x

```console
$ docker pull debian@sha256:28b6a08d478be62a362e6385d7a975fafecfb1710f52dcd480c00560debea8db
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.1 MB (52108240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f047458ec9c6f9731d5e8046248297a728491f996781cfa5598ef1a2e0cdd0e2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:43:20 GMT
ADD file:79d77ce0e127a883c7393aaca5f89cab2b36703e9d08104596c40e09674d59f1 in / 
# Tue, 12 Jan 2021 00:43:23 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 00:43:29 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:deacf9aa62ade6e1002e481ea38b97d12b800eae2cb010989bdf011c18c51650`  
		Last Modified: Tue, 12 Jan 2021 01:01:15 GMT  
		Size: 52.1 MB (52108018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ae6283a679eba511c1c20a5bcf1547c1bdac5a50bc0bff9ebd328376c5287f2`  
		Last Modified: Tue, 12 Jan 2021 01:02:27 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
