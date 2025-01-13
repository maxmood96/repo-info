<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `archlinux`

-	[`archlinux:base`](#archlinuxbase)
-	[`archlinux:base-20250112.0.297543`](#archlinuxbase-202501120297543)
-	[`archlinux:base-devel`](#archlinuxbase-devel)
-	[`archlinux:base-devel-20250112.0.297543`](#archlinuxbase-devel-202501120297543)
-	[`archlinux:latest`](#archlinuxlatest)
-	[`archlinux:multilib-devel`](#archlinuxmultilib-devel)
-	[`archlinux:multilib-devel-20250112.0.297543`](#archlinuxmultilib-devel-202501120297543)

## `archlinux:base`

```console
$ docker pull archlinux@sha256:292bb4ec7866af67f8d66fe2114eef840eebc74302db00b891dcb2d278bec80a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:da131d0947336cbabc971ee7e400d94f2a2f4c32e6bc759e2a0b0f09fe2245cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.1 MB (153107935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdf34a96768a3e964a69639d9573d0e50984783a1bd1d005745e9b5efbe0993d`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 05 Jan 2025 00:08:06 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
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
	-	`sha256:734567a21ac630b02c05a26a3b8bdedcba14ff5644a33b2bb998c65564bf7647`  
		Last Modified: Tue, 07 Jan 2025 01:29:16 GMT  
		Size: 153.1 MB (153099589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2720411fb211aad740ff49e678394c60d7fb50bb25e8facf43fcaa4b69c0841e`  
		Last Modified: Wed, 08 Jan 2025 17:58:13 GMT  
		Size: 8.3 KB (8346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:1d20104a9198b4c02c8e513610d2454cd5dff48415eb7307c0f0239955b1dd98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8100826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f480a73f486501c3b42fdddb3b95874342168690ba88abe7802bec934095c63b`

```dockerfile
```

-	Layers:
	-	`sha256:0cc3395c8528c58062d37eb37fa11ad9176baf5d9d6f812631d1ab95bb8e48a1`  
		Last Modified: Wed, 08 Jan 2025 17:58:13 GMT  
		Size: 8.1 MB (8088854 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d459c75d9f78faab6db5c1038683dc414844909ce309f42e39d9fd777d4298c`  
		Last Modified: Wed, 08 Jan 2025 17:58:13 GMT  
		Size: 12.0 KB (11972 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-20250112.0.297543`

**does not exist** (yet?)

## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:9ecc262fbd132fa18063fc304531e7dcaf55914fa0ff994096d892cb3d70b349
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:26979d8c51891f396ece05f2c90b53409cae63a87772a2877b5f1bac54da9e1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.2 MB (274213234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1447420cef64fa70a34e3ca281f0026e5cb5c9ab2ab0c1342a66ef44585e3ab6`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 05 Jan 2025 00:08:06 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
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
	-	`sha256:680acf88979475a77fdde57deae10e0d8eb993a7fa27c17ea6fd78b65cfe855e`  
		Last Modified: Tue, 07 Jan 2025 01:29:59 GMT  
		Size: 274.2 MB (274204153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:100804ba99fdbc32e55b6f12d0aedce47acc4cea4bca527ba0a7e7acadca624c`  
		Last Modified: Wed, 08 Jan 2025 17:58:47 GMT  
		Size: 9.1 KB (9081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:1dd85f8569762b98ea87e074c90883936d1db6607f7d1db9ec07e3c93f921d6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.9 MB (11908056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e97937616da1706ac16b85533cd21d1afd388b9938b013a56e0b301fe4b6419`

```dockerfile
```

-	Layers:
	-	`sha256:dcb1c443c16ca59c7b58814eee54cb028987b595258f627e91ea9b551eff676f`  
		Last Modified: Wed, 08 Jan 2025 17:58:47 GMT  
		Size: 11.9 MB (11896302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f906c019f07af9f364187d9b8b62e582e755180382c5684c153d76a9884581b`  
		Last Modified: Wed, 08 Jan 2025 17:58:47 GMT  
		Size: 11.8 KB (11754 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel-20250112.0.297543`

**does not exist** (yet?)

## `archlinux:latest`

```console
$ docker pull archlinux@sha256:292bb4ec7866af67f8d66fe2114eef840eebc74302db00b891dcb2d278bec80a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:da131d0947336cbabc971ee7e400d94f2a2f4c32e6bc759e2a0b0f09fe2245cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.1 MB (153107935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdf34a96768a3e964a69639d9573d0e50984783a1bd1d005745e9b5efbe0993d`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 05 Jan 2025 00:08:06 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
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
	-	`sha256:734567a21ac630b02c05a26a3b8bdedcba14ff5644a33b2bb998c65564bf7647`  
		Last Modified: Tue, 07 Jan 2025 01:29:16 GMT  
		Size: 153.1 MB (153099589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2720411fb211aad740ff49e678394c60d7fb50bb25e8facf43fcaa4b69c0841e`  
		Last Modified: Wed, 08 Jan 2025 17:58:13 GMT  
		Size: 8.3 KB (8346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:latest` - unknown; unknown

```console
$ docker pull archlinux@sha256:1d20104a9198b4c02c8e513610d2454cd5dff48415eb7307c0f0239955b1dd98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8100826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f480a73f486501c3b42fdddb3b95874342168690ba88abe7802bec934095c63b`

```dockerfile
```

-	Layers:
	-	`sha256:0cc3395c8528c58062d37eb37fa11ad9176baf5d9d6f812631d1ab95bb8e48a1`  
		Last Modified: Wed, 08 Jan 2025 17:58:13 GMT  
		Size: 8.1 MB (8088854 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d459c75d9f78faab6db5c1038683dc414844909ce309f42e39d9fd777d4298c`  
		Last Modified: Wed, 08 Jan 2025 17:58:13 GMT  
		Size: 12.0 KB (11972 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:bad5c9c74cbbae376f711c1a420161e1d3245a84753cae0fc696c512c1cc631c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

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

### `archlinux:multilib-devel` - unknown; unknown

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

## `archlinux:multilib-devel-20250112.0.297543`

**does not exist** (yet?)
