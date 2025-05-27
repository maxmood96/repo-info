## `archlinux:multilib-devel-20250525.0.354646`

```console
$ docker pull archlinux@sha256:68302e0528cde22744d1a740ef41bf39b53499760afe63b70bcc5476e104b305
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel-20250525.0.354646` - linux; amd64

```console
$ docker pull archlinux@sha256:c610420447bbbc5123790a6d276b3f5a375334bca7b7bf2ab3fdaa6bea459fa1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.2 MB (338202536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea2873f8627434d281f5aaedd55a7d4db9f6018a9bd58f5d34136ab52a215228`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 25 May 2025 00:07:55 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 25 May 2025 00:07:55 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 25 May 2025 00:07:55 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 25 May 2025 00:07:55 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 25 May 2025 00:07:55 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 25 May 2025 00:07:55 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 25 May 2025 00:07:55 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 25 May 2025 00:07:55 GMT
LABEL org.opencontainers.image.version=20250525.0.354646
# Sun, 25 May 2025 00:07:55 GMT
LABEL org.opencontainers.image.revision=ae0527df18a9c5b94b28351b2265a20012d2fda0
# Sun, 25 May 2025 00:07:55 GMT
LABEL org.opencontainers.image.created=2025-05-25T00:07:54+00:00
# Sun, 25 May 2025 00:07:55 GMT
COPY /rootfs/ / # buildkit
# Sun, 25 May 2025 00:07:55 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250525.0.354646' /etc/os-release # buildkit
# Sun, 25 May 2025 00:07:55 GMT
ENV LANG=C.UTF-8
# Sun, 25 May 2025 00:07:55 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:078d9a48ab98980e9814165084b9aa06cc353b71dc529f18e74b34151ebfb280`  
		Last Modified: Tue, 27 May 2025 18:52:12 GMT  
		Size: 338.2 MB (338192260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb5ab2201e23756fed572b08087aba5ebefbe2f9f0dfa8454b5fb7e35cf95f1d`  
		Last Modified: Tue, 27 May 2025 18:52:03 GMT  
		Size: 10.3 KB (10276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel-20250525.0.354646` - unknown; unknown

```console
$ docker pull archlinux@sha256:807766c09a13af3b22e93cdee9eba25197ec30a094d353529eb45f2ad9465874
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12310317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f9737f64c584866a464e033db3f7d93a71d45bfe9c5a139d84a1ffe486673d6`

```dockerfile
```

-	Layers:
	-	`sha256:1d95f4771e90617bc7424144d65e65ec7df971fc4da8eeca002302da837ac1df`  
		Last Modified: Tue, 27 May 2025 18:52:04 GMT  
		Size: 12.3 MB (12298507 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:879b785c42df989918859ef0986c7aa55a06cdb731041c4d14c40c1bf65bde6d`  
		Last Modified: Tue, 27 May 2025 18:52:03 GMT  
		Size: 11.8 KB (11810 bytes)  
		MIME: application/vnd.in-toto+json
