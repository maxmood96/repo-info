<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `archlinux`

-	[`archlinux:base`](#archlinuxbase)
-	[`archlinux:base-20260524.0.535079`](#archlinuxbase-202605240535079)
-	[`archlinux:base-devel`](#archlinuxbase-devel)
-	[`archlinux:base-devel-20260524.0.535079`](#archlinuxbase-devel-202605240535079)
-	[`archlinux:latest`](#archlinuxlatest)
-	[`archlinux:multilib-devel`](#archlinuxmultilib-devel)
-	[`archlinux:multilib-devel-20260524.0.535079`](#archlinuxmultilib-devel-202605240535079)

## `archlinux:base`

```console
$ docker pull archlinux@sha256:1047e6e7878d58e4ee47e1cd6459a32fab41246b0efc4109e11b7ef16f50b14d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:42215a8ac2213d27d2bebd539737196b1bcea14382c375a5ff5a166408074fab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.5 MB (131531164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95026cd5ba836e50589e3ccf1ebabddc5ca562e8e27c1dcddbbc7e140cf58c8b`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 18 May 2026 21:49:13 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Mon, 18 May 2026 21:49:13 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 18 May 2026 21:49:13 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 18 May 2026 21:49:13 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 18 May 2026 21:49:13 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 18 May 2026 21:49:13 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 18 May 2026 21:49:13 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 18 May 2026 21:49:13 GMT
LABEL org.opencontainers.image.version=20260517.0.530531
# Mon, 18 May 2026 21:49:13 GMT
LABEL org.opencontainers.image.revision=34b87485162b028c8d957bdcd2674359d883cd21
# Mon, 18 May 2026 21:49:13 GMT
LABEL org.opencontainers.image.created=2026-05-17T00:09:11+00:00
# Mon, 18 May 2026 21:49:13 GMT
COPY /rootfs/ / # buildkit
# Mon, 18 May 2026 21:49:15 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260517.0.530531' /etc/os-release # buildkit
# Mon, 18 May 2026 21:49:15 GMT
ENV LANG=C.UTF-8
# Mon, 18 May 2026 21:49:15 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:54b8626685668f7f8af95a079ff42364fac0252de2e6a4080bf1ae6363bc1f18`  
		Last Modified: Mon, 18 May 2026 21:49:47 GMT  
		Size: 131.5 MB (131522499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6d2dac6ee5f200ecc82f8cbeaebb86261dca5de1552b71a47a953c6d2ba2e7f`  
		Last Modified: Mon, 18 May 2026 21:49:39 GMT  
		Size: 8.7 KB (8665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:e01962c564f0d3c980a949782a4558a51a1599a0b786394e2d244958728a2905
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8193065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81c72c339fb8f01e8e158d7fe54967e96c09ba91ac985e6ef09dad3b36484673`

```dockerfile
```

-	Layers:
	-	`sha256:688e0a39cb99915dc563d9588850c7d3b3543dd9286cf2793eb7ad1a5b6b68a8`  
		Last Modified: Mon, 18 May 2026 21:49:39 GMT  
		Size: 8.2 MB (8181137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e261ca3733559df04d34bc4ea600670046a2ee9bb08854de1ecd8dcd577ba5a2`  
		Last Modified: Mon, 18 May 2026 21:49:39 GMT  
		Size: 11.9 KB (11928 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-20260524.0.535079`

**does not exist** (yet?)

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

## `archlinux:base-devel-20260524.0.535079`

**does not exist** (yet?)

## `archlinux:latest`

```console
$ docker pull archlinux@sha256:1047e6e7878d58e4ee47e1cd6459a32fab41246b0efc4109e11b7ef16f50b14d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:42215a8ac2213d27d2bebd539737196b1bcea14382c375a5ff5a166408074fab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.5 MB (131531164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95026cd5ba836e50589e3ccf1ebabddc5ca562e8e27c1dcddbbc7e140cf58c8b`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 18 May 2026 21:49:13 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Mon, 18 May 2026 21:49:13 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 18 May 2026 21:49:13 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 18 May 2026 21:49:13 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 18 May 2026 21:49:13 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 18 May 2026 21:49:13 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 18 May 2026 21:49:13 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 18 May 2026 21:49:13 GMT
LABEL org.opencontainers.image.version=20260517.0.530531
# Mon, 18 May 2026 21:49:13 GMT
LABEL org.opencontainers.image.revision=34b87485162b028c8d957bdcd2674359d883cd21
# Mon, 18 May 2026 21:49:13 GMT
LABEL org.opencontainers.image.created=2026-05-17T00:09:11+00:00
# Mon, 18 May 2026 21:49:13 GMT
COPY /rootfs/ / # buildkit
# Mon, 18 May 2026 21:49:15 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260517.0.530531' /etc/os-release # buildkit
# Mon, 18 May 2026 21:49:15 GMT
ENV LANG=C.UTF-8
# Mon, 18 May 2026 21:49:15 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:54b8626685668f7f8af95a079ff42364fac0252de2e6a4080bf1ae6363bc1f18`  
		Last Modified: Mon, 18 May 2026 21:49:47 GMT  
		Size: 131.5 MB (131522499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6d2dac6ee5f200ecc82f8cbeaebb86261dca5de1552b71a47a953c6d2ba2e7f`  
		Last Modified: Mon, 18 May 2026 21:49:39 GMT  
		Size: 8.7 KB (8665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:latest` - unknown; unknown

```console
$ docker pull archlinux@sha256:e01962c564f0d3c980a949782a4558a51a1599a0b786394e2d244958728a2905
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8193065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81c72c339fb8f01e8e158d7fe54967e96c09ba91ac985e6ef09dad3b36484673`

```dockerfile
```

-	Layers:
	-	`sha256:688e0a39cb99915dc563d9588850c7d3b3543dd9286cf2793eb7ad1a5b6b68a8`  
		Last Modified: Mon, 18 May 2026 21:49:39 GMT  
		Size: 8.2 MB (8181137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e261ca3733559df04d34bc4ea600670046a2ee9bb08854de1ecd8dcd577ba5a2`  
		Last Modified: Mon, 18 May 2026 21:49:39 GMT  
		Size: 11.9 KB (11928 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:881022c38f3338dd74f06ee0bf5ac05748e40efc6162a23dbbdbfef14634e506
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:445aaca11be510adf10b9ddcf30259d4ae4c8474530a8d5d71ca93199184ee70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.0 MB (325975046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ae6b25d6884216d69cdf94215f539a6531cc5365f409d2aecf40e54d93c75ec`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 18 May 2026 21:50:23 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Mon, 18 May 2026 21:50:23 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 18 May 2026 21:50:23 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 18 May 2026 21:50:23 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 18 May 2026 21:50:23 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 18 May 2026 21:50:23 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 18 May 2026 21:50:23 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 18 May 2026 21:50:23 GMT
LABEL org.opencontainers.image.version=20260517.0.530531
# Mon, 18 May 2026 21:50:23 GMT
LABEL org.opencontainers.image.revision=34b87485162b028c8d957bdcd2674359d883cd21
# Mon, 18 May 2026 21:50:23 GMT
LABEL org.opencontainers.image.created=2026-05-17T00:09:11+00:00
# Mon, 18 May 2026 21:50:23 GMT
COPY /rootfs/ / # buildkit
# Mon, 18 May 2026 21:50:31 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260517.0.530531' /etc/os-release # buildkit
# Mon, 18 May 2026 21:50:31 GMT
ENV LANG=C.UTF-8
# Mon, 18 May 2026 21:50:31 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:218564e2f8d63e6df94802e5115b23deb1041ba00fc7cf32cf180e239b11c7c2`  
		Last Modified: Mon, 18 May 2026 21:51:32 GMT  
		Size: 326.0 MB (325962465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26746621d3475df01f66df81be8930f7f25274c51a57a80bb03ea9537fe52cfd`  
		Last Modified: Mon, 18 May 2026 21:51:25 GMT  
		Size: 12.6 KB (12581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:3b08d6810090289dfc5f1994d8a38d2f7a74ab5fc489aaf0cbb4502cb5a8acbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14667077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9c43c7b9e0e77008c941959f6a9b99be5759270793c210268ab3286eef3a1c2`

```dockerfile
```

-	Layers:
	-	`sha256:790db6cb300f80a3b1ae5e1007a4876f01ffc72106844cef06ee6a2ae945c10d`  
		Last Modified: Mon, 18 May 2026 21:51:26 GMT  
		Size: 14.7 MB (14655309 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b66f7e1795b0bd401264c978fd0736e749f900a939bdd0d3895918c7640bbeb`  
		Last Modified: Mon, 18 May 2026 21:51:25 GMT  
		Size: 11.8 KB (11768 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel-20260524.0.535079`

**does not exist** (yet?)
