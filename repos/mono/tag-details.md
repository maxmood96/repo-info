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
$ docker pull mono@sha256:bcc2d36c88898cdd62a9e18f97ad863c44b30fb74a23585549808f7db216a717
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
$ docker pull mono@sha256:c868b8345d1b67f672c229bfb330f5e1ba58cfcc33a6d46a9375b39bc25d5bda
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.4 MB (254416410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4527a2fc6d1eab132a7db6cd829d5d905553a692c5680c5e233251932e8d2e3`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 01:20:43 GMT
ADD file:0513eda9512e010cb9459591b62e0c9d9319750923df091b64250ad6e98c2878 in / 
# Sat, 28 May 2022 01:20:43 GMT
CMD ["bash"]
# Wed, 22 Jun 2022 21:33:20 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 22 Jun 2022 21:33:29 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jun 2022 21:33:47 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 22 Jun 2022 21:34:59 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:c1ad9731b2c7bf7fddea67f2f3f553515179a375c489e591e2372700fcaca766`  
		Last Modified: Sat, 28 May 2022 01:26:05 GMT  
		Size: 27.1 MB (27140144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36bdd50eb1bac9261e7d11ef7736774181be91ac4c30c02e1c1c4cc1c567a999`  
		Last Modified: Wed, 22 Jun 2022 21:35:25 GMT  
		Size: 2.8 MB (2777561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aba950124d67df356ccc1d947efdfd8cb5c8a7769434bc4057d371b5897b4d2e`  
		Last Modified: Wed, 22 Jun 2022 21:35:35 GMT  
		Size: 64.8 MB (64772708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e06195ea08da0f4b76c03b1a888e1149b4b7456b3137a22534ed08d300e9e9ff`  
		Last Modified: Wed, 22 Jun 2022 21:36:17 GMT  
		Size: 159.7 MB (159725997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6` - linux; arm variant v5

```console
$ docker pull mono@sha256:eecb4ce0a2143b972b80438d19719eedce94ea3734c1209e616f2c7b1752e397
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.9 MB (192881569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc56159c8ddff3dd73991b2b958f358c0e6b8a5dc881ad7a926c459b4be00031`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 02:04:06 GMT
ADD file:26e9ed6c41ec12bf5fd602b7f86b924d34537bbc82442f630763f9f6c48bf3b3 in / 
# Sat, 28 May 2022 02:04:07 GMT
CMD ["bash"]
# Wed, 22 Jun 2022 19:49:00 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 22 Jun 2022 19:49:28 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jun 2022 19:50:19 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 22 Jun 2022 19:54:03 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:19389fd1100abdedaa775b43242838cdd2d5c8c3388643a7e52da2b7b4399c15`  
		Last Modified: Sat, 28 May 2022 02:20:06 GMT  
		Size: 24.9 MB (24890069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa92f2f021e75803ce535a7facb85567bc17614f5919ffd2ded82252e6d03d5e`  
		Last Modified: Wed, 22 Jun 2022 19:55:44 GMT  
		Size: 2.5 MB (2467777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:946e5a3fcfdd33b760be56e03b5bd597eb8df3d50ee8880f36418e4b23a50fd8`  
		Last Modified: Wed, 22 Jun 2022 19:56:01 GMT  
		Size: 24.5 MB (24503493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e7dcb1cf8147d4ccbe01cb4986ecc814d15c96443e421575b6ec406ce783e98`  
		Last Modified: Wed, 22 Jun 2022 19:58:06 GMT  
		Size: 141.0 MB (141020230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6` - linux; arm variant v7

```console
$ docker pull mono@sha256:8e6e34d1a1ae5a2de0c439461a0cb502b0cd22220cd6774b90cb62fa5e240a92
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.8 MB (188782584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8afa747cef2c601df113d6bbdf74340305ece2fa03b83f9dd709d64178ced488`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 01:00:54 GMT
ADD file:c89d47099a38749a424760d9c7d3a6e982089455ba9d04140db15ba9eb4cdda1 in / 
# Sat, 28 May 2022 01:00:55 GMT
CMD ["bash"]
# Wed, 22 Jun 2022 21:53:04 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 22 Jun 2022 21:53:30 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jun 2022 21:54:14 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 22 Jun 2022 21:57:44 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:e41117292dc8c199b63ae1ec4485358841dbcba68dcbd13f379b66182efe832e`  
		Last Modified: Sat, 28 May 2022 01:16:58 GMT  
		Size: 22.7 MB (22748097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cea7b08703ed144c6d58b457cac40359088319d3ed62617dcbd6e3f36943b28a`  
		Last Modified: Wed, 22 Jun 2022 21:59:22 GMT  
		Size: 2.4 MB (2367003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c63834d12328a6bcb0b82fbfb83fef45b3596496346470249ba9c388730688a2`  
		Last Modified: Wed, 22 Jun 2022 21:59:38 GMT  
		Size: 23.8 MB (23789737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ec56912b25995fca9411a168ff99dcefede44b3e81975719b204e56f0a02971`  
		Last Modified: Wed, 22 Jun 2022 22:01:46 GMT  
		Size: 139.9 MB (139877747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:4654e59232e7dc6ba687050cc60cb311e0ef287235be7e88b313d69fa8565a7b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.9 MB (215904246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cae1924b9544a9ab52d1b2e09daec6d8f9560b3cbccb8f50929cc577b91940ab`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 00:41:05 GMT
ADD file:d0e42d603f275c040783ec7b6c051200815492fc35b73110234dfcd584e6cdec in / 
# Sat, 28 May 2022 00:41:05 GMT
CMD ["bash"]
# Wed, 22 Jun 2022 20:48:48 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 22 Jun 2022 20:48:57 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jun 2022 20:49:12 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 22 Jun 2022 20:50:20 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:4931fb8ba4223cb35034141162105ee5482122692b2931eb69eec912ce64606d`  
		Last Modified: Sat, 28 May 2022 00:48:26 GMT  
		Size: 25.9 MB (25914033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f06cddbf5d49ff334333bc51c02936695c616c52497d3284e91848de8085104a`  
		Last Modified: Wed, 22 Jun 2022 20:51:01 GMT  
		Size: 2.6 MB (2641202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:751c39f1c5edbe681c6c8ee877cb5e858b51e875ddf051ef6c2d8ef93b840da5`  
		Last Modified: Wed, 22 Jun 2022 20:51:06 GMT  
		Size: 29.3 MB (29333416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fcd120a21e937a94366c7d43691992fa5fcd977e2f57b855fd8228d72bdcf2b`  
		Last Modified: Wed, 22 Jun 2022 20:51:52 GMT  
		Size: 158.0 MB (158015595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6` - linux; 386

```console
$ docker pull mono@sha256:077ff268e88653929ca63f7c94b2e831ed47deda1898a7dab145be46bc43dca5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.1 MB (259079011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e4374dff0b027269b8b0431e17ebeb06e2a686d388a8c1592acc87d1a729552`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 00:40:01 GMT
ADD file:9aea7a35c215cdd778adec1dd5213973ef9b4830110e4550f2ead85679551ee5 in / 
# Sat, 28 May 2022 00:40:01 GMT
CMD ["bash"]
# Wed, 22 Jun 2022 21:09:07 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 22 Jun 2022 21:09:17 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jun 2022 21:09:41 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 22 Jun 2022 21:11:03 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:40837b3d848885c0b0c031d6d950b38e6a26962a5ee49704cb3ca2d2db535617`  
		Last Modified: Sat, 28 May 2022 00:47:36 GMT  
		Size: 27.8 MB (27799572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f5200b7ae28ef6430e06f086a32f10b738467f7b8d657b48c49d175705a2439`  
		Last Modified: Wed, 22 Jun 2022 21:11:47 GMT  
		Size: 2.8 MB (2789326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39fde061d95ef131491c0e1d327f4052f99ac1349bc834556e204012adc8392b`  
		Last Modified: Wed, 22 Jun 2022 21:11:56 GMT  
		Size: 68.6 MB (68586144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7134f7256858262305eb34494cf4e9b1fca7a8e3139732ec59ae0e26a5b5808`  
		Last Modified: Wed, 22 Jun 2022 21:12:45 GMT  
		Size: 159.9 MB (159903969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6` - linux; ppc64le

```console
$ docker pull mono@sha256:7eac0dfce15caa1b45ca234122e7853ce90c084da4661daafbce43c170cbfd73
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.2 MB (204236244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab1afeae8582e0f00846a4ec3004a268ac2997c3995b17a6f31c32addd8961e5`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 01:23:57 GMT
ADD file:a8c6c897bc64da424049ad04a354d123b0622abda1a56b2725f72de5e4569df8 in / 
# Sat, 28 May 2022 01:24:04 GMT
CMD ["bash"]
# Wed, 22 Jun 2022 22:32:51 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 22 Jun 2022 22:36:09 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jun 2022 22:39:29 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 22 Jun 2022 22:59:57 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:087d40850259bdcd3bee3d5d30d5a2070216727f72c1c9731b514ac3dbf7573e`  
		Last Modified: Sat, 28 May 2022 01:33:30 GMT  
		Size: 30.6 MB (30560238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbd0cf1c03bf6b16f117de84792baa6f69e374958138eb1f18c6cfb9dd43bbad`  
		Last Modified: Wed, 22 Jun 2022 23:09:45 GMT  
		Size: 2.9 MB (2893026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e43a06d332d2410820bebe341037d6c6dee278dbc6f235c702a6713f9e3dcab`  
		Last Modified: Wed, 22 Jun 2022 23:09:50 GMT  
		Size: 26.9 MB (26897354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd50f7a2e62c331e54ff9a3a987c99b7719f64428153fd4aff50ef0d6c661e3`  
		Last Modified: Wed, 22 Jun 2022 23:14:42 GMT  
		Size: 143.9 MB (143885626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6-slim`

```console
$ docker pull mono@sha256:2a988c2c837506a6d94e5eb2c939cce53c86996a9474cb8fdfe9f580ad32cac1
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
$ docker pull mono@sha256:fa12e7083a98b6812cc29d29f0a085ea2f029c0e4670819a01fbb8a663faeb64
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.7 MB (94690413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61736b8ef52963f0ca986605f518457372d0c66f0a74040721c0e014a2119f80`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 01:20:43 GMT
ADD file:0513eda9512e010cb9459591b62e0c9d9319750923df091b64250ad6e98c2878 in / 
# Sat, 28 May 2022 01:20:43 GMT
CMD ["bash"]
# Wed, 22 Jun 2022 21:33:20 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 22 Jun 2022 21:33:29 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jun 2022 21:33:47 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:c1ad9731b2c7bf7fddea67f2f3f553515179a375c489e591e2372700fcaca766`  
		Last Modified: Sat, 28 May 2022 01:26:05 GMT  
		Size: 27.1 MB (27140144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36bdd50eb1bac9261e7d11ef7736774181be91ac4c30c02e1c1c4cc1c567a999`  
		Last Modified: Wed, 22 Jun 2022 21:35:25 GMT  
		Size: 2.8 MB (2777561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aba950124d67df356ccc1d947efdfd8cb5c8a7769434bc4057d371b5897b4d2e`  
		Last Modified: Wed, 22 Jun 2022 21:35:35 GMT  
		Size: 64.8 MB (64772708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:63988b42501e95210c718ff7135a1864484fbc220ec2ec6bf545a2227018fcac
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.9 MB (51861339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c8a27d1ba9bc597baeac26ffe42cbbdffae549aeaa642f7bd17e856d9a3f7df`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 02:04:06 GMT
ADD file:26e9ed6c41ec12bf5fd602b7f86b924d34537bbc82442f630763f9f6c48bf3b3 in / 
# Sat, 28 May 2022 02:04:07 GMT
CMD ["bash"]
# Wed, 22 Jun 2022 19:49:00 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 22 Jun 2022 19:49:28 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jun 2022 19:50:19 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:19389fd1100abdedaa775b43242838cdd2d5c8c3388643a7e52da2b7b4399c15`  
		Last Modified: Sat, 28 May 2022 02:20:06 GMT  
		Size: 24.9 MB (24890069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa92f2f021e75803ce535a7facb85567bc17614f5919ffd2ded82252e6d03d5e`  
		Last Modified: Wed, 22 Jun 2022 19:55:44 GMT  
		Size: 2.5 MB (2467777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:946e5a3fcfdd33b760be56e03b5bd597eb8df3d50ee8880f36418e4b23a50fd8`  
		Last Modified: Wed, 22 Jun 2022 19:56:01 GMT  
		Size: 24.5 MB (24503493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:cedb57185a1bf7814ec666fc9803c0151fa8c5b4d4c8825092defa4a67ce92a5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48904837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80c02c8e8e7adb45c0a2629edac2478b91fb970b7cd16d064ea6a269db94729e`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 01:00:54 GMT
ADD file:c89d47099a38749a424760d9c7d3a6e982089455ba9d04140db15ba9eb4cdda1 in / 
# Sat, 28 May 2022 01:00:55 GMT
CMD ["bash"]
# Wed, 22 Jun 2022 21:53:04 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 22 Jun 2022 21:53:30 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jun 2022 21:54:14 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:e41117292dc8c199b63ae1ec4485358841dbcba68dcbd13f379b66182efe832e`  
		Last Modified: Sat, 28 May 2022 01:16:58 GMT  
		Size: 22.7 MB (22748097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cea7b08703ed144c6d58b457cac40359088319d3ed62617dcbd6e3f36943b28a`  
		Last Modified: Wed, 22 Jun 2022 21:59:22 GMT  
		Size: 2.4 MB (2367003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c63834d12328a6bcb0b82fbfb83fef45b3596496346470249ba9c388730688a2`  
		Last Modified: Wed, 22 Jun 2022 21:59:38 GMT  
		Size: 23.8 MB (23789737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:349bfae18e0c38993d262c97c4e5dfcc08d672b0a775b8cebaacb2805bbb9469
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.9 MB (57888651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14037cb8b94bf65da4202f7a2f4b5bc9edd22cfe2a40b5712e6ff5260abbd44a`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 00:41:05 GMT
ADD file:d0e42d603f275c040783ec7b6c051200815492fc35b73110234dfcd584e6cdec in / 
# Sat, 28 May 2022 00:41:05 GMT
CMD ["bash"]
# Wed, 22 Jun 2022 20:48:48 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 22 Jun 2022 20:48:57 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jun 2022 20:49:12 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:4931fb8ba4223cb35034141162105ee5482122692b2931eb69eec912ce64606d`  
		Last Modified: Sat, 28 May 2022 00:48:26 GMT  
		Size: 25.9 MB (25914033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f06cddbf5d49ff334333bc51c02936695c616c52497d3284e91848de8085104a`  
		Last Modified: Wed, 22 Jun 2022 20:51:01 GMT  
		Size: 2.6 MB (2641202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:751c39f1c5edbe681c6c8ee877cb5e858b51e875ddf051ef6c2d8ef93b840da5`  
		Last Modified: Wed, 22 Jun 2022 20:51:06 GMT  
		Size: 29.3 MB (29333416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6-slim` - linux; 386

```console
$ docker pull mono@sha256:3bb47bffd3d5b15f72dd10214baaaf4c2d7552cadec24c67c4ccccd6966ce009
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.2 MB (99175042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebd693bbe60229e9032cc548cbd25cbbd5c053d51845c4e7896959ccf6d068a1`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 00:40:01 GMT
ADD file:9aea7a35c215cdd778adec1dd5213973ef9b4830110e4550f2ead85679551ee5 in / 
# Sat, 28 May 2022 00:40:01 GMT
CMD ["bash"]
# Wed, 22 Jun 2022 21:09:07 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 22 Jun 2022 21:09:17 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jun 2022 21:09:41 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:40837b3d848885c0b0c031d6d950b38e6a26962a5ee49704cb3ca2d2db535617`  
		Last Modified: Sat, 28 May 2022 00:47:36 GMT  
		Size: 27.8 MB (27799572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f5200b7ae28ef6430e06f086a32f10b738467f7b8d657b48c49d175705a2439`  
		Last Modified: Wed, 22 Jun 2022 21:11:47 GMT  
		Size: 2.8 MB (2789326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39fde061d95ef131491c0e1d327f4052f99ac1349bc834556e204012adc8392b`  
		Last Modified: Wed, 22 Jun 2022 21:11:56 GMT  
		Size: 68.6 MB (68586144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:1ac19e6ece7d6fe0e4208ee88f5941537dd1a5d3394da83468d2bc55527d7378
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.4 MB (60350618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:065d97346ce613488eb9e0d9d912aead0311ee56f9c1eed798b5de4ec6472d1a`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 01:23:57 GMT
ADD file:a8c6c897bc64da424049ad04a354d123b0622abda1a56b2725f72de5e4569df8 in / 
# Sat, 28 May 2022 01:24:04 GMT
CMD ["bash"]
# Wed, 22 Jun 2022 22:32:51 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 22 Jun 2022 22:36:09 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jun 2022 22:39:29 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:087d40850259bdcd3bee3d5d30d5a2070216727f72c1c9731b514ac3dbf7573e`  
		Last Modified: Sat, 28 May 2022 01:33:30 GMT  
		Size: 30.6 MB (30560238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbd0cf1c03bf6b16f117de84792baa6f69e374958138eb1f18c6cfb9dd43bbad`  
		Last Modified: Wed, 22 Jun 2022 23:09:45 GMT  
		Size: 2.9 MB (2893026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e43a06d332d2410820bebe341037d6c6dee278dbc6f235c702a6713f9e3dcab`  
		Last Modified: Wed, 22 Jun 2022 23:09:50 GMT  
		Size: 26.9 MB (26897354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.10`

```console
$ docker pull mono@sha256:7fba975ee6fcad096a0c6822cb350bac90d8c5bfe8612ba9f9a78dd79722bd83
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
$ docker pull mono@sha256:66a99f9ed2a2c483aa5072a20049e2dd28742ad0a2b83e9727ec7ebf8a78de4c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.0 MB (225005893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91215f97e46cd1e11118e1d37a1b77a4ff94a998afcdadb40b8127cae3fa65bc`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 01:20:43 GMT
ADD file:0513eda9512e010cb9459591b62e0c9d9319750923df091b64250ad6e98c2878 in / 
# Sat, 28 May 2022 01:20:43 GMT
CMD ["bash"]
# Sat, 28 May 2022 11:35:41 GMT
ENV MONO_VERSION=6.10.0.104
# Sat, 28 May 2022 11:35:50 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 May 2022 11:36:17 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 28 May 2022 11:46:47 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:c1ad9731b2c7bf7fddea67f2f3f553515179a375c489e591e2372700fcaca766`  
		Last Modified: Sat, 28 May 2022 01:26:05 GMT  
		Size: 27.1 MB (27140144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:634a317d34eeec1b0e96f4fb4273064fea3fd708e5cfa450d4d09046d4cfc3d1`  
		Last Modified: Sat, 28 May 2022 11:47:38 GMT  
		Size: 2.8 MB (2777558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22b4be749876c6f886fe310e24cf0937bad3c1864521575a4af4e0e1412501ac`  
		Last Modified: Sat, 28 May 2022 11:47:48 GMT  
		Size: 64.8 MB (64778980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce15f229c8f857d448d87bfa56087e614ab3b63aca6261f823d63ef3b8ffe614`  
		Last Modified: Sat, 28 May 2022 11:48:55 GMT  
		Size: 130.3 MB (130309211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10` - linux; arm variant v5

```console
$ docker pull mono@sha256:0d0eaa12e7fcbbf941468045aa3512b501d40de39a152d93210d1c1dc54fe108
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.9 MB (180859738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:945cbaa5a9e079652bb0afec334b0d9abf93fec7db23291505ef02f47db7ed03`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 02:04:06 GMT
ADD file:26e9ed6c41ec12bf5fd602b7f86b924d34537bbc82442f630763f9f6c48bf3b3 in / 
# Sat, 28 May 2022 02:04:07 GMT
CMD ["bash"]
# Sat, 28 May 2022 04:03:10 GMT
ENV MONO_VERSION=6.10.0.104
# Sat, 28 May 2022 04:03:38 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 May 2022 04:04:26 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 28 May 2022 04:11:30 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:19389fd1100abdedaa775b43242838cdd2d5c8c3388643a7e52da2b7b4399c15`  
		Last Modified: Sat, 28 May 2022 02:20:06 GMT  
		Size: 24.9 MB (24890069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26e8b570b3ab504ed3e8f73b1c63efee3410fb86aaab255274f2a7e1328ca292`  
		Last Modified: Sat, 28 May 2022 04:13:34 GMT  
		Size: 2.5 MB (2467793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daa9619bad699d3b6b5711965b8847aa3c3536cb1c715a01c67006bbf0423924`  
		Last Modified: Sat, 28 May 2022 04:13:53 GMT  
		Size: 24.5 MB (24521830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:888817f0aafc0a9a017db76412ae019f21d2b979bcbaf99ab971eeaa02c08aa4`  
		Last Modified: Sat, 28 May 2022 04:17:32 GMT  
		Size: 129.0 MB (128980046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10` - linux; arm variant v7

```console
$ docker pull mono@sha256:5aa1ee4b7be1cbc3de8d81a09f8dbf8874577cd2a43d5ad0b7828471bdd8b3b5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.8 MB (176760688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cabb4c7bf6f805396026c2954759df5d49ce531973ad40eac0579afe71c6c84a`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 01:00:54 GMT
ADD file:c89d47099a38749a424760d9c7d3a6e982089455ba9d04140db15ba9eb4cdda1 in / 
# Sat, 28 May 2022 01:00:55 GMT
CMD ["bash"]
# Sun, 29 May 2022 07:05:56 GMT
ENV MONO_VERSION=6.10.0.104
# Sun, 29 May 2022 07:06:21 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sun, 29 May 2022 07:07:05 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sun, 29 May 2022 07:13:38 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:e41117292dc8c199b63ae1ec4485358841dbcba68dcbd13f379b66182efe832e`  
		Last Modified: Sat, 28 May 2022 01:16:58 GMT  
		Size: 22.7 MB (22748097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6b5f036a1216ac3e5915abea1a84831b74a1ff2b871db263e10c2e2e08b4142`  
		Last Modified: Sun, 29 May 2022 07:15:59 GMT  
		Size: 2.4 MB (2367010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:409ae0fbf5bf28a310fd03aadd6bffa63395647f871b13eaed93f64f950ba059`  
		Last Modified: Sun, 29 May 2022 07:16:09 GMT  
		Size: 23.8 MB (23814967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec96bdf28d4efd5575ecd00a81662307a45ee3647b1390250af23a417e9a6221`  
		Last Modified: Sun, 29 May 2022 07:18:32 GMT  
		Size: 127.8 MB (127830614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:4ad913193626124b371502c710e3339314f1f3bb74a0703db420ae4bf6115a73
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.4 MB (203364918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:772841f62edfdc3e44bdd0436bfa5fed09c6157d48fc0de3e2b9eaf93d29827a`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 00:41:05 GMT
ADD file:d0e42d603f275c040783ec7b6c051200815492fc35b73110234dfcd584e6cdec in / 
# Sat, 28 May 2022 00:41:05 GMT
CMD ["bash"]
# Sat, 28 May 2022 02:46:43 GMT
ENV MONO_VERSION=6.10.0.104
# Sat, 28 May 2022 02:46:56 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 May 2022 02:47:14 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 28 May 2022 02:49:42 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:4931fb8ba4223cb35034141162105ee5482122692b2931eb69eec912ce64606d`  
		Last Modified: Sat, 28 May 2022 00:48:26 GMT  
		Size: 25.9 MB (25914033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6c3b79fd8739d62f93b944c9df39ec0bf58c435823f5f6a513475d6545957fc`  
		Last Modified: Sat, 28 May 2022 02:50:47 GMT  
		Size: 2.6 MB (2641216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bd0b9d99a83cb1025314f18922e46290d9a8382984731de170c80555917bf88`  
		Last Modified: Sat, 28 May 2022 02:50:51 GMT  
		Size: 29.4 MB (29361373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fb21fd069762e361e5da65f994ba2dbbbfe69cff454d3587851a4c666dde1ac`  
		Last Modified: Sat, 28 May 2022 02:52:16 GMT  
		Size: 145.4 MB (145448296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10` - linux; 386

```console
$ docker pull mono@sha256:0a73655e94432bad92444b880c42977cd7a8d62c8c6beb451d3cb32364877d05
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.6 MB (230599470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f507210b13f9280f6b61ad3f51bc8158e7be3f949ca09f9ea1753415dd3f5508`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 00:40:01 GMT
ADD file:9aea7a35c215cdd778adec1dd5213973ef9b4830110e4550f2ead85679551ee5 in / 
# Sat, 28 May 2022 00:40:01 GMT
CMD ["bash"]
# Sat, 28 May 2022 03:46:25 GMT
ENV MONO_VERSION=6.10.0.104
# Sat, 28 May 2022 03:46:34 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 May 2022 03:46:57 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 28 May 2022 03:49:12 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:40837b3d848885c0b0c031d6d950b38e6a26962a5ee49704cb3ca2d2db535617`  
		Last Modified: Sat, 28 May 2022 00:47:36 GMT  
		Size: 27.8 MB (27799572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26c6f8d6dc5ceb0245c7840d3b8da79357e1e8dd082fd7c9652130845db89c80`  
		Last Modified: Sat, 28 May 2022 03:50:22 GMT  
		Size: 2.8 MB (2789329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fead69f7918b01952264f38b6148b7d4314ce4252dbd1ee1a1e477b8b2822323`  
		Last Modified: Sat, 28 May 2022 03:50:30 GMT  
		Size: 68.6 MB (68594113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37c3a22651e50a3f63c488401e2d164f8a05f1762463b2d1d5cf4ada30af01f3`  
		Last Modified: Sat, 28 May 2022 03:51:45 GMT  
		Size: 131.4 MB (131416456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10` - linux; ppc64le

```console
$ docker pull mono@sha256:fb21783f284ccd779d5cef774e3f2dc0ad65e092abc475e64fa920c204a34302
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.4 MB (192389720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c0d0620cf6d3d1c6844a5dd250a98ea9609241a0ecc00c9fbfd2bbf89fd283a`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 01:23:57 GMT
ADD file:a8c6c897bc64da424049ad04a354d123b0622abda1a56b2725f72de5e4569df8 in / 
# Sat, 28 May 2022 01:24:04 GMT
CMD ["bash"]
# Sat, 28 May 2022 07:01:39 GMT
ENV MONO_VERSION=6.10.0.104
# Sat, 28 May 2022 07:03:48 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 May 2022 07:04:58 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 28 May 2022 07:17:29 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:087d40850259bdcd3bee3d5d30d5a2070216727f72c1c9731b514ac3dbf7573e`  
		Last Modified: Sat, 28 May 2022 01:33:30 GMT  
		Size: 30.6 MB (30560238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93d15a4ed9e901c5973893d29da58346eb48933e55206b3f7bd5ab1a643b74c8`  
		Last Modified: Sat, 28 May 2022 07:18:57 GMT  
		Size: 2.9 MB (2892867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8453c12e4cdeaa1c20bb9884f8734579ed65294e9471d7349d895c568095b17e`  
		Last Modified: Sat, 28 May 2022 07:19:02 GMT  
		Size: 26.9 MB (26917810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1f6f8925221fb7d06fdbc2a81cf45a97ad5a82cd6a18e0d7629d560814bf36e`  
		Last Modified: Sat, 28 May 2022 07:20:33 GMT  
		Size: 132.0 MB (132018805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.10-slim`

```console
$ docker pull mono@sha256:2e81f7396b4cc3b31c8d48bb63fc1e71b884f00fe8bfdfa9665a4d891976a7e4
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
$ docker pull mono@sha256:95bdd6da39b31ff61184a0eb476e5e1d7b6ee24483b33a342a20cf4c15c8212f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.7 MB (94696682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84dc7c154d8c8383f24dfcbffd657a561f53e383add8c16cf69119b1f5abb682`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 01:20:43 GMT
ADD file:0513eda9512e010cb9459591b62e0c9d9319750923df091b64250ad6e98c2878 in / 
# Sat, 28 May 2022 01:20:43 GMT
CMD ["bash"]
# Sat, 28 May 2022 11:35:41 GMT
ENV MONO_VERSION=6.10.0.104
# Sat, 28 May 2022 11:35:50 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 May 2022 11:36:17 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:c1ad9731b2c7bf7fddea67f2f3f553515179a375c489e591e2372700fcaca766`  
		Last Modified: Sat, 28 May 2022 01:26:05 GMT  
		Size: 27.1 MB (27140144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:634a317d34eeec1b0e96f4fb4273064fea3fd708e5cfa450d4d09046d4cfc3d1`  
		Last Modified: Sat, 28 May 2022 11:47:38 GMT  
		Size: 2.8 MB (2777558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22b4be749876c6f886fe310e24cf0937bad3c1864521575a4af4e0e1412501ac`  
		Last Modified: Sat, 28 May 2022 11:47:48 GMT  
		Size: 64.8 MB (64778980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:e015623df135cd61f2bf8171aa6563257d49bbb13cb5ff3db08a6b8d0f87dd98
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.9 MB (51879692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79e43cb237e900ab2aef994a1a4352ab16654cefb27225709468db6bb80898f9`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 02:04:06 GMT
ADD file:26e9ed6c41ec12bf5fd602b7f86b924d34537bbc82442f630763f9f6c48bf3b3 in / 
# Sat, 28 May 2022 02:04:07 GMT
CMD ["bash"]
# Sat, 28 May 2022 04:03:10 GMT
ENV MONO_VERSION=6.10.0.104
# Sat, 28 May 2022 04:03:38 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 May 2022 04:04:26 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:19389fd1100abdedaa775b43242838cdd2d5c8c3388643a7e52da2b7b4399c15`  
		Last Modified: Sat, 28 May 2022 02:20:06 GMT  
		Size: 24.9 MB (24890069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26e8b570b3ab504ed3e8f73b1c63efee3410fb86aaab255274f2a7e1328ca292`  
		Last Modified: Sat, 28 May 2022 04:13:34 GMT  
		Size: 2.5 MB (2467793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daa9619bad699d3b6b5711965b8847aa3c3536cb1c715a01c67006bbf0423924`  
		Last Modified: Sat, 28 May 2022 04:13:53 GMT  
		Size: 24.5 MB (24521830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:00e2ff0bbe2d8dde7366b674a81b55485ca47c9fc9d9eb657864596803e63e81
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48930074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9c66231fc4aeb331b82f02cef080fe031976041453a368d0edb35f63665a900`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 01:00:54 GMT
ADD file:c89d47099a38749a424760d9c7d3a6e982089455ba9d04140db15ba9eb4cdda1 in / 
# Sat, 28 May 2022 01:00:55 GMT
CMD ["bash"]
# Sun, 29 May 2022 07:05:56 GMT
ENV MONO_VERSION=6.10.0.104
# Sun, 29 May 2022 07:06:21 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sun, 29 May 2022 07:07:05 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:e41117292dc8c199b63ae1ec4485358841dbcba68dcbd13f379b66182efe832e`  
		Last Modified: Sat, 28 May 2022 01:16:58 GMT  
		Size: 22.7 MB (22748097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6b5f036a1216ac3e5915abea1a84831b74a1ff2b871db263e10c2e2e08b4142`  
		Last Modified: Sun, 29 May 2022 07:15:59 GMT  
		Size: 2.4 MB (2367010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:409ae0fbf5bf28a310fd03aadd6bffa63395647f871b13eaed93f64f950ba059`  
		Last Modified: Sun, 29 May 2022 07:16:09 GMT  
		Size: 23.8 MB (23814967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:fa9b3688727ac29a197f1d7f614caeb60d8f2c6a6d98778d2b1c50bf77cf70b7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.9 MB (57916622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7833738a45dfc65adccd1ce72b119dd01df6d00a358d11655befaa5585339619`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 00:41:05 GMT
ADD file:d0e42d603f275c040783ec7b6c051200815492fc35b73110234dfcd584e6cdec in / 
# Sat, 28 May 2022 00:41:05 GMT
CMD ["bash"]
# Sat, 28 May 2022 02:46:43 GMT
ENV MONO_VERSION=6.10.0.104
# Sat, 28 May 2022 02:46:56 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 May 2022 02:47:14 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:4931fb8ba4223cb35034141162105ee5482122692b2931eb69eec912ce64606d`  
		Last Modified: Sat, 28 May 2022 00:48:26 GMT  
		Size: 25.9 MB (25914033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6c3b79fd8739d62f93b944c9df39ec0bf58c435823f5f6a513475d6545957fc`  
		Last Modified: Sat, 28 May 2022 02:50:47 GMT  
		Size: 2.6 MB (2641216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bd0b9d99a83cb1025314f18922e46290d9a8382984731de170c80555917bf88`  
		Last Modified: Sat, 28 May 2022 02:50:51 GMT  
		Size: 29.4 MB (29361373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10-slim` - linux; 386

```console
$ docker pull mono@sha256:ac20cc1e76afce9f3b1127a20e48cf2c70161808946240d3302c28a56667316f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.2 MB (99183014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f96e4af273d68648a685813d84b6f6d0be541181718dc699cb831bb35e250f8b`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 00:40:01 GMT
ADD file:9aea7a35c215cdd778adec1dd5213973ef9b4830110e4550f2ead85679551ee5 in / 
# Sat, 28 May 2022 00:40:01 GMT
CMD ["bash"]
# Sat, 28 May 2022 03:46:25 GMT
ENV MONO_VERSION=6.10.0.104
# Sat, 28 May 2022 03:46:34 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 May 2022 03:46:57 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:40837b3d848885c0b0c031d6d950b38e6a26962a5ee49704cb3ca2d2db535617`  
		Last Modified: Sat, 28 May 2022 00:47:36 GMT  
		Size: 27.8 MB (27799572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26c6f8d6dc5ceb0245c7840d3b8da79357e1e8dd082fd7c9652130845db89c80`  
		Last Modified: Sat, 28 May 2022 03:50:22 GMT  
		Size: 2.8 MB (2789329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fead69f7918b01952264f38b6148b7d4314ce4252dbd1ee1a1e477b8b2822323`  
		Last Modified: Sat, 28 May 2022 03:50:30 GMT  
		Size: 68.6 MB (68594113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:a48caf0aad4142ffafcb33cc547cfc4f0b150937091d028ca6c1458caf2ba8d5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.4 MB (60370915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e54f2a8abc8c29ec28498e2c94d2a987003b5c44baaa1586e81b05520da49d97`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 01:23:57 GMT
ADD file:a8c6c897bc64da424049ad04a354d123b0622abda1a56b2725f72de5e4569df8 in / 
# Sat, 28 May 2022 01:24:04 GMT
CMD ["bash"]
# Sat, 28 May 2022 07:01:39 GMT
ENV MONO_VERSION=6.10.0.104
# Sat, 28 May 2022 07:03:48 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 May 2022 07:04:58 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:087d40850259bdcd3bee3d5d30d5a2070216727f72c1c9731b514ac3dbf7573e`  
		Last Modified: Sat, 28 May 2022 01:33:30 GMT  
		Size: 30.6 MB (30560238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93d15a4ed9e901c5973893d29da58346eb48933e55206b3f7bd5ab1a643b74c8`  
		Last Modified: Sat, 28 May 2022 07:18:57 GMT  
		Size: 2.9 MB (2892867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8453c12e4cdeaa1c20bb9884f8734579ed65294e9471d7349d895c568095b17e`  
		Last Modified: Sat, 28 May 2022 07:19:02 GMT  
		Size: 26.9 MB (26917810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.10.0`

```console
$ docker pull mono@sha256:7fba975ee6fcad096a0c6822cb350bac90d8c5bfe8612ba9f9a78dd79722bd83
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
$ docker pull mono@sha256:66a99f9ed2a2c483aa5072a20049e2dd28742ad0a2b83e9727ec7ebf8a78de4c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.0 MB (225005893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91215f97e46cd1e11118e1d37a1b77a4ff94a998afcdadb40b8127cae3fa65bc`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 01:20:43 GMT
ADD file:0513eda9512e010cb9459591b62e0c9d9319750923df091b64250ad6e98c2878 in / 
# Sat, 28 May 2022 01:20:43 GMT
CMD ["bash"]
# Sat, 28 May 2022 11:35:41 GMT
ENV MONO_VERSION=6.10.0.104
# Sat, 28 May 2022 11:35:50 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 May 2022 11:36:17 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 28 May 2022 11:46:47 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:c1ad9731b2c7bf7fddea67f2f3f553515179a375c489e591e2372700fcaca766`  
		Last Modified: Sat, 28 May 2022 01:26:05 GMT  
		Size: 27.1 MB (27140144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:634a317d34eeec1b0e96f4fb4273064fea3fd708e5cfa450d4d09046d4cfc3d1`  
		Last Modified: Sat, 28 May 2022 11:47:38 GMT  
		Size: 2.8 MB (2777558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22b4be749876c6f886fe310e24cf0937bad3c1864521575a4af4e0e1412501ac`  
		Last Modified: Sat, 28 May 2022 11:47:48 GMT  
		Size: 64.8 MB (64778980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce15f229c8f857d448d87bfa56087e614ab3b63aca6261f823d63ef3b8ffe614`  
		Last Modified: Sat, 28 May 2022 11:48:55 GMT  
		Size: 130.3 MB (130309211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0` - linux; arm variant v5

```console
$ docker pull mono@sha256:0d0eaa12e7fcbbf941468045aa3512b501d40de39a152d93210d1c1dc54fe108
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.9 MB (180859738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:945cbaa5a9e079652bb0afec334b0d9abf93fec7db23291505ef02f47db7ed03`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 02:04:06 GMT
ADD file:26e9ed6c41ec12bf5fd602b7f86b924d34537bbc82442f630763f9f6c48bf3b3 in / 
# Sat, 28 May 2022 02:04:07 GMT
CMD ["bash"]
# Sat, 28 May 2022 04:03:10 GMT
ENV MONO_VERSION=6.10.0.104
# Sat, 28 May 2022 04:03:38 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 May 2022 04:04:26 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 28 May 2022 04:11:30 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:19389fd1100abdedaa775b43242838cdd2d5c8c3388643a7e52da2b7b4399c15`  
		Last Modified: Sat, 28 May 2022 02:20:06 GMT  
		Size: 24.9 MB (24890069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26e8b570b3ab504ed3e8f73b1c63efee3410fb86aaab255274f2a7e1328ca292`  
		Last Modified: Sat, 28 May 2022 04:13:34 GMT  
		Size: 2.5 MB (2467793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daa9619bad699d3b6b5711965b8847aa3c3536cb1c715a01c67006bbf0423924`  
		Last Modified: Sat, 28 May 2022 04:13:53 GMT  
		Size: 24.5 MB (24521830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:888817f0aafc0a9a017db76412ae019f21d2b979bcbaf99ab971eeaa02c08aa4`  
		Last Modified: Sat, 28 May 2022 04:17:32 GMT  
		Size: 129.0 MB (128980046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0` - linux; arm variant v7

```console
$ docker pull mono@sha256:5aa1ee4b7be1cbc3de8d81a09f8dbf8874577cd2a43d5ad0b7828471bdd8b3b5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.8 MB (176760688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cabb4c7bf6f805396026c2954759df5d49ce531973ad40eac0579afe71c6c84a`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 01:00:54 GMT
ADD file:c89d47099a38749a424760d9c7d3a6e982089455ba9d04140db15ba9eb4cdda1 in / 
# Sat, 28 May 2022 01:00:55 GMT
CMD ["bash"]
# Sun, 29 May 2022 07:05:56 GMT
ENV MONO_VERSION=6.10.0.104
# Sun, 29 May 2022 07:06:21 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sun, 29 May 2022 07:07:05 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sun, 29 May 2022 07:13:38 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:e41117292dc8c199b63ae1ec4485358841dbcba68dcbd13f379b66182efe832e`  
		Last Modified: Sat, 28 May 2022 01:16:58 GMT  
		Size: 22.7 MB (22748097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6b5f036a1216ac3e5915abea1a84831b74a1ff2b871db263e10c2e2e08b4142`  
		Last Modified: Sun, 29 May 2022 07:15:59 GMT  
		Size: 2.4 MB (2367010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:409ae0fbf5bf28a310fd03aadd6bffa63395647f871b13eaed93f64f950ba059`  
		Last Modified: Sun, 29 May 2022 07:16:09 GMT  
		Size: 23.8 MB (23814967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec96bdf28d4efd5575ecd00a81662307a45ee3647b1390250af23a417e9a6221`  
		Last Modified: Sun, 29 May 2022 07:18:32 GMT  
		Size: 127.8 MB (127830614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:4ad913193626124b371502c710e3339314f1f3bb74a0703db420ae4bf6115a73
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.4 MB (203364918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:772841f62edfdc3e44bdd0436bfa5fed09c6157d48fc0de3e2b9eaf93d29827a`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 00:41:05 GMT
ADD file:d0e42d603f275c040783ec7b6c051200815492fc35b73110234dfcd584e6cdec in / 
# Sat, 28 May 2022 00:41:05 GMT
CMD ["bash"]
# Sat, 28 May 2022 02:46:43 GMT
ENV MONO_VERSION=6.10.0.104
# Sat, 28 May 2022 02:46:56 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 May 2022 02:47:14 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 28 May 2022 02:49:42 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:4931fb8ba4223cb35034141162105ee5482122692b2931eb69eec912ce64606d`  
		Last Modified: Sat, 28 May 2022 00:48:26 GMT  
		Size: 25.9 MB (25914033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6c3b79fd8739d62f93b944c9df39ec0bf58c435823f5f6a513475d6545957fc`  
		Last Modified: Sat, 28 May 2022 02:50:47 GMT  
		Size: 2.6 MB (2641216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bd0b9d99a83cb1025314f18922e46290d9a8382984731de170c80555917bf88`  
		Last Modified: Sat, 28 May 2022 02:50:51 GMT  
		Size: 29.4 MB (29361373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fb21fd069762e361e5da65f994ba2dbbbfe69cff454d3587851a4c666dde1ac`  
		Last Modified: Sat, 28 May 2022 02:52:16 GMT  
		Size: 145.4 MB (145448296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0` - linux; 386

```console
$ docker pull mono@sha256:0a73655e94432bad92444b880c42977cd7a8d62c8c6beb451d3cb32364877d05
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.6 MB (230599470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f507210b13f9280f6b61ad3f51bc8158e7be3f949ca09f9ea1753415dd3f5508`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 00:40:01 GMT
ADD file:9aea7a35c215cdd778adec1dd5213973ef9b4830110e4550f2ead85679551ee5 in / 
# Sat, 28 May 2022 00:40:01 GMT
CMD ["bash"]
# Sat, 28 May 2022 03:46:25 GMT
ENV MONO_VERSION=6.10.0.104
# Sat, 28 May 2022 03:46:34 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 May 2022 03:46:57 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 28 May 2022 03:49:12 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:40837b3d848885c0b0c031d6d950b38e6a26962a5ee49704cb3ca2d2db535617`  
		Last Modified: Sat, 28 May 2022 00:47:36 GMT  
		Size: 27.8 MB (27799572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26c6f8d6dc5ceb0245c7840d3b8da79357e1e8dd082fd7c9652130845db89c80`  
		Last Modified: Sat, 28 May 2022 03:50:22 GMT  
		Size: 2.8 MB (2789329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fead69f7918b01952264f38b6148b7d4314ce4252dbd1ee1a1e477b8b2822323`  
		Last Modified: Sat, 28 May 2022 03:50:30 GMT  
		Size: 68.6 MB (68594113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37c3a22651e50a3f63c488401e2d164f8a05f1762463b2d1d5cf4ada30af01f3`  
		Last Modified: Sat, 28 May 2022 03:51:45 GMT  
		Size: 131.4 MB (131416456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0` - linux; ppc64le

```console
$ docker pull mono@sha256:fb21783f284ccd779d5cef774e3f2dc0ad65e092abc475e64fa920c204a34302
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.4 MB (192389720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c0d0620cf6d3d1c6844a5dd250a98ea9609241a0ecc00c9fbfd2bbf89fd283a`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 01:23:57 GMT
ADD file:a8c6c897bc64da424049ad04a354d123b0622abda1a56b2725f72de5e4569df8 in / 
# Sat, 28 May 2022 01:24:04 GMT
CMD ["bash"]
# Sat, 28 May 2022 07:01:39 GMT
ENV MONO_VERSION=6.10.0.104
# Sat, 28 May 2022 07:03:48 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 May 2022 07:04:58 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 28 May 2022 07:17:29 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:087d40850259bdcd3bee3d5d30d5a2070216727f72c1c9731b514ac3dbf7573e`  
		Last Modified: Sat, 28 May 2022 01:33:30 GMT  
		Size: 30.6 MB (30560238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93d15a4ed9e901c5973893d29da58346eb48933e55206b3f7bd5ab1a643b74c8`  
		Last Modified: Sat, 28 May 2022 07:18:57 GMT  
		Size: 2.9 MB (2892867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8453c12e4cdeaa1c20bb9884f8734579ed65294e9471d7349d895c568095b17e`  
		Last Modified: Sat, 28 May 2022 07:19:02 GMT  
		Size: 26.9 MB (26917810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1f6f8925221fb7d06fdbc2a81cf45a97ad5a82cd6a18e0d7629d560814bf36e`  
		Last Modified: Sat, 28 May 2022 07:20:33 GMT  
		Size: 132.0 MB (132018805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.10.0-slim`

```console
$ docker pull mono@sha256:2e81f7396b4cc3b31c8d48bb63fc1e71b884f00fe8bfdfa9665a4d891976a7e4
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
$ docker pull mono@sha256:95bdd6da39b31ff61184a0eb476e5e1d7b6ee24483b33a342a20cf4c15c8212f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.7 MB (94696682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84dc7c154d8c8383f24dfcbffd657a561f53e383add8c16cf69119b1f5abb682`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 01:20:43 GMT
ADD file:0513eda9512e010cb9459591b62e0c9d9319750923df091b64250ad6e98c2878 in / 
# Sat, 28 May 2022 01:20:43 GMT
CMD ["bash"]
# Sat, 28 May 2022 11:35:41 GMT
ENV MONO_VERSION=6.10.0.104
# Sat, 28 May 2022 11:35:50 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 May 2022 11:36:17 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:c1ad9731b2c7bf7fddea67f2f3f553515179a375c489e591e2372700fcaca766`  
		Last Modified: Sat, 28 May 2022 01:26:05 GMT  
		Size: 27.1 MB (27140144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:634a317d34eeec1b0e96f4fb4273064fea3fd708e5cfa450d4d09046d4cfc3d1`  
		Last Modified: Sat, 28 May 2022 11:47:38 GMT  
		Size: 2.8 MB (2777558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22b4be749876c6f886fe310e24cf0937bad3c1864521575a4af4e0e1412501ac`  
		Last Modified: Sat, 28 May 2022 11:47:48 GMT  
		Size: 64.8 MB (64778980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:e015623df135cd61f2bf8171aa6563257d49bbb13cb5ff3db08a6b8d0f87dd98
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.9 MB (51879692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79e43cb237e900ab2aef994a1a4352ab16654cefb27225709468db6bb80898f9`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 02:04:06 GMT
ADD file:26e9ed6c41ec12bf5fd602b7f86b924d34537bbc82442f630763f9f6c48bf3b3 in / 
# Sat, 28 May 2022 02:04:07 GMT
CMD ["bash"]
# Sat, 28 May 2022 04:03:10 GMT
ENV MONO_VERSION=6.10.0.104
# Sat, 28 May 2022 04:03:38 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 May 2022 04:04:26 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:19389fd1100abdedaa775b43242838cdd2d5c8c3388643a7e52da2b7b4399c15`  
		Last Modified: Sat, 28 May 2022 02:20:06 GMT  
		Size: 24.9 MB (24890069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26e8b570b3ab504ed3e8f73b1c63efee3410fb86aaab255274f2a7e1328ca292`  
		Last Modified: Sat, 28 May 2022 04:13:34 GMT  
		Size: 2.5 MB (2467793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daa9619bad699d3b6b5711965b8847aa3c3536cb1c715a01c67006bbf0423924`  
		Last Modified: Sat, 28 May 2022 04:13:53 GMT  
		Size: 24.5 MB (24521830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:00e2ff0bbe2d8dde7366b674a81b55485ca47c9fc9d9eb657864596803e63e81
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48930074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9c66231fc4aeb331b82f02cef080fe031976041453a368d0edb35f63665a900`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 01:00:54 GMT
ADD file:c89d47099a38749a424760d9c7d3a6e982089455ba9d04140db15ba9eb4cdda1 in / 
# Sat, 28 May 2022 01:00:55 GMT
CMD ["bash"]
# Sun, 29 May 2022 07:05:56 GMT
ENV MONO_VERSION=6.10.0.104
# Sun, 29 May 2022 07:06:21 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sun, 29 May 2022 07:07:05 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:e41117292dc8c199b63ae1ec4485358841dbcba68dcbd13f379b66182efe832e`  
		Last Modified: Sat, 28 May 2022 01:16:58 GMT  
		Size: 22.7 MB (22748097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6b5f036a1216ac3e5915abea1a84831b74a1ff2b871db263e10c2e2e08b4142`  
		Last Modified: Sun, 29 May 2022 07:15:59 GMT  
		Size: 2.4 MB (2367010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:409ae0fbf5bf28a310fd03aadd6bffa63395647f871b13eaed93f64f950ba059`  
		Last Modified: Sun, 29 May 2022 07:16:09 GMT  
		Size: 23.8 MB (23814967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:fa9b3688727ac29a197f1d7f614caeb60d8f2c6a6d98778d2b1c50bf77cf70b7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.9 MB (57916622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7833738a45dfc65adccd1ce72b119dd01df6d00a358d11655befaa5585339619`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 00:41:05 GMT
ADD file:d0e42d603f275c040783ec7b6c051200815492fc35b73110234dfcd584e6cdec in / 
# Sat, 28 May 2022 00:41:05 GMT
CMD ["bash"]
# Sat, 28 May 2022 02:46:43 GMT
ENV MONO_VERSION=6.10.0.104
# Sat, 28 May 2022 02:46:56 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 May 2022 02:47:14 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:4931fb8ba4223cb35034141162105ee5482122692b2931eb69eec912ce64606d`  
		Last Modified: Sat, 28 May 2022 00:48:26 GMT  
		Size: 25.9 MB (25914033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6c3b79fd8739d62f93b944c9df39ec0bf58c435823f5f6a513475d6545957fc`  
		Last Modified: Sat, 28 May 2022 02:50:47 GMT  
		Size: 2.6 MB (2641216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bd0b9d99a83cb1025314f18922e46290d9a8382984731de170c80555917bf88`  
		Last Modified: Sat, 28 May 2022 02:50:51 GMT  
		Size: 29.4 MB (29361373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0-slim` - linux; 386

```console
$ docker pull mono@sha256:ac20cc1e76afce9f3b1127a20e48cf2c70161808946240d3302c28a56667316f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.2 MB (99183014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f96e4af273d68648a685813d84b6f6d0be541181718dc699cb831bb35e250f8b`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 00:40:01 GMT
ADD file:9aea7a35c215cdd778adec1dd5213973ef9b4830110e4550f2ead85679551ee5 in / 
# Sat, 28 May 2022 00:40:01 GMT
CMD ["bash"]
# Sat, 28 May 2022 03:46:25 GMT
ENV MONO_VERSION=6.10.0.104
# Sat, 28 May 2022 03:46:34 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 May 2022 03:46:57 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:40837b3d848885c0b0c031d6d950b38e6a26962a5ee49704cb3ca2d2db535617`  
		Last Modified: Sat, 28 May 2022 00:47:36 GMT  
		Size: 27.8 MB (27799572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26c6f8d6dc5ceb0245c7840d3b8da79357e1e8dd082fd7c9652130845db89c80`  
		Last Modified: Sat, 28 May 2022 03:50:22 GMT  
		Size: 2.8 MB (2789329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fead69f7918b01952264f38b6148b7d4314ce4252dbd1ee1a1e477b8b2822323`  
		Last Modified: Sat, 28 May 2022 03:50:30 GMT  
		Size: 68.6 MB (68594113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:a48caf0aad4142ffafcb33cc547cfc4f0b150937091d028ca6c1458caf2ba8d5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.4 MB (60370915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e54f2a8abc8c29ec28498e2c94d2a987003b5c44baaa1586e81b05520da49d97`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 01:23:57 GMT
ADD file:a8c6c897bc64da424049ad04a354d123b0622abda1a56b2725f72de5e4569df8 in / 
# Sat, 28 May 2022 01:24:04 GMT
CMD ["bash"]
# Sat, 28 May 2022 07:01:39 GMT
ENV MONO_VERSION=6.10.0.104
# Sat, 28 May 2022 07:03:48 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 May 2022 07:04:58 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:087d40850259bdcd3bee3d5d30d5a2070216727f72c1c9731b514ac3dbf7573e`  
		Last Modified: Sat, 28 May 2022 01:33:30 GMT  
		Size: 30.6 MB (30560238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93d15a4ed9e901c5973893d29da58346eb48933e55206b3f7bd5ab1a643b74c8`  
		Last Modified: Sat, 28 May 2022 07:18:57 GMT  
		Size: 2.9 MB (2892867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8453c12e4cdeaa1c20bb9884f8734579ed65294e9471d7349d895c568095b17e`  
		Last Modified: Sat, 28 May 2022 07:19:02 GMT  
		Size: 26.9 MB (26917810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.10.0.104`

```console
$ docker pull mono@sha256:7fba975ee6fcad096a0c6822cb350bac90d8c5bfe8612ba9f9a78dd79722bd83
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
$ docker pull mono@sha256:66a99f9ed2a2c483aa5072a20049e2dd28742ad0a2b83e9727ec7ebf8a78de4c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.0 MB (225005893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91215f97e46cd1e11118e1d37a1b77a4ff94a998afcdadb40b8127cae3fa65bc`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 01:20:43 GMT
ADD file:0513eda9512e010cb9459591b62e0c9d9319750923df091b64250ad6e98c2878 in / 
# Sat, 28 May 2022 01:20:43 GMT
CMD ["bash"]
# Sat, 28 May 2022 11:35:41 GMT
ENV MONO_VERSION=6.10.0.104
# Sat, 28 May 2022 11:35:50 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 May 2022 11:36:17 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 28 May 2022 11:46:47 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:c1ad9731b2c7bf7fddea67f2f3f553515179a375c489e591e2372700fcaca766`  
		Last Modified: Sat, 28 May 2022 01:26:05 GMT  
		Size: 27.1 MB (27140144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:634a317d34eeec1b0e96f4fb4273064fea3fd708e5cfa450d4d09046d4cfc3d1`  
		Last Modified: Sat, 28 May 2022 11:47:38 GMT  
		Size: 2.8 MB (2777558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22b4be749876c6f886fe310e24cf0937bad3c1864521575a4af4e0e1412501ac`  
		Last Modified: Sat, 28 May 2022 11:47:48 GMT  
		Size: 64.8 MB (64778980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce15f229c8f857d448d87bfa56087e614ab3b63aca6261f823d63ef3b8ffe614`  
		Last Modified: Sat, 28 May 2022 11:48:55 GMT  
		Size: 130.3 MB (130309211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0.104` - linux; arm variant v5

```console
$ docker pull mono@sha256:0d0eaa12e7fcbbf941468045aa3512b501d40de39a152d93210d1c1dc54fe108
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.9 MB (180859738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:945cbaa5a9e079652bb0afec334b0d9abf93fec7db23291505ef02f47db7ed03`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 02:04:06 GMT
ADD file:26e9ed6c41ec12bf5fd602b7f86b924d34537bbc82442f630763f9f6c48bf3b3 in / 
# Sat, 28 May 2022 02:04:07 GMT
CMD ["bash"]
# Sat, 28 May 2022 04:03:10 GMT
ENV MONO_VERSION=6.10.0.104
# Sat, 28 May 2022 04:03:38 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 May 2022 04:04:26 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 28 May 2022 04:11:30 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:19389fd1100abdedaa775b43242838cdd2d5c8c3388643a7e52da2b7b4399c15`  
		Last Modified: Sat, 28 May 2022 02:20:06 GMT  
		Size: 24.9 MB (24890069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26e8b570b3ab504ed3e8f73b1c63efee3410fb86aaab255274f2a7e1328ca292`  
		Last Modified: Sat, 28 May 2022 04:13:34 GMT  
		Size: 2.5 MB (2467793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daa9619bad699d3b6b5711965b8847aa3c3536cb1c715a01c67006bbf0423924`  
		Last Modified: Sat, 28 May 2022 04:13:53 GMT  
		Size: 24.5 MB (24521830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:888817f0aafc0a9a017db76412ae019f21d2b979bcbaf99ab971eeaa02c08aa4`  
		Last Modified: Sat, 28 May 2022 04:17:32 GMT  
		Size: 129.0 MB (128980046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0.104` - linux; arm variant v7

```console
$ docker pull mono@sha256:5aa1ee4b7be1cbc3de8d81a09f8dbf8874577cd2a43d5ad0b7828471bdd8b3b5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.8 MB (176760688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cabb4c7bf6f805396026c2954759df5d49ce531973ad40eac0579afe71c6c84a`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 01:00:54 GMT
ADD file:c89d47099a38749a424760d9c7d3a6e982089455ba9d04140db15ba9eb4cdda1 in / 
# Sat, 28 May 2022 01:00:55 GMT
CMD ["bash"]
# Sun, 29 May 2022 07:05:56 GMT
ENV MONO_VERSION=6.10.0.104
# Sun, 29 May 2022 07:06:21 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sun, 29 May 2022 07:07:05 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sun, 29 May 2022 07:13:38 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:e41117292dc8c199b63ae1ec4485358841dbcba68dcbd13f379b66182efe832e`  
		Last Modified: Sat, 28 May 2022 01:16:58 GMT  
		Size: 22.7 MB (22748097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6b5f036a1216ac3e5915abea1a84831b74a1ff2b871db263e10c2e2e08b4142`  
		Last Modified: Sun, 29 May 2022 07:15:59 GMT  
		Size: 2.4 MB (2367010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:409ae0fbf5bf28a310fd03aadd6bffa63395647f871b13eaed93f64f950ba059`  
		Last Modified: Sun, 29 May 2022 07:16:09 GMT  
		Size: 23.8 MB (23814967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec96bdf28d4efd5575ecd00a81662307a45ee3647b1390250af23a417e9a6221`  
		Last Modified: Sun, 29 May 2022 07:18:32 GMT  
		Size: 127.8 MB (127830614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0.104` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:4ad913193626124b371502c710e3339314f1f3bb74a0703db420ae4bf6115a73
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.4 MB (203364918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:772841f62edfdc3e44bdd0436bfa5fed09c6157d48fc0de3e2b9eaf93d29827a`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 00:41:05 GMT
ADD file:d0e42d603f275c040783ec7b6c051200815492fc35b73110234dfcd584e6cdec in / 
# Sat, 28 May 2022 00:41:05 GMT
CMD ["bash"]
# Sat, 28 May 2022 02:46:43 GMT
ENV MONO_VERSION=6.10.0.104
# Sat, 28 May 2022 02:46:56 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 May 2022 02:47:14 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 28 May 2022 02:49:42 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:4931fb8ba4223cb35034141162105ee5482122692b2931eb69eec912ce64606d`  
		Last Modified: Sat, 28 May 2022 00:48:26 GMT  
		Size: 25.9 MB (25914033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6c3b79fd8739d62f93b944c9df39ec0bf58c435823f5f6a513475d6545957fc`  
		Last Modified: Sat, 28 May 2022 02:50:47 GMT  
		Size: 2.6 MB (2641216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bd0b9d99a83cb1025314f18922e46290d9a8382984731de170c80555917bf88`  
		Last Modified: Sat, 28 May 2022 02:50:51 GMT  
		Size: 29.4 MB (29361373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fb21fd069762e361e5da65f994ba2dbbbfe69cff454d3587851a4c666dde1ac`  
		Last Modified: Sat, 28 May 2022 02:52:16 GMT  
		Size: 145.4 MB (145448296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0.104` - linux; 386

```console
$ docker pull mono@sha256:0a73655e94432bad92444b880c42977cd7a8d62c8c6beb451d3cb32364877d05
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.6 MB (230599470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f507210b13f9280f6b61ad3f51bc8158e7be3f949ca09f9ea1753415dd3f5508`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 00:40:01 GMT
ADD file:9aea7a35c215cdd778adec1dd5213973ef9b4830110e4550f2ead85679551ee5 in / 
# Sat, 28 May 2022 00:40:01 GMT
CMD ["bash"]
# Sat, 28 May 2022 03:46:25 GMT
ENV MONO_VERSION=6.10.0.104
# Sat, 28 May 2022 03:46:34 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 May 2022 03:46:57 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 28 May 2022 03:49:12 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:40837b3d848885c0b0c031d6d950b38e6a26962a5ee49704cb3ca2d2db535617`  
		Last Modified: Sat, 28 May 2022 00:47:36 GMT  
		Size: 27.8 MB (27799572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26c6f8d6dc5ceb0245c7840d3b8da79357e1e8dd082fd7c9652130845db89c80`  
		Last Modified: Sat, 28 May 2022 03:50:22 GMT  
		Size: 2.8 MB (2789329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fead69f7918b01952264f38b6148b7d4314ce4252dbd1ee1a1e477b8b2822323`  
		Last Modified: Sat, 28 May 2022 03:50:30 GMT  
		Size: 68.6 MB (68594113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37c3a22651e50a3f63c488401e2d164f8a05f1762463b2d1d5cf4ada30af01f3`  
		Last Modified: Sat, 28 May 2022 03:51:45 GMT  
		Size: 131.4 MB (131416456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0.104` - linux; ppc64le

```console
$ docker pull mono@sha256:fb21783f284ccd779d5cef774e3f2dc0ad65e092abc475e64fa920c204a34302
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.4 MB (192389720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c0d0620cf6d3d1c6844a5dd250a98ea9609241a0ecc00c9fbfd2bbf89fd283a`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 01:23:57 GMT
ADD file:a8c6c897bc64da424049ad04a354d123b0622abda1a56b2725f72de5e4569df8 in / 
# Sat, 28 May 2022 01:24:04 GMT
CMD ["bash"]
# Sat, 28 May 2022 07:01:39 GMT
ENV MONO_VERSION=6.10.0.104
# Sat, 28 May 2022 07:03:48 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 May 2022 07:04:58 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 28 May 2022 07:17:29 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:087d40850259bdcd3bee3d5d30d5a2070216727f72c1c9731b514ac3dbf7573e`  
		Last Modified: Sat, 28 May 2022 01:33:30 GMT  
		Size: 30.6 MB (30560238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93d15a4ed9e901c5973893d29da58346eb48933e55206b3f7bd5ab1a643b74c8`  
		Last Modified: Sat, 28 May 2022 07:18:57 GMT  
		Size: 2.9 MB (2892867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8453c12e4cdeaa1c20bb9884f8734579ed65294e9471d7349d895c568095b17e`  
		Last Modified: Sat, 28 May 2022 07:19:02 GMT  
		Size: 26.9 MB (26917810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1f6f8925221fb7d06fdbc2a81cf45a97ad5a82cd6a18e0d7629d560814bf36e`  
		Last Modified: Sat, 28 May 2022 07:20:33 GMT  
		Size: 132.0 MB (132018805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.10.0.104-slim`

```console
$ docker pull mono@sha256:2e81f7396b4cc3b31c8d48bb63fc1e71b884f00fe8bfdfa9665a4d891976a7e4
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
$ docker pull mono@sha256:95bdd6da39b31ff61184a0eb476e5e1d7b6ee24483b33a342a20cf4c15c8212f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.7 MB (94696682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84dc7c154d8c8383f24dfcbffd657a561f53e383add8c16cf69119b1f5abb682`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 01:20:43 GMT
ADD file:0513eda9512e010cb9459591b62e0c9d9319750923df091b64250ad6e98c2878 in / 
# Sat, 28 May 2022 01:20:43 GMT
CMD ["bash"]
# Sat, 28 May 2022 11:35:41 GMT
ENV MONO_VERSION=6.10.0.104
# Sat, 28 May 2022 11:35:50 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 May 2022 11:36:17 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:c1ad9731b2c7bf7fddea67f2f3f553515179a375c489e591e2372700fcaca766`  
		Last Modified: Sat, 28 May 2022 01:26:05 GMT  
		Size: 27.1 MB (27140144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:634a317d34eeec1b0e96f4fb4273064fea3fd708e5cfa450d4d09046d4cfc3d1`  
		Last Modified: Sat, 28 May 2022 11:47:38 GMT  
		Size: 2.8 MB (2777558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22b4be749876c6f886fe310e24cf0937bad3c1864521575a4af4e0e1412501ac`  
		Last Modified: Sat, 28 May 2022 11:47:48 GMT  
		Size: 64.8 MB (64778980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0.104-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:e015623df135cd61f2bf8171aa6563257d49bbb13cb5ff3db08a6b8d0f87dd98
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.9 MB (51879692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79e43cb237e900ab2aef994a1a4352ab16654cefb27225709468db6bb80898f9`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 02:04:06 GMT
ADD file:26e9ed6c41ec12bf5fd602b7f86b924d34537bbc82442f630763f9f6c48bf3b3 in / 
# Sat, 28 May 2022 02:04:07 GMT
CMD ["bash"]
# Sat, 28 May 2022 04:03:10 GMT
ENV MONO_VERSION=6.10.0.104
# Sat, 28 May 2022 04:03:38 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 May 2022 04:04:26 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:19389fd1100abdedaa775b43242838cdd2d5c8c3388643a7e52da2b7b4399c15`  
		Last Modified: Sat, 28 May 2022 02:20:06 GMT  
		Size: 24.9 MB (24890069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26e8b570b3ab504ed3e8f73b1c63efee3410fb86aaab255274f2a7e1328ca292`  
		Last Modified: Sat, 28 May 2022 04:13:34 GMT  
		Size: 2.5 MB (2467793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daa9619bad699d3b6b5711965b8847aa3c3536cb1c715a01c67006bbf0423924`  
		Last Modified: Sat, 28 May 2022 04:13:53 GMT  
		Size: 24.5 MB (24521830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0.104-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:00e2ff0bbe2d8dde7366b674a81b55485ca47c9fc9d9eb657864596803e63e81
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48930074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9c66231fc4aeb331b82f02cef080fe031976041453a368d0edb35f63665a900`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 01:00:54 GMT
ADD file:c89d47099a38749a424760d9c7d3a6e982089455ba9d04140db15ba9eb4cdda1 in / 
# Sat, 28 May 2022 01:00:55 GMT
CMD ["bash"]
# Sun, 29 May 2022 07:05:56 GMT
ENV MONO_VERSION=6.10.0.104
# Sun, 29 May 2022 07:06:21 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sun, 29 May 2022 07:07:05 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:e41117292dc8c199b63ae1ec4485358841dbcba68dcbd13f379b66182efe832e`  
		Last Modified: Sat, 28 May 2022 01:16:58 GMT  
		Size: 22.7 MB (22748097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6b5f036a1216ac3e5915abea1a84831b74a1ff2b871db263e10c2e2e08b4142`  
		Last Modified: Sun, 29 May 2022 07:15:59 GMT  
		Size: 2.4 MB (2367010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:409ae0fbf5bf28a310fd03aadd6bffa63395647f871b13eaed93f64f950ba059`  
		Last Modified: Sun, 29 May 2022 07:16:09 GMT  
		Size: 23.8 MB (23814967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0.104-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:fa9b3688727ac29a197f1d7f614caeb60d8f2c6a6d98778d2b1c50bf77cf70b7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.9 MB (57916622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7833738a45dfc65adccd1ce72b119dd01df6d00a358d11655befaa5585339619`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 00:41:05 GMT
ADD file:d0e42d603f275c040783ec7b6c051200815492fc35b73110234dfcd584e6cdec in / 
# Sat, 28 May 2022 00:41:05 GMT
CMD ["bash"]
# Sat, 28 May 2022 02:46:43 GMT
ENV MONO_VERSION=6.10.0.104
# Sat, 28 May 2022 02:46:56 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 May 2022 02:47:14 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:4931fb8ba4223cb35034141162105ee5482122692b2931eb69eec912ce64606d`  
		Last Modified: Sat, 28 May 2022 00:48:26 GMT  
		Size: 25.9 MB (25914033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6c3b79fd8739d62f93b944c9df39ec0bf58c435823f5f6a513475d6545957fc`  
		Last Modified: Sat, 28 May 2022 02:50:47 GMT  
		Size: 2.6 MB (2641216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bd0b9d99a83cb1025314f18922e46290d9a8382984731de170c80555917bf88`  
		Last Modified: Sat, 28 May 2022 02:50:51 GMT  
		Size: 29.4 MB (29361373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0.104-slim` - linux; 386

```console
$ docker pull mono@sha256:ac20cc1e76afce9f3b1127a20e48cf2c70161808946240d3302c28a56667316f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.2 MB (99183014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f96e4af273d68648a685813d84b6f6d0be541181718dc699cb831bb35e250f8b`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 00:40:01 GMT
ADD file:9aea7a35c215cdd778adec1dd5213973ef9b4830110e4550f2ead85679551ee5 in / 
# Sat, 28 May 2022 00:40:01 GMT
CMD ["bash"]
# Sat, 28 May 2022 03:46:25 GMT
ENV MONO_VERSION=6.10.0.104
# Sat, 28 May 2022 03:46:34 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 May 2022 03:46:57 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:40837b3d848885c0b0c031d6d950b38e6a26962a5ee49704cb3ca2d2db535617`  
		Last Modified: Sat, 28 May 2022 00:47:36 GMT  
		Size: 27.8 MB (27799572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26c6f8d6dc5ceb0245c7840d3b8da79357e1e8dd082fd7c9652130845db89c80`  
		Last Modified: Sat, 28 May 2022 03:50:22 GMT  
		Size: 2.8 MB (2789329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fead69f7918b01952264f38b6148b7d4314ce4252dbd1ee1a1e477b8b2822323`  
		Last Modified: Sat, 28 May 2022 03:50:30 GMT  
		Size: 68.6 MB (68594113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0.104-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:a48caf0aad4142ffafcb33cc547cfc4f0b150937091d028ca6c1458caf2ba8d5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.4 MB (60370915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e54f2a8abc8c29ec28498e2c94d2a987003b5c44baaa1586e81b05520da49d97`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 01:23:57 GMT
ADD file:a8c6c897bc64da424049ad04a354d123b0622abda1a56b2725f72de5e4569df8 in / 
# Sat, 28 May 2022 01:24:04 GMT
CMD ["bash"]
# Sat, 28 May 2022 07:01:39 GMT
ENV MONO_VERSION=6.10.0.104
# Sat, 28 May 2022 07:03:48 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 May 2022 07:04:58 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:087d40850259bdcd3bee3d5d30d5a2070216727f72c1c9731b514ac3dbf7573e`  
		Last Modified: Sat, 28 May 2022 01:33:30 GMT  
		Size: 30.6 MB (30560238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93d15a4ed9e901c5973893d29da58346eb48933e55206b3f7bd5ab1a643b74c8`  
		Last Modified: Sat, 28 May 2022 07:18:57 GMT  
		Size: 2.9 MB (2892867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8453c12e4cdeaa1c20bb9884f8734579ed65294e9471d7349d895c568095b17e`  
		Last Modified: Sat, 28 May 2022 07:19:02 GMT  
		Size: 26.9 MB (26917810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.12`

```console
$ docker pull mono@sha256:bcc2d36c88898cdd62a9e18f97ad863c44b30fb74a23585549808f7db216a717
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
$ docker pull mono@sha256:c868b8345d1b67f672c229bfb330f5e1ba58cfcc33a6d46a9375b39bc25d5bda
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.4 MB (254416410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4527a2fc6d1eab132a7db6cd829d5d905553a692c5680c5e233251932e8d2e3`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 01:20:43 GMT
ADD file:0513eda9512e010cb9459591b62e0c9d9319750923df091b64250ad6e98c2878 in / 
# Sat, 28 May 2022 01:20:43 GMT
CMD ["bash"]
# Wed, 22 Jun 2022 21:33:20 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 22 Jun 2022 21:33:29 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jun 2022 21:33:47 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 22 Jun 2022 21:34:59 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:c1ad9731b2c7bf7fddea67f2f3f553515179a375c489e591e2372700fcaca766`  
		Last Modified: Sat, 28 May 2022 01:26:05 GMT  
		Size: 27.1 MB (27140144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36bdd50eb1bac9261e7d11ef7736774181be91ac4c30c02e1c1c4cc1c567a999`  
		Last Modified: Wed, 22 Jun 2022 21:35:25 GMT  
		Size: 2.8 MB (2777561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aba950124d67df356ccc1d947efdfd8cb5c8a7769434bc4057d371b5897b4d2e`  
		Last Modified: Wed, 22 Jun 2022 21:35:35 GMT  
		Size: 64.8 MB (64772708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e06195ea08da0f4b76c03b1a888e1149b4b7456b3137a22534ed08d300e9e9ff`  
		Last Modified: Wed, 22 Jun 2022 21:36:17 GMT  
		Size: 159.7 MB (159725997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12` - linux; arm variant v5

```console
$ docker pull mono@sha256:eecb4ce0a2143b972b80438d19719eedce94ea3734c1209e616f2c7b1752e397
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.9 MB (192881569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc56159c8ddff3dd73991b2b958f358c0e6b8a5dc881ad7a926c459b4be00031`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 02:04:06 GMT
ADD file:26e9ed6c41ec12bf5fd602b7f86b924d34537bbc82442f630763f9f6c48bf3b3 in / 
# Sat, 28 May 2022 02:04:07 GMT
CMD ["bash"]
# Wed, 22 Jun 2022 19:49:00 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 22 Jun 2022 19:49:28 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jun 2022 19:50:19 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 22 Jun 2022 19:54:03 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:19389fd1100abdedaa775b43242838cdd2d5c8c3388643a7e52da2b7b4399c15`  
		Last Modified: Sat, 28 May 2022 02:20:06 GMT  
		Size: 24.9 MB (24890069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa92f2f021e75803ce535a7facb85567bc17614f5919ffd2ded82252e6d03d5e`  
		Last Modified: Wed, 22 Jun 2022 19:55:44 GMT  
		Size: 2.5 MB (2467777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:946e5a3fcfdd33b760be56e03b5bd597eb8df3d50ee8880f36418e4b23a50fd8`  
		Last Modified: Wed, 22 Jun 2022 19:56:01 GMT  
		Size: 24.5 MB (24503493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e7dcb1cf8147d4ccbe01cb4986ecc814d15c96443e421575b6ec406ce783e98`  
		Last Modified: Wed, 22 Jun 2022 19:58:06 GMT  
		Size: 141.0 MB (141020230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12` - linux; arm variant v7

```console
$ docker pull mono@sha256:8e6e34d1a1ae5a2de0c439461a0cb502b0cd22220cd6774b90cb62fa5e240a92
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.8 MB (188782584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8afa747cef2c601df113d6bbdf74340305ece2fa03b83f9dd709d64178ced488`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 01:00:54 GMT
ADD file:c89d47099a38749a424760d9c7d3a6e982089455ba9d04140db15ba9eb4cdda1 in / 
# Sat, 28 May 2022 01:00:55 GMT
CMD ["bash"]
# Wed, 22 Jun 2022 21:53:04 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 22 Jun 2022 21:53:30 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jun 2022 21:54:14 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 22 Jun 2022 21:57:44 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:e41117292dc8c199b63ae1ec4485358841dbcba68dcbd13f379b66182efe832e`  
		Last Modified: Sat, 28 May 2022 01:16:58 GMT  
		Size: 22.7 MB (22748097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cea7b08703ed144c6d58b457cac40359088319d3ed62617dcbd6e3f36943b28a`  
		Last Modified: Wed, 22 Jun 2022 21:59:22 GMT  
		Size: 2.4 MB (2367003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c63834d12328a6bcb0b82fbfb83fef45b3596496346470249ba9c388730688a2`  
		Last Modified: Wed, 22 Jun 2022 21:59:38 GMT  
		Size: 23.8 MB (23789737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ec56912b25995fca9411a168ff99dcefede44b3e81975719b204e56f0a02971`  
		Last Modified: Wed, 22 Jun 2022 22:01:46 GMT  
		Size: 139.9 MB (139877747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:4654e59232e7dc6ba687050cc60cb311e0ef287235be7e88b313d69fa8565a7b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.9 MB (215904246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cae1924b9544a9ab52d1b2e09daec6d8f9560b3cbccb8f50929cc577b91940ab`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 00:41:05 GMT
ADD file:d0e42d603f275c040783ec7b6c051200815492fc35b73110234dfcd584e6cdec in / 
# Sat, 28 May 2022 00:41:05 GMT
CMD ["bash"]
# Wed, 22 Jun 2022 20:48:48 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 22 Jun 2022 20:48:57 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jun 2022 20:49:12 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 22 Jun 2022 20:50:20 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:4931fb8ba4223cb35034141162105ee5482122692b2931eb69eec912ce64606d`  
		Last Modified: Sat, 28 May 2022 00:48:26 GMT  
		Size: 25.9 MB (25914033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f06cddbf5d49ff334333bc51c02936695c616c52497d3284e91848de8085104a`  
		Last Modified: Wed, 22 Jun 2022 20:51:01 GMT  
		Size: 2.6 MB (2641202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:751c39f1c5edbe681c6c8ee877cb5e858b51e875ddf051ef6c2d8ef93b840da5`  
		Last Modified: Wed, 22 Jun 2022 20:51:06 GMT  
		Size: 29.3 MB (29333416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fcd120a21e937a94366c7d43691992fa5fcd977e2f57b855fd8228d72bdcf2b`  
		Last Modified: Wed, 22 Jun 2022 20:51:52 GMT  
		Size: 158.0 MB (158015595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12` - linux; 386

```console
$ docker pull mono@sha256:077ff268e88653929ca63f7c94b2e831ed47deda1898a7dab145be46bc43dca5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.1 MB (259079011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e4374dff0b027269b8b0431e17ebeb06e2a686d388a8c1592acc87d1a729552`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 00:40:01 GMT
ADD file:9aea7a35c215cdd778adec1dd5213973ef9b4830110e4550f2ead85679551ee5 in / 
# Sat, 28 May 2022 00:40:01 GMT
CMD ["bash"]
# Wed, 22 Jun 2022 21:09:07 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 22 Jun 2022 21:09:17 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jun 2022 21:09:41 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 22 Jun 2022 21:11:03 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:40837b3d848885c0b0c031d6d950b38e6a26962a5ee49704cb3ca2d2db535617`  
		Last Modified: Sat, 28 May 2022 00:47:36 GMT  
		Size: 27.8 MB (27799572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f5200b7ae28ef6430e06f086a32f10b738467f7b8d657b48c49d175705a2439`  
		Last Modified: Wed, 22 Jun 2022 21:11:47 GMT  
		Size: 2.8 MB (2789326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39fde061d95ef131491c0e1d327f4052f99ac1349bc834556e204012adc8392b`  
		Last Modified: Wed, 22 Jun 2022 21:11:56 GMT  
		Size: 68.6 MB (68586144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7134f7256858262305eb34494cf4e9b1fca7a8e3139732ec59ae0e26a5b5808`  
		Last Modified: Wed, 22 Jun 2022 21:12:45 GMT  
		Size: 159.9 MB (159903969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12` - linux; ppc64le

```console
$ docker pull mono@sha256:7eac0dfce15caa1b45ca234122e7853ce90c084da4661daafbce43c170cbfd73
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.2 MB (204236244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab1afeae8582e0f00846a4ec3004a268ac2997c3995b17a6f31c32addd8961e5`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 01:23:57 GMT
ADD file:a8c6c897bc64da424049ad04a354d123b0622abda1a56b2725f72de5e4569df8 in / 
# Sat, 28 May 2022 01:24:04 GMT
CMD ["bash"]
# Wed, 22 Jun 2022 22:32:51 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 22 Jun 2022 22:36:09 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jun 2022 22:39:29 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 22 Jun 2022 22:59:57 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:087d40850259bdcd3bee3d5d30d5a2070216727f72c1c9731b514ac3dbf7573e`  
		Last Modified: Sat, 28 May 2022 01:33:30 GMT  
		Size: 30.6 MB (30560238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbd0cf1c03bf6b16f117de84792baa6f69e374958138eb1f18c6cfb9dd43bbad`  
		Last Modified: Wed, 22 Jun 2022 23:09:45 GMT  
		Size: 2.9 MB (2893026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e43a06d332d2410820bebe341037d6c6dee278dbc6f235c702a6713f9e3dcab`  
		Last Modified: Wed, 22 Jun 2022 23:09:50 GMT  
		Size: 26.9 MB (26897354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd50f7a2e62c331e54ff9a3a987c99b7719f64428153fd4aff50ef0d6c661e3`  
		Last Modified: Wed, 22 Jun 2022 23:14:42 GMT  
		Size: 143.9 MB (143885626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.12-slim`

```console
$ docker pull mono@sha256:2a988c2c837506a6d94e5eb2c939cce53c86996a9474cb8fdfe9f580ad32cac1
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
$ docker pull mono@sha256:fa12e7083a98b6812cc29d29f0a085ea2f029c0e4670819a01fbb8a663faeb64
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.7 MB (94690413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61736b8ef52963f0ca986605f518457372d0c66f0a74040721c0e014a2119f80`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 01:20:43 GMT
ADD file:0513eda9512e010cb9459591b62e0c9d9319750923df091b64250ad6e98c2878 in / 
# Sat, 28 May 2022 01:20:43 GMT
CMD ["bash"]
# Wed, 22 Jun 2022 21:33:20 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 22 Jun 2022 21:33:29 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jun 2022 21:33:47 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:c1ad9731b2c7bf7fddea67f2f3f553515179a375c489e591e2372700fcaca766`  
		Last Modified: Sat, 28 May 2022 01:26:05 GMT  
		Size: 27.1 MB (27140144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36bdd50eb1bac9261e7d11ef7736774181be91ac4c30c02e1c1c4cc1c567a999`  
		Last Modified: Wed, 22 Jun 2022 21:35:25 GMT  
		Size: 2.8 MB (2777561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aba950124d67df356ccc1d947efdfd8cb5c8a7769434bc4057d371b5897b4d2e`  
		Last Modified: Wed, 22 Jun 2022 21:35:35 GMT  
		Size: 64.8 MB (64772708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:63988b42501e95210c718ff7135a1864484fbc220ec2ec6bf545a2227018fcac
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.9 MB (51861339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c8a27d1ba9bc597baeac26ffe42cbbdffae549aeaa642f7bd17e856d9a3f7df`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 02:04:06 GMT
ADD file:26e9ed6c41ec12bf5fd602b7f86b924d34537bbc82442f630763f9f6c48bf3b3 in / 
# Sat, 28 May 2022 02:04:07 GMT
CMD ["bash"]
# Wed, 22 Jun 2022 19:49:00 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 22 Jun 2022 19:49:28 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jun 2022 19:50:19 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:19389fd1100abdedaa775b43242838cdd2d5c8c3388643a7e52da2b7b4399c15`  
		Last Modified: Sat, 28 May 2022 02:20:06 GMT  
		Size: 24.9 MB (24890069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa92f2f021e75803ce535a7facb85567bc17614f5919ffd2ded82252e6d03d5e`  
		Last Modified: Wed, 22 Jun 2022 19:55:44 GMT  
		Size: 2.5 MB (2467777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:946e5a3fcfdd33b760be56e03b5bd597eb8df3d50ee8880f36418e4b23a50fd8`  
		Last Modified: Wed, 22 Jun 2022 19:56:01 GMT  
		Size: 24.5 MB (24503493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:cedb57185a1bf7814ec666fc9803c0151fa8c5b4d4c8825092defa4a67ce92a5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48904837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80c02c8e8e7adb45c0a2629edac2478b91fb970b7cd16d064ea6a269db94729e`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 01:00:54 GMT
ADD file:c89d47099a38749a424760d9c7d3a6e982089455ba9d04140db15ba9eb4cdda1 in / 
# Sat, 28 May 2022 01:00:55 GMT
CMD ["bash"]
# Wed, 22 Jun 2022 21:53:04 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 22 Jun 2022 21:53:30 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jun 2022 21:54:14 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:e41117292dc8c199b63ae1ec4485358841dbcba68dcbd13f379b66182efe832e`  
		Last Modified: Sat, 28 May 2022 01:16:58 GMT  
		Size: 22.7 MB (22748097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cea7b08703ed144c6d58b457cac40359088319d3ed62617dcbd6e3f36943b28a`  
		Last Modified: Wed, 22 Jun 2022 21:59:22 GMT  
		Size: 2.4 MB (2367003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c63834d12328a6bcb0b82fbfb83fef45b3596496346470249ba9c388730688a2`  
		Last Modified: Wed, 22 Jun 2022 21:59:38 GMT  
		Size: 23.8 MB (23789737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:349bfae18e0c38993d262c97c4e5dfcc08d672b0a775b8cebaacb2805bbb9469
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.9 MB (57888651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14037cb8b94bf65da4202f7a2f4b5bc9edd22cfe2a40b5712e6ff5260abbd44a`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 00:41:05 GMT
ADD file:d0e42d603f275c040783ec7b6c051200815492fc35b73110234dfcd584e6cdec in / 
# Sat, 28 May 2022 00:41:05 GMT
CMD ["bash"]
# Wed, 22 Jun 2022 20:48:48 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 22 Jun 2022 20:48:57 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jun 2022 20:49:12 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:4931fb8ba4223cb35034141162105ee5482122692b2931eb69eec912ce64606d`  
		Last Modified: Sat, 28 May 2022 00:48:26 GMT  
		Size: 25.9 MB (25914033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f06cddbf5d49ff334333bc51c02936695c616c52497d3284e91848de8085104a`  
		Last Modified: Wed, 22 Jun 2022 20:51:01 GMT  
		Size: 2.6 MB (2641202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:751c39f1c5edbe681c6c8ee877cb5e858b51e875ddf051ef6c2d8ef93b840da5`  
		Last Modified: Wed, 22 Jun 2022 20:51:06 GMT  
		Size: 29.3 MB (29333416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12-slim` - linux; 386

```console
$ docker pull mono@sha256:3bb47bffd3d5b15f72dd10214baaaf4c2d7552cadec24c67c4ccccd6966ce009
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.2 MB (99175042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebd693bbe60229e9032cc548cbd25cbbd5c053d51845c4e7896959ccf6d068a1`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 00:40:01 GMT
ADD file:9aea7a35c215cdd778adec1dd5213973ef9b4830110e4550f2ead85679551ee5 in / 
# Sat, 28 May 2022 00:40:01 GMT
CMD ["bash"]
# Wed, 22 Jun 2022 21:09:07 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 22 Jun 2022 21:09:17 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jun 2022 21:09:41 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:40837b3d848885c0b0c031d6d950b38e6a26962a5ee49704cb3ca2d2db535617`  
		Last Modified: Sat, 28 May 2022 00:47:36 GMT  
		Size: 27.8 MB (27799572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f5200b7ae28ef6430e06f086a32f10b738467f7b8d657b48c49d175705a2439`  
		Last Modified: Wed, 22 Jun 2022 21:11:47 GMT  
		Size: 2.8 MB (2789326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39fde061d95ef131491c0e1d327f4052f99ac1349bc834556e204012adc8392b`  
		Last Modified: Wed, 22 Jun 2022 21:11:56 GMT  
		Size: 68.6 MB (68586144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:1ac19e6ece7d6fe0e4208ee88f5941537dd1a5d3394da83468d2bc55527d7378
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.4 MB (60350618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:065d97346ce613488eb9e0d9d912aead0311ee56f9c1eed798b5de4ec6472d1a`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 01:23:57 GMT
ADD file:a8c6c897bc64da424049ad04a354d123b0622abda1a56b2725f72de5e4569df8 in / 
# Sat, 28 May 2022 01:24:04 GMT
CMD ["bash"]
# Wed, 22 Jun 2022 22:32:51 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 22 Jun 2022 22:36:09 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jun 2022 22:39:29 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:087d40850259bdcd3bee3d5d30d5a2070216727f72c1c9731b514ac3dbf7573e`  
		Last Modified: Sat, 28 May 2022 01:33:30 GMT  
		Size: 30.6 MB (30560238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbd0cf1c03bf6b16f117de84792baa6f69e374958138eb1f18c6cfb9dd43bbad`  
		Last Modified: Wed, 22 Jun 2022 23:09:45 GMT  
		Size: 2.9 MB (2893026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e43a06d332d2410820bebe341037d6c6dee278dbc6f235c702a6713f9e3dcab`  
		Last Modified: Wed, 22 Jun 2022 23:09:50 GMT  
		Size: 26.9 MB (26897354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.12.0`

```console
$ docker pull mono@sha256:bcc2d36c88898cdd62a9e18f97ad863c44b30fb74a23585549808f7db216a717
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
$ docker pull mono@sha256:c868b8345d1b67f672c229bfb330f5e1ba58cfcc33a6d46a9375b39bc25d5bda
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.4 MB (254416410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4527a2fc6d1eab132a7db6cd829d5d905553a692c5680c5e233251932e8d2e3`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 01:20:43 GMT
ADD file:0513eda9512e010cb9459591b62e0c9d9319750923df091b64250ad6e98c2878 in / 
# Sat, 28 May 2022 01:20:43 GMT
CMD ["bash"]
# Wed, 22 Jun 2022 21:33:20 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 22 Jun 2022 21:33:29 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jun 2022 21:33:47 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 22 Jun 2022 21:34:59 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:c1ad9731b2c7bf7fddea67f2f3f553515179a375c489e591e2372700fcaca766`  
		Last Modified: Sat, 28 May 2022 01:26:05 GMT  
		Size: 27.1 MB (27140144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36bdd50eb1bac9261e7d11ef7736774181be91ac4c30c02e1c1c4cc1c567a999`  
		Last Modified: Wed, 22 Jun 2022 21:35:25 GMT  
		Size: 2.8 MB (2777561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aba950124d67df356ccc1d947efdfd8cb5c8a7769434bc4057d371b5897b4d2e`  
		Last Modified: Wed, 22 Jun 2022 21:35:35 GMT  
		Size: 64.8 MB (64772708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e06195ea08da0f4b76c03b1a888e1149b4b7456b3137a22534ed08d300e9e9ff`  
		Last Modified: Wed, 22 Jun 2022 21:36:17 GMT  
		Size: 159.7 MB (159725997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0` - linux; arm variant v5

```console
$ docker pull mono@sha256:eecb4ce0a2143b972b80438d19719eedce94ea3734c1209e616f2c7b1752e397
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.9 MB (192881569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc56159c8ddff3dd73991b2b958f358c0e6b8a5dc881ad7a926c459b4be00031`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 02:04:06 GMT
ADD file:26e9ed6c41ec12bf5fd602b7f86b924d34537bbc82442f630763f9f6c48bf3b3 in / 
# Sat, 28 May 2022 02:04:07 GMT
CMD ["bash"]
# Wed, 22 Jun 2022 19:49:00 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 22 Jun 2022 19:49:28 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jun 2022 19:50:19 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 22 Jun 2022 19:54:03 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:19389fd1100abdedaa775b43242838cdd2d5c8c3388643a7e52da2b7b4399c15`  
		Last Modified: Sat, 28 May 2022 02:20:06 GMT  
		Size: 24.9 MB (24890069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa92f2f021e75803ce535a7facb85567bc17614f5919ffd2ded82252e6d03d5e`  
		Last Modified: Wed, 22 Jun 2022 19:55:44 GMT  
		Size: 2.5 MB (2467777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:946e5a3fcfdd33b760be56e03b5bd597eb8df3d50ee8880f36418e4b23a50fd8`  
		Last Modified: Wed, 22 Jun 2022 19:56:01 GMT  
		Size: 24.5 MB (24503493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e7dcb1cf8147d4ccbe01cb4986ecc814d15c96443e421575b6ec406ce783e98`  
		Last Modified: Wed, 22 Jun 2022 19:58:06 GMT  
		Size: 141.0 MB (141020230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0` - linux; arm variant v7

```console
$ docker pull mono@sha256:8e6e34d1a1ae5a2de0c439461a0cb502b0cd22220cd6774b90cb62fa5e240a92
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.8 MB (188782584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8afa747cef2c601df113d6bbdf74340305ece2fa03b83f9dd709d64178ced488`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 01:00:54 GMT
ADD file:c89d47099a38749a424760d9c7d3a6e982089455ba9d04140db15ba9eb4cdda1 in / 
# Sat, 28 May 2022 01:00:55 GMT
CMD ["bash"]
# Wed, 22 Jun 2022 21:53:04 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 22 Jun 2022 21:53:30 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jun 2022 21:54:14 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 22 Jun 2022 21:57:44 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:e41117292dc8c199b63ae1ec4485358841dbcba68dcbd13f379b66182efe832e`  
		Last Modified: Sat, 28 May 2022 01:16:58 GMT  
		Size: 22.7 MB (22748097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cea7b08703ed144c6d58b457cac40359088319d3ed62617dcbd6e3f36943b28a`  
		Last Modified: Wed, 22 Jun 2022 21:59:22 GMT  
		Size: 2.4 MB (2367003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c63834d12328a6bcb0b82fbfb83fef45b3596496346470249ba9c388730688a2`  
		Last Modified: Wed, 22 Jun 2022 21:59:38 GMT  
		Size: 23.8 MB (23789737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ec56912b25995fca9411a168ff99dcefede44b3e81975719b204e56f0a02971`  
		Last Modified: Wed, 22 Jun 2022 22:01:46 GMT  
		Size: 139.9 MB (139877747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:4654e59232e7dc6ba687050cc60cb311e0ef287235be7e88b313d69fa8565a7b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.9 MB (215904246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cae1924b9544a9ab52d1b2e09daec6d8f9560b3cbccb8f50929cc577b91940ab`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 00:41:05 GMT
ADD file:d0e42d603f275c040783ec7b6c051200815492fc35b73110234dfcd584e6cdec in / 
# Sat, 28 May 2022 00:41:05 GMT
CMD ["bash"]
# Wed, 22 Jun 2022 20:48:48 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 22 Jun 2022 20:48:57 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jun 2022 20:49:12 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 22 Jun 2022 20:50:20 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:4931fb8ba4223cb35034141162105ee5482122692b2931eb69eec912ce64606d`  
		Last Modified: Sat, 28 May 2022 00:48:26 GMT  
		Size: 25.9 MB (25914033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f06cddbf5d49ff334333bc51c02936695c616c52497d3284e91848de8085104a`  
		Last Modified: Wed, 22 Jun 2022 20:51:01 GMT  
		Size: 2.6 MB (2641202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:751c39f1c5edbe681c6c8ee877cb5e858b51e875ddf051ef6c2d8ef93b840da5`  
		Last Modified: Wed, 22 Jun 2022 20:51:06 GMT  
		Size: 29.3 MB (29333416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fcd120a21e937a94366c7d43691992fa5fcd977e2f57b855fd8228d72bdcf2b`  
		Last Modified: Wed, 22 Jun 2022 20:51:52 GMT  
		Size: 158.0 MB (158015595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0` - linux; 386

```console
$ docker pull mono@sha256:077ff268e88653929ca63f7c94b2e831ed47deda1898a7dab145be46bc43dca5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.1 MB (259079011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e4374dff0b027269b8b0431e17ebeb06e2a686d388a8c1592acc87d1a729552`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 00:40:01 GMT
ADD file:9aea7a35c215cdd778adec1dd5213973ef9b4830110e4550f2ead85679551ee5 in / 
# Sat, 28 May 2022 00:40:01 GMT
CMD ["bash"]
# Wed, 22 Jun 2022 21:09:07 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 22 Jun 2022 21:09:17 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jun 2022 21:09:41 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 22 Jun 2022 21:11:03 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:40837b3d848885c0b0c031d6d950b38e6a26962a5ee49704cb3ca2d2db535617`  
		Last Modified: Sat, 28 May 2022 00:47:36 GMT  
		Size: 27.8 MB (27799572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f5200b7ae28ef6430e06f086a32f10b738467f7b8d657b48c49d175705a2439`  
		Last Modified: Wed, 22 Jun 2022 21:11:47 GMT  
		Size: 2.8 MB (2789326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39fde061d95ef131491c0e1d327f4052f99ac1349bc834556e204012adc8392b`  
		Last Modified: Wed, 22 Jun 2022 21:11:56 GMT  
		Size: 68.6 MB (68586144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7134f7256858262305eb34494cf4e9b1fca7a8e3139732ec59ae0e26a5b5808`  
		Last Modified: Wed, 22 Jun 2022 21:12:45 GMT  
		Size: 159.9 MB (159903969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0` - linux; ppc64le

```console
$ docker pull mono@sha256:7eac0dfce15caa1b45ca234122e7853ce90c084da4661daafbce43c170cbfd73
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.2 MB (204236244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab1afeae8582e0f00846a4ec3004a268ac2997c3995b17a6f31c32addd8961e5`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 01:23:57 GMT
ADD file:a8c6c897bc64da424049ad04a354d123b0622abda1a56b2725f72de5e4569df8 in / 
# Sat, 28 May 2022 01:24:04 GMT
CMD ["bash"]
# Wed, 22 Jun 2022 22:32:51 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 22 Jun 2022 22:36:09 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jun 2022 22:39:29 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 22 Jun 2022 22:59:57 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:087d40850259bdcd3bee3d5d30d5a2070216727f72c1c9731b514ac3dbf7573e`  
		Last Modified: Sat, 28 May 2022 01:33:30 GMT  
		Size: 30.6 MB (30560238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbd0cf1c03bf6b16f117de84792baa6f69e374958138eb1f18c6cfb9dd43bbad`  
		Last Modified: Wed, 22 Jun 2022 23:09:45 GMT  
		Size: 2.9 MB (2893026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e43a06d332d2410820bebe341037d6c6dee278dbc6f235c702a6713f9e3dcab`  
		Last Modified: Wed, 22 Jun 2022 23:09:50 GMT  
		Size: 26.9 MB (26897354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd50f7a2e62c331e54ff9a3a987c99b7719f64428153fd4aff50ef0d6c661e3`  
		Last Modified: Wed, 22 Jun 2022 23:14:42 GMT  
		Size: 143.9 MB (143885626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.12.0-slim`

```console
$ docker pull mono@sha256:2a988c2c837506a6d94e5eb2c939cce53c86996a9474cb8fdfe9f580ad32cac1
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
$ docker pull mono@sha256:fa12e7083a98b6812cc29d29f0a085ea2f029c0e4670819a01fbb8a663faeb64
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.7 MB (94690413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61736b8ef52963f0ca986605f518457372d0c66f0a74040721c0e014a2119f80`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 01:20:43 GMT
ADD file:0513eda9512e010cb9459591b62e0c9d9319750923df091b64250ad6e98c2878 in / 
# Sat, 28 May 2022 01:20:43 GMT
CMD ["bash"]
# Wed, 22 Jun 2022 21:33:20 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 22 Jun 2022 21:33:29 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jun 2022 21:33:47 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:c1ad9731b2c7bf7fddea67f2f3f553515179a375c489e591e2372700fcaca766`  
		Last Modified: Sat, 28 May 2022 01:26:05 GMT  
		Size: 27.1 MB (27140144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36bdd50eb1bac9261e7d11ef7736774181be91ac4c30c02e1c1c4cc1c567a999`  
		Last Modified: Wed, 22 Jun 2022 21:35:25 GMT  
		Size: 2.8 MB (2777561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aba950124d67df356ccc1d947efdfd8cb5c8a7769434bc4057d371b5897b4d2e`  
		Last Modified: Wed, 22 Jun 2022 21:35:35 GMT  
		Size: 64.8 MB (64772708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:63988b42501e95210c718ff7135a1864484fbc220ec2ec6bf545a2227018fcac
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.9 MB (51861339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c8a27d1ba9bc597baeac26ffe42cbbdffae549aeaa642f7bd17e856d9a3f7df`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 02:04:06 GMT
ADD file:26e9ed6c41ec12bf5fd602b7f86b924d34537bbc82442f630763f9f6c48bf3b3 in / 
# Sat, 28 May 2022 02:04:07 GMT
CMD ["bash"]
# Wed, 22 Jun 2022 19:49:00 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 22 Jun 2022 19:49:28 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jun 2022 19:50:19 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:19389fd1100abdedaa775b43242838cdd2d5c8c3388643a7e52da2b7b4399c15`  
		Last Modified: Sat, 28 May 2022 02:20:06 GMT  
		Size: 24.9 MB (24890069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa92f2f021e75803ce535a7facb85567bc17614f5919ffd2ded82252e6d03d5e`  
		Last Modified: Wed, 22 Jun 2022 19:55:44 GMT  
		Size: 2.5 MB (2467777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:946e5a3fcfdd33b760be56e03b5bd597eb8df3d50ee8880f36418e4b23a50fd8`  
		Last Modified: Wed, 22 Jun 2022 19:56:01 GMT  
		Size: 24.5 MB (24503493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:cedb57185a1bf7814ec666fc9803c0151fa8c5b4d4c8825092defa4a67ce92a5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48904837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80c02c8e8e7adb45c0a2629edac2478b91fb970b7cd16d064ea6a269db94729e`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 01:00:54 GMT
ADD file:c89d47099a38749a424760d9c7d3a6e982089455ba9d04140db15ba9eb4cdda1 in / 
# Sat, 28 May 2022 01:00:55 GMT
CMD ["bash"]
# Wed, 22 Jun 2022 21:53:04 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 22 Jun 2022 21:53:30 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jun 2022 21:54:14 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:e41117292dc8c199b63ae1ec4485358841dbcba68dcbd13f379b66182efe832e`  
		Last Modified: Sat, 28 May 2022 01:16:58 GMT  
		Size: 22.7 MB (22748097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cea7b08703ed144c6d58b457cac40359088319d3ed62617dcbd6e3f36943b28a`  
		Last Modified: Wed, 22 Jun 2022 21:59:22 GMT  
		Size: 2.4 MB (2367003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c63834d12328a6bcb0b82fbfb83fef45b3596496346470249ba9c388730688a2`  
		Last Modified: Wed, 22 Jun 2022 21:59:38 GMT  
		Size: 23.8 MB (23789737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:349bfae18e0c38993d262c97c4e5dfcc08d672b0a775b8cebaacb2805bbb9469
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.9 MB (57888651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14037cb8b94bf65da4202f7a2f4b5bc9edd22cfe2a40b5712e6ff5260abbd44a`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 00:41:05 GMT
ADD file:d0e42d603f275c040783ec7b6c051200815492fc35b73110234dfcd584e6cdec in / 
# Sat, 28 May 2022 00:41:05 GMT
CMD ["bash"]
# Wed, 22 Jun 2022 20:48:48 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 22 Jun 2022 20:48:57 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jun 2022 20:49:12 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:4931fb8ba4223cb35034141162105ee5482122692b2931eb69eec912ce64606d`  
		Last Modified: Sat, 28 May 2022 00:48:26 GMT  
		Size: 25.9 MB (25914033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f06cddbf5d49ff334333bc51c02936695c616c52497d3284e91848de8085104a`  
		Last Modified: Wed, 22 Jun 2022 20:51:01 GMT  
		Size: 2.6 MB (2641202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:751c39f1c5edbe681c6c8ee877cb5e858b51e875ddf051ef6c2d8ef93b840da5`  
		Last Modified: Wed, 22 Jun 2022 20:51:06 GMT  
		Size: 29.3 MB (29333416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0-slim` - linux; 386

```console
$ docker pull mono@sha256:3bb47bffd3d5b15f72dd10214baaaf4c2d7552cadec24c67c4ccccd6966ce009
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.2 MB (99175042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebd693bbe60229e9032cc548cbd25cbbd5c053d51845c4e7896959ccf6d068a1`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 00:40:01 GMT
ADD file:9aea7a35c215cdd778adec1dd5213973ef9b4830110e4550f2ead85679551ee5 in / 
# Sat, 28 May 2022 00:40:01 GMT
CMD ["bash"]
# Wed, 22 Jun 2022 21:09:07 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 22 Jun 2022 21:09:17 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jun 2022 21:09:41 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:40837b3d848885c0b0c031d6d950b38e6a26962a5ee49704cb3ca2d2db535617`  
		Last Modified: Sat, 28 May 2022 00:47:36 GMT  
		Size: 27.8 MB (27799572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f5200b7ae28ef6430e06f086a32f10b738467f7b8d657b48c49d175705a2439`  
		Last Modified: Wed, 22 Jun 2022 21:11:47 GMT  
		Size: 2.8 MB (2789326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39fde061d95ef131491c0e1d327f4052f99ac1349bc834556e204012adc8392b`  
		Last Modified: Wed, 22 Jun 2022 21:11:56 GMT  
		Size: 68.6 MB (68586144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:1ac19e6ece7d6fe0e4208ee88f5941537dd1a5d3394da83468d2bc55527d7378
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.4 MB (60350618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:065d97346ce613488eb9e0d9d912aead0311ee56f9c1eed798b5de4ec6472d1a`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 01:23:57 GMT
ADD file:a8c6c897bc64da424049ad04a354d123b0622abda1a56b2725f72de5e4569df8 in / 
# Sat, 28 May 2022 01:24:04 GMT
CMD ["bash"]
# Wed, 22 Jun 2022 22:32:51 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 22 Jun 2022 22:36:09 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jun 2022 22:39:29 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:087d40850259bdcd3bee3d5d30d5a2070216727f72c1c9731b514ac3dbf7573e`  
		Last Modified: Sat, 28 May 2022 01:33:30 GMT  
		Size: 30.6 MB (30560238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbd0cf1c03bf6b16f117de84792baa6f69e374958138eb1f18c6cfb9dd43bbad`  
		Last Modified: Wed, 22 Jun 2022 23:09:45 GMT  
		Size: 2.9 MB (2893026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e43a06d332d2410820bebe341037d6c6dee278dbc6f235c702a6713f9e3dcab`  
		Last Modified: Wed, 22 Jun 2022 23:09:50 GMT  
		Size: 26.9 MB (26897354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.12.0.182`

```console
$ docker pull mono@sha256:bcc2d36c88898cdd62a9e18f97ad863c44b30fb74a23585549808f7db216a717
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
$ docker pull mono@sha256:c868b8345d1b67f672c229bfb330f5e1ba58cfcc33a6d46a9375b39bc25d5bda
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.4 MB (254416410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4527a2fc6d1eab132a7db6cd829d5d905553a692c5680c5e233251932e8d2e3`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 01:20:43 GMT
ADD file:0513eda9512e010cb9459591b62e0c9d9319750923df091b64250ad6e98c2878 in / 
# Sat, 28 May 2022 01:20:43 GMT
CMD ["bash"]
# Wed, 22 Jun 2022 21:33:20 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 22 Jun 2022 21:33:29 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jun 2022 21:33:47 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 22 Jun 2022 21:34:59 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:c1ad9731b2c7bf7fddea67f2f3f553515179a375c489e591e2372700fcaca766`  
		Last Modified: Sat, 28 May 2022 01:26:05 GMT  
		Size: 27.1 MB (27140144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36bdd50eb1bac9261e7d11ef7736774181be91ac4c30c02e1c1c4cc1c567a999`  
		Last Modified: Wed, 22 Jun 2022 21:35:25 GMT  
		Size: 2.8 MB (2777561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aba950124d67df356ccc1d947efdfd8cb5c8a7769434bc4057d371b5897b4d2e`  
		Last Modified: Wed, 22 Jun 2022 21:35:35 GMT  
		Size: 64.8 MB (64772708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e06195ea08da0f4b76c03b1a888e1149b4b7456b3137a22534ed08d300e9e9ff`  
		Last Modified: Wed, 22 Jun 2022 21:36:17 GMT  
		Size: 159.7 MB (159725997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0.182` - linux; arm variant v5

```console
$ docker pull mono@sha256:eecb4ce0a2143b972b80438d19719eedce94ea3734c1209e616f2c7b1752e397
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.9 MB (192881569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc56159c8ddff3dd73991b2b958f358c0e6b8a5dc881ad7a926c459b4be00031`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 02:04:06 GMT
ADD file:26e9ed6c41ec12bf5fd602b7f86b924d34537bbc82442f630763f9f6c48bf3b3 in / 
# Sat, 28 May 2022 02:04:07 GMT
CMD ["bash"]
# Wed, 22 Jun 2022 19:49:00 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 22 Jun 2022 19:49:28 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jun 2022 19:50:19 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 22 Jun 2022 19:54:03 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:19389fd1100abdedaa775b43242838cdd2d5c8c3388643a7e52da2b7b4399c15`  
		Last Modified: Sat, 28 May 2022 02:20:06 GMT  
		Size: 24.9 MB (24890069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa92f2f021e75803ce535a7facb85567bc17614f5919ffd2ded82252e6d03d5e`  
		Last Modified: Wed, 22 Jun 2022 19:55:44 GMT  
		Size: 2.5 MB (2467777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:946e5a3fcfdd33b760be56e03b5bd597eb8df3d50ee8880f36418e4b23a50fd8`  
		Last Modified: Wed, 22 Jun 2022 19:56:01 GMT  
		Size: 24.5 MB (24503493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e7dcb1cf8147d4ccbe01cb4986ecc814d15c96443e421575b6ec406ce783e98`  
		Last Modified: Wed, 22 Jun 2022 19:58:06 GMT  
		Size: 141.0 MB (141020230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0.182` - linux; arm variant v7

```console
$ docker pull mono@sha256:8e6e34d1a1ae5a2de0c439461a0cb502b0cd22220cd6774b90cb62fa5e240a92
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.8 MB (188782584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8afa747cef2c601df113d6bbdf74340305ece2fa03b83f9dd709d64178ced488`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 01:00:54 GMT
ADD file:c89d47099a38749a424760d9c7d3a6e982089455ba9d04140db15ba9eb4cdda1 in / 
# Sat, 28 May 2022 01:00:55 GMT
CMD ["bash"]
# Wed, 22 Jun 2022 21:53:04 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 22 Jun 2022 21:53:30 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jun 2022 21:54:14 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 22 Jun 2022 21:57:44 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:e41117292dc8c199b63ae1ec4485358841dbcba68dcbd13f379b66182efe832e`  
		Last Modified: Sat, 28 May 2022 01:16:58 GMT  
		Size: 22.7 MB (22748097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cea7b08703ed144c6d58b457cac40359088319d3ed62617dcbd6e3f36943b28a`  
		Last Modified: Wed, 22 Jun 2022 21:59:22 GMT  
		Size: 2.4 MB (2367003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c63834d12328a6bcb0b82fbfb83fef45b3596496346470249ba9c388730688a2`  
		Last Modified: Wed, 22 Jun 2022 21:59:38 GMT  
		Size: 23.8 MB (23789737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ec56912b25995fca9411a168ff99dcefede44b3e81975719b204e56f0a02971`  
		Last Modified: Wed, 22 Jun 2022 22:01:46 GMT  
		Size: 139.9 MB (139877747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0.182` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:4654e59232e7dc6ba687050cc60cb311e0ef287235be7e88b313d69fa8565a7b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.9 MB (215904246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cae1924b9544a9ab52d1b2e09daec6d8f9560b3cbccb8f50929cc577b91940ab`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 00:41:05 GMT
ADD file:d0e42d603f275c040783ec7b6c051200815492fc35b73110234dfcd584e6cdec in / 
# Sat, 28 May 2022 00:41:05 GMT
CMD ["bash"]
# Wed, 22 Jun 2022 20:48:48 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 22 Jun 2022 20:48:57 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jun 2022 20:49:12 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 22 Jun 2022 20:50:20 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:4931fb8ba4223cb35034141162105ee5482122692b2931eb69eec912ce64606d`  
		Last Modified: Sat, 28 May 2022 00:48:26 GMT  
		Size: 25.9 MB (25914033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f06cddbf5d49ff334333bc51c02936695c616c52497d3284e91848de8085104a`  
		Last Modified: Wed, 22 Jun 2022 20:51:01 GMT  
		Size: 2.6 MB (2641202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:751c39f1c5edbe681c6c8ee877cb5e858b51e875ddf051ef6c2d8ef93b840da5`  
		Last Modified: Wed, 22 Jun 2022 20:51:06 GMT  
		Size: 29.3 MB (29333416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fcd120a21e937a94366c7d43691992fa5fcd977e2f57b855fd8228d72bdcf2b`  
		Last Modified: Wed, 22 Jun 2022 20:51:52 GMT  
		Size: 158.0 MB (158015595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0.182` - linux; 386

```console
$ docker pull mono@sha256:077ff268e88653929ca63f7c94b2e831ed47deda1898a7dab145be46bc43dca5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.1 MB (259079011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e4374dff0b027269b8b0431e17ebeb06e2a686d388a8c1592acc87d1a729552`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 00:40:01 GMT
ADD file:9aea7a35c215cdd778adec1dd5213973ef9b4830110e4550f2ead85679551ee5 in / 
# Sat, 28 May 2022 00:40:01 GMT
CMD ["bash"]
# Wed, 22 Jun 2022 21:09:07 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 22 Jun 2022 21:09:17 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jun 2022 21:09:41 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 22 Jun 2022 21:11:03 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:40837b3d848885c0b0c031d6d950b38e6a26962a5ee49704cb3ca2d2db535617`  
		Last Modified: Sat, 28 May 2022 00:47:36 GMT  
		Size: 27.8 MB (27799572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f5200b7ae28ef6430e06f086a32f10b738467f7b8d657b48c49d175705a2439`  
		Last Modified: Wed, 22 Jun 2022 21:11:47 GMT  
		Size: 2.8 MB (2789326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39fde061d95ef131491c0e1d327f4052f99ac1349bc834556e204012adc8392b`  
		Last Modified: Wed, 22 Jun 2022 21:11:56 GMT  
		Size: 68.6 MB (68586144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7134f7256858262305eb34494cf4e9b1fca7a8e3139732ec59ae0e26a5b5808`  
		Last Modified: Wed, 22 Jun 2022 21:12:45 GMT  
		Size: 159.9 MB (159903969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0.182` - linux; ppc64le

```console
$ docker pull mono@sha256:7eac0dfce15caa1b45ca234122e7853ce90c084da4661daafbce43c170cbfd73
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.2 MB (204236244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab1afeae8582e0f00846a4ec3004a268ac2997c3995b17a6f31c32addd8961e5`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 01:23:57 GMT
ADD file:a8c6c897bc64da424049ad04a354d123b0622abda1a56b2725f72de5e4569df8 in / 
# Sat, 28 May 2022 01:24:04 GMT
CMD ["bash"]
# Wed, 22 Jun 2022 22:32:51 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 22 Jun 2022 22:36:09 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jun 2022 22:39:29 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 22 Jun 2022 22:59:57 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:087d40850259bdcd3bee3d5d30d5a2070216727f72c1c9731b514ac3dbf7573e`  
		Last Modified: Sat, 28 May 2022 01:33:30 GMT  
		Size: 30.6 MB (30560238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbd0cf1c03bf6b16f117de84792baa6f69e374958138eb1f18c6cfb9dd43bbad`  
		Last Modified: Wed, 22 Jun 2022 23:09:45 GMT  
		Size: 2.9 MB (2893026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e43a06d332d2410820bebe341037d6c6dee278dbc6f235c702a6713f9e3dcab`  
		Last Modified: Wed, 22 Jun 2022 23:09:50 GMT  
		Size: 26.9 MB (26897354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd50f7a2e62c331e54ff9a3a987c99b7719f64428153fd4aff50ef0d6c661e3`  
		Last Modified: Wed, 22 Jun 2022 23:14:42 GMT  
		Size: 143.9 MB (143885626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.12.0.182-slim`

```console
$ docker pull mono@sha256:2a988c2c837506a6d94e5eb2c939cce53c86996a9474cb8fdfe9f580ad32cac1
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
$ docker pull mono@sha256:fa12e7083a98b6812cc29d29f0a085ea2f029c0e4670819a01fbb8a663faeb64
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.7 MB (94690413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61736b8ef52963f0ca986605f518457372d0c66f0a74040721c0e014a2119f80`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 01:20:43 GMT
ADD file:0513eda9512e010cb9459591b62e0c9d9319750923df091b64250ad6e98c2878 in / 
# Sat, 28 May 2022 01:20:43 GMT
CMD ["bash"]
# Wed, 22 Jun 2022 21:33:20 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 22 Jun 2022 21:33:29 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jun 2022 21:33:47 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:c1ad9731b2c7bf7fddea67f2f3f553515179a375c489e591e2372700fcaca766`  
		Last Modified: Sat, 28 May 2022 01:26:05 GMT  
		Size: 27.1 MB (27140144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36bdd50eb1bac9261e7d11ef7736774181be91ac4c30c02e1c1c4cc1c567a999`  
		Last Modified: Wed, 22 Jun 2022 21:35:25 GMT  
		Size: 2.8 MB (2777561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aba950124d67df356ccc1d947efdfd8cb5c8a7769434bc4057d371b5897b4d2e`  
		Last Modified: Wed, 22 Jun 2022 21:35:35 GMT  
		Size: 64.8 MB (64772708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0.182-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:63988b42501e95210c718ff7135a1864484fbc220ec2ec6bf545a2227018fcac
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.9 MB (51861339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c8a27d1ba9bc597baeac26ffe42cbbdffae549aeaa642f7bd17e856d9a3f7df`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 02:04:06 GMT
ADD file:26e9ed6c41ec12bf5fd602b7f86b924d34537bbc82442f630763f9f6c48bf3b3 in / 
# Sat, 28 May 2022 02:04:07 GMT
CMD ["bash"]
# Wed, 22 Jun 2022 19:49:00 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 22 Jun 2022 19:49:28 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jun 2022 19:50:19 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:19389fd1100abdedaa775b43242838cdd2d5c8c3388643a7e52da2b7b4399c15`  
		Last Modified: Sat, 28 May 2022 02:20:06 GMT  
		Size: 24.9 MB (24890069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa92f2f021e75803ce535a7facb85567bc17614f5919ffd2ded82252e6d03d5e`  
		Last Modified: Wed, 22 Jun 2022 19:55:44 GMT  
		Size: 2.5 MB (2467777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:946e5a3fcfdd33b760be56e03b5bd597eb8df3d50ee8880f36418e4b23a50fd8`  
		Last Modified: Wed, 22 Jun 2022 19:56:01 GMT  
		Size: 24.5 MB (24503493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0.182-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:cedb57185a1bf7814ec666fc9803c0151fa8c5b4d4c8825092defa4a67ce92a5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48904837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80c02c8e8e7adb45c0a2629edac2478b91fb970b7cd16d064ea6a269db94729e`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 01:00:54 GMT
ADD file:c89d47099a38749a424760d9c7d3a6e982089455ba9d04140db15ba9eb4cdda1 in / 
# Sat, 28 May 2022 01:00:55 GMT
CMD ["bash"]
# Wed, 22 Jun 2022 21:53:04 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 22 Jun 2022 21:53:30 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jun 2022 21:54:14 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:e41117292dc8c199b63ae1ec4485358841dbcba68dcbd13f379b66182efe832e`  
		Last Modified: Sat, 28 May 2022 01:16:58 GMT  
		Size: 22.7 MB (22748097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cea7b08703ed144c6d58b457cac40359088319d3ed62617dcbd6e3f36943b28a`  
		Last Modified: Wed, 22 Jun 2022 21:59:22 GMT  
		Size: 2.4 MB (2367003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c63834d12328a6bcb0b82fbfb83fef45b3596496346470249ba9c388730688a2`  
		Last Modified: Wed, 22 Jun 2022 21:59:38 GMT  
		Size: 23.8 MB (23789737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0.182-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:349bfae18e0c38993d262c97c4e5dfcc08d672b0a775b8cebaacb2805bbb9469
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.9 MB (57888651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14037cb8b94bf65da4202f7a2f4b5bc9edd22cfe2a40b5712e6ff5260abbd44a`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 00:41:05 GMT
ADD file:d0e42d603f275c040783ec7b6c051200815492fc35b73110234dfcd584e6cdec in / 
# Sat, 28 May 2022 00:41:05 GMT
CMD ["bash"]
# Wed, 22 Jun 2022 20:48:48 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 22 Jun 2022 20:48:57 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jun 2022 20:49:12 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:4931fb8ba4223cb35034141162105ee5482122692b2931eb69eec912ce64606d`  
		Last Modified: Sat, 28 May 2022 00:48:26 GMT  
		Size: 25.9 MB (25914033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f06cddbf5d49ff334333bc51c02936695c616c52497d3284e91848de8085104a`  
		Last Modified: Wed, 22 Jun 2022 20:51:01 GMT  
		Size: 2.6 MB (2641202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:751c39f1c5edbe681c6c8ee877cb5e858b51e875ddf051ef6c2d8ef93b840da5`  
		Last Modified: Wed, 22 Jun 2022 20:51:06 GMT  
		Size: 29.3 MB (29333416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0.182-slim` - linux; 386

```console
$ docker pull mono@sha256:3bb47bffd3d5b15f72dd10214baaaf4c2d7552cadec24c67c4ccccd6966ce009
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.2 MB (99175042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebd693bbe60229e9032cc548cbd25cbbd5c053d51845c4e7896959ccf6d068a1`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 00:40:01 GMT
ADD file:9aea7a35c215cdd778adec1dd5213973ef9b4830110e4550f2ead85679551ee5 in / 
# Sat, 28 May 2022 00:40:01 GMT
CMD ["bash"]
# Wed, 22 Jun 2022 21:09:07 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 22 Jun 2022 21:09:17 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jun 2022 21:09:41 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:40837b3d848885c0b0c031d6d950b38e6a26962a5ee49704cb3ca2d2db535617`  
		Last Modified: Sat, 28 May 2022 00:47:36 GMT  
		Size: 27.8 MB (27799572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f5200b7ae28ef6430e06f086a32f10b738467f7b8d657b48c49d175705a2439`  
		Last Modified: Wed, 22 Jun 2022 21:11:47 GMT  
		Size: 2.8 MB (2789326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39fde061d95ef131491c0e1d327f4052f99ac1349bc834556e204012adc8392b`  
		Last Modified: Wed, 22 Jun 2022 21:11:56 GMT  
		Size: 68.6 MB (68586144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0.182-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:1ac19e6ece7d6fe0e4208ee88f5941537dd1a5d3394da83468d2bc55527d7378
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.4 MB (60350618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:065d97346ce613488eb9e0d9d912aead0311ee56f9c1eed798b5de4ec6472d1a`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 01:23:57 GMT
ADD file:a8c6c897bc64da424049ad04a354d123b0622abda1a56b2725f72de5e4569df8 in / 
# Sat, 28 May 2022 01:24:04 GMT
CMD ["bash"]
# Wed, 22 Jun 2022 22:32:51 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 22 Jun 2022 22:36:09 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jun 2022 22:39:29 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:087d40850259bdcd3bee3d5d30d5a2070216727f72c1c9731b514ac3dbf7573e`  
		Last Modified: Sat, 28 May 2022 01:33:30 GMT  
		Size: 30.6 MB (30560238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbd0cf1c03bf6b16f117de84792baa6f69e374958138eb1f18c6cfb9dd43bbad`  
		Last Modified: Wed, 22 Jun 2022 23:09:45 GMT  
		Size: 2.9 MB (2893026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e43a06d332d2410820bebe341037d6c6dee278dbc6f235c702a6713f9e3dcab`  
		Last Modified: Wed, 22 Jun 2022 23:09:50 GMT  
		Size: 26.9 MB (26897354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:latest`

```console
$ docker pull mono@sha256:bcc2d36c88898cdd62a9e18f97ad863c44b30fb74a23585549808f7db216a717
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
$ docker pull mono@sha256:c868b8345d1b67f672c229bfb330f5e1ba58cfcc33a6d46a9375b39bc25d5bda
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.4 MB (254416410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4527a2fc6d1eab132a7db6cd829d5d905553a692c5680c5e233251932e8d2e3`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 01:20:43 GMT
ADD file:0513eda9512e010cb9459591b62e0c9d9319750923df091b64250ad6e98c2878 in / 
# Sat, 28 May 2022 01:20:43 GMT
CMD ["bash"]
# Wed, 22 Jun 2022 21:33:20 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 22 Jun 2022 21:33:29 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jun 2022 21:33:47 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 22 Jun 2022 21:34:59 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:c1ad9731b2c7bf7fddea67f2f3f553515179a375c489e591e2372700fcaca766`  
		Last Modified: Sat, 28 May 2022 01:26:05 GMT  
		Size: 27.1 MB (27140144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36bdd50eb1bac9261e7d11ef7736774181be91ac4c30c02e1c1c4cc1c567a999`  
		Last Modified: Wed, 22 Jun 2022 21:35:25 GMT  
		Size: 2.8 MB (2777561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aba950124d67df356ccc1d947efdfd8cb5c8a7769434bc4057d371b5897b4d2e`  
		Last Modified: Wed, 22 Jun 2022 21:35:35 GMT  
		Size: 64.8 MB (64772708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e06195ea08da0f4b76c03b1a888e1149b4b7456b3137a22534ed08d300e9e9ff`  
		Last Modified: Wed, 22 Jun 2022 21:36:17 GMT  
		Size: 159.7 MB (159725997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:latest` - linux; arm variant v5

```console
$ docker pull mono@sha256:eecb4ce0a2143b972b80438d19719eedce94ea3734c1209e616f2c7b1752e397
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.9 MB (192881569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc56159c8ddff3dd73991b2b958f358c0e6b8a5dc881ad7a926c459b4be00031`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 02:04:06 GMT
ADD file:26e9ed6c41ec12bf5fd602b7f86b924d34537bbc82442f630763f9f6c48bf3b3 in / 
# Sat, 28 May 2022 02:04:07 GMT
CMD ["bash"]
# Wed, 22 Jun 2022 19:49:00 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 22 Jun 2022 19:49:28 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jun 2022 19:50:19 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 22 Jun 2022 19:54:03 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:19389fd1100abdedaa775b43242838cdd2d5c8c3388643a7e52da2b7b4399c15`  
		Last Modified: Sat, 28 May 2022 02:20:06 GMT  
		Size: 24.9 MB (24890069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa92f2f021e75803ce535a7facb85567bc17614f5919ffd2ded82252e6d03d5e`  
		Last Modified: Wed, 22 Jun 2022 19:55:44 GMT  
		Size: 2.5 MB (2467777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:946e5a3fcfdd33b760be56e03b5bd597eb8df3d50ee8880f36418e4b23a50fd8`  
		Last Modified: Wed, 22 Jun 2022 19:56:01 GMT  
		Size: 24.5 MB (24503493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e7dcb1cf8147d4ccbe01cb4986ecc814d15c96443e421575b6ec406ce783e98`  
		Last Modified: Wed, 22 Jun 2022 19:58:06 GMT  
		Size: 141.0 MB (141020230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:latest` - linux; arm variant v7

```console
$ docker pull mono@sha256:8e6e34d1a1ae5a2de0c439461a0cb502b0cd22220cd6774b90cb62fa5e240a92
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.8 MB (188782584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8afa747cef2c601df113d6bbdf74340305ece2fa03b83f9dd709d64178ced488`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 01:00:54 GMT
ADD file:c89d47099a38749a424760d9c7d3a6e982089455ba9d04140db15ba9eb4cdda1 in / 
# Sat, 28 May 2022 01:00:55 GMT
CMD ["bash"]
# Wed, 22 Jun 2022 21:53:04 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 22 Jun 2022 21:53:30 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jun 2022 21:54:14 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 22 Jun 2022 21:57:44 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:e41117292dc8c199b63ae1ec4485358841dbcba68dcbd13f379b66182efe832e`  
		Last Modified: Sat, 28 May 2022 01:16:58 GMT  
		Size: 22.7 MB (22748097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cea7b08703ed144c6d58b457cac40359088319d3ed62617dcbd6e3f36943b28a`  
		Last Modified: Wed, 22 Jun 2022 21:59:22 GMT  
		Size: 2.4 MB (2367003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c63834d12328a6bcb0b82fbfb83fef45b3596496346470249ba9c388730688a2`  
		Last Modified: Wed, 22 Jun 2022 21:59:38 GMT  
		Size: 23.8 MB (23789737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ec56912b25995fca9411a168ff99dcefede44b3e81975719b204e56f0a02971`  
		Last Modified: Wed, 22 Jun 2022 22:01:46 GMT  
		Size: 139.9 MB (139877747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:latest` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:4654e59232e7dc6ba687050cc60cb311e0ef287235be7e88b313d69fa8565a7b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.9 MB (215904246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cae1924b9544a9ab52d1b2e09daec6d8f9560b3cbccb8f50929cc577b91940ab`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 00:41:05 GMT
ADD file:d0e42d603f275c040783ec7b6c051200815492fc35b73110234dfcd584e6cdec in / 
# Sat, 28 May 2022 00:41:05 GMT
CMD ["bash"]
# Wed, 22 Jun 2022 20:48:48 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 22 Jun 2022 20:48:57 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jun 2022 20:49:12 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 22 Jun 2022 20:50:20 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:4931fb8ba4223cb35034141162105ee5482122692b2931eb69eec912ce64606d`  
		Last Modified: Sat, 28 May 2022 00:48:26 GMT  
		Size: 25.9 MB (25914033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f06cddbf5d49ff334333bc51c02936695c616c52497d3284e91848de8085104a`  
		Last Modified: Wed, 22 Jun 2022 20:51:01 GMT  
		Size: 2.6 MB (2641202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:751c39f1c5edbe681c6c8ee877cb5e858b51e875ddf051ef6c2d8ef93b840da5`  
		Last Modified: Wed, 22 Jun 2022 20:51:06 GMT  
		Size: 29.3 MB (29333416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fcd120a21e937a94366c7d43691992fa5fcd977e2f57b855fd8228d72bdcf2b`  
		Last Modified: Wed, 22 Jun 2022 20:51:52 GMT  
		Size: 158.0 MB (158015595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:latest` - linux; 386

```console
$ docker pull mono@sha256:077ff268e88653929ca63f7c94b2e831ed47deda1898a7dab145be46bc43dca5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.1 MB (259079011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e4374dff0b027269b8b0431e17ebeb06e2a686d388a8c1592acc87d1a729552`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 00:40:01 GMT
ADD file:9aea7a35c215cdd778adec1dd5213973ef9b4830110e4550f2ead85679551ee5 in / 
# Sat, 28 May 2022 00:40:01 GMT
CMD ["bash"]
# Wed, 22 Jun 2022 21:09:07 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 22 Jun 2022 21:09:17 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jun 2022 21:09:41 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 22 Jun 2022 21:11:03 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:40837b3d848885c0b0c031d6d950b38e6a26962a5ee49704cb3ca2d2db535617`  
		Last Modified: Sat, 28 May 2022 00:47:36 GMT  
		Size: 27.8 MB (27799572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f5200b7ae28ef6430e06f086a32f10b738467f7b8d657b48c49d175705a2439`  
		Last Modified: Wed, 22 Jun 2022 21:11:47 GMT  
		Size: 2.8 MB (2789326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39fde061d95ef131491c0e1d327f4052f99ac1349bc834556e204012adc8392b`  
		Last Modified: Wed, 22 Jun 2022 21:11:56 GMT  
		Size: 68.6 MB (68586144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7134f7256858262305eb34494cf4e9b1fca7a8e3139732ec59ae0e26a5b5808`  
		Last Modified: Wed, 22 Jun 2022 21:12:45 GMT  
		Size: 159.9 MB (159903969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:latest` - linux; ppc64le

```console
$ docker pull mono@sha256:7eac0dfce15caa1b45ca234122e7853ce90c084da4661daafbce43c170cbfd73
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.2 MB (204236244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab1afeae8582e0f00846a4ec3004a268ac2997c3995b17a6f31c32addd8961e5`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 01:23:57 GMT
ADD file:a8c6c897bc64da424049ad04a354d123b0622abda1a56b2725f72de5e4569df8 in / 
# Sat, 28 May 2022 01:24:04 GMT
CMD ["bash"]
# Wed, 22 Jun 2022 22:32:51 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 22 Jun 2022 22:36:09 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jun 2022 22:39:29 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 22 Jun 2022 22:59:57 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:087d40850259bdcd3bee3d5d30d5a2070216727f72c1c9731b514ac3dbf7573e`  
		Last Modified: Sat, 28 May 2022 01:33:30 GMT  
		Size: 30.6 MB (30560238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbd0cf1c03bf6b16f117de84792baa6f69e374958138eb1f18c6cfb9dd43bbad`  
		Last Modified: Wed, 22 Jun 2022 23:09:45 GMT  
		Size: 2.9 MB (2893026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e43a06d332d2410820bebe341037d6c6dee278dbc6f235c702a6713f9e3dcab`  
		Last Modified: Wed, 22 Jun 2022 23:09:50 GMT  
		Size: 26.9 MB (26897354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd50f7a2e62c331e54ff9a3a987c99b7719f64428153fd4aff50ef0d6c661e3`  
		Last Modified: Wed, 22 Jun 2022 23:14:42 GMT  
		Size: 143.9 MB (143885626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:slim`

```console
$ docker pull mono@sha256:2a988c2c837506a6d94e5eb2c939cce53c86996a9474cb8fdfe9f580ad32cac1
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
$ docker pull mono@sha256:fa12e7083a98b6812cc29d29f0a085ea2f029c0e4670819a01fbb8a663faeb64
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.7 MB (94690413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61736b8ef52963f0ca986605f518457372d0c66f0a74040721c0e014a2119f80`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 01:20:43 GMT
ADD file:0513eda9512e010cb9459591b62e0c9d9319750923df091b64250ad6e98c2878 in / 
# Sat, 28 May 2022 01:20:43 GMT
CMD ["bash"]
# Wed, 22 Jun 2022 21:33:20 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 22 Jun 2022 21:33:29 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jun 2022 21:33:47 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:c1ad9731b2c7bf7fddea67f2f3f553515179a375c489e591e2372700fcaca766`  
		Last Modified: Sat, 28 May 2022 01:26:05 GMT  
		Size: 27.1 MB (27140144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36bdd50eb1bac9261e7d11ef7736774181be91ac4c30c02e1c1c4cc1c567a999`  
		Last Modified: Wed, 22 Jun 2022 21:35:25 GMT  
		Size: 2.8 MB (2777561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aba950124d67df356ccc1d947efdfd8cb5c8a7769434bc4057d371b5897b4d2e`  
		Last Modified: Wed, 22 Jun 2022 21:35:35 GMT  
		Size: 64.8 MB (64772708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:63988b42501e95210c718ff7135a1864484fbc220ec2ec6bf545a2227018fcac
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.9 MB (51861339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c8a27d1ba9bc597baeac26ffe42cbbdffae549aeaa642f7bd17e856d9a3f7df`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 02:04:06 GMT
ADD file:26e9ed6c41ec12bf5fd602b7f86b924d34537bbc82442f630763f9f6c48bf3b3 in / 
# Sat, 28 May 2022 02:04:07 GMT
CMD ["bash"]
# Wed, 22 Jun 2022 19:49:00 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 22 Jun 2022 19:49:28 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jun 2022 19:50:19 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:19389fd1100abdedaa775b43242838cdd2d5c8c3388643a7e52da2b7b4399c15`  
		Last Modified: Sat, 28 May 2022 02:20:06 GMT  
		Size: 24.9 MB (24890069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa92f2f021e75803ce535a7facb85567bc17614f5919ffd2ded82252e6d03d5e`  
		Last Modified: Wed, 22 Jun 2022 19:55:44 GMT  
		Size: 2.5 MB (2467777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:946e5a3fcfdd33b760be56e03b5bd597eb8df3d50ee8880f36418e4b23a50fd8`  
		Last Modified: Wed, 22 Jun 2022 19:56:01 GMT  
		Size: 24.5 MB (24503493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:cedb57185a1bf7814ec666fc9803c0151fa8c5b4d4c8825092defa4a67ce92a5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48904837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80c02c8e8e7adb45c0a2629edac2478b91fb970b7cd16d064ea6a269db94729e`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 01:00:54 GMT
ADD file:c89d47099a38749a424760d9c7d3a6e982089455ba9d04140db15ba9eb4cdda1 in / 
# Sat, 28 May 2022 01:00:55 GMT
CMD ["bash"]
# Wed, 22 Jun 2022 21:53:04 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 22 Jun 2022 21:53:30 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jun 2022 21:54:14 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:e41117292dc8c199b63ae1ec4485358841dbcba68dcbd13f379b66182efe832e`  
		Last Modified: Sat, 28 May 2022 01:16:58 GMT  
		Size: 22.7 MB (22748097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cea7b08703ed144c6d58b457cac40359088319d3ed62617dcbd6e3f36943b28a`  
		Last Modified: Wed, 22 Jun 2022 21:59:22 GMT  
		Size: 2.4 MB (2367003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c63834d12328a6bcb0b82fbfb83fef45b3596496346470249ba9c388730688a2`  
		Last Modified: Wed, 22 Jun 2022 21:59:38 GMT  
		Size: 23.8 MB (23789737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:349bfae18e0c38993d262c97c4e5dfcc08d672b0a775b8cebaacb2805bbb9469
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.9 MB (57888651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14037cb8b94bf65da4202f7a2f4b5bc9edd22cfe2a40b5712e6ff5260abbd44a`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 00:41:05 GMT
ADD file:d0e42d603f275c040783ec7b6c051200815492fc35b73110234dfcd584e6cdec in / 
# Sat, 28 May 2022 00:41:05 GMT
CMD ["bash"]
# Wed, 22 Jun 2022 20:48:48 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 22 Jun 2022 20:48:57 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jun 2022 20:49:12 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:4931fb8ba4223cb35034141162105ee5482122692b2931eb69eec912ce64606d`  
		Last Modified: Sat, 28 May 2022 00:48:26 GMT  
		Size: 25.9 MB (25914033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f06cddbf5d49ff334333bc51c02936695c616c52497d3284e91848de8085104a`  
		Last Modified: Wed, 22 Jun 2022 20:51:01 GMT  
		Size: 2.6 MB (2641202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:751c39f1c5edbe681c6c8ee877cb5e858b51e875ddf051ef6c2d8ef93b840da5`  
		Last Modified: Wed, 22 Jun 2022 20:51:06 GMT  
		Size: 29.3 MB (29333416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:slim` - linux; 386

```console
$ docker pull mono@sha256:3bb47bffd3d5b15f72dd10214baaaf4c2d7552cadec24c67c4ccccd6966ce009
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.2 MB (99175042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebd693bbe60229e9032cc548cbd25cbbd5c053d51845c4e7896959ccf6d068a1`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 00:40:01 GMT
ADD file:9aea7a35c215cdd778adec1dd5213973ef9b4830110e4550f2ead85679551ee5 in / 
# Sat, 28 May 2022 00:40:01 GMT
CMD ["bash"]
# Wed, 22 Jun 2022 21:09:07 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 22 Jun 2022 21:09:17 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jun 2022 21:09:41 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:40837b3d848885c0b0c031d6d950b38e6a26962a5ee49704cb3ca2d2db535617`  
		Last Modified: Sat, 28 May 2022 00:47:36 GMT  
		Size: 27.8 MB (27799572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f5200b7ae28ef6430e06f086a32f10b738467f7b8d657b48c49d175705a2439`  
		Last Modified: Wed, 22 Jun 2022 21:11:47 GMT  
		Size: 2.8 MB (2789326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39fde061d95ef131491c0e1d327f4052f99ac1349bc834556e204012adc8392b`  
		Last Modified: Wed, 22 Jun 2022 21:11:56 GMT  
		Size: 68.6 MB (68586144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:slim` - linux; ppc64le

```console
$ docker pull mono@sha256:1ac19e6ece7d6fe0e4208ee88f5941537dd1a5d3394da83468d2bc55527d7378
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.4 MB (60350618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:065d97346ce613488eb9e0d9d912aead0311ee56f9c1eed798b5de4ec6472d1a`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 01:23:57 GMT
ADD file:a8c6c897bc64da424049ad04a354d123b0622abda1a56b2725f72de5e4569df8 in / 
# Sat, 28 May 2022 01:24:04 GMT
CMD ["bash"]
# Wed, 22 Jun 2022 22:32:51 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 22 Jun 2022 22:36:09 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jun 2022 22:39:29 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:087d40850259bdcd3bee3d5d30d5a2070216727f72c1c9731b514ac3dbf7573e`  
		Last Modified: Sat, 28 May 2022 01:33:30 GMT  
		Size: 30.6 MB (30560238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbd0cf1c03bf6b16f117de84792baa6f69e374958138eb1f18c6cfb9dd43bbad`  
		Last Modified: Wed, 22 Jun 2022 23:09:45 GMT  
		Size: 2.9 MB (2893026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e43a06d332d2410820bebe341037d6c6dee278dbc6f235c702a6713f9e3dcab`  
		Last Modified: Wed, 22 Jun 2022 23:09:50 GMT  
		Size: 26.9 MB (26897354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
