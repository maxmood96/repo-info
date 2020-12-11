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
$ docker pull mono@sha256:d5a47ab075bb6538f095417f256e7bec03e1d67c1926488d278443a4a1ba85d8
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
$ docker pull mono@sha256:facbe0a70ded15ca8315155b22f0ed9176e4fd16040c51dad384c2107ceaf0c1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.7 MB (191705978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43b6e40880e80c6dfd2c3ff378b679952a88601a74d31ed7eca93df4176d3594`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 11 Dec 2020 02:04:49 GMT
ADD file:58ebb3ffaf26d9b7621efba5f109ae9d22832f2f22865cda36604b138cbdb7b8 in / 
# Fri, 11 Dec 2020 02:04:56 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 03:41:57 GMT
ENV MONO_VERSION=6.12.0.107
# Fri, 11 Dec 2020 03:42:24 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 11 Dec 2020 03:43:10 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Fri, 11 Dec 2020 03:47:34 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:8cbd1f790d64c77fcac6c9dbfe4d4c82f0365de9438f1a42b0560dc88f9e6a55`  
		Last Modified: Fri, 11 Dec 2020 02:14:44 GMT  
		Size: 24.8 MB (24843461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc539c64dc00d4039c50099fac2985998f6c5a718bf3a99b1ed39ca7622e9fcc`  
		Last Modified: Fri, 11 Dec 2020 03:52:45 GMT  
		Size: 256.0 KB (255989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:686f758c22e775b28fea1be4a5cab430f1644e1d6f259657dcd574a30a046d85`  
		Last Modified: Fri, 11 Dec 2020 03:52:59 GMT  
		Size: 26.5 MB (26499303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f2b21a188ebe615c0e00705c9bbcdd6a64afd4d2fb9bcde2131024f20bf082d`  
		Last Modified: Fri, 11 Dec 2020 03:54:51 GMT  
		Size: 140.1 MB (140107225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6` - linux; arm variant v7

```console
$ docker pull mono@sha256:60b395dbd94129df45bba140e9fef7c5f92213399cd9a7010b29f0a4651619f2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.6 MB (187602846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7587a90d765fbf4f92a5395222e0f6d2d6202dd641a9f777234751e917bf4f8b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 11 Dec 2020 02:23:37 GMT
ADD file:75ca842ac2d6e9f6617bb3df280af1e4c9619c9805fd5e00c1c3d6b8b4e3d802 in / 
# Fri, 11 Dec 2020 02:23:39 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 16:04:55 GMT
ENV MONO_VERSION=6.12.0.107
# Fri, 11 Dec 2020 16:05:16 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 11 Dec 2020 16:05:58 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Fri, 11 Dec 2020 16:10:08 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:c06905228d4fc5a5c840a70e2e6ced56596a8bc73abc69e6a1867bbb6f7ae7e7`  
		Last Modified: Fri, 11 Dec 2020 02:33:07 GMT  
		Size: 22.7 MB (22707662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b6050173e7f0c096548a7d0ae4600b1aa634ebd0f04d2a0641e1de70d735a81`  
		Last Modified: Fri, 11 Dec 2020 16:14:05 GMT  
		Size: 256.0 KB (255961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c669a631af9fa12abb498a87e56c428d7767752fae1125211f976b7a97582cc`  
		Last Modified: Fri, 11 Dec 2020 16:14:13 GMT  
		Size: 25.7 MB (25697324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64499980fa6ccec57ab43eb6769c5a83d01abd1e45411c2a06374ddffcfe9d30`  
		Last Modified: Fri, 11 Dec 2020 16:15:37 GMT  
		Size: 138.9 MB (138941899 bytes)  
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
$ docker pull mono@sha256:d228a286a9634f5ceb87c4a6880446a34a60dd18fd4f375ff15de765fdf6f3b1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.3 MB (203315195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3ba7e6d47f9b23521f48b0071ccec29f62ed8ecb7f0b9d923452236802a6c02`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 11 Dec 2020 03:34:02 GMT
ADD file:eca1a7737bd5e84ff883c4c284c0cd22492145d9cd7ae3b8e7b490e3d8e5aefb in / 
# Fri, 11 Dec 2020 03:34:11 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 03:47:17 GMT
ENV MONO_VERSION=6.12.0.107
# Fri, 11 Dec 2020 03:48:45 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 11 Dec 2020 03:51:05 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Fri, 11 Dec 2020 04:05:16 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:c0f0648876332890be87a9f32ec4ad2a939e805be3152ab991a923f7dec2b35d`  
		Last Modified: Fri, 11 Dec 2020 03:41:39 GMT  
		Size: 30.5 MB (30524717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:833550a83d07a1b6e220c1a79afe3f7627de214a70b02861832cbf79941b586b`  
		Last Modified: Fri, 11 Dec 2020 04:14:40 GMT  
		Size: 256.2 KB (256229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f3ed8da96c8ea7c70fad6716cfd341810be1c4a0a5ed6c88546a60db481d428`  
		Last Modified: Fri, 11 Dec 2020 04:14:46 GMT  
		Size: 29.3 MB (29311114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9499aa37e5b0b65ee6a349eb1fbcfdeabfb3916c0f0299ce5a99ecead9ee8df`  
		Last Modified: Fri, 11 Dec 2020 04:15:56 GMT  
		Size: 143.2 MB (143223135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.10`

```console
$ docker pull mono@sha256:4b7ad20f196c69874b3693bb84eb38b36819cf3472d844bdf29d14bb0d468cbf
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
$ docker pull mono@sha256:90a0cb9c0c9628de7bb79f50e274f31a6d49b920f52bd5d5a5e7634fab5ebd58
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.6 MB (180593296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abd9f8c374a1c1fbe6961dd4297ad779f484379312881c25229ce7d165e59d13`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 11 Dec 2020 02:04:49 GMT
ADD file:58ebb3ffaf26d9b7621efba5f109ae9d22832f2f22865cda36604b138cbdb7b8 in / 
# Fri, 11 Dec 2020 02:04:56 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 03:43:24 GMT
ENV MONO_VERSION=6.10.0.104
# Fri, 11 Dec 2020 03:43:48 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 11 Dec 2020 03:44:39 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Fri, 11 Dec 2020 03:51:53 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:8cbd1f790d64c77fcac6c9dbfe4d4c82f0365de9438f1a42b0560dc88f9e6a55`  
		Last Modified: Fri, 11 Dec 2020 02:14:44 GMT  
		Size: 24.8 MB (24843461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47ce2de1378f2c6ab4eca46976f6279a962dfe0cc9089e517d5a05b551e6039e`  
		Last Modified: Fri, 11 Dec 2020 03:53:14 GMT  
		Size: 256.0 KB (256005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87bce6a1c04f1d0bfcbf7e1d10350ec4284b35dc11ff2103f81873e88ac889fa`  
		Last Modified: Fri, 11 Dec 2020 03:53:29 GMT  
		Size: 26.5 MB (26531426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a0193368648b6afdf7d4e0887900ad3a8fca5ece4f4acccc60e5aa1b02856af`  
		Last Modified: Fri, 11 Dec 2020 03:55:58 GMT  
		Size: 129.0 MB (128962404 bytes)  
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
$ docker pull mono@sha256:0efc9c7edd1b2b9f0b313e3085ca477317e90354b7ac93426e49a552fd16f6b9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.1 MB (192109591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30aa5c0deaa0327a30cd8b8cab122157981a2c4316847ac11831ec506404bd17`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 11 Dec 2020 03:34:02 GMT
ADD file:eca1a7737bd5e84ff883c4c284c0cd22492145d9cd7ae3b8e7b490e3d8e5aefb in / 
# Fri, 11 Dec 2020 03:34:11 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 03:51:31 GMT
ENV MONO_VERSION=6.10.0.104
# Fri, 11 Dec 2020 03:53:08 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 11 Dec 2020 03:55:51 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Fri, 11 Dec 2020 04:14:02 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:c0f0648876332890be87a9f32ec4ad2a939e805be3152ab991a923f7dec2b35d`  
		Last Modified: Fri, 11 Dec 2020 03:41:39 GMT  
		Size: 30.5 MB (30524717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b8492dfbf2d49f9342cac21d3baf53200be1b0fdaa3ad54edeb80da7c1de831`  
		Last Modified: Fri, 11 Dec 2020 04:15:06 GMT  
		Size: 256.3 KB (256273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ca01eda9d559b83aa7bd5c9fcd4aae1813f368b3ffcbc0232282153f5ea0c96`  
		Last Modified: Fri, 11 Dec 2020 04:15:12 GMT  
		Size: 29.4 MB (29350199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec766bd339ec3ccd2168bafd723a67166d94ebfc751de38e08ba83ae2179765`  
		Last Modified: Fri, 11 Dec 2020 04:16:43 GMT  
		Size: 132.0 MB (131978402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.10.0`

```console
$ docker pull mono@sha256:4b7ad20f196c69874b3693bb84eb38b36819cf3472d844bdf29d14bb0d468cbf
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
$ docker pull mono@sha256:90a0cb9c0c9628de7bb79f50e274f31a6d49b920f52bd5d5a5e7634fab5ebd58
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.6 MB (180593296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abd9f8c374a1c1fbe6961dd4297ad779f484379312881c25229ce7d165e59d13`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 11 Dec 2020 02:04:49 GMT
ADD file:58ebb3ffaf26d9b7621efba5f109ae9d22832f2f22865cda36604b138cbdb7b8 in / 
# Fri, 11 Dec 2020 02:04:56 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 03:43:24 GMT
ENV MONO_VERSION=6.10.0.104
# Fri, 11 Dec 2020 03:43:48 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 11 Dec 2020 03:44:39 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Fri, 11 Dec 2020 03:51:53 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:8cbd1f790d64c77fcac6c9dbfe4d4c82f0365de9438f1a42b0560dc88f9e6a55`  
		Last Modified: Fri, 11 Dec 2020 02:14:44 GMT  
		Size: 24.8 MB (24843461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47ce2de1378f2c6ab4eca46976f6279a962dfe0cc9089e517d5a05b551e6039e`  
		Last Modified: Fri, 11 Dec 2020 03:53:14 GMT  
		Size: 256.0 KB (256005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87bce6a1c04f1d0bfcbf7e1d10350ec4284b35dc11ff2103f81873e88ac889fa`  
		Last Modified: Fri, 11 Dec 2020 03:53:29 GMT  
		Size: 26.5 MB (26531426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a0193368648b6afdf7d4e0887900ad3a8fca5ece4f4acccc60e5aa1b02856af`  
		Last Modified: Fri, 11 Dec 2020 03:55:58 GMT  
		Size: 129.0 MB (128962404 bytes)  
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
$ docker pull mono@sha256:0efc9c7edd1b2b9f0b313e3085ca477317e90354b7ac93426e49a552fd16f6b9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.1 MB (192109591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30aa5c0deaa0327a30cd8b8cab122157981a2c4316847ac11831ec506404bd17`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 11 Dec 2020 03:34:02 GMT
ADD file:eca1a7737bd5e84ff883c4c284c0cd22492145d9cd7ae3b8e7b490e3d8e5aefb in / 
# Fri, 11 Dec 2020 03:34:11 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 03:51:31 GMT
ENV MONO_VERSION=6.10.0.104
# Fri, 11 Dec 2020 03:53:08 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 11 Dec 2020 03:55:51 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Fri, 11 Dec 2020 04:14:02 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:c0f0648876332890be87a9f32ec4ad2a939e805be3152ab991a923f7dec2b35d`  
		Last Modified: Fri, 11 Dec 2020 03:41:39 GMT  
		Size: 30.5 MB (30524717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b8492dfbf2d49f9342cac21d3baf53200be1b0fdaa3ad54edeb80da7c1de831`  
		Last Modified: Fri, 11 Dec 2020 04:15:06 GMT  
		Size: 256.3 KB (256273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ca01eda9d559b83aa7bd5c9fcd4aae1813f368b3ffcbc0232282153f5ea0c96`  
		Last Modified: Fri, 11 Dec 2020 04:15:12 GMT  
		Size: 29.4 MB (29350199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec766bd339ec3ccd2168bafd723a67166d94ebfc751de38e08ba83ae2179765`  
		Last Modified: Fri, 11 Dec 2020 04:16:43 GMT  
		Size: 132.0 MB (131978402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.10.0.104`

```console
$ docker pull mono@sha256:4b7ad20f196c69874b3693bb84eb38b36819cf3472d844bdf29d14bb0d468cbf
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
$ docker pull mono@sha256:90a0cb9c0c9628de7bb79f50e274f31a6d49b920f52bd5d5a5e7634fab5ebd58
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.6 MB (180593296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abd9f8c374a1c1fbe6961dd4297ad779f484379312881c25229ce7d165e59d13`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 11 Dec 2020 02:04:49 GMT
ADD file:58ebb3ffaf26d9b7621efba5f109ae9d22832f2f22865cda36604b138cbdb7b8 in / 
# Fri, 11 Dec 2020 02:04:56 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 03:43:24 GMT
ENV MONO_VERSION=6.10.0.104
# Fri, 11 Dec 2020 03:43:48 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 11 Dec 2020 03:44:39 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Fri, 11 Dec 2020 03:51:53 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:8cbd1f790d64c77fcac6c9dbfe4d4c82f0365de9438f1a42b0560dc88f9e6a55`  
		Last Modified: Fri, 11 Dec 2020 02:14:44 GMT  
		Size: 24.8 MB (24843461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47ce2de1378f2c6ab4eca46976f6279a962dfe0cc9089e517d5a05b551e6039e`  
		Last Modified: Fri, 11 Dec 2020 03:53:14 GMT  
		Size: 256.0 KB (256005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87bce6a1c04f1d0bfcbf7e1d10350ec4284b35dc11ff2103f81873e88ac889fa`  
		Last Modified: Fri, 11 Dec 2020 03:53:29 GMT  
		Size: 26.5 MB (26531426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a0193368648b6afdf7d4e0887900ad3a8fca5ece4f4acccc60e5aa1b02856af`  
		Last Modified: Fri, 11 Dec 2020 03:55:58 GMT  
		Size: 129.0 MB (128962404 bytes)  
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
$ docker pull mono@sha256:0efc9c7edd1b2b9f0b313e3085ca477317e90354b7ac93426e49a552fd16f6b9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.1 MB (192109591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30aa5c0deaa0327a30cd8b8cab122157981a2c4316847ac11831ec506404bd17`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 11 Dec 2020 03:34:02 GMT
ADD file:eca1a7737bd5e84ff883c4c284c0cd22492145d9cd7ae3b8e7b490e3d8e5aefb in / 
# Fri, 11 Dec 2020 03:34:11 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 03:51:31 GMT
ENV MONO_VERSION=6.10.0.104
# Fri, 11 Dec 2020 03:53:08 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 11 Dec 2020 03:55:51 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Fri, 11 Dec 2020 04:14:02 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:c0f0648876332890be87a9f32ec4ad2a939e805be3152ab991a923f7dec2b35d`  
		Last Modified: Fri, 11 Dec 2020 03:41:39 GMT  
		Size: 30.5 MB (30524717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b8492dfbf2d49f9342cac21d3baf53200be1b0fdaa3ad54edeb80da7c1de831`  
		Last Modified: Fri, 11 Dec 2020 04:15:06 GMT  
		Size: 256.3 KB (256273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ca01eda9d559b83aa7bd5c9fcd4aae1813f368b3ffcbc0232282153f5ea0c96`  
		Last Modified: Fri, 11 Dec 2020 04:15:12 GMT  
		Size: 29.4 MB (29350199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec766bd339ec3ccd2168bafd723a67166d94ebfc751de38e08ba83ae2179765`  
		Last Modified: Fri, 11 Dec 2020 04:16:43 GMT  
		Size: 132.0 MB (131978402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.10.0.104-slim`

```console
$ docker pull mono@sha256:54fc62f8189835c4c81242210e111abcd3c4f77e10fb431eff592f40341b7037
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
$ docker pull mono@sha256:b397bd17c33be859c3f0ef1cb99f90b4649f61cdf605d755281f8ee598262023
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51630892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a76a2595ccd522a290e2ad829915bc1b71d72a5d6832e344842e1ed5996a3e78`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 11 Dec 2020 02:04:49 GMT
ADD file:58ebb3ffaf26d9b7621efba5f109ae9d22832f2f22865cda36604b138cbdb7b8 in / 
# Fri, 11 Dec 2020 02:04:56 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 03:43:24 GMT
ENV MONO_VERSION=6.10.0.104
# Fri, 11 Dec 2020 03:43:48 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 11 Dec 2020 03:44:39 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:8cbd1f790d64c77fcac6c9dbfe4d4c82f0365de9438f1a42b0560dc88f9e6a55`  
		Last Modified: Fri, 11 Dec 2020 02:14:44 GMT  
		Size: 24.8 MB (24843461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47ce2de1378f2c6ab4eca46976f6279a962dfe0cc9089e517d5a05b551e6039e`  
		Last Modified: Fri, 11 Dec 2020 03:53:14 GMT  
		Size: 256.0 KB (256005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87bce6a1c04f1d0bfcbf7e1d10350ec4284b35dc11ff2103f81873e88ac889fa`  
		Last Modified: Fri, 11 Dec 2020 03:53:29 GMT  
		Size: 26.5 MB (26531426 bytes)  
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
$ docker pull mono@sha256:d4cb95875cf635fb34ebeca27620d59f0066abd32f75fd7daafcc941f531826d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60131189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af4c6c1f8b62c2a9a59580f0fd790a91acc01884957605545e807f002ae9679c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 11 Dec 2020 03:34:02 GMT
ADD file:eca1a7737bd5e84ff883c4c284c0cd22492145d9cd7ae3b8e7b490e3d8e5aefb in / 
# Fri, 11 Dec 2020 03:34:11 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 03:51:31 GMT
ENV MONO_VERSION=6.10.0.104
# Fri, 11 Dec 2020 03:53:08 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 11 Dec 2020 03:55:51 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:c0f0648876332890be87a9f32ec4ad2a939e805be3152ab991a923f7dec2b35d`  
		Last Modified: Fri, 11 Dec 2020 03:41:39 GMT  
		Size: 30.5 MB (30524717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b8492dfbf2d49f9342cac21d3baf53200be1b0fdaa3ad54edeb80da7c1de831`  
		Last Modified: Fri, 11 Dec 2020 04:15:06 GMT  
		Size: 256.3 KB (256273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ca01eda9d559b83aa7bd5c9fcd4aae1813f368b3ffcbc0232282153f5ea0c96`  
		Last Modified: Fri, 11 Dec 2020 04:15:12 GMT  
		Size: 29.4 MB (29350199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.10.0-slim`

```console
$ docker pull mono@sha256:54fc62f8189835c4c81242210e111abcd3c4f77e10fb431eff592f40341b7037
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
$ docker pull mono@sha256:b397bd17c33be859c3f0ef1cb99f90b4649f61cdf605d755281f8ee598262023
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51630892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a76a2595ccd522a290e2ad829915bc1b71d72a5d6832e344842e1ed5996a3e78`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 11 Dec 2020 02:04:49 GMT
ADD file:58ebb3ffaf26d9b7621efba5f109ae9d22832f2f22865cda36604b138cbdb7b8 in / 
# Fri, 11 Dec 2020 02:04:56 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 03:43:24 GMT
ENV MONO_VERSION=6.10.0.104
# Fri, 11 Dec 2020 03:43:48 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 11 Dec 2020 03:44:39 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:8cbd1f790d64c77fcac6c9dbfe4d4c82f0365de9438f1a42b0560dc88f9e6a55`  
		Last Modified: Fri, 11 Dec 2020 02:14:44 GMT  
		Size: 24.8 MB (24843461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47ce2de1378f2c6ab4eca46976f6279a962dfe0cc9089e517d5a05b551e6039e`  
		Last Modified: Fri, 11 Dec 2020 03:53:14 GMT  
		Size: 256.0 KB (256005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87bce6a1c04f1d0bfcbf7e1d10350ec4284b35dc11ff2103f81873e88ac889fa`  
		Last Modified: Fri, 11 Dec 2020 03:53:29 GMT  
		Size: 26.5 MB (26531426 bytes)  
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
$ docker pull mono@sha256:d4cb95875cf635fb34ebeca27620d59f0066abd32f75fd7daafcc941f531826d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60131189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af4c6c1f8b62c2a9a59580f0fd790a91acc01884957605545e807f002ae9679c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 11 Dec 2020 03:34:02 GMT
ADD file:eca1a7737bd5e84ff883c4c284c0cd22492145d9cd7ae3b8e7b490e3d8e5aefb in / 
# Fri, 11 Dec 2020 03:34:11 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 03:51:31 GMT
ENV MONO_VERSION=6.10.0.104
# Fri, 11 Dec 2020 03:53:08 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 11 Dec 2020 03:55:51 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:c0f0648876332890be87a9f32ec4ad2a939e805be3152ab991a923f7dec2b35d`  
		Last Modified: Fri, 11 Dec 2020 03:41:39 GMT  
		Size: 30.5 MB (30524717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b8492dfbf2d49f9342cac21d3baf53200be1b0fdaa3ad54edeb80da7c1de831`  
		Last Modified: Fri, 11 Dec 2020 04:15:06 GMT  
		Size: 256.3 KB (256273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ca01eda9d559b83aa7bd5c9fcd4aae1813f368b3ffcbc0232282153f5ea0c96`  
		Last Modified: Fri, 11 Dec 2020 04:15:12 GMT  
		Size: 29.4 MB (29350199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.10-slim`

```console
$ docker pull mono@sha256:54fc62f8189835c4c81242210e111abcd3c4f77e10fb431eff592f40341b7037
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
$ docker pull mono@sha256:b397bd17c33be859c3f0ef1cb99f90b4649f61cdf605d755281f8ee598262023
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51630892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a76a2595ccd522a290e2ad829915bc1b71d72a5d6832e344842e1ed5996a3e78`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 11 Dec 2020 02:04:49 GMT
ADD file:58ebb3ffaf26d9b7621efba5f109ae9d22832f2f22865cda36604b138cbdb7b8 in / 
# Fri, 11 Dec 2020 02:04:56 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 03:43:24 GMT
ENV MONO_VERSION=6.10.0.104
# Fri, 11 Dec 2020 03:43:48 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 11 Dec 2020 03:44:39 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:8cbd1f790d64c77fcac6c9dbfe4d4c82f0365de9438f1a42b0560dc88f9e6a55`  
		Last Modified: Fri, 11 Dec 2020 02:14:44 GMT  
		Size: 24.8 MB (24843461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47ce2de1378f2c6ab4eca46976f6279a962dfe0cc9089e517d5a05b551e6039e`  
		Last Modified: Fri, 11 Dec 2020 03:53:14 GMT  
		Size: 256.0 KB (256005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87bce6a1c04f1d0bfcbf7e1d10350ec4284b35dc11ff2103f81873e88ac889fa`  
		Last Modified: Fri, 11 Dec 2020 03:53:29 GMT  
		Size: 26.5 MB (26531426 bytes)  
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
$ docker pull mono@sha256:d4cb95875cf635fb34ebeca27620d59f0066abd32f75fd7daafcc941f531826d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60131189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af4c6c1f8b62c2a9a59580f0fd790a91acc01884957605545e807f002ae9679c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 11 Dec 2020 03:34:02 GMT
ADD file:eca1a7737bd5e84ff883c4c284c0cd22492145d9cd7ae3b8e7b490e3d8e5aefb in / 
# Fri, 11 Dec 2020 03:34:11 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 03:51:31 GMT
ENV MONO_VERSION=6.10.0.104
# Fri, 11 Dec 2020 03:53:08 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 11 Dec 2020 03:55:51 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:c0f0648876332890be87a9f32ec4ad2a939e805be3152ab991a923f7dec2b35d`  
		Last Modified: Fri, 11 Dec 2020 03:41:39 GMT  
		Size: 30.5 MB (30524717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b8492dfbf2d49f9342cac21d3baf53200be1b0fdaa3ad54edeb80da7c1de831`  
		Last Modified: Fri, 11 Dec 2020 04:15:06 GMT  
		Size: 256.3 KB (256273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ca01eda9d559b83aa7bd5c9fcd4aae1813f368b3ffcbc0232282153f5ea0c96`  
		Last Modified: Fri, 11 Dec 2020 04:15:12 GMT  
		Size: 29.4 MB (29350199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.12`

```console
$ docker pull mono@sha256:0c215dd2576ef581ece800b74cf4f9aa1642af6f2923d46cad2d7b5cfcd853ff
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
$ docker pull mono@sha256:facbe0a70ded15ca8315155b22f0ed9176e4fd16040c51dad384c2107ceaf0c1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.7 MB (191705978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43b6e40880e80c6dfd2c3ff378b679952a88601a74d31ed7eca93df4176d3594`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 11 Dec 2020 02:04:49 GMT
ADD file:58ebb3ffaf26d9b7621efba5f109ae9d22832f2f22865cda36604b138cbdb7b8 in / 
# Fri, 11 Dec 2020 02:04:56 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 03:41:57 GMT
ENV MONO_VERSION=6.12.0.107
# Fri, 11 Dec 2020 03:42:24 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 11 Dec 2020 03:43:10 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Fri, 11 Dec 2020 03:47:34 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:8cbd1f790d64c77fcac6c9dbfe4d4c82f0365de9438f1a42b0560dc88f9e6a55`  
		Last Modified: Fri, 11 Dec 2020 02:14:44 GMT  
		Size: 24.8 MB (24843461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc539c64dc00d4039c50099fac2985998f6c5a718bf3a99b1ed39ca7622e9fcc`  
		Last Modified: Fri, 11 Dec 2020 03:52:45 GMT  
		Size: 256.0 KB (255989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:686f758c22e775b28fea1be4a5cab430f1644e1d6f259657dcd574a30a046d85`  
		Last Modified: Fri, 11 Dec 2020 03:52:59 GMT  
		Size: 26.5 MB (26499303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f2b21a188ebe615c0e00705c9bbcdd6a64afd4d2fb9bcde2131024f20bf082d`  
		Last Modified: Fri, 11 Dec 2020 03:54:51 GMT  
		Size: 140.1 MB (140107225 bytes)  
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
$ docker pull mono@sha256:d228a286a9634f5ceb87c4a6880446a34a60dd18fd4f375ff15de765fdf6f3b1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.3 MB (203315195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3ba7e6d47f9b23521f48b0071ccec29f62ed8ecb7f0b9d923452236802a6c02`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 11 Dec 2020 03:34:02 GMT
ADD file:eca1a7737bd5e84ff883c4c284c0cd22492145d9cd7ae3b8e7b490e3d8e5aefb in / 
# Fri, 11 Dec 2020 03:34:11 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 03:47:17 GMT
ENV MONO_VERSION=6.12.0.107
# Fri, 11 Dec 2020 03:48:45 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 11 Dec 2020 03:51:05 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Fri, 11 Dec 2020 04:05:16 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:c0f0648876332890be87a9f32ec4ad2a939e805be3152ab991a923f7dec2b35d`  
		Last Modified: Fri, 11 Dec 2020 03:41:39 GMT  
		Size: 30.5 MB (30524717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:833550a83d07a1b6e220c1a79afe3f7627de214a70b02861832cbf79941b586b`  
		Last Modified: Fri, 11 Dec 2020 04:14:40 GMT  
		Size: 256.2 KB (256229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f3ed8da96c8ea7c70fad6716cfd341810be1c4a0a5ed6c88546a60db481d428`  
		Last Modified: Fri, 11 Dec 2020 04:14:46 GMT  
		Size: 29.3 MB (29311114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9499aa37e5b0b65ee6a349eb1fbcfdeabfb3916c0f0299ce5a99ecead9ee8df`  
		Last Modified: Fri, 11 Dec 2020 04:15:56 GMT  
		Size: 143.2 MB (143223135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.12.0`

```console
$ docker pull mono@sha256:0c215dd2576ef581ece800b74cf4f9aa1642af6f2923d46cad2d7b5cfcd853ff
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
$ docker pull mono@sha256:facbe0a70ded15ca8315155b22f0ed9176e4fd16040c51dad384c2107ceaf0c1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.7 MB (191705978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43b6e40880e80c6dfd2c3ff378b679952a88601a74d31ed7eca93df4176d3594`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 11 Dec 2020 02:04:49 GMT
ADD file:58ebb3ffaf26d9b7621efba5f109ae9d22832f2f22865cda36604b138cbdb7b8 in / 
# Fri, 11 Dec 2020 02:04:56 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 03:41:57 GMT
ENV MONO_VERSION=6.12.0.107
# Fri, 11 Dec 2020 03:42:24 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 11 Dec 2020 03:43:10 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Fri, 11 Dec 2020 03:47:34 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:8cbd1f790d64c77fcac6c9dbfe4d4c82f0365de9438f1a42b0560dc88f9e6a55`  
		Last Modified: Fri, 11 Dec 2020 02:14:44 GMT  
		Size: 24.8 MB (24843461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc539c64dc00d4039c50099fac2985998f6c5a718bf3a99b1ed39ca7622e9fcc`  
		Last Modified: Fri, 11 Dec 2020 03:52:45 GMT  
		Size: 256.0 KB (255989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:686f758c22e775b28fea1be4a5cab430f1644e1d6f259657dcd574a30a046d85`  
		Last Modified: Fri, 11 Dec 2020 03:52:59 GMT  
		Size: 26.5 MB (26499303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f2b21a188ebe615c0e00705c9bbcdd6a64afd4d2fb9bcde2131024f20bf082d`  
		Last Modified: Fri, 11 Dec 2020 03:54:51 GMT  
		Size: 140.1 MB (140107225 bytes)  
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
$ docker pull mono@sha256:d228a286a9634f5ceb87c4a6880446a34a60dd18fd4f375ff15de765fdf6f3b1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.3 MB (203315195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3ba7e6d47f9b23521f48b0071ccec29f62ed8ecb7f0b9d923452236802a6c02`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 11 Dec 2020 03:34:02 GMT
ADD file:eca1a7737bd5e84ff883c4c284c0cd22492145d9cd7ae3b8e7b490e3d8e5aefb in / 
# Fri, 11 Dec 2020 03:34:11 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 03:47:17 GMT
ENV MONO_VERSION=6.12.0.107
# Fri, 11 Dec 2020 03:48:45 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 11 Dec 2020 03:51:05 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Fri, 11 Dec 2020 04:05:16 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:c0f0648876332890be87a9f32ec4ad2a939e805be3152ab991a923f7dec2b35d`  
		Last Modified: Fri, 11 Dec 2020 03:41:39 GMT  
		Size: 30.5 MB (30524717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:833550a83d07a1b6e220c1a79afe3f7627de214a70b02861832cbf79941b586b`  
		Last Modified: Fri, 11 Dec 2020 04:14:40 GMT  
		Size: 256.2 KB (256229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f3ed8da96c8ea7c70fad6716cfd341810be1c4a0a5ed6c88546a60db481d428`  
		Last Modified: Fri, 11 Dec 2020 04:14:46 GMT  
		Size: 29.3 MB (29311114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9499aa37e5b0b65ee6a349eb1fbcfdeabfb3916c0f0299ce5a99ecead9ee8df`  
		Last Modified: Fri, 11 Dec 2020 04:15:56 GMT  
		Size: 143.2 MB (143223135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.12.0.107`

```console
$ docker pull mono@sha256:0c215dd2576ef581ece800b74cf4f9aa1642af6f2923d46cad2d7b5cfcd853ff
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
$ docker pull mono@sha256:facbe0a70ded15ca8315155b22f0ed9176e4fd16040c51dad384c2107ceaf0c1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.7 MB (191705978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43b6e40880e80c6dfd2c3ff378b679952a88601a74d31ed7eca93df4176d3594`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 11 Dec 2020 02:04:49 GMT
ADD file:58ebb3ffaf26d9b7621efba5f109ae9d22832f2f22865cda36604b138cbdb7b8 in / 
# Fri, 11 Dec 2020 02:04:56 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 03:41:57 GMT
ENV MONO_VERSION=6.12.0.107
# Fri, 11 Dec 2020 03:42:24 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 11 Dec 2020 03:43:10 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Fri, 11 Dec 2020 03:47:34 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:8cbd1f790d64c77fcac6c9dbfe4d4c82f0365de9438f1a42b0560dc88f9e6a55`  
		Last Modified: Fri, 11 Dec 2020 02:14:44 GMT  
		Size: 24.8 MB (24843461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc539c64dc00d4039c50099fac2985998f6c5a718bf3a99b1ed39ca7622e9fcc`  
		Last Modified: Fri, 11 Dec 2020 03:52:45 GMT  
		Size: 256.0 KB (255989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:686f758c22e775b28fea1be4a5cab430f1644e1d6f259657dcd574a30a046d85`  
		Last Modified: Fri, 11 Dec 2020 03:52:59 GMT  
		Size: 26.5 MB (26499303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f2b21a188ebe615c0e00705c9bbcdd6a64afd4d2fb9bcde2131024f20bf082d`  
		Last Modified: Fri, 11 Dec 2020 03:54:51 GMT  
		Size: 140.1 MB (140107225 bytes)  
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
$ docker pull mono@sha256:d228a286a9634f5ceb87c4a6880446a34a60dd18fd4f375ff15de765fdf6f3b1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.3 MB (203315195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3ba7e6d47f9b23521f48b0071ccec29f62ed8ecb7f0b9d923452236802a6c02`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 11 Dec 2020 03:34:02 GMT
ADD file:eca1a7737bd5e84ff883c4c284c0cd22492145d9cd7ae3b8e7b490e3d8e5aefb in / 
# Fri, 11 Dec 2020 03:34:11 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 03:47:17 GMT
ENV MONO_VERSION=6.12.0.107
# Fri, 11 Dec 2020 03:48:45 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 11 Dec 2020 03:51:05 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Fri, 11 Dec 2020 04:05:16 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:c0f0648876332890be87a9f32ec4ad2a939e805be3152ab991a923f7dec2b35d`  
		Last Modified: Fri, 11 Dec 2020 03:41:39 GMT  
		Size: 30.5 MB (30524717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:833550a83d07a1b6e220c1a79afe3f7627de214a70b02861832cbf79941b586b`  
		Last Modified: Fri, 11 Dec 2020 04:14:40 GMT  
		Size: 256.2 KB (256229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f3ed8da96c8ea7c70fad6716cfd341810be1c4a0a5ed6c88546a60db481d428`  
		Last Modified: Fri, 11 Dec 2020 04:14:46 GMT  
		Size: 29.3 MB (29311114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9499aa37e5b0b65ee6a349eb1fbcfdeabfb3916c0f0299ce5a99ecead9ee8df`  
		Last Modified: Fri, 11 Dec 2020 04:15:56 GMT  
		Size: 143.2 MB (143223135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.12.0.107-slim`

```console
$ docker pull mono@sha256:346a69efa561119c7edf438fb9d03e0a1eac5a9e7302585180e781bff0fa87ae
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
$ docker pull mono@sha256:b1ee94f4a5601850bcbd7ddd3e2a432d2d2fccffffd65aef19274dfb7465139b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51598753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0acf66a2efccb8d2b04f037d6c482d855f1ac0a5785ad2d11444fb79a884c4ef`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 11 Dec 2020 02:04:49 GMT
ADD file:58ebb3ffaf26d9b7621efba5f109ae9d22832f2f22865cda36604b138cbdb7b8 in / 
# Fri, 11 Dec 2020 02:04:56 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 03:41:57 GMT
ENV MONO_VERSION=6.12.0.107
# Fri, 11 Dec 2020 03:42:24 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 11 Dec 2020 03:43:10 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:8cbd1f790d64c77fcac6c9dbfe4d4c82f0365de9438f1a42b0560dc88f9e6a55`  
		Last Modified: Fri, 11 Dec 2020 02:14:44 GMT  
		Size: 24.8 MB (24843461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc539c64dc00d4039c50099fac2985998f6c5a718bf3a99b1ed39ca7622e9fcc`  
		Last Modified: Fri, 11 Dec 2020 03:52:45 GMT  
		Size: 256.0 KB (255989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:686f758c22e775b28fea1be4a5cab430f1644e1d6f259657dcd574a30a046d85`  
		Last Modified: Fri, 11 Dec 2020 03:52:59 GMT  
		Size: 26.5 MB (26499303 bytes)  
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
$ docker pull mono@sha256:99059ede7dec72369488f094708b5aee5a3149a5e08eca0e553e6f1a3493fd21
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60092060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0126153e1f3ce853b883f7bf0340bb25f06be319fe89aab5242fdbe98260a8b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 11 Dec 2020 03:34:02 GMT
ADD file:eca1a7737bd5e84ff883c4c284c0cd22492145d9cd7ae3b8e7b490e3d8e5aefb in / 
# Fri, 11 Dec 2020 03:34:11 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 03:47:17 GMT
ENV MONO_VERSION=6.12.0.107
# Fri, 11 Dec 2020 03:48:45 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 11 Dec 2020 03:51:05 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:c0f0648876332890be87a9f32ec4ad2a939e805be3152ab991a923f7dec2b35d`  
		Last Modified: Fri, 11 Dec 2020 03:41:39 GMT  
		Size: 30.5 MB (30524717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:833550a83d07a1b6e220c1a79afe3f7627de214a70b02861832cbf79941b586b`  
		Last Modified: Fri, 11 Dec 2020 04:14:40 GMT  
		Size: 256.2 KB (256229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f3ed8da96c8ea7c70fad6716cfd341810be1c4a0a5ed6c88546a60db481d428`  
		Last Modified: Fri, 11 Dec 2020 04:14:46 GMT  
		Size: 29.3 MB (29311114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.12.0-slim`

```console
$ docker pull mono@sha256:346a69efa561119c7edf438fb9d03e0a1eac5a9e7302585180e781bff0fa87ae
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
$ docker pull mono@sha256:b1ee94f4a5601850bcbd7ddd3e2a432d2d2fccffffd65aef19274dfb7465139b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51598753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0acf66a2efccb8d2b04f037d6c482d855f1ac0a5785ad2d11444fb79a884c4ef`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 11 Dec 2020 02:04:49 GMT
ADD file:58ebb3ffaf26d9b7621efba5f109ae9d22832f2f22865cda36604b138cbdb7b8 in / 
# Fri, 11 Dec 2020 02:04:56 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 03:41:57 GMT
ENV MONO_VERSION=6.12.0.107
# Fri, 11 Dec 2020 03:42:24 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 11 Dec 2020 03:43:10 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:8cbd1f790d64c77fcac6c9dbfe4d4c82f0365de9438f1a42b0560dc88f9e6a55`  
		Last Modified: Fri, 11 Dec 2020 02:14:44 GMT  
		Size: 24.8 MB (24843461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc539c64dc00d4039c50099fac2985998f6c5a718bf3a99b1ed39ca7622e9fcc`  
		Last Modified: Fri, 11 Dec 2020 03:52:45 GMT  
		Size: 256.0 KB (255989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:686f758c22e775b28fea1be4a5cab430f1644e1d6f259657dcd574a30a046d85`  
		Last Modified: Fri, 11 Dec 2020 03:52:59 GMT  
		Size: 26.5 MB (26499303 bytes)  
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
$ docker pull mono@sha256:99059ede7dec72369488f094708b5aee5a3149a5e08eca0e553e6f1a3493fd21
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60092060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0126153e1f3ce853b883f7bf0340bb25f06be319fe89aab5242fdbe98260a8b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 11 Dec 2020 03:34:02 GMT
ADD file:eca1a7737bd5e84ff883c4c284c0cd22492145d9cd7ae3b8e7b490e3d8e5aefb in / 
# Fri, 11 Dec 2020 03:34:11 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 03:47:17 GMT
ENV MONO_VERSION=6.12.0.107
# Fri, 11 Dec 2020 03:48:45 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 11 Dec 2020 03:51:05 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:c0f0648876332890be87a9f32ec4ad2a939e805be3152ab991a923f7dec2b35d`  
		Last Modified: Fri, 11 Dec 2020 03:41:39 GMT  
		Size: 30.5 MB (30524717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:833550a83d07a1b6e220c1a79afe3f7627de214a70b02861832cbf79941b586b`  
		Last Modified: Fri, 11 Dec 2020 04:14:40 GMT  
		Size: 256.2 KB (256229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f3ed8da96c8ea7c70fad6716cfd341810be1c4a0a5ed6c88546a60db481d428`  
		Last Modified: Fri, 11 Dec 2020 04:14:46 GMT  
		Size: 29.3 MB (29311114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.12-slim`

```console
$ docker pull mono@sha256:346a69efa561119c7edf438fb9d03e0a1eac5a9e7302585180e781bff0fa87ae
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
$ docker pull mono@sha256:b1ee94f4a5601850bcbd7ddd3e2a432d2d2fccffffd65aef19274dfb7465139b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51598753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0acf66a2efccb8d2b04f037d6c482d855f1ac0a5785ad2d11444fb79a884c4ef`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 11 Dec 2020 02:04:49 GMT
ADD file:58ebb3ffaf26d9b7621efba5f109ae9d22832f2f22865cda36604b138cbdb7b8 in / 
# Fri, 11 Dec 2020 02:04:56 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 03:41:57 GMT
ENV MONO_VERSION=6.12.0.107
# Fri, 11 Dec 2020 03:42:24 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 11 Dec 2020 03:43:10 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:8cbd1f790d64c77fcac6c9dbfe4d4c82f0365de9438f1a42b0560dc88f9e6a55`  
		Last Modified: Fri, 11 Dec 2020 02:14:44 GMT  
		Size: 24.8 MB (24843461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc539c64dc00d4039c50099fac2985998f6c5a718bf3a99b1ed39ca7622e9fcc`  
		Last Modified: Fri, 11 Dec 2020 03:52:45 GMT  
		Size: 256.0 KB (255989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:686f758c22e775b28fea1be4a5cab430f1644e1d6f259657dcd574a30a046d85`  
		Last Modified: Fri, 11 Dec 2020 03:52:59 GMT  
		Size: 26.5 MB (26499303 bytes)  
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
$ docker pull mono@sha256:99059ede7dec72369488f094708b5aee5a3149a5e08eca0e553e6f1a3493fd21
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60092060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0126153e1f3ce853b883f7bf0340bb25f06be319fe89aab5242fdbe98260a8b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 11 Dec 2020 03:34:02 GMT
ADD file:eca1a7737bd5e84ff883c4c284c0cd22492145d9cd7ae3b8e7b490e3d8e5aefb in / 
# Fri, 11 Dec 2020 03:34:11 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 03:47:17 GMT
ENV MONO_VERSION=6.12.0.107
# Fri, 11 Dec 2020 03:48:45 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 11 Dec 2020 03:51:05 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:c0f0648876332890be87a9f32ec4ad2a939e805be3152ab991a923f7dec2b35d`  
		Last Modified: Fri, 11 Dec 2020 03:41:39 GMT  
		Size: 30.5 MB (30524717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:833550a83d07a1b6e220c1a79afe3f7627de214a70b02861832cbf79941b586b`  
		Last Modified: Fri, 11 Dec 2020 04:14:40 GMT  
		Size: 256.2 KB (256229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f3ed8da96c8ea7c70fad6716cfd341810be1c4a0a5ed6c88546a60db481d428`  
		Last Modified: Fri, 11 Dec 2020 04:14:46 GMT  
		Size: 29.3 MB (29311114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6-slim`

```console
$ docker pull mono@sha256:01454354a0a0389e2049ccfb7ff6ba2f81e37618a57af70133a8c0d6f5d231bb
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
$ docker pull mono@sha256:b1ee94f4a5601850bcbd7ddd3e2a432d2d2fccffffd65aef19274dfb7465139b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51598753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0acf66a2efccb8d2b04f037d6c482d855f1ac0a5785ad2d11444fb79a884c4ef`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 11 Dec 2020 02:04:49 GMT
ADD file:58ebb3ffaf26d9b7621efba5f109ae9d22832f2f22865cda36604b138cbdb7b8 in / 
# Fri, 11 Dec 2020 02:04:56 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 03:41:57 GMT
ENV MONO_VERSION=6.12.0.107
# Fri, 11 Dec 2020 03:42:24 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 11 Dec 2020 03:43:10 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:8cbd1f790d64c77fcac6c9dbfe4d4c82f0365de9438f1a42b0560dc88f9e6a55`  
		Last Modified: Fri, 11 Dec 2020 02:14:44 GMT  
		Size: 24.8 MB (24843461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc539c64dc00d4039c50099fac2985998f6c5a718bf3a99b1ed39ca7622e9fcc`  
		Last Modified: Fri, 11 Dec 2020 03:52:45 GMT  
		Size: 256.0 KB (255989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:686f758c22e775b28fea1be4a5cab430f1644e1d6f259657dcd574a30a046d85`  
		Last Modified: Fri, 11 Dec 2020 03:52:59 GMT  
		Size: 26.5 MB (26499303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:287246e970f9f50960368aa4ca97f2e8c1721f5b9055af90534a9f8fbed78e4b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48660947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dffd81d0d1c05541223059044f24fa18217de604218a76ba44f34ef71dd53115`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 11 Dec 2020 02:23:37 GMT
ADD file:75ca842ac2d6e9f6617bb3df280af1e4c9619c9805fd5e00c1c3d6b8b4e3d802 in / 
# Fri, 11 Dec 2020 02:23:39 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 16:04:55 GMT
ENV MONO_VERSION=6.12.0.107
# Fri, 11 Dec 2020 16:05:16 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 11 Dec 2020 16:05:58 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:c06905228d4fc5a5c840a70e2e6ced56596a8bc73abc69e6a1867bbb6f7ae7e7`  
		Last Modified: Fri, 11 Dec 2020 02:33:07 GMT  
		Size: 22.7 MB (22707662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b6050173e7f0c096548a7d0ae4600b1aa634ebd0f04d2a0641e1de70d735a81`  
		Last Modified: Fri, 11 Dec 2020 16:14:05 GMT  
		Size: 256.0 KB (255961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c669a631af9fa12abb498a87e56c428d7767752fae1125211f976b7a97582cc`  
		Last Modified: Fri, 11 Dec 2020 16:14:13 GMT  
		Size: 25.7 MB (25697324 bytes)  
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
$ docker pull mono@sha256:99059ede7dec72369488f094708b5aee5a3149a5e08eca0e553e6f1a3493fd21
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60092060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0126153e1f3ce853b883f7bf0340bb25f06be319fe89aab5242fdbe98260a8b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 11 Dec 2020 03:34:02 GMT
ADD file:eca1a7737bd5e84ff883c4c284c0cd22492145d9cd7ae3b8e7b490e3d8e5aefb in / 
# Fri, 11 Dec 2020 03:34:11 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 03:47:17 GMT
ENV MONO_VERSION=6.12.0.107
# Fri, 11 Dec 2020 03:48:45 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 11 Dec 2020 03:51:05 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:c0f0648876332890be87a9f32ec4ad2a939e805be3152ab991a923f7dec2b35d`  
		Last Modified: Fri, 11 Dec 2020 03:41:39 GMT  
		Size: 30.5 MB (30524717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:833550a83d07a1b6e220c1a79afe3f7627de214a70b02861832cbf79941b586b`  
		Last Modified: Fri, 11 Dec 2020 04:14:40 GMT  
		Size: 256.2 KB (256229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f3ed8da96c8ea7c70fad6716cfd341810be1c4a0a5ed6c88546a60db481d428`  
		Last Modified: Fri, 11 Dec 2020 04:14:46 GMT  
		Size: 29.3 MB (29311114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:latest`

```console
$ docker pull mono@sha256:0c215dd2576ef581ece800b74cf4f9aa1642af6f2923d46cad2d7b5cfcd853ff
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
$ docker pull mono@sha256:facbe0a70ded15ca8315155b22f0ed9176e4fd16040c51dad384c2107ceaf0c1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.7 MB (191705978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43b6e40880e80c6dfd2c3ff378b679952a88601a74d31ed7eca93df4176d3594`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 11 Dec 2020 02:04:49 GMT
ADD file:58ebb3ffaf26d9b7621efba5f109ae9d22832f2f22865cda36604b138cbdb7b8 in / 
# Fri, 11 Dec 2020 02:04:56 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 03:41:57 GMT
ENV MONO_VERSION=6.12.0.107
# Fri, 11 Dec 2020 03:42:24 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 11 Dec 2020 03:43:10 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Fri, 11 Dec 2020 03:47:34 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:8cbd1f790d64c77fcac6c9dbfe4d4c82f0365de9438f1a42b0560dc88f9e6a55`  
		Last Modified: Fri, 11 Dec 2020 02:14:44 GMT  
		Size: 24.8 MB (24843461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc539c64dc00d4039c50099fac2985998f6c5a718bf3a99b1ed39ca7622e9fcc`  
		Last Modified: Fri, 11 Dec 2020 03:52:45 GMT  
		Size: 256.0 KB (255989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:686f758c22e775b28fea1be4a5cab430f1644e1d6f259657dcd574a30a046d85`  
		Last Modified: Fri, 11 Dec 2020 03:52:59 GMT  
		Size: 26.5 MB (26499303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f2b21a188ebe615c0e00705c9bbcdd6a64afd4d2fb9bcde2131024f20bf082d`  
		Last Modified: Fri, 11 Dec 2020 03:54:51 GMT  
		Size: 140.1 MB (140107225 bytes)  
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
$ docker pull mono@sha256:d228a286a9634f5ceb87c4a6880446a34a60dd18fd4f375ff15de765fdf6f3b1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.3 MB (203315195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3ba7e6d47f9b23521f48b0071ccec29f62ed8ecb7f0b9d923452236802a6c02`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 11 Dec 2020 03:34:02 GMT
ADD file:eca1a7737bd5e84ff883c4c284c0cd22492145d9cd7ae3b8e7b490e3d8e5aefb in / 
# Fri, 11 Dec 2020 03:34:11 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 03:47:17 GMT
ENV MONO_VERSION=6.12.0.107
# Fri, 11 Dec 2020 03:48:45 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 11 Dec 2020 03:51:05 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Fri, 11 Dec 2020 04:05:16 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:c0f0648876332890be87a9f32ec4ad2a939e805be3152ab991a923f7dec2b35d`  
		Last Modified: Fri, 11 Dec 2020 03:41:39 GMT  
		Size: 30.5 MB (30524717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:833550a83d07a1b6e220c1a79afe3f7627de214a70b02861832cbf79941b586b`  
		Last Modified: Fri, 11 Dec 2020 04:14:40 GMT  
		Size: 256.2 KB (256229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f3ed8da96c8ea7c70fad6716cfd341810be1c4a0a5ed6c88546a60db481d428`  
		Last Modified: Fri, 11 Dec 2020 04:14:46 GMT  
		Size: 29.3 MB (29311114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9499aa37e5b0b65ee6a349eb1fbcfdeabfb3916c0f0299ce5a99ecead9ee8df`  
		Last Modified: Fri, 11 Dec 2020 04:15:56 GMT  
		Size: 143.2 MB (143223135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:slim`

```console
$ docker pull mono@sha256:346a69efa561119c7edf438fb9d03e0a1eac5a9e7302585180e781bff0fa87ae
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
$ docker pull mono@sha256:b1ee94f4a5601850bcbd7ddd3e2a432d2d2fccffffd65aef19274dfb7465139b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51598753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0acf66a2efccb8d2b04f037d6c482d855f1ac0a5785ad2d11444fb79a884c4ef`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 11 Dec 2020 02:04:49 GMT
ADD file:58ebb3ffaf26d9b7621efba5f109ae9d22832f2f22865cda36604b138cbdb7b8 in / 
# Fri, 11 Dec 2020 02:04:56 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 03:41:57 GMT
ENV MONO_VERSION=6.12.0.107
# Fri, 11 Dec 2020 03:42:24 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 11 Dec 2020 03:43:10 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:8cbd1f790d64c77fcac6c9dbfe4d4c82f0365de9438f1a42b0560dc88f9e6a55`  
		Last Modified: Fri, 11 Dec 2020 02:14:44 GMT  
		Size: 24.8 MB (24843461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc539c64dc00d4039c50099fac2985998f6c5a718bf3a99b1ed39ca7622e9fcc`  
		Last Modified: Fri, 11 Dec 2020 03:52:45 GMT  
		Size: 256.0 KB (255989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:686f758c22e775b28fea1be4a5cab430f1644e1d6f259657dcd574a30a046d85`  
		Last Modified: Fri, 11 Dec 2020 03:52:59 GMT  
		Size: 26.5 MB (26499303 bytes)  
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
$ docker pull mono@sha256:99059ede7dec72369488f094708b5aee5a3149a5e08eca0e553e6f1a3493fd21
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60092060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0126153e1f3ce853b883f7bf0340bb25f06be319fe89aab5242fdbe98260a8b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 11 Dec 2020 03:34:02 GMT
ADD file:eca1a7737bd5e84ff883c4c284c0cd22492145d9cd7ae3b8e7b490e3d8e5aefb in / 
# Fri, 11 Dec 2020 03:34:11 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 03:47:17 GMT
ENV MONO_VERSION=6.12.0.107
# Fri, 11 Dec 2020 03:48:45 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 11 Dec 2020 03:51:05 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:c0f0648876332890be87a9f32ec4ad2a939e805be3152ab991a923f7dec2b35d`  
		Last Modified: Fri, 11 Dec 2020 03:41:39 GMT  
		Size: 30.5 MB (30524717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:833550a83d07a1b6e220c1a79afe3f7627de214a70b02861832cbf79941b586b`  
		Last Modified: Fri, 11 Dec 2020 04:14:40 GMT  
		Size: 256.2 KB (256229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f3ed8da96c8ea7c70fad6716cfd341810be1c4a0a5ed6c88546a60db481d428`  
		Last Modified: Fri, 11 Dec 2020 04:14:46 GMT  
		Size: 29.3 MB (29311114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
