## `mono:slim`

```console
$ docker pull mono@sha256:d124eebf64f110db652f42c9e1e4a0627f84b6fc375ea3801751f7edcc74711b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
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
$ docker pull mono@sha256:beaab14b4de16ae0f14cb615383dddbe283523fbd00c8494f8a55ce1299ec4ce
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49105758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:053650949e0e3231b0c67fad4f4dd10e2cb9a84beb0a82569b203ce3a1716fbd`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:58:15 GMT
ADD file:ab786d88497f915679b3ac228e3bd805a58501dcb33b3d25e49cf1898770f9a7 in / 
# Thu, 13 Jun 2024 00:58:15 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 08:31:10 GMT
ENV MONO_VERSION=6.12.0.182
# Thu, 13 Jun 2024 08:31:24 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 13 Jun 2024 08:31:48 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:99d1ebcdd364332a1427098feecc8f94a8978ec971b171f7cca03bf01d1a149c`  
		Last Modified: Thu, 13 Jun 2024 01:03:01 GMT  
		Size: 22.9 MB (22944997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b7db2a28ee4fa8f5e893c5ca0f653dc9514221149d19d3632816e874498e112`  
		Last Modified: Thu, 13 Jun 2024 08:36:36 GMT  
		Size: 2.4 MB (2370421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f10ac972dcba288ded8e2044b27a0cdf74494394d8408e9383d92fce7e867d7`  
		Last Modified: Thu, 13 Jun 2024 08:36:40 GMT  
		Size: 23.8 MB (23790340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:f0cc2d1cdff3f4c9132e03486d350424d918e8a58e17997314a1de02a04b24fc
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.3 MB (58299671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7c7359194914e922baaffe35e36d41958cbdc56e1dfe1475fdeda11d4d860f0`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:40:19 GMT
ADD file:de9a2b323e6d7d969277e7e781875e3daf3f49f2c1dcc569a1eec4f5bd789c46 in / 
# Thu, 13 Jun 2024 00:40:19 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 02:40:00 GMT
ENV MONO_VERSION=6.12.0.182
# Thu, 13 Jun 2024 02:40:07 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 13 Jun 2024 02:40:22 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7abf9f73c7747bb840a8edcd895830e53f09498136de3015568a9cd9f5ab10ed`  
		Last Modified: Thu, 13 Jun 2024 00:44:26 GMT  
		Size: 26.1 MB (26109272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0b5b6710e68b3b250dd681138cde05cf6596b6f323c42d994db4dcdb4761526`  
		Last Modified: Thu, 13 Jun 2024 02:44:41 GMT  
		Size: 2.6 MB (2645492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd67156f41b6153be4d7339a8c26d81d9648cfb9a9e365f2486f34aa6f6f507f`  
		Last Modified: Thu, 13 Jun 2024 02:44:44 GMT  
		Size: 29.5 MB (29544907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

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
		Last Modified: Thu, 13 Jun 2024 00:44:44 GMT  
		Size: 28.0 MB (27994640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a198cb1aaae91cef3ed2eaed184c0a10f0b74e857bd5ea91dcde2955746f20f9`  
		Last Modified: Fri, 21 Jun 2024 01:03:12 GMT  
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
		Last Modified: Fri, 21 Jun 2024 01:03:12 GMT  
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
