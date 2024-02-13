## `mono:latest`

```console
$ docker pull mono@sha256:85c1db20f347a8a7b7c5771eed11f664dcc92143d842ef28b97ff422262a2a89
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
$ docker pull mono@sha256:24835daedbec7f1497e229da89538b3ad495236c9a3741149b20a965e2693f90
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.7 MB (254676208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cdb9da9adb34e859e192946189bf53729545b6a7cf609dd22dbfd2bfe0026ba`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:36:03 GMT
ADD file:a857ebb18123e76fc79a7d720dfdcc496ba12a79af323564b965627d399a5b04 in / 
# Wed, 31 Jan 2024 22:36:04 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 01:14:27 GMT
ENV MONO_VERSION=6.12.0.182
# Thu, 01 Feb 2024 01:14:37 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 01 Feb 2024 01:14:58 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 01 Feb 2024 01:16:43 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:b992ca815489079dcc6d19cf381c63d057e1b924edd453734f694be5ee23dfd9`  
		Last Modified: Wed, 31 Jan 2024 22:41:30 GMT  
		Size: 27.2 MB (27188593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d22fee0d29d553ce201329aaea2dc449252f35fe06d90618fe25d7fb34c5d9e1`  
		Last Modified: Thu, 01 Feb 2024 01:21:51 GMT  
		Size: 2.8 MB (2781001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ea84e4c56c4974fbb3cf7f2c89620bde22b27cfa41fb763e7cf2f2ab5a41f9c`  
		Last Modified: Thu, 01 Feb 2024 01:22:00 GMT  
		Size: 64.8 MB (64774023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31faf9977ea6e24126e6587319618044af8455c477b3368994cc0d5a7208ffba`  
		Last Modified: Thu, 01 Feb 2024 01:22:58 GMT  
		Size: 159.9 MB (159932591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:latest` - linux; arm variant v5

```console
$ docker pull mono@sha256:dea4d3a6cf8d83cd0b747ac36b0b7a279de919c38227c259e8f0dd933ad99d3d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.9 MB (192868079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52646a30a3e2966b0a92b143b872a725a0eaa3c003a2b6c3030454d2f5f26220`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 00:49:37 GMT
ADD file:2ed7ca0d45c68b46a10ae186e8a03f98e72cadfeed17105668f53adf14d31e1f in / 
# Tue, 02 Aug 2022 00:49:38 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 07:17:55 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 01 Mar 2023 07:18:17 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 01 Mar 2023 07:18:42 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 01 Mar 2023 07:20:53 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:187ecffbd1e0eae5de6567dff32bd58f28623635657779760c9d9539d6b7cc59`  
		Last Modified: Tue, 02 Aug 2022 00:57:06 GMT  
		Size: 24.9 MB (24889750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6702eef9c7d9ec6ede2c5f9a15a047b314ccc9140f25694f337c0127478bb25b`  
		Last Modified: Wed, 01 Mar 2023 07:23:12 GMT  
		Size: 2.5 MB (2467715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3781ed66d8db4f1e7c7b6323f62af11c65550a10f339ad7c0fb68f9467f8026d`  
		Last Modified: Wed, 01 Mar 2023 07:23:17 GMT  
		Size: 24.5 MB (24503499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f32f45a77bbef0505ff02ad954c1ce25d1cb8f5b668bbd7c73fa538966d0c0b`  
		Last Modified: Wed, 01 Mar 2023 07:24:21 GMT  
		Size: 141.0 MB (141007115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:latest` - linux; arm variant v7

```console
$ docker pull mono@sha256:3e2de0c728b5aefd276bcbf8c438ac36581e43f5c198b332e8f58ef985983a19
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.0 MB (189020647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be7763682d74a2c876385b44ce6249bab6e70e67516371f6945836c224c42df2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:21:12 GMT
ADD file:3bb84527315f3c157a6224d42c0b9c078d85e8977d02365719d3fa69b9b7544b in / 
# Tue, 13 Feb 2024 01:21:13 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 02:41:27 GMT
ENV MONO_VERSION=6.12.0.182
# Tue, 13 Feb 2024 02:41:49 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 13 Feb 2024 02:42:22 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 13 Feb 2024 02:45:03 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:1190235a63a2fd50345e786cc24ebcb4ae4619484192480a44a203616017624f`  
		Last Modified: Tue, 13 Feb 2024 01:28:25 GMT  
		Size: 22.8 MB (22795757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ea68bf41cd27db26661ba886fe9c5464b3855d5265d4ff4ca0b4930efd29a99`  
		Last Modified: Tue, 13 Feb 2024 02:47:53 GMT  
		Size: 2.4 MB (2370846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54638cd0153cd25eb38134f629e890f7d70f170d4136fb1ec6c6ac4b0411ba44`  
		Last Modified: Tue, 13 Feb 2024 02:47:59 GMT  
		Size: 23.8 MB (23790775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b56eaa62c87ba3a5b91da35675d3dba1b02f06225453b9129957501afd0c9c`  
		Last Modified: Tue, 13 Feb 2024 02:48:59 GMT  
		Size: 140.1 MB (140063269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:latest` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:f7348b7bce5bea251235c5a3e985046a502a9ffdbf7189edf083af19da95afae
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.4 MB (216408601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbde375b928394c00c43f559660d7511c98c48711972319d358d64b25cf3f4ca`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:56 GMT
ADD file:de90e50e142aa92c29d5128e1cd025fd5c5b91f879a19a06a8b49451a4e6afb9 in / 
# Wed, 31 Jan 2024 22:44:57 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 07:23:59 GMT
ENV MONO_VERSION=6.12.0.182
# Thu, 01 Feb 2024 07:24:07 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 01 Feb 2024 07:24:21 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 01 Feb 2024 07:25:43 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:42641f7bf1512c205041cf7899e52e2185e49bcd6cfa0cb8ebfc73e3009221b7`  
		Last Modified: Wed, 31 Jan 2024 22:49:34 GMT  
		Size: 26.0 MB (25970227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d23db6d7a349c8c323fcaf6aed87c7173ab657ae5a2f5b8c11ee9c8c6d93c81`  
		Last Modified: Thu, 01 Feb 2024 07:27:00 GMT  
		Size: 2.6 MB (2645831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de6d03e6166699786dffd4edb593ec218c39146d2f7711cc7f152a1d69a718e1`  
		Last Modified: Thu, 01 Feb 2024 07:27:03 GMT  
		Size: 29.5 MB (29545178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:331e508c87b20f269dd276e4ac1a92896f34ed0899123a136bbb5cd3728fb56b`  
		Last Modified: Thu, 01 Feb 2024 07:27:53 GMT  
		Size: 158.2 MB (158247365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:latest` - linux; 386

```console
$ docker pull mono@sha256:d1283e1e40b3629d6b295548ffd79b657cb8ace99e1f27b0ef1530fc2fc5f4f9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.6 MB (259559004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2647d4dd269d9a7626bce411c0ae83e295e5451e288a3e4733c4be6db07e8cac`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:39:40 GMT
ADD file:3ff71d8500563a5fdf27e800f24879e0da378a12b7855b0b22093604455859ae in / 
# Tue, 13 Feb 2024 00:39:41 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 04:42:50 GMT
ENV MONO_VERSION=6.12.0.182
# Tue, 13 Feb 2024 04:43:03 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 13 Feb 2024 04:43:37 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 13 Feb 2024 04:45:58 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:157da6991ef444d47f503ec5cd3d6e3043ba6dca39090f157c423c1f8097d0ac`  
		Last Modified: Tue, 13 Feb 2024 00:45:25 GMT  
		Size: 27.8 MB (27846861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:007a514eb3f05ec68786ccc04f84fec3f7edd1c40f2813b222a9c817a6cf9685`  
		Last Modified: Tue, 13 Feb 2024 04:48:35 GMT  
		Size: 2.8 MB (2792538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81fb7926c38069022c10fe01395ffa888d1ac955a4cfada1cf78e55280204c29`  
		Last Modified: Tue, 13 Feb 2024 04:48:49 GMT  
		Size: 68.8 MB (68800556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d409f71415e2e5c19d456463cc900b4901bcc780664861030e945348f2fafd0`  
		Last Modified: Tue, 13 Feb 2024 04:50:06 GMT  
		Size: 160.1 MB (160119049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:latest` - linux; ppc64le

```console
$ docker pull mono@sha256:fbfb5b60906856f25cc0ffb3ed273fa5da089aed24eab6afb049cc150c221768
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.7 MB (221654331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45a10e5a16545c25df57d5cf1f034acbb78fb5a3c968378416dc576fa88386ef`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:04 GMT
ADD file:6d33ba25d3625e5f445fc2183b60c64e2cbc780cb541d7f8ac76ce193b311d13 in / 
# Tue, 02 Aug 2022 01:18:06 GMT
CMD ["bash"]
# Wed, 03 Aug 2022 02:07:46 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 03 Aug 2022 02:08:06 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 03 Aug 2022 02:08:41 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 03 Aug 2022 02:11:40 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:fc8842eebb7ccaf249b2bb2d6a3878fffdae26c9db8f23b393c7f76a6249d2f6`  
		Last Modified: Tue, 02 Aug 2022 01:25:45 GMT  
		Size: 30.6 MB (30560308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1100971c8a3b3eb42c6e22a4c25f405143f007bda60d16697d49b333925b4d84`  
		Last Modified: Wed, 03 Aug 2022 02:15:13 GMT  
		Size: 2.9 MB (2892658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:390f883f1594b5d2d40b7ba4dc50f375439dd1611f38f0c3d071a38bf2ac62cd`  
		Last Modified: Wed, 03 Aug 2022 02:15:27 GMT  
		Size: 41.9 MB (41897345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ae94af697c95b6bf75033b813f19ec72f68da49a681d5ce7078753923129147`  
		Last Modified: Wed, 03 Aug 2022 02:16:58 GMT  
		Size: 146.3 MB (146304020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
