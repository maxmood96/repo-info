## `clearlinux:latest`

```console
$ docker pull clearlinux@sha256:93a77268d454e485efabd50298424b99473137746639b08fd2a99270b3a82456
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:latest` - linux; amd64

```console
$ docker pull clearlinux@sha256:44f654ec37342e04269532404379778a422454d82c49bff7fd2925685e2d21b6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.6 MB (91571919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:429f8ca5d785f3c834d1abb8be955b8ab0dbfdd2220c3c33cacf09ca5de803fb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Mar 2021 00:22:54 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Tue, 17 Jan 2023 20:26:25 GMT
ADD file:02500b6bf0e2d9f61fefddb114f098eff218bd3982eb13d37ba644e7cf9c4083 in / 
# Tue, 17 Jan 2023 20:26:27 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     grep root /usr/share/defaults/etc/shadow > /etc/shadow
# Tue, 17 Jan 2023 20:26:27 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:fad672096b8fd6a8de15088ebee1b22f9f55f621e7dcd7f22ed0a9fbce07aef2`  
		Last Modified: Tue, 17 Jan 2023 20:26:48 GMT  
		Size: 91.6 MB (91571701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:848c119bffc5a4046a0c687cbcd2cacc880fb927599e790316e45985157c08ab`  
		Last Modified: Tue, 17 Jan 2023 20:26:36 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
