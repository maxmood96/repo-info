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
$ docker pull mono@sha256:86767b090cf14a50f9f006191e72be7fa71c0a0eda8afcc56c0d6f1031110fa7
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
$ docker pull mono@sha256:fd331c4c7a1b2b895a97f4e7829e8f40045c2dcab4156a2c1f13f1a17d58ad21
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.8 MB (254822861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1c1a10a5340e5cc64fa235e6d0d4baf42815e4de3f3389e0d10c302b2604b9b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:50 GMT
ADD file:9b846fb660cf816c4e731c6f547b8e389343bc05aa2ec510b1dfc2bddd4d1c8a in / 
# Wed, 24 Apr 2024 03:28:51 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 13:44:56 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 24 Apr 2024 13:45:07 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 24 Apr 2024 13:45:29 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 24 Apr 2024 13:47:22 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:74ff537ac401802b30ae451fd049f6337b6ed0ee93f7f7e1b00cc09b9ae7f2af`  
		Last Modified: Wed, 24 Apr 2024 03:33:56 GMT  
		Size: 27.3 MB (27337575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ffd837dfe32dada37b2b83dc3294fdb8c5b1aa8e9d843a9d939191c5358a355`  
		Last Modified: Wed, 24 Apr 2024 13:52:29 GMT  
		Size: 2.8 MB (2780777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acc88837dcf46a86e66bf61f6da043eac5337cd9d1bb0b8771350b1a536ffdc1`  
		Last Modified: Wed, 24 Apr 2024 13:52:38 GMT  
		Size: 64.8 MB (64773978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9f93b564c87b034a6f8e8f6fb69a30afc9e039b5220024dae7bb2f6f40659ce`  
		Last Modified: Wed, 24 Apr 2024 13:53:36 GMT  
		Size: 159.9 MB (159930531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

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
$ docker pull mono@sha256:bd8a12d74ce824caff0f9f8958c7bcfffb892449f02a0e4df9cf6e8192b54176
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.2 MB (189166436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cb250b5d8f4152de3c52f3965099ebcfa87068ef5395e9795797f24516e93a0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 04:07:41 GMT
ADD file:985460a24e46cb6fd38e9ecdf21565547413f5f50d7c5c96d367b89aa94b91fa in / 
# Wed, 24 Apr 2024 04:07:41 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 07:02:59 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 24 Apr 2024 07:03:11 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 24 Apr 2024 07:03:30 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 24 Apr 2024 07:05:23 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a26123864d4d41f3f97e44b15f7ae2ecb9a15cbc37d6085d418a129976773e32`  
		Last Modified: Wed, 24 Apr 2024 04:12:31 GMT  
		Size: 22.9 MB (22945064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e354d269265092711be691142d28fc8002953b5bfb897dbd91cd4789aa0d7f2c`  
		Last Modified: Wed, 24 Apr 2024 07:07:19 GMT  
		Size: 2.4 MB (2370522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce30d34e592060862296941593408133f444860b8431bd82c0f709acf3400dac`  
		Last Modified: Wed, 24 Apr 2024 07:07:23 GMT  
		Size: 23.8 MB (23790719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0cf8b7baf15a56b76905e86633595d7d9f122406ce84adb136eb23cf3619250`  
		Last Modified: Wed, 24 Apr 2024 07:08:15 GMT  
		Size: 140.1 MB (140060131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:e315d205d62cd6c04d52b11ecaf05e16c4f51b7eba142a8852e042c0283c1b01
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.6 MB (216552462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61d85bf404e8cc493498953016e368e84808ab7154fb3b866fb9b0257e80dcbb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 00:40:08 GMT
ADD file:469a091f7763af8b8b723185853358a0516954941c82654915e259a2356612ae in / 
# Tue, 14 May 2024 00:40:08 GMT
CMD ["bash"]
# Tue, 14 May 2024 03:01:03 GMT
ENV MONO_VERSION=6.12.0.182
# Tue, 14 May 2024 03:01:12 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 14 May 2024 03:02:44 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 14 May 2024 03:06:59 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:ad8110ff35cfa20fc3638a9f2a63a1113c1e4f724bc3b8c11d7ae280154356ca`  
		Last Modified: Tue, 14 May 2024 00:44:04 GMT  
		Size: 26.1 MB (26109106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a529a8ce298691a652a87333069ec6318e368ff0af7e2171b0ec58c5bf349dd8`  
		Last Modified: Tue, 14 May 2024 03:13:31 GMT  
		Size: 2.6 MB (2645561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79c2d783bd9b494f35fa932c80b7d810922f24489d8661f9f7e6626244d07bad`  
		Last Modified: Tue, 14 May 2024 03:13:34 GMT  
		Size: 29.5 MB (29545286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4ec1315f421edc1ff66ccc5ba4bcdd5d658530a2364f7438d255c14e6d80366`  
		Last Modified: Tue, 14 May 2024 03:14:19 GMT  
		Size: 158.3 MB (158252509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6` - linux; 386

```console
$ docker pull mono@sha256:067ca9a38acaaf9fdea29d7de110e8fd76261197be74a6b479b610eedd5a9b3d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.7 MB (259701817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:883e88334262384fea165fb01f2ec11dde2d61bc921c9f3bd6b3f1489f83d508`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 00:47:54 GMT
ADD file:75dbbf2d7d721b8debce2bfecdbf3ea14eb9b4dfe8a6354a21dd21725cafaff8 in / 
# Tue, 14 May 2024 00:47:54 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:16:51 GMT
ENV MONO_VERSION=6.12.0.182
# Tue, 14 May 2024 01:17:03 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 14 May 2024 01:17:39 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 14 May 2024 01:21:06 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:261459e26de7bf625f6d2ad5439fdd881d51b8e9bc959e0f3eb3b67ebacc250f`  
		Last Modified: Tue, 14 May 2024 00:53:24 GMT  
		Size: 28.0 MB (27994475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:036bbf0cc3e0f790c56486ebf068c9323a5e7716334c0114c7e3551fd1005100`  
		Last Modified: Tue, 14 May 2024 01:23:54 GMT  
		Size: 2.8 MB (2792366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb6f765ea19029790391afd07a05f782804dc82a94340049c2ad63c4eade3caf`  
		Last Modified: Tue, 14 May 2024 01:24:08 GMT  
		Size: 68.8 MB (68800484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47f132e8616f7a3f460f3dd4f3369385c8c9b4d238922ab196b9e2387f25e5c3`  
		Last Modified: Tue, 14 May 2024 01:25:24 GMT  
		Size: 160.1 MB (160114492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

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
$ docker pull mono@sha256:6d47290645de36eb0f9185f3794730b07d931e71dd1f01749ae3a117adafa41b
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
$ docker pull mono@sha256:0749e711811842967d725da21612af6129be80c84e3ed529fb700cfbf81e455d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.9 MB (94892330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:593772cbcad062ca2e93e73111024a35645d7510a450b015dbe1012eb08b05fc`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:50 GMT
ADD file:9b846fb660cf816c4e731c6f547b8e389343bc05aa2ec510b1dfc2bddd4d1c8a in / 
# Wed, 24 Apr 2024 03:28:51 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 13:44:56 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 24 Apr 2024 13:45:07 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 24 Apr 2024 13:45:29 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:74ff537ac401802b30ae451fd049f6337b6ed0ee93f7f7e1b00cc09b9ae7f2af`  
		Last Modified: Wed, 24 Apr 2024 03:33:56 GMT  
		Size: 27.3 MB (27337575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ffd837dfe32dada37b2b83dc3294fdb8c5b1aa8e9d843a9d939191c5358a355`  
		Last Modified: Wed, 24 Apr 2024 13:52:29 GMT  
		Size: 2.8 MB (2780777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acc88837dcf46a86e66bf61f6da043eac5337cd9d1bb0b8771350b1a536ffdc1`  
		Last Modified: Wed, 24 Apr 2024 13:52:38 GMT  
		Size: 64.8 MB (64773978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

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
$ docker pull mono@sha256:fa609c04866c144a99440dc2501eb77993b62e2a149d5fe1781a0539a5af518b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49106305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:634defc256033a7bfb1b71133d25e64724d595feb9f1d983b457847c7773360e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 04:07:41 GMT
ADD file:985460a24e46cb6fd38e9ecdf21565547413f5f50d7c5c96d367b89aa94b91fa in / 
# Wed, 24 Apr 2024 04:07:41 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 07:02:59 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 24 Apr 2024 07:03:11 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 24 Apr 2024 07:03:30 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a26123864d4d41f3f97e44b15f7ae2ecb9a15cbc37d6085d418a129976773e32`  
		Last Modified: Wed, 24 Apr 2024 04:12:31 GMT  
		Size: 22.9 MB (22945064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e354d269265092711be691142d28fc8002953b5bfb897dbd91cd4789aa0d7f2c`  
		Last Modified: Wed, 24 Apr 2024 07:07:19 GMT  
		Size: 2.4 MB (2370522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce30d34e592060862296941593408133f444860b8431bd82c0f709acf3400dac`  
		Last Modified: Wed, 24 Apr 2024 07:07:23 GMT  
		Size: 23.8 MB (23790719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:e2727d8c2692fbaf5a3abaaf56a98d49a6e5b24ff7c727cb564f88ad2cb240bc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.3 MB (58299953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9dcf5344b0840b1056715bc2ba296aed99407dab01e0c67ab889f9980e8e77b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 00:40:08 GMT
ADD file:469a091f7763af8b8b723185853358a0516954941c82654915e259a2356612ae in / 
# Tue, 14 May 2024 00:40:08 GMT
CMD ["bash"]
# Tue, 14 May 2024 03:01:03 GMT
ENV MONO_VERSION=6.12.0.182
# Tue, 14 May 2024 03:01:12 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 14 May 2024 03:02:44 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:ad8110ff35cfa20fc3638a9f2a63a1113c1e4f724bc3b8c11d7ae280154356ca`  
		Last Modified: Tue, 14 May 2024 00:44:04 GMT  
		Size: 26.1 MB (26109106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a529a8ce298691a652a87333069ec6318e368ff0af7e2171b0ec58c5bf349dd8`  
		Last Modified: Tue, 14 May 2024 03:13:31 GMT  
		Size: 2.6 MB (2645561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79c2d783bd9b494f35fa932c80b7d810922f24489d8661f9f7e6626244d07bad`  
		Last Modified: Tue, 14 May 2024 03:13:34 GMT  
		Size: 29.5 MB (29545286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6-slim` - linux; 386

```console
$ docker pull mono@sha256:7290a085e73bf2acdf312667141ed3060c3ecbbcdabd4e2f345865b5e8090612
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.6 MB (99587325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0122e8a6790708e8b29c1a50eb7a19482e2483089f00f9c46226457b9baa8325`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 00:47:54 GMT
ADD file:75dbbf2d7d721b8debce2bfecdbf3ea14eb9b4dfe8a6354a21dd21725cafaff8 in / 
# Tue, 14 May 2024 00:47:54 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:16:51 GMT
ENV MONO_VERSION=6.12.0.182
# Tue, 14 May 2024 01:17:03 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 14 May 2024 01:17:39 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:261459e26de7bf625f6d2ad5439fdd881d51b8e9bc959e0f3eb3b67ebacc250f`  
		Last Modified: Tue, 14 May 2024 00:53:24 GMT  
		Size: 28.0 MB (27994475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:036bbf0cc3e0f790c56486ebf068c9323a5e7716334c0114c7e3551fd1005100`  
		Last Modified: Tue, 14 May 2024 01:23:54 GMT  
		Size: 2.8 MB (2792366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb6f765ea19029790391afd07a05f782804dc82a94340049c2ad63c4eade3caf`  
		Last Modified: Tue, 14 May 2024 01:24:08 GMT  
		Size: 68.8 MB (68800484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

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
$ docker pull mono@sha256:b229c98da12419ddf62c0e49ead7a8b28a52bc52ee30d211286c3ff3b350d7f1
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
$ docker pull mono@sha256:2835babf96dff90fe86e45f0fb9e476d1d6705a7a69a2819d0819854f1b612bb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.2 MB (225232047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edea99883fa4636fccfa4b0b112d15f032827d9554ad8e3291f0a45b8b25fd48`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:50 GMT
ADD file:9b846fb660cf816c4e731c6f547b8e389343bc05aa2ec510b1dfc2bddd4d1c8a in / 
# Wed, 24 Apr 2024 03:28:51 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 13:45:38 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 24 Apr 2024 13:45:47 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 24 Apr 2024 13:46:09 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 24 Apr 2024 13:52:09 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:74ff537ac401802b30ae451fd049f6337b6ed0ee93f7f7e1b00cc09b9ae7f2af`  
		Last Modified: Wed, 24 Apr 2024 03:33:56 GMT  
		Size: 27.3 MB (27337575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de69173ac5dc57b1bff6ca742571c692a9d0059ca5039f1546275a70eae8e66e`  
		Last Modified: Wed, 24 Apr 2024 13:52:54 GMT  
		Size: 2.8 MB (2780823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dadd7019a9ea55b7f9dbfca86a546e8846c9c203686b04dd273fd9b13aa2041`  
		Last Modified: Wed, 24 Apr 2024 13:53:03 GMT  
		Size: 64.8 MB (64780285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46de26ee7797d4777c37763e32361320626fb1e09d0a30e521c065ae2a1edddd`  
		Last Modified: Wed, 24 Apr 2024 13:54:08 GMT  
		Size: 130.3 MB (130333364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

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
$ docker pull mono@sha256:6072350263c1422bffa85718df883e3ce12ea3b2494868fad86af67e3cf61167
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.0 MB (176955353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ce8fec035219f1fe5b9e36df20454bd7c5f807b37082483781ed3d187e3fded`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 04:07:41 GMT
ADD file:985460a24e46cb6fd38e9ecdf21565547413f5f50d7c5c96d367b89aa94b91fa in / 
# Wed, 24 Apr 2024 04:07:41 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 07:03:32 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 24 Apr 2024 07:03:41 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 24 Apr 2024 07:04:01 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 24 Apr 2024 07:06:49 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a26123864d4d41f3f97e44b15f7ae2ecb9a15cbc37d6085d418a129976773e32`  
		Last Modified: Wed, 24 Apr 2024 04:12:31 GMT  
		Size: 22.9 MB (22945064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c20deacbb5552442449e92cfa65bb3e47b454eb158f7e02b73e26f0c451aa7d7`  
		Last Modified: Wed, 24 Apr 2024 07:07:37 GMT  
		Size: 2.4 MB (2370498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66a6381d33c325b2fc10fea2ccb3063ec32f09298fbcba6a5680adf58bea081b`  
		Last Modified: Wed, 24 Apr 2024 07:07:41 GMT  
		Size: 23.8 MB (23815984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a6328f4e34a27975511a13553d718dbf5851c9f562bd96cbd6a45da4bc79721`  
		Last Modified: Wed, 24 Apr 2024 07:08:52 GMT  
		Size: 127.8 MB (127823807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:8d9feaa88a3cb999e90781b597e1b0d245569c00d181ba5d49754b9ca2f511fb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.8 MB (203824562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f4ec35cda17fecea36cdd5bdbf3e31158dd5804f3cbafe49a31d9ad583fddbc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 00:40:08 GMT
ADD file:469a091f7763af8b8b723185853358a0516954941c82654915e259a2356612ae in / 
# Tue, 14 May 2024 00:40:08 GMT
CMD ["bash"]
# Tue, 14 May 2024 03:02:56 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 14 May 2024 03:03:04 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 14 May 2024 03:04:45 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 14 May 2024 03:13:02 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:ad8110ff35cfa20fc3638a9f2a63a1113c1e4f724bc3b8c11d7ae280154356ca`  
		Last Modified: Tue, 14 May 2024 00:44:04 GMT  
		Size: 26.1 MB (26109106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de210138ebc49b057b24b4ebfa1a1b2879b1e0db5d6dd499ee017d962487af73`  
		Last Modified: Tue, 14 May 2024 03:13:47 GMT  
		Size: 2.6 MB (2645569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:189a105128c26fd639e04ae79ae9dee9024b808475e0060f87f6e8ea2c842cd5`  
		Last Modified: Tue, 14 May 2024 03:13:51 GMT  
		Size: 29.6 MB (29575186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:309df2a030de7d30b87b24c401991712094e5a83beed5fb849171e8c3ab42d38`  
		Last Modified: Tue, 14 May 2024 03:14:50 GMT  
		Size: 145.5 MB (145494701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10` - linux; 386

```console
$ docker pull mono@sha256:976c308c970a488d2c3ff5348077a0ecd9363a870e830eae8683e916d250f3a9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.0 MB (231042464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4657bcf96ae2f5d9717b876758b9c137d832ae5440f6c3d6734077bc47fc116`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 00:47:54 GMT
ADD file:75dbbf2d7d721b8debce2bfecdbf3ea14eb9b4dfe8a6354a21dd21725cafaff8 in / 
# Tue, 14 May 2024 00:47:54 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:17:49 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 14 May 2024 01:18:00 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 14 May 2024 01:18:33 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 14 May 2024 01:23:27 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:261459e26de7bf625f6d2ad5439fdd881d51b8e9bc959e0f3eb3b67ebacc250f`  
		Last Modified: Tue, 14 May 2024 00:53:24 GMT  
		Size: 28.0 MB (27994475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d60b49ed6027113d5c2a31b5b98be0218f2e87f0203a1363a31ac4d30bbe3be`  
		Last Modified: Tue, 14 May 2024 01:24:25 GMT  
		Size: 2.8 MB (2792316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3252ffbfb712663e2665e56c94ac9a64b085bdebda6c3b18a61ddd1a6d001835`  
		Last Modified: Tue, 14 May 2024 01:24:39 GMT  
		Size: 68.8 MB (68809512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca930432a0d0862a13944f362fa095178ff23139e1149e5ef2b30702bea9f9df`  
		Last Modified: Tue, 14 May 2024 01:26:09 GMT  
		Size: 131.4 MB (131446161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

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
$ docker pull mono@sha256:c39dc0f28c8ed2dd04fde2c77bf2ea0cfae83256410d5ab7499737e118e630aa
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
$ docker pull mono@sha256:5775ef7a361f8db7d9e0592b937bd9b5ee10590eabfa05da5444aa49a11b1111
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.9 MB (94898683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cb1e72c2817f2e870b2b1faf088df393f0cc3c09269b3794025e6ee5fb71082`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:50 GMT
ADD file:9b846fb660cf816c4e731c6f547b8e389343bc05aa2ec510b1dfc2bddd4d1c8a in / 
# Wed, 24 Apr 2024 03:28:51 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 13:45:38 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 24 Apr 2024 13:45:47 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 24 Apr 2024 13:46:09 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:74ff537ac401802b30ae451fd049f6337b6ed0ee93f7f7e1b00cc09b9ae7f2af`  
		Last Modified: Wed, 24 Apr 2024 03:33:56 GMT  
		Size: 27.3 MB (27337575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de69173ac5dc57b1bff6ca742571c692a9d0059ca5039f1546275a70eae8e66e`  
		Last Modified: Wed, 24 Apr 2024 13:52:54 GMT  
		Size: 2.8 MB (2780823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dadd7019a9ea55b7f9dbfca86a546e8846c9c203686b04dd273fd9b13aa2041`  
		Last Modified: Wed, 24 Apr 2024 13:53:03 GMT  
		Size: 64.8 MB (64780285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

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
$ docker pull mono@sha256:a90f77ad468d1add8546223d8b6e5fd51a8f6e89bf0b76b90c24d018c82221cf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49131546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81b91c8ff16e8fa7d7c50a1ce5d562cbce1aafe0f49892f8848d50b7b073a2a4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 04:07:41 GMT
ADD file:985460a24e46cb6fd38e9ecdf21565547413f5f50d7c5c96d367b89aa94b91fa in / 
# Wed, 24 Apr 2024 04:07:41 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 07:03:32 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 24 Apr 2024 07:03:41 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 24 Apr 2024 07:04:01 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a26123864d4d41f3f97e44b15f7ae2ecb9a15cbc37d6085d418a129976773e32`  
		Last Modified: Wed, 24 Apr 2024 04:12:31 GMT  
		Size: 22.9 MB (22945064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c20deacbb5552442449e92cfa65bb3e47b454eb158f7e02b73e26f0c451aa7d7`  
		Last Modified: Wed, 24 Apr 2024 07:07:37 GMT  
		Size: 2.4 MB (2370498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66a6381d33c325b2fc10fea2ccb3063ec32f09298fbcba6a5680adf58bea081b`  
		Last Modified: Wed, 24 Apr 2024 07:07:41 GMT  
		Size: 23.8 MB (23815984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:5efcbde5e0f8fb609f2d83ff541a907f5f9ea6f81408bd7acf2c953e0bc2a65d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.3 MB (58329861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fb8af29a796e3c86fe790e994ac1ae11a80809fb4001e62609b748833b52f0e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 00:40:08 GMT
ADD file:469a091f7763af8b8b723185853358a0516954941c82654915e259a2356612ae in / 
# Tue, 14 May 2024 00:40:08 GMT
CMD ["bash"]
# Tue, 14 May 2024 03:02:56 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 14 May 2024 03:03:04 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 14 May 2024 03:04:45 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:ad8110ff35cfa20fc3638a9f2a63a1113c1e4f724bc3b8c11d7ae280154356ca`  
		Last Modified: Tue, 14 May 2024 00:44:04 GMT  
		Size: 26.1 MB (26109106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de210138ebc49b057b24b4ebfa1a1b2879b1e0db5d6dd499ee017d962487af73`  
		Last Modified: Tue, 14 May 2024 03:13:47 GMT  
		Size: 2.6 MB (2645569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:189a105128c26fd639e04ae79ae9dee9024b808475e0060f87f6e8ea2c842cd5`  
		Last Modified: Tue, 14 May 2024 03:13:51 GMT  
		Size: 29.6 MB (29575186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10-slim` - linux; 386

```console
$ docker pull mono@sha256:77d4a1a1db1496d5cdbe58891e11ba0c64a12c1bd66a078d0e890c5454450ad5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.6 MB (99596303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dda2618a8f113f6462ef8fd3d33a14a3b4daecdb03db4de5e6ecbcf9b9d5750e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 00:47:54 GMT
ADD file:75dbbf2d7d721b8debce2bfecdbf3ea14eb9b4dfe8a6354a21dd21725cafaff8 in / 
# Tue, 14 May 2024 00:47:54 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:17:49 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 14 May 2024 01:18:00 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 14 May 2024 01:18:33 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:261459e26de7bf625f6d2ad5439fdd881d51b8e9bc959e0f3eb3b67ebacc250f`  
		Last Modified: Tue, 14 May 2024 00:53:24 GMT  
		Size: 28.0 MB (27994475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d60b49ed6027113d5c2a31b5b98be0218f2e87f0203a1363a31ac4d30bbe3be`  
		Last Modified: Tue, 14 May 2024 01:24:25 GMT  
		Size: 2.8 MB (2792316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3252ffbfb712663e2665e56c94ac9a64b085bdebda6c3b18a61ddd1a6d001835`  
		Last Modified: Tue, 14 May 2024 01:24:39 GMT  
		Size: 68.8 MB (68809512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

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
$ docker pull mono@sha256:b229c98da12419ddf62c0e49ead7a8b28a52bc52ee30d211286c3ff3b350d7f1
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
$ docker pull mono@sha256:2835babf96dff90fe86e45f0fb9e476d1d6705a7a69a2819d0819854f1b612bb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.2 MB (225232047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edea99883fa4636fccfa4b0b112d15f032827d9554ad8e3291f0a45b8b25fd48`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:50 GMT
ADD file:9b846fb660cf816c4e731c6f547b8e389343bc05aa2ec510b1dfc2bddd4d1c8a in / 
# Wed, 24 Apr 2024 03:28:51 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 13:45:38 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 24 Apr 2024 13:45:47 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 24 Apr 2024 13:46:09 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 24 Apr 2024 13:52:09 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:74ff537ac401802b30ae451fd049f6337b6ed0ee93f7f7e1b00cc09b9ae7f2af`  
		Last Modified: Wed, 24 Apr 2024 03:33:56 GMT  
		Size: 27.3 MB (27337575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de69173ac5dc57b1bff6ca742571c692a9d0059ca5039f1546275a70eae8e66e`  
		Last Modified: Wed, 24 Apr 2024 13:52:54 GMT  
		Size: 2.8 MB (2780823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dadd7019a9ea55b7f9dbfca86a546e8846c9c203686b04dd273fd9b13aa2041`  
		Last Modified: Wed, 24 Apr 2024 13:53:03 GMT  
		Size: 64.8 MB (64780285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46de26ee7797d4777c37763e32361320626fb1e09d0a30e521c065ae2a1edddd`  
		Last Modified: Wed, 24 Apr 2024 13:54:08 GMT  
		Size: 130.3 MB (130333364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

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
$ docker pull mono@sha256:6072350263c1422bffa85718df883e3ce12ea3b2494868fad86af67e3cf61167
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.0 MB (176955353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ce8fec035219f1fe5b9e36df20454bd7c5f807b37082483781ed3d187e3fded`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 04:07:41 GMT
ADD file:985460a24e46cb6fd38e9ecdf21565547413f5f50d7c5c96d367b89aa94b91fa in / 
# Wed, 24 Apr 2024 04:07:41 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 07:03:32 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 24 Apr 2024 07:03:41 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 24 Apr 2024 07:04:01 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 24 Apr 2024 07:06:49 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a26123864d4d41f3f97e44b15f7ae2ecb9a15cbc37d6085d418a129976773e32`  
		Last Modified: Wed, 24 Apr 2024 04:12:31 GMT  
		Size: 22.9 MB (22945064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c20deacbb5552442449e92cfa65bb3e47b454eb158f7e02b73e26f0c451aa7d7`  
		Last Modified: Wed, 24 Apr 2024 07:07:37 GMT  
		Size: 2.4 MB (2370498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66a6381d33c325b2fc10fea2ccb3063ec32f09298fbcba6a5680adf58bea081b`  
		Last Modified: Wed, 24 Apr 2024 07:07:41 GMT  
		Size: 23.8 MB (23815984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a6328f4e34a27975511a13553d718dbf5851c9f562bd96cbd6a45da4bc79721`  
		Last Modified: Wed, 24 Apr 2024 07:08:52 GMT  
		Size: 127.8 MB (127823807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:8d9feaa88a3cb999e90781b597e1b0d245569c00d181ba5d49754b9ca2f511fb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.8 MB (203824562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f4ec35cda17fecea36cdd5bdbf3e31158dd5804f3cbafe49a31d9ad583fddbc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 00:40:08 GMT
ADD file:469a091f7763af8b8b723185853358a0516954941c82654915e259a2356612ae in / 
# Tue, 14 May 2024 00:40:08 GMT
CMD ["bash"]
# Tue, 14 May 2024 03:02:56 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 14 May 2024 03:03:04 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 14 May 2024 03:04:45 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 14 May 2024 03:13:02 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:ad8110ff35cfa20fc3638a9f2a63a1113c1e4f724bc3b8c11d7ae280154356ca`  
		Last Modified: Tue, 14 May 2024 00:44:04 GMT  
		Size: 26.1 MB (26109106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de210138ebc49b057b24b4ebfa1a1b2879b1e0db5d6dd499ee017d962487af73`  
		Last Modified: Tue, 14 May 2024 03:13:47 GMT  
		Size: 2.6 MB (2645569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:189a105128c26fd639e04ae79ae9dee9024b808475e0060f87f6e8ea2c842cd5`  
		Last Modified: Tue, 14 May 2024 03:13:51 GMT  
		Size: 29.6 MB (29575186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:309df2a030de7d30b87b24c401991712094e5a83beed5fb849171e8c3ab42d38`  
		Last Modified: Tue, 14 May 2024 03:14:50 GMT  
		Size: 145.5 MB (145494701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0` - linux; 386

```console
$ docker pull mono@sha256:976c308c970a488d2c3ff5348077a0ecd9363a870e830eae8683e916d250f3a9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.0 MB (231042464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4657bcf96ae2f5d9717b876758b9c137d832ae5440f6c3d6734077bc47fc116`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 00:47:54 GMT
ADD file:75dbbf2d7d721b8debce2bfecdbf3ea14eb9b4dfe8a6354a21dd21725cafaff8 in / 
# Tue, 14 May 2024 00:47:54 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:17:49 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 14 May 2024 01:18:00 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 14 May 2024 01:18:33 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 14 May 2024 01:23:27 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:261459e26de7bf625f6d2ad5439fdd881d51b8e9bc959e0f3eb3b67ebacc250f`  
		Last Modified: Tue, 14 May 2024 00:53:24 GMT  
		Size: 28.0 MB (27994475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d60b49ed6027113d5c2a31b5b98be0218f2e87f0203a1363a31ac4d30bbe3be`  
		Last Modified: Tue, 14 May 2024 01:24:25 GMT  
		Size: 2.8 MB (2792316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3252ffbfb712663e2665e56c94ac9a64b085bdebda6c3b18a61ddd1a6d001835`  
		Last Modified: Tue, 14 May 2024 01:24:39 GMT  
		Size: 68.8 MB (68809512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca930432a0d0862a13944f362fa095178ff23139e1149e5ef2b30702bea9f9df`  
		Last Modified: Tue, 14 May 2024 01:26:09 GMT  
		Size: 131.4 MB (131446161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

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
$ docker pull mono@sha256:c39dc0f28c8ed2dd04fde2c77bf2ea0cfae83256410d5ab7499737e118e630aa
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
$ docker pull mono@sha256:5775ef7a361f8db7d9e0592b937bd9b5ee10590eabfa05da5444aa49a11b1111
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.9 MB (94898683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cb1e72c2817f2e870b2b1faf088df393f0cc3c09269b3794025e6ee5fb71082`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:50 GMT
ADD file:9b846fb660cf816c4e731c6f547b8e389343bc05aa2ec510b1dfc2bddd4d1c8a in / 
# Wed, 24 Apr 2024 03:28:51 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 13:45:38 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 24 Apr 2024 13:45:47 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 24 Apr 2024 13:46:09 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:74ff537ac401802b30ae451fd049f6337b6ed0ee93f7f7e1b00cc09b9ae7f2af`  
		Last Modified: Wed, 24 Apr 2024 03:33:56 GMT  
		Size: 27.3 MB (27337575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de69173ac5dc57b1bff6ca742571c692a9d0059ca5039f1546275a70eae8e66e`  
		Last Modified: Wed, 24 Apr 2024 13:52:54 GMT  
		Size: 2.8 MB (2780823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dadd7019a9ea55b7f9dbfca86a546e8846c9c203686b04dd273fd9b13aa2041`  
		Last Modified: Wed, 24 Apr 2024 13:53:03 GMT  
		Size: 64.8 MB (64780285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

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
$ docker pull mono@sha256:a90f77ad468d1add8546223d8b6e5fd51a8f6e89bf0b76b90c24d018c82221cf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49131546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81b91c8ff16e8fa7d7c50a1ce5d562cbce1aafe0f49892f8848d50b7b073a2a4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 04:07:41 GMT
ADD file:985460a24e46cb6fd38e9ecdf21565547413f5f50d7c5c96d367b89aa94b91fa in / 
# Wed, 24 Apr 2024 04:07:41 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 07:03:32 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 24 Apr 2024 07:03:41 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 24 Apr 2024 07:04:01 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a26123864d4d41f3f97e44b15f7ae2ecb9a15cbc37d6085d418a129976773e32`  
		Last Modified: Wed, 24 Apr 2024 04:12:31 GMT  
		Size: 22.9 MB (22945064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c20deacbb5552442449e92cfa65bb3e47b454eb158f7e02b73e26f0c451aa7d7`  
		Last Modified: Wed, 24 Apr 2024 07:07:37 GMT  
		Size: 2.4 MB (2370498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66a6381d33c325b2fc10fea2ccb3063ec32f09298fbcba6a5680adf58bea081b`  
		Last Modified: Wed, 24 Apr 2024 07:07:41 GMT  
		Size: 23.8 MB (23815984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:5efcbde5e0f8fb609f2d83ff541a907f5f9ea6f81408bd7acf2c953e0bc2a65d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.3 MB (58329861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fb8af29a796e3c86fe790e994ac1ae11a80809fb4001e62609b748833b52f0e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 00:40:08 GMT
ADD file:469a091f7763af8b8b723185853358a0516954941c82654915e259a2356612ae in / 
# Tue, 14 May 2024 00:40:08 GMT
CMD ["bash"]
# Tue, 14 May 2024 03:02:56 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 14 May 2024 03:03:04 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 14 May 2024 03:04:45 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:ad8110ff35cfa20fc3638a9f2a63a1113c1e4f724bc3b8c11d7ae280154356ca`  
		Last Modified: Tue, 14 May 2024 00:44:04 GMT  
		Size: 26.1 MB (26109106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de210138ebc49b057b24b4ebfa1a1b2879b1e0db5d6dd499ee017d962487af73`  
		Last Modified: Tue, 14 May 2024 03:13:47 GMT  
		Size: 2.6 MB (2645569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:189a105128c26fd639e04ae79ae9dee9024b808475e0060f87f6e8ea2c842cd5`  
		Last Modified: Tue, 14 May 2024 03:13:51 GMT  
		Size: 29.6 MB (29575186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0-slim` - linux; 386

```console
$ docker pull mono@sha256:77d4a1a1db1496d5cdbe58891e11ba0c64a12c1bd66a078d0e890c5454450ad5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.6 MB (99596303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dda2618a8f113f6462ef8fd3d33a14a3b4daecdb03db4de5e6ecbcf9b9d5750e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 00:47:54 GMT
ADD file:75dbbf2d7d721b8debce2bfecdbf3ea14eb9b4dfe8a6354a21dd21725cafaff8 in / 
# Tue, 14 May 2024 00:47:54 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:17:49 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 14 May 2024 01:18:00 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 14 May 2024 01:18:33 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:261459e26de7bf625f6d2ad5439fdd881d51b8e9bc959e0f3eb3b67ebacc250f`  
		Last Modified: Tue, 14 May 2024 00:53:24 GMT  
		Size: 28.0 MB (27994475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d60b49ed6027113d5c2a31b5b98be0218f2e87f0203a1363a31ac4d30bbe3be`  
		Last Modified: Tue, 14 May 2024 01:24:25 GMT  
		Size: 2.8 MB (2792316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3252ffbfb712663e2665e56c94ac9a64b085bdebda6c3b18a61ddd1a6d001835`  
		Last Modified: Tue, 14 May 2024 01:24:39 GMT  
		Size: 68.8 MB (68809512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

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
$ docker pull mono@sha256:b229c98da12419ddf62c0e49ead7a8b28a52bc52ee30d211286c3ff3b350d7f1
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
$ docker pull mono@sha256:2835babf96dff90fe86e45f0fb9e476d1d6705a7a69a2819d0819854f1b612bb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.2 MB (225232047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edea99883fa4636fccfa4b0b112d15f032827d9554ad8e3291f0a45b8b25fd48`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:50 GMT
ADD file:9b846fb660cf816c4e731c6f547b8e389343bc05aa2ec510b1dfc2bddd4d1c8a in / 
# Wed, 24 Apr 2024 03:28:51 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 13:45:38 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 24 Apr 2024 13:45:47 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 24 Apr 2024 13:46:09 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 24 Apr 2024 13:52:09 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:74ff537ac401802b30ae451fd049f6337b6ed0ee93f7f7e1b00cc09b9ae7f2af`  
		Last Modified: Wed, 24 Apr 2024 03:33:56 GMT  
		Size: 27.3 MB (27337575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de69173ac5dc57b1bff6ca742571c692a9d0059ca5039f1546275a70eae8e66e`  
		Last Modified: Wed, 24 Apr 2024 13:52:54 GMT  
		Size: 2.8 MB (2780823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dadd7019a9ea55b7f9dbfca86a546e8846c9c203686b04dd273fd9b13aa2041`  
		Last Modified: Wed, 24 Apr 2024 13:53:03 GMT  
		Size: 64.8 MB (64780285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46de26ee7797d4777c37763e32361320626fb1e09d0a30e521c065ae2a1edddd`  
		Last Modified: Wed, 24 Apr 2024 13:54:08 GMT  
		Size: 130.3 MB (130333364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

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
$ docker pull mono@sha256:6072350263c1422bffa85718df883e3ce12ea3b2494868fad86af67e3cf61167
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.0 MB (176955353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ce8fec035219f1fe5b9e36df20454bd7c5f807b37082483781ed3d187e3fded`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 04:07:41 GMT
ADD file:985460a24e46cb6fd38e9ecdf21565547413f5f50d7c5c96d367b89aa94b91fa in / 
# Wed, 24 Apr 2024 04:07:41 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 07:03:32 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 24 Apr 2024 07:03:41 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 24 Apr 2024 07:04:01 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 24 Apr 2024 07:06:49 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a26123864d4d41f3f97e44b15f7ae2ecb9a15cbc37d6085d418a129976773e32`  
		Last Modified: Wed, 24 Apr 2024 04:12:31 GMT  
		Size: 22.9 MB (22945064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c20deacbb5552442449e92cfa65bb3e47b454eb158f7e02b73e26f0c451aa7d7`  
		Last Modified: Wed, 24 Apr 2024 07:07:37 GMT  
		Size: 2.4 MB (2370498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66a6381d33c325b2fc10fea2ccb3063ec32f09298fbcba6a5680adf58bea081b`  
		Last Modified: Wed, 24 Apr 2024 07:07:41 GMT  
		Size: 23.8 MB (23815984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a6328f4e34a27975511a13553d718dbf5851c9f562bd96cbd6a45da4bc79721`  
		Last Modified: Wed, 24 Apr 2024 07:08:52 GMT  
		Size: 127.8 MB (127823807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0.104` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:8d9feaa88a3cb999e90781b597e1b0d245569c00d181ba5d49754b9ca2f511fb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.8 MB (203824562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f4ec35cda17fecea36cdd5bdbf3e31158dd5804f3cbafe49a31d9ad583fddbc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 00:40:08 GMT
ADD file:469a091f7763af8b8b723185853358a0516954941c82654915e259a2356612ae in / 
# Tue, 14 May 2024 00:40:08 GMT
CMD ["bash"]
# Tue, 14 May 2024 03:02:56 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 14 May 2024 03:03:04 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 14 May 2024 03:04:45 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 14 May 2024 03:13:02 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:ad8110ff35cfa20fc3638a9f2a63a1113c1e4f724bc3b8c11d7ae280154356ca`  
		Last Modified: Tue, 14 May 2024 00:44:04 GMT  
		Size: 26.1 MB (26109106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de210138ebc49b057b24b4ebfa1a1b2879b1e0db5d6dd499ee017d962487af73`  
		Last Modified: Tue, 14 May 2024 03:13:47 GMT  
		Size: 2.6 MB (2645569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:189a105128c26fd639e04ae79ae9dee9024b808475e0060f87f6e8ea2c842cd5`  
		Last Modified: Tue, 14 May 2024 03:13:51 GMT  
		Size: 29.6 MB (29575186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:309df2a030de7d30b87b24c401991712094e5a83beed5fb849171e8c3ab42d38`  
		Last Modified: Tue, 14 May 2024 03:14:50 GMT  
		Size: 145.5 MB (145494701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0.104` - linux; 386

```console
$ docker pull mono@sha256:976c308c970a488d2c3ff5348077a0ecd9363a870e830eae8683e916d250f3a9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.0 MB (231042464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4657bcf96ae2f5d9717b876758b9c137d832ae5440f6c3d6734077bc47fc116`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 00:47:54 GMT
ADD file:75dbbf2d7d721b8debce2bfecdbf3ea14eb9b4dfe8a6354a21dd21725cafaff8 in / 
# Tue, 14 May 2024 00:47:54 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:17:49 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 14 May 2024 01:18:00 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 14 May 2024 01:18:33 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 14 May 2024 01:23:27 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:261459e26de7bf625f6d2ad5439fdd881d51b8e9bc959e0f3eb3b67ebacc250f`  
		Last Modified: Tue, 14 May 2024 00:53:24 GMT  
		Size: 28.0 MB (27994475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d60b49ed6027113d5c2a31b5b98be0218f2e87f0203a1363a31ac4d30bbe3be`  
		Last Modified: Tue, 14 May 2024 01:24:25 GMT  
		Size: 2.8 MB (2792316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3252ffbfb712663e2665e56c94ac9a64b085bdebda6c3b18a61ddd1a6d001835`  
		Last Modified: Tue, 14 May 2024 01:24:39 GMT  
		Size: 68.8 MB (68809512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca930432a0d0862a13944f362fa095178ff23139e1149e5ef2b30702bea9f9df`  
		Last Modified: Tue, 14 May 2024 01:26:09 GMT  
		Size: 131.4 MB (131446161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

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
$ docker pull mono@sha256:c39dc0f28c8ed2dd04fde2c77bf2ea0cfae83256410d5ab7499737e118e630aa
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
$ docker pull mono@sha256:5775ef7a361f8db7d9e0592b937bd9b5ee10590eabfa05da5444aa49a11b1111
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.9 MB (94898683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cb1e72c2817f2e870b2b1faf088df393f0cc3c09269b3794025e6ee5fb71082`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:50 GMT
ADD file:9b846fb660cf816c4e731c6f547b8e389343bc05aa2ec510b1dfc2bddd4d1c8a in / 
# Wed, 24 Apr 2024 03:28:51 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 13:45:38 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 24 Apr 2024 13:45:47 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 24 Apr 2024 13:46:09 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:74ff537ac401802b30ae451fd049f6337b6ed0ee93f7f7e1b00cc09b9ae7f2af`  
		Last Modified: Wed, 24 Apr 2024 03:33:56 GMT  
		Size: 27.3 MB (27337575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de69173ac5dc57b1bff6ca742571c692a9d0059ca5039f1546275a70eae8e66e`  
		Last Modified: Wed, 24 Apr 2024 13:52:54 GMT  
		Size: 2.8 MB (2780823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dadd7019a9ea55b7f9dbfca86a546e8846c9c203686b04dd273fd9b13aa2041`  
		Last Modified: Wed, 24 Apr 2024 13:53:03 GMT  
		Size: 64.8 MB (64780285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

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
$ docker pull mono@sha256:a90f77ad468d1add8546223d8b6e5fd51a8f6e89bf0b76b90c24d018c82221cf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49131546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81b91c8ff16e8fa7d7c50a1ce5d562cbce1aafe0f49892f8848d50b7b073a2a4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 04:07:41 GMT
ADD file:985460a24e46cb6fd38e9ecdf21565547413f5f50d7c5c96d367b89aa94b91fa in / 
# Wed, 24 Apr 2024 04:07:41 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 07:03:32 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 24 Apr 2024 07:03:41 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 24 Apr 2024 07:04:01 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a26123864d4d41f3f97e44b15f7ae2ecb9a15cbc37d6085d418a129976773e32`  
		Last Modified: Wed, 24 Apr 2024 04:12:31 GMT  
		Size: 22.9 MB (22945064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c20deacbb5552442449e92cfa65bb3e47b454eb158f7e02b73e26f0c451aa7d7`  
		Last Modified: Wed, 24 Apr 2024 07:07:37 GMT  
		Size: 2.4 MB (2370498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66a6381d33c325b2fc10fea2ccb3063ec32f09298fbcba6a5680adf58bea081b`  
		Last Modified: Wed, 24 Apr 2024 07:07:41 GMT  
		Size: 23.8 MB (23815984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0.104-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:5efcbde5e0f8fb609f2d83ff541a907f5f9ea6f81408bd7acf2c953e0bc2a65d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.3 MB (58329861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fb8af29a796e3c86fe790e994ac1ae11a80809fb4001e62609b748833b52f0e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 00:40:08 GMT
ADD file:469a091f7763af8b8b723185853358a0516954941c82654915e259a2356612ae in / 
# Tue, 14 May 2024 00:40:08 GMT
CMD ["bash"]
# Tue, 14 May 2024 03:02:56 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 14 May 2024 03:03:04 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 14 May 2024 03:04:45 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:ad8110ff35cfa20fc3638a9f2a63a1113c1e4f724bc3b8c11d7ae280154356ca`  
		Last Modified: Tue, 14 May 2024 00:44:04 GMT  
		Size: 26.1 MB (26109106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de210138ebc49b057b24b4ebfa1a1b2879b1e0db5d6dd499ee017d962487af73`  
		Last Modified: Tue, 14 May 2024 03:13:47 GMT  
		Size: 2.6 MB (2645569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:189a105128c26fd639e04ae79ae9dee9024b808475e0060f87f6e8ea2c842cd5`  
		Last Modified: Tue, 14 May 2024 03:13:51 GMT  
		Size: 29.6 MB (29575186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0.104-slim` - linux; 386

```console
$ docker pull mono@sha256:77d4a1a1db1496d5cdbe58891e11ba0c64a12c1bd66a078d0e890c5454450ad5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.6 MB (99596303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dda2618a8f113f6462ef8fd3d33a14a3b4daecdb03db4de5e6ecbcf9b9d5750e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 00:47:54 GMT
ADD file:75dbbf2d7d721b8debce2bfecdbf3ea14eb9b4dfe8a6354a21dd21725cafaff8 in / 
# Tue, 14 May 2024 00:47:54 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:17:49 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 14 May 2024 01:18:00 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 14 May 2024 01:18:33 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:261459e26de7bf625f6d2ad5439fdd881d51b8e9bc959e0f3eb3b67ebacc250f`  
		Last Modified: Tue, 14 May 2024 00:53:24 GMT  
		Size: 28.0 MB (27994475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d60b49ed6027113d5c2a31b5b98be0218f2e87f0203a1363a31ac4d30bbe3be`  
		Last Modified: Tue, 14 May 2024 01:24:25 GMT  
		Size: 2.8 MB (2792316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3252ffbfb712663e2665e56c94ac9a64b085bdebda6c3b18a61ddd1a6d001835`  
		Last Modified: Tue, 14 May 2024 01:24:39 GMT  
		Size: 68.8 MB (68809512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

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
$ docker pull mono@sha256:86767b090cf14a50f9f006191e72be7fa71c0a0eda8afcc56c0d6f1031110fa7
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
$ docker pull mono@sha256:fd331c4c7a1b2b895a97f4e7829e8f40045c2dcab4156a2c1f13f1a17d58ad21
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.8 MB (254822861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1c1a10a5340e5cc64fa235e6d0d4baf42815e4de3f3389e0d10c302b2604b9b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:50 GMT
ADD file:9b846fb660cf816c4e731c6f547b8e389343bc05aa2ec510b1dfc2bddd4d1c8a in / 
# Wed, 24 Apr 2024 03:28:51 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 13:44:56 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 24 Apr 2024 13:45:07 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 24 Apr 2024 13:45:29 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 24 Apr 2024 13:47:22 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:74ff537ac401802b30ae451fd049f6337b6ed0ee93f7f7e1b00cc09b9ae7f2af`  
		Last Modified: Wed, 24 Apr 2024 03:33:56 GMT  
		Size: 27.3 MB (27337575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ffd837dfe32dada37b2b83dc3294fdb8c5b1aa8e9d843a9d939191c5358a355`  
		Last Modified: Wed, 24 Apr 2024 13:52:29 GMT  
		Size: 2.8 MB (2780777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acc88837dcf46a86e66bf61f6da043eac5337cd9d1bb0b8771350b1a536ffdc1`  
		Last Modified: Wed, 24 Apr 2024 13:52:38 GMT  
		Size: 64.8 MB (64773978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9f93b564c87b034a6f8e8f6fb69a30afc9e039b5220024dae7bb2f6f40659ce`  
		Last Modified: Wed, 24 Apr 2024 13:53:36 GMT  
		Size: 159.9 MB (159930531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

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
$ docker pull mono@sha256:bd8a12d74ce824caff0f9f8958c7bcfffb892449f02a0e4df9cf6e8192b54176
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.2 MB (189166436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cb250b5d8f4152de3c52f3965099ebcfa87068ef5395e9795797f24516e93a0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 04:07:41 GMT
ADD file:985460a24e46cb6fd38e9ecdf21565547413f5f50d7c5c96d367b89aa94b91fa in / 
# Wed, 24 Apr 2024 04:07:41 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 07:02:59 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 24 Apr 2024 07:03:11 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 24 Apr 2024 07:03:30 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 24 Apr 2024 07:05:23 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a26123864d4d41f3f97e44b15f7ae2ecb9a15cbc37d6085d418a129976773e32`  
		Last Modified: Wed, 24 Apr 2024 04:12:31 GMT  
		Size: 22.9 MB (22945064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e354d269265092711be691142d28fc8002953b5bfb897dbd91cd4789aa0d7f2c`  
		Last Modified: Wed, 24 Apr 2024 07:07:19 GMT  
		Size: 2.4 MB (2370522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce30d34e592060862296941593408133f444860b8431bd82c0f709acf3400dac`  
		Last Modified: Wed, 24 Apr 2024 07:07:23 GMT  
		Size: 23.8 MB (23790719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0cf8b7baf15a56b76905e86633595d7d9f122406ce84adb136eb23cf3619250`  
		Last Modified: Wed, 24 Apr 2024 07:08:15 GMT  
		Size: 140.1 MB (140060131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:e315d205d62cd6c04d52b11ecaf05e16c4f51b7eba142a8852e042c0283c1b01
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.6 MB (216552462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61d85bf404e8cc493498953016e368e84808ab7154fb3b866fb9b0257e80dcbb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 00:40:08 GMT
ADD file:469a091f7763af8b8b723185853358a0516954941c82654915e259a2356612ae in / 
# Tue, 14 May 2024 00:40:08 GMT
CMD ["bash"]
# Tue, 14 May 2024 03:01:03 GMT
ENV MONO_VERSION=6.12.0.182
# Tue, 14 May 2024 03:01:12 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 14 May 2024 03:02:44 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 14 May 2024 03:06:59 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:ad8110ff35cfa20fc3638a9f2a63a1113c1e4f724bc3b8c11d7ae280154356ca`  
		Last Modified: Tue, 14 May 2024 00:44:04 GMT  
		Size: 26.1 MB (26109106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a529a8ce298691a652a87333069ec6318e368ff0af7e2171b0ec58c5bf349dd8`  
		Last Modified: Tue, 14 May 2024 03:13:31 GMT  
		Size: 2.6 MB (2645561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79c2d783bd9b494f35fa932c80b7d810922f24489d8661f9f7e6626244d07bad`  
		Last Modified: Tue, 14 May 2024 03:13:34 GMT  
		Size: 29.5 MB (29545286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4ec1315f421edc1ff66ccc5ba4bcdd5d658530a2364f7438d255c14e6d80366`  
		Last Modified: Tue, 14 May 2024 03:14:19 GMT  
		Size: 158.3 MB (158252509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12` - linux; 386

```console
$ docker pull mono@sha256:067ca9a38acaaf9fdea29d7de110e8fd76261197be74a6b479b610eedd5a9b3d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.7 MB (259701817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:883e88334262384fea165fb01f2ec11dde2d61bc921c9f3bd6b3f1489f83d508`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 00:47:54 GMT
ADD file:75dbbf2d7d721b8debce2bfecdbf3ea14eb9b4dfe8a6354a21dd21725cafaff8 in / 
# Tue, 14 May 2024 00:47:54 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:16:51 GMT
ENV MONO_VERSION=6.12.0.182
# Tue, 14 May 2024 01:17:03 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 14 May 2024 01:17:39 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 14 May 2024 01:21:06 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:261459e26de7bf625f6d2ad5439fdd881d51b8e9bc959e0f3eb3b67ebacc250f`  
		Last Modified: Tue, 14 May 2024 00:53:24 GMT  
		Size: 28.0 MB (27994475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:036bbf0cc3e0f790c56486ebf068c9323a5e7716334c0114c7e3551fd1005100`  
		Last Modified: Tue, 14 May 2024 01:23:54 GMT  
		Size: 2.8 MB (2792366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb6f765ea19029790391afd07a05f782804dc82a94340049c2ad63c4eade3caf`  
		Last Modified: Tue, 14 May 2024 01:24:08 GMT  
		Size: 68.8 MB (68800484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47f132e8616f7a3f460f3dd4f3369385c8c9b4d238922ab196b9e2387f25e5c3`  
		Last Modified: Tue, 14 May 2024 01:25:24 GMT  
		Size: 160.1 MB (160114492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

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
$ docker pull mono@sha256:6d47290645de36eb0f9185f3794730b07d931e71dd1f01749ae3a117adafa41b
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
$ docker pull mono@sha256:0749e711811842967d725da21612af6129be80c84e3ed529fb700cfbf81e455d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.9 MB (94892330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:593772cbcad062ca2e93e73111024a35645d7510a450b015dbe1012eb08b05fc`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:50 GMT
ADD file:9b846fb660cf816c4e731c6f547b8e389343bc05aa2ec510b1dfc2bddd4d1c8a in / 
# Wed, 24 Apr 2024 03:28:51 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 13:44:56 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 24 Apr 2024 13:45:07 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 24 Apr 2024 13:45:29 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:74ff537ac401802b30ae451fd049f6337b6ed0ee93f7f7e1b00cc09b9ae7f2af`  
		Last Modified: Wed, 24 Apr 2024 03:33:56 GMT  
		Size: 27.3 MB (27337575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ffd837dfe32dada37b2b83dc3294fdb8c5b1aa8e9d843a9d939191c5358a355`  
		Last Modified: Wed, 24 Apr 2024 13:52:29 GMT  
		Size: 2.8 MB (2780777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acc88837dcf46a86e66bf61f6da043eac5337cd9d1bb0b8771350b1a536ffdc1`  
		Last Modified: Wed, 24 Apr 2024 13:52:38 GMT  
		Size: 64.8 MB (64773978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

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
$ docker pull mono@sha256:fa609c04866c144a99440dc2501eb77993b62e2a149d5fe1781a0539a5af518b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49106305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:634defc256033a7bfb1b71133d25e64724d595feb9f1d983b457847c7773360e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 04:07:41 GMT
ADD file:985460a24e46cb6fd38e9ecdf21565547413f5f50d7c5c96d367b89aa94b91fa in / 
# Wed, 24 Apr 2024 04:07:41 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 07:02:59 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 24 Apr 2024 07:03:11 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 24 Apr 2024 07:03:30 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a26123864d4d41f3f97e44b15f7ae2ecb9a15cbc37d6085d418a129976773e32`  
		Last Modified: Wed, 24 Apr 2024 04:12:31 GMT  
		Size: 22.9 MB (22945064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e354d269265092711be691142d28fc8002953b5bfb897dbd91cd4789aa0d7f2c`  
		Last Modified: Wed, 24 Apr 2024 07:07:19 GMT  
		Size: 2.4 MB (2370522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce30d34e592060862296941593408133f444860b8431bd82c0f709acf3400dac`  
		Last Modified: Wed, 24 Apr 2024 07:07:23 GMT  
		Size: 23.8 MB (23790719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:e2727d8c2692fbaf5a3abaaf56a98d49a6e5b24ff7c727cb564f88ad2cb240bc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.3 MB (58299953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9dcf5344b0840b1056715bc2ba296aed99407dab01e0c67ab889f9980e8e77b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 00:40:08 GMT
ADD file:469a091f7763af8b8b723185853358a0516954941c82654915e259a2356612ae in / 
# Tue, 14 May 2024 00:40:08 GMT
CMD ["bash"]
# Tue, 14 May 2024 03:01:03 GMT
ENV MONO_VERSION=6.12.0.182
# Tue, 14 May 2024 03:01:12 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 14 May 2024 03:02:44 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:ad8110ff35cfa20fc3638a9f2a63a1113c1e4f724bc3b8c11d7ae280154356ca`  
		Last Modified: Tue, 14 May 2024 00:44:04 GMT  
		Size: 26.1 MB (26109106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a529a8ce298691a652a87333069ec6318e368ff0af7e2171b0ec58c5bf349dd8`  
		Last Modified: Tue, 14 May 2024 03:13:31 GMT  
		Size: 2.6 MB (2645561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79c2d783bd9b494f35fa932c80b7d810922f24489d8661f9f7e6626244d07bad`  
		Last Modified: Tue, 14 May 2024 03:13:34 GMT  
		Size: 29.5 MB (29545286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12-slim` - linux; 386

```console
$ docker pull mono@sha256:7290a085e73bf2acdf312667141ed3060c3ecbbcdabd4e2f345865b5e8090612
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.6 MB (99587325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0122e8a6790708e8b29c1a50eb7a19482e2483089f00f9c46226457b9baa8325`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 00:47:54 GMT
ADD file:75dbbf2d7d721b8debce2bfecdbf3ea14eb9b4dfe8a6354a21dd21725cafaff8 in / 
# Tue, 14 May 2024 00:47:54 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:16:51 GMT
ENV MONO_VERSION=6.12.0.182
# Tue, 14 May 2024 01:17:03 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 14 May 2024 01:17:39 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:261459e26de7bf625f6d2ad5439fdd881d51b8e9bc959e0f3eb3b67ebacc250f`  
		Last Modified: Tue, 14 May 2024 00:53:24 GMT  
		Size: 28.0 MB (27994475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:036bbf0cc3e0f790c56486ebf068c9323a5e7716334c0114c7e3551fd1005100`  
		Last Modified: Tue, 14 May 2024 01:23:54 GMT  
		Size: 2.8 MB (2792366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb6f765ea19029790391afd07a05f782804dc82a94340049c2ad63c4eade3caf`  
		Last Modified: Tue, 14 May 2024 01:24:08 GMT  
		Size: 68.8 MB (68800484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

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
$ docker pull mono@sha256:86767b090cf14a50f9f006191e72be7fa71c0a0eda8afcc56c0d6f1031110fa7
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
$ docker pull mono@sha256:fd331c4c7a1b2b895a97f4e7829e8f40045c2dcab4156a2c1f13f1a17d58ad21
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.8 MB (254822861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1c1a10a5340e5cc64fa235e6d0d4baf42815e4de3f3389e0d10c302b2604b9b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:50 GMT
ADD file:9b846fb660cf816c4e731c6f547b8e389343bc05aa2ec510b1dfc2bddd4d1c8a in / 
# Wed, 24 Apr 2024 03:28:51 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 13:44:56 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 24 Apr 2024 13:45:07 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 24 Apr 2024 13:45:29 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 24 Apr 2024 13:47:22 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:74ff537ac401802b30ae451fd049f6337b6ed0ee93f7f7e1b00cc09b9ae7f2af`  
		Last Modified: Wed, 24 Apr 2024 03:33:56 GMT  
		Size: 27.3 MB (27337575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ffd837dfe32dada37b2b83dc3294fdb8c5b1aa8e9d843a9d939191c5358a355`  
		Last Modified: Wed, 24 Apr 2024 13:52:29 GMT  
		Size: 2.8 MB (2780777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acc88837dcf46a86e66bf61f6da043eac5337cd9d1bb0b8771350b1a536ffdc1`  
		Last Modified: Wed, 24 Apr 2024 13:52:38 GMT  
		Size: 64.8 MB (64773978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9f93b564c87b034a6f8e8f6fb69a30afc9e039b5220024dae7bb2f6f40659ce`  
		Last Modified: Wed, 24 Apr 2024 13:53:36 GMT  
		Size: 159.9 MB (159930531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

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
$ docker pull mono@sha256:bd8a12d74ce824caff0f9f8958c7bcfffb892449f02a0e4df9cf6e8192b54176
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.2 MB (189166436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cb250b5d8f4152de3c52f3965099ebcfa87068ef5395e9795797f24516e93a0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 04:07:41 GMT
ADD file:985460a24e46cb6fd38e9ecdf21565547413f5f50d7c5c96d367b89aa94b91fa in / 
# Wed, 24 Apr 2024 04:07:41 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 07:02:59 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 24 Apr 2024 07:03:11 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 24 Apr 2024 07:03:30 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 24 Apr 2024 07:05:23 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a26123864d4d41f3f97e44b15f7ae2ecb9a15cbc37d6085d418a129976773e32`  
		Last Modified: Wed, 24 Apr 2024 04:12:31 GMT  
		Size: 22.9 MB (22945064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e354d269265092711be691142d28fc8002953b5bfb897dbd91cd4789aa0d7f2c`  
		Last Modified: Wed, 24 Apr 2024 07:07:19 GMT  
		Size: 2.4 MB (2370522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce30d34e592060862296941593408133f444860b8431bd82c0f709acf3400dac`  
		Last Modified: Wed, 24 Apr 2024 07:07:23 GMT  
		Size: 23.8 MB (23790719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0cf8b7baf15a56b76905e86633595d7d9f122406ce84adb136eb23cf3619250`  
		Last Modified: Wed, 24 Apr 2024 07:08:15 GMT  
		Size: 140.1 MB (140060131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:e315d205d62cd6c04d52b11ecaf05e16c4f51b7eba142a8852e042c0283c1b01
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.6 MB (216552462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61d85bf404e8cc493498953016e368e84808ab7154fb3b866fb9b0257e80dcbb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 00:40:08 GMT
ADD file:469a091f7763af8b8b723185853358a0516954941c82654915e259a2356612ae in / 
# Tue, 14 May 2024 00:40:08 GMT
CMD ["bash"]
# Tue, 14 May 2024 03:01:03 GMT
ENV MONO_VERSION=6.12.0.182
# Tue, 14 May 2024 03:01:12 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 14 May 2024 03:02:44 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 14 May 2024 03:06:59 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:ad8110ff35cfa20fc3638a9f2a63a1113c1e4f724bc3b8c11d7ae280154356ca`  
		Last Modified: Tue, 14 May 2024 00:44:04 GMT  
		Size: 26.1 MB (26109106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a529a8ce298691a652a87333069ec6318e368ff0af7e2171b0ec58c5bf349dd8`  
		Last Modified: Tue, 14 May 2024 03:13:31 GMT  
		Size: 2.6 MB (2645561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79c2d783bd9b494f35fa932c80b7d810922f24489d8661f9f7e6626244d07bad`  
		Last Modified: Tue, 14 May 2024 03:13:34 GMT  
		Size: 29.5 MB (29545286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4ec1315f421edc1ff66ccc5ba4bcdd5d658530a2364f7438d255c14e6d80366`  
		Last Modified: Tue, 14 May 2024 03:14:19 GMT  
		Size: 158.3 MB (158252509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0` - linux; 386

```console
$ docker pull mono@sha256:067ca9a38acaaf9fdea29d7de110e8fd76261197be74a6b479b610eedd5a9b3d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.7 MB (259701817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:883e88334262384fea165fb01f2ec11dde2d61bc921c9f3bd6b3f1489f83d508`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 00:47:54 GMT
ADD file:75dbbf2d7d721b8debce2bfecdbf3ea14eb9b4dfe8a6354a21dd21725cafaff8 in / 
# Tue, 14 May 2024 00:47:54 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:16:51 GMT
ENV MONO_VERSION=6.12.0.182
# Tue, 14 May 2024 01:17:03 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 14 May 2024 01:17:39 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 14 May 2024 01:21:06 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:261459e26de7bf625f6d2ad5439fdd881d51b8e9bc959e0f3eb3b67ebacc250f`  
		Last Modified: Tue, 14 May 2024 00:53:24 GMT  
		Size: 28.0 MB (27994475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:036bbf0cc3e0f790c56486ebf068c9323a5e7716334c0114c7e3551fd1005100`  
		Last Modified: Tue, 14 May 2024 01:23:54 GMT  
		Size: 2.8 MB (2792366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb6f765ea19029790391afd07a05f782804dc82a94340049c2ad63c4eade3caf`  
		Last Modified: Tue, 14 May 2024 01:24:08 GMT  
		Size: 68.8 MB (68800484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47f132e8616f7a3f460f3dd4f3369385c8c9b4d238922ab196b9e2387f25e5c3`  
		Last Modified: Tue, 14 May 2024 01:25:24 GMT  
		Size: 160.1 MB (160114492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

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
$ docker pull mono@sha256:6d47290645de36eb0f9185f3794730b07d931e71dd1f01749ae3a117adafa41b
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
$ docker pull mono@sha256:0749e711811842967d725da21612af6129be80c84e3ed529fb700cfbf81e455d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.9 MB (94892330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:593772cbcad062ca2e93e73111024a35645d7510a450b015dbe1012eb08b05fc`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:50 GMT
ADD file:9b846fb660cf816c4e731c6f547b8e389343bc05aa2ec510b1dfc2bddd4d1c8a in / 
# Wed, 24 Apr 2024 03:28:51 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 13:44:56 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 24 Apr 2024 13:45:07 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 24 Apr 2024 13:45:29 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:74ff537ac401802b30ae451fd049f6337b6ed0ee93f7f7e1b00cc09b9ae7f2af`  
		Last Modified: Wed, 24 Apr 2024 03:33:56 GMT  
		Size: 27.3 MB (27337575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ffd837dfe32dada37b2b83dc3294fdb8c5b1aa8e9d843a9d939191c5358a355`  
		Last Modified: Wed, 24 Apr 2024 13:52:29 GMT  
		Size: 2.8 MB (2780777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acc88837dcf46a86e66bf61f6da043eac5337cd9d1bb0b8771350b1a536ffdc1`  
		Last Modified: Wed, 24 Apr 2024 13:52:38 GMT  
		Size: 64.8 MB (64773978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

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
$ docker pull mono@sha256:fa609c04866c144a99440dc2501eb77993b62e2a149d5fe1781a0539a5af518b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49106305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:634defc256033a7bfb1b71133d25e64724d595feb9f1d983b457847c7773360e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 04:07:41 GMT
ADD file:985460a24e46cb6fd38e9ecdf21565547413f5f50d7c5c96d367b89aa94b91fa in / 
# Wed, 24 Apr 2024 04:07:41 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 07:02:59 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 24 Apr 2024 07:03:11 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 24 Apr 2024 07:03:30 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a26123864d4d41f3f97e44b15f7ae2ecb9a15cbc37d6085d418a129976773e32`  
		Last Modified: Wed, 24 Apr 2024 04:12:31 GMT  
		Size: 22.9 MB (22945064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e354d269265092711be691142d28fc8002953b5bfb897dbd91cd4789aa0d7f2c`  
		Last Modified: Wed, 24 Apr 2024 07:07:19 GMT  
		Size: 2.4 MB (2370522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce30d34e592060862296941593408133f444860b8431bd82c0f709acf3400dac`  
		Last Modified: Wed, 24 Apr 2024 07:07:23 GMT  
		Size: 23.8 MB (23790719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:e2727d8c2692fbaf5a3abaaf56a98d49a6e5b24ff7c727cb564f88ad2cb240bc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.3 MB (58299953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9dcf5344b0840b1056715bc2ba296aed99407dab01e0c67ab889f9980e8e77b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 00:40:08 GMT
ADD file:469a091f7763af8b8b723185853358a0516954941c82654915e259a2356612ae in / 
# Tue, 14 May 2024 00:40:08 GMT
CMD ["bash"]
# Tue, 14 May 2024 03:01:03 GMT
ENV MONO_VERSION=6.12.0.182
# Tue, 14 May 2024 03:01:12 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 14 May 2024 03:02:44 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:ad8110ff35cfa20fc3638a9f2a63a1113c1e4f724bc3b8c11d7ae280154356ca`  
		Last Modified: Tue, 14 May 2024 00:44:04 GMT  
		Size: 26.1 MB (26109106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a529a8ce298691a652a87333069ec6318e368ff0af7e2171b0ec58c5bf349dd8`  
		Last Modified: Tue, 14 May 2024 03:13:31 GMT  
		Size: 2.6 MB (2645561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79c2d783bd9b494f35fa932c80b7d810922f24489d8661f9f7e6626244d07bad`  
		Last Modified: Tue, 14 May 2024 03:13:34 GMT  
		Size: 29.5 MB (29545286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0-slim` - linux; 386

```console
$ docker pull mono@sha256:7290a085e73bf2acdf312667141ed3060c3ecbbcdabd4e2f345865b5e8090612
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.6 MB (99587325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0122e8a6790708e8b29c1a50eb7a19482e2483089f00f9c46226457b9baa8325`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 00:47:54 GMT
ADD file:75dbbf2d7d721b8debce2bfecdbf3ea14eb9b4dfe8a6354a21dd21725cafaff8 in / 
# Tue, 14 May 2024 00:47:54 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:16:51 GMT
ENV MONO_VERSION=6.12.0.182
# Tue, 14 May 2024 01:17:03 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 14 May 2024 01:17:39 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:261459e26de7bf625f6d2ad5439fdd881d51b8e9bc959e0f3eb3b67ebacc250f`  
		Last Modified: Tue, 14 May 2024 00:53:24 GMT  
		Size: 28.0 MB (27994475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:036bbf0cc3e0f790c56486ebf068c9323a5e7716334c0114c7e3551fd1005100`  
		Last Modified: Tue, 14 May 2024 01:23:54 GMT  
		Size: 2.8 MB (2792366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb6f765ea19029790391afd07a05f782804dc82a94340049c2ad63c4eade3caf`  
		Last Modified: Tue, 14 May 2024 01:24:08 GMT  
		Size: 68.8 MB (68800484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

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
$ docker pull mono@sha256:86767b090cf14a50f9f006191e72be7fa71c0a0eda8afcc56c0d6f1031110fa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:6.12.0.182` - linux; amd64

```console
$ docker pull mono@sha256:fd331c4c7a1b2b895a97f4e7829e8f40045c2dcab4156a2c1f13f1a17d58ad21
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.8 MB (254822861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1c1a10a5340e5cc64fa235e6d0d4baf42815e4de3f3389e0d10c302b2604b9b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:50 GMT
ADD file:9b846fb660cf816c4e731c6f547b8e389343bc05aa2ec510b1dfc2bddd4d1c8a in / 
# Wed, 24 Apr 2024 03:28:51 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 13:44:56 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 24 Apr 2024 13:45:07 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 24 Apr 2024 13:45:29 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 24 Apr 2024 13:47:22 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:74ff537ac401802b30ae451fd049f6337b6ed0ee93f7f7e1b00cc09b9ae7f2af`  
		Last Modified: Wed, 24 Apr 2024 03:33:56 GMT  
		Size: 27.3 MB (27337575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ffd837dfe32dada37b2b83dc3294fdb8c5b1aa8e9d843a9d939191c5358a355`  
		Last Modified: Wed, 24 Apr 2024 13:52:29 GMT  
		Size: 2.8 MB (2780777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acc88837dcf46a86e66bf61f6da043eac5337cd9d1bb0b8771350b1a536ffdc1`  
		Last Modified: Wed, 24 Apr 2024 13:52:38 GMT  
		Size: 64.8 MB (64773978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9f93b564c87b034a6f8e8f6fb69a30afc9e039b5220024dae7bb2f6f40659ce`  
		Last Modified: Wed, 24 Apr 2024 13:53:36 GMT  
		Size: 159.9 MB (159930531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

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
$ docker pull mono@sha256:bd8a12d74ce824caff0f9f8958c7bcfffb892449f02a0e4df9cf6e8192b54176
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.2 MB (189166436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cb250b5d8f4152de3c52f3965099ebcfa87068ef5395e9795797f24516e93a0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 04:07:41 GMT
ADD file:985460a24e46cb6fd38e9ecdf21565547413f5f50d7c5c96d367b89aa94b91fa in / 
# Wed, 24 Apr 2024 04:07:41 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 07:02:59 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 24 Apr 2024 07:03:11 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 24 Apr 2024 07:03:30 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 24 Apr 2024 07:05:23 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a26123864d4d41f3f97e44b15f7ae2ecb9a15cbc37d6085d418a129976773e32`  
		Last Modified: Wed, 24 Apr 2024 04:12:31 GMT  
		Size: 22.9 MB (22945064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e354d269265092711be691142d28fc8002953b5bfb897dbd91cd4789aa0d7f2c`  
		Last Modified: Wed, 24 Apr 2024 07:07:19 GMT  
		Size: 2.4 MB (2370522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce30d34e592060862296941593408133f444860b8431bd82c0f709acf3400dac`  
		Last Modified: Wed, 24 Apr 2024 07:07:23 GMT  
		Size: 23.8 MB (23790719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0cf8b7baf15a56b76905e86633595d7d9f122406ce84adb136eb23cf3619250`  
		Last Modified: Wed, 24 Apr 2024 07:08:15 GMT  
		Size: 140.1 MB (140060131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0.182` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:e315d205d62cd6c04d52b11ecaf05e16c4f51b7eba142a8852e042c0283c1b01
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.6 MB (216552462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61d85bf404e8cc493498953016e368e84808ab7154fb3b866fb9b0257e80dcbb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 00:40:08 GMT
ADD file:469a091f7763af8b8b723185853358a0516954941c82654915e259a2356612ae in / 
# Tue, 14 May 2024 00:40:08 GMT
CMD ["bash"]
# Tue, 14 May 2024 03:01:03 GMT
ENV MONO_VERSION=6.12.0.182
# Tue, 14 May 2024 03:01:12 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 14 May 2024 03:02:44 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 14 May 2024 03:06:59 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:ad8110ff35cfa20fc3638a9f2a63a1113c1e4f724bc3b8c11d7ae280154356ca`  
		Last Modified: Tue, 14 May 2024 00:44:04 GMT  
		Size: 26.1 MB (26109106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a529a8ce298691a652a87333069ec6318e368ff0af7e2171b0ec58c5bf349dd8`  
		Last Modified: Tue, 14 May 2024 03:13:31 GMT  
		Size: 2.6 MB (2645561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79c2d783bd9b494f35fa932c80b7d810922f24489d8661f9f7e6626244d07bad`  
		Last Modified: Tue, 14 May 2024 03:13:34 GMT  
		Size: 29.5 MB (29545286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4ec1315f421edc1ff66ccc5ba4bcdd5d658530a2364f7438d255c14e6d80366`  
		Last Modified: Tue, 14 May 2024 03:14:19 GMT  
		Size: 158.3 MB (158252509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0.182` - linux; 386

```console
$ docker pull mono@sha256:067ca9a38acaaf9fdea29d7de110e8fd76261197be74a6b479b610eedd5a9b3d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.7 MB (259701817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:883e88334262384fea165fb01f2ec11dde2d61bc921c9f3bd6b3f1489f83d508`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 00:47:54 GMT
ADD file:75dbbf2d7d721b8debce2bfecdbf3ea14eb9b4dfe8a6354a21dd21725cafaff8 in / 
# Tue, 14 May 2024 00:47:54 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:16:51 GMT
ENV MONO_VERSION=6.12.0.182
# Tue, 14 May 2024 01:17:03 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 14 May 2024 01:17:39 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 14 May 2024 01:21:06 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:261459e26de7bf625f6d2ad5439fdd881d51b8e9bc959e0f3eb3b67ebacc250f`  
		Last Modified: Tue, 14 May 2024 00:53:24 GMT  
		Size: 28.0 MB (27994475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:036bbf0cc3e0f790c56486ebf068c9323a5e7716334c0114c7e3551fd1005100`  
		Last Modified: Tue, 14 May 2024 01:23:54 GMT  
		Size: 2.8 MB (2792366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb6f765ea19029790391afd07a05f782804dc82a94340049c2ad63c4eade3caf`  
		Last Modified: Tue, 14 May 2024 01:24:08 GMT  
		Size: 68.8 MB (68800484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47f132e8616f7a3f460f3dd4f3369385c8c9b4d238922ab196b9e2387f25e5c3`  
		Last Modified: Tue, 14 May 2024 01:25:24 GMT  
		Size: 160.1 MB (160114492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

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
$ docker pull mono@sha256:6d47290645de36eb0f9185f3794730b07d931e71dd1f01749ae3a117adafa41b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:6.12.0.182-slim` - linux; amd64

```console
$ docker pull mono@sha256:0749e711811842967d725da21612af6129be80c84e3ed529fb700cfbf81e455d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.9 MB (94892330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:593772cbcad062ca2e93e73111024a35645d7510a450b015dbe1012eb08b05fc`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:50 GMT
ADD file:9b846fb660cf816c4e731c6f547b8e389343bc05aa2ec510b1dfc2bddd4d1c8a in / 
# Wed, 24 Apr 2024 03:28:51 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 13:44:56 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 24 Apr 2024 13:45:07 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 24 Apr 2024 13:45:29 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:74ff537ac401802b30ae451fd049f6337b6ed0ee93f7f7e1b00cc09b9ae7f2af`  
		Last Modified: Wed, 24 Apr 2024 03:33:56 GMT  
		Size: 27.3 MB (27337575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ffd837dfe32dada37b2b83dc3294fdb8c5b1aa8e9d843a9d939191c5358a355`  
		Last Modified: Wed, 24 Apr 2024 13:52:29 GMT  
		Size: 2.8 MB (2780777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acc88837dcf46a86e66bf61f6da043eac5337cd9d1bb0b8771350b1a536ffdc1`  
		Last Modified: Wed, 24 Apr 2024 13:52:38 GMT  
		Size: 64.8 MB (64773978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

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
$ docker pull mono@sha256:fa609c04866c144a99440dc2501eb77993b62e2a149d5fe1781a0539a5af518b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49106305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:634defc256033a7bfb1b71133d25e64724d595feb9f1d983b457847c7773360e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 04:07:41 GMT
ADD file:985460a24e46cb6fd38e9ecdf21565547413f5f50d7c5c96d367b89aa94b91fa in / 
# Wed, 24 Apr 2024 04:07:41 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 07:02:59 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 24 Apr 2024 07:03:11 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 24 Apr 2024 07:03:30 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a26123864d4d41f3f97e44b15f7ae2ecb9a15cbc37d6085d418a129976773e32`  
		Last Modified: Wed, 24 Apr 2024 04:12:31 GMT  
		Size: 22.9 MB (22945064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e354d269265092711be691142d28fc8002953b5bfb897dbd91cd4789aa0d7f2c`  
		Last Modified: Wed, 24 Apr 2024 07:07:19 GMT  
		Size: 2.4 MB (2370522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce30d34e592060862296941593408133f444860b8431bd82c0f709acf3400dac`  
		Last Modified: Wed, 24 Apr 2024 07:07:23 GMT  
		Size: 23.8 MB (23790719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0.182-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:e2727d8c2692fbaf5a3abaaf56a98d49a6e5b24ff7c727cb564f88ad2cb240bc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.3 MB (58299953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9dcf5344b0840b1056715bc2ba296aed99407dab01e0c67ab889f9980e8e77b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 00:40:08 GMT
ADD file:469a091f7763af8b8b723185853358a0516954941c82654915e259a2356612ae in / 
# Tue, 14 May 2024 00:40:08 GMT
CMD ["bash"]
# Tue, 14 May 2024 03:01:03 GMT
ENV MONO_VERSION=6.12.0.182
# Tue, 14 May 2024 03:01:12 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 14 May 2024 03:02:44 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:ad8110ff35cfa20fc3638a9f2a63a1113c1e4f724bc3b8c11d7ae280154356ca`  
		Last Modified: Tue, 14 May 2024 00:44:04 GMT  
		Size: 26.1 MB (26109106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a529a8ce298691a652a87333069ec6318e368ff0af7e2171b0ec58c5bf349dd8`  
		Last Modified: Tue, 14 May 2024 03:13:31 GMT  
		Size: 2.6 MB (2645561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79c2d783bd9b494f35fa932c80b7d810922f24489d8661f9f7e6626244d07bad`  
		Last Modified: Tue, 14 May 2024 03:13:34 GMT  
		Size: 29.5 MB (29545286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0.182-slim` - linux; 386

```console
$ docker pull mono@sha256:7290a085e73bf2acdf312667141ed3060c3ecbbcdabd4e2f345865b5e8090612
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.6 MB (99587325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0122e8a6790708e8b29c1a50eb7a19482e2483089f00f9c46226457b9baa8325`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 00:47:54 GMT
ADD file:75dbbf2d7d721b8debce2bfecdbf3ea14eb9b4dfe8a6354a21dd21725cafaff8 in / 
# Tue, 14 May 2024 00:47:54 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:16:51 GMT
ENV MONO_VERSION=6.12.0.182
# Tue, 14 May 2024 01:17:03 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 14 May 2024 01:17:39 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:261459e26de7bf625f6d2ad5439fdd881d51b8e9bc959e0f3eb3b67ebacc250f`  
		Last Modified: Tue, 14 May 2024 00:53:24 GMT  
		Size: 28.0 MB (27994475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:036bbf0cc3e0f790c56486ebf068c9323a5e7716334c0114c7e3551fd1005100`  
		Last Modified: Tue, 14 May 2024 01:23:54 GMT  
		Size: 2.8 MB (2792366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb6f765ea19029790391afd07a05f782804dc82a94340049c2ad63c4eade3caf`  
		Last Modified: Tue, 14 May 2024 01:24:08 GMT  
		Size: 68.8 MB (68800484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

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
$ docker pull mono@sha256:86767b090cf14a50f9f006191e72be7fa71c0a0eda8afcc56c0d6f1031110fa7
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
$ docker pull mono@sha256:fd331c4c7a1b2b895a97f4e7829e8f40045c2dcab4156a2c1f13f1a17d58ad21
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.8 MB (254822861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1c1a10a5340e5cc64fa235e6d0d4baf42815e4de3f3389e0d10c302b2604b9b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:50 GMT
ADD file:9b846fb660cf816c4e731c6f547b8e389343bc05aa2ec510b1dfc2bddd4d1c8a in / 
# Wed, 24 Apr 2024 03:28:51 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 13:44:56 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 24 Apr 2024 13:45:07 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 24 Apr 2024 13:45:29 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 24 Apr 2024 13:47:22 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:74ff537ac401802b30ae451fd049f6337b6ed0ee93f7f7e1b00cc09b9ae7f2af`  
		Last Modified: Wed, 24 Apr 2024 03:33:56 GMT  
		Size: 27.3 MB (27337575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ffd837dfe32dada37b2b83dc3294fdb8c5b1aa8e9d843a9d939191c5358a355`  
		Last Modified: Wed, 24 Apr 2024 13:52:29 GMT  
		Size: 2.8 MB (2780777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acc88837dcf46a86e66bf61f6da043eac5337cd9d1bb0b8771350b1a536ffdc1`  
		Last Modified: Wed, 24 Apr 2024 13:52:38 GMT  
		Size: 64.8 MB (64773978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9f93b564c87b034a6f8e8f6fb69a30afc9e039b5220024dae7bb2f6f40659ce`  
		Last Modified: Wed, 24 Apr 2024 13:53:36 GMT  
		Size: 159.9 MB (159930531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

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
$ docker pull mono@sha256:bd8a12d74ce824caff0f9f8958c7bcfffb892449f02a0e4df9cf6e8192b54176
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.2 MB (189166436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cb250b5d8f4152de3c52f3965099ebcfa87068ef5395e9795797f24516e93a0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 04:07:41 GMT
ADD file:985460a24e46cb6fd38e9ecdf21565547413f5f50d7c5c96d367b89aa94b91fa in / 
# Wed, 24 Apr 2024 04:07:41 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 07:02:59 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 24 Apr 2024 07:03:11 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 24 Apr 2024 07:03:30 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 24 Apr 2024 07:05:23 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a26123864d4d41f3f97e44b15f7ae2ecb9a15cbc37d6085d418a129976773e32`  
		Last Modified: Wed, 24 Apr 2024 04:12:31 GMT  
		Size: 22.9 MB (22945064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e354d269265092711be691142d28fc8002953b5bfb897dbd91cd4789aa0d7f2c`  
		Last Modified: Wed, 24 Apr 2024 07:07:19 GMT  
		Size: 2.4 MB (2370522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce30d34e592060862296941593408133f444860b8431bd82c0f709acf3400dac`  
		Last Modified: Wed, 24 Apr 2024 07:07:23 GMT  
		Size: 23.8 MB (23790719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0cf8b7baf15a56b76905e86633595d7d9f122406ce84adb136eb23cf3619250`  
		Last Modified: Wed, 24 Apr 2024 07:08:15 GMT  
		Size: 140.1 MB (140060131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:latest` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:e315d205d62cd6c04d52b11ecaf05e16c4f51b7eba142a8852e042c0283c1b01
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.6 MB (216552462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61d85bf404e8cc493498953016e368e84808ab7154fb3b866fb9b0257e80dcbb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 00:40:08 GMT
ADD file:469a091f7763af8b8b723185853358a0516954941c82654915e259a2356612ae in / 
# Tue, 14 May 2024 00:40:08 GMT
CMD ["bash"]
# Tue, 14 May 2024 03:01:03 GMT
ENV MONO_VERSION=6.12.0.182
# Tue, 14 May 2024 03:01:12 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 14 May 2024 03:02:44 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 14 May 2024 03:06:59 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:ad8110ff35cfa20fc3638a9f2a63a1113c1e4f724bc3b8c11d7ae280154356ca`  
		Last Modified: Tue, 14 May 2024 00:44:04 GMT  
		Size: 26.1 MB (26109106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a529a8ce298691a652a87333069ec6318e368ff0af7e2171b0ec58c5bf349dd8`  
		Last Modified: Tue, 14 May 2024 03:13:31 GMT  
		Size: 2.6 MB (2645561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79c2d783bd9b494f35fa932c80b7d810922f24489d8661f9f7e6626244d07bad`  
		Last Modified: Tue, 14 May 2024 03:13:34 GMT  
		Size: 29.5 MB (29545286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4ec1315f421edc1ff66ccc5ba4bcdd5d658530a2364f7438d255c14e6d80366`  
		Last Modified: Tue, 14 May 2024 03:14:19 GMT  
		Size: 158.3 MB (158252509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:latest` - linux; 386

```console
$ docker pull mono@sha256:067ca9a38acaaf9fdea29d7de110e8fd76261197be74a6b479b610eedd5a9b3d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.7 MB (259701817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:883e88334262384fea165fb01f2ec11dde2d61bc921c9f3bd6b3f1489f83d508`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 00:47:54 GMT
ADD file:75dbbf2d7d721b8debce2bfecdbf3ea14eb9b4dfe8a6354a21dd21725cafaff8 in / 
# Tue, 14 May 2024 00:47:54 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:16:51 GMT
ENV MONO_VERSION=6.12.0.182
# Tue, 14 May 2024 01:17:03 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 14 May 2024 01:17:39 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 14 May 2024 01:21:06 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:261459e26de7bf625f6d2ad5439fdd881d51b8e9bc959e0f3eb3b67ebacc250f`  
		Last Modified: Tue, 14 May 2024 00:53:24 GMT  
		Size: 28.0 MB (27994475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:036bbf0cc3e0f790c56486ebf068c9323a5e7716334c0114c7e3551fd1005100`  
		Last Modified: Tue, 14 May 2024 01:23:54 GMT  
		Size: 2.8 MB (2792366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb6f765ea19029790391afd07a05f782804dc82a94340049c2ad63c4eade3caf`  
		Last Modified: Tue, 14 May 2024 01:24:08 GMT  
		Size: 68.8 MB (68800484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47f132e8616f7a3f460f3dd4f3369385c8c9b4d238922ab196b9e2387f25e5c3`  
		Last Modified: Tue, 14 May 2024 01:25:24 GMT  
		Size: 160.1 MB (160114492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

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
$ docker pull mono@sha256:6d47290645de36eb0f9185f3794730b07d931e71dd1f01749ae3a117adafa41b
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
$ docker pull mono@sha256:0749e711811842967d725da21612af6129be80c84e3ed529fb700cfbf81e455d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.9 MB (94892330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:593772cbcad062ca2e93e73111024a35645d7510a450b015dbe1012eb08b05fc`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:50 GMT
ADD file:9b846fb660cf816c4e731c6f547b8e389343bc05aa2ec510b1dfc2bddd4d1c8a in / 
# Wed, 24 Apr 2024 03:28:51 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 13:44:56 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 24 Apr 2024 13:45:07 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 24 Apr 2024 13:45:29 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:74ff537ac401802b30ae451fd049f6337b6ed0ee93f7f7e1b00cc09b9ae7f2af`  
		Last Modified: Wed, 24 Apr 2024 03:33:56 GMT  
		Size: 27.3 MB (27337575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ffd837dfe32dada37b2b83dc3294fdb8c5b1aa8e9d843a9d939191c5358a355`  
		Last Modified: Wed, 24 Apr 2024 13:52:29 GMT  
		Size: 2.8 MB (2780777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acc88837dcf46a86e66bf61f6da043eac5337cd9d1bb0b8771350b1a536ffdc1`  
		Last Modified: Wed, 24 Apr 2024 13:52:38 GMT  
		Size: 64.8 MB (64773978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

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
$ docker pull mono@sha256:fa609c04866c144a99440dc2501eb77993b62e2a149d5fe1781a0539a5af518b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49106305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:634defc256033a7bfb1b71133d25e64724d595feb9f1d983b457847c7773360e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 04:07:41 GMT
ADD file:985460a24e46cb6fd38e9ecdf21565547413f5f50d7c5c96d367b89aa94b91fa in / 
# Wed, 24 Apr 2024 04:07:41 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 07:02:59 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 24 Apr 2024 07:03:11 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 24 Apr 2024 07:03:30 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a26123864d4d41f3f97e44b15f7ae2ecb9a15cbc37d6085d418a129976773e32`  
		Last Modified: Wed, 24 Apr 2024 04:12:31 GMT  
		Size: 22.9 MB (22945064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e354d269265092711be691142d28fc8002953b5bfb897dbd91cd4789aa0d7f2c`  
		Last Modified: Wed, 24 Apr 2024 07:07:19 GMT  
		Size: 2.4 MB (2370522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce30d34e592060862296941593408133f444860b8431bd82c0f709acf3400dac`  
		Last Modified: Wed, 24 Apr 2024 07:07:23 GMT  
		Size: 23.8 MB (23790719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:e2727d8c2692fbaf5a3abaaf56a98d49a6e5b24ff7c727cb564f88ad2cb240bc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.3 MB (58299953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9dcf5344b0840b1056715bc2ba296aed99407dab01e0c67ab889f9980e8e77b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 00:40:08 GMT
ADD file:469a091f7763af8b8b723185853358a0516954941c82654915e259a2356612ae in / 
# Tue, 14 May 2024 00:40:08 GMT
CMD ["bash"]
# Tue, 14 May 2024 03:01:03 GMT
ENV MONO_VERSION=6.12.0.182
# Tue, 14 May 2024 03:01:12 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 14 May 2024 03:02:44 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:ad8110ff35cfa20fc3638a9f2a63a1113c1e4f724bc3b8c11d7ae280154356ca`  
		Last Modified: Tue, 14 May 2024 00:44:04 GMT  
		Size: 26.1 MB (26109106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a529a8ce298691a652a87333069ec6318e368ff0af7e2171b0ec58c5bf349dd8`  
		Last Modified: Tue, 14 May 2024 03:13:31 GMT  
		Size: 2.6 MB (2645561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79c2d783bd9b494f35fa932c80b7d810922f24489d8661f9f7e6626244d07bad`  
		Last Modified: Tue, 14 May 2024 03:13:34 GMT  
		Size: 29.5 MB (29545286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:slim` - linux; 386

```console
$ docker pull mono@sha256:7290a085e73bf2acdf312667141ed3060c3ecbbcdabd4e2f345865b5e8090612
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.6 MB (99587325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0122e8a6790708e8b29c1a50eb7a19482e2483089f00f9c46226457b9baa8325`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 00:47:54 GMT
ADD file:75dbbf2d7d721b8debce2bfecdbf3ea14eb9b4dfe8a6354a21dd21725cafaff8 in / 
# Tue, 14 May 2024 00:47:54 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:16:51 GMT
ENV MONO_VERSION=6.12.0.182
# Tue, 14 May 2024 01:17:03 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 14 May 2024 01:17:39 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:261459e26de7bf625f6d2ad5439fdd881d51b8e9bc959e0f3eb3b67ebacc250f`  
		Last Modified: Tue, 14 May 2024 00:53:24 GMT  
		Size: 28.0 MB (27994475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:036bbf0cc3e0f790c56486ebf068c9323a5e7716334c0114c7e3551fd1005100`  
		Last Modified: Tue, 14 May 2024 01:23:54 GMT  
		Size: 2.8 MB (2792366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb6f765ea19029790391afd07a05f782804dc82a94340049c2ad63c4eade3caf`  
		Last Modified: Tue, 14 May 2024 01:24:08 GMT  
		Size: 68.8 MB (68800484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

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
