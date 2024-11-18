## `archlinux:multilib-devel-20241117.0.280007`

```console
$ docker pull archlinux@sha256:71c9b81ecb343d10bb75aab8daf7deec25372f5f65488adc8481a6543e35432c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel-20241117.0.280007` - linux; amd64

```console
$ docker pull archlinux@sha256:ed22ca153e83fa62a2d20da071e35a466d57712c531a333efffe9066f54833e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.3 MB (322304184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0238fe4342e6ad0b556c499c57efdce516d709ff060f57f8c76065473cad192b`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 17 Nov 2024 00:08:06 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 17 Nov 2024 00:08:06 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 17 Nov 2024 00:08:06 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 17 Nov 2024 00:08:06 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 17 Nov 2024 00:08:06 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 17 Nov 2024 00:08:06 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 17 Nov 2024 00:08:06 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 17 Nov 2024 00:08:06 GMT
LABEL org.opencontainers.image.version=20241117.0.280007
# Sun, 17 Nov 2024 00:08:06 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 17 Nov 2024 00:08:06 GMT
LABEL org.opencontainers.image.created=2024-11-17T00:08:06+00:00
# Sun, 17 Nov 2024 00:08:06 GMT
COPY /rootfs/ / # buildkit
# Sun, 17 Nov 2024 00:08:06 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20241117.0.280007' /etc/os-release # buildkit
# Sun, 17 Nov 2024 00:08:06 GMT
ENV LANG=C.UTF-8
# Sun, 17 Nov 2024 00:08:06 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:bc3a3f8d212d78a51736400db0f99c87929fecb779492a3ab85f465087fee5b1`  
		Last Modified: Mon, 18 Nov 2024 19:06:43 GMT  
		Size: 322.3 MB (322293956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b58bd3f7846a9afc0bb13ac63948cee775ace6dc94031e913c57f13b79eecaa`  
		Last Modified: Mon, 18 Nov 2024 19:06:35 GMT  
		Size: 10.2 KB (10228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel-20241117.0.280007` - unknown; unknown

```console
$ docker pull archlinux@sha256:3082c9babb0fa9c04d667f7f881babe90fce18e3fada33182b57b54871237c48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12176307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35db4ac340f9b4d1a12c6c579cecbd8b8a8ed1c0e31920fb267ad05e3bd5a71d`

```dockerfile
```

-	Layers:
	-	`sha256:33d959197b31181beaace8d3e8d66fbc84b8ac82d440cdf01c8a521437739846`  
		Last Modified: Mon, 18 Nov 2024 19:06:36 GMT  
		Size: 12.2 MB (12164496 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ff1c36045df7445ea2b09130c539b2cfd0412ed4e49bf7358ab0bbab0c9e86c`  
		Last Modified: Mon, 18 Nov 2024 19:06:35 GMT  
		Size: 11.8 KB (11811 bytes)  
		MIME: application/vnd.in-toto+json
