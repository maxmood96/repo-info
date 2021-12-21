## `mono:6-slim`

```console
$ docker pull mono@sha256:4b58ceae2c0806c778c7b89c0456625d50554720cc8fcc2481021e6b692b38db
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
$ docker pull mono@sha256:b1f160c4960056a755f78c87acbe28ab65b2090c7ce0beba9a0a347d1b34a168
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.7 MB (94680923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f795cebdb9ba7d4af431453595977d286d08cda538a80f67ad5e72e6901cf51`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 01:23:04 GMT
ADD file:bd5c9e0e0145fe33beee9d73615cc89b5c5459bb84ea164cb1bbd8c999f0c2e4 in / 
# Tue, 21 Dec 2021 01:23:04 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 02:36:49 GMT
ENV MONO_VERSION=6.12.0.122
# Tue, 21 Dec 2021 02:37:06 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 21 Dec 2021 02:37:36 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:72a69066d2febc34d8f3dbcb645f7b851a57e9681322ece7ad8007503b783c19`  
		Last Modified: Tue, 21 Dec 2021 01:28:32 GMT  
		Size: 27.2 MB (27153723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8678af474ab209c6f77514a3e861bb6e382fdd4f519efa3c08708b70676f7714`  
		Last Modified: Tue, 21 Dec 2021 02:52:42 GMT  
		Size: 2.8 MB (2767125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad55ab33cb43c5e91426eb50f5804dfaa25e4ca85d8faef05dc9894b16af2148`  
		Last Modified: Tue, 21 Dec 2021 02:52:54 GMT  
		Size: 64.8 MB (64760075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:7a492665403e90271d5c3b662906813c65b7d7c3be9305d959f2bb81503e4d00
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51842123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:641ab77374480b3447a0627f55cdeb9f8d39f59fdf5ed7ce029dc87beee42cc3`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Dec 2021 02:51:44 GMT
ADD file:b509d9889433e2e1b4e7d30f6a1461c93f9c6a2a6f60e1802710cbc20e7a0e81 in / 
# Thu, 02 Dec 2021 02:51:46 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 04:57:23 GMT
ENV MONO_VERSION=6.12.0.122
# Thu, 02 Dec 2021 04:58:17 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 02 Dec 2021 04:59:21 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:6f8ed9eedee034be125ab31b8087fb60cf54bd4085e7e2dfbdc92ccae717fa06`  
		Last Modified: Thu, 02 Dec 2021 03:10:47 GMT  
		Size: 24.9 MB (24886215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caf042ad57da9cb94c54fcdd4dc859942a33b513f08500061993b7179f6ec8fd`  
		Last Modified: Thu, 02 Dec 2021 05:10:48 GMT  
		Size: 2.5 MB (2462625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64b3874211babf64b45d2e08178915f7e516b27c5ff49234a107d91a92d2e5aa`  
		Last Modified: Thu, 02 Dec 2021 05:10:58 GMT  
		Size: 24.5 MB (24493283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:3c63ba670d3b02c53ccb84db50bcc3d856532d456af2784173e3f5a2b21313a9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48899121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69ac8565cf40be82a89e16698fa13fc328912da6a5d596654664bded46853df2`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Dec 2021 09:06:21 GMT
ADD file:7b30d743b30e84b21888f23cb7f266caba09db98b7a4c8800abebcf03d28c01d in / 
# Thu, 02 Dec 2021 09:06:22 GMT
CMD ["bash"]
# Fri, 03 Dec 2021 07:30:59 GMT
ENV MONO_VERSION=6.12.0.122
# Fri, 03 Dec 2021 07:31:30 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 03 Dec 2021 07:32:13 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:2aa85085c98821a25a3058f7fc2c6427064f2228ea8eac904e9e7db4dbdaa01a`  
		Last Modified: Thu, 02 Dec 2021 09:22:26 GMT  
		Size: 22.8 MB (22754365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d589d994b7b2874fc4f15521e081541498cce1ac0f5b4445a505fdc375e9f4c`  
		Last Modified: Fri, 03 Dec 2021 07:41:37 GMT  
		Size: 2.4 MB (2361904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:756e9ce9a8da0f163934712336478a5a2499a4456d4782d2851fd3ff27673f42`  
		Last Modified: Fri, 03 Dec 2021 07:41:53 GMT  
		Size: 23.8 MB (23782852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:abd750b08116c7f7a3a04db0e669d49fcec322ff4724cce81fff8a58c101dec1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.9 MB (57876215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8985e0d0c74bb76657b4366297bf7ef10f1188897831bdbfc65ee14994ea211e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Dec 2021 08:08:34 GMT
ADD file:83d9e760a84be2bd8754e31e33b3f782b44f6e7b7e02c156f519715c88c40615 in / 
# Thu, 02 Dec 2021 08:08:35 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 10:31:32 GMT
ENV MONO_VERSION=6.12.0.122
# Thu, 02 Dec 2021 10:31:49 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 02 Dec 2021 10:32:05 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:2a37a2e6ba8cbf21e3950cf7b2455f0af054667b6a35719fb2bd6070973bfa76`  
		Last Modified: Thu, 02 Dec 2021 08:41:37 GMT  
		Size: 25.9 MB (25923144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9881b3a1bbaf2479f58c7e7e0a008ba9dfcfd9a404b8a45f61e67b19f8a2b493`  
		Last Modified: Thu, 02 Dec 2021 10:35:43 GMT  
		Size: 2.6 MB (2634639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5a63bac7bf077258f21a6462bb51b790fdfd8c75ff13922648615e0ecd2755c`  
		Last Modified: Thu, 02 Dec 2021 10:35:48 GMT  
		Size: 29.3 MB (29318432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6-slim` - linux; 386

```console
$ docker pull mono@sha256:9bb720a3e2fe2fac5af3d2868e8f635ab7de67622d1dcb87fcd9622e6e1ca5e1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.4 MB (99364470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d552f788d57a0cc6924c3f1df81c6577715d0788660292b50b4f80a15e3d9d6`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Dec 2021 02:40:25 GMT
ADD file:9063906ecf2b5c82bf37cb574e78f61add2cd7aa8d0675647be379e30e19b6a9 in / 
# Thu, 02 Dec 2021 02:40:25 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 14:55:37 GMT
ENV MONO_VERSION=6.12.0.122
# Thu, 02 Dec 2021 14:55:51 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 02 Dec 2021 14:56:21 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:3b938b4b72623e9d1494d498630cd883df97fd6882fb9e0edb7af6714fce4e83`  
		Last Modified: Thu, 02 Dec 2021 02:49:02 GMT  
		Size: 27.8 MB (27804562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33df0d561cd5f2e983795fefe65289181d4ec840095931cf18b11ff6c7bf28c2`  
		Last Modified: Thu, 02 Dec 2021 15:03:01 GMT  
		Size: 2.8 MB (2781457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d2ba8412a0fc14d63cab8249ab154c0f32239599e76bfd072203cc83b8a6bc4`  
		Last Modified: Thu, 02 Dec 2021 15:03:22 GMT  
		Size: 68.8 MB (68778451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:4477347cbd87acd14478a07fd821c4db13e06e7ad655d1fb1c8ff7baade212b1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60320852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf8007428e9c8975924b16eef8ba6a5e5f814d4cbf8a20ff1a067db84218929c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Dec 2021 07:22:12 GMT
ADD file:b9b5697bc2dd3ded7a158d973abc939cc5d197f1f0d9ff1fa8b3db3b7906de7a in / 
# Thu, 02 Dec 2021 07:22:18 GMT
CMD ["bash"]
# Fri, 03 Dec 2021 06:48:59 GMT
ENV MONO_VERSION=6.12.0.122
# Fri, 03 Dec 2021 06:50:18 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 03 Dec 2021 06:51:17 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:da5263f5d65ecaf2dcd9400908302b4c477c13afa707110e4d85b4b946e9a3ae`  
		Last Modified: Thu, 02 Dec 2021 07:32:41 GMT  
		Size: 30.6 MB (30562306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0548556c2a8c0921fc8a80efc22ff605dfaae8553c4352630e695132dcd243f9`  
		Last Modified: Fri, 03 Dec 2021 07:08:33 GMT  
		Size: 2.9 MB (2884574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e15713b5382b49b2c5005d764ebcb5f12fb5822bb238768c131e5ec1465aa6f`  
		Last Modified: Fri, 03 Dec 2021 07:08:38 GMT  
		Size: 26.9 MB (26873972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
