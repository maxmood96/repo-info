<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `mono`

-	[`mono:6`](#mono6)
-	[`mono:6-slim`](#mono6-slim)
-	[`mono:6.10`](#mono610)
-	[`mono:6.10-slim`](#mono610-slim)
-	[`mono:6.10.0`](#mono6100)
-	[`mono:6.10.0-slim`](#mono6100-slim)
-	[`mono:6.10.0.104`](#mono6100104)
-	[`mono:6.10.0.104-slim`](#mono6100104-slim)
-	[`mono:6.12`](#mono612)
-	[`mono:6.12-slim`](#mono612-slim)
-	[`mono:6.12.0`](#mono6120)
-	[`mono:6.12.0-slim`](#mono6120-slim)
-	[`mono:6.12.0.122`](#mono6120122)
-	[`mono:6.12.0.122-slim`](#mono6120122-slim)
-	[`mono:latest`](#monolatest)
-	[`mono:slim`](#monoslim)

## `mono:6`

```console
$ docker pull mono@sha256:b04d988ca0c1985b75f30422238cd0cf6cac7030e8492117b2ea2fd25194f6a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:6` - linux; amd64

```console
$ docker pull mono@sha256:481fce9886677b30abb23cf0b1aa5d477482a89b02f1207d0ef6cd6f462357bf
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.1 MB (236118149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0973a336ea5cc60790a8d4d304b05ddb030fea89166482e2d2372c9b1d6abf1e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:21:02 GMT
ADD file:3c54ad257f2e04f7294ce879b884820cf4726c8e93ec548172825963e40c79ad in / 
# Wed, 17 Nov 2021 02:21:02 GMT
CMD ["bash"]
# Tue, 23 Nov 2021 22:35:14 GMT
ENV MONO_VERSION=6.12.0.122
# Tue, 23 Nov 2021 22:35:29 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 23 Nov 2021 22:35:48 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 23 Nov 2021 22:41:26 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a10c77af261312e7c92bcc184f2d1726175ff7f142e44b01c5779cd79348b9fd`  
		Last Modified: Wed, 17 Nov 2021 02:26:31 GMT  
		Size: 27.2 MB (27153675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:290db4dba8dd1a22feca175d2300b4ca8dd16fe86ecc6022a566329a5b654ecf`  
		Last Modified: Tue, 23 Nov 2021 22:48:37 GMT  
		Size: 2.8 MB (2766933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbb78a53a304279c9bb401cfd5979e972f8fc1e746e9d36fc42525cd0676e372`  
		Last Modified: Tue, 23 Nov 2021 22:48:50 GMT  
		Size: 64.8 MB (64759889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b2ee3bb2622395bc301b422eccf0178ef24425f0fbd2392e582b3858628472c`  
		Last Modified: Tue, 23 Nov 2021 22:49:59 GMT  
		Size: 141.4 MB (141437652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6` - linux; arm variant v5

```console
$ docker pull mono@sha256:32c6613aba67088647674775dc9bc4936d1495cf10902d45fc8f51eb726a6a9c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.9 MB (191928998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4777f90f93be6f3b59383b98fa7e7ae724fadac57fde9062cba89d56d422826`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:51:39 GMT
ADD file:e580d4d2066301375327ea51dd8db3af956e5a465495bf09d69d6deec9b0bfae in / 
# Wed, 17 Nov 2021 02:51:40 GMT
CMD ["bash"]
# Tue, 23 Nov 2021 21:57:24 GMT
ENV MONO_VERSION=6.12.0.122
# Tue, 23 Nov 2021 21:57:55 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 23 Nov 2021 21:58:42 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 23 Nov 2021 22:03:49 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:dba255a4b166bb02562ca152d0da236ba8f211de5bf9d79e35ee023b1fce203e`  
		Last Modified: Wed, 17 Nov 2021 03:07:41 GMT  
		Size: 24.9 MB (24886310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01af261a6c29946e34b32228d294c69a86ca06cdfd0b0cfafbb568e9fc6b57b3`  
		Last Modified: Tue, 23 Nov 2021 22:08:39 GMT  
		Size: 2.5 MB (2462561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c562f4f3fb32ceeded7f153ed48a677c98f4efaee9d19ed32a8fcfa7fe236b27`  
		Last Modified: Tue, 23 Nov 2021 22:08:52 GMT  
		Size: 24.5 MB (24493189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6142af18d42fb857ff86fc8a7f00fbd715e0d8db30845d2424ff947cd9058276`  
		Last Modified: Tue, 23 Nov 2021 22:11:15 GMT  
		Size: 140.1 MB (140086938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6` - linux; arm variant v7

```console
$ docker pull mono@sha256:224100530ddf0867a699f0e1448fd2646c62e088c97bbe9fea0cfa488e8813c4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.8 MB (187845574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a6b45021de699193ede4308d6e2ae5eb2cc57e8def386c8a6e60d7a52c2c704`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:00:46 GMT
ADD file:4ac0de0d740f0c221cd4f912861a67009942fa5bdad24ac8b62c690dfa15024a in / 
# Wed, 17 Nov 2021 02:00:47 GMT
CMD ["bash"]
# Tue, 23 Nov 2021 22:28:21 GMT
ENV MONO_VERSION=6.12.0.122
# Tue, 23 Nov 2021 22:28:52 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 23 Nov 2021 22:29:35 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 23 Nov 2021 22:34:09 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7bd9e64406c6f3044bd15f89c367f07ec4eaafb1035a5c3ee2f7b138be68017f`  
		Last Modified: Wed, 17 Nov 2021 02:16:39 GMT  
		Size: 22.8 MB (22754359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:049b685383367eaa00b28d290b7f521588cc2a6fddec236420129ec04830f7ad`  
		Last Modified: Tue, 23 Nov 2021 22:38:55 GMT  
		Size: 2.4 MB (2361954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d696071cf20a8d6e7031e1c8c4453e1fcbd73fbd07d0e299ab428402906f012c`  
		Last Modified: Tue, 23 Nov 2021 22:39:06 GMT  
		Size: 23.8 MB (23782697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f919fba63d40094ff8de7041bdf8ea1ea33c8fb98dec1524acc0ddb1c7144658`  
		Last Modified: Tue, 23 Nov 2021 22:41:39 GMT  
		Size: 138.9 MB (138946564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:f51c87edd3a0bb05ecb545084c025665f2a4cc4c47b21b9fd7bd712ac9c8fd4b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.5 MB (214451528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32097382767f78b6abfadcb70f6979c659ec28225f0c64f08bdd820d4cb582f9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:40:44 GMT
ADD file:b7921dd77c7620d46a18a4b5952557620210bf7ad9de20fe8e695a371188122a in / 
# Wed, 17 Nov 2021 02:40:44 GMT
CMD ["bash"]
# Tue, 23 Nov 2021 21:51:44 GMT
ENV MONO_VERSION=6.12.0.122
# Tue, 23 Nov 2021 21:51:59 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 23 Nov 2021 21:52:15 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 23 Nov 2021 21:54:06 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:8ccb9871ed7bebcea8889b08e06fe5bd0116711ca7b110429b987475bf4d40e8`  
		Last Modified: Wed, 17 Nov 2021 02:48:07 GMT  
		Size: 25.9 MB (25923117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9d1d375755ac6c8647c886eb68f427d617cb789ae0c98372e585311a5395aa0`  
		Last Modified: Tue, 23 Nov 2021 21:57:01 GMT  
		Size: 2.6 MB (2634589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a5575918894c723f49db7b67bad957b34f1f6b88828b67489943f4618f2fdc4`  
		Last Modified: Tue, 23 Nov 2021 21:57:05 GMT  
		Size: 29.3 MB (29318238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ec24743e7bc80a3baec7c0697b8bd9d87e12e26d3c50e6d7e18c36dd63bd005`  
		Last Modified: Tue, 23 Nov 2021 21:58:08 GMT  
		Size: 156.6 MB (156575584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6` - linux; 386

```console
$ docker pull mono@sha256:487eab41ead5858f6e434ae442e99515059f95651604e49d867d41095e05f2eb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.9 MB (241920178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f058eee97b6682f2e4715db0d188185468cddc542f881b8053c7b1fbaf4567e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:40:22 GMT
ADD file:2adea3474b7ebda2bf77361304ee3e6966a9118aafd8220b81c4027be1f4d583 in / 
# Wed, 17 Nov 2021 02:40:22 GMT
CMD ["bash"]
# Tue, 23 Nov 2021 21:42:03 GMT
ENV MONO_VERSION=6.12.0.122
# Tue, 23 Nov 2021 21:42:22 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 23 Nov 2021 21:42:48 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 23 Nov 2021 21:44:49 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7af5c9e671306e395c50a515c7bbe33d6f418ea08535b01c884457f78114eb08`  
		Last Modified: Wed, 17 Nov 2021 02:48:49 GMT  
		Size: 27.8 MB (27804550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:178b44cff3441bdb1ada9b30fbb42c9e7143127e42b7e4715f38610b2d122927`  
		Last Modified: Tue, 23 Nov 2021 21:47:45 GMT  
		Size: 2.8 MB (2781502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b82f010a190c7a767fdbe0299862791645a573a4844487ee187efe7e6a34941`  
		Last Modified: Tue, 23 Nov 2021 21:47:59 GMT  
		Size: 68.8 MB (68778522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7c603a243c2c3d8943de83d6e0d8a8eaba5b511e76a1b921dcb9b576ef046b7`  
		Last Modified: Tue, 23 Nov 2021 21:49:18 GMT  
		Size: 142.6 MB (142555604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6` - linux; ppc64le

```console
$ docker pull mono@sha256:58c35decefee6c034da009565f9e354b1d3f0defbba53730df12f3cde2aeaeab
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.4 MB (203412519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99b8277a5b9fc92177d5f86fa33e2ff383ae55de6452afe5b1dd0d9215ba5f46`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Oct 2021 01:26:46 GMT
ADD file:5526880c6f19a4b4231a8b2bd7cfc625d116764c4918eff6f0b55f8c1eb38e1a in / 
# Tue, 12 Oct 2021 01:26:50 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 07:07:14 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 12 Oct 2021 07:08:29 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 12 Oct 2021 07:10:10 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 12 Oct 2021 07:21:13 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:d69973af32573c07c8789c0f9c144a5c0b822a1e85b59db3ce9f8ebc489ce85d`  
		Last Modified: Tue, 12 Oct 2021 01:38:40 GMT  
		Size: 30.5 MB (30547197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:411a4d07ce6468d0126e5f9f0ad6098034f004bb482027b2349909c0ebc277d4`  
		Last Modified: Tue, 12 Oct 2021 07:31:06 GMT  
		Size: 256.1 KB (256142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa7805400cade2c3fda94906cc3502961f0a85bf26f07aeb6d74f4ba6866961b`  
		Last Modified: Tue, 12 Oct 2021 07:31:12 GMT  
		Size: 29.4 MB (29359244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5bfdf96e676582679b152400f854a0a0c03af4dcd5f3abd6c9afc2068238061`  
		Last Modified: Tue, 12 Oct 2021 07:32:19 GMT  
		Size: 143.2 MB (143249936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6-slim`

```console
$ docker pull mono@sha256:9d4ba66e353e699a1e0d2970e87b39e26cd619d3103cab57e29968c1a62c0c1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:6-slim` - linux; amd64

```console
$ docker pull mono@sha256:cdecd1e409a3bf015b2df7cab751b32aa1912942800c38c26dbbda077bd24a1d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.7 MB (94680497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:179c410963b2d950b30018aa2f7198d4bbf4750a44af79963bc2ec7eb619a78a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:21:02 GMT
ADD file:3c54ad257f2e04f7294ce879b884820cf4726c8e93ec548172825963e40c79ad in / 
# Wed, 17 Nov 2021 02:21:02 GMT
CMD ["bash"]
# Tue, 23 Nov 2021 22:35:14 GMT
ENV MONO_VERSION=6.12.0.122
# Tue, 23 Nov 2021 22:35:29 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 23 Nov 2021 22:35:48 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a10c77af261312e7c92bcc184f2d1726175ff7f142e44b01c5779cd79348b9fd`  
		Last Modified: Wed, 17 Nov 2021 02:26:31 GMT  
		Size: 27.2 MB (27153675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:290db4dba8dd1a22feca175d2300b4ca8dd16fe86ecc6022a566329a5b654ecf`  
		Last Modified: Tue, 23 Nov 2021 22:48:37 GMT  
		Size: 2.8 MB (2766933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbb78a53a304279c9bb401cfd5979e972f8fc1e746e9d36fc42525cd0676e372`  
		Last Modified: Tue, 23 Nov 2021 22:48:50 GMT  
		Size: 64.8 MB (64759889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:56e40b4d67adf3a932be68db6867706afb08420aa4ec4d1ce823c62f6369ca0a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51842060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76c279d60b298986449ea01c00551166b76185c559f47d494efc568cf54ea1c6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:51:39 GMT
ADD file:e580d4d2066301375327ea51dd8db3af956e5a465495bf09d69d6deec9b0bfae in / 
# Wed, 17 Nov 2021 02:51:40 GMT
CMD ["bash"]
# Tue, 23 Nov 2021 21:57:24 GMT
ENV MONO_VERSION=6.12.0.122
# Tue, 23 Nov 2021 21:57:55 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 23 Nov 2021 21:58:42 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:dba255a4b166bb02562ca152d0da236ba8f211de5bf9d79e35ee023b1fce203e`  
		Last Modified: Wed, 17 Nov 2021 03:07:41 GMT  
		Size: 24.9 MB (24886310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01af261a6c29946e34b32228d294c69a86ca06cdfd0b0cfafbb568e9fc6b57b3`  
		Last Modified: Tue, 23 Nov 2021 22:08:39 GMT  
		Size: 2.5 MB (2462561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c562f4f3fb32ceeded7f153ed48a677c98f4efaee9d19ed32a8fcfa7fe236b27`  
		Last Modified: Tue, 23 Nov 2021 22:08:52 GMT  
		Size: 24.5 MB (24493189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:abbc7a96a87a8fc3a75f3f9ee465f954103af6cb8caeeb2a58dcfa5775d9a5a6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48899010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:888f04b4468fa13c7dd2d4d3e6758e38cd6a1f2b8743d602ea8d6170470bc53f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:00:46 GMT
ADD file:4ac0de0d740f0c221cd4f912861a67009942fa5bdad24ac8b62c690dfa15024a in / 
# Wed, 17 Nov 2021 02:00:47 GMT
CMD ["bash"]
# Tue, 23 Nov 2021 22:28:21 GMT
ENV MONO_VERSION=6.12.0.122
# Tue, 23 Nov 2021 22:28:52 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 23 Nov 2021 22:29:35 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7bd9e64406c6f3044bd15f89c367f07ec4eaafb1035a5c3ee2f7b138be68017f`  
		Last Modified: Wed, 17 Nov 2021 02:16:39 GMT  
		Size: 22.8 MB (22754359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:049b685383367eaa00b28d290b7f521588cc2a6fddec236420129ec04830f7ad`  
		Last Modified: Tue, 23 Nov 2021 22:38:55 GMT  
		Size: 2.4 MB (2361954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d696071cf20a8d6e7031e1c8c4453e1fcbd73fbd07d0e299ab428402906f012c`  
		Last Modified: Tue, 23 Nov 2021 22:39:06 GMT  
		Size: 23.8 MB (23782697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:c8b6095166e5103eaa00541e4c8296a5082fc22f8b0c47f22b68524841854dda
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.9 MB (57875944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d2788a0d6a78feae4f3714b45819c05d06a535d1d2cd624e9cdb52386b96ff3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:40:44 GMT
ADD file:b7921dd77c7620d46a18a4b5952557620210bf7ad9de20fe8e695a371188122a in / 
# Wed, 17 Nov 2021 02:40:44 GMT
CMD ["bash"]
# Tue, 23 Nov 2021 21:51:44 GMT
ENV MONO_VERSION=6.12.0.122
# Tue, 23 Nov 2021 21:51:59 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 23 Nov 2021 21:52:15 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:8ccb9871ed7bebcea8889b08e06fe5bd0116711ca7b110429b987475bf4d40e8`  
		Last Modified: Wed, 17 Nov 2021 02:48:07 GMT  
		Size: 25.9 MB (25923117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9d1d375755ac6c8647c886eb68f427d617cb789ae0c98372e585311a5395aa0`  
		Last Modified: Tue, 23 Nov 2021 21:57:01 GMT  
		Size: 2.6 MB (2634589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a5575918894c723f49db7b67bad957b34f1f6b88828b67489943f4618f2fdc4`  
		Last Modified: Tue, 23 Nov 2021 21:57:05 GMT  
		Size: 29.3 MB (29318238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6-slim` - linux; 386

```console
$ docker pull mono@sha256:d5c218c6f846f064e3d68efb7e677d60a558d54067c13fe5a9554b1b6d2b8bdd
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.4 MB (99364574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2145d963dc4718d45ccb94e26a0153de7d7f1ee66964d3607401681ae010517d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:40:22 GMT
ADD file:2adea3474b7ebda2bf77361304ee3e6966a9118aafd8220b81c4027be1f4d583 in / 
# Wed, 17 Nov 2021 02:40:22 GMT
CMD ["bash"]
# Tue, 23 Nov 2021 21:42:03 GMT
ENV MONO_VERSION=6.12.0.122
# Tue, 23 Nov 2021 21:42:22 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 23 Nov 2021 21:42:48 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7af5c9e671306e395c50a515c7bbe33d6f418ea08535b01c884457f78114eb08`  
		Last Modified: Wed, 17 Nov 2021 02:48:49 GMT  
		Size: 27.8 MB (27804550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:178b44cff3441bdb1ada9b30fbb42c9e7143127e42b7e4715f38610b2d122927`  
		Last Modified: Tue, 23 Nov 2021 21:47:45 GMT  
		Size: 2.8 MB (2781502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b82f010a190c7a767fdbe0299862791645a573a4844487ee187efe7e6a34941`  
		Last Modified: Tue, 23 Nov 2021 21:47:59 GMT  
		Size: 68.8 MB (68778522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:7834ad815013a312211d9f24df0f88d7e3f04386d7c192b726662658029697f7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60162583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ee89c05071148752e8c61c25ab1424ba5b066d04b57a4f785fa443265cf2703`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Oct 2021 01:26:46 GMT
ADD file:5526880c6f19a4b4231a8b2bd7cfc625d116764c4918eff6f0b55f8c1eb38e1a in / 
# Tue, 12 Oct 2021 01:26:50 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 07:07:14 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 12 Oct 2021 07:08:29 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 12 Oct 2021 07:10:10 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:d69973af32573c07c8789c0f9c144a5c0b822a1e85b59db3ce9f8ebc489ce85d`  
		Last Modified: Tue, 12 Oct 2021 01:38:40 GMT  
		Size: 30.5 MB (30547197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:411a4d07ce6468d0126e5f9f0ad6098034f004bb482027b2349909c0ebc277d4`  
		Last Modified: Tue, 12 Oct 2021 07:31:06 GMT  
		Size: 256.1 KB (256142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa7805400cade2c3fda94906cc3502961f0a85bf26f07aeb6d74f4ba6866961b`  
		Last Modified: Tue, 12 Oct 2021 07:31:12 GMT  
		Size: 29.4 MB (29359244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.10`

```console
$ docker pull mono@sha256:4b9611fd8dd34a3146aead1ff2e295b51f0de69ef13834d3ef9d97ba0aec9638
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:6.10` - linux; amd64

```console
$ docker pull mono@sha256:0cf13f9562c9d11274e63a553424114e707b1c623e3ffa1473db274aabfe63df
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.0 MB (224997077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a44543d8ef83451851e6c11a847197cbbf3d0c2518b421fef883a261174aefd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:21:02 GMT
ADD file:3c54ad257f2e04f7294ce879b884820cf4726c8e93ec548172825963e40c79ad in / 
# Wed, 17 Nov 2021 02:21:02 GMT
CMD ["bash"]
# Fri, 19 Nov 2021 18:07:22 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 23 Nov 2021 22:36:08 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 23 Nov 2021 22:36:35 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 23 Nov 2021 22:48:07 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a10c77af261312e7c92bcc184f2d1726175ff7f142e44b01c5779cd79348b9fd`  
		Last Modified: Wed, 17 Nov 2021 02:26:31 GMT  
		Size: 27.2 MB (27153675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:273126c48d3776a7ad57be8dd21eddd8abf9b8c8f680eb1cb099fd6368f37b5c`  
		Last Modified: Tue, 23 Nov 2021 22:49:11 GMT  
		Size: 2.8 MB (2766983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed66b2de85cb6c71b90485e1631e323405ebd14607d265cb9d99867ff8afaeb8`  
		Last Modified: Tue, 23 Nov 2021 22:49:24 GMT  
		Size: 64.8 MB (64778925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2af59af55a6b336fa2e2b015f603c7aab2e0f4c0a332ea68649a0a096a8b933e`  
		Last Modified: Tue, 23 Nov 2021 22:50:39 GMT  
		Size: 130.3 MB (130297494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10` - linux; arm variant v5

```console
$ docker pull mono@sha256:354d5ee143fce2a6d8f090998b0152a5d1da9c6989fd60593b15a8da5c2df609
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.8 MB (180835880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1a33cbf87c99ee2e9ccf3126e51b8a0a1cdfd6bd1d975e4836e7b2bb9e79f28`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:51:39 GMT
ADD file:e580d4d2066301375327ea51dd8db3af956e5a465495bf09d69d6deec9b0bfae in / 
# Wed, 17 Nov 2021 02:51:40 GMT
CMD ["bash"]
# Tue, 23 Nov 2021 21:58:58 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 23 Nov 2021 21:59:33 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 23 Nov 2021 22:00:23 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 23 Nov 2021 22:07:12 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:dba255a4b166bb02562ca152d0da236ba8f211de5bf9d79e35ee023b1fce203e`  
		Last Modified: Wed, 17 Nov 2021 03:07:41 GMT  
		Size: 24.9 MB (24886310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ad85ab459382acb2813393b444e74920a65fbda3c4dcac61accfcf3bcf8cc77`  
		Last Modified: Tue, 23 Nov 2021 22:09:16 GMT  
		Size: 2.5 MB (2462560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7da8ebf7fcb6a4bf2222d798936426e3b6b4b504d96636004e700384d84a2b3e`  
		Last Modified: Tue, 23 Nov 2021 22:09:34 GMT  
		Size: 24.5 MB (24521813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c977aea9fa20aa837984bc124c498b124453fbd3cf3292cd4bc5af01786c7ef2`  
		Last Modified: Tue, 23 Nov 2021 22:13:10 GMT  
		Size: 129.0 MB (128965197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10` - linux; arm variant v7

```console
$ docker pull mono@sha256:7f3192a4525653287eae1fda37fe44531970c191fdfe57ff5a2955681eb4357f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.7 MB (176747046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f366363cc3952166a325d0012fa28cea8b1b008cfda0e049de2b7d426550aed5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:00:46 GMT
ADD file:4ac0de0d740f0c221cd4f912861a67009942fa5bdad24ac8b62c690dfa15024a in / 
# Wed, 17 Nov 2021 02:00:47 GMT
CMD ["bash"]
# Tue, 23 Nov 2021 22:29:55 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 23 Nov 2021 22:30:21 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 23 Nov 2021 22:31:04 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 23 Nov 2021 22:37:21 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7bd9e64406c6f3044bd15f89c367f07ec4eaafb1035a5c3ee2f7b138be68017f`  
		Last Modified: Wed, 17 Nov 2021 02:16:39 GMT  
		Size: 22.8 MB (22754359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:882235cc500d8281ee0a15448763a7034c68722bd8a945e915a1e759e70bd0c5`  
		Last Modified: Tue, 23 Nov 2021 22:39:31 GMT  
		Size: 2.4 MB (2361930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f37b676aae9d9d570e3b23306a2f9e6002eccc2cc37e365de82d3507032e4bb`  
		Last Modified: Tue, 23 Nov 2021 22:39:47 GMT  
		Size: 23.8 MB (23814916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:876e4eef53ef0f3c07bd6ed444168b1f4d19470551ae6313c4354fe605bf6189`  
		Last Modified: Tue, 23 Nov 2021 22:43:30 GMT  
		Size: 127.8 MB (127815841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:e49df4a24b2a5616f81aa9d774b4fad45f099aa1d7fb6792fd0484c217d64ba8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.4 MB (203356384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e55028e5828fa2d6224d63e8abea5f99e11b2eecf95a3b696443837f35fd228`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:40:44 GMT
ADD file:b7921dd77c7620d46a18a4b5952557620210bf7ad9de20fe8e695a371188122a in / 
# Wed, 17 Nov 2021 02:40:44 GMT
CMD ["bash"]
# Tue, 23 Nov 2021 21:52:21 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 23 Nov 2021 21:52:36 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 23 Nov 2021 21:52:58 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 23 Nov 2021 21:56:11 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:8ccb9871ed7bebcea8889b08e06fe5bd0116711ca7b110429b987475bf4d40e8`  
		Last Modified: Wed, 17 Nov 2021 02:48:07 GMT  
		Size: 25.9 MB (25923117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:723c9d46816fb741563e21c619d24385493cd49870e216b2bae35afe8dd938e0`  
		Last Modified: Tue, 23 Nov 2021 21:57:25 GMT  
		Size: 2.6 MB (2634593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6568a153ab8cf03d93526176aeec1c3f26ef57d4c7ffd86962594338c298386`  
		Last Modified: Tue, 23 Nov 2021 21:57:29 GMT  
		Size: 29.4 MB (29361620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:408a8acf227e74b822ba43375b9cbb2cc7af2faa2d259e706688baed41ea5d23`  
		Last Modified: Tue, 23 Nov 2021 21:58:55 GMT  
		Size: 145.4 MB (145437054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10` - linux; 386

```console
$ docker pull mono@sha256:7bb1a6e027e854282e09993d3da26d262c2982fc0854b5d27f3769c4c822262f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.8 MB (230807729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cf958da044325b351d58a6c7f8ad0fdf1683e4f58939cc19fc59b692cacb52e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:40:22 GMT
ADD file:2adea3474b7ebda2bf77361304ee3e6966a9118aafd8220b81c4027be1f4d583 in / 
# Wed, 17 Nov 2021 02:40:22 GMT
CMD ["bash"]
# Tue, 23 Nov 2021 21:42:55 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 23 Nov 2021 21:43:06 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 23 Nov 2021 21:43:37 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 23 Nov 2021 21:46:49 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7af5c9e671306e395c50a515c7bbe33d6f418ea08535b01c884457f78114eb08`  
		Last Modified: Wed, 17 Nov 2021 02:48:49 GMT  
		Size: 27.8 MB (27804550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d7176b139e9d9d316125cbe0c447bd6c1782c85a6c010a3642875a92c5b34e2`  
		Last Modified: Tue, 23 Nov 2021 21:48:21 GMT  
		Size: 2.8 MB (2781479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:081a66c890e4a4553da2c97618d817d7b365fdc62be809a493e53a0831f0c51d`  
		Last Modified: Tue, 23 Nov 2021 21:48:34 GMT  
		Size: 68.8 MB (68808217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8849c561c944700667c90a5586a74043828dd71d1ec6521a0bace4fe0415c0e`  
		Last Modified: Tue, 23 Nov 2021 21:50:05 GMT  
		Size: 131.4 MB (131413483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10` - linux; ppc64le

```console
$ docker pull mono@sha256:3f0887d326b63d7f5ad0866c2df678fc12f15a6edec9372dfc7b8ec6851338be
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.2 MB (192198562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4abd1b0c5695acacd4d9674e8d7f5db40074541017b2eec4b420533c6c56256e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Oct 2021 01:26:46 GMT
ADD file:5526880c6f19a4b4231a8b2bd7cfc625d116764c4918eff6f0b55f8c1eb38e1a in / 
# Tue, 12 Oct 2021 01:26:50 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 07:10:24 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 12 Oct 2021 07:12:18 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 12 Oct 2021 07:13:59 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 12 Oct 2021 07:29:54 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:d69973af32573c07c8789c0f9c144a5c0b822a1e85b59db3ce9f8ebc489ce85d`  
		Last Modified: Tue, 12 Oct 2021 01:38:40 GMT  
		Size: 30.5 MB (30547197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5181947e119d32c630d3afa4d57d30f1a958bfd4d29188dee7f90434d0bd6a22`  
		Last Modified: Tue, 12 Oct 2021 07:31:31 GMT  
		Size: 256.2 KB (256205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd4135299632e51ae71a0819d91059f490f63c9199515d79828151d9b66a0dda`  
		Last Modified: Tue, 12 Oct 2021 07:31:38 GMT  
		Size: 29.4 MB (29393095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df49308dff9e71d49d0f41f0b92b643ff65f9075cf3333a0f6a5d7a5fcc15bfb`  
		Last Modified: Tue, 12 Oct 2021 07:33:04 GMT  
		Size: 132.0 MB (132002065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.10-slim`

```console
$ docker pull mono@sha256:fedf956359c65fe0bc0208f7605fb8bf57e49a6ef70ac7a18f823e63203a1c54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:6.10-slim` - linux; amd64

```console
$ docker pull mono@sha256:e305fbed051d15d03c92bac9d0150e1dad833c76e0b3e32c708cd2111f08965c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.7 MB (94699583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:160817976db188f65554948b05a9049a1750667f18b7dd8067c479c22408284f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:21:02 GMT
ADD file:3c54ad257f2e04f7294ce879b884820cf4726c8e93ec548172825963e40c79ad in / 
# Wed, 17 Nov 2021 02:21:02 GMT
CMD ["bash"]
# Fri, 19 Nov 2021 18:07:22 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 23 Nov 2021 22:36:08 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 23 Nov 2021 22:36:35 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a10c77af261312e7c92bcc184f2d1726175ff7f142e44b01c5779cd79348b9fd`  
		Last Modified: Wed, 17 Nov 2021 02:26:31 GMT  
		Size: 27.2 MB (27153675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:273126c48d3776a7ad57be8dd21eddd8abf9b8c8f680eb1cb099fd6368f37b5c`  
		Last Modified: Tue, 23 Nov 2021 22:49:11 GMT  
		Size: 2.8 MB (2766983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed66b2de85cb6c71b90485e1631e323405ebd14607d265cb9d99867ff8afaeb8`  
		Last Modified: Tue, 23 Nov 2021 22:49:24 GMT  
		Size: 64.8 MB (64778925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:a66c13603c315c786307f7536f2a9b5eb1a09e56eb5c1fc0ae79db3977768edd
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.9 MB (51870683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5688ad22b579ad594ffeb2483d821320b4b36147d4d895a05d91b5d401ffd2d5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:51:39 GMT
ADD file:e580d4d2066301375327ea51dd8db3af956e5a465495bf09d69d6deec9b0bfae in / 
# Wed, 17 Nov 2021 02:51:40 GMT
CMD ["bash"]
# Tue, 23 Nov 2021 21:58:58 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 23 Nov 2021 21:59:33 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 23 Nov 2021 22:00:23 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:dba255a4b166bb02562ca152d0da236ba8f211de5bf9d79e35ee023b1fce203e`  
		Last Modified: Wed, 17 Nov 2021 03:07:41 GMT  
		Size: 24.9 MB (24886310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ad85ab459382acb2813393b444e74920a65fbda3c4dcac61accfcf3bcf8cc77`  
		Last Modified: Tue, 23 Nov 2021 22:09:16 GMT  
		Size: 2.5 MB (2462560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7da8ebf7fcb6a4bf2222d798936426e3b6b4b504d96636004e700384d84a2b3e`  
		Last Modified: Tue, 23 Nov 2021 22:09:34 GMT  
		Size: 24.5 MB (24521813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:c8ff9a0586e39f7acd102d70dbc7dd6166d7599906973f3160c43a82b43059c8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48931205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a0eab126aaddec11cd0037ca4557a1b84edd4d1fcb4a1b5abaec84682450444`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:00:46 GMT
ADD file:4ac0de0d740f0c221cd4f912861a67009942fa5bdad24ac8b62c690dfa15024a in / 
# Wed, 17 Nov 2021 02:00:47 GMT
CMD ["bash"]
# Tue, 23 Nov 2021 22:29:55 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 23 Nov 2021 22:30:21 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 23 Nov 2021 22:31:04 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7bd9e64406c6f3044bd15f89c367f07ec4eaafb1035a5c3ee2f7b138be68017f`  
		Last Modified: Wed, 17 Nov 2021 02:16:39 GMT  
		Size: 22.8 MB (22754359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:882235cc500d8281ee0a15448763a7034c68722bd8a945e915a1e759e70bd0c5`  
		Last Modified: Tue, 23 Nov 2021 22:39:31 GMT  
		Size: 2.4 MB (2361930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f37b676aae9d9d570e3b23306a2f9e6002eccc2cc37e365de82d3507032e4bb`  
		Last Modified: Tue, 23 Nov 2021 22:39:47 GMT  
		Size: 23.8 MB (23814916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:63b0c5934fce7b0a6a38596c023a413e5f0a6dcd8b20090b40e7b0a30136c8f0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.9 MB (57919330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3b0088bedb03704e609d452ab9183945bfcdacdfdcdaed39333e33cffe5c399`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:40:44 GMT
ADD file:b7921dd77c7620d46a18a4b5952557620210bf7ad9de20fe8e695a371188122a in / 
# Wed, 17 Nov 2021 02:40:44 GMT
CMD ["bash"]
# Tue, 23 Nov 2021 21:52:21 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 23 Nov 2021 21:52:36 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 23 Nov 2021 21:52:58 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:8ccb9871ed7bebcea8889b08e06fe5bd0116711ca7b110429b987475bf4d40e8`  
		Last Modified: Wed, 17 Nov 2021 02:48:07 GMT  
		Size: 25.9 MB (25923117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:723c9d46816fb741563e21c619d24385493cd49870e216b2bae35afe8dd938e0`  
		Last Modified: Tue, 23 Nov 2021 21:57:25 GMT  
		Size: 2.6 MB (2634593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6568a153ab8cf03d93526176aeec1c3f26ef57d4c7ffd86962594338c298386`  
		Last Modified: Tue, 23 Nov 2021 21:57:29 GMT  
		Size: 29.4 MB (29361620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10-slim` - linux; 386

```console
$ docker pull mono@sha256:1a63ed19070bfc16afea69b217bbc04dfba58a9fe251c4503ca3362cf59bec97
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.4 MB (99394246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07742a64c0cc1ba5ca5462ff474a058a75b8026eea9aed48dd184bfa060b5cfd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:40:22 GMT
ADD file:2adea3474b7ebda2bf77361304ee3e6966a9118aafd8220b81c4027be1f4d583 in / 
# Wed, 17 Nov 2021 02:40:22 GMT
CMD ["bash"]
# Tue, 23 Nov 2021 21:42:55 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 23 Nov 2021 21:43:06 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 23 Nov 2021 21:43:37 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7af5c9e671306e395c50a515c7bbe33d6f418ea08535b01c884457f78114eb08`  
		Last Modified: Wed, 17 Nov 2021 02:48:49 GMT  
		Size: 27.8 MB (27804550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d7176b139e9d9d316125cbe0c447bd6c1782c85a6c010a3642875a92c5b34e2`  
		Last Modified: Tue, 23 Nov 2021 21:48:21 GMT  
		Size: 2.8 MB (2781479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:081a66c890e4a4553da2c97618d817d7b365fdc62be809a493e53a0831f0c51d`  
		Last Modified: Tue, 23 Nov 2021 21:48:34 GMT  
		Size: 68.8 MB (68808217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:132a46e1847bec4f03ca6da9436d408477e5e02a32c71a189d5952150cfc9c6e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60196497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d367dc195070e60b968e16ebbc297423526d8a782d7a13bf471f66d530fe51b9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Oct 2021 01:26:46 GMT
ADD file:5526880c6f19a4b4231a8b2bd7cfc625d116764c4918eff6f0b55f8c1eb38e1a in / 
# Tue, 12 Oct 2021 01:26:50 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 07:10:24 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 12 Oct 2021 07:12:18 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 12 Oct 2021 07:13:59 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:d69973af32573c07c8789c0f9c144a5c0b822a1e85b59db3ce9f8ebc489ce85d`  
		Last Modified: Tue, 12 Oct 2021 01:38:40 GMT  
		Size: 30.5 MB (30547197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5181947e119d32c630d3afa4d57d30f1a958bfd4d29188dee7f90434d0bd6a22`  
		Last Modified: Tue, 12 Oct 2021 07:31:31 GMT  
		Size: 256.2 KB (256205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd4135299632e51ae71a0819d91059f490f63c9199515d79828151d9b66a0dda`  
		Last Modified: Tue, 12 Oct 2021 07:31:38 GMT  
		Size: 29.4 MB (29393095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.10.0`

```console
$ docker pull mono@sha256:4b9611fd8dd34a3146aead1ff2e295b51f0de69ef13834d3ef9d97ba0aec9638
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:6.10.0` - linux; amd64

```console
$ docker pull mono@sha256:0cf13f9562c9d11274e63a553424114e707b1c623e3ffa1473db274aabfe63df
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.0 MB (224997077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a44543d8ef83451851e6c11a847197cbbf3d0c2518b421fef883a261174aefd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:21:02 GMT
ADD file:3c54ad257f2e04f7294ce879b884820cf4726c8e93ec548172825963e40c79ad in / 
# Wed, 17 Nov 2021 02:21:02 GMT
CMD ["bash"]
# Fri, 19 Nov 2021 18:07:22 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 23 Nov 2021 22:36:08 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 23 Nov 2021 22:36:35 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 23 Nov 2021 22:48:07 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a10c77af261312e7c92bcc184f2d1726175ff7f142e44b01c5779cd79348b9fd`  
		Last Modified: Wed, 17 Nov 2021 02:26:31 GMT  
		Size: 27.2 MB (27153675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:273126c48d3776a7ad57be8dd21eddd8abf9b8c8f680eb1cb099fd6368f37b5c`  
		Last Modified: Tue, 23 Nov 2021 22:49:11 GMT  
		Size: 2.8 MB (2766983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed66b2de85cb6c71b90485e1631e323405ebd14607d265cb9d99867ff8afaeb8`  
		Last Modified: Tue, 23 Nov 2021 22:49:24 GMT  
		Size: 64.8 MB (64778925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2af59af55a6b336fa2e2b015f603c7aab2e0f4c0a332ea68649a0a096a8b933e`  
		Last Modified: Tue, 23 Nov 2021 22:50:39 GMT  
		Size: 130.3 MB (130297494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0` - linux; arm variant v5

```console
$ docker pull mono@sha256:354d5ee143fce2a6d8f090998b0152a5d1da9c6989fd60593b15a8da5c2df609
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.8 MB (180835880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1a33cbf87c99ee2e9ccf3126e51b8a0a1cdfd6bd1d975e4836e7b2bb9e79f28`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:51:39 GMT
ADD file:e580d4d2066301375327ea51dd8db3af956e5a465495bf09d69d6deec9b0bfae in / 
# Wed, 17 Nov 2021 02:51:40 GMT
CMD ["bash"]
# Tue, 23 Nov 2021 21:58:58 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 23 Nov 2021 21:59:33 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 23 Nov 2021 22:00:23 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 23 Nov 2021 22:07:12 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:dba255a4b166bb02562ca152d0da236ba8f211de5bf9d79e35ee023b1fce203e`  
		Last Modified: Wed, 17 Nov 2021 03:07:41 GMT  
		Size: 24.9 MB (24886310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ad85ab459382acb2813393b444e74920a65fbda3c4dcac61accfcf3bcf8cc77`  
		Last Modified: Tue, 23 Nov 2021 22:09:16 GMT  
		Size: 2.5 MB (2462560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7da8ebf7fcb6a4bf2222d798936426e3b6b4b504d96636004e700384d84a2b3e`  
		Last Modified: Tue, 23 Nov 2021 22:09:34 GMT  
		Size: 24.5 MB (24521813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c977aea9fa20aa837984bc124c498b124453fbd3cf3292cd4bc5af01786c7ef2`  
		Last Modified: Tue, 23 Nov 2021 22:13:10 GMT  
		Size: 129.0 MB (128965197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0` - linux; arm variant v7

```console
$ docker pull mono@sha256:7f3192a4525653287eae1fda37fe44531970c191fdfe57ff5a2955681eb4357f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.7 MB (176747046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f366363cc3952166a325d0012fa28cea8b1b008cfda0e049de2b7d426550aed5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:00:46 GMT
ADD file:4ac0de0d740f0c221cd4f912861a67009942fa5bdad24ac8b62c690dfa15024a in / 
# Wed, 17 Nov 2021 02:00:47 GMT
CMD ["bash"]
# Tue, 23 Nov 2021 22:29:55 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 23 Nov 2021 22:30:21 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 23 Nov 2021 22:31:04 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 23 Nov 2021 22:37:21 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7bd9e64406c6f3044bd15f89c367f07ec4eaafb1035a5c3ee2f7b138be68017f`  
		Last Modified: Wed, 17 Nov 2021 02:16:39 GMT  
		Size: 22.8 MB (22754359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:882235cc500d8281ee0a15448763a7034c68722bd8a945e915a1e759e70bd0c5`  
		Last Modified: Tue, 23 Nov 2021 22:39:31 GMT  
		Size: 2.4 MB (2361930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f37b676aae9d9d570e3b23306a2f9e6002eccc2cc37e365de82d3507032e4bb`  
		Last Modified: Tue, 23 Nov 2021 22:39:47 GMT  
		Size: 23.8 MB (23814916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:876e4eef53ef0f3c07bd6ed444168b1f4d19470551ae6313c4354fe605bf6189`  
		Last Modified: Tue, 23 Nov 2021 22:43:30 GMT  
		Size: 127.8 MB (127815841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:e49df4a24b2a5616f81aa9d774b4fad45f099aa1d7fb6792fd0484c217d64ba8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.4 MB (203356384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e55028e5828fa2d6224d63e8abea5f99e11b2eecf95a3b696443837f35fd228`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:40:44 GMT
ADD file:b7921dd77c7620d46a18a4b5952557620210bf7ad9de20fe8e695a371188122a in / 
# Wed, 17 Nov 2021 02:40:44 GMT
CMD ["bash"]
# Tue, 23 Nov 2021 21:52:21 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 23 Nov 2021 21:52:36 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 23 Nov 2021 21:52:58 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 23 Nov 2021 21:56:11 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:8ccb9871ed7bebcea8889b08e06fe5bd0116711ca7b110429b987475bf4d40e8`  
		Last Modified: Wed, 17 Nov 2021 02:48:07 GMT  
		Size: 25.9 MB (25923117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:723c9d46816fb741563e21c619d24385493cd49870e216b2bae35afe8dd938e0`  
		Last Modified: Tue, 23 Nov 2021 21:57:25 GMT  
		Size: 2.6 MB (2634593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6568a153ab8cf03d93526176aeec1c3f26ef57d4c7ffd86962594338c298386`  
		Last Modified: Tue, 23 Nov 2021 21:57:29 GMT  
		Size: 29.4 MB (29361620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:408a8acf227e74b822ba43375b9cbb2cc7af2faa2d259e706688baed41ea5d23`  
		Last Modified: Tue, 23 Nov 2021 21:58:55 GMT  
		Size: 145.4 MB (145437054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0` - linux; 386

```console
$ docker pull mono@sha256:7bb1a6e027e854282e09993d3da26d262c2982fc0854b5d27f3769c4c822262f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.8 MB (230807729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cf958da044325b351d58a6c7f8ad0fdf1683e4f58939cc19fc59b692cacb52e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:40:22 GMT
ADD file:2adea3474b7ebda2bf77361304ee3e6966a9118aafd8220b81c4027be1f4d583 in / 
# Wed, 17 Nov 2021 02:40:22 GMT
CMD ["bash"]
# Tue, 23 Nov 2021 21:42:55 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 23 Nov 2021 21:43:06 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 23 Nov 2021 21:43:37 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 23 Nov 2021 21:46:49 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7af5c9e671306e395c50a515c7bbe33d6f418ea08535b01c884457f78114eb08`  
		Last Modified: Wed, 17 Nov 2021 02:48:49 GMT  
		Size: 27.8 MB (27804550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d7176b139e9d9d316125cbe0c447bd6c1782c85a6c010a3642875a92c5b34e2`  
		Last Modified: Tue, 23 Nov 2021 21:48:21 GMT  
		Size: 2.8 MB (2781479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:081a66c890e4a4553da2c97618d817d7b365fdc62be809a493e53a0831f0c51d`  
		Last Modified: Tue, 23 Nov 2021 21:48:34 GMT  
		Size: 68.8 MB (68808217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8849c561c944700667c90a5586a74043828dd71d1ec6521a0bace4fe0415c0e`  
		Last Modified: Tue, 23 Nov 2021 21:50:05 GMT  
		Size: 131.4 MB (131413483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0` - linux; ppc64le

```console
$ docker pull mono@sha256:3f0887d326b63d7f5ad0866c2df678fc12f15a6edec9372dfc7b8ec6851338be
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.2 MB (192198562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4abd1b0c5695acacd4d9674e8d7f5db40074541017b2eec4b420533c6c56256e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Oct 2021 01:26:46 GMT
ADD file:5526880c6f19a4b4231a8b2bd7cfc625d116764c4918eff6f0b55f8c1eb38e1a in / 
# Tue, 12 Oct 2021 01:26:50 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 07:10:24 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 12 Oct 2021 07:12:18 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 12 Oct 2021 07:13:59 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 12 Oct 2021 07:29:54 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:d69973af32573c07c8789c0f9c144a5c0b822a1e85b59db3ce9f8ebc489ce85d`  
		Last Modified: Tue, 12 Oct 2021 01:38:40 GMT  
		Size: 30.5 MB (30547197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5181947e119d32c630d3afa4d57d30f1a958bfd4d29188dee7f90434d0bd6a22`  
		Last Modified: Tue, 12 Oct 2021 07:31:31 GMT  
		Size: 256.2 KB (256205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd4135299632e51ae71a0819d91059f490f63c9199515d79828151d9b66a0dda`  
		Last Modified: Tue, 12 Oct 2021 07:31:38 GMT  
		Size: 29.4 MB (29393095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df49308dff9e71d49d0f41f0b92b643ff65f9075cf3333a0f6a5d7a5fcc15bfb`  
		Last Modified: Tue, 12 Oct 2021 07:33:04 GMT  
		Size: 132.0 MB (132002065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.10.0-slim`

```console
$ docker pull mono@sha256:fedf956359c65fe0bc0208f7605fb8bf57e49a6ef70ac7a18f823e63203a1c54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:6.10.0-slim` - linux; amd64

```console
$ docker pull mono@sha256:e305fbed051d15d03c92bac9d0150e1dad833c76e0b3e32c708cd2111f08965c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.7 MB (94699583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:160817976db188f65554948b05a9049a1750667f18b7dd8067c479c22408284f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:21:02 GMT
ADD file:3c54ad257f2e04f7294ce879b884820cf4726c8e93ec548172825963e40c79ad in / 
# Wed, 17 Nov 2021 02:21:02 GMT
CMD ["bash"]
# Fri, 19 Nov 2021 18:07:22 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 23 Nov 2021 22:36:08 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 23 Nov 2021 22:36:35 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a10c77af261312e7c92bcc184f2d1726175ff7f142e44b01c5779cd79348b9fd`  
		Last Modified: Wed, 17 Nov 2021 02:26:31 GMT  
		Size: 27.2 MB (27153675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:273126c48d3776a7ad57be8dd21eddd8abf9b8c8f680eb1cb099fd6368f37b5c`  
		Last Modified: Tue, 23 Nov 2021 22:49:11 GMT  
		Size: 2.8 MB (2766983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed66b2de85cb6c71b90485e1631e323405ebd14607d265cb9d99867ff8afaeb8`  
		Last Modified: Tue, 23 Nov 2021 22:49:24 GMT  
		Size: 64.8 MB (64778925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:a66c13603c315c786307f7536f2a9b5eb1a09e56eb5c1fc0ae79db3977768edd
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.9 MB (51870683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5688ad22b579ad594ffeb2483d821320b4b36147d4d895a05d91b5d401ffd2d5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:51:39 GMT
ADD file:e580d4d2066301375327ea51dd8db3af956e5a465495bf09d69d6deec9b0bfae in / 
# Wed, 17 Nov 2021 02:51:40 GMT
CMD ["bash"]
# Tue, 23 Nov 2021 21:58:58 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 23 Nov 2021 21:59:33 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 23 Nov 2021 22:00:23 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:dba255a4b166bb02562ca152d0da236ba8f211de5bf9d79e35ee023b1fce203e`  
		Last Modified: Wed, 17 Nov 2021 03:07:41 GMT  
		Size: 24.9 MB (24886310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ad85ab459382acb2813393b444e74920a65fbda3c4dcac61accfcf3bcf8cc77`  
		Last Modified: Tue, 23 Nov 2021 22:09:16 GMT  
		Size: 2.5 MB (2462560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7da8ebf7fcb6a4bf2222d798936426e3b6b4b504d96636004e700384d84a2b3e`  
		Last Modified: Tue, 23 Nov 2021 22:09:34 GMT  
		Size: 24.5 MB (24521813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:c8ff9a0586e39f7acd102d70dbc7dd6166d7599906973f3160c43a82b43059c8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48931205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a0eab126aaddec11cd0037ca4557a1b84edd4d1fcb4a1b5abaec84682450444`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:00:46 GMT
ADD file:4ac0de0d740f0c221cd4f912861a67009942fa5bdad24ac8b62c690dfa15024a in / 
# Wed, 17 Nov 2021 02:00:47 GMT
CMD ["bash"]
# Tue, 23 Nov 2021 22:29:55 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 23 Nov 2021 22:30:21 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 23 Nov 2021 22:31:04 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7bd9e64406c6f3044bd15f89c367f07ec4eaafb1035a5c3ee2f7b138be68017f`  
		Last Modified: Wed, 17 Nov 2021 02:16:39 GMT  
		Size: 22.8 MB (22754359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:882235cc500d8281ee0a15448763a7034c68722bd8a945e915a1e759e70bd0c5`  
		Last Modified: Tue, 23 Nov 2021 22:39:31 GMT  
		Size: 2.4 MB (2361930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f37b676aae9d9d570e3b23306a2f9e6002eccc2cc37e365de82d3507032e4bb`  
		Last Modified: Tue, 23 Nov 2021 22:39:47 GMT  
		Size: 23.8 MB (23814916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:63b0c5934fce7b0a6a38596c023a413e5f0a6dcd8b20090b40e7b0a30136c8f0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.9 MB (57919330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3b0088bedb03704e609d452ab9183945bfcdacdfdcdaed39333e33cffe5c399`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:40:44 GMT
ADD file:b7921dd77c7620d46a18a4b5952557620210bf7ad9de20fe8e695a371188122a in / 
# Wed, 17 Nov 2021 02:40:44 GMT
CMD ["bash"]
# Tue, 23 Nov 2021 21:52:21 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 23 Nov 2021 21:52:36 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 23 Nov 2021 21:52:58 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:8ccb9871ed7bebcea8889b08e06fe5bd0116711ca7b110429b987475bf4d40e8`  
		Last Modified: Wed, 17 Nov 2021 02:48:07 GMT  
		Size: 25.9 MB (25923117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:723c9d46816fb741563e21c619d24385493cd49870e216b2bae35afe8dd938e0`  
		Last Modified: Tue, 23 Nov 2021 21:57:25 GMT  
		Size: 2.6 MB (2634593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6568a153ab8cf03d93526176aeec1c3f26ef57d4c7ffd86962594338c298386`  
		Last Modified: Tue, 23 Nov 2021 21:57:29 GMT  
		Size: 29.4 MB (29361620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0-slim` - linux; 386

```console
$ docker pull mono@sha256:1a63ed19070bfc16afea69b217bbc04dfba58a9fe251c4503ca3362cf59bec97
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.4 MB (99394246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07742a64c0cc1ba5ca5462ff474a058a75b8026eea9aed48dd184bfa060b5cfd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:40:22 GMT
ADD file:2adea3474b7ebda2bf77361304ee3e6966a9118aafd8220b81c4027be1f4d583 in / 
# Wed, 17 Nov 2021 02:40:22 GMT
CMD ["bash"]
# Tue, 23 Nov 2021 21:42:55 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 23 Nov 2021 21:43:06 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 23 Nov 2021 21:43:37 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7af5c9e671306e395c50a515c7bbe33d6f418ea08535b01c884457f78114eb08`  
		Last Modified: Wed, 17 Nov 2021 02:48:49 GMT  
		Size: 27.8 MB (27804550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d7176b139e9d9d316125cbe0c447bd6c1782c85a6c010a3642875a92c5b34e2`  
		Last Modified: Tue, 23 Nov 2021 21:48:21 GMT  
		Size: 2.8 MB (2781479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:081a66c890e4a4553da2c97618d817d7b365fdc62be809a493e53a0831f0c51d`  
		Last Modified: Tue, 23 Nov 2021 21:48:34 GMT  
		Size: 68.8 MB (68808217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:132a46e1847bec4f03ca6da9436d408477e5e02a32c71a189d5952150cfc9c6e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60196497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d367dc195070e60b968e16ebbc297423526d8a782d7a13bf471f66d530fe51b9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Oct 2021 01:26:46 GMT
ADD file:5526880c6f19a4b4231a8b2bd7cfc625d116764c4918eff6f0b55f8c1eb38e1a in / 
# Tue, 12 Oct 2021 01:26:50 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 07:10:24 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 12 Oct 2021 07:12:18 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 12 Oct 2021 07:13:59 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:d69973af32573c07c8789c0f9c144a5c0b822a1e85b59db3ce9f8ebc489ce85d`  
		Last Modified: Tue, 12 Oct 2021 01:38:40 GMT  
		Size: 30.5 MB (30547197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5181947e119d32c630d3afa4d57d30f1a958bfd4d29188dee7f90434d0bd6a22`  
		Last Modified: Tue, 12 Oct 2021 07:31:31 GMT  
		Size: 256.2 KB (256205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd4135299632e51ae71a0819d91059f490f63c9199515d79828151d9b66a0dda`  
		Last Modified: Tue, 12 Oct 2021 07:31:38 GMT  
		Size: 29.4 MB (29393095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.10.0.104`

```console
$ docker pull mono@sha256:4b9611fd8dd34a3146aead1ff2e295b51f0de69ef13834d3ef9d97ba0aec9638
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:6.10.0.104` - linux; amd64

```console
$ docker pull mono@sha256:0cf13f9562c9d11274e63a553424114e707b1c623e3ffa1473db274aabfe63df
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.0 MB (224997077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a44543d8ef83451851e6c11a847197cbbf3d0c2518b421fef883a261174aefd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:21:02 GMT
ADD file:3c54ad257f2e04f7294ce879b884820cf4726c8e93ec548172825963e40c79ad in / 
# Wed, 17 Nov 2021 02:21:02 GMT
CMD ["bash"]
# Fri, 19 Nov 2021 18:07:22 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 23 Nov 2021 22:36:08 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 23 Nov 2021 22:36:35 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 23 Nov 2021 22:48:07 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a10c77af261312e7c92bcc184f2d1726175ff7f142e44b01c5779cd79348b9fd`  
		Last Modified: Wed, 17 Nov 2021 02:26:31 GMT  
		Size: 27.2 MB (27153675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:273126c48d3776a7ad57be8dd21eddd8abf9b8c8f680eb1cb099fd6368f37b5c`  
		Last Modified: Tue, 23 Nov 2021 22:49:11 GMT  
		Size: 2.8 MB (2766983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed66b2de85cb6c71b90485e1631e323405ebd14607d265cb9d99867ff8afaeb8`  
		Last Modified: Tue, 23 Nov 2021 22:49:24 GMT  
		Size: 64.8 MB (64778925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2af59af55a6b336fa2e2b015f603c7aab2e0f4c0a332ea68649a0a096a8b933e`  
		Last Modified: Tue, 23 Nov 2021 22:50:39 GMT  
		Size: 130.3 MB (130297494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0.104` - linux; arm variant v5

```console
$ docker pull mono@sha256:354d5ee143fce2a6d8f090998b0152a5d1da9c6989fd60593b15a8da5c2df609
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.8 MB (180835880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1a33cbf87c99ee2e9ccf3126e51b8a0a1cdfd6bd1d975e4836e7b2bb9e79f28`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:51:39 GMT
ADD file:e580d4d2066301375327ea51dd8db3af956e5a465495bf09d69d6deec9b0bfae in / 
# Wed, 17 Nov 2021 02:51:40 GMT
CMD ["bash"]
# Tue, 23 Nov 2021 21:58:58 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 23 Nov 2021 21:59:33 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 23 Nov 2021 22:00:23 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 23 Nov 2021 22:07:12 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:dba255a4b166bb02562ca152d0da236ba8f211de5bf9d79e35ee023b1fce203e`  
		Last Modified: Wed, 17 Nov 2021 03:07:41 GMT  
		Size: 24.9 MB (24886310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ad85ab459382acb2813393b444e74920a65fbda3c4dcac61accfcf3bcf8cc77`  
		Last Modified: Tue, 23 Nov 2021 22:09:16 GMT  
		Size: 2.5 MB (2462560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7da8ebf7fcb6a4bf2222d798936426e3b6b4b504d96636004e700384d84a2b3e`  
		Last Modified: Tue, 23 Nov 2021 22:09:34 GMT  
		Size: 24.5 MB (24521813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c977aea9fa20aa837984bc124c498b124453fbd3cf3292cd4bc5af01786c7ef2`  
		Last Modified: Tue, 23 Nov 2021 22:13:10 GMT  
		Size: 129.0 MB (128965197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0.104` - linux; arm variant v7

```console
$ docker pull mono@sha256:7f3192a4525653287eae1fda37fe44531970c191fdfe57ff5a2955681eb4357f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.7 MB (176747046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f366363cc3952166a325d0012fa28cea8b1b008cfda0e049de2b7d426550aed5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:00:46 GMT
ADD file:4ac0de0d740f0c221cd4f912861a67009942fa5bdad24ac8b62c690dfa15024a in / 
# Wed, 17 Nov 2021 02:00:47 GMT
CMD ["bash"]
# Tue, 23 Nov 2021 22:29:55 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 23 Nov 2021 22:30:21 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 23 Nov 2021 22:31:04 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 23 Nov 2021 22:37:21 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7bd9e64406c6f3044bd15f89c367f07ec4eaafb1035a5c3ee2f7b138be68017f`  
		Last Modified: Wed, 17 Nov 2021 02:16:39 GMT  
		Size: 22.8 MB (22754359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:882235cc500d8281ee0a15448763a7034c68722bd8a945e915a1e759e70bd0c5`  
		Last Modified: Tue, 23 Nov 2021 22:39:31 GMT  
		Size: 2.4 MB (2361930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f37b676aae9d9d570e3b23306a2f9e6002eccc2cc37e365de82d3507032e4bb`  
		Last Modified: Tue, 23 Nov 2021 22:39:47 GMT  
		Size: 23.8 MB (23814916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:876e4eef53ef0f3c07bd6ed444168b1f4d19470551ae6313c4354fe605bf6189`  
		Last Modified: Tue, 23 Nov 2021 22:43:30 GMT  
		Size: 127.8 MB (127815841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0.104` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:e49df4a24b2a5616f81aa9d774b4fad45f099aa1d7fb6792fd0484c217d64ba8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.4 MB (203356384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e55028e5828fa2d6224d63e8abea5f99e11b2eecf95a3b696443837f35fd228`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:40:44 GMT
ADD file:b7921dd77c7620d46a18a4b5952557620210bf7ad9de20fe8e695a371188122a in / 
# Wed, 17 Nov 2021 02:40:44 GMT
CMD ["bash"]
# Tue, 23 Nov 2021 21:52:21 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 23 Nov 2021 21:52:36 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 23 Nov 2021 21:52:58 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 23 Nov 2021 21:56:11 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:8ccb9871ed7bebcea8889b08e06fe5bd0116711ca7b110429b987475bf4d40e8`  
		Last Modified: Wed, 17 Nov 2021 02:48:07 GMT  
		Size: 25.9 MB (25923117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:723c9d46816fb741563e21c619d24385493cd49870e216b2bae35afe8dd938e0`  
		Last Modified: Tue, 23 Nov 2021 21:57:25 GMT  
		Size: 2.6 MB (2634593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6568a153ab8cf03d93526176aeec1c3f26ef57d4c7ffd86962594338c298386`  
		Last Modified: Tue, 23 Nov 2021 21:57:29 GMT  
		Size: 29.4 MB (29361620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:408a8acf227e74b822ba43375b9cbb2cc7af2faa2d259e706688baed41ea5d23`  
		Last Modified: Tue, 23 Nov 2021 21:58:55 GMT  
		Size: 145.4 MB (145437054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0.104` - linux; 386

```console
$ docker pull mono@sha256:7bb1a6e027e854282e09993d3da26d262c2982fc0854b5d27f3769c4c822262f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.8 MB (230807729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cf958da044325b351d58a6c7f8ad0fdf1683e4f58939cc19fc59b692cacb52e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:40:22 GMT
ADD file:2adea3474b7ebda2bf77361304ee3e6966a9118aafd8220b81c4027be1f4d583 in / 
# Wed, 17 Nov 2021 02:40:22 GMT
CMD ["bash"]
# Tue, 23 Nov 2021 21:42:55 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 23 Nov 2021 21:43:06 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 23 Nov 2021 21:43:37 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 23 Nov 2021 21:46:49 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7af5c9e671306e395c50a515c7bbe33d6f418ea08535b01c884457f78114eb08`  
		Last Modified: Wed, 17 Nov 2021 02:48:49 GMT  
		Size: 27.8 MB (27804550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d7176b139e9d9d316125cbe0c447bd6c1782c85a6c010a3642875a92c5b34e2`  
		Last Modified: Tue, 23 Nov 2021 21:48:21 GMT  
		Size: 2.8 MB (2781479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:081a66c890e4a4553da2c97618d817d7b365fdc62be809a493e53a0831f0c51d`  
		Last Modified: Tue, 23 Nov 2021 21:48:34 GMT  
		Size: 68.8 MB (68808217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8849c561c944700667c90a5586a74043828dd71d1ec6521a0bace4fe0415c0e`  
		Last Modified: Tue, 23 Nov 2021 21:50:05 GMT  
		Size: 131.4 MB (131413483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0.104` - linux; ppc64le

```console
$ docker pull mono@sha256:3f0887d326b63d7f5ad0866c2df678fc12f15a6edec9372dfc7b8ec6851338be
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.2 MB (192198562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4abd1b0c5695acacd4d9674e8d7f5db40074541017b2eec4b420533c6c56256e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Oct 2021 01:26:46 GMT
ADD file:5526880c6f19a4b4231a8b2bd7cfc625d116764c4918eff6f0b55f8c1eb38e1a in / 
# Tue, 12 Oct 2021 01:26:50 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 07:10:24 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 12 Oct 2021 07:12:18 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 12 Oct 2021 07:13:59 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 12 Oct 2021 07:29:54 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:d69973af32573c07c8789c0f9c144a5c0b822a1e85b59db3ce9f8ebc489ce85d`  
		Last Modified: Tue, 12 Oct 2021 01:38:40 GMT  
		Size: 30.5 MB (30547197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5181947e119d32c630d3afa4d57d30f1a958bfd4d29188dee7f90434d0bd6a22`  
		Last Modified: Tue, 12 Oct 2021 07:31:31 GMT  
		Size: 256.2 KB (256205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd4135299632e51ae71a0819d91059f490f63c9199515d79828151d9b66a0dda`  
		Last Modified: Tue, 12 Oct 2021 07:31:38 GMT  
		Size: 29.4 MB (29393095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df49308dff9e71d49d0f41f0b92b643ff65f9075cf3333a0f6a5d7a5fcc15bfb`  
		Last Modified: Tue, 12 Oct 2021 07:33:04 GMT  
		Size: 132.0 MB (132002065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.10.0.104-slim`

```console
$ docker pull mono@sha256:fedf956359c65fe0bc0208f7605fb8bf57e49a6ef70ac7a18f823e63203a1c54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:6.10.0.104-slim` - linux; amd64

```console
$ docker pull mono@sha256:e305fbed051d15d03c92bac9d0150e1dad833c76e0b3e32c708cd2111f08965c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.7 MB (94699583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:160817976db188f65554948b05a9049a1750667f18b7dd8067c479c22408284f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:21:02 GMT
ADD file:3c54ad257f2e04f7294ce879b884820cf4726c8e93ec548172825963e40c79ad in / 
# Wed, 17 Nov 2021 02:21:02 GMT
CMD ["bash"]
# Fri, 19 Nov 2021 18:07:22 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 23 Nov 2021 22:36:08 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 23 Nov 2021 22:36:35 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a10c77af261312e7c92bcc184f2d1726175ff7f142e44b01c5779cd79348b9fd`  
		Last Modified: Wed, 17 Nov 2021 02:26:31 GMT  
		Size: 27.2 MB (27153675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:273126c48d3776a7ad57be8dd21eddd8abf9b8c8f680eb1cb099fd6368f37b5c`  
		Last Modified: Tue, 23 Nov 2021 22:49:11 GMT  
		Size: 2.8 MB (2766983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed66b2de85cb6c71b90485e1631e323405ebd14607d265cb9d99867ff8afaeb8`  
		Last Modified: Tue, 23 Nov 2021 22:49:24 GMT  
		Size: 64.8 MB (64778925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0.104-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:a66c13603c315c786307f7536f2a9b5eb1a09e56eb5c1fc0ae79db3977768edd
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.9 MB (51870683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5688ad22b579ad594ffeb2483d821320b4b36147d4d895a05d91b5d401ffd2d5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:51:39 GMT
ADD file:e580d4d2066301375327ea51dd8db3af956e5a465495bf09d69d6deec9b0bfae in / 
# Wed, 17 Nov 2021 02:51:40 GMT
CMD ["bash"]
# Tue, 23 Nov 2021 21:58:58 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 23 Nov 2021 21:59:33 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 23 Nov 2021 22:00:23 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:dba255a4b166bb02562ca152d0da236ba8f211de5bf9d79e35ee023b1fce203e`  
		Last Modified: Wed, 17 Nov 2021 03:07:41 GMT  
		Size: 24.9 MB (24886310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ad85ab459382acb2813393b444e74920a65fbda3c4dcac61accfcf3bcf8cc77`  
		Last Modified: Tue, 23 Nov 2021 22:09:16 GMT  
		Size: 2.5 MB (2462560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7da8ebf7fcb6a4bf2222d798936426e3b6b4b504d96636004e700384d84a2b3e`  
		Last Modified: Tue, 23 Nov 2021 22:09:34 GMT  
		Size: 24.5 MB (24521813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0.104-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:c8ff9a0586e39f7acd102d70dbc7dd6166d7599906973f3160c43a82b43059c8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48931205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a0eab126aaddec11cd0037ca4557a1b84edd4d1fcb4a1b5abaec84682450444`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:00:46 GMT
ADD file:4ac0de0d740f0c221cd4f912861a67009942fa5bdad24ac8b62c690dfa15024a in / 
# Wed, 17 Nov 2021 02:00:47 GMT
CMD ["bash"]
# Tue, 23 Nov 2021 22:29:55 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 23 Nov 2021 22:30:21 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 23 Nov 2021 22:31:04 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7bd9e64406c6f3044bd15f89c367f07ec4eaafb1035a5c3ee2f7b138be68017f`  
		Last Modified: Wed, 17 Nov 2021 02:16:39 GMT  
		Size: 22.8 MB (22754359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:882235cc500d8281ee0a15448763a7034c68722bd8a945e915a1e759e70bd0c5`  
		Last Modified: Tue, 23 Nov 2021 22:39:31 GMT  
		Size: 2.4 MB (2361930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f37b676aae9d9d570e3b23306a2f9e6002eccc2cc37e365de82d3507032e4bb`  
		Last Modified: Tue, 23 Nov 2021 22:39:47 GMT  
		Size: 23.8 MB (23814916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0.104-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:63b0c5934fce7b0a6a38596c023a413e5f0a6dcd8b20090b40e7b0a30136c8f0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.9 MB (57919330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3b0088bedb03704e609d452ab9183945bfcdacdfdcdaed39333e33cffe5c399`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:40:44 GMT
ADD file:b7921dd77c7620d46a18a4b5952557620210bf7ad9de20fe8e695a371188122a in / 
# Wed, 17 Nov 2021 02:40:44 GMT
CMD ["bash"]
# Tue, 23 Nov 2021 21:52:21 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 23 Nov 2021 21:52:36 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 23 Nov 2021 21:52:58 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:8ccb9871ed7bebcea8889b08e06fe5bd0116711ca7b110429b987475bf4d40e8`  
		Last Modified: Wed, 17 Nov 2021 02:48:07 GMT  
		Size: 25.9 MB (25923117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:723c9d46816fb741563e21c619d24385493cd49870e216b2bae35afe8dd938e0`  
		Last Modified: Tue, 23 Nov 2021 21:57:25 GMT  
		Size: 2.6 MB (2634593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6568a153ab8cf03d93526176aeec1c3f26ef57d4c7ffd86962594338c298386`  
		Last Modified: Tue, 23 Nov 2021 21:57:29 GMT  
		Size: 29.4 MB (29361620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0.104-slim` - linux; 386

```console
$ docker pull mono@sha256:1a63ed19070bfc16afea69b217bbc04dfba58a9fe251c4503ca3362cf59bec97
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.4 MB (99394246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07742a64c0cc1ba5ca5462ff474a058a75b8026eea9aed48dd184bfa060b5cfd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:40:22 GMT
ADD file:2adea3474b7ebda2bf77361304ee3e6966a9118aafd8220b81c4027be1f4d583 in / 
# Wed, 17 Nov 2021 02:40:22 GMT
CMD ["bash"]
# Tue, 23 Nov 2021 21:42:55 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 23 Nov 2021 21:43:06 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 23 Nov 2021 21:43:37 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7af5c9e671306e395c50a515c7bbe33d6f418ea08535b01c884457f78114eb08`  
		Last Modified: Wed, 17 Nov 2021 02:48:49 GMT  
		Size: 27.8 MB (27804550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d7176b139e9d9d316125cbe0c447bd6c1782c85a6c010a3642875a92c5b34e2`  
		Last Modified: Tue, 23 Nov 2021 21:48:21 GMT  
		Size: 2.8 MB (2781479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:081a66c890e4a4553da2c97618d817d7b365fdc62be809a493e53a0831f0c51d`  
		Last Modified: Tue, 23 Nov 2021 21:48:34 GMT  
		Size: 68.8 MB (68808217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0.104-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:132a46e1847bec4f03ca6da9436d408477e5e02a32c71a189d5952150cfc9c6e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60196497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d367dc195070e60b968e16ebbc297423526d8a782d7a13bf471f66d530fe51b9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Oct 2021 01:26:46 GMT
ADD file:5526880c6f19a4b4231a8b2bd7cfc625d116764c4918eff6f0b55f8c1eb38e1a in / 
# Tue, 12 Oct 2021 01:26:50 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 07:10:24 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 12 Oct 2021 07:12:18 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 12 Oct 2021 07:13:59 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:d69973af32573c07c8789c0f9c144a5c0b822a1e85b59db3ce9f8ebc489ce85d`  
		Last Modified: Tue, 12 Oct 2021 01:38:40 GMT  
		Size: 30.5 MB (30547197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5181947e119d32c630d3afa4d57d30f1a958bfd4d29188dee7f90434d0bd6a22`  
		Last Modified: Tue, 12 Oct 2021 07:31:31 GMT  
		Size: 256.2 KB (256205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd4135299632e51ae71a0819d91059f490f63c9199515d79828151d9b66a0dda`  
		Last Modified: Tue, 12 Oct 2021 07:31:38 GMT  
		Size: 29.4 MB (29393095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.12`

```console
$ docker pull mono@sha256:b04d988ca0c1985b75f30422238cd0cf6cac7030e8492117b2ea2fd25194f6a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:6.12` - linux; amd64

```console
$ docker pull mono@sha256:481fce9886677b30abb23cf0b1aa5d477482a89b02f1207d0ef6cd6f462357bf
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.1 MB (236118149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0973a336ea5cc60790a8d4d304b05ddb030fea89166482e2d2372c9b1d6abf1e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:21:02 GMT
ADD file:3c54ad257f2e04f7294ce879b884820cf4726c8e93ec548172825963e40c79ad in / 
# Wed, 17 Nov 2021 02:21:02 GMT
CMD ["bash"]
# Tue, 23 Nov 2021 22:35:14 GMT
ENV MONO_VERSION=6.12.0.122
# Tue, 23 Nov 2021 22:35:29 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 23 Nov 2021 22:35:48 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 23 Nov 2021 22:41:26 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a10c77af261312e7c92bcc184f2d1726175ff7f142e44b01c5779cd79348b9fd`  
		Last Modified: Wed, 17 Nov 2021 02:26:31 GMT  
		Size: 27.2 MB (27153675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:290db4dba8dd1a22feca175d2300b4ca8dd16fe86ecc6022a566329a5b654ecf`  
		Last Modified: Tue, 23 Nov 2021 22:48:37 GMT  
		Size: 2.8 MB (2766933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbb78a53a304279c9bb401cfd5979e972f8fc1e746e9d36fc42525cd0676e372`  
		Last Modified: Tue, 23 Nov 2021 22:48:50 GMT  
		Size: 64.8 MB (64759889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b2ee3bb2622395bc301b422eccf0178ef24425f0fbd2392e582b3858628472c`  
		Last Modified: Tue, 23 Nov 2021 22:49:59 GMT  
		Size: 141.4 MB (141437652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12` - linux; arm variant v5

```console
$ docker pull mono@sha256:32c6613aba67088647674775dc9bc4936d1495cf10902d45fc8f51eb726a6a9c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.9 MB (191928998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4777f90f93be6f3b59383b98fa7e7ae724fadac57fde9062cba89d56d422826`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:51:39 GMT
ADD file:e580d4d2066301375327ea51dd8db3af956e5a465495bf09d69d6deec9b0bfae in / 
# Wed, 17 Nov 2021 02:51:40 GMT
CMD ["bash"]
# Tue, 23 Nov 2021 21:57:24 GMT
ENV MONO_VERSION=6.12.0.122
# Tue, 23 Nov 2021 21:57:55 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 23 Nov 2021 21:58:42 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 23 Nov 2021 22:03:49 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:dba255a4b166bb02562ca152d0da236ba8f211de5bf9d79e35ee023b1fce203e`  
		Last Modified: Wed, 17 Nov 2021 03:07:41 GMT  
		Size: 24.9 MB (24886310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01af261a6c29946e34b32228d294c69a86ca06cdfd0b0cfafbb568e9fc6b57b3`  
		Last Modified: Tue, 23 Nov 2021 22:08:39 GMT  
		Size: 2.5 MB (2462561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c562f4f3fb32ceeded7f153ed48a677c98f4efaee9d19ed32a8fcfa7fe236b27`  
		Last Modified: Tue, 23 Nov 2021 22:08:52 GMT  
		Size: 24.5 MB (24493189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6142af18d42fb857ff86fc8a7f00fbd715e0d8db30845d2424ff947cd9058276`  
		Last Modified: Tue, 23 Nov 2021 22:11:15 GMT  
		Size: 140.1 MB (140086938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12` - linux; arm variant v7

```console
$ docker pull mono@sha256:224100530ddf0867a699f0e1448fd2646c62e088c97bbe9fea0cfa488e8813c4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.8 MB (187845574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a6b45021de699193ede4308d6e2ae5eb2cc57e8def386c8a6e60d7a52c2c704`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:00:46 GMT
ADD file:4ac0de0d740f0c221cd4f912861a67009942fa5bdad24ac8b62c690dfa15024a in / 
# Wed, 17 Nov 2021 02:00:47 GMT
CMD ["bash"]
# Tue, 23 Nov 2021 22:28:21 GMT
ENV MONO_VERSION=6.12.0.122
# Tue, 23 Nov 2021 22:28:52 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 23 Nov 2021 22:29:35 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 23 Nov 2021 22:34:09 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7bd9e64406c6f3044bd15f89c367f07ec4eaafb1035a5c3ee2f7b138be68017f`  
		Last Modified: Wed, 17 Nov 2021 02:16:39 GMT  
		Size: 22.8 MB (22754359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:049b685383367eaa00b28d290b7f521588cc2a6fddec236420129ec04830f7ad`  
		Last Modified: Tue, 23 Nov 2021 22:38:55 GMT  
		Size: 2.4 MB (2361954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d696071cf20a8d6e7031e1c8c4453e1fcbd73fbd07d0e299ab428402906f012c`  
		Last Modified: Tue, 23 Nov 2021 22:39:06 GMT  
		Size: 23.8 MB (23782697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f919fba63d40094ff8de7041bdf8ea1ea33c8fb98dec1524acc0ddb1c7144658`  
		Last Modified: Tue, 23 Nov 2021 22:41:39 GMT  
		Size: 138.9 MB (138946564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:f51c87edd3a0bb05ecb545084c025665f2a4cc4c47b21b9fd7bd712ac9c8fd4b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.5 MB (214451528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32097382767f78b6abfadcb70f6979c659ec28225f0c64f08bdd820d4cb582f9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:40:44 GMT
ADD file:b7921dd77c7620d46a18a4b5952557620210bf7ad9de20fe8e695a371188122a in / 
# Wed, 17 Nov 2021 02:40:44 GMT
CMD ["bash"]
# Tue, 23 Nov 2021 21:51:44 GMT
ENV MONO_VERSION=6.12.0.122
# Tue, 23 Nov 2021 21:51:59 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 23 Nov 2021 21:52:15 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 23 Nov 2021 21:54:06 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:8ccb9871ed7bebcea8889b08e06fe5bd0116711ca7b110429b987475bf4d40e8`  
		Last Modified: Wed, 17 Nov 2021 02:48:07 GMT  
		Size: 25.9 MB (25923117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9d1d375755ac6c8647c886eb68f427d617cb789ae0c98372e585311a5395aa0`  
		Last Modified: Tue, 23 Nov 2021 21:57:01 GMT  
		Size: 2.6 MB (2634589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a5575918894c723f49db7b67bad957b34f1f6b88828b67489943f4618f2fdc4`  
		Last Modified: Tue, 23 Nov 2021 21:57:05 GMT  
		Size: 29.3 MB (29318238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ec24743e7bc80a3baec7c0697b8bd9d87e12e26d3c50e6d7e18c36dd63bd005`  
		Last Modified: Tue, 23 Nov 2021 21:58:08 GMT  
		Size: 156.6 MB (156575584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12` - linux; 386

```console
$ docker pull mono@sha256:487eab41ead5858f6e434ae442e99515059f95651604e49d867d41095e05f2eb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.9 MB (241920178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f058eee97b6682f2e4715db0d188185468cddc542f881b8053c7b1fbaf4567e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:40:22 GMT
ADD file:2adea3474b7ebda2bf77361304ee3e6966a9118aafd8220b81c4027be1f4d583 in / 
# Wed, 17 Nov 2021 02:40:22 GMT
CMD ["bash"]
# Tue, 23 Nov 2021 21:42:03 GMT
ENV MONO_VERSION=6.12.0.122
# Tue, 23 Nov 2021 21:42:22 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 23 Nov 2021 21:42:48 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 23 Nov 2021 21:44:49 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7af5c9e671306e395c50a515c7bbe33d6f418ea08535b01c884457f78114eb08`  
		Last Modified: Wed, 17 Nov 2021 02:48:49 GMT  
		Size: 27.8 MB (27804550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:178b44cff3441bdb1ada9b30fbb42c9e7143127e42b7e4715f38610b2d122927`  
		Last Modified: Tue, 23 Nov 2021 21:47:45 GMT  
		Size: 2.8 MB (2781502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b82f010a190c7a767fdbe0299862791645a573a4844487ee187efe7e6a34941`  
		Last Modified: Tue, 23 Nov 2021 21:47:59 GMT  
		Size: 68.8 MB (68778522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7c603a243c2c3d8943de83d6e0d8a8eaba5b511e76a1b921dcb9b576ef046b7`  
		Last Modified: Tue, 23 Nov 2021 21:49:18 GMT  
		Size: 142.6 MB (142555604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12` - linux; ppc64le

```console
$ docker pull mono@sha256:58c35decefee6c034da009565f9e354b1d3f0defbba53730df12f3cde2aeaeab
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.4 MB (203412519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99b8277a5b9fc92177d5f86fa33e2ff383ae55de6452afe5b1dd0d9215ba5f46`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Oct 2021 01:26:46 GMT
ADD file:5526880c6f19a4b4231a8b2bd7cfc625d116764c4918eff6f0b55f8c1eb38e1a in / 
# Tue, 12 Oct 2021 01:26:50 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 07:07:14 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 12 Oct 2021 07:08:29 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 12 Oct 2021 07:10:10 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 12 Oct 2021 07:21:13 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:d69973af32573c07c8789c0f9c144a5c0b822a1e85b59db3ce9f8ebc489ce85d`  
		Last Modified: Tue, 12 Oct 2021 01:38:40 GMT  
		Size: 30.5 MB (30547197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:411a4d07ce6468d0126e5f9f0ad6098034f004bb482027b2349909c0ebc277d4`  
		Last Modified: Tue, 12 Oct 2021 07:31:06 GMT  
		Size: 256.1 KB (256142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa7805400cade2c3fda94906cc3502961f0a85bf26f07aeb6d74f4ba6866961b`  
		Last Modified: Tue, 12 Oct 2021 07:31:12 GMT  
		Size: 29.4 MB (29359244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5bfdf96e676582679b152400f854a0a0c03af4dcd5f3abd6c9afc2068238061`  
		Last Modified: Tue, 12 Oct 2021 07:32:19 GMT  
		Size: 143.2 MB (143249936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.12-slim`

```console
$ docker pull mono@sha256:9d4ba66e353e699a1e0d2970e87b39e26cd619d3103cab57e29968c1a62c0c1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:6.12-slim` - linux; amd64

```console
$ docker pull mono@sha256:cdecd1e409a3bf015b2df7cab751b32aa1912942800c38c26dbbda077bd24a1d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.7 MB (94680497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:179c410963b2d950b30018aa2f7198d4bbf4750a44af79963bc2ec7eb619a78a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:21:02 GMT
ADD file:3c54ad257f2e04f7294ce879b884820cf4726c8e93ec548172825963e40c79ad in / 
# Wed, 17 Nov 2021 02:21:02 GMT
CMD ["bash"]
# Tue, 23 Nov 2021 22:35:14 GMT
ENV MONO_VERSION=6.12.0.122
# Tue, 23 Nov 2021 22:35:29 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 23 Nov 2021 22:35:48 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a10c77af261312e7c92bcc184f2d1726175ff7f142e44b01c5779cd79348b9fd`  
		Last Modified: Wed, 17 Nov 2021 02:26:31 GMT  
		Size: 27.2 MB (27153675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:290db4dba8dd1a22feca175d2300b4ca8dd16fe86ecc6022a566329a5b654ecf`  
		Last Modified: Tue, 23 Nov 2021 22:48:37 GMT  
		Size: 2.8 MB (2766933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbb78a53a304279c9bb401cfd5979e972f8fc1e746e9d36fc42525cd0676e372`  
		Last Modified: Tue, 23 Nov 2021 22:48:50 GMT  
		Size: 64.8 MB (64759889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:56e40b4d67adf3a932be68db6867706afb08420aa4ec4d1ce823c62f6369ca0a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51842060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76c279d60b298986449ea01c00551166b76185c559f47d494efc568cf54ea1c6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:51:39 GMT
ADD file:e580d4d2066301375327ea51dd8db3af956e5a465495bf09d69d6deec9b0bfae in / 
# Wed, 17 Nov 2021 02:51:40 GMT
CMD ["bash"]
# Tue, 23 Nov 2021 21:57:24 GMT
ENV MONO_VERSION=6.12.0.122
# Tue, 23 Nov 2021 21:57:55 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 23 Nov 2021 21:58:42 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:dba255a4b166bb02562ca152d0da236ba8f211de5bf9d79e35ee023b1fce203e`  
		Last Modified: Wed, 17 Nov 2021 03:07:41 GMT  
		Size: 24.9 MB (24886310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01af261a6c29946e34b32228d294c69a86ca06cdfd0b0cfafbb568e9fc6b57b3`  
		Last Modified: Tue, 23 Nov 2021 22:08:39 GMT  
		Size: 2.5 MB (2462561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c562f4f3fb32ceeded7f153ed48a677c98f4efaee9d19ed32a8fcfa7fe236b27`  
		Last Modified: Tue, 23 Nov 2021 22:08:52 GMT  
		Size: 24.5 MB (24493189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:abbc7a96a87a8fc3a75f3f9ee465f954103af6cb8caeeb2a58dcfa5775d9a5a6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48899010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:888f04b4468fa13c7dd2d4d3e6758e38cd6a1f2b8743d602ea8d6170470bc53f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:00:46 GMT
ADD file:4ac0de0d740f0c221cd4f912861a67009942fa5bdad24ac8b62c690dfa15024a in / 
# Wed, 17 Nov 2021 02:00:47 GMT
CMD ["bash"]
# Tue, 23 Nov 2021 22:28:21 GMT
ENV MONO_VERSION=6.12.0.122
# Tue, 23 Nov 2021 22:28:52 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 23 Nov 2021 22:29:35 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7bd9e64406c6f3044bd15f89c367f07ec4eaafb1035a5c3ee2f7b138be68017f`  
		Last Modified: Wed, 17 Nov 2021 02:16:39 GMT  
		Size: 22.8 MB (22754359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:049b685383367eaa00b28d290b7f521588cc2a6fddec236420129ec04830f7ad`  
		Last Modified: Tue, 23 Nov 2021 22:38:55 GMT  
		Size: 2.4 MB (2361954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d696071cf20a8d6e7031e1c8c4453e1fcbd73fbd07d0e299ab428402906f012c`  
		Last Modified: Tue, 23 Nov 2021 22:39:06 GMT  
		Size: 23.8 MB (23782697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:c8b6095166e5103eaa00541e4c8296a5082fc22f8b0c47f22b68524841854dda
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.9 MB (57875944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d2788a0d6a78feae4f3714b45819c05d06a535d1d2cd624e9cdb52386b96ff3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:40:44 GMT
ADD file:b7921dd77c7620d46a18a4b5952557620210bf7ad9de20fe8e695a371188122a in / 
# Wed, 17 Nov 2021 02:40:44 GMT
CMD ["bash"]
# Tue, 23 Nov 2021 21:51:44 GMT
ENV MONO_VERSION=6.12.0.122
# Tue, 23 Nov 2021 21:51:59 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 23 Nov 2021 21:52:15 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:8ccb9871ed7bebcea8889b08e06fe5bd0116711ca7b110429b987475bf4d40e8`  
		Last Modified: Wed, 17 Nov 2021 02:48:07 GMT  
		Size: 25.9 MB (25923117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9d1d375755ac6c8647c886eb68f427d617cb789ae0c98372e585311a5395aa0`  
		Last Modified: Tue, 23 Nov 2021 21:57:01 GMT  
		Size: 2.6 MB (2634589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a5575918894c723f49db7b67bad957b34f1f6b88828b67489943f4618f2fdc4`  
		Last Modified: Tue, 23 Nov 2021 21:57:05 GMT  
		Size: 29.3 MB (29318238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12-slim` - linux; 386

```console
$ docker pull mono@sha256:d5c218c6f846f064e3d68efb7e677d60a558d54067c13fe5a9554b1b6d2b8bdd
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.4 MB (99364574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2145d963dc4718d45ccb94e26a0153de7d7f1ee66964d3607401681ae010517d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:40:22 GMT
ADD file:2adea3474b7ebda2bf77361304ee3e6966a9118aafd8220b81c4027be1f4d583 in / 
# Wed, 17 Nov 2021 02:40:22 GMT
CMD ["bash"]
# Tue, 23 Nov 2021 21:42:03 GMT
ENV MONO_VERSION=6.12.0.122
# Tue, 23 Nov 2021 21:42:22 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 23 Nov 2021 21:42:48 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7af5c9e671306e395c50a515c7bbe33d6f418ea08535b01c884457f78114eb08`  
		Last Modified: Wed, 17 Nov 2021 02:48:49 GMT  
		Size: 27.8 MB (27804550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:178b44cff3441bdb1ada9b30fbb42c9e7143127e42b7e4715f38610b2d122927`  
		Last Modified: Tue, 23 Nov 2021 21:47:45 GMT  
		Size: 2.8 MB (2781502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b82f010a190c7a767fdbe0299862791645a573a4844487ee187efe7e6a34941`  
		Last Modified: Tue, 23 Nov 2021 21:47:59 GMT  
		Size: 68.8 MB (68778522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:7834ad815013a312211d9f24df0f88d7e3f04386d7c192b726662658029697f7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60162583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ee89c05071148752e8c61c25ab1424ba5b066d04b57a4f785fa443265cf2703`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Oct 2021 01:26:46 GMT
ADD file:5526880c6f19a4b4231a8b2bd7cfc625d116764c4918eff6f0b55f8c1eb38e1a in / 
# Tue, 12 Oct 2021 01:26:50 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 07:07:14 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 12 Oct 2021 07:08:29 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 12 Oct 2021 07:10:10 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:d69973af32573c07c8789c0f9c144a5c0b822a1e85b59db3ce9f8ebc489ce85d`  
		Last Modified: Tue, 12 Oct 2021 01:38:40 GMT  
		Size: 30.5 MB (30547197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:411a4d07ce6468d0126e5f9f0ad6098034f004bb482027b2349909c0ebc277d4`  
		Last Modified: Tue, 12 Oct 2021 07:31:06 GMT  
		Size: 256.1 KB (256142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa7805400cade2c3fda94906cc3502961f0a85bf26f07aeb6d74f4ba6866961b`  
		Last Modified: Tue, 12 Oct 2021 07:31:12 GMT  
		Size: 29.4 MB (29359244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.12.0`

```console
$ docker pull mono@sha256:b04d988ca0c1985b75f30422238cd0cf6cac7030e8492117b2ea2fd25194f6a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:6.12.0` - linux; amd64

```console
$ docker pull mono@sha256:481fce9886677b30abb23cf0b1aa5d477482a89b02f1207d0ef6cd6f462357bf
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.1 MB (236118149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0973a336ea5cc60790a8d4d304b05ddb030fea89166482e2d2372c9b1d6abf1e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:21:02 GMT
ADD file:3c54ad257f2e04f7294ce879b884820cf4726c8e93ec548172825963e40c79ad in / 
# Wed, 17 Nov 2021 02:21:02 GMT
CMD ["bash"]
# Tue, 23 Nov 2021 22:35:14 GMT
ENV MONO_VERSION=6.12.0.122
# Tue, 23 Nov 2021 22:35:29 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 23 Nov 2021 22:35:48 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 23 Nov 2021 22:41:26 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a10c77af261312e7c92bcc184f2d1726175ff7f142e44b01c5779cd79348b9fd`  
		Last Modified: Wed, 17 Nov 2021 02:26:31 GMT  
		Size: 27.2 MB (27153675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:290db4dba8dd1a22feca175d2300b4ca8dd16fe86ecc6022a566329a5b654ecf`  
		Last Modified: Tue, 23 Nov 2021 22:48:37 GMT  
		Size: 2.8 MB (2766933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbb78a53a304279c9bb401cfd5979e972f8fc1e746e9d36fc42525cd0676e372`  
		Last Modified: Tue, 23 Nov 2021 22:48:50 GMT  
		Size: 64.8 MB (64759889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b2ee3bb2622395bc301b422eccf0178ef24425f0fbd2392e582b3858628472c`  
		Last Modified: Tue, 23 Nov 2021 22:49:59 GMT  
		Size: 141.4 MB (141437652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0` - linux; arm variant v5

```console
$ docker pull mono@sha256:32c6613aba67088647674775dc9bc4936d1495cf10902d45fc8f51eb726a6a9c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.9 MB (191928998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4777f90f93be6f3b59383b98fa7e7ae724fadac57fde9062cba89d56d422826`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:51:39 GMT
ADD file:e580d4d2066301375327ea51dd8db3af956e5a465495bf09d69d6deec9b0bfae in / 
# Wed, 17 Nov 2021 02:51:40 GMT
CMD ["bash"]
# Tue, 23 Nov 2021 21:57:24 GMT
ENV MONO_VERSION=6.12.0.122
# Tue, 23 Nov 2021 21:57:55 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 23 Nov 2021 21:58:42 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 23 Nov 2021 22:03:49 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:dba255a4b166bb02562ca152d0da236ba8f211de5bf9d79e35ee023b1fce203e`  
		Last Modified: Wed, 17 Nov 2021 03:07:41 GMT  
		Size: 24.9 MB (24886310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01af261a6c29946e34b32228d294c69a86ca06cdfd0b0cfafbb568e9fc6b57b3`  
		Last Modified: Tue, 23 Nov 2021 22:08:39 GMT  
		Size: 2.5 MB (2462561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c562f4f3fb32ceeded7f153ed48a677c98f4efaee9d19ed32a8fcfa7fe236b27`  
		Last Modified: Tue, 23 Nov 2021 22:08:52 GMT  
		Size: 24.5 MB (24493189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6142af18d42fb857ff86fc8a7f00fbd715e0d8db30845d2424ff947cd9058276`  
		Last Modified: Tue, 23 Nov 2021 22:11:15 GMT  
		Size: 140.1 MB (140086938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0` - linux; arm variant v7

```console
$ docker pull mono@sha256:224100530ddf0867a699f0e1448fd2646c62e088c97bbe9fea0cfa488e8813c4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.8 MB (187845574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a6b45021de699193ede4308d6e2ae5eb2cc57e8def386c8a6e60d7a52c2c704`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:00:46 GMT
ADD file:4ac0de0d740f0c221cd4f912861a67009942fa5bdad24ac8b62c690dfa15024a in / 
# Wed, 17 Nov 2021 02:00:47 GMT
CMD ["bash"]
# Tue, 23 Nov 2021 22:28:21 GMT
ENV MONO_VERSION=6.12.0.122
# Tue, 23 Nov 2021 22:28:52 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 23 Nov 2021 22:29:35 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 23 Nov 2021 22:34:09 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7bd9e64406c6f3044bd15f89c367f07ec4eaafb1035a5c3ee2f7b138be68017f`  
		Last Modified: Wed, 17 Nov 2021 02:16:39 GMT  
		Size: 22.8 MB (22754359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:049b685383367eaa00b28d290b7f521588cc2a6fddec236420129ec04830f7ad`  
		Last Modified: Tue, 23 Nov 2021 22:38:55 GMT  
		Size: 2.4 MB (2361954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d696071cf20a8d6e7031e1c8c4453e1fcbd73fbd07d0e299ab428402906f012c`  
		Last Modified: Tue, 23 Nov 2021 22:39:06 GMT  
		Size: 23.8 MB (23782697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f919fba63d40094ff8de7041bdf8ea1ea33c8fb98dec1524acc0ddb1c7144658`  
		Last Modified: Tue, 23 Nov 2021 22:41:39 GMT  
		Size: 138.9 MB (138946564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:f51c87edd3a0bb05ecb545084c025665f2a4cc4c47b21b9fd7bd712ac9c8fd4b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.5 MB (214451528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32097382767f78b6abfadcb70f6979c659ec28225f0c64f08bdd820d4cb582f9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:40:44 GMT
ADD file:b7921dd77c7620d46a18a4b5952557620210bf7ad9de20fe8e695a371188122a in / 
# Wed, 17 Nov 2021 02:40:44 GMT
CMD ["bash"]
# Tue, 23 Nov 2021 21:51:44 GMT
ENV MONO_VERSION=6.12.0.122
# Tue, 23 Nov 2021 21:51:59 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 23 Nov 2021 21:52:15 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 23 Nov 2021 21:54:06 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:8ccb9871ed7bebcea8889b08e06fe5bd0116711ca7b110429b987475bf4d40e8`  
		Last Modified: Wed, 17 Nov 2021 02:48:07 GMT  
		Size: 25.9 MB (25923117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9d1d375755ac6c8647c886eb68f427d617cb789ae0c98372e585311a5395aa0`  
		Last Modified: Tue, 23 Nov 2021 21:57:01 GMT  
		Size: 2.6 MB (2634589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a5575918894c723f49db7b67bad957b34f1f6b88828b67489943f4618f2fdc4`  
		Last Modified: Tue, 23 Nov 2021 21:57:05 GMT  
		Size: 29.3 MB (29318238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ec24743e7bc80a3baec7c0697b8bd9d87e12e26d3c50e6d7e18c36dd63bd005`  
		Last Modified: Tue, 23 Nov 2021 21:58:08 GMT  
		Size: 156.6 MB (156575584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0` - linux; 386

```console
$ docker pull mono@sha256:487eab41ead5858f6e434ae442e99515059f95651604e49d867d41095e05f2eb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.9 MB (241920178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f058eee97b6682f2e4715db0d188185468cddc542f881b8053c7b1fbaf4567e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:40:22 GMT
ADD file:2adea3474b7ebda2bf77361304ee3e6966a9118aafd8220b81c4027be1f4d583 in / 
# Wed, 17 Nov 2021 02:40:22 GMT
CMD ["bash"]
# Tue, 23 Nov 2021 21:42:03 GMT
ENV MONO_VERSION=6.12.0.122
# Tue, 23 Nov 2021 21:42:22 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 23 Nov 2021 21:42:48 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 23 Nov 2021 21:44:49 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7af5c9e671306e395c50a515c7bbe33d6f418ea08535b01c884457f78114eb08`  
		Last Modified: Wed, 17 Nov 2021 02:48:49 GMT  
		Size: 27.8 MB (27804550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:178b44cff3441bdb1ada9b30fbb42c9e7143127e42b7e4715f38610b2d122927`  
		Last Modified: Tue, 23 Nov 2021 21:47:45 GMT  
		Size: 2.8 MB (2781502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b82f010a190c7a767fdbe0299862791645a573a4844487ee187efe7e6a34941`  
		Last Modified: Tue, 23 Nov 2021 21:47:59 GMT  
		Size: 68.8 MB (68778522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7c603a243c2c3d8943de83d6e0d8a8eaba5b511e76a1b921dcb9b576ef046b7`  
		Last Modified: Tue, 23 Nov 2021 21:49:18 GMT  
		Size: 142.6 MB (142555604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0` - linux; ppc64le

```console
$ docker pull mono@sha256:58c35decefee6c034da009565f9e354b1d3f0defbba53730df12f3cde2aeaeab
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.4 MB (203412519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99b8277a5b9fc92177d5f86fa33e2ff383ae55de6452afe5b1dd0d9215ba5f46`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Oct 2021 01:26:46 GMT
ADD file:5526880c6f19a4b4231a8b2bd7cfc625d116764c4918eff6f0b55f8c1eb38e1a in / 
# Tue, 12 Oct 2021 01:26:50 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 07:07:14 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 12 Oct 2021 07:08:29 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 12 Oct 2021 07:10:10 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 12 Oct 2021 07:21:13 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:d69973af32573c07c8789c0f9c144a5c0b822a1e85b59db3ce9f8ebc489ce85d`  
		Last Modified: Tue, 12 Oct 2021 01:38:40 GMT  
		Size: 30.5 MB (30547197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:411a4d07ce6468d0126e5f9f0ad6098034f004bb482027b2349909c0ebc277d4`  
		Last Modified: Tue, 12 Oct 2021 07:31:06 GMT  
		Size: 256.1 KB (256142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa7805400cade2c3fda94906cc3502961f0a85bf26f07aeb6d74f4ba6866961b`  
		Last Modified: Tue, 12 Oct 2021 07:31:12 GMT  
		Size: 29.4 MB (29359244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5bfdf96e676582679b152400f854a0a0c03af4dcd5f3abd6c9afc2068238061`  
		Last Modified: Tue, 12 Oct 2021 07:32:19 GMT  
		Size: 143.2 MB (143249936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.12.0-slim`

```console
$ docker pull mono@sha256:9d4ba66e353e699a1e0d2970e87b39e26cd619d3103cab57e29968c1a62c0c1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:6.12.0-slim` - linux; amd64

```console
$ docker pull mono@sha256:cdecd1e409a3bf015b2df7cab751b32aa1912942800c38c26dbbda077bd24a1d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.7 MB (94680497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:179c410963b2d950b30018aa2f7198d4bbf4750a44af79963bc2ec7eb619a78a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:21:02 GMT
ADD file:3c54ad257f2e04f7294ce879b884820cf4726c8e93ec548172825963e40c79ad in / 
# Wed, 17 Nov 2021 02:21:02 GMT
CMD ["bash"]
# Tue, 23 Nov 2021 22:35:14 GMT
ENV MONO_VERSION=6.12.0.122
# Tue, 23 Nov 2021 22:35:29 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 23 Nov 2021 22:35:48 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a10c77af261312e7c92bcc184f2d1726175ff7f142e44b01c5779cd79348b9fd`  
		Last Modified: Wed, 17 Nov 2021 02:26:31 GMT  
		Size: 27.2 MB (27153675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:290db4dba8dd1a22feca175d2300b4ca8dd16fe86ecc6022a566329a5b654ecf`  
		Last Modified: Tue, 23 Nov 2021 22:48:37 GMT  
		Size: 2.8 MB (2766933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbb78a53a304279c9bb401cfd5979e972f8fc1e746e9d36fc42525cd0676e372`  
		Last Modified: Tue, 23 Nov 2021 22:48:50 GMT  
		Size: 64.8 MB (64759889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:56e40b4d67adf3a932be68db6867706afb08420aa4ec4d1ce823c62f6369ca0a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51842060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76c279d60b298986449ea01c00551166b76185c559f47d494efc568cf54ea1c6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:51:39 GMT
ADD file:e580d4d2066301375327ea51dd8db3af956e5a465495bf09d69d6deec9b0bfae in / 
# Wed, 17 Nov 2021 02:51:40 GMT
CMD ["bash"]
# Tue, 23 Nov 2021 21:57:24 GMT
ENV MONO_VERSION=6.12.0.122
# Tue, 23 Nov 2021 21:57:55 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 23 Nov 2021 21:58:42 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:dba255a4b166bb02562ca152d0da236ba8f211de5bf9d79e35ee023b1fce203e`  
		Last Modified: Wed, 17 Nov 2021 03:07:41 GMT  
		Size: 24.9 MB (24886310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01af261a6c29946e34b32228d294c69a86ca06cdfd0b0cfafbb568e9fc6b57b3`  
		Last Modified: Tue, 23 Nov 2021 22:08:39 GMT  
		Size: 2.5 MB (2462561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c562f4f3fb32ceeded7f153ed48a677c98f4efaee9d19ed32a8fcfa7fe236b27`  
		Last Modified: Tue, 23 Nov 2021 22:08:52 GMT  
		Size: 24.5 MB (24493189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:abbc7a96a87a8fc3a75f3f9ee465f954103af6cb8caeeb2a58dcfa5775d9a5a6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48899010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:888f04b4468fa13c7dd2d4d3e6758e38cd6a1f2b8743d602ea8d6170470bc53f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:00:46 GMT
ADD file:4ac0de0d740f0c221cd4f912861a67009942fa5bdad24ac8b62c690dfa15024a in / 
# Wed, 17 Nov 2021 02:00:47 GMT
CMD ["bash"]
# Tue, 23 Nov 2021 22:28:21 GMT
ENV MONO_VERSION=6.12.0.122
# Tue, 23 Nov 2021 22:28:52 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 23 Nov 2021 22:29:35 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7bd9e64406c6f3044bd15f89c367f07ec4eaafb1035a5c3ee2f7b138be68017f`  
		Last Modified: Wed, 17 Nov 2021 02:16:39 GMT  
		Size: 22.8 MB (22754359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:049b685383367eaa00b28d290b7f521588cc2a6fddec236420129ec04830f7ad`  
		Last Modified: Tue, 23 Nov 2021 22:38:55 GMT  
		Size: 2.4 MB (2361954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d696071cf20a8d6e7031e1c8c4453e1fcbd73fbd07d0e299ab428402906f012c`  
		Last Modified: Tue, 23 Nov 2021 22:39:06 GMT  
		Size: 23.8 MB (23782697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:c8b6095166e5103eaa00541e4c8296a5082fc22f8b0c47f22b68524841854dda
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.9 MB (57875944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d2788a0d6a78feae4f3714b45819c05d06a535d1d2cd624e9cdb52386b96ff3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:40:44 GMT
ADD file:b7921dd77c7620d46a18a4b5952557620210bf7ad9de20fe8e695a371188122a in / 
# Wed, 17 Nov 2021 02:40:44 GMT
CMD ["bash"]
# Tue, 23 Nov 2021 21:51:44 GMT
ENV MONO_VERSION=6.12.0.122
# Tue, 23 Nov 2021 21:51:59 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 23 Nov 2021 21:52:15 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:8ccb9871ed7bebcea8889b08e06fe5bd0116711ca7b110429b987475bf4d40e8`  
		Last Modified: Wed, 17 Nov 2021 02:48:07 GMT  
		Size: 25.9 MB (25923117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9d1d375755ac6c8647c886eb68f427d617cb789ae0c98372e585311a5395aa0`  
		Last Modified: Tue, 23 Nov 2021 21:57:01 GMT  
		Size: 2.6 MB (2634589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a5575918894c723f49db7b67bad957b34f1f6b88828b67489943f4618f2fdc4`  
		Last Modified: Tue, 23 Nov 2021 21:57:05 GMT  
		Size: 29.3 MB (29318238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0-slim` - linux; 386

```console
$ docker pull mono@sha256:d5c218c6f846f064e3d68efb7e677d60a558d54067c13fe5a9554b1b6d2b8bdd
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.4 MB (99364574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2145d963dc4718d45ccb94e26a0153de7d7f1ee66964d3607401681ae010517d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:40:22 GMT
ADD file:2adea3474b7ebda2bf77361304ee3e6966a9118aafd8220b81c4027be1f4d583 in / 
# Wed, 17 Nov 2021 02:40:22 GMT
CMD ["bash"]
# Tue, 23 Nov 2021 21:42:03 GMT
ENV MONO_VERSION=6.12.0.122
# Tue, 23 Nov 2021 21:42:22 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 23 Nov 2021 21:42:48 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7af5c9e671306e395c50a515c7bbe33d6f418ea08535b01c884457f78114eb08`  
		Last Modified: Wed, 17 Nov 2021 02:48:49 GMT  
		Size: 27.8 MB (27804550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:178b44cff3441bdb1ada9b30fbb42c9e7143127e42b7e4715f38610b2d122927`  
		Last Modified: Tue, 23 Nov 2021 21:47:45 GMT  
		Size: 2.8 MB (2781502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b82f010a190c7a767fdbe0299862791645a573a4844487ee187efe7e6a34941`  
		Last Modified: Tue, 23 Nov 2021 21:47:59 GMT  
		Size: 68.8 MB (68778522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:7834ad815013a312211d9f24df0f88d7e3f04386d7c192b726662658029697f7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60162583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ee89c05071148752e8c61c25ab1424ba5b066d04b57a4f785fa443265cf2703`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Oct 2021 01:26:46 GMT
ADD file:5526880c6f19a4b4231a8b2bd7cfc625d116764c4918eff6f0b55f8c1eb38e1a in / 
# Tue, 12 Oct 2021 01:26:50 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 07:07:14 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 12 Oct 2021 07:08:29 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 12 Oct 2021 07:10:10 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:d69973af32573c07c8789c0f9c144a5c0b822a1e85b59db3ce9f8ebc489ce85d`  
		Last Modified: Tue, 12 Oct 2021 01:38:40 GMT  
		Size: 30.5 MB (30547197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:411a4d07ce6468d0126e5f9f0ad6098034f004bb482027b2349909c0ebc277d4`  
		Last Modified: Tue, 12 Oct 2021 07:31:06 GMT  
		Size: 256.1 KB (256142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa7805400cade2c3fda94906cc3502961f0a85bf26f07aeb6d74f4ba6866961b`  
		Last Modified: Tue, 12 Oct 2021 07:31:12 GMT  
		Size: 29.4 MB (29359244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.12.0.122`

```console
$ docker pull mono@sha256:32e6e7f766ae80dac494124973084366f69231272f15666f4c243153c23163c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `mono:6.12.0.122` - linux; amd64

```console
$ docker pull mono@sha256:481fce9886677b30abb23cf0b1aa5d477482a89b02f1207d0ef6cd6f462357bf
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.1 MB (236118149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0973a336ea5cc60790a8d4d304b05ddb030fea89166482e2d2372c9b1d6abf1e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:21:02 GMT
ADD file:3c54ad257f2e04f7294ce879b884820cf4726c8e93ec548172825963e40c79ad in / 
# Wed, 17 Nov 2021 02:21:02 GMT
CMD ["bash"]
# Tue, 23 Nov 2021 22:35:14 GMT
ENV MONO_VERSION=6.12.0.122
# Tue, 23 Nov 2021 22:35:29 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 23 Nov 2021 22:35:48 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 23 Nov 2021 22:41:26 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a10c77af261312e7c92bcc184f2d1726175ff7f142e44b01c5779cd79348b9fd`  
		Last Modified: Wed, 17 Nov 2021 02:26:31 GMT  
		Size: 27.2 MB (27153675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:290db4dba8dd1a22feca175d2300b4ca8dd16fe86ecc6022a566329a5b654ecf`  
		Last Modified: Tue, 23 Nov 2021 22:48:37 GMT  
		Size: 2.8 MB (2766933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbb78a53a304279c9bb401cfd5979e972f8fc1e746e9d36fc42525cd0676e372`  
		Last Modified: Tue, 23 Nov 2021 22:48:50 GMT  
		Size: 64.8 MB (64759889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b2ee3bb2622395bc301b422eccf0178ef24425f0fbd2392e582b3858628472c`  
		Last Modified: Tue, 23 Nov 2021 22:49:59 GMT  
		Size: 141.4 MB (141437652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0.122` - linux; arm variant v5

```console
$ docker pull mono@sha256:32c6613aba67088647674775dc9bc4936d1495cf10902d45fc8f51eb726a6a9c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.9 MB (191928998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4777f90f93be6f3b59383b98fa7e7ae724fadac57fde9062cba89d56d422826`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:51:39 GMT
ADD file:e580d4d2066301375327ea51dd8db3af956e5a465495bf09d69d6deec9b0bfae in / 
# Wed, 17 Nov 2021 02:51:40 GMT
CMD ["bash"]
# Tue, 23 Nov 2021 21:57:24 GMT
ENV MONO_VERSION=6.12.0.122
# Tue, 23 Nov 2021 21:57:55 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 23 Nov 2021 21:58:42 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 23 Nov 2021 22:03:49 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:dba255a4b166bb02562ca152d0da236ba8f211de5bf9d79e35ee023b1fce203e`  
		Last Modified: Wed, 17 Nov 2021 03:07:41 GMT  
		Size: 24.9 MB (24886310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01af261a6c29946e34b32228d294c69a86ca06cdfd0b0cfafbb568e9fc6b57b3`  
		Last Modified: Tue, 23 Nov 2021 22:08:39 GMT  
		Size: 2.5 MB (2462561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c562f4f3fb32ceeded7f153ed48a677c98f4efaee9d19ed32a8fcfa7fe236b27`  
		Last Modified: Tue, 23 Nov 2021 22:08:52 GMT  
		Size: 24.5 MB (24493189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6142af18d42fb857ff86fc8a7f00fbd715e0d8db30845d2424ff947cd9058276`  
		Last Modified: Tue, 23 Nov 2021 22:11:15 GMT  
		Size: 140.1 MB (140086938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0.122` - linux; arm variant v7

```console
$ docker pull mono@sha256:224100530ddf0867a699f0e1448fd2646c62e088c97bbe9fea0cfa488e8813c4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.8 MB (187845574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a6b45021de699193ede4308d6e2ae5eb2cc57e8def386c8a6e60d7a52c2c704`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:00:46 GMT
ADD file:4ac0de0d740f0c221cd4f912861a67009942fa5bdad24ac8b62c690dfa15024a in / 
# Wed, 17 Nov 2021 02:00:47 GMT
CMD ["bash"]
# Tue, 23 Nov 2021 22:28:21 GMT
ENV MONO_VERSION=6.12.0.122
# Tue, 23 Nov 2021 22:28:52 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 23 Nov 2021 22:29:35 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 23 Nov 2021 22:34:09 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7bd9e64406c6f3044bd15f89c367f07ec4eaafb1035a5c3ee2f7b138be68017f`  
		Last Modified: Wed, 17 Nov 2021 02:16:39 GMT  
		Size: 22.8 MB (22754359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:049b685383367eaa00b28d290b7f521588cc2a6fddec236420129ec04830f7ad`  
		Last Modified: Tue, 23 Nov 2021 22:38:55 GMT  
		Size: 2.4 MB (2361954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d696071cf20a8d6e7031e1c8c4453e1fcbd73fbd07d0e299ab428402906f012c`  
		Last Modified: Tue, 23 Nov 2021 22:39:06 GMT  
		Size: 23.8 MB (23782697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f919fba63d40094ff8de7041bdf8ea1ea33c8fb98dec1524acc0ddb1c7144658`  
		Last Modified: Tue, 23 Nov 2021 22:41:39 GMT  
		Size: 138.9 MB (138946564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0.122` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:f51c87edd3a0bb05ecb545084c025665f2a4cc4c47b21b9fd7bd712ac9c8fd4b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.5 MB (214451528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32097382767f78b6abfadcb70f6979c659ec28225f0c64f08bdd820d4cb582f9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:40:44 GMT
ADD file:b7921dd77c7620d46a18a4b5952557620210bf7ad9de20fe8e695a371188122a in / 
# Wed, 17 Nov 2021 02:40:44 GMT
CMD ["bash"]
# Tue, 23 Nov 2021 21:51:44 GMT
ENV MONO_VERSION=6.12.0.122
# Tue, 23 Nov 2021 21:51:59 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 23 Nov 2021 21:52:15 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 23 Nov 2021 21:54:06 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:8ccb9871ed7bebcea8889b08e06fe5bd0116711ca7b110429b987475bf4d40e8`  
		Last Modified: Wed, 17 Nov 2021 02:48:07 GMT  
		Size: 25.9 MB (25923117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9d1d375755ac6c8647c886eb68f427d617cb789ae0c98372e585311a5395aa0`  
		Last Modified: Tue, 23 Nov 2021 21:57:01 GMT  
		Size: 2.6 MB (2634589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a5575918894c723f49db7b67bad957b34f1f6b88828b67489943f4618f2fdc4`  
		Last Modified: Tue, 23 Nov 2021 21:57:05 GMT  
		Size: 29.3 MB (29318238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ec24743e7bc80a3baec7c0697b8bd9d87e12e26d3c50e6d7e18c36dd63bd005`  
		Last Modified: Tue, 23 Nov 2021 21:58:08 GMT  
		Size: 156.6 MB (156575584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0.122` - linux; 386

```console
$ docker pull mono@sha256:487eab41ead5858f6e434ae442e99515059f95651604e49d867d41095e05f2eb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.9 MB (241920178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f058eee97b6682f2e4715db0d188185468cddc542f881b8053c7b1fbaf4567e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:40:22 GMT
ADD file:2adea3474b7ebda2bf77361304ee3e6966a9118aafd8220b81c4027be1f4d583 in / 
# Wed, 17 Nov 2021 02:40:22 GMT
CMD ["bash"]
# Tue, 23 Nov 2021 21:42:03 GMT
ENV MONO_VERSION=6.12.0.122
# Tue, 23 Nov 2021 21:42:22 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 23 Nov 2021 21:42:48 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 23 Nov 2021 21:44:49 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7af5c9e671306e395c50a515c7bbe33d6f418ea08535b01c884457f78114eb08`  
		Last Modified: Wed, 17 Nov 2021 02:48:49 GMT  
		Size: 27.8 MB (27804550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:178b44cff3441bdb1ada9b30fbb42c9e7143127e42b7e4715f38610b2d122927`  
		Last Modified: Tue, 23 Nov 2021 21:47:45 GMT  
		Size: 2.8 MB (2781502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b82f010a190c7a767fdbe0299862791645a573a4844487ee187efe7e6a34941`  
		Last Modified: Tue, 23 Nov 2021 21:47:59 GMT  
		Size: 68.8 MB (68778522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7c603a243c2c3d8943de83d6e0d8a8eaba5b511e76a1b921dcb9b576ef046b7`  
		Last Modified: Tue, 23 Nov 2021 21:49:18 GMT  
		Size: 142.6 MB (142555604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.12.0.122-slim`

```console
$ docker pull mono@sha256:70679e54b8a763ec131504f3eb23bce8bcd9f838c1ea8265b4f1ceaf2b24b385
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `mono:6.12.0.122-slim` - linux; amd64

```console
$ docker pull mono@sha256:cdecd1e409a3bf015b2df7cab751b32aa1912942800c38c26dbbda077bd24a1d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.7 MB (94680497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:179c410963b2d950b30018aa2f7198d4bbf4750a44af79963bc2ec7eb619a78a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:21:02 GMT
ADD file:3c54ad257f2e04f7294ce879b884820cf4726c8e93ec548172825963e40c79ad in / 
# Wed, 17 Nov 2021 02:21:02 GMT
CMD ["bash"]
# Tue, 23 Nov 2021 22:35:14 GMT
ENV MONO_VERSION=6.12.0.122
# Tue, 23 Nov 2021 22:35:29 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 23 Nov 2021 22:35:48 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a10c77af261312e7c92bcc184f2d1726175ff7f142e44b01c5779cd79348b9fd`  
		Last Modified: Wed, 17 Nov 2021 02:26:31 GMT  
		Size: 27.2 MB (27153675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:290db4dba8dd1a22feca175d2300b4ca8dd16fe86ecc6022a566329a5b654ecf`  
		Last Modified: Tue, 23 Nov 2021 22:48:37 GMT  
		Size: 2.8 MB (2766933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbb78a53a304279c9bb401cfd5979e972f8fc1e746e9d36fc42525cd0676e372`  
		Last Modified: Tue, 23 Nov 2021 22:48:50 GMT  
		Size: 64.8 MB (64759889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0.122-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:56e40b4d67adf3a932be68db6867706afb08420aa4ec4d1ce823c62f6369ca0a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51842060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76c279d60b298986449ea01c00551166b76185c559f47d494efc568cf54ea1c6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:51:39 GMT
ADD file:e580d4d2066301375327ea51dd8db3af956e5a465495bf09d69d6deec9b0bfae in / 
# Wed, 17 Nov 2021 02:51:40 GMT
CMD ["bash"]
# Tue, 23 Nov 2021 21:57:24 GMT
ENV MONO_VERSION=6.12.0.122
# Tue, 23 Nov 2021 21:57:55 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 23 Nov 2021 21:58:42 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:dba255a4b166bb02562ca152d0da236ba8f211de5bf9d79e35ee023b1fce203e`  
		Last Modified: Wed, 17 Nov 2021 03:07:41 GMT  
		Size: 24.9 MB (24886310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01af261a6c29946e34b32228d294c69a86ca06cdfd0b0cfafbb568e9fc6b57b3`  
		Last Modified: Tue, 23 Nov 2021 22:08:39 GMT  
		Size: 2.5 MB (2462561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c562f4f3fb32ceeded7f153ed48a677c98f4efaee9d19ed32a8fcfa7fe236b27`  
		Last Modified: Tue, 23 Nov 2021 22:08:52 GMT  
		Size: 24.5 MB (24493189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0.122-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:abbc7a96a87a8fc3a75f3f9ee465f954103af6cb8caeeb2a58dcfa5775d9a5a6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48899010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:888f04b4468fa13c7dd2d4d3e6758e38cd6a1f2b8743d602ea8d6170470bc53f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:00:46 GMT
ADD file:4ac0de0d740f0c221cd4f912861a67009942fa5bdad24ac8b62c690dfa15024a in / 
# Wed, 17 Nov 2021 02:00:47 GMT
CMD ["bash"]
# Tue, 23 Nov 2021 22:28:21 GMT
ENV MONO_VERSION=6.12.0.122
# Tue, 23 Nov 2021 22:28:52 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 23 Nov 2021 22:29:35 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7bd9e64406c6f3044bd15f89c367f07ec4eaafb1035a5c3ee2f7b138be68017f`  
		Last Modified: Wed, 17 Nov 2021 02:16:39 GMT  
		Size: 22.8 MB (22754359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:049b685383367eaa00b28d290b7f521588cc2a6fddec236420129ec04830f7ad`  
		Last Modified: Tue, 23 Nov 2021 22:38:55 GMT  
		Size: 2.4 MB (2361954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d696071cf20a8d6e7031e1c8c4453e1fcbd73fbd07d0e299ab428402906f012c`  
		Last Modified: Tue, 23 Nov 2021 22:39:06 GMT  
		Size: 23.8 MB (23782697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0.122-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:c8b6095166e5103eaa00541e4c8296a5082fc22f8b0c47f22b68524841854dda
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.9 MB (57875944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d2788a0d6a78feae4f3714b45819c05d06a535d1d2cd624e9cdb52386b96ff3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:40:44 GMT
ADD file:b7921dd77c7620d46a18a4b5952557620210bf7ad9de20fe8e695a371188122a in / 
# Wed, 17 Nov 2021 02:40:44 GMT
CMD ["bash"]
# Tue, 23 Nov 2021 21:51:44 GMT
ENV MONO_VERSION=6.12.0.122
# Tue, 23 Nov 2021 21:51:59 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 23 Nov 2021 21:52:15 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:8ccb9871ed7bebcea8889b08e06fe5bd0116711ca7b110429b987475bf4d40e8`  
		Last Modified: Wed, 17 Nov 2021 02:48:07 GMT  
		Size: 25.9 MB (25923117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9d1d375755ac6c8647c886eb68f427d617cb789ae0c98372e585311a5395aa0`  
		Last Modified: Tue, 23 Nov 2021 21:57:01 GMT  
		Size: 2.6 MB (2634589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a5575918894c723f49db7b67bad957b34f1f6b88828b67489943f4618f2fdc4`  
		Last Modified: Tue, 23 Nov 2021 21:57:05 GMT  
		Size: 29.3 MB (29318238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0.122-slim` - linux; 386

```console
$ docker pull mono@sha256:d5c218c6f846f064e3d68efb7e677d60a558d54067c13fe5a9554b1b6d2b8bdd
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.4 MB (99364574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2145d963dc4718d45ccb94e26a0153de7d7f1ee66964d3607401681ae010517d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:40:22 GMT
ADD file:2adea3474b7ebda2bf77361304ee3e6966a9118aafd8220b81c4027be1f4d583 in / 
# Wed, 17 Nov 2021 02:40:22 GMT
CMD ["bash"]
# Tue, 23 Nov 2021 21:42:03 GMT
ENV MONO_VERSION=6.12.0.122
# Tue, 23 Nov 2021 21:42:22 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 23 Nov 2021 21:42:48 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7af5c9e671306e395c50a515c7bbe33d6f418ea08535b01c884457f78114eb08`  
		Last Modified: Wed, 17 Nov 2021 02:48:49 GMT  
		Size: 27.8 MB (27804550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:178b44cff3441bdb1ada9b30fbb42c9e7143127e42b7e4715f38610b2d122927`  
		Last Modified: Tue, 23 Nov 2021 21:47:45 GMT  
		Size: 2.8 MB (2781502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b82f010a190c7a767fdbe0299862791645a573a4844487ee187efe7e6a34941`  
		Last Modified: Tue, 23 Nov 2021 21:47:59 GMT  
		Size: 68.8 MB (68778522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:latest`

```console
$ docker pull mono@sha256:b04d988ca0c1985b75f30422238cd0cf6cac7030e8492117b2ea2fd25194f6a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:latest` - linux; amd64

```console
$ docker pull mono@sha256:481fce9886677b30abb23cf0b1aa5d477482a89b02f1207d0ef6cd6f462357bf
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.1 MB (236118149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0973a336ea5cc60790a8d4d304b05ddb030fea89166482e2d2372c9b1d6abf1e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:21:02 GMT
ADD file:3c54ad257f2e04f7294ce879b884820cf4726c8e93ec548172825963e40c79ad in / 
# Wed, 17 Nov 2021 02:21:02 GMT
CMD ["bash"]
# Tue, 23 Nov 2021 22:35:14 GMT
ENV MONO_VERSION=6.12.0.122
# Tue, 23 Nov 2021 22:35:29 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 23 Nov 2021 22:35:48 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 23 Nov 2021 22:41:26 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a10c77af261312e7c92bcc184f2d1726175ff7f142e44b01c5779cd79348b9fd`  
		Last Modified: Wed, 17 Nov 2021 02:26:31 GMT  
		Size: 27.2 MB (27153675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:290db4dba8dd1a22feca175d2300b4ca8dd16fe86ecc6022a566329a5b654ecf`  
		Last Modified: Tue, 23 Nov 2021 22:48:37 GMT  
		Size: 2.8 MB (2766933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbb78a53a304279c9bb401cfd5979e972f8fc1e746e9d36fc42525cd0676e372`  
		Last Modified: Tue, 23 Nov 2021 22:48:50 GMT  
		Size: 64.8 MB (64759889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b2ee3bb2622395bc301b422eccf0178ef24425f0fbd2392e582b3858628472c`  
		Last Modified: Tue, 23 Nov 2021 22:49:59 GMT  
		Size: 141.4 MB (141437652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:latest` - linux; arm variant v5

```console
$ docker pull mono@sha256:32c6613aba67088647674775dc9bc4936d1495cf10902d45fc8f51eb726a6a9c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.9 MB (191928998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4777f90f93be6f3b59383b98fa7e7ae724fadac57fde9062cba89d56d422826`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:51:39 GMT
ADD file:e580d4d2066301375327ea51dd8db3af956e5a465495bf09d69d6deec9b0bfae in / 
# Wed, 17 Nov 2021 02:51:40 GMT
CMD ["bash"]
# Tue, 23 Nov 2021 21:57:24 GMT
ENV MONO_VERSION=6.12.0.122
# Tue, 23 Nov 2021 21:57:55 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 23 Nov 2021 21:58:42 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 23 Nov 2021 22:03:49 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:dba255a4b166bb02562ca152d0da236ba8f211de5bf9d79e35ee023b1fce203e`  
		Last Modified: Wed, 17 Nov 2021 03:07:41 GMT  
		Size: 24.9 MB (24886310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01af261a6c29946e34b32228d294c69a86ca06cdfd0b0cfafbb568e9fc6b57b3`  
		Last Modified: Tue, 23 Nov 2021 22:08:39 GMT  
		Size: 2.5 MB (2462561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c562f4f3fb32ceeded7f153ed48a677c98f4efaee9d19ed32a8fcfa7fe236b27`  
		Last Modified: Tue, 23 Nov 2021 22:08:52 GMT  
		Size: 24.5 MB (24493189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6142af18d42fb857ff86fc8a7f00fbd715e0d8db30845d2424ff947cd9058276`  
		Last Modified: Tue, 23 Nov 2021 22:11:15 GMT  
		Size: 140.1 MB (140086938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:latest` - linux; arm variant v7

```console
$ docker pull mono@sha256:224100530ddf0867a699f0e1448fd2646c62e088c97bbe9fea0cfa488e8813c4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.8 MB (187845574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a6b45021de699193ede4308d6e2ae5eb2cc57e8def386c8a6e60d7a52c2c704`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:00:46 GMT
ADD file:4ac0de0d740f0c221cd4f912861a67009942fa5bdad24ac8b62c690dfa15024a in / 
# Wed, 17 Nov 2021 02:00:47 GMT
CMD ["bash"]
# Tue, 23 Nov 2021 22:28:21 GMT
ENV MONO_VERSION=6.12.0.122
# Tue, 23 Nov 2021 22:28:52 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 23 Nov 2021 22:29:35 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 23 Nov 2021 22:34:09 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7bd9e64406c6f3044bd15f89c367f07ec4eaafb1035a5c3ee2f7b138be68017f`  
		Last Modified: Wed, 17 Nov 2021 02:16:39 GMT  
		Size: 22.8 MB (22754359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:049b685383367eaa00b28d290b7f521588cc2a6fddec236420129ec04830f7ad`  
		Last Modified: Tue, 23 Nov 2021 22:38:55 GMT  
		Size: 2.4 MB (2361954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d696071cf20a8d6e7031e1c8c4453e1fcbd73fbd07d0e299ab428402906f012c`  
		Last Modified: Tue, 23 Nov 2021 22:39:06 GMT  
		Size: 23.8 MB (23782697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f919fba63d40094ff8de7041bdf8ea1ea33c8fb98dec1524acc0ddb1c7144658`  
		Last Modified: Tue, 23 Nov 2021 22:41:39 GMT  
		Size: 138.9 MB (138946564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:latest` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:f51c87edd3a0bb05ecb545084c025665f2a4cc4c47b21b9fd7bd712ac9c8fd4b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.5 MB (214451528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32097382767f78b6abfadcb70f6979c659ec28225f0c64f08bdd820d4cb582f9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:40:44 GMT
ADD file:b7921dd77c7620d46a18a4b5952557620210bf7ad9de20fe8e695a371188122a in / 
# Wed, 17 Nov 2021 02:40:44 GMT
CMD ["bash"]
# Tue, 23 Nov 2021 21:51:44 GMT
ENV MONO_VERSION=6.12.0.122
# Tue, 23 Nov 2021 21:51:59 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 23 Nov 2021 21:52:15 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 23 Nov 2021 21:54:06 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:8ccb9871ed7bebcea8889b08e06fe5bd0116711ca7b110429b987475bf4d40e8`  
		Last Modified: Wed, 17 Nov 2021 02:48:07 GMT  
		Size: 25.9 MB (25923117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9d1d375755ac6c8647c886eb68f427d617cb789ae0c98372e585311a5395aa0`  
		Last Modified: Tue, 23 Nov 2021 21:57:01 GMT  
		Size: 2.6 MB (2634589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a5575918894c723f49db7b67bad957b34f1f6b88828b67489943f4618f2fdc4`  
		Last Modified: Tue, 23 Nov 2021 21:57:05 GMT  
		Size: 29.3 MB (29318238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ec24743e7bc80a3baec7c0697b8bd9d87e12e26d3c50e6d7e18c36dd63bd005`  
		Last Modified: Tue, 23 Nov 2021 21:58:08 GMT  
		Size: 156.6 MB (156575584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:latest` - linux; 386

```console
$ docker pull mono@sha256:487eab41ead5858f6e434ae442e99515059f95651604e49d867d41095e05f2eb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.9 MB (241920178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f058eee97b6682f2e4715db0d188185468cddc542f881b8053c7b1fbaf4567e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:40:22 GMT
ADD file:2adea3474b7ebda2bf77361304ee3e6966a9118aafd8220b81c4027be1f4d583 in / 
# Wed, 17 Nov 2021 02:40:22 GMT
CMD ["bash"]
# Tue, 23 Nov 2021 21:42:03 GMT
ENV MONO_VERSION=6.12.0.122
# Tue, 23 Nov 2021 21:42:22 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 23 Nov 2021 21:42:48 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 23 Nov 2021 21:44:49 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7af5c9e671306e395c50a515c7bbe33d6f418ea08535b01c884457f78114eb08`  
		Last Modified: Wed, 17 Nov 2021 02:48:49 GMT  
		Size: 27.8 MB (27804550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:178b44cff3441bdb1ada9b30fbb42c9e7143127e42b7e4715f38610b2d122927`  
		Last Modified: Tue, 23 Nov 2021 21:47:45 GMT  
		Size: 2.8 MB (2781502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b82f010a190c7a767fdbe0299862791645a573a4844487ee187efe7e6a34941`  
		Last Modified: Tue, 23 Nov 2021 21:47:59 GMT  
		Size: 68.8 MB (68778522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7c603a243c2c3d8943de83d6e0d8a8eaba5b511e76a1b921dcb9b576ef046b7`  
		Last Modified: Tue, 23 Nov 2021 21:49:18 GMT  
		Size: 142.6 MB (142555604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:latest` - linux; ppc64le

```console
$ docker pull mono@sha256:58c35decefee6c034da009565f9e354b1d3f0defbba53730df12f3cde2aeaeab
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.4 MB (203412519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99b8277a5b9fc92177d5f86fa33e2ff383ae55de6452afe5b1dd0d9215ba5f46`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Oct 2021 01:26:46 GMT
ADD file:5526880c6f19a4b4231a8b2bd7cfc625d116764c4918eff6f0b55f8c1eb38e1a in / 
# Tue, 12 Oct 2021 01:26:50 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 07:07:14 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 12 Oct 2021 07:08:29 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 12 Oct 2021 07:10:10 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 12 Oct 2021 07:21:13 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:d69973af32573c07c8789c0f9c144a5c0b822a1e85b59db3ce9f8ebc489ce85d`  
		Last Modified: Tue, 12 Oct 2021 01:38:40 GMT  
		Size: 30.5 MB (30547197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:411a4d07ce6468d0126e5f9f0ad6098034f004bb482027b2349909c0ebc277d4`  
		Last Modified: Tue, 12 Oct 2021 07:31:06 GMT  
		Size: 256.1 KB (256142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa7805400cade2c3fda94906cc3502961f0a85bf26f07aeb6d74f4ba6866961b`  
		Last Modified: Tue, 12 Oct 2021 07:31:12 GMT  
		Size: 29.4 MB (29359244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5bfdf96e676582679b152400f854a0a0c03af4dcd5f3abd6c9afc2068238061`  
		Last Modified: Tue, 12 Oct 2021 07:32:19 GMT  
		Size: 143.2 MB (143249936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:slim`

```console
$ docker pull mono@sha256:9d4ba66e353e699a1e0d2970e87b39e26cd619d3103cab57e29968c1a62c0c1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:slim` - linux; amd64

```console
$ docker pull mono@sha256:cdecd1e409a3bf015b2df7cab751b32aa1912942800c38c26dbbda077bd24a1d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.7 MB (94680497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:179c410963b2d950b30018aa2f7198d4bbf4750a44af79963bc2ec7eb619a78a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:21:02 GMT
ADD file:3c54ad257f2e04f7294ce879b884820cf4726c8e93ec548172825963e40c79ad in / 
# Wed, 17 Nov 2021 02:21:02 GMT
CMD ["bash"]
# Tue, 23 Nov 2021 22:35:14 GMT
ENV MONO_VERSION=6.12.0.122
# Tue, 23 Nov 2021 22:35:29 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 23 Nov 2021 22:35:48 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a10c77af261312e7c92bcc184f2d1726175ff7f142e44b01c5779cd79348b9fd`  
		Last Modified: Wed, 17 Nov 2021 02:26:31 GMT  
		Size: 27.2 MB (27153675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:290db4dba8dd1a22feca175d2300b4ca8dd16fe86ecc6022a566329a5b654ecf`  
		Last Modified: Tue, 23 Nov 2021 22:48:37 GMT  
		Size: 2.8 MB (2766933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbb78a53a304279c9bb401cfd5979e972f8fc1e746e9d36fc42525cd0676e372`  
		Last Modified: Tue, 23 Nov 2021 22:48:50 GMT  
		Size: 64.8 MB (64759889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:56e40b4d67adf3a932be68db6867706afb08420aa4ec4d1ce823c62f6369ca0a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51842060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76c279d60b298986449ea01c00551166b76185c559f47d494efc568cf54ea1c6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:51:39 GMT
ADD file:e580d4d2066301375327ea51dd8db3af956e5a465495bf09d69d6deec9b0bfae in / 
# Wed, 17 Nov 2021 02:51:40 GMT
CMD ["bash"]
# Tue, 23 Nov 2021 21:57:24 GMT
ENV MONO_VERSION=6.12.0.122
# Tue, 23 Nov 2021 21:57:55 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 23 Nov 2021 21:58:42 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:dba255a4b166bb02562ca152d0da236ba8f211de5bf9d79e35ee023b1fce203e`  
		Last Modified: Wed, 17 Nov 2021 03:07:41 GMT  
		Size: 24.9 MB (24886310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01af261a6c29946e34b32228d294c69a86ca06cdfd0b0cfafbb568e9fc6b57b3`  
		Last Modified: Tue, 23 Nov 2021 22:08:39 GMT  
		Size: 2.5 MB (2462561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c562f4f3fb32ceeded7f153ed48a677c98f4efaee9d19ed32a8fcfa7fe236b27`  
		Last Modified: Tue, 23 Nov 2021 22:08:52 GMT  
		Size: 24.5 MB (24493189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:abbc7a96a87a8fc3a75f3f9ee465f954103af6cb8caeeb2a58dcfa5775d9a5a6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48899010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:888f04b4468fa13c7dd2d4d3e6758e38cd6a1f2b8743d602ea8d6170470bc53f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:00:46 GMT
ADD file:4ac0de0d740f0c221cd4f912861a67009942fa5bdad24ac8b62c690dfa15024a in / 
# Wed, 17 Nov 2021 02:00:47 GMT
CMD ["bash"]
# Tue, 23 Nov 2021 22:28:21 GMT
ENV MONO_VERSION=6.12.0.122
# Tue, 23 Nov 2021 22:28:52 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 23 Nov 2021 22:29:35 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7bd9e64406c6f3044bd15f89c367f07ec4eaafb1035a5c3ee2f7b138be68017f`  
		Last Modified: Wed, 17 Nov 2021 02:16:39 GMT  
		Size: 22.8 MB (22754359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:049b685383367eaa00b28d290b7f521588cc2a6fddec236420129ec04830f7ad`  
		Last Modified: Tue, 23 Nov 2021 22:38:55 GMT  
		Size: 2.4 MB (2361954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d696071cf20a8d6e7031e1c8c4453e1fcbd73fbd07d0e299ab428402906f012c`  
		Last Modified: Tue, 23 Nov 2021 22:39:06 GMT  
		Size: 23.8 MB (23782697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:c8b6095166e5103eaa00541e4c8296a5082fc22f8b0c47f22b68524841854dda
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.9 MB (57875944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d2788a0d6a78feae4f3714b45819c05d06a535d1d2cd624e9cdb52386b96ff3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:40:44 GMT
ADD file:b7921dd77c7620d46a18a4b5952557620210bf7ad9de20fe8e695a371188122a in / 
# Wed, 17 Nov 2021 02:40:44 GMT
CMD ["bash"]
# Tue, 23 Nov 2021 21:51:44 GMT
ENV MONO_VERSION=6.12.0.122
# Tue, 23 Nov 2021 21:51:59 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 23 Nov 2021 21:52:15 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:8ccb9871ed7bebcea8889b08e06fe5bd0116711ca7b110429b987475bf4d40e8`  
		Last Modified: Wed, 17 Nov 2021 02:48:07 GMT  
		Size: 25.9 MB (25923117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9d1d375755ac6c8647c886eb68f427d617cb789ae0c98372e585311a5395aa0`  
		Last Modified: Tue, 23 Nov 2021 21:57:01 GMT  
		Size: 2.6 MB (2634589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a5575918894c723f49db7b67bad957b34f1f6b88828b67489943f4618f2fdc4`  
		Last Modified: Tue, 23 Nov 2021 21:57:05 GMT  
		Size: 29.3 MB (29318238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:slim` - linux; 386

```console
$ docker pull mono@sha256:d5c218c6f846f064e3d68efb7e677d60a558d54067c13fe5a9554b1b6d2b8bdd
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.4 MB (99364574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2145d963dc4718d45ccb94e26a0153de7d7f1ee66964d3607401681ae010517d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:40:22 GMT
ADD file:2adea3474b7ebda2bf77361304ee3e6966a9118aafd8220b81c4027be1f4d583 in / 
# Wed, 17 Nov 2021 02:40:22 GMT
CMD ["bash"]
# Tue, 23 Nov 2021 21:42:03 GMT
ENV MONO_VERSION=6.12.0.122
# Tue, 23 Nov 2021 21:42:22 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 23 Nov 2021 21:42:48 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7af5c9e671306e395c50a515c7bbe33d6f418ea08535b01c884457f78114eb08`  
		Last Modified: Wed, 17 Nov 2021 02:48:49 GMT  
		Size: 27.8 MB (27804550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:178b44cff3441bdb1ada9b30fbb42c9e7143127e42b7e4715f38610b2d122927`  
		Last Modified: Tue, 23 Nov 2021 21:47:45 GMT  
		Size: 2.8 MB (2781502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b82f010a190c7a767fdbe0299862791645a573a4844487ee187efe7e6a34941`  
		Last Modified: Tue, 23 Nov 2021 21:47:59 GMT  
		Size: 68.8 MB (68778522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:slim` - linux; ppc64le

```console
$ docker pull mono@sha256:7834ad815013a312211d9f24df0f88d7e3f04386d7c192b726662658029697f7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60162583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ee89c05071148752e8c61c25ab1424ba5b066d04b57a4f785fa443265cf2703`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Oct 2021 01:26:46 GMT
ADD file:5526880c6f19a4b4231a8b2bd7cfc625d116764c4918eff6f0b55f8c1eb38e1a in / 
# Tue, 12 Oct 2021 01:26:50 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 07:07:14 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 12 Oct 2021 07:08:29 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 12 Oct 2021 07:10:10 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:d69973af32573c07c8789c0f9c144a5c0b822a1e85b59db3ce9f8ebc489ce85d`  
		Last Modified: Tue, 12 Oct 2021 01:38:40 GMT  
		Size: 30.5 MB (30547197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:411a4d07ce6468d0126e5f9f0ad6098034f004bb482027b2349909c0ebc277d4`  
		Last Modified: Tue, 12 Oct 2021 07:31:06 GMT  
		Size: 256.1 KB (256142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa7805400cade2c3fda94906cc3502961f0a85bf26f07aeb6d74f4ba6866961b`  
		Last Modified: Tue, 12 Oct 2021 07:31:12 GMT  
		Size: 29.4 MB (29359244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
