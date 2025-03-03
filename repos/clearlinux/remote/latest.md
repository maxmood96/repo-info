## `clearlinux:latest`

```console
$ docker pull clearlinux@sha256:1cdc8a3ca524623d2b6e48424b4d05e1189a6401b58caff0725a4ec3821dc1db
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `clearlinux:latest` - linux; amd64

```console
$ docker pull clearlinux@sha256:0cb6e93cb202e93115e5cbc2366fb2129bb613b490cd2a163cf3c6de7c00c1f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.4 MB (72380117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bce7dd1654505df7db688cc0eee6b2cb80ac026948398419b43d44c7c7ed8ec`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Feb 2025 22:09:04 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Thu, 27 Feb 2025 22:09:04 GMT
ADD base.tar.xz / # buildkit
# Thu, 27 Feb 2025 22:09:04 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     echo 'root:!:::::::' > /etc/shadow # buildkit
# Thu, 27 Feb 2025 22:09:04 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:014817c23aa429e7621423eb3f6470f9cb2e8c4635047d07662da2986d961a89`  
		Last Modified: Mon, 03 Mar 2025 19:14:30 GMT  
		Size: 72.4 MB (72379902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79f4bb3b3bb7b800058281043f60a05d48170f5abb34f52f5111b0d61501e420`  
		Last Modified: Mon, 03 Mar 2025 19:14:29 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clearlinux:latest` - unknown; unknown

```console
$ docker pull clearlinux@sha256:2572867efa46ec81fb5eb8ca5ef24105eeb74173a56323e5dc458aa542ab1fb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 KB (6275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63fdcd3c37d777be25a4843c18bbacf11c1c7ba5f3a296d984766824981703e9`

```dockerfile
```

-	Layers:
	-	`sha256:5702fba937a01afc3c2db851ce832125b6f8965057c58d57a126102b3ee56cf2`  
		Last Modified: Mon, 03 Mar 2025 19:14:29 GMT  
		Size: 6.3 KB (6275 bytes)  
		MIME: application/vnd.in-toto+json
