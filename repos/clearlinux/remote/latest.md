## `clearlinux:latest`

```console
$ docker pull clearlinux@sha256:86987dfe8e7dc45bc6038a5d6d3a0dd40ef9415fb5c0dd1e0bf5efd4c86e3e29
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `clearlinux:latest` - linux; amd64

```console
$ docker pull clearlinux@sha256:e953a0eaf1a8073a21d3161359b87a920e1630ac2e987fce9975774db0236c56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.8 MB (72795692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0151660bd4ecdccf0184c2e3123e84c5fa75981bd8083230631532684693eb52`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 10 Apr 2025 16:23:07 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Thu, 10 Apr 2025 16:23:07 GMT
ADD base.tar.xz / # buildkit
# Thu, 10 Apr 2025 16:23:07 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     echo 'root:!:::::::' > /etc/shadow # buildkit
# Thu, 10 Apr 2025 16:23:07 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:742e9337a836629ad4ff3117fb22835fc47c894fb118360d390b99cfb05ac5cc`  
		Last Modified: Mon, 14 Apr 2025 18:02:47 GMT  
		Size: 72.8 MB (72795477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:714b59d4ec51e078e17fdcea4d30d10974128461268a4362827f8d6759d070a3`  
		Last Modified: Mon, 14 Apr 2025 18:02:44 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clearlinux:latest` - unknown; unknown

```console
$ docker pull clearlinux@sha256:f62a3b673f60a39fb21a2af94a03b33ce26a168162209c9d11fb3c910db3ad89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 KB (6275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ba693851dd860f7306d43532eefefedb6f7109641c0f3b6fba80c8cceeeea00`

```dockerfile
```

-	Layers:
	-	`sha256:9e7feabc0e93e3a208c40c4fcc476bb4a32b65d356605ef995f6ce1efaec4d30`  
		Last Modified: Mon, 14 Apr 2025 18:02:44 GMT  
		Size: 6.3 KB (6275 bytes)  
		MIME: application/vnd.in-toto+json
