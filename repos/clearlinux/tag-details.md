<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `clearlinux`

-	[`clearlinux:base`](#clearlinuxbase)
-	[`clearlinux:latest`](#clearlinuxlatest)

## `clearlinux:base`

```console
$ docker pull clearlinux@sha256:6fd0e2b06b784f1f981e9f7ae8bf1398a880efe033954615bdb4fb7762f9f420
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `clearlinux:base` - linux; amd64

```console
$ docker pull clearlinux@sha256:0d63fcff94caa61afc502a2f545b5311a83a292f6d0a5910b5b80ea996456c19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.1 MB (74082003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4503632e1a6769be85de11e87bf5cf5a3622bf199572cf903fb1c8ec4475ded0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 22 May 2025 16:09:50 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Thu, 22 May 2025 16:09:50 GMT
ADD base.tar.xz / # buildkit
# Thu, 22 May 2025 16:09:50 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     echo 'root:!:::::::' > /etc/shadow # buildkit
# Thu, 22 May 2025 16:09:50 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:5b58bce671667b1f9f4aeaa06a94a672cd1007979e898500785ff61c26b33038`  
		Last Modified: Tue, 27 May 2025 18:53:54 GMT  
		Size: 74.1 MB (74081790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f2007758092f5682e0a9f8177139555d716715cdc22b06a7f1e446f2d2cc26`  
		Last Modified: Tue, 27 May 2025 18:53:53 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clearlinux:base` - unknown; unknown

```console
$ docker pull clearlinux@sha256:065bd21ccc13683f05400805adf25372fe6b96d91bfea7ea649e3628b49aa7de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 KB (6275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb60a6f4c8a31c77d5d24687ee27d602d84253633efb9f3811f1b7bd9e2191d7`

```dockerfile
```

-	Layers:
	-	`sha256:fe72afae5c127ae2ec464d409facde41d2d66bfcd24a5d60067b242f7d0e8fc8`  
		Last Modified: Tue, 27 May 2025 18:53:53 GMT  
		Size: 6.3 KB (6275 bytes)  
		MIME: application/vnd.in-toto+json

## `clearlinux:latest`

```console
$ docker pull clearlinux@sha256:6fd0e2b06b784f1f981e9f7ae8bf1398a880efe033954615bdb4fb7762f9f420
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `clearlinux:latest` - linux; amd64

```console
$ docker pull clearlinux@sha256:0d63fcff94caa61afc502a2f545b5311a83a292f6d0a5910b5b80ea996456c19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.1 MB (74082003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4503632e1a6769be85de11e87bf5cf5a3622bf199572cf903fb1c8ec4475ded0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 22 May 2025 16:09:50 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Thu, 22 May 2025 16:09:50 GMT
ADD base.tar.xz / # buildkit
# Thu, 22 May 2025 16:09:50 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     echo 'root:!:::::::' > /etc/shadow # buildkit
# Thu, 22 May 2025 16:09:50 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:5b58bce671667b1f9f4aeaa06a94a672cd1007979e898500785ff61c26b33038`  
		Last Modified: Tue, 27 May 2025 18:53:54 GMT  
		Size: 74.1 MB (74081790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f2007758092f5682e0a9f8177139555d716715cdc22b06a7f1e446f2d2cc26`  
		Last Modified: Tue, 27 May 2025 18:53:53 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clearlinux:latest` - unknown; unknown

```console
$ docker pull clearlinux@sha256:065bd21ccc13683f05400805adf25372fe6b96d91bfea7ea649e3628b49aa7de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 KB (6275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb60a6f4c8a31c77d5d24687ee27d602d84253633efb9f3811f1b7bd9e2191d7`

```dockerfile
```

-	Layers:
	-	`sha256:fe72afae5c127ae2ec464d409facde41d2d66bfcd24a5d60067b242f7d0e8fc8`  
		Last Modified: Tue, 27 May 2025 18:53:53 GMT  
		Size: 6.3 KB (6275 bytes)  
		MIME: application/vnd.in-toto+json
