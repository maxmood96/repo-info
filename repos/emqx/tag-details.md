<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `emqx`

-	[`emqx:4`](#emqx4)
-	[`emqx:4.4`](#emqx44)
-	[`emqx:4.4.18`](#emqx4418)
-	[`emqx:5`](#emqx5)
-	[`emqx:5.0`](#emqx50)
-	[`emqx:5.0.24`](#emqx5024)
-	[`emqx:latest`](#emqxlatest)

## `emqx:4`

```console
$ docker pull emqx@sha256:77996497798edcc4217178c052e7ae95f88faca4dd62c773bc8d8a7aedee006d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:4` - linux; amd64

```console
$ docker pull emqx@sha256:9fdd9a1f20f87a9fd3ce211c4c0f72f512a0e1aaa16282941f8e100b57a538e2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.3 MB (81291277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3827a210aa39b77ef10d0ba5fd16644363311c03c199d6320268b6564454491`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Wed, 12 Apr 2023 00:20:06 GMT
ADD file:11b1acca3f68b5c5787e292ff8dbdd114964a7272bf3519ab07710cbc01a0838 in / 
# Wed, 12 Apr 2023 00:20:06 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 00:42:35 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 00:42:35 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx
# Fri, 28 Apr 2023 18:19:26 GMT
ENV EMQX_VERSION=4.4.18
# Fri, 28 Apr 2023 18:19:26 GMT
ENV OTP=otp24.3.4.2-1
# Fri, 28 Apr 2023 18:19:31 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="53712834a3cf209e488b97842ed9d6bae887e6e79ebaae3a0887018aab59b05b"; fi;     if [ ${arch} = "arm64" ]; then sha256="5fe04b2a10fc5e43ee582b38ecd526480a44ae277f5e6aa68ccd85f45e76baad"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Fri, 28 Apr 2023 18:19:31 GMT
WORKDIR /opt/emqx
# Fri, 28 Apr 2023 18:19:31 GMT
USER emqx
# Fri, 28 Apr 2023 18:19:31 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Fri, 28 Apr 2023 18:19:31 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Fri, 28 Apr 2023 18:19:31 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Fri, 28 Apr 2023 18:19:31 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Fri, 28 Apr 2023 18:19:31 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:26c5c85e47da3022f1bdb9a112103646c5c29517d757e95426f16e4bd9533405`  
		Last Modified: Wed, 12 Apr 2023 00:23:43 GMT  
		Size: 31.4 MB (31418228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e901aaad2c36dc10a256fae9d94810d0bcd1d3732eb3e172f7d18eba970956df`  
		Last Modified: Wed, 12 Apr 2023 00:43:09 GMT  
		Size: 2.6 MB (2569627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f607aa293305bd4722109d3b17853a91b8de9754b42fe37d71be6cf3c9abb42`  
		Last Modified: Wed, 12 Apr 2023 00:43:08 GMT  
		Size: 4.1 KB (4105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c134636201addd0926a6662a21cd1b4ced8ebda109f498e8aa7ec6a3b03f9d88`  
		Last Modified: Fri, 28 Apr 2023 18:19:47 GMT  
		Size: 47.3 MB (47298208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a80756697f5d1e4c858a833f50a4365ecebd06b4439a652623a697172ddc4d53`  
		Last Modified: Fri, 28 Apr 2023 18:19:43 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:4` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:8e0d58732509353013c1b904bae07e0329d294ba52c2bd04f53bd25c502d4143
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72697245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:804639c65a2a511d2bed3309d5f86522f6d22dbc8a51e8f139e5fec392650d63`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Wed, 03 May 2023 00:22:49 GMT
ADD file:66d4d9078579608530442620145336062a293cc19f159b154a63a1bcdcce3f4c in / 
# Wed, 03 May 2023 00:22:50 GMT
CMD ["bash"]
# Wed, 03 May 2023 18:31:08 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 18:31:08 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx
# Wed, 03 May 2023 18:31:09 GMT
ENV EMQX_VERSION=4.4.18
# Wed, 03 May 2023 18:31:09 GMT
ENV OTP=otp24.3.4.2-1
# Wed, 03 May 2023 18:31:13 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="53712834a3cf209e488b97842ed9d6bae887e6e79ebaae3a0887018aab59b05b"; fi;     if [ ${arch} = "arm64" ]; then sha256="5fe04b2a10fc5e43ee582b38ecd526480a44ae277f5e6aa68ccd85f45e76baad"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Wed, 03 May 2023 18:31:13 GMT
WORKDIR /opt/emqx
# Wed, 03 May 2023 18:31:13 GMT
USER emqx
# Wed, 03 May 2023 18:31:13 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 03 May 2023 18:31:14 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Wed, 03 May 2023 18:31:14 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Wed, 03 May 2023 18:31:14 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 03 May 2023 18:31:14 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:b5d25b35c1dbfa256bea3dd164b2048d6c7f8074a555213c493c36f07bf4c559`  
		Last Modified: Wed, 03 May 2023 00:25:53 GMT  
		Size: 30.1 MB (30052733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7e7f51cc8da6fe6eddb0fd850db3e636cee3e3bf53295f3a92848743419ad42`  
		Last Modified: Wed, 03 May 2023 18:31:40 GMT  
		Size: 2.6 MB (2559413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b3d3ca96bb54f431601711afa294d7451ac1a5e31a4badb232efd929f1c1704`  
		Last Modified: Wed, 03 May 2023 18:31:39 GMT  
		Size: 4.1 KB (4109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff06d9350693c4f454f1e9f2ea815a24db1f44dad7dbf3c14cdb68600ef4fecd`  
		Last Modified: Wed, 03 May 2023 18:31:43 GMT  
		Size: 40.1 MB (40079882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0bb7f52eead47eddb019a9b93e2a9d788bcdace6d6e356c9aef8cecc7990f61`  
		Last Modified: Wed, 03 May 2023 18:31:40 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:4.4`

```console
$ docker pull emqx@sha256:77996497798edcc4217178c052e7ae95f88faca4dd62c773bc8d8a7aedee006d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:4.4` - linux; amd64

```console
$ docker pull emqx@sha256:9fdd9a1f20f87a9fd3ce211c4c0f72f512a0e1aaa16282941f8e100b57a538e2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.3 MB (81291277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3827a210aa39b77ef10d0ba5fd16644363311c03c199d6320268b6564454491`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Wed, 12 Apr 2023 00:20:06 GMT
ADD file:11b1acca3f68b5c5787e292ff8dbdd114964a7272bf3519ab07710cbc01a0838 in / 
# Wed, 12 Apr 2023 00:20:06 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 00:42:35 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 00:42:35 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx
# Fri, 28 Apr 2023 18:19:26 GMT
ENV EMQX_VERSION=4.4.18
# Fri, 28 Apr 2023 18:19:26 GMT
ENV OTP=otp24.3.4.2-1
# Fri, 28 Apr 2023 18:19:31 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="53712834a3cf209e488b97842ed9d6bae887e6e79ebaae3a0887018aab59b05b"; fi;     if [ ${arch} = "arm64" ]; then sha256="5fe04b2a10fc5e43ee582b38ecd526480a44ae277f5e6aa68ccd85f45e76baad"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Fri, 28 Apr 2023 18:19:31 GMT
WORKDIR /opt/emqx
# Fri, 28 Apr 2023 18:19:31 GMT
USER emqx
# Fri, 28 Apr 2023 18:19:31 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Fri, 28 Apr 2023 18:19:31 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Fri, 28 Apr 2023 18:19:31 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Fri, 28 Apr 2023 18:19:31 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Fri, 28 Apr 2023 18:19:31 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:26c5c85e47da3022f1bdb9a112103646c5c29517d757e95426f16e4bd9533405`  
		Last Modified: Wed, 12 Apr 2023 00:23:43 GMT  
		Size: 31.4 MB (31418228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e901aaad2c36dc10a256fae9d94810d0bcd1d3732eb3e172f7d18eba970956df`  
		Last Modified: Wed, 12 Apr 2023 00:43:09 GMT  
		Size: 2.6 MB (2569627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f607aa293305bd4722109d3b17853a91b8de9754b42fe37d71be6cf3c9abb42`  
		Last Modified: Wed, 12 Apr 2023 00:43:08 GMT  
		Size: 4.1 KB (4105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c134636201addd0926a6662a21cd1b4ced8ebda109f498e8aa7ec6a3b03f9d88`  
		Last Modified: Fri, 28 Apr 2023 18:19:47 GMT  
		Size: 47.3 MB (47298208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a80756697f5d1e4c858a833f50a4365ecebd06b4439a652623a697172ddc4d53`  
		Last Modified: Fri, 28 Apr 2023 18:19:43 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:4.4` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:8e0d58732509353013c1b904bae07e0329d294ba52c2bd04f53bd25c502d4143
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72697245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:804639c65a2a511d2bed3309d5f86522f6d22dbc8a51e8f139e5fec392650d63`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Wed, 03 May 2023 00:22:49 GMT
ADD file:66d4d9078579608530442620145336062a293cc19f159b154a63a1bcdcce3f4c in / 
# Wed, 03 May 2023 00:22:50 GMT
CMD ["bash"]
# Wed, 03 May 2023 18:31:08 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 18:31:08 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx
# Wed, 03 May 2023 18:31:09 GMT
ENV EMQX_VERSION=4.4.18
# Wed, 03 May 2023 18:31:09 GMT
ENV OTP=otp24.3.4.2-1
# Wed, 03 May 2023 18:31:13 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="53712834a3cf209e488b97842ed9d6bae887e6e79ebaae3a0887018aab59b05b"; fi;     if [ ${arch} = "arm64" ]; then sha256="5fe04b2a10fc5e43ee582b38ecd526480a44ae277f5e6aa68ccd85f45e76baad"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Wed, 03 May 2023 18:31:13 GMT
WORKDIR /opt/emqx
# Wed, 03 May 2023 18:31:13 GMT
USER emqx
# Wed, 03 May 2023 18:31:13 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 03 May 2023 18:31:14 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Wed, 03 May 2023 18:31:14 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Wed, 03 May 2023 18:31:14 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 03 May 2023 18:31:14 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:b5d25b35c1dbfa256bea3dd164b2048d6c7f8074a555213c493c36f07bf4c559`  
		Last Modified: Wed, 03 May 2023 00:25:53 GMT  
		Size: 30.1 MB (30052733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7e7f51cc8da6fe6eddb0fd850db3e636cee3e3bf53295f3a92848743419ad42`  
		Last Modified: Wed, 03 May 2023 18:31:40 GMT  
		Size: 2.6 MB (2559413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b3d3ca96bb54f431601711afa294d7451ac1a5e31a4badb232efd929f1c1704`  
		Last Modified: Wed, 03 May 2023 18:31:39 GMT  
		Size: 4.1 KB (4109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff06d9350693c4f454f1e9f2ea815a24db1f44dad7dbf3c14cdb68600ef4fecd`  
		Last Modified: Wed, 03 May 2023 18:31:43 GMT  
		Size: 40.1 MB (40079882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0bb7f52eead47eddb019a9b93e2a9d788bcdace6d6e356c9aef8cecc7990f61`  
		Last Modified: Wed, 03 May 2023 18:31:40 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:4.4.18`

```console
$ docker pull emqx@sha256:77996497798edcc4217178c052e7ae95f88faca4dd62c773bc8d8a7aedee006d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:4.4.18` - linux; amd64

```console
$ docker pull emqx@sha256:9fdd9a1f20f87a9fd3ce211c4c0f72f512a0e1aaa16282941f8e100b57a538e2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.3 MB (81291277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3827a210aa39b77ef10d0ba5fd16644363311c03c199d6320268b6564454491`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Wed, 12 Apr 2023 00:20:06 GMT
ADD file:11b1acca3f68b5c5787e292ff8dbdd114964a7272bf3519ab07710cbc01a0838 in / 
# Wed, 12 Apr 2023 00:20:06 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 00:42:35 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 00:42:35 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx
# Fri, 28 Apr 2023 18:19:26 GMT
ENV EMQX_VERSION=4.4.18
# Fri, 28 Apr 2023 18:19:26 GMT
ENV OTP=otp24.3.4.2-1
# Fri, 28 Apr 2023 18:19:31 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="53712834a3cf209e488b97842ed9d6bae887e6e79ebaae3a0887018aab59b05b"; fi;     if [ ${arch} = "arm64" ]; then sha256="5fe04b2a10fc5e43ee582b38ecd526480a44ae277f5e6aa68ccd85f45e76baad"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Fri, 28 Apr 2023 18:19:31 GMT
WORKDIR /opt/emqx
# Fri, 28 Apr 2023 18:19:31 GMT
USER emqx
# Fri, 28 Apr 2023 18:19:31 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Fri, 28 Apr 2023 18:19:31 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Fri, 28 Apr 2023 18:19:31 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Fri, 28 Apr 2023 18:19:31 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Fri, 28 Apr 2023 18:19:31 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:26c5c85e47da3022f1bdb9a112103646c5c29517d757e95426f16e4bd9533405`  
		Last Modified: Wed, 12 Apr 2023 00:23:43 GMT  
		Size: 31.4 MB (31418228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e901aaad2c36dc10a256fae9d94810d0bcd1d3732eb3e172f7d18eba970956df`  
		Last Modified: Wed, 12 Apr 2023 00:43:09 GMT  
		Size: 2.6 MB (2569627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f607aa293305bd4722109d3b17853a91b8de9754b42fe37d71be6cf3c9abb42`  
		Last Modified: Wed, 12 Apr 2023 00:43:08 GMT  
		Size: 4.1 KB (4105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c134636201addd0926a6662a21cd1b4ced8ebda109f498e8aa7ec6a3b03f9d88`  
		Last Modified: Fri, 28 Apr 2023 18:19:47 GMT  
		Size: 47.3 MB (47298208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a80756697f5d1e4c858a833f50a4365ecebd06b4439a652623a697172ddc4d53`  
		Last Modified: Fri, 28 Apr 2023 18:19:43 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:4.4.18` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:8e0d58732509353013c1b904bae07e0329d294ba52c2bd04f53bd25c502d4143
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72697245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:804639c65a2a511d2bed3309d5f86522f6d22dbc8a51e8f139e5fec392650d63`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Wed, 03 May 2023 00:22:49 GMT
ADD file:66d4d9078579608530442620145336062a293cc19f159b154a63a1bcdcce3f4c in / 
# Wed, 03 May 2023 00:22:50 GMT
CMD ["bash"]
# Wed, 03 May 2023 18:31:08 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 18:31:08 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx
# Wed, 03 May 2023 18:31:09 GMT
ENV EMQX_VERSION=4.4.18
# Wed, 03 May 2023 18:31:09 GMT
ENV OTP=otp24.3.4.2-1
# Wed, 03 May 2023 18:31:13 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="53712834a3cf209e488b97842ed9d6bae887e6e79ebaae3a0887018aab59b05b"; fi;     if [ ${arch} = "arm64" ]; then sha256="5fe04b2a10fc5e43ee582b38ecd526480a44ae277f5e6aa68ccd85f45e76baad"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Wed, 03 May 2023 18:31:13 GMT
WORKDIR /opt/emqx
# Wed, 03 May 2023 18:31:13 GMT
USER emqx
# Wed, 03 May 2023 18:31:13 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 03 May 2023 18:31:14 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Wed, 03 May 2023 18:31:14 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Wed, 03 May 2023 18:31:14 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 03 May 2023 18:31:14 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:b5d25b35c1dbfa256bea3dd164b2048d6c7f8074a555213c493c36f07bf4c559`  
		Last Modified: Wed, 03 May 2023 00:25:53 GMT  
		Size: 30.1 MB (30052733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7e7f51cc8da6fe6eddb0fd850db3e636cee3e3bf53295f3a92848743419ad42`  
		Last Modified: Wed, 03 May 2023 18:31:40 GMT  
		Size: 2.6 MB (2559413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b3d3ca96bb54f431601711afa294d7451ac1a5e31a4badb232efd929f1c1704`  
		Last Modified: Wed, 03 May 2023 18:31:39 GMT  
		Size: 4.1 KB (4109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff06d9350693c4f454f1e9f2ea815a24db1f44dad7dbf3c14cdb68600ef4fecd`  
		Last Modified: Wed, 03 May 2023 18:31:43 GMT  
		Size: 40.1 MB (40079882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0bb7f52eead47eddb019a9b93e2a9d788bcdace6d6e356c9aef8cecc7990f61`  
		Last Modified: Wed, 03 May 2023 18:31:40 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5`

```console
$ docker pull emqx@sha256:755b174745a233ad8794e3a7b52ffe968656759f723f2d472128ff7a513b9ca1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5` - linux; amd64

```console
$ docker pull emqx@sha256:bf9cbff4d72692150db0b8e71c12169682e4a1ecabaf31a0815a124b2c8c7191
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.4 MB (110351254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:324d003bff51e7326b599161e64280e9fb441616cc376c65b64979a6e57e1fca`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 12 Apr 2023 00:20:06 GMT
ADD file:11b1acca3f68b5c5787e292ff8dbdd114964a7272bf3519ab07710cbc01a0838 in / 
# Wed, 12 Apr 2023 00:20:06 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 00:42:50 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 00:42:51 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Thu, 27 Apr 2023 18:19:36 GMT
ENV EMQX_VERSION=5.0.24
# Thu, 27 Apr 2023 18:19:36 GMT
ENV AMD64_SHA256=d104bc3e1839447f5ceeaadbb3feb6c604c5f74b07ca33ab4c37baf2a9b33ae3
# Thu, 27 Apr 2023 18:19:36 GMT
ENV ARM64_SHA256=40d387b7d4dfc4aa7162ef628f25bcb33e8a3fc67740b3cdb5a6d843aa87c2ec
# Thu, 27 Apr 2023 18:19:36 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 27 Apr 2023 18:19:43 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg} &&     echo "$sha256 *$pkg" | sha256sum -c &&     mkdir /opt/emqx &&     tar zxf $pkg -C /opt/emqx &&     chgrp -Rf emqx /opt/emqx &&     chmod -Rf g+w /opt/emqx &&     chown -Rf emqx /opt/emqx &&     ln -s /opt/emqx/bin/* /usr/local/bin/ &&     rm -f $pkg
# Thu, 27 Apr 2023 18:19:43 GMT
WORKDIR /opt/emqx
# Thu, 27 Apr 2023 18:19:44 GMT
USER emqx
# Thu, 27 Apr 2023 18:19:44 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 27 Apr 2023 18:19:44 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Thu, 27 Apr 2023 18:19:44 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Thu, 27 Apr 2023 18:19:44 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 27 Apr 2023 18:19:44 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:26c5c85e47da3022f1bdb9a112103646c5c29517d757e95426f16e4bd9533405`  
		Last Modified: Wed, 12 Apr 2023 00:23:43 GMT  
		Size: 31.4 MB (31418228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f79c821cbd23fa1420033390e2828e0922b8efe06687c960eb7ff40edfbd0d6`  
		Last Modified: Wed, 12 Apr 2023 00:43:23 GMT  
		Size: 3.0 MB (2987825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:048c1bdd86f15f4d429d049f898a2d3c0f0732c5b7e68a31b824acae055655d8`  
		Last Modified: Wed, 12 Apr 2023 00:43:22 GMT  
		Size: 4.1 KB (4105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53ffb33fdb8e8734d8315c830f113b34280d1b709d9b2022540e77ce0012c71a`  
		Last Modified: Thu, 27 Apr 2023 18:20:04 GMT  
		Size: 75.9 MB (75940194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baedd37ee870a8649d239a5d45f6d6c498c1a0da32321dfdf8af290f463d9969`  
		Last Modified: Thu, 27 Apr 2023 18:19:55 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:4b50e10fb46731814c64c2f4895fb915e46bed6a02dbfb2c47f1cc850549541e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.4 MB (101420929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb178575b71345d1c69f7ed729a26d14a2f31906a357eb0af08e7bdacf1ea59a`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 03 May 2023 00:22:49 GMT
ADD file:66d4d9078579608530442620145336062a293cc19f159b154a63a1bcdcce3f4c in / 
# Wed, 03 May 2023 00:22:50 GMT
CMD ["bash"]
# Wed, 03 May 2023 18:31:21 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 18:31:22 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Wed, 03 May 2023 18:31:22 GMT
ENV EMQX_VERSION=5.0.24
# Wed, 03 May 2023 18:31:22 GMT
ENV AMD64_SHA256=d104bc3e1839447f5ceeaadbb3feb6c604c5f74b07ca33ab4c37baf2a9b33ae3
# Wed, 03 May 2023 18:31:22 GMT
ENV ARM64_SHA256=40d387b7d4dfc4aa7162ef628f25bcb33e8a3fc67740b3cdb5a6d843aa87c2ec
# Wed, 03 May 2023 18:31:22 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 03 May 2023 18:31:28 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg} &&     echo "$sha256 *$pkg" | sha256sum -c &&     mkdir /opt/emqx &&     tar zxf $pkg -C /opt/emqx &&     chgrp -Rf emqx /opt/emqx &&     chmod -Rf g+w /opt/emqx &&     chown -Rf emqx /opt/emqx &&     ln -s /opt/emqx/bin/* /usr/local/bin/ &&     rm -f $pkg
# Wed, 03 May 2023 18:31:29 GMT
WORKDIR /opt/emqx
# Wed, 03 May 2023 18:31:29 GMT
USER emqx
# Wed, 03 May 2023 18:31:29 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 03 May 2023 18:31:29 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Wed, 03 May 2023 18:31:30 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Wed, 03 May 2023 18:31:30 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 03 May 2023 18:31:30 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:b5d25b35c1dbfa256bea3dd164b2048d6c7f8074a555213c493c36f07bf4c559`  
		Last Modified: Wed, 03 May 2023 00:25:53 GMT  
		Size: 30.1 MB (30052733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a64a0a959a91944f5ffb31084a10b9b4826a9d805233e915031b76e42b602615`  
		Last Modified: Wed, 03 May 2023 18:31:54 GMT  
		Size: 3.0 MB (3003014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56882cfb1383ca5cd03757133ba3ae8958e9dcda03842b24d3ea7be1a5976eae`  
		Last Modified: Wed, 03 May 2023 18:31:53 GMT  
		Size: 4.1 KB (4111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f17d94cdbd45a137fdd4e9550c9063287635b1f489a5643b0d1ef2b4b97988a0`  
		Last Modified: Wed, 03 May 2023 18:32:00 GMT  
		Size: 68.4 MB (68360168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0135dc909c80db97e23cd34ad7cb67e57fe22c9cc1b3e4fd2bec3168f4446084`  
		Last Modified: Wed, 03 May 2023 18:31:53 GMT  
		Size: 903.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.0`

```console
$ docker pull emqx@sha256:755b174745a233ad8794e3a7b52ffe968656759f723f2d472128ff7a513b9ca1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.0` - linux; amd64

```console
$ docker pull emqx@sha256:bf9cbff4d72692150db0b8e71c12169682e4a1ecabaf31a0815a124b2c8c7191
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.4 MB (110351254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:324d003bff51e7326b599161e64280e9fb441616cc376c65b64979a6e57e1fca`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 12 Apr 2023 00:20:06 GMT
ADD file:11b1acca3f68b5c5787e292ff8dbdd114964a7272bf3519ab07710cbc01a0838 in / 
# Wed, 12 Apr 2023 00:20:06 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 00:42:50 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 00:42:51 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Thu, 27 Apr 2023 18:19:36 GMT
ENV EMQX_VERSION=5.0.24
# Thu, 27 Apr 2023 18:19:36 GMT
ENV AMD64_SHA256=d104bc3e1839447f5ceeaadbb3feb6c604c5f74b07ca33ab4c37baf2a9b33ae3
# Thu, 27 Apr 2023 18:19:36 GMT
ENV ARM64_SHA256=40d387b7d4dfc4aa7162ef628f25bcb33e8a3fc67740b3cdb5a6d843aa87c2ec
# Thu, 27 Apr 2023 18:19:36 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 27 Apr 2023 18:19:43 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg} &&     echo "$sha256 *$pkg" | sha256sum -c &&     mkdir /opt/emqx &&     tar zxf $pkg -C /opt/emqx &&     chgrp -Rf emqx /opt/emqx &&     chmod -Rf g+w /opt/emqx &&     chown -Rf emqx /opt/emqx &&     ln -s /opt/emqx/bin/* /usr/local/bin/ &&     rm -f $pkg
# Thu, 27 Apr 2023 18:19:43 GMT
WORKDIR /opt/emqx
# Thu, 27 Apr 2023 18:19:44 GMT
USER emqx
# Thu, 27 Apr 2023 18:19:44 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 27 Apr 2023 18:19:44 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Thu, 27 Apr 2023 18:19:44 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Thu, 27 Apr 2023 18:19:44 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 27 Apr 2023 18:19:44 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:26c5c85e47da3022f1bdb9a112103646c5c29517d757e95426f16e4bd9533405`  
		Last Modified: Wed, 12 Apr 2023 00:23:43 GMT  
		Size: 31.4 MB (31418228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f79c821cbd23fa1420033390e2828e0922b8efe06687c960eb7ff40edfbd0d6`  
		Last Modified: Wed, 12 Apr 2023 00:43:23 GMT  
		Size: 3.0 MB (2987825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:048c1bdd86f15f4d429d049f898a2d3c0f0732c5b7e68a31b824acae055655d8`  
		Last Modified: Wed, 12 Apr 2023 00:43:22 GMT  
		Size: 4.1 KB (4105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53ffb33fdb8e8734d8315c830f113b34280d1b709d9b2022540e77ce0012c71a`  
		Last Modified: Thu, 27 Apr 2023 18:20:04 GMT  
		Size: 75.9 MB (75940194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baedd37ee870a8649d239a5d45f6d6c498c1a0da32321dfdf8af290f463d9969`  
		Last Modified: Thu, 27 Apr 2023 18:19:55 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.0` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:4b50e10fb46731814c64c2f4895fb915e46bed6a02dbfb2c47f1cc850549541e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.4 MB (101420929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb178575b71345d1c69f7ed729a26d14a2f31906a357eb0af08e7bdacf1ea59a`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 03 May 2023 00:22:49 GMT
ADD file:66d4d9078579608530442620145336062a293cc19f159b154a63a1bcdcce3f4c in / 
# Wed, 03 May 2023 00:22:50 GMT
CMD ["bash"]
# Wed, 03 May 2023 18:31:21 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 18:31:22 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Wed, 03 May 2023 18:31:22 GMT
ENV EMQX_VERSION=5.0.24
# Wed, 03 May 2023 18:31:22 GMT
ENV AMD64_SHA256=d104bc3e1839447f5ceeaadbb3feb6c604c5f74b07ca33ab4c37baf2a9b33ae3
# Wed, 03 May 2023 18:31:22 GMT
ENV ARM64_SHA256=40d387b7d4dfc4aa7162ef628f25bcb33e8a3fc67740b3cdb5a6d843aa87c2ec
# Wed, 03 May 2023 18:31:22 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 03 May 2023 18:31:28 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg} &&     echo "$sha256 *$pkg" | sha256sum -c &&     mkdir /opt/emqx &&     tar zxf $pkg -C /opt/emqx &&     chgrp -Rf emqx /opt/emqx &&     chmod -Rf g+w /opt/emqx &&     chown -Rf emqx /opt/emqx &&     ln -s /opt/emqx/bin/* /usr/local/bin/ &&     rm -f $pkg
# Wed, 03 May 2023 18:31:29 GMT
WORKDIR /opt/emqx
# Wed, 03 May 2023 18:31:29 GMT
USER emqx
# Wed, 03 May 2023 18:31:29 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 03 May 2023 18:31:29 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Wed, 03 May 2023 18:31:30 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Wed, 03 May 2023 18:31:30 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 03 May 2023 18:31:30 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:b5d25b35c1dbfa256bea3dd164b2048d6c7f8074a555213c493c36f07bf4c559`  
		Last Modified: Wed, 03 May 2023 00:25:53 GMT  
		Size: 30.1 MB (30052733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a64a0a959a91944f5ffb31084a10b9b4826a9d805233e915031b76e42b602615`  
		Last Modified: Wed, 03 May 2023 18:31:54 GMT  
		Size: 3.0 MB (3003014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56882cfb1383ca5cd03757133ba3ae8958e9dcda03842b24d3ea7be1a5976eae`  
		Last Modified: Wed, 03 May 2023 18:31:53 GMT  
		Size: 4.1 KB (4111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f17d94cdbd45a137fdd4e9550c9063287635b1f489a5643b0d1ef2b4b97988a0`  
		Last Modified: Wed, 03 May 2023 18:32:00 GMT  
		Size: 68.4 MB (68360168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0135dc909c80db97e23cd34ad7cb67e57fe22c9cc1b3e4fd2bec3168f4446084`  
		Last Modified: Wed, 03 May 2023 18:31:53 GMT  
		Size: 903.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.0.24`

```console
$ docker pull emqx@sha256:755b174745a233ad8794e3a7b52ffe968656759f723f2d472128ff7a513b9ca1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.0.24` - linux; amd64

```console
$ docker pull emqx@sha256:bf9cbff4d72692150db0b8e71c12169682e4a1ecabaf31a0815a124b2c8c7191
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.4 MB (110351254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:324d003bff51e7326b599161e64280e9fb441616cc376c65b64979a6e57e1fca`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 12 Apr 2023 00:20:06 GMT
ADD file:11b1acca3f68b5c5787e292ff8dbdd114964a7272bf3519ab07710cbc01a0838 in / 
# Wed, 12 Apr 2023 00:20:06 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 00:42:50 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 00:42:51 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Thu, 27 Apr 2023 18:19:36 GMT
ENV EMQX_VERSION=5.0.24
# Thu, 27 Apr 2023 18:19:36 GMT
ENV AMD64_SHA256=d104bc3e1839447f5ceeaadbb3feb6c604c5f74b07ca33ab4c37baf2a9b33ae3
# Thu, 27 Apr 2023 18:19:36 GMT
ENV ARM64_SHA256=40d387b7d4dfc4aa7162ef628f25bcb33e8a3fc67740b3cdb5a6d843aa87c2ec
# Thu, 27 Apr 2023 18:19:36 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 27 Apr 2023 18:19:43 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg} &&     echo "$sha256 *$pkg" | sha256sum -c &&     mkdir /opt/emqx &&     tar zxf $pkg -C /opt/emqx &&     chgrp -Rf emqx /opt/emqx &&     chmod -Rf g+w /opt/emqx &&     chown -Rf emqx /opt/emqx &&     ln -s /opt/emqx/bin/* /usr/local/bin/ &&     rm -f $pkg
# Thu, 27 Apr 2023 18:19:43 GMT
WORKDIR /opt/emqx
# Thu, 27 Apr 2023 18:19:44 GMT
USER emqx
# Thu, 27 Apr 2023 18:19:44 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 27 Apr 2023 18:19:44 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Thu, 27 Apr 2023 18:19:44 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Thu, 27 Apr 2023 18:19:44 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 27 Apr 2023 18:19:44 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:26c5c85e47da3022f1bdb9a112103646c5c29517d757e95426f16e4bd9533405`  
		Last Modified: Wed, 12 Apr 2023 00:23:43 GMT  
		Size: 31.4 MB (31418228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f79c821cbd23fa1420033390e2828e0922b8efe06687c960eb7ff40edfbd0d6`  
		Last Modified: Wed, 12 Apr 2023 00:43:23 GMT  
		Size: 3.0 MB (2987825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:048c1bdd86f15f4d429d049f898a2d3c0f0732c5b7e68a31b824acae055655d8`  
		Last Modified: Wed, 12 Apr 2023 00:43:22 GMT  
		Size: 4.1 KB (4105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53ffb33fdb8e8734d8315c830f113b34280d1b709d9b2022540e77ce0012c71a`  
		Last Modified: Thu, 27 Apr 2023 18:20:04 GMT  
		Size: 75.9 MB (75940194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baedd37ee870a8649d239a5d45f6d6c498c1a0da32321dfdf8af290f463d9969`  
		Last Modified: Thu, 27 Apr 2023 18:19:55 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.0.24` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:4b50e10fb46731814c64c2f4895fb915e46bed6a02dbfb2c47f1cc850549541e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.4 MB (101420929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb178575b71345d1c69f7ed729a26d14a2f31906a357eb0af08e7bdacf1ea59a`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 03 May 2023 00:22:49 GMT
ADD file:66d4d9078579608530442620145336062a293cc19f159b154a63a1bcdcce3f4c in / 
# Wed, 03 May 2023 00:22:50 GMT
CMD ["bash"]
# Wed, 03 May 2023 18:31:21 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 18:31:22 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Wed, 03 May 2023 18:31:22 GMT
ENV EMQX_VERSION=5.0.24
# Wed, 03 May 2023 18:31:22 GMT
ENV AMD64_SHA256=d104bc3e1839447f5ceeaadbb3feb6c604c5f74b07ca33ab4c37baf2a9b33ae3
# Wed, 03 May 2023 18:31:22 GMT
ENV ARM64_SHA256=40d387b7d4dfc4aa7162ef628f25bcb33e8a3fc67740b3cdb5a6d843aa87c2ec
# Wed, 03 May 2023 18:31:22 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 03 May 2023 18:31:28 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg} &&     echo "$sha256 *$pkg" | sha256sum -c &&     mkdir /opt/emqx &&     tar zxf $pkg -C /opt/emqx &&     chgrp -Rf emqx /opt/emqx &&     chmod -Rf g+w /opt/emqx &&     chown -Rf emqx /opt/emqx &&     ln -s /opt/emqx/bin/* /usr/local/bin/ &&     rm -f $pkg
# Wed, 03 May 2023 18:31:29 GMT
WORKDIR /opt/emqx
# Wed, 03 May 2023 18:31:29 GMT
USER emqx
# Wed, 03 May 2023 18:31:29 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 03 May 2023 18:31:29 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Wed, 03 May 2023 18:31:30 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Wed, 03 May 2023 18:31:30 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 03 May 2023 18:31:30 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:b5d25b35c1dbfa256bea3dd164b2048d6c7f8074a555213c493c36f07bf4c559`  
		Last Modified: Wed, 03 May 2023 00:25:53 GMT  
		Size: 30.1 MB (30052733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a64a0a959a91944f5ffb31084a10b9b4826a9d805233e915031b76e42b602615`  
		Last Modified: Wed, 03 May 2023 18:31:54 GMT  
		Size: 3.0 MB (3003014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56882cfb1383ca5cd03757133ba3ae8958e9dcda03842b24d3ea7be1a5976eae`  
		Last Modified: Wed, 03 May 2023 18:31:53 GMT  
		Size: 4.1 KB (4111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f17d94cdbd45a137fdd4e9550c9063287635b1f489a5643b0d1ef2b4b97988a0`  
		Last Modified: Wed, 03 May 2023 18:32:00 GMT  
		Size: 68.4 MB (68360168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0135dc909c80db97e23cd34ad7cb67e57fe22c9cc1b3e4fd2bec3168f4446084`  
		Last Modified: Wed, 03 May 2023 18:31:53 GMT  
		Size: 903.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:latest`

```console
$ docker pull emqx@sha256:755b174745a233ad8794e3a7b52ffe968656759f723f2d472128ff7a513b9ca1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:latest` - linux; amd64

```console
$ docker pull emqx@sha256:bf9cbff4d72692150db0b8e71c12169682e4a1ecabaf31a0815a124b2c8c7191
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.4 MB (110351254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:324d003bff51e7326b599161e64280e9fb441616cc376c65b64979a6e57e1fca`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 12 Apr 2023 00:20:06 GMT
ADD file:11b1acca3f68b5c5787e292ff8dbdd114964a7272bf3519ab07710cbc01a0838 in / 
# Wed, 12 Apr 2023 00:20:06 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 00:42:50 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 00:42:51 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Thu, 27 Apr 2023 18:19:36 GMT
ENV EMQX_VERSION=5.0.24
# Thu, 27 Apr 2023 18:19:36 GMT
ENV AMD64_SHA256=d104bc3e1839447f5ceeaadbb3feb6c604c5f74b07ca33ab4c37baf2a9b33ae3
# Thu, 27 Apr 2023 18:19:36 GMT
ENV ARM64_SHA256=40d387b7d4dfc4aa7162ef628f25bcb33e8a3fc67740b3cdb5a6d843aa87c2ec
# Thu, 27 Apr 2023 18:19:36 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 27 Apr 2023 18:19:43 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg} &&     echo "$sha256 *$pkg" | sha256sum -c &&     mkdir /opt/emqx &&     tar zxf $pkg -C /opt/emqx &&     chgrp -Rf emqx /opt/emqx &&     chmod -Rf g+w /opt/emqx &&     chown -Rf emqx /opt/emqx &&     ln -s /opt/emqx/bin/* /usr/local/bin/ &&     rm -f $pkg
# Thu, 27 Apr 2023 18:19:43 GMT
WORKDIR /opt/emqx
# Thu, 27 Apr 2023 18:19:44 GMT
USER emqx
# Thu, 27 Apr 2023 18:19:44 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 27 Apr 2023 18:19:44 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Thu, 27 Apr 2023 18:19:44 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Thu, 27 Apr 2023 18:19:44 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 27 Apr 2023 18:19:44 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:26c5c85e47da3022f1bdb9a112103646c5c29517d757e95426f16e4bd9533405`  
		Last Modified: Wed, 12 Apr 2023 00:23:43 GMT  
		Size: 31.4 MB (31418228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f79c821cbd23fa1420033390e2828e0922b8efe06687c960eb7ff40edfbd0d6`  
		Last Modified: Wed, 12 Apr 2023 00:43:23 GMT  
		Size: 3.0 MB (2987825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:048c1bdd86f15f4d429d049f898a2d3c0f0732c5b7e68a31b824acae055655d8`  
		Last Modified: Wed, 12 Apr 2023 00:43:22 GMT  
		Size: 4.1 KB (4105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53ffb33fdb8e8734d8315c830f113b34280d1b709d9b2022540e77ce0012c71a`  
		Last Modified: Thu, 27 Apr 2023 18:20:04 GMT  
		Size: 75.9 MB (75940194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baedd37ee870a8649d239a5d45f6d6c498c1a0da32321dfdf8af290f463d9969`  
		Last Modified: Thu, 27 Apr 2023 18:19:55 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:latest` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:4b50e10fb46731814c64c2f4895fb915e46bed6a02dbfb2c47f1cc850549541e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.4 MB (101420929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb178575b71345d1c69f7ed729a26d14a2f31906a357eb0af08e7bdacf1ea59a`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 03 May 2023 00:22:49 GMT
ADD file:66d4d9078579608530442620145336062a293cc19f159b154a63a1bcdcce3f4c in / 
# Wed, 03 May 2023 00:22:50 GMT
CMD ["bash"]
# Wed, 03 May 2023 18:31:21 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 18:31:22 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Wed, 03 May 2023 18:31:22 GMT
ENV EMQX_VERSION=5.0.24
# Wed, 03 May 2023 18:31:22 GMT
ENV AMD64_SHA256=d104bc3e1839447f5ceeaadbb3feb6c604c5f74b07ca33ab4c37baf2a9b33ae3
# Wed, 03 May 2023 18:31:22 GMT
ENV ARM64_SHA256=40d387b7d4dfc4aa7162ef628f25bcb33e8a3fc67740b3cdb5a6d843aa87c2ec
# Wed, 03 May 2023 18:31:22 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 03 May 2023 18:31:28 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg} &&     echo "$sha256 *$pkg" | sha256sum -c &&     mkdir /opt/emqx &&     tar zxf $pkg -C /opt/emqx &&     chgrp -Rf emqx /opt/emqx &&     chmod -Rf g+w /opt/emqx &&     chown -Rf emqx /opt/emqx &&     ln -s /opt/emqx/bin/* /usr/local/bin/ &&     rm -f $pkg
# Wed, 03 May 2023 18:31:29 GMT
WORKDIR /opt/emqx
# Wed, 03 May 2023 18:31:29 GMT
USER emqx
# Wed, 03 May 2023 18:31:29 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 03 May 2023 18:31:29 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Wed, 03 May 2023 18:31:30 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Wed, 03 May 2023 18:31:30 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 03 May 2023 18:31:30 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:b5d25b35c1dbfa256bea3dd164b2048d6c7f8074a555213c493c36f07bf4c559`  
		Last Modified: Wed, 03 May 2023 00:25:53 GMT  
		Size: 30.1 MB (30052733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a64a0a959a91944f5ffb31084a10b9b4826a9d805233e915031b76e42b602615`  
		Last Modified: Wed, 03 May 2023 18:31:54 GMT  
		Size: 3.0 MB (3003014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56882cfb1383ca5cd03757133ba3ae8958e9dcda03842b24d3ea7be1a5976eae`  
		Last Modified: Wed, 03 May 2023 18:31:53 GMT  
		Size: 4.1 KB (4111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f17d94cdbd45a137fdd4e9550c9063287635b1f489a5643b0d1ef2b4b97988a0`  
		Last Modified: Wed, 03 May 2023 18:32:00 GMT  
		Size: 68.4 MB (68360168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0135dc909c80db97e23cd34ad7cb67e57fe22c9cc1b3e4fd2bec3168f4446084`  
		Last Modified: Wed, 03 May 2023 18:31:53 GMT  
		Size: 903.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
