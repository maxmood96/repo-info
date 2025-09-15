## `archlinux:multilib-devel-20250914.0.420821`

```console
$ docker pull archlinux@sha256:31c2103de5109437b8d9f48accfaf526a3191c6b1f92ba87371331f7d4ff99bc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel-20250914.0.420821` - linux; amd64

```console
$ docker pull archlinux@sha256:c2dc5ad75555575d940a924c65b276f7183cf1d3cebe60cdefd5f08bfa66e94b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.7 MB (340729932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6826e30ceeb7b4bce3fead594bfa2ae3e21daf9b55d3bdd3bdf4aa18771d3b0f`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 14 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 14 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 14 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 14 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 14 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 14 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 14 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 14 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.version=20250914.0.420821
# Sun, 14 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.revision=744b1c5c6a7f999c9a8b3daa5897c922e86563ee
# Sun, 14 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.created=2025-09-14T00:07:14+00:00
# Sun, 14 Sep 2025 00:07:14 GMT
COPY /rootfs/ / # buildkit
# Sun, 14 Sep 2025 00:07:14 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250914.0.420821' /etc/os-release # buildkit
# Sun, 14 Sep 2025 00:07:14 GMT
ENV LANG=C.UTF-8
# Sun, 14 Sep 2025 00:07:14 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:9f25f03a61659fe88c998948478e8e8f4a78af4baae6861c412264c76cefc2b6`  
		Last Modified: Mon, 15 Sep 2025 17:06:59 GMT  
		Size: 340.7 MB (340719665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdfafbbd681a837939cadf718167f2af172360fd711bb567305c2b211eeeb494`  
		Last Modified: Mon, 15 Sep 2025 17:01:06 GMT  
		Size: 10.3 KB (10267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel-20250914.0.420821` - unknown; unknown

```console
$ docker pull archlinux@sha256:24083930c4b61846e3f755875a11552711957c6077032fe49372655b16076255
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 MB (12364860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3cf0ae21e4fe36e3c456e424fd048d968ef00a9c7141f2cc8a6c8911b12190a`

```dockerfile
```

-	Layers:
	-	`sha256:08b76a7a61d4cb877dc88025799a71acbacfdae595c647e7929ad213895d1e37`  
		Last Modified: Mon, 15 Sep 2025 19:48:36 GMT  
		Size: 12.4 MB (12353049 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2a8a116e8ead8b781f97da6ea87d3fb5f8a3a8449fc8ef7f0a56c5ab3676f42`  
		Last Modified: Mon, 15 Sep 2025 19:48:37 GMT  
		Size: 11.8 KB (11811 bytes)  
		MIME: application/vnd.in-toto+json
