## `debian:oldoldstable-backports`

```console
$ docker pull debian@sha256:067e4178e79c503c4b2af93794032b5f00ff310a9d0cfaa1a2f8eed4154fd211
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `debian:oldoldstable-backports` - linux; amd64

```console
$ docker pull debian@sha256:0cae6e96b521fb7355ce22a162082cb7e18980bc76a81b2b10c768bb74c533ef
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45429980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55c2a832006bda8644a418b6350dc390c4389878bb7621042b94863dde198c81`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 01:20:52 GMT
ADD file:3dadaca9df106adf321c9a84fff075b6984cbf27eb8a1c71309d9d3e88a3dc23 in / 
# Sat, 28 May 2022 01:20:53 GMT
CMD ["bash"]
# Sat, 28 May 2022 01:20:56 GMT
RUN echo 'deb http://deb.debian.org/debian oldoldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:0c0681296b3852cbaf5a0eaa7317780e1141b408a379636bd22755e85d01519a`  
		Last Modified: Sat, 28 May 2022 01:26:24 GMT  
		Size: 45.4 MB (45429752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8a60b9a427a77e0b50477105552222b60e358abeb240fc40fcd59b729ca6430`  
		Last Modified: Sat, 28 May 2022 01:26:33 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldoldstable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:e4158f76a84812d843d5dc3e844222ab33d8b39eb038acf48c8ee6530613f781
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.1 MB (44124810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da55b65ddf143e301da8a569443ca325c6dc52748b1e27938156c11ea5ce0c79`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 02:04:33 GMT
ADD file:8d7ca166b0802c7b2ab09fd086c9753c7b3f7ca5c822ed5778850ff261d042b8 in / 
# Sat, 28 May 2022 02:04:34 GMT
CMD ["bash"]
# Sat, 28 May 2022 02:04:46 GMT
RUN echo 'deb http://deb.debian.org/debian oldoldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:3f950971cc5677dfe2b2746b7e070ec85bd5b4124485f562e90412b77bfb5457`  
		Last Modified: Sat, 28 May 2022 02:20:52 GMT  
		Size: 44.1 MB (44124581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff3f664ed64daf306866c75fdfffd8c3f44574cef6d3db992fe2fe4e66b82f5b`  
		Last Modified: Sat, 28 May 2022 02:21:04 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldoldstable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:4f094503f5ed5348a3247736a65cac6e5028870605fb2f01185c9d2a45924cb5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.2 MB (42151022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f74f13a7104e54a1135011c13fc65d9c59ab2d27a51fd8e00a03bdf1318147b8`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 01:01:22 GMT
ADD file:d57d35bb2ef5ab1b89240fc0879ce8ea57a56ce03835a264175b03072bed30fc in / 
# Sat, 28 May 2022 01:01:24 GMT
CMD ["bash"]
# Sat, 28 May 2022 01:01:37 GMT
RUN echo 'deb http://deb.debian.org/debian oldoldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:e652aa8e91b0055f8432978e043c744bd6456b290dc0741c223e254badc519e0`  
		Last Modified: Sat, 28 May 2022 01:17:40 GMT  
		Size: 42.2 MB (42150793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:245e5a83cfe6021a0fca422e8853c46c435323d696bab668fa64b6f4b386d4b3`  
		Last Modified: Sat, 28 May 2022 01:17:52 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldoldstable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:5ffa04fa60d5b9ab200b5e41624cd406cf6bf187e1f25ff8e640f2ace1da163a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.2 MB (43213072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8adc3f21cb5adabfe066c8fb981a499d2862358ddc90c64de93f2fc3551a20a0`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 00:41:15 GMT
ADD file:47d38918898d0d5f23861643c07993476ceaa0fd2494ea182b005d136dbea90f in / 
# Sat, 28 May 2022 00:41:16 GMT
CMD ["bash"]
# Sat, 28 May 2022 00:41:22 GMT
RUN echo 'deb http://deb.debian.org/debian oldoldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:944dc1be71122e13738cd92a22625279fc54718f081f865944241e8ae774d619`  
		Last Modified: Sat, 28 May 2022 00:48:49 GMT  
		Size: 43.2 MB (43212844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f722c195bafaba3de1e67acc490b9bfb6c4e5d1be532340467214cd08f11082`  
		Last Modified: Sat, 28 May 2022 00:48:59 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldoldstable-backports` - linux; 386

```console
$ docker pull debian@sha256:06b181756050fcbb90c0ead427b1cf9c4cbd82db98130ea405290073b498a3e7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.2 MB (46150394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a99afbdd94c05067f705b371480de79b0d73483d1f1b84a6732fe6ceab4b56e3`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 00:40:12 GMT
ADD file:5b0d9d0e1f09d8658b36ea70ebf7b209faa4801f72e67b3a83d8bd0d810f7333 in / 
# Sat, 28 May 2022 00:40:13 GMT
CMD ["bash"]
# Sat, 28 May 2022 00:40:19 GMT
RUN echo 'deb http://deb.debian.org/debian oldoldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:4f74e9e54590523cbd0703a11ecc089fe05c0f9ec8ea4d3e344eff5e4a5c2fde`  
		Last Modified: Sat, 28 May 2022 00:47:58 GMT  
		Size: 46.2 MB (46150166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba187ab79e302b885fc32323aad217b62921a55f71f89f4071392b31770d6718`  
		Last Modified: Sat, 28 May 2022 00:48:09 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
