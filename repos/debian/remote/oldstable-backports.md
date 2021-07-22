## `debian:oldstable-backports`

```console
$ docker pull debian@sha256:fb9d75201245b9b7f7075a4a4d8c2073ebd930ac29df18888a5aabbc66afeefd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `debian:oldstable-backports` - linux; amd64

```console
$ docker pull debian@sha256:c88ddd00b28c7e86611b15913311fd86ffde13287c1fb0095b5dfd50fa940fd5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45379986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:180aa2e7d6d20da166053495017f40b43c1cf2880c8bf7796e137077a8893549`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 22 Jul 2021 00:45:56 GMT
ADD file:3d0b9371eaa53baabfc76be00853df6176b9a01e2addba6795435a5da5463036 in / 
# Thu, 22 Jul 2021 00:45:56 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 00:46:01 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:f2dcaed17b23454647219b5c8e39183bb720828c85f0c513541f435aee363dd3`  
		Last Modified: Thu, 22 Jul 2021 00:50:57 GMT  
		Size: 45.4 MB (45379762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4c48f5c8d86d51b5c5e1ca2015ff39ee3fcf9b95e3be3a786aece052332dbf2`  
		Last Modified: Thu, 22 Jul 2021 00:51:07 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:9892900ac91c259ee0c43ddb4d82e2aa23b7a2bdc7ccb4ba7110f1abb454bf0f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.1 MB (44091955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd25e6bce1397efeadaa9cc3b991e252527c344dcd4bc8c38635daad57b9e505`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 22 Jul 2021 00:50:32 GMT
ADD file:5e9f5837f2d689303f1becbb1f16002d8fbbc307b05f635b7910ed22c86bc62e in / 
# Thu, 22 Jul 2021 00:50:33 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 00:50:45 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:41178ba1df4fddd620059f58dbb2436b5f13d3aa3bb503b42b3dab13c79f8288`  
		Last Modified: Thu, 22 Jul 2021 01:02:57 GMT  
		Size: 44.1 MB (44091727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4084af1045cc8974c2b3a95582f1363655e4779bf0c546aba7ed0b8425516d9`  
		Last Modified: Thu, 22 Jul 2021 01:03:10 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:7cbdc1e6dd2fccc8ce4883045fec3a7056f496faa6c6750dd5d18773b6fb3214
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42120150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5802d8715cc453d6ddf900874c07e2f82a8d845ecfdc773fadf1d65590d9823e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 23 Jun 2021 00:20:53 GMT
ADD file:6149df75ddf19d47690e962c672d889496581efd3f91c8de4a5035268d0f3c1a in / 
# Wed, 23 Jun 2021 00:20:54 GMT
CMD ["bash"]
# Wed, 23 Jun 2021 00:21:06 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:26957e3a4db2d81be1b1d8cdb0f2c51181c416a7987c443f1be43fab133e5877`  
		Last Modified: Wed, 23 Jun 2021 00:32:35 GMT  
		Size: 42.1 MB (42119924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a1468a6c089040bf5cb1d8944e42c7e25735b0f3cc95e5b909c78231cc8f4a1`  
		Last Modified: Wed, 23 Jun 2021 00:32:47 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:018d102e1c7d6e6a8aeff19d5278ec84126b10c30944bd45e0c19a21c56c262b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.2 MB (43178638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b798644917e1e2148aac5d4dfc26ee68c08539b32342d948dddb7ebf2bad387c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 22 Jul 2021 00:40:24 GMT
ADD file:398a8aa06199f4b3ea894d17d36517a5683f36e3bee4e8ad82fca7ffe47f257c in / 
# Thu, 22 Jul 2021 00:40:24 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 00:40:30 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:5770c37508f55d5a3fb70a81606105f0ff7d537208d4a1a5cb1ed9ffd6f2e2cd`  
		Last Modified: Thu, 22 Jul 2021 00:46:17 GMT  
		Size: 43.2 MB (43178410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69315092b5f8af5700dcbff8e39289cd3ef6d416f9fe6109e1cde49cc0e34153`  
		Last Modified: Thu, 22 Jul 2021 00:46:28 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; 386

```console
$ docker pull debian@sha256:6508790c451bfc2e6900d3593880ce0dd00ae37b9f41ba341712c448a4ea25f7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.1 MB (46097491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:610fe537ae2a947610c9bd2b665f96701ccc0e32a2934d73e911a2e60d400668`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 22 Jul 2021 00:40:04 GMT
ADD file:54561266b1fab3822e1d57e363ffff35f21f6f667909ab6222f057372b67b0e0 in / 
# Thu, 22 Jul 2021 00:40:05 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 00:40:11 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:e80780f8940a669ebba1d2c9c4303b7c56ddc033181c10bfc95a9a360daec407`  
		Last Modified: Thu, 22 Jul 2021 00:47:04 GMT  
		Size: 46.1 MB (46097263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9af73e22371590d747e1b55b216312f1e17d33a2b81a1c2dc0adf93ce598566f`  
		Last Modified: Thu, 22 Jul 2021 00:47:15 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
