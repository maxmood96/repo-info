## `debian:stretch-backports`

```console
$ docker pull debian@sha256:8a38ff9b7f4b4fceb8df22ef0a0d164410151015f0265874d90f474327c0e349
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `debian:stretch-backports` - linux; amd64

```console
$ docker pull debian@sha256:48b4cf8debbb4aa4bbb9f631566e4757148b7b6af834779afea9a333cf722922
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45377262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb61eec4385f5174048a2efbe45c21279a286620c43eee537080f71bea0daf3c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:24:10 GMT
ADD file:373a8875589f170b51fa677a3bf736feeb46ea278c553950a3eb3169a2056c12 in / 
# Tue, 17 Nov 2020 20:24:11 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 20:24:17 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:7919f5b7d60254cafc73c0d097b8ccffb72e0b6472957ece4dd5b378c5ca7cc1`  
		Last Modified: Tue, 17 Nov 2020 20:30:26 GMT  
		Size: 45.4 MB (45377037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96e9aafbb76f6e309659747bacf8c1b5aeda224580acf0bc893afea9e5159121`  
		Last Modified: Tue, 17 Nov 2020 20:30:33 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stretch-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:ec4798a0738a323809d18bbb625179fc332c669ae382ca04d6d89c7da07212fe
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.1 MB (44088954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ef276abd75ceeb0386e632f54f6564cabae2312e0c92a256963974d88527d59`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:24:57 GMT
ADD file:757e33f8832983f079f91ba77cfca5d62b54fe656af623e8566481f0f7a35d8a in / 
# Tue, 17 Nov 2020 20:25:15 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 20:25:27 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:7850b9d990d72513afd82e6c3923a3fa328516bcda19d9e0d7a63ea8f62f0b0c`  
		Last Modified: Tue, 17 Nov 2020 20:34:29 GMT  
		Size: 44.1 MB (44088729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b57f3199277a79baa3e2c8249d3b7934ec95ac2397bdcf07ca0c4d531fefcaaf`  
		Last Modified: Tue, 17 Nov 2020 20:34:41 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stretch-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:49344eadfdd9bedb52cf78f7b8b9c62fd43ffc12cb8ec3d051b868e63092858c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42117959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4302c30da59e0f72ea5832e4af9d3283d5e4170ea618ea3d80e347b9902f1e89`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:26:47 GMT
ADD file:58b80132bbfb3cae1eb2a9345e362cce1e39de41055fdcef8e5a8a8a447f69b0 in / 
# Tue, 17 Nov 2020 20:26:50 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 20:27:05 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:cfc77fa15d772230821249f78cfbb69a8fc6596f6867601b9dad16aedb424325`  
		Last Modified: Tue, 17 Nov 2020 20:35:24 GMT  
		Size: 42.1 MB (42117734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e60de6db33b70d75bb6efda5daee8117a22a6f86fe2bf5fd2170547367f3c773`  
		Last Modified: Tue, 17 Nov 2020 20:35:36 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stretch-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:15578aedf769a0ef34820fda405bbc21544cae13ab9ff0c9881b24c8472410fb
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.2 MB (43176234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38cca9624902137f55e9e5d1adda1616c258010f2c64967d0771e7a892f183ab`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:27:33 GMT
ADD file:d2e307c3e54ad69dff47f6bdacca7c8ee0957a09346bb21baec02b9de1a657e1 in / 
# Tue, 17 Nov 2020 20:27:37 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 20:27:53 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:f99bf631c0ebddf9e32516b47bf6e198efc42d06c3eb86d6f5f5739757b5839c`  
		Last Modified: Tue, 17 Nov 2020 20:34:17 GMT  
		Size: 43.2 MB (43176009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d7103c9e865ac19d1de3297456eebdd6f8a4d7d6a175ddfccc5d213608090f4`  
		Last Modified: Tue, 17 Nov 2020 20:34:27 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stretch-backports` - linux; 386

```console
$ docker pull debian@sha256:45483e32d6b51b5f6928705aeef4ddff741b44912b47bd9c47febc6d170fb0ab
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.1 MB (46095108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1c7d358d7e67b01936395bfc02f74e7c1ba01b7283df409fb25c6df0e6bdcd9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:23:07 GMT
ADD file:7d3a7e4509bddfd0743cfbbcf7420937a48151e0123a0cae600e9485a3f4bfe5 in / 
# Tue, 17 Nov 2020 20:23:07 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 20:23:12 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:893c5e9df6a4376b9e3596b0e60bdcebb5a49a311ea41ef3742718b00f71656c`  
		Last Modified: Tue, 17 Nov 2020 20:30:04 GMT  
		Size: 46.1 MB (46094887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8cef3f3f0753de6b56d42c4fcc4e7a5a78a5f7806f64a8db8c98c6d9c668456`  
		Last Modified: Tue, 17 Nov 2020 20:30:12 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
