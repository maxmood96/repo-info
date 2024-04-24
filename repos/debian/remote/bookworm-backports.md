## `debian:bookworm-backports`

```console
$ docker pull debian@sha256:ae854a354abd0e3b73144e01559fe729322193070bad14e157327c855b4a3045
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
$ docker pull debian@sha256:bee16b849d2fac18a649a9ae4715f9aa4e669c1f6393ee5bc29a28c9307d76e5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49576509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f65596694d593a9d3575a7240421854437cc722d12698bdd5c274b46e53cca1b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:27:57 GMT
ADD file:2cc4cba2834c189d0dc41b5d79e1236770862c38452517fcbbb28015b88ab5cf in / 
# Wed, 24 Apr 2024 03:27:57 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 03:28:01 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:1468e7ff95fcb865fbc4dee7094f8b99c4dcddd6eb2180cf044c7396baf6fc2f`  
		Last Modified: Wed, 24 Apr 2024 03:32:18 GMT  
		Size: 49.6 MB (49576283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bb24b2010fc467023bce1b844153acf3c45c6f41c94c99ddf1626a655d2f2ae`  
		Last Modified: Wed, 24 Apr 2024 03:32:31 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:5ad4eee857f8752e55714fe5752c2751d31c5c8297717a0643070328fa515109
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47338901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:429482ee459847f71ee0cc64c758de8c8596e6356364a25fb247f027e9bf6782`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:53:02 GMT
ADD file:458ef8c446d0c1da2aca3270d75aeaf985b33ec7da8acf785930f7c48c85c8ac in / 
# Wed, 24 Apr 2024 03:53:03 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 03:53:06 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:cb55d4975809ec76ad68f4174322fed658295a5f59cfef69c5aa183cebddacc9`  
		Last Modified: Wed, 24 Apr 2024 03:56:04 GMT  
		Size: 47.3 MB (47338674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbf0cac5991fb91a9a96ff3db2416e23419502fb7bfe32c5545688205b8ec783`  
		Last Modified: Wed, 24 Apr 2024 03:56:17 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:48f6716c3447a3f3e71034ed25e4e81e1358392dc66278bca00f5613fe3c80a3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45175219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb6b7419391a2e36524a5454d5fbdda0955481446d22e780691c97aa25a4e27c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 04:06:51 GMT
ADD file:b6d26ef7cfc03fe202f7a5ac219566bc37f382ffadc9acdad685f2dd318cf0e4 in / 
# Wed, 24 Apr 2024 04:06:52 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:06:58 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:80e84b3257949a283234599e3906626cfb4ff482d06fa4dc3eaf1dd36551dafa`  
		Last Modified: Wed, 24 Apr 2024 04:10:48 GMT  
		Size: 45.2 MB (45174994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:634ccbd60b538afea6c23a549868eea142abeab57c9786bd0d0f66f68831cd99`  
		Last Modified: Wed, 24 Apr 2024 04:11:02 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:71a08247ba94a011eabb47fc93f8e8c0d7da6469dcf385d472afc40faa1edf3c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49613565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ab37646d3231afd4403f876056b534ecb71118625769b3cc4e4984c5680bff0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:30 GMT
ADD file:07ae70ad05f39a24007b6bde4418c9934bc3865fe855dfcf62a44d8a30375739 in / 
# Wed, 24 Apr 2024 04:10:31 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:10:34 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:60bdaf986dbe787297bb85c9f6a28d13ea7b9608b95206ef7ce6cdea50cd5505`  
		Last Modified: Wed, 24 Apr 2024 04:13:43 GMT  
		Size: 49.6 MB (49613341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6eb735f447f13867655a9edfd5bffc3cc8f2d16083fc04ddba93bc01eedd7c5`  
		Last Modified: Wed, 24 Apr 2024 04:13:57 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; 386

```console
$ docker pull debian@sha256:8c1a5ace914cd3c8a9c1f3475c89a9f7ddd28c16ff3e1a32d20fa493d618e8ea
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50602790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c08e5d90c44753f215947aeb6631764848935beaa297afba96efee2f0f1f5a41`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:38:48 GMT
ADD file:f9a006425066d79ec04210dee08da23c9a68df2b7ea7e47b41cbc9d8b7545361 in / 
# Wed, 24 Apr 2024 03:38:48 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 03:38:51 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:c7b4c0568972903287c2ba295779f478db7fc45d1844ec5d10e22332f4cd1d84`  
		Last Modified: Wed, 24 Apr 2024 03:43:10 GMT  
		Size: 50.6 MB (50602565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:529bff58a0adabd10f9129963fdbe983bf500c06ebeccc4c42a1b889a88bfe7a`  
		Last Modified: Wed, 24 Apr 2024 03:43:24 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; mips64le

```console
$ docker pull debian@sha256:d841c4a403014d3985a432abf4797bfa2019653df1b75d946ce6a2deef40be1f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49583013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c50434e014c1c62da7b5dc49860e1b842566180da9103b73defe8d2ec6b3c26`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:13:30 GMT
ADD file:bd5e48bc3973f1ba0b2958f5feb2ef619d1da33cebe3daa160741598f3a64020 in / 
# Wed, 24 Apr 2024 03:13:35 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 03:13:55 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:128b5268b494ed46f2601900fdc8201341f67542053dd84964164d230083ab26`  
		Last Modified: Wed, 24 Apr 2024 03:24:37 GMT  
		Size: 49.6 MB (49582786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:929e4b836c8ab1861d9f0e13b75187df335520ced07a6215435b1e68f9f087d4`  
		Last Modified: Wed, 24 Apr 2024 03:24:53 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:577ae577faf2064c5756509051ff298262c9acc3fc9f889908479b3f5fc9b06d
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 MB (53580395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a1560db9bc23cfc90c28f5014385a63325e0a90bbb4114b7157d5c8a4fc31c3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:20:52 GMT
ADD file:6b48a0374d2bf17058a1ace290a29b25ef9f56d85e94d8cd33ac09dbdc5daddf in / 
# Wed, 24 Apr 2024 03:20:55 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 03:21:05 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:bf47934b0700489c27f4b1918c464037353ebec2ebc12585ceea997c9a34c71c`  
		Last Modified: Wed, 24 Apr 2024 03:25:57 GMT  
		Size: 53.6 MB (53580168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4303489edf6501d15efb16262224fe72e7d7adb7135699bda4cd666558efeea3`  
		Last Modified: Wed, 24 Apr 2024 03:26:12 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; s390x

```console
$ docker pull debian@sha256:9d5b157d5f4eb2db572b3214e773d9181075911761ee3c26e73673200a8391a5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.9 MB (47942433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:620d88e561fcf4934d8fd0860164e98467f2cf80529a33ba80e25f6b33a00ffb`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:42:45 GMT
ADD file:6b0e091009ac95d80973222b4f56557fc521253f20bb18eea1c9da2b61ed5cc2 in / 
# Wed, 24 Apr 2024 03:42:53 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 03:43:04 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:ea1cd174fa855055f0cc0296260c9e987dbd4cddfc8655fe48891b91e5af95b7`  
		Last Modified: Wed, 24 Apr 2024 03:48:59 GMT  
		Size: 47.9 MB (47942206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:047841b0c2d09476b7910b9f2b6951c871ca55ba2eb1e6ee7c038909ef9b6029`  
		Last Modified: Wed, 24 Apr 2024 03:49:10 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
