## `mono:latest`

```console
$ docker pull mono@sha256:9fefd4832ac9383d5887f18c3929dab6e362aa4af3e0604c1d387b3320a5eb60
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
$ docker pull mono@sha256:2351a2ba6c2228ecac8696680f65e49607432bb7fd6c0494fd254060c48f6a02
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.1 MB (235136555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59599093bfc20b4291b6019e7cd8bd648dab8dc3c341bc26001f807264ac44dc`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:23:03 GMT
ADD file:08ea1ff3fcd4efc24ab4f262cfa24e55e65844f6858e41a46fe0635d247f174d in / 
# Thu, 23 Apr 2020 00:23:03 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:48:15 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 23 Apr 2020 01:48:26 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 01:48:58 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Apr 2020 01:59:28 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:b248fa9f6d2ae427ad7f00de3537ab256ae7eb413565f8be0773ee9b86ef57d4`  
		Last Modified: Thu, 23 Apr 2020 00:27:46 GMT  
		Size: 22.5 MB (22513488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d5f98f65ba396764fe9568783d5a5c15abaed85471ba915f7533777d9ee788d`  
		Last Modified: Thu, 23 Apr 2020 02:19:07 GMT  
		Size: 244.5 KB (244473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06df397516278d03ee36a7c24249bc8b0b57b23701952818c89538b9856c1ffb`  
		Last Modified: Thu, 23 Apr 2020 02:19:25 GMT  
		Size: 64.6 MB (64584374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29e83f8e35ba5681f2772165e09a403fab75e2cb54d9c6166e85301ad905d258`  
		Last Modified: Thu, 23 Apr 2020 02:20:55 GMT  
		Size: 147.8 MB (147794220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:latest` - linux; arm variant v5

```console
$ docker pull mono@sha256:dbe58efd8bb2b2a11ced1ee1d922fc856c4009bc1394eab3343abc03bdbb6131
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.7 MB (176694785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9dcb0c3b5b0c67efa1168410a65899de5aa5503978ddf3c06719ebf3d5c69c5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 13 May 2020 21:55:26 GMT
ADD file:9ae861b3016cc7e568c2f4f1f2a84ab78e21058bf3e65683c5e32f148bb0d834 in / 
# Wed, 13 May 2020 21:55:27 GMT
CMD ["bash"]
# Thu, 14 May 2020 03:52:16 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 14 May 2020 03:52:38 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 14 May 2020 03:53:32 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 14 May 2020 03:59:48 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:8d8bd6103e4f9e46eaf8c99b66d0017a7f616535993c72d6d02dce33ad4e616c`  
		Last Modified: Wed, 13 May 2020 22:03:26 GMT  
		Size: 21.2 MB (21190862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f81f4d5b6c060bd62f79cbe8ea07a285134eb7ece2926e8ed80b126f8b1b4cf6`  
		Last Modified: Thu, 14 May 2020 04:07:56 GMT  
		Size: 244.5 KB (244516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f12d431057ad3d238e7bb5f762d81429e12fe47af291dc9b9de1caf3c9a4947f`  
		Last Modified: Thu, 14 May 2020 04:08:06 GMT  
		Size: 25.4 MB (25367720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b28656c4952ef72163db34f2802328c4bee6074c6238f05b9eeabe0498db4ee`  
		Last Modified: Thu, 14 May 2020 04:09:33 GMT  
		Size: 129.9 MB (129891687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:latest` - linux; arm variant v7

```console
$ docker pull mono@sha256:55ef6d96d85e1d0e3aca832b8c2a7a0b7da50bffa2dacf77542fbd7aff27a559
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.7 MB (172707764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc9acd8a77a391a80d27014968c3dfe08186f34930cc569f44c35d2a7a09b22c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 13 May 2020 21:19:24 GMT
ADD file:aac27626ed8520bcfd1f03f5b7aa780a4e94978b86afcc507994a8c240953561 in / 
# Wed, 13 May 2020 21:19:26 GMT
CMD ["bash"]
# Thu, 14 May 2020 00:26:29 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 14 May 2020 00:26:48 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 14 May 2020 00:27:40 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 14 May 2020 00:33:55 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:307a7e70a6dd41fc81298d6cb2641ebfa8e7bc00b0b27f30f6559f9976a46f1e`  
		Last Modified: Wed, 13 May 2020 21:28:39 GMT  
		Size: 19.3 MB (19298476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91631fd0b2baefb452095603fc22b8be62f3657d1ae76086f6318c48f36cae25`  
		Last Modified: Thu, 14 May 2020 00:42:46 GMT  
		Size: 244.5 KB (244516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:707e4565b23eaef80b85f8caf65db746d521af83f33888a710630ea91c60de18`  
		Last Modified: Thu, 14 May 2020 00:42:55 GMT  
		Size: 24.6 MB (24608714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40a42be730e2ad23f35deb8b93a0913d13edb02be20a73fa837770d36acbbf74`  
		Last Modified: Thu, 14 May 2020 00:44:20 GMT  
		Size: 128.6 MB (128556058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:latest` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:cbc1409b11ea1fd492744b6396ef5a9afa4bd427de25d89ea8406fbd9189d0a7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.7 MB (194747627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:939138ef9b9d3ec1af2baae95869f7cf8c66020511a3bb70138be5e5dd8450f2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 13 May 2020 21:48:17 GMT
ADD file:53d95477395267e3c1059f1101e29a7d4b0fcb2bb52351542f4ac065ccb0b973 in / 
# Wed, 13 May 2020 21:48:19 GMT
CMD ["bash"]
# Thu, 14 May 2020 02:00:25 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 14 May 2020 02:00:49 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 14 May 2020 02:01:47 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 14 May 2020 02:07:30 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:1d8af20f9b50479a890734605435a9de85d69f19b65d29c9c92f43eea2463979`  
		Last Modified: Wed, 13 May 2020 21:56:26 GMT  
		Size: 20.4 MB (20370044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b5f88aa673180f3a9e54d2d3fc9c67565c9545d3072c1a42eee0eda3192c039`  
		Last Modified: Thu, 14 May 2020 02:14:51 GMT  
		Size: 244.4 KB (244366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5622468da1cdc4403ec0072a3093de5483f907e82f7e7493e9bcf66765d2367`  
		Last Modified: Thu, 14 May 2020 02:14:59 GMT  
		Size: 29.4 MB (29419827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a79b7e06bf892f3f0e1c21e1bdc62517abc6fd4fd31a2f0be27e369398f2d0ca`  
		Last Modified: Thu, 14 May 2020 02:16:28 GMT  
		Size: 144.7 MB (144713390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:latest` - linux; 386

```console
$ docker pull mono@sha256:91becebb427753ead531605be391b0528b1b8176f46762f3fb896b58fbf493f5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.5 MB (243509833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d912f07467de168fbaadffea2b2be97d24f40de4675c1ef98b3b7c70f274b9c5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 13 May 2020 21:42:40 GMT
ADD file:39f8a4c4274f123e2c0a2ef48ac1a111bcc59fda68f3946ab5d644f480fab499 in / 
# Wed, 13 May 2020 21:42:41 GMT
CMD ["bash"]
# Thu, 14 May 2020 00:33:55 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 14 May 2020 00:34:10 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 14 May 2020 00:34:57 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 14 May 2020 00:40:29 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:1fa825514fac4b3d9226a943b4954a2efb197db27c0c1c5019bf4a5f7529746e`  
		Last Modified: Wed, 13 May 2020 21:50:17 GMT  
		Size: 23.1 MB (23141460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eac1a2c3c2e8b2376318177cabaab6efa4884e4a1262be8019864dd8d79b02d`  
		Last Modified: Thu, 14 May 2020 00:46:50 GMT  
		Size: 244.5 KB (244476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0517e1b7f3b81bc5e21be055d429fe5465bebb94609a0824c5064f1c2198ea92`  
		Last Modified: Thu, 14 May 2020 00:47:08 GMT  
		Size: 68.6 MB (68630757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b33be2fe9551abfc1002c4bad0c8ce971f275c3ca146936540551c5776b4fd4`  
		Last Modified: Thu, 14 May 2020 00:49:07 GMT  
		Size: 151.5 MB (151493140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:latest` - linux; ppc64le

```console
$ docker pull mono@sha256:28211181008fc8a25dbc12b5f75fd4857e92af22ee4716fd13064027ba80c113
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.0 MB (178995744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcbdcf050885aeb282b85d9942bee597145d594577643da02a09cb638cd2edb9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 13 May 2020 22:42:09 GMT
ADD file:341dbc564992a44e81b3a4f399f7de14d7340a45b73c577edb78e16da2c14584 in / 
# Wed, 13 May 2020 22:42:12 GMT
CMD ["bash"]
# Thu, 14 May 2020 01:44:38 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 14 May 2020 01:45:44 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 14 May 2020 01:47:00 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 14 May 2020 01:57:53 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:3b6ae894780534c0f99588e9cce4beb8fb7884b4578e6206b72f2db75116bb1c`  
		Last Modified: Wed, 13 May 2020 23:02:51 GMT  
		Size: 22.8 MB (22785361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c0d85174db6ce48c895d3bbf3f847e1cba986fc66e705bd86bb13e3fbf73286`  
		Last Modified: Thu, 14 May 2020 02:10:48 GMT  
		Size: 244.5 KB (244533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6124cc55d37923fca85643397621b030dae64f93ddf2c45ed9704bf9e9e5d141`  
		Last Modified: Thu, 14 May 2020 02:11:06 GMT  
		Size: 25.8 MB (25775347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64bc6db4438da29e772ebf533c91b52b035c322c12bf45899c0cbcff8a42ba24`  
		Last Modified: Thu, 14 May 2020 02:13:51 GMT  
		Size: 130.2 MB (130190503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
