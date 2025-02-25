## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:cd39606466737d54e804fd5bad28c0fd195aba0042cd3c38c60aca14e281b895
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:85a806225854c084f6122ff453517e22f5d998094bef13b0ad74f4f983250865
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.2 MB (280244252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07b648ccfa3dd5007f0201036d2d5803938cac01d6b7ca66c4cbbbc45a5b04cc`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 23 Feb 2025 00:07:38 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 23 Feb 2025 00:07:38 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 23 Feb 2025 00:07:38 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 23 Feb 2025 00:07:38 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 23 Feb 2025 00:07:38 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 23 Feb 2025 00:07:38 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 23 Feb 2025 00:07:38 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 23 Feb 2025 00:07:38 GMT
LABEL org.opencontainers.image.version=20250223.0.312761
# Sun, 23 Feb 2025 00:07:38 GMT
LABEL org.opencontainers.image.revision=ae0527df18a9c5b94b28351b2265a20012d2fda0
# Sun, 23 Feb 2025 00:07:38 GMT
LABEL org.opencontainers.image.created=2025-02-23T00:07:38+00:00
# Sun, 23 Feb 2025 00:07:38 GMT
COPY /rootfs/ / # buildkit
# Sun, 23 Feb 2025 00:07:38 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250223.0.312761' /etc/os-release # buildkit
# Sun, 23 Feb 2025 00:07:38 GMT
ENV LANG=C.UTF-8
# Sun, 23 Feb 2025 00:07:38 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:52c18e014de0f10e1675122d732c121993497f96975726b19208798ac5ec9328`  
		Last Modified: Mon, 24 Feb 2025 20:29:41 GMT  
		Size: 280.2 MB (280235177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51fb5e786de9d4a3fd6ce9778e8a34ae5c72b3e36c34d7a4f9b63a6228fd8b61`  
		Last Modified: Mon, 24 Feb 2025 20:29:37 GMT  
		Size: 9.1 KB (9075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:71f1cea6167ec0211286fd788ff0c81677d8bbb823ecedbda9e6fcdc10665cee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.0 MB (11980146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30c0650c190dd2e5181a313618f945c98df1f28b3eb86d80df6ead6591681d39`

```dockerfile
```

-	Layers:
	-	`sha256:0882295c03fe1a298bbf8fb2d58765305b0a41aa33ff2486ac4244ccc19fee25`  
		Last Modified: Mon, 24 Feb 2025 20:29:37 GMT  
		Size: 12.0 MB (11968392 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1160a80a4f8dfc675a9ec6bc950a108524b349c7f53bd872ff584223bd6ffc01`  
		Last Modified: Mon, 24 Feb 2025 20:29:37 GMT  
		Size: 11.8 KB (11754 bytes)  
		MIME: application/vnd.in-toto+json
