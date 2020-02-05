<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `archlinux`

-	[`archlinux:20191006`](#archlinux20191006)
-	[`archlinux:20191105`](#archlinux20191105)
-	[`archlinux:20191205`](#archlinux20191205)
-	[`archlinux:20200106`](#archlinux20200106)
-	[`archlinux:20200205`](#archlinux20200205)
-	[`archlinux:latest`](#archlinuxlatest)

## `archlinux:20191006`

```console
$ docker pull archlinux@sha256:f39d7add5a48567f6c97b54cdde706f834a6d86c3c79c6ce460215ac500c2d87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `archlinux:20191006` - linux; amd64

```console
$ docker pull archlinux@sha256:703de9ba7e6cd9b2d47fe96e857cc8b60f386f70bd96693e156f09b66654eea3
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.0 MB (157036428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f769c15abfb1ef0f7d0f8e9281e2cbe79698ef3d652dd5949b164eca323f86d`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Tue, 15 Oct 2019 01:19:46 GMT
ADD file:a0297838c2d092be25078cf56ae1c047434d974328d2e161feb46c6272c893c0 in / 
# Tue, 15 Oct 2019 01:19:50 GMT
RUN ldconfig && update-ca-trust && locale-gen
# Tue, 15 Oct 2019 01:19:50 GMT
RUN sh -c 'ls usr/lib/sysusers.d/*.conf | /usr/share/libalpm/scripts/systemd-hook sysusers '
# Tue, 15 Oct 2019 01:19:57 GMT
RUN pacman-key --init && pacman-key --populate archlinux
# Tue, 15 Oct 2019 01:19:57 GMT
RUN rm -rf etc/pacman.d/gnupg/{openpgp-revocs.d/,private-keys-v1.d/,pugring.gpg~,gnupg.S.}*
# Tue, 15 Oct 2019 01:19:58 GMT
ENV LANG=en_US.UTF-8
# Tue, 15 Oct 2019 01:19:58 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:29a9b3d832c1c80ca31cb63cff7bbbf09d948bc74f29474d325c22ae4925c93f`  
		Last Modified: Tue, 15 Oct 2019 01:20:37 GMT  
		Size: 154.1 MB (154094977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:633f223bf01d63f7026c5d8fa16ae1a8ca12128f27d26788809e954981874de0`  
		Last Modified: Tue, 15 Oct 2019 01:20:12 GMT  
		Size: 1.6 MB (1591745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c51f018dbc4edccc726589a5df9d51fbdacfdf78f0251f29608828a2ba71bed7`  
		Last Modified: Tue, 15 Oct 2019 01:20:11 GMT  
		Size: 1.1 KB (1143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa88dce40330d63ac577747b9e0d5c579441d76675cd4e7ed81cbd53881a7988`  
		Last Modified: Tue, 15 Oct 2019 01:20:11 GMT  
		Size: 1.3 MB (1348256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd40569445b84002d098f93fce57474bc695df04fbc10b504a0df47239368a6f`  
		Last Modified: Tue, 15 Oct 2019 01:20:11 GMT  
		Size: 307.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `archlinux:20191105`

```console
$ docker pull archlinux@sha256:3fcb6f0c3a1266b579f7d5a89cbb66db1530e8dd533794b9c9588b630255b754
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `archlinux:20191105` - linux; amd64

```console
$ docker pull archlinux@sha256:1097437745db73ba839d60b9b9b96e6648e62751519a1319bfccc849f6a3f74c
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.6 MB (166570023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ee688d008f44d8f6e19d23f251f1b3c7031b51e79ddc0f84e956fc6b0176187`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Tue, 05 Nov 2019 22:20:12 GMT
ADD file:25458d2f6ada9b844ffbbc2f5667646cc2125a77e52ced2e2dbb013bc191f7ce in / 
# Tue, 05 Nov 2019 22:20:16 GMT
RUN ldconfig && update-ca-trust && locale-gen
# Tue, 05 Nov 2019 22:20:17 GMT
RUN sh -c 'ls usr/lib/sysusers.d/*.conf | /usr/share/libalpm/scripts/systemd-hook sysusers '
# Tue, 05 Nov 2019 22:20:27 GMT
RUN pacman-key --init && pacman-key --populate archlinux
# Tue, 05 Nov 2019 22:20:28 GMT
RUN rm -rf etc/pacman.d/gnupg/{openpgp-revocs.d/,private-keys-v1.d/,pugring.gpg~,gnupg.S.}*
# Tue, 05 Nov 2019 22:20:28 GMT
ENV LANG=en_US.UTF-8
# Tue, 05 Nov 2019 22:20:28 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:611c498dd85ddec8b455110ddb6d783509f75f7ed38b6384e242ca0390fe47d8`  
		Last Modified: Tue, 05 Nov 2019 22:21:16 GMT  
		Size: 163.2 MB (163241551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75ef025d1fb2b09b7399e9f351b9e7a5a34698003f00a173270385712b53e0eb`  
		Last Modified: Tue, 05 Nov 2019 22:20:48 GMT  
		Size: 1.6 MB (1591867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2881a4bfd8618552d2839ddd5b13e6bca53709d76df4ec1fd30b1190fc275867`  
		Last Modified: Tue, 05 Nov 2019 22:20:48 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a6ad23bc3869ebf1fa12e9f8f90ba46d33fe06c10597de0d2554a63d19492c9`  
		Last Modified: Tue, 05 Nov 2019 22:20:48 GMT  
		Size: 1.7 MB (1735178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:080b3ed0e730c2f009727cf32abf849de02ab889163c160724b19c0ba2f5faac`  
		Last Modified: Tue, 05 Nov 2019 22:20:48 GMT  
		Size: 299.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `archlinux:20191205`

```console
$ docker pull archlinux@sha256:4e758a6fa19533f6c5367a740ab6868c78a87bbc06f710fb8e336d3bde248833
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `archlinux:20191205` - linux; amd64

```console
$ docker pull archlinux@sha256:ba3d8ab3f76c7c218c6c98380763514e84724f0afae9dcbb61c2125dcf720781
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.1 MB (118073105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b389db977f2cac6eef00cb5e54a80794adc1ebeecb46186e8deaed6b0637919b`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Fri, 06 Dec 2019 23:20:25 GMT
ADD file:0ecbe6fb215979f96729ee65e033dcaac423bc16836b4675135fc3bd3b419148 in / 
# Fri, 06 Dec 2019 23:20:29 GMT
RUN ldconfig && update-ca-trust && locale-gen
# Fri, 06 Dec 2019 23:20:30 GMT
RUN sh -c 'ls usr/lib/sysusers.d/*.conf | /usr/share/libalpm/scripts/systemd-hook sysusers '
# Fri, 06 Dec 2019 23:20:37 GMT
RUN pacman-key --init && pacman-key --populate archlinux
# Fri, 06 Dec 2019 23:20:38 GMT
RUN rm -rf etc/pacman.d/gnupg/{openpgp-revocs.d/,private-keys-v1.d/,pugring.gpg~,gnupg.S.}*
# Fri, 06 Dec 2019 23:20:38 GMT
ENV LANG=en_US.UTF-8
# Fri, 06 Dec 2019 23:20:39 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:94012c774717588b98c5f341e992b71387f9bc2432c3dec54e2a16a7b20639a4`  
		Last Modified: Fri, 06 Dec 2019 23:21:18 GMT  
		Size: 114.9 MB (114877731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb303f4daf3192919262552f62e04d8a54d5a5515e6746690d53124f7aa886f9`  
		Last Modified: Fri, 06 Dec 2019 23:20:56 GMT  
		Size: 1.6 MB (1591886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c003ccab720b38b82a49b1bcf487d3a652fb7d4b86857caf1b1cfbac9d14848c`  
		Last Modified: Fri, 06 Dec 2019 23:20:56 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:611e91f2fbf878b3a7bfda348cf0722517fc043a16464d63ed705c3672d000be`  
		Last Modified: Fri, 06 Dec 2019 23:20:56 GMT  
		Size: 1.6 MB (1602059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d71957b4d7f770a5c5771580b8785bd2b37b01046f7a3be2b550f363b4c5cda6`  
		Last Modified: Fri, 06 Dec 2019 23:20:56 GMT  
		Size: 298.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `archlinux:20200106`

```console
$ docker pull archlinux@sha256:9057a3c8070123672381945d32c598bf7f8e51ebcd17c83383b6b695c3500f24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `archlinux:20200106` - linux; amd64

```console
$ docker pull archlinux@sha256:2e1bdf0192b69df3d2ac30c5279897c232aae362569afa2efba01a01f71061fb
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.5 MB (127549862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0152bf6f0800e4895458ac450649d01f5d23e975185a362a28cf6ae587b73393`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Tue, 07 Jan 2020 23:19:52 GMT
ADD file:57412d849d364b1175de88d9f5258bee961b7cc5e7a9d4d031f8453af655c4fa in / 
# Tue, 07 Jan 2020 23:19:56 GMT
RUN ldconfig && update-ca-trust && locale-gen
# Tue, 07 Jan 2020 23:19:57 GMT
RUN sh -c 'ls usr/lib/sysusers.d/*.conf | /usr/share/libalpm/scripts/systemd-hook sysusers '
# Tue, 07 Jan 2020 23:20:06 GMT
RUN pacman-key --init && pacman-key --populate archlinux
# Tue, 07 Jan 2020 23:20:07 GMT
RUN rm -rf etc/pacman.d/gnupg/{openpgp-revocs.d/,private-keys-v1.d/,pugring.gpg~,gnupg.S.}*
# Tue, 07 Jan 2020 23:20:07 GMT
ENV LANG=en_US.UTF-8
# Tue, 07 Jan 2020 23:20:07 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:4cc56b3c1f51e20a7fd352805ded7e8a4c5b66755d0fdc7d9ae62fe20a5397c4`  
		Last Modified: Tue, 07 Jan 2020 23:21:13 GMT  
		Size: 124.1 MB (124122627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:301fea36cd6b5e893f1f45277d35498d544495b8111115c7ace2438f1a3b8fb1`  
		Last Modified: Tue, 07 Jan 2020 23:20:50 GMT  
		Size: 1.6 MB (1598506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a16580cb32d70452c7e0685072f2196beacdcb0bd0b313a8ddaf21fb0fd3bff`  
		Last Modified: Tue, 07 Jan 2020 23:20:48 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b4488c39e20af5c8cc320db7e673c1161fca1e4f31ad07143e76d5685c63bcd`  
		Last Modified: Tue, 07 Jan 2020 23:20:49 GMT  
		Size: 1.8 MB (1827301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:074e17f44799d40d1b4e9ec99c8ccddead9cf366aefcca5bfbac0692f0aaf707`  
		Last Modified: Tue, 07 Jan 2020 23:20:48 GMT  
		Size: 297.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `archlinux:20200205`

**does not exist** (yet?)

## `archlinux:latest`

```console
$ docker pull archlinux@sha256:9057a3c8070123672381945d32c598bf7f8e51ebcd17c83383b6b695c3500f24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:2e1bdf0192b69df3d2ac30c5279897c232aae362569afa2efba01a01f71061fb
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.5 MB (127549862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0152bf6f0800e4895458ac450649d01f5d23e975185a362a28cf6ae587b73393`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Tue, 07 Jan 2020 23:19:52 GMT
ADD file:57412d849d364b1175de88d9f5258bee961b7cc5e7a9d4d031f8453af655c4fa in / 
# Tue, 07 Jan 2020 23:19:56 GMT
RUN ldconfig && update-ca-trust && locale-gen
# Tue, 07 Jan 2020 23:19:57 GMT
RUN sh -c 'ls usr/lib/sysusers.d/*.conf | /usr/share/libalpm/scripts/systemd-hook sysusers '
# Tue, 07 Jan 2020 23:20:06 GMT
RUN pacman-key --init && pacman-key --populate archlinux
# Tue, 07 Jan 2020 23:20:07 GMT
RUN rm -rf etc/pacman.d/gnupg/{openpgp-revocs.d/,private-keys-v1.d/,pugring.gpg~,gnupg.S.}*
# Tue, 07 Jan 2020 23:20:07 GMT
ENV LANG=en_US.UTF-8
# Tue, 07 Jan 2020 23:20:07 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:4cc56b3c1f51e20a7fd352805ded7e8a4c5b66755d0fdc7d9ae62fe20a5397c4`  
		Last Modified: Tue, 07 Jan 2020 23:21:13 GMT  
		Size: 124.1 MB (124122627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:301fea36cd6b5e893f1f45277d35498d544495b8111115c7ace2438f1a3b8fb1`  
		Last Modified: Tue, 07 Jan 2020 23:20:50 GMT  
		Size: 1.6 MB (1598506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a16580cb32d70452c7e0685072f2196beacdcb0bd0b313a8ddaf21fb0fd3bff`  
		Last Modified: Tue, 07 Jan 2020 23:20:48 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b4488c39e20af5c8cc320db7e673c1161fca1e4f31ad07143e76d5685c63bcd`  
		Last Modified: Tue, 07 Jan 2020 23:20:49 GMT  
		Size: 1.8 MB (1827301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:074e17f44799d40d1b4e9ec99c8ccddead9cf366aefcca5bfbac0692f0aaf707`  
		Last Modified: Tue, 07 Jan 2020 23:20:48 GMT  
		Size: 297.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
