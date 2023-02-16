## `amazonlinux:with-sources`

```console
$ docker pull amazonlinux@sha256:d84ca9fbf5d90070f2ebd369f57c1bd3aa40de27d82b2bf6d4da25f501ffef0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:2d38587453f08b16b63169a66451ee34d0934db2399ee95c2614e86a5a7dae1b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **492.5 MB (492531606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad43da7b8649e85abd2f228c42dfa04e55336f23d3af0f78794e4307de8d545f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 22:20:04 GMT
ADD file:6ebab25a4f1aa82238dbf1a48f38d22c6421052d0d158cf88cbc1a4d01b5c5c1 in / 
# Thu, 26 Jan 2023 22:20:04 GMT
CMD ["/bin/bash"]
# Thu, 26 Jan 2023 22:20:30 GMT
RUN mkdir /usr/src/srpm     && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-5f290fbb01ed6cae6ec9436094897096f0cd61aa0fb90afb412045f989363faa.tar.gz"     && echo "a2345704122103f0cf035d1ae3d4fa863db8c73c0f08e6f8656f5ac9274b0eba  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:1e78b99dd1fd1031c6513834c4b5f594fa3cec5d06cdeb4b65ee104180bc0d4c`  
		Last Modified: Thu, 26 Jan 2023 20:44:53 GMT  
		Size: 62.3 MB (62341068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb9c62719ce9a736ff6f49a8d84be8316820a6035ab43ac69eaafb9ec7975bcd`  
		Last Modified: Thu, 26 Jan 2023 22:21:33 GMT  
		Size: 430.2 MB (430190538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:with-sources` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:ba3f1afa6fa0103b96d2c2d4a70a860e5e21426cc566d1fba15be4558808f5b9
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **494.4 MB (494350183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41b75bcfc11d633380eb8a00eaa5fbd5672efa3107a1d65f850b71dfea70bf46`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 16 Feb 2023 20:39:31 GMT
ADD file:17574026c2754afa903450c59a6d8f7d0905209b174cbe9c13252a61d5a6f916 in / 
# Thu, 16 Feb 2023 20:39:31 GMT
CMD ["/bin/bash"]
# Thu, 16 Feb 2023 20:39:53 GMT
RUN mkdir /usr/src/srpm     && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-7e289542d782642b256d8350ebcc22b568c00303c6cedda53c0cc26f5de6cca4.tar.gz"     && echo "28173c8559de7e4838d9ae0e1c163243d6d1274f28d242ced6e7fa44272b36bb  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:71343c2791199c6e2c19c308cff6493497a02f57e225c11405e1934dc7428b3c`  
		Last Modified: Wed, 15 Feb 2023 03:16:17 GMT  
		Size: 64.0 MB (64003805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b64a7d1a6cba2e41239f96a04c0f08457a2254983add1e7c6f48ed5668abad4b`  
		Last Modified: Thu, 16 Feb 2023 20:40:47 GMT  
		Size: 430.3 MB (430346378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
