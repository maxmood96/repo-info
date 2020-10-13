## `mono:slim`

```console
$ docker pull mono@sha256:2908c04bb370f95935550b9fea10a6b96ca036ae71b32d17128402a624a327a2
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
$ docker pull mono@sha256:73fadf674046469a3fc25c496c1fb3ac58ad2eda9e26aa126e5479306ed0cf95
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94440255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9430b8012739f9826cdd9f118f69e95b47e049a35266f1c31f50002f1024fd57`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 10 Sep 2020 00:23:29 GMT
ADD file:e7407f2294ad23634565820b9669b18ff2a2ca0212a7ec84b9c89d8550859954 in / 
# Thu, 10 Sep 2020 00:23:30 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 06:19:25 GMT
ENV MONO_VERSION=6.10.0.104
# Thu, 10 Sep 2020 06:19:35 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 10 Sep 2020 06:20:13 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:d121f8d1c4128ebc1e95e5bfad90a0189b84eadbbb2fbaad20cbb26d20b2c8a2`  
		Last Modified: Thu, 10 Sep 2020 00:34:02 GMT  
		Size: 27.1 MB (27092161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:140dba57f56b96691dfd0551d17470bb5f21984005c4c372509a3cc39d8618ff`  
		Last Modified: Thu, 10 Sep 2020 06:39:36 GMT  
		Size: 255.9 KB (255922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad432be9d8d43b429c26f097fa65f3e8ce3af20bd0cff99c69f5ae3ba83d421b`  
		Last Modified: Thu, 10 Sep 2020 06:39:51 GMT  
		Size: 67.1 MB (67092172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:4f1935b74f258609d63b31cd01cabf54f735b72c77385b4d0486116f7b9ef1db
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51622580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8aaea1ec0574bca839c762a7724f248e6384ba44765e12d60a1eeb21f04760d2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Oct 2020 01:52:17 GMT
ADD file:b71c0fa4957d6b65af37231a105f3d17cdbafe5c7d6c37b5843ebf619c608aaa in / 
# Tue, 13 Oct 2020 01:52:27 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 02:36:19 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 13 Oct 2020 02:36:43 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 13 Oct 2020 02:37:31 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:f991c1e1ee2c48f16625b6b61310bf3c0616c0dbda4762019117e86fd29cf9ce`  
		Last Modified: Tue, 13 Oct 2020 02:01:27 GMT  
		Size: 24.8 MB (24835992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d27e131b9898d8f02267f410169b8627b889f6585ad9300d14a4775194301b55`  
		Last Modified: Tue, 13 Oct 2020 02:44:49 GMT  
		Size: 255.9 KB (255938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07b82cc14a51474e2d05a0fd59b3fde70aa8fda539de5a302992983e4ffce7b8`  
		Last Modified: Tue, 13 Oct 2020 02:45:01 GMT  
		Size: 26.5 MB (26530650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:bf61cbd2fff2e9323d1f89b46e33accc00aa6aef0f7f4ab533d44ff2d3672097
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48685097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4593f3eb7182d83642b75181ed79a20590556ea1d6460aef0cad9e805bef1e10`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Oct 2020 00:59:29 GMT
ADD file:e423f30ca19eb205a98de21b0545d0a764cfc4f832a9a9631542354d914d98d9 in / 
# Tue, 13 Oct 2020 00:59:31 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 04:43:09 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 13 Oct 2020 04:43:27 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 13 Oct 2020 04:44:11 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:d6d8411ad43db0022fa0fce094cd2e8b1dd2f8a09d6880ed9beb6b4204867027`  
		Last Modified: Tue, 13 Oct 2020 01:08:28 GMT  
		Size: 22.7 MB (22699849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5228b93feed3135603bc1b4bbda140b6e3e712167c9dd5ccaad1732370cd6b93`  
		Last Modified: Tue, 13 Oct 2020 04:50:37 GMT  
		Size: 255.9 KB (255921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4e85494910fa31cd3bb70be77361cab8fa0b333de462a10ce0e2181ee165c0a`  
		Last Modified: Tue, 13 Oct 2020 04:50:46 GMT  
		Size: 25.7 MB (25729327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:837debd8ec883ec2335ef1d2a49134236314f42b645ff3f6c7c3bba8edd39122
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.9 MB (57855412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a67ab8b67f587104f2fad4384a16c674fd915ee9365d079ff0007afd7fc611a6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 09 Sep 2020 23:50:54 GMT
ADD file:d870fb0484ea283840d9cc923c9c3fe36d1bb6b3b5ecfefcce06aa26a22c9414 in / 
# Wed, 09 Sep 2020 23:50:57 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 04:11:35 GMT
ENV MONO_VERSION=6.10.0.104
# Thu, 10 Sep 2020 04:11:50 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 10 Sep 2020 04:12:25 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a6d76de28f58f3470aff71c934c0fec4e5d0fad788f8b8bcc50601266fc1b34d`  
		Last Modified: Wed, 09 Sep 2020 23:59:09 GMT  
		Size: 25.8 MB (25849325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e6286cef3ccb7f414187d0d407d414d80aefc9cbac5f8afc8b61c2144468e9d`  
		Last Modified: Thu, 10 Sep 2020 04:18:37 GMT  
		Size: 255.9 KB (255919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2922d176e5f282d1cab4d82a18705798bb201e72254252e9365c6e6d79f9193`  
		Last Modified: Thu, 10 Sep 2020 04:18:47 GMT  
		Size: 31.8 MB (31750168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:slim` - linux; 386

```console
$ docker pull mono@sha256:2a9fab669e67041d25fdb369e933e3590824683abc66c630331417cfc165ba14
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.1 MB (99142396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cc2e1b2ceaeba60abb7a332bf82875ce0709f9c94f0eda84ca9f39bc53f8b70`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 09 Sep 2020 23:40:19 GMT
ADD file:08dc20c9cd727ebf02cac6e4b287c3009274682174aee9222494491cd6c671b8 in / 
# Wed, 09 Sep 2020 23:40:19 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 02:37:15 GMT
ENV MONO_VERSION=6.10.0.104
# Thu, 10 Sep 2020 02:37:27 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 10 Sep 2020 02:38:12 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:31e6582dbd9f9a84903d46339df0c393a63d2cbfb001b06b3204653cceafcc61`  
		Last Modified: Wed, 09 Sep 2020 23:46:30 GMT  
		Size: 27.8 MB (27750334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10a5b4050174b76ed23d2d3bbb436d66899f93eba56641cd1faf810f75242c67`  
		Last Modified: Thu, 10 Sep 2020 02:44:13 GMT  
		Size: 255.8 KB (255795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a251d8984c7c93892d00e6d7ad246f6eb96eb1ccef85f2aa4931d99e3fa536d0`  
		Last Modified: Thu, 10 Sep 2020 02:44:42 GMT  
		Size: 71.1 MB (71136267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:slim` - linux; ppc64le

```console
$ docker pull mono@sha256:0747d27029d283c5d079fd0b849b546bb95eeae5adf789b192f20a6714a1f523
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60124211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60fa8a532fd76be8dc5c2045033500043c8b1d5a968372c9b52cfd0f3819eb3e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 10 Sep 2020 01:06:11 GMT
ADD file:4dede556abae88027bd22f3166fdbc38778a6fcd686c5ce768c3ca024ab3f9cf in / 
# Thu, 10 Sep 2020 01:06:20 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 19:01:16 GMT
ENV MONO_VERSION=6.10.0.104
# Thu, 10 Sep 2020 19:05:10 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 10 Sep 2020 19:07:24 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:f8aef3d2247e5f990bc767bc99f575b9bcec34aaa37183414eebe28fcd09519d`  
		Last Modified: Thu, 10 Sep 2020 01:28:12 GMT  
		Size: 30.5 MB (30517880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91a5b381ce455eca298e810bbcff286cc9167c82392b00241d01cc6bc65cfe86`  
		Last Modified: Thu, 10 Sep 2020 19:42:19 GMT  
		Size: 256.3 KB (256260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3df1215b828b18d641c32013a7c8597874acf4085e9fc7b404d9216a5e67ecc3`  
		Last Modified: Thu, 10 Sep 2020 19:42:28 GMT  
		Size: 29.4 MB (29350071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
