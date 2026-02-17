## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:f7c8aff548bd590bcf6c4b53e0d6dee711e6da52f4ee9e75959e195251e98637
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:0a97b836b7baa8a78ac87d4c636f002fad5caf20c89f782c94e23aa742053948
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.0 MB (267974118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a08bd07a0428d372cd6129c0e386cc9389b24d011a12f0b1579d02ded0752ee4`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Tue, 17 Feb 2026 18:12:27 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Tue, 17 Feb 2026 18:12:27 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Tue, 17 Feb 2026 18:12:27 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Tue, 17 Feb 2026 18:12:27 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Tue, 17 Feb 2026 18:12:27 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Tue, 17 Feb 2026 18:12:27 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Tue, 17 Feb 2026 18:12:27 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Tue, 17 Feb 2026 18:12:27 GMT
LABEL org.opencontainers.image.version=20260215.0.490969
# Tue, 17 Feb 2026 18:12:27 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Tue, 17 Feb 2026 18:12:27 GMT
LABEL org.opencontainers.image.created=2026-02-15T00:06:54+00:00
# Tue, 17 Feb 2026 18:12:27 GMT
COPY /rootfs/ / # buildkit
# Tue, 17 Feb 2026 18:12:33 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260215.0.490969' /etc/os-release # buildkit
# Tue, 17 Feb 2026 18:12:33 GMT
ENV LANG=C.UTF-8
# Tue, 17 Feb 2026 18:12:33 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:f5acad426fd0c8126c49ed2eee9bd51ed358460059421e9c596fad49547ffde9`  
		Last Modified: Tue, 17 Feb 2026 18:13:22 GMT  
		Size: 268.0 MB (267963820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83e2adf10a195d94a1ae1215fbd8f09cc1bd0eb475a4c040015d8c0f969202a3`  
		Last Modified: Tue, 17 Feb 2026 18:13:16 GMT  
		Size: 10.3 KB (10298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:bb73fb599efcf64181205e95c034e3afdb43175d4b133c66dc5e55247e696693
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.5 MB (12503554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c11ed0a1b2e5736033f663cba6f81d6494d8b92c4ff43ae72e737e7ffa52b132`

```dockerfile
```

-	Layers:
	-	`sha256:b48e8385a988ff8b589c4afac6ee025d1c7d36404cc90b62f8b08f382f765620`  
		Last Modified: Tue, 17 Feb 2026 18:13:17 GMT  
		Size: 12.5 MB (12491786 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e684cb327c93a3da56d43647df9a4e2e1981bd6008fdcc6f1a229560184ecd0`  
		Last Modified: Tue, 17 Feb 2026 18:13:16 GMT  
		Size: 11.8 KB (11768 bytes)  
		MIME: application/vnd.in-toto+json
