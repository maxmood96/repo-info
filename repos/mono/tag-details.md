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
-	[`mono:6.12.0.182`](#mono6120182)
-	[`mono:6.12.0.182-slim`](#mono6120182-slim)
-	[`mono:latest`](#monolatest)
-	[`mono:slim`](#monoslim)

## `mono:6`

```console
$ docker pull mono@sha256:122a14d6bb94876a6584fc7dc27acf61fdcce1b612442f6a27c4e6adbe57bd50
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le

### `mono:6` - linux; amd64

```console
$ docker pull mono@sha256:d2ae1881a608fb6401bcebbf0d444fc2fcadf0db27f07c87153a79e7b14e861a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.6 MB (254589877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16d98cfcc673531288833a5cdb9f87087aa18082d1fed9ebe02021c67b1fdf0f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jun 2022 16:43:21 GMT
ADD file:cce4de1623245f9f28e3365e6cf749d85dcfedddea2d6fbc963c309a40818f52 in / 
# Wed, 22 Jun 2022 16:43:21 GMT
CMD ["bash"]
# Wed, 22 Jun 2022 16:43:21 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 22 Jun 2022 16:43:21 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr # buildkit
# Wed, 22 Jun 2022 16:43:21 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
# Wed, 22 Jun 2022 16:43:21 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
```

-	Layers:
	-	`sha256:b338562f40a7fb7360dfae935da6d7e40d2545db18bc461d9d70ec1b2b657f33`  
		Last Modified: Thu, 13 Jun 2024 01:26:49 GMT  
		Size: 27.3 MB (27337703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b1b752ddf75c64e105424fb16f5a2053ddad33f059e3be8e520e35908cc4e97`  
		Last Modified: Fri, 21 Jun 2024 01:03:10 GMT  
		Size: 2.8 MB (2780035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d574eb224b5ddbe14656e28913cf5eeb5b14aa651aa3bcb9288aa43f1000aec5`  
		Last Modified: Fri, 21 Jun 2024 01:03:11 GMT  
		Size: 64.6 MB (64555923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb9d6fb145c5367510a78273891d0ba84d7257b0bfdf3cd340f4e3d6f211de0a`  
		Last Modified: Fri, 21 Jun 2024 02:02:49 GMT  
		Size: 159.9 MB (159916216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mono:6` - unknown; unknown

```console
$ docker pull mono@sha256:fc661c46136b8f9cbe60f721c811fb05d600f7614c9ddef8306ca5a261a6ea24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11085967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6322617bf4f258627a38887597f3d55cd3e73d36de6aa5f4734d1d6fcd3e7fd9`

```dockerfile
```

-	Layers:
	-	`sha256:08c2cae238c884d7e44ae9bd57336a51412c9603e15025c0a456eca7dd888aba`  
		Last Modified: Fri, 21 Jun 2024 02:02:46 GMT  
		Size: 11.1 MB (11078059 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2dda4ada58791fac758ee1dc7c9ee2756a6d55125463cc11427657bfedecb286`  
		Last Modified: Fri, 21 Jun 2024 02:02:46 GMT  
		Size: 7.9 KB (7908 bytes)  
		MIME: application/vnd.in-toto+json

### `mono:6` - linux; arm variant v5

```console
$ docker pull mono@sha256:dea4d3a6cf8d83cd0b747ac36b0b7a279de919c38227c259e8f0dd933ad99d3d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.9 MB (192868079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52646a30a3e2966b0a92b143b872a725a0eaa3c003a2b6c3030454d2f5f26220`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 00:49:37 GMT
ADD file:2ed7ca0d45c68b46a10ae186e8a03f98e72cadfeed17105668f53adf14d31e1f in / 
# Tue, 02 Aug 2022 00:49:38 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 07:17:55 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 01 Mar 2023 07:18:17 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 01 Mar 2023 07:18:42 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 01 Mar 2023 07:20:53 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:187ecffbd1e0eae5de6567dff32bd58f28623635657779760c9d9539d6b7cc59`  
		Last Modified: Tue, 02 Aug 2022 00:57:06 GMT  
		Size: 24.9 MB (24889750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6702eef9c7d9ec6ede2c5f9a15a047b314ccc9140f25694f337c0127478bb25b`  
		Last Modified: Wed, 01 Mar 2023 07:23:12 GMT  
		Size: 2.5 MB (2467715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3781ed66d8db4f1e7c7b6323f62af11c65550a10f339ad7c0fb68f9467f8026d`  
		Last Modified: Wed, 01 Mar 2023 07:23:17 GMT  
		Size: 24.5 MB (24503499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f32f45a77bbef0505ff02ad954c1ce25d1cb8f5b668bbd7c73fa538966d0c0b`  
		Last Modified: Wed, 01 Mar 2023 07:24:21 GMT  
		Size: 141.0 MB (141007115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6` - linux; arm variant v7

```console
$ docker pull mono@sha256:0dfc1dd87793c5f9c7d9197edaa5bf64b13fd37064afba0ac721ecd09f554a22
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.2 MB (189174773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ed768bb4ba02e014621f121844e472e5e513d725bdf417d80780af7b0938c6e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:58:15 GMT
ADD file:ab786d88497f915679b3ac228e3bd805a58501dcb33b3d25e49cf1898770f9a7 in / 
# Thu, 13 Jun 2024 00:58:15 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 08:31:10 GMT
ENV MONO_VERSION=6.12.0.182
# Thu, 13 Jun 2024 08:31:24 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 13 Jun 2024 08:31:48 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 13 Jun 2024 08:34:33 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:99d1ebcdd364332a1427098feecc8f94a8978ec971b171f7cca03bf01d1a149c`  
		Last Modified: Thu, 13 Jun 2024 01:03:01 GMT  
		Size: 22.9 MB (22944997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b7db2a28ee4fa8f5e893c5ca0f653dc9514221149d19d3632816e874498e112`  
		Last Modified: Thu, 13 Jun 2024 08:36:36 GMT  
		Size: 2.4 MB (2370421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f10ac972dcba288ded8e2044b27a0cdf74494394d8408e9383d92fce7e867d7`  
		Last Modified: Thu, 13 Jun 2024 08:36:40 GMT  
		Size: 23.8 MB (23790340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bd48720e38dbaaaef8fb759054f29f92b12cbbea01eab398573da7dac4160a3`  
		Last Modified: Thu, 13 Jun 2024 08:37:30 GMT  
		Size: 140.1 MB (140069015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:83a8328a667e7c0256a9832d8a8f2a3ccb189ac80da5ef1737a9b0d1c34d80ab
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.6 MB (216552576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ca3c4505019d48c31f72bda38a3d30a9661510b2d90cc6407c5585d49362028`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:40:19 GMT
ADD file:de9a2b323e6d7d969277e7e781875e3daf3f49f2c1dcc569a1eec4f5bd789c46 in / 
# Thu, 13 Jun 2024 00:40:19 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 02:40:00 GMT
ENV MONO_VERSION=6.12.0.182
# Thu, 13 Jun 2024 02:40:07 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 13 Jun 2024 02:40:22 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 13 Jun 2024 02:43:03 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7abf9f73c7747bb840a8edcd895830e53f09498136de3015568a9cd9f5ab10ed`  
		Last Modified: Thu, 13 Jun 2024 00:44:26 GMT  
		Size: 26.1 MB (26109272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0b5b6710e68b3b250dd681138cde05cf6596b6f323c42d994db4dcdb4761526`  
		Last Modified: Thu, 13 Jun 2024 02:44:41 GMT  
		Size: 2.6 MB (2645492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd67156f41b6153be4d7339a8c26d81d9648cfb9a9e365f2486f34aa6f6f507f`  
		Last Modified: Thu, 13 Jun 2024 02:44:44 GMT  
		Size: 29.5 MB (29544907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0091f5b1c3c6fe88db8dcb2b7849fe146d7c3571535910ff86aef81e76776d8`  
		Last Modified: Thu, 13 Jun 2024 02:45:28 GMT  
		Size: 158.3 MB (158252905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6` - linux; 386

```console
$ docker pull mono@sha256:8f10891be25745681bd6f98bf48e1234094816dc4b5dbef73d48f53f67536601
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.5 MB (259458549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2775d67ed2568bc292fd99d9a4c6e6e31195ae5382d5d3f1d76cb0f034c34e5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jun 2022 16:43:21 GMT
ADD file:7bc8fc617f718bf5e65e7fd718531a01122acc1783af5233c98aa9d31b0f093e in / 
# Wed, 22 Jun 2022 16:43:21 GMT
CMD ["bash"]
# Wed, 22 Jun 2022 16:43:21 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 22 Jun 2022 16:43:21 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr # buildkit
# Wed, 22 Jun 2022 16:43:21 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
# Wed, 22 Jun 2022 16:43:21 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
```

-	Layers:
	-	`sha256:1dfc643447ff7a82c599b429eda0d998c6dbad4ab2786eed580821b5b888204e`  
		Last Modified: Thu, 13 Jun 2024 00:44:44 GMT  
		Size: 28.0 MB (27994640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a198cb1aaae91cef3ed2eaed184c0a10f0b74e857bd5ea91dcde2955746f20f9`  
		Last Modified: Fri, 21 Jun 2024 01:03:12 GMT  
		Size: 2.8 MB (2791765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd658841b3e1b2084a6340e82f84033bf765e9ea9830350aa5a4aba88cbf3166`  
		Last Modified: Fri, 21 Jun 2024 01:03:14 GMT  
		Size: 68.6 MB (68585515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30bbf7033252959af4d7a4d2f468bba517cf0aeaf9f9e131902187bdc9737e6d`  
		Last Modified: Fri, 21 Jun 2024 02:04:03 GMT  
		Size: 160.1 MB (160086629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mono:6` - unknown; unknown

```console
$ docker pull mono@sha256:e69c4a0ff0efcd311f3ec0da7e72cbafaa9689b8555686674db7d3d689e13230
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11081926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48b0f05b8c3e2ec0bdb3fcbf2f85778a7584ea1dfd621e838399e99f0e6aac47`

```dockerfile
```

-	Layers:
	-	`sha256:f5bc84e8ea570b2500296b1f25f4226e60f0c15178c4ed81b09fa2c5ddf35fc6`  
		Last Modified: Fri, 21 Jun 2024 02:03:58 GMT  
		Size: 11.1 MB (11074056 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f11f469c7181081a082c334f89f2885f7a6a0953d5e152e5f75db2af4504d80e`  
		Last Modified: Fri, 21 Jun 2024 02:03:57 GMT  
		Size: 7.9 KB (7870 bytes)  
		MIME: application/vnd.in-toto+json

### `mono:6` - linux; ppc64le

```console
$ docker pull mono@sha256:fbfb5b60906856f25cc0ffb3ed273fa5da089aed24eab6afb049cc150c221768
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.7 MB (221654331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45a10e5a16545c25df57d5cf1f034acbb78fb5a3c968378416dc576fa88386ef`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:04 GMT
ADD file:6d33ba25d3625e5f445fc2183b60c64e2cbc780cb541d7f8ac76ce193b311d13 in / 
# Tue, 02 Aug 2022 01:18:06 GMT
CMD ["bash"]
# Wed, 03 Aug 2022 02:07:46 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 03 Aug 2022 02:08:06 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 03 Aug 2022 02:08:41 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 03 Aug 2022 02:11:40 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:fc8842eebb7ccaf249b2bb2d6a3878fffdae26c9db8f23b393c7f76a6249d2f6`  
		Last Modified: Tue, 02 Aug 2022 01:25:45 GMT  
		Size: 30.6 MB (30560308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1100971c8a3b3eb42c6e22a4c25f405143f007bda60d16697d49b333925b4d84`  
		Last Modified: Wed, 03 Aug 2022 02:15:13 GMT  
		Size: 2.9 MB (2892658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:390f883f1594b5d2d40b7ba4dc50f375439dd1611f38f0c3d071a38bf2ac62cd`  
		Last Modified: Wed, 03 Aug 2022 02:15:27 GMT  
		Size: 41.9 MB (41897345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ae94af697c95b6bf75033b813f19ec72f68da49a681d5ce7078753923129147`  
		Last Modified: Wed, 03 Aug 2022 02:16:58 GMT  
		Size: 146.3 MB (146304020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6-slim`

```console
$ docker pull mono@sha256:d124eebf64f110db652f42c9e1e4a0627f84b6fc375ea3801751f7edcc74711b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le

### `mono:6-slim` - linux; amd64

```console
$ docker pull mono@sha256:749851d74745492754d1ebb3c50fc335d4b84a7bb34e17a4e7c3909c5ec1212b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.7 MB (94673661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5a2a70110040ee175a00069fa147d036d49deb2decd03a6374e83da337706e8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jun 2022 16:43:21 GMT
ADD file:cce4de1623245f9f28e3365e6cf749d85dcfedddea2d6fbc963c309a40818f52 in / 
# Wed, 22 Jun 2022 16:43:21 GMT
CMD ["bash"]
# Wed, 22 Jun 2022 16:43:21 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 22 Jun 2022 16:43:21 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr # buildkit
# Wed, 22 Jun 2022 16:43:21 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
```

-	Layers:
	-	`sha256:b338562f40a7fb7360dfae935da6d7e40d2545db18bc461d9d70ec1b2b657f33`  
		Last Modified: Thu, 13 Jun 2024 01:26:49 GMT  
		Size: 27.3 MB (27337703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b1b752ddf75c64e105424fb16f5a2053ddad33f059e3be8e520e35908cc4e97`  
		Last Modified: Fri, 21 Jun 2024 01:03:10 GMT  
		Size: 2.8 MB (2780035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d574eb224b5ddbe14656e28913cf5eeb5b14aa651aa3bcb9288aa43f1000aec5`  
		Last Modified: Fri, 21 Jun 2024 01:03:11 GMT  
		Size: 64.6 MB (64555923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mono:6-slim` - unknown; unknown

```console
$ docker pull mono@sha256:5a8421c386b586f98034983cc67448394e910e05ff857862418296991eddcf54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4134119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7daf4a5e106256a64c61c2f6e62ec4e5aa7020398e1b40c8bbe8b4e7458bec8d`

```dockerfile
```

-	Layers:
	-	`sha256:68c0c6a6586378e1af3fd618d65a15dd0a69c3e36744d2db3c2a64b91f8842b8`  
		Last Modified: Fri, 21 Jun 2024 01:03:10 GMT  
		Size: 4.1 MB (4124009 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ec35e37e8929d1729d15f72eaafb529c88604e0eb2b568452d3927312850835`  
		Last Modified: Fri, 21 Jun 2024 01:03:10 GMT  
		Size: 10.1 KB (10110 bytes)  
		MIME: application/vnd.in-toto+json

### `mono:6-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:f7c133539fa6a4add7484e9c93bc9b62ec32236d4b619f320c20b3248fb4739a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.9 MB (51860964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe52652f149ceedc89ed0c0f70985fcd898b6cd5cc98aa6f99f9ca06fd83046c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 00:49:37 GMT
ADD file:2ed7ca0d45c68b46a10ae186e8a03f98e72cadfeed17105668f53adf14d31e1f in / 
# Tue, 02 Aug 2022 00:49:38 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 07:17:55 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 01 Mar 2023 07:18:17 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 01 Mar 2023 07:18:42 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:187ecffbd1e0eae5de6567dff32bd58f28623635657779760c9d9539d6b7cc59`  
		Last Modified: Tue, 02 Aug 2022 00:57:06 GMT  
		Size: 24.9 MB (24889750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6702eef9c7d9ec6ede2c5f9a15a047b314ccc9140f25694f337c0127478bb25b`  
		Last Modified: Wed, 01 Mar 2023 07:23:12 GMT  
		Size: 2.5 MB (2467715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3781ed66d8db4f1e7c7b6323f62af11c65550a10f339ad7c0fb68f9467f8026d`  
		Last Modified: Wed, 01 Mar 2023 07:23:17 GMT  
		Size: 24.5 MB (24503499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:beaab14b4de16ae0f14cb615383dddbe283523fbd00c8494f8a55ce1299ec4ce
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49105758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:053650949e0e3231b0c67fad4f4dd10e2cb9a84beb0a82569b203ce3a1716fbd`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:58:15 GMT
ADD file:ab786d88497f915679b3ac228e3bd805a58501dcb33b3d25e49cf1898770f9a7 in / 
# Thu, 13 Jun 2024 00:58:15 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 08:31:10 GMT
ENV MONO_VERSION=6.12.0.182
# Thu, 13 Jun 2024 08:31:24 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 13 Jun 2024 08:31:48 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:99d1ebcdd364332a1427098feecc8f94a8978ec971b171f7cca03bf01d1a149c`  
		Last Modified: Thu, 13 Jun 2024 01:03:01 GMT  
		Size: 22.9 MB (22944997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b7db2a28ee4fa8f5e893c5ca0f653dc9514221149d19d3632816e874498e112`  
		Last Modified: Thu, 13 Jun 2024 08:36:36 GMT  
		Size: 2.4 MB (2370421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f10ac972dcba288ded8e2044b27a0cdf74494394d8408e9383d92fce7e867d7`  
		Last Modified: Thu, 13 Jun 2024 08:36:40 GMT  
		Size: 23.8 MB (23790340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:f0cc2d1cdff3f4c9132e03486d350424d918e8a58e17997314a1de02a04b24fc
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.3 MB (58299671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7c7359194914e922baaffe35e36d41958cbdc56e1dfe1475fdeda11d4d860f0`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:40:19 GMT
ADD file:de9a2b323e6d7d969277e7e781875e3daf3f49f2c1dcc569a1eec4f5bd789c46 in / 
# Thu, 13 Jun 2024 00:40:19 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 02:40:00 GMT
ENV MONO_VERSION=6.12.0.182
# Thu, 13 Jun 2024 02:40:07 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 13 Jun 2024 02:40:22 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7abf9f73c7747bb840a8edcd895830e53f09498136de3015568a9cd9f5ab10ed`  
		Last Modified: Thu, 13 Jun 2024 00:44:26 GMT  
		Size: 26.1 MB (26109272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0b5b6710e68b3b250dd681138cde05cf6596b6f323c42d994db4dcdb4761526`  
		Last Modified: Thu, 13 Jun 2024 02:44:41 GMT  
		Size: 2.6 MB (2645492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd67156f41b6153be4d7339a8c26d81d9648cfb9a9e365f2486f34aa6f6f507f`  
		Last Modified: Thu, 13 Jun 2024 02:44:44 GMT  
		Size: 29.5 MB (29544907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6-slim` - linux; 386

```console
$ docker pull mono@sha256:819bc68ca415cdb49ad461b4afb9a27004e442878b2bbdefc8a67317bc5b2ddf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.4 MB (99371920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c360bfbb224cb22cd13ba52ccd63bc77562ef28647c535cd0a42518f0773a842`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jun 2022 16:43:21 GMT
ADD file:7bc8fc617f718bf5e65e7fd718531a01122acc1783af5233c98aa9d31b0f093e in / 
# Wed, 22 Jun 2022 16:43:21 GMT
CMD ["bash"]
# Wed, 22 Jun 2022 16:43:21 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 22 Jun 2022 16:43:21 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr # buildkit
# Wed, 22 Jun 2022 16:43:21 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
```

-	Layers:
	-	`sha256:1dfc643447ff7a82c599b429eda0d998c6dbad4ab2786eed580821b5b888204e`  
		Last Modified: Thu, 13 Jun 2024 00:44:44 GMT  
		Size: 28.0 MB (27994640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a198cb1aaae91cef3ed2eaed184c0a10f0b74e857bd5ea91dcde2955746f20f9`  
		Last Modified: Fri, 21 Jun 2024 01:03:12 GMT  
		Size: 2.8 MB (2791765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd658841b3e1b2084a6340e82f84033bf765e9ea9830350aa5a4aba88cbf3166`  
		Last Modified: Fri, 21 Jun 2024 01:03:14 GMT  
		Size: 68.6 MB (68585515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mono:6-slim` - unknown; unknown

```console
$ docker pull mono@sha256:21b839469b89df687807ffdd3f870708c16efa44a6b299510e9d6391ba6499fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4130249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80ef153a1ce2f246cf50247bdbe0e53a65f2eca1f65498fe5be40b5242f5f8b1`

```dockerfile
```

-	Layers:
	-	`sha256:053ce445b27e3a8e224b16a3d2a8cdc9dc1d84ebee53d08de3d37ec36d5de95c`  
		Last Modified: Fri, 21 Jun 2024 01:03:12 GMT  
		Size: 4.1 MB (4120175 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:190e2c58614be0d956b94cdc868f9beb77c2f2d8ef16c981339f2b2c23f56975`  
		Last Modified: Fri, 21 Jun 2024 01:03:12 GMT  
		Size: 10.1 KB (10074 bytes)  
		MIME: application/vnd.in-toto+json

### `mono:6-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:b83383e51874bbee097571b303be3299c87d7da8c4c6b0f4e067cfaa552ad925
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75350311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c28d9c810a28445dd3b5767c5be8a3a5c5f459f859498e49f59bb419b735510`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:04 GMT
ADD file:6d33ba25d3625e5f445fc2183b60c64e2cbc780cb541d7f8ac76ce193b311d13 in / 
# Tue, 02 Aug 2022 01:18:06 GMT
CMD ["bash"]
# Wed, 03 Aug 2022 02:07:46 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 03 Aug 2022 02:08:06 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 03 Aug 2022 02:08:41 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:fc8842eebb7ccaf249b2bb2d6a3878fffdae26c9db8f23b393c7f76a6249d2f6`  
		Last Modified: Tue, 02 Aug 2022 01:25:45 GMT  
		Size: 30.6 MB (30560308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1100971c8a3b3eb42c6e22a4c25f405143f007bda60d16697d49b333925b4d84`  
		Last Modified: Wed, 03 Aug 2022 02:15:13 GMT  
		Size: 2.9 MB (2892658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:390f883f1594b5d2d40b7ba4dc50f375439dd1611f38f0c3d071a38bf2ac62cd`  
		Last Modified: Wed, 03 Aug 2022 02:15:27 GMT  
		Size: 41.9 MB (41897345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.10`

```console
$ docker pull mono@sha256:90c888289bcd3935634a4b13d26ff6718f2850764f3aaeb56511ce093af19bf9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le

### `mono:6.10` - linux; amd64

```console
$ docker pull mono@sha256:843c03721d4c4c3dc7df49913f7ec8b961da0b80934d7e2fc1ab386584503cf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.0 MB (224997323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:874411c91faac3f25999aad4273d41541fbfea71027283a4dbae8cb6bf804647`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Nov 2021 20:21:03 GMT
ADD file:cce4de1623245f9f28e3365e6cf749d85dcfedddea2d6fbc963c309a40818f52 in / 
# Tue, 23 Nov 2021 20:21:03 GMT
CMD ["bash"]
# Tue, 23 Nov 2021 20:21:03 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 23 Nov 2021 20:21:03 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr # buildkit
# Tue, 23 Nov 2021 20:21:03 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
# Tue, 23 Nov 2021 20:21:03 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
```

-	Layers:
	-	`sha256:b338562f40a7fb7360dfae935da6d7e40d2545db18bc461d9d70ec1b2b657f33`  
		Last Modified: Thu, 13 Jun 2024 01:26:49 GMT  
		Size: 27.3 MB (27337703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17858d27bab2d3cac617525d602bdb6430ef30203a5879d871c8ac9c5ed9ccc3`  
		Last Modified: Fri, 21 Jun 2024 01:03:10 GMT  
		Size: 2.8 MB (2780056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95304a756dfd5de0e2f44edffff0c73d65982f8523d664fd5f1d97ea84d3fba5`  
		Last Modified: Fri, 21 Jun 2024 01:03:11 GMT  
		Size: 64.6 MB (64563570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d38d92e81b89d82472ba771ba73bd96f9d7434d0a078d894095ba9332fedb7e4`  
		Last Modified: Fri, 21 Jun 2024 02:10:26 GMT  
		Size: 130.3 MB (130315994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mono:6.10` - unknown; unknown

```console
$ docker pull mono@sha256:f6671a285cbddce3760628595ffd4269c14d56576a01a7e1c1d9e0d22e9e3b52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.0 MB (11001689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:804b6302fcfc8892b5ad5455687216266c9950964c2ec1c967cc45dcd95365eb`

```dockerfile
```

-	Layers:
	-	`sha256:3f1bc3f47a2da7c663404a8b55db0810f54025932a6bfdbd60ed373988d5c3a3`  
		Last Modified: Fri, 21 Jun 2024 02:10:25 GMT  
		Size: 11.0 MB (10994359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bddb6bc492023a1217e6c5d5449b14b7a64e1659932a9e489d3eac1a6c8cbdb2`  
		Last Modified: Fri, 21 Jun 2024 02:10:24 GMT  
		Size: 7.3 KB (7330 bytes)  
		MIME: application/vnd.in-toto+json

### `mono:6.10` - linux; arm variant v5

```console
$ docker pull mono@sha256:5fd28ff75f47e10162fa8359e3457ed77e6a13c9eb64585df39efdf63e70a1a1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.9 MB (180861329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efa9d1dae1421f12f6f7eecf8cfaac5d7da3f6b99f6874365ce2f2f5fc9d9662`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 00:49:37 GMT
ADD file:2ed7ca0d45c68b46a10ae186e8a03f98e72cadfeed17105668f53adf14d31e1f in / 
# Tue, 02 Aug 2022 00:49:38 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 07:18:54 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 01 Mar 2023 07:19:03 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 01 Mar 2023 07:19:22 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 01 Mar 2023 07:22:13 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:187ecffbd1e0eae5de6567dff32bd58f28623635657779760c9d9539d6b7cc59`  
		Last Modified: Tue, 02 Aug 2022 00:57:06 GMT  
		Size: 24.9 MB (24889750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb25ee9d7e5ee2ba3d5fe6104206a45f2c5c425365a535e0aaac7bb9bd71034e`  
		Last Modified: Wed, 01 Mar 2023 07:23:36 GMT  
		Size: 2.5 MB (2467730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4b5b10e99353e19dd9c56deed1fd46d8ffc3c3eb2ad78b8d36ac029a085764e`  
		Last Modified: Wed, 01 Mar 2023 07:23:40 GMT  
		Size: 24.5 MB (24521836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75576104ae9839169a1957af7269a139e0be7d50d8cef2a4fe4011b528926e18`  
		Last Modified: Wed, 01 Mar 2023 07:25:04 GMT  
		Size: 129.0 MB (128982013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10` - linux; arm variant v7

```console
$ docker pull mono@sha256:a3de5ccef2538996b08c45bfd49cb46ea3590422b3225da143eeac99597ffcd3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.0 MB (176956877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea702c2c35dc05380a1ae6669baccde15c03026d470bd888d4ab700d21fff1a5`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:58:15 GMT
ADD file:ab786d88497f915679b3ac228e3bd805a58501dcb33b3d25e49cf1898770f9a7 in / 
# Thu, 13 Jun 2024 00:58:15 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 08:31:58 GMT
ENV MONO_VERSION=6.10.0.104
# Thu, 13 Jun 2024 08:32:08 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 13 Jun 2024 08:32:30 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 13 Jun 2024 08:36:17 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:99d1ebcdd364332a1427098feecc8f94a8978ec971b171f7cca03bf01d1a149c`  
		Last Modified: Thu, 13 Jun 2024 01:03:01 GMT  
		Size: 22.9 MB (22944997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2f2e243171f4163b5037b1bcf6c2bc90be788f5a944d7b2ef8d1ad32f64012f`  
		Last Modified: Thu, 13 Jun 2024 08:36:53 GMT  
		Size: 2.4 MB (2370411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf14cd536965f05b51ee4f1e379cda295071d3bf204fcefd378b8e08dd9d7776`  
		Last Modified: Thu, 13 Jun 2024 08:36:57 GMT  
		Size: 23.8 MB (23816031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56fcde8e253ae8fe8ff09311561e73ac906a5978f76a314f9dee8ac3cd0f9fb0`  
		Last Modified: Thu, 13 Jun 2024 08:38:05 GMT  
		Size: 127.8 MB (127825438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:55d24011cec396844b9ae537ca5df01446d6e83715aebcc2c398863a33f40f80
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.8 MB (203824717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aac85fdbee98fe73bd2017cf5949eadab47b515ad98598c6d98dcba6d6d86833`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:40:19 GMT
ADD file:de9a2b323e6d7d969277e7e781875e3daf3f49f2c1dcc569a1eec4f5bd789c46 in / 
# Thu, 13 Jun 2024 00:40:19 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 02:40:28 GMT
ENV MONO_VERSION=6.10.0.104
# Thu, 13 Jun 2024 02:40:35 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 13 Jun 2024 02:40:50 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 13 Jun 2024 02:44:18 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7abf9f73c7747bb840a8edcd895830e53f09498136de3015568a9cd9f5ab10ed`  
		Last Modified: Thu, 13 Jun 2024 00:44:26 GMT  
		Size: 26.1 MB (26109272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:879958e785e6e477c521bba5e76ed1f61399ef247e4ae1218c778adfe5b38160`  
		Last Modified: Thu, 13 Jun 2024 02:44:57 GMT  
		Size: 2.6 MB (2645504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98651d9c2b89ddac9896e0807df9859069b12ace5592e15653ca94df208438d4`  
		Last Modified: Thu, 13 Jun 2024 02:45:00 GMT  
		Size: 29.6 MB (29574983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3432ee081e7eeffb9ccc5d4a2939025b406b9678c395c72df9b2c374fc603d82`  
		Last Modified: Thu, 13 Jun 2024 02:45:58 GMT  
		Size: 145.5 MB (145494958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10` - linux; 386

```console
$ docker pull mono@sha256:1ff9e0605a84ebc9c1425cf380fa6538513957f14ff53668bb1415bc0de06276
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.8 MB (230808213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:165beb97a02082ea41ab2c93bf8061f5337e9c3e47d92a7c3fdbb3d91c05cf4f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Nov 2021 20:21:03 GMT
ADD file:7bc8fc617f718bf5e65e7fd718531a01122acc1783af5233c98aa9d31b0f093e in / 
# Tue, 23 Nov 2021 20:21:03 GMT
CMD ["bash"]
# Tue, 23 Nov 2021 20:21:03 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 23 Nov 2021 20:21:03 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr # buildkit
# Tue, 23 Nov 2021 20:21:03 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
# Tue, 23 Nov 2021 20:21:03 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
```

-	Layers:
	-	`sha256:1dfc643447ff7a82c599b429eda0d998c6dbad4ab2786eed580821b5b888204e`  
		Last Modified: Thu, 13 Jun 2024 00:44:44 GMT  
		Size: 28.0 MB (27994640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1fd38227c501a8e3a4c2ddbc366821c42ebe8fad426425d041d37315dd39d6b`  
		Last Modified: Fri, 21 Jun 2024 01:03:29 GMT  
		Size: 2.8 MB (2791746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69732935ca2831417791f9677707cd4ac5cce2cc5ceac6ccf0939905aa577562`  
		Last Modified: Fri, 21 Jun 2024 01:03:31 GMT  
		Size: 68.6 MB (68593059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af0ac94ccf1051dd80381d13771eba83828ecbdd644eca8d13963217a4fcad77`  
		Last Modified: Fri, 21 Jun 2024 02:02:45 GMT  
		Size: 131.4 MB (131428768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mono:6.10` - unknown; unknown

```console
$ docker pull mono@sha256:219a320599f64567f69e1dd47dcf68ea4ca8e9a382081f8459ea5df8f38492ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.0 MB (10997669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a69753b371d3937f23742ab4adf60505bc438fff530ce728a4cc8e30701256d`

```dockerfile
```

-	Layers:
	-	`sha256:9b3055c084df3c88817dd92cc8a2a1626a67e7926baf283baef3da5734e362cf`  
		Last Modified: Fri, 21 Jun 2024 02:02:42 GMT  
		Size: 11.0 MB (10990366 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7af35d4525a5846d4e984a6519b904a3595ee966a75f1a1f352401f5074bcc2`  
		Last Modified: Fri, 21 Jun 2024 02:02:42 GMT  
		Size: 7.3 KB (7303 bytes)  
		MIME: application/vnd.in-toto+json

### `mono:6.10` - linux; ppc64le

```console
$ docker pull mono@sha256:6126f0b2219e750b391e2e0d63ac7a2df863d9e2356c43fba06fee0708676038
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.7 MB (209715776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e4e952c22c47db9a79c5ca425c7de3d576d719e2042713424b88a3dae8e5129`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:04 GMT
ADD file:6d33ba25d3625e5f445fc2183b60c64e2cbc780cb541d7f8ac76ce193b311d13 in / 
# Tue, 02 Aug 2022 01:18:06 GMT
CMD ["bash"]
# Wed, 03 Aug 2022 02:08:58 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 03 Aug 2022 02:09:16 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 03 Aug 2022 02:09:49 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 03 Aug 2022 02:14:18 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:fc8842eebb7ccaf249b2bb2d6a3878fffdae26c9db8f23b393c7f76a6249d2f6`  
		Last Modified: Tue, 02 Aug 2022 01:25:45 GMT  
		Size: 30.6 MB (30560308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c0b96bc274eefbc8d34a02735b6f704f29aaf7e6c4095edb588a74c1ffb2825`  
		Last Modified: Wed, 03 Aug 2022 02:15:49 GMT  
		Size: 2.9 MB (2892610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7f103eac188d225f1b73fa0b0d6a3f2560c7fc46d7ec0f0e7e7a07330eb1ff0`  
		Last Modified: Wed, 03 Aug 2022 02:16:04 GMT  
		Size: 41.8 MB (41839360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3a64f5c66cdaf23afe83539fd8177bddc2e783d6ca6ee6eb3cabd08a6a5c375`  
		Last Modified: Wed, 03 Aug 2022 02:17:54 GMT  
		Size: 134.4 MB (134423498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.10-slim`

```console
$ docker pull mono@sha256:997252b188a7de167d4e81924def4fff75b83b9af264581b426e26f590c1cbcc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le

### `mono:6.10-slim` - linux; amd64

```console
$ docker pull mono@sha256:814dbcff677039e433ef2250b3f89b944e891faf2655a84e5fb9e24e832b20a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.7 MB (94681329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23a4fb2221d45ec07871359574d68e579e293dd9212fa65bb61dc818d9c79a73`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Nov 2021 20:21:03 GMT
ADD file:cce4de1623245f9f28e3365e6cf749d85dcfedddea2d6fbc963c309a40818f52 in / 
# Tue, 23 Nov 2021 20:21:03 GMT
CMD ["bash"]
# Tue, 23 Nov 2021 20:21:03 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 23 Nov 2021 20:21:03 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr # buildkit
# Tue, 23 Nov 2021 20:21:03 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
```

-	Layers:
	-	`sha256:b338562f40a7fb7360dfae935da6d7e40d2545db18bc461d9d70ec1b2b657f33`  
		Last Modified: Thu, 13 Jun 2024 01:26:49 GMT  
		Size: 27.3 MB (27337703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17858d27bab2d3cac617525d602bdb6430ef30203a5879d871c8ac9c5ed9ccc3`  
		Last Modified: Fri, 21 Jun 2024 01:03:10 GMT  
		Size: 2.8 MB (2780056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95304a756dfd5de0e2f44edffff0c73d65982f8523d664fd5f1d97ea84d3fba5`  
		Last Modified: Fri, 21 Jun 2024 01:03:11 GMT  
		Size: 64.6 MB (64563570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mono:6.10-slim` - unknown; unknown

```console
$ docker pull mono@sha256:491d5d49289d1b9a5bc4b07908d133d9cb48ef0683dcc08baefbf6f5811aff98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4132989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6ced6d0d7431bd499931fcee411750b9a8e9490f620918b716c506ac384aaa1`

```dockerfile
```

-	Layers:
	-	`sha256:f0b4de9e8b45105e3a7b5b7820ec78abe67d446be81e23c068710fa4467ce393`  
		Last Modified: Fri, 21 Jun 2024 01:03:10 GMT  
		Size: 4.1 MB (4123463 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fbb819f516836e26bb95911256c4b78f388e9c1de432e7a3639d7164f01e7d29`  
		Last Modified: Fri, 21 Jun 2024 01:03:10 GMT  
		Size: 9.5 KB (9526 bytes)  
		MIME: application/vnd.in-toto+json

### `mono:6.10-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:9d52e2f9db76c24f9964eec255de917d7a05b180e6e45f98545846b130400ab6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.9 MB (51879316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccac5ddbcee195ea38a9828f45d157f2ef674624fb9a6a2d5529fc2f8e6b736a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 00:49:37 GMT
ADD file:2ed7ca0d45c68b46a10ae186e8a03f98e72cadfeed17105668f53adf14d31e1f in / 
# Tue, 02 Aug 2022 00:49:38 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 07:18:54 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 01 Mar 2023 07:19:03 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 01 Mar 2023 07:19:22 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:187ecffbd1e0eae5de6567dff32bd58f28623635657779760c9d9539d6b7cc59`  
		Last Modified: Tue, 02 Aug 2022 00:57:06 GMT  
		Size: 24.9 MB (24889750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb25ee9d7e5ee2ba3d5fe6104206a45f2c5c425365a535e0aaac7bb9bd71034e`  
		Last Modified: Wed, 01 Mar 2023 07:23:36 GMT  
		Size: 2.5 MB (2467730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4b5b10e99353e19dd9c56deed1fd46d8ffc3c3eb2ad78b8d36ac029a085764e`  
		Last Modified: Wed, 01 Mar 2023 07:23:40 GMT  
		Size: 24.5 MB (24521836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:f788e39c64bc81a99ebc71841cfdb44616b8a780cdf7d6c4103a07590c4ed13d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49131439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9da1f749b46b22975ae899c2925624b519c409162edbca3067a515980114bd9a`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:58:15 GMT
ADD file:ab786d88497f915679b3ac228e3bd805a58501dcb33b3d25e49cf1898770f9a7 in / 
# Thu, 13 Jun 2024 00:58:15 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 08:31:58 GMT
ENV MONO_VERSION=6.10.0.104
# Thu, 13 Jun 2024 08:32:08 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 13 Jun 2024 08:32:30 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:99d1ebcdd364332a1427098feecc8f94a8978ec971b171f7cca03bf01d1a149c`  
		Last Modified: Thu, 13 Jun 2024 01:03:01 GMT  
		Size: 22.9 MB (22944997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2f2e243171f4163b5037b1bcf6c2bc90be788f5a944d7b2ef8d1ad32f64012f`  
		Last Modified: Thu, 13 Jun 2024 08:36:53 GMT  
		Size: 2.4 MB (2370411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf14cd536965f05b51ee4f1e379cda295071d3bf204fcefd378b8e08dd9d7776`  
		Last Modified: Thu, 13 Jun 2024 08:36:57 GMT  
		Size: 23.8 MB (23816031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:2586824f4404d8e6252193767366b20681c79d29284065c7fcad3fae0e2a0210
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.3 MB (58329759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c5abbcbdafdf051b7b9510d4392cdd8fe76a592ba0cc6aef61f2915f09843df`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:40:19 GMT
ADD file:de9a2b323e6d7d969277e7e781875e3daf3f49f2c1dcc569a1eec4f5bd789c46 in / 
# Thu, 13 Jun 2024 00:40:19 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 02:40:28 GMT
ENV MONO_VERSION=6.10.0.104
# Thu, 13 Jun 2024 02:40:35 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 13 Jun 2024 02:40:50 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7abf9f73c7747bb840a8edcd895830e53f09498136de3015568a9cd9f5ab10ed`  
		Last Modified: Thu, 13 Jun 2024 00:44:26 GMT  
		Size: 26.1 MB (26109272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:879958e785e6e477c521bba5e76ed1f61399ef247e4ae1218c778adfe5b38160`  
		Last Modified: Thu, 13 Jun 2024 02:44:57 GMT  
		Size: 2.6 MB (2645504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98651d9c2b89ddac9896e0807df9859069b12ace5592e15653ca94df208438d4`  
		Last Modified: Thu, 13 Jun 2024 02:45:00 GMT  
		Size: 29.6 MB (29574983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10-slim` - linux; 386

```console
$ docker pull mono@sha256:7e31f221c58cec452ee510c920dfbf8012b4ca33614cb6bc3d8d592e1ea87cfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.4 MB (99379445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89f170f621f13cadeb2e8c70c95a554eb5d0fda433dc2465673365d3d3d9b047`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Nov 2021 20:21:03 GMT
ADD file:7bc8fc617f718bf5e65e7fd718531a01122acc1783af5233c98aa9d31b0f093e in / 
# Tue, 23 Nov 2021 20:21:03 GMT
CMD ["bash"]
# Tue, 23 Nov 2021 20:21:03 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 23 Nov 2021 20:21:03 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr # buildkit
# Tue, 23 Nov 2021 20:21:03 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
```

-	Layers:
	-	`sha256:1dfc643447ff7a82c599b429eda0d998c6dbad4ab2786eed580821b5b888204e`  
		Last Modified: Thu, 13 Jun 2024 00:44:44 GMT  
		Size: 28.0 MB (27994640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1fd38227c501a8e3a4c2ddbc366821c42ebe8fad426425d041d37315dd39d6b`  
		Last Modified: Fri, 21 Jun 2024 01:03:29 GMT  
		Size: 2.8 MB (2791746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69732935ca2831417791f9677707cd4ac5cce2cc5ceac6ccf0939905aa577562`  
		Last Modified: Fri, 21 Jun 2024 01:03:31 GMT  
		Size: 68.6 MB (68593059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mono:6.10-slim` - unknown; unknown

```console
$ docker pull mono@sha256:af2cca3ede0f45937d1f08bea05e1e69c4ffa371a4c56eb56df016825486e19a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4129139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd3ff001a6d90676b013ef8d12dd787c62ec6e8d2b16046c50c0b07cfde1bfa6`

```dockerfile
```

-	Layers:
	-	`sha256:1ed57169d510571d116c2eb97578bcb8bc86e9f5a81d45fa519f2dcbf6a70c18`  
		Last Modified: Fri, 21 Jun 2024 01:03:29 GMT  
		Size: 4.1 MB (4119639 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:058644825e2ae60ddee3857e80f06301c1446a83d3108a8d7539f9337ec24f79`  
		Last Modified: Fri, 21 Jun 2024 01:03:29 GMT  
		Size: 9.5 KB (9500 bytes)  
		MIME: application/vnd.in-toto+json

### `mono:6.10-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:defa2f8c047d839e590b97fb1b9652e93b82414d17f8dea7279f1bc0f467fcf0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.3 MB (75292278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98e30e35a5de236a142e7288a3c84a86005d1c742b41498b3f75a9f26b3a76ca`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:04 GMT
ADD file:6d33ba25d3625e5f445fc2183b60c64e2cbc780cb541d7f8ac76ce193b311d13 in / 
# Tue, 02 Aug 2022 01:18:06 GMT
CMD ["bash"]
# Wed, 03 Aug 2022 02:08:58 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 03 Aug 2022 02:09:16 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 03 Aug 2022 02:09:49 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:fc8842eebb7ccaf249b2bb2d6a3878fffdae26c9db8f23b393c7f76a6249d2f6`  
		Last Modified: Tue, 02 Aug 2022 01:25:45 GMT  
		Size: 30.6 MB (30560308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c0b96bc274eefbc8d34a02735b6f704f29aaf7e6c4095edb588a74c1ffb2825`  
		Last Modified: Wed, 03 Aug 2022 02:15:49 GMT  
		Size: 2.9 MB (2892610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7f103eac188d225f1b73fa0b0d6a3f2560c7fc46d7ec0f0e7e7a07330eb1ff0`  
		Last Modified: Wed, 03 Aug 2022 02:16:04 GMT  
		Size: 41.8 MB (41839360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.10.0`

```console
$ docker pull mono@sha256:90c888289bcd3935634a4b13d26ff6718f2850764f3aaeb56511ce093af19bf9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le

### `mono:6.10.0` - linux; amd64

```console
$ docker pull mono@sha256:843c03721d4c4c3dc7df49913f7ec8b961da0b80934d7e2fc1ab386584503cf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.0 MB (224997323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:874411c91faac3f25999aad4273d41541fbfea71027283a4dbae8cb6bf804647`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Nov 2021 20:21:03 GMT
ADD file:cce4de1623245f9f28e3365e6cf749d85dcfedddea2d6fbc963c309a40818f52 in / 
# Tue, 23 Nov 2021 20:21:03 GMT
CMD ["bash"]
# Tue, 23 Nov 2021 20:21:03 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 23 Nov 2021 20:21:03 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr # buildkit
# Tue, 23 Nov 2021 20:21:03 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
# Tue, 23 Nov 2021 20:21:03 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
```

-	Layers:
	-	`sha256:b338562f40a7fb7360dfae935da6d7e40d2545db18bc461d9d70ec1b2b657f33`  
		Last Modified: Thu, 13 Jun 2024 01:26:49 GMT  
		Size: 27.3 MB (27337703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17858d27bab2d3cac617525d602bdb6430ef30203a5879d871c8ac9c5ed9ccc3`  
		Last Modified: Fri, 21 Jun 2024 01:03:10 GMT  
		Size: 2.8 MB (2780056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95304a756dfd5de0e2f44edffff0c73d65982f8523d664fd5f1d97ea84d3fba5`  
		Last Modified: Fri, 21 Jun 2024 01:03:11 GMT  
		Size: 64.6 MB (64563570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d38d92e81b89d82472ba771ba73bd96f9d7434d0a078d894095ba9332fedb7e4`  
		Last Modified: Fri, 21 Jun 2024 02:10:26 GMT  
		Size: 130.3 MB (130315994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mono:6.10.0` - unknown; unknown

```console
$ docker pull mono@sha256:f6671a285cbddce3760628595ffd4269c14d56576a01a7e1c1d9e0d22e9e3b52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.0 MB (11001689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:804b6302fcfc8892b5ad5455687216266c9950964c2ec1c967cc45dcd95365eb`

```dockerfile
```

-	Layers:
	-	`sha256:3f1bc3f47a2da7c663404a8b55db0810f54025932a6bfdbd60ed373988d5c3a3`  
		Last Modified: Fri, 21 Jun 2024 02:10:25 GMT  
		Size: 11.0 MB (10994359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bddb6bc492023a1217e6c5d5449b14b7a64e1659932a9e489d3eac1a6c8cbdb2`  
		Last Modified: Fri, 21 Jun 2024 02:10:24 GMT  
		Size: 7.3 KB (7330 bytes)  
		MIME: application/vnd.in-toto+json

### `mono:6.10.0` - linux; arm variant v5

```console
$ docker pull mono@sha256:5fd28ff75f47e10162fa8359e3457ed77e6a13c9eb64585df39efdf63e70a1a1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.9 MB (180861329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efa9d1dae1421f12f6f7eecf8cfaac5d7da3f6b99f6874365ce2f2f5fc9d9662`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 00:49:37 GMT
ADD file:2ed7ca0d45c68b46a10ae186e8a03f98e72cadfeed17105668f53adf14d31e1f in / 
# Tue, 02 Aug 2022 00:49:38 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 07:18:54 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 01 Mar 2023 07:19:03 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 01 Mar 2023 07:19:22 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 01 Mar 2023 07:22:13 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:187ecffbd1e0eae5de6567dff32bd58f28623635657779760c9d9539d6b7cc59`  
		Last Modified: Tue, 02 Aug 2022 00:57:06 GMT  
		Size: 24.9 MB (24889750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb25ee9d7e5ee2ba3d5fe6104206a45f2c5c425365a535e0aaac7bb9bd71034e`  
		Last Modified: Wed, 01 Mar 2023 07:23:36 GMT  
		Size: 2.5 MB (2467730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4b5b10e99353e19dd9c56deed1fd46d8ffc3c3eb2ad78b8d36ac029a085764e`  
		Last Modified: Wed, 01 Mar 2023 07:23:40 GMT  
		Size: 24.5 MB (24521836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75576104ae9839169a1957af7269a139e0be7d50d8cef2a4fe4011b528926e18`  
		Last Modified: Wed, 01 Mar 2023 07:25:04 GMT  
		Size: 129.0 MB (128982013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0` - linux; arm variant v7

```console
$ docker pull mono@sha256:a3de5ccef2538996b08c45bfd49cb46ea3590422b3225da143eeac99597ffcd3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.0 MB (176956877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea702c2c35dc05380a1ae6669baccde15c03026d470bd888d4ab700d21fff1a5`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:58:15 GMT
ADD file:ab786d88497f915679b3ac228e3bd805a58501dcb33b3d25e49cf1898770f9a7 in / 
# Thu, 13 Jun 2024 00:58:15 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 08:31:58 GMT
ENV MONO_VERSION=6.10.0.104
# Thu, 13 Jun 2024 08:32:08 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 13 Jun 2024 08:32:30 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 13 Jun 2024 08:36:17 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:99d1ebcdd364332a1427098feecc8f94a8978ec971b171f7cca03bf01d1a149c`  
		Last Modified: Thu, 13 Jun 2024 01:03:01 GMT  
		Size: 22.9 MB (22944997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2f2e243171f4163b5037b1bcf6c2bc90be788f5a944d7b2ef8d1ad32f64012f`  
		Last Modified: Thu, 13 Jun 2024 08:36:53 GMT  
		Size: 2.4 MB (2370411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf14cd536965f05b51ee4f1e379cda295071d3bf204fcefd378b8e08dd9d7776`  
		Last Modified: Thu, 13 Jun 2024 08:36:57 GMT  
		Size: 23.8 MB (23816031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56fcde8e253ae8fe8ff09311561e73ac906a5978f76a314f9dee8ac3cd0f9fb0`  
		Last Modified: Thu, 13 Jun 2024 08:38:05 GMT  
		Size: 127.8 MB (127825438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:55d24011cec396844b9ae537ca5df01446d6e83715aebcc2c398863a33f40f80
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.8 MB (203824717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aac85fdbee98fe73bd2017cf5949eadab47b515ad98598c6d98dcba6d6d86833`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:40:19 GMT
ADD file:de9a2b323e6d7d969277e7e781875e3daf3f49f2c1dcc569a1eec4f5bd789c46 in / 
# Thu, 13 Jun 2024 00:40:19 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 02:40:28 GMT
ENV MONO_VERSION=6.10.0.104
# Thu, 13 Jun 2024 02:40:35 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 13 Jun 2024 02:40:50 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 13 Jun 2024 02:44:18 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7abf9f73c7747bb840a8edcd895830e53f09498136de3015568a9cd9f5ab10ed`  
		Last Modified: Thu, 13 Jun 2024 00:44:26 GMT  
		Size: 26.1 MB (26109272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:879958e785e6e477c521bba5e76ed1f61399ef247e4ae1218c778adfe5b38160`  
		Last Modified: Thu, 13 Jun 2024 02:44:57 GMT  
		Size: 2.6 MB (2645504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98651d9c2b89ddac9896e0807df9859069b12ace5592e15653ca94df208438d4`  
		Last Modified: Thu, 13 Jun 2024 02:45:00 GMT  
		Size: 29.6 MB (29574983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3432ee081e7eeffb9ccc5d4a2939025b406b9678c395c72df9b2c374fc603d82`  
		Last Modified: Thu, 13 Jun 2024 02:45:58 GMT  
		Size: 145.5 MB (145494958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0` - linux; 386

```console
$ docker pull mono@sha256:1ff9e0605a84ebc9c1425cf380fa6538513957f14ff53668bb1415bc0de06276
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.8 MB (230808213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:165beb97a02082ea41ab2c93bf8061f5337e9c3e47d92a7c3fdbb3d91c05cf4f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Nov 2021 20:21:03 GMT
ADD file:7bc8fc617f718bf5e65e7fd718531a01122acc1783af5233c98aa9d31b0f093e in / 
# Tue, 23 Nov 2021 20:21:03 GMT
CMD ["bash"]
# Tue, 23 Nov 2021 20:21:03 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 23 Nov 2021 20:21:03 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr # buildkit
# Tue, 23 Nov 2021 20:21:03 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
# Tue, 23 Nov 2021 20:21:03 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
```

-	Layers:
	-	`sha256:1dfc643447ff7a82c599b429eda0d998c6dbad4ab2786eed580821b5b888204e`  
		Last Modified: Thu, 13 Jun 2024 00:44:44 GMT  
		Size: 28.0 MB (27994640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1fd38227c501a8e3a4c2ddbc366821c42ebe8fad426425d041d37315dd39d6b`  
		Last Modified: Fri, 21 Jun 2024 01:03:29 GMT  
		Size: 2.8 MB (2791746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69732935ca2831417791f9677707cd4ac5cce2cc5ceac6ccf0939905aa577562`  
		Last Modified: Fri, 21 Jun 2024 01:03:31 GMT  
		Size: 68.6 MB (68593059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af0ac94ccf1051dd80381d13771eba83828ecbdd644eca8d13963217a4fcad77`  
		Last Modified: Fri, 21 Jun 2024 02:02:45 GMT  
		Size: 131.4 MB (131428768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mono:6.10.0` - unknown; unknown

```console
$ docker pull mono@sha256:219a320599f64567f69e1dd47dcf68ea4ca8e9a382081f8459ea5df8f38492ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.0 MB (10997669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a69753b371d3937f23742ab4adf60505bc438fff530ce728a4cc8e30701256d`

```dockerfile
```

-	Layers:
	-	`sha256:9b3055c084df3c88817dd92cc8a2a1626a67e7926baf283baef3da5734e362cf`  
		Last Modified: Fri, 21 Jun 2024 02:02:42 GMT  
		Size: 11.0 MB (10990366 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7af35d4525a5846d4e984a6519b904a3595ee966a75f1a1f352401f5074bcc2`  
		Last Modified: Fri, 21 Jun 2024 02:02:42 GMT  
		Size: 7.3 KB (7303 bytes)  
		MIME: application/vnd.in-toto+json

### `mono:6.10.0` - linux; ppc64le

```console
$ docker pull mono@sha256:6126f0b2219e750b391e2e0d63ac7a2df863d9e2356c43fba06fee0708676038
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.7 MB (209715776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e4e952c22c47db9a79c5ca425c7de3d576d719e2042713424b88a3dae8e5129`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:04 GMT
ADD file:6d33ba25d3625e5f445fc2183b60c64e2cbc780cb541d7f8ac76ce193b311d13 in / 
# Tue, 02 Aug 2022 01:18:06 GMT
CMD ["bash"]
# Wed, 03 Aug 2022 02:08:58 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 03 Aug 2022 02:09:16 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 03 Aug 2022 02:09:49 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 03 Aug 2022 02:14:18 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:fc8842eebb7ccaf249b2bb2d6a3878fffdae26c9db8f23b393c7f76a6249d2f6`  
		Last Modified: Tue, 02 Aug 2022 01:25:45 GMT  
		Size: 30.6 MB (30560308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c0b96bc274eefbc8d34a02735b6f704f29aaf7e6c4095edb588a74c1ffb2825`  
		Last Modified: Wed, 03 Aug 2022 02:15:49 GMT  
		Size: 2.9 MB (2892610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7f103eac188d225f1b73fa0b0d6a3f2560c7fc46d7ec0f0e7e7a07330eb1ff0`  
		Last Modified: Wed, 03 Aug 2022 02:16:04 GMT  
		Size: 41.8 MB (41839360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3a64f5c66cdaf23afe83539fd8177bddc2e783d6ca6ee6eb3cabd08a6a5c375`  
		Last Modified: Wed, 03 Aug 2022 02:17:54 GMT  
		Size: 134.4 MB (134423498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.10.0-slim`

```console
$ docker pull mono@sha256:997252b188a7de167d4e81924def4fff75b83b9af264581b426e26f590c1cbcc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le

### `mono:6.10.0-slim` - linux; amd64

```console
$ docker pull mono@sha256:814dbcff677039e433ef2250b3f89b944e891faf2655a84e5fb9e24e832b20a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.7 MB (94681329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23a4fb2221d45ec07871359574d68e579e293dd9212fa65bb61dc818d9c79a73`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Nov 2021 20:21:03 GMT
ADD file:cce4de1623245f9f28e3365e6cf749d85dcfedddea2d6fbc963c309a40818f52 in / 
# Tue, 23 Nov 2021 20:21:03 GMT
CMD ["bash"]
# Tue, 23 Nov 2021 20:21:03 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 23 Nov 2021 20:21:03 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr # buildkit
# Tue, 23 Nov 2021 20:21:03 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
```

-	Layers:
	-	`sha256:b338562f40a7fb7360dfae935da6d7e40d2545db18bc461d9d70ec1b2b657f33`  
		Last Modified: Thu, 13 Jun 2024 01:26:49 GMT  
		Size: 27.3 MB (27337703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17858d27bab2d3cac617525d602bdb6430ef30203a5879d871c8ac9c5ed9ccc3`  
		Last Modified: Fri, 21 Jun 2024 01:03:10 GMT  
		Size: 2.8 MB (2780056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95304a756dfd5de0e2f44edffff0c73d65982f8523d664fd5f1d97ea84d3fba5`  
		Last Modified: Fri, 21 Jun 2024 01:03:11 GMT  
		Size: 64.6 MB (64563570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mono:6.10.0-slim` - unknown; unknown

```console
$ docker pull mono@sha256:491d5d49289d1b9a5bc4b07908d133d9cb48ef0683dcc08baefbf6f5811aff98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4132989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6ced6d0d7431bd499931fcee411750b9a8e9490f620918b716c506ac384aaa1`

```dockerfile
```

-	Layers:
	-	`sha256:f0b4de9e8b45105e3a7b5b7820ec78abe67d446be81e23c068710fa4467ce393`  
		Last Modified: Fri, 21 Jun 2024 01:03:10 GMT  
		Size: 4.1 MB (4123463 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fbb819f516836e26bb95911256c4b78f388e9c1de432e7a3639d7164f01e7d29`  
		Last Modified: Fri, 21 Jun 2024 01:03:10 GMT  
		Size: 9.5 KB (9526 bytes)  
		MIME: application/vnd.in-toto+json

### `mono:6.10.0-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:9d52e2f9db76c24f9964eec255de917d7a05b180e6e45f98545846b130400ab6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.9 MB (51879316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccac5ddbcee195ea38a9828f45d157f2ef674624fb9a6a2d5529fc2f8e6b736a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 00:49:37 GMT
ADD file:2ed7ca0d45c68b46a10ae186e8a03f98e72cadfeed17105668f53adf14d31e1f in / 
# Tue, 02 Aug 2022 00:49:38 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 07:18:54 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 01 Mar 2023 07:19:03 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 01 Mar 2023 07:19:22 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:187ecffbd1e0eae5de6567dff32bd58f28623635657779760c9d9539d6b7cc59`  
		Last Modified: Tue, 02 Aug 2022 00:57:06 GMT  
		Size: 24.9 MB (24889750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb25ee9d7e5ee2ba3d5fe6104206a45f2c5c425365a535e0aaac7bb9bd71034e`  
		Last Modified: Wed, 01 Mar 2023 07:23:36 GMT  
		Size: 2.5 MB (2467730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4b5b10e99353e19dd9c56deed1fd46d8ffc3c3eb2ad78b8d36ac029a085764e`  
		Last Modified: Wed, 01 Mar 2023 07:23:40 GMT  
		Size: 24.5 MB (24521836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:f788e39c64bc81a99ebc71841cfdb44616b8a780cdf7d6c4103a07590c4ed13d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49131439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9da1f749b46b22975ae899c2925624b519c409162edbca3067a515980114bd9a`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:58:15 GMT
ADD file:ab786d88497f915679b3ac228e3bd805a58501dcb33b3d25e49cf1898770f9a7 in / 
# Thu, 13 Jun 2024 00:58:15 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 08:31:58 GMT
ENV MONO_VERSION=6.10.0.104
# Thu, 13 Jun 2024 08:32:08 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 13 Jun 2024 08:32:30 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:99d1ebcdd364332a1427098feecc8f94a8978ec971b171f7cca03bf01d1a149c`  
		Last Modified: Thu, 13 Jun 2024 01:03:01 GMT  
		Size: 22.9 MB (22944997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2f2e243171f4163b5037b1bcf6c2bc90be788f5a944d7b2ef8d1ad32f64012f`  
		Last Modified: Thu, 13 Jun 2024 08:36:53 GMT  
		Size: 2.4 MB (2370411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf14cd536965f05b51ee4f1e379cda295071d3bf204fcefd378b8e08dd9d7776`  
		Last Modified: Thu, 13 Jun 2024 08:36:57 GMT  
		Size: 23.8 MB (23816031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:2586824f4404d8e6252193767366b20681c79d29284065c7fcad3fae0e2a0210
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.3 MB (58329759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c5abbcbdafdf051b7b9510d4392cdd8fe76a592ba0cc6aef61f2915f09843df`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:40:19 GMT
ADD file:de9a2b323e6d7d969277e7e781875e3daf3f49f2c1dcc569a1eec4f5bd789c46 in / 
# Thu, 13 Jun 2024 00:40:19 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 02:40:28 GMT
ENV MONO_VERSION=6.10.0.104
# Thu, 13 Jun 2024 02:40:35 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 13 Jun 2024 02:40:50 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7abf9f73c7747bb840a8edcd895830e53f09498136de3015568a9cd9f5ab10ed`  
		Last Modified: Thu, 13 Jun 2024 00:44:26 GMT  
		Size: 26.1 MB (26109272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:879958e785e6e477c521bba5e76ed1f61399ef247e4ae1218c778adfe5b38160`  
		Last Modified: Thu, 13 Jun 2024 02:44:57 GMT  
		Size: 2.6 MB (2645504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98651d9c2b89ddac9896e0807df9859069b12ace5592e15653ca94df208438d4`  
		Last Modified: Thu, 13 Jun 2024 02:45:00 GMT  
		Size: 29.6 MB (29574983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0-slim` - linux; 386

```console
$ docker pull mono@sha256:7e31f221c58cec452ee510c920dfbf8012b4ca33614cb6bc3d8d592e1ea87cfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.4 MB (99379445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89f170f621f13cadeb2e8c70c95a554eb5d0fda433dc2465673365d3d3d9b047`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Nov 2021 20:21:03 GMT
ADD file:7bc8fc617f718bf5e65e7fd718531a01122acc1783af5233c98aa9d31b0f093e in / 
# Tue, 23 Nov 2021 20:21:03 GMT
CMD ["bash"]
# Tue, 23 Nov 2021 20:21:03 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 23 Nov 2021 20:21:03 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr # buildkit
# Tue, 23 Nov 2021 20:21:03 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
```

-	Layers:
	-	`sha256:1dfc643447ff7a82c599b429eda0d998c6dbad4ab2786eed580821b5b888204e`  
		Last Modified: Thu, 13 Jun 2024 00:44:44 GMT  
		Size: 28.0 MB (27994640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1fd38227c501a8e3a4c2ddbc366821c42ebe8fad426425d041d37315dd39d6b`  
		Last Modified: Fri, 21 Jun 2024 01:03:29 GMT  
		Size: 2.8 MB (2791746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69732935ca2831417791f9677707cd4ac5cce2cc5ceac6ccf0939905aa577562`  
		Last Modified: Fri, 21 Jun 2024 01:03:31 GMT  
		Size: 68.6 MB (68593059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mono:6.10.0-slim` - unknown; unknown

```console
$ docker pull mono@sha256:af2cca3ede0f45937d1f08bea05e1e69c4ffa371a4c56eb56df016825486e19a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4129139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd3ff001a6d90676b013ef8d12dd787c62ec6e8d2b16046c50c0b07cfde1bfa6`

```dockerfile
```

-	Layers:
	-	`sha256:1ed57169d510571d116c2eb97578bcb8bc86e9f5a81d45fa519f2dcbf6a70c18`  
		Last Modified: Fri, 21 Jun 2024 01:03:29 GMT  
		Size: 4.1 MB (4119639 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:058644825e2ae60ddee3857e80f06301c1446a83d3108a8d7539f9337ec24f79`  
		Last Modified: Fri, 21 Jun 2024 01:03:29 GMT  
		Size: 9.5 KB (9500 bytes)  
		MIME: application/vnd.in-toto+json

### `mono:6.10.0-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:defa2f8c047d839e590b97fb1b9652e93b82414d17f8dea7279f1bc0f467fcf0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.3 MB (75292278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98e30e35a5de236a142e7288a3c84a86005d1c742b41498b3f75a9f26b3a76ca`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:04 GMT
ADD file:6d33ba25d3625e5f445fc2183b60c64e2cbc780cb541d7f8ac76ce193b311d13 in / 
# Tue, 02 Aug 2022 01:18:06 GMT
CMD ["bash"]
# Wed, 03 Aug 2022 02:08:58 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 03 Aug 2022 02:09:16 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 03 Aug 2022 02:09:49 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:fc8842eebb7ccaf249b2bb2d6a3878fffdae26c9db8f23b393c7f76a6249d2f6`  
		Last Modified: Tue, 02 Aug 2022 01:25:45 GMT  
		Size: 30.6 MB (30560308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c0b96bc274eefbc8d34a02735b6f704f29aaf7e6c4095edb588a74c1ffb2825`  
		Last Modified: Wed, 03 Aug 2022 02:15:49 GMT  
		Size: 2.9 MB (2892610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7f103eac188d225f1b73fa0b0d6a3f2560c7fc46d7ec0f0e7e7a07330eb1ff0`  
		Last Modified: Wed, 03 Aug 2022 02:16:04 GMT  
		Size: 41.8 MB (41839360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.10.0.104`

```console
$ docker pull mono@sha256:90c888289bcd3935634a4b13d26ff6718f2850764f3aaeb56511ce093af19bf9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le

### `mono:6.10.0.104` - linux; amd64

```console
$ docker pull mono@sha256:843c03721d4c4c3dc7df49913f7ec8b961da0b80934d7e2fc1ab386584503cf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.0 MB (224997323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:874411c91faac3f25999aad4273d41541fbfea71027283a4dbae8cb6bf804647`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Nov 2021 20:21:03 GMT
ADD file:cce4de1623245f9f28e3365e6cf749d85dcfedddea2d6fbc963c309a40818f52 in / 
# Tue, 23 Nov 2021 20:21:03 GMT
CMD ["bash"]
# Tue, 23 Nov 2021 20:21:03 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 23 Nov 2021 20:21:03 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr # buildkit
# Tue, 23 Nov 2021 20:21:03 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
# Tue, 23 Nov 2021 20:21:03 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
```

-	Layers:
	-	`sha256:b338562f40a7fb7360dfae935da6d7e40d2545db18bc461d9d70ec1b2b657f33`  
		Last Modified: Thu, 13 Jun 2024 01:26:49 GMT  
		Size: 27.3 MB (27337703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17858d27bab2d3cac617525d602bdb6430ef30203a5879d871c8ac9c5ed9ccc3`  
		Last Modified: Fri, 21 Jun 2024 01:03:10 GMT  
		Size: 2.8 MB (2780056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95304a756dfd5de0e2f44edffff0c73d65982f8523d664fd5f1d97ea84d3fba5`  
		Last Modified: Fri, 21 Jun 2024 01:03:11 GMT  
		Size: 64.6 MB (64563570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d38d92e81b89d82472ba771ba73bd96f9d7434d0a078d894095ba9332fedb7e4`  
		Last Modified: Fri, 21 Jun 2024 02:10:26 GMT  
		Size: 130.3 MB (130315994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mono:6.10.0.104` - unknown; unknown

```console
$ docker pull mono@sha256:f6671a285cbddce3760628595ffd4269c14d56576a01a7e1c1d9e0d22e9e3b52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.0 MB (11001689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:804b6302fcfc8892b5ad5455687216266c9950964c2ec1c967cc45dcd95365eb`

```dockerfile
```

-	Layers:
	-	`sha256:3f1bc3f47a2da7c663404a8b55db0810f54025932a6bfdbd60ed373988d5c3a3`  
		Last Modified: Fri, 21 Jun 2024 02:10:25 GMT  
		Size: 11.0 MB (10994359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bddb6bc492023a1217e6c5d5449b14b7a64e1659932a9e489d3eac1a6c8cbdb2`  
		Last Modified: Fri, 21 Jun 2024 02:10:24 GMT  
		Size: 7.3 KB (7330 bytes)  
		MIME: application/vnd.in-toto+json

### `mono:6.10.0.104` - linux; arm variant v5

```console
$ docker pull mono@sha256:5fd28ff75f47e10162fa8359e3457ed77e6a13c9eb64585df39efdf63e70a1a1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.9 MB (180861329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efa9d1dae1421f12f6f7eecf8cfaac5d7da3f6b99f6874365ce2f2f5fc9d9662`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 00:49:37 GMT
ADD file:2ed7ca0d45c68b46a10ae186e8a03f98e72cadfeed17105668f53adf14d31e1f in / 
# Tue, 02 Aug 2022 00:49:38 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 07:18:54 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 01 Mar 2023 07:19:03 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 01 Mar 2023 07:19:22 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 01 Mar 2023 07:22:13 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:187ecffbd1e0eae5de6567dff32bd58f28623635657779760c9d9539d6b7cc59`  
		Last Modified: Tue, 02 Aug 2022 00:57:06 GMT  
		Size: 24.9 MB (24889750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb25ee9d7e5ee2ba3d5fe6104206a45f2c5c425365a535e0aaac7bb9bd71034e`  
		Last Modified: Wed, 01 Mar 2023 07:23:36 GMT  
		Size: 2.5 MB (2467730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4b5b10e99353e19dd9c56deed1fd46d8ffc3c3eb2ad78b8d36ac029a085764e`  
		Last Modified: Wed, 01 Mar 2023 07:23:40 GMT  
		Size: 24.5 MB (24521836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75576104ae9839169a1957af7269a139e0be7d50d8cef2a4fe4011b528926e18`  
		Last Modified: Wed, 01 Mar 2023 07:25:04 GMT  
		Size: 129.0 MB (128982013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0.104` - linux; arm variant v7

```console
$ docker pull mono@sha256:a3de5ccef2538996b08c45bfd49cb46ea3590422b3225da143eeac99597ffcd3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.0 MB (176956877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea702c2c35dc05380a1ae6669baccde15c03026d470bd888d4ab700d21fff1a5`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:58:15 GMT
ADD file:ab786d88497f915679b3ac228e3bd805a58501dcb33b3d25e49cf1898770f9a7 in / 
# Thu, 13 Jun 2024 00:58:15 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 08:31:58 GMT
ENV MONO_VERSION=6.10.0.104
# Thu, 13 Jun 2024 08:32:08 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 13 Jun 2024 08:32:30 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 13 Jun 2024 08:36:17 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:99d1ebcdd364332a1427098feecc8f94a8978ec971b171f7cca03bf01d1a149c`  
		Last Modified: Thu, 13 Jun 2024 01:03:01 GMT  
		Size: 22.9 MB (22944997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2f2e243171f4163b5037b1bcf6c2bc90be788f5a944d7b2ef8d1ad32f64012f`  
		Last Modified: Thu, 13 Jun 2024 08:36:53 GMT  
		Size: 2.4 MB (2370411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf14cd536965f05b51ee4f1e379cda295071d3bf204fcefd378b8e08dd9d7776`  
		Last Modified: Thu, 13 Jun 2024 08:36:57 GMT  
		Size: 23.8 MB (23816031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56fcde8e253ae8fe8ff09311561e73ac906a5978f76a314f9dee8ac3cd0f9fb0`  
		Last Modified: Thu, 13 Jun 2024 08:38:05 GMT  
		Size: 127.8 MB (127825438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0.104` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:55d24011cec396844b9ae537ca5df01446d6e83715aebcc2c398863a33f40f80
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.8 MB (203824717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aac85fdbee98fe73bd2017cf5949eadab47b515ad98598c6d98dcba6d6d86833`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:40:19 GMT
ADD file:de9a2b323e6d7d969277e7e781875e3daf3f49f2c1dcc569a1eec4f5bd789c46 in / 
# Thu, 13 Jun 2024 00:40:19 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 02:40:28 GMT
ENV MONO_VERSION=6.10.0.104
# Thu, 13 Jun 2024 02:40:35 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 13 Jun 2024 02:40:50 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 13 Jun 2024 02:44:18 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7abf9f73c7747bb840a8edcd895830e53f09498136de3015568a9cd9f5ab10ed`  
		Last Modified: Thu, 13 Jun 2024 00:44:26 GMT  
		Size: 26.1 MB (26109272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:879958e785e6e477c521bba5e76ed1f61399ef247e4ae1218c778adfe5b38160`  
		Last Modified: Thu, 13 Jun 2024 02:44:57 GMT  
		Size: 2.6 MB (2645504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98651d9c2b89ddac9896e0807df9859069b12ace5592e15653ca94df208438d4`  
		Last Modified: Thu, 13 Jun 2024 02:45:00 GMT  
		Size: 29.6 MB (29574983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3432ee081e7eeffb9ccc5d4a2939025b406b9678c395c72df9b2c374fc603d82`  
		Last Modified: Thu, 13 Jun 2024 02:45:58 GMT  
		Size: 145.5 MB (145494958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0.104` - linux; 386

```console
$ docker pull mono@sha256:1ff9e0605a84ebc9c1425cf380fa6538513957f14ff53668bb1415bc0de06276
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.8 MB (230808213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:165beb97a02082ea41ab2c93bf8061f5337e9c3e47d92a7c3fdbb3d91c05cf4f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Nov 2021 20:21:03 GMT
ADD file:7bc8fc617f718bf5e65e7fd718531a01122acc1783af5233c98aa9d31b0f093e in / 
# Tue, 23 Nov 2021 20:21:03 GMT
CMD ["bash"]
# Tue, 23 Nov 2021 20:21:03 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 23 Nov 2021 20:21:03 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr # buildkit
# Tue, 23 Nov 2021 20:21:03 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
# Tue, 23 Nov 2021 20:21:03 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
```

-	Layers:
	-	`sha256:1dfc643447ff7a82c599b429eda0d998c6dbad4ab2786eed580821b5b888204e`  
		Last Modified: Thu, 13 Jun 2024 00:44:44 GMT  
		Size: 28.0 MB (27994640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1fd38227c501a8e3a4c2ddbc366821c42ebe8fad426425d041d37315dd39d6b`  
		Last Modified: Fri, 21 Jun 2024 01:03:29 GMT  
		Size: 2.8 MB (2791746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69732935ca2831417791f9677707cd4ac5cce2cc5ceac6ccf0939905aa577562`  
		Last Modified: Fri, 21 Jun 2024 01:03:31 GMT  
		Size: 68.6 MB (68593059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af0ac94ccf1051dd80381d13771eba83828ecbdd644eca8d13963217a4fcad77`  
		Last Modified: Fri, 21 Jun 2024 02:02:45 GMT  
		Size: 131.4 MB (131428768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mono:6.10.0.104` - unknown; unknown

```console
$ docker pull mono@sha256:219a320599f64567f69e1dd47dcf68ea4ca8e9a382081f8459ea5df8f38492ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.0 MB (10997669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a69753b371d3937f23742ab4adf60505bc438fff530ce728a4cc8e30701256d`

```dockerfile
```

-	Layers:
	-	`sha256:9b3055c084df3c88817dd92cc8a2a1626a67e7926baf283baef3da5734e362cf`  
		Last Modified: Fri, 21 Jun 2024 02:02:42 GMT  
		Size: 11.0 MB (10990366 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7af35d4525a5846d4e984a6519b904a3595ee966a75f1a1f352401f5074bcc2`  
		Last Modified: Fri, 21 Jun 2024 02:02:42 GMT  
		Size: 7.3 KB (7303 bytes)  
		MIME: application/vnd.in-toto+json

### `mono:6.10.0.104` - linux; ppc64le

```console
$ docker pull mono@sha256:6126f0b2219e750b391e2e0d63ac7a2df863d9e2356c43fba06fee0708676038
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.7 MB (209715776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e4e952c22c47db9a79c5ca425c7de3d576d719e2042713424b88a3dae8e5129`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:04 GMT
ADD file:6d33ba25d3625e5f445fc2183b60c64e2cbc780cb541d7f8ac76ce193b311d13 in / 
# Tue, 02 Aug 2022 01:18:06 GMT
CMD ["bash"]
# Wed, 03 Aug 2022 02:08:58 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 03 Aug 2022 02:09:16 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 03 Aug 2022 02:09:49 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 03 Aug 2022 02:14:18 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:fc8842eebb7ccaf249b2bb2d6a3878fffdae26c9db8f23b393c7f76a6249d2f6`  
		Last Modified: Tue, 02 Aug 2022 01:25:45 GMT  
		Size: 30.6 MB (30560308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c0b96bc274eefbc8d34a02735b6f704f29aaf7e6c4095edb588a74c1ffb2825`  
		Last Modified: Wed, 03 Aug 2022 02:15:49 GMT  
		Size: 2.9 MB (2892610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7f103eac188d225f1b73fa0b0d6a3f2560c7fc46d7ec0f0e7e7a07330eb1ff0`  
		Last Modified: Wed, 03 Aug 2022 02:16:04 GMT  
		Size: 41.8 MB (41839360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3a64f5c66cdaf23afe83539fd8177bddc2e783d6ca6ee6eb3cabd08a6a5c375`  
		Last Modified: Wed, 03 Aug 2022 02:17:54 GMT  
		Size: 134.4 MB (134423498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.10.0.104-slim`

```console
$ docker pull mono@sha256:997252b188a7de167d4e81924def4fff75b83b9af264581b426e26f590c1cbcc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le

### `mono:6.10.0.104-slim` - linux; amd64

```console
$ docker pull mono@sha256:814dbcff677039e433ef2250b3f89b944e891faf2655a84e5fb9e24e832b20a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.7 MB (94681329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23a4fb2221d45ec07871359574d68e579e293dd9212fa65bb61dc818d9c79a73`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Nov 2021 20:21:03 GMT
ADD file:cce4de1623245f9f28e3365e6cf749d85dcfedddea2d6fbc963c309a40818f52 in / 
# Tue, 23 Nov 2021 20:21:03 GMT
CMD ["bash"]
# Tue, 23 Nov 2021 20:21:03 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 23 Nov 2021 20:21:03 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr # buildkit
# Tue, 23 Nov 2021 20:21:03 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
```

-	Layers:
	-	`sha256:b338562f40a7fb7360dfae935da6d7e40d2545db18bc461d9d70ec1b2b657f33`  
		Last Modified: Thu, 13 Jun 2024 01:26:49 GMT  
		Size: 27.3 MB (27337703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17858d27bab2d3cac617525d602bdb6430ef30203a5879d871c8ac9c5ed9ccc3`  
		Last Modified: Fri, 21 Jun 2024 01:03:10 GMT  
		Size: 2.8 MB (2780056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95304a756dfd5de0e2f44edffff0c73d65982f8523d664fd5f1d97ea84d3fba5`  
		Last Modified: Fri, 21 Jun 2024 01:03:11 GMT  
		Size: 64.6 MB (64563570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mono:6.10.0.104-slim` - unknown; unknown

```console
$ docker pull mono@sha256:491d5d49289d1b9a5bc4b07908d133d9cb48ef0683dcc08baefbf6f5811aff98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4132989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6ced6d0d7431bd499931fcee411750b9a8e9490f620918b716c506ac384aaa1`

```dockerfile
```

-	Layers:
	-	`sha256:f0b4de9e8b45105e3a7b5b7820ec78abe67d446be81e23c068710fa4467ce393`  
		Last Modified: Fri, 21 Jun 2024 01:03:10 GMT  
		Size: 4.1 MB (4123463 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fbb819f516836e26bb95911256c4b78f388e9c1de432e7a3639d7164f01e7d29`  
		Last Modified: Fri, 21 Jun 2024 01:03:10 GMT  
		Size: 9.5 KB (9526 bytes)  
		MIME: application/vnd.in-toto+json

### `mono:6.10.0.104-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:9d52e2f9db76c24f9964eec255de917d7a05b180e6e45f98545846b130400ab6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.9 MB (51879316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccac5ddbcee195ea38a9828f45d157f2ef674624fb9a6a2d5529fc2f8e6b736a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 00:49:37 GMT
ADD file:2ed7ca0d45c68b46a10ae186e8a03f98e72cadfeed17105668f53adf14d31e1f in / 
# Tue, 02 Aug 2022 00:49:38 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 07:18:54 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 01 Mar 2023 07:19:03 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 01 Mar 2023 07:19:22 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:187ecffbd1e0eae5de6567dff32bd58f28623635657779760c9d9539d6b7cc59`  
		Last Modified: Tue, 02 Aug 2022 00:57:06 GMT  
		Size: 24.9 MB (24889750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb25ee9d7e5ee2ba3d5fe6104206a45f2c5c425365a535e0aaac7bb9bd71034e`  
		Last Modified: Wed, 01 Mar 2023 07:23:36 GMT  
		Size: 2.5 MB (2467730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4b5b10e99353e19dd9c56deed1fd46d8ffc3c3eb2ad78b8d36ac029a085764e`  
		Last Modified: Wed, 01 Mar 2023 07:23:40 GMT  
		Size: 24.5 MB (24521836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0.104-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:f788e39c64bc81a99ebc71841cfdb44616b8a780cdf7d6c4103a07590c4ed13d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49131439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9da1f749b46b22975ae899c2925624b519c409162edbca3067a515980114bd9a`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:58:15 GMT
ADD file:ab786d88497f915679b3ac228e3bd805a58501dcb33b3d25e49cf1898770f9a7 in / 
# Thu, 13 Jun 2024 00:58:15 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 08:31:58 GMT
ENV MONO_VERSION=6.10.0.104
# Thu, 13 Jun 2024 08:32:08 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 13 Jun 2024 08:32:30 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:99d1ebcdd364332a1427098feecc8f94a8978ec971b171f7cca03bf01d1a149c`  
		Last Modified: Thu, 13 Jun 2024 01:03:01 GMT  
		Size: 22.9 MB (22944997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2f2e243171f4163b5037b1bcf6c2bc90be788f5a944d7b2ef8d1ad32f64012f`  
		Last Modified: Thu, 13 Jun 2024 08:36:53 GMT  
		Size: 2.4 MB (2370411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf14cd536965f05b51ee4f1e379cda295071d3bf204fcefd378b8e08dd9d7776`  
		Last Modified: Thu, 13 Jun 2024 08:36:57 GMT  
		Size: 23.8 MB (23816031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0.104-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:2586824f4404d8e6252193767366b20681c79d29284065c7fcad3fae0e2a0210
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.3 MB (58329759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c5abbcbdafdf051b7b9510d4392cdd8fe76a592ba0cc6aef61f2915f09843df`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:40:19 GMT
ADD file:de9a2b323e6d7d969277e7e781875e3daf3f49f2c1dcc569a1eec4f5bd789c46 in / 
# Thu, 13 Jun 2024 00:40:19 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 02:40:28 GMT
ENV MONO_VERSION=6.10.0.104
# Thu, 13 Jun 2024 02:40:35 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 13 Jun 2024 02:40:50 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7abf9f73c7747bb840a8edcd895830e53f09498136de3015568a9cd9f5ab10ed`  
		Last Modified: Thu, 13 Jun 2024 00:44:26 GMT  
		Size: 26.1 MB (26109272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:879958e785e6e477c521bba5e76ed1f61399ef247e4ae1218c778adfe5b38160`  
		Last Modified: Thu, 13 Jun 2024 02:44:57 GMT  
		Size: 2.6 MB (2645504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98651d9c2b89ddac9896e0807df9859069b12ace5592e15653ca94df208438d4`  
		Last Modified: Thu, 13 Jun 2024 02:45:00 GMT  
		Size: 29.6 MB (29574983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0.104-slim` - linux; 386

```console
$ docker pull mono@sha256:7e31f221c58cec452ee510c920dfbf8012b4ca33614cb6bc3d8d592e1ea87cfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.4 MB (99379445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89f170f621f13cadeb2e8c70c95a554eb5d0fda433dc2465673365d3d3d9b047`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Nov 2021 20:21:03 GMT
ADD file:7bc8fc617f718bf5e65e7fd718531a01122acc1783af5233c98aa9d31b0f093e in / 
# Tue, 23 Nov 2021 20:21:03 GMT
CMD ["bash"]
# Tue, 23 Nov 2021 20:21:03 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 23 Nov 2021 20:21:03 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr # buildkit
# Tue, 23 Nov 2021 20:21:03 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
```

-	Layers:
	-	`sha256:1dfc643447ff7a82c599b429eda0d998c6dbad4ab2786eed580821b5b888204e`  
		Last Modified: Thu, 13 Jun 2024 00:44:44 GMT  
		Size: 28.0 MB (27994640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1fd38227c501a8e3a4c2ddbc366821c42ebe8fad426425d041d37315dd39d6b`  
		Last Modified: Fri, 21 Jun 2024 01:03:29 GMT  
		Size: 2.8 MB (2791746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69732935ca2831417791f9677707cd4ac5cce2cc5ceac6ccf0939905aa577562`  
		Last Modified: Fri, 21 Jun 2024 01:03:31 GMT  
		Size: 68.6 MB (68593059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mono:6.10.0.104-slim` - unknown; unknown

```console
$ docker pull mono@sha256:af2cca3ede0f45937d1f08bea05e1e69c4ffa371a4c56eb56df016825486e19a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4129139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd3ff001a6d90676b013ef8d12dd787c62ec6e8d2b16046c50c0b07cfde1bfa6`

```dockerfile
```

-	Layers:
	-	`sha256:1ed57169d510571d116c2eb97578bcb8bc86e9f5a81d45fa519f2dcbf6a70c18`  
		Last Modified: Fri, 21 Jun 2024 01:03:29 GMT  
		Size: 4.1 MB (4119639 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:058644825e2ae60ddee3857e80f06301c1446a83d3108a8d7539f9337ec24f79`  
		Last Modified: Fri, 21 Jun 2024 01:03:29 GMT  
		Size: 9.5 KB (9500 bytes)  
		MIME: application/vnd.in-toto+json

### `mono:6.10.0.104-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:defa2f8c047d839e590b97fb1b9652e93b82414d17f8dea7279f1bc0f467fcf0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.3 MB (75292278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98e30e35a5de236a142e7288a3c84a86005d1c742b41498b3f75a9f26b3a76ca`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:04 GMT
ADD file:6d33ba25d3625e5f445fc2183b60c64e2cbc780cb541d7f8ac76ce193b311d13 in / 
# Tue, 02 Aug 2022 01:18:06 GMT
CMD ["bash"]
# Wed, 03 Aug 2022 02:08:58 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 03 Aug 2022 02:09:16 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 03 Aug 2022 02:09:49 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:fc8842eebb7ccaf249b2bb2d6a3878fffdae26c9db8f23b393c7f76a6249d2f6`  
		Last Modified: Tue, 02 Aug 2022 01:25:45 GMT  
		Size: 30.6 MB (30560308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c0b96bc274eefbc8d34a02735b6f704f29aaf7e6c4095edb588a74c1ffb2825`  
		Last Modified: Wed, 03 Aug 2022 02:15:49 GMT  
		Size: 2.9 MB (2892610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7f103eac188d225f1b73fa0b0d6a3f2560c7fc46d7ec0f0e7e7a07330eb1ff0`  
		Last Modified: Wed, 03 Aug 2022 02:16:04 GMT  
		Size: 41.8 MB (41839360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.12`

```console
$ docker pull mono@sha256:122a14d6bb94876a6584fc7dc27acf61fdcce1b612442f6a27c4e6adbe57bd50
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le

### `mono:6.12` - linux; amd64

```console
$ docker pull mono@sha256:d2ae1881a608fb6401bcebbf0d444fc2fcadf0db27f07c87153a79e7b14e861a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.6 MB (254589877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16d98cfcc673531288833a5cdb9f87087aa18082d1fed9ebe02021c67b1fdf0f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jun 2022 16:43:21 GMT
ADD file:cce4de1623245f9f28e3365e6cf749d85dcfedddea2d6fbc963c309a40818f52 in / 
# Wed, 22 Jun 2022 16:43:21 GMT
CMD ["bash"]
# Wed, 22 Jun 2022 16:43:21 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 22 Jun 2022 16:43:21 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr # buildkit
# Wed, 22 Jun 2022 16:43:21 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
# Wed, 22 Jun 2022 16:43:21 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
```

-	Layers:
	-	`sha256:b338562f40a7fb7360dfae935da6d7e40d2545db18bc461d9d70ec1b2b657f33`  
		Last Modified: Thu, 13 Jun 2024 01:26:49 GMT  
		Size: 27.3 MB (27337703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b1b752ddf75c64e105424fb16f5a2053ddad33f059e3be8e520e35908cc4e97`  
		Last Modified: Fri, 21 Jun 2024 01:03:10 GMT  
		Size: 2.8 MB (2780035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d574eb224b5ddbe14656e28913cf5eeb5b14aa651aa3bcb9288aa43f1000aec5`  
		Last Modified: Fri, 21 Jun 2024 01:03:11 GMT  
		Size: 64.6 MB (64555923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb9d6fb145c5367510a78273891d0ba84d7257b0bfdf3cd340f4e3d6f211de0a`  
		Last Modified: Fri, 21 Jun 2024 02:02:49 GMT  
		Size: 159.9 MB (159916216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mono:6.12` - unknown; unknown

```console
$ docker pull mono@sha256:fc661c46136b8f9cbe60f721c811fb05d600f7614c9ddef8306ca5a261a6ea24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11085967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6322617bf4f258627a38887597f3d55cd3e73d36de6aa5f4734d1d6fcd3e7fd9`

```dockerfile
```

-	Layers:
	-	`sha256:08c2cae238c884d7e44ae9bd57336a51412c9603e15025c0a456eca7dd888aba`  
		Last Modified: Fri, 21 Jun 2024 02:02:46 GMT  
		Size: 11.1 MB (11078059 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2dda4ada58791fac758ee1dc7c9ee2756a6d55125463cc11427657bfedecb286`  
		Last Modified: Fri, 21 Jun 2024 02:02:46 GMT  
		Size: 7.9 KB (7908 bytes)  
		MIME: application/vnd.in-toto+json

### `mono:6.12` - linux; arm variant v5

```console
$ docker pull mono@sha256:dea4d3a6cf8d83cd0b747ac36b0b7a279de919c38227c259e8f0dd933ad99d3d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.9 MB (192868079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52646a30a3e2966b0a92b143b872a725a0eaa3c003a2b6c3030454d2f5f26220`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 00:49:37 GMT
ADD file:2ed7ca0d45c68b46a10ae186e8a03f98e72cadfeed17105668f53adf14d31e1f in / 
# Tue, 02 Aug 2022 00:49:38 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 07:17:55 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 01 Mar 2023 07:18:17 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 01 Mar 2023 07:18:42 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 01 Mar 2023 07:20:53 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:187ecffbd1e0eae5de6567dff32bd58f28623635657779760c9d9539d6b7cc59`  
		Last Modified: Tue, 02 Aug 2022 00:57:06 GMT  
		Size: 24.9 MB (24889750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6702eef9c7d9ec6ede2c5f9a15a047b314ccc9140f25694f337c0127478bb25b`  
		Last Modified: Wed, 01 Mar 2023 07:23:12 GMT  
		Size: 2.5 MB (2467715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3781ed66d8db4f1e7c7b6323f62af11c65550a10f339ad7c0fb68f9467f8026d`  
		Last Modified: Wed, 01 Mar 2023 07:23:17 GMT  
		Size: 24.5 MB (24503499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f32f45a77bbef0505ff02ad954c1ce25d1cb8f5b668bbd7c73fa538966d0c0b`  
		Last Modified: Wed, 01 Mar 2023 07:24:21 GMT  
		Size: 141.0 MB (141007115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12` - linux; arm variant v7

```console
$ docker pull mono@sha256:0dfc1dd87793c5f9c7d9197edaa5bf64b13fd37064afba0ac721ecd09f554a22
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.2 MB (189174773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ed768bb4ba02e014621f121844e472e5e513d725bdf417d80780af7b0938c6e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:58:15 GMT
ADD file:ab786d88497f915679b3ac228e3bd805a58501dcb33b3d25e49cf1898770f9a7 in / 
# Thu, 13 Jun 2024 00:58:15 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 08:31:10 GMT
ENV MONO_VERSION=6.12.0.182
# Thu, 13 Jun 2024 08:31:24 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 13 Jun 2024 08:31:48 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 13 Jun 2024 08:34:33 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:99d1ebcdd364332a1427098feecc8f94a8978ec971b171f7cca03bf01d1a149c`  
		Last Modified: Thu, 13 Jun 2024 01:03:01 GMT  
		Size: 22.9 MB (22944997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b7db2a28ee4fa8f5e893c5ca0f653dc9514221149d19d3632816e874498e112`  
		Last Modified: Thu, 13 Jun 2024 08:36:36 GMT  
		Size: 2.4 MB (2370421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f10ac972dcba288ded8e2044b27a0cdf74494394d8408e9383d92fce7e867d7`  
		Last Modified: Thu, 13 Jun 2024 08:36:40 GMT  
		Size: 23.8 MB (23790340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bd48720e38dbaaaef8fb759054f29f92b12cbbea01eab398573da7dac4160a3`  
		Last Modified: Thu, 13 Jun 2024 08:37:30 GMT  
		Size: 140.1 MB (140069015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:83a8328a667e7c0256a9832d8a8f2a3ccb189ac80da5ef1737a9b0d1c34d80ab
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.6 MB (216552576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ca3c4505019d48c31f72bda38a3d30a9661510b2d90cc6407c5585d49362028`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:40:19 GMT
ADD file:de9a2b323e6d7d969277e7e781875e3daf3f49f2c1dcc569a1eec4f5bd789c46 in / 
# Thu, 13 Jun 2024 00:40:19 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 02:40:00 GMT
ENV MONO_VERSION=6.12.0.182
# Thu, 13 Jun 2024 02:40:07 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 13 Jun 2024 02:40:22 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 13 Jun 2024 02:43:03 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7abf9f73c7747bb840a8edcd895830e53f09498136de3015568a9cd9f5ab10ed`  
		Last Modified: Thu, 13 Jun 2024 00:44:26 GMT  
		Size: 26.1 MB (26109272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0b5b6710e68b3b250dd681138cde05cf6596b6f323c42d994db4dcdb4761526`  
		Last Modified: Thu, 13 Jun 2024 02:44:41 GMT  
		Size: 2.6 MB (2645492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd67156f41b6153be4d7339a8c26d81d9648cfb9a9e365f2486f34aa6f6f507f`  
		Last Modified: Thu, 13 Jun 2024 02:44:44 GMT  
		Size: 29.5 MB (29544907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0091f5b1c3c6fe88db8dcb2b7849fe146d7c3571535910ff86aef81e76776d8`  
		Last Modified: Thu, 13 Jun 2024 02:45:28 GMT  
		Size: 158.3 MB (158252905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12` - linux; 386

```console
$ docker pull mono@sha256:8f10891be25745681bd6f98bf48e1234094816dc4b5dbef73d48f53f67536601
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.5 MB (259458549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2775d67ed2568bc292fd99d9a4c6e6e31195ae5382d5d3f1d76cb0f034c34e5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jun 2022 16:43:21 GMT
ADD file:7bc8fc617f718bf5e65e7fd718531a01122acc1783af5233c98aa9d31b0f093e in / 
# Wed, 22 Jun 2022 16:43:21 GMT
CMD ["bash"]
# Wed, 22 Jun 2022 16:43:21 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 22 Jun 2022 16:43:21 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr # buildkit
# Wed, 22 Jun 2022 16:43:21 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
# Wed, 22 Jun 2022 16:43:21 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
```

-	Layers:
	-	`sha256:1dfc643447ff7a82c599b429eda0d998c6dbad4ab2786eed580821b5b888204e`  
		Last Modified: Thu, 13 Jun 2024 00:44:44 GMT  
		Size: 28.0 MB (27994640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a198cb1aaae91cef3ed2eaed184c0a10f0b74e857bd5ea91dcde2955746f20f9`  
		Last Modified: Fri, 21 Jun 2024 01:03:12 GMT  
		Size: 2.8 MB (2791765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd658841b3e1b2084a6340e82f84033bf765e9ea9830350aa5a4aba88cbf3166`  
		Last Modified: Fri, 21 Jun 2024 01:03:14 GMT  
		Size: 68.6 MB (68585515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30bbf7033252959af4d7a4d2f468bba517cf0aeaf9f9e131902187bdc9737e6d`  
		Last Modified: Fri, 21 Jun 2024 02:04:03 GMT  
		Size: 160.1 MB (160086629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mono:6.12` - unknown; unknown

```console
$ docker pull mono@sha256:e69c4a0ff0efcd311f3ec0da7e72cbafaa9689b8555686674db7d3d689e13230
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11081926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48b0f05b8c3e2ec0bdb3fcbf2f85778a7584ea1dfd621e838399e99f0e6aac47`

```dockerfile
```

-	Layers:
	-	`sha256:f5bc84e8ea570b2500296b1f25f4226e60f0c15178c4ed81b09fa2c5ddf35fc6`  
		Last Modified: Fri, 21 Jun 2024 02:03:58 GMT  
		Size: 11.1 MB (11074056 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f11f469c7181081a082c334f89f2885f7a6a0953d5e152e5f75db2af4504d80e`  
		Last Modified: Fri, 21 Jun 2024 02:03:57 GMT  
		Size: 7.9 KB (7870 bytes)  
		MIME: application/vnd.in-toto+json

### `mono:6.12` - linux; ppc64le

```console
$ docker pull mono@sha256:fbfb5b60906856f25cc0ffb3ed273fa5da089aed24eab6afb049cc150c221768
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.7 MB (221654331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45a10e5a16545c25df57d5cf1f034acbb78fb5a3c968378416dc576fa88386ef`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:04 GMT
ADD file:6d33ba25d3625e5f445fc2183b60c64e2cbc780cb541d7f8ac76ce193b311d13 in / 
# Tue, 02 Aug 2022 01:18:06 GMT
CMD ["bash"]
# Wed, 03 Aug 2022 02:07:46 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 03 Aug 2022 02:08:06 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 03 Aug 2022 02:08:41 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 03 Aug 2022 02:11:40 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:fc8842eebb7ccaf249b2bb2d6a3878fffdae26c9db8f23b393c7f76a6249d2f6`  
		Last Modified: Tue, 02 Aug 2022 01:25:45 GMT  
		Size: 30.6 MB (30560308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1100971c8a3b3eb42c6e22a4c25f405143f007bda60d16697d49b333925b4d84`  
		Last Modified: Wed, 03 Aug 2022 02:15:13 GMT  
		Size: 2.9 MB (2892658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:390f883f1594b5d2d40b7ba4dc50f375439dd1611f38f0c3d071a38bf2ac62cd`  
		Last Modified: Wed, 03 Aug 2022 02:15:27 GMT  
		Size: 41.9 MB (41897345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ae94af697c95b6bf75033b813f19ec72f68da49a681d5ce7078753923129147`  
		Last Modified: Wed, 03 Aug 2022 02:16:58 GMT  
		Size: 146.3 MB (146304020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.12-slim`

```console
$ docker pull mono@sha256:d124eebf64f110db652f42c9e1e4a0627f84b6fc375ea3801751f7edcc74711b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le

### `mono:6.12-slim` - linux; amd64

```console
$ docker pull mono@sha256:749851d74745492754d1ebb3c50fc335d4b84a7bb34e17a4e7c3909c5ec1212b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.7 MB (94673661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5a2a70110040ee175a00069fa147d036d49deb2decd03a6374e83da337706e8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jun 2022 16:43:21 GMT
ADD file:cce4de1623245f9f28e3365e6cf749d85dcfedddea2d6fbc963c309a40818f52 in / 
# Wed, 22 Jun 2022 16:43:21 GMT
CMD ["bash"]
# Wed, 22 Jun 2022 16:43:21 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 22 Jun 2022 16:43:21 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr # buildkit
# Wed, 22 Jun 2022 16:43:21 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
```

-	Layers:
	-	`sha256:b338562f40a7fb7360dfae935da6d7e40d2545db18bc461d9d70ec1b2b657f33`  
		Last Modified: Thu, 13 Jun 2024 01:26:49 GMT  
		Size: 27.3 MB (27337703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b1b752ddf75c64e105424fb16f5a2053ddad33f059e3be8e520e35908cc4e97`  
		Last Modified: Fri, 21 Jun 2024 01:03:10 GMT  
		Size: 2.8 MB (2780035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d574eb224b5ddbe14656e28913cf5eeb5b14aa651aa3bcb9288aa43f1000aec5`  
		Last Modified: Fri, 21 Jun 2024 01:03:11 GMT  
		Size: 64.6 MB (64555923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mono:6.12-slim` - unknown; unknown

```console
$ docker pull mono@sha256:5a8421c386b586f98034983cc67448394e910e05ff857862418296991eddcf54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4134119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7daf4a5e106256a64c61c2f6e62ec4e5aa7020398e1b40c8bbe8b4e7458bec8d`

```dockerfile
```

-	Layers:
	-	`sha256:68c0c6a6586378e1af3fd618d65a15dd0a69c3e36744d2db3c2a64b91f8842b8`  
		Last Modified: Fri, 21 Jun 2024 01:03:10 GMT  
		Size: 4.1 MB (4124009 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ec35e37e8929d1729d15f72eaafb529c88604e0eb2b568452d3927312850835`  
		Last Modified: Fri, 21 Jun 2024 01:03:10 GMT  
		Size: 10.1 KB (10110 bytes)  
		MIME: application/vnd.in-toto+json

### `mono:6.12-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:f7c133539fa6a4add7484e9c93bc9b62ec32236d4b619f320c20b3248fb4739a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.9 MB (51860964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe52652f149ceedc89ed0c0f70985fcd898b6cd5cc98aa6f99f9ca06fd83046c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 00:49:37 GMT
ADD file:2ed7ca0d45c68b46a10ae186e8a03f98e72cadfeed17105668f53adf14d31e1f in / 
# Tue, 02 Aug 2022 00:49:38 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 07:17:55 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 01 Mar 2023 07:18:17 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 01 Mar 2023 07:18:42 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:187ecffbd1e0eae5de6567dff32bd58f28623635657779760c9d9539d6b7cc59`  
		Last Modified: Tue, 02 Aug 2022 00:57:06 GMT  
		Size: 24.9 MB (24889750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6702eef9c7d9ec6ede2c5f9a15a047b314ccc9140f25694f337c0127478bb25b`  
		Last Modified: Wed, 01 Mar 2023 07:23:12 GMT  
		Size: 2.5 MB (2467715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3781ed66d8db4f1e7c7b6323f62af11c65550a10f339ad7c0fb68f9467f8026d`  
		Last Modified: Wed, 01 Mar 2023 07:23:17 GMT  
		Size: 24.5 MB (24503499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:beaab14b4de16ae0f14cb615383dddbe283523fbd00c8494f8a55ce1299ec4ce
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49105758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:053650949e0e3231b0c67fad4f4dd10e2cb9a84beb0a82569b203ce3a1716fbd`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:58:15 GMT
ADD file:ab786d88497f915679b3ac228e3bd805a58501dcb33b3d25e49cf1898770f9a7 in / 
# Thu, 13 Jun 2024 00:58:15 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 08:31:10 GMT
ENV MONO_VERSION=6.12.0.182
# Thu, 13 Jun 2024 08:31:24 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 13 Jun 2024 08:31:48 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:99d1ebcdd364332a1427098feecc8f94a8978ec971b171f7cca03bf01d1a149c`  
		Last Modified: Thu, 13 Jun 2024 01:03:01 GMT  
		Size: 22.9 MB (22944997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b7db2a28ee4fa8f5e893c5ca0f653dc9514221149d19d3632816e874498e112`  
		Last Modified: Thu, 13 Jun 2024 08:36:36 GMT  
		Size: 2.4 MB (2370421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f10ac972dcba288ded8e2044b27a0cdf74494394d8408e9383d92fce7e867d7`  
		Last Modified: Thu, 13 Jun 2024 08:36:40 GMT  
		Size: 23.8 MB (23790340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:f0cc2d1cdff3f4c9132e03486d350424d918e8a58e17997314a1de02a04b24fc
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.3 MB (58299671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7c7359194914e922baaffe35e36d41958cbdc56e1dfe1475fdeda11d4d860f0`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:40:19 GMT
ADD file:de9a2b323e6d7d969277e7e781875e3daf3f49f2c1dcc569a1eec4f5bd789c46 in / 
# Thu, 13 Jun 2024 00:40:19 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 02:40:00 GMT
ENV MONO_VERSION=6.12.0.182
# Thu, 13 Jun 2024 02:40:07 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 13 Jun 2024 02:40:22 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7abf9f73c7747bb840a8edcd895830e53f09498136de3015568a9cd9f5ab10ed`  
		Last Modified: Thu, 13 Jun 2024 00:44:26 GMT  
		Size: 26.1 MB (26109272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0b5b6710e68b3b250dd681138cde05cf6596b6f323c42d994db4dcdb4761526`  
		Last Modified: Thu, 13 Jun 2024 02:44:41 GMT  
		Size: 2.6 MB (2645492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd67156f41b6153be4d7339a8c26d81d9648cfb9a9e365f2486f34aa6f6f507f`  
		Last Modified: Thu, 13 Jun 2024 02:44:44 GMT  
		Size: 29.5 MB (29544907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12-slim` - linux; 386

```console
$ docker pull mono@sha256:819bc68ca415cdb49ad461b4afb9a27004e442878b2bbdefc8a67317bc5b2ddf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.4 MB (99371920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c360bfbb224cb22cd13ba52ccd63bc77562ef28647c535cd0a42518f0773a842`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jun 2022 16:43:21 GMT
ADD file:7bc8fc617f718bf5e65e7fd718531a01122acc1783af5233c98aa9d31b0f093e in / 
# Wed, 22 Jun 2022 16:43:21 GMT
CMD ["bash"]
# Wed, 22 Jun 2022 16:43:21 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 22 Jun 2022 16:43:21 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr # buildkit
# Wed, 22 Jun 2022 16:43:21 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
```

-	Layers:
	-	`sha256:1dfc643447ff7a82c599b429eda0d998c6dbad4ab2786eed580821b5b888204e`  
		Last Modified: Thu, 13 Jun 2024 00:44:44 GMT  
		Size: 28.0 MB (27994640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a198cb1aaae91cef3ed2eaed184c0a10f0b74e857bd5ea91dcde2955746f20f9`  
		Last Modified: Fri, 21 Jun 2024 01:03:12 GMT  
		Size: 2.8 MB (2791765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd658841b3e1b2084a6340e82f84033bf765e9ea9830350aa5a4aba88cbf3166`  
		Last Modified: Fri, 21 Jun 2024 01:03:14 GMT  
		Size: 68.6 MB (68585515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mono:6.12-slim` - unknown; unknown

```console
$ docker pull mono@sha256:21b839469b89df687807ffdd3f870708c16efa44a6b299510e9d6391ba6499fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4130249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80ef153a1ce2f246cf50247bdbe0e53a65f2eca1f65498fe5be40b5242f5f8b1`

```dockerfile
```

-	Layers:
	-	`sha256:053ce445b27e3a8e224b16a3d2a8cdc9dc1d84ebee53d08de3d37ec36d5de95c`  
		Last Modified: Fri, 21 Jun 2024 01:03:12 GMT  
		Size: 4.1 MB (4120175 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:190e2c58614be0d956b94cdc868f9beb77c2f2d8ef16c981339f2b2c23f56975`  
		Last Modified: Fri, 21 Jun 2024 01:03:12 GMT  
		Size: 10.1 KB (10074 bytes)  
		MIME: application/vnd.in-toto+json

### `mono:6.12-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:b83383e51874bbee097571b303be3299c87d7da8c4c6b0f4e067cfaa552ad925
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75350311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c28d9c810a28445dd3b5767c5be8a3a5c5f459f859498e49f59bb419b735510`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:04 GMT
ADD file:6d33ba25d3625e5f445fc2183b60c64e2cbc780cb541d7f8ac76ce193b311d13 in / 
# Tue, 02 Aug 2022 01:18:06 GMT
CMD ["bash"]
# Wed, 03 Aug 2022 02:07:46 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 03 Aug 2022 02:08:06 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 03 Aug 2022 02:08:41 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:fc8842eebb7ccaf249b2bb2d6a3878fffdae26c9db8f23b393c7f76a6249d2f6`  
		Last Modified: Tue, 02 Aug 2022 01:25:45 GMT  
		Size: 30.6 MB (30560308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1100971c8a3b3eb42c6e22a4c25f405143f007bda60d16697d49b333925b4d84`  
		Last Modified: Wed, 03 Aug 2022 02:15:13 GMT  
		Size: 2.9 MB (2892658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:390f883f1594b5d2d40b7ba4dc50f375439dd1611f38f0c3d071a38bf2ac62cd`  
		Last Modified: Wed, 03 Aug 2022 02:15:27 GMT  
		Size: 41.9 MB (41897345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.12.0`

```console
$ docker pull mono@sha256:122a14d6bb94876a6584fc7dc27acf61fdcce1b612442f6a27c4e6adbe57bd50
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le

### `mono:6.12.0` - linux; amd64

```console
$ docker pull mono@sha256:d2ae1881a608fb6401bcebbf0d444fc2fcadf0db27f07c87153a79e7b14e861a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.6 MB (254589877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16d98cfcc673531288833a5cdb9f87087aa18082d1fed9ebe02021c67b1fdf0f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jun 2022 16:43:21 GMT
ADD file:cce4de1623245f9f28e3365e6cf749d85dcfedddea2d6fbc963c309a40818f52 in / 
# Wed, 22 Jun 2022 16:43:21 GMT
CMD ["bash"]
# Wed, 22 Jun 2022 16:43:21 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 22 Jun 2022 16:43:21 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr # buildkit
# Wed, 22 Jun 2022 16:43:21 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
# Wed, 22 Jun 2022 16:43:21 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
```

-	Layers:
	-	`sha256:b338562f40a7fb7360dfae935da6d7e40d2545db18bc461d9d70ec1b2b657f33`  
		Last Modified: Thu, 13 Jun 2024 01:26:49 GMT  
		Size: 27.3 MB (27337703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b1b752ddf75c64e105424fb16f5a2053ddad33f059e3be8e520e35908cc4e97`  
		Last Modified: Fri, 21 Jun 2024 01:03:10 GMT  
		Size: 2.8 MB (2780035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d574eb224b5ddbe14656e28913cf5eeb5b14aa651aa3bcb9288aa43f1000aec5`  
		Last Modified: Fri, 21 Jun 2024 01:03:11 GMT  
		Size: 64.6 MB (64555923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb9d6fb145c5367510a78273891d0ba84d7257b0bfdf3cd340f4e3d6f211de0a`  
		Last Modified: Fri, 21 Jun 2024 02:02:49 GMT  
		Size: 159.9 MB (159916216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mono:6.12.0` - unknown; unknown

```console
$ docker pull mono@sha256:fc661c46136b8f9cbe60f721c811fb05d600f7614c9ddef8306ca5a261a6ea24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11085967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6322617bf4f258627a38887597f3d55cd3e73d36de6aa5f4734d1d6fcd3e7fd9`

```dockerfile
```

-	Layers:
	-	`sha256:08c2cae238c884d7e44ae9bd57336a51412c9603e15025c0a456eca7dd888aba`  
		Last Modified: Fri, 21 Jun 2024 02:02:46 GMT  
		Size: 11.1 MB (11078059 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2dda4ada58791fac758ee1dc7c9ee2756a6d55125463cc11427657bfedecb286`  
		Last Modified: Fri, 21 Jun 2024 02:02:46 GMT  
		Size: 7.9 KB (7908 bytes)  
		MIME: application/vnd.in-toto+json

### `mono:6.12.0` - linux; arm variant v5

```console
$ docker pull mono@sha256:dea4d3a6cf8d83cd0b747ac36b0b7a279de919c38227c259e8f0dd933ad99d3d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.9 MB (192868079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52646a30a3e2966b0a92b143b872a725a0eaa3c003a2b6c3030454d2f5f26220`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 00:49:37 GMT
ADD file:2ed7ca0d45c68b46a10ae186e8a03f98e72cadfeed17105668f53adf14d31e1f in / 
# Tue, 02 Aug 2022 00:49:38 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 07:17:55 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 01 Mar 2023 07:18:17 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 01 Mar 2023 07:18:42 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 01 Mar 2023 07:20:53 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:187ecffbd1e0eae5de6567dff32bd58f28623635657779760c9d9539d6b7cc59`  
		Last Modified: Tue, 02 Aug 2022 00:57:06 GMT  
		Size: 24.9 MB (24889750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6702eef9c7d9ec6ede2c5f9a15a047b314ccc9140f25694f337c0127478bb25b`  
		Last Modified: Wed, 01 Mar 2023 07:23:12 GMT  
		Size: 2.5 MB (2467715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3781ed66d8db4f1e7c7b6323f62af11c65550a10f339ad7c0fb68f9467f8026d`  
		Last Modified: Wed, 01 Mar 2023 07:23:17 GMT  
		Size: 24.5 MB (24503499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f32f45a77bbef0505ff02ad954c1ce25d1cb8f5b668bbd7c73fa538966d0c0b`  
		Last Modified: Wed, 01 Mar 2023 07:24:21 GMT  
		Size: 141.0 MB (141007115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0` - linux; arm variant v7

```console
$ docker pull mono@sha256:0dfc1dd87793c5f9c7d9197edaa5bf64b13fd37064afba0ac721ecd09f554a22
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.2 MB (189174773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ed768bb4ba02e014621f121844e472e5e513d725bdf417d80780af7b0938c6e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:58:15 GMT
ADD file:ab786d88497f915679b3ac228e3bd805a58501dcb33b3d25e49cf1898770f9a7 in / 
# Thu, 13 Jun 2024 00:58:15 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 08:31:10 GMT
ENV MONO_VERSION=6.12.0.182
# Thu, 13 Jun 2024 08:31:24 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 13 Jun 2024 08:31:48 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 13 Jun 2024 08:34:33 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:99d1ebcdd364332a1427098feecc8f94a8978ec971b171f7cca03bf01d1a149c`  
		Last Modified: Thu, 13 Jun 2024 01:03:01 GMT  
		Size: 22.9 MB (22944997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b7db2a28ee4fa8f5e893c5ca0f653dc9514221149d19d3632816e874498e112`  
		Last Modified: Thu, 13 Jun 2024 08:36:36 GMT  
		Size: 2.4 MB (2370421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f10ac972dcba288ded8e2044b27a0cdf74494394d8408e9383d92fce7e867d7`  
		Last Modified: Thu, 13 Jun 2024 08:36:40 GMT  
		Size: 23.8 MB (23790340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bd48720e38dbaaaef8fb759054f29f92b12cbbea01eab398573da7dac4160a3`  
		Last Modified: Thu, 13 Jun 2024 08:37:30 GMT  
		Size: 140.1 MB (140069015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:83a8328a667e7c0256a9832d8a8f2a3ccb189ac80da5ef1737a9b0d1c34d80ab
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.6 MB (216552576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ca3c4505019d48c31f72bda38a3d30a9661510b2d90cc6407c5585d49362028`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:40:19 GMT
ADD file:de9a2b323e6d7d969277e7e781875e3daf3f49f2c1dcc569a1eec4f5bd789c46 in / 
# Thu, 13 Jun 2024 00:40:19 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 02:40:00 GMT
ENV MONO_VERSION=6.12.0.182
# Thu, 13 Jun 2024 02:40:07 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 13 Jun 2024 02:40:22 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 13 Jun 2024 02:43:03 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7abf9f73c7747bb840a8edcd895830e53f09498136de3015568a9cd9f5ab10ed`  
		Last Modified: Thu, 13 Jun 2024 00:44:26 GMT  
		Size: 26.1 MB (26109272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0b5b6710e68b3b250dd681138cde05cf6596b6f323c42d994db4dcdb4761526`  
		Last Modified: Thu, 13 Jun 2024 02:44:41 GMT  
		Size: 2.6 MB (2645492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd67156f41b6153be4d7339a8c26d81d9648cfb9a9e365f2486f34aa6f6f507f`  
		Last Modified: Thu, 13 Jun 2024 02:44:44 GMT  
		Size: 29.5 MB (29544907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0091f5b1c3c6fe88db8dcb2b7849fe146d7c3571535910ff86aef81e76776d8`  
		Last Modified: Thu, 13 Jun 2024 02:45:28 GMT  
		Size: 158.3 MB (158252905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0` - linux; 386

```console
$ docker pull mono@sha256:8f10891be25745681bd6f98bf48e1234094816dc4b5dbef73d48f53f67536601
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.5 MB (259458549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2775d67ed2568bc292fd99d9a4c6e6e31195ae5382d5d3f1d76cb0f034c34e5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jun 2022 16:43:21 GMT
ADD file:7bc8fc617f718bf5e65e7fd718531a01122acc1783af5233c98aa9d31b0f093e in / 
# Wed, 22 Jun 2022 16:43:21 GMT
CMD ["bash"]
# Wed, 22 Jun 2022 16:43:21 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 22 Jun 2022 16:43:21 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr # buildkit
# Wed, 22 Jun 2022 16:43:21 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
# Wed, 22 Jun 2022 16:43:21 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
```

-	Layers:
	-	`sha256:1dfc643447ff7a82c599b429eda0d998c6dbad4ab2786eed580821b5b888204e`  
		Last Modified: Thu, 13 Jun 2024 00:44:44 GMT  
		Size: 28.0 MB (27994640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a198cb1aaae91cef3ed2eaed184c0a10f0b74e857bd5ea91dcde2955746f20f9`  
		Last Modified: Fri, 21 Jun 2024 01:03:12 GMT  
		Size: 2.8 MB (2791765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd658841b3e1b2084a6340e82f84033bf765e9ea9830350aa5a4aba88cbf3166`  
		Last Modified: Fri, 21 Jun 2024 01:03:14 GMT  
		Size: 68.6 MB (68585515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30bbf7033252959af4d7a4d2f468bba517cf0aeaf9f9e131902187bdc9737e6d`  
		Last Modified: Fri, 21 Jun 2024 02:04:03 GMT  
		Size: 160.1 MB (160086629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mono:6.12.0` - unknown; unknown

```console
$ docker pull mono@sha256:e69c4a0ff0efcd311f3ec0da7e72cbafaa9689b8555686674db7d3d689e13230
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11081926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48b0f05b8c3e2ec0bdb3fcbf2f85778a7584ea1dfd621e838399e99f0e6aac47`

```dockerfile
```

-	Layers:
	-	`sha256:f5bc84e8ea570b2500296b1f25f4226e60f0c15178c4ed81b09fa2c5ddf35fc6`  
		Last Modified: Fri, 21 Jun 2024 02:03:58 GMT  
		Size: 11.1 MB (11074056 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f11f469c7181081a082c334f89f2885f7a6a0953d5e152e5f75db2af4504d80e`  
		Last Modified: Fri, 21 Jun 2024 02:03:57 GMT  
		Size: 7.9 KB (7870 bytes)  
		MIME: application/vnd.in-toto+json

### `mono:6.12.0` - linux; ppc64le

```console
$ docker pull mono@sha256:fbfb5b60906856f25cc0ffb3ed273fa5da089aed24eab6afb049cc150c221768
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.7 MB (221654331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45a10e5a16545c25df57d5cf1f034acbb78fb5a3c968378416dc576fa88386ef`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:04 GMT
ADD file:6d33ba25d3625e5f445fc2183b60c64e2cbc780cb541d7f8ac76ce193b311d13 in / 
# Tue, 02 Aug 2022 01:18:06 GMT
CMD ["bash"]
# Wed, 03 Aug 2022 02:07:46 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 03 Aug 2022 02:08:06 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 03 Aug 2022 02:08:41 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 03 Aug 2022 02:11:40 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:fc8842eebb7ccaf249b2bb2d6a3878fffdae26c9db8f23b393c7f76a6249d2f6`  
		Last Modified: Tue, 02 Aug 2022 01:25:45 GMT  
		Size: 30.6 MB (30560308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1100971c8a3b3eb42c6e22a4c25f405143f007bda60d16697d49b333925b4d84`  
		Last Modified: Wed, 03 Aug 2022 02:15:13 GMT  
		Size: 2.9 MB (2892658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:390f883f1594b5d2d40b7ba4dc50f375439dd1611f38f0c3d071a38bf2ac62cd`  
		Last Modified: Wed, 03 Aug 2022 02:15:27 GMT  
		Size: 41.9 MB (41897345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ae94af697c95b6bf75033b813f19ec72f68da49a681d5ce7078753923129147`  
		Last Modified: Wed, 03 Aug 2022 02:16:58 GMT  
		Size: 146.3 MB (146304020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.12.0-slim`

```console
$ docker pull mono@sha256:d124eebf64f110db652f42c9e1e4a0627f84b6fc375ea3801751f7edcc74711b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le

### `mono:6.12.0-slim` - linux; amd64

```console
$ docker pull mono@sha256:749851d74745492754d1ebb3c50fc335d4b84a7bb34e17a4e7c3909c5ec1212b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.7 MB (94673661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5a2a70110040ee175a00069fa147d036d49deb2decd03a6374e83da337706e8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jun 2022 16:43:21 GMT
ADD file:cce4de1623245f9f28e3365e6cf749d85dcfedddea2d6fbc963c309a40818f52 in / 
# Wed, 22 Jun 2022 16:43:21 GMT
CMD ["bash"]
# Wed, 22 Jun 2022 16:43:21 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 22 Jun 2022 16:43:21 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr # buildkit
# Wed, 22 Jun 2022 16:43:21 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
```

-	Layers:
	-	`sha256:b338562f40a7fb7360dfae935da6d7e40d2545db18bc461d9d70ec1b2b657f33`  
		Last Modified: Thu, 13 Jun 2024 01:26:49 GMT  
		Size: 27.3 MB (27337703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b1b752ddf75c64e105424fb16f5a2053ddad33f059e3be8e520e35908cc4e97`  
		Last Modified: Fri, 21 Jun 2024 01:03:10 GMT  
		Size: 2.8 MB (2780035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d574eb224b5ddbe14656e28913cf5eeb5b14aa651aa3bcb9288aa43f1000aec5`  
		Last Modified: Fri, 21 Jun 2024 01:03:11 GMT  
		Size: 64.6 MB (64555923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mono:6.12.0-slim` - unknown; unknown

```console
$ docker pull mono@sha256:5a8421c386b586f98034983cc67448394e910e05ff857862418296991eddcf54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4134119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7daf4a5e106256a64c61c2f6e62ec4e5aa7020398e1b40c8bbe8b4e7458bec8d`

```dockerfile
```

-	Layers:
	-	`sha256:68c0c6a6586378e1af3fd618d65a15dd0a69c3e36744d2db3c2a64b91f8842b8`  
		Last Modified: Fri, 21 Jun 2024 01:03:10 GMT  
		Size: 4.1 MB (4124009 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ec35e37e8929d1729d15f72eaafb529c88604e0eb2b568452d3927312850835`  
		Last Modified: Fri, 21 Jun 2024 01:03:10 GMT  
		Size: 10.1 KB (10110 bytes)  
		MIME: application/vnd.in-toto+json

### `mono:6.12.0-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:f7c133539fa6a4add7484e9c93bc9b62ec32236d4b619f320c20b3248fb4739a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.9 MB (51860964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe52652f149ceedc89ed0c0f70985fcd898b6cd5cc98aa6f99f9ca06fd83046c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 00:49:37 GMT
ADD file:2ed7ca0d45c68b46a10ae186e8a03f98e72cadfeed17105668f53adf14d31e1f in / 
# Tue, 02 Aug 2022 00:49:38 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 07:17:55 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 01 Mar 2023 07:18:17 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 01 Mar 2023 07:18:42 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:187ecffbd1e0eae5de6567dff32bd58f28623635657779760c9d9539d6b7cc59`  
		Last Modified: Tue, 02 Aug 2022 00:57:06 GMT  
		Size: 24.9 MB (24889750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6702eef9c7d9ec6ede2c5f9a15a047b314ccc9140f25694f337c0127478bb25b`  
		Last Modified: Wed, 01 Mar 2023 07:23:12 GMT  
		Size: 2.5 MB (2467715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3781ed66d8db4f1e7c7b6323f62af11c65550a10f339ad7c0fb68f9467f8026d`  
		Last Modified: Wed, 01 Mar 2023 07:23:17 GMT  
		Size: 24.5 MB (24503499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:beaab14b4de16ae0f14cb615383dddbe283523fbd00c8494f8a55ce1299ec4ce
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49105758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:053650949e0e3231b0c67fad4f4dd10e2cb9a84beb0a82569b203ce3a1716fbd`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:58:15 GMT
ADD file:ab786d88497f915679b3ac228e3bd805a58501dcb33b3d25e49cf1898770f9a7 in / 
# Thu, 13 Jun 2024 00:58:15 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 08:31:10 GMT
ENV MONO_VERSION=6.12.0.182
# Thu, 13 Jun 2024 08:31:24 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 13 Jun 2024 08:31:48 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:99d1ebcdd364332a1427098feecc8f94a8978ec971b171f7cca03bf01d1a149c`  
		Last Modified: Thu, 13 Jun 2024 01:03:01 GMT  
		Size: 22.9 MB (22944997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b7db2a28ee4fa8f5e893c5ca0f653dc9514221149d19d3632816e874498e112`  
		Last Modified: Thu, 13 Jun 2024 08:36:36 GMT  
		Size: 2.4 MB (2370421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f10ac972dcba288ded8e2044b27a0cdf74494394d8408e9383d92fce7e867d7`  
		Last Modified: Thu, 13 Jun 2024 08:36:40 GMT  
		Size: 23.8 MB (23790340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:f0cc2d1cdff3f4c9132e03486d350424d918e8a58e17997314a1de02a04b24fc
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.3 MB (58299671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7c7359194914e922baaffe35e36d41958cbdc56e1dfe1475fdeda11d4d860f0`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:40:19 GMT
ADD file:de9a2b323e6d7d969277e7e781875e3daf3f49f2c1dcc569a1eec4f5bd789c46 in / 
# Thu, 13 Jun 2024 00:40:19 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 02:40:00 GMT
ENV MONO_VERSION=6.12.0.182
# Thu, 13 Jun 2024 02:40:07 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 13 Jun 2024 02:40:22 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7abf9f73c7747bb840a8edcd895830e53f09498136de3015568a9cd9f5ab10ed`  
		Last Modified: Thu, 13 Jun 2024 00:44:26 GMT  
		Size: 26.1 MB (26109272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0b5b6710e68b3b250dd681138cde05cf6596b6f323c42d994db4dcdb4761526`  
		Last Modified: Thu, 13 Jun 2024 02:44:41 GMT  
		Size: 2.6 MB (2645492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd67156f41b6153be4d7339a8c26d81d9648cfb9a9e365f2486f34aa6f6f507f`  
		Last Modified: Thu, 13 Jun 2024 02:44:44 GMT  
		Size: 29.5 MB (29544907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0-slim` - linux; 386

```console
$ docker pull mono@sha256:819bc68ca415cdb49ad461b4afb9a27004e442878b2bbdefc8a67317bc5b2ddf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.4 MB (99371920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c360bfbb224cb22cd13ba52ccd63bc77562ef28647c535cd0a42518f0773a842`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jun 2022 16:43:21 GMT
ADD file:7bc8fc617f718bf5e65e7fd718531a01122acc1783af5233c98aa9d31b0f093e in / 
# Wed, 22 Jun 2022 16:43:21 GMT
CMD ["bash"]
# Wed, 22 Jun 2022 16:43:21 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 22 Jun 2022 16:43:21 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr # buildkit
# Wed, 22 Jun 2022 16:43:21 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
```

-	Layers:
	-	`sha256:1dfc643447ff7a82c599b429eda0d998c6dbad4ab2786eed580821b5b888204e`  
		Last Modified: Thu, 13 Jun 2024 00:44:44 GMT  
		Size: 28.0 MB (27994640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a198cb1aaae91cef3ed2eaed184c0a10f0b74e857bd5ea91dcde2955746f20f9`  
		Last Modified: Fri, 21 Jun 2024 01:03:12 GMT  
		Size: 2.8 MB (2791765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd658841b3e1b2084a6340e82f84033bf765e9ea9830350aa5a4aba88cbf3166`  
		Last Modified: Fri, 21 Jun 2024 01:03:14 GMT  
		Size: 68.6 MB (68585515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mono:6.12.0-slim` - unknown; unknown

```console
$ docker pull mono@sha256:21b839469b89df687807ffdd3f870708c16efa44a6b299510e9d6391ba6499fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4130249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80ef153a1ce2f246cf50247bdbe0e53a65f2eca1f65498fe5be40b5242f5f8b1`

```dockerfile
```

-	Layers:
	-	`sha256:053ce445b27e3a8e224b16a3d2a8cdc9dc1d84ebee53d08de3d37ec36d5de95c`  
		Last Modified: Fri, 21 Jun 2024 01:03:12 GMT  
		Size: 4.1 MB (4120175 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:190e2c58614be0d956b94cdc868f9beb77c2f2d8ef16c981339f2b2c23f56975`  
		Last Modified: Fri, 21 Jun 2024 01:03:12 GMT  
		Size: 10.1 KB (10074 bytes)  
		MIME: application/vnd.in-toto+json

### `mono:6.12.0-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:b83383e51874bbee097571b303be3299c87d7da8c4c6b0f4e067cfaa552ad925
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75350311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c28d9c810a28445dd3b5767c5be8a3a5c5f459f859498e49f59bb419b735510`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:04 GMT
ADD file:6d33ba25d3625e5f445fc2183b60c64e2cbc780cb541d7f8ac76ce193b311d13 in / 
# Tue, 02 Aug 2022 01:18:06 GMT
CMD ["bash"]
# Wed, 03 Aug 2022 02:07:46 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 03 Aug 2022 02:08:06 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 03 Aug 2022 02:08:41 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:fc8842eebb7ccaf249b2bb2d6a3878fffdae26c9db8f23b393c7f76a6249d2f6`  
		Last Modified: Tue, 02 Aug 2022 01:25:45 GMT  
		Size: 30.6 MB (30560308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1100971c8a3b3eb42c6e22a4c25f405143f007bda60d16697d49b333925b4d84`  
		Last Modified: Wed, 03 Aug 2022 02:15:13 GMT  
		Size: 2.9 MB (2892658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:390f883f1594b5d2d40b7ba4dc50f375439dd1611f38f0c3d071a38bf2ac62cd`  
		Last Modified: Wed, 03 Aug 2022 02:15:27 GMT  
		Size: 41.9 MB (41897345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.12.0.182`

```console
$ docker pull mono@sha256:122a14d6bb94876a6584fc7dc27acf61fdcce1b612442f6a27c4e6adbe57bd50
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le

### `mono:6.12.0.182` - linux; amd64

```console
$ docker pull mono@sha256:d2ae1881a608fb6401bcebbf0d444fc2fcadf0db27f07c87153a79e7b14e861a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.6 MB (254589877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16d98cfcc673531288833a5cdb9f87087aa18082d1fed9ebe02021c67b1fdf0f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jun 2022 16:43:21 GMT
ADD file:cce4de1623245f9f28e3365e6cf749d85dcfedddea2d6fbc963c309a40818f52 in / 
# Wed, 22 Jun 2022 16:43:21 GMT
CMD ["bash"]
# Wed, 22 Jun 2022 16:43:21 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 22 Jun 2022 16:43:21 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr # buildkit
# Wed, 22 Jun 2022 16:43:21 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
# Wed, 22 Jun 2022 16:43:21 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
```

-	Layers:
	-	`sha256:b338562f40a7fb7360dfae935da6d7e40d2545db18bc461d9d70ec1b2b657f33`  
		Last Modified: Thu, 13 Jun 2024 01:26:49 GMT  
		Size: 27.3 MB (27337703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b1b752ddf75c64e105424fb16f5a2053ddad33f059e3be8e520e35908cc4e97`  
		Last Modified: Fri, 21 Jun 2024 01:03:10 GMT  
		Size: 2.8 MB (2780035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d574eb224b5ddbe14656e28913cf5eeb5b14aa651aa3bcb9288aa43f1000aec5`  
		Last Modified: Fri, 21 Jun 2024 01:03:11 GMT  
		Size: 64.6 MB (64555923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb9d6fb145c5367510a78273891d0ba84d7257b0bfdf3cd340f4e3d6f211de0a`  
		Last Modified: Fri, 21 Jun 2024 02:02:49 GMT  
		Size: 159.9 MB (159916216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mono:6.12.0.182` - unknown; unknown

```console
$ docker pull mono@sha256:fc661c46136b8f9cbe60f721c811fb05d600f7614c9ddef8306ca5a261a6ea24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11085967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6322617bf4f258627a38887597f3d55cd3e73d36de6aa5f4734d1d6fcd3e7fd9`

```dockerfile
```

-	Layers:
	-	`sha256:08c2cae238c884d7e44ae9bd57336a51412c9603e15025c0a456eca7dd888aba`  
		Last Modified: Fri, 21 Jun 2024 02:02:46 GMT  
		Size: 11.1 MB (11078059 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2dda4ada58791fac758ee1dc7c9ee2756a6d55125463cc11427657bfedecb286`  
		Last Modified: Fri, 21 Jun 2024 02:02:46 GMT  
		Size: 7.9 KB (7908 bytes)  
		MIME: application/vnd.in-toto+json

### `mono:6.12.0.182` - linux; arm variant v5

```console
$ docker pull mono@sha256:dea4d3a6cf8d83cd0b747ac36b0b7a279de919c38227c259e8f0dd933ad99d3d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.9 MB (192868079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52646a30a3e2966b0a92b143b872a725a0eaa3c003a2b6c3030454d2f5f26220`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 00:49:37 GMT
ADD file:2ed7ca0d45c68b46a10ae186e8a03f98e72cadfeed17105668f53adf14d31e1f in / 
# Tue, 02 Aug 2022 00:49:38 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 07:17:55 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 01 Mar 2023 07:18:17 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 01 Mar 2023 07:18:42 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 01 Mar 2023 07:20:53 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:187ecffbd1e0eae5de6567dff32bd58f28623635657779760c9d9539d6b7cc59`  
		Last Modified: Tue, 02 Aug 2022 00:57:06 GMT  
		Size: 24.9 MB (24889750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6702eef9c7d9ec6ede2c5f9a15a047b314ccc9140f25694f337c0127478bb25b`  
		Last Modified: Wed, 01 Mar 2023 07:23:12 GMT  
		Size: 2.5 MB (2467715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3781ed66d8db4f1e7c7b6323f62af11c65550a10f339ad7c0fb68f9467f8026d`  
		Last Modified: Wed, 01 Mar 2023 07:23:17 GMT  
		Size: 24.5 MB (24503499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f32f45a77bbef0505ff02ad954c1ce25d1cb8f5b668bbd7c73fa538966d0c0b`  
		Last Modified: Wed, 01 Mar 2023 07:24:21 GMT  
		Size: 141.0 MB (141007115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0.182` - linux; arm variant v7

```console
$ docker pull mono@sha256:0dfc1dd87793c5f9c7d9197edaa5bf64b13fd37064afba0ac721ecd09f554a22
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.2 MB (189174773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ed768bb4ba02e014621f121844e472e5e513d725bdf417d80780af7b0938c6e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:58:15 GMT
ADD file:ab786d88497f915679b3ac228e3bd805a58501dcb33b3d25e49cf1898770f9a7 in / 
# Thu, 13 Jun 2024 00:58:15 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 08:31:10 GMT
ENV MONO_VERSION=6.12.0.182
# Thu, 13 Jun 2024 08:31:24 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 13 Jun 2024 08:31:48 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 13 Jun 2024 08:34:33 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:99d1ebcdd364332a1427098feecc8f94a8978ec971b171f7cca03bf01d1a149c`  
		Last Modified: Thu, 13 Jun 2024 01:03:01 GMT  
		Size: 22.9 MB (22944997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b7db2a28ee4fa8f5e893c5ca0f653dc9514221149d19d3632816e874498e112`  
		Last Modified: Thu, 13 Jun 2024 08:36:36 GMT  
		Size: 2.4 MB (2370421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f10ac972dcba288ded8e2044b27a0cdf74494394d8408e9383d92fce7e867d7`  
		Last Modified: Thu, 13 Jun 2024 08:36:40 GMT  
		Size: 23.8 MB (23790340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bd48720e38dbaaaef8fb759054f29f92b12cbbea01eab398573da7dac4160a3`  
		Last Modified: Thu, 13 Jun 2024 08:37:30 GMT  
		Size: 140.1 MB (140069015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0.182` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:83a8328a667e7c0256a9832d8a8f2a3ccb189ac80da5ef1737a9b0d1c34d80ab
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.6 MB (216552576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ca3c4505019d48c31f72bda38a3d30a9661510b2d90cc6407c5585d49362028`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:40:19 GMT
ADD file:de9a2b323e6d7d969277e7e781875e3daf3f49f2c1dcc569a1eec4f5bd789c46 in / 
# Thu, 13 Jun 2024 00:40:19 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 02:40:00 GMT
ENV MONO_VERSION=6.12.0.182
# Thu, 13 Jun 2024 02:40:07 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 13 Jun 2024 02:40:22 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 13 Jun 2024 02:43:03 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7abf9f73c7747bb840a8edcd895830e53f09498136de3015568a9cd9f5ab10ed`  
		Last Modified: Thu, 13 Jun 2024 00:44:26 GMT  
		Size: 26.1 MB (26109272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0b5b6710e68b3b250dd681138cde05cf6596b6f323c42d994db4dcdb4761526`  
		Last Modified: Thu, 13 Jun 2024 02:44:41 GMT  
		Size: 2.6 MB (2645492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd67156f41b6153be4d7339a8c26d81d9648cfb9a9e365f2486f34aa6f6f507f`  
		Last Modified: Thu, 13 Jun 2024 02:44:44 GMT  
		Size: 29.5 MB (29544907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0091f5b1c3c6fe88db8dcb2b7849fe146d7c3571535910ff86aef81e76776d8`  
		Last Modified: Thu, 13 Jun 2024 02:45:28 GMT  
		Size: 158.3 MB (158252905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0.182` - linux; 386

```console
$ docker pull mono@sha256:8f10891be25745681bd6f98bf48e1234094816dc4b5dbef73d48f53f67536601
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.5 MB (259458549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2775d67ed2568bc292fd99d9a4c6e6e31195ae5382d5d3f1d76cb0f034c34e5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jun 2022 16:43:21 GMT
ADD file:7bc8fc617f718bf5e65e7fd718531a01122acc1783af5233c98aa9d31b0f093e in / 
# Wed, 22 Jun 2022 16:43:21 GMT
CMD ["bash"]
# Wed, 22 Jun 2022 16:43:21 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 22 Jun 2022 16:43:21 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr # buildkit
# Wed, 22 Jun 2022 16:43:21 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
# Wed, 22 Jun 2022 16:43:21 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
```

-	Layers:
	-	`sha256:1dfc643447ff7a82c599b429eda0d998c6dbad4ab2786eed580821b5b888204e`  
		Last Modified: Thu, 13 Jun 2024 00:44:44 GMT  
		Size: 28.0 MB (27994640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a198cb1aaae91cef3ed2eaed184c0a10f0b74e857bd5ea91dcde2955746f20f9`  
		Last Modified: Fri, 21 Jun 2024 01:03:12 GMT  
		Size: 2.8 MB (2791765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd658841b3e1b2084a6340e82f84033bf765e9ea9830350aa5a4aba88cbf3166`  
		Last Modified: Fri, 21 Jun 2024 01:03:14 GMT  
		Size: 68.6 MB (68585515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30bbf7033252959af4d7a4d2f468bba517cf0aeaf9f9e131902187bdc9737e6d`  
		Last Modified: Fri, 21 Jun 2024 02:04:03 GMT  
		Size: 160.1 MB (160086629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mono:6.12.0.182` - unknown; unknown

```console
$ docker pull mono@sha256:e69c4a0ff0efcd311f3ec0da7e72cbafaa9689b8555686674db7d3d689e13230
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11081926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48b0f05b8c3e2ec0bdb3fcbf2f85778a7584ea1dfd621e838399e99f0e6aac47`

```dockerfile
```

-	Layers:
	-	`sha256:f5bc84e8ea570b2500296b1f25f4226e60f0c15178c4ed81b09fa2c5ddf35fc6`  
		Last Modified: Fri, 21 Jun 2024 02:03:58 GMT  
		Size: 11.1 MB (11074056 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f11f469c7181081a082c334f89f2885f7a6a0953d5e152e5f75db2af4504d80e`  
		Last Modified: Fri, 21 Jun 2024 02:03:57 GMT  
		Size: 7.9 KB (7870 bytes)  
		MIME: application/vnd.in-toto+json

### `mono:6.12.0.182` - linux; ppc64le

```console
$ docker pull mono@sha256:fbfb5b60906856f25cc0ffb3ed273fa5da089aed24eab6afb049cc150c221768
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.7 MB (221654331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45a10e5a16545c25df57d5cf1f034acbb78fb5a3c968378416dc576fa88386ef`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:04 GMT
ADD file:6d33ba25d3625e5f445fc2183b60c64e2cbc780cb541d7f8ac76ce193b311d13 in / 
# Tue, 02 Aug 2022 01:18:06 GMT
CMD ["bash"]
# Wed, 03 Aug 2022 02:07:46 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 03 Aug 2022 02:08:06 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 03 Aug 2022 02:08:41 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 03 Aug 2022 02:11:40 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:fc8842eebb7ccaf249b2bb2d6a3878fffdae26c9db8f23b393c7f76a6249d2f6`  
		Last Modified: Tue, 02 Aug 2022 01:25:45 GMT  
		Size: 30.6 MB (30560308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1100971c8a3b3eb42c6e22a4c25f405143f007bda60d16697d49b333925b4d84`  
		Last Modified: Wed, 03 Aug 2022 02:15:13 GMT  
		Size: 2.9 MB (2892658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:390f883f1594b5d2d40b7ba4dc50f375439dd1611f38f0c3d071a38bf2ac62cd`  
		Last Modified: Wed, 03 Aug 2022 02:15:27 GMT  
		Size: 41.9 MB (41897345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ae94af697c95b6bf75033b813f19ec72f68da49a681d5ce7078753923129147`  
		Last Modified: Wed, 03 Aug 2022 02:16:58 GMT  
		Size: 146.3 MB (146304020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.12.0.182-slim`

```console
$ docker pull mono@sha256:d124eebf64f110db652f42c9e1e4a0627f84b6fc375ea3801751f7edcc74711b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le

### `mono:6.12.0.182-slim` - linux; amd64

```console
$ docker pull mono@sha256:749851d74745492754d1ebb3c50fc335d4b84a7bb34e17a4e7c3909c5ec1212b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.7 MB (94673661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5a2a70110040ee175a00069fa147d036d49deb2decd03a6374e83da337706e8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jun 2022 16:43:21 GMT
ADD file:cce4de1623245f9f28e3365e6cf749d85dcfedddea2d6fbc963c309a40818f52 in / 
# Wed, 22 Jun 2022 16:43:21 GMT
CMD ["bash"]
# Wed, 22 Jun 2022 16:43:21 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 22 Jun 2022 16:43:21 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr # buildkit
# Wed, 22 Jun 2022 16:43:21 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
```

-	Layers:
	-	`sha256:b338562f40a7fb7360dfae935da6d7e40d2545db18bc461d9d70ec1b2b657f33`  
		Last Modified: Thu, 13 Jun 2024 01:26:49 GMT  
		Size: 27.3 MB (27337703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b1b752ddf75c64e105424fb16f5a2053ddad33f059e3be8e520e35908cc4e97`  
		Last Modified: Fri, 21 Jun 2024 01:03:10 GMT  
		Size: 2.8 MB (2780035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d574eb224b5ddbe14656e28913cf5eeb5b14aa651aa3bcb9288aa43f1000aec5`  
		Last Modified: Fri, 21 Jun 2024 01:03:11 GMT  
		Size: 64.6 MB (64555923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mono:6.12.0.182-slim` - unknown; unknown

```console
$ docker pull mono@sha256:5a8421c386b586f98034983cc67448394e910e05ff857862418296991eddcf54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4134119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7daf4a5e106256a64c61c2f6e62ec4e5aa7020398e1b40c8bbe8b4e7458bec8d`

```dockerfile
```

-	Layers:
	-	`sha256:68c0c6a6586378e1af3fd618d65a15dd0a69c3e36744d2db3c2a64b91f8842b8`  
		Last Modified: Fri, 21 Jun 2024 01:03:10 GMT  
		Size: 4.1 MB (4124009 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ec35e37e8929d1729d15f72eaafb529c88604e0eb2b568452d3927312850835`  
		Last Modified: Fri, 21 Jun 2024 01:03:10 GMT  
		Size: 10.1 KB (10110 bytes)  
		MIME: application/vnd.in-toto+json

### `mono:6.12.0.182-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:f7c133539fa6a4add7484e9c93bc9b62ec32236d4b619f320c20b3248fb4739a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.9 MB (51860964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe52652f149ceedc89ed0c0f70985fcd898b6cd5cc98aa6f99f9ca06fd83046c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 00:49:37 GMT
ADD file:2ed7ca0d45c68b46a10ae186e8a03f98e72cadfeed17105668f53adf14d31e1f in / 
# Tue, 02 Aug 2022 00:49:38 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 07:17:55 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 01 Mar 2023 07:18:17 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 01 Mar 2023 07:18:42 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:187ecffbd1e0eae5de6567dff32bd58f28623635657779760c9d9539d6b7cc59`  
		Last Modified: Tue, 02 Aug 2022 00:57:06 GMT  
		Size: 24.9 MB (24889750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6702eef9c7d9ec6ede2c5f9a15a047b314ccc9140f25694f337c0127478bb25b`  
		Last Modified: Wed, 01 Mar 2023 07:23:12 GMT  
		Size: 2.5 MB (2467715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3781ed66d8db4f1e7c7b6323f62af11c65550a10f339ad7c0fb68f9467f8026d`  
		Last Modified: Wed, 01 Mar 2023 07:23:17 GMT  
		Size: 24.5 MB (24503499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0.182-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:beaab14b4de16ae0f14cb615383dddbe283523fbd00c8494f8a55ce1299ec4ce
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49105758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:053650949e0e3231b0c67fad4f4dd10e2cb9a84beb0a82569b203ce3a1716fbd`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:58:15 GMT
ADD file:ab786d88497f915679b3ac228e3bd805a58501dcb33b3d25e49cf1898770f9a7 in / 
# Thu, 13 Jun 2024 00:58:15 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 08:31:10 GMT
ENV MONO_VERSION=6.12.0.182
# Thu, 13 Jun 2024 08:31:24 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 13 Jun 2024 08:31:48 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:99d1ebcdd364332a1427098feecc8f94a8978ec971b171f7cca03bf01d1a149c`  
		Last Modified: Thu, 13 Jun 2024 01:03:01 GMT  
		Size: 22.9 MB (22944997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b7db2a28ee4fa8f5e893c5ca0f653dc9514221149d19d3632816e874498e112`  
		Last Modified: Thu, 13 Jun 2024 08:36:36 GMT  
		Size: 2.4 MB (2370421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f10ac972dcba288ded8e2044b27a0cdf74494394d8408e9383d92fce7e867d7`  
		Last Modified: Thu, 13 Jun 2024 08:36:40 GMT  
		Size: 23.8 MB (23790340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0.182-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:f0cc2d1cdff3f4c9132e03486d350424d918e8a58e17997314a1de02a04b24fc
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.3 MB (58299671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7c7359194914e922baaffe35e36d41958cbdc56e1dfe1475fdeda11d4d860f0`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:40:19 GMT
ADD file:de9a2b323e6d7d969277e7e781875e3daf3f49f2c1dcc569a1eec4f5bd789c46 in / 
# Thu, 13 Jun 2024 00:40:19 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 02:40:00 GMT
ENV MONO_VERSION=6.12.0.182
# Thu, 13 Jun 2024 02:40:07 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 13 Jun 2024 02:40:22 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7abf9f73c7747bb840a8edcd895830e53f09498136de3015568a9cd9f5ab10ed`  
		Last Modified: Thu, 13 Jun 2024 00:44:26 GMT  
		Size: 26.1 MB (26109272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0b5b6710e68b3b250dd681138cde05cf6596b6f323c42d994db4dcdb4761526`  
		Last Modified: Thu, 13 Jun 2024 02:44:41 GMT  
		Size: 2.6 MB (2645492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd67156f41b6153be4d7339a8c26d81d9648cfb9a9e365f2486f34aa6f6f507f`  
		Last Modified: Thu, 13 Jun 2024 02:44:44 GMT  
		Size: 29.5 MB (29544907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0.182-slim` - linux; 386

```console
$ docker pull mono@sha256:819bc68ca415cdb49ad461b4afb9a27004e442878b2bbdefc8a67317bc5b2ddf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.4 MB (99371920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c360bfbb224cb22cd13ba52ccd63bc77562ef28647c535cd0a42518f0773a842`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jun 2022 16:43:21 GMT
ADD file:7bc8fc617f718bf5e65e7fd718531a01122acc1783af5233c98aa9d31b0f093e in / 
# Wed, 22 Jun 2022 16:43:21 GMT
CMD ["bash"]
# Wed, 22 Jun 2022 16:43:21 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 22 Jun 2022 16:43:21 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr # buildkit
# Wed, 22 Jun 2022 16:43:21 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
```

-	Layers:
	-	`sha256:1dfc643447ff7a82c599b429eda0d998c6dbad4ab2786eed580821b5b888204e`  
		Last Modified: Thu, 13 Jun 2024 00:44:44 GMT  
		Size: 28.0 MB (27994640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a198cb1aaae91cef3ed2eaed184c0a10f0b74e857bd5ea91dcde2955746f20f9`  
		Last Modified: Fri, 21 Jun 2024 01:03:12 GMT  
		Size: 2.8 MB (2791765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd658841b3e1b2084a6340e82f84033bf765e9ea9830350aa5a4aba88cbf3166`  
		Last Modified: Fri, 21 Jun 2024 01:03:14 GMT  
		Size: 68.6 MB (68585515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mono:6.12.0.182-slim` - unknown; unknown

```console
$ docker pull mono@sha256:21b839469b89df687807ffdd3f870708c16efa44a6b299510e9d6391ba6499fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4130249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80ef153a1ce2f246cf50247bdbe0e53a65f2eca1f65498fe5be40b5242f5f8b1`

```dockerfile
```

-	Layers:
	-	`sha256:053ce445b27e3a8e224b16a3d2a8cdc9dc1d84ebee53d08de3d37ec36d5de95c`  
		Last Modified: Fri, 21 Jun 2024 01:03:12 GMT  
		Size: 4.1 MB (4120175 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:190e2c58614be0d956b94cdc868f9beb77c2f2d8ef16c981339f2b2c23f56975`  
		Last Modified: Fri, 21 Jun 2024 01:03:12 GMT  
		Size: 10.1 KB (10074 bytes)  
		MIME: application/vnd.in-toto+json

### `mono:6.12.0.182-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:b83383e51874bbee097571b303be3299c87d7da8c4c6b0f4e067cfaa552ad925
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75350311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c28d9c810a28445dd3b5767c5be8a3a5c5f459f859498e49f59bb419b735510`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:04 GMT
ADD file:6d33ba25d3625e5f445fc2183b60c64e2cbc780cb541d7f8ac76ce193b311d13 in / 
# Tue, 02 Aug 2022 01:18:06 GMT
CMD ["bash"]
# Wed, 03 Aug 2022 02:07:46 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 03 Aug 2022 02:08:06 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 03 Aug 2022 02:08:41 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:fc8842eebb7ccaf249b2bb2d6a3878fffdae26c9db8f23b393c7f76a6249d2f6`  
		Last Modified: Tue, 02 Aug 2022 01:25:45 GMT  
		Size: 30.6 MB (30560308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1100971c8a3b3eb42c6e22a4c25f405143f007bda60d16697d49b333925b4d84`  
		Last Modified: Wed, 03 Aug 2022 02:15:13 GMT  
		Size: 2.9 MB (2892658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:390f883f1594b5d2d40b7ba4dc50f375439dd1611f38f0c3d071a38bf2ac62cd`  
		Last Modified: Wed, 03 Aug 2022 02:15:27 GMT  
		Size: 41.9 MB (41897345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:latest`

```console
$ docker pull mono@sha256:122a14d6bb94876a6584fc7dc27acf61fdcce1b612442f6a27c4e6adbe57bd50
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le

### `mono:latest` - linux; amd64

```console
$ docker pull mono@sha256:d2ae1881a608fb6401bcebbf0d444fc2fcadf0db27f07c87153a79e7b14e861a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.6 MB (254589877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16d98cfcc673531288833a5cdb9f87087aa18082d1fed9ebe02021c67b1fdf0f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jun 2022 16:43:21 GMT
ADD file:cce4de1623245f9f28e3365e6cf749d85dcfedddea2d6fbc963c309a40818f52 in / 
# Wed, 22 Jun 2022 16:43:21 GMT
CMD ["bash"]
# Wed, 22 Jun 2022 16:43:21 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 22 Jun 2022 16:43:21 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr # buildkit
# Wed, 22 Jun 2022 16:43:21 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
# Wed, 22 Jun 2022 16:43:21 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
```

-	Layers:
	-	`sha256:b338562f40a7fb7360dfae935da6d7e40d2545db18bc461d9d70ec1b2b657f33`  
		Last Modified: Thu, 13 Jun 2024 01:26:49 GMT  
		Size: 27.3 MB (27337703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b1b752ddf75c64e105424fb16f5a2053ddad33f059e3be8e520e35908cc4e97`  
		Last Modified: Fri, 21 Jun 2024 01:03:10 GMT  
		Size: 2.8 MB (2780035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d574eb224b5ddbe14656e28913cf5eeb5b14aa651aa3bcb9288aa43f1000aec5`  
		Last Modified: Fri, 21 Jun 2024 01:03:11 GMT  
		Size: 64.6 MB (64555923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb9d6fb145c5367510a78273891d0ba84d7257b0bfdf3cd340f4e3d6f211de0a`  
		Last Modified: Fri, 21 Jun 2024 02:02:49 GMT  
		Size: 159.9 MB (159916216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mono:latest` - unknown; unknown

```console
$ docker pull mono@sha256:fc661c46136b8f9cbe60f721c811fb05d600f7614c9ddef8306ca5a261a6ea24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11085967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6322617bf4f258627a38887597f3d55cd3e73d36de6aa5f4734d1d6fcd3e7fd9`

```dockerfile
```

-	Layers:
	-	`sha256:08c2cae238c884d7e44ae9bd57336a51412c9603e15025c0a456eca7dd888aba`  
		Last Modified: Fri, 21 Jun 2024 02:02:46 GMT  
		Size: 11.1 MB (11078059 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2dda4ada58791fac758ee1dc7c9ee2756a6d55125463cc11427657bfedecb286`  
		Last Modified: Fri, 21 Jun 2024 02:02:46 GMT  
		Size: 7.9 KB (7908 bytes)  
		MIME: application/vnd.in-toto+json

### `mono:latest` - linux; arm variant v5

```console
$ docker pull mono@sha256:dea4d3a6cf8d83cd0b747ac36b0b7a279de919c38227c259e8f0dd933ad99d3d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.9 MB (192868079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52646a30a3e2966b0a92b143b872a725a0eaa3c003a2b6c3030454d2f5f26220`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 00:49:37 GMT
ADD file:2ed7ca0d45c68b46a10ae186e8a03f98e72cadfeed17105668f53adf14d31e1f in / 
# Tue, 02 Aug 2022 00:49:38 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 07:17:55 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 01 Mar 2023 07:18:17 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 01 Mar 2023 07:18:42 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 01 Mar 2023 07:20:53 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:187ecffbd1e0eae5de6567dff32bd58f28623635657779760c9d9539d6b7cc59`  
		Last Modified: Tue, 02 Aug 2022 00:57:06 GMT  
		Size: 24.9 MB (24889750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6702eef9c7d9ec6ede2c5f9a15a047b314ccc9140f25694f337c0127478bb25b`  
		Last Modified: Wed, 01 Mar 2023 07:23:12 GMT  
		Size: 2.5 MB (2467715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3781ed66d8db4f1e7c7b6323f62af11c65550a10f339ad7c0fb68f9467f8026d`  
		Last Modified: Wed, 01 Mar 2023 07:23:17 GMT  
		Size: 24.5 MB (24503499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f32f45a77bbef0505ff02ad954c1ce25d1cb8f5b668bbd7c73fa538966d0c0b`  
		Last Modified: Wed, 01 Mar 2023 07:24:21 GMT  
		Size: 141.0 MB (141007115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:latest` - linux; arm variant v7

```console
$ docker pull mono@sha256:0dfc1dd87793c5f9c7d9197edaa5bf64b13fd37064afba0ac721ecd09f554a22
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.2 MB (189174773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ed768bb4ba02e014621f121844e472e5e513d725bdf417d80780af7b0938c6e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:58:15 GMT
ADD file:ab786d88497f915679b3ac228e3bd805a58501dcb33b3d25e49cf1898770f9a7 in / 
# Thu, 13 Jun 2024 00:58:15 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 08:31:10 GMT
ENV MONO_VERSION=6.12.0.182
# Thu, 13 Jun 2024 08:31:24 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 13 Jun 2024 08:31:48 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 13 Jun 2024 08:34:33 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:99d1ebcdd364332a1427098feecc8f94a8978ec971b171f7cca03bf01d1a149c`  
		Last Modified: Thu, 13 Jun 2024 01:03:01 GMT  
		Size: 22.9 MB (22944997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b7db2a28ee4fa8f5e893c5ca0f653dc9514221149d19d3632816e874498e112`  
		Last Modified: Thu, 13 Jun 2024 08:36:36 GMT  
		Size: 2.4 MB (2370421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f10ac972dcba288ded8e2044b27a0cdf74494394d8408e9383d92fce7e867d7`  
		Last Modified: Thu, 13 Jun 2024 08:36:40 GMT  
		Size: 23.8 MB (23790340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bd48720e38dbaaaef8fb759054f29f92b12cbbea01eab398573da7dac4160a3`  
		Last Modified: Thu, 13 Jun 2024 08:37:30 GMT  
		Size: 140.1 MB (140069015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:latest` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:83a8328a667e7c0256a9832d8a8f2a3ccb189ac80da5ef1737a9b0d1c34d80ab
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.6 MB (216552576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ca3c4505019d48c31f72bda38a3d30a9661510b2d90cc6407c5585d49362028`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:40:19 GMT
ADD file:de9a2b323e6d7d969277e7e781875e3daf3f49f2c1dcc569a1eec4f5bd789c46 in / 
# Thu, 13 Jun 2024 00:40:19 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 02:40:00 GMT
ENV MONO_VERSION=6.12.0.182
# Thu, 13 Jun 2024 02:40:07 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 13 Jun 2024 02:40:22 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 13 Jun 2024 02:43:03 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7abf9f73c7747bb840a8edcd895830e53f09498136de3015568a9cd9f5ab10ed`  
		Last Modified: Thu, 13 Jun 2024 00:44:26 GMT  
		Size: 26.1 MB (26109272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0b5b6710e68b3b250dd681138cde05cf6596b6f323c42d994db4dcdb4761526`  
		Last Modified: Thu, 13 Jun 2024 02:44:41 GMT  
		Size: 2.6 MB (2645492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd67156f41b6153be4d7339a8c26d81d9648cfb9a9e365f2486f34aa6f6f507f`  
		Last Modified: Thu, 13 Jun 2024 02:44:44 GMT  
		Size: 29.5 MB (29544907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0091f5b1c3c6fe88db8dcb2b7849fe146d7c3571535910ff86aef81e76776d8`  
		Last Modified: Thu, 13 Jun 2024 02:45:28 GMT  
		Size: 158.3 MB (158252905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:latest` - linux; 386

```console
$ docker pull mono@sha256:8f10891be25745681bd6f98bf48e1234094816dc4b5dbef73d48f53f67536601
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.5 MB (259458549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2775d67ed2568bc292fd99d9a4c6e6e31195ae5382d5d3f1d76cb0f034c34e5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jun 2022 16:43:21 GMT
ADD file:7bc8fc617f718bf5e65e7fd718531a01122acc1783af5233c98aa9d31b0f093e in / 
# Wed, 22 Jun 2022 16:43:21 GMT
CMD ["bash"]
# Wed, 22 Jun 2022 16:43:21 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 22 Jun 2022 16:43:21 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr # buildkit
# Wed, 22 Jun 2022 16:43:21 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
# Wed, 22 Jun 2022 16:43:21 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
```

-	Layers:
	-	`sha256:1dfc643447ff7a82c599b429eda0d998c6dbad4ab2786eed580821b5b888204e`  
		Last Modified: Thu, 13 Jun 2024 00:44:44 GMT  
		Size: 28.0 MB (27994640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a198cb1aaae91cef3ed2eaed184c0a10f0b74e857bd5ea91dcde2955746f20f9`  
		Last Modified: Fri, 21 Jun 2024 01:03:12 GMT  
		Size: 2.8 MB (2791765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd658841b3e1b2084a6340e82f84033bf765e9ea9830350aa5a4aba88cbf3166`  
		Last Modified: Fri, 21 Jun 2024 01:03:14 GMT  
		Size: 68.6 MB (68585515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30bbf7033252959af4d7a4d2f468bba517cf0aeaf9f9e131902187bdc9737e6d`  
		Last Modified: Fri, 21 Jun 2024 02:04:03 GMT  
		Size: 160.1 MB (160086629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mono:latest` - unknown; unknown

```console
$ docker pull mono@sha256:e69c4a0ff0efcd311f3ec0da7e72cbafaa9689b8555686674db7d3d689e13230
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11081926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48b0f05b8c3e2ec0bdb3fcbf2f85778a7584ea1dfd621e838399e99f0e6aac47`

```dockerfile
```

-	Layers:
	-	`sha256:f5bc84e8ea570b2500296b1f25f4226e60f0c15178c4ed81b09fa2c5ddf35fc6`  
		Last Modified: Fri, 21 Jun 2024 02:03:58 GMT  
		Size: 11.1 MB (11074056 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f11f469c7181081a082c334f89f2885f7a6a0953d5e152e5f75db2af4504d80e`  
		Last Modified: Fri, 21 Jun 2024 02:03:57 GMT  
		Size: 7.9 KB (7870 bytes)  
		MIME: application/vnd.in-toto+json

### `mono:latest` - linux; ppc64le

```console
$ docker pull mono@sha256:fbfb5b60906856f25cc0ffb3ed273fa5da089aed24eab6afb049cc150c221768
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.7 MB (221654331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45a10e5a16545c25df57d5cf1f034acbb78fb5a3c968378416dc576fa88386ef`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:04 GMT
ADD file:6d33ba25d3625e5f445fc2183b60c64e2cbc780cb541d7f8ac76ce193b311d13 in / 
# Tue, 02 Aug 2022 01:18:06 GMT
CMD ["bash"]
# Wed, 03 Aug 2022 02:07:46 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 03 Aug 2022 02:08:06 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 03 Aug 2022 02:08:41 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 03 Aug 2022 02:11:40 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:fc8842eebb7ccaf249b2bb2d6a3878fffdae26c9db8f23b393c7f76a6249d2f6`  
		Last Modified: Tue, 02 Aug 2022 01:25:45 GMT  
		Size: 30.6 MB (30560308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1100971c8a3b3eb42c6e22a4c25f405143f007bda60d16697d49b333925b4d84`  
		Last Modified: Wed, 03 Aug 2022 02:15:13 GMT  
		Size: 2.9 MB (2892658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:390f883f1594b5d2d40b7ba4dc50f375439dd1611f38f0c3d071a38bf2ac62cd`  
		Last Modified: Wed, 03 Aug 2022 02:15:27 GMT  
		Size: 41.9 MB (41897345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ae94af697c95b6bf75033b813f19ec72f68da49a681d5ce7078753923129147`  
		Last Modified: Wed, 03 Aug 2022 02:16:58 GMT  
		Size: 146.3 MB (146304020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:slim`

```console
$ docker pull mono@sha256:d124eebf64f110db652f42c9e1e4a0627f84b6fc375ea3801751f7edcc74711b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le

### `mono:slim` - linux; amd64

```console
$ docker pull mono@sha256:749851d74745492754d1ebb3c50fc335d4b84a7bb34e17a4e7c3909c5ec1212b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.7 MB (94673661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5a2a70110040ee175a00069fa147d036d49deb2decd03a6374e83da337706e8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jun 2022 16:43:21 GMT
ADD file:cce4de1623245f9f28e3365e6cf749d85dcfedddea2d6fbc963c309a40818f52 in / 
# Wed, 22 Jun 2022 16:43:21 GMT
CMD ["bash"]
# Wed, 22 Jun 2022 16:43:21 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 22 Jun 2022 16:43:21 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr # buildkit
# Wed, 22 Jun 2022 16:43:21 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
```

-	Layers:
	-	`sha256:b338562f40a7fb7360dfae935da6d7e40d2545db18bc461d9d70ec1b2b657f33`  
		Last Modified: Thu, 13 Jun 2024 01:26:49 GMT  
		Size: 27.3 MB (27337703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b1b752ddf75c64e105424fb16f5a2053ddad33f059e3be8e520e35908cc4e97`  
		Last Modified: Fri, 21 Jun 2024 01:03:10 GMT  
		Size: 2.8 MB (2780035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d574eb224b5ddbe14656e28913cf5eeb5b14aa651aa3bcb9288aa43f1000aec5`  
		Last Modified: Fri, 21 Jun 2024 01:03:11 GMT  
		Size: 64.6 MB (64555923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mono:slim` - unknown; unknown

```console
$ docker pull mono@sha256:5a8421c386b586f98034983cc67448394e910e05ff857862418296991eddcf54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4134119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7daf4a5e106256a64c61c2f6e62ec4e5aa7020398e1b40c8bbe8b4e7458bec8d`

```dockerfile
```

-	Layers:
	-	`sha256:68c0c6a6586378e1af3fd618d65a15dd0a69c3e36744d2db3c2a64b91f8842b8`  
		Last Modified: Fri, 21 Jun 2024 01:03:10 GMT  
		Size: 4.1 MB (4124009 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ec35e37e8929d1729d15f72eaafb529c88604e0eb2b568452d3927312850835`  
		Last Modified: Fri, 21 Jun 2024 01:03:10 GMT  
		Size: 10.1 KB (10110 bytes)  
		MIME: application/vnd.in-toto+json

### `mono:slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:f7c133539fa6a4add7484e9c93bc9b62ec32236d4b619f320c20b3248fb4739a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.9 MB (51860964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe52652f149ceedc89ed0c0f70985fcd898b6cd5cc98aa6f99f9ca06fd83046c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 00:49:37 GMT
ADD file:2ed7ca0d45c68b46a10ae186e8a03f98e72cadfeed17105668f53adf14d31e1f in / 
# Tue, 02 Aug 2022 00:49:38 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 07:17:55 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 01 Mar 2023 07:18:17 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 01 Mar 2023 07:18:42 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:187ecffbd1e0eae5de6567dff32bd58f28623635657779760c9d9539d6b7cc59`  
		Last Modified: Tue, 02 Aug 2022 00:57:06 GMT  
		Size: 24.9 MB (24889750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6702eef9c7d9ec6ede2c5f9a15a047b314ccc9140f25694f337c0127478bb25b`  
		Last Modified: Wed, 01 Mar 2023 07:23:12 GMT  
		Size: 2.5 MB (2467715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3781ed66d8db4f1e7c7b6323f62af11c65550a10f339ad7c0fb68f9467f8026d`  
		Last Modified: Wed, 01 Mar 2023 07:23:17 GMT  
		Size: 24.5 MB (24503499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:beaab14b4de16ae0f14cb615383dddbe283523fbd00c8494f8a55ce1299ec4ce
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49105758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:053650949e0e3231b0c67fad4f4dd10e2cb9a84beb0a82569b203ce3a1716fbd`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:58:15 GMT
ADD file:ab786d88497f915679b3ac228e3bd805a58501dcb33b3d25e49cf1898770f9a7 in / 
# Thu, 13 Jun 2024 00:58:15 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 08:31:10 GMT
ENV MONO_VERSION=6.12.0.182
# Thu, 13 Jun 2024 08:31:24 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 13 Jun 2024 08:31:48 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:99d1ebcdd364332a1427098feecc8f94a8978ec971b171f7cca03bf01d1a149c`  
		Last Modified: Thu, 13 Jun 2024 01:03:01 GMT  
		Size: 22.9 MB (22944997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b7db2a28ee4fa8f5e893c5ca0f653dc9514221149d19d3632816e874498e112`  
		Last Modified: Thu, 13 Jun 2024 08:36:36 GMT  
		Size: 2.4 MB (2370421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f10ac972dcba288ded8e2044b27a0cdf74494394d8408e9383d92fce7e867d7`  
		Last Modified: Thu, 13 Jun 2024 08:36:40 GMT  
		Size: 23.8 MB (23790340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:f0cc2d1cdff3f4c9132e03486d350424d918e8a58e17997314a1de02a04b24fc
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.3 MB (58299671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7c7359194914e922baaffe35e36d41958cbdc56e1dfe1475fdeda11d4d860f0`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:40:19 GMT
ADD file:de9a2b323e6d7d969277e7e781875e3daf3f49f2c1dcc569a1eec4f5bd789c46 in / 
# Thu, 13 Jun 2024 00:40:19 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 02:40:00 GMT
ENV MONO_VERSION=6.12.0.182
# Thu, 13 Jun 2024 02:40:07 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 13 Jun 2024 02:40:22 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7abf9f73c7747bb840a8edcd895830e53f09498136de3015568a9cd9f5ab10ed`  
		Last Modified: Thu, 13 Jun 2024 00:44:26 GMT  
		Size: 26.1 MB (26109272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0b5b6710e68b3b250dd681138cde05cf6596b6f323c42d994db4dcdb4761526`  
		Last Modified: Thu, 13 Jun 2024 02:44:41 GMT  
		Size: 2.6 MB (2645492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd67156f41b6153be4d7339a8c26d81d9648cfb9a9e365f2486f34aa6f6f507f`  
		Last Modified: Thu, 13 Jun 2024 02:44:44 GMT  
		Size: 29.5 MB (29544907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:slim` - linux; 386

```console
$ docker pull mono@sha256:819bc68ca415cdb49ad461b4afb9a27004e442878b2bbdefc8a67317bc5b2ddf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.4 MB (99371920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c360bfbb224cb22cd13ba52ccd63bc77562ef28647c535cd0a42518f0773a842`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jun 2022 16:43:21 GMT
ADD file:7bc8fc617f718bf5e65e7fd718531a01122acc1783af5233c98aa9d31b0f093e in / 
# Wed, 22 Jun 2022 16:43:21 GMT
CMD ["bash"]
# Wed, 22 Jun 2022 16:43:21 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 22 Jun 2022 16:43:21 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr # buildkit
# Wed, 22 Jun 2022 16:43:21 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
```

-	Layers:
	-	`sha256:1dfc643447ff7a82c599b429eda0d998c6dbad4ab2786eed580821b5b888204e`  
		Last Modified: Thu, 13 Jun 2024 00:44:44 GMT  
		Size: 28.0 MB (27994640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a198cb1aaae91cef3ed2eaed184c0a10f0b74e857bd5ea91dcde2955746f20f9`  
		Last Modified: Fri, 21 Jun 2024 01:03:12 GMT  
		Size: 2.8 MB (2791765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd658841b3e1b2084a6340e82f84033bf765e9ea9830350aa5a4aba88cbf3166`  
		Last Modified: Fri, 21 Jun 2024 01:03:14 GMT  
		Size: 68.6 MB (68585515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mono:slim` - unknown; unknown

```console
$ docker pull mono@sha256:21b839469b89df687807ffdd3f870708c16efa44a6b299510e9d6391ba6499fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4130249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80ef153a1ce2f246cf50247bdbe0e53a65f2eca1f65498fe5be40b5242f5f8b1`

```dockerfile
```

-	Layers:
	-	`sha256:053ce445b27e3a8e224b16a3d2a8cdc9dc1d84ebee53d08de3d37ec36d5de95c`  
		Last Modified: Fri, 21 Jun 2024 01:03:12 GMT  
		Size: 4.1 MB (4120175 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:190e2c58614be0d956b94cdc868f9beb77c2f2d8ef16c981339f2b2c23f56975`  
		Last Modified: Fri, 21 Jun 2024 01:03:12 GMT  
		Size: 10.1 KB (10074 bytes)  
		MIME: application/vnd.in-toto+json

### `mono:slim` - linux; ppc64le

```console
$ docker pull mono@sha256:b83383e51874bbee097571b303be3299c87d7da8c4c6b0f4e067cfaa552ad925
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75350311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c28d9c810a28445dd3b5767c5be8a3a5c5f459f859498e49f59bb419b735510`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:04 GMT
ADD file:6d33ba25d3625e5f445fc2183b60c64e2cbc780cb541d7f8ac76ce193b311d13 in / 
# Tue, 02 Aug 2022 01:18:06 GMT
CMD ["bash"]
# Wed, 03 Aug 2022 02:07:46 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 03 Aug 2022 02:08:06 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 03 Aug 2022 02:08:41 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:fc8842eebb7ccaf249b2bb2d6a3878fffdae26c9db8f23b393c7f76a6249d2f6`  
		Last Modified: Tue, 02 Aug 2022 01:25:45 GMT  
		Size: 30.6 MB (30560308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1100971c8a3b3eb42c6e22a4c25f405143f007bda60d16697d49b333925b4d84`  
		Last Modified: Wed, 03 Aug 2022 02:15:13 GMT  
		Size: 2.9 MB (2892658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:390f883f1594b5d2d40b7ba4dc50f375439dd1611f38f0c3d071a38bf2ac62cd`  
		Last Modified: Wed, 03 Aug 2022 02:15:27 GMT  
		Size: 41.9 MB (41897345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
