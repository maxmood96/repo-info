## `debian:experimental-20240926`

```console
$ docker pull debian@sha256:0d0f9e1676d12e0b45f35152f65f5862208a870abfa1e88148126507fb843c99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm64 variant v8
	-	linux; s390x

### `debian:experimental-20240926` - linux; amd64

```console
$ docker pull debian@sha256:80c62a0c55a91d7e7a8e99f045c154463296f8713388f10cfde4d7649d2e3980
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53250243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3624d22ed208bd81b785b10928bf110a2243baa5af1b7a6006c64c30a688248`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 04:31:57 GMT
ADD file:c62a9730747ddafd9396dd56054876bb04694cd6c405069f37e76f34e85661f5 in / 
# Fri, 27 Sep 2024 04:31:57 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 04:32:10 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:97d7e22c4c55866c728f706982a641627a33b27bd4385a3738894f213919fb7b`  
		Last Modified: Fri, 27 Sep 2024 04:36:32 GMT  
		Size: 53.3 MB (53250025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecb30da4964c76c2f51d6aae2e2e1919fe1fd6dc88eac8107ea5a02fe2394129`  
		Last Modified: Fri, 27 Sep 2024 04:36:52 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

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

### `debian:experimental-20240926` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:8d61bae67a417195f375b1cf72ebf8b830d9ca83aed18574fa021ab98bb5f453
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 MB (53594466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4800ac03f1533bf0ce650216e23d4954937e0e4aa6fb0db0f91b29e6e071cad8`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 04:39:52 GMT
ADD file:e014c06e0ee28a401f9a8a62b2b8a815ba9afafec7c84eb6b0795de0946fb7e9 in / 
# Fri, 27 Sep 2024 04:39:53 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 04:40:01 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:a5d67d16dc00ba13dab5a84610c9eaab11745150f644c09325e9e8b822fcea80`  
		Last Modified: Fri, 27 Sep 2024 04:44:00 GMT  
		Size: 53.6 MB (53594246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35ef1ab33c686b5598c5cf2d9fce64c8d0d6bd9a43d671c0a0350a476b04875b`  
		Last Modified: Fri, 27 Sep 2024 04:44:18 GMT  
		Size: 220.0 B  
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
