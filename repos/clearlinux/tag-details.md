<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `clearlinux`

-	[`clearlinux:base`](#clearlinuxbase)
-	[`clearlinux:latest`](#clearlinuxlatest)

## `clearlinux:base`

```console
$ docker pull clearlinux@sha256:0c758f0738682da47ce58727a240b979198e4cf80183fdb676e4126471ca9d25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:base` - linux; amd64

```console
$ docker pull clearlinux@sha256:34ac851f289b75c83dfe824bd2b1326b49b67f53ba976e2082a104a68eb8bd43
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.4 MB (65362180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e6dc2a151f6551061650bec4c9512d9d614cc9883461014bcf96e30e6486981`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Mar 2021 00:22:54 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Mon, 25 Mar 2024 19:52:21 GMT
ADD file:14e1af085b694a1af7efd555094d0f46b5cb3b856031ab83b0d025d507fc1926 in / 
# Mon, 25 Mar 2024 19:52:22 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     echo 'root:!:::::::' > /etc/shadow
# Mon, 25 Mar 2024 19:52:22 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:14a55f159712a7f7083b5953d579f8acff088af16986129c83e8b0cf1f4d75bb`  
		Last Modified: Mon, 25 Mar 2024 19:52:39 GMT  
		Size: 65.4 MB (65361967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e919cac579060cb8db584357008564c6d1085c00b3e8329a201858d29ef25c37`  
		Last Modified: Mon, 25 Mar 2024 19:52:31 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `clearlinux:latest`

```console
$ docker pull clearlinux@sha256:0c758f0738682da47ce58727a240b979198e4cf80183fdb676e4126471ca9d25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:latest` - linux; amd64

```console
$ docker pull clearlinux@sha256:34ac851f289b75c83dfe824bd2b1326b49b67f53ba976e2082a104a68eb8bd43
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.4 MB (65362180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e6dc2a151f6551061650bec4c9512d9d614cc9883461014bcf96e30e6486981`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Mar 2021 00:22:54 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Mon, 25 Mar 2024 19:52:21 GMT
ADD file:14e1af085b694a1af7efd555094d0f46b5cb3b856031ab83b0d025d507fc1926 in / 
# Mon, 25 Mar 2024 19:52:22 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     echo 'root:!:::::::' > /etc/shadow
# Mon, 25 Mar 2024 19:52:22 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:14a55f159712a7f7083b5953d579f8acff088af16986129c83e8b0cf1f4d75bb`  
		Last Modified: Mon, 25 Mar 2024 19:52:39 GMT  
		Size: 65.4 MB (65361967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e919cac579060cb8db584357008564c6d1085c00b3e8329a201858d29ef25c37`  
		Last Modified: Mon, 25 Mar 2024 19:52:31 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
