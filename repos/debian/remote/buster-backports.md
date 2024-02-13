## `debian:buster-backports`

```console
$ docker pull debian@sha256:25072e62be3b4a57ded37479baa38e6a32bb683b09cb980dad5b2c8ab82518d9
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
$ docker pull debian@sha256:f2980495b0321a37762a9d265d4939ae76b51f6e67d069c23055d028be5ad449
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (45966923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06aa1b18e864b860b2c9b0aabd8f7093b134ebafacf3d4581d44c3ffe8150216`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:51 GMT
ADD file:f7d675054a4ba85691acd979742ab5f8839e1e198ce8bb7830a06479744db901 in / 
# Wed, 31 Jan 2024 22:44:54 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 22:44:57 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:d262abdf15e38f7960a48edbd9d8d9de475362307d40e6620e518de8d55b49d6`  
		Last Modified: Wed, 31 Jan 2024 22:49:56 GMT  
		Size: 46.0 MB (45966700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:677aab6ce61fd8df8379a2bc49055e7f7a101ea6c828c4f063deec834c955c9d`  
		Last Modified: Wed, 31 Jan 2024 22:50:09 GMT  
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
