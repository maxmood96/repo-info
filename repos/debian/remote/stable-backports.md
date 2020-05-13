## `debian:stable-backports`

```console
$ docker pull debian@sha256:3e0aaf7b71efd95f9fdc1625f480171c3c97381022c5d8f3abce90aee0012179
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

### `debian:stable-backports` - linux; amd64

```console
$ docker pull debian@sha256:503715580fea25477efab424d660fb14f5c90695ec4eee9d363f55aa85baffb9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50387707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbbf58805393b76368d24d7a2a3418d3019bfbe3ddea13368239982d60bba608`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 13 May 2020 21:23:00 GMT
ADD file:e9c40bd50f470b0a7b37d1ab060af34f57c76aca440f0b1d79aab4e8910ee17e in / 
# Wed, 13 May 2020 21:23:00 GMT
CMD ["bash"]
# Wed, 13 May 2020 21:23:06 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:b524cedb63ffa97ab17d2647036a25750d2dfa4771dc136237acbcfb09fa0462`  
		Last Modified: Wed, 13 May 2020 21:29:30 GMT  
		Size: 50.4 MB (50387485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbcaf5e6e52801eb9a61f29b168d00c0e8fc6c1cf915b4cddbf49ce29b319aa4`  
		Last Modified: Wed, 13 May 2020 21:29:36 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:fffee85ba06b4ba5b917ec6fc78cd1061e3337acbd5618e13d9d5fb0f5d41968
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 MB (48096963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15c4d17ecbe175a7468fcd9a9f312c88c29644c59e04da38b835c9a2a416617e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:55:04 GMT
ADD file:82c130da53ee3bd119b10da370ede912b233caa259bfb647ca931feb92be2dc1 in / 
# Thu, 23 Apr 2020 00:55:05 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 00:55:12 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:5252cc0bde5f71c14833a3a353f87d023c7ff6c96b5178d86b5f2283abf7252a`  
		Last Modified: Thu, 23 Apr 2020 01:02:54 GMT  
		Size: 48.1 MB (48096738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e8bede32ccc866a77d3f3975c0b52cc8183a622b26d30e5bcf519e04da531b9`  
		Last Modified: Thu, 23 Apr 2020 01:03:03 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:49da7d2dd5c82c4ae064f823c7b0b70abc9205b4c17dc6ea005c53a612643916
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45871513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb8bea0fdb3b8688736e14f7df5d059332e0f2c0bed123b05533e08bcb480fd4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 13 May 2020 21:17:59 GMT
ADD file:a8598238d38d8e7815511cd4c1041c0283ed5814b02e1f5348a99a68c9aaed4f in / 
# Wed, 13 May 2020 21:18:01 GMT
CMD ["bash"]
# Wed, 13 May 2020 21:18:09 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:477908ea56bab4a69000b3730a514d140f087cc945aab3dbaf4e9dd950168a25`  
		Last Modified: Wed, 13 May 2020 21:27:35 GMT  
		Size: 45.9 MB (45871288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c63feb38e93dc755acc146895fc9ea8f91ec9740007b76afaf67d64263b14e9`  
		Last Modified: Wed, 13 May 2020 21:27:42 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:e3302e7f49fc7a4f05741b765c142eeedcd2c41ae08f48d8d2db2079f81f3cff
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49168431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af55b82d6e639e99f678e7715df9083874a9e54dcc56d13455cdf004092499f2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 13 May 2020 21:46:26 GMT
ADD file:834efa6ef9a13c35ab72dc6a73453ac6cc7033ad45c00eaee6a8419b11ef1a2f in / 
# Wed, 13 May 2020 21:46:28 GMT
CMD ["bash"]
# Wed, 13 May 2020 21:46:37 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:d4e97e57656451a538b8a11ffe5155f994ef3442904490aa0382bac955ce5dcf`  
		Last Modified: Wed, 13 May 2020 21:55:26 GMT  
		Size: 49.2 MB (49168207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63814573b27fafac27f727c3f09bbd908a16699a9bc9f2d1daab70b835bdb6e7`  
		Last Modified: Wed, 13 May 2020 21:55:34 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; 386

```console
$ docker pull debian@sha256:b5a3782dda1914d491abf2c7d80610dd7280082a323bbce3dd31b4e7d4fe0f54
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.2 MB (51154070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45d4bcc2e40f46f34efd99c84bec41a48dbb1ec0c9a629e398a80b72a11e287e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 13 May 2020 21:41:49 GMT
ADD file:62f39b7b3178937d8163f0f9d653af6b0a8f30bc47fd77276588c93343009410 in / 
# Wed, 13 May 2020 21:41:49 GMT
CMD ["bash"]
# Wed, 13 May 2020 21:41:54 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:2b8382d3daf21cc75211afcc47e584b30c43e3830bd9b7e8ccb8a44e649385fc`  
		Last Modified: Wed, 13 May 2020 21:49:12 GMT  
		Size: 51.2 MB (51153849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57b94829fbcf595608f89f1fc5dce3069bfeb1b4c59075586f7cf88a2c375f3b`  
		Last Modified: Wed, 13 May 2020 21:49:17 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; mips64le

```console
$ docker pull debian@sha256:639b176e27fb227c06ed1318e504daadeb4281f73d8219b1a515701e0001ac30
```

-	Docker Version: 19.03.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (49019385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1df606ffcb68f591ac21c81e6aecae0920cd3f3575c35d913341080b4449023b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:11:42 GMT
ADD file:5a0065ff326073bf141f8523672b836937bbf34a234e73e42466ed4e18e3bdd7 in / 
# Thu, 23 Apr 2020 00:11:43 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 00:11:50 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:192cb836eb60701de82e3544a2c2279127dbd4f93030d06a700b28355cee7d0f`  
		Last Modified: Thu, 23 Apr 2020 00:21:17 GMT  
		Size: 49.0 MB (49019161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70f26bb7e4228c121e48d3e89dd9fa8569c51bffc6ce0a89cd6c5afed485d2d3`  
		Last Modified: Thu, 23 Apr 2020 00:21:28 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:f0101b3ffaa629cbba3edc80e46f4c3a71835501a7ecff4e981fc807344fc767
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.1 MB (54139822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb52e62651bf5ebba1ac6a9ed79d03f0e3b87749df423d83a1d997bba037b2a5`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:40:13 GMT
ADD file:352901ca72bb329990bed05b43df906f3e61a21a39acf4e7c9a4426339ace2f9 in / 
# Thu, 23 Apr 2020 00:40:17 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 00:40:30 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:c9efe11753157bb4a8b8a89e3186c0413b69200a36afd569d90ccc842a051bf7`  
		Last Modified: Thu, 23 Apr 2020 00:53:23 GMT  
		Size: 54.1 MB (54139597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abd08b9c0abc67885550a2fbb8e7241b0fd376f9a1f3fcf8f2c5b861af6c815f`  
		Last Modified: Thu, 23 Apr 2020 00:53:33 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; s390x

```console
$ docker pull debian@sha256:c05cb5cdb50b4355299572f9d402b454314680a3ed10f96133480c5ac03e8e43
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (48965285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c14bdb3da567855f9170bbcc632fd467846df8768c738cdd89f55c88dc7f897a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 13 May 2020 21:43:48 GMT
ADD file:e5f501377817ca10a81b8a490d52093fc2e343a22fe4804c53043d8af457cda8 in / 
# Wed, 13 May 2020 21:43:50 GMT
CMD ["bash"]
# Wed, 13 May 2020 21:43:55 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:21fc17a33cc162000a4116b24564e99d26cedf1519cfea314ca866447d3d7b35`  
		Last Modified: Wed, 13 May 2020 21:48:07 GMT  
		Size: 49.0 MB (48965062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9cfc3df30500ff41f78b8b6eca2c343587ac073cd6f800a25cdebb312dd4e03`  
		Last Modified: Wed, 13 May 2020 21:48:13 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
