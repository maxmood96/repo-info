## `clearlinux:latest`

```console
$ docker pull clearlinux@sha256:18a3b4f23d1efa72c6cd23f07d7d766b8883b645c441aa07d387585101f487a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:latest` - linux; amd64

```console
$ docker pull clearlinux@sha256:7f6a22969f8ecfb38143351ae294279112c3f14347bac8bcc3ada7256b2225c9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.8 MB (94752626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4b4d8ceb6ae982efd06cdfc00da8e02fe1577ba52158e49818724f1ba59eeee`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Mar 2021 00:22:54 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Tue, 05 Jul 2022 19:22:24 GMT
ADD file:601986a38401d048b2cb5eecf0521178198311e5acc32f2ab8ee6423e9f9b000 in / 
# Tue, 05 Jul 2022 19:22:25 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     grep root /usr/share/defaults/etc/shadow > /etc/shadow
# Tue, 05 Jul 2022 19:22:25 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:2eac17aeb9c40dd02d1192e2800dd1b2f4f8641b176c7acda5fa87c05645687e`  
		Last Modified: Tue, 05 Jul 2022 19:22:52 GMT  
		Size: 94.8 MB (94752409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71e7cdfb90ff80e83e0a51883de9529ffae0dbc94ff5bf54ab8f06b0820e5142`  
		Last Modified: Tue, 05 Jul 2022 19:22:38 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
