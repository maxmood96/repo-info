## `archlinux:latest`

```console
$ docker pull archlinux@sha256:e0cdf8208d276f77eaba78e1ef0e94f7a70c15090cfc09299be5521ceb4a0705
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:2fe50139e8eff5be59fffa698e09003df948e655a3fd4e841b15e858e4982ecf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.0 MB (147995421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:350179b164059944a654dfab989fddbb68a8e857dacc97777e3b625aa418155b`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.version=20240101.0.204074
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.revision=98cd79111dd530447f491d547d14f3c38e227e46
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.created=2024-01-01T19:08:40+00:00
# Mon, 01 Jan 2024 19:08:40 GMT
COPY /rootfs/ / # buildkit
# Mon, 01 Jan 2024 19:08:40 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20240101.0.204074' /etc/os-release # buildkit
# Mon, 01 Jan 2024 19:08:40 GMT
ENV LANG=C.UTF-8
# Mon, 01 Jan 2024 19:08:40 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:d9884827b07bb5df1be9734d10e7db68899aedbb38552f40a11adf399debdaaf`  
		Last Modified: Wed, 08 May 2024 21:11:13 GMT  
		Size: 148.0 MB (147987269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bc4fe693d3a172aaa30338898d9358941319d1114416838bbdc38e762ece972`  
		Last Modified: Wed, 29 May 2024 19:56:56 GMT  
		Size: 8.2 KB (8152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:latest` - unknown; unknown

```console
$ docker pull archlinux@sha256:4bfed7edac7290affed5bd244ee801be39a21a77d6720c8fba25f2244edfc1f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7813966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6adf6ab28a1db76d18f8e5817bd69b096ff53792075f2c4e6bdcac25fcbba85`

```dockerfile
```

-	Layers:
	-	`sha256:af2795535157dbf5923f794df4a6b3287816159811c94c924a62e2fb96ade8f1`  
		Last Modified: Wed, 29 May 2024 19:56:56 GMT  
		Size: 7.8 MB (7802294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:842e8ca534a4db9ef4c4f93594e2291833dde88df585ed57339c67f8e805bd7d`  
		Last Modified: Wed, 29 May 2024 19:56:56 GMT  
		Size: 11.7 KB (11672 bytes)  
		MIME: application/vnd.in-toto+json
