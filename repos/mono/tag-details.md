<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `mono`

-	[`mono:6`](#mono6)
-	[`mono:6.10`](#mono610)
-	[`mono:6.10.0`](#mono6100)
-	[`mono:6.10.0.104`](#mono6100104)
-	[`mono:6.10.0.104-slim`](#mono6100104-slim)
-	[`mono:6.10.0-slim`](#mono6100-slim)
-	[`mono:6.10-slim`](#mono610-slim)
-	[`mono:6.8`](#mono68)
-	[`mono:6.8.0`](#mono680)
-	[`mono:6.8.0.123`](#mono680123)
-	[`mono:6.8.0.123-slim`](#mono680123-slim)
-	[`mono:6.8.0-slim`](#mono680-slim)
-	[`mono:6.8-slim`](#mono68-slim)
-	[`mono:6-slim`](#mono6-slim)
-	[`mono:latest`](#monolatest)
-	[`mono:slim`](#monoslim)

## `mono:6`

```console
$ docker pull mono@sha256:51c78c2462224a085af0bc077f69420ee58ded25392f96b396fc84999767b360
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
$ docker pull mono@sha256:8ddb0aa61e691c3e02dc60e6d9d37d48c9adbdcf96690d4e3b0e1f157d864f0c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.7 MB (224730258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e643114dd794dcb7b32b4cebb995622e6404e198c2698b435be26a772765604`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 10 Sep 2020 00:23:29 GMT
ADD file:e7407f2294ad23634565820b9669b18ff2a2ca0212a7ec84b9c89d8550859954 in / 
# Thu, 10 Sep 2020 00:23:30 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 06:19:25 GMT
ENV MONO_VERSION=6.10.0.104
# Thu, 10 Sep 2020 06:19:35 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 10 Sep 2020 06:20:13 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 10 Sep 2020 06:38:36 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:d121f8d1c4128ebc1e95e5bfad90a0189b84eadbbb2fbaad20cbb26d20b2c8a2`  
		Last Modified: Thu, 10 Sep 2020 00:34:02 GMT  
		Size: 27.1 MB (27092161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:140dba57f56b96691dfd0551d17470bb5f21984005c4c372509a3cc39d8618ff`  
		Last Modified: Thu, 10 Sep 2020 06:39:36 GMT  
		Size: 255.9 KB (255922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad432be9d8d43b429c26f097fa65f3e8ce3af20bd0cff99c69f5ae3ba83d421b`  
		Last Modified: Thu, 10 Sep 2020 06:39:51 GMT  
		Size: 67.1 MB (67092172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:647a8876e15683db1ea6901f3102f72d4b0cd4a6f92f4321d25cdd9410e6acf0`  
		Last Modified: Thu, 10 Sep 2020 06:41:41 GMT  
		Size: 130.3 MB (130290003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6` - linux; arm variant v5

```console
$ docker pull mono@sha256:3e601afbb4577fd538dfa06145643ef0c370d3b98b7fdbdeb8e69e6e7c3cc44b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.6 MB (180580641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0b1583a0f54587294ef3fb13293551714e84d35168baa3b742491aac91dc394`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Oct 2020 01:52:17 GMT
ADD file:b71c0fa4957d6b65af37231a105f3d17cdbafe5c7d6c37b5843ebf619c608aaa in / 
# Tue, 13 Oct 2020 01:52:27 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 02:36:19 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 13 Oct 2020 02:36:43 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 13 Oct 2020 02:37:31 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 13 Oct 2020 02:44:00 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:f991c1e1ee2c48f16625b6b61310bf3c0616c0dbda4762019117e86fd29cf9ce`  
		Last Modified: Tue, 13 Oct 2020 02:01:27 GMT  
		Size: 24.8 MB (24835992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d27e131b9898d8f02267f410169b8627b889f6585ad9300d14a4775194301b55`  
		Last Modified: Tue, 13 Oct 2020 02:44:49 GMT  
		Size: 255.9 KB (255938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07b82cc14a51474e2d05a0fd59b3fde70aa8fda539de5a302992983e4ffce7b8`  
		Last Modified: Tue, 13 Oct 2020 02:45:01 GMT  
		Size: 26.5 MB (26530650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f94ad0d9899e6c5c16486a97103eb9bbff1261c084ef2366534ae27653b23704`  
		Last Modified: Tue, 13 Oct 2020 02:46:59 GMT  
		Size: 129.0 MB (128958061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6` - linux; arm variant v7

```console
$ docker pull mono@sha256:0e797969122f94b85e9178dd9bece13c7ebd2cacf124520f4275e0ac7cd2b15d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.5 MB (176483530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b81a3bb43255d115e920754f87906a5cd00c5c5ae23a85f06c756f2c42a455b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Oct 2020 00:59:29 GMT
ADD file:e423f30ca19eb205a98de21b0545d0a764cfc4f832a9a9631542354d914d98d9 in / 
# Tue, 13 Oct 2020 00:59:31 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 04:43:09 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 13 Oct 2020 04:43:27 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 13 Oct 2020 04:44:11 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 13 Oct 2020 04:49:53 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:d6d8411ad43db0022fa0fce094cd2e8b1dd2f8a09d6880ed9beb6b4204867027`  
		Last Modified: Tue, 13 Oct 2020 01:08:28 GMT  
		Size: 22.7 MB (22699849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5228b93feed3135603bc1b4bbda140b6e3e712167c9dd5ccaad1732370cd6b93`  
		Last Modified: Tue, 13 Oct 2020 04:50:37 GMT  
		Size: 255.9 KB (255921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4e85494910fa31cd3bb70be77361cab8fa0b333de462a10ce0e2181ee165c0a`  
		Last Modified: Tue, 13 Oct 2020 04:50:46 GMT  
		Size: 25.7 MB (25729327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c0179ccf237338944b3401bc8ed480a53bd10956472cd41d05647aeb7fa46ee`  
		Last Modified: Tue, 13 Oct 2020 04:52:43 GMT  
		Size: 127.8 MB (127798433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:aed137508847cbf4f9a780482c89ec7185a4925bb21c49455867253f783b3756
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.3 MB (203294488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:932c2fe803dcfd13acda14b21319c3cc542c19c177c473ab3a72d42ec87c407a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 09 Sep 2020 23:50:54 GMT
ADD file:d870fb0484ea283840d9cc923c9c3fe36d1bb6b3b5ecfefcce06aa26a22c9414 in / 
# Wed, 09 Sep 2020 23:50:57 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 04:11:35 GMT
ENV MONO_VERSION=6.10.0.104
# Thu, 10 Sep 2020 04:11:50 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 10 Sep 2020 04:12:25 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 10 Sep 2020 04:17:44 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a6d76de28f58f3470aff71c934c0fec4e5d0fad788f8b8bcc50601266fc1b34d`  
		Last Modified: Wed, 09 Sep 2020 23:59:09 GMT  
		Size: 25.8 MB (25849325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e6286cef3ccb7f414187d0d407d414d80aefc9cbac5f8afc8b61c2144468e9d`  
		Last Modified: Thu, 10 Sep 2020 04:18:37 GMT  
		Size: 255.9 KB (255919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2922d176e5f282d1cab4d82a18705798bb201e72254252e9365c6e6d79f9193`  
		Last Modified: Thu, 10 Sep 2020 04:18:47 GMT  
		Size: 31.8 MB (31750168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:516e789eeddd8a9df62f3440c69b597818ad508f4cef3e636f2c25150e64e036`  
		Last Modified: Thu, 10 Sep 2020 04:20:35 GMT  
		Size: 145.4 MB (145439076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6` - linux; 386

```console
$ docker pull mono@sha256:d111852f67f667bb664ca166bcaf57863be573e5f9abcf640261a13ce768af9f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.5 MB (230534575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c670b9156ca83df138822e88a059b2ef4b85870178733601534fdb68cc075916`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 09 Sep 2020 23:40:19 GMT
ADD file:08dc20c9cd727ebf02cac6e4b287c3009274682174aee9222494491cd6c671b8 in / 
# Wed, 09 Sep 2020 23:40:19 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 02:37:15 GMT
ENV MONO_VERSION=6.10.0.104
# Thu, 10 Sep 2020 02:37:27 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 10 Sep 2020 02:38:12 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 10 Sep 2020 02:43:19 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:31e6582dbd9f9a84903d46339df0c393a63d2cbfb001b06b3204653cceafcc61`  
		Last Modified: Wed, 09 Sep 2020 23:46:30 GMT  
		Size: 27.8 MB (27750334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10a5b4050174b76ed23d2d3bbb436d66899f93eba56641cd1faf810f75242c67`  
		Last Modified: Thu, 10 Sep 2020 02:44:13 GMT  
		Size: 255.8 KB (255795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a251d8984c7c93892d00e6d7ad246f6eb96eb1ccef85f2aa4931d99e3fa536d0`  
		Last Modified: Thu, 10 Sep 2020 02:44:42 GMT  
		Size: 71.1 MB (71136267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:977fb5b989bb54968bfa64f742226d8805f4ec1552243874881f524b81fb29ae`  
		Last Modified: Thu, 10 Sep 2020 02:46:21 GMT  
		Size: 131.4 MB (131392179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6` - linux; ppc64le

```console
$ docker pull mono@sha256:b8c551764ab121348d5a5b162b12f0b2a502a49198c74891cdd0c24e8cb6edb1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.1 MB (192085402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:986fc10b226d2b7a4e6847eb4e4451f452b95bad5fb31f38f99795e2fae34446`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 10 Sep 2020 01:06:11 GMT
ADD file:4dede556abae88027bd22f3166fdbc38778a6fcd686c5ce768c3ca024ab3f9cf in / 
# Thu, 10 Sep 2020 01:06:20 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 19:01:16 GMT
ENV MONO_VERSION=6.10.0.104
# Thu, 10 Sep 2020 19:05:10 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 10 Sep 2020 19:07:24 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 10 Sep 2020 19:41:11 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:f8aef3d2247e5f990bc767bc99f575b9bcec34aaa37183414eebe28fcd09519d`  
		Last Modified: Thu, 10 Sep 2020 01:28:12 GMT  
		Size: 30.5 MB (30517880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91a5b381ce455eca298e810bbcff286cc9167c82392b00241d01cc6bc65cfe86`  
		Last Modified: Thu, 10 Sep 2020 19:42:19 GMT  
		Size: 256.3 KB (256260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3df1215b828b18d641c32013a7c8597874acf4085e9fc7b404d9216a5e67ecc3`  
		Last Modified: Thu, 10 Sep 2020 19:42:28 GMT  
		Size: 29.4 MB (29350071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96ac3143de444eb2aa16dc11160d058e94b7f635cfc9b210a3438a1535c643b1`  
		Last Modified: Thu, 10 Sep 2020 19:44:16 GMT  
		Size: 132.0 MB (131961191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.10`

```console
$ docker pull mono@sha256:51c78c2462224a085af0bc077f69420ee58ded25392f96b396fc84999767b360
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:6.10` - linux; amd64

```console
$ docker pull mono@sha256:8ddb0aa61e691c3e02dc60e6d9d37d48c9adbdcf96690d4e3b0e1f157d864f0c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.7 MB (224730258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e643114dd794dcb7b32b4cebb995622e6404e198c2698b435be26a772765604`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 10 Sep 2020 00:23:29 GMT
ADD file:e7407f2294ad23634565820b9669b18ff2a2ca0212a7ec84b9c89d8550859954 in / 
# Thu, 10 Sep 2020 00:23:30 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 06:19:25 GMT
ENV MONO_VERSION=6.10.0.104
# Thu, 10 Sep 2020 06:19:35 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 10 Sep 2020 06:20:13 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 10 Sep 2020 06:38:36 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:d121f8d1c4128ebc1e95e5bfad90a0189b84eadbbb2fbaad20cbb26d20b2c8a2`  
		Last Modified: Thu, 10 Sep 2020 00:34:02 GMT  
		Size: 27.1 MB (27092161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:140dba57f56b96691dfd0551d17470bb5f21984005c4c372509a3cc39d8618ff`  
		Last Modified: Thu, 10 Sep 2020 06:39:36 GMT  
		Size: 255.9 KB (255922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad432be9d8d43b429c26f097fa65f3e8ce3af20bd0cff99c69f5ae3ba83d421b`  
		Last Modified: Thu, 10 Sep 2020 06:39:51 GMT  
		Size: 67.1 MB (67092172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:647a8876e15683db1ea6901f3102f72d4b0cd4a6f92f4321d25cdd9410e6acf0`  
		Last Modified: Thu, 10 Sep 2020 06:41:41 GMT  
		Size: 130.3 MB (130290003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10` - linux; arm variant v5

```console
$ docker pull mono@sha256:3e601afbb4577fd538dfa06145643ef0c370d3b98b7fdbdeb8e69e6e7c3cc44b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.6 MB (180580641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0b1583a0f54587294ef3fb13293551714e84d35168baa3b742491aac91dc394`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Oct 2020 01:52:17 GMT
ADD file:b71c0fa4957d6b65af37231a105f3d17cdbafe5c7d6c37b5843ebf619c608aaa in / 
# Tue, 13 Oct 2020 01:52:27 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 02:36:19 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 13 Oct 2020 02:36:43 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 13 Oct 2020 02:37:31 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 13 Oct 2020 02:44:00 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:f991c1e1ee2c48f16625b6b61310bf3c0616c0dbda4762019117e86fd29cf9ce`  
		Last Modified: Tue, 13 Oct 2020 02:01:27 GMT  
		Size: 24.8 MB (24835992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d27e131b9898d8f02267f410169b8627b889f6585ad9300d14a4775194301b55`  
		Last Modified: Tue, 13 Oct 2020 02:44:49 GMT  
		Size: 255.9 KB (255938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07b82cc14a51474e2d05a0fd59b3fde70aa8fda539de5a302992983e4ffce7b8`  
		Last Modified: Tue, 13 Oct 2020 02:45:01 GMT  
		Size: 26.5 MB (26530650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f94ad0d9899e6c5c16486a97103eb9bbff1261c084ef2366534ae27653b23704`  
		Last Modified: Tue, 13 Oct 2020 02:46:59 GMT  
		Size: 129.0 MB (128958061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10` - linux; arm variant v7

```console
$ docker pull mono@sha256:0e797969122f94b85e9178dd9bece13c7ebd2cacf124520f4275e0ac7cd2b15d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.5 MB (176483530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b81a3bb43255d115e920754f87906a5cd00c5c5ae23a85f06c756f2c42a455b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Oct 2020 00:59:29 GMT
ADD file:e423f30ca19eb205a98de21b0545d0a764cfc4f832a9a9631542354d914d98d9 in / 
# Tue, 13 Oct 2020 00:59:31 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 04:43:09 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 13 Oct 2020 04:43:27 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 13 Oct 2020 04:44:11 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 13 Oct 2020 04:49:53 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:d6d8411ad43db0022fa0fce094cd2e8b1dd2f8a09d6880ed9beb6b4204867027`  
		Last Modified: Tue, 13 Oct 2020 01:08:28 GMT  
		Size: 22.7 MB (22699849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5228b93feed3135603bc1b4bbda140b6e3e712167c9dd5ccaad1732370cd6b93`  
		Last Modified: Tue, 13 Oct 2020 04:50:37 GMT  
		Size: 255.9 KB (255921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4e85494910fa31cd3bb70be77361cab8fa0b333de462a10ce0e2181ee165c0a`  
		Last Modified: Tue, 13 Oct 2020 04:50:46 GMT  
		Size: 25.7 MB (25729327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c0179ccf237338944b3401bc8ed480a53bd10956472cd41d05647aeb7fa46ee`  
		Last Modified: Tue, 13 Oct 2020 04:52:43 GMT  
		Size: 127.8 MB (127798433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:aed137508847cbf4f9a780482c89ec7185a4925bb21c49455867253f783b3756
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.3 MB (203294488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:932c2fe803dcfd13acda14b21319c3cc542c19c177c473ab3a72d42ec87c407a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 09 Sep 2020 23:50:54 GMT
ADD file:d870fb0484ea283840d9cc923c9c3fe36d1bb6b3b5ecfefcce06aa26a22c9414 in / 
# Wed, 09 Sep 2020 23:50:57 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 04:11:35 GMT
ENV MONO_VERSION=6.10.0.104
# Thu, 10 Sep 2020 04:11:50 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 10 Sep 2020 04:12:25 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 10 Sep 2020 04:17:44 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a6d76de28f58f3470aff71c934c0fec4e5d0fad788f8b8bcc50601266fc1b34d`  
		Last Modified: Wed, 09 Sep 2020 23:59:09 GMT  
		Size: 25.8 MB (25849325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e6286cef3ccb7f414187d0d407d414d80aefc9cbac5f8afc8b61c2144468e9d`  
		Last Modified: Thu, 10 Sep 2020 04:18:37 GMT  
		Size: 255.9 KB (255919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2922d176e5f282d1cab4d82a18705798bb201e72254252e9365c6e6d79f9193`  
		Last Modified: Thu, 10 Sep 2020 04:18:47 GMT  
		Size: 31.8 MB (31750168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:516e789eeddd8a9df62f3440c69b597818ad508f4cef3e636f2c25150e64e036`  
		Last Modified: Thu, 10 Sep 2020 04:20:35 GMT  
		Size: 145.4 MB (145439076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10` - linux; 386

```console
$ docker pull mono@sha256:d111852f67f667bb664ca166bcaf57863be573e5f9abcf640261a13ce768af9f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.5 MB (230534575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c670b9156ca83df138822e88a059b2ef4b85870178733601534fdb68cc075916`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 09 Sep 2020 23:40:19 GMT
ADD file:08dc20c9cd727ebf02cac6e4b287c3009274682174aee9222494491cd6c671b8 in / 
# Wed, 09 Sep 2020 23:40:19 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 02:37:15 GMT
ENV MONO_VERSION=6.10.0.104
# Thu, 10 Sep 2020 02:37:27 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 10 Sep 2020 02:38:12 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 10 Sep 2020 02:43:19 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:31e6582dbd9f9a84903d46339df0c393a63d2cbfb001b06b3204653cceafcc61`  
		Last Modified: Wed, 09 Sep 2020 23:46:30 GMT  
		Size: 27.8 MB (27750334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10a5b4050174b76ed23d2d3bbb436d66899f93eba56641cd1faf810f75242c67`  
		Last Modified: Thu, 10 Sep 2020 02:44:13 GMT  
		Size: 255.8 KB (255795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a251d8984c7c93892d00e6d7ad246f6eb96eb1ccef85f2aa4931d99e3fa536d0`  
		Last Modified: Thu, 10 Sep 2020 02:44:42 GMT  
		Size: 71.1 MB (71136267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:977fb5b989bb54968bfa64f742226d8805f4ec1552243874881f524b81fb29ae`  
		Last Modified: Thu, 10 Sep 2020 02:46:21 GMT  
		Size: 131.4 MB (131392179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10` - linux; ppc64le

```console
$ docker pull mono@sha256:b8c551764ab121348d5a5b162b12f0b2a502a49198c74891cdd0c24e8cb6edb1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.1 MB (192085402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:986fc10b226d2b7a4e6847eb4e4451f452b95bad5fb31f38f99795e2fae34446`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 10 Sep 2020 01:06:11 GMT
ADD file:4dede556abae88027bd22f3166fdbc38778a6fcd686c5ce768c3ca024ab3f9cf in / 
# Thu, 10 Sep 2020 01:06:20 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 19:01:16 GMT
ENV MONO_VERSION=6.10.0.104
# Thu, 10 Sep 2020 19:05:10 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 10 Sep 2020 19:07:24 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 10 Sep 2020 19:41:11 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:f8aef3d2247e5f990bc767bc99f575b9bcec34aaa37183414eebe28fcd09519d`  
		Last Modified: Thu, 10 Sep 2020 01:28:12 GMT  
		Size: 30.5 MB (30517880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91a5b381ce455eca298e810bbcff286cc9167c82392b00241d01cc6bc65cfe86`  
		Last Modified: Thu, 10 Sep 2020 19:42:19 GMT  
		Size: 256.3 KB (256260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3df1215b828b18d641c32013a7c8597874acf4085e9fc7b404d9216a5e67ecc3`  
		Last Modified: Thu, 10 Sep 2020 19:42:28 GMT  
		Size: 29.4 MB (29350071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96ac3143de444eb2aa16dc11160d058e94b7f635cfc9b210a3438a1535c643b1`  
		Last Modified: Thu, 10 Sep 2020 19:44:16 GMT  
		Size: 132.0 MB (131961191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.10.0`

```console
$ docker pull mono@sha256:51c78c2462224a085af0bc077f69420ee58ded25392f96b396fc84999767b360
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:6.10.0` - linux; amd64

```console
$ docker pull mono@sha256:8ddb0aa61e691c3e02dc60e6d9d37d48c9adbdcf96690d4e3b0e1f157d864f0c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.7 MB (224730258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e643114dd794dcb7b32b4cebb995622e6404e198c2698b435be26a772765604`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 10 Sep 2020 00:23:29 GMT
ADD file:e7407f2294ad23634565820b9669b18ff2a2ca0212a7ec84b9c89d8550859954 in / 
# Thu, 10 Sep 2020 00:23:30 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 06:19:25 GMT
ENV MONO_VERSION=6.10.0.104
# Thu, 10 Sep 2020 06:19:35 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 10 Sep 2020 06:20:13 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 10 Sep 2020 06:38:36 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:d121f8d1c4128ebc1e95e5bfad90a0189b84eadbbb2fbaad20cbb26d20b2c8a2`  
		Last Modified: Thu, 10 Sep 2020 00:34:02 GMT  
		Size: 27.1 MB (27092161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:140dba57f56b96691dfd0551d17470bb5f21984005c4c372509a3cc39d8618ff`  
		Last Modified: Thu, 10 Sep 2020 06:39:36 GMT  
		Size: 255.9 KB (255922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad432be9d8d43b429c26f097fa65f3e8ce3af20bd0cff99c69f5ae3ba83d421b`  
		Last Modified: Thu, 10 Sep 2020 06:39:51 GMT  
		Size: 67.1 MB (67092172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:647a8876e15683db1ea6901f3102f72d4b0cd4a6f92f4321d25cdd9410e6acf0`  
		Last Modified: Thu, 10 Sep 2020 06:41:41 GMT  
		Size: 130.3 MB (130290003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0` - linux; arm variant v5

```console
$ docker pull mono@sha256:3e601afbb4577fd538dfa06145643ef0c370d3b98b7fdbdeb8e69e6e7c3cc44b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.6 MB (180580641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0b1583a0f54587294ef3fb13293551714e84d35168baa3b742491aac91dc394`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Oct 2020 01:52:17 GMT
ADD file:b71c0fa4957d6b65af37231a105f3d17cdbafe5c7d6c37b5843ebf619c608aaa in / 
# Tue, 13 Oct 2020 01:52:27 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 02:36:19 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 13 Oct 2020 02:36:43 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 13 Oct 2020 02:37:31 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 13 Oct 2020 02:44:00 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:f991c1e1ee2c48f16625b6b61310bf3c0616c0dbda4762019117e86fd29cf9ce`  
		Last Modified: Tue, 13 Oct 2020 02:01:27 GMT  
		Size: 24.8 MB (24835992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d27e131b9898d8f02267f410169b8627b889f6585ad9300d14a4775194301b55`  
		Last Modified: Tue, 13 Oct 2020 02:44:49 GMT  
		Size: 255.9 KB (255938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07b82cc14a51474e2d05a0fd59b3fde70aa8fda539de5a302992983e4ffce7b8`  
		Last Modified: Tue, 13 Oct 2020 02:45:01 GMT  
		Size: 26.5 MB (26530650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f94ad0d9899e6c5c16486a97103eb9bbff1261c084ef2366534ae27653b23704`  
		Last Modified: Tue, 13 Oct 2020 02:46:59 GMT  
		Size: 129.0 MB (128958061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0` - linux; arm variant v7

```console
$ docker pull mono@sha256:0e797969122f94b85e9178dd9bece13c7ebd2cacf124520f4275e0ac7cd2b15d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.5 MB (176483530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b81a3bb43255d115e920754f87906a5cd00c5c5ae23a85f06c756f2c42a455b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Oct 2020 00:59:29 GMT
ADD file:e423f30ca19eb205a98de21b0545d0a764cfc4f832a9a9631542354d914d98d9 in / 
# Tue, 13 Oct 2020 00:59:31 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 04:43:09 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 13 Oct 2020 04:43:27 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 13 Oct 2020 04:44:11 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 13 Oct 2020 04:49:53 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:d6d8411ad43db0022fa0fce094cd2e8b1dd2f8a09d6880ed9beb6b4204867027`  
		Last Modified: Tue, 13 Oct 2020 01:08:28 GMT  
		Size: 22.7 MB (22699849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5228b93feed3135603bc1b4bbda140b6e3e712167c9dd5ccaad1732370cd6b93`  
		Last Modified: Tue, 13 Oct 2020 04:50:37 GMT  
		Size: 255.9 KB (255921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4e85494910fa31cd3bb70be77361cab8fa0b333de462a10ce0e2181ee165c0a`  
		Last Modified: Tue, 13 Oct 2020 04:50:46 GMT  
		Size: 25.7 MB (25729327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c0179ccf237338944b3401bc8ed480a53bd10956472cd41d05647aeb7fa46ee`  
		Last Modified: Tue, 13 Oct 2020 04:52:43 GMT  
		Size: 127.8 MB (127798433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:aed137508847cbf4f9a780482c89ec7185a4925bb21c49455867253f783b3756
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.3 MB (203294488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:932c2fe803dcfd13acda14b21319c3cc542c19c177c473ab3a72d42ec87c407a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 09 Sep 2020 23:50:54 GMT
ADD file:d870fb0484ea283840d9cc923c9c3fe36d1bb6b3b5ecfefcce06aa26a22c9414 in / 
# Wed, 09 Sep 2020 23:50:57 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 04:11:35 GMT
ENV MONO_VERSION=6.10.0.104
# Thu, 10 Sep 2020 04:11:50 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 10 Sep 2020 04:12:25 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 10 Sep 2020 04:17:44 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a6d76de28f58f3470aff71c934c0fec4e5d0fad788f8b8bcc50601266fc1b34d`  
		Last Modified: Wed, 09 Sep 2020 23:59:09 GMT  
		Size: 25.8 MB (25849325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e6286cef3ccb7f414187d0d407d414d80aefc9cbac5f8afc8b61c2144468e9d`  
		Last Modified: Thu, 10 Sep 2020 04:18:37 GMT  
		Size: 255.9 KB (255919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2922d176e5f282d1cab4d82a18705798bb201e72254252e9365c6e6d79f9193`  
		Last Modified: Thu, 10 Sep 2020 04:18:47 GMT  
		Size: 31.8 MB (31750168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:516e789eeddd8a9df62f3440c69b597818ad508f4cef3e636f2c25150e64e036`  
		Last Modified: Thu, 10 Sep 2020 04:20:35 GMT  
		Size: 145.4 MB (145439076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0` - linux; 386

```console
$ docker pull mono@sha256:d111852f67f667bb664ca166bcaf57863be573e5f9abcf640261a13ce768af9f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.5 MB (230534575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c670b9156ca83df138822e88a059b2ef4b85870178733601534fdb68cc075916`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 09 Sep 2020 23:40:19 GMT
ADD file:08dc20c9cd727ebf02cac6e4b287c3009274682174aee9222494491cd6c671b8 in / 
# Wed, 09 Sep 2020 23:40:19 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 02:37:15 GMT
ENV MONO_VERSION=6.10.0.104
# Thu, 10 Sep 2020 02:37:27 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 10 Sep 2020 02:38:12 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 10 Sep 2020 02:43:19 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:31e6582dbd9f9a84903d46339df0c393a63d2cbfb001b06b3204653cceafcc61`  
		Last Modified: Wed, 09 Sep 2020 23:46:30 GMT  
		Size: 27.8 MB (27750334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10a5b4050174b76ed23d2d3bbb436d66899f93eba56641cd1faf810f75242c67`  
		Last Modified: Thu, 10 Sep 2020 02:44:13 GMT  
		Size: 255.8 KB (255795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a251d8984c7c93892d00e6d7ad246f6eb96eb1ccef85f2aa4931d99e3fa536d0`  
		Last Modified: Thu, 10 Sep 2020 02:44:42 GMT  
		Size: 71.1 MB (71136267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:977fb5b989bb54968bfa64f742226d8805f4ec1552243874881f524b81fb29ae`  
		Last Modified: Thu, 10 Sep 2020 02:46:21 GMT  
		Size: 131.4 MB (131392179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0` - linux; ppc64le

```console
$ docker pull mono@sha256:b8c551764ab121348d5a5b162b12f0b2a502a49198c74891cdd0c24e8cb6edb1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.1 MB (192085402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:986fc10b226d2b7a4e6847eb4e4451f452b95bad5fb31f38f99795e2fae34446`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 10 Sep 2020 01:06:11 GMT
ADD file:4dede556abae88027bd22f3166fdbc38778a6fcd686c5ce768c3ca024ab3f9cf in / 
# Thu, 10 Sep 2020 01:06:20 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 19:01:16 GMT
ENV MONO_VERSION=6.10.0.104
# Thu, 10 Sep 2020 19:05:10 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 10 Sep 2020 19:07:24 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 10 Sep 2020 19:41:11 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:f8aef3d2247e5f990bc767bc99f575b9bcec34aaa37183414eebe28fcd09519d`  
		Last Modified: Thu, 10 Sep 2020 01:28:12 GMT  
		Size: 30.5 MB (30517880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91a5b381ce455eca298e810bbcff286cc9167c82392b00241d01cc6bc65cfe86`  
		Last Modified: Thu, 10 Sep 2020 19:42:19 GMT  
		Size: 256.3 KB (256260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3df1215b828b18d641c32013a7c8597874acf4085e9fc7b404d9216a5e67ecc3`  
		Last Modified: Thu, 10 Sep 2020 19:42:28 GMT  
		Size: 29.4 MB (29350071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96ac3143de444eb2aa16dc11160d058e94b7f635cfc9b210a3438a1535c643b1`  
		Last Modified: Thu, 10 Sep 2020 19:44:16 GMT  
		Size: 132.0 MB (131961191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.10.0.104`

```console
$ docker pull mono@sha256:51c78c2462224a085af0bc077f69420ee58ded25392f96b396fc84999767b360
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:6.10.0.104` - linux; amd64

```console
$ docker pull mono@sha256:8ddb0aa61e691c3e02dc60e6d9d37d48c9adbdcf96690d4e3b0e1f157d864f0c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.7 MB (224730258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e643114dd794dcb7b32b4cebb995622e6404e198c2698b435be26a772765604`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 10 Sep 2020 00:23:29 GMT
ADD file:e7407f2294ad23634565820b9669b18ff2a2ca0212a7ec84b9c89d8550859954 in / 
# Thu, 10 Sep 2020 00:23:30 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 06:19:25 GMT
ENV MONO_VERSION=6.10.0.104
# Thu, 10 Sep 2020 06:19:35 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 10 Sep 2020 06:20:13 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 10 Sep 2020 06:38:36 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:d121f8d1c4128ebc1e95e5bfad90a0189b84eadbbb2fbaad20cbb26d20b2c8a2`  
		Last Modified: Thu, 10 Sep 2020 00:34:02 GMT  
		Size: 27.1 MB (27092161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:140dba57f56b96691dfd0551d17470bb5f21984005c4c372509a3cc39d8618ff`  
		Last Modified: Thu, 10 Sep 2020 06:39:36 GMT  
		Size: 255.9 KB (255922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad432be9d8d43b429c26f097fa65f3e8ce3af20bd0cff99c69f5ae3ba83d421b`  
		Last Modified: Thu, 10 Sep 2020 06:39:51 GMT  
		Size: 67.1 MB (67092172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:647a8876e15683db1ea6901f3102f72d4b0cd4a6f92f4321d25cdd9410e6acf0`  
		Last Modified: Thu, 10 Sep 2020 06:41:41 GMT  
		Size: 130.3 MB (130290003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0.104` - linux; arm variant v5

```console
$ docker pull mono@sha256:3e601afbb4577fd538dfa06145643ef0c370d3b98b7fdbdeb8e69e6e7c3cc44b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.6 MB (180580641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0b1583a0f54587294ef3fb13293551714e84d35168baa3b742491aac91dc394`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Oct 2020 01:52:17 GMT
ADD file:b71c0fa4957d6b65af37231a105f3d17cdbafe5c7d6c37b5843ebf619c608aaa in / 
# Tue, 13 Oct 2020 01:52:27 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 02:36:19 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 13 Oct 2020 02:36:43 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 13 Oct 2020 02:37:31 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 13 Oct 2020 02:44:00 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:f991c1e1ee2c48f16625b6b61310bf3c0616c0dbda4762019117e86fd29cf9ce`  
		Last Modified: Tue, 13 Oct 2020 02:01:27 GMT  
		Size: 24.8 MB (24835992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d27e131b9898d8f02267f410169b8627b889f6585ad9300d14a4775194301b55`  
		Last Modified: Tue, 13 Oct 2020 02:44:49 GMT  
		Size: 255.9 KB (255938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07b82cc14a51474e2d05a0fd59b3fde70aa8fda539de5a302992983e4ffce7b8`  
		Last Modified: Tue, 13 Oct 2020 02:45:01 GMT  
		Size: 26.5 MB (26530650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f94ad0d9899e6c5c16486a97103eb9bbff1261c084ef2366534ae27653b23704`  
		Last Modified: Tue, 13 Oct 2020 02:46:59 GMT  
		Size: 129.0 MB (128958061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0.104` - linux; arm variant v7

```console
$ docker pull mono@sha256:0e797969122f94b85e9178dd9bece13c7ebd2cacf124520f4275e0ac7cd2b15d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.5 MB (176483530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b81a3bb43255d115e920754f87906a5cd00c5c5ae23a85f06c756f2c42a455b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Oct 2020 00:59:29 GMT
ADD file:e423f30ca19eb205a98de21b0545d0a764cfc4f832a9a9631542354d914d98d9 in / 
# Tue, 13 Oct 2020 00:59:31 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 04:43:09 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 13 Oct 2020 04:43:27 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 13 Oct 2020 04:44:11 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 13 Oct 2020 04:49:53 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:d6d8411ad43db0022fa0fce094cd2e8b1dd2f8a09d6880ed9beb6b4204867027`  
		Last Modified: Tue, 13 Oct 2020 01:08:28 GMT  
		Size: 22.7 MB (22699849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5228b93feed3135603bc1b4bbda140b6e3e712167c9dd5ccaad1732370cd6b93`  
		Last Modified: Tue, 13 Oct 2020 04:50:37 GMT  
		Size: 255.9 KB (255921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4e85494910fa31cd3bb70be77361cab8fa0b333de462a10ce0e2181ee165c0a`  
		Last Modified: Tue, 13 Oct 2020 04:50:46 GMT  
		Size: 25.7 MB (25729327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c0179ccf237338944b3401bc8ed480a53bd10956472cd41d05647aeb7fa46ee`  
		Last Modified: Tue, 13 Oct 2020 04:52:43 GMT  
		Size: 127.8 MB (127798433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0.104` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:aed137508847cbf4f9a780482c89ec7185a4925bb21c49455867253f783b3756
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.3 MB (203294488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:932c2fe803dcfd13acda14b21319c3cc542c19c177c473ab3a72d42ec87c407a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 09 Sep 2020 23:50:54 GMT
ADD file:d870fb0484ea283840d9cc923c9c3fe36d1bb6b3b5ecfefcce06aa26a22c9414 in / 
# Wed, 09 Sep 2020 23:50:57 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 04:11:35 GMT
ENV MONO_VERSION=6.10.0.104
# Thu, 10 Sep 2020 04:11:50 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 10 Sep 2020 04:12:25 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 10 Sep 2020 04:17:44 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a6d76de28f58f3470aff71c934c0fec4e5d0fad788f8b8bcc50601266fc1b34d`  
		Last Modified: Wed, 09 Sep 2020 23:59:09 GMT  
		Size: 25.8 MB (25849325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e6286cef3ccb7f414187d0d407d414d80aefc9cbac5f8afc8b61c2144468e9d`  
		Last Modified: Thu, 10 Sep 2020 04:18:37 GMT  
		Size: 255.9 KB (255919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2922d176e5f282d1cab4d82a18705798bb201e72254252e9365c6e6d79f9193`  
		Last Modified: Thu, 10 Sep 2020 04:18:47 GMT  
		Size: 31.8 MB (31750168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:516e789eeddd8a9df62f3440c69b597818ad508f4cef3e636f2c25150e64e036`  
		Last Modified: Thu, 10 Sep 2020 04:20:35 GMT  
		Size: 145.4 MB (145439076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0.104` - linux; 386

```console
$ docker pull mono@sha256:d111852f67f667bb664ca166bcaf57863be573e5f9abcf640261a13ce768af9f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.5 MB (230534575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c670b9156ca83df138822e88a059b2ef4b85870178733601534fdb68cc075916`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 09 Sep 2020 23:40:19 GMT
ADD file:08dc20c9cd727ebf02cac6e4b287c3009274682174aee9222494491cd6c671b8 in / 
# Wed, 09 Sep 2020 23:40:19 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 02:37:15 GMT
ENV MONO_VERSION=6.10.0.104
# Thu, 10 Sep 2020 02:37:27 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 10 Sep 2020 02:38:12 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 10 Sep 2020 02:43:19 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:31e6582dbd9f9a84903d46339df0c393a63d2cbfb001b06b3204653cceafcc61`  
		Last Modified: Wed, 09 Sep 2020 23:46:30 GMT  
		Size: 27.8 MB (27750334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10a5b4050174b76ed23d2d3bbb436d66899f93eba56641cd1faf810f75242c67`  
		Last Modified: Thu, 10 Sep 2020 02:44:13 GMT  
		Size: 255.8 KB (255795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a251d8984c7c93892d00e6d7ad246f6eb96eb1ccef85f2aa4931d99e3fa536d0`  
		Last Modified: Thu, 10 Sep 2020 02:44:42 GMT  
		Size: 71.1 MB (71136267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:977fb5b989bb54968bfa64f742226d8805f4ec1552243874881f524b81fb29ae`  
		Last Modified: Thu, 10 Sep 2020 02:46:21 GMT  
		Size: 131.4 MB (131392179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0.104` - linux; ppc64le

```console
$ docker pull mono@sha256:b8c551764ab121348d5a5b162b12f0b2a502a49198c74891cdd0c24e8cb6edb1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.1 MB (192085402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:986fc10b226d2b7a4e6847eb4e4451f452b95bad5fb31f38f99795e2fae34446`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 10 Sep 2020 01:06:11 GMT
ADD file:4dede556abae88027bd22f3166fdbc38778a6fcd686c5ce768c3ca024ab3f9cf in / 
# Thu, 10 Sep 2020 01:06:20 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 19:01:16 GMT
ENV MONO_VERSION=6.10.0.104
# Thu, 10 Sep 2020 19:05:10 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 10 Sep 2020 19:07:24 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 10 Sep 2020 19:41:11 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:f8aef3d2247e5f990bc767bc99f575b9bcec34aaa37183414eebe28fcd09519d`  
		Last Modified: Thu, 10 Sep 2020 01:28:12 GMT  
		Size: 30.5 MB (30517880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91a5b381ce455eca298e810bbcff286cc9167c82392b00241d01cc6bc65cfe86`  
		Last Modified: Thu, 10 Sep 2020 19:42:19 GMT  
		Size: 256.3 KB (256260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3df1215b828b18d641c32013a7c8597874acf4085e9fc7b404d9216a5e67ecc3`  
		Last Modified: Thu, 10 Sep 2020 19:42:28 GMT  
		Size: 29.4 MB (29350071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96ac3143de444eb2aa16dc11160d058e94b7f635cfc9b210a3438a1535c643b1`  
		Last Modified: Thu, 10 Sep 2020 19:44:16 GMT  
		Size: 132.0 MB (131961191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.10.0.104-slim`

```console
$ docker pull mono@sha256:2908c04bb370f95935550b9fea10a6b96ca036ae71b32d17128402a624a327a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:6.10.0.104-slim` - linux; amd64

```console
$ docker pull mono@sha256:73fadf674046469a3fc25c496c1fb3ac58ad2eda9e26aa126e5479306ed0cf95
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94440255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9430b8012739f9826cdd9f118f69e95b47e049a35266f1c31f50002f1024fd57`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 10 Sep 2020 00:23:29 GMT
ADD file:e7407f2294ad23634565820b9669b18ff2a2ca0212a7ec84b9c89d8550859954 in / 
# Thu, 10 Sep 2020 00:23:30 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 06:19:25 GMT
ENV MONO_VERSION=6.10.0.104
# Thu, 10 Sep 2020 06:19:35 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 10 Sep 2020 06:20:13 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:d121f8d1c4128ebc1e95e5bfad90a0189b84eadbbb2fbaad20cbb26d20b2c8a2`  
		Last Modified: Thu, 10 Sep 2020 00:34:02 GMT  
		Size: 27.1 MB (27092161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:140dba57f56b96691dfd0551d17470bb5f21984005c4c372509a3cc39d8618ff`  
		Last Modified: Thu, 10 Sep 2020 06:39:36 GMT  
		Size: 255.9 KB (255922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad432be9d8d43b429c26f097fa65f3e8ce3af20bd0cff99c69f5ae3ba83d421b`  
		Last Modified: Thu, 10 Sep 2020 06:39:51 GMT  
		Size: 67.1 MB (67092172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0.104-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:4f1935b74f258609d63b31cd01cabf54f735b72c77385b4d0486116f7b9ef1db
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51622580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8aaea1ec0574bca839c762a7724f248e6384ba44765e12d60a1eeb21f04760d2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Oct 2020 01:52:17 GMT
ADD file:b71c0fa4957d6b65af37231a105f3d17cdbafe5c7d6c37b5843ebf619c608aaa in / 
# Tue, 13 Oct 2020 01:52:27 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 02:36:19 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 13 Oct 2020 02:36:43 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 13 Oct 2020 02:37:31 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:f991c1e1ee2c48f16625b6b61310bf3c0616c0dbda4762019117e86fd29cf9ce`  
		Last Modified: Tue, 13 Oct 2020 02:01:27 GMT  
		Size: 24.8 MB (24835992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d27e131b9898d8f02267f410169b8627b889f6585ad9300d14a4775194301b55`  
		Last Modified: Tue, 13 Oct 2020 02:44:49 GMT  
		Size: 255.9 KB (255938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07b82cc14a51474e2d05a0fd59b3fde70aa8fda539de5a302992983e4ffce7b8`  
		Last Modified: Tue, 13 Oct 2020 02:45:01 GMT  
		Size: 26.5 MB (26530650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0.104-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:bf61cbd2fff2e9323d1f89b46e33accc00aa6aef0f7f4ab533d44ff2d3672097
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48685097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4593f3eb7182d83642b75181ed79a20590556ea1d6460aef0cad9e805bef1e10`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Oct 2020 00:59:29 GMT
ADD file:e423f30ca19eb205a98de21b0545d0a764cfc4f832a9a9631542354d914d98d9 in / 
# Tue, 13 Oct 2020 00:59:31 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 04:43:09 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 13 Oct 2020 04:43:27 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 13 Oct 2020 04:44:11 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:d6d8411ad43db0022fa0fce094cd2e8b1dd2f8a09d6880ed9beb6b4204867027`  
		Last Modified: Tue, 13 Oct 2020 01:08:28 GMT  
		Size: 22.7 MB (22699849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5228b93feed3135603bc1b4bbda140b6e3e712167c9dd5ccaad1732370cd6b93`  
		Last Modified: Tue, 13 Oct 2020 04:50:37 GMT  
		Size: 255.9 KB (255921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4e85494910fa31cd3bb70be77361cab8fa0b333de462a10ce0e2181ee165c0a`  
		Last Modified: Tue, 13 Oct 2020 04:50:46 GMT  
		Size: 25.7 MB (25729327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0.104-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:837debd8ec883ec2335ef1d2a49134236314f42b645ff3f6c7c3bba8edd39122
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.9 MB (57855412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a67ab8b67f587104f2fad4384a16c674fd915ee9365d079ff0007afd7fc611a6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 09 Sep 2020 23:50:54 GMT
ADD file:d870fb0484ea283840d9cc923c9c3fe36d1bb6b3b5ecfefcce06aa26a22c9414 in / 
# Wed, 09 Sep 2020 23:50:57 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 04:11:35 GMT
ENV MONO_VERSION=6.10.0.104
# Thu, 10 Sep 2020 04:11:50 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 10 Sep 2020 04:12:25 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a6d76de28f58f3470aff71c934c0fec4e5d0fad788f8b8bcc50601266fc1b34d`  
		Last Modified: Wed, 09 Sep 2020 23:59:09 GMT  
		Size: 25.8 MB (25849325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e6286cef3ccb7f414187d0d407d414d80aefc9cbac5f8afc8b61c2144468e9d`  
		Last Modified: Thu, 10 Sep 2020 04:18:37 GMT  
		Size: 255.9 KB (255919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2922d176e5f282d1cab4d82a18705798bb201e72254252e9365c6e6d79f9193`  
		Last Modified: Thu, 10 Sep 2020 04:18:47 GMT  
		Size: 31.8 MB (31750168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0.104-slim` - linux; 386

```console
$ docker pull mono@sha256:2a9fab669e67041d25fdb369e933e3590824683abc66c630331417cfc165ba14
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.1 MB (99142396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cc2e1b2ceaeba60abb7a332bf82875ce0709f9c94f0eda84ca9f39bc53f8b70`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 09 Sep 2020 23:40:19 GMT
ADD file:08dc20c9cd727ebf02cac6e4b287c3009274682174aee9222494491cd6c671b8 in / 
# Wed, 09 Sep 2020 23:40:19 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 02:37:15 GMT
ENV MONO_VERSION=6.10.0.104
# Thu, 10 Sep 2020 02:37:27 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 10 Sep 2020 02:38:12 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:31e6582dbd9f9a84903d46339df0c393a63d2cbfb001b06b3204653cceafcc61`  
		Last Modified: Wed, 09 Sep 2020 23:46:30 GMT  
		Size: 27.8 MB (27750334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10a5b4050174b76ed23d2d3bbb436d66899f93eba56641cd1faf810f75242c67`  
		Last Modified: Thu, 10 Sep 2020 02:44:13 GMT  
		Size: 255.8 KB (255795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a251d8984c7c93892d00e6d7ad246f6eb96eb1ccef85f2aa4931d99e3fa536d0`  
		Last Modified: Thu, 10 Sep 2020 02:44:42 GMT  
		Size: 71.1 MB (71136267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0.104-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:0747d27029d283c5d079fd0b849b546bb95eeae5adf789b192f20a6714a1f523
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60124211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60fa8a532fd76be8dc5c2045033500043c8b1d5a968372c9b52cfd0f3819eb3e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 10 Sep 2020 01:06:11 GMT
ADD file:4dede556abae88027bd22f3166fdbc38778a6fcd686c5ce768c3ca024ab3f9cf in / 
# Thu, 10 Sep 2020 01:06:20 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 19:01:16 GMT
ENV MONO_VERSION=6.10.0.104
# Thu, 10 Sep 2020 19:05:10 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 10 Sep 2020 19:07:24 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:f8aef3d2247e5f990bc767bc99f575b9bcec34aaa37183414eebe28fcd09519d`  
		Last Modified: Thu, 10 Sep 2020 01:28:12 GMT  
		Size: 30.5 MB (30517880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91a5b381ce455eca298e810bbcff286cc9167c82392b00241d01cc6bc65cfe86`  
		Last Modified: Thu, 10 Sep 2020 19:42:19 GMT  
		Size: 256.3 KB (256260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3df1215b828b18d641c32013a7c8597874acf4085e9fc7b404d9216a5e67ecc3`  
		Last Modified: Thu, 10 Sep 2020 19:42:28 GMT  
		Size: 29.4 MB (29350071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.10.0-slim`

```console
$ docker pull mono@sha256:2908c04bb370f95935550b9fea10a6b96ca036ae71b32d17128402a624a327a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:6.10.0-slim` - linux; amd64

```console
$ docker pull mono@sha256:73fadf674046469a3fc25c496c1fb3ac58ad2eda9e26aa126e5479306ed0cf95
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94440255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9430b8012739f9826cdd9f118f69e95b47e049a35266f1c31f50002f1024fd57`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 10 Sep 2020 00:23:29 GMT
ADD file:e7407f2294ad23634565820b9669b18ff2a2ca0212a7ec84b9c89d8550859954 in / 
# Thu, 10 Sep 2020 00:23:30 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 06:19:25 GMT
ENV MONO_VERSION=6.10.0.104
# Thu, 10 Sep 2020 06:19:35 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 10 Sep 2020 06:20:13 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:d121f8d1c4128ebc1e95e5bfad90a0189b84eadbbb2fbaad20cbb26d20b2c8a2`  
		Last Modified: Thu, 10 Sep 2020 00:34:02 GMT  
		Size: 27.1 MB (27092161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:140dba57f56b96691dfd0551d17470bb5f21984005c4c372509a3cc39d8618ff`  
		Last Modified: Thu, 10 Sep 2020 06:39:36 GMT  
		Size: 255.9 KB (255922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad432be9d8d43b429c26f097fa65f3e8ce3af20bd0cff99c69f5ae3ba83d421b`  
		Last Modified: Thu, 10 Sep 2020 06:39:51 GMT  
		Size: 67.1 MB (67092172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:4f1935b74f258609d63b31cd01cabf54f735b72c77385b4d0486116f7b9ef1db
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51622580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8aaea1ec0574bca839c762a7724f248e6384ba44765e12d60a1eeb21f04760d2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Oct 2020 01:52:17 GMT
ADD file:b71c0fa4957d6b65af37231a105f3d17cdbafe5c7d6c37b5843ebf619c608aaa in / 
# Tue, 13 Oct 2020 01:52:27 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 02:36:19 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 13 Oct 2020 02:36:43 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 13 Oct 2020 02:37:31 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:f991c1e1ee2c48f16625b6b61310bf3c0616c0dbda4762019117e86fd29cf9ce`  
		Last Modified: Tue, 13 Oct 2020 02:01:27 GMT  
		Size: 24.8 MB (24835992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d27e131b9898d8f02267f410169b8627b889f6585ad9300d14a4775194301b55`  
		Last Modified: Tue, 13 Oct 2020 02:44:49 GMT  
		Size: 255.9 KB (255938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07b82cc14a51474e2d05a0fd59b3fde70aa8fda539de5a302992983e4ffce7b8`  
		Last Modified: Tue, 13 Oct 2020 02:45:01 GMT  
		Size: 26.5 MB (26530650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:bf61cbd2fff2e9323d1f89b46e33accc00aa6aef0f7f4ab533d44ff2d3672097
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48685097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4593f3eb7182d83642b75181ed79a20590556ea1d6460aef0cad9e805bef1e10`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Oct 2020 00:59:29 GMT
ADD file:e423f30ca19eb205a98de21b0545d0a764cfc4f832a9a9631542354d914d98d9 in / 
# Tue, 13 Oct 2020 00:59:31 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 04:43:09 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 13 Oct 2020 04:43:27 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 13 Oct 2020 04:44:11 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:d6d8411ad43db0022fa0fce094cd2e8b1dd2f8a09d6880ed9beb6b4204867027`  
		Last Modified: Tue, 13 Oct 2020 01:08:28 GMT  
		Size: 22.7 MB (22699849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5228b93feed3135603bc1b4bbda140b6e3e712167c9dd5ccaad1732370cd6b93`  
		Last Modified: Tue, 13 Oct 2020 04:50:37 GMT  
		Size: 255.9 KB (255921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4e85494910fa31cd3bb70be77361cab8fa0b333de462a10ce0e2181ee165c0a`  
		Last Modified: Tue, 13 Oct 2020 04:50:46 GMT  
		Size: 25.7 MB (25729327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:837debd8ec883ec2335ef1d2a49134236314f42b645ff3f6c7c3bba8edd39122
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.9 MB (57855412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a67ab8b67f587104f2fad4384a16c674fd915ee9365d079ff0007afd7fc611a6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 09 Sep 2020 23:50:54 GMT
ADD file:d870fb0484ea283840d9cc923c9c3fe36d1bb6b3b5ecfefcce06aa26a22c9414 in / 
# Wed, 09 Sep 2020 23:50:57 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 04:11:35 GMT
ENV MONO_VERSION=6.10.0.104
# Thu, 10 Sep 2020 04:11:50 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 10 Sep 2020 04:12:25 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a6d76de28f58f3470aff71c934c0fec4e5d0fad788f8b8bcc50601266fc1b34d`  
		Last Modified: Wed, 09 Sep 2020 23:59:09 GMT  
		Size: 25.8 MB (25849325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e6286cef3ccb7f414187d0d407d414d80aefc9cbac5f8afc8b61c2144468e9d`  
		Last Modified: Thu, 10 Sep 2020 04:18:37 GMT  
		Size: 255.9 KB (255919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2922d176e5f282d1cab4d82a18705798bb201e72254252e9365c6e6d79f9193`  
		Last Modified: Thu, 10 Sep 2020 04:18:47 GMT  
		Size: 31.8 MB (31750168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0-slim` - linux; 386

```console
$ docker pull mono@sha256:2a9fab669e67041d25fdb369e933e3590824683abc66c630331417cfc165ba14
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.1 MB (99142396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cc2e1b2ceaeba60abb7a332bf82875ce0709f9c94f0eda84ca9f39bc53f8b70`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 09 Sep 2020 23:40:19 GMT
ADD file:08dc20c9cd727ebf02cac6e4b287c3009274682174aee9222494491cd6c671b8 in / 
# Wed, 09 Sep 2020 23:40:19 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 02:37:15 GMT
ENV MONO_VERSION=6.10.0.104
# Thu, 10 Sep 2020 02:37:27 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 10 Sep 2020 02:38:12 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:31e6582dbd9f9a84903d46339df0c393a63d2cbfb001b06b3204653cceafcc61`  
		Last Modified: Wed, 09 Sep 2020 23:46:30 GMT  
		Size: 27.8 MB (27750334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10a5b4050174b76ed23d2d3bbb436d66899f93eba56641cd1faf810f75242c67`  
		Last Modified: Thu, 10 Sep 2020 02:44:13 GMT  
		Size: 255.8 KB (255795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a251d8984c7c93892d00e6d7ad246f6eb96eb1ccef85f2aa4931d99e3fa536d0`  
		Last Modified: Thu, 10 Sep 2020 02:44:42 GMT  
		Size: 71.1 MB (71136267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:0747d27029d283c5d079fd0b849b546bb95eeae5adf789b192f20a6714a1f523
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60124211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60fa8a532fd76be8dc5c2045033500043c8b1d5a968372c9b52cfd0f3819eb3e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 10 Sep 2020 01:06:11 GMT
ADD file:4dede556abae88027bd22f3166fdbc38778a6fcd686c5ce768c3ca024ab3f9cf in / 
# Thu, 10 Sep 2020 01:06:20 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 19:01:16 GMT
ENV MONO_VERSION=6.10.0.104
# Thu, 10 Sep 2020 19:05:10 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 10 Sep 2020 19:07:24 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:f8aef3d2247e5f990bc767bc99f575b9bcec34aaa37183414eebe28fcd09519d`  
		Last Modified: Thu, 10 Sep 2020 01:28:12 GMT  
		Size: 30.5 MB (30517880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91a5b381ce455eca298e810bbcff286cc9167c82392b00241d01cc6bc65cfe86`  
		Last Modified: Thu, 10 Sep 2020 19:42:19 GMT  
		Size: 256.3 KB (256260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3df1215b828b18d641c32013a7c8597874acf4085e9fc7b404d9216a5e67ecc3`  
		Last Modified: Thu, 10 Sep 2020 19:42:28 GMT  
		Size: 29.4 MB (29350071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.10-slim`

```console
$ docker pull mono@sha256:2908c04bb370f95935550b9fea10a6b96ca036ae71b32d17128402a624a327a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:6.10-slim` - linux; amd64

```console
$ docker pull mono@sha256:73fadf674046469a3fc25c496c1fb3ac58ad2eda9e26aa126e5479306ed0cf95
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94440255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9430b8012739f9826cdd9f118f69e95b47e049a35266f1c31f50002f1024fd57`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 10 Sep 2020 00:23:29 GMT
ADD file:e7407f2294ad23634565820b9669b18ff2a2ca0212a7ec84b9c89d8550859954 in / 
# Thu, 10 Sep 2020 00:23:30 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 06:19:25 GMT
ENV MONO_VERSION=6.10.0.104
# Thu, 10 Sep 2020 06:19:35 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 10 Sep 2020 06:20:13 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:d121f8d1c4128ebc1e95e5bfad90a0189b84eadbbb2fbaad20cbb26d20b2c8a2`  
		Last Modified: Thu, 10 Sep 2020 00:34:02 GMT  
		Size: 27.1 MB (27092161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:140dba57f56b96691dfd0551d17470bb5f21984005c4c372509a3cc39d8618ff`  
		Last Modified: Thu, 10 Sep 2020 06:39:36 GMT  
		Size: 255.9 KB (255922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad432be9d8d43b429c26f097fa65f3e8ce3af20bd0cff99c69f5ae3ba83d421b`  
		Last Modified: Thu, 10 Sep 2020 06:39:51 GMT  
		Size: 67.1 MB (67092172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:4f1935b74f258609d63b31cd01cabf54f735b72c77385b4d0486116f7b9ef1db
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51622580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8aaea1ec0574bca839c762a7724f248e6384ba44765e12d60a1eeb21f04760d2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Oct 2020 01:52:17 GMT
ADD file:b71c0fa4957d6b65af37231a105f3d17cdbafe5c7d6c37b5843ebf619c608aaa in / 
# Tue, 13 Oct 2020 01:52:27 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 02:36:19 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 13 Oct 2020 02:36:43 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 13 Oct 2020 02:37:31 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:f991c1e1ee2c48f16625b6b61310bf3c0616c0dbda4762019117e86fd29cf9ce`  
		Last Modified: Tue, 13 Oct 2020 02:01:27 GMT  
		Size: 24.8 MB (24835992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d27e131b9898d8f02267f410169b8627b889f6585ad9300d14a4775194301b55`  
		Last Modified: Tue, 13 Oct 2020 02:44:49 GMT  
		Size: 255.9 KB (255938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07b82cc14a51474e2d05a0fd59b3fde70aa8fda539de5a302992983e4ffce7b8`  
		Last Modified: Tue, 13 Oct 2020 02:45:01 GMT  
		Size: 26.5 MB (26530650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:bf61cbd2fff2e9323d1f89b46e33accc00aa6aef0f7f4ab533d44ff2d3672097
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48685097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4593f3eb7182d83642b75181ed79a20590556ea1d6460aef0cad9e805bef1e10`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Oct 2020 00:59:29 GMT
ADD file:e423f30ca19eb205a98de21b0545d0a764cfc4f832a9a9631542354d914d98d9 in / 
# Tue, 13 Oct 2020 00:59:31 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 04:43:09 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 13 Oct 2020 04:43:27 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 13 Oct 2020 04:44:11 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:d6d8411ad43db0022fa0fce094cd2e8b1dd2f8a09d6880ed9beb6b4204867027`  
		Last Modified: Tue, 13 Oct 2020 01:08:28 GMT  
		Size: 22.7 MB (22699849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5228b93feed3135603bc1b4bbda140b6e3e712167c9dd5ccaad1732370cd6b93`  
		Last Modified: Tue, 13 Oct 2020 04:50:37 GMT  
		Size: 255.9 KB (255921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4e85494910fa31cd3bb70be77361cab8fa0b333de462a10ce0e2181ee165c0a`  
		Last Modified: Tue, 13 Oct 2020 04:50:46 GMT  
		Size: 25.7 MB (25729327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:837debd8ec883ec2335ef1d2a49134236314f42b645ff3f6c7c3bba8edd39122
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.9 MB (57855412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a67ab8b67f587104f2fad4384a16c674fd915ee9365d079ff0007afd7fc611a6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 09 Sep 2020 23:50:54 GMT
ADD file:d870fb0484ea283840d9cc923c9c3fe36d1bb6b3b5ecfefcce06aa26a22c9414 in / 
# Wed, 09 Sep 2020 23:50:57 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 04:11:35 GMT
ENV MONO_VERSION=6.10.0.104
# Thu, 10 Sep 2020 04:11:50 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 10 Sep 2020 04:12:25 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a6d76de28f58f3470aff71c934c0fec4e5d0fad788f8b8bcc50601266fc1b34d`  
		Last Modified: Wed, 09 Sep 2020 23:59:09 GMT  
		Size: 25.8 MB (25849325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e6286cef3ccb7f414187d0d407d414d80aefc9cbac5f8afc8b61c2144468e9d`  
		Last Modified: Thu, 10 Sep 2020 04:18:37 GMT  
		Size: 255.9 KB (255919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2922d176e5f282d1cab4d82a18705798bb201e72254252e9365c6e6d79f9193`  
		Last Modified: Thu, 10 Sep 2020 04:18:47 GMT  
		Size: 31.8 MB (31750168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10-slim` - linux; 386

```console
$ docker pull mono@sha256:2a9fab669e67041d25fdb369e933e3590824683abc66c630331417cfc165ba14
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.1 MB (99142396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cc2e1b2ceaeba60abb7a332bf82875ce0709f9c94f0eda84ca9f39bc53f8b70`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 09 Sep 2020 23:40:19 GMT
ADD file:08dc20c9cd727ebf02cac6e4b287c3009274682174aee9222494491cd6c671b8 in / 
# Wed, 09 Sep 2020 23:40:19 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 02:37:15 GMT
ENV MONO_VERSION=6.10.0.104
# Thu, 10 Sep 2020 02:37:27 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 10 Sep 2020 02:38:12 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:31e6582dbd9f9a84903d46339df0c393a63d2cbfb001b06b3204653cceafcc61`  
		Last Modified: Wed, 09 Sep 2020 23:46:30 GMT  
		Size: 27.8 MB (27750334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10a5b4050174b76ed23d2d3bbb436d66899f93eba56641cd1faf810f75242c67`  
		Last Modified: Thu, 10 Sep 2020 02:44:13 GMT  
		Size: 255.8 KB (255795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a251d8984c7c93892d00e6d7ad246f6eb96eb1ccef85f2aa4931d99e3fa536d0`  
		Last Modified: Thu, 10 Sep 2020 02:44:42 GMT  
		Size: 71.1 MB (71136267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:0747d27029d283c5d079fd0b849b546bb95eeae5adf789b192f20a6714a1f523
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60124211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60fa8a532fd76be8dc5c2045033500043c8b1d5a968372c9b52cfd0f3819eb3e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 10 Sep 2020 01:06:11 GMT
ADD file:4dede556abae88027bd22f3166fdbc38778a6fcd686c5ce768c3ca024ab3f9cf in / 
# Thu, 10 Sep 2020 01:06:20 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 19:01:16 GMT
ENV MONO_VERSION=6.10.0.104
# Thu, 10 Sep 2020 19:05:10 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 10 Sep 2020 19:07:24 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:f8aef3d2247e5f990bc767bc99f575b9bcec34aaa37183414eebe28fcd09519d`  
		Last Modified: Thu, 10 Sep 2020 01:28:12 GMT  
		Size: 30.5 MB (30517880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91a5b381ce455eca298e810bbcff286cc9167c82392b00241d01cc6bc65cfe86`  
		Last Modified: Thu, 10 Sep 2020 19:42:19 GMT  
		Size: 256.3 KB (256260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3df1215b828b18d641c32013a7c8597874acf4085e9fc7b404d9216a5e67ecc3`  
		Last Modified: Thu, 10 Sep 2020 19:42:28 GMT  
		Size: 29.4 MB (29350071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.8`

```console
$ docker pull mono@sha256:320a37ede62106d58b181b9a9dbd59309ec8f59a046cf31d04c48412f67b61d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:6.8` - linux; amd64

```console
$ docker pull mono@sha256:8c19244da5caa58568e7c2c468d4bbb767f53a3182c4f54f671d66f4b6488d9b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.6 MB (240618118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:127e40437fda375b11b577c6df357138da9adaa4ca3ab4c3e72a7a087b6d9017`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 10 Sep 2020 00:23:29 GMT
ADD file:e7407f2294ad23634565820b9669b18ff2a2ca0212a7ec84b9c89d8550859954 in / 
# Thu, 10 Sep 2020 00:23:30 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 06:18:29 GMT
ENV MONO_VERSION=6.8.0.123
# Thu, 10 Sep 2020 06:18:37 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 10 Sep 2020 06:19:16 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 10 Sep 2020 06:30:55 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:d121f8d1c4128ebc1e95e5bfad90a0189b84eadbbb2fbaad20cbb26d20b2c8a2`  
		Last Modified: Thu, 10 Sep 2020 00:34:02 GMT  
		Size: 27.1 MB (27092161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:143cb4fce8901da7905e2b4c0a47695a56b33e87da8be61225696ecec6767fdf`  
		Last Modified: Thu, 10 Sep 2020 06:39:13 GMT  
		Size: 255.9 KB (255893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f107f38aa9f6205e799d0db51290869d0b07b0d1f196ee41b21a36718f7655d0`  
		Last Modified: Thu, 10 Sep 2020 06:39:32 GMT  
		Size: 67.1 MB (67083998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15093c297e530b3e2481d0f72da74eb1627a441dcc13f1fbef7bcd47810cf04a`  
		Last Modified: Thu, 10 Sep 2020 06:40:34 GMT  
		Size: 146.2 MB (146186066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8` - linux; arm variant v5

```console
$ docker pull mono@sha256:a0a1a561f24b8db06e703f007caa49771a3ded79bfc07da63a4266618839a4df
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.9 MB (179921571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b41e1c51d61456193c2e5b4ac15db06ad90625b510bd72e08fe44315a015aba6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Oct 2020 01:52:17 GMT
ADD file:b71c0fa4957d6b65af37231a105f3d17cdbafe5c7d6c37b5843ebf619c608aaa in / 
# Tue, 13 Oct 2020 01:52:27 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 02:34:46 GMT
ENV MONO_VERSION=6.8.0.123
# Tue, 13 Oct 2020 02:35:14 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 13 Oct 2020 02:36:05 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 13 Oct 2020 02:40:37 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:f991c1e1ee2c48f16625b6b61310bf3c0616c0dbda4762019117e86fd29cf9ce`  
		Last Modified: Tue, 13 Oct 2020 02:01:27 GMT  
		Size: 24.8 MB (24835992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d58c01c93058384dcced83ee11026a0e5e2652432af5c3eaa02592a2cebdfdf6`  
		Last Modified: Tue, 13 Oct 2020 02:44:29 GMT  
		Size: 256.0 KB (255998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfd8d0a31f42e3311b822b7c94bb005cf72849efb2f5c39943b70702c6631de9`  
		Last Modified: Tue, 13 Oct 2020 02:44:40 GMT  
		Size: 26.5 MB (26542426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08a0dc85b1e28eca63d1eca67c1f5eb3106274e0105c3c7a0472772c6a1a29ef`  
		Last Modified: Tue, 13 Oct 2020 02:46:02 GMT  
		Size: 128.3 MB (128287155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8` - linux; arm variant v7

```console
$ docker pull mono@sha256:1ebaea3f991a9b92059fd344af338b680011d16745947186b7cd73741eba7157
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.8 MB (175801368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75ea12bfc2cc9a20e0025697f00d3707f17f0e2d0501f3ea8ebe292614dd72ec`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Oct 2020 00:59:29 GMT
ADD file:e423f30ca19eb205a98de21b0545d0a764cfc4f832a9a9631542354d914d98d9 in / 
# Tue, 13 Oct 2020 00:59:31 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 04:42:00 GMT
ENV MONO_VERSION=6.8.0.123
# Tue, 13 Oct 2020 04:42:16 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 13 Oct 2020 04:43:00 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 13 Oct 2020 04:47:05 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:d6d8411ad43db0022fa0fce094cd2e8b1dd2f8a09d6880ed9beb6b4204867027`  
		Last Modified: Tue, 13 Oct 2020 01:08:28 GMT  
		Size: 22.7 MB (22699849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:053722f7b6b8ff8b79ff2487965425c4a35e48783e16f602bac9cc463f1514c7`  
		Last Modified: Tue, 13 Oct 2020 04:50:17 GMT  
		Size: 255.9 KB (255908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e3dc69451bafa4aa4ed7b7eed809f3e7039f7e9362c96bff1bb37179a1f035e`  
		Last Modified: Tue, 13 Oct 2020 04:50:28 GMT  
		Size: 25.7 MB (25726500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fc49c6d1dda18c03351b7935d16b6e3eceddcc30881a4f5416d9f147a3e4ac4`  
		Last Modified: Tue, 13 Oct 2020 04:51:47 GMT  
		Size: 127.1 MB (127119111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:9a32e3984acd138e7d669ce175fb7f9b0b0a53c6d43ffa3a1e36f5eab47e9888
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.4 MB (202436881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ac9254d357bc82ad2c566b4e95d5854c5a890b8e369c3eec3dc87ba57e4a402`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 09 Sep 2020 23:50:54 GMT
ADD file:d870fb0484ea283840d9cc923c9c3fe36d1bb6b3b5ecfefcce06aa26a22c9414 in / 
# Wed, 09 Sep 2020 23:50:57 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 04:10:03 GMT
ENV MONO_VERSION=6.8.0.123
# Thu, 10 Sep 2020 04:10:38 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 10 Sep 2020 04:11:18 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 10 Sep 2020 04:15:03 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a6d76de28f58f3470aff71c934c0fec4e5d0fad788f8b8bcc50601266fc1b34d`  
		Last Modified: Wed, 09 Sep 2020 23:59:09 GMT  
		Size: 25.8 MB (25849325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad3035f033e5c50e5b72b987ddabe67b8e1673b67a80594cb6c2e166fbc2451e`  
		Last Modified: Thu, 10 Sep 2020 04:18:20 GMT  
		Size: 256.0 KB (256014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2318ec3a198c5af2eb8b18a4c69afe779cfc4e227dccc44b0b616f1eba0e623`  
		Last Modified: Thu, 10 Sep 2020 04:18:28 GMT  
		Size: 31.7 MB (31694738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd008299a57d7af0368120e267f43d96703a551eb8833e667f8d21f21a709ea1`  
		Last Modified: Thu, 10 Sep 2020 04:19:44 GMT  
		Size: 144.6 MB (144636804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8` - linux; 386

```console
$ docker pull mono@sha256:0c38cc7c1f3753e0ccf036502e97fe356961431f342cd5616d3bb0e174bd7be8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.2 MB (249227694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51c9b17ca8f0b950231189ae43c79238a8279d76221f31a2478dd7563e7bc684`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 09 Sep 2020 23:40:19 GMT
ADD file:08dc20c9cd727ebf02cac6e4b287c3009274682174aee9222494491cd6c671b8 in / 
# Wed, 09 Sep 2020 23:40:19 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 02:35:58 GMT
ENV MONO_VERSION=6.8.0.123
# Thu, 10 Sep 2020 02:36:10 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 10 Sep 2020 02:36:59 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 10 Sep 2020 02:40:54 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:31e6582dbd9f9a84903d46339df0c393a63d2cbfb001b06b3204653cceafcc61`  
		Last Modified: Wed, 09 Sep 2020 23:46:30 GMT  
		Size: 27.8 MB (27750334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aad82c343652f6abb0aa2c6b4c58d68ba7bb6d70f0a52f9674b18a54d41bdabc`  
		Last Modified: Thu, 10 Sep 2020 02:43:37 GMT  
		Size: 255.8 KB (255778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d4a52d2efb3aede424ea811ba691119d849c54bd5efda04c9f6c0cfaf84f4dd`  
		Last Modified: Thu, 10 Sep 2020 02:44:08 GMT  
		Size: 71.1 MB (71106160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d6598ae0ae4aad9c2f4d2778c76e02ccff85f7b4ae078a9180e107b2a56e165`  
		Last Modified: Thu, 10 Sep 2020 02:45:39 GMT  
		Size: 150.1 MB (150115422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8` - linux; ppc64le

```console
$ docker pull mono@sha256:a29cfb3813914a9f853d846520df134a2dd9c8e47cda20356159a8a9b3740507
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.3 MB (191349005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdbc99ed3dcf46e56af3cedefe9bb943d84c5940f4b023f37dc6c9493fd16c71`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 10 Sep 2020 01:06:11 GMT
ADD file:4dede556abae88027bd22f3166fdbc38778a6fcd686c5ce768c3ca024ab3f9cf in / 
# Thu, 10 Sep 2020 01:06:20 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 18:54:59 GMT
ENV MONO_VERSION=6.8.0.123
# Thu, 10 Sep 2020 18:58:23 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 10 Sep 2020 19:00:53 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 10 Sep 2020 19:21:26 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:f8aef3d2247e5f990bc767bc99f575b9bcec34aaa37183414eebe28fcd09519d`  
		Last Modified: Thu, 10 Sep 2020 01:28:12 GMT  
		Size: 30.5 MB (30517880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:693942962ba9930c35c80ccb1f1e3d6b8cf4ea69312000f87c7e70a8a583bd97`  
		Last Modified: Thu, 10 Sep 2020 19:41:53 GMT  
		Size: 256.3 KB (256333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed2a64806f5e29d588d2c7ba26ea2707bb2c9579d445ddcf7819f57344c4b54c`  
		Last Modified: Thu, 10 Sep 2020 19:42:03 GMT  
		Size: 29.3 MB (29331160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f27bec131ea13c7e217983784bb2dd8156e98292b5aea70d9b890887a3fb19ac`  
		Last Modified: Thu, 10 Sep 2020 19:43:23 GMT  
		Size: 131.2 MB (131243632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.8.0`

```console
$ docker pull mono@sha256:320a37ede62106d58b181b9a9dbd59309ec8f59a046cf31d04c48412f67b61d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:6.8.0` - linux; amd64

```console
$ docker pull mono@sha256:8c19244da5caa58568e7c2c468d4bbb767f53a3182c4f54f671d66f4b6488d9b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.6 MB (240618118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:127e40437fda375b11b577c6df357138da9adaa4ca3ab4c3e72a7a087b6d9017`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 10 Sep 2020 00:23:29 GMT
ADD file:e7407f2294ad23634565820b9669b18ff2a2ca0212a7ec84b9c89d8550859954 in / 
# Thu, 10 Sep 2020 00:23:30 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 06:18:29 GMT
ENV MONO_VERSION=6.8.0.123
# Thu, 10 Sep 2020 06:18:37 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 10 Sep 2020 06:19:16 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 10 Sep 2020 06:30:55 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:d121f8d1c4128ebc1e95e5bfad90a0189b84eadbbb2fbaad20cbb26d20b2c8a2`  
		Last Modified: Thu, 10 Sep 2020 00:34:02 GMT  
		Size: 27.1 MB (27092161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:143cb4fce8901da7905e2b4c0a47695a56b33e87da8be61225696ecec6767fdf`  
		Last Modified: Thu, 10 Sep 2020 06:39:13 GMT  
		Size: 255.9 KB (255893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f107f38aa9f6205e799d0db51290869d0b07b0d1f196ee41b21a36718f7655d0`  
		Last Modified: Thu, 10 Sep 2020 06:39:32 GMT  
		Size: 67.1 MB (67083998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15093c297e530b3e2481d0f72da74eb1627a441dcc13f1fbef7bcd47810cf04a`  
		Last Modified: Thu, 10 Sep 2020 06:40:34 GMT  
		Size: 146.2 MB (146186066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8.0` - linux; arm variant v5

```console
$ docker pull mono@sha256:a0a1a561f24b8db06e703f007caa49771a3ded79bfc07da63a4266618839a4df
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.9 MB (179921571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b41e1c51d61456193c2e5b4ac15db06ad90625b510bd72e08fe44315a015aba6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Oct 2020 01:52:17 GMT
ADD file:b71c0fa4957d6b65af37231a105f3d17cdbafe5c7d6c37b5843ebf619c608aaa in / 
# Tue, 13 Oct 2020 01:52:27 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 02:34:46 GMT
ENV MONO_VERSION=6.8.0.123
# Tue, 13 Oct 2020 02:35:14 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 13 Oct 2020 02:36:05 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 13 Oct 2020 02:40:37 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:f991c1e1ee2c48f16625b6b61310bf3c0616c0dbda4762019117e86fd29cf9ce`  
		Last Modified: Tue, 13 Oct 2020 02:01:27 GMT  
		Size: 24.8 MB (24835992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d58c01c93058384dcced83ee11026a0e5e2652432af5c3eaa02592a2cebdfdf6`  
		Last Modified: Tue, 13 Oct 2020 02:44:29 GMT  
		Size: 256.0 KB (255998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfd8d0a31f42e3311b822b7c94bb005cf72849efb2f5c39943b70702c6631de9`  
		Last Modified: Tue, 13 Oct 2020 02:44:40 GMT  
		Size: 26.5 MB (26542426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08a0dc85b1e28eca63d1eca67c1f5eb3106274e0105c3c7a0472772c6a1a29ef`  
		Last Modified: Tue, 13 Oct 2020 02:46:02 GMT  
		Size: 128.3 MB (128287155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8.0` - linux; arm variant v7

```console
$ docker pull mono@sha256:1ebaea3f991a9b92059fd344af338b680011d16745947186b7cd73741eba7157
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.8 MB (175801368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75ea12bfc2cc9a20e0025697f00d3707f17f0e2d0501f3ea8ebe292614dd72ec`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Oct 2020 00:59:29 GMT
ADD file:e423f30ca19eb205a98de21b0545d0a764cfc4f832a9a9631542354d914d98d9 in / 
# Tue, 13 Oct 2020 00:59:31 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 04:42:00 GMT
ENV MONO_VERSION=6.8.0.123
# Tue, 13 Oct 2020 04:42:16 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 13 Oct 2020 04:43:00 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 13 Oct 2020 04:47:05 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:d6d8411ad43db0022fa0fce094cd2e8b1dd2f8a09d6880ed9beb6b4204867027`  
		Last Modified: Tue, 13 Oct 2020 01:08:28 GMT  
		Size: 22.7 MB (22699849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:053722f7b6b8ff8b79ff2487965425c4a35e48783e16f602bac9cc463f1514c7`  
		Last Modified: Tue, 13 Oct 2020 04:50:17 GMT  
		Size: 255.9 KB (255908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e3dc69451bafa4aa4ed7b7eed809f3e7039f7e9362c96bff1bb37179a1f035e`  
		Last Modified: Tue, 13 Oct 2020 04:50:28 GMT  
		Size: 25.7 MB (25726500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fc49c6d1dda18c03351b7935d16b6e3eceddcc30881a4f5416d9f147a3e4ac4`  
		Last Modified: Tue, 13 Oct 2020 04:51:47 GMT  
		Size: 127.1 MB (127119111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8.0` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:9a32e3984acd138e7d669ce175fb7f9b0b0a53c6d43ffa3a1e36f5eab47e9888
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.4 MB (202436881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ac9254d357bc82ad2c566b4e95d5854c5a890b8e369c3eec3dc87ba57e4a402`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 09 Sep 2020 23:50:54 GMT
ADD file:d870fb0484ea283840d9cc923c9c3fe36d1bb6b3b5ecfefcce06aa26a22c9414 in / 
# Wed, 09 Sep 2020 23:50:57 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 04:10:03 GMT
ENV MONO_VERSION=6.8.0.123
# Thu, 10 Sep 2020 04:10:38 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 10 Sep 2020 04:11:18 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 10 Sep 2020 04:15:03 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a6d76de28f58f3470aff71c934c0fec4e5d0fad788f8b8bcc50601266fc1b34d`  
		Last Modified: Wed, 09 Sep 2020 23:59:09 GMT  
		Size: 25.8 MB (25849325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad3035f033e5c50e5b72b987ddabe67b8e1673b67a80594cb6c2e166fbc2451e`  
		Last Modified: Thu, 10 Sep 2020 04:18:20 GMT  
		Size: 256.0 KB (256014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2318ec3a198c5af2eb8b18a4c69afe779cfc4e227dccc44b0b616f1eba0e623`  
		Last Modified: Thu, 10 Sep 2020 04:18:28 GMT  
		Size: 31.7 MB (31694738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd008299a57d7af0368120e267f43d96703a551eb8833e667f8d21f21a709ea1`  
		Last Modified: Thu, 10 Sep 2020 04:19:44 GMT  
		Size: 144.6 MB (144636804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8.0` - linux; 386

```console
$ docker pull mono@sha256:0c38cc7c1f3753e0ccf036502e97fe356961431f342cd5616d3bb0e174bd7be8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.2 MB (249227694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51c9b17ca8f0b950231189ae43c79238a8279d76221f31a2478dd7563e7bc684`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 09 Sep 2020 23:40:19 GMT
ADD file:08dc20c9cd727ebf02cac6e4b287c3009274682174aee9222494491cd6c671b8 in / 
# Wed, 09 Sep 2020 23:40:19 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 02:35:58 GMT
ENV MONO_VERSION=6.8.0.123
# Thu, 10 Sep 2020 02:36:10 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 10 Sep 2020 02:36:59 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 10 Sep 2020 02:40:54 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:31e6582dbd9f9a84903d46339df0c393a63d2cbfb001b06b3204653cceafcc61`  
		Last Modified: Wed, 09 Sep 2020 23:46:30 GMT  
		Size: 27.8 MB (27750334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aad82c343652f6abb0aa2c6b4c58d68ba7bb6d70f0a52f9674b18a54d41bdabc`  
		Last Modified: Thu, 10 Sep 2020 02:43:37 GMT  
		Size: 255.8 KB (255778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d4a52d2efb3aede424ea811ba691119d849c54bd5efda04c9f6c0cfaf84f4dd`  
		Last Modified: Thu, 10 Sep 2020 02:44:08 GMT  
		Size: 71.1 MB (71106160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d6598ae0ae4aad9c2f4d2778c76e02ccff85f7b4ae078a9180e107b2a56e165`  
		Last Modified: Thu, 10 Sep 2020 02:45:39 GMT  
		Size: 150.1 MB (150115422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8.0` - linux; ppc64le

```console
$ docker pull mono@sha256:a29cfb3813914a9f853d846520df134a2dd9c8e47cda20356159a8a9b3740507
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.3 MB (191349005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdbc99ed3dcf46e56af3cedefe9bb943d84c5940f4b023f37dc6c9493fd16c71`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 10 Sep 2020 01:06:11 GMT
ADD file:4dede556abae88027bd22f3166fdbc38778a6fcd686c5ce768c3ca024ab3f9cf in / 
# Thu, 10 Sep 2020 01:06:20 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 18:54:59 GMT
ENV MONO_VERSION=6.8.0.123
# Thu, 10 Sep 2020 18:58:23 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 10 Sep 2020 19:00:53 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 10 Sep 2020 19:21:26 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:f8aef3d2247e5f990bc767bc99f575b9bcec34aaa37183414eebe28fcd09519d`  
		Last Modified: Thu, 10 Sep 2020 01:28:12 GMT  
		Size: 30.5 MB (30517880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:693942962ba9930c35c80ccb1f1e3d6b8cf4ea69312000f87c7e70a8a583bd97`  
		Last Modified: Thu, 10 Sep 2020 19:41:53 GMT  
		Size: 256.3 KB (256333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed2a64806f5e29d588d2c7ba26ea2707bb2c9579d445ddcf7819f57344c4b54c`  
		Last Modified: Thu, 10 Sep 2020 19:42:03 GMT  
		Size: 29.3 MB (29331160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f27bec131ea13c7e217983784bb2dd8156e98292b5aea70d9b890887a3fb19ac`  
		Last Modified: Thu, 10 Sep 2020 19:43:23 GMT  
		Size: 131.2 MB (131243632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.8.0.123`

```console
$ docker pull mono@sha256:320a37ede62106d58b181b9a9dbd59309ec8f59a046cf31d04c48412f67b61d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:6.8.0.123` - linux; amd64

```console
$ docker pull mono@sha256:8c19244da5caa58568e7c2c468d4bbb767f53a3182c4f54f671d66f4b6488d9b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.6 MB (240618118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:127e40437fda375b11b577c6df357138da9adaa4ca3ab4c3e72a7a087b6d9017`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 10 Sep 2020 00:23:29 GMT
ADD file:e7407f2294ad23634565820b9669b18ff2a2ca0212a7ec84b9c89d8550859954 in / 
# Thu, 10 Sep 2020 00:23:30 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 06:18:29 GMT
ENV MONO_VERSION=6.8.0.123
# Thu, 10 Sep 2020 06:18:37 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 10 Sep 2020 06:19:16 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 10 Sep 2020 06:30:55 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:d121f8d1c4128ebc1e95e5bfad90a0189b84eadbbb2fbaad20cbb26d20b2c8a2`  
		Last Modified: Thu, 10 Sep 2020 00:34:02 GMT  
		Size: 27.1 MB (27092161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:143cb4fce8901da7905e2b4c0a47695a56b33e87da8be61225696ecec6767fdf`  
		Last Modified: Thu, 10 Sep 2020 06:39:13 GMT  
		Size: 255.9 KB (255893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f107f38aa9f6205e799d0db51290869d0b07b0d1f196ee41b21a36718f7655d0`  
		Last Modified: Thu, 10 Sep 2020 06:39:32 GMT  
		Size: 67.1 MB (67083998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15093c297e530b3e2481d0f72da74eb1627a441dcc13f1fbef7bcd47810cf04a`  
		Last Modified: Thu, 10 Sep 2020 06:40:34 GMT  
		Size: 146.2 MB (146186066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8.0.123` - linux; arm variant v5

```console
$ docker pull mono@sha256:a0a1a561f24b8db06e703f007caa49771a3ded79bfc07da63a4266618839a4df
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.9 MB (179921571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b41e1c51d61456193c2e5b4ac15db06ad90625b510bd72e08fe44315a015aba6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Oct 2020 01:52:17 GMT
ADD file:b71c0fa4957d6b65af37231a105f3d17cdbafe5c7d6c37b5843ebf619c608aaa in / 
# Tue, 13 Oct 2020 01:52:27 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 02:34:46 GMT
ENV MONO_VERSION=6.8.0.123
# Tue, 13 Oct 2020 02:35:14 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 13 Oct 2020 02:36:05 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 13 Oct 2020 02:40:37 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:f991c1e1ee2c48f16625b6b61310bf3c0616c0dbda4762019117e86fd29cf9ce`  
		Last Modified: Tue, 13 Oct 2020 02:01:27 GMT  
		Size: 24.8 MB (24835992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d58c01c93058384dcced83ee11026a0e5e2652432af5c3eaa02592a2cebdfdf6`  
		Last Modified: Tue, 13 Oct 2020 02:44:29 GMT  
		Size: 256.0 KB (255998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfd8d0a31f42e3311b822b7c94bb005cf72849efb2f5c39943b70702c6631de9`  
		Last Modified: Tue, 13 Oct 2020 02:44:40 GMT  
		Size: 26.5 MB (26542426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08a0dc85b1e28eca63d1eca67c1f5eb3106274e0105c3c7a0472772c6a1a29ef`  
		Last Modified: Tue, 13 Oct 2020 02:46:02 GMT  
		Size: 128.3 MB (128287155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8.0.123` - linux; arm variant v7

```console
$ docker pull mono@sha256:1ebaea3f991a9b92059fd344af338b680011d16745947186b7cd73741eba7157
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.8 MB (175801368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75ea12bfc2cc9a20e0025697f00d3707f17f0e2d0501f3ea8ebe292614dd72ec`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Oct 2020 00:59:29 GMT
ADD file:e423f30ca19eb205a98de21b0545d0a764cfc4f832a9a9631542354d914d98d9 in / 
# Tue, 13 Oct 2020 00:59:31 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 04:42:00 GMT
ENV MONO_VERSION=6.8.0.123
# Tue, 13 Oct 2020 04:42:16 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 13 Oct 2020 04:43:00 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 13 Oct 2020 04:47:05 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:d6d8411ad43db0022fa0fce094cd2e8b1dd2f8a09d6880ed9beb6b4204867027`  
		Last Modified: Tue, 13 Oct 2020 01:08:28 GMT  
		Size: 22.7 MB (22699849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:053722f7b6b8ff8b79ff2487965425c4a35e48783e16f602bac9cc463f1514c7`  
		Last Modified: Tue, 13 Oct 2020 04:50:17 GMT  
		Size: 255.9 KB (255908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e3dc69451bafa4aa4ed7b7eed809f3e7039f7e9362c96bff1bb37179a1f035e`  
		Last Modified: Tue, 13 Oct 2020 04:50:28 GMT  
		Size: 25.7 MB (25726500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fc49c6d1dda18c03351b7935d16b6e3eceddcc30881a4f5416d9f147a3e4ac4`  
		Last Modified: Tue, 13 Oct 2020 04:51:47 GMT  
		Size: 127.1 MB (127119111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8.0.123` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:9a32e3984acd138e7d669ce175fb7f9b0b0a53c6d43ffa3a1e36f5eab47e9888
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.4 MB (202436881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ac9254d357bc82ad2c566b4e95d5854c5a890b8e369c3eec3dc87ba57e4a402`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 09 Sep 2020 23:50:54 GMT
ADD file:d870fb0484ea283840d9cc923c9c3fe36d1bb6b3b5ecfefcce06aa26a22c9414 in / 
# Wed, 09 Sep 2020 23:50:57 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 04:10:03 GMT
ENV MONO_VERSION=6.8.0.123
# Thu, 10 Sep 2020 04:10:38 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 10 Sep 2020 04:11:18 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 10 Sep 2020 04:15:03 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a6d76de28f58f3470aff71c934c0fec4e5d0fad788f8b8bcc50601266fc1b34d`  
		Last Modified: Wed, 09 Sep 2020 23:59:09 GMT  
		Size: 25.8 MB (25849325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad3035f033e5c50e5b72b987ddabe67b8e1673b67a80594cb6c2e166fbc2451e`  
		Last Modified: Thu, 10 Sep 2020 04:18:20 GMT  
		Size: 256.0 KB (256014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2318ec3a198c5af2eb8b18a4c69afe779cfc4e227dccc44b0b616f1eba0e623`  
		Last Modified: Thu, 10 Sep 2020 04:18:28 GMT  
		Size: 31.7 MB (31694738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd008299a57d7af0368120e267f43d96703a551eb8833e667f8d21f21a709ea1`  
		Last Modified: Thu, 10 Sep 2020 04:19:44 GMT  
		Size: 144.6 MB (144636804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8.0.123` - linux; 386

```console
$ docker pull mono@sha256:0c38cc7c1f3753e0ccf036502e97fe356961431f342cd5616d3bb0e174bd7be8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.2 MB (249227694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51c9b17ca8f0b950231189ae43c79238a8279d76221f31a2478dd7563e7bc684`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 09 Sep 2020 23:40:19 GMT
ADD file:08dc20c9cd727ebf02cac6e4b287c3009274682174aee9222494491cd6c671b8 in / 
# Wed, 09 Sep 2020 23:40:19 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 02:35:58 GMT
ENV MONO_VERSION=6.8.0.123
# Thu, 10 Sep 2020 02:36:10 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 10 Sep 2020 02:36:59 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 10 Sep 2020 02:40:54 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:31e6582dbd9f9a84903d46339df0c393a63d2cbfb001b06b3204653cceafcc61`  
		Last Modified: Wed, 09 Sep 2020 23:46:30 GMT  
		Size: 27.8 MB (27750334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aad82c343652f6abb0aa2c6b4c58d68ba7bb6d70f0a52f9674b18a54d41bdabc`  
		Last Modified: Thu, 10 Sep 2020 02:43:37 GMT  
		Size: 255.8 KB (255778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d4a52d2efb3aede424ea811ba691119d849c54bd5efda04c9f6c0cfaf84f4dd`  
		Last Modified: Thu, 10 Sep 2020 02:44:08 GMT  
		Size: 71.1 MB (71106160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d6598ae0ae4aad9c2f4d2778c76e02ccff85f7b4ae078a9180e107b2a56e165`  
		Last Modified: Thu, 10 Sep 2020 02:45:39 GMT  
		Size: 150.1 MB (150115422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8.0.123` - linux; ppc64le

```console
$ docker pull mono@sha256:a29cfb3813914a9f853d846520df134a2dd9c8e47cda20356159a8a9b3740507
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.3 MB (191349005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdbc99ed3dcf46e56af3cedefe9bb943d84c5940f4b023f37dc6c9493fd16c71`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 10 Sep 2020 01:06:11 GMT
ADD file:4dede556abae88027bd22f3166fdbc38778a6fcd686c5ce768c3ca024ab3f9cf in / 
# Thu, 10 Sep 2020 01:06:20 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 18:54:59 GMT
ENV MONO_VERSION=6.8.0.123
# Thu, 10 Sep 2020 18:58:23 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 10 Sep 2020 19:00:53 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 10 Sep 2020 19:21:26 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:f8aef3d2247e5f990bc767bc99f575b9bcec34aaa37183414eebe28fcd09519d`  
		Last Modified: Thu, 10 Sep 2020 01:28:12 GMT  
		Size: 30.5 MB (30517880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:693942962ba9930c35c80ccb1f1e3d6b8cf4ea69312000f87c7e70a8a583bd97`  
		Last Modified: Thu, 10 Sep 2020 19:41:53 GMT  
		Size: 256.3 KB (256333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed2a64806f5e29d588d2c7ba26ea2707bb2c9579d445ddcf7819f57344c4b54c`  
		Last Modified: Thu, 10 Sep 2020 19:42:03 GMT  
		Size: 29.3 MB (29331160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f27bec131ea13c7e217983784bb2dd8156e98292b5aea70d9b890887a3fb19ac`  
		Last Modified: Thu, 10 Sep 2020 19:43:23 GMT  
		Size: 131.2 MB (131243632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.8.0.123-slim`

```console
$ docker pull mono@sha256:a29ccea4800457877ae3df6bf10ae8876eed869e6805822393373061d5919cf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:6.8.0.123-slim` - linux; amd64

```console
$ docker pull mono@sha256:d84f1695c730ef32a960bccaea556addd23f91fe2f242f8269ed0969991066aa
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94432052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7af1f0c80506315073babf76da5546320a9495ed1558335fa4ca4e99c213f558`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 10 Sep 2020 00:23:29 GMT
ADD file:e7407f2294ad23634565820b9669b18ff2a2ca0212a7ec84b9c89d8550859954 in / 
# Thu, 10 Sep 2020 00:23:30 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 06:18:29 GMT
ENV MONO_VERSION=6.8.0.123
# Thu, 10 Sep 2020 06:18:37 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 10 Sep 2020 06:19:16 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:d121f8d1c4128ebc1e95e5bfad90a0189b84eadbbb2fbaad20cbb26d20b2c8a2`  
		Last Modified: Thu, 10 Sep 2020 00:34:02 GMT  
		Size: 27.1 MB (27092161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:143cb4fce8901da7905e2b4c0a47695a56b33e87da8be61225696ecec6767fdf`  
		Last Modified: Thu, 10 Sep 2020 06:39:13 GMT  
		Size: 255.9 KB (255893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f107f38aa9f6205e799d0db51290869d0b07b0d1f196ee41b21a36718f7655d0`  
		Last Modified: Thu, 10 Sep 2020 06:39:32 GMT  
		Size: 67.1 MB (67083998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8.0.123-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:251f066260187f7daae44d2b0e1c18197b67dc6275508075ae0d2dafa72c2bb8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51634416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bf6a0e393f1c11eff16fe15845a386c8de46aac69339c4113f206093c491b7e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Oct 2020 01:52:17 GMT
ADD file:b71c0fa4957d6b65af37231a105f3d17cdbafe5c7d6c37b5843ebf619c608aaa in / 
# Tue, 13 Oct 2020 01:52:27 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 02:34:46 GMT
ENV MONO_VERSION=6.8.0.123
# Tue, 13 Oct 2020 02:35:14 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 13 Oct 2020 02:36:05 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:f991c1e1ee2c48f16625b6b61310bf3c0616c0dbda4762019117e86fd29cf9ce`  
		Last Modified: Tue, 13 Oct 2020 02:01:27 GMT  
		Size: 24.8 MB (24835992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d58c01c93058384dcced83ee11026a0e5e2652432af5c3eaa02592a2cebdfdf6`  
		Last Modified: Tue, 13 Oct 2020 02:44:29 GMT  
		Size: 256.0 KB (255998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfd8d0a31f42e3311b822b7c94bb005cf72849efb2f5c39943b70702c6631de9`  
		Last Modified: Tue, 13 Oct 2020 02:44:40 GMT  
		Size: 26.5 MB (26542426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8.0.123-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:c84e88fc96c15e99d24c04f88bbbc4b73ff77f7a9bfa07c45f384136199087fc
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48682257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6f5defcf8cb930642b2a9728a83524bbf0e39ae20d2f0e63aa786a2b8d1a0e0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Oct 2020 00:59:29 GMT
ADD file:e423f30ca19eb205a98de21b0545d0a764cfc4f832a9a9631542354d914d98d9 in / 
# Tue, 13 Oct 2020 00:59:31 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 04:42:00 GMT
ENV MONO_VERSION=6.8.0.123
# Tue, 13 Oct 2020 04:42:16 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 13 Oct 2020 04:43:00 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:d6d8411ad43db0022fa0fce094cd2e8b1dd2f8a09d6880ed9beb6b4204867027`  
		Last Modified: Tue, 13 Oct 2020 01:08:28 GMT  
		Size: 22.7 MB (22699849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:053722f7b6b8ff8b79ff2487965425c4a35e48783e16f602bac9cc463f1514c7`  
		Last Modified: Tue, 13 Oct 2020 04:50:17 GMT  
		Size: 255.9 KB (255908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e3dc69451bafa4aa4ed7b7eed809f3e7039f7e9362c96bff1bb37179a1f035e`  
		Last Modified: Tue, 13 Oct 2020 04:50:28 GMT  
		Size: 25.7 MB (25726500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8.0.123-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:ee2ecb2a55c342b81a21b347bd747aebc5a4005c9fd0c087ebe376422f288ac3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.8 MB (57800077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7387d7bba2a93692cf71646146f6f075afa133a11c216361cc53362b72eb572d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 09 Sep 2020 23:50:54 GMT
ADD file:d870fb0484ea283840d9cc923c9c3fe36d1bb6b3b5ecfefcce06aa26a22c9414 in / 
# Wed, 09 Sep 2020 23:50:57 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 04:10:03 GMT
ENV MONO_VERSION=6.8.0.123
# Thu, 10 Sep 2020 04:10:38 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 10 Sep 2020 04:11:18 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a6d76de28f58f3470aff71c934c0fec4e5d0fad788f8b8bcc50601266fc1b34d`  
		Last Modified: Wed, 09 Sep 2020 23:59:09 GMT  
		Size: 25.8 MB (25849325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad3035f033e5c50e5b72b987ddabe67b8e1673b67a80594cb6c2e166fbc2451e`  
		Last Modified: Thu, 10 Sep 2020 04:18:20 GMT  
		Size: 256.0 KB (256014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2318ec3a198c5af2eb8b18a4c69afe779cfc4e227dccc44b0b616f1eba0e623`  
		Last Modified: Thu, 10 Sep 2020 04:18:28 GMT  
		Size: 31.7 MB (31694738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8.0.123-slim` - linux; 386

```console
$ docker pull mono@sha256:d1ba26182ea9eeeec138e323c54257bf1651fba14495922974e132989a3c6e7b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.1 MB (99112272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b701dfe0fd831da557161245b218185627513738fd6d2731b2d82aecfe2d1068`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 09 Sep 2020 23:40:19 GMT
ADD file:08dc20c9cd727ebf02cac6e4b287c3009274682174aee9222494491cd6c671b8 in / 
# Wed, 09 Sep 2020 23:40:19 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 02:35:58 GMT
ENV MONO_VERSION=6.8.0.123
# Thu, 10 Sep 2020 02:36:10 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 10 Sep 2020 02:36:59 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:31e6582dbd9f9a84903d46339df0c393a63d2cbfb001b06b3204653cceafcc61`  
		Last Modified: Wed, 09 Sep 2020 23:46:30 GMT  
		Size: 27.8 MB (27750334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aad82c343652f6abb0aa2c6b4c58d68ba7bb6d70f0a52f9674b18a54d41bdabc`  
		Last Modified: Thu, 10 Sep 2020 02:43:37 GMT  
		Size: 255.8 KB (255778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d4a52d2efb3aede424ea811ba691119d849c54bd5efda04c9f6c0cfaf84f4dd`  
		Last Modified: Thu, 10 Sep 2020 02:44:08 GMT  
		Size: 71.1 MB (71106160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8.0.123-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:3232b1f1bbf506eb4accea4b54f16f7abf22c502b0b103d44069dd50445ff4dd
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60105373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:740f5af31ca3b0f0b62e034adaae7a2c36d73038b8da8b7a58b2e25b25a4711a`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 10 Sep 2020 01:06:11 GMT
ADD file:4dede556abae88027bd22f3166fdbc38778a6fcd686c5ce768c3ca024ab3f9cf in / 
# Thu, 10 Sep 2020 01:06:20 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 18:54:59 GMT
ENV MONO_VERSION=6.8.0.123
# Thu, 10 Sep 2020 18:58:23 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 10 Sep 2020 19:00:53 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:f8aef3d2247e5f990bc767bc99f575b9bcec34aaa37183414eebe28fcd09519d`  
		Last Modified: Thu, 10 Sep 2020 01:28:12 GMT  
		Size: 30.5 MB (30517880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:693942962ba9930c35c80ccb1f1e3d6b8cf4ea69312000f87c7e70a8a583bd97`  
		Last Modified: Thu, 10 Sep 2020 19:41:53 GMT  
		Size: 256.3 KB (256333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed2a64806f5e29d588d2c7ba26ea2707bb2c9579d445ddcf7819f57344c4b54c`  
		Last Modified: Thu, 10 Sep 2020 19:42:03 GMT  
		Size: 29.3 MB (29331160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.8.0-slim`

```console
$ docker pull mono@sha256:a29ccea4800457877ae3df6bf10ae8876eed869e6805822393373061d5919cf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:6.8.0-slim` - linux; amd64

```console
$ docker pull mono@sha256:d84f1695c730ef32a960bccaea556addd23f91fe2f242f8269ed0969991066aa
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94432052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7af1f0c80506315073babf76da5546320a9495ed1558335fa4ca4e99c213f558`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 10 Sep 2020 00:23:29 GMT
ADD file:e7407f2294ad23634565820b9669b18ff2a2ca0212a7ec84b9c89d8550859954 in / 
# Thu, 10 Sep 2020 00:23:30 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 06:18:29 GMT
ENV MONO_VERSION=6.8.0.123
# Thu, 10 Sep 2020 06:18:37 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 10 Sep 2020 06:19:16 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:d121f8d1c4128ebc1e95e5bfad90a0189b84eadbbb2fbaad20cbb26d20b2c8a2`  
		Last Modified: Thu, 10 Sep 2020 00:34:02 GMT  
		Size: 27.1 MB (27092161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:143cb4fce8901da7905e2b4c0a47695a56b33e87da8be61225696ecec6767fdf`  
		Last Modified: Thu, 10 Sep 2020 06:39:13 GMT  
		Size: 255.9 KB (255893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f107f38aa9f6205e799d0db51290869d0b07b0d1f196ee41b21a36718f7655d0`  
		Last Modified: Thu, 10 Sep 2020 06:39:32 GMT  
		Size: 67.1 MB (67083998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8.0-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:251f066260187f7daae44d2b0e1c18197b67dc6275508075ae0d2dafa72c2bb8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51634416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bf6a0e393f1c11eff16fe15845a386c8de46aac69339c4113f206093c491b7e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Oct 2020 01:52:17 GMT
ADD file:b71c0fa4957d6b65af37231a105f3d17cdbafe5c7d6c37b5843ebf619c608aaa in / 
# Tue, 13 Oct 2020 01:52:27 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 02:34:46 GMT
ENV MONO_VERSION=6.8.0.123
# Tue, 13 Oct 2020 02:35:14 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 13 Oct 2020 02:36:05 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:f991c1e1ee2c48f16625b6b61310bf3c0616c0dbda4762019117e86fd29cf9ce`  
		Last Modified: Tue, 13 Oct 2020 02:01:27 GMT  
		Size: 24.8 MB (24835992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d58c01c93058384dcced83ee11026a0e5e2652432af5c3eaa02592a2cebdfdf6`  
		Last Modified: Tue, 13 Oct 2020 02:44:29 GMT  
		Size: 256.0 KB (255998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfd8d0a31f42e3311b822b7c94bb005cf72849efb2f5c39943b70702c6631de9`  
		Last Modified: Tue, 13 Oct 2020 02:44:40 GMT  
		Size: 26.5 MB (26542426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8.0-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:c84e88fc96c15e99d24c04f88bbbc4b73ff77f7a9bfa07c45f384136199087fc
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48682257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6f5defcf8cb930642b2a9728a83524bbf0e39ae20d2f0e63aa786a2b8d1a0e0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Oct 2020 00:59:29 GMT
ADD file:e423f30ca19eb205a98de21b0545d0a764cfc4f832a9a9631542354d914d98d9 in / 
# Tue, 13 Oct 2020 00:59:31 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 04:42:00 GMT
ENV MONO_VERSION=6.8.0.123
# Tue, 13 Oct 2020 04:42:16 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 13 Oct 2020 04:43:00 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:d6d8411ad43db0022fa0fce094cd2e8b1dd2f8a09d6880ed9beb6b4204867027`  
		Last Modified: Tue, 13 Oct 2020 01:08:28 GMT  
		Size: 22.7 MB (22699849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:053722f7b6b8ff8b79ff2487965425c4a35e48783e16f602bac9cc463f1514c7`  
		Last Modified: Tue, 13 Oct 2020 04:50:17 GMT  
		Size: 255.9 KB (255908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e3dc69451bafa4aa4ed7b7eed809f3e7039f7e9362c96bff1bb37179a1f035e`  
		Last Modified: Tue, 13 Oct 2020 04:50:28 GMT  
		Size: 25.7 MB (25726500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8.0-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:ee2ecb2a55c342b81a21b347bd747aebc5a4005c9fd0c087ebe376422f288ac3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.8 MB (57800077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7387d7bba2a93692cf71646146f6f075afa133a11c216361cc53362b72eb572d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 09 Sep 2020 23:50:54 GMT
ADD file:d870fb0484ea283840d9cc923c9c3fe36d1bb6b3b5ecfefcce06aa26a22c9414 in / 
# Wed, 09 Sep 2020 23:50:57 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 04:10:03 GMT
ENV MONO_VERSION=6.8.0.123
# Thu, 10 Sep 2020 04:10:38 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 10 Sep 2020 04:11:18 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a6d76de28f58f3470aff71c934c0fec4e5d0fad788f8b8bcc50601266fc1b34d`  
		Last Modified: Wed, 09 Sep 2020 23:59:09 GMT  
		Size: 25.8 MB (25849325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad3035f033e5c50e5b72b987ddabe67b8e1673b67a80594cb6c2e166fbc2451e`  
		Last Modified: Thu, 10 Sep 2020 04:18:20 GMT  
		Size: 256.0 KB (256014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2318ec3a198c5af2eb8b18a4c69afe779cfc4e227dccc44b0b616f1eba0e623`  
		Last Modified: Thu, 10 Sep 2020 04:18:28 GMT  
		Size: 31.7 MB (31694738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8.0-slim` - linux; 386

```console
$ docker pull mono@sha256:d1ba26182ea9eeeec138e323c54257bf1651fba14495922974e132989a3c6e7b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.1 MB (99112272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b701dfe0fd831da557161245b218185627513738fd6d2731b2d82aecfe2d1068`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 09 Sep 2020 23:40:19 GMT
ADD file:08dc20c9cd727ebf02cac6e4b287c3009274682174aee9222494491cd6c671b8 in / 
# Wed, 09 Sep 2020 23:40:19 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 02:35:58 GMT
ENV MONO_VERSION=6.8.0.123
# Thu, 10 Sep 2020 02:36:10 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 10 Sep 2020 02:36:59 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:31e6582dbd9f9a84903d46339df0c393a63d2cbfb001b06b3204653cceafcc61`  
		Last Modified: Wed, 09 Sep 2020 23:46:30 GMT  
		Size: 27.8 MB (27750334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aad82c343652f6abb0aa2c6b4c58d68ba7bb6d70f0a52f9674b18a54d41bdabc`  
		Last Modified: Thu, 10 Sep 2020 02:43:37 GMT  
		Size: 255.8 KB (255778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d4a52d2efb3aede424ea811ba691119d849c54bd5efda04c9f6c0cfaf84f4dd`  
		Last Modified: Thu, 10 Sep 2020 02:44:08 GMT  
		Size: 71.1 MB (71106160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8.0-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:3232b1f1bbf506eb4accea4b54f16f7abf22c502b0b103d44069dd50445ff4dd
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60105373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:740f5af31ca3b0f0b62e034adaae7a2c36d73038b8da8b7a58b2e25b25a4711a`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 10 Sep 2020 01:06:11 GMT
ADD file:4dede556abae88027bd22f3166fdbc38778a6fcd686c5ce768c3ca024ab3f9cf in / 
# Thu, 10 Sep 2020 01:06:20 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 18:54:59 GMT
ENV MONO_VERSION=6.8.0.123
# Thu, 10 Sep 2020 18:58:23 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 10 Sep 2020 19:00:53 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:f8aef3d2247e5f990bc767bc99f575b9bcec34aaa37183414eebe28fcd09519d`  
		Last Modified: Thu, 10 Sep 2020 01:28:12 GMT  
		Size: 30.5 MB (30517880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:693942962ba9930c35c80ccb1f1e3d6b8cf4ea69312000f87c7e70a8a583bd97`  
		Last Modified: Thu, 10 Sep 2020 19:41:53 GMT  
		Size: 256.3 KB (256333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed2a64806f5e29d588d2c7ba26ea2707bb2c9579d445ddcf7819f57344c4b54c`  
		Last Modified: Thu, 10 Sep 2020 19:42:03 GMT  
		Size: 29.3 MB (29331160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.8-slim`

```console
$ docker pull mono@sha256:a29ccea4800457877ae3df6bf10ae8876eed869e6805822393373061d5919cf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:6.8-slim` - linux; amd64

```console
$ docker pull mono@sha256:d84f1695c730ef32a960bccaea556addd23f91fe2f242f8269ed0969991066aa
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94432052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7af1f0c80506315073babf76da5546320a9495ed1558335fa4ca4e99c213f558`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 10 Sep 2020 00:23:29 GMT
ADD file:e7407f2294ad23634565820b9669b18ff2a2ca0212a7ec84b9c89d8550859954 in / 
# Thu, 10 Sep 2020 00:23:30 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 06:18:29 GMT
ENV MONO_VERSION=6.8.0.123
# Thu, 10 Sep 2020 06:18:37 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 10 Sep 2020 06:19:16 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:d121f8d1c4128ebc1e95e5bfad90a0189b84eadbbb2fbaad20cbb26d20b2c8a2`  
		Last Modified: Thu, 10 Sep 2020 00:34:02 GMT  
		Size: 27.1 MB (27092161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:143cb4fce8901da7905e2b4c0a47695a56b33e87da8be61225696ecec6767fdf`  
		Last Modified: Thu, 10 Sep 2020 06:39:13 GMT  
		Size: 255.9 KB (255893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f107f38aa9f6205e799d0db51290869d0b07b0d1f196ee41b21a36718f7655d0`  
		Last Modified: Thu, 10 Sep 2020 06:39:32 GMT  
		Size: 67.1 MB (67083998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:251f066260187f7daae44d2b0e1c18197b67dc6275508075ae0d2dafa72c2bb8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51634416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bf6a0e393f1c11eff16fe15845a386c8de46aac69339c4113f206093c491b7e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Oct 2020 01:52:17 GMT
ADD file:b71c0fa4957d6b65af37231a105f3d17cdbafe5c7d6c37b5843ebf619c608aaa in / 
# Tue, 13 Oct 2020 01:52:27 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 02:34:46 GMT
ENV MONO_VERSION=6.8.0.123
# Tue, 13 Oct 2020 02:35:14 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 13 Oct 2020 02:36:05 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:f991c1e1ee2c48f16625b6b61310bf3c0616c0dbda4762019117e86fd29cf9ce`  
		Last Modified: Tue, 13 Oct 2020 02:01:27 GMT  
		Size: 24.8 MB (24835992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d58c01c93058384dcced83ee11026a0e5e2652432af5c3eaa02592a2cebdfdf6`  
		Last Modified: Tue, 13 Oct 2020 02:44:29 GMT  
		Size: 256.0 KB (255998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfd8d0a31f42e3311b822b7c94bb005cf72849efb2f5c39943b70702c6631de9`  
		Last Modified: Tue, 13 Oct 2020 02:44:40 GMT  
		Size: 26.5 MB (26542426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:c84e88fc96c15e99d24c04f88bbbc4b73ff77f7a9bfa07c45f384136199087fc
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48682257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6f5defcf8cb930642b2a9728a83524bbf0e39ae20d2f0e63aa786a2b8d1a0e0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Oct 2020 00:59:29 GMT
ADD file:e423f30ca19eb205a98de21b0545d0a764cfc4f832a9a9631542354d914d98d9 in / 
# Tue, 13 Oct 2020 00:59:31 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 04:42:00 GMT
ENV MONO_VERSION=6.8.0.123
# Tue, 13 Oct 2020 04:42:16 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 13 Oct 2020 04:43:00 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:d6d8411ad43db0022fa0fce094cd2e8b1dd2f8a09d6880ed9beb6b4204867027`  
		Last Modified: Tue, 13 Oct 2020 01:08:28 GMT  
		Size: 22.7 MB (22699849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:053722f7b6b8ff8b79ff2487965425c4a35e48783e16f602bac9cc463f1514c7`  
		Last Modified: Tue, 13 Oct 2020 04:50:17 GMT  
		Size: 255.9 KB (255908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e3dc69451bafa4aa4ed7b7eed809f3e7039f7e9362c96bff1bb37179a1f035e`  
		Last Modified: Tue, 13 Oct 2020 04:50:28 GMT  
		Size: 25.7 MB (25726500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:ee2ecb2a55c342b81a21b347bd747aebc5a4005c9fd0c087ebe376422f288ac3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.8 MB (57800077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7387d7bba2a93692cf71646146f6f075afa133a11c216361cc53362b72eb572d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 09 Sep 2020 23:50:54 GMT
ADD file:d870fb0484ea283840d9cc923c9c3fe36d1bb6b3b5ecfefcce06aa26a22c9414 in / 
# Wed, 09 Sep 2020 23:50:57 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 04:10:03 GMT
ENV MONO_VERSION=6.8.0.123
# Thu, 10 Sep 2020 04:10:38 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 10 Sep 2020 04:11:18 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a6d76de28f58f3470aff71c934c0fec4e5d0fad788f8b8bcc50601266fc1b34d`  
		Last Modified: Wed, 09 Sep 2020 23:59:09 GMT  
		Size: 25.8 MB (25849325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad3035f033e5c50e5b72b987ddabe67b8e1673b67a80594cb6c2e166fbc2451e`  
		Last Modified: Thu, 10 Sep 2020 04:18:20 GMT  
		Size: 256.0 KB (256014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2318ec3a198c5af2eb8b18a4c69afe779cfc4e227dccc44b0b616f1eba0e623`  
		Last Modified: Thu, 10 Sep 2020 04:18:28 GMT  
		Size: 31.7 MB (31694738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8-slim` - linux; 386

```console
$ docker pull mono@sha256:d1ba26182ea9eeeec138e323c54257bf1651fba14495922974e132989a3c6e7b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.1 MB (99112272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b701dfe0fd831da557161245b218185627513738fd6d2731b2d82aecfe2d1068`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 09 Sep 2020 23:40:19 GMT
ADD file:08dc20c9cd727ebf02cac6e4b287c3009274682174aee9222494491cd6c671b8 in / 
# Wed, 09 Sep 2020 23:40:19 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 02:35:58 GMT
ENV MONO_VERSION=6.8.0.123
# Thu, 10 Sep 2020 02:36:10 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 10 Sep 2020 02:36:59 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:31e6582dbd9f9a84903d46339df0c393a63d2cbfb001b06b3204653cceafcc61`  
		Last Modified: Wed, 09 Sep 2020 23:46:30 GMT  
		Size: 27.8 MB (27750334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aad82c343652f6abb0aa2c6b4c58d68ba7bb6d70f0a52f9674b18a54d41bdabc`  
		Last Modified: Thu, 10 Sep 2020 02:43:37 GMT  
		Size: 255.8 KB (255778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d4a52d2efb3aede424ea811ba691119d849c54bd5efda04c9f6c0cfaf84f4dd`  
		Last Modified: Thu, 10 Sep 2020 02:44:08 GMT  
		Size: 71.1 MB (71106160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:3232b1f1bbf506eb4accea4b54f16f7abf22c502b0b103d44069dd50445ff4dd
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60105373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:740f5af31ca3b0f0b62e034adaae7a2c36d73038b8da8b7a58b2e25b25a4711a`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 10 Sep 2020 01:06:11 GMT
ADD file:4dede556abae88027bd22f3166fdbc38778a6fcd686c5ce768c3ca024ab3f9cf in / 
# Thu, 10 Sep 2020 01:06:20 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 18:54:59 GMT
ENV MONO_VERSION=6.8.0.123
# Thu, 10 Sep 2020 18:58:23 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 10 Sep 2020 19:00:53 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:f8aef3d2247e5f990bc767bc99f575b9bcec34aaa37183414eebe28fcd09519d`  
		Last Modified: Thu, 10 Sep 2020 01:28:12 GMT  
		Size: 30.5 MB (30517880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:693942962ba9930c35c80ccb1f1e3d6b8cf4ea69312000f87c7e70a8a583bd97`  
		Last Modified: Thu, 10 Sep 2020 19:41:53 GMT  
		Size: 256.3 KB (256333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed2a64806f5e29d588d2c7ba26ea2707bb2c9579d445ddcf7819f57344c4b54c`  
		Last Modified: Thu, 10 Sep 2020 19:42:03 GMT  
		Size: 29.3 MB (29331160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6-slim`

```console
$ docker pull mono@sha256:2908c04bb370f95935550b9fea10a6b96ca036ae71b32d17128402a624a327a2
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
$ docker pull mono@sha256:73fadf674046469a3fc25c496c1fb3ac58ad2eda9e26aa126e5479306ed0cf95
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94440255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9430b8012739f9826cdd9f118f69e95b47e049a35266f1c31f50002f1024fd57`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 10 Sep 2020 00:23:29 GMT
ADD file:e7407f2294ad23634565820b9669b18ff2a2ca0212a7ec84b9c89d8550859954 in / 
# Thu, 10 Sep 2020 00:23:30 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 06:19:25 GMT
ENV MONO_VERSION=6.10.0.104
# Thu, 10 Sep 2020 06:19:35 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 10 Sep 2020 06:20:13 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:d121f8d1c4128ebc1e95e5bfad90a0189b84eadbbb2fbaad20cbb26d20b2c8a2`  
		Last Modified: Thu, 10 Sep 2020 00:34:02 GMT  
		Size: 27.1 MB (27092161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:140dba57f56b96691dfd0551d17470bb5f21984005c4c372509a3cc39d8618ff`  
		Last Modified: Thu, 10 Sep 2020 06:39:36 GMT  
		Size: 255.9 KB (255922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad432be9d8d43b429c26f097fa65f3e8ce3af20bd0cff99c69f5ae3ba83d421b`  
		Last Modified: Thu, 10 Sep 2020 06:39:51 GMT  
		Size: 67.1 MB (67092172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:4f1935b74f258609d63b31cd01cabf54f735b72c77385b4d0486116f7b9ef1db
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51622580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8aaea1ec0574bca839c762a7724f248e6384ba44765e12d60a1eeb21f04760d2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Oct 2020 01:52:17 GMT
ADD file:b71c0fa4957d6b65af37231a105f3d17cdbafe5c7d6c37b5843ebf619c608aaa in / 
# Tue, 13 Oct 2020 01:52:27 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 02:36:19 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 13 Oct 2020 02:36:43 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 13 Oct 2020 02:37:31 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:f991c1e1ee2c48f16625b6b61310bf3c0616c0dbda4762019117e86fd29cf9ce`  
		Last Modified: Tue, 13 Oct 2020 02:01:27 GMT  
		Size: 24.8 MB (24835992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d27e131b9898d8f02267f410169b8627b889f6585ad9300d14a4775194301b55`  
		Last Modified: Tue, 13 Oct 2020 02:44:49 GMT  
		Size: 255.9 KB (255938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07b82cc14a51474e2d05a0fd59b3fde70aa8fda539de5a302992983e4ffce7b8`  
		Last Modified: Tue, 13 Oct 2020 02:45:01 GMT  
		Size: 26.5 MB (26530650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:bf61cbd2fff2e9323d1f89b46e33accc00aa6aef0f7f4ab533d44ff2d3672097
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48685097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4593f3eb7182d83642b75181ed79a20590556ea1d6460aef0cad9e805bef1e10`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Oct 2020 00:59:29 GMT
ADD file:e423f30ca19eb205a98de21b0545d0a764cfc4f832a9a9631542354d914d98d9 in / 
# Tue, 13 Oct 2020 00:59:31 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 04:43:09 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 13 Oct 2020 04:43:27 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 13 Oct 2020 04:44:11 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:d6d8411ad43db0022fa0fce094cd2e8b1dd2f8a09d6880ed9beb6b4204867027`  
		Last Modified: Tue, 13 Oct 2020 01:08:28 GMT  
		Size: 22.7 MB (22699849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5228b93feed3135603bc1b4bbda140b6e3e712167c9dd5ccaad1732370cd6b93`  
		Last Modified: Tue, 13 Oct 2020 04:50:37 GMT  
		Size: 255.9 KB (255921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4e85494910fa31cd3bb70be77361cab8fa0b333de462a10ce0e2181ee165c0a`  
		Last Modified: Tue, 13 Oct 2020 04:50:46 GMT  
		Size: 25.7 MB (25729327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:837debd8ec883ec2335ef1d2a49134236314f42b645ff3f6c7c3bba8edd39122
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.9 MB (57855412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a67ab8b67f587104f2fad4384a16c674fd915ee9365d079ff0007afd7fc611a6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 09 Sep 2020 23:50:54 GMT
ADD file:d870fb0484ea283840d9cc923c9c3fe36d1bb6b3b5ecfefcce06aa26a22c9414 in / 
# Wed, 09 Sep 2020 23:50:57 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 04:11:35 GMT
ENV MONO_VERSION=6.10.0.104
# Thu, 10 Sep 2020 04:11:50 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 10 Sep 2020 04:12:25 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a6d76de28f58f3470aff71c934c0fec4e5d0fad788f8b8bcc50601266fc1b34d`  
		Last Modified: Wed, 09 Sep 2020 23:59:09 GMT  
		Size: 25.8 MB (25849325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e6286cef3ccb7f414187d0d407d414d80aefc9cbac5f8afc8b61c2144468e9d`  
		Last Modified: Thu, 10 Sep 2020 04:18:37 GMT  
		Size: 255.9 KB (255919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2922d176e5f282d1cab4d82a18705798bb201e72254252e9365c6e6d79f9193`  
		Last Modified: Thu, 10 Sep 2020 04:18:47 GMT  
		Size: 31.8 MB (31750168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6-slim` - linux; 386

```console
$ docker pull mono@sha256:2a9fab669e67041d25fdb369e933e3590824683abc66c630331417cfc165ba14
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.1 MB (99142396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cc2e1b2ceaeba60abb7a332bf82875ce0709f9c94f0eda84ca9f39bc53f8b70`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 09 Sep 2020 23:40:19 GMT
ADD file:08dc20c9cd727ebf02cac6e4b287c3009274682174aee9222494491cd6c671b8 in / 
# Wed, 09 Sep 2020 23:40:19 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 02:37:15 GMT
ENV MONO_VERSION=6.10.0.104
# Thu, 10 Sep 2020 02:37:27 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 10 Sep 2020 02:38:12 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:31e6582dbd9f9a84903d46339df0c393a63d2cbfb001b06b3204653cceafcc61`  
		Last Modified: Wed, 09 Sep 2020 23:46:30 GMT  
		Size: 27.8 MB (27750334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10a5b4050174b76ed23d2d3bbb436d66899f93eba56641cd1faf810f75242c67`  
		Last Modified: Thu, 10 Sep 2020 02:44:13 GMT  
		Size: 255.8 KB (255795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a251d8984c7c93892d00e6d7ad246f6eb96eb1ccef85f2aa4931d99e3fa536d0`  
		Last Modified: Thu, 10 Sep 2020 02:44:42 GMT  
		Size: 71.1 MB (71136267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:0747d27029d283c5d079fd0b849b546bb95eeae5adf789b192f20a6714a1f523
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60124211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60fa8a532fd76be8dc5c2045033500043c8b1d5a968372c9b52cfd0f3819eb3e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 10 Sep 2020 01:06:11 GMT
ADD file:4dede556abae88027bd22f3166fdbc38778a6fcd686c5ce768c3ca024ab3f9cf in / 
# Thu, 10 Sep 2020 01:06:20 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 19:01:16 GMT
ENV MONO_VERSION=6.10.0.104
# Thu, 10 Sep 2020 19:05:10 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 10 Sep 2020 19:07:24 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:f8aef3d2247e5f990bc767bc99f575b9bcec34aaa37183414eebe28fcd09519d`  
		Last Modified: Thu, 10 Sep 2020 01:28:12 GMT  
		Size: 30.5 MB (30517880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91a5b381ce455eca298e810bbcff286cc9167c82392b00241d01cc6bc65cfe86`  
		Last Modified: Thu, 10 Sep 2020 19:42:19 GMT  
		Size: 256.3 KB (256260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3df1215b828b18d641c32013a7c8597874acf4085e9fc7b404d9216a5e67ecc3`  
		Last Modified: Thu, 10 Sep 2020 19:42:28 GMT  
		Size: 29.4 MB (29350071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:latest`

```console
$ docker pull mono@sha256:51c78c2462224a085af0bc077f69420ee58ded25392f96b396fc84999767b360
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
$ docker pull mono@sha256:8ddb0aa61e691c3e02dc60e6d9d37d48c9adbdcf96690d4e3b0e1f157d864f0c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.7 MB (224730258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e643114dd794dcb7b32b4cebb995622e6404e198c2698b435be26a772765604`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 10 Sep 2020 00:23:29 GMT
ADD file:e7407f2294ad23634565820b9669b18ff2a2ca0212a7ec84b9c89d8550859954 in / 
# Thu, 10 Sep 2020 00:23:30 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 06:19:25 GMT
ENV MONO_VERSION=6.10.0.104
# Thu, 10 Sep 2020 06:19:35 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 10 Sep 2020 06:20:13 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 10 Sep 2020 06:38:36 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:d121f8d1c4128ebc1e95e5bfad90a0189b84eadbbb2fbaad20cbb26d20b2c8a2`  
		Last Modified: Thu, 10 Sep 2020 00:34:02 GMT  
		Size: 27.1 MB (27092161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:140dba57f56b96691dfd0551d17470bb5f21984005c4c372509a3cc39d8618ff`  
		Last Modified: Thu, 10 Sep 2020 06:39:36 GMT  
		Size: 255.9 KB (255922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad432be9d8d43b429c26f097fa65f3e8ce3af20bd0cff99c69f5ae3ba83d421b`  
		Last Modified: Thu, 10 Sep 2020 06:39:51 GMT  
		Size: 67.1 MB (67092172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:647a8876e15683db1ea6901f3102f72d4b0cd4a6f92f4321d25cdd9410e6acf0`  
		Last Modified: Thu, 10 Sep 2020 06:41:41 GMT  
		Size: 130.3 MB (130290003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:latest` - linux; arm variant v5

```console
$ docker pull mono@sha256:3e601afbb4577fd538dfa06145643ef0c370d3b98b7fdbdeb8e69e6e7c3cc44b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.6 MB (180580641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0b1583a0f54587294ef3fb13293551714e84d35168baa3b742491aac91dc394`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Oct 2020 01:52:17 GMT
ADD file:b71c0fa4957d6b65af37231a105f3d17cdbafe5c7d6c37b5843ebf619c608aaa in / 
# Tue, 13 Oct 2020 01:52:27 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 02:36:19 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 13 Oct 2020 02:36:43 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 13 Oct 2020 02:37:31 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 13 Oct 2020 02:44:00 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:f991c1e1ee2c48f16625b6b61310bf3c0616c0dbda4762019117e86fd29cf9ce`  
		Last Modified: Tue, 13 Oct 2020 02:01:27 GMT  
		Size: 24.8 MB (24835992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d27e131b9898d8f02267f410169b8627b889f6585ad9300d14a4775194301b55`  
		Last Modified: Tue, 13 Oct 2020 02:44:49 GMT  
		Size: 255.9 KB (255938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07b82cc14a51474e2d05a0fd59b3fde70aa8fda539de5a302992983e4ffce7b8`  
		Last Modified: Tue, 13 Oct 2020 02:45:01 GMT  
		Size: 26.5 MB (26530650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f94ad0d9899e6c5c16486a97103eb9bbff1261c084ef2366534ae27653b23704`  
		Last Modified: Tue, 13 Oct 2020 02:46:59 GMT  
		Size: 129.0 MB (128958061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:latest` - linux; arm variant v7

```console
$ docker pull mono@sha256:0e797969122f94b85e9178dd9bece13c7ebd2cacf124520f4275e0ac7cd2b15d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.5 MB (176483530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b81a3bb43255d115e920754f87906a5cd00c5c5ae23a85f06c756f2c42a455b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Oct 2020 00:59:29 GMT
ADD file:e423f30ca19eb205a98de21b0545d0a764cfc4f832a9a9631542354d914d98d9 in / 
# Tue, 13 Oct 2020 00:59:31 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 04:43:09 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 13 Oct 2020 04:43:27 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 13 Oct 2020 04:44:11 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 13 Oct 2020 04:49:53 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:d6d8411ad43db0022fa0fce094cd2e8b1dd2f8a09d6880ed9beb6b4204867027`  
		Last Modified: Tue, 13 Oct 2020 01:08:28 GMT  
		Size: 22.7 MB (22699849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5228b93feed3135603bc1b4bbda140b6e3e712167c9dd5ccaad1732370cd6b93`  
		Last Modified: Tue, 13 Oct 2020 04:50:37 GMT  
		Size: 255.9 KB (255921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4e85494910fa31cd3bb70be77361cab8fa0b333de462a10ce0e2181ee165c0a`  
		Last Modified: Tue, 13 Oct 2020 04:50:46 GMT  
		Size: 25.7 MB (25729327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c0179ccf237338944b3401bc8ed480a53bd10956472cd41d05647aeb7fa46ee`  
		Last Modified: Tue, 13 Oct 2020 04:52:43 GMT  
		Size: 127.8 MB (127798433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:latest` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:aed137508847cbf4f9a780482c89ec7185a4925bb21c49455867253f783b3756
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.3 MB (203294488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:932c2fe803dcfd13acda14b21319c3cc542c19c177c473ab3a72d42ec87c407a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 09 Sep 2020 23:50:54 GMT
ADD file:d870fb0484ea283840d9cc923c9c3fe36d1bb6b3b5ecfefcce06aa26a22c9414 in / 
# Wed, 09 Sep 2020 23:50:57 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 04:11:35 GMT
ENV MONO_VERSION=6.10.0.104
# Thu, 10 Sep 2020 04:11:50 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 10 Sep 2020 04:12:25 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 10 Sep 2020 04:17:44 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a6d76de28f58f3470aff71c934c0fec4e5d0fad788f8b8bcc50601266fc1b34d`  
		Last Modified: Wed, 09 Sep 2020 23:59:09 GMT  
		Size: 25.8 MB (25849325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e6286cef3ccb7f414187d0d407d414d80aefc9cbac5f8afc8b61c2144468e9d`  
		Last Modified: Thu, 10 Sep 2020 04:18:37 GMT  
		Size: 255.9 KB (255919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2922d176e5f282d1cab4d82a18705798bb201e72254252e9365c6e6d79f9193`  
		Last Modified: Thu, 10 Sep 2020 04:18:47 GMT  
		Size: 31.8 MB (31750168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:516e789eeddd8a9df62f3440c69b597818ad508f4cef3e636f2c25150e64e036`  
		Last Modified: Thu, 10 Sep 2020 04:20:35 GMT  
		Size: 145.4 MB (145439076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:latest` - linux; 386

```console
$ docker pull mono@sha256:d111852f67f667bb664ca166bcaf57863be573e5f9abcf640261a13ce768af9f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.5 MB (230534575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c670b9156ca83df138822e88a059b2ef4b85870178733601534fdb68cc075916`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 09 Sep 2020 23:40:19 GMT
ADD file:08dc20c9cd727ebf02cac6e4b287c3009274682174aee9222494491cd6c671b8 in / 
# Wed, 09 Sep 2020 23:40:19 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 02:37:15 GMT
ENV MONO_VERSION=6.10.0.104
# Thu, 10 Sep 2020 02:37:27 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 10 Sep 2020 02:38:12 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 10 Sep 2020 02:43:19 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:31e6582dbd9f9a84903d46339df0c393a63d2cbfb001b06b3204653cceafcc61`  
		Last Modified: Wed, 09 Sep 2020 23:46:30 GMT  
		Size: 27.8 MB (27750334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10a5b4050174b76ed23d2d3bbb436d66899f93eba56641cd1faf810f75242c67`  
		Last Modified: Thu, 10 Sep 2020 02:44:13 GMT  
		Size: 255.8 KB (255795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a251d8984c7c93892d00e6d7ad246f6eb96eb1ccef85f2aa4931d99e3fa536d0`  
		Last Modified: Thu, 10 Sep 2020 02:44:42 GMT  
		Size: 71.1 MB (71136267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:977fb5b989bb54968bfa64f742226d8805f4ec1552243874881f524b81fb29ae`  
		Last Modified: Thu, 10 Sep 2020 02:46:21 GMT  
		Size: 131.4 MB (131392179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:latest` - linux; ppc64le

```console
$ docker pull mono@sha256:b8c551764ab121348d5a5b162b12f0b2a502a49198c74891cdd0c24e8cb6edb1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.1 MB (192085402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:986fc10b226d2b7a4e6847eb4e4451f452b95bad5fb31f38f99795e2fae34446`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 10 Sep 2020 01:06:11 GMT
ADD file:4dede556abae88027bd22f3166fdbc38778a6fcd686c5ce768c3ca024ab3f9cf in / 
# Thu, 10 Sep 2020 01:06:20 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 19:01:16 GMT
ENV MONO_VERSION=6.10.0.104
# Thu, 10 Sep 2020 19:05:10 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 10 Sep 2020 19:07:24 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 10 Sep 2020 19:41:11 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:f8aef3d2247e5f990bc767bc99f575b9bcec34aaa37183414eebe28fcd09519d`  
		Last Modified: Thu, 10 Sep 2020 01:28:12 GMT  
		Size: 30.5 MB (30517880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91a5b381ce455eca298e810bbcff286cc9167c82392b00241d01cc6bc65cfe86`  
		Last Modified: Thu, 10 Sep 2020 19:42:19 GMT  
		Size: 256.3 KB (256260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3df1215b828b18d641c32013a7c8597874acf4085e9fc7b404d9216a5e67ecc3`  
		Last Modified: Thu, 10 Sep 2020 19:42:28 GMT  
		Size: 29.4 MB (29350071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96ac3143de444eb2aa16dc11160d058e94b7f635cfc9b210a3438a1535c643b1`  
		Last Modified: Thu, 10 Sep 2020 19:44:16 GMT  
		Size: 132.0 MB (131961191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:slim`

```console
$ docker pull mono@sha256:2908c04bb370f95935550b9fea10a6b96ca036ae71b32d17128402a624a327a2
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
$ docker pull mono@sha256:73fadf674046469a3fc25c496c1fb3ac58ad2eda9e26aa126e5479306ed0cf95
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94440255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9430b8012739f9826cdd9f118f69e95b47e049a35266f1c31f50002f1024fd57`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 10 Sep 2020 00:23:29 GMT
ADD file:e7407f2294ad23634565820b9669b18ff2a2ca0212a7ec84b9c89d8550859954 in / 
# Thu, 10 Sep 2020 00:23:30 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 06:19:25 GMT
ENV MONO_VERSION=6.10.0.104
# Thu, 10 Sep 2020 06:19:35 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 10 Sep 2020 06:20:13 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:d121f8d1c4128ebc1e95e5bfad90a0189b84eadbbb2fbaad20cbb26d20b2c8a2`  
		Last Modified: Thu, 10 Sep 2020 00:34:02 GMT  
		Size: 27.1 MB (27092161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:140dba57f56b96691dfd0551d17470bb5f21984005c4c372509a3cc39d8618ff`  
		Last Modified: Thu, 10 Sep 2020 06:39:36 GMT  
		Size: 255.9 KB (255922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad432be9d8d43b429c26f097fa65f3e8ce3af20bd0cff99c69f5ae3ba83d421b`  
		Last Modified: Thu, 10 Sep 2020 06:39:51 GMT  
		Size: 67.1 MB (67092172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:4f1935b74f258609d63b31cd01cabf54f735b72c77385b4d0486116f7b9ef1db
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51622580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8aaea1ec0574bca839c762a7724f248e6384ba44765e12d60a1eeb21f04760d2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Oct 2020 01:52:17 GMT
ADD file:b71c0fa4957d6b65af37231a105f3d17cdbafe5c7d6c37b5843ebf619c608aaa in / 
# Tue, 13 Oct 2020 01:52:27 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 02:36:19 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 13 Oct 2020 02:36:43 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 13 Oct 2020 02:37:31 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:f991c1e1ee2c48f16625b6b61310bf3c0616c0dbda4762019117e86fd29cf9ce`  
		Last Modified: Tue, 13 Oct 2020 02:01:27 GMT  
		Size: 24.8 MB (24835992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d27e131b9898d8f02267f410169b8627b889f6585ad9300d14a4775194301b55`  
		Last Modified: Tue, 13 Oct 2020 02:44:49 GMT  
		Size: 255.9 KB (255938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07b82cc14a51474e2d05a0fd59b3fde70aa8fda539de5a302992983e4ffce7b8`  
		Last Modified: Tue, 13 Oct 2020 02:45:01 GMT  
		Size: 26.5 MB (26530650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:bf61cbd2fff2e9323d1f89b46e33accc00aa6aef0f7f4ab533d44ff2d3672097
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48685097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4593f3eb7182d83642b75181ed79a20590556ea1d6460aef0cad9e805bef1e10`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Oct 2020 00:59:29 GMT
ADD file:e423f30ca19eb205a98de21b0545d0a764cfc4f832a9a9631542354d914d98d9 in / 
# Tue, 13 Oct 2020 00:59:31 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 04:43:09 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 13 Oct 2020 04:43:27 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 13 Oct 2020 04:44:11 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:d6d8411ad43db0022fa0fce094cd2e8b1dd2f8a09d6880ed9beb6b4204867027`  
		Last Modified: Tue, 13 Oct 2020 01:08:28 GMT  
		Size: 22.7 MB (22699849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5228b93feed3135603bc1b4bbda140b6e3e712167c9dd5ccaad1732370cd6b93`  
		Last Modified: Tue, 13 Oct 2020 04:50:37 GMT  
		Size: 255.9 KB (255921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4e85494910fa31cd3bb70be77361cab8fa0b333de462a10ce0e2181ee165c0a`  
		Last Modified: Tue, 13 Oct 2020 04:50:46 GMT  
		Size: 25.7 MB (25729327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:837debd8ec883ec2335ef1d2a49134236314f42b645ff3f6c7c3bba8edd39122
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.9 MB (57855412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a67ab8b67f587104f2fad4384a16c674fd915ee9365d079ff0007afd7fc611a6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 09 Sep 2020 23:50:54 GMT
ADD file:d870fb0484ea283840d9cc923c9c3fe36d1bb6b3b5ecfefcce06aa26a22c9414 in / 
# Wed, 09 Sep 2020 23:50:57 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 04:11:35 GMT
ENV MONO_VERSION=6.10.0.104
# Thu, 10 Sep 2020 04:11:50 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 10 Sep 2020 04:12:25 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a6d76de28f58f3470aff71c934c0fec4e5d0fad788f8b8bcc50601266fc1b34d`  
		Last Modified: Wed, 09 Sep 2020 23:59:09 GMT  
		Size: 25.8 MB (25849325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e6286cef3ccb7f414187d0d407d414d80aefc9cbac5f8afc8b61c2144468e9d`  
		Last Modified: Thu, 10 Sep 2020 04:18:37 GMT  
		Size: 255.9 KB (255919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2922d176e5f282d1cab4d82a18705798bb201e72254252e9365c6e6d79f9193`  
		Last Modified: Thu, 10 Sep 2020 04:18:47 GMT  
		Size: 31.8 MB (31750168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:slim` - linux; 386

```console
$ docker pull mono@sha256:2a9fab669e67041d25fdb369e933e3590824683abc66c630331417cfc165ba14
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.1 MB (99142396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cc2e1b2ceaeba60abb7a332bf82875ce0709f9c94f0eda84ca9f39bc53f8b70`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 09 Sep 2020 23:40:19 GMT
ADD file:08dc20c9cd727ebf02cac6e4b287c3009274682174aee9222494491cd6c671b8 in / 
# Wed, 09 Sep 2020 23:40:19 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 02:37:15 GMT
ENV MONO_VERSION=6.10.0.104
# Thu, 10 Sep 2020 02:37:27 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 10 Sep 2020 02:38:12 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:31e6582dbd9f9a84903d46339df0c393a63d2cbfb001b06b3204653cceafcc61`  
		Last Modified: Wed, 09 Sep 2020 23:46:30 GMT  
		Size: 27.8 MB (27750334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10a5b4050174b76ed23d2d3bbb436d66899f93eba56641cd1faf810f75242c67`  
		Last Modified: Thu, 10 Sep 2020 02:44:13 GMT  
		Size: 255.8 KB (255795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a251d8984c7c93892d00e6d7ad246f6eb96eb1ccef85f2aa4931d99e3fa536d0`  
		Last Modified: Thu, 10 Sep 2020 02:44:42 GMT  
		Size: 71.1 MB (71136267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:slim` - linux; ppc64le

```console
$ docker pull mono@sha256:0747d27029d283c5d079fd0b849b546bb95eeae5adf789b192f20a6714a1f523
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60124211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60fa8a532fd76be8dc5c2045033500043c8b1d5a968372c9b52cfd0f3819eb3e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 10 Sep 2020 01:06:11 GMT
ADD file:4dede556abae88027bd22f3166fdbc38778a6fcd686c5ce768c3ca024ab3f9cf in / 
# Thu, 10 Sep 2020 01:06:20 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 19:01:16 GMT
ENV MONO_VERSION=6.10.0.104
# Thu, 10 Sep 2020 19:05:10 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 10 Sep 2020 19:07:24 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:f8aef3d2247e5f990bc767bc99f575b9bcec34aaa37183414eebe28fcd09519d`  
		Last Modified: Thu, 10 Sep 2020 01:28:12 GMT  
		Size: 30.5 MB (30517880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91a5b381ce455eca298e810bbcff286cc9167c82392b00241d01cc6bc65cfe86`  
		Last Modified: Thu, 10 Sep 2020 19:42:19 GMT  
		Size: 256.3 KB (256260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3df1215b828b18d641c32013a7c8597874acf4085e9fc7b404d9216a5e67ecc3`  
		Last Modified: Thu, 10 Sep 2020 19:42:28 GMT  
		Size: 29.4 MB (29350071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
