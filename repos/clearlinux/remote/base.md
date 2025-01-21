## `clearlinux:base`

```console
$ docker pull clearlinux@sha256:62a6a9b47791fbe162024213d4f26fd1b3546108c26d1e5e020c87ee5aa574c4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `clearlinux:base` - linux; amd64

```console
$ docker pull clearlinux@sha256:4e718ee34aabcbde3b26e8b250e50f8475520199f46a7564f67e31343647756a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.1 MB (72137333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af5337d5e11a1166c9e51727dc932f40667f3f92af343bfb71b5532c4f294097`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 17 Jan 2025 03:55:12 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Fri, 17 Jan 2025 03:55:12 GMT
ADD base.tar.xz / # buildkit
# Fri, 17 Jan 2025 03:55:12 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     echo 'root:!:::::::' > /etc/shadow # buildkit
# Fri, 17 Jan 2025 03:55:12 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:edacd45727e8265d4fab4d17e2366f261dedb044a3f3767e44e1de153c305e70`  
		Last Modified: Tue, 21 Jan 2025 19:28:25 GMT  
		Size: 72.1 MB (72137119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81c532e5d36b192e6de9bfdfbfb3ec3da1e03afffc13f24692f26b3c748d647c`  
		Last Modified: Tue, 21 Jan 2025 19:28:22 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clearlinux:base` - unknown; unknown

```console
$ docker pull clearlinux@sha256:fa7652efe9532585d17721452a0eff0ef86867f70abfa6811cf5eb86cbf851da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 KB (6275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:672004c819de86d52e23dc30b81a85e91b2ff34b143f12f9d5d445d566e7c393`

```dockerfile
```

-	Layers:
	-	`sha256:0421ea82d4f1dedeaf1c2abf271a9318fabcadf3479c9bb69afca3e40d4a0903`  
		Last Modified: Tue, 21 Jan 2025 19:28:22 GMT  
		Size: 6.3 KB (6275 bytes)  
		MIME: application/vnd.in-toto+json
