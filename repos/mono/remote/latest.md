## `mono:latest`

```console
$ docker pull mono@sha256:36b0024d53395cd75d4e693959902b69526c696f9ffc411149faa6e5ad9c3d84
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
$ docker pull mono@sha256:d8256bf20739bb8f3aada1f7659b14fcd61e5f818338f99aa73ea3ef38ad1a4b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.1 MB (236126852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:716daf7ba794dd88525056449f625344562dc6a1ffa4fc9749aea72946db8d7b`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 01:20:43 GMT
ADD file:0513eda9512e010cb9459591b62e0c9d9319750923df091b64250ad6e98c2878 in / 
# Sat, 28 May 2022 01:20:43 GMT
CMD ["bash"]
# Sat, 28 May 2022 11:35:02 GMT
ENV MONO_VERSION=6.12.0.122
# Sat, 28 May 2022 11:35:10 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 May 2022 11:35:38 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 28 May 2022 11:41:13 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:c1ad9731b2c7bf7fddea67f2f3f553515179a375c489e591e2372700fcaca766`  
		Last Modified: Sat, 28 May 2022 01:26:05 GMT  
		Size: 27.1 MB (27140144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d83e829864ffe1d3e8e8013e50d81c17226075b248525f29649c9972933b833e`  
		Last Modified: Sat, 28 May 2022 11:47:12 GMT  
		Size: 2.8 MB (2777562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f4869636bcfc5c8d20940c1500acc491e8eb70ca73d6be03efccf597b60782f`  
		Last Modified: Sat, 28 May 2022 11:47:21 GMT  
		Size: 64.8 MB (64759878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96159769413f6bc94fad1d22a36a0d95982838d8365db9e79365ef688d4f06ae`  
		Last Modified: Sat, 28 May 2022 11:48:20 GMT  
		Size: 141.4 MB (141449268 bytes)  
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
$ docker pull mono@sha256:c866d649b5951c39167ebfb90c1db5a6d77191ee48448a24be2d0ec0d7295548
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.9 MB (187866518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d52ef30f17e2b7fd5591de5f947b64fb7b1a0c6e9d123e9e00ed0c708cf966c7`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 01:00:54 GMT
ADD file:c89d47099a38749a424760d9c7d3a6e982089455ba9d04140db15ba9eb4cdda1 in / 
# Sat, 28 May 2022 01:00:55 GMT
CMD ["bash"]
# Sun, 29 May 2022 07:04:32 GMT
ENV MONO_VERSION=6.12.0.122
# Sun, 29 May 2022 07:04:57 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sun, 29 May 2022 07:05:41 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sun, 29 May 2022 07:10:17 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:e41117292dc8c199b63ae1ec4485358841dbcba68dcbd13f379b66182efe832e`  
		Last Modified: Sat, 28 May 2022 01:16:58 GMT  
		Size: 22.7 MB (22748097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24697b1e682d4e680652caab3abaff53ea1eac1e024e05809f316d328e31963b`  
		Last Modified: Sun, 29 May 2022 07:15:20 GMT  
		Size: 2.4 MB (2366999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:137c5282e00af27ac584ec932a982fbd4ea0305214e0f4bcd56f886eb6c5f4d1`  
		Last Modified: Sun, 29 May 2022 07:15:29 GMT  
		Size: 23.8 MB (23782813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bf143d484b4488038ed3641bee7580d57271ad5d1cb4d6207f2e51e00c7ca49`  
		Last Modified: Sun, 29 May 2022 07:17:17 GMT  
		Size: 139.0 MB (138968609 bytes)  
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
$ docker pull mono@sha256:9678111e3730b2d76acfbb44fa36e8141e11309290555d49e3551af5f21885a7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.6 MB (203608343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27a258cc60099ba5bee36e5914ac4666c049a7b817331f5c5bce58e26fbb862d`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 01:23:57 GMT
ADD file:a8c6c897bc64da424049ad04a354d123b0622abda1a56b2725f72de5e4569df8 in / 
# Sat, 28 May 2022 01:24:04 GMT
CMD ["bash"]
# Sat, 28 May 2022 06:58:38 GMT
ENV MONO_VERSION=6.12.0.122
# Sat, 28 May 2022 07:00:20 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 May 2022 07:01:23 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 28 May 2022 07:10:27 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:087d40850259bdcd3bee3d5d30d5a2070216727f72c1c9731b514ac3dbf7573e`  
		Last Modified: Sat, 28 May 2022 01:33:30 GMT  
		Size: 30.6 MB (30560238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63e152c4faa2cb2bf2e15d23a8f5c7c862e9ddecfe4a0e5ac502b9e541865967`  
		Last Modified: Sat, 28 May 2022 07:18:30 GMT  
		Size: 2.9 MB (2892793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d34489a9a680aaa76b6e1402289bf21135f719d2d80a90211577e7b2c9462903`  
		Last Modified: Sat, 28 May 2022 07:18:35 GMT  
		Size: 26.9 MB (26873645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:209ea5f178496acebf329a804cc39a40f3e3ca6462f391d563bef6f4f71285f8`  
		Last Modified: Sat, 28 May 2022 07:19:45 GMT  
		Size: 143.3 MB (143281667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
