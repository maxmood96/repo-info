## `archlinux:latest`

```console
$ docker pull archlinux@sha256:42a33e798a4962982756560a6bd4b630e5394bca4d82ba199df0fc45ad3af7bf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:0bcb48829c8419196a0e426710c0cce34b5a3d980884d879809aae3120d169c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.2 MB (159211558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a49736c0aab9f79496a44c9b436ddb9b9b4714e16daf298c4497dee340fb7f9`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 16 Mar 2025 00:07:29 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 16 Mar 2025 00:07:29 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 16 Mar 2025 00:07:29 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 16 Mar 2025 00:07:29 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 16 Mar 2025 00:07:29 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 16 Mar 2025 00:07:29 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 16 Mar 2025 00:07:29 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 16 Mar 2025 00:07:29 GMT
LABEL org.opencontainers.image.version=20250316.0.322463
# Sun, 16 Mar 2025 00:07:29 GMT
LABEL org.opencontainers.image.revision=ae0527df18a9c5b94b28351b2265a20012d2fda0
# Sun, 16 Mar 2025 00:07:29 GMT
LABEL org.opencontainers.image.created=2025-03-16T00:07:29+00:00
# Sun, 16 Mar 2025 00:07:29 GMT
COPY /rootfs/ / # buildkit
# Sun, 16 Mar 2025 00:07:29 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250316.0.322463' /etc/os-release # buildkit
# Sun, 16 Mar 2025 00:07:29 GMT
ENV LANG=C.UTF-8
# Sun, 16 Mar 2025 00:07:29 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:ffc1d56182e7518eb7a75cb1a01ef2681d8002a8055b34dd5b4f4ae66a123b82`  
		Last Modified: Mon, 17 Mar 2025 17:50:10 GMT  
		Size: 159.2 MB (159203223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38beca783d0980c57587c0c5c1fdb07460ef01ef4d360869a605f3951d88369c`  
		Last Modified: Mon, 17 Mar 2025 17:50:08 GMT  
		Size: 8.3 KB (8335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:latest` - unknown; unknown

```console
$ docker pull archlinux@sha256:e448b27734677034f8a29b189c9aa7d34e3ead9dd78349cd4dd9a86df76cb775
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8167493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2a090ade9cbbbf15d3b2a62ccb6a76b35ada2018ac07fce46485d70d8fa3af3`

```dockerfile
```

-	Layers:
	-	`sha256:42b8262092613dfed596b7845c3afc30aaa6c350b5c3ee02759aa1fdfbdd8747`  
		Last Modified: Mon, 17 Mar 2025 17:50:08 GMT  
		Size: 8.2 MB (8155521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:027d2e3ce2b938c982d8c106b2bd67f50aa09713581dc5f51a2851c5fae53a80`  
		Last Modified: Mon, 17 Mar 2025 17:50:08 GMT  
		Size: 12.0 KB (11972 bytes)  
		MIME: application/vnd.in-toto+json
