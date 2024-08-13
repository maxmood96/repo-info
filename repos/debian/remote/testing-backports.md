## `debian:testing-backports`

```console
$ docker pull debian@sha256:f18254aad0c88e05b9f629690bfa2587ae431a428d7f5996257d55bbc292ca71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 9
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `debian:testing-backports` - linux; amd64

```console
$ docker pull debian@sha256:2c062ee9f8d00c9f50af32bfb2ed3ea5a1a25eabc2ca721b88caa0e199819f99
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.8 MB (52821443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3e8a6c0dbd65cfb1200c3ec43d365acf3729444326d495964beb5ebde3c58c0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 05:25:54 GMT
ADD file:619723247570b0124cdbdcd330640fb9768a7a0580fcd6674fc64a59361d9b61 in / 
# Tue, 23 Jul 2024 05:25:54 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 05:25:59 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:082e67d038aa34d78979422af7626a1fa8594a4afa81d6465c09f9626234451e`  
		Last Modified: Tue, 23 Jul 2024 05:30:14 GMT  
		Size: 52.8 MB (52821221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:514f8b6bd9a682680c3b599827d69bee0fe9453b48b4960bce61710bac3b1c7d`  
		Last Modified: Tue, 23 Jul 2024 05:30:23 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:2bdc18a8e3f2f51ba7c7f77338dbbf285ae78803f949577ffb58b3a5dc5d8353
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.8 MB (49808022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73c23db6a01425f7e2fef0e3de9aa7ba05254819e0cd498b370319c7931c7cac`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 22 Jul 2024 23:58:52 GMT
ADD file:95ca29691d7fa462af2c12d48d13c9648f2c9f6692075cf3d658e8a87b893bcc in / 
# Mon, 22 Jul 2024 23:58:52 GMT
CMD ["bash"]
# Mon, 22 Jul 2024 23:58:56 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:d9c993b948d36b0ef7cf0af9a1260ea54e372fb65f76b2c38c0992002e055fb4`  
		Last Modified: Tue, 23 Jul 2024 00:04:07 GMT  
		Size: 49.8 MB (49807801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e710940dcb58c711c158d98408724f2a7b97a763604c8c30ff6432dd0bccf6e2`  
		Last Modified: Tue, 23 Jul 2024 00:04:15 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:368e5c9cfb745e4455c7944826a328b9bce5a369fad732a4512ead0d5f5ff276
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47313666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e52b7509aa1d343f3450c380f5c93441120f0ce556b6b6bdd46a1e666b13ead`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 03:04:42 GMT
ADD file:0fc5e170d02d8d7d4a26b3ff8a1aa2dcdca6988d8310f3050e6d404faeff939e in / 
# Tue, 23 Jul 2024 03:04:43 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:04:47 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:4a6d7c49012f37d7abd43f93d3f8deb6379d11009e106897da9e6ae153b5a6b8`  
		Last Modified: Tue, 23 Jul 2024 03:09:28 GMT  
		Size: 47.3 MB (47313443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4410691afdc2b8d49b466918420ab54f81838d9c448593b9ba9638f6f72f8169`  
		Last Modified: Tue, 23 Jul 2024 03:09:36 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:06cd18d8980ac77c4e3c0382e88adbfaf9f3e37be18e97a883591aa889878cec
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.0 MB (53026557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c16dbdf12f07fc2275745e2b4f009586f744d0deadc8f5a6a7f357e9d87110c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 04:18:56 GMT
ADD file:191eea951292a448fdf8391f23851acc883220c3612e40314b0a5264d37462a3 in / 
# Tue, 23 Jul 2024 04:18:56 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 04:18:59 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:8178889186a4cf7f663eadfa45ade24cd1b46b0ef61e6ea2ad08abad38cc802b`  
		Last Modified: Tue, 23 Jul 2024 04:22:35 GMT  
		Size: 53.0 MB (53026332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a17b676ea4657de361369678338ebed50198f8255b0d59f926e99e0adf916063`  
		Last Modified: Tue, 23 Jul 2024 04:22:42 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; 386

```console
$ docker pull debian@sha256:c6d64adec92ee91de278df856f15ec1e57cc00e6cdff6997907bbb50ae91991c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53681465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0af2822c3ba5dc45f64074d86d141bbaede5dfeadfd4cbe963ab27ef5db75841`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 03:55:49 GMT
ADD file:a2e91e15b0778617191348e094a5d3fd2dc47b1fa8928e4cac6bb030ad48b512 in / 
# Tue, 23 Jul 2024 03:55:50 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:55:54 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:d16221d6c6a5a974420204b1f52a2b2b7cd4193dc70702b7a2679865e124cc88`  
		Last Modified: Tue, 23 Jul 2024 04:00:40 GMT  
		Size: 53.7 MB (53681242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdf7464a6eeb421d0f2058e4aa5560a9f2b17bcd6545546916a70825ca63c065`  
		Last Modified: Tue, 23 Jul 2024 04:00:48 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; mips64le

```console
$ docker pull debian@sha256:ff9224f36d3ee660dfef9805f9745713db57a54c89e0ce4dc6d963cca7a0eed4
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51636358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9366e311756ab1d330d73f48368089b2b35ed3321a06f5a6671d36d261435cc8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 00:43:30 GMT
ADD file:035eef829f8ed8debad518a0347f504fc645e4cba511b125ae162ab49ba8aea8 in / 
# Tue, 23 Jul 2024 00:43:35 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 00:43:50 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:93c19873f49c0f13a725bcbfd845bc3e335a676bf9dd214b236254fd75159048`  
		Last Modified: Tue, 23 Jul 2024 00:54:58 GMT  
		Size: 51.6 MB (51636135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29bf4c1162b8e7d505c8c87b47f65abb4b1abf764778169ac86afcb98c5393eb`  
		Last Modified: Tue, 23 Jul 2024 00:55:08 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:64acb94c480653cbe130edec70e0c8ec847a5e9a2f40f751b22df8b617293dca
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.7 MB (56722285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8968a3e5ad555f352df604eefeff98836d8a3621f63f8b9ad1cc73463d6163e0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 01:28:52 GMT
ADD file:a2a9ed566b597667e2ca2f80c13e7f6156ef9de7770cd85f3275359c96ec5da5 in / 
# Tue, 23 Jul 2024 01:28:55 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 01:28:59 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:720dc0d16caf9c5de466cdb031bdddbf8af5b09238053dbfe371c831d5114ecf`  
		Last Modified: Tue, 23 Jul 2024 01:33:54 GMT  
		Size: 56.7 MB (56722063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ae8cc976d952aed17eb68e3c420ad96a43e607a2718637279d8cfa37e49d108`  
		Last Modified: Tue, 23 Jul 2024 01:34:02 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; riscv64

```console
$ docker pull debian@sha256:1e9433a66b06e3fe69d25676ec6b4a4a833a357820f10b568a8e647ced2beb23
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51127422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db1f42909c6de3250b49909febc3c19fa7685f276868ec2f88fe2671f81acbea`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:12:07 GMT
ADD file:52b983ed2ad4f2b7372fe244036fa274e305c652cc773028b8d61d68868812b7 in / 
# Tue, 13 Aug 2024 00:12:10 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 00:12:22 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:0f4dcbe9066fd7cf9df1f5c2e6f31e2bcb9fe3ec2a5221e465d90eed0eeab067`  
		Last Modified: Tue, 13 Aug 2024 00:17:31 GMT  
		Size: 51.1 MB (51127197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58597e153883797c9d6ebf2d4cb3c5e0ddefd3bfa8458725188e9b1c6909808b`  
		Last Modified: Tue, 13 Aug 2024 00:17:41 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; s390x

```console
$ docker pull debian@sha256:096c77fcb7fdf2c53f70a658e672b7f10f77b5c6b0b2db15241e3cadf4ba63f6
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.4 MB (52414471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32827b9391dae4cc331e495583c85b4fa1dde6a2251c6bb432996e866811b6e6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 02:30:13 GMT
ADD file:c24c5de69f78a6ef3e0df2856d26ea708ca0ebdee3694d47c33faaf3b5a060ff in / 
# Tue, 23 Jul 2024 02:30:16 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 02:30:23 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:79d588d68b7011912ab3b5fa8c08ba9b146dab2ef01b4ce5b083d84fffa630d7`  
		Last Modified: Tue, 23 Jul 2024 02:34:36 GMT  
		Size: 52.4 MB (52414249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aab7a151a67e4b21a61c5b1d12d6fc8fc8d1c5622fb47f768d1467a64d74754`  
		Last Modified: Tue, 23 Jul 2024 02:34:42 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
