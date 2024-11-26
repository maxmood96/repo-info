<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `clearlinux`

-	[`clearlinux:base`](#clearlinuxbase)
-	[`clearlinux:latest`](#clearlinuxlatest)

## `clearlinux:base`

```console
$ docker pull clearlinux@sha256:9450f61f65d599213479e38dcab5784bbfcc9abaadd9f7a62e95a519eb6ab9a6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `clearlinux:base` - linux; amd64

```console
$ docker pull clearlinux@sha256:021d7e6e95059dc75fd7a7ff39dfb0456dd8942d0d5833908f80922ae9e104bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.1 MB (72067736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1211fa623d46c0d7d50869bb98be1dcf1d9061ccfc525e511e58c14f705c134`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 19 Nov 2024 23:37:10 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Tue, 19 Nov 2024 23:37:10 GMT
ADD base.tar.xz / # buildkit
# Tue, 19 Nov 2024 23:37:10 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     echo 'root:!:::::::' > /etc/shadow # buildkit
# Tue, 19 Nov 2024 23:37:10 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:7e457e7b95d3b6808c8f3b89f1d4add01d433d9135d496635c510329bf6d305a`  
		Last Modified: Mon, 25 Nov 2024 20:23:45 GMT  
		Size: 72.1 MB (72067522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f89d4f847aa09b827fcfa600d89611d801bd884ea62321545d4e4b26969b5ba8`  
		Last Modified: Mon, 25 Nov 2024 20:23:44 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clearlinux:base` - unknown; unknown

```console
$ docker pull clearlinux@sha256:07cd0ae33d061fcd700144de96906fa1c13740f3b5afb35f7cb6802f01ffe5ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 KB (6275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d669f753018fd548cb97f1c373356cdda46f33d76f6c5bd62823e5ceedb9fcb`

```dockerfile
```

-	Layers:
	-	`sha256:16beadf54659c60ab47dc858183b7cb669fbad1c8c5ce2dc53a8e726725b9666`  
		Last Modified: Mon, 25 Nov 2024 20:23:44 GMT  
		Size: 6.3 KB (6275 bytes)  
		MIME: application/vnd.in-toto+json

## `clearlinux:latest`

```console
$ docker pull clearlinux@sha256:9450f61f65d599213479e38dcab5784bbfcc9abaadd9f7a62e95a519eb6ab9a6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `clearlinux:latest` - linux; amd64

```console
$ docker pull clearlinux@sha256:021d7e6e95059dc75fd7a7ff39dfb0456dd8942d0d5833908f80922ae9e104bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.1 MB (72067736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1211fa623d46c0d7d50869bb98be1dcf1d9061ccfc525e511e58c14f705c134`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 19 Nov 2024 23:37:10 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Tue, 19 Nov 2024 23:37:10 GMT
ADD base.tar.xz / # buildkit
# Tue, 19 Nov 2024 23:37:10 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     echo 'root:!:::::::' > /etc/shadow # buildkit
# Tue, 19 Nov 2024 23:37:10 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:7e457e7b95d3b6808c8f3b89f1d4add01d433d9135d496635c510329bf6d305a`  
		Last Modified: Mon, 25 Nov 2024 20:23:45 GMT  
		Size: 72.1 MB (72067522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f89d4f847aa09b827fcfa600d89611d801bd884ea62321545d4e4b26969b5ba8`  
		Last Modified: Mon, 25 Nov 2024 20:23:44 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clearlinux:latest` - unknown; unknown

```console
$ docker pull clearlinux@sha256:07cd0ae33d061fcd700144de96906fa1c13740f3b5afb35f7cb6802f01ffe5ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 KB (6275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d669f753018fd548cb97f1c373356cdda46f33d76f6c5bd62823e5ceedb9fcb`

```dockerfile
```

-	Layers:
	-	`sha256:16beadf54659c60ab47dc858183b7cb669fbad1c8c5ce2dc53a8e726725b9666`  
		Last Modified: Mon, 25 Nov 2024 20:23:44 GMT  
		Size: 6.3 KB (6275 bytes)  
		MIME: application/vnd.in-toto+json
