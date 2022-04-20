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
$ docker pull mono@sha256:288dce942fc8031ee29e492d5c8f6beec7d6a38df14ee0f8cf28070d4d555e44
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
$ docker pull mono@sha256:abcb22d3b82c95b20ff5c90f329cb759314b70e1781a67315b1ec2bb719e0cda
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.1 MB (236137951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a0982a1a3d0d9f836f390567b3d9452c91ca96d6b8b2e633edf0cf7994be535`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:38 GMT
ADD file:59187422476c57db46e60f894a4cfd0f243e80230ef9ea75b2d8dd4925d59df3 in / 
# Tue, 29 Mar 2022 00:22:38 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 22:50:30 GMT
ENV MONO_VERSION=6.12.0.122
# Tue, 29 Mar 2022 22:50:38 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 29 Mar 2022 22:51:01 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 29 Mar 2022 22:56:06 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:f003217c5aaebdfee0b9a448fbabd995e5f0159f5b231460c0ecc21baf171953`  
		Last Modified: Tue, 29 Mar 2022 00:28:02 GMT  
		Size: 27.2 MB (27151970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d839cde201cd1385a1c2c927214c614f1cd1bab02a62fd34b6df69e6f95daa7e`  
		Last Modified: Tue, 29 Mar 2022 23:02:05 GMT  
		Size: 2.8 MB (2777377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:158befabd0cf5fbeb7cb51a0cfc2f6c20399efe3be6abfd6d7dc8187d886b4a0`  
		Last Modified: Tue, 29 Mar 2022 23:02:14 GMT  
		Size: 64.8 MB (64760477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7f69220c106af4aa5ecc61935d51050e43fe6450996488e6c1d7fe5c5d7c2e1`  
		Last Modified: Tue, 29 Mar 2022 23:03:13 GMT  
		Size: 141.4 MB (141448127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6` - linux; arm variant v5

```console
$ docker pull mono@sha256:7f7e694bccdf74a53d7491c00db8088add1265f44830d8b0a365c7915304ef04
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.0 MB (191954448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71bb1b7df7ff58e8b649bb79421666f8422e0606d35629b29b8cf7c2b7ca4596`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:51:36 GMT
ADD file:7ac5498e2c44686d7eb272ef7645a0a64486cf942610f6754aa4a932f5b1a4be in / 
# Tue, 29 Mar 2022 00:51:37 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 08:50:15 GMT
ENV MONO_VERSION=6.12.0.122
# Tue, 29 Mar 2022 08:50:42 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 29 Mar 2022 08:51:31 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 29 Mar 2022 08:56:31 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:8f10b1b67f0119a2dd5f838a3e98ab2c412e4b51fb1e4841e2b79fd4cae86105`  
		Last Modified: Tue, 29 Mar 2022 01:06:51 GMT  
		Size: 24.9 MB (24887495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:103ccfc95d14718dd5bd47005c93225d5f82bdc075ccfc346e1b366afb616d57`  
		Last Modified: Tue, 29 Mar 2022 09:01:39 GMT  
		Size: 2.5 MB (2467692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13697b82f395905c310bf0030c74844e8f8fc5979a009c041a18de4488636164`  
		Last Modified: Tue, 29 Mar 2022 09:01:50 GMT  
		Size: 24.5 MB (24493260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90cc18056a6a14a94b009cdae75817ab5f9d1bea6b12aaf50cf5127985d9277f`  
		Last Modified: Tue, 29 Mar 2022 09:04:22 GMT  
		Size: 140.1 MB (140106001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6` - linux; arm variant v7

```console
$ docker pull mono@sha256:de55a06147b60da0b002c65b61e35e5bbcd09bb5d0a3c734b2004494af9e90b5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.9 MB (187869490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:068cd3b6737d2700c491cd15edf19aa585b83d26ea05ebaa0f5602558b0e57b7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 02:19:40 GMT
ADD file:8d54e000817531229c35a32eee074105c7b4d3c08b7ca56b1abdd80571687f28 in / 
# Tue, 29 Mar 2022 02:19:41 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 21:55:56 GMT
ENV MONO_VERSION=6.12.0.122
# Wed, 30 Mar 2022 21:56:22 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 30 Mar 2022 21:57:04 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 30 Mar 2022 22:01:31 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:d4bf0b27c669e589de33695047d638174fc2ca819a4366d5f80d1ad6b01c0c0e`  
		Last Modified: Tue, 29 Mar 2022 02:35:26 GMT  
		Size: 22.8 MB (22753045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:756cc431341070c1f6a772929e5d5daab96f2b040732e70d3cb93b3ce98d8542`  
		Last Modified: Wed, 30 Mar 2022 22:06:01 GMT  
		Size: 2.4 MB (2366920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:419ca67b5ee0885d9bcc46429070d185a04feb680b643fc29ceda334987a6a6f`  
		Last Modified: Wed, 30 Mar 2022 22:06:18 GMT  
		Size: 23.8 MB (23782719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:672029c9759800f327c1f06dc30ce05aac300a39d8f40f9c5d475f006a5486ba`  
		Last Modified: Wed, 30 Mar 2022 22:08:52 GMT  
		Size: 139.0 MB (138966806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:617fd6f5ff9238ff8782c0b154f5fbb1e51864ad1f009da0d0c5fcd54ff179c0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.5 MB (214465680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:721976153f55a700a3368032ce347eb3ae7b930fc6151b879332e0e99f1ca0cc`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Apr 2022 04:29:36 GMT
ADD file:5de4397c1295f7249c93907be599d96efbd9cd25909340d245ec8d1c9770f444 in / 
# Wed, 20 Apr 2022 04:29:37 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 09:34:15 GMT
ENV MONO_VERSION=6.12.0.122
# Wed, 20 Apr 2022 09:34:25 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 20 Apr 2022 09:34:40 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 20 Apr 2022 09:36:17 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:6c3e5b218d6477ff77053280968d5bdeaa5dcf16a803e917d98dd0ea8b93ac82`  
		Last Modified: Wed, 20 Apr 2022 04:36:38 GMT  
		Size: 25.9 MB (25908349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a5583d434a71d4775ae033dd3567325a5f5d01a34ff9f805631b17426570d60`  
		Last Modified: Wed, 20 Apr 2022 09:38:16 GMT  
		Size: 2.6 MB (2641065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1df7a4f3775402176b947b2ffb1f930879581b64904846f29bd8e5aa4000e4d`  
		Last Modified: Wed, 20 Apr 2022 09:38:20 GMT  
		Size: 29.3 MB (29318359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7f80c1eac9d435a1e808ae3c8eaf8a76d9e653e54edc1090cf4c2fc47f29f6e`  
		Last Modified: Wed, 20 Apr 2022 09:39:21 GMT  
		Size: 156.6 MB (156597907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6` - linux; 386

```console
$ docker pull mono@sha256:ef781f5c402c37c294ccf7397654b6a780c16c68ab05b1ee598260446e0049b0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.7 MB (241696337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faa267e26ab7e853336277f2575154ad396b6536c3cd9e8ba22824250ccc6fbd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Apr 2022 07:38:03 GMT
ADD file:602a25173054242f635a5a299845b7f1b56864ac5d3b8af1ae29dec3a9da119f in / 
# Wed, 20 Apr 2022 07:38:04 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 12:49:08 GMT
ENV MONO_VERSION=6.12.0.122
# Wed, 20 Apr 2022 12:49:17 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 20 Apr 2022 12:49:40 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 20 Apr 2022 12:51:19 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a13b13d818745c4d2234aab71df26e4a01bfe59f396ab62f20d156b94803650c`  
		Last Modified: Wed, 20 Apr 2022 07:45:46 GMT  
		Size: 27.8 MB (27799825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc07624832ff4b064bd2b3797a6774618e27f4c3a1e24419874628eeb613e7ba`  
		Last Modified: Wed, 20 Apr 2022 12:53:02 GMT  
		Size: 2.8 MB (2789161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d6af1a94baa95c219eaba2db2fb27e299572ac8d2859e1399838abdccae784c`  
		Last Modified: Wed, 20 Apr 2022 12:53:11 GMT  
		Size: 68.6 MB (68568946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cec0646bfa3d97be6f7515ad03d0cbb859adebe6cf3785cf1d36d06c8aa3f224`  
		Last Modified: Wed, 20 Apr 2022 12:54:22 GMT  
		Size: 142.5 MB (142538405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6` - linux; ppc64le

```console
$ docker pull mono@sha256:d8969fd75bcf7f2415543c536c50458a18d28e8cdab323db80eb053827d08c60
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.6 MB (203608008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:226cb9d82e8bfc2114d8f6e225a71870230cc71a214527422e1a68b2185008bc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:59 GMT
ADD file:7271d778d432a07f57fedf8d50d83699ef545acc9db9346f6fe75b0054af4cd1 in / 
# Tue, 29 Mar 2022 00:23:00 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 06:30:50 GMT
ENV MONO_VERSION=6.12.0.122
# Wed, 30 Mar 2022 06:32:19 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 30 Mar 2022 06:33:27 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 30 Mar 2022 06:43:44 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7db831386ce67ac1cf2b4f1513fe3746c9ea2b8d4c82efca75be638eaf533614`  
		Last Modified: Tue, 29 Mar 2022 00:34:41 GMT  
		Size: 30.6 MB (30560163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55feab57ab15634326c723014da448815650e9737d6c5671ca5a4cd4503905cb`  
		Last Modified: Wed, 30 Mar 2022 06:53:14 GMT  
		Size: 2.9 MB (2892687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c00a3dcf742861f8ca53669004126ef6bead547f42b4f28c1d7ba21debbc8b5`  
		Last Modified: Wed, 30 Mar 2022 06:53:20 GMT  
		Size: 26.9 MB (26873425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af736d47f1875d0d79d7c43b3fce41fcb3f2129622c09182d7916c44b731e9b2`  
		Last Modified: Wed, 30 Mar 2022 06:54:30 GMT  
		Size: 143.3 MB (143281733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6-slim`

```console
$ docker pull mono@sha256:bc7933bac89d6c7f5e9c656111b402a44420deb7a05c7adefcef682c114cc212
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
$ docker pull mono@sha256:87038a7da02d5efff3bfab1ec93dc3020d04cd3fad6bff479d3252cf3cb13695
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.7 MB (94689824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcc621103738e68eb59281907e2ec643435dbb8dd82d504d49655526191a0199`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:38 GMT
ADD file:59187422476c57db46e60f894a4cfd0f243e80230ef9ea75b2d8dd4925d59df3 in / 
# Tue, 29 Mar 2022 00:22:38 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 22:50:30 GMT
ENV MONO_VERSION=6.12.0.122
# Tue, 29 Mar 2022 22:50:38 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 29 Mar 2022 22:51:01 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:f003217c5aaebdfee0b9a448fbabd995e5f0159f5b231460c0ecc21baf171953`  
		Last Modified: Tue, 29 Mar 2022 00:28:02 GMT  
		Size: 27.2 MB (27151970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d839cde201cd1385a1c2c927214c614f1cd1bab02a62fd34b6df69e6f95daa7e`  
		Last Modified: Tue, 29 Mar 2022 23:02:05 GMT  
		Size: 2.8 MB (2777377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:158befabd0cf5fbeb7cb51a0cfc2f6c20399efe3be6abfd6d7dc8187d886b4a0`  
		Last Modified: Tue, 29 Mar 2022 23:02:14 GMT  
		Size: 64.8 MB (64760477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:2858e2824edbcaaefd73dd8b888c39d6c10cfd27bc7b2b1b420570403b00a924
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51848447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41535ed442f086e8d8103e40ebab589e248cc742505317bfb8c17b5746bc567f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:51:36 GMT
ADD file:7ac5498e2c44686d7eb272ef7645a0a64486cf942610f6754aa4a932f5b1a4be in / 
# Tue, 29 Mar 2022 00:51:37 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 08:50:15 GMT
ENV MONO_VERSION=6.12.0.122
# Tue, 29 Mar 2022 08:50:42 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 29 Mar 2022 08:51:31 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:8f10b1b67f0119a2dd5f838a3e98ab2c412e4b51fb1e4841e2b79fd4cae86105`  
		Last Modified: Tue, 29 Mar 2022 01:06:51 GMT  
		Size: 24.9 MB (24887495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:103ccfc95d14718dd5bd47005c93225d5f82bdc075ccfc346e1b366afb616d57`  
		Last Modified: Tue, 29 Mar 2022 09:01:39 GMT  
		Size: 2.5 MB (2467692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13697b82f395905c310bf0030c74844e8f8fc5979a009c041a18de4488636164`  
		Last Modified: Tue, 29 Mar 2022 09:01:50 GMT  
		Size: 24.5 MB (24493260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:c8f9bff7726932d61ceb479135172d8ad8d953634e902d99afa4b04b35c8979c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48902684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35df12dffc423503a586d8b0c8f4b5056157ba44d8baa9a3a8ebc94f4b728f4e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 02:19:40 GMT
ADD file:8d54e000817531229c35a32eee074105c7b4d3c08b7ca56b1abdd80571687f28 in / 
# Tue, 29 Mar 2022 02:19:41 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 21:55:56 GMT
ENV MONO_VERSION=6.12.0.122
# Wed, 30 Mar 2022 21:56:22 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 30 Mar 2022 21:57:04 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:d4bf0b27c669e589de33695047d638174fc2ca819a4366d5f80d1ad6b01c0c0e`  
		Last Modified: Tue, 29 Mar 2022 02:35:26 GMT  
		Size: 22.8 MB (22753045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:756cc431341070c1f6a772929e5d5daab96f2b040732e70d3cb93b3ce98d8542`  
		Last Modified: Wed, 30 Mar 2022 22:06:01 GMT  
		Size: 2.4 MB (2366920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:419ca67b5ee0885d9bcc46429070d185a04feb680b643fc29ceda334987a6a6f`  
		Last Modified: Wed, 30 Mar 2022 22:06:18 GMT  
		Size: 23.8 MB (23782719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:0f3837c80f89d4cc61d33d11680310dd7b9170aa4a20287829db1cf4ff83169c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.9 MB (57867773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a03207fd5f3c9c31e878dec4d955581897e75177774ac4915f726360915f8e8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Apr 2022 04:29:36 GMT
ADD file:5de4397c1295f7249c93907be599d96efbd9cd25909340d245ec8d1c9770f444 in / 
# Wed, 20 Apr 2022 04:29:37 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 09:34:15 GMT
ENV MONO_VERSION=6.12.0.122
# Wed, 20 Apr 2022 09:34:25 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 20 Apr 2022 09:34:40 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:6c3e5b218d6477ff77053280968d5bdeaa5dcf16a803e917d98dd0ea8b93ac82`  
		Last Modified: Wed, 20 Apr 2022 04:36:38 GMT  
		Size: 25.9 MB (25908349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a5583d434a71d4775ae033dd3567325a5f5d01a34ff9f805631b17426570d60`  
		Last Modified: Wed, 20 Apr 2022 09:38:16 GMT  
		Size: 2.6 MB (2641065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1df7a4f3775402176b947b2ffb1f930879581b64904846f29bd8e5aa4000e4d`  
		Last Modified: Wed, 20 Apr 2022 09:38:20 GMT  
		Size: 29.3 MB (29318359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6-slim` - linux; 386

```console
$ docker pull mono@sha256:a620c36d6b438c94797eaa6b17b2452369ac55ab8a59a1bcf8b4501df1eea0c5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.2 MB (99157932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95ff55aea4f3ffc1da74cea929a23a78ed6dc8901847098c5878018368c9da5d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Apr 2022 07:38:03 GMT
ADD file:602a25173054242f635a5a299845b7f1b56864ac5d3b8af1ae29dec3a9da119f in / 
# Wed, 20 Apr 2022 07:38:04 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 12:49:08 GMT
ENV MONO_VERSION=6.12.0.122
# Wed, 20 Apr 2022 12:49:17 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 20 Apr 2022 12:49:40 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a13b13d818745c4d2234aab71df26e4a01bfe59f396ab62f20d156b94803650c`  
		Last Modified: Wed, 20 Apr 2022 07:45:46 GMT  
		Size: 27.8 MB (27799825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc07624832ff4b064bd2b3797a6774618e27f4c3a1e24419874628eeb613e7ba`  
		Last Modified: Wed, 20 Apr 2022 12:53:02 GMT  
		Size: 2.8 MB (2789161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d6af1a94baa95c219eaba2db2fb27e299572ac8d2859e1399838abdccae784c`  
		Last Modified: Wed, 20 Apr 2022 12:53:11 GMT  
		Size: 68.6 MB (68568946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:9b3a0defce0a5c2ae9bfc6d34af244911ccd407e7973e0f3eedce5fe3670f57e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60326275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5184331441c848755861d28d51bfb13f10dc8e51ace7607db24b3326be9c1166`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:59 GMT
ADD file:7271d778d432a07f57fedf8d50d83699ef545acc9db9346f6fe75b0054af4cd1 in / 
# Tue, 29 Mar 2022 00:23:00 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 06:30:50 GMT
ENV MONO_VERSION=6.12.0.122
# Wed, 30 Mar 2022 06:32:19 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 30 Mar 2022 06:33:27 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7db831386ce67ac1cf2b4f1513fe3746c9ea2b8d4c82efca75be638eaf533614`  
		Last Modified: Tue, 29 Mar 2022 00:34:41 GMT  
		Size: 30.6 MB (30560163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55feab57ab15634326c723014da448815650e9737d6c5671ca5a4cd4503905cb`  
		Last Modified: Wed, 30 Mar 2022 06:53:14 GMT  
		Size: 2.9 MB (2892687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c00a3dcf742861f8ca53669004126ef6bead547f42b4f28c1d7ba21debbc8b5`  
		Last Modified: Wed, 30 Mar 2022 06:53:20 GMT  
		Size: 26.9 MB (26873425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.10`

```console
$ docker pull mono@sha256:2c1cdfc346d2b4708c4985a17fffc9f2a5bd2701402c3fa85c60b1cee6052f53
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
$ docker pull mono@sha256:7d05fdb89242ddd492352dd07e116e4265a0bc74887cdbec241e678bda999e8d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.0 MB (225016606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd568696105f84add5464497cd947fbc9578d6d45bdc8d6581a6cd3b8ab308ef`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:38 GMT
ADD file:59187422476c57db46e60f894a4cfd0f243e80230ef9ea75b2d8dd4925d59df3 in / 
# Tue, 29 Mar 2022 00:22:38 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 22:51:04 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 29 Mar 2022 22:51:12 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 29 Mar 2022 22:51:39 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 29 Mar 2022 23:01:35 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:f003217c5aaebdfee0b9a448fbabd995e5f0159f5b231460c0ecc21baf171953`  
		Last Modified: Tue, 29 Mar 2022 00:28:02 GMT  
		Size: 27.2 MB (27151970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ae9dab17d49756cbd842116bb4c8ecb5a2d64d39c08d729451e14400a8b433f`  
		Last Modified: Tue, 29 Mar 2022 23:02:31 GMT  
		Size: 2.8 MB (2777394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a496246b00b4b65da977fb279486fb8752dd631c5119990bb08a199626d0ee3`  
		Last Modified: Tue, 29 Mar 2022 23:02:41 GMT  
		Size: 64.8 MB (64778479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ac0981c4bbcf3da52e65fa962a538ab5a5aa9e4aebf9ebcdb25780723272e10`  
		Last Modified: Tue, 29 Mar 2022 23:03:49 GMT  
		Size: 130.3 MB (130308763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10` - linux; arm variant v5

```console
$ docker pull mono@sha256:c258968ed62efa47680adb7fc1435612b46ad3b48d63ed93093f319cdab04935
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.9 MB (180855371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7caefcc734f172d8b5b345e474f7e7e113a9b40e6e7eb92cadbb0c680abc6c8f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:51:36 GMT
ADD file:7ac5498e2c44686d7eb272ef7645a0a64486cf942610f6754aa4a932f5b1a4be in / 
# Tue, 29 Mar 2022 00:51:37 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 08:51:50 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 29 Mar 2022 08:52:17 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 29 Mar 2022 08:53:05 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 29 Mar 2022 09:00:04 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:8f10b1b67f0119a2dd5f838a3e98ab2c412e4b51fb1e4841e2b79fd4cae86105`  
		Last Modified: Tue, 29 Mar 2022 01:06:51 GMT  
		Size: 24.9 MB (24887495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a48926cfb9ba33532fb4a1f42ce2a984010491b46d8002b4db306c821d4e10f4`  
		Last Modified: Tue, 29 Mar 2022 09:02:13 GMT  
		Size: 2.5 MB (2467645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f429b0f7cd5e4638b807cc3bab5e07aaddbf1b55eb066703c660685b59adfe2c`  
		Last Modified: Tue, 29 Mar 2022 09:02:29 GMT  
		Size: 24.5 MB (24521524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8edee1c13cf6286aa56485e7352b2a7fe83505c4807123216a51538d9382f3bb`  
		Last Modified: Tue, 29 Mar 2022 09:06:16 GMT  
		Size: 129.0 MB (128978707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10` - linux; arm variant v7

```console
$ docker pull mono@sha256:96c725241edcf4d0f1e81cd0bd8d986a517516b802d3f2e1b8b93f07dc85a545
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.8 MB (176764272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70f601485ff40d1369d729a725cae9ef7a65addf94e8d47aedd20e919380aebf`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 02:19:40 GMT
ADD file:8d54e000817531229c35a32eee074105c7b4d3c08b7ca56b1abdd80571687f28 in / 
# Tue, 29 Mar 2022 02:19:41 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 21:57:19 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 30 Mar 2022 21:57:44 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 30 Mar 2022 21:58:27 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 30 Mar 2022 22:04:35 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:d4bf0b27c669e589de33695047d638174fc2ca819a4366d5f80d1ad6b01c0c0e`  
		Last Modified: Tue, 29 Mar 2022 02:35:26 GMT  
		Size: 22.8 MB (22753045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56011a574ad043bc367af54ab51081b83c20f4fe32556bd822cbcf01be0df28f`  
		Last Modified: Wed, 30 Mar 2022 22:06:42 GMT  
		Size: 2.4 MB (2366866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0562aaca95b07d80f29aaea2ea5f8560179271cd296e0e14f9118c113b715d1`  
		Last Modified: Wed, 30 Mar 2022 22:06:58 GMT  
		Size: 23.8 MB (23814839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4069a4b0106e127b7d470d7d0d21eeac4b14eab70c362cf2cd382ea10cf32ab`  
		Last Modified: Wed, 30 Mar 2022 22:10:46 GMT  
		Size: 127.8 MB (127829522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:db4ccba0ea3a15d03bce129dc7b8f8c1d17eb414d22d0ce50f04c91aa9dc8e6b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.4 MB (203357942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:542f1d2be1793e91d33d40c760fdeff6d2626a9c03e0bb060de4fc1929460c11`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Apr 2022 04:29:36 GMT
ADD file:5de4397c1295f7249c93907be599d96efbd9cd25909340d245ec8d1c9770f444 in / 
# Wed, 20 Apr 2022 04:29:37 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 09:34:48 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 20 Apr 2022 09:34:57 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 20 Apr 2022 09:35:12 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 20 Apr 2022 09:37:30 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:6c3e5b218d6477ff77053280968d5bdeaa5dcf16a803e917d98dd0ea8b93ac82`  
		Last Modified: Wed, 20 Apr 2022 04:36:38 GMT  
		Size: 25.9 MB (25908349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df56c08b5590c539b81f96718f5057b07ceaaf7017a28704b0f095af7166af2f`  
		Last Modified: Wed, 20 Apr 2022 09:38:39 GMT  
		Size: 2.6 MB (2641023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a34f53b7c9a1d5af7034cdc60069b6b9c3b2099c676574b0de7e22085ba360dc`  
		Last Modified: Wed, 20 Apr 2022 09:38:44 GMT  
		Size: 29.4 MB (29361704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a3f7de6536f999251c110135ca6a52d08565af7071c6fe5eea96fbd6578aa58`  
		Last Modified: Wed, 20 Apr 2022 09:40:03 GMT  
		Size: 145.4 MB (145446866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10` - linux; 386

```console
$ docker pull mono@sha256:3e640bbe614e2c612a0234a760239253353017f54ea632d8e70ca5007fc1129d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.6 MB (230599389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38c8b38fb0ee5f997e90812c188e9956c7ea18acf1131589a9e1d93bc640c80a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Apr 2022 07:38:03 GMT
ADD file:602a25173054242f635a5a299845b7f1b56864ac5d3b8af1ae29dec3a9da119f in / 
# Wed, 20 Apr 2022 07:38:04 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 12:49:46 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 20 Apr 2022 12:49:55 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 20 Apr 2022 12:50:19 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 20 Apr 2022 12:52:21 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a13b13d818745c4d2234aab71df26e4a01bfe59f396ab62f20d156b94803650c`  
		Last Modified: Wed, 20 Apr 2022 07:45:46 GMT  
		Size: 27.8 MB (27799825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc19bd2071107b873877fbe3bf3e623d524ecd131b76d25f818ed40f8888a5ae`  
		Last Modified: Wed, 20 Apr 2022 12:53:33 GMT  
		Size: 2.8 MB (2789172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c731ec96f4a6bd8004ee92ad713c93444a1f646c970369e7c6d60ed2ffcf37b`  
		Last Modified: Wed, 20 Apr 2022 12:53:47 GMT  
		Size: 68.6 MB (68594373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0af0ca9622588725474f2f5434ce305f02b1b9a597c878f49af99e99c444e22d`  
		Last Modified: Wed, 20 Apr 2022 12:55:04 GMT  
		Size: 131.4 MB (131416019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10` - linux; ppc64le

```console
$ docker pull mono@sha256:ccbe3a2584d91b1ca5c73d0bbd0dd764fb51f342832b8a644ab523169d6f071f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.4 MB (192388947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaf8e4db6dcac0e22d89a234e7bdb9d9fa90a402a650c944f4ca1d61c758dc18`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:59 GMT
ADD file:7271d778d432a07f57fedf8d50d83699ef545acc9db9346f6fe75b0054af4cd1 in / 
# Tue, 29 Mar 2022 00:23:00 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 06:33:42 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 30 Mar 2022 06:35:18 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 30 Mar 2022 06:36:24 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 30 Mar 2022 06:52:21 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7db831386ce67ac1cf2b4f1513fe3746c9ea2b8d4c82efca75be638eaf533614`  
		Last Modified: Tue, 29 Mar 2022 00:34:41 GMT  
		Size: 30.6 MB (30560163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5beee7bbe2070c64db910f012c8de134f5d7e04cce73425b9b3252cfdac7dabf`  
		Last Modified: Wed, 30 Mar 2022 06:53:43 GMT  
		Size: 2.9 MB (2892707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cecf8b2b1c2486a60cd71f13b29a003199e7acfb8e65eb35a7103d2be2c21424`  
		Last Modified: Wed, 30 Mar 2022 06:53:48 GMT  
		Size: 26.9 MB (26917725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cc6f7f81b1a255a5706b8520a6843611040386aedd1032c8ae7325fb6e5b8bd`  
		Last Modified: Wed, 30 Mar 2022 06:55:16 GMT  
		Size: 132.0 MB (132018352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.10-slim`

```console
$ docker pull mono@sha256:41df20dd54c69b2ef78feba5472d309ebdd8ae0763ec4a5d087e6080c9f23932
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
$ docker pull mono@sha256:2434c8862d32d50b83dd36a485d026303c92cae34ef6ff56186d003f637ff8c8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.7 MB (94707843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f7a8dd762bb2153e2729296500f08d54e3a73061201f49d96977f8572d33531`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:38 GMT
ADD file:59187422476c57db46e60f894a4cfd0f243e80230ef9ea75b2d8dd4925d59df3 in / 
# Tue, 29 Mar 2022 00:22:38 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 22:51:04 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 29 Mar 2022 22:51:12 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 29 Mar 2022 22:51:39 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:f003217c5aaebdfee0b9a448fbabd995e5f0159f5b231460c0ecc21baf171953`  
		Last Modified: Tue, 29 Mar 2022 00:28:02 GMT  
		Size: 27.2 MB (27151970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ae9dab17d49756cbd842116bb4c8ecb5a2d64d39c08d729451e14400a8b433f`  
		Last Modified: Tue, 29 Mar 2022 23:02:31 GMT  
		Size: 2.8 MB (2777394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a496246b00b4b65da977fb279486fb8752dd631c5119990bb08a199626d0ee3`  
		Last Modified: Tue, 29 Mar 2022 23:02:41 GMT  
		Size: 64.8 MB (64778479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:cf2c912a55906fd6a4e96d2ca6c0adc9b64765ec9feb9c2b3763aaea11e645ce
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.9 MB (51876664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a031511624fa3c816d95f06c0692434ee36e2a5d28235d0c83863ebe44463281`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:51:36 GMT
ADD file:7ac5498e2c44686d7eb272ef7645a0a64486cf942610f6754aa4a932f5b1a4be in / 
# Tue, 29 Mar 2022 00:51:37 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 08:51:50 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 29 Mar 2022 08:52:17 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 29 Mar 2022 08:53:05 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:8f10b1b67f0119a2dd5f838a3e98ab2c412e4b51fb1e4841e2b79fd4cae86105`  
		Last Modified: Tue, 29 Mar 2022 01:06:51 GMT  
		Size: 24.9 MB (24887495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a48926cfb9ba33532fb4a1f42ce2a984010491b46d8002b4db306c821d4e10f4`  
		Last Modified: Tue, 29 Mar 2022 09:02:13 GMT  
		Size: 2.5 MB (2467645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f429b0f7cd5e4638b807cc3bab5e07aaddbf1b55eb066703c660685b59adfe2c`  
		Last Modified: Tue, 29 Mar 2022 09:02:29 GMT  
		Size: 24.5 MB (24521524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:1b48beb386f0dee7a252b4f4a39555729e170af382d2ca70a386cbc849fed677
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48934750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f29fa6f525c588db746b1f3a3eed667e5aef45aae3eb6db3953ba52d6ff6d45`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 02:19:40 GMT
ADD file:8d54e000817531229c35a32eee074105c7b4d3c08b7ca56b1abdd80571687f28 in / 
# Tue, 29 Mar 2022 02:19:41 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 21:57:19 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 30 Mar 2022 21:57:44 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 30 Mar 2022 21:58:27 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:d4bf0b27c669e589de33695047d638174fc2ca819a4366d5f80d1ad6b01c0c0e`  
		Last Modified: Tue, 29 Mar 2022 02:35:26 GMT  
		Size: 22.8 MB (22753045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56011a574ad043bc367af54ab51081b83c20f4fe32556bd822cbcf01be0df28f`  
		Last Modified: Wed, 30 Mar 2022 22:06:42 GMT  
		Size: 2.4 MB (2366866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0562aaca95b07d80f29aaea2ea5f8560179271cd296e0e14f9118c113b715d1`  
		Last Modified: Wed, 30 Mar 2022 22:06:58 GMT  
		Size: 23.8 MB (23814839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:fd0ffe089ab133d58978ea5e51d43135e9a8c87b86be3997fd1e5b0d581cc2ee
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.9 MB (57911076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:147cc7fd6295707399eab462793e12cbddb6d439837b2897b3c69b2125dbc6e2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Apr 2022 04:29:36 GMT
ADD file:5de4397c1295f7249c93907be599d96efbd9cd25909340d245ec8d1c9770f444 in / 
# Wed, 20 Apr 2022 04:29:37 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 09:34:48 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 20 Apr 2022 09:34:57 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 20 Apr 2022 09:35:12 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:6c3e5b218d6477ff77053280968d5bdeaa5dcf16a803e917d98dd0ea8b93ac82`  
		Last Modified: Wed, 20 Apr 2022 04:36:38 GMT  
		Size: 25.9 MB (25908349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df56c08b5590c539b81f96718f5057b07ceaaf7017a28704b0f095af7166af2f`  
		Last Modified: Wed, 20 Apr 2022 09:38:39 GMT  
		Size: 2.6 MB (2641023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a34f53b7c9a1d5af7034cdc60069b6b9c3b2099c676574b0de7e22085ba360dc`  
		Last Modified: Wed, 20 Apr 2022 09:38:44 GMT  
		Size: 29.4 MB (29361704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10-slim` - linux; 386

```console
$ docker pull mono@sha256:8a2f06c25415df8cc6ae7315e81ca06a9ff079a357c05caf0d1b57045ad265fa
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.2 MB (99183370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a4588d79da86f7cab111b6c2fc82a13c1680b1134d953242a251f3c0da28b4a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Apr 2022 07:38:03 GMT
ADD file:602a25173054242f635a5a299845b7f1b56864ac5d3b8af1ae29dec3a9da119f in / 
# Wed, 20 Apr 2022 07:38:04 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 12:49:46 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 20 Apr 2022 12:49:55 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 20 Apr 2022 12:50:19 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a13b13d818745c4d2234aab71df26e4a01bfe59f396ab62f20d156b94803650c`  
		Last Modified: Wed, 20 Apr 2022 07:45:46 GMT  
		Size: 27.8 MB (27799825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc19bd2071107b873877fbe3bf3e623d524ecd131b76d25f818ed40f8888a5ae`  
		Last Modified: Wed, 20 Apr 2022 12:53:33 GMT  
		Size: 2.8 MB (2789172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c731ec96f4a6bd8004ee92ad713c93444a1f646c970369e7c6d60ed2ffcf37b`  
		Last Modified: Wed, 20 Apr 2022 12:53:47 GMT  
		Size: 68.6 MB (68594373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:949677eaaf0421b89ed25dc185f9ca51c2b21b0aaff569226a3f3a9a49cf0649
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.4 MB (60370595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a37887fb66d953ed3542898f048cd47ccbde3d6b9532aefb36b9877cdb8bff93`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:59 GMT
ADD file:7271d778d432a07f57fedf8d50d83699ef545acc9db9346f6fe75b0054af4cd1 in / 
# Tue, 29 Mar 2022 00:23:00 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 06:33:42 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 30 Mar 2022 06:35:18 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 30 Mar 2022 06:36:24 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7db831386ce67ac1cf2b4f1513fe3746c9ea2b8d4c82efca75be638eaf533614`  
		Last Modified: Tue, 29 Mar 2022 00:34:41 GMT  
		Size: 30.6 MB (30560163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5beee7bbe2070c64db910f012c8de134f5d7e04cce73425b9b3252cfdac7dabf`  
		Last Modified: Wed, 30 Mar 2022 06:53:43 GMT  
		Size: 2.9 MB (2892707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cecf8b2b1c2486a60cd71f13b29a003199e7acfb8e65eb35a7103d2be2c21424`  
		Last Modified: Wed, 30 Mar 2022 06:53:48 GMT  
		Size: 26.9 MB (26917725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.10.0`

```console
$ docker pull mono@sha256:2c1cdfc346d2b4708c4985a17fffc9f2a5bd2701402c3fa85c60b1cee6052f53
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
$ docker pull mono@sha256:7d05fdb89242ddd492352dd07e116e4265a0bc74887cdbec241e678bda999e8d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.0 MB (225016606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd568696105f84add5464497cd947fbc9578d6d45bdc8d6581a6cd3b8ab308ef`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:38 GMT
ADD file:59187422476c57db46e60f894a4cfd0f243e80230ef9ea75b2d8dd4925d59df3 in / 
# Tue, 29 Mar 2022 00:22:38 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 22:51:04 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 29 Mar 2022 22:51:12 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 29 Mar 2022 22:51:39 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 29 Mar 2022 23:01:35 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:f003217c5aaebdfee0b9a448fbabd995e5f0159f5b231460c0ecc21baf171953`  
		Last Modified: Tue, 29 Mar 2022 00:28:02 GMT  
		Size: 27.2 MB (27151970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ae9dab17d49756cbd842116bb4c8ecb5a2d64d39c08d729451e14400a8b433f`  
		Last Modified: Tue, 29 Mar 2022 23:02:31 GMT  
		Size: 2.8 MB (2777394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a496246b00b4b65da977fb279486fb8752dd631c5119990bb08a199626d0ee3`  
		Last Modified: Tue, 29 Mar 2022 23:02:41 GMT  
		Size: 64.8 MB (64778479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ac0981c4bbcf3da52e65fa962a538ab5a5aa9e4aebf9ebcdb25780723272e10`  
		Last Modified: Tue, 29 Mar 2022 23:03:49 GMT  
		Size: 130.3 MB (130308763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0` - linux; arm variant v5

```console
$ docker pull mono@sha256:c258968ed62efa47680adb7fc1435612b46ad3b48d63ed93093f319cdab04935
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.9 MB (180855371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7caefcc734f172d8b5b345e474f7e7e113a9b40e6e7eb92cadbb0c680abc6c8f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:51:36 GMT
ADD file:7ac5498e2c44686d7eb272ef7645a0a64486cf942610f6754aa4a932f5b1a4be in / 
# Tue, 29 Mar 2022 00:51:37 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 08:51:50 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 29 Mar 2022 08:52:17 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 29 Mar 2022 08:53:05 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 29 Mar 2022 09:00:04 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:8f10b1b67f0119a2dd5f838a3e98ab2c412e4b51fb1e4841e2b79fd4cae86105`  
		Last Modified: Tue, 29 Mar 2022 01:06:51 GMT  
		Size: 24.9 MB (24887495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a48926cfb9ba33532fb4a1f42ce2a984010491b46d8002b4db306c821d4e10f4`  
		Last Modified: Tue, 29 Mar 2022 09:02:13 GMT  
		Size: 2.5 MB (2467645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f429b0f7cd5e4638b807cc3bab5e07aaddbf1b55eb066703c660685b59adfe2c`  
		Last Modified: Tue, 29 Mar 2022 09:02:29 GMT  
		Size: 24.5 MB (24521524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8edee1c13cf6286aa56485e7352b2a7fe83505c4807123216a51538d9382f3bb`  
		Last Modified: Tue, 29 Mar 2022 09:06:16 GMT  
		Size: 129.0 MB (128978707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0` - linux; arm variant v7

```console
$ docker pull mono@sha256:96c725241edcf4d0f1e81cd0bd8d986a517516b802d3f2e1b8b93f07dc85a545
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.8 MB (176764272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70f601485ff40d1369d729a725cae9ef7a65addf94e8d47aedd20e919380aebf`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 02:19:40 GMT
ADD file:8d54e000817531229c35a32eee074105c7b4d3c08b7ca56b1abdd80571687f28 in / 
# Tue, 29 Mar 2022 02:19:41 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 21:57:19 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 30 Mar 2022 21:57:44 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 30 Mar 2022 21:58:27 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 30 Mar 2022 22:04:35 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:d4bf0b27c669e589de33695047d638174fc2ca819a4366d5f80d1ad6b01c0c0e`  
		Last Modified: Tue, 29 Mar 2022 02:35:26 GMT  
		Size: 22.8 MB (22753045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56011a574ad043bc367af54ab51081b83c20f4fe32556bd822cbcf01be0df28f`  
		Last Modified: Wed, 30 Mar 2022 22:06:42 GMT  
		Size: 2.4 MB (2366866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0562aaca95b07d80f29aaea2ea5f8560179271cd296e0e14f9118c113b715d1`  
		Last Modified: Wed, 30 Mar 2022 22:06:58 GMT  
		Size: 23.8 MB (23814839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4069a4b0106e127b7d470d7d0d21eeac4b14eab70c362cf2cd382ea10cf32ab`  
		Last Modified: Wed, 30 Mar 2022 22:10:46 GMT  
		Size: 127.8 MB (127829522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:db4ccba0ea3a15d03bce129dc7b8f8c1d17eb414d22d0ce50f04c91aa9dc8e6b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.4 MB (203357942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:542f1d2be1793e91d33d40c760fdeff6d2626a9c03e0bb060de4fc1929460c11`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Apr 2022 04:29:36 GMT
ADD file:5de4397c1295f7249c93907be599d96efbd9cd25909340d245ec8d1c9770f444 in / 
# Wed, 20 Apr 2022 04:29:37 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 09:34:48 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 20 Apr 2022 09:34:57 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 20 Apr 2022 09:35:12 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 20 Apr 2022 09:37:30 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:6c3e5b218d6477ff77053280968d5bdeaa5dcf16a803e917d98dd0ea8b93ac82`  
		Last Modified: Wed, 20 Apr 2022 04:36:38 GMT  
		Size: 25.9 MB (25908349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df56c08b5590c539b81f96718f5057b07ceaaf7017a28704b0f095af7166af2f`  
		Last Modified: Wed, 20 Apr 2022 09:38:39 GMT  
		Size: 2.6 MB (2641023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a34f53b7c9a1d5af7034cdc60069b6b9c3b2099c676574b0de7e22085ba360dc`  
		Last Modified: Wed, 20 Apr 2022 09:38:44 GMT  
		Size: 29.4 MB (29361704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a3f7de6536f999251c110135ca6a52d08565af7071c6fe5eea96fbd6578aa58`  
		Last Modified: Wed, 20 Apr 2022 09:40:03 GMT  
		Size: 145.4 MB (145446866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0` - linux; 386

```console
$ docker pull mono@sha256:3e640bbe614e2c612a0234a760239253353017f54ea632d8e70ca5007fc1129d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.6 MB (230599389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38c8b38fb0ee5f997e90812c188e9956c7ea18acf1131589a9e1d93bc640c80a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Apr 2022 07:38:03 GMT
ADD file:602a25173054242f635a5a299845b7f1b56864ac5d3b8af1ae29dec3a9da119f in / 
# Wed, 20 Apr 2022 07:38:04 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 12:49:46 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 20 Apr 2022 12:49:55 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 20 Apr 2022 12:50:19 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 20 Apr 2022 12:52:21 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a13b13d818745c4d2234aab71df26e4a01bfe59f396ab62f20d156b94803650c`  
		Last Modified: Wed, 20 Apr 2022 07:45:46 GMT  
		Size: 27.8 MB (27799825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc19bd2071107b873877fbe3bf3e623d524ecd131b76d25f818ed40f8888a5ae`  
		Last Modified: Wed, 20 Apr 2022 12:53:33 GMT  
		Size: 2.8 MB (2789172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c731ec96f4a6bd8004ee92ad713c93444a1f646c970369e7c6d60ed2ffcf37b`  
		Last Modified: Wed, 20 Apr 2022 12:53:47 GMT  
		Size: 68.6 MB (68594373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0af0ca9622588725474f2f5434ce305f02b1b9a597c878f49af99e99c444e22d`  
		Last Modified: Wed, 20 Apr 2022 12:55:04 GMT  
		Size: 131.4 MB (131416019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0` - linux; ppc64le

```console
$ docker pull mono@sha256:ccbe3a2584d91b1ca5c73d0bbd0dd764fb51f342832b8a644ab523169d6f071f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.4 MB (192388947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaf8e4db6dcac0e22d89a234e7bdb9d9fa90a402a650c944f4ca1d61c758dc18`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:59 GMT
ADD file:7271d778d432a07f57fedf8d50d83699ef545acc9db9346f6fe75b0054af4cd1 in / 
# Tue, 29 Mar 2022 00:23:00 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 06:33:42 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 30 Mar 2022 06:35:18 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 30 Mar 2022 06:36:24 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 30 Mar 2022 06:52:21 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7db831386ce67ac1cf2b4f1513fe3746c9ea2b8d4c82efca75be638eaf533614`  
		Last Modified: Tue, 29 Mar 2022 00:34:41 GMT  
		Size: 30.6 MB (30560163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5beee7bbe2070c64db910f012c8de134f5d7e04cce73425b9b3252cfdac7dabf`  
		Last Modified: Wed, 30 Mar 2022 06:53:43 GMT  
		Size: 2.9 MB (2892707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cecf8b2b1c2486a60cd71f13b29a003199e7acfb8e65eb35a7103d2be2c21424`  
		Last Modified: Wed, 30 Mar 2022 06:53:48 GMT  
		Size: 26.9 MB (26917725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cc6f7f81b1a255a5706b8520a6843611040386aedd1032c8ae7325fb6e5b8bd`  
		Last Modified: Wed, 30 Mar 2022 06:55:16 GMT  
		Size: 132.0 MB (132018352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.10.0-slim`

```console
$ docker pull mono@sha256:41df20dd54c69b2ef78feba5472d309ebdd8ae0763ec4a5d087e6080c9f23932
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
$ docker pull mono@sha256:2434c8862d32d50b83dd36a485d026303c92cae34ef6ff56186d003f637ff8c8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.7 MB (94707843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f7a8dd762bb2153e2729296500f08d54e3a73061201f49d96977f8572d33531`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:38 GMT
ADD file:59187422476c57db46e60f894a4cfd0f243e80230ef9ea75b2d8dd4925d59df3 in / 
# Tue, 29 Mar 2022 00:22:38 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 22:51:04 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 29 Mar 2022 22:51:12 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 29 Mar 2022 22:51:39 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:f003217c5aaebdfee0b9a448fbabd995e5f0159f5b231460c0ecc21baf171953`  
		Last Modified: Tue, 29 Mar 2022 00:28:02 GMT  
		Size: 27.2 MB (27151970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ae9dab17d49756cbd842116bb4c8ecb5a2d64d39c08d729451e14400a8b433f`  
		Last Modified: Tue, 29 Mar 2022 23:02:31 GMT  
		Size: 2.8 MB (2777394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a496246b00b4b65da977fb279486fb8752dd631c5119990bb08a199626d0ee3`  
		Last Modified: Tue, 29 Mar 2022 23:02:41 GMT  
		Size: 64.8 MB (64778479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:cf2c912a55906fd6a4e96d2ca6c0adc9b64765ec9feb9c2b3763aaea11e645ce
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.9 MB (51876664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a031511624fa3c816d95f06c0692434ee36e2a5d28235d0c83863ebe44463281`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:51:36 GMT
ADD file:7ac5498e2c44686d7eb272ef7645a0a64486cf942610f6754aa4a932f5b1a4be in / 
# Tue, 29 Mar 2022 00:51:37 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 08:51:50 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 29 Mar 2022 08:52:17 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 29 Mar 2022 08:53:05 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:8f10b1b67f0119a2dd5f838a3e98ab2c412e4b51fb1e4841e2b79fd4cae86105`  
		Last Modified: Tue, 29 Mar 2022 01:06:51 GMT  
		Size: 24.9 MB (24887495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a48926cfb9ba33532fb4a1f42ce2a984010491b46d8002b4db306c821d4e10f4`  
		Last Modified: Tue, 29 Mar 2022 09:02:13 GMT  
		Size: 2.5 MB (2467645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f429b0f7cd5e4638b807cc3bab5e07aaddbf1b55eb066703c660685b59adfe2c`  
		Last Modified: Tue, 29 Mar 2022 09:02:29 GMT  
		Size: 24.5 MB (24521524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:1b48beb386f0dee7a252b4f4a39555729e170af382d2ca70a386cbc849fed677
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48934750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f29fa6f525c588db746b1f3a3eed667e5aef45aae3eb6db3953ba52d6ff6d45`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 02:19:40 GMT
ADD file:8d54e000817531229c35a32eee074105c7b4d3c08b7ca56b1abdd80571687f28 in / 
# Tue, 29 Mar 2022 02:19:41 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 21:57:19 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 30 Mar 2022 21:57:44 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 30 Mar 2022 21:58:27 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:d4bf0b27c669e589de33695047d638174fc2ca819a4366d5f80d1ad6b01c0c0e`  
		Last Modified: Tue, 29 Mar 2022 02:35:26 GMT  
		Size: 22.8 MB (22753045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56011a574ad043bc367af54ab51081b83c20f4fe32556bd822cbcf01be0df28f`  
		Last Modified: Wed, 30 Mar 2022 22:06:42 GMT  
		Size: 2.4 MB (2366866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0562aaca95b07d80f29aaea2ea5f8560179271cd296e0e14f9118c113b715d1`  
		Last Modified: Wed, 30 Mar 2022 22:06:58 GMT  
		Size: 23.8 MB (23814839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:fd0ffe089ab133d58978ea5e51d43135e9a8c87b86be3997fd1e5b0d581cc2ee
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.9 MB (57911076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:147cc7fd6295707399eab462793e12cbddb6d439837b2897b3c69b2125dbc6e2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Apr 2022 04:29:36 GMT
ADD file:5de4397c1295f7249c93907be599d96efbd9cd25909340d245ec8d1c9770f444 in / 
# Wed, 20 Apr 2022 04:29:37 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 09:34:48 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 20 Apr 2022 09:34:57 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 20 Apr 2022 09:35:12 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:6c3e5b218d6477ff77053280968d5bdeaa5dcf16a803e917d98dd0ea8b93ac82`  
		Last Modified: Wed, 20 Apr 2022 04:36:38 GMT  
		Size: 25.9 MB (25908349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df56c08b5590c539b81f96718f5057b07ceaaf7017a28704b0f095af7166af2f`  
		Last Modified: Wed, 20 Apr 2022 09:38:39 GMT  
		Size: 2.6 MB (2641023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a34f53b7c9a1d5af7034cdc60069b6b9c3b2099c676574b0de7e22085ba360dc`  
		Last Modified: Wed, 20 Apr 2022 09:38:44 GMT  
		Size: 29.4 MB (29361704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0-slim` - linux; 386

```console
$ docker pull mono@sha256:8a2f06c25415df8cc6ae7315e81ca06a9ff079a357c05caf0d1b57045ad265fa
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.2 MB (99183370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a4588d79da86f7cab111b6c2fc82a13c1680b1134d953242a251f3c0da28b4a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Apr 2022 07:38:03 GMT
ADD file:602a25173054242f635a5a299845b7f1b56864ac5d3b8af1ae29dec3a9da119f in / 
# Wed, 20 Apr 2022 07:38:04 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 12:49:46 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 20 Apr 2022 12:49:55 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 20 Apr 2022 12:50:19 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a13b13d818745c4d2234aab71df26e4a01bfe59f396ab62f20d156b94803650c`  
		Last Modified: Wed, 20 Apr 2022 07:45:46 GMT  
		Size: 27.8 MB (27799825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc19bd2071107b873877fbe3bf3e623d524ecd131b76d25f818ed40f8888a5ae`  
		Last Modified: Wed, 20 Apr 2022 12:53:33 GMT  
		Size: 2.8 MB (2789172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c731ec96f4a6bd8004ee92ad713c93444a1f646c970369e7c6d60ed2ffcf37b`  
		Last Modified: Wed, 20 Apr 2022 12:53:47 GMT  
		Size: 68.6 MB (68594373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:949677eaaf0421b89ed25dc185f9ca51c2b21b0aaff569226a3f3a9a49cf0649
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.4 MB (60370595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a37887fb66d953ed3542898f048cd47ccbde3d6b9532aefb36b9877cdb8bff93`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:59 GMT
ADD file:7271d778d432a07f57fedf8d50d83699ef545acc9db9346f6fe75b0054af4cd1 in / 
# Tue, 29 Mar 2022 00:23:00 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 06:33:42 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 30 Mar 2022 06:35:18 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 30 Mar 2022 06:36:24 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7db831386ce67ac1cf2b4f1513fe3746c9ea2b8d4c82efca75be638eaf533614`  
		Last Modified: Tue, 29 Mar 2022 00:34:41 GMT  
		Size: 30.6 MB (30560163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5beee7bbe2070c64db910f012c8de134f5d7e04cce73425b9b3252cfdac7dabf`  
		Last Modified: Wed, 30 Mar 2022 06:53:43 GMT  
		Size: 2.9 MB (2892707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cecf8b2b1c2486a60cd71f13b29a003199e7acfb8e65eb35a7103d2be2c21424`  
		Last Modified: Wed, 30 Mar 2022 06:53:48 GMT  
		Size: 26.9 MB (26917725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.10.0.104`

```console
$ docker pull mono@sha256:2c1cdfc346d2b4708c4985a17fffc9f2a5bd2701402c3fa85c60b1cee6052f53
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
$ docker pull mono@sha256:7d05fdb89242ddd492352dd07e116e4265a0bc74887cdbec241e678bda999e8d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.0 MB (225016606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd568696105f84add5464497cd947fbc9578d6d45bdc8d6581a6cd3b8ab308ef`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:38 GMT
ADD file:59187422476c57db46e60f894a4cfd0f243e80230ef9ea75b2d8dd4925d59df3 in / 
# Tue, 29 Mar 2022 00:22:38 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 22:51:04 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 29 Mar 2022 22:51:12 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 29 Mar 2022 22:51:39 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 29 Mar 2022 23:01:35 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:f003217c5aaebdfee0b9a448fbabd995e5f0159f5b231460c0ecc21baf171953`  
		Last Modified: Tue, 29 Mar 2022 00:28:02 GMT  
		Size: 27.2 MB (27151970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ae9dab17d49756cbd842116bb4c8ecb5a2d64d39c08d729451e14400a8b433f`  
		Last Modified: Tue, 29 Mar 2022 23:02:31 GMT  
		Size: 2.8 MB (2777394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a496246b00b4b65da977fb279486fb8752dd631c5119990bb08a199626d0ee3`  
		Last Modified: Tue, 29 Mar 2022 23:02:41 GMT  
		Size: 64.8 MB (64778479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ac0981c4bbcf3da52e65fa962a538ab5a5aa9e4aebf9ebcdb25780723272e10`  
		Last Modified: Tue, 29 Mar 2022 23:03:49 GMT  
		Size: 130.3 MB (130308763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0.104` - linux; arm variant v5

```console
$ docker pull mono@sha256:c258968ed62efa47680adb7fc1435612b46ad3b48d63ed93093f319cdab04935
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.9 MB (180855371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7caefcc734f172d8b5b345e474f7e7e113a9b40e6e7eb92cadbb0c680abc6c8f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:51:36 GMT
ADD file:7ac5498e2c44686d7eb272ef7645a0a64486cf942610f6754aa4a932f5b1a4be in / 
# Tue, 29 Mar 2022 00:51:37 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 08:51:50 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 29 Mar 2022 08:52:17 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 29 Mar 2022 08:53:05 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 29 Mar 2022 09:00:04 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:8f10b1b67f0119a2dd5f838a3e98ab2c412e4b51fb1e4841e2b79fd4cae86105`  
		Last Modified: Tue, 29 Mar 2022 01:06:51 GMT  
		Size: 24.9 MB (24887495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a48926cfb9ba33532fb4a1f42ce2a984010491b46d8002b4db306c821d4e10f4`  
		Last Modified: Tue, 29 Mar 2022 09:02:13 GMT  
		Size: 2.5 MB (2467645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f429b0f7cd5e4638b807cc3bab5e07aaddbf1b55eb066703c660685b59adfe2c`  
		Last Modified: Tue, 29 Mar 2022 09:02:29 GMT  
		Size: 24.5 MB (24521524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8edee1c13cf6286aa56485e7352b2a7fe83505c4807123216a51538d9382f3bb`  
		Last Modified: Tue, 29 Mar 2022 09:06:16 GMT  
		Size: 129.0 MB (128978707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0.104` - linux; arm variant v7

```console
$ docker pull mono@sha256:96c725241edcf4d0f1e81cd0bd8d986a517516b802d3f2e1b8b93f07dc85a545
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.8 MB (176764272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70f601485ff40d1369d729a725cae9ef7a65addf94e8d47aedd20e919380aebf`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 02:19:40 GMT
ADD file:8d54e000817531229c35a32eee074105c7b4d3c08b7ca56b1abdd80571687f28 in / 
# Tue, 29 Mar 2022 02:19:41 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 21:57:19 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 30 Mar 2022 21:57:44 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 30 Mar 2022 21:58:27 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 30 Mar 2022 22:04:35 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:d4bf0b27c669e589de33695047d638174fc2ca819a4366d5f80d1ad6b01c0c0e`  
		Last Modified: Tue, 29 Mar 2022 02:35:26 GMT  
		Size: 22.8 MB (22753045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56011a574ad043bc367af54ab51081b83c20f4fe32556bd822cbcf01be0df28f`  
		Last Modified: Wed, 30 Mar 2022 22:06:42 GMT  
		Size: 2.4 MB (2366866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0562aaca95b07d80f29aaea2ea5f8560179271cd296e0e14f9118c113b715d1`  
		Last Modified: Wed, 30 Mar 2022 22:06:58 GMT  
		Size: 23.8 MB (23814839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4069a4b0106e127b7d470d7d0d21eeac4b14eab70c362cf2cd382ea10cf32ab`  
		Last Modified: Wed, 30 Mar 2022 22:10:46 GMT  
		Size: 127.8 MB (127829522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0.104` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:db4ccba0ea3a15d03bce129dc7b8f8c1d17eb414d22d0ce50f04c91aa9dc8e6b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.4 MB (203357942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:542f1d2be1793e91d33d40c760fdeff6d2626a9c03e0bb060de4fc1929460c11`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Apr 2022 04:29:36 GMT
ADD file:5de4397c1295f7249c93907be599d96efbd9cd25909340d245ec8d1c9770f444 in / 
# Wed, 20 Apr 2022 04:29:37 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 09:34:48 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 20 Apr 2022 09:34:57 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 20 Apr 2022 09:35:12 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 20 Apr 2022 09:37:30 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:6c3e5b218d6477ff77053280968d5bdeaa5dcf16a803e917d98dd0ea8b93ac82`  
		Last Modified: Wed, 20 Apr 2022 04:36:38 GMT  
		Size: 25.9 MB (25908349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df56c08b5590c539b81f96718f5057b07ceaaf7017a28704b0f095af7166af2f`  
		Last Modified: Wed, 20 Apr 2022 09:38:39 GMT  
		Size: 2.6 MB (2641023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a34f53b7c9a1d5af7034cdc60069b6b9c3b2099c676574b0de7e22085ba360dc`  
		Last Modified: Wed, 20 Apr 2022 09:38:44 GMT  
		Size: 29.4 MB (29361704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a3f7de6536f999251c110135ca6a52d08565af7071c6fe5eea96fbd6578aa58`  
		Last Modified: Wed, 20 Apr 2022 09:40:03 GMT  
		Size: 145.4 MB (145446866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0.104` - linux; 386

```console
$ docker pull mono@sha256:3e640bbe614e2c612a0234a760239253353017f54ea632d8e70ca5007fc1129d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.6 MB (230599389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38c8b38fb0ee5f997e90812c188e9956c7ea18acf1131589a9e1d93bc640c80a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Apr 2022 07:38:03 GMT
ADD file:602a25173054242f635a5a299845b7f1b56864ac5d3b8af1ae29dec3a9da119f in / 
# Wed, 20 Apr 2022 07:38:04 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 12:49:46 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 20 Apr 2022 12:49:55 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 20 Apr 2022 12:50:19 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 20 Apr 2022 12:52:21 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a13b13d818745c4d2234aab71df26e4a01bfe59f396ab62f20d156b94803650c`  
		Last Modified: Wed, 20 Apr 2022 07:45:46 GMT  
		Size: 27.8 MB (27799825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc19bd2071107b873877fbe3bf3e623d524ecd131b76d25f818ed40f8888a5ae`  
		Last Modified: Wed, 20 Apr 2022 12:53:33 GMT  
		Size: 2.8 MB (2789172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c731ec96f4a6bd8004ee92ad713c93444a1f646c970369e7c6d60ed2ffcf37b`  
		Last Modified: Wed, 20 Apr 2022 12:53:47 GMT  
		Size: 68.6 MB (68594373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0af0ca9622588725474f2f5434ce305f02b1b9a597c878f49af99e99c444e22d`  
		Last Modified: Wed, 20 Apr 2022 12:55:04 GMT  
		Size: 131.4 MB (131416019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0.104` - linux; ppc64le

```console
$ docker pull mono@sha256:ccbe3a2584d91b1ca5c73d0bbd0dd764fb51f342832b8a644ab523169d6f071f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.4 MB (192388947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaf8e4db6dcac0e22d89a234e7bdb9d9fa90a402a650c944f4ca1d61c758dc18`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:59 GMT
ADD file:7271d778d432a07f57fedf8d50d83699ef545acc9db9346f6fe75b0054af4cd1 in / 
# Tue, 29 Mar 2022 00:23:00 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 06:33:42 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 30 Mar 2022 06:35:18 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 30 Mar 2022 06:36:24 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 30 Mar 2022 06:52:21 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7db831386ce67ac1cf2b4f1513fe3746c9ea2b8d4c82efca75be638eaf533614`  
		Last Modified: Tue, 29 Mar 2022 00:34:41 GMT  
		Size: 30.6 MB (30560163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5beee7bbe2070c64db910f012c8de134f5d7e04cce73425b9b3252cfdac7dabf`  
		Last Modified: Wed, 30 Mar 2022 06:53:43 GMT  
		Size: 2.9 MB (2892707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cecf8b2b1c2486a60cd71f13b29a003199e7acfb8e65eb35a7103d2be2c21424`  
		Last Modified: Wed, 30 Mar 2022 06:53:48 GMT  
		Size: 26.9 MB (26917725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cc6f7f81b1a255a5706b8520a6843611040386aedd1032c8ae7325fb6e5b8bd`  
		Last Modified: Wed, 30 Mar 2022 06:55:16 GMT  
		Size: 132.0 MB (132018352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.10.0.104-slim`

```console
$ docker pull mono@sha256:41df20dd54c69b2ef78feba5472d309ebdd8ae0763ec4a5d087e6080c9f23932
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
$ docker pull mono@sha256:2434c8862d32d50b83dd36a485d026303c92cae34ef6ff56186d003f637ff8c8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.7 MB (94707843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f7a8dd762bb2153e2729296500f08d54e3a73061201f49d96977f8572d33531`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:38 GMT
ADD file:59187422476c57db46e60f894a4cfd0f243e80230ef9ea75b2d8dd4925d59df3 in / 
# Tue, 29 Mar 2022 00:22:38 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 22:51:04 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 29 Mar 2022 22:51:12 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 29 Mar 2022 22:51:39 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:f003217c5aaebdfee0b9a448fbabd995e5f0159f5b231460c0ecc21baf171953`  
		Last Modified: Tue, 29 Mar 2022 00:28:02 GMT  
		Size: 27.2 MB (27151970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ae9dab17d49756cbd842116bb4c8ecb5a2d64d39c08d729451e14400a8b433f`  
		Last Modified: Tue, 29 Mar 2022 23:02:31 GMT  
		Size: 2.8 MB (2777394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a496246b00b4b65da977fb279486fb8752dd631c5119990bb08a199626d0ee3`  
		Last Modified: Tue, 29 Mar 2022 23:02:41 GMT  
		Size: 64.8 MB (64778479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0.104-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:cf2c912a55906fd6a4e96d2ca6c0adc9b64765ec9feb9c2b3763aaea11e645ce
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.9 MB (51876664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a031511624fa3c816d95f06c0692434ee36e2a5d28235d0c83863ebe44463281`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:51:36 GMT
ADD file:7ac5498e2c44686d7eb272ef7645a0a64486cf942610f6754aa4a932f5b1a4be in / 
# Tue, 29 Mar 2022 00:51:37 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 08:51:50 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 29 Mar 2022 08:52:17 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 29 Mar 2022 08:53:05 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:8f10b1b67f0119a2dd5f838a3e98ab2c412e4b51fb1e4841e2b79fd4cae86105`  
		Last Modified: Tue, 29 Mar 2022 01:06:51 GMT  
		Size: 24.9 MB (24887495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a48926cfb9ba33532fb4a1f42ce2a984010491b46d8002b4db306c821d4e10f4`  
		Last Modified: Tue, 29 Mar 2022 09:02:13 GMT  
		Size: 2.5 MB (2467645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f429b0f7cd5e4638b807cc3bab5e07aaddbf1b55eb066703c660685b59adfe2c`  
		Last Modified: Tue, 29 Mar 2022 09:02:29 GMT  
		Size: 24.5 MB (24521524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0.104-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:1b48beb386f0dee7a252b4f4a39555729e170af382d2ca70a386cbc849fed677
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48934750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f29fa6f525c588db746b1f3a3eed667e5aef45aae3eb6db3953ba52d6ff6d45`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 02:19:40 GMT
ADD file:8d54e000817531229c35a32eee074105c7b4d3c08b7ca56b1abdd80571687f28 in / 
# Tue, 29 Mar 2022 02:19:41 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 21:57:19 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 30 Mar 2022 21:57:44 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 30 Mar 2022 21:58:27 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:d4bf0b27c669e589de33695047d638174fc2ca819a4366d5f80d1ad6b01c0c0e`  
		Last Modified: Tue, 29 Mar 2022 02:35:26 GMT  
		Size: 22.8 MB (22753045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56011a574ad043bc367af54ab51081b83c20f4fe32556bd822cbcf01be0df28f`  
		Last Modified: Wed, 30 Mar 2022 22:06:42 GMT  
		Size: 2.4 MB (2366866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0562aaca95b07d80f29aaea2ea5f8560179271cd296e0e14f9118c113b715d1`  
		Last Modified: Wed, 30 Mar 2022 22:06:58 GMT  
		Size: 23.8 MB (23814839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0.104-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:fd0ffe089ab133d58978ea5e51d43135e9a8c87b86be3997fd1e5b0d581cc2ee
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.9 MB (57911076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:147cc7fd6295707399eab462793e12cbddb6d439837b2897b3c69b2125dbc6e2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Apr 2022 04:29:36 GMT
ADD file:5de4397c1295f7249c93907be599d96efbd9cd25909340d245ec8d1c9770f444 in / 
# Wed, 20 Apr 2022 04:29:37 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 09:34:48 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 20 Apr 2022 09:34:57 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 20 Apr 2022 09:35:12 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:6c3e5b218d6477ff77053280968d5bdeaa5dcf16a803e917d98dd0ea8b93ac82`  
		Last Modified: Wed, 20 Apr 2022 04:36:38 GMT  
		Size: 25.9 MB (25908349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df56c08b5590c539b81f96718f5057b07ceaaf7017a28704b0f095af7166af2f`  
		Last Modified: Wed, 20 Apr 2022 09:38:39 GMT  
		Size: 2.6 MB (2641023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a34f53b7c9a1d5af7034cdc60069b6b9c3b2099c676574b0de7e22085ba360dc`  
		Last Modified: Wed, 20 Apr 2022 09:38:44 GMT  
		Size: 29.4 MB (29361704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0.104-slim` - linux; 386

```console
$ docker pull mono@sha256:8a2f06c25415df8cc6ae7315e81ca06a9ff079a357c05caf0d1b57045ad265fa
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.2 MB (99183370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a4588d79da86f7cab111b6c2fc82a13c1680b1134d953242a251f3c0da28b4a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Apr 2022 07:38:03 GMT
ADD file:602a25173054242f635a5a299845b7f1b56864ac5d3b8af1ae29dec3a9da119f in / 
# Wed, 20 Apr 2022 07:38:04 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 12:49:46 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 20 Apr 2022 12:49:55 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 20 Apr 2022 12:50:19 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a13b13d818745c4d2234aab71df26e4a01bfe59f396ab62f20d156b94803650c`  
		Last Modified: Wed, 20 Apr 2022 07:45:46 GMT  
		Size: 27.8 MB (27799825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc19bd2071107b873877fbe3bf3e623d524ecd131b76d25f818ed40f8888a5ae`  
		Last Modified: Wed, 20 Apr 2022 12:53:33 GMT  
		Size: 2.8 MB (2789172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c731ec96f4a6bd8004ee92ad713c93444a1f646c970369e7c6d60ed2ffcf37b`  
		Last Modified: Wed, 20 Apr 2022 12:53:47 GMT  
		Size: 68.6 MB (68594373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0.104-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:949677eaaf0421b89ed25dc185f9ca51c2b21b0aaff569226a3f3a9a49cf0649
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.4 MB (60370595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a37887fb66d953ed3542898f048cd47ccbde3d6b9532aefb36b9877cdb8bff93`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:59 GMT
ADD file:7271d778d432a07f57fedf8d50d83699ef545acc9db9346f6fe75b0054af4cd1 in / 
# Tue, 29 Mar 2022 00:23:00 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 06:33:42 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 30 Mar 2022 06:35:18 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 30 Mar 2022 06:36:24 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7db831386ce67ac1cf2b4f1513fe3746c9ea2b8d4c82efca75be638eaf533614`  
		Last Modified: Tue, 29 Mar 2022 00:34:41 GMT  
		Size: 30.6 MB (30560163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5beee7bbe2070c64db910f012c8de134f5d7e04cce73425b9b3252cfdac7dabf`  
		Last Modified: Wed, 30 Mar 2022 06:53:43 GMT  
		Size: 2.9 MB (2892707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cecf8b2b1c2486a60cd71f13b29a003199e7acfb8e65eb35a7103d2be2c21424`  
		Last Modified: Wed, 30 Mar 2022 06:53:48 GMT  
		Size: 26.9 MB (26917725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.12`

```console
$ docker pull mono@sha256:288dce942fc8031ee29e492d5c8f6beec7d6a38df14ee0f8cf28070d4d555e44
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
$ docker pull mono@sha256:abcb22d3b82c95b20ff5c90f329cb759314b70e1781a67315b1ec2bb719e0cda
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.1 MB (236137951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a0982a1a3d0d9f836f390567b3d9452c91ca96d6b8b2e633edf0cf7994be535`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:38 GMT
ADD file:59187422476c57db46e60f894a4cfd0f243e80230ef9ea75b2d8dd4925d59df3 in / 
# Tue, 29 Mar 2022 00:22:38 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 22:50:30 GMT
ENV MONO_VERSION=6.12.0.122
# Tue, 29 Mar 2022 22:50:38 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 29 Mar 2022 22:51:01 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 29 Mar 2022 22:56:06 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:f003217c5aaebdfee0b9a448fbabd995e5f0159f5b231460c0ecc21baf171953`  
		Last Modified: Tue, 29 Mar 2022 00:28:02 GMT  
		Size: 27.2 MB (27151970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d839cde201cd1385a1c2c927214c614f1cd1bab02a62fd34b6df69e6f95daa7e`  
		Last Modified: Tue, 29 Mar 2022 23:02:05 GMT  
		Size: 2.8 MB (2777377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:158befabd0cf5fbeb7cb51a0cfc2f6c20399efe3be6abfd6d7dc8187d886b4a0`  
		Last Modified: Tue, 29 Mar 2022 23:02:14 GMT  
		Size: 64.8 MB (64760477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7f69220c106af4aa5ecc61935d51050e43fe6450996488e6c1d7fe5c5d7c2e1`  
		Last Modified: Tue, 29 Mar 2022 23:03:13 GMT  
		Size: 141.4 MB (141448127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12` - linux; arm variant v5

```console
$ docker pull mono@sha256:7f7e694bccdf74a53d7491c00db8088add1265f44830d8b0a365c7915304ef04
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.0 MB (191954448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71bb1b7df7ff58e8b649bb79421666f8422e0606d35629b29b8cf7c2b7ca4596`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:51:36 GMT
ADD file:7ac5498e2c44686d7eb272ef7645a0a64486cf942610f6754aa4a932f5b1a4be in / 
# Tue, 29 Mar 2022 00:51:37 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 08:50:15 GMT
ENV MONO_VERSION=6.12.0.122
# Tue, 29 Mar 2022 08:50:42 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 29 Mar 2022 08:51:31 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 29 Mar 2022 08:56:31 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:8f10b1b67f0119a2dd5f838a3e98ab2c412e4b51fb1e4841e2b79fd4cae86105`  
		Last Modified: Tue, 29 Mar 2022 01:06:51 GMT  
		Size: 24.9 MB (24887495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:103ccfc95d14718dd5bd47005c93225d5f82bdc075ccfc346e1b366afb616d57`  
		Last Modified: Tue, 29 Mar 2022 09:01:39 GMT  
		Size: 2.5 MB (2467692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13697b82f395905c310bf0030c74844e8f8fc5979a009c041a18de4488636164`  
		Last Modified: Tue, 29 Mar 2022 09:01:50 GMT  
		Size: 24.5 MB (24493260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90cc18056a6a14a94b009cdae75817ab5f9d1bea6b12aaf50cf5127985d9277f`  
		Last Modified: Tue, 29 Mar 2022 09:04:22 GMT  
		Size: 140.1 MB (140106001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12` - linux; arm variant v7

```console
$ docker pull mono@sha256:de55a06147b60da0b002c65b61e35e5bbcd09bb5d0a3c734b2004494af9e90b5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.9 MB (187869490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:068cd3b6737d2700c491cd15edf19aa585b83d26ea05ebaa0f5602558b0e57b7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 02:19:40 GMT
ADD file:8d54e000817531229c35a32eee074105c7b4d3c08b7ca56b1abdd80571687f28 in / 
# Tue, 29 Mar 2022 02:19:41 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 21:55:56 GMT
ENV MONO_VERSION=6.12.0.122
# Wed, 30 Mar 2022 21:56:22 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 30 Mar 2022 21:57:04 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 30 Mar 2022 22:01:31 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:d4bf0b27c669e589de33695047d638174fc2ca819a4366d5f80d1ad6b01c0c0e`  
		Last Modified: Tue, 29 Mar 2022 02:35:26 GMT  
		Size: 22.8 MB (22753045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:756cc431341070c1f6a772929e5d5daab96f2b040732e70d3cb93b3ce98d8542`  
		Last Modified: Wed, 30 Mar 2022 22:06:01 GMT  
		Size: 2.4 MB (2366920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:419ca67b5ee0885d9bcc46429070d185a04feb680b643fc29ceda334987a6a6f`  
		Last Modified: Wed, 30 Mar 2022 22:06:18 GMT  
		Size: 23.8 MB (23782719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:672029c9759800f327c1f06dc30ce05aac300a39d8f40f9c5d475f006a5486ba`  
		Last Modified: Wed, 30 Mar 2022 22:08:52 GMT  
		Size: 139.0 MB (138966806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:617fd6f5ff9238ff8782c0b154f5fbb1e51864ad1f009da0d0c5fcd54ff179c0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.5 MB (214465680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:721976153f55a700a3368032ce347eb3ae7b930fc6151b879332e0e99f1ca0cc`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Apr 2022 04:29:36 GMT
ADD file:5de4397c1295f7249c93907be599d96efbd9cd25909340d245ec8d1c9770f444 in / 
# Wed, 20 Apr 2022 04:29:37 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 09:34:15 GMT
ENV MONO_VERSION=6.12.0.122
# Wed, 20 Apr 2022 09:34:25 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 20 Apr 2022 09:34:40 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 20 Apr 2022 09:36:17 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:6c3e5b218d6477ff77053280968d5bdeaa5dcf16a803e917d98dd0ea8b93ac82`  
		Last Modified: Wed, 20 Apr 2022 04:36:38 GMT  
		Size: 25.9 MB (25908349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a5583d434a71d4775ae033dd3567325a5f5d01a34ff9f805631b17426570d60`  
		Last Modified: Wed, 20 Apr 2022 09:38:16 GMT  
		Size: 2.6 MB (2641065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1df7a4f3775402176b947b2ffb1f930879581b64904846f29bd8e5aa4000e4d`  
		Last Modified: Wed, 20 Apr 2022 09:38:20 GMT  
		Size: 29.3 MB (29318359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7f80c1eac9d435a1e808ae3c8eaf8a76d9e653e54edc1090cf4c2fc47f29f6e`  
		Last Modified: Wed, 20 Apr 2022 09:39:21 GMT  
		Size: 156.6 MB (156597907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12` - linux; 386

```console
$ docker pull mono@sha256:ef781f5c402c37c294ccf7397654b6a780c16c68ab05b1ee598260446e0049b0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.7 MB (241696337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faa267e26ab7e853336277f2575154ad396b6536c3cd9e8ba22824250ccc6fbd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Apr 2022 07:38:03 GMT
ADD file:602a25173054242f635a5a299845b7f1b56864ac5d3b8af1ae29dec3a9da119f in / 
# Wed, 20 Apr 2022 07:38:04 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 12:49:08 GMT
ENV MONO_VERSION=6.12.0.122
# Wed, 20 Apr 2022 12:49:17 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 20 Apr 2022 12:49:40 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 20 Apr 2022 12:51:19 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a13b13d818745c4d2234aab71df26e4a01bfe59f396ab62f20d156b94803650c`  
		Last Modified: Wed, 20 Apr 2022 07:45:46 GMT  
		Size: 27.8 MB (27799825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc07624832ff4b064bd2b3797a6774618e27f4c3a1e24419874628eeb613e7ba`  
		Last Modified: Wed, 20 Apr 2022 12:53:02 GMT  
		Size: 2.8 MB (2789161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d6af1a94baa95c219eaba2db2fb27e299572ac8d2859e1399838abdccae784c`  
		Last Modified: Wed, 20 Apr 2022 12:53:11 GMT  
		Size: 68.6 MB (68568946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cec0646bfa3d97be6f7515ad03d0cbb859adebe6cf3785cf1d36d06c8aa3f224`  
		Last Modified: Wed, 20 Apr 2022 12:54:22 GMT  
		Size: 142.5 MB (142538405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12` - linux; ppc64le

```console
$ docker pull mono@sha256:d8969fd75bcf7f2415543c536c50458a18d28e8cdab323db80eb053827d08c60
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.6 MB (203608008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:226cb9d82e8bfc2114d8f6e225a71870230cc71a214527422e1a68b2185008bc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:59 GMT
ADD file:7271d778d432a07f57fedf8d50d83699ef545acc9db9346f6fe75b0054af4cd1 in / 
# Tue, 29 Mar 2022 00:23:00 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 06:30:50 GMT
ENV MONO_VERSION=6.12.0.122
# Wed, 30 Mar 2022 06:32:19 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 30 Mar 2022 06:33:27 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 30 Mar 2022 06:43:44 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7db831386ce67ac1cf2b4f1513fe3746c9ea2b8d4c82efca75be638eaf533614`  
		Last Modified: Tue, 29 Mar 2022 00:34:41 GMT  
		Size: 30.6 MB (30560163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55feab57ab15634326c723014da448815650e9737d6c5671ca5a4cd4503905cb`  
		Last Modified: Wed, 30 Mar 2022 06:53:14 GMT  
		Size: 2.9 MB (2892687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c00a3dcf742861f8ca53669004126ef6bead547f42b4f28c1d7ba21debbc8b5`  
		Last Modified: Wed, 30 Mar 2022 06:53:20 GMT  
		Size: 26.9 MB (26873425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af736d47f1875d0d79d7c43b3fce41fcb3f2129622c09182d7916c44b731e9b2`  
		Last Modified: Wed, 30 Mar 2022 06:54:30 GMT  
		Size: 143.3 MB (143281733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.12-slim`

```console
$ docker pull mono@sha256:bc7933bac89d6c7f5e9c656111b402a44420deb7a05c7adefcef682c114cc212
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
$ docker pull mono@sha256:87038a7da02d5efff3bfab1ec93dc3020d04cd3fad6bff479d3252cf3cb13695
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.7 MB (94689824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcc621103738e68eb59281907e2ec643435dbb8dd82d504d49655526191a0199`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:38 GMT
ADD file:59187422476c57db46e60f894a4cfd0f243e80230ef9ea75b2d8dd4925d59df3 in / 
# Tue, 29 Mar 2022 00:22:38 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 22:50:30 GMT
ENV MONO_VERSION=6.12.0.122
# Tue, 29 Mar 2022 22:50:38 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 29 Mar 2022 22:51:01 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:f003217c5aaebdfee0b9a448fbabd995e5f0159f5b231460c0ecc21baf171953`  
		Last Modified: Tue, 29 Mar 2022 00:28:02 GMT  
		Size: 27.2 MB (27151970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d839cde201cd1385a1c2c927214c614f1cd1bab02a62fd34b6df69e6f95daa7e`  
		Last Modified: Tue, 29 Mar 2022 23:02:05 GMT  
		Size: 2.8 MB (2777377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:158befabd0cf5fbeb7cb51a0cfc2f6c20399efe3be6abfd6d7dc8187d886b4a0`  
		Last Modified: Tue, 29 Mar 2022 23:02:14 GMT  
		Size: 64.8 MB (64760477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:2858e2824edbcaaefd73dd8b888c39d6c10cfd27bc7b2b1b420570403b00a924
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51848447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41535ed442f086e8d8103e40ebab589e248cc742505317bfb8c17b5746bc567f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:51:36 GMT
ADD file:7ac5498e2c44686d7eb272ef7645a0a64486cf942610f6754aa4a932f5b1a4be in / 
# Tue, 29 Mar 2022 00:51:37 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 08:50:15 GMT
ENV MONO_VERSION=6.12.0.122
# Tue, 29 Mar 2022 08:50:42 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 29 Mar 2022 08:51:31 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:8f10b1b67f0119a2dd5f838a3e98ab2c412e4b51fb1e4841e2b79fd4cae86105`  
		Last Modified: Tue, 29 Mar 2022 01:06:51 GMT  
		Size: 24.9 MB (24887495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:103ccfc95d14718dd5bd47005c93225d5f82bdc075ccfc346e1b366afb616d57`  
		Last Modified: Tue, 29 Mar 2022 09:01:39 GMT  
		Size: 2.5 MB (2467692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13697b82f395905c310bf0030c74844e8f8fc5979a009c041a18de4488636164`  
		Last Modified: Tue, 29 Mar 2022 09:01:50 GMT  
		Size: 24.5 MB (24493260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:c8f9bff7726932d61ceb479135172d8ad8d953634e902d99afa4b04b35c8979c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48902684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35df12dffc423503a586d8b0c8f4b5056157ba44d8baa9a3a8ebc94f4b728f4e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 02:19:40 GMT
ADD file:8d54e000817531229c35a32eee074105c7b4d3c08b7ca56b1abdd80571687f28 in / 
# Tue, 29 Mar 2022 02:19:41 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 21:55:56 GMT
ENV MONO_VERSION=6.12.0.122
# Wed, 30 Mar 2022 21:56:22 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 30 Mar 2022 21:57:04 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:d4bf0b27c669e589de33695047d638174fc2ca819a4366d5f80d1ad6b01c0c0e`  
		Last Modified: Tue, 29 Mar 2022 02:35:26 GMT  
		Size: 22.8 MB (22753045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:756cc431341070c1f6a772929e5d5daab96f2b040732e70d3cb93b3ce98d8542`  
		Last Modified: Wed, 30 Mar 2022 22:06:01 GMT  
		Size: 2.4 MB (2366920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:419ca67b5ee0885d9bcc46429070d185a04feb680b643fc29ceda334987a6a6f`  
		Last Modified: Wed, 30 Mar 2022 22:06:18 GMT  
		Size: 23.8 MB (23782719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:0f3837c80f89d4cc61d33d11680310dd7b9170aa4a20287829db1cf4ff83169c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.9 MB (57867773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a03207fd5f3c9c31e878dec4d955581897e75177774ac4915f726360915f8e8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Apr 2022 04:29:36 GMT
ADD file:5de4397c1295f7249c93907be599d96efbd9cd25909340d245ec8d1c9770f444 in / 
# Wed, 20 Apr 2022 04:29:37 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 09:34:15 GMT
ENV MONO_VERSION=6.12.0.122
# Wed, 20 Apr 2022 09:34:25 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 20 Apr 2022 09:34:40 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:6c3e5b218d6477ff77053280968d5bdeaa5dcf16a803e917d98dd0ea8b93ac82`  
		Last Modified: Wed, 20 Apr 2022 04:36:38 GMT  
		Size: 25.9 MB (25908349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a5583d434a71d4775ae033dd3567325a5f5d01a34ff9f805631b17426570d60`  
		Last Modified: Wed, 20 Apr 2022 09:38:16 GMT  
		Size: 2.6 MB (2641065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1df7a4f3775402176b947b2ffb1f930879581b64904846f29bd8e5aa4000e4d`  
		Last Modified: Wed, 20 Apr 2022 09:38:20 GMT  
		Size: 29.3 MB (29318359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12-slim` - linux; 386

```console
$ docker pull mono@sha256:a620c36d6b438c94797eaa6b17b2452369ac55ab8a59a1bcf8b4501df1eea0c5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.2 MB (99157932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95ff55aea4f3ffc1da74cea929a23a78ed6dc8901847098c5878018368c9da5d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Apr 2022 07:38:03 GMT
ADD file:602a25173054242f635a5a299845b7f1b56864ac5d3b8af1ae29dec3a9da119f in / 
# Wed, 20 Apr 2022 07:38:04 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 12:49:08 GMT
ENV MONO_VERSION=6.12.0.122
# Wed, 20 Apr 2022 12:49:17 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 20 Apr 2022 12:49:40 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a13b13d818745c4d2234aab71df26e4a01bfe59f396ab62f20d156b94803650c`  
		Last Modified: Wed, 20 Apr 2022 07:45:46 GMT  
		Size: 27.8 MB (27799825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc07624832ff4b064bd2b3797a6774618e27f4c3a1e24419874628eeb613e7ba`  
		Last Modified: Wed, 20 Apr 2022 12:53:02 GMT  
		Size: 2.8 MB (2789161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d6af1a94baa95c219eaba2db2fb27e299572ac8d2859e1399838abdccae784c`  
		Last Modified: Wed, 20 Apr 2022 12:53:11 GMT  
		Size: 68.6 MB (68568946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:9b3a0defce0a5c2ae9bfc6d34af244911ccd407e7973e0f3eedce5fe3670f57e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60326275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5184331441c848755861d28d51bfb13f10dc8e51ace7607db24b3326be9c1166`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:59 GMT
ADD file:7271d778d432a07f57fedf8d50d83699ef545acc9db9346f6fe75b0054af4cd1 in / 
# Tue, 29 Mar 2022 00:23:00 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 06:30:50 GMT
ENV MONO_VERSION=6.12.0.122
# Wed, 30 Mar 2022 06:32:19 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 30 Mar 2022 06:33:27 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7db831386ce67ac1cf2b4f1513fe3746c9ea2b8d4c82efca75be638eaf533614`  
		Last Modified: Tue, 29 Mar 2022 00:34:41 GMT  
		Size: 30.6 MB (30560163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55feab57ab15634326c723014da448815650e9737d6c5671ca5a4cd4503905cb`  
		Last Modified: Wed, 30 Mar 2022 06:53:14 GMT  
		Size: 2.9 MB (2892687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c00a3dcf742861f8ca53669004126ef6bead547f42b4f28c1d7ba21debbc8b5`  
		Last Modified: Wed, 30 Mar 2022 06:53:20 GMT  
		Size: 26.9 MB (26873425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.12.0`

```console
$ docker pull mono@sha256:288dce942fc8031ee29e492d5c8f6beec7d6a38df14ee0f8cf28070d4d555e44
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
$ docker pull mono@sha256:abcb22d3b82c95b20ff5c90f329cb759314b70e1781a67315b1ec2bb719e0cda
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.1 MB (236137951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a0982a1a3d0d9f836f390567b3d9452c91ca96d6b8b2e633edf0cf7994be535`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:38 GMT
ADD file:59187422476c57db46e60f894a4cfd0f243e80230ef9ea75b2d8dd4925d59df3 in / 
# Tue, 29 Mar 2022 00:22:38 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 22:50:30 GMT
ENV MONO_VERSION=6.12.0.122
# Tue, 29 Mar 2022 22:50:38 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 29 Mar 2022 22:51:01 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 29 Mar 2022 22:56:06 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:f003217c5aaebdfee0b9a448fbabd995e5f0159f5b231460c0ecc21baf171953`  
		Last Modified: Tue, 29 Mar 2022 00:28:02 GMT  
		Size: 27.2 MB (27151970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d839cde201cd1385a1c2c927214c614f1cd1bab02a62fd34b6df69e6f95daa7e`  
		Last Modified: Tue, 29 Mar 2022 23:02:05 GMT  
		Size: 2.8 MB (2777377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:158befabd0cf5fbeb7cb51a0cfc2f6c20399efe3be6abfd6d7dc8187d886b4a0`  
		Last Modified: Tue, 29 Mar 2022 23:02:14 GMT  
		Size: 64.8 MB (64760477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7f69220c106af4aa5ecc61935d51050e43fe6450996488e6c1d7fe5c5d7c2e1`  
		Last Modified: Tue, 29 Mar 2022 23:03:13 GMT  
		Size: 141.4 MB (141448127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0` - linux; arm variant v5

```console
$ docker pull mono@sha256:7f7e694bccdf74a53d7491c00db8088add1265f44830d8b0a365c7915304ef04
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.0 MB (191954448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71bb1b7df7ff58e8b649bb79421666f8422e0606d35629b29b8cf7c2b7ca4596`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:51:36 GMT
ADD file:7ac5498e2c44686d7eb272ef7645a0a64486cf942610f6754aa4a932f5b1a4be in / 
# Tue, 29 Mar 2022 00:51:37 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 08:50:15 GMT
ENV MONO_VERSION=6.12.0.122
# Tue, 29 Mar 2022 08:50:42 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 29 Mar 2022 08:51:31 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 29 Mar 2022 08:56:31 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:8f10b1b67f0119a2dd5f838a3e98ab2c412e4b51fb1e4841e2b79fd4cae86105`  
		Last Modified: Tue, 29 Mar 2022 01:06:51 GMT  
		Size: 24.9 MB (24887495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:103ccfc95d14718dd5bd47005c93225d5f82bdc075ccfc346e1b366afb616d57`  
		Last Modified: Tue, 29 Mar 2022 09:01:39 GMT  
		Size: 2.5 MB (2467692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13697b82f395905c310bf0030c74844e8f8fc5979a009c041a18de4488636164`  
		Last Modified: Tue, 29 Mar 2022 09:01:50 GMT  
		Size: 24.5 MB (24493260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90cc18056a6a14a94b009cdae75817ab5f9d1bea6b12aaf50cf5127985d9277f`  
		Last Modified: Tue, 29 Mar 2022 09:04:22 GMT  
		Size: 140.1 MB (140106001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0` - linux; arm variant v7

```console
$ docker pull mono@sha256:de55a06147b60da0b002c65b61e35e5bbcd09bb5d0a3c734b2004494af9e90b5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.9 MB (187869490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:068cd3b6737d2700c491cd15edf19aa585b83d26ea05ebaa0f5602558b0e57b7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 02:19:40 GMT
ADD file:8d54e000817531229c35a32eee074105c7b4d3c08b7ca56b1abdd80571687f28 in / 
# Tue, 29 Mar 2022 02:19:41 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 21:55:56 GMT
ENV MONO_VERSION=6.12.0.122
# Wed, 30 Mar 2022 21:56:22 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 30 Mar 2022 21:57:04 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 30 Mar 2022 22:01:31 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:d4bf0b27c669e589de33695047d638174fc2ca819a4366d5f80d1ad6b01c0c0e`  
		Last Modified: Tue, 29 Mar 2022 02:35:26 GMT  
		Size: 22.8 MB (22753045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:756cc431341070c1f6a772929e5d5daab96f2b040732e70d3cb93b3ce98d8542`  
		Last Modified: Wed, 30 Mar 2022 22:06:01 GMT  
		Size: 2.4 MB (2366920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:419ca67b5ee0885d9bcc46429070d185a04feb680b643fc29ceda334987a6a6f`  
		Last Modified: Wed, 30 Mar 2022 22:06:18 GMT  
		Size: 23.8 MB (23782719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:672029c9759800f327c1f06dc30ce05aac300a39d8f40f9c5d475f006a5486ba`  
		Last Modified: Wed, 30 Mar 2022 22:08:52 GMT  
		Size: 139.0 MB (138966806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:617fd6f5ff9238ff8782c0b154f5fbb1e51864ad1f009da0d0c5fcd54ff179c0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.5 MB (214465680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:721976153f55a700a3368032ce347eb3ae7b930fc6151b879332e0e99f1ca0cc`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Apr 2022 04:29:36 GMT
ADD file:5de4397c1295f7249c93907be599d96efbd9cd25909340d245ec8d1c9770f444 in / 
# Wed, 20 Apr 2022 04:29:37 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 09:34:15 GMT
ENV MONO_VERSION=6.12.0.122
# Wed, 20 Apr 2022 09:34:25 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 20 Apr 2022 09:34:40 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 20 Apr 2022 09:36:17 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:6c3e5b218d6477ff77053280968d5bdeaa5dcf16a803e917d98dd0ea8b93ac82`  
		Last Modified: Wed, 20 Apr 2022 04:36:38 GMT  
		Size: 25.9 MB (25908349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a5583d434a71d4775ae033dd3567325a5f5d01a34ff9f805631b17426570d60`  
		Last Modified: Wed, 20 Apr 2022 09:38:16 GMT  
		Size: 2.6 MB (2641065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1df7a4f3775402176b947b2ffb1f930879581b64904846f29bd8e5aa4000e4d`  
		Last Modified: Wed, 20 Apr 2022 09:38:20 GMT  
		Size: 29.3 MB (29318359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7f80c1eac9d435a1e808ae3c8eaf8a76d9e653e54edc1090cf4c2fc47f29f6e`  
		Last Modified: Wed, 20 Apr 2022 09:39:21 GMT  
		Size: 156.6 MB (156597907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0` - linux; 386

```console
$ docker pull mono@sha256:ef781f5c402c37c294ccf7397654b6a780c16c68ab05b1ee598260446e0049b0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.7 MB (241696337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faa267e26ab7e853336277f2575154ad396b6536c3cd9e8ba22824250ccc6fbd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Apr 2022 07:38:03 GMT
ADD file:602a25173054242f635a5a299845b7f1b56864ac5d3b8af1ae29dec3a9da119f in / 
# Wed, 20 Apr 2022 07:38:04 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 12:49:08 GMT
ENV MONO_VERSION=6.12.0.122
# Wed, 20 Apr 2022 12:49:17 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 20 Apr 2022 12:49:40 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 20 Apr 2022 12:51:19 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a13b13d818745c4d2234aab71df26e4a01bfe59f396ab62f20d156b94803650c`  
		Last Modified: Wed, 20 Apr 2022 07:45:46 GMT  
		Size: 27.8 MB (27799825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc07624832ff4b064bd2b3797a6774618e27f4c3a1e24419874628eeb613e7ba`  
		Last Modified: Wed, 20 Apr 2022 12:53:02 GMT  
		Size: 2.8 MB (2789161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d6af1a94baa95c219eaba2db2fb27e299572ac8d2859e1399838abdccae784c`  
		Last Modified: Wed, 20 Apr 2022 12:53:11 GMT  
		Size: 68.6 MB (68568946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cec0646bfa3d97be6f7515ad03d0cbb859adebe6cf3785cf1d36d06c8aa3f224`  
		Last Modified: Wed, 20 Apr 2022 12:54:22 GMT  
		Size: 142.5 MB (142538405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0` - linux; ppc64le

```console
$ docker pull mono@sha256:d8969fd75bcf7f2415543c536c50458a18d28e8cdab323db80eb053827d08c60
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.6 MB (203608008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:226cb9d82e8bfc2114d8f6e225a71870230cc71a214527422e1a68b2185008bc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:59 GMT
ADD file:7271d778d432a07f57fedf8d50d83699ef545acc9db9346f6fe75b0054af4cd1 in / 
# Tue, 29 Mar 2022 00:23:00 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 06:30:50 GMT
ENV MONO_VERSION=6.12.0.122
# Wed, 30 Mar 2022 06:32:19 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 30 Mar 2022 06:33:27 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 30 Mar 2022 06:43:44 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7db831386ce67ac1cf2b4f1513fe3746c9ea2b8d4c82efca75be638eaf533614`  
		Last Modified: Tue, 29 Mar 2022 00:34:41 GMT  
		Size: 30.6 MB (30560163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55feab57ab15634326c723014da448815650e9737d6c5671ca5a4cd4503905cb`  
		Last Modified: Wed, 30 Mar 2022 06:53:14 GMT  
		Size: 2.9 MB (2892687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c00a3dcf742861f8ca53669004126ef6bead547f42b4f28c1d7ba21debbc8b5`  
		Last Modified: Wed, 30 Mar 2022 06:53:20 GMT  
		Size: 26.9 MB (26873425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af736d47f1875d0d79d7c43b3fce41fcb3f2129622c09182d7916c44b731e9b2`  
		Last Modified: Wed, 30 Mar 2022 06:54:30 GMT  
		Size: 143.3 MB (143281733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.12.0-slim`

```console
$ docker pull mono@sha256:bc7933bac89d6c7f5e9c656111b402a44420deb7a05c7adefcef682c114cc212
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
$ docker pull mono@sha256:87038a7da02d5efff3bfab1ec93dc3020d04cd3fad6bff479d3252cf3cb13695
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.7 MB (94689824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcc621103738e68eb59281907e2ec643435dbb8dd82d504d49655526191a0199`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:38 GMT
ADD file:59187422476c57db46e60f894a4cfd0f243e80230ef9ea75b2d8dd4925d59df3 in / 
# Tue, 29 Mar 2022 00:22:38 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 22:50:30 GMT
ENV MONO_VERSION=6.12.0.122
# Tue, 29 Mar 2022 22:50:38 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 29 Mar 2022 22:51:01 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:f003217c5aaebdfee0b9a448fbabd995e5f0159f5b231460c0ecc21baf171953`  
		Last Modified: Tue, 29 Mar 2022 00:28:02 GMT  
		Size: 27.2 MB (27151970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d839cde201cd1385a1c2c927214c614f1cd1bab02a62fd34b6df69e6f95daa7e`  
		Last Modified: Tue, 29 Mar 2022 23:02:05 GMT  
		Size: 2.8 MB (2777377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:158befabd0cf5fbeb7cb51a0cfc2f6c20399efe3be6abfd6d7dc8187d886b4a0`  
		Last Modified: Tue, 29 Mar 2022 23:02:14 GMT  
		Size: 64.8 MB (64760477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:2858e2824edbcaaefd73dd8b888c39d6c10cfd27bc7b2b1b420570403b00a924
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51848447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41535ed442f086e8d8103e40ebab589e248cc742505317bfb8c17b5746bc567f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:51:36 GMT
ADD file:7ac5498e2c44686d7eb272ef7645a0a64486cf942610f6754aa4a932f5b1a4be in / 
# Tue, 29 Mar 2022 00:51:37 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 08:50:15 GMT
ENV MONO_VERSION=6.12.0.122
# Tue, 29 Mar 2022 08:50:42 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 29 Mar 2022 08:51:31 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:8f10b1b67f0119a2dd5f838a3e98ab2c412e4b51fb1e4841e2b79fd4cae86105`  
		Last Modified: Tue, 29 Mar 2022 01:06:51 GMT  
		Size: 24.9 MB (24887495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:103ccfc95d14718dd5bd47005c93225d5f82bdc075ccfc346e1b366afb616d57`  
		Last Modified: Tue, 29 Mar 2022 09:01:39 GMT  
		Size: 2.5 MB (2467692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13697b82f395905c310bf0030c74844e8f8fc5979a009c041a18de4488636164`  
		Last Modified: Tue, 29 Mar 2022 09:01:50 GMT  
		Size: 24.5 MB (24493260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:c8f9bff7726932d61ceb479135172d8ad8d953634e902d99afa4b04b35c8979c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48902684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35df12dffc423503a586d8b0c8f4b5056157ba44d8baa9a3a8ebc94f4b728f4e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 02:19:40 GMT
ADD file:8d54e000817531229c35a32eee074105c7b4d3c08b7ca56b1abdd80571687f28 in / 
# Tue, 29 Mar 2022 02:19:41 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 21:55:56 GMT
ENV MONO_VERSION=6.12.0.122
# Wed, 30 Mar 2022 21:56:22 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 30 Mar 2022 21:57:04 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:d4bf0b27c669e589de33695047d638174fc2ca819a4366d5f80d1ad6b01c0c0e`  
		Last Modified: Tue, 29 Mar 2022 02:35:26 GMT  
		Size: 22.8 MB (22753045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:756cc431341070c1f6a772929e5d5daab96f2b040732e70d3cb93b3ce98d8542`  
		Last Modified: Wed, 30 Mar 2022 22:06:01 GMT  
		Size: 2.4 MB (2366920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:419ca67b5ee0885d9bcc46429070d185a04feb680b643fc29ceda334987a6a6f`  
		Last Modified: Wed, 30 Mar 2022 22:06:18 GMT  
		Size: 23.8 MB (23782719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:0f3837c80f89d4cc61d33d11680310dd7b9170aa4a20287829db1cf4ff83169c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.9 MB (57867773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a03207fd5f3c9c31e878dec4d955581897e75177774ac4915f726360915f8e8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Apr 2022 04:29:36 GMT
ADD file:5de4397c1295f7249c93907be599d96efbd9cd25909340d245ec8d1c9770f444 in / 
# Wed, 20 Apr 2022 04:29:37 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 09:34:15 GMT
ENV MONO_VERSION=6.12.0.122
# Wed, 20 Apr 2022 09:34:25 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 20 Apr 2022 09:34:40 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:6c3e5b218d6477ff77053280968d5bdeaa5dcf16a803e917d98dd0ea8b93ac82`  
		Last Modified: Wed, 20 Apr 2022 04:36:38 GMT  
		Size: 25.9 MB (25908349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a5583d434a71d4775ae033dd3567325a5f5d01a34ff9f805631b17426570d60`  
		Last Modified: Wed, 20 Apr 2022 09:38:16 GMT  
		Size: 2.6 MB (2641065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1df7a4f3775402176b947b2ffb1f930879581b64904846f29bd8e5aa4000e4d`  
		Last Modified: Wed, 20 Apr 2022 09:38:20 GMT  
		Size: 29.3 MB (29318359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0-slim` - linux; 386

```console
$ docker pull mono@sha256:a620c36d6b438c94797eaa6b17b2452369ac55ab8a59a1bcf8b4501df1eea0c5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.2 MB (99157932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95ff55aea4f3ffc1da74cea929a23a78ed6dc8901847098c5878018368c9da5d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Apr 2022 07:38:03 GMT
ADD file:602a25173054242f635a5a299845b7f1b56864ac5d3b8af1ae29dec3a9da119f in / 
# Wed, 20 Apr 2022 07:38:04 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 12:49:08 GMT
ENV MONO_VERSION=6.12.0.122
# Wed, 20 Apr 2022 12:49:17 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 20 Apr 2022 12:49:40 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a13b13d818745c4d2234aab71df26e4a01bfe59f396ab62f20d156b94803650c`  
		Last Modified: Wed, 20 Apr 2022 07:45:46 GMT  
		Size: 27.8 MB (27799825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc07624832ff4b064bd2b3797a6774618e27f4c3a1e24419874628eeb613e7ba`  
		Last Modified: Wed, 20 Apr 2022 12:53:02 GMT  
		Size: 2.8 MB (2789161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d6af1a94baa95c219eaba2db2fb27e299572ac8d2859e1399838abdccae784c`  
		Last Modified: Wed, 20 Apr 2022 12:53:11 GMT  
		Size: 68.6 MB (68568946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:9b3a0defce0a5c2ae9bfc6d34af244911ccd407e7973e0f3eedce5fe3670f57e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60326275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5184331441c848755861d28d51bfb13f10dc8e51ace7607db24b3326be9c1166`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:59 GMT
ADD file:7271d778d432a07f57fedf8d50d83699ef545acc9db9346f6fe75b0054af4cd1 in / 
# Tue, 29 Mar 2022 00:23:00 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 06:30:50 GMT
ENV MONO_VERSION=6.12.0.122
# Wed, 30 Mar 2022 06:32:19 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 30 Mar 2022 06:33:27 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7db831386ce67ac1cf2b4f1513fe3746c9ea2b8d4c82efca75be638eaf533614`  
		Last Modified: Tue, 29 Mar 2022 00:34:41 GMT  
		Size: 30.6 MB (30560163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55feab57ab15634326c723014da448815650e9737d6c5671ca5a4cd4503905cb`  
		Last Modified: Wed, 30 Mar 2022 06:53:14 GMT  
		Size: 2.9 MB (2892687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c00a3dcf742861f8ca53669004126ef6bead547f42b4f28c1d7ba21debbc8b5`  
		Last Modified: Wed, 30 Mar 2022 06:53:20 GMT  
		Size: 26.9 MB (26873425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.12.0.122`

```console
$ docker pull mono@sha256:288dce942fc8031ee29e492d5c8f6beec7d6a38df14ee0f8cf28070d4d555e44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:6.12.0.122` - linux; amd64

```console
$ docker pull mono@sha256:abcb22d3b82c95b20ff5c90f329cb759314b70e1781a67315b1ec2bb719e0cda
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.1 MB (236137951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a0982a1a3d0d9f836f390567b3d9452c91ca96d6b8b2e633edf0cf7994be535`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:38 GMT
ADD file:59187422476c57db46e60f894a4cfd0f243e80230ef9ea75b2d8dd4925d59df3 in / 
# Tue, 29 Mar 2022 00:22:38 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 22:50:30 GMT
ENV MONO_VERSION=6.12.0.122
# Tue, 29 Mar 2022 22:50:38 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 29 Mar 2022 22:51:01 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 29 Mar 2022 22:56:06 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:f003217c5aaebdfee0b9a448fbabd995e5f0159f5b231460c0ecc21baf171953`  
		Last Modified: Tue, 29 Mar 2022 00:28:02 GMT  
		Size: 27.2 MB (27151970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d839cde201cd1385a1c2c927214c614f1cd1bab02a62fd34b6df69e6f95daa7e`  
		Last Modified: Tue, 29 Mar 2022 23:02:05 GMT  
		Size: 2.8 MB (2777377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:158befabd0cf5fbeb7cb51a0cfc2f6c20399efe3be6abfd6d7dc8187d886b4a0`  
		Last Modified: Tue, 29 Mar 2022 23:02:14 GMT  
		Size: 64.8 MB (64760477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7f69220c106af4aa5ecc61935d51050e43fe6450996488e6c1d7fe5c5d7c2e1`  
		Last Modified: Tue, 29 Mar 2022 23:03:13 GMT  
		Size: 141.4 MB (141448127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0.122` - linux; arm variant v5

```console
$ docker pull mono@sha256:7f7e694bccdf74a53d7491c00db8088add1265f44830d8b0a365c7915304ef04
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.0 MB (191954448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71bb1b7df7ff58e8b649bb79421666f8422e0606d35629b29b8cf7c2b7ca4596`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:51:36 GMT
ADD file:7ac5498e2c44686d7eb272ef7645a0a64486cf942610f6754aa4a932f5b1a4be in / 
# Tue, 29 Mar 2022 00:51:37 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 08:50:15 GMT
ENV MONO_VERSION=6.12.0.122
# Tue, 29 Mar 2022 08:50:42 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 29 Mar 2022 08:51:31 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 29 Mar 2022 08:56:31 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:8f10b1b67f0119a2dd5f838a3e98ab2c412e4b51fb1e4841e2b79fd4cae86105`  
		Last Modified: Tue, 29 Mar 2022 01:06:51 GMT  
		Size: 24.9 MB (24887495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:103ccfc95d14718dd5bd47005c93225d5f82bdc075ccfc346e1b366afb616d57`  
		Last Modified: Tue, 29 Mar 2022 09:01:39 GMT  
		Size: 2.5 MB (2467692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13697b82f395905c310bf0030c74844e8f8fc5979a009c041a18de4488636164`  
		Last Modified: Tue, 29 Mar 2022 09:01:50 GMT  
		Size: 24.5 MB (24493260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90cc18056a6a14a94b009cdae75817ab5f9d1bea6b12aaf50cf5127985d9277f`  
		Last Modified: Tue, 29 Mar 2022 09:04:22 GMT  
		Size: 140.1 MB (140106001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0.122` - linux; arm variant v7

```console
$ docker pull mono@sha256:de55a06147b60da0b002c65b61e35e5bbcd09bb5d0a3c734b2004494af9e90b5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.9 MB (187869490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:068cd3b6737d2700c491cd15edf19aa585b83d26ea05ebaa0f5602558b0e57b7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 02:19:40 GMT
ADD file:8d54e000817531229c35a32eee074105c7b4d3c08b7ca56b1abdd80571687f28 in / 
# Tue, 29 Mar 2022 02:19:41 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 21:55:56 GMT
ENV MONO_VERSION=6.12.0.122
# Wed, 30 Mar 2022 21:56:22 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 30 Mar 2022 21:57:04 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 30 Mar 2022 22:01:31 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:d4bf0b27c669e589de33695047d638174fc2ca819a4366d5f80d1ad6b01c0c0e`  
		Last Modified: Tue, 29 Mar 2022 02:35:26 GMT  
		Size: 22.8 MB (22753045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:756cc431341070c1f6a772929e5d5daab96f2b040732e70d3cb93b3ce98d8542`  
		Last Modified: Wed, 30 Mar 2022 22:06:01 GMT  
		Size: 2.4 MB (2366920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:419ca67b5ee0885d9bcc46429070d185a04feb680b643fc29ceda334987a6a6f`  
		Last Modified: Wed, 30 Mar 2022 22:06:18 GMT  
		Size: 23.8 MB (23782719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:672029c9759800f327c1f06dc30ce05aac300a39d8f40f9c5d475f006a5486ba`  
		Last Modified: Wed, 30 Mar 2022 22:08:52 GMT  
		Size: 139.0 MB (138966806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0.122` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:617fd6f5ff9238ff8782c0b154f5fbb1e51864ad1f009da0d0c5fcd54ff179c0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.5 MB (214465680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:721976153f55a700a3368032ce347eb3ae7b930fc6151b879332e0e99f1ca0cc`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Apr 2022 04:29:36 GMT
ADD file:5de4397c1295f7249c93907be599d96efbd9cd25909340d245ec8d1c9770f444 in / 
# Wed, 20 Apr 2022 04:29:37 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 09:34:15 GMT
ENV MONO_VERSION=6.12.0.122
# Wed, 20 Apr 2022 09:34:25 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 20 Apr 2022 09:34:40 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 20 Apr 2022 09:36:17 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:6c3e5b218d6477ff77053280968d5bdeaa5dcf16a803e917d98dd0ea8b93ac82`  
		Last Modified: Wed, 20 Apr 2022 04:36:38 GMT  
		Size: 25.9 MB (25908349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a5583d434a71d4775ae033dd3567325a5f5d01a34ff9f805631b17426570d60`  
		Last Modified: Wed, 20 Apr 2022 09:38:16 GMT  
		Size: 2.6 MB (2641065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1df7a4f3775402176b947b2ffb1f930879581b64904846f29bd8e5aa4000e4d`  
		Last Modified: Wed, 20 Apr 2022 09:38:20 GMT  
		Size: 29.3 MB (29318359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7f80c1eac9d435a1e808ae3c8eaf8a76d9e653e54edc1090cf4c2fc47f29f6e`  
		Last Modified: Wed, 20 Apr 2022 09:39:21 GMT  
		Size: 156.6 MB (156597907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0.122` - linux; 386

```console
$ docker pull mono@sha256:ef781f5c402c37c294ccf7397654b6a780c16c68ab05b1ee598260446e0049b0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.7 MB (241696337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faa267e26ab7e853336277f2575154ad396b6536c3cd9e8ba22824250ccc6fbd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Apr 2022 07:38:03 GMT
ADD file:602a25173054242f635a5a299845b7f1b56864ac5d3b8af1ae29dec3a9da119f in / 
# Wed, 20 Apr 2022 07:38:04 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 12:49:08 GMT
ENV MONO_VERSION=6.12.0.122
# Wed, 20 Apr 2022 12:49:17 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 20 Apr 2022 12:49:40 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 20 Apr 2022 12:51:19 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a13b13d818745c4d2234aab71df26e4a01bfe59f396ab62f20d156b94803650c`  
		Last Modified: Wed, 20 Apr 2022 07:45:46 GMT  
		Size: 27.8 MB (27799825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc07624832ff4b064bd2b3797a6774618e27f4c3a1e24419874628eeb613e7ba`  
		Last Modified: Wed, 20 Apr 2022 12:53:02 GMT  
		Size: 2.8 MB (2789161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d6af1a94baa95c219eaba2db2fb27e299572ac8d2859e1399838abdccae784c`  
		Last Modified: Wed, 20 Apr 2022 12:53:11 GMT  
		Size: 68.6 MB (68568946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cec0646bfa3d97be6f7515ad03d0cbb859adebe6cf3785cf1d36d06c8aa3f224`  
		Last Modified: Wed, 20 Apr 2022 12:54:22 GMT  
		Size: 142.5 MB (142538405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0.122` - linux; ppc64le

```console
$ docker pull mono@sha256:d8969fd75bcf7f2415543c536c50458a18d28e8cdab323db80eb053827d08c60
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.6 MB (203608008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:226cb9d82e8bfc2114d8f6e225a71870230cc71a214527422e1a68b2185008bc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:59 GMT
ADD file:7271d778d432a07f57fedf8d50d83699ef545acc9db9346f6fe75b0054af4cd1 in / 
# Tue, 29 Mar 2022 00:23:00 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 06:30:50 GMT
ENV MONO_VERSION=6.12.0.122
# Wed, 30 Mar 2022 06:32:19 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 30 Mar 2022 06:33:27 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 30 Mar 2022 06:43:44 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7db831386ce67ac1cf2b4f1513fe3746c9ea2b8d4c82efca75be638eaf533614`  
		Last Modified: Tue, 29 Mar 2022 00:34:41 GMT  
		Size: 30.6 MB (30560163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55feab57ab15634326c723014da448815650e9737d6c5671ca5a4cd4503905cb`  
		Last Modified: Wed, 30 Mar 2022 06:53:14 GMT  
		Size: 2.9 MB (2892687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c00a3dcf742861f8ca53669004126ef6bead547f42b4f28c1d7ba21debbc8b5`  
		Last Modified: Wed, 30 Mar 2022 06:53:20 GMT  
		Size: 26.9 MB (26873425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af736d47f1875d0d79d7c43b3fce41fcb3f2129622c09182d7916c44b731e9b2`  
		Last Modified: Wed, 30 Mar 2022 06:54:30 GMT  
		Size: 143.3 MB (143281733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.12.0.122-slim`

```console
$ docker pull mono@sha256:bc7933bac89d6c7f5e9c656111b402a44420deb7a05c7adefcef682c114cc212
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:6.12.0.122-slim` - linux; amd64

```console
$ docker pull mono@sha256:87038a7da02d5efff3bfab1ec93dc3020d04cd3fad6bff479d3252cf3cb13695
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.7 MB (94689824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcc621103738e68eb59281907e2ec643435dbb8dd82d504d49655526191a0199`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:38 GMT
ADD file:59187422476c57db46e60f894a4cfd0f243e80230ef9ea75b2d8dd4925d59df3 in / 
# Tue, 29 Mar 2022 00:22:38 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 22:50:30 GMT
ENV MONO_VERSION=6.12.0.122
# Tue, 29 Mar 2022 22:50:38 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 29 Mar 2022 22:51:01 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:f003217c5aaebdfee0b9a448fbabd995e5f0159f5b231460c0ecc21baf171953`  
		Last Modified: Tue, 29 Mar 2022 00:28:02 GMT  
		Size: 27.2 MB (27151970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d839cde201cd1385a1c2c927214c614f1cd1bab02a62fd34b6df69e6f95daa7e`  
		Last Modified: Tue, 29 Mar 2022 23:02:05 GMT  
		Size: 2.8 MB (2777377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:158befabd0cf5fbeb7cb51a0cfc2f6c20399efe3be6abfd6d7dc8187d886b4a0`  
		Last Modified: Tue, 29 Mar 2022 23:02:14 GMT  
		Size: 64.8 MB (64760477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0.122-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:2858e2824edbcaaefd73dd8b888c39d6c10cfd27bc7b2b1b420570403b00a924
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51848447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41535ed442f086e8d8103e40ebab589e248cc742505317bfb8c17b5746bc567f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:51:36 GMT
ADD file:7ac5498e2c44686d7eb272ef7645a0a64486cf942610f6754aa4a932f5b1a4be in / 
# Tue, 29 Mar 2022 00:51:37 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 08:50:15 GMT
ENV MONO_VERSION=6.12.0.122
# Tue, 29 Mar 2022 08:50:42 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 29 Mar 2022 08:51:31 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:8f10b1b67f0119a2dd5f838a3e98ab2c412e4b51fb1e4841e2b79fd4cae86105`  
		Last Modified: Tue, 29 Mar 2022 01:06:51 GMT  
		Size: 24.9 MB (24887495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:103ccfc95d14718dd5bd47005c93225d5f82bdc075ccfc346e1b366afb616d57`  
		Last Modified: Tue, 29 Mar 2022 09:01:39 GMT  
		Size: 2.5 MB (2467692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13697b82f395905c310bf0030c74844e8f8fc5979a009c041a18de4488636164`  
		Last Modified: Tue, 29 Mar 2022 09:01:50 GMT  
		Size: 24.5 MB (24493260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0.122-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:c8f9bff7726932d61ceb479135172d8ad8d953634e902d99afa4b04b35c8979c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48902684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35df12dffc423503a586d8b0c8f4b5056157ba44d8baa9a3a8ebc94f4b728f4e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 02:19:40 GMT
ADD file:8d54e000817531229c35a32eee074105c7b4d3c08b7ca56b1abdd80571687f28 in / 
# Tue, 29 Mar 2022 02:19:41 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 21:55:56 GMT
ENV MONO_VERSION=6.12.0.122
# Wed, 30 Mar 2022 21:56:22 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 30 Mar 2022 21:57:04 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:d4bf0b27c669e589de33695047d638174fc2ca819a4366d5f80d1ad6b01c0c0e`  
		Last Modified: Tue, 29 Mar 2022 02:35:26 GMT  
		Size: 22.8 MB (22753045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:756cc431341070c1f6a772929e5d5daab96f2b040732e70d3cb93b3ce98d8542`  
		Last Modified: Wed, 30 Mar 2022 22:06:01 GMT  
		Size: 2.4 MB (2366920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:419ca67b5ee0885d9bcc46429070d185a04feb680b643fc29ceda334987a6a6f`  
		Last Modified: Wed, 30 Mar 2022 22:06:18 GMT  
		Size: 23.8 MB (23782719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0.122-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:0f3837c80f89d4cc61d33d11680310dd7b9170aa4a20287829db1cf4ff83169c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.9 MB (57867773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a03207fd5f3c9c31e878dec4d955581897e75177774ac4915f726360915f8e8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Apr 2022 04:29:36 GMT
ADD file:5de4397c1295f7249c93907be599d96efbd9cd25909340d245ec8d1c9770f444 in / 
# Wed, 20 Apr 2022 04:29:37 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 09:34:15 GMT
ENV MONO_VERSION=6.12.0.122
# Wed, 20 Apr 2022 09:34:25 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 20 Apr 2022 09:34:40 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:6c3e5b218d6477ff77053280968d5bdeaa5dcf16a803e917d98dd0ea8b93ac82`  
		Last Modified: Wed, 20 Apr 2022 04:36:38 GMT  
		Size: 25.9 MB (25908349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a5583d434a71d4775ae033dd3567325a5f5d01a34ff9f805631b17426570d60`  
		Last Modified: Wed, 20 Apr 2022 09:38:16 GMT  
		Size: 2.6 MB (2641065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1df7a4f3775402176b947b2ffb1f930879581b64904846f29bd8e5aa4000e4d`  
		Last Modified: Wed, 20 Apr 2022 09:38:20 GMT  
		Size: 29.3 MB (29318359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0.122-slim` - linux; 386

```console
$ docker pull mono@sha256:a620c36d6b438c94797eaa6b17b2452369ac55ab8a59a1bcf8b4501df1eea0c5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.2 MB (99157932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95ff55aea4f3ffc1da74cea929a23a78ed6dc8901847098c5878018368c9da5d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Apr 2022 07:38:03 GMT
ADD file:602a25173054242f635a5a299845b7f1b56864ac5d3b8af1ae29dec3a9da119f in / 
# Wed, 20 Apr 2022 07:38:04 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 12:49:08 GMT
ENV MONO_VERSION=6.12.0.122
# Wed, 20 Apr 2022 12:49:17 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 20 Apr 2022 12:49:40 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a13b13d818745c4d2234aab71df26e4a01bfe59f396ab62f20d156b94803650c`  
		Last Modified: Wed, 20 Apr 2022 07:45:46 GMT  
		Size: 27.8 MB (27799825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc07624832ff4b064bd2b3797a6774618e27f4c3a1e24419874628eeb613e7ba`  
		Last Modified: Wed, 20 Apr 2022 12:53:02 GMT  
		Size: 2.8 MB (2789161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d6af1a94baa95c219eaba2db2fb27e299572ac8d2859e1399838abdccae784c`  
		Last Modified: Wed, 20 Apr 2022 12:53:11 GMT  
		Size: 68.6 MB (68568946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0.122-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:9b3a0defce0a5c2ae9bfc6d34af244911ccd407e7973e0f3eedce5fe3670f57e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60326275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5184331441c848755861d28d51bfb13f10dc8e51ace7607db24b3326be9c1166`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:59 GMT
ADD file:7271d778d432a07f57fedf8d50d83699ef545acc9db9346f6fe75b0054af4cd1 in / 
# Tue, 29 Mar 2022 00:23:00 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 06:30:50 GMT
ENV MONO_VERSION=6.12.0.122
# Wed, 30 Mar 2022 06:32:19 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 30 Mar 2022 06:33:27 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7db831386ce67ac1cf2b4f1513fe3746c9ea2b8d4c82efca75be638eaf533614`  
		Last Modified: Tue, 29 Mar 2022 00:34:41 GMT  
		Size: 30.6 MB (30560163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55feab57ab15634326c723014da448815650e9737d6c5671ca5a4cd4503905cb`  
		Last Modified: Wed, 30 Mar 2022 06:53:14 GMT  
		Size: 2.9 MB (2892687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c00a3dcf742861f8ca53669004126ef6bead547f42b4f28c1d7ba21debbc8b5`  
		Last Modified: Wed, 30 Mar 2022 06:53:20 GMT  
		Size: 26.9 MB (26873425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:latest`

```console
$ docker pull mono@sha256:288dce942fc8031ee29e492d5c8f6beec7d6a38df14ee0f8cf28070d4d555e44
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
$ docker pull mono@sha256:abcb22d3b82c95b20ff5c90f329cb759314b70e1781a67315b1ec2bb719e0cda
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.1 MB (236137951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a0982a1a3d0d9f836f390567b3d9452c91ca96d6b8b2e633edf0cf7994be535`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:38 GMT
ADD file:59187422476c57db46e60f894a4cfd0f243e80230ef9ea75b2d8dd4925d59df3 in / 
# Tue, 29 Mar 2022 00:22:38 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 22:50:30 GMT
ENV MONO_VERSION=6.12.0.122
# Tue, 29 Mar 2022 22:50:38 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 29 Mar 2022 22:51:01 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 29 Mar 2022 22:56:06 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:f003217c5aaebdfee0b9a448fbabd995e5f0159f5b231460c0ecc21baf171953`  
		Last Modified: Tue, 29 Mar 2022 00:28:02 GMT  
		Size: 27.2 MB (27151970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d839cde201cd1385a1c2c927214c614f1cd1bab02a62fd34b6df69e6f95daa7e`  
		Last Modified: Tue, 29 Mar 2022 23:02:05 GMT  
		Size: 2.8 MB (2777377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:158befabd0cf5fbeb7cb51a0cfc2f6c20399efe3be6abfd6d7dc8187d886b4a0`  
		Last Modified: Tue, 29 Mar 2022 23:02:14 GMT  
		Size: 64.8 MB (64760477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7f69220c106af4aa5ecc61935d51050e43fe6450996488e6c1d7fe5c5d7c2e1`  
		Last Modified: Tue, 29 Mar 2022 23:03:13 GMT  
		Size: 141.4 MB (141448127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:latest` - linux; arm variant v5

```console
$ docker pull mono@sha256:7f7e694bccdf74a53d7491c00db8088add1265f44830d8b0a365c7915304ef04
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.0 MB (191954448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71bb1b7df7ff58e8b649bb79421666f8422e0606d35629b29b8cf7c2b7ca4596`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:51:36 GMT
ADD file:7ac5498e2c44686d7eb272ef7645a0a64486cf942610f6754aa4a932f5b1a4be in / 
# Tue, 29 Mar 2022 00:51:37 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 08:50:15 GMT
ENV MONO_VERSION=6.12.0.122
# Tue, 29 Mar 2022 08:50:42 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 29 Mar 2022 08:51:31 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 29 Mar 2022 08:56:31 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:8f10b1b67f0119a2dd5f838a3e98ab2c412e4b51fb1e4841e2b79fd4cae86105`  
		Last Modified: Tue, 29 Mar 2022 01:06:51 GMT  
		Size: 24.9 MB (24887495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:103ccfc95d14718dd5bd47005c93225d5f82bdc075ccfc346e1b366afb616d57`  
		Last Modified: Tue, 29 Mar 2022 09:01:39 GMT  
		Size: 2.5 MB (2467692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13697b82f395905c310bf0030c74844e8f8fc5979a009c041a18de4488636164`  
		Last Modified: Tue, 29 Mar 2022 09:01:50 GMT  
		Size: 24.5 MB (24493260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90cc18056a6a14a94b009cdae75817ab5f9d1bea6b12aaf50cf5127985d9277f`  
		Last Modified: Tue, 29 Mar 2022 09:04:22 GMT  
		Size: 140.1 MB (140106001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:latest` - linux; arm variant v7

```console
$ docker pull mono@sha256:de55a06147b60da0b002c65b61e35e5bbcd09bb5d0a3c734b2004494af9e90b5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.9 MB (187869490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:068cd3b6737d2700c491cd15edf19aa585b83d26ea05ebaa0f5602558b0e57b7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 02:19:40 GMT
ADD file:8d54e000817531229c35a32eee074105c7b4d3c08b7ca56b1abdd80571687f28 in / 
# Tue, 29 Mar 2022 02:19:41 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 21:55:56 GMT
ENV MONO_VERSION=6.12.0.122
# Wed, 30 Mar 2022 21:56:22 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 30 Mar 2022 21:57:04 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 30 Mar 2022 22:01:31 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:d4bf0b27c669e589de33695047d638174fc2ca819a4366d5f80d1ad6b01c0c0e`  
		Last Modified: Tue, 29 Mar 2022 02:35:26 GMT  
		Size: 22.8 MB (22753045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:756cc431341070c1f6a772929e5d5daab96f2b040732e70d3cb93b3ce98d8542`  
		Last Modified: Wed, 30 Mar 2022 22:06:01 GMT  
		Size: 2.4 MB (2366920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:419ca67b5ee0885d9bcc46429070d185a04feb680b643fc29ceda334987a6a6f`  
		Last Modified: Wed, 30 Mar 2022 22:06:18 GMT  
		Size: 23.8 MB (23782719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:672029c9759800f327c1f06dc30ce05aac300a39d8f40f9c5d475f006a5486ba`  
		Last Modified: Wed, 30 Mar 2022 22:08:52 GMT  
		Size: 139.0 MB (138966806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:latest` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:617fd6f5ff9238ff8782c0b154f5fbb1e51864ad1f009da0d0c5fcd54ff179c0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.5 MB (214465680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:721976153f55a700a3368032ce347eb3ae7b930fc6151b879332e0e99f1ca0cc`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Apr 2022 04:29:36 GMT
ADD file:5de4397c1295f7249c93907be599d96efbd9cd25909340d245ec8d1c9770f444 in / 
# Wed, 20 Apr 2022 04:29:37 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 09:34:15 GMT
ENV MONO_VERSION=6.12.0.122
# Wed, 20 Apr 2022 09:34:25 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 20 Apr 2022 09:34:40 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 20 Apr 2022 09:36:17 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:6c3e5b218d6477ff77053280968d5bdeaa5dcf16a803e917d98dd0ea8b93ac82`  
		Last Modified: Wed, 20 Apr 2022 04:36:38 GMT  
		Size: 25.9 MB (25908349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a5583d434a71d4775ae033dd3567325a5f5d01a34ff9f805631b17426570d60`  
		Last Modified: Wed, 20 Apr 2022 09:38:16 GMT  
		Size: 2.6 MB (2641065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1df7a4f3775402176b947b2ffb1f930879581b64904846f29bd8e5aa4000e4d`  
		Last Modified: Wed, 20 Apr 2022 09:38:20 GMT  
		Size: 29.3 MB (29318359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7f80c1eac9d435a1e808ae3c8eaf8a76d9e653e54edc1090cf4c2fc47f29f6e`  
		Last Modified: Wed, 20 Apr 2022 09:39:21 GMT  
		Size: 156.6 MB (156597907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:latest` - linux; 386

```console
$ docker pull mono@sha256:ef781f5c402c37c294ccf7397654b6a780c16c68ab05b1ee598260446e0049b0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.7 MB (241696337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faa267e26ab7e853336277f2575154ad396b6536c3cd9e8ba22824250ccc6fbd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Apr 2022 07:38:03 GMT
ADD file:602a25173054242f635a5a299845b7f1b56864ac5d3b8af1ae29dec3a9da119f in / 
# Wed, 20 Apr 2022 07:38:04 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 12:49:08 GMT
ENV MONO_VERSION=6.12.0.122
# Wed, 20 Apr 2022 12:49:17 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 20 Apr 2022 12:49:40 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 20 Apr 2022 12:51:19 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a13b13d818745c4d2234aab71df26e4a01bfe59f396ab62f20d156b94803650c`  
		Last Modified: Wed, 20 Apr 2022 07:45:46 GMT  
		Size: 27.8 MB (27799825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc07624832ff4b064bd2b3797a6774618e27f4c3a1e24419874628eeb613e7ba`  
		Last Modified: Wed, 20 Apr 2022 12:53:02 GMT  
		Size: 2.8 MB (2789161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d6af1a94baa95c219eaba2db2fb27e299572ac8d2859e1399838abdccae784c`  
		Last Modified: Wed, 20 Apr 2022 12:53:11 GMT  
		Size: 68.6 MB (68568946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cec0646bfa3d97be6f7515ad03d0cbb859adebe6cf3785cf1d36d06c8aa3f224`  
		Last Modified: Wed, 20 Apr 2022 12:54:22 GMT  
		Size: 142.5 MB (142538405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:latest` - linux; ppc64le

```console
$ docker pull mono@sha256:d8969fd75bcf7f2415543c536c50458a18d28e8cdab323db80eb053827d08c60
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.6 MB (203608008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:226cb9d82e8bfc2114d8f6e225a71870230cc71a214527422e1a68b2185008bc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:59 GMT
ADD file:7271d778d432a07f57fedf8d50d83699ef545acc9db9346f6fe75b0054af4cd1 in / 
# Tue, 29 Mar 2022 00:23:00 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 06:30:50 GMT
ENV MONO_VERSION=6.12.0.122
# Wed, 30 Mar 2022 06:32:19 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 30 Mar 2022 06:33:27 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 30 Mar 2022 06:43:44 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7db831386ce67ac1cf2b4f1513fe3746c9ea2b8d4c82efca75be638eaf533614`  
		Last Modified: Tue, 29 Mar 2022 00:34:41 GMT  
		Size: 30.6 MB (30560163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55feab57ab15634326c723014da448815650e9737d6c5671ca5a4cd4503905cb`  
		Last Modified: Wed, 30 Mar 2022 06:53:14 GMT  
		Size: 2.9 MB (2892687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c00a3dcf742861f8ca53669004126ef6bead547f42b4f28c1d7ba21debbc8b5`  
		Last Modified: Wed, 30 Mar 2022 06:53:20 GMT  
		Size: 26.9 MB (26873425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af736d47f1875d0d79d7c43b3fce41fcb3f2129622c09182d7916c44b731e9b2`  
		Last Modified: Wed, 30 Mar 2022 06:54:30 GMT  
		Size: 143.3 MB (143281733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:slim`

```console
$ docker pull mono@sha256:bc7933bac89d6c7f5e9c656111b402a44420deb7a05c7adefcef682c114cc212
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
$ docker pull mono@sha256:87038a7da02d5efff3bfab1ec93dc3020d04cd3fad6bff479d3252cf3cb13695
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.7 MB (94689824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcc621103738e68eb59281907e2ec643435dbb8dd82d504d49655526191a0199`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:38 GMT
ADD file:59187422476c57db46e60f894a4cfd0f243e80230ef9ea75b2d8dd4925d59df3 in / 
# Tue, 29 Mar 2022 00:22:38 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 22:50:30 GMT
ENV MONO_VERSION=6.12.0.122
# Tue, 29 Mar 2022 22:50:38 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 29 Mar 2022 22:51:01 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:f003217c5aaebdfee0b9a448fbabd995e5f0159f5b231460c0ecc21baf171953`  
		Last Modified: Tue, 29 Mar 2022 00:28:02 GMT  
		Size: 27.2 MB (27151970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d839cde201cd1385a1c2c927214c614f1cd1bab02a62fd34b6df69e6f95daa7e`  
		Last Modified: Tue, 29 Mar 2022 23:02:05 GMT  
		Size: 2.8 MB (2777377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:158befabd0cf5fbeb7cb51a0cfc2f6c20399efe3be6abfd6d7dc8187d886b4a0`  
		Last Modified: Tue, 29 Mar 2022 23:02:14 GMT  
		Size: 64.8 MB (64760477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:2858e2824edbcaaefd73dd8b888c39d6c10cfd27bc7b2b1b420570403b00a924
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51848447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41535ed442f086e8d8103e40ebab589e248cc742505317bfb8c17b5746bc567f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:51:36 GMT
ADD file:7ac5498e2c44686d7eb272ef7645a0a64486cf942610f6754aa4a932f5b1a4be in / 
# Tue, 29 Mar 2022 00:51:37 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 08:50:15 GMT
ENV MONO_VERSION=6.12.0.122
# Tue, 29 Mar 2022 08:50:42 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 29 Mar 2022 08:51:31 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:8f10b1b67f0119a2dd5f838a3e98ab2c412e4b51fb1e4841e2b79fd4cae86105`  
		Last Modified: Tue, 29 Mar 2022 01:06:51 GMT  
		Size: 24.9 MB (24887495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:103ccfc95d14718dd5bd47005c93225d5f82bdc075ccfc346e1b366afb616d57`  
		Last Modified: Tue, 29 Mar 2022 09:01:39 GMT  
		Size: 2.5 MB (2467692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13697b82f395905c310bf0030c74844e8f8fc5979a009c041a18de4488636164`  
		Last Modified: Tue, 29 Mar 2022 09:01:50 GMT  
		Size: 24.5 MB (24493260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:c8f9bff7726932d61ceb479135172d8ad8d953634e902d99afa4b04b35c8979c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48902684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35df12dffc423503a586d8b0c8f4b5056157ba44d8baa9a3a8ebc94f4b728f4e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 02:19:40 GMT
ADD file:8d54e000817531229c35a32eee074105c7b4d3c08b7ca56b1abdd80571687f28 in / 
# Tue, 29 Mar 2022 02:19:41 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 21:55:56 GMT
ENV MONO_VERSION=6.12.0.122
# Wed, 30 Mar 2022 21:56:22 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 30 Mar 2022 21:57:04 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:d4bf0b27c669e589de33695047d638174fc2ca819a4366d5f80d1ad6b01c0c0e`  
		Last Modified: Tue, 29 Mar 2022 02:35:26 GMT  
		Size: 22.8 MB (22753045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:756cc431341070c1f6a772929e5d5daab96f2b040732e70d3cb93b3ce98d8542`  
		Last Modified: Wed, 30 Mar 2022 22:06:01 GMT  
		Size: 2.4 MB (2366920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:419ca67b5ee0885d9bcc46429070d185a04feb680b643fc29ceda334987a6a6f`  
		Last Modified: Wed, 30 Mar 2022 22:06:18 GMT  
		Size: 23.8 MB (23782719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:0f3837c80f89d4cc61d33d11680310dd7b9170aa4a20287829db1cf4ff83169c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.9 MB (57867773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a03207fd5f3c9c31e878dec4d955581897e75177774ac4915f726360915f8e8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Apr 2022 04:29:36 GMT
ADD file:5de4397c1295f7249c93907be599d96efbd9cd25909340d245ec8d1c9770f444 in / 
# Wed, 20 Apr 2022 04:29:37 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 09:34:15 GMT
ENV MONO_VERSION=6.12.0.122
# Wed, 20 Apr 2022 09:34:25 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 20 Apr 2022 09:34:40 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:6c3e5b218d6477ff77053280968d5bdeaa5dcf16a803e917d98dd0ea8b93ac82`  
		Last Modified: Wed, 20 Apr 2022 04:36:38 GMT  
		Size: 25.9 MB (25908349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a5583d434a71d4775ae033dd3567325a5f5d01a34ff9f805631b17426570d60`  
		Last Modified: Wed, 20 Apr 2022 09:38:16 GMT  
		Size: 2.6 MB (2641065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1df7a4f3775402176b947b2ffb1f930879581b64904846f29bd8e5aa4000e4d`  
		Last Modified: Wed, 20 Apr 2022 09:38:20 GMT  
		Size: 29.3 MB (29318359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:slim` - linux; 386

```console
$ docker pull mono@sha256:a620c36d6b438c94797eaa6b17b2452369ac55ab8a59a1bcf8b4501df1eea0c5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.2 MB (99157932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95ff55aea4f3ffc1da74cea929a23a78ed6dc8901847098c5878018368c9da5d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Apr 2022 07:38:03 GMT
ADD file:602a25173054242f635a5a299845b7f1b56864ac5d3b8af1ae29dec3a9da119f in / 
# Wed, 20 Apr 2022 07:38:04 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 12:49:08 GMT
ENV MONO_VERSION=6.12.0.122
# Wed, 20 Apr 2022 12:49:17 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 20 Apr 2022 12:49:40 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a13b13d818745c4d2234aab71df26e4a01bfe59f396ab62f20d156b94803650c`  
		Last Modified: Wed, 20 Apr 2022 07:45:46 GMT  
		Size: 27.8 MB (27799825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc07624832ff4b064bd2b3797a6774618e27f4c3a1e24419874628eeb613e7ba`  
		Last Modified: Wed, 20 Apr 2022 12:53:02 GMT  
		Size: 2.8 MB (2789161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d6af1a94baa95c219eaba2db2fb27e299572ac8d2859e1399838abdccae784c`  
		Last Modified: Wed, 20 Apr 2022 12:53:11 GMT  
		Size: 68.6 MB (68568946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:slim` - linux; ppc64le

```console
$ docker pull mono@sha256:9b3a0defce0a5c2ae9bfc6d34af244911ccd407e7973e0f3eedce5fe3670f57e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60326275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5184331441c848755861d28d51bfb13f10dc8e51ace7607db24b3326be9c1166`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:59 GMT
ADD file:7271d778d432a07f57fedf8d50d83699ef545acc9db9346f6fe75b0054af4cd1 in / 
# Tue, 29 Mar 2022 00:23:00 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 06:30:50 GMT
ENV MONO_VERSION=6.12.0.122
# Wed, 30 Mar 2022 06:32:19 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 30 Mar 2022 06:33:27 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7db831386ce67ac1cf2b4f1513fe3746c9ea2b8d4c82efca75be638eaf533614`  
		Last Modified: Tue, 29 Mar 2022 00:34:41 GMT  
		Size: 30.6 MB (30560163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55feab57ab15634326c723014da448815650e9737d6c5671ca5a4cd4503905cb`  
		Last Modified: Wed, 30 Mar 2022 06:53:14 GMT  
		Size: 2.9 MB (2892687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c00a3dcf742861f8ca53669004126ef6bead547f42b4f28c1d7ba21debbc8b5`  
		Last Modified: Wed, 30 Mar 2022 06:53:20 GMT  
		Size: 26.9 MB (26873425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
