## `debian:rc-buggy`

```console
$ docker pull debian@sha256:563eb87869cc1210b146c452c6487880d5f0f194a10ffd83cc285e2ac5d375ed
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

### `debian:rc-buggy` - linux; amd64

```console
$ docker pull debian@sha256:34f6fe15e57ee65e8db1d275bdf75c54eef5e0f77b2f2ffe82fd6ac3292f5129
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52340558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe30f3c7b3c35195617977c1b1937fb79abf1ef122d621f665c74bc2711edf6d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 02:05:41 GMT
ADD file:388f29164844b8493d30bf1feffd1158559ab161886928f977604c10f983a704 in / 
# Wed, 22 Jul 2020 02:05:41 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 02:08:33 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:babaea2ea26ef0e3e4a90ecc928d26bf25d699e1dcba843f16b8a2f0a153b3d7`  
		Last Modified: Wed, 22 Jul 2020 02:11:28 GMT  
		Size: 52.3 MB (52340330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0b98bca4adf1b0fb367e73524f31703023b69573bb6b5e88c57d5005bac9b10`  
		Last Modified: Wed, 22 Jul 2020 02:13:23 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; arm variant v5

```console
$ docker pull debian@sha256:255e3b26604488e71004c19751846faa2db4e95100f729552fa3b45a1d4e37e1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50268961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c98462e8b82e0e714444219d2b6500eb0fa174f24dfdcad9e89b815205758c72`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 00:53:26 GMT
ADD file:72bf1dc350aa2201a007e97d34f6d8ae4edadbfae65004d87b70d8bde1ca66f6 in / 
# Wed, 22 Jul 2020 00:53:27 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 00:56:49 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:3868d999f42cbdf70764edb51ce2454cdb2f061f76b646ca6b109e3294cd106a`  
		Last Modified: Wed, 22 Jul 2020 01:01:42 GMT  
		Size: 50.3 MB (50268734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f452f563dfabcfb0f06908969c9d6d8f3184df372c4aaafe7651178b9cd1543c`  
		Last Modified: Wed, 22 Jul 2020 01:05:04 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; arm variant v7

```console
$ docker pull debian@sha256:1e9c719902cfb76adf1c72167781622269a615ec4d49106314e89f72739a00df
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (48046820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b253ed5c727ce193a2f68b9cf1c7628e0d1b26ce1b728eaa6225e41a47a44782`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 01:27:52 GMT
ADD file:3ab6a11382a4a9f69a874d734a83342969068fe2d2a62b325658fb5ac421f650 in / 
# Wed, 22 Jul 2020 01:27:59 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 01:38:39 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:04602b0eaf483684b8d51ffeb79a3e05e2f29421e1090b3050c1b163ef02f10e`  
		Last Modified: Wed, 22 Jul 2020 01:42:51 GMT  
		Size: 48.0 MB (48046591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f605a7aa3e2e74731da137f607be6510dc68890ee7f332e8e881dd14f80db43`  
		Last Modified: Wed, 22 Jul 2020 01:45:59 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:d5bbdc4e919544701c97acde7b941dcab8bfdb79df875d0d778d1e152cd11b79
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.7 MB (50699779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69051a844be897cb2c3b46ccad8848d17e8df991c26869761ed0c14a13adc88d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 00:42:14 GMT
ADD file:0f4a1ab6b889d98f711b241dde31787e633494e233067fe98dce73de73c2d7f3 in / 
# Wed, 22 Jul 2020 00:42:17 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 00:45:54 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:3af651ddf153ddf8519b20c192d158afb60045252366ddc81e15c938b792982e`  
		Last Modified: Wed, 22 Jul 2020 00:48:41 GMT  
		Size: 50.7 MB (50699554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68749f3989b54988d502731fab53de931d3b1cdee8b1932f31552c4296b9c0fd`  
		Last Modified: Wed, 22 Jul 2020 00:51:43 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; 386

```console
$ docker pull debian@sha256:6e39f401dfcc6edf3e40b131c3cf17ad78868556986ee88307c19120532e1343
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.4 MB (53433800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79531a27f3b792d58ffc4789eb791d791f0c70658e59baa48977c91da1682756`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 02:11:12 GMT
ADD file:1c3529ea5c695a0705497b4510edaf2034b3d29a608dea3db741a4298a117d33 in / 
# Wed, 22 Jul 2020 02:11:13 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 02:13:55 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:32126ce0c55cb16ee9848f6d067e47a287f981a106ba123e3f2590544677f0e6`  
		Last Modified: Wed, 22 Jul 2020 02:18:12 GMT  
		Size: 53.4 MB (53433577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afe8f08db9e4344b4a0f5f8bec66f6a0b8ec9ad1fd8902f24a776e35138c1879`  
		Last Modified: Wed, 22 Jul 2020 02:20:39 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; mips64le

```console
$ docker pull debian@sha256:7f86547c82f2264d26aca71829cb17c0ad9b312b759b5a1fc75c58ba0ac94602
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51079098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:465397e5b9b712511d388011ea972a306d130e6511677447c6bd42062d2a3037`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 01:10:23 GMT
ADD file:ba027e751512c2bd75301e89e6e4ff2f37ba0d5a4dc18785ef0805c0c44217bc in / 
# Wed, 22 Jul 2020 01:10:24 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 01:13:39 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:c1d6004a331270728a8745881ac080835166c19dd8097eeccdb751f6118875fd`  
		Last Modified: Wed, 22 Jul 2020 01:17:34 GMT  
		Size: 51.1 MB (51078870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8502524ecca370b2640c107e9e3d047770276ab2c0c0a9dba5a1482167ec9c9a`  
		Last Modified: Wed, 22 Jul 2020 01:22:22 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; ppc64le

```console
$ docker pull debian@sha256:cb0a11d968f8c85f1289c5cf1d00f8c4aad031bc736fd7c05ea9515a2274cbad
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.1 MB (56108248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98a895fc08d21b5edaf42df0886fca83dfd3ca91972625eb2e0620805b2cfec9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 02:16:35 GMT
ADD file:ca372c2f3271854631f36130adcf0999ef2bedda1861c3d9eca094bcbf3309d6 in / 
# Wed, 22 Jul 2020 02:16:42 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 02:20:32 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:704e914d9d9038374759febe1260b7ddd11c6c32ee44b3d5a2acd6fca2eb8377`  
		Last Modified: Wed, 22 Jul 2020 02:27:16 GMT  
		Size: 56.1 MB (56108021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30f6202acd481368161682609362b898dbe9624c8a6e3689e00aaf85a3a62c6f`  
		Last Modified: Wed, 22 Jul 2020 02:33:37 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; s390x

```console
$ docker pull debian@sha256:7cd84df58894b83666edbbd9a0267f1c3a7065af7fccfc9eb2760155b2d960d4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (50989903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faf5fc14276aeade613b9a7961171dde3bf169e7cef0c12fd34d74886aba1dc0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Aug 2020 01:17:26 GMT
ADD file:a96b6121a19d104791604cd0cd10ee066e9d0f56abcc8f3f9cc1cfa691f2c4eb in / 
# Tue, 04 Aug 2020 01:17:28 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 01:18:53 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:1776f15db22f5bcf0f222cdcea18411e8904b4ebbb37ce537b90d8cea466e2cf`  
		Last Modified: Tue, 04 Aug 2020 01:20:17 GMT  
		Size: 51.0 MB (50989676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dfb232e1eef173702754cf6bc85a74ce5bccaec93a13feaff5b1c68db6279ed`  
		Last Modified: Tue, 04 Aug 2020 01:21:52 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
