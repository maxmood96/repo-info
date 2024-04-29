## `clearlinux:latest`

```console
$ docker pull clearlinux@sha256:ab6ab877fc09e50760ae638edfbe6f0b1b1a1868c04de6365f1518c14943aae8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:latest` - linux; amd64

```console
$ docker pull clearlinux@sha256:84d8ae90bc2698ef42215e7cc766d7b806168853ed07ab0a7a310b8e429604a6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.1 MB (69061782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac0183b5ff5dcf9b3b04fa3632eebd33e321308f55330d6ea69e874a1497a2c9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Mar 2021 00:22:54 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Mon, 29 Apr 2024 18:40:51 GMT
ADD file:aa9ada014db689d2d9c966e686a206f5ed21cb545c127c2e569d68c0754dee35 in / 
# Mon, 29 Apr 2024 18:40:52 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     echo 'root:!:::::::' > /etc/shadow
# Mon, 29 Apr 2024 18:40:53 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:0256d3543e0180eaf70c1408705f6156a68dce2a9e5cdd312b91c5954fdea202`  
		Last Modified: Mon, 29 Apr 2024 18:41:09 GMT  
		Size: 69.1 MB (69061572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91172b49fdeb690edfd53566844b9f9d481979f894fb53fdacd18fcdfbd0a036`  
		Last Modified: Mon, 29 Apr 2024 18:41:01 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
