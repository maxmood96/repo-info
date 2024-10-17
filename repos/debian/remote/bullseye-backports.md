## `debian:bullseye-backports`

```console
$ docker pull debian@sha256:063d20a0cfb799c4208c37c9f20d7d09ad040aebbebb4f228ad3c077536791be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `debian:bullseye-backports` - linux; amd64

```console
$ docker pull debian@sha256:cb15a6d9780cd1b188fbe4cffea894c60feb9efae5357a1c607cb2f641fa89df
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.1 MB (55080838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0827f8d4cda3d9aa4babb385390c46db1ff98d3bbdac402e189cdb2c15248ca9`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 00:20:39 GMT
ADD file:603894b180221fc8174e291cd1177a2b9c09a07d1d9ba4d5b5aecdf80ad91fbb in / 
# Thu, 17 Oct 2024 00:20:39 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 00:20:44 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:9439c0e98e5f72dba1ea7cf303c3ca61ff9a91b26911886adb4266e2ad40bb58`  
		Last Modified: Thu, 17 Oct 2024 00:24:16 GMT  
		Size: 55.1 MB (55080611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52fe356f32e7e4e6dd3dfdb285b7f74cc7fb60dce453aacc08a72b5dfb78cb76`  
		Last Modified: Thu, 17 Oct 2024 00:24:27 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:54b21df3bc6b689553df5fba2cb37c9606934371b51dc1513b29aec642bdffa0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 MB (50240605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58e018657cca65f1cc593927b4b0f177e350d5a69c75f2670a750eda1ea2b0ed`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 05:13:55 GMT
ADD file:9ce266c398209e90f7206a05ac5b3ad0e1b36639b555d8c794491312b40e94cc in / 
# Fri, 27 Sep 2024 05:13:56 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:13:58 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:5b73fe599d8a11adf217817ed59555cdbc95d93efb1d72ea85683e0e5ea179d6`  
		Last Modified: Fri, 27 Sep 2024 05:17:30 GMT  
		Size: 50.2 MB (50240380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f1b9328e2b5ff3492529ba7ccd7bd64e327b6cfdebff876d125ce2c62e967e0`  
		Last Modified: Fri, 27 Sep 2024 05:17:43 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:8580633832ce5d0e075639792d4a19a284a90224b5cee1dad08e93107aa6189e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53734090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43a7750227531927b07d17caf5c3ca530ea463bf24176cb6f3eeb80bbade1b20`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:24 GMT
ADD file:20638e93d5a3e884b24b90ba3bef17ad5a4c795085c457bd5729f2f5caaf6a73 in / 
# Fri, 27 Sep 2024 04:38:25 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 04:38:27 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:374a548aba539daa8d37f8b0fe7326b582daa60fe22cc343a838af2e82a4ca1c`  
		Last Modified: Fri, 27 Sep 2024 04:41:08 GMT  
		Size: 53.7 MB (53733864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a143de137675c5a7cab210f67b90e2de5eb6460e6bbf6252548c4fa2399865e4`  
		Last Modified: Fri, 27 Sep 2024 04:41:19 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; 386

```console
$ docker pull debian@sha256:1de14a33a77bdfa25b1321ba1c1bb781218b774e30af08dbd68c7c5ccf35e7dc
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.1 MB (56078047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f4906522eb86d7d945bbfae8e8cee9f7f2601b16fad470e9e73a45e1078c630`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 00:39:07 GMT
ADD file:31542b73f2ef95a398c04a3361c14f990df163d3e44e6722e9514136e87e3e77 in / 
# Thu, 17 Oct 2024 00:39:08 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 00:39:11 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:cd6bd96dbaa583d06df851786128ccc2ec26b49565e22942268380380fa3588a`  
		Last Modified: Thu, 17 Oct 2024 00:42:53 GMT  
		Size: 56.1 MB (56077823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9f6d7cea03c5f62b2407320f518b6faf28c1e90392c5f0490fe04cddeed3c47`  
		Last Modified: Thu, 17 Oct 2024 00:43:04 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
