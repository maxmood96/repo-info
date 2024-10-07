## `archlinux:base-devel-20241006.0.268140`

```console
$ docker pull archlinux@sha256:7005fdc99327fc48e89005dd615cf60841946d1d5ccb27eb6abb860fd8d103a2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel-20241006.0.268140` - linux; amd64

```console
$ docker pull archlinux@sha256:898bf8a910407b6cda843b358b13f67ecb4344ab367a0043ea57fd29951ccc94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.2 MB (272195562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:183fc87f7e6f523b82ef186d6a61acb54e95a40e7b21749a7a46100d0482679d`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 06 Oct 2024 00:07:56 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 06 Oct 2024 00:07:56 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 06 Oct 2024 00:07:56 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 06 Oct 2024 00:07:56 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 06 Oct 2024 00:07:56 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 06 Oct 2024 00:07:56 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 06 Oct 2024 00:07:56 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 06 Oct 2024 00:07:56 GMT
LABEL org.opencontainers.image.version=20241006.0.268140
# Sun, 06 Oct 2024 00:07:56 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 06 Oct 2024 00:07:56 GMT
LABEL org.opencontainers.image.created=2024-10-06T00:07:56+00:00
# Sun, 06 Oct 2024 00:07:56 GMT
COPY /rootfs/ / # buildkit
# Sun, 06 Oct 2024 00:07:56 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20241006.0.268140' /etc/os-release # buildkit
# Sun, 06 Oct 2024 00:07:56 GMT
ENV LANG=C.UTF-8
# Sun, 06 Oct 2024 00:07:56 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:847aa64f2f293bb49d2b17e764ee9200d747a883b79d54a1c994d479035f926a`  
		Last Modified: Mon, 07 Oct 2024 19:59:05 GMT  
		Size: 272.2 MB (272186561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:690b067d888f599b2c2f8c93f736614865740a49ac55d01c4230aebd2def3a8e`  
		Last Modified: Mon, 07 Oct 2024 19:59:02 GMT  
		Size: 9.0 KB (9001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel-20241006.0.268140` - unknown; unknown

```console
$ docker pull archlinux@sha256:3f87eb8f85cccbad4d90363d6971e9db4a5f152908fd57b3fe3700933cfe2274
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.9 MB (11912075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adfdfbf7ec3224a6c79ae6a593230a595f528c14dba4d90e6dfdd641bbdb0012`

```dockerfile
```

-	Layers:
	-	`sha256:dc642c6e736f6172f840f026d90bf885f37c835fbb2335200850d3820b8d86a1`  
		Last Modified: Mon, 07 Oct 2024 19:59:02 GMT  
		Size: 11.9 MB (11900567 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e8d5db069b498c291ebdfc756604a1c6db842c359f2d89f6dae7e12b7761400`  
		Last Modified: Mon, 07 Oct 2024 19:59:02 GMT  
		Size: 11.5 KB (11508 bytes)  
		MIME: application/vnd.in-toto+json
