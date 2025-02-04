## `clearlinux:base`

```console
$ docker pull clearlinux@sha256:b4649309ac2eef239a8c7e0a4a1720719616fbd3f723c16739ae835c9082e2f1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `clearlinux:base` - linux; amd64

```console
$ docker pull clearlinux@sha256:31bf15f10c9f7d172ca86127f00b9c21926bfc7eb078bd24bf13541840fdc271
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.2 MB (72221591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c77f0b683aa20798501a7040e8ed3b29ba4660d46036c5277740f871ca2ce4ed`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 28 Jan 2025 17:32:12 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Tue, 28 Jan 2025 17:32:12 GMT
ADD base.tar.xz / # buildkit
# Tue, 28 Jan 2025 17:32:12 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     echo 'root:!:::::::' > /etc/shadow # buildkit
# Tue, 28 Jan 2025 17:32:12 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:1856c168652a1a1468e7fa2a18070d8507f4d9ae1c77b50742b60a9f76be4ed2`  
		Last Modified: Mon, 03 Feb 2025 20:26:37 GMT  
		Size: 72.2 MB (72221377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d1afbf688660561d6ca7a6e586ca2faa470c45f999f44487714561798624fef`  
		Last Modified: Mon, 03 Feb 2025 20:26:36 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clearlinux:base` - unknown; unknown

```console
$ docker pull clearlinux@sha256:ab78a6b23eab6415c604fe3e5a5e520b27085af0d5cc7670348aa3ba71c4b408
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 KB (6275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56ae7581e32a4c66275410b37aef4754e02c5e64cc42f649ec38b1a3bd2a7d95`

```dockerfile
```

-	Layers:
	-	`sha256:4336175a47bf8d7859588af391b0a8a2fa7b1c0c79ffa76b9818b8d6e3d33fec`  
		Last Modified: Mon, 03 Feb 2025 20:26:36 GMT  
		Size: 6.3 KB (6275 bytes)  
		MIME: application/vnd.in-toto+json
