## `mono:latest`

```console
$ docker pull mono@sha256:fff51756a3f0b773cc17f3738a9685a9db8807c92c3c8cf3dc479ef963949f0a
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
$ docker pull mono@sha256:d39c8c6482df4412d445f13e8fdff7593e9d1cb82ce48238be0dbf52378ede32
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.9 MB (235926166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3808870ff18d02c3dfc54505d0085f5f4d8c5502e9718f2844d43354eb351fcb`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Mar 2021 15:20:59 GMT
ADD file:b2085f4b0a7cb0e5754874c712254e5cd941062b27b8d7ed2080520196b91597 in / 
# Fri, 26 Mar 2021 15:20:59 GMT
CMD ["bash"]
# Sat, 27 Mar 2021 06:23:09 GMT
ENV MONO_VERSION=6.12.0.107
# Sat, 27 Mar 2021 06:23:19 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 27 Mar 2021 06:23:50 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 27 Mar 2021 06:30:35 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:ac2522cc72690febc428fb46fb39a4efc5e0a721c3ad15d9992b01515f2fad1a`  
		Last Modified: Fri, 26 Mar 2021 15:27:47 GMT  
		Size: 27.1 MB (27100996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ec5055bd72daa5d7f6173b255cdb410ef66b1ea9cadbcd38c1870f8482a495c`  
		Last Modified: Sat, 27 Mar 2021 06:37:34 GMT  
		Size: 256.0 KB (256010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c932c33d3ede1f17ad9dc4f702a85d8f1d9d7b3ea1266b6e1c0e787c971ad2f`  
		Last Modified: Sat, 27 Mar 2021 06:37:47 GMT  
		Size: 67.1 MB (67128677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11100088d6507123f2ea359c621ef79f11dcfcbe2d3c3fce0cdbf28715f027ee`  
		Last Modified: Sat, 27 Mar 2021 06:39:01 GMT  
		Size: 141.4 MB (141440483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:latest` - linux; arm variant v5

```console
$ docker pull mono@sha256:c1018cc74bfac980315c3d606d6614e31099f0715fc1939fe75c17ac72e7fdf8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.8 MB (191787840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75659769146021e6b9ed2ebdbb8b250a55bd699b06e904f0f902a936c41807db`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 21:51:08 GMT
ADD file:779165b34b3be18f6c24e448997bf6497e3b27ff72954fe3cdced0ebcc77b6b8 in / 
# Tue, 30 Mar 2021 21:51:11 GMT
CMD ["bash"]
# Tue, 30 Mar 2021 22:59:46 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 30 Mar 2021 23:00:07 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 30 Mar 2021 23:00:55 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 30 Mar 2021 23:05:14 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7cbaf854daf876ddd338771dec41777b0dfcad33c1fc8ea3512a0708333e4465`  
		Last Modified: Tue, 30 Mar 2021 21:58:44 GMT  
		Size: 24.9 MB (24873214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fecc1879253d988f851b426e45eab1f00dc37e06175a483a2947d82c87ca693a`  
		Last Modified: Tue, 30 Mar 2021 23:08:40 GMT  
		Size: 256.0 KB (255971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0e6c4a26fc503c88bc0ca6e466b49d45bffe4eff185334b88d266c3ff2fac5`  
		Last Modified: Tue, 30 Mar 2021 23:08:51 GMT  
		Size: 26.6 MB (26550096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d41835d228f7030fcede189a173bd594d51881369bd5413aadec2cd6caaf6b90`  
		Last Modified: Tue, 30 Mar 2021 23:10:16 GMT  
		Size: 140.1 MB (140108559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:latest` - linux; arm variant v7

```console
$ docker pull mono@sha256:37bed4aae0165bf8cdc2ec35cda4585aa3d45675d6210cc2b5e4a99b27a995d2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.7 MB (187672912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ba418b8af22818a8aaaa279b7b2f7808af5c9f847c1e94d8f9079ce48175839`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 23:08:38 GMT
ADD file:c1eeb99fc8ec483e175d4948a58d7f7b246b0d6b887f435a5fef07ef43699f76 in / 
# Tue, 30 Mar 2021 23:08:41 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 02:09:19 GMT
ENV MONO_VERSION=6.12.0.107
# Wed, 31 Mar 2021 02:09:39 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 31 Mar 2021 02:10:22 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 31 Mar 2021 02:14:21 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:ee0a2cc24f2963b99b1d30dc2613f196b7c9e38337cf99332d6c4efe07f01ef2`  
		Last Modified: Tue, 30 Mar 2021 23:16:25 GMT  
		Size: 22.7 MB (22739814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db2630b9e89b3f8e8bf5cf459714f0533e6965dd6f7a15c681f983fd753a5052`  
		Last Modified: Wed, 31 Mar 2021 02:17:26 GMT  
		Size: 256.0 KB (256007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:688600d68f090a392c73014c7e4218a813575f2ab38e51dbe586c894b269087d`  
		Last Modified: Wed, 31 Mar 2021 02:17:36 GMT  
		Size: 25.7 MB (25738177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c2c49c3ba5fae015dc4d96f60186f4f4130581809c6f9b54c601500bc7876cb`  
		Last Modified: Wed, 31 Mar 2021 02:18:55 GMT  
		Size: 138.9 MB (138938914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:latest` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:ab7191405acfc4ead53f78b16701d311de07615307bfb304bdfbaba1981d3bf9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.5 MB (214513849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9dd6ff96d37bcb9f3bc1790e37b1d6343f0cfb5b1ed6830cfec063f2fa59e53`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 21:47:15 GMT
ADD file:a9b57ded2400fc7f60ea40e5ccdd3e9bf0f72acfcc47223ceb66b4fa16955059 in / 
# Tue, 30 Mar 2021 21:47:16 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 00:39:21 GMT
ENV MONO_VERSION=6.12.0.107
# Wed, 31 Mar 2021 00:39:40 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 31 Mar 2021 00:40:21 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 31 Mar 2021 00:44:02 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:6fcf2156bc23db75595b822b865fbc962ed6f4521dec8cae509e66742a6a5ad3`  
		Last Modified: Tue, 30 Mar 2021 21:54:27 GMT  
		Size: 25.9 MB (25904513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9580211237e340484647d3b7247615a7af051f85cfd9b3f5682bc81b0ad81bf1`  
		Last Modified: Wed, 31 Mar 2021 00:47:06 GMT  
		Size: 256.0 KB (255973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b84925b1302919cd20a82a541f5db57fa566b54d5cdc0f88d267859471e0495`  
		Last Modified: Wed, 31 Mar 2021 00:47:13 GMT  
		Size: 31.8 MB (31769562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b7a09d57266a1dda9f6e7aea520280baf520a95c3afc2c94fd5caafcee3499d`  
		Last Modified: Wed, 31 Mar 2021 00:48:45 GMT  
		Size: 156.6 MB (156583801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:latest` - linux; 386

```console
$ docker pull mono@sha256:f71ffa9e2a24c11ebd07053eecfe0fb8f43fbabeaecedf9bfc77c7d2cd8b7be5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.7 MB (241743217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b45e707d5b2754a3784dfd3b60f01aa8ac01f96336d4185936572cd82ff537ca`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 21:39:48 GMT
ADD file:d11c47560c0a88a83a3a0ce5af82fc17a07075e877293e4f922f126959810ea3 in / 
# Tue, 30 Mar 2021 21:39:49 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 01:00:01 GMT
ENV MONO_VERSION=6.12.0.107
# Wed, 31 Mar 2021 01:00:13 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 31 Mar 2021 01:01:00 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 31 Mar 2021 01:04:07 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:548dde0830bd6b881c0c068db5a4e39aa720d2a0c5ac3897296a023dda7b3391`  
		Last Modified: Tue, 30 Mar 2021 21:46:41 GMT  
		Size: 27.8 MB (27788996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c98ead88653c863870e7a39eb99edc7de4d043f96c4e0929a8b9b0a9fcb8ae6`  
		Last Modified: Wed, 31 Mar 2021 01:07:58 GMT  
		Size: 256.0 KB (255958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a71b5743d08a8b002bb14a919acbb40e11d6f112d1bc1be653046a2e08a28c9d`  
		Last Modified: Wed, 31 Mar 2021 01:08:14 GMT  
		Size: 71.2 MB (71152861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cff0459dd9be36d8cb55c9982a60ab9750af9f4a3ac029dcae263faaaf7307fd`  
		Last Modified: Wed, 31 Mar 2021 01:09:44 GMT  
		Size: 142.5 MB (142545402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:latest` - linux; ppc64le

```console
$ docker pull mono@sha256:ff186505b33ab4d3e14cf3746009665de2e4391896fea8c1a4b37fba6eeca8a2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.4 MB (203364926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cbf1769a9e52186775e25fa85c26c601e6ed2496aa50dc27aae5ab42bc29d07`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Mar 2021 15:14:22 GMT
ADD file:feb26657639018f8f43408e43e8ecec7e84632f33b42d5521241b842b58747d5 in / 
# Fri, 26 Mar 2021 15:14:28 GMT
CMD ["bash"]
# Sat, 27 Mar 2021 05:44:07 GMT
ENV MONO_VERSION=6.12.0.107
# Sat, 27 Mar 2021 05:45:15 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 27 Mar 2021 05:47:01 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 27 Mar 2021 05:55:09 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:035681ea37d9aab4545aa2211af3bf79addea316f71afde84412406734ef8a85`  
		Last Modified: Fri, 26 Mar 2021 15:22:05 GMT  
		Size: 30.5 MB (30525677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e0e9e31ca7180e13cb07afe4514fe1e6230ef35b16ea365fc88d74cfc58c444`  
		Last Modified: Sat, 27 Mar 2021 06:04:27 GMT  
		Size: 256.1 KB (256150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31398d223c853e2e82c08cb3043f63528f4526d86b2c735c88e856bd63329f35`  
		Last Modified: Sat, 27 Mar 2021 06:04:34 GMT  
		Size: 29.4 MB (29358106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8fd5f596d595bb436c6f8cecdf693f245d4c9d7ae2830139ec6bd1be17f60fc`  
		Last Modified: Sat, 27 Mar 2021 06:05:43 GMT  
		Size: 143.2 MB (143224993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
