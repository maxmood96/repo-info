## `mono:slim`

```console
$ docker pull mono@sha256:ead596a192a26cde82229a4210f2407a78b25f36425a90add50cf9e0f86079d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:slim` - linux; amd64

```console
$ docker pull mono@sha256:65870f6becef922e545100a7d4c94141a33241a5201f76fd71e155ef9102a9cc
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.5 MB (94530202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97b845c6666af9fd4cadc13e1b03f8addc33c6892b33133395e1bd48b5318650`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 23 Jun 2021 00:20:40 GMT
ADD file:4903a19c327468b0e08e4f463cfc162c66b85b4618b5803d71365862f6302e0b in / 
# Wed, 23 Jun 2021 00:20:40 GMT
CMD ["bash"]
# Wed, 23 Jun 2021 06:53:38 GMT
ENV MONO_VERSION=6.12.0.107
# Wed, 23 Jun 2021 06:53:50 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 23 Jun 2021 06:54:14 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:b4d181a07f8025e00e0cb28f1cc14613da2ce26450b80c54aea537fa93cf3bda`  
		Last Modified: Wed, 23 Jun 2021 00:25:39 GMT  
		Size: 27.1 MB (27145851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b29842205e94c5d811f3b97626ea51cbea0154670040ce682ca4318dcdee726`  
		Last Modified: Wed, 23 Jun 2021 07:08:03 GMT  
		Size: 256.1 KB (256064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4c003560d37df00a9eff42a6a315ee9d745c823ccd604e3ee84c52d781db219`  
		Last Modified: Wed, 23 Jun 2021 07:08:18 GMT  
		Size: 67.1 MB (67128287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:c68c41ab2f1a21e451e1637993a3f7507bfc83f77684e4f3457bb6b68512e278
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51685758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc64cb0a70c475230abad5af0b1294d8f6e6fdeb9f6560f70232bf7aa8c83793`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 22 Jul 2021 00:50:06 GMT
ADD file:885454a996e63d5eb93f1f365a3be77a441f368d7f5a77a7fd1636edf5d0b8cd in / 
# Thu, 22 Jul 2021 00:50:07 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 06:29:21 GMT
ENV MONO_VERSION=6.12.0.107
# Thu, 22 Jul 2021 06:29:40 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 22 Jul 2021 06:30:34 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:2b96a0a1ddfe4fab89025b13e583392414251af73361434f28af076c3db77100`  
		Last Modified: Thu, 22 Jul 2021 01:02:11 GMT  
		Size: 24.9 MB (24879093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5629d3e8dbc3b856d838c9f71f50e76f9ff6836312e0268f1c52e18d9321be21`  
		Last Modified: Thu, 22 Jul 2021 06:40:11 GMT  
		Size: 256.0 KB (255989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61036cae96bfba635c19d52cb460db870eb76be49c109403a1f07a5e9ff59ccc`  
		Last Modified: Thu, 22 Jul 2021 06:40:25 GMT  
		Size: 26.6 MB (26550676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:8d2ee48fb4fa2ea218e6af5e9b3a78101d874bf172e4b3f46f5384dc42639cb7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48740042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef003a71508474768e47507cf00dca304aa3253441cec71dd3cf65297b98dfa6`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 22 Jul 2021 02:03:46 GMT
ADD file:8f466611d9ba85407e1768128a6a2a51886b78675a4775badb9d42e57c4a182e in / 
# Thu, 22 Jul 2021 02:03:47 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 08:41:24 GMT
ENV MONO_VERSION=6.12.0.107
# Thu, 22 Jul 2021 08:41:41 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 22 Jul 2021 08:42:30 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:607f77084e8a15bf45d56215b058a593cdcf4e0039e5326157954b12663c0d31`  
		Last Modified: Thu, 22 Jul 2021 02:16:17 GMT  
		Size: 22.7 MB (22745974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f14ae55244daffd4eb3637bd099580d405a5483c05316160294b7199b4a2689`  
		Last Modified: Thu, 22 Jul 2021 08:51:27 GMT  
		Size: 256.0 KB (256001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70d2b04713203bdbf029bb5a3d5af7c6059dcb949a3e6b4bb95df0fbe1416292`  
		Last Modified: Thu, 22 Jul 2021 08:51:44 GMT  
		Size: 25.7 MB (25738067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:bfa9690ddff5634fa376e7a4be397f9be92de6cd468c1c4ee6a8c34e46477c75
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.9 MB (57939883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f5566d0a69b586e5b1087c0b0c5eb46ea9f998876f5c2acaf0bfef893856b51`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 22 Jul 2021 00:40:14 GMT
ADD file:074ffc2065bab83c9a5c596576656b04d271dd78406aadad160b68e38f38269f in / 
# Thu, 22 Jul 2021 00:40:14 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 04:37:38 GMT
ENV MONO_VERSION=6.12.0.107
# Thu, 22 Jul 2021 04:37:45 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 22 Jul 2021 04:38:08 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:513c6babab2b9079da61a69300c0e26d1037ca98910376098e9ae87baeb112c0`  
		Last Modified: Thu, 22 Jul 2021 00:45:53 GMT  
		Size: 25.9 MB (25914794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f3c7ec9b3b27a755074c4b9f18bbc7ce2af31ae06e879defa123c3ad421f51b`  
		Last Modified: Thu, 22 Jul 2021 04:43:22 GMT  
		Size: 255.9 KB (255893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35ac245314198d71730d8e3be57f875a2953864a7e0374398d5e3a83bccabe2c`  
		Last Modified: Thu, 22 Jul 2021 04:43:28 GMT  
		Size: 31.8 MB (31769196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:slim` - linux; 386

```console
$ docker pull mono@sha256:a72675568da344f506fc5a5f530fda433972657a65d12815d0f26cfde809eda5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.2 MB (99206669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91f4b8d95c8a1553ce45ca4a7413c69333bf3cc5849bf4a1502f892d8df80cec`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 22 Jul 2021 00:39:50 GMT
ADD file:cb657a3d01f25bf815677ce223e8802d054f11aeb95f85b160982277916637bd in / 
# Thu, 22 Jul 2021 00:39:51 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 04:58:11 GMT
ENV MONO_VERSION=6.12.0.107
# Thu, 22 Jul 2021 04:58:19 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 22 Jul 2021 04:58:55 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:fa9d06db5f4195bd51665a89e08e2e7db25636ac28ab162fe876ae0a53093fe5`  
		Last Modified: Thu, 22 Jul 2021 00:46:36 GMT  
		Size: 27.8 MB (27797459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0a4d03527d058620f221cc87eaeb48b8c7ac81f94ed4922cf45eb3b660709b8`  
		Last Modified: Thu, 22 Jul 2021 05:04:50 GMT  
		Size: 256.0 KB (255966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8da2f3ee756552b30842fb2ee7a830400e077210a06d9849698fce3a993b8ff0`  
		Last Modified: Thu, 22 Jul 2021 05:05:09 GMT  
		Size: 71.2 MB (71153244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:slim` - linux; ppc64le

```console
$ docker pull mono@sha256:80109d48a2ac23f85fb9339217b0e3818680744d5d6455d40d84d15f87106d18
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60168058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62d9ad11b542f78aefec089ebbe5cb44745f32a26e68476292ec35b45b04c2b8`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 22 Jul 2021 00:19:04 GMT
ADD file:3a6bd6ce3eff98b88a13de5d0f26cff0b026f876674204dbad6f84fafcf145b1 in / 
# Thu, 22 Jul 2021 00:19:13 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 08:16:54 GMT
ENV MONO_VERSION=6.12.0.107
# Thu, 22 Jul 2021 08:20:13 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 22 Jul 2021 08:21:35 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:1130517d52da84a09f9465006bddab5e49afd398860890eab6274fd0bff32371`  
		Last Modified: Thu, 22 Jul 2021 00:27:49 GMT  
		Size: 30.6 MB (30553709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fde06615d835963941491be7d6247a658cef9ed8469d4832be20518178765cf`  
		Last Modified: Thu, 22 Jul 2021 08:46:25 GMT  
		Size: 256.3 KB (256256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17257934790bc3f01bb0d65cf61b5f17c6e10ca880c4b9403523269f2d40f09c`  
		Last Modified: Thu, 22 Jul 2021 08:46:32 GMT  
		Size: 29.4 MB (29358093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
