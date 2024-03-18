## `clearlinux:latest`

```console
$ docker pull clearlinux@sha256:0f27ae2a2c9b9e6230930c2746c606ba1f771bfc2b131df9ca0c4e35281b797f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:latest` - linux; amd64

```console
$ docker pull clearlinux@sha256:7792ff89fa60f0084fd81d14ec53c0569fa0143dcdfd49b6aa8a03cd8d4e4ff4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.4 MB (65363050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62d10f9aa47d7d81939e72da3fdd0a3361e80f4160121203090e43b4b2f9f07c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Mar 2021 00:22:54 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Mon, 18 Mar 2024 19:48:23 GMT
ADD file:e46231c13a95ffaa67b4a0086c9014821cc3aef3a56a5a9463ba929bce2e3d92 in / 
# Mon, 18 Mar 2024 19:48:24 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     echo 'root:!:::::::' > /etc/shadow
# Mon, 18 Mar 2024 19:48:24 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:4577296588cd31661f312af1c190842102d6602016dc1eab59dd67658465a22d`  
		Last Modified: Mon, 18 Mar 2024 19:48:42 GMT  
		Size: 65.4 MB (65362838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa20eb9cec9c0811c348c8de60b2ce1db9321ca79dcedd5b0c07857b2b72c7bf`  
		Last Modified: Mon, 18 Mar 2024 19:48:33 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
