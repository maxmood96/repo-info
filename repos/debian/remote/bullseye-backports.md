## `debian:bullseye-backports`

```console
$ docker pull debian@sha256:284d1e5c0790df1d055d94fbe3bb7b5a71438a35e44c1bd7d1595697d50dfbd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `debian:bullseye-backports` - linux; amd64

```console
$ docker pull debian@sha256:ac419add526e323e1b9c32b7ec371dda6aa282df4aaa583a20c1deb64c0e1a48
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.9 MB (51906755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3994d2be3c6763c5ad537feb497b54a787f9cc49ecdccb68b5ad7df4bf49899c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 10 Sep 2020 00:20:54 GMT
ADD file:375c01cd4aba0ddf77202decfeed5df5e3119ce460fcbf1f3b47f540a70b3864 in / 
# Thu, 10 Sep 2020 00:20:55 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 00:21:10 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:08d7334100fee80149028a0d0df44589b68e0c31592157808d18b68e6a572fd3`  
		Last Modified: Thu, 10 Sep 2020 00:33:04 GMT  
		Size: 51.9 MB (51906528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6558ed5e46ae10bf539736667840711d2c6c869f6ecd08358949dd5bea885b1c`  
		Last Modified: Thu, 10 Sep 2020 00:33:11 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:1933a3f75c74757b3bbb846d0da153f8aa9c36e1d8560a149fcee01fc1c64788
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.9 MB (49868527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc5cb36d8d03c812a7e1574cb32713c6eb53a0a8797e05d469c7114c6a13b1f5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 09 Sep 2020 23:52:26 GMT
ADD file:f71e0d87d6d096130aa8dce14ce4db75b3a50725e9ba2aaab46f722a444291c9 in / 
# Wed, 09 Sep 2020 23:52:28 GMT
CMD ["bash"]
# Wed, 09 Sep 2020 23:52:37 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:23e3aed2d466532e16ed7a54a2dc8d1ab497d8cd849573a7aa149e39f499eb77`  
		Last Modified: Thu, 10 Sep 2020 00:01:42 GMT  
		Size: 49.9 MB (49868299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31cdc75a4d7f4274b2d65c08b08635cc7fc4f8d214e28c55be6a540c5575ae83`  
		Last Modified: Thu, 10 Sep 2020 00:01:49 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:bfe79c437815ad8f2ba1e24b5ed1fd4e7669d68e8dc9acfabe87bf124b245eb0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.2 MB (48237087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5759935a8f74e1a1281eee3446023869ba131456277e68058c1402016d316a5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Oct 2020 00:58:08 GMT
ADD file:fb1050c1c18a08781bda11a75976f0483098ae971141de440f987df6c3da5eb3 in / 
# Tue, 13 Oct 2020 00:58:11 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 00:58:20 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:a1cc4a9f93bac620cf7887911c999122564026a7a9c2ca50766b3df4909c806f`  
		Last Modified: Tue, 13 Oct 2020 01:07:26 GMT  
		Size: 48.2 MB (48236859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6da2603da558a0106ba361a9c749b9fc0c4e481c621bd2d3ed9f1d87b53edc22`  
		Last Modified: Tue, 13 Oct 2020 01:07:33 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:9a036981b261715e7f776db21ce84961565eb535420cf4844f2904dbc870044e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.8 MB (50825623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e8e93b704f6a4131c7ea7dc58dd63a3868fe6609fe49ff903fa8f62c31efd44`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 09 Sep 2020 23:49:11 GMT
ADD file:82c33a26fb9be3ddaf17956539af2b205bdb6e28fe5ff1c7304ae8f294fe9581 in / 
# Wed, 09 Sep 2020 23:49:14 GMT
CMD ["bash"]
# Wed, 09 Sep 2020 23:49:33 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:5a65667356fa05b061c6733c879afab36ec44c6877341c2527e321b7206a26b2`  
		Last Modified: Wed, 09 Sep 2020 23:58:05 GMT  
		Size: 50.8 MB (50825395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d81b4c481fabc5ea85411056e259ca0e564317c5cb8b6d85e0faf85eac4675b5`  
		Last Modified: Wed, 09 Sep 2020 23:58:13 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; 386

```console
$ docker pull debian@sha256:ab5c95f9cc680f2d7bc8803f5d8363d02233d14209a39445b0ddd064aff48304
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.0 MB (52969415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec639ff533dfe3d080aad477fe1e9b27ea785e06e02d20bc8c3b8488de5297b2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 09 Sep 2020 23:39:17 GMT
ADD file:f37f3bb35b6cca1cef993e4f39f48aab88ed76e0c47d97d61b4329fd8c5c5d03 in / 
# Wed, 09 Sep 2020 23:39:17 GMT
CMD ["bash"]
# Wed, 09 Sep 2020 23:39:28 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:4e5adf65093f5c6d699308a44f2173fac564be9f4e4daf24d82204c617b438d5`  
		Last Modified: Wed, 09 Sep 2020 23:45:45 GMT  
		Size: 53.0 MB (52969189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:887ce1dc9958d1acd7a0b02370c21011c9df246d3971cd763906e6f7c7b9b73f`  
		Last Modified: Wed, 09 Sep 2020 23:45:50 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; mips64le

```console
$ docker pull debian@sha256:d1e233d8c22b212e0d6d58fb02b9482e9ffeea86063039ea81326cdac4a90ee5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.3 MB (51280006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:048ec4b5bd4545d5a7067639ecaabf2ebb1d30345e2e315a6d4fcf9f5812e467`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Oct 2020 01:08:29 GMT
ADD file:ca35129fd2f6a5420278e6a1790ba92b4afcb01f474e67f950b277b7d75db37e in / 
# Tue, 13 Oct 2020 01:08:30 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 01:08:35 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:abe3595453fb68f277799325ac06eb70b1ca68c849710051325993f2f22b051f`  
		Last Modified: Tue, 13 Oct 2020 01:14:37 GMT  
		Size: 51.3 MB (51279779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:032f4a7573f8f33ea2c1c881a7160efa4146dbea665632c44a7a14d7742638fe`  
		Last Modified: Tue, 13 Oct 2020 01:14:48 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:8275b9aefc3d02676990c7a9595f2237c4c5d31ec51b84b073cc568e19439a1b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.8 MB (55774734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48a6eb34676370e84fe55d46406921708f8968df3a918c887c7f06b5bd850d52`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 10 Sep 2020 00:54:23 GMT
ADD file:4529de4df0d9d1d1c2fc4ea683021e7ff678a24ca45c21d9dfaeb7c4dc1da51f in / 
# Thu, 10 Sep 2020 00:54:39 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 00:55:19 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:6146fe38f8409e50a43aec229f36623c0f8c195d2cdf9bad02573a9d952a31a1`  
		Last Modified: Thu, 10 Sep 2020 01:23:23 GMT  
		Size: 55.8 MB (55774504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a01b09bd366af03f367224e2c042476b80aa937460432db6e5b7f58ae45bc346`  
		Last Modified: Thu, 10 Sep 2020 01:23:35 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; s390x

```console
$ docker pull debian@sha256:d8aab12a3ce1602a90f62016cf9b3deab2931df85e1368f2b6d6118ba566207d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51118950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac6c1fe16a5939a7973963c8476a3952318819d9005fe8d333c9f1265145fddd`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Oct 2020 01:41:35 GMT
ADD file:1952263a13d56f052b56241e876c31bad8764b58e4a2c516a99d4f39950caf39 in / 
# Tue, 13 Oct 2020 01:41:37 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 01:41:43 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:cf0128f5938d0a765169c542feff60f3c439d59fb9c4be101b86202a01e6f72d`  
		Last Modified: Tue, 13 Oct 2020 01:45:00 GMT  
		Size: 51.1 MB (51118723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:216b165b42c799e02a93430bd3f8d9149b73d75db94235ead10831da902df19b`  
		Last Modified: Tue, 13 Oct 2020 01:45:08 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
