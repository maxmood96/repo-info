## `debian:experimental-20241016`

```console
$ docker pull debian@sha256:afe20874fad3ea700566f2bb1d4195798ad6ae50c59ab267c0406cd985cc6980
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; 386

### `debian:experimental-20241016` - linux; amd64

```console
$ docker pull debian@sha256:15258696b8fef401644241a42ab606b93e8b85910d83f8d5823828596ed28621
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53272098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:322e1de3d0c0c606b0b7f8747db2cd43ad36b6ac297e35274a49daf214a62232`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 00:22:45 GMT
ADD file:344a17234e227a6dfa7b04784891c1537d678103d91d40841996e0355c691cd7 in / 
# Thu, 17 Oct 2024 00:22:45 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 00:22:57 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:8158e735f4852d21000cf76f6872a1dc489fc2e307ba70c037a21e8a9b26a9bb`  
		Last Modified: Thu, 17 Oct 2024 00:27:25 GMT  
		Size: 53.3 MB (53271880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efff54737272af3f5af9d53ac46d031426fc2dc97bf383061907271f36468053`  
		Last Modified: Thu, 17 Oct 2024 00:27:44 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental-20241016` - linux; arm variant v5

```console
$ docker pull debian@sha256:9882549b0774f07d73fd59e753768b33591285258fe531dbf6b0bff63d147646
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50147816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:946ae543859ea5651ae6a4567aac099f5b5db3663bf9d303bd9c4f7622019d71`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 00:56:16 GMT
ADD file:554322c0ec63d40c650e4a8fe2d49f827ed18c023a8362874dc4d169f68d91ae in / 
# Thu, 17 Oct 2024 00:56:18 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 00:56:30 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:859c2459faa82042e0d9d83a9a47b8a82df9185d1986dffd244e0b4a254e6169`  
		Last Modified: Thu, 17 Oct 2024 01:00:02 GMT  
		Size: 50.1 MB (50147597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a89af18f0c0edb22dceedb41b430e1bcfa23d0de14454a5e69bd3614f019be8`  
		Last Modified: Thu, 17 Oct 2024 01:00:25 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental-20241016` - linux; 386

```console
$ docker pull debian@sha256:1b18c1c1397ef00d72d84511108a342252f0644a32e92cbafdf7aac6dccfa6dc
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.1 MB (54118201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d4d25dad58fd6edf85fbd4880d60bd5b9652368bfd71218d2dbf697320ea0a8`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 00:41:17 GMT
ADD file:aa65c5e8505403221c9db052fbc81b96cd9afc8ee1534405a8a50005a73b98d3 in / 
# Thu, 17 Oct 2024 00:41:18 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 00:41:30 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:6fef21ff2cdae44e0d2057631ea5ea8ffb7f4f1057257e79ba71fe18c37d566e`  
		Last Modified: Thu, 17 Oct 2024 00:46:29 GMT  
		Size: 54.1 MB (54117984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa68d6988dc64883000bdff187324c6259207c07ea24e014c1749cf9eed74220`  
		Last Modified: Thu, 17 Oct 2024 00:46:51 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
