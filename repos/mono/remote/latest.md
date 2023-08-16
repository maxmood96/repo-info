## `mono:latest`

```console
$ docker pull mono@sha256:40c097a0ba4d51aceac77b5e767b027f0a7c06fd6029342dc890177c452839e2
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
$ docker pull mono@sha256:312c08a95ef6d46ef6e4c8fafdd00a3db2217a08a723b2522b34202587c4d022
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.7 MB (254674669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bdd38b14cfa4b2efc29dbdd11524b52dbce269382bba20486585d925feb75b4`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jul 2023 23:25:29 GMT
ADD file:20e7ad6bec617357895302b08431eb3430cce3113bdf0a8ff9827115f858d313 in / 
# Thu, 27 Jul 2023 23:25:30 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 02:09:38 GMT
ENV MONO_VERSION=6.12.0.182
# Fri, 28 Jul 2023 02:09:47 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 28 Jul 2023 02:10:14 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Fri, 28 Jul 2023 02:13:35 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:3240fe174df9a5a4923c4b52f1d887dd1ad1a9ee69245c1fb867f399167584dd`  
		Last Modified: Thu, 27 Jul 2023 23:30:49 GMT  
		Size: 27.2 MB (27187431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fe764ada48e9c07b599b90c63ebf3a1516f625cfe72cdf4ba823f1dfcd9e713`  
		Last Modified: Fri, 28 Jul 2023 02:20:05 GMT  
		Size: 2.8 MB (2780934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8209140f449ce8c93dde23e84011feda1a897dd0d7876f5cc4a254360ace6840`  
		Last Modified: Fri, 28 Jul 2023 02:20:14 GMT  
		Size: 64.8 MB (64774344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:271c2c4f0ae1503f76d16d77b0a241d5be0f7d669404ae4df1b6ae7ee4deb3ce`  
		Last Modified: Fri, 28 Jul 2023 02:21:14 GMT  
		Size: 159.9 MB (159931960 bytes)  
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
$ docker pull mono@sha256:32aaba69c65b0c72f986a13ae160390f8d6df601ba4fe3e32bb93cc006a600dc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.0 MB (189020763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a538f8d540bab3fb1f7c85666af7e424d3e41b1ff6792fd1caa35ef9cbf49bd7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 16 Aug 2023 00:17:52 GMT
ADD file:c676b622e67d7e8923f6eb310001d3118e7e31af842dd82f006d8900860f1f4e in / 
# Wed, 16 Aug 2023 00:17:52 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 07:42:49 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 16 Aug 2023 07:42:59 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 16 Aug 2023 07:43:23 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 16 Aug 2023 07:45:22 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:87da7f83f545c68a0ecbfd834e0fec4078d10fbcc8f3eee04eb7d85bddf5f41a`  
		Last Modified: Wed, 16 Aug 2023 00:22:48 GMT  
		Size: 22.8 MB (22795639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6006cfa0f7479024cdc10e6ba8d43b7122e40f58f9b78221176dbd6716c5e8b3`  
		Last Modified: Wed, 16 Aug 2023 07:47:52 GMT  
		Size: 2.4 MB (2370820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e267e25cd3dbcfa255411cf89544ec5a9a2c2b5b26277ff012463a197538335`  
		Last Modified: Wed, 16 Aug 2023 07:47:56 GMT  
		Size: 23.8 MB (23790816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8ea7ec467a28a5965ab6a076ec6cb6303179d6fbba0350ef242c0c2b364b036`  
		Last Modified: Wed, 16 Aug 2023 07:48:48 GMT  
		Size: 140.1 MB (140063488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:latest` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:591a5cd229dfb4339331dfc97771581207ef38d131d351fe76f7abaa8b6c4107
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.4 MB (216405080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ade8ea9371e554b9b7ffdb4ac2799f9688a60781f155d56563905b3d31254ba`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Aug 2023 23:40:25 GMT
ADD file:cc6c5417b68ddd7a05f4a3896e20ff80bbd9ae8951adb686823f4039db4eba9a in / 
# Tue, 15 Aug 2023 23:40:26 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 03:39:06 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 16 Aug 2023 03:39:14 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 16 Aug 2023 03:39:33 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 16 Aug 2023 03:41:58 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:5b18dd3a8fc62fc571f4c7e2207d4072601fe59c0a6d3d739f4fddbff7f0dae3`  
		Last Modified: Tue, 15 Aug 2023 23:44:37 GMT  
		Size: 26.0 MB (25967768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82139475d626a0187fb04e25d24838c8130c5d5c0eac8a3795057bf6f3803f15`  
		Last Modified: Wed, 16 Aug 2023 03:44:11 GMT  
		Size: 2.6 MB (2645830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4769ca050aba2b9d89f260e66fa2b89d0cb997362eeea64ca065579638f7438`  
		Last Modified: Wed, 16 Aug 2023 03:44:15 GMT  
		Size: 29.5 MB (29545395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b271177a04b0d434389a9d7c85a0d3d166e8245b0115fe284cb2adb4e0cca48`  
		Last Modified: Wed, 16 Aug 2023 03:45:00 GMT  
		Size: 158.2 MB (158246087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:latest` - linux; 386

```console
$ docker pull mono@sha256:1c5f4caca4cce6f99b6c360bca43499da6471f93cb3382548133c45c3301ff5b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.6 MB (259559303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afc318cff1d908e73180f1168f11a2d7e1327709c80436c93543d7e80222d7e6`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jul 2023 23:39:38 GMT
ADD file:a97f1ea317cafcf2810dfbe8ff5dfde5c43414d9cd1480b4e5f49d3ada8633f7 in / 
# Thu, 27 Jul 2023 23:39:38 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 00:17:04 GMT
ENV MONO_VERSION=6.12.0.182
# Fri, 28 Jul 2023 00:17:19 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 28 Jul 2023 00:17:51 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Fri, 28 Jul 2023 00:20:55 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7eefe1e1e0f6af56fb4d37f33d6efcd121b57a2c33f6ce8272858d586e51f9d0`  
		Last Modified: Thu, 27 Jul 2023 23:44:57 GMT  
		Size: 27.8 MB (27846808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4faf5b429a2c65753fbcbf71ad8350c16724286c522a53fdeca6f8c9de6a894`  
		Last Modified: Fri, 28 Jul 2023 00:23:35 GMT  
		Size: 2.8 MB (2792567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c3bc6db4d28a564350a4e9900fdf992bb455b93448bc0f64c5fbad0bea76da8`  
		Last Modified: Fri, 28 Jul 2023 00:23:48 GMT  
		Size: 68.8 MB (68800619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:584274866dcb05649b337a249dc340029a4a5b359ef05fd57c4ade73be901175`  
		Last Modified: Fri, 28 Jul 2023 00:25:02 GMT  
		Size: 160.1 MB (160119309 bytes)  
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
