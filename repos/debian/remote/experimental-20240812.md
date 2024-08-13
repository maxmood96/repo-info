## `debian:experimental-20240812`

```console
$ docker pull debian@sha256:bc8150ab171b2afe1a3d6250fea6786487a7354c5ed4ea545c97abcd6b87e449
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; riscv64

### `debian:experimental-20240812` - linux; riscv64

```console
$ docker pull debian@sha256:f2a15f24ca138ae9a5d06863270de6018c25f04ee4ff29dc54060fd1312dda2d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51106348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afe0fde3e4b3019a5e372d9b92b398da5d8c8eb9e1b848f45c72a5c1d324edfe`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:14:29 GMT
ADD file:64a9e7a1acff8052c3bab28245f16e447b984e8538a4369f6edd9856e45a4472 in / 
# Tue, 13 Aug 2024 00:14:31 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 00:15:05 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:f6e6770d8a1e53c60789615dd085dafe5a0f12f2390d47a1a970a0443f54e391`  
		Last Modified: Tue, 13 Aug 2024 00:20:16 GMT  
		Size: 51.1 MB (51106125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e396fedada7d4e6fcda4b237be3e919424272bbc41e0721b44ed7be204e9757b`  
		Last Modified: Tue, 13 Aug 2024 00:20:56 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
