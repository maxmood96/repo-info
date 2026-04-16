<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `archlinux`

-	[`archlinux:base`](#archlinuxbase)
-	[`archlinux:base-20260412.0.513370`](#archlinuxbase-202604120513370)
-	[`archlinux:base-devel`](#archlinuxbase-devel)
-	[`archlinux:base-devel-20260412.0.513370`](#archlinuxbase-devel-202604120513370)
-	[`archlinux:latest`](#archlinuxlatest)
-	[`archlinux:multilib-devel`](#archlinuxmultilib-devel)
-	[`archlinux:multilib-devel-20260412.0.513370`](#archlinuxmultilib-devel-202604120513370)

## `archlinux:base`

```console
$ docker pull archlinux@sha256:d0adc0bcc3bdfeacf9f30abd853c8d4d1dd40b6363e17cc158312a40423e063b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:9d95c7c95276ea44e5e87f4974672a91f46e38e91d60f5c342f94274f477aa40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.4 MB (129432808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0082c6f3fedcad36c9bf0b649b33b3a0d0de025080683a350e76a67122360843`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Wed, 15 Apr 2026 20:12:35 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Wed, 15 Apr 2026 20:12:35 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Wed, 15 Apr 2026 20:12:35 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Wed, 15 Apr 2026 20:12:35 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Wed, 15 Apr 2026 20:12:35 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Wed, 15 Apr 2026 20:12:35 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Wed, 15 Apr 2026 20:12:35 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Wed, 15 Apr 2026 20:12:35 GMT
LABEL org.opencontainers.image.version=20260412.0.513370
# Wed, 15 Apr 2026 20:12:35 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Wed, 15 Apr 2026 20:12:35 GMT
LABEL org.opencontainers.image.created=2026-04-12T00:06:50+00:00
# Wed, 15 Apr 2026 20:12:35 GMT
COPY /rootfs/ / # buildkit
# Wed, 15 Apr 2026 20:12:37 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260412.0.513370' /etc/os-release # buildkit
# Wed, 15 Apr 2026 20:12:37 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:12:37 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:edfbbe617b176994dfb9c35ff5c72f5a5021c1716196804101a97c25fafd913e`  
		Last Modified: Mon, 13 Apr 2026 17:47:35 GMT  
		Size: 129.4 MB (129424120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0701943b1d3aa9ce3357b7a156410dae4c3b95c95c7c079e772dbd4698e93eb4`  
		Last Modified: Wed, 15 Apr 2026 20:13:00 GMT  
		Size: 8.7 KB (8688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:6782d5c66d267b9a89529fa5fa71688700fbaf8198bd657afab980b234e6c5bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8189956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc73e76a84f653ec9c086e981cfbc2b9067bd1d21227327db159a3977f4cf918`

```dockerfile
```

-	Layers:
	-	`sha256:a85a804278e31c019eb5a80c85e1e4cd5401171c12a4d284967e8991a3c546ec`  
		Last Modified: Wed, 15 Apr 2026 20:13:01 GMT  
		Size: 8.2 MB (8178027 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ff24ba3d9f24f786acf54a6660fcc2b92dffdf9207212546844483fe417ac31`  
		Last Modified: Wed, 15 Apr 2026 20:13:00 GMT  
		Size: 11.9 KB (11929 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-20260412.0.513370`

```console
$ docker pull archlinux@sha256:d0adc0bcc3bdfeacf9f30abd853c8d4d1dd40b6363e17cc158312a40423e063b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-20260412.0.513370` - linux; amd64

```console
$ docker pull archlinux@sha256:9d95c7c95276ea44e5e87f4974672a91f46e38e91d60f5c342f94274f477aa40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.4 MB (129432808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0082c6f3fedcad36c9bf0b649b33b3a0d0de025080683a350e76a67122360843`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Wed, 15 Apr 2026 20:12:35 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Wed, 15 Apr 2026 20:12:35 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Wed, 15 Apr 2026 20:12:35 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Wed, 15 Apr 2026 20:12:35 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Wed, 15 Apr 2026 20:12:35 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Wed, 15 Apr 2026 20:12:35 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Wed, 15 Apr 2026 20:12:35 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Wed, 15 Apr 2026 20:12:35 GMT
LABEL org.opencontainers.image.version=20260412.0.513370
# Wed, 15 Apr 2026 20:12:35 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Wed, 15 Apr 2026 20:12:35 GMT
LABEL org.opencontainers.image.created=2026-04-12T00:06:50+00:00
# Wed, 15 Apr 2026 20:12:35 GMT
COPY /rootfs/ / # buildkit
# Wed, 15 Apr 2026 20:12:37 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260412.0.513370' /etc/os-release # buildkit
# Wed, 15 Apr 2026 20:12:37 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:12:37 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:edfbbe617b176994dfb9c35ff5c72f5a5021c1716196804101a97c25fafd913e`  
		Last Modified: Mon, 13 Apr 2026 17:47:35 GMT  
		Size: 129.4 MB (129424120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0701943b1d3aa9ce3357b7a156410dae4c3b95c95c7c079e772dbd4698e93eb4`  
		Last Modified: Wed, 15 Apr 2026 20:13:00 GMT  
		Size: 8.7 KB (8688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-20260412.0.513370` - unknown; unknown

```console
$ docker pull archlinux@sha256:6782d5c66d267b9a89529fa5fa71688700fbaf8198bd657afab980b234e6c5bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8189956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc73e76a84f653ec9c086e981cfbc2b9067bd1d21227327db159a3977f4cf918`

```dockerfile
```

-	Layers:
	-	`sha256:a85a804278e31c019eb5a80c85e1e4cd5401171c12a4d284967e8991a3c546ec`  
		Last Modified: Wed, 15 Apr 2026 20:13:01 GMT  
		Size: 8.2 MB (8178027 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ff24ba3d9f24f786acf54a6660fcc2b92dffdf9207212546844483fe417ac31`  
		Last Modified: Wed, 15 Apr 2026 20:13:00 GMT  
		Size: 11.9 KB (11929 bytes)  
		MIME: application/vnd.in-toto+json

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

## `archlinux:base-devel-20260412.0.513370`

```console
$ docker pull archlinux@sha256:c528201c37821ac7883af233a18eba79fbce9bd900aeae07462888a607741abe
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel-20260412.0.513370` - linux; amd64

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

### `archlinux:base-devel-20260412.0.513370` - unknown; unknown

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

## `archlinux:latest`

```console
$ docker pull archlinux@sha256:d0adc0bcc3bdfeacf9f30abd853c8d4d1dd40b6363e17cc158312a40423e063b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:9d95c7c95276ea44e5e87f4974672a91f46e38e91d60f5c342f94274f477aa40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.4 MB (129432808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0082c6f3fedcad36c9bf0b649b33b3a0d0de025080683a350e76a67122360843`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Wed, 15 Apr 2026 20:12:35 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Wed, 15 Apr 2026 20:12:35 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Wed, 15 Apr 2026 20:12:35 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Wed, 15 Apr 2026 20:12:35 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Wed, 15 Apr 2026 20:12:35 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Wed, 15 Apr 2026 20:12:35 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Wed, 15 Apr 2026 20:12:35 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Wed, 15 Apr 2026 20:12:35 GMT
LABEL org.opencontainers.image.version=20260412.0.513370
# Wed, 15 Apr 2026 20:12:35 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Wed, 15 Apr 2026 20:12:35 GMT
LABEL org.opencontainers.image.created=2026-04-12T00:06:50+00:00
# Wed, 15 Apr 2026 20:12:35 GMT
COPY /rootfs/ / # buildkit
# Wed, 15 Apr 2026 20:12:37 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260412.0.513370' /etc/os-release # buildkit
# Wed, 15 Apr 2026 20:12:37 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:12:37 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:edfbbe617b176994dfb9c35ff5c72f5a5021c1716196804101a97c25fafd913e`  
		Last Modified: Mon, 13 Apr 2026 17:47:35 GMT  
		Size: 129.4 MB (129424120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0701943b1d3aa9ce3357b7a156410dae4c3b95c95c7c079e772dbd4698e93eb4`  
		Last Modified: Wed, 15 Apr 2026 20:13:00 GMT  
		Size: 8.7 KB (8688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:latest` - unknown; unknown

```console
$ docker pull archlinux@sha256:6782d5c66d267b9a89529fa5fa71688700fbaf8198bd657afab980b234e6c5bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8189956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc73e76a84f653ec9c086e981cfbc2b9067bd1d21227327db159a3977f4cf918`

```dockerfile
```

-	Layers:
	-	`sha256:a85a804278e31c019eb5a80c85e1e4cd5401171c12a4d284967e8991a3c546ec`  
		Last Modified: Wed, 15 Apr 2026 20:13:01 GMT  
		Size: 8.2 MB (8178027 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ff24ba3d9f24f786acf54a6660fcc2b92dffdf9207212546844483fe417ac31`  
		Last Modified: Wed, 15 Apr 2026 20:13:00 GMT  
		Size: 11.9 KB (11929 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:f9b793d23b89cb123c643aa2106744ddc0142d185d3d5a7749887cb3d046826a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:504a56aed69d537dbc4713fcdf13e9e228640d4bb840dc98f4e4a1ef17d4bcc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.3 MB (269252304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec8d318d707c4570e74f786b911c178bc841b653ccd53d654fd43c6948d13e5c`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Wed, 15 Apr 2026 20:14:48 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Wed, 15 Apr 2026 20:14:48 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Wed, 15 Apr 2026 20:14:48 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Wed, 15 Apr 2026 20:14:48 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Wed, 15 Apr 2026 20:14:48 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Wed, 15 Apr 2026 20:14:48 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Wed, 15 Apr 2026 20:14:48 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Wed, 15 Apr 2026 20:14:48 GMT
LABEL org.opencontainers.image.version=20260412.0.513370
# Wed, 15 Apr 2026 20:14:48 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Wed, 15 Apr 2026 20:14:48 GMT
LABEL org.opencontainers.image.created=2026-04-12T00:06:50+00:00
# Wed, 15 Apr 2026 20:14:48 GMT
COPY /rootfs/ / # buildkit
# Wed, 15 Apr 2026 20:14:54 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260412.0.513370' /etc/os-release # buildkit
# Wed, 15 Apr 2026 20:14:54 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:14:54 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:58f17d36b1f875da33d63bcf8aca97555ff01fd66e8541aa5ba8046f40f02bde`  
		Last Modified: Mon, 13 Apr 2026 17:49:04 GMT  
		Size: 269.2 MB (269241935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6715389c3c30f1c8a355b1df8f844c5e3dacb1ddc36f042bd90533848d9cc95d`  
		Last Modified: Wed, 15 Apr 2026 20:15:39 GMT  
		Size: 10.4 KB (10369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:85e7aa73ed5ebd91b18de8e0841c0fe40ef5cf338b692bd7015a739c7ffdad7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12246414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8822b03ae05742dd5f83f716bd647976bda299429cc2d002728f84cab6f9e3b5`

```dockerfile
```

-	Layers:
	-	`sha256:a02d7474b59935c8137e1e12f105713ac8f714f88fa0cd4ca0dc9eead32fe78f`  
		Last Modified: Wed, 15 Apr 2026 20:15:40 GMT  
		Size: 12.2 MB (12234646 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:baf76508a559f2e70a7f6b6853ce6471268959406b5ca1e7a9fcbca9b62e9799`  
		Last Modified: Wed, 15 Apr 2026 20:15:40 GMT  
		Size: 11.8 KB (11768 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel-20260412.0.513370`

```console
$ docker pull archlinux@sha256:f9b793d23b89cb123c643aa2106744ddc0142d185d3d5a7749887cb3d046826a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel-20260412.0.513370` - linux; amd64

```console
$ docker pull archlinux@sha256:504a56aed69d537dbc4713fcdf13e9e228640d4bb840dc98f4e4a1ef17d4bcc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.3 MB (269252304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec8d318d707c4570e74f786b911c178bc841b653ccd53d654fd43c6948d13e5c`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Wed, 15 Apr 2026 20:14:48 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Wed, 15 Apr 2026 20:14:48 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Wed, 15 Apr 2026 20:14:48 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Wed, 15 Apr 2026 20:14:48 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Wed, 15 Apr 2026 20:14:48 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Wed, 15 Apr 2026 20:14:48 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Wed, 15 Apr 2026 20:14:48 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Wed, 15 Apr 2026 20:14:48 GMT
LABEL org.opencontainers.image.version=20260412.0.513370
# Wed, 15 Apr 2026 20:14:48 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Wed, 15 Apr 2026 20:14:48 GMT
LABEL org.opencontainers.image.created=2026-04-12T00:06:50+00:00
# Wed, 15 Apr 2026 20:14:48 GMT
COPY /rootfs/ / # buildkit
# Wed, 15 Apr 2026 20:14:54 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260412.0.513370' /etc/os-release # buildkit
# Wed, 15 Apr 2026 20:14:54 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:14:54 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:58f17d36b1f875da33d63bcf8aca97555ff01fd66e8541aa5ba8046f40f02bde`  
		Last Modified: Mon, 13 Apr 2026 17:49:04 GMT  
		Size: 269.2 MB (269241935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6715389c3c30f1c8a355b1df8f844c5e3dacb1ddc36f042bd90533848d9cc95d`  
		Last Modified: Wed, 15 Apr 2026 20:15:39 GMT  
		Size: 10.4 KB (10369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel-20260412.0.513370` - unknown; unknown

```console
$ docker pull archlinux@sha256:85e7aa73ed5ebd91b18de8e0841c0fe40ef5cf338b692bd7015a739c7ffdad7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12246414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8822b03ae05742dd5f83f716bd647976bda299429cc2d002728f84cab6f9e3b5`

```dockerfile
```

-	Layers:
	-	`sha256:a02d7474b59935c8137e1e12f105713ac8f714f88fa0cd4ca0dc9eead32fe78f`  
		Last Modified: Wed, 15 Apr 2026 20:15:40 GMT  
		Size: 12.2 MB (12234646 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:baf76508a559f2e70a7f6b6853ce6471268959406b5ca1e7a9fcbca9b62e9799`  
		Last Modified: Wed, 15 Apr 2026 20:15:40 GMT  
		Size: 11.8 KB (11768 bytes)  
		MIME: application/vnd.in-toto+json
