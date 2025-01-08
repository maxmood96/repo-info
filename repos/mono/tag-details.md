<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `mono`

-	[`mono:6`](#mono6)
-	[`mono:6-slim`](#mono6-slim)
-	[`mono:6.10`](#mono610)
-	[`mono:6.10-slim`](#mono610-slim)
-	[`mono:6.10.0`](#mono6100)
-	[`mono:6.10.0-slim`](#mono6100-slim)
-	[`mono:6.10.0.104`](#mono6100104)
-	[`mono:6.10.0.104-slim`](#mono6100104-slim)
-	[`mono:6.12`](#mono612)
-	[`mono:6.12-slim`](#mono612-slim)
-	[`mono:6.12.0`](#mono6120)
-	[`mono:6.12.0-slim`](#mono6120-slim)
-	[`mono:6.12.0.182`](#mono6120182)
-	[`mono:6.12.0.182-slim`](#mono6120182-slim)
-	[`mono:latest`](#monolatest)
-	[`mono:slim`](#monoslim)

## `mono:6`

```console
$ docker pull mono@sha256:34d816779b1248b5cfd095770b64ecbaf1798e2aca693a91c11a018dce9c7ad5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le

### `mono:6` - linux; amd64

```console
$ docker pull mono@sha256:d2ae1881a608fb6401bcebbf0d444fc2fcadf0db27f07c87153a79e7b14e861a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.6 MB (254589877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16d98cfcc673531288833a5cdb9f87087aa18082d1fed9ebe02021c67b1fdf0f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jun 2022 16:43:21 GMT
ADD file:cce4de1623245f9f28e3365e6cf749d85dcfedddea2d6fbc963c309a40818f52 in / 
# Wed, 22 Jun 2022 16:43:21 GMT
CMD ["bash"]
# Wed, 22 Jun 2022 16:43:21 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 22 Jun 2022 16:43:21 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr # buildkit
# Wed, 22 Jun 2022 16:43:21 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
# Wed, 22 Jun 2022 16:43:21 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
```

-	Layers:
	-	`sha256:b338562f40a7fb7360dfae935da6d7e40d2545db18bc461d9d70ec1b2b657f33`  
		Last Modified: Thu, 13 Jun 2024 01:26:49 GMT  
		Size: 27.3 MB (27337703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b1b752ddf75c64e105424fb16f5a2053ddad33f059e3be8e520e35908cc4e97`  
		Last Modified: Fri, 21 Jun 2024 01:03:10 GMT  
		Size: 2.8 MB (2780035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d574eb224b5ddbe14656e28913cf5eeb5b14aa651aa3bcb9288aa43f1000aec5`  
		Last Modified: Fri, 21 Jun 2024 01:03:11 GMT  
		Size: 64.6 MB (64555923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb9d6fb145c5367510a78273891d0ba84d7257b0bfdf3cd340f4e3d6f211de0a`  
		Last Modified: Fri, 21 Jun 2024 02:02:49 GMT  
		Size: 159.9 MB (159916216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mono:6` - unknown; unknown

```console
$ docker pull mono@sha256:fc661c46136b8f9cbe60f721c811fb05d600f7614c9ddef8306ca5a261a6ea24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11085967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6322617bf4f258627a38887597f3d55cd3e73d36de6aa5f4734d1d6fcd3e7fd9`

```dockerfile
```

-	Layers:
	-	`sha256:08c2cae238c884d7e44ae9bd57336a51412c9603e15025c0a456eca7dd888aba`  
		Last Modified: Fri, 21 Jun 2024 02:02:46 GMT  
		Size: 11.1 MB (11078059 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2dda4ada58791fac758ee1dc7c9ee2756a6d55125463cc11427657bfedecb286`  
		Last Modified: Fri, 21 Jun 2024 02:02:46 GMT  
		Size: 7.9 KB (7908 bytes)  
		MIME: application/vnd.in-toto+json

### `mono:6` - linux; arm variant v5

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

### `mono:6` - linux; arm variant v7

```console
$ docker pull mono@sha256:bb330a955d4e30fc342e6a770e76253662e2ab4eaf51dbb51f988815f6b28f29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.9 MB (188935459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d07296a48da608d892f2dcc9928236339e8eaedab5e92f1a0bb2cb73c9a1693e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jun 2022 16:43:21 GMT
ADD file:ab786d88497f915679b3ac228e3bd805a58501dcb33b3d25e49cf1898770f9a7 in / 
# Wed, 22 Jun 2022 16:43:21 GMT
CMD ["bash"]
# Wed, 22 Jun 2022 16:43:21 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 22 Jun 2022 16:43:21 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr # buildkit
# Wed, 22 Jun 2022 16:43:21 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
# Wed, 22 Jun 2022 16:43:21 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
```

-	Layers:
	-	`sha256:99d1ebcdd364332a1427098feecc8f94a8978ec971b171f7cca03bf01d1a149c`  
		Size: 22.9 MB (22944997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47de34cd92203a1c44adc48be4330b559dcef9e18da3b5babab329d0fd26e11f`  
		Last Modified: Fri, 21 Jun 2024 05:26:04 GMT  
		Size: 2.4 MB (2370028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14dae79eba6437cf8f1fe8c17653348408d9b42ad8948d93472bbffd86792d7b`  
		Last Modified: Fri, 21 Jun 2024 05:26:05 GMT  
		Size: 23.6 MB (23573077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f623ef7b096557bbf700a18c1f6616fa36cfb781282427c32b42ee2bf6f5d788`  
		Last Modified: Fri, 21 Jun 2024 13:15:11 GMT  
		Size: 140.0 MB (140047357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mono:6` - unknown; unknown

```console
$ docker pull mono@sha256:85360b79dd6fd6383cee0bf95518112f77c11353aaa15ab291ba68db619e15ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.0 MB (10995859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2bed6a6671ce784ea5373b029adbbe3d4b3b1ff7a8f59eed60bb7fed2baee0e`

```dockerfile
```

-	Layers:
	-	`sha256:a2750707e64721db5673f1d8443493f0a94e552993057b314e46f727642deefe`  
		Last Modified: Fri, 21 Jun 2024 13:15:08 GMT  
		Size: 11.0 MB (10987855 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:626e6cbf5e9f3aba334705529601969366e52b1b76d405943e486e844d7bbfea`  
		Last Modified: Fri, 21 Jun 2024 13:15:07 GMT  
		Size: 8.0 KB (8004 bytes)  
		MIME: application/vnd.in-toto+json

### `mono:6` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:5b876dc42dbdf92201a17d179906d941011b64493b32ce09d0d1faf12f470361
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.3 MB (216300519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bbe627177b284938a13b85f3505e07a72c220eeae1d6d4b9a675687f4a9f9be`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jun 2022 16:43:21 GMT
ADD file:de9a2b323e6d7d969277e7e781875e3daf3f49f2c1dcc569a1eec4f5bd789c46 in / 
# Wed, 22 Jun 2022 16:43:21 GMT
CMD ["bash"]
# Wed, 22 Jun 2022 16:43:21 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 22 Jun 2022 16:43:21 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr # buildkit
# Wed, 22 Jun 2022 16:43:21 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
# Wed, 22 Jun 2022 16:43:21 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
```

-	Layers:
	-	`sha256:7abf9f73c7747bb840a8edcd895830e53f09498136de3015568a9cd9f5ab10ed`  
		Last Modified: Thu, 13 Jun 2024 00:44:26 GMT  
		Size: 26.1 MB (26109272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eedc96c6829dd818687f02719ed29ee02b62d29b93d260a87cbfdf65bd82307`  
		Last Modified: Fri, 21 Jun 2024 07:34:59 GMT  
		Size: 2.6 MB (2644870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc18ec37f21948c54422a8a2bd31634ae80dc4cd7d1f82b12857c17ad3e4aeec`  
		Size: 29.3 MB (29329348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a97a948909451f0ef002b4ce1035b5a09a3acde1633d198b1b7d25d6729f696`  
		Last Modified: Fri, 21 Jun 2024 17:09:25 GMT  
		Size: 158.2 MB (158217029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mono:6` - unknown; unknown

```console
$ docker pull mono@sha256:06f899f1f0a8c6a50d0cccbe9f415f29eb3eb9dba67e1076050fb7fa3214bc38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.2 MB (11173870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0a16765ae4b4d709f200047ad778fd0e6b25c0149b15eeb60dff4320acaf196`

```dockerfile
```

-	Layers:
	-	`sha256:3d8ff956fff2b5ea5a8f2a0f26101974ab6b290a4863020c141f56ce0ff86582`  
		Last Modified: Fri, 21 Jun 2024 17:09:17 GMT  
		Size: 11.2 MB (11165553 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0812c62e6dd0b6028ef0d86e34492bdbb20ebf6bae746864504d4121912d4cba`  
		Last Modified: Fri, 21 Jun 2024 17:09:16 GMT  
		Size: 8.3 KB (8317 bytes)  
		MIME: application/vnd.in-toto+json

### `mono:6` - linux; 386

```console
$ docker pull mono@sha256:8f10891be25745681bd6f98bf48e1234094816dc4b5dbef73d48f53f67536601
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.5 MB (259458549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2775d67ed2568bc292fd99d9a4c6e6e31195ae5382d5d3f1d76cb0f034c34e5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jun 2022 16:43:21 GMT
ADD file:7bc8fc617f718bf5e65e7fd718531a01122acc1783af5233c98aa9d31b0f093e in / 
# Wed, 22 Jun 2022 16:43:21 GMT
CMD ["bash"]
# Wed, 22 Jun 2022 16:43:21 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 22 Jun 2022 16:43:21 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr # buildkit
# Wed, 22 Jun 2022 16:43:21 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
# Wed, 22 Jun 2022 16:43:21 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
```

-	Layers:
	-	`sha256:1dfc643447ff7a82c599b429eda0d998c6dbad4ab2786eed580821b5b888204e`  
		Last Modified: Wed, 08 Jan 2025 03:46:41 GMT  
		Size: 28.0 MB (27994640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a198cb1aaae91cef3ed2eaed184c0a10f0b74e857bd5ea91dcde2955746f20f9`  
		Last Modified: Wed, 08 Jan 2025 03:46:41 GMT  
		Size: 2.8 MB (2791765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd658841b3e1b2084a6340e82f84033bf765e9ea9830350aa5a4aba88cbf3166`  
		Last Modified: Fri, 21 Jun 2024 01:03:14 GMT  
		Size: 68.6 MB (68585515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30bbf7033252959af4d7a4d2f468bba517cf0aeaf9f9e131902187bdc9737e6d`  
		Last Modified: Fri, 21 Jun 2024 02:04:03 GMT  
		Size: 160.1 MB (160086629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mono:6` - unknown; unknown

```console
$ docker pull mono@sha256:e69c4a0ff0efcd311f3ec0da7e72cbafaa9689b8555686674db7d3d689e13230
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11081926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48b0f05b8c3e2ec0bdb3fcbf2f85778a7584ea1dfd621e838399e99f0e6aac47`

```dockerfile
```

-	Layers:
	-	`sha256:f5bc84e8ea570b2500296b1f25f4226e60f0c15178c4ed81b09fa2c5ddf35fc6`  
		Last Modified: Fri, 21 Jun 2024 02:03:58 GMT  
		Size: 11.1 MB (11074056 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f11f469c7181081a082c334f89f2885f7a6a0953d5e152e5f75db2af4504d80e`  
		Last Modified: Fri, 21 Jun 2024 02:03:57 GMT  
		Size: 7.9 KB (7870 bytes)  
		MIME: application/vnd.in-toto+json

### `mono:6` - linux; ppc64le

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

## `mono:6-slim`

```console
$ docker pull mono@sha256:eb9a8d42dc58090cdb0d39b36422d9560f33e9d2cce22f4c888da263cee46c45
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le

### `mono:6-slim` - linux; amd64

```console
$ docker pull mono@sha256:749851d74745492754d1ebb3c50fc335d4b84a7bb34e17a4e7c3909c5ec1212b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.7 MB (94673661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5a2a70110040ee175a00069fa147d036d49deb2decd03a6374e83da337706e8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jun 2022 16:43:21 GMT
ADD file:cce4de1623245f9f28e3365e6cf749d85dcfedddea2d6fbc963c309a40818f52 in / 
# Wed, 22 Jun 2022 16:43:21 GMT
CMD ["bash"]
# Wed, 22 Jun 2022 16:43:21 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 22 Jun 2022 16:43:21 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr # buildkit
# Wed, 22 Jun 2022 16:43:21 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
```

-	Layers:
	-	`sha256:b338562f40a7fb7360dfae935da6d7e40d2545db18bc461d9d70ec1b2b657f33`  
		Last Modified: Thu, 13 Jun 2024 01:26:49 GMT  
		Size: 27.3 MB (27337703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b1b752ddf75c64e105424fb16f5a2053ddad33f059e3be8e520e35908cc4e97`  
		Last Modified: Fri, 21 Jun 2024 01:03:10 GMT  
		Size: 2.8 MB (2780035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d574eb224b5ddbe14656e28913cf5eeb5b14aa651aa3bcb9288aa43f1000aec5`  
		Last Modified: Fri, 21 Jun 2024 01:03:11 GMT  
		Size: 64.6 MB (64555923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mono:6-slim` - unknown; unknown

```console
$ docker pull mono@sha256:5a8421c386b586f98034983cc67448394e910e05ff857862418296991eddcf54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4134119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7daf4a5e106256a64c61c2f6e62ec4e5aa7020398e1b40c8bbe8b4e7458bec8d`

```dockerfile
```

-	Layers:
	-	`sha256:68c0c6a6586378e1af3fd618d65a15dd0a69c3e36744d2db3c2a64b91f8842b8`  
		Last Modified: Fri, 21 Jun 2024 01:03:10 GMT  
		Size: 4.1 MB (4124009 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ec35e37e8929d1729d15f72eaafb529c88604e0eb2b568452d3927312850835`  
		Last Modified: Fri, 21 Jun 2024 01:03:10 GMT  
		Size: 10.1 KB (10110 bytes)  
		MIME: application/vnd.in-toto+json

### `mono:6-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:f7c133539fa6a4add7484e9c93bc9b62ec32236d4b619f320c20b3248fb4739a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.9 MB (51860964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe52652f149ceedc89ed0c0f70985fcd898b6cd5cc98aa6f99f9ca06fd83046c`
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

### `mono:6-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:dd07ed6527eaa5860d31d50e7a3c5521b6f559eed9822aeeeb8667ce8390e378
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48888102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f645d1e48f0116b7141165a6952885d2f77e3033c87231c6d63152270ffd7a33`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jun 2022 16:43:21 GMT
ADD file:ab786d88497f915679b3ac228e3bd805a58501dcb33b3d25e49cf1898770f9a7 in / 
# Wed, 22 Jun 2022 16:43:21 GMT
CMD ["bash"]
# Wed, 22 Jun 2022 16:43:21 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 22 Jun 2022 16:43:21 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr # buildkit
# Wed, 22 Jun 2022 16:43:21 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
```

-	Layers:
	-	`sha256:99d1ebcdd364332a1427098feecc8f94a8978ec971b171f7cca03bf01d1a149c`  
		Size: 22.9 MB (22944997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47de34cd92203a1c44adc48be4330b559dcef9e18da3b5babab329d0fd26e11f`  
		Last Modified: Fri, 21 Jun 2024 05:26:04 GMT  
		Size: 2.4 MB (2370028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14dae79eba6437cf8f1fe8c17653348408d9b42ad8948d93472bbffd86792d7b`  
		Last Modified: Fri, 21 Jun 2024 05:26:05 GMT  
		Size: 23.6 MB (23573077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mono:6-slim` - unknown; unknown

```console
$ docker pull mono@sha256:ee35f615c2629a07e18483c6e85d7a3c83498ec7a51d34e09c6831e8720ee843
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4043799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e77739a150c122ee693247b621455e84030503770aa1098a0d6e90ae5d11efea`

```dockerfile
```

-	Layers:
	-	`sha256:e211386d3756bb307e96a299f301c5ef1eb874182b4c4a9e23f63b9ae5388ec3`  
		Last Modified: Fri, 21 Jun 2024 05:26:05 GMT  
		Size: 4.0 MB (4033599 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78feeadf8c15b58b8ecdee782634016d91ad2995f88bccaf8f187a8adc6ef4ff`  
		Last Modified: Fri, 21 Jun 2024 05:26:04 GMT  
		Size: 10.2 KB (10200 bytes)  
		MIME: application/vnd.in-toto+json

### `mono:6-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:f8ca545da29ef84d991bc3713b7284fcee5344a8e73eac40567bfefcf7de4a20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.1 MB (58083490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:337ba12936b175b1f418a4a2fb20db97d206faf71ca52fd475c94ac4d3993a3e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jun 2022 16:43:21 GMT
ADD file:de9a2b323e6d7d969277e7e781875e3daf3f49f2c1dcc569a1eec4f5bd789c46 in / 
# Wed, 22 Jun 2022 16:43:21 GMT
CMD ["bash"]
# Wed, 22 Jun 2022 16:43:21 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 22 Jun 2022 16:43:21 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr # buildkit
# Wed, 22 Jun 2022 16:43:21 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
```

-	Layers:
	-	`sha256:7abf9f73c7747bb840a8edcd895830e53f09498136de3015568a9cd9f5ab10ed`  
		Last Modified: Thu, 13 Jun 2024 00:44:26 GMT  
		Size: 26.1 MB (26109272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eedc96c6829dd818687f02719ed29ee02b62d29b93d260a87cbfdf65bd82307`  
		Last Modified: Fri, 21 Jun 2024 07:34:59 GMT  
		Size: 2.6 MB (2644870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc18ec37f21948c54422a8a2bd31634ae80dc4cd7d1f82b12857c17ad3e4aeec`  
		Size: 29.3 MB (29329348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mono:6-slim` - unknown; unknown

```console
$ docker pull mono@sha256:cd9b48412dc563b39c0103943d5ed3cbc90b60a7c49d51e07903e020b8cfb981
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4221860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fefffedbcde83d1d79c60cf414a8e8472225ffa87437cbd87ed93cbcde2840f2`

```dockerfile
```

-	Layers:
	-	`sha256:681a9485d68b8e56f7c721e96ecc685811a344e8356bab9dcbb7ed283fc771a4`  
		Last Modified: Fri, 21 Jun 2024 07:34:59 GMT  
		Size: 4.2 MB (4211431 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a953520626886eee4ff5675e5962fcd17b1795c5421161e5d957486e675fec3b`  
		Last Modified: Fri, 21 Jun 2024 07:34:58 GMT  
		Size: 10.4 KB (10429 bytes)  
		MIME: application/vnd.in-toto+json

### `mono:6-slim` - linux; 386

```console
$ docker pull mono@sha256:819bc68ca415cdb49ad461b4afb9a27004e442878b2bbdefc8a67317bc5b2ddf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.4 MB (99371920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c360bfbb224cb22cd13ba52ccd63bc77562ef28647c535cd0a42518f0773a842`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jun 2022 16:43:21 GMT
ADD file:7bc8fc617f718bf5e65e7fd718531a01122acc1783af5233c98aa9d31b0f093e in / 
# Wed, 22 Jun 2022 16:43:21 GMT
CMD ["bash"]
# Wed, 22 Jun 2022 16:43:21 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 22 Jun 2022 16:43:21 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr # buildkit
# Wed, 22 Jun 2022 16:43:21 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
```

-	Layers:
	-	`sha256:1dfc643447ff7a82c599b429eda0d998c6dbad4ab2786eed580821b5b888204e`  
		Last Modified: Wed, 08 Jan 2025 03:46:41 GMT  
		Size: 28.0 MB (27994640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a198cb1aaae91cef3ed2eaed184c0a10f0b74e857bd5ea91dcde2955746f20f9`  
		Last Modified: Wed, 08 Jan 2025 03:46:41 GMT  
		Size: 2.8 MB (2791765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd658841b3e1b2084a6340e82f84033bf765e9ea9830350aa5a4aba88cbf3166`  
		Last Modified: Fri, 21 Jun 2024 01:03:14 GMT  
		Size: 68.6 MB (68585515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mono:6-slim` - unknown; unknown

```console
$ docker pull mono@sha256:21b839469b89df687807ffdd3f870708c16efa44a6b299510e9d6391ba6499fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4130249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80ef153a1ce2f246cf50247bdbe0e53a65f2eca1f65498fe5be40b5242f5f8b1`

```dockerfile
```

-	Layers:
	-	`sha256:053ce445b27e3a8e224b16a3d2a8cdc9dc1d84ebee53d08de3d37ec36d5de95c`  
		Size: 4.1 MB (4120175 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:190e2c58614be0d956b94cdc868f9beb77c2f2d8ef16c981339f2b2c23f56975`  
		Last Modified: Fri, 21 Jun 2024 01:03:12 GMT  
		Size: 10.1 KB (10074 bytes)  
		MIME: application/vnd.in-toto+json

### `mono:6-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:b83383e51874bbee097571b303be3299c87d7da8c4c6b0f4e067cfaa552ad925
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75350311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c28d9c810a28445dd3b5767c5be8a3a5c5f459f859498e49f59bb419b735510`
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

## `mono:6.10`

```console
$ docker pull mono@sha256:5b05ebda98b4e0e247a53e00c3748edc89dceeab763817999f0a6cfe37162e02
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le

### `mono:6.10` - linux; amd64

```console
$ docker pull mono@sha256:843c03721d4c4c3dc7df49913f7ec8b961da0b80934d7e2fc1ab386584503cf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.0 MB (224997323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:874411c91faac3f25999aad4273d41541fbfea71027283a4dbae8cb6bf804647`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Nov 2021 20:21:03 GMT
ADD file:cce4de1623245f9f28e3365e6cf749d85dcfedddea2d6fbc963c309a40818f52 in / 
# Tue, 23 Nov 2021 20:21:03 GMT
CMD ["bash"]
# Tue, 23 Nov 2021 20:21:03 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 23 Nov 2021 20:21:03 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr # buildkit
# Tue, 23 Nov 2021 20:21:03 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
# Tue, 23 Nov 2021 20:21:03 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
```

-	Layers:
	-	`sha256:b338562f40a7fb7360dfae935da6d7e40d2545db18bc461d9d70ec1b2b657f33`  
		Last Modified: Thu, 13 Jun 2024 01:26:49 GMT  
		Size: 27.3 MB (27337703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17858d27bab2d3cac617525d602bdb6430ef30203a5879d871c8ac9c5ed9ccc3`  
		Last Modified: Fri, 21 Jun 2024 01:03:10 GMT  
		Size: 2.8 MB (2780056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95304a756dfd5de0e2f44edffff0c73d65982f8523d664fd5f1d97ea84d3fba5`  
		Last Modified: Fri, 21 Jun 2024 01:03:11 GMT  
		Size: 64.6 MB (64563570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d38d92e81b89d82472ba771ba73bd96f9d7434d0a078d894095ba9332fedb7e4`  
		Last Modified: Fri, 21 Jun 2024 02:10:26 GMT  
		Size: 130.3 MB (130315994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mono:6.10` - unknown; unknown

```console
$ docker pull mono@sha256:f6671a285cbddce3760628595ffd4269c14d56576a01a7e1c1d9e0d22e9e3b52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.0 MB (11001689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:804b6302fcfc8892b5ad5455687216266c9950964c2ec1c967cc45dcd95365eb`

```dockerfile
```

-	Layers:
	-	`sha256:3f1bc3f47a2da7c663404a8b55db0810f54025932a6bfdbd60ed373988d5c3a3`  
		Last Modified: Fri, 21 Jun 2024 02:10:25 GMT  
		Size: 11.0 MB (10994359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bddb6bc492023a1217e6c5d5449b14b7a64e1659932a9e489d3eac1a6c8cbdb2`  
		Last Modified: Fri, 21 Jun 2024 02:10:24 GMT  
		Size: 7.3 KB (7330 bytes)  
		MIME: application/vnd.in-toto+json

### `mono:6.10` - linux; arm variant v5

```console
$ docker pull mono@sha256:5fd28ff75f47e10162fa8359e3457ed77e6a13c9eb64585df39efdf63e70a1a1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.9 MB (180861329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efa9d1dae1421f12f6f7eecf8cfaac5d7da3f6b99f6874365ce2f2f5fc9d9662`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 00:49:37 GMT
ADD file:2ed7ca0d45c68b46a10ae186e8a03f98e72cadfeed17105668f53adf14d31e1f in / 
# Tue, 02 Aug 2022 00:49:38 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 07:18:54 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 01 Mar 2023 07:19:03 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 01 Mar 2023 07:19:22 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 01 Mar 2023 07:22:13 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:187ecffbd1e0eae5de6567dff32bd58f28623635657779760c9d9539d6b7cc59`  
		Last Modified: Tue, 02 Aug 2022 00:57:06 GMT  
		Size: 24.9 MB (24889750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb25ee9d7e5ee2ba3d5fe6104206a45f2c5c425365a535e0aaac7bb9bd71034e`  
		Last Modified: Wed, 01 Mar 2023 07:23:36 GMT  
		Size: 2.5 MB (2467730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4b5b10e99353e19dd9c56deed1fd46d8ffc3c3eb2ad78b8d36ac029a085764e`  
		Last Modified: Wed, 01 Mar 2023 07:23:40 GMT  
		Size: 24.5 MB (24521836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75576104ae9839169a1957af7269a139e0be7d50d8cef2a4fe4011b528926e18`  
		Last Modified: Wed, 01 Mar 2023 07:25:04 GMT  
		Size: 129.0 MB (128982013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10` - linux; arm variant v7

```console
$ docker pull mono@sha256:b64c7fec47098f7cef6a337440933e17160202b129379df9d69709d368a9e4ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.7 MB (176724730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:706b8666526419ef5c72339aa6da41a1531a2451fc0f6f3c3b47aa597e3d1bf9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Nov 2021 20:21:03 GMT
ADD file:ab786d88497f915679b3ac228e3bd805a58501dcb33b3d25e49cf1898770f9a7 in / 
# Tue, 23 Nov 2021 20:21:03 GMT
CMD ["bash"]
# Tue, 23 Nov 2021 20:21:03 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 23 Nov 2021 20:21:03 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr # buildkit
# Tue, 23 Nov 2021 20:21:03 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
# Tue, 23 Nov 2021 20:21:03 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
```

-	Layers:
	-	`sha256:99d1ebcdd364332a1427098feecc8f94a8978ec971b171f7cca03bf01d1a149c`  
		Size: 22.9 MB (22944997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f82b184891ecf71303c14e6658ace46e95f5f157682da9b582cb967e9648c10d`  
		Size: 2.4 MB (2370004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0593643cc80b45c3e95e55271aebb7b5b474a3c444cff93983b44b2a84dafeae`  
		Last Modified: Fri, 21 Jun 2024 05:27:16 GMT  
		Size: 23.6 MB (23601401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f5da2a8951d66ec9b732a2291ad3fee626491fc08869d73bb850877aa7135f6`  
		Last Modified: Fri, 21 Jun 2024 13:18:42 GMT  
		Size: 127.8 MB (127808328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mono:6.10` - unknown; unknown

```console
$ docker pull mono@sha256:127701c9a8598ed4210ada06533b7a2a814bbf1668a53a6fd700eeb265417bcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10911546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce5c28342bce9abcfa397f21f9383ab304c6fcc24beda749f961319badf97c7d`

```dockerfile
```

-	Layers:
	-	`sha256:700ee908ff26cfb514951f19bc2ca97f1e8b7dcec561da7e3a8617b923ccace3`  
		Last Modified: Fri, 21 Jun 2024 13:18:39 GMT  
		Size: 10.9 MB (10904137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eca39222920792a108e34122757e88db4c17ce48dae31e3a423f1c69d039d4bd`  
		Last Modified: Fri, 21 Jun 2024 13:18:38 GMT  
		Size: 7.4 KB (7409 bytes)  
		MIME: application/vnd.in-toto+json

### `mono:6.10` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:d7c0737bfe98e3ea5ccdcd827b1acc4ffc40158eff330e229298454aa8263763
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.6 MB (203595079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2910c477dd60bc2f1053dc681f8d56d36a4b3512cca404a60e230718f6b485a8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Nov 2021 20:21:03 GMT
ADD file:de9a2b323e6d7d969277e7e781875e3daf3f49f2c1dcc569a1eec4f5bd789c46 in / 
# Tue, 23 Nov 2021 20:21:03 GMT
CMD ["bash"]
# Tue, 23 Nov 2021 20:21:03 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 23 Nov 2021 20:21:03 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr # buildkit
# Tue, 23 Nov 2021 20:21:03 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
# Tue, 23 Nov 2021 20:21:03 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
```

-	Layers:
	-	`sha256:7abf9f73c7747bb840a8edcd895830e53f09498136de3015568a9cd9f5ab10ed`  
		Last Modified: Thu, 13 Jun 2024 00:44:26 GMT  
		Size: 26.1 MB (26109272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c486eb1fc96e8a0a90813bfa8a70b20adbe94ff7d89de75830366f1a316340fc`  
		Last Modified: Fri, 21 Jun 2024 07:35:43 GMT  
		Size: 2.6 MB (2644871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ace1bfdd6d06b8bfc35d8fa73745e008236ccb724d7a1b921904f981903a0d68`  
		Last Modified: Fri, 21 Jun 2024 07:35:44 GMT  
		Size: 29.4 MB (29358249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1568d30ad91e8fe704c9799d461b35a06a344a8f88f2341179f5931eb8f409e`  
		Last Modified: Fri, 21 Jun 2024 17:12:27 GMT  
		Size: 145.5 MB (145482687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mono:6.10` - unknown; unknown

```console
$ docker pull mono@sha256:abfa7fa09981d22676e93c2590a9dadea0d36a6933ba87241bfca4190daea5c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11089541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46874ea2f565c3d4b2c7539eb7c4dd87650854ecad1c0491d702d1195eb0fc1e`

```dockerfile
```

-	Layers:
	-	`sha256:74ac47f39057ef5ffc07174295f77e6be6506ad0eece9418721ecea147466433`  
		Size: 11.1 MB (11081827 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1826670f27c4749b3087c12c4ab418cb4325b69292d42f3f91d398474b70c506`  
		Last Modified: Fri, 21 Jun 2024 17:12:23 GMT  
		Size: 7.7 KB (7714 bytes)  
		MIME: application/vnd.in-toto+json

### `mono:6.10` - linux; 386

```console
$ docker pull mono@sha256:1ff9e0605a84ebc9c1425cf380fa6538513957f14ff53668bb1415bc0de06276
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.8 MB (230808213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:165beb97a02082ea41ab2c93bf8061f5337e9c3e47d92a7c3fdbb3d91c05cf4f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Nov 2021 20:21:03 GMT
ADD file:7bc8fc617f718bf5e65e7fd718531a01122acc1783af5233c98aa9d31b0f093e in / 
# Tue, 23 Nov 2021 20:21:03 GMT
CMD ["bash"]
# Tue, 23 Nov 2021 20:21:03 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 23 Nov 2021 20:21:03 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr # buildkit
# Tue, 23 Nov 2021 20:21:03 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
# Tue, 23 Nov 2021 20:21:03 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
```

-	Layers:
	-	`sha256:1dfc643447ff7a82c599b429eda0d998c6dbad4ab2786eed580821b5b888204e`  
		Last Modified: Wed, 08 Jan 2025 03:46:41 GMT  
		Size: 28.0 MB (27994640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1fd38227c501a8e3a4c2ddbc366821c42ebe8fad426425d041d37315dd39d6b`  
		Last Modified: Fri, 21 Jun 2024 01:03:29 GMT  
		Size: 2.8 MB (2791746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69732935ca2831417791f9677707cd4ac5cce2cc5ceac6ccf0939905aa577562`  
		Last Modified: Fri, 21 Jun 2024 01:03:31 GMT  
		Size: 68.6 MB (68593059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af0ac94ccf1051dd80381d13771eba83828ecbdd644eca8d13963217a4fcad77`  
		Last Modified: Fri, 21 Jun 2024 02:02:45 GMT  
		Size: 131.4 MB (131428768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mono:6.10` - unknown; unknown

```console
$ docker pull mono@sha256:219a320599f64567f69e1dd47dcf68ea4ca8e9a382081f8459ea5df8f38492ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.0 MB (10997669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a69753b371d3937f23742ab4adf60505bc438fff530ce728a4cc8e30701256d`

```dockerfile
```

-	Layers:
	-	`sha256:9b3055c084df3c88817dd92cc8a2a1626a67e7926baf283baef3da5734e362cf`  
		Size: 11.0 MB (10990366 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7af35d4525a5846d4e984a6519b904a3595ee966a75f1a1f352401f5074bcc2`  
		Last Modified: Fri, 21 Jun 2024 02:02:42 GMT  
		Size: 7.3 KB (7303 bytes)  
		MIME: application/vnd.in-toto+json

### `mono:6.10` - linux; ppc64le

```console
$ docker pull mono@sha256:6126f0b2219e750b391e2e0d63ac7a2df863d9e2356c43fba06fee0708676038
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.7 MB (209715776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e4e952c22c47db9a79c5ca425c7de3d576d719e2042713424b88a3dae8e5129`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:04 GMT
ADD file:6d33ba25d3625e5f445fc2183b60c64e2cbc780cb541d7f8ac76ce193b311d13 in / 
# Tue, 02 Aug 2022 01:18:06 GMT
CMD ["bash"]
# Wed, 03 Aug 2022 02:08:58 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 03 Aug 2022 02:09:16 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 03 Aug 2022 02:09:49 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 03 Aug 2022 02:14:18 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:fc8842eebb7ccaf249b2bb2d6a3878fffdae26c9db8f23b393c7f76a6249d2f6`  
		Last Modified: Tue, 02 Aug 2022 01:25:45 GMT  
		Size: 30.6 MB (30560308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c0b96bc274eefbc8d34a02735b6f704f29aaf7e6c4095edb588a74c1ffb2825`  
		Last Modified: Wed, 03 Aug 2022 02:15:49 GMT  
		Size: 2.9 MB (2892610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7f103eac188d225f1b73fa0b0d6a3f2560c7fc46d7ec0f0e7e7a07330eb1ff0`  
		Last Modified: Wed, 03 Aug 2022 02:16:04 GMT  
		Size: 41.8 MB (41839360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3a64f5c66cdaf23afe83539fd8177bddc2e783d6ca6ee6eb3cabd08a6a5c375`  
		Last Modified: Wed, 03 Aug 2022 02:17:54 GMT  
		Size: 134.4 MB (134423498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.10-slim`

```console
$ docker pull mono@sha256:b6ff198d57023a6babe396421cbbebdbbb3cea331db3e02c1a2f7c677479ee4d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le

### `mono:6.10-slim` - linux; amd64

```console
$ docker pull mono@sha256:814dbcff677039e433ef2250b3f89b944e891faf2655a84e5fb9e24e832b20a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.7 MB (94681329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23a4fb2221d45ec07871359574d68e579e293dd9212fa65bb61dc818d9c79a73`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Nov 2021 20:21:03 GMT
ADD file:cce4de1623245f9f28e3365e6cf749d85dcfedddea2d6fbc963c309a40818f52 in / 
# Tue, 23 Nov 2021 20:21:03 GMT
CMD ["bash"]
# Tue, 23 Nov 2021 20:21:03 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 23 Nov 2021 20:21:03 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr # buildkit
# Tue, 23 Nov 2021 20:21:03 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
```

-	Layers:
	-	`sha256:b338562f40a7fb7360dfae935da6d7e40d2545db18bc461d9d70ec1b2b657f33`  
		Last Modified: Thu, 13 Jun 2024 01:26:49 GMT  
		Size: 27.3 MB (27337703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17858d27bab2d3cac617525d602bdb6430ef30203a5879d871c8ac9c5ed9ccc3`  
		Last Modified: Fri, 21 Jun 2024 01:03:10 GMT  
		Size: 2.8 MB (2780056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95304a756dfd5de0e2f44edffff0c73d65982f8523d664fd5f1d97ea84d3fba5`  
		Last Modified: Fri, 21 Jun 2024 01:03:11 GMT  
		Size: 64.6 MB (64563570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mono:6.10-slim` - unknown; unknown

```console
$ docker pull mono@sha256:491d5d49289d1b9a5bc4b07908d133d9cb48ef0683dcc08baefbf6f5811aff98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4132989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6ced6d0d7431bd499931fcee411750b9a8e9490f620918b716c506ac384aaa1`

```dockerfile
```

-	Layers:
	-	`sha256:f0b4de9e8b45105e3a7b5b7820ec78abe67d446be81e23c068710fa4467ce393`  
		Last Modified: Fri, 21 Jun 2024 01:03:10 GMT  
		Size: 4.1 MB (4123463 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fbb819f516836e26bb95911256c4b78f388e9c1de432e7a3639d7164f01e7d29`  
		Last Modified: Fri, 21 Jun 2024 01:03:10 GMT  
		Size: 9.5 KB (9526 bytes)  
		MIME: application/vnd.in-toto+json

### `mono:6.10-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:9d52e2f9db76c24f9964eec255de917d7a05b180e6e45f98545846b130400ab6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.9 MB (51879316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccac5ddbcee195ea38a9828f45d157f2ef674624fb9a6a2d5529fc2f8e6b736a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 00:49:37 GMT
ADD file:2ed7ca0d45c68b46a10ae186e8a03f98e72cadfeed17105668f53adf14d31e1f in / 
# Tue, 02 Aug 2022 00:49:38 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 07:18:54 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 01 Mar 2023 07:19:03 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 01 Mar 2023 07:19:22 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:187ecffbd1e0eae5de6567dff32bd58f28623635657779760c9d9539d6b7cc59`  
		Last Modified: Tue, 02 Aug 2022 00:57:06 GMT  
		Size: 24.9 MB (24889750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb25ee9d7e5ee2ba3d5fe6104206a45f2c5c425365a535e0aaac7bb9bd71034e`  
		Last Modified: Wed, 01 Mar 2023 07:23:36 GMT  
		Size: 2.5 MB (2467730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4b5b10e99353e19dd9c56deed1fd46d8ffc3c3eb2ad78b8d36ac029a085764e`  
		Last Modified: Wed, 01 Mar 2023 07:23:40 GMT  
		Size: 24.5 MB (24521836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:2e60489fe99a60254762f3286cf06072e2d9dba3b5a0d6e0b328472fa571e3e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48916402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f230905f863bc3230237c5db85203c793cd6de7910dd233f7eaf25acf60fccd`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Nov 2021 20:21:03 GMT
ADD file:ab786d88497f915679b3ac228e3bd805a58501dcb33b3d25e49cf1898770f9a7 in / 
# Tue, 23 Nov 2021 20:21:03 GMT
CMD ["bash"]
# Tue, 23 Nov 2021 20:21:03 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 23 Nov 2021 20:21:03 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr # buildkit
# Tue, 23 Nov 2021 20:21:03 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
```

-	Layers:
	-	`sha256:99d1ebcdd364332a1427098feecc8f94a8978ec971b171f7cca03bf01d1a149c`  
		Size: 22.9 MB (22944997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f82b184891ecf71303c14e6658ace46e95f5f157682da9b582cb967e9648c10d`  
		Size: 2.4 MB (2370004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0593643cc80b45c3e95e55271aebb7b5b474a3c444cff93983b44b2a84dafeae`  
		Last Modified: Fri, 21 Jun 2024 05:27:16 GMT  
		Size: 23.6 MB (23601401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mono:6.10-slim` - unknown; unknown

```console
$ docker pull mono@sha256:af9aa3d2e47127aab2e357a9ea276d08bdd273a6c5aaf87cd45400faf4f21a4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4042636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ade408cd408c024aa993519e25f634c616936284452679d9918877a93effd198`

```dockerfile
```

-	Layers:
	-	`sha256:8be89a42680753d1fc2276e6a396e95cea8773106f77e26aec995d0df0ca7a8c`  
		Last Modified: Fri, 21 Jun 2024 05:27:14 GMT  
		Size: 4.0 MB (4033035 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37aea1d9ffd12da273a2d239b6f7316eb3559a4d114eed112ff0adae18c136a8`  
		Last Modified: Fri, 21 Jun 2024 05:27:14 GMT  
		Size: 9.6 KB (9601 bytes)  
		MIME: application/vnd.in-toto+json

### `mono:6.10-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:05b52d0d590923d38d64ceadc102b859d43b753a0d0c2019d5b73c44c0f1364e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.1 MB (58112392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b9d5f21893447aad86e2f8a970a0f93bd8a334d4f5238f09d18d2404a10b2c2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Nov 2021 20:21:03 GMT
ADD file:de9a2b323e6d7d969277e7e781875e3daf3f49f2c1dcc569a1eec4f5bd789c46 in / 
# Tue, 23 Nov 2021 20:21:03 GMT
CMD ["bash"]
# Tue, 23 Nov 2021 20:21:03 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 23 Nov 2021 20:21:03 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr # buildkit
# Tue, 23 Nov 2021 20:21:03 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
```

-	Layers:
	-	`sha256:7abf9f73c7747bb840a8edcd895830e53f09498136de3015568a9cd9f5ab10ed`  
		Last Modified: Thu, 13 Jun 2024 00:44:26 GMT  
		Size: 26.1 MB (26109272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c486eb1fc96e8a0a90813bfa8a70b20adbe94ff7d89de75830366f1a316340fc`  
		Last Modified: Fri, 21 Jun 2024 07:35:43 GMT  
		Size: 2.6 MB (2644871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ace1bfdd6d06b8bfc35d8fa73745e008236ccb724d7a1b921904f981903a0d68`  
		Last Modified: Fri, 21 Jun 2024 07:35:44 GMT  
		Size: 29.4 MB (29358249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mono:6.10-slim` - unknown; unknown

```console
$ docker pull mono@sha256:cb6ea045039436a7ffb2b4a851e21d222a3ab50e16db14cba82f5b773ceb34ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4220679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ff7c5a78fe39004ae386eaf18040bfcb7814d94d8fdeb4d51423ec8154c9d50`

```dockerfile
```

-	Layers:
	-	`sha256:122244e8664114192b7f28265caef1f2123b2899783668e9222c20adcd2664a5`  
		Last Modified: Fri, 21 Jun 2024 07:35:43 GMT  
		Size: 4.2 MB (4210859 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32ed1c0c42cb60b60caf090d9b22e9a2ab0f6ae5d58ae3fedf7caceaaeb4a557`  
		Last Modified: Fri, 21 Jun 2024 07:35:43 GMT  
		Size: 9.8 KB (9820 bytes)  
		MIME: application/vnd.in-toto+json

### `mono:6.10-slim` - linux; 386

```console
$ docker pull mono@sha256:7e31f221c58cec452ee510c920dfbf8012b4ca33614cb6bc3d8d592e1ea87cfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.4 MB (99379445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89f170f621f13cadeb2e8c70c95a554eb5d0fda433dc2465673365d3d3d9b047`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Nov 2021 20:21:03 GMT
ADD file:7bc8fc617f718bf5e65e7fd718531a01122acc1783af5233c98aa9d31b0f093e in / 
# Tue, 23 Nov 2021 20:21:03 GMT
CMD ["bash"]
# Tue, 23 Nov 2021 20:21:03 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 23 Nov 2021 20:21:03 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr # buildkit
# Tue, 23 Nov 2021 20:21:03 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
```

-	Layers:
	-	`sha256:1dfc643447ff7a82c599b429eda0d998c6dbad4ab2786eed580821b5b888204e`  
		Last Modified: Wed, 08 Jan 2025 03:46:41 GMT  
		Size: 28.0 MB (27994640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1fd38227c501a8e3a4c2ddbc366821c42ebe8fad426425d041d37315dd39d6b`  
		Last Modified: Fri, 21 Jun 2024 01:03:29 GMT  
		Size: 2.8 MB (2791746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69732935ca2831417791f9677707cd4ac5cce2cc5ceac6ccf0939905aa577562`  
		Last Modified: Fri, 21 Jun 2024 01:03:31 GMT  
		Size: 68.6 MB (68593059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mono:6.10-slim` - unknown; unknown

```console
$ docker pull mono@sha256:af2cca3ede0f45937d1f08bea05e1e69c4ffa371a4c56eb56df016825486e19a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4129139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd3ff001a6d90676b013ef8d12dd787c62ec6e8d2b16046c50c0b07cfde1bfa6`

```dockerfile
```

-	Layers:
	-	`sha256:1ed57169d510571d116c2eb97578bcb8bc86e9f5a81d45fa519f2dcbf6a70c18`  
		Last Modified: Fri, 21 Jun 2024 01:03:29 GMT  
		Size: 4.1 MB (4119639 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:058644825e2ae60ddee3857e80f06301c1446a83d3108a8d7539f9337ec24f79`  
		Last Modified: Fri, 21 Jun 2024 01:03:29 GMT  
		Size: 9.5 KB (9500 bytes)  
		MIME: application/vnd.in-toto+json

### `mono:6.10-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:defa2f8c047d839e590b97fb1b9652e93b82414d17f8dea7279f1bc0f467fcf0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.3 MB (75292278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98e30e35a5de236a142e7288a3c84a86005d1c742b41498b3f75a9f26b3a76ca`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:04 GMT
ADD file:6d33ba25d3625e5f445fc2183b60c64e2cbc780cb541d7f8ac76ce193b311d13 in / 
# Tue, 02 Aug 2022 01:18:06 GMT
CMD ["bash"]
# Wed, 03 Aug 2022 02:08:58 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 03 Aug 2022 02:09:16 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 03 Aug 2022 02:09:49 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:fc8842eebb7ccaf249b2bb2d6a3878fffdae26c9db8f23b393c7f76a6249d2f6`  
		Last Modified: Tue, 02 Aug 2022 01:25:45 GMT  
		Size: 30.6 MB (30560308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c0b96bc274eefbc8d34a02735b6f704f29aaf7e6c4095edb588a74c1ffb2825`  
		Last Modified: Wed, 03 Aug 2022 02:15:49 GMT  
		Size: 2.9 MB (2892610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7f103eac188d225f1b73fa0b0d6a3f2560c7fc46d7ec0f0e7e7a07330eb1ff0`  
		Last Modified: Wed, 03 Aug 2022 02:16:04 GMT  
		Size: 41.8 MB (41839360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.10.0`

```console
$ docker pull mono@sha256:5b05ebda98b4e0e247a53e00c3748edc89dceeab763817999f0a6cfe37162e02
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le

### `mono:6.10.0` - linux; amd64

```console
$ docker pull mono@sha256:843c03721d4c4c3dc7df49913f7ec8b961da0b80934d7e2fc1ab386584503cf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.0 MB (224997323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:874411c91faac3f25999aad4273d41541fbfea71027283a4dbae8cb6bf804647`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Nov 2021 20:21:03 GMT
ADD file:cce4de1623245f9f28e3365e6cf749d85dcfedddea2d6fbc963c309a40818f52 in / 
# Tue, 23 Nov 2021 20:21:03 GMT
CMD ["bash"]
# Tue, 23 Nov 2021 20:21:03 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 23 Nov 2021 20:21:03 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr # buildkit
# Tue, 23 Nov 2021 20:21:03 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
# Tue, 23 Nov 2021 20:21:03 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
```

-	Layers:
	-	`sha256:b338562f40a7fb7360dfae935da6d7e40d2545db18bc461d9d70ec1b2b657f33`  
		Last Modified: Thu, 13 Jun 2024 01:26:49 GMT  
		Size: 27.3 MB (27337703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17858d27bab2d3cac617525d602bdb6430ef30203a5879d871c8ac9c5ed9ccc3`  
		Last Modified: Fri, 21 Jun 2024 01:03:10 GMT  
		Size: 2.8 MB (2780056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95304a756dfd5de0e2f44edffff0c73d65982f8523d664fd5f1d97ea84d3fba5`  
		Last Modified: Fri, 21 Jun 2024 01:03:11 GMT  
		Size: 64.6 MB (64563570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d38d92e81b89d82472ba771ba73bd96f9d7434d0a078d894095ba9332fedb7e4`  
		Last Modified: Fri, 21 Jun 2024 02:10:26 GMT  
		Size: 130.3 MB (130315994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mono:6.10.0` - unknown; unknown

```console
$ docker pull mono@sha256:f6671a285cbddce3760628595ffd4269c14d56576a01a7e1c1d9e0d22e9e3b52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.0 MB (11001689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:804b6302fcfc8892b5ad5455687216266c9950964c2ec1c967cc45dcd95365eb`

```dockerfile
```

-	Layers:
	-	`sha256:3f1bc3f47a2da7c663404a8b55db0810f54025932a6bfdbd60ed373988d5c3a3`  
		Last Modified: Fri, 21 Jun 2024 02:10:25 GMT  
		Size: 11.0 MB (10994359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bddb6bc492023a1217e6c5d5449b14b7a64e1659932a9e489d3eac1a6c8cbdb2`  
		Last Modified: Fri, 21 Jun 2024 02:10:24 GMT  
		Size: 7.3 KB (7330 bytes)  
		MIME: application/vnd.in-toto+json

### `mono:6.10.0` - linux; arm variant v5

```console
$ docker pull mono@sha256:5fd28ff75f47e10162fa8359e3457ed77e6a13c9eb64585df39efdf63e70a1a1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.9 MB (180861329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efa9d1dae1421f12f6f7eecf8cfaac5d7da3f6b99f6874365ce2f2f5fc9d9662`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 00:49:37 GMT
ADD file:2ed7ca0d45c68b46a10ae186e8a03f98e72cadfeed17105668f53adf14d31e1f in / 
# Tue, 02 Aug 2022 00:49:38 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 07:18:54 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 01 Mar 2023 07:19:03 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 01 Mar 2023 07:19:22 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 01 Mar 2023 07:22:13 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:187ecffbd1e0eae5de6567dff32bd58f28623635657779760c9d9539d6b7cc59`  
		Last Modified: Tue, 02 Aug 2022 00:57:06 GMT  
		Size: 24.9 MB (24889750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb25ee9d7e5ee2ba3d5fe6104206a45f2c5c425365a535e0aaac7bb9bd71034e`  
		Last Modified: Wed, 01 Mar 2023 07:23:36 GMT  
		Size: 2.5 MB (2467730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4b5b10e99353e19dd9c56deed1fd46d8ffc3c3eb2ad78b8d36ac029a085764e`  
		Last Modified: Wed, 01 Mar 2023 07:23:40 GMT  
		Size: 24.5 MB (24521836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75576104ae9839169a1957af7269a139e0be7d50d8cef2a4fe4011b528926e18`  
		Last Modified: Wed, 01 Mar 2023 07:25:04 GMT  
		Size: 129.0 MB (128982013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0` - linux; arm variant v7

```console
$ docker pull mono@sha256:b64c7fec47098f7cef6a337440933e17160202b129379df9d69709d368a9e4ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.7 MB (176724730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:706b8666526419ef5c72339aa6da41a1531a2451fc0f6f3c3b47aa597e3d1bf9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Nov 2021 20:21:03 GMT
ADD file:ab786d88497f915679b3ac228e3bd805a58501dcb33b3d25e49cf1898770f9a7 in / 
# Tue, 23 Nov 2021 20:21:03 GMT
CMD ["bash"]
# Tue, 23 Nov 2021 20:21:03 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 23 Nov 2021 20:21:03 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr # buildkit
# Tue, 23 Nov 2021 20:21:03 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
# Tue, 23 Nov 2021 20:21:03 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
```

-	Layers:
	-	`sha256:99d1ebcdd364332a1427098feecc8f94a8978ec971b171f7cca03bf01d1a149c`  
		Size: 22.9 MB (22944997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f82b184891ecf71303c14e6658ace46e95f5f157682da9b582cb967e9648c10d`  
		Size: 2.4 MB (2370004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0593643cc80b45c3e95e55271aebb7b5b474a3c444cff93983b44b2a84dafeae`  
		Last Modified: Fri, 21 Jun 2024 05:27:16 GMT  
		Size: 23.6 MB (23601401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f5da2a8951d66ec9b732a2291ad3fee626491fc08869d73bb850877aa7135f6`  
		Last Modified: Fri, 21 Jun 2024 13:18:42 GMT  
		Size: 127.8 MB (127808328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mono:6.10.0` - unknown; unknown

```console
$ docker pull mono@sha256:127701c9a8598ed4210ada06533b7a2a814bbf1668a53a6fd700eeb265417bcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10911546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce5c28342bce9abcfa397f21f9383ab304c6fcc24beda749f961319badf97c7d`

```dockerfile
```

-	Layers:
	-	`sha256:700ee908ff26cfb514951f19bc2ca97f1e8b7dcec561da7e3a8617b923ccace3`  
		Last Modified: Fri, 21 Jun 2024 13:18:39 GMT  
		Size: 10.9 MB (10904137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eca39222920792a108e34122757e88db4c17ce48dae31e3a423f1c69d039d4bd`  
		Last Modified: Fri, 21 Jun 2024 13:18:38 GMT  
		Size: 7.4 KB (7409 bytes)  
		MIME: application/vnd.in-toto+json

### `mono:6.10.0` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:d7c0737bfe98e3ea5ccdcd827b1acc4ffc40158eff330e229298454aa8263763
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.6 MB (203595079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2910c477dd60bc2f1053dc681f8d56d36a4b3512cca404a60e230718f6b485a8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Nov 2021 20:21:03 GMT
ADD file:de9a2b323e6d7d969277e7e781875e3daf3f49f2c1dcc569a1eec4f5bd789c46 in / 
# Tue, 23 Nov 2021 20:21:03 GMT
CMD ["bash"]
# Tue, 23 Nov 2021 20:21:03 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 23 Nov 2021 20:21:03 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr # buildkit
# Tue, 23 Nov 2021 20:21:03 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
# Tue, 23 Nov 2021 20:21:03 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
```

-	Layers:
	-	`sha256:7abf9f73c7747bb840a8edcd895830e53f09498136de3015568a9cd9f5ab10ed`  
		Last Modified: Thu, 13 Jun 2024 00:44:26 GMT  
		Size: 26.1 MB (26109272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c486eb1fc96e8a0a90813bfa8a70b20adbe94ff7d89de75830366f1a316340fc`  
		Last Modified: Fri, 21 Jun 2024 07:35:43 GMT  
		Size: 2.6 MB (2644871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ace1bfdd6d06b8bfc35d8fa73745e008236ccb724d7a1b921904f981903a0d68`  
		Last Modified: Fri, 21 Jun 2024 07:35:44 GMT  
		Size: 29.4 MB (29358249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1568d30ad91e8fe704c9799d461b35a06a344a8f88f2341179f5931eb8f409e`  
		Last Modified: Fri, 21 Jun 2024 17:12:27 GMT  
		Size: 145.5 MB (145482687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mono:6.10.0` - unknown; unknown

```console
$ docker pull mono@sha256:abfa7fa09981d22676e93c2590a9dadea0d36a6933ba87241bfca4190daea5c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11089541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46874ea2f565c3d4b2c7539eb7c4dd87650854ecad1c0491d702d1195eb0fc1e`

```dockerfile
```

-	Layers:
	-	`sha256:74ac47f39057ef5ffc07174295f77e6be6506ad0eece9418721ecea147466433`  
		Size: 11.1 MB (11081827 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1826670f27c4749b3087c12c4ab418cb4325b69292d42f3f91d398474b70c506`  
		Last Modified: Fri, 21 Jun 2024 17:12:23 GMT  
		Size: 7.7 KB (7714 bytes)  
		MIME: application/vnd.in-toto+json

### `mono:6.10.0` - linux; 386

```console
$ docker pull mono@sha256:1ff9e0605a84ebc9c1425cf380fa6538513957f14ff53668bb1415bc0de06276
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.8 MB (230808213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:165beb97a02082ea41ab2c93bf8061f5337e9c3e47d92a7c3fdbb3d91c05cf4f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Nov 2021 20:21:03 GMT
ADD file:7bc8fc617f718bf5e65e7fd718531a01122acc1783af5233c98aa9d31b0f093e in / 
# Tue, 23 Nov 2021 20:21:03 GMT
CMD ["bash"]
# Tue, 23 Nov 2021 20:21:03 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 23 Nov 2021 20:21:03 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr # buildkit
# Tue, 23 Nov 2021 20:21:03 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
# Tue, 23 Nov 2021 20:21:03 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
```

-	Layers:
	-	`sha256:1dfc643447ff7a82c599b429eda0d998c6dbad4ab2786eed580821b5b888204e`  
		Last Modified: Wed, 08 Jan 2025 03:46:41 GMT  
		Size: 28.0 MB (27994640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1fd38227c501a8e3a4c2ddbc366821c42ebe8fad426425d041d37315dd39d6b`  
		Last Modified: Fri, 21 Jun 2024 01:03:29 GMT  
		Size: 2.8 MB (2791746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69732935ca2831417791f9677707cd4ac5cce2cc5ceac6ccf0939905aa577562`  
		Last Modified: Fri, 21 Jun 2024 01:03:31 GMT  
		Size: 68.6 MB (68593059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af0ac94ccf1051dd80381d13771eba83828ecbdd644eca8d13963217a4fcad77`  
		Last Modified: Fri, 21 Jun 2024 02:02:45 GMT  
		Size: 131.4 MB (131428768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mono:6.10.0` - unknown; unknown

```console
$ docker pull mono@sha256:219a320599f64567f69e1dd47dcf68ea4ca8e9a382081f8459ea5df8f38492ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.0 MB (10997669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a69753b371d3937f23742ab4adf60505bc438fff530ce728a4cc8e30701256d`

```dockerfile
```

-	Layers:
	-	`sha256:9b3055c084df3c88817dd92cc8a2a1626a67e7926baf283baef3da5734e362cf`  
		Size: 11.0 MB (10990366 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7af35d4525a5846d4e984a6519b904a3595ee966a75f1a1f352401f5074bcc2`  
		Last Modified: Fri, 21 Jun 2024 02:02:42 GMT  
		Size: 7.3 KB (7303 bytes)  
		MIME: application/vnd.in-toto+json

### `mono:6.10.0` - linux; ppc64le

```console
$ docker pull mono@sha256:6126f0b2219e750b391e2e0d63ac7a2df863d9e2356c43fba06fee0708676038
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.7 MB (209715776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e4e952c22c47db9a79c5ca425c7de3d576d719e2042713424b88a3dae8e5129`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:04 GMT
ADD file:6d33ba25d3625e5f445fc2183b60c64e2cbc780cb541d7f8ac76ce193b311d13 in / 
# Tue, 02 Aug 2022 01:18:06 GMT
CMD ["bash"]
# Wed, 03 Aug 2022 02:08:58 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 03 Aug 2022 02:09:16 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 03 Aug 2022 02:09:49 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 03 Aug 2022 02:14:18 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:fc8842eebb7ccaf249b2bb2d6a3878fffdae26c9db8f23b393c7f76a6249d2f6`  
		Last Modified: Tue, 02 Aug 2022 01:25:45 GMT  
		Size: 30.6 MB (30560308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c0b96bc274eefbc8d34a02735b6f704f29aaf7e6c4095edb588a74c1ffb2825`  
		Last Modified: Wed, 03 Aug 2022 02:15:49 GMT  
		Size: 2.9 MB (2892610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7f103eac188d225f1b73fa0b0d6a3f2560c7fc46d7ec0f0e7e7a07330eb1ff0`  
		Last Modified: Wed, 03 Aug 2022 02:16:04 GMT  
		Size: 41.8 MB (41839360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3a64f5c66cdaf23afe83539fd8177bddc2e783d6ca6ee6eb3cabd08a6a5c375`  
		Last Modified: Wed, 03 Aug 2022 02:17:54 GMT  
		Size: 134.4 MB (134423498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.10.0-slim`

```console
$ docker pull mono@sha256:b6ff198d57023a6babe396421cbbebdbbb3cea331db3e02c1a2f7c677479ee4d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le

### `mono:6.10.0-slim` - linux; amd64

```console
$ docker pull mono@sha256:814dbcff677039e433ef2250b3f89b944e891faf2655a84e5fb9e24e832b20a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.7 MB (94681329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23a4fb2221d45ec07871359574d68e579e293dd9212fa65bb61dc818d9c79a73`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Nov 2021 20:21:03 GMT
ADD file:cce4de1623245f9f28e3365e6cf749d85dcfedddea2d6fbc963c309a40818f52 in / 
# Tue, 23 Nov 2021 20:21:03 GMT
CMD ["bash"]
# Tue, 23 Nov 2021 20:21:03 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 23 Nov 2021 20:21:03 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr # buildkit
# Tue, 23 Nov 2021 20:21:03 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
```

-	Layers:
	-	`sha256:b338562f40a7fb7360dfae935da6d7e40d2545db18bc461d9d70ec1b2b657f33`  
		Last Modified: Thu, 13 Jun 2024 01:26:49 GMT  
		Size: 27.3 MB (27337703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17858d27bab2d3cac617525d602bdb6430ef30203a5879d871c8ac9c5ed9ccc3`  
		Last Modified: Fri, 21 Jun 2024 01:03:10 GMT  
		Size: 2.8 MB (2780056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95304a756dfd5de0e2f44edffff0c73d65982f8523d664fd5f1d97ea84d3fba5`  
		Last Modified: Fri, 21 Jun 2024 01:03:11 GMT  
		Size: 64.6 MB (64563570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mono:6.10.0-slim` - unknown; unknown

```console
$ docker pull mono@sha256:491d5d49289d1b9a5bc4b07908d133d9cb48ef0683dcc08baefbf6f5811aff98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4132989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6ced6d0d7431bd499931fcee411750b9a8e9490f620918b716c506ac384aaa1`

```dockerfile
```

-	Layers:
	-	`sha256:f0b4de9e8b45105e3a7b5b7820ec78abe67d446be81e23c068710fa4467ce393`  
		Last Modified: Fri, 21 Jun 2024 01:03:10 GMT  
		Size: 4.1 MB (4123463 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fbb819f516836e26bb95911256c4b78f388e9c1de432e7a3639d7164f01e7d29`  
		Last Modified: Fri, 21 Jun 2024 01:03:10 GMT  
		Size: 9.5 KB (9526 bytes)  
		MIME: application/vnd.in-toto+json

### `mono:6.10.0-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:9d52e2f9db76c24f9964eec255de917d7a05b180e6e45f98545846b130400ab6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.9 MB (51879316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccac5ddbcee195ea38a9828f45d157f2ef674624fb9a6a2d5529fc2f8e6b736a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 00:49:37 GMT
ADD file:2ed7ca0d45c68b46a10ae186e8a03f98e72cadfeed17105668f53adf14d31e1f in / 
# Tue, 02 Aug 2022 00:49:38 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 07:18:54 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 01 Mar 2023 07:19:03 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 01 Mar 2023 07:19:22 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:187ecffbd1e0eae5de6567dff32bd58f28623635657779760c9d9539d6b7cc59`  
		Last Modified: Tue, 02 Aug 2022 00:57:06 GMT  
		Size: 24.9 MB (24889750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb25ee9d7e5ee2ba3d5fe6104206a45f2c5c425365a535e0aaac7bb9bd71034e`  
		Last Modified: Wed, 01 Mar 2023 07:23:36 GMT  
		Size: 2.5 MB (2467730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4b5b10e99353e19dd9c56deed1fd46d8ffc3c3eb2ad78b8d36ac029a085764e`  
		Last Modified: Wed, 01 Mar 2023 07:23:40 GMT  
		Size: 24.5 MB (24521836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:2e60489fe99a60254762f3286cf06072e2d9dba3b5a0d6e0b328472fa571e3e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48916402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f230905f863bc3230237c5db85203c793cd6de7910dd233f7eaf25acf60fccd`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Nov 2021 20:21:03 GMT
ADD file:ab786d88497f915679b3ac228e3bd805a58501dcb33b3d25e49cf1898770f9a7 in / 
# Tue, 23 Nov 2021 20:21:03 GMT
CMD ["bash"]
# Tue, 23 Nov 2021 20:21:03 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 23 Nov 2021 20:21:03 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr # buildkit
# Tue, 23 Nov 2021 20:21:03 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
```

-	Layers:
	-	`sha256:99d1ebcdd364332a1427098feecc8f94a8978ec971b171f7cca03bf01d1a149c`  
		Size: 22.9 MB (22944997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f82b184891ecf71303c14e6658ace46e95f5f157682da9b582cb967e9648c10d`  
		Size: 2.4 MB (2370004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0593643cc80b45c3e95e55271aebb7b5b474a3c444cff93983b44b2a84dafeae`  
		Last Modified: Fri, 21 Jun 2024 05:27:16 GMT  
		Size: 23.6 MB (23601401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mono:6.10.0-slim` - unknown; unknown

```console
$ docker pull mono@sha256:af9aa3d2e47127aab2e357a9ea276d08bdd273a6c5aaf87cd45400faf4f21a4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4042636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ade408cd408c024aa993519e25f634c616936284452679d9918877a93effd198`

```dockerfile
```

-	Layers:
	-	`sha256:8be89a42680753d1fc2276e6a396e95cea8773106f77e26aec995d0df0ca7a8c`  
		Last Modified: Fri, 21 Jun 2024 05:27:14 GMT  
		Size: 4.0 MB (4033035 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37aea1d9ffd12da273a2d239b6f7316eb3559a4d114eed112ff0adae18c136a8`  
		Last Modified: Fri, 21 Jun 2024 05:27:14 GMT  
		Size: 9.6 KB (9601 bytes)  
		MIME: application/vnd.in-toto+json

### `mono:6.10.0-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:05b52d0d590923d38d64ceadc102b859d43b753a0d0c2019d5b73c44c0f1364e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.1 MB (58112392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b9d5f21893447aad86e2f8a970a0f93bd8a334d4f5238f09d18d2404a10b2c2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Nov 2021 20:21:03 GMT
ADD file:de9a2b323e6d7d969277e7e781875e3daf3f49f2c1dcc569a1eec4f5bd789c46 in / 
# Tue, 23 Nov 2021 20:21:03 GMT
CMD ["bash"]
# Tue, 23 Nov 2021 20:21:03 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 23 Nov 2021 20:21:03 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr # buildkit
# Tue, 23 Nov 2021 20:21:03 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
```

-	Layers:
	-	`sha256:7abf9f73c7747bb840a8edcd895830e53f09498136de3015568a9cd9f5ab10ed`  
		Last Modified: Thu, 13 Jun 2024 00:44:26 GMT  
		Size: 26.1 MB (26109272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c486eb1fc96e8a0a90813bfa8a70b20adbe94ff7d89de75830366f1a316340fc`  
		Last Modified: Fri, 21 Jun 2024 07:35:43 GMT  
		Size: 2.6 MB (2644871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ace1bfdd6d06b8bfc35d8fa73745e008236ccb724d7a1b921904f981903a0d68`  
		Last Modified: Fri, 21 Jun 2024 07:35:44 GMT  
		Size: 29.4 MB (29358249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mono:6.10.0-slim` - unknown; unknown

```console
$ docker pull mono@sha256:cb6ea045039436a7ffb2b4a851e21d222a3ab50e16db14cba82f5b773ceb34ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4220679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ff7c5a78fe39004ae386eaf18040bfcb7814d94d8fdeb4d51423ec8154c9d50`

```dockerfile
```

-	Layers:
	-	`sha256:122244e8664114192b7f28265caef1f2123b2899783668e9222c20adcd2664a5`  
		Last Modified: Fri, 21 Jun 2024 07:35:43 GMT  
		Size: 4.2 MB (4210859 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32ed1c0c42cb60b60caf090d9b22e9a2ab0f6ae5d58ae3fedf7caceaaeb4a557`  
		Last Modified: Fri, 21 Jun 2024 07:35:43 GMT  
		Size: 9.8 KB (9820 bytes)  
		MIME: application/vnd.in-toto+json

### `mono:6.10.0-slim` - linux; 386

```console
$ docker pull mono@sha256:7e31f221c58cec452ee510c920dfbf8012b4ca33614cb6bc3d8d592e1ea87cfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.4 MB (99379445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89f170f621f13cadeb2e8c70c95a554eb5d0fda433dc2465673365d3d3d9b047`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Nov 2021 20:21:03 GMT
ADD file:7bc8fc617f718bf5e65e7fd718531a01122acc1783af5233c98aa9d31b0f093e in / 
# Tue, 23 Nov 2021 20:21:03 GMT
CMD ["bash"]
# Tue, 23 Nov 2021 20:21:03 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 23 Nov 2021 20:21:03 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr # buildkit
# Tue, 23 Nov 2021 20:21:03 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
```

-	Layers:
	-	`sha256:1dfc643447ff7a82c599b429eda0d998c6dbad4ab2786eed580821b5b888204e`  
		Last Modified: Wed, 08 Jan 2025 03:46:41 GMT  
		Size: 28.0 MB (27994640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1fd38227c501a8e3a4c2ddbc366821c42ebe8fad426425d041d37315dd39d6b`  
		Last Modified: Fri, 21 Jun 2024 01:03:29 GMT  
		Size: 2.8 MB (2791746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69732935ca2831417791f9677707cd4ac5cce2cc5ceac6ccf0939905aa577562`  
		Last Modified: Fri, 21 Jun 2024 01:03:31 GMT  
		Size: 68.6 MB (68593059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mono:6.10.0-slim` - unknown; unknown

```console
$ docker pull mono@sha256:af2cca3ede0f45937d1f08bea05e1e69c4ffa371a4c56eb56df016825486e19a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4129139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd3ff001a6d90676b013ef8d12dd787c62ec6e8d2b16046c50c0b07cfde1bfa6`

```dockerfile
```

-	Layers:
	-	`sha256:1ed57169d510571d116c2eb97578bcb8bc86e9f5a81d45fa519f2dcbf6a70c18`  
		Last Modified: Fri, 21 Jun 2024 01:03:29 GMT  
		Size: 4.1 MB (4119639 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:058644825e2ae60ddee3857e80f06301c1446a83d3108a8d7539f9337ec24f79`  
		Last Modified: Fri, 21 Jun 2024 01:03:29 GMT  
		Size: 9.5 KB (9500 bytes)  
		MIME: application/vnd.in-toto+json

### `mono:6.10.0-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:defa2f8c047d839e590b97fb1b9652e93b82414d17f8dea7279f1bc0f467fcf0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.3 MB (75292278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98e30e35a5de236a142e7288a3c84a86005d1c742b41498b3f75a9f26b3a76ca`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:04 GMT
ADD file:6d33ba25d3625e5f445fc2183b60c64e2cbc780cb541d7f8ac76ce193b311d13 in / 
# Tue, 02 Aug 2022 01:18:06 GMT
CMD ["bash"]
# Wed, 03 Aug 2022 02:08:58 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 03 Aug 2022 02:09:16 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 03 Aug 2022 02:09:49 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:fc8842eebb7ccaf249b2bb2d6a3878fffdae26c9db8f23b393c7f76a6249d2f6`  
		Last Modified: Tue, 02 Aug 2022 01:25:45 GMT  
		Size: 30.6 MB (30560308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c0b96bc274eefbc8d34a02735b6f704f29aaf7e6c4095edb588a74c1ffb2825`  
		Last Modified: Wed, 03 Aug 2022 02:15:49 GMT  
		Size: 2.9 MB (2892610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7f103eac188d225f1b73fa0b0d6a3f2560c7fc46d7ec0f0e7e7a07330eb1ff0`  
		Last Modified: Wed, 03 Aug 2022 02:16:04 GMT  
		Size: 41.8 MB (41839360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.10.0.104`

```console
$ docker pull mono@sha256:5b05ebda98b4e0e247a53e00c3748edc89dceeab763817999f0a6cfe37162e02
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le

### `mono:6.10.0.104` - linux; amd64

```console
$ docker pull mono@sha256:843c03721d4c4c3dc7df49913f7ec8b961da0b80934d7e2fc1ab386584503cf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.0 MB (224997323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:874411c91faac3f25999aad4273d41541fbfea71027283a4dbae8cb6bf804647`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Nov 2021 20:21:03 GMT
ADD file:cce4de1623245f9f28e3365e6cf749d85dcfedddea2d6fbc963c309a40818f52 in / 
# Tue, 23 Nov 2021 20:21:03 GMT
CMD ["bash"]
# Tue, 23 Nov 2021 20:21:03 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 23 Nov 2021 20:21:03 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr # buildkit
# Tue, 23 Nov 2021 20:21:03 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
# Tue, 23 Nov 2021 20:21:03 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
```

-	Layers:
	-	`sha256:b338562f40a7fb7360dfae935da6d7e40d2545db18bc461d9d70ec1b2b657f33`  
		Last Modified: Thu, 13 Jun 2024 01:26:49 GMT  
		Size: 27.3 MB (27337703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17858d27bab2d3cac617525d602bdb6430ef30203a5879d871c8ac9c5ed9ccc3`  
		Last Modified: Fri, 21 Jun 2024 01:03:10 GMT  
		Size: 2.8 MB (2780056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95304a756dfd5de0e2f44edffff0c73d65982f8523d664fd5f1d97ea84d3fba5`  
		Last Modified: Fri, 21 Jun 2024 01:03:11 GMT  
		Size: 64.6 MB (64563570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d38d92e81b89d82472ba771ba73bd96f9d7434d0a078d894095ba9332fedb7e4`  
		Last Modified: Fri, 21 Jun 2024 02:10:26 GMT  
		Size: 130.3 MB (130315994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mono:6.10.0.104` - unknown; unknown

```console
$ docker pull mono@sha256:f6671a285cbddce3760628595ffd4269c14d56576a01a7e1c1d9e0d22e9e3b52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.0 MB (11001689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:804b6302fcfc8892b5ad5455687216266c9950964c2ec1c967cc45dcd95365eb`

```dockerfile
```

-	Layers:
	-	`sha256:3f1bc3f47a2da7c663404a8b55db0810f54025932a6bfdbd60ed373988d5c3a3`  
		Last Modified: Fri, 21 Jun 2024 02:10:25 GMT  
		Size: 11.0 MB (10994359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bddb6bc492023a1217e6c5d5449b14b7a64e1659932a9e489d3eac1a6c8cbdb2`  
		Last Modified: Fri, 21 Jun 2024 02:10:24 GMT  
		Size: 7.3 KB (7330 bytes)  
		MIME: application/vnd.in-toto+json

### `mono:6.10.0.104` - linux; arm variant v5

```console
$ docker pull mono@sha256:5fd28ff75f47e10162fa8359e3457ed77e6a13c9eb64585df39efdf63e70a1a1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.9 MB (180861329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efa9d1dae1421f12f6f7eecf8cfaac5d7da3f6b99f6874365ce2f2f5fc9d9662`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 00:49:37 GMT
ADD file:2ed7ca0d45c68b46a10ae186e8a03f98e72cadfeed17105668f53adf14d31e1f in / 
# Tue, 02 Aug 2022 00:49:38 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 07:18:54 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 01 Mar 2023 07:19:03 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 01 Mar 2023 07:19:22 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 01 Mar 2023 07:22:13 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:187ecffbd1e0eae5de6567dff32bd58f28623635657779760c9d9539d6b7cc59`  
		Last Modified: Tue, 02 Aug 2022 00:57:06 GMT  
		Size: 24.9 MB (24889750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb25ee9d7e5ee2ba3d5fe6104206a45f2c5c425365a535e0aaac7bb9bd71034e`  
		Last Modified: Wed, 01 Mar 2023 07:23:36 GMT  
		Size: 2.5 MB (2467730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4b5b10e99353e19dd9c56deed1fd46d8ffc3c3eb2ad78b8d36ac029a085764e`  
		Last Modified: Wed, 01 Mar 2023 07:23:40 GMT  
		Size: 24.5 MB (24521836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75576104ae9839169a1957af7269a139e0be7d50d8cef2a4fe4011b528926e18`  
		Last Modified: Wed, 01 Mar 2023 07:25:04 GMT  
		Size: 129.0 MB (128982013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0.104` - linux; arm variant v7

```console
$ docker pull mono@sha256:b64c7fec47098f7cef6a337440933e17160202b129379df9d69709d368a9e4ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.7 MB (176724730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:706b8666526419ef5c72339aa6da41a1531a2451fc0f6f3c3b47aa597e3d1bf9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Nov 2021 20:21:03 GMT
ADD file:ab786d88497f915679b3ac228e3bd805a58501dcb33b3d25e49cf1898770f9a7 in / 
# Tue, 23 Nov 2021 20:21:03 GMT
CMD ["bash"]
# Tue, 23 Nov 2021 20:21:03 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 23 Nov 2021 20:21:03 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr # buildkit
# Tue, 23 Nov 2021 20:21:03 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
# Tue, 23 Nov 2021 20:21:03 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
```

-	Layers:
	-	`sha256:99d1ebcdd364332a1427098feecc8f94a8978ec971b171f7cca03bf01d1a149c`  
		Size: 22.9 MB (22944997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f82b184891ecf71303c14e6658ace46e95f5f157682da9b582cb967e9648c10d`  
		Size: 2.4 MB (2370004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0593643cc80b45c3e95e55271aebb7b5b474a3c444cff93983b44b2a84dafeae`  
		Last Modified: Fri, 21 Jun 2024 05:27:16 GMT  
		Size: 23.6 MB (23601401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f5da2a8951d66ec9b732a2291ad3fee626491fc08869d73bb850877aa7135f6`  
		Last Modified: Fri, 21 Jun 2024 13:18:42 GMT  
		Size: 127.8 MB (127808328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mono:6.10.0.104` - unknown; unknown

```console
$ docker pull mono@sha256:127701c9a8598ed4210ada06533b7a2a814bbf1668a53a6fd700eeb265417bcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10911546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce5c28342bce9abcfa397f21f9383ab304c6fcc24beda749f961319badf97c7d`

```dockerfile
```

-	Layers:
	-	`sha256:700ee908ff26cfb514951f19bc2ca97f1e8b7dcec561da7e3a8617b923ccace3`  
		Last Modified: Fri, 21 Jun 2024 13:18:39 GMT  
		Size: 10.9 MB (10904137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eca39222920792a108e34122757e88db4c17ce48dae31e3a423f1c69d039d4bd`  
		Last Modified: Fri, 21 Jun 2024 13:18:38 GMT  
		Size: 7.4 KB (7409 bytes)  
		MIME: application/vnd.in-toto+json

### `mono:6.10.0.104` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:d7c0737bfe98e3ea5ccdcd827b1acc4ffc40158eff330e229298454aa8263763
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.6 MB (203595079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2910c477dd60bc2f1053dc681f8d56d36a4b3512cca404a60e230718f6b485a8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Nov 2021 20:21:03 GMT
ADD file:de9a2b323e6d7d969277e7e781875e3daf3f49f2c1dcc569a1eec4f5bd789c46 in / 
# Tue, 23 Nov 2021 20:21:03 GMT
CMD ["bash"]
# Tue, 23 Nov 2021 20:21:03 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 23 Nov 2021 20:21:03 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr # buildkit
# Tue, 23 Nov 2021 20:21:03 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
# Tue, 23 Nov 2021 20:21:03 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
```

-	Layers:
	-	`sha256:7abf9f73c7747bb840a8edcd895830e53f09498136de3015568a9cd9f5ab10ed`  
		Last Modified: Thu, 13 Jun 2024 00:44:26 GMT  
		Size: 26.1 MB (26109272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c486eb1fc96e8a0a90813bfa8a70b20adbe94ff7d89de75830366f1a316340fc`  
		Last Modified: Fri, 21 Jun 2024 07:35:43 GMT  
		Size: 2.6 MB (2644871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ace1bfdd6d06b8bfc35d8fa73745e008236ccb724d7a1b921904f981903a0d68`  
		Last Modified: Fri, 21 Jun 2024 07:35:44 GMT  
		Size: 29.4 MB (29358249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1568d30ad91e8fe704c9799d461b35a06a344a8f88f2341179f5931eb8f409e`  
		Last Modified: Fri, 21 Jun 2024 17:12:27 GMT  
		Size: 145.5 MB (145482687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mono:6.10.0.104` - unknown; unknown

```console
$ docker pull mono@sha256:abfa7fa09981d22676e93c2590a9dadea0d36a6933ba87241bfca4190daea5c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11089541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46874ea2f565c3d4b2c7539eb7c4dd87650854ecad1c0491d702d1195eb0fc1e`

```dockerfile
```

-	Layers:
	-	`sha256:74ac47f39057ef5ffc07174295f77e6be6506ad0eece9418721ecea147466433`  
		Size: 11.1 MB (11081827 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1826670f27c4749b3087c12c4ab418cb4325b69292d42f3f91d398474b70c506`  
		Last Modified: Fri, 21 Jun 2024 17:12:23 GMT  
		Size: 7.7 KB (7714 bytes)  
		MIME: application/vnd.in-toto+json

### `mono:6.10.0.104` - linux; 386

```console
$ docker pull mono@sha256:1ff9e0605a84ebc9c1425cf380fa6538513957f14ff53668bb1415bc0de06276
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.8 MB (230808213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:165beb97a02082ea41ab2c93bf8061f5337e9c3e47d92a7c3fdbb3d91c05cf4f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Nov 2021 20:21:03 GMT
ADD file:7bc8fc617f718bf5e65e7fd718531a01122acc1783af5233c98aa9d31b0f093e in / 
# Tue, 23 Nov 2021 20:21:03 GMT
CMD ["bash"]
# Tue, 23 Nov 2021 20:21:03 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 23 Nov 2021 20:21:03 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr # buildkit
# Tue, 23 Nov 2021 20:21:03 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
# Tue, 23 Nov 2021 20:21:03 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
```

-	Layers:
	-	`sha256:1dfc643447ff7a82c599b429eda0d998c6dbad4ab2786eed580821b5b888204e`  
		Last Modified: Wed, 08 Jan 2025 03:46:41 GMT  
		Size: 28.0 MB (27994640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1fd38227c501a8e3a4c2ddbc366821c42ebe8fad426425d041d37315dd39d6b`  
		Last Modified: Fri, 21 Jun 2024 01:03:29 GMT  
		Size: 2.8 MB (2791746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69732935ca2831417791f9677707cd4ac5cce2cc5ceac6ccf0939905aa577562`  
		Last Modified: Fri, 21 Jun 2024 01:03:31 GMT  
		Size: 68.6 MB (68593059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af0ac94ccf1051dd80381d13771eba83828ecbdd644eca8d13963217a4fcad77`  
		Last Modified: Fri, 21 Jun 2024 02:02:45 GMT  
		Size: 131.4 MB (131428768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mono:6.10.0.104` - unknown; unknown

```console
$ docker pull mono@sha256:219a320599f64567f69e1dd47dcf68ea4ca8e9a382081f8459ea5df8f38492ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.0 MB (10997669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a69753b371d3937f23742ab4adf60505bc438fff530ce728a4cc8e30701256d`

```dockerfile
```

-	Layers:
	-	`sha256:9b3055c084df3c88817dd92cc8a2a1626a67e7926baf283baef3da5734e362cf`  
		Size: 11.0 MB (10990366 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7af35d4525a5846d4e984a6519b904a3595ee966a75f1a1f352401f5074bcc2`  
		Last Modified: Fri, 21 Jun 2024 02:02:42 GMT  
		Size: 7.3 KB (7303 bytes)  
		MIME: application/vnd.in-toto+json

### `mono:6.10.0.104` - linux; ppc64le

```console
$ docker pull mono@sha256:6126f0b2219e750b391e2e0d63ac7a2df863d9e2356c43fba06fee0708676038
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.7 MB (209715776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e4e952c22c47db9a79c5ca425c7de3d576d719e2042713424b88a3dae8e5129`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:04 GMT
ADD file:6d33ba25d3625e5f445fc2183b60c64e2cbc780cb541d7f8ac76ce193b311d13 in / 
# Tue, 02 Aug 2022 01:18:06 GMT
CMD ["bash"]
# Wed, 03 Aug 2022 02:08:58 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 03 Aug 2022 02:09:16 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 03 Aug 2022 02:09:49 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 03 Aug 2022 02:14:18 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:fc8842eebb7ccaf249b2bb2d6a3878fffdae26c9db8f23b393c7f76a6249d2f6`  
		Last Modified: Tue, 02 Aug 2022 01:25:45 GMT  
		Size: 30.6 MB (30560308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c0b96bc274eefbc8d34a02735b6f704f29aaf7e6c4095edb588a74c1ffb2825`  
		Last Modified: Wed, 03 Aug 2022 02:15:49 GMT  
		Size: 2.9 MB (2892610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7f103eac188d225f1b73fa0b0d6a3f2560c7fc46d7ec0f0e7e7a07330eb1ff0`  
		Last Modified: Wed, 03 Aug 2022 02:16:04 GMT  
		Size: 41.8 MB (41839360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3a64f5c66cdaf23afe83539fd8177bddc2e783d6ca6ee6eb3cabd08a6a5c375`  
		Last Modified: Wed, 03 Aug 2022 02:17:54 GMT  
		Size: 134.4 MB (134423498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.10.0.104-slim`

```console
$ docker pull mono@sha256:b6ff198d57023a6babe396421cbbebdbbb3cea331db3e02c1a2f7c677479ee4d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le

### `mono:6.10.0.104-slim` - linux; amd64

```console
$ docker pull mono@sha256:814dbcff677039e433ef2250b3f89b944e891faf2655a84e5fb9e24e832b20a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.7 MB (94681329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23a4fb2221d45ec07871359574d68e579e293dd9212fa65bb61dc818d9c79a73`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Nov 2021 20:21:03 GMT
ADD file:cce4de1623245f9f28e3365e6cf749d85dcfedddea2d6fbc963c309a40818f52 in / 
# Tue, 23 Nov 2021 20:21:03 GMT
CMD ["bash"]
# Tue, 23 Nov 2021 20:21:03 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 23 Nov 2021 20:21:03 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr # buildkit
# Tue, 23 Nov 2021 20:21:03 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
```

-	Layers:
	-	`sha256:b338562f40a7fb7360dfae935da6d7e40d2545db18bc461d9d70ec1b2b657f33`  
		Last Modified: Thu, 13 Jun 2024 01:26:49 GMT  
		Size: 27.3 MB (27337703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17858d27bab2d3cac617525d602bdb6430ef30203a5879d871c8ac9c5ed9ccc3`  
		Last Modified: Fri, 21 Jun 2024 01:03:10 GMT  
		Size: 2.8 MB (2780056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95304a756dfd5de0e2f44edffff0c73d65982f8523d664fd5f1d97ea84d3fba5`  
		Last Modified: Fri, 21 Jun 2024 01:03:11 GMT  
		Size: 64.6 MB (64563570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mono:6.10.0.104-slim` - unknown; unknown

```console
$ docker pull mono@sha256:491d5d49289d1b9a5bc4b07908d133d9cb48ef0683dcc08baefbf6f5811aff98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4132989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6ced6d0d7431bd499931fcee411750b9a8e9490f620918b716c506ac384aaa1`

```dockerfile
```

-	Layers:
	-	`sha256:f0b4de9e8b45105e3a7b5b7820ec78abe67d446be81e23c068710fa4467ce393`  
		Last Modified: Fri, 21 Jun 2024 01:03:10 GMT  
		Size: 4.1 MB (4123463 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fbb819f516836e26bb95911256c4b78f388e9c1de432e7a3639d7164f01e7d29`  
		Last Modified: Fri, 21 Jun 2024 01:03:10 GMT  
		Size: 9.5 KB (9526 bytes)  
		MIME: application/vnd.in-toto+json

### `mono:6.10.0.104-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:9d52e2f9db76c24f9964eec255de917d7a05b180e6e45f98545846b130400ab6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.9 MB (51879316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccac5ddbcee195ea38a9828f45d157f2ef674624fb9a6a2d5529fc2f8e6b736a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 00:49:37 GMT
ADD file:2ed7ca0d45c68b46a10ae186e8a03f98e72cadfeed17105668f53adf14d31e1f in / 
# Tue, 02 Aug 2022 00:49:38 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 07:18:54 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 01 Mar 2023 07:19:03 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 01 Mar 2023 07:19:22 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:187ecffbd1e0eae5de6567dff32bd58f28623635657779760c9d9539d6b7cc59`  
		Last Modified: Tue, 02 Aug 2022 00:57:06 GMT  
		Size: 24.9 MB (24889750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb25ee9d7e5ee2ba3d5fe6104206a45f2c5c425365a535e0aaac7bb9bd71034e`  
		Last Modified: Wed, 01 Mar 2023 07:23:36 GMT  
		Size: 2.5 MB (2467730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4b5b10e99353e19dd9c56deed1fd46d8ffc3c3eb2ad78b8d36ac029a085764e`  
		Last Modified: Wed, 01 Mar 2023 07:23:40 GMT  
		Size: 24.5 MB (24521836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0.104-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:2e60489fe99a60254762f3286cf06072e2d9dba3b5a0d6e0b328472fa571e3e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48916402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f230905f863bc3230237c5db85203c793cd6de7910dd233f7eaf25acf60fccd`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Nov 2021 20:21:03 GMT
ADD file:ab786d88497f915679b3ac228e3bd805a58501dcb33b3d25e49cf1898770f9a7 in / 
# Tue, 23 Nov 2021 20:21:03 GMT
CMD ["bash"]
# Tue, 23 Nov 2021 20:21:03 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 23 Nov 2021 20:21:03 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr # buildkit
# Tue, 23 Nov 2021 20:21:03 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
```

-	Layers:
	-	`sha256:99d1ebcdd364332a1427098feecc8f94a8978ec971b171f7cca03bf01d1a149c`  
		Size: 22.9 MB (22944997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f82b184891ecf71303c14e6658ace46e95f5f157682da9b582cb967e9648c10d`  
		Size: 2.4 MB (2370004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0593643cc80b45c3e95e55271aebb7b5b474a3c444cff93983b44b2a84dafeae`  
		Last Modified: Fri, 21 Jun 2024 05:27:16 GMT  
		Size: 23.6 MB (23601401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mono:6.10.0.104-slim` - unknown; unknown

```console
$ docker pull mono@sha256:af9aa3d2e47127aab2e357a9ea276d08bdd273a6c5aaf87cd45400faf4f21a4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4042636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ade408cd408c024aa993519e25f634c616936284452679d9918877a93effd198`

```dockerfile
```

-	Layers:
	-	`sha256:8be89a42680753d1fc2276e6a396e95cea8773106f77e26aec995d0df0ca7a8c`  
		Last Modified: Fri, 21 Jun 2024 05:27:14 GMT  
		Size: 4.0 MB (4033035 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37aea1d9ffd12da273a2d239b6f7316eb3559a4d114eed112ff0adae18c136a8`  
		Last Modified: Fri, 21 Jun 2024 05:27:14 GMT  
		Size: 9.6 KB (9601 bytes)  
		MIME: application/vnd.in-toto+json

### `mono:6.10.0.104-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:05b52d0d590923d38d64ceadc102b859d43b753a0d0c2019d5b73c44c0f1364e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.1 MB (58112392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b9d5f21893447aad86e2f8a970a0f93bd8a334d4f5238f09d18d2404a10b2c2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Nov 2021 20:21:03 GMT
ADD file:de9a2b323e6d7d969277e7e781875e3daf3f49f2c1dcc569a1eec4f5bd789c46 in / 
# Tue, 23 Nov 2021 20:21:03 GMT
CMD ["bash"]
# Tue, 23 Nov 2021 20:21:03 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 23 Nov 2021 20:21:03 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr # buildkit
# Tue, 23 Nov 2021 20:21:03 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
```

-	Layers:
	-	`sha256:7abf9f73c7747bb840a8edcd895830e53f09498136de3015568a9cd9f5ab10ed`  
		Last Modified: Thu, 13 Jun 2024 00:44:26 GMT  
		Size: 26.1 MB (26109272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c486eb1fc96e8a0a90813bfa8a70b20adbe94ff7d89de75830366f1a316340fc`  
		Last Modified: Fri, 21 Jun 2024 07:35:43 GMT  
		Size: 2.6 MB (2644871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ace1bfdd6d06b8bfc35d8fa73745e008236ccb724d7a1b921904f981903a0d68`  
		Last Modified: Fri, 21 Jun 2024 07:35:44 GMT  
		Size: 29.4 MB (29358249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mono:6.10.0.104-slim` - unknown; unknown

```console
$ docker pull mono@sha256:cb6ea045039436a7ffb2b4a851e21d222a3ab50e16db14cba82f5b773ceb34ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4220679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ff7c5a78fe39004ae386eaf18040bfcb7814d94d8fdeb4d51423ec8154c9d50`

```dockerfile
```

-	Layers:
	-	`sha256:122244e8664114192b7f28265caef1f2123b2899783668e9222c20adcd2664a5`  
		Last Modified: Fri, 21 Jun 2024 07:35:43 GMT  
		Size: 4.2 MB (4210859 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32ed1c0c42cb60b60caf090d9b22e9a2ab0f6ae5d58ae3fedf7caceaaeb4a557`  
		Last Modified: Fri, 21 Jun 2024 07:35:43 GMT  
		Size: 9.8 KB (9820 bytes)  
		MIME: application/vnd.in-toto+json

### `mono:6.10.0.104-slim` - linux; 386

```console
$ docker pull mono@sha256:7e31f221c58cec452ee510c920dfbf8012b4ca33614cb6bc3d8d592e1ea87cfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.4 MB (99379445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89f170f621f13cadeb2e8c70c95a554eb5d0fda433dc2465673365d3d3d9b047`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Nov 2021 20:21:03 GMT
ADD file:7bc8fc617f718bf5e65e7fd718531a01122acc1783af5233c98aa9d31b0f093e in / 
# Tue, 23 Nov 2021 20:21:03 GMT
CMD ["bash"]
# Tue, 23 Nov 2021 20:21:03 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 23 Nov 2021 20:21:03 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr # buildkit
# Tue, 23 Nov 2021 20:21:03 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
```

-	Layers:
	-	`sha256:1dfc643447ff7a82c599b429eda0d998c6dbad4ab2786eed580821b5b888204e`  
		Last Modified: Wed, 08 Jan 2025 03:46:41 GMT  
		Size: 28.0 MB (27994640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1fd38227c501a8e3a4c2ddbc366821c42ebe8fad426425d041d37315dd39d6b`  
		Last Modified: Fri, 21 Jun 2024 01:03:29 GMT  
		Size: 2.8 MB (2791746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69732935ca2831417791f9677707cd4ac5cce2cc5ceac6ccf0939905aa577562`  
		Last Modified: Fri, 21 Jun 2024 01:03:31 GMT  
		Size: 68.6 MB (68593059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mono:6.10.0.104-slim` - unknown; unknown

```console
$ docker pull mono@sha256:af2cca3ede0f45937d1f08bea05e1e69c4ffa371a4c56eb56df016825486e19a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4129139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd3ff001a6d90676b013ef8d12dd787c62ec6e8d2b16046c50c0b07cfde1bfa6`

```dockerfile
```

-	Layers:
	-	`sha256:1ed57169d510571d116c2eb97578bcb8bc86e9f5a81d45fa519f2dcbf6a70c18`  
		Last Modified: Fri, 21 Jun 2024 01:03:29 GMT  
		Size: 4.1 MB (4119639 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:058644825e2ae60ddee3857e80f06301c1446a83d3108a8d7539f9337ec24f79`  
		Last Modified: Fri, 21 Jun 2024 01:03:29 GMT  
		Size: 9.5 KB (9500 bytes)  
		MIME: application/vnd.in-toto+json

### `mono:6.10.0.104-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:defa2f8c047d839e590b97fb1b9652e93b82414d17f8dea7279f1bc0f467fcf0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.3 MB (75292278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98e30e35a5de236a142e7288a3c84a86005d1c742b41498b3f75a9f26b3a76ca`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:04 GMT
ADD file:6d33ba25d3625e5f445fc2183b60c64e2cbc780cb541d7f8ac76ce193b311d13 in / 
# Tue, 02 Aug 2022 01:18:06 GMT
CMD ["bash"]
# Wed, 03 Aug 2022 02:08:58 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 03 Aug 2022 02:09:16 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 03 Aug 2022 02:09:49 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:fc8842eebb7ccaf249b2bb2d6a3878fffdae26c9db8f23b393c7f76a6249d2f6`  
		Last Modified: Tue, 02 Aug 2022 01:25:45 GMT  
		Size: 30.6 MB (30560308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c0b96bc274eefbc8d34a02735b6f704f29aaf7e6c4095edb588a74c1ffb2825`  
		Last Modified: Wed, 03 Aug 2022 02:15:49 GMT  
		Size: 2.9 MB (2892610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7f103eac188d225f1b73fa0b0d6a3f2560c7fc46d7ec0f0e7e7a07330eb1ff0`  
		Last Modified: Wed, 03 Aug 2022 02:16:04 GMT  
		Size: 41.8 MB (41839360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.12`

```console
$ docker pull mono@sha256:34d816779b1248b5cfd095770b64ecbaf1798e2aca693a91c11a018dce9c7ad5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le

### `mono:6.12` - linux; amd64

```console
$ docker pull mono@sha256:d2ae1881a608fb6401bcebbf0d444fc2fcadf0db27f07c87153a79e7b14e861a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.6 MB (254589877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16d98cfcc673531288833a5cdb9f87087aa18082d1fed9ebe02021c67b1fdf0f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jun 2022 16:43:21 GMT
ADD file:cce4de1623245f9f28e3365e6cf749d85dcfedddea2d6fbc963c309a40818f52 in / 
# Wed, 22 Jun 2022 16:43:21 GMT
CMD ["bash"]
# Wed, 22 Jun 2022 16:43:21 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 22 Jun 2022 16:43:21 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr # buildkit
# Wed, 22 Jun 2022 16:43:21 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
# Wed, 22 Jun 2022 16:43:21 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
```

-	Layers:
	-	`sha256:b338562f40a7fb7360dfae935da6d7e40d2545db18bc461d9d70ec1b2b657f33`  
		Last Modified: Thu, 13 Jun 2024 01:26:49 GMT  
		Size: 27.3 MB (27337703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b1b752ddf75c64e105424fb16f5a2053ddad33f059e3be8e520e35908cc4e97`  
		Last Modified: Fri, 21 Jun 2024 01:03:10 GMT  
		Size: 2.8 MB (2780035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d574eb224b5ddbe14656e28913cf5eeb5b14aa651aa3bcb9288aa43f1000aec5`  
		Last Modified: Fri, 21 Jun 2024 01:03:11 GMT  
		Size: 64.6 MB (64555923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb9d6fb145c5367510a78273891d0ba84d7257b0bfdf3cd340f4e3d6f211de0a`  
		Last Modified: Fri, 21 Jun 2024 02:02:49 GMT  
		Size: 159.9 MB (159916216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mono:6.12` - unknown; unknown

```console
$ docker pull mono@sha256:fc661c46136b8f9cbe60f721c811fb05d600f7614c9ddef8306ca5a261a6ea24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11085967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6322617bf4f258627a38887597f3d55cd3e73d36de6aa5f4734d1d6fcd3e7fd9`

```dockerfile
```

-	Layers:
	-	`sha256:08c2cae238c884d7e44ae9bd57336a51412c9603e15025c0a456eca7dd888aba`  
		Last Modified: Fri, 21 Jun 2024 02:02:46 GMT  
		Size: 11.1 MB (11078059 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2dda4ada58791fac758ee1dc7c9ee2756a6d55125463cc11427657bfedecb286`  
		Last Modified: Fri, 21 Jun 2024 02:02:46 GMT  
		Size: 7.9 KB (7908 bytes)  
		MIME: application/vnd.in-toto+json

### `mono:6.12` - linux; arm variant v5

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

### `mono:6.12` - linux; arm variant v7

```console
$ docker pull mono@sha256:bb330a955d4e30fc342e6a770e76253662e2ab4eaf51dbb51f988815f6b28f29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.9 MB (188935459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d07296a48da608d892f2dcc9928236339e8eaedab5e92f1a0bb2cb73c9a1693e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jun 2022 16:43:21 GMT
ADD file:ab786d88497f915679b3ac228e3bd805a58501dcb33b3d25e49cf1898770f9a7 in / 
# Wed, 22 Jun 2022 16:43:21 GMT
CMD ["bash"]
# Wed, 22 Jun 2022 16:43:21 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 22 Jun 2022 16:43:21 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr # buildkit
# Wed, 22 Jun 2022 16:43:21 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
# Wed, 22 Jun 2022 16:43:21 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
```

-	Layers:
	-	`sha256:99d1ebcdd364332a1427098feecc8f94a8978ec971b171f7cca03bf01d1a149c`  
		Size: 22.9 MB (22944997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47de34cd92203a1c44adc48be4330b559dcef9e18da3b5babab329d0fd26e11f`  
		Last Modified: Fri, 21 Jun 2024 05:26:04 GMT  
		Size: 2.4 MB (2370028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14dae79eba6437cf8f1fe8c17653348408d9b42ad8948d93472bbffd86792d7b`  
		Last Modified: Fri, 21 Jun 2024 05:26:05 GMT  
		Size: 23.6 MB (23573077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f623ef7b096557bbf700a18c1f6616fa36cfb781282427c32b42ee2bf6f5d788`  
		Last Modified: Fri, 21 Jun 2024 13:15:11 GMT  
		Size: 140.0 MB (140047357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mono:6.12` - unknown; unknown

```console
$ docker pull mono@sha256:85360b79dd6fd6383cee0bf95518112f77c11353aaa15ab291ba68db619e15ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.0 MB (10995859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2bed6a6671ce784ea5373b029adbbe3d4b3b1ff7a8f59eed60bb7fed2baee0e`

```dockerfile
```

-	Layers:
	-	`sha256:a2750707e64721db5673f1d8443493f0a94e552993057b314e46f727642deefe`  
		Last Modified: Fri, 21 Jun 2024 13:15:08 GMT  
		Size: 11.0 MB (10987855 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:626e6cbf5e9f3aba334705529601969366e52b1b76d405943e486e844d7bbfea`  
		Last Modified: Fri, 21 Jun 2024 13:15:07 GMT  
		Size: 8.0 KB (8004 bytes)  
		MIME: application/vnd.in-toto+json

### `mono:6.12` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:5b876dc42dbdf92201a17d179906d941011b64493b32ce09d0d1faf12f470361
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.3 MB (216300519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bbe627177b284938a13b85f3505e07a72c220eeae1d6d4b9a675687f4a9f9be`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jun 2022 16:43:21 GMT
ADD file:de9a2b323e6d7d969277e7e781875e3daf3f49f2c1dcc569a1eec4f5bd789c46 in / 
# Wed, 22 Jun 2022 16:43:21 GMT
CMD ["bash"]
# Wed, 22 Jun 2022 16:43:21 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 22 Jun 2022 16:43:21 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr # buildkit
# Wed, 22 Jun 2022 16:43:21 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
# Wed, 22 Jun 2022 16:43:21 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
```

-	Layers:
	-	`sha256:7abf9f73c7747bb840a8edcd895830e53f09498136de3015568a9cd9f5ab10ed`  
		Last Modified: Thu, 13 Jun 2024 00:44:26 GMT  
		Size: 26.1 MB (26109272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eedc96c6829dd818687f02719ed29ee02b62d29b93d260a87cbfdf65bd82307`  
		Last Modified: Fri, 21 Jun 2024 07:34:59 GMT  
		Size: 2.6 MB (2644870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc18ec37f21948c54422a8a2bd31634ae80dc4cd7d1f82b12857c17ad3e4aeec`  
		Size: 29.3 MB (29329348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a97a948909451f0ef002b4ce1035b5a09a3acde1633d198b1b7d25d6729f696`  
		Last Modified: Fri, 21 Jun 2024 17:09:25 GMT  
		Size: 158.2 MB (158217029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mono:6.12` - unknown; unknown

```console
$ docker pull mono@sha256:06f899f1f0a8c6a50d0cccbe9f415f29eb3eb9dba67e1076050fb7fa3214bc38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.2 MB (11173870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0a16765ae4b4d709f200047ad778fd0e6b25c0149b15eeb60dff4320acaf196`

```dockerfile
```

-	Layers:
	-	`sha256:3d8ff956fff2b5ea5a8f2a0f26101974ab6b290a4863020c141f56ce0ff86582`  
		Last Modified: Fri, 21 Jun 2024 17:09:17 GMT  
		Size: 11.2 MB (11165553 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0812c62e6dd0b6028ef0d86e34492bdbb20ebf6bae746864504d4121912d4cba`  
		Last Modified: Fri, 21 Jun 2024 17:09:16 GMT  
		Size: 8.3 KB (8317 bytes)  
		MIME: application/vnd.in-toto+json

### `mono:6.12` - linux; 386

```console
$ docker pull mono@sha256:8f10891be25745681bd6f98bf48e1234094816dc4b5dbef73d48f53f67536601
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.5 MB (259458549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2775d67ed2568bc292fd99d9a4c6e6e31195ae5382d5d3f1d76cb0f034c34e5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jun 2022 16:43:21 GMT
ADD file:7bc8fc617f718bf5e65e7fd718531a01122acc1783af5233c98aa9d31b0f093e in / 
# Wed, 22 Jun 2022 16:43:21 GMT
CMD ["bash"]
# Wed, 22 Jun 2022 16:43:21 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 22 Jun 2022 16:43:21 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr # buildkit
# Wed, 22 Jun 2022 16:43:21 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
# Wed, 22 Jun 2022 16:43:21 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
```

-	Layers:
	-	`sha256:1dfc643447ff7a82c599b429eda0d998c6dbad4ab2786eed580821b5b888204e`  
		Last Modified: Wed, 08 Jan 2025 03:46:41 GMT  
		Size: 28.0 MB (27994640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a198cb1aaae91cef3ed2eaed184c0a10f0b74e857bd5ea91dcde2955746f20f9`  
		Last Modified: Wed, 08 Jan 2025 03:46:41 GMT  
		Size: 2.8 MB (2791765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd658841b3e1b2084a6340e82f84033bf765e9ea9830350aa5a4aba88cbf3166`  
		Last Modified: Fri, 21 Jun 2024 01:03:14 GMT  
		Size: 68.6 MB (68585515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30bbf7033252959af4d7a4d2f468bba517cf0aeaf9f9e131902187bdc9737e6d`  
		Last Modified: Fri, 21 Jun 2024 02:04:03 GMT  
		Size: 160.1 MB (160086629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mono:6.12` - unknown; unknown

```console
$ docker pull mono@sha256:e69c4a0ff0efcd311f3ec0da7e72cbafaa9689b8555686674db7d3d689e13230
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11081926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48b0f05b8c3e2ec0bdb3fcbf2f85778a7584ea1dfd621e838399e99f0e6aac47`

```dockerfile
```

-	Layers:
	-	`sha256:f5bc84e8ea570b2500296b1f25f4226e60f0c15178c4ed81b09fa2c5ddf35fc6`  
		Last Modified: Fri, 21 Jun 2024 02:03:58 GMT  
		Size: 11.1 MB (11074056 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f11f469c7181081a082c334f89f2885f7a6a0953d5e152e5f75db2af4504d80e`  
		Last Modified: Fri, 21 Jun 2024 02:03:57 GMT  
		Size: 7.9 KB (7870 bytes)  
		MIME: application/vnd.in-toto+json

### `mono:6.12` - linux; ppc64le

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

## `mono:6.12-slim`

```console
$ docker pull mono@sha256:eb9a8d42dc58090cdb0d39b36422d9560f33e9d2cce22f4c888da263cee46c45
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le

### `mono:6.12-slim` - linux; amd64

```console
$ docker pull mono@sha256:749851d74745492754d1ebb3c50fc335d4b84a7bb34e17a4e7c3909c5ec1212b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.7 MB (94673661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5a2a70110040ee175a00069fa147d036d49deb2decd03a6374e83da337706e8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jun 2022 16:43:21 GMT
ADD file:cce4de1623245f9f28e3365e6cf749d85dcfedddea2d6fbc963c309a40818f52 in / 
# Wed, 22 Jun 2022 16:43:21 GMT
CMD ["bash"]
# Wed, 22 Jun 2022 16:43:21 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 22 Jun 2022 16:43:21 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr # buildkit
# Wed, 22 Jun 2022 16:43:21 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
```

-	Layers:
	-	`sha256:b338562f40a7fb7360dfae935da6d7e40d2545db18bc461d9d70ec1b2b657f33`  
		Last Modified: Thu, 13 Jun 2024 01:26:49 GMT  
		Size: 27.3 MB (27337703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b1b752ddf75c64e105424fb16f5a2053ddad33f059e3be8e520e35908cc4e97`  
		Last Modified: Fri, 21 Jun 2024 01:03:10 GMT  
		Size: 2.8 MB (2780035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d574eb224b5ddbe14656e28913cf5eeb5b14aa651aa3bcb9288aa43f1000aec5`  
		Last Modified: Fri, 21 Jun 2024 01:03:11 GMT  
		Size: 64.6 MB (64555923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mono:6.12-slim` - unknown; unknown

```console
$ docker pull mono@sha256:5a8421c386b586f98034983cc67448394e910e05ff857862418296991eddcf54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4134119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7daf4a5e106256a64c61c2f6e62ec4e5aa7020398e1b40c8bbe8b4e7458bec8d`

```dockerfile
```

-	Layers:
	-	`sha256:68c0c6a6586378e1af3fd618d65a15dd0a69c3e36744d2db3c2a64b91f8842b8`  
		Last Modified: Fri, 21 Jun 2024 01:03:10 GMT  
		Size: 4.1 MB (4124009 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ec35e37e8929d1729d15f72eaafb529c88604e0eb2b568452d3927312850835`  
		Last Modified: Fri, 21 Jun 2024 01:03:10 GMT  
		Size: 10.1 KB (10110 bytes)  
		MIME: application/vnd.in-toto+json

### `mono:6.12-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:f7c133539fa6a4add7484e9c93bc9b62ec32236d4b619f320c20b3248fb4739a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.9 MB (51860964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe52652f149ceedc89ed0c0f70985fcd898b6cd5cc98aa6f99f9ca06fd83046c`
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

### `mono:6.12-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:dd07ed6527eaa5860d31d50e7a3c5521b6f559eed9822aeeeb8667ce8390e378
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48888102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f645d1e48f0116b7141165a6952885d2f77e3033c87231c6d63152270ffd7a33`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jun 2022 16:43:21 GMT
ADD file:ab786d88497f915679b3ac228e3bd805a58501dcb33b3d25e49cf1898770f9a7 in / 
# Wed, 22 Jun 2022 16:43:21 GMT
CMD ["bash"]
# Wed, 22 Jun 2022 16:43:21 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 22 Jun 2022 16:43:21 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr # buildkit
# Wed, 22 Jun 2022 16:43:21 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
```

-	Layers:
	-	`sha256:99d1ebcdd364332a1427098feecc8f94a8978ec971b171f7cca03bf01d1a149c`  
		Size: 22.9 MB (22944997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47de34cd92203a1c44adc48be4330b559dcef9e18da3b5babab329d0fd26e11f`  
		Last Modified: Fri, 21 Jun 2024 05:26:04 GMT  
		Size: 2.4 MB (2370028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14dae79eba6437cf8f1fe8c17653348408d9b42ad8948d93472bbffd86792d7b`  
		Last Modified: Fri, 21 Jun 2024 05:26:05 GMT  
		Size: 23.6 MB (23573077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mono:6.12-slim` - unknown; unknown

```console
$ docker pull mono@sha256:ee35f615c2629a07e18483c6e85d7a3c83498ec7a51d34e09c6831e8720ee843
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4043799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e77739a150c122ee693247b621455e84030503770aa1098a0d6e90ae5d11efea`

```dockerfile
```

-	Layers:
	-	`sha256:e211386d3756bb307e96a299f301c5ef1eb874182b4c4a9e23f63b9ae5388ec3`  
		Last Modified: Fri, 21 Jun 2024 05:26:05 GMT  
		Size: 4.0 MB (4033599 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78feeadf8c15b58b8ecdee782634016d91ad2995f88bccaf8f187a8adc6ef4ff`  
		Last Modified: Fri, 21 Jun 2024 05:26:04 GMT  
		Size: 10.2 KB (10200 bytes)  
		MIME: application/vnd.in-toto+json

### `mono:6.12-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:f8ca545da29ef84d991bc3713b7284fcee5344a8e73eac40567bfefcf7de4a20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.1 MB (58083490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:337ba12936b175b1f418a4a2fb20db97d206faf71ca52fd475c94ac4d3993a3e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jun 2022 16:43:21 GMT
ADD file:de9a2b323e6d7d969277e7e781875e3daf3f49f2c1dcc569a1eec4f5bd789c46 in / 
# Wed, 22 Jun 2022 16:43:21 GMT
CMD ["bash"]
# Wed, 22 Jun 2022 16:43:21 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 22 Jun 2022 16:43:21 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr # buildkit
# Wed, 22 Jun 2022 16:43:21 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
```

-	Layers:
	-	`sha256:7abf9f73c7747bb840a8edcd895830e53f09498136de3015568a9cd9f5ab10ed`  
		Last Modified: Thu, 13 Jun 2024 00:44:26 GMT  
		Size: 26.1 MB (26109272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eedc96c6829dd818687f02719ed29ee02b62d29b93d260a87cbfdf65bd82307`  
		Last Modified: Fri, 21 Jun 2024 07:34:59 GMT  
		Size: 2.6 MB (2644870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc18ec37f21948c54422a8a2bd31634ae80dc4cd7d1f82b12857c17ad3e4aeec`  
		Size: 29.3 MB (29329348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mono:6.12-slim` - unknown; unknown

```console
$ docker pull mono@sha256:cd9b48412dc563b39c0103943d5ed3cbc90b60a7c49d51e07903e020b8cfb981
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4221860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fefffedbcde83d1d79c60cf414a8e8472225ffa87437cbd87ed93cbcde2840f2`

```dockerfile
```

-	Layers:
	-	`sha256:681a9485d68b8e56f7c721e96ecc685811a344e8356bab9dcbb7ed283fc771a4`  
		Last Modified: Fri, 21 Jun 2024 07:34:59 GMT  
		Size: 4.2 MB (4211431 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a953520626886eee4ff5675e5962fcd17b1795c5421161e5d957486e675fec3b`  
		Last Modified: Fri, 21 Jun 2024 07:34:58 GMT  
		Size: 10.4 KB (10429 bytes)  
		MIME: application/vnd.in-toto+json

### `mono:6.12-slim` - linux; 386

```console
$ docker pull mono@sha256:819bc68ca415cdb49ad461b4afb9a27004e442878b2bbdefc8a67317bc5b2ddf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.4 MB (99371920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c360bfbb224cb22cd13ba52ccd63bc77562ef28647c535cd0a42518f0773a842`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jun 2022 16:43:21 GMT
ADD file:7bc8fc617f718bf5e65e7fd718531a01122acc1783af5233c98aa9d31b0f093e in / 
# Wed, 22 Jun 2022 16:43:21 GMT
CMD ["bash"]
# Wed, 22 Jun 2022 16:43:21 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 22 Jun 2022 16:43:21 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr # buildkit
# Wed, 22 Jun 2022 16:43:21 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
```

-	Layers:
	-	`sha256:1dfc643447ff7a82c599b429eda0d998c6dbad4ab2786eed580821b5b888204e`  
		Last Modified: Wed, 08 Jan 2025 03:46:41 GMT  
		Size: 28.0 MB (27994640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a198cb1aaae91cef3ed2eaed184c0a10f0b74e857bd5ea91dcde2955746f20f9`  
		Last Modified: Wed, 08 Jan 2025 03:46:41 GMT  
		Size: 2.8 MB (2791765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd658841b3e1b2084a6340e82f84033bf765e9ea9830350aa5a4aba88cbf3166`  
		Last Modified: Fri, 21 Jun 2024 01:03:14 GMT  
		Size: 68.6 MB (68585515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mono:6.12-slim` - unknown; unknown

```console
$ docker pull mono@sha256:21b839469b89df687807ffdd3f870708c16efa44a6b299510e9d6391ba6499fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4130249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80ef153a1ce2f246cf50247bdbe0e53a65f2eca1f65498fe5be40b5242f5f8b1`

```dockerfile
```

-	Layers:
	-	`sha256:053ce445b27e3a8e224b16a3d2a8cdc9dc1d84ebee53d08de3d37ec36d5de95c`  
		Size: 4.1 MB (4120175 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:190e2c58614be0d956b94cdc868f9beb77c2f2d8ef16c981339f2b2c23f56975`  
		Last Modified: Fri, 21 Jun 2024 01:03:12 GMT  
		Size: 10.1 KB (10074 bytes)  
		MIME: application/vnd.in-toto+json

### `mono:6.12-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:b83383e51874bbee097571b303be3299c87d7da8c4c6b0f4e067cfaa552ad925
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75350311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c28d9c810a28445dd3b5767c5be8a3a5c5f459f859498e49f59bb419b735510`
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

## `mono:6.12.0`

```console
$ docker pull mono@sha256:34d816779b1248b5cfd095770b64ecbaf1798e2aca693a91c11a018dce9c7ad5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le

### `mono:6.12.0` - linux; amd64

```console
$ docker pull mono@sha256:d2ae1881a608fb6401bcebbf0d444fc2fcadf0db27f07c87153a79e7b14e861a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.6 MB (254589877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16d98cfcc673531288833a5cdb9f87087aa18082d1fed9ebe02021c67b1fdf0f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jun 2022 16:43:21 GMT
ADD file:cce4de1623245f9f28e3365e6cf749d85dcfedddea2d6fbc963c309a40818f52 in / 
# Wed, 22 Jun 2022 16:43:21 GMT
CMD ["bash"]
# Wed, 22 Jun 2022 16:43:21 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 22 Jun 2022 16:43:21 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr # buildkit
# Wed, 22 Jun 2022 16:43:21 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
# Wed, 22 Jun 2022 16:43:21 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
```

-	Layers:
	-	`sha256:b338562f40a7fb7360dfae935da6d7e40d2545db18bc461d9d70ec1b2b657f33`  
		Last Modified: Thu, 13 Jun 2024 01:26:49 GMT  
		Size: 27.3 MB (27337703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b1b752ddf75c64e105424fb16f5a2053ddad33f059e3be8e520e35908cc4e97`  
		Last Modified: Fri, 21 Jun 2024 01:03:10 GMT  
		Size: 2.8 MB (2780035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d574eb224b5ddbe14656e28913cf5eeb5b14aa651aa3bcb9288aa43f1000aec5`  
		Last Modified: Fri, 21 Jun 2024 01:03:11 GMT  
		Size: 64.6 MB (64555923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb9d6fb145c5367510a78273891d0ba84d7257b0bfdf3cd340f4e3d6f211de0a`  
		Last Modified: Fri, 21 Jun 2024 02:02:49 GMT  
		Size: 159.9 MB (159916216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mono:6.12.0` - unknown; unknown

```console
$ docker pull mono@sha256:fc661c46136b8f9cbe60f721c811fb05d600f7614c9ddef8306ca5a261a6ea24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11085967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6322617bf4f258627a38887597f3d55cd3e73d36de6aa5f4734d1d6fcd3e7fd9`

```dockerfile
```

-	Layers:
	-	`sha256:08c2cae238c884d7e44ae9bd57336a51412c9603e15025c0a456eca7dd888aba`  
		Last Modified: Fri, 21 Jun 2024 02:02:46 GMT  
		Size: 11.1 MB (11078059 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2dda4ada58791fac758ee1dc7c9ee2756a6d55125463cc11427657bfedecb286`  
		Last Modified: Fri, 21 Jun 2024 02:02:46 GMT  
		Size: 7.9 KB (7908 bytes)  
		MIME: application/vnd.in-toto+json

### `mono:6.12.0` - linux; arm variant v5

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

### `mono:6.12.0` - linux; arm variant v7

```console
$ docker pull mono@sha256:bb330a955d4e30fc342e6a770e76253662e2ab4eaf51dbb51f988815f6b28f29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.9 MB (188935459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d07296a48da608d892f2dcc9928236339e8eaedab5e92f1a0bb2cb73c9a1693e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jun 2022 16:43:21 GMT
ADD file:ab786d88497f915679b3ac228e3bd805a58501dcb33b3d25e49cf1898770f9a7 in / 
# Wed, 22 Jun 2022 16:43:21 GMT
CMD ["bash"]
# Wed, 22 Jun 2022 16:43:21 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 22 Jun 2022 16:43:21 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr # buildkit
# Wed, 22 Jun 2022 16:43:21 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
# Wed, 22 Jun 2022 16:43:21 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
```

-	Layers:
	-	`sha256:99d1ebcdd364332a1427098feecc8f94a8978ec971b171f7cca03bf01d1a149c`  
		Size: 22.9 MB (22944997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47de34cd92203a1c44adc48be4330b559dcef9e18da3b5babab329d0fd26e11f`  
		Last Modified: Fri, 21 Jun 2024 05:26:04 GMT  
		Size: 2.4 MB (2370028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14dae79eba6437cf8f1fe8c17653348408d9b42ad8948d93472bbffd86792d7b`  
		Last Modified: Fri, 21 Jun 2024 05:26:05 GMT  
		Size: 23.6 MB (23573077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f623ef7b096557bbf700a18c1f6616fa36cfb781282427c32b42ee2bf6f5d788`  
		Last Modified: Fri, 21 Jun 2024 13:15:11 GMT  
		Size: 140.0 MB (140047357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mono:6.12.0` - unknown; unknown

```console
$ docker pull mono@sha256:85360b79dd6fd6383cee0bf95518112f77c11353aaa15ab291ba68db619e15ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.0 MB (10995859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2bed6a6671ce784ea5373b029adbbe3d4b3b1ff7a8f59eed60bb7fed2baee0e`

```dockerfile
```

-	Layers:
	-	`sha256:a2750707e64721db5673f1d8443493f0a94e552993057b314e46f727642deefe`  
		Last Modified: Fri, 21 Jun 2024 13:15:08 GMT  
		Size: 11.0 MB (10987855 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:626e6cbf5e9f3aba334705529601969366e52b1b76d405943e486e844d7bbfea`  
		Last Modified: Fri, 21 Jun 2024 13:15:07 GMT  
		Size: 8.0 KB (8004 bytes)  
		MIME: application/vnd.in-toto+json

### `mono:6.12.0` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:5b876dc42dbdf92201a17d179906d941011b64493b32ce09d0d1faf12f470361
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.3 MB (216300519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bbe627177b284938a13b85f3505e07a72c220eeae1d6d4b9a675687f4a9f9be`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jun 2022 16:43:21 GMT
ADD file:de9a2b323e6d7d969277e7e781875e3daf3f49f2c1dcc569a1eec4f5bd789c46 in / 
# Wed, 22 Jun 2022 16:43:21 GMT
CMD ["bash"]
# Wed, 22 Jun 2022 16:43:21 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 22 Jun 2022 16:43:21 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr # buildkit
# Wed, 22 Jun 2022 16:43:21 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
# Wed, 22 Jun 2022 16:43:21 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
```

-	Layers:
	-	`sha256:7abf9f73c7747bb840a8edcd895830e53f09498136de3015568a9cd9f5ab10ed`  
		Last Modified: Thu, 13 Jun 2024 00:44:26 GMT  
		Size: 26.1 MB (26109272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eedc96c6829dd818687f02719ed29ee02b62d29b93d260a87cbfdf65bd82307`  
		Last Modified: Fri, 21 Jun 2024 07:34:59 GMT  
		Size: 2.6 MB (2644870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc18ec37f21948c54422a8a2bd31634ae80dc4cd7d1f82b12857c17ad3e4aeec`  
		Size: 29.3 MB (29329348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a97a948909451f0ef002b4ce1035b5a09a3acde1633d198b1b7d25d6729f696`  
		Last Modified: Fri, 21 Jun 2024 17:09:25 GMT  
		Size: 158.2 MB (158217029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mono:6.12.0` - unknown; unknown

```console
$ docker pull mono@sha256:06f899f1f0a8c6a50d0cccbe9f415f29eb3eb9dba67e1076050fb7fa3214bc38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.2 MB (11173870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0a16765ae4b4d709f200047ad778fd0e6b25c0149b15eeb60dff4320acaf196`

```dockerfile
```

-	Layers:
	-	`sha256:3d8ff956fff2b5ea5a8f2a0f26101974ab6b290a4863020c141f56ce0ff86582`  
		Last Modified: Fri, 21 Jun 2024 17:09:17 GMT  
		Size: 11.2 MB (11165553 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0812c62e6dd0b6028ef0d86e34492bdbb20ebf6bae746864504d4121912d4cba`  
		Last Modified: Fri, 21 Jun 2024 17:09:16 GMT  
		Size: 8.3 KB (8317 bytes)  
		MIME: application/vnd.in-toto+json

### `mono:6.12.0` - linux; 386

```console
$ docker pull mono@sha256:8f10891be25745681bd6f98bf48e1234094816dc4b5dbef73d48f53f67536601
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.5 MB (259458549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2775d67ed2568bc292fd99d9a4c6e6e31195ae5382d5d3f1d76cb0f034c34e5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jun 2022 16:43:21 GMT
ADD file:7bc8fc617f718bf5e65e7fd718531a01122acc1783af5233c98aa9d31b0f093e in / 
# Wed, 22 Jun 2022 16:43:21 GMT
CMD ["bash"]
# Wed, 22 Jun 2022 16:43:21 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 22 Jun 2022 16:43:21 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr # buildkit
# Wed, 22 Jun 2022 16:43:21 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
# Wed, 22 Jun 2022 16:43:21 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
```

-	Layers:
	-	`sha256:1dfc643447ff7a82c599b429eda0d998c6dbad4ab2786eed580821b5b888204e`  
		Last Modified: Wed, 08 Jan 2025 03:46:41 GMT  
		Size: 28.0 MB (27994640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a198cb1aaae91cef3ed2eaed184c0a10f0b74e857bd5ea91dcde2955746f20f9`  
		Last Modified: Wed, 08 Jan 2025 03:46:41 GMT  
		Size: 2.8 MB (2791765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd658841b3e1b2084a6340e82f84033bf765e9ea9830350aa5a4aba88cbf3166`  
		Last Modified: Fri, 21 Jun 2024 01:03:14 GMT  
		Size: 68.6 MB (68585515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30bbf7033252959af4d7a4d2f468bba517cf0aeaf9f9e131902187bdc9737e6d`  
		Last Modified: Fri, 21 Jun 2024 02:04:03 GMT  
		Size: 160.1 MB (160086629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mono:6.12.0` - unknown; unknown

```console
$ docker pull mono@sha256:e69c4a0ff0efcd311f3ec0da7e72cbafaa9689b8555686674db7d3d689e13230
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11081926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48b0f05b8c3e2ec0bdb3fcbf2f85778a7584ea1dfd621e838399e99f0e6aac47`

```dockerfile
```

-	Layers:
	-	`sha256:f5bc84e8ea570b2500296b1f25f4226e60f0c15178c4ed81b09fa2c5ddf35fc6`  
		Last Modified: Fri, 21 Jun 2024 02:03:58 GMT  
		Size: 11.1 MB (11074056 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f11f469c7181081a082c334f89f2885f7a6a0953d5e152e5f75db2af4504d80e`  
		Last Modified: Fri, 21 Jun 2024 02:03:57 GMT  
		Size: 7.9 KB (7870 bytes)  
		MIME: application/vnd.in-toto+json

### `mono:6.12.0` - linux; ppc64le

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

## `mono:6.12.0-slim`

```console
$ docker pull mono@sha256:eb9a8d42dc58090cdb0d39b36422d9560f33e9d2cce22f4c888da263cee46c45
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le

### `mono:6.12.0-slim` - linux; amd64

```console
$ docker pull mono@sha256:749851d74745492754d1ebb3c50fc335d4b84a7bb34e17a4e7c3909c5ec1212b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.7 MB (94673661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5a2a70110040ee175a00069fa147d036d49deb2decd03a6374e83da337706e8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jun 2022 16:43:21 GMT
ADD file:cce4de1623245f9f28e3365e6cf749d85dcfedddea2d6fbc963c309a40818f52 in / 
# Wed, 22 Jun 2022 16:43:21 GMT
CMD ["bash"]
# Wed, 22 Jun 2022 16:43:21 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 22 Jun 2022 16:43:21 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr # buildkit
# Wed, 22 Jun 2022 16:43:21 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
```

-	Layers:
	-	`sha256:b338562f40a7fb7360dfae935da6d7e40d2545db18bc461d9d70ec1b2b657f33`  
		Last Modified: Thu, 13 Jun 2024 01:26:49 GMT  
		Size: 27.3 MB (27337703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b1b752ddf75c64e105424fb16f5a2053ddad33f059e3be8e520e35908cc4e97`  
		Last Modified: Fri, 21 Jun 2024 01:03:10 GMT  
		Size: 2.8 MB (2780035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d574eb224b5ddbe14656e28913cf5eeb5b14aa651aa3bcb9288aa43f1000aec5`  
		Last Modified: Fri, 21 Jun 2024 01:03:11 GMT  
		Size: 64.6 MB (64555923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mono:6.12.0-slim` - unknown; unknown

```console
$ docker pull mono@sha256:5a8421c386b586f98034983cc67448394e910e05ff857862418296991eddcf54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4134119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7daf4a5e106256a64c61c2f6e62ec4e5aa7020398e1b40c8bbe8b4e7458bec8d`

```dockerfile
```

-	Layers:
	-	`sha256:68c0c6a6586378e1af3fd618d65a15dd0a69c3e36744d2db3c2a64b91f8842b8`  
		Last Modified: Fri, 21 Jun 2024 01:03:10 GMT  
		Size: 4.1 MB (4124009 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ec35e37e8929d1729d15f72eaafb529c88604e0eb2b568452d3927312850835`  
		Last Modified: Fri, 21 Jun 2024 01:03:10 GMT  
		Size: 10.1 KB (10110 bytes)  
		MIME: application/vnd.in-toto+json

### `mono:6.12.0-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:f7c133539fa6a4add7484e9c93bc9b62ec32236d4b619f320c20b3248fb4739a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.9 MB (51860964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe52652f149ceedc89ed0c0f70985fcd898b6cd5cc98aa6f99f9ca06fd83046c`
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

### `mono:6.12.0-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:dd07ed6527eaa5860d31d50e7a3c5521b6f559eed9822aeeeb8667ce8390e378
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48888102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f645d1e48f0116b7141165a6952885d2f77e3033c87231c6d63152270ffd7a33`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jun 2022 16:43:21 GMT
ADD file:ab786d88497f915679b3ac228e3bd805a58501dcb33b3d25e49cf1898770f9a7 in / 
# Wed, 22 Jun 2022 16:43:21 GMT
CMD ["bash"]
# Wed, 22 Jun 2022 16:43:21 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 22 Jun 2022 16:43:21 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr # buildkit
# Wed, 22 Jun 2022 16:43:21 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
```

-	Layers:
	-	`sha256:99d1ebcdd364332a1427098feecc8f94a8978ec971b171f7cca03bf01d1a149c`  
		Size: 22.9 MB (22944997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47de34cd92203a1c44adc48be4330b559dcef9e18da3b5babab329d0fd26e11f`  
		Last Modified: Fri, 21 Jun 2024 05:26:04 GMT  
		Size: 2.4 MB (2370028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14dae79eba6437cf8f1fe8c17653348408d9b42ad8948d93472bbffd86792d7b`  
		Last Modified: Fri, 21 Jun 2024 05:26:05 GMT  
		Size: 23.6 MB (23573077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mono:6.12.0-slim` - unknown; unknown

```console
$ docker pull mono@sha256:ee35f615c2629a07e18483c6e85d7a3c83498ec7a51d34e09c6831e8720ee843
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4043799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e77739a150c122ee693247b621455e84030503770aa1098a0d6e90ae5d11efea`

```dockerfile
```

-	Layers:
	-	`sha256:e211386d3756bb307e96a299f301c5ef1eb874182b4c4a9e23f63b9ae5388ec3`  
		Last Modified: Fri, 21 Jun 2024 05:26:05 GMT  
		Size: 4.0 MB (4033599 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78feeadf8c15b58b8ecdee782634016d91ad2995f88bccaf8f187a8adc6ef4ff`  
		Last Modified: Fri, 21 Jun 2024 05:26:04 GMT  
		Size: 10.2 KB (10200 bytes)  
		MIME: application/vnd.in-toto+json

### `mono:6.12.0-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:f8ca545da29ef84d991bc3713b7284fcee5344a8e73eac40567bfefcf7de4a20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.1 MB (58083490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:337ba12936b175b1f418a4a2fb20db97d206faf71ca52fd475c94ac4d3993a3e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jun 2022 16:43:21 GMT
ADD file:de9a2b323e6d7d969277e7e781875e3daf3f49f2c1dcc569a1eec4f5bd789c46 in / 
# Wed, 22 Jun 2022 16:43:21 GMT
CMD ["bash"]
# Wed, 22 Jun 2022 16:43:21 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 22 Jun 2022 16:43:21 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr # buildkit
# Wed, 22 Jun 2022 16:43:21 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
```

-	Layers:
	-	`sha256:7abf9f73c7747bb840a8edcd895830e53f09498136de3015568a9cd9f5ab10ed`  
		Last Modified: Thu, 13 Jun 2024 00:44:26 GMT  
		Size: 26.1 MB (26109272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eedc96c6829dd818687f02719ed29ee02b62d29b93d260a87cbfdf65bd82307`  
		Last Modified: Fri, 21 Jun 2024 07:34:59 GMT  
		Size: 2.6 MB (2644870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc18ec37f21948c54422a8a2bd31634ae80dc4cd7d1f82b12857c17ad3e4aeec`  
		Size: 29.3 MB (29329348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mono:6.12.0-slim` - unknown; unknown

```console
$ docker pull mono@sha256:cd9b48412dc563b39c0103943d5ed3cbc90b60a7c49d51e07903e020b8cfb981
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4221860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fefffedbcde83d1d79c60cf414a8e8472225ffa87437cbd87ed93cbcde2840f2`

```dockerfile
```

-	Layers:
	-	`sha256:681a9485d68b8e56f7c721e96ecc685811a344e8356bab9dcbb7ed283fc771a4`  
		Last Modified: Fri, 21 Jun 2024 07:34:59 GMT  
		Size: 4.2 MB (4211431 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a953520626886eee4ff5675e5962fcd17b1795c5421161e5d957486e675fec3b`  
		Last Modified: Fri, 21 Jun 2024 07:34:58 GMT  
		Size: 10.4 KB (10429 bytes)  
		MIME: application/vnd.in-toto+json

### `mono:6.12.0-slim` - linux; 386

```console
$ docker pull mono@sha256:819bc68ca415cdb49ad461b4afb9a27004e442878b2bbdefc8a67317bc5b2ddf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.4 MB (99371920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c360bfbb224cb22cd13ba52ccd63bc77562ef28647c535cd0a42518f0773a842`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jun 2022 16:43:21 GMT
ADD file:7bc8fc617f718bf5e65e7fd718531a01122acc1783af5233c98aa9d31b0f093e in / 
# Wed, 22 Jun 2022 16:43:21 GMT
CMD ["bash"]
# Wed, 22 Jun 2022 16:43:21 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 22 Jun 2022 16:43:21 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr # buildkit
# Wed, 22 Jun 2022 16:43:21 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
```

-	Layers:
	-	`sha256:1dfc643447ff7a82c599b429eda0d998c6dbad4ab2786eed580821b5b888204e`  
		Last Modified: Wed, 08 Jan 2025 03:46:41 GMT  
		Size: 28.0 MB (27994640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a198cb1aaae91cef3ed2eaed184c0a10f0b74e857bd5ea91dcde2955746f20f9`  
		Last Modified: Wed, 08 Jan 2025 03:46:41 GMT  
		Size: 2.8 MB (2791765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd658841b3e1b2084a6340e82f84033bf765e9ea9830350aa5a4aba88cbf3166`  
		Last Modified: Fri, 21 Jun 2024 01:03:14 GMT  
		Size: 68.6 MB (68585515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mono:6.12.0-slim` - unknown; unknown

```console
$ docker pull mono@sha256:21b839469b89df687807ffdd3f870708c16efa44a6b299510e9d6391ba6499fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4130249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80ef153a1ce2f246cf50247bdbe0e53a65f2eca1f65498fe5be40b5242f5f8b1`

```dockerfile
```

-	Layers:
	-	`sha256:053ce445b27e3a8e224b16a3d2a8cdc9dc1d84ebee53d08de3d37ec36d5de95c`  
		Size: 4.1 MB (4120175 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:190e2c58614be0d956b94cdc868f9beb77c2f2d8ef16c981339f2b2c23f56975`  
		Last Modified: Fri, 21 Jun 2024 01:03:12 GMT  
		Size: 10.1 KB (10074 bytes)  
		MIME: application/vnd.in-toto+json

### `mono:6.12.0-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:b83383e51874bbee097571b303be3299c87d7da8c4c6b0f4e067cfaa552ad925
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75350311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c28d9c810a28445dd3b5767c5be8a3a5c5f459f859498e49f59bb419b735510`
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

## `mono:6.12.0.182`

```console
$ docker pull mono@sha256:34d816779b1248b5cfd095770b64ecbaf1798e2aca693a91c11a018dce9c7ad5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le

### `mono:6.12.0.182` - linux; amd64

```console
$ docker pull mono@sha256:d2ae1881a608fb6401bcebbf0d444fc2fcadf0db27f07c87153a79e7b14e861a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.6 MB (254589877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16d98cfcc673531288833a5cdb9f87087aa18082d1fed9ebe02021c67b1fdf0f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jun 2022 16:43:21 GMT
ADD file:cce4de1623245f9f28e3365e6cf749d85dcfedddea2d6fbc963c309a40818f52 in / 
# Wed, 22 Jun 2022 16:43:21 GMT
CMD ["bash"]
# Wed, 22 Jun 2022 16:43:21 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 22 Jun 2022 16:43:21 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr # buildkit
# Wed, 22 Jun 2022 16:43:21 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
# Wed, 22 Jun 2022 16:43:21 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
```

-	Layers:
	-	`sha256:b338562f40a7fb7360dfae935da6d7e40d2545db18bc461d9d70ec1b2b657f33`  
		Last Modified: Thu, 13 Jun 2024 01:26:49 GMT  
		Size: 27.3 MB (27337703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b1b752ddf75c64e105424fb16f5a2053ddad33f059e3be8e520e35908cc4e97`  
		Last Modified: Fri, 21 Jun 2024 01:03:10 GMT  
		Size: 2.8 MB (2780035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d574eb224b5ddbe14656e28913cf5eeb5b14aa651aa3bcb9288aa43f1000aec5`  
		Last Modified: Fri, 21 Jun 2024 01:03:11 GMT  
		Size: 64.6 MB (64555923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb9d6fb145c5367510a78273891d0ba84d7257b0bfdf3cd340f4e3d6f211de0a`  
		Last Modified: Fri, 21 Jun 2024 02:02:49 GMT  
		Size: 159.9 MB (159916216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mono:6.12.0.182` - unknown; unknown

```console
$ docker pull mono@sha256:fc661c46136b8f9cbe60f721c811fb05d600f7614c9ddef8306ca5a261a6ea24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11085967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6322617bf4f258627a38887597f3d55cd3e73d36de6aa5f4734d1d6fcd3e7fd9`

```dockerfile
```

-	Layers:
	-	`sha256:08c2cae238c884d7e44ae9bd57336a51412c9603e15025c0a456eca7dd888aba`  
		Last Modified: Fri, 21 Jun 2024 02:02:46 GMT  
		Size: 11.1 MB (11078059 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2dda4ada58791fac758ee1dc7c9ee2756a6d55125463cc11427657bfedecb286`  
		Last Modified: Fri, 21 Jun 2024 02:02:46 GMT  
		Size: 7.9 KB (7908 bytes)  
		MIME: application/vnd.in-toto+json

### `mono:6.12.0.182` - linux; arm variant v5

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

### `mono:6.12.0.182` - linux; arm variant v7

```console
$ docker pull mono@sha256:bb330a955d4e30fc342e6a770e76253662e2ab4eaf51dbb51f988815f6b28f29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.9 MB (188935459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d07296a48da608d892f2dcc9928236339e8eaedab5e92f1a0bb2cb73c9a1693e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jun 2022 16:43:21 GMT
ADD file:ab786d88497f915679b3ac228e3bd805a58501dcb33b3d25e49cf1898770f9a7 in / 
# Wed, 22 Jun 2022 16:43:21 GMT
CMD ["bash"]
# Wed, 22 Jun 2022 16:43:21 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 22 Jun 2022 16:43:21 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr # buildkit
# Wed, 22 Jun 2022 16:43:21 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
# Wed, 22 Jun 2022 16:43:21 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
```

-	Layers:
	-	`sha256:99d1ebcdd364332a1427098feecc8f94a8978ec971b171f7cca03bf01d1a149c`  
		Size: 22.9 MB (22944997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47de34cd92203a1c44adc48be4330b559dcef9e18da3b5babab329d0fd26e11f`  
		Last Modified: Fri, 21 Jun 2024 05:26:04 GMT  
		Size: 2.4 MB (2370028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14dae79eba6437cf8f1fe8c17653348408d9b42ad8948d93472bbffd86792d7b`  
		Last Modified: Fri, 21 Jun 2024 05:26:05 GMT  
		Size: 23.6 MB (23573077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f623ef7b096557bbf700a18c1f6616fa36cfb781282427c32b42ee2bf6f5d788`  
		Last Modified: Fri, 21 Jun 2024 13:15:11 GMT  
		Size: 140.0 MB (140047357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mono:6.12.0.182` - unknown; unknown

```console
$ docker pull mono@sha256:85360b79dd6fd6383cee0bf95518112f77c11353aaa15ab291ba68db619e15ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.0 MB (10995859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2bed6a6671ce784ea5373b029adbbe3d4b3b1ff7a8f59eed60bb7fed2baee0e`

```dockerfile
```

-	Layers:
	-	`sha256:a2750707e64721db5673f1d8443493f0a94e552993057b314e46f727642deefe`  
		Last Modified: Fri, 21 Jun 2024 13:15:08 GMT  
		Size: 11.0 MB (10987855 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:626e6cbf5e9f3aba334705529601969366e52b1b76d405943e486e844d7bbfea`  
		Last Modified: Fri, 21 Jun 2024 13:15:07 GMT  
		Size: 8.0 KB (8004 bytes)  
		MIME: application/vnd.in-toto+json

### `mono:6.12.0.182` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:5b876dc42dbdf92201a17d179906d941011b64493b32ce09d0d1faf12f470361
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.3 MB (216300519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bbe627177b284938a13b85f3505e07a72c220eeae1d6d4b9a675687f4a9f9be`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jun 2022 16:43:21 GMT
ADD file:de9a2b323e6d7d969277e7e781875e3daf3f49f2c1dcc569a1eec4f5bd789c46 in / 
# Wed, 22 Jun 2022 16:43:21 GMT
CMD ["bash"]
# Wed, 22 Jun 2022 16:43:21 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 22 Jun 2022 16:43:21 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr # buildkit
# Wed, 22 Jun 2022 16:43:21 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
# Wed, 22 Jun 2022 16:43:21 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
```

-	Layers:
	-	`sha256:7abf9f73c7747bb840a8edcd895830e53f09498136de3015568a9cd9f5ab10ed`  
		Last Modified: Thu, 13 Jun 2024 00:44:26 GMT  
		Size: 26.1 MB (26109272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eedc96c6829dd818687f02719ed29ee02b62d29b93d260a87cbfdf65bd82307`  
		Last Modified: Fri, 21 Jun 2024 07:34:59 GMT  
		Size: 2.6 MB (2644870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc18ec37f21948c54422a8a2bd31634ae80dc4cd7d1f82b12857c17ad3e4aeec`  
		Size: 29.3 MB (29329348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a97a948909451f0ef002b4ce1035b5a09a3acde1633d198b1b7d25d6729f696`  
		Last Modified: Fri, 21 Jun 2024 17:09:25 GMT  
		Size: 158.2 MB (158217029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mono:6.12.0.182` - unknown; unknown

```console
$ docker pull mono@sha256:06f899f1f0a8c6a50d0cccbe9f415f29eb3eb9dba67e1076050fb7fa3214bc38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.2 MB (11173870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0a16765ae4b4d709f200047ad778fd0e6b25c0149b15eeb60dff4320acaf196`

```dockerfile
```

-	Layers:
	-	`sha256:3d8ff956fff2b5ea5a8f2a0f26101974ab6b290a4863020c141f56ce0ff86582`  
		Last Modified: Fri, 21 Jun 2024 17:09:17 GMT  
		Size: 11.2 MB (11165553 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0812c62e6dd0b6028ef0d86e34492bdbb20ebf6bae746864504d4121912d4cba`  
		Last Modified: Fri, 21 Jun 2024 17:09:16 GMT  
		Size: 8.3 KB (8317 bytes)  
		MIME: application/vnd.in-toto+json

### `mono:6.12.0.182` - linux; 386

```console
$ docker pull mono@sha256:8f10891be25745681bd6f98bf48e1234094816dc4b5dbef73d48f53f67536601
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.5 MB (259458549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2775d67ed2568bc292fd99d9a4c6e6e31195ae5382d5d3f1d76cb0f034c34e5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jun 2022 16:43:21 GMT
ADD file:7bc8fc617f718bf5e65e7fd718531a01122acc1783af5233c98aa9d31b0f093e in / 
# Wed, 22 Jun 2022 16:43:21 GMT
CMD ["bash"]
# Wed, 22 Jun 2022 16:43:21 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 22 Jun 2022 16:43:21 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr # buildkit
# Wed, 22 Jun 2022 16:43:21 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
# Wed, 22 Jun 2022 16:43:21 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
```

-	Layers:
	-	`sha256:1dfc643447ff7a82c599b429eda0d998c6dbad4ab2786eed580821b5b888204e`  
		Last Modified: Wed, 08 Jan 2025 03:46:41 GMT  
		Size: 28.0 MB (27994640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a198cb1aaae91cef3ed2eaed184c0a10f0b74e857bd5ea91dcde2955746f20f9`  
		Last Modified: Wed, 08 Jan 2025 03:46:41 GMT  
		Size: 2.8 MB (2791765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd658841b3e1b2084a6340e82f84033bf765e9ea9830350aa5a4aba88cbf3166`  
		Last Modified: Fri, 21 Jun 2024 01:03:14 GMT  
		Size: 68.6 MB (68585515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30bbf7033252959af4d7a4d2f468bba517cf0aeaf9f9e131902187bdc9737e6d`  
		Last Modified: Fri, 21 Jun 2024 02:04:03 GMT  
		Size: 160.1 MB (160086629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mono:6.12.0.182` - unknown; unknown

```console
$ docker pull mono@sha256:e69c4a0ff0efcd311f3ec0da7e72cbafaa9689b8555686674db7d3d689e13230
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11081926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48b0f05b8c3e2ec0bdb3fcbf2f85778a7584ea1dfd621e838399e99f0e6aac47`

```dockerfile
```

-	Layers:
	-	`sha256:f5bc84e8ea570b2500296b1f25f4226e60f0c15178c4ed81b09fa2c5ddf35fc6`  
		Last Modified: Fri, 21 Jun 2024 02:03:58 GMT  
		Size: 11.1 MB (11074056 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f11f469c7181081a082c334f89f2885f7a6a0953d5e152e5f75db2af4504d80e`  
		Last Modified: Fri, 21 Jun 2024 02:03:57 GMT  
		Size: 7.9 KB (7870 bytes)  
		MIME: application/vnd.in-toto+json

### `mono:6.12.0.182` - linux; ppc64le

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

## `mono:6.12.0.182-slim`

```console
$ docker pull mono@sha256:eb9a8d42dc58090cdb0d39b36422d9560f33e9d2cce22f4c888da263cee46c45
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le

### `mono:6.12.0.182-slim` - linux; amd64

```console
$ docker pull mono@sha256:749851d74745492754d1ebb3c50fc335d4b84a7bb34e17a4e7c3909c5ec1212b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.7 MB (94673661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5a2a70110040ee175a00069fa147d036d49deb2decd03a6374e83da337706e8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jun 2022 16:43:21 GMT
ADD file:cce4de1623245f9f28e3365e6cf749d85dcfedddea2d6fbc963c309a40818f52 in / 
# Wed, 22 Jun 2022 16:43:21 GMT
CMD ["bash"]
# Wed, 22 Jun 2022 16:43:21 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 22 Jun 2022 16:43:21 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr # buildkit
# Wed, 22 Jun 2022 16:43:21 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
```

-	Layers:
	-	`sha256:b338562f40a7fb7360dfae935da6d7e40d2545db18bc461d9d70ec1b2b657f33`  
		Last Modified: Thu, 13 Jun 2024 01:26:49 GMT  
		Size: 27.3 MB (27337703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b1b752ddf75c64e105424fb16f5a2053ddad33f059e3be8e520e35908cc4e97`  
		Last Modified: Fri, 21 Jun 2024 01:03:10 GMT  
		Size: 2.8 MB (2780035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d574eb224b5ddbe14656e28913cf5eeb5b14aa651aa3bcb9288aa43f1000aec5`  
		Last Modified: Fri, 21 Jun 2024 01:03:11 GMT  
		Size: 64.6 MB (64555923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mono:6.12.0.182-slim` - unknown; unknown

```console
$ docker pull mono@sha256:5a8421c386b586f98034983cc67448394e910e05ff857862418296991eddcf54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4134119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7daf4a5e106256a64c61c2f6e62ec4e5aa7020398e1b40c8bbe8b4e7458bec8d`

```dockerfile
```

-	Layers:
	-	`sha256:68c0c6a6586378e1af3fd618d65a15dd0a69c3e36744d2db3c2a64b91f8842b8`  
		Last Modified: Fri, 21 Jun 2024 01:03:10 GMT  
		Size: 4.1 MB (4124009 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ec35e37e8929d1729d15f72eaafb529c88604e0eb2b568452d3927312850835`  
		Last Modified: Fri, 21 Jun 2024 01:03:10 GMT  
		Size: 10.1 KB (10110 bytes)  
		MIME: application/vnd.in-toto+json

### `mono:6.12.0.182-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:f7c133539fa6a4add7484e9c93bc9b62ec32236d4b619f320c20b3248fb4739a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.9 MB (51860964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe52652f149ceedc89ed0c0f70985fcd898b6cd5cc98aa6f99f9ca06fd83046c`
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

### `mono:6.12.0.182-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:dd07ed6527eaa5860d31d50e7a3c5521b6f559eed9822aeeeb8667ce8390e378
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48888102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f645d1e48f0116b7141165a6952885d2f77e3033c87231c6d63152270ffd7a33`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jun 2022 16:43:21 GMT
ADD file:ab786d88497f915679b3ac228e3bd805a58501dcb33b3d25e49cf1898770f9a7 in / 
# Wed, 22 Jun 2022 16:43:21 GMT
CMD ["bash"]
# Wed, 22 Jun 2022 16:43:21 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 22 Jun 2022 16:43:21 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr # buildkit
# Wed, 22 Jun 2022 16:43:21 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
```

-	Layers:
	-	`sha256:99d1ebcdd364332a1427098feecc8f94a8978ec971b171f7cca03bf01d1a149c`  
		Size: 22.9 MB (22944997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47de34cd92203a1c44adc48be4330b559dcef9e18da3b5babab329d0fd26e11f`  
		Last Modified: Fri, 21 Jun 2024 05:26:04 GMT  
		Size: 2.4 MB (2370028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14dae79eba6437cf8f1fe8c17653348408d9b42ad8948d93472bbffd86792d7b`  
		Last Modified: Fri, 21 Jun 2024 05:26:05 GMT  
		Size: 23.6 MB (23573077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mono:6.12.0.182-slim` - unknown; unknown

```console
$ docker pull mono@sha256:ee35f615c2629a07e18483c6e85d7a3c83498ec7a51d34e09c6831e8720ee843
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4043799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e77739a150c122ee693247b621455e84030503770aa1098a0d6e90ae5d11efea`

```dockerfile
```

-	Layers:
	-	`sha256:e211386d3756bb307e96a299f301c5ef1eb874182b4c4a9e23f63b9ae5388ec3`  
		Last Modified: Fri, 21 Jun 2024 05:26:05 GMT  
		Size: 4.0 MB (4033599 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78feeadf8c15b58b8ecdee782634016d91ad2995f88bccaf8f187a8adc6ef4ff`  
		Last Modified: Fri, 21 Jun 2024 05:26:04 GMT  
		Size: 10.2 KB (10200 bytes)  
		MIME: application/vnd.in-toto+json

### `mono:6.12.0.182-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:f8ca545da29ef84d991bc3713b7284fcee5344a8e73eac40567bfefcf7de4a20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.1 MB (58083490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:337ba12936b175b1f418a4a2fb20db97d206faf71ca52fd475c94ac4d3993a3e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jun 2022 16:43:21 GMT
ADD file:de9a2b323e6d7d969277e7e781875e3daf3f49f2c1dcc569a1eec4f5bd789c46 in / 
# Wed, 22 Jun 2022 16:43:21 GMT
CMD ["bash"]
# Wed, 22 Jun 2022 16:43:21 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 22 Jun 2022 16:43:21 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr # buildkit
# Wed, 22 Jun 2022 16:43:21 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
```

-	Layers:
	-	`sha256:7abf9f73c7747bb840a8edcd895830e53f09498136de3015568a9cd9f5ab10ed`  
		Last Modified: Thu, 13 Jun 2024 00:44:26 GMT  
		Size: 26.1 MB (26109272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eedc96c6829dd818687f02719ed29ee02b62d29b93d260a87cbfdf65bd82307`  
		Last Modified: Fri, 21 Jun 2024 07:34:59 GMT  
		Size: 2.6 MB (2644870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc18ec37f21948c54422a8a2bd31634ae80dc4cd7d1f82b12857c17ad3e4aeec`  
		Size: 29.3 MB (29329348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mono:6.12.0.182-slim` - unknown; unknown

```console
$ docker pull mono@sha256:cd9b48412dc563b39c0103943d5ed3cbc90b60a7c49d51e07903e020b8cfb981
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4221860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fefffedbcde83d1d79c60cf414a8e8472225ffa87437cbd87ed93cbcde2840f2`

```dockerfile
```

-	Layers:
	-	`sha256:681a9485d68b8e56f7c721e96ecc685811a344e8356bab9dcbb7ed283fc771a4`  
		Last Modified: Fri, 21 Jun 2024 07:34:59 GMT  
		Size: 4.2 MB (4211431 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a953520626886eee4ff5675e5962fcd17b1795c5421161e5d957486e675fec3b`  
		Last Modified: Fri, 21 Jun 2024 07:34:58 GMT  
		Size: 10.4 KB (10429 bytes)  
		MIME: application/vnd.in-toto+json

### `mono:6.12.0.182-slim` - linux; 386

```console
$ docker pull mono@sha256:819bc68ca415cdb49ad461b4afb9a27004e442878b2bbdefc8a67317bc5b2ddf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.4 MB (99371920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c360bfbb224cb22cd13ba52ccd63bc77562ef28647c535cd0a42518f0773a842`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jun 2022 16:43:21 GMT
ADD file:7bc8fc617f718bf5e65e7fd718531a01122acc1783af5233c98aa9d31b0f093e in / 
# Wed, 22 Jun 2022 16:43:21 GMT
CMD ["bash"]
# Wed, 22 Jun 2022 16:43:21 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 22 Jun 2022 16:43:21 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr # buildkit
# Wed, 22 Jun 2022 16:43:21 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
```

-	Layers:
	-	`sha256:1dfc643447ff7a82c599b429eda0d998c6dbad4ab2786eed580821b5b888204e`  
		Last Modified: Wed, 08 Jan 2025 03:46:41 GMT  
		Size: 28.0 MB (27994640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a198cb1aaae91cef3ed2eaed184c0a10f0b74e857bd5ea91dcde2955746f20f9`  
		Last Modified: Wed, 08 Jan 2025 03:46:41 GMT  
		Size: 2.8 MB (2791765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd658841b3e1b2084a6340e82f84033bf765e9ea9830350aa5a4aba88cbf3166`  
		Last Modified: Fri, 21 Jun 2024 01:03:14 GMT  
		Size: 68.6 MB (68585515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mono:6.12.0.182-slim` - unknown; unknown

```console
$ docker pull mono@sha256:21b839469b89df687807ffdd3f870708c16efa44a6b299510e9d6391ba6499fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4130249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80ef153a1ce2f246cf50247bdbe0e53a65f2eca1f65498fe5be40b5242f5f8b1`

```dockerfile
```

-	Layers:
	-	`sha256:053ce445b27e3a8e224b16a3d2a8cdc9dc1d84ebee53d08de3d37ec36d5de95c`  
		Size: 4.1 MB (4120175 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:190e2c58614be0d956b94cdc868f9beb77c2f2d8ef16c981339f2b2c23f56975`  
		Last Modified: Fri, 21 Jun 2024 01:03:12 GMT  
		Size: 10.1 KB (10074 bytes)  
		MIME: application/vnd.in-toto+json

### `mono:6.12.0.182-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:b83383e51874bbee097571b303be3299c87d7da8c4c6b0f4e067cfaa552ad925
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75350311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c28d9c810a28445dd3b5767c5be8a3a5c5f459f859498e49f59bb419b735510`
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

## `mono:latest`

```console
$ docker pull mono@sha256:34d816779b1248b5cfd095770b64ecbaf1798e2aca693a91c11a018dce9c7ad5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le

### `mono:latest` - linux; amd64

```console
$ docker pull mono@sha256:d2ae1881a608fb6401bcebbf0d444fc2fcadf0db27f07c87153a79e7b14e861a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.6 MB (254589877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16d98cfcc673531288833a5cdb9f87087aa18082d1fed9ebe02021c67b1fdf0f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jun 2022 16:43:21 GMT
ADD file:cce4de1623245f9f28e3365e6cf749d85dcfedddea2d6fbc963c309a40818f52 in / 
# Wed, 22 Jun 2022 16:43:21 GMT
CMD ["bash"]
# Wed, 22 Jun 2022 16:43:21 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 22 Jun 2022 16:43:21 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr # buildkit
# Wed, 22 Jun 2022 16:43:21 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
# Wed, 22 Jun 2022 16:43:21 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
```

-	Layers:
	-	`sha256:b338562f40a7fb7360dfae935da6d7e40d2545db18bc461d9d70ec1b2b657f33`  
		Last Modified: Thu, 13 Jun 2024 01:26:49 GMT  
		Size: 27.3 MB (27337703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b1b752ddf75c64e105424fb16f5a2053ddad33f059e3be8e520e35908cc4e97`  
		Last Modified: Fri, 21 Jun 2024 01:03:10 GMT  
		Size: 2.8 MB (2780035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d574eb224b5ddbe14656e28913cf5eeb5b14aa651aa3bcb9288aa43f1000aec5`  
		Last Modified: Fri, 21 Jun 2024 01:03:11 GMT  
		Size: 64.6 MB (64555923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb9d6fb145c5367510a78273891d0ba84d7257b0bfdf3cd340f4e3d6f211de0a`  
		Last Modified: Fri, 21 Jun 2024 02:02:49 GMT  
		Size: 159.9 MB (159916216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mono:latest` - unknown; unknown

```console
$ docker pull mono@sha256:fc661c46136b8f9cbe60f721c811fb05d600f7614c9ddef8306ca5a261a6ea24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11085967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6322617bf4f258627a38887597f3d55cd3e73d36de6aa5f4734d1d6fcd3e7fd9`

```dockerfile
```

-	Layers:
	-	`sha256:08c2cae238c884d7e44ae9bd57336a51412c9603e15025c0a456eca7dd888aba`  
		Last Modified: Fri, 21 Jun 2024 02:02:46 GMT  
		Size: 11.1 MB (11078059 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2dda4ada58791fac758ee1dc7c9ee2756a6d55125463cc11427657bfedecb286`  
		Last Modified: Fri, 21 Jun 2024 02:02:46 GMT  
		Size: 7.9 KB (7908 bytes)  
		MIME: application/vnd.in-toto+json

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
$ docker pull mono@sha256:bb330a955d4e30fc342e6a770e76253662e2ab4eaf51dbb51f988815f6b28f29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.9 MB (188935459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d07296a48da608d892f2dcc9928236339e8eaedab5e92f1a0bb2cb73c9a1693e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jun 2022 16:43:21 GMT
ADD file:ab786d88497f915679b3ac228e3bd805a58501dcb33b3d25e49cf1898770f9a7 in / 
# Wed, 22 Jun 2022 16:43:21 GMT
CMD ["bash"]
# Wed, 22 Jun 2022 16:43:21 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 22 Jun 2022 16:43:21 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr # buildkit
# Wed, 22 Jun 2022 16:43:21 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
# Wed, 22 Jun 2022 16:43:21 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
```

-	Layers:
	-	`sha256:99d1ebcdd364332a1427098feecc8f94a8978ec971b171f7cca03bf01d1a149c`  
		Size: 22.9 MB (22944997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47de34cd92203a1c44adc48be4330b559dcef9e18da3b5babab329d0fd26e11f`  
		Last Modified: Fri, 21 Jun 2024 05:26:04 GMT  
		Size: 2.4 MB (2370028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14dae79eba6437cf8f1fe8c17653348408d9b42ad8948d93472bbffd86792d7b`  
		Last Modified: Fri, 21 Jun 2024 05:26:05 GMT  
		Size: 23.6 MB (23573077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f623ef7b096557bbf700a18c1f6616fa36cfb781282427c32b42ee2bf6f5d788`  
		Last Modified: Fri, 21 Jun 2024 13:15:11 GMT  
		Size: 140.0 MB (140047357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mono:latest` - unknown; unknown

```console
$ docker pull mono@sha256:85360b79dd6fd6383cee0bf95518112f77c11353aaa15ab291ba68db619e15ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.0 MB (10995859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2bed6a6671ce784ea5373b029adbbe3d4b3b1ff7a8f59eed60bb7fed2baee0e`

```dockerfile
```

-	Layers:
	-	`sha256:a2750707e64721db5673f1d8443493f0a94e552993057b314e46f727642deefe`  
		Last Modified: Fri, 21 Jun 2024 13:15:08 GMT  
		Size: 11.0 MB (10987855 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:626e6cbf5e9f3aba334705529601969366e52b1b76d405943e486e844d7bbfea`  
		Last Modified: Fri, 21 Jun 2024 13:15:07 GMT  
		Size: 8.0 KB (8004 bytes)  
		MIME: application/vnd.in-toto+json

### `mono:latest` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:5b876dc42dbdf92201a17d179906d941011b64493b32ce09d0d1faf12f470361
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.3 MB (216300519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bbe627177b284938a13b85f3505e07a72c220eeae1d6d4b9a675687f4a9f9be`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jun 2022 16:43:21 GMT
ADD file:de9a2b323e6d7d969277e7e781875e3daf3f49f2c1dcc569a1eec4f5bd789c46 in / 
# Wed, 22 Jun 2022 16:43:21 GMT
CMD ["bash"]
# Wed, 22 Jun 2022 16:43:21 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 22 Jun 2022 16:43:21 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr # buildkit
# Wed, 22 Jun 2022 16:43:21 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
# Wed, 22 Jun 2022 16:43:21 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
```

-	Layers:
	-	`sha256:7abf9f73c7747bb840a8edcd895830e53f09498136de3015568a9cd9f5ab10ed`  
		Last Modified: Thu, 13 Jun 2024 00:44:26 GMT  
		Size: 26.1 MB (26109272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eedc96c6829dd818687f02719ed29ee02b62d29b93d260a87cbfdf65bd82307`  
		Last Modified: Fri, 21 Jun 2024 07:34:59 GMT  
		Size: 2.6 MB (2644870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc18ec37f21948c54422a8a2bd31634ae80dc4cd7d1f82b12857c17ad3e4aeec`  
		Size: 29.3 MB (29329348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a97a948909451f0ef002b4ce1035b5a09a3acde1633d198b1b7d25d6729f696`  
		Last Modified: Fri, 21 Jun 2024 17:09:25 GMT  
		Size: 158.2 MB (158217029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mono:latest` - unknown; unknown

```console
$ docker pull mono@sha256:06f899f1f0a8c6a50d0cccbe9f415f29eb3eb9dba67e1076050fb7fa3214bc38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.2 MB (11173870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0a16765ae4b4d709f200047ad778fd0e6b25c0149b15eeb60dff4320acaf196`

```dockerfile
```

-	Layers:
	-	`sha256:3d8ff956fff2b5ea5a8f2a0f26101974ab6b290a4863020c141f56ce0ff86582`  
		Last Modified: Fri, 21 Jun 2024 17:09:17 GMT  
		Size: 11.2 MB (11165553 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0812c62e6dd0b6028ef0d86e34492bdbb20ebf6bae746864504d4121912d4cba`  
		Last Modified: Fri, 21 Jun 2024 17:09:16 GMT  
		Size: 8.3 KB (8317 bytes)  
		MIME: application/vnd.in-toto+json

### `mono:latest` - linux; 386

```console
$ docker pull mono@sha256:8f10891be25745681bd6f98bf48e1234094816dc4b5dbef73d48f53f67536601
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.5 MB (259458549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2775d67ed2568bc292fd99d9a4c6e6e31195ae5382d5d3f1d76cb0f034c34e5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jun 2022 16:43:21 GMT
ADD file:7bc8fc617f718bf5e65e7fd718531a01122acc1783af5233c98aa9d31b0f093e in / 
# Wed, 22 Jun 2022 16:43:21 GMT
CMD ["bash"]
# Wed, 22 Jun 2022 16:43:21 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 22 Jun 2022 16:43:21 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr # buildkit
# Wed, 22 Jun 2022 16:43:21 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
# Wed, 22 Jun 2022 16:43:21 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
```

-	Layers:
	-	`sha256:1dfc643447ff7a82c599b429eda0d998c6dbad4ab2786eed580821b5b888204e`  
		Last Modified: Wed, 08 Jan 2025 03:46:41 GMT  
		Size: 28.0 MB (27994640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a198cb1aaae91cef3ed2eaed184c0a10f0b74e857bd5ea91dcde2955746f20f9`  
		Last Modified: Wed, 08 Jan 2025 03:46:41 GMT  
		Size: 2.8 MB (2791765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd658841b3e1b2084a6340e82f84033bf765e9ea9830350aa5a4aba88cbf3166`  
		Last Modified: Fri, 21 Jun 2024 01:03:14 GMT  
		Size: 68.6 MB (68585515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30bbf7033252959af4d7a4d2f468bba517cf0aeaf9f9e131902187bdc9737e6d`  
		Last Modified: Fri, 21 Jun 2024 02:04:03 GMT  
		Size: 160.1 MB (160086629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mono:latest` - unknown; unknown

```console
$ docker pull mono@sha256:e69c4a0ff0efcd311f3ec0da7e72cbafaa9689b8555686674db7d3d689e13230
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11081926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48b0f05b8c3e2ec0bdb3fcbf2f85778a7584ea1dfd621e838399e99f0e6aac47`

```dockerfile
```

-	Layers:
	-	`sha256:f5bc84e8ea570b2500296b1f25f4226e60f0c15178c4ed81b09fa2c5ddf35fc6`  
		Last Modified: Fri, 21 Jun 2024 02:03:58 GMT  
		Size: 11.1 MB (11074056 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f11f469c7181081a082c334f89f2885f7a6a0953d5e152e5f75db2af4504d80e`  
		Last Modified: Fri, 21 Jun 2024 02:03:57 GMT  
		Size: 7.9 KB (7870 bytes)  
		MIME: application/vnd.in-toto+json

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

## `mono:slim`

```console
$ docker pull mono@sha256:eb9a8d42dc58090cdb0d39b36422d9560f33e9d2cce22f4c888da263cee46c45
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le

### `mono:slim` - linux; amd64

```console
$ docker pull mono@sha256:749851d74745492754d1ebb3c50fc335d4b84a7bb34e17a4e7c3909c5ec1212b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.7 MB (94673661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5a2a70110040ee175a00069fa147d036d49deb2decd03a6374e83da337706e8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jun 2022 16:43:21 GMT
ADD file:cce4de1623245f9f28e3365e6cf749d85dcfedddea2d6fbc963c309a40818f52 in / 
# Wed, 22 Jun 2022 16:43:21 GMT
CMD ["bash"]
# Wed, 22 Jun 2022 16:43:21 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 22 Jun 2022 16:43:21 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr # buildkit
# Wed, 22 Jun 2022 16:43:21 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
```

-	Layers:
	-	`sha256:b338562f40a7fb7360dfae935da6d7e40d2545db18bc461d9d70ec1b2b657f33`  
		Last Modified: Thu, 13 Jun 2024 01:26:49 GMT  
		Size: 27.3 MB (27337703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b1b752ddf75c64e105424fb16f5a2053ddad33f059e3be8e520e35908cc4e97`  
		Last Modified: Fri, 21 Jun 2024 01:03:10 GMT  
		Size: 2.8 MB (2780035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d574eb224b5ddbe14656e28913cf5eeb5b14aa651aa3bcb9288aa43f1000aec5`  
		Last Modified: Fri, 21 Jun 2024 01:03:11 GMT  
		Size: 64.6 MB (64555923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mono:slim` - unknown; unknown

```console
$ docker pull mono@sha256:5a8421c386b586f98034983cc67448394e910e05ff857862418296991eddcf54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4134119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7daf4a5e106256a64c61c2f6e62ec4e5aa7020398e1b40c8bbe8b4e7458bec8d`

```dockerfile
```

-	Layers:
	-	`sha256:68c0c6a6586378e1af3fd618d65a15dd0a69c3e36744d2db3c2a64b91f8842b8`  
		Last Modified: Fri, 21 Jun 2024 01:03:10 GMT  
		Size: 4.1 MB (4124009 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ec35e37e8929d1729d15f72eaafb529c88604e0eb2b568452d3927312850835`  
		Last Modified: Fri, 21 Jun 2024 01:03:10 GMT  
		Size: 10.1 KB (10110 bytes)  
		MIME: application/vnd.in-toto+json

### `mono:slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:f7c133539fa6a4add7484e9c93bc9b62ec32236d4b619f320c20b3248fb4739a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.9 MB (51860964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe52652f149ceedc89ed0c0f70985fcd898b6cd5cc98aa6f99f9ca06fd83046c`
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

### `mono:slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:dd07ed6527eaa5860d31d50e7a3c5521b6f559eed9822aeeeb8667ce8390e378
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48888102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f645d1e48f0116b7141165a6952885d2f77e3033c87231c6d63152270ffd7a33`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jun 2022 16:43:21 GMT
ADD file:ab786d88497f915679b3ac228e3bd805a58501dcb33b3d25e49cf1898770f9a7 in / 
# Wed, 22 Jun 2022 16:43:21 GMT
CMD ["bash"]
# Wed, 22 Jun 2022 16:43:21 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 22 Jun 2022 16:43:21 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr # buildkit
# Wed, 22 Jun 2022 16:43:21 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
```

-	Layers:
	-	`sha256:99d1ebcdd364332a1427098feecc8f94a8978ec971b171f7cca03bf01d1a149c`  
		Size: 22.9 MB (22944997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47de34cd92203a1c44adc48be4330b559dcef9e18da3b5babab329d0fd26e11f`  
		Last Modified: Fri, 21 Jun 2024 05:26:04 GMT  
		Size: 2.4 MB (2370028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14dae79eba6437cf8f1fe8c17653348408d9b42ad8948d93472bbffd86792d7b`  
		Last Modified: Fri, 21 Jun 2024 05:26:05 GMT  
		Size: 23.6 MB (23573077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mono:slim` - unknown; unknown

```console
$ docker pull mono@sha256:ee35f615c2629a07e18483c6e85d7a3c83498ec7a51d34e09c6831e8720ee843
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4043799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e77739a150c122ee693247b621455e84030503770aa1098a0d6e90ae5d11efea`

```dockerfile
```

-	Layers:
	-	`sha256:e211386d3756bb307e96a299f301c5ef1eb874182b4c4a9e23f63b9ae5388ec3`  
		Last Modified: Fri, 21 Jun 2024 05:26:05 GMT  
		Size: 4.0 MB (4033599 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78feeadf8c15b58b8ecdee782634016d91ad2995f88bccaf8f187a8adc6ef4ff`  
		Last Modified: Fri, 21 Jun 2024 05:26:04 GMT  
		Size: 10.2 KB (10200 bytes)  
		MIME: application/vnd.in-toto+json

### `mono:slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:f8ca545da29ef84d991bc3713b7284fcee5344a8e73eac40567bfefcf7de4a20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.1 MB (58083490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:337ba12936b175b1f418a4a2fb20db97d206faf71ca52fd475c94ac4d3993a3e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jun 2022 16:43:21 GMT
ADD file:de9a2b323e6d7d969277e7e781875e3daf3f49f2c1dcc569a1eec4f5bd789c46 in / 
# Wed, 22 Jun 2022 16:43:21 GMT
CMD ["bash"]
# Wed, 22 Jun 2022 16:43:21 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 22 Jun 2022 16:43:21 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr # buildkit
# Wed, 22 Jun 2022 16:43:21 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
```

-	Layers:
	-	`sha256:7abf9f73c7747bb840a8edcd895830e53f09498136de3015568a9cd9f5ab10ed`  
		Last Modified: Thu, 13 Jun 2024 00:44:26 GMT  
		Size: 26.1 MB (26109272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eedc96c6829dd818687f02719ed29ee02b62d29b93d260a87cbfdf65bd82307`  
		Last Modified: Fri, 21 Jun 2024 07:34:59 GMT  
		Size: 2.6 MB (2644870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc18ec37f21948c54422a8a2bd31634ae80dc4cd7d1f82b12857c17ad3e4aeec`  
		Size: 29.3 MB (29329348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mono:slim` - unknown; unknown

```console
$ docker pull mono@sha256:cd9b48412dc563b39c0103943d5ed3cbc90b60a7c49d51e07903e020b8cfb981
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4221860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fefffedbcde83d1d79c60cf414a8e8472225ffa87437cbd87ed93cbcde2840f2`

```dockerfile
```

-	Layers:
	-	`sha256:681a9485d68b8e56f7c721e96ecc685811a344e8356bab9dcbb7ed283fc771a4`  
		Last Modified: Fri, 21 Jun 2024 07:34:59 GMT  
		Size: 4.2 MB (4211431 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a953520626886eee4ff5675e5962fcd17b1795c5421161e5d957486e675fec3b`  
		Last Modified: Fri, 21 Jun 2024 07:34:58 GMT  
		Size: 10.4 KB (10429 bytes)  
		MIME: application/vnd.in-toto+json

### `mono:slim` - linux; 386

```console
$ docker pull mono@sha256:819bc68ca415cdb49ad461b4afb9a27004e442878b2bbdefc8a67317bc5b2ddf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.4 MB (99371920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c360bfbb224cb22cd13ba52ccd63bc77562ef28647c535cd0a42518f0773a842`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jun 2022 16:43:21 GMT
ADD file:7bc8fc617f718bf5e65e7fd718531a01122acc1783af5233c98aa9d31b0f093e in / 
# Wed, 22 Jun 2022 16:43:21 GMT
CMD ["bash"]
# Wed, 22 Jun 2022 16:43:21 GMT
ENV MONO_VERSION=6.12.0.182
# Wed, 22 Jun 2022 16:43:21 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr # buildkit
# Wed, 22 Jun 2022 16:43:21 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/* # buildkit
```

-	Layers:
	-	`sha256:1dfc643447ff7a82c599b429eda0d998c6dbad4ab2786eed580821b5b888204e`  
		Last Modified: Wed, 08 Jan 2025 03:46:41 GMT  
		Size: 28.0 MB (27994640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a198cb1aaae91cef3ed2eaed184c0a10f0b74e857bd5ea91dcde2955746f20f9`  
		Last Modified: Wed, 08 Jan 2025 03:46:41 GMT  
		Size: 2.8 MB (2791765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd658841b3e1b2084a6340e82f84033bf765e9ea9830350aa5a4aba88cbf3166`  
		Last Modified: Fri, 21 Jun 2024 01:03:14 GMT  
		Size: 68.6 MB (68585515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mono:slim` - unknown; unknown

```console
$ docker pull mono@sha256:21b839469b89df687807ffdd3f870708c16efa44a6b299510e9d6391ba6499fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4130249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80ef153a1ce2f246cf50247bdbe0e53a65f2eca1f65498fe5be40b5242f5f8b1`

```dockerfile
```

-	Layers:
	-	`sha256:053ce445b27e3a8e224b16a3d2a8cdc9dc1d84ebee53d08de3d37ec36d5de95c`  
		Size: 4.1 MB (4120175 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:190e2c58614be0d956b94cdc868f9beb77c2f2d8ef16c981339f2b2c23f56975`  
		Last Modified: Fri, 21 Jun 2024 01:03:12 GMT  
		Size: 10.1 KB (10074 bytes)  
		MIME: application/vnd.in-toto+json

### `mono:slim` - linux; ppc64le

```console
$ docker pull mono@sha256:b83383e51874bbee097571b303be3299c87d7da8c4c6b0f4e067cfaa552ad925
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75350311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c28d9c810a28445dd3b5767c5be8a3a5c5f459f859498e49f59bb419b735510`
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
