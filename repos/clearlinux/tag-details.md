<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `clearlinux`

-	[`clearlinux:base`](#clearlinuxbase)
-	[`clearlinux:latest`](#clearlinuxlatest)

## `clearlinux:base`

```console
$ docker pull clearlinux@sha256:68cfba7bf2ce144862faa0a9ee86bbb913d254f6b59afd0d6b8c2bd0e4586380
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:base` - linux; amd64

```console
$ docker pull clearlinux@sha256:1eab04ea3339fccb706fc75209137f943d6357284d54f4be18107ab37658c98b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.3 MB (69300831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92ee1f7d0922c2806bccdc8d21aa82559e11b2e5d50dfe95000ba4ee975e93ff`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 28 May 2024 19:38:39 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Mon, 03 Jun 2024 18:46:14 GMT
ADD file:0ef1ed0c077a35b0bbb31562f07b749d50ed21870db34d23a8e25bd67cb97d34 in / 
# Mon, 03 Jun 2024 18:46:15 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     echo 'root:!:::::::' > /etc/shadow
# Mon, 03 Jun 2024 18:46:16 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:796333ca3902a0c41d7fb57adddf67a684d30f882ed2a2e6445271273f6d2ca5`  
		Last Modified: Mon, 03 Jun 2024 18:46:33 GMT  
		Size: 69.3 MB (69300618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf50ace99a00c03f1e25b59da889c0e5eac02049f617c263b34d6976e1ce6b3a`  
		Last Modified: Mon, 03 Jun 2024 18:46:24 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `clearlinux:latest`

```console
$ docker pull clearlinux@sha256:68cfba7bf2ce144862faa0a9ee86bbb913d254f6b59afd0d6b8c2bd0e4586380
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:latest` - linux; amd64

```console
$ docker pull clearlinux@sha256:1eab04ea3339fccb706fc75209137f943d6357284d54f4be18107ab37658c98b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.3 MB (69300831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92ee1f7d0922c2806bccdc8d21aa82559e11b2e5d50dfe95000ba4ee975e93ff`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 28 May 2024 19:38:39 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Mon, 03 Jun 2024 18:46:14 GMT
ADD file:0ef1ed0c077a35b0bbb31562f07b749d50ed21870db34d23a8e25bd67cb97d34 in / 
# Mon, 03 Jun 2024 18:46:15 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     echo 'root:!:::::::' > /etc/shadow
# Mon, 03 Jun 2024 18:46:16 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:796333ca3902a0c41d7fb57adddf67a684d30f882ed2a2e6445271273f6d2ca5`  
		Last Modified: Mon, 03 Jun 2024 18:46:33 GMT  
		Size: 69.3 MB (69300618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf50ace99a00c03f1e25b59da889c0e5eac02049f617c263b34d6976e1ce6b3a`  
		Last Modified: Mon, 03 Jun 2024 18:46:24 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
