## `debian:oldstable-backports`

```console
$ docker pull debian@sha256:1d6257ded8df296a094318786459d9f9710a833cc38cb547cd232105e7f7fc8c
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
$ docker pull debian@sha256:06f14d6293f794573205190153eda56e0fbf0370c7c5481bdd114907d6856e55
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.1 MB (55081559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0aa371d472df6292d6aa7374990b16cdbb3f2a9ff69d9134777924f02d802a8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:31:18 GMT
ADD file:fa640ee07f5a1b92a251f94b312b1eb8701db72aca7befd9f6332395216c87cb in / 
# Wed, 04 Sep 2024 22:31:18 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:31:23 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:e6c19f19bd45c1f6fe66d27571cf1df1e4fb7a7152998ef94bc7868d64e14d5f`  
		Last Modified: Wed, 04 Sep 2024 22:35:12 GMT  
		Size: 55.1 MB (55081332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e377d1d68fc68df7cabcbbdc3813c29ee929e2a80d530bf338e5eae8aa332fda`  
		Last Modified: Wed, 04 Sep 2024 22:35:19 GMT  
		Size: 227.0 B  
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
$ docker pull debian@sha256:994841a528e91a7d0551e6bc0d933b8c20cb46691d94f28e349a29c8b102775c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.1 MB (56076372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef12386d05d53c44368fb918eb9be3a53f69609903606856a3f1fd113189cf9b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:45:06 GMT
ADD file:80987a1bc79cda72954e1a362e5bab721a49cb043c31d7a5e0a0f6ef7724047a in / 
# Wed, 04 Sep 2024 22:45:07 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:45:11 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:ddc3d843871f2ff4e892fa6a6c6e548fa150061d0f837c1e78195357bf15944b`  
		Last Modified: Wed, 04 Sep 2024 22:49:11 GMT  
		Size: 56.1 MB (56076147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:081f84e18f70edf646620793f4ef38903896430bfe0b1cd5b968bd1eba92b234`  
		Last Modified: Wed, 04 Sep 2024 22:49:18 GMT  
		Size: 225.0 B  
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
