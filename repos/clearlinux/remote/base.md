## `clearlinux:base`

```console
$ docker pull clearlinux@sha256:01fc5ea57e24b7825cd9034c8df85575e0f461b9074105a85e3129c7a4b760f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:base` - linux; amd64

```console
$ docker pull clearlinux@sha256:234930b3ef20dfda05086a19ec5e5d0f5f4cd7c6fc8ded4d75a0aaaaa1e17c23
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.8 MB (68783250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d25c792b22134369ab4889f9ee5083b84effad564ad0d36475283a39c42c17c3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Mar 2021 00:22:54 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Mon, 03 Oct 2022 21:26:21 GMT
ADD file:a6f08fb9b32779c881ddc7b6f7185bebbe91b42e5b7e5feb22f46cb73e487642 in / 
# Mon, 03 Oct 2022 21:26:22 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     grep root /usr/share/defaults/etc/shadow > /etc/shadow
# Mon, 03 Oct 2022 21:26:22 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:c0a2afcf4dd43a438edaee2ada845a523591932a2b65f1ec60e704a83b8599de`  
		Last Modified: Mon, 03 Oct 2022 21:26:44 GMT  
		Size: 68.8 MB (68783032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c54004836780bd1b4eb0318f043f9d14a18a54ad6721b97edc5a910f2997d340`  
		Last Modified: Mon, 03 Oct 2022 21:26:34 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
