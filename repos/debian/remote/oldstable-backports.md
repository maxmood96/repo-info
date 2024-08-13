## `debian:oldstable-backports`

```console
$ docker pull debian@sha256:1ce1a3d220dc4c41e7d368b61db52709c68b31221e5eafd7ebee1931486a338c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `debian:oldstable-backports` - linux; amd64

```console
$ docker pull debian@sha256:2355cc85f7b4154448dadf3918d592d9c84e324d2b7fb40caa5234c300b98ef0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.1 MB (55084974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c918ad46bc35099911e1f99fd79c29bd19059608c85094648c32950efee48faa`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:20:51 GMT
ADD file:a23ad42ddd755d0c3dafb161963502e1a275e1908733b4c7c4f5fed199e0a4dd in / 
# Tue, 13 Aug 2024 00:20:51 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 00:20:56 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:6bf2fad52ddedb373cdd11fff6106ce90bc514b208870ad6a6bc5efa810135f9`  
		Last Modified: Tue, 13 Aug 2024 00:24:41 GMT  
		Size: 55.1 MB (55084751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15018df19171670131c6840042c963a02afc7b3baff6b52bf44de3aaf539c231`  
		Last Modified: Tue, 13 Aug 2024 00:24:49 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:9b10b35d2b6377eb9347ca189ff6e9f218b733a26c472e634127ec3b9eb36771
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.6 MB (52589245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d80af56d4dda4910408d70de819d2ab117249481bede54857763c6be7dc2f1c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:55:54 GMT
ADD file:335a9be5101a9c2c3b694e43329d9c282915249bb1c121e4899694b4c345db3c in / 
# Tue, 13 Aug 2024 00:55:54 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 00:55:57 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:7d788dbf6162dd0215380531bdc06ab4b069b8050669f0256149c49abc094bf4`  
		Last Modified: Tue, 13 Aug 2024 00:59:29 GMT  
		Size: 52.6 MB (52589022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5894957f2379cf56916db2a667e59c006465bf34c6c46e3981caa5563c484f94`  
		Last Modified: Tue, 13 Aug 2024 00:59:39 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:666b8e081457b93fe5a470676731866723612114748f4af8a55e09664a2f71a7
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 MB (50242592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1a25039098a1f7e934d7476fd9418f9c12414e3c5afdd0b9b01b13cd764a220`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:58:03 GMT
ADD file:fbffb42a64d87f23a220583997bef782711a07c01cc1f6b695ff8640a5123d3b in / 
# Tue, 13 Aug 2024 00:58:04 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 00:58:08 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:c8294e44b911282cc62c1fe335372bb78ce2b7ce7346c2f2e6f7d1df768fc292`  
		Last Modified: Tue, 13 Aug 2024 01:01:58 GMT  
		Size: 50.2 MB (50242367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c02c4d73843741d5e74a0f762db60b4b6bc0487f5a49a126222a7bf85881826`  
		Last Modified: Tue, 13 Aug 2024 01:02:06 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:d6e19b190f31f830cc907342004b79f80fe2e82a754b00326636e971abaca072
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53730117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94341935e463a8116da0f777f8d53656c5d752ca019156d2177e734377cf8f35`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:40:13 GMT
ADD file:e32c27be4ad6f42f28d9d2ee50a1f3ccc28bbf1d6dbfa547b64ceea06dc96a9e in / 
# Tue, 13 Aug 2024 00:40:13 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 00:40:16 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:ce67a5a207b5ec2d0411ac74f064de7500499b2ccfb94e875ec8cfd375d7c65d`  
		Last Modified: Tue, 13 Aug 2024 00:43:42 GMT  
		Size: 53.7 MB (53729894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de0defaf8ec7383b22162abb5dc55562ae8888a2d28912ec6dfd9c1be5bbf3a4`  
		Last Modified: Tue, 13 Aug 2024 00:43:49 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; 386

```console
$ docker pull debian@sha256:86befc8f017da855fe356bdb381def8f5a1ec13c25b1b1345f650fa87438cc8b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.1 MB (56074313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c1289360fd7d62e6b5327bdc117343ecaee5c0e66c6aa0339d8ffe7fe99fcc0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:39:29 GMT
ADD file:10707af2748644df26353b64715f89b8e3723f75aae60d7f03a4f169de5df217 in / 
# Tue, 13 Aug 2024 00:39:30 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 00:39:33 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:5f81aee582ae09590d2aaef29272cf0c9bbad317f3211b17d62f19fffdfdb6b5`  
		Last Modified: Tue, 13 Aug 2024 00:43:37 GMT  
		Size: 56.1 MB (56074090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bae9b73b6c68c0b79efd42bab694e9a18be8bbf1c014c9a1ab39389ecfad6163`  
		Last Modified: Tue, 13 Aug 2024 00:43:45 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; mips64le

```console
$ docker pull debian@sha256:951aef1c79cef78eeda16394ce26e57b2fd2724cfcdc386c3946b05f61258d47
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53310822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe44ca8444a5137912e5b499e4e4c380e675b339ae1cddfc103db7f802830401`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:13:05 GMT
ADD file:e075a3635fa54e73b3ab73bcdb7e714a0573c7f2de3e10cf584653bc3c8e895a in / 
# Tue, 13 Aug 2024 00:13:12 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 00:13:27 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:a4c7a7dcd3bddff4f9649e851e2758d0e2c9a4e78e43dd90a92e7fed7ebabd47`  
		Last Modified: Tue, 13 Aug 2024 00:24:36 GMT  
		Size: 53.3 MB (53310595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8b523c1fe779b226fa265872ee818b8470dcf3a46d9fa368b35263d353c4242`  
		Last Modified: Tue, 13 Aug 2024 00:24:45 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:55f2ac40d58e2c799ece113d7c2f45730decc100367a377ce137c2ef32027b8f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.0 MB (58954884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4dac42e068b95f2aca6126586bb3e301f8cf60eef76e8daaf7d7245007f5355`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:22:43 GMT
ADD file:5d452bb95b0c427755de721ae849bd23f9450d55a57c8641474afc13db17b3f1 in / 
# Tue, 13 Aug 2024 00:22:46 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 00:22:51 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:569451625922fd229f93fd26b504954375543232bb3316613f310ef1da8accd6`  
		Last Modified: Tue, 13 Aug 2024 00:27:34 GMT  
		Size: 59.0 MB (58954657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f55bd82c0c6467d1feb679088169ab4fbff90d4c753351ef9efa3b0c6c3afc6`  
		Last Modified: Tue, 13 Aug 2024 00:27:42 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; s390x

```console
$ docker pull debian@sha256:ee1ca360a118a67590e66d06bc19f8de10d96dd4d893485f5b8765048299c251
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53324284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa53421b65ce21bf37d6f9be82cf8eca4528844931a4ea30f7804f3876b7b9c0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:43:25 GMT
ADD file:40a99bec6b921c924289a2784fac7fa09d77ae5d7eb7eee17698791e6fb6647e in / 
# Tue, 13 Aug 2024 00:43:27 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 00:43:35 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:3e44302faddd925455a1c847003aa3e7d8641143918d0250bab96441f42ddd82`  
		Last Modified: Tue, 13 Aug 2024 00:48:10 GMT  
		Size: 53.3 MB (53324061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19877028e7847474eb92df004e84fe0d6e33fc9b5ddbd07b8b3d8595793b959b`  
		Last Modified: Tue, 13 Aug 2024 00:48:15 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
