## `debian:oldstable-backports`

```console
$ docker pull debian@sha256:3511b521539d2fee7b325ef5752bb8991b4a78151864f52b7baee4bc764191d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `debian:oldstable-backports` - linux; amd64

```console
$ docker pull debian@sha256:72f92eecf81ae4c9d2c5f5bd0b7aa8dc5850701d2dea2d40150c61389d19a17e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.1 MB (55081632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d205b946a3a93480aadeeed34961a8f933b794f45336bdd6e7d3465d13d61bc2`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 04:30:05 GMT
ADD file:9702ad73a9bdf05a3bfb1fdf00f4add7fe7d6423d816ea5736dc09c38571271e in / 
# Fri, 27 Sep 2024 04:30:06 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 04:30:10 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:1f25ed91b431651611133faee8034e0ff11333b8a3908f9c394e5eb7238a5d39`  
		Last Modified: Fri, 27 Sep 2024 04:34:07 GMT  
		Size: 55.1 MB (55081407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6577420bff5c6a4799ad60fabd1f888d644fb973c7bad7264aa062d8eb121b2`  
		Last Modified: Fri, 27 Sep 2024 04:34:14 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:6e02d255907cd2aa796cb52c794e3d22cae656e4239061a674324653ff5e5f51
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 MB (50240491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55649b38f1653b909ac2e93b334b36039ed0c39ba51eb6ba2c29c721f34f95e1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:58:38 GMT
ADD file:1491f8eddfc713dac57f3c08caaf2ad833f4185044b61395ba260517a39cb5ba in / 
# Wed, 04 Sep 2024 21:58:39 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 21:58:42 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:0ad03ef6392933717d8aaa8084ca76329c1b63498bd61f17227357b08afbf819`  
		Last Modified: Wed, 04 Sep 2024 22:02:46 GMT  
		Size: 50.2 MB (50240265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3f00c05b05d67c46d071ecd7a483ff06441d48d4434fc32975f353e75d2f5d5`  
		Last Modified: Wed, 04 Sep 2024 22:02:53 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:4efa10feb56f76b32217bff214d705f2ca91a78e04b651e4c2d560529302b50b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53734068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaceb8d2077aa0611b7404ba0e8bf0724242a0fa73e6ba48c0e245883947ab6f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:39 GMT
ADD file:dbceb67a4459d0f5870a40e38032da74fb1fd32243f3301f930ad8775661d894 in / 
# Fri, 27 Sep 2024 04:38:40 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 04:38:42 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:423f448f6c5029ccef4300fc9d14c8304a116615c4b5daf9470abe27f958cdab`  
		Last Modified: Fri, 27 Sep 2024 04:41:43 GMT  
		Size: 53.7 MB (53733847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c107c797ae49b0c9fd8478156100a74a82d035616f55af91fc5faca566522f44`  
		Last Modified: Fri, 27 Sep 2024 04:41:51 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; 386

```console
$ docker pull debian@sha256:994841a528e91a7d0551e6bc0d933b8c20cb46691d94f28e349a29c8b102775c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.1 MB (56076372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef12386d05d53c44368fb918eb9be3a53f69609903606856a3f1fd113189cf9b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:45:06 GMT
ADD file:80987a1bc79cda72954e1a362e5bab721a49cb043c31d7a5e0a0f6ef7724047a in / 
# Wed, 04 Sep 2024 22:45:07 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:45:11 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:ddc3d843871f2ff4e892fa6a6c6e548fa150061d0f837c1e78195357bf15944b`  
		Last Modified: Wed, 04 Sep 2024 22:49:11 GMT  
		Size: 56.1 MB (56076147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:081f84e18f70edf646620793f4ef38903896430bfe0b1cd5b968bd1eba92b234`  
		Last Modified: Wed, 04 Sep 2024 22:49:18 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
