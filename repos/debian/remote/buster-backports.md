## `debian:buster-backports`

```console
$ docker pull debian@sha256:7e8950f87ebf6a728f85497ef71429baf27c55065f3b60bb2278271e929f5595
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `debian:buster-backports` - linux; amd64

```console
$ docker pull debian@sha256:f681002937a644c0f1a64f3ad00f5ebd0ce1b06a4bfadc464a7bdc0fc5a025f8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50500341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e607be249e1ab840fa5bcb4785fc20f3c77842b931861407c0216efc12f7770e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:53 GMT
ADD file:dccb5d0cbcf502fb7c4135575f44ac26d665fc92f50546f3a7f9e4d433726453 in / 
# Tue, 13 Feb 2024 00:37:54 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 00:37:58 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:544676cb5e57a1ca47f178393253edded2bd54fba92674c7384013b4ddc87226`  
		Last Modified: Tue, 13 Feb 2024 00:43:09 GMT  
		Size: 50.5 MB (50500120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a99da7f24205ee4f2941f4c1fce89b1e10c8ef63ddd2e1fb286a04bc810cfccf`  
		Last Modified: Tue, 13 Feb 2024 00:43:21 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:c97d737f37abb3caf67f34ee0257aa7aee612523ffa15516889cb1d516f33fd1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (45967848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f25568b7080c896c71065b0fd7f8b67818c2435b72e838e31b7a489da9c575cf`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:20:54 GMT
ADD file:952ff0908ecc63aa19ee3459c5e4ffbf10a0917e72f12212cec4e26ca37e18d3 in / 
# Tue, 13 Feb 2024 01:20:55 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:21:01 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:23a6e5471cecf9aa4fa6cf1fd7037e25b9e75821953151df1a9eb5cac88d5dae`  
		Last Modified: Tue, 13 Feb 2024 01:28:01 GMT  
		Size: 46.0 MB (45967625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ad102b2e8648a79022ab17c789984d7d274fa51b221e4a71f0e75400e688482`  
		Last Modified: Tue, 13 Feb 2024 01:28:15 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:ab3f885f094d357c814899e4cc0d98714b83fce042aeeda509379afce6bdbbd9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49288985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d5ba4b6ab69033b25e7bf026bfd53ed65e0ba01e2ee7fabdf8053b71f8e6501`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:41 GMT
ADD file:d671633736a15466494172d0076cd1a54d5c7a6b2972f9e84d0fb5136ec19f80 in / 
# Tue, 13 Feb 2024 00:41:42 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 00:41:44 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:b2f3ac0fe192916cc6604d5941f01da385bf4b3d3bad97186f040b26e521c464`  
		Last Modified: Tue, 13 Feb 2024 00:45:57 GMT  
		Size: 49.3 MB (49288763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:412331b5a63ac46cef9d5bbe1228606c6b0433018e134da4ea029639a1784329`  
		Last Modified: Tue, 13 Feb 2024 00:46:09 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; 386

```console
$ docker pull debian@sha256:fa5a48262dfed6061644212d8668afb97a4f0592237daceb0707c3781ba76daf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.3 MB (51255580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1376bfd1671cf10f87b3d915944672fa249cbf14a075e815e1e7f14d40a7be0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:39:30 GMT
ADD file:654c015ee394379d17dbff41ad51721cde33b46fa1db3b0e9a7d54473d92d291 in / 
# Tue, 13 Feb 2024 00:39:30 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 00:39:33 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:33a96960e66e0a13921d9c0fbd1ff84e40544f75b84b3cb7124dc858fc844dc3`  
		Last Modified: Tue, 13 Feb 2024 00:44:58 GMT  
		Size: 51.3 MB (51255359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54c57b0921e0843d6f7e864434c898dfe00105e92ff20ee7ffc6aeb772e5de3d`  
		Last Modified: Tue, 13 Feb 2024 00:45:13 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
