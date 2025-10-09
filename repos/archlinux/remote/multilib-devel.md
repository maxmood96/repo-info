## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:9f6f04ef67cea4f618e10c45817c50dbd7e575bddff5fa4d71a38ac55bcc781b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:3b8be9f0edbf296a5dc67ec43dc322dc4c6c4da7464d53e78c7f50284fa414d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.7 MB (341657928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20b29667e376d3033990daed8f956ad8162f511ac82a5ecf9c3a2de844016646`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.version=20251005.0.430597
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.revision=744b1c5c6a7f999c9a8b3daa5897c922e86563ee
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.created=2025-10-05T00:07:46+00:00
# Sun, 05 Oct 2025 00:07:46 GMT
COPY /rootfs/ / # buildkit
# Sun, 05 Oct 2025 00:07:46 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20251005.0.430597' /etc/os-release # buildkit
# Sun, 05 Oct 2025 00:07:46 GMT
ENV LANG=C.UTF-8
# Sun, 05 Oct 2025 00:07:46 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:57d32341d0b304edbdd20efcf9481afeb1fb71b457948c77d909ebc150363d3e`  
		Last Modified: Mon, 06 Oct 2025 19:51:26 GMT  
		Size: 341.6 MB (341647654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e64da822fa5ec92466fb9b1d251f582d911d9c790c885007dab622a1d327b871`  
		Last Modified: Wed, 08 Oct 2025 22:18:19 GMT  
		Size: 10.3 KB (10274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:1d3bd5c105654c180708d87ee1ddc01a2b20595c2309e80aefad7a4e7426bcad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 MB (12400183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50e817dec3eb673f3f94149ce924e8fa36ba53824d7d5c8278d5ef9baec098d5`

```dockerfile
```

-	Layers:
	-	`sha256:9ad82c0988e315385a06db740bb36b328c4e594c9e47be33aa65ddca196b3ec8`  
		Last Modified: Thu, 09 Oct 2025 01:48:31 GMT  
		Size: 12.4 MB (12388372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:845fd47d51db66d960eeac4ce73f2e97b31281b40ebcb1f8cfc41f0532798327`  
		Last Modified: Thu, 09 Oct 2025 01:48:32 GMT  
		Size: 11.8 KB (11811 bytes)  
		MIME: application/vnd.in-toto+json
