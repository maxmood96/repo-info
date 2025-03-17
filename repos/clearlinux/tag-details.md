<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `clearlinux`

-	[`clearlinux:base`](#clearlinuxbase)
-	[`clearlinux:latest`](#clearlinuxlatest)

## `clearlinux:base`

```console
$ docker pull clearlinux@sha256:2020f6349e31da069f462e877808524508dd451ea73e2fb146e0637a15e6fdac
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `clearlinux:base` - linux; amd64

```console
$ docker pull clearlinux@sha256:357cc9b42d19eb3899e4e493bfaa5d47c40fd1ca4d534a6cfe039b75c02889bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.6 MB (73637409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:396e20cada7199bb09047e5643727c01fd2f40e3137567fd4a20781115eb9dc5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Mar 2025 18:01:59 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Thu, 13 Mar 2025 18:01:59 GMT
ADD base.tar.xz / # buildkit
# Thu, 13 Mar 2025 18:01:59 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     echo 'root:!:::::::' > /etc/shadow # buildkit
# Thu, 13 Mar 2025 18:01:59 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:9a546e2a7a493970292a9d95feed68a21f43f5b46460343cfbe40541bff7852f`  
		Last Modified: Mon, 17 Mar 2025 17:42:04 GMT  
		Size: 73.6 MB (73637197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d139099b3f99cef404bfc308776e7be83a921b32ae75eaf1716c33c6e0b4dc7`  
		Last Modified: Mon, 17 Mar 2025 17:42:01 GMT  
		Size: 212.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clearlinux:base` - unknown; unknown

```console
$ docker pull clearlinux@sha256:d5a196efd026118e7d23849e37b33aa0f3fee9f16d29f6a823462b89b5eb7411
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 KB (6274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15235648286864230b2fb37dc4203b54a9129e3f714e36348978b138015920a3`

```dockerfile
```

-	Layers:
	-	`sha256:e7a54e08f406861caf321a9d48fcc523f8134a5e5775102fd5d45f34cd8f93f6`  
		Last Modified: Mon, 17 Mar 2025 17:42:01 GMT  
		Size: 6.3 KB (6274 bytes)  
		MIME: application/vnd.in-toto+json

## `clearlinux:latest`

```console
$ docker pull clearlinux@sha256:2020f6349e31da069f462e877808524508dd451ea73e2fb146e0637a15e6fdac
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `clearlinux:latest` - linux; amd64

```console
$ docker pull clearlinux@sha256:357cc9b42d19eb3899e4e493bfaa5d47c40fd1ca4d534a6cfe039b75c02889bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.6 MB (73637409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:396e20cada7199bb09047e5643727c01fd2f40e3137567fd4a20781115eb9dc5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Mar 2025 18:01:59 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Thu, 13 Mar 2025 18:01:59 GMT
ADD base.tar.xz / # buildkit
# Thu, 13 Mar 2025 18:01:59 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     echo 'root:!:::::::' > /etc/shadow # buildkit
# Thu, 13 Mar 2025 18:01:59 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:9a546e2a7a493970292a9d95feed68a21f43f5b46460343cfbe40541bff7852f`  
		Last Modified: Mon, 17 Mar 2025 17:42:04 GMT  
		Size: 73.6 MB (73637197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d139099b3f99cef404bfc308776e7be83a921b32ae75eaf1716c33c6e0b4dc7`  
		Last Modified: Mon, 17 Mar 2025 17:42:01 GMT  
		Size: 212.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clearlinux:latest` - unknown; unknown

```console
$ docker pull clearlinux@sha256:d5a196efd026118e7d23849e37b33aa0f3fee9f16d29f6a823462b89b5eb7411
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 KB (6274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15235648286864230b2fb37dc4203b54a9129e3f714e36348978b138015920a3`

```dockerfile
```

-	Layers:
	-	`sha256:e7a54e08f406861caf321a9d48fcc523f8134a5e5775102fd5d45f34cd8f93f6`  
		Last Modified: Mon, 17 Mar 2025 17:42:01 GMT  
		Size: 6.3 KB (6274 bytes)  
		MIME: application/vnd.in-toto+json
