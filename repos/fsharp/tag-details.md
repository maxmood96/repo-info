<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `fsharp`

-	[`fsharp:10`](#fsharp10)
-	[`fsharp:10.10`](#fsharp1010)
-	[`fsharp:10.10.0`](#fsharp10100)
-	[`fsharp:10.10.0-netcore`](#fsharp10100-netcore)
-	[`fsharp:10.10-netcore`](#fsharp1010-netcore)
-	[`fsharp:10-netcore`](#fsharp10-netcore)
-	[`fsharp:4`](#fsharp4)
-	[`fsharp:4.1`](#fsharp41)
-	[`fsharp:4.1.34`](#fsharp4134)
-	[`fsharp:latest`](#fsharplatest)
-	[`fsharp:netcore`](#fsharpnetcore)

## `fsharp:10`

```console
$ docker pull fsharp@sha256:4cc2ce49d433271ad3ec56129386dced09643d7c7f035461212c0e1a03772818
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `fsharp:10` - linux; amd64

```console
$ docker pull fsharp@sha256:aade83420e7ffa1d331e0b7d6ea8a79d6669b3e40406a2ee69762cc95adc9a47
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.6 MB (187596612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:565b414f7f0e6e90b91f8303481bd43940b8d88674d515dae9a67adf1cb51946`
-	Default Command: `["fsharpi"]`

```dockerfile
# Fri, 11 Dec 2020 02:06:10 GMT
ADD file:3a7bff4e139bcacc5831fd70a035c130a91b5da001dd91c08b2acd635c7064e8 in / 
# Fri, 11 Dec 2020 02:06:10 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 20:53:28 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Steve Desmond <steve@stevedesmond.ca>
# Fri, 11 Dec 2020 20:53:29 GMT
ENV MONO_THREADS_PER_CPU=50
# Fri, 11 Dec 2020 21:05:44 GMT
RUN MONO_VERSION=6.10.0.104 &&     FSHARP_VERSION=10.2.3 &&     FSHARP_BASENAME=fsharp-$FSHARP_VERSION &&     FSHARP_ARCHIVE=$FSHARP_VERSION.tar.gz &&     FSHARP_ARCHIVE_URL=https://github.com/fsharp/fsharp/archive/$FSHARP_VERSION.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     apt-get update && apt-get --no-install-recommends install -y gnupg dirmngr ca-certificates apt-transport-https &&     apt-key adv --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF &&     echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" | tee /etc/apt/sources.list.d/mono-official-stable.list &&     apt-get update -y &&     apt-get --no-install-recommends install -y pkg-config make nuget mono-devel msbuild ca-certificates-mono locales &&     rm -rf /var/lib/apt/lists/* &&     echo 'en_US.UTF-8 UTF-8' > /etc/locale.gen && /usr/sbin/locale-gen &&     mkdir -p /tmp/src &&     cd /tmp/src &&     printf "namespace a { class b { public static void Main(string[] args) { new System.Net.WebClient().DownloadFile(\"%s\", \"%s\");}}}" $FSHARP_ARCHIVE_URL $FSHARP_ARCHIVE > download-fsharp.cs &&     mcs download-fsharp.cs && mono download-fsharp.exe && rm download-fsharp.exe download-fsharp.cs &&     tar xf $FSHARP_ARCHIVE &&     cd $FSHARP_BASENAME &&     make &&     make install &&     cd ~ &&     rm -rf /tmp/src /tmp/NuGetScratch ~/.nuget ~/.config ~/.local "$GNUPGHOME" &&     apt-get purge -y make gnupg dirmngr &&     apt-get clean
# Fri, 11 Dec 2020 21:05:44 GMT
WORKDIR /root
# Fri, 11 Dec 2020 21:05:45 GMT
CMD ["fsharpi"]
```

-	Layers:
	-	`sha256:6ec7b7d162b24bd6df88abde89ceb6d7bbc2be927f025c9dd061af2b0c328cfe`  
		Last Modified: Fri, 11 Dec 2020 02:12:26 GMT  
		Size: 27.1 MB (27099295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:592b66fc0e6146332225bd3c9209957573ade3841386d2e76930121562261c53`  
		Last Modified: Fri, 11 Dec 2020 21:23:15 GMT  
		Size: 160.5 MB (160497317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fsharp:10` - linux; arm64 variant v8

```console
$ docker pull fsharp@sha256:92dd3ad7cf2e30413a8e4a6531c320ad72caaded363414cf7d9cd1ae4679d624
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.6 MB (184638587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99b435785b824a1e25bb1ce7ab1313c1b188dbd3563077aa34f157816e8f6ba6`
-	Default Command: `["fsharpi"]`

```dockerfile
# Fri, 11 Dec 2020 02:45:53 GMT
ADD file:a5a2f039c00bc638b88cefdff4c3cd1865b4d415bf80c4fe6b496d975af7cc1f in / 
# Fri, 11 Dec 2020 02:45:57 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 18:29:06 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Steve Desmond <steve@stevedesmond.ca>
# Fri, 11 Dec 2020 18:29:06 GMT
ENV MONO_THREADS_PER_CPU=50
# Fri, 11 Dec 2020 18:45:47 GMT
RUN MONO_VERSION=6.10.0.104 &&     FSHARP_VERSION=10.2.3 &&     FSHARP_BASENAME=fsharp-$FSHARP_VERSION &&     FSHARP_ARCHIVE=$FSHARP_VERSION.tar.gz &&     FSHARP_ARCHIVE_URL=https://github.com/fsharp/fsharp/archive/$FSHARP_VERSION.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     apt-get update && apt-get --no-install-recommends install -y gnupg dirmngr ca-certificates apt-transport-https &&     apt-key adv --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF &&     echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" | tee /etc/apt/sources.list.d/mono-official-stable.list &&     apt-get update -y &&     apt-get --no-install-recommends install -y pkg-config make nuget mono-devel msbuild ca-certificates-mono locales &&     rm -rf /var/lib/apt/lists/* &&     echo 'en_US.UTF-8 UTF-8' > /etc/locale.gen && /usr/sbin/locale-gen &&     mkdir -p /tmp/src &&     cd /tmp/src &&     printf "namespace a { class b { public static void Main(string[] args) { new System.Net.WebClient().DownloadFile(\"%s\", \"%s\");}}}" $FSHARP_ARCHIVE_URL $FSHARP_ARCHIVE > download-fsharp.cs &&     mcs download-fsharp.cs && mono download-fsharp.exe && rm download-fsharp.exe download-fsharp.cs &&     tar xf $FSHARP_ARCHIVE &&     cd $FSHARP_BASENAME &&     make &&     make install &&     cd ~ &&     rm -rf /tmp/src /tmp/NuGetScratch ~/.nuget ~/.config ~/.local "$GNUPGHOME" &&     apt-get purge -y make gnupg dirmngr &&     apt-get clean
# Fri, 11 Dec 2020 18:45:50 GMT
WORKDIR /root
# Fri, 11 Dec 2020 18:45:51 GMT
CMD ["fsharpi"]
```

-	Layers:
	-	`sha256:c9648d7fcbb6d597cf33916d8fcd207fde8ec05d764b4480d4f3e884e142a902`  
		Last Modified: Fri, 11 Dec 2020 02:53:14 GMT  
		Size: 25.9 MB (25856191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faaa9119f12b1196aa197a9a420cd83a697f01ae5773a1a4a989e5aeb3d57686`  
		Last Modified: Fri, 11 Dec 2020 18:46:51 GMT  
		Size: 158.8 MB (158782396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `fsharp:10.10`

```console
$ docker pull fsharp@sha256:4cc2ce49d433271ad3ec56129386dced09643d7c7f035461212c0e1a03772818
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `fsharp:10.10` - linux; amd64

```console
$ docker pull fsharp@sha256:aade83420e7ffa1d331e0b7d6ea8a79d6669b3e40406a2ee69762cc95adc9a47
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.6 MB (187596612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:565b414f7f0e6e90b91f8303481bd43940b8d88674d515dae9a67adf1cb51946`
-	Default Command: `["fsharpi"]`

```dockerfile
# Fri, 11 Dec 2020 02:06:10 GMT
ADD file:3a7bff4e139bcacc5831fd70a035c130a91b5da001dd91c08b2acd635c7064e8 in / 
# Fri, 11 Dec 2020 02:06:10 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 20:53:28 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Steve Desmond <steve@stevedesmond.ca>
# Fri, 11 Dec 2020 20:53:29 GMT
ENV MONO_THREADS_PER_CPU=50
# Fri, 11 Dec 2020 21:05:44 GMT
RUN MONO_VERSION=6.10.0.104 &&     FSHARP_VERSION=10.2.3 &&     FSHARP_BASENAME=fsharp-$FSHARP_VERSION &&     FSHARP_ARCHIVE=$FSHARP_VERSION.tar.gz &&     FSHARP_ARCHIVE_URL=https://github.com/fsharp/fsharp/archive/$FSHARP_VERSION.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     apt-get update && apt-get --no-install-recommends install -y gnupg dirmngr ca-certificates apt-transport-https &&     apt-key adv --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF &&     echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" | tee /etc/apt/sources.list.d/mono-official-stable.list &&     apt-get update -y &&     apt-get --no-install-recommends install -y pkg-config make nuget mono-devel msbuild ca-certificates-mono locales &&     rm -rf /var/lib/apt/lists/* &&     echo 'en_US.UTF-8 UTF-8' > /etc/locale.gen && /usr/sbin/locale-gen &&     mkdir -p /tmp/src &&     cd /tmp/src &&     printf "namespace a { class b { public static void Main(string[] args) { new System.Net.WebClient().DownloadFile(\"%s\", \"%s\");}}}" $FSHARP_ARCHIVE_URL $FSHARP_ARCHIVE > download-fsharp.cs &&     mcs download-fsharp.cs && mono download-fsharp.exe && rm download-fsharp.exe download-fsharp.cs &&     tar xf $FSHARP_ARCHIVE &&     cd $FSHARP_BASENAME &&     make &&     make install &&     cd ~ &&     rm -rf /tmp/src /tmp/NuGetScratch ~/.nuget ~/.config ~/.local "$GNUPGHOME" &&     apt-get purge -y make gnupg dirmngr &&     apt-get clean
# Fri, 11 Dec 2020 21:05:44 GMT
WORKDIR /root
# Fri, 11 Dec 2020 21:05:45 GMT
CMD ["fsharpi"]
```

-	Layers:
	-	`sha256:6ec7b7d162b24bd6df88abde89ceb6d7bbc2be927f025c9dd061af2b0c328cfe`  
		Last Modified: Fri, 11 Dec 2020 02:12:26 GMT  
		Size: 27.1 MB (27099295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:592b66fc0e6146332225bd3c9209957573ade3841386d2e76930121562261c53`  
		Last Modified: Fri, 11 Dec 2020 21:23:15 GMT  
		Size: 160.5 MB (160497317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fsharp:10.10` - linux; arm64 variant v8

```console
$ docker pull fsharp@sha256:92dd3ad7cf2e30413a8e4a6531c320ad72caaded363414cf7d9cd1ae4679d624
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.6 MB (184638587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99b435785b824a1e25bb1ce7ab1313c1b188dbd3563077aa34f157816e8f6ba6`
-	Default Command: `["fsharpi"]`

```dockerfile
# Fri, 11 Dec 2020 02:45:53 GMT
ADD file:a5a2f039c00bc638b88cefdff4c3cd1865b4d415bf80c4fe6b496d975af7cc1f in / 
# Fri, 11 Dec 2020 02:45:57 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 18:29:06 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Steve Desmond <steve@stevedesmond.ca>
# Fri, 11 Dec 2020 18:29:06 GMT
ENV MONO_THREADS_PER_CPU=50
# Fri, 11 Dec 2020 18:45:47 GMT
RUN MONO_VERSION=6.10.0.104 &&     FSHARP_VERSION=10.2.3 &&     FSHARP_BASENAME=fsharp-$FSHARP_VERSION &&     FSHARP_ARCHIVE=$FSHARP_VERSION.tar.gz &&     FSHARP_ARCHIVE_URL=https://github.com/fsharp/fsharp/archive/$FSHARP_VERSION.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     apt-get update && apt-get --no-install-recommends install -y gnupg dirmngr ca-certificates apt-transport-https &&     apt-key adv --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF &&     echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" | tee /etc/apt/sources.list.d/mono-official-stable.list &&     apt-get update -y &&     apt-get --no-install-recommends install -y pkg-config make nuget mono-devel msbuild ca-certificates-mono locales &&     rm -rf /var/lib/apt/lists/* &&     echo 'en_US.UTF-8 UTF-8' > /etc/locale.gen && /usr/sbin/locale-gen &&     mkdir -p /tmp/src &&     cd /tmp/src &&     printf "namespace a { class b { public static void Main(string[] args) { new System.Net.WebClient().DownloadFile(\"%s\", \"%s\");}}}" $FSHARP_ARCHIVE_URL $FSHARP_ARCHIVE > download-fsharp.cs &&     mcs download-fsharp.cs && mono download-fsharp.exe && rm download-fsharp.exe download-fsharp.cs &&     tar xf $FSHARP_ARCHIVE &&     cd $FSHARP_BASENAME &&     make &&     make install &&     cd ~ &&     rm -rf /tmp/src /tmp/NuGetScratch ~/.nuget ~/.config ~/.local "$GNUPGHOME" &&     apt-get purge -y make gnupg dirmngr &&     apt-get clean
# Fri, 11 Dec 2020 18:45:50 GMT
WORKDIR /root
# Fri, 11 Dec 2020 18:45:51 GMT
CMD ["fsharpi"]
```

-	Layers:
	-	`sha256:c9648d7fcbb6d597cf33916d8fcd207fde8ec05d764b4480d4f3e884e142a902`  
		Last Modified: Fri, 11 Dec 2020 02:53:14 GMT  
		Size: 25.9 MB (25856191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faaa9119f12b1196aa197a9a420cd83a697f01ae5773a1a4a989e5aeb3d57686`  
		Last Modified: Fri, 11 Dec 2020 18:46:51 GMT  
		Size: 158.8 MB (158782396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `fsharp:10.10.0`

```console
$ docker pull fsharp@sha256:4cc2ce49d433271ad3ec56129386dced09643d7c7f035461212c0e1a03772818
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `fsharp:10.10.0` - linux; amd64

```console
$ docker pull fsharp@sha256:aade83420e7ffa1d331e0b7d6ea8a79d6669b3e40406a2ee69762cc95adc9a47
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.6 MB (187596612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:565b414f7f0e6e90b91f8303481bd43940b8d88674d515dae9a67adf1cb51946`
-	Default Command: `["fsharpi"]`

```dockerfile
# Fri, 11 Dec 2020 02:06:10 GMT
ADD file:3a7bff4e139bcacc5831fd70a035c130a91b5da001dd91c08b2acd635c7064e8 in / 
# Fri, 11 Dec 2020 02:06:10 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 20:53:28 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Steve Desmond <steve@stevedesmond.ca>
# Fri, 11 Dec 2020 20:53:29 GMT
ENV MONO_THREADS_PER_CPU=50
# Fri, 11 Dec 2020 21:05:44 GMT
RUN MONO_VERSION=6.10.0.104 &&     FSHARP_VERSION=10.2.3 &&     FSHARP_BASENAME=fsharp-$FSHARP_VERSION &&     FSHARP_ARCHIVE=$FSHARP_VERSION.tar.gz &&     FSHARP_ARCHIVE_URL=https://github.com/fsharp/fsharp/archive/$FSHARP_VERSION.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     apt-get update && apt-get --no-install-recommends install -y gnupg dirmngr ca-certificates apt-transport-https &&     apt-key adv --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF &&     echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" | tee /etc/apt/sources.list.d/mono-official-stable.list &&     apt-get update -y &&     apt-get --no-install-recommends install -y pkg-config make nuget mono-devel msbuild ca-certificates-mono locales &&     rm -rf /var/lib/apt/lists/* &&     echo 'en_US.UTF-8 UTF-8' > /etc/locale.gen && /usr/sbin/locale-gen &&     mkdir -p /tmp/src &&     cd /tmp/src &&     printf "namespace a { class b { public static void Main(string[] args) { new System.Net.WebClient().DownloadFile(\"%s\", \"%s\");}}}" $FSHARP_ARCHIVE_URL $FSHARP_ARCHIVE > download-fsharp.cs &&     mcs download-fsharp.cs && mono download-fsharp.exe && rm download-fsharp.exe download-fsharp.cs &&     tar xf $FSHARP_ARCHIVE &&     cd $FSHARP_BASENAME &&     make &&     make install &&     cd ~ &&     rm -rf /tmp/src /tmp/NuGetScratch ~/.nuget ~/.config ~/.local "$GNUPGHOME" &&     apt-get purge -y make gnupg dirmngr &&     apt-get clean
# Fri, 11 Dec 2020 21:05:44 GMT
WORKDIR /root
# Fri, 11 Dec 2020 21:05:45 GMT
CMD ["fsharpi"]
```

-	Layers:
	-	`sha256:6ec7b7d162b24bd6df88abde89ceb6d7bbc2be927f025c9dd061af2b0c328cfe`  
		Last Modified: Fri, 11 Dec 2020 02:12:26 GMT  
		Size: 27.1 MB (27099295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:592b66fc0e6146332225bd3c9209957573ade3841386d2e76930121562261c53`  
		Last Modified: Fri, 11 Dec 2020 21:23:15 GMT  
		Size: 160.5 MB (160497317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fsharp:10.10.0` - linux; arm64 variant v8

```console
$ docker pull fsharp@sha256:92dd3ad7cf2e30413a8e4a6531c320ad72caaded363414cf7d9cd1ae4679d624
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.6 MB (184638587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99b435785b824a1e25bb1ce7ab1313c1b188dbd3563077aa34f157816e8f6ba6`
-	Default Command: `["fsharpi"]`

```dockerfile
# Fri, 11 Dec 2020 02:45:53 GMT
ADD file:a5a2f039c00bc638b88cefdff4c3cd1865b4d415bf80c4fe6b496d975af7cc1f in / 
# Fri, 11 Dec 2020 02:45:57 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 18:29:06 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Steve Desmond <steve@stevedesmond.ca>
# Fri, 11 Dec 2020 18:29:06 GMT
ENV MONO_THREADS_PER_CPU=50
# Fri, 11 Dec 2020 18:45:47 GMT
RUN MONO_VERSION=6.10.0.104 &&     FSHARP_VERSION=10.2.3 &&     FSHARP_BASENAME=fsharp-$FSHARP_VERSION &&     FSHARP_ARCHIVE=$FSHARP_VERSION.tar.gz &&     FSHARP_ARCHIVE_URL=https://github.com/fsharp/fsharp/archive/$FSHARP_VERSION.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     apt-get update && apt-get --no-install-recommends install -y gnupg dirmngr ca-certificates apt-transport-https &&     apt-key adv --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF &&     echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" | tee /etc/apt/sources.list.d/mono-official-stable.list &&     apt-get update -y &&     apt-get --no-install-recommends install -y pkg-config make nuget mono-devel msbuild ca-certificates-mono locales &&     rm -rf /var/lib/apt/lists/* &&     echo 'en_US.UTF-8 UTF-8' > /etc/locale.gen && /usr/sbin/locale-gen &&     mkdir -p /tmp/src &&     cd /tmp/src &&     printf "namespace a { class b { public static void Main(string[] args) { new System.Net.WebClient().DownloadFile(\"%s\", \"%s\");}}}" $FSHARP_ARCHIVE_URL $FSHARP_ARCHIVE > download-fsharp.cs &&     mcs download-fsharp.cs && mono download-fsharp.exe && rm download-fsharp.exe download-fsharp.cs &&     tar xf $FSHARP_ARCHIVE &&     cd $FSHARP_BASENAME &&     make &&     make install &&     cd ~ &&     rm -rf /tmp/src /tmp/NuGetScratch ~/.nuget ~/.config ~/.local "$GNUPGHOME" &&     apt-get purge -y make gnupg dirmngr &&     apt-get clean
# Fri, 11 Dec 2020 18:45:50 GMT
WORKDIR /root
# Fri, 11 Dec 2020 18:45:51 GMT
CMD ["fsharpi"]
```

-	Layers:
	-	`sha256:c9648d7fcbb6d597cf33916d8fcd207fde8ec05d764b4480d4f3e884e142a902`  
		Last Modified: Fri, 11 Dec 2020 02:53:14 GMT  
		Size: 25.9 MB (25856191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faaa9119f12b1196aa197a9a420cd83a697f01ae5773a1a4a989e5aeb3d57686`  
		Last Modified: Fri, 11 Dec 2020 18:46:51 GMT  
		Size: 158.8 MB (158782396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `fsharp:10.10.0-netcore`

```console
$ docker pull fsharp@sha256:28e56ee182f526797442189b0f7db5d00a9f45e14d9258861068e3a7dda59b4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `fsharp:10.10.0-netcore` - linux; amd64

```console
$ docker pull fsharp@sha256:01d52abb34297b6148e22dcf4b9aa76be8c98efb697bc7753caa9d5af34f7d7c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.9 MB (332924118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c5549b0f5f12fa7c92ee3b7426c78f09bc2ef3c767d66d1b8a85cf4d249ff83`
-	Default Command: `["dotnet","fsi"]`

```dockerfile
# Fri, 11 Dec 2020 02:06:10 GMT
ADD file:3a7bff4e139bcacc5831fd70a035c130a91b5da001dd91c08b2acd635c7064e8 in / 
# Fri, 11 Dec 2020 02:06:10 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 20:53:28 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Steve Desmond <steve@stevedesmond.ca>
# Fri, 11 Dec 2020 20:53:29 GMT
ENV MONO_THREADS_PER_CPU=50
# Fri, 11 Dec 2020 21:05:44 GMT
RUN MONO_VERSION=6.10.0.104 &&     FSHARP_VERSION=10.2.3 &&     FSHARP_BASENAME=fsharp-$FSHARP_VERSION &&     FSHARP_ARCHIVE=$FSHARP_VERSION.tar.gz &&     FSHARP_ARCHIVE_URL=https://github.com/fsharp/fsharp/archive/$FSHARP_VERSION.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     apt-get update && apt-get --no-install-recommends install -y gnupg dirmngr ca-certificates apt-transport-https &&     apt-key adv --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF &&     echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" | tee /etc/apt/sources.list.d/mono-official-stable.list &&     apt-get update -y &&     apt-get --no-install-recommends install -y pkg-config make nuget mono-devel msbuild ca-certificates-mono locales &&     rm -rf /var/lib/apt/lists/* &&     echo 'en_US.UTF-8 UTF-8' > /etc/locale.gen && /usr/sbin/locale-gen &&     mkdir -p /tmp/src &&     cd /tmp/src &&     printf "namespace a { class b { public static void Main(string[] args) { new System.Net.WebClient().DownloadFile(\"%s\", \"%s\");}}}" $FSHARP_ARCHIVE_URL $FSHARP_ARCHIVE > download-fsharp.cs &&     mcs download-fsharp.cs && mono download-fsharp.exe && rm download-fsharp.exe download-fsharp.cs &&     tar xf $FSHARP_ARCHIVE &&     cd $FSHARP_BASENAME &&     make &&     make install &&     cd ~ &&     rm -rf /tmp/src /tmp/NuGetScratch ~/.nuget ~/.config ~/.local "$GNUPGHOME" &&     apt-get purge -y make gnupg dirmngr &&     apt-get clean
# Fri, 11 Dec 2020 21:05:44 GMT
WORKDIR /root
# Fri, 11 Dec 2020 21:05:45 GMT
CMD ["fsharpi"]
# Fri, 11 Dec 2020 21:21:29 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Steve Desmond <steve@stevedesmond.ca>
# Fri, 11 Dec 2020 21:21:30 GMT
ENV FrameworkPathOverride=/usr/lib/mono/4.8-api/
# Fri, 11 Dec 2020 21:21:30 GMT
ENV NUGET_XMLDOC_MODE=skip DOTNET_RUNNING_IN_CONTAINER=true DOTNET_USE_POLLING_FILE_WATCHER=true
# Fri, 11 Dec 2020 21:21:46 GMT
RUN apt-get update &&     apt-get --no-install-recommends install -y     curl     libunwind8     gettext     apt-transport-https     libc6     libcurl4     libgcc1     libgssapi-krb5-2     libicu63     liblttng-ust0     libssl1.1     libstdc++6     libunwind8     libuuid1     zlib1g &&     rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 21:22:05 GMT
RUN DOTNET_SDK_VERSION=3.1.403 &&     DOTNET_SDK_DOWNLOAD_URL=https://dotnetcli.blob.core.windows.net/dotnet/Sdk/$DOTNET_SDK_VERSION/dotnet-sdk-$DOTNET_SDK_VERSION-linux-x64.tar.gz &&     DOTNET_SDK_DOWNLOAD_SHA=0a0319ee8e9042bf04b6e83211c2d6e44e40e604bff0a133ba0d246d08bff76ebd88918ab5e10e6f7f0d2b504ddeb65c0108c6539bc4fbc4f09e4af3937e88ea &&     curl -SL $DOTNET_SDK_DOWNLOAD_URL --output dotnet.tar.gz &&     echo "$DOTNET_SDK_DOWNLOAD_SHA dotnet.tar.gz" | sha512sum -c - &&     mkdir -p /usr/share/dotnet &&     tar -zxf dotnet.tar.gz -C /usr/share/dotnet &&     rm dotnet.tar.gz &&     ln -s /usr/share/dotnet/dotnet /usr/bin/dotnet
# Fri, 11 Dec 2020 21:22:08 GMT
RUN mkdir warmup &&     cd warmup &&     dotnet new &&     cd - &&     rm -rf warmup /tmp/NuGetScratch
# Fri, 11 Dec 2020 21:22:08 GMT
WORKDIR /root
# Fri, 11 Dec 2020 21:22:08 GMT
CMD ["dotnet" "fsi"]
```

-	Layers:
	-	`sha256:6ec7b7d162b24bd6df88abde89ceb6d7bbc2be927f025c9dd061af2b0c328cfe`  
		Last Modified: Fri, 11 Dec 2020 02:12:26 GMT  
		Size: 27.1 MB (27099295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:592b66fc0e6146332225bd3c9209957573ade3841386d2e76930121562261c53`  
		Last Modified: Fri, 11 Dec 2020 21:23:15 GMT  
		Size: 160.5 MB (160497317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f30a41990d8aadbf81e4422ef3715f0985f735ca6bcbdeb016e6d5db760fc005`  
		Last Modified: Fri, 11 Dec 2020 21:24:09 GMT  
		Size: 17.2 MB (17205406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e30c25efa90ffeeb491d709a2e0e7da78bab948e0a1f44cf069e665dc646bbc`  
		Last Modified: Fri, 11 Dec 2020 21:24:31 GMT  
		Size: 123.8 MB (123846235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed800c9c105ce424d66e6991a33c4ee02c4aaec21d38288362b356b9dcc34229`  
		Last Modified: Fri, 11 Dec 2020 21:24:06 GMT  
		Size: 4.3 MB (4275865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `fsharp:10.10-netcore`

```console
$ docker pull fsharp@sha256:28e56ee182f526797442189b0f7db5d00a9f45e14d9258861068e3a7dda59b4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `fsharp:10.10-netcore` - linux; amd64

```console
$ docker pull fsharp@sha256:01d52abb34297b6148e22dcf4b9aa76be8c98efb697bc7753caa9d5af34f7d7c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.9 MB (332924118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c5549b0f5f12fa7c92ee3b7426c78f09bc2ef3c767d66d1b8a85cf4d249ff83`
-	Default Command: `["dotnet","fsi"]`

```dockerfile
# Fri, 11 Dec 2020 02:06:10 GMT
ADD file:3a7bff4e139bcacc5831fd70a035c130a91b5da001dd91c08b2acd635c7064e8 in / 
# Fri, 11 Dec 2020 02:06:10 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 20:53:28 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Steve Desmond <steve@stevedesmond.ca>
# Fri, 11 Dec 2020 20:53:29 GMT
ENV MONO_THREADS_PER_CPU=50
# Fri, 11 Dec 2020 21:05:44 GMT
RUN MONO_VERSION=6.10.0.104 &&     FSHARP_VERSION=10.2.3 &&     FSHARP_BASENAME=fsharp-$FSHARP_VERSION &&     FSHARP_ARCHIVE=$FSHARP_VERSION.tar.gz &&     FSHARP_ARCHIVE_URL=https://github.com/fsharp/fsharp/archive/$FSHARP_VERSION.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     apt-get update && apt-get --no-install-recommends install -y gnupg dirmngr ca-certificates apt-transport-https &&     apt-key adv --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF &&     echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" | tee /etc/apt/sources.list.d/mono-official-stable.list &&     apt-get update -y &&     apt-get --no-install-recommends install -y pkg-config make nuget mono-devel msbuild ca-certificates-mono locales &&     rm -rf /var/lib/apt/lists/* &&     echo 'en_US.UTF-8 UTF-8' > /etc/locale.gen && /usr/sbin/locale-gen &&     mkdir -p /tmp/src &&     cd /tmp/src &&     printf "namespace a { class b { public static void Main(string[] args) { new System.Net.WebClient().DownloadFile(\"%s\", \"%s\");}}}" $FSHARP_ARCHIVE_URL $FSHARP_ARCHIVE > download-fsharp.cs &&     mcs download-fsharp.cs && mono download-fsharp.exe && rm download-fsharp.exe download-fsharp.cs &&     tar xf $FSHARP_ARCHIVE &&     cd $FSHARP_BASENAME &&     make &&     make install &&     cd ~ &&     rm -rf /tmp/src /tmp/NuGetScratch ~/.nuget ~/.config ~/.local "$GNUPGHOME" &&     apt-get purge -y make gnupg dirmngr &&     apt-get clean
# Fri, 11 Dec 2020 21:05:44 GMT
WORKDIR /root
# Fri, 11 Dec 2020 21:05:45 GMT
CMD ["fsharpi"]
# Fri, 11 Dec 2020 21:21:29 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Steve Desmond <steve@stevedesmond.ca>
# Fri, 11 Dec 2020 21:21:30 GMT
ENV FrameworkPathOverride=/usr/lib/mono/4.8-api/
# Fri, 11 Dec 2020 21:21:30 GMT
ENV NUGET_XMLDOC_MODE=skip DOTNET_RUNNING_IN_CONTAINER=true DOTNET_USE_POLLING_FILE_WATCHER=true
# Fri, 11 Dec 2020 21:21:46 GMT
RUN apt-get update &&     apt-get --no-install-recommends install -y     curl     libunwind8     gettext     apt-transport-https     libc6     libcurl4     libgcc1     libgssapi-krb5-2     libicu63     liblttng-ust0     libssl1.1     libstdc++6     libunwind8     libuuid1     zlib1g &&     rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 21:22:05 GMT
RUN DOTNET_SDK_VERSION=3.1.403 &&     DOTNET_SDK_DOWNLOAD_URL=https://dotnetcli.blob.core.windows.net/dotnet/Sdk/$DOTNET_SDK_VERSION/dotnet-sdk-$DOTNET_SDK_VERSION-linux-x64.tar.gz &&     DOTNET_SDK_DOWNLOAD_SHA=0a0319ee8e9042bf04b6e83211c2d6e44e40e604bff0a133ba0d246d08bff76ebd88918ab5e10e6f7f0d2b504ddeb65c0108c6539bc4fbc4f09e4af3937e88ea &&     curl -SL $DOTNET_SDK_DOWNLOAD_URL --output dotnet.tar.gz &&     echo "$DOTNET_SDK_DOWNLOAD_SHA dotnet.tar.gz" | sha512sum -c - &&     mkdir -p /usr/share/dotnet &&     tar -zxf dotnet.tar.gz -C /usr/share/dotnet &&     rm dotnet.tar.gz &&     ln -s /usr/share/dotnet/dotnet /usr/bin/dotnet
# Fri, 11 Dec 2020 21:22:08 GMT
RUN mkdir warmup &&     cd warmup &&     dotnet new &&     cd - &&     rm -rf warmup /tmp/NuGetScratch
# Fri, 11 Dec 2020 21:22:08 GMT
WORKDIR /root
# Fri, 11 Dec 2020 21:22:08 GMT
CMD ["dotnet" "fsi"]
```

-	Layers:
	-	`sha256:6ec7b7d162b24bd6df88abde89ceb6d7bbc2be927f025c9dd061af2b0c328cfe`  
		Last Modified: Fri, 11 Dec 2020 02:12:26 GMT  
		Size: 27.1 MB (27099295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:592b66fc0e6146332225bd3c9209957573ade3841386d2e76930121562261c53`  
		Last Modified: Fri, 11 Dec 2020 21:23:15 GMT  
		Size: 160.5 MB (160497317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f30a41990d8aadbf81e4422ef3715f0985f735ca6bcbdeb016e6d5db760fc005`  
		Last Modified: Fri, 11 Dec 2020 21:24:09 GMT  
		Size: 17.2 MB (17205406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e30c25efa90ffeeb491d709a2e0e7da78bab948e0a1f44cf069e665dc646bbc`  
		Last Modified: Fri, 11 Dec 2020 21:24:31 GMT  
		Size: 123.8 MB (123846235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed800c9c105ce424d66e6991a33c4ee02c4aaec21d38288362b356b9dcc34229`  
		Last Modified: Fri, 11 Dec 2020 21:24:06 GMT  
		Size: 4.3 MB (4275865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `fsharp:10-netcore`

```console
$ docker pull fsharp@sha256:28e56ee182f526797442189b0f7db5d00a9f45e14d9258861068e3a7dda59b4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `fsharp:10-netcore` - linux; amd64

```console
$ docker pull fsharp@sha256:01d52abb34297b6148e22dcf4b9aa76be8c98efb697bc7753caa9d5af34f7d7c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.9 MB (332924118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c5549b0f5f12fa7c92ee3b7426c78f09bc2ef3c767d66d1b8a85cf4d249ff83`
-	Default Command: `["dotnet","fsi"]`

```dockerfile
# Fri, 11 Dec 2020 02:06:10 GMT
ADD file:3a7bff4e139bcacc5831fd70a035c130a91b5da001dd91c08b2acd635c7064e8 in / 
# Fri, 11 Dec 2020 02:06:10 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 20:53:28 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Steve Desmond <steve@stevedesmond.ca>
# Fri, 11 Dec 2020 20:53:29 GMT
ENV MONO_THREADS_PER_CPU=50
# Fri, 11 Dec 2020 21:05:44 GMT
RUN MONO_VERSION=6.10.0.104 &&     FSHARP_VERSION=10.2.3 &&     FSHARP_BASENAME=fsharp-$FSHARP_VERSION &&     FSHARP_ARCHIVE=$FSHARP_VERSION.tar.gz &&     FSHARP_ARCHIVE_URL=https://github.com/fsharp/fsharp/archive/$FSHARP_VERSION.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     apt-get update && apt-get --no-install-recommends install -y gnupg dirmngr ca-certificates apt-transport-https &&     apt-key adv --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF &&     echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" | tee /etc/apt/sources.list.d/mono-official-stable.list &&     apt-get update -y &&     apt-get --no-install-recommends install -y pkg-config make nuget mono-devel msbuild ca-certificates-mono locales &&     rm -rf /var/lib/apt/lists/* &&     echo 'en_US.UTF-8 UTF-8' > /etc/locale.gen && /usr/sbin/locale-gen &&     mkdir -p /tmp/src &&     cd /tmp/src &&     printf "namespace a { class b { public static void Main(string[] args) { new System.Net.WebClient().DownloadFile(\"%s\", \"%s\");}}}" $FSHARP_ARCHIVE_URL $FSHARP_ARCHIVE > download-fsharp.cs &&     mcs download-fsharp.cs && mono download-fsharp.exe && rm download-fsharp.exe download-fsharp.cs &&     tar xf $FSHARP_ARCHIVE &&     cd $FSHARP_BASENAME &&     make &&     make install &&     cd ~ &&     rm -rf /tmp/src /tmp/NuGetScratch ~/.nuget ~/.config ~/.local "$GNUPGHOME" &&     apt-get purge -y make gnupg dirmngr &&     apt-get clean
# Fri, 11 Dec 2020 21:05:44 GMT
WORKDIR /root
# Fri, 11 Dec 2020 21:05:45 GMT
CMD ["fsharpi"]
# Fri, 11 Dec 2020 21:21:29 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Steve Desmond <steve@stevedesmond.ca>
# Fri, 11 Dec 2020 21:21:30 GMT
ENV FrameworkPathOverride=/usr/lib/mono/4.8-api/
# Fri, 11 Dec 2020 21:21:30 GMT
ENV NUGET_XMLDOC_MODE=skip DOTNET_RUNNING_IN_CONTAINER=true DOTNET_USE_POLLING_FILE_WATCHER=true
# Fri, 11 Dec 2020 21:21:46 GMT
RUN apt-get update &&     apt-get --no-install-recommends install -y     curl     libunwind8     gettext     apt-transport-https     libc6     libcurl4     libgcc1     libgssapi-krb5-2     libicu63     liblttng-ust0     libssl1.1     libstdc++6     libunwind8     libuuid1     zlib1g &&     rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 21:22:05 GMT
RUN DOTNET_SDK_VERSION=3.1.403 &&     DOTNET_SDK_DOWNLOAD_URL=https://dotnetcli.blob.core.windows.net/dotnet/Sdk/$DOTNET_SDK_VERSION/dotnet-sdk-$DOTNET_SDK_VERSION-linux-x64.tar.gz &&     DOTNET_SDK_DOWNLOAD_SHA=0a0319ee8e9042bf04b6e83211c2d6e44e40e604bff0a133ba0d246d08bff76ebd88918ab5e10e6f7f0d2b504ddeb65c0108c6539bc4fbc4f09e4af3937e88ea &&     curl -SL $DOTNET_SDK_DOWNLOAD_URL --output dotnet.tar.gz &&     echo "$DOTNET_SDK_DOWNLOAD_SHA dotnet.tar.gz" | sha512sum -c - &&     mkdir -p /usr/share/dotnet &&     tar -zxf dotnet.tar.gz -C /usr/share/dotnet &&     rm dotnet.tar.gz &&     ln -s /usr/share/dotnet/dotnet /usr/bin/dotnet
# Fri, 11 Dec 2020 21:22:08 GMT
RUN mkdir warmup &&     cd warmup &&     dotnet new &&     cd - &&     rm -rf warmup /tmp/NuGetScratch
# Fri, 11 Dec 2020 21:22:08 GMT
WORKDIR /root
# Fri, 11 Dec 2020 21:22:08 GMT
CMD ["dotnet" "fsi"]
```

-	Layers:
	-	`sha256:6ec7b7d162b24bd6df88abde89ceb6d7bbc2be927f025c9dd061af2b0c328cfe`  
		Last Modified: Fri, 11 Dec 2020 02:12:26 GMT  
		Size: 27.1 MB (27099295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:592b66fc0e6146332225bd3c9209957573ade3841386d2e76930121562261c53`  
		Last Modified: Fri, 11 Dec 2020 21:23:15 GMT  
		Size: 160.5 MB (160497317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f30a41990d8aadbf81e4422ef3715f0985f735ca6bcbdeb016e6d5db760fc005`  
		Last Modified: Fri, 11 Dec 2020 21:24:09 GMT  
		Size: 17.2 MB (17205406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e30c25efa90ffeeb491d709a2e0e7da78bab948e0a1f44cf069e665dc646bbc`  
		Last Modified: Fri, 11 Dec 2020 21:24:31 GMT  
		Size: 123.8 MB (123846235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed800c9c105ce424d66e6991a33c4ee02c4aaec21d38288362b356b9dcc34229`  
		Last Modified: Fri, 11 Dec 2020 21:24:06 GMT  
		Size: 4.3 MB (4275865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `fsharp:4`

```console
$ docker pull fsharp@sha256:105e5bf54200e8793d42ccd760d826448ab791a0b53142f6aaa3a58c83baffa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `fsharp:4` - linux; amd64

```console
$ docker pull fsharp@sha256:9c410159ef06d0a9eb866da569d80177d53c57b094230348087beb8880a153a7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.3 MB (176301201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3231a9abdfffb5e4094c783908cb611f953eef65d48156b73aaf3301670bc3ba`
-	Default Command: `["fsharpi"]`

```dockerfile
# Fri, 11 Dec 2020 02:06:38 GMT
ADD file:af2b011a1bf144775df803945ea05c1f390e292cb2ee570501c61318d6df0618 in / 
# Fri, 11 Dec 2020 02:06:39 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 21:05:56 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Steve Desmond <steve@stevedesmond.ca>
# Fri, 11 Dec 2020 21:05:57 GMT
ENV MONO_THREADS_PER_CPU=50
# Fri, 11 Dec 2020 21:21:13 GMT
RUN MONO_VERSION=5.8.0.108 &&     FSHARP_VERSION=4.1.34 &&     FSHARP_PREFIX=/usr &&     FSHARP_GACDIR=/usr/lib/mono/gac &&     FSHARP_BASENAME=fsharp-$FSHARP_VERSION &&     FSHARP_ARCHIVE=$FSHARP_VERSION.tar.gz &&     FSHARP_ARCHIVE_URL=https://github.com/fsharp/fsharp/archive/$FSHARP_VERSION.tar.gz &&     apt-key adv --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF &&     echo "deb http://download.mono-project.com/repo/debian jessie/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official.list &&     apt-get update -y &&     apt-get --no-install-recommends install -y autoconf libtool pkg-config make automake nuget mono-devel msbuild ca-certificates-mono &&     rm -rf /var/lib/apt/lists/* &&     mkdir -p /tmp/src &&     cd /tmp/src &&     printf "namespace a { class b { public static void Main(string[] args) { new System.Net.WebClient().DownloadFile(\"%s\", \"%s\");}}}" $FSHARP_ARCHIVE_URL $FSHARP_ARCHIVE > download-fsharp.cs &&     mcs download-fsharp.cs && mono download-fsharp.exe && rm download-fsharp.exe download-fsharp.cs &&     tar xf $FSHARP_ARCHIVE &&     cd $FSHARP_BASENAME &&     ./autogen.sh --prefix=$FSHARP_PREFIX --with-gacdir=$FSHARP_GACDIR &&     make &&     make install &&     cd ~ &&     rm -rf /tmp/src /tmp/NuGetScratch ~/.nuget ~/.config ~/.local &&     apt-get purge -y autoconf libtool make automake &&     apt-get clean
# Fri, 11 Dec 2020 21:21:14 GMT
WORKDIR /root
# Fri, 11 Dec 2020 21:21:14 GMT
CMD ["fsharpi"]
```

-	Layers:
	-	`sha256:dcd56748d94df613708f45494d30c45e8e94b1d61a697cbbf113327fac0d96a7`  
		Last Modified: Fri, 11 Dec 2020 02:12:59 GMT  
		Size: 30.2 MB (30159877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcad88aabd46d82f501c4aa9bb6e437cf2c4f331a74ceaf3f7f03856677fb804`  
		Last Modified: Fri, 11 Dec 2020 21:23:57 GMT  
		Size: 146.1 MB (146141324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `fsharp:4.1`

```console
$ docker pull fsharp@sha256:105e5bf54200e8793d42ccd760d826448ab791a0b53142f6aaa3a58c83baffa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `fsharp:4.1` - linux; amd64

```console
$ docker pull fsharp@sha256:9c410159ef06d0a9eb866da569d80177d53c57b094230348087beb8880a153a7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.3 MB (176301201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3231a9abdfffb5e4094c783908cb611f953eef65d48156b73aaf3301670bc3ba`
-	Default Command: `["fsharpi"]`

```dockerfile
# Fri, 11 Dec 2020 02:06:38 GMT
ADD file:af2b011a1bf144775df803945ea05c1f390e292cb2ee570501c61318d6df0618 in / 
# Fri, 11 Dec 2020 02:06:39 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 21:05:56 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Steve Desmond <steve@stevedesmond.ca>
# Fri, 11 Dec 2020 21:05:57 GMT
ENV MONO_THREADS_PER_CPU=50
# Fri, 11 Dec 2020 21:21:13 GMT
RUN MONO_VERSION=5.8.0.108 &&     FSHARP_VERSION=4.1.34 &&     FSHARP_PREFIX=/usr &&     FSHARP_GACDIR=/usr/lib/mono/gac &&     FSHARP_BASENAME=fsharp-$FSHARP_VERSION &&     FSHARP_ARCHIVE=$FSHARP_VERSION.tar.gz &&     FSHARP_ARCHIVE_URL=https://github.com/fsharp/fsharp/archive/$FSHARP_VERSION.tar.gz &&     apt-key adv --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF &&     echo "deb http://download.mono-project.com/repo/debian jessie/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official.list &&     apt-get update -y &&     apt-get --no-install-recommends install -y autoconf libtool pkg-config make automake nuget mono-devel msbuild ca-certificates-mono &&     rm -rf /var/lib/apt/lists/* &&     mkdir -p /tmp/src &&     cd /tmp/src &&     printf "namespace a { class b { public static void Main(string[] args) { new System.Net.WebClient().DownloadFile(\"%s\", \"%s\");}}}" $FSHARP_ARCHIVE_URL $FSHARP_ARCHIVE > download-fsharp.cs &&     mcs download-fsharp.cs && mono download-fsharp.exe && rm download-fsharp.exe download-fsharp.cs &&     tar xf $FSHARP_ARCHIVE &&     cd $FSHARP_BASENAME &&     ./autogen.sh --prefix=$FSHARP_PREFIX --with-gacdir=$FSHARP_GACDIR &&     make &&     make install &&     cd ~ &&     rm -rf /tmp/src /tmp/NuGetScratch ~/.nuget ~/.config ~/.local &&     apt-get purge -y autoconf libtool make automake &&     apt-get clean
# Fri, 11 Dec 2020 21:21:14 GMT
WORKDIR /root
# Fri, 11 Dec 2020 21:21:14 GMT
CMD ["fsharpi"]
```

-	Layers:
	-	`sha256:dcd56748d94df613708f45494d30c45e8e94b1d61a697cbbf113327fac0d96a7`  
		Last Modified: Fri, 11 Dec 2020 02:12:59 GMT  
		Size: 30.2 MB (30159877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcad88aabd46d82f501c4aa9bb6e437cf2c4f331a74ceaf3f7f03856677fb804`  
		Last Modified: Fri, 11 Dec 2020 21:23:57 GMT  
		Size: 146.1 MB (146141324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `fsharp:4.1.34`

```console
$ docker pull fsharp@sha256:105e5bf54200e8793d42ccd760d826448ab791a0b53142f6aaa3a58c83baffa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `fsharp:4.1.34` - linux; amd64

```console
$ docker pull fsharp@sha256:9c410159ef06d0a9eb866da569d80177d53c57b094230348087beb8880a153a7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.3 MB (176301201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3231a9abdfffb5e4094c783908cb611f953eef65d48156b73aaf3301670bc3ba`
-	Default Command: `["fsharpi"]`

```dockerfile
# Fri, 11 Dec 2020 02:06:38 GMT
ADD file:af2b011a1bf144775df803945ea05c1f390e292cb2ee570501c61318d6df0618 in / 
# Fri, 11 Dec 2020 02:06:39 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 21:05:56 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Steve Desmond <steve@stevedesmond.ca>
# Fri, 11 Dec 2020 21:05:57 GMT
ENV MONO_THREADS_PER_CPU=50
# Fri, 11 Dec 2020 21:21:13 GMT
RUN MONO_VERSION=5.8.0.108 &&     FSHARP_VERSION=4.1.34 &&     FSHARP_PREFIX=/usr &&     FSHARP_GACDIR=/usr/lib/mono/gac &&     FSHARP_BASENAME=fsharp-$FSHARP_VERSION &&     FSHARP_ARCHIVE=$FSHARP_VERSION.tar.gz &&     FSHARP_ARCHIVE_URL=https://github.com/fsharp/fsharp/archive/$FSHARP_VERSION.tar.gz &&     apt-key adv --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF &&     echo "deb http://download.mono-project.com/repo/debian jessie/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official.list &&     apt-get update -y &&     apt-get --no-install-recommends install -y autoconf libtool pkg-config make automake nuget mono-devel msbuild ca-certificates-mono &&     rm -rf /var/lib/apt/lists/* &&     mkdir -p /tmp/src &&     cd /tmp/src &&     printf "namespace a { class b { public static void Main(string[] args) { new System.Net.WebClient().DownloadFile(\"%s\", \"%s\");}}}" $FSHARP_ARCHIVE_URL $FSHARP_ARCHIVE > download-fsharp.cs &&     mcs download-fsharp.cs && mono download-fsharp.exe && rm download-fsharp.exe download-fsharp.cs &&     tar xf $FSHARP_ARCHIVE &&     cd $FSHARP_BASENAME &&     ./autogen.sh --prefix=$FSHARP_PREFIX --with-gacdir=$FSHARP_GACDIR &&     make &&     make install &&     cd ~ &&     rm -rf /tmp/src /tmp/NuGetScratch ~/.nuget ~/.config ~/.local &&     apt-get purge -y autoconf libtool make automake &&     apt-get clean
# Fri, 11 Dec 2020 21:21:14 GMT
WORKDIR /root
# Fri, 11 Dec 2020 21:21:14 GMT
CMD ["fsharpi"]
```

-	Layers:
	-	`sha256:dcd56748d94df613708f45494d30c45e8e94b1d61a697cbbf113327fac0d96a7`  
		Last Modified: Fri, 11 Dec 2020 02:12:59 GMT  
		Size: 30.2 MB (30159877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcad88aabd46d82f501c4aa9bb6e437cf2c4f331a74ceaf3f7f03856677fb804`  
		Last Modified: Fri, 11 Dec 2020 21:23:57 GMT  
		Size: 146.1 MB (146141324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `fsharp:latest`

```console
$ docker pull fsharp@sha256:4cc2ce49d433271ad3ec56129386dced09643d7c7f035461212c0e1a03772818
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `fsharp:latest` - linux; amd64

```console
$ docker pull fsharp@sha256:aade83420e7ffa1d331e0b7d6ea8a79d6669b3e40406a2ee69762cc95adc9a47
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.6 MB (187596612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:565b414f7f0e6e90b91f8303481bd43940b8d88674d515dae9a67adf1cb51946`
-	Default Command: `["fsharpi"]`

```dockerfile
# Fri, 11 Dec 2020 02:06:10 GMT
ADD file:3a7bff4e139bcacc5831fd70a035c130a91b5da001dd91c08b2acd635c7064e8 in / 
# Fri, 11 Dec 2020 02:06:10 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 20:53:28 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Steve Desmond <steve@stevedesmond.ca>
# Fri, 11 Dec 2020 20:53:29 GMT
ENV MONO_THREADS_PER_CPU=50
# Fri, 11 Dec 2020 21:05:44 GMT
RUN MONO_VERSION=6.10.0.104 &&     FSHARP_VERSION=10.2.3 &&     FSHARP_BASENAME=fsharp-$FSHARP_VERSION &&     FSHARP_ARCHIVE=$FSHARP_VERSION.tar.gz &&     FSHARP_ARCHIVE_URL=https://github.com/fsharp/fsharp/archive/$FSHARP_VERSION.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     apt-get update && apt-get --no-install-recommends install -y gnupg dirmngr ca-certificates apt-transport-https &&     apt-key adv --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF &&     echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" | tee /etc/apt/sources.list.d/mono-official-stable.list &&     apt-get update -y &&     apt-get --no-install-recommends install -y pkg-config make nuget mono-devel msbuild ca-certificates-mono locales &&     rm -rf /var/lib/apt/lists/* &&     echo 'en_US.UTF-8 UTF-8' > /etc/locale.gen && /usr/sbin/locale-gen &&     mkdir -p /tmp/src &&     cd /tmp/src &&     printf "namespace a { class b { public static void Main(string[] args) { new System.Net.WebClient().DownloadFile(\"%s\", \"%s\");}}}" $FSHARP_ARCHIVE_URL $FSHARP_ARCHIVE > download-fsharp.cs &&     mcs download-fsharp.cs && mono download-fsharp.exe && rm download-fsharp.exe download-fsharp.cs &&     tar xf $FSHARP_ARCHIVE &&     cd $FSHARP_BASENAME &&     make &&     make install &&     cd ~ &&     rm -rf /tmp/src /tmp/NuGetScratch ~/.nuget ~/.config ~/.local "$GNUPGHOME" &&     apt-get purge -y make gnupg dirmngr &&     apt-get clean
# Fri, 11 Dec 2020 21:05:44 GMT
WORKDIR /root
# Fri, 11 Dec 2020 21:05:45 GMT
CMD ["fsharpi"]
```

-	Layers:
	-	`sha256:6ec7b7d162b24bd6df88abde89ceb6d7bbc2be927f025c9dd061af2b0c328cfe`  
		Last Modified: Fri, 11 Dec 2020 02:12:26 GMT  
		Size: 27.1 MB (27099295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:592b66fc0e6146332225bd3c9209957573ade3841386d2e76930121562261c53`  
		Last Modified: Fri, 11 Dec 2020 21:23:15 GMT  
		Size: 160.5 MB (160497317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fsharp:latest` - linux; arm64 variant v8

```console
$ docker pull fsharp@sha256:92dd3ad7cf2e30413a8e4a6531c320ad72caaded363414cf7d9cd1ae4679d624
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.6 MB (184638587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99b435785b824a1e25bb1ce7ab1313c1b188dbd3563077aa34f157816e8f6ba6`
-	Default Command: `["fsharpi"]`

```dockerfile
# Fri, 11 Dec 2020 02:45:53 GMT
ADD file:a5a2f039c00bc638b88cefdff4c3cd1865b4d415bf80c4fe6b496d975af7cc1f in / 
# Fri, 11 Dec 2020 02:45:57 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 18:29:06 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Steve Desmond <steve@stevedesmond.ca>
# Fri, 11 Dec 2020 18:29:06 GMT
ENV MONO_THREADS_PER_CPU=50
# Fri, 11 Dec 2020 18:45:47 GMT
RUN MONO_VERSION=6.10.0.104 &&     FSHARP_VERSION=10.2.3 &&     FSHARP_BASENAME=fsharp-$FSHARP_VERSION &&     FSHARP_ARCHIVE=$FSHARP_VERSION.tar.gz &&     FSHARP_ARCHIVE_URL=https://github.com/fsharp/fsharp/archive/$FSHARP_VERSION.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     apt-get update && apt-get --no-install-recommends install -y gnupg dirmngr ca-certificates apt-transport-https &&     apt-key adv --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF &&     echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" | tee /etc/apt/sources.list.d/mono-official-stable.list &&     apt-get update -y &&     apt-get --no-install-recommends install -y pkg-config make nuget mono-devel msbuild ca-certificates-mono locales &&     rm -rf /var/lib/apt/lists/* &&     echo 'en_US.UTF-8 UTF-8' > /etc/locale.gen && /usr/sbin/locale-gen &&     mkdir -p /tmp/src &&     cd /tmp/src &&     printf "namespace a { class b { public static void Main(string[] args) { new System.Net.WebClient().DownloadFile(\"%s\", \"%s\");}}}" $FSHARP_ARCHIVE_URL $FSHARP_ARCHIVE > download-fsharp.cs &&     mcs download-fsharp.cs && mono download-fsharp.exe && rm download-fsharp.exe download-fsharp.cs &&     tar xf $FSHARP_ARCHIVE &&     cd $FSHARP_BASENAME &&     make &&     make install &&     cd ~ &&     rm -rf /tmp/src /tmp/NuGetScratch ~/.nuget ~/.config ~/.local "$GNUPGHOME" &&     apt-get purge -y make gnupg dirmngr &&     apt-get clean
# Fri, 11 Dec 2020 18:45:50 GMT
WORKDIR /root
# Fri, 11 Dec 2020 18:45:51 GMT
CMD ["fsharpi"]
```

-	Layers:
	-	`sha256:c9648d7fcbb6d597cf33916d8fcd207fde8ec05d764b4480d4f3e884e142a902`  
		Last Modified: Fri, 11 Dec 2020 02:53:14 GMT  
		Size: 25.9 MB (25856191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faaa9119f12b1196aa197a9a420cd83a697f01ae5773a1a4a989e5aeb3d57686`  
		Last Modified: Fri, 11 Dec 2020 18:46:51 GMT  
		Size: 158.8 MB (158782396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `fsharp:netcore`

```console
$ docker pull fsharp@sha256:28e56ee182f526797442189b0f7db5d00a9f45e14d9258861068e3a7dda59b4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `fsharp:netcore` - linux; amd64

```console
$ docker pull fsharp@sha256:01d52abb34297b6148e22dcf4b9aa76be8c98efb697bc7753caa9d5af34f7d7c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.9 MB (332924118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c5549b0f5f12fa7c92ee3b7426c78f09bc2ef3c767d66d1b8a85cf4d249ff83`
-	Default Command: `["dotnet","fsi"]`

```dockerfile
# Fri, 11 Dec 2020 02:06:10 GMT
ADD file:3a7bff4e139bcacc5831fd70a035c130a91b5da001dd91c08b2acd635c7064e8 in / 
# Fri, 11 Dec 2020 02:06:10 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 20:53:28 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Steve Desmond <steve@stevedesmond.ca>
# Fri, 11 Dec 2020 20:53:29 GMT
ENV MONO_THREADS_PER_CPU=50
# Fri, 11 Dec 2020 21:05:44 GMT
RUN MONO_VERSION=6.10.0.104 &&     FSHARP_VERSION=10.2.3 &&     FSHARP_BASENAME=fsharp-$FSHARP_VERSION &&     FSHARP_ARCHIVE=$FSHARP_VERSION.tar.gz &&     FSHARP_ARCHIVE_URL=https://github.com/fsharp/fsharp/archive/$FSHARP_VERSION.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     apt-get update && apt-get --no-install-recommends install -y gnupg dirmngr ca-certificates apt-transport-https &&     apt-key adv --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF &&     echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" | tee /etc/apt/sources.list.d/mono-official-stable.list &&     apt-get update -y &&     apt-get --no-install-recommends install -y pkg-config make nuget mono-devel msbuild ca-certificates-mono locales &&     rm -rf /var/lib/apt/lists/* &&     echo 'en_US.UTF-8 UTF-8' > /etc/locale.gen && /usr/sbin/locale-gen &&     mkdir -p /tmp/src &&     cd /tmp/src &&     printf "namespace a { class b { public static void Main(string[] args) { new System.Net.WebClient().DownloadFile(\"%s\", \"%s\");}}}" $FSHARP_ARCHIVE_URL $FSHARP_ARCHIVE > download-fsharp.cs &&     mcs download-fsharp.cs && mono download-fsharp.exe && rm download-fsharp.exe download-fsharp.cs &&     tar xf $FSHARP_ARCHIVE &&     cd $FSHARP_BASENAME &&     make &&     make install &&     cd ~ &&     rm -rf /tmp/src /tmp/NuGetScratch ~/.nuget ~/.config ~/.local "$GNUPGHOME" &&     apt-get purge -y make gnupg dirmngr &&     apt-get clean
# Fri, 11 Dec 2020 21:05:44 GMT
WORKDIR /root
# Fri, 11 Dec 2020 21:05:45 GMT
CMD ["fsharpi"]
# Fri, 11 Dec 2020 21:21:29 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Steve Desmond <steve@stevedesmond.ca>
# Fri, 11 Dec 2020 21:21:30 GMT
ENV FrameworkPathOverride=/usr/lib/mono/4.8-api/
# Fri, 11 Dec 2020 21:21:30 GMT
ENV NUGET_XMLDOC_MODE=skip DOTNET_RUNNING_IN_CONTAINER=true DOTNET_USE_POLLING_FILE_WATCHER=true
# Fri, 11 Dec 2020 21:21:46 GMT
RUN apt-get update &&     apt-get --no-install-recommends install -y     curl     libunwind8     gettext     apt-transport-https     libc6     libcurl4     libgcc1     libgssapi-krb5-2     libicu63     liblttng-ust0     libssl1.1     libstdc++6     libunwind8     libuuid1     zlib1g &&     rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 21:22:05 GMT
RUN DOTNET_SDK_VERSION=3.1.403 &&     DOTNET_SDK_DOWNLOAD_URL=https://dotnetcli.blob.core.windows.net/dotnet/Sdk/$DOTNET_SDK_VERSION/dotnet-sdk-$DOTNET_SDK_VERSION-linux-x64.tar.gz &&     DOTNET_SDK_DOWNLOAD_SHA=0a0319ee8e9042bf04b6e83211c2d6e44e40e604bff0a133ba0d246d08bff76ebd88918ab5e10e6f7f0d2b504ddeb65c0108c6539bc4fbc4f09e4af3937e88ea &&     curl -SL $DOTNET_SDK_DOWNLOAD_URL --output dotnet.tar.gz &&     echo "$DOTNET_SDK_DOWNLOAD_SHA dotnet.tar.gz" | sha512sum -c - &&     mkdir -p /usr/share/dotnet &&     tar -zxf dotnet.tar.gz -C /usr/share/dotnet &&     rm dotnet.tar.gz &&     ln -s /usr/share/dotnet/dotnet /usr/bin/dotnet
# Fri, 11 Dec 2020 21:22:08 GMT
RUN mkdir warmup &&     cd warmup &&     dotnet new &&     cd - &&     rm -rf warmup /tmp/NuGetScratch
# Fri, 11 Dec 2020 21:22:08 GMT
WORKDIR /root
# Fri, 11 Dec 2020 21:22:08 GMT
CMD ["dotnet" "fsi"]
```

-	Layers:
	-	`sha256:6ec7b7d162b24bd6df88abde89ceb6d7bbc2be927f025c9dd061af2b0c328cfe`  
		Last Modified: Fri, 11 Dec 2020 02:12:26 GMT  
		Size: 27.1 MB (27099295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:592b66fc0e6146332225bd3c9209957573ade3841386d2e76930121562261c53`  
		Last Modified: Fri, 11 Dec 2020 21:23:15 GMT  
		Size: 160.5 MB (160497317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f30a41990d8aadbf81e4422ef3715f0985f735ca6bcbdeb016e6d5db760fc005`  
		Last Modified: Fri, 11 Dec 2020 21:24:09 GMT  
		Size: 17.2 MB (17205406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e30c25efa90ffeeb491d709a2e0e7da78bab948e0a1f44cf069e665dc646bbc`  
		Last Modified: Fri, 11 Dec 2020 21:24:31 GMT  
		Size: 123.8 MB (123846235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed800c9c105ce424d66e6991a33c4ee02c4aaec21d38288362b356b9dcc34229`  
		Last Modified: Fri, 11 Dec 2020 21:24:06 GMT  
		Size: 4.3 MB (4275865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
