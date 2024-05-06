## `alt:latest`

```console
$ docker pull alt@sha256:04c4909a94163a1f52cec9f1774f052e0c0ff35cbb7c449236916ba273a1acd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `alt:latest` - linux; amd64

```console
$ docker pull alt@sha256:27b04510c503f52648bb5c281fc248252611015ebec890232b8595070608f9a0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.0 MB (43995139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9f482e38e5276576d5fd186ca9602a9d234151374690890eefe66c3a6fb6205`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 04 Aug 2021 22:28:37 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Mikhail Gordeev <obirvalger@altlinux.org]
# Mon, 06 May 2024 18:34:49 GMT
ADD file:5baae488d66c9db34fe5f32c3e1fb75771157c1567f03f9cf327db694f9d4c18 in / 
# Mon, 06 May 2024 18:34:50 GMT
RUN true > /etc/security/limits.d/50-defaults.conf
# Mon, 06 May 2024 18:34:50 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f9d0f8e7cd3d320e39cae2eb5a101ba901cd06afd57b822c967b626e09819552`  
		Last Modified: Mon, 06 May 2024 18:35:17 GMT  
		Size: 44.0 MB (43994946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e14468d58849c27c825bc822a71f7132bfda4c4227b4c2bff1e2880ccbde19e4`  
		Last Modified: Mon, 06 May 2024 18:35:11 GMT  
		Size: 193.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `alt:latest` - linux; arm64 variant v8

```console
$ docker pull alt@sha256:c831dc270b8d04cc6b40f600e46c75f464914699eda9e4ab28972afbd7107492
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.2 MB (43207857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3371129c9fa4cd8280c9fcd94fdfec2da5b0171f749b231ecf6e0c19c4dca6b6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 15 Nov 2022 01:39:36 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Mikhail Gordeev <obirvalger@altlinux.org]
# Tue, 26 Mar 2024 00:27:34 GMT
ADD file:464b73a0a4e7e611c1e9bfb06a33188428f2f4e1ce2372e6ba1c90decd3afcd7 in / 
# Tue, 26 Mar 2024 00:27:35 GMT
RUN true > /etc/security/limits.d/50-defaults.conf
# Tue, 26 Mar 2024 00:27:35 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:e6ac60b6d26d53fc2a403207e6c6af42c76edc8a3aad45af5e76e52064c7184d`  
		Last Modified: Tue, 26 Mar 2024 00:27:59 GMT  
		Size: 43.2 MB (43207666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3154bda171f7d3c2fff4daf3ff18fb8947537671c39cb1c6afd9ea1627f0f2f`  
		Last Modified: Tue, 26 Mar 2024 00:27:54 GMT  
		Size: 191.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `alt:latest` - linux; 386

```console
$ docker pull alt@sha256:463047774482e650a17dbf89e9f5e57916e4ceb13b711bccc9d7f8473a2c13f6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.7 MB (44685504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72fd0fec3e03d5a8076b22badd250b5a6326ca0b89fc1c3f841c66b5452002ad`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 19 Jul 2023 23:38:46 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Mikhail Gordeev <obirvalger@altlinux.org]
# Mon, 06 May 2024 18:48:37 GMT
ADD file:2887da676f8bfc9522ebd869867543aa01020a5f5c4fe025d395631a2dbbdd53 in / 
# Mon, 06 May 2024 18:48:38 GMT
RUN true > /etc/security/limits.d/50-defaults.conf
# Mon, 06 May 2024 18:48:38 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:61211fe58e0e98026ceb39e06ac107f437a48266175d321ff461ec607480fe58`  
		Last Modified: Mon, 06 May 2024 18:49:07 GMT  
		Size: 44.7 MB (44685315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d978b7542e02dc034fd88e846e6bf7dfabc49293912cf17cd4077df2d018db4e`  
		Last Modified: Mon, 06 May 2024 18:48:57 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
