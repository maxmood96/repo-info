<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `archlinux`

-	[`archlinux:base`](#archlinuxbase)
-	[`archlinux:base-20250119.0.299327`](#archlinuxbase-202501190299327)
-	[`archlinux:base-devel`](#archlinuxbase-devel)
-	[`archlinux:base-devel-20250119.0.299327`](#archlinuxbase-devel-202501190299327)
-	[`archlinux:latest`](#archlinuxlatest)
-	[`archlinux:multilib-devel`](#archlinuxmultilib-devel)
-	[`archlinux:multilib-devel-20250119.0.299327`](#archlinuxmultilib-devel-202501190299327)

## `archlinux:base`

```console
$ docker pull archlinux@sha256:4ec00881e67eaf063c4e8d4f3a7e47eb7bc5de77edfd45477e0c6a734a60eb51
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:9d946f864864c3792284dbda5819833a861d05120411b1ac25f8640db71d6b81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.1 MB (153104257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:059aaefc5329241cbf7482d75f7e0bab4a02518960bbab758fd80de22620546b`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 12 Jan 2025 00:07:47 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 12 Jan 2025 00:07:47 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 12 Jan 2025 00:07:47 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 12 Jan 2025 00:07:47 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 12 Jan 2025 00:07:47 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 12 Jan 2025 00:07:47 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 12 Jan 2025 00:07:47 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 12 Jan 2025 00:07:47 GMT
LABEL org.opencontainers.image.version=20250112.0.297543
# Sun, 12 Jan 2025 00:07:47 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 12 Jan 2025 00:07:47 GMT
LABEL org.opencontainers.image.created=2025-01-12T00:07:47+00:00
# Sun, 12 Jan 2025 00:07:47 GMT
COPY /rootfs/ / # buildkit
# Sun, 12 Jan 2025 00:07:47 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250112.0.297543' /etc/os-release # buildkit
# Sun, 12 Jan 2025 00:07:47 GMT
ENV LANG=C.UTF-8
# Sun, 12 Jan 2025 00:07:47 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:b72827dcfa2c12402f1ecdb33cfbeaf084768197dbafd59f153a30daa3e81911`  
		Last Modified: Mon, 13 Jan 2025 19:28:46 GMT  
		Size: 153.1 MB (153095897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f99b68cf689f9e3f5f9fa63b0094740f7085a5548cf40f0184b379cc01998b39`  
		Last Modified: Mon, 13 Jan 2025 19:28:43 GMT  
		Size: 8.4 KB (8360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:d72ff4e11e1d6c429a7cbdba4fcf2dc287f1b23c921c099ccfa7aa74dfe66881
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8100838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ffa730d46ab21d683319fcadaa3de03311af1daefce45ac13c8df2a742ef329`

```dockerfile
```

-	Layers:
	-	`sha256:1138062713ffbf051ec2f9529014d6e1304810945ded6c3a55a9457d4982cb2a`  
		Last Modified: Mon, 13 Jan 2025 19:28:43 GMT  
		Size: 8.1 MB (8088866 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa54eefdf8ca1213df5017d8bde7fea68a91b08efd9b869c6efd4f0627a07686`  
		Last Modified: Mon, 13 Jan 2025 19:28:43 GMT  
		Size: 12.0 KB (11972 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-20250119.0.299327`

```console
$ docker pull archlinux@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:5bffbf54bf180c86fbe2ade792cd2d3e957df50fa45da63cb8995564aa90ff9e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:bfdcc60a7bff6bd7f45b02b9fa64d7962c050d5e223b1df1052b05389bbaf7e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.2 MB (274245183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:590a83b1826554594b9cbc44667fb9065d7e895ccb4d5c871c4d17fe44f53137`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 12 Jan 2025 00:07:47 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 12 Jan 2025 00:07:47 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 12 Jan 2025 00:07:47 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 12 Jan 2025 00:07:47 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 12 Jan 2025 00:07:47 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 12 Jan 2025 00:07:47 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 12 Jan 2025 00:07:47 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 12 Jan 2025 00:07:47 GMT
LABEL org.opencontainers.image.version=20250112.0.297543
# Sun, 12 Jan 2025 00:07:47 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 12 Jan 2025 00:07:47 GMT
LABEL org.opencontainers.image.created=2025-01-12T00:07:47+00:00
# Sun, 12 Jan 2025 00:07:47 GMT
COPY /rootfs/ / # buildkit
# Sun, 12 Jan 2025 00:07:47 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250112.0.297543' /etc/os-release # buildkit
# Sun, 12 Jan 2025 00:07:47 GMT
ENV LANG=C.UTF-8
# Sun, 12 Jan 2025 00:07:47 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:19a599bcbe68b61c0f6ac716193c401951e23f55a309045c997dba16a3374820`  
		Last Modified: Mon, 13 Jan 2025 19:29:14 GMT  
		Size: 274.2 MB (274236106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91e2925da3e00761896ebcd51442a961926b6578f306e242b3ec6e43d776b39b`  
		Last Modified: Mon, 13 Jan 2025 19:29:10 GMT  
		Size: 9.1 KB (9077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:1faa61dc7071bc3420230183ac805815f7a8ebae57d33c356f09fb68e9b1e2db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.9 MB (11907476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63e49912cfbaad5f8ad029aca7edd8708a25abf9cc08411c1d26e7d27092f340`

```dockerfile
```

-	Layers:
	-	`sha256:c8405add251a7d5a7598e1a190f49786176e17c2ec8e8de3aca813f82c75c6bf`  
		Last Modified: Mon, 13 Jan 2025 19:29:10 GMT  
		Size: 11.9 MB (11895722 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4a2e25c40caf508460a713b94556306d42d5b7a4e927fbf64d985fb7c3cb10a`  
		Last Modified: Mon, 13 Jan 2025 19:29:10 GMT  
		Size: 11.8 KB (11754 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel-20250119.0.299327`

```console
$ docker pull archlinux@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `archlinux:latest`

```console
$ docker pull archlinux@sha256:4ec00881e67eaf063c4e8d4f3a7e47eb7bc5de77edfd45477e0c6a734a60eb51
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:9d946f864864c3792284dbda5819833a861d05120411b1ac25f8640db71d6b81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.1 MB (153104257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:059aaefc5329241cbf7482d75f7e0bab4a02518960bbab758fd80de22620546b`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 12 Jan 2025 00:07:47 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 12 Jan 2025 00:07:47 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 12 Jan 2025 00:07:47 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 12 Jan 2025 00:07:47 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 12 Jan 2025 00:07:47 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 12 Jan 2025 00:07:47 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 12 Jan 2025 00:07:47 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 12 Jan 2025 00:07:47 GMT
LABEL org.opencontainers.image.version=20250112.0.297543
# Sun, 12 Jan 2025 00:07:47 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 12 Jan 2025 00:07:47 GMT
LABEL org.opencontainers.image.created=2025-01-12T00:07:47+00:00
# Sun, 12 Jan 2025 00:07:47 GMT
COPY /rootfs/ / # buildkit
# Sun, 12 Jan 2025 00:07:47 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250112.0.297543' /etc/os-release # buildkit
# Sun, 12 Jan 2025 00:07:47 GMT
ENV LANG=C.UTF-8
# Sun, 12 Jan 2025 00:07:47 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:b72827dcfa2c12402f1ecdb33cfbeaf084768197dbafd59f153a30daa3e81911`  
		Last Modified: Mon, 13 Jan 2025 19:28:46 GMT  
		Size: 153.1 MB (153095897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f99b68cf689f9e3f5f9fa63b0094740f7085a5548cf40f0184b379cc01998b39`  
		Last Modified: Mon, 13 Jan 2025 19:28:43 GMT  
		Size: 8.4 KB (8360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:latest` - unknown; unknown

```console
$ docker pull archlinux@sha256:d72ff4e11e1d6c429a7cbdba4fcf2dc287f1b23c921c099ccfa7aa74dfe66881
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8100838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ffa730d46ab21d683319fcadaa3de03311af1daefce45ac13c8df2a742ef329`

```dockerfile
```

-	Layers:
	-	`sha256:1138062713ffbf051ec2f9529014d6e1304810945ded6c3a55a9457d4982cb2a`  
		Last Modified: Mon, 13 Jan 2025 19:28:43 GMT  
		Size: 8.1 MB (8088866 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa54eefdf8ca1213df5017d8bde7fea68a91b08efd9b869c6efd4f0627a07686`  
		Last Modified: Mon, 13 Jan 2025 19:28:43 GMT  
		Size: 12.0 KB (11972 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:13b1036c6c31622d924812de5ebc41353e0cf0a20dce28f2633385dc94b9a607
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:0e70b49bf26e1c17fe6c9bdf1f1fb49cbd3eb93ce2f7dce22521199cd8b2538e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.1 MB (324100005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44ae797a5b95acbbc644e03de6411b8833ccb24eafe2b9a1d8b09aec1410d959`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 12 Jan 2025 00:07:47 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 12 Jan 2025 00:07:47 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 12 Jan 2025 00:07:47 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 12 Jan 2025 00:07:47 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 12 Jan 2025 00:07:47 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 12 Jan 2025 00:07:47 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 12 Jan 2025 00:07:47 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 12 Jan 2025 00:07:47 GMT
LABEL org.opencontainers.image.version=20250112.0.297543
# Sun, 12 Jan 2025 00:07:47 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 12 Jan 2025 00:07:47 GMT
LABEL org.opencontainers.image.created=2025-01-12T00:07:47+00:00
# Sun, 12 Jan 2025 00:07:47 GMT
COPY /rootfs/ / # buildkit
# Sun, 12 Jan 2025 00:07:47 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250112.0.297543' /etc/os-release # buildkit
# Sun, 12 Jan 2025 00:07:47 GMT
ENV LANG=C.UTF-8
# Sun, 12 Jan 2025 00:07:47 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:c8449f073c3e398c721f972d23d1572901515bfa70be188a331897942c0ef478`  
		Last Modified: Mon, 13 Jan 2025 19:29:28 GMT  
		Size: 324.1 MB (324089754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a546a2758b768631b3aeab8ab930c455db81ff37e4d540a676c9a9b33cf5452a`  
		Last Modified: Mon, 13 Jan 2025 19:29:22 GMT  
		Size: 10.3 KB (10251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:87272d00fd78879b7156e469e97936274f59c1b0531c532ddc48d637812c05c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12176052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11546494ab0da0ce3d273f535973ffb098f0cb4936738ea7f66c6e847d9f4d45`

```dockerfile
```

-	Layers:
	-	`sha256:674f22cd0d28f3b3135fbce0f9d3b3d30d081aefbc303ce42ec5432f92ea9c28`  
		Last Modified: Mon, 13 Jan 2025 19:29:22 GMT  
		Size: 12.2 MB (12164242 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5919c5ab0ea9cfc5108838cd2b99a023a245f65fa0adf6792623e84bf459099e`  
		Last Modified: Mon, 13 Jan 2025 19:29:22 GMT  
		Size: 11.8 KB (11810 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel-20250119.0.299327`

```console
$ docker pull archlinux@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0
