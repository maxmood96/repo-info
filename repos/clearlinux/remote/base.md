## `clearlinux:base`

```console
$ docker pull clearlinux@sha256:649b29eca8296b9b05f18136080165ff42d1d010881fdc68fafa3ee70ac6c3aa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `clearlinux:base` - linux; amd64

```console
$ docker pull clearlinux@sha256:8dbd94608a4046096cbffdb770734246493ae69a3c785966fabf76e11855bbfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.6 MB (73640377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:202109cef637a46a19026cd763de30aafe57b396e1d7942a2f8026572a485602`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 20 Mar 2025 22:54:39 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Thu, 20 Mar 2025 22:54:39 GMT
ADD base.tar.xz / # buildkit
# Thu, 20 Mar 2025 22:54:39 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     echo 'root:!:::::::' > /etc/shadow # buildkit
# Thu, 20 Mar 2025 22:54:39 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:9f97b20b7e625b2b1561cbe461316564e6343386901cfa97690a503778eea809`  
		Last Modified: Mon, 24 Mar 2025 17:02:33 GMT  
		Size: 73.6 MB (73640163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:490f853bf4a8a5995487d25eb3e7c41f3b48a3cd2b66a59e74cf661415a26c53`  
		Last Modified: Mon, 24 Mar 2025 17:02:30 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clearlinux:base` - unknown; unknown

```console
$ docker pull clearlinux@sha256:d96bde245d8a6b3d626ba1036432d957b1233212c299c72a2006d3f154d1e53e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 KB (6275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bac1c30ceded729909fbb3c6dbb5c3da88f5391751febee735d402891ec6f40`

```dockerfile
```

-	Layers:
	-	`sha256:038f2ebc6f602f0e516f7b9b9792155f386c7d71d9bc5af118409f5278b4a409`  
		Last Modified: Mon, 24 Mar 2025 17:02:30 GMT  
		Size: 6.3 KB (6275 bytes)  
		MIME: application/vnd.in-toto+json
