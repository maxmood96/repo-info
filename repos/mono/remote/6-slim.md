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
