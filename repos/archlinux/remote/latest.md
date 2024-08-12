## `archlinux:latest`

```console
$ docker pull archlinux@sha256:271083843fa6569f02dfc78b2bab94fce8d705c8aa9d581fc838437930ed977b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:9ce68291a5781e56550e15a02a17d1b96f0ec27a3868b9db497b35999876afb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.2 MB (151159668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f475d1d5e29bed7d90cbc70f34b8da466f942d649bdf21d3f28c45e96124d166`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 11 Aug 2024 00:07:52 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 11 Aug 2024 00:07:52 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 11 Aug 2024 00:07:52 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 11 Aug 2024 00:07:52 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 11 Aug 2024 00:07:52 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 11 Aug 2024 00:07:52 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 11 Aug 2024 00:07:52 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 11 Aug 2024 00:07:52 GMT
LABEL org.opencontainers.image.version=20240811.0.253648
# Sun, 11 Aug 2024 00:07:52 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 11 Aug 2024 00:07:52 GMT
LABEL org.opencontainers.image.created=2024-08-11T00:07:52+00:00
# Sun, 11 Aug 2024 00:07:52 GMT
COPY /rootfs/ / # buildkit
# Sun, 11 Aug 2024 00:07:52 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20240811.0.253648' /etc/os-release # buildkit
# Sun, 11 Aug 2024 00:07:52 GMT
ENV LANG=C.UTF-8
# Sun, 11 Aug 2024 00:07:52 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:41b97f57fdb9eda7d32a74c17046812257d854ea5fc34380b033a53f66b80190`  
		Last Modified: Mon, 12 Aug 2024 16:56:31 GMT  
		Size: 151.2 MB (151151362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eff8d7dad74c783bba3d3e4f5c92ffd8353c6167149683f41670239942a3e52`  
		Last Modified: Mon, 12 Aug 2024 16:56:29 GMT  
		Size: 8.3 KB (8306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:latest` - unknown; unknown

```console
$ docker pull archlinux@sha256:98969c9c385675332f7db299be43a7276a2726f32474561b3508156f657b098d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8115650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20d7e2b0beaf1a1649c859c1a21e7a92add0cd8263d9f962bb89b549d5dbbd2e`

```dockerfile
```

-	Layers:
	-	`sha256:59e2c175a479dcb6e2f89efe40e5fb53adae76e41a4f296c3c8245d40e78a76b`  
		Last Modified: Mon, 12 Aug 2024 16:56:30 GMT  
		Size: 8.1 MB (8103929 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96baec7823e60d53894e6d9920ded7076830ac276a86fea35a85d99dd75dfafb`  
		Last Modified: Mon, 12 Aug 2024 16:56:30 GMT  
		Size: 11.7 KB (11721 bytes)  
		MIME: application/vnd.in-toto+json
