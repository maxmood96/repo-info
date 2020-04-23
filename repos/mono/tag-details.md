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
$ docker pull mono@sha256:3e82694bac861af3e95a6c27463de52c9a2fda93f204e516648cf6f757de3f94
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
$ docker pull mono@sha256:5a92bf10791c43b420fc92731abd5dc7a45f917f9f045d7dfbf17189d2a8c140
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.3 MB (218271789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f85de24a0449aa4cd2d919f1e046ac62fc8328eccc323989297cfba756ec915d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 03:27:50 GMT
ADD file:40f52c233aecabf572a9db7450590d54d5e125fb00ecbb4a26fecd0b71e84eb8 in / 
# Thu, 16 Apr 2020 03:27:50 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 09:13:38 GMT
ENV MONO_VERSION=5.20.1.34
# Thu, 16 Apr 2020 09:13:48 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Apr 2020 09:14:25 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 16 Apr 2020 09:46:10 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:5e35bd43cf7898d036f8515be74d45b2e3abd2a5534fc280de63a9c22dd175bd`  
		Last Modified: Thu, 16 Apr 2020 03:35:04 GMT  
		Size: 22.5 MB (22513476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27914964de9bbbd7f3daceed10bf3b1e9b4f60b8f305449c247e05ba453e9f90`  
		Last Modified: Thu, 16 Apr 2020 09:47:20 GMT  
		Size: 244.5 KB (244500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ffb2a3a9de8dfc06d17c1ba1b8f42ccae089474466f5d3efa1e21fbf8b5918e`  
		Last Modified: Thu, 16 Apr 2020 09:47:31 GMT  
		Size: 55.5 MB (55519628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75b3f90a4605765f6721d9c5a6f5957f14c000c42d8258588eb069f98c3a547b`  
		Last Modified: Thu, 16 Apr 2020 09:49:48 GMT  
		Size: 140.0 MB (139994185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5` - linux; arm variant v5

```console
$ docker pull mono@sha256:728b3a09731eabb589d971feaf17a5833942c6843ab9cd8358b32ff1b6383cd9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.9 MB (170941920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ee915002d6e2050563346a5fc0731204436dda9794421c36437fc915a77105d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 00:54:51 GMT
ADD file:ba6c5e03457e69f59231e8e7c6465c1ec985812f0d8f7a65d9842f2be3e947fb in / 
# Thu, 16 Apr 2020 00:54:54 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 03:25:11 GMT
ENV MONO_VERSION=5.20.1.34
# Thu, 16 Apr 2020 03:25:36 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Apr 2020 03:26:21 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 16 Apr 2020 03:35:41 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:b7d527e4baf13a6c926fb354fe1b38cb42b96f249ae65fdc0f52c853b654e06e`  
		Last Modified: Thu, 16 Apr 2020 01:02:32 GMT  
		Size: 21.2 MB (21190797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8340381d358ecc9e44596343db49a1d8fe9fc408313742adb549d7acbfa010d9`  
		Last Modified: Thu, 16 Apr 2020 03:36:49 GMT  
		Size: 244.5 KB (244533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89c829c702c9ea78e5f1e834e27d5270a1aeb340e0c387fd2bcca835a6508a18`  
		Last Modified: Thu, 16 Apr 2020 03:36:59 GMT  
		Size: 24.3 MB (24265251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26391aed7c1279d19a1ba1f92bea83bd9306ccb069b953d6af33c408532dccc7`  
		Last Modified: Thu, 16 Apr 2020 03:39:37 GMT  
		Size: 125.2 MB (125241339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5` - linux; arm variant v7

```console
$ docker pull mono@sha256:259a95f5c94430a70d4bfbb3aff1c86b1c46f66e932e58986f5eb0d57da28d35
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.0 MB (166993370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25818813ac0ce16ba21dc50510c7e882df7888a2fde8c2e99ecdcfd9d9bc02f9`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 01:05:08 GMT
ADD file:e37c4728c0c89ac126542ac35e7e493425c021bfac751079c9b266821a1b4e99 in / 
# Thu, 16 Apr 2020 01:05:10 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 04:43:14 GMT
ENV MONO_VERSION=5.20.1.34
# Thu, 16 Apr 2020 04:43:33 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Apr 2020 04:44:18 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 16 Apr 2020 04:53:30 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:f78d9963dfddc4747d6200353b50f6093a6e37ca82e1612fa397d64ff13e7299`  
		Last Modified: Thu, 16 Apr 2020 01:12:33 GMT  
		Size: 19.3 MB (19298546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caf684cdea8a2272c82e09cbbb5024552c6e67b7dcf59ea62af547f9c730474e`  
		Last Modified: Thu, 16 Apr 2020 04:54:37 GMT  
		Size: 244.6 KB (244560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:249d36139d8bc596df209162b7386211edf003733b4286aa7405033282389c33`  
		Last Modified: Thu, 16 Apr 2020 04:54:47 GMT  
		Size: 23.6 MB (23562096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c90019bfc9c5e3ea379d7a72fbc13f136f207f2c152f545a4225d506472e4cec`  
		Last Modified: Thu, 16 Apr 2020 04:57:32 GMT  
		Size: 123.9 MB (123888168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:110949e51fd64f0a4861ad92137d717f431d06f6d24f8e519a5cf346185fde38
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.8 MB (187800067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d6f3e069a025df695d5e7cdae84f0ad9c50ec134a1ef7ed87c306daf10c4955`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 02:45:19 GMT
ADD file:1588320d1c43714ec0353b7471f2ffd649045ca0f5f70dcb1eb064875fff9578 in / 
# Thu, 16 Apr 2020 02:45:21 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 06:49:41 GMT
ENV MONO_VERSION=5.20.1.34
# Thu, 16 Apr 2020 06:50:01 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Apr 2020 06:50:40 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 16 Apr 2020 06:58:49 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:8978c87ff45d64d1663a585dcf1ed66d9e711c2e4048d83ef561da9514ef46e6`  
		Last Modified: Thu, 16 Apr 2020 02:51:32 GMT  
		Size: 20.4 MB (20370106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:554199a06aed010aa14e2e6ed810ac12e3f7ea1f01b4b484029b46c769a914b5`  
		Last Modified: Thu, 16 Apr 2020 07:00:00 GMT  
		Size: 244.4 KB (244384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2f9c219c23779432f95dca105f2822e4e5cce0035ec90439890cb4ba1c4b3e0`  
		Last Modified: Thu, 16 Apr 2020 07:00:06 GMT  
		Size: 28.2 MB (28156920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:706e37f95124ae6304e93e036c626bc45828f29f97c939ca3dc7b4d8d51e31f6`  
		Last Modified: Thu, 16 Apr 2020 07:02:52 GMT  
		Size: 139.0 MB (139028657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5` - linux; 386

```console
$ docker pull mono@sha256:d23260f2eb55831d7a644c2090e68183c31cd94cce445d07f31ad077313cab92
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.8 MB (227782164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:917877589f53f998a6928fe9997618f6d6fe19a80de19b911e67d5d6ec383707`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:42:13 GMT
ADD file:82f76d577eec142f824456d027e5f82f681c9f5a09aeef4f711cef4662dcaea4 in / 
# Thu, 23 Apr 2020 00:42:13 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:06:02 GMT
ENV MONO_VERSION=5.20.1.34
# Thu, 23 Apr 2020 01:06:12 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 01:06:47 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Apr 2020 01:13:57 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7cb0551c4675347b94a8c63d7ee1f99dea4ab34aa7f23602ca587b6894d0211b`  
		Last Modified: Thu, 23 Apr 2020 00:47:39 GMT  
		Size: 23.1 MB (23141423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f99a2ee486012fc5349a1f2fc838b03077a9aa47e79c414bc5af7e6be55d0ac`  
		Last Modified: Thu, 23 Apr 2020 01:15:02 GMT  
		Size: 244.5 KB (244504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3666eed20e513a6d57a046805936faf49f4e8af6f172fefa71261014ee05c479`  
		Last Modified: Thu, 23 Apr 2020 01:15:18 GMT  
		Size: 58.6 MB (58556498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bdddfacaf4baebf50319e32e2db6159513b09a35b5034627accd2490cded313`  
		Last Modified: Thu, 23 Apr 2020 01:17:45 GMT  
		Size: 145.8 MB (145839739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5` - linux; ppc64le

```console
$ docker pull mono@sha256:10f28b145295a978f9628fb30440d346accccf597d45f8b66e8d390fb00f5d12
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.3 MB (173292013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69236ccfa3a77e72c4d43a2c28acf141d1bebac5e126f5c9e4a764fa4b508c23`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 01:43:57 GMT
ADD file:1c7f60f778e4b93490d570487d56275925e5eb477632e71cb9f035ce6edf2460 in / 
# Thu, 16 Apr 2020 01:44:03 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 06:44:48 GMT
ENV MONO_VERSION=5.20.1.34
# Thu, 16 Apr 2020 06:46:25 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Apr 2020 06:47:57 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 16 Apr 2020 07:18:06 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:15e508b90ba1d327da83b72fc494ca263c1566ef6f70b91001cf2093395ffa3d`  
		Last Modified: Thu, 16 Apr 2020 02:04:33 GMT  
		Size: 22.8 MB (22785425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58f669c3fbfce943d77701b69e7857eb6d1b88bbf7f9167a449d80be23eb3243`  
		Last Modified: Thu, 16 Apr 2020 07:19:18 GMT  
		Size: 244.6 KB (244638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c16782e8edab25bcd823ec760e3d334f1009343a5a1ef80520730ea6acd56e3`  
		Last Modified: Thu, 16 Apr 2020 07:19:25 GMT  
		Size: 24.6 MB (24639647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8407cfcba2823e2d7d5cf4a042cc54da9defa5fb96119e64542272d1eb1ff98e`  
		Last Modified: Thu, 16 Apr 2020 07:21:36 GMT  
		Size: 125.6 MB (125622303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:5.20`

```console
$ docker pull mono@sha256:3e82694bac861af3e95a6c27463de52c9a2fda93f204e516648cf6f757de3f94
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
$ docker pull mono@sha256:5a92bf10791c43b420fc92731abd5dc7a45f917f9f045d7dfbf17189d2a8c140
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.3 MB (218271789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f85de24a0449aa4cd2d919f1e046ac62fc8328eccc323989297cfba756ec915d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 03:27:50 GMT
ADD file:40f52c233aecabf572a9db7450590d54d5e125fb00ecbb4a26fecd0b71e84eb8 in / 
# Thu, 16 Apr 2020 03:27:50 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 09:13:38 GMT
ENV MONO_VERSION=5.20.1.34
# Thu, 16 Apr 2020 09:13:48 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Apr 2020 09:14:25 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 16 Apr 2020 09:46:10 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:5e35bd43cf7898d036f8515be74d45b2e3abd2a5534fc280de63a9c22dd175bd`  
		Last Modified: Thu, 16 Apr 2020 03:35:04 GMT  
		Size: 22.5 MB (22513476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27914964de9bbbd7f3daceed10bf3b1e9b4f60b8f305449c247e05ba453e9f90`  
		Last Modified: Thu, 16 Apr 2020 09:47:20 GMT  
		Size: 244.5 KB (244500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ffb2a3a9de8dfc06d17c1ba1b8f42ccae089474466f5d3efa1e21fbf8b5918e`  
		Last Modified: Thu, 16 Apr 2020 09:47:31 GMT  
		Size: 55.5 MB (55519628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75b3f90a4605765f6721d9c5a6f5957f14c000c42d8258588eb069f98c3a547b`  
		Last Modified: Thu, 16 Apr 2020 09:49:48 GMT  
		Size: 140.0 MB (139994185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20` - linux; arm variant v5

```console
$ docker pull mono@sha256:728b3a09731eabb589d971feaf17a5833942c6843ab9cd8358b32ff1b6383cd9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.9 MB (170941920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ee915002d6e2050563346a5fc0731204436dda9794421c36437fc915a77105d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 00:54:51 GMT
ADD file:ba6c5e03457e69f59231e8e7c6465c1ec985812f0d8f7a65d9842f2be3e947fb in / 
# Thu, 16 Apr 2020 00:54:54 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 03:25:11 GMT
ENV MONO_VERSION=5.20.1.34
# Thu, 16 Apr 2020 03:25:36 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Apr 2020 03:26:21 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 16 Apr 2020 03:35:41 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:b7d527e4baf13a6c926fb354fe1b38cb42b96f249ae65fdc0f52c853b654e06e`  
		Last Modified: Thu, 16 Apr 2020 01:02:32 GMT  
		Size: 21.2 MB (21190797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8340381d358ecc9e44596343db49a1d8fe9fc408313742adb549d7acbfa010d9`  
		Last Modified: Thu, 16 Apr 2020 03:36:49 GMT  
		Size: 244.5 KB (244533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89c829c702c9ea78e5f1e834e27d5270a1aeb340e0c387fd2bcca835a6508a18`  
		Last Modified: Thu, 16 Apr 2020 03:36:59 GMT  
		Size: 24.3 MB (24265251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26391aed7c1279d19a1ba1f92bea83bd9306ccb069b953d6af33c408532dccc7`  
		Last Modified: Thu, 16 Apr 2020 03:39:37 GMT  
		Size: 125.2 MB (125241339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20` - linux; arm variant v7

```console
$ docker pull mono@sha256:259a95f5c94430a70d4bfbb3aff1c86b1c46f66e932e58986f5eb0d57da28d35
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.0 MB (166993370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25818813ac0ce16ba21dc50510c7e882df7888a2fde8c2e99ecdcfd9d9bc02f9`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 01:05:08 GMT
ADD file:e37c4728c0c89ac126542ac35e7e493425c021bfac751079c9b266821a1b4e99 in / 
# Thu, 16 Apr 2020 01:05:10 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 04:43:14 GMT
ENV MONO_VERSION=5.20.1.34
# Thu, 16 Apr 2020 04:43:33 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Apr 2020 04:44:18 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 16 Apr 2020 04:53:30 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:f78d9963dfddc4747d6200353b50f6093a6e37ca82e1612fa397d64ff13e7299`  
		Last Modified: Thu, 16 Apr 2020 01:12:33 GMT  
		Size: 19.3 MB (19298546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caf684cdea8a2272c82e09cbbb5024552c6e67b7dcf59ea62af547f9c730474e`  
		Last Modified: Thu, 16 Apr 2020 04:54:37 GMT  
		Size: 244.6 KB (244560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:249d36139d8bc596df209162b7386211edf003733b4286aa7405033282389c33`  
		Last Modified: Thu, 16 Apr 2020 04:54:47 GMT  
		Size: 23.6 MB (23562096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c90019bfc9c5e3ea379d7a72fbc13f136f207f2c152f545a4225d506472e4cec`  
		Last Modified: Thu, 16 Apr 2020 04:57:32 GMT  
		Size: 123.9 MB (123888168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:110949e51fd64f0a4861ad92137d717f431d06f6d24f8e519a5cf346185fde38
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.8 MB (187800067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d6f3e069a025df695d5e7cdae84f0ad9c50ec134a1ef7ed87c306daf10c4955`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 02:45:19 GMT
ADD file:1588320d1c43714ec0353b7471f2ffd649045ca0f5f70dcb1eb064875fff9578 in / 
# Thu, 16 Apr 2020 02:45:21 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 06:49:41 GMT
ENV MONO_VERSION=5.20.1.34
# Thu, 16 Apr 2020 06:50:01 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Apr 2020 06:50:40 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 16 Apr 2020 06:58:49 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:8978c87ff45d64d1663a585dcf1ed66d9e711c2e4048d83ef561da9514ef46e6`  
		Last Modified: Thu, 16 Apr 2020 02:51:32 GMT  
		Size: 20.4 MB (20370106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:554199a06aed010aa14e2e6ed810ac12e3f7ea1f01b4b484029b46c769a914b5`  
		Last Modified: Thu, 16 Apr 2020 07:00:00 GMT  
		Size: 244.4 KB (244384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2f9c219c23779432f95dca105f2822e4e5cce0035ec90439890cb4ba1c4b3e0`  
		Last Modified: Thu, 16 Apr 2020 07:00:06 GMT  
		Size: 28.2 MB (28156920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:706e37f95124ae6304e93e036c626bc45828f29f97c939ca3dc7b4d8d51e31f6`  
		Last Modified: Thu, 16 Apr 2020 07:02:52 GMT  
		Size: 139.0 MB (139028657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20` - linux; 386

```console
$ docker pull mono@sha256:d23260f2eb55831d7a644c2090e68183c31cd94cce445d07f31ad077313cab92
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.8 MB (227782164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:917877589f53f998a6928fe9997618f6d6fe19a80de19b911e67d5d6ec383707`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:42:13 GMT
ADD file:82f76d577eec142f824456d027e5f82f681c9f5a09aeef4f711cef4662dcaea4 in / 
# Thu, 23 Apr 2020 00:42:13 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:06:02 GMT
ENV MONO_VERSION=5.20.1.34
# Thu, 23 Apr 2020 01:06:12 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 01:06:47 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Apr 2020 01:13:57 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7cb0551c4675347b94a8c63d7ee1f99dea4ab34aa7f23602ca587b6894d0211b`  
		Last Modified: Thu, 23 Apr 2020 00:47:39 GMT  
		Size: 23.1 MB (23141423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f99a2ee486012fc5349a1f2fc838b03077a9aa47e79c414bc5af7e6be55d0ac`  
		Last Modified: Thu, 23 Apr 2020 01:15:02 GMT  
		Size: 244.5 KB (244504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3666eed20e513a6d57a046805936faf49f4e8af6f172fefa71261014ee05c479`  
		Last Modified: Thu, 23 Apr 2020 01:15:18 GMT  
		Size: 58.6 MB (58556498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bdddfacaf4baebf50319e32e2db6159513b09a35b5034627accd2490cded313`  
		Last Modified: Thu, 23 Apr 2020 01:17:45 GMT  
		Size: 145.8 MB (145839739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20` - linux; ppc64le

```console
$ docker pull mono@sha256:10f28b145295a978f9628fb30440d346accccf597d45f8b66e8d390fb00f5d12
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.3 MB (173292013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69236ccfa3a77e72c4d43a2c28acf141d1bebac5e126f5c9e4a764fa4b508c23`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 01:43:57 GMT
ADD file:1c7f60f778e4b93490d570487d56275925e5eb477632e71cb9f035ce6edf2460 in / 
# Thu, 16 Apr 2020 01:44:03 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 06:44:48 GMT
ENV MONO_VERSION=5.20.1.34
# Thu, 16 Apr 2020 06:46:25 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Apr 2020 06:47:57 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 16 Apr 2020 07:18:06 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:15e508b90ba1d327da83b72fc494ca263c1566ef6f70b91001cf2093395ffa3d`  
		Last Modified: Thu, 16 Apr 2020 02:04:33 GMT  
		Size: 22.8 MB (22785425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58f669c3fbfce943d77701b69e7857eb6d1b88bbf7f9167a449d80be23eb3243`  
		Last Modified: Thu, 16 Apr 2020 07:19:18 GMT  
		Size: 244.6 KB (244638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c16782e8edab25bcd823ec760e3d334f1009343a5a1ef80520730ea6acd56e3`  
		Last Modified: Thu, 16 Apr 2020 07:19:25 GMT  
		Size: 24.6 MB (24639647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8407cfcba2823e2d7d5cf4a042cc54da9defa5fb96119e64542272d1eb1ff98e`  
		Last Modified: Thu, 16 Apr 2020 07:21:36 GMT  
		Size: 125.6 MB (125622303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:5.20.1`

```console
$ docker pull mono@sha256:3e82694bac861af3e95a6c27463de52c9a2fda93f204e516648cf6f757de3f94
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
$ docker pull mono@sha256:5a92bf10791c43b420fc92731abd5dc7a45f917f9f045d7dfbf17189d2a8c140
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.3 MB (218271789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f85de24a0449aa4cd2d919f1e046ac62fc8328eccc323989297cfba756ec915d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 03:27:50 GMT
ADD file:40f52c233aecabf572a9db7450590d54d5e125fb00ecbb4a26fecd0b71e84eb8 in / 
# Thu, 16 Apr 2020 03:27:50 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 09:13:38 GMT
ENV MONO_VERSION=5.20.1.34
# Thu, 16 Apr 2020 09:13:48 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Apr 2020 09:14:25 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 16 Apr 2020 09:46:10 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:5e35bd43cf7898d036f8515be74d45b2e3abd2a5534fc280de63a9c22dd175bd`  
		Last Modified: Thu, 16 Apr 2020 03:35:04 GMT  
		Size: 22.5 MB (22513476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27914964de9bbbd7f3daceed10bf3b1e9b4f60b8f305449c247e05ba453e9f90`  
		Last Modified: Thu, 16 Apr 2020 09:47:20 GMT  
		Size: 244.5 KB (244500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ffb2a3a9de8dfc06d17c1ba1b8f42ccae089474466f5d3efa1e21fbf8b5918e`  
		Last Modified: Thu, 16 Apr 2020 09:47:31 GMT  
		Size: 55.5 MB (55519628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75b3f90a4605765f6721d9c5a6f5957f14c000c42d8258588eb069f98c3a547b`  
		Last Modified: Thu, 16 Apr 2020 09:49:48 GMT  
		Size: 140.0 MB (139994185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20.1` - linux; arm variant v5

```console
$ docker pull mono@sha256:728b3a09731eabb589d971feaf17a5833942c6843ab9cd8358b32ff1b6383cd9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.9 MB (170941920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ee915002d6e2050563346a5fc0731204436dda9794421c36437fc915a77105d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 00:54:51 GMT
ADD file:ba6c5e03457e69f59231e8e7c6465c1ec985812f0d8f7a65d9842f2be3e947fb in / 
# Thu, 16 Apr 2020 00:54:54 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 03:25:11 GMT
ENV MONO_VERSION=5.20.1.34
# Thu, 16 Apr 2020 03:25:36 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Apr 2020 03:26:21 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 16 Apr 2020 03:35:41 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:b7d527e4baf13a6c926fb354fe1b38cb42b96f249ae65fdc0f52c853b654e06e`  
		Last Modified: Thu, 16 Apr 2020 01:02:32 GMT  
		Size: 21.2 MB (21190797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8340381d358ecc9e44596343db49a1d8fe9fc408313742adb549d7acbfa010d9`  
		Last Modified: Thu, 16 Apr 2020 03:36:49 GMT  
		Size: 244.5 KB (244533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89c829c702c9ea78e5f1e834e27d5270a1aeb340e0c387fd2bcca835a6508a18`  
		Last Modified: Thu, 16 Apr 2020 03:36:59 GMT  
		Size: 24.3 MB (24265251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26391aed7c1279d19a1ba1f92bea83bd9306ccb069b953d6af33c408532dccc7`  
		Last Modified: Thu, 16 Apr 2020 03:39:37 GMT  
		Size: 125.2 MB (125241339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20.1` - linux; arm variant v7

```console
$ docker pull mono@sha256:259a95f5c94430a70d4bfbb3aff1c86b1c46f66e932e58986f5eb0d57da28d35
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.0 MB (166993370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25818813ac0ce16ba21dc50510c7e882df7888a2fde8c2e99ecdcfd9d9bc02f9`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 01:05:08 GMT
ADD file:e37c4728c0c89ac126542ac35e7e493425c021bfac751079c9b266821a1b4e99 in / 
# Thu, 16 Apr 2020 01:05:10 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 04:43:14 GMT
ENV MONO_VERSION=5.20.1.34
# Thu, 16 Apr 2020 04:43:33 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Apr 2020 04:44:18 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 16 Apr 2020 04:53:30 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:f78d9963dfddc4747d6200353b50f6093a6e37ca82e1612fa397d64ff13e7299`  
		Last Modified: Thu, 16 Apr 2020 01:12:33 GMT  
		Size: 19.3 MB (19298546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caf684cdea8a2272c82e09cbbb5024552c6e67b7dcf59ea62af547f9c730474e`  
		Last Modified: Thu, 16 Apr 2020 04:54:37 GMT  
		Size: 244.6 KB (244560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:249d36139d8bc596df209162b7386211edf003733b4286aa7405033282389c33`  
		Last Modified: Thu, 16 Apr 2020 04:54:47 GMT  
		Size: 23.6 MB (23562096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c90019bfc9c5e3ea379d7a72fbc13f136f207f2c152f545a4225d506472e4cec`  
		Last Modified: Thu, 16 Apr 2020 04:57:32 GMT  
		Size: 123.9 MB (123888168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20.1` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:110949e51fd64f0a4861ad92137d717f431d06f6d24f8e519a5cf346185fde38
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.8 MB (187800067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d6f3e069a025df695d5e7cdae84f0ad9c50ec134a1ef7ed87c306daf10c4955`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 02:45:19 GMT
ADD file:1588320d1c43714ec0353b7471f2ffd649045ca0f5f70dcb1eb064875fff9578 in / 
# Thu, 16 Apr 2020 02:45:21 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 06:49:41 GMT
ENV MONO_VERSION=5.20.1.34
# Thu, 16 Apr 2020 06:50:01 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Apr 2020 06:50:40 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 16 Apr 2020 06:58:49 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:8978c87ff45d64d1663a585dcf1ed66d9e711c2e4048d83ef561da9514ef46e6`  
		Last Modified: Thu, 16 Apr 2020 02:51:32 GMT  
		Size: 20.4 MB (20370106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:554199a06aed010aa14e2e6ed810ac12e3f7ea1f01b4b484029b46c769a914b5`  
		Last Modified: Thu, 16 Apr 2020 07:00:00 GMT  
		Size: 244.4 KB (244384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2f9c219c23779432f95dca105f2822e4e5cce0035ec90439890cb4ba1c4b3e0`  
		Last Modified: Thu, 16 Apr 2020 07:00:06 GMT  
		Size: 28.2 MB (28156920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:706e37f95124ae6304e93e036c626bc45828f29f97c939ca3dc7b4d8d51e31f6`  
		Last Modified: Thu, 16 Apr 2020 07:02:52 GMT  
		Size: 139.0 MB (139028657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20.1` - linux; 386

```console
$ docker pull mono@sha256:d23260f2eb55831d7a644c2090e68183c31cd94cce445d07f31ad077313cab92
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.8 MB (227782164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:917877589f53f998a6928fe9997618f6d6fe19a80de19b911e67d5d6ec383707`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:42:13 GMT
ADD file:82f76d577eec142f824456d027e5f82f681c9f5a09aeef4f711cef4662dcaea4 in / 
# Thu, 23 Apr 2020 00:42:13 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:06:02 GMT
ENV MONO_VERSION=5.20.1.34
# Thu, 23 Apr 2020 01:06:12 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 01:06:47 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Apr 2020 01:13:57 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7cb0551c4675347b94a8c63d7ee1f99dea4ab34aa7f23602ca587b6894d0211b`  
		Last Modified: Thu, 23 Apr 2020 00:47:39 GMT  
		Size: 23.1 MB (23141423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f99a2ee486012fc5349a1f2fc838b03077a9aa47e79c414bc5af7e6be55d0ac`  
		Last Modified: Thu, 23 Apr 2020 01:15:02 GMT  
		Size: 244.5 KB (244504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3666eed20e513a6d57a046805936faf49f4e8af6f172fefa71261014ee05c479`  
		Last Modified: Thu, 23 Apr 2020 01:15:18 GMT  
		Size: 58.6 MB (58556498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bdddfacaf4baebf50319e32e2db6159513b09a35b5034627accd2490cded313`  
		Last Modified: Thu, 23 Apr 2020 01:17:45 GMT  
		Size: 145.8 MB (145839739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20.1` - linux; ppc64le

```console
$ docker pull mono@sha256:10f28b145295a978f9628fb30440d346accccf597d45f8b66e8d390fb00f5d12
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.3 MB (173292013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69236ccfa3a77e72c4d43a2c28acf141d1bebac5e126f5c9e4a764fa4b508c23`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 01:43:57 GMT
ADD file:1c7f60f778e4b93490d570487d56275925e5eb477632e71cb9f035ce6edf2460 in / 
# Thu, 16 Apr 2020 01:44:03 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 06:44:48 GMT
ENV MONO_VERSION=5.20.1.34
# Thu, 16 Apr 2020 06:46:25 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Apr 2020 06:47:57 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 16 Apr 2020 07:18:06 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:15e508b90ba1d327da83b72fc494ca263c1566ef6f70b91001cf2093395ffa3d`  
		Last Modified: Thu, 16 Apr 2020 02:04:33 GMT  
		Size: 22.8 MB (22785425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58f669c3fbfce943d77701b69e7857eb6d1b88bbf7f9167a449d80be23eb3243`  
		Last Modified: Thu, 16 Apr 2020 07:19:18 GMT  
		Size: 244.6 KB (244638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c16782e8edab25bcd823ec760e3d334f1009343a5a1ef80520730ea6acd56e3`  
		Last Modified: Thu, 16 Apr 2020 07:19:25 GMT  
		Size: 24.6 MB (24639647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8407cfcba2823e2d7d5cf4a042cc54da9defa5fb96119e64542272d1eb1ff98e`  
		Last Modified: Thu, 16 Apr 2020 07:21:36 GMT  
		Size: 125.6 MB (125622303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:5.20.1.34`

```console
$ docker pull mono@sha256:3e82694bac861af3e95a6c27463de52c9a2fda93f204e516648cf6f757de3f94
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
$ docker pull mono@sha256:5a92bf10791c43b420fc92731abd5dc7a45f917f9f045d7dfbf17189d2a8c140
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.3 MB (218271789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f85de24a0449aa4cd2d919f1e046ac62fc8328eccc323989297cfba756ec915d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 03:27:50 GMT
ADD file:40f52c233aecabf572a9db7450590d54d5e125fb00ecbb4a26fecd0b71e84eb8 in / 
# Thu, 16 Apr 2020 03:27:50 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 09:13:38 GMT
ENV MONO_VERSION=5.20.1.34
# Thu, 16 Apr 2020 09:13:48 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Apr 2020 09:14:25 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 16 Apr 2020 09:46:10 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:5e35bd43cf7898d036f8515be74d45b2e3abd2a5534fc280de63a9c22dd175bd`  
		Last Modified: Thu, 16 Apr 2020 03:35:04 GMT  
		Size: 22.5 MB (22513476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27914964de9bbbd7f3daceed10bf3b1e9b4f60b8f305449c247e05ba453e9f90`  
		Last Modified: Thu, 16 Apr 2020 09:47:20 GMT  
		Size: 244.5 KB (244500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ffb2a3a9de8dfc06d17c1ba1b8f42ccae089474466f5d3efa1e21fbf8b5918e`  
		Last Modified: Thu, 16 Apr 2020 09:47:31 GMT  
		Size: 55.5 MB (55519628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75b3f90a4605765f6721d9c5a6f5957f14c000c42d8258588eb069f98c3a547b`  
		Last Modified: Thu, 16 Apr 2020 09:49:48 GMT  
		Size: 140.0 MB (139994185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20.1.34` - linux; arm variant v5

```console
$ docker pull mono@sha256:728b3a09731eabb589d971feaf17a5833942c6843ab9cd8358b32ff1b6383cd9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.9 MB (170941920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ee915002d6e2050563346a5fc0731204436dda9794421c36437fc915a77105d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 00:54:51 GMT
ADD file:ba6c5e03457e69f59231e8e7c6465c1ec985812f0d8f7a65d9842f2be3e947fb in / 
# Thu, 16 Apr 2020 00:54:54 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 03:25:11 GMT
ENV MONO_VERSION=5.20.1.34
# Thu, 16 Apr 2020 03:25:36 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Apr 2020 03:26:21 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 16 Apr 2020 03:35:41 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:b7d527e4baf13a6c926fb354fe1b38cb42b96f249ae65fdc0f52c853b654e06e`  
		Last Modified: Thu, 16 Apr 2020 01:02:32 GMT  
		Size: 21.2 MB (21190797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8340381d358ecc9e44596343db49a1d8fe9fc408313742adb549d7acbfa010d9`  
		Last Modified: Thu, 16 Apr 2020 03:36:49 GMT  
		Size: 244.5 KB (244533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89c829c702c9ea78e5f1e834e27d5270a1aeb340e0c387fd2bcca835a6508a18`  
		Last Modified: Thu, 16 Apr 2020 03:36:59 GMT  
		Size: 24.3 MB (24265251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26391aed7c1279d19a1ba1f92bea83bd9306ccb069b953d6af33c408532dccc7`  
		Last Modified: Thu, 16 Apr 2020 03:39:37 GMT  
		Size: 125.2 MB (125241339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20.1.34` - linux; arm variant v7

```console
$ docker pull mono@sha256:259a95f5c94430a70d4bfbb3aff1c86b1c46f66e932e58986f5eb0d57da28d35
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.0 MB (166993370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25818813ac0ce16ba21dc50510c7e882df7888a2fde8c2e99ecdcfd9d9bc02f9`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 01:05:08 GMT
ADD file:e37c4728c0c89ac126542ac35e7e493425c021bfac751079c9b266821a1b4e99 in / 
# Thu, 16 Apr 2020 01:05:10 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 04:43:14 GMT
ENV MONO_VERSION=5.20.1.34
# Thu, 16 Apr 2020 04:43:33 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Apr 2020 04:44:18 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 16 Apr 2020 04:53:30 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:f78d9963dfddc4747d6200353b50f6093a6e37ca82e1612fa397d64ff13e7299`  
		Last Modified: Thu, 16 Apr 2020 01:12:33 GMT  
		Size: 19.3 MB (19298546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caf684cdea8a2272c82e09cbbb5024552c6e67b7dcf59ea62af547f9c730474e`  
		Last Modified: Thu, 16 Apr 2020 04:54:37 GMT  
		Size: 244.6 KB (244560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:249d36139d8bc596df209162b7386211edf003733b4286aa7405033282389c33`  
		Last Modified: Thu, 16 Apr 2020 04:54:47 GMT  
		Size: 23.6 MB (23562096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c90019bfc9c5e3ea379d7a72fbc13f136f207f2c152f545a4225d506472e4cec`  
		Last Modified: Thu, 16 Apr 2020 04:57:32 GMT  
		Size: 123.9 MB (123888168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20.1.34` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:110949e51fd64f0a4861ad92137d717f431d06f6d24f8e519a5cf346185fde38
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.8 MB (187800067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d6f3e069a025df695d5e7cdae84f0ad9c50ec134a1ef7ed87c306daf10c4955`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 02:45:19 GMT
ADD file:1588320d1c43714ec0353b7471f2ffd649045ca0f5f70dcb1eb064875fff9578 in / 
# Thu, 16 Apr 2020 02:45:21 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 06:49:41 GMT
ENV MONO_VERSION=5.20.1.34
# Thu, 16 Apr 2020 06:50:01 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Apr 2020 06:50:40 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 16 Apr 2020 06:58:49 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:8978c87ff45d64d1663a585dcf1ed66d9e711c2e4048d83ef561da9514ef46e6`  
		Last Modified: Thu, 16 Apr 2020 02:51:32 GMT  
		Size: 20.4 MB (20370106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:554199a06aed010aa14e2e6ed810ac12e3f7ea1f01b4b484029b46c769a914b5`  
		Last Modified: Thu, 16 Apr 2020 07:00:00 GMT  
		Size: 244.4 KB (244384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2f9c219c23779432f95dca105f2822e4e5cce0035ec90439890cb4ba1c4b3e0`  
		Last Modified: Thu, 16 Apr 2020 07:00:06 GMT  
		Size: 28.2 MB (28156920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:706e37f95124ae6304e93e036c626bc45828f29f97c939ca3dc7b4d8d51e31f6`  
		Last Modified: Thu, 16 Apr 2020 07:02:52 GMT  
		Size: 139.0 MB (139028657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20.1.34` - linux; 386

```console
$ docker pull mono@sha256:d23260f2eb55831d7a644c2090e68183c31cd94cce445d07f31ad077313cab92
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.8 MB (227782164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:917877589f53f998a6928fe9997618f6d6fe19a80de19b911e67d5d6ec383707`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:42:13 GMT
ADD file:82f76d577eec142f824456d027e5f82f681c9f5a09aeef4f711cef4662dcaea4 in / 
# Thu, 23 Apr 2020 00:42:13 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:06:02 GMT
ENV MONO_VERSION=5.20.1.34
# Thu, 23 Apr 2020 01:06:12 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 01:06:47 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Apr 2020 01:13:57 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7cb0551c4675347b94a8c63d7ee1f99dea4ab34aa7f23602ca587b6894d0211b`  
		Last Modified: Thu, 23 Apr 2020 00:47:39 GMT  
		Size: 23.1 MB (23141423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f99a2ee486012fc5349a1f2fc838b03077a9aa47e79c414bc5af7e6be55d0ac`  
		Last Modified: Thu, 23 Apr 2020 01:15:02 GMT  
		Size: 244.5 KB (244504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3666eed20e513a6d57a046805936faf49f4e8af6f172fefa71261014ee05c479`  
		Last Modified: Thu, 23 Apr 2020 01:15:18 GMT  
		Size: 58.6 MB (58556498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bdddfacaf4baebf50319e32e2db6159513b09a35b5034627accd2490cded313`  
		Last Modified: Thu, 23 Apr 2020 01:17:45 GMT  
		Size: 145.8 MB (145839739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20.1.34` - linux; ppc64le

```console
$ docker pull mono@sha256:10f28b145295a978f9628fb30440d346accccf597d45f8b66e8d390fb00f5d12
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.3 MB (173292013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69236ccfa3a77e72c4d43a2c28acf141d1bebac5e126f5c9e4a764fa4b508c23`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 01:43:57 GMT
ADD file:1c7f60f778e4b93490d570487d56275925e5eb477632e71cb9f035ce6edf2460 in / 
# Thu, 16 Apr 2020 01:44:03 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 06:44:48 GMT
ENV MONO_VERSION=5.20.1.34
# Thu, 16 Apr 2020 06:46:25 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Apr 2020 06:47:57 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 16 Apr 2020 07:18:06 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:15e508b90ba1d327da83b72fc494ca263c1566ef6f70b91001cf2093395ffa3d`  
		Last Modified: Thu, 16 Apr 2020 02:04:33 GMT  
		Size: 22.8 MB (22785425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58f669c3fbfce943d77701b69e7857eb6d1b88bbf7f9167a449d80be23eb3243`  
		Last Modified: Thu, 16 Apr 2020 07:19:18 GMT  
		Size: 244.6 KB (244638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c16782e8edab25bcd823ec760e3d334f1009343a5a1ef80520730ea6acd56e3`  
		Last Modified: Thu, 16 Apr 2020 07:19:25 GMT  
		Size: 24.6 MB (24639647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8407cfcba2823e2d7d5cf4a042cc54da9defa5fb96119e64542272d1eb1ff98e`  
		Last Modified: Thu, 16 Apr 2020 07:21:36 GMT  
		Size: 125.6 MB (125622303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:5.20.1.34-slim`

```console
$ docker pull mono@sha256:f54d8a6f6d24cb0f4a77dc81054eacdf2cddc792cb433fc1993b69c22748af3c
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
$ docker pull mono@sha256:6412a9e5863081fae60b17b4b60622acbd385f9f6187b2d6bdf7f3f657de1352
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.3 MB (78277604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ec8523ec89cdaca7f4e9500615ae1200ab87254843543f0e87bb510b0766e7c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 03:27:50 GMT
ADD file:40f52c233aecabf572a9db7450590d54d5e125fb00ecbb4a26fecd0b71e84eb8 in / 
# Thu, 16 Apr 2020 03:27:50 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 09:13:38 GMT
ENV MONO_VERSION=5.20.1.34
# Thu, 16 Apr 2020 09:13:48 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Apr 2020 09:14:25 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:5e35bd43cf7898d036f8515be74d45b2e3abd2a5534fc280de63a9c22dd175bd`  
		Last Modified: Thu, 16 Apr 2020 03:35:04 GMT  
		Size: 22.5 MB (22513476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27914964de9bbbd7f3daceed10bf3b1e9b4f60b8f305449c247e05ba453e9f90`  
		Last Modified: Thu, 16 Apr 2020 09:47:20 GMT  
		Size: 244.5 KB (244500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ffb2a3a9de8dfc06d17c1ba1b8f42ccae089474466f5d3efa1e21fbf8b5918e`  
		Last Modified: Thu, 16 Apr 2020 09:47:31 GMT  
		Size: 55.5 MB (55519628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20.1.34-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:24277a451c25923284bd552e52a477c6d5f0550d5bc4bf36c6f011cdab833f5a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45700581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19ded18f1bc26bdd165c560e353704c774e72c61edf6306f0a301734b1cd592d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 00:54:51 GMT
ADD file:ba6c5e03457e69f59231e8e7c6465c1ec985812f0d8f7a65d9842f2be3e947fb in / 
# Thu, 16 Apr 2020 00:54:54 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 03:25:11 GMT
ENV MONO_VERSION=5.20.1.34
# Thu, 16 Apr 2020 03:25:36 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Apr 2020 03:26:21 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:b7d527e4baf13a6c926fb354fe1b38cb42b96f249ae65fdc0f52c853b654e06e`  
		Last Modified: Thu, 16 Apr 2020 01:02:32 GMT  
		Size: 21.2 MB (21190797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8340381d358ecc9e44596343db49a1d8fe9fc408313742adb549d7acbfa010d9`  
		Last Modified: Thu, 16 Apr 2020 03:36:49 GMT  
		Size: 244.5 KB (244533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89c829c702c9ea78e5f1e834e27d5270a1aeb340e0c387fd2bcca835a6508a18`  
		Last Modified: Thu, 16 Apr 2020 03:36:59 GMT  
		Size: 24.3 MB (24265251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20.1.34-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:82879b2317895d2b306e14bd38f26be346070655d8441662bd05aa9f85797783
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.1 MB (43105202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab6576fb1edf563a52cf0994636f3e1619b6508c783b4906ed59494f06d03533`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 01:05:08 GMT
ADD file:e37c4728c0c89ac126542ac35e7e493425c021bfac751079c9b266821a1b4e99 in / 
# Thu, 16 Apr 2020 01:05:10 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 04:43:14 GMT
ENV MONO_VERSION=5.20.1.34
# Thu, 16 Apr 2020 04:43:33 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Apr 2020 04:44:18 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:f78d9963dfddc4747d6200353b50f6093a6e37ca82e1612fa397d64ff13e7299`  
		Last Modified: Thu, 16 Apr 2020 01:12:33 GMT  
		Size: 19.3 MB (19298546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caf684cdea8a2272c82e09cbbb5024552c6e67b7dcf59ea62af547f9c730474e`  
		Last Modified: Thu, 16 Apr 2020 04:54:37 GMT  
		Size: 244.6 KB (244560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:249d36139d8bc596df209162b7386211edf003733b4286aa7405033282389c33`  
		Last Modified: Thu, 16 Apr 2020 04:54:47 GMT  
		Size: 23.6 MB (23562096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20.1.34-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:373e3d9ccf313cac211d9ede8eec8a2ccb1d1c0303fc5312fddfccc026277c41
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48771410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43f116c952bab72566e217b3d9571b9572c6e2ac731995c266825ca5ff059e14`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 02:45:19 GMT
ADD file:1588320d1c43714ec0353b7471f2ffd649045ca0f5f70dcb1eb064875fff9578 in / 
# Thu, 16 Apr 2020 02:45:21 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 06:49:41 GMT
ENV MONO_VERSION=5.20.1.34
# Thu, 16 Apr 2020 06:50:01 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Apr 2020 06:50:40 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:8978c87ff45d64d1663a585dcf1ed66d9e711c2e4048d83ef561da9514ef46e6`  
		Last Modified: Thu, 16 Apr 2020 02:51:32 GMT  
		Size: 20.4 MB (20370106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:554199a06aed010aa14e2e6ed810ac12e3f7ea1f01b4b484029b46c769a914b5`  
		Last Modified: Thu, 16 Apr 2020 07:00:00 GMT  
		Size: 244.4 KB (244384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2f9c219c23779432f95dca105f2822e4e5cce0035ec90439890cb4ba1c4b3e0`  
		Last Modified: Thu, 16 Apr 2020 07:00:06 GMT  
		Size: 28.2 MB (28156920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20.1.34-slim` - linux; 386

```console
$ docker pull mono@sha256:f298a5136fcc732fb7f7c1b06514978d91489ec0402751f79366829250420a41
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.9 MB (81942425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4471b379bc228d2d7acf3bf17250d5dc21bc3475d42956005eef5b84e23100b8`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:42:13 GMT
ADD file:82f76d577eec142f824456d027e5f82f681c9f5a09aeef4f711cef4662dcaea4 in / 
# Thu, 23 Apr 2020 00:42:13 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:06:02 GMT
ENV MONO_VERSION=5.20.1.34
# Thu, 23 Apr 2020 01:06:12 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 01:06:47 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7cb0551c4675347b94a8c63d7ee1f99dea4ab34aa7f23602ca587b6894d0211b`  
		Last Modified: Thu, 23 Apr 2020 00:47:39 GMT  
		Size: 23.1 MB (23141423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f99a2ee486012fc5349a1f2fc838b03077a9aa47e79c414bc5af7e6be55d0ac`  
		Last Modified: Thu, 23 Apr 2020 01:15:02 GMT  
		Size: 244.5 KB (244504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3666eed20e513a6d57a046805936faf49f4e8af6f172fefa71261014ee05c479`  
		Last Modified: Thu, 23 Apr 2020 01:15:18 GMT  
		Size: 58.6 MB (58556498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20.1.34-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:8075f272b67d3b0230b83dec1f4ea321e0f9e68390fb4208b5cbfbde3e339a6c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47669710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b4f4a283b7df8fb74adb07675407330610860bf778c831f068775f705090dfd`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 01:43:57 GMT
ADD file:1c7f60f778e4b93490d570487d56275925e5eb477632e71cb9f035ce6edf2460 in / 
# Thu, 16 Apr 2020 01:44:03 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 06:44:48 GMT
ENV MONO_VERSION=5.20.1.34
# Thu, 16 Apr 2020 06:46:25 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Apr 2020 06:47:57 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:15e508b90ba1d327da83b72fc494ca263c1566ef6f70b91001cf2093395ffa3d`  
		Last Modified: Thu, 16 Apr 2020 02:04:33 GMT  
		Size: 22.8 MB (22785425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58f669c3fbfce943d77701b69e7857eb6d1b88bbf7f9167a449d80be23eb3243`  
		Last Modified: Thu, 16 Apr 2020 07:19:18 GMT  
		Size: 244.6 KB (244638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c16782e8edab25bcd823ec760e3d334f1009343a5a1ef80520730ea6acd56e3`  
		Last Modified: Thu, 16 Apr 2020 07:19:25 GMT  
		Size: 24.6 MB (24639647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:5.20.1-slim`

```console
$ docker pull mono@sha256:f54d8a6f6d24cb0f4a77dc81054eacdf2cddc792cb433fc1993b69c22748af3c
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
$ docker pull mono@sha256:6412a9e5863081fae60b17b4b60622acbd385f9f6187b2d6bdf7f3f657de1352
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.3 MB (78277604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ec8523ec89cdaca7f4e9500615ae1200ab87254843543f0e87bb510b0766e7c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 03:27:50 GMT
ADD file:40f52c233aecabf572a9db7450590d54d5e125fb00ecbb4a26fecd0b71e84eb8 in / 
# Thu, 16 Apr 2020 03:27:50 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 09:13:38 GMT
ENV MONO_VERSION=5.20.1.34
# Thu, 16 Apr 2020 09:13:48 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Apr 2020 09:14:25 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:5e35bd43cf7898d036f8515be74d45b2e3abd2a5534fc280de63a9c22dd175bd`  
		Last Modified: Thu, 16 Apr 2020 03:35:04 GMT  
		Size: 22.5 MB (22513476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27914964de9bbbd7f3daceed10bf3b1e9b4f60b8f305449c247e05ba453e9f90`  
		Last Modified: Thu, 16 Apr 2020 09:47:20 GMT  
		Size: 244.5 KB (244500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ffb2a3a9de8dfc06d17c1ba1b8f42ccae089474466f5d3efa1e21fbf8b5918e`  
		Last Modified: Thu, 16 Apr 2020 09:47:31 GMT  
		Size: 55.5 MB (55519628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20.1-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:24277a451c25923284bd552e52a477c6d5f0550d5bc4bf36c6f011cdab833f5a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45700581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19ded18f1bc26bdd165c560e353704c774e72c61edf6306f0a301734b1cd592d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 00:54:51 GMT
ADD file:ba6c5e03457e69f59231e8e7c6465c1ec985812f0d8f7a65d9842f2be3e947fb in / 
# Thu, 16 Apr 2020 00:54:54 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 03:25:11 GMT
ENV MONO_VERSION=5.20.1.34
# Thu, 16 Apr 2020 03:25:36 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Apr 2020 03:26:21 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:b7d527e4baf13a6c926fb354fe1b38cb42b96f249ae65fdc0f52c853b654e06e`  
		Last Modified: Thu, 16 Apr 2020 01:02:32 GMT  
		Size: 21.2 MB (21190797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8340381d358ecc9e44596343db49a1d8fe9fc408313742adb549d7acbfa010d9`  
		Last Modified: Thu, 16 Apr 2020 03:36:49 GMT  
		Size: 244.5 KB (244533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89c829c702c9ea78e5f1e834e27d5270a1aeb340e0c387fd2bcca835a6508a18`  
		Last Modified: Thu, 16 Apr 2020 03:36:59 GMT  
		Size: 24.3 MB (24265251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20.1-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:82879b2317895d2b306e14bd38f26be346070655d8441662bd05aa9f85797783
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.1 MB (43105202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab6576fb1edf563a52cf0994636f3e1619b6508c783b4906ed59494f06d03533`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 01:05:08 GMT
ADD file:e37c4728c0c89ac126542ac35e7e493425c021bfac751079c9b266821a1b4e99 in / 
# Thu, 16 Apr 2020 01:05:10 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 04:43:14 GMT
ENV MONO_VERSION=5.20.1.34
# Thu, 16 Apr 2020 04:43:33 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Apr 2020 04:44:18 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:f78d9963dfddc4747d6200353b50f6093a6e37ca82e1612fa397d64ff13e7299`  
		Last Modified: Thu, 16 Apr 2020 01:12:33 GMT  
		Size: 19.3 MB (19298546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caf684cdea8a2272c82e09cbbb5024552c6e67b7dcf59ea62af547f9c730474e`  
		Last Modified: Thu, 16 Apr 2020 04:54:37 GMT  
		Size: 244.6 KB (244560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:249d36139d8bc596df209162b7386211edf003733b4286aa7405033282389c33`  
		Last Modified: Thu, 16 Apr 2020 04:54:47 GMT  
		Size: 23.6 MB (23562096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20.1-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:373e3d9ccf313cac211d9ede8eec8a2ccb1d1c0303fc5312fddfccc026277c41
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48771410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43f116c952bab72566e217b3d9571b9572c6e2ac731995c266825ca5ff059e14`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 02:45:19 GMT
ADD file:1588320d1c43714ec0353b7471f2ffd649045ca0f5f70dcb1eb064875fff9578 in / 
# Thu, 16 Apr 2020 02:45:21 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 06:49:41 GMT
ENV MONO_VERSION=5.20.1.34
# Thu, 16 Apr 2020 06:50:01 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Apr 2020 06:50:40 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:8978c87ff45d64d1663a585dcf1ed66d9e711c2e4048d83ef561da9514ef46e6`  
		Last Modified: Thu, 16 Apr 2020 02:51:32 GMT  
		Size: 20.4 MB (20370106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:554199a06aed010aa14e2e6ed810ac12e3f7ea1f01b4b484029b46c769a914b5`  
		Last Modified: Thu, 16 Apr 2020 07:00:00 GMT  
		Size: 244.4 KB (244384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2f9c219c23779432f95dca105f2822e4e5cce0035ec90439890cb4ba1c4b3e0`  
		Last Modified: Thu, 16 Apr 2020 07:00:06 GMT  
		Size: 28.2 MB (28156920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20.1-slim` - linux; 386

```console
$ docker pull mono@sha256:f298a5136fcc732fb7f7c1b06514978d91489ec0402751f79366829250420a41
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.9 MB (81942425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4471b379bc228d2d7acf3bf17250d5dc21bc3475d42956005eef5b84e23100b8`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:42:13 GMT
ADD file:82f76d577eec142f824456d027e5f82f681c9f5a09aeef4f711cef4662dcaea4 in / 
# Thu, 23 Apr 2020 00:42:13 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:06:02 GMT
ENV MONO_VERSION=5.20.1.34
# Thu, 23 Apr 2020 01:06:12 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 01:06:47 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7cb0551c4675347b94a8c63d7ee1f99dea4ab34aa7f23602ca587b6894d0211b`  
		Last Modified: Thu, 23 Apr 2020 00:47:39 GMT  
		Size: 23.1 MB (23141423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f99a2ee486012fc5349a1f2fc838b03077a9aa47e79c414bc5af7e6be55d0ac`  
		Last Modified: Thu, 23 Apr 2020 01:15:02 GMT  
		Size: 244.5 KB (244504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3666eed20e513a6d57a046805936faf49f4e8af6f172fefa71261014ee05c479`  
		Last Modified: Thu, 23 Apr 2020 01:15:18 GMT  
		Size: 58.6 MB (58556498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20.1-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:8075f272b67d3b0230b83dec1f4ea321e0f9e68390fb4208b5cbfbde3e339a6c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47669710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b4f4a283b7df8fb74adb07675407330610860bf778c831f068775f705090dfd`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 01:43:57 GMT
ADD file:1c7f60f778e4b93490d570487d56275925e5eb477632e71cb9f035ce6edf2460 in / 
# Thu, 16 Apr 2020 01:44:03 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 06:44:48 GMT
ENV MONO_VERSION=5.20.1.34
# Thu, 16 Apr 2020 06:46:25 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Apr 2020 06:47:57 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:15e508b90ba1d327da83b72fc494ca263c1566ef6f70b91001cf2093395ffa3d`  
		Last Modified: Thu, 16 Apr 2020 02:04:33 GMT  
		Size: 22.8 MB (22785425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58f669c3fbfce943d77701b69e7857eb6d1b88bbf7f9167a449d80be23eb3243`  
		Last Modified: Thu, 16 Apr 2020 07:19:18 GMT  
		Size: 244.6 KB (244638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c16782e8edab25bcd823ec760e3d334f1009343a5a1ef80520730ea6acd56e3`  
		Last Modified: Thu, 16 Apr 2020 07:19:25 GMT  
		Size: 24.6 MB (24639647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:5.20-slim`

```console
$ docker pull mono@sha256:f54d8a6f6d24cb0f4a77dc81054eacdf2cddc792cb433fc1993b69c22748af3c
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
$ docker pull mono@sha256:6412a9e5863081fae60b17b4b60622acbd385f9f6187b2d6bdf7f3f657de1352
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.3 MB (78277604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ec8523ec89cdaca7f4e9500615ae1200ab87254843543f0e87bb510b0766e7c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 03:27:50 GMT
ADD file:40f52c233aecabf572a9db7450590d54d5e125fb00ecbb4a26fecd0b71e84eb8 in / 
# Thu, 16 Apr 2020 03:27:50 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 09:13:38 GMT
ENV MONO_VERSION=5.20.1.34
# Thu, 16 Apr 2020 09:13:48 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Apr 2020 09:14:25 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:5e35bd43cf7898d036f8515be74d45b2e3abd2a5534fc280de63a9c22dd175bd`  
		Last Modified: Thu, 16 Apr 2020 03:35:04 GMT  
		Size: 22.5 MB (22513476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27914964de9bbbd7f3daceed10bf3b1e9b4f60b8f305449c247e05ba453e9f90`  
		Last Modified: Thu, 16 Apr 2020 09:47:20 GMT  
		Size: 244.5 KB (244500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ffb2a3a9de8dfc06d17c1ba1b8f42ccae089474466f5d3efa1e21fbf8b5918e`  
		Last Modified: Thu, 16 Apr 2020 09:47:31 GMT  
		Size: 55.5 MB (55519628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:24277a451c25923284bd552e52a477c6d5f0550d5bc4bf36c6f011cdab833f5a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45700581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19ded18f1bc26bdd165c560e353704c774e72c61edf6306f0a301734b1cd592d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 00:54:51 GMT
ADD file:ba6c5e03457e69f59231e8e7c6465c1ec985812f0d8f7a65d9842f2be3e947fb in / 
# Thu, 16 Apr 2020 00:54:54 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 03:25:11 GMT
ENV MONO_VERSION=5.20.1.34
# Thu, 16 Apr 2020 03:25:36 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Apr 2020 03:26:21 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:b7d527e4baf13a6c926fb354fe1b38cb42b96f249ae65fdc0f52c853b654e06e`  
		Last Modified: Thu, 16 Apr 2020 01:02:32 GMT  
		Size: 21.2 MB (21190797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8340381d358ecc9e44596343db49a1d8fe9fc408313742adb549d7acbfa010d9`  
		Last Modified: Thu, 16 Apr 2020 03:36:49 GMT  
		Size: 244.5 KB (244533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89c829c702c9ea78e5f1e834e27d5270a1aeb340e0c387fd2bcca835a6508a18`  
		Last Modified: Thu, 16 Apr 2020 03:36:59 GMT  
		Size: 24.3 MB (24265251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:82879b2317895d2b306e14bd38f26be346070655d8441662bd05aa9f85797783
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.1 MB (43105202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab6576fb1edf563a52cf0994636f3e1619b6508c783b4906ed59494f06d03533`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 01:05:08 GMT
ADD file:e37c4728c0c89ac126542ac35e7e493425c021bfac751079c9b266821a1b4e99 in / 
# Thu, 16 Apr 2020 01:05:10 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 04:43:14 GMT
ENV MONO_VERSION=5.20.1.34
# Thu, 16 Apr 2020 04:43:33 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Apr 2020 04:44:18 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:f78d9963dfddc4747d6200353b50f6093a6e37ca82e1612fa397d64ff13e7299`  
		Last Modified: Thu, 16 Apr 2020 01:12:33 GMT  
		Size: 19.3 MB (19298546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caf684cdea8a2272c82e09cbbb5024552c6e67b7dcf59ea62af547f9c730474e`  
		Last Modified: Thu, 16 Apr 2020 04:54:37 GMT  
		Size: 244.6 KB (244560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:249d36139d8bc596df209162b7386211edf003733b4286aa7405033282389c33`  
		Last Modified: Thu, 16 Apr 2020 04:54:47 GMT  
		Size: 23.6 MB (23562096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:373e3d9ccf313cac211d9ede8eec8a2ccb1d1c0303fc5312fddfccc026277c41
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48771410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43f116c952bab72566e217b3d9571b9572c6e2ac731995c266825ca5ff059e14`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 02:45:19 GMT
ADD file:1588320d1c43714ec0353b7471f2ffd649045ca0f5f70dcb1eb064875fff9578 in / 
# Thu, 16 Apr 2020 02:45:21 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 06:49:41 GMT
ENV MONO_VERSION=5.20.1.34
# Thu, 16 Apr 2020 06:50:01 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Apr 2020 06:50:40 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:8978c87ff45d64d1663a585dcf1ed66d9e711c2e4048d83ef561da9514ef46e6`  
		Last Modified: Thu, 16 Apr 2020 02:51:32 GMT  
		Size: 20.4 MB (20370106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:554199a06aed010aa14e2e6ed810ac12e3f7ea1f01b4b484029b46c769a914b5`  
		Last Modified: Thu, 16 Apr 2020 07:00:00 GMT  
		Size: 244.4 KB (244384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2f9c219c23779432f95dca105f2822e4e5cce0035ec90439890cb4ba1c4b3e0`  
		Last Modified: Thu, 16 Apr 2020 07:00:06 GMT  
		Size: 28.2 MB (28156920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20-slim` - linux; 386

```console
$ docker pull mono@sha256:f298a5136fcc732fb7f7c1b06514978d91489ec0402751f79366829250420a41
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.9 MB (81942425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4471b379bc228d2d7acf3bf17250d5dc21bc3475d42956005eef5b84e23100b8`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:42:13 GMT
ADD file:82f76d577eec142f824456d027e5f82f681c9f5a09aeef4f711cef4662dcaea4 in / 
# Thu, 23 Apr 2020 00:42:13 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:06:02 GMT
ENV MONO_VERSION=5.20.1.34
# Thu, 23 Apr 2020 01:06:12 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 01:06:47 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7cb0551c4675347b94a8c63d7ee1f99dea4ab34aa7f23602ca587b6894d0211b`  
		Last Modified: Thu, 23 Apr 2020 00:47:39 GMT  
		Size: 23.1 MB (23141423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f99a2ee486012fc5349a1f2fc838b03077a9aa47e79c414bc5af7e6be55d0ac`  
		Last Modified: Thu, 23 Apr 2020 01:15:02 GMT  
		Size: 244.5 KB (244504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3666eed20e513a6d57a046805936faf49f4e8af6f172fefa71261014ee05c479`  
		Last Modified: Thu, 23 Apr 2020 01:15:18 GMT  
		Size: 58.6 MB (58556498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:8075f272b67d3b0230b83dec1f4ea321e0f9e68390fb4208b5cbfbde3e339a6c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47669710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b4f4a283b7df8fb74adb07675407330610860bf778c831f068775f705090dfd`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 01:43:57 GMT
ADD file:1c7f60f778e4b93490d570487d56275925e5eb477632e71cb9f035ce6edf2460 in / 
# Thu, 16 Apr 2020 01:44:03 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 06:44:48 GMT
ENV MONO_VERSION=5.20.1.34
# Thu, 16 Apr 2020 06:46:25 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Apr 2020 06:47:57 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:15e508b90ba1d327da83b72fc494ca263c1566ef6f70b91001cf2093395ffa3d`  
		Last Modified: Thu, 16 Apr 2020 02:04:33 GMT  
		Size: 22.8 MB (22785425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58f669c3fbfce943d77701b69e7857eb6d1b88bbf7f9167a449d80be23eb3243`  
		Last Modified: Thu, 16 Apr 2020 07:19:18 GMT  
		Size: 244.6 KB (244638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c16782e8edab25bcd823ec760e3d334f1009343a5a1ef80520730ea6acd56e3`  
		Last Modified: Thu, 16 Apr 2020 07:19:25 GMT  
		Size: 24.6 MB (24639647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:5-slim`

```console
$ docker pull mono@sha256:f54d8a6f6d24cb0f4a77dc81054eacdf2cddc792cb433fc1993b69c22748af3c
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
$ docker pull mono@sha256:6412a9e5863081fae60b17b4b60622acbd385f9f6187b2d6bdf7f3f657de1352
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.3 MB (78277604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ec8523ec89cdaca7f4e9500615ae1200ab87254843543f0e87bb510b0766e7c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 03:27:50 GMT
ADD file:40f52c233aecabf572a9db7450590d54d5e125fb00ecbb4a26fecd0b71e84eb8 in / 
# Thu, 16 Apr 2020 03:27:50 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 09:13:38 GMT
ENV MONO_VERSION=5.20.1.34
# Thu, 16 Apr 2020 09:13:48 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Apr 2020 09:14:25 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:5e35bd43cf7898d036f8515be74d45b2e3abd2a5534fc280de63a9c22dd175bd`  
		Last Modified: Thu, 16 Apr 2020 03:35:04 GMT  
		Size: 22.5 MB (22513476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27914964de9bbbd7f3daceed10bf3b1e9b4f60b8f305449c247e05ba453e9f90`  
		Last Modified: Thu, 16 Apr 2020 09:47:20 GMT  
		Size: 244.5 KB (244500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ffb2a3a9de8dfc06d17c1ba1b8f42ccae089474466f5d3efa1e21fbf8b5918e`  
		Last Modified: Thu, 16 Apr 2020 09:47:31 GMT  
		Size: 55.5 MB (55519628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:24277a451c25923284bd552e52a477c6d5f0550d5bc4bf36c6f011cdab833f5a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45700581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19ded18f1bc26bdd165c560e353704c774e72c61edf6306f0a301734b1cd592d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 00:54:51 GMT
ADD file:ba6c5e03457e69f59231e8e7c6465c1ec985812f0d8f7a65d9842f2be3e947fb in / 
# Thu, 16 Apr 2020 00:54:54 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 03:25:11 GMT
ENV MONO_VERSION=5.20.1.34
# Thu, 16 Apr 2020 03:25:36 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Apr 2020 03:26:21 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:b7d527e4baf13a6c926fb354fe1b38cb42b96f249ae65fdc0f52c853b654e06e`  
		Last Modified: Thu, 16 Apr 2020 01:02:32 GMT  
		Size: 21.2 MB (21190797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8340381d358ecc9e44596343db49a1d8fe9fc408313742adb549d7acbfa010d9`  
		Last Modified: Thu, 16 Apr 2020 03:36:49 GMT  
		Size: 244.5 KB (244533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89c829c702c9ea78e5f1e834e27d5270a1aeb340e0c387fd2bcca835a6508a18`  
		Last Modified: Thu, 16 Apr 2020 03:36:59 GMT  
		Size: 24.3 MB (24265251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:82879b2317895d2b306e14bd38f26be346070655d8441662bd05aa9f85797783
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.1 MB (43105202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab6576fb1edf563a52cf0994636f3e1619b6508c783b4906ed59494f06d03533`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 01:05:08 GMT
ADD file:e37c4728c0c89ac126542ac35e7e493425c021bfac751079c9b266821a1b4e99 in / 
# Thu, 16 Apr 2020 01:05:10 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 04:43:14 GMT
ENV MONO_VERSION=5.20.1.34
# Thu, 16 Apr 2020 04:43:33 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Apr 2020 04:44:18 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:f78d9963dfddc4747d6200353b50f6093a6e37ca82e1612fa397d64ff13e7299`  
		Last Modified: Thu, 16 Apr 2020 01:12:33 GMT  
		Size: 19.3 MB (19298546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caf684cdea8a2272c82e09cbbb5024552c6e67b7dcf59ea62af547f9c730474e`  
		Last Modified: Thu, 16 Apr 2020 04:54:37 GMT  
		Size: 244.6 KB (244560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:249d36139d8bc596df209162b7386211edf003733b4286aa7405033282389c33`  
		Last Modified: Thu, 16 Apr 2020 04:54:47 GMT  
		Size: 23.6 MB (23562096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:373e3d9ccf313cac211d9ede8eec8a2ccb1d1c0303fc5312fddfccc026277c41
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48771410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43f116c952bab72566e217b3d9571b9572c6e2ac731995c266825ca5ff059e14`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 02:45:19 GMT
ADD file:1588320d1c43714ec0353b7471f2ffd649045ca0f5f70dcb1eb064875fff9578 in / 
# Thu, 16 Apr 2020 02:45:21 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 06:49:41 GMT
ENV MONO_VERSION=5.20.1.34
# Thu, 16 Apr 2020 06:50:01 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Apr 2020 06:50:40 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:8978c87ff45d64d1663a585dcf1ed66d9e711c2e4048d83ef561da9514ef46e6`  
		Last Modified: Thu, 16 Apr 2020 02:51:32 GMT  
		Size: 20.4 MB (20370106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:554199a06aed010aa14e2e6ed810ac12e3f7ea1f01b4b484029b46c769a914b5`  
		Last Modified: Thu, 16 Apr 2020 07:00:00 GMT  
		Size: 244.4 KB (244384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2f9c219c23779432f95dca105f2822e4e5cce0035ec90439890cb4ba1c4b3e0`  
		Last Modified: Thu, 16 Apr 2020 07:00:06 GMT  
		Size: 28.2 MB (28156920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5-slim` - linux; 386

```console
$ docker pull mono@sha256:f298a5136fcc732fb7f7c1b06514978d91489ec0402751f79366829250420a41
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.9 MB (81942425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4471b379bc228d2d7acf3bf17250d5dc21bc3475d42956005eef5b84e23100b8`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:42:13 GMT
ADD file:82f76d577eec142f824456d027e5f82f681c9f5a09aeef4f711cef4662dcaea4 in / 
# Thu, 23 Apr 2020 00:42:13 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:06:02 GMT
ENV MONO_VERSION=5.20.1.34
# Thu, 23 Apr 2020 01:06:12 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 01:06:47 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7cb0551c4675347b94a8c63d7ee1f99dea4ab34aa7f23602ca587b6894d0211b`  
		Last Modified: Thu, 23 Apr 2020 00:47:39 GMT  
		Size: 23.1 MB (23141423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f99a2ee486012fc5349a1f2fc838b03077a9aa47e79c414bc5af7e6be55d0ac`  
		Last Modified: Thu, 23 Apr 2020 01:15:02 GMT  
		Size: 244.5 KB (244504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3666eed20e513a6d57a046805936faf49f4e8af6f172fefa71261014ee05c479`  
		Last Modified: Thu, 23 Apr 2020 01:15:18 GMT  
		Size: 58.6 MB (58556498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:8075f272b67d3b0230b83dec1f4ea321e0f9e68390fb4208b5cbfbde3e339a6c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47669710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b4f4a283b7df8fb74adb07675407330610860bf778c831f068775f705090dfd`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 01:43:57 GMT
ADD file:1c7f60f778e4b93490d570487d56275925e5eb477632e71cb9f035ce6edf2460 in / 
# Thu, 16 Apr 2020 01:44:03 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 06:44:48 GMT
ENV MONO_VERSION=5.20.1.34
# Thu, 16 Apr 2020 06:46:25 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Apr 2020 06:47:57 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:15e508b90ba1d327da83b72fc494ca263c1566ef6f70b91001cf2093395ffa3d`  
		Last Modified: Thu, 16 Apr 2020 02:04:33 GMT  
		Size: 22.8 MB (22785425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58f669c3fbfce943d77701b69e7857eb6d1b88bbf7f9167a449d80be23eb3243`  
		Last Modified: Thu, 16 Apr 2020 07:19:18 GMT  
		Size: 244.6 KB (244638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c16782e8edab25bcd823ec760e3d334f1009343a5a1ef80520730ea6acd56e3`  
		Last Modified: Thu, 16 Apr 2020 07:19:25 GMT  
		Size: 24.6 MB (24639647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6`

```console
$ docker pull mono@sha256:8b4551b8332e7efec0aa7c0fed4f53a7cf6bed12cbee05f6858ffb65a79aa5cd
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
$ docker pull mono@sha256:3d109ece622c61e26832ecee8eafdafa2e72535b9c74d735d879ca179b1a13b8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.1 MB (235135830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51f7ccdd96f0dfed7dc0f8f3af746f9edb7e71a7f93e19af1ea4b9bccb53d336`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 03:27:50 GMT
ADD file:40f52c233aecabf572a9db7450590d54d5e125fb00ecbb4a26fecd0b71e84eb8 in / 
# Thu, 16 Apr 2020 03:27:50 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 09:11:48 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 16 Apr 2020 09:12:00 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Apr 2020 09:12:35 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 16 Apr 2020 09:25:34 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:5e35bd43cf7898d036f8515be74d45b2e3abd2a5534fc280de63a9c22dd175bd`  
		Last Modified: Thu, 16 Apr 2020 03:35:04 GMT  
		Size: 22.5 MB (22513476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79f990050ea7755c8b4310123b2d720a7fede3eaa9cf5a76acb2a5fbd0af58d5`  
		Last Modified: Thu, 16 Apr 2020 09:46:33 GMT  
		Size: 244.5 KB (244519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b463238d61e87361acee422c7ed4ee873ebc66a2a7b4dde702ca6956a532ecf`  
		Last Modified: Thu, 16 Apr 2020 09:46:52 GMT  
		Size: 64.6 MB (64584108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04da7d857cd9fd3a2c4f7e602c9a50f2993fd66e67372efe5765e3b227eb1e73`  
		Last Modified: Thu, 16 Apr 2020 09:48:16 GMT  
		Size: 147.8 MB (147793727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6` - linux; arm variant v5

```console
$ docker pull mono@sha256:039a6be7bba94963928fb63f0cd7624bdcc24ff437d3511659983bf8a15da61c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.7 MB (176695282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbb0da5905f2877688de5793cf7d5f0c6b5cdbb737868e678439fec995215cfa`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 00:54:51 GMT
ADD file:ba6c5e03457e69f59231e8e7c6465c1ec985812f0d8f7a65d9842f2be3e947fb in / 
# Thu, 16 Apr 2020 00:54:54 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 03:22:05 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 16 Apr 2020 03:22:36 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Apr 2020 03:23:29 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 16 Apr 2020 03:29:10 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:b7d527e4baf13a6c926fb354fe1b38cb42b96f249ae65fdc0f52c853b654e06e`  
		Last Modified: Thu, 16 Apr 2020 01:02:32 GMT  
		Size: 21.2 MB (21190797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5251e801555d8cd1370a8d39ca953a0fb8f39729ff494b4a60bd03b4255c45be`  
		Last Modified: Thu, 16 Apr 2020 03:36:12 GMT  
		Size: 244.6 KB (244555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7c9b96b75ebb7a3cac23cf75e27179b71b5aa2cee0c40c33aca6399e29516f2`  
		Last Modified: Thu, 16 Apr 2020 03:36:22 GMT  
		Size: 25.4 MB (25367763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c33b43ad8da6addb8c852a68a9848cba5f48be98873fc8db208731eb55f31b9b`  
		Last Modified: Thu, 16 Apr 2020 03:37:53 GMT  
		Size: 129.9 MB (129892167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6` - linux; arm variant v7

```console
$ docker pull mono@sha256:09076495aacfba71beb6f4e5812d597a2d059b58d0d1a053068e4fa0fdec8443
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.7 MB (172708239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6e489c47305d9f8c107b00d2a1e335c874014e8fa4a3fc5ecb9082df7c5be0f`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 01:05:08 GMT
ADD file:e37c4728c0c89ac126542ac35e7e493425c021bfac751079c9b266821a1b4e99 in / 
# Thu, 16 Apr 2020 01:05:10 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 04:40:35 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 16 Apr 2020 04:40:56 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Apr 2020 04:41:45 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 16 Apr 2020 04:47:13 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:f78d9963dfddc4747d6200353b50f6093a6e37ca82e1612fa397d64ff13e7299`  
		Last Modified: Thu, 16 Apr 2020 01:12:33 GMT  
		Size: 19.3 MB (19298546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70114347da279136ebd21697ef769dc5764f716c6f7331568bbf7306c17da63c`  
		Last Modified: Thu, 16 Apr 2020 04:54:02 GMT  
		Size: 244.6 KB (244551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:802f26edffea7b59f9cc74e47561799e0c847d999b0db0dd2d99497c42af3511`  
		Last Modified: Thu, 16 Apr 2020 04:54:10 GMT  
		Size: 24.6 MB (24608740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62a9fd3d7648204f077b0034260c1887fe3c12c26ffadbb4223d8dc7ff65c1eb`  
		Last Modified: Thu, 16 Apr 2020 04:55:42 GMT  
		Size: 128.6 MB (128556402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:abe9ae9da3ff9d1c710471ec6a5c1b39b18e33e11b0abba7d4245a3e75b11dc0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.7 MB (194747450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5a96031ff7018d8a3f1e18642728c41f24ad314d26c4fc40907ef19fce71fcd`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 02:45:19 GMT
ADD file:1588320d1c43714ec0353b7471f2ffd649045ca0f5f70dcb1eb064875fff9578 in / 
# Thu, 16 Apr 2020 02:45:21 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 06:47:03 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 16 Apr 2020 06:47:21 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Apr 2020 06:48:05 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 16 Apr 2020 06:53:15 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:8978c87ff45d64d1663a585dcf1ed66d9e711c2e4048d83ef561da9514ef46e6`  
		Last Modified: Thu, 16 Apr 2020 02:51:32 GMT  
		Size: 20.4 MB (20370106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:090b996e11040b9a724d4b94b5f6fea43f5cee5558fdcdcb2e4627d1c596f82c`  
		Last Modified: Thu, 16 Apr 2020 06:59:20 GMT  
		Size: 244.4 KB (244369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be77ae0e8a98b883233d159b79364894a76d49f1b02badb9f57b227a26a8e1a`  
		Last Modified: Thu, 16 Apr 2020 06:59:30 GMT  
		Size: 29.4 MB (29420188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1774c3e17e0d83d02e086998900775da6efe1356459c585e7d5800434b5aaf21`  
		Last Modified: Thu, 16 Apr 2020 07:01:03 GMT  
		Size: 144.7 MB (144712787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6` - linux; 386

```console
$ docker pull mono@sha256:9c689075bb69bade3f528bb36bfe204fd3529387d13addcfe9d2c43db444d7a4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.5 MB (243509400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1505bc590d4dce8f057579c70b93a89b4ce6d044fd5f80a06eb1765872b2e2b1`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:42:13 GMT
ADD file:82f76d577eec142f824456d027e5f82f681c9f5a09aeef4f711cef4662dcaea4 in / 
# Thu, 23 Apr 2020 00:42:13 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:04:12 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 23 Apr 2020 01:04:23 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 01:05:02 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Apr 2020 01:09:10 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7cb0551c4675347b94a8c63d7ee1f99dea4ab34aa7f23602ca587b6894d0211b`  
		Last Modified: Thu, 23 Apr 2020 00:47:39 GMT  
		Size: 23.1 MB (23141423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa3b9d440d2c40f2a9f3756fc7f8347bb9ec214b84fa396a388bd94782e1a678`  
		Last Modified: Thu, 23 Apr 2020 01:14:10 GMT  
		Size: 244.5 KB (244496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de2b74896e741d2269bb5084cfdbe6af6d2fc8d9d0ed1fc3f055d7c644afad5d`  
		Last Modified: Thu, 23 Apr 2020 01:14:29 GMT  
		Size: 68.6 MB (68630969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:753f8d38ff41ce32cf902046d0c45ed81a3a5475418bddade545b50a630ae181`  
		Last Modified: Thu, 23 Apr 2020 01:16:08 GMT  
		Size: 151.5 MB (151492512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6` - linux; ppc64le

```console
$ docker pull mono@sha256:0434d01a8617e75170a4dd8a638d786d1e67ac13c9fc880e023ccd0950428e36
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.0 MB (178997743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b5e14702ff1aff3bacfb8485b742086b08ff9d01cadd82d9f8327e6ac887fcc`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 01:43:57 GMT
ADD file:1c7f60f778e4b93490d570487d56275925e5eb477632e71cb9f035ce6edf2460 in / 
# Thu, 16 Apr 2020 01:44:03 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 06:37:42 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 16 Apr 2020 06:39:43 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Apr 2020 06:41:27 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 16 Apr 2020 06:58:08 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:15e508b90ba1d327da83b72fc494ca263c1566ef6f70b91001cf2093395ffa3d`  
		Last Modified: Thu, 16 Apr 2020 02:04:33 GMT  
		Size: 22.8 MB (22785425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1629fdf02d54d31ae3023cd8b4a515c3c17a085c6135c7a10e412896d06a1f62`  
		Last Modified: Thu, 16 Apr 2020 07:18:38 GMT  
		Size: 244.7 KB (244669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fc63fa4246f2b9b66f762d8c33434e375c088c1ca73c3a389a8fb2525f93c7c`  
		Last Modified: Thu, 16 Apr 2020 07:18:43 GMT  
		Size: 25.8 MB (25775805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90ed038a48cf0007c67072a64fc2d4d1d4efd20b275bff6a15884fcfe67b0afa`  
		Last Modified: Thu, 16 Apr 2020 07:20:07 GMT  
		Size: 130.2 MB (130191844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.6`

```console
$ docker pull mono@sha256:a7fb3160feb8b4f8cfd50f8f8db1224876a71b615669b94b04740b9979853a2b
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
$ docker pull mono@sha256:0b433fb0621e18ac0684b0856a02e22fe9e60c4825c893dc33224e2285537c10
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (233037618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7db13482ea72da7effe51ad083a644e0c8bb62c71eb2b3437327862b017c603`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 03:27:50 GMT
ADD file:40f52c233aecabf572a9db7450590d54d5e125fb00ecbb4a26fecd0b71e84eb8 in / 
# Thu, 16 Apr 2020 03:27:50 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 09:12:43 GMT
ENV MONO_VERSION=6.6.0.161
# Thu, 16 Apr 2020 09:12:53 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Apr 2020 09:13:30 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 16 Apr 2020 09:36:35 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:5e35bd43cf7898d036f8515be74d45b2e3abd2a5534fc280de63a9c22dd175bd`  
		Last Modified: Thu, 16 Apr 2020 03:35:04 GMT  
		Size: 22.5 MB (22513476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f76aee1152e1c17c5c2fde70a7bebdd5d5c8a9895316482efbb1bf3cab92edb5`  
		Last Modified: Thu, 16 Apr 2020 09:46:59 GMT  
		Size: 244.5 KB (244511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b21609b816b63406b186989f8e6ea95d37bb9e8f9fc6a39377d450d2888dd633`  
		Last Modified: Thu, 16 Apr 2020 09:47:15 GMT  
		Size: 63.0 MB (62972017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39364a66c8bcea35cb1bbc438ec3b34aa23c52b5bd6b5d1781c8ad74843041dc`  
		Last Modified: Thu, 16 Apr 2020 09:49:06 GMT  
		Size: 147.3 MB (147307614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6` - linux; arm variant v5

```console
$ docker pull mono@sha256:953b98f308c725c908039c6b0119c4308afde0a43bee73a9212123c246e3ba14
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.5 MB (176499196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30ab99fcbe0706e2c5cbf3b3f402c4f222fa6a4deec87d1658ac0883e0de7c94`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 00:54:51 GMT
ADD file:ba6c5e03457e69f59231e8e7c6465c1ec985812f0d8f7a65d9842f2be3e947fb in / 
# Thu, 16 Apr 2020 00:54:54 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 03:23:39 GMT
ENV MONO_VERSION=6.6.0.161
# Thu, 16 Apr 2020 03:24:08 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Apr 2020 03:25:01 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 16 Apr 2020 03:32:10 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:b7d527e4baf13a6c926fb354fe1b38cb42b96f249ae65fdc0f52c853b654e06e`  
		Last Modified: Thu, 16 Apr 2020 01:02:32 GMT  
		Size: 21.2 MB (21190797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2182e7eff26a84a3839979b8dc30f86f313c10d5a9c5cb556911ea13a0a09b7`  
		Last Modified: Thu, 16 Apr 2020 03:36:31 GMT  
		Size: 244.6 KB (244558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65ecd30f76c6d61fc0338f94136d06ae87f496afd7cccaea0a67ef39cc037534`  
		Last Modified: Thu, 16 Apr 2020 03:36:42 GMT  
		Size: 25.4 MB (25414654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71bbeb6d8b71001853c4ac6381a1e2da4bed657325144da5a05f53de8571155b`  
		Last Modified: Thu, 16 Apr 2020 03:38:48 GMT  
		Size: 129.6 MB (129649187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6` - linux; arm variant v7

```console
$ docker pull mono@sha256:dfff052f102fe7d4378e5d2b0245680892904cbd70cb13786faf09e0ac56dfb3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.5 MB (172506927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b22ad409e9a2275f54ce587900650610baa7b303fd2f52317ef1049368fce42`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 01:05:08 GMT
ADD file:e37c4728c0c89ac126542ac35e7e493425c021bfac751079c9b266821a1b4e99 in / 
# Thu, 16 Apr 2020 01:05:10 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 04:41:55 GMT
ENV MONO_VERSION=6.6.0.161
# Thu, 16 Apr 2020 04:42:15 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Apr 2020 04:43:04 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 16 Apr 2020 04:50:27 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:f78d9963dfddc4747d6200353b50f6093a6e37ca82e1612fa397d64ff13e7299`  
		Last Modified: Thu, 16 Apr 2020 01:12:33 GMT  
		Size: 19.3 MB (19298546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7c709444af1581614022f19533f2bd4e0a3468d7051453df34e50bf99df9321`  
		Last Modified: Thu, 16 Apr 2020 04:54:19 GMT  
		Size: 244.5 KB (244546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a96b6dd89ea6225de279fd91629a436f6398c0547a59d1d7935d302802dec507`  
		Last Modified: Thu, 16 Apr 2020 04:54:29 GMT  
		Size: 24.6 MB (24648627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ff75ba1385b277ecc3e4c7e6201fd3706aa69b722a429fefcc75f0c5beb09b7`  
		Last Modified: Thu, 16 Apr 2020 04:56:40 GMT  
		Size: 128.3 MB (128315208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:d50f772e76b54a7da4d565208fcabf191b1246e0ad0853a269e282f7824d2623
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.4 MB (194394691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daed0db4cc3b4df6b71cd4424bfe0f98d8c6bffb99925929d809841240cd7d31`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 02:45:19 GMT
ADD file:1588320d1c43714ec0353b7471f2ffd649045ca0f5f70dcb1eb064875fff9578 in / 
# Thu, 16 Apr 2020 02:45:21 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 06:48:23 GMT
ENV MONO_VERSION=6.6.0.161
# Thu, 16 Apr 2020 06:48:40 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Apr 2020 06:49:27 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 16 Apr 2020 06:56:13 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:8978c87ff45d64d1663a585dcf1ed66d9e711c2e4048d83ef561da9514ef46e6`  
		Last Modified: Thu, 16 Apr 2020 02:51:32 GMT  
		Size: 20.4 MB (20370106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f4cefd4f77cad9e57aea080af9eb57c1991ab847ef1ab0a04c72c47d4d11332`  
		Last Modified: Thu, 16 Apr 2020 06:59:39 GMT  
		Size: 244.4 KB (244371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16a24563d28e05e4d85e2e968cf5a1be1fd764682e892a24a0323b2c2daee23a`  
		Last Modified: Thu, 16 Apr 2020 06:59:49 GMT  
		Size: 29.4 MB (29438693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e5fd0d429b209d5930a2be3ed4225f606136251ea4a38b4a31f015eb3c3b25a`  
		Last Modified: Thu, 16 Apr 2020 07:02:02 GMT  
		Size: 144.3 MB (144341521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6` - linux; 386

```console
$ docker pull mono@sha256:94e58f1ce29ecb43527eb823856f0434fa0d3a0812ecc31df88f0e9d2e1c3eb2
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.3 MB (241294092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce5575a49e77c965605a2abaa50aa38f2aa1668e66c41a766b116df708ca2d2f`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:42:13 GMT
ADD file:82f76d577eec142f824456d027e5f82f681c9f5a09aeef4f711cef4662dcaea4 in / 
# Thu, 23 Apr 2020 00:42:13 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:05:07 GMT
ENV MONO_VERSION=6.6.0.161
# Thu, 23 Apr 2020 01:05:17 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 01:05:53 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Apr 2020 01:11:47 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7cb0551c4675347b94a8c63d7ee1f99dea4ab34aa7f23602ca587b6894d0211b`  
		Last Modified: Thu, 23 Apr 2020 00:47:39 GMT  
		Size: 23.1 MB (23141423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2beb89e4f0bd2e26a4512b29f2528cda17c529914331e656630af13f14143f8`  
		Last Modified: Thu, 23 Apr 2020 01:14:38 GMT  
		Size: 244.5 KB (244501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c70df528f46cab25e9c07e896d643cac9c7968e0e534e9d4702c3645865f689b`  
		Last Modified: Thu, 23 Apr 2020 01:14:55 GMT  
		Size: 66.7 MB (66747446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb378b781be2a120cd2fa519211a18f9a67e6bd23b8442b3ae140570f8371226`  
		Last Modified: Thu, 23 Apr 2020 01:16:57 GMT  
		Size: 151.2 MB (151160722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6` - linux; ppc64le

```console
$ docker pull mono@sha256:4235fd48012578b4b57f350c979ce60090348f15633d786dc80f4411f4c99add
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.8 MB (178801331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0e1d4c00d6874adca289180ab7f6005e5ac7d7624540b0086d8e64f470f7981`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 01:43:57 GMT
ADD file:1c7f60f778e4b93490d570487d56275925e5eb477632e71cb9f035ce6edf2460 in / 
# Thu, 16 Apr 2020 01:44:03 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 06:41:39 GMT
ENV MONO_VERSION=6.6.0.161
# Thu, 16 Apr 2020 06:42:53 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Apr 2020 06:44:39 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 16 Apr 2020 07:10:39 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:15e508b90ba1d327da83b72fc494ca263c1566ef6f70b91001cf2093395ffa3d`  
		Last Modified: Thu, 16 Apr 2020 02:04:33 GMT  
		Size: 22.8 MB (22785425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:800a5760720ebbe560ce8ace6be98139c4a1b70fe59bfc7d95e64b47f5b3d969`  
		Last Modified: Thu, 16 Apr 2020 07:19:01 GMT  
		Size: 244.6 KB (244581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3f899767b86a83eb94a1fb10e4abe4060361f3991cd7998c06677ee9f1875d4`  
		Last Modified: Thu, 16 Apr 2020 07:19:06 GMT  
		Size: 25.8 MB (25828268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05e9c715d026067720e1b2fda245dc97d172d2aeb0bd6be2d86bd4cc8807af4c`  
		Last Modified: Thu, 16 Apr 2020 07:20:54 GMT  
		Size: 129.9 MB (129943057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.6.0`

```console
$ docker pull mono@sha256:a7fb3160feb8b4f8cfd50f8f8db1224876a71b615669b94b04740b9979853a2b
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
$ docker pull mono@sha256:0b433fb0621e18ac0684b0856a02e22fe9e60c4825c893dc33224e2285537c10
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (233037618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7db13482ea72da7effe51ad083a644e0c8bb62c71eb2b3437327862b017c603`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 03:27:50 GMT
ADD file:40f52c233aecabf572a9db7450590d54d5e125fb00ecbb4a26fecd0b71e84eb8 in / 
# Thu, 16 Apr 2020 03:27:50 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 09:12:43 GMT
ENV MONO_VERSION=6.6.0.161
# Thu, 16 Apr 2020 09:12:53 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Apr 2020 09:13:30 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 16 Apr 2020 09:36:35 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:5e35bd43cf7898d036f8515be74d45b2e3abd2a5534fc280de63a9c22dd175bd`  
		Last Modified: Thu, 16 Apr 2020 03:35:04 GMT  
		Size: 22.5 MB (22513476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f76aee1152e1c17c5c2fde70a7bebdd5d5c8a9895316482efbb1bf3cab92edb5`  
		Last Modified: Thu, 16 Apr 2020 09:46:59 GMT  
		Size: 244.5 KB (244511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b21609b816b63406b186989f8e6ea95d37bb9e8f9fc6a39377d450d2888dd633`  
		Last Modified: Thu, 16 Apr 2020 09:47:15 GMT  
		Size: 63.0 MB (62972017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39364a66c8bcea35cb1bbc438ec3b34aa23c52b5bd6b5d1781c8ad74843041dc`  
		Last Modified: Thu, 16 Apr 2020 09:49:06 GMT  
		Size: 147.3 MB (147307614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6.0` - linux; arm variant v5

```console
$ docker pull mono@sha256:953b98f308c725c908039c6b0119c4308afde0a43bee73a9212123c246e3ba14
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.5 MB (176499196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30ab99fcbe0706e2c5cbf3b3f402c4f222fa6a4deec87d1658ac0883e0de7c94`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 00:54:51 GMT
ADD file:ba6c5e03457e69f59231e8e7c6465c1ec985812f0d8f7a65d9842f2be3e947fb in / 
# Thu, 16 Apr 2020 00:54:54 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 03:23:39 GMT
ENV MONO_VERSION=6.6.0.161
# Thu, 16 Apr 2020 03:24:08 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Apr 2020 03:25:01 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 16 Apr 2020 03:32:10 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:b7d527e4baf13a6c926fb354fe1b38cb42b96f249ae65fdc0f52c853b654e06e`  
		Last Modified: Thu, 16 Apr 2020 01:02:32 GMT  
		Size: 21.2 MB (21190797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2182e7eff26a84a3839979b8dc30f86f313c10d5a9c5cb556911ea13a0a09b7`  
		Last Modified: Thu, 16 Apr 2020 03:36:31 GMT  
		Size: 244.6 KB (244558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65ecd30f76c6d61fc0338f94136d06ae87f496afd7cccaea0a67ef39cc037534`  
		Last Modified: Thu, 16 Apr 2020 03:36:42 GMT  
		Size: 25.4 MB (25414654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71bbeb6d8b71001853c4ac6381a1e2da4bed657325144da5a05f53de8571155b`  
		Last Modified: Thu, 16 Apr 2020 03:38:48 GMT  
		Size: 129.6 MB (129649187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6.0` - linux; arm variant v7

```console
$ docker pull mono@sha256:dfff052f102fe7d4378e5d2b0245680892904cbd70cb13786faf09e0ac56dfb3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.5 MB (172506927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b22ad409e9a2275f54ce587900650610baa7b303fd2f52317ef1049368fce42`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 01:05:08 GMT
ADD file:e37c4728c0c89ac126542ac35e7e493425c021bfac751079c9b266821a1b4e99 in / 
# Thu, 16 Apr 2020 01:05:10 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 04:41:55 GMT
ENV MONO_VERSION=6.6.0.161
# Thu, 16 Apr 2020 04:42:15 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Apr 2020 04:43:04 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 16 Apr 2020 04:50:27 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:f78d9963dfddc4747d6200353b50f6093a6e37ca82e1612fa397d64ff13e7299`  
		Last Modified: Thu, 16 Apr 2020 01:12:33 GMT  
		Size: 19.3 MB (19298546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7c709444af1581614022f19533f2bd4e0a3468d7051453df34e50bf99df9321`  
		Last Modified: Thu, 16 Apr 2020 04:54:19 GMT  
		Size: 244.5 KB (244546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a96b6dd89ea6225de279fd91629a436f6398c0547a59d1d7935d302802dec507`  
		Last Modified: Thu, 16 Apr 2020 04:54:29 GMT  
		Size: 24.6 MB (24648627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ff75ba1385b277ecc3e4c7e6201fd3706aa69b722a429fefcc75f0c5beb09b7`  
		Last Modified: Thu, 16 Apr 2020 04:56:40 GMT  
		Size: 128.3 MB (128315208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6.0` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:d50f772e76b54a7da4d565208fcabf191b1246e0ad0853a269e282f7824d2623
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.4 MB (194394691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daed0db4cc3b4df6b71cd4424bfe0f98d8c6bffb99925929d809841240cd7d31`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 02:45:19 GMT
ADD file:1588320d1c43714ec0353b7471f2ffd649045ca0f5f70dcb1eb064875fff9578 in / 
# Thu, 16 Apr 2020 02:45:21 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 06:48:23 GMT
ENV MONO_VERSION=6.6.0.161
# Thu, 16 Apr 2020 06:48:40 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Apr 2020 06:49:27 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 16 Apr 2020 06:56:13 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:8978c87ff45d64d1663a585dcf1ed66d9e711c2e4048d83ef561da9514ef46e6`  
		Last Modified: Thu, 16 Apr 2020 02:51:32 GMT  
		Size: 20.4 MB (20370106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f4cefd4f77cad9e57aea080af9eb57c1991ab847ef1ab0a04c72c47d4d11332`  
		Last Modified: Thu, 16 Apr 2020 06:59:39 GMT  
		Size: 244.4 KB (244371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16a24563d28e05e4d85e2e968cf5a1be1fd764682e892a24a0323b2c2daee23a`  
		Last Modified: Thu, 16 Apr 2020 06:59:49 GMT  
		Size: 29.4 MB (29438693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e5fd0d429b209d5930a2be3ed4225f606136251ea4a38b4a31f015eb3c3b25a`  
		Last Modified: Thu, 16 Apr 2020 07:02:02 GMT  
		Size: 144.3 MB (144341521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6.0` - linux; 386

```console
$ docker pull mono@sha256:94e58f1ce29ecb43527eb823856f0434fa0d3a0812ecc31df88f0e9d2e1c3eb2
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.3 MB (241294092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce5575a49e77c965605a2abaa50aa38f2aa1668e66c41a766b116df708ca2d2f`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:42:13 GMT
ADD file:82f76d577eec142f824456d027e5f82f681c9f5a09aeef4f711cef4662dcaea4 in / 
# Thu, 23 Apr 2020 00:42:13 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:05:07 GMT
ENV MONO_VERSION=6.6.0.161
# Thu, 23 Apr 2020 01:05:17 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 01:05:53 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Apr 2020 01:11:47 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7cb0551c4675347b94a8c63d7ee1f99dea4ab34aa7f23602ca587b6894d0211b`  
		Last Modified: Thu, 23 Apr 2020 00:47:39 GMT  
		Size: 23.1 MB (23141423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2beb89e4f0bd2e26a4512b29f2528cda17c529914331e656630af13f14143f8`  
		Last Modified: Thu, 23 Apr 2020 01:14:38 GMT  
		Size: 244.5 KB (244501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c70df528f46cab25e9c07e896d643cac9c7968e0e534e9d4702c3645865f689b`  
		Last Modified: Thu, 23 Apr 2020 01:14:55 GMT  
		Size: 66.7 MB (66747446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb378b781be2a120cd2fa519211a18f9a67e6bd23b8442b3ae140570f8371226`  
		Last Modified: Thu, 23 Apr 2020 01:16:57 GMT  
		Size: 151.2 MB (151160722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6.0` - linux; ppc64le

```console
$ docker pull mono@sha256:4235fd48012578b4b57f350c979ce60090348f15633d786dc80f4411f4c99add
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.8 MB (178801331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0e1d4c00d6874adca289180ab7f6005e5ac7d7624540b0086d8e64f470f7981`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 01:43:57 GMT
ADD file:1c7f60f778e4b93490d570487d56275925e5eb477632e71cb9f035ce6edf2460 in / 
# Thu, 16 Apr 2020 01:44:03 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 06:41:39 GMT
ENV MONO_VERSION=6.6.0.161
# Thu, 16 Apr 2020 06:42:53 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Apr 2020 06:44:39 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 16 Apr 2020 07:10:39 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:15e508b90ba1d327da83b72fc494ca263c1566ef6f70b91001cf2093395ffa3d`  
		Last Modified: Thu, 16 Apr 2020 02:04:33 GMT  
		Size: 22.8 MB (22785425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:800a5760720ebbe560ce8ace6be98139c4a1b70fe59bfc7d95e64b47f5b3d969`  
		Last Modified: Thu, 16 Apr 2020 07:19:01 GMT  
		Size: 244.6 KB (244581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3f899767b86a83eb94a1fb10e4abe4060361f3991cd7998c06677ee9f1875d4`  
		Last Modified: Thu, 16 Apr 2020 07:19:06 GMT  
		Size: 25.8 MB (25828268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05e9c715d026067720e1b2fda245dc97d172d2aeb0bd6be2d86bd4cc8807af4c`  
		Last Modified: Thu, 16 Apr 2020 07:20:54 GMT  
		Size: 129.9 MB (129943057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.6.0.161`

```console
$ docker pull mono@sha256:a7fb3160feb8b4f8cfd50f8f8db1224876a71b615669b94b04740b9979853a2b
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
$ docker pull mono@sha256:0b433fb0621e18ac0684b0856a02e22fe9e60c4825c893dc33224e2285537c10
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (233037618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7db13482ea72da7effe51ad083a644e0c8bb62c71eb2b3437327862b017c603`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 03:27:50 GMT
ADD file:40f52c233aecabf572a9db7450590d54d5e125fb00ecbb4a26fecd0b71e84eb8 in / 
# Thu, 16 Apr 2020 03:27:50 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 09:12:43 GMT
ENV MONO_VERSION=6.6.0.161
# Thu, 16 Apr 2020 09:12:53 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Apr 2020 09:13:30 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 16 Apr 2020 09:36:35 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:5e35bd43cf7898d036f8515be74d45b2e3abd2a5534fc280de63a9c22dd175bd`  
		Last Modified: Thu, 16 Apr 2020 03:35:04 GMT  
		Size: 22.5 MB (22513476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f76aee1152e1c17c5c2fde70a7bebdd5d5c8a9895316482efbb1bf3cab92edb5`  
		Last Modified: Thu, 16 Apr 2020 09:46:59 GMT  
		Size: 244.5 KB (244511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b21609b816b63406b186989f8e6ea95d37bb9e8f9fc6a39377d450d2888dd633`  
		Last Modified: Thu, 16 Apr 2020 09:47:15 GMT  
		Size: 63.0 MB (62972017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39364a66c8bcea35cb1bbc438ec3b34aa23c52b5bd6b5d1781c8ad74843041dc`  
		Last Modified: Thu, 16 Apr 2020 09:49:06 GMT  
		Size: 147.3 MB (147307614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6.0.161` - linux; arm variant v5

```console
$ docker pull mono@sha256:953b98f308c725c908039c6b0119c4308afde0a43bee73a9212123c246e3ba14
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.5 MB (176499196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30ab99fcbe0706e2c5cbf3b3f402c4f222fa6a4deec87d1658ac0883e0de7c94`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 00:54:51 GMT
ADD file:ba6c5e03457e69f59231e8e7c6465c1ec985812f0d8f7a65d9842f2be3e947fb in / 
# Thu, 16 Apr 2020 00:54:54 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 03:23:39 GMT
ENV MONO_VERSION=6.6.0.161
# Thu, 16 Apr 2020 03:24:08 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Apr 2020 03:25:01 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 16 Apr 2020 03:32:10 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:b7d527e4baf13a6c926fb354fe1b38cb42b96f249ae65fdc0f52c853b654e06e`  
		Last Modified: Thu, 16 Apr 2020 01:02:32 GMT  
		Size: 21.2 MB (21190797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2182e7eff26a84a3839979b8dc30f86f313c10d5a9c5cb556911ea13a0a09b7`  
		Last Modified: Thu, 16 Apr 2020 03:36:31 GMT  
		Size: 244.6 KB (244558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65ecd30f76c6d61fc0338f94136d06ae87f496afd7cccaea0a67ef39cc037534`  
		Last Modified: Thu, 16 Apr 2020 03:36:42 GMT  
		Size: 25.4 MB (25414654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71bbeb6d8b71001853c4ac6381a1e2da4bed657325144da5a05f53de8571155b`  
		Last Modified: Thu, 16 Apr 2020 03:38:48 GMT  
		Size: 129.6 MB (129649187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6.0.161` - linux; arm variant v7

```console
$ docker pull mono@sha256:dfff052f102fe7d4378e5d2b0245680892904cbd70cb13786faf09e0ac56dfb3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.5 MB (172506927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b22ad409e9a2275f54ce587900650610baa7b303fd2f52317ef1049368fce42`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 01:05:08 GMT
ADD file:e37c4728c0c89ac126542ac35e7e493425c021bfac751079c9b266821a1b4e99 in / 
# Thu, 16 Apr 2020 01:05:10 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 04:41:55 GMT
ENV MONO_VERSION=6.6.0.161
# Thu, 16 Apr 2020 04:42:15 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Apr 2020 04:43:04 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 16 Apr 2020 04:50:27 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:f78d9963dfddc4747d6200353b50f6093a6e37ca82e1612fa397d64ff13e7299`  
		Last Modified: Thu, 16 Apr 2020 01:12:33 GMT  
		Size: 19.3 MB (19298546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7c709444af1581614022f19533f2bd4e0a3468d7051453df34e50bf99df9321`  
		Last Modified: Thu, 16 Apr 2020 04:54:19 GMT  
		Size: 244.5 KB (244546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a96b6dd89ea6225de279fd91629a436f6398c0547a59d1d7935d302802dec507`  
		Last Modified: Thu, 16 Apr 2020 04:54:29 GMT  
		Size: 24.6 MB (24648627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ff75ba1385b277ecc3e4c7e6201fd3706aa69b722a429fefcc75f0c5beb09b7`  
		Last Modified: Thu, 16 Apr 2020 04:56:40 GMT  
		Size: 128.3 MB (128315208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6.0.161` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:d50f772e76b54a7da4d565208fcabf191b1246e0ad0853a269e282f7824d2623
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.4 MB (194394691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daed0db4cc3b4df6b71cd4424bfe0f98d8c6bffb99925929d809841240cd7d31`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 02:45:19 GMT
ADD file:1588320d1c43714ec0353b7471f2ffd649045ca0f5f70dcb1eb064875fff9578 in / 
# Thu, 16 Apr 2020 02:45:21 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 06:48:23 GMT
ENV MONO_VERSION=6.6.0.161
# Thu, 16 Apr 2020 06:48:40 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Apr 2020 06:49:27 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 16 Apr 2020 06:56:13 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:8978c87ff45d64d1663a585dcf1ed66d9e711c2e4048d83ef561da9514ef46e6`  
		Last Modified: Thu, 16 Apr 2020 02:51:32 GMT  
		Size: 20.4 MB (20370106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f4cefd4f77cad9e57aea080af9eb57c1991ab847ef1ab0a04c72c47d4d11332`  
		Last Modified: Thu, 16 Apr 2020 06:59:39 GMT  
		Size: 244.4 KB (244371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16a24563d28e05e4d85e2e968cf5a1be1fd764682e892a24a0323b2c2daee23a`  
		Last Modified: Thu, 16 Apr 2020 06:59:49 GMT  
		Size: 29.4 MB (29438693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e5fd0d429b209d5930a2be3ed4225f606136251ea4a38b4a31f015eb3c3b25a`  
		Last Modified: Thu, 16 Apr 2020 07:02:02 GMT  
		Size: 144.3 MB (144341521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6.0.161` - linux; 386

```console
$ docker pull mono@sha256:94e58f1ce29ecb43527eb823856f0434fa0d3a0812ecc31df88f0e9d2e1c3eb2
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.3 MB (241294092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce5575a49e77c965605a2abaa50aa38f2aa1668e66c41a766b116df708ca2d2f`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:42:13 GMT
ADD file:82f76d577eec142f824456d027e5f82f681c9f5a09aeef4f711cef4662dcaea4 in / 
# Thu, 23 Apr 2020 00:42:13 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:05:07 GMT
ENV MONO_VERSION=6.6.0.161
# Thu, 23 Apr 2020 01:05:17 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 01:05:53 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Apr 2020 01:11:47 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7cb0551c4675347b94a8c63d7ee1f99dea4ab34aa7f23602ca587b6894d0211b`  
		Last Modified: Thu, 23 Apr 2020 00:47:39 GMT  
		Size: 23.1 MB (23141423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2beb89e4f0bd2e26a4512b29f2528cda17c529914331e656630af13f14143f8`  
		Last Modified: Thu, 23 Apr 2020 01:14:38 GMT  
		Size: 244.5 KB (244501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c70df528f46cab25e9c07e896d643cac9c7968e0e534e9d4702c3645865f689b`  
		Last Modified: Thu, 23 Apr 2020 01:14:55 GMT  
		Size: 66.7 MB (66747446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb378b781be2a120cd2fa519211a18f9a67e6bd23b8442b3ae140570f8371226`  
		Last Modified: Thu, 23 Apr 2020 01:16:57 GMT  
		Size: 151.2 MB (151160722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6.0.161` - linux; ppc64le

```console
$ docker pull mono@sha256:4235fd48012578b4b57f350c979ce60090348f15633d786dc80f4411f4c99add
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.8 MB (178801331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0e1d4c00d6874adca289180ab7f6005e5ac7d7624540b0086d8e64f470f7981`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 01:43:57 GMT
ADD file:1c7f60f778e4b93490d570487d56275925e5eb477632e71cb9f035ce6edf2460 in / 
# Thu, 16 Apr 2020 01:44:03 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 06:41:39 GMT
ENV MONO_VERSION=6.6.0.161
# Thu, 16 Apr 2020 06:42:53 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Apr 2020 06:44:39 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 16 Apr 2020 07:10:39 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:15e508b90ba1d327da83b72fc494ca263c1566ef6f70b91001cf2093395ffa3d`  
		Last Modified: Thu, 16 Apr 2020 02:04:33 GMT  
		Size: 22.8 MB (22785425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:800a5760720ebbe560ce8ace6be98139c4a1b70fe59bfc7d95e64b47f5b3d969`  
		Last Modified: Thu, 16 Apr 2020 07:19:01 GMT  
		Size: 244.6 KB (244581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3f899767b86a83eb94a1fb10e4abe4060361f3991cd7998c06677ee9f1875d4`  
		Last Modified: Thu, 16 Apr 2020 07:19:06 GMT  
		Size: 25.8 MB (25828268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05e9c715d026067720e1b2fda245dc97d172d2aeb0bd6be2d86bd4cc8807af4c`  
		Last Modified: Thu, 16 Apr 2020 07:20:54 GMT  
		Size: 129.9 MB (129943057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.6.0.161-slim`

```console
$ docker pull mono@sha256:ef4486fa1f5b8098bb66308dec1895859ecb8e18ce2a0eb1ded57fe03ee7e7ec
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
$ docker pull mono@sha256:07da38c1895db10fbb994fb860763a3fab963f4b1cb804b987e038e16c69760f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.7 MB (85730004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ed56916298153ea67a2ea8de93827d991a1a7fd05921a1ae3edee55ed29d0c1`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 03:27:50 GMT
ADD file:40f52c233aecabf572a9db7450590d54d5e125fb00ecbb4a26fecd0b71e84eb8 in / 
# Thu, 16 Apr 2020 03:27:50 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 09:12:43 GMT
ENV MONO_VERSION=6.6.0.161
# Thu, 16 Apr 2020 09:12:53 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Apr 2020 09:13:30 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:5e35bd43cf7898d036f8515be74d45b2e3abd2a5534fc280de63a9c22dd175bd`  
		Last Modified: Thu, 16 Apr 2020 03:35:04 GMT  
		Size: 22.5 MB (22513476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f76aee1152e1c17c5c2fde70a7bebdd5d5c8a9895316482efbb1bf3cab92edb5`  
		Last Modified: Thu, 16 Apr 2020 09:46:59 GMT  
		Size: 244.5 KB (244511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b21609b816b63406b186989f8e6ea95d37bb9e8f9fc6a39377d450d2888dd633`  
		Last Modified: Thu, 16 Apr 2020 09:47:15 GMT  
		Size: 63.0 MB (62972017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6.0.161-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:ff7be92bffd22f5c5c9ee40c5ca9dc8bfc0a339f7b2d1258d8fcd80f473fe8d9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46850009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cb507c773d86606ba4283207fa5d7c414c8a0e2600d98a83fab25e2a0000af4`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 00:54:51 GMT
ADD file:ba6c5e03457e69f59231e8e7c6465c1ec985812f0d8f7a65d9842f2be3e947fb in / 
# Thu, 16 Apr 2020 00:54:54 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 03:23:39 GMT
ENV MONO_VERSION=6.6.0.161
# Thu, 16 Apr 2020 03:24:08 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Apr 2020 03:25:01 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:b7d527e4baf13a6c926fb354fe1b38cb42b96f249ae65fdc0f52c853b654e06e`  
		Last Modified: Thu, 16 Apr 2020 01:02:32 GMT  
		Size: 21.2 MB (21190797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2182e7eff26a84a3839979b8dc30f86f313c10d5a9c5cb556911ea13a0a09b7`  
		Last Modified: Thu, 16 Apr 2020 03:36:31 GMT  
		Size: 244.6 KB (244558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65ecd30f76c6d61fc0338f94136d06ae87f496afd7cccaea0a67ef39cc037534`  
		Last Modified: Thu, 16 Apr 2020 03:36:42 GMT  
		Size: 25.4 MB (25414654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6.0.161-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:178e41cc93222a41c9213913be27ccaef31e8bdae25c236b9bc7f15c586556fa
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44191719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b603e30bde8ac1284185618c04169108253926d664211535358329cdba084966`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 01:05:08 GMT
ADD file:e37c4728c0c89ac126542ac35e7e493425c021bfac751079c9b266821a1b4e99 in / 
# Thu, 16 Apr 2020 01:05:10 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 04:41:55 GMT
ENV MONO_VERSION=6.6.0.161
# Thu, 16 Apr 2020 04:42:15 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Apr 2020 04:43:04 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:f78d9963dfddc4747d6200353b50f6093a6e37ca82e1612fa397d64ff13e7299`  
		Last Modified: Thu, 16 Apr 2020 01:12:33 GMT  
		Size: 19.3 MB (19298546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7c709444af1581614022f19533f2bd4e0a3468d7051453df34e50bf99df9321`  
		Last Modified: Thu, 16 Apr 2020 04:54:19 GMT  
		Size: 244.5 KB (244546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a96b6dd89ea6225de279fd91629a436f6398c0547a59d1d7935d302802dec507`  
		Last Modified: Thu, 16 Apr 2020 04:54:29 GMT  
		Size: 24.6 MB (24648627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6.0.161-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:1073439807b38491b1361fa823ed651e7d2fe8946f4daa186cdb534c5806a53e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50053170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f03b552f7a35880b1429c8cd04ab1e514af560cdec6a4b938eec85fb4171df4a`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 02:45:19 GMT
ADD file:1588320d1c43714ec0353b7471f2ffd649045ca0f5f70dcb1eb064875fff9578 in / 
# Thu, 16 Apr 2020 02:45:21 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 06:48:23 GMT
ENV MONO_VERSION=6.6.0.161
# Thu, 16 Apr 2020 06:48:40 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Apr 2020 06:49:27 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:8978c87ff45d64d1663a585dcf1ed66d9e711c2e4048d83ef561da9514ef46e6`  
		Last Modified: Thu, 16 Apr 2020 02:51:32 GMT  
		Size: 20.4 MB (20370106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f4cefd4f77cad9e57aea080af9eb57c1991ab847ef1ab0a04c72c47d4d11332`  
		Last Modified: Thu, 16 Apr 2020 06:59:39 GMT  
		Size: 244.4 KB (244371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16a24563d28e05e4d85e2e968cf5a1be1fd764682e892a24a0323b2c2daee23a`  
		Last Modified: Thu, 16 Apr 2020 06:59:49 GMT  
		Size: 29.4 MB (29438693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6.0.161-slim` - linux; 386

```console
$ docker pull mono@sha256:a0ac6b4bdd3d9afea4096b59694f0b606472414433c3d035705aed0080cfe308
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.1 MB (90133370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4d67cb1f0471d746abc265542e8168ced8da1ff1614c4118e963641dd9629f6`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:42:13 GMT
ADD file:82f76d577eec142f824456d027e5f82f681c9f5a09aeef4f711cef4662dcaea4 in / 
# Thu, 23 Apr 2020 00:42:13 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:05:07 GMT
ENV MONO_VERSION=6.6.0.161
# Thu, 23 Apr 2020 01:05:17 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 01:05:53 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7cb0551c4675347b94a8c63d7ee1f99dea4ab34aa7f23602ca587b6894d0211b`  
		Last Modified: Thu, 23 Apr 2020 00:47:39 GMT  
		Size: 23.1 MB (23141423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2beb89e4f0bd2e26a4512b29f2528cda17c529914331e656630af13f14143f8`  
		Last Modified: Thu, 23 Apr 2020 01:14:38 GMT  
		Size: 244.5 KB (244501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c70df528f46cab25e9c07e896d643cac9c7968e0e534e9d4702c3645865f689b`  
		Last Modified: Thu, 23 Apr 2020 01:14:55 GMT  
		Size: 66.7 MB (66747446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6.0.161-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:fe2739cc6a3e74a354559a9adf6a4ef35e99e02919f63f61a638212d94db1cf3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48858274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a7b23b2940938c882d83d74c0abfcb54a61b2ffe4ee58f84c629f4339ea2007`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 01:43:57 GMT
ADD file:1c7f60f778e4b93490d570487d56275925e5eb477632e71cb9f035ce6edf2460 in / 
# Thu, 16 Apr 2020 01:44:03 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 06:41:39 GMT
ENV MONO_VERSION=6.6.0.161
# Thu, 16 Apr 2020 06:42:53 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Apr 2020 06:44:39 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:15e508b90ba1d327da83b72fc494ca263c1566ef6f70b91001cf2093395ffa3d`  
		Last Modified: Thu, 16 Apr 2020 02:04:33 GMT  
		Size: 22.8 MB (22785425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:800a5760720ebbe560ce8ace6be98139c4a1b70fe59bfc7d95e64b47f5b3d969`  
		Last Modified: Thu, 16 Apr 2020 07:19:01 GMT  
		Size: 244.6 KB (244581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3f899767b86a83eb94a1fb10e4abe4060361f3991cd7998c06677ee9f1875d4`  
		Last Modified: Thu, 16 Apr 2020 07:19:06 GMT  
		Size: 25.8 MB (25828268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.6.0-slim`

```console
$ docker pull mono@sha256:ef4486fa1f5b8098bb66308dec1895859ecb8e18ce2a0eb1ded57fe03ee7e7ec
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
$ docker pull mono@sha256:07da38c1895db10fbb994fb860763a3fab963f4b1cb804b987e038e16c69760f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.7 MB (85730004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ed56916298153ea67a2ea8de93827d991a1a7fd05921a1ae3edee55ed29d0c1`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 03:27:50 GMT
ADD file:40f52c233aecabf572a9db7450590d54d5e125fb00ecbb4a26fecd0b71e84eb8 in / 
# Thu, 16 Apr 2020 03:27:50 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 09:12:43 GMT
ENV MONO_VERSION=6.6.0.161
# Thu, 16 Apr 2020 09:12:53 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Apr 2020 09:13:30 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:5e35bd43cf7898d036f8515be74d45b2e3abd2a5534fc280de63a9c22dd175bd`  
		Last Modified: Thu, 16 Apr 2020 03:35:04 GMT  
		Size: 22.5 MB (22513476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f76aee1152e1c17c5c2fde70a7bebdd5d5c8a9895316482efbb1bf3cab92edb5`  
		Last Modified: Thu, 16 Apr 2020 09:46:59 GMT  
		Size: 244.5 KB (244511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b21609b816b63406b186989f8e6ea95d37bb9e8f9fc6a39377d450d2888dd633`  
		Last Modified: Thu, 16 Apr 2020 09:47:15 GMT  
		Size: 63.0 MB (62972017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6.0-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:ff7be92bffd22f5c5c9ee40c5ca9dc8bfc0a339f7b2d1258d8fcd80f473fe8d9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46850009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cb507c773d86606ba4283207fa5d7c414c8a0e2600d98a83fab25e2a0000af4`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 00:54:51 GMT
ADD file:ba6c5e03457e69f59231e8e7c6465c1ec985812f0d8f7a65d9842f2be3e947fb in / 
# Thu, 16 Apr 2020 00:54:54 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 03:23:39 GMT
ENV MONO_VERSION=6.6.0.161
# Thu, 16 Apr 2020 03:24:08 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Apr 2020 03:25:01 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:b7d527e4baf13a6c926fb354fe1b38cb42b96f249ae65fdc0f52c853b654e06e`  
		Last Modified: Thu, 16 Apr 2020 01:02:32 GMT  
		Size: 21.2 MB (21190797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2182e7eff26a84a3839979b8dc30f86f313c10d5a9c5cb556911ea13a0a09b7`  
		Last Modified: Thu, 16 Apr 2020 03:36:31 GMT  
		Size: 244.6 KB (244558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65ecd30f76c6d61fc0338f94136d06ae87f496afd7cccaea0a67ef39cc037534`  
		Last Modified: Thu, 16 Apr 2020 03:36:42 GMT  
		Size: 25.4 MB (25414654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6.0-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:178e41cc93222a41c9213913be27ccaef31e8bdae25c236b9bc7f15c586556fa
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44191719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b603e30bde8ac1284185618c04169108253926d664211535358329cdba084966`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 01:05:08 GMT
ADD file:e37c4728c0c89ac126542ac35e7e493425c021bfac751079c9b266821a1b4e99 in / 
# Thu, 16 Apr 2020 01:05:10 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 04:41:55 GMT
ENV MONO_VERSION=6.6.0.161
# Thu, 16 Apr 2020 04:42:15 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Apr 2020 04:43:04 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:f78d9963dfddc4747d6200353b50f6093a6e37ca82e1612fa397d64ff13e7299`  
		Last Modified: Thu, 16 Apr 2020 01:12:33 GMT  
		Size: 19.3 MB (19298546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7c709444af1581614022f19533f2bd4e0a3468d7051453df34e50bf99df9321`  
		Last Modified: Thu, 16 Apr 2020 04:54:19 GMT  
		Size: 244.5 KB (244546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a96b6dd89ea6225de279fd91629a436f6398c0547a59d1d7935d302802dec507`  
		Last Modified: Thu, 16 Apr 2020 04:54:29 GMT  
		Size: 24.6 MB (24648627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6.0-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:1073439807b38491b1361fa823ed651e7d2fe8946f4daa186cdb534c5806a53e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50053170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f03b552f7a35880b1429c8cd04ab1e514af560cdec6a4b938eec85fb4171df4a`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 02:45:19 GMT
ADD file:1588320d1c43714ec0353b7471f2ffd649045ca0f5f70dcb1eb064875fff9578 in / 
# Thu, 16 Apr 2020 02:45:21 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 06:48:23 GMT
ENV MONO_VERSION=6.6.0.161
# Thu, 16 Apr 2020 06:48:40 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Apr 2020 06:49:27 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:8978c87ff45d64d1663a585dcf1ed66d9e711c2e4048d83ef561da9514ef46e6`  
		Last Modified: Thu, 16 Apr 2020 02:51:32 GMT  
		Size: 20.4 MB (20370106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f4cefd4f77cad9e57aea080af9eb57c1991ab847ef1ab0a04c72c47d4d11332`  
		Last Modified: Thu, 16 Apr 2020 06:59:39 GMT  
		Size: 244.4 KB (244371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16a24563d28e05e4d85e2e968cf5a1be1fd764682e892a24a0323b2c2daee23a`  
		Last Modified: Thu, 16 Apr 2020 06:59:49 GMT  
		Size: 29.4 MB (29438693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6.0-slim` - linux; 386

```console
$ docker pull mono@sha256:a0ac6b4bdd3d9afea4096b59694f0b606472414433c3d035705aed0080cfe308
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.1 MB (90133370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4d67cb1f0471d746abc265542e8168ced8da1ff1614c4118e963641dd9629f6`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:42:13 GMT
ADD file:82f76d577eec142f824456d027e5f82f681c9f5a09aeef4f711cef4662dcaea4 in / 
# Thu, 23 Apr 2020 00:42:13 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:05:07 GMT
ENV MONO_VERSION=6.6.0.161
# Thu, 23 Apr 2020 01:05:17 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 01:05:53 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7cb0551c4675347b94a8c63d7ee1f99dea4ab34aa7f23602ca587b6894d0211b`  
		Last Modified: Thu, 23 Apr 2020 00:47:39 GMT  
		Size: 23.1 MB (23141423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2beb89e4f0bd2e26a4512b29f2528cda17c529914331e656630af13f14143f8`  
		Last Modified: Thu, 23 Apr 2020 01:14:38 GMT  
		Size: 244.5 KB (244501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c70df528f46cab25e9c07e896d643cac9c7968e0e534e9d4702c3645865f689b`  
		Last Modified: Thu, 23 Apr 2020 01:14:55 GMT  
		Size: 66.7 MB (66747446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6.0-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:fe2739cc6a3e74a354559a9adf6a4ef35e99e02919f63f61a638212d94db1cf3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48858274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a7b23b2940938c882d83d74c0abfcb54a61b2ffe4ee58f84c629f4339ea2007`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 01:43:57 GMT
ADD file:1c7f60f778e4b93490d570487d56275925e5eb477632e71cb9f035ce6edf2460 in / 
# Thu, 16 Apr 2020 01:44:03 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 06:41:39 GMT
ENV MONO_VERSION=6.6.0.161
# Thu, 16 Apr 2020 06:42:53 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Apr 2020 06:44:39 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:15e508b90ba1d327da83b72fc494ca263c1566ef6f70b91001cf2093395ffa3d`  
		Last Modified: Thu, 16 Apr 2020 02:04:33 GMT  
		Size: 22.8 MB (22785425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:800a5760720ebbe560ce8ace6be98139c4a1b70fe59bfc7d95e64b47f5b3d969`  
		Last Modified: Thu, 16 Apr 2020 07:19:01 GMT  
		Size: 244.6 KB (244581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3f899767b86a83eb94a1fb10e4abe4060361f3991cd7998c06677ee9f1875d4`  
		Last Modified: Thu, 16 Apr 2020 07:19:06 GMT  
		Size: 25.8 MB (25828268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.6-slim`

```console
$ docker pull mono@sha256:ef4486fa1f5b8098bb66308dec1895859ecb8e18ce2a0eb1ded57fe03ee7e7ec
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
$ docker pull mono@sha256:07da38c1895db10fbb994fb860763a3fab963f4b1cb804b987e038e16c69760f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.7 MB (85730004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ed56916298153ea67a2ea8de93827d991a1a7fd05921a1ae3edee55ed29d0c1`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 03:27:50 GMT
ADD file:40f52c233aecabf572a9db7450590d54d5e125fb00ecbb4a26fecd0b71e84eb8 in / 
# Thu, 16 Apr 2020 03:27:50 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 09:12:43 GMT
ENV MONO_VERSION=6.6.0.161
# Thu, 16 Apr 2020 09:12:53 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Apr 2020 09:13:30 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:5e35bd43cf7898d036f8515be74d45b2e3abd2a5534fc280de63a9c22dd175bd`  
		Last Modified: Thu, 16 Apr 2020 03:35:04 GMT  
		Size: 22.5 MB (22513476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f76aee1152e1c17c5c2fde70a7bebdd5d5c8a9895316482efbb1bf3cab92edb5`  
		Last Modified: Thu, 16 Apr 2020 09:46:59 GMT  
		Size: 244.5 KB (244511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b21609b816b63406b186989f8e6ea95d37bb9e8f9fc6a39377d450d2888dd633`  
		Last Modified: Thu, 16 Apr 2020 09:47:15 GMT  
		Size: 63.0 MB (62972017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:ff7be92bffd22f5c5c9ee40c5ca9dc8bfc0a339f7b2d1258d8fcd80f473fe8d9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46850009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cb507c773d86606ba4283207fa5d7c414c8a0e2600d98a83fab25e2a0000af4`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 00:54:51 GMT
ADD file:ba6c5e03457e69f59231e8e7c6465c1ec985812f0d8f7a65d9842f2be3e947fb in / 
# Thu, 16 Apr 2020 00:54:54 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 03:23:39 GMT
ENV MONO_VERSION=6.6.0.161
# Thu, 16 Apr 2020 03:24:08 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Apr 2020 03:25:01 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:b7d527e4baf13a6c926fb354fe1b38cb42b96f249ae65fdc0f52c853b654e06e`  
		Last Modified: Thu, 16 Apr 2020 01:02:32 GMT  
		Size: 21.2 MB (21190797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2182e7eff26a84a3839979b8dc30f86f313c10d5a9c5cb556911ea13a0a09b7`  
		Last Modified: Thu, 16 Apr 2020 03:36:31 GMT  
		Size: 244.6 KB (244558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65ecd30f76c6d61fc0338f94136d06ae87f496afd7cccaea0a67ef39cc037534`  
		Last Modified: Thu, 16 Apr 2020 03:36:42 GMT  
		Size: 25.4 MB (25414654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:178e41cc93222a41c9213913be27ccaef31e8bdae25c236b9bc7f15c586556fa
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44191719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b603e30bde8ac1284185618c04169108253926d664211535358329cdba084966`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 01:05:08 GMT
ADD file:e37c4728c0c89ac126542ac35e7e493425c021bfac751079c9b266821a1b4e99 in / 
# Thu, 16 Apr 2020 01:05:10 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 04:41:55 GMT
ENV MONO_VERSION=6.6.0.161
# Thu, 16 Apr 2020 04:42:15 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Apr 2020 04:43:04 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:f78d9963dfddc4747d6200353b50f6093a6e37ca82e1612fa397d64ff13e7299`  
		Last Modified: Thu, 16 Apr 2020 01:12:33 GMT  
		Size: 19.3 MB (19298546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7c709444af1581614022f19533f2bd4e0a3468d7051453df34e50bf99df9321`  
		Last Modified: Thu, 16 Apr 2020 04:54:19 GMT  
		Size: 244.5 KB (244546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a96b6dd89ea6225de279fd91629a436f6398c0547a59d1d7935d302802dec507`  
		Last Modified: Thu, 16 Apr 2020 04:54:29 GMT  
		Size: 24.6 MB (24648627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:1073439807b38491b1361fa823ed651e7d2fe8946f4daa186cdb534c5806a53e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50053170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f03b552f7a35880b1429c8cd04ab1e514af560cdec6a4b938eec85fb4171df4a`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 02:45:19 GMT
ADD file:1588320d1c43714ec0353b7471f2ffd649045ca0f5f70dcb1eb064875fff9578 in / 
# Thu, 16 Apr 2020 02:45:21 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 06:48:23 GMT
ENV MONO_VERSION=6.6.0.161
# Thu, 16 Apr 2020 06:48:40 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Apr 2020 06:49:27 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:8978c87ff45d64d1663a585dcf1ed66d9e711c2e4048d83ef561da9514ef46e6`  
		Last Modified: Thu, 16 Apr 2020 02:51:32 GMT  
		Size: 20.4 MB (20370106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f4cefd4f77cad9e57aea080af9eb57c1991ab847ef1ab0a04c72c47d4d11332`  
		Last Modified: Thu, 16 Apr 2020 06:59:39 GMT  
		Size: 244.4 KB (244371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16a24563d28e05e4d85e2e968cf5a1be1fd764682e892a24a0323b2c2daee23a`  
		Last Modified: Thu, 16 Apr 2020 06:59:49 GMT  
		Size: 29.4 MB (29438693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6-slim` - linux; 386

```console
$ docker pull mono@sha256:a0ac6b4bdd3d9afea4096b59694f0b606472414433c3d035705aed0080cfe308
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.1 MB (90133370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4d67cb1f0471d746abc265542e8168ced8da1ff1614c4118e963641dd9629f6`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:42:13 GMT
ADD file:82f76d577eec142f824456d027e5f82f681c9f5a09aeef4f711cef4662dcaea4 in / 
# Thu, 23 Apr 2020 00:42:13 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:05:07 GMT
ENV MONO_VERSION=6.6.0.161
# Thu, 23 Apr 2020 01:05:17 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 01:05:53 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7cb0551c4675347b94a8c63d7ee1f99dea4ab34aa7f23602ca587b6894d0211b`  
		Last Modified: Thu, 23 Apr 2020 00:47:39 GMT  
		Size: 23.1 MB (23141423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2beb89e4f0bd2e26a4512b29f2528cda17c529914331e656630af13f14143f8`  
		Last Modified: Thu, 23 Apr 2020 01:14:38 GMT  
		Size: 244.5 KB (244501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c70df528f46cab25e9c07e896d643cac9c7968e0e534e9d4702c3645865f689b`  
		Last Modified: Thu, 23 Apr 2020 01:14:55 GMT  
		Size: 66.7 MB (66747446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:fe2739cc6a3e74a354559a9adf6a4ef35e99e02919f63f61a638212d94db1cf3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48858274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a7b23b2940938c882d83d74c0abfcb54a61b2ffe4ee58f84c629f4339ea2007`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 01:43:57 GMT
ADD file:1c7f60f778e4b93490d570487d56275925e5eb477632e71cb9f035ce6edf2460 in / 
# Thu, 16 Apr 2020 01:44:03 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 06:41:39 GMT
ENV MONO_VERSION=6.6.0.161
# Thu, 16 Apr 2020 06:42:53 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Apr 2020 06:44:39 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:15e508b90ba1d327da83b72fc494ca263c1566ef6f70b91001cf2093395ffa3d`  
		Last Modified: Thu, 16 Apr 2020 02:04:33 GMT  
		Size: 22.8 MB (22785425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:800a5760720ebbe560ce8ace6be98139c4a1b70fe59bfc7d95e64b47f5b3d969`  
		Last Modified: Thu, 16 Apr 2020 07:19:01 GMT  
		Size: 244.6 KB (244581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3f899767b86a83eb94a1fb10e4abe4060361f3991cd7998c06677ee9f1875d4`  
		Last Modified: Thu, 16 Apr 2020 07:19:06 GMT  
		Size: 25.8 MB (25828268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.8`

```console
$ docker pull mono@sha256:8b4551b8332e7efec0aa7c0fed4f53a7cf6bed12cbee05f6858ffb65a79aa5cd
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
$ docker pull mono@sha256:3d109ece622c61e26832ecee8eafdafa2e72535b9c74d735d879ca179b1a13b8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.1 MB (235135830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51f7ccdd96f0dfed7dc0f8f3af746f9edb7e71a7f93e19af1ea4b9bccb53d336`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 03:27:50 GMT
ADD file:40f52c233aecabf572a9db7450590d54d5e125fb00ecbb4a26fecd0b71e84eb8 in / 
# Thu, 16 Apr 2020 03:27:50 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 09:11:48 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 16 Apr 2020 09:12:00 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Apr 2020 09:12:35 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 16 Apr 2020 09:25:34 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:5e35bd43cf7898d036f8515be74d45b2e3abd2a5534fc280de63a9c22dd175bd`  
		Last Modified: Thu, 16 Apr 2020 03:35:04 GMT  
		Size: 22.5 MB (22513476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79f990050ea7755c8b4310123b2d720a7fede3eaa9cf5a76acb2a5fbd0af58d5`  
		Last Modified: Thu, 16 Apr 2020 09:46:33 GMT  
		Size: 244.5 KB (244519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b463238d61e87361acee422c7ed4ee873ebc66a2a7b4dde702ca6956a532ecf`  
		Last Modified: Thu, 16 Apr 2020 09:46:52 GMT  
		Size: 64.6 MB (64584108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04da7d857cd9fd3a2c4f7e602c9a50f2993fd66e67372efe5765e3b227eb1e73`  
		Last Modified: Thu, 16 Apr 2020 09:48:16 GMT  
		Size: 147.8 MB (147793727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8` - linux; arm variant v5

```console
$ docker pull mono@sha256:039a6be7bba94963928fb63f0cd7624bdcc24ff437d3511659983bf8a15da61c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.7 MB (176695282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbb0da5905f2877688de5793cf7d5f0c6b5cdbb737868e678439fec995215cfa`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 00:54:51 GMT
ADD file:ba6c5e03457e69f59231e8e7c6465c1ec985812f0d8f7a65d9842f2be3e947fb in / 
# Thu, 16 Apr 2020 00:54:54 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 03:22:05 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 16 Apr 2020 03:22:36 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Apr 2020 03:23:29 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 16 Apr 2020 03:29:10 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:b7d527e4baf13a6c926fb354fe1b38cb42b96f249ae65fdc0f52c853b654e06e`  
		Last Modified: Thu, 16 Apr 2020 01:02:32 GMT  
		Size: 21.2 MB (21190797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5251e801555d8cd1370a8d39ca953a0fb8f39729ff494b4a60bd03b4255c45be`  
		Last Modified: Thu, 16 Apr 2020 03:36:12 GMT  
		Size: 244.6 KB (244555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7c9b96b75ebb7a3cac23cf75e27179b71b5aa2cee0c40c33aca6399e29516f2`  
		Last Modified: Thu, 16 Apr 2020 03:36:22 GMT  
		Size: 25.4 MB (25367763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c33b43ad8da6addb8c852a68a9848cba5f48be98873fc8db208731eb55f31b9b`  
		Last Modified: Thu, 16 Apr 2020 03:37:53 GMT  
		Size: 129.9 MB (129892167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8` - linux; arm variant v7

```console
$ docker pull mono@sha256:09076495aacfba71beb6f4e5812d597a2d059b58d0d1a053068e4fa0fdec8443
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.7 MB (172708239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6e489c47305d9f8c107b00d2a1e335c874014e8fa4a3fc5ecb9082df7c5be0f`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 01:05:08 GMT
ADD file:e37c4728c0c89ac126542ac35e7e493425c021bfac751079c9b266821a1b4e99 in / 
# Thu, 16 Apr 2020 01:05:10 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 04:40:35 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 16 Apr 2020 04:40:56 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Apr 2020 04:41:45 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 16 Apr 2020 04:47:13 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:f78d9963dfddc4747d6200353b50f6093a6e37ca82e1612fa397d64ff13e7299`  
		Last Modified: Thu, 16 Apr 2020 01:12:33 GMT  
		Size: 19.3 MB (19298546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70114347da279136ebd21697ef769dc5764f716c6f7331568bbf7306c17da63c`  
		Last Modified: Thu, 16 Apr 2020 04:54:02 GMT  
		Size: 244.6 KB (244551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:802f26edffea7b59f9cc74e47561799e0c847d999b0db0dd2d99497c42af3511`  
		Last Modified: Thu, 16 Apr 2020 04:54:10 GMT  
		Size: 24.6 MB (24608740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62a9fd3d7648204f077b0034260c1887fe3c12c26ffadbb4223d8dc7ff65c1eb`  
		Last Modified: Thu, 16 Apr 2020 04:55:42 GMT  
		Size: 128.6 MB (128556402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:abe9ae9da3ff9d1c710471ec6a5c1b39b18e33e11b0abba7d4245a3e75b11dc0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.7 MB (194747450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5a96031ff7018d8a3f1e18642728c41f24ad314d26c4fc40907ef19fce71fcd`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 02:45:19 GMT
ADD file:1588320d1c43714ec0353b7471f2ffd649045ca0f5f70dcb1eb064875fff9578 in / 
# Thu, 16 Apr 2020 02:45:21 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 06:47:03 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 16 Apr 2020 06:47:21 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Apr 2020 06:48:05 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 16 Apr 2020 06:53:15 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:8978c87ff45d64d1663a585dcf1ed66d9e711c2e4048d83ef561da9514ef46e6`  
		Last Modified: Thu, 16 Apr 2020 02:51:32 GMT  
		Size: 20.4 MB (20370106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:090b996e11040b9a724d4b94b5f6fea43f5cee5558fdcdcb2e4627d1c596f82c`  
		Last Modified: Thu, 16 Apr 2020 06:59:20 GMT  
		Size: 244.4 KB (244369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be77ae0e8a98b883233d159b79364894a76d49f1b02badb9f57b227a26a8e1a`  
		Last Modified: Thu, 16 Apr 2020 06:59:30 GMT  
		Size: 29.4 MB (29420188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1774c3e17e0d83d02e086998900775da6efe1356459c585e7d5800434b5aaf21`  
		Last Modified: Thu, 16 Apr 2020 07:01:03 GMT  
		Size: 144.7 MB (144712787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8` - linux; 386

```console
$ docker pull mono@sha256:9c689075bb69bade3f528bb36bfe204fd3529387d13addcfe9d2c43db444d7a4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.5 MB (243509400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1505bc590d4dce8f057579c70b93a89b4ce6d044fd5f80a06eb1765872b2e2b1`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:42:13 GMT
ADD file:82f76d577eec142f824456d027e5f82f681c9f5a09aeef4f711cef4662dcaea4 in / 
# Thu, 23 Apr 2020 00:42:13 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:04:12 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 23 Apr 2020 01:04:23 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 01:05:02 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Apr 2020 01:09:10 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7cb0551c4675347b94a8c63d7ee1f99dea4ab34aa7f23602ca587b6894d0211b`  
		Last Modified: Thu, 23 Apr 2020 00:47:39 GMT  
		Size: 23.1 MB (23141423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa3b9d440d2c40f2a9f3756fc7f8347bb9ec214b84fa396a388bd94782e1a678`  
		Last Modified: Thu, 23 Apr 2020 01:14:10 GMT  
		Size: 244.5 KB (244496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de2b74896e741d2269bb5084cfdbe6af6d2fc8d9d0ed1fc3f055d7c644afad5d`  
		Last Modified: Thu, 23 Apr 2020 01:14:29 GMT  
		Size: 68.6 MB (68630969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:753f8d38ff41ce32cf902046d0c45ed81a3a5475418bddade545b50a630ae181`  
		Last Modified: Thu, 23 Apr 2020 01:16:08 GMT  
		Size: 151.5 MB (151492512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8` - linux; ppc64le

```console
$ docker pull mono@sha256:0434d01a8617e75170a4dd8a638d786d1e67ac13c9fc880e023ccd0950428e36
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.0 MB (178997743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b5e14702ff1aff3bacfb8485b742086b08ff9d01cadd82d9f8327e6ac887fcc`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 01:43:57 GMT
ADD file:1c7f60f778e4b93490d570487d56275925e5eb477632e71cb9f035ce6edf2460 in / 
# Thu, 16 Apr 2020 01:44:03 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 06:37:42 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 16 Apr 2020 06:39:43 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Apr 2020 06:41:27 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 16 Apr 2020 06:58:08 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:15e508b90ba1d327da83b72fc494ca263c1566ef6f70b91001cf2093395ffa3d`  
		Last Modified: Thu, 16 Apr 2020 02:04:33 GMT  
		Size: 22.8 MB (22785425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1629fdf02d54d31ae3023cd8b4a515c3c17a085c6135c7a10e412896d06a1f62`  
		Last Modified: Thu, 16 Apr 2020 07:18:38 GMT  
		Size: 244.7 KB (244669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fc63fa4246f2b9b66f762d8c33434e375c088c1ca73c3a389a8fb2525f93c7c`  
		Last Modified: Thu, 16 Apr 2020 07:18:43 GMT  
		Size: 25.8 MB (25775805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90ed038a48cf0007c67072a64fc2d4d1d4efd20b275bff6a15884fcfe67b0afa`  
		Last Modified: Thu, 16 Apr 2020 07:20:07 GMT  
		Size: 130.2 MB (130191844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.8.0`

```console
$ docker pull mono@sha256:8b4551b8332e7efec0aa7c0fed4f53a7cf6bed12cbee05f6858ffb65a79aa5cd
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
$ docker pull mono@sha256:3d109ece622c61e26832ecee8eafdafa2e72535b9c74d735d879ca179b1a13b8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.1 MB (235135830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51f7ccdd96f0dfed7dc0f8f3af746f9edb7e71a7f93e19af1ea4b9bccb53d336`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 03:27:50 GMT
ADD file:40f52c233aecabf572a9db7450590d54d5e125fb00ecbb4a26fecd0b71e84eb8 in / 
# Thu, 16 Apr 2020 03:27:50 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 09:11:48 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 16 Apr 2020 09:12:00 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Apr 2020 09:12:35 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 16 Apr 2020 09:25:34 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:5e35bd43cf7898d036f8515be74d45b2e3abd2a5534fc280de63a9c22dd175bd`  
		Last Modified: Thu, 16 Apr 2020 03:35:04 GMT  
		Size: 22.5 MB (22513476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79f990050ea7755c8b4310123b2d720a7fede3eaa9cf5a76acb2a5fbd0af58d5`  
		Last Modified: Thu, 16 Apr 2020 09:46:33 GMT  
		Size: 244.5 KB (244519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b463238d61e87361acee422c7ed4ee873ebc66a2a7b4dde702ca6956a532ecf`  
		Last Modified: Thu, 16 Apr 2020 09:46:52 GMT  
		Size: 64.6 MB (64584108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04da7d857cd9fd3a2c4f7e602c9a50f2993fd66e67372efe5765e3b227eb1e73`  
		Last Modified: Thu, 16 Apr 2020 09:48:16 GMT  
		Size: 147.8 MB (147793727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8.0` - linux; arm variant v5

```console
$ docker pull mono@sha256:039a6be7bba94963928fb63f0cd7624bdcc24ff437d3511659983bf8a15da61c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.7 MB (176695282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbb0da5905f2877688de5793cf7d5f0c6b5cdbb737868e678439fec995215cfa`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 00:54:51 GMT
ADD file:ba6c5e03457e69f59231e8e7c6465c1ec985812f0d8f7a65d9842f2be3e947fb in / 
# Thu, 16 Apr 2020 00:54:54 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 03:22:05 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 16 Apr 2020 03:22:36 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Apr 2020 03:23:29 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 16 Apr 2020 03:29:10 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:b7d527e4baf13a6c926fb354fe1b38cb42b96f249ae65fdc0f52c853b654e06e`  
		Last Modified: Thu, 16 Apr 2020 01:02:32 GMT  
		Size: 21.2 MB (21190797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5251e801555d8cd1370a8d39ca953a0fb8f39729ff494b4a60bd03b4255c45be`  
		Last Modified: Thu, 16 Apr 2020 03:36:12 GMT  
		Size: 244.6 KB (244555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7c9b96b75ebb7a3cac23cf75e27179b71b5aa2cee0c40c33aca6399e29516f2`  
		Last Modified: Thu, 16 Apr 2020 03:36:22 GMT  
		Size: 25.4 MB (25367763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c33b43ad8da6addb8c852a68a9848cba5f48be98873fc8db208731eb55f31b9b`  
		Last Modified: Thu, 16 Apr 2020 03:37:53 GMT  
		Size: 129.9 MB (129892167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8.0` - linux; arm variant v7

```console
$ docker pull mono@sha256:09076495aacfba71beb6f4e5812d597a2d059b58d0d1a053068e4fa0fdec8443
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.7 MB (172708239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6e489c47305d9f8c107b00d2a1e335c874014e8fa4a3fc5ecb9082df7c5be0f`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 01:05:08 GMT
ADD file:e37c4728c0c89ac126542ac35e7e493425c021bfac751079c9b266821a1b4e99 in / 
# Thu, 16 Apr 2020 01:05:10 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 04:40:35 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 16 Apr 2020 04:40:56 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Apr 2020 04:41:45 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 16 Apr 2020 04:47:13 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:f78d9963dfddc4747d6200353b50f6093a6e37ca82e1612fa397d64ff13e7299`  
		Last Modified: Thu, 16 Apr 2020 01:12:33 GMT  
		Size: 19.3 MB (19298546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70114347da279136ebd21697ef769dc5764f716c6f7331568bbf7306c17da63c`  
		Last Modified: Thu, 16 Apr 2020 04:54:02 GMT  
		Size: 244.6 KB (244551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:802f26edffea7b59f9cc74e47561799e0c847d999b0db0dd2d99497c42af3511`  
		Last Modified: Thu, 16 Apr 2020 04:54:10 GMT  
		Size: 24.6 MB (24608740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62a9fd3d7648204f077b0034260c1887fe3c12c26ffadbb4223d8dc7ff65c1eb`  
		Last Modified: Thu, 16 Apr 2020 04:55:42 GMT  
		Size: 128.6 MB (128556402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8.0` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:abe9ae9da3ff9d1c710471ec6a5c1b39b18e33e11b0abba7d4245a3e75b11dc0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.7 MB (194747450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5a96031ff7018d8a3f1e18642728c41f24ad314d26c4fc40907ef19fce71fcd`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 02:45:19 GMT
ADD file:1588320d1c43714ec0353b7471f2ffd649045ca0f5f70dcb1eb064875fff9578 in / 
# Thu, 16 Apr 2020 02:45:21 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 06:47:03 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 16 Apr 2020 06:47:21 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Apr 2020 06:48:05 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 16 Apr 2020 06:53:15 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:8978c87ff45d64d1663a585dcf1ed66d9e711c2e4048d83ef561da9514ef46e6`  
		Last Modified: Thu, 16 Apr 2020 02:51:32 GMT  
		Size: 20.4 MB (20370106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:090b996e11040b9a724d4b94b5f6fea43f5cee5558fdcdcb2e4627d1c596f82c`  
		Last Modified: Thu, 16 Apr 2020 06:59:20 GMT  
		Size: 244.4 KB (244369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be77ae0e8a98b883233d159b79364894a76d49f1b02badb9f57b227a26a8e1a`  
		Last Modified: Thu, 16 Apr 2020 06:59:30 GMT  
		Size: 29.4 MB (29420188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1774c3e17e0d83d02e086998900775da6efe1356459c585e7d5800434b5aaf21`  
		Last Modified: Thu, 16 Apr 2020 07:01:03 GMT  
		Size: 144.7 MB (144712787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8.0` - linux; 386

```console
$ docker pull mono@sha256:9c689075bb69bade3f528bb36bfe204fd3529387d13addcfe9d2c43db444d7a4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.5 MB (243509400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1505bc590d4dce8f057579c70b93a89b4ce6d044fd5f80a06eb1765872b2e2b1`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:42:13 GMT
ADD file:82f76d577eec142f824456d027e5f82f681c9f5a09aeef4f711cef4662dcaea4 in / 
# Thu, 23 Apr 2020 00:42:13 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:04:12 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 23 Apr 2020 01:04:23 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 01:05:02 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Apr 2020 01:09:10 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7cb0551c4675347b94a8c63d7ee1f99dea4ab34aa7f23602ca587b6894d0211b`  
		Last Modified: Thu, 23 Apr 2020 00:47:39 GMT  
		Size: 23.1 MB (23141423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa3b9d440d2c40f2a9f3756fc7f8347bb9ec214b84fa396a388bd94782e1a678`  
		Last Modified: Thu, 23 Apr 2020 01:14:10 GMT  
		Size: 244.5 KB (244496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de2b74896e741d2269bb5084cfdbe6af6d2fc8d9d0ed1fc3f055d7c644afad5d`  
		Last Modified: Thu, 23 Apr 2020 01:14:29 GMT  
		Size: 68.6 MB (68630969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:753f8d38ff41ce32cf902046d0c45ed81a3a5475418bddade545b50a630ae181`  
		Last Modified: Thu, 23 Apr 2020 01:16:08 GMT  
		Size: 151.5 MB (151492512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8.0` - linux; ppc64le

```console
$ docker pull mono@sha256:0434d01a8617e75170a4dd8a638d786d1e67ac13c9fc880e023ccd0950428e36
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.0 MB (178997743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b5e14702ff1aff3bacfb8485b742086b08ff9d01cadd82d9f8327e6ac887fcc`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 01:43:57 GMT
ADD file:1c7f60f778e4b93490d570487d56275925e5eb477632e71cb9f035ce6edf2460 in / 
# Thu, 16 Apr 2020 01:44:03 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 06:37:42 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 16 Apr 2020 06:39:43 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Apr 2020 06:41:27 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 16 Apr 2020 06:58:08 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:15e508b90ba1d327da83b72fc494ca263c1566ef6f70b91001cf2093395ffa3d`  
		Last Modified: Thu, 16 Apr 2020 02:04:33 GMT  
		Size: 22.8 MB (22785425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1629fdf02d54d31ae3023cd8b4a515c3c17a085c6135c7a10e412896d06a1f62`  
		Last Modified: Thu, 16 Apr 2020 07:18:38 GMT  
		Size: 244.7 KB (244669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fc63fa4246f2b9b66f762d8c33434e375c088c1ca73c3a389a8fb2525f93c7c`  
		Last Modified: Thu, 16 Apr 2020 07:18:43 GMT  
		Size: 25.8 MB (25775805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90ed038a48cf0007c67072a64fc2d4d1d4efd20b275bff6a15884fcfe67b0afa`  
		Last Modified: Thu, 16 Apr 2020 07:20:07 GMT  
		Size: 130.2 MB (130191844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.8.0.96`

```console
$ docker pull mono@sha256:8b4551b8332e7efec0aa7c0fed4f53a7cf6bed12cbee05f6858ffb65a79aa5cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:6.8.0.96` - linux; amd64

```console
$ docker pull mono@sha256:3d109ece622c61e26832ecee8eafdafa2e72535b9c74d735d879ca179b1a13b8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.1 MB (235135830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51f7ccdd96f0dfed7dc0f8f3af746f9edb7e71a7f93e19af1ea4b9bccb53d336`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 03:27:50 GMT
ADD file:40f52c233aecabf572a9db7450590d54d5e125fb00ecbb4a26fecd0b71e84eb8 in / 
# Thu, 16 Apr 2020 03:27:50 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 09:11:48 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 16 Apr 2020 09:12:00 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Apr 2020 09:12:35 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 16 Apr 2020 09:25:34 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:5e35bd43cf7898d036f8515be74d45b2e3abd2a5534fc280de63a9c22dd175bd`  
		Last Modified: Thu, 16 Apr 2020 03:35:04 GMT  
		Size: 22.5 MB (22513476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79f990050ea7755c8b4310123b2d720a7fede3eaa9cf5a76acb2a5fbd0af58d5`  
		Last Modified: Thu, 16 Apr 2020 09:46:33 GMT  
		Size: 244.5 KB (244519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b463238d61e87361acee422c7ed4ee873ebc66a2a7b4dde702ca6956a532ecf`  
		Last Modified: Thu, 16 Apr 2020 09:46:52 GMT  
		Size: 64.6 MB (64584108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04da7d857cd9fd3a2c4f7e602c9a50f2993fd66e67372efe5765e3b227eb1e73`  
		Last Modified: Thu, 16 Apr 2020 09:48:16 GMT  
		Size: 147.8 MB (147793727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8.0.96` - linux; arm variant v5

```console
$ docker pull mono@sha256:039a6be7bba94963928fb63f0cd7624bdcc24ff437d3511659983bf8a15da61c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.7 MB (176695282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbb0da5905f2877688de5793cf7d5f0c6b5cdbb737868e678439fec995215cfa`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 00:54:51 GMT
ADD file:ba6c5e03457e69f59231e8e7c6465c1ec985812f0d8f7a65d9842f2be3e947fb in / 
# Thu, 16 Apr 2020 00:54:54 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 03:22:05 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 16 Apr 2020 03:22:36 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Apr 2020 03:23:29 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 16 Apr 2020 03:29:10 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:b7d527e4baf13a6c926fb354fe1b38cb42b96f249ae65fdc0f52c853b654e06e`  
		Last Modified: Thu, 16 Apr 2020 01:02:32 GMT  
		Size: 21.2 MB (21190797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5251e801555d8cd1370a8d39ca953a0fb8f39729ff494b4a60bd03b4255c45be`  
		Last Modified: Thu, 16 Apr 2020 03:36:12 GMT  
		Size: 244.6 KB (244555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7c9b96b75ebb7a3cac23cf75e27179b71b5aa2cee0c40c33aca6399e29516f2`  
		Last Modified: Thu, 16 Apr 2020 03:36:22 GMT  
		Size: 25.4 MB (25367763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c33b43ad8da6addb8c852a68a9848cba5f48be98873fc8db208731eb55f31b9b`  
		Last Modified: Thu, 16 Apr 2020 03:37:53 GMT  
		Size: 129.9 MB (129892167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8.0.96` - linux; arm variant v7

```console
$ docker pull mono@sha256:09076495aacfba71beb6f4e5812d597a2d059b58d0d1a053068e4fa0fdec8443
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.7 MB (172708239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6e489c47305d9f8c107b00d2a1e335c874014e8fa4a3fc5ecb9082df7c5be0f`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 01:05:08 GMT
ADD file:e37c4728c0c89ac126542ac35e7e493425c021bfac751079c9b266821a1b4e99 in / 
# Thu, 16 Apr 2020 01:05:10 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 04:40:35 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 16 Apr 2020 04:40:56 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Apr 2020 04:41:45 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 16 Apr 2020 04:47:13 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:f78d9963dfddc4747d6200353b50f6093a6e37ca82e1612fa397d64ff13e7299`  
		Last Modified: Thu, 16 Apr 2020 01:12:33 GMT  
		Size: 19.3 MB (19298546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70114347da279136ebd21697ef769dc5764f716c6f7331568bbf7306c17da63c`  
		Last Modified: Thu, 16 Apr 2020 04:54:02 GMT  
		Size: 244.6 KB (244551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:802f26edffea7b59f9cc74e47561799e0c847d999b0db0dd2d99497c42af3511`  
		Last Modified: Thu, 16 Apr 2020 04:54:10 GMT  
		Size: 24.6 MB (24608740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62a9fd3d7648204f077b0034260c1887fe3c12c26ffadbb4223d8dc7ff65c1eb`  
		Last Modified: Thu, 16 Apr 2020 04:55:42 GMT  
		Size: 128.6 MB (128556402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8.0.96` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:abe9ae9da3ff9d1c710471ec6a5c1b39b18e33e11b0abba7d4245a3e75b11dc0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.7 MB (194747450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5a96031ff7018d8a3f1e18642728c41f24ad314d26c4fc40907ef19fce71fcd`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 02:45:19 GMT
ADD file:1588320d1c43714ec0353b7471f2ffd649045ca0f5f70dcb1eb064875fff9578 in / 
# Thu, 16 Apr 2020 02:45:21 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 06:47:03 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 16 Apr 2020 06:47:21 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Apr 2020 06:48:05 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 16 Apr 2020 06:53:15 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:8978c87ff45d64d1663a585dcf1ed66d9e711c2e4048d83ef561da9514ef46e6`  
		Last Modified: Thu, 16 Apr 2020 02:51:32 GMT  
		Size: 20.4 MB (20370106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:090b996e11040b9a724d4b94b5f6fea43f5cee5558fdcdcb2e4627d1c596f82c`  
		Last Modified: Thu, 16 Apr 2020 06:59:20 GMT  
		Size: 244.4 KB (244369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be77ae0e8a98b883233d159b79364894a76d49f1b02badb9f57b227a26a8e1a`  
		Last Modified: Thu, 16 Apr 2020 06:59:30 GMT  
		Size: 29.4 MB (29420188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1774c3e17e0d83d02e086998900775da6efe1356459c585e7d5800434b5aaf21`  
		Last Modified: Thu, 16 Apr 2020 07:01:03 GMT  
		Size: 144.7 MB (144712787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8.0.96` - linux; 386

```console
$ docker pull mono@sha256:9c689075bb69bade3f528bb36bfe204fd3529387d13addcfe9d2c43db444d7a4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.5 MB (243509400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1505bc590d4dce8f057579c70b93a89b4ce6d044fd5f80a06eb1765872b2e2b1`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:42:13 GMT
ADD file:82f76d577eec142f824456d027e5f82f681c9f5a09aeef4f711cef4662dcaea4 in / 
# Thu, 23 Apr 2020 00:42:13 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:04:12 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 23 Apr 2020 01:04:23 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 01:05:02 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Apr 2020 01:09:10 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7cb0551c4675347b94a8c63d7ee1f99dea4ab34aa7f23602ca587b6894d0211b`  
		Last Modified: Thu, 23 Apr 2020 00:47:39 GMT  
		Size: 23.1 MB (23141423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa3b9d440d2c40f2a9f3756fc7f8347bb9ec214b84fa396a388bd94782e1a678`  
		Last Modified: Thu, 23 Apr 2020 01:14:10 GMT  
		Size: 244.5 KB (244496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de2b74896e741d2269bb5084cfdbe6af6d2fc8d9d0ed1fc3f055d7c644afad5d`  
		Last Modified: Thu, 23 Apr 2020 01:14:29 GMT  
		Size: 68.6 MB (68630969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:753f8d38ff41ce32cf902046d0c45ed81a3a5475418bddade545b50a630ae181`  
		Last Modified: Thu, 23 Apr 2020 01:16:08 GMT  
		Size: 151.5 MB (151492512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8.0.96` - linux; ppc64le

```console
$ docker pull mono@sha256:0434d01a8617e75170a4dd8a638d786d1e67ac13c9fc880e023ccd0950428e36
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.0 MB (178997743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b5e14702ff1aff3bacfb8485b742086b08ff9d01cadd82d9f8327e6ac887fcc`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 01:43:57 GMT
ADD file:1c7f60f778e4b93490d570487d56275925e5eb477632e71cb9f035ce6edf2460 in / 
# Thu, 16 Apr 2020 01:44:03 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 06:37:42 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 16 Apr 2020 06:39:43 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Apr 2020 06:41:27 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 16 Apr 2020 06:58:08 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:15e508b90ba1d327da83b72fc494ca263c1566ef6f70b91001cf2093395ffa3d`  
		Last Modified: Thu, 16 Apr 2020 02:04:33 GMT  
		Size: 22.8 MB (22785425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1629fdf02d54d31ae3023cd8b4a515c3c17a085c6135c7a10e412896d06a1f62`  
		Last Modified: Thu, 16 Apr 2020 07:18:38 GMT  
		Size: 244.7 KB (244669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fc63fa4246f2b9b66f762d8c33434e375c088c1ca73c3a389a8fb2525f93c7c`  
		Last Modified: Thu, 16 Apr 2020 07:18:43 GMT  
		Size: 25.8 MB (25775805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90ed038a48cf0007c67072a64fc2d4d1d4efd20b275bff6a15884fcfe67b0afa`  
		Last Modified: Thu, 16 Apr 2020 07:20:07 GMT  
		Size: 130.2 MB (130191844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.8.0.96-slim`

```console
$ docker pull mono@sha256:27926c2c4a63765cb2fa66d25e6836c91f1d26dd544da3af02ea309bc3cb1496
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:6.8.0.96-slim` - linux; amd64

```console
$ docker pull mono@sha256:56079cf2e66e1c99c7df99a94af6e878735015befb38696382d11558f8691cb1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.3 MB (87342103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37a90f53167c056eec1636d8eeacce331e20daf9aad0b15a9b40df3706ef58d0`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 03:27:50 GMT
ADD file:40f52c233aecabf572a9db7450590d54d5e125fb00ecbb4a26fecd0b71e84eb8 in / 
# Thu, 16 Apr 2020 03:27:50 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 09:11:48 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 16 Apr 2020 09:12:00 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Apr 2020 09:12:35 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:5e35bd43cf7898d036f8515be74d45b2e3abd2a5534fc280de63a9c22dd175bd`  
		Last Modified: Thu, 16 Apr 2020 03:35:04 GMT  
		Size: 22.5 MB (22513476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79f990050ea7755c8b4310123b2d720a7fede3eaa9cf5a76acb2a5fbd0af58d5`  
		Last Modified: Thu, 16 Apr 2020 09:46:33 GMT  
		Size: 244.5 KB (244519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b463238d61e87361acee422c7ed4ee873ebc66a2a7b4dde702ca6956a532ecf`  
		Last Modified: Thu, 16 Apr 2020 09:46:52 GMT  
		Size: 64.6 MB (64584108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8.0.96-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:988781ce7fd3739dba6c395332912434cb391801f362378ff13316fdc0c50a3b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46803115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8e01bfb2e90fa41fdda2d35621f00b8a0d51e600f008dd4e4518771218af14c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 00:54:51 GMT
ADD file:ba6c5e03457e69f59231e8e7c6465c1ec985812f0d8f7a65d9842f2be3e947fb in / 
# Thu, 16 Apr 2020 00:54:54 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 03:22:05 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 16 Apr 2020 03:22:36 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Apr 2020 03:23:29 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:b7d527e4baf13a6c926fb354fe1b38cb42b96f249ae65fdc0f52c853b654e06e`  
		Last Modified: Thu, 16 Apr 2020 01:02:32 GMT  
		Size: 21.2 MB (21190797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5251e801555d8cd1370a8d39ca953a0fb8f39729ff494b4a60bd03b4255c45be`  
		Last Modified: Thu, 16 Apr 2020 03:36:12 GMT  
		Size: 244.6 KB (244555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7c9b96b75ebb7a3cac23cf75e27179b71b5aa2cee0c40c33aca6399e29516f2`  
		Last Modified: Thu, 16 Apr 2020 03:36:22 GMT  
		Size: 25.4 MB (25367763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8.0.96-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:fec0e4861eab05dd7c3eb364beefae8f8d5fc2ef225162e038b210af4cb3d508
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44151837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b78272cf77806b892fb8ce1da5a728ff7eaee3e059bb9ed6a77bd80478f1be7`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 01:05:08 GMT
ADD file:e37c4728c0c89ac126542ac35e7e493425c021bfac751079c9b266821a1b4e99 in / 
# Thu, 16 Apr 2020 01:05:10 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 04:40:35 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 16 Apr 2020 04:40:56 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Apr 2020 04:41:45 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:f78d9963dfddc4747d6200353b50f6093a6e37ca82e1612fa397d64ff13e7299`  
		Last Modified: Thu, 16 Apr 2020 01:12:33 GMT  
		Size: 19.3 MB (19298546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70114347da279136ebd21697ef769dc5764f716c6f7331568bbf7306c17da63c`  
		Last Modified: Thu, 16 Apr 2020 04:54:02 GMT  
		Size: 244.6 KB (244551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:802f26edffea7b59f9cc74e47561799e0c847d999b0db0dd2d99497c42af3511`  
		Last Modified: Thu, 16 Apr 2020 04:54:10 GMT  
		Size: 24.6 MB (24608740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8.0.96-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:d08953373b3ef1fc7db79f7f13d8698af415ccec4a187b24ccd2e20c729b8c7d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (50034663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4c3ba9afd0517a25a4e83d0efc8b8d5d84880dbcc969fd912d6ce0463995374`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 02:45:19 GMT
ADD file:1588320d1c43714ec0353b7471f2ffd649045ca0f5f70dcb1eb064875fff9578 in / 
# Thu, 16 Apr 2020 02:45:21 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 06:47:03 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 16 Apr 2020 06:47:21 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Apr 2020 06:48:05 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:8978c87ff45d64d1663a585dcf1ed66d9e711c2e4048d83ef561da9514ef46e6`  
		Last Modified: Thu, 16 Apr 2020 02:51:32 GMT  
		Size: 20.4 MB (20370106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:090b996e11040b9a724d4b94b5f6fea43f5cee5558fdcdcb2e4627d1c596f82c`  
		Last Modified: Thu, 16 Apr 2020 06:59:20 GMT  
		Size: 244.4 KB (244369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be77ae0e8a98b883233d159b79364894a76d49f1b02badb9f57b227a26a8e1a`  
		Last Modified: Thu, 16 Apr 2020 06:59:30 GMT  
		Size: 29.4 MB (29420188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8.0.96-slim` - linux; 386

```console
$ docker pull mono@sha256:992d47fb588cd80517b999abe4626317c65dcfd5eb0dea3bea6b02cdb56b5db5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.0 MB (92016888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f41612f812aa87758c87bf3cf7d3d08ab20128631db6c4454c68b94583387608`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:42:13 GMT
ADD file:82f76d577eec142f824456d027e5f82f681c9f5a09aeef4f711cef4662dcaea4 in / 
# Thu, 23 Apr 2020 00:42:13 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:04:12 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 23 Apr 2020 01:04:23 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 01:05:02 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7cb0551c4675347b94a8c63d7ee1f99dea4ab34aa7f23602ca587b6894d0211b`  
		Last Modified: Thu, 23 Apr 2020 00:47:39 GMT  
		Size: 23.1 MB (23141423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa3b9d440d2c40f2a9f3756fc7f8347bb9ec214b84fa396a388bd94782e1a678`  
		Last Modified: Thu, 23 Apr 2020 01:14:10 GMT  
		Size: 244.5 KB (244496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de2b74896e741d2269bb5084cfdbe6af6d2fc8d9d0ed1fc3f055d7c644afad5d`  
		Last Modified: Thu, 23 Apr 2020 01:14:29 GMT  
		Size: 68.6 MB (68630969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8.0.96-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:fa72fc4c116a54fd72fa979ab6db10a3798c1a0719a1b40884ceabbb476291c2
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48805899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccafa8bda50e8b6b041a02bca8290435a0dac26f6b7f52a0f59d6d21222413f1`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 01:43:57 GMT
ADD file:1c7f60f778e4b93490d570487d56275925e5eb477632e71cb9f035ce6edf2460 in / 
# Thu, 16 Apr 2020 01:44:03 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 06:37:42 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 16 Apr 2020 06:39:43 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Apr 2020 06:41:27 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:15e508b90ba1d327da83b72fc494ca263c1566ef6f70b91001cf2093395ffa3d`  
		Last Modified: Thu, 16 Apr 2020 02:04:33 GMT  
		Size: 22.8 MB (22785425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1629fdf02d54d31ae3023cd8b4a515c3c17a085c6135c7a10e412896d06a1f62`  
		Last Modified: Thu, 16 Apr 2020 07:18:38 GMT  
		Size: 244.7 KB (244669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fc63fa4246f2b9b66f762d8c33434e375c088c1ca73c3a389a8fb2525f93c7c`  
		Last Modified: Thu, 16 Apr 2020 07:18:43 GMT  
		Size: 25.8 MB (25775805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.8.0-slim`

```console
$ docker pull mono@sha256:27926c2c4a63765cb2fa66d25e6836c91f1d26dd544da3af02ea309bc3cb1496
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
$ docker pull mono@sha256:56079cf2e66e1c99c7df99a94af6e878735015befb38696382d11558f8691cb1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.3 MB (87342103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37a90f53167c056eec1636d8eeacce331e20daf9aad0b15a9b40df3706ef58d0`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 03:27:50 GMT
ADD file:40f52c233aecabf572a9db7450590d54d5e125fb00ecbb4a26fecd0b71e84eb8 in / 
# Thu, 16 Apr 2020 03:27:50 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 09:11:48 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 16 Apr 2020 09:12:00 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Apr 2020 09:12:35 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:5e35bd43cf7898d036f8515be74d45b2e3abd2a5534fc280de63a9c22dd175bd`  
		Last Modified: Thu, 16 Apr 2020 03:35:04 GMT  
		Size: 22.5 MB (22513476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79f990050ea7755c8b4310123b2d720a7fede3eaa9cf5a76acb2a5fbd0af58d5`  
		Last Modified: Thu, 16 Apr 2020 09:46:33 GMT  
		Size: 244.5 KB (244519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b463238d61e87361acee422c7ed4ee873ebc66a2a7b4dde702ca6956a532ecf`  
		Last Modified: Thu, 16 Apr 2020 09:46:52 GMT  
		Size: 64.6 MB (64584108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8.0-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:988781ce7fd3739dba6c395332912434cb391801f362378ff13316fdc0c50a3b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46803115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8e01bfb2e90fa41fdda2d35621f00b8a0d51e600f008dd4e4518771218af14c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 00:54:51 GMT
ADD file:ba6c5e03457e69f59231e8e7c6465c1ec985812f0d8f7a65d9842f2be3e947fb in / 
# Thu, 16 Apr 2020 00:54:54 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 03:22:05 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 16 Apr 2020 03:22:36 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Apr 2020 03:23:29 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:b7d527e4baf13a6c926fb354fe1b38cb42b96f249ae65fdc0f52c853b654e06e`  
		Last Modified: Thu, 16 Apr 2020 01:02:32 GMT  
		Size: 21.2 MB (21190797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5251e801555d8cd1370a8d39ca953a0fb8f39729ff494b4a60bd03b4255c45be`  
		Last Modified: Thu, 16 Apr 2020 03:36:12 GMT  
		Size: 244.6 KB (244555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7c9b96b75ebb7a3cac23cf75e27179b71b5aa2cee0c40c33aca6399e29516f2`  
		Last Modified: Thu, 16 Apr 2020 03:36:22 GMT  
		Size: 25.4 MB (25367763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8.0-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:fec0e4861eab05dd7c3eb364beefae8f8d5fc2ef225162e038b210af4cb3d508
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44151837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b78272cf77806b892fb8ce1da5a728ff7eaee3e059bb9ed6a77bd80478f1be7`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 01:05:08 GMT
ADD file:e37c4728c0c89ac126542ac35e7e493425c021bfac751079c9b266821a1b4e99 in / 
# Thu, 16 Apr 2020 01:05:10 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 04:40:35 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 16 Apr 2020 04:40:56 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Apr 2020 04:41:45 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:f78d9963dfddc4747d6200353b50f6093a6e37ca82e1612fa397d64ff13e7299`  
		Last Modified: Thu, 16 Apr 2020 01:12:33 GMT  
		Size: 19.3 MB (19298546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70114347da279136ebd21697ef769dc5764f716c6f7331568bbf7306c17da63c`  
		Last Modified: Thu, 16 Apr 2020 04:54:02 GMT  
		Size: 244.6 KB (244551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:802f26edffea7b59f9cc74e47561799e0c847d999b0db0dd2d99497c42af3511`  
		Last Modified: Thu, 16 Apr 2020 04:54:10 GMT  
		Size: 24.6 MB (24608740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8.0-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:d08953373b3ef1fc7db79f7f13d8698af415ccec4a187b24ccd2e20c729b8c7d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (50034663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4c3ba9afd0517a25a4e83d0efc8b8d5d84880dbcc969fd912d6ce0463995374`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 02:45:19 GMT
ADD file:1588320d1c43714ec0353b7471f2ffd649045ca0f5f70dcb1eb064875fff9578 in / 
# Thu, 16 Apr 2020 02:45:21 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 06:47:03 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 16 Apr 2020 06:47:21 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Apr 2020 06:48:05 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:8978c87ff45d64d1663a585dcf1ed66d9e711c2e4048d83ef561da9514ef46e6`  
		Last Modified: Thu, 16 Apr 2020 02:51:32 GMT  
		Size: 20.4 MB (20370106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:090b996e11040b9a724d4b94b5f6fea43f5cee5558fdcdcb2e4627d1c596f82c`  
		Last Modified: Thu, 16 Apr 2020 06:59:20 GMT  
		Size: 244.4 KB (244369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be77ae0e8a98b883233d159b79364894a76d49f1b02badb9f57b227a26a8e1a`  
		Last Modified: Thu, 16 Apr 2020 06:59:30 GMT  
		Size: 29.4 MB (29420188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8.0-slim` - linux; 386

```console
$ docker pull mono@sha256:992d47fb588cd80517b999abe4626317c65dcfd5eb0dea3bea6b02cdb56b5db5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.0 MB (92016888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f41612f812aa87758c87bf3cf7d3d08ab20128631db6c4454c68b94583387608`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:42:13 GMT
ADD file:82f76d577eec142f824456d027e5f82f681c9f5a09aeef4f711cef4662dcaea4 in / 
# Thu, 23 Apr 2020 00:42:13 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:04:12 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 23 Apr 2020 01:04:23 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 01:05:02 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7cb0551c4675347b94a8c63d7ee1f99dea4ab34aa7f23602ca587b6894d0211b`  
		Last Modified: Thu, 23 Apr 2020 00:47:39 GMT  
		Size: 23.1 MB (23141423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa3b9d440d2c40f2a9f3756fc7f8347bb9ec214b84fa396a388bd94782e1a678`  
		Last Modified: Thu, 23 Apr 2020 01:14:10 GMT  
		Size: 244.5 KB (244496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de2b74896e741d2269bb5084cfdbe6af6d2fc8d9d0ed1fc3f055d7c644afad5d`  
		Last Modified: Thu, 23 Apr 2020 01:14:29 GMT  
		Size: 68.6 MB (68630969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8.0-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:fa72fc4c116a54fd72fa979ab6db10a3798c1a0719a1b40884ceabbb476291c2
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48805899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccafa8bda50e8b6b041a02bca8290435a0dac26f6b7f52a0f59d6d21222413f1`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 01:43:57 GMT
ADD file:1c7f60f778e4b93490d570487d56275925e5eb477632e71cb9f035ce6edf2460 in / 
# Thu, 16 Apr 2020 01:44:03 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 06:37:42 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 16 Apr 2020 06:39:43 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Apr 2020 06:41:27 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:15e508b90ba1d327da83b72fc494ca263c1566ef6f70b91001cf2093395ffa3d`  
		Last Modified: Thu, 16 Apr 2020 02:04:33 GMT  
		Size: 22.8 MB (22785425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1629fdf02d54d31ae3023cd8b4a515c3c17a085c6135c7a10e412896d06a1f62`  
		Last Modified: Thu, 16 Apr 2020 07:18:38 GMT  
		Size: 244.7 KB (244669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fc63fa4246f2b9b66f762d8c33434e375c088c1ca73c3a389a8fb2525f93c7c`  
		Last Modified: Thu, 16 Apr 2020 07:18:43 GMT  
		Size: 25.8 MB (25775805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.8-slim`

```console
$ docker pull mono@sha256:27926c2c4a63765cb2fa66d25e6836c91f1d26dd544da3af02ea309bc3cb1496
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
$ docker pull mono@sha256:56079cf2e66e1c99c7df99a94af6e878735015befb38696382d11558f8691cb1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.3 MB (87342103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37a90f53167c056eec1636d8eeacce331e20daf9aad0b15a9b40df3706ef58d0`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 03:27:50 GMT
ADD file:40f52c233aecabf572a9db7450590d54d5e125fb00ecbb4a26fecd0b71e84eb8 in / 
# Thu, 16 Apr 2020 03:27:50 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 09:11:48 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 16 Apr 2020 09:12:00 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Apr 2020 09:12:35 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:5e35bd43cf7898d036f8515be74d45b2e3abd2a5534fc280de63a9c22dd175bd`  
		Last Modified: Thu, 16 Apr 2020 03:35:04 GMT  
		Size: 22.5 MB (22513476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79f990050ea7755c8b4310123b2d720a7fede3eaa9cf5a76acb2a5fbd0af58d5`  
		Last Modified: Thu, 16 Apr 2020 09:46:33 GMT  
		Size: 244.5 KB (244519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b463238d61e87361acee422c7ed4ee873ebc66a2a7b4dde702ca6956a532ecf`  
		Last Modified: Thu, 16 Apr 2020 09:46:52 GMT  
		Size: 64.6 MB (64584108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:988781ce7fd3739dba6c395332912434cb391801f362378ff13316fdc0c50a3b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46803115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8e01bfb2e90fa41fdda2d35621f00b8a0d51e600f008dd4e4518771218af14c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 00:54:51 GMT
ADD file:ba6c5e03457e69f59231e8e7c6465c1ec985812f0d8f7a65d9842f2be3e947fb in / 
# Thu, 16 Apr 2020 00:54:54 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 03:22:05 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 16 Apr 2020 03:22:36 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Apr 2020 03:23:29 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:b7d527e4baf13a6c926fb354fe1b38cb42b96f249ae65fdc0f52c853b654e06e`  
		Last Modified: Thu, 16 Apr 2020 01:02:32 GMT  
		Size: 21.2 MB (21190797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5251e801555d8cd1370a8d39ca953a0fb8f39729ff494b4a60bd03b4255c45be`  
		Last Modified: Thu, 16 Apr 2020 03:36:12 GMT  
		Size: 244.6 KB (244555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7c9b96b75ebb7a3cac23cf75e27179b71b5aa2cee0c40c33aca6399e29516f2`  
		Last Modified: Thu, 16 Apr 2020 03:36:22 GMT  
		Size: 25.4 MB (25367763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:fec0e4861eab05dd7c3eb364beefae8f8d5fc2ef225162e038b210af4cb3d508
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44151837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b78272cf77806b892fb8ce1da5a728ff7eaee3e059bb9ed6a77bd80478f1be7`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 01:05:08 GMT
ADD file:e37c4728c0c89ac126542ac35e7e493425c021bfac751079c9b266821a1b4e99 in / 
# Thu, 16 Apr 2020 01:05:10 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 04:40:35 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 16 Apr 2020 04:40:56 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Apr 2020 04:41:45 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:f78d9963dfddc4747d6200353b50f6093a6e37ca82e1612fa397d64ff13e7299`  
		Last Modified: Thu, 16 Apr 2020 01:12:33 GMT  
		Size: 19.3 MB (19298546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70114347da279136ebd21697ef769dc5764f716c6f7331568bbf7306c17da63c`  
		Last Modified: Thu, 16 Apr 2020 04:54:02 GMT  
		Size: 244.6 KB (244551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:802f26edffea7b59f9cc74e47561799e0c847d999b0db0dd2d99497c42af3511`  
		Last Modified: Thu, 16 Apr 2020 04:54:10 GMT  
		Size: 24.6 MB (24608740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:d08953373b3ef1fc7db79f7f13d8698af415ccec4a187b24ccd2e20c729b8c7d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (50034663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4c3ba9afd0517a25a4e83d0efc8b8d5d84880dbcc969fd912d6ce0463995374`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 02:45:19 GMT
ADD file:1588320d1c43714ec0353b7471f2ffd649045ca0f5f70dcb1eb064875fff9578 in / 
# Thu, 16 Apr 2020 02:45:21 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 06:47:03 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 16 Apr 2020 06:47:21 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Apr 2020 06:48:05 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:8978c87ff45d64d1663a585dcf1ed66d9e711c2e4048d83ef561da9514ef46e6`  
		Last Modified: Thu, 16 Apr 2020 02:51:32 GMT  
		Size: 20.4 MB (20370106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:090b996e11040b9a724d4b94b5f6fea43f5cee5558fdcdcb2e4627d1c596f82c`  
		Last Modified: Thu, 16 Apr 2020 06:59:20 GMT  
		Size: 244.4 KB (244369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be77ae0e8a98b883233d159b79364894a76d49f1b02badb9f57b227a26a8e1a`  
		Last Modified: Thu, 16 Apr 2020 06:59:30 GMT  
		Size: 29.4 MB (29420188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8-slim` - linux; 386

```console
$ docker pull mono@sha256:992d47fb588cd80517b999abe4626317c65dcfd5eb0dea3bea6b02cdb56b5db5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.0 MB (92016888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f41612f812aa87758c87bf3cf7d3d08ab20128631db6c4454c68b94583387608`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:42:13 GMT
ADD file:82f76d577eec142f824456d027e5f82f681c9f5a09aeef4f711cef4662dcaea4 in / 
# Thu, 23 Apr 2020 00:42:13 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:04:12 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 23 Apr 2020 01:04:23 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 01:05:02 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7cb0551c4675347b94a8c63d7ee1f99dea4ab34aa7f23602ca587b6894d0211b`  
		Last Modified: Thu, 23 Apr 2020 00:47:39 GMT  
		Size: 23.1 MB (23141423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa3b9d440d2c40f2a9f3756fc7f8347bb9ec214b84fa396a388bd94782e1a678`  
		Last Modified: Thu, 23 Apr 2020 01:14:10 GMT  
		Size: 244.5 KB (244496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de2b74896e741d2269bb5084cfdbe6af6d2fc8d9d0ed1fc3f055d7c644afad5d`  
		Last Modified: Thu, 23 Apr 2020 01:14:29 GMT  
		Size: 68.6 MB (68630969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:fa72fc4c116a54fd72fa979ab6db10a3798c1a0719a1b40884ceabbb476291c2
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48805899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccafa8bda50e8b6b041a02bca8290435a0dac26f6b7f52a0f59d6d21222413f1`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 01:43:57 GMT
ADD file:1c7f60f778e4b93490d570487d56275925e5eb477632e71cb9f035ce6edf2460 in / 
# Thu, 16 Apr 2020 01:44:03 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 06:37:42 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 16 Apr 2020 06:39:43 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Apr 2020 06:41:27 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:15e508b90ba1d327da83b72fc494ca263c1566ef6f70b91001cf2093395ffa3d`  
		Last Modified: Thu, 16 Apr 2020 02:04:33 GMT  
		Size: 22.8 MB (22785425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1629fdf02d54d31ae3023cd8b4a515c3c17a085c6135c7a10e412896d06a1f62`  
		Last Modified: Thu, 16 Apr 2020 07:18:38 GMT  
		Size: 244.7 KB (244669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fc63fa4246f2b9b66f762d8c33434e375c088c1ca73c3a389a8fb2525f93c7c`  
		Last Modified: Thu, 16 Apr 2020 07:18:43 GMT  
		Size: 25.8 MB (25775805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6-slim`

```console
$ docker pull mono@sha256:27926c2c4a63765cb2fa66d25e6836c91f1d26dd544da3af02ea309bc3cb1496
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
$ docker pull mono@sha256:56079cf2e66e1c99c7df99a94af6e878735015befb38696382d11558f8691cb1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.3 MB (87342103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37a90f53167c056eec1636d8eeacce331e20daf9aad0b15a9b40df3706ef58d0`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 03:27:50 GMT
ADD file:40f52c233aecabf572a9db7450590d54d5e125fb00ecbb4a26fecd0b71e84eb8 in / 
# Thu, 16 Apr 2020 03:27:50 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 09:11:48 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 16 Apr 2020 09:12:00 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Apr 2020 09:12:35 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:5e35bd43cf7898d036f8515be74d45b2e3abd2a5534fc280de63a9c22dd175bd`  
		Last Modified: Thu, 16 Apr 2020 03:35:04 GMT  
		Size: 22.5 MB (22513476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79f990050ea7755c8b4310123b2d720a7fede3eaa9cf5a76acb2a5fbd0af58d5`  
		Last Modified: Thu, 16 Apr 2020 09:46:33 GMT  
		Size: 244.5 KB (244519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b463238d61e87361acee422c7ed4ee873ebc66a2a7b4dde702ca6956a532ecf`  
		Last Modified: Thu, 16 Apr 2020 09:46:52 GMT  
		Size: 64.6 MB (64584108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:988781ce7fd3739dba6c395332912434cb391801f362378ff13316fdc0c50a3b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46803115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8e01bfb2e90fa41fdda2d35621f00b8a0d51e600f008dd4e4518771218af14c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 00:54:51 GMT
ADD file:ba6c5e03457e69f59231e8e7c6465c1ec985812f0d8f7a65d9842f2be3e947fb in / 
# Thu, 16 Apr 2020 00:54:54 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 03:22:05 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 16 Apr 2020 03:22:36 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Apr 2020 03:23:29 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:b7d527e4baf13a6c926fb354fe1b38cb42b96f249ae65fdc0f52c853b654e06e`  
		Last Modified: Thu, 16 Apr 2020 01:02:32 GMT  
		Size: 21.2 MB (21190797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5251e801555d8cd1370a8d39ca953a0fb8f39729ff494b4a60bd03b4255c45be`  
		Last Modified: Thu, 16 Apr 2020 03:36:12 GMT  
		Size: 244.6 KB (244555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7c9b96b75ebb7a3cac23cf75e27179b71b5aa2cee0c40c33aca6399e29516f2`  
		Last Modified: Thu, 16 Apr 2020 03:36:22 GMT  
		Size: 25.4 MB (25367763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:fec0e4861eab05dd7c3eb364beefae8f8d5fc2ef225162e038b210af4cb3d508
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44151837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b78272cf77806b892fb8ce1da5a728ff7eaee3e059bb9ed6a77bd80478f1be7`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 01:05:08 GMT
ADD file:e37c4728c0c89ac126542ac35e7e493425c021bfac751079c9b266821a1b4e99 in / 
# Thu, 16 Apr 2020 01:05:10 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 04:40:35 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 16 Apr 2020 04:40:56 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Apr 2020 04:41:45 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:f78d9963dfddc4747d6200353b50f6093a6e37ca82e1612fa397d64ff13e7299`  
		Last Modified: Thu, 16 Apr 2020 01:12:33 GMT  
		Size: 19.3 MB (19298546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70114347da279136ebd21697ef769dc5764f716c6f7331568bbf7306c17da63c`  
		Last Modified: Thu, 16 Apr 2020 04:54:02 GMT  
		Size: 244.6 KB (244551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:802f26edffea7b59f9cc74e47561799e0c847d999b0db0dd2d99497c42af3511`  
		Last Modified: Thu, 16 Apr 2020 04:54:10 GMT  
		Size: 24.6 MB (24608740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:d08953373b3ef1fc7db79f7f13d8698af415ccec4a187b24ccd2e20c729b8c7d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (50034663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4c3ba9afd0517a25a4e83d0efc8b8d5d84880dbcc969fd912d6ce0463995374`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 02:45:19 GMT
ADD file:1588320d1c43714ec0353b7471f2ffd649045ca0f5f70dcb1eb064875fff9578 in / 
# Thu, 16 Apr 2020 02:45:21 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 06:47:03 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 16 Apr 2020 06:47:21 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Apr 2020 06:48:05 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:8978c87ff45d64d1663a585dcf1ed66d9e711c2e4048d83ef561da9514ef46e6`  
		Last Modified: Thu, 16 Apr 2020 02:51:32 GMT  
		Size: 20.4 MB (20370106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:090b996e11040b9a724d4b94b5f6fea43f5cee5558fdcdcb2e4627d1c596f82c`  
		Last Modified: Thu, 16 Apr 2020 06:59:20 GMT  
		Size: 244.4 KB (244369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be77ae0e8a98b883233d159b79364894a76d49f1b02badb9f57b227a26a8e1a`  
		Last Modified: Thu, 16 Apr 2020 06:59:30 GMT  
		Size: 29.4 MB (29420188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6-slim` - linux; 386

```console
$ docker pull mono@sha256:992d47fb588cd80517b999abe4626317c65dcfd5eb0dea3bea6b02cdb56b5db5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.0 MB (92016888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f41612f812aa87758c87bf3cf7d3d08ab20128631db6c4454c68b94583387608`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:42:13 GMT
ADD file:82f76d577eec142f824456d027e5f82f681c9f5a09aeef4f711cef4662dcaea4 in / 
# Thu, 23 Apr 2020 00:42:13 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:04:12 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 23 Apr 2020 01:04:23 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 01:05:02 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7cb0551c4675347b94a8c63d7ee1f99dea4ab34aa7f23602ca587b6894d0211b`  
		Last Modified: Thu, 23 Apr 2020 00:47:39 GMT  
		Size: 23.1 MB (23141423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa3b9d440d2c40f2a9f3756fc7f8347bb9ec214b84fa396a388bd94782e1a678`  
		Last Modified: Thu, 23 Apr 2020 01:14:10 GMT  
		Size: 244.5 KB (244496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de2b74896e741d2269bb5084cfdbe6af6d2fc8d9d0ed1fc3f055d7c644afad5d`  
		Last Modified: Thu, 23 Apr 2020 01:14:29 GMT  
		Size: 68.6 MB (68630969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:fa72fc4c116a54fd72fa979ab6db10a3798c1a0719a1b40884ceabbb476291c2
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48805899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccafa8bda50e8b6b041a02bca8290435a0dac26f6b7f52a0f59d6d21222413f1`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 01:43:57 GMT
ADD file:1c7f60f778e4b93490d570487d56275925e5eb477632e71cb9f035ce6edf2460 in / 
# Thu, 16 Apr 2020 01:44:03 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 06:37:42 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 16 Apr 2020 06:39:43 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Apr 2020 06:41:27 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:15e508b90ba1d327da83b72fc494ca263c1566ef6f70b91001cf2093395ffa3d`  
		Last Modified: Thu, 16 Apr 2020 02:04:33 GMT  
		Size: 22.8 MB (22785425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1629fdf02d54d31ae3023cd8b4a515c3c17a085c6135c7a10e412896d06a1f62`  
		Last Modified: Thu, 16 Apr 2020 07:18:38 GMT  
		Size: 244.7 KB (244669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fc63fa4246f2b9b66f762d8c33434e375c088c1ca73c3a389a8fb2525f93c7c`  
		Last Modified: Thu, 16 Apr 2020 07:18:43 GMT  
		Size: 25.8 MB (25775805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:latest`

```console
$ docker pull mono@sha256:8b4551b8332e7efec0aa7c0fed4f53a7cf6bed12cbee05f6858ffb65a79aa5cd
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
$ docker pull mono@sha256:3d109ece622c61e26832ecee8eafdafa2e72535b9c74d735d879ca179b1a13b8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.1 MB (235135830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51f7ccdd96f0dfed7dc0f8f3af746f9edb7e71a7f93e19af1ea4b9bccb53d336`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 03:27:50 GMT
ADD file:40f52c233aecabf572a9db7450590d54d5e125fb00ecbb4a26fecd0b71e84eb8 in / 
# Thu, 16 Apr 2020 03:27:50 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 09:11:48 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 16 Apr 2020 09:12:00 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Apr 2020 09:12:35 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 16 Apr 2020 09:25:34 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:5e35bd43cf7898d036f8515be74d45b2e3abd2a5534fc280de63a9c22dd175bd`  
		Last Modified: Thu, 16 Apr 2020 03:35:04 GMT  
		Size: 22.5 MB (22513476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79f990050ea7755c8b4310123b2d720a7fede3eaa9cf5a76acb2a5fbd0af58d5`  
		Last Modified: Thu, 16 Apr 2020 09:46:33 GMT  
		Size: 244.5 KB (244519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b463238d61e87361acee422c7ed4ee873ebc66a2a7b4dde702ca6956a532ecf`  
		Last Modified: Thu, 16 Apr 2020 09:46:52 GMT  
		Size: 64.6 MB (64584108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04da7d857cd9fd3a2c4f7e602c9a50f2993fd66e67372efe5765e3b227eb1e73`  
		Last Modified: Thu, 16 Apr 2020 09:48:16 GMT  
		Size: 147.8 MB (147793727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:latest` - linux; arm variant v5

```console
$ docker pull mono@sha256:039a6be7bba94963928fb63f0cd7624bdcc24ff437d3511659983bf8a15da61c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.7 MB (176695282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbb0da5905f2877688de5793cf7d5f0c6b5cdbb737868e678439fec995215cfa`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 00:54:51 GMT
ADD file:ba6c5e03457e69f59231e8e7c6465c1ec985812f0d8f7a65d9842f2be3e947fb in / 
# Thu, 16 Apr 2020 00:54:54 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 03:22:05 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 16 Apr 2020 03:22:36 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Apr 2020 03:23:29 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 16 Apr 2020 03:29:10 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:b7d527e4baf13a6c926fb354fe1b38cb42b96f249ae65fdc0f52c853b654e06e`  
		Last Modified: Thu, 16 Apr 2020 01:02:32 GMT  
		Size: 21.2 MB (21190797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5251e801555d8cd1370a8d39ca953a0fb8f39729ff494b4a60bd03b4255c45be`  
		Last Modified: Thu, 16 Apr 2020 03:36:12 GMT  
		Size: 244.6 KB (244555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7c9b96b75ebb7a3cac23cf75e27179b71b5aa2cee0c40c33aca6399e29516f2`  
		Last Modified: Thu, 16 Apr 2020 03:36:22 GMT  
		Size: 25.4 MB (25367763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c33b43ad8da6addb8c852a68a9848cba5f48be98873fc8db208731eb55f31b9b`  
		Last Modified: Thu, 16 Apr 2020 03:37:53 GMT  
		Size: 129.9 MB (129892167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:latest` - linux; arm variant v7

```console
$ docker pull mono@sha256:09076495aacfba71beb6f4e5812d597a2d059b58d0d1a053068e4fa0fdec8443
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.7 MB (172708239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6e489c47305d9f8c107b00d2a1e335c874014e8fa4a3fc5ecb9082df7c5be0f`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 01:05:08 GMT
ADD file:e37c4728c0c89ac126542ac35e7e493425c021bfac751079c9b266821a1b4e99 in / 
# Thu, 16 Apr 2020 01:05:10 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 04:40:35 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 16 Apr 2020 04:40:56 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Apr 2020 04:41:45 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 16 Apr 2020 04:47:13 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:f78d9963dfddc4747d6200353b50f6093a6e37ca82e1612fa397d64ff13e7299`  
		Last Modified: Thu, 16 Apr 2020 01:12:33 GMT  
		Size: 19.3 MB (19298546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70114347da279136ebd21697ef769dc5764f716c6f7331568bbf7306c17da63c`  
		Last Modified: Thu, 16 Apr 2020 04:54:02 GMT  
		Size: 244.6 KB (244551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:802f26edffea7b59f9cc74e47561799e0c847d999b0db0dd2d99497c42af3511`  
		Last Modified: Thu, 16 Apr 2020 04:54:10 GMT  
		Size: 24.6 MB (24608740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62a9fd3d7648204f077b0034260c1887fe3c12c26ffadbb4223d8dc7ff65c1eb`  
		Last Modified: Thu, 16 Apr 2020 04:55:42 GMT  
		Size: 128.6 MB (128556402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:latest` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:abe9ae9da3ff9d1c710471ec6a5c1b39b18e33e11b0abba7d4245a3e75b11dc0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.7 MB (194747450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5a96031ff7018d8a3f1e18642728c41f24ad314d26c4fc40907ef19fce71fcd`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 02:45:19 GMT
ADD file:1588320d1c43714ec0353b7471f2ffd649045ca0f5f70dcb1eb064875fff9578 in / 
# Thu, 16 Apr 2020 02:45:21 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 06:47:03 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 16 Apr 2020 06:47:21 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Apr 2020 06:48:05 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 16 Apr 2020 06:53:15 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:8978c87ff45d64d1663a585dcf1ed66d9e711c2e4048d83ef561da9514ef46e6`  
		Last Modified: Thu, 16 Apr 2020 02:51:32 GMT  
		Size: 20.4 MB (20370106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:090b996e11040b9a724d4b94b5f6fea43f5cee5558fdcdcb2e4627d1c596f82c`  
		Last Modified: Thu, 16 Apr 2020 06:59:20 GMT  
		Size: 244.4 KB (244369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be77ae0e8a98b883233d159b79364894a76d49f1b02badb9f57b227a26a8e1a`  
		Last Modified: Thu, 16 Apr 2020 06:59:30 GMT  
		Size: 29.4 MB (29420188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1774c3e17e0d83d02e086998900775da6efe1356459c585e7d5800434b5aaf21`  
		Last Modified: Thu, 16 Apr 2020 07:01:03 GMT  
		Size: 144.7 MB (144712787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:latest` - linux; 386

```console
$ docker pull mono@sha256:9c689075bb69bade3f528bb36bfe204fd3529387d13addcfe9d2c43db444d7a4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.5 MB (243509400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1505bc590d4dce8f057579c70b93a89b4ce6d044fd5f80a06eb1765872b2e2b1`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:42:13 GMT
ADD file:82f76d577eec142f824456d027e5f82f681c9f5a09aeef4f711cef4662dcaea4 in / 
# Thu, 23 Apr 2020 00:42:13 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:04:12 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 23 Apr 2020 01:04:23 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 01:05:02 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Apr 2020 01:09:10 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7cb0551c4675347b94a8c63d7ee1f99dea4ab34aa7f23602ca587b6894d0211b`  
		Last Modified: Thu, 23 Apr 2020 00:47:39 GMT  
		Size: 23.1 MB (23141423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa3b9d440d2c40f2a9f3756fc7f8347bb9ec214b84fa396a388bd94782e1a678`  
		Last Modified: Thu, 23 Apr 2020 01:14:10 GMT  
		Size: 244.5 KB (244496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de2b74896e741d2269bb5084cfdbe6af6d2fc8d9d0ed1fc3f055d7c644afad5d`  
		Last Modified: Thu, 23 Apr 2020 01:14:29 GMT  
		Size: 68.6 MB (68630969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:753f8d38ff41ce32cf902046d0c45ed81a3a5475418bddade545b50a630ae181`  
		Last Modified: Thu, 23 Apr 2020 01:16:08 GMT  
		Size: 151.5 MB (151492512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:latest` - linux; ppc64le

```console
$ docker pull mono@sha256:0434d01a8617e75170a4dd8a638d786d1e67ac13c9fc880e023ccd0950428e36
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.0 MB (178997743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b5e14702ff1aff3bacfb8485b742086b08ff9d01cadd82d9f8327e6ac887fcc`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 01:43:57 GMT
ADD file:1c7f60f778e4b93490d570487d56275925e5eb477632e71cb9f035ce6edf2460 in / 
# Thu, 16 Apr 2020 01:44:03 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 06:37:42 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 16 Apr 2020 06:39:43 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Apr 2020 06:41:27 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 16 Apr 2020 06:58:08 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:15e508b90ba1d327da83b72fc494ca263c1566ef6f70b91001cf2093395ffa3d`  
		Last Modified: Thu, 16 Apr 2020 02:04:33 GMT  
		Size: 22.8 MB (22785425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1629fdf02d54d31ae3023cd8b4a515c3c17a085c6135c7a10e412896d06a1f62`  
		Last Modified: Thu, 16 Apr 2020 07:18:38 GMT  
		Size: 244.7 KB (244669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fc63fa4246f2b9b66f762d8c33434e375c088c1ca73c3a389a8fb2525f93c7c`  
		Last Modified: Thu, 16 Apr 2020 07:18:43 GMT  
		Size: 25.8 MB (25775805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90ed038a48cf0007c67072a64fc2d4d1d4efd20b275bff6a15884fcfe67b0afa`  
		Last Modified: Thu, 16 Apr 2020 07:20:07 GMT  
		Size: 130.2 MB (130191844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:slim`

```console
$ docker pull mono@sha256:27926c2c4a63765cb2fa66d25e6836c91f1d26dd544da3af02ea309bc3cb1496
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
$ docker pull mono@sha256:56079cf2e66e1c99c7df99a94af6e878735015befb38696382d11558f8691cb1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.3 MB (87342103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37a90f53167c056eec1636d8eeacce331e20daf9aad0b15a9b40df3706ef58d0`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 03:27:50 GMT
ADD file:40f52c233aecabf572a9db7450590d54d5e125fb00ecbb4a26fecd0b71e84eb8 in / 
# Thu, 16 Apr 2020 03:27:50 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 09:11:48 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 16 Apr 2020 09:12:00 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Apr 2020 09:12:35 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:5e35bd43cf7898d036f8515be74d45b2e3abd2a5534fc280de63a9c22dd175bd`  
		Last Modified: Thu, 16 Apr 2020 03:35:04 GMT  
		Size: 22.5 MB (22513476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79f990050ea7755c8b4310123b2d720a7fede3eaa9cf5a76acb2a5fbd0af58d5`  
		Last Modified: Thu, 16 Apr 2020 09:46:33 GMT  
		Size: 244.5 KB (244519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b463238d61e87361acee422c7ed4ee873ebc66a2a7b4dde702ca6956a532ecf`  
		Last Modified: Thu, 16 Apr 2020 09:46:52 GMT  
		Size: 64.6 MB (64584108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:988781ce7fd3739dba6c395332912434cb391801f362378ff13316fdc0c50a3b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46803115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8e01bfb2e90fa41fdda2d35621f00b8a0d51e600f008dd4e4518771218af14c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 00:54:51 GMT
ADD file:ba6c5e03457e69f59231e8e7c6465c1ec985812f0d8f7a65d9842f2be3e947fb in / 
# Thu, 16 Apr 2020 00:54:54 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 03:22:05 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 16 Apr 2020 03:22:36 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Apr 2020 03:23:29 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:b7d527e4baf13a6c926fb354fe1b38cb42b96f249ae65fdc0f52c853b654e06e`  
		Last Modified: Thu, 16 Apr 2020 01:02:32 GMT  
		Size: 21.2 MB (21190797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5251e801555d8cd1370a8d39ca953a0fb8f39729ff494b4a60bd03b4255c45be`  
		Last Modified: Thu, 16 Apr 2020 03:36:12 GMT  
		Size: 244.6 KB (244555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7c9b96b75ebb7a3cac23cf75e27179b71b5aa2cee0c40c33aca6399e29516f2`  
		Last Modified: Thu, 16 Apr 2020 03:36:22 GMT  
		Size: 25.4 MB (25367763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:fec0e4861eab05dd7c3eb364beefae8f8d5fc2ef225162e038b210af4cb3d508
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44151837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b78272cf77806b892fb8ce1da5a728ff7eaee3e059bb9ed6a77bd80478f1be7`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 01:05:08 GMT
ADD file:e37c4728c0c89ac126542ac35e7e493425c021bfac751079c9b266821a1b4e99 in / 
# Thu, 16 Apr 2020 01:05:10 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 04:40:35 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 16 Apr 2020 04:40:56 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Apr 2020 04:41:45 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:f78d9963dfddc4747d6200353b50f6093a6e37ca82e1612fa397d64ff13e7299`  
		Last Modified: Thu, 16 Apr 2020 01:12:33 GMT  
		Size: 19.3 MB (19298546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70114347da279136ebd21697ef769dc5764f716c6f7331568bbf7306c17da63c`  
		Last Modified: Thu, 16 Apr 2020 04:54:02 GMT  
		Size: 244.6 KB (244551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:802f26edffea7b59f9cc74e47561799e0c847d999b0db0dd2d99497c42af3511`  
		Last Modified: Thu, 16 Apr 2020 04:54:10 GMT  
		Size: 24.6 MB (24608740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:d08953373b3ef1fc7db79f7f13d8698af415ccec4a187b24ccd2e20c729b8c7d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (50034663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4c3ba9afd0517a25a4e83d0efc8b8d5d84880dbcc969fd912d6ce0463995374`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 02:45:19 GMT
ADD file:1588320d1c43714ec0353b7471f2ffd649045ca0f5f70dcb1eb064875fff9578 in / 
# Thu, 16 Apr 2020 02:45:21 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 06:47:03 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 16 Apr 2020 06:47:21 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Apr 2020 06:48:05 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:8978c87ff45d64d1663a585dcf1ed66d9e711c2e4048d83ef561da9514ef46e6`  
		Last Modified: Thu, 16 Apr 2020 02:51:32 GMT  
		Size: 20.4 MB (20370106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:090b996e11040b9a724d4b94b5f6fea43f5cee5558fdcdcb2e4627d1c596f82c`  
		Last Modified: Thu, 16 Apr 2020 06:59:20 GMT  
		Size: 244.4 KB (244369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be77ae0e8a98b883233d159b79364894a76d49f1b02badb9f57b227a26a8e1a`  
		Last Modified: Thu, 16 Apr 2020 06:59:30 GMT  
		Size: 29.4 MB (29420188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:slim` - linux; 386

```console
$ docker pull mono@sha256:992d47fb588cd80517b999abe4626317c65dcfd5eb0dea3bea6b02cdb56b5db5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.0 MB (92016888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f41612f812aa87758c87bf3cf7d3d08ab20128631db6c4454c68b94583387608`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:42:13 GMT
ADD file:82f76d577eec142f824456d027e5f82f681c9f5a09aeef4f711cef4662dcaea4 in / 
# Thu, 23 Apr 2020 00:42:13 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:04:12 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 23 Apr 2020 01:04:23 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 01:05:02 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7cb0551c4675347b94a8c63d7ee1f99dea4ab34aa7f23602ca587b6894d0211b`  
		Last Modified: Thu, 23 Apr 2020 00:47:39 GMT  
		Size: 23.1 MB (23141423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa3b9d440d2c40f2a9f3756fc7f8347bb9ec214b84fa396a388bd94782e1a678`  
		Last Modified: Thu, 23 Apr 2020 01:14:10 GMT  
		Size: 244.5 KB (244496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de2b74896e741d2269bb5084cfdbe6af6d2fc8d9d0ed1fc3f055d7c644afad5d`  
		Last Modified: Thu, 23 Apr 2020 01:14:29 GMT  
		Size: 68.6 MB (68630969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:slim` - linux; ppc64le

```console
$ docker pull mono@sha256:fa72fc4c116a54fd72fa979ab6db10a3798c1a0719a1b40884ceabbb476291c2
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48805899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccafa8bda50e8b6b041a02bca8290435a0dac26f6b7f52a0f59d6d21222413f1`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 01:43:57 GMT
ADD file:1c7f60f778e4b93490d570487d56275925e5eb477632e71cb9f035ce6edf2460 in / 
# Thu, 16 Apr 2020 01:44:03 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 06:37:42 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 16 Apr 2020 06:39:43 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Apr 2020 06:41:27 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:15e508b90ba1d327da83b72fc494ca263c1566ef6f70b91001cf2093395ffa3d`  
		Last Modified: Thu, 16 Apr 2020 02:04:33 GMT  
		Size: 22.8 MB (22785425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1629fdf02d54d31ae3023cd8b4a515c3c17a085c6135c7a10e412896d06a1f62`  
		Last Modified: Thu, 16 Apr 2020 07:18:38 GMT  
		Size: 244.7 KB (244669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fc63fa4246f2b9b66f762d8c33434e375c088c1ca73c3a389a8fb2525f93c7c`  
		Last Modified: Thu, 16 Apr 2020 07:18:43 GMT  
		Size: 25.8 MB (25775805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
