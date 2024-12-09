## `clearlinux:latest`

```console
$ docker pull clearlinux@sha256:1f3fa7d095420e5a6093e051a4396cf62faa9ff180d3bc5dc42cbddbffcc89aa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `clearlinux:latest` - linux; amd64

```console
$ docker pull clearlinux@sha256:aef2d423eaec7765e0335c7248ede2333539a4ac8d0fe6ed0698c89c2a9b6e00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.1 MB (72063210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:328342b58853e7a267d0edecdc5fc57f8f051a402ce4715c0e98357362cebc15`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 05 Dec 2024 19:46:52 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Thu, 05 Dec 2024 19:46:52 GMT
ADD base.tar.xz / # buildkit
# Thu, 05 Dec 2024 19:46:52 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     echo 'root:!:::::::' > /etc/shadow # buildkit
# Thu, 05 Dec 2024 19:46:52 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:8530661b1675220ac3b06c5f2b25653621d0d56b00ba8bc9403d57da8d5f2142`  
		Last Modified: Mon, 09 Dec 2024 19:28:10 GMT  
		Size: 72.1 MB (72062997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98de1f0075e8d05edbb55a0194e22e9468308c013be168129b51823118e4671b`  
		Last Modified: Mon, 09 Dec 2024 19:28:09 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clearlinux:latest` - unknown; unknown

```console
$ docker pull clearlinux@sha256:079428f47cadce7fa7a6f0c15c44250f395d0df6cc64eab57f95c0e9c808c91f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 KB (6275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abb35224104e5d6551b2eec26c52a3bddf01cc6f421a1d9ccd14ebc49a07904b`

```dockerfile
```

-	Layers:
	-	`sha256:e9924367ca0d9ad347c86504df2639fbbf3335ac70b9d553746ab0d0c655f7b3`  
		Last Modified: Mon, 09 Dec 2024 19:28:09 GMT  
		Size: 6.3 KB (6275 bytes)  
		MIME: application/vnd.in-toto+json
