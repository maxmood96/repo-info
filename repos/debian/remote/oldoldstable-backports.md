## `debian:oldoldstable-backports`

```console
$ docker pull debian@sha256:48ff0c45e352deb3c6887eb26688791dee1906a1bcd5444c452a4adc5f9b19b3
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
$ docker pull debian@sha256:ccb588b16198037b8d238c294b6b15964b44379c35d28f7bfb0d591650f00c4e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45380652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:358bae219553235e04a37d1285aae66c127db65b647ad5725b908023e7089682`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:21:11 GMT
ADD file:41411e498f99721f107b9f5f8ab721441c8b3b171ae2a11cac626a562e2fe147 in / 
# Wed, 17 Nov 2021 02:21:11 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 02:21:15 GMT
RUN echo 'deb http://deb.debian.org/debian oldoldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:95dc2f784b302e53b28c5011779964a13473fa55794a88c73489c34978f95069`  
		Last Modified: Wed, 17 Nov 2021 02:26:52 GMT  
		Size: 45.4 MB (45380426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17e854a23605b11c1d81bd6e18e20935704fc60bf076f2ac7d30a3a7197d1ba0`  
		Last Modified: Wed, 17 Nov 2021 02:27:02 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldoldstable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:1df20084f8e7bb0f596ec23b9ad9c3e76ccfa8dc2e2193fd31ee59b4aba4e9be
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.1 MB (44091629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf2ad52cc6663b6708dae8b731b45c11d38aa3bd7bec9be6d872a8cbcea509ff`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:52:06 GMT
ADD file:68aa157a5d8e0ac1947f151a597ad6fd7e29853cbe29a9be5cd21482e4afa35f in / 
# Wed, 17 Nov 2021 02:52:08 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 02:52:21 GMT
RUN echo 'deb http://deb.debian.org/debian oldoldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:25da075bdc56c2191aa7ef6e7631f3c24a42006f6f84920454aabedb691ac1e7`  
		Last Modified: Wed, 17 Nov 2021 03:08:26 GMT  
		Size: 44.1 MB (44091400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57b841ca46d16f569d615d69d1914ab8023ee8db35e6a9353e0d2b113cbe4209`  
		Last Modified: Wed, 17 Nov 2021 03:08:38 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldoldstable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:cb37b86bbe2ba86b56a5c7203c87f1e6f01dd0e00c569b40ccc51009e6291b2e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42117111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7e2ce471b56e3825aaa732f5a4be369e4b8ac48246d4182caf19126e10cc45e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:01:14 GMT
ADD file:9fe034588d3d2f104d5aeabbd50c5962d6eaca10ab66ca53a733c09c2198092d in / 
# Wed, 17 Nov 2021 02:01:15 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 02:01:28 GMT
RUN echo 'deb http://deb.debian.org/debian oldoldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:b09753a0fa5832cd6796122a4aba45a3ed13f0371593065aef0ffef747c6030c`  
		Last Modified: Wed, 17 Nov 2021 02:17:25 GMT  
		Size: 42.1 MB (42116885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d08254bee10751f58926233ae8599c4b0b561e99ac1e45446d67688ecb984055`  
		Last Modified: Wed, 17 Nov 2021 02:17:37 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldoldstable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:8fdbfa45bd7a8726650d2d9fac77131deb41faad7d7688b6968eaaab7377e5be
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.2 MB (43174701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b06b908f38d2799d6c6f591f9b1a1980354bb617845ac1039dc41714d571d25`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:40:55 GMT
ADD file:7a50bbd1118cbbcc95d6c4e1ae912bab0503d10209cf27e88bd7241a76390f9b in / 
# Wed, 17 Nov 2021 02:40:56 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 02:41:01 GMT
RUN echo 'deb http://deb.debian.org/debian oldoldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:08e624181b9f21c13fbf44c78f84881aba565b51554e1bae8e119c729bd3d356`  
		Last Modified: Wed, 17 Nov 2021 02:48:29 GMT  
		Size: 43.2 MB (43174476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02842259569577bd1aed1ebb82de30ef678f78e4477945e85d1411807e4aa19e`  
		Last Modified: Wed, 17 Nov 2021 02:48:40 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldoldstable-backports` - linux; 386

```console
$ docker pull debian@sha256:b5122ba3a72e11bba5931b952b9f2a4c87665d80135ddc3704f41fe5ebf573a7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.1 MB (46097451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:051e765d98da904e947021dcbce64e92f4390b4ed609f516d692ac2bb065670e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:40:34 GMT
ADD file:d3dfab18ec2c72e27a89da2e6f06868d67ed554aa27eebb2febe59ba6a8769a3 in / 
# Wed, 17 Nov 2021 02:40:35 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 02:40:41 GMT
RUN echo 'deb http://deb.debian.org/debian oldoldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:06ce23efa1728c9324b4972ad13ac7716bb38b5bb8a38c549671e53368ea18dc`  
		Last Modified: Wed, 17 Nov 2021 02:49:16 GMT  
		Size: 46.1 MB (46097226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2c8c9ca27609632844301d834992b0141f71bc4815ce285b3af7313f0caf41b`  
		Last Modified: Wed, 17 Nov 2021 02:49:27 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
