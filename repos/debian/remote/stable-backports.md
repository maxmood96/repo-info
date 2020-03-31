## `debian:stable-backports`

```console
$ docker pull debian@sha256:1f86895815d0a5d2edf20873ed9d23b6b452935ad3f7634310f7e43746a1e2f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `debian:stable-backports` - linux; amd64

```console
$ docker pull debian@sha256:5441cc13468145bb037bd6777cd301fb6bba138497fa1e5c71bd37ef55e453c6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50382260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6cc06b9f263512ce2b043391e8ba0dc8805e04ad08ae2397a0827ab48396a60`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Mar 2020 01:23:17 GMT
ADD file:cb0e66fdb9a172efbd019fe6bb9f91a657cc9a5c5430497a08a60f7ac33f01f3 in / 
# Tue, 31 Mar 2020 01:23:17 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 01:23:23 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:cba288b0d4fd0fa57bd941c9f37069df1c6b451324bc2bb4ecb1aa000a901d39`  
		Last Modified: Tue, 31 Mar 2020 01:28:46 GMT  
		Size: 50.4 MB (50382038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:753cbf8540af400959c23adaba363cf776ee7e89957b67ed099c04e016ab193b`  
		Last Modified: Tue, 31 Mar 2020 01:28:51 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:6b435b932b3c54d71e2f1766e40a88c5ddca5ba12dbed94e5713c1206e7dd7fc
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 MB (48095953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0461cada7d2d27cf57594f4ff46d732cb69c8e49733d0bb0af6ccde0c5cf40d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Mar 2020 01:28:21 GMT
ADD file:c47268787a41955886d01dc087dea104f811f89c4469e95fc7f95996003c40d9 in / 
# Tue, 31 Mar 2020 01:28:24 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 01:28:31 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:b53893f1463fd9439a92848da3c05e8ee4a94bf0c679efbc213e4531642739b5`  
		Last Modified: Tue, 31 Mar 2020 01:35:55 GMT  
		Size: 48.1 MB (48095729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a734cd1fa9d4ebdd2acb3fcfb87da33181c126905be4c81b12264c896ea6918`  
		Last Modified: Tue, 31 Mar 2020 01:36:01 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:8e1cb673982c8bbe877f2a4de000ac83b93046fcf87e1b22ff64a1728757e625
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45863060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ceaa50ea70de9b3f6d8241f153295f44ccf92b60e097487ae524098cb35c30bf`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Mar 2020 01:51:36 GMT
ADD file:a7c11e5cfec49d49de3e1ae706b9f03d0bda20640d8e30af59cc6ebf919f28bb in / 
# Tue, 31 Mar 2020 01:51:39 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 01:51:46 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:6e3906bc2a30f43ba24bd4c3a3dd5a3112153d31dab0f7e25dff62fe5cab5456`  
		Last Modified: Tue, 31 Mar 2020 01:59:17 GMT  
		Size: 45.9 MB (45862834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2e81c258e59b4e39a6b4e2b23d074d1895a66cd90a4781027ed1045734351a4`  
		Last Modified: Tue, 31 Mar 2020 01:59:23 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:d30067e15cf2642d2eb0845e960103ec89c78bdac4595a64d39437bb80319904
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49170221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:317858f33a18851feec05d636f8dcf42a03c341031c0afd795d6f4e85a180d10`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Mar 2020 02:07:24 GMT
ADD file:24974cf37212425e3e1f9d3c47acbbdb1a313c7450730e51260c65ce7e0249e6 in / 
# Tue, 31 Mar 2020 02:07:27 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 02:07:37 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:e7f31d14b111df4e0defd9723b43156e46ea7a621e26d218aa1a69ad07e5f01d`  
		Last Modified: Tue, 31 Mar 2020 02:13:38 GMT  
		Size: 49.2 MB (49169996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3d828b61624c6e7c3135abf4d7f9a78ebc5e7aec49c105444da7d24e0d1e8d4`  
		Last Modified: Tue, 31 Mar 2020 02:13:44 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; 386

```console
$ docker pull debian@sha256:d1890a373a91473aa7cc08a6a2f2b59c6ffa51145ddf0d68cb3ee11437f9a850
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51146332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dc2375f802326f7b5f45b7d1162fbbcf1e9935aa95c4d04cf1cee5c8a77f7b8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Mar 2020 00:42:01 GMT
ADD file:f92259534a8b90e109d636415e2aa01ec55961636c0c3a4120d041763fe06282 in / 
# Tue, 31 Mar 2020 00:42:02 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 00:42:06 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:a4eb08ca4bc2f614dd30301c5e930ea6e68c5bf13455f68ba437f47b6c679d2f`  
		Last Modified: Tue, 31 Mar 2020 00:47:57 GMT  
		Size: 51.1 MB (51146107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c335e79562d1d0ce09c5281486a5e4b4256ddeb34b680bc418bd55fd966b3132`  
		Last Modified: Tue, 31 Mar 2020 00:48:01 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:4c212edaf3daaf6ae892924b331e10ded3f8fe35467983a2448c64f708bd0579
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.1 MB (54138783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef3b30b2866210a0c4f2aced2bc66eb4821f49e43562a0c0af6aaa17c014e04e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Mar 2020 01:35:09 GMT
ADD file:14a462f8c003fa1450aafb16dbea70da424b1bae74f5e3c75ddd69c936b80190 in / 
# Tue, 31 Mar 2020 01:35:15 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 01:35:29 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:9f81f094c8988a20a0dd52a488939c3c8e27164ed057bbc5057a05f0157f7a17`  
		Last Modified: Tue, 31 Mar 2020 01:50:45 GMT  
		Size: 54.1 MB (54138559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9898180f8fd894bb0fc08e1110f3c1229b259ca5b83f899927ba28fdd9888a67`  
		Last Modified: Tue, 31 Mar 2020 01:50:58 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; s390x

```console
$ docker pull debian@sha256:d06075e53108d0b93d4f4d350ffd8726d0bcd6d34e7f08d435af28f61e3bd433
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (48958348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6847d4d17101a3fe0a01cc377a8eab35cf7a5a3823c78486c62e2564d87ae2d3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Mar 2020 01:09:54 GMT
ADD file:9a5b4d20c7ea1a8efa79b6b4909d06950a496a8f44b8cbc96a744eed489d0e60 in / 
# Tue, 31 Mar 2020 01:09:56 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 01:10:02 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:180adba0995c42b1c28d393cfd464e4e1857317afd3768d307a56b43000d3bd3`  
		Last Modified: Tue, 31 Mar 2020 01:13:38 GMT  
		Size: 49.0 MB (48958123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:367478cd55ea43593f7311563d935e4d9ecc190f8ef731631769ab18fbd262eb`  
		Last Modified: Tue, 31 Mar 2020 01:13:47 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
