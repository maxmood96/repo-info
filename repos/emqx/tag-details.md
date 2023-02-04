<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `emqx`

-	[`emqx:4`](#emqx4)
-	[`emqx:4.3`](#emqx43)
-	[`emqx:4.3.22`](#emqx4322)
-	[`emqx:4.4`](#emqx44)
-	[`emqx:4.4.14`](#emqx4414)
-	[`emqx:5`](#emqx5)
-	[`emqx:5.0`](#emqx50)
-	[`emqx:5.0.16`](#emqx5016)
-	[`emqx:latest`](#emqxlatest)

## `emqx:4`

```console
$ docker pull emqx@sha256:7d2edc7005268a5801fb888c88ad71f8c2646249a1cba216cfb25b5d055de426
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:4` - linux; amd64

```console
$ docker pull emqx@sha256:68e3c4cf14de12049f185ed10856a20c4d2877fc25b1bbd46b361f014021eb1f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.2 MB (81163364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8ccd049b8d4801b9210896ff4dfc14728bd48e22f959425075f4ed83f7d77a2`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Sat, 04 Feb 2023 06:51:41 GMT
ADD file:1d256392bb7afe6942d157db84ca62774ac4114f8a3816fd50bace8d73130b57 in / 
# Sat, 04 Feb 2023 06:51:41 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 09:43:07 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 09:43:08 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx
# Sat, 04 Feb 2023 09:43:08 GMT
ENV EMQX_VERSION=4.4.14
# Sat, 04 Feb 2023 09:43:08 GMT
ENV OTP=otp24.3.4.2-1
# Sat, 04 Feb 2023 09:43:12 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="b70590c16effa60759f6ab08a4a0e666ad4487cf0eb88263ab992e44b440b815"; fi;     if [ ${arch} = "arm64" ]; then sha256="98b78798577ddb7685c42dc41b7a758aacfe27924c8be4510e2057527a142ba0"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Sat, 04 Feb 2023 09:43:13 GMT
WORKDIR /opt/emqx
# Sat, 04 Feb 2023 09:43:13 GMT
USER emqx
# Sat, 04 Feb 2023 09:43:13 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Sat, 04 Feb 2023 09:43:13 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Sat, 04 Feb 2023 09:43:13 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Sat, 04 Feb 2023 09:43:13 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Sat, 04 Feb 2023 09:43:13 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:01b5b2efb836d74b8b49da819514eca52e25290d1688db59420ffb9c6b65a03c`  
		Last Modified: Sat, 04 Feb 2023 06:56:17 GMT  
		Size: 31.4 MB (31396919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44b1dd2db476ed4e57c5ca37c056259f8631cbc76152850a4dcd2384c65f5bd9`  
		Last Modified: Sat, 04 Feb 2023 09:43:57 GMT  
		Size: 2.6 MB (2569476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c2403ed3c15b3e1a815dda88b784d5f764c40c218ffeedfddbf6c1a57201d7d`  
		Last Modified: Sat, 04 Feb 2023 09:43:56 GMT  
		Size: 4.1 KB (4109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc68bef4c8d077f6c96d2f94f9a41e9895ac8958574e4454c1a5ec28e4868538`  
		Last Modified: Sat, 04 Feb 2023 09:44:01 GMT  
		Size: 47.2 MB (47191752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa3f00dd0e4af12cc33b1284d73f71e5424f6b28964c9ad75fa6ef43e812d6c6`  
		Last Modified: Sat, 04 Feb 2023 09:43:56 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:4` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:4f3833eb279e1fd88cb92fe8b65d47e9007fd389ec4800c5b3b8937ccb66308b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.6 MB (72585164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d075ee49d59bb1a9b2aa85050fa39d32355859539ee9561ae4c1d144c171503d`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Sat, 04 Feb 2023 06:17:37 GMT
ADD file:f613775c59ebd3ca219dc6bbad83115eb74bbbc1980ca4b63e7cb8ab3fa364e4 in / 
# Sat, 04 Feb 2023 06:17:37 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 06:58:16 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 06:58:17 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx
# Sat, 04 Feb 2023 06:58:17 GMT
ENV EMQX_VERSION=4.4.14
# Sat, 04 Feb 2023 06:58:17 GMT
ENV OTP=otp24.3.4.2-1
# Sat, 04 Feb 2023 06:58:21 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="b70590c16effa60759f6ab08a4a0e666ad4487cf0eb88263ab992e44b440b815"; fi;     if [ ${arch} = "arm64" ]; then sha256="98b78798577ddb7685c42dc41b7a758aacfe27924c8be4510e2057527a142ba0"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Sat, 04 Feb 2023 06:58:21 GMT
WORKDIR /opt/emqx
# Sat, 04 Feb 2023 06:58:21 GMT
USER emqx
# Sat, 04 Feb 2023 06:58:21 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Sat, 04 Feb 2023 06:58:21 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Sat, 04 Feb 2023 06:58:21 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Sat, 04 Feb 2023 06:58:21 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Sat, 04 Feb 2023 06:58:21 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:f79f8cc5c20d534298dd6317333f38b7691da6d66e063ff10699727982c852be`  
		Last Modified: Sat, 04 Feb 2023 06:21:25 GMT  
		Size: 30.0 MB (30044792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ec19e49c9f1b83bf7a10aa9acb42fc320322675664694fcef2fae78ffac35be`  
		Last Modified: Sat, 04 Feb 2023 06:59:01 GMT  
		Size: 2.6 MB (2559256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03d493f75b8396c6e4a7f2feffd26ee8057d9b7b6cad297c3996cfb6d5bc0ac8`  
		Last Modified: Sat, 04 Feb 2023 06:59:00 GMT  
		Size: 4.1 KB (4114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c811c1943693213c6c81a5bf842a147189dcae0bfef07a44a0cd6bc208374c20`  
		Last Modified: Sat, 04 Feb 2023 06:59:04 GMT  
		Size: 40.0 MB (39975894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41d52f0f105891e2e78398c2176de25fd53665f62bdb4d8e89440eb852607184`  
		Last Modified: Sat, 04 Feb 2023 06:59:00 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:4.3`

```console
$ docker pull emqx@sha256:2194436d3c0b38762a503960899820aa385e570a989fd171067a17fdaed2d39b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:4.3` - linux; amd64

```console
$ docker pull emqx@sha256:008cc35b017844bbdc406c1265402a34413632c1db958b0beb305d35b0ea7f0b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.3 MB (68297084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7724845abc4f4eea54f52e5f2b071344c1632b44f52a543527831ad55b0df508`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Sat, 04 Feb 2023 06:52:07 GMT
ADD file:4fbe1e3712cf37c85529cc81e0d03c82085203de00d64b0d669b5996e975925a in / 
# Sat, 04 Feb 2023 06:52:07 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 09:42:52 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 09:42:53 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx
# Sat, 04 Feb 2023 09:42:53 GMT
ENV EMQX_VERSION=4.3.22
# Sat, 04 Feb 2023 09:42:56 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="e5f6874eb29f83cce9c84afae95cc05de11ed8aa47f046783afa1c75e812a4b7"; fi;     if [ ${arch} = "arm64" ]; then sha256="85bf586fdf1c11f4057f6137faa4390100a3f3eb0e285e8a68e63c7d15bea09b"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${ID}${VERSION_ID}-${EMQX_VERSION}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Sat, 04 Feb 2023 09:42:57 GMT
WORKDIR /opt/emqx
# Sat, 04 Feb 2023 09:42:57 GMT
USER emqx
# Sat, 04 Feb 2023 09:42:57 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Sat, 04 Feb 2023 09:42:57 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Sat, 04 Feb 2023 09:42:57 GMT
COPY file:715d536465bb73dc7e7d11b7af4806884602823836c36e9ec561de98ccbf3424 in /usr/bin/ 
# Sat, 04 Feb 2023 09:42:57 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Sat, 04 Feb 2023 09:42:57 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:0cf508b37688dca559387b506062329202aaf08b48be5f55f9278b2a818ad2c9`  
		Last Modified: Sat, 04 Feb 2023 06:56:58 GMT  
		Size: 27.1 MB (27140353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aac6f37da7b7c67d88072ab6d4b76838f237e080513cbc0c933681903cd2008b`  
		Last Modified: Sat, 04 Feb 2023 09:43:45 GMT  
		Size: 4.6 MB (4612867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02d31eb5fe3dc14e3b8b5ba81b2c6eebc1edf24a6df997467fda2e3e7a31fc14`  
		Last Modified: Sat, 04 Feb 2023 09:43:44 GMT  
		Size: 4.1 KB (4105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4ced84bd691c557b242898d34bfc9f71a26354eb9d93f166ea9f0a5e970ba28`  
		Last Modified: Sat, 04 Feb 2023 09:43:48 GMT  
		Size: 36.5 MB (36538718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa758931ab5521b078ff76068074b9851ed274c53f9b4a33dee0478ac6b30832`  
		Last Modified: Sat, 04 Feb 2023 09:43:44 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:4.3` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:fc7986c666bd10ad6a53c1acb232080b84174434a5d36ecb4b2fa3a0d4666108
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.6 MB (66636280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:130ef8d5f10e6b27081e90fc43f04a5b782e56f97adda24785cabc80a7153f9d`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Sat, 04 Feb 2023 06:17:54 GMT
ADD file:cf6ecb1d6b034b0d4fc309542cb25fff0c997661b323f524ecc258ac323e43f6 in / 
# Sat, 04 Feb 2023 06:17:55 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 06:58:05 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 06:58:05 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx
# Sat, 04 Feb 2023 06:58:06 GMT
ENV EMQX_VERSION=4.3.22
# Sat, 04 Feb 2023 06:58:09 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="e5f6874eb29f83cce9c84afae95cc05de11ed8aa47f046783afa1c75e812a4b7"; fi;     if [ ${arch} = "arm64" ]; then sha256="85bf586fdf1c11f4057f6137faa4390100a3f3eb0e285e8a68e63c7d15bea09b"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${ID}${VERSION_ID}-${EMQX_VERSION}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Sat, 04 Feb 2023 06:58:09 GMT
WORKDIR /opt/emqx
# Sat, 04 Feb 2023 06:58:09 GMT
USER emqx
# Sat, 04 Feb 2023 06:58:09 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Sat, 04 Feb 2023 06:58:10 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Sat, 04 Feb 2023 06:58:10 GMT
COPY file:715d536465bb73dc7e7d11b7af4806884602823836c36e9ec561de98ccbf3424 in /usr/bin/ 
# Sat, 04 Feb 2023 06:58:10 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Sat, 04 Feb 2023 06:58:10 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:bd2853c1424a5596deda2f31e1f82920613a03c667c3ff58cb461340b7bb89cd`  
		Last Modified: Sat, 04 Feb 2023 06:22:04 GMT  
		Size: 25.9 MB (25922631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28ad649ff2be9c41db4434f42a3e7a7481d41fcfa1259fb1c8290eb259812a26`  
		Last Modified: Sat, 04 Feb 2023 06:58:50 GMT  
		Size: 4.5 MB (4490611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8be082951b179c83e960fdc4c9f869e0cc81c0af48b34c3b20ca99daf78bdc36`  
		Last Modified: Sat, 04 Feb 2023 06:58:49 GMT  
		Size: 4.1 KB (4111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f90827bc4623d04b7905a87aeb3b35f60f34699f3c6d3cd9611cd20be107f1fe`  
		Last Modified: Sat, 04 Feb 2023 06:58:52 GMT  
		Size: 36.2 MB (36217886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3487570ed0dd7c61b0d01a35bf1f3fd9a948cbaa24f05951e6538397cbeef454`  
		Last Modified: Sat, 04 Feb 2023 06:58:49 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:4.3.22`

```console
$ docker pull emqx@sha256:2194436d3c0b38762a503960899820aa385e570a989fd171067a17fdaed2d39b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:4.3.22` - linux; amd64

```console
$ docker pull emqx@sha256:008cc35b017844bbdc406c1265402a34413632c1db958b0beb305d35b0ea7f0b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.3 MB (68297084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7724845abc4f4eea54f52e5f2b071344c1632b44f52a543527831ad55b0df508`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Sat, 04 Feb 2023 06:52:07 GMT
ADD file:4fbe1e3712cf37c85529cc81e0d03c82085203de00d64b0d669b5996e975925a in / 
# Sat, 04 Feb 2023 06:52:07 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 09:42:52 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 09:42:53 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx
# Sat, 04 Feb 2023 09:42:53 GMT
ENV EMQX_VERSION=4.3.22
# Sat, 04 Feb 2023 09:42:56 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="e5f6874eb29f83cce9c84afae95cc05de11ed8aa47f046783afa1c75e812a4b7"; fi;     if [ ${arch} = "arm64" ]; then sha256="85bf586fdf1c11f4057f6137faa4390100a3f3eb0e285e8a68e63c7d15bea09b"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${ID}${VERSION_ID}-${EMQX_VERSION}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Sat, 04 Feb 2023 09:42:57 GMT
WORKDIR /opt/emqx
# Sat, 04 Feb 2023 09:42:57 GMT
USER emqx
# Sat, 04 Feb 2023 09:42:57 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Sat, 04 Feb 2023 09:42:57 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Sat, 04 Feb 2023 09:42:57 GMT
COPY file:715d536465bb73dc7e7d11b7af4806884602823836c36e9ec561de98ccbf3424 in /usr/bin/ 
# Sat, 04 Feb 2023 09:42:57 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Sat, 04 Feb 2023 09:42:57 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:0cf508b37688dca559387b506062329202aaf08b48be5f55f9278b2a818ad2c9`  
		Last Modified: Sat, 04 Feb 2023 06:56:58 GMT  
		Size: 27.1 MB (27140353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aac6f37da7b7c67d88072ab6d4b76838f237e080513cbc0c933681903cd2008b`  
		Last Modified: Sat, 04 Feb 2023 09:43:45 GMT  
		Size: 4.6 MB (4612867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02d31eb5fe3dc14e3b8b5ba81b2c6eebc1edf24a6df997467fda2e3e7a31fc14`  
		Last Modified: Sat, 04 Feb 2023 09:43:44 GMT  
		Size: 4.1 KB (4105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4ced84bd691c557b242898d34bfc9f71a26354eb9d93f166ea9f0a5e970ba28`  
		Last Modified: Sat, 04 Feb 2023 09:43:48 GMT  
		Size: 36.5 MB (36538718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa758931ab5521b078ff76068074b9851ed274c53f9b4a33dee0478ac6b30832`  
		Last Modified: Sat, 04 Feb 2023 09:43:44 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:4.3.22` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:fc7986c666bd10ad6a53c1acb232080b84174434a5d36ecb4b2fa3a0d4666108
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.6 MB (66636280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:130ef8d5f10e6b27081e90fc43f04a5b782e56f97adda24785cabc80a7153f9d`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Sat, 04 Feb 2023 06:17:54 GMT
ADD file:cf6ecb1d6b034b0d4fc309542cb25fff0c997661b323f524ecc258ac323e43f6 in / 
# Sat, 04 Feb 2023 06:17:55 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 06:58:05 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 06:58:05 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx
# Sat, 04 Feb 2023 06:58:06 GMT
ENV EMQX_VERSION=4.3.22
# Sat, 04 Feb 2023 06:58:09 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="e5f6874eb29f83cce9c84afae95cc05de11ed8aa47f046783afa1c75e812a4b7"; fi;     if [ ${arch} = "arm64" ]; then sha256="85bf586fdf1c11f4057f6137faa4390100a3f3eb0e285e8a68e63c7d15bea09b"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${ID}${VERSION_ID}-${EMQX_VERSION}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Sat, 04 Feb 2023 06:58:09 GMT
WORKDIR /opt/emqx
# Sat, 04 Feb 2023 06:58:09 GMT
USER emqx
# Sat, 04 Feb 2023 06:58:09 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Sat, 04 Feb 2023 06:58:10 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Sat, 04 Feb 2023 06:58:10 GMT
COPY file:715d536465bb73dc7e7d11b7af4806884602823836c36e9ec561de98ccbf3424 in /usr/bin/ 
# Sat, 04 Feb 2023 06:58:10 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Sat, 04 Feb 2023 06:58:10 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:bd2853c1424a5596deda2f31e1f82920613a03c667c3ff58cb461340b7bb89cd`  
		Last Modified: Sat, 04 Feb 2023 06:22:04 GMT  
		Size: 25.9 MB (25922631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28ad649ff2be9c41db4434f42a3e7a7481d41fcfa1259fb1c8290eb259812a26`  
		Last Modified: Sat, 04 Feb 2023 06:58:50 GMT  
		Size: 4.5 MB (4490611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8be082951b179c83e960fdc4c9f869e0cc81c0af48b34c3b20ca99daf78bdc36`  
		Last Modified: Sat, 04 Feb 2023 06:58:49 GMT  
		Size: 4.1 KB (4111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f90827bc4623d04b7905a87aeb3b35f60f34699f3c6d3cd9611cd20be107f1fe`  
		Last Modified: Sat, 04 Feb 2023 06:58:52 GMT  
		Size: 36.2 MB (36217886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3487570ed0dd7c61b0d01a35bf1f3fd9a948cbaa24f05951e6538397cbeef454`  
		Last Modified: Sat, 04 Feb 2023 06:58:49 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:4.4`

```console
$ docker pull emqx@sha256:7d2edc7005268a5801fb888c88ad71f8c2646249a1cba216cfb25b5d055de426
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:4.4` - linux; amd64

```console
$ docker pull emqx@sha256:68e3c4cf14de12049f185ed10856a20c4d2877fc25b1bbd46b361f014021eb1f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.2 MB (81163364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8ccd049b8d4801b9210896ff4dfc14728bd48e22f959425075f4ed83f7d77a2`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Sat, 04 Feb 2023 06:51:41 GMT
ADD file:1d256392bb7afe6942d157db84ca62774ac4114f8a3816fd50bace8d73130b57 in / 
# Sat, 04 Feb 2023 06:51:41 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 09:43:07 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 09:43:08 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx
# Sat, 04 Feb 2023 09:43:08 GMT
ENV EMQX_VERSION=4.4.14
# Sat, 04 Feb 2023 09:43:08 GMT
ENV OTP=otp24.3.4.2-1
# Sat, 04 Feb 2023 09:43:12 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="b70590c16effa60759f6ab08a4a0e666ad4487cf0eb88263ab992e44b440b815"; fi;     if [ ${arch} = "arm64" ]; then sha256="98b78798577ddb7685c42dc41b7a758aacfe27924c8be4510e2057527a142ba0"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Sat, 04 Feb 2023 09:43:13 GMT
WORKDIR /opt/emqx
# Sat, 04 Feb 2023 09:43:13 GMT
USER emqx
# Sat, 04 Feb 2023 09:43:13 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Sat, 04 Feb 2023 09:43:13 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Sat, 04 Feb 2023 09:43:13 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Sat, 04 Feb 2023 09:43:13 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Sat, 04 Feb 2023 09:43:13 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:01b5b2efb836d74b8b49da819514eca52e25290d1688db59420ffb9c6b65a03c`  
		Last Modified: Sat, 04 Feb 2023 06:56:17 GMT  
		Size: 31.4 MB (31396919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44b1dd2db476ed4e57c5ca37c056259f8631cbc76152850a4dcd2384c65f5bd9`  
		Last Modified: Sat, 04 Feb 2023 09:43:57 GMT  
		Size: 2.6 MB (2569476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c2403ed3c15b3e1a815dda88b784d5f764c40c218ffeedfddbf6c1a57201d7d`  
		Last Modified: Sat, 04 Feb 2023 09:43:56 GMT  
		Size: 4.1 KB (4109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc68bef4c8d077f6c96d2f94f9a41e9895ac8958574e4454c1a5ec28e4868538`  
		Last Modified: Sat, 04 Feb 2023 09:44:01 GMT  
		Size: 47.2 MB (47191752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa3f00dd0e4af12cc33b1284d73f71e5424f6b28964c9ad75fa6ef43e812d6c6`  
		Last Modified: Sat, 04 Feb 2023 09:43:56 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:4.4` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:4f3833eb279e1fd88cb92fe8b65d47e9007fd389ec4800c5b3b8937ccb66308b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.6 MB (72585164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d075ee49d59bb1a9b2aa85050fa39d32355859539ee9561ae4c1d144c171503d`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Sat, 04 Feb 2023 06:17:37 GMT
ADD file:f613775c59ebd3ca219dc6bbad83115eb74bbbc1980ca4b63e7cb8ab3fa364e4 in / 
# Sat, 04 Feb 2023 06:17:37 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 06:58:16 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 06:58:17 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx
# Sat, 04 Feb 2023 06:58:17 GMT
ENV EMQX_VERSION=4.4.14
# Sat, 04 Feb 2023 06:58:17 GMT
ENV OTP=otp24.3.4.2-1
# Sat, 04 Feb 2023 06:58:21 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="b70590c16effa60759f6ab08a4a0e666ad4487cf0eb88263ab992e44b440b815"; fi;     if [ ${arch} = "arm64" ]; then sha256="98b78798577ddb7685c42dc41b7a758aacfe27924c8be4510e2057527a142ba0"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Sat, 04 Feb 2023 06:58:21 GMT
WORKDIR /opt/emqx
# Sat, 04 Feb 2023 06:58:21 GMT
USER emqx
# Sat, 04 Feb 2023 06:58:21 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Sat, 04 Feb 2023 06:58:21 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Sat, 04 Feb 2023 06:58:21 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Sat, 04 Feb 2023 06:58:21 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Sat, 04 Feb 2023 06:58:21 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:f79f8cc5c20d534298dd6317333f38b7691da6d66e063ff10699727982c852be`  
		Last Modified: Sat, 04 Feb 2023 06:21:25 GMT  
		Size: 30.0 MB (30044792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ec19e49c9f1b83bf7a10aa9acb42fc320322675664694fcef2fae78ffac35be`  
		Last Modified: Sat, 04 Feb 2023 06:59:01 GMT  
		Size: 2.6 MB (2559256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03d493f75b8396c6e4a7f2feffd26ee8057d9b7b6cad297c3996cfb6d5bc0ac8`  
		Last Modified: Sat, 04 Feb 2023 06:59:00 GMT  
		Size: 4.1 KB (4114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c811c1943693213c6c81a5bf842a147189dcae0bfef07a44a0cd6bc208374c20`  
		Last Modified: Sat, 04 Feb 2023 06:59:04 GMT  
		Size: 40.0 MB (39975894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41d52f0f105891e2e78398c2176de25fd53665f62bdb4d8e89440eb852607184`  
		Last Modified: Sat, 04 Feb 2023 06:59:00 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:4.4.14`

```console
$ docker pull emqx@sha256:7d2edc7005268a5801fb888c88ad71f8c2646249a1cba216cfb25b5d055de426
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:4.4.14` - linux; amd64

```console
$ docker pull emqx@sha256:68e3c4cf14de12049f185ed10856a20c4d2877fc25b1bbd46b361f014021eb1f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.2 MB (81163364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8ccd049b8d4801b9210896ff4dfc14728bd48e22f959425075f4ed83f7d77a2`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Sat, 04 Feb 2023 06:51:41 GMT
ADD file:1d256392bb7afe6942d157db84ca62774ac4114f8a3816fd50bace8d73130b57 in / 
# Sat, 04 Feb 2023 06:51:41 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 09:43:07 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 09:43:08 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx
# Sat, 04 Feb 2023 09:43:08 GMT
ENV EMQX_VERSION=4.4.14
# Sat, 04 Feb 2023 09:43:08 GMT
ENV OTP=otp24.3.4.2-1
# Sat, 04 Feb 2023 09:43:12 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="b70590c16effa60759f6ab08a4a0e666ad4487cf0eb88263ab992e44b440b815"; fi;     if [ ${arch} = "arm64" ]; then sha256="98b78798577ddb7685c42dc41b7a758aacfe27924c8be4510e2057527a142ba0"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Sat, 04 Feb 2023 09:43:13 GMT
WORKDIR /opt/emqx
# Sat, 04 Feb 2023 09:43:13 GMT
USER emqx
# Sat, 04 Feb 2023 09:43:13 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Sat, 04 Feb 2023 09:43:13 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Sat, 04 Feb 2023 09:43:13 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Sat, 04 Feb 2023 09:43:13 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Sat, 04 Feb 2023 09:43:13 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:01b5b2efb836d74b8b49da819514eca52e25290d1688db59420ffb9c6b65a03c`  
		Last Modified: Sat, 04 Feb 2023 06:56:17 GMT  
		Size: 31.4 MB (31396919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44b1dd2db476ed4e57c5ca37c056259f8631cbc76152850a4dcd2384c65f5bd9`  
		Last Modified: Sat, 04 Feb 2023 09:43:57 GMT  
		Size: 2.6 MB (2569476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c2403ed3c15b3e1a815dda88b784d5f764c40c218ffeedfddbf6c1a57201d7d`  
		Last Modified: Sat, 04 Feb 2023 09:43:56 GMT  
		Size: 4.1 KB (4109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc68bef4c8d077f6c96d2f94f9a41e9895ac8958574e4454c1a5ec28e4868538`  
		Last Modified: Sat, 04 Feb 2023 09:44:01 GMT  
		Size: 47.2 MB (47191752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa3f00dd0e4af12cc33b1284d73f71e5424f6b28964c9ad75fa6ef43e812d6c6`  
		Last Modified: Sat, 04 Feb 2023 09:43:56 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:4.4.14` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:4f3833eb279e1fd88cb92fe8b65d47e9007fd389ec4800c5b3b8937ccb66308b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.6 MB (72585164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d075ee49d59bb1a9b2aa85050fa39d32355859539ee9561ae4c1d144c171503d`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Sat, 04 Feb 2023 06:17:37 GMT
ADD file:f613775c59ebd3ca219dc6bbad83115eb74bbbc1980ca4b63e7cb8ab3fa364e4 in / 
# Sat, 04 Feb 2023 06:17:37 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 06:58:16 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 06:58:17 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx
# Sat, 04 Feb 2023 06:58:17 GMT
ENV EMQX_VERSION=4.4.14
# Sat, 04 Feb 2023 06:58:17 GMT
ENV OTP=otp24.3.4.2-1
# Sat, 04 Feb 2023 06:58:21 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="b70590c16effa60759f6ab08a4a0e666ad4487cf0eb88263ab992e44b440b815"; fi;     if [ ${arch} = "arm64" ]; then sha256="98b78798577ddb7685c42dc41b7a758aacfe27924c8be4510e2057527a142ba0"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Sat, 04 Feb 2023 06:58:21 GMT
WORKDIR /opt/emqx
# Sat, 04 Feb 2023 06:58:21 GMT
USER emqx
# Sat, 04 Feb 2023 06:58:21 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Sat, 04 Feb 2023 06:58:21 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Sat, 04 Feb 2023 06:58:21 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Sat, 04 Feb 2023 06:58:21 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Sat, 04 Feb 2023 06:58:21 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:f79f8cc5c20d534298dd6317333f38b7691da6d66e063ff10699727982c852be`  
		Last Modified: Sat, 04 Feb 2023 06:21:25 GMT  
		Size: 30.0 MB (30044792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ec19e49c9f1b83bf7a10aa9acb42fc320322675664694fcef2fae78ffac35be`  
		Last Modified: Sat, 04 Feb 2023 06:59:01 GMT  
		Size: 2.6 MB (2559256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03d493f75b8396c6e4a7f2feffd26ee8057d9b7b6cad297c3996cfb6d5bc0ac8`  
		Last Modified: Sat, 04 Feb 2023 06:59:00 GMT  
		Size: 4.1 KB (4114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c811c1943693213c6c81a5bf842a147189dcae0bfef07a44a0cd6bc208374c20`  
		Last Modified: Sat, 04 Feb 2023 06:59:04 GMT  
		Size: 40.0 MB (39975894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41d52f0f105891e2e78398c2176de25fd53665f62bdb4d8e89440eb852607184`  
		Last Modified: Sat, 04 Feb 2023 06:59:00 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5`

```console
$ docker pull emqx@sha256:4992fafb1d05ca825ae286ee253b583077bf0ebf9e20aacfcad3159a8e064201
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5` - linux; amd64

```console
$ docker pull emqx@sha256:4cf23cfdc48b071a5192dce0e92dacf5098189b781251a083ec2262026a49ab9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.3 MB (100331710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d16d706969e1d656f9c7459c09ccd4000e0347758d882436e9b8eb140618ff6c`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Sat, 04 Feb 2023 06:51:41 GMT
ADD file:1d256392bb7afe6942d157db84ca62774ac4114f8a3816fd50bace8d73130b57 in / 
# Sat, 04 Feb 2023 06:51:41 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 09:43:21 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 09:43:22 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Sat, 04 Feb 2023 09:43:22 GMT
ENV EMQX_VERSION=5.0.16
# Sat, 04 Feb 2023 09:43:22 GMT
ENV AMD64_SHA256=ee95db4baeaa51ff19bb37104013d0a954be64478d02015466a2dfc8d825d19c
# Sat, 04 Feb 2023 09:43:22 GMT
ENV ARM64_SHA256=8bf96461796da3bb0640c0f7456e3bc36b68ddd1ab9c5dae950553645d4859a6
# Sat, 04 Feb 2023 09:43:22 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Sat, 04 Feb 2023 09:43:28 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg} &&     echo "$sha256 *$pkg" | sha256sum -c &&     mkdir /opt/emqx &&     tar zxf $pkg -C /opt/emqx &&     chgrp -Rf emqx /opt/emqx &&     chmod -Rf g+w /opt/emqx &&     chown -Rf emqx /opt/emqx &&     ln -s /opt/emqx/bin/* /usr/local/bin/ &&     rm -f $pkg
# Sat, 04 Feb 2023 09:43:29 GMT
WORKDIR /opt/emqx
# Sat, 04 Feb 2023 09:43:29 GMT
USER emqx
# Sat, 04 Feb 2023 09:43:29 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Sat, 04 Feb 2023 09:43:29 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Sat, 04 Feb 2023 09:43:29 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Sat, 04 Feb 2023 09:43:29 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Sat, 04 Feb 2023 09:43:29 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:01b5b2efb836d74b8b49da819514eca52e25290d1688db59420ffb9c6b65a03c`  
		Last Modified: Sat, 04 Feb 2023 06:56:17 GMT  
		Size: 31.4 MB (31396919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47e6532db9a038680416e8ef543353751b6e0342f58dedecf7b363df12e9e6be`  
		Last Modified: Sat, 04 Feb 2023 09:44:12 GMT  
		Size: 3.0 MB (2987639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b72559d8fff6b37b4a0f570e7efc9ed5caf76e39238f6d12b9a2a09ccc68dce`  
		Last Modified: Sat, 04 Feb 2023 09:44:12 GMT  
		Size: 4.1 KB (4105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcf3ac344ecc06a8bb2632e3dea5dc3671b248c24c3b2cd1bc155c8b8f2b34bd`  
		Last Modified: Sat, 04 Feb 2023 09:44:20 GMT  
		Size: 65.9 MB (65942144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c52952ae762e97cd22d1066e8e0ce18d0690be5fada9c84bfc3d1eeabbe11b68`  
		Last Modified: Sat, 04 Feb 2023 09:44:12 GMT  
		Size: 903.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:75aeeada68d11f4130ee5572f39867ef58f4d6e1b2cbf144b6f1cd4de82adf69
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.4 MB (91426110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:771d1a97b5fc626468184c1ec01292eb3fb63c91fcca97411350c7898154d897`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Sat, 04 Feb 2023 06:17:37 GMT
ADD file:f613775c59ebd3ca219dc6bbad83115eb74bbbc1980ca4b63e7cb8ab3fa364e4 in / 
# Sat, 04 Feb 2023 06:17:37 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 06:58:28 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 06:58:29 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Sat, 04 Feb 2023 06:58:29 GMT
ENV EMQX_VERSION=5.0.16
# Sat, 04 Feb 2023 06:58:29 GMT
ENV AMD64_SHA256=ee95db4baeaa51ff19bb37104013d0a954be64478d02015466a2dfc8d825d19c
# Sat, 04 Feb 2023 06:58:29 GMT
ENV ARM64_SHA256=8bf96461796da3bb0640c0f7456e3bc36b68ddd1ab9c5dae950553645d4859a6
# Sat, 04 Feb 2023 06:58:29 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Sat, 04 Feb 2023 06:58:33 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg} &&     echo "$sha256 *$pkg" | sha256sum -c &&     mkdir /opt/emqx &&     tar zxf $pkg -C /opt/emqx &&     chgrp -Rf emqx /opt/emqx &&     chmod -Rf g+w /opt/emqx &&     chown -Rf emqx /opt/emqx &&     ln -s /opt/emqx/bin/* /usr/local/bin/ &&     rm -f $pkg
# Sat, 04 Feb 2023 06:58:34 GMT
WORKDIR /opt/emqx
# Sat, 04 Feb 2023 06:58:34 GMT
USER emqx
# Sat, 04 Feb 2023 06:58:34 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Sat, 04 Feb 2023 06:58:34 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Sat, 04 Feb 2023 06:58:34 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Sat, 04 Feb 2023 06:58:34 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Sat, 04 Feb 2023 06:58:34 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:f79f8cc5c20d534298dd6317333f38b7691da6d66e063ff10699727982c852be`  
		Last Modified: Sat, 04 Feb 2023 06:21:25 GMT  
		Size: 30.0 MB (30044792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2df3b032d76ee04c762ca45c13d20cc97e3a552190bf307bb662aa8ad8a6b74f`  
		Last Modified: Sat, 04 Feb 2023 06:59:15 GMT  
		Size: 3.0 MB (3002716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fc23a2f376c6744b63203db8042aed32611c322263c42d2247668e256b60ec4`  
		Last Modified: Sat, 04 Feb 2023 06:59:14 GMT  
		Size: 4.1 KB (4112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:651de4374a28919ba86a076a0c255e4fe0e94de8069906a5dea43db5c34562d5`  
		Last Modified: Sat, 04 Feb 2023 06:59:20 GMT  
		Size: 58.4 MB (58373588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3932ab6d8b453c204fa46e29e69624f4b7d516c6096902028d45c137d92c71ff`  
		Last Modified: Sat, 04 Feb 2023 06:59:14 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.0`

```console
$ docker pull emqx@sha256:4992fafb1d05ca825ae286ee253b583077bf0ebf9e20aacfcad3159a8e064201
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.0` - linux; amd64

```console
$ docker pull emqx@sha256:4cf23cfdc48b071a5192dce0e92dacf5098189b781251a083ec2262026a49ab9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.3 MB (100331710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d16d706969e1d656f9c7459c09ccd4000e0347758d882436e9b8eb140618ff6c`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Sat, 04 Feb 2023 06:51:41 GMT
ADD file:1d256392bb7afe6942d157db84ca62774ac4114f8a3816fd50bace8d73130b57 in / 
# Sat, 04 Feb 2023 06:51:41 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 09:43:21 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 09:43:22 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Sat, 04 Feb 2023 09:43:22 GMT
ENV EMQX_VERSION=5.0.16
# Sat, 04 Feb 2023 09:43:22 GMT
ENV AMD64_SHA256=ee95db4baeaa51ff19bb37104013d0a954be64478d02015466a2dfc8d825d19c
# Sat, 04 Feb 2023 09:43:22 GMT
ENV ARM64_SHA256=8bf96461796da3bb0640c0f7456e3bc36b68ddd1ab9c5dae950553645d4859a6
# Sat, 04 Feb 2023 09:43:22 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Sat, 04 Feb 2023 09:43:28 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg} &&     echo "$sha256 *$pkg" | sha256sum -c &&     mkdir /opt/emqx &&     tar zxf $pkg -C /opt/emqx &&     chgrp -Rf emqx /opt/emqx &&     chmod -Rf g+w /opt/emqx &&     chown -Rf emqx /opt/emqx &&     ln -s /opt/emqx/bin/* /usr/local/bin/ &&     rm -f $pkg
# Sat, 04 Feb 2023 09:43:29 GMT
WORKDIR /opt/emqx
# Sat, 04 Feb 2023 09:43:29 GMT
USER emqx
# Sat, 04 Feb 2023 09:43:29 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Sat, 04 Feb 2023 09:43:29 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Sat, 04 Feb 2023 09:43:29 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Sat, 04 Feb 2023 09:43:29 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Sat, 04 Feb 2023 09:43:29 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:01b5b2efb836d74b8b49da819514eca52e25290d1688db59420ffb9c6b65a03c`  
		Last Modified: Sat, 04 Feb 2023 06:56:17 GMT  
		Size: 31.4 MB (31396919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47e6532db9a038680416e8ef543353751b6e0342f58dedecf7b363df12e9e6be`  
		Last Modified: Sat, 04 Feb 2023 09:44:12 GMT  
		Size: 3.0 MB (2987639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b72559d8fff6b37b4a0f570e7efc9ed5caf76e39238f6d12b9a2a09ccc68dce`  
		Last Modified: Sat, 04 Feb 2023 09:44:12 GMT  
		Size: 4.1 KB (4105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcf3ac344ecc06a8bb2632e3dea5dc3671b248c24c3b2cd1bc155c8b8f2b34bd`  
		Last Modified: Sat, 04 Feb 2023 09:44:20 GMT  
		Size: 65.9 MB (65942144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c52952ae762e97cd22d1066e8e0ce18d0690be5fada9c84bfc3d1eeabbe11b68`  
		Last Modified: Sat, 04 Feb 2023 09:44:12 GMT  
		Size: 903.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.0` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:75aeeada68d11f4130ee5572f39867ef58f4d6e1b2cbf144b6f1cd4de82adf69
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.4 MB (91426110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:771d1a97b5fc626468184c1ec01292eb3fb63c91fcca97411350c7898154d897`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Sat, 04 Feb 2023 06:17:37 GMT
ADD file:f613775c59ebd3ca219dc6bbad83115eb74bbbc1980ca4b63e7cb8ab3fa364e4 in / 
# Sat, 04 Feb 2023 06:17:37 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 06:58:28 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 06:58:29 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Sat, 04 Feb 2023 06:58:29 GMT
ENV EMQX_VERSION=5.0.16
# Sat, 04 Feb 2023 06:58:29 GMT
ENV AMD64_SHA256=ee95db4baeaa51ff19bb37104013d0a954be64478d02015466a2dfc8d825d19c
# Sat, 04 Feb 2023 06:58:29 GMT
ENV ARM64_SHA256=8bf96461796da3bb0640c0f7456e3bc36b68ddd1ab9c5dae950553645d4859a6
# Sat, 04 Feb 2023 06:58:29 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Sat, 04 Feb 2023 06:58:33 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg} &&     echo "$sha256 *$pkg" | sha256sum -c &&     mkdir /opt/emqx &&     tar zxf $pkg -C /opt/emqx &&     chgrp -Rf emqx /opt/emqx &&     chmod -Rf g+w /opt/emqx &&     chown -Rf emqx /opt/emqx &&     ln -s /opt/emqx/bin/* /usr/local/bin/ &&     rm -f $pkg
# Sat, 04 Feb 2023 06:58:34 GMT
WORKDIR /opt/emqx
# Sat, 04 Feb 2023 06:58:34 GMT
USER emqx
# Sat, 04 Feb 2023 06:58:34 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Sat, 04 Feb 2023 06:58:34 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Sat, 04 Feb 2023 06:58:34 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Sat, 04 Feb 2023 06:58:34 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Sat, 04 Feb 2023 06:58:34 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:f79f8cc5c20d534298dd6317333f38b7691da6d66e063ff10699727982c852be`  
		Last Modified: Sat, 04 Feb 2023 06:21:25 GMT  
		Size: 30.0 MB (30044792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2df3b032d76ee04c762ca45c13d20cc97e3a552190bf307bb662aa8ad8a6b74f`  
		Last Modified: Sat, 04 Feb 2023 06:59:15 GMT  
		Size: 3.0 MB (3002716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fc23a2f376c6744b63203db8042aed32611c322263c42d2247668e256b60ec4`  
		Last Modified: Sat, 04 Feb 2023 06:59:14 GMT  
		Size: 4.1 KB (4112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:651de4374a28919ba86a076a0c255e4fe0e94de8069906a5dea43db5c34562d5`  
		Last Modified: Sat, 04 Feb 2023 06:59:20 GMT  
		Size: 58.4 MB (58373588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3932ab6d8b453c204fa46e29e69624f4b7d516c6096902028d45c137d92c71ff`  
		Last Modified: Sat, 04 Feb 2023 06:59:14 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.0.16`

```console
$ docker pull emqx@sha256:4992fafb1d05ca825ae286ee253b583077bf0ebf9e20aacfcad3159a8e064201
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.0.16` - linux; amd64

```console
$ docker pull emqx@sha256:4cf23cfdc48b071a5192dce0e92dacf5098189b781251a083ec2262026a49ab9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.3 MB (100331710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d16d706969e1d656f9c7459c09ccd4000e0347758d882436e9b8eb140618ff6c`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Sat, 04 Feb 2023 06:51:41 GMT
ADD file:1d256392bb7afe6942d157db84ca62774ac4114f8a3816fd50bace8d73130b57 in / 
# Sat, 04 Feb 2023 06:51:41 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 09:43:21 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 09:43:22 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Sat, 04 Feb 2023 09:43:22 GMT
ENV EMQX_VERSION=5.0.16
# Sat, 04 Feb 2023 09:43:22 GMT
ENV AMD64_SHA256=ee95db4baeaa51ff19bb37104013d0a954be64478d02015466a2dfc8d825d19c
# Sat, 04 Feb 2023 09:43:22 GMT
ENV ARM64_SHA256=8bf96461796da3bb0640c0f7456e3bc36b68ddd1ab9c5dae950553645d4859a6
# Sat, 04 Feb 2023 09:43:22 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Sat, 04 Feb 2023 09:43:28 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg} &&     echo "$sha256 *$pkg" | sha256sum -c &&     mkdir /opt/emqx &&     tar zxf $pkg -C /opt/emqx &&     chgrp -Rf emqx /opt/emqx &&     chmod -Rf g+w /opt/emqx &&     chown -Rf emqx /opt/emqx &&     ln -s /opt/emqx/bin/* /usr/local/bin/ &&     rm -f $pkg
# Sat, 04 Feb 2023 09:43:29 GMT
WORKDIR /opt/emqx
# Sat, 04 Feb 2023 09:43:29 GMT
USER emqx
# Sat, 04 Feb 2023 09:43:29 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Sat, 04 Feb 2023 09:43:29 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Sat, 04 Feb 2023 09:43:29 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Sat, 04 Feb 2023 09:43:29 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Sat, 04 Feb 2023 09:43:29 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:01b5b2efb836d74b8b49da819514eca52e25290d1688db59420ffb9c6b65a03c`  
		Last Modified: Sat, 04 Feb 2023 06:56:17 GMT  
		Size: 31.4 MB (31396919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47e6532db9a038680416e8ef543353751b6e0342f58dedecf7b363df12e9e6be`  
		Last Modified: Sat, 04 Feb 2023 09:44:12 GMT  
		Size: 3.0 MB (2987639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b72559d8fff6b37b4a0f570e7efc9ed5caf76e39238f6d12b9a2a09ccc68dce`  
		Last Modified: Sat, 04 Feb 2023 09:44:12 GMT  
		Size: 4.1 KB (4105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcf3ac344ecc06a8bb2632e3dea5dc3671b248c24c3b2cd1bc155c8b8f2b34bd`  
		Last Modified: Sat, 04 Feb 2023 09:44:20 GMT  
		Size: 65.9 MB (65942144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c52952ae762e97cd22d1066e8e0ce18d0690be5fada9c84bfc3d1eeabbe11b68`  
		Last Modified: Sat, 04 Feb 2023 09:44:12 GMT  
		Size: 903.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.0.16` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:75aeeada68d11f4130ee5572f39867ef58f4d6e1b2cbf144b6f1cd4de82adf69
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.4 MB (91426110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:771d1a97b5fc626468184c1ec01292eb3fb63c91fcca97411350c7898154d897`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Sat, 04 Feb 2023 06:17:37 GMT
ADD file:f613775c59ebd3ca219dc6bbad83115eb74bbbc1980ca4b63e7cb8ab3fa364e4 in / 
# Sat, 04 Feb 2023 06:17:37 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 06:58:28 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 06:58:29 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Sat, 04 Feb 2023 06:58:29 GMT
ENV EMQX_VERSION=5.0.16
# Sat, 04 Feb 2023 06:58:29 GMT
ENV AMD64_SHA256=ee95db4baeaa51ff19bb37104013d0a954be64478d02015466a2dfc8d825d19c
# Sat, 04 Feb 2023 06:58:29 GMT
ENV ARM64_SHA256=8bf96461796da3bb0640c0f7456e3bc36b68ddd1ab9c5dae950553645d4859a6
# Sat, 04 Feb 2023 06:58:29 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Sat, 04 Feb 2023 06:58:33 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg} &&     echo "$sha256 *$pkg" | sha256sum -c &&     mkdir /opt/emqx &&     tar zxf $pkg -C /opt/emqx &&     chgrp -Rf emqx /opt/emqx &&     chmod -Rf g+w /opt/emqx &&     chown -Rf emqx /opt/emqx &&     ln -s /opt/emqx/bin/* /usr/local/bin/ &&     rm -f $pkg
# Sat, 04 Feb 2023 06:58:34 GMT
WORKDIR /opt/emqx
# Sat, 04 Feb 2023 06:58:34 GMT
USER emqx
# Sat, 04 Feb 2023 06:58:34 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Sat, 04 Feb 2023 06:58:34 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Sat, 04 Feb 2023 06:58:34 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Sat, 04 Feb 2023 06:58:34 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Sat, 04 Feb 2023 06:58:34 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:f79f8cc5c20d534298dd6317333f38b7691da6d66e063ff10699727982c852be`  
		Last Modified: Sat, 04 Feb 2023 06:21:25 GMT  
		Size: 30.0 MB (30044792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2df3b032d76ee04c762ca45c13d20cc97e3a552190bf307bb662aa8ad8a6b74f`  
		Last Modified: Sat, 04 Feb 2023 06:59:15 GMT  
		Size: 3.0 MB (3002716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fc23a2f376c6744b63203db8042aed32611c322263c42d2247668e256b60ec4`  
		Last Modified: Sat, 04 Feb 2023 06:59:14 GMT  
		Size: 4.1 KB (4112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:651de4374a28919ba86a076a0c255e4fe0e94de8069906a5dea43db5c34562d5`  
		Last Modified: Sat, 04 Feb 2023 06:59:20 GMT  
		Size: 58.4 MB (58373588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3932ab6d8b453c204fa46e29e69624f4b7d516c6096902028d45c137d92c71ff`  
		Last Modified: Sat, 04 Feb 2023 06:59:14 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:latest`

```console
$ docker pull emqx@sha256:4992fafb1d05ca825ae286ee253b583077bf0ebf9e20aacfcad3159a8e064201
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:latest` - linux; amd64

```console
$ docker pull emqx@sha256:4cf23cfdc48b071a5192dce0e92dacf5098189b781251a083ec2262026a49ab9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.3 MB (100331710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d16d706969e1d656f9c7459c09ccd4000e0347758d882436e9b8eb140618ff6c`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Sat, 04 Feb 2023 06:51:41 GMT
ADD file:1d256392bb7afe6942d157db84ca62774ac4114f8a3816fd50bace8d73130b57 in / 
# Sat, 04 Feb 2023 06:51:41 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 09:43:21 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 09:43:22 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Sat, 04 Feb 2023 09:43:22 GMT
ENV EMQX_VERSION=5.0.16
# Sat, 04 Feb 2023 09:43:22 GMT
ENV AMD64_SHA256=ee95db4baeaa51ff19bb37104013d0a954be64478d02015466a2dfc8d825d19c
# Sat, 04 Feb 2023 09:43:22 GMT
ENV ARM64_SHA256=8bf96461796da3bb0640c0f7456e3bc36b68ddd1ab9c5dae950553645d4859a6
# Sat, 04 Feb 2023 09:43:22 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Sat, 04 Feb 2023 09:43:28 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg} &&     echo "$sha256 *$pkg" | sha256sum -c &&     mkdir /opt/emqx &&     tar zxf $pkg -C /opt/emqx &&     chgrp -Rf emqx /opt/emqx &&     chmod -Rf g+w /opt/emqx &&     chown -Rf emqx /opt/emqx &&     ln -s /opt/emqx/bin/* /usr/local/bin/ &&     rm -f $pkg
# Sat, 04 Feb 2023 09:43:29 GMT
WORKDIR /opt/emqx
# Sat, 04 Feb 2023 09:43:29 GMT
USER emqx
# Sat, 04 Feb 2023 09:43:29 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Sat, 04 Feb 2023 09:43:29 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Sat, 04 Feb 2023 09:43:29 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Sat, 04 Feb 2023 09:43:29 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Sat, 04 Feb 2023 09:43:29 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:01b5b2efb836d74b8b49da819514eca52e25290d1688db59420ffb9c6b65a03c`  
		Last Modified: Sat, 04 Feb 2023 06:56:17 GMT  
		Size: 31.4 MB (31396919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47e6532db9a038680416e8ef543353751b6e0342f58dedecf7b363df12e9e6be`  
		Last Modified: Sat, 04 Feb 2023 09:44:12 GMT  
		Size: 3.0 MB (2987639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b72559d8fff6b37b4a0f570e7efc9ed5caf76e39238f6d12b9a2a09ccc68dce`  
		Last Modified: Sat, 04 Feb 2023 09:44:12 GMT  
		Size: 4.1 KB (4105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcf3ac344ecc06a8bb2632e3dea5dc3671b248c24c3b2cd1bc155c8b8f2b34bd`  
		Last Modified: Sat, 04 Feb 2023 09:44:20 GMT  
		Size: 65.9 MB (65942144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c52952ae762e97cd22d1066e8e0ce18d0690be5fada9c84bfc3d1eeabbe11b68`  
		Last Modified: Sat, 04 Feb 2023 09:44:12 GMT  
		Size: 903.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:latest` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:75aeeada68d11f4130ee5572f39867ef58f4d6e1b2cbf144b6f1cd4de82adf69
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.4 MB (91426110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:771d1a97b5fc626468184c1ec01292eb3fb63c91fcca97411350c7898154d897`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Sat, 04 Feb 2023 06:17:37 GMT
ADD file:f613775c59ebd3ca219dc6bbad83115eb74bbbc1980ca4b63e7cb8ab3fa364e4 in / 
# Sat, 04 Feb 2023 06:17:37 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 06:58:28 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 06:58:29 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Sat, 04 Feb 2023 06:58:29 GMT
ENV EMQX_VERSION=5.0.16
# Sat, 04 Feb 2023 06:58:29 GMT
ENV AMD64_SHA256=ee95db4baeaa51ff19bb37104013d0a954be64478d02015466a2dfc8d825d19c
# Sat, 04 Feb 2023 06:58:29 GMT
ENV ARM64_SHA256=8bf96461796da3bb0640c0f7456e3bc36b68ddd1ab9c5dae950553645d4859a6
# Sat, 04 Feb 2023 06:58:29 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Sat, 04 Feb 2023 06:58:33 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg} &&     echo "$sha256 *$pkg" | sha256sum -c &&     mkdir /opt/emqx &&     tar zxf $pkg -C /opt/emqx &&     chgrp -Rf emqx /opt/emqx &&     chmod -Rf g+w /opt/emqx &&     chown -Rf emqx /opt/emqx &&     ln -s /opt/emqx/bin/* /usr/local/bin/ &&     rm -f $pkg
# Sat, 04 Feb 2023 06:58:34 GMT
WORKDIR /opt/emqx
# Sat, 04 Feb 2023 06:58:34 GMT
USER emqx
# Sat, 04 Feb 2023 06:58:34 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Sat, 04 Feb 2023 06:58:34 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Sat, 04 Feb 2023 06:58:34 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Sat, 04 Feb 2023 06:58:34 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Sat, 04 Feb 2023 06:58:34 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:f79f8cc5c20d534298dd6317333f38b7691da6d66e063ff10699727982c852be`  
		Last Modified: Sat, 04 Feb 2023 06:21:25 GMT  
		Size: 30.0 MB (30044792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2df3b032d76ee04c762ca45c13d20cc97e3a552190bf307bb662aa8ad8a6b74f`  
		Last Modified: Sat, 04 Feb 2023 06:59:15 GMT  
		Size: 3.0 MB (3002716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fc23a2f376c6744b63203db8042aed32611c322263c42d2247668e256b60ec4`  
		Last Modified: Sat, 04 Feb 2023 06:59:14 GMT  
		Size: 4.1 KB (4112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:651de4374a28919ba86a076a0c255e4fe0e94de8069906a5dea43db5c34562d5`  
		Last Modified: Sat, 04 Feb 2023 06:59:20 GMT  
		Size: 58.4 MB (58373588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3932ab6d8b453c204fa46e29e69624f4b7d516c6096902028d45c137d92c71ff`  
		Last Modified: Sat, 04 Feb 2023 06:59:14 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
