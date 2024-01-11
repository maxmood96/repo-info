## `debian:oldoldstable-backports`

```console
$ docker pull debian@sha256:3cd7ac32afe9ddd3dd4a3a9a2ee76781546b18daa24909863d4e6eb32d5355c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `debian:oldoldstable-backports` - linux; amd64

```console
$ docker pull debian@sha256:8c91e37c767dcf266da69afd16733284bc823d31a26ac97c933b7ae66cd24113
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50500478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d60efcddbbd62082f1e361b5dfb31a9ac5e56e07b7ff4eae2d4776ff1b2f9561`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:49 GMT
ADD file:581e147bf583aeadae2072e6ee1f54513914693c26d735a9bb7e6c793b8226de in / 
# Thu, 11 Jan 2024 02:38:50 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 02:38:54 GMT
RUN echo 'deb http://deb.debian.org/debian oldoldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:e2940dd5f07fdef73873c4b3e8db46b840fab9d53fa7676371776881eb432ad0`  
		Last Modified: Thu, 11 Jan 2024 02:44:07 GMT  
		Size: 50.5 MB (50500249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a9d894c9960b70ec56d0e5219bef4041ec279c81e53673aa4c27aa709a3d9d9`  
		Last Modified: Thu, 11 Jan 2024 02:44:15 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldoldstable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:8f5eed93aace9423e5823b60b02337d49e368ea1a756d81dda934fdb501bc485
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (45967848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4a64f8201d171fb11755c7ae91fd224db7d473ab9ff23d06a56edd987090254`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:43:21 GMT
ADD file:17784553a5c416b721259316b62c32720e638edfce9c66148e495439ddfa79d2 in / 
# Thu, 11 Jan 2024 02:43:22 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 02:43:27 GMT
RUN echo 'deb http://deb.debian.org/debian oldoldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:8789fe271e1c8f69e1ab39dadd8138a896dc6c7b1962d2aaf3a1cf70b24a26d3`  
		Last Modified: Thu, 11 Jan 2024 02:50:30 GMT  
		Size: 46.0 MB (45967620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d903c2b2f69462f975df020676b6d42b5b1e005bf26656a575359367797820ee`  
		Last Modified: Thu, 11 Jan 2024 02:50:40 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldoldstable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:4e79d90a44194e3300b4ca897a5d1dc817b53bb17beccdf0de336a080a319404
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49289072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bc257d1e766bebf46a3272f9a77b9c5144003725a819458e92ce0e47d354274`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:41:20 GMT
ADD file:2bde5ae81add5f828a0e079f7895878d4ec9a13a8d5466882456a51d9408cc87 in / 
# Thu, 11 Jan 2024 02:41:21 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 02:41:23 GMT
RUN echo 'deb http://deb.debian.org/debian oldoldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:28d879fd2b97bec8017445268bbf78a54ae960a60073652c382f4ff9085356de`  
		Last Modified: Thu, 11 Jan 2024 02:45:40 GMT  
		Size: 49.3 MB (49288847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c36cea79b9250f04d53b02f788f6bbc32b64bfe7cdc07f7062d94ada692d3cc0`  
		Last Modified: Thu, 11 Jan 2024 02:45:49 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldoldstable-backports` - linux; 386

```console
$ docker pull debian@sha256:d0c560bafdbf657c1c3b8e00e838428ea6e6df1d40a2646842627f0ba33073fe
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.3 MB (51255466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac861223904d6251e44f496b3d561a20202af033690b358f56d20c6db0821725`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:39:33 GMT
ADD file:f6e65ca07b661c414b14f9c2232b39a1372e15b16ab44e901adf632fe3c19340 in / 
# Thu, 11 Jan 2024 02:39:34 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 02:39:38 GMT
RUN echo 'deb http://deb.debian.org/debian oldoldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:215e009d09e2a9b0f6e04f24b79e9e76c5e15200b9b8c01db4b29aa98b82643f`  
		Last Modified: Thu, 11 Jan 2024 02:45:17 GMT  
		Size: 51.3 MB (51255240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d49387fced6345892f5210dde3712d0fb2b6b240e2b5bd0761679b80c415ea9c`  
		Last Modified: Thu, 11 Jan 2024 02:45:26 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
