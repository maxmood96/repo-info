## `archlinux:latest`

```console
$ docker pull archlinux@sha256:29670d7f6a5d9ac4eaf90e63c488ad48e99d21ba61ffb6c31a0e15306c953d9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:62c34da77870e6b871fa597774eb670131dfece3ca5d9f5ca20a8923f6853af0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.7 MB (150698269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3c2a2d74968d4cfa7801c87beb1d072c5daf564308881e8c12298d7da201ebb`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 09 Nov 2020 19:20:17 GMT
COPY dir:65dfb913148069566128f539f8b6a6a5b8da0dd6eea7a2342250c996fd2c200c in / 
# Mon, 09 Nov 2020 19:20:21 GMT
RUN ldconfig && update-ca-trust && locale-gen
# Mon, 09 Nov 2020 19:20:23 GMT
RUN sh -c 'ls usr/lib/sysusers.d/*.conf | /usr/share/libalpm/scripts/systemd-hook sysusers '
# Mon, 09 Nov 2020 19:20:26 GMT
RUN ln -s /usr/lib/os-release /etc/os-release
# Mon, 09 Nov 2020 19:20:39 GMT
RUN pacman-key --init && pacman-key --populate archlinux && bash -c "rm -rf etc/pacman.d/gnupg/{openpgp-revocs.d/,private-keys-v1.d/,pubring.gpg~,gnupg.S.}*"
# Mon, 09 Nov 2020 19:20:39 GMT
ENV LANG=en_US.UTF-8
# Mon, 09 Nov 2020 19:20:39 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:1d8c42a4dcd25bc7effd6e2e5e801f481766ffbbc9978870d9760cb3e660e6ea`  
		Last Modified: Mon, 09 Nov 2020 19:22:48 GMT  
		Size: 148.2 MB (148175805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eac260ed46fc8290fce81f7da22e7866c72898e68a79060fcc2f7456c662d385`  
		Last Modified: Mon, 09 Nov 2020 19:22:22 GMT  
		Size: 1.6 MB (1584803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbcfe54348aa8c69f5f2d2c7df17e0c94f5c6a018eb49190dd7a548ff1a3fd1e`  
		Last Modified: Mon, 09 Nov 2020 19:22:21 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45be770bc8c643a743696e81683a36c6093bfd571308c212576fd5493cd869e3`  
		Last Modified: Mon, 09 Nov 2020 19:22:22 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1668eeb355c4bcaa516eef218bb9101a831e7d3b4d024d54ac249fcc3792b80a`  
		Last Modified: Mon, 09 Nov 2020 19:22:22 GMT  
		Size: 936.4 KB (936393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
