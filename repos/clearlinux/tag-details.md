<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `clearlinux`

-	[`clearlinux:base`](#clearlinuxbase)
-	[`clearlinux:latest`](#clearlinuxlatest)

## `clearlinux:base`

```console
$ docker pull clearlinux@sha256:78a9f76be5297fe4455e29169cdd2f12f27e0e093468354933db78f6921f6c50
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `clearlinux:base` - linux; amd64

```console
$ docker pull clearlinux@sha256:ccaf55331ac4d8c815e158493959d73342d631d325badfb789e98d7f84d335b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.3 MB (72254071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36b6bf15d1c7239e4e1b035b2e702340bd80352a5f0c117ee8a16200fc84f3c4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 04 Feb 2025 18:07:55 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Tue, 04 Feb 2025 18:07:55 GMT
ADD base.tar.xz / # buildkit
# Tue, 04 Feb 2025 18:07:55 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     echo 'root:!:::::::' > /etc/shadow # buildkit
# Tue, 04 Feb 2025 18:07:55 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:d8b446266af417203ddeabfe64ef9ec39bd9602c347380c3e611ddd70af07332`  
		Last Modified: Tue, 11 Feb 2025 03:11:49 GMT  
		Size: 72.3 MB (72253857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:457f4d5b67f8e66ba8be9f3ca344480f0283e4837e4ce3bd6e1e8c9dfb3cd84a`  
		Last Modified: Tue, 11 Feb 2025 03:18:29 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clearlinux:base` - unknown; unknown

```console
$ docker pull clearlinux@sha256:44ce812ea5f0a464b838f3c69f7ad5f9fc8b42e885b1bb4cfd4a29f7bd1759aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 KB (6275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8c8c74facc9e7f5695266bdae7322e18d27f670ae3640f6b37939eb3da8584f`

```dockerfile
```

-	Layers:
	-	`sha256:d61a2ac69a90a5cec059104eaa2555d001114bc1410aab76099a4c55724f455d`  
		Last Modified: Mon, 17 Feb 2025 16:14:47 GMT  
		Size: 6.3 KB (6275 bytes)  
		MIME: application/vnd.in-toto+json

## `clearlinux:latest`

```console
$ docker pull clearlinux@sha256:78a9f76be5297fe4455e29169cdd2f12f27e0e093468354933db78f6921f6c50
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `clearlinux:latest` - linux; amd64

```console
$ docker pull clearlinux@sha256:ccaf55331ac4d8c815e158493959d73342d631d325badfb789e98d7f84d335b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.3 MB (72254071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36b6bf15d1c7239e4e1b035b2e702340bd80352a5f0c117ee8a16200fc84f3c4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 04 Feb 2025 18:07:55 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Tue, 04 Feb 2025 18:07:55 GMT
ADD base.tar.xz / # buildkit
# Tue, 04 Feb 2025 18:07:55 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     echo 'root:!:::::::' > /etc/shadow # buildkit
# Tue, 04 Feb 2025 18:07:55 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:d8b446266af417203ddeabfe64ef9ec39bd9602c347380c3e611ddd70af07332`  
		Last Modified: Tue, 11 Feb 2025 03:11:49 GMT  
		Size: 72.3 MB (72253857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:457f4d5b67f8e66ba8be9f3ca344480f0283e4837e4ce3bd6e1e8c9dfb3cd84a`  
		Last Modified: Tue, 11 Feb 2025 03:18:29 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clearlinux:latest` - unknown; unknown

```console
$ docker pull clearlinux@sha256:44ce812ea5f0a464b838f3c69f7ad5f9fc8b42e885b1bb4cfd4a29f7bd1759aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 KB (6275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8c8c74facc9e7f5695266bdae7322e18d27f670ae3640f6b37939eb3da8584f`

```dockerfile
```

-	Layers:
	-	`sha256:d61a2ac69a90a5cec059104eaa2555d001114bc1410aab76099a4c55724f455d`  
		Last Modified: Mon, 17 Feb 2025 16:14:47 GMT  
		Size: 6.3 KB (6275 bytes)  
		MIME: application/vnd.in-toto+json
