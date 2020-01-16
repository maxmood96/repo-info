<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `mono`

-	[`mono:5`](#mono5)
-	[`mono:5.20`](#mono520)
-	[`mono:5.20.1`](#mono5201)
-	[`mono:5.20.1.34`](#mono520134)
-	[`mono:5.20.1.34-slim`](#mono520134-slim)
-	[`mono:5.20.1-slim`](#mono5201-slim)
-	[`mono:5.20-slim`](#mono520-slim)
-	[`mono:5-slim`](#mono5-slim)
-	[`mono:6`](#mono6)
-	[`mono:6.6`](#mono66)
-	[`mono:6.6.0`](#mono660)
-	[`mono:6.6.0.161`](#mono660161)
-	[`mono:6.6.0.161-slim`](#mono660161-slim)
-	[`mono:6.6.0-slim`](#mono660-slim)
-	[`mono:6.6-slim`](#mono66-slim)
-	[`mono:6.8`](#mono68)
-	[`mono:6.8.0`](#mono680)
-	[`mono:6.8.0.96`](#mono68096)
-	[`mono:6.8.0.96-slim`](#mono68096-slim)
-	[`mono:6.8.0-slim`](#mono680-slim)
-	[`mono:6.8-slim`](#mono68-slim)
-	[`mono:6-slim`](#mono6-slim)
-	[`mono:latest`](#monolatest)
-	[`mono:slim`](#monoslim)

## `mono:5`

```console
$ docker pull mono@sha256:31176b864859ad670d8d30fd14edf662f8b32012cc41eafb9ea2a475542a1077
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:5` - linux; amd64

```console
$ docker pull mono@sha256:5c3479e37ebaba3938b41d85e43aa685b34b38c7d39f65838ccc250a77a1bdfe
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.3 MB (218283926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:843d1b62c0468f21ddbfb2ead8f14088f88b3483c3d7c5bbc29fcb42f3a8e8f5`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:47 GMT
ADD file:90a2c81769a336bed3f731f44a385f2a65b0916f517a0b77c06c224579bf9a9a in / 
# Sat, 28 Dec 2019 04:23:47 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 13:16:12 GMT
ENV MONO_VERSION=5.20.1.34
# Sat, 28 Dec 2019 13:16:24 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 13:17:03 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 28 Dec 2019 13:47:56 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:804555ee037604c40de144f9f8da0d826d38db82f15d74cded32790fe279a8f6`  
		Last Modified: Sat, 28 Dec 2019 04:28:38 GMT  
		Size: 22.5 MB (22524609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8529aa2b8c8794ada5de4f9745d3c774968df5014c707878957d1a32ac17603`  
		Last Modified: Sat, 28 Dec 2019 13:48:56 GMT  
		Size: 244.5 KB (244484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:972ee02007ec21f650fb90f3cac4c917ac5b5a84240a1092ff9be02b256bad72`  
		Last Modified: Sat, 28 Dec 2019 13:49:08 GMT  
		Size: 55.5 MB (55521389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:239a7387a2c6ed35e9e5467be5fcd6f83491d432b82e02ec511057d4c8575205`  
		Last Modified: Sat, 28 Dec 2019 13:50:58 GMT  
		Size: 140.0 MB (139993444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5` - linux; arm variant v5

```console
$ docker pull mono@sha256:921141ae8dd056ee2c6ab66dde3ee626f76ecebd3941aaef44a81385fa7eb3e6
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.0 MB (170952313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3270863ca29345901057a594ed47d2cb0e53b9b46570af2b4297f3a0e092cfa3`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:53:16 GMT
ADD file:7d6af454b55cb354e31c096e935358dd5914688ded04ebc76243a4ff598c4495 in / 
# Sat, 28 Dec 2019 04:53:18 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 07:31:47 GMT
ENV MONO_VERSION=5.20.1.34
# Sat, 28 Dec 2019 07:32:25 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 07:33:38 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 28 Dec 2019 07:43:54 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:af28f499fd964f4506ea46c2ac342bc52328a8c30cd633661b69f383a5144e9b`  
		Last Modified: Sat, 28 Dec 2019 05:00:23 GMT  
		Size: 21.2 MB (21202822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e30f4dec85338cf63b2a0a4635e2307d966fbfa5356fe9e83d6a9bcf294768c4`  
		Last Modified: Sat, 28 Dec 2019 07:44:59 GMT  
		Size: 244.6 KB (244563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d859f970551d160b36092ef79b226a92798c6c82b5610774fb345988f6ab6cb`  
		Last Modified: Sat, 28 Dec 2019 07:45:08 GMT  
		Size: 24.3 MB (24265462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efb69e22f6d5bc15e3d4811d51cca77b50460d4f38ad4131151a2df9b8fee768`  
		Last Modified: Sat, 28 Dec 2019 07:48:01 GMT  
		Size: 125.2 MB (125239466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5` - linux; arm variant v7

```console
$ docker pull mono@sha256:ea5d643ecc5f26c0f9f1edeb49fee6ea5323762e8727d392a1f813c4b8862460
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.0 MB (167004578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:631abf1b9406641e5331da51a0d793dd163877e353aece2468f77d0b962d5775`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 05:03:51 GMT
ADD file:2002ba672e32ae75369830ed6a4734ce62e0118e42390b4d657f0985d6b7fd6a in / 
# Sat, 28 Dec 2019 05:03:53 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 07:39:44 GMT
ENV MONO_VERSION=5.20.1.34
# Sat, 28 Dec 2019 07:40:06 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 07:40:54 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 28 Dec 2019 07:50:10 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:77cf262539006c8df77496f500f74a8c1edd158062440fd94d43d5b1292cefee`  
		Last Modified: Sat, 28 Dec 2019 05:11:13 GMT  
		Size: 19.3 MB (19311587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5d99eb936b9cc5835bf59846bd4e0ae6c236cda6f4adce2cb3d14125cb51956`  
		Last Modified: Sat, 28 Dec 2019 07:51:22 GMT  
		Size: 244.6 KB (244557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08fd6bf39cd6ba01aa22f88d8bed99d3c486440b3a5a1d22c82716aa505d7702`  
		Last Modified: Sat, 28 Dec 2019 07:51:30 GMT  
		Size: 23.6 MB (23561478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42a7e7be5a6639501eb7d74f9ca29ade62656f3ca932b2c23aaca5ff7ea944c5`  
		Last Modified: Sat, 28 Dec 2019 07:54:12 GMT  
		Size: 123.9 MB (123886956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:63f81fec16f4d06039611927c73b16343f5b754011fa30d6eb203a8cbca341f6
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.8 MB (187816201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a39a2a666a7d75dfb72de8ea33faba47d1dfe373d964481dac471c5a8048e36`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:43:36 GMT
ADD file:ba40f5080cbd89c576c350bfe5acfe16f2ec59636fdb082efc3a8cef66ae7cb7 in / 
# Sat, 28 Dec 2019 04:43:39 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 08:42:12 GMT
ENV MONO_VERSION=5.20.1.34
# Sat, 28 Dec 2019 08:42:34 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 08:43:17 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 28 Dec 2019 08:51:26 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:588374d57fdb5120d024340eef3d8927af23a5b806d41b4f049ee430a153c0b4`  
		Last Modified: Sat, 28 Dec 2019 04:49:14 GMT  
		Size: 20.4 MB (20385801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:643f8d37cb48de8371d76dd11de4426d0de6e6b6f437e904e981c69341183784`  
		Last Modified: Sat, 28 Dec 2019 08:52:37 GMT  
		Size: 244.4 KB (244409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4eb44ac018125d88f4c42299e8ddfc11bf3983fda5ec1626f7e7dff77c32323`  
		Last Modified: Sat, 28 Dec 2019 08:52:47 GMT  
		Size: 28.2 MB (28156055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:390946e3d8f4fc0557faba9b870bac3bab643073f29e0b9d32e7035b3b634083`  
		Last Modified: Sat, 28 Dec 2019 08:55:20 GMT  
		Size: 139.0 MB (139029936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5` - linux; 386

```console
$ docker pull mono@sha256:f7dc31da4a9c0214be8de4be179c3447a71b7b3de432db0a73f592aa388349e8
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.8 MB (227783487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfbff081eeb3cc7d2fbd105c967757897aedc5e0aa95508184be517694b48419`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:42:05 GMT
ADD file:d43798bcf0e72b342c261b8585dde072d9363d19fab4b8d9f08f15db189f287b in / 
# Sat, 28 Dec 2019 04:42:05 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 08:55:21 GMT
ENV MONO_VERSION=5.20.1.34
# Sat, 28 Dec 2019 08:55:34 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 08:56:06 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 28 Dec 2019 09:03:30 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:2cb401c016d2f9802d5ef9cf6c6dc07251e9f87757a0de0a8df318fb7f00385c`  
		Last Modified: Sat, 28 Dec 2019 04:47:36 GMT  
		Size: 23.2 MB (23152142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b34b6f7471907c646ec285955dc4cf7094149b0ad93ea3e95125c4ef5f5d1171`  
		Last Modified: Sat, 28 Dec 2019 09:04:39 GMT  
		Size: 244.5 KB (244474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e1c87cf35f42f1f93ef3f7676dee0b1b3f1ca6657c6afa49443d888dbc3360d`  
		Last Modified: Sat, 28 Dec 2019 09:04:53 GMT  
		Size: 58.6 MB (58551781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:724b594c451feb85210631e54662992230c04f5e689387accacb9bf2825c06ed`  
		Last Modified: Sat, 28 Dec 2019 09:07:08 GMT  
		Size: 145.8 MB (145835090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5` - linux; ppc64le

```console
$ docker pull mono@sha256:b414ce326f06449a5a441ad050f57286bf41f79b0e0130a25928f9f9617f3e8e
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.3 MB (173304358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee71b36f2a14a9487be1b834ccb9a4c1682b90900f74f6a88ba2a4c937fa4272`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:21 GMT
ADD file:a1ee5955ff3ede8df9558f4bec0c7962d54c43374f857e1da7e2639ddf82a9f1 in / 
# Sat, 28 Dec 2019 04:23:24 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 06:05:00 GMT
ENV MONO_VERSION=5.20.1.34
# Sat, 28 Dec 2019 06:05:42 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 06:06:42 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 28 Dec 2019 06:21:25 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:af52e7ef6e83efadeae17be91daa6ecf61b7dfb39709c29be9b24876e60c0e36`  
		Last Modified: Sat, 28 Dec 2019 04:33:19 GMT  
		Size: 22.8 MB (22800791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:657bad46700417171f7961a2ff50ecc946522119a9a065f23416906ee79d822d`  
		Last Modified: Sat, 28 Dec 2019 06:22:56 GMT  
		Size: 244.5 KB (244499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13c9779877dadfcd9c157fa02d2fbd6becf203c18e9c2727702df72179644d61`  
		Last Modified: Sat, 28 Dec 2019 06:23:14 GMT  
		Size: 24.6 MB (24638971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f31ee19914bb9f2e2b65604baa6905997d5f54e1d4012f6ed60ed63ad1b3c735`  
		Last Modified: Sat, 28 Dec 2019 06:25:31 GMT  
		Size: 125.6 MB (125620097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:5.20`

```console
$ docker pull mono@sha256:31176b864859ad670d8d30fd14edf662f8b32012cc41eafb9ea2a475542a1077
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:5.20` - linux; amd64

```console
$ docker pull mono@sha256:5c3479e37ebaba3938b41d85e43aa685b34b38c7d39f65838ccc250a77a1bdfe
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.3 MB (218283926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:843d1b62c0468f21ddbfb2ead8f14088f88b3483c3d7c5bbc29fcb42f3a8e8f5`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:47 GMT
ADD file:90a2c81769a336bed3f731f44a385f2a65b0916f517a0b77c06c224579bf9a9a in / 
# Sat, 28 Dec 2019 04:23:47 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 13:16:12 GMT
ENV MONO_VERSION=5.20.1.34
# Sat, 28 Dec 2019 13:16:24 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 13:17:03 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 28 Dec 2019 13:47:56 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:804555ee037604c40de144f9f8da0d826d38db82f15d74cded32790fe279a8f6`  
		Last Modified: Sat, 28 Dec 2019 04:28:38 GMT  
		Size: 22.5 MB (22524609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8529aa2b8c8794ada5de4f9745d3c774968df5014c707878957d1a32ac17603`  
		Last Modified: Sat, 28 Dec 2019 13:48:56 GMT  
		Size: 244.5 KB (244484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:972ee02007ec21f650fb90f3cac4c917ac5b5a84240a1092ff9be02b256bad72`  
		Last Modified: Sat, 28 Dec 2019 13:49:08 GMT  
		Size: 55.5 MB (55521389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:239a7387a2c6ed35e9e5467be5fcd6f83491d432b82e02ec511057d4c8575205`  
		Last Modified: Sat, 28 Dec 2019 13:50:58 GMT  
		Size: 140.0 MB (139993444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20` - linux; arm variant v5

```console
$ docker pull mono@sha256:921141ae8dd056ee2c6ab66dde3ee626f76ecebd3941aaef44a81385fa7eb3e6
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.0 MB (170952313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3270863ca29345901057a594ed47d2cb0e53b9b46570af2b4297f3a0e092cfa3`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:53:16 GMT
ADD file:7d6af454b55cb354e31c096e935358dd5914688ded04ebc76243a4ff598c4495 in / 
# Sat, 28 Dec 2019 04:53:18 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 07:31:47 GMT
ENV MONO_VERSION=5.20.1.34
# Sat, 28 Dec 2019 07:32:25 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 07:33:38 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 28 Dec 2019 07:43:54 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:af28f499fd964f4506ea46c2ac342bc52328a8c30cd633661b69f383a5144e9b`  
		Last Modified: Sat, 28 Dec 2019 05:00:23 GMT  
		Size: 21.2 MB (21202822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e30f4dec85338cf63b2a0a4635e2307d966fbfa5356fe9e83d6a9bcf294768c4`  
		Last Modified: Sat, 28 Dec 2019 07:44:59 GMT  
		Size: 244.6 KB (244563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d859f970551d160b36092ef79b226a92798c6c82b5610774fb345988f6ab6cb`  
		Last Modified: Sat, 28 Dec 2019 07:45:08 GMT  
		Size: 24.3 MB (24265462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efb69e22f6d5bc15e3d4811d51cca77b50460d4f38ad4131151a2df9b8fee768`  
		Last Modified: Sat, 28 Dec 2019 07:48:01 GMT  
		Size: 125.2 MB (125239466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20` - linux; arm variant v7

```console
$ docker pull mono@sha256:ea5d643ecc5f26c0f9f1edeb49fee6ea5323762e8727d392a1f813c4b8862460
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.0 MB (167004578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:631abf1b9406641e5331da51a0d793dd163877e353aece2468f77d0b962d5775`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 05:03:51 GMT
ADD file:2002ba672e32ae75369830ed6a4734ce62e0118e42390b4d657f0985d6b7fd6a in / 
# Sat, 28 Dec 2019 05:03:53 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 07:39:44 GMT
ENV MONO_VERSION=5.20.1.34
# Sat, 28 Dec 2019 07:40:06 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 07:40:54 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 28 Dec 2019 07:50:10 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:77cf262539006c8df77496f500f74a8c1edd158062440fd94d43d5b1292cefee`  
		Last Modified: Sat, 28 Dec 2019 05:11:13 GMT  
		Size: 19.3 MB (19311587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5d99eb936b9cc5835bf59846bd4e0ae6c236cda6f4adce2cb3d14125cb51956`  
		Last Modified: Sat, 28 Dec 2019 07:51:22 GMT  
		Size: 244.6 KB (244557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08fd6bf39cd6ba01aa22f88d8bed99d3c486440b3a5a1d22c82716aa505d7702`  
		Last Modified: Sat, 28 Dec 2019 07:51:30 GMT  
		Size: 23.6 MB (23561478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42a7e7be5a6639501eb7d74f9ca29ade62656f3ca932b2c23aaca5ff7ea944c5`  
		Last Modified: Sat, 28 Dec 2019 07:54:12 GMT  
		Size: 123.9 MB (123886956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:63f81fec16f4d06039611927c73b16343f5b754011fa30d6eb203a8cbca341f6
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.8 MB (187816201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a39a2a666a7d75dfb72de8ea33faba47d1dfe373d964481dac471c5a8048e36`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:43:36 GMT
ADD file:ba40f5080cbd89c576c350bfe5acfe16f2ec59636fdb082efc3a8cef66ae7cb7 in / 
# Sat, 28 Dec 2019 04:43:39 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 08:42:12 GMT
ENV MONO_VERSION=5.20.1.34
# Sat, 28 Dec 2019 08:42:34 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 08:43:17 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 28 Dec 2019 08:51:26 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:588374d57fdb5120d024340eef3d8927af23a5b806d41b4f049ee430a153c0b4`  
		Last Modified: Sat, 28 Dec 2019 04:49:14 GMT  
		Size: 20.4 MB (20385801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:643f8d37cb48de8371d76dd11de4426d0de6e6b6f437e904e981c69341183784`  
		Last Modified: Sat, 28 Dec 2019 08:52:37 GMT  
		Size: 244.4 KB (244409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4eb44ac018125d88f4c42299e8ddfc11bf3983fda5ec1626f7e7dff77c32323`  
		Last Modified: Sat, 28 Dec 2019 08:52:47 GMT  
		Size: 28.2 MB (28156055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:390946e3d8f4fc0557faba9b870bac3bab643073f29e0b9d32e7035b3b634083`  
		Last Modified: Sat, 28 Dec 2019 08:55:20 GMT  
		Size: 139.0 MB (139029936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20` - linux; 386

```console
$ docker pull mono@sha256:f7dc31da4a9c0214be8de4be179c3447a71b7b3de432db0a73f592aa388349e8
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.8 MB (227783487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfbff081eeb3cc7d2fbd105c967757897aedc5e0aa95508184be517694b48419`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:42:05 GMT
ADD file:d43798bcf0e72b342c261b8585dde072d9363d19fab4b8d9f08f15db189f287b in / 
# Sat, 28 Dec 2019 04:42:05 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 08:55:21 GMT
ENV MONO_VERSION=5.20.1.34
# Sat, 28 Dec 2019 08:55:34 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 08:56:06 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 28 Dec 2019 09:03:30 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:2cb401c016d2f9802d5ef9cf6c6dc07251e9f87757a0de0a8df318fb7f00385c`  
		Last Modified: Sat, 28 Dec 2019 04:47:36 GMT  
		Size: 23.2 MB (23152142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b34b6f7471907c646ec285955dc4cf7094149b0ad93ea3e95125c4ef5f5d1171`  
		Last Modified: Sat, 28 Dec 2019 09:04:39 GMT  
		Size: 244.5 KB (244474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e1c87cf35f42f1f93ef3f7676dee0b1b3f1ca6657c6afa49443d888dbc3360d`  
		Last Modified: Sat, 28 Dec 2019 09:04:53 GMT  
		Size: 58.6 MB (58551781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:724b594c451feb85210631e54662992230c04f5e689387accacb9bf2825c06ed`  
		Last Modified: Sat, 28 Dec 2019 09:07:08 GMT  
		Size: 145.8 MB (145835090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20` - linux; ppc64le

```console
$ docker pull mono@sha256:b414ce326f06449a5a441ad050f57286bf41f79b0e0130a25928f9f9617f3e8e
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.3 MB (173304358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee71b36f2a14a9487be1b834ccb9a4c1682b90900f74f6a88ba2a4c937fa4272`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:21 GMT
ADD file:a1ee5955ff3ede8df9558f4bec0c7962d54c43374f857e1da7e2639ddf82a9f1 in / 
# Sat, 28 Dec 2019 04:23:24 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 06:05:00 GMT
ENV MONO_VERSION=5.20.1.34
# Sat, 28 Dec 2019 06:05:42 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 06:06:42 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 28 Dec 2019 06:21:25 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:af52e7ef6e83efadeae17be91daa6ecf61b7dfb39709c29be9b24876e60c0e36`  
		Last Modified: Sat, 28 Dec 2019 04:33:19 GMT  
		Size: 22.8 MB (22800791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:657bad46700417171f7961a2ff50ecc946522119a9a065f23416906ee79d822d`  
		Last Modified: Sat, 28 Dec 2019 06:22:56 GMT  
		Size: 244.5 KB (244499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13c9779877dadfcd9c157fa02d2fbd6becf203c18e9c2727702df72179644d61`  
		Last Modified: Sat, 28 Dec 2019 06:23:14 GMT  
		Size: 24.6 MB (24638971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f31ee19914bb9f2e2b65604baa6905997d5f54e1d4012f6ed60ed63ad1b3c735`  
		Last Modified: Sat, 28 Dec 2019 06:25:31 GMT  
		Size: 125.6 MB (125620097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:5.20.1`

```console
$ docker pull mono@sha256:31176b864859ad670d8d30fd14edf662f8b32012cc41eafb9ea2a475542a1077
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:5.20.1` - linux; amd64

```console
$ docker pull mono@sha256:5c3479e37ebaba3938b41d85e43aa685b34b38c7d39f65838ccc250a77a1bdfe
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.3 MB (218283926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:843d1b62c0468f21ddbfb2ead8f14088f88b3483c3d7c5bbc29fcb42f3a8e8f5`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:47 GMT
ADD file:90a2c81769a336bed3f731f44a385f2a65b0916f517a0b77c06c224579bf9a9a in / 
# Sat, 28 Dec 2019 04:23:47 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 13:16:12 GMT
ENV MONO_VERSION=5.20.1.34
# Sat, 28 Dec 2019 13:16:24 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 13:17:03 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 28 Dec 2019 13:47:56 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:804555ee037604c40de144f9f8da0d826d38db82f15d74cded32790fe279a8f6`  
		Last Modified: Sat, 28 Dec 2019 04:28:38 GMT  
		Size: 22.5 MB (22524609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8529aa2b8c8794ada5de4f9745d3c774968df5014c707878957d1a32ac17603`  
		Last Modified: Sat, 28 Dec 2019 13:48:56 GMT  
		Size: 244.5 KB (244484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:972ee02007ec21f650fb90f3cac4c917ac5b5a84240a1092ff9be02b256bad72`  
		Last Modified: Sat, 28 Dec 2019 13:49:08 GMT  
		Size: 55.5 MB (55521389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:239a7387a2c6ed35e9e5467be5fcd6f83491d432b82e02ec511057d4c8575205`  
		Last Modified: Sat, 28 Dec 2019 13:50:58 GMT  
		Size: 140.0 MB (139993444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20.1` - linux; arm variant v5

```console
$ docker pull mono@sha256:921141ae8dd056ee2c6ab66dde3ee626f76ecebd3941aaef44a81385fa7eb3e6
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.0 MB (170952313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3270863ca29345901057a594ed47d2cb0e53b9b46570af2b4297f3a0e092cfa3`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:53:16 GMT
ADD file:7d6af454b55cb354e31c096e935358dd5914688ded04ebc76243a4ff598c4495 in / 
# Sat, 28 Dec 2019 04:53:18 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 07:31:47 GMT
ENV MONO_VERSION=5.20.1.34
# Sat, 28 Dec 2019 07:32:25 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 07:33:38 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 28 Dec 2019 07:43:54 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:af28f499fd964f4506ea46c2ac342bc52328a8c30cd633661b69f383a5144e9b`  
		Last Modified: Sat, 28 Dec 2019 05:00:23 GMT  
		Size: 21.2 MB (21202822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e30f4dec85338cf63b2a0a4635e2307d966fbfa5356fe9e83d6a9bcf294768c4`  
		Last Modified: Sat, 28 Dec 2019 07:44:59 GMT  
		Size: 244.6 KB (244563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d859f970551d160b36092ef79b226a92798c6c82b5610774fb345988f6ab6cb`  
		Last Modified: Sat, 28 Dec 2019 07:45:08 GMT  
		Size: 24.3 MB (24265462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efb69e22f6d5bc15e3d4811d51cca77b50460d4f38ad4131151a2df9b8fee768`  
		Last Modified: Sat, 28 Dec 2019 07:48:01 GMT  
		Size: 125.2 MB (125239466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20.1` - linux; arm variant v7

```console
$ docker pull mono@sha256:ea5d643ecc5f26c0f9f1edeb49fee6ea5323762e8727d392a1f813c4b8862460
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.0 MB (167004578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:631abf1b9406641e5331da51a0d793dd163877e353aece2468f77d0b962d5775`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 05:03:51 GMT
ADD file:2002ba672e32ae75369830ed6a4734ce62e0118e42390b4d657f0985d6b7fd6a in / 
# Sat, 28 Dec 2019 05:03:53 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 07:39:44 GMT
ENV MONO_VERSION=5.20.1.34
# Sat, 28 Dec 2019 07:40:06 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 07:40:54 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 28 Dec 2019 07:50:10 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:77cf262539006c8df77496f500f74a8c1edd158062440fd94d43d5b1292cefee`  
		Last Modified: Sat, 28 Dec 2019 05:11:13 GMT  
		Size: 19.3 MB (19311587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5d99eb936b9cc5835bf59846bd4e0ae6c236cda6f4adce2cb3d14125cb51956`  
		Last Modified: Sat, 28 Dec 2019 07:51:22 GMT  
		Size: 244.6 KB (244557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08fd6bf39cd6ba01aa22f88d8bed99d3c486440b3a5a1d22c82716aa505d7702`  
		Last Modified: Sat, 28 Dec 2019 07:51:30 GMT  
		Size: 23.6 MB (23561478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42a7e7be5a6639501eb7d74f9ca29ade62656f3ca932b2c23aaca5ff7ea944c5`  
		Last Modified: Sat, 28 Dec 2019 07:54:12 GMT  
		Size: 123.9 MB (123886956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20.1` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:63f81fec16f4d06039611927c73b16343f5b754011fa30d6eb203a8cbca341f6
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.8 MB (187816201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a39a2a666a7d75dfb72de8ea33faba47d1dfe373d964481dac471c5a8048e36`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:43:36 GMT
ADD file:ba40f5080cbd89c576c350bfe5acfe16f2ec59636fdb082efc3a8cef66ae7cb7 in / 
# Sat, 28 Dec 2019 04:43:39 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 08:42:12 GMT
ENV MONO_VERSION=5.20.1.34
# Sat, 28 Dec 2019 08:42:34 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 08:43:17 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 28 Dec 2019 08:51:26 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:588374d57fdb5120d024340eef3d8927af23a5b806d41b4f049ee430a153c0b4`  
		Last Modified: Sat, 28 Dec 2019 04:49:14 GMT  
		Size: 20.4 MB (20385801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:643f8d37cb48de8371d76dd11de4426d0de6e6b6f437e904e981c69341183784`  
		Last Modified: Sat, 28 Dec 2019 08:52:37 GMT  
		Size: 244.4 KB (244409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4eb44ac018125d88f4c42299e8ddfc11bf3983fda5ec1626f7e7dff77c32323`  
		Last Modified: Sat, 28 Dec 2019 08:52:47 GMT  
		Size: 28.2 MB (28156055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:390946e3d8f4fc0557faba9b870bac3bab643073f29e0b9d32e7035b3b634083`  
		Last Modified: Sat, 28 Dec 2019 08:55:20 GMT  
		Size: 139.0 MB (139029936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20.1` - linux; 386

```console
$ docker pull mono@sha256:f7dc31da4a9c0214be8de4be179c3447a71b7b3de432db0a73f592aa388349e8
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.8 MB (227783487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfbff081eeb3cc7d2fbd105c967757897aedc5e0aa95508184be517694b48419`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:42:05 GMT
ADD file:d43798bcf0e72b342c261b8585dde072d9363d19fab4b8d9f08f15db189f287b in / 
# Sat, 28 Dec 2019 04:42:05 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 08:55:21 GMT
ENV MONO_VERSION=5.20.1.34
# Sat, 28 Dec 2019 08:55:34 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 08:56:06 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 28 Dec 2019 09:03:30 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:2cb401c016d2f9802d5ef9cf6c6dc07251e9f87757a0de0a8df318fb7f00385c`  
		Last Modified: Sat, 28 Dec 2019 04:47:36 GMT  
		Size: 23.2 MB (23152142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b34b6f7471907c646ec285955dc4cf7094149b0ad93ea3e95125c4ef5f5d1171`  
		Last Modified: Sat, 28 Dec 2019 09:04:39 GMT  
		Size: 244.5 KB (244474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e1c87cf35f42f1f93ef3f7676dee0b1b3f1ca6657c6afa49443d888dbc3360d`  
		Last Modified: Sat, 28 Dec 2019 09:04:53 GMT  
		Size: 58.6 MB (58551781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:724b594c451feb85210631e54662992230c04f5e689387accacb9bf2825c06ed`  
		Last Modified: Sat, 28 Dec 2019 09:07:08 GMT  
		Size: 145.8 MB (145835090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20.1` - linux; ppc64le

```console
$ docker pull mono@sha256:b414ce326f06449a5a441ad050f57286bf41f79b0e0130a25928f9f9617f3e8e
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.3 MB (173304358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee71b36f2a14a9487be1b834ccb9a4c1682b90900f74f6a88ba2a4c937fa4272`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:21 GMT
ADD file:a1ee5955ff3ede8df9558f4bec0c7962d54c43374f857e1da7e2639ddf82a9f1 in / 
# Sat, 28 Dec 2019 04:23:24 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 06:05:00 GMT
ENV MONO_VERSION=5.20.1.34
# Sat, 28 Dec 2019 06:05:42 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 06:06:42 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 28 Dec 2019 06:21:25 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:af52e7ef6e83efadeae17be91daa6ecf61b7dfb39709c29be9b24876e60c0e36`  
		Last Modified: Sat, 28 Dec 2019 04:33:19 GMT  
		Size: 22.8 MB (22800791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:657bad46700417171f7961a2ff50ecc946522119a9a065f23416906ee79d822d`  
		Last Modified: Sat, 28 Dec 2019 06:22:56 GMT  
		Size: 244.5 KB (244499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13c9779877dadfcd9c157fa02d2fbd6becf203c18e9c2727702df72179644d61`  
		Last Modified: Sat, 28 Dec 2019 06:23:14 GMT  
		Size: 24.6 MB (24638971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f31ee19914bb9f2e2b65604baa6905997d5f54e1d4012f6ed60ed63ad1b3c735`  
		Last Modified: Sat, 28 Dec 2019 06:25:31 GMT  
		Size: 125.6 MB (125620097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:5.20.1.34`

```console
$ docker pull mono@sha256:31176b864859ad670d8d30fd14edf662f8b32012cc41eafb9ea2a475542a1077
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:5.20.1.34` - linux; amd64

```console
$ docker pull mono@sha256:5c3479e37ebaba3938b41d85e43aa685b34b38c7d39f65838ccc250a77a1bdfe
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.3 MB (218283926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:843d1b62c0468f21ddbfb2ead8f14088f88b3483c3d7c5bbc29fcb42f3a8e8f5`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:47 GMT
ADD file:90a2c81769a336bed3f731f44a385f2a65b0916f517a0b77c06c224579bf9a9a in / 
# Sat, 28 Dec 2019 04:23:47 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 13:16:12 GMT
ENV MONO_VERSION=5.20.1.34
# Sat, 28 Dec 2019 13:16:24 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 13:17:03 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 28 Dec 2019 13:47:56 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:804555ee037604c40de144f9f8da0d826d38db82f15d74cded32790fe279a8f6`  
		Last Modified: Sat, 28 Dec 2019 04:28:38 GMT  
		Size: 22.5 MB (22524609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8529aa2b8c8794ada5de4f9745d3c774968df5014c707878957d1a32ac17603`  
		Last Modified: Sat, 28 Dec 2019 13:48:56 GMT  
		Size: 244.5 KB (244484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:972ee02007ec21f650fb90f3cac4c917ac5b5a84240a1092ff9be02b256bad72`  
		Last Modified: Sat, 28 Dec 2019 13:49:08 GMT  
		Size: 55.5 MB (55521389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:239a7387a2c6ed35e9e5467be5fcd6f83491d432b82e02ec511057d4c8575205`  
		Last Modified: Sat, 28 Dec 2019 13:50:58 GMT  
		Size: 140.0 MB (139993444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20.1.34` - linux; arm variant v5

```console
$ docker pull mono@sha256:921141ae8dd056ee2c6ab66dde3ee626f76ecebd3941aaef44a81385fa7eb3e6
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.0 MB (170952313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3270863ca29345901057a594ed47d2cb0e53b9b46570af2b4297f3a0e092cfa3`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:53:16 GMT
ADD file:7d6af454b55cb354e31c096e935358dd5914688ded04ebc76243a4ff598c4495 in / 
# Sat, 28 Dec 2019 04:53:18 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 07:31:47 GMT
ENV MONO_VERSION=5.20.1.34
# Sat, 28 Dec 2019 07:32:25 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 07:33:38 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 28 Dec 2019 07:43:54 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:af28f499fd964f4506ea46c2ac342bc52328a8c30cd633661b69f383a5144e9b`  
		Last Modified: Sat, 28 Dec 2019 05:00:23 GMT  
		Size: 21.2 MB (21202822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e30f4dec85338cf63b2a0a4635e2307d966fbfa5356fe9e83d6a9bcf294768c4`  
		Last Modified: Sat, 28 Dec 2019 07:44:59 GMT  
		Size: 244.6 KB (244563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d859f970551d160b36092ef79b226a92798c6c82b5610774fb345988f6ab6cb`  
		Last Modified: Sat, 28 Dec 2019 07:45:08 GMT  
		Size: 24.3 MB (24265462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efb69e22f6d5bc15e3d4811d51cca77b50460d4f38ad4131151a2df9b8fee768`  
		Last Modified: Sat, 28 Dec 2019 07:48:01 GMT  
		Size: 125.2 MB (125239466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20.1.34` - linux; arm variant v7

```console
$ docker pull mono@sha256:ea5d643ecc5f26c0f9f1edeb49fee6ea5323762e8727d392a1f813c4b8862460
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.0 MB (167004578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:631abf1b9406641e5331da51a0d793dd163877e353aece2468f77d0b962d5775`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 05:03:51 GMT
ADD file:2002ba672e32ae75369830ed6a4734ce62e0118e42390b4d657f0985d6b7fd6a in / 
# Sat, 28 Dec 2019 05:03:53 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 07:39:44 GMT
ENV MONO_VERSION=5.20.1.34
# Sat, 28 Dec 2019 07:40:06 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 07:40:54 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 28 Dec 2019 07:50:10 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:77cf262539006c8df77496f500f74a8c1edd158062440fd94d43d5b1292cefee`  
		Last Modified: Sat, 28 Dec 2019 05:11:13 GMT  
		Size: 19.3 MB (19311587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5d99eb936b9cc5835bf59846bd4e0ae6c236cda6f4adce2cb3d14125cb51956`  
		Last Modified: Sat, 28 Dec 2019 07:51:22 GMT  
		Size: 244.6 KB (244557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08fd6bf39cd6ba01aa22f88d8bed99d3c486440b3a5a1d22c82716aa505d7702`  
		Last Modified: Sat, 28 Dec 2019 07:51:30 GMT  
		Size: 23.6 MB (23561478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42a7e7be5a6639501eb7d74f9ca29ade62656f3ca932b2c23aaca5ff7ea944c5`  
		Last Modified: Sat, 28 Dec 2019 07:54:12 GMT  
		Size: 123.9 MB (123886956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20.1.34` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:63f81fec16f4d06039611927c73b16343f5b754011fa30d6eb203a8cbca341f6
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.8 MB (187816201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a39a2a666a7d75dfb72de8ea33faba47d1dfe373d964481dac471c5a8048e36`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:43:36 GMT
ADD file:ba40f5080cbd89c576c350bfe5acfe16f2ec59636fdb082efc3a8cef66ae7cb7 in / 
# Sat, 28 Dec 2019 04:43:39 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 08:42:12 GMT
ENV MONO_VERSION=5.20.1.34
# Sat, 28 Dec 2019 08:42:34 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 08:43:17 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 28 Dec 2019 08:51:26 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:588374d57fdb5120d024340eef3d8927af23a5b806d41b4f049ee430a153c0b4`  
		Last Modified: Sat, 28 Dec 2019 04:49:14 GMT  
		Size: 20.4 MB (20385801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:643f8d37cb48de8371d76dd11de4426d0de6e6b6f437e904e981c69341183784`  
		Last Modified: Sat, 28 Dec 2019 08:52:37 GMT  
		Size: 244.4 KB (244409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4eb44ac018125d88f4c42299e8ddfc11bf3983fda5ec1626f7e7dff77c32323`  
		Last Modified: Sat, 28 Dec 2019 08:52:47 GMT  
		Size: 28.2 MB (28156055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:390946e3d8f4fc0557faba9b870bac3bab643073f29e0b9d32e7035b3b634083`  
		Last Modified: Sat, 28 Dec 2019 08:55:20 GMT  
		Size: 139.0 MB (139029936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20.1.34` - linux; 386

```console
$ docker pull mono@sha256:f7dc31da4a9c0214be8de4be179c3447a71b7b3de432db0a73f592aa388349e8
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.8 MB (227783487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfbff081eeb3cc7d2fbd105c967757897aedc5e0aa95508184be517694b48419`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:42:05 GMT
ADD file:d43798bcf0e72b342c261b8585dde072d9363d19fab4b8d9f08f15db189f287b in / 
# Sat, 28 Dec 2019 04:42:05 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 08:55:21 GMT
ENV MONO_VERSION=5.20.1.34
# Sat, 28 Dec 2019 08:55:34 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 08:56:06 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 28 Dec 2019 09:03:30 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:2cb401c016d2f9802d5ef9cf6c6dc07251e9f87757a0de0a8df318fb7f00385c`  
		Last Modified: Sat, 28 Dec 2019 04:47:36 GMT  
		Size: 23.2 MB (23152142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b34b6f7471907c646ec285955dc4cf7094149b0ad93ea3e95125c4ef5f5d1171`  
		Last Modified: Sat, 28 Dec 2019 09:04:39 GMT  
		Size: 244.5 KB (244474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e1c87cf35f42f1f93ef3f7676dee0b1b3f1ca6657c6afa49443d888dbc3360d`  
		Last Modified: Sat, 28 Dec 2019 09:04:53 GMT  
		Size: 58.6 MB (58551781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:724b594c451feb85210631e54662992230c04f5e689387accacb9bf2825c06ed`  
		Last Modified: Sat, 28 Dec 2019 09:07:08 GMT  
		Size: 145.8 MB (145835090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20.1.34` - linux; ppc64le

```console
$ docker pull mono@sha256:b414ce326f06449a5a441ad050f57286bf41f79b0e0130a25928f9f9617f3e8e
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.3 MB (173304358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee71b36f2a14a9487be1b834ccb9a4c1682b90900f74f6a88ba2a4c937fa4272`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:21 GMT
ADD file:a1ee5955ff3ede8df9558f4bec0c7962d54c43374f857e1da7e2639ddf82a9f1 in / 
# Sat, 28 Dec 2019 04:23:24 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 06:05:00 GMT
ENV MONO_VERSION=5.20.1.34
# Sat, 28 Dec 2019 06:05:42 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 06:06:42 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 28 Dec 2019 06:21:25 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:af52e7ef6e83efadeae17be91daa6ecf61b7dfb39709c29be9b24876e60c0e36`  
		Last Modified: Sat, 28 Dec 2019 04:33:19 GMT  
		Size: 22.8 MB (22800791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:657bad46700417171f7961a2ff50ecc946522119a9a065f23416906ee79d822d`  
		Last Modified: Sat, 28 Dec 2019 06:22:56 GMT  
		Size: 244.5 KB (244499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13c9779877dadfcd9c157fa02d2fbd6becf203c18e9c2727702df72179644d61`  
		Last Modified: Sat, 28 Dec 2019 06:23:14 GMT  
		Size: 24.6 MB (24638971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f31ee19914bb9f2e2b65604baa6905997d5f54e1d4012f6ed60ed63ad1b3c735`  
		Last Modified: Sat, 28 Dec 2019 06:25:31 GMT  
		Size: 125.6 MB (125620097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:5.20.1.34-slim`

```console
$ docker pull mono@sha256:f2787dc83ec8318b9ee66150cb75263c95d0cab57d0988be6a27253b0f3f008c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:5.20.1.34-slim` - linux; amd64

```console
$ docker pull mono@sha256:cdacbba352e15efb4a84f8b75ec4e96c43ae5dcd8d2f2a76b5fb53100b32214e
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.3 MB (78290482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee1fc6fc66317cf629fd0743dff6784c1fad2e8e88cd9a07be738bc8a6ccfef6`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:47 GMT
ADD file:90a2c81769a336bed3f731f44a385f2a65b0916f517a0b77c06c224579bf9a9a in / 
# Sat, 28 Dec 2019 04:23:47 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 13:16:12 GMT
ENV MONO_VERSION=5.20.1.34
# Sat, 28 Dec 2019 13:16:24 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 13:17:03 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:804555ee037604c40de144f9f8da0d826d38db82f15d74cded32790fe279a8f6`  
		Last Modified: Sat, 28 Dec 2019 04:28:38 GMT  
		Size: 22.5 MB (22524609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8529aa2b8c8794ada5de4f9745d3c774968df5014c707878957d1a32ac17603`  
		Last Modified: Sat, 28 Dec 2019 13:48:56 GMT  
		Size: 244.5 KB (244484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:972ee02007ec21f650fb90f3cac4c917ac5b5a84240a1092ff9be02b256bad72`  
		Last Modified: Sat, 28 Dec 2019 13:49:08 GMT  
		Size: 55.5 MB (55521389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20.1.34-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:84ba79b228b895ae28fc2cc6e7b153952f08df639473bf6a6ad88b31b82f0a01
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45712847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58072baece060776cb79a8f6bdbdc0f3a9c5a85bda29c3ac356f0068443d3d8e`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:53:16 GMT
ADD file:7d6af454b55cb354e31c096e935358dd5914688ded04ebc76243a4ff598c4495 in / 
# Sat, 28 Dec 2019 04:53:18 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 07:31:47 GMT
ENV MONO_VERSION=5.20.1.34
# Sat, 28 Dec 2019 07:32:25 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 07:33:38 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:af28f499fd964f4506ea46c2ac342bc52328a8c30cd633661b69f383a5144e9b`  
		Last Modified: Sat, 28 Dec 2019 05:00:23 GMT  
		Size: 21.2 MB (21202822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e30f4dec85338cf63b2a0a4635e2307d966fbfa5356fe9e83d6a9bcf294768c4`  
		Last Modified: Sat, 28 Dec 2019 07:44:59 GMT  
		Size: 244.6 KB (244563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d859f970551d160b36092ef79b226a92798c6c82b5610774fb345988f6ab6cb`  
		Last Modified: Sat, 28 Dec 2019 07:45:08 GMT  
		Size: 24.3 MB (24265462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20.1.34-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:d804f4bb2c5ff9bf8088ea66eb9543f3addacd400ed79782099001d18d396a31
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.1 MB (43117622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee7b70d3c2d1b9f9631a97c637f72660d3b7ae52250cb5c5dd618a88cd22aef6`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 05:03:51 GMT
ADD file:2002ba672e32ae75369830ed6a4734ce62e0118e42390b4d657f0985d6b7fd6a in / 
# Sat, 28 Dec 2019 05:03:53 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 07:39:44 GMT
ENV MONO_VERSION=5.20.1.34
# Sat, 28 Dec 2019 07:40:06 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 07:40:54 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:77cf262539006c8df77496f500f74a8c1edd158062440fd94d43d5b1292cefee`  
		Last Modified: Sat, 28 Dec 2019 05:11:13 GMT  
		Size: 19.3 MB (19311587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5d99eb936b9cc5835bf59846bd4e0ae6c236cda6f4adce2cb3d14125cb51956`  
		Last Modified: Sat, 28 Dec 2019 07:51:22 GMT  
		Size: 244.6 KB (244557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08fd6bf39cd6ba01aa22f88d8bed99d3c486440b3a5a1d22c82716aa505d7702`  
		Last Modified: Sat, 28 Dec 2019 07:51:30 GMT  
		Size: 23.6 MB (23561478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20.1.34-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:4e4b4dd925e65ee593e173c5daa58a381460320e629b91d58d44d260c4c409ea
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48786265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b94cd3a0f65a95b6690073b4784c51f4bd59f3b84718654f6fc76f833c60b901`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:43:36 GMT
ADD file:ba40f5080cbd89c576c350bfe5acfe16f2ec59636fdb082efc3a8cef66ae7cb7 in / 
# Sat, 28 Dec 2019 04:43:39 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 08:42:12 GMT
ENV MONO_VERSION=5.20.1.34
# Sat, 28 Dec 2019 08:42:34 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 08:43:17 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:588374d57fdb5120d024340eef3d8927af23a5b806d41b4f049ee430a153c0b4`  
		Last Modified: Sat, 28 Dec 2019 04:49:14 GMT  
		Size: 20.4 MB (20385801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:643f8d37cb48de8371d76dd11de4426d0de6e6b6f437e904e981c69341183784`  
		Last Modified: Sat, 28 Dec 2019 08:52:37 GMT  
		Size: 244.4 KB (244409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4eb44ac018125d88f4c42299e8ddfc11bf3983fda5ec1626f7e7dff77c32323`  
		Last Modified: Sat, 28 Dec 2019 08:52:47 GMT  
		Size: 28.2 MB (28156055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20.1.34-slim` - linux; 386

```console
$ docker pull mono@sha256:96288130247b476a2e36fe48056efd7645d8ff9772e13178024ae4529801ea1f
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.9 MB (81948397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60bf00a5e27af46784e6f08920565478037a23309428ca7975d58b5a5814f8ba`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:42:05 GMT
ADD file:d43798bcf0e72b342c261b8585dde072d9363d19fab4b8d9f08f15db189f287b in / 
# Sat, 28 Dec 2019 04:42:05 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 08:55:21 GMT
ENV MONO_VERSION=5.20.1.34
# Sat, 28 Dec 2019 08:55:34 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 08:56:06 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:2cb401c016d2f9802d5ef9cf6c6dc07251e9f87757a0de0a8df318fb7f00385c`  
		Last Modified: Sat, 28 Dec 2019 04:47:36 GMT  
		Size: 23.2 MB (23152142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b34b6f7471907c646ec285955dc4cf7094149b0ad93ea3e95125c4ef5f5d1171`  
		Last Modified: Sat, 28 Dec 2019 09:04:39 GMT  
		Size: 244.5 KB (244474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e1c87cf35f42f1f93ef3f7676dee0b1b3f1ca6657c6afa49443d888dbc3360d`  
		Last Modified: Sat, 28 Dec 2019 09:04:53 GMT  
		Size: 58.6 MB (58551781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20.1.34-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:aed3a9827f0d572f25d9f40d95b1f6932009f3fa43c45edd12c7bd4a1a7e118d
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47684261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:558f9d54d3463ad40c540b19d52f4576c3edd30ec719da37da034a8bcdc494ca`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:21 GMT
ADD file:a1ee5955ff3ede8df9558f4bec0c7962d54c43374f857e1da7e2639ddf82a9f1 in / 
# Sat, 28 Dec 2019 04:23:24 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 06:05:00 GMT
ENV MONO_VERSION=5.20.1.34
# Sat, 28 Dec 2019 06:05:42 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 06:06:42 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:af52e7ef6e83efadeae17be91daa6ecf61b7dfb39709c29be9b24876e60c0e36`  
		Last Modified: Sat, 28 Dec 2019 04:33:19 GMT  
		Size: 22.8 MB (22800791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:657bad46700417171f7961a2ff50ecc946522119a9a065f23416906ee79d822d`  
		Last Modified: Sat, 28 Dec 2019 06:22:56 GMT  
		Size: 244.5 KB (244499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13c9779877dadfcd9c157fa02d2fbd6becf203c18e9c2727702df72179644d61`  
		Last Modified: Sat, 28 Dec 2019 06:23:14 GMT  
		Size: 24.6 MB (24638971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:5.20.1-slim`

```console
$ docker pull mono@sha256:f2787dc83ec8318b9ee66150cb75263c95d0cab57d0988be6a27253b0f3f008c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:5.20.1-slim` - linux; amd64

```console
$ docker pull mono@sha256:cdacbba352e15efb4a84f8b75ec4e96c43ae5dcd8d2f2a76b5fb53100b32214e
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.3 MB (78290482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee1fc6fc66317cf629fd0743dff6784c1fad2e8e88cd9a07be738bc8a6ccfef6`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:47 GMT
ADD file:90a2c81769a336bed3f731f44a385f2a65b0916f517a0b77c06c224579bf9a9a in / 
# Sat, 28 Dec 2019 04:23:47 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 13:16:12 GMT
ENV MONO_VERSION=5.20.1.34
# Sat, 28 Dec 2019 13:16:24 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 13:17:03 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:804555ee037604c40de144f9f8da0d826d38db82f15d74cded32790fe279a8f6`  
		Last Modified: Sat, 28 Dec 2019 04:28:38 GMT  
		Size: 22.5 MB (22524609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8529aa2b8c8794ada5de4f9745d3c774968df5014c707878957d1a32ac17603`  
		Last Modified: Sat, 28 Dec 2019 13:48:56 GMT  
		Size: 244.5 KB (244484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:972ee02007ec21f650fb90f3cac4c917ac5b5a84240a1092ff9be02b256bad72`  
		Last Modified: Sat, 28 Dec 2019 13:49:08 GMT  
		Size: 55.5 MB (55521389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20.1-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:84ba79b228b895ae28fc2cc6e7b153952f08df639473bf6a6ad88b31b82f0a01
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45712847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58072baece060776cb79a8f6bdbdc0f3a9c5a85bda29c3ac356f0068443d3d8e`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:53:16 GMT
ADD file:7d6af454b55cb354e31c096e935358dd5914688ded04ebc76243a4ff598c4495 in / 
# Sat, 28 Dec 2019 04:53:18 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 07:31:47 GMT
ENV MONO_VERSION=5.20.1.34
# Sat, 28 Dec 2019 07:32:25 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 07:33:38 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:af28f499fd964f4506ea46c2ac342bc52328a8c30cd633661b69f383a5144e9b`  
		Last Modified: Sat, 28 Dec 2019 05:00:23 GMT  
		Size: 21.2 MB (21202822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e30f4dec85338cf63b2a0a4635e2307d966fbfa5356fe9e83d6a9bcf294768c4`  
		Last Modified: Sat, 28 Dec 2019 07:44:59 GMT  
		Size: 244.6 KB (244563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d859f970551d160b36092ef79b226a92798c6c82b5610774fb345988f6ab6cb`  
		Last Modified: Sat, 28 Dec 2019 07:45:08 GMT  
		Size: 24.3 MB (24265462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20.1-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:d804f4bb2c5ff9bf8088ea66eb9543f3addacd400ed79782099001d18d396a31
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.1 MB (43117622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee7b70d3c2d1b9f9631a97c637f72660d3b7ae52250cb5c5dd618a88cd22aef6`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 05:03:51 GMT
ADD file:2002ba672e32ae75369830ed6a4734ce62e0118e42390b4d657f0985d6b7fd6a in / 
# Sat, 28 Dec 2019 05:03:53 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 07:39:44 GMT
ENV MONO_VERSION=5.20.1.34
# Sat, 28 Dec 2019 07:40:06 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 07:40:54 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:77cf262539006c8df77496f500f74a8c1edd158062440fd94d43d5b1292cefee`  
		Last Modified: Sat, 28 Dec 2019 05:11:13 GMT  
		Size: 19.3 MB (19311587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5d99eb936b9cc5835bf59846bd4e0ae6c236cda6f4adce2cb3d14125cb51956`  
		Last Modified: Sat, 28 Dec 2019 07:51:22 GMT  
		Size: 244.6 KB (244557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08fd6bf39cd6ba01aa22f88d8bed99d3c486440b3a5a1d22c82716aa505d7702`  
		Last Modified: Sat, 28 Dec 2019 07:51:30 GMT  
		Size: 23.6 MB (23561478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20.1-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:4e4b4dd925e65ee593e173c5daa58a381460320e629b91d58d44d260c4c409ea
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48786265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b94cd3a0f65a95b6690073b4784c51f4bd59f3b84718654f6fc76f833c60b901`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:43:36 GMT
ADD file:ba40f5080cbd89c576c350bfe5acfe16f2ec59636fdb082efc3a8cef66ae7cb7 in / 
# Sat, 28 Dec 2019 04:43:39 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 08:42:12 GMT
ENV MONO_VERSION=5.20.1.34
# Sat, 28 Dec 2019 08:42:34 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 08:43:17 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:588374d57fdb5120d024340eef3d8927af23a5b806d41b4f049ee430a153c0b4`  
		Last Modified: Sat, 28 Dec 2019 04:49:14 GMT  
		Size: 20.4 MB (20385801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:643f8d37cb48de8371d76dd11de4426d0de6e6b6f437e904e981c69341183784`  
		Last Modified: Sat, 28 Dec 2019 08:52:37 GMT  
		Size: 244.4 KB (244409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4eb44ac018125d88f4c42299e8ddfc11bf3983fda5ec1626f7e7dff77c32323`  
		Last Modified: Sat, 28 Dec 2019 08:52:47 GMT  
		Size: 28.2 MB (28156055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20.1-slim` - linux; 386

```console
$ docker pull mono@sha256:96288130247b476a2e36fe48056efd7645d8ff9772e13178024ae4529801ea1f
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.9 MB (81948397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60bf00a5e27af46784e6f08920565478037a23309428ca7975d58b5a5814f8ba`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:42:05 GMT
ADD file:d43798bcf0e72b342c261b8585dde072d9363d19fab4b8d9f08f15db189f287b in / 
# Sat, 28 Dec 2019 04:42:05 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 08:55:21 GMT
ENV MONO_VERSION=5.20.1.34
# Sat, 28 Dec 2019 08:55:34 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 08:56:06 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:2cb401c016d2f9802d5ef9cf6c6dc07251e9f87757a0de0a8df318fb7f00385c`  
		Last Modified: Sat, 28 Dec 2019 04:47:36 GMT  
		Size: 23.2 MB (23152142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b34b6f7471907c646ec285955dc4cf7094149b0ad93ea3e95125c4ef5f5d1171`  
		Last Modified: Sat, 28 Dec 2019 09:04:39 GMT  
		Size: 244.5 KB (244474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e1c87cf35f42f1f93ef3f7676dee0b1b3f1ca6657c6afa49443d888dbc3360d`  
		Last Modified: Sat, 28 Dec 2019 09:04:53 GMT  
		Size: 58.6 MB (58551781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20.1-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:aed3a9827f0d572f25d9f40d95b1f6932009f3fa43c45edd12c7bd4a1a7e118d
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47684261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:558f9d54d3463ad40c540b19d52f4576c3edd30ec719da37da034a8bcdc494ca`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:21 GMT
ADD file:a1ee5955ff3ede8df9558f4bec0c7962d54c43374f857e1da7e2639ddf82a9f1 in / 
# Sat, 28 Dec 2019 04:23:24 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 06:05:00 GMT
ENV MONO_VERSION=5.20.1.34
# Sat, 28 Dec 2019 06:05:42 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 06:06:42 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:af52e7ef6e83efadeae17be91daa6ecf61b7dfb39709c29be9b24876e60c0e36`  
		Last Modified: Sat, 28 Dec 2019 04:33:19 GMT  
		Size: 22.8 MB (22800791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:657bad46700417171f7961a2ff50ecc946522119a9a065f23416906ee79d822d`  
		Last Modified: Sat, 28 Dec 2019 06:22:56 GMT  
		Size: 244.5 KB (244499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13c9779877dadfcd9c157fa02d2fbd6becf203c18e9c2727702df72179644d61`  
		Last Modified: Sat, 28 Dec 2019 06:23:14 GMT  
		Size: 24.6 MB (24638971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:5.20-slim`

```console
$ docker pull mono@sha256:f2787dc83ec8318b9ee66150cb75263c95d0cab57d0988be6a27253b0f3f008c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:5.20-slim` - linux; amd64

```console
$ docker pull mono@sha256:cdacbba352e15efb4a84f8b75ec4e96c43ae5dcd8d2f2a76b5fb53100b32214e
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.3 MB (78290482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee1fc6fc66317cf629fd0743dff6784c1fad2e8e88cd9a07be738bc8a6ccfef6`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:47 GMT
ADD file:90a2c81769a336bed3f731f44a385f2a65b0916f517a0b77c06c224579bf9a9a in / 
# Sat, 28 Dec 2019 04:23:47 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 13:16:12 GMT
ENV MONO_VERSION=5.20.1.34
# Sat, 28 Dec 2019 13:16:24 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 13:17:03 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:804555ee037604c40de144f9f8da0d826d38db82f15d74cded32790fe279a8f6`  
		Last Modified: Sat, 28 Dec 2019 04:28:38 GMT  
		Size: 22.5 MB (22524609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8529aa2b8c8794ada5de4f9745d3c774968df5014c707878957d1a32ac17603`  
		Last Modified: Sat, 28 Dec 2019 13:48:56 GMT  
		Size: 244.5 KB (244484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:972ee02007ec21f650fb90f3cac4c917ac5b5a84240a1092ff9be02b256bad72`  
		Last Modified: Sat, 28 Dec 2019 13:49:08 GMT  
		Size: 55.5 MB (55521389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:84ba79b228b895ae28fc2cc6e7b153952f08df639473bf6a6ad88b31b82f0a01
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45712847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58072baece060776cb79a8f6bdbdc0f3a9c5a85bda29c3ac356f0068443d3d8e`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:53:16 GMT
ADD file:7d6af454b55cb354e31c096e935358dd5914688ded04ebc76243a4ff598c4495 in / 
# Sat, 28 Dec 2019 04:53:18 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 07:31:47 GMT
ENV MONO_VERSION=5.20.1.34
# Sat, 28 Dec 2019 07:32:25 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 07:33:38 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:af28f499fd964f4506ea46c2ac342bc52328a8c30cd633661b69f383a5144e9b`  
		Last Modified: Sat, 28 Dec 2019 05:00:23 GMT  
		Size: 21.2 MB (21202822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e30f4dec85338cf63b2a0a4635e2307d966fbfa5356fe9e83d6a9bcf294768c4`  
		Last Modified: Sat, 28 Dec 2019 07:44:59 GMT  
		Size: 244.6 KB (244563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d859f970551d160b36092ef79b226a92798c6c82b5610774fb345988f6ab6cb`  
		Last Modified: Sat, 28 Dec 2019 07:45:08 GMT  
		Size: 24.3 MB (24265462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:d804f4bb2c5ff9bf8088ea66eb9543f3addacd400ed79782099001d18d396a31
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.1 MB (43117622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee7b70d3c2d1b9f9631a97c637f72660d3b7ae52250cb5c5dd618a88cd22aef6`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 05:03:51 GMT
ADD file:2002ba672e32ae75369830ed6a4734ce62e0118e42390b4d657f0985d6b7fd6a in / 
# Sat, 28 Dec 2019 05:03:53 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 07:39:44 GMT
ENV MONO_VERSION=5.20.1.34
# Sat, 28 Dec 2019 07:40:06 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 07:40:54 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:77cf262539006c8df77496f500f74a8c1edd158062440fd94d43d5b1292cefee`  
		Last Modified: Sat, 28 Dec 2019 05:11:13 GMT  
		Size: 19.3 MB (19311587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5d99eb936b9cc5835bf59846bd4e0ae6c236cda6f4adce2cb3d14125cb51956`  
		Last Modified: Sat, 28 Dec 2019 07:51:22 GMT  
		Size: 244.6 KB (244557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08fd6bf39cd6ba01aa22f88d8bed99d3c486440b3a5a1d22c82716aa505d7702`  
		Last Modified: Sat, 28 Dec 2019 07:51:30 GMT  
		Size: 23.6 MB (23561478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:4e4b4dd925e65ee593e173c5daa58a381460320e629b91d58d44d260c4c409ea
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48786265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b94cd3a0f65a95b6690073b4784c51f4bd59f3b84718654f6fc76f833c60b901`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:43:36 GMT
ADD file:ba40f5080cbd89c576c350bfe5acfe16f2ec59636fdb082efc3a8cef66ae7cb7 in / 
# Sat, 28 Dec 2019 04:43:39 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 08:42:12 GMT
ENV MONO_VERSION=5.20.1.34
# Sat, 28 Dec 2019 08:42:34 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 08:43:17 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:588374d57fdb5120d024340eef3d8927af23a5b806d41b4f049ee430a153c0b4`  
		Last Modified: Sat, 28 Dec 2019 04:49:14 GMT  
		Size: 20.4 MB (20385801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:643f8d37cb48de8371d76dd11de4426d0de6e6b6f437e904e981c69341183784`  
		Last Modified: Sat, 28 Dec 2019 08:52:37 GMT  
		Size: 244.4 KB (244409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4eb44ac018125d88f4c42299e8ddfc11bf3983fda5ec1626f7e7dff77c32323`  
		Last Modified: Sat, 28 Dec 2019 08:52:47 GMT  
		Size: 28.2 MB (28156055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20-slim` - linux; 386

```console
$ docker pull mono@sha256:96288130247b476a2e36fe48056efd7645d8ff9772e13178024ae4529801ea1f
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.9 MB (81948397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60bf00a5e27af46784e6f08920565478037a23309428ca7975d58b5a5814f8ba`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:42:05 GMT
ADD file:d43798bcf0e72b342c261b8585dde072d9363d19fab4b8d9f08f15db189f287b in / 
# Sat, 28 Dec 2019 04:42:05 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 08:55:21 GMT
ENV MONO_VERSION=5.20.1.34
# Sat, 28 Dec 2019 08:55:34 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 08:56:06 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:2cb401c016d2f9802d5ef9cf6c6dc07251e9f87757a0de0a8df318fb7f00385c`  
		Last Modified: Sat, 28 Dec 2019 04:47:36 GMT  
		Size: 23.2 MB (23152142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b34b6f7471907c646ec285955dc4cf7094149b0ad93ea3e95125c4ef5f5d1171`  
		Last Modified: Sat, 28 Dec 2019 09:04:39 GMT  
		Size: 244.5 KB (244474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e1c87cf35f42f1f93ef3f7676dee0b1b3f1ca6657c6afa49443d888dbc3360d`  
		Last Modified: Sat, 28 Dec 2019 09:04:53 GMT  
		Size: 58.6 MB (58551781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:aed3a9827f0d572f25d9f40d95b1f6932009f3fa43c45edd12c7bd4a1a7e118d
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47684261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:558f9d54d3463ad40c540b19d52f4576c3edd30ec719da37da034a8bcdc494ca`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:21 GMT
ADD file:a1ee5955ff3ede8df9558f4bec0c7962d54c43374f857e1da7e2639ddf82a9f1 in / 
# Sat, 28 Dec 2019 04:23:24 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 06:05:00 GMT
ENV MONO_VERSION=5.20.1.34
# Sat, 28 Dec 2019 06:05:42 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 06:06:42 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:af52e7ef6e83efadeae17be91daa6ecf61b7dfb39709c29be9b24876e60c0e36`  
		Last Modified: Sat, 28 Dec 2019 04:33:19 GMT  
		Size: 22.8 MB (22800791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:657bad46700417171f7961a2ff50ecc946522119a9a065f23416906ee79d822d`  
		Last Modified: Sat, 28 Dec 2019 06:22:56 GMT  
		Size: 244.5 KB (244499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13c9779877dadfcd9c157fa02d2fbd6becf203c18e9c2727702df72179644d61`  
		Last Modified: Sat, 28 Dec 2019 06:23:14 GMT  
		Size: 24.6 MB (24638971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:5-slim`

```console
$ docker pull mono@sha256:f2787dc83ec8318b9ee66150cb75263c95d0cab57d0988be6a27253b0f3f008c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:5-slim` - linux; amd64

```console
$ docker pull mono@sha256:cdacbba352e15efb4a84f8b75ec4e96c43ae5dcd8d2f2a76b5fb53100b32214e
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.3 MB (78290482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee1fc6fc66317cf629fd0743dff6784c1fad2e8e88cd9a07be738bc8a6ccfef6`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:47 GMT
ADD file:90a2c81769a336bed3f731f44a385f2a65b0916f517a0b77c06c224579bf9a9a in / 
# Sat, 28 Dec 2019 04:23:47 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 13:16:12 GMT
ENV MONO_VERSION=5.20.1.34
# Sat, 28 Dec 2019 13:16:24 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 13:17:03 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:804555ee037604c40de144f9f8da0d826d38db82f15d74cded32790fe279a8f6`  
		Last Modified: Sat, 28 Dec 2019 04:28:38 GMT  
		Size: 22.5 MB (22524609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8529aa2b8c8794ada5de4f9745d3c774968df5014c707878957d1a32ac17603`  
		Last Modified: Sat, 28 Dec 2019 13:48:56 GMT  
		Size: 244.5 KB (244484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:972ee02007ec21f650fb90f3cac4c917ac5b5a84240a1092ff9be02b256bad72`  
		Last Modified: Sat, 28 Dec 2019 13:49:08 GMT  
		Size: 55.5 MB (55521389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:84ba79b228b895ae28fc2cc6e7b153952f08df639473bf6a6ad88b31b82f0a01
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45712847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58072baece060776cb79a8f6bdbdc0f3a9c5a85bda29c3ac356f0068443d3d8e`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:53:16 GMT
ADD file:7d6af454b55cb354e31c096e935358dd5914688ded04ebc76243a4ff598c4495 in / 
# Sat, 28 Dec 2019 04:53:18 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 07:31:47 GMT
ENV MONO_VERSION=5.20.1.34
# Sat, 28 Dec 2019 07:32:25 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 07:33:38 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:af28f499fd964f4506ea46c2ac342bc52328a8c30cd633661b69f383a5144e9b`  
		Last Modified: Sat, 28 Dec 2019 05:00:23 GMT  
		Size: 21.2 MB (21202822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e30f4dec85338cf63b2a0a4635e2307d966fbfa5356fe9e83d6a9bcf294768c4`  
		Last Modified: Sat, 28 Dec 2019 07:44:59 GMT  
		Size: 244.6 KB (244563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d859f970551d160b36092ef79b226a92798c6c82b5610774fb345988f6ab6cb`  
		Last Modified: Sat, 28 Dec 2019 07:45:08 GMT  
		Size: 24.3 MB (24265462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:d804f4bb2c5ff9bf8088ea66eb9543f3addacd400ed79782099001d18d396a31
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.1 MB (43117622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee7b70d3c2d1b9f9631a97c637f72660d3b7ae52250cb5c5dd618a88cd22aef6`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 05:03:51 GMT
ADD file:2002ba672e32ae75369830ed6a4734ce62e0118e42390b4d657f0985d6b7fd6a in / 
# Sat, 28 Dec 2019 05:03:53 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 07:39:44 GMT
ENV MONO_VERSION=5.20.1.34
# Sat, 28 Dec 2019 07:40:06 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 07:40:54 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:77cf262539006c8df77496f500f74a8c1edd158062440fd94d43d5b1292cefee`  
		Last Modified: Sat, 28 Dec 2019 05:11:13 GMT  
		Size: 19.3 MB (19311587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5d99eb936b9cc5835bf59846bd4e0ae6c236cda6f4adce2cb3d14125cb51956`  
		Last Modified: Sat, 28 Dec 2019 07:51:22 GMT  
		Size: 244.6 KB (244557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08fd6bf39cd6ba01aa22f88d8bed99d3c486440b3a5a1d22c82716aa505d7702`  
		Last Modified: Sat, 28 Dec 2019 07:51:30 GMT  
		Size: 23.6 MB (23561478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:4e4b4dd925e65ee593e173c5daa58a381460320e629b91d58d44d260c4c409ea
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48786265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b94cd3a0f65a95b6690073b4784c51f4bd59f3b84718654f6fc76f833c60b901`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:43:36 GMT
ADD file:ba40f5080cbd89c576c350bfe5acfe16f2ec59636fdb082efc3a8cef66ae7cb7 in / 
# Sat, 28 Dec 2019 04:43:39 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 08:42:12 GMT
ENV MONO_VERSION=5.20.1.34
# Sat, 28 Dec 2019 08:42:34 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 08:43:17 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:588374d57fdb5120d024340eef3d8927af23a5b806d41b4f049ee430a153c0b4`  
		Last Modified: Sat, 28 Dec 2019 04:49:14 GMT  
		Size: 20.4 MB (20385801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:643f8d37cb48de8371d76dd11de4426d0de6e6b6f437e904e981c69341183784`  
		Last Modified: Sat, 28 Dec 2019 08:52:37 GMT  
		Size: 244.4 KB (244409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4eb44ac018125d88f4c42299e8ddfc11bf3983fda5ec1626f7e7dff77c32323`  
		Last Modified: Sat, 28 Dec 2019 08:52:47 GMT  
		Size: 28.2 MB (28156055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5-slim` - linux; 386

```console
$ docker pull mono@sha256:96288130247b476a2e36fe48056efd7645d8ff9772e13178024ae4529801ea1f
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.9 MB (81948397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60bf00a5e27af46784e6f08920565478037a23309428ca7975d58b5a5814f8ba`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:42:05 GMT
ADD file:d43798bcf0e72b342c261b8585dde072d9363d19fab4b8d9f08f15db189f287b in / 
# Sat, 28 Dec 2019 04:42:05 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 08:55:21 GMT
ENV MONO_VERSION=5.20.1.34
# Sat, 28 Dec 2019 08:55:34 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 08:56:06 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:2cb401c016d2f9802d5ef9cf6c6dc07251e9f87757a0de0a8df318fb7f00385c`  
		Last Modified: Sat, 28 Dec 2019 04:47:36 GMT  
		Size: 23.2 MB (23152142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b34b6f7471907c646ec285955dc4cf7094149b0ad93ea3e95125c4ef5f5d1171`  
		Last Modified: Sat, 28 Dec 2019 09:04:39 GMT  
		Size: 244.5 KB (244474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e1c87cf35f42f1f93ef3f7676dee0b1b3f1ca6657c6afa49443d888dbc3360d`  
		Last Modified: Sat, 28 Dec 2019 09:04:53 GMT  
		Size: 58.6 MB (58551781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:aed3a9827f0d572f25d9f40d95b1f6932009f3fa43c45edd12c7bd4a1a7e118d
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47684261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:558f9d54d3463ad40c540b19d52f4576c3edd30ec719da37da034a8bcdc494ca`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:21 GMT
ADD file:a1ee5955ff3ede8df9558f4bec0c7962d54c43374f857e1da7e2639ddf82a9f1 in / 
# Sat, 28 Dec 2019 04:23:24 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 06:05:00 GMT
ENV MONO_VERSION=5.20.1.34
# Sat, 28 Dec 2019 06:05:42 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 06:06:42 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:af52e7ef6e83efadeae17be91daa6ecf61b7dfb39709c29be9b24876e60c0e36`  
		Last Modified: Sat, 28 Dec 2019 04:33:19 GMT  
		Size: 22.8 MB (22800791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:657bad46700417171f7961a2ff50ecc946522119a9a065f23416906ee79d822d`  
		Last Modified: Sat, 28 Dec 2019 06:22:56 GMT  
		Size: 244.5 KB (244499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13c9779877dadfcd9c157fa02d2fbd6becf203c18e9c2727702df72179644d61`  
		Last Modified: Sat, 28 Dec 2019 06:23:14 GMT  
		Size: 24.6 MB (24638971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6`

```console
$ docker pull mono@sha256:cb8035058b1a14a610fe7a43bc3b3b77ebf97b24313c15a8f414e748f02a7dbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:6` - linux; amd64

```console
$ docker pull mono@sha256:3f3ad551a8789a79e3b59c836a659dc748626b0c18543cc9d32ecc1f3d01ee32
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233195367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13ed216b8ba57507781ef13d31102febe0415d37333dd05d96e05f92ad9e9ca3`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:47 GMT
ADD file:90a2c81769a336bed3f731f44a385f2a65b0916f517a0b77c06c224579bf9a9a in / 
# Sat, 28 Dec 2019 04:23:47 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 13:14:15 GMT
ENV MONO_VERSION=6.6.0.161
# Sat, 28 Dec 2019 13:14:25 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 13:15:04 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 28 Dec 2019 13:27:55 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:804555ee037604c40de144f9f8da0d826d38db82f15d74cded32790fe279a8f6`  
		Last Modified: Sat, 28 Dec 2019 04:28:38 GMT  
		Size: 22.5 MB (22524609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01e78f3e714bb9645ac8b6e172f033253467b1312e6dd4889da24aeee207e091`  
		Last Modified: Sat, 28 Dec 2019 13:48:14 GMT  
		Size: 244.5 KB (244485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b64c5ff00a44477231f8da775a76ef1611f6e7879ef3116862f0e13f16e5575f`  
		Last Modified: Sat, 28 Dec 2019 13:48:30 GMT  
		Size: 63.0 MB (62973929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9e6e2e990789fcd233754f316f68b3dcf7fcc8affcb267f1770e6abecd0a4df`  
		Last Modified: Sat, 28 Dec 2019 13:49:41 GMT  
		Size: 147.5 MB (147452344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6` - linux; arm variant v5

```console
$ docker pull mono@sha256:71075f43a6acd5d4900e8b4050bc87b552302d7b550e2d9da1a55aa37eb95852
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.7 MB (176653531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41594e91a86b24e549ebe9f4c951e2403e6e22200d648d599d853dbc7ebe37a5`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:53:16 GMT
ADD file:7d6af454b55cb354e31c096e935358dd5914688ded04ebc76243a4ff598c4495 in / 
# Sat, 28 Dec 2019 04:53:18 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 07:28:31 GMT
ENV MONO_VERSION=6.6.0.161
# Sat, 28 Dec 2019 07:28:56 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 07:29:51 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 28 Dec 2019 07:37:00 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:af28f499fd964f4506ea46c2ac342bc52328a8c30cd633661b69f383a5144e9b`  
		Last Modified: Sat, 28 Dec 2019 05:00:23 GMT  
		Size: 21.2 MB (21202822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f759ae685ca874cea702ae1f63627810d814a2cae6a44c704003176e0c8b37c`  
		Last Modified: Sat, 28 Dec 2019 07:44:23 GMT  
		Size: 244.6 KB (244552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:720fbe46ab0c5e8c2e3e9ed44413d9fde2ad1d45d9161dd0c6a021855acc1b78`  
		Last Modified: Sat, 28 Dec 2019 07:44:33 GMT  
		Size: 25.4 MB (25416500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:906dd0e12894eb03a4ab34eacdf91d163dfd6c09d61c9005e666875d42c1b91b`  
		Last Modified: Sat, 28 Dec 2019 07:46:06 GMT  
		Size: 129.8 MB (129789657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6` - linux; arm variant v7

```console
$ docker pull mono@sha256:7e7ebdba687fb7bac2a796eb557210fe8f5fa55c86cfa342bd56d213a27dcaf3
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.7 MB (172655347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c77176fb08c03220255179938d178739f8882569f72ecaae83ba7b5fc620aef`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 05:03:51 GMT
ADD file:2002ba672e32ae75369830ed6a4734ce62e0118e42390b4d657f0985d6b7fd6a in / 
# Sat, 28 Dec 2019 05:03:53 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 07:37:00 GMT
ENV MONO_VERSION=6.6.0.161
# Sat, 28 Dec 2019 07:37:19 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 07:38:02 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 28 Dec 2019 07:44:03 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:77cf262539006c8df77496f500f74a8c1edd158062440fd94d43d5b1292cefee`  
		Last Modified: Sat, 28 Dec 2019 05:11:13 GMT  
		Size: 19.3 MB (19311587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63ea3a0398ee0834c6b8b5a98490a2451261135d85bbd06845c7077aff2a4667`  
		Last Modified: Sat, 28 Dec 2019 07:50:49 GMT  
		Size: 244.5 KB (244525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f543438b2494429fd7ef0a5cbe2145241dfa4aa2f1008038a251526056612dc`  
		Last Modified: Sat, 28 Dec 2019 07:50:58 GMT  
		Size: 24.6 MB (24648229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:184b3a33ac95fb2ba207e6fc82f4e7fac1dc71bad49531f182c2a7046b54bd39`  
		Last Modified: Sat, 28 Dec 2019 07:52:21 GMT  
		Size: 128.5 MB (128451006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:8aed237906aca013f801430a60e500a1ad6f159c804e14bf4869e9abfcabb89d
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.5 MB (194537478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45a4c03521b1b035e910a91ec512dae28e62411186750460178c6daa0e9809af`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:43:36 GMT
ADD file:ba40f5080cbd89c576c350bfe5acfe16f2ec59636fdb082efc3a8cef66ae7cb7 in / 
# Sat, 28 Dec 2019 04:43:39 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 08:39:40 GMT
ENV MONO_VERSION=6.6.0.161
# Sat, 28 Dec 2019 08:39:58 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 08:40:48 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 28 Dec 2019 08:45:43 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:588374d57fdb5120d024340eef3d8927af23a5b806d41b4f049ee430a153c0b4`  
		Last Modified: Sat, 28 Dec 2019 04:49:14 GMT  
		Size: 20.4 MB (20385801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:506cd7f059eaff3f2d682d7b6fccc5ab35050a7391a08c2d2624abd71e7c684c`  
		Last Modified: Sat, 28 Dec 2019 08:51:58 GMT  
		Size: 244.4 KB (244395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88f2783a0e4238e577522ec7c6a6b32cd37f547c4168c768fd5fcbfaa92b6de5`  
		Last Modified: Sat, 28 Dec 2019 08:52:09 GMT  
		Size: 29.4 MB (29433817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb6f35beab9dd7284dbe38b9cf839f586f175ad37c1dcb2833bfdcdbf03a4539`  
		Last Modified: Sat, 28 Dec 2019 08:53:38 GMT  
		Size: 144.5 MB (144473465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6` - linux; 386

```console
$ docker pull mono@sha256:113663c398fb93fe981888f95186bb46d53ceb70ec40b9dd5d2062147bcf30cb
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.4 MB (241440865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67c3139144abd4f519d829e1787e239be574822453c53467c29462efab37ff42`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:42:05 GMT
ADD file:d43798bcf0e72b342c261b8585dde072d9363d19fab4b8d9f08f15db189f287b in / 
# Sat, 28 Dec 2019 04:42:05 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 08:53:34 GMT
ENV MONO_VERSION=6.6.0.161
# Sat, 28 Dec 2019 08:53:44 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 08:54:22 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 28 Dec 2019 08:58:35 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:2cb401c016d2f9802d5ef9cf6c6dc07251e9f87757a0de0a8df318fb7f00385c`  
		Last Modified: Sat, 28 Dec 2019 04:47:36 GMT  
		Size: 23.2 MB (23152142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f6b4fc901f01e72498a390f3e82b1885f694d21c0c86b2c5b722170744653ee`  
		Last Modified: Sat, 28 Dec 2019 09:03:51 GMT  
		Size: 244.5 KB (244481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ef8b692587284955aed9af38c783ccb1813e5f21a78f50075e3a462a575820e`  
		Last Modified: Sat, 28 Dec 2019 09:04:10 GMT  
		Size: 66.7 MB (66749769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e126a79dc65a7868221d13b2fe454087df416e1ea28ef3fb313d2abba6692268`  
		Last Modified: Sat, 28 Dec 2019 09:05:37 GMT  
		Size: 151.3 MB (151294473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6` - linux; ppc64le

```console
$ docker pull mono@sha256:8be78d5e96a5e63f2d4754a3686943f1d8edfd75c46a313cd27984c010e27c52
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.9 MB (178943769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c75d8bc1699ea912f280f4dcb86edababad529239b8eeb28e3801bcd9a015066`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:21 GMT
ADD file:a1ee5955ff3ede8df9558f4bec0c7962d54c43374f857e1da7e2639ddf82a9f1 in / 
# Sat, 28 Dec 2019 04:23:24 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 06:00:10 GMT
ENV MONO_VERSION=6.6.0.161
# Sat, 28 Dec 2019 06:01:14 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 06:02:17 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 28 Dec 2019 06:11:01 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:af52e7ef6e83efadeae17be91daa6ecf61b7dfb39709c29be9b24876e60c0e36`  
		Last Modified: Sat, 28 Dec 2019 04:33:19 GMT  
		Size: 22.8 MB (22800791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:367bf0f7a48952d80f9489622c9b118004dd0fd4763a1fd6153d9b12a571b1ee`  
		Last Modified: Sat, 28 Dec 2019 06:22:04 GMT  
		Size: 244.5 KB (244543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bf3902985b2f759ba0edff57a78d4eb7e81f59e8327b7d243b8f3b4b8ca7c79`  
		Last Modified: Sat, 28 Dec 2019 06:22:14 GMT  
		Size: 25.8 MB (25828829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b12c28397b6cede6691c7e5447b466791fb395f4ecb3d1fb78e68dc1ffe4eb9`  
		Last Modified: Sat, 28 Dec 2019 06:24:05 GMT  
		Size: 130.1 MB (130069606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.6`

```console
$ docker pull mono@sha256:cb8035058b1a14a610fe7a43bc3b3b77ebf97b24313c15a8f414e748f02a7dbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:6.6` - linux; amd64

```console
$ docker pull mono@sha256:3f3ad551a8789a79e3b59c836a659dc748626b0c18543cc9d32ecc1f3d01ee32
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233195367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13ed216b8ba57507781ef13d31102febe0415d37333dd05d96e05f92ad9e9ca3`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:47 GMT
ADD file:90a2c81769a336bed3f731f44a385f2a65b0916f517a0b77c06c224579bf9a9a in / 
# Sat, 28 Dec 2019 04:23:47 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 13:14:15 GMT
ENV MONO_VERSION=6.6.0.161
# Sat, 28 Dec 2019 13:14:25 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 13:15:04 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 28 Dec 2019 13:27:55 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:804555ee037604c40de144f9f8da0d826d38db82f15d74cded32790fe279a8f6`  
		Last Modified: Sat, 28 Dec 2019 04:28:38 GMT  
		Size: 22.5 MB (22524609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01e78f3e714bb9645ac8b6e172f033253467b1312e6dd4889da24aeee207e091`  
		Last Modified: Sat, 28 Dec 2019 13:48:14 GMT  
		Size: 244.5 KB (244485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b64c5ff00a44477231f8da775a76ef1611f6e7879ef3116862f0e13f16e5575f`  
		Last Modified: Sat, 28 Dec 2019 13:48:30 GMT  
		Size: 63.0 MB (62973929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9e6e2e990789fcd233754f316f68b3dcf7fcc8affcb267f1770e6abecd0a4df`  
		Last Modified: Sat, 28 Dec 2019 13:49:41 GMT  
		Size: 147.5 MB (147452344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6` - linux; arm variant v5

```console
$ docker pull mono@sha256:71075f43a6acd5d4900e8b4050bc87b552302d7b550e2d9da1a55aa37eb95852
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.7 MB (176653531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41594e91a86b24e549ebe9f4c951e2403e6e22200d648d599d853dbc7ebe37a5`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:53:16 GMT
ADD file:7d6af454b55cb354e31c096e935358dd5914688ded04ebc76243a4ff598c4495 in / 
# Sat, 28 Dec 2019 04:53:18 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 07:28:31 GMT
ENV MONO_VERSION=6.6.0.161
# Sat, 28 Dec 2019 07:28:56 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 07:29:51 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 28 Dec 2019 07:37:00 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:af28f499fd964f4506ea46c2ac342bc52328a8c30cd633661b69f383a5144e9b`  
		Last Modified: Sat, 28 Dec 2019 05:00:23 GMT  
		Size: 21.2 MB (21202822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f759ae685ca874cea702ae1f63627810d814a2cae6a44c704003176e0c8b37c`  
		Last Modified: Sat, 28 Dec 2019 07:44:23 GMT  
		Size: 244.6 KB (244552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:720fbe46ab0c5e8c2e3e9ed44413d9fde2ad1d45d9161dd0c6a021855acc1b78`  
		Last Modified: Sat, 28 Dec 2019 07:44:33 GMT  
		Size: 25.4 MB (25416500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:906dd0e12894eb03a4ab34eacdf91d163dfd6c09d61c9005e666875d42c1b91b`  
		Last Modified: Sat, 28 Dec 2019 07:46:06 GMT  
		Size: 129.8 MB (129789657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6` - linux; arm variant v7

```console
$ docker pull mono@sha256:7e7ebdba687fb7bac2a796eb557210fe8f5fa55c86cfa342bd56d213a27dcaf3
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.7 MB (172655347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c77176fb08c03220255179938d178739f8882569f72ecaae83ba7b5fc620aef`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 05:03:51 GMT
ADD file:2002ba672e32ae75369830ed6a4734ce62e0118e42390b4d657f0985d6b7fd6a in / 
# Sat, 28 Dec 2019 05:03:53 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 07:37:00 GMT
ENV MONO_VERSION=6.6.0.161
# Sat, 28 Dec 2019 07:37:19 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 07:38:02 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 28 Dec 2019 07:44:03 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:77cf262539006c8df77496f500f74a8c1edd158062440fd94d43d5b1292cefee`  
		Last Modified: Sat, 28 Dec 2019 05:11:13 GMT  
		Size: 19.3 MB (19311587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63ea3a0398ee0834c6b8b5a98490a2451261135d85bbd06845c7077aff2a4667`  
		Last Modified: Sat, 28 Dec 2019 07:50:49 GMT  
		Size: 244.5 KB (244525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f543438b2494429fd7ef0a5cbe2145241dfa4aa2f1008038a251526056612dc`  
		Last Modified: Sat, 28 Dec 2019 07:50:58 GMT  
		Size: 24.6 MB (24648229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:184b3a33ac95fb2ba207e6fc82f4e7fac1dc71bad49531f182c2a7046b54bd39`  
		Last Modified: Sat, 28 Dec 2019 07:52:21 GMT  
		Size: 128.5 MB (128451006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:8aed237906aca013f801430a60e500a1ad6f159c804e14bf4869e9abfcabb89d
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.5 MB (194537478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45a4c03521b1b035e910a91ec512dae28e62411186750460178c6daa0e9809af`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:43:36 GMT
ADD file:ba40f5080cbd89c576c350bfe5acfe16f2ec59636fdb082efc3a8cef66ae7cb7 in / 
# Sat, 28 Dec 2019 04:43:39 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 08:39:40 GMT
ENV MONO_VERSION=6.6.0.161
# Sat, 28 Dec 2019 08:39:58 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 08:40:48 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 28 Dec 2019 08:45:43 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:588374d57fdb5120d024340eef3d8927af23a5b806d41b4f049ee430a153c0b4`  
		Last Modified: Sat, 28 Dec 2019 04:49:14 GMT  
		Size: 20.4 MB (20385801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:506cd7f059eaff3f2d682d7b6fccc5ab35050a7391a08c2d2624abd71e7c684c`  
		Last Modified: Sat, 28 Dec 2019 08:51:58 GMT  
		Size: 244.4 KB (244395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88f2783a0e4238e577522ec7c6a6b32cd37f547c4168c768fd5fcbfaa92b6de5`  
		Last Modified: Sat, 28 Dec 2019 08:52:09 GMT  
		Size: 29.4 MB (29433817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb6f35beab9dd7284dbe38b9cf839f586f175ad37c1dcb2833bfdcdbf03a4539`  
		Last Modified: Sat, 28 Dec 2019 08:53:38 GMT  
		Size: 144.5 MB (144473465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6` - linux; 386

```console
$ docker pull mono@sha256:113663c398fb93fe981888f95186bb46d53ceb70ec40b9dd5d2062147bcf30cb
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.4 MB (241440865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67c3139144abd4f519d829e1787e239be574822453c53467c29462efab37ff42`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:42:05 GMT
ADD file:d43798bcf0e72b342c261b8585dde072d9363d19fab4b8d9f08f15db189f287b in / 
# Sat, 28 Dec 2019 04:42:05 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 08:53:34 GMT
ENV MONO_VERSION=6.6.0.161
# Sat, 28 Dec 2019 08:53:44 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 08:54:22 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 28 Dec 2019 08:58:35 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:2cb401c016d2f9802d5ef9cf6c6dc07251e9f87757a0de0a8df318fb7f00385c`  
		Last Modified: Sat, 28 Dec 2019 04:47:36 GMT  
		Size: 23.2 MB (23152142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f6b4fc901f01e72498a390f3e82b1885f694d21c0c86b2c5b722170744653ee`  
		Last Modified: Sat, 28 Dec 2019 09:03:51 GMT  
		Size: 244.5 KB (244481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ef8b692587284955aed9af38c783ccb1813e5f21a78f50075e3a462a575820e`  
		Last Modified: Sat, 28 Dec 2019 09:04:10 GMT  
		Size: 66.7 MB (66749769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e126a79dc65a7868221d13b2fe454087df416e1ea28ef3fb313d2abba6692268`  
		Last Modified: Sat, 28 Dec 2019 09:05:37 GMT  
		Size: 151.3 MB (151294473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6` - linux; ppc64le

```console
$ docker pull mono@sha256:8be78d5e96a5e63f2d4754a3686943f1d8edfd75c46a313cd27984c010e27c52
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.9 MB (178943769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c75d8bc1699ea912f280f4dcb86edababad529239b8eeb28e3801bcd9a015066`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:21 GMT
ADD file:a1ee5955ff3ede8df9558f4bec0c7962d54c43374f857e1da7e2639ddf82a9f1 in / 
# Sat, 28 Dec 2019 04:23:24 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 06:00:10 GMT
ENV MONO_VERSION=6.6.0.161
# Sat, 28 Dec 2019 06:01:14 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 06:02:17 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 28 Dec 2019 06:11:01 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:af52e7ef6e83efadeae17be91daa6ecf61b7dfb39709c29be9b24876e60c0e36`  
		Last Modified: Sat, 28 Dec 2019 04:33:19 GMT  
		Size: 22.8 MB (22800791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:367bf0f7a48952d80f9489622c9b118004dd0fd4763a1fd6153d9b12a571b1ee`  
		Last Modified: Sat, 28 Dec 2019 06:22:04 GMT  
		Size: 244.5 KB (244543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bf3902985b2f759ba0edff57a78d4eb7e81f59e8327b7d243b8f3b4b8ca7c79`  
		Last Modified: Sat, 28 Dec 2019 06:22:14 GMT  
		Size: 25.8 MB (25828829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b12c28397b6cede6691c7e5447b466791fb395f4ecb3d1fb78e68dc1ffe4eb9`  
		Last Modified: Sat, 28 Dec 2019 06:24:05 GMT  
		Size: 130.1 MB (130069606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.6.0`

```console
$ docker pull mono@sha256:cb8035058b1a14a610fe7a43bc3b3b77ebf97b24313c15a8f414e748f02a7dbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:6.6.0` - linux; amd64

```console
$ docker pull mono@sha256:3f3ad551a8789a79e3b59c836a659dc748626b0c18543cc9d32ecc1f3d01ee32
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233195367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13ed216b8ba57507781ef13d31102febe0415d37333dd05d96e05f92ad9e9ca3`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:47 GMT
ADD file:90a2c81769a336bed3f731f44a385f2a65b0916f517a0b77c06c224579bf9a9a in / 
# Sat, 28 Dec 2019 04:23:47 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 13:14:15 GMT
ENV MONO_VERSION=6.6.0.161
# Sat, 28 Dec 2019 13:14:25 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 13:15:04 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 28 Dec 2019 13:27:55 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:804555ee037604c40de144f9f8da0d826d38db82f15d74cded32790fe279a8f6`  
		Last Modified: Sat, 28 Dec 2019 04:28:38 GMT  
		Size: 22.5 MB (22524609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01e78f3e714bb9645ac8b6e172f033253467b1312e6dd4889da24aeee207e091`  
		Last Modified: Sat, 28 Dec 2019 13:48:14 GMT  
		Size: 244.5 KB (244485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b64c5ff00a44477231f8da775a76ef1611f6e7879ef3116862f0e13f16e5575f`  
		Last Modified: Sat, 28 Dec 2019 13:48:30 GMT  
		Size: 63.0 MB (62973929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9e6e2e990789fcd233754f316f68b3dcf7fcc8affcb267f1770e6abecd0a4df`  
		Last Modified: Sat, 28 Dec 2019 13:49:41 GMT  
		Size: 147.5 MB (147452344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6.0` - linux; arm variant v5

```console
$ docker pull mono@sha256:71075f43a6acd5d4900e8b4050bc87b552302d7b550e2d9da1a55aa37eb95852
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.7 MB (176653531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41594e91a86b24e549ebe9f4c951e2403e6e22200d648d599d853dbc7ebe37a5`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:53:16 GMT
ADD file:7d6af454b55cb354e31c096e935358dd5914688ded04ebc76243a4ff598c4495 in / 
# Sat, 28 Dec 2019 04:53:18 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 07:28:31 GMT
ENV MONO_VERSION=6.6.0.161
# Sat, 28 Dec 2019 07:28:56 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 07:29:51 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 28 Dec 2019 07:37:00 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:af28f499fd964f4506ea46c2ac342bc52328a8c30cd633661b69f383a5144e9b`  
		Last Modified: Sat, 28 Dec 2019 05:00:23 GMT  
		Size: 21.2 MB (21202822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f759ae685ca874cea702ae1f63627810d814a2cae6a44c704003176e0c8b37c`  
		Last Modified: Sat, 28 Dec 2019 07:44:23 GMT  
		Size: 244.6 KB (244552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:720fbe46ab0c5e8c2e3e9ed44413d9fde2ad1d45d9161dd0c6a021855acc1b78`  
		Last Modified: Sat, 28 Dec 2019 07:44:33 GMT  
		Size: 25.4 MB (25416500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:906dd0e12894eb03a4ab34eacdf91d163dfd6c09d61c9005e666875d42c1b91b`  
		Last Modified: Sat, 28 Dec 2019 07:46:06 GMT  
		Size: 129.8 MB (129789657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6.0` - linux; arm variant v7

```console
$ docker pull mono@sha256:7e7ebdba687fb7bac2a796eb557210fe8f5fa55c86cfa342bd56d213a27dcaf3
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.7 MB (172655347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c77176fb08c03220255179938d178739f8882569f72ecaae83ba7b5fc620aef`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 05:03:51 GMT
ADD file:2002ba672e32ae75369830ed6a4734ce62e0118e42390b4d657f0985d6b7fd6a in / 
# Sat, 28 Dec 2019 05:03:53 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 07:37:00 GMT
ENV MONO_VERSION=6.6.0.161
# Sat, 28 Dec 2019 07:37:19 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 07:38:02 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 28 Dec 2019 07:44:03 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:77cf262539006c8df77496f500f74a8c1edd158062440fd94d43d5b1292cefee`  
		Last Modified: Sat, 28 Dec 2019 05:11:13 GMT  
		Size: 19.3 MB (19311587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63ea3a0398ee0834c6b8b5a98490a2451261135d85bbd06845c7077aff2a4667`  
		Last Modified: Sat, 28 Dec 2019 07:50:49 GMT  
		Size: 244.5 KB (244525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f543438b2494429fd7ef0a5cbe2145241dfa4aa2f1008038a251526056612dc`  
		Last Modified: Sat, 28 Dec 2019 07:50:58 GMT  
		Size: 24.6 MB (24648229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:184b3a33ac95fb2ba207e6fc82f4e7fac1dc71bad49531f182c2a7046b54bd39`  
		Last Modified: Sat, 28 Dec 2019 07:52:21 GMT  
		Size: 128.5 MB (128451006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6.0` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:8aed237906aca013f801430a60e500a1ad6f159c804e14bf4869e9abfcabb89d
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.5 MB (194537478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45a4c03521b1b035e910a91ec512dae28e62411186750460178c6daa0e9809af`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:43:36 GMT
ADD file:ba40f5080cbd89c576c350bfe5acfe16f2ec59636fdb082efc3a8cef66ae7cb7 in / 
# Sat, 28 Dec 2019 04:43:39 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 08:39:40 GMT
ENV MONO_VERSION=6.6.0.161
# Sat, 28 Dec 2019 08:39:58 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 08:40:48 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 28 Dec 2019 08:45:43 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:588374d57fdb5120d024340eef3d8927af23a5b806d41b4f049ee430a153c0b4`  
		Last Modified: Sat, 28 Dec 2019 04:49:14 GMT  
		Size: 20.4 MB (20385801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:506cd7f059eaff3f2d682d7b6fccc5ab35050a7391a08c2d2624abd71e7c684c`  
		Last Modified: Sat, 28 Dec 2019 08:51:58 GMT  
		Size: 244.4 KB (244395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88f2783a0e4238e577522ec7c6a6b32cd37f547c4168c768fd5fcbfaa92b6de5`  
		Last Modified: Sat, 28 Dec 2019 08:52:09 GMT  
		Size: 29.4 MB (29433817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb6f35beab9dd7284dbe38b9cf839f586f175ad37c1dcb2833bfdcdbf03a4539`  
		Last Modified: Sat, 28 Dec 2019 08:53:38 GMT  
		Size: 144.5 MB (144473465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6.0` - linux; 386

```console
$ docker pull mono@sha256:113663c398fb93fe981888f95186bb46d53ceb70ec40b9dd5d2062147bcf30cb
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.4 MB (241440865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67c3139144abd4f519d829e1787e239be574822453c53467c29462efab37ff42`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:42:05 GMT
ADD file:d43798bcf0e72b342c261b8585dde072d9363d19fab4b8d9f08f15db189f287b in / 
# Sat, 28 Dec 2019 04:42:05 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 08:53:34 GMT
ENV MONO_VERSION=6.6.0.161
# Sat, 28 Dec 2019 08:53:44 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 08:54:22 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 28 Dec 2019 08:58:35 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:2cb401c016d2f9802d5ef9cf6c6dc07251e9f87757a0de0a8df318fb7f00385c`  
		Last Modified: Sat, 28 Dec 2019 04:47:36 GMT  
		Size: 23.2 MB (23152142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f6b4fc901f01e72498a390f3e82b1885f694d21c0c86b2c5b722170744653ee`  
		Last Modified: Sat, 28 Dec 2019 09:03:51 GMT  
		Size: 244.5 KB (244481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ef8b692587284955aed9af38c783ccb1813e5f21a78f50075e3a462a575820e`  
		Last Modified: Sat, 28 Dec 2019 09:04:10 GMT  
		Size: 66.7 MB (66749769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e126a79dc65a7868221d13b2fe454087df416e1ea28ef3fb313d2abba6692268`  
		Last Modified: Sat, 28 Dec 2019 09:05:37 GMT  
		Size: 151.3 MB (151294473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6.0` - linux; ppc64le

```console
$ docker pull mono@sha256:8be78d5e96a5e63f2d4754a3686943f1d8edfd75c46a313cd27984c010e27c52
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.9 MB (178943769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c75d8bc1699ea912f280f4dcb86edababad529239b8eeb28e3801bcd9a015066`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:21 GMT
ADD file:a1ee5955ff3ede8df9558f4bec0c7962d54c43374f857e1da7e2639ddf82a9f1 in / 
# Sat, 28 Dec 2019 04:23:24 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 06:00:10 GMT
ENV MONO_VERSION=6.6.0.161
# Sat, 28 Dec 2019 06:01:14 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 06:02:17 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 28 Dec 2019 06:11:01 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:af52e7ef6e83efadeae17be91daa6ecf61b7dfb39709c29be9b24876e60c0e36`  
		Last Modified: Sat, 28 Dec 2019 04:33:19 GMT  
		Size: 22.8 MB (22800791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:367bf0f7a48952d80f9489622c9b118004dd0fd4763a1fd6153d9b12a571b1ee`  
		Last Modified: Sat, 28 Dec 2019 06:22:04 GMT  
		Size: 244.5 KB (244543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bf3902985b2f759ba0edff57a78d4eb7e81f59e8327b7d243b8f3b4b8ca7c79`  
		Last Modified: Sat, 28 Dec 2019 06:22:14 GMT  
		Size: 25.8 MB (25828829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b12c28397b6cede6691c7e5447b466791fb395f4ecb3d1fb78e68dc1ffe4eb9`  
		Last Modified: Sat, 28 Dec 2019 06:24:05 GMT  
		Size: 130.1 MB (130069606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.6.0.161`

```console
$ docker pull mono@sha256:cb8035058b1a14a610fe7a43bc3b3b77ebf97b24313c15a8f414e748f02a7dbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:6.6.0.161` - linux; amd64

```console
$ docker pull mono@sha256:3f3ad551a8789a79e3b59c836a659dc748626b0c18543cc9d32ecc1f3d01ee32
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233195367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13ed216b8ba57507781ef13d31102febe0415d37333dd05d96e05f92ad9e9ca3`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:47 GMT
ADD file:90a2c81769a336bed3f731f44a385f2a65b0916f517a0b77c06c224579bf9a9a in / 
# Sat, 28 Dec 2019 04:23:47 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 13:14:15 GMT
ENV MONO_VERSION=6.6.0.161
# Sat, 28 Dec 2019 13:14:25 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 13:15:04 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 28 Dec 2019 13:27:55 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:804555ee037604c40de144f9f8da0d826d38db82f15d74cded32790fe279a8f6`  
		Last Modified: Sat, 28 Dec 2019 04:28:38 GMT  
		Size: 22.5 MB (22524609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01e78f3e714bb9645ac8b6e172f033253467b1312e6dd4889da24aeee207e091`  
		Last Modified: Sat, 28 Dec 2019 13:48:14 GMT  
		Size: 244.5 KB (244485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b64c5ff00a44477231f8da775a76ef1611f6e7879ef3116862f0e13f16e5575f`  
		Last Modified: Sat, 28 Dec 2019 13:48:30 GMT  
		Size: 63.0 MB (62973929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9e6e2e990789fcd233754f316f68b3dcf7fcc8affcb267f1770e6abecd0a4df`  
		Last Modified: Sat, 28 Dec 2019 13:49:41 GMT  
		Size: 147.5 MB (147452344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6.0.161` - linux; arm variant v5

```console
$ docker pull mono@sha256:71075f43a6acd5d4900e8b4050bc87b552302d7b550e2d9da1a55aa37eb95852
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.7 MB (176653531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41594e91a86b24e549ebe9f4c951e2403e6e22200d648d599d853dbc7ebe37a5`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:53:16 GMT
ADD file:7d6af454b55cb354e31c096e935358dd5914688ded04ebc76243a4ff598c4495 in / 
# Sat, 28 Dec 2019 04:53:18 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 07:28:31 GMT
ENV MONO_VERSION=6.6.0.161
# Sat, 28 Dec 2019 07:28:56 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 07:29:51 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 28 Dec 2019 07:37:00 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:af28f499fd964f4506ea46c2ac342bc52328a8c30cd633661b69f383a5144e9b`  
		Last Modified: Sat, 28 Dec 2019 05:00:23 GMT  
		Size: 21.2 MB (21202822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f759ae685ca874cea702ae1f63627810d814a2cae6a44c704003176e0c8b37c`  
		Last Modified: Sat, 28 Dec 2019 07:44:23 GMT  
		Size: 244.6 KB (244552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:720fbe46ab0c5e8c2e3e9ed44413d9fde2ad1d45d9161dd0c6a021855acc1b78`  
		Last Modified: Sat, 28 Dec 2019 07:44:33 GMT  
		Size: 25.4 MB (25416500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:906dd0e12894eb03a4ab34eacdf91d163dfd6c09d61c9005e666875d42c1b91b`  
		Last Modified: Sat, 28 Dec 2019 07:46:06 GMT  
		Size: 129.8 MB (129789657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6.0.161` - linux; arm variant v7

```console
$ docker pull mono@sha256:7e7ebdba687fb7bac2a796eb557210fe8f5fa55c86cfa342bd56d213a27dcaf3
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.7 MB (172655347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c77176fb08c03220255179938d178739f8882569f72ecaae83ba7b5fc620aef`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 05:03:51 GMT
ADD file:2002ba672e32ae75369830ed6a4734ce62e0118e42390b4d657f0985d6b7fd6a in / 
# Sat, 28 Dec 2019 05:03:53 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 07:37:00 GMT
ENV MONO_VERSION=6.6.0.161
# Sat, 28 Dec 2019 07:37:19 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 07:38:02 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 28 Dec 2019 07:44:03 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:77cf262539006c8df77496f500f74a8c1edd158062440fd94d43d5b1292cefee`  
		Last Modified: Sat, 28 Dec 2019 05:11:13 GMT  
		Size: 19.3 MB (19311587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63ea3a0398ee0834c6b8b5a98490a2451261135d85bbd06845c7077aff2a4667`  
		Last Modified: Sat, 28 Dec 2019 07:50:49 GMT  
		Size: 244.5 KB (244525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f543438b2494429fd7ef0a5cbe2145241dfa4aa2f1008038a251526056612dc`  
		Last Modified: Sat, 28 Dec 2019 07:50:58 GMT  
		Size: 24.6 MB (24648229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:184b3a33ac95fb2ba207e6fc82f4e7fac1dc71bad49531f182c2a7046b54bd39`  
		Last Modified: Sat, 28 Dec 2019 07:52:21 GMT  
		Size: 128.5 MB (128451006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6.0.161` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:8aed237906aca013f801430a60e500a1ad6f159c804e14bf4869e9abfcabb89d
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.5 MB (194537478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45a4c03521b1b035e910a91ec512dae28e62411186750460178c6daa0e9809af`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:43:36 GMT
ADD file:ba40f5080cbd89c576c350bfe5acfe16f2ec59636fdb082efc3a8cef66ae7cb7 in / 
# Sat, 28 Dec 2019 04:43:39 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 08:39:40 GMT
ENV MONO_VERSION=6.6.0.161
# Sat, 28 Dec 2019 08:39:58 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 08:40:48 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 28 Dec 2019 08:45:43 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:588374d57fdb5120d024340eef3d8927af23a5b806d41b4f049ee430a153c0b4`  
		Last Modified: Sat, 28 Dec 2019 04:49:14 GMT  
		Size: 20.4 MB (20385801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:506cd7f059eaff3f2d682d7b6fccc5ab35050a7391a08c2d2624abd71e7c684c`  
		Last Modified: Sat, 28 Dec 2019 08:51:58 GMT  
		Size: 244.4 KB (244395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88f2783a0e4238e577522ec7c6a6b32cd37f547c4168c768fd5fcbfaa92b6de5`  
		Last Modified: Sat, 28 Dec 2019 08:52:09 GMT  
		Size: 29.4 MB (29433817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb6f35beab9dd7284dbe38b9cf839f586f175ad37c1dcb2833bfdcdbf03a4539`  
		Last Modified: Sat, 28 Dec 2019 08:53:38 GMT  
		Size: 144.5 MB (144473465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6.0.161` - linux; 386

```console
$ docker pull mono@sha256:113663c398fb93fe981888f95186bb46d53ceb70ec40b9dd5d2062147bcf30cb
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.4 MB (241440865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67c3139144abd4f519d829e1787e239be574822453c53467c29462efab37ff42`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:42:05 GMT
ADD file:d43798bcf0e72b342c261b8585dde072d9363d19fab4b8d9f08f15db189f287b in / 
# Sat, 28 Dec 2019 04:42:05 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 08:53:34 GMT
ENV MONO_VERSION=6.6.0.161
# Sat, 28 Dec 2019 08:53:44 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 08:54:22 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 28 Dec 2019 08:58:35 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:2cb401c016d2f9802d5ef9cf6c6dc07251e9f87757a0de0a8df318fb7f00385c`  
		Last Modified: Sat, 28 Dec 2019 04:47:36 GMT  
		Size: 23.2 MB (23152142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f6b4fc901f01e72498a390f3e82b1885f694d21c0c86b2c5b722170744653ee`  
		Last Modified: Sat, 28 Dec 2019 09:03:51 GMT  
		Size: 244.5 KB (244481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ef8b692587284955aed9af38c783ccb1813e5f21a78f50075e3a462a575820e`  
		Last Modified: Sat, 28 Dec 2019 09:04:10 GMT  
		Size: 66.7 MB (66749769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e126a79dc65a7868221d13b2fe454087df416e1ea28ef3fb313d2abba6692268`  
		Last Modified: Sat, 28 Dec 2019 09:05:37 GMT  
		Size: 151.3 MB (151294473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6.0.161` - linux; ppc64le

```console
$ docker pull mono@sha256:8be78d5e96a5e63f2d4754a3686943f1d8edfd75c46a313cd27984c010e27c52
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.9 MB (178943769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c75d8bc1699ea912f280f4dcb86edababad529239b8eeb28e3801bcd9a015066`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:21 GMT
ADD file:a1ee5955ff3ede8df9558f4bec0c7962d54c43374f857e1da7e2639ddf82a9f1 in / 
# Sat, 28 Dec 2019 04:23:24 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 06:00:10 GMT
ENV MONO_VERSION=6.6.0.161
# Sat, 28 Dec 2019 06:01:14 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 06:02:17 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 28 Dec 2019 06:11:01 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:af52e7ef6e83efadeae17be91daa6ecf61b7dfb39709c29be9b24876e60c0e36`  
		Last Modified: Sat, 28 Dec 2019 04:33:19 GMT  
		Size: 22.8 MB (22800791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:367bf0f7a48952d80f9489622c9b118004dd0fd4763a1fd6153d9b12a571b1ee`  
		Last Modified: Sat, 28 Dec 2019 06:22:04 GMT  
		Size: 244.5 KB (244543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bf3902985b2f759ba0edff57a78d4eb7e81f59e8327b7d243b8f3b4b8ca7c79`  
		Last Modified: Sat, 28 Dec 2019 06:22:14 GMT  
		Size: 25.8 MB (25828829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b12c28397b6cede6691c7e5447b466791fb395f4ecb3d1fb78e68dc1ffe4eb9`  
		Last Modified: Sat, 28 Dec 2019 06:24:05 GMT  
		Size: 130.1 MB (130069606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.6.0.161-slim`

```console
$ docker pull mono@sha256:dcd8a1b2f83384f688f944067becc698beb04988f213a0bfee2d785977e15bbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:6.6.0.161-slim` - linux; amd64

```console
$ docker pull mono@sha256:dbf079afc972cbf36017055c5dfa8b63e8495e68ed7a12782ff4e3b632100af0
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.7 MB (85743023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c13361f8aea3337ed6ca565868d63ed73db5104f6c26dfa91ce41d1ce1e5082`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:47 GMT
ADD file:90a2c81769a336bed3f731f44a385f2a65b0916f517a0b77c06c224579bf9a9a in / 
# Sat, 28 Dec 2019 04:23:47 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 13:14:15 GMT
ENV MONO_VERSION=6.6.0.161
# Sat, 28 Dec 2019 13:14:25 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 13:15:04 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:804555ee037604c40de144f9f8da0d826d38db82f15d74cded32790fe279a8f6`  
		Last Modified: Sat, 28 Dec 2019 04:28:38 GMT  
		Size: 22.5 MB (22524609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01e78f3e714bb9645ac8b6e172f033253467b1312e6dd4889da24aeee207e091`  
		Last Modified: Sat, 28 Dec 2019 13:48:14 GMT  
		Size: 244.5 KB (244485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b64c5ff00a44477231f8da775a76ef1611f6e7879ef3116862f0e13f16e5575f`  
		Last Modified: Sat, 28 Dec 2019 13:48:30 GMT  
		Size: 63.0 MB (62973929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6.0.161-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:263841647b1413f97ede49244a3250c2bd9224534cfda1f58a4cef015523f95e
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46863874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f24cceab2b02f7699b97ad45390d24175d4f6cbc35951f14304e31bb40284717`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:53:16 GMT
ADD file:7d6af454b55cb354e31c096e935358dd5914688ded04ebc76243a4ff598c4495 in / 
# Sat, 28 Dec 2019 04:53:18 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 07:28:31 GMT
ENV MONO_VERSION=6.6.0.161
# Sat, 28 Dec 2019 07:28:56 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 07:29:51 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:af28f499fd964f4506ea46c2ac342bc52328a8c30cd633661b69f383a5144e9b`  
		Last Modified: Sat, 28 Dec 2019 05:00:23 GMT  
		Size: 21.2 MB (21202822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f759ae685ca874cea702ae1f63627810d814a2cae6a44c704003176e0c8b37c`  
		Last Modified: Sat, 28 Dec 2019 07:44:23 GMT  
		Size: 244.6 KB (244552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:720fbe46ab0c5e8c2e3e9ed44413d9fde2ad1d45d9161dd0c6a021855acc1b78`  
		Last Modified: Sat, 28 Dec 2019 07:44:33 GMT  
		Size: 25.4 MB (25416500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6.0.161-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:70f8a6f90eedb2b040cdfe84d228b3b26f0549a32b275183a056543a822ebc44
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44204341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f0d6480804e64f949cbbdd9cc9ba45c6e077cd0266e5641b4822ce6ac3e6663`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 05:03:51 GMT
ADD file:2002ba672e32ae75369830ed6a4734ce62e0118e42390b4d657f0985d6b7fd6a in / 
# Sat, 28 Dec 2019 05:03:53 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 07:37:00 GMT
ENV MONO_VERSION=6.6.0.161
# Sat, 28 Dec 2019 07:37:19 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 07:38:02 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:77cf262539006c8df77496f500f74a8c1edd158062440fd94d43d5b1292cefee`  
		Last Modified: Sat, 28 Dec 2019 05:11:13 GMT  
		Size: 19.3 MB (19311587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63ea3a0398ee0834c6b8b5a98490a2451261135d85bbd06845c7077aff2a4667`  
		Last Modified: Sat, 28 Dec 2019 07:50:49 GMT  
		Size: 244.5 KB (244525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f543438b2494429fd7ef0a5cbe2145241dfa4aa2f1008038a251526056612dc`  
		Last Modified: Sat, 28 Dec 2019 07:50:58 GMT  
		Size: 24.6 MB (24648229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6.0.161-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:0bd2ad5bfc5c4cddadd84d69dbf002b1e0669df16b5f6d1cf7051c6a3802d260
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50064013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b627d7b684f3642760e6c76a7e5a63fbe1006453301de18a9166f7ec9b9071f`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:43:36 GMT
ADD file:ba40f5080cbd89c576c350bfe5acfe16f2ec59636fdb082efc3a8cef66ae7cb7 in / 
# Sat, 28 Dec 2019 04:43:39 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 08:39:40 GMT
ENV MONO_VERSION=6.6.0.161
# Sat, 28 Dec 2019 08:39:58 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 08:40:48 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:588374d57fdb5120d024340eef3d8927af23a5b806d41b4f049ee430a153c0b4`  
		Last Modified: Sat, 28 Dec 2019 04:49:14 GMT  
		Size: 20.4 MB (20385801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:506cd7f059eaff3f2d682d7b6fccc5ab35050a7391a08c2d2624abd71e7c684c`  
		Last Modified: Sat, 28 Dec 2019 08:51:58 GMT  
		Size: 244.4 KB (244395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88f2783a0e4238e577522ec7c6a6b32cd37f547c4168c768fd5fcbfaa92b6de5`  
		Last Modified: Sat, 28 Dec 2019 08:52:09 GMT  
		Size: 29.4 MB (29433817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6.0.161-slim` - linux; 386

```console
$ docker pull mono@sha256:1470434632f62ac60985681302e025a1a93fb7c696224fa2f5fbafb8f168bf7e
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.1 MB (90146392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6872c3284610e489106962651891765f6a5b3a1418c06cda514d1db86209162e`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:42:05 GMT
ADD file:d43798bcf0e72b342c261b8585dde072d9363d19fab4b8d9f08f15db189f287b in / 
# Sat, 28 Dec 2019 04:42:05 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 08:53:34 GMT
ENV MONO_VERSION=6.6.0.161
# Sat, 28 Dec 2019 08:53:44 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 08:54:22 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:2cb401c016d2f9802d5ef9cf6c6dc07251e9f87757a0de0a8df318fb7f00385c`  
		Last Modified: Sat, 28 Dec 2019 04:47:36 GMT  
		Size: 23.2 MB (23152142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f6b4fc901f01e72498a390f3e82b1885f694d21c0c86b2c5b722170744653ee`  
		Last Modified: Sat, 28 Dec 2019 09:03:51 GMT  
		Size: 244.5 KB (244481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ef8b692587284955aed9af38c783ccb1813e5f21a78f50075e3a462a575820e`  
		Last Modified: Sat, 28 Dec 2019 09:04:10 GMT  
		Size: 66.7 MB (66749769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6.0.161-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:a7840aa6d9953b14f7d37472ed11dc4785cff7c5edbf16718bfc36a6d9cf58b6
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48874163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ea84dffac95f8be085f5eeb79990afa1341135da9867d71688f2d9a3b61bfbf`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:21 GMT
ADD file:a1ee5955ff3ede8df9558f4bec0c7962d54c43374f857e1da7e2639ddf82a9f1 in / 
# Sat, 28 Dec 2019 04:23:24 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 06:00:10 GMT
ENV MONO_VERSION=6.6.0.161
# Sat, 28 Dec 2019 06:01:14 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 06:02:17 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:af52e7ef6e83efadeae17be91daa6ecf61b7dfb39709c29be9b24876e60c0e36`  
		Last Modified: Sat, 28 Dec 2019 04:33:19 GMT  
		Size: 22.8 MB (22800791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:367bf0f7a48952d80f9489622c9b118004dd0fd4763a1fd6153d9b12a571b1ee`  
		Last Modified: Sat, 28 Dec 2019 06:22:04 GMT  
		Size: 244.5 KB (244543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bf3902985b2f759ba0edff57a78d4eb7e81f59e8327b7d243b8f3b4b8ca7c79`  
		Last Modified: Sat, 28 Dec 2019 06:22:14 GMT  
		Size: 25.8 MB (25828829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.6.0-slim`

```console
$ docker pull mono@sha256:dcd8a1b2f83384f688f944067becc698beb04988f213a0bfee2d785977e15bbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:6.6.0-slim` - linux; amd64

```console
$ docker pull mono@sha256:dbf079afc972cbf36017055c5dfa8b63e8495e68ed7a12782ff4e3b632100af0
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.7 MB (85743023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c13361f8aea3337ed6ca565868d63ed73db5104f6c26dfa91ce41d1ce1e5082`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:47 GMT
ADD file:90a2c81769a336bed3f731f44a385f2a65b0916f517a0b77c06c224579bf9a9a in / 
# Sat, 28 Dec 2019 04:23:47 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 13:14:15 GMT
ENV MONO_VERSION=6.6.0.161
# Sat, 28 Dec 2019 13:14:25 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 13:15:04 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:804555ee037604c40de144f9f8da0d826d38db82f15d74cded32790fe279a8f6`  
		Last Modified: Sat, 28 Dec 2019 04:28:38 GMT  
		Size: 22.5 MB (22524609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01e78f3e714bb9645ac8b6e172f033253467b1312e6dd4889da24aeee207e091`  
		Last Modified: Sat, 28 Dec 2019 13:48:14 GMT  
		Size: 244.5 KB (244485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b64c5ff00a44477231f8da775a76ef1611f6e7879ef3116862f0e13f16e5575f`  
		Last Modified: Sat, 28 Dec 2019 13:48:30 GMT  
		Size: 63.0 MB (62973929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6.0-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:263841647b1413f97ede49244a3250c2bd9224534cfda1f58a4cef015523f95e
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46863874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f24cceab2b02f7699b97ad45390d24175d4f6cbc35951f14304e31bb40284717`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:53:16 GMT
ADD file:7d6af454b55cb354e31c096e935358dd5914688ded04ebc76243a4ff598c4495 in / 
# Sat, 28 Dec 2019 04:53:18 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 07:28:31 GMT
ENV MONO_VERSION=6.6.0.161
# Sat, 28 Dec 2019 07:28:56 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 07:29:51 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:af28f499fd964f4506ea46c2ac342bc52328a8c30cd633661b69f383a5144e9b`  
		Last Modified: Sat, 28 Dec 2019 05:00:23 GMT  
		Size: 21.2 MB (21202822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f759ae685ca874cea702ae1f63627810d814a2cae6a44c704003176e0c8b37c`  
		Last Modified: Sat, 28 Dec 2019 07:44:23 GMT  
		Size: 244.6 KB (244552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:720fbe46ab0c5e8c2e3e9ed44413d9fde2ad1d45d9161dd0c6a021855acc1b78`  
		Last Modified: Sat, 28 Dec 2019 07:44:33 GMT  
		Size: 25.4 MB (25416500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6.0-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:70f8a6f90eedb2b040cdfe84d228b3b26f0549a32b275183a056543a822ebc44
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44204341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f0d6480804e64f949cbbdd9cc9ba45c6e077cd0266e5641b4822ce6ac3e6663`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 05:03:51 GMT
ADD file:2002ba672e32ae75369830ed6a4734ce62e0118e42390b4d657f0985d6b7fd6a in / 
# Sat, 28 Dec 2019 05:03:53 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 07:37:00 GMT
ENV MONO_VERSION=6.6.0.161
# Sat, 28 Dec 2019 07:37:19 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 07:38:02 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:77cf262539006c8df77496f500f74a8c1edd158062440fd94d43d5b1292cefee`  
		Last Modified: Sat, 28 Dec 2019 05:11:13 GMT  
		Size: 19.3 MB (19311587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63ea3a0398ee0834c6b8b5a98490a2451261135d85bbd06845c7077aff2a4667`  
		Last Modified: Sat, 28 Dec 2019 07:50:49 GMT  
		Size: 244.5 KB (244525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f543438b2494429fd7ef0a5cbe2145241dfa4aa2f1008038a251526056612dc`  
		Last Modified: Sat, 28 Dec 2019 07:50:58 GMT  
		Size: 24.6 MB (24648229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6.0-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:0bd2ad5bfc5c4cddadd84d69dbf002b1e0669df16b5f6d1cf7051c6a3802d260
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50064013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b627d7b684f3642760e6c76a7e5a63fbe1006453301de18a9166f7ec9b9071f`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:43:36 GMT
ADD file:ba40f5080cbd89c576c350bfe5acfe16f2ec59636fdb082efc3a8cef66ae7cb7 in / 
# Sat, 28 Dec 2019 04:43:39 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 08:39:40 GMT
ENV MONO_VERSION=6.6.0.161
# Sat, 28 Dec 2019 08:39:58 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 08:40:48 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:588374d57fdb5120d024340eef3d8927af23a5b806d41b4f049ee430a153c0b4`  
		Last Modified: Sat, 28 Dec 2019 04:49:14 GMT  
		Size: 20.4 MB (20385801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:506cd7f059eaff3f2d682d7b6fccc5ab35050a7391a08c2d2624abd71e7c684c`  
		Last Modified: Sat, 28 Dec 2019 08:51:58 GMT  
		Size: 244.4 KB (244395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88f2783a0e4238e577522ec7c6a6b32cd37f547c4168c768fd5fcbfaa92b6de5`  
		Last Modified: Sat, 28 Dec 2019 08:52:09 GMT  
		Size: 29.4 MB (29433817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6.0-slim` - linux; 386

```console
$ docker pull mono@sha256:1470434632f62ac60985681302e025a1a93fb7c696224fa2f5fbafb8f168bf7e
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.1 MB (90146392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6872c3284610e489106962651891765f6a5b3a1418c06cda514d1db86209162e`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:42:05 GMT
ADD file:d43798bcf0e72b342c261b8585dde072d9363d19fab4b8d9f08f15db189f287b in / 
# Sat, 28 Dec 2019 04:42:05 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 08:53:34 GMT
ENV MONO_VERSION=6.6.0.161
# Sat, 28 Dec 2019 08:53:44 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 08:54:22 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:2cb401c016d2f9802d5ef9cf6c6dc07251e9f87757a0de0a8df318fb7f00385c`  
		Last Modified: Sat, 28 Dec 2019 04:47:36 GMT  
		Size: 23.2 MB (23152142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f6b4fc901f01e72498a390f3e82b1885f694d21c0c86b2c5b722170744653ee`  
		Last Modified: Sat, 28 Dec 2019 09:03:51 GMT  
		Size: 244.5 KB (244481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ef8b692587284955aed9af38c783ccb1813e5f21a78f50075e3a462a575820e`  
		Last Modified: Sat, 28 Dec 2019 09:04:10 GMT  
		Size: 66.7 MB (66749769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6.0-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:a7840aa6d9953b14f7d37472ed11dc4785cff7c5edbf16718bfc36a6d9cf58b6
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48874163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ea84dffac95f8be085f5eeb79990afa1341135da9867d71688f2d9a3b61bfbf`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:21 GMT
ADD file:a1ee5955ff3ede8df9558f4bec0c7962d54c43374f857e1da7e2639ddf82a9f1 in / 
# Sat, 28 Dec 2019 04:23:24 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 06:00:10 GMT
ENV MONO_VERSION=6.6.0.161
# Sat, 28 Dec 2019 06:01:14 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 06:02:17 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:af52e7ef6e83efadeae17be91daa6ecf61b7dfb39709c29be9b24876e60c0e36`  
		Last Modified: Sat, 28 Dec 2019 04:33:19 GMT  
		Size: 22.8 MB (22800791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:367bf0f7a48952d80f9489622c9b118004dd0fd4763a1fd6153d9b12a571b1ee`  
		Last Modified: Sat, 28 Dec 2019 06:22:04 GMT  
		Size: 244.5 KB (244543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bf3902985b2f759ba0edff57a78d4eb7e81f59e8327b7d243b8f3b4b8ca7c79`  
		Last Modified: Sat, 28 Dec 2019 06:22:14 GMT  
		Size: 25.8 MB (25828829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.6-slim`

```console
$ docker pull mono@sha256:dcd8a1b2f83384f688f944067becc698beb04988f213a0bfee2d785977e15bbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:6.6-slim` - linux; amd64

```console
$ docker pull mono@sha256:dbf079afc972cbf36017055c5dfa8b63e8495e68ed7a12782ff4e3b632100af0
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.7 MB (85743023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c13361f8aea3337ed6ca565868d63ed73db5104f6c26dfa91ce41d1ce1e5082`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:47 GMT
ADD file:90a2c81769a336bed3f731f44a385f2a65b0916f517a0b77c06c224579bf9a9a in / 
# Sat, 28 Dec 2019 04:23:47 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 13:14:15 GMT
ENV MONO_VERSION=6.6.0.161
# Sat, 28 Dec 2019 13:14:25 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 13:15:04 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:804555ee037604c40de144f9f8da0d826d38db82f15d74cded32790fe279a8f6`  
		Last Modified: Sat, 28 Dec 2019 04:28:38 GMT  
		Size: 22.5 MB (22524609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01e78f3e714bb9645ac8b6e172f033253467b1312e6dd4889da24aeee207e091`  
		Last Modified: Sat, 28 Dec 2019 13:48:14 GMT  
		Size: 244.5 KB (244485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b64c5ff00a44477231f8da775a76ef1611f6e7879ef3116862f0e13f16e5575f`  
		Last Modified: Sat, 28 Dec 2019 13:48:30 GMT  
		Size: 63.0 MB (62973929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:263841647b1413f97ede49244a3250c2bd9224534cfda1f58a4cef015523f95e
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46863874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f24cceab2b02f7699b97ad45390d24175d4f6cbc35951f14304e31bb40284717`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:53:16 GMT
ADD file:7d6af454b55cb354e31c096e935358dd5914688ded04ebc76243a4ff598c4495 in / 
# Sat, 28 Dec 2019 04:53:18 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 07:28:31 GMT
ENV MONO_VERSION=6.6.0.161
# Sat, 28 Dec 2019 07:28:56 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 07:29:51 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:af28f499fd964f4506ea46c2ac342bc52328a8c30cd633661b69f383a5144e9b`  
		Last Modified: Sat, 28 Dec 2019 05:00:23 GMT  
		Size: 21.2 MB (21202822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f759ae685ca874cea702ae1f63627810d814a2cae6a44c704003176e0c8b37c`  
		Last Modified: Sat, 28 Dec 2019 07:44:23 GMT  
		Size: 244.6 KB (244552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:720fbe46ab0c5e8c2e3e9ed44413d9fde2ad1d45d9161dd0c6a021855acc1b78`  
		Last Modified: Sat, 28 Dec 2019 07:44:33 GMT  
		Size: 25.4 MB (25416500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:70f8a6f90eedb2b040cdfe84d228b3b26f0549a32b275183a056543a822ebc44
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44204341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f0d6480804e64f949cbbdd9cc9ba45c6e077cd0266e5641b4822ce6ac3e6663`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 05:03:51 GMT
ADD file:2002ba672e32ae75369830ed6a4734ce62e0118e42390b4d657f0985d6b7fd6a in / 
# Sat, 28 Dec 2019 05:03:53 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 07:37:00 GMT
ENV MONO_VERSION=6.6.0.161
# Sat, 28 Dec 2019 07:37:19 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 07:38:02 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:77cf262539006c8df77496f500f74a8c1edd158062440fd94d43d5b1292cefee`  
		Last Modified: Sat, 28 Dec 2019 05:11:13 GMT  
		Size: 19.3 MB (19311587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63ea3a0398ee0834c6b8b5a98490a2451261135d85bbd06845c7077aff2a4667`  
		Last Modified: Sat, 28 Dec 2019 07:50:49 GMT  
		Size: 244.5 KB (244525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f543438b2494429fd7ef0a5cbe2145241dfa4aa2f1008038a251526056612dc`  
		Last Modified: Sat, 28 Dec 2019 07:50:58 GMT  
		Size: 24.6 MB (24648229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:0bd2ad5bfc5c4cddadd84d69dbf002b1e0669df16b5f6d1cf7051c6a3802d260
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50064013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b627d7b684f3642760e6c76a7e5a63fbe1006453301de18a9166f7ec9b9071f`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:43:36 GMT
ADD file:ba40f5080cbd89c576c350bfe5acfe16f2ec59636fdb082efc3a8cef66ae7cb7 in / 
# Sat, 28 Dec 2019 04:43:39 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 08:39:40 GMT
ENV MONO_VERSION=6.6.0.161
# Sat, 28 Dec 2019 08:39:58 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 08:40:48 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:588374d57fdb5120d024340eef3d8927af23a5b806d41b4f049ee430a153c0b4`  
		Last Modified: Sat, 28 Dec 2019 04:49:14 GMT  
		Size: 20.4 MB (20385801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:506cd7f059eaff3f2d682d7b6fccc5ab35050a7391a08c2d2624abd71e7c684c`  
		Last Modified: Sat, 28 Dec 2019 08:51:58 GMT  
		Size: 244.4 KB (244395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88f2783a0e4238e577522ec7c6a6b32cd37f547c4168c768fd5fcbfaa92b6de5`  
		Last Modified: Sat, 28 Dec 2019 08:52:09 GMT  
		Size: 29.4 MB (29433817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6-slim` - linux; 386

```console
$ docker pull mono@sha256:1470434632f62ac60985681302e025a1a93fb7c696224fa2f5fbafb8f168bf7e
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.1 MB (90146392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6872c3284610e489106962651891765f6a5b3a1418c06cda514d1db86209162e`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:42:05 GMT
ADD file:d43798bcf0e72b342c261b8585dde072d9363d19fab4b8d9f08f15db189f287b in / 
# Sat, 28 Dec 2019 04:42:05 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 08:53:34 GMT
ENV MONO_VERSION=6.6.0.161
# Sat, 28 Dec 2019 08:53:44 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 08:54:22 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:2cb401c016d2f9802d5ef9cf6c6dc07251e9f87757a0de0a8df318fb7f00385c`  
		Last Modified: Sat, 28 Dec 2019 04:47:36 GMT  
		Size: 23.2 MB (23152142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f6b4fc901f01e72498a390f3e82b1885f694d21c0c86b2c5b722170744653ee`  
		Last Modified: Sat, 28 Dec 2019 09:03:51 GMT  
		Size: 244.5 KB (244481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ef8b692587284955aed9af38c783ccb1813e5f21a78f50075e3a462a575820e`  
		Last Modified: Sat, 28 Dec 2019 09:04:10 GMT  
		Size: 66.7 MB (66749769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:a7840aa6d9953b14f7d37472ed11dc4785cff7c5edbf16718bfc36a6d9cf58b6
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48874163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ea84dffac95f8be085f5eeb79990afa1341135da9867d71688f2d9a3b61bfbf`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:21 GMT
ADD file:a1ee5955ff3ede8df9558f4bec0c7962d54c43374f857e1da7e2639ddf82a9f1 in / 
# Sat, 28 Dec 2019 04:23:24 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 06:00:10 GMT
ENV MONO_VERSION=6.6.0.161
# Sat, 28 Dec 2019 06:01:14 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 06:02:17 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:af52e7ef6e83efadeae17be91daa6ecf61b7dfb39709c29be9b24876e60c0e36`  
		Last Modified: Sat, 28 Dec 2019 04:33:19 GMT  
		Size: 22.8 MB (22800791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:367bf0f7a48952d80f9489622c9b118004dd0fd4763a1fd6153d9b12a571b1ee`  
		Last Modified: Sat, 28 Dec 2019 06:22:04 GMT  
		Size: 244.5 KB (244543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bf3902985b2f759ba0edff57a78d4eb7e81f59e8327b7d243b8f3b4b8ca7c79`  
		Last Modified: Sat, 28 Dec 2019 06:22:14 GMT  
		Size: 25.8 MB (25828829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.8`

```console
$ docker pull mono@sha256:a8409dff6597f2ef5f7ecd3c672671bb2af9a390073efd74f95c54aa41cba22a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:

## `mono:6.8.0`

```console
$ docker pull mono@sha256:a8409dff6597f2ef5f7ecd3c672671bb2af9a390073efd74f95c54aa41cba22a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:

## `mono:6.8.0.96`

```console
$ docker pull mono@sha256:a8409dff6597f2ef5f7ecd3c672671bb2af9a390073efd74f95c54aa41cba22a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:

## `mono:6.8.0.96-slim`

```console
$ docker pull mono@sha256:a8409dff6597f2ef5f7ecd3c672671bb2af9a390073efd74f95c54aa41cba22a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:

## `mono:6.8.0-slim`

```console
$ docker pull mono@sha256:a8409dff6597f2ef5f7ecd3c672671bb2af9a390073efd74f95c54aa41cba22a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:

## `mono:6.8-slim`

```console
$ docker pull mono@sha256:a8409dff6597f2ef5f7ecd3c672671bb2af9a390073efd74f95c54aa41cba22a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:

## `mono:6-slim`

```console
$ docker pull mono@sha256:dcd8a1b2f83384f688f944067becc698beb04988f213a0bfee2d785977e15bbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:6-slim` - linux; amd64

```console
$ docker pull mono@sha256:dbf079afc972cbf36017055c5dfa8b63e8495e68ed7a12782ff4e3b632100af0
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.7 MB (85743023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c13361f8aea3337ed6ca565868d63ed73db5104f6c26dfa91ce41d1ce1e5082`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:47 GMT
ADD file:90a2c81769a336bed3f731f44a385f2a65b0916f517a0b77c06c224579bf9a9a in / 
# Sat, 28 Dec 2019 04:23:47 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 13:14:15 GMT
ENV MONO_VERSION=6.6.0.161
# Sat, 28 Dec 2019 13:14:25 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 13:15:04 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:804555ee037604c40de144f9f8da0d826d38db82f15d74cded32790fe279a8f6`  
		Last Modified: Sat, 28 Dec 2019 04:28:38 GMT  
		Size: 22.5 MB (22524609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01e78f3e714bb9645ac8b6e172f033253467b1312e6dd4889da24aeee207e091`  
		Last Modified: Sat, 28 Dec 2019 13:48:14 GMT  
		Size: 244.5 KB (244485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b64c5ff00a44477231f8da775a76ef1611f6e7879ef3116862f0e13f16e5575f`  
		Last Modified: Sat, 28 Dec 2019 13:48:30 GMT  
		Size: 63.0 MB (62973929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:263841647b1413f97ede49244a3250c2bd9224534cfda1f58a4cef015523f95e
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46863874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f24cceab2b02f7699b97ad45390d24175d4f6cbc35951f14304e31bb40284717`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:53:16 GMT
ADD file:7d6af454b55cb354e31c096e935358dd5914688ded04ebc76243a4ff598c4495 in / 
# Sat, 28 Dec 2019 04:53:18 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 07:28:31 GMT
ENV MONO_VERSION=6.6.0.161
# Sat, 28 Dec 2019 07:28:56 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 07:29:51 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:af28f499fd964f4506ea46c2ac342bc52328a8c30cd633661b69f383a5144e9b`  
		Last Modified: Sat, 28 Dec 2019 05:00:23 GMT  
		Size: 21.2 MB (21202822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f759ae685ca874cea702ae1f63627810d814a2cae6a44c704003176e0c8b37c`  
		Last Modified: Sat, 28 Dec 2019 07:44:23 GMT  
		Size: 244.6 KB (244552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:720fbe46ab0c5e8c2e3e9ed44413d9fde2ad1d45d9161dd0c6a021855acc1b78`  
		Last Modified: Sat, 28 Dec 2019 07:44:33 GMT  
		Size: 25.4 MB (25416500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:70f8a6f90eedb2b040cdfe84d228b3b26f0549a32b275183a056543a822ebc44
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44204341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f0d6480804e64f949cbbdd9cc9ba45c6e077cd0266e5641b4822ce6ac3e6663`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 05:03:51 GMT
ADD file:2002ba672e32ae75369830ed6a4734ce62e0118e42390b4d657f0985d6b7fd6a in / 
# Sat, 28 Dec 2019 05:03:53 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 07:37:00 GMT
ENV MONO_VERSION=6.6.0.161
# Sat, 28 Dec 2019 07:37:19 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 07:38:02 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:77cf262539006c8df77496f500f74a8c1edd158062440fd94d43d5b1292cefee`  
		Last Modified: Sat, 28 Dec 2019 05:11:13 GMT  
		Size: 19.3 MB (19311587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63ea3a0398ee0834c6b8b5a98490a2451261135d85bbd06845c7077aff2a4667`  
		Last Modified: Sat, 28 Dec 2019 07:50:49 GMT  
		Size: 244.5 KB (244525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f543438b2494429fd7ef0a5cbe2145241dfa4aa2f1008038a251526056612dc`  
		Last Modified: Sat, 28 Dec 2019 07:50:58 GMT  
		Size: 24.6 MB (24648229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:0bd2ad5bfc5c4cddadd84d69dbf002b1e0669df16b5f6d1cf7051c6a3802d260
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50064013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b627d7b684f3642760e6c76a7e5a63fbe1006453301de18a9166f7ec9b9071f`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:43:36 GMT
ADD file:ba40f5080cbd89c576c350bfe5acfe16f2ec59636fdb082efc3a8cef66ae7cb7 in / 
# Sat, 28 Dec 2019 04:43:39 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 08:39:40 GMT
ENV MONO_VERSION=6.6.0.161
# Sat, 28 Dec 2019 08:39:58 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 08:40:48 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:588374d57fdb5120d024340eef3d8927af23a5b806d41b4f049ee430a153c0b4`  
		Last Modified: Sat, 28 Dec 2019 04:49:14 GMT  
		Size: 20.4 MB (20385801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:506cd7f059eaff3f2d682d7b6fccc5ab35050a7391a08c2d2624abd71e7c684c`  
		Last Modified: Sat, 28 Dec 2019 08:51:58 GMT  
		Size: 244.4 KB (244395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88f2783a0e4238e577522ec7c6a6b32cd37f547c4168c768fd5fcbfaa92b6de5`  
		Last Modified: Sat, 28 Dec 2019 08:52:09 GMT  
		Size: 29.4 MB (29433817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6-slim` - linux; 386

```console
$ docker pull mono@sha256:1470434632f62ac60985681302e025a1a93fb7c696224fa2f5fbafb8f168bf7e
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.1 MB (90146392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6872c3284610e489106962651891765f6a5b3a1418c06cda514d1db86209162e`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:42:05 GMT
ADD file:d43798bcf0e72b342c261b8585dde072d9363d19fab4b8d9f08f15db189f287b in / 
# Sat, 28 Dec 2019 04:42:05 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 08:53:34 GMT
ENV MONO_VERSION=6.6.0.161
# Sat, 28 Dec 2019 08:53:44 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 08:54:22 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:2cb401c016d2f9802d5ef9cf6c6dc07251e9f87757a0de0a8df318fb7f00385c`  
		Last Modified: Sat, 28 Dec 2019 04:47:36 GMT  
		Size: 23.2 MB (23152142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f6b4fc901f01e72498a390f3e82b1885f694d21c0c86b2c5b722170744653ee`  
		Last Modified: Sat, 28 Dec 2019 09:03:51 GMT  
		Size: 244.5 KB (244481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ef8b692587284955aed9af38c783ccb1813e5f21a78f50075e3a462a575820e`  
		Last Modified: Sat, 28 Dec 2019 09:04:10 GMT  
		Size: 66.7 MB (66749769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:a7840aa6d9953b14f7d37472ed11dc4785cff7c5edbf16718bfc36a6d9cf58b6
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48874163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ea84dffac95f8be085f5eeb79990afa1341135da9867d71688f2d9a3b61bfbf`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:21 GMT
ADD file:a1ee5955ff3ede8df9558f4bec0c7962d54c43374f857e1da7e2639ddf82a9f1 in / 
# Sat, 28 Dec 2019 04:23:24 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 06:00:10 GMT
ENV MONO_VERSION=6.6.0.161
# Sat, 28 Dec 2019 06:01:14 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 06:02:17 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:af52e7ef6e83efadeae17be91daa6ecf61b7dfb39709c29be9b24876e60c0e36`  
		Last Modified: Sat, 28 Dec 2019 04:33:19 GMT  
		Size: 22.8 MB (22800791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:367bf0f7a48952d80f9489622c9b118004dd0fd4763a1fd6153d9b12a571b1ee`  
		Last Modified: Sat, 28 Dec 2019 06:22:04 GMT  
		Size: 244.5 KB (244543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bf3902985b2f759ba0edff57a78d4eb7e81f59e8327b7d243b8f3b4b8ca7c79`  
		Last Modified: Sat, 28 Dec 2019 06:22:14 GMT  
		Size: 25.8 MB (25828829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:latest`

```console
$ docker pull mono@sha256:cb8035058b1a14a610fe7a43bc3b3b77ebf97b24313c15a8f414e748f02a7dbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:latest` - linux; amd64

```console
$ docker pull mono@sha256:3f3ad551a8789a79e3b59c836a659dc748626b0c18543cc9d32ecc1f3d01ee32
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233195367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13ed216b8ba57507781ef13d31102febe0415d37333dd05d96e05f92ad9e9ca3`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:47 GMT
ADD file:90a2c81769a336bed3f731f44a385f2a65b0916f517a0b77c06c224579bf9a9a in / 
# Sat, 28 Dec 2019 04:23:47 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 13:14:15 GMT
ENV MONO_VERSION=6.6.0.161
# Sat, 28 Dec 2019 13:14:25 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 13:15:04 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 28 Dec 2019 13:27:55 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:804555ee037604c40de144f9f8da0d826d38db82f15d74cded32790fe279a8f6`  
		Last Modified: Sat, 28 Dec 2019 04:28:38 GMT  
		Size: 22.5 MB (22524609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01e78f3e714bb9645ac8b6e172f033253467b1312e6dd4889da24aeee207e091`  
		Last Modified: Sat, 28 Dec 2019 13:48:14 GMT  
		Size: 244.5 KB (244485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b64c5ff00a44477231f8da775a76ef1611f6e7879ef3116862f0e13f16e5575f`  
		Last Modified: Sat, 28 Dec 2019 13:48:30 GMT  
		Size: 63.0 MB (62973929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9e6e2e990789fcd233754f316f68b3dcf7fcc8affcb267f1770e6abecd0a4df`  
		Last Modified: Sat, 28 Dec 2019 13:49:41 GMT  
		Size: 147.5 MB (147452344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:latest` - linux; arm variant v5

```console
$ docker pull mono@sha256:71075f43a6acd5d4900e8b4050bc87b552302d7b550e2d9da1a55aa37eb95852
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.7 MB (176653531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41594e91a86b24e549ebe9f4c951e2403e6e22200d648d599d853dbc7ebe37a5`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:53:16 GMT
ADD file:7d6af454b55cb354e31c096e935358dd5914688ded04ebc76243a4ff598c4495 in / 
# Sat, 28 Dec 2019 04:53:18 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 07:28:31 GMT
ENV MONO_VERSION=6.6.0.161
# Sat, 28 Dec 2019 07:28:56 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 07:29:51 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 28 Dec 2019 07:37:00 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:af28f499fd964f4506ea46c2ac342bc52328a8c30cd633661b69f383a5144e9b`  
		Last Modified: Sat, 28 Dec 2019 05:00:23 GMT  
		Size: 21.2 MB (21202822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f759ae685ca874cea702ae1f63627810d814a2cae6a44c704003176e0c8b37c`  
		Last Modified: Sat, 28 Dec 2019 07:44:23 GMT  
		Size: 244.6 KB (244552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:720fbe46ab0c5e8c2e3e9ed44413d9fde2ad1d45d9161dd0c6a021855acc1b78`  
		Last Modified: Sat, 28 Dec 2019 07:44:33 GMT  
		Size: 25.4 MB (25416500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:906dd0e12894eb03a4ab34eacdf91d163dfd6c09d61c9005e666875d42c1b91b`  
		Last Modified: Sat, 28 Dec 2019 07:46:06 GMT  
		Size: 129.8 MB (129789657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:latest` - linux; arm variant v7

```console
$ docker pull mono@sha256:7e7ebdba687fb7bac2a796eb557210fe8f5fa55c86cfa342bd56d213a27dcaf3
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.7 MB (172655347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c77176fb08c03220255179938d178739f8882569f72ecaae83ba7b5fc620aef`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 05:03:51 GMT
ADD file:2002ba672e32ae75369830ed6a4734ce62e0118e42390b4d657f0985d6b7fd6a in / 
# Sat, 28 Dec 2019 05:03:53 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 07:37:00 GMT
ENV MONO_VERSION=6.6.0.161
# Sat, 28 Dec 2019 07:37:19 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 07:38:02 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 28 Dec 2019 07:44:03 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:77cf262539006c8df77496f500f74a8c1edd158062440fd94d43d5b1292cefee`  
		Last Modified: Sat, 28 Dec 2019 05:11:13 GMT  
		Size: 19.3 MB (19311587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63ea3a0398ee0834c6b8b5a98490a2451261135d85bbd06845c7077aff2a4667`  
		Last Modified: Sat, 28 Dec 2019 07:50:49 GMT  
		Size: 244.5 KB (244525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f543438b2494429fd7ef0a5cbe2145241dfa4aa2f1008038a251526056612dc`  
		Last Modified: Sat, 28 Dec 2019 07:50:58 GMT  
		Size: 24.6 MB (24648229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:184b3a33ac95fb2ba207e6fc82f4e7fac1dc71bad49531f182c2a7046b54bd39`  
		Last Modified: Sat, 28 Dec 2019 07:52:21 GMT  
		Size: 128.5 MB (128451006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:latest` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:8aed237906aca013f801430a60e500a1ad6f159c804e14bf4869e9abfcabb89d
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.5 MB (194537478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45a4c03521b1b035e910a91ec512dae28e62411186750460178c6daa0e9809af`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:43:36 GMT
ADD file:ba40f5080cbd89c576c350bfe5acfe16f2ec59636fdb082efc3a8cef66ae7cb7 in / 
# Sat, 28 Dec 2019 04:43:39 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 08:39:40 GMT
ENV MONO_VERSION=6.6.0.161
# Sat, 28 Dec 2019 08:39:58 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 08:40:48 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 28 Dec 2019 08:45:43 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:588374d57fdb5120d024340eef3d8927af23a5b806d41b4f049ee430a153c0b4`  
		Last Modified: Sat, 28 Dec 2019 04:49:14 GMT  
		Size: 20.4 MB (20385801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:506cd7f059eaff3f2d682d7b6fccc5ab35050a7391a08c2d2624abd71e7c684c`  
		Last Modified: Sat, 28 Dec 2019 08:51:58 GMT  
		Size: 244.4 KB (244395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88f2783a0e4238e577522ec7c6a6b32cd37f547c4168c768fd5fcbfaa92b6de5`  
		Last Modified: Sat, 28 Dec 2019 08:52:09 GMT  
		Size: 29.4 MB (29433817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb6f35beab9dd7284dbe38b9cf839f586f175ad37c1dcb2833bfdcdbf03a4539`  
		Last Modified: Sat, 28 Dec 2019 08:53:38 GMT  
		Size: 144.5 MB (144473465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:latest` - linux; 386

```console
$ docker pull mono@sha256:113663c398fb93fe981888f95186bb46d53ceb70ec40b9dd5d2062147bcf30cb
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.4 MB (241440865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67c3139144abd4f519d829e1787e239be574822453c53467c29462efab37ff42`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:42:05 GMT
ADD file:d43798bcf0e72b342c261b8585dde072d9363d19fab4b8d9f08f15db189f287b in / 
# Sat, 28 Dec 2019 04:42:05 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 08:53:34 GMT
ENV MONO_VERSION=6.6.0.161
# Sat, 28 Dec 2019 08:53:44 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 08:54:22 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 28 Dec 2019 08:58:35 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:2cb401c016d2f9802d5ef9cf6c6dc07251e9f87757a0de0a8df318fb7f00385c`  
		Last Modified: Sat, 28 Dec 2019 04:47:36 GMT  
		Size: 23.2 MB (23152142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f6b4fc901f01e72498a390f3e82b1885f694d21c0c86b2c5b722170744653ee`  
		Last Modified: Sat, 28 Dec 2019 09:03:51 GMT  
		Size: 244.5 KB (244481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ef8b692587284955aed9af38c783ccb1813e5f21a78f50075e3a462a575820e`  
		Last Modified: Sat, 28 Dec 2019 09:04:10 GMT  
		Size: 66.7 MB (66749769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e126a79dc65a7868221d13b2fe454087df416e1ea28ef3fb313d2abba6692268`  
		Last Modified: Sat, 28 Dec 2019 09:05:37 GMT  
		Size: 151.3 MB (151294473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:latest` - linux; ppc64le

```console
$ docker pull mono@sha256:8be78d5e96a5e63f2d4754a3686943f1d8edfd75c46a313cd27984c010e27c52
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.9 MB (178943769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c75d8bc1699ea912f280f4dcb86edababad529239b8eeb28e3801bcd9a015066`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:21 GMT
ADD file:a1ee5955ff3ede8df9558f4bec0c7962d54c43374f857e1da7e2639ddf82a9f1 in / 
# Sat, 28 Dec 2019 04:23:24 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 06:00:10 GMT
ENV MONO_VERSION=6.6.0.161
# Sat, 28 Dec 2019 06:01:14 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 06:02:17 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 28 Dec 2019 06:11:01 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:af52e7ef6e83efadeae17be91daa6ecf61b7dfb39709c29be9b24876e60c0e36`  
		Last Modified: Sat, 28 Dec 2019 04:33:19 GMT  
		Size: 22.8 MB (22800791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:367bf0f7a48952d80f9489622c9b118004dd0fd4763a1fd6153d9b12a571b1ee`  
		Last Modified: Sat, 28 Dec 2019 06:22:04 GMT  
		Size: 244.5 KB (244543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bf3902985b2f759ba0edff57a78d4eb7e81f59e8327b7d243b8f3b4b8ca7c79`  
		Last Modified: Sat, 28 Dec 2019 06:22:14 GMT  
		Size: 25.8 MB (25828829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b12c28397b6cede6691c7e5447b466791fb395f4ecb3d1fb78e68dc1ffe4eb9`  
		Last Modified: Sat, 28 Dec 2019 06:24:05 GMT  
		Size: 130.1 MB (130069606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:slim`

```console
$ docker pull mono@sha256:dcd8a1b2f83384f688f944067becc698beb04988f213a0bfee2d785977e15bbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:slim` - linux; amd64

```console
$ docker pull mono@sha256:dbf079afc972cbf36017055c5dfa8b63e8495e68ed7a12782ff4e3b632100af0
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.7 MB (85743023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c13361f8aea3337ed6ca565868d63ed73db5104f6c26dfa91ce41d1ce1e5082`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:47 GMT
ADD file:90a2c81769a336bed3f731f44a385f2a65b0916f517a0b77c06c224579bf9a9a in / 
# Sat, 28 Dec 2019 04:23:47 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 13:14:15 GMT
ENV MONO_VERSION=6.6.0.161
# Sat, 28 Dec 2019 13:14:25 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 13:15:04 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:804555ee037604c40de144f9f8da0d826d38db82f15d74cded32790fe279a8f6`  
		Last Modified: Sat, 28 Dec 2019 04:28:38 GMT  
		Size: 22.5 MB (22524609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01e78f3e714bb9645ac8b6e172f033253467b1312e6dd4889da24aeee207e091`  
		Last Modified: Sat, 28 Dec 2019 13:48:14 GMT  
		Size: 244.5 KB (244485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b64c5ff00a44477231f8da775a76ef1611f6e7879ef3116862f0e13f16e5575f`  
		Last Modified: Sat, 28 Dec 2019 13:48:30 GMT  
		Size: 63.0 MB (62973929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:263841647b1413f97ede49244a3250c2bd9224534cfda1f58a4cef015523f95e
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46863874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f24cceab2b02f7699b97ad45390d24175d4f6cbc35951f14304e31bb40284717`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:53:16 GMT
ADD file:7d6af454b55cb354e31c096e935358dd5914688ded04ebc76243a4ff598c4495 in / 
# Sat, 28 Dec 2019 04:53:18 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 07:28:31 GMT
ENV MONO_VERSION=6.6.0.161
# Sat, 28 Dec 2019 07:28:56 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 07:29:51 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:af28f499fd964f4506ea46c2ac342bc52328a8c30cd633661b69f383a5144e9b`  
		Last Modified: Sat, 28 Dec 2019 05:00:23 GMT  
		Size: 21.2 MB (21202822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f759ae685ca874cea702ae1f63627810d814a2cae6a44c704003176e0c8b37c`  
		Last Modified: Sat, 28 Dec 2019 07:44:23 GMT  
		Size: 244.6 KB (244552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:720fbe46ab0c5e8c2e3e9ed44413d9fde2ad1d45d9161dd0c6a021855acc1b78`  
		Last Modified: Sat, 28 Dec 2019 07:44:33 GMT  
		Size: 25.4 MB (25416500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:70f8a6f90eedb2b040cdfe84d228b3b26f0549a32b275183a056543a822ebc44
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44204341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f0d6480804e64f949cbbdd9cc9ba45c6e077cd0266e5641b4822ce6ac3e6663`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 05:03:51 GMT
ADD file:2002ba672e32ae75369830ed6a4734ce62e0118e42390b4d657f0985d6b7fd6a in / 
# Sat, 28 Dec 2019 05:03:53 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 07:37:00 GMT
ENV MONO_VERSION=6.6.0.161
# Sat, 28 Dec 2019 07:37:19 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 07:38:02 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:77cf262539006c8df77496f500f74a8c1edd158062440fd94d43d5b1292cefee`  
		Last Modified: Sat, 28 Dec 2019 05:11:13 GMT  
		Size: 19.3 MB (19311587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63ea3a0398ee0834c6b8b5a98490a2451261135d85bbd06845c7077aff2a4667`  
		Last Modified: Sat, 28 Dec 2019 07:50:49 GMT  
		Size: 244.5 KB (244525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f543438b2494429fd7ef0a5cbe2145241dfa4aa2f1008038a251526056612dc`  
		Last Modified: Sat, 28 Dec 2019 07:50:58 GMT  
		Size: 24.6 MB (24648229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:0bd2ad5bfc5c4cddadd84d69dbf002b1e0669df16b5f6d1cf7051c6a3802d260
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50064013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b627d7b684f3642760e6c76a7e5a63fbe1006453301de18a9166f7ec9b9071f`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:43:36 GMT
ADD file:ba40f5080cbd89c576c350bfe5acfe16f2ec59636fdb082efc3a8cef66ae7cb7 in / 
# Sat, 28 Dec 2019 04:43:39 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 08:39:40 GMT
ENV MONO_VERSION=6.6.0.161
# Sat, 28 Dec 2019 08:39:58 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 08:40:48 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:588374d57fdb5120d024340eef3d8927af23a5b806d41b4f049ee430a153c0b4`  
		Last Modified: Sat, 28 Dec 2019 04:49:14 GMT  
		Size: 20.4 MB (20385801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:506cd7f059eaff3f2d682d7b6fccc5ab35050a7391a08c2d2624abd71e7c684c`  
		Last Modified: Sat, 28 Dec 2019 08:51:58 GMT  
		Size: 244.4 KB (244395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88f2783a0e4238e577522ec7c6a6b32cd37f547c4168c768fd5fcbfaa92b6de5`  
		Last Modified: Sat, 28 Dec 2019 08:52:09 GMT  
		Size: 29.4 MB (29433817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:slim` - linux; 386

```console
$ docker pull mono@sha256:1470434632f62ac60985681302e025a1a93fb7c696224fa2f5fbafb8f168bf7e
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.1 MB (90146392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6872c3284610e489106962651891765f6a5b3a1418c06cda514d1db86209162e`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:42:05 GMT
ADD file:d43798bcf0e72b342c261b8585dde072d9363d19fab4b8d9f08f15db189f287b in / 
# Sat, 28 Dec 2019 04:42:05 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 08:53:34 GMT
ENV MONO_VERSION=6.6.0.161
# Sat, 28 Dec 2019 08:53:44 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 08:54:22 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:2cb401c016d2f9802d5ef9cf6c6dc07251e9f87757a0de0a8df318fb7f00385c`  
		Last Modified: Sat, 28 Dec 2019 04:47:36 GMT  
		Size: 23.2 MB (23152142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f6b4fc901f01e72498a390f3e82b1885f694d21c0c86b2c5b722170744653ee`  
		Last Modified: Sat, 28 Dec 2019 09:03:51 GMT  
		Size: 244.5 KB (244481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ef8b692587284955aed9af38c783ccb1813e5f21a78f50075e3a462a575820e`  
		Last Modified: Sat, 28 Dec 2019 09:04:10 GMT  
		Size: 66.7 MB (66749769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:slim` - linux; ppc64le

```console
$ docker pull mono@sha256:a7840aa6d9953b14f7d37472ed11dc4785cff7c5edbf16718bfc36a6d9cf58b6
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48874163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ea84dffac95f8be085f5eeb79990afa1341135da9867d71688f2d9a3b61bfbf`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:21 GMT
ADD file:a1ee5955ff3ede8df9558f4bec0c7962d54c43374f857e1da7e2639ddf82a9f1 in / 
# Sat, 28 Dec 2019 04:23:24 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 06:00:10 GMT
ENV MONO_VERSION=6.6.0.161
# Sat, 28 Dec 2019 06:01:14 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 06:02:17 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:af52e7ef6e83efadeae17be91daa6ecf61b7dfb39709c29be9b24876e60c0e36`  
		Last Modified: Sat, 28 Dec 2019 04:33:19 GMT  
		Size: 22.8 MB (22800791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:367bf0f7a48952d80f9489622c9b118004dd0fd4763a1fd6153d9b12a571b1ee`  
		Last Modified: Sat, 28 Dec 2019 06:22:04 GMT  
		Size: 244.5 KB (244543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bf3902985b2f759ba0edff57a78d4eb7e81f59e8327b7d243b8f3b4b8ca7c79`  
		Last Modified: Sat, 28 Dec 2019 06:22:14 GMT  
		Size: 25.8 MB (25828829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
