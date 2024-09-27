## `debian:experimental-20240926`

```console
$ docker pull debian@sha256:ef544964773fba348619a179168c993be1ae1a6b0cff8ac9c5192c7c74675b0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
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

### `debian:experimental-20240926` - linux; arm variant v7

```console
$ docker pull debian@sha256:4a9040e58fbcccee1a0e92e07403eb853a97bf6dd9f448a6081f0fd20e8bc926
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47657086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39b5020334864bc5e7cd57e484028d93ed3e85897a318438d7a3dbaf830cd8c4`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 05:16:05 GMT
ADD file:ee2f1ffef76f355c1bc3786a4cd225246fb084deb46f8f7a0ebb50e0a39678f9 in / 
# Fri, 27 Sep 2024 05:16:05 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:16:16 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:622ffd55c3dbb74d17226398ebea86b658a64d0757e987c80a410d1daf7a4e86`  
		Last Modified: Fri, 27 Sep 2024 05:20:33 GMT  
		Size: 47.7 MB (47656866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c8cebc5d402e1185423a7b7204f5c06361024d2fa0f715e91d2c98b3cbad64e`  
		Last Modified: Fri, 27 Sep 2024 05:20:55 GMT  
		Size: 220.0 B  
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

### `debian:experimental-20240926` - linux; 386

```console
$ docker pull debian@sha256:3e689803ad69a593c551d1b56fe1eb1d68bc75790fb0e5bbb48cec2dbe31fbaf
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.1 MB (54078030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a0b1a38252df815ea2501fb8750235c3c36f86df5e7decb2ca723e768cf6dc7`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 07:25:29 GMT
ADD file:a528ba393860cdb127144bcf9dcc31d316a4af0fc0b25383f3dd11fd6581b908 in / 
# Fri, 27 Sep 2024 07:25:30 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 07:25:43 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:5b33ac5a9c31ec0b63e2208b52ec1fec42050ae282a115b73e2969f91d7debea`  
		Last Modified: Fri, 27 Sep 2024 07:31:05 GMT  
		Size: 54.1 MB (54077808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f26fdb97184a2a15e2317368b8bad489279dc24d08a0a2ef5e52a7ce387d8a92`  
		Last Modified: Fri, 27 Sep 2024 07:31:27 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental-20240926` - linux; ppc64le

```console
$ docker pull debian@sha256:1ae383f1b02ef017574ee64c521036bb918c6459138407b424229e64b3fbe89c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.1 MB (57123375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:878799a1f03ad719b4df114e9511dfdf2b16696ba3537efcc59fa5593ebde099`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 05:35:01 GMT
ADD file:2eed4107bf1f631a87c3f0ff4c7b82f747d5a594d8c9fe2fa4067f4e2a826e14 in / 
# Fri, 27 Sep 2024 05:35:04 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:35:20 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:256e99e676463da71c3f5fdc7aca05ec4eaffbb4baa444cd2609b955d401b342`  
		Last Modified: Fri, 27 Sep 2024 05:38:57 GMT  
		Size: 57.1 MB (57123152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f7da5e6e8ea65b11e231f56c0137399b76cb381f11d510c7dfc94fd6092abcd`  
		Last Modified: Fri, 27 Sep 2024 05:39:19 GMT  
		Size: 223.0 B  
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
