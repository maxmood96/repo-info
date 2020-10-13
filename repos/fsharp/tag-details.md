<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `fsharp`

-	[`fsharp:10`](#fsharp10)
-	[`fsharp:10.7`](#fsharp107)
-	[`fsharp:10.7.0`](#fsharp1070)
-	[`fsharp:10.7.0-netcore`](#fsharp1070-netcore)
-	[`fsharp:10.7-netcore`](#fsharp107-netcore)
-	[`fsharp:10-netcore`](#fsharp10-netcore)
-	[`fsharp:4`](#fsharp4)
-	[`fsharp:4.1`](#fsharp41)
-	[`fsharp:4.1.34`](#fsharp4134)
-	[`fsharp:latest`](#fsharplatest)
-	[`fsharp:netcore`](#fsharpnetcore)

## `fsharp:10`

```console
$ docker pull fsharp@sha256:2e1a5e8854e63fd437f4fb312cd3bc074ddd6a0c1c5e482f6eb3f5eb6a04fb33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `fsharp:10` - linux; amd64

```console
$ docker pull fsharp@sha256:1be0abf91a4e1a37906acfa0391cd3c413f91100a8d60a167cc47df8dd7857cf
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.6 MB (186621433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a19ba504662e2d2240a9eee95446b3dd474a3137a8d6f102cc2e4f6519dbb82b`
-	Default Command: `["fsharpi"]`

```dockerfile
# Tue, 13 Oct 2020 01:39:05 GMT
ADD file:0dc53e7886c35bc21ae6c4f6cedda54d56ae9c9e9cd367678f1a72e68b3c43d4 in / 
# Tue, 13 Oct 2020 01:39:05 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 06:44:51 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Steve Desmond <steve@stevedesmond.ca>
# Tue, 13 Oct 2020 06:44:51 GMT
ENV MONO_THREADS_PER_CPU=50
# Tue, 13 Oct 2020 06:57:14 GMT
RUN MONO_VERSION=6.8.0.105 &&     FSHARP_VERSION=10.2.3 &&     FSHARP_BASENAME=fsharp-$FSHARP_VERSION &&     FSHARP_ARCHIVE=$FSHARP_VERSION.tar.gz &&     FSHARP_ARCHIVE_URL=https://github.com/fsharp/fsharp/archive/$FSHARP_VERSION.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     apt-get update && apt-get --no-install-recommends install -y gnupg dirmngr ca-certificates apt-transport-https &&     apt-key adv --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF &&     echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" | tee /etc/apt/sources.list.d/mono-official-stable.list &&     apt-get update -y &&     apt-get --no-install-recommends install -y pkg-config make nuget mono-devel msbuild ca-certificates-mono locales &&     rm -rf /var/lib/apt/lists/* &&     echo 'en_US.UTF-8 UTF-8' > /etc/locale.gen && /usr/sbin/locale-gen &&     mkdir -p /tmp/src &&     cd /tmp/src &&     printf "namespace a { class b { public static void Main(string[] args) { new System.Net.WebClient().DownloadFile(\"%s\", \"%s\");}}}" $FSHARP_ARCHIVE_URL $FSHARP_ARCHIVE > download-fsharp.cs &&     mcs download-fsharp.cs && mono download-fsharp.exe && rm download-fsharp.exe download-fsharp.cs &&     tar xf $FSHARP_ARCHIVE &&     cd $FSHARP_BASENAME &&     make &&     make install &&     cd ~ &&     rm -rf /tmp/src /tmp/NuGetScratch ~/.nuget ~/.config ~/.local "$GNUPGHOME" &&     apt-get purge -y make gnupg dirmngr &&     apt-get clean
# Tue, 13 Oct 2020 06:57:15 GMT
WORKDIR /root
# Tue, 13 Oct 2020 06:57:15 GMT
CMD ["fsharpi"]
```

-	Layers:
	-	`sha256:bb79b6b2107fea8e8a47133a660b78e3a546998fcf0427be39ac9a0af4a97e90`  
		Last Modified: Tue, 13 Oct 2020 01:48:17 GMT  
		Size: 27.1 MB (27092228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:529ea17475edae1e854ee868ace575ed7a796bb85204b6ac6e5288984d1089f9`  
		Last Modified: Tue, 13 Oct 2020 07:13:15 GMT  
		Size: 159.5 MB (159529205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fsharp:10` - linux; arm64 variant v8

```console
$ docker pull fsharp@sha256:7f37d8f06cc2045142946c3af6c66c72dd2c34a04b4b6e65df0d202e71f2a6c1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.6 MB (183616406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:380ff0d99e05d272abe4d85af5295cddf539d1961abc1115a1b4c7fcb9391eeb`
-	Default Command: `["fsharpi"]`

```dockerfile
# Tue, 13 Oct 2020 01:41:09 GMT
ADD file:3488b1423094a75be5bb5956e9187827b8dd35d7a1f2b14081f8e74a1629e7d0 in / 
# Tue, 13 Oct 2020 01:41:11 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 02:08:20 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Steve Desmond <steve@stevedesmond.ca>
# Tue, 13 Oct 2020 02:08:21 GMT
ENV MONO_THREADS_PER_CPU=50
# Tue, 13 Oct 2020 02:27:00 GMT
RUN MONO_VERSION=6.8.0.105 &&     FSHARP_VERSION=10.2.3 &&     FSHARP_BASENAME=fsharp-$FSHARP_VERSION &&     FSHARP_ARCHIVE=$FSHARP_VERSION.tar.gz &&     FSHARP_ARCHIVE_URL=https://github.com/fsharp/fsharp/archive/$FSHARP_VERSION.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     apt-get update && apt-get --no-install-recommends install -y gnupg dirmngr ca-certificates apt-transport-https &&     apt-key adv --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF &&     echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" | tee /etc/apt/sources.list.d/mono-official-stable.list &&     apt-get update -y &&     apt-get --no-install-recommends install -y pkg-config make nuget mono-devel msbuild ca-certificates-mono locales &&     rm -rf /var/lib/apt/lists/* &&     echo 'en_US.UTF-8 UTF-8' > /etc/locale.gen && /usr/sbin/locale-gen &&     mkdir -p /tmp/src &&     cd /tmp/src &&     printf "namespace a { class b { public static void Main(string[] args) { new System.Net.WebClient().DownloadFile(\"%s\", \"%s\");}}}" $FSHARP_ARCHIVE_URL $FSHARP_ARCHIVE > download-fsharp.cs &&     mcs download-fsharp.cs && mono download-fsharp.exe && rm download-fsharp.exe download-fsharp.cs &&     tar xf $FSHARP_ARCHIVE &&     cd $FSHARP_BASENAME &&     make &&     make install &&     cd ~ &&     rm -rf /tmp/src /tmp/NuGetScratch ~/.nuget ~/.config ~/.local "$GNUPGHOME" &&     apt-get purge -y make gnupg dirmngr &&     apt-get clean
# Tue, 13 Oct 2020 02:27:08 GMT
WORKDIR /root
# Tue, 13 Oct 2020 02:27:10 GMT
CMD ["fsharpi"]
```

-	Layers:
	-	`sha256:4e6164a63b7b4cf981546947e191644c122214975d40b51ede0536791ebec3d4`  
		Last Modified: Tue, 13 Oct 2020 01:48:17 GMT  
		Size: 25.8 MB (25849329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29cc5bd99c5182580c6fc18aa496c999caed5c87f1d6bfc8d81725da288d90f7`  
		Last Modified: Tue, 13 Oct 2020 02:28:23 GMT  
		Size: 157.8 MB (157767077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `fsharp:10.7`

```console
$ docker pull fsharp@sha256:2e1a5e8854e63fd437f4fb312cd3bc074ddd6a0c1c5e482f6eb3f5eb6a04fb33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `fsharp:10.7` - linux; amd64

```console
$ docker pull fsharp@sha256:1be0abf91a4e1a37906acfa0391cd3c413f91100a8d60a167cc47df8dd7857cf
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.6 MB (186621433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a19ba504662e2d2240a9eee95446b3dd474a3137a8d6f102cc2e4f6519dbb82b`
-	Default Command: `["fsharpi"]`

```dockerfile
# Tue, 13 Oct 2020 01:39:05 GMT
ADD file:0dc53e7886c35bc21ae6c4f6cedda54d56ae9c9e9cd367678f1a72e68b3c43d4 in / 
# Tue, 13 Oct 2020 01:39:05 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 06:44:51 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Steve Desmond <steve@stevedesmond.ca>
# Tue, 13 Oct 2020 06:44:51 GMT
ENV MONO_THREADS_PER_CPU=50
# Tue, 13 Oct 2020 06:57:14 GMT
RUN MONO_VERSION=6.8.0.105 &&     FSHARP_VERSION=10.2.3 &&     FSHARP_BASENAME=fsharp-$FSHARP_VERSION &&     FSHARP_ARCHIVE=$FSHARP_VERSION.tar.gz &&     FSHARP_ARCHIVE_URL=https://github.com/fsharp/fsharp/archive/$FSHARP_VERSION.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     apt-get update && apt-get --no-install-recommends install -y gnupg dirmngr ca-certificates apt-transport-https &&     apt-key adv --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF &&     echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" | tee /etc/apt/sources.list.d/mono-official-stable.list &&     apt-get update -y &&     apt-get --no-install-recommends install -y pkg-config make nuget mono-devel msbuild ca-certificates-mono locales &&     rm -rf /var/lib/apt/lists/* &&     echo 'en_US.UTF-8 UTF-8' > /etc/locale.gen && /usr/sbin/locale-gen &&     mkdir -p /tmp/src &&     cd /tmp/src &&     printf "namespace a { class b { public static void Main(string[] args) { new System.Net.WebClient().DownloadFile(\"%s\", \"%s\");}}}" $FSHARP_ARCHIVE_URL $FSHARP_ARCHIVE > download-fsharp.cs &&     mcs download-fsharp.cs && mono download-fsharp.exe && rm download-fsharp.exe download-fsharp.cs &&     tar xf $FSHARP_ARCHIVE &&     cd $FSHARP_BASENAME &&     make &&     make install &&     cd ~ &&     rm -rf /tmp/src /tmp/NuGetScratch ~/.nuget ~/.config ~/.local "$GNUPGHOME" &&     apt-get purge -y make gnupg dirmngr &&     apt-get clean
# Tue, 13 Oct 2020 06:57:15 GMT
WORKDIR /root
# Tue, 13 Oct 2020 06:57:15 GMT
CMD ["fsharpi"]
```

-	Layers:
	-	`sha256:bb79b6b2107fea8e8a47133a660b78e3a546998fcf0427be39ac9a0af4a97e90`  
		Last Modified: Tue, 13 Oct 2020 01:48:17 GMT  
		Size: 27.1 MB (27092228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:529ea17475edae1e854ee868ace575ed7a796bb85204b6ac6e5288984d1089f9`  
		Last Modified: Tue, 13 Oct 2020 07:13:15 GMT  
		Size: 159.5 MB (159529205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fsharp:10.7` - linux; arm64 variant v8

```console
$ docker pull fsharp@sha256:7f37d8f06cc2045142946c3af6c66c72dd2c34a04b4b6e65df0d202e71f2a6c1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.6 MB (183616406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:380ff0d99e05d272abe4d85af5295cddf539d1961abc1115a1b4c7fcb9391eeb`
-	Default Command: `["fsharpi"]`

```dockerfile
# Tue, 13 Oct 2020 01:41:09 GMT
ADD file:3488b1423094a75be5bb5956e9187827b8dd35d7a1f2b14081f8e74a1629e7d0 in / 
# Tue, 13 Oct 2020 01:41:11 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 02:08:20 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Steve Desmond <steve@stevedesmond.ca>
# Tue, 13 Oct 2020 02:08:21 GMT
ENV MONO_THREADS_PER_CPU=50
# Tue, 13 Oct 2020 02:27:00 GMT
RUN MONO_VERSION=6.8.0.105 &&     FSHARP_VERSION=10.2.3 &&     FSHARP_BASENAME=fsharp-$FSHARP_VERSION &&     FSHARP_ARCHIVE=$FSHARP_VERSION.tar.gz &&     FSHARP_ARCHIVE_URL=https://github.com/fsharp/fsharp/archive/$FSHARP_VERSION.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     apt-get update && apt-get --no-install-recommends install -y gnupg dirmngr ca-certificates apt-transport-https &&     apt-key adv --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF &&     echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" | tee /etc/apt/sources.list.d/mono-official-stable.list &&     apt-get update -y &&     apt-get --no-install-recommends install -y pkg-config make nuget mono-devel msbuild ca-certificates-mono locales &&     rm -rf /var/lib/apt/lists/* &&     echo 'en_US.UTF-8 UTF-8' > /etc/locale.gen && /usr/sbin/locale-gen &&     mkdir -p /tmp/src &&     cd /tmp/src &&     printf "namespace a { class b { public static void Main(string[] args) { new System.Net.WebClient().DownloadFile(\"%s\", \"%s\");}}}" $FSHARP_ARCHIVE_URL $FSHARP_ARCHIVE > download-fsharp.cs &&     mcs download-fsharp.cs && mono download-fsharp.exe && rm download-fsharp.exe download-fsharp.cs &&     tar xf $FSHARP_ARCHIVE &&     cd $FSHARP_BASENAME &&     make &&     make install &&     cd ~ &&     rm -rf /tmp/src /tmp/NuGetScratch ~/.nuget ~/.config ~/.local "$GNUPGHOME" &&     apt-get purge -y make gnupg dirmngr &&     apt-get clean
# Tue, 13 Oct 2020 02:27:08 GMT
WORKDIR /root
# Tue, 13 Oct 2020 02:27:10 GMT
CMD ["fsharpi"]
```

-	Layers:
	-	`sha256:4e6164a63b7b4cf981546947e191644c122214975d40b51ede0536791ebec3d4`  
		Last Modified: Tue, 13 Oct 2020 01:48:17 GMT  
		Size: 25.8 MB (25849329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29cc5bd99c5182580c6fc18aa496c999caed5c87f1d6bfc8d81725da288d90f7`  
		Last Modified: Tue, 13 Oct 2020 02:28:23 GMT  
		Size: 157.8 MB (157767077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `fsharp:10.7.0`

```console
$ docker pull fsharp@sha256:2e1a5e8854e63fd437f4fb312cd3bc074ddd6a0c1c5e482f6eb3f5eb6a04fb33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `fsharp:10.7.0` - linux; amd64

```console
$ docker pull fsharp@sha256:1be0abf91a4e1a37906acfa0391cd3c413f91100a8d60a167cc47df8dd7857cf
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.6 MB (186621433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a19ba504662e2d2240a9eee95446b3dd474a3137a8d6f102cc2e4f6519dbb82b`
-	Default Command: `["fsharpi"]`

```dockerfile
# Tue, 13 Oct 2020 01:39:05 GMT
ADD file:0dc53e7886c35bc21ae6c4f6cedda54d56ae9c9e9cd367678f1a72e68b3c43d4 in / 
# Tue, 13 Oct 2020 01:39:05 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 06:44:51 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Steve Desmond <steve@stevedesmond.ca>
# Tue, 13 Oct 2020 06:44:51 GMT
ENV MONO_THREADS_PER_CPU=50
# Tue, 13 Oct 2020 06:57:14 GMT
RUN MONO_VERSION=6.8.0.105 &&     FSHARP_VERSION=10.2.3 &&     FSHARP_BASENAME=fsharp-$FSHARP_VERSION &&     FSHARP_ARCHIVE=$FSHARP_VERSION.tar.gz &&     FSHARP_ARCHIVE_URL=https://github.com/fsharp/fsharp/archive/$FSHARP_VERSION.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     apt-get update && apt-get --no-install-recommends install -y gnupg dirmngr ca-certificates apt-transport-https &&     apt-key adv --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF &&     echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" | tee /etc/apt/sources.list.d/mono-official-stable.list &&     apt-get update -y &&     apt-get --no-install-recommends install -y pkg-config make nuget mono-devel msbuild ca-certificates-mono locales &&     rm -rf /var/lib/apt/lists/* &&     echo 'en_US.UTF-8 UTF-8' > /etc/locale.gen && /usr/sbin/locale-gen &&     mkdir -p /tmp/src &&     cd /tmp/src &&     printf "namespace a { class b { public static void Main(string[] args) { new System.Net.WebClient().DownloadFile(\"%s\", \"%s\");}}}" $FSHARP_ARCHIVE_URL $FSHARP_ARCHIVE > download-fsharp.cs &&     mcs download-fsharp.cs && mono download-fsharp.exe && rm download-fsharp.exe download-fsharp.cs &&     tar xf $FSHARP_ARCHIVE &&     cd $FSHARP_BASENAME &&     make &&     make install &&     cd ~ &&     rm -rf /tmp/src /tmp/NuGetScratch ~/.nuget ~/.config ~/.local "$GNUPGHOME" &&     apt-get purge -y make gnupg dirmngr &&     apt-get clean
# Tue, 13 Oct 2020 06:57:15 GMT
WORKDIR /root
# Tue, 13 Oct 2020 06:57:15 GMT
CMD ["fsharpi"]
```

-	Layers:
	-	`sha256:bb79b6b2107fea8e8a47133a660b78e3a546998fcf0427be39ac9a0af4a97e90`  
		Last Modified: Tue, 13 Oct 2020 01:48:17 GMT  
		Size: 27.1 MB (27092228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:529ea17475edae1e854ee868ace575ed7a796bb85204b6ac6e5288984d1089f9`  
		Last Modified: Tue, 13 Oct 2020 07:13:15 GMT  
		Size: 159.5 MB (159529205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fsharp:10.7.0` - linux; arm64 variant v8

```console
$ docker pull fsharp@sha256:7f37d8f06cc2045142946c3af6c66c72dd2c34a04b4b6e65df0d202e71f2a6c1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.6 MB (183616406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:380ff0d99e05d272abe4d85af5295cddf539d1961abc1115a1b4c7fcb9391eeb`
-	Default Command: `["fsharpi"]`

```dockerfile
# Tue, 13 Oct 2020 01:41:09 GMT
ADD file:3488b1423094a75be5bb5956e9187827b8dd35d7a1f2b14081f8e74a1629e7d0 in / 
# Tue, 13 Oct 2020 01:41:11 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 02:08:20 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Steve Desmond <steve@stevedesmond.ca>
# Tue, 13 Oct 2020 02:08:21 GMT
ENV MONO_THREADS_PER_CPU=50
# Tue, 13 Oct 2020 02:27:00 GMT
RUN MONO_VERSION=6.8.0.105 &&     FSHARP_VERSION=10.2.3 &&     FSHARP_BASENAME=fsharp-$FSHARP_VERSION &&     FSHARP_ARCHIVE=$FSHARP_VERSION.tar.gz &&     FSHARP_ARCHIVE_URL=https://github.com/fsharp/fsharp/archive/$FSHARP_VERSION.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     apt-get update && apt-get --no-install-recommends install -y gnupg dirmngr ca-certificates apt-transport-https &&     apt-key adv --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF &&     echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" | tee /etc/apt/sources.list.d/mono-official-stable.list &&     apt-get update -y &&     apt-get --no-install-recommends install -y pkg-config make nuget mono-devel msbuild ca-certificates-mono locales &&     rm -rf /var/lib/apt/lists/* &&     echo 'en_US.UTF-8 UTF-8' > /etc/locale.gen && /usr/sbin/locale-gen &&     mkdir -p /tmp/src &&     cd /tmp/src &&     printf "namespace a { class b { public static void Main(string[] args) { new System.Net.WebClient().DownloadFile(\"%s\", \"%s\");}}}" $FSHARP_ARCHIVE_URL $FSHARP_ARCHIVE > download-fsharp.cs &&     mcs download-fsharp.cs && mono download-fsharp.exe && rm download-fsharp.exe download-fsharp.cs &&     tar xf $FSHARP_ARCHIVE &&     cd $FSHARP_BASENAME &&     make &&     make install &&     cd ~ &&     rm -rf /tmp/src /tmp/NuGetScratch ~/.nuget ~/.config ~/.local "$GNUPGHOME" &&     apt-get purge -y make gnupg dirmngr &&     apt-get clean
# Tue, 13 Oct 2020 02:27:08 GMT
WORKDIR /root
# Tue, 13 Oct 2020 02:27:10 GMT
CMD ["fsharpi"]
```

-	Layers:
	-	`sha256:4e6164a63b7b4cf981546947e191644c122214975d40b51ede0536791ebec3d4`  
		Last Modified: Tue, 13 Oct 2020 01:48:17 GMT  
		Size: 25.8 MB (25849329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29cc5bd99c5182580c6fc18aa496c999caed5c87f1d6bfc8d81725da288d90f7`  
		Last Modified: Tue, 13 Oct 2020 02:28:23 GMT  
		Size: 157.8 MB (157767077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `fsharp:10.7.0-netcore`

```console
$ docker pull fsharp@sha256:e18fd4b2916ffb6955f07a30ea3763afffcc5446263e0e908a058284b9c93b7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `fsharp:10.7.0-netcore` - linux; amd64

```console
$ docker pull fsharp@sha256:4f6b2681b2dbeb18b4581144fb75d29d566cbfbb1be4f3c58d58a1f336e0fdf3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.7 MB (323684249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db715b2b622748de2cfae107a3fe2c234c500fcfbbf5b7c4f62c6f132bb7a528`
-	Default Command: `["dotnet","fsi"]`

```dockerfile
# Tue, 13 Oct 2020 01:39:05 GMT
ADD file:0dc53e7886c35bc21ae6c4f6cedda54d56ae9c9e9cd367678f1a72e68b3c43d4 in / 
# Tue, 13 Oct 2020 01:39:05 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 06:44:51 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Steve Desmond <steve@stevedesmond.ca>
# Tue, 13 Oct 2020 06:44:51 GMT
ENV MONO_THREADS_PER_CPU=50
# Tue, 13 Oct 2020 06:57:14 GMT
RUN MONO_VERSION=6.8.0.105 &&     FSHARP_VERSION=10.2.3 &&     FSHARP_BASENAME=fsharp-$FSHARP_VERSION &&     FSHARP_ARCHIVE=$FSHARP_VERSION.tar.gz &&     FSHARP_ARCHIVE_URL=https://github.com/fsharp/fsharp/archive/$FSHARP_VERSION.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     apt-get update && apt-get --no-install-recommends install -y gnupg dirmngr ca-certificates apt-transport-https &&     apt-key adv --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF &&     echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" | tee /etc/apt/sources.list.d/mono-official-stable.list &&     apt-get update -y &&     apt-get --no-install-recommends install -y pkg-config make nuget mono-devel msbuild ca-certificates-mono locales &&     rm -rf /var/lib/apt/lists/* &&     echo 'en_US.UTF-8 UTF-8' > /etc/locale.gen && /usr/sbin/locale-gen &&     mkdir -p /tmp/src &&     cd /tmp/src &&     printf "namespace a { class b { public static void Main(string[] args) { new System.Net.WebClient().DownloadFile(\"%s\", \"%s\");}}}" $FSHARP_ARCHIVE_URL $FSHARP_ARCHIVE > download-fsharp.cs &&     mcs download-fsharp.cs && mono download-fsharp.exe && rm download-fsharp.exe download-fsharp.cs &&     tar xf $FSHARP_ARCHIVE &&     cd $FSHARP_BASENAME &&     make &&     make install &&     cd ~ &&     rm -rf /tmp/src /tmp/NuGetScratch ~/.nuget ~/.config ~/.local "$GNUPGHOME" &&     apt-get purge -y make gnupg dirmngr &&     apt-get clean
# Tue, 13 Oct 2020 06:57:15 GMT
WORKDIR /root
# Tue, 13 Oct 2020 06:57:15 GMT
CMD ["fsharpi"]
# Tue, 13 Oct 2020 07:11:46 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Steve Desmond <steve@stevedesmond.ca>
# Tue, 13 Oct 2020 07:11:46 GMT
ENV FrameworkPathOverride=/usr/lib/mono/4.7.2-api/
# Tue, 13 Oct 2020 07:11:46 GMT
ENV NUGET_XMLDOC_MODE=skip DOTNET_RUNNING_IN_CONTAINER=true DOTNET_USE_POLLING_FILE_WATCHER=true
# Tue, 13 Oct 2020 07:11:54 GMT
RUN apt-get update &&     apt-get --no-install-recommends install -y     curl     libunwind8     gettext     apt-transport-https     libc6     libcurl4     libgcc1     libgssapi-krb5-2     libicu63     liblttng-ust0     libssl1.1     libstdc++6     libunwind8     libuuid1     zlib1g &&     rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 07:12:14 GMT
RUN DOTNET_SDK_VERSION=3.1.102 &&     DOTNET_SDK_DOWNLOAD_URL=https://dotnetcli.blob.core.windows.net/dotnet/Sdk/$DOTNET_SDK_VERSION/dotnet-sdk-$DOTNET_SDK_VERSION-linux-x64.tar.gz &&     DOTNET_SDK_DOWNLOAD_SHA=9cacdc9700468a915e6fa51a3e5539b3519dd35b13e7f9d6c4dd0077e298baac0e50ad1880181df6781ef1dc64a232e9f78ad8e4494022987d12812c4ca15f29 &&     curl -SL $DOTNET_SDK_DOWNLOAD_URL --output dotnet.tar.gz &&     echo "$DOTNET_SDK_DOWNLOAD_SHA dotnet.tar.gz" | sha512sum -c - &&     mkdir -p /usr/share/dotnet &&     tar -zxf dotnet.tar.gz -C /usr/share/dotnet &&     rm dotnet.tar.gz &&     ln -s /usr/share/dotnet/dotnet /usr/bin/dotnet
# Tue, 13 Oct 2020 07:12:16 GMT
RUN mkdir warmup &&     cd warmup &&     dotnet new &&     cd - &&     rm -rf warmup /tmp/NuGetScratch
# Tue, 13 Oct 2020 07:12:17 GMT
WORKDIR /root
# Tue, 13 Oct 2020 07:12:17 GMT
CMD ["dotnet" "fsi"]
```

-	Layers:
	-	`sha256:bb79b6b2107fea8e8a47133a660b78e3a546998fcf0427be39ac9a0af4a97e90`  
		Last Modified: Tue, 13 Oct 2020 01:48:17 GMT  
		Size: 27.1 MB (27092228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:529ea17475edae1e854ee868ace575ed7a796bb85204b6ac6e5288984d1089f9`  
		Last Modified: Tue, 13 Oct 2020 07:13:15 GMT  
		Size: 159.5 MB (159529205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:082adf3fca7a62809930045eba1bd2c21b529ca4c2e0a3a1d44e91a18855949c`  
		Last Modified: Tue, 13 Oct 2020 07:14:00 GMT  
		Size: 17.2 MB (17202075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29d2716a33e8bd0d5f485078132a1134a27a94033049c471744eab5f4484779d`  
		Last Modified: Tue, 13 Oct 2020 07:14:17 GMT  
		Size: 115.9 MB (115919111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff6ef5cd95122ee55e9a647239c80c03992b0d62bd497b86113611630f1e6898`  
		Last Modified: Tue, 13 Oct 2020 07:13:57 GMT  
		Size: 3.9 MB (3941630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `fsharp:10.7-netcore`

```console
$ docker pull fsharp@sha256:e18fd4b2916ffb6955f07a30ea3763afffcc5446263e0e908a058284b9c93b7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `fsharp:10.7-netcore` - linux; amd64

```console
$ docker pull fsharp@sha256:4f6b2681b2dbeb18b4581144fb75d29d566cbfbb1be4f3c58d58a1f336e0fdf3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.7 MB (323684249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db715b2b622748de2cfae107a3fe2c234c500fcfbbf5b7c4f62c6f132bb7a528`
-	Default Command: `["dotnet","fsi"]`

```dockerfile
# Tue, 13 Oct 2020 01:39:05 GMT
ADD file:0dc53e7886c35bc21ae6c4f6cedda54d56ae9c9e9cd367678f1a72e68b3c43d4 in / 
# Tue, 13 Oct 2020 01:39:05 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 06:44:51 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Steve Desmond <steve@stevedesmond.ca>
# Tue, 13 Oct 2020 06:44:51 GMT
ENV MONO_THREADS_PER_CPU=50
# Tue, 13 Oct 2020 06:57:14 GMT
RUN MONO_VERSION=6.8.0.105 &&     FSHARP_VERSION=10.2.3 &&     FSHARP_BASENAME=fsharp-$FSHARP_VERSION &&     FSHARP_ARCHIVE=$FSHARP_VERSION.tar.gz &&     FSHARP_ARCHIVE_URL=https://github.com/fsharp/fsharp/archive/$FSHARP_VERSION.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     apt-get update && apt-get --no-install-recommends install -y gnupg dirmngr ca-certificates apt-transport-https &&     apt-key adv --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF &&     echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" | tee /etc/apt/sources.list.d/mono-official-stable.list &&     apt-get update -y &&     apt-get --no-install-recommends install -y pkg-config make nuget mono-devel msbuild ca-certificates-mono locales &&     rm -rf /var/lib/apt/lists/* &&     echo 'en_US.UTF-8 UTF-8' > /etc/locale.gen && /usr/sbin/locale-gen &&     mkdir -p /tmp/src &&     cd /tmp/src &&     printf "namespace a { class b { public static void Main(string[] args) { new System.Net.WebClient().DownloadFile(\"%s\", \"%s\");}}}" $FSHARP_ARCHIVE_URL $FSHARP_ARCHIVE > download-fsharp.cs &&     mcs download-fsharp.cs && mono download-fsharp.exe && rm download-fsharp.exe download-fsharp.cs &&     tar xf $FSHARP_ARCHIVE &&     cd $FSHARP_BASENAME &&     make &&     make install &&     cd ~ &&     rm -rf /tmp/src /tmp/NuGetScratch ~/.nuget ~/.config ~/.local "$GNUPGHOME" &&     apt-get purge -y make gnupg dirmngr &&     apt-get clean
# Tue, 13 Oct 2020 06:57:15 GMT
WORKDIR /root
# Tue, 13 Oct 2020 06:57:15 GMT
CMD ["fsharpi"]
# Tue, 13 Oct 2020 07:11:46 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Steve Desmond <steve@stevedesmond.ca>
# Tue, 13 Oct 2020 07:11:46 GMT
ENV FrameworkPathOverride=/usr/lib/mono/4.7.2-api/
# Tue, 13 Oct 2020 07:11:46 GMT
ENV NUGET_XMLDOC_MODE=skip DOTNET_RUNNING_IN_CONTAINER=true DOTNET_USE_POLLING_FILE_WATCHER=true
# Tue, 13 Oct 2020 07:11:54 GMT
RUN apt-get update &&     apt-get --no-install-recommends install -y     curl     libunwind8     gettext     apt-transport-https     libc6     libcurl4     libgcc1     libgssapi-krb5-2     libicu63     liblttng-ust0     libssl1.1     libstdc++6     libunwind8     libuuid1     zlib1g &&     rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 07:12:14 GMT
RUN DOTNET_SDK_VERSION=3.1.102 &&     DOTNET_SDK_DOWNLOAD_URL=https://dotnetcli.blob.core.windows.net/dotnet/Sdk/$DOTNET_SDK_VERSION/dotnet-sdk-$DOTNET_SDK_VERSION-linux-x64.tar.gz &&     DOTNET_SDK_DOWNLOAD_SHA=9cacdc9700468a915e6fa51a3e5539b3519dd35b13e7f9d6c4dd0077e298baac0e50ad1880181df6781ef1dc64a232e9f78ad8e4494022987d12812c4ca15f29 &&     curl -SL $DOTNET_SDK_DOWNLOAD_URL --output dotnet.tar.gz &&     echo "$DOTNET_SDK_DOWNLOAD_SHA dotnet.tar.gz" | sha512sum -c - &&     mkdir -p /usr/share/dotnet &&     tar -zxf dotnet.tar.gz -C /usr/share/dotnet &&     rm dotnet.tar.gz &&     ln -s /usr/share/dotnet/dotnet /usr/bin/dotnet
# Tue, 13 Oct 2020 07:12:16 GMT
RUN mkdir warmup &&     cd warmup &&     dotnet new &&     cd - &&     rm -rf warmup /tmp/NuGetScratch
# Tue, 13 Oct 2020 07:12:17 GMT
WORKDIR /root
# Tue, 13 Oct 2020 07:12:17 GMT
CMD ["dotnet" "fsi"]
```

-	Layers:
	-	`sha256:bb79b6b2107fea8e8a47133a660b78e3a546998fcf0427be39ac9a0af4a97e90`  
		Last Modified: Tue, 13 Oct 2020 01:48:17 GMT  
		Size: 27.1 MB (27092228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:529ea17475edae1e854ee868ace575ed7a796bb85204b6ac6e5288984d1089f9`  
		Last Modified: Tue, 13 Oct 2020 07:13:15 GMT  
		Size: 159.5 MB (159529205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:082adf3fca7a62809930045eba1bd2c21b529ca4c2e0a3a1d44e91a18855949c`  
		Last Modified: Tue, 13 Oct 2020 07:14:00 GMT  
		Size: 17.2 MB (17202075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29d2716a33e8bd0d5f485078132a1134a27a94033049c471744eab5f4484779d`  
		Last Modified: Tue, 13 Oct 2020 07:14:17 GMT  
		Size: 115.9 MB (115919111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff6ef5cd95122ee55e9a647239c80c03992b0d62bd497b86113611630f1e6898`  
		Last Modified: Tue, 13 Oct 2020 07:13:57 GMT  
		Size: 3.9 MB (3941630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `fsharp:10-netcore`

```console
$ docker pull fsharp@sha256:e18fd4b2916ffb6955f07a30ea3763afffcc5446263e0e908a058284b9c93b7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `fsharp:10-netcore` - linux; amd64

```console
$ docker pull fsharp@sha256:4f6b2681b2dbeb18b4581144fb75d29d566cbfbb1be4f3c58d58a1f336e0fdf3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.7 MB (323684249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db715b2b622748de2cfae107a3fe2c234c500fcfbbf5b7c4f62c6f132bb7a528`
-	Default Command: `["dotnet","fsi"]`

```dockerfile
# Tue, 13 Oct 2020 01:39:05 GMT
ADD file:0dc53e7886c35bc21ae6c4f6cedda54d56ae9c9e9cd367678f1a72e68b3c43d4 in / 
# Tue, 13 Oct 2020 01:39:05 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 06:44:51 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Steve Desmond <steve@stevedesmond.ca>
# Tue, 13 Oct 2020 06:44:51 GMT
ENV MONO_THREADS_PER_CPU=50
# Tue, 13 Oct 2020 06:57:14 GMT
RUN MONO_VERSION=6.8.0.105 &&     FSHARP_VERSION=10.2.3 &&     FSHARP_BASENAME=fsharp-$FSHARP_VERSION &&     FSHARP_ARCHIVE=$FSHARP_VERSION.tar.gz &&     FSHARP_ARCHIVE_URL=https://github.com/fsharp/fsharp/archive/$FSHARP_VERSION.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     apt-get update && apt-get --no-install-recommends install -y gnupg dirmngr ca-certificates apt-transport-https &&     apt-key adv --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF &&     echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" | tee /etc/apt/sources.list.d/mono-official-stable.list &&     apt-get update -y &&     apt-get --no-install-recommends install -y pkg-config make nuget mono-devel msbuild ca-certificates-mono locales &&     rm -rf /var/lib/apt/lists/* &&     echo 'en_US.UTF-8 UTF-8' > /etc/locale.gen && /usr/sbin/locale-gen &&     mkdir -p /tmp/src &&     cd /tmp/src &&     printf "namespace a { class b { public static void Main(string[] args) { new System.Net.WebClient().DownloadFile(\"%s\", \"%s\");}}}" $FSHARP_ARCHIVE_URL $FSHARP_ARCHIVE > download-fsharp.cs &&     mcs download-fsharp.cs && mono download-fsharp.exe && rm download-fsharp.exe download-fsharp.cs &&     tar xf $FSHARP_ARCHIVE &&     cd $FSHARP_BASENAME &&     make &&     make install &&     cd ~ &&     rm -rf /tmp/src /tmp/NuGetScratch ~/.nuget ~/.config ~/.local "$GNUPGHOME" &&     apt-get purge -y make gnupg dirmngr &&     apt-get clean
# Tue, 13 Oct 2020 06:57:15 GMT
WORKDIR /root
# Tue, 13 Oct 2020 06:57:15 GMT
CMD ["fsharpi"]
# Tue, 13 Oct 2020 07:11:46 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Steve Desmond <steve@stevedesmond.ca>
# Tue, 13 Oct 2020 07:11:46 GMT
ENV FrameworkPathOverride=/usr/lib/mono/4.7.2-api/
# Tue, 13 Oct 2020 07:11:46 GMT
ENV NUGET_XMLDOC_MODE=skip DOTNET_RUNNING_IN_CONTAINER=true DOTNET_USE_POLLING_FILE_WATCHER=true
# Tue, 13 Oct 2020 07:11:54 GMT
RUN apt-get update &&     apt-get --no-install-recommends install -y     curl     libunwind8     gettext     apt-transport-https     libc6     libcurl4     libgcc1     libgssapi-krb5-2     libicu63     liblttng-ust0     libssl1.1     libstdc++6     libunwind8     libuuid1     zlib1g &&     rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 07:12:14 GMT
RUN DOTNET_SDK_VERSION=3.1.102 &&     DOTNET_SDK_DOWNLOAD_URL=https://dotnetcli.blob.core.windows.net/dotnet/Sdk/$DOTNET_SDK_VERSION/dotnet-sdk-$DOTNET_SDK_VERSION-linux-x64.tar.gz &&     DOTNET_SDK_DOWNLOAD_SHA=9cacdc9700468a915e6fa51a3e5539b3519dd35b13e7f9d6c4dd0077e298baac0e50ad1880181df6781ef1dc64a232e9f78ad8e4494022987d12812c4ca15f29 &&     curl -SL $DOTNET_SDK_DOWNLOAD_URL --output dotnet.tar.gz &&     echo "$DOTNET_SDK_DOWNLOAD_SHA dotnet.tar.gz" | sha512sum -c - &&     mkdir -p /usr/share/dotnet &&     tar -zxf dotnet.tar.gz -C /usr/share/dotnet &&     rm dotnet.tar.gz &&     ln -s /usr/share/dotnet/dotnet /usr/bin/dotnet
# Tue, 13 Oct 2020 07:12:16 GMT
RUN mkdir warmup &&     cd warmup &&     dotnet new &&     cd - &&     rm -rf warmup /tmp/NuGetScratch
# Tue, 13 Oct 2020 07:12:17 GMT
WORKDIR /root
# Tue, 13 Oct 2020 07:12:17 GMT
CMD ["dotnet" "fsi"]
```

-	Layers:
	-	`sha256:bb79b6b2107fea8e8a47133a660b78e3a546998fcf0427be39ac9a0af4a97e90`  
		Last Modified: Tue, 13 Oct 2020 01:48:17 GMT  
		Size: 27.1 MB (27092228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:529ea17475edae1e854ee868ace575ed7a796bb85204b6ac6e5288984d1089f9`  
		Last Modified: Tue, 13 Oct 2020 07:13:15 GMT  
		Size: 159.5 MB (159529205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:082adf3fca7a62809930045eba1bd2c21b529ca4c2e0a3a1d44e91a18855949c`  
		Last Modified: Tue, 13 Oct 2020 07:14:00 GMT  
		Size: 17.2 MB (17202075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29d2716a33e8bd0d5f485078132a1134a27a94033049c471744eab5f4484779d`  
		Last Modified: Tue, 13 Oct 2020 07:14:17 GMT  
		Size: 115.9 MB (115919111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff6ef5cd95122ee55e9a647239c80c03992b0d62bd497b86113611630f1e6898`  
		Last Modified: Tue, 13 Oct 2020 07:13:57 GMT  
		Size: 3.9 MB (3941630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `fsharp:4`

```console
$ docker pull fsharp@sha256:0250a8027924fa928a5f847da3571d33f0adf31382cba4d5eefe3f71517f10cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `fsharp:4` - linux; amd64

```console
$ docker pull fsharp@sha256:d8520811535d71492d4f016e8f79dc3d33fd565c0e860168e3338b2a0b508bb4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.3 MB (176300744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74092d750103f5df89666aae0cc70dcc2e81f305a3d6777c1dbfdc3e328463c4`
-	Default Command: `["fsharpi"]`

```dockerfile
# Tue, 13 Oct 2020 01:40:00 GMT
ADD file:ce4857398d963428cc93cbf7215159279fc5be5f51713a4637fb734be1c438b4 in / 
# Tue, 13 Oct 2020 01:40:01 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 06:57:32 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Steve Desmond <steve@stevedesmond.ca>
# Tue, 13 Oct 2020 06:57:32 GMT
ENV MONO_THREADS_PER_CPU=50
# Tue, 13 Oct 2020 07:11:28 GMT
RUN MONO_VERSION=5.8.0.108 &&     FSHARP_VERSION=4.1.34 &&     FSHARP_PREFIX=/usr &&     FSHARP_GACDIR=/usr/lib/mono/gac &&     FSHARP_BASENAME=fsharp-$FSHARP_VERSION &&     FSHARP_ARCHIVE=$FSHARP_VERSION.tar.gz &&     FSHARP_ARCHIVE_URL=https://github.com/fsharp/fsharp/archive/$FSHARP_VERSION.tar.gz &&     apt-key adv --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF &&     echo "deb http://download.mono-project.com/repo/debian jessie/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official.list &&     apt-get update -y &&     apt-get --no-install-recommends install -y autoconf libtool pkg-config make automake nuget mono-devel msbuild ca-certificates-mono &&     rm -rf /var/lib/apt/lists/* &&     mkdir -p /tmp/src &&     cd /tmp/src &&     printf "namespace a { class b { public static void Main(string[] args) { new System.Net.WebClient().DownloadFile(\"%s\", \"%s\");}}}" $FSHARP_ARCHIVE_URL $FSHARP_ARCHIVE > download-fsharp.cs &&     mcs download-fsharp.cs && mono download-fsharp.exe && rm download-fsharp.exe download-fsharp.cs &&     tar xf $FSHARP_ARCHIVE &&     cd $FSHARP_BASENAME &&     ./autogen.sh --prefix=$FSHARP_PREFIX --with-gacdir=$FSHARP_GACDIR &&     make &&     make install &&     cd ~ &&     rm -rf /tmp/src /tmp/NuGetScratch ~/.nuget ~/.config ~/.local &&     apt-get purge -y autoconf libtool make automake &&     apt-get clean
# Tue, 13 Oct 2020 07:11:28 GMT
WORKDIR /root
# Tue, 13 Oct 2020 07:11:28 GMT
CMD ["fsharpi"]
```

-	Layers:
	-	`sha256:4429b8d1a27b563a13bea19a39dc9cda477b77bb94dcf95236b80bfaeaddd4b9`  
		Last Modified: Tue, 13 Oct 2020 01:48:48 GMT  
		Size: 30.2 MB (30159756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e40c1c27d97bc188fda2ba53aadc994e43eddd47fa9bf73f0f1a8f689d23437a`  
		Last Modified: Tue, 13 Oct 2020 07:13:52 GMT  
		Size: 146.1 MB (146140988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `fsharp:4.1`

```console
$ docker pull fsharp@sha256:0250a8027924fa928a5f847da3571d33f0adf31382cba4d5eefe3f71517f10cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `fsharp:4.1` - linux; amd64

```console
$ docker pull fsharp@sha256:d8520811535d71492d4f016e8f79dc3d33fd565c0e860168e3338b2a0b508bb4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.3 MB (176300744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74092d750103f5df89666aae0cc70dcc2e81f305a3d6777c1dbfdc3e328463c4`
-	Default Command: `["fsharpi"]`

```dockerfile
# Tue, 13 Oct 2020 01:40:00 GMT
ADD file:ce4857398d963428cc93cbf7215159279fc5be5f51713a4637fb734be1c438b4 in / 
# Tue, 13 Oct 2020 01:40:01 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 06:57:32 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Steve Desmond <steve@stevedesmond.ca>
# Tue, 13 Oct 2020 06:57:32 GMT
ENV MONO_THREADS_PER_CPU=50
# Tue, 13 Oct 2020 07:11:28 GMT
RUN MONO_VERSION=5.8.0.108 &&     FSHARP_VERSION=4.1.34 &&     FSHARP_PREFIX=/usr &&     FSHARP_GACDIR=/usr/lib/mono/gac &&     FSHARP_BASENAME=fsharp-$FSHARP_VERSION &&     FSHARP_ARCHIVE=$FSHARP_VERSION.tar.gz &&     FSHARP_ARCHIVE_URL=https://github.com/fsharp/fsharp/archive/$FSHARP_VERSION.tar.gz &&     apt-key adv --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF &&     echo "deb http://download.mono-project.com/repo/debian jessie/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official.list &&     apt-get update -y &&     apt-get --no-install-recommends install -y autoconf libtool pkg-config make automake nuget mono-devel msbuild ca-certificates-mono &&     rm -rf /var/lib/apt/lists/* &&     mkdir -p /tmp/src &&     cd /tmp/src &&     printf "namespace a { class b { public static void Main(string[] args) { new System.Net.WebClient().DownloadFile(\"%s\", \"%s\");}}}" $FSHARP_ARCHIVE_URL $FSHARP_ARCHIVE > download-fsharp.cs &&     mcs download-fsharp.cs && mono download-fsharp.exe && rm download-fsharp.exe download-fsharp.cs &&     tar xf $FSHARP_ARCHIVE &&     cd $FSHARP_BASENAME &&     ./autogen.sh --prefix=$FSHARP_PREFIX --with-gacdir=$FSHARP_GACDIR &&     make &&     make install &&     cd ~ &&     rm -rf /tmp/src /tmp/NuGetScratch ~/.nuget ~/.config ~/.local &&     apt-get purge -y autoconf libtool make automake &&     apt-get clean
# Tue, 13 Oct 2020 07:11:28 GMT
WORKDIR /root
# Tue, 13 Oct 2020 07:11:28 GMT
CMD ["fsharpi"]
```

-	Layers:
	-	`sha256:4429b8d1a27b563a13bea19a39dc9cda477b77bb94dcf95236b80bfaeaddd4b9`  
		Last Modified: Tue, 13 Oct 2020 01:48:48 GMT  
		Size: 30.2 MB (30159756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e40c1c27d97bc188fda2ba53aadc994e43eddd47fa9bf73f0f1a8f689d23437a`  
		Last Modified: Tue, 13 Oct 2020 07:13:52 GMT  
		Size: 146.1 MB (146140988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `fsharp:4.1.34`

```console
$ docker pull fsharp@sha256:0250a8027924fa928a5f847da3571d33f0adf31382cba4d5eefe3f71517f10cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `fsharp:4.1.34` - linux; amd64

```console
$ docker pull fsharp@sha256:d8520811535d71492d4f016e8f79dc3d33fd565c0e860168e3338b2a0b508bb4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.3 MB (176300744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74092d750103f5df89666aae0cc70dcc2e81f305a3d6777c1dbfdc3e328463c4`
-	Default Command: `["fsharpi"]`

```dockerfile
# Tue, 13 Oct 2020 01:40:00 GMT
ADD file:ce4857398d963428cc93cbf7215159279fc5be5f51713a4637fb734be1c438b4 in / 
# Tue, 13 Oct 2020 01:40:01 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 06:57:32 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Steve Desmond <steve@stevedesmond.ca>
# Tue, 13 Oct 2020 06:57:32 GMT
ENV MONO_THREADS_PER_CPU=50
# Tue, 13 Oct 2020 07:11:28 GMT
RUN MONO_VERSION=5.8.0.108 &&     FSHARP_VERSION=4.1.34 &&     FSHARP_PREFIX=/usr &&     FSHARP_GACDIR=/usr/lib/mono/gac &&     FSHARP_BASENAME=fsharp-$FSHARP_VERSION &&     FSHARP_ARCHIVE=$FSHARP_VERSION.tar.gz &&     FSHARP_ARCHIVE_URL=https://github.com/fsharp/fsharp/archive/$FSHARP_VERSION.tar.gz &&     apt-key adv --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF &&     echo "deb http://download.mono-project.com/repo/debian jessie/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official.list &&     apt-get update -y &&     apt-get --no-install-recommends install -y autoconf libtool pkg-config make automake nuget mono-devel msbuild ca-certificates-mono &&     rm -rf /var/lib/apt/lists/* &&     mkdir -p /tmp/src &&     cd /tmp/src &&     printf "namespace a { class b { public static void Main(string[] args) { new System.Net.WebClient().DownloadFile(\"%s\", \"%s\");}}}" $FSHARP_ARCHIVE_URL $FSHARP_ARCHIVE > download-fsharp.cs &&     mcs download-fsharp.cs && mono download-fsharp.exe && rm download-fsharp.exe download-fsharp.cs &&     tar xf $FSHARP_ARCHIVE &&     cd $FSHARP_BASENAME &&     ./autogen.sh --prefix=$FSHARP_PREFIX --with-gacdir=$FSHARP_GACDIR &&     make &&     make install &&     cd ~ &&     rm -rf /tmp/src /tmp/NuGetScratch ~/.nuget ~/.config ~/.local &&     apt-get purge -y autoconf libtool make automake &&     apt-get clean
# Tue, 13 Oct 2020 07:11:28 GMT
WORKDIR /root
# Tue, 13 Oct 2020 07:11:28 GMT
CMD ["fsharpi"]
```

-	Layers:
	-	`sha256:4429b8d1a27b563a13bea19a39dc9cda477b77bb94dcf95236b80bfaeaddd4b9`  
		Last Modified: Tue, 13 Oct 2020 01:48:48 GMT  
		Size: 30.2 MB (30159756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e40c1c27d97bc188fda2ba53aadc994e43eddd47fa9bf73f0f1a8f689d23437a`  
		Last Modified: Tue, 13 Oct 2020 07:13:52 GMT  
		Size: 146.1 MB (146140988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `fsharp:latest`

```console
$ docker pull fsharp@sha256:2e1a5e8854e63fd437f4fb312cd3bc074ddd6a0c1c5e482f6eb3f5eb6a04fb33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `fsharp:latest` - linux; amd64

```console
$ docker pull fsharp@sha256:1be0abf91a4e1a37906acfa0391cd3c413f91100a8d60a167cc47df8dd7857cf
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.6 MB (186621433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a19ba504662e2d2240a9eee95446b3dd474a3137a8d6f102cc2e4f6519dbb82b`
-	Default Command: `["fsharpi"]`

```dockerfile
# Tue, 13 Oct 2020 01:39:05 GMT
ADD file:0dc53e7886c35bc21ae6c4f6cedda54d56ae9c9e9cd367678f1a72e68b3c43d4 in / 
# Tue, 13 Oct 2020 01:39:05 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 06:44:51 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Steve Desmond <steve@stevedesmond.ca>
# Tue, 13 Oct 2020 06:44:51 GMT
ENV MONO_THREADS_PER_CPU=50
# Tue, 13 Oct 2020 06:57:14 GMT
RUN MONO_VERSION=6.8.0.105 &&     FSHARP_VERSION=10.2.3 &&     FSHARP_BASENAME=fsharp-$FSHARP_VERSION &&     FSHARP_ARCHIVE=$FSHARP_VERSION.tar.gz &&     FSHARP_ARCHIVE_URL=https://github.com/fsharp/fsharp/archive/$FSHARP_VERSION.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     apt-get update && apt-get --no-install-recommends install -y gnupg dirmngr ca-certificates apt-transport-https &&     apt-key adv --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF &&     echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" | tee /etc/apt/sources.list.d/mono-official-stable.list &&     apt-get update -y &&     apt-get --no-install-recommends install -y pkg-config make nuget mono-devel msbuild ca-certificates-mono locales &&     rm -rf /var/lib/apt/lists/* &&     echo 'en_US.UTF-8 UTF-8' > /etc/locale.gen && /usr/sbin/locale-gen &&     mkdir -p /tmp/src &&     cd /tmp/src &&     printf "namespace a { class b { public static void Main(string[] args) { new System.Net.WebClient().DownloadFile(\"%s\", \"%s\");}}}" $FSHARP_ARCHIVE_URL $FSHARP_ARCHIVE > download-fsharp.cs &&     mcs download-fsharp.cs && mono download-fsharp.exe && rm download-fsharp.exe download-fsharp.cs &&     tar xf $FSHARP_ARCHIVE &&     cd $FSHARP_BASENAME &&     make &&     make install &&     cd ~ &&     rm -rf /tmp/src /tmp/NuGetScratch ~/.nuget ~/.config ~/.local "$GNUPGHOME" &&     apt-get purge -y make gnupg dirmngr &&     apt-get clean
# Tue, 13 Oct 2020 06:57:15 GMT
WORKDIR /root
# Tue, 13 Oct 2020 06:57:15 GMT
CMD ["fsharpi"]
```

-	Layers:
	-	`sha256:bb79b6b2107fea8e8a47133a660b78e3a546998fcf0427be39ac9a0af4a97e90`  
		Last Modified: Tue, 13 Oct 2020 01:48:17 GMT  
		Size: 27.1 MB (27092228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:529ea17475edae1e854ee868ace575ed7a796bb85204b6ac6e5288984d1089f9`  
		Last Modified: Tue, 13 Oct 2020 07:13:15 GMT  
		Size: 159.5 MB (159529205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fsharp:latest` - linux; arm64 variant v8

```console
$ docker pull fsharp@sha256:7f37d8f06cc2045142946c3af6c66c72dd2c34a04b4b6e65df0d202e71f2a6c1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.6 MB (183616406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:380ff0d99e05d272abe4d85af5295cddf539d1961abc1115a1b4c7fcb9391eeb`
-	Default Command: `["fsharpi"]`

```dockerfile
# Tue, 13 Oct 2020 01:41:09 GMT
ADD file:3488b1423094a75be5bb5956e9187827b8dd35d7a1f2b14081f8e74a1629e7d0 in / 
# Tue, 13 Oct 2020 01:41:11 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 02:08:20 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Steve Desmond <steve@stevedesmond.ca>
# Tue, 13 Oct 2020 02:08:21 GMT
ENV MONO_THREADS_PER_CPU=50
# Tue, 13 Oct 2020 02:27:00 GMT
RUN MONO_VERSION=6.8.0.105 &&     FSHARP_VERSION=10.2.3 &&     FSHARP_BASENAME=fsharp-$FSHARP_VERSION &&     FSHARP_ARCHIVE=$FSHARP_VERSION.tar.gz &&     FSHARP_ARCHIVE_URL=https://github.com/fsharp/fsharp/archive/$FSHARP_VERSION.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     apt-get update && apt-get --no-install-recommends install -y gnupg dirmngr ca-certificates apt-transport-https &&     apt-key adv --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF &&     echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" | tee /etc/apt/sources.list.d/mono-official-stable.list &&     apt-get update -y &&     apt-get --no-install-recommends install -y pkg-config make nuget mono-devel msbuild ca-certificates-mono locales &&     rm -rf /var/lib/apt/lists/* &&     echo 'en_US.UTF-8 UTF-8' > /etc/locale.gen && /usr/sbin/locale-gen &&     mkdir -p /tmp/src &&     cd /tmp/src &&     printf "namespace a { class b { public static void Main(string[] args) { new System.Net.WebClient().DownloadFile(\"%s\", \"%s\");}}}" $FSHARP_ARCHIVE_URL $FSHARP_ARCHIVE > download-fsharp.cs &&     mcs download-fsharp.cs && mono download-fsharp.exe && rm download-fsharp.exe download-fsharp.cs &&     tar xf $FSHARP_ARCHIVE &&     cd $FSHARP_BASENAME &&     make &&     make install &&     cd ~ &&     rm -rf /tmp/src /tmp/NuGetScratch ~/.nuget ~/.config ~/.local "$GNUPGHOME" &&     apt-get purge -y make gnupg dirmngr &&     apt-get clean
# Tue, 13 Oct 2020 02:27:08 GMT
WORKDIR /root
# Tue, 13 Oct 2020 02:27:10 GMT
CMD ["fsharpi"]
```

-	Layers:
	-	`sha256:4e6164a63b7b4cf981546947e191644c122214975d40b51ede0536791ebec3d4`  
		Last Modified: Tue, 13 Oct 2020 01:48:17 GMT  
		Size: 25.8 MB (25849329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29cc5bd99c5182580c6fc18aa496c999caed5c87f1d6bfc8d81725da288d90f7`  
		Last Modified: Tue, 13 Oct 2020 02:28:23 GMT  
		Size: 157.8 MB (157767077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `fsharp:netcore`

```console
$ docker pull fsharp@sha256:e18fd4b2916ffb6955f07a30ea3763afffcc5446263e0e908a058284b9c93b7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `fsharp:netcore` - linux; amd64

```console
$ docker pull fsharp@sha256:4f6b2681b2dbeb18b4581144fb75d29d566cbfbb1be4f3c58d58a1f336e0fdf3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.7 MB (323684249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db715b2b622748de2cfae107a3fe2c234c500fcfbbf5b7c4f62c6f132bb7a528`
-	Default Command: `["dotnet","fsi"]`

```dockerfile
# Tue, 13 Oct 2020 01:39:05 GMT
ADD file:0dc53e7886c35bc21ae6c4f6cedda54d56ae9c9e9cd367678f1a72e68b3c43d4 in / 
# Tue, 13 Oct 2020 01:39:05 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 06:44:51 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Steve Desmond <steve@stevedesmond.ca>
# Tue, 13 Oct 2020 06:44:51 GMT
ENV MONO_THREADS_PER_CPU=50
# Tue, 13 Oct 2020 06:57:14 GMT
RUN MONO_VERSION=6.8.0.105 &&     FSHARP_VERSION=10.2.3 &&     FSHARP_BASENAME=fsharp-$FSHARP_VERSION &&     FSHARP_ARCHIVE=$FSHARP_VERSION.tar.gz &&     FSHARP_ARCHIVE_URL=https://github.com/fsharp/fsharp/archive/$FSHARP_VERSION.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     apt-get update && apt-get --no-install-recommends install -y gnupg dirmngr ca-certificates apt-transport-https &&     apt-key adv --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF &&     echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" | tee /etc/apt/sources.list.d/mono-official-stable.list &&     apt-get update -y &&     apt-get --no-install-recommends install -y pkg-config make nuget mono-devel msbuild ca-certificates-mono locales &&     rm -rf /var/lib/apt/lists/* &&     echo 'en_US.UTF-8 UTF-8' > /etc/locale.gen && /usr/sbin/locale-gen &&     mkdir -p /tmp/src &&     cd /tmp/src &&     printf "namespace a { class b { public static void Main(string[] args) { new System.Net.WebClient().DownloadFile(\"%s\", \"%s\");}}}" $FSHARP_ARCHIVE_URL $FSHARP_ARCHIVE > download-fsharp.cs &&     mcs download-fsharp.cs && mono download-fsharp.exe && rm download-fsharp.exe download-fsharp.cs &&     tar xf $FSHARP_ARCHIVE &&     cd $FSHARP_BASENAME &&     make &&     make install &&     cd ~ &&     rm -rf /tmp/src /tmp/NuGetScratch ~/.nuget ~/.config ~/.local "$GNUPGHOME" &&     apt-get purge -y make gnupg dirmngr &&     apt-get clean
# Tue, 13 Oct 2020 06:57:15 GMT
WORKDIR /root
# Tue, 13 Oct 2020 06:57:15 GMT
CMD ["fsharpi"]
# Tue, 13 Oct 2020 07:11:46 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Steve Desmond <steve@stevedesmond.ca>
# Tue, 13 Oct 2020 07:11:46 GMT
ENV FrameworkPathOverride=/usr/lib/mono/4.7.2-api/
# Tue, 13 Oct 2020 07:11:46 GMT
ENV NUGET_XMLDOC_MODE=skip DOTNET_RUNNING_IN_CONTAINER=true DOTNET_USE_POLLING_FILE_WATCHER=true
# Tue, 13 Oct 2020 07:11:54 GMT
RUN apt-get update &&     apt-get --no-install-recommends install -y     curl     libunwind8     gettext     apt-transport-https     libc6     libcurl4     libgcc1     libgssapi-krb5-2     libicu63     liblttng-ust0     libssl1.1     libstdc++6     libunwind8     libuuid1     zlib1g &&     rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 07:12:14 GMT
RUN DOTNET_SDK_VERSION=3.1.102 &&     DOTNET_SDK_DOWNLOAD_URL=https://dotnetcli.blob.core.windows.net/dotnet/Sdk/$DOTNET_SDK_VERSION/dotnet-sdk-$DOTNET_SDK_VERSION-linux-x64.tar.gz &&     DOTNET_SDK_DOWNLOAD_SHA=9cacdc9700468a915e6fa51a3e5539b3519dd35b13e7f9d6c4dd0077e298baac0e50ad1880181df6781ef1dc64a232e9f78ad8e4494022987d12812c4ca15f29 &&     curl -SL $DOTNET_SDK_DOWNLOAD_URL --output dotnet.tar.gz &&     echo "$DOTNET_SDK_DOWNLOAD_SHA dotnet.tar.gz" | sha512sum -c - &&     mkdir -p /usr/share/dotnet &&     tar -zxf dotnet.tar.gz -C /usr/share/dotnet &&     rm dotnet.tar.gz &&     ln -s /usr/share/dotnet/dotnet /usr/bin/dotnet
# Tue, 13 Oct 2020 07:12:16 GMT
RUN mkdir warmup &&     cd warmup &&     dotnet new &&     cd - &&     rm -rf warmup /tmp/NuGetScratch
# Tue, 13 Oct 2020 07:12:17 GMT
WORKDIR /root
# Tue, 13 Oct 2020 07:12:17 GMT
CMD ["dotnet" "fsi"]
```

-	Layers:
	-	`sha256:bb79b6b2107fea8e8a47133a660b78e3a546998fcf0427be39ac9a0af4a97e90`  
		Last Modified: Tue, 13 Oct 2020 01:48:17 GMT  
		Size: 27.1 MB (27092228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:529ea17475edae1e854ee868ace575ed7a796bb85204b6ac6e5288984d1089f9`  
		Last Modified: Tue, 13 Oct 2020 07:13:15 GMT  
		Size: 159.5 MB (159529205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:082adf3fca7a62809930045eba1bd2c21b529ca4c2e0a3a1d44e91a18855949c`  
		Last Modified: Tue, 13 Oct 2020 07:14:00 GMT  
		Size: 17.2 MB (17202075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29d2716a33e8bd0d5f485078132a1134a27a94033049c471744eab5f4484779d`  
		Last Modified: Tue, 13 Oct 2020 07:14:17 GMT  
		Size: 115.9 MB (115919111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff6ef5cd95122ee55e9a647239c80c03992b0d62bd497b86113611630f1e6898`  
		Last Modified: Tue, 13 Oct 2020 07:13:57 GMT  
		Size: 3.9 MB (3941630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
