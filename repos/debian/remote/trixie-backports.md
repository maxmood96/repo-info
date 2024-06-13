## `debian:trixie-backports`

```console
$ docker pull debian@sha256:6c0073dd1d05678bc5f896768085016077f1577b03f2877e685bb56afeb37962
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

### `debian:trixie-backports` - linux; amd64

```console
$ docker pull debian@sha256:581b44645604f916d48c439eece9d253aaec112d76ff455a0ebef06b82d2a974
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52277986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:904bd675d95580f3a536bde25940f2d07cd59303062cbb8ac609e610fba18385`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 01:23:33 GMT
ADD file:fb6f38952a56f7cbaa95d8ba94e80e8248829fe8e6ea398f1cbcb89942bd1547 in / 
# Thu, 13 Jun 2024 01:23:34 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:23:38 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:e1794c1f4707f1bb7231b64706e50d1615843d67660a3142771596a820e257b8`  
		Last Modified: Thu, 13 Jun 2024 01:29:39 GMT  
		Size: 52.3 MB (52277762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:558367f762493b6467beac3d043ada333067688a77ef29c0f1aa1fd08f6457fa`  
		Last Modified: Thu, 13 Jun 2024 01:29:47 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:trixie-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:533a79afb8654af8a8334f671a9dc5dec52d29f230b34cc36113dad88158c695
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49352646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33f4e1504ada56cc0d573450466bef25f00d0cc9a24140c8eac5561b29938d9b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:49:58 GMT
ADD file:67cf4d8ec08d8be721c8b3c00d573d157c1ced0941182f1bc4963de79d90968e in / 
# Thu, 13 Jun 2024 00:49:59 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 00:50:02 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:29844d0657d8dd02a9b897db6c4c33e6651c566ad1edc4743031852caa791e09`  
		Last Modified: Thu, 13 Jun 2024 00:54:51 GMT  
		Size: 49.4 MB (49352422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e4b31b1197bea04a486e19ffbca034c1ce1be6b6c7e6ab4a42f1f0bcd76832f`  
		Last Modified: Thu, 13 Jun 2024 00:54:59 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:trixie-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:45b666e0ef6406d1833ca62e0fe566ec8e356ffcba2aa32216f173103c693d52
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46856405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48eaefef7eab9f12c467f8a31275e31e997b4ff246e535c0626fdbd33c2eb8a8`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:59:47 GMT
ADD file:d796d27ece53d8f1990a8b90cf835997d1cb9520f76b3476f3fb834465a282f4 in / 
# Thu, 13 Jun 2024 00:59:48 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 00:59:51 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:16fb7fece780cd7b9bbf82b2be73b9d8d6a4780cdebb977a5f734fcc541dae72`  
		Last Modified: Thu, 13 Jun 2024 01:05:53 GMT  
		Size: 46.9 MB (46856182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39447d500309d319163e714858da736360e735c13fd5e4b4e71a0b2e031c6260`  
		Last Modified: Thu, 13 Jun 2024 01:06:01 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:trixie-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:4b27f20934af29507df8bbe7863b4aa349e77b152ceb3d0b49fe6a18c11749c6
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.5 MB (52514603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb382a56796c4e673d2c5a5eb83fdf1bf894b0cd5c2d7d6eb9272b8c870ea90d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:41:36 GMT
ADD file:c7b7f4f414b176b634ecfd58cd24ff7ad3d2b36f1fefaf2139e52ba8948ce751 in / 
# Thu, 13 Jun 2024 00:41:36 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 00:41:39 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:f5ff74329e5ae53cf8fd13f7790e7a8ad37f71aeaaf9d356f6e2d2b40673d16d`  
		Last Modified: Thu, 13 Jun 2024 00:47:05 GMT  
		Size: 52.5 MB (52514381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a96d6ed97da3f5bd95d71c664357d855b3fb05738e6704bfb93aeefbfe163015`  
		Last Modified: Thu, 13 Jun 2024 00:47:13 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:trixie-backports` - linux; 386

```console
$ docker pull debian@sha256:bb11d2aa652a10a400b360911304216837428c17146dfef91ee4e289e215cdeb
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.1 MB (53147688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8f1f30dc7bfb8dcba83ee118fbe1cc8c8a7b7468ee67fcc74d71607eae61882`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:41:32 GMT
ADD file:de9bc4e6489e3b2b2a8a1580ca8e391816a25c5cc50d80300c6624a24c656187 in / 
# Thu, 13 Jun 2024 00:41:33 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 00:41:37 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:c13178907b62803a756f9dd247be54c121b0e86bd70c25c38ec3ad97e2a3f6ed`  
		Last Modified: Thu, 13 Jun 2024 00:47:56 GMT  
		Size: 53.1 MB (53147470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de28e38dc0a6d2bb247701d594a95244e2455c9f7657ff679f1c033e4a5b6596`  
		Last Modified: Thu, 13 Jun 2024 00:48:04 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:trixie-backports` - linux; mips64le

```console
$ docker pull debian@sha256:1af7cda1dcd47a644de2d976cc75399f1a59dfde95c7a3f684761a38a4308100
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51137487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a5863dbd87ef93aa58e95ef884077eed8fe8ca1e80f7f4e0d506823c757aa41`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 01:17:26 GMT
ADD file:4f8e64cb73f0bac5394470bb779521bb9b544dd7513205d8a870b13ebce84cf0 in / 
# Thu, 13 Jun 2024 01:17:33 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:17:47 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:82cf140ea060591c60ad59c1c2af2452121c8cf77b184829ed04be1d69b176dd`  
		Last Modified: Thu, 13 Jun 2024 01:29:05 GMT  
		Size: 51.1 MB (51137261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eda84962dbd94609ae191a57f98b515216bd95fe141ab00bc273c7e4688aafa`  
		Last Modified: Thu, 13 Jun 2024 01:29:15 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:trixie-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:f68b3e36d47d63e60ae89b7dee9ae3c2ec517e6c99dcbc8559aa0a335ff91087
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.1 MB (56146741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc9c6e6a5fe15712fe2a61a4ae70bf7260c4ed9146b2f3e3739e1dfc3812a950`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 01:19:22 GMT
ADD file:7f11aeb3b831c3c6b30678c3d7984daa533d1db8a095121fa83cd6eccfd45947 in / 
# Thu, 13 Jun 2024 01:19:25 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:19:30 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:c454865e432a2e42969df66627ee25256e1007a229199ac385d2d91b138f54b7`  
		Last Modified: Thu, 13 Jun 2024 01:25:21 GMT  
		Size: 56.1 MB (56146517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd68cee396e047e32c98f5f0ad307216ba192183aac8f024e81d4a9393f5f018`  
		Last Modified: Thu, 13 Jun 2024 01:25:29 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:trixie-backports` - linux; s390x

```console
$ docker pull debian@sha256:496b26dd16523c8d22e594ace7f8e5dccd50e5c1e2b4390e6679705ecafea4b2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.9 MB (51895557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef236cdff90024b62a003aae9a34e18cdafc050137163078b525b756f852c6ca`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:45:25 GMT
ADD file:1021b70eed1c798afb52193fbb22f6cde06dc4de4ba0e601974f25a3ba8db833 in / 
# Thu, 13 Jun 2024 00:45:27 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 00:45:34 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:9bf5f2c747732ad70198f12b8184edafc2dc0d62b3b69d1720a7860e85d2991a`  
		Last Modified: Thu, 13 Jun 2024 00:50:09 GMT  
		Size: 51.9 MB (51895333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0113bd4e46ed2fba0a50c9557be3e23f9ee69d3b48b202b018482f88ad423f8`  
		Last Modified: Thu, 13 Jun 2024 00:50:15 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
