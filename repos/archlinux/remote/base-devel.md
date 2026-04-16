## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:c528201c37821ac7883af233a18eba79fbce9bd900aeae07462888a607741abe
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:5d566859254d6e7bab01fe4c84b3c34225635fd7325997a20d1dcfe070ec4012
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.1 MB (247090930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1d6752db797d0c58355267abfc01676c4de55605ea4e0347eec28521d2bbe0c`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Wed, 15 Apr 2026 20:13:30 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Wed, 15 Apr 2026 20:13:30 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Wed, 15 Apr 2026 20:13:30 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Wed, 15 Apr 2026 20:13:30 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Wed, 15 Apr 2026 20:13:30 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Wed, 15 Apr 2026 20:13:30 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Wed, 15 Apr 2026 20:13:30 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Wed, 15 Apr 2026 20:13:30 GMT
LABEL org.opencontainers.image.version=20260412.0.513370
# Wed, 15 Apr 2026 20:13:30 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Wed, 15 Apr 2026 20:13:30 GMT
LABEL org.opencontainers.image.created=2026-04-12T00:06:50+00:00
# Wed, 15 Apr 2026 20:13:30 GMT
COPY /rootfs/ / # buildkit
# Wed, 15 Apr 2026 20:13:35 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260412.0.513370' /etc/os-release # buildkit
# Wed, 15 Apr 2026 20:13:35 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:13:35 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:5c1f30f5a8968675635fdbe2ce53d92208401558240cf52fcdaf22993ac0aaca`  
		Last Modified: Mon, 13 Apr 2026 17:49:09 GMT  
		Size: 247.1 MB (247081762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:523280c44e7faa57b0d2d5cb35be382177a90d8c331dce34893b214ad76af178`  
		Last Modified: Wed, 15 Apr 2026 20:14:17 GMT  
		Size: 9.2 KB (9168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:8218774c140b512b8b4219cdd5bb256b040b058c6e4fe4edf98f93a0a7a257f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.0 MB (11976487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4acd59f8199b91219b75287adad2a4a589c4d8de00018d6f68bebc8008fbf5e9`

```dockerfile
```

-	Layers:
	-	`sha256:89280d33137b311d2821b31e2d98fb36ed029f6436f92adc22e4fed1ad4370cd`  
		Last Modified: Wed, 15 Apr 2026 20:14:17 GMT  
		Size: 12.0 MB (11964776 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:756b40acbb75c4ba1965694c098d12de89622ca535b5fcd6d7a079ce52123bb2`  
		Last Modified: Wed, 15 Apr 2026 20:14:17 GMT  
		Size: 11.7 KB (11711 bytes)  
		MIME: application/vnd.in-toto+json
