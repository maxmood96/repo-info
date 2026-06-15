<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `archlinux`

-	[`archlinux:base`](#archlinuxbase)
-	[`archlinux:base-20260614.0.544538`](#archlinuxbase-202606140544538)
-	[`archlinux:base-devel`](#archlinuxbase-devel)
-	[`archlinux:base-devel-20260614.0.544538`](#archlinuxbase-devel-202606140544538)
-	[`archlinux:latest`](#archlinuxlatest)
-	[`archlinux:multilib-devel`](#archlinuxmultilib-devel)
-	[`archlinux:multilib-devel-20260614.0.544538`](#archlinuxmultilib-devel-202606140544538)

## `archlinux:base`

```console
$ docker pull archlinux@sha256:a1f78e6a19f19d0f6cd9bf35ec59de31fe0bdeff6a94e968be0276ca255f14cd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:fb47d15e0fd28369c700edcfa46dd44e234d8ab6fee9627ee5f1ead5f1fc6c21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.2 MB (131171103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e18054cdf72229c2a48277565a6d80f3e2a7b91209010f8b0b50e43b97bd133f`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 08 Jun 2026 18:50:15 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Mon, 08 Jun 2026 18:50:15 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 08 Jun 2026 18:50:15 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 08 Jun 2026 18:50:15 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 08 Jun 2026 18:50:15 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 08 Jun 2026 18:50:15 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 08 Jun 2026 18:50:15 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 08 Jun 2026 18:50:15 GMT
LABEL org.opencontainers.image.version=20260607.0.541780
# Mon, 08 Jun 2026 18:50:15 GMT
LABEL org.opencontainers.image.revision=34b87485162b028c8d957bdcd2674359d883cd21
# Mon, 08 Jun 2026 18:50:15 GMT
LABEL org.opencontainers.image.created=2026-06-07T00:09:31+00:00
# Mon, 08 Jun 2026 18:50:15 GMT
COPY /rootfs/ / # buildkit
# Mon, 08 Jun 2026 18:50:18 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260607.0.541780' /etc/os-release # buildkit
# Mon, 08 Jun 2026 18:50:18 GMT
ENV LANG=C.UTF-8
# Mon, 08 Jun 2026 18:50:18 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:f84cafa04e5c2c4a470761f8140e0f2a20f298d0c1385f4e465a3ceded3ede79`  
		Last Modified: Mon, 08 Jun 2026 18:50:44 GMT  
		Size: 131.2 MB (131162431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cba61d83f91dee65cd4786c6eee321d3b838b887ed4b36c5c50cbcda73d13605`  
		Last Modified: Mon, 08 Jun 2026 18:50:41 GMT  
		Size: 8.7 KB (8672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:49bcbaa8d06bca06f4ba14af2d182758028dfce62c41410a23c1c6d25fed3791
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8194357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c1723c5e4cfe344f0486568cdadd2b48667a0b8fa5fb374ffcfee3a28892e26`

```dockerfile
```

-	Layers:
	-	`sha256:ba018fc32aa7762cf7829b138d39eebbc36af9547c240c4046fadbcb9cd275ff`  
		Last Modified: Mon, 08 Jun 2026 18:50:41 GMT  
		Size: 8.2 MB (8182429 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e4d2ee4f5ebb9c953b3045d16444d4873dfc971af37231b328cdf801391a47b`  
		Last Modified: Mon, 08 Jun 2026 18:50:41 GMT  
		Size: 11.9 KB (11928 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-20260614.0.544538`

```console
$ docker pull archlinux@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:dd60dfcca90f1ee6c2dd265ed27062070a1fb2e3b307723838a9d97741284722
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:f557e49eaad9b696f0ef71cd12f2a2418407c8d4c441f311c38bd95186afd85f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.2 MB (303239264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc16ee0e5ffe5c241a261f07c78777b0cfc4b0b38456930bf2179fdabb7fa034`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 08 Jun 2026 18:51:18 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Mon, 08 Jun 2026 18:51:18 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 08 Jun 2026 18:51:18 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 08 Jun 2026 18:51:18 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 08 Jun 2026 18:51:18 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 08 Jun 2026 18:51:18 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 08 Jun 2026 18:51:18 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 08 Jun 2026 18:51:18 GMT
LABEL org.opencontainers.image.version=20260607.0.541780
# Mon, 08 Jun 2026 18:51:18 GMT
LABEL org.opencontainers.image.revision=34b87485162b028c8d957bdcd2674359d883cd21
# Mon, 08 Jun 2026 18:51:18 GMT
LABEL org.opencontainers.image.created=2026-06-07T00:09:31+00:00
# Mon, 08 Jun 2026 18:51:18 GMT
COPY /rootfs/ / # buildkit
# Mon, 08 Jun 2026 18:51:25 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260607.0.541780' /etc/os-release # buildkit
# Mon, 08 Jun 2026 18:51:25 GMT
ENV LANG=C.UTF-8
# Mon, 08 Jun 2026 18:51:25 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:011844ffd4c148ed1ec219c23df98cce9131911699615bbfab580bda4db5ae24`  
		Last Modified: Mon, 08 Jun 2026 18:52:22 GMT  
		Size: 303.2 MB (303227863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b02c2b8021a1d28b03a38d0831afce2be8c98cb144398fd5ae3456d3a071cd9`  
		Last Modified: Mon, 08 Jun 2026 18:52:15 GMT  
		Size: 11.4 KB (11401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:33fc398841b252e7e2878e984122ff50851b08c29a081b3e089362d98794dfbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 MB (14397498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14261b8fd4b8b8dbfff97eb0fa942351512c96f58d1072c3f32bec47992145f6`

```dockerfile
```

-	Layers:
	-	`sha256:d94d3b6c8ed5a2e3a7aaef3a2f556ce6f645cc89d6c56d8640f3838cc7abc89f`  
		Last Modified: Mon, 08 Jun 2026 18:52:16 GMT  
		Size: 14.4 MB (14385786 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:783351bb6d2edb4b4c0a2ca43ae7ba325a8b63037c9b1cb16c2586da79a13a3e`  
		Last Modified: Mon, 08 Jun 2026 18:52:15 GMT  
		Size: 11.7 KB (11712 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel-20260614.0.544538`

```console
$ docker pull archlinux@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `archlinux:latest`

```console
$ docker pull archlinux@sha256:a1f78e6a19f19d0f6cd9bf35ec59de31fe0bdeff6a94e968be0276ca255f14cd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:fb47d15e0fd28369c700edcfa46dd44e234d8ab6fee9627ee5f1ead5f1fc6c21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.2 MB (131171103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e18054cdf72229c2a48277565a6d80f3e2a7b91209010f8b0b50e43b97bd133f`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 08 Jun 2026 18:50:15 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Mon, 08 Jun 2026 18:50:15 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 08 Jun 2026 18:50:15 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 08 Jun 2026 18:50:15 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 08 Jun 2026 18:50:15 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 08 Jun 2026 18:50:15 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 08 Jun 2026 18:50:15 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 08 Jun 2026 18:50:15 GMT
LABEL org.opencontainers.image.version=20260607.0.541780
# Mon, 08 Jun 2026 18:50:15 GMT
LABEL org.opencontainers.image.revision=34b87485162b028c8d957bdcd2674359d883cd21
# Mon, 08 Jun 2026 18:50:15 GMT
LABEL org.opencontainers.image.created=2026-06-07T00:09:31+00:00
# Mon, 08 Jun 2026 18:50:15 GMT
COPY /rootfs/ / # buildkit
# Mon, 08 Jun 2026 18:50:18 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260607.0.541780' /etc/os-release # buildkit
# Mon, 08 Jun 2026 18:50:18 GMT
ENV LANG=C.UTF-8
# Mon, 08 Jun 2026 18:50:18 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:f84cafa04e5c2c4a470761f8140e0f2a20f298d0c1385f4e465a3ceded3ede79`  
		Last Modified: Mon, 08 Jun 2026 18:50:44 GMT  
		Size: 131.2 MB (131162431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cba61d83f91dee65cd4786c6eee321d3b838b887ed4b36c5c50cbcda73d13605`  
		Last Modified: Mon, 08 Jun 2026 18:50:41 GMT  
		Size: 8.7 KB (8672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:latest` - unknown; unknown

```console
$ docker pull archlinux@sha256:49bcbaa8d06bca06f4ba14af2d182758028dfce62c41410a23c1c6d25fed3791
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8194357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c1723c5e4cfe344f0486568cdadd2b48667a0b8fa5fb374ffcfee3a28892e26`

```dockerfile
```

-	Layers:
	-	`sha256:ba018fc32aa7762cf7829b138d39eebbc36af9547c240c4046fadbcb9cd275ff`  
		Last Modified: Mon, 08 Jun 2026 18:50:41 GMT  
		Size: 8.2 MB (8182429 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e4d2ee4f5ebb9c953b3045d16444d4873dfc971af37231b328cdf801391a47b`  
		Last Modified: Mon, 08 Jun 2026 18:50:41 GMT  
		Size: 11.9 KB (11928 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:e6c4eacdc7d29cf643f18e4cfb7a31a2e893a58812fb848ba082f8998e7ea79d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:bac38ab00bbb724ce28c462090a16c945b63a240decb6a7cf379bdbbcd965bf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.6 MB (325614860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4432acb6ef1440624e07af21515fc71e8acf2c675d70b286b05a2057b5c36f2c`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 08 Jun 2026 18:52:59 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Mon, 08 Jun 2026 18:52:59 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 08 Jun 2026 18:52:59 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 08 Jun 2026 18:52:59 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 08 Jun 2026 18:52:59 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 08 Jun 2026 18:52:59 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 08 Jun 2026 18:52:59 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 08 Jun 2026 18:52:59 GMT
LABEL org.opencontainers.image.version=20260607.0.541780
# Mon, 08 Jun 2026 18:52:59 GMT
LABEL org.opencontainers.image.revision=34b87485162b028c8d957bdcd2674359d883cd21
# Mon, 08 Jun 2026 18:52:59 GMT
LABEL org.opencontainers.image.created=2026-06-07T00:09:31+00:00
# Mon, 08 Jun 2026 18:52:59 GMT
COPY /rootfs/ / # buildkit
# Mon, 08 Jun 2026 18:53:06 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260607.0.541780' /etc/os-release # buildkit
# Mon, 08 Jun 2026 18:53:06 GMT
ENV LANG=C.UTF-8
# Mon, 08 Jun 2026 18:53:06 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:33c542c269fab0fd2e79e751ea20038d1a2b9f0b429f58b9d3c2557c5198706a`  
		Last Modified: Mon, 08 Jun 2026 18:54:07 GMT  
		Size: 325.6 MB (325602302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c928c01f537d741e5384fb5a33143a6e0be2634345a1ddd8d1e3f71dd5bbd3f`  
		Last Modified: Mon, 08 Jun 2026 18:54:01 GMT  
		Size: 12.6 KB (12558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:85beb6033726c2975b70e73ae357bad61a36871fb12466b42855b32b102f1a73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14668220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8360cc6388d36e4dda0c02ede03d280e4c4a02d41f7e060cdb1cc7684f8a860d`

```dockerfile
```

-	Layers:
	-	`sha256:b5e77fc1adf1127c92c9b1546ef6c7135128f200100a85d4e0545a20d60c37a9`  
		Last Modified: Mon, 08 Jun 2026 18:54:02 GMT  
		Size: 14.7 MB (14656453 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce182fab25d3f5e50b56f19ef7f7769a45867dcd1f3f9f23c7522e75fdf7ef15`  
		Last Modified: Mon, 08 Jun 2026 18:54:01 GMT  
		Size: 11.8 KB (11767 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel-20260614.0.544538`

```console
$ docker pull archlinux@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0
