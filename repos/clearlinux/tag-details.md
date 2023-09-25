<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `clearlinux`

-	[`clearlinux:base`](#clearlinuxbase)
-	[`clearlinux:latest`](#clearlinuxlatest)

## `clearlinux:base`

```console
$ docker pull clearlinux@sha256:c6443e8dd5a41b85a14fe69259b71251b045c298106d9735b579771656386ec4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:base` - linux; amd64

```console
$ docker pull clearlinux@sha256:a9ea2ecba81da05f538975418842a1d351db44941d8254d782001fe3d206dd4b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67695242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f671c2dbb6aa815630a0275708fb45429cf56aed0d3e9a815ccd2c135e563b67`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Mar 2021 00:22:54 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Mon, 25 Sep 2023 19:19:47 GMT
ADD file:16b22a04f302038e4d2cc74475b13bdce27e00e21866f3256638ef33821020e5 in / 
# Mon, 25 Sep 2023 19:19:48 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     grep root /usr/share/defaults/etc/shadow > /etc/shadow
# Mon, 25 Sep 2023 19:19:48 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:5e60d49f583da3e0b439b807e1451f613d70462ceb3e661a4cbfebb56b3c9ba6`  
		Last Modified: Mon, 25 Sep 2023 19:20:05 GMT  
		Size: 67.7 MB (67695025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b39fe0031b82c4dc402cdbec260deec2fd6cc06b19b15fe9451af7257a4dad2`  
		Last Modified: Mon, 25 Sep 2023 19:19:56 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `clearlinux:latest`

```console
$ docker pull clearlinux@sha256:c6443e8dd5a41b85a14fe69259b71251b045c298106d9735b579771656386ec4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:latest` - linux; amd64

```console
$ docker pull clearlinux@sha256:a9ea2ecba81da05f538975418842a1d351db44941d8254d782001fe3d206dd4b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67695242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f671c2dbb6aa815630a0275708fb45429cf56aed0d3e9a815ccd2c135e563b67`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Mar 2021 00:22:54 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Mon, 25 Sep 2023 19:19:47 GMT
ADD file:16b22a04f302038e4d2cc74475b13bdce27e00e21866f3256638ef33821020e5 in / 
# Mon, 25 Sep 2023 19:19:48 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     grep root /usr/share/defaults/etc/shadow > /etc/shadow
# Mon, 25 Sep 2023 19:19:48 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:5e60d49f583da3e0b439b807e1451f613d70462ceb3e661a4cbfebb56b3c9ba6`  
		Last Modified: Mon, 25 Sep 2023 19:20:05 GMT  
		Size: 67.7 MB (67695025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b39fe0031b82c4dc402cdbec260deec2fd6cc06b19b15fe9451af7257a4dad2`  
		Last Modified: Mon, 25 Sep 2023 19:19:56 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
