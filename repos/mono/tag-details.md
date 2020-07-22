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
$ docker pull mono@sha256:7abb3572d2875ec62570e481f69277dbf44a7f5c386b45d8b2c33cbdfb6b4a86
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
$ docker pull mono@sha256:c4118ed710f19848f2f29877a06271e11cfc3577e23c0018360a4cb347da404e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.0 MB (235018613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13d1331c323d17d5bd48ce6ff2e86f956687ec264d9d39f96bd0b6714de6272e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 02:07:07 GMT
ADD file:c11db0b135382f4c5b0f55b50740639bd8c1a22153b931b409cb9e41136734f2 in / 
# Wed, 22 Jul 2020 02:07:07 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 19:26:50 GMT
ENV MONO_VERSION=6.8.0.96
# Wed, 22 Jul 2020 19:26:59 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jul 2020 19:27:42 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 22 Jul 2020 19:40:41 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:cbd31ae332794bb723708526045b062b2fe6a08ccc0f143ea7dc18e0ebe46dea`  
		Last Modified: Wed, 22 Jul 2020 02:12:25 GMT  
		Size: 22.5 MB (22515635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fa40bfbf0082f2bae5777ccd52f3ca2add17d21a2375de40cb7b6a738aee92a`  
		Last Modified: Wed, 22 Jul 2020 20:02:10 GMT  
		Size: 244.5 KB (244495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:989dabcb56d661ce7dac9d54d0c22d40088fb13ced11ca7807786cd9cd61431d`  
		Last Modified: Wed, 22 Jul 2020 20:02:28 GMT  
		Size: 64.5 MB (64467293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11e08265401bb5017665068ac267affc91b2e11ffe852bd9b9d73572f1ebdede`  
		Last Modified: Wed, 22 Jul 2020 20:03:51 GMT  
		Size: 147.8 MB (147791190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6` - linux; arm variant v5

```console
$ docker pull mono@sha256:d216197c3136cf659053d08e0eb5d8f3961128d38d9893e9f8b19e7bddf3c51c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.6 MB (180580599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e9781e28afc6ae2bd019f175f92455997398b3d6b80688994a75f6b4acbb27f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 00:51:01 GMT
ADD file:4ea2d111c970d510f4eccf0fa08caafde1d227fc4c249d67c1b9d99998b0b906 in / 
# Wed, 22 Jul 2020 00:51:04 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 21:12:42 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 22 Jul 2020 21:13:14 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jul 2020 21:14:39 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 22 Jul 2020 21:20:33 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7ae4223cfc253e8d54407ec654ed8fb606352daea8da124f33dacd17626259ad`  
		Last Modified: Wed, 22 Jul 2020 00:58:53 GMT  
		Size: 24.8 MB (24837461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34b201b7c93f2f75a8f765155e3fd569dbc95a79c57c644b4595e1eff9afe8e9`  
		Last Modified: Wed, 22 Jul 2020 21:21:16 GMT  
		Size: 256.0 KB (255977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47783e7ea018044b2c75ce172154e65072809be55a95a291093f770a8c261e75`  
		Last Modified: Wed, 22 Jul 2020 21:21:27 GMT  
		Size: 26.5 MB (26529324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9bba9be5aff5dfd8562a172dd933fd2bddcdbfc9c5cf46797c28e7f1d276576`  
		Last Modified: Wed, 22 Jul 2020 21:23:21 GMT  
		Size: 129.0 MB (128957837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6` - linux; arm variant v7

```console
$ docker pull mono@sha256:0e79b73ff74791117dd0a42084eee5040160bdfa1d76e7e4cf2ffdd2b18b3cb9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.6 MB (172599115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a12c1996dc94982e4e9871cb355f1304e8c978c416bef75350d2fc25fb5fcad2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 01:33:30 GMT
ADD file:49b1a1b4f5c2201b0e23e29dca24c4f6ffc14620196c4bd77770952500c4bee1 in / 
# Wed, 22 Jul 2020 01:33:38 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 02:15:12 GMT
ENV MONO_VERSION=6.8.0.96
# Wed, 22 Jul 2020 02:15:59 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jul 2020 02:17:08 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 22 Jul 2020 02:24:59 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:cd38ad753522d120e27c5343b08f661ee3aebfe531d60102d7c624c16dba4d09`  
		Last Modified: Wed, 22 Jul 2020 01:44:24 GMT  
		Size: 19.3 MB (19298267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:678b77b1123ed730afaccee19cb50f8fdf077e6011636b04af9cd365e6ebdf13`  
		Last Modified: Wed, 22 Jul 2020 02:32:32 GMT  
		Size: 244.6 KB (244569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35ee2966b2ed591a8caba8af3012b33613fdcd2925dffc5f9eaa9328292c5af9`  
		Last Modified: Wed, 22 Jul 2020 02:32:40 GMT  
		Size: 24.5 MB (24495473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:156d85b212d8926604522d94038ef09d4862f7a5aebd52d8f0c5e9546ef12c06`  
		Last Modified: Wed, 22 Jul 2020 02:34:24 GMT  
		Size: 128.6 MB (128560806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:888ae4aa5ec89b8fe21ff0815140dbed997effd0932cbe5046516be559a83c90
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.6 MB (194638406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6452050a1767019963d92db7ac949255c631277d251a379db9d9ac31e4c21997`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 00:44:08 GMT
ADD file:7a721f0a6a7d3eb45184986201740dc57ec00c3d3da61af70966d87f3675d2ef in / 
# Wed, 22 Jul 2020 00:44:10 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 05:38:42 GMT
ENV MONO_VERSION=6.8.0.96
# Wed, 22 Jul 2020 05:40:12 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jul 2020 05:41:47 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 22 Jul 2020 05:48:15 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:3d187d5a7d59d9a1bf03dbd41bc2d56080ed75d089110b59508e3b246ae0e944`  
		Last Modified: Wed, 22 Jul 2020 00:50:16 GMT  
		Size: 20.4 MB (20371158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:010d54085bbf9d8fb8c9010cc33873fe9f927d1fb45a8f2cf12a0cac6b313c2e`  
		Last Modified: Wed, 22 Jul 2020 05:54:22 GMT  
		Size: 244.5 KB (244545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:387e5ec55166d1b19edc03874e2b9e69860136ecddc6a7604b9140ecd8234338`  
		Last Modified: Wed, 22 Jul 2020 05:54:32 GMT  
		Size: 29.3 MB (29310033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:515cf7fb56e986d5f139d0c4e32bdf6b2bbfb0ac59d01f5879526ce990b786fd`  
		Last Modified: Wed, 22 Jul 2020 05:56:01 GMT  
		Size: 144.7 MB (144712670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6` - linux; 386

```console
$ docker pull mono@sha256:47f8d8559a64fef3db99d26af7fa428e266f29cce84528d3b88bd4870f4b81e4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.4 MB (243399979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f780610af78a645413c9016e174b343103ba6dc312f51ac6b09bd4da66393c9d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 02:12:37 GMT
ADD file:9d59e7e41b146c16bca3047e3a0451abb508d22a91b64dfe2ce6d147381f800d in / 
# Wed, 22 Jul 2020 02:12:37 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 08:14:06 GMT
ENV MONO_VERSION=6.8.0.96
# Wed, 22 Jul 2020 08:14:20 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jul 2020 08:15:03 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 22 Jul 2020 08:20:11 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:5562cfdfc3152571ce0700e9d6816dede132432ab48c7ef147e89863eac98d4d`  
		Last Modified: Wed, 22 Jul 2020 02:19:28 GMT  
		Size: 23.1 MB (23142189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb45bd2f94e2f0fe1aba8e0d40510779b6f02ba16673b85345aac02fe6df273f`  
		Last Modified: Wed, 22 Jul 2020 08:26:18 GMT  
		Size: 244.5 KB (244513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:850d9d5c8af28167dbad00d62240efef6bf70bc2d23ae0735b14eceae8ad854c`  
		Last Modified: Wed, 22 Jul 2020 08:26:45 GMT  
		Size: 68.5 MB (68518539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52bcc6dadd8a1a4a2c311ea3bfab70c1a1cab2cea051b42df42f3aaf448a54e9`  
		Last Modified: Wed, 22 Jul 2020 08:28:56 GMT  
		Size: 151.5 MB (151494738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6` - linux; ppc64le

```console
$ docker pull mono@sha256:70c1fcea14ad2b7622978d2eb2d5626f8d5363e014b6f4974af4a4d5c15f7fac
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.9 MB (178895806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86adafe85745a7a969d3013f3ec3d1d66c603a377e21e1973c2c1eea147f78da`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:25:38 GMT
ADD file:41ec53d65aa183c2835f73989c9e4922f818e59774811eaa6e7395e5a36d5eab in / 
# Tue, 09 Jun 2020 01:25:42 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 04:37:42 GMT
ENV MONO_VERSION=6.8.0.96
# Tue, 09 Jun 2020 04:39:26 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Jun 2020 04:40:39 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 09 Jun 2020 04:51:22 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a29e28607c9b96acae7ff89e56214e4339a87c59e40a6f030fa4cbcaab753f2c`  
		Last Modified: Tue, 09 Jun 2020 01:37:25 GMT  
		Size: 22.8 MB (22791269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e1fc192a4485fb46ca92b8e704feb4d02fab0a2a37cb4238017caf8d50239d5`  
		Last Modified: Tue, 09 Jun 2020 05:05:25 GMT  
		Size: 244.7 KB (244663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc43661bb843c17c3ae2b4bc4f6d7ffbc36d936efa982c85608c72360c89b849`  
		Last Modified: Tue, 09 Jun 2020 05:05:31 GMT  
		Size: 25.7 MB (25670188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:942f4a6a782ccadbdc03b5cda25e2632ae9bf2dbd213b5dfee3b75376ad65086`  
		Last Modified: Tue, 09 Jun 2020 05:06:55 GMT  
		Size: 130.2 MB (130189686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.10`

```console
$ docker pull mono@sha256:062db8bf3dbabeb795c93d3454356c9a83378b1daf0177bec825e12f86666af4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; arm variant v5

### `mono:6.10` - linux; arm variant v5

```console
$ docker pull mono@sha256:d216197c3136cf659053d08e0eb5d8f3961128d38d9893e9f8b19e7bddf3c51c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.6 MB (180580599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e9781e28afc6ae2bd019f175f92455997398b3d6b80688994a75f6b4acbb27f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 00:51:01 GMT
ADD file:4ea2d111c970d510f4eccf0fa08caafde1d227fc4c249d67c1b9d99998b0b906 in / 
# Wed, 22 Jul 2020 00:51:04 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 21:12:42 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 22 Jul 2020 21:13:14 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jul 2020 21:14:39 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 22 Jul 2020 21:20:33 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7ae4223cfc253e8d54407ec654ed8fb606352daea8da124f33dacd17626259ad`  
		Last Modified: Wed, 22 Jul 2020 00:58:53 GMT  
		Size: 24.8 MB (24837461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34b201b7c93f2f75a8f765155e3fd569dbc95a79c57c644b4595e1eff9afe8e9`  
		Last Modified: Wed, 22 Jul 2020 21:21:16 GMT  
		Size: 256.0 KB (255977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47783e7ea018044b2c75ce172154e65072809be55a95a291093f770a8c261e75`  
		Last Modified: Wed, 22 Jul 2020 21:21:27 GMT  
		Size: 26.5 MB (26529324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9bba9be5aff5dfd8562a172dd933fd2bddcdbfc9c5cf46797c28e7f1d276576`  
		Last Modified: Wed, 22 Jul 2020 21:23:21 GMT  
		Size: 129.0 MB (128957837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.10.0`

```console
$ docker pull mono@sha256:062db8bf3dbabeb795c93d3454356c9a83378b1daf0177bec825e12f86666af4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; arm variant v5

### `mono:6.10.0` - linux; arm variant v5

```console
$ docker pull mono@sha256:d216197c3136cf659053d08e0eb5d8f3961128d38d9893e9f8b19e7bddf3c51c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.6 MB (180580599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e9781e28afc6ae2bd019f175f92455997398b3d6b80688994a75f6b4acbb27f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 00:51:01 GMT
ADD file:4ea2d111c970d510f4eccf0fa08caafde1d227fc4c249d67c1b9d99998b0b906 in / 
# Wed, 22 Jul 2020 00:51:04 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 21:12:42 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 22 Jul 2020 21:13:14 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jul 2020 21:14:39 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 22 Jul 2020 21:20:33 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7ae4223cfc253e8d54407ec654ed8fb606352daea8da124f33dacd17626259ad`  
		Last Modified: Wed, 22 Jul 2020 00:58:53 GMT  
		Size: 24.8 MB (24837461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34b201b7c93f2f75a8f765155e3fd569dbc95a79c57c644b4595e1eff9afe8e9`  
		Last Modified: Wed, 22 Jul 2020 21:21:16 GMT  
		Size: 256.0 KB (255977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47783e7ea018044b2c75ce172154e65072809be55a95a291093f770a8c261e75`  
		Last Modified: Wed, 22 Jul 2020 21:21:27 GMT  
		Size: 26.5 MB (26529324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9bba9be5aff5dfd8562a172dd933fd2bddcdbfc9c5cf46797c28e7f1d276576`  
		Last Modified: Wed, 22 Jul 2020 21:23:21 GMT  
		Size: 129.0 MB (128957837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.10.0.104`

```console
$ docker pull mono@sha256:062db8bf3dbabeb795c93d3454356c9a83378b1daf0177bec825e12f86666af4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; arm variant v5

### `mono:6.10.0.104` - linux; arm variant v5

```console
$ docker pull mono@sha256:d216197c3136cf659053d08e0eb5d8f3961128d38d9893e9f8b19e7bddf3c51c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.6 MB (180580599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e9781e28afc6ae2bd019f175f92455997398b3d6b80688994a75f6b4acbb27f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 00:51:01 GMT
ADD file:4ea2d111c970d510f4eccf0fa08caafde1d227fc4c249d67c1b9d99998b0b906 in / 
# Wed, 22 Jul 2020 00:51:04 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 21:12:42 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 22 Jul 2020 21:13:14 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jul 2020 21:14:39 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 22 Jul 2020 21:20:33 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7ae4223cfc253e8d54407ec654ed8fb606352daea8da124f33dacd17626259ad`  
		Last Modified: Wed, 22 Jul 2020 00:58:53 GMT  
		Size: 24.8 MB (24837461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34b201b7c93f2f75a8f765155e3fd569dbc95a79c57c644b4595e1eff9afe8e9`  
		Last Modified: Wed, 22 Jul 2020 21:21:16 GMT  
		Size: 256.0 KB (255977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47783e7ea018044b2c75ce172154e65072809be55a95a291093f770a8c261e75`  
		Last Modified: Wed, 22 Jul 2020 21:21:27 GMT  
		Size: 26.5 MB (26529324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9bba9be5aff5dfd8562a172dd933fd2bddcdbfc9c5cf46797c28e7f1d276576`  
		Last Modified: Wed, 22 Jul 2020 21:23:21 GMT  
		Size: 129.0 MB (128957837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.10.0.104-slim`

```console
$ docker pull mono@sha256:43e1cfc33949728da60e17cb4f5793adaca94aa80c42d438b3f7fd7d8b07467f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; arm variant v5

### `mono:6.10.0.104-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:bfbf7d0dd6ec900bd4fb046e1171472d0cc6b4bc32c10095bcc1718d0d2fb4f3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51622762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0887bb40baf7e1ebaa4491740009839e418df248c2f18e393048574e7a3283aa`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 00:51:01 GMT
ADD file:4ea2d111c970d510f4eccf0fa08caafde1d227fc4c249d67c1b9d99998b0b906 in / 
# Wed, 22 Jul 2020 00:51:04 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 21:12:42 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 22 Jul 2020 21:13:14 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jul 2020 21:14:39 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7ae4223cfc253e8d54407ec654ed8fb606352daea8da124f33dacd17626259ad`  
		Last Modified: Wed, 22 Jul 2020 00:58:53 GMT  
		Size: 24.8 MB (24837461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34b201b7c93f2f75a8f765155e3fd569dbc95a79c57c644b4595e1eff9afe8e9`  
		Last Modified: Wed, 22 Jul 2020 21:21:16 GMT  
		Size: 256.0 KB (255977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47783e7ea018044b2c75ce172154e65072809be55a95a291093f770a8c261e75`  
		Last Modified: Wed, 22 Jul 2020 21:21:27 GMT  
		Size: 26.5 MB (26529324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.10.0-slim`

```console
$ docker pull mono@sha256:43e1cfc33949728da60e17cb4f5793adaca94aa80c42d438b3f7fd7d8b07467f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; arm variant v5

### `mono:6.10.0-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:bfbf7d0dd6ec900bd4fb046e1171472d0cc6b4bc32c10095bcc1718d0d2fb4f3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51622762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0887bb40baf7e1ebaa4491740009839e418df248c2f18e393048574e7a3283aa`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 00:51:01 GMT
ADD file:4ea2d111c970d510f4eccf0fa08caafde1d227fc4c249d67c1b9d99998b0b906 in / 
# Wed, 22 Jul 2020 00:51:04 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 21:12:42 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 22 Jul 2020 21:13:14 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jul 2020 21:14:39 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7ae4223cfc253e8d54407ec654ed8fb606352daea8da124f33dacd17626259ad`  
		Last Modified: Wed, 22 Jul 2020 00:58:53 GMT  
		Size: 24.8 MB (24837461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34b201b7c93f2f75a8f765155e3fd569dbc95a79c57c644b4595e1eff9afe8e9`  
		Last Modified: Wed, 22 Jul 2020 21:21:16 GMT  
		Size: 256.0 KB (255977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47783e7ea018044b2c75ce172154e65072809be55a95a291093f770a8c261e75`  
		Last Modified: Wed, 22 Jul 2020 21:21:27 GMT  
		Size: 26.5 MB (26529324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.10-slim`

```console
$ docker pull mono@sha256:43e1cfc33949728da60e17cb4f5793adaca94aa80c42d438b3f7fd7d8b07467f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; arm variant v5

### `mono:6.10-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:bfbf7d0dd6ec900bd4fb046e1171472d0cc6b4bc32c10095bcc1718d0d2fb4f3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51622762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0887bb40baf7e1ebaa4491740009839e418df248c2f18e393048574e7a3283aa`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 00:51:01 GMT
ADD file:4ea2d111c970d510f4eccf0fa08caafde1d227fc4c249d67c1b9d99998b0b906 in / 
# Wed, 22 Jul 2020 00:51:04 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 21:12:42 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 22 Jul 2020 21:13:14 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jul 2020 21:14:39 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7ae4223cfc253e8d54407ec654ed8fb606352daea8da124f33dacd17626259ad`  
		Last Modified: Wed, 22 Jul 2020 00:58:53 GMT  
		Size: 24.8 MB (24837461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34b201b7c93f2f75a8f765155e3fd569dbc95a79c57c644b4595e1eff9afe8e9`  
		Last Modified: Wed, 22 Jul 2020 21:21:16 GMT  
		Size: 256.0 KB (255977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47783e7ea018044b2c75ce172154e65072809be55a95a291093f770a8c261e75`  
		Last Modified: Wed, 22 Jul 2020 21:21:27 GMT  
		Size: 26.5 MB (26529324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.8`

```console
$ docker pull mono@sha256:4dc46871593f8f6bb9713db1892e635dbfa7282675bee18bb07d25634ee88c53
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
$ docker pull mono@sha256:c4118ed710f19848f2f29877a06271e11cfc3577e23c0018360a4cb347da404e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.0 MB (235018613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13d1331c323d17d5bd48ce6ff2e86f956687ec264d9d39f96bd0b6714de6272e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 02:07:07 GMT
ADD file:c11db0b135382f4c5b0f55b50740639bd8c1a22153b931b409cb9e41136734f2 in / 
# Wed, 22 Jul 2020 02:07:07 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 19:26:50 GMT
ENV MONO_VERSION=6.8.0.96
# Wed, 22 Jul 2020 19:26:59 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jul 2020 19:27:42 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 22 Jul 2020 19:40:41 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:cbd31ae332794bb723708526045b062b2fe6a08ccc0f143ea7dc18e0ebe46dea`  
		Last Modified: Wed, 22 Jul 2020 02:12:25 GMT  
		Size: 22.5 MB (22515635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fa40bfbf0082f2bae5777ccd52f3ca2add17d21a2375de40cb7b6a738aee92a`  
		Last Modified: Wed, 22 Jul 2020 20:02:10 GMT  
		Size: 244.5 KB (244495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:989dabcb56d661ce7dac9d54d0c22d40088fb13ced11ca7807786cd9cd61431d`  
		Last Modified: Wed, 22 Jul 2020 20:02:28 GMT  
		Size: 64.5 MB (64467293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11e08265401bb5017665068ac267affc91b2e11ffe852bd9b9d73572f1ebdede`  
		Last Modified: Wed, 22 Jul 2020 20:03:51 GMT  
		Size: 147.8 MB (147791190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8` - linux; arm variant v5

```console
$ docker pull mono@sha256:222855f1d87c83fc2078370052f5fd4895631780e62d693aade0aeff3c769bf2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.9 MB (179916751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91f1f1ff386350118a8ce9a2c7f17dd5696cc6b55c330292451eb4d9ee1465fb`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 00:51:01 GMT
ADD file:4ea2d111c970d510f4eccf0fa08caafde1d227fc4c249d67c1b9d99998b0b906 in / 
# Wed, 22 Jul 2020 00:51:04 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 21:11:24 GMT
ENV MONO_VERSION=6.8.0.123
# Wed, 22 Jul 2020 21:11:44 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jul 2020 21:12:30 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 22 Jul 2020 21:17:46 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7ae4223cfc253e8d54407ec654ed8fb606352daea8da124f33dacd17626259ad`  
		Last Modified: Wed, 22 Jul 2020 00:58:53 GMT  
		Size: 24.8 MB (24837461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82d8c961c83915aef58530df48e050cb089a654dc4fb1a86eb474065650ef16f`  
		Last Modified: Wed, 22 Jul 2020 21:20:59 GMT  
		Size: 255.9 KB (255928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4d001b5f08f93019fc37285f1115dde2c26f6bf3c49763f303bb4f1b33ec04a`  
		Last Modified: Wed, 22 Jul 2020 21:21:08 GMT  
		Size: 26.5 MB (26538537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d77ff39a638b9bd63864c5bb7680d2b7abb8e400600f65e1b3316c3c26d9ff8a`  
		Last Modified: Wed, 22 Jul 2020 21:22:24 GMT  
		Size: 128.3 MB (128284825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8` - linux; arm variant v7

```console
$ docker pull mono@sha256:0e79b73ff74791117dd0a42084eee5040160bdfa1d76e7e4cf2ffdd2b18b3cb9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.6 MB (172599115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a12c1996dc94982e4e9871cb355f1304e8c978c416bef75350d2fc25fb5fcad2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 01:33:30 GMT
ADD file:49b1a1b4f5c2201b0e23e29dca24c4f6ffc14620196c4bd77770952500c4bee1 in / 
# Wed, 22 Jul 2020 01:33:38 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 02:15:12 GMT
ENV MONO_VERSION=6.8.0.96
# Wed, 22 Jul 2020 02:15:59 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jul 2020 02:17:08 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 22 Jul 2020 02:24:59 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:cd38ad753522d120e27c5343b08f661ee3aebfe531d60102d7c624c16dba4d09`  
		Last Modified: Wed, 22 Jul 2020 01:44:24 GMT  
		Size: 19.3 MB (19298267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:678b77b1123ed730afaccee19cb50f8fdf077e6011636b04af9cd365e6ebdf13`  
		Last Modified: Wed, 22 Jul 2020 02:32:32 GMT  
		Size: 244.6 KB (244569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35ee2966b2ed591a8caba8af3012b33613fdcd2925dffc5f9eaa9328292c5af9`  
		Last Modified: Wed, 22 Jul 2020 02:32:40 GMT  
		Size: 24.5 MB (24495473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:156d85b212d8926604522d94038ef09d4862f7a5aebd52d8f0c5e9546ef12c06`  
		Last Modified: Wed, 22 Jul 2020 02:34:24 GMT  
		Size: 128.6 MB (128560806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:888ae4aa5ec89b8fe21ff0815140dbed997effd0932cbe5046516be559a83c90
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.6 MB (194638406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6452050a1767019963d92db7ac949255c631277d251a379db9d9ac31e4c21997`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 00:44:08 GMT
ADD file:7a721f0a6a7d3eb45184986201740dc57ec00c3d3da61af70966d87f3675d2ef in / 
# Wed, 22 Jul 2020 00:44:10 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 05:38:42 GMT
ENV MONO_VERSION=6.8.0.96
# Wed, 22 Jul 2020 05:40:12 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jul 2020 05:41:47 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 22 Jul 2020 05:48:15 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:3d187d5a7d59d9a1bf03dbd41bc2d56080ed75d089110b59508e3b246ae0e944`  
		Last Modified: Wed, 22 Jul 2020 00:50:16 GMT  
		Size: 20.4 MB (20371158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:010d54085bbf9d8fb8c9010cc33873fe9f927d1fb45a8f2cf12a0cac6b313c2e`  
		Last Modified: Wed, 22 Jul 2020 05:54:22 GMT  
		Size: 244.5 KB (244545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:387e5ec55166d1b19edc03874e2b9e69860136ecddc6a7604b9140ecd8234338`  
		Last Modified: Wed, 22 Jul 2020 05:54:32 GMT  
		Size: 29.3 MB (29310033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:515cf7fb56e986d5f139d0c4e32bdf6b2bbfb0ac59d01f5879526ce990b786fd`  
		Last Modified: Wed, 22 Jul 2020 05:56:01 GMT  
		Size: 144.7 MB (144712670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8` - linux; 386

```console
$ docker pull mono@sha256:47f8d8559a64fef3db99d26af7fa428e266f29cce84528d3b88bd4870f4b81e4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.4 MB (243399979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f780610af78a645413c9016e174b343103ba6dc312f51ac6b09bd4da66393c9d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 02:12:37 GMT
ADD file:9d59e7e41b146c16bca3047e3a0451abb508d22a91b64dfe2ce6d147381f800d in / 
# Wed, 22 Jul 2020 02:12:37 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 08:14:06 GMT
ENV MONO_VERSION=6.8.0.96
# Wed, 22 Jul 2020 08:14:20 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jul 2020 08:15:03 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 22 Jul 2020 08:20:11 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:5562cfdfc3152571ce0700e9d6816dede132432ab48c7ef147e89863eac98d4d`  
		Last Modified: Wed, 22 Jul 2020 02:19:28 GMT  
		Size: 23.1 MB (23142189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb45bd2f94e2f0fe1aba8e0d40510779b6f02ba16673b85345aac02fe6df273f`  
		Last Modified: Wed, 22 Jul 2020 08:26:18 GMT  
		Size: 244.5 KB (244513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:850d9d5c8af28167dbad00d62240efef6bf70bc2d23ae0735b14eceae8ad854c`  
		Last Modified: Wed, 22 Jul 2020 08:26:45 GMT  
		Size: 68.5 MB (68518539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52bcc6dadd8a1a4a2c311ea3bfab70c1a1cab2cea051b42df42f3aaf448a54e9`  
		Last Modified: Wed, 22 Jul 2020 08:28:56 GMT  
		Size: 151.5 MB (151494738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8` - linux; ppc64le

```console
$ docker pull mono@sha256:70c1fcea14ad2b7622978d2eb2d5626f8d5363e014b6f4974af4a4d5c15f7fac
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.9 MB (178895806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86adafe85745a7a969d3013f3ec3d1d66c603a377e21e1973c2c1eea147f78da`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:25:38 GMT
ADD file:41ec53d65aa183c2835f73989c9e4922f818e59774811eaa6e7395e5a36d5eab in / 
# Tue, 09 Jun 2020 01:25:42 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 04:37:42 GMT
ENV MONO_VERSION=6.8.0.96
# Tue, 09 Jun 2020 04:39:26 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Jun 2020 04:40:39 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 09 Jun 2020 04:51:22 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a29e28607c9b96acae7ff89e56214e4339a87c59e40a6f030fa4cbcaab753f2c`  
		Last Modified: Tue, 09 Jun 2020 01:37:25 GMT  
		Size: 22.8 MB (22791269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e1fc192a4485fb46ca92b8e704feb4d02fab0a2a37cb4238017caf8d50239d5`  
		Last Modified: Tue, 09 Jun 2020 05:05:25 GMT  
		Size: 244.7 KB (244663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc43661bb843c17c3ae2b4bc4f6d7ffbc36d936efa982c85608c72360c89b849`  
		Last Modified: Tue, 09 Jun 2020 05:05:31 GMT  
		Size: 25.7 MB (25670188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:942f4a6a782ccadbdc03b5cda25e2632ae9bf2dbd213b5dfee3b75376ad65086`  
		Last Modified: Tue, 09 Jun 2020 05:06:55 GMT  
		Size: 130.2 MB (130189686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.8.0`

```console
$ docker pull mono@sha256:4dc46871593f8f6bb9713db1892e635dbfa7282675bee18bb07d25634ee88c53
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
$ docker pull mono@sha256:c4118ed710f19848f2f29877a06271e11cfc3577e23c0018360a4cb347da404e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.0 MB (235018613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13d1331c323d17d5bd48ce6ff2e86f956687ec264d9d39f96bd0b6714de6272e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 02:07:07 GMT
ADD file:c11db0b135382f4c5b0f55b50740639bd8c1a22153b931b409cb9e41136734f2 in / 
# Wed, 22 Jul 2020 02:07:07 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 19:26:50 GMT
ENV MONO_VERSION=6.8.0.96
# Wed, 22 Jul 2020 19:26:59 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jul 2020 19:27:42 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 22 Jul 2020 19:40:41 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:cbd31ae332794bb723708526045b062b2fe6a08ccc0f143ea7dc18e0ebe46dea`  
		Last Modified: Wed, 22 Jul 2020 02:12:25 GMT  
		Size: 22.5 MB (22515635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fa40bfbf0082f2bae5777ccd52f3ca2add17d21a2375de40cb7b6a738aee92a`  
		Last Modified: Wed, 22 Jul 2020 20:02:10 GMT  
		Size: 244.5 KB (244495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:989dabcb56d661ce7dac9d54d0c22d40088fb13ced11ca7807786cd9cd61431d`  
		Last Modified: Wed, 22 Jul 2020 20:02:28 GMT  
		Size: 64.5 MB (64467293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11e08265401bb5017665068ac267affc91b2e11ffe852bd9b9d73572f1ebdede`  
		Last Modified: Wed, 22 Jul 2020 20:03:51 GMT  
		Size: 147.8 MB (147791190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8.0` - linux; arm variant v5

```console
$ docker pull mono@sha256:222855f1d87c83fc2078370052f5fd4895631780e62d693aade0aeff3c769bf2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.9 MB (179916751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91f1f1ff386350118a8ce9a2c7f17dd5696cc6b55c330292451eb4d9ee1465fb`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 00:51:01 GMT
ADD file:4ea2d111c970d510f4eccf0fa08caafde1d227fc4c249d67c1b9d99998b0b906 in / 
# Wed, 22 Jul 2020 00:51:04 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 21:11:24 GMT
ENV MONO_VERSION=6.8.0.123
# Wed, 22 Jul 2020 21:11:44 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jul 2020 21:12:30 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 22 Jul 2020 21:17:46 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7ae4223cfc253e8d54407ec654ed8fb606352daea8da124f33dacd17626259ad`  
		Last Modified: Wed, 22 Jul 2020 00:58:53 GMT  
		Size: 24.8 MB (24837461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82d8c961c83915aef58530df48e050cb089a654dc4fb1a86eb474065650ef16f`  
		Last Modified: Wed, 22 Jul 2020 21:20:59 GMT  
		Size: 255.9 KB (255928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4d001b5f08f93019fc37285f1115dde2c26f6bf3c49763f303bb4f1b33ec04a`  
		Last Modified: Wed, 22 Jul 2020 21:21:08 GMT  
		Size: 26.5 MB (26538537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d77ff39a638b9bd63864c5bb7680d2b7abb8e400600f65e1b3316c3c26d9ff8a`  
		Last Modified: Wed, 22 Jul 2020 21:22:24 GMT  
		Size: 128.3 MB (128284825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8.0` - linux; arm variant v7

```console
$ docker pull mono@sha256:0e79b73ff74791117dd0a42084eee5040160bdfa1d76e7e4cf2ffdd2b18b3cb9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.6 MB (172599115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a12c1996dc94982e4e9871cb355f1304e8c978c416bef75350d2fc25fb5fcad2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 01:33:30 GMT
ADD file:49b1a1b4f5c2201b0e23e29dca24c4f6ffc14620196c4bd77770952500c4bee1 in / 
# Wed, 22 Jul 2020 01:33:38 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 02:15:12 GMT
ENV MONO_VERSION=6.8.0.96
# Wed, 22 Jul 2020 02:15:59 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jul 2020 02:17:08 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 22 Jul 2020 02:24:59 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:cd38ad753522d120e27c5343b08f661ee3aebfe531d60102d7c624c16dba4d09`  
		Last Modified: Wed, 22 Jul 2020 01:44:24 GMT  
		Size: 19.3 MB (19298267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:678b77b1123ed730afaccee19cb50f8fdf077e6011636b04af9cd365e6ebdf13`  
		Last Modified: Wed, 22 Jul 2020 02:32:32 GMT  
		Size: 244.6 KB (244569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35ee2966b2ed591a8caba8af3012b33613fdcd2925dffc5f9eaa9328292c5af9`  
		Last Modified: Wed, 22 Jul 2020 02:32:40 GMT  
		Size: 24.5 MB (24495473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:156d85b212d8926604522d94038ef09d4862f7a5aebd52d8f0c5e9546ef12c06`  
		Last Modified: Wed, 22 Jul 2020 02:34:24 GMT  
		Size: 128.6 MB (128560806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8.0` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:888ae4aa5ec89b8fe21ff0815140dbed997effd0932cbe5046516be559a83c90
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.6 MB (194638406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6452050a1767019963d92db7ac949255c631277d251a379db9d9ac31e4c21997`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 00:44:08 GMT
ADD file:7a721f0a6a7d3eb45184986201740dc57ec00c3d3da61af70966d87f3675d2ef in / 
# Wed, 22 Jul 2020 00:44:10 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 05:38:42 GMT
ENV MONO_VERSION=6.8.0.96
# Wed, 22 Jul 2020 05:40:12 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jul 2020 05:41:47 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 22 Jul 2020 05:48:15 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:3d187d5a7d59d9a1bf03dbd41bc2d56080ed75d089110b59508e3b246ae0e944`  
		Last Modified: Wed, 22 Jul 2020 00:50:16 GMT  
		Size: 20.4 MB (20371158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:010d54085bbf9d8fb8c9010cc33873fe9f927d1fb45a8f2cf12a0cac6b313c2e`  
		Last Modified: Wed, 22 Jul 2020 05:54:22 GMT  
		Size: 244.5 KB (244545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:387e5ec55166d1b19edc03874e2b9e69860136ecddc6a7604b9140ecd8234338`  
		Last Modified: Wed, 22 Jul 2020 05:54:32 GMT  
		Size: 29.3 MB (29310033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:515cf7fb56e986d5f139d0c4e32bdf6b2bbfb0ac59d01f5879526ce990b786fd`  
		Last Modified: Wed, 22 Jul 2020 05:56:01 GMT  
		Size: 144.7 MB (144712670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8.0` - linux; 386

```console
$ docker pull mono@sha256:47f8d8559a64fef3db99d26af7fa428e266f29cce84528d3b88bd4870f4b81e4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.4 MB (243399979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f780610af78a645413c9016e174b343103ba6dc312f51ac6b09bd4da66393c9d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 02:12:37 GMT
ADD file:9d59e7e41b146c16bca3047e3a0451abb508d22a91b64dfe2ce6d147381f800d in / 
# Wed, 22 Jul 2020 02:12:37 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 08:14:06 GMT
ENV MONO_VERSION=6.8.0.96
# Wed, 22 Jul 2020 08:14:20 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jul 2020 08:15:03 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 22 Jul 2020 08:20:11 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:5562cfdfc3152571ce0700e9d6816dede132432ab48c7ef147e89863eac98d4d`  
		Last Modified: Wed, 22 Jul 2020 02:19:28 GMT  
		Size: 23.1 MB (23142189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb45bd2f94e2f0fe1aba8e0d40510779b6f02ba16673b85345aac02fe6df273f`  
		Last Modified: Wed, 22 Jul 2020 08:26:18 GMT  
		Size: 244.5 KB (244513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:850d9d5c8af28167dbad00d62240efef6bf70bc2d23ae0735b14eceae8ad854c`  
		Last Modified: Wed, 22 Jul 2020 08:26:45 GMT  
		Size: 68.5 MB (68518539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52bcc6dadd8a1a4a2c311ea3bfab70c1a1cab2cea051b42df42f3aaf448a54e9`  
		Last Modified: Wed, 22 Jul 2020 08:28:56 GMT  
		Size: 151.5 MB (151494738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8.0` - linux; ppc64le

```console
$ docker pull mono@sha256:70c1fcea14ad2b7622978d2eb2d5626f8d5363e014b6f4974af4a4d5c15f7fac
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.9 MB (178895806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86adafe85745a7a969d3013f3ec3d1d66c603a377e21e1973c2c1eea147f78da`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:25:38 GMT
ADD file:41ec53d65aa183c2835f73989c9e4922f818e59774811eaa6e7395e5a36d5eab in / 
# Tue, 09 Jun 2020 01:25:42 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 04:37:42 GMT
ENV MONO_VERSION=6.8.0.96
# Tue, 09 Jun 2020 04:39:26 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Jun 2020 04:40:39 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 09 Jun 2020 04:51:22 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a29e28607c9b96acae7ff89e56214e4339a87c59e40a6f030fa4cbcaab753f2c`  
		Last Modified: Tue, 09 Jun 2020 01:37:25 GMT  
		Size: 22.8 MB (22791269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e1fc192a4485fb46ca92b8e704feb4d02fab0a2a37cb4238017caf8d50239d5`  
		Last Modified: Tue, 09 Jun 2020 05:05:25 GMT  
		Size: 244.7 KB (244663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc43661bb843c17c3ae2b4bc4f6d7ffbc36d936efa982c85608c72360c89b849`  
		Last Modified: Tue, 09 Jun 2020 05:05:31 GMT  
		Size: 25.7 MB (25670188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:942f4a6a782ccadbdc03b5cda25e2632ae9bf2dbd213b5dfee3b75376ad65086`  
		Last Modified: Tue, 09 Jun 2020 05:06:55 GMT  
		Size: 130.2 MB (130189686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.8.0.123`

```console
$ docker pull mono@sha256:db52f7e4b2ae702f9bc59dd2b9fb1cf1f3fbf836a567746188b6af718320fc17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; arm variant v5

### `mono:6.8.0.123` - linux; arm variant v5

```console
$ docker pull mono@sha256:222855f1d87c83fc2078370052f5fd4895631780e62d693aade0aeff3c769bf2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.9 MB (179916751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91f1f1ff386350118a8ce9a2c7f17dd5696cc6b55c330292451eb4d9ee1465fb`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 00:51:01 GMT
ADD file:4ea2d111c970d510f4eccf0fa08caafde1d227fc4c249d67c1b9d99998b0b906 in / 
# Wed, 22 Jul 2020 00:51:04 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 21:11:24 GMT
ENV MONO_VERSION=6.8.0.123
# Wed, 22 Jul 2020 21:11:44 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jul 2020 21:12:30 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 22 Jul 2020 21:17:46 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7ae4223cfc253e8d54407ec654ed8fb606352daea8da124f33dacd17626259ad`  
		Last Modified: Wed, 22 Jul 2020 00:58:53 GMT  
		Size: 24.8 MB (24837461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82d8c961c83915aef58530df48e050cb089a654dc4fb1a86eb474065650ef16f`  
		Last Modified: Wed, 22 Jul 2020 21:20:59 GMT  
		Size: 255.9 KB (255928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4d001b5f08f93019fc37285f1115dde2c26f6bf3c49763f303bb4f1b33ec04a`  
		Last Modified: Wed, 22 Jul 2020 21:21:08 GMT  
		Size: 26.5 MB (26538537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d77ff39a638b9bd63864c5bb7680d2b7abb8e400600f65e1b3316c3c26d9ff8a`  
		Last Modified: Wed, 22 Jul 2020 21:22:24 GMT  
		Size: 128.3 MB (128284825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.8.0.123-slim`

```console
$ docker pull mono@sha256:eb66916b1bd64cb14a7ecb58aefa7ddb19797e60255581044a6db3f3ea324088
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; arm variant v5

### `mono:6.8.0.123-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:d72c898eb547cda9a6e5857284580215f3602b27ba2234b8764a6ae1b650f86e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51631926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bc12135113cfe2a5c3ed5bdaf06aeb9429d60e66859df0814d3b5247740995e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 00:51:01 GMT
ADD file:4ea2d111c970d510f4eccf0fa08caafde1d227fc4c249d67c1b9d99998b0b906 in / 
# Wed, 22 Jul 2020 00:51:04 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 21:11:24 GMT
ENV MONO_VERSION=6.8.0.123
# Wed, 22 Jul 2020 21:11:44 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jul 2020 21:12:30 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7ae4223cfc253e8d54407ec654ed8fb606352daea8da124f33dacd17626259ad`  
		Last Modified: Wed, 22 Jul 2020 00:58:53 GMT  
		Size: 24.8 MB (24837461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82d8c961c83915aef58530df48e050cb089a654dc4fb1a86eb474065650ef16f`  
		Last Modified: Wed, 22 Jul 2020 21:20:59 GMT  
		Size: 255.9 KB (255928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4d001b5f08f93019fc37285f1115dde2c26f6bf3c49763f303bb4f1b33ec04a`  
		Last Modified: Wed, 22 Jul 2020 21:21:08 GMT  
		Size: 26.5 MB (26538537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.8.0-slim`

```console
$ docker pull mono@sha256:95c1986e0de07cecb9d4644bf33d49dcdcad70595f893cfe7c8e8d5be81737ee
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
$ docker pull mono@sha256:8662fe5f43ce6662afc770942a78620711529e22bfb3a6915d08de61f0391b0c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.2 MB (87227423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c8044236c95b15c23c907be455632697f74ca4ba4e6a5836dd26b5d9b5cbcd4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 02:07:07 GMT
ADD file:c11db0b135382f4c5b0f55b50740639bd8c1a22153b931b409cb9e41136734f2 in / 
# Wed, 22 Jul 2020 02:07:07 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 19:26:50 GMT
ENV MONO_VERSION=6.8.0.96
# Wed, 22 Jul 2020 19:26:59 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jul 2020 19:27:42 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:cbd31ae332794bb723708526045b062b2fe6a08ccc0f143ea7dc18e0ebe46dea`  
		Last Modified: Wed, 22 Jul 2020 02:12:25 GMT  
		Size: 22.5 MB (22515635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fa40bfbf0082f2bae5777ccd52f3ca2add17d21a2375de40cb7b6a738aee92a`  
		Last Modified: Wed, 22 Jul 2020 20:02:10 GMT  
		Size: 244.5 KB (244495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:989dabcb56d661ce7dac9d54d0c22d40088fb13ced11ca7807786cd9cd61431d`  
		Last Modified: Wed, 22 Jul 2020 20:02:28 GMT  
		Size: 64.5 MB (64467293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8.0-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:d72c898eb547cda9a6e5857284580215f3602b27ba2234b8764a6ae1b650f86e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51631926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bc12135113cfe2a5c3ed5bdaf06aeb9429d60e66859df0814d3b5247740995e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 00:51:01 GMT
ADD file:4ea2d111c970d510f4eccf0fa08caafde1d227fc4c249d67c1b9d99998b0b906 in / 
# Wed, 22 Jul 2020 00:51:04 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 21:11:24 GMT
ENV MONO_VERSION=6.8.0.123
# Wed, 22 Jul 2020 21:11:44 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jul 2020 21:12:30 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7ae4223cfc253e8d54407ec654ed8fb606352daea8da124f33dacd17626259ad`  
		Last Modified: Wed, 22 Jul 2020 00:58:53 GMT  
		Size: 24.8 MB (24837461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82d8c961c83915aef58530df48e050cb089a654dc4fb1a86eb474065650ef16f`  
		Last Modified: Wed, 22 Jul 2020 21:20:59 GMT  
		Size: 255.9 KB (255928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4d001b5f08f93019fc37285f1115dde2c26f6bf3c49763f303bb4f1b33ec04a`  
		Last Modified: Wed, 22 Jul 2020 21:21:08 GMT  
		Size: 26.5 MB (26538537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8.0-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:43efe3765087680c99e00ef8f63dd9f8d1ba2a569c9a8af61dc54a18d82f9cc6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.0 MB (44038309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:777fd2ade7d45508d862b53c0c85624224196846719397190648e897a2222b24`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 01:33:30 GMT
ADD file:49b1a1b4f5c2201b0e23e29dca24c4f6ffc14620196c4bd77770952500c4bee1 in / 
# Wed, 22 Jul 2020 01:33:38 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 02:15:12 GMT
ENV MONO_VERSION=6.8.0.96
# Wed, 22 Jul 2020 02:15:59 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jul 2020 02:17:08 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:cd38ad753522d120e27c5343b08f661ee3aebfe531d60102d7c624c16dba4d09`  
		Last Modified: Wed, 22 Jul 2020 01:44:24 GMT  
		Size: 19.3 MB (19298267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:678b77b1123ed730afaccee19cb50f8fdf077e6011636b04af9cd365e6ebdf13`  
		Last Modified: Wed, 22 Jul 2020 02:32:32 GMT  
		Size: 244.6 KB (244569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35ee2966b2ed591a8caba8af3012b33613fdcd2925dffc5f9eaa9328292c5af9`  
		Last Modified: Wed, 22 Jul 2020 02:32:40 GMT  
		Size: 24.5 MB (24495473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8.0-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:00acf49f28e23596d8e8fa4a26ff3874f6441274d46982dbb711f476ace6b4c5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.9 MB (49925736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff11b6d6c16ae8fedd62839a4e6cf2bdc599022d5c77b0f6917b8c0029e4a883`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 00:44:08 GMT
ADD file:7a721f0a6a7d3eb45184986201740dc57ec00c3d3da61af70966d87f3675d2ef in / 
# Wed, 22 Jul 2020 00:44:10 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 05:38:42 GMT
ENV MONO_VERSION=6.8.0.96
# Wed, 22 Jul 2020 05:40:12 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jul 2020 05:41:47 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:3d187d5a7d59d9a1bf03dbd41bc2d56080ed75d089110b59508e3b246ae0e944`  
		Last Modified: Wed, 22 Jul 2020 00:50:16 GMT  
		Size: 20.4 MB (20371158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:010d54085bbf9d8fb8c9010cc33873fe9f927d1fb45a8f2cf12a0cac6b313c2e`  
		Last Modified: Wed, 22 Jul 2020 05:54:22 GMT  
		Size: 244.5 KB (244545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:387e5ec55166d1b19edc03874e2b9e69860136ecddc6a7604b9140ecd8234338`  
		Last Modified: Wed, 22 Jul 2020 05:54:32 GMT  
		Size: 29.3 MB (29310033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8.0-slim` - linux; 386

```console
$ docker pull mono@sha256:aa9bd9bf67b98aa34b06359dfe70fe3814af371907798d119a8462588cd65082
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.9 MB (91905241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8fca40a8702c7daddc16b743a8debdf7ff39e7886317d2f9c9c786ad5ec816e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 02:12:37 GMT
ADD file:9d59e7e41b146c16bca3047e3a0451abb508d22a91b64dfe2ce6d147381f800d in / 
# Wed, 22 Jul 2020 02:12:37 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 08:14:06 GMT
ENV MONO_VERSION=6.8.0.96
# Wed, 22 Jul 2020 08:14:20 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jul 2020 08:15:03 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:5562cfdfc3152571ce0700e9d6816dede132432ab48c7ef147e89863eac98d4d`  
		Last Modified: Wed, 22 Jul 2020 02:19:28 GMT  
		Size: 23.1 MB (23142189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb45bd2f94e2f0fe1aba8e0d40510779b6f02ba16673b85345aac02fe6df273f`  
		Last Modified: Wed, 22 Jul 2020 08:26:18 GMT  
		Size: 244.5 KB (244513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:850d9d5c8af28167dbad00d62240efef6bf70bc2d23ae0735b14eceae8ad854c`  
		Last Modified: Wed, 22 Jul 2020 08:26:45 GMT  
		Size: 68.5 MB (68518539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8.0-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:2c4949379a4b86afc1273f4a7339ff7bc658bc7749205fb8df632bfb7a7f1d63
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48706120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17986d4009e9231ade165cd631103027df60340b2b4b6fa078cdb34805a602ba`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:25:38 GMT
ADD file:41ec53d65aa183c2835f73989c9e4922f818e59774811eaa6e7395e5a36d5eab in / 
# Tue, 09 Jun 2020 01:25:42 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 04:37:42 GMT
ENV MONO_VERSION=6.8.0.96
# Tue, 09 Jun 2020 04:39:26 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Jun 2020 04:40:39 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a29e28607c9b96acae7ff89e56214e4339a87c59e40a6f030fa4cbcaab753f2c`  
		Last Modified: Tue, 09 Jun 2020 01:37:25 GMT  
		Size: 22.8 MB (22791269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e1fc192a4485fb46ca92b8e704feb4d02fab0a2a37cb4238017caf8d50239d5`  
		Last Modified: Tue, 09 Jun 2020 05:05:25 GMT  
		Size: 244.7 KB (244663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc43661bb843c17c3ae2b4bc4f6d7ffbc36d936efa982c85608c72360c89b849`  
		Last Modified: Tue, 09 Jun 2020 05:05:31 GMT  
		Size: 25.7 MB (25670188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.8-slim`

```console
$ docker pull mono@sha256:95c1986e0de07cecb9d4644bf33d49dcdcad70595f893cfe7c8e8d5be81737ee
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
$ docker pull mono@sha256:8662fe5f43ce6662afc770942a78620711529e22bfb3a6915d08de61f0391b0c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.2 MB (87227423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c8044236c95b15c23c907be455632697f74ca4ba4e6a5836dd26b5d9b5cbcd4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 02:07:07 GMT
ADD file:c11db0b135382f4c5b0f55b50740639bd8c1a22153b931b409cb9e41136734f2 in / 
# Wed, 22 Jul 2020 02:07:07 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 19:26:50 GMT
ENV MONO_VERSION=6.8.0.96
# Wed, 22 Jul 2020 19:26:59 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jul 2020 19:27:42 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:cbd31ae332794bb723708526045b062b2fe6a08ccc0f143ea7dc18e0ebe46dea`  
		Last Modified: Wed, 22 Jul 2020 02:12:25 GMT  
		Size: 22.5 MB (22515635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fa40bfbf0082f2bae5777ccd52f3ca2add17d21a2375de40cb7b6a738aee92a`  
		Last Modified: Wed, 22 Jul 2020 20:02:10 GMT  
		Size: 244.5 KB (244495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:989dabcb56d661ce7dac9d54d0c22d40088fb13ced11ca7807786cd9cd61431d`  
		Last Modified: Wed, 22 Jul 2020 20:02:28 GMT  
		Size: 64.5 MB (64467293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:d72c898eb547cda9a6e5857284580215f3602b27ba2234b8764a6ae1b650f86e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51631926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bc12135113cfe2a5c3ed5bdaf06aeb9429d60e66859df0814d3b5247740995e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 00:51:01 GMT
ADD file:4ea2d111c970d510f4eccf0fa08caafde1d227fc4c249d67c1b9d99998b0b906 in / 
# Wed, 22 Jul 2020 00:51:04 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 21:11:24 GMT
ENV MONO_VERSION=6.8.0.123
# Wed, 22 Jul 2020 21:11:44 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jul 2020 21:12:30 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7ae4223cfc253e8d54407ec654ed8fb606352daea8da124f33dacd17626259ad`  
		Last Modified: Wed, 22 Jul 2020 00:58:53 GMT  
		Size: 24.8 MB (24837461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82d8c961c83915aef58530df48e050cb089a654dc4fb1a86eb474065650ef16f`  
		Last Modified: Wed, 22 Jul 2020 21:20:59 GMT  
		Size: 255.9 KB (255928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4d001b5f08f93019fc37285f1115dde2c26f6bf3c49763f303bb4f1b33ec04a`  
		Last Modified: Wed, 22 Jul 2020 21:21:08 GMT  
		Size: 26.5 MB (26538537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:43efe3765087680c99e00ef8f63dd9f8d1ba2a569c9a8af61dc54a18d82f9cc6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.0 MB (44038309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:777fd2ade7d45508d862b53c0c85624224196846719397190648e897a2222b24`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 01:33:30 GMT
ADD file:49b1a1b4f5c2201b0e23e29dca24c4f6ffc14620196c4bd77770952500c4bee1 in / 
# Wed, 22 Jul 2020 01:33:38 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 02:15:12 GMT
ENV MONO_VERSION=6.8.0.96
# Wed, 22 Jul 2020 02:15:59 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jul 2020 02:17:08 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:cd38ad753522d120e27c5343b08f661ee3aebfe531d60102d7c624c16dba4d09`  
		Last Modified: Wed, 22 Jul 2020 01:44:24 GMT  
		Size: 19.3 MB (19298267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:678b77b1123ed730afaccee19cb50f8fdf077e6011636b04af9cd365e6ebdf13`  
		Last Modified: Wed, 22 Jul 2020 02:32:32 GMT  
		Size: 244.6 KB (244569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35ee2966b2ed591a8caba8af3012b33613fdcd2925dffc5f9eaa9328292c5af9`  
		Last Modified: Wed, 22 Jul 2020 02:32:40 GMT  
		Size: 24.5 MB (24495473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:00acf49f28e23596d8e8fa4a26ff3874f6441274d46982dbb711f476ace6b4c5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.9 MB (49925736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff11b6d6c16ae8fedd62839a4e6cf2bdc599022d5c77b0f6917b8c0029e4a883`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 00:44:08 GMT
ADD file:7a721f0a6a7d3eb45184986201740dc57ec00c3d3da61af70966d87f3675d2ef in / 
# Wed, 22 Jul 2020 00:44:10 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 05:38:42 GMT
ENV MONO_VERSION=6.8.0.96
# Wed, 22 Jul 2020 05:40:12 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jul 2020 05:41:47 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:3d187d5a7d59d9a1bf03dbd41bc2d56080ed75d089110b59508e3b246ae0e944`  
		Last Modified: Wed, 22 Jul 2020 00:50:16 GMT  
		Size: 20.4 MB (20371158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:010d54085bbf9d8fb8c9010cc33873fe9f927d1fb45a8f2cf12a0cac6b313c2e`  
		Last Modified: Wed, 22 Jul 2020 05:54:22 GMT  
		Size: 244.5 KB (244545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:387e5ec55166d1b19edc03874e2b9e69860136ecddc6a7604b9140ecd8234338`  
		Last Modified: Wed, 22 Jul 2020 05:54:32 GMT  
		Size: 29.3 MB (29310033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8-slim` - linux; 386

```console
$ docker pull mono@sha256:aa9bd9bf67b98aa34b06359dfe70fe3814af371907798d119a8462588cd65082
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.9 MB (91905241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8fca40a8702c7daddc16b743a8debdf7ff39e7886317d2f9c9c786ad5ec816e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 02:12:37 GMT
ADD file:9d59e7e41b146c16bca3047e3a0451abb508d22a91b64dfe2ce6d147381f800d in / 
# Wed, 22 Jul 2020 02:12:37 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 08:14:06 GMT
ENV MONO_VERSION=6.8.0.96
# Wed, 22 Jul 2020 08:14:20 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jul 2020 08:15:03 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:5562cfdfc3152571ce0700e9d6816dede132432ab48c7ef147e89863eac98d4d`  
		Last Modified: Wed, 22 Jul 2020 02:19:28 GMT  
		Size: 23.1 MB (23142189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb45bd2f94e2f0fe1aba8e0d40510779b6f02ba16673b85345aac02fe6df273f`  
		Last Modified: Wed, 22 Jul 2020 08:26:18 GMT  
		Size: 244.5 KB (244513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:850d9d5c8af28167dbad00d62240efef6bf70bc2d23ae0735b14eceae8ad854c`  
		Last Modified: Wed, 22 Jul 2020 08:26:45 GMT  
		Size: 68.5 MB (68518539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:2c4949379a4b86afc1273f4a7339ff7bc658bc7749205fb8df632bfb7a7f1d63
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48706120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17986d4009e9231ade165cd631103027df60340b2b4b6fa078cdb34805a602ba`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:25:38 GMT
ADD file:41ec53d65aa183c2835f73989c9e4922f818e59774811eaa6e7395e5a36d5eab in / 
# Tue, 09 Jun 2020 01:25:42 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 04:37:42 GMT
ENV MONO_VERSION=6.8.0.96
# Tue, 09 Jun 2020 04:39:26 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Jun 2020 04:40:39 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a29e28607c9b96acae7ff89e56214e4339a87c59e40a6f030fa4cbcaab753f2c`  
		Last Modified: Tue, 09 Jun 2020 01:37:25 GMT  
		Size: 22.8 MB (22791269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e1fc192a4485fb46ca92b8e704feb4d02fab0a2a37cb4238017caf8d50239d5`  
		Last Modified: Tue, 09 Jun 2020 05:05:25 GMT  
		Size: 244.7 KB (244663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc43661bb843c17c3ae2b4bc4f6d7ffbc36d936efa982c85608c72360c89b849`  
		Last Modified: Tue, 09 Jun 2020 05:05:31 GMT  
		Size: 25.7 MB (25670188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6-slim`

```console
$ docker pull mono@sha256:c5e8207614454e092eb1208baa21230c2fb40ccb06358d190b2edd2fb39ddb59
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
$ docker pull mono@sha256:8662fe5f43ce6662afc770942a78620711529e22bfb3a6915d08de61f0391b0c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.2 MB (87227423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c8044236c95b15c23c907be455632697f74ca4ba4e6a5836dd26b5d9b5cbcd4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 02:07:07 GMT
ADD file:c11db0b135382f4c5b0f55b50740639bd8c1a22153b931b409cb9e41136734f2 in / 
# Wed, 22 Jul 2020 02:07:07 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 19:26:50 GMT
ENV MONO_VERSION=6.8.0.96
# Wed, 22 Jul 2020 19:26:59 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jul 2020 19:27:42 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:cbd31ae332794bb723708526045b062b2fe6a08ccc0f143ea7dc18e0ebe46dea`  
		Last Modified: Wed, 22 Jul 2020 02:12:25 GMT  
		Size: 22.5 MB (22515635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fa40bfbf0082f2bae5777ccd52f3ca2add17d21a2375de40cb7b6a738aee92a`  
		Last Modified: Wed, 22 Jul 2020 20:02:10 GMT  
		Size: 244.5 KB (244495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:989dabcb56d661ce7dac9d54d0c22d40088fb13ced11ca7807786cd9cd61431d`  
		Last Modified: Wed, 22 Jul 2020 20:02:28 GMT  
		Size: 64.5 MB (64467293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:bfbf7d0dd6ec900bd4fb046e1171472d0cc6b4bc32c10095bcc1718d0d2fb4f3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51622762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0887bb40baf7e1ebaa4491740009839e418df248c2f18e393048574e7a3283aa`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 00:51:01 GMT
ADD file:4ea2d111c970d510f4eccf0fa08caafde1d227fc4c249d67c1b9d99998b0b906 in / 
# Wed, 22 Jul 2020 00:51:04 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 21:12:42 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 22 Jul 2020 21:13:14 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jul 2020 21:14:39 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7ae4223cfc253e8d54407ec654ed8fb606352daea8da124f33dacd17626259ad`  
		Last Modified: Wed, 22 Jul 2020 00:58:53 GMT  
		Size: 24.8 MB (24837461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34b201b7c93f2f75a8f765155e3fd569dbc95a79c57c644b4595e1eff9afe8e9`  
		Last Modified: Wed, 22 Jul 2020 21:21:16 GMT  
		Size: 256.0 KB (255977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47783e7ea018044b2c75ce172154e65072809be55a95a291093f770a8c261e75`  
		Last Modified: Wed, 22 Jul 2020 21:21:27 GMT  
		Size: 26.5 MB (26529324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:43efe3765087680c99e00ef8f63dd9f8d1ba2a569c9a8af61dc54a18d82f9cc6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.0 MB (44038309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:777fd2ade7d45508d862b53c0c85624224196846719397190648e897a2222b24`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 01:33:30 GMT
ADD file:49b1a1b4f5c2201b0e23e29dca24c4f6ffc14620196c4bd77770952500c4bee1 in / 
# Wed, 22 Jul 2020 01:33:38 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 02:15:12 GMT
ENV MONO_VERSION=6.8.0.96
# Wed, 22 Jul 2020 02:15:59 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jul 2020 02:17:08 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:cd38ad753522d120e27c5343b08f661ee3aebfe531d60102d7c624c16dba4d09`  
		Last Modified: Wed, 22 Jul 2020 01:44:24 GMT  
		Size: 19.3 MB (19298267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:678b77b1123ed730afaccee19cb50f8fdf077e6011636b04af9cd365e6ebdf13`  
		Last Modified: Wed, 22 Jul 2020 02:32:32 GMT  
		Size: 244.6 KB (244569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35ee2966b2ed591a8caba8af3012b33613fdcd2925dffc5f9eaa9328292c5af9`  
		Last Modified: Wed, 22 Jul 2020 02:32:40 GMT  
		Size: 24.5 MB (24495473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:00acf49f28e23596d8e8fa4a26ff3874f6441274d46982dbb711f476ace6b4c5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.9 MB (49925736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff11b6d6c16ae8fedd62839a4e6cf2bdc599022d5c77b0f6917b8c0029e4a883`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 00:44:08 GMT
ADD file:7a721f0a6a7d3eb45184986201740dc57ec00c3d3da61af70966d87f3675d2ef in / 
# Wed, 22 Jul 2020 00:44:10 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 05:38:42 GMT
ENV MONO_VERSION=6.8.0.96
# Wed, 22 Jul 2020 05:40:12 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jul 2020 05:41:47 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:3d187d5a7d59d9a1bf03dbd41bc2d56080ed75d089110b59508e3b246ae0e944`  
		Last Modified: Wed, 22 Jul 2020 00:50:16 GMT  
		Size: 20.4 MB (20371158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:010d54085bbf9d8fb8c9010cc33873fe9f927d1fb45a8f2cf12a0cac6b313c2e`  
		Last Modified: Wed, 22 Jul 2020 05:54:22 GMT  
		Size: 244.5 KB (244545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:387e5ec55166d1b19edc03874e2b9e69860136ecddc6a7604b9140ecd8234338`  
		Last Modified: Wed, 22 Jul 2020 05:54:32 GMT  
		Size: 29.3 MB (29310033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6-slim` - linux; 386

```console
$ docker pull mono@sha256:aa9bd9bf67b98aa34b06359dfe70fe3814af371907798d119a8462588cd65082
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.9 MB (91905241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8fca40a8702c7daddc16b743a8debdf7ff39e7886317d2f9c9c786ad5ec816e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 02:12:37 GMT
ADD file:9d59e7e41b146c16bca3047e3a0451abb508d22a91b64dfe2ce6d147381f800d in / 
# Wed, 22 Jul 2020 02:12:37 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 08:14:06 GMT
ENV MONO_VERSION=6.8.0.96
# Wed, 22 Jul 2020 08:14:20 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jul 2020 08:15:03 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:5562cfdfc3152571ce0700e9d6816dede132432ab48c7ef147e89863eac98d4d`  
		Last Modified: Wed, 22 Jul 2020 02:19:28 GMT  
		Size: 23.1 MB (23142189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb45bd2f94e2f0fe1aba8e0d40510779b6f02ba16673b85345aac02fe6df273f`  
		Last Modified: Wed, 22 Jul 2020 08:26:18 GMT  
		Size: 244.5 KB (244513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:850d9d5c8af28167dbad00d62240efef6bf70bc2d23ae0735b14eceae8ad854c`  
		Last Modified: Wed, 22 Jul 2020 08:26:45 GMT  
		Size: 68.5 MB (68518539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:2c4949379a4b86afc1273f4a7339ff7bc658bc7749205fb8df632bfb7a7f1d63
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48706120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17986d4009e9231ade165cd631103027df60340b2b4b6fa078cdb34805a602ba`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:25:38 GMT
ADD file:41ec53d65aa183c2835f73989c9e4922f818e59774811eaa6e7395e5a36d5eab in / 
# Tue, 09 Jun 2020 01:25:42 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 04:37:42 GMT
ENV MONO_VERSION=6.8.0.96
# Tue, 09 Jun 2020 04:39:26 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Jun 2020 04:40:39 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a29e28607c9b96acae7ff89e56214e4339a87c59e40a6f030fa4cbcaab753f2c`  
		Last Modified: Tue, 09 Jun 2020 01:37:25 GMT  
		Size: 22.8 MB (22791269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e1fc192a4485fb46ca92b8e704feb4d02fab0a2a37cb4238017caf8d50239d5`  
		Last Modified: Tue, 09 Jun 2020 05:05:25 GMT  
		Size: 244.7 KB (244663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc43661bb843c17c3ae2b4bc4f6d7ffbc36d936efa982c85608c72360c89b849`  
		Last Modified: Tue, 09 Jun 2020 05:05:31 GMT  
		Size: 25.7 MB (25670188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:latest`

```console
$ docker pull mono@sha256:7abb3572d2875ec62570e481f69277dbf44a7f5c386b45d8b2c33cbdfb6b4a86
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
$ docker pull mono@sha256:c4118ed710f19848f2f29877a06271e11cfc3577e23c0018360a4cb347da404e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.0 MB (235018613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13d1331c323d17d5bd48ce6ff2e86f956687ec264d9d39f96bd0b6714de6272e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 02:07:07 GMT
ADD file:c11db0b135382f4c5b0f55b50740639bd8c1a22153b931b409cb9e41136734f2 in / 
# Wed, 22 Jul 2020 02:07:07 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 19:26:50 GMT
ENV MONO_VERSION=6.8.0.96
# Wed, 22 Jul 2020 19:26:59 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jul 2020 19:27:42 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 22 Jul 2020 19:40:41 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:cbd31ae332794bb723708526045b062b2fe6a08ccc0f143ea7dc18e0ebe46dea`  
		Last Modified: Wed, 22 Jul 2020 02:12:25 GMT  
		Size: 22.5 MB (22515635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fa40bfbf0082f2bae5777ccd52f3ca2add17d21a2375de40cb7b6a738aee92a`  
		Last Modified: Wed, 22 Jul 2020 20:02:10 GMT  
		Size: 244.5 KB (244495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:989dabcb56d661ce7dac9d54d0c22d40088fb13ced11ca7807786cd9cd61431d`  
		Last Modified: Wed, 22 Jul 2020 20:02:28 GMT  
		Size: 64.5 MB (64467293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11e08265401bb5017665068ac267affc91b2e11ffe852bd9b9d73572f1ebdede`  
		Last Modified: Wed, 22 Jul 2020 20:03:51 GMT  
		Size: 147.8 MB (147791190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:latest` - linux; arm variant v5

```console
$ docker pull mono@sha256:d216197c3136cf659053d08e0eb5d8f3961128d38d9893e9f8b19e7bddf3c51c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.6 MB (180580599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e9781e28afc6ae2bd019f175f92455997398b3d6b80688994a75f6b4acbb27f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 00:51:01 GMT
ADD file:4ea2d111c970d510f4eccf0fa08caafde1d227fc4c249d67c1b9d99998b0b906 in / 
# Wed, 22 Jul 2020 00:51:04 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 21:12:42 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 22 Jul 2020 21:13:14 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jul 2020 21:14:39 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 22 Jul 2020 21:20:33 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7ae4223cfc253e8d54407ec654ed8fb606352daea8da124f33dacd17626259ad`  
		Last Modified: Wed, 22 Jul 2020 00:58:53 GMT  
		Size: 24.8 MB (24837461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34b201b7c93f2f75a8f765155e3fd569dbc95a79c57c644b4595e1eff9afe8e9`  
		Last Modified: Wed, 22 Jul 2020 21:21:16 GMT  
		Size: 256.0 KB (255977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47783e7ea018044b2c75ce172154e65072809be55a95a291093f770a8c261e75`  
		Last Modified: Wed, 22 Jul 2020 21:21:27 GMT  
		Size: 26.5 MB (26529324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9bba9be5aff5dfd8562a172dd933fd2bddcdbfc9c5cf46797c28e7f1d276576`  
		Last Modified: Wed, 22 Jul 2020 21:23:21 GMT  
		Size: 129.0 MB (128957837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:latest` - linux; arm variant v7

```console
$ docker pull mono@sha256:0e79b73ff74791117dd0a42084eee5040160bdfa1d76e7e4cf2ffdd2b18b3cb9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.6 MB (172599115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a12c1996dc94982e4e9871cb355f1304e8c978c416bef75350d2fc25fb5fcad2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 01:33:30 GMT
ADD file:49b1a1b4f5c2201b0e23e29dca24c4f6ffc14620196c4bd77770952500c4bee1 in / 
# Wed, 22 Jul 2020 01:33:38 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 02:15:12 GMT
ENV MONO_VERSION=6.8.0.96
# Wed, 22 Jul 2020 02:15:59 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jul 2020 02:17:08 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 22 Jul 2020 02:24:59 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:cd38ad753522d120e27c5343b08f661ee3aebfe531d60102d7c624c16dba4d09`  
		Last Modified: Wed, 22 Jul 2020 01:44:24 GMT  
		Size: 19.3 MB (19298267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:678b77b1123ed730afaccee19cb50f8fdf077e6011636b04af9cd365e6ebdf13`  
		Last Modified: Wed, 22 Jul 2020 02:32:32 GMT  
		Size: 244.6 KB (244569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35ee2966b2ed591a8caba8af3012b33613fdcd2925dffc5f9eaa9328292c5af9`  
		Last Modified: Wed, 22 Jul 2020 02:32:40 GMT  
		Size: 24.5 MB (24495473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:156d85b212d8926604522d94038ef09d4862f7a5aebd52d8f0c5e9546ef12c06`  
		Last Modified: Wed, 22 Jul 2020 02:34:24 GMT  
		Size: 128.6 MB (128560806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:latest` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:888ae4aa5ec89b8fe21ff0815140dbed997effd0932cbe5046516be559a83c90
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.6 MB (194638406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6452050a1767019963d92db7ac949255c631277d251a379db9d9ac31e4c21997`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 00:44:08 GMT
ADD file:7a721f0a6a7d3eb45184986201740dc57ec00c3d3da61af70966d87f3675d2ef in / 
# Wed, 22 Jul 2020 00:44:10 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 05:38:42 GMT
ENV MONO_VERSION=6.8.0.96
# Wed, 22 Jul 2020 05:40:12 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jul 2020 05:41:47 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 22 Jul 2020 05:48:15 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:3d187d5a7d59d9a1bf03dbd41bc2d56080ed75d089110b59508e3b246ae0e944`  
		Last Modified: Wed, 22 Jul 2020 00:50:16 GMT  
		Size: 20.4 MB (20371158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:010d54085bbf9d8fb8c9010cc33873fe9f927d1fb45a8f2cf12a0cac6b313c2e`  
		Last Modified: Wed, 22 Jul 2020 05:54:22 GMT  
		Size: 244.5 KB (244545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:387e5ec55166d1b19edc03874e2b9e69860136ecddc6a7604b9140ecd8234338`  
		Last Modified: Wed, 22 Jul 2020 05:54:32 GMT  
		Size: 29.3 MB (29310033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:515cf7fb56e986d5f139d0c4e32bdf6b2bbfb0ac59d01f5879526ce990b786fd`  
		Last Modified: Wed, 22 Jul 2020 05:56:01 GMT  
		Size: 144.7 MB (144712670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:latest` - linux; 386

```console
$ docker pull mono@sha256:47f8d8559a64fef3db99d26af7fa428e266f29cce84528d3b88bd4870f4b81e4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.4 MB (243399979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f780610af78a645413c9016e174b343103ba6dc312f51ac6b09bd4da66393c9d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 02:12:37 GMT
ADD file:9d59e7e41b146c16bca3047e3a0451abb508d22a91b64dfe2ce6d147381f800d in / 
# Wed, 22 Jul 2020 02:12:37 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 08:14:06 GMT
ENV MONO_VERSION=6.8.0.96
# Wed, 22 Jul 2020 08:14:20 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jul 2020 08:15:03 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 22 Jul 2020 08:20:11 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:5562cfdfc3152571ce0700e9d6816dede132432ab48c7ef147e89863eac98d4d`  
		Last Modified: Wed, 22 Jul 2020 02:19:28 GMT  
		Size: 23.1 MB (23142189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb45bd2f94e2f0fe1aba8e0d40510779b6f02ba16673b85345aac02fe6df273f`  
		Last Modified: Wed, 22 Jul 2020 08:26:18 GMT  
		Size: 244.5 KB (244513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:850d9d5c8af28167dbad00d62240efef6bf70bc2d23ae0735b14eceae8ad854c`  
		Last Modified: Wed, 22 Jul 2020 08:26:45 GMT  
		Size: 68.5 MB (68518539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52bcc6dadd8a1a4a2c311ea3bfab70c1a1cab2cea051b42df42f3aaf448a54e9`  
		Last Modified: Wed, 22 Jul 2020 08:28:56 GMT  
		Size: 151.5 MB (151494738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:latest` - linux; ppc64le

```console
$ docker pull mono@sha256:70c1fcea14ad2b7622978d2eb2d5626f8d5363e014b6f4974af4a4d5c15f7fac
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.9 MB (178895806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86adafe85745a7a969d3013f3ec3d1d66c603a377e21e1973c2c1eea147f78da`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:25:38 GMT
ADD file:41ec53d65aa183c2835f73989c9e4922f818e59774811eaa6e7395e5a36d5eab in / 
# Tue, 09 Jun 2020 01:25:42 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 04:37:42 GMT
ENV MONO_VERSION=6.8.0.96
# Tue, 09 Jun 2020 04:39:26 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Jun 2020 04:40:39 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 09 Jun 2020 04:51:22 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a29e28607c9b96acae7ff89e56214e4339a87c59e40a6f030fa4cbcaab753f2c`  
		Last Modified: Tue, 09 Jun 2020 01:37:25 GMT  
		Size: 22.8 MB (22791269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e1fc192a4485fb46ca92b8e704feb4d02fab0a2a37cb4238017caf8d50239d5`  
		Last Modified: Tue, 09 Jun 2020 05:05:25 GMT  
		Size: 244.7 KB (244663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc43661bb843c17c3ae2b4bc4f6d7ffbc36d936efa982c85608c72360c89b849`  
		Last Modified: Tue, 09 Jun 2020 05:05:31 GMT  
		Size: 25.7 MB (25670188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:942f4a6a782ccadbdc03b5cda25e2632ae9bf2dbd213b5dfee3b75376ad65086`  
		Last Modified: Tue, 09 Jun 2020 05:06:55 GMT  
		Size: 130.2 MB (130189686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:slim`

```console
$ docker pull mono@sha256:c5e8207614454e092eb1208baa21230c2fb40ccb06358d190b2edd2fb39ddb59
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
$ docker pull mono@sha256:8662fe5f43ce6662afc770942a78620711529e22bfb3a6915d08de61f0391b0c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.2 MB (87227423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c8044236c95b15c23c907be455632697f74ca4ba4e6a5836dd26b5d9b5cbcd4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 02:07:07 GMT
ADD file:c11db0b135382f4c5b0f55b50740639bd8c1a22153b931b409cb9e41136734f2 in / 
# Wed, 22 Jul 2020 02:07:07 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 19:26:50 GMT
ENV MONO_VERSION=6.8.0.96
# Wed, 22 Jul 2020 19:26:59 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jul 2020 19:27:42 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:cbd31ae332794bb723708526045b062b2fe6a08ccc0f143ea7dc18e0ebe46dea`  
		Last Modified: Wed, 22 Jul 2020 02:12:25 GMT  
		Size: 22.5 MB (22515635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fa40bfbf0082f2bae5777ccd52f3ca2add17d21a2375de40cb7b6a738aee92a`  
		Last Modified: Wed, 22 Jul 2020 20:02:10 GMT  
		Size: 244.5 KB (244495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:989dabcb56d661ce7dac9d54d0c22d40088fb13ced11ca7807786cd9cd61431d`  
		Last Modified: Wed, 22 Jul 2020 20:02:28 GMT  
		Size: 64.5 MB (64467293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:bfbf7d0dd6ec900bd4fb046e1171472d0cc6b4bc32c10095bcc1718d0d2fb4f3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51622762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0887bb40baf7e1ebaa4491740009839e418df248c2f18e393048574e7a3283aa`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 00:51:01 GMT
ADD file:4ea2d111c970d510f4eccf0fa08caafde1d227fc4c249d67c1b9d99998b0b906 in / 
# Wed, 22 Jul 2020 00:51:04 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 21:12:42 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 22 Jul 2020 21:13:14 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jul 2020 21:14:39 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7ae4223cfc253e8d54407ec654ed8fb606352daea8da124f33dacd17626259ad`  
		Last Modified: Wed, 22 Jul 2020 00:58:53 GMT  
		Size: 24.8 MB (24837461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34b201b7c93f2f75a8f765155e3fd569dbc95a79c57c644b4595e1eff9afe8e9`  
		Last Modified: Wed, 22 Jul 2020 21:21:16 GMT  
		Size: 256.0 KB (255977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47783e7ea018044b2c75ce172154e65072809be55a95a291093f770a8c261e75`  
		Last Modified: Wed, 22 Jul 2020 21:21:27 GMT  
		Size: 26.5 MB (26529324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:43efe3765087680c99e00ef8f63dd9f8d1ba2a569c9a8af61dc54a18d82f9cc6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.0 MB (44038309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:777fd2ade7d45508d862b53c0c85624224196846719397190648e897a2222b24`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 01:33:30 GMT
ADD file:49b1a1b4f5c2201b0e23e29dca24c4f6ffc14620196c4bd77770952500c4bee1 in / 
# Wed, 22 Jul 2020 01:33:38 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 02:15:12 GMT
ENV MONO_VERSION=6.8.0.96
# Wed, 22 Jul 2020 02:15:59 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jul 2020 02:17:08 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:cd38ad753522d120e27c5343b08f661ee3aebfe531d60102d7c624c16dba4d09`  
		Last Modified: Wed, 22 Jul 2020 01:44:24 GMT  
		Size: 19.3 MB (19298267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:678b77b1123ed730afaccee19cb50f8fdf077e6011636b04af9cd365e6ebdf13`  
		Last Modified: Wed, 22 Jul 2020 02:32:32 GMT  
		Size: 244.6 KB (244569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35ee2966b2ed591a8caba8af3012b33613fdcd2925dffc5f9eaa9328292c5af9`  
		Last Modified: Wed, 22 Jul 2020 02:32:40 GMT  
		Size: 24.5 MB (24495473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:00acf49f28e23596d8e8fa4a26ff3874f6441274d46982dbb711f476ace6b4c5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.9 MB (49925736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff11b6d6c16ae8fedd62839a4e6cf2bdc599022d5c77b0f6917b8c0029e4a883`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 00:44:08 GMT
ADD file:7a721f0a6a7d3eb45184986201740dc57ec00c3d3da61af70966d87f3675d2ef in / 
# Wed, 22 Jul 2020 00:44:10 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 05:38:42 GMT
ENV MONO_VERSION=6.8.0.96
# Wed, 22 Jul 2020 05:40:12 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jul 2020 05:41:47 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:3d187d5a7d59d9a1bf03dbd41bc2d56080ed75d089110b59508e3b246ae0e944`  
		Last Modified: Wed, 22 Jul 2020 00:50:16 GMT  
		Size: 20.4 MB (20371158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:010d54085bbf9d8fb8c9010cc33873fe9f927d1fb45a8f2cf12a0cac6b313c2e`  
		Last Modified: Wed, 22 Jul 2020 05:54:22 GMT  
		Size: 244.5 KB (244545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:387e5ec55166d1b19edc03874e2b9e69860136ecddc6a7604b9140ecd8234338`  
		Last Modified: Wed, 22 Jul 2020 05:54:32 GMT  
		Size: 29.3 MB (29310033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:slim` - linux; 386

```console
$ docker pull mono@sha256:aa9bd9bf67b98aa34b06359dfe70fe3814af371907798d119a8462588cd65082
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.9 MB (91905241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8fca40a8702c7daddc16b743a8debdf7ff39e7886317d2f9c9c786ad5ec816e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 02:12:37 GMT
ADD file:9d59e7e41b146c16bca3047e3a0451abb508d22a91b64dfe2ce6d147381f800d in / 
# Wed, 22 Jul 2020 02:12:37 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 08:14:06 GMT
ENV MONO_VERSION=6.8.0.96
# Wed, 22 Jul 2020 08:14:20 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jul 2020 08:15:03 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:5562cfdfc3152571ce0700e9d6816dede132432ab48c7ef147e89863eac98d4d`  
		Last Modified: Wed, 22 Jul 2020 02:19:28 GMT  
		Size: 23.1 MB (23142189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb45bd2f94e2f0fe1aba8e0d40510779b6f02ba16673b85345aac02fe6df273f`  
		Last Modified: Wed, 22 Jul 2020 08:26:18 GMT  
		Size: 244.5 KB (244513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:850d9d5c8af28167dbad00d62240efef6bf70bc2d23ae0735b14eceae8ad854c`  
		Last Modified: Wed, 22 Jul 2020 08:26:45 GMT  
		Size: 68.5 MB (68518539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:slim` - linux; ppc64le

```console
$ docker pull mono@sha256:2c4949379a4b86afc1273f4a7339ff7bc658bc7749205fb8df632bfb7a7f1d63
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48706120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17986d4009e9231ade165cd631103027df60340b2b4b6fa078cdb34805a602ba`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:25:38 GMT
ADD file:41ec53d65aa183c2835f73989c9e4922f818e59774811eaa6e7395e5a36d5eab in / 
# Tue, 09 Jun 2020 01:25:42 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 04:37:42 GMT
ENV MONO_VERSION=6.8.0.96
# Tue, 09 Jun 2020 04:39:26 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Jun 2020 04:40:39 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a29e28607c9b96acae7ff89e56214e4339a87c59e40a6f030fa4cbcaab753f2c`  
		Last Modified: Tue, 09 Jun 2020 01:37:25 GMT  
		Size: 22.8 MB (22791269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e1fc192a4485fb46ca92b8e704feb4d02fab0a2a37cb4238017caf8d50239d5`  
		Last Modified: Tue, 09 Jun 2020 05:05:25 GMT  
		Size: 244.7 KB (244663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc43661bb843c17c3ae2b4bc4f6d7ffbc36d936efa982c85608c72360c89b849`  
		Last Modified: Tue, 09 Jun 2020 05:05:31 GMT  
		Size: 25.7 MB (25670188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
