<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `mono`

-	[`mono:5`](#mono5)
-	[`mono:5.20`](#mono520)
-	[`mono:5.20.1`](#mono5201)
-	[`mono:5.20.1.34`](#mono520134)
-	[`mono:5.20.1.34-slim`](#mono520134-slim)
-	[`mono:5.20.1-slim`](#mono5201-slim)
-	[`mono:5.20-slim`](#mono520-slim)
-	[`mono:5-slim`](#mono5-slim)
-	[`mono:6`](#mono6)
-	[`mono:6.6`](#mono66)
-	[`mono:6.6.0`](#mono660)
-	[`mono:6.6.0.161`](#mono660161)
-	[`mono:6.6.0.161-slim`](#mono660161-slim)
-	[`mono:6.6.0-slim`](#mono660-slim)
-	[`mono:6.6-slim`](#mono66-slim)
-	[`mono:6.8`](#mono68)
-	[`mono:6.8.0`](#mono680)
-	[`mono:6.8.0.96`](#mono68096)
-	[`mono:6.8.0.96-slim`](#mono68096-slim)
-	[`mono:6.8.0-slim`](#mono680-slim)
-	[`mono:6.8-slim`](#mono68-slim)
-	[`mono:6-slim`](#mono6-slim)
-	[`mono:latest`](#monolatest)
-	[`mono:slim`](#monoslim)

## `mono:5`

```console
$ docker pull mono@sha256:7c3897b79001e719cb00400400cf20520aa794779e0fee851c77db395d2bf901
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:5` - linux; amd64

```console
$ docker pull mono@sha256:0707bc551c8f0483db89e2698f140d4a3747ec5d05681d65f35c1c520cfc6d3e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.2 MB (218165276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:429edcd2234d98f14afc83c7cad33e40f41773a70f625fad37ab67baafdc39dd`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:23:35 GMT
ADD file:57b431451a292755d0f13673f5f3bea9f62aea36c7a1b59d34d7d200ba134fea in / 
# Tue, 09 Jun 2020 01:23:35 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 07:25:19 GMT
ENV MONO_VERSION=5.20.1.34
# Tue, 09 Jun 2020 07:25:31 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Jun 2020 07:25:58 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 09 Jun 2020 07:57:07 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7d2977b12acb33f192e3f20b7e15a467cc8f3f5124a15d975a6d4afe5fa3d258`  
		Last Modified: Tue, 09 Jun 2020 01:28:13 GMT  
		Size: 22.5 MB (22519600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3a96016cede2bbab34292fab9e759f8d6e76cdccf5e984c01f8efd90e6df05b`  
		Last Modified: Tue, 09 Jun 2020 07:58:27 GMT  
		Size: 244.5 KB (244463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05a6ab00376aa34c88796f85c2d808035931da42c558e6f9ff32907a9641b062`  
		Last Modified: Tue, 09 Jun 2020 07:58:43 GMT  
		Size: 55.4 MB (55407571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cebe820795cc4389f4a9bf096d8509cf6ec74165c3dca4d2a090a4d1d9c0e6e9`  
		Last Modified: Tue, 09 Jun 2020 08:01:09 GMT  
		Size: 140.0 MB (139993642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5` - linux; arm variant v5

```console
$ docker pull mono@sha256:f068482b1f0b192e200beffde233675842a2834082c65cd2f557491d078c271a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.8 MB (170828767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40422756bc15d6c9573b6c1a15eda0670c58fc8b0d4b5661a52ce9dfbd27cef5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 00:55:12 GMT
ADD file:0b9f2b88887a8060402a052c243c31641d9c217edcdb232c7b7a057cf5a70d66 in / 
# Wed, 22 Jul 2020 00:55:13 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 04:50:57 GMT
ENV MONO_VERSION=5.20.1.34
# Wed, 22 Jul 2020 04:51:29 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jul 2020 04:52:30 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 22 Jul 2020 05:02:14 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:319109fcb6fa9b08528c518426e7ce105aac7313066432efcea95f59ff6e6788`  
		Last Modified: Wed, 22 Jul 2020 01:03:27 GMT  
		Size: 21.2 MB (21189131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:214f724afb987f92ce9133d6327bf39c60bb2f5e639abe876e341a07f439d60e`  
		Last Modified: Wed, 22 Jul 2020 05:03:20 GMT  
		Size: 244.6 KB (244590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1738e5f6ebf3cc4543e52c88b7aa0fc6f9113fabde1e2980a289aafa5559d5b1`  
		Last Modified: Wed, 22 Jul 2020 05:03:29 GMT  
		Size: 24.2 MB (24150571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecdfd5f9763ca3e982c3a51730342a64a0697da0877ff7dad8f8c39ee2356001`  
		Last Modified: Wed, 22 Jul 2020 05:06:06 GMT  
		Size: 125.2 MB (125244475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5` - linux; arm variant v7

```console
$ docker pull mono@sha256:8328a11a821af5a680bdef017afccdd45d62b737555d11c9bd51c18c842a29cf
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.9 MB (166884235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8bc37db2a9a8b1caccb7c4ae6f82f9e8d05cb22f20e6763ef73dc275f8db3fb`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 01:33:30 GMT
ADD file:49b1a1b4f5c2201b0e23e29dca24c4f6ffc14620196c4bd77770952500c4bee1 in / 
# Wed, 22 Jul 2020 01:33:38 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 02:20:07 GMT
ENV MONO_VERSION=5.20.1.34
# Wed, 22 Jul 2020 02:20:49 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jul 2020 02:21:51 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 22 Jul 2020 02:32:01 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:cd38ad753522d120e27c5343b08f661ee3aebfe531d60102d7c624c16dba4d09`  
		Last Modified: Wed, 22 Jul 2020 01:44:24 GMT  
		Size: 19.3 MB (19298267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae6961338dbeec44b6e92646723bb59c030769220b24193c12f7827ce9ca826f`  
		Last Modified: Wed, 22 Jul 2020 02:33:13 GMT  
		Size: 244.6 KB (244556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:829fd514f3675f9e41ec1f1bc082852015f100014cc48e3b90e1b3023c34fa51`  
		Last Modified: Wed, 22 Jul 2020 02:33:22 GMT  
		Size: 23.5 MB (23453570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:396070eca2a0ddb7dbe1dd76c086672f187f84252665d73b6827e15ad8b0e2ed`  
		Last Modified: Wed, 22 Jul 2020 02:36:16 GMT  
		Size: 123.9 MB (123887842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:fd867443d6b38edb7b351a5f08f953107f530d3a0d9fc76a47ba6ab767ea21cc
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.7 MB (187697331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61776a2e50d7b9d3c215e6d87d93742c511f700b26c7d724654df01daafcf8a3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:54:49 GMT
ADD file:c85d28567b6123deb660b71c8b60d92378b5ba15ba5dcf495d9388817dc3aa44 in / 
# Tue, 09 Jun 2020 01:54:52 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 03:26:55 GMT
ENV MONO_VERSION=5.20.1.34
# Tue, 09 Jun 2020 03:27:13 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Jun 2020 03:27:54 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 09 Jun 2020 03:36:29 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:622dc742b82743ebf5607b215a65869096390ee41b0a61b5532f859fb94590b1`  
		Last Modified: Tue, 09 Jun 2020 02:00:28 GMT  
		Size: 20.4 MB (20375150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47cfdc0a506e196319f490a8bb5e0036dd589b207aa03c9571763b3ee8dea29f`  
		Last Modified: Tue, 09 Jun 2020 03:37:36 GMT  
		Size: 244.4 KB (244372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f6b08527e586e0f80506a226402a72b5cf43e106073bc06aa87862249894d0a`  
		Last Modified: Tue, 09 Jun 2020 03:37:45 GMT  
		Size: 28.0 MB (28049990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da477870a6058bd59427cbbc64d0b14a9abebe5cd6b910fa3ddfe36f278837e0`  
		Last Modified: Tue, 09 Jun 2020 03:40:26 GMT  
		Size: 139.0 MB (139027819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5` - linux; 386

```console
$ docker pull mono@sha256:1ea82d19a0f7414cfe3e98105b310e8d63f06f8f277f3848c6a884b92b77f05b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.7 MB (227671637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bc71aebacae50bcaa4b4f804a23f5f230ae27e5ec7fb10a0f1dd08c3d429ffd`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:42:33 GMT
ADD file:8ef252685ffefc58654053bf145c830928a2cf423a6c757180649df772f1523d in / 
# Tue, 09 Jun 2020 01:42:34 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 07:01:47 GMT
ENV MONO_VERSION=5.20.1.34
# Tue, 09 Jun 2020 07:02:01 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Jun 2020 07:02:35 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 09 Jun 2020 07:09:48 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:4ffbd6ec7974e514763a8d7d9fcf5e86e9440e2280e6e9561ea373b4bc50588e`  
		Last Modified: Tue, 09 Jun 2020 01:48:28 GMT  
		Size: 23.1 MB (23147892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79f35120db9bc30d6de494b0e58b8a74d62fe7a85cdc188357ea98ca2797e839`  
		Last Modified: Tue, 09 Jun 2020 07:11:10 GMT  
		Size: 244.5 KB (244478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d12cec6c246292b2edce2de333f893fefd5d9460042faa8e270bfde498b21612`  
		Last Modified: Tue, 09 Jun 2020 07:11:24 GMT  
		Size: 58.4 MB (58439805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13e5499fc7470d9d9b363a6494025ec430b6c28a85a563b44637506b9da2eca2`  
		Last Modified: Tue, 09 Jun 2020 07:13:37 GMT  
		Size: 145.8 MB (145839462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5` - linux; ppc64le

```console
$ docker pull mono@sha256:15c0c9e91312a3cbd18b060a447868b37ba4d2ef668c759b7e1c19f314bf9dd8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.2 MB (173185683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:065963fd30de2ed1faa7464809f20c63f66805ff3dad0867a93e21adeb544c22`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:25:38 GMT
ADD file:41ec53d65aa183c2835f73989c9e4922f818e59774811eaa6e7395e5a36d5eab in / 
# Tue, 09 Jun 2020 01:25:42 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 04:43:07 GMT
ENV MONO_VERSION=5.20.1.34
# Tue, 09 Jun 2020 04:44:25 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Jun 2020 04:45:52 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 09 Jun 2020 05:04:54 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a29e28607c9b96acae7ff89e56214e4339a87c59e40a6f030fa4cbcaab753f2c`  
		Last Modified: Tue, 09 Jun 2020 01:37:25 GMT  
		Size: 22.8 MB (22791269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21d9971248b8a3142c8d28700658bc11b1313694441bf51b7febefd26adddbe1`  
		Last Modified: Tue, 09 Jun 2020 05:06:08 GMT  
		Size: 244.6 KB (244636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c629efc5a0d859723a7100a060a51da7cbe12ff931fcd2edcb1be81b2d112240`  
		Last Modified: Tue, 09 Jun 2020 05:06:13 GMT  
		Size: 24.5 MB (24528005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2764189724404bbc9ecbb4c41c717a46e45a9dd50a25b2aaeaaccb46a9f95d48`  
		Last Modified: Tue, 09 Jun 2020 05:08:21 GMT  
		Size: 125.6 MB (125621773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:5.20`

```console
$ docker pull mono@sha256:7c3897b79001e719cb00400400cf20520aa794779e0fee851c77db395d2bf901
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:5.20` - linux; amd64

```console
$ docker pull mono@sha256:0707bc551c8f0483db89e2698f140d4a3747ec5d05681d65f35c1c520cfc6d3e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.2 MB (218165276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:429edcd2234d98f14afc83c7cad33e40f41773a70f625fad37ab67baafdc39dd`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:23:35 GMT
ADD file:57b431451a292755d0f13673f5f3bea9f62aea36c7a1b59d34d7d200ba134fea in / 
# Tue, 09 Jun 2020 01:23:35 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 07:25:19 GMT
ENV MONO_VERSION=5.20.1.34
# Tue, 09 Jun 2020 07:25:31 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Jun 2020 07:25:58 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 09 Jun 2020 07:57:07 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7d2977b12acb33f192e3f20b7e15a467cc8f3f5124a15d975a6d4afe5fa3d258`  
		Last Modified: Tue, 09 Jun 2020 01:28:13 GMT  
		Size: 22.5 MB (22519600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3a96016cede2bbab34292fab9e759f8d6e76cdccf5e984c01f8efd90e6df05b`  
		Last Modified: Tue, 09 Jun 2020 07:58:27 GMT  
		Size: 244.5 KB (244463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05a6ab00376aa34c88796f85c2d808035931da42c558e6f9ff32907a9641b062`  
		Last Modified: Tue, 09 Jun 2020 07:58:43 GMT  
		Size: 55.4 MB (55407571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cebe820795cc4389f4a9bf096d8509cf6ec74165c3dca4d2a090a4d1d9c0e6e9`  
		Last Modified: Tue, 09 Jun 2020 08:01:09 GMT  
		Size: 140.0 MB (139993642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20` - linux; arm variant v5

```console
$ docker pull mono@sha256:f068482b1f0b192e200beffde233675842a2834082c65cd2f557491d078c271a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.8 MB (170828767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40422756bc15d6c9573b6c1a15eda0670c58fc8b0d4b5661a52ce9dfbd27cef5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 00:55:12 GMT
ADD file:0b9f2b88887a8060402a052c243c31641d9c217edcdb232c7b7a057cf5a70d66 in / 
# Wed, 22 Jul 2020 00:55:13 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 04:50:57 GMT
ENV MONO_VERSION=5.20.1.34
# Wed, 22 Jul 2020 04:51:29 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jul 2020 04:52:30 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 22 Jul 2020 05:02:14 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:319109fcb6fa9b08528c518426e7ce105aac7313066432efcea95f59ff6e6788`  
		Last Modified: Wed, 22 Jul 2020 01:03:27 GMT  
		Size: 21.2 MB (21189131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:214f724afb987f92ce9133d6327bf39c60bb2f5e639abe876e341a07f439d60e`  
		Last Modified: Wed, 22 Jul 2020 05:03:20 GMT  
		Size: 244.6 KB (244590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1738e5f6ebf3cc4543e52c88b7aa0fc6f9113fabde1e2980a289aafa5559d5b1`  
		Last Modified: Wed, 22 Jul 2020 05:03:29 GMT  
		Size: 24.2 MB (24150571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecdfd5f9763ca3e982c3a51730342a64a0697da0877ff7dad8f8c39ee2356001`  
		Last Modified: Wed, 22 Jul 2020 05:06:06 GMT  
		Size: 125.2 MB (125244475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20` - linux; arm variant v7

```console
$ docker pull mono@sha256:8328a11a821af5a680bdef017afccdd45d62b737555d11c9bd51c18c842a29cf
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.9 MB (166884235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8bc37db2a9a8b1caccb7c4ae6f82f9e8d05cb22f20e6763ef73dc275f8db3fb`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 01:33:30 GMT
ADD file:49b1a1b4f5c2201b0e23e29dca24c4f6ffc14620196c4bd77770952500c4bee1 in / 
# Wed, 22 Jul 2020 01:33:38 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 02:20:07 GMT
ENV MONO_VERSION=5.20.1.34
# Wed, 22 Jul 2020 02:20:49 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jul 2020 02:21:51 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 22 Jul 2020 02:32:01 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:cd38ad753522d120e27c5343b08f661ee3aebfe531d60102d7c624c16dba4d09`  
		Last Modified: Wed, 22 Jul 2020 01:44:24 GMT  
		Size: 19.3 MB (19298267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae6961338dbeec44b6e92646723bb59c030769220b24193c12f7827ce9ca826f`  
		Last Modified: Wed, 22 Jul 2020 02:33:13 GMT  
		Size: 244.6 KB (244556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:829fd514f3675f9e41ec1f1bc082852015f100014cc48e3b90e1b3023c34fa51`  
		Last Modified: Wed, 22 Jul 2020 02:33:22 GMT  
		Size: 23.5 MB (23453570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:396070eca2a0ddb7dbe1dd76c086672f187f84252665d73b6827e15ad8b0e2ed`  
		Last Modified: Wed, 22 Jul 2020 02:36:16 GMT  
		Size: 123.9 MB (123887842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:fd867443d6b38edb7b351a5f08f953107f530d3a0d9fc76a47ba6ab767ea21cc
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.7 MB (187697331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61776a2e50d7b9d3c215e6d87d93742c511f700b26c7d724654df01daafcf8a3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:54:49 GMT
ADD file:c85d28567b6123deb660b71c8b60d92378b5ba15ba5dcf495d9388817dc3aa44 in / 
# Tue, 09 Jun 2020 01:54:52 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 03:26:55 GMT
ENV MONO_VERSION=5.20.1.34
# Tue, 09 Jun 2020 03:27:13 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Jun 2020 03:27:54 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 09 Jun 2020 03:36:29 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:622dc742b82743ebf5607b215a65869096390ee41b0a61b5532f859fb94590b1`  
		Last Modified: Tue, 09 Jun 2020 02:00:28 GMT  
		Size: 20.4 MB (20375150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47cfdc0a506e196319f490a8bb5e0036dd589b207aa03c9571763b3ee8dea29f`  
		Last Modified: Tue, 09 Jun 2020 03:37:36 GMT  
		Size: 244.4 KB (244372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f6b08527e586e0f80506a226402a72b5cf43e106073bc06aa87862249894d0a`  
		Last Modified: Tue, 09 Jun 2020 03:37:45 GMT  
		Size: 28.0 MB (28049990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da477870a6058bd59427cbbc64d0b14a9abebe5cd6b910fa3ddfe36f278837e0`  
		Last Modified: Tue, 09 Jun 2020 03:40:26 GMT  
		Size: 139.0 MB (139027819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20` - linux; 386

```console
$ docker pull mono@sha256:1ea82d19a0f7414cfe3e98105b310e8d63f06f8f277f3848c6a884b92b77f05b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.7 MB (227671637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bc71aebacae50bcaa4b4f804a23f5f230ae27e5ec7fb10a0f1dd08c3d429ffd`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:42:33 GMT
ADD file:8ef252685ffefc58654053bf145c830928a2cf423a6c757180649df772f1523d in / 
# Tue, 09 Jun 2020 01:42:34 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 07:01:47 GMT
ENV MONO_VERSION=5.20.1.34
# Tue, 09 Jun 2020 07:02:01 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Jun 2020 07:02:35 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 09 Jun 2020 07:09:48 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:4ffbd6ec7974e514763a8d7d9fcf5e86e9440e2280e6e9561ea373b4bc50588e`  
		Last Modified: Tue, 09 Jun 2020 01:48:28 GMT  
		Size: 23.1 MB (23147892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79f35120db9bc30d6de494b0e58b8a74d62fe7a85cdc188357ea98ca2797e839`  
		Last Modified: Tue, 09 Jun 2020 07:11:10 GMT  
		Size: 244.5 KB (244478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d12cec6c246292b2edce2de333f893fefd5d9460042faa8e270bfde498b21612`  
		Last Modified: Tue, 09 Jun 2020 07:11:24 GMT  
		Size: 58.4 MB (58439805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13e5499fc7470d9d9b363a6494025ec430b6c28a85a563b44637506b9da2eca2`  
		Last Modified: Tue, 09 Jun 2020 07:13:37 GMT  
		Size: 145.8 MB (145839462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20` - linux; ppc64le

```console
$ docker pull mono@sha256:15c0c9e91312a3cbd18b060a447868b37ba4d2ef668c759b7e1c19f314bf9dd8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.2 MB (173185683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:065963fd30de2ed1faa7464809f20c63f66805ff3dad0867a93e21adeb544c22`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:25:38 GMT
ADD file:41ec53d65aa183c2835f73989c9e4922f818e59774811eaa6e7395e5a36d5eab in / 
# Tue, 09 Jun 2020 01:25:42 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 04:43:07 GMT
ENV MONO_VERSION=5.20.1.34
# Tue, 09 Jun 2020 04:44:25 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Jun 2020 04:45:52 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 09 Jun 2020 05:04:54 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a29e28607c9b96acae7ff89e56214e4339a87c59e40a6f030fa4cbcaab753f2c`  
		Last Modified: Tue, 09 Jun 2020 01:37:25 GMT  
		Size: 22.8 MB (22791269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21d9971248b8a3142c8d28700658bc11b1313694441bf51b7febefd26adddbe1`  
		Last Modified: Tue, 09 Jun 2020 05:06:08 GMT  
		Size: 244.6 KB (244636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c629efc5a0d859723a7100a060a51da7cbe12ff931fcd2edcb1be81b2d112240`  
		Last Modified: Tue, 09 Jun 2020 05:06:13 GMT  
		Size: 24.5 MB (24528005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2764189724404bbc9ecbb4c41c717a46e45a9dd50a25b2aaeaaccb46a9f95d48`  
		Last Modified: Tue, 09 Jun 2020 05:08:21 GMT  
		Size: 125.6 MB (125621773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:5.20.1`

```console
$ docker pull mono@sha256:7c3897b79001e719cb00400400cf20520aa794779e0fee851c77db395d2bf901
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:5.20.1` - linux; amd64

```console
$ docker pull mono@sha256:0707bc551c8f0483db89e2698f140d4a3747ec5d05681d65f35c1c520cfc6d3e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.2 MB (218165276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:429edcd2234d98f14afc83c7cad33e40f41773a70f625fad37ab67baafdc39dd`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:23:35 GMT
ADD file:57b431451a292755d0f13673f5f3bea9f62aea36c7a1b59d34d7d200ba134fea in / 
# Tue, 09 Jun 2020 01:23:35 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 07:25:19 GMT
ENV MONO_VERSION=5.20.1.34
# Tue, 09 Jun 2020 07:25:31 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Jun 2020 07:25:58 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 09 Jun 2020 07:57:07 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7d2977b12acb33f192e3f20b7e15a467cc8f3f5124a15d975a6d4afe5fa3d258`  
		Last Modified: Tue, 09 Jun 2020 01:28:13 GMT  
		Size: 22.5 MB (22519600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3a96016cede2bbab34292fab9e759f8d6e76cdccf5e984c01f8efd90e6df05b`  
		Last Modified: Tue, 09 Jun 2020 07:58:27 GMT  
		Size: 244.5 KB (244463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05a6ab00376aa34c88796f85c2d808035931da42c558e6f9ff32907a9641b062`  
		Last Modified: Tue, 09 Jun 2020 07:58:43 GMT  
		Size: 55.4 MB (55407571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cebe820795cc4389f4a9bf096d8509cf6ec74165c3dca4d2a090a4d1d9c0e6e9`  
		Last Modified: Tue, 09 Jun 2020 08:01:09 GMT  
		Size: 140.0 MB (139993642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20.1` - linux; arm variant v5

```console
$ docker pull mono@sha256:f068482b1f0b192e200beffde233675842a2834082c65cd2f557491d078c271a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.8 MB (170828767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40422756bc15d6c9573b6c1a15eda0670c58fc8b0d4b5661a52ce9dfbd27cef5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 00:55:12 GMT
ADD file:0b9f2b88887a8060402a052c243c31641d9c217edcdb232c7b7a057cf5a70d66 in / 
# Wed, 22 Jul 2020 00:55:13 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 04:50:57 GMT
ENV MONO_VERSION=5.20.1.34
# Wed, 22 Jul 2020 04:51:29 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jul 2020 04:52:30 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 22 Jul 2020 05:02:14 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:319109fcb6fa9b08528c518426e7ce105aac7313066432efcea95f59ff6e6788`  
		Last Modified: Wed, 22 Jul 2020 01:03:27 GMT  
		Size: 21.2 MB (21189131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:214f724afb987f92ce9133d6327bf39c60bb2f5e639abe876e341a07f439d60e`  
		Last Modified: Wed, 22 Jul 2020 05:03:20 GMT  
		Size: 244.6 KB (244590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1738e5f6ebf3cc4543e52c88b7aa0fc6f9113fabde1e2980a289aafa5559d5b1`  
		Last Modified: Wed, 22 Jul 2020 05:03:29 GMT  
		Size: 24.2 MB (24150571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecdfd5f9763ca3e982c3a51730342a64a0697da0877ff7dad8f8c39ee2356001`  
		Last Modified: Wed, 22 Jul 2020 05:06:06 GMT  
		Size: 125.2 MB (125244475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20.1` - linux; arm variant v7

```console
$ docker pull mono@sha256:8328a11a821af5a680bdef017afccdd45d62b737555d11c9bd51c18c842a29cf
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.9 MB (166884235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8bc37db2a9a8b1caccb7c4ae6f82f9e8d05cb22f20e6763ef73dc275f8db3fb`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 01:33:30 GMT
ADD file:49b1a1b4f5c2201b0e23e29dca24c4f6ffc14620196c4bd77770952500c4bee1 in / 
# Wed, 22 Jul 2020 01:33:38 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 02:20:07 GMT
ENV MONO_VERSION=5.20.1.34
# Wed, 22 Jul 2020 02:20:49 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jul 2020 02:21:51 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 22 Jul 2020 02:32:01 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:cd38ad753522d120e27c5343b08f661ee3aebfe531d60102d7c624c16dba4d09`  
		Last Modified: Wed, 22 Jul 2020 01:44:24 GMT  
		Size: 19.3 MB (19298267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae6961338dbeec44b6e92646723bb59c030769220b24193c12f7827ce9ca826f`  
		Last Modified: Wed, 22 Jul 2020 02:33:13 GMT  
		Size: 244.6 KB (244556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:829fd514f3675f9e41ec1f1bc082852015f100014cc48e3b90e1b3023c34fa51`  
		Last Modified: Wed, 22 Jul 2020 02:33:22 GMT  
		Size: 23.5 MB (23453570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:396070eca2a0ddb7dbe1dd76c086672f187f84252665d73b6827e15ad8b0e2ed`  
		Last Modified: Wed, 22 Jul 2020 02:36:16 GMT  
		Size: 123.9 MB (123887842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20.1` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:fd867443d6b38edb7b351a5f08f953107f530d3a0d9fc76a47ba6ab767ea21cc
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.7 MB (187697331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61776a2e50d7b9d3c215e6d87d93742c511f700b26c7d724654df01daafcf8a3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:54:49 GMT
ADD file:c85d28567b6123deb660b71c8b60d92378b5ba15ba5dcf495d9388817dc3aa44 in / 
# Tue, 09 Jun 2020 01:54:52 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 03:26:55 GMT
ENV MONO_VERSION=5.20.1.34
# Tue, 09 Jun 2020 03:27:13 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Jun 2020 03:27:54 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 09 Jun 2020 03:36:29 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:622dc742b82743ebf5607b215a65869096390ee41b0a61b5532f859fb94590b1`  
		Last Modified: Tue, 09 Jun 2020 02:00:28 GMT  
		Size: 20.4 MB (20375150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47cfdc0a506e196319f490a8bb5e0036dd589b207aa03c9571763b3ee8dea29f`  
		Last Modified: Tue, 09 Jun 2020 03:37:36 GMT  
		Size: 244.4 KB (244372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f6b08527e586e0f80506a226402a72b5cf43e106073bc06aa87862249894d0a`  
		Last Modified: Tue, 09 Jun 2020 03:37:45 GMT  
		Size: 28.0 MB (28049990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da477870a6058bd59427cbbc64d0b14a9abebe5cd6b910fa3ddfe36f278837e0`  
		Last Modified: Tue, 09 Jun 2020 03:40:26 GMT  
		Size: 139.0 MB (139027819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20.1` - linux; 386

```console
$ docker pull mono@sha256:1ea82d19a0f7414cfe3e98105b310e8d63f06f8f277f3848c6a884b92b77f05b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.7 MB (227671637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bc71aebacae50bcaa4b4f804a23f5f230ae27e5ec7fb10a0f1dd08c3d429ffd`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:42:33 GMT
ADD file:8ef252685ffefc58654053bf145c830928a2cf423a6c757180649df772f1523d in / 
# Tue, 09 Jun 2020 01:42:34 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 07:01:47 GMT
ENV MONO_VERSION=5.20.1.34
# Tue, 09 Jun 2020 07:02:01 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Jun 2020 07:02:35 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 09 Jun 2020 07:09:48 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:4ffbd6ec7974e514763a8d7d9fcf5e86e9440e2280e6e9561ea373b4bc50588e`  
		Last Modified: Tue, 09 Jun 2020 01:48:28 GMT  
		Size: 23.1 MB (23147892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79f35120db9bc30d6de494b0e58b8a74d62fe7a85cdc188357ea98ca2797e839`  
		Last Modified: Tue, 09 Jun 2020 07:11:10 GMT  
		Size: 244.5 KB (244478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d12cec6c246292b2edce2de333f893fefd5d9460042faa8e270bfde498b21612`  
		Last Modified: Tue, 09 Jun 2020 07:11:24 GMT  
		Size: 58.4 MB (58439805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13e5499fc7470d9d9b363a6494025ec430b6c28a85a563b44637506b9da2eca2`  
		Last Modified: Tue, 09 Jun 2020 07:13:37 GMT  
		Size: 145.8 MB (145839462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20.1` - linux; ppc64le

```console
$ docker pull mono@sha256:15c0c9e91312a3cbd18b060a447868b37ba4d2ef668c759b7e1c19f314bf9dd8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.2 MB (173185683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:065963fd30de2ed1faa7464809f20c63f66805ff3dad0867a93e21adeb544c22`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:25:38 GMT
ADD file:41ec53d65aa183c2835f73989c9e4922f818e59774811eaa6e7395e5a36d5eab in / 
# Tue, 09 Jun 2020 01:25:42 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 04:43:07 GMT
ENV MONO_VERSION=5.20.1.34
# Tue, 09 Jun 2020 04:44:25 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Jun 2020 04:45:52 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 09 Jun 2020 05:04:54 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a29e28607c9b96acae7ff89e56214e4339a87c59e40a6f030fa4cbcaab753f2c`  
		Last Modified: Tue, 09 Jun 2020 01:37:25 GMT  
		Size: 22.8 MB (22791269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21d9971248b8a3142c8d28700658bc11b1313694441bf51b7febefd26adddbe1`  
		Last Modified: Tue, 09 Jun 2020 05:06:08 GMT  
		Size: 244.6 KB (244636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c629efc5a0d859723a7100a060a51da7cbe12ff931fcd2edcb1be81b2d112240`  
		Last Modified: Tue, 09 Jun 2020 05:06:13 GMT  
		Size: 24.5 MB (24528005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2764189724404bbc9ecbb4c41c717a46e45a9dd50a25b2aaeaaccb46a9f95d48`  
		Last Modified: Tue, 09 Jun 2020 05:08:21 GMT  
		Size: 125.6 MB (125621773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:5.20.1.34`

```console
$ docker pull mono@sha256:7c3897b79001e719cb00400400cf20520aa794779e0fee851c77db395d2bf901
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:5.20.1.34` - linux; amd64

```console
$ docker pull mono@sha256:0707bc551c8f0483db89e2698f140d4a3747ec5d05681d65f35c1c520cfc6d3e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.2 MB (218165276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:429edcd2234d98f14afc83c7cad33e40f41773a70f625fad37ab67baafdc39dd`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:23:35 GMT
ADD file:57b431451a292755d0f13673f5f3bea9f62aea36c7a1b59d34d7d200ba134fea in / 
# Tue, 09 Jun 2020 01:23:35 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 07:25:19 GMT
ENV MONO_VERSION=5.20.1.34
# Tue, 09 Jun 2020 07:25:31 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Jun 2020 07:25:58 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 09 Jun 2020 07:57:07 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7d2977b12acb33f192e3f20b7e15a467cc8f3f5124a15d975a6d4afe5fa3d258`  
		Last Modified: Tue, 09 Jun 2020 01:28:13 GMT  
		Size: 22.5 MB (22519600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3a96016cede2bbab34292fab9e759f8d6e76cdccf5e984c01f8efd90e6df05b`  
		Last Modified: Tue, 09 Jun 2020 07:58:27 GMT  
		Size: 244.5 KB (244463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05a6ab00376aa34c88796f85c2d808035931da42c558e6f9ff32907a9641b062`  
		Last Modified: Tue, 09 Jun 2020 07:58:43 GMT  
		Size: 55.4 MB (55407571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cebe820795cc4389f4a9bf096d8509cf6ec74165c3dca4d2a090a4d1d9c0e6e9`  
		Last Modified: Tue, 09 Jun 2020 08:01:09 GMT  
		Size: 140.0 MB (139993642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20.1.34` - linux; arm variant v5

```console
$ docker pull mono@sha256:f068482b1f0b192e200beffde233675842a2834082c65cd2f557491d078c271a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.8 MB (170828767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40422756bc15d6c9573b6c1a15eda0670c58fc8b0d4b5661a52ce9dfbd27cef5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 00:55:12 GMT
ADD file:0b9f2b88887a8060402a052c243c31641d9c217edcdb232c7b7a057cf5a70d66 in / 
# Wed, 22 Jul 2020 00:55:13 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 04:50:57 GMT
ENV MONO_VERSION=5.20.1.34
# Wed, 22 Jul 2020 04:51:29 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jul 2020 04:52:30 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 22 Jul 2020 05:02:14 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:319109fcb6fa9b08528c518426e7ce105aac7313066432efcea95f59ff6e6788`  
		Last Modified: Wed, 22 Jul 2020 01:03:27 GMT  
		Size: 21.2 MB (21189131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:214f724afb987f92ce9133d6327bf39c60bb2f5e639abe876e341a07f439d60e`  
		Last Modified: Wed, 22 Jul 2020 05:03:20 GMT  
		Size: 244.6 KB (244590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1738e5f6ebf3cc4543e52c88b7aa0fc6f9113fabde1e2980a289aafa5559d5b1`  
		Last Modified: Wed, 22 Jul 2020 05:03:29 GMT  
		Size: 24.2 MB (24150571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecdfd5f9763ca3e982c3a51730342a64a0697da0877ff7dad8f8c39ee2356001`  
		Last Modified: Wed, 22 Jul 2020 05:06:06 GMT  
		Size: 125.2 MB (125244475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20.1.34` - linux; arm variant v7

```console
$ docker pull mono@sha256:8328a11a821af5a680bdef017afccdd45d62b737555d11c9bd51c18c842a29cf
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.9 MB (166884235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8bc37db2a9a8b1caccb7c4ae6f82f9e8d05cb22f20e6763ef73dc275f8db3fb`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 01:33:30 GMT
ADD file:49b1a1b4f5c2201b0e23e29dca24c4f6ffc14620196c4bd77770952500c4bee1 in / 
# Wed, 22 Jul 2020 01:33:38 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 02:20:07 GMT
ENV MONO_VERSION=5.20.1.34
# Wed, 22 Jul 2020 02:20:49 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jul 2020 02:21:51 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 22 Jul 2020 02:32:01 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:cd38ad753522d120e27c5343b08f661ee3aebfe531d60102d7c624c16dba4d09`  
		Last Modified: Wed, 22 Jul 2020 01:44:24 GMT  
		Size: 19.3 MB (19298267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae6961338dbeec44b6e92646723bb59c030769220b24193c12f7827ce9ca826f`  
		Last Modified: Wed, 22 Jul 2020 02:33:13 GMT  
		Size: 244.6 KB (244556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:829fd514f3675f9e41ec1f1bc082852015f100014cc48e3b90e1b3023c34fa51`  
		Last Modified: Wed, 22 Jul 2020 02:33:22 GMT  
		Size: 23.5 MB (23453570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:396070eca2a0ddb7dbe1dd76c086672f187f84252665d73b6827e15ad8b0e2ed`  
		Last Modified: Wed, 22 Jul 2020 02:36:16 GMT  
		Size: 123.9 MB (123887842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20.1.34` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:fd867443d6b38edb7b351a5f08f953107f530d3a0d9fc76a47ba6ab767ea21cc
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.7 MB (187697331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61776a2e50d7b9d3c215e6d87d93742c511f700b26c7d724654df01daafcf8a3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:54:49 GMT
ADD file:c85d28567b6123deb660b71c8b60d92378b5ba15ba5dcf495d9388817dc3aa44 in / 
# Tue, 09 Jun 2020 01:54:52 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 03:26:55 GMT
ENV MONO_VERSION=5.20.1.34
# Tue, 09 Jun 2020 03:27:13 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Jun 2020 03:27:54 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 09 Jun 2020 03:36:29 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:622dc742b82743ebf5607b215a65869096390ee41b0a61b5532f859fb94590b1`  
		Last Modified: Tue, 09 Jun 2020 02:00:28 GMT  
		Size: 20.4 MB (20375150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47cfdc0a506e196319f490a8bb5e0036dd589b207aa03c9571763b3ee8dea29f`  
		Last Modified: Tue, 09 Jun 2020 03:37:36 GMT  
		Size: 244.4 KB (244372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f6b08527e586e0f80506a226402a72b5cf43e106073bc06aa87862249894d0a`  
		Last Modified: Tue, 09 Jun 2020 03:37:45 GMT  
		Size: 28.0 MB (28049990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da477870a6058bd59427cbbc64d0b14a9abebe5cd6b910fa3ddfe36f278837e0`  
		Last Modified: Tue, 09 Jun 2020 03:40:26 GMT  
		Size: 139.0 MB (139027819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20.1.34` - linux; 386

```console
$ docker pull mono@sha256:1ea82d19a0f7414cfe3e98105b310e8d63f06f8f277f3848c6a884b92b77f05b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.7 MB (227671637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bc71aebacae50bcaa4b4f804a23f5f230ae27e5ec7fb10a0f1dd08c3d429ffd`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:42:33 GMT
ADD file:8ef252685ffefc58654053bf145c830928a2cf423a6c757180649df772f1523d in / 
# Tue, 09 Jun 2020 01:42:34 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 07:01:47 GMT
ENV MONO_VERSION=5.20.1.34
# Tue, 09 Jun 2020 07:02:01 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Jun 2020 07:02:35 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 09 Jun 2020 07:09:48 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:4ffbd6ec7974e514763a8d7d9fcf5e86e9440e2280e6e9561ea373b4bc50588e`  
		Last Modified: Tue, 09 Jun 2020 01:48:28 GMT  
		Size: 23.1 MB (23147892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79f35120db9bc30d6de494b0e58b8a74d62fe7a85cdc188357ea98ca2797e839`  
		Last Modified: Tue, 09 Jun 2020 07:11:10 GMT  
		Size: 244.5 KB (244478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d12cec6c246292b2edce2de333f893fefd5d9460042faa8e270bfde498b21612`  
		Last Modified: Tue, 09 Jun 2020 07:11:24 GMT  
		Size: 58.4 MB (58439805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13e5499fc7470d9d9b363a6494025ec430b6c28a85a563b44637506b9da2eca2`  
		Last Modified: Tue, 09 Jun 2020 07:13:37 GMT  
		Size: 145.8 MB (145839462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20.1.34` - linux; ppc64le

```console
$ docker pull mono@sha256:15c0c9e91312a3cbd18b060a447868b37ba4d2ef668c759b7e1c19f314bf9dd8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.2 MB (173185683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:065963fd30de2ed1faa7464809f20c63f66805ff3dad0867a93e21adeb544c22`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:25:38 GMT
ADD file:41ec53d65aa183c2835f73989c9e4922f818e59774811eaa6e7395e5a36d5eab in / 
# Tue, 09 Jun 2020 01:25:42 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 04:43:07 GMT
ENV MONO_VERSION=5.20.1.34
# Tue, 09 Jun 2020 04:44:25 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Jun 2020 04:45:52 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 09 Jun 2020 05:04:54 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a29e28607c9b96acae7ff89e56214e4339a87c59e40a6f030fa4cbcaab753f2c`  
		Last Modified: Tue, 09 Jun 2020 01:37:25 GMT  
		Size: 22.8 MB (22791269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21d9971248b8a3142c8d28700658bc11b1313694441bf51b7febefd26adddbe1`  
		Last Modified: Tue, 09 Jun 2020 05:06:08 GMT  
		Size: 244.6 KB (244636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c629efc5a0d859723a7100a060a51da7cbe12ff931fcd2edcb1be81b2d112240`  
		Last Modified: Tue, 09 Jun 2020 05:06:13 GMT  
		Size: 24.5 MB (24528005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2764189724404bbc9ecbb4c41c717a46e45a9dd50a25b2aaeaaccb46a9f95d48`  
		Last Modified: Tue, 09 Jun 2020 05:08:21 GMT  
		Size: 125.6 MB (125621773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:5.20.1.34-slim`

```console
$ docker pull mono@sha256:7b1baf75b397d0fa3c79cfc483e0dd83ae7b40987a60d269d8d0f900def6a281
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:5.20.1.34-slim` - linux; amd64

```console
$ docker pull mono@sha256:16162056f6d04d68d3b297f123edad3e7bba54f4e0ee84c5cd5012610935b7c9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.2 MB (78171634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd0eab449535c70e3a40b2293d483a0213d2426f5a4a6539ce69688dca0ddee0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:23:35 GMT
ADD file:57b431451a292755d0f13673f5f3bea9f62aea36c7a1b59d34d7d200ba134fea in / 
# Tue, 09 Jun 2020 01:23:35 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 07:25:19 GMT
ENV MONO_VERSION=5.20.1.34
# Tue, 09 Jun 2020 07:25:31 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Jun 2020 07:25:58 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7d2977b12acb33f192e3f20b7e15a467cc8f3f5124a15d975a6d4afe5fa3d258`  
		Last Modified: Tue, 09 Jun 2020 01:28:13 GMT  
		Size: 22.5 MB (22519600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3a96016cede2bbab34292fab9e759f8d6e76cdccf5e984c01f8efd90e6df05b`  
		Last Modified: Tue, 09 Jun 2020 07:58:27 GMT  
		Size: 244.5 KB (244463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05a6ab00376aa34c88796f85c2d808035931da42c558e6f9ff32907a9641b062`  
		Last Modified: Tue, 09 Jun 2020 07:58:43 GMT  
		Size: 55.4 MB (55407571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20.1.34-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:ec3602c25a4a890750685bb5f19d7a34a20516a37059153579b68a4f74f17f3d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45584292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae3c8177fa72be71e59c5119b36ba1f5f0a9099f41a0d3032bd34b486c34c3f6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 00:55:12 GMT
ADD file:0b9f2b88887a8060402a052c243c31641d9c217edcdb232c7b7a057cf5a70d66 in / 
# Wed, 22 Jul 2020 00:55:13 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 04:50:57 GMT
ENV MONO_VERSION=5.20.1.34
# Wed, 22 Jul 2020 04:51:29 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jul 2020 04:52:30 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:319109fcb6fa9b08528c518426e7ce105aac7313066432efcea95f59ff6e6788`  
		Last Modified: Wed, 22 Jul 2020 01:03:27 GMT  
		Size: 21.2 MB (21189131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:214f724afb987f92ce9133d6327bf39c60bb2f5e639abe876e341a07f439d60e`  
		Last Modified: Wed, 22 Jul 2020 05:03:20 GMT  
		Size: 244.6 KB (244590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1738e5f6ebf3cc4543e52c88b7aa0fc6f9113fabde1e2980a289aafa5559d5b1`  
		Last Modified: Wed, 22 Jul 2020 05:03:29 GMT  
		Size: 24.2 MB (24150571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20.1.34-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:4386b149b67f32efb634322ead66cbd1af15e940a4fdbed1096cea4a7b5c0e1e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.0 MB (42996393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f18852418937a80e1446631268ee77d13a3bc5e056f76139117a44a72ecdc3ca`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 01:33:30 GMT
ADD file:49b1a1b4f5c2201b0e23e29dca24c4f6ffc14620196c4bd77770952500c4bee1 in / 
# Wed, 22 Jul 2020 01:33:38 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 02:20:07 GMT
ENV MONO_VERSION=5.20.1.34
# Wed, 22 Jul 2020 02:20:49 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jul 2020 02:21:51 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:cd38ad753522d120e27c5343b08f661ee3aebfe531d60102d7c624c16dba4d09`  
		Last Modified: Wed, 22 Jul 2020 01:44:24 GMT  
		Size: 19.3 MB (19298267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae6961338dbeec44b6e92646723bb59c030769220b24193c12f7827ce9ca826f`  
		Last Modified: Wed, 22 Jul 2020 02:33:13 GMT  
		Size: 244.6 KB (244556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:829fd514f3675f9e41ec1f1bc082852015f100014cc48e3b90e1b3023c34fa51`  
		Last Modified: Wed, 22 Jul 2020 02:33:22 GMT  
		Size: 23.5 MB (23453570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20.1.34-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:48d8d81739bb780c0f6f54e39773ed7239fa34117e4baed155af459bdc7bb08e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48669512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4ef5ae213ee661f770b0931778cc05a349d7bac270e37715b391431cb89a305`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:54:49 GMT
ADD file:c85d28567b6123deb660b71c8b60d92378b5ba15ba5dcf495d9388817dc3aa44 in / 
# Tue, 09 Jun 2020 01:54:52 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 03:26:55 GMT
ENV MONO_VERSION=5.20.1.34
# Tue, 09 Jun 2020 03:27:13 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Jun 2020 03:27:54 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:622dc742b82743ebf5607b215a65869096390ee41b0a61b5532f859fb94590b1`  
		Last Modified: Tue, 09 Jun 2020 02:00:28 GMT  
		Size: 20.4 MB (20375150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47cfdc0a506e196319f490a8bb5e0036dd589b207aa03c9571763b3ee8dea29f`  
		Last Modified: Tue, 09 Jun 2020 03:37:36 GMT  
		Size: 244.4 KB (244372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f6b08527e586e0f80506a226402a72b5cf43e106073bc06aa87862249894d0a`  
		Last Modified: Tue, 09 Jun 2020 03:37:45 GMT  
		Size: 28.0 MB (28049990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20.1.34-slim` - linux; 386

```console
$ docker pull mono@sha256:4222a99c9b296042587b96f689ebbf6634a8d8d2c635c4cd04d351e97712e0b9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.8 MB (81832175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4614f168389960f66e555809e63b35524bfd333eae47ec3048ab9ceb067a573`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:42:33 GMT
ADD file:8ef252685ffefc58654053bf145c830928a2cf423a6c757180649df772f1523d in / 
# Tue, 09 Jun 2020 01:42:34 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 07:01:47 GMT
ENV MONO_VERSION=5.20.1.34
# Tue, 09 Jun 2020 07:02:01 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Jun 2020 07:02:35 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:4ffbd6ec7974e514763a8d7d9fcf5e86e9440e2280e6e9561ea373b4bc50588e`  
		Last Modified: Tue, 09 Jun 2020 01:48:28 GMT  
		Size: 23.1 MB (23147892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79f35120db9bc30d6de494b0e58b8a74d62fe7a85cdc188357ea98ca2797e839`  
		Last Modified: Tue, 09 Jun 2020 07:11:10 GMT  
		Size: 244.5 KB (244478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d12cec6c246292b2edce2de333f893fefd5d9460042faa8e270bfde498b21612`  
		Last Modified: Tue, 09 Jun 2020 07:11:24 GMT  
		Size: 58.4 MB (58439805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20.1.34-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:176998bc9e1646c37ff64d0d4f385f36e1f8922f56319d19bb3c38f981738c0d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.6 MB (47563910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:406b118562a7fad8d6cb5ebd56d606c3007c1d31422152f7a9d5141a7803798b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:25:38 GMT
ADD file:41ec53d65aa183c2835f73989c9e4922f818e59774811eaa6e7395e5a36d5eab in / 
# Tue, 09 Jun 2020 01:25:42 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 04:43:07 GMT
ENV MONO_VERSION=5.20.1.34
# Tue, 09 Jun 2020 04:44:25 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Jun 2020 04:45:52 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a29e28607c9b96acae7ff89e56214e4339a87c59e40a6f030fa4cbcaab753f2c`  
		Last Modified: Tue, 09 Jun 2020 01:37:25 GMT  
		Size: 22.8 MB (22791269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21d9971248b8a3142c8d28700658bc11b1313694441bf51b7febefd26adddbe1`  
		Last Modified: Tue, 09 Jun 2020 05:06:08 GMT  
		Size: 244.6 KB (244636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c629efc5a0d859723a7100a060a51da7cbe12ff931fcd2edcb1be81b2d112240`  
		Last Modified: Tue, 09 Jun 2020 05:06:13 GMT  
		Size: 24.5 MB (24528005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:5.20.1-slim`

```console
$ docker pull mono@sha256:7b1baf75b397d0fa3c79cfc483e0dd83ae7b40987a60d269d8d0f900def6a281
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:5.20.1-slim` - linux; amd64

```console
$ docker pull mono@sha256:16162056f6d04d68d3b297f123edad3e7bba54f4e0ee84c5cd5012610935b7c9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.2 MB (78171634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd0eab449535c70e3a40b2293d483a0213d2426f5a4a6539ce69688dca0ddee0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:23:35 GMT
ADD file:57b431451a292755d0f13673f5f3bea9f62aea36c7a1b59d34d7d200ba134fea in / 
# Tue, 09 Jun 2020 01:23:35 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 07:25:19 GMT
ENV MONO_VERSION=5.20.1.34
# Tue, 09 Jun 2020 07:25:31 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Jun 2020 07:25:58 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7d2977b12acb33f192e3f20b7e15a467cc8f3f5124a15d975a6d4afe5fa3d258`  
		Last Modified: Tue, 09 Jun 2020 01:28:13 GMT  
		Size: 22.5 MB (22519600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3a96016cede2bbab34292fab9e759f8d6e76cdccf5e984c01f8efd90e6df05b`  
		Last Modified: Tue, 09 Jun 2020 07:58:27 GMT  
		Size: 244.5 KB (244463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05a6ab00376aa34c88796f85c2d808035931da42c558e6f9ff32907a9641b062`  
		Last Modified: Tue, 09 Jun 2020 07:58:43 GMT  
		Size: 55.4 MB (55407571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20.1-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:ec3602c25a4a890750685bb5f19d7a34a20516a37059153579b68a4f74f17f3d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45584292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae3c8177fa72be71e59c5119b36ba1f5f0a9099f41a0d3032bd34b486c34c3f6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 00:55:12 GMT
ADD file:0b9f2b88887a8060402a052c243c31641d9c217edcdb232c7b7a057cf5a70d66 in / 
# Wed, 22 Jul 2020 00:55:13 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 04:50:57 GMT
ENV MONO_VERSION=5.20.1.34
# Wed, 22 Jul 2020 04:51:29 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jul 2020 04:52:30 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:319109fcb6fa9b08528c518426e7ce105aac7313066432efcea95f59ff6e6788`  
		Last Modified: Wed, 22 Jul 2020 01:03:27 GMT  
		Size: 21.2 MB (21189131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:214f724afb987f92ce9133d6327bf39c60bb2f5e639abe876e341a07f439d60e`  
		Last Modified: Wed, 22 Jul 2020 05:03:20 GMT  
		Size: 244.6 KB (244590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1738e5f6ebf3cc4543e52c88b7aa0fc6f9113fabde1e2980a289aafa5559d5b1`  
		Last Modified: Wed, 22 Jul 2020 05:03:29 GMT  
		Size: 24.2 MB (24150571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20.1-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:4386b149b67f32efb634322ead66cbd1af15e940a4fdbed1096cea4a7b5c0e1e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.0 MB (42996393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f18852418937a80e1446631268ee77d13a3bc5e056f76139117a44a72ecdc3ca`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 01:33:30 GMT
ADD file:49b1a1b4f5c2201b0e23e29dca24c4f6ffc14620196c4bd77770952500c4bee1 in / 
# Wed, 22 Jul 2020 01:33:38 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 02:20:07 GMT
ENV MONO_VERSION=5.20.1.34
# Wed, 22 Jul 2020 02:20:49 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jul 2020 02:21:51 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:cd38ad753522d120e27c5343b08f661ee3aebfe531d60102d7c624c16dba4d09`  
		Last Modified: Wed, 22 Jul 2020 01:44:24 GMT  
		Size: 19.3 MB (19298267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae6961338dbeec44b6e92646723bb59c030769220b24193c12f7827ce9ca826f`  
		Last Modified: Wed, 22 Jul 2020 02:33:13 GMT  
		Size: 244.6 KB (244556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:829fd514f3675f9e41ec1f1bc082852015f100014cc48e3b90e1b3023c34fa51`  
		Last Modified: Wed, 22 Jul 2020 02:33:22 GMT  
		Size: 23.5 MB (23453570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20.1-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:48d8d81739bb780c0f6f54e39773ed7239fa34117e4baed155af459bdc7bb08e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48669512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4ef5ae213ee661f770b0931778cc05a349d7bac270e37715b391431cb89a305`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:54:49 GMT
ADD file:c85d28567b6123deb660b71c8b60d92378b5ba15ba5dcf495d9388817dc3aa44 in / 
# Tue, 09 Jun 2020 01:54:52 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 03:26:55 GMT
ENV MONO_VERSION=5.20.1.34
# Tue, 09 Jun 2020 03:27:13 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Jun 2020 03:27:54 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:622dc742b82743ebf5607b215a65869096390ee41b0a61b5532f859fb94590b1`  
		Last Modified: Tue, 09 Jun 2020 02:00:28 GMT  
		Size: 20.4 MB (20375150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47cfdc0a506e196319f490a8bb5e0036dd589b207aa03c9571763b3ee8dea29f`  
		Last Modified: Tue, 09 Jun 2020 03:37:36 GMT  
		Size: 244.4 KB (244372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f6b08527e586e0f80506a226402a72b5cf43e106073bc06aa87862249894d0a`  
		Last Modified: Tue, 09 Jun 2020 03:37:45 GMT  
		Size: 28.0 MB (28049990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20.1-slim` - linux; 386

```console
$ docker pull mono@sha256:4222a99c9b296042587b96f689ebbf6634a8d8d2c635c4cd04d351e97712e0b9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.8 MB (81832175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4614f168389960f66e555809e63b35524bfd333eae47ec3048ab9ceb067a573`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:42:33 GMT
ADD file:8ef252685ffefc58654053bf145c830928a2cf423a6c757180649df772f1523d in / 
# Tue, 09 Jun 2020 01:42:34 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 07:01:47 GMT
ENV MONO_VERSION=5.20.1.34
# Tue, 09 Jun 2020 07:02:01 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Jun 2020 07:02:35 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:4ffbd6ec7974e514763a8d7d9fcf5e86e9440e2280e6e9561ea373b4bc50588e`  
		Last Modified: Tue, 09 Jun 2020 01:48:28 GMT  
		Size: 23.1 MB (23147892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79f35120db9bc30d6de494b0e58b8a74d62fe7a85cdc188357ea98ca2797e839`  
		Last Modified: Tue, 09 Jun 2020 07:11:10 GMT  
		Size: 244.5 KB (244478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d12cec6c246292b2edce2de333f893fefd5d9460042faa8e270bfde498b21612`  
		Last Modified: Tue, 09 Jun 2020 07:11:24 GMT  
		Size: 58.4 MB (58439805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20.1-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:176998bc9e1646c37ff64d0d4f385f36e1f8922f56319d19bb3c38f981738c0d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.6 MB (47563910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:406b118562a7fad8d6cb5ebd56d606c3007c1d31422152f7a9d5141a7803798b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:25:38 GMT
ADD file:41ec53d65aa183c2835f73989c9e4922f818e59774811eaa6e7395e5a36d5eab in / 
# Tue, 09 Jun 2020 01:25:42 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 04:43:07 GMT
ENV MONO_VERSION=5.20.1.34
# Tue, 09 Jun 2020 04:44:25 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Jun 2020 04:45:52 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a29e28607c9b96acae7ff89e56214e4339a87c59e40a6f030fa4cbcaab753f2c`  
		Last Modified: Tue, 09 Jun 2020 01:37:25 GMT  
		Size: 22.8 MB (22791269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21d9971248b8a3142c8d28700658bc11b1313694441bf51b7febefd26adddbe1`  
		Last Modified: Tue, 09 Jun 2020 05:06:08 GMT  
		Size: 244.6 KB (244636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c629efc5a0d859723a7100a060a51da7cbe12ff931fcd2edcb1be81b2d112240`  
		Last Modified: Tue, 09 Jun 2020 05:06:13 GMT  
		Size: 24.5 MB (24528005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:5.20-slim`

```console
$ docker pull mono@sha256:7b1baf75b397d0fa3c79cfc483e0dd83ae7b40987a60d269d8d0f900def6a281
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:5.20-slim` - linux; amd64

```console
$ docker pull mono@sha256:16162056f6d04d68d3b297f123edad3e7bba54f4e0ee84c5cd5012610935b7c9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.2 MB (78171634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd0eab449535c70e3a40b2293d483a0213d2426f5a4a6539ce69688dca0ddee0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:23:35 GMT
ADD file:57b431451a292755d0f13673f5f3bea9f62aea36c7a1b59d34d7d200ba134fea in / 
# Tue, 09 Jun 2020 01:23:35 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 07:25:19 GMT
ENV MONO_VERSION=5.20.1.34
# Tue, 09 Jun 2020 07:25:31 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Jun 2020 07:25:58 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7d2977b12acb33f192e3f20b7e15a467cc8f3f5124a15d975a6d4afe5fa3d258`  
		Last Modified: Tue, 09 Jun 2020 01:28:13 GMT  
		Size: 22.5 MB (22519600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3a96016cede2bbab34292fab9e759f8d6e76cdccf5e984c01f8efd90e6df05b`  
		Last Modified: Tue, 09 Jun 2020 07:58:27 GMT  
		Size: 244.5 KB (244463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05a6ab00376aa34c88796f85c2d808035931da42c558e6f9ff32907a9641b062`  
		Last Modified: Tue, 09 Jun 2020 07:58:43 GMT  
		Size: 55.4 MB (55407571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:ec3602c25a4a890750685bb5f19d7a34a20516a37059153579b68a4f74f17f3d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45584292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae3c8177fa72be71e59c5119b36ba1f5f0a9099f41a0d3032bd34b486c34c3f6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 00:55:12 GMT
ADD file:0b9f2b88887a8060402a052c243c31641d9c217edcdb232c7b7a057cf5a70d66 in / 
# Wed, 22 Jul 2020 00:55:13 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 04:50:57 GMT
ENV MONO_VERSION=5.20.1.34
# Wed, 22 Jul 2020 04:51:29 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jul 2020 04:52:30 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:319109fcb6fa9b08528c518426e7ce105aac7313066432efcea95f59ff6e6788`  
		Last Modified: Wed, 22 Jul 2020 01:03:27 GMT  
		Size: 21.2 MB (21189131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:214f724afb987f92ce9133d6327bf39c60bb2f5e639abe876e341a07f439d60e`  
		Last Modified: Wed, 22 Jul 2020 05:03:20 GMT  
		Size: 244.6 KB (244590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1738e5f6ebf3cc4543e52c88b7aa0fc6f9113fabde1e2980a289aafa5559d5b1`  
		Last Modified: Wed, 22 Jul 2020 05:03:29 GMT  
		Size: 24.2 MB (24150571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:4386b149b67f32efb634322ead66cbd1af15e940a4fdbed1096cea4a7b5c0e1e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.0 MB (42996393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f18852418937a80e1446631268ee77d13a3bc5e056f76139117a44a72ecdc3ca`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 01:33:30 GMT
ADD file:49b1a1b4f5c2201b0e23e29dca24c4f6ffc14620196c4bd77770952500c4bee1 in / 
# Wed, 22 Jul 2020 01:33:38 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 02:20:07 GMT
ENV MONO_VERSION=5.20.1.34
# Wed, 22 Jul 2020 02:20:49 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jul 2020 02:21:51 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:cd38ad753522d120e27c5343b08f661ee3aebfe531d60102d7c624c16dba4d09`  
		Last Modified: Wed, 22 Jul 2020 01:44:24 GMT  
		Size: 19.3 MB (19298267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae6961338dbeec44b6e92646723bb59c030769220b24193c12f7827ce9ca826f`  
		Last Modified: Wed, 22 Jul 2020 02:33:13 GMT  
		Size: 244.6 KB (244556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:829fd514f3675f9e41ec1f1bc082852015f100014cc48e3b90e1b3023c34fa51`  
		Last Modified: Wed, 22 Jul 2020 02:33:22 GMT  
		Size: 23.5 MB (23453570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:48d8d81739bb780c0f6f54e39773ed7239fa34117e4baed155af459bdc7bb08e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48669512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4ef5ae213ee661f770b0931778cc05a349d7bac270e37715b391431cb89a305`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:54:49 GMT
ADD file:c85d28567b6123deb660b71c8b60d92378b5ba15ba5dcf495d9388817dc3aa44 in / 
# Tue, 09 Jun 2020 01:54:52 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 03:26:55 GMT
ENV MONO_VERSION=5.20.1.34
# Tue, 09 Jun 2020 03:27:13 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Jun 2020 03:27:54 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:622dc742b82743ebf5607b215a65869096390ee41b0a61b5532f859fb94590b1`  
		Last Modified: Tue, 09 Jun 2020 02:00:28 GMT  
		Size: 20.4 MB (20375150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47cfdc0a506e196319f490a8bb5e0036dd589b207aa03c9571763b3ee8dea29f`  
		Last Modified: Tue, 09 Jun 2020 03:37:36 GMT  
		Size: 244.4 KB (244372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f6b08527e586e0f80506a226402a72b5cf43e106073bc06aa87862249894d0a`  
		Last Modified: Tue, 09 Jun 2020 03:37:45 GMT  
		Size: 28.0 MB (28049990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20-slim` - linux; 386

```console
$ docker pull mono@sha256:4222a99c9b296042587b96f689ebbf6634a8d8d2c635c4cd04d351e97712e0b9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.8 MB (81832175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4614f168389960f66e555809e63b35524bfd333eae47ec3048ab9ceb067a573`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:42:33 GMT
ADD file:8ef252685ffefc58654053bf145c830928a2cf423a6c757180649df772f1523d in / 
# Tue, 09 Jun 2020 01:42:34 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 07:01:47 GMT
ENV MONO_VERSION=5.20.1.34
# Tue, 09 Jun 2020 07:02:01 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Jun 2020 07:02:35 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:4ffbd6ec7974e514763a8d7d9fcf5e86e9440e2280e6e9561ea373b4bc50588e`  
		Last Modified: Tue, 09 Jun 2020 01:48:28 GMT  
		Size: 23.1 MB (23147892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79f35120db9bc30d6de494b0e58b8a74d62fe7a85cdc188357ea98ca2797e839`  
		Last Modified: Tue, 09 Jun 2020 07:11:10 GMT  
		Size: 244.5 KB (244478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d12cec6c246292b2edce2de333f893fefd5d9460042faa8e270bfde498b21612`  
		Last Modified: Tue, 09 Jun 2020 07:11:24 GMT  
		Size: 58.4 MB (58439805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:176998bc9e1646c37ff64d0d4f385f36e1f8922f56319d19bb3c38f981738c0d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.6 MB (47563910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:406b118562a7fad8d6cb5ebd56d606c3007c1d31422152f7a9d5141a7803798b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:25:38 GMT
ADD file:41ec53d65aa183c2835f73989c9e4922f818e59774811eaa6e7395e5a36d5eab in / 
# Tue, 09 Jun 2020 01:25:42 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 04:43:07 GMT
ENV MONO_VERSION=5.20.1.34
# Tue, 09 Jun 2020 04:44:25 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Jun 2020 04:45:52 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a29e28607c9b96acae7ff89e56214e4339a87c59e40a6f030fa4cbcaab753f2c`  
		Last Modified: Tue, 09 Jun 2020 01:37:25 GMT  
		Size: 22.8 MB (22791269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21d9971248b8a3142c8d28700658bc11b1313694441bf51b7febefd26adddbe1`  
		Last Modified: Tue, 09 Jun 2020 05:06:08 GMT  
		Size: 244.6 KB (244636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c629efc5a0d859723a7100a060a51da7cbe12ff931fcd2edcb1be81b2d112240`  
		Last Modified: Tue, 09 Jun 2020 05:06:13 GMT  
		Size: 24.5 MB (24528005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:5-slim`

```console
$ docker pull mono@sha256:7b1baf75b397d0fa3c79cfc483e0dd83ae7b40987a60d269d8d0f900def6a281
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:5-slim` - linux; amd64

```console
$ docker pull mono@sha256:16162056f6d04d68d3b297f123edad3e7bba54f4e0ee84c5cd5012610935b7c9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.2 MB (78171634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd0eab449535c70e3a40b2293d483a0213d2426f5a4a6539ce69688dca0ddee0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:23:35 GMT
ADD file:57b431451a292755d0f13673f5f3bea9f62aea36c7a1b59d34d7d200ba134fea in / 
# Tue, 09 Jun 2020 01:23:35 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 07:25:19 GMT
ENV MONO_VERSION=5.20.1.34
# Tue, 09 Jun 2020 07:25:31 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Jun 2020 07:25:58 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7d2977b12acb33f192e3f20b7e15a467cc8f3f5124a15d975a6d4afe5fa3d258`  
		Last Modified: Tue, 09 Jun 2020 01:28:13 GMT  
		Size: 22.5 MB (22519600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3a96016cede2bbab34292fab9e759f8d6e76cdccf5e984c01f8efd90e6df05b`  
		Last Modified: Tue, 09 Jun 2020 07:58:27 GMT  
		Size: 244.5 KB (244463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05a6ab00376aa34c88796f85c2d808035931da42c558e6f9ff32907a9641b062`  
		Last Modified: Tue, 09 Jun 2020 07:58:43 GMT  
		Size: 55.4 MB (55407571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:ec3602c25a4a890750685bb5f19d7a34a20516a37059153579b68a4f74f17f3d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45584292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae3c8177fa72be71e59c5119b36ba1f5f0a9099f41a0d3032bd34b486c34c3f6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 00:55:12 GMT
ADD file:0b9f2b88887a8060402a052c243c31641d9c217edcdb232c7b7a057cf5a70d66 in / 
# Wed, 22 Jul 2020 00:55:13 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 04:50:57 GMT
ENV MONO_VERSION=5.20.1.34
# Wed, 22 Jul 2020 04:51:29 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jul 2020 04:52:30 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:319109fcb6fa9b08528c518426e7ce105aac7313066432efcea95f59ff6e6788`  
		Last Modified: Wed, 22 Jul 2020 01:03:27 GMT  
		Size: 21.2 MB (21189131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:214f724afb987f92ce9133d6327bf39c60bb2f5e639abe876e341a07f439d60e`  
		Last Modified: Wed, 22 Jul 2020 05:03:20 GMT  
		Size: 244.6 KB (244590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1738e5f6ebf3cc4543e52c88b7aa0fc6f9113fabde1e2980a289aafa5559d5b1`  
		Last Modified: Wed, 22 Jul 2020 05:03:29 GMT  
		Size: 24.2 MB (24150571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:4386b149b67f32efb634322ead66cbd1af15e940a4fdbed1096cea4a7b5c0e1e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.0 MB (42996393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f18852418937a80e1446631268ee77d13a3bc5e056f76139117a44a72ecdc3ca`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 01:33:30 GMT
ADD file:49b1a1b4f5c2201b0e23e29dca24c4f6ffc14620196c4bd77770952500c4bee1 in / 
# Wed, 22 Jul 2020 01:33:38 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 02:20:07 GMT
ENV MONO_VERSION=5.20.1.34
# Wed, 22 Jul 2020 02:20:49 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jul 2020 02:21:51 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:cd38ad753522d120e27c5343b08f661ee3aebfe531d60102d7c624c16dba4d09`  
		Last Modified: Wed, 22 Jul 2020 01:44:24 GMT  
		Size: 19.3 MB (19298267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae6961338dbeec44b6e92646723bb59c030769220b24193c12f7827ce9ca826f`  
		Last Modified: Wed, 22 Jul 2020 02:33:13 GMT  
		Size: 244.6 KB (244556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:829fd514f3675f9e41ec1f1bc082852015f100014cc48e3b90e1b3023c34fa51`  
		Last Modified: Wed, 22 Jul 2020 02:33:22 GMT  
		Size: 23.5 MB (23453570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:48d8d81739bb780c0f6f54e39773ed7239fa34117e4baed155af459bdc7bb08e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48669512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4ef5ae213ee661f770b0931778cc05a349d7bac270e37715b391431cb89a305`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:54:49 GMT
ADD file:c85d28567b6123deb660b71c8b60d92378b5ba15ba5dcf495d9388817dc3aa44 in / 
# Tue, 09 Jun 2020 01:54:52 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 03:26:55 GMT
ENV MONO_VERSION=5.20.1.34
# Tue, 09 Jun 2020 03:27:13 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Jun 2020 03:27:54 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:622dc742b82743ebf5607b215a65869096390ee41b0a61b5532f859fb94590b1`  
		Last Modified: Tue, 09 Jun 2020 02:00:28 GMT  
		Size: 20.4 MB (20375150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47cfdc0a506e196319f490a8bb5e0036dd589b207aa03c9571763b3ee8dea29f`  
		Last Modified: Tue, 09 Jun 2020 03:37:36 GMT  
		Size: 244.4 KB (244372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f6b08527e586e0f80506a226402a72b5cf43e106073bc06aa87862249894d0a`  
		Last Modified: Tue, 09 Jun 2020 03:37:45 GMT  
		Size: 28.0 MB (28049990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5-slim` - linux; 386

```console
$ docker pull mono@sha256:4222a99c9b296042587b96f689ebbf6634a8d8d2c635c4cd04d351e97712e0b9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.8 MB (81832175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4614f168389960f66e555809e63b35524bfd333eae47ec3048ab9ceb067a573`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:42:33 GMT
ADD file:8ef252685ffefc58654053bf145c830928a2cf423a6c757180649df772f1523d in / 
# Tue, 09 Jun 2020 01:42:34 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 07:01:47 GMT
ENV MONO_VERSION=5.20.1.34
# Tue, 09 Jun 2020 07:02:01 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Jun 2020 07:02:35 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:4ffbd6ec7974e514763a8d7d9fcf5e86e9440e2280e6e9561ea373b4bc50588e`  
		Last Modified: Tue, 09 Jun 2020 01:48:28 GMT  
		Size: 23.1 MB (23147892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79f35120db9bc30d6de494b0e58b8a74d62fe7a85cdc188357ea98ca2797e839`  
		Last Modified: Tue, 09 Jun 2020 07:11:10 GMT  
		Size: 244.5 KB (244478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d12cec6c246292b2edce2de333f893fefd5d9460042faa8e270bfde498b21612`  
		Last Modified: Tue, 09 Jun 2020 07:11:24 GMT  
		Size: 58.4 MB (58439805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:176998bc9e1646c37ff64d0d4f385f36e1f8922f56319d19bb3c38f981738c0d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.6 MB (47563910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:406b118562a7fad8d6cb5ebd56d606c3007c1d31422152f7a9d5141a7803798b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:25:38 GMT
ADD file:41ec53d65aa183c2835f73989c9e4922f818e59774811eaa6e7395e5a36d5eab in / 
# Tue, 09 Jun 2020 01:25:42 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 04:43:07 GMT
ENV MONO_VERSION=5.20.1.34
# Tue, 09 Jun 2020 04:44:25 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Jun 2020 04:45:52 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a29e28607c9b96acae7ff89e56214e4339a87c59e40a6f030fa4cbcaab753f2c`  
		Last Modified: Tue, 09 Jun 2020 01:37:25 GMT  
		Size: 22.8 MB (22791269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21d9971248b8a3142c8d28700658bc11b1313694441bf51b7febefd26adddbe1`  
		Last Modified: Tue, 09 Jun 2020 05:06:08 GMT  
		Size: 244.6 KB (244636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c629efc5a0d859723a7100a060a51da7cbe12ff931fcd2edcb1be81b2d112240`  
		Last Modified: Tue, 09 Jun 2020 05:06:13 GMT  
		Size: 24.5 MB (24528005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6`

```console
$ docker pull mono@sha256:4edd8d6d3134e4de4f25836d12a6a9a9de23fa572846e74709b2f19f7371995a
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
$ docker pull mono@sha256:d4717190e9fd6118cb2775e2f084daf223583c24bc1f014c33dea48485bc7ff2
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.0 MB (235024583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a6baf0a892689f2f75227c4c04ab734c8497ab6853b037bb733184b2417c751`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:23:35 GMT
ADD file:57b431451a292755d0f13673f5f3bea9f62aea36c7a1b59d34d7d200ba134fea in / 
# Tue, 09 Jun 2020 01:23:35 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 07:23:45 GMT
ENV MONO_VERSION=6.8.0.96
# Tue, 09 Jun 2020 07:23:55 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Jun 2020 07:24:27 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 09 Jun 2020 07:36:17 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7d2977b12acb33f192e3f20b7e15a467cc8f3f5124a15d975a6d4afe5fa3d258`  
		Last Modified: Tue, 09 Jun 2020 01:28:13 GMT  
		Size: 22.5 MB (22519600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:086ef7a7e886327a728a6c520ae895632459590d19d2691114827740ae2f70e8`  
		Last Modified: Tue, 09 Jun 2020 07:57:38 GMT  
		Size: 244.5 KB (244473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28855cf8f97ad7e71803802cd6b3c77cc8335c628b34fc3f6283688061cdad11`  
		Last Modified: Tue, 09 Jun 2020 07:57:56 GMT  
		Size: 64.5 MB (64467452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e1b1cfd1a055e22c600005e10f64b8b2b3557bff82aa4bc012ab66cb8786346`  
		Last Modified: Tue, 09 Jun 2020 07:59:31 GMT  
		Size: 147.8 MB (147793058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6` - linux; arm variant v5

```console
$ docker pull mono@sha256:899467182dd8b6e055181cdce28cc3cae6935b0d914393224be26af46629c004
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.6 MB (176588520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42bd2219f249736535bcd1ba211ff5d352edc655fe81450544fbb344fc18b015`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 00:55:12 GMT
ADD file:0b9f2b88887a8060402a052c243c31641d9c217edcdb232c7b7a057cf5a70d66 in / 
# Wed, 22 Jul 2020 00:55:13 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 04:47:49 GMT
ENV MONO_VERSION=6.8.0.96
# Wed, 22 Jul 2020 04:48:12 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jul 2020 04:49:00 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 22 Jul 2020 04:55:31 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:319109fcb6fa9b08528c518426e7ce105aac7313066432efcea95f59ff6e6788`  
		Last Modified: Wed, 22 Jul 2020 01:03:27 GMT  
		Size: 21.2 MB (21189131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a62cce824a648193694f4121faf883e003fd11739ec85458d954e3cf0f8860ec`  
		Last Modified: Wed, 22 Jul 2020 05:02:47 GMT  
		Size: 244.5 KB (244541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f82e724d353f93153e6d1203349f4b687bc703c55e3b1cc2438b3ffad6974124`  
		Last Modified: Wed, 22 Jul 2020 05:02:55 GMT  
		Size: 25.3 MB (25253549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:225b191f3416f0c2fd00c0c702d8819f8c61a0faece5b5d2dcb4815b23191907`  
		Last Modified: Wed, 22 Jul 2020 05:04:19 GMT  
		Size: 129.9 MB (129901299 bytes)  
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
$ docker pull mono@sha256:68d1db7da63e2106ddea8d7850cf3badfaa16a94d8d23a12910f86785e4decc8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.6 MB (194642181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf6ff587bef5367449ceee09405f75d3b5a38e19c0d360ec43da1874b37497aa`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:54:49 GMT
ADD file:c85d28567b6123deb660b71c8b60d92378b5ba15ba5dcf495d9388817dc3aa44 in / 
# Tue, 09 Jun 2020 01:54:52 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 03:24:02 GMT
ENV MONO_VERSION=6.8.0.96
# Tue, 09 Jun 2020 03:24:21 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Jun 2020 03:25:06 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 09 Jun 2020 03:30:31 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:622dc742b82743ebf5607b215a65869096390ee41b0a61b5532f859fb94590b1`  
		Last Modified: Tue, 09 Jun 2020 02:00:28 GMT  
		Size: 20.4 MB (20375150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:334cf34398cfa7031d68bad42f6b2a8d870a4ad5c2b0454f3f6fdd0fb4433237`  
		Last Modified: Tue, 09 Jun 2020 03:37:02 GMT  
		Size: 244.4 KB (244374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aa8cbd821b66a8c4a38ce3d6711cc1ee5489b04a017ab6a7fd368f08beec89e`  
		Last Modified: Tue, 09 Jun 2020 03:37:10 GMT  
		Size: 29.3 MB (29310269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f78bf65ea03cc9db2213ce7ff8e07d3a77604a43ef0a7d81b88b5c965515dfe`  
		Last Modified: Tue, 09 Jun 2020 03:38:38 GMT  
		Size: 144.7 MB (144712388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6` - linux; 386

```console
$ docker pull mono@sha256:443376dd685b5fcd1e0b6b7a685c5b6a24a79fad8b9619e983293b70e84c8bb6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.4 MB (243401430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6948fdbf966360cb7a728eae30756da2daa5cc4b0362dd09e3a352f4ee44e5dc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:42:33 GMT
ADD file:8ef252685ffefc58654053bf145c830928a2cf423a6c757180649df772f1523d in / 
# Tue, 09 Jun 2020 01:42:34 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 06:59:35 GMT
ENV MONO_VERSION=6.8.0.96
# Tue, 09 Jun 2020 06:59:46 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Jun 2020 07:00:24 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 09 Jun 2020 07:05:03 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:4ffbd6ec7974e514763a8d7d9fcf5e86e9440e2280e6e9561ea373b4bc50588e`  
		Last Modified: Tue, 09 Jun 2020 01:48:28 GMT  
		Size: 23.1 MB (23147892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b3a90700548ab3df378beb07af7fba67e7ea89ead888d8c78d529c40633c7ed`  
		Last Modified: Tue, 09 Jun 2020 07:10:23 GMT  
		Size: 244.5 KB (244462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbcec5e4a352eead9b06946ed8fb1855a57123b280b3941614dac805987d5b65`  
		Last Modified: Tue, 09 Jun 2020 07:10:41 GMT  
		Size: 68.5 MB (68517280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae8167823b3a297ca26719112fd4ae0b1b90e5df5ef7edf3302022c64061697f`  
		Last Modified: Tue, 09 Jun 2020 07:12:09 GMT  
		Size: 151.5 MB (151491796 bytes)  
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

## `mono:6.6`

```console
$ docker pull mono@sha256:9b624a751c19431ab8e4e757a9d2e64fedebefd580fd0873ff786558c1cd324a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:6.6` - linux; amd64

```console
$ docker pull mono@sha256:8bb8e48079657895c96840430c4c9e736a4767e96df524faac86712be54512d9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.9 MB (232916901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fae3c0f53e86b63bfc2d0ddba5f788153818be13839c70c8dfb9540e64826fe`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:23:35 GMT
ADD file:57b431451a292755d0f13673f5f3bea9f62aea36c7a1b59d34d7d200ba134fea in / 
# Tue, 09 Jun 2020 01:23:35 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 07:24:32 GMT
ENV MONO_VERSION=6.6.0.161
# Tue, 09 Jun 2020 07:24:42 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Jun 2020 07:25:14 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 09 Jun 2020 07:47:35 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7d2977b12acb33f192e3f20b7e15a467cc8f3f5124a15d975a6d4afe5fa3d258`  
		Last Modified: Tue, 09 Jun 2020 01:28:13 GMT  
		Size: 22.5 MB (22519600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20c821ecf18976f07ebc44d5e8f60b56baf477680dd1e8b7b20a095ce6b0fe2a`  
		Last Modified: Tue, 09 Jun 2020 07:58:03 GMT  
		Size: 244.5 KB (244473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57b71e1fdcdf5a134a49b7b4375e7c683147eb59f6c09717238e01135cdd7e40`  
		Last Modified: Tue, 09 Jun 2020 07:58:21 GMT  
		Size: 62.8 MB (62846142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d47b0ac9af5c17359b4579fd7d0b5b32015c5ae71d0b9a0aea6de5d2609c6f7`  
		Last Modified: Tue, 09 Jun 2020 08:00:16 GMT  
		Size: 147.3 MB (147306686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6` - linux; arm variant v5

```console
$ docker pull mono@sha256:e9c8877f6252ba146b8fc2a50afe0dc671febbaf9d9a17ff6453aee83baf5744
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.4 MB (176397416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b28d8cab6597c4fe5553208f72ec92e949a5a8f976ca8ce74bdd3bfbae497da`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 00:55:12 GMT
ADD file:0b9f2b88887a8060402a052c243c31641d9c217edcdb232c7b7a057cf5a70d66 in / 
# Wed, 22 Jul 2020 00:55:13 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 04:49:08 GMT
ENV MONO_VERSION=6.6.0.161
# Wed, 22 Jul 2020 04:49:43 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jul 2020 04:50:49 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 22 Jul 2020 04:58:35 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:319109fcb6fa9b08528c518426e7ce105aac7313066432efcea95f59ff6e6788`  
		Last Modified: Wed, 22 Jul 2020 01:03:27 GMT  
		Size: 21.2 MB (21189131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80846289d34adc8ed8a1ce2ab050633f8d9d1c16defa48525d5ffb4cfae0849a`  
		Last Modified: Wed, 22 Jul 2020 05:03:04 GMT  
		Size: 244.6 KB (244586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9fafd2cc65b4de32fff13f1e5aa9b86cf7162bfbadb5082fb9eb5cc0d817172`  
		Last Modified: Wed, 22 Jul 2020 05:03:13 GMT  
		Size: 25.3 MB (25308019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb7945a48c50dabaec415a31a0e2c642c7c5ea31d3ee16ecba5d3b742bd72862`  
		Last Modified: Wed, 22 Jul 2020 05:05:16 GMT  
		Size: 129.7 MB (129655680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6` - linux; arm variant v7

```console
$ docker pull mono@sha256:b1b3c548af184e85697fe37e5d839ee2de388225878eac29bcbee7d26134d4c7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.4 MB (172400396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a28c375e6458278e60b860d0041642d8529ac570fdae8843fb3c35a337cb9885`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 01:33:30 GMT
ADD file:49b1a1b4f5c2201b0e23e29dca24c4f6ffc14620196c4bd77770952500c4bee1 in / 
# Wed, 22 Jul 2020 01:33:38 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 02:17:29 GMT
ENV MONO_VERSION=6.6.0.161
# Wed, 22 Jul 2020 02:18:15 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jul 2020 02:19:37 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 22 Jul 2020 02:28:29 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:cd38ad753522d120e27c5343b08f661ee3aebfe531d60102d7c624c16dba4d09`  
		Last Modified: Wed, 22 Jul 2020 01:44:24 GMT  
		Size: 19.3 MB (19298267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b2680436a276aad21c6a0cca92c394a14e7525ef975ef46d35a8992d89e1257`  
		Last Modified: Wed, 22 Jul 2020 02:32:51 GMT  
		Size: 244.6 KB (244560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d961717bb11902ebe7f61b28efbaad39e135b491ea8b0251b94bcd51baebe8f4`  
		Last Modified: Wed, 22 Jul 2020 02:33:00 GMT  
		Size: 24.5 MB (24543391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eb896732fd25681bd9250272a5771be5ab421113a908ebd0a0b9bcfbd6d3880`  
		Last Modified: Wed, 22 Jul 2020 02:35:17 GMT  
		Size: 128.3 MB (128314178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:9ed842b0a7ac3cef21acce0287ae5ca88394337f09b62fa6db65b5363caff541
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.3 MB (194286054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01dcc3513017fae48738d43fcc06c221afbb7fdef66f67b4e66f956af21fba59`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:54:49 GMT
ADD file:c85d28567b6123deb660b71c8b60d92378b5ba15ba5dcf495d9388817dc3aa44 in / 
# Tue, 09 Jun 2020 01:54:52 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 03:25:21 GMT
ENV MONO_VERSION=6.6.0.161
# Tue, 09 Jun 2020 03:25:41 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Jun 2020 03:26:31 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 09 Jun 2020 03:33:33 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:622dc742b82743ebf5607b215a65869096390ee41b0a61b5532f859fb94590b1`  
		Last Modified: Tue, 09 Jun 2020 02:00:28 GMT  
		Size: 20.4 MB (20375150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4290c2f990444deb0f93dd0ba68fc5d94357ce1cfdb252dec480eb8dc62df72`  
		Last Modified: Tue, 09 Jun 2020 03:37:19 GMT  
		Size: 244.4 KB (244381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f7365212009d85dfb9bd0fefee678ef2259929ed35a819d5d1d63931c29d142`  
		Last Modified: Tue, 09 Jun 2020 03:37:29 GMT  
		Size: 29.3 MB (29326238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a51ebbe9cd667dc8e9df498e44d5deeb4bac46ee95d4178ba191cd683a7b0224`  
		Last Modified: Tue, 09 Jun 2020 03:39:31 GMT  
		Size: 144.3 MB (144340285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6` - linux; 386

```console
$ docker pull mono@sha256:b9fda283e13398b40025d4368ac714e986347671b79ca74e5cca1d62d624730c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.2 MB (241191319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:219f26f416326e6efb9890d9950166c794593974d0ff38adc4c61421c81d6265`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:42:33 GMT
ADD file:8ef252685ffefc58654053bf145c830928a2cf423a6c757180649df772f1523d in / 
# Tue, 09 Jun 2020 01:42:34 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 07:00:31 GMT
ENV MONO_VERSION=6.6.0.161
# Tue, 09 Jun 2020 07:00:43 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Jun 2020 07:01:34 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 09 Jun 2020 07:07:35 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:4ffbd6ec7974e514763a8d7d9fcf5e86e9440e2280e6e9561ea373b4bc50588e`  
		Last Modified: Tue, 09 Jun 2020 01:48:28 GMT  
		Size: 23.1 MB (23147892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dac86da952cf07d4efdc128f7ad526f39026bebd6fd96ce97f984d213ff33beb`  
		Last Modified: Tue, 09 Jun 2020 07:10:48 GMT  
		Size: 244.5 KB (244473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44aea1cbf2eb9bf3490c39e0036b585c6bd70cb027e4d67779122b5337b7eec8`  
		Last Modified: Tue, 09 Jun 2020 07:11:04 GMT  
		Size: 66.6 MB (66638665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c53f7b67e9ddb24f8be1459afa90a46f0c2d0fab6eb67b6e0113781b8a896b8e`  
		Last Modified: Tue, 09 Jun 2020 07:12:55 GMT  
		Size: 151.2 MB (151160289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6` - linux; ppc64le

```console
$ docker pull mono@sha256:c0eb7651cb590936ee508d9f2c9118e01890e604f4ea77eb9f09f4a747b0267a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.7 MB (178692095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d66a6cad95995cff3f64cf89aab342aab7fc0ae29ec2b3cfc6b732b6c326a80`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:25:38 GMT
ADD file:41ec53d65aa183c2835f73989c9e4922f818e59774811eaa6e7395e5a36d5eab in / 
# Tue, 09 Jun 2020 01:25:42 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 04:40:54 GMT
ENV MONO_VERSION=6.6.0.161
# Tue, 09 Jun 2020 04:41:50 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Jun 2020 04:42:57 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 09 Jun 2020 04:57:13 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a29e28607c9b96acae7ff89e56214e4339a87c59e40a6f030fa4cbcaab753f2c`  
		Last Modified: Tue, 09 Jun 2020 01:37:25 GMT  
		Size: 22.8 MB (22791269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79f61e53535e34c8ba847db7a0b997284c1aa54e60b26ed23e5bfa4cab2fcd91`  
		Last Modified: Tue, 09 Jun 2020 05:05:48 GMT  
		Size: 244.6 KB (244568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:563625e3974512d700bb578934524f8dbbb23413ac33824ac5c60129e7c109d7`  
		Last Modified: Tue, 09 Jun 2020 05:05:55 GMT  
		Size: 25.7 MB (25715556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d60af5c37498a2f246576decb845b382d75e96ceac5eea1f395585d7eebca979`  
		Last Modified: Tue, 09 Jun 2020 05:07:41 GMT  
		Size: 129.9 MB (129940702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.6.0`

```console
$ docker pull mono@sha256:9b624a751c19431ab8e4e757a9d2e64fedebefd580fd0873ff786558c1cd324a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:6.6.0` - linux; amd64

```console
$ docker pull mono@sha256:8bb8e48079657895c96840430c4c9e736a4767e96df524faac86712be54512d9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.9 MB (232916901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fae3c0f53e86b63bfc2d0ddba5f788153818be13839c70c8dfb9540e64826fe`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:23:35 GMT
ADD file:57b431451a292755d0f13673f5f3bea9f62aea36c7a1b59d34d7d200ba134fea in / 
# Tue, 09 Jun 2020 01:23:35 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 07:24:32 GMT
ENV MONO_VERSION=6.6.0.161
# Tue, 09 Jun 2020 07:24:42 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Jun 2020 07:25:14 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 09 Jun 2020 07:47:35 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7d2977b12acb33f192e3f20b7e15a467cc8f3f5124a15d975a6d4afe5fa3d258`  
		Last Modified: Tue, 09 Jun 2020 01:28:13 GMT  
		Size: 22.5 MB (22519600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20c821ecf18976f07ebc44d5e8f60b56baf477680dd1e8b7b20a095ce6b0fe2a`  
		Last Modified: Tue, 09 Jun 2020 07:58:03 GMT  
		Size: 244.5 KB (244473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57b71e1fdcdf5a134a49b7b4375e7c683147eb59f6c09717238e01135cdd7e40`  
		Last Modified: Tue, 09 Jun 2020 07:58:21 GMT  
		Size: 62.8 MB (62846142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d47b0ac9af5c17359b4579fd7d0b5b32015c5ae71d0b9a0aea6de5d2609c6f7`  
		Last Modified: Tue, 09 Jun 2020 08:00:16 GMT  
		Size: 147.3 MB (147306686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6.0` - linux; arm variant v5

```console
$ docker pull mono@sha256:e9c8877f6252ba146b8fc2a50afe0dc671febbaf9d9a17ff6453aee83baf5744
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.4 MB (176397416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b28d8cab6597c4fe5553208f72ec92e949a5a8f976ca8ce74bdd3bfbae497da`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 00:55:12 GMT
ADD file:0b9f2b88887a8060402a052c243c31641d9c217edcdb232c7b7a057cf5a70d66 in / 
# Wed, 22 Jul 2020 00:55:13 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 04:49:08 GMT
ENV MONO_VERSION=6.6.0.161
# Wed, 22 Jul 2020 04:49:43 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jul 2020 04:50:49 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 22 Jul 2020 04:58:35 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:319109fcb6fa9b08528c518426e7ce105aac7313066432efcea95f59ff6e6788`  
		Last Modified: Wed, 22 Jul 2020 01:03:27 GMT  
		Size: 21.2 MB (21189131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80846289d34adc8ed8a1ce2ab050633f8d9d1c16defa48525d5ffb4cfae0849a`  
		Last Modified: Wed, 22 Jul 2020 05:03:04 GMT  
		Size: 244.6 KB (244586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9fafd2cc65b4de32fff13f1e5aa9b86cf7162bfbadb5082fb9eb5cc0d817172`  
		Last Modified: Wed, 22 Jul 2020 05:03:13 GMT  
		Size: 25.3 MB (25308019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb7945a48c50dabaec415a31a0e2c642c7c5ea31d3ee16ecba5d3b742bd72862`  
		Last Modified: Wed, 22 Jul 2020 05:05:16 GMT  
		Size: 129.7 MB (129655680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6.0` - linux; arm variant v7

```console
$ docker pull mono@sha256:b1b3c548af184e85697fe37e5d839ee2de388225878eac29bcbee7d26134d4c7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.4 MB (172400396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a28c375e6458278e60b860d0041642d8529ac570fdae8843fb3c35a337cb9885`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 01:33:30 GMT
ADD file:49b1a1b4f5c2201b0e23e29dca24c4f6ffc14620196c4bd77770952500c4bee1 in / 
# Wed, 22 Jul 2020 01:33:38 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 02:17:29 GMT
ENV MONO_VERSION=6.6.0.161
# Wed, 22 Jul 2020 02:18:15 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jul 2020 02:19:37 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 22 Jul 2020 02:28:29 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:cd38ad753522d120e27c5343b08f661ee3aebfe531d60102d7c624c16dba4d09`  
		Last Modified: Wed, 22 Jul 2020 01:44:24 GMT  
		Size: 19.3 MB (19298267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b2680436a276aad21c6a0cca92c394a14e7525ef975ef46d35a8992d89e1257`  
		Last Modified: Wed, 22 Jul 2020 02:32:51 GMT  
		Size: 244.6 KB (244560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d961717bb11902ebe7f61b28efbaad39e135b491ea8b0251b94bcd51baebe8f4`  
		Last Modified: Wed, 22 Jul 2020 02:33:00 GMT  
		Size: 24.5 MB (24543391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eb896732fd25681bd9250272a5771be5ab421113a908ebd0a0b9bcfbd6d3880`  
		Last Modified: Wed, 22 Jul 2020 02:35:17 GMT  
		Size: 128.3 MB (128314178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6.0` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:9ed842b0a7ac3cef21acce0287ae5ca88394337f09b62fa6db65b5363caff541
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.3 MB (194286054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01dcc3513017fae48738d43fcc06c221afbb7fdef66f67b4e66f956af21fba59`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:54:49 GMT
ADD file:c85d28567b6123deb660b71c8b60d92378b5ba15ba5dcf495d9388817dc3aa44 in / 
# Tue, 09 Jun 2020 01:54:52 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 03:25:21 GMT
ENV MONO_VERSION=6.6.0.161
# Tue, 09 Jun 2020 03:25:41 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Jun 2020 03:26:31 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 09 Jun 2020 03:33:33 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:622dc742b82743ebf5607b215a65869096390ee41b0a61b5532f859fb94590b1`  
		Last Modified: Tue, 09 Jun 2020 02:00:28 GMT  
		Size: 20.4 MB (20375150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4290c2f990444deb0f93dd0ba68fc5d94357ce1cfdb252dec480eb8dc62df72`  
		Last Modified: Tue, 09 Jun 2020 03:37:19 GMT  
		Size: 244.4 KB (244381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f7365212009d85dfb9bd0fefee678ef2259929ed35a819d5d1d63931c29d142`  
		Last Modified: Tue, 09 Jun 2020 03:37:29 GMT  
		Size: 29.3 MB (29326238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a51ebbe9cd667dc8e9df498e44d5deeb4bac46ee95d4178ba191cd683a7b0224`  
		Last Modified: Tue, 09 Jun 2020 03:39:31 GMT  
		Size: 144.3 MB (144340285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6.0` - linux; 386

```console
$ docker pull mono@sha256:b9fda283e13398b40025d4368ac714e986347671b79ca74e5cca1d62d624730c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.2 MB (241191319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:219f26f416326e6efb9890d9950166c794593974d0ff38adc4c61421c81d6265`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:42:33 GMT
ADD file:8ef252685ffefc58654053bf145c830928a2cf423a6c757180649df772f1523d in / 
# Tue, 09 Jun 2020 01:42:34 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 07:00:31 GMT
ENV MONO_VERSION=6.6.0.161
# Tue, 09 Jun 2020 07:00:43 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Jun 2020 07:01:34 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 09 Jun 2020 07:07:35 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:4ffbd6ec7974e514763a8d7d9fcf5e86e9440e2280e6e9561ea373b4bc50588e`  
		Last Modified: Tue, 09 Jun 2020 01:48:28 GMT  
		Size: 23.1 MB (23147892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dac86da952cf07d4efdc128f7ad526f39026bebd6fd96ce97f984d213ff33beb`  
		Last Modified: Tue, 09 Jun 2020 07:10:48 GMT  
		Size: 244.5 KB (244473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44aea1cbf2eb9bf3490c39e0036b585c6bd70cb027e4d67779122b5337b7eec8`  
		Last Modified: Tue, 09 Jun 2020 07:11:04 GMT  
		Size: 66.6 MB (66638665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c53f7b67e9ddb24f8be1459afa90a46f0c2d0fab6eb67b6e0113781b8a896b8e`  
		Last Modified: Tue, 09 Jun 2020 07:12:55 GMT  
		Size: 151.2 MB (151160289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6.0` - linux; ppc64le

```console
$ docker pull mono@sha256:c0eb7651cb590936ee508d9f2c9118e01890e604f4ea77eb9f09f4a747b0267a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.7 MB (178692095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d66a6cad95995cff3f64cf89aab342aab7fc0ae29ec2b3cfc6b732b6c326a80`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:25:38 GMT
ADD file:41ec53d65aa183c2835f73989c9e4922f818e59774811eaa6e7395e5a36d5eab in / 
# Tue, 09 Jun 2020 01:25:42 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 04:40:54 GMT
ENV MONO_VERSION=6.6.0.161
# Tue, 09 Jun 2020 04:41:50 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Jun 2020 04:42:57 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 09 Jun 2020 04:57:13 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a29e28607c9b96acae7ff89e56214e4339a87c59e40a6f030fa4cbcaab753f2c`  
		Last Modified: Tue, 09 Jun 2020 01:37:25 GMT  
		Size: 22.8 MB (22791269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79f61e53535e34c8ba847db7a0b997284c1aa54e60b26ed23e5bfa4cab2fcd91`  
		Last Modified: Tue, 09 Jun 2020 05:05:48 GMT  
		Size: 244.6 KB (244568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:563625e3974512d700bb578934524f8dbbb23413ac33824ac5c60129e7c109d7`  
		Last Modified: Tue, 09 Jun 2020 05:05:55 GMT  
		Size: 25.7 MB (25715556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d60af5c37498a2f246576decb845b382d75e96ceac5eea1f395585d7eebca979`  
		Last Modified: Tue, 09 Jun 2020 05:07:41 GMT  
		Size: 129.9 MB (129940702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.6.0.161`

```console
$ docker pull mono@sha256:9b624a751c19431ab8e4e757a9d2e64fedebefd580fd0873ff786558c1cd324a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:6.6.0.161` - linux; amd64

```console
$ docker pull mono@sha256:8bb8e48079657895c96840430c4c9e736a4767e96df524faac86712be54512d9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.9 MB (232916901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fae3c0f53e86b63bfc2d0ddba5f788153818be13839c70c8dfb9540e64826fe`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:23:35 GMT
ADD file:57b431451a292755d0f13673f5f3bea9f62aea36c7a1b59d34d7d200ba134fea in / 
# Tue, 09 Jun 2020 01:23:35 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 07:24:32 GMT
ENV MONO_VERSION=6.6.0.161
# Tue, 09 Jun 2020 07:24:42 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Jun 2020 07:25:14 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 09 Jun 2020 07:47:35 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7d2977b12acb33f192e3f20b7e15a467cc8f3f5124a15d975a6d4afe5fa3d258`  
		Last Modified: Tue, 09 Jun 2020 01:28:13 GMT  
		Size: 22.5 MB (22519600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20c821ecf18976f07ebc44d5e8f60b56baf477680dd1e8b7b20a095ce6b0fe2a`  
		Last Modified: Tue, 09 Jun 2020 07:58:03 GMT  
		Size: 244.5 KB (244473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57b71e1fdcdf5a134a49b7b4375e7c683147eb59f6c09717238e01135cdd7e40`  
		Last Modified: Tue, 09 Jun 2020 07:58:21 GMT  
		Size: 62.8 MB (62846142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d47b0ac9af5c17359b4579fd7d0b5b32015c5ae71d0b9a0aea6de5d2609c6f7`  
		Last Modified: Tue, 09 Jun 2020 08:00:16 GMT  
		Size: 147.3 MB (147306686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6.0.161` - linux; arm variant v5

```console
$ docker pull mono@sha256:e9c8877f6252ba146b8fc2a50afe0dc671febbaf9d9a17ff6453aee83baf5744
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.4 MB (176397416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b28d8cab6597c4fe5553208f72ec92e949a5a8f976ca8ce74bdd3bfbae497da`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 00:55:12 GMT
ADD file:0b9f2b88887a8060402a052c243c31641d9c217edcdb232c7b7a057cf5a70d66 in / 
# Wed, 22 Jul 2020 00:55:13 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 04:49:08 GMT
ENV MONO_VERSION=6.6.0.161
# Wed, 22 Jul 2020 04:49:43 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jul 2020 04:50:49 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 22 Jul 2020 04:58:35 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:319109fcb6fa9b08528c518426e7ce105aac7313066432efcea95f59ff6e6788`  
		Last Modified: Wed, 22 Jul 2020 01:03:27 GMT  
		Size: 21.2 MB (21189131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80846289d34adc8ed8a1ce2ab050633f8d9d1c16defa48525d5ffb4cfae0849a`  
		Last Modified: Wed, 22 Jul 2020 05:03:04 GMT  
		Size: 244.6 KB (244586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9fafd2cc65b4de32fff13f1e5aa9b86cf7162bfbadb5082fb9eb5cc0d817172`  
		Last Modified: Wed, 22 Jul 2020 05:03:13 GMT  
		Size: 25.3 MB (25308019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb7945a48c50dabaec415a31a0e2c642c7c5ea31d3ee16ecba5d3b742bd72862`  
		Last Modified: Wed, 22 Jul 2020 05:05:16 GMT  
		Size: 129.7 MB (129655680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6.0.161` - linux; arm variant v7

```console
$ docker pull mono@sha256:b1b3c548af184e85697fe37e5d839ee2de388225878eac29bcbee7d26134d4c7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.4 MB (172400396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a28c375e6458278e60b860d0041642d8529ac570fdae8843fb3c35a337cb9885`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 01:33:30 GMT
ADD file:49b1a1b4f5c2201b0e23e29dca24c4f6ffc14620196c4bd77770952500c4bee1 in / 
# Wed, 22 Jul 2020 01:33:38 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 02:17:29 GMT
ENV MONO_VERSION=6.6.0.161
# Wed, 22 Jul 2020 02:18:15 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jul 2020 02:19:37 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 22 Jul 2020 02:28:29 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:cd38ad753522d120e27c5343b08f661ee3aebfe531d60102d7c624c16dba4d09`  
		Last Modified: Wed, 22 Jul 2020 01:44:24 GMT  
		Size: 19.3 MB (19298267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b2680436a276aad21c6a0cca92c394a14e7525ef975ef46d35a8992d89e1257`  
		Last Modified: Wed, 22 Jul 2020 02:32:51 GMT  
		Size: 244.6 KB (244560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d961717bb11902ebe7f61b28efbaad39e135b491ea8b0251b94bcd51baebe8f4`  
		Last Modified: Wed, 22 Jul 2020 02:33:00 GMT  
		Size: 24.5 MB (24543391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eb896732fd25681bd9250272a5771be5ab421113a908ebd0a0b9bcfbd6d3880`  
		Last Modified: Wed, 22 Jul 2020 02:35:17 GMT  
		Size: 128.3 MB (128314178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6.0.161` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:9ed842b0a7ac3cef21acce0287ae5ca88394337f09b62fa6db65b5363caff541
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.3 MB (194286054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01dcc3513017fae48738d43fcc06c221afbb7fdef66f67b4e66f956af21fba59`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:54:49 GMT
ADD file:c85d28567b6123deb660b71c8b60d92378b5ba15ba5dcf495d9388817dc3aa44 in / 
# Tue, 09 Jun 2020 01:54:52 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 03:25:21 GMT
ENV MONO_VERSION=6.6.0.161
# Tue, 09 Jun 2020 03:25:41 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Jun 2020 03:26:31 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 09 Jun 2020 03:33:33 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:622dc742b82743ebf5607b215a65869096390ee41b0a61b5532f859fb94590b1`  
		Last Modified: Tue, 09 Jun 2020 02:00:28 GMT  
		Size: 20.4 MB (20375150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4290c2f990444deb0f93dd0ba68fc5d94357ce1cfdb252dec480eb8dc62df72`  
		Last Modified: Tue, 09 Jun 2020 03:37:19 GMT  
		Size: 244.4 KB (244381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f7365212009d85dfb9bd0fefee678ef2259929ed35a819d5d1d63931c29d142`  
		Last Modified: Tue, 09 Jun 2020 03:37:29 GMT  
		Size: 29.3 MB (29326238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a51ebbe9cd667dc8e9df498e44d5deeb4bac46ee95d4178ba191cd683a7b0224`  
		Last Modified: Tue, 09 Jun 2020 03:39:31 GMT  
		Size: 144.3 MB (144340285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6.0.161` - linux; 386

```console
$ docker pull mono@sha256:b9fda283e13398b40025d4368ac714e986347671b79ca74e5cca1d62d624730c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.2 MB (241191319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:219f26f416326e6efb9890d9950166c794593974d0ff38adc4c61421c81d6265`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:42:33 GMT
ADD file:8ef252685ffefc58654053bf145c830928a2cf423a6c757180649df772f1523d in / 
# Tue, 09 Jun 2020 01:42:34 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 07:00:31 GMT
ENV MONO_VERSION=6.6.0.161
# Tue, 09 Jun 2020 07:00:43 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Jun 2020 07:01:34 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 09 Jun 2020 07:07:35 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:4ffbd6ec7974e514763a8d7d9fcf5e86e9440e2280e6e9561ea373b4bc50588e`  
		Last Modified: Tue, 09 Jun 2020 01:48:28 GMT  
		Size: 23.1 MB (23147892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dac86da952cf07d4efdc128f7ad526f39026bebd6fd96ce97f984d213ff33beb`  
		Last Modified: Tue, 09 Jun 2020 07:10:48 GMT  
		Size: 244.5 KB (244473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44aea1cbf2eb9bf3490c39e0036b585c6bd70cb027e4d67779122b5337b7eec8`  
		Last Modified: Tue, 09 Jun 2020 07:11:04 GMT  
		Size: 66.6 MB (66638665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c53f7b67e9ddb24f8be1459afa90a46f0c2d0fab6eb67b6e0113781b8a896b8e`  
		Last Modified: Tue, 09 Jun 2020 07:12:55 GMT  
		Size: 151.2 MB (151160289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6.0.161` - linux; ppc64le

```console
$ docker pull mono@sha256:c0eb7651cb590936ee508d9f2c9118e01890e604f4ea77eb9f09f4a747b0267a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.7 MB (178692095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d66a6cad95995cff3f64cf89aab342aab7fc0ae29ec2b3cfc6b732b6c326a80`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:25:38 GMT
ADD file:41ec53d65aa183c2835f73989c9e4922f818e59774811eaa6e7395e5a36d5eab in / 
# Tue, 09 Jun 2020 01:25:42 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 04:40:54 GMT
ENV MONO_VERSION=6.6.0.161
# Tue, 09 Jun 2020 04:41:50 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Jun 2020 04:42:57 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 09 Jun 2020 04:57:13 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a29e28607c9b96acae7ff89e56214e4339a87c59e40a6f030fa4cbcaab753f2c`  
		Last Modified: Tue, 09 Jun 2020 01:37:25 GMT  
		Size: 22.8 MB (22791269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79f61e53535e34c8ba847db7a0b997284c1aa54e60b26ed23e5bfa4cab2fcd91`  
		Last Modified: Tue, 09 Jun 2020 05:05:48 GMT  
		Size: 244.6 KB (244568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:563625e3974512d700bb578934524f8dbbb23413ac33824ac5c60129e7c109d7`  
		Last Modified: Tue, 09 Jun 2020 05:05:55 GMT  
		Size: 25.7 MB (25715556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d60af5c37498a2f246576decb845b382d75e96ceac5eea1f395585d7eebca979`  
		Last Modified: Tue, 09 Jun 2020 05:07:41 GMT  
		Size: 129.9 MB (129940702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.6.0.161-slim`

```console
$ docker pull mono@sha256:582138ec5465d837705c24321d7dcdb63806e22407483fc5a7b974b978b15140
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:6.6.0.161-slim` - linux; amd64

```console
$ docker pull mono@sha256:724f93d88c54fc788bc87dbc6931739df3dbb2b65c7206065f3194317a59a9ee
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.6 MB (85610215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c852ee32c5901bfbb43906406f35f1b7eaf9ed3e2f6a67c3b3c7c8c59be8fa4e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:23:35 GMT
ADD file:57b431451a292755d0f13673f5f3bea9f62aea36c7a1b59d34d7d200ba134fea in / 
# Tue, 09 Jun 2020 01:23:35 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 07:24:32 GMT
ENV MONO_VERSION=6.6.0.161
# Tue, 09 Jun 2020 07:24:42 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Jun 2020 07:25:14 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7d2977b12acb33f192e3f20b7e15a467cc8f3f5124a15d975a6d4afe5fa3d258`  
		Last Modified: Tue, 09 Jun 2020 01:28:13 GMT  
		Size: 22.5 MB (22519600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20c821ecf18976f07ebc44d5e8f60b56baf477680dd1e8b7b20a095ce6b0fe2a`  
		Last Modified: Tue, 09 Jun 2020 07:58:03 GMT  
		Size: 244.5 KB (244473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57b71e1fdcdf5a134a49b7b4375e7c683147eb59f6c09717238e01135cdd7e40`  
		Last Modified: Tue, 09 Jun 2020 07:58:21 GMT  
		Size: 62.8 MB (62846142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6.0.161-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:76c9a8aa860d3832e3f1f33cd7f6429459bd33cdc24a5e80f0fb867a012c777d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.7 MB (46741736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4c26f6eeec8140f621d9560fe9ccf3fe4bab827488eb10b4d49f1bb374e6f6b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 00:55:12 GMT
ADD file:0b9f2b88887a8060402a052c243c31641d9c217edcdb232c7b7a057cf5a70d66 in / 
# Wed, 22 Jul 2020 00:55:13 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 04:49:08 GMT
ENV MONO_VERSION=6.6.0.161
# Wed, 22 Jul 2020 04:49:43 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jul 2020 04:50:49 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:319109fcb6fa9b08528c518426e7ce105aac7313066432efcea95f59ff6e6788`  
		Last Modified: Wed, 22 Jul 2020 01:03:27 GMT  
		Size: 21.2 MB (21189131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80846289d34adc8ed8a1ce2ab050633f8d9d1c16defa48525d5ffb4cfae0849a`  
		Last Modified: Wed, 22 Jul 2020 05:03:04 GMT  
		Size: 244.6 KB (244586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9fafd2cc65b4de32fff13f1e5aa9b86cf7162bfbadb5082fb9eb5cc0d817172`  
		Last Modified: Wed, 22 Jul 2020 05:03:13 GMT  
		Size: 25.3 MB (25308019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6.0.161-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:4021746b21e557dd685768996f96e6e40bd2453921df6a7d1344253a9af213ed
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.1 MB (44086218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fcf4d17a831f0d4a17972f1c4ef71a2d8223efba3969c6e7e9a0c8900f8e878`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 01:33:30 GMT
ADD file:49b1a1b4f5c2201b0e23e29dca24c4f6ffc14620196c4bd77770952500c4bee1 in / 
# Wed, 22 Jul 2020 01:33:38 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 02:17:29 GMT
ENV MONO_VERSION=6.6.0.161
# Wed, 22 Jul 2020 02:18:15 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jul 2020 02:19:37 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:cd38ad753522d120e27c5343b08f661ee3aebfe531d60102d7c624c16dba4d09`  
		Last Modified: Wed, 22 Jul 2020 01:44:24 GMT  
		Size: 19.3 MB (19298267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b2680436a276aad21c6a0cca92c394a14e7525ef975ef46d35a8992d89e1257`  
		Last Modified: Wed, 22 Jul 2020 02:32:51 GMT  
		Size: 244.6 KB (244560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d961717bb11902ebe7f61b28efbaad39e135b491ea8b0251b94bcd51baebe8f4`  
		Last Modified: Wed, 22 Jul 2020 02:33:00 GMT  
		Size: 24.5 MB (24543391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6.0.161-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:0548c64057ccda46f006db6e0a843bc84ef1a1933a2d648f1375bae2a789afc9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.9 MB (49945769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f97dae24f93657a335b68d01bd3b74f8aff6ade8e76d786837880b0fbe8b64e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:54:49 GMT
ADD file:c85d28567b6123deb660b71c8b60d92378b5ba15ba5dcf495d9388817dc3aa44 in / 
# Tue, 09 Jun 2020 01:54:52 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 03:25:21 GMT
ENV MONO_VERSION=6.6.0.161
# Tue, 09 Jun 2020 03:25:41 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Jun 2020 03:26:31 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:622dc742b82743ebf5607b215a65869096390ee41b0a61b5532f859fb94590b1`  
		Last Modified: Tue, 09 Jun 2020 02:00:28 GMT  
		Size: 20.4 MB (20375150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4290c2f990444deb0f93dd0ba68fc5d94357ce1cfdb252dec480eb8dc62df72`  
		Last Modified: Tue, 09 Jun 2020 03:37:19 GMT  
		Size: 244.4 KB (244381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f7365212009d85dfb9bd0fefee678ef2259929ed35a819d5d1d63931c29d142`  
		Last Modified: Tue, 09 Jun 2020 03:37:29 GMT  
		Size: 29.3 MB (29326238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6.0.161-slim` - linux; 386

```console
$ docker pull mono@sha256:932000e44cdd35e26b77f4c0c5677f1628fc274a874d3d582b6308b5582a1908
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.0 MB (90031030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07cc18c7941b425b71c3f02fae3f465e1e968dd84e133e4c9fb08c67b10fd434`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:42:33 GMT
ADD file:8ef252685ffefc58654053bf145c830928a2cf423a6c757180649df772f1523d in / 
# Tue, 09 Jun 2020 01:42:34 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 07:00:31 GMT
ENV MONO_VERSION=6.6.0.161
# Tue, 09 Jun 2020 07:00:43 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Jun 2020 07:01:34 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:4ffbd6ec7974e514763a8d7d9fcf5e86e9440e2280e6e9561ea373b4bc50588e`  
		Last Modified: Tue, 09 Jun 2020 01:48:28 GMT  
		Size: 23.1 MB (23147892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dac86da952cf07d4efdc128f7ad526f39026bebd6fd96ce97f984d213ff33beb`  
		Last Modified: Tue, 09 Jun 2020 07:10:48 GMT  
		Size: 244.5 KB (244473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44aea1cbf2eb9bf3490c39e0036b585c6bd70cb027e4d67779122b5337b7eec8`  
		Last Modified: Tue, 09 Jun 2020 07:11:04 GMT  
		Size: 66.6 MB (66638665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6.0.161-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:57d9303ed37696b8b21c488b4aca34261b07a9c5a1acf2568a56cf10ef898de5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48751393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4aa115ab28661971a7391f318eae5c36b475f431e9cd1085efb4a3f7f4338a8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:25:38 GMT
ADD file:41ec53d65aa183c2835f73989c9e4922f818e59774811eaa6e7395e5a36d5eab in / 
# Tue, 09 Jun 2020 01:25:42 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 04:40:54 GMT
ENV MONO_VERSION=6.6.0.161
# Tue, 09 Jun 2020 04:41:50 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Jun 2020 04:42:57 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a29e28607c9b96acae7ff89e56214e4339a87c59e40a6f030fa4cbcaab753f2c`  
		Last Modified: Tue, 09 Jun 2020 01:37:25 GMT  
		Size: 22.8 MB (22791269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79f61e53535e34c8ba847db7a0b997284c1aa54e60b26ed23e5bfa4cab2fcd91`  
		Last Modified: Tue, 09 Jun 2020 05:05:48 GMT  
		Size: 244.6 KB (244568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:563625e3974512d700bb578934524f8dbbb23413ac33824ac5c60129e7c109d7`  
		Last Modified: Tue, 09 Jun 2020 05:05:55 GMT  
		Size: 25.7 MB (25715556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.6.0-slim`

```console
$ docker pull mono@sha256:582138ec5465d837705c24321d7dcdb63806e22407483fc5a7b974b978b15140
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:6.6.0-slim` - linux; amd64

```console
$ docker pull mono@sha256:724f93d88c54fc788bc87dbc6931739df3dbb2b65c7206065f3194317a59a9ee
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.6 MB (85610215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c852ee32c5901bfbb43906406f35f1b7eaf9ed3e2f6a67c3b3c7c8c59be8fa4e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:23:35 GMT
ADD file:57b431451a292755d0f13673f5f3bea9f62aea36c7a1b59d34d7d200ba134fea in / 
# Tue, 09 Jun 2020 01:23:35 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 07:24:32 GMT
ENV MONO_VERSION=6.6.0.161
# Tue, 09 Jun 2020 07:24:42 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Jun 2020 07:25:14 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7d2977b12acb33f192e3f20b7e15a467cc8f3f5124a15d975a6d4afe5fa3d258`  
		Last Modified: Tue, 09 Jun 2020 01:28:13 GMT  
		Size: 22.5 MB (22519600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20c821ecf18976f07ebc44d5e8f60b56baf477680dd1e8b7b20a095ce6b0fe2a`  
		Last Modified: Tue, 09 Jun 2020 07:58:03 GMT  
		Size: 244.5 KB (244473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57b71e1fdcdf5a134a49b7b4375e7c683147eb59f6c09717238e01135cdd7e40`  
		Last Modified: Tue, 09 Jun 2020 07:58:21 GMT  
		Size: 62.8 MB (62846142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6.0-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:76c9a8aa860d3832e3f1f33cd7f6429459bd33cdc24a5e80f0fb867a012c777d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.7 MB (46741736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4c26f6eeec8140f621d9560fe9ccf3fe4bab827488eb10b4d49f1bb374e6f6b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 00:55:12 GMT
ADD file:0b9f2b88887a8060402a052c243c31641d9c217edcdb232c7b7a057cf5a70d66 in / 
# Wed, 22 Jul 2020 00:55:13 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 04:49:08 GMT
ENV MONO_VERSION=6.6.0.161
# Wed, 22 Jul 2020 04:49:43 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jul 2020 04:50:49 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:319109fcb6fa9b08528c518426e7ce105aac7313066432efcea95f59ff6e6788`  
		Last Modified: Wed, 22 Jul 2020 01:03:27 GMT  
		Size: 21.2 MB (21189131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80846289d34adc8ed8a1ce2ab050633f8d9d1c16defa48525d5ffb4cfae0849a`  
		Last Modified: Wed, 22 Jul 2020 05:03:04 GMT  
		Size: 244.6 KB (244586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9fafd2cc65b4de32fff13f1e5aa9b86cf7162bfbadb5082fb9eb5cc0d817172`  
		Last Modified: Wed, 22 Jul 2020 05:03:13 GMT  
		Size: 25.3 MB (25308019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6.0-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:4021746b21e557dd685768996f96e6e40bd2453921df6a7d1344253a9af213ed
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.1 MB (44086218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fcf4d17a831f0d4a17972f1c4ef71a2d8223efba3969c6e7e9a0c8900f8e878`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 01:33:30 GMT
ADD file:49b1a1b4f5c2201b0e23e29dca24c4f6ffc14620196c4bd77770952500c4bee1 in / 
# Wed, 22 Jul 2020 01:33:38 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 02:17:29 GMT
ENV MONO_VERSION=6.6.0.161
# Wed, 22 Jul 2020 02:18:15 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jul 2020 02:19:37 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:cd38ad753522d120e27c5343b08f661ee3aebfe531d60102d7c624c16dba4d09`  
		Last Modified: Wed, 22 Jul 2020 01:44:24 GMT  
		Size: 19.3 MB (19298267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b2680436a276aad21c6a0cca92c394a14e7525ef975ef46d35a8992d89e1257`  
		Last Modified: Wed, 22 Jul 2020 02:32:51 GMT  
		Size: 244.6 KB (244560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d961717bb11902ebe7f61b28efbaad39e135b491ea8b0251b94bcd51baebe8f4`  
		Last Modified: Wed, 22 Jul 2020 02:33:00 GMT  
		Size: 24.5 MB (24543391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6.0-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:0548c64057ccda46f006db6e0a843bc84ef1a1933a2d648f1375bae2a789afc9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.9 MB (49945769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f97dae24f93657a335b68d01bd3b74f8aff6ade8e76d786837880b0fbe8b64e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:54:49 GMT
ADD file:c85d28567b6123deb660b71c8b60d92378b5ba15ba5dcf495d9388817dc3aa44 in / 
# Tue, 09 Jun 2020 01:54:52 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 03:25:21 GMT
ENV MONO_VERSION=6.6.0.161
# Tue, 09 Jun 2020 03:25:41 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Jun 2020 03:26:31 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:622dc742b82743ebf5607b215a65869096390ee41b0a61b5532f859fb94590b1`  
		Last Modified: Tue, 09 Jun 2020 02:00:28 GMT  
		Size: 20.4 MB (20375150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4290c2f990444deb0f93dd0ba68fc5d94357ce1cfdb252dec480eb8dc62df72`  
		Last Modified: Tue, 09 Jun 2020 03:37:19 GMT  
		Size: 244.4 KB (244381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f7365212009d85dfb9bd0fefee678ef2259929ed35a819d5d1d63931c29d142`  
		Last Modified: Tue, 09 Jun 2020 03:37:29 GMT  
		Size: 29.3 MB (29326238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6.0-slim` - linux; 386

```console
$ docker pull mono@sha256:932000e44cdd35e26b77f4c0c5677f1628fc274a874d3d582b6308b5582a1908
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.0 MB (90031030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07cc18c7941b425b71c3f02fae3f465e1e968dd84e133e4c9fb08c67b10fd434`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:42:33 GMT
ADD file:8ef252685ffefc58654053bf145c830928a2cf423a6c757180649df772f1523d in / 
# Tue, 09 Jun 2020 01:42:34 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 07:00:31 GMT
ENV MONO_VERSION=6.6.0.161
# Tue, 09 Jun 2020 07:00:43 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Jun 2020 07:01:34 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:4ffbd6ec7974e514763a8d7d9fcf5e86e9440e2280e6e9561ea373b4bc50588e`  
		Last Modified: Tue, 09 Jun 2020 01:48:28 GMT  
		Size: 23.1 MB (23147892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dac86da952cf07d4efdc128f7ad526f39026bebd6fd96ce97f984d213ff33beb`  
		Last Modified: Tue, 09 Jun 2020 07:10:48 GMT  
		Size: 244.5 KB (244473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44aea1cbf2eb9bf3490c39e0036b585c6bd70cb027e4d67779122b5337b7eec8`  
		Last Modified: Tue, 09 Jun 2020 07:11:04 GMT  
		Size: 66.6 MB (66638665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6.0-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:57d9303ed37696b8b21c488b4aca34261b07a9c5a1acf2568a56cf10ef898de5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48751393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4aa115ab28661971a7391f318eae5c36b475f431e9cd1085efb4a3f7f4338a8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:25:38 GMT
ADD file:41ec53d65aa183c2835f73989c9e4922f818e59774811eaa6e7395e5a36d5eab in / 
# Tue, 09 Jun 2020 01:25:42 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 04:40:54 GMT
ENV MONO_VERSION=6.6.0.161
# Tue, 09 Jun 2020 04:41:50 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Jun 2020 04:42:57 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a29e28607c9b96acae7ff89e56214e4339a87c59e40a6f030fa4cbcaab753f2c`  
		Last Modified: Tue, 09 Jun 2020 01:37:25 GMT  
		Size: 22.8 MB (22791269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79f61e53535e34c8ba847db7a0b997284c1aa54e60b26ed23e5bfa4cab2fcd91`  
		Last Modified: Tue, 09 Jun 2020 05:05:48 GMT  
		Size: 244.6 KB (244568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:563625e3974512d700bb578934524f8dbbb23413ac33824ac5c60129e7c109d7`  
		Last Modified: Tue, 09 Jun 2020 05:05:55 GMT  
		Size: 25.7 MB (25715556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.6-slim`

```console
$ docker pull mono@sha256:582138ec5465d837705c24321d7dcdb63806e22407483fc5a7b974b978b15140
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:6.6-slim` - linux; amd64

```console
$ docker pull mono@sha256:724f93d88c54fc788bc87dbc6931739df3dbb2b65c7206065f3194317a59a9ee
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.6 MB (85610215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c852ee32c5901bfbb43906406f35f1b7eaf9ed3e2f6a67c3b3c7c8c59be8fa4e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:23:35 GMT
ADD file:57b431451a292755d0f13673f5f3bea9f62aea36c7a1b59d34d7d200ba134fea in / 
# Tue, 09 Jun 2020 01:23:35 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 07:24:32 GMT
ENV MONO_VERSION=6.6.0.161
# Tue, 09 Jun 2020 07:24:42 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Jun 2020 07:25:14 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7d2977b12acb33f192e3f20b7e15a467cc8f3f5124a15d975a6d4afe5fa3d258`  
		Last Modified: Tue, 09 Jun 2020 01:28:13 GMT  
		Size: 22.5 MB (22519600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20c821ecf18976f07ebc44d5e8f60b56baf477680dd1e8b7b20a095ce6b0fe2a`  
		Last Modified: Tue, 09 Jun 2020 07:58:03 GMT  
		Size: 244.5 KB (244473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57b71e1fdcdf5a134a49b7b4375e7c683147eb59f6c09717238e01135cdd7e40`  
		Last Modified: Tue, 09 Jun 2020 07:58:21 GMT  
		Size: 62.8 MB (62846142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:76c9a8aa860d3832e3f1f33cd7f6429459bd33cdc24a5e80f0fb867a012c777d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.7 MB (46741736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4c26f6eeec8140f621d9560fe9ccf3fe4bab827488eb10b4d49f1bb374e6f6b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 00:55:12 GMT
ADD file:0b9f2b88887a8060402a052c243c31641d9c217edcdb232c7b7a057cf5a70d66 in / 
# Wed, 22 Jul 2020 00:55:13 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 04:49:08 GMT
ENV MONO_VERSION=6.6.0.161
# Wed, 22 Jul 2020 04:49:43 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jul 2020 04:50:49 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:319109fcb6fa9b08528c518426e7ce105aac7313066432efcea95f59ff6e6788`  
		Last Modified: Wed, 22 Jul 2020 01:03:27 GMT  
		Size: 21.2 MB (21189131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80846289d34adc8ed8a1ce2ab050633f8d9d1c16defa48525d5ffb4cfae0849a`  
		Last Modified: Wed, 22 Jul 2020 05:03:04 GMT  
		Size: 244.6 KB (244586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9fafd2cc65b4de32fff13f1e5aa9b86cf7162bfbadb5082fb9eb5cc0d817172`  
		Last Modified: Wed, 22 Jul 2020 05:03:13 GMT  
		Size: 25.3 MB (25308019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:4021746b21e557dd685768996f96e6e40bd2453921df6a7d1344253a9af213ed
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.1 MB (44086218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fcf4d17a831f0d4a17972f1c4ef71a2d8223efba3969c6e7e9a0c8900f8e878`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 01:33:30 GMT
ADD file:49b1a1b4f5c2201b0e23e29dca24c4f6ffc14620196c4bd77770952500c4bee1 in / 
# Wed, 22 Jul 2020 01:33:38 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 02:17:29 GMT
ENV MONO_VERSION=6.6.0.161
# Wed, 22 Jul 2020 02:18:15 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jul 2020 02:19:37 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:cd38ad753522d120e27c5343b08f661ee3aebfe531d60102d7c624c16dba4d09`  
		Last Modified: Wed, 22 Jul 2020 01:44:24 GMT  
		Size: 19.3 MB (19298267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b2680436a276aad21c6a0cca92c394a14e7525ef975ef46d35a8992d89e1257`  
		Last Modified: Wed, 22 Jul 2020 02:32:51 GMT  
		Size: 244.6 KB (244560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d961717bb11902ebe7f61b28efbaad39e135b491ea8b0251b94bcd51baebe8f4`  
		Last Modified: Wed, 22 Jul 2020 02:33:00 GMT  
		Size: 24.5 MB (24543391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:0548c64057ccda46f006db6e0a843bc84ef1a1933a2d648f1375bae2a789afc9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.9 MB (49945769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f97dae24f93657a335b68d01bd3b74f8aff6ade8e76d786837880b0fbe8b64e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:54:49 GMT
ADD file:c85d28567b6123deb660b71c8b60d92378b5ba15ba5dcf495d9388817dc3aa44 in / 
# Tue, 09 Jun 2020 01:54:52 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 03:25:21 GMT
ENV MONO_VERSION=6.6.0.161
# Tue, 09 Jun 2020 03:25:41 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Jun 2020 03:26:31 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:622dc742b82743ebf5607b215a65869096390ee41b0a61b5532f859fb94590b1`  
		Last Modified: Tue, 09 Jun 2020 02:00:28 GMT  
		Size: 20.4 MB (20375150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4290c2f990444deb0f93dd0ba68fc5d94357ce1cfdb252dec480eb8dc62df72`  
		Last Modified: Tue, 09 Jun 2020 03:37:19 GMT  
		Size: 244.4 KB (244381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f7365212009d85dfb9bd0fefee678ef2259929ed35a819d5d1d63931c29d142`  
		Last Modified: Tue, 09 Jun 2020 03:37:29 GMT  
		Size: 29.3 MB (29326238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6-slim` - linux; 386

```console
$ docker pull mono@sha256:932000e44cdd35e26b77f4c0c5677f1628fc274a874d3d582b6308b5582a1908
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.0 MB (90031030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07cc18c7941b425b71c3f02fae3f465e1e968dd84e133e4c9fb08c67b10fd434`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:42:33 GMT
ADD file:8ef252685ffefc58654053bf145c830928a2cf423a6c757180649df772f1523d in / 
# Tue, 09 Jun 2020 01:42:34 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 07:00:31 GMT
ENV MONO_VERSION=6.6.0.161
# Tue, 09 Jun 2020 07:00:43 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Jun 2020 07:01:34 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:4ffbd6ec7974e514763a8d7d9fcf5e86e9440e2280e6e9561ea373b4bc50588e`  
		Last Modified: Tue, 09 Jun 2020 01:48:28 GMT  
		Size: 23.1 MB (23147892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dac86da952cf07d4efdc128f7ad526f39026bebd6fd96ce97f984d213ff33beb`  
		Last Modified: Tue, 09 Jun 2020 07:10:48 GMT  
		Size: 244.5 KB (244473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44aea1cbf2eb9bf3490c39e0036b585c6bd70cb027e4d67779122b5337b7eec8`  
		Last Modified: Tue, 09 Jun 2020 07:11:04 GMT  
		Size: 66.6 MB (66638665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:57d9303ed37696b8b21c488b4aca34261b07a9c5a1acf2568a56cf10ef898de5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48751393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4aa115ab28661971a7391f318eae5c36b475f431e9cd1085efb4a3f7f4338a8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:25:38 GMT
ADD file:41ec53d65aa183c2835f73989c9e4922f818e59774811eaa6e7395e5a36d5eab in / 
# Tue, 09 Jun 2020 01:25:42 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 04:40:54 GMT
ENV MONO_VERSION=6.6.0.161
# Tue, 09 Jun 2020 04:41:50 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Jun 2020 04:42:57 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a29e28607c9b96acae7ff89e56214e4339a87c59e40a6f030fa4cbcaab753f2c`  
		Last Modified: Tue, 09 Jun 2020 01:37:25 GMT  
		Size: 22.8 MB (22791269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79f61e53535e34c8ba847db7a0b997284c1aa54e60b26ed23e5bfa4cab2fcd91`  
		Last Modified: Tue, 09 Jun 2020 05:05:48 GMT  
		Size: 244.6 KB (244568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:563625e3974512d700bb578934524f8dbbb23413ac33824ac5c60129e7c109d7`  
		Last Modified: Tue, 09 Jun 2020 05:05:55 GMT  
		Size: 25.7 MB (25715556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.8`

```console
$ docker pull mono@sha256:4edd8d6d3134e4de4f25836d12a6a9a9de23fa572846e74709b2f19f7371995a
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
$ docker pull mono@sha256:d4717190e9fd6118cb2775e2f084daf223583c24bc1f014c33dea48485bc7ff2
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.0 MB (235024583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a6baf0a892689f2f75227c4c04ab734c8497ab6853b037bb733184b2417c751`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:23:35 GMT
ADD file:57b431451a292755d0f13673f5f3bea9f62aea36c7a1b59d34d7d200ba134fea in / 
# Tue, 09 Jun 2020 01:23:35 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 07:23:45 GMT
ENV MONO_VERSION=6.8.0.96
# Tue, 09 Jun 2020 07:23:55 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Jun 2020 07:24:27 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 09 Jun 2020 07:36:17 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7d2977b12acb33f192e3f20b7e15a467cc8f3f5124a15d975a6d4afe5fa3d258`  
		Last Modified: Tue, 09 Jun 2020 01:28:13 GMT  
		Size: 22.5 MB (22519600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:086ef7a7e886327a728a6c520ae895632459590d19d2691114827740ae2f70e8`  
		Last Modified: Tue, 09 Jun 2020 07:57:38 GMT  
		Size: 244.5 KB (244473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28855cf8f97ad7e71803802cd6b3c77cc8335c628b34fc3f6283688061cdad11`  
		Last Modified: Tue, 09 Jun 2020 07:57:56 GMT  
		Size: 64.5 MB (64467452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e1b1cfd1a055e22c600005e10f64b8b2b3557bff82aa4bc012ab66cb8786346`  
		Last Modified: Tue, 09 Jun 2020 07:59:31 GMT  
		Size: 147.8 MB (147793058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8` - linux; arm variant v5

```console
$ docker pull mono@sha256:899467182dd8b6e055181cdce28cc3cae6935b0d914393224be26af46629c004
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.6 MB (176588520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42bd2219f249736535bcd1ba211ff5d352edc655fe81450544fbb344fc18b015`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 00:55:12 GMT
ADD file:0b9f2b88887a8060402a052c243c31641d9c217edcdb232c7b7a057cf5a70d66 in / 
# Wed, 22 Jul 2020 00:55:13 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 04:47:49 GMT
ENV MONO_VERSION=6.8.0.96
# Wed, 22 Jul 2020 04:48:12 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jul 2020 04:49:00 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 22 Jul 2020 04:55:31 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:319109fcb6fa9b08528c518426e7ce105aac7313066432efcea95f59ff6e6788`  
		Last Modified: Wed, 22 Jul 2020 01:03:27 GMT  
		Size: 21.2 MB (21189131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a62cce824a648193694f4121faf883e003fd11739ec85458d954e3cf0f8860ec`  
		Last Modified: Wed, 22 Jul 2020 05:02:47 GMT  
		Size: 244.5 KB (244541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f82e724d353f93153e6d1203349f4b687bc703c55e3b1cc2438b3ffad6974124`  
		Last Modified: Wed, 22 Jul 2020 05:02:55 GMT  
		Size: 25.3 MB (25253549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:225b191f3416f0c2fd00c0c702d8819f8c61a0faece5b5d2dcb4815b23191907`  
		Last Modified: Wed, 22 Jul 2020 05:04:19 GMT  
		Size: 129.9 MB (129901299 bytes)  
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
$ docker pull mono@sha256:68d1db7da63e2106ddea8d7850cf3badfaa16a94d8d23a12910f86785e4decc8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.6 MB (194642181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf6ff587bef5367449ceee09405f75d3b5a38e19c0d360ec43da1874b37497aa`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:54:49 GMT
ADD file:c85d28567b6123deb660b71c8b60d92378b5ba15ba5dcf495d9388817dc3aa44 in / 
# Tue, 09 Jun 2020 01:54:52 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 03:24:02 GMT
ENV MONO_VERSION=6.8.0.96
# Tue, 09 Jun 2020 03:24:21 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Jun 2020 03:25:06 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 09 Jun 2020 03:30:31 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:622dc742b82743ebf5607b215a65869096390ee41b0a61b5532f859fb94590b1`  
		Last Modified: Tue, 09 Jun 2020 02:00:28 GMT  
		Size: 20.4 MB (20375150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:334cf34398cfa7031d68bad42f6b2a8d870a4ad5c2b0454f3f6fdd0fb4433237`  
		Last Modified: Tue, 09 Jun 2020 03:37:02 GMT  
		Size: 244.4 KB (244374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aa8cbd821b66a8c4a38ce3d6711cc1ee5489b04a017ab6a7fd368f08beec89e`  
		Last Modified: Tue, 09 Jun 2020 03:37:10 GMT  
		Size: 29.3 MB (29310269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f78bf65ea03cc9db2213ce7ff8e07d3a77604a43ef0a7d81b88b5c965515dfe`  
		Last Modified: Tue, 09 Jun 2020 03:38:38 GMT  
		Size: 144.7 MB (144712388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8` - linux; 386

```console
$ docker pull mono@sha256:443376dd685b5fcd1e0b6b7a685c5b6a24a79fad8b9619e983293b70e84c8bb6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.4 MB (243401430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6948fdbf966360cb7a728eae30756da2daa5cc4b0362dd09e3a352f4ee44e5dc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:42:33 GMT
ADD file:8ef252685ffefc58654053bf145c830928a2cf423a6c757180649df772f1523d in / 
# Tue, 09 Jun 2020 01:42:34 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 06:59:35 GMT
ENV MONO_VERSION=6.8.0.96
# Tue, 09 Jun 2020 06:59:46 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Jun 2020 07:00:24 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 09 Jun 2020 07:05:03 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:4ffbd6ec7974e514763a8d7d9fcf5e86e9440e2280e6e9561ea373b4bc50588e`  
		Last Modified: Tue, 09 Jun 2020 01:48:28 GMT  
		Size: 23.1 MB (23147892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b3a90700548ab3df378beb07af7fba67e7ea89ead888d8c78d529c40633c7ed`  
		Last Modified: Tue, 09 Jun 2020 07:10:23 GMT  
		Size: 244.5 KB (244462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbcec5e4a352eead9b06946ed8fb1855a57123b280b3941614dac805987d5b65`  
		Last Modified: Tue, 09 Jun 2020 07:10:41 GMT  
		Size: 68.5 MB (68517280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae8167823b3a297ca26719112fd4ae0b1b90e5df5ef7edf3302022c64061697f`  
		Last Modified: Tue, 09 Jun 2020 07:12:09 GMT  
		Size: 151.5 MB (151491796 bytes)  
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
$ docker pull mono@sha256:4edd8d6d3134e4de4f25836d12a6a9a9de23fa572846e74709b2f19f7371995a
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
$ docker pull mono@sha256:d4717190e9fd6118cb2775e2f084daf223583c24bc1f014c33dea48485bc7ff2
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.0 MB (235024583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a6baf0a892689f2f75227c4c04ab734c8497ab6853b037bb733184b2417c751`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:23:35 GMT
ADD file:57b431451a292755d0f13673f5f3bea9f62aea36c7a1b59d34d7d200ba134fea in / 
# Tue, 09 Jun 2020 01:23:35 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 07:23:45 GMT
ENV MONO_VERSION=6.8.0.96
# Tue, 09 Jun 2020 07:23:55 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Jun 2020 07:24:27 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 09 Jun 2020 07:36:17 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7d2977b12acb33f192e3f20b7e15a467cc8f3f5124a15d975a6d4afe5fa3d258`  
		Last Modified: Tue, 09 Jun 2020 01:28:13 GMT  
		Size: 22.5 MB (22519600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:086ef7a7e886327a728a6c520ae895632459590d19d2691114827740ae2f70e8`  
		Last Modified: Tue, 09 Jun 2020 07:57:38 GMT  
		Size: 244.5 KB (244473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28855cf8f97ad7e71803802cd6b3c77cc8335c628b34fc3f6283688061cdad11`  
		Last Modified: Tue, 09 Jun 2020 07:57:56 GMT  
		Size: 64.5 MB (64467452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e1b1cfd1a055e22c600005e10f64b8b2b3557bff82aa4bc012ab66cb8786346`  
		Last Modified: Tue, 09 Jun 2020 07:59:31 GMT  
		Size: 147.8 MB (147793058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8.0` - linux; arm variant v5

```console
$ docker pull mono@sha256:899467182dd8b6e055181cdce28cc3cae6935b0d914393224be26af46629c004
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.6 MB (176588520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42bd2219f249736535bcd1ba211ff5d352edc655fe81450544fbb344fc18b015`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 00:55:12 GMT
ADD file:0b9f2b88887a8060402a052c243c31641d9c217edcdb232c7b7a057cf5a70d66 in / 
# Wed, 22 Jul 2020 00:55:13 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 04:47:49 GMT
ENV MONO_VERSION=6.8.0.96
# Wed, 22 Jul 2020 04:48:12 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jul 2020 04:49:00 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 22 Jul 2020 04:55:31 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:319109fcb6fa9b08528c518426e7ce105aac7313066432efcea95f59ff6e6788`  
		Last Modified: Wed, 22 Jul 2020 01:03:27 GMT  
		Size: 21.2 MB (21189131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a62cce824a648193694f4121faf883e003fd11739ec85458d954e3cf0f8860ec`  
		Last Modified: Wed, 22 Jul 2020 05:02:47 GMT  
		Size: 244.5 KB (244541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f82e724d353f93153e6d1203349f4b687bc703c55e3b1cc2438b3ffad6974124`  
		Last Modified: Wed, 22 Jul 2020 05:02:55 GMT  
		Size: 25.3 MB (25253549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:225b191f3416f0c2fd00c0c702d8819f8c61a0faece5b5d2dcb4815b23191907`  
		Last Modified: Wed, 22 Jul 2020 05:04:19 GMT  
		Size: 129.9 MB (129901299 bytes)  
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
$ docker pull mono@sha256:68d1db7da63e2106ddea8d7850cf3badfaa16a94d8d23a12910f86785e4decc8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.6 MB (194642181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf6ff587bef5367449ceee09405f75d3b5a38e19c0d360ec43da1874b37497aa`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:54:49 GMT
ADD file:c85d28567b6123deb660b71c8b60d92378b5ba15ba5dcf495d9388817dc3aa44 in / 
# Tue, 09 Jun 2020 01:54:52 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 03:24:02 GMT
ENV MONO_VERSION=6.8.0.96
# Tue, 09 Jun 2020 03:24:21 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Jun 2020 03:25:06 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 09 Jun 2020 03:30:31 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:622dc742b82743ebf5607b215a65869096390ee41b0a61b5532f859fb94590b1`  
		Last Modified: Tue, 09 Jun 2020 02:00:28 GMT  
		Size: 20.4 MB (20375150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:334cf34398cfa7031d68bad42f6b2a8d870a4ad5c2b0454f3f6fdd0fb4433237`  
		Last Modified: Tue, 09 Jun 2020 03:37:02 GMT  
		Size: 244.4 KB (244374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aa8cbd821b66a8c4a38ce3d6711cc1ee5489b04a017ab6a7fd368f08beec89e`  
		Last Modified: Tue, 09 Jun 2020 03:37:10 GMT  
		Size: 29.3 MB (29310269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f78bf65ea03cc9db2213ce7ff8e07d3a77604a43ef0a7d81b88b5c965515dfe`  
		Last Modified: Tue, 09 Jun 2020 03:38:38 GMT  
		Size: 144.7 MB (144712388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8.0` - linux; 386

```console
$ docker pull mono@sha256:443376dd685b5fcd1e0b6b7a685c5b6a24a79fad8b9619e983293b70e84c8bb6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.4 MB (243401430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6948fdbf966360cb7a728eae30756da2daa5cc4b0362dd09e3a352f4ee44e5dc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:42:33 GMT
ADD file:8ef252685ffefc58654053bf145c830928a2cf423a6c757180649df772f1523d in / 
# Tue, 09 Jun 2020 01:42:34 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 06:59:35 GMT
ENV MONO_VERSION=6.8.0.96
# Tue, 09 Jun 2020 06:59:46 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Jun 2020 07:00:24 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 09 Jun 2020 07:05:03 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:4ffbd6ec7974e514763a8d7d9fcf5e86e9440e2280e6e9561ea373b4bc50588e`  
		Last Modified: Tue, 09 Jun 2020 01:48:28 GMT  
		Size: 23.1 MB (23147892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b3a90700548ab3df378beb07af7fba67e7ea89ead888d8c78d529c40633c7ed`  
		Last Modified: Tue, 09 Jun 2020 07:10:23 GMT  
		Size: 244.5 KB (244462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbcec5e4a352eead9b06946ed8fb1855a57123b280b3941614dac805987d5b65`  
		Last Modified: Tue, 09 Jun 2020 07:10:41 GMT  
		Size: 68.5 MB (68517280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae8167823b3a297ca26719112fd4ae0b1b90e5df5ef7edf3302022c64061697f`  
		Last Modified: Tue, 09 Jun 2020 07:12:09 GMT  
		Size: 151.5 MB (151491796 bytes)  
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

## `mono:6.8.0.96`

```console
$ docker pull mono@sha256:4edd8d6d3134e4de4f25836d12a6a9a9de23fa572846e74709b2f19f7371995a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:6.8.0.96` - linux; amd64

```console
$ docker pull mono@sha256:d4717190e9fd6118cb2775e2f084daf223583c24bc1f014c33dea48485bc7ff2
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.0 MB (235024583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a6baf0a892689f2f75227c4c04ab734c8497ab6853b037bb733184b2417c751`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:23:35 GMT
ADD file:57b431451a292755d0f13673f5f3bea9f62aea36c7a1b59d34d7d200ba134fea in / 
# Tue, 09 Jun 2020 01:23:35 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 07:23:45 GMT
ENV MONO_VERSION=6.8.0.96
# Tue, 09 Jun 2020 07:23:55 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Jun 2020 07:24:27 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 09 Jun 2020 07:36:17 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7d2977b12acb33f192e3f20b7e15a467cc8f3f5124a15d975a6d4afe5fa3d258`  
		Last Modified: Tue, 09 Jun 2020 01:28:13 GMT  
		Size: 22.5 MB (22519600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:086ef7a7e886327a728a6c520ae895632459590d19d2691114827740ae2f70e8`  
		Last Modified: Tue, 09 Jun 2020 07:57:38 GMT  
		Size: 244.5 KB (244473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28855cf8f97ad7e71803802cd6b3c77cc8335c628b34fc3f6283688061cdad11`  
		Last Modified: Tue, 09 Jun 2020 07:57:56 GMT  
		Size: 64.5 MB (64467452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e1b1cfd1a055e22c600005e10f64b8b2b3557bff82aa4bc012ab66cb8786346`  
		Last Modified: Tue, 09 Jun 2020 07:59:31 GMT  
		Size: 147.8 MB (147793058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8.0.96` - linux; arm variant v5

```console
$ docker pull mono@sha256:899467182dd8b6e055181cdce28cc3cae6935b0d914393224be26af46629c004
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.6 MB (176588520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42bd2219f249736535bcd1ba211ff5d352edc655fe81450544fbb344fc18b015`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 00:55:12 GMT
ADD file:0b9f2b88887a8060402a052c243c31641d9c217edcdb232c7b7a057cf5a70d66 in / 
# Wed, 22 Jul 2020 00:55:13 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 04:47:49 GMT
ENV MONO_VERSION=6.8.0.96
# Wed, 22 Jul 2020 04:48:12 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jul 2020 04:49:00 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 22 Jul 2020 04:55:31 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:319109fcb6fa9b08528c518426e7ce105aac7313066432efcea95f59ff6e6788`  
		Last Modified: Wed, 22 Jul 2020 01:03:27 GMT  
		Size: 21.2 MB (21189131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a62cce824a648193694f4121faf883e003fd11739ec85458d954e3cf0f8860ec`  
		Last Modified: Wed, 22 Jul 2020 05:02:47 GMT  
		Size: 244.5 KB (244541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f82e724d353f93153e6d1203349f4b687bc703c55e3b1cc2438b3ffad6974124`  
		Last Modified: Wed, 22 Jul 2020 05:02:55 GMT  
		Size: 25.3 MB (25253549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:225b191f3416f0c2fd00c0c702d8819f8c61a0faece5b5d2dcb4815b23191907`  
		Last Modified: Wed, 22 Jul 2020 05:04:19 GMT  
		Size: 129.9 MB (129901299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8.0.96` - linux; arm variant v7

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

### `mono:6.8.0.96` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:68d1db7da63e2106ddea8d7850cf3badfaa16a94d8d23a12910f86785e4decc8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.6 MB (194642181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf6ff587bef5367449ceee09405f75d3b5a38e19c0d360ec43da1874b37497aa`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:54:49 GMT
ADD file:c85d28567b6123deb660b71c8b60d92378b5ba15ba5dcf495d9388817dc3aa44 in / 
# Tue, 09 Jun 2020 01:54:52 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 03:24:02 GMT
ENV MONO_VERSION=6.8.0.96
# Tue, 09 Jun 2020 03:24:21 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Jun 2020 03:25:06 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 09 Jun 2020 03:30:31 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:622dc742b82743ebf5607b215a65869096390ee41b0a61b5532f859fb94590b1`  
		Last Modified: Tue, 09 Jun 2020 02:00:28 GMT  
		Size: 20.4 MB (20375150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:334cf34398cfa7031d68bad42f6b2a8d870a4ad5c2b0454f3f6fdd0fb4433237`  
		Last Modified: Tue, 09 Jun 2020 03:37:02 GMT  
		Size: 244.4 KB (244374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aa8cbd821b66a8c4a38ce3d6711cc1ee5489b04a017ab6a7fd368f08beec89e`  
		Last Modified: Tue, 09 Jun 2020 03:37:10 GMT  
		Size: 29.3 MB (29310269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f78bf65ea03cc9db2213ce7ff8e07d3a77604a43ef0a7d81b88b5c965515dfe`  
		Last Modified: Tue, 09 Jun 2020 03:38:38 GMT  
		Size: 144.7 MB (144712388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8.0.96` - linux; 386

```console
$ docker pull mono@sha256:443376dd685b5fcd1e0b6b7a685c5b6a24a79fad8b9619e983293b70e84c8bb6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.4 MB (243401430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6948fdbf966360cb7a728eae30756da2daa5cc4b0362dd09e3a352f4ee44e5dc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:42:33 GMT
ADD file:8ef252685ffefc58654053bf145c830928a2cf423a6c757180649df772f1523d in / 
# Tue, 09 Jun 2020 01:42:34 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 06:59:35 GMT
ENV MONO_VERSION=6.8.0.96
# Tue, 09 Jun 2020 06:59:46 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Jun 2020 07:00:24 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 09 Jun 2020 07:05:03 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:4ffbd6ec7974e514763a8d7d9fcf5e86e9440e2280e6e9561ea373b4bc50588e`  
		Last Modified: Tue, 09 Jun 2020 01:48:28 GMT  
		Size: 23.1 MB (23147892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b3a90700548ab3df378beb07af7fba67e7ea89ead888d8c78d529c40633c7ed`  
		Last Modified: Tue, 09 Jun 2020 07:10:23 GMT  
		Size: 244.5 KB (244462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbcec5e4a352eead9b06946ed8fb1855a57123b280b3941614dac805987d5b65`  
		Last Modified: Tue, 09 Jun 2020 07:10:41 GMT  
		Size: 68.5 MB (68517280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae8167823b3a297ca26719112fd4ae0b1b90e5df5ef7edf3302022c64061697f`  
		Last Modified: Tue, 09 Jun 2020 07:12:09 GMT  
		Size: 151.5 MB (151491796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8.0.96` - linux; ppc64le

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

## `mono:6.8.0.96-slim`

```console
$ docker pull mono@sha256:ce1717f66152b5a364712978c58f62ff0f06c11659d033fdafdf26fb7407e2f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:6.8.0.96-slim` - linux; amd64

```console
$ docker pull mono@sha256:a6e184082378911b563cafc02a2f4d4bc5b1c5a4ff0c2fbdf62471e2cbed0d68
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.2 MB (87231525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bd253379aef6e46ed99c035c08e92c0ec3d33da796131035aa4da08949ed069`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:23:35 GMT
ADD file:57b431451a292755d0f13673f5f3bea9f62aea36c7a1b59d34d7d200ba134fea in / 
# Tue, 09 Jun 2020 01:23:35 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 07:23:45 GMT
ENV MONO_VERSION=6.8.0.96
# Tue, 09 Jun 2020 07:23:55 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Jun 2020 07:24:27 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7d2977b12acb33f192e3f20b7e15a467cc8f3f5124a15d975a6d4afe5fa3d258`  
		Last Modified: Tue, 09 Jun 2020 01:28:13 GMT  
		Size: 22.5 MB (22519600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:086ef7a7e886327a728a6c520ae895632459590d19d2691114827740ae2f70e8`  
		Last Modified: Tue, 09 Jun 2020 07:57:38 GMT  
		Size: 244.5 KB (244473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28855cf8f97ad7e71803802cd6b3c77cc8335c628b34fc3f6283688061cdad11`  
		Last Modified: Tue, 09 Jun 2020 07:57:56 GMT  
		Size: 64.5 MB (64467452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8.0.96-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:e6de1477ff957c4b2f0ab6f4f790dc1225b873ced9b789c54d346c25703217e6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.7 MB (46687221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efe6f734a291cceabb4881569dc5bda10268e94b9483be02ba8fdb2ba3d2f9c7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 00:55:12 GMT
ADD file:0b9f2b88887a8060402a052c243c31641d9c217edcdb232c7b7a057cf5a70d66 in / 
# Wed, 22 Jul 2020 00:55:13 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 04:47:49 GMT
ENV MONO_VERSION=6.8.0.96
# Wed, 22 Jul 2020 04:48:12 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jul 2020 04:49:00 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:319109fcb6fa9b08528c518426e7ce105aac7313066432efcea95f59ff6e6788`  
		Last Modified: Wed, 22 Jul 2020 01:03:27 GMT  
		Size: 21.2 MB (21189131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a62cce824a648193694f4121faf883e003fd11739ec85458d954e3cf0f8860ec`  
		Last Modified: Wed, 22 Jul 2020 05:02:47 GMT  
		Size: 244.5 KB (244541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f82e724d353f93153e6d1203349f4b687bc703c55e3b1cc2438b3ffad6974124`  
		Last Modified: Wed, 22 Jul 2020 05:02:55 GMT  
		Size: 25.3 MB (25253549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8.0.96-slim` - linux; arm variant v7

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

### `mono:6.8.0.96-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:24d8471bd7e59cc38ba65db018794a92fc6d54960784f86d52c913e4a8f5c9a9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.9 MB (49929793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb86494c128abaa467fc19a192852bfde9ae94e0d13aa1f9f1b70d9adb68697d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:54:49 GMT
ADD file:c85d28567b6123deb660b71c8b60d92378b5ba15ba5dcf495d9388817dc3aa44 in / 
# Tue, 09 Jun 2020 01:54:52 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 03:24:02 GMT
ENV MONO_VERSION=6.8.0.96
# Tue, 09 Jun 2020 03:24:21 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Jun 2020 03:25:06 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:622dc742b82743ebf5607b215a65869096390ee41b0a61b5532f859fb94590b1`  
		Last Modified: Tue, 09 Jun 2020 02:00:28 GMT  
		Size: 20.4 MB (20375150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:334cf34398cfa7031d68bad42f6b2a8d870a4ad5c2b0454f3f6fdd0fb4433237`  
		Last Modified: Tue, 09 Jun 2020 03:37:02 GMT  
		Size: 244.4 KB (244374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aa8cbd821b66a8c4a38ce3d6711cc1ee5489b04a017ab6a7fd368f08beec89e`  
		Last Modified: Tue, 09 Jun 2020 03:37:10 GMT  
		Size: 29.3 MB (29310269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8.0.96-slim` - linux; 386

```console
$ docker pull mono@sha256:e78d5446f93beef2216681d481890fe6388d64c704eb5cd4cc2e7010748818bd
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.9 MB (91909634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ebdb565c91f1fbc53a06cbfb5b9c374ab82f491c6934131ce4f1ae6524b43cf`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:42:33 GMT
ADD file:8ef252685ffefc58654053bf145c830928a2cf423a6c757180649df772f1523d in / 
# Tue, 09 Jun 2020 01:42:34 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 06:59:35 GMT
ENV MONO_VERSION=6.8.0.96
# Tue, 09 Jun 2020 06:59:46 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Jun 2020 07:00:24 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:4ffbd6ec7974e514763a8d7d9fcf5e86e9440e2280e6e9561ea373b4bc50588e`  
		Last Modified: Tue, 09 Jun 2020 01:48:28 GMT  
		Size: 23.1 MB (23147892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b3a90700548ab3df378beb07af7fba67e7ea89ead888d8c78d529c40633c7ed`  
		Last Modified: Tue, 09 Jun 2020 07:10:23 GMT  
		Size: 244.5 KB (244462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbcec5e4a352eead9b06946ed8fb1855a57123b280b3941614dac805987d5b65`  
		Last Modified: Tue, 09 Jun 2020 07:10:41 GMT  
		Size: 68.5 MB (68517280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8.0.96-slim` - linux; ppc64le

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

## `mono:6.8.0-slim`

```console
$ docker pull mono@sha256:ce1717f66152b5a364712978c58f62ff0f06c11659d033fdafdf26fb7407e2f9
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
$ docker pull mono@sha256:a6e184082378911b563cafc02a2f4d4bc5b1c5a4ff0c2fbdf62471e2cbed0d68
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.2 MB (87231525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bd253379aef6e46ed99c035c08e92c0ec3d33da796131035aa4da08949ed069`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:23:35 GMT
ADD file:57b431451a292755d0f13673f5f3bea9f62aea36c7a1b59d34d7d200ba134fea in / 
# Tue, 09 Jun 2020 01:23:35 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 07:23:45 GMT
ENV MONO_VERSION=6.8.0.96
# Tue, 09 Jun 2020 07:23:55 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Jun 2020 07:24:27 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7d2977b12acb33f192e3f20b7e15a467cc8f3f5124a15d975a6d4afe5fa3d258`  
		Last Modified: Tue, 09 Jun 2020 01:28:13 GMT  
		Size: 22.5 MB (22519600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:086ef7a7e886327a728a6c520ae895632459590d19d2691114827740ae2f70e8`  
		Last Modified: Tue, 09 Jun 2020 07:57:38 GMT  
		Size: 244.5 KB (244473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28855cf8f97ad7e71803802cd6b3c77cc8335c628b34fc3f6283688061cdad11`  
		Last Modified: Tue, 09 Jun 2020 07:57:56 GMT  
		Size: 64.5 MB (64467452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8.0-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:e6de1477ff957c4b2f0ab6f4f790dc1225b873ced9b789c54d346c25703217e6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.7 MB (46687221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efe6f734a291cceabb4881569dc5bda10268e94b9483be02ba8fdb2ba3d2f9c7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 00:55:12 GMT
ADD file:0b9f2b88887a8060402a052c243c31641d9c217edcdb232c7b7a057cf5a70d66 in / 
# Wed, 22 Jul 2020 00:55:13 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 04:47:49 GMT
ENV MONO_VERSION=6.8.0.96
# Wed, 22 Jul 2020 04:48:12 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jul 2020 04:49:00 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:319109fcb6fa9b08528c518426e7ce105aac7313066432efcea95f59ff6e6788`  
		Last Modified: Wed, 22 Jul 2020 01:03:27 GMT  
		Size: 21.2 MB (21189131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a62cce824a648193694f4121faf883e003fd11739ec85458d954e3cf0f8860ec`  
		Last Modified: Wed, 22 Jul 2020 05:02:47 GMT  
		Size: 244.5 KB (244541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f82e724d353f93153e6d1203349f4b687bc703c55e3b1cc2438b3ffad6974124`  
		Last Modified: Wed, 22 Jul 2020 05:02:55 GMT  
		Size: 25.3 MB (25253549 bytes)  
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
$ docker pull mono@sha256:24d8471bd7e59cc38ba65db018794a92fc6d54960784f86d52c913e4a8f5c9a9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.9 MB (49929793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb86494c128abaa467fc19a192852bfde9ae94e0d13aa1f9f1b70d9adb68697d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:54:49 GMT
ADD file:c85d28567b6123deb660b71c8b60d92378b5ba15ba5dcf495d9388817dc3aa44 in / 
# Tue, 09 Jun 2020 01:54:52 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 03:24:02 GMT
ENV MONO_VERSION=6.8.0.96
# Tue, 09 Jun 2020 03:24:21 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Jun 2020 03:25:06 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:622dc742b82743ebf5607b215a65869096390ee41b0a61b5532f859fb94590b1`  
		Last Modified: Tue, 09 Jun 2020 02:00:28 GMT  
		Size: 20.4 MB (20375150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:334cf34398cfa7031d68bad42f6b2a8d870a4ad5c2b0454f3f6fdd0fb4433237`  
		Last Modified: Tue, 09 Jun 2020 03:37:02 GMT  
		Size: 244.4 KB (244374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aa8cbd821b66a8c4a38ce3d6711cc1ee5489b04a017ab6a7fd368f08beec89e`  
		Last Modified: Tue, 09 Jun 2020 03:37:10 GMT  
		Size: 29.3 MB (29310269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8.0-slim` - linux; 386

```console
$ docker pull mono@sha256:e78d5446f93beef2216681d481890fe6388d64c704eb5cd4cc2e7010748818bd
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.9 MB (91909634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ebdb565c91f1fbc53a06cbfb5b9c374ab82f491c6934131ce4f1ae6524b43cf`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:42:33 GMT
ADD file:8ef252685ffefc58654053bf145c830928a2cf423a6c757180649df772f1523d in / 
# Tue, 09 Jun 2020 01:42:34 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 06:59:35 GMT
ENV MONO_VERSION=6.8.0.96
# Tue, 09 Jun 2020 06:59:46 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Jun 2020 07:00:24 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:4ffbd6ec7974e514763a8d7d9fcf5e86e9440e2280e6e9561ea373b4bc50588e`  
		Last Modified: Tue, 09 Jun 2020 01:48:28 GMT  
		Size: 23.1 MB (23147892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b3a90700548ab3df378beb07af7fba67e7ea89ead888d8c78d529c40633c7ed`  
		Last Modified: Tue, 09 Jun 2020 07:10:23 GMT  
		Size: 244.5 KB (244462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbcec5e4a352eead9b06946ed8fb1855a57123b280b3941614dac805987d5b65`  
		Last Modified: Tue, 09 Jun 2020 07:10:41 GMT  
		Size: 68.5 MB (68517280 bytes)  
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
$ docker pull mono@sha256:ce1717f66152b5a364712978c58f62ff0f06c11659d033fdafdf26fb7407e2f9
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
$ docker pull mono@sha256:a6e184082378911b563cafc02a2f4d4bc5b1c5a4ff0c2fbdf62471e2cbed0d68
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.2 MB (87231525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bd253379aef6e46ed99c035c08e92c0ec3d33da796131035aa4da08949ed069`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:23:35 GMT
ADD file:57b431451a292755d0f13673f5f3bea9f62aea36c7a1b59d34d7d200ba134fea in / 
# Tue, 09 Jun 2020 01:23:35 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 07:23:45 GMT
ENV MONO_VERSION=6.8.0.96
# Tue, 09 Jun 2020 07:23:55 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Jun 2020 07:24:27 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7d2977b12acb33f192e3f20b7e15a467cc8f3f5124a15d975a6d4afe5fa3d258`  
		Last Modified: Tue, 09 Jun 2020 01:28:13 GMT  
		Size: 22.5 MB (22519600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:086ef7a7e886327a728a6c520ae895632459590d19d2691114827740ae2f70e8`  
		Last Modified: Tue, 09 Jun 2020 07:57:38 GMT  
		Size: 244.5 KB (244473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28855cf8f97ad7e71803802cd6b3c77cc8335c628b34fc3f6283688061cdad11`  
		Last Modified: Tue, 09 Jun 2020 07:57:56 GMT  
		Size: 64.5 MB (64467452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:e6de1477ff957c4b2f0ab6f4f790dc1225b873ced9b789c54d346c25703217e6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.7 MB (46687221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efe6f734a291cceabb4881569dc5bda10268e94b9483be02ba8fdb2ba3d2f9c7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 00:55:12 GMT
ADD file:0b9f2b88887a8060402a052c243c31641d9c217edcdb232c7b7a057cf5a70d66 in / 
# Wed, 22 Jul 2020 00:55:13 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 04:47:49 GMT
ENV MONO_VERSION=6.8.0.96
# Wed, 22 Jul 2020 04:48:12 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jul 2020 04:49:00 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:319109fcb6fa9b08528c518426e7ce105aac7313066432efcea95f59ff6e6788`  
		Last Modified: Wed, 22 Jul 2020 01:03:27 GMT  
		Size: 21.2 MB (21189131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a62cce824a648193694f4121faf883e003fd11739ec85458d954e3cf0f8860ec`  
		Last Modified: Wed, 22 Jul 2020 05:02:47 GMT  
		Size: 244.5 KB (244541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f82e724d353f93153e6d1203349f4b687bc703c55e3b1cc2438b3ffad6974124`  
		Last Modified: Wed, 22 Jul 2020 05:02:55 GMT  
		Size: 25.3 MB (25253549 bytes)  
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
$ docker pull mono@sha256:24d8471bd7e59cc38ba65db018794a92fc6d54960784f86d52c913e4a8f5c9a9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.9 MB (49929793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb86494c128abaa467fc19a192852bfde9ae94e0d13aa1f9f1b70d9adb68697d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:54:49 GMT
ADD file:c85d28567b6123deb660b71c8b60d92378b5ba15ba5dcf495d9388817dc3aa44 in / 
# Tue, 09 Jun 2020 01:54:52 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 03:24:02 GMT
ENV MONO_VERSION=6.8.0.96
# Tue, 09 Jun 2020 03:24:21 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Jun 2020 03:25:06 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:622dc742b82743ebf5607b215a65869096390ee41b0a61b5532f859fb94590b1`  
		Last Modified: Tue, 09 Jun 2020 02:00:28 GMT  
		Size: 20.4 MB (20375150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:334cf34398cfa7031d68bad42f6b2a8d870a4ad5c2b0454f3f6fdd0fb4433237`  
		Last Modified: Tue, 09 Jun 2020 03:37:02 GMT  
		Size: 244.4 KB (244374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aa8cbd821b66a8c4a38ce3d6711cc1ee5489b04a017ab6a7fd368f08beec89e`  
		Last Modified: Tue, 09 Jun 2020 03:37:10 GMT  
		Size: 29.3 MB (29310269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8-slim` - linux; 386

```console
$ docker pull mono@sha256:e78d5446f93beef2216681d481890fe6388d64c704eb5cd4cc2e7010748818bd
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.9 MB (91909634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ebdb565c91f1fbc53a06cbfb5b9c374ab82f491c6934131ce4f1ae6524b43cf`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:42:33 GMT
ADD file:8ef252685ffefc58654053bf145c830928a2cf423a6c757180649df772f1523d in / 
# Tue, 09 Jun 2020 01:42:34 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 06:59:35 GMT
ENV MONO_VERSION=6.8.0.96
# Tue, 09 Jun 2020 06:59:46 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Jun 2020 07:00:24 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:4ffbd6ec7974e514763a8d7d9fcf5e86e9440e2280e6e9561ea373b4bc50588e`  
		Last Modified: Tue, 09 Jun 2020 01:48:28 GMT  
		Size: 23.1 MB (23147892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b3a90700548ab3df378beb07af7fba67e7ea89ead888d8c78d529c40633c7ed`  
		Last Modified: Tue, 09 Jun 2020 07:10:23 GMT  
		Size: 244.5 KB (244462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbcec5e4a352eead9b06946ed8fb1855a57123b280b3941614dac805987d5b65`  
		Last Modified: Tue, 09 Jun 2020 07:10:41 GMT  
		Size: 68.5 MB (68517280 bytes)  
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
$ docker pull mono@sha256:ce1717f66152b5a364712978c58f62ff0f06c11659d033fdafdf26fb7407e2f9
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
$ docker pull mono@sha256:a6e184082378911b563cafc02a2f4d4bc5b1c5a4ff0c2fbdf62471e2cbed0d68
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.2 MB (87231525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bd253379aef6e46ed99c035c08e92c0ec3d33da796131035aa4da08949ed069`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:23:35 GMT
ADD file:57b431451a292755d0f13673f5f3bea9f62aea36c7a1b59d34d7d200ba134fea in / 
# Tue, 09 Jun 2020 01:23:35 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 07:23:45 GMT
ENV MONO_VERSION=6.8.0.96
# Tue, 09 Jun 2020 07:23:55 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Jun 2020 07:24:27 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7d2977b12acb33f192e3f20b7e15a467cc8f3f5124a15d975a6d4afe5fa3d258`  
		Last Modified: Tue, 09 Jun 2020 01:28:13 GMT  
		Size: 22.5 MB (22519600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:086ef7a7e886327a728a6c520ae895632459590d19d2691114827740ae2f70e8`  
		Last Modified: Tue, 09 Jun 2020 07:57:38 GMT  
		Size: 244.5 KB (244473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28855cf8f97ad7e71803802cd6b3c77cc8335c628b34fc3f6283688061cdad11`  
		Last Modified: Tue, 09 Jun 2020 07:57:56 GMT  
		Size: 64.5 MB (64467452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:e6de1477ff957c4b2f0ab6f4f790dc1225b873ced9b789c54d346c25703217e6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.7 MB (46687221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efe6f734a291cceabb4881569dc5bda10268e94b9483be02ba8fdb2ba3d2f9c7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 00:55:12 GMT
ADD file:0b9f2b88887a8060402a052c243c31641d9c217edcdb232c7b7a057cf5a70d66 in / 
# Wed, 22 Jul 2020 00:55:13 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 04:47:49 GMT
ENV MONO_VERSION=6.8.0.96
# Wed, 22 Jul 2020 04:48:12 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jul 2020 04:49:00 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:319109fcb6fa9b08528c518426e7ce105aac7313066432efcea95f59ff6e6788`  
		Last Modified: Wed, 22 Jul 2020 01:03:27 GMT  
		Size: 21.2 MB (21189131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a62cce824a648193694f4121faf883e003fd11739ec85458d954e3cf0f8860ec`  
		Last Modified: Wed, 22 Jul 2020 05:02:47 GMT  
		Size: 244.5 KB (244541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f82e724d353f93153e6d1203349f4b687bc703c55e3b1cc2438b3ffad6974124`  
		Last Modified: Wed, 22 Jul 2020 05:02:55 GMT  
		Size: 25.3 MB (25253549 bytes)  
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
$ docker pull mono@sha256:24d8471bd7e59cc38ba65db018794a92fc6d54960784f86d52c913e4a8f5c9a9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.9 MB (49929793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb86494c128abaa467fc19a192852bfde9ae94e0d13aa1f9f1b70d9adb68697d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:54:49 GMT
ADD file:c85d28567b6123deb660b71c8b60d92378b5ba15ba5dcf495d9388817dc3aa44 in / 
# Tue, 09 Jun 2020 01:54:52 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 03:24:02 GMT
ENV MONO_VERSION=6.8.0.96
# Tue, 09 Jun 2020 03:24:21 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Jun 2020 03:25:06 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:622dc742b82743ebf5607b215a65869096390ee41b0a61b5532f859fb94590b1`  
		Last Modified: Tue, 09 Jun 2020 02:00:28 GMT  
		Size: 20.4 MB (20375150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:334cf34398cfa7031d68bad42f6b2a8d870a4ad5c2b0454f3f6fdd0fb4433237`  
		Last Modified: Tue, 09 Jun 2020 03:37:02 GMT  
		Size: 244.4 KB (244374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aa8cbd821b66a8c4a38ce3d6711cc1ee5489b04a017ab6a7fd368f08beec89e`  
		Last Modified: Tue, 09 Jun 2020 03:37:10 GMT  
		Size: 29.3 MB (29310269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6-slim` - linux; 386

```console
$ docker pull mono@sha256:e78d5446f93beef2216681d481890fe6388d64c704eb5cd4cc2e7010748818bd
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.9 MB (91909634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ebdb565c91f1fbc53a06cbfb5b9c374ab82f491c6934131ce4f1ae6524b43cf`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:42:33 GMT
ADD file:8ef252685ffefc58654053bf145c830928a2cf423a6c757180649df772f1523d in / 
# Tue, 09 Jun 2020 01:42:34 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 06:59:35 GMT
ENV MONO_VERSION=6.8.0.96
# Tue, 09 Jun 2020 06:59:46 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Jun 2020 07:00:24 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:4ffbd6ec7974e514763a8d7d9fcf5e86e9440e2280e6e9561ea373b4bc50588e`  
		Last Modified: Tue, 09 Jun 2020 01:48:28 GMT  
		Size: 23.1 MB (23147892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b3a90700548ab3df378beb07af7fba67e7ea89ead888d8c78d529c40633c7ed`  
		Last Modified: Tue, 09 Jun 2020 07:10:23 GMT  
		Size: 244.5 KB (244462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbcec5e4a352eead9b06946ed8fb1855a57123b280b3941614dac805987d5b65`  
		Last Modified: Tue, 09 Jun 2020 07:10:41 GMT  
		Size: 68.5 MB (68517280 bytes)  
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
$ docker pull mono@sha256:4edd8d6d3134e4de4f25836d12a6a9a9de23fa572846e74709b2f19f7371995a
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
$ docker pull mono@sha256:d4717190e9fd6118cb2775e2f084daf223583c24bc1f014c33dea48485bc7ff2
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.0 MB (235024583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a6baf0a892689f2f75227c4c04ab734c8497ab6853b037bb733184b2417c751`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:23:35 GMT
ADD file:57b431451a292755d0f13673f5f3bea9f62aea36c7a1b59d34d7d200ba134fea in / 
# Tue, 09 Jun 2020 01:23:35 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 07:23:45 GMT
ENV MONO_VERSION=6.8.0.96
# Tue, 09 Jun 2020 07:23:55 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Jun 2020 07:24:27 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 09 Jun 2020 07:36:17 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7d2977b12acb33f192e3f20b7e15a467cc8f3f5124a15d975a6d4afe5fa3d258`  
		Last Modified: Tue, 09 Jun 2020 01:28:13 GMT  
		Size: 22.5 MB (22519600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:086ef7a7e886327a728a6c520ae895632459590d19d2691114827740ae2f70e8`  
		Last Modified: Tue, 09 Jun 2020 07:57:38 GMT  
		Size: 244.5 KB (244473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28855cf8f97ad7e71803802cd6b3c77cc8335c628b34fc3f6283688061cdad11`  
		Last Modified: Tue, 09 Jun 2020 07:57:56 GMT  
		Size: 64.5 MB (64467452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e1b1cfd1a055e22c600005e10f64b8b2b3557bff82aa4bc012ab66cb8786346`  
		Last Modified: Tue, 09 Jun 2020 07:59:31 GMT  
		Size: 147.8 MB (147793058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:latest` - linux; arm variant v5

```console
$ docker pull mono@sha256:899467182dd8b6e055181cdce28cc3cae6935b0d914393224be26af46629c004
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.6 MB (176588520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42bd2219f249736535bcd1ba211ff5d352edc655fe81450544fbb344fc18b015`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 00:55:12 GMT
ADD file:0b9f2b88887a8060402a052c243c31641d9c217edcdb232c7b7a057cf5a70d66 in / 
# Wed, 22 Jul 2020 00:55:13 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 04:47:49 GMT
ENV MONO_VERSION=6.8.0.96
# Wed, 22 Jul 2020 04:48:12 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jul 2020 04:49:00 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 22 Jul 2020 04:55:31 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:319109fcb6fa9b08528c518426e7ce105aac7313066432efcea95f59ff6e6788`  
		Last Modified: Wed, 22 Jul 2020 01:03:27 GMT  
		Size: 21.2 MB (21189131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a62cce824a648193694f4121faf883e003fd11739ec85458d954e3cf0f8860ec`  
		Last Modified: Wed, 22 Jul 2020 05:02:47 GMT  
		Size: 244.5 KB (244541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f82e724d353f93153e6d1203349f4b687bc703c55e3b1cc2438b3ffad6974124`  
		Last Modified: Wed, 22 Jul 2020 05:02:55 GMT  
		Size: 25.3 MB (25253549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:225b191f3416f0c2fd00c0c702d8819f8c61a0faece5b5d2dcb4815b23191907`  
		Last Modified: Wed, 22 Jul 2020 05:04:19 GMT  
		Size: 129.9 MB (129901299 bytes)  
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
$ docker pull mono@sha256:68d1db7da63e2106ddea8d7850cf3badfaa16a94d8d23a12910f86785e4decc8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.6 MB (194642181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf6ff587bef5367449ceee09405f75d3b5a38e19c0d360ec43da1874b37497aa`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:54:49 GMT
ADD file:c85d28567b6123deb660b71c8b60d92378b5ba15ba5dcf495d9388817dc3aa44 in / 
# Tue, 09 Jun 2020 01:54:52 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 03:24:02 GMT
ENV MONO_VERSION=6.8.0.96
# Tue, 09 Jun 2020 03:24:21 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Jun 2020 03:25:06 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 09 Jun 2020 03:30:31 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:622dc742b82743ebf5607b215a65869096390ee41b0a61b5532f859fb94590b1`  
		Last Modified: Tue, 09 Jun 2020 02:00:28 GMT  
		Size: 20.4 MB (20375150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:334cf34398cfa7031d68bad42f6b2a8d870a4ad5c2b0454f3f6fdd0fb4433237`  
		Last Modified: Tue, 09 Jun 2020 03:37:02 GMT  
		Size: 244.4 KB (244374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aa8cbd821b66a8c4a38ce3d6711cc1ee5489b04a017ab6a7fd368f08beec89e`  
		Last Modified: Tue, 09 Jun 2020 03:37:10 GMT  
		Size: 29.3 MB (29310269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f78bf65ea03cc9db2213ce7ff8e07d3a77604a43ef0a7d81b88b5c965515dfe`  
		Last Modified: Tue, 09 Jun 2020 03:38:38 GMT  
		Size: 144.7 MB (144712388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:latest` - linux; 386

```console
$ docker pull mono@sha256:443376dd685b5fcd1e0b6b7a685c5b6a24a79fad8b9619e983293b70e84c8bb6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.4 MB (243401430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6948fdbf966360cb7a728eae30756da2daa5cc4b0362dd09e3a352f4ee44e5dc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:42:33 GMT
ADD file:8ef252685ffefc58654053bf145c830928a2cf423a6c757180649df772f1523d in / 
# Tue, 09 Jun 2020 01:42:34 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 06:59:35 GMT
ENV MONO_VERSION=6.8.0.96
# Tue, 09 Jun 2020 06:59:46 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Jun 2020 07:00:24 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 09 Jun 2020 07:05:03 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:4ffbd6ec7974e514763a8d7d9fcf5e86e9440e2280e6e9561ea373b4bc50588e`  
		Last Modified: Tue, 09 Jun 2020 01:48:28 GMT  
		Size: 23.1 MB (23147892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b3a90700548ab3df378beb07af7fba67e7ea89ead888d8c78d529c40633c7ed`  
		Last Modified: Tue, 09 Jun 2020 07:10:23 GMT  
		Size: 244.5 KB (244462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbcec5e4a352eead9b06946ed8fb1855a57123b280b3941614dac805987d5b65`  
		Last Modified: Tue, 09 Jun 2020 07:10:41 GMT  
		Size: 68.5 MB (68517280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae8167823b3a297ca26719112fd4ae0b1b90e5df5ef7edf3302022c64061697f`  
		Last Modified: Tue, 09 Jun 2020 07:12:09 GMT  
		Size: 151.5 MB (151491796 bytes)  
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
$ docker pull mono@sha256:ce1717f66152b5a364712978c58f62ff0f06c11659d033fdafdf26fb7407e2f9
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
$ docker pull mono@sha256:a6e184082378911b563cafc02a2f4d4bc5b1c5a4ff0c2fbdf62471e2cbed0d68
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.2 MB (87231525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bd253379aef6e46ed99c035c08e92c0ec3d33da796131035aa4da08949ed069`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:23:35 GMT
ADD file:57b431451a292755d0f13673f5f3bea9f62aea36c7a1b59d34d7d200ba134fea in / 
# Tue, 09 Jun 2020 01:23:35 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 07:23:45 GMT
ENV MONO_VERSION=6.8.0.96
# Tue, 09 Jun 2020 07:23:55 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Jun 2020 07:24:27 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7d2977b12acb33f192e3f20b7e15a467cc8f3f5124a15d975a6d4afe5fa3d258`  
		Last Modified: Tue, 09 Jun 2020 01:28:13 GMT  
		Size: 22.5 MB (22519600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:086ef7a7e886327a728a6c520ae895632459590d19d2691114827740ae2f70e8`  
		Last Modified: Tue, 09 Jun 2020 07:57:38 GMT  
		Size: 244.5 KB (244473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28855cf8f97ad7e71803802cd6b3c77cc8335c628b34fc3f6283688061cdad11`  
		Last Modified: Tue, 09 Jun 2020 07:57:56 GMT  
		Size: 64.5 MB (64467452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:e6de1477ff957c4b2f0ab6f4f790dc1225b873ced9b789c54d346c25703217e6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.7 MB (46687221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efe6f734a291cceabb4881569dc5bda10268e94b9483be02ba8fdb2ba3d2f9c7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 00:55:12 GMT
ADD file:0b9f2b88887a8060402a052c243c31641d9c217edcdb232c7b7a057cf5a70d66 in / 
# Wed, 22 Jul 2020 00:55:13 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 04:47:49 GMT
ENV MONO_VERSION=6.8.0.96
# Wed, 22 Jul 2020 04:48:12 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 22 Jul 2020 04:49:00 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:319109fcb6fa9b08528c518426e7ce105aac7313066432efcea95f59ff6e6788`  
		Last Modified: Wed, 22 Jul 2020 01:03:27 GMT  
		Size: 21.2 MB (21189131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a62cce824a648193694f4121faf883e003fd11739ec85458d954e3cf0f8860ec`  
		Last Modified: Wed, 22 Jul 2020 05:02:47 GMT  
		Size: 244.5 KB (244541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f82e724d353f93153e6d1203349f4b687bc703c55e3b1cc2438b3ffad6974124`  
		Last Modified: Wed, 22 Jul 2020 05:02:55 GMT  
		Size: 25.3 MB (25253549 bytes)  
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
$ docker pull mono@sha256:24d8471bd7e59cc38ba65db018794a92fc6d54960784f86d52c913e4a8f5c9a9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.9 MB (49929793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb86494c128abaa467fc19a192852bfde9ae94e0d13aa1f9f1b70d9adb68697d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:54:49 GMT
ADD file:c85d28567b6123deb660b71c8b60d92378b5ba15ba5dcf495d9388817dc3aa44 in / 
# Tue, 09 Jun 2020 01:54:52 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 03:24:02 GMT
ENV MONO_VERSION=6.8.0.96
# Tue, 09 Jun 2020 03:24:21 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Jun 2020 03:25:06 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:622dc742b82743ebf5607b215a65869096390ee41b0a61b5532f859fb94590b1`  
		Last Modified: Tue, 09 Jun 2020 02:00:28 GMT  
		Size: 20.4 MB (20375150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:334cf34398cfa7031d68bad42f6b2a8d870a4ad5c2b0454f3f6fdd0fb4433237`  
		Last Modified: Tue, 09 Jun 2020 03:37:02 GMT  
		Size: 244.4 KB (244374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aa8cbd821b66a8c4a38ce3d6711cc1ee5489b04a017ab6a7fd368f08beec89e`  
		Last Modified: Tue, 09 Jun 2020 03:37:10 GMT  
		Size: 29.3 MB (29310269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:slim` - linux; 386

```console
$ docker pull mono@sha256:e78d5446f93beef2216681d481890fe6388d64c704eb5cd4cc2e7010748818bd
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.9 MB (91909634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ebdb565c91f1fbc53a06cbfb5b9c374ab82f491c6934131ce4f1ae6524b43cf`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:42:33 GMT
ADD file:8ef252685ffefc58654053bf145c830928a2cf423a6c757180649df772f1523d in / 
# Tue, 09 Jun 2020 01:42:34 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 06:59:35 GMT
ENV MONO_VERSION=6.8.0.96
# Tue, 09 Jun 2020 06:59:46 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Jun 2020 07:00:24 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:4ffbd6ec7974e514763a8d7d9fcf5e86e9440e2280e6e9561ea373b4bc50588e`  
		Last Modified: Tue, 09 Jun 2020 01:48:28 GMT  
		Size: 23.1 MB (23147892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b3a90700548ab3df378beb07af7fba67e7ea89ead888d8c78d529c40633c7ed`  
		Last Modified: Tue, 09 Jun 2020 07:10:23 GMT  
		Size: 244.5 KB (244462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbcec5e4a352eead9b06946ed8fb1855a57123b280b3941614dac805987d5b65`  
		Last Modified: Tue, 09 Jun 2020 07:10:41 GMT  
		Size: 68.5 MB (68517280 bytes)  
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
