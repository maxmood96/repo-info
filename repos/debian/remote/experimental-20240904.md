## `debian:experimental-20240904`

```console
$ docker pull debian@sha256:e566034407acdaaaf187bbd4fd40108a985a4d6debd9cd6279004895e9954e79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; mips64le
	-	linux; s390x

### `debian:experimental-20240904` - linux; arm variant v5

```console
$ docker pull debian@sha256:3219adcc5d1030d6fb5f90278ca6d63c421ce716ba3b54012b9c617e145b51a0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50112637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7422a850addc21988195516806b08b20c8a49e1b98bc3a4a8d3e3cd3b764bf6f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:50:15 GMT
ADD file:035cc76743532187e73d879925a708b94f4d30d4443fb9f56466a3e28d4b49a5 in / 
# Wed, 04 Sep 2024 21:50:16 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 21:50:25 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:53016ff6120a902ca592b9aade494e94d68b1d815e958dbcb1c159e6dd4186a4`  
		Last Modified: Wed, 04 Sep 2024 21:55:10 GMT  
		Size: 50.1 MB (50112418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25667b1c97c7614fb2269be1ee5c562e09c3334d42de7d949a89ca0483d591b8`  
		Last Modified: Wed, 04 Sep 2024 21:55:29 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental-20240904` - linux; arm variant v7

```console
$ docker pull debian@sha256:4347b3905200fc49f63939114a4b2010365b60d78d8bd47b70698b43265c25f9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.6 MB (47606229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8177b72ca7367c05691c00bfc93e9503f8471ffa4c148a73f19827717f23e86a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:00:18 GMT
ADD file:188ee06c4b07174ebe1efb972f07c189698c8e6aaec4e4681653eb66ede7229f in / 
# Wed, 04 Sep 2024 22:00:19 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:00:31 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:f0fe53e8c1a634d14df73d8f5c5df0a5976514a2e5bb70738ae9a513a65bdc37`  
		Last Modified: Wed, 04 Sep 2024 22:05:21 GMT  
		Size: 47.6 MB (47606009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff6d1ef272ee9604d9bc413130a443961dcf2ebef77ffc6cd8fdf995e3d5e5d8`  
		Last Modified: Wed, 04 Sep 2024 22:05:40 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental-20240904` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:a94925b56e194b592512978045b923ffa4c47711c4f0023ace4a80fbefcd793f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 MB (53597457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fc02a9d72214b31205f5a865e9ebccc629f34dab60941775bdaee28992b7461`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:41:26 GMT
ADD file:c73496213c4364e2afe7cef81c73160ee1800949da3213240afd91189005b16a in / 
# Wed, 04 Sep 2024 21:41:27 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 21:41:35 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:7a144dc5a59a2e9a4d1bc4511848122724c21361996780033589efa72cdc9052`  
		Last Modified: Wed, 04 Sep 2024 21:45:42 GMT  
		Size: 53.6 MB (53597236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a600f3d8136da5f8c4e5076de5514e98da99383def1983323a40f4c1e6dc3ace`  
		Last Modified: Wed, 04 Sep 2024 21:46:01 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental-20240904` - linux; mips64le

```console
$ docker pull debian@sha256:d261e58407ce3bb37e70dea0e299c76889e08d8d1330175b70dd8d15b7d2e0ea
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.1 MB (52121298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cfb15aba87fd0596bbbc72669c3fd54f09100081461ee47e8afaa3ada03de14`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:21:27 GMT
ADD file:3af3a6c8cd92604c983d6cb309fd33ce4cadcac06889b993c99ebaaeb5bf84cf in / 
# Wed, 04 Sep 2024 22:21:32 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:22:15 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:298ea0ea36a0164973530e4d46c179547253c4db616f218cf9614b1bef05e1c5`  
		Last Modified: Wed, 04 Sep 2024 22:29:45 GMT  
		Size: 52.1 MB (52121076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:009fa8f6adb140e03b58270a990bf1804360da7449705135f639343ba180ffef`  
		Last Modified: Wed, 04 Sep 2024 22:30:23 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental-20240904` - linux; s390x

```console
$ docker pull debian@sha256:e5b0ba6010b3422ef5136cfed97e2640f2042757753d29b5e0c1acdfdc90f010
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.8 MB (52756813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd41269b8e238f8ec564b4f0ec7bf3f2b180e6babf3482749c748b5ff9d97d8c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:46:08 GMT
ADD file:36ed7c04c3421390b664f58f54282b7c1b195cf0e518af9daeb01fb90a75503e in / 
# Wed, 04 Sep 2024 21:46:10 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 21:46:27 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:77c600cb326d786cab19d46a6eebfeff1cbb1218d5ee0194b5ad30e8ab4763c4`  
		Last Modified: Wed, 04 Sep 2024 21:50:18 GMT  
		Size: 52.8 MB (52756593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93914f73df49f80dc675440c1c2c465dd65fa937b013a2d42301127332d7c875`  
		Last Modified: Wed, 04 Sep 2024 21:50:33 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
