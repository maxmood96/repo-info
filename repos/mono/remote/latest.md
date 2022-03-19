## `mono:latest`

```console
$ docker pull mono@sha256:df7f4585bc2fa885bb0c461e0b18aea5c4e92b3317a3a294dae698c8fa7bfc62
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
$ docker pull mono@sha256:5e0b64a6e6bf6797a1bcd845b6d98d586e4348f33541f5effdad1a2bcba22bb2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.1 MB (236119102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:157578c1bb5e11b011d2de33f9302b67e62f97d0a09ceefa21804ab6d91144d7`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 04:04:26 GMT
ADD file:7f5787c324936e09d339f9426eec4a0120431e2a4b6ccb0db28b94d61f074ab2 in / 
# Thu, 17 Mar 2022 04:04:27 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 07:44:04 GMT
ENV MONO_VERSION=6.12.0.122
# Fri, 18 Mar 2022 07:44:45 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 18 Mar 2022 07:45:04 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Fri, 18 Mar 2022 07:52:15 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a4b007099961706d45bdb3eb0a3aab719916c3e36d6da7577b0c9060260e65f8`  
		Last Modified: Thu, 17 Mar 2022 04:10:54 GMT  
		Size: 27.2 MB (27153828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18785d1845f5dc614f27707490b6c71380904abc63e90f7949b3ecb05d0ba112`  
		Last Modified: Fri, 18 Mar 2022 08:00:08 GMT  
		Size: 2.8 MB (2766982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f29cf656fe8852554cdf541174b617b360b706faa7543418512200be4ec12595`  
		Last Modified: Fri, 18 Mar 2022 08:00:21 GMT  
		Size: 64.8 MB (64759765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c82c867b64975d6ae9a264681213e6d11b583fdebf1b64aa1007fac1f83d50e`  
		Last Modified: Fri, 18 Mar 2022 08:01:34 GMT  
		Size: 141.4 MB (141438527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:latest` - linux; arm variant v5

```console
$ docker pull mono@sha256:0e601f3b8afbee36f105bd380a94710da3d459d0a656fca2389de84e203edfd4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.9 MB (191932425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93faaf1bef796b49f0ebffe6b54a0639f777ebbda95f857da9e7c5e1dfa1378a`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 05:20:46 GMT
ADD file:4b7bce60b3e3455ba9b14c881ffa61187b9e56365fe4f275ee871e7c7e930fb9 in / 
# Thu, 17 Mar 2022 05:20:46 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 10:13:07 GMT
ENV MONO_VERSION=6.12.0.122
# Thu, 17 Mar 2022 10:13:53 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 17 Mar 2022 10:14:39 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 17 Mar 2022 10:19:32 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:f193682138b0c37054cb843ef2155a75706f248a369d454bf6444833f120aefc`  
		Last Modified: Thu, 17 Mar 2022 05:36:29 GMT  
		Size: 24.9 MB (24886195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b8842964e659b65aea8d54a049486cc3546f4fdcadce63992fd7f59864031fd`  
		Last Modified: Thu, 17 Mar 2022 10:24:22 GMT  
		Size: 2.5 MB (2462530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:121633eec53916213dcd2c006b09980543b3c594a15f99842dd7f038aa052152`  
		Last Modified: Thu, 17 Mar 2022 10:24:39 GMT  
		Size: 24.5 MB (24492565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4b85b5ece21b384dfe2c2b33b9b4c18c244e35d7434c2de03683a91fc1cd336`  
		Last Modified: Thu, 17 Mar 2022 10:27:05 GMT  
		Size: 140.1 MB (140091135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:latest` - linux; arm variant v7

```console
$ docker pull mono@sha256:31fbf9e91eb2101d0872397de4770b9b1686986f8e7b00bc592b22c943506949
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.9 MB (187852543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c01fcb1ec1e569073cabc744de90c68b0d94e4c1f8af64944407f93b43e78f55`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 09:32:07 GMT
ADD file:ca7a6b7c138de7fd85996719398396d0ed0f059d2e12b7f401cd460b64924e25 in / 
# Thu, 17 Mar 2022 09:32:08 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 04:12:25 GMT
ENV MONO_VERSION=6.12.0.122
# Sat, 19 Mar 2022 04:13:03 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 19 Mar 2022 04:13:46 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 19 Mar 2022 04:18:40 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:0b8f06901fc5e8a29999e260b4ada4ee1cc4415e5c1a16fb7bb21cc2ac995f72`  
		Last Modified: Thu, 17 Mar 2022 09:48:01 GMT  
		Size: 22.8 MB (22754389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:635212b9c70cb02c0aa647ee91ce1417572add8cdc66e2e2998bcb3a9ad605d8`  
		Last Modified: Sat, 19 Mar 2022 04:23:11 GMT  
		Size: 2.4 MB (2361883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54f2618a06f8bc8c9377958b480ea3d540f429435783b225a5bf6c0246baf3af`  
		Last Modified: Sat, 19 Mar 2022 04:23:27 GMT  
		Size: 23.8 MB (23782774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6dca04f966c2a1ed84c4d9c7746998b838c704076a805d58ae9c52598d67a4a`  
		Last Modified: Sat, 19 Mar 2022 04:25:59 GMT  
		Size: 139.0 MB (138953497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:latest` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:ef7a2ed6a3f244e9ee528665f48fd1a5c61de3251f8a53589108fbd013baa570
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.5 MB (214460692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:157824826295d6bfdb01f28bc27b6f4369428303484c8db9b2e120c4e2ea8cca`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 03:22:22 GMT
ADD file:1c7d8cedf5dc79c676acebde5252ecd3005088a9f29e5e6be547f659f41efb1f in / 
# Thu, 17 Mar 2022 03:22:22 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 23:11:49 GMT
ENV MONO_VERSION=6.12.0.122
# Thu, 17 Mar 2022 23:12:36 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 17 Mar 2022 23:12:51 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 17 Mar 2022 23:15:01 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:c9277cac12165646c33f028489f2a5be3f70745382f4385cd9ed12fcc8cec183`  
		Last Modified: Thu, 17 Mar 2022 03:29:27 GMT  
		Size: 25.9 MB (25923233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f27367e69cb7b3ff75b7196e775fe63ab5f00dd80e96eb8c7f273c70b9b4c9a`  
		Last Modified: Thu, 17 Mar 2022 23:16:51 GMT  
		Size: 2.6 MB (2634667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b014c14ab68a6b650aa566e7e891e4824d9d3f8c3410c1de318a4a2d5840ae4b`  
		Last Modified: Thu, 17 Mar 2022 23:16:56 GMT  
		Size: 29.3 MB (29318310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c662eb78bf51e4cd352ecf4b1e1e41ddad13bb89a9ed4194a6e2b6a3dcc0282`  
		Last Modified: Thu, 17 Mar 2022 23:17:59 GMT  
		Size: 156.6 MB (156584482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:latest` - linux; 386

```console
$ docker pull mono@sha256:999b460669ae89ec1d7d68067ab38929254d61d4a61c9d58f01076e410ec7a4a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.9 MB (241918263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76c9a6d9dd6e18299c4495a39e178822f6d53b63aaf291b2208e0ddac6c650c3`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 08:16:28 GMT
ADD file:39b40ec7bd2f4e691b74f0287e43ab64ef32f99953e606d9e4b72d058659209c in / 
# Thu, 17 Mar 2022 08:16:29 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 11:05:21 GMT
ENV MONO_VERSION=6.12.0.122
# Fri, 18 Mar 2022 11:06:11 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 18 Mar 2022 11:06:45 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Fri, 18 Mar 2022 11:09:47 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:cef703cf0f3e19a7a5f8b305254c02563c8b07f5b842bb99741d3a2fd136e9f0`  
		Last Modified: Thu, 17 Mar 2022 08:24:59 GMT  
		Size: 27.8 MB (27804570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b116ab65d31117c55d4fe2777444289c5652e79d071a0da41eeaadfb5b4550d`  
		Last Modified: Fri, 18 Mar 2022 11:13:11 GMT  
		Size: 2.8 MB (2781485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37baa24dfc5fcf9d672f9d79c7acf6358c6ecd3ea10d898868c5a492af2beca4`  
		Last Modified: Fri, 18 Mar 2022 11:13:29 GMT  
		Size: 68.8 MB (68778247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bff805e7a04c272dd5c6b507ca0cc3f7c121c34edd1709e4d1e0aed8e98605c0`  
		Last Modified: Fri, 18 Mar 2022 11:15:19 GMT  
		Size: 142.6 MB (142553961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:latest` - linux; ppc64le

```console
$ docker pull mono@sha256:39ff8e30c14539f61252cc048e85f52aac66223f9c5897ffa9325018e290fb54
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.6 MB (203590295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80be2528fb974e84c463e06af27e47cfcbe0b9f26252d5b5428ee0440e3caa4e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 11:19:08 GMT
ADD file:0af430b7759619d4d40ea316f823599879e4f3e0dfc8877bdee731020fb2620d in / 
# Thu, 17 Mar 2022 11:19:12 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 07:27:44 GMT
ENV MONO_VERSION=6.12.0.122
# Sat, 19 Mar 2022 07:29:35 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 19 Mar 2022 07:30:53 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 19 Mar 2022 07:39:43 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:303d92340e7868a8dc0fdad5d6c67a8a819a74a2bc47038b26339d5be6084bf4`  
		Last Modified: Thu, 17 Mar 2022 11:29:21 GMT  
		Size: 30.6 MB (30562350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d4316542fb6ac5647290bf8fc3273bd907ea2788aab876a425e0c683c30536e`  
		Last Modified: Sat, 19 Mar 2022 07:45:52 GMT  
		Size: 2.9 MB (2884710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bfc5ae0671a1f811f6836c48efb56e82b259a22cd98dc9df71508f7f3eae1d4`  
		Last Modified: Sat, 19 Mar 2022 07:45:56 GMT  
		Size: 26.9 MB (26873811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b714472ca1272d2460a4a64c207c6e7254f637463acf0a258422bd89c3585a9`  
		Last Modified: Sat, 19 Mar 2022 07:47:11 GMT  
		Size: 143.3 MB (143269424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
