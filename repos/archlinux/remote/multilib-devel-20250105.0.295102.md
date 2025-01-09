## `archlinux:multilib-devel-20250105.0.295102`

```console
$ docker pull archlinux@sha256:bad5c9c74cbbae376f711c1a420161e1d3245a84753cae0fc696c512c1cc631c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel-20250105.0.295102` - linux; amd64

```console
$ docker pull archlinux@sha256:540bace3cceebdff27645b3c5e802740e64d24d2a3391d217193c3b094f3b662
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.1 MB (324062560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c4a8b7bf79e579d6cc2f025e8164ee73f5d15c859200d5b058baf329ce50024`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 05 Jan 2025 00:08:06 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 05 Jan 2025 00:08:06 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 05 Jan 2025 00:08:06 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 05 Jan 2025 00:08:06 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 05 Jan 2025 00:08:06 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 05 Jan 2025 00:08:06 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 05 Jan 2025 00:08:06 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 05 Jan 2025 00:08:06 GMT
LABEL org.opencontainers.image.version=20250105.0.295102
# Sun, 05 Jan 2025 00:08:06 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 05 Jan 2025 00:08:06 GMT
LABEL org.opencontainers.image.created=2025-01-05T00:08:06+00:00
# Sun, 05 Jan 2025 00:08:06 GMT
COPY /rootfs/ / # buildkit
# Sun, 05 Jan 2025 00:08:06 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250105.0.295102' /etc/os-release # buildkit
# Sun, 05 Jan 2025 00:08:06 GMT
ENV LANG=C.UTF-8
# Sun, 05 Jan 2025 00:08:06 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:35f18d87fe1c34fb6189104a5557fc7dd308f8df7e0bb81cf374e2a2d3b7c8a2`  
		Last Modified: Tue, 07 Jan 2025 01:30:06 GMT  
		Size: 324.1 MB (324052296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9737da604a768aeb1ca922987f580ce649f9f6056360e6d8b88f3cc3c346f2f`  
		Last Modified: Wed, 08 Jan 2025 17:58:57 GMT  
		Size: 10.3 KB (10264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel-20250105.0.295102` - unknown; unknown

```console
$ docker pull archlinux@sha256:2cc23c3f4e4b885063bd6061c07cd1b12cffae55c5b72418f3639d19177f75d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12176633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef6521468393f2402bde55557aea3baa3e2be4a08f77f4d6c313760798b30d64`

```dockerfile
```

-	Layers:
	-	`sha256:00b524be2472347852dcd7b062f18ea0bef952c808f4b6ba838d9a2d625c5005`  
		Last Modified: Wed, 08 Jan 2025 17:58:57 GMT  
		Size: 12.2 MB (12164822 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:772b8278c459c08e0e08e5d4a85a958232a2014fa4099bc7d4ea38b729517b6f`  
		Last Modified: Wed, 08 Jan 2025 17:58:57 GMT  
		Size: 11.8 KB (11811 bytes)  
		MIME: application/vnd.in-toto+json
