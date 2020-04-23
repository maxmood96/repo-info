## `debian:experimental`

```console
$ docker pull debian@sha256:fe184c51b8144ca0c5ae1053c07e38c443e0299234b4e064fdecbe0c9ef15696
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

### `debian:experimental` - linux; amd64

```console
$ docker pull debian@sha256:22585778342597709836b5e03fca3e64cdc602d0204b8d6dfbcf15d2145e8dd9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.0 MB (51979935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:598a0c29c569fde1a99fe781d590d72db5706b51d8f510431849666ef988c9be`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:23:42 GMT
ADD file:6ee109aa41831586899e9a04462a7c3a57fe9b599a263fb0ed2fc3ba1ed57b9b in / 
# Thu, 23 Apr 2020 00:23:43 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 00:23:58 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:1411ff81de269e0758691342315f4c16f9a93db2b77b392e2e3fc3f3ba93b2f1`  
		Last Modified: Thu, 23 Apr 2020 00:28:27 GMT  
		Size: 52.0 MB (51979713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f31581696a65b3d4173140a5bb8db1d74ed3c22a7c834e1eb8b8f4d19dc60ab`  
		Last Modified: Thu, 23 Apr 2020 00:28:40 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; arm variant v5

```console
$ docker pull debian@sha256:54fb39d322972638dd9552f23376feaeec1a4604b158844371774125689ccca2
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.9 MB (49937946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:754d03e4924ad139350f9bbc62e9c109d6dd77fdbdc031d91eab9ba0b4ee0b72`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:57:16 GMT
ADD file:344dfbe772d659e7f36c6e2f9116eed46e7fe1242882a7fb2264686b7db7a043 in / 
# Thu, 23 Apr 2020 00:57:18 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 00:57:41 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:7a7799c9a71deef56beed269fd45a7dc5f11faa42251a24e191e7979161b16b3`  
		Last Modified: Thu, 23 Apr 2020 01:04:52 GMT  
		Size: 49.9 MB (49937721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2f6131f002a16b4d2ed7bdbf980ca21b543e6fec52622c29f60a660c4b532ac`  
		Last Modified: Thu, 23 Apr 2020 01:05:13 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; arm variant v7

```console
$ docker pull debian@sha256:ca38fde2cb27874b193d3d873cb627ea826d174cce0d9ba9ab2b30d22db7472e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47659294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a77d9f7f244f0e83dd1c4d03863b0ddfd668a9064447dc4c6d3940f30581b6a6`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 01:08:42 GMT
ADD file:1c27d249bca87f83ea15214c872a24bd113e48209c08cac9e58d2617d16ed14b in / 
# Thu, 23 Apr 2020 01:08:45 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:09:13 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:968cb96b15219e43c5154c4ed291ed115d2b76c305ca949ea322d2c7c0b857fd`  
		Last Modified: Thu, 23 Apr 2020 01:15:38 GMT  
		Size: 47.7 MB (47659069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:948a9b5cb12051f05545690a975f8dd49bbf524e91a403132e27b952f73ca985`  
		Last Modified: Thu, 23 Apr 2020 01:15:57 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:14d8dbf0cf28e9f13989d0e36bad6c2981d33ef5e343e7996707086b6d14751b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50909332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf9b16b04763bdda359d9a0a1d2de536328e6336b08d6b7aa6f2a9ff8024574c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 01:00:35 GMT
ADD file:73c6e4d709b4c6fabe9152f6b7fe35571630578d5a1fa9d7c475f789732f0aa0 in / 
# Thu, 23 Apr 2020 01:00:39 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:01:23 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:d0a61e2b658180eb67795006d401e97e9c4a9399d3a478970fdbcfaad9bb4e8c`  
		Last Modified: Thu, 23 Apr 2020 01:07:11 GMT  
		Size: 50.9 MB (50909107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7d8a5716081bee935b30fb4dabf749d09f7d1a2fc5d4fcd16f5dcfb763c1ec6`  
		Last Modified: Thu, 23 Apr 2020 01:07:33 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; 386

```console
$ docker pull debian@sha256:869b054be7d001857ecdad8f97673228a71efbcabf8e8d598336720272a7ed1b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.1 MB (53123934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9822202228ca7c667ce8f0631b1f005460b34212e0e292884ccc74a6e70c8043`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:42:55 GMT
ADD file:1175e5211df616c0061144ef189e0e4972721e25de7304d81f14126234b4bcec in / 
# Thu, 23 Apr 2020 00:42:55 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 00:43:11 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:1831d7d095361283b5fc12083dd3b6702748739d46bc96b030aadf6dfb65f769`  
		Last Modified: Thu, 23 Apr 2020 00:48:31 GMT  
		Size: 53.1 MB (53123709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5550f45d064b7dce5076b86de7c11b525f0ebad9481b0c136a4412e7ddaf8ee5`  
		Last Modified: Thu, 23 Apr 2020 00:48:49 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; mips64le

```console
$ docker pull debian@sha256:2c5ff7c29542ee3bd0bb1957764f633b50ad05898e1cac66f36f4d4b687a30c9
```

-	Docker Version: 19.03.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.7 MB (50696359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c04cd5f22a1eaf19f4ead327fbb4bb4c70d6aa23248725359498c5b8e1660c59`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:14:06 GMT
ADD file:f4f731cdf85bc353f740a040496bad65f39a579c6a7ee34955a69c0e09ea983b in / 
# Thu, 23 Apr 2020 00:14:07 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 00:14:31 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:5cd8c4531ac615911882437b1e6150cbdcaee37eb6cd1a20c0178acd6b29ab6e`  
		Last Modified: Thu, 23 Apr 2020 00:25:33 GMT  
		Size: 50.7 MB (50696136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c13a62aa1f5581f14603946532b9f2ef19ebd8d7536234a2c46950aa957a52b0`  
		Last Modified: Thu, 23 Apr 2020 00:26:15 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; ppc64le

```console
$ docker pull debian@sha256:bfec9d2cf27a3dd1cf48a1ee0d38ab8cf6fa95d11d19bf8d42449f574c07e478
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.9 MB (55855703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2eec65390779f8c845d72600d0525dea4028ba0f2420d5b666b9f05407d692e3`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:45:29 GMT
ADD file:88b56ec49dda47a2ab6e0472bfe15d92ddd0416de0756a7487af9ebdadc304c5 in / 
# Thu, 23 Apr 2020 00:45:33 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 00:46:50 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:7e5405fcb9ad38fb28c749ae22e37e07987237ad6e83c59a65f1b9dd32be46a0`  
		Last Modified: Thu, 23 Apr 2020 00:57:23 GMT  
		Size: 55.9 MB (55855479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9dd0c2e7f8795828ff95b02faf8a5e43bf2c461bfed3584d083eee0980cede3`  
		Last Modified: Thu, 23 Apr 2020 00:58:03 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; s390x

```console
$ docker pull debian@sha256:3e0e32b8091b24befbc9f1cea39f65cbb4faf5552799006587f42e5eb951bb66
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50581503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e442ef05bf7120286f53cd7b7f54142dfd5a145eea8597608aef9c08ad19f5d0`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:54:28 GMT
ADD file:a9556113774030bc14c004293576b34bdea9ca5fb01feb6753155b9d6f893ab2 in / 
# Thu, 23 Apr 2020 00:54:32 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 00:54:51 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:58ea4c36b8c8b892c10b861354c144856390a600b724cd897da04d259a6ca1f0`  
		Last Modified: Thu, 23 Apr 2020 00:58:13 GMT  
		Size: 50.6 MB (50581281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4443edaad0e2adf97112428ee8420b691b342ac5648aaa6c6e092c12699fd50`  
		Last Modified: Thu, 23 Apr 2020 00:58:27 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
