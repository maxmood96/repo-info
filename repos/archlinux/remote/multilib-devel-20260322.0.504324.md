## `archlinux:multilib-devel-20260322.0.504324`

```console
$ docker pull archlinux@sha256:8d0ae41cc3261c424b4a00af0982a9ca35257740b3a23ae5bda2ceb7212467aa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel-20260322.0.504324` - linux; amd64

```console
$ docker pull archlinux@sha256:ac3f08986561daddd69300793660bddebf3f795fe5de725715f29afe9c506724
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.4 MB (268448104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca969d1167bf24ce7f3aad6a3daa62918b454f4b768a7a2d8db427e4c7024743`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 23 Mar 2026 16:50:36 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Mon, 23 Mar 2026 16:50:36 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 23 Mar 2026 16:50:36 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 23 Mar 2026 16:50:36 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 23 Mar 2026 16:50:36 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 23 Mar 2026 16:50:36 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 23 Mar 2026 16:50:36 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 23 Mar 2026 16:50:36 GMT
LABEL org.opencontainers.image.version=20260322.0.504324
# Mon, 23 Mar 2026 16:50:36 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Mon, 23 Mar 2026 16:50:36 GMT
LABEL org.opencontainers.image.created=2026-03-22T00:06:34+00:00
# Mon, 23 Mar 2026 16:50:36 GMT
COPY /rootfs/ / # buildkit
# Mon, 23 Mar 2026 16:50:42 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260322.0.504324' /etc/os-release # buildkit
# Mon, 23 Mar 2026 16:50:42 GMT
ENV LANG=C.UTF-8
# Mon, 23 Mar 2026 16:50:42 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:c52b47f47cd63adb3262045f0c9366d519ea9bab319a612d9eeaf03a37c25b20`  
		Last Modified: Mon, 23 Mar 2026 16:51:33 GMT  
		Size: 268.4 MB (268437781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5926d58339bb1a7c2c7e8042eba02ab1a32dd5f0aba0e54b5a6170eb39bfe61e`  
		Last Modified: Mon, 23 Mar 2026 16:51:27 GMT  
		Size: 10.3 KB (10323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel-20260322.0.504324` - unknown; unknown

```console
$ docker pull archlinux@sha256:3d2e7c0a66b29c119115044157b1a4500202cd78613d12337ed25e546f548829
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12208888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:750285c53182f7dafc406384341a17cc15ec699aaf051806beda5b07fb867ac5`

```dockerfile
```

-	Layers:
	-	`sha256:e7312f8bc40d7be95914cb3d6db40cd171562471a5e03700dd02183351e76249`  
		Last Modified: Mon, 23 Mar 2026 16:51:28 GMT  
		Size: 12.2 MB (12197120 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a37ab2fadaed5446beeccf7ca85c53fc1ac1600177cdb40abbe5951c72c8d212`  
		Last Modified: Mon, 23 Mar 2026 16:51:28 GMT  
		Size: 11.8 KB (11768 bytes)  
		MIME: application/vnd.in-toto+json
