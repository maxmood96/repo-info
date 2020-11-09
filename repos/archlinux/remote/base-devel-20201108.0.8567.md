## `archlinux:base-devel-20201108.0.8567`

```console
$ docker pull archlinux@sha256:9374c2e17de72231bb413e547cdfc96d0156b5e27e0bc73ce4803f6e4ca883b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `archlinux:base-devel-20201108.0.8567` - linux; amd64

```console
$ docker pull archlinux@sha256:b63827b5c4b05c1349e615afbf6adfd4ed1da10a2d79d60a62b162ab59a46006
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.0 MB (221046743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:482c4a34dfa47bc45c082c28444280837b43e229f28d8795305177ece8b744de`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 09 Nov 2020 19:21:43 GMT
COPY dir:4ccd7097e48442170bd10677337727f26c86021a03132c711d021202ffc28b75 in / 
# Mon, 09 Nov 2020 19:21:47 GMT
RUN ldconfig && update-ca-trust && locale-gen
# Mon, 09 Nov 2020 19:21:48 GMT
RUN sh -c 'ls usr/lib/sysusers.d/*.conf | /usr/share/libalpm/scripts/systemd-hook sysusers '
# Mon, 09 Nov 2020 19:21:49 GMT
RUN ln -s /usr/lib/os-release /etc/os-release
# Mon, 09 Nov 2020 19:22:03 GMT
RUN pacman-key --init && pacman-key --populate archlinux && bash -c "rm -rf etc/pacman.d/gnupg/{openpgp-revocs.d/,private-keys-v1.d/,pubring.gpg~,gnupg.S.}*"
# Mon, 09 Nov 2020 19:22:03 GMT
ENV LANG=en_US.UTF-8
# Mon, 09 Nov 2020 19:22:03 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:5fa85902c5877921c2c34e68bf211ceb91534b9c09f1db52a39cfbeb854513cf`  
		Last Modified: Mon, 09 Nov 2020 19:23:32 GMT  
		Size: 218.5 MB (218523842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9611c65a06151300147b5f962baf4b3f17cd27f1d355e4f60c8548a55d45809`  
		Last Modified: Mon, 09 Nov 2020 19:22:55 GMT  
		Size: 1.6 MB (1585250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dc36629d2dc0bd1931e1b723a7e7d3831556b197003a21de8fdc6574acc58cc`  
		Last Modified: Mon, 09 Nov 2020 19:22:55 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52d487bf82e0a0d3d650d8f2f2694e1d2b818095e839df88312c6ee3acb85c48`  
		Last Modified: Mon, 09 Nov 2020 19:22:54 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:819c4d4d6632eb02dd9bf74ef4fc0faf1c87e4a2298e9296e45dcb2ceda356ef`  
		Last Modified: Mon, 09 Nov 2020 19:22:55 GMT  
		Size: 936.4 KB (936384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
