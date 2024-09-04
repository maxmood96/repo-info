## `debian:oldstable-backports`

```console
$ docker pull debian@sha256:d2cbe781e7f75abc76ef85e6e02f73e4fd42dd22287a73fff3f9d4601e09c442
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
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
$ docker pull debian@sha256:15bc769382be5e9c7d387e03bc60e6accb961c567c4476629fba3fb43133a150
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.6 MB (52583007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:896c747fc8d552592cce8f91ad9f91b410d45cc5e77fc1f4c8aa1bf7031ba170`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:48:55 GMT
ADD file:7d5ee5743d2923bca25b678c62afd60a5d6477c1571933f669873e727d77a088 in / 
# Wed, 04 Sep 2024 21:48:57 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 21:49:00 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:2f94ed228f09e345a68ccd61bd5cc808c9d0e0290b3e3ac72e2fa27e8ad41a35`  
		Last Modified: Wed, 04 Sep 2024 21:52:34 GMT  
		Size: 52.6 MB (52582783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eab7dbcd7d7eedc59c11a3395dd0f9e605d8aed80bda9be3cc770a37aab83bc`  
		Last Modified: Wed, 04 Sep 2024 21:52:41 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:6e02d255907cd2aa796cb52c794e3d22cae656e4239061a674324653ff5e5f51
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 MB (50240491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55649b38f1653b909ac2e93b334b36039ed0c39ba51eb6ba2c29c721f34f95e1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:58:38 GMT
ADD file:1491f8eddfc713dac57f3c08caaf2ad833f4185044b61395ba260517a39cb5ba in / 
# Wed, 04 Sep 2024 21:58:39 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 21:58:42 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:0ad03ef6392933717d8aaa8084ca76329c1b63498bd61f17227357b08afbf819`  
		Last Modified: Wed, 04 Sep 2024 22:02:46 GMT  
		Size: 50.2 MB (50240265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3f00c05b05d67c46d071ecd7a483ff06441d48d4434fc32975f353e75d2f5d5`  
		Last Modified: Wed, 04 Sep 2024 22:02:53 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:15afb321091b757de4505365301cac3e2a7083cc828d0bd7f3a27e77feba6ebd
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53731837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba25526936242ad3ca6ff22d5660b340eae66a4bbb7f9c242a0976de6f5399c5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:40:14 GMT
ADD file:8c9f5386a01aaa5837e1e1347350c4ddacf829295eb50a39a7e5b05ac2fd4b65 in / 
# Wed, 04 Sep 2024 21:40:15 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 21:40:18 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:b0392e397a831b6f1f54a92f4e3593642c5fdf645b301586cfe7f9f58a627184`  
		Last Modified: Wed, 04 Sep 2024 21:43:26 GMT  
		Size: 53.7 MB (53731610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cc77fdfebf1426538d0db5ce6f0f2bf4cfabf146788b4897b96c2b99ca157ce`  
		Last Modified: Wed, 04 Sep 2024 21:43:33 GMT  
		Size: 227.0 B  
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

### `debian:oldstable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:80458ec6c57ad01813eda27f0ea7566113ca6743ea52979c0f5ab965f736b84a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.0 MB (58950346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74b75311d54e1c79d9790a547575e9ccfdb5e09da4689c20c0ca39e0b8cd0d22`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:26:30 GMT
ADD file:334aa396c7a04dd8faabd698293c296e9d578d69e315024860543df72ab2a9e2 in / 
# Wed, 04 Sep 2024 22:26:33 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:26:38 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:8ebe7eae5809c0b8b2236e3e2f8dfaccd7ef7c6438c1f4f37e42124bda07a86d`  
		Last Modified: Wed, 04 Sep 2024 22:31:18 GMT  
		Size: 59.0 MB (58950123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe67a24f52fc7e573f7d9a6fa66376381c3d7680d22145eb151adaa501ad392d`  
		Last Modified: Wed, 04 Sep 2024 22:31:26 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; s390x

```console
$ docker pull debian@sha256:0156ae1ff022f43c87021ebced16f6d828e17a50226d002dafe43a36903bd31e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53317443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13c62bb15503de4831f5ea198e49efe69fdbfbce7f8863467fbcff13965122b4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:43:39 GMT
ADD file:0e9421e45782d72ae01fba29cf7ab45205b6aeae3f10907baaa646b3d0761386 in / 
# Wed, 04 Sep 2024 21:43:42 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 21:43:49 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:583ee6158926b881c6b1f01b9387ae4ac1c2ca8e49f38a71657274b2d607791f`  
		Last Modified: Wed, 04 Sep 2024 21:48:23 GMT  
		Size: 53.3 MB (53317219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21349200dc4715512e5191369be93cd4c78c910fa0b787e0a95bffb4ad188a83`  
		Last Modified: Wed, 04 Sep 2024 21:48:28 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
