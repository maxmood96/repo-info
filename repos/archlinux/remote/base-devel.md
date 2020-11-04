## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:93ebac3c3c6aa236aabf50507766ec896a566262abfc1e1354b81c9024136257
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:2de343a5b3be645972cab2c577b294d22819fa3417a5d2d88d682073f2a1ce5c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.0 MB (221031956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6eb0ac01bd73590c415d6d140997078d9193da52bd3bdcde51bde4ccb792e02e`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Wed, 04 Nov 2020 20:21:28 GMT
COPY dir:3bbd6d707516b932ffd619fa524b56af1f1856eba3a59fdadf696785cc6ab9b5 in / 
# Wed, 04 Nov 2020 20:21:32 GMT
RUN ldconfig && update-ca-trust && locale-gen
# Wed, 04 Nov 2020 20:21:33 GMT
RUN sh -c 'ls usr/lib/sysusers.d/*.conf | /usr/share/libalpm/scripts/systemd-hook sysusers '
# Wed, 04 Nov 2020 20:21:34 GMT
RUN ln -s /usr/lib/os-release /etc/os-release
# Wed, 04 Nov 2020 20:21:48 GMT
RUN pacman-key --init && pacman-key --populate archlinux && bash -c "rm -rf etc/pacman.d/gnupg/{openpgp-revocs.d/,private-keys-v1.d/,pubring.gpg~,gnupg.S.}*"
# Wed, 04 Nov 2020 20:21:48 GMT
ENV LANG=en_US.UTF-8
# Wed, 04 Nov 2020 20:21:48 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:dc37e78fa77e6788859b037b93c2651f6f7389bdc7c1609e8fa41fcc1b004d1c`  
		Last Modified: Wed, 04 Nov 2020 20:23:20 GMT  
		Size: 218.5 MB (218509078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dc6b3830f30c0bb731f38ebbc84aea9dfe9ba1fef5df8c5e1ce9ed3dc0581b9`  
		Last Modified: Wed, 04 Nov 2020 20:22:33 GMT  
		Size: 1.6 MB (1585223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eb3edc663d3925af83e1e3395b95eac3a41be5412e9bf42bb82b7f600d8425a`  
		Last Modified: Wed, 04 Nov 2020 20:22:33 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6044b7e30446da300b2355d7c33ff02d44afed0f1dc9f1fea08cb990d7793bdf`  
		Last Modified: Wed, 04 Nov 2020 20:22:33 GMT  
		Size: 134.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c925352aecf100bb003b448f54e10ff2f642fb77ad404d8cc536b2cecfb837c`  
		Last Modified: Wed, 04 Nov 2020 20:22:32 GMT  
		Size: 936.4 KB (936391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
