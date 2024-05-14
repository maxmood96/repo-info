## `debian:testing-backports`

```console
$ docker pull debian@sha256:d257c1f651aeaa3687fe066ccd470dfd1beecda94a0481a0e042e5dba95482ef
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

### `debian:testing-backports` - linux; amd64

```console
$ docker pull debian@sha256:90747a59dc0fa2527a066bc18d73d13978dd2adc4ff6f0376b2f942f026bdbaa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52338863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4563224c560a1ec5ea76eb4492bd726b849c0f24477fd16f8b269ce2d1423a8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:30:21 GMT
ADD file:b8a11a0dc4e697e9f924afdacd33c6c1a4744e43ff2938c4539b5650bc3207a4 in / 
# Wed, 24 Apr 2024 03:30:22 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 03:30:26 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:efa2370e55f34d719cde5ccb31ebc8ceacbdfc1b76afe2aae60adf06d58474c5`  
		Last Modified: Wed, 24 Apr 2024 03:36:14 GMT  
		Size: 52.3 MB (52338640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cb02be9c6475422468f1a6ec57dfc19cbc07fc9854b7ea3c6c5a7a35730bb54`  
		Last Modified: Wed, 24 Apr 2024 03:36:23 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:f7d09c503302629b2ee53ad70e19771070bd3d4a37389533f845f01dadabb98e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49744988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a8c38514c0d92357c4ea6d9114f75e86891cdb86c02037e631d6f25e0fa94ea`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 00:49:44 GMT
ADD file:c9afe5b0a108631c043e9eb0d4e5e257843ed802ae7705c0851e82e73d538611 in / 
# Tue, 14 May 2024 00:49:45 GMT
CMD ["bash"]
# Tue, 14 May 2024 00:49:48 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:f0c10670fab205862628f1e7a3f0e32d0a10c09fe90e24279f858b7f1f447b9a`  
		Last Modified: Tue, 14 May 2024 00:54:13 GMT  
		Size: 49.7 MB (49744768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9b5b39da926b4599866cc9650d5efba9ddc734a5409372eeb40fbf32b5f66a7`  
		Last Modified: Tue, 14 May 2024 00:54:21 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:2644f59914d139c9bf985670e55a581aa802f928d2148b0dba8dcaaf8cd8168e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46930586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b17b774cb61eb119f9f52a1ff077a757302c437911a57a2593fe3576d9f431e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 04:09:02 GMT
ADD file:2b4a467dc630bd5a96cfa038ee05d8ed4302bd61d17bb3a98fcc98c0ab904610 in / 
# Wed, 24 Apr 2024 04:09:02 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:09:06 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:78ad51e512969e922ddb678eb808c8ec3053c79958e7142f172d57bc5742d09f`  
		Last Modified: Wed, 24 Apr 2024 04:14:47 GMT  
		Size: 46.9 MB (46930361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8018ba14defccc8ca659651b4a240c758276dc672c4cab7d4f480f90c0c447d2`  
		Last Modified: Wed, 24 Apr 2024 04:14:55 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:f740d9b039179946b8201cbfc645c5c7c4487793e369408bc0128055256e387b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.9 MB (52912298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f98af461e087c21a81bd36ba2d9969b6a12984e71d4a410551b86c06737bd39d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 00:41:08 GMT
ADD file:d7aee0a25e3d206c1ca526373ab1236a244025e76ee8802b2de9c7851fc7fc80 in / 
# Tue, 14 May 2024 00:41:09 GMT
CMD ["bash"]
# Tue, 14 May 2024 00:41:12 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:25b146dc3d2d8d07e05474869061ffbe0ccb76a9c19a029a9eb03dfe587453f9`  
		Last Modified: Tue, 14 May 2024 00:46:09 GMT  
		Size: 52.9 MB (52912074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:430c3e309fc08b47a5a9c4055cf762826fe348bf04d5712d2e45c83f3d78cf5d`  
		Last Modified: Tue, 14 May 2024 00:46:18 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; 386

```console
$ docker pull debian@sha256:4ccd1a2f83a768225f630a2eddaf3253ce43b18429cda9c18c406ca844770fd0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.5 MB (53536835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f5e4469d10ea0e14586ba996a031b0e10b078b0581e00375fc685dfbb137906`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 00:49:30 GMT
ADD file:6faa0308dec78b7bf27c8098473df2d1d3bf3fdf83099a1a13f777a963b69ba1 in / 
# Tue, 14 May 2024 00:49:31 GMT
CMD ["bash"]
# Tue, 14 May 2024 00:49:35 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:e05023f22044acc27df160b1a20bd50e4de5074e0a396d66d1428472a62b2746`  
		Last Modified: Tue, 14 May 2024 00:56:15 GMT  
		Size: 53.5 MB (53536612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7405aed4d1601ffdb0b5f77fc11cf6400ab60cdf2600fef82a83226caf3b8f40`  
		Last Modified: Tue, 14 May 2024 00:56:24 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; mips64le

```console
$ docker pull debian@sha256:eb994a169ecc345cf928f82aa93c46b6255281abf26dbcabb83e93c356e9585d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.4 MB (51411521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d50c3d7e4063589a0bc8ae5163ef51c595e1bfc3ff3c2b8de88cc63a638fa57c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:19:45 GMT
ADD file:39997cd262fdb7c1ab86e5bd329bbdec0b99411434fa65268aa5f2f141d1d66a in / 
# Wed, 24 Apr 2024 03:19:50 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 03:20:05 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:789997181d7b1af2be77f38fd01378403217cac798b22c2b91152db6857ce361`  
		Last Modified: Wed, 24 Apr 2024 03:31:09 GMT  
		Size: 51.4 MB (51411296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b6f63b784a0b3d9390b3db46784128848192a181cd18938a2148952a34f4928`  
		Last Modified: Wed, 24 Apr 2024 03:31:21 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:64dee8a1aaf454de73c4b67d99c850f2ed4fff38d0df7eb996498ee69f9eb1a6
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.3 MB (56253500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a8bdcd168326f7991d84693ce3eae9b73ba7c6cc0bb9f56429ccaa036e98d3e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:23:25 GMT
ADD file:96a5c70b6b470689ae9f76bf58dbbdca302ccda081b6d6fb25d3249c5a22038c in / 
# Wed, 24 Apr 2024 03:23:29 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 03:23:35 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:ce4f206e19e1d340400f7cf79402f651c42ad37cfaf199791fb616c2c0c64fbb`  
		Last Modified: Wed, 24 Apr 2024 03:29:58 GMT  
		Size: 56.3 MB (56253275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc632e4899d3df8820b37b4214114635bf6e115d519b55d751eea25b9d77dad8`  
		Last Modified: Wed, 24 Apr 2024 03:30:10 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; s390x

```console
$ docker pull debian@sha256:0e8e40ffc0a1dbfd0371a5cc5722eedb7d855ed7b95b35fa52a961b82e2f2bd3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52291273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a8a0af26846b46fce9ea347bfc320edaab17e1865a5d4d145cac00c2808522f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 00:44:50 GMT
ADD file:4648ccf21b5ed0ffb91f4df711a7a846c609705bfcc60f590fcd41b3c5fab226 in / 
# Tue, 14 May 2024 00:44:53 GMT
CMD ["bash"]
# Tue, 14 May 2024 00:45:00 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:b6988741f7ba3983b538f656a90da504a35a297351fdda81be0d7cec90e792d9`  
		Last Modified: Tue, 14 May 2024 00:49:38 GMT  
		Size: 52.3 MB (52291052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c6fe5e08df169627e7e714292ab53447725ef198e98336a77c55674489c233a`  
		Last Modified: Tue, 14 May 2024 00:49:44 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
