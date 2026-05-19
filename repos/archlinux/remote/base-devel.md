## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:6db772fd1dd128b9cf7b7231ca5284af70879596fe4ec754c911cfc4ac30d5eb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:bb2334c57045a9cbb6e5f6f968f40096da5ab3ae4ff26d0d9711c18d39d45619
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.6 MB (303602635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:390cd713630c6ceb7d3e7b1b747f1b706f0599d2898001ba751a57b4092e17d6`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 18 May 2026 21:50:49 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Mon, 18 May 2026 21:50:49 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 18 May 2026 21:50:49 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 18 May 2026 21:50:49 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 18 May 2026 21:50:49 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 18 May 2026 21:50:49 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 18 May 2026 21:50:49 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 18 May 2026 21:50:49 GMT
LABEL org.opencontainers.image.version=20260517.0.530531
# Mon, 18 May 2026 21:50:49 GMT
LABEL org.opencontainers.image.revision=34b87485162b028c8d957bdcd2674359d883cd21
# Mon, 18 May 2026 21:50:49 GMT
LABEL org.opencontainers.image.created=2026-05-17T00:09:11+00:00
# Mon, 18 May 2026 21:50:49 GMT
COPY /rootfs/ / # buildkit
# Mon, 18 May 2026 21:50:56 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260517.0.530531' /etc/os-release # buildkit
# Mon, 18 May 2026 21:50:56 GMT
ENV LANG=C.UTF-8
# Mon, 18 May 2026 21:50:56 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:60247dd0c17be857b345faa90691b432a692e6d507a510cf6c303e9c7453603a`  
		Last Modified: Mon, 18 May 2026 21:51:53 GMT  
		Size: 303.6 MB (303591223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44b3c8b03ba73dd39003da39223aad555ebb2b47af6d9f3500ac750256e93cbf`  
		Last Modified: Mon, 18 May 2026 21:51:46 GMT  
		Size: 11.4 KB (11412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:8495108c9aae6056b06b96ec8073d93f57bc42bca539de78c704dfd46a770bf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 MB (14396280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8505bca8b9f0c1f4f6a37eaee1708d818279f357eb122ce72d2189e1cc2375d9`

```dockerfile
```

-	Layers:
	-	`sha256:1bb047cf7fa0bf72881d5bab8c52f8814ab631d5d18179fc9e17d82efec0dae0`  
		Last Modified: Mon, 18 May 2026 21:51:47 GMT  
		Size: 14.4 MB (14384568 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c9a4fed6043e0ddd78c9923228a14dfcdc3adbef21fbeb325d04ac8a6e99089`  
		Last Modified: Mon, 18 May 2026 21:51:46 GMT  
		Size: 11.7 KB (11712 bytes)  
		MIME: application/vnd.in-toto+json
