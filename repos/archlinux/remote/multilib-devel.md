## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:c173b8e612164227dc475cad83e9e126938925e6e4ce89ec9ccc2a8a117c8288
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:9d637ee873ac25906ef22dfb5bf3832adbeec8998c786b8fc18227b593547aa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.8 MB (330834610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e32bf15ddf39ce2ecb3d3e153874f44851505506cf57506316ec19ba7eb24c7`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 30 Mar 2025 00:07:39 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 30 Mar 2025 00:07:39 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 30 Mar 2025 00:07:39 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 30 Mar 2025 00:07:39 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 30 Mar 2025 00:07:39 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 30 Mar 2025 00:07:39 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 30 Mar 2025 00:07:39 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 30 Mar 2025 00:07:39 GMT
LABEL org.opencontainers.image.version=20250330.0.328921
# Sun, 30 Mar 2025 00:07:39 GMT
LABEL org.opencontainers.image.revision=ae0527df18a9c5b94b28351b2265a20012d2fda0
# Sun, 30 Mar 2025 00:07:39 GMT
LABEL org.opencontainers.image.created=2025-03-30T00:07:39+00:00
# Sun, 30 Mar 2025 00:07:39 GMT
COPY /rootfs/ / # buildkit
# Sun, 30 Mar 2025 00:07:39 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250330.0.328921' /etc/os-release # buildkit
# Sun, 30 Mar 2025 00:07:39 GMT
ENV LANG=C.UTF-8
# Sun, 30 Mar 2025 00:07:39 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:ad34537c3749262aa4117f2f3c7acbd59db0eced0a6efee1cdba55032a967b0e`  
		Last Modified: Mon, 31 Mar 2025 16:35:15 GMT  
		Size: 330.8 MB (330824353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83cdf2da152fe4648b2bfb5f57eb0fdce85b8fabb9b153f5a67f3fe5b292366f`  
		Last Modified: Mon, 31 Mar 2025 16:35:07 GMT  
		Size: 10.3 KB (10257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:87ebf1488c6902a4bbfe2567053ac58f7d7437a1d085b4a819e1402abfd0e6c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12262463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46f1bd9df030ad99b19aec22187fb2c00b76fd4a60916de6485392d5172038e2`

```dockerfile
```

-	Layers:
	-	`sha256:c1bd5878d4df9fe2426591610e1e64791efc50249a36114b2b85e054e45f0dcd`  
		Last Modified: Mon, 31 Mar 2025 16:35:08 GMT  
		Size: 12.3 MB (12250652 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a891cbe827c9043a292ac6b68b0833c420170a44e75ab68364d2668954fa20c3`  
		Last Modified: Mon, 31 Mar 2025 16:35:07 GMT  
		Size: 11.8 KB (11811 bytes)  
		MIME: application/vnd.in-toto+json
