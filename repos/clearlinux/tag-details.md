<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `clearlinux`

-	[`clearlinux:base`](#clearlinuxbase)
-	[`clearlinux:latest`](#clearlinuxlatest)

## `clearlinux:base`

```console
$ docker pull clearlinux@sha256:f1fca5b697de4f5d7740fbe0374bafd80c900974691b007951c0c1190ef48254
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `clearlinux:base` - linux; amd64

```console
$ docker pull clearlinux@sha256:be6b753d5677ec5ae47e3324652b8125ef7bd1174f5b032e3058197ae1f64995
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72735093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f85a4568209283776224478ed5759597005e334a06af3e48d7d7ece494175868`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 17 Apr 2025 16:10:14 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Thu, 17 Apr 2025 16:10:14 GMT
ADD base.tar.xz / # buildkit
# Thu, 17 Apr 2025 16:10:14 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     echo 'root:!:::::::' > /etc/shadow # buildkit
# Thu, 17 Apr 2025 16:10:14 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:0c7c93c8a23d66cddf9cf058da328e39370b8b5985d0149db6179049221cae4d`  
		Last Modified: Mon, 21 Apr 2025 22:33:52 GMT  
		Size: 72.7 MB (72734881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6734e6479551f54332f942d46efe92720253121bff18bb100936e7df05a73e9`  
		Last Modified: Mon, 21 Apr 2025 22:33:51 GMT  
		Size: 212.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clearlinux:base` - unknown; unknown

```console
$ docker pull clearlinux@sha256:8cae1df1fbce67b9974e2e02a53debb7ccfc17baad69a462d6a23e3022789466
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 KB (6275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcc2ab1e0b33e1b0cd3a415e5dd7b813a712fd3cf6d1390cb2fa2453a781de5e`

```dockerfile
```

-	Layers:
	-	`sha256:9984c5ac8b8b2a77fa56aa8f32f29ca2b8472caba274eeebc5f95864091ea5e4`  
		Last Modified: Mon, 21 Apr 2025 22:33:51 GMT  
		Size: 6.3 KB (6275 bytes)  
		MIME: application/vnd.in-toto+json

## `clearlinux:latest`

```console
$ docker pull clearlinux@sha256:f1fca5b697de4f5d7740fbe0374bafd80c900974691b007951c0c1190ef48254
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `clearlinux:latest` - linux; amd64

```console
$ docker pull clearlinux@sha256:be6b753d5677ec5ae47e3324652b8125ef7bd1174f5b032e3058197ae1f64995
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72735093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f85a4568209283776224478ed5759597005e334a06af3e48d7d7ece494175868`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 17 Apr 2025 16:10:14 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Thu, 17 Apr 2025 16:10:14 GMT
ADD base.tar.xz / # buildkit
# Thu, 17 Apr 2025 16:10:14 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     echo 'root:!:::::::' > /etc/shadow # buildkit
# Thu, 17 Apr 2025 16:10:14 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:0c7c93c8a23d66cddf9cf058da328e39370b8b5985d0149db6179049221cae4d`  
		Last Modified: Mon, 21 Apr 2025 22:33:52 GMT  
		Size: 72.7 MB (72734881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6734e6479551f54332f942d46efe92720253121bff18bb100936e7df05a73e9`  
		Last Modified: Mon, 21 Apr 2025 22:33:51 GMT  
		Size: 212.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clearlinux:latest` - unknown; unknown

```console
$ docker pull clearlinux@sha256:8cae1df1fbce67b9974e2e02a53debb7ccfc17baad69a462d6a23e3022789466
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 KB (6275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcc2ab1e0b33e1b0cd3a415e5dd7b813a712fd3cf6d1390cb2fa2453a781de5e`

```dockerfile
```

-	Layers:
	-	`sha256:9984c5ac8b8b2a77fa56aa8f32f29ca2b8472caba274eeebc5f95864091ea5e4`  
		Last Modified: Mon, 21 Apr 2025 22:33:51 GMT  
		Size: 6.3 KB (6275 bytes)  
		MIME: application/vnd.in-toto+json
