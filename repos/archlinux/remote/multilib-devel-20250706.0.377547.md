## `archlinux:multilib-devel-20250706.0.377547`

```console
$ docker pull archlinux@sha256:8e2026123f027a115b7a0f77d2dc6a8b6e2432681d9362506e24a4cf66eeb10d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel-20250706.0.377547` - linux; amd64

```console
$ docker pull archlinux@sha256:910dd2c30735771a6939a5bec6c9e3983edbf52d71217515861024dfa96b035e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.2 MB (339156701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:662187e8fa94c93225e4f441c71d120988ee206404f5ad169648b4b639d99ffe`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 06 Jul 2025 00:07:04 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 06 Jul 2025 00:07:04 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 06 Jul 2025 00:07:04 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 06 Jul 2025 00:07:04 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 06 Jul 2025 00:07:04 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 06 Jul 2025 00:07:04 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 06 Jul 2025 00:07:04 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 06 Jul 2025 00:07:04 GMT
LABEL org.opencontainers.image.version=20250706.0.377547
# Sun, 06 Jul 2025 00:07:04 GMT
LABEL org.opencontainers.image.revision=744b1c5c6a7f999c9a8b3daa5897c922e86563ee
# Sun, 06 Jul 2025 00:07:04 GMT
LABEL org.opencontainers.image.created=2025-07-06T00:07:03+00:00
# Sun, 06 Jul 2025 00:07:04 GMT
COPY /rootfs/ / # buildkit
# Sun, 06 Jul 2025 00:07:04 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250706.0.377547' /etc/os-release # buildkit
# Sun, 06 Jul 2025 00:07:04 GMT
ENV LANG=C.UTF-8
# Sun, 06 Jul 2025 00:07:04 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:6b021388ae3bc2cffb6dc29835ef55bf7407e0b696e9b961f8d1116618fd8d70`  
		Last Modified: Tue, 08 Jul 2025 00:07:29 GMT  
		Size: 339.1 MB (339146422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c78db3818f1db2189e0a57f97efea2333e9b61e5a8d3c3d6b9e54ce3f31e4742`  
		Last Modified: Mon, 07 Jul 2025 20:42:47 GMT  
		Size: 10.3 KB (10279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel-20250706.0.377547` - unknown; unknown

```console
$ docker pull archlinux@sha256:91cbc873824ad65fe3474dc1f5a45f64519e569b521fc12cb4055a0acb8b8d8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12292202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1a365bd922e9a109f43e2ca18aa38a5493ce724c5115cd5e400a3a169fd0cd4`

```dockerfile
```

-	Layers:
	-	`sha256:cda3835e97859e858bc6cbfd7d9fc5feb27b63f699ce1c810fc4a0a754ce9d94`  
		Last Modified: Mon, 07 Jul 2025 22:48:25 GMT  
		Size: 12.3 MB (12280391 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a221803e31b8bcf6e39316220cbb37a5ff5a078f60ada706e433fa0211620f4`  
		Last Modified: Mon, 07 Jul 2025 22:48:27 GMT  
		Size: 11.8 KB (11811 bytes)  
		MIME: application/vnd.in-toto+json
