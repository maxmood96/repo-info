## `mono:6-slim`

```console
$ docker pull mono@sha256:fa044316df475b097233ec9ee3188a3982ae6c8159b6b2489437abe337796ac2
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
$ docker pull mono@sha256:34cde2feaeec304a4f2b1ddd3d1b755035776d57c2eff7af6c0bfe7d0ce0a148
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.5 MB (94530536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d28e9dd0a08d41adc2be8de6bc0bdffc1bc0283f7d8d4b57d6bf4872e3a207c6`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Sep 2021 01:21:46 GMT
ADD file:4ff85d9f6aa246746912db62dea02eb71750474bb29611e770516a1fcd217add in / 
# Fri, 03 Sep 2021 01:21:46 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 07:06:49 GMT
ENV MONO_VERSION=6.12.0.107
# Fri, 03 Sep 2021 07:07:01 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 03 Sep 2021 07:07:36 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a330b6cecb98cd2425fd25fce36669073f593b3176b4ee14731e48c05d678cdd`  
		Last Modified: Fri, 03 Sep 2021 01:28:19 GMT  
		Size: 27.1 MB (27145844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7754c8c88d417ee3d657ef6008443c143d0566aa7b208ee11ccfe808f566a3a`  
		Last Modified: Fri, 03 Sep 2021 07:21:25 GMT  
		Size: 256.1 KB (256063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fa0313e284cae6bee7d0627451dafbb8e42045c19e74be7d2fb2699cf321b17`  
		Last Modified: Fri, 03 Sep 2021 07:21:39 GMT  
		Size: 67.1 MB (67128629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:fe5fd5427cba76e9864da89184c9acbdbb505e49730e23170f60a077c4bbf13d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51686355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4b7d30fe3166b1a1be07f2ab3bd6c6c34caa4e31c72cd40624ec9f3031815a1`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Sep 2021 00:51:26 GMT
ADD file:350748a564076da397b991745cd42e0688d15c72b9fd5c81f8ea0bb8938a2b3d in / 
# Fri, 03 Sep 2021 00:51:27 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 03:04:06 GMT
ENV MONO_VERSION=6.12.0.107
# Fri, 03 Sep 2021 03:04:29 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 03 Sep 2021 03:05:22 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:b019db4b5197128481d48d92ecacd6bb356c027a3d08393f6567a6fa183ba769`  
		Last Modified: Fri, 03 Sep 2021 01:07:12 GMT  
		Size: 24.9 MB (24879114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:828064d1142810d6abe00b2e08d14bbf4420ee169359b192d08b40d8aae10e5f`  
		Last Modified: Fri, 03 Sep 2021 03:14:59 GMT  
		Size: 256.0 KB (255970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2c465dd0ac4c8ce158165e98366d0ba4306a911e1b2d2bd390d257461e51a3c`  
		Last Modified: Fri, 03 Sep 2021 03:15:19 GMT  
		Size: 26.6 MB (26551271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:2c2cfd1988c13d32f9b0ad2ceb4d88421a5b877b3f5f86dc99f4dfc6a936c1a1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48739856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c59e8321cabd2c937293ef6752fba1bbca466979018d57651dd08e3404ac03e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Sep 2021 01:00:40 GMT
ADD file:4754bbccf4c59f77dd54f3888871f0635a2f9655cda53f50e63237f1580286e0 in / 
# Fri, 03 Sep 2021 01:00:41 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 07:13:29 GMT
ENV MONO_VERSION=6.12.0.107
# Fri, 03 Sep 2021 07:13:48 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 03 Sep 2021 07:14:37 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:2215ad7863d95c38f1f794f1d5b4d6c5ca4ca7e921e4bb7218b803f7ed270675`  
		Last Modified: Fri, 03 Sep 2021 01:16:23 GMT  
		Size: 22.7 MB (22746151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aaa844351522fac27215e39f522d477371158e68add695f3fa0d3e3eb7a405c`  
		Last Modified: Fri, 03 Sep 2021 07:23:37 GMT  
		Size: 256.0 KB (255951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9d985c8447020bf59910488f403f842aa681c83349963f713e2552b54cc1559`  
		Last Modified: Fri, 03 Sep 2021 07:23:56 GMT  
		Size: 25.7 MB (25737754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:f3721cf677ee4fe6eeb9c757e7e0bf0faebbfdfe5942c6f515b0cf1e45372425
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.9 MB (57940907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20f450d60fb7b5103dad6aa7b14ae87b78da88df0a7cf341bed22d676b455e95`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 28 Sep 2021 01:41:13 GMT
ADD file:3e2426765cfe2b896fc847bcb435624930753c72ac00b87d2c73f4a81c813fd4 in / 
# Tue, 28 Sep 2021 01:41:13 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 04:53:28 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 28 Sep 2021 04:53:43 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 28 Sep 2021 04:54:06 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:896f18f54b28590b15a0f3354b13e8ea2f88a05f13de4117720f88cef30206ee`  
		Last Modified: Tue, 28 Sep 2021 01:49:22 GMT  
		Size: 25.9 MB (25915039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b751b21d089e680f6da69f7b8eba65cfd34ec336fdc51580b3847b39965ef9a`  
		Last Modified: Tue, 28 Sep 2021 04:59:58 GMT  
		Size: 255.9 KB (255923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2601a6dd7d5beaad12a0519f8ba90c7df66acb8a5dc81279c35fe6162d50a4e6`  
		Last Modified: Tue, 28 Sep 2021 05:00:04 GMT  
		Size: 31.8 MB (31769945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6-slim` - linux; 386

```console
$ docker pull mono@sha256:bb507f350d5b23f031a40cbda844ce0e87213eacc263de8b097cea1afed2d2ad
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.2 MB (99207389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7da82a0c34ced1fc2c4f41d51436233401c6bb1adf2dd81a545f44e1cba32c5`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Sep 2021 00:40:24 GMT
ADD file:6bf4b6f4aa28306610ef10c68f422a7210ff2fbd5345cec07bc5f76d54a4c8bc in / 
# Fri, 03 Sep 2021 00:40:24 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 16:39:29 GMT
ENV MONO_VERSION=6.12.0.107
# Fri, 03 Sep 2021 16:39:38 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 03 Sep 2021 16:40:17 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7e87f600658a0c0d3bd8b82b9c645b5ec2763492ec627c1c1c1183c2ad3c45d5`  
		Last Modified: Fri, 03 Sep 2021 00:49:06 GMT  
		Size: 27.8 MB (27797513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71a38d4287cb185a3e4f657850afc6baf9f74a793e476eb7f45c16ef6196a03f`  
		Last Modified: Fri, 03 Sep 2021 16:45:20 GMT  
		Size: 255.9 KB (255946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9afd479d86a82ef00c0de5471e1b1e4bf441b20817bf32bf99083a37dcb3c47`  
		Last Modified: Fri, 03 Sep 2021 16:45:34 GMT  
		Size: 71.2 MB (71153930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:246b89a98ed402f68e362e5071d08884b53e4a6e66a0594ba58a2f7fcb27764a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60170004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f4e719554a822c0a6e8d0da2a4d9711f875e416cb9993bc0e3adf300c33d822`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Sep 2021 01:24:33 GMT
ADD file:6c1662ddb92232ae8969a86a18dacab97b3b5792a1ecda49e6ac741a1a5c878c in / 
# Fri, 03 Sep 2021 01:24:41 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 08:23:08 GMT
ENV MONO_VERSION=6.12.0.107
# Fri, 03 Sep 2021 08:25:01 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 03 Sep 2021 08:26:36 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:8258146296247df1f308a336d4abf286afae14e3375edefb87a091e80745e29f`  
		Last Modified: Fri, 03 Sep 2021 01:39:45 GMT  
		Size: 30.6 MB (30553675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e16fcd88e98a8c542138e173bd2d3a18fbf8dd3cda3b870b754928dabcc051ad`  
		Last Modified: Fri, 03 Sep 2021 08:45:34 GMT  
		Size: 256.1 KB (256149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d0042f91bcb537d4c7e2f158954a705080702b91cc826701626dc0375b741ab`  
		Last Modified: Fri, 03 Sep 2021 08:45:40 GMT  
		Size: 29.4 MB (29360180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
