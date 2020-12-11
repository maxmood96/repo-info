<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `mono`

-	[`mono:6`](#mono6)
-	[`mono:6.10`](#mono610)
-	[`mono:6.10.0`](#mono6100)
-	[`mono:6.10.0.104`](#mono6100104)
-	[`mono:6.10.0.104-slim`](#mono6100104-slim)
-	[`mono:6.10.0-slim`](#mono6100-slim)
-	[`mono:6.10-slim`](#mono610-slim)
-	[`mono:6.12`](#mono612)
-	[`mono:6.12.0`](#mono6120)
-	[`mono:6.12.0.107`](#mono6120107)
-	[`mono:6.12.0.107-slim`](#mono6120107-slim)
-	[`mono:6.12.0-slim`](#mono6120-slim)
-	[`mono:6.12-slim`](#mono612-slim)
-	[`mono:6-slim`](#mono6-slim)
-	[`mono:latest`](#monolatest)
-	[`mono:slim`](#monoslim)

## `mono:6`

```console
$ docker pull mono@sha256:d431506c2d11911eb64c2d9f39659db0e169497e109d6267192a60be06f7b44b
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
$ docker pull mono@sha256:96b84ede5d78d547e62b92d0825eee974cfbacc9f47b9f75af69478695a58d13
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.9 MB (235853741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:822277e848fa10c7140c66c299eba734801c87387ddc178735d778ac15424d98`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:21:17 GMT
ADD file:d2abb0e4e7ac1773741f51f57d3a0b8ffc7907348842d773f8c341ba17f856d5 in / 
# Tue, 17 Nov 2020 20:21:17 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 01:19:50 GMT
ENV MONO_VERSION=6.12.0.107
# Fri, 11 Dec 2020 01:19:57 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 11 Dec 2020 01:20:26 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Fri, 11 Dec 2020 01:26:13 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:852e50cd189dfeb54d97680d9fa6bed21a6d7d18cfb56d6abfe2de9d7f173795`  
		Last Modified: Tue, 17 Nov 2020 20:27:25 GMT  
		Size: 27.1 MB (27105484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e6233064e514b285c8ae365ea7d55fbf0a713ad2fca931700c8079d6446c49b`  
		Last Modified: Fri, 11 Dec 2020 01:26:51 GMT  
		Size: 255.9 KB (255875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f9ac2c1f775d37886a9bd817e589ee9d4f94498b47c6943859cef15bf40f644`  
		Last Modified: Fri, 11 Dec 2020 01:27:03 GMT  
		Size: 67.1 MB (67079224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f718081e23030a8a5ee7297892ab3243006007a4d3079089e53f7c1a576a5704`  
		Last Modified: Fri, 11 Dec 2020 01:27:38 GMT  
		Size: 141.4 MB (141413158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6` - linux; arm variant v5

```console
$ docker pull mono@sha256:473d4f85ae7cc53f4f40e4cec170ffb02ae051156e692328dc20edab624a0384
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.7 MB (191713047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adb27fc6a3ca19d052ab16220598fea32e5b5376e577a9fabac102703373498d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:20:37 GMT
ADD file:d75cebdc79385debd2d6d1c8c34855d2bd4779b13ee47f76e34c6d8fca037531 in / 
# Tue, 17 Nov 2020 20:20:45 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 00:48:44 GMT
ENV MONO_VERSION=6.12.0.107
# Fri, 11 Dec 2020 00:49:07 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 11 Dec 2020 00:49:53 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Fri, 11 Dec 2020 00:53:25 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:1b8dd2ec17ab788b6ea03a9b6cf68afada9a8692681d29e9795db0abf6554404`  
		Last Modified: Tue, 17 Nov 2020 20:30:33 GMT  
		Size: 24.9 MB (24850311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05baa1a4580b5db26b6e95be46ea7c3c911e02763abc687ff0b7ff1ac8c3d69e`  
		Last Modified: Fri, 11 Dec 2020 00:53:53 GMT  
		Size: 255.9 KB (255949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fcd83802c296fe8f139c457197e375b3de65bebb1f2b2a4f96b337a147d3010`  
		Last Modified: Fri, 11 Dec 2020 00:54:03 GMT  
		Size: 26.5 MB (26499209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd173961b252fccb0b1cb9ce85aeb7fead6cfde53661f8220657d0219c852c93`  
		Last Modified: Fri, 11 Dec 2020 00:55:07 GMT  
		Size: 140.1 MB (140107578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6` - linux; arm variant v7

```console
$ docker pull mono@sha256:6840c9b51b31901fef43c1a0d7a1b9c1ec8326305d87b9b4ba29250cc5d1e318
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.6 MB (187609654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:359606b19f2fa4d122660a6d4e2e26a97fbdf9e60420856ba2749ee9fa8984c5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:21:06 GMT
ADD file:2035658a8d20545ee7b2ab3ee791a371925fca7968ac29435303da24a1378f34 in / 
# Tue, 17 Nov 2020 20:21:10 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 01:19:56 GMT
ENV MONO_VERSION=6.12.0.107
# Fri, 11 Dec 2020 01:20:12 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 11 Dec 2020 01:20:52 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Fri, 11 Dec 2020 01:23:21 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:d5029e4b387017f20ad9f77baf3b81dd41f851d6340363b842a8a1d9786a60a0`  
		Last Modified: Tue, 17 Nov 2020 20:31:46 GMT  
		Size: 22.7 MB (22714186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b10337bd0f9a5533e53c8e57aa108beb3685d96b1f29a24c1945cf8094e9c5da`  
		Last Modified: Fri, 11 Dec 2020 01:23:59 GMT  
		Size: 255.9 KB (255913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0908544f1142db6230e88978959bd9c49919463ca61ea613cda8c14c6e8532f7`  
		Last Modified: Fri, 11 Dec 2020 01:24:09 GMT  
		Size: 25.7 MB (25697558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0bf7204709176636291b8e80c80feb213cf279c6ee49042b457a680a1e67bb0`  
		Last Modified: Fri, 11 Dec 2020 01:25:23 GMT  
		Size: 138.9 MB (138941997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:d9ce20966960efd33ea082f4be5611194898724cb5c2ad35c52df854481cf3e5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.4 MB (214420258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d37443135e41fd61c8c20eb555b7f08dc740c82b8e491b8b30f1621606d2a72f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:23:31 GMT
ADD file:a70d8c01f8f04f36038968567af779883f3b5ba3147b662b7d170d80418bc23c in / 
# Tue, 17 Nov 2020 20:23:32 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 00:40:21 GMT
ENV MONO_VERSION=6.12.0.107
# Fri, 11 Dec 2020 00:40:42 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 11 Dec 2020 00:41:18 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Fri, 11 Dec 2020 00:43:37 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:29ade854e0dcedde295dd89890d45271e9df839e42124558eb5283508ca70f5c`  
		Last Modified: Tue, 17 Nov 2020 20:32:02 GMT  
		Size: 25.9 MB (25862532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dc9211a1c3bffc7a39cf8c3174d7f7de9329295b6474bdd8d72ab9644fff94e`  
		Last Modified: Fri, 11 Dec 2020 00:44:08 GMT  
		Size: 255.9 KB (255921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc83dcb6b6716a71be07cbacf280c77737ea97150be83a369ab6b491deef0418`  
		Last Modified: Fri, 11 Dec 2020 00:44:18 GMT  
		Size: 31.7 MB (31720201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:605dbd553726e1c842cd862bd130bda02b5dd2dd87c1c7be25c140457394ab24`  
		Last Modified: Fri, 11 Dec 2020 00:45:18 GMT  
		Size: 156.6 MB (156581604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6` - linux; 386

```console
$ docker pull mono@sha256:aceece2f87de6b14a1d759171c3298d106329198865762c07512328c4ea9c9f1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.6 MB (241638109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77f8c8e180ef4b56a8317b0e7f56bf15637e67f9cbe2765dd931c94901200840`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:19:58 GMT
ADD file:b17dfa607fcb298beb9c58bfbb8b9b0743ceb385875776c56269db2506840edf in / 
# Tue, 17 Nov 2020 20:19:58 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 00:38:44 GMT
ENV MONO_VERSION=6.12.0.107
# Fri, 11 Dec 2020 00:38:53 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 11 Dec 2020 00:39:26 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Fri, 11 Dec 2020 00:41:19 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:e8e82c9fb36b8f3a9b8f18fe1d88e4d425d5c45968e3f2e94cdbb1255feb4878`  
		Last Modified: Tue, 17 Nov 2020 20:26:45 GMT  
		Size: 27.8 MB (27766186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddafc845098e9a2a66850e53bdcfaa1173904510dc84bf2c6910925a4c3c045a`  
		Last Modified: Fri, 11 Dec 2020 00:41:47 GMT  
		Size: 255.8 KB (255802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18dbe8684dd9be0f4cf763eb0f7f7c137403ef2666575c628e10ed25e8938eef`  
		Last Modified: Fri, 11 Dec 2020 00:42:06 GMT  
		Size: 71.1 MB (71105266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b01d92c97d300c373e938a159f2198670e8486deadc76da9641fc06fccc49e8`  
		Last Modified: Fri, 11 Dec 2020 00:43:01 GMT  
		Size: 142.5 MB (142510855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6` - linux; ppc64le

```console
$ docker pull mono@sha256:bfa4cad02f57da9b1a2aab29e864a791c4cd652fabd5640a7088ae867c848db7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.3 MB (203322144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c96fb8cd25f6f2747352c471e02a0dd9f40eb53eb73c9324267b695fcd44637`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 23:23:06 GMT
ADD file:49cd8b08964980901349e1f3d6cb34abd8145dea6e6d9ab83502452281ac73ca in / 
# Tue, 17 Nov 2020 23:23:11 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 02:25:07 GMT
ENV MONO_VERSION=6.12.0.107
# Fri, 11 Dec 2020 02:27:07 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 11 Dec 2020 02:29:15 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Fri, 11 Dec 2020 02:38:24 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:d79345c10f03543bff3982aedb35a18ba18626c0074014387ff5e1dc14474e2b`  
		Last Modified: Tue, 17 Nov 2020 23:32:54 GMT  
		Size: 30.5 MB (30531702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:733aef212d5acea62b32e63a1a43fed9cb16944c22591c847bf1c02c81f2c825`  
		Last Modified: Fri, 11 Dec 2020 02:39:11 GMT  
		Size: 256.2 KB (256158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cad78cba8d670a26f74487900565a5e53b2b5d740157a89bd6eb41e697f0ae30`  
		Last Modified: Fri, 11 Dec 2020 02:39:17 GMT  
		Size: 29.3 MB (29311041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d81d40cea93af85e059a41187a7c7944c7f55d440959b55db9f5ad40f1eb4f8`  
		Last Modified: Fri, 11 Dec 2020 02:40:11 GMT  
		Size: 143.2 MB (143223243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.10`

```console
$ docker pull mono@sha256:cd34752c3bc2eded3acb5e3c49d71c3a895330031bfb626060771b950beb5070
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
$ docker pull mono@sha256:5593db39654d852ce818d8ef25c787eebf0f8ef8cdb11e5a2b12b00c904a778b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.7 MB (224742364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7a7a844a50dff51cc37dfa94a83b177590504eab1e131240073fd146b8dcf66`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:21:17 GMT
ADD file:d2abb0e4e7ac1773741f51f57d3a0b8ffc7907348842d773f8c341ba17f856d5 in / 
# Tue, 17 Nov 2020 20:21:17 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 07:08:45 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 18 Nov 2020 07:08:53 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 18 Nov 2020 07:09:24 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 18 Nov 2020 07:26:21 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:852e50cd189dfeb54d97680d9fa6bed21a6d7d18cfb56d6abfe2de9d7f173795`  
		Last Modified: Tue, 17 Nov 2020 20:27:25 GMT  
		Size: 27.1 MB (27105484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5e204cb0a8a1bcd014c8e9cd36d92f0d1a42125d7203b02283c9b039997aeac`  
		Last Modified: Wed, 18 Nov 2020 07:27:13 GMT  
		Size: 255.9 KB (255899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b378d0795c2a4b816636afdff794c4c0bb82d4d4e6a63d36d8de5be2f6872f1`  
		Last Modified: Wed, 18 Nov 2020 07:27:32 GMT  
		Size: 67.1 MB (67091983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27823e34066c504ad4b748d5e0d7ad0d2aacf4b68d913d80f0d729df49015d4c`  
		Last Modified: Wed, 18 Nov 2020 07:29:01 GMT  
		Size: 130.3 MB (130288998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10` - linux; arm variant v5

```console
$ docker pull mono@sha256:d45aa8784789253c8ce9fa5391898d6ca47ea04e83fa898266db88d513155628
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.6 MB (180595716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa918415172556b17a31b86e1be88c085e853a3e56be4d9a67da48add24abdf3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:20:37 GMT
ADD file:d75cebdc79385debd2d6d1c8c34855d2bd4779b13ee47f76e34c6d8fca037531 in / 
# Tue, 17 Nov 2020 20:20:45 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 05:46:58 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 18 Nov 2020 05:47:24 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 18 Nov 2020 05:48:16 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 18 Nov 2020 05:55:14 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:1b8dd2ec17ab788b6ea03a9b6cf68afada9a8692681d29e9795db0abf6554404`  
		Last Modified: Tue, 17 Nov 2020 20:30:33 GMT  
		Size: 24.9 MB (24850311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3228f7d7fd4527c495e957cad4161151c2770de40c3aba653d35301bde93de86`  
		Last Modified: Wed, 18 Nov 2020 05:55:58 GMT  
		Size: 256.0 KB (255956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0d828e50270469d9d028f2b4605b76cbac6d171d8a2c96f333f0f239ae792e7`  
		Last Modified: Wed, 18 Nov 2020 05:56:07 GMT  
		Size: 26.5 MB (26530821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5af7a2ddbd1cc7bb6d0d2f58d73a979910db73f017bf8414c4538e3b5af2fd0e`  
		Last Modified: Wed, 18 Nov 2020 05:57:55 GMT  
		Size: 129.0 MB (128958628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10` - linux; arm variant v7

```console
$ docker pull mono@sha256:4b2244e9e398d0e9c0aeac23f848893f33b629bd67c0b8184a15e69b66a40596
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.5 MB (176498939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0992eb45ed8362ddad1e241cd7e1b8f538fcea42cf1d2fcbd363bcce95b9ddf`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:21:06 GMT
ADD file:2035658a8d20545ee7b2ab3ee791a371925fca7968ac29435303da24a1378f34 in / 
# Tue, 17 Nov 2020 20:21:10 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 14:56:54 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 18 Nov 2020 14:57:16 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 18 Nov 2020 14:58:11 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 18 Nov 2020 15:06:51 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:d5029e4b387017f20ad9f77baf3b81dd41f851d6340363b842a8a1d9786a60a0`  
		Last Modified: Tue, 17 Nov 2020 20:31:46 GMT  
		Size: 22.7 MB (22714186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7071e69fcfb9ee0aee198b34d2e65971bce210154ca78029673f7a4587dba98c`  
		Last Modified: Wed, 18 Nov 2020 15:07:42 GMT  
		Size: 256.0 KB (255978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0c6379263fdd01744f7b8bcdcf328bb04a1efc5e78229d1770f08c3ab63adf9`  
		Last Modified: Wed, 18 Nov 2020 15:07:51 GMT  
		Size: 25.7 MB (25729440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:065fb66dbd135e6fd255f3b5d1732920e266c1d0d2690ba903afd46166d6e124`  
		Last Modified: Wed, 18 Nov 2020 15:09:44 GMT  
		Size: 127.8 MB (127799335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:0b5ce90bc0624cc3be76e2f4faa9b5ece9459fbda3fd2d1e600b0d03a6693710
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.3 MB (203308506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:684f822e67b92095a97967c053ec1acb78c5d01f5ca24b36822f3fee9136d53f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:23:31 GMT
ADD file:a70d8c01f8f04f36038968567af779883f3b5ba3147b662b7d170d80418bc23c in / 
# Tue, 17 Nov 2020 20:23:32 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 01:28:53 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 18 Nov 2020 01:29:10 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 18 Nov 2020 01:29:56 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 18 Nov 2020 01:35:25 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:29ade854e0dcedde295dd89890d45271e9df839e42124558eb5283508ca70f5c`  
		Last Modified: Tue, 17 Nov 2020 20:32:02 GMT  
		Size: 25.9 MB (25862532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:808368e9cd11971fa6e53b4a3fbb5559d120515e05c721adff9b9e493870a0f5`  
		Last Modified: Wed, 18 Nov 2020 01:36:25 GMT  
		Size: 255.9 KB (255886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cdf6ac0c679ba4beaf9bad32b903763540d340a1b59395c930a56b288947efe`  
		Last Modified: Wed, 18 Nov 2020 01:36:35 GMT  
		Size: 31.8 MB (31750189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a85a8c7edd4b4a3cbd35f220923da50329be4d48bbff3d793963214b91d5e4c9`  
		Last Modified: Wed, 18 Nov 2020 01:38:19 GMT  
		Size: 145.4 MB (145439899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10` - linux; 386

```console
$ docker pull mono@sha256:b6a3f46742bbeebd7491950574d6670f15863a5ae4c604ed38c6eab1212211ea
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.5 MB (230548555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eff3efc70af7902825ccee149ea5f3fa588813efc83e2ac90d90289c04a1e94`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:19:58 GMT
ADD file:b17dfa607fcb298beb9c58bfbb8b9b0743ceb385875776c56269db2506840edf in / 
# Tue, 17 Nov 2020 20:19:58 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 07:10:34 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 18 Nov 2020 07:10:43 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 18 Nov 2020 07:11:17 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 18 Nov 2020 07:15:25 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:e8e82c9fb36b8f3a9b8f18fe1d88e4d425d5c45968e3f2e94cdbb1255feb4878`  
		Last Modified: Tue, 17 Nov 2020 20:26:45 GMT  
		Size: 27.8 MB (27766186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7728bf5c7d01242edd3caa5516ba67b527e7e5ebacc60acc92ec87ab4a216ca3`  
		Last Modified: Wed, 18 Nov 2020 07:16:18 GMT  
		Size: 255.8 KB (255787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1b312aaf488353a9cc2301775941b37a63ac9657c3ea5f34cb83895f0d7f5c9`  
		Last Modified: Wed, 18 Nov 2020 07:16:37 GMT  
		Size: 71.1 MB (71136113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a53fe17c731caaa48043bd0e7a92d35f1db96a495f92451cd76b92e6a099b53`  
		Last Modified: Wed, 18 Nov 2020 07:18:16 GMT  
		Size: 131.4 MB (131390469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10` - linux; ppc64le

```console
$ docker pull mono@sha256:cb6d3a3c47acd14b27e76bbba7077cf19f76fc9b86c279ce9b2d1470faba4d4f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.1 MB (192096926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3b83ed59adcd6362c0fcec407ca8017ca3ef638df84b06b2fd4d36c6f4eaec5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 23:23:06 GMT
ADD file:49cd8b08964980901349e1f3d6cb34abd8145dea6e6d9ab83502452281ac73ca in / 
# Tue, 17 Nov 2020 23:23:11 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 02:30:57 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 18 Nov 2020 02:34:55 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 18 Nov 2020 02:38:07 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 18 Nov 2020 03:13:46 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:d79345c10f03543bff3982aedb35a18ba18626c0074014387ff5e1dc14474e2b`  
		Last Modified: Tue, 17 Nov 2020 23:32:54 GMT  
		Size: 30.5 MB (30531702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b14255bc818ce18b4ab09d9ee61d303092bc8657a173fc74c8c64df944e601a5`  
		Last Modified: Wed, 18 Nov 2020 03:15:04 GMT  
		Size: 256.3 KB (256335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2851074b86d7cc53505b83fe532498eba28284dcefcfa6e682fe54a43bbc6298`  
		Last Modified: Wed, 18 Nov 2020 03:15:10 GMT  
		Size: 29.4 MB (29350154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:657abbc039836a14e1056151333245607dc809d83c5cda326e16ceb5a97b8e3d`  
		Last Modified: Wed, 18 Nov 2020 03:16:43 GMT  
		Size: 132.0 MB (131958735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.10.0`

```console
$ docker pull mono@sha256:cd34752c3bc2eded3acb5e3c49d71c3a895330031bfb626060771b950beb5070
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
$ docker pull mono@sha256:5593db39654d852ce818d8ef25c787eebf0f8ef8cdb11e5a2b12b00c904a778b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.7 MB (224742364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7a7a844a50dff51cc37dfa94a83b177590504eab1e131240073fd146b8dcf66`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:21:17 GMT
ADD file:d2abb0e4e7ac1773741f51f57d3a0b8ffc7907348842d773f8c341ba17f856d5 in / 
# Tue, 17 Nov 2020 20:21:17 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 07:08:45 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 18 Nov 2020 07:08:53 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 18 Nov 2020 07:09:24 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 18 Nov 2020 07:26:21 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:852e50cd189dfeb54d97680d9fa6bed21a6d7d18cfb56d6abfe2de9d7f173795`  
		Last Modified: Tue, 17 Nov 2020 20:27:25 GMT  
		Size: 27.1 MB (27105484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5e204cb0a8a1bcd014c8e9cd36d92f0d1a42125d7203b02283c9b039997aeac`  
		Last Modified: Wed, 18 Nov 2020 07:27:13 GMT  
		Size: 255.9 KB (255899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b378d0795c2a4b816636afdff794c4c0bb82d4d4e6a63d36d8de5be2f6872f1`  
		Last Modified: Wed, 18 Nov 2020 07:27:32 GMT  
		Size: 67.1 MB (67091983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27823e34066c504ad4b748d5e0d7ad0d2aacf4b68d913d80f0d729df49015d4c`  
		Last Modified: Wed, 18 Nov 2020 07:29:01 GMT  
		Size: 130.3 MB (130288998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0` - linux; arm variant v5

```console
$ docker pull mono@sha256:d45aa8784789253c8ce9fa5391898d6ca47ea04e83fa898266db88d513155628
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.6 MB (180595716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa918415172556b17a31b86e1be88c085e853a3e56be4d9a67da48add24abdf3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:20:37 GMT
ADD file:d75cebdc79385debd2d6d1c8c34855d2bd4779b13ee47f76e34c6d8fca037531 in / 
# Tue, 17 Nov 2020 20:20:45 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 05:46:58 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 18 Nov 2020 05:47:24 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 18 Nov 2020 05:48:16 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 18 Nov 2020 05:55:14 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:1b8dd2ec17ab788b6ea03a9b6cf68afada9a8692681d29e9795db0abf6554404`  
		Last Modified: Tue, 17 Nov 2020 20:30:33 GMT  
		Size: 24.9 MB (24850311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3228f7d7fd4527c495e957cad4161151c2770de40c3aba653d35301bde93de86`  
		Last Modified: Wed, 18 Nov 2020 05:55:58 GMT  
		Size: 256.0 KB (255956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0d828e50270469d9d028f2b4605b76cbac6d171d8a2c96f333f0f239ae792e7`  
		Last Modified: Wed, 18 Nov 2020 05:56:07 GMT  
		Size: 26.5 MB (26530821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5af7a2ddbd1cc7bb6d0d2f58d73a979910db73f017bf8414c4538e3b5af2fd0e`  
		Last Modified: Wed, 18 Nov 2020 05:57:55 GMT  
		Size: 129.0 MB (128958628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0` - linux; arm variant v7

```console
$ docker pull mono@sha256:4b2244e9e398d0e9c0aeac23f848893f33b629bd67c0b8184a15e69b66a40596
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.5 MB (176498939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0992eb45ed8362ddad1e241cd7e1b8f538fcea42cf1d2fcbd363bcce95b9ddf`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:21:06 GMT
ADD file:2035658a8d20545ee7b2ab3ee791a371925fca7968ac29435303da24a1378f34 in / 
# Tue, 17 Nov 2020 20:21:10 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 14:56:54 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 18 Nov 2020 14:57:16 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 18 Nov 2020 14:58:11 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 18 Nov 2020 15:06:51 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:d5029e4b387017f20ad9f77baf3b81dd41f851d6340363b842a8a1d9786a60a0`  
		Last Modified: Tue, 17 Nov 2020 20:31:46 GMT  
		Size: 22.7 MB (22714186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7071e69fcfb9ee0aee198b34d2e65971bce210154ca78029673f7a4587dba98c`  
		Last Modified: Wed, 18 Nov 2020 15:07:42 GMT  
		Size: 256.0 KB (255978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0c6379263fdd01744f7b8bcdcf328bb04a1efc5e78229d1770f08c3ab63adf9`  
		Last Modified: Wed, 18 Nov 2020 15:07:51 GMT  
		Size: 25.7 MB (25729440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:065fb66dbd135e6fd255f3b5d1732920e266c1d0d2690ba903afd46166d6e124`  
		Last Modified: Wed, 18 Nov 2020 15:09:44 GMT  
		Size: 127.8 MB (127799335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:0b5ce90bc0624cc3be76e2f4faa9b5ece9459fbda3fd2d1e600b0d03a6693710
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.3 MB (203308506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:684f822e67b92095a97967c053ec1acb78c5d01f5ca24b36822f3fee9136d53f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:23:31 GMT
ADD file:a70d8c01f8f04f36038968567af779883f3b5ba3147b662b7d170d80418bc23c in / 
# Tue, 17 Nov 2020 20:23:32 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 01:28:53 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 18 Nov 2020 01:29:10 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 18 Nov 2020 01:29:56 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 18 Nov 2020 01:35:25 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:29ade854e0dcedde295dd89890d45271e9df839e42124558eb5283508ca70f5c`  
		Last Modified: Tue, 17 Nov 2020 20:32:02 GMT  
		Size: 25.9 MB (25862532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:808368e9cd11971fa6e53b4a3fbb5559d120515e05c721adff9b9e493870a0f5`  
		Last Modified: Wed, 18 Nov 2020 01:36:25 GMT  
		Size: 255.9 KB (255886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cdf6ac0c679ba4beaf9bad32b903763540d340a1b59395c930a56b288947efe`  
		Last Modified: Wed, 18 Nov 2020 01:36:35 GMT  
		Size: 31.8 MB (31750189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a85a8c7edd4b4a3cbd35f220923da50329be4d48bbff3d793963214b91d5e4c9`  
		Last Modified: Wed, 18 Nov 2020 01:38:19 GMT  
		Size: 145.4 MB (145439899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0` - linux; 386

```console
$ docker pull mono@sha256:b6a3f46742bbeebd7491950574d6670f15863a5ae4c604ed38c6eab1212211ea
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.5 MB (230548555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eff3efc70af7902825ccee149ea5f3fa588813efc83e2ac90d90289c04a1e94`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:19:58 GMT
ADD file:b17dfa607fcb298beb9c58bfbb8b9b0743ceb385875776c56269db2506840edf in / 
# Tue, 17 Nov 2020 20:19:58 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 07:10:34 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 18 Nov 2020 07:10:43 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 18 Nov 2020 07:11:17 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 18 Nov 2020 07:15:25 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:e8e82c9fb36b8f3a9b8f18fe1d88e4d425d5c45968e3f2e94cdbb1255feb4878`  
		Last Modified: Tue, 17 Nov 2020 20:26:45 GMT  
		Size: 27.8 MB (27766186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7728bf5c7d01242edd3caa5516ba67b527e7e5ebacc60acc92ec87ab4a216ca3`  
		Last Modified: Wed, 18 Nov 2020 07:16:18 GMT  
		Size: 255.8 KB (255787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1b312aaf488353a9cc2301775941b37a63ac9657c3ea5f34cb83895f0d7f5c9`  
		Last Modified: Wed, 18 Nov 2020 07:16:37 GMT  
		Size: 71.1 MB (71136113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a53fe17c731caaa48043bd0e7a92d35f1db96a495f92451cd76b92e6a099b53`  
		Last Modified: Wed, 18 Nov 2020 07:18:16 GMT  
		Size: 131.4 MB (131390469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0` - linux; ppc64le

```console
$ docker pull mono@sha256:cb6d3a3c47acd14b27e76bbba7077cf19f76fc9b86c279ce9b2d1470faba4d4f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.1 MB (192096926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3b83ed59adcd6362c0fcec407ca8017ca3ef638df84b06b2fd4d36c6f4eaec5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 23:23:06 GMT
ADD file:49cd8b08964980901349e1f3d6cb34abd8145dea6e6d9ab83502452281ac73ca in / 
# Tue, 17 Nov 2020 23:23:11 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 02:30:57 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 18 Nov 2020 02:34:55 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 18 Nov 2020 02:38:07 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 18 Nov 2020 03:13:46 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:d79345c10f03543bff3982aedb35a18ba18626c0074014387ff5e1dc14474e2b`  
		Last Modified: Tue, 17 Nov 2020 23:32:54 GMT  
		Size: 30.5 MB (30531702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b14255bc818ce18b4ab09d9ee61d303092bc8657a173fc74c8c64df944e601a5`  
		Last Modified: Wed, 18 Nov 2020 03:15:04 GMT  
		Size: 256.3 KB (256335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2851074b86d7cc53505b83fe532498eba28284dcefcfa6e682fe54a43bbc6298`  
		Last Modified: Wed, 18 Nov 2020 03:15:10 GMT  
		Size: 29.4 MB (29350154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:657abbc039836a14e1056151333245607dc809d83c5cda326e16ceb5a97b8e3d`  
		Last Modified: Wed, 18 Nov 2020 03:16:43 GMT  
		Size: 132.0 MB (131958735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.10.0.104`

```console
$ docker pull mono@sha256:cd34752c3bc2eded3acb5e3c49d71c3a895330031bfb626060771b950beb5070
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
$ docker pull mono@sha256:5593db39654d852ce818d8ef25c787eebf0f8ef8cdb11e5a2b12b00c904a778b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.7 MB (224742364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7a7a844a50dff51cc37dfa94a83b177590504eab1e131240073fd146b8dcf66`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:21:17 GMT
ADD file:d2abb0e4e7ac1773741f51f57d3a0b8ffc7907348842d773f8c341ba17f856d5 in / 
# Tue, 17 Nov 2020 20:21:17 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 07:08:45 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 18 Nov 2020 07:08:53 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 18 Nov 2020 07:09:24 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 18 Nov 2020 07:26:21 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:852e50cd189dfeb54d97680d9fa6bed21a6d7d18cfb56d6abfe2de9d7f173795`  
		Last Modified: Tue, 17 Nov 2020 20:27:25 GMT  
		Size: 27.1 MB (27105484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5e204cb0a8a1bcd014c8e9cd36d92f0d1a42125d7203b02283c9b039997aeac`  
		Last Modified: Wed, 18 Nov 2020 07:27:13 GMT  
		Size: 255.9 KB (255899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b378d0795c2a4b816636afdff794c4c0bb82d4d4e6a63d36d8de5be2f6872f1`  
		Last Modified: Wed, 18 Nov 2020 07:27:32 GMT  
		Size: 67.1 MB (67091983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27823e34066c504ad4b748d5e0d7ad0d2aacf4b68d913d80f0d729df49015d4c`  
		Last Modified: Wed, 18 Nov 2020 07:29:01 GMT  
		Size: 130.3 MB (130288998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0.104` - linux; arm variant v5

```console
$ docker pull mono@sha256:d45aa8784789253c8ce9fa5391898d6ca47ea04e83fa898266db88d513155628
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.6 MB (180595716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa918415172556b17a31b86e1be88c085e853a3e56be4d9a67da48add24abdf3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:20:37 GMT
ADD file:d75cebdc79385debd2d6d1c8c34855d2bd4779b13ee47f76e34c6d8fca037531 in / 
# Tue, 17 Nov 2020 20:20:45 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 05:46:58 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 18 Nov 2020 05:47:24 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 18 Nov 2020 05:48:16 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 18 Nov 2020 05:55:14 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:1b8dd2ec17ab788b6ea03a9b6cf68afada9a8692681d29e9795db0abf6554404`  
		Last Modified: Tue, 17 Nov 2020 20:30:33 GMT  
		Size: 24.9 MB (24850311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3228f7d7fd4527c495e957cad4161151c2770de40c3aba653d35301bde93de86`  
		Last Modified: Wed, 18 Nov 2020 05:55:58 GMT  
		Size: 256.0 KB (255956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0d828e50270469d9d028f2b4605b76cbac6d171d8a2c96f333f0f239ae792e7`  
		Last Modified: Wed, 18 Nov 2020 05:56:07 GMT  
		Size: 26.5 MB (26530821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5af7a2ddbd1cc7bb6d0d2f58d73a979910db73f017bf8414c4538e3b5af2fd0e`  
		Last Modified: Wed, 18 Nov 2020 05:57:55 GMT  
		Size: 129.0 MB (128958628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0.104` - linux; arm variant v7

```console
$ docker pull mono@sha256:4b2244e9e398d0e9c0aeac23f848893f33b629bd67c0b8184a15e69b66a40596
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.5 MB (176498939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0992eb45ed8362ddad1e241cd7e1b8f538fcea42cf1d2fcbd363bcce95b9ddf`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:21:06 GMT
ADD file:2035658a8d20545ee7b2ab3ee791a371925fca7968ac29435303da24a1378f34 in / 
# Tue, 17 Nov 2020 20:21:10 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 14:56:54 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 18 Nov 2020 14:57:16 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 18 Nov 2020 14:58:11 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 18 Nov 2020 15:06:51 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:d5029e4b387017f20ad9f77baf3b81dd41f851d6340363b842a8a1d9786a60a0`  
		Last Modified: Tue, 17 Nov 2020 20:31:46 GMT  
		Size: 22.7 MB (22714186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7071e69fcfb9ee0aee198b34d2e65971bce210154ca78029673f7a4587dba98c`  
		Last Modified: Wed, 18 Nov 2020 15:07:42 GMT  
		Size: 256.0 KB (255978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0c6379263fdd01744f7b8bcdcf328bb04a1efc5e78229d1770f08c3ab63adf9`  
		Last Modified: Wed, 18 Nov 2020 15:07:51 GMT  
		Size: 25.7 MB (25729440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:065fb66dbd135e6fd255f3b5d1732920e266c1d0d2690ba903afd46166d6e124`  
		Last Modified: Wed, 18 Nov 2020 15:09:44 GMT  
		Size: 127.8 MB (127799335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0.104` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:0b5ce90bc0624cc3be76e2f4faa9b5ece9459fbda3fd2d1e600b0d03a6693710
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.3 MB (203308506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:684f822e67b92095a97967c053ec1acb78c5d01f5ca24b36822f3fee9136d53f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:23:31 GMT
ADD file:a70d8c01f8f04f36038968567af779883f3b5ba3147b662b7d170d80418bc23c in / 
# Tue, 17 Nov 2020 20:23:32 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 01:28:53 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 18 Nov 2020 01:29:10 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 18 Nov 2020 01:29:56 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 18 Nov 2020 01:35:25 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:29ade854e0dcedde295dd89890d45271e9df839e42124558eb5283508ca70f5c`  
		Last Modified: Tue, 17 Nov 2020 20:32:02 GMT  
		Size: 25.9 MB (25862532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:808368e9cd11971fa6e53b4a3fbb5559d120515e05c721adff9b9e493870a0f5`  
		Last Modified: Wed, 18 Nov 2020 01:36:25 GMT  
		Size: 255.9 KB (255886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cdf6ac0c679ba4beaf9bad32b903763540d340a1b59395c930a56b288947efe`  
		Last Modified: Wed, 18 Nov 2020 01:36:35 GMT  
		Size: 31.8 MB (31750189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a85a8c7edd4b4a3cbd35f220923da50329be4d48bbff3d793963214b91d5e4c9`  
		Last Modified: Wed, 18 Nov 2020 01:38:19 GMT  
		Size: 145.4 MB (145439899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0.104` - linux; 386

```console
$ docker pull mono@sha256:b6a3f46742bbeebd7491950574d6670f15863a5ae4c604ed38c6eab1212211ea
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.5 MB (230548555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eff3efc70af7902825ccee149ea5f3fa588813efc83e2ac90d90289c04a1e94`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:19:58 GMT
ADD file:b17dfa607fcb298beb9c58bfbb8b9b0743ceb385875776c56269db2506840edf in / 
# Tue, 17 Nov 2020 20:19:58 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 07:10:34 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 18 Nov 2020 07:10:43 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 18 Nov 2020 07:11:17 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 18 Nov 2020 07:15:25 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:e8e82c9fb36b8f3a9b8f18fe1d88e4d425d5c45968e3f2e94cdbb1255feb4878`  
		Last Modified: Tue, 17 Nov 2020 20:26:45 GMT  
		Size: 27.8 MB (27766186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7728bf5c7d01242edd3caa5516ba67b527e7e5ebacc60acc92ec87ab4a216ca3`  
		Last Modified: Wed, 18 Nov 2020 07:16:18 GMT  
		Size: 255.8 KB (255787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1b312aaf488353a9cc2301775941b37a63ac9657c3ea5f34cb83895f0d7f5c9`  
		Last Modified: Wed, 18 Nov 2020 07:16:37 GMT  
		Size: 71.1 MB (71136113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a53fe17c731caaa48043bd0e7a92d35f1db96a495f92451cd76b92e6a099b53`  
		Last Modified: Wed, 18 Nov 2020 07:18:16 GMT  
		Size: 131.4 MB (131390469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0.104` - linux; ppc64le

```console
$ docker pull mono@sha256:cb6d3a3c47acd14b27e76bbba7077cf19f76fc9b86c279ce9b2d1470faba4d4f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.1 MB (192096926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3b83ed59adcd6362c0fcec407ca8017ca3ef638df84b06b2fd4d36c6f4eaec5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 23:23:06 GMT
ADD file:49cd8b08964980901349e1f3d6cb34abd8145dea6e6d9ab83502452281ac73ca in / 
# Tue, 17 Nov 2020 23:23:11 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 02:30:57 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 18 Nov 2020 02:34:55 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 18 Nov 2020 02:38:07 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 18 Nov 2020 03:13:46 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:d79345c10f03543bff3982aedb35a18ba18626c0074014387ff5e1dc14474e2b`  
		Last Modified: Tue, 17 Nov 2020 23:32:54 GMT  
		Size: 30.5 MB (30531702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b14255bc818ce18b4ab09d9ee61d303092bc8657a173fc74c8c64df944e601a5`  
		Last Modified: Wed, 18 Nov 2020 03:15:04 GMT  
		Size: 256.3 KB (256335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2851074b86d7cc53505b83fe532498eba28284dcefcfa6e682fe54a43bbc6298`  
		Last Modified: Wed, 18 Nov 2020 03:15:10 GMT  
		Size: 29.4 MB (29350154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:657abbc039836a14e1056151333245607dc809d83c5cda326e16ceb5a97b8e3d`  
		Last Modified: Wed, 18 Nov 2020 03:16:43 GMT  
		Size: 132.0 MB (131958735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.10.0.104-slim`

```console
$ docker pull mono@sha256:a42ac573866bc6ec1b9878159e423c073e544a2fd5b3740955e601a62a693cf3
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
$ docker pull mono@sha256:97fea20b1b77d25cc11fac7ad33c667d95c7bfa42d70a4cb747db480ce72db47
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.5 MB (94453366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2452815b8c37bc96ea426ec2f1186a97e324ac5037e7f1a97a171adb6230dab4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:21:17 GMT
ADD file:d2abb0e4e7ac1773741f51f57d3a0b8ffc7907348842d773f8c341ba17f856d5 in / 
# Tue, 17 Nov 2020 20:21:17 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 07:08:45 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 18 Nov 2020 07:08:53 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 18 Nov 2020 07:09:24 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:852e50cd189dfeb54d97680d9fa6bed21a6d7d18cfb56d6abfe2de9d7f173795`  
		Last Modified: Tue, 17 Nov 2020 20:27:25 GMT  
		Size: 27.1 MB (27105484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5e204cb0a8a1bcd014c8e9cd36d92f0d1a42125d7203b02283c9b039997aeac`  
		Last Modified: Wed, 18 Nov 2020 07:27:13 GMT  
		Size: 255.9 KB (255899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b378d0795c2a4b816636afdff794c4c0bb82d4d4e6a63d36d8de5be2f6872f1`  
		Last Modified: Wed, 18 Nov 2020 07:27:32 GMT  
		Size: 67.1 MB (67091983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0.104-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:8e28d0ed25bf60bb6135857e9f72c435bc8a98460e9bf74f12976b2fa8429895
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51637088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2741f7b52ab236756f8e743bf84f6540178588e89316f62276e8e9bb5331995a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:20:37 GMT
ADD file:d75cebdc79385debd2d6d1c8c34855d2bd4779b13ee47f76e34c6d8fca037531 in / 
# Tue, 17 Nov 2020 20:20:45 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 05:46:58 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 18 Nov 2020 05:47:24 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 18 Nov 2020 05:48:16 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:1b8dd2ec17ab788b6ea03a9b6cf68afada9a8692681d29e9795db0abf6554404`  
		Last Modified: Tue, 17 Nov 2020 20:30:33 GMT  
		Size: 24.9 MB (24850311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3228f7d7fd4527c495e957cad4161151c2770de40c3aba653d35301bde93de86`  
		Last Modified: Wed, 18 Nov 2020 05:55:58 GMT  
		Size: 256.0 KB (255956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0d828e50270469d9d028f2b4605b76cbac6d171d8a2c96f333f0f239ae792e7`  
		Last Modified: Wed, 18 Nov 2020 05:56:07 GMT  
		Size: 26.5 MB (26530821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0.104-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:800fceb9a67e83837fae2e11f4b64ae33b8d3553062c74eb27a773036ea5be92
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48699604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12763218e02f17c76b24f4a7331eddeb6198fbee718bc11b781c70c9ba124d01`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:21:06 GMT
ADD file:2035658a8d20545ee7b2ab3ee791a371925fca7968ac29435303da24a1378f34 in / 
# Tue, 17 Nov 2020 20:21:10 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 14:56:54 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 18 Nov 2020 14:57:16 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 18 Nov 2020 14:58:11 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:d5029e4b387017f20ad9f77baf3b81dd41f851d6340363b842a8a1d9786a60a0`  
		Last Modified: Tue, 17 Nov 2020 20:31:46 GMT  
		Size: 22.7 MB (22714186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7071e69fcfb9ee0aee198b34d2e65971bce210154ca78029673f7a4587dba98c`  
		Last Modified: Wed, 18 Nov 2020 15:07:42 GMT  
		Size: 256.0 KB (255978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0c6379263fdd01744f7b8bcdcf328bb04a1efc5e78229d1770f08c3ab63adf9`  
		Last Modified: Wed, 18 Nov 2020 15:07:51 GMT  
		Size: 25.7 MB (25729440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0.104-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:f61a1980078fd63569530291f822a8b6ae13ad45b2b80ab0966e6e274bd43760
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.9 MB (57868607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecd1dcf4046ccc6dd611bd3d6b63c8138e7d813b6c0ccd08cd1606e395148fe1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:23:31 GMT
ADD file:a70d8c01f8f04f36038968567af779883f3b5ba3147b662b7d170d80418bc23c in / 
# Tue, 17 Nov 2020 20:23:32 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 01:28:53 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 18 Nov 2020 01:29:10 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 18 Nov 2020 01:29:56 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:29ade854e0dcedde295dd89890d45271e9df839e42124558eb5283508ca70f5c`  
		Last Modified: Tue, 17 Nov 2020 20:32:02 GMT  
		Size: 25.9 MB (25862532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:808368e9cd11971fa6e53b4a3fbb5559d120515e05c721adff9b9e493870a0f5`  
		Last Modified: Wed, 18 Nov 2020 01:36:25 GMT  
		Size: 255.9 KB (255886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cdf6ac0c679ba4beaf9bad32b903763540d340a1b59395c930a56b288947efe`  
		Last Modified: Wed, 18 Nov 2020 01:36:35 GMT  
		Size: 31.8 MB (31750189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0.104-slim` - linux; 386

```console
$ docker pull mono@sha256:4acb7b91a9c89254785f96073b67fcf64d99da56147b757288e820bf82b3daa0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.2 MB (99158086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f90534e856c9d4d5903471056089eae0d51fc0b0d45e9cc2fe371a62bf09709e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:19:58 GMT
ADD file:b17dfa607fcb298beb9c58bfbb8b9b0743ceb385875776c56269db2506840edf in / 
# Tue, 17 Nov 2020 20:19:58 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 07:10:34 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 18 Nov 2020 07:10:43 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 18 Nov 2020 07:11:17 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:e8e82c9fb36b8f3a9b8f18fe1d88e4d425d5c45968e3f2e94cdbb1255feb4878`  
		Last Modified: Tue, 17 Nov 2020 20:26:45 GMT  
		Size: 27.8 MB (27766186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7728bf5c7d01242edd3caa5516ba67b527e7e5ebacc60acc92ec87ab4a216ca3`  
		Last Modified: Wed, 18 Nov 2020 07:16:18 GMT  
		Size: 255.8 KB (255787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1b312aaf488353a9cc2301775941b37a63ac9657c3ea5f34cb83895f0d7f5c9`  
		Last Modified: Wed, 18 Nov 2020 07:16:37 GMT  
		Size: 71.1 MB (71136113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0.104-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:56fd040b508e826ca2b4b9571814abb328162114225e6359bb91fe88d073102b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60138191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbb3e30769d83f47adfb9790d84cf97bcfa99f68ec9d8f786d76e0c1156a4ad1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 23:23:06 GMT
ADD file:49cd8b08964980901349e1f3d6cb34abd8145dea6e6d9ab83502452281ac73ca in / 
# Tue, 17 Nov 2020 23:23:11 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 02:30:57 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 18 Nov 2020 02:34:55 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 18 Nov 2020 02:38:07 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:d79345c10f03543bff3982aedb35a18ba18626c0074014387ff5e1dc14474e2b`  
		Last Modified: Tue, 17 Nov 2020 23:32:54 GMT  
		Size: 30.5 MB (30531702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b14255bc818ce18b4ab09d9ee61d303092bc8657a173fc74c8c64df944e601a5`  
		Last Modified: Wed, 18 Nov 2020 03:15:04 GMT  
		Size: 256.3 KB (256335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2851074b86d7cc53505b83fe532498eba28284dcefcfa6e682fe54a43bbc6298`  
		Last Modified: Wed, 18 Nov 2020 03:15:10 GMT  
		Size: 29.4 MB (29350154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.10.0-slim`

```console
$ docker pull mono@sha256:a42ac573866bc6ec1b9878159e423c073e544a2fd5b3740955e601a62a693cf3
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
$ docker pull mono@sha256:97fea20b1b77d25cc11fac7ad33c667d95c7bfa42d70a4cb747db480ce72db47
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.5 MB (94453366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2452815b8c37bc96ea426ec2f1186a97e324ac5037e7f1a97a171adb6230dab4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:21:17 GMT
ADD file:d2abb0e4e7ac1773741f51f57d3a0b8ffc7907348842d773f8c341ba17f856d5 in / 
# Tue, 17 Nov 2020 20:21:17 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 07:08:45 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 18 Nov 2020 07:08:53 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 18 Nov 2020 07:09:24 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:852e50cd189dfeb54d97680d9fa6bed21a6d7d18cfb56d6abfe2de9d7f173795`  
		Last Modified: Tue, 17 Nov 2020 20:27:25 GMT  
		Size: 27.1 MB (27105484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5e204cb0a8a1bcd014c8e9cd36d92f0d1a42125d7203b02283c9b039997aeac`  
		Last Modified: Wed, 18 Nov 2020 07:27:13 GMT  
		Size: 255.9 KB (255899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b378d0795c2a4b816636afdff794c4c0bb82d4d4e6a63d36d8de5be2f6872f1`  
		Last Modified: Wed, 18 Nov 2020 07:27:32 GMT  
		Size: 67.1 MB (67091983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:8e28d0ed25bf60bb6135857e9f72c435bc8a98460e9bf74f12976b2fa8429895
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51637088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2741f7b52ab236756f8e743bf84f6540178588e89316f62276e8e9bb5331995a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:20:37 GMT
ADD file:d75cebdc79385debd2d6d1c8c34855d2bd4779b13ee47f76e34c6d8fca037531 in / 
# Tue, 17 Nov 2020 20:20:45 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 05:46:58 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 18 Nov 2020 05:47:24 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 18 Nov 2020 05:48:16 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:1b8dd2ec17ab788b6ea03a9b6cf68afada9a8692681d29e9795db0abf6554404`  
		Last Modified: Tue, 17 Nov 2020 20:30:33 GMT  
		Size: 24.9 MB (24850311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3228f7d7fd4527c495e957cad4161151c2770de40c3aba653d35301bde93de86`  
		Last Modified: Wed, 18 Nov 2020 05:55:58 GMT  
		Size: 256.0 KB (255956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0d828e50270469d9d028f2b4605b76cbac6d171d8a2c96f333f0f239ae792e7`  
		Last Modified: Wed, 18 Nov 2020 05:56:07 GMT  
		Size: 26.5 MB (26530821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:800fceb9a67e83837fae2e11f4b64ae33b8d3553062c74eb27a773036ea5be92
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48699604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12763218e02f17c76b24f4a7331eddeb6198fbee718bc11b781c70c9ba124d01`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:21:06 GMT
ADD file:2035658a8d20545ee7b2ab3ee791a371925fca7968ac29435303da24a1378f34 in / 
# Tue, 17 Nov 2020 20:21:10 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 14:56:54 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 18 Nov 2020 14:57:16 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 18 Nov 2020 14:58:11 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:d5029e4b387017f20ad9f77baf3b81dd41f851d6340363b842a8a1d9786a60a0`  
		Last Modified: Tue, 17 Nov 2020 20:31:46 GMT  
		Size: 22.7 MB (22714186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7071e69fcfb9ee0aee198b34d2e65971bce210154ca78029673f7a4587dba98c`  
		Last Modified: Wed, 18 Nov 2020 15:07:42 GMT  
		Size: 256.0 KB (255978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0c6379263fdd01744f7b8bcdcf328bb04a1efc5e78229d1770f08c3ab63adf9`  
		Last Modified: Wed, 18 Nov 2020 15:07:51 GMT  
		Size: 25.7 MB (25729440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:f61a1980078fd63569530291f822a8b6ae13ad45b2b80ab0966e6e274bd43760
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.9 MB (57868607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecd1dcf4046ccc6dd611bd3d6b63c8138e7d813b6c0ccd08cd1606e395148fe1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:23:31 GMT
ADD file:a70d8c01f8f04f36038968567af779883f3b5ba3147b662b7d170d80418bc23c in / 
# Tue, 17 Nov 2020 20:23:32 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 01:28:53 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 18 Nov 2020 01:29:10 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 18 Nov 2020 01:29:56 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:29ade854e0dcedde295dd89890d45271e9df839e42124558eb5283508ca70f5c`  
		Last Modified: Tue, 17 Nov 2020 20:32:02 GMT  
		Size: 25.9 MB (25862532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:808368e9cd11971fa6e53b4a3fbb5559d120515e05c721adff9b9e493870a0f5`  
		Last Modified: Wed, 18 Nov 2020 01:36:25 GMT  
		Size: 255.9 KB (255886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cdf6ac0c679ba4beaf9bad32b903763540d340a1b59395c930a56b288947efe`  
		Last Modified: Wed, 18 Nov 2020 01:36:35 GMT  
		Size: 31.8 MB (31750189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0-slim` - linux; 386

```console
$ docker pull mono@sha256:4acb7b91a9c89254785f96073b67fcf64d99da56147b757288e820bf82b3daa0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.2 MB (99158086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f90534e856c9d4d5903471056089eae0d51fc0b0d45e9cc2fe371a62bf09709e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:19:58 GMT
ADD file:b17dfa607fcb298beb9c58bfbb8b9b0743ceb385875776c56269db2506840edf in / 
# Tue, 17 Nov 2020 20:19:58 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 07:10:34 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 18 Nov 2020 07:10:43 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 18 Nov 2020 07:11:17 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:e8e82c9fb36b8f3a9b8f18fe1d88e4d425d5c45968e3f2e94cdbb1255feb4878`  
		Last Modified: Tue, 17 Nov 2020 20:26:45 GMT  
		Size: 27.8 MB (27766186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7728bf5c7d01242edd3caa5516ba67b527e7e5ebacc60acc92ec87ab4a216ca3`  
		Last Modified: Wed, 18 Nov 2020 07:16:18 GMT  
		Size: 255.8 KB (255787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1b312aaf488353a9cc2301775941b37a63ac9657c3ea5f34cb83895f0d7f5c9`  
		Last Modified: Wed, 18 Nov 2020 07:16:37 GMT  
		Size: 71.1 MB (71136113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:56fd040b508e826ca2b4b9571814abb328162114225e6359bb91fe88d073102b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60138191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbb3e30769d83f47adfb9790d84cf97bcfa99f68ec9d8f786d76e0c1156a4ad1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 23:23:06 GMT
ADD file:49cd8b08964980901349e1f3d6cb34abd8145dea6e6d9ab83502452281ac73ca in / 
# Tue, 17 Nov 2020 23:23:11 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 02:30:57 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 18 Nov 2020 02:34:55 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 18 Nov 2020 02:38:07 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:d79345c10f03543bff3982aedb35a18ba18626c0074014387ff5e1dc14474e2b`  
		Last Modified: Tue, 17 Nov 2020 23:32:54 GMT  
		Size: 30.5 MB (30531702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b14255bc818ce18b4ab09d9ee61d303092bc8657a173fc74c8c64df944e601a5`  
		Last Modified: Wed, 18 Nov 2020 03:15:04 GMT  
		Size: 256.3 KB (256335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2851074b86d7cc53505b83fe532498eba28284dcefcfa6e682fe54a43bbc6298`  
		Last Modified: Wed, 18 Nov 2020 03:15:10 GMT  
		Size: 29.4 MB (29350154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.10-slim`

```console
$ docker pull mono@sha256:a42ac573866bc6ec1b9878159e423c073e544a2fd5b3740955e601a62a693cf3
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
$ docker pull mono@sha256:97fea20b1b77d25cc11fac7ad33c667d95c7bfa42d70a4cb747db480ce72db47
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.5 MB (94453366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2452815b8c37bc96ea426ec2f1186a97e324ac5037e7f1a97a171adb6230dab4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:21:17 GMT
ADD file:d2abb0e4e7ac1773741f51f57d3a0b8ffc7907348842d773f8c341ba17f856d5 in / 
# Tue, 17 Nov 2020 20:21:17 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 07:08:45 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 18 Nov 2020 07:08:53 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 18 Nov 2020 07:09:24 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:852e50cd189dfeb54d97680d9fa6bed21a6d7d18cfb56d6abfe2de9d7f173795`  
		Last Modified: Tue, 17 Nov 2020 20:27:25 GMT  
		Size: 27.1 MB (27105484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5e204cb0a8a1bcd014c8e9cd36d92f0d1a42125d7203b02283c9b039997aeac`  
		Last Modified: Wed, 18 Nov 2020 07:27:13 GMT  
		Size: 255.9 KB (255899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b378d0795c2a4b816636afdff794c4c0bb82d4d4e6a63d36d8de5be2f6872f1`  
		Last Modified: Wed, 18 Nov 2020 07:27:32 GMT  
		Size: 67.1 MB (67091983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:8e28d0ed25bf60bb6135857e9f72c435bc8a98460e9bf74f12976b2fa8429895
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51637088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2741f7b52ab236756f8e743bf84f6540178588e89316f62276e8e9bb5331995a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:20:37 GMT
ADD file:d75cebdc79385debd2d6d1c8c34855d2bd4779b13ee47f76e34c6d8fca037531 in / 
# Tue, 17 Nov 2020 20:20:45 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 05:46:58 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 18 Nov 2020 05:47:24 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 18 Nov 2020 05:48:16 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:1b8dd2ec17ab788b6ea03a9b6cf68afada9a8692681d29e9795db0abf6554404`  
		Last Modified: Tue, 17 Nov 2020 20:30:33 GMT  
		Size: 24.9 MB (24850311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3228f7d7fd4527c495e957cad4161151c2770de40c3aba653d35301bde93de86`  
		Last Modified: Wed, 18 Nov 2020 05:55:58 GMT  
		Size: 256.0 KB (255956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0d828e50270469d9d028f2b4605b76cbac6d171d8a2c96f333f0f239ae792e7`  
		Last Modified: Wed, 18 Nov 2020 05:56:07 GMT  
		Size: 26.5 MB (26530821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:800fceb9a67e83837fae2e11f4b64ae33b8d3553062c74eb27a773036ea5be92
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48699604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12763218e02f17c76b24f4a7331eddeb6198fbee718bc11b781c70c9ba124d01`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:21:06 GMT
ADD file:2035658a8d20545ee7b2ab3ee791a371925fca7968ac29435303da24a1378f34 in / 
# Tue, 17 Nov 2020 20:21:10 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 14:56:54 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 18 Nov 2020 14:57:16 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 18 Nov 2020 14:58:11 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:d5029e4b387017f20ad9f77baf3b81dd41f851d6340363b842a8a1d9786a60a0`  
		Last Modified: Tue, 17 Nov 2020 20:31:46 GMT  
		Size: 22.7 MB (22714186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7071e69fcfb9ee0aee198b34d2e65971bce210154ca78029673f7a4587dba98c`  
		Last Modified: Wed, 18 Nov 2020 15:07:42 GMT  
		Size: 256.0 KB (255978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0c6379263fdd01744f7b8bcdcf328bb04a1efc5e78229d1770f08c3ab63adf9`  
		Last Modified: Wed, 18 Nov 2020 15:07:51 GMT  
		Size: 25.7 MB (25729440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:f61a1980078fd63569530291f822a8b6ae13ad45b2b80ab0966e6e274bd43760
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.9 MB (57868607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecd1dcf4046ccc6dd611bd3d6b63c8138e7d813b6c0ccd08cd1606e395148fe1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:23:31 GMT
ADD file:a70d8c01f8f04f36038968567af779883f3b5ba3147b662b7d170d80418bc23c in / 
# Tue, 17 Nov 2020 20:23:32 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 01:28:53 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 18 Nov 2020 01:29:10 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 18 Nov 2020 01:29:56 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:29ade854e0dcedde295dd89890d45271e9df839e42124558eb5283508ca70f5c`  
		Last Modified: Tue, 17 Nov 2020 20:32:02 GMT  
		Size: 25.9 MB (25862532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:808368e9cd11971fa6e53b4a3fbb5559d120515e05c721adff9b9e493870a0f5`  
		Last Modified: Wed, 18 Nov 2020 01:36:25 GMT  
		Size: 255.9 KB (255886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cdf6ac0c679ba4beaf9bad32b903763540d340a1b59395c930a56b288947efe`  
		Last Modified: Wed, 18 Nov 2020 01:36:35 GMT  
		Size: 31.8 MB (31750189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10-slim` - linux; 386

```console
$ docker pull mono@sha256:4acb7b91a9c89254785f96073b67fcf64d99da56147b757288e820bf82b3daa0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.2 MB (99158086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f90534e856c9d4d5903471056089eae0d51fc0b0d45e9cc2fe371a62bf09709e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:19:58 GMT
ADD file:b17dfa607fcb298beb9c58bfbb8b9b0743ceb385875776c56269db2506840edf in / 
# Tue, 17 Nov 2020 20:19:58 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 07:10:34 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 18 Nov 2020 07:10:43 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 18 Nov 2020 07:11:17 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:e8e82c9fb36b8f3a9b8f18fe1d88e4d425d5c45968e3f2e94cdbb1255feb4878`  
		Last Modified: Tue, 17 Nov 2020 20:26:45 GMT  
		Size: 27.8 MB (27766186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7728bf5c7d01242edd3caa5516ba67b527e7e5ebacc60acc92ec87ab4a216ca3`  
		Last Modified: Wed, 18 Nov 2020 07:16:18 GMT  
		Size: 255.8 KB (255787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1b312aaf488353a9cc2301775941b37a63ac9657c3ea5f34cb83895f0d7f5c9`  
		Last Modified: Wed, 18 Nov 2020 07:16:37 GMT  
		Size: 71.1 MB (71136113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:56fd040b508e826ca2b4b9571814abb328162114225e6359bb91fe88d073102b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60138191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbb3e30769d83f47adfb9790d84cf97bcfa99f68ec9d8f786d76e0c1156a4ad1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 23:23:06 GMT
ADD file:49cd8b08964980901349e1f3d6cb34abd8145dea6e6d9ab83502452281ac73ca in / 
# Tue, 17 Nov 2020 23:23:11 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 02:30:57 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 18 Nov 2020 02:34:55 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 18 Nov 2020 02:38:07 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:d79345c10f03543bff3982aedb35a18ba18626c0074014387ff5e1dc14474e2b`  
		Last Modified: Tue, 17 Nov 2020 23:32:54 GMT  
		Size: 30.5 MB (30531702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b14255bc818ce18b4ab09d9ee61d303092bc8657a173fc74c8c64df944e601a5`  
		Last Modified: Wed, 18 Nov 2020 03:15:04 GMT  
		Size: 256.3 KB (256335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2851074b86d7cc53505b83fe532498eba28284dcefcfa6e682fe54a43bbc6298`  
		Last Modified: Wed, 18 Nov 2020 03:15:10 GMT  
		Size: 29.4 MB (29350154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.12`

```console
$ docker pull mono@sha256:d431506c2d11911eb64c2d9f39659db0e169497e109d6267192a60be06f7b44b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:6.12` - linux; amd64

```console
$ docker pull mono@sha256:96b84ede5d78d547e62b92d0825eee974cfbacc9f47b9f75af69478695a58d13
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.9 MB (235853741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:822277e848fa10c7140c66c299eba734801c87387ddc178735d778ac15424d98`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:21:17 GMT
ADD file:d2abb0e4e7ac1773741f51f57d3a0b8ffc7907348842d773f8c341ba17f856d5 in / 
# Tue, 17 Nov 2020 20:21:17 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 01:19:50 GMT
ENV MONO_VERSION=6.12.0.107
# Fri, 11 Dec 2020 01:19:57 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 11 Dec 2020 01:20:26 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Fri, 11 Dec 2020 01:26:13 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:852e50cd189dfeb54d97680d9fa6bed21a6d7d18cfb56d6abfe2de9d7f173795`  
		Last Modified: Tue, 17 Nov 2020 20:27:25 GMT  
		Size: 27.1 MB (27105484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e6233064e514b285c8ae365ea7d55fbf0a713ad2fca931700c8079d6446c49b`  
		Last Modified: Fri, 11 Dec 2020 01:26:51 GMT  
		Size: 255.9 KB (255875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f9ac2c1f775d37886a9bd817e589ee9d4f94498b47c6943859cef15bf40f644`  
		Last Modified: Fri, 11 Dec 2020 01:27:03 GMT  
		Size: 67.1 MB (67079224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f718081e23030a8a5ee7297892ab3243006007a4d3079089e53f7c1a576a5704`  
		Last Modified: Fri, 11 Dec 2020 01:27:38 GMT  
		Size: 141.4 MB (141413158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12` - linux; arm variant v5

```console
$ docker pull mono@sha256:473d4f85ae7cc53f4f40e4cec170ffb02ae051156e692328dc20edab624a0384
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.7 MB (191713047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adb27fc6a3ca19d052ab16220598fea32e5b5376e577a9fabac102703373498d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:20:37 GMT
ADD file:d75cebdc79385debd2d6d1c8c34855d2bd4779b13ee47f76e34c6d8fca037531 in / 
# Tue, 17 Nov 2020 20:20:45 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 00:48:44 GMT
ENV MONO_VERSION=6.12.0.107
# Fri, 11 Dec 2020 00:49:07 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 11 Dec 2020 00:49:53 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Fri, 11 Dec 2020 00:53:25 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:1b8dd2ec17ab788b6ea03a9b6cf68afada9a8692681d29e9795db0abf6554404`  
		Last Modified: Tue, 17 Nov 2020 20:30:33 GMT  
		Size: 24.9 MB (24850311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05baa1a4580b5db26b6e95be46ea7c3c911e02763abc687ff0b7ff1ac8c3d69e`  
		Last Modified: Fri, 11 Dec 2020 00:53:53 GMT  
		Size: 255.9 KB (255949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fcd83802c296fe8f139c457197e375b3de65bebb1f2b2a4f96b337a147d3010`  
		Last Modified: Fri, 11 Dec 2020 00:54:03 GMT  
		Size: 26.5 MB (26499209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd173961b252fccb0b1cb9ce85aeb7fead6cfde53661f8220657d0219c852c93`  
		Last Modified: Fri, 11 Dec 2020 00:55:07 GMT  
		Size: 140.1 MB (140107578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12` - linux; arm variant v7

```console
$ docker pull mono@sha256:6840c9b51b31901fef43c1a0d7a1b9c1ec8326305d87b9b4ba29250cc5d1e318
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.6 MB (187609654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:359606b19f2fa4d122660a6d4e2e26a97fbdf9e60420856ba2749ee9fa8984c5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:21:06 GMT
ADD file:2035658a8d20545ee7b2ab3ee791a371925fca7968ac29435303da24a1378f34 in / 
# Tue, 17 Nov 2020 20:21:10 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 01:19:56 GMT
ENV MONO_VERSION=6.12.0.107
# Fri, 11 Dec 2020 01:20:12 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 11 Dec 2020 01:20:52 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Fri, 11 Dec 2020 01:23:21 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:d5029e4b387017f20ad9f77baf3b81dd41f851d6340363b842a8a1d9786a60a0`  
		Last Modified: Tue, 17 Nov 2020 20:31:46 GMT  
		Size: 22.7 MB (22714186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b10337bd0f9a5533e53c8e57aa108beb3685d96b1f29a24c1945cf8094e9c5da`  
		Last Modified: Fri, 11 Dec 2020 01:23:59 GMT  
		Size: 255.9 KB (255913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0908544f1142db6230e88978959bd9c49919463ca61ea613cda8c14c6e8532f7`  
		Last Modified: Fri, 11 Dec 2020 01:24:09 GMT  
		Size: 25.7 MB (25697558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0bf7204709176636291b8e80c80feb213cf279c6ee49042b457a680a1e67bb0`  
		Last Modified: Fri, 11 Dec 2020 01:25:23 GMT  
		Size: 138.9 MB (138941997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:d9ce20966960efd33ea082f4be5611194898724cb5c2ad35c52df854481cf3e5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.4 MB (214420258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d37443135e41fd61c8c20eb555b7f08dc740c82b8e491b8b30f1621606d2a72f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:23:31 GMT
ADD file:a70d8c01f8f04f36038968567af779883f3b5ba3147b662b7d170d80418bc23c in / 
# Tue, 17 Nov 2020 20:23:32 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 00:40:21 GMT
ENV MONO_VERSION=6.12.0.107
# Fri, 11 Dec 2020 00:40:42 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 11 Dec 2020 00:41:18 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Fri, 11 Dec 2020 00:43:37 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:29ade854e0dcedde295dd89890d45271e9df839e42124558eb5283508ca70f5c`  
		Last Modified: Tue, 17 Nov 2020 20:32:02 GMT  
		Size: 25.9 MB (25862532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dc9211a1c3bffc7a39cf8c3174d7f7de9329295b6474bdd8d72ab9644fff94e`  
		Last Modified: Fri, 11 Dec 2020 00:44:08 GMT  
		Size: 255.9 KB (255921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc83dcb6b6716a71be07cbacf280c77737ea97150be83a369ab6b491deef0418`  
		Last Modified: Fri, 11 Dec 2020 00:44:18 GMT  
		Size: 31.7 MB (31720201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:605dbd553726e1c842cd862bd130bda02b5dd2dd87c1c7be25c140457394ab24`  
		Last Modified: Fri, 11 Dec 2020 00:45:18 GMT  
		Size: 156.6 MB (156581604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12` - linux; 386

```console
$ docker pull mono@sha256:aceece2f87de6b14a1d759171c3298d106329198865762c07512328c4ea9c9f1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.6 MB (241638109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77f8c8e180ef4b56a8317b0e7f56bf15637e67f9cbe2765dd931c94901200840`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:19:58 GMT
ADD file:b17dfa607fcb298beb9c58bfbb8b9b0743ceb385875776c56269db2506840edf in / 
# Tue, 17 Nov 2020 20:19:58 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 00:38:44 GMT
ENV MONO_VERSION=6.12.0.107
# Fri, 11 Dec 2020 00:38:53 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 11 Dec 2020 00:39:26 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Fri, 11 Dec 2020 00:41:19 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:e8e82c9fb36b8f3a9b8f18fe1d88e4d425d5c45968e3f2e94cdbb1255feb4878`  
		Last Modified: Tue, 17 Nov 2020 20:26:45 GMT  
		Size: 27.8 MB (27766186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddafc845098e9a2a66850e53bdcfaa1173904510dc84bf2c6910925a4c3c045a`  
		Last Modified: Fri, 11 Dec 2020 00:41:47 GMT  
		Size: 255.8 KB (255802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18dbe8684dd9be0f4cf763eb0f7f7c137403ef2666575c628e10ed25e8938eef`  
		Last Modified: Fri, 11 Dec 2020 00:42:06 GMT  
		Size: 71.1 MB (71105266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b01d92c97d300c373e938a159f2198670e8486deadc76da9641fc06fccc49e8`  
		Last Modified: Fri, 11 Dec 2020 00:43:01 GMT  
		Size: 142.5 MB (142510855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12` - linux; ppc64le

```console
$ docker pull mono@sha256:bfa4cad02f57da9b1a2aab29e864a791c4cd652fabd5640a7088ae867c848db7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.3 MB (203322144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c96fb8cd25f6f2747352c471e02a0dd9f40eb53eb73c9324267b695fcd44637`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 23:23:06 GMT
ADD file:49cd8b08964980901349e1f3d6cb34abd8145dea6e6d9ab83502452281ac73ca in / 
# Tue, 17 Nov 2020 23:23:11 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 02:25:07 GMT
ENV MONO_VERSION=6.12.0.107
# Fri, 11 Dec 2020 02:27:07 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 11 Dec 2020 02:29:15 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Fri, 11 Dec 2020 02:38:24 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:d79345c10f03543bff3982aedb35a18ba18626c0074014387ff5e1dc14474e2b`  
		Last Modified: Tue, 17 Nov 2020 23:32:54 GMT  
		Size: 30.5 MB (30531702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:733aef212d5acea62b32e63a1a43fed9cb16944c22591c847bf1c02c81f2c825`  
		Last Modified: Fri, 11 Dec 2020 02:39:11 GMT  
		Size: 256.2 KB (256158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cad78cba8d670a26f74487900565a5e53b2b5d740157a89bd6eb41e697f0ae30`  
		Last Modified: Fri, 11 Dec 2020 02:39:17 GMT  
		Size: 29.3 MB (29311041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d81d40cea93af85e059a41187a7c7944c7f55d440959b55db9f5ad40f1eb4f8`  
		Last Modified: Fri, 11 Dec 2020 02:40:11 GMT  
		Size: 143.2 MB (143223243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.12.0`

```console
$ docker pull mono@sha256:d431506c2d11911eb64c2d9f39659db0e169497e109d6267192a60be06f7b44b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:6.12.0` - linux; amd64

```console
$ docker pull mono@sha256:96b84ede5d78d547e62b92d0825eee974cfbacc9f47b9f75af69478695a58d13
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.9 MB (235853741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:822277e848fa10c7140c66c299eba734801c87387ddc178735d778ac15424d98`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:21:17 GMT
ADD file:d2abb0e4e7ac1773741f51f57d3a0b8ffc7907348842d773f8c341ba17f856d5 in / 
# Tue, 17 Nov 2020 20:21:17 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 01:19:50 GMT
ENV MONO_VERSION=6.12.0.107
# Fri, 11 Dec 2020 01:19:57 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 11 Dec 2020 01:20:26 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Fri, 11 Dec 2020 01:26:13 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:852e50cd189dfeb54d97680d9fa6bed21a6d7d18cfb56d6abfe2de9d7f173795`  
		Last Modified: Tue, 17 Nov 2020 20:27:25 GMT  
		Size: 27.1 MB (27105484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e6233064e514b285c8ae365ea7d55fbf0a713ad2fca931700c8079d6446c49b`  
		Last Modified: Fri, 11 Dec 2020 01:26:51 GMT  
		Size: 255.9 KB (255875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f9ac2c1f775d37886a9bd817e589ee9d4f94498b47c6943859cef15bf40f644`  
		Last Modified: Fri, 11 Dec 2020 01:27:03 GMT  
		Size: 67.1 MB (67079224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f718081e23030a8a5ee7297892ab3243006007a4d3079089e53f7c1a576a5704`  
		Last Modified: Fri, 11 Dec 2020 01:27:38 GMT  
		Size: 141.4 MB (141413158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0` - linux; arm variant v5

```console
$ docker pull mono@sha256:473d4f85ae7cc53f4f40e4cec170ffb02ae051156e692328dc20edab624a0384
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.7 MB (191713047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adb27fc6a3ca19d052ab16220598fea32e5b5376e577a9fabac102703373498d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:20:37 GMT
ADD file:d75cebdc79385debd2d6d1c8c34855d2bd4779b13ee47f76e34c6d8fca037531 in / 
# Tue, 17 Nov 2020 20:20:45 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 00:48:44 GMT
ENV MONO_VERSION=6.12.0.107
# Fri, 11 Dec 2020 00:49:07 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 11 Dec 2020 00:49:53 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Fri, 11 Dec 2020 00:53:25 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:1b8dd2ec17ab788b6ea03a9b6cf68afada9a8692681d29e9795db0abf6554404`  
		Last Modified: Tue, 17 Nov 2020 20:30:33 GMT  
		Size: 24.9 MB (24850311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05baa1a4580b5db26b6e95be46ea7c3c911e02763abc687ff0b7ff1ac8c3d69e`  
		Last Modified: Fri, 11 Dec 2020 00:53:53 GMT  
		Size: 255.9 KB (255949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fcd83802c296fe8f139c457197e375b3de65bebb1f2b2a4f96b337a147d3010`  
		Last Modified: Fri, 11 Dec 2020 00:54:03 GMT  
		Size: 26.5 MB (26499209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd173961b252fccb0b1cb9ce85aeb7fead6cfde53661f8220657d0219c852c93`  
		Last Modified: Fri, 11 Dec 2020 00:55:07 GMT  
		Size: 140.1 MB (140107578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0` - linux; arm variant v7

```console
$ docker pull mono@sha256:6840c9b51b31901fef43c1a0d7a1b9c1ec8326305d87b9b4ba29250cc5d1e318
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.6 MB (187609654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:359606b19f2fa4d122660a6d4e2e26a97fbdf9e60420856ba2749ee9fa8984c5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:21:06 GMT
ADD file:2035658a8d20545ee7b2ab3ee791a371925fca7968ac29435303da24a1378f34 in / 
# Tue, 17 Nov 2020 20:21:10 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 01:19:56 GMT
ENV MONO_VERSION=6.12.0.107
# Fri, 11 Dec 2020 01:20:12 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 11 Dec 2020 01:20:52 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Fri, 11 Dec 2020 01:23:21 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:d5029e4b387017f20ad9f77baf3b81dd41f851d6340363b842a8a1d9786a60a0`  
		Last Modified: Tue, 17 Nov 2020 20:31:46 GMT  
		Size: 22.7 MB (22714186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b10337bd0f9a5533e53c8e57aa108beb3685d96b1f29a24c1945cf8094e9c5da`  
		Last Modified: Fri, 11 Dec 2020 01:23:59 GMT  
		Size: 255.9 KB (255913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0908544f1142db6230e88978959bd9c49919463ca61ea613cda8c14c6e8532f7`  
		Last Modified: Fri, 11 Dec 2020 01:24:09 GMT  
		Size: 25.7 MB (25697558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0bf7204709176636291b8e80c80feb213cf279c6ee49042b457a680a1e67bb0`  
		Last Modified: Fri, 11 Dec 2020 01:25:23 GMT  
		Size: 138.9 MB (138941997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:d9ce20966960efd33ea082f4be5611194898724cb5c2ad35c52df854481cf3e5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.4 MB (214420258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d37443135e41fd61c8c20eb555b7f08dc740c82b8e491b8b30f1621606d2a72f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:23:31 GMT
ADD file:a70d8c01f8f04f36038968567af779883f3b5ba3147b662b7d170d80418bc23c in / 
# Tue, 17 Nov 2020 20:23:32 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 00:40:21 GMT
ENV MONO_VERSION=6.12.0.107
# Fri, 11 Dec 2020 00:40:42 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 11 Dec 2020 00:41:18 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Fri, 11 Dec 2020 00:43:37 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:29ade854e0dcedde295dd89890d45271e9df839e42124558eb5283508ca70f5c`  
		Last Modified: Tue, 17 Nov 2020 20:32:02 GMT  
		Size: 25.9 MB (25862532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dc9211a1c3bffc7a39cf8c3174d7f7de9329295b6474bdd8d72ab9644fff94e`  
		Last Modified: Fri, 11 Dec 2020 00:44:08 GMT  
		Size: 255.9 KB (255921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc83dcb6b6716a71be07cbacf280c77737ea97150be83a369ab6b491deef0418`  
		Last Modified: Fri, 11 Dec 2020 00:44:18 GMT  
		Size: 31.7 MB (31720201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:605dbd553726e1c842cd862bd130bda02b5dd2dd87c1c7be25c140457394ab24`  
		Last Modified: Fri, 11 Dec 2020 00:45:18 GMT  
		Size: 156.6 MB (156581604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0` - linux; 386

```console
$ docker pull mono@sha256:aceece2f87de6b14a1d759171c3298d106329198865762c07512328c4ea9c9f1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.6 MB (241638109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77f8c8e180ef4b56a8317b0e7f56bf15637e67f9cbe2765dd931c94901200840`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:19:58 GMT
ADD file:b17dfa607fcb298beb9c58bfbb8b9b0743ceb385875776c56269db2506840edf in / 
# Tue, 17 Nov 2020 20:19:58 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 00:38:44 GMT
ENV MONO_VERSION=6.12.0.107
# Fri, 11 Dec 2020 00:38:53 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 11 Dec 2020 00:39:26 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Fri, 11 Dec 2020 00:41:19 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:e8e82c9fb36b8f3a9b8f18fe1d88e4d425d5c45968e3f2e94cdbb1255feb4878`  
		Last Modified: Tue, 17 Nov 2020 20:26:45 GMT  
		Size: 27.8 MB (27766186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddafc845098e9a2a66850e53bdcfaa1173904510dc84bf2c6910925a4c3c045a`  
		Last Modified: Fri, 11 Dec 2020 00:41:47 GMT  
		Size: 255.8 KB (255802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18dbe8684dd9be0f4cf763eb0f7f7c137403ef2666575c628e10ed25e8938eef`  
		Last Modified: Fri, 11 Dec 2020 00:42:06 GMT  
		Size: 71.1 MB (71105266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b01d92c97d300c373e938a159f2198670e8486deadc76da9641fc06fccc49e8`  
		Last Modified: Fri, 11 Dec 2020 00:43:01 GMT  
		Size: 142.5 MB (142510855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0` - linux; ppc64le

```console
$ docker pull mono@sha256:bfa4cad02f57da9b1a2aab29e864a791c4cd652fabd5640a7088ae867c848db7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.3 MB (203322144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c96fb8cd25f6f2747352c471e02a0dd9f40eb53eb73c9324267b695fcd44637`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 23:23:06 GMT
ADD file:49cd8b08964980901349e1f3d6cb34abd8145dea6e6d9ab83502452281ac73ca in / 
# Tue, 17 Nov 2020 23:23:11 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 02:25:07 GMT
ENV MONO_VERSION=6.12.0.107
# Fri, 11 Dec 2020 02:27:07 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 11 Dec 2020 02:29:15 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Fri, 11 Dec 2020 02:38:24 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:d79345c10f03543bff3982aedb35a18ba18626c0074014387ff5e1dc14474e2b`  
		Last Modified: Tue, 17 Nov 2020 23:32:54 GMT  
		Size: 30.5 MB (30531702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:733aef212d5acea62b32e63a1a43fed9cb16944c22591c847bf1c02c81f2c825`  
		Last Modified: Fri, 11 Dec 2020 02:39:11 GMT  
		Size: 256.2 KB (256158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cad78cba8d670a26f74487900565a5e53b2b5d740157a89bd6eb41e697f0ae30`  
		Last Modified: Fri, 11 Dec 2020 02:39:17 GMT  
		Size: 29.3 MB (29311041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d81d40cea93af85e059a41187a7c7944c7f55d440959b55db9f5ad40f1eb4f8`  
		Last Modified: Fri, 11 Dec 2020 02:40:11 GMT  
		Size: 143.2 MB (143223243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.12.0.107`

```console
$ docker pull mono@sha256:d431506c2d11911eb64c2d9f39659db0e169497e109d6267192a60be06f7b44b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:6.12.0.107` - linux; amd64

```console
$ docker pull mono@sha256:96b84ede5d78d547e62b92d0825eee974cfbacc9f47b9f75af69478695a58d13
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.9 MB (235853741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:822277e848fa10c7140c66c299eba734801c87387ddc178735d778ac15424d98`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:21:17 GMT
ADD file:d2abb0e4e7ac1773741f51f57d3a0b8ffc7907348842d773f8c341ba17f856d5 in / 
# Tue, 17 Nov 2020 20:21:17 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 01:19:50 GMT
ENV MONO_VERSION=6.12.0.107
# Fri, 11 Dec 2020 01:19:57 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 11 Dec 2020 01:20:26 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Fri, 11 Dec 2020 01:26:13 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:852e50cd189dfeb54d97680d9fa6bed21a6d7d18cfb56d6abfe2de9d7f173795`  
		Last Modified: Tue, 17 Nov 2020 20:27:25 GMT  
		Size: 27.1 MB (27105484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e6233064e514b285c8ae365ea7d55fbf0a713ad2fca931700c8079d6446c49b`  
		Last Modified: Fri, 11 Dec 2020 01:26:51 GMT  
		Size: 255.9 KB (255875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f9ac2c1f775d37886a9bd817e589ee9d4f94498b47c6943859cef15bf40f644`  
		Last Modified: Fri, 11 Dec 2020 01:27:03 GMT  
		Size: 67.1 MB (67079224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f718081e23030a8a5ee7297892ab3243006007a4d3079089e53f7c1a576a5704`  
		Last Modified: Fri, 11 Dec 2020 01:27:38 GMT  
		Size: 141.4 MB (141413158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0.107` - linux; arm variant v5

```console
$ docker pull mono@sha256:473d4f85ae7cc53f4f40e4cec170ffb02ae051156e692328dc20edab624a0384
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.7 MB (191713047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adb27fc6a3ca19d052ab16220598fea32e5b5376e577a9fabac102703373498d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:20:37 GMT
ADD file:d75cebdc79385debd2d6d1c8c34855d2bd4779b13ee47f76e34c6d8fca037531 in / 
# Tue, 17 Nov 2020 20:20:45 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 00:48:44 GMT
ENV MONO_VERSION=6.12.0.107
# Fri, 11 Dec 2020 00:49:07 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 11 Dec 2020 00:49:53 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Fri, 11 Dec 2020 00:53:25 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:1b8dd2ec17ab788b6ea03a9b6cf68afada9a8692681d29e9795db0abf6554404`  
		Last Modified: Tue, 17 Nov 2020 20:30:33 GMT  
		Size: 24.9 MB (24850311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05baa1a4580b5db26b6e95be46ea7c3c911e02763abc687ff0b7ff1ac8c3d69e`  
		Last Modified: Fri, 11 Dec 2020 00:53:53 GMT  
		Size: 255.9 KB (255949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fcd83802c296fe8f139c457197e375b3de65bebb1f2b2a4f96b337a147d3010`  
		Last Modified: Fri, 11 Dec 2020 00:54:03 GMT  
		Size: 26.5 MB (26499209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd173961b252fccb0b1cb9ce85aeb7fead6cfde53661f8220657d0219c852c93`  
		Last Modified: Fri, 11 Dec 2020 00:55:07 GMT  
		Size: 140.1 MB (140107578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0.107` - linux; arm variant v7

```console
$ docker pull mono@sha256:6840c9b51b31901fef43c1a0d7a1b9c1ec8326305d87b9b4ba29250cc5d1e318
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.6 MB (187609654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:359606b19f2fa4d122660a6d4e2e26a97fbdf9e60420856ba2749ee9fa8984c5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:21:06 GMT
ADD file:2035658a8d20545ee7b2ab3ee791a371925fca7968ac29435303da24a1378f34 in / 
# Tue, 17 Nov 2020 20:21:10 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 01:19:56 GMT
ENV MONO_VERSION=6.12.0.107
# Fri, 11 Dec 2020 01:20:12 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 11 Dec 2020 01:20:52 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Fri, 11 Dec 2020 01:23:21 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:d5029e4b387017f20ad9f77baf3b81dd41f851d6340363b842a8a1d9786a60a0`  
		Last Modified: Tue, 17 Nov 2020 20:31:46 GMT  
		Size: 22.7 MB (22714186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b10337bd0f9a5533e53c8e57aa108beb3685d96b1f29a24c1945cf8094e9c5da`  
		Last Modified: Fri, 11 Dec 2020 01:23:59 GMT  
		Size: 255.9 KB (255913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0908544f1142db6230e88978959bd9c49919463ca61ea613cda8c14c6e8532f7`  
		Last Modified: Fri, 11 Dec 2020 01:24:09 GMT  
		Size: 25.7 MB (25697558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0bf7204709176636291b8e80c80feb213cf279c6ee49042b457a680a1e67bb0`  
		Last Modified: Fri, 11 Dec 2020 01:25:23 GMT  
		Size: 138.9 MB (138941997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0.107` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:d9ce20966960efd33ea082f4be5611194898724cb5c2ad35c52df854481cf3e5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.4 MB (214420258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d37443135e41fd61c8c20eb555b7f08dc740c82b8e491b8b30f1621606d2a72f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:23:31 GMT
ADD file:a70d8c01f8f04f36038968567af779883f3b5ba3147b662b7d170d80418bc23c in / 
# Tue, 17 Nov 2020 20:23:32 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 00:40:21 GMT
ENV MONO_VERSION=6.12.0.107
# Fri, 11 Dec 2020 00:40:42 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 11 Dec 2020 00:41:18 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Fri, 11 Dec 2020 00:43:37 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:29ade854e0dcedde295dd89890d45271e9df839e42124558eb5283508ca70f5c`  
		Last Modified: Tue, 17 Nov 2020 20:32:02 GMT  
		Size: 25.9 MB (25862532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dc9211a1c3bffc7a39cf8c3174d7f7de9329295b6474bdd8d72ab9644fff94e`  
		Last Modified: Fri, 11 Dec 2020 00:44:08 GMT  
		Size: 255.9 KB (255921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc83dcb6b6716a71be07cbacf280c77737ea97150be83a369ab6b491deef0418`  
		Last Modified: Fri, 11 Dec 2020 00:44:18 GMT  
		Size: 31.7 MB (31720201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:605dbd553726e1c842cd862bd130bda02b5dd2dd87c1c7be25c140457394ab24`  
		Last Modified: Fri, 11 Dec 2020 00:45:18 GMT  
		Size: 156.6 MB (156581604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0.107` - linux; 386

```console
$ docker pull mono@sha256:aceece2f87de6b14a1d759171c3298d106329198865762c07512328c4ea9c9f1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.6 MB (241638109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77f8c8e180ef4b56a8317b0e7f56bf15637e67f9cbe2765dd931c94901200840`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:19:58 GMT
ADD file:b17dfa607fcb298beb9c58bfbb8b9b0743ceb385875776c56269db2506840edf in / 
# Tue, 17 Nov 2020 20:19:58 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 00:38:44 GMT
ENV MONO_VERSION=6.12.0.107
# Fri, 11 Dec 2020 00:38:53 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 11 Dec 2020 00:39:26 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Fri, 11 Dec 2020 00:41:19 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:e8e82c9fb36b8f3a9b8f18fe1d88e4d425d5c45968e3f2e94cdbb1255feb4878`  
		Last Modified: Tue, 17 Nov 2020 20:26:45 GMT  
		Size: 27.8 MB (27766186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddafc845098e9a2a66850e53bdcfaa1173904510dc84bf2c6910925a4c3c045a`  
		Last Modified: Fri, 11 Dec 2020 00:41:47 GMT  
		Size: 255.8 KB (255802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18dbe8684dd9be0f4cf763eb0f7f7c137403ef2666575c628e10ed25e8938eef`  
		Last Modified: Fri, 11 Dec 2020 00:42:06 GMT  
		Size: 71.1 MB (71105266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b01d92c97d300c373e938a159f2198670e8486deadc76da9641fc06fccc49e8`  
		Last Modified: Fri, 11 Dec 2020 00:43:01 GMT  
		Size: 142.5 MB (142510855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0.107` - linux; ppc64le

```console
$ docker pull mono@sha256:bfa4cad02f57da9b1a2aab29e864a791c4cd652fabd5640a7088ae867c848db7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.3 MB (203322144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c96fb8cd25f6f2747352c471e02a0dd9f40eb53eb73c9324267b695fcd44637`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 23:23:06 GMT
ADD file:49cd8b08964980901349e1f3d6cb34abd8145dea6e6d9ab83502452281ac73ca in / 
# Tue, 17 Nov 2020 23:23:11 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 02:25:07 GMT
ENV MONO_VERSION=6.12.0.107
# Fri, 11 Dec 2020 02:27:07 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 11 Dec 2020 02:29:15 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Fri, 11 Dec 2020 02:38:24 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:d79345c10f03543bff3982aedb35a18ba18626c0074014387ff5e1dc14474e2b`  
		Last Modified: Tue, 17 Nov 2020 23:32:54 GMT  
		Size: 30.5 MB (30531702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:733aef212d5acea62b32e63a1a43fed9cb16944c22591c847bf1c02c81f2c825`  
		Last Modified: Fri, 11 Dec 2020 02:39:11 GMT  
		Size: 256.2 KB (256158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cad78cba8d670a26f74487900565a5e53b2b5d740157a89bd6eb41e697f0ae30`  
		Last Modified: Fri, 11 Dec 2020 02:39:17 GMT  
		Size: 29.3 MB (29311041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d81d40cea93af85e059a41187a7c7944c7f55d440959b55db9f5ad40f1eb4f8`  
		Last Modified: Fri, 11 Dec 2020 02:40:11 GMT  
		Size: 143.2 MB (143223243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.12.0.107-slim`

```console
$ docker pull mono@sha256:be9a5ff6178824d7124f9e4d39a194f410e5a44ed57d59545001e7c0f84543a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:6.12.0.107-slim` - linux; amd64

```console
$ docker pull mono@sha256:1eb171450dd6701ff0da96ad36a467fa7a40dd16bced4c759472821c59139a28
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94440583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be26e7ac872c9fc5fb61ab40207c6d3b1d121dfbb7430a08ddb0840dd0bf2184`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:21:17 GMT
ADD file:d2abb0e4e7ac1773741f51f57d3a0b8ffc7907348842d773f8c341ba17f856d5 in / 
# Tue, 17 Nov 2020 20:21:17 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 01:19:50 GMT
ENV MONO_VERSION=6.12.0.107
# Fri, 11 Dec 2020 01:19:57 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 11 Dec 2020 01:20:26 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:852e50cd189dfeb54d97680d9fa6bed21a6d7d18cfb56d6abfe2de9d7f173795`  
		Last Modified: Tue, 17 Nov 2020 20:27:25 GMT  
		Size: 27.1 MB (27105484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e6233064e514b285c8ae365ea7d55fbf0a713ad2fca931700c8079d6446c49b`  
		Last Modified: Fri, 11 Dec 2020 01:26:51 GMT  
		Size: 255.9 KB (255875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f9ac2c1f775d37886a9bd817e589ee9d4f94498b47c6943859cef15bf40f644`  
		Last Modified: Fri, 11 Dec 2020 01:27:03 GMT  
		Size: 67.1 MB (67079224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0.107-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:4f5d32d9ec766bfaf329547b4755bfe02eefb4d45046cbdfa491b9feed6d23fc
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51605469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecb6ab1e05a0017d8e4c4beaf5fabda95e3a4f4db3453015c92807fbd2af6d7f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:20:37 GMT
ADD file:d75cebdc79385debd2d6d1c8c34855d2bd4779b13ee47f76e34c6d8fca037531 in / 
# Tue, 17 Nov 2020 20:20:45 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 00:48:44 GMT
ENV MONO_VERSION=6.12.0.107
# Fri, 11 Dec 2020 00:49:07 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 11 Dec 2020 00:49:53 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:1b8dd2ec17ab788b6ea03a9b6cf68afada9a8692681d29e9795db0abf6554404`  
		Last Modified: Tue, 17 Nov 2020 20:30:33 GMT  
		Size: 24.9 MB (24850311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05baa1a4580b5db26b6e95be46ea7c3c911e02763abc687ff0b7ff1ac8c3d69e`  
		Last Modified: Fri, 11 Dec 2020 00:53:53 GMT  
		Size: 255.9 KB (255949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fcd83802c296fe8f139c457197e375b3de65bebb1f2b2a4f96b337a147d3010`  
		Last Modified: Fri, 11 Dec 2020 00:54:03 GMT  
		Size: 26.5 MB (26499209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0.107-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:ac90fe185cfd4867438e47c398161782a84cf4cd9850b5b07d2114728946bb3d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48667657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ad2823f93454f90ae1046833ea5666c8561336e25fb317c8da2c1eebf14e1c1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:21:06 GMT
ADD file:2035658a8d20545ee7b2ab3ee791a371925fca7968ac29435303da24a1378f34 in / 
# Tue, 17 Nov 2020 20:21:10 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 01:19:56 GMT
ENV MONO_VERSION=6.12.0.107
# Fri, 11 Dec 2020 01:20:12 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 11 Dec 2020 01:20:52 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:d5029e4b387017f20ad9f77baf3b81dd41f851d6340363b842a8a1d9786a60a0`  
		Last Modified: Tue, 17 Nov 2020 20:31:46 GMT  
		Size: 22.7 MB (22714186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b10337bd0f9a5533e53c8e57aa108beb3685d96b1f29a24c1945cf8094e9c5da`  
		Last Modified: Fri, 11 Dec 2020 01:23:59 GMT  
		Size: 255.9 KB (255913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0908544f1142db6230e88978959bd9c49919463ca61ea613cda8c14c6e8532f7`  
		Last Modified: Fri, 11 Dec 2020 01:24:09 GMT  
		Size: 25.7 MB (25697558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0.107-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:0e552be64b73e95995178f3530c280d8b01a775904f49958c49105ef6f7f8e61
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.8 MB (57838654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3089f8d93db672126a2806d8d9cc50d2bcda4ba3dbaecca6bb9e7e8426eaa201`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:23:31 GMT
ADD file:a70d8c01f8f04f36038968567af779883f3b5ba3147b662b7d170d80418bc23c in / 
# Tue, 17 Nov 2020 20:23:32 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 00:40:21 GMT
ENV MONO_VERSION=6.12.0.107
# Fri, 11 Dec 2020 00:40:42 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 11 Dec 2020 00:41:18 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:29ade854e0dcedde295dd89890d45271e9df839e42124558eb5283508ca70f5c`  
		Last Modified: Tue, 17 Nov 2020 20:32:02 GMT  
		Size: 25.9 MB (25862532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dc9211a1c3bffc7a39cf8c3174d7f7de9329295b6474bdd8d72ab9644fff94e`  
		Last Modified: Fri, 11 Dec 2020 00:44:08 GMT  
		Size: 255.9 KB (255921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc83dcb6b6716a71be07cbacf280c77737ea97150be83a369ab6b491deef0418`  
		Last Modified: Fri, 11 Dec 2020 00:44:18 GMT  
		Size: 31.7 MB (31720201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0.107-slim` - linux; 386

```console
$ docker pull mono@sha256:922f4e6c316eab63210eb6f2f45686bfa934cd76a3b57e0a6ddc887bc4665dc2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.1 MB (99127254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3340aca337949030e11c7970bba606992f53421fdc526f4cebfc013e77c38303`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:19:58 GMT
ADD file:b17dfa607fcb298beb9c58bfbb8b9b0743ceb385875776c56269db2506840edf in / 
# Tue, 17 Nov 2020 20:19:58 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 00:38:44 GMT
ENV MONO_VERSION=6.12.0.107
# Fri, 11 Dec 2020 00:38:53 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 11 Dec 2020 00:39:26 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:e8e82c9fb36b8f3a9b8f18fe1d88e4d425d5c45968e3f2e94cdbb1255feb4878`  
		Last Modified: Tue, 17 Nov 2020 20:26:45 GMT  
		Size: 27.8 MB (27766186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddafc845098e9a2a66850e53bdcfaa1173904510dc84bf2c6910925a4c3c045a`  
		Last Modified: Fri, 11 Dec 2020 00:41:47 GMT  
		Size: 255.8 KB (255802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18dbe8684dd9be0f4cf763eb0f7f7c137403ef2666575c628e10ed25e8938eef`  
		Last Modified: Fri, 11 Dec 2020 00:42:06 GMT  
		Size: 71.1 MB (71105266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0.107-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:04a707304805b1f376c53430168f30cb75ae852b796082517e764214f3aab783
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60098901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ae8340ce5c4eb35b3ef3714e1229ae55cf292aa1ae48516fd26e42743642f66`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 23:23:06 GMT
ADD file:49cd8b08964980901349e1f3d6cb34abd8145dea6e6d9ab83502452281ac73ca in / 
# Tue, 17 Nov 2020 23:23:11 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 02:25:07 GMT
ENV MONO_VERSION=6.12.0.107
# Fri, 11 Dec 2020 02:27:07 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 11 Dec 2020 02:29:15 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:d79345c10f03543bff3982aedb35a18ba18626c0074014387ff5e1dc14474e2b`  
		Last Modified: Tue, 17 Nov 2020 23:32:54 GMT  
		Size: 30.5 MB (30531702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:733aef212d5acea62b32e63a1a43fed9cb16944c22591c847bf1c02c81f2c825`  
		Last Modified: Fri, 11 Dec 2020 02:39:11 GMT  
		Size: 256.2 KB (256158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cad78cba8d670a26f74487900565a5e53b2b5d740157a89bd6eb41e697f0ae30`  
		Last Modified: Fri, 11 Dec 2020 02:39:17 GMT  
		Size: 29.3 MB (29311041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.12.0-slim`

```console
$ docker pull mono@sha256:be9a5ff6178824d7124f9e4d39a194f410e5a44ed57d59545001e7c0f84543a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:6.12.0-slim` - linux; amd64

```console
$ docker pull mono@sha256:1eb171450dd6701ff0da96ad36a467fa7a40dd16bced4c759472821c59139a28
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94440583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be26e7ac872c9fc5fb61ab40207c6d3b1d121dfbb7430a08ddb0840dd0bf2184`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:21:17 GMT
ADD file:d2abb0e4e7ac1773741f51f57d3a0b8ffc7907348842d773f8c341ba17f856d5 in / 
# Tue, 17 Nov 2020 20:21:17 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 01:19:50 GMT
ENV MONO_VERSION=6.12.0.107
# Fri, 11 Dec 2020 01:19:57 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 11 Dec 2020 01:20:26 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:852e50cd189dfeb54d97680d9fa6bed21a6d7d18cfb56d6abfe2de9d7f173795`  
		Last Modified: Tue, 17 Nov 2020 20:27:25 GMT  
		Size: 27.1 MB (27105484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e6233064e514b285c8ae365ea7d55fbf0a713ad2fca931700c8079d6446c49b`  
		Last Modified: Fri, 11 Dec 2020 01:26:51 GMT  
		Size: 255.9 KB (255875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f9ac2c1f775d37886a9bd817e589ee9d4f94498b47c6943859cef15bf40f644`  
		Last Modified: Fri, 11 Dec 2020 01:27:03 GMT  
		Size: 67.1 MB (67079224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:4f5d32d9ec766bfaf329547b4755bfe02eefb4d45046cbdfa491b9feed6d23fc
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51605469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecb6ab1e05a0017d8e4c4beaf5fabda95e3a4f4db3453015c92807fbd2af6d7f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:20:37 GMT
ADD file:d75cebdc79385debd2d6d1c8c34855d2bd4779b13ee47f76e34c6d8fca037531 in / 
# Tue, 17 Nov 2020 20:20:45 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 00:48:44 GMT
ENV MONO_VERSION=6.12.0.107
# Fri, 11 Dec 2020 00:49:07 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 11 Dec 2020 00:49:53 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:1b8dd2ec17ab788b6ea03a9b6cf68afada9a8692681d29e9795db0abf6554404`  
		Last Modified: Tue, 17 Nov 2020 20:30:33 GMT  
		Size: 24.9 MB (24850311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05baa1a4580b5db26b6e95be46ea7c3c911e02763abc687ff0b7ff1ac8c3d69e`  
		Last Modified: Fri, 11 Dec 2020 00:53:53 GMT  
		Size: 255.9 KB (255949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fcd83802c296fe8f139c457197e375b3de65bebb1f2b2a4f96b337a147d3010`  
		Last Modified: Fri, 11 Dec 2020 00:54:03 GMT  
		Size: 26.5 MB (26499209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:ac90fe185cfd4867438e47c398161782a84cf4cd9850b5b07d2114728946bb3d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48667657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ad2823f93454f90ae1046833ea5666c8561336e25fb317c8da2c1eebf14e1c1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:21:06 GMT
ADD file:2035658a8d20545ee7b2ab3ee791a371925fca7968ac29435303da24a1378f34 in / 
# Tue, 17 Nov 2020 20:21:10 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 01:19:56 GMT
ENV MONO_VERSION=6.12.0.107
# Fri, 11 Dec 2020 01:20:12 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 11 Dec 2020 01:20:52 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:d5029e4b387017f20ad9f77baf3b81dd41f851d6340363b842a8a1d9786a60a0`  
		Last Modified: Tue, 17 Nov 2020 20:31:46 GMT  
		Size: 22.7 MB (22714186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b10337bd0f9a5533e53c8e57aa108beb3685d96b1f29a24c1945cf8094e9c5da`  
		Last Modified: Fri, 11 Dec 2020 01:23:59 GMT  
		Size: 255.9 KB (255913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0908544f1142db6230e88978959bd9c49919463ca61ea613cda8c14c6e8532f7`  
		Last Modified: Fri, 11 Dec 2020 01:24:09 GMT  
		Size: 25.7 MB (25697558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:0e552be64b73e95995178f3530c280d8b01a775904f49958c49105ef6f7f8e61
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.8 MB (57838654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3089f8d93db672126a2806d8d9cc50d2bcda4ba3dbaecca6bb9e7e8426eaa201`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:23:31 GMT
ADD file:a70d8c01f8f04f36038968567af779883f3b5ba3147b662b7d170d80418bc23c in / 
# Tue, 17 Nov 2020 20:23:32 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 00:40:21 GMT
ENV MONO_VERSION=6.12.0.107
# Fri, 11 Dec 2020 00:40:42 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 11 Dec 2020 00:41:18 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:29ade854e0dcedde295dd89890d45271e9df839e42124558eb5283508ca70f5c`  
		Last Modified: Tue, 17 Nov 2020 20:32:02 GMT  
		Size: 25.9 MB (25862532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dc9211a1c3bffc7a39cf8c3174d7f7de9329295b6474bdd8d72ab9644fff94e`  
		Last Modified: Fri, 11 Dec 2020 00:44:08 GMT  
		Size: 255.9 KB (255921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc83dcb6b6716a71be07cbacf280c77737ea97150be83a369ab6b491deef0418`  
		Last Modified: Fri, 11 Dec 2020 00:44:18 GMT  
		Size: 31.7 MB (31720201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0-slim` - linux; 386

```console
$ docker pull mono@sha256:922f4e6c316eab63210eb6f2f45686bfa934cd76a3b57e0a6ddc887bc4665dc2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.1 MB (99127254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3340aca337949030e11c7970bba606992f53421fdc526f4cebfc013e77c38303`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:19:58 GMT
ADD file:b17dfa607fcb298beb9c58bfbb8b9b0743ceb385875776c56269db2506840edf in / 
# Tue, 17 Nov 2020 20:19:58 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 00:38:44 GMT
ENV MONO_VERSION=6.12.0.107
# Fri, 11 Dec 2020 00:38:53 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 11 Dec 2020 00:39:26 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:e8e82c9fb36b8f3a9b8f18fe1d88e4d425d5c45968e3f2e94cdbb1255feb4878`  
		Last Modified: Tue, 17 Nov 2020 20:26:45 GMT  
		Size: 27.8 MB (27766186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddafc845098e9a2a66850e53bdcfaa1173904510dc84bf2c6910925a4c3c045a`  
		Last Modified: Fri, 11 Dec 2020 00:41:47 GMT  
		Size: 255.8 KB (255802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18dbe8684dd9be0f4cf763eb0f7f7c137403ef2666575c628e10ed25e8938eef`  
		Last Modified: Fri, 11 Dec 2020 00:42:06 GMT  
		Size: 71.1 MB (71105266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:04a707304805b1f376c53430168f30cb75ae852b796082517e764214f3aab783
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60098901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ae8340ce5c4eb35b3ef3714e1229ae55cf292aa1ae48516fd26e42743642f66`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 23:23:06 GMT
ADD file:49cd8b08964980901349e1f3d6cb34abd8145dea6e6d9ab83502452281ac73ca in / 
# Tue, 17 Nov 2020 23:23:11 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 02:25:07 GMT
ENV MONO_VERSION=6.12.0.107
# Fri, 11 Dec 2020 02:27:07 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 11 Dec 2020 02:29:15 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:d79345c10f03543bff3982aedb35a18ba18626c0074014387ff5e1dc14474e2b`  
		Last Modified: Tue, 17 Nov 2020 23:32:54 GMT  
		Size: 30.5 MB (30531702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:733aef212d5acea62b32e63a1a43fed9cb16944c22591c847bf1c02c81f2c825`  
		Last Modified: Fri, 11 Dec 2020 02:39:11 GMT  
		Size: 256.2 KB (256158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cad78cba8d670a26f74487900565a5e53b2b5d740157a89bd6eb41e697f0ae30`  
		Last Modified: Fri, 11 Dec 2020 02:39:17 GMT  
		Size: 29.3 MB (29311041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.12-slim`

```console
$ docker pull mono@sha256:be9a5ff6178824d7124f9e4d39a194f410e5a44ed57d59545001e7c0f84543a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:6.12-slim` - linux; amd64

```console
$ docker pull mono@sha256:1eb171450dd6701ff0da96ad36a467fa7a40dd16bced4c759472821c59139a28
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94440583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be26e7ac872c9fc5fb61ab40207c6d3b1d121dfbb7430a08ddb0840dd0bf2184`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:21:17 GMT
ADD file:d2abb0e4e7ac1773741f51f57d3a0b8ffc7907348842d773f8c341ba17f856d5 in / 
# Tue, 17 Nov 2020 20:21:17 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 01:19:50 GMT
ENV MONO_VERSION=6.12.0.107
# Fri, 11 Dec 2020 01:19:57 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 11 Dec 2020 01:20:26 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:852e50cd189dfeb54d97680d9fa6bed21a6d7d18cfb56d6abfe2de9d7f173795`  
		Last Modified: Tue, 17 Nov 2020 20:27:25 GMT  
		Size: 27.1 MB (27105484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e6233064e514b285c8ae365ea7d55fbf0a713ad2fca931700c8079d6446c49b`  
		Last Modified: Fri, 11 Dec 2020 01:26:51 GMT  
		Size: 255.9 KB (255875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f9ac2c1f775d37886a9bd817e589ee9d4f94498b47c6943859cef15bf40f644`  
		Last Modified: Fri, 11 Dec 2020 01:27:03 GMT  
		Size: 67.1 MB (67079224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:4f5d32d9ec766bfaf329547b4755bfe02eefb4d45046cbdfa491b9feed6d23fc
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51605469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecb6ab1e05a0017d8e4c4beaf5fabda95e3a4f4db3453015c92807fbd2af6d7f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:20:37 GMT
ADD file:d75cebdc79385debd2d6d1c8c34855d2bd4779b13ee47f76e34c6d8fca037531 in / 
# Tue, 17 Nov 2020 20:20:45 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 00:48:44 GMT
ENV MONO_VERSION=6.12.0.107
# Fri, 11 Dec 2020 00:49:07 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 11 Dec 2020 00:49:53 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:1b8dd2ec17ab788b6ea03a9b6cf68afada9a8692681d29e9795db0abf6554404`  
		Last Modified: Tue, 17 Nov 2020 20:30:33 GMT  
		Size: 24.9 MB (24850311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05baa1a4580b5db26b6e95be46ea7c3c911e02763abc687ff0b7ff1ac8c3d69e`  
		Last Modified: Fri, 11 Dec 2020 00:53:53 GMT  
		Size: 255.9 KB (255949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fcd83802c296fe8f139c457197e375b3de65bebb1f2b2a4f96b337a147d3010`  
		Last Modified: Fri, 11 Dec 2020 00:54:03 GMT  
		Size: 26.5 MB (26499209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:ac90fe185cfd4867438e47c398161782a84cf4cd9850b5b07d2114728946bb3d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48667657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ad2823f93454f90ae1046833ea5666c8561336e25fb317c8da2c1eebf14e1c1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:21:06 GMT
ADD file:2035658a8d20545ee7b2ab3ee791a371925fca7968ac29435303da24a1378f34 in / 
# Tue, 17 Nov 2020 20:21:10 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 01:19:56 GMT
ENV MONO_VERSION=6.12.0.107
# Fri, 11 Dec 2020 01:20:12 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 11 Dec 2020 01:20:52 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:d5029e4b387017f20ad9f77baf3b81dd41f851d6340363b842a8a1d9786a60a0`  
		Last Modified: Tue, 17 Nov 2020 20:31:46 GMT  
		Size: 22.7 MB (22714186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b10337bd0f9a5533e53c8e57aa108beb3685d96b1f29a24c1945cf8094e9c5da`  
		Last Modified: Fri, 11 Dec 2020 01:23:59 GMT  
		Size: 255.9 KB (255913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0908544f1142db6230e88978959bd9c49919463ca61ea613cda8c14c6e8532f7`  
		Last Modified: Fri, 11 Dec 2020 01:24:09 GMT  
		Size: 25.7 MB (25697558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:0e552be64b73e95995178f3530c280d8b01a775904f49958c49105ef6f7f8e61
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.8 MB (57838654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3089f8d93db672126a2806d8d9cc50d2bcda4ba3dbaecca6bb9e7e8426eaa201`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:23:31 GMT
ADD file:a70d8c01f8f04f36038968567af779883f3b5ba3147b662b7d170d80418bc23c in / 
# Tue, 17 Nov 2020 20:23:32 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 00:40:21 GMT
ENV MONO_VERSION=6.12.0.107
# Fri, 11 Dec 2020 00:40:42 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 11 Dec 2020 00:41:18 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:29ade854e0dcedde295dd89890d45271e9df839e42124558eb5283508ca70f5c`  
		Last Modified: Tue, 17 Nov 2020 20:32:02 GMT  
		Size: 25.9 MB (25862532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dc9211a1c3bffc7a39cf8c3174d7f7de9329295b6474bdd8d72ab9644fff94e`  
		Last Modified: Fri, 11 Dec 2020 00:44:08 GMT  
		Size: 255.9 KB (255921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc83dcb6b6716a71be07cbacf280c77737ea97150be83a369ab6b491deef0418`  
		Last Modified: Fri, 11 Dec 2020 00:44:18 GMT  
		Size: 31.7 MB (31720201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12-slim` - linux; 386

```console
$ docker pull mono@sha256:922f4e6c316eab63210eb6f2f45686bfa934cd76a3b57e0a6ddc887bc4665dc2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.1 MB (99127254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3340aca337949030e11c7970bba606992f53421fdc526f4cebfc013e77c38303`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:19:58 GMT
ADD file:b17dfa607fcb298beb9c58bfbb8b9b0743ceb385875776c56269db2506840edf in / 
# Tue, 17 Nov 2020 20:19:58 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 00:38:44 GMT
ENV MONO_VERSION=6.12.0.107
# Fri, 11 Dec 2020 00:38:53 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 11 Dec 2020 00:39:26 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:e8e82c9fb36b8f3a9b8f18fe1d88e4d425d5c45968e3f2e94cdbb1255feb4878`  
		Last Modified: Tue, 17 Nov 2020 20:26:45 GMT  
		Size: 27.8 MB (27766186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddafc845098e9a2a66850e53bdcfaa1173904510dc84bf2c6910925a4c3c045a`  
		Last Modified: Fri, 11 Dec 2020 00:41:47 GMT  
		Size: 255.8 KB (255802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18dbe8684dd9be0f4cf763eb0f7f7c137403ef2666575c628e10ed25e8938eef`  
		Last Modified: Fri, 11 Dec 2020 00:42:06 GMT  
		Size: 71.1 MB (71105266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:04a707304805b1f376c53430168f30cb75ae852b796082517e764214f3aab783
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60098901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ae8340ce5c4eb35b3ef3714e1229ae55cf292aa1ae48516fd26e42743642f66`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 23:23:06 GMT
ADD file:49cd8b08964980901349e1f3d6cb34abd8145dea6e6d9ab83502452281ac73ca in / 
# Tue, 17 Nov 2020 23:23:11 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 02:25:07 GMT
ENV MONO_VERSION=6.12.0.107
# Fri, 11 Dec 2020 02:27:07 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 11 Dec 2020 02:29:15 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:d79345c10f03543bff3982aedb35a18ba18626c0074014387ff5e1dc14474e2b`  
		Last Modified: Tue, 17 Nov 2020 23:32:54 GMT  
		Size: 30.5 MB (30531702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:733aef212d5acea62b32e63a1a43fed9cb16944c22591c847bf1c02c81f2c825`  
		Last Modified: Fri, 11 Dec 2020 02:39:11 GMT  
		Size: 256.2 KB (256158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cad78cba8d670a26f74487900565a5e53b2b5d740157a89bd6eb41e697f0ae30`  
		Last Modified: Fri, 11 Dec 2020 02:39:17 GMT  
		Size: 29.3 MB (29311041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6-slim`

```console
$ docker pull mono@sha256:be9a5ff6178824d7124f9e4d39a194f410e5a44ed57d59545001e7c0f84543a6
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
$ docker pull mono@sha256:1eb171450dd6701ff0da96ad36a467fa7a40dd16bced4c759472821c59139a28
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94440583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be26e7ac872c9fc5fb61ab40207c6d3b1d121dfbb7430a08ddb0840dd0bf2184`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:21:17 GMT
ADD file:d2abb0e4e7ac1773741f51f57d3a0b8ffc7907348842d773f8c341ba17f856d5 in / 
# Tue, 17 Nov 2020 20:21:17 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 01:19:50 GMT
ENV MONO_VERSION=6.12.0.107
# Fri, 11 Dec 2020 01:19:57 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 11 Dec 2020 01:20:26 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:852e50cd189dfeb54d97680d9fa6bed21a6d7d18cfb56d6abfe2de9d7f173795`  
		Last Modified: Tue, 17 Nov 2020 20:27:25 GMT  
		Size: 27.1 MB (27105484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e6233064e514b285c8ae365ea7d55fbf0a713ad2fca931700c8079d6446c49b`  
		Last Modified: Fri, 11 Dec 2020 01:26:51 GMT  
		Size: 255.9 KB (255875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f9ac2c1f775d37886a9bd817e589ee9d4f94498b47c6943859cef15bf40f644`  
		Last Modified: Fri, 11 Dec 2020 01:27:03 GMT  
		Size: 67.1 MB (67079224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:4f5d32d9ec766bfaf329547b4755bfe02eefb4d45046cbdfa491b9feed6d23fc
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51605469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecb6ab1e05a0017d8e4c4beaf5fabda95e3a4f4db3453015c92807fbd2af6d7f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:20:37 GMT
ADD file:d75cebdc79385debd2d6d1c8c34855d2bd4779b13ee47f76e34c6d8fca037531 in / 
# Tue, 17 Nov 2020 20:20:45 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 00:48:44 GMT
ENV MONO_VERSION=6.12.0.107
# Fri, 11 Dec 2020 00:49:07 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 11 Dec 2020 00:49:53 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:1b8dd2ec17ab788b6ea03a9b6cf68afada9a8692681d29e9795db0abf6554404`  
		Last Modified: Tue, 17 Nov 2020 20:30:33 GMT  
		Size: 24.9 MB (24850311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05baa1a4580b5db26b6e95be46ea7c3c911e02763abc687ff0b7ff1ac8c3d69e`  
		Last Modified: Fri, 11 Dec 2020 00:53:53 GMT  
		Size: 255.9 KB (255949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fcd83802c296fe8f139c457197e375b3de65bebb1f2b2a4f96b337a147d3010`  
		Last Modified: Fri, 11 Dec 2020 00:54:03 GMT  
		Size: 26.5 MB (26499209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:ac90fe185cfd4867438e47c398161782a84cf4cd9850b5b07d2114728946bb3d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48667657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ad2823f93454f90ae1046833ea5666c8561336e25fb317c8da2c1eebf14e1c1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:21:06 GMT
ADD file:2035658a8d20545ee7b2ab3ee791a371925fca7968ac29435303da24a1378f34 in / 
# Tue, 17 Nov 2020 20:21:10 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 01:19:56 GMT
ENV MONO_VERSION=6.12.0.107
# Fri, 11 Dec 2020 01:20:12 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 11 Dec 2020 01:20:52 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:d5029e4b387017f20ad9f77baf3b81dd41f851d6340363b842a8a1d9786a60a0`  
		Last Modified: Tue, 17 Nov 2020 20:31:46 GMT  
		Size: 22.7 MB (22714186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b10337bd0f9a5533e53c8e57aa108beb3685d96b1f29a24c1945cf8094e9c5da`  
		Last Modified: Fri, 11 Dec 2020 01:23:59 GMT  
		Size: 255.9 KB (255913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0908544f1142db6230e88978959bd9c49919463ca61ea613cda8c14c6e8532f7`  
		Last Modified: Fri, 11 Dec 2020 01:24:09 GMT  
		Size: 25.7 MB (25697558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:0e552be64b73e95995178f3530c280d8b01a775904f49958c49105ef6f7f8e61
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.8 MB (57838654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3089f8d93db672126a2806d8d9cc50d2bcda4ba3dbaecca6bb9e7e8426eaa201`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:23:31 GMT
ADD file:a70d8c01f8f04f36038968567af779883f3b5ba3147b662b7d170d80418bc23c in / 
# Tue, 17 Nov 2020 20:23:32 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 00:40:21 GMT
ENV MONO_VERSION=6.12.0.107
# Fri, 11 Dec 2020 00:40:42 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 11 Dec 2020 00:41:18 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:29ade854e0dcedde295dd89890d45271e9df839e42124558eb5283508ca70f5c`  
		Last Modified: Tue, 17 Nov 2020 20:32:02 GMT  
		Size: 25.9 MB (25862532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dc9211a1c3bffc7a39cf8c3174d7f7de9329295b6474bdd8d72ab9644fff94e`  
		Last Modified: Fri, 11 Dec 2020 00:44:08 GMT  
		Size: 255.9 KB (255921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc83dcb6b6716a71be07cbacf280c77737ea97150be83a369ab6b491deef0418`  
		Last Modified: Fri, 11 Dec 2020 00:44:18 GMT  
		Size: 31.7 MB (31720201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6-slim` - linux; 386

```console
$ docker pull mono@sha256:922f4e6c316eab63210eb6f2f45686bfa934cd76a3b57e0a6ddc887bc4665dc2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.1 MB (99127254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3340aca337949030e11c7970bba606992f53421fdc526f4cebfc013e77c38303`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:19:58 GMT
ADD file:b17dfa607fcb298beb9c58bfbb8b9b0743ceb385875776c56269db2506840edf in / 
# Tue, 17 Nov 2020 20:19:58 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 00:38:44 GMT
ENV MONO_VERSION=6.12.0.107
# Fri, 11 Dec 2020 00:38:53 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 11 Dec 2020 00:39:26 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:e8e82c9fb36b8f3a9b8f18fe1d88e4d425d5c45968e3f2e94cdbb1255feb4878`  
		Last Modified: Tue, 17 Nov 2020 20:26:45 GMT  
		Size: 27.8 MB (27766186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddafc845098e9a2a66850e53bdcfaa1173904510dc84bf2c6910925a4c3c045a`  
		Last Modified: Fri, 11 Dec 2020 00:41:47 GMT  
		Size: 255.8 KB (255802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18dbe8684dd9be0f4cf763eb0f7f7c137403ef2666575c628e10ed25e8938eef`  
		Last Modified: Fri, 11 Dec 2020 00:42:06 GMT  
		Size: 71.1 MB (71105266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:04a707304805b1f376c53430168f30cb75ae852b796082517e764214f3aab783
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60098901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ae8340ce5c4eb35b3ef3714e1229ae55cf292aa1ae48516fd26e42743642f66`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 23:23:06 GMT
ADD file:49cd8b08964980901349e1f3d6cb34abd8145dea6e6d9ab83502452281ac73ca in / 
# Tue, 17 Nov 2020 23:23:11 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 02:25:07 GMT
ENV MONO_VERSION=6.12.0.107
# Fri, 11 Dec 2020 02:27:07 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 11 Dec 2020 02:29:15 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:d79345c10f03543bff3982aedb35a18ba18626c0074014387ff5e1dc14474e2b`  
		Last Modified: Tue, 17 Nov 2020 23:32:54 GMT  
		Size: 30.5 MB (30531702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:733aef212d5acea62b32e63a1a43fed9cb16944c22591c847bf1c02c81f2c825`  
		Last Modified: Fri, 11 Dec 2020 02:39:11 GMT  
		Size: 256.2 KB (256158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cad78cba8d670a26f74487900565a5e53b2b5d740157a89bd6eb41e697f0ae30`  
		Last Modified: Fri, 11 Dec 2020 02:39:17 GMT  
		Size: 29.3 MB (29311041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:latest`

```console
$ docker pull mono@sha256:d431506c2d11911eb64c2d9f39659db0e169497e109d6267192a60be06f7b44b
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
$ docker pull mono@sha256:96b84ede5d78d547e62b92d0825eee974cfbacc9f47b9f75af69478695a58d13
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.9 MB (235853741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:822277e848fa10c7140c66c299eba734801c87387ddc178735d778ac15424d98`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:21:17 GMT
ADD file:d2abb0e4e7ac1773741f51f57d3a0b8ffc7907348842d773f8c341ba17f856d5 in / 
# Tue, 17 Nov 2020 20:21:17 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 01:19:50 GMT
ENV MONO_VERSION=6.12.0.107
# Fri, 11 Dec 2020 01:19:57 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 11 Dec 2020 01:20:26 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Fri, 11 Dec 2020 01:26:13 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:852e50cd189dfeb54d97680d9fa6bed21a6d7d18cfb56d6abfe2de9d7f173795`  
		Last Modified: Tue, 17 Nov 2020 20:27:25 GMT  
		Size: 27.1 MB (27105484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e6233064e514b285c8ae365ea7d55fbf0a713ad2fca931700c8079d6446c49b`  
		Last Modified: Fri, 11 Dec 2020 01:26:51 GMT  
		Size: 255.9 KB (255875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f9ac2c1f775d37886a9bd817e589ee9d4f94498b47c6943859cef15bf40f644`  
		Last Modified: Fri, 11 Dec 2020 01:27:03 GMT  
		Size: 67.1 MB (67079224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f718081e23030a8a5ee7297892ab3243006007a4d3079089e53f7c1a576a5704`  
		Last Modified: Fri, 11 Dec 2020 01:27:38 GMT  
		Size: 141.4 MB (141413158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:latest` - linux; arm variant v5

```console
$ docker pull mono@sha256:473d4f85ae7cc53f4f40e4cec170ffb02ae051156e692328dc20edab624a0384
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.7 MB (191713047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adb27fc6a3ca19d052ab16220598fea32e5b5376e577a9fabac102703373498d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:20:37 GMT
ADD file:d75cebdc79385debd2d6d1c8c34855d2bd4779b13ee47f76e34c6d8fca037531 in / 
# Tue, 17 Nov 2020 20:20:45 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 00:48:44 GMT
ENV MONO_VERSION=6.12.0.107
# Fri, 11 Dec 2020 00:49:07 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 11 Dec 2020 00:49:53 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Fri, 11 Dec 2020 00:53:25 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:1b8dd2ec17ab788b6ea03a9b6cf68afada9a8692681d29e9795db0abf6554404`  
		Last Modified: Tue, 17 Nov 2020 20:30:33 GMT  
		Size: 24.9 MB (24850311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05baa1a4580b5db26b6e95be46ea7c3c911e02763abc687ff0b7ff1ac8c3d69e`  
		Last Modified: Fri, 11 Dec 2020 00:53:53 GMT  
		Size: 255.9 KB (255949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fcd83802c296fe8f139c457197e375b3de65bebb1f2b2a4f96b337a147d3010`  
		Last Modified: Fri, 11 Dec 2020 00:54:03 GMT  
		Size: 26.5 MB (26499209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd173961b252fccb0b1cb9ce85aeb7fead6cfde53661f8220657d0219c852c93`  
		Last Modified: Fri, 11 Dec 2020 00:55:07 GMT  
		Size: 140.1 MB (140107578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:latest` - linux; arm variant v7

```console
$ docker pull mono@sha256:6840c9b51b31901fef43c1a0d7a1b9c1ec8326305d87b9b4ba29250cc5d1e318
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.6 MB (187609654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:359606b19f2fa4d122660a6d4e2e26a97fbdf9e60420856ba2749ee9fa8984c5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:21:06 GMT
ADD file:2035658a8d20545ee7b2ab3ee791a371925fca7968ac29435303da24a1378f34 in / 
# Tue, 17 Nov 2020 20:21:10 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 01:19:56 GMT
ENV MONO_VERSION=6.12.0.107
# Fri, 11 Dec 2020 01:20:12 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 11 Dec 2020 01:20:52 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Fri, 11 Dec 2020 01:23:21 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:d5029e4b387017f20ad9f77baf3b81dd41f851d6340363b842a8a1d9786a60a0`  
		Last Modified: Tue, 17 Nov 2020 20:31:46 GMT  
		Size: 22.7 MB (22714186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b10337bd0f9a5533e53c8e57aa108beb3685d96b1f29a24c1945cf8094e9c5da`  
		Last Modified: Fri, 11 Dec 2020 01:23:59 GMT  
		Size: 255.9 KB (255913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0908544f1142db6230e88978959bd9c49919463ca61ea613cda8c14c6e8532f7`  
		Last Modified: Fri, 11 Dec 2020 01:24:09 GMT  
		Size: 25.7 MB (25697558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0bf7204709176636291b8e80c80feb213cf279c6ee49042b457a680a1e67bb0`  
		Last Modified: Fri, 11 Dec 2020 01:25:23 GMT  
		Size: 138.9 MB (138941997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:latest` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:d9ce20966960efd33ea082f4be5611194898724cb5c2ad35c52df854481cf3e5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.4 MB (214420258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d37443135e41fd61c8c20eb555b7f08dc740c82b8e491b8b30f1621606d2a72f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:23:31 GMT
ADD file:a70d8c01f8f04f36038968567af779883f3b5ba3147b662b7d170d80418bc23c in / 
# Tue, 17 Nov 2020 20:23:32 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 00:40:21 GMT
ENV MONO_VERSION=6.12.0.107
# Fri, 11 Dec 2020 00:40:42 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 11 Dec 2020 00:41:18 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Fri, 11 Dec 2020 00:43:37 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:29ade854e0dcedde295dd89890d45271e9df839e42124558eb5283508ca70f5c`  
		Last Modified: Tue, 17 Nov 2020 20:32:02 GMT  
		Size: 25.9 MB (25862532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dc9211a1c3bffc7a39cf8c3174d7f7de9329295b6474bdd8d72ab9644fff94e`  
		Last Modified: Fri, 11 Dec 2020 00:44:08 GMT  
		Size: 255.9 KB (255921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc83dcb6b6716a71be07cbacf280c77737ea97150be83a369ab6b491deef0418`  
		Last Modified: Fri, 11 Dec 2020 00:44:18 GMT  
		Size: 31.7 MB (31720201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:605dbd553726e1c842cd862bd130bda02b5dd2dd87c1c7be25c140457394ab24`  
		Last Modified: Fri, 11 Dec 2020 00:45:18 GMT  
		Size: 156.6 MB (156581604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:latest` - linux; 386

```console
$ docker pull mono@sha256:aceece2f87de6b14a1d759171c3298d106329198865762c07512328c4ea9c9f1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.6 MB (241638109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77f8c8e180ef4b56a8317b0e7f56bf15637e67f9cbe2765dd931c94901200840`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:19:58 GMT
ADD file:b17dfa607fcb298beb9c58bfbb8b9b0743ceb385875776c56269db2506840edf in / 
# Tue, 17 Nov 2020 20:19:58 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 00:38:44 GMT
ENV MONO_VERSION=6.12.0.107
# Fri, 11 Dec 2020 00:38:53 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 11 Dec 2020 00:39:26 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Fri, 11 Dec 2020 00:41:19 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:e8e82c9fb36b8f3a9b8f18fe1d88e4d425d5c45968e3f2e94cdbb1255feb4878`  
		Last Modified: Tue, 17 Nov 2020 20:26:45 GMT  
		Size: 27.8 MB (27766186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddafc845098e9a2a66850e53bdcfaa1173904510dc84bf2c6910925a4c3c045a`  
		Last Modified: Fri, 11 Dec 2020 00:41:47 GMT  
		Size: 255.8 KB (255802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18dbe8684dd9be0f4cf763eb0f7f7c137403ef2666575c628e10ed25e8938eef`  
		Last Modified: Fri, 11 Dec 2020 00:42:06 GMT  
		Size: 71.1 MB (71105266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b01d92c97d300c373e938a159f2198670e8486deadc76da9641fc06fccc49e8`  
		Last Modified: Fri, 11 Dec 2020 00:43:01 GMT  
		Size: 142.5 MB (142510855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:latest` - linux; ppc64le

```console
$ docker pull mono@sha256:bfa4cad02f57da9b1a2aab29e864a791c4cd652fabd5640a7088ae867c848db7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.3 MB (203322144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c96fb8cd25f6f2747352c471e02a0dd9f40eb53eb73c9324267b695fcd44637`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 23:23:06 GMT
ADD file:49cd8b08964980901349e1f3d6cb34abd8145dea6e6d9ab83502452281ac73ca in / 
# Tue, 17 Nov 2020 23:23:11 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 02:25:07 GMT
ENV MONO_VERSION=6.12.0.107
# Fri, 11 Dec 2020 02:27:07 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 11 Dec 2020 02:29:15 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Fri, 11 Dec 2020 02:38:24 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:d79345c10f03543bff3982aedb35a18ba18626c0074014387ff5e1dc14474e2b`  
		Last Modified: Tue, 17 Nov 2020 23:32:54 GMT  
		Size: 30.5 MB (30531702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:733aef212d5acea62b32e63a1a43fed9cb16944c22591c847bf1c02c81f2c825`  
		Last Modified: Fri, 11 Dec 2020 02:39:11 GMT  
		Size: 256.2 KB (256158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cad78cba8d670a26f74487900565a5e53b2b5d740157a89bd6eb41e697f0ae30`  
		Last Modified: Fri, 11 Dec 2020 02:39:17 GMT  
		Size: 29.3 MB (29311041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d81d40cea93af85e059a41187a7c7944c7f55d440959b55db9f5ad40f1eb4f8`  
		Last Modified: Fri, 11 Dec 2020 02:40:11 GMT  
		Size: 143.2 MB (143223243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:slim`

```console
$ docker pull mono@sha256:be9a5ff6178824d7124f9e4d39a194f410e5a44ed57d59545001e7c0f84543a6
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
$ docker pull mono@sha256:1eb171450dd6701ff0da96ad36a467fa7a40dd16bced4c759472821c59139a28
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94440583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be26e7ac872c9fc5fb61ab40207c6d3b1d121dfbb7430a08ddb0840dd0bf2184`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:21:17 GMT
ADD file:d2abb0e4e7ac1773741f51f57d3a0b8ffc7907348842d773f8c341ba17f856d5 in / 
# Tue, 17 Nov 2020 20:21:17 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 01:19:50 GMT
ENV MONO_VERSION=6.12.0.107
# Fri, 11 Dec 2020 01:19:57 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 11 Dec 2020 01:20:26 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:852e50cd189dfeb54d97680d9fa6bed21a6d7d18cfb56d6abfe2de9d7f173795`  
		Last Modified: Tue, 17 Nov 2020 20:27:25 GMT  
		Size: 27.1 MB (27105484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e6233064e514b285c8ae365ea7d55fbf0a713ad2fca931700c8079d6446c49b`  
		Last Modified: Fri, 11 Dec 2020 01:26:51 GMT  
		Size: 255.9 KB (255875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f9ac2c1f775d37886a9bd817e589ee9d4f94498b47c6943859cef15bf40f644`  
		Last Modified: Fri, 11 Dec 2020 01:27:03 GMT  
		Size: 67.1 MB (67079224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:4f5d32d9ec766bfaf329547b4755bfe02eefb4d45046cbdfa491b9feed6d23fc
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51605469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecb6ab1e05a0017d8e4c4beaf5fabda95e3a4f4db3453015c92807fbd2af6d7f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:20:37 GMT
ADD file:d75cebdc79385debd2d6d1c8c34855d2bd4779b13ee47f76e34c6d8fca037531 in / 
# Tue, 17 Nov 2020 20:20:45 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 00:48:44 GMT
ENV MONO_VERSION=6.12.0.107
# Fri, 11 Dec 2020 00:49:07 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 11 Dec 2020 00:49:53 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:1b8dd2ec17ab788b6ea03a9b6cf68afada9a8692681d29e9795db0abf6554404`  
		Last Modified: Tue, 17 Nov 2020 20:30:33 GMT  
		Size: 24.9 MB (24850311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05baa1a4580b5db26b6e95be46ea7c3c911e02763abc687ff0b7ff1ac8c3d69e`  
		Last Modified: Fri, 11 Dec 2020 00:53:53 GMT  
		Size: 255.9 KB (255949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fcd83802c296fe8f139c457197e375b3de65bebb1f2b2a4f96b337a147d3010`  
		Last Modified: Fri, 11 Dec 2020 00:54:03 GMT  
		Size: 26.5 MB (26499209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:ac90fe185cfd4867438e47c398161782a84cf4cd9850b5b07d2114728946bb3d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48667657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ad2823f93454f90ae1046833ea5666c8561336e25fb317c8da2c1eebf14e1c1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:21:06 GMT
ADD file:2035658a8d20545ee7b2ab3ee791a371925fca7968ac29435303da24a1378f34 in / 
# Tue, 17 Nov 2020 20:21:10 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 01:19:56 GMT
ENV MONO_VERSION=6.12.0.107
# Fri, 11 Dec 2020 01:20:12 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 11 Dec 2020 01:20:52 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:d5029e4b387017f20ad9f77baf3b81dd41f851d6340363b842a8a1d9786a60a0`  
		Last Modified: Tue, 17 Nov 2020 20:31:46 GMT  
		Size: 22.7 MB (22714186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b10337bd0f9a5533e53c8e57aa108beb3685d96b1f29a24c1945cf8094e9c5da`  
		Last Modified: Fri, 11 Dec 2020 01:23:59 GMT  
		Size: 255.9 KB (255913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0908544f1142db6230e88978959bd9c49919463ca61ea613cda8c14c6e8532f7`  
		Last Modified: Fri, 11 Dec 2020 01:24:09 GMT  
		Size: 25.7 MB (25697558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:0e552be64b73e95995178f3530c280d8b01a775904f49958c49105ef6f7f8e61
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.8 MB (57838654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3089f8d93db672126a2806d8d9cc50d2bcda4ba3dbaecca6bb9e7e8426eaa201`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:23:31 GMT
ADD file:a70d8c01f8f04f36038968567af779883f3b5ba3147b662b7d170d80418bc23c in / 
# Tue, 17 Nov 2020 20:23:32 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 00:40:21 GMT
ENV MONO_VERSION=6.12.0.107
# Fri, 11 Dec 2020 00:40:42 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 11 Dec 2020 00:41:18 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:29ade854e0dcedde295dd89890d45271e9df839e42124558eb5283508ca70f5c`  
		Last Modified: Tue, 17 Nov 2020 20:32:02 GMT  
		Size: 25.9 MB (25862532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dc9211a1c3bffc7a39cf8c3174d7f7de9329295b6474bdd8d72ab9644fff94e`  
		Last Modified: Fri, 11 Dec 2020 00:44:08 GMT  
		Size: 255.9 KB (255921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc83dcb6b6716a71be07cbacf280c77737ea97150be83a369ab6b491deef0418`  
		Last Modified: Fri, 11 Dec 2020 00:44:18 GMT  
		Size: 31.7 MB (31720201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:slim` - linux; 386

```console
$ docker pull mono@sha256:922f4e6c316eab63210eb6f2f45686bfa934cd76a3b57e0a6ddc887bc4665dc2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.1 MB (99127254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3340aca337949030e11c7970bba606992f53421fdc526f4cebfc013e77c38303`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:19:58 GMT
ADD file:b17dfa607fcb298beb9c58bfbb8b9b0743ceb385875776c56269db2506840edf in / 
# Tue, 17 Nov 2020 20:19:58 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 00:38:44 GMT
ENV MONO_VERSION=6.12.0.107
# Fri, 11 Dec 2020 00:38:53 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 11 Dec 2020 00:39:26 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:e8e82c9fb36b8f3a9b8f18fe1d88e4d425d5c45968e3f2e94cdbb1255feb4878`  
		Last Modified: Tue, 17 Nov 2020 20:26:45 GMT  
		Size: 27.8 MB (27766186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddafc845098e9a2a66850e53bdcfaa1173904510dc84bf2c6910925a4c3c045a`  
		Last Modified: Fri, 11 Dec 2020 00:41:47 GMT  
		Size: 255.8 KB (255802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18dbe8684dd9be0f4cf763eb0f7f7c137403ef2666575c628e10ed25e8938eef`  
		Last Modified: Fri, 11 Dec 2020 00:42:06 GMT  
		Size: 71.1 MB (71105266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:slim` - linux; ppc64le

```console
$ docker pull mono@sha256:04a707304805b1f376c53430168f30cb75ae852b796082517e764214f3aab783
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60098901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ae8340ce5c4eb35b3ef3714e1229ae55cf292aa1ae48516fd26e42743642f66`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 23:23:06 GMT
ADD file:49cd8b08964980901349e1f3d6cb34abd8145dea6e6d9ab83502452281ac73ca in / 
# Tue, 17 Nov 2020 23:23:11 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 02:25:07 GMT
ENV MONO_VERSION=6.12.0.107
# Fri, 11 Dec 2020 02:27:07 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 11 Dec 2020 02:29:15 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:d79345c10f03543bff3982aedb35a18ba18626c0074014387ff5e1dc14474e2b`  
		Last Modified: Tue, 17 Nov 2020 23:32:54 GMT  
		Size: 30.5 MB (30531702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:733aef212d5acea62b32e63a1a43fed9cb16944c22591c847bf1c02c81f2c825`  
		Last Modified: Fri, 11 Dec 2020 02:39:11 GMT  
		Size: 256.2 KB (256158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cad78cba8d670a26f74487900565a5e53b2b5d740157a89bd6eb41e697f0ae30`  
		Last Modified: Fri, 11 Dec 2020 02:39:17 GMT  
		Size: 29.3 MB (29311041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
