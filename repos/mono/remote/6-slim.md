## `mono:6-slim`

```console
$ docker pull mono@sha256:9d4ba66e353e699a1e0d2970e87b39e26cd619d3103cab57e29968c1a62c0c1d
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
$ docker pull mono@sha256:cdecd1e409a3bf015b2df7cab751b32aa1912942800c38c26dbbda077bd24a1d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.7 MB (94680497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:179c410963b2d950b30018aa2f7198d4bbf4750a44af79963bc2ec7eb619a78a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:21:02 GMT
ADD file:3c54ad257f2e04f7294ce879b884820cf4726c8e93ec548172825963e40c79ad in / 
# Wed, 17 Nov 2021 02:21:02 GMT
CMD ["bash"]
# Tue, 23 Nov 2021 22:35:14 GMT
ENV MONO_VERSION=6.12.0.122
# Tue, 23 Nov 2021 22:35:29 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 23 Nov 2021 22:35:48 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a10c77af261312e7c92bcc184f2d1726175ff7f142e44b01c5779cd79348b9fd`  
		Last Modified: Wed, 17 Nov 2021 02:26:31 GMT  
		Size: 27.2 MB (27153675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:290db4dba8dd1a22feca175d2300b4ca8dd16fe86ecc6022a566329a5b654ecf`  
		Last Modified: Tue, 23 Nov 2021 22:48:37 GMT  
		Size: 2.8 MB (2766933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbb78a53a304279c9bb401cfd5979e972f8fc1e746e9d36fc42525cd0676e372`  
		Last Modified: Tue, 23 Nov 2021 22:48:50 GMT  
		Size: 64.8 MB (64759889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:56e40b4d67adf3a932be68db6867706afb08420aa4ec4d1ce823c62f6369ca0a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51842060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76c279d60b298986449ea01c00551166b76185c559f47d494efc568cf54ea1c6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:51:39 GMT
ADD file:e580d4d2066301375327ea51dd8db3af956e5a465495bf09d69d6deec9b0bfae in / 
# Wed, 17 Nov 2021 02:51:40 GMT
CMD ["bash"]
# Tue, 23 Nov 2021 21:57:24 GMT
ENV MONO_VERSION=6.12.0.122
# Tue, 23 Nov 2021 21:57:55 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 23 Nov 2021 21:58:42 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:dba255a4b166bb02562ca152d0da236ba8f211de5bf9d79e35ee023b1fce203e`  
		Last Modified: Wed, 17 Nov 2021 03:07:41 GMT  
		Size: 24.9 MB (24886310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01af261a6c29946e34b32228d294c69a86ca06cdfd0b0cfafbb568e9fc6b57b3`  
		Last Modified: Tue, 23 Nov 2021 22:08:39 GMT  
		Size: 2.5 MB (2462561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c562f4f3fb32ceeded7f153ed48a677c98f4efaee9d19ed32a8fcfa7fe236b27`  
		Last Modified: Tue, 23 Nov 2021 22:08:52 GMT  
		Size: 24.5 MB (24493189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:abbc7a96a87a8fc3a75f3f9ee465f954103af6cb8caeeb2a58dcfa5775d9a5a6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48899010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:888f04b4468fa13c7dd2d4d3e6758e38cd6a1f2b8743d602ea8d6170470bc53f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:00:46 GMT
ADD file:4ac0de0d740f0c221cd4f912861a67009942fa5bdad24ac8b62c690dfa15024a in / 
# Wed, 17 Nov 2021 02:00:47 GMT
CMD ["bash"]
# Tue, 23 Nov 2021 22:28:21 GMT
ENV MONO_VERSION=6.12.0.122
# Tue, 23 Nov 2021 22:28:52 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 23 Nov 2021 22:29:35 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7bd9e64406c6f3044bd15f89c367f07ec4eaafb1035a5c3ee2f7b138be68017f`  
		Last Modified: Wed, 17 Nov 2021 02:16:39 GMT  
		Size: 22.8 MB (22754359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:049b685383367eaa00b28d290b7f521588cc2a6fddec236420129ec04830f7ad`  
		Last Modified: Tue, 23 Nov 2021 22:38:55 GMT  
		Size: 2.4 MB (2361954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d696071cf20a8d6e7031e1c8c4453e1fcbd73fbd07d0e299ab428402906f012c`  
		Last Modified: Tue, 23 Nov 2021 22:39:06 GMT  
		Size: 23.8 MB (23782697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:c8b6095166e5103eaa00541e4c8296a5082fc22f8b0c47f22b68524841854dda
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.9 MB (57875944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d2788a0d6a78feae4f3714b45819c05d06a535d1d2cd624e9cdb52386b96ff3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:40:44 GMT
ADD file:b7921dd77c7620d46a18a4b5952557620210bf7ad9de20fe8e695a371188122a in / 
# Wed, 17 Nov 2021 02:40:44 GMT
CMD ["bash"]
# Tue, 23 Nov 2021 21:51:44 GMT
ENV MONO_VERSION=6.12.0.122
# Tue, 23 Nov 2021 21:51:59 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 23 Nov 2021 21:52:15 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:8ccb9871ed7bebcea8889b08e06fe5bd0116711ca7b110429b987475bf4d40e8`  
		Last Modified: Wed, 17 Nov 2021 02:48:07 GMT  
		Size: 25.9 MB (25923117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9d1d375755ac6c8647c886eb68f427d617cb789ae0c98372e585311a5395aa0`  
		Last Modified: Tue, 23 Nov 2021 21:57:01 GMT  
		Size: 2.6 MB (2634589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a5575918894c723f49db7b67bad957b34f1f6b88828b67489943f4618f2fdc4`  
		Last Modified: Tue, 23 Nov 2021 21:57:05 GMT  
		Size: 29.3 MB (29318238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6-slim` - linux; 386

```console
$ docker pull mono@sha256:d5c218c6f846f064e3d68efb7e677d60a558d54067c13fe5a9554b1b6d2b8bdd
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.4 MB (99364574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2145d963dc4718d45ccb94e26a0153de7d7f1ee66964d3607401681ae010517d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:40:22 GMT
ADD file:2adea3474b7ebda2bf77361304ee3e6966a9118aafd8220b81c4027be1f4d583 in / 
# Wed, 17 Nov 2021 02:40:22 GMT
CMD ["bash"]
# Tue, 23 Nov 2021 21:42:03 GMT
ENV MONO_VERSION=6.12.0.122
# Tue, 23 Nov 2021 21:42:22 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 23 Nov 2021 21:42:48 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7af5c9e671306e395c50a515c7bbe33d6f418ea08535b01c884457f78114eb08`  
		Last Modified: Wed, 17 Nov 2021 02:48:49 GMT  
		Size: 27.8 MB (27804550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:178b44cff3441bdb1ada9b30fbb42c9e7143127e42b7e4715f38610b2d122927`  
		Last Modified: Tue, 23 Nov 2021 21:47:45 GMT  
		Size: 2.8 MB (2781502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b82f010a190c7a767fdbe0299862791645a573a4844487ee187efe7e6a34941`  
		Last Modified: Tue, 23 Nov 2021 21:47:59 GMT  
		Size: 68.8 MB (68778522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:7834ad815013a312211d9f24df0f88d7e3f04386d7c192b726662658029697f7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60162583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ee89c05071148752e8c61c25ab1424ba5b066d04b57a4f785fa443265cf2703`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Oct 2021 01:26:46 GMT
ADD file:5526880c6f19a4b4231a8b2bd7cfc625d116764c4918eff6f0b55f8c1eb38e1a in / 
# Tue, 12 Oct 2021 01:26:50 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 07:07:14 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 12 Oct 2021 07:08:29 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 12 Oct 2021 07:10:10 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:d69973af32573c07c8789c0f9c144a5c0b822a1e85b59db3ce9f8ebc489ce85d`  
		Last Modified: Tue, 12 Oct 2021 01:38:40 GMT  
		Size: 30.5 MB (30547197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:411a4d07ce6468d0126e5f9f0ad6098034f004bb482027b2349909c0ebc277d4`  
		Last Modified: Tue, 12 Oct 2021 07:31:06 GMT  
		Size: 256.1 KB (256142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa7805400cade2c3fda94906cc3502961f0a85bf26f07aeb6d74f4ba6866961b`  
		Last Modified: Tue, 12 Oct 2021 07:31:12 GMT  
		Size: 29.4 MB (29359244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
