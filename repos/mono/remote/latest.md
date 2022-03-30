## `mono:latest`

```console
$ docker pull mono@sha256:dbff4ee37ec2db8542789185219b86a70a0c92bcb3bbe8ea5575aaaf52bb83e8
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
$ docker pull mono@sha256:abcb22d3b82c95b20ff5c90f329cb759314b70e1781a67315b1ec2bb719e0cda
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.1 MB (236137951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a0982a1a3d0d9f836f390567b3d9452c91ca96d6b8b2e633edf0cf7994be535`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:38 GMT
ADD file:59187422476c57db46e60f894a4cfd0f243e80230ef9ea75b2d8dd4925d59df3 in / 
# Tue, 29 Mar 2022 00:22:38 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 22:50:30 GMT
ENV MONO_VERSION=6.12.0.122
# Tue, 29 Mar 2022 22:50:38 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 29 Mar 2022 22:51:01 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 29 Mar 2022 22:56:06 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:f003217c5aaebdfee0b9a448fbabd995e5f0159f5b231460c0ecc21baf171953`  
		Last Modified: Tue, 29 Mar 2022 00:28:02 GMT  
		Size: 27.2 MB (27151970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d839cde201cd1385a1c2c927214c614f1cd1bab02a62fd34b6df69e6f95daa7e`  
		Last Modified: Tue, 29 Mar 2022 23:02:05 GMT  
		Size: 2.8 MB (2777377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:158befabd0cf5fbeb7cb51a0cfc2f6c20399efe3be6abfd6d7dc8187d886b4a0`  
		Last Modified: Tue, 29 Mar 2022 23:02:14 GMT  
		Size: 64.8 MB (64760477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7f69220c106af4aa5ecc61935d51050e43fe6450996488e6c1d7fe5c5d7c2e1`  
		Last Modified: Tue, 29 Mar 2022 23:03:13 GMT  
		Size: 141.4 MB (141448127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:latest` - linux; arm variant v5

```console
$ docker pull mono@sha256:7f7e694bccdf74a53d7491c00db8088add1265f44830d8b0a365c7915304ef04
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.0 MB (191954448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71bb1b7df7ff58e8b649bb79421666f8422e0606d35629b29b8cf7c2b7ca4596`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:51:36 GMT
ADD file:7ac5498e2c44686d7eb272ef7645a0a64486cf942610f6754aa4a932f5b1a4be in / 
# Tue, 29 Mar 2022 00:51:37 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 08:50:15 GMT
ENV MONO_VERSION=6.12.0.122
# Tue, 29 Mar 2022 08:50:42 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 29 Mar 2022 08:51:31 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 29 Mar 2022 08:56:31 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:8f10b1b67f0119a2dd5f838a3e98ab2c412e4b51fb1e4841e2b79fd4cae86105`  
		Last Modified: Tue, 29 Mar 2022 01:06:51 GMT  
		Size: 24.9 MB (24887495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:103ccfc95d14718dd5bd47005c93225d5f82bdc075ccfc346e1b366afb616d57`  
		Last Modified: Tue, 29 Mar 2022 09:01:39 GMT  
		Size: 2.5 MB (2467692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13697b82f395905c310bf0030c74844e8f8fc5979a009c041a18de4488636164`  
		Last Modified: Tue, 29 Mar 2022 09:01:50 GMT  
		Size: 24.5 MB (24493260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90cc18056a6a14a94b009cdae75817ab5f9d1bea6b12aaf50cf5127985d9277f`  
		Last Modified: Tue, 29 Mar 2022 09:04:22 GMT  
		Size: 140.1 MB (140106001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:latest` - linux; arm variant v7

```console
$ docker pull mono@sha256:31fbf9e91eb2101d0872397de4770b9b1686986f8e7b00bc592b22c943506949
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.9 MB (187852543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c01fcb1ec1e569073cabc744de90c68b0d94e4c1f8af64944407f93b43e78f55`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 09:32:07 GMT
ADD file:ca7a6b7c138de7fd85996719398396d0ed0f059d2e12b7f401cd460b64924e25 in / 
# Thu, 17 Mar 2022 09:32:08 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 04:12:25 GMT
ENV MONO_VERSION=6.12.0.122
# Sat, 19 Mar 2022 04:13:03 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 19 Mar 2022 04:13:46 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 19 Mar 2022 04:18:40 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:0b8f06901fc5e8a29999e260b4ada4ee1cc4415e5c1a16fb7bb21cc2ac995f72`  
		Last Modified: Thu, 17 Mar 2022 09:48:01 GMT  
		Size: 22.8 MB (22754389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:635212b9c70cb02c0aa647ee91ce1417572add8cdc66e2e2998bcb3a9ad605d8`  
		Last Modified: Sat, 19 Mar 2022 04:23:11 GMT  
		Size: 2.4 MB (2361883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54f2618a06f8bc8c9377958b480ea3d540f429435783b225a5bf6c0246baf3af`  
		Last Modified: Sat, 19 Mar 2022 04:23:27 GMT  
		Size: 23.8 MB (23782774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6dca04f966c2a1ed84c4d9c7746998b838c704076a805d58ae9c52598d67a4a`  
		Last Modified: Sat, 19 Mar 2022 04:25:59 GMT  
		Size: 139.0 MB (138953497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:latest` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:ef7a2ed6a3f244e9ee528665f48fd1a5c61de3251f8a53589108fbd013baa570
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.5 MB (214460692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:157824826295d6bfdb01f28bc27b6f4369428303484c8db9b2e120c4e2ea8cca`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 03:22:22 GMT
ADD file:1c7d8cedf5dc79c676acebde5252ecd3005088a9f29e5e6be547f659f41efb1f in / 
# Thu, 17 Mar 2022 03:22:22 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 23:11:49 GMT
ENV MONO_VERSION=6.12.0.122
# Thu, 17 Mar 2022 23:12:36 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 17 Mar 2022 23:12:51 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 17 Mar 2022 23:15:01 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:c9277cac12165646c33f028489f2a5be3f70745382f4385cd9ed12fcc8cec183`  
		Last Modified: Thu, 17 Mar 2022 03:29:27 GMT  
		Size: 25.9 MB (25923233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f27367e69cb7b3ff75b7196e775fe63ab5f00dd80e96eb8c7f273c70b9b4c9a`  
		Last Modified: Thu, 17 Mar 2022 23:16:51 GMT  
		Size: 2.6 MB (2634667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b014c14ab68a6b650aa566e7e891e4824d9d3f8c3410c1de318a4a2d5840ae4b`  
		Last Modified: Thu, 17 Mar 2022 23:16:56 GMT  
		Size: 29.3 MB (29318310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c662eb78bf51e4cd352ecf4b1e1e41ddad13bb89a9ed4194a6e2b6a3dcc0282`  
		Last Modified: Thu, 17 Mar 2022 23:17:59 GMT  
		Size: 156.6 MB (156584482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:latest` - linux; 386

```console
$ docker pull mono@sha256:3dfa04e6e1b62f553024380bcec96d6565e40696a49190ce4b216bbe7d4338fb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.7 MB (241701680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:614ea889364fa8d1bd9d03bbd4671ed1beabfe6a4b606642b4ca1b05c1521020`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:42:26 GMT
ADD file:bcf3d504dc285de8b639c7f4017c41a4593a6c2aa6f046c9be79e587d05b5120 in / 
# Tue, 29 Mar 2022 00:42:27 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 15:02:04 GMT
ENV MONO_VERSION=6.12.0.122
# Tue, 29 Mar 2022 15:02:13 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 29 Mar 2022 15:02:36 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 29 Mar 2022 15:04:22 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:65b92490caa5e2c0588fab60d39315a2a8c09aa8ea0fe208d23f6984a47ecc03`  
		Last Modified: Tue, 29 Mar 2022 00:50:02 GMT  
		Size: 27.8 MB (27801252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aebbeca4656bb310b6dac7751436576af2e3c06066b222f9a962062ff4114cc1`  
		Last Modified: Tue, 29 Mar 2022 15:06:05 GMT  
		Size: 2.8 MB (2789213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a98d81278fc0743b83c503c809fdcffbaa11e083f06455ea6dfed18642791ba`  
		Last Modified: Tue, 29 Mar 2022 15:06:14 GMT  
		Size: 68.6 MB (68569346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:149100c1eb325c4a4b4141ffdeaeb14a9f47207ff4dcf7cf878dcfb9515ac1ee`  
		Last Modified: Tue, 29 Mar 2022 15:07:26 GMT  
		Size: 142.5 MB (142541869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:latest` - linux; ppc64le

```console
$ docker pull mono@sha256:39ff8e30c14539f61252cc048e85f52aac66223f9c5897ffa9325018e290fb54
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.6 MB (203590295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80be2528fb974e84c463e06af27e47cfcbe0b9f26252d5b5428ee0440e3caa4e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 11:19:08 GMT
ADD file:0af430b7759619d4d40ea316f823599879e4f3e0dfc8877bdee731020fb2620d in / 
# Thu, 17 Mar 2022 11:19:12 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 07:27:44 GMT
ENV MONO_VERSION=6.12.0.122
# Sat, 19 Mar 2022 07:29:35 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 19 Mar 2022 07:30:53 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 19 Mar 2022 07:39:43 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:303d92340e7868a8dc0fdad5d6c67a8a819a74a2bc47038b26339d5be6084bf4`  
		Last Modified: Thu, 17 Mar 2022 11:29:21 GMT  
		Size: 30.6 MB (30562350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d4316542fb6ac5647290bf8fc3273bd907ea2788aab876a425e0c683c30536e`  
		Last Modified: Sat, 19 Mar 2022 07:45:52 GMT  
		Size: 2.9 MB (2884710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bfc5ae0671a1f811f6836c48efb56e82b259a22cd98dc9df71508f7f3eae1d4`  
		Last Modified: Sat, 19 Mar 2022 07:45:56 GMT  
		Size: 26.9 MB (26873811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b714472ca1272d2460a4a64c207c6e7254f637463acf0a258422bd89c3585a9`  
		Last Modified: Sat, 19 Mar 2022 07:47:11 GMT  
		Size: 143.3 MB (143269424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
