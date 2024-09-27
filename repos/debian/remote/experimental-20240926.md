## `debian:experimental-20240926`

```console
$ docker pull debian@sha256:1febe3c43a2fd775457c4d1e0677b8b5e456071ca543e57083ad1c62c20b5778
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; arm variant v5
	-	linux; s390x

### `debian:experimental-20240926` - linux; arm variant v5

```console
$ docker pull debian@sha256:c39647f4dc8dfc4f572d731cc8c58379da8cf124f4861477354481071e7fbaaf
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50141380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:653f019711f56657b39aca10f8e743e7738d1e57507fe0b5c3f85867e0ae3d1c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 03:20:40 GMT
ADD file:b26a61b8e7db76219af21581be9afbb06fee5e29051cdf3c47c8096bb2c4ac54 in / 
# Fri, 27 Sep 2024 03:20:41 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 03:20:51 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:dcf3e23fd72d511560b1be1a67624efab694e53d2487e00b4b4c031fde6efa3d`  
		Last Modified: Fri, 27 Sep 2024 03:24:07 GMT  
		Size: 50.1 MB (50141161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:622bb3a8e3cbb4adb647a3ba31ac73ed82bc871eab13c7fc03993249858d6dc2`  
		Last Modified: Fri, 27 Sep 2024 03:24:26 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental-20240926` - linux; s390x

```console
$ docker pull debian@sha256:7cf547eb9bfe7b1b9ade0f03abd7b25b40cc04864234d89b8f3d8b527c13c05d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.8 MB (52808359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c81412ff602f20c4f08341254546635d424e4adee1f89b42e710e0486d87ee6`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 02:45:56 GMT
ADD file:20427de214380a70658eb94ab60555c5a52f911b8a3754bfd34eae3a7387726c in / 
# Fri, 27 Sep 2024 02:45:58 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 02:46:17 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:bc3c84d7eec1449ed3e2007e849d064645c2eca9cfc41327102553e89c550f44`  
		Last Modified: Fri, 27 Sep 2024 02:49:16 GMT  
		Size: 52.8 MB (52808139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9712c795678d33d454dbba4df63f8d0417259f8181e963851ef44b36ab63b1f8`  
		Last Modified: Fri, 27 Sep 2024 02:49:31 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
