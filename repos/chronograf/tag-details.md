<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `chronograf`

-	[`chronograf:1.10`](#chronograf110)
-	[`chronograf:1.10-alpine`](#chronograf110-alpine)
-	[`chronograf:1.10.0`](#chronograf1100)
-	[`chronograf:1.10.0-alpine`](#chronograf1100-alpine)
-	[`chronograf:1.7`](#chronograf17)
-	[`chronograf:1.7-alpine`](#chronograf17-alpine)
-	[`chronograf:1.7.17`](#chronograf1717)
-	[`chronograf:1.7.17-alpine`](#chronograf1717-alpine)
-	[`chronograf:1.8`](#chronograf18)
-	[`chronograf:1.8-alpine`](#chronograf18-alpine)
-	[`chronograf:1.8.10`](#chronograf1810)
-	[`chronograf:1.8.10-alpine`](#chronograf1810-alpine)
-	[`chronograf:1.9`](#chronograf19)
-	[`chronograf:1.9-alpine`](#chronograf19-alpine)
-	[`chronograf:1.9.4`](#chronograf194)
-	[`chronograf:1.9.4-alpine`](#chronograf194-alpine)
-	[`chronograf:alpine`](#chronografalpine)
-	[`chronograf:latest`](#chronograflatest)

## `chronograf:1.10`

```console
$ docker pull chronograf@sha256:5f801513652ec6ead872a616599e58f92915b0dc35890c7bc0e37633b07c71cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.10` - linux; amd64

```console
$ docker pull chronograf@sha256:29ab1b9d91d0c5493c5a5da0a6d8d81098d48a4217cdfe1452dcefa8b5e4a720
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.3 MB (81254093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bc3e83e2be670ef62324a08070a2c4836172d7f37b0b841a50fcc5705ea594c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 06 Dec 2022 01:20:54 GMT
ADD file:1f1efd56601ebc26a041a7b994a380ef68112b91a078e225753bee7b3196d22c in / 
# Tue, 06 Dec 2022 01:20:54 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 01:46:01 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 06 Dec 2022 01:46:27 GMT
ENV CHRONOGRAF_VERSION=1.10.0
# Tue, 06 Dec 2022 01:46:34 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 06 Dec 2022 01:46:34 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 06 Dec 2022 01:46:35 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 06 Dec 2022 01:46:35 GMT
EXPOSE 8888
# Tue, 06 Dec 2022 01:46:35 GMT
VOLUME [/var/lib/chronograf]
# Tue, 06 Dec 2022 01:46:35 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 06 Dec 2022 01:46:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 06 Dec 2022 01:46:35 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:025c56f98b679f70b7a54241917e56da7b59ab9d2defecc6ebdb0bf2750484bb`  
		Last Modified: Tue, 06 Dec 2022 01:25:12 GMT  
		Size: 31.4 MB (31412852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89ff5a347561490589cdaddbb9c1d1fd79814edac3ddf8bc928b34dddfd7c5bb`  
		Last Modified: Tue, 06 Dec 2022 01:47:14 GMT  
		Size: 5.2 MB (5228712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a86e4af0a7ab80153783e9829b83a062eb28cb99ba473fdb07e876952c8354b1`  
		Last Modified: Tue, 06 Dec 2022 01:47:47 GMT  
		Size: 44.6 MB (44588133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edc2df382812100ec1f9eee6ae9216b67d9d9ae41984fab817ddf26ef056701d`  
		Last Modified: Tue, 06 Dec 2022 01:47:41 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbb68818fcfd812eb6559bb580d3b5be78474c1a0bda9b702987437c87c66309`  
		Last Modified: Tue, 06 Dec 2022 01:47:41 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c1a18d308edf2a5a71cfaffc3459b9585962a4b199e557cc2c662df81a27165`  
		Last Modified: Tue, 06 Dec 2022 01:47:41 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.10` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:940df312875251e09bb551952c88e719e921217382ca2c0e458d679581d0206b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.6 MB (73560703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d46c8e5d166b1c72df66ec7e56027579e92b228d2e13fff21043839e020152f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 06 Dec 2022 00:58:51 GMT
ADD file:cb354f875d5631d5d4542ab57d0b9b323a261f5c631d5917127504d6eb54d85a in / 
# Tue, 06 Dec 2022 00:58:52 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 10:15:54 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 06 Dec 2022 10:16:29 GMT
ENV CHRONOGRAF_VERSION=1.10.0
# Tue, 06 Dec 2022 10:16:38 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 06 Dec 2022 10:16:38 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 06 Dec 2022 10:16:38 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 06 Dec 2022 10:16:38 GMT
EXPOSE 8888
# Tue, 06 Dec 2022 10:16:39 GMT
VOLUME [/var/lib/chronograf]
# Tue, 06 Dec 2022 10:16:39 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 06 Dec 2022 10:16:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 06 Dec 2022 10:16:39 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:4f32a98d14d26603bb8e8cf9bda992e24606d2fe00101767049a01d5176929e1`  
		Last Modified: Tue, 06 Dec 2022 01:06:05 GMT  
		Size: 26.6 MB (26576348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13331aa96eaee2e9e3ef374955946cbe0508467ec66e9c44cb3122bc85393b6e`  
		Last Modified: Tue, 06 Dec 2022 10:17:29 GMT  
		Size: 4.5 MB (4495026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72b493b2a2579f2080785c4a4e7d3db8e4d7e25e6e0afce8a048cafd3b0c0cfb`  
		Last Modified: Tue, 06 Dec 2022 10:18:08 GMT  
		Size: 42.5 MB (42464936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8875c67483f82bc20ddf506d0b3f57cac5bdc74b4ff8c31caf40a6b3b8931597`  
		Last Modified: Tue, 06 Dec 2022 10:18:00 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1458f13cd06ea42cd5ae8d1d467c93cf83f290077dad0887a29a5b3f74a87596`  
		Last Modified: Tue, 06 Dec 2022 10:18:00 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31c35ed9bc20a5bb6678297d9f268738785c2af7b2a63949d0ad2e4dd873b310`  
		Last Modified: Tue, 06 Dec 2022 10:18:00 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.10` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:b9a923a7f9577ea18562ca96d20f9092d3564d8b7fdbab907678a2125762c73d
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.9 MB (77914187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36b562de4f793f8bfe522fb78778dadf5df254c69bff24023d08eda93fbfe602`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 06 Dec 2022 01:40:17 GMT
ADD file:379d6ac56afdb6e02d71fa0faebc13b8a2554fc6ae76c5f5bbdb5b8e475135d6 in / 
# Tue, 06 Dec 2022 01:40:17 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 02:15:19 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 06 Dec 2022 02:15:36 GMT
ENV CHRONOGRAF_VERSION=1.10.0
# Tue, 06 Dec 2022 02:15:41 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 06 Dec 2022 02:15:42 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 06 Dec 2022 02:15:42 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 06 Dec 2022 02:15:42 GMT
EXPOSE 8888
# Tue, 06 Dec 2022 02:15:42 GMT
VOLUME [/var/lib/chronograf]
# Tue, 06 Dec 2022 02:15:42 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 06 Dec 2022 02:15:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 06 Dec 2022 02:15:43 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:6064e7e5b6afa4dc711228eddfd250aebac271830dc184c400ce640020bc2cb0`  
		Last Modified: Tue, 06 Dec 2022 01:43:56 GMT  
		Size: 30.1 MB (30060320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:010bcfd47e4f0331c64dfb2af5573bf99a4b88b4d972387850c61ff6ef0d11a9`  
		Last Modified: Tue, 06 Dec 2022 02:16:10 GMT  
		Size: 5.2 MB (5211566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f63cfceb30c24c808b43865619c58241102c036bd153c354e2f2f1457954400`  
		Last Modified: Tue, 06 Dec 2022 02:16:37 GMT  
		Size: 42.6 MB (42617907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb34459112efb5b29d1c5cbe97dad350e283c8259b45e077aa3104ff0a7c432b`  
		Last Modified: Tue, 06 Dec 2022 02:16:32 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21072e41358457fcdb1399f31b7dd73322af50a96fc66fe37b8841d39bb92579`  
		Last Modified: Tue, 06 Dec 2022 02:16:32 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ca77523a925a0d9872b733837dba904a8a82c95de486d5f95f5bf8678deb165`  
		Last Modified: Tue, 06 Dec 2022 02:16:32 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.10-alpine`

```console
$ docker pull chronograf@sha256:c92d2e5d3aaed3d5abd3e21e85b3dd60e8169f7bf6699f473aed28eabff1d043
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.10-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:de6c4148eeb1291ced92120697fad8332c74a726171672daf7c7b67e21d3850b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30311143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d58f859d1dc29bb2ee9f917635f6eb5621000d9d6619ec8ad4549203995550f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:07 GMT
ADD file:b9bd10cf83356cb7281baa0fbaca5186cf27491f59eda87abe57f83a5aaf5ec1 in / 
# Tue, 09 Aug 2022 17:20:08 GMT
CMD ["/bin/sh"]
# Thu, 06 Oct 2022 20:15:36 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 06 Oct 2022 20:15:37 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Thu, 06 Oct 2022 20:16:09 GMT
ENV CHRONOGRAF_VERSION=1.10.0
# Thu, 06 Oct 2022 20:16:16 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 06 Oct 2022 20:16:17 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 06 Oct 2022 20:16:17 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 06 Oct 2022 20:16:17 GMT
EXPOSE 8888
# Thu, 06 Oct 2022 20:16:17 GMT
VOLUME [/var/lib/chronograf]
# Thu, 06 Oct 2022 20:16:17 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Thu, 06 Oct 2022 20:16:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 06 Oct 2022 20:16:17 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:c7ed990a2339ee598662849de4f56e2241399f5a32340c8c4a7bbd5378a12b5f`  
		Last Modified: Tue, 09 Aug 2022 17:21:06 GMT  
		Size: 2.8 MB (2827489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:133509570f70da73b5369d8311a4269568dbea851313f10ea1b8cb1a2c4e2fe8`  
		Last Modified: Thu, 06 Oct 2022 20:16:43 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ed07ae854e5b9e7d93d0c5eb8bbcfb2d6e5eddeb00720efe7b55766ce5bfbab`  
		Last Modified: Thu, 06 Oct 2022 20:16:41 GMT  
		Size: 284.6 KB (284583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eea9d4a8a69cd5e2e5fca1b123ba2cd44364cf36b128c2fe59a5edf12221dfd`  
		Last Modified: Thu, 06 Oct 2022 20:17:26 GMT  
		Size: 27.2 MB (27174517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76a685cca594b365e8c9e5d2a452959ac02b6fde12a79d898abf1a833a483707`  
		Last Modified: Thu, 06 Oct 2022 20:17:21 GMT  
		Size: 12.3 KB (12265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80dba48a5545ef21547b2590458104e7bf680e4a5afbd1707de156d2d9420751`  
		Last Modified: Thu, 06 Oct 2022 20:17:21 GMT  
		Size: 11.9 KB (11897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ece5a9a06b7739faf864ebca0e4561819e3e331b928666a09e2c5bb2b9b2181`  
		Last Modified: Thu, 06 Oct 2022 20:17:21 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.10.0`

```console
$ docker pull chronograf@sha256:5f801513652ec6ead872a616599e58f92915b0dc35890c7bc0e37633b07c71cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.10.0` - linux; amd64

```console
$ docker pull chronograf@sha256:29ab1b9d91d0c5493c5a5da0a6d8d81098d48a4217cdfe1452dcefa8b5e4a720
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.3 MB (81254093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bc3e83e2be670ef62324a08070a2c4836172d7f37b0b841a50fcc5705ea594c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 06 Dec 2022 01:20:54 GMT
ADD file:1f1efd56601ebc26a041a7b994a380ef68112b91a078e225753bee7b3196d22c in / 
# Tue, 06 Dec 2022 01:20:54 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 01:46:01 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 06 Dec 2022 01:46:27 GMT
ENV CHRONOGRAF_VERSION=1.10.0
# Tue, 06 Dec 2022 01:46:34 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 06 Dec 2022 01:46:34 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 06 Dec 2022 01:46:35 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 06 Dec 2022 01:46:35 GMT
EXPOSE 8888
# Tue, 06 Dec 2022 01:46:35 GMT
VOLUME [/var/lib/chronograf]
# Tue, 06 Dec 2022 01:46:35 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 06 Dec 2022 01:46:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 06 Dec 2022 01:46:35 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:025c56f98b679f70b7a54241917e56da7b59ab9d2defecc6ebdb0bf2750484bb`  
		Last Modified: Tue, 06 Dec 2022 01:25:12 GMT  
		Size: 31.4 MB (31412852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89ff5a347561490589cdaddbb9c1d1fd79814edac3ddf8bc928b34dddfd7c5bb`  
		Last Modified: Tue, 06 Dec 2022 01:47:14 GMT  
		Size: 5.2 MB (5228712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a86e4af0a7ab80153783e9829b83a062eb28cb99ba473fdb07e876952c8354b1`  
		Last Modified: Tue, 06 Dec 2022 01:47:47 GMT  
		Size: 44.6 MB (44588133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edc2df382812100ec1f9eee6ae9216b67d9d9ae41984fab817ddf26ef056701d`  
		Last Modified: Tue, 06 Dec 2022 01:47:41 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbb68818fcfd812eb6559bb580d3b5be78474c1a0bda9b702987437c87c66309`  
		Last Modified: Tue, 06 Dec 2022 01:47:41 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c1a18d308edf2a5a71cfaffc3459b9585962a4b199e557cc2c662df81a27165`  
		Last Modified: Tue, 06 Dec 2022 01:47:41 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.10.0` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:940df312875251e09bb551952c88e719e921217382ca2c0e458d679581d0206b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.6 MB (73560703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d46c8e5d166b1c72df66ec7e56027579e92b228d2e13fff21043839e020152f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 06 Dec 2022 00:58:51 GMT
ADD file:cb354f875d5631d5d4542ab57d0b9b323a261f5c631d5917127504d6eb54d85a in / 
# Tue, 06 Dec 2022 00:58:52 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 10:15:54 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 06 Dec 2022 10:16:29 GMT
ENV CHRONOGRAF_VERSION=1.10.0
# Tue, 06 Dec 2022 10:16:38 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 06 Dec 2022 10:16:38 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 06 Dec 2022 10:16:38 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 06 Dec 2022 10:16:38 GMT
EXPOSE 8888
# Tue, 06 Dec 2022 10:16:39 GMT
VOLUME [/var/lib/chronograf]
# Tue, 06 Dec 2022 10:16:39 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 06 Dec 2022 10:16:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 06 Dec 2022 10:16:39 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:4f32a98d14d26603bb8e8cf9bda992e24606d2fe00101767049a01d5176929e1`  
		Last Modified: Tue, 06 Dec 2022 01:06:05 GMT  
		Size: 26.6 MB (26576348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13331aa96eaee2e9e3ef374955946cbe0508467ec66e9c44cb3122bc85393b6e`  
		Last Modified: Tue, 06 Dec 2022 10:17:29 GMT  
		Size: 4.5 MB (4495026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72b493b2a2579f2080785c4a4e7d3db8e4d7e25e6e0afce8a048cafd3b0c0cfb`  
		Last Modified: Tue, 06 Dec 2022 10:18:08 GMT  
		Size: 42.5 MB (42464936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8875c67483f82bc20ddf506d0b3f57cac5bdc74b4ff8c31caf40a6b3b8931597`  
		Last Modified: Tue, 06 Dec 2022 10:18:00 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1458f13cd06ea42cd5ae8d1d467c93cf83f290077dad0887a29a5b3f74a87596`  
		Last Modified: Tue, 06 Dec 2022 10:18:00 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31c35ed9bc20a5bb6678297d9f268738785c2af7b2a63949d0ad2e4dd873b310`  
		Last Modified: Tue, 06 Dec 2022 10:18:00 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.10.0` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:b9a923a7f9577ea18562ca96d20f9092d3564d8b7fdbab907678a2125762c73d
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.9 MB (77914187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36b562de4f793f8bfe522fb78778dadf5df254c69bff24023d08eda93fbfe602`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 06 Dec 2022 01:40:17 GMT
ADD file:379d6ac56afdb6e02d71fa0faebc13b8a2554fc6ae76c5f5bbdb5b8e475135d6 in / 
# Tue, 06 Dec 2022 01:40:17 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 02:15:19 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 06 Dec 2022 02:15:36 GMT
ENV CHRONOGRAF_VERSION=1.10.0
# Tue, 06 Dec 2022 02:15:41 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 06 Dec 2022 02:15:42 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 06 Dec 2022 02:15:42 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 06 Dec 2022 02:15:42 GMT
EXPOSE 8888
# Tue, 06 Dec 2022 02:15:42 GMT
VOLUME [/var/lib/chronograf]
# Tue, 06 Dec 2022 02:15:42 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 06 Dec 2022 02:15:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 06 Dec 2022 02:15:43 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:6064e7e5b6afa4dc711228eddfd250aebac271830dc184c400ce640020bc2cb0`  
		Last Modified: Tue, 06 Dec 2022 01:43:56 GMT  
		Size: 30.1 MB (30060320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:010bcfd47e4f0331c64dfb2af5573bf99a4b88b4d972387850c61ff6ef0d11a9`  
		Last Modified: Tue, 06 Dec 2022 02:16:10 GMT  
		Size: 5.2 MB (5211566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f63cfceb30c24c808b43865619c58241102c036bd153c354e2f2f1457954400`  
		Last Modified: Tue, 06 Dec 2022 02:16:37 GMT  
		Size: 42.6 MB (42617907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb34459112efb5b29d1c5cbe97dad350e283c8259b45e077aa3104ff0a7c432b`  
		Last Modified: Tue, 06 Dec 2022 02:16:32 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21072e41358457fcdb1399f31b7dd73322af50a96fc66fe37b8841d39bb92579`  
		Last Modified: Tue, 06 Dec 2022 02:16:32 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ca77523a925a0d9872b733837dba904a8a82c95de486d5f95f5bf8678deb165`  
		Last Modified: Tue, 06 Dec 2022 02:16:32 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.10.0-alpine`

```console
$ docker pull chronograf@sha256:c92d2e5d3aaed3d5abd3e21e85b3dd60e8169f7bf6699f473aed28eabff1d043
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.10.0-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:de6c4148eeb1291ced92120697fad8332c74a726171672daf7c7b67e21d3850b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30311143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d58f859d1dc29bb2ee9f917635f6eb5621000d9d6619ec8ad4549203995550f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:07 GMT
ADD file:b9bd10cf83356cb7281baa0fbaca5186cf27491f59eda87abe57f83a5aaf5ec1 in / 
# Tue, 09 Aug 2022 17:20:08 GMT
CMD ["/bin/sh"]
# Thu, 06 Oct 2022 20:15:36 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 06 Oct 2022 20:15:37 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Thu, 06 Oct 2022 20:16:09 GMT
ENV CHRONOGRAF_VERSION=1.10.0
# Thu, 06 Oct 2022 20:16:16 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 06 Oct 2022 20:16:17 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 06 Oct 2022 20:16:17 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 06 Oct 2022 20:16:17 GMT
EXPOSE 8888
# Thu, 06 Oct 2022 20:16:17 GMT
VOLUME [/var/lib/chronograf]
# Thu, 06 Oct 2022 20:16:17 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Thu, 06 Oct 2022 20:16:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 06 Oct 2022 20:16:17 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:c7ed990a2339ee598662849de4f56e2241399f5a32340c8c4a7bbd5378a12b5f`  
		Last Modified: Tue, 09 Aug 2022 17:21:06 GMT  
		Size: 2.8 MB (2827489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:133509570f70da73b5369d8311a4269568dbea851313f10ea1b8cb1a2c4e2fe8`  
		Last Modified: Thu, 06 Oct 2022 20:16:43 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ed07ae854e5b9e7d93d0c5eb8bbcfb2d6e5eddeb00720efe7b55766ce5bfbab`  
		Last Modified: Thu, 06 Oct 2022 20:16:41 GMT  
		Size: 284.6 KB (284583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eea9d4a8a69cd5e2e5fca1b123ba2cd44364cf36b128c2fe59a5edf12221dfd`  
		Last Modified: Thu, 06 Oct 2022 20:17:26 GMT  
		Size: 27.2 MB (27174517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76a685cca594b365e8c9e5d2a452959ac02b6fde12a79d898abf1a833a483707`  
		Last Modified: Thu, 06 Oct 2022 20:17:21 GMT  
		Size: 12.3 KB (12265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80dba48a5545ef21547b2590458104e7bf680e4a5afbd1707de156d2d9420751`  
		Last Modified: Thu, 06 Oct 2022 20:17:21 GMT  
		Size: 11.9 KB (11897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ece5a9a06b7739faf864ebca0e4561819e3e331b928666a09e2c5bb2b9b2181`  
		Last Modified: Thu, 06 Oct 2022 20:17:21 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.7`

```console
$ docker pull chronograf@sha256:d1615c1102005b2aaf7674aa038279c08853731f72918b2f9c405095113c525d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.7` - linux; amd64

```console
$ docker pull chronograf@sha256:50caec28c1075bf254888de8c0e02554d47f8324853228ba530df5ea458341fe
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.6 MB (70594980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:555b44ff48d39db996c3e79be782ad48631ac45f23e8de56e1f4c0c42f48f198`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 06 Dec 2022 01:20:54 GMT
ADD file:1f1efd56601ebc26a041a7b994a380ef68112b91a078e225753bee7b3196d22c in / 
# Tue, 06 Dec 2022 01:20:54 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 01:45:38 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 06 Dec 2022 01:45:38 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 06 Dec 2022 01:45:46 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 06 Dec 2022 01:45:47 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 06 Dec 2022 01:45:47 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 06 Dec 2022 01:45:47 GMT
EXPOSE 8888
# Tue, 06 Dec 2022 01:45:47 GMT
VOLUME [/var/lib/chronograf]
# Tue, 06 Dec 2022 01:45:47 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 06 Dec 2022 01:45:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 06 Dec 2022 01:45:47 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:025c56f98b679f70b7a54241917e56da7b59ab9d2defecc6ebdb0bf2750484bb`  
		Last Modified: Tue, 06 Dec 2022 01:25:12 GMT  
		Size: 31.4 MB (31412852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3270db00f4c8fe7aefb8e1c61c6267f22cbce5933e6b54c04c5c8256455c03cb`  
		Last Modified: Tue, 06 Dec 2022 01:47:00 GMT  
		Size: 4.4 MB (4418903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5f76063734be6be6b8d1c1feac14a72a8762cab0180171afcf5ab51f3e48553`  
		Last Modified: Tue, 06 Dec 2022 01:47:04 GMT  
		Size: 34.7 MB (34738833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05a5f55c28f0f9e61991e25e9a524c75c6e218fb5dc11513699f7eb1b946c845`  
		Last Modified: Tue, 06 Dec 2022 01:46:59 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0098bc12a78ce913e6f2f58e34924ce25ff83b3b2ac1685b460b7fa7cddc4d41`  
		Last Modified: Tue, 06 Dec 2022 01:46:59 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d109bc36fa69995e4fce8412dcd7c1d47c2b1817478385ea33aaf571096fc46`  
		Last Modified: Tue, 06 Dec 2022 01:47:00 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.7` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:9124ff967cebfff08607465ca11b53756898f3e173a6b54b5c876f0ea666f75b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.4 MB (63419483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31787789ddcf1b05e16113bf4dbdaf9ee0ef72e35727d10fd052c1938cf0f774`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 06 Dec 2022 00:58:51 GMT
ADD file:cb354f875d5631d5d4542ab57d0b9b323a261f5c631d5917127504d6eb54d85a in / 
# Tue, 06 Dec 2022 00:58:52 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 10:15:28 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 06 Dec 2022 10:15:28 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 06 Dec 2022 10:15:38 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 06 Dec 2022 10:15:39 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 06 Dec 2022 10:15:39 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 06 Dec 2022 10:15:39 GMT
EXPOSE 8888
# Tue, 06 Dec 2022 10:15:39 GMT
VOLUME [/var/lib/chronograf]
# Tue, 06 Dec 2022 10:15:39 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 06 Dec 2022 10:15:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 06 Dec 2022 10:15:39 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:4f32a98d14d26603bb8e8cf9bda992e24606d2fe00101767049a01d5176929e1`  
		Last Modified: Tue, 06 Dec 2022 01:06:05 GMT  
		Size: 26.6 MB (26576348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3987ac3351dc260c0aa9a72031d77c64ba54b7752f7fc74fb14f85628900eae4`  
		Last Modified: Tue, 06 Dec 2022 10:17:13 GMT  
		Size: 3.7 MB (3720256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9af4281aa2dba6e7be7e454b72fe57d876e94314d64d98fb4713f8e46269c93`  
		Last Modified: Tue, 06 Dec 2022 10:17:18 GMT  
		Size: 33.1 MB (33098492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28af7f9512f6e0e0b2bb21312a0c5fc8688780775fde1f1e06a8992f9f900f83`  
		Last Modified: Tue, 06 Dec 2022 10:17:12 GMT  
		Size: 12.2 KB (12243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47833aae4b2482aac34256423a27e698e5cec8e1b879755a799b4e813047557a`  
		Last Modified: Tue, 06 Dec 2022 10:17:12 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e2bfb3b7643ffe77d492b6dbf41ae3a7db4ac11fc319c50205e6cc7839f4a29`  
		Last Modified: Tue, 06 Dec 2022 10:17:12 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.7` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:6fdd80e612a3d07a0791e1358f1bee6453fe44c5f48c609304d639320cdd0424
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67743435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:247f873dbe7a69eef60a158359920198a0ab1aa690ba51bed90b950188eae237`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 06 Dec 2022 01:40:17 GMT
ADD file:379d6ac56afdb6e02d71fa0faebc13b8a2554fc6ae76c5f5bbdb5b8e475135d6 in / 
# Tue, 06 Dec 2022 01:40:17 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 02:15:04 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 06 Dec 2022 02:15:04 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 06 Dec 2022 02:15:11 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 06 Dec 2022 02:15:11 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 06 Dec 2022 02:15:11 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 06 Dec 2022 02:15:11 GMT
EXPOSE 8888
# Tue, 06 Dec 2022 02:15:11 GMT
VOLUME [/var/lib/chronograf]
# Tue, 06 Dec 2022 02:15:11 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 06 Dec 2022 02:15:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 06 Dec 2022 02:15:11 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:6064e7e5b6afa4dc711228eddfd250aebac271830dc184c400ce640020bc2cb0`  
		Last Modified: Tue, 06 Dec 2022 01:43:56 GMT  
		Size: 30.1 MB (30060320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4858362dd2cfcdbdefe006f4d52a982021fb6edbf6d2385b9d0c8c72259c5429`  
		Last Modified: Tue, 06 Dec 2022 02:15:59 GMT  
		Size: 4.4 MB (4420017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60a160e47181d59d7f53b99aeafe006533ee07203af66bb1dada64f2f46b0cfe`  
		Last Modified: Tue, 06 Dec 2022 02:16:01 GMT  
		Size: 33.2 MB (33238701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3f999fe98c9aa7dbf728a5e0b0fba1d910b7726f4c5f001d11ee659e4331198`  
		Last Modified: Tue, 06 Dec 2022 02:15:58 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f020b6c13512c1b5116a07a15c3bd2ba1c797738b6eba0078525f5500156d083`  
		Last Modified: Tue, 06 Dec 2022 02:15:58 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85cc09f92d5202904a7ace285437410e866285482448698a347cabcea59a9f33`  
		Last Modified: Tue, 06 Dec 2022 02:15:58 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.7-alpine`

```console
$ docker pull chronograf@sha256:9d26ac37c933bc166fe620ded24d156485d317e71f04c4eb2878c565b984849f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.7-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:4b6a35a54e58b60f161d3f2f58aed998b7a0ae7074ca382fda7ec2ada7c2e902
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22693433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6af57497b0aa0aca47fc1ff15bd6c753ed5fa7230450329b86857ba4351cc0a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:07 GMT
ADD file:b9bd10cf83356cb7281baa0fbaca5186cf27491f59eda87abe57f83a5aaf5ec1 in / 
# Tue, 09 Aug 2022 17:20:08 GMT
CMD ["/bin/sh"]
# Thu, 06 Oct 2022 20:15:36 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 06 Oct 2022 20:15:37 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Thu, 06 Oct 2022 20:15:37 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Thu, 06 Oct 2022 20:15:42 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 06 Oct 2022 20:15:42 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 06 Oct 2022 20:15:42 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 06 Oct 2022 20:15:42 GMT
EXPOSE 8888
# Thu, 06 Oct 2022 20:15:43 GMT
VOLUME [/var/lib/chronograf]
# Thu, 06 Oct 2022 20:15:43 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Thu, 06 Oct 2022 20:15:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 06 Oct 2022 20:15:43 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:c7ed990a2339ee598662849de4f56e2241399f5a32340c8c4a7bbd5378a12b5f`  
		Last Modified: Tue, 09 Aug 2022 17:21:06 GMT  
		Size: 2.8 MB (2827489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:133509570f70da73b5369d8311a4269568dbea851313f10ea1b8cb1a2c4e2fe8`  
		Last Modified: Thu, 06 Oct 2022 20:16:43 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ed07ae854e5b9e7d93d0c5eb8bbcfb2d6e5eddeb00720efe7b55766ce5bfbab`  
		Last Modified: Thu, 06 Oct 2022 20:16:41 GMT  
		Size: 284.6 KB (284583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fda7c0dc93cbe974534daa33cf7bf0b94c5803f47fb7f8116f83829cc52a701`  
		Last Modified: Thu, 06 Oct 2022 20:16:44 GMT  
		Size: 19.6 MB (19556809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25bf26481c4767c4543af0f2684354471d9d92c1d3ff7e3a43f714669312ddb5`  
		Last Modified: Thu, 06 Oct 2022 20:16:41 GMT  
		Size: 12.3 KB (12264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93ba3ac2384cc84a067095232897c2f0e30822a778f2bc4d7136e30d336f9a7b`  
		Last Modified: Thu, 06 Oct 2022 20:16:41 GMT  
		Size: 11.9 KB (11896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7cdc8000c1828cc4d9f01bcd32824b8ef240f8130b247937bfb0159e925f412`  
		Last Modified: Thu, 06 Oct 2022 20:16:41 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.7.17`

```console
$ docker pull chronograf@sha256:d1615c1102005b2aaf7674aa038279c08853731f72918b2f9c405095113c525d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.7.17` - linux; amd64

```console
$ docker pull chronograf@sha256:50caec28c1075bf254888de8c0e02554d47f8324853228ba530df5ea458341fe
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.6 MB (70594980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:555b44ff48d39db996c3e79be782ad48631ac45f23e8de56e1f4c0c42f48f198`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 06 Dec 2022 01:20:54 GMT
ADD file:1f1efd56601ebc26a041a7b994a380ef68112b91a078e225753bee7b3196d22c in / 
# Tue, 06 Dec 2022 01:20:54 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 01:45:38 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 06 Dec 2022 01:45:38 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 06 Dec 2022 01:45:46 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 06 Dec 2022 01:45:47 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 06 Dec 2022 01:45:47 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 06 Dec 2022 01:45:47 GMT
EXPOSE 8888
# Tue, 06 Dec 2022 01:45:47 GMT
VOLUME [/var/lib/chronograf]
# Tue, 06 Dec 2022 01:45:47 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 06 Dec 2022 01:45:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 06 Dec 2022 01:45:47 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:025c56f98b679f70b7a54241917e56da7b59ab9d2defecc6ebdb0bf2750484bb`  
		Last Modified: Tue, 06 Dec 2022 01:25:12 GMT  
		Size: 31.4 MB (31412852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3270db00f4c8fe7aefb8e1c61c6267f22cbce5933e6b54c04c5c8256455c03cb`  
		Last Modified: Tue, 06 Dec 2022 01:47:00 GMT  
		Size: 4.4 MB (4418903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5f76063734be6be6b8d1c1feac14a72a8762cab0180171afcf5ab51f3e48553`  
		Last Modified: Tue, 06 Dec 2022 01:47:04 GMT  
		Size: 34.7 MB (34738833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05a5f55c28f0f9e61991e25e9a524c75c6e218fb5dc11513699f7eb1b946c845`  
		Last Modified: Tue, 06 Dec 2022 01:46:59 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0098bc12a78ce913e6f2f58e34924ce25ff83b3b2ac1685b460b7fa7cddc4d41`  
		Last Modified: Tue, 06 Dec 2022 01:46:59 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d109bc36fa69995e4fce8412dcd7c1d47c2b1817478385ea33aaf571096fc46`  
		Last Modified: Tue, 06 Dec 2022 01:47:00 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.7.17` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:9124ff967cebfff08607465ca11b53756898f3e173a6b54b5c876f0ea666f75b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.4 MB (63419483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31787789ddcf1b05e16113bf4dbdaf9ee0ef72e35727d10fd052c1938cf0f774`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 06 Dec 2022 00:58:51 GMT
ADD file:cb354f875d5631d5d4542ab57d0b9b323a261f5c631d5917127504d6eb54d85a in / 
# Tue, 06 Dec 2022 00:58:52 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 10:15:28 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 06 Dec 2022 10:15:28 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 06 Dec 2022 10:15:38 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 06 Dec 2022 10:15:39 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 06 Dec 2022 10:15:39 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 06 Dec 2022 10:15:39 GMT
EXPOSE 8888
# Tue, 06 Dec 2022 10:15:39 GMT
VOLUME [/var/lib/chronograf]
# Tue, 06 Dec 2022 10:15:39 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 06 Dec 2022 10:15:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 06 Dec 2022 10:15:39 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:4f32a98d14d26603bb8e8cf9bda992e24606d2fe00101767049a01d5176929e1`  
		Last Modified: Tue, 06 Dec 2022 01:06:05 GMT  
		Size: 26.6 MB (26576348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3987ac3351dc260c0aa9a72031d77c64ba54b7752f7fc74fb14f85628900eae4`  
		Last Modified: Tue, 06 Dec 2022 10:17:13 GMT  
		Size: 3.7 MB (3720256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9af4281aa2dba6e7be7e454b72fe57d876e94314d64d98fb4713f8e46269c93`  
		Last Modified: Tue, 06 Dec 2022 10:17:18 GMT  
		Size: 33.1 MB (33098492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28af7f9512f6e0e0b2bb21312a0c5fc8688780775fde1f1e06a8992f9f900f83`  
		Last Modified: Tue, 06 Dec 2022 10:17:12 GMT  
		Size: 12.2 KB (12243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47833aae4b2482aac34256423a27e698e5cec8e1b879755a799b4e813047557a`  
		Last Modified: Tue, 06 Dec 2022 10:17:12 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e2bfb3b7643ffe77d492b6dbf41ae3a7db4ac11fc319c50205e6cc7839f4a29`  
		Last Modified: Tue, 06 Dec 2022 10:17:12 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.7.17` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:6fdd80e612a3d07a0791e1358f1bee6453fe44c5f48c609304d639320cdd0424
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67743435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:247f873dbe7a69eef60a158359920198a0ab1aa690ba51bed90b950188eae237`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 06 Dec 2022 01:40:17 GMT
ADD file:379d6ac56afdb6e02d71fa0faebc13b8a2554fc6ae76c5f5bbdb5b8e475135d6 in / 
# Tue, 06 Dec 2022 01:40:17 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 02:15:04 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 06 Dec 2022 02:15:04 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 06 Dec 2022 02:15:11 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 06 Dec 2022 02:15:11 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 06 Dec 2022 02:15:11 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 06 Dec 2022 02:15:11 GMT
EXPOSE 8888
# Tue, 06 Dec 2022 02:15:11 GMT
VOLUME [/var/lib/chronograf]
# Tue, 06 Dec 2022 02:15:11 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 06 Dec 2022 02:15:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 06 Dec 2022 02:15:11 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:6064e7e5b6afa4dc711228eddfd250aebac271830dc184c400ce640020bc2cb0`  
		Last Modified: Tue, 06 Dec 2022 01:43:56 GMT  
		Size: 30.1 MB (30060320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4858362dd2cfcdbdefe006f4d52a982021fb6edbf6d2385b9d0c8c72259c5429`  
		Last Modified: Tue, 06 Dec 2022 02:15:59 GMT  
		Size: 4.4 MB (4420017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60a160e47181d59d7f53b99aeafe006533ee07203af66bb1dada64f2f46b0cfe`  
		Last Modified: Tue, 06 Dec 2022 02:16:01 GMT  
		Size: 33.2 MB (33238701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3f999fe98c9aa7dbf728a5e0b0fba1d910b7726f4c5f001d11ee659e4331198`  
		Last Modified: Tue, 06 Dec 2022 02:15:58 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f020b6c13512c1b5116a07a15c3bd2ba1c797738b6eba0078525f5500156d083`  
		Last Modified: Tue, 06 Dec 2022 02:15:58 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85cc09f92d5202904a7ace285437410e866285482448698a347cabcea59a9f33`  
		Last Modified: Tue, 06 Dec 2022 02:15:58 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.7.17-alpine`

```console
$ docker pull chronograf@sha256:9d26ac37c933bc166fe620ded24d156485d317e71f04c4eb2878c565b984849f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.7.17-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:4b6a35a54e58b60f161d3f2f58aed998b7a0ae7074ca382fda7ec2ada7c2e902
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22693433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6af57497b0aa0aca47fc1ff15bd6c753ed5fa7230450329b86857ba4351cc0a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:07 GMT
ADD file:b9bd10cf83356cb7281baa0fbaca5186cf27491f59eda87abe57f83a5aaf5ec1 in / 
# Tue, 09 Aug 2022 17:20:08 GMT
CMD ["/bin/sh"]
# Thu, 06 Oct 2022 20:15:36 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 06 Oct 2022 20:15:37 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Thu, 06 Oct 2022 20:15:37 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Thu, 06 Oct 2022 20:15:42 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 06 Oct 2022 20:15:42 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 06 Oct 2022 20:15:42 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 06 Oct 2022 20:15:42 GMT
EXPOSE 8888
# Thu, 06 Oct 2022 20:15:43 GMT
VOLUME [/var/lib/chronograf]
# Thu, 06 Oct 2022 20:15:43 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Thu, 06 Oct 2022 20:15:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 06 Oct 2022 20:15:43 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:c7ed990a2339ee598662849de4f56e2241399f5a32340c8c4a7bbd5378a12b5f`  
		Last Modified: Tue, 09 Aug 2022 17:21:06 GMT  
		Size: 2.8 MB (2827489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:133509570f70da73b5369d8311a4269568dbea851313f10ea1b8cb1a2c4e2fe8`  
		Last Modified: Thu, 06 Oct 2022 20:16:43 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ed07ae854e5b9e7d93d0c5eb8bbcfb2d6e5eddeb00720efe7b55766ce5bfbab`  
		Last Modified: Thu, 06 Oct 2022 20:16:41 GMT  
		Size: 284.6 KB (284583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fda7c0dc93cbe974534daa33cf7bf0b94c5803f47fb7f8116f83829cc52a701`  
		Last Modified: Thu, 06 Oct 2022 20:16:44 GMT  
		Size: 19.6 MB (19556809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25bf26481c4767c4543af0f2684354471d9d92c1d3ff7e3a43f714669312ddb5`  
		Last Modified: Thu, 06 Oct 2022 20:16:41 GMT  
		Size: 12.3 KB (12264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93ba3ac2384cc84a067095232897c2f0e30822a778f2bc4d7136e30d336f9a7b`  
		Last Modified: Thu, 06 Oct 2022 20:16:41 GMT  
		Size: 11.9 KB (11896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7cdc8000c1828cc4d9f01bcd32824b8ef240f8130b247937bfb0159e925f412`  
		Last Modified: Thu, 06 Oct 2022 20:16:41 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.8`

```console
$ docker pull chronograf@sha256:b02536e5ee782fb1640f06a1b151ae34141d458436173bc775306045649acc46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.8` - linux; amd64

```console
$ docker pull chronograf@sha256:42813fcf36456a75acdd5bd22a714ca6735a8c9dfe6e0d1518f94dc993a49ee0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 MB (71245636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b7bdbd9ddb2062a7cad251e94c45c0ac311bd4247728b6f8e85e905b5b9abd7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 06 Dec 2022 01:20:54 GMT
ADD file:1f1efd56601ebc26a041a7b994a380ef68112b91a078e225753bee7b3196d22c in / 
# Tue, 06 Dec 2022 01:20:54 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 01:46:01 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 06 Dec 2022 01:46:01 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Tue, 06 Dec 2022 01:46:07 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 06 Dec 2022 01:46:08 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 06 Dec 2022 01:46:08 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 06 Dec 2022 01:46:08 GMT
EXPOSE 8888
# Tue, 06 Dec 2022 01:46:08 GMT
VOLUME [/var/lib/chronograf]
# Tue, 06 Dec 2022 01:46:08 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 06 Dec 2022 01:46:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 06 Dec 2022 01:46:08 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:025c56f98b679f70b7a54241917e56da7b59ab9d2defecc6ebdb0bf2750484bb`  
		Last Modified: Tue, 06 Dec 2022 01:25:12 GMT  
		Size: 31.4 MB (31412852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89ff5a347561490589cdaddbb9c1d1fd79814edac3ddf8bc928b34dddfd7c5bb`  
		Last Modified: Tue, 06 Dec 2022 01:47:14 GMT  
		Size: 5.2 MB (5228712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f864b46ac289a1acbaeba736aafac666d7d5473dbcc6d288a984f59ec490e863`  
		Last Modified: Tue, 06 Dec 2022 01:47:18 GMT  
		Size: 34.6 MB (34579677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:917c0be3a7081282ca8862edeb8c854e138c0b8f8e8b170c7a9a4d7053ea402d`  
		Last Modified: Tue, 06 Dec 2022 01:47:14 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7deedcb62df61cd0669793329230afc1e55efc26aa72e1971fd639f0913cdc3e`  
		Last Modified: Tue, 06 Dec 2022 01:47:13 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfcb490407d09f5f256c76bd638ff4b48edf03f361377c5162b056211efdb298`  
		Last Modified: Tue, 06 Dec 2022 01:47:13 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.8` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:fa40febdfbb338e756c0952bd5f306841abf43c2abb912df967be41670fc5ca0
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.8 MB (63847024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0557cea89412ab590fc3cb24dcb19e140b9240de2851330f1a3bafa587ddf7ca`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 06 Dec 2022 00:58:51 GMT
ADD file:cb354f875d5631d5d4542ab57d0b9b323a261f5c631d5917127504d6eb54d85a in / 
# Tue, 06 Dec 2022 00:58:52 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 10:15:54 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 06 Dec 2022 10:15:54 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Tue, 06 Dec 2022 10:16:02 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 06 Dec 2022 10:16:02 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 06 Dec 2022 10:16:02 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 06 Dec 2022 10:16:02 GMT
EXPOSE 8888
# Tue, 06 Dec 2022 10:16:02 GMT
VOLUME [/var/lib/chronograf]
# Tue, 06 Dec 2022 10:16:03 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 06 Dec 2022 10:16:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 06 Dec 2022 10:16:03 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:4f32a98d14d26603bb8e8cf9bda992e24606d2fe00101767049a01d5176929e1`  
		Last Modified: Tue, 06 Dec 2022 01:06:05 GMT  
		Size: 26.6 MB (26576348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13331aa96eaee2e9e3ef374955946cbe0508467ec66e9c44cb3122bc85393b6e`  
		Last Modified: Tue, 06 Dec 2022 10:17:29 GMT  
		Size: 4.5 MB (4495026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f307337f5b8fc975010fd51dcf917f9ff9c3815ba4d2d9d0ba175c37f6b79db1`  
		Last Modified: Tue, 06 Dec 2022 10:17:33 GMT  
		Size: 32.8 MB (32751262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b028aadc82f9b298c459f5c54103f5007a2ff7e951caa282277492874507e7b4`  
		Last Modified: Tue, 06 Dec 2022 10:17:28 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb871e02c6caf5893930d845ea36dc5baa4a2d497ae17cf90ac2d5916b671a95`  
		Last Modified: Tue, 06 Dec 2022 10:17:28 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a4224227a24e8a4bb7fe3094517b2fd0db8a0e783a0bb2d26aa8585afb0f0e9`  
		Last Modified: Tue, 06 Dec 2022 10:17:28 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.8` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:44a74094f7dae0031e6b2328d1cbb363d729883baf4bc18b7d5447c1b44566b7
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.9 MB (67940744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8603e8f6b0029318cbe0a8c6d3a66c41bf0fc09b2695e3fa08e7b5e75f1d450e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 06 Dec 2022 01:40:17 GMT
ADD file:379d6ac56afdb6e02d71fa0faebc13b8a2554fc6ae76c5f5bbdb5b8e475135d6 in / 
# Tue, 06 Dec 2022 01:40:17 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 02:15:19 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 06 Dec 2022 02:15:19 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Tue, 06 Dec 2022 02:15:25 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 06 Dec 2022 02:15:25 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 06 Dec 2022 02:15:25 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 06 Dec 2022 02:15:25 GMT
EXPOSE 8888
# Tue, 06 Dec 2022 02:15:25 GMT
VOLUME [/var/lib/chronograf]
# Tue, 06 Dec 2022 02:15:25 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 06 Dec 2022 02:15:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 06 Dec 2022 02:15:25 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:6064e7e5b6afa4dc711228eddfd250aebac271830dc184c400ce640020bc2cb0`  
		Last Modified: Tue, 06 Dec 2022 01:43:56 GMT  
		Size: 30.1 MB (30060320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:010bcfd47e4f0331c64dfb2af5573bf99a4b88b4d972387850c61ff6ef0d11a9`  
		Last Modified: Tue, 06 Dec 2022 02:16:10 GMT  
		Size: 5.2 MB (5211566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8e6ced064fb49b2ed67884e80e75c35ef0f54c12b2a2e64e1f38b8870d57873`  
		Last Modified: Tue, 06 Dec 2022 02:16:13 GMT  
		Size: 32.6 MB (32644461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b847223e4fd1c399cf3727ce777de262527aeafcaed1eceb458b83067c43eff7`  
		Last Modified: Tue, 06 Dec 2022 02:16:10 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:459ddd3a24b7d124f90be5f6d5d71c5a84eef0a4576f2a5aba099194686f3dae`  
		Last Modified: Tue, 06 Dec 2022 02:16:10 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99cdbcafbac9348b3197828f3370a14944a01c59d360ff7a6e0e54f2032d2a4c`  
		Last Modified: Tue, 06 Dec 2022 02:16:10 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.8-alpine`

```console
$ docker pull chronograf@sha256:a430e7dd4d3f94b4b711a4000e847f59465fe1e3d7e9997d59800fc7a5da10cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.8-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:2d4ad97697ce5c225b6e38515e3ea3b543e28f102c45917f4239ecca0ebadda5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.3 MB (22340855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:610057aef173c70f1c0a6ce869e16af679c0a1e65c669ac3b8eaba8d112a527a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:07 GMT
ADD file:b9bd10cf83356cb7281baa0fbaca5186cf27491f59eda87abe57f83a5aaf5ec1 in / 
# Tue, 09 Aug 2022 17:20:08 GMT
CMD ["/bin/sh"]
# Thu, 06 Oct 2022 20:15:36 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 06 Oct 2022 20:15:37 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Thu, 06 Oct 2022 20:15:47 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Thu, 06 Oct 2022 20:15:52 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 06 Oct 2022 20:15:53 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 06 Oct 2022 20:15:53 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 06 Oct 2022 20:15:53 GMT
EXPOSE 8888
# Thu, 06 Oct 2022 20:15:53 GMT
VOLUME [/var/lib/chronograf]
# Thu, 06 Oct 2022 20:15:53 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Thu, 06 Oct 2022 20:15:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 06 Oct 2022 20:15:53 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:c7ed990a2339ee598662849de4f56e2241399f5a32340c8c4a7bbd5378a12b5f`  
		Last Modified: Tue, 09 Aug 2022 17:21:06 GMT  
		Size: 2.8 MB (2827489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:133509570f70da73b5369d8311a4269568dbea851313f10ea1b8cb1a2c4e2fe8`  
		Last Modified: Thu, 06 Oct 2022 20:16:43 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ed07ae854e5b9e7d93d0c5eb8bbcfb2d6e5eddeb00720efe7b55766ce5bfbab`  
		Last Modified: Thu, 06 Oct 2022 20:16:41 GMT  
		Size: 284.6 KB (284583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d59d8c24f659459b77a60f9b6c97614166735dca2ae5a9254e7733b3382432fa`  
		Last Modified: Thu, 06 Oct 2022 20:16:58 GMT  
		Size: 19.2 MB (19204225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eaef5e9f5e1eba8a7b3a73db5c4d6efe6ba62e72d3c1a86384494b5fc0b6bc3`  
		Last Modified: Thu, 06 Oct 2022 20:16:55 GMT  
		Size: 12.3 KB (12267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dd6d1543ef965519e2d993c8db13568b477c3c72bae7b6023a2cde9350376d1`  
		Last Modified: Thu, 06 Oct 2022 20:16:55 GMT  
		Size: 11.9 KB (11899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68f5df71d2bc59720fcde07d37a3c2f558595676b2519551f3efda4830e28abc`  
		Last Modified: Thu, 06 Oct 2022 20:16:55 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.8.10`

```console
$ docker pull chronograf@sha256:b02536e5ee782fb1640f06a1b151ae34141d458436173bc775306045649acc46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.8.10` - linux; amd64

```console
$ docker pull chronograf@sha256:42813fcf36456a75acdd5bd22a714ca6735a8c9dfe6e0d1518f94dc993a49ee0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 MB (71245636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b7bdbd9ddb2062a7cad251e94c45c0ac311bd4247728b6f8e85e905b5b9abd7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 06 Dec 2022 01:20:54 GMT
ADD file:1f1efd56601ebc26a041a7b994a380ef68112b91a078e225753bee7b3196d22c in / 
# Tue, 06 Dec 2022 01:20:54 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 01:46:01 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 06 Dec 2022 01:46:01 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Tue, 06 Dec 2022 01:46:07 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 06 Dec 2022 01:46:08 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 06 Dec 2022 01:46:08 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 06 Dec 2022 01:46:08 GMT
EXPOSE 8888
# Tue, 06 Dec 2022 01:46:08 GMT
VOLUME [/var/lib/chronograf]
# Tue, 06 Dec 2022 01:46:08 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 06 Dec 2022 01:46:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 06 Dec 2022 01:46:08 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:025c56f98b679f70b7a54241917e56da7b59ab9d2defecc6ebdb0bf2750484bb`  
		Last Modified: Tue, 06 Dec 2022 01:25:12 GMT  
		Size: 31.4 MB (31412852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89ff5a347561490589cdaddbb9c1d1fd79814edac3ddf8bc928b34dddfd7c5bb`  
		Last Modified: Tue, 06 Dec 2022 01:47:14 GMT  
		Size: 5.2 MB (5228712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f864b46ac289a1acbaeba736aafac666d7d5473dbcc6d288a984f59ec490e863`  
		Last Modified: Tue, 06 Dec 2022 01:47:18 GMT  
		Size: 34.6 MB (34579677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:917c0be3a7081282ca8862edeb8c854e138c0b8f8e8b170c7a9a4d7053ea402d`  
		Last Modified: Tue, 06 Dec 2022 01:47:14 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7deedcb62df61cd0669793329230afc1e55efc26aa72e1971fd639f0913cdc3e`  
		Last Modified: Tue, 06 Dec 2022 01:47:13 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfcb490407d09f5f256c76bd638ff4b48edf03f361377c5162b056211efdb298`  
		Last Modified: Tue, 06 Dec 2022 01:47:13 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.8.10` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:fa40febdfbb338e756c0952bd5f306841abf43c2abb912df967be41670fc5ca0
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.8 MB (63847024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0557cea89412ab590fc3cb24dcb19e140b9240de2851330f1a3bafa587ddf7ca`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 06 Dec 2022 00:58:51 GMT
ADD file:cb354f875d5631d5d4542ab57d0b9b323a261f5c631d5917127504d6eb54d85a in / 
# Tue, 06 Dec 2022 00:58:52 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 10:15:54 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 06 Dec 2022 10:15:54 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Tue, 06 Dec 2022 10:16:02 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 06 Dec 2022 10:16:02 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 06 Dec 2022 10:16:02 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 06 Dec 2022 10:16:02 GMT
EXPOSE 8888
# Tue, 06 Dec 2022 10:16:02 GMT
VOLUME [/var/lib/chronograf]
# Tue, 06 Dec 2022 10:16:03 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 06 Dec 2022 10:16:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 06 Dec 2022 10:16:03 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:4f32a98d14d26603bb8e8cf9bda992e24606d2fe00101767049a01d5176929e1`  
		Last Modified: Tue, 06 Dec 2022 01:06:05 GMT  
		Size: 26.6 MB (26576348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13331aa96eaee2e9e3ef374955946cbe0508467ec66e9c44cb3122bc85393b6e`  
		Last Modified: Tue, 06 Dec 2022 10:17:29 GMT  
		Size: 4.5 MB (4495026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f307337f5b8fc975010fd51dcf917f9ff9c3815ba4d2d9d0ba175c37f6b79db1`  
		Last Modified: Tue, 06 Dec 2022 10:17:33 GMT  
		Size: 32.8 MB (32751262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b028aadc82f9b298c459f5c54103f5007a2ff7e951caa282277492874507e7b4`  
		Last Modified: Tue, 06 Dec 2022 10:17:28 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb871e02c6caf5893930d845ea36dc5baa4a2d497ae17cf90ac2d5916b671a95`  
		Last Modified: Tue, 06 Dec 2022 10:17:28 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a4224227a24e8a4bb7fe3094517b2fd0db8a0e783a0bb2d26aa8585afb0f0e9`  
		Last Modified: Tue, 06 Dec 2022 10:17:28 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.8.10` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:44a74094f7dae0031e6b2328d1cbb363d729883baf4bc18b7d5447c1b44566b7
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.9 MB (67940744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8603e8f6b0029318cbe0a8c6d3a66c41bf0fc09b2695e3fa08e7b5e75f1d450e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 06 Dec 2022 01:40:17 GMT
ADD file:379d6ac56afdb6e02d71fa0faebc13b8a2554fc6ae76c5f5bbdb5b8e475135d6 in / 
# Tue, 06 Dec 2022 01:40:17 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 02:15:19 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 06 Dec 2022 02:15:19 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Tue, 06 Dec 2022 02:15:25 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 06 Dec 2022 02:15:25 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 06 Dec 2022 02:15:25 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 06 Dec 2022 02:15:25 GMT
EXPOSE 8888
# Tue, 06 Dec 2022 02:15:25 GMT
VOLUME [/var/lib/chronograf]
# Tue, 06 Dec 2022 02:15:25 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 06 Dec 2022 02:15:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 06 Dec 2022 02:15:25 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:6064e7e5b6afa4dc711228eddfd250aebac271830dc184c400ce640020bc2cb0`  
		Last Modified: Tue, 06 Dec 2022 01:43:56 GMT  
		Size: 30.1 MB (30060320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:010bcfd47e4f0331c64dfb2af5573bf99a4b88b4d972387850c61ff6ef0d11a9`  
		Last Modified: Tue, 06 Dec 2022 02:16:10 GMT  
		Size: 5.2 MB (5211566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8e6ced064fb49b2ed67884e80e75c35ef0f54c12b2a2e64e1f38b8870d57873`  
		Last Modified: Tue, 06 Dec 2022 02:16:13 GMT  
		Size: 32.6 MB (32644461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b847223e4fd1c399cf3727ce777de262527aeafcaed1eceb458b83067c43eff7`  
		Last Modified: Tue, 06 Dec 2022 02:16:10 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:459ddd3a24b7d124f90be5f6d5d71c5a84eef0a4576f2a5aba099194686f3dae`  
		Last Modified: Tue, 06 Dec 2022 02:16:10 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99cdbcafbac9348b3197828f3370a14944a01c59d360ff7a6e0e54f2032d2a4c`  
		Last Modified: Tue, 06 Dec 2022 02:16:10 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.8.10-alpine`

```console
$ docker pull chronograf@sha256:a430e7dd4d3f94b4b711a4000e847f59465fe1e3d7e9997d59800fc7a5da10cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.8.10-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:2d4ad97697ce5c225b6e38515e3ea3b543e28f102c45917f4239ecca0ebadda5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.3 MB (22340855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:610057aef173c70f1c0a6ce869e16af679c0a1e65c669ac3b8eaba8d112a527a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:07 GMT
ADD file:b9bd10cf83356cb7281baa0fbaca5186cf27491f59eda87abe57f83a5aaf5ec1 in / 
# Tue, 09 Aug 2022 17:20:08 GMT
CMD ["/bin/sh"]
# Thu, 06 Oct 2022 20:15:36 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 06 Oct 2022 20:15:37 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Thu, 06 Oct 2022 20:15:47 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Thu, 06 Oct 2022 20:15:52 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 06 Oct 2022 20:15:53 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 06 Oct 2022 20:15:53 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 06 Oct 2022 20:15:53 GMT
EXPOSE 8888
# Thu, 06 Oct 2022 20:15:53 GMT
VOLUME [/var/lib/chronograf]
# Thu, 06 Oct 2022 20:15:53 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Thu, 06 Oct 2022 20:15:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 06 Oct 2022 20:15:53 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:c7ed990a2339ee598662849de4f56e2241399f5a32340c8c4a7bbd5378a12b5f`  
		Last Modified: Tue, 09 Aug 2022 17:21:06 GMT  
		Size: 2.8 MB (2827489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:133509570f70da73b5369d8311a4269568dbea851313f10ea1b8cb1a2c4e2fe8`  
		Last Modified: Thu, 06 Oct 2022 20:16:43 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ed07ae854e5b9e7d93d0c5eb8bbcfb2d6e5eddeb00720efe7b55766ce5bfbab`  
		Last Modified: Thu, 06 Oct 2022 20:16:41 GMT  
		Size: 284.6 KB (284583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d59d8c24f659459b77a60f9b6c97614166735dca2ae5a9254e7733b3382432fa`  
		Last Modified: Thu, 06 Oct 2022 20:16:58 GMT  
		Size: 19.2 MB (19204225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eaef5e9f5e1eba8a7b3a73db5c4d6efe6ba62e72d3c1a86384494b5fc0b6bc3`  
		Last Modified: Thu, 06 Oct 2022 20:16:55 GMT  
		Size: 12.3 KB (12267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dd6d1543ef965519e2d993c8db13568b477c3c72bae7b6023a2cde9350376d1`  
		Last Modified: Thu, 06 Oct 2022 20:16:55 GMT  
		Size: 11.9 KB (11899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68f5df71d2bc59720fcde07d37a3c2f558595676b2519551f3efda4830e28abc`  
		Last Modified: Thu, 06 Oct 2022 20:16:55 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.9`

```console
$ docker pull chronograf@sha256:c3891d39dbc4cd376673d033e5856ec27ed18564892b47b5c8ed2d46c93ab105
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.9` - linux; amd64

```console
$ docker pull chronograf@sha256:77dcda159b24234472f487a0d9703c21626b21cec71dcff9c28ac1f3e62a7722
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.9 MB (71893158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ff236bd7d27544765b1d01128fe139d958ae6b1fdadf0d4c33cf30d61aea6ae`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 06 Dec 2022 01:20:54 GMT
ADD file:1f1efd56601ebc26a041a7b994a380ef68112b91a078e225753bee7b3196d22c in / 
# Tue, 06 Dec 2022 01:20:54 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 01:46:01 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 06 Dec 2022 01:46:15 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Tue, 06 Dec 2022 01:46:21 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 06 Dec 2022 01:46:22 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 06 Dec 2022 01:46:22 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 06 Dec 2022 01:46:22 GMT
EXPOSE 8888
# Tue, 06 Dec 2022 01:46:22 GMT
VOLUME [/var/lib/chronograf]
# Tue, 06 Dec 2022 01:46:22 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 06 Dec 2022 01:46:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 06 Dec 2022 01:46:22 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:025c56f98b679f70b7a54241917e56da7b59ab9d2defecc6ebdb0bf2750484bb`  
		Last Modified: Tue, 06 Dec 2022 01:25:12 GMT  
		Size: 31.4 MB (31412852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89ff5a347561490589cdaddbb9c1d1fd79814edac3ddf8bc928b34dddfd7c5bb`  
		Last Modified: Tue, 06 Dec 2022 01:47:14 GMT  
		Size: 5.2 MB (5228712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89241c75c50f880ed90c2dbd0beac90c0bc6581697b0fda169f45d406a9cd4eb`  
		Last Modified: Tue, 06 Dec 2022 01:47:32 GMT  
		Size: 35.2 MB (35227198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3a36af006d058a48c486d22562ac07cd4bea2b0893f47ebb8df5b824971298c`  
		Last Modified: Tue, 06 Dec 2022 01:47:27 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36f9240df4d8e765ae2758e0121c46c97d85f54518d6a362bc6e738b0b4589a4`  
		Last Modified: Tue, 06 Dec 2022 01:47:27 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:578f1dc253b92877cc2fa83f6915f2da40e1ce656c24bcdecb14a601f8b968ae`  
		Last Modified: Tue, 06 Dec 2022 01:47:27 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.9` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:209e08e0a6cc986af18e5339a3c73e306c205a3d0d58daaf579209e71168d48d
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.6 MB (64623102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac5a6f780c2825e02c18a0f21062eab9e6f2197aaed356fe5501a92f0e8f4c2d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 06 Dec 2022 00:58:51 GMT
ADD file:cb354f875d5631d5d4542ab57d0b9b323a261f5c631d5917127504d6eb54d85a in / 
# Tue, 06 Dec 2022 00:58:52 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 10:15:54 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 06 Dec 2022 10:16:09 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Tue, 06 Dec 2022 10:16:21 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 06 Dec 2022 10:16:21 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 06 Dec 2022 10:16:21 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 06 Dec 2022 10:16:21 GMT
EXPOSE 8888
# Tue, 06 Dec 2022 10:16:21 GMT
VOLUME [/var/lib/chronograf]
# Tue, 06 Dec 2022 10:16:21 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 06 Dec 2022 10:16:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 06 Dec 2022 10:16:22 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:4f32a98d14d26603bb8e8cf9bda992e24606d2fe00101767049a01d5176929e1`  
		Last Modified: Tue, 06 Dec 2022 01:06:05 GMT  
		Size: 26.6 MB (26576348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13331aa96eaee2e9e3ef374955946cbe0508467ec66e9c44cb3122bc85393b6e`  
		Last Modified: Tue, 06 Dec 2022 10:17:29 GMT  
		Size: 4.5 MB (4495026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab72917b02d77d51a7c49c67c107d7e6183be276c54897df8df47e576eb1b919`  
		Last Modified: Tue, 06 Dec 2022 10:17:49 GMT  
		Size: 33.5 MB (33527341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0159240fe941ef8ea347d4fb25396ac8f4d2d266e557d7c959cee9b6644f2c1e`  
		Last Modified: Tue, 06 Dec 2022 10:17:43 GMT  
		Size: 12.2 KB (12243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ebe06fcfe03778ec0c45133332153ba0e48e81d3f9c5659624f2c64d3167076`  
		Last Modified: Tue, 06 Dec 2022 10:17:43 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f06ded5f9fe194e222f728c3e7398721f3a8e70529c1afbe82c5e116f342fa7`  
		Last Modified: Tue, 06 Dec 2022 10:17:43 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.9` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:072695c9d52b9fa71600dbb90ae79c40abd8fbcdcb89173b134918eae47957c9
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.7 MB (68692372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7005d665f49943cf6c63dd57c490f620d56e0141833ee2b68b96d6273201158c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 06 Dec 2022 01:40:17 GMT
ADD file:379d6ac56afdb6e02d71fa0faebc13b8a2554fc6ae76c5f5bbdb5b8e475135d6 in / 
# Tue, 06 Dec 2022 01:40:17 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 02:15:19 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 06 Dec 2022 02:15:28 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Tue, 06 Dec 2022 02:15:33 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 06 Dec 2022 02:15:33 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 06 Dec 2022 02:15:33 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 06 Dec 2022 02:15:33 GMT
EXPOSE 8888
# Tue, 06 Dec 2022 02:15:33 GMT
VOLUME [/var/lib/chronograf]
# Tue, 06 Dec 2022 02:15:33 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 06 Dec 2022 02:15:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 06 Dec 2022 02:15:33 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:6064e7e5b6afa4dc711228eddfd250aebac271830dc184c400ce640020bc2cb0`  
		Last Modified: Tue, 06 Dec 2022 01:43:56 GMT  
		Size: 30.1 MB (30060320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:010bcfd47e4f0331c64dfb2af5573bf99a4b88b4d972387850c61ff6ef0d11a9`  
		Last Modified: Tue, 06 Dec 2022 02:16:10 GMT  
		Size: 5.2 MB (5211566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:078cb746615a87f5ba39054d911b35aef942b230844e37067fe759a262e2eb0d`  
		Last Modified: Tue, 06 Dec 2022 02:16:25 GMT  
		Size: 33.4 MB (33396086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37a5e9999a32f15a0865821f11ee141ed1e249e16c17ce3edad72cda83a45c37`  
		Last Modified: Tue, 06 Dec 2022 02:16:21 GMT  
		Size: 12.3 KB (12251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77d1b66099a255749d54616ffbe7321452a6406e79d59c87d7cb0a59f835d068`  
		Last Modified: Tue, 06 Dec 2022 02:16:21 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7622c43f2c36b1dfac004cfe4f8d8427da230a2aafbaf025a7bd8066d010eee`  
		Last Modified: Tue, 06 Dec 2022 02:16:21 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.9-alpine`

```console
$ docker pull chronograf@sha256:22f17928ed0e686715e2b906f6e647ccc55c1e216dff1a563b76264f87f5392d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.9-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:d0b7ec6f54d4499c9a81a50fd7148b478b660fc8ded25155fb3a13baa4bf6239
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.8 MB (22808795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a3777d2e14c286895c264ba3580085a048c076a33a63ce90569c4ea6d7b2f98`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:07 GMT
ADD file:b9bd10cf83356cb7281baa0fbaca5186cf27491f59eda87abe57f83a5aaf5ec1 in / 
# Tue, 09 Aug 2022 17:20:08 GMT
CMD ["/bin/sh"]
# Thu, 06 Oct 2022 20:15:36 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 06 Oct 2022 20:15:37 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Thu, 06 Oct 2022 20:15:57 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Thu, 06 Oct 2022 20:16:03 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 06 Oct 2022 20:16:03 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 06 Oct 2022 20:16:03 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 06 Oct 2022 20:16:04 GMT
EXPOSE 8888
# Thu, 06 Oct 2022 20:16:04 GMT
VOLUME [/var/lib/chronograf]
# Thu, 06 Oct 2022 20:16:04 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Thu, 06 Oct 2022 20:16:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 06 Oct 2022 20:16:04 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:c7ed990a2339ee598662849de4f56e2241399f5a32340c8c4a7bbd5378a12b5f`  
		Last Modified: Tue, 09 Aug 2022 17:21:06 GMT  
		Size: 2.8 MB (2827489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:133509570f70da73b5369d8311a4269568dbea851313f10ea1b8cb1a2c4e2fe8`  
		Last Modified: Thu, 06 Oct 2022 20:16:43 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ed07ae854e5b9e7d93d0c5eb8bbcfb2d6e5eddeb00720efe7b55766ce5bfbab`  
		Last Modified: Thu, 06 Oct 2022 20:16:41 GMT  
		Size: 284.6 KB (284583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19dfd580c937a95d72fb2af50a28c6814b4886872b951143883b0ffde4712c5f`  
		Last Modified: Thu, 06 Oct 2022 20:17:11 GMT  
		Size: 19.7 MB (19672168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9e61e6634ea5e9aa1e5e15257ac4db9252543ec14ac7bd8989d98dca8f7b54f`  
		Last Modified: Thu, 06 Oct 2022 20:17:08 GMT  
		Size: 12.3 KB (12265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f00f1a43c212b770a42e5c7bc1563a4df034c07a36e2d6f937d26b1d907303e`  
		Last Modified: Thu, 06 Oct 2022 20:17:08 GMT  
		Size: 11.9 KB (11898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4bb73bba03a148277f19627c4b0811fb06e034afa29b8939eb47b20577a3537`  
		Last Modified: Thu, 06 Oct 2022 20:17:08 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.9.4`

```console
$ docker pull chronograf@sha256:c3891d39dbc4cd376673d033e5856ec27ed18564892b47b5c8ed2d46c93ab105
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.9.4` - linux; amd64

```console
$ docker pull chronograf@sha256:77dcda159b24234472f487a0d9703c21626b21cec71dcff9c28ac1f3e62a7722
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.9 MB (71893158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ff236bd7d27544765b1d01128fe139d958ae6b1fdadf0d4c33cf30d61aea6ae`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 06 Dec 2022 01:20:54 GMT
ADD file:1f1efd56601ebc26a041a7b994a380ef68112b91a078e225753bee7b3196d22c in / 
# Tue, 06 Dec 2022 01:20:54 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 01:46:01 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 06 Dec 2022 01:46:15 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Tue, 06 Dec 2022 01:46:21 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 06 Dec 2022 01:46:22 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 06 Dec 2022 01:46:22 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 06 Dec 2022 01:46:22 GMT
EXPOSE 8888
# Tue, 06 Dec 2022 01:46:22 GMT
VOLUME [/var/lib/chronograf]
# Tue, 06 Dec 2022 01:46:22 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 06 Dec 2022 01:46:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 06 Dec 2022 01:46:22 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:025c56f98b679f70b7a54241917e56da7b59ab9d2defecc6ebdb0bf2750484bb`  
		Last Modified: Tue, 06 Dec 2022 01:25:12 GMT  
		Size: 31.4 MB (31412852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89ff5a347561490589cdaddbb9c1d1fd79814edac3ddf8bc928b34dddfd7c5bb`  
		Last Modified: Tue, 06 Dec 2022 01:47:14 GMT  
		Size: 5.2 MB (5228712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89241c75c50f880ed90c2dbd0beac90c0bc6581697b0fda169f45d406a9cd4eb`  
		Last Modified: Tue, 06 Dec 2022 01:47:32 GMT  
		Size: 35.2 MB (35227198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3a36af006d058a48c486d22562ac07cd4bea2b0893f47ebb8df5b824971298c`  
		Last Modified: Tue, 06 Dec 2022 01:47:27 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36f9240df4d8e765ae2758e0121c46c97d85f54518d6a362bc6e738b0b4589a4`  
		Last Modified: Tue, 06 Dec 2022 01:47:27 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:578f1dc253b92877cc2fa83f6915f2da40e1ce656c24bcdecb14a601f8b968ae`  
		Last Modified: Tue, 06 Dec 2022 01:47:27 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.9.4` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:209e08e0a6cc986af18e5339a3c73e306c205a3d0d58daaf579209e71168d48d
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.6 MB (64623102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac5a6f780c2825e02c18a0f21062eab9e6f2197aaed356fe5501a92f0e8f4c2d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 06 Dec 2022 00:58:51 GMT
ADD file:cb354f875d5631d5d4542ab57d0b9b323a261f5c631d5917127504d6eb54d85a in / 
# Tue, 06 Dec 2022 00:58:52 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 10:15:54 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 06 Dec 2022 10:16:09 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Tue, 06 Dec 2022 10:16:21 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 06 Dec 2022 10:16:21 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 06 Dec 2022 10:16:21 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 06 Dec 2022 10:16:21 GMT
EXPOSE 8888
# Tue, 06 Dec 2022 10:16:21 GMT
VOLUME [/var/lib/chronograf]
# Tue, 06 Dec 2022 10:16:21 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 06 Dec 2022 10:16:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 06 Dec 2022 10:16:22 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:4f32a98d14d26603bb8e8cf9bda992e24606d2fe00101767049a01d5176929e1`  
		Last Modified: Tue, 06 Dec 2022 01:06:05 GMT  
		Size: 26.6 MB (26576348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13331aa96eaee2e9e3ef374955946cbe0508467ec66e9c44cb3122bc85393b6e`  
		Last Modified: Tue, 06 Dec 2022 10:17:29 GMT  
		Size: 4.5 MB (4495026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab72917b02d77d51a7c49c67c107d7e6183be276c54897df8df47e576eb1b919`  
		Last Modified: Tue, 06 Dec 2022 10:17:49 GMT  
		Size: 33.5 MB (33527341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0159240fe941ef8ea347d4fb25396ac8f4d2d266e557d7c959cee9b6644f2c1e`  
		Last Modified: Tue, 06 Dec 2022 10:17:43 GMT  
		Size: 12.2 KB (12243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ebe06fcfe03778ec0c45133332153ba0e48e81d3f9c5659624f2c64d3167076`  
		Last Modified: Tue, 06 Dec 2022 10:17:43 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f06ded5f9fe194e222f728c3e7398721f3a8e70529c1afbe82c5e116f342fa7`  
		Last Modified: Tue, 06 Dec 2022 10:17:43 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.9.4` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:072695c9d52b9fa71600dbb90ae79c40abd8fbcdcb89173b134918eae47957c9
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.7 MB (68692372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7005d665f49943cf6c63dd57c490f620d56e0141833ee2b68b96d6273201158c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 06 Dec 2022 01:40:17 GMT
ADD file:379d6ac56afdb6e02d71fa0faebc13b8a2554fc6ae76c5f5bbdb5b8e475135d6 in / 
# Tue, 06 Dec 2022 01:40:17 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 02:15:19 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 06 Dec 2022 02:15:28 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Tue, 06 Dec 2022 02:15:33 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 06 Dec 2022 02:15:33 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 06 Dec 2022 02:15:33 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 06 Dec 2022 02:15:33 GMT
EXPOSE 8888
# Tue, 06 Dec 2022 02:15:33 GMT
VOLUME [/var/lib/chronograf]
# Tue, 06 Dec 2022 02:15:33 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 06 Dec 2022 02:15:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 06 Dec 2022 02:15:33 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:6064e7e5b6afa4dc711228eddfd250aebac271830dc184c400ce640020bc2cb0`  
		Last Modified: Tue, 06 Dec 2022 01:43:56 GMT  
		Size: 30.1 MB (30060320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:010bcfd47e4f0331c64dfb2af5573bf99a4b88b4d972387850c61ff6ef0d11a9`  
		Last Modified: Tue, 06 Dec 2022 02:16:10 GMT  
		Size: 5.2 MB (5211566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:078cb746615a87f5ba39054d911b35aef942b230844e37067fe759a262e2eb0d`  
		Last Modified: Tue, 06 Dec 2022 02:16:25 GMT  
		Size: 33.4 MB (33396086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37a5e9999a32f15a0865821f11ee141ed1e249e16c17ce3edad72cda83a45c37`  
		Last Modified: Tue, 06 Dec 2022 02:16:21 GMT  
		Size: 12.3 KB (12251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77d1b66099a255749d54616ffbe7321452a6406e79d59c87d7cb0a59f835d068`  
		Last Modified: Tue, 06 Dec 2022 02:16:21 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7622c43f2c36b1dfac004cfe4f8d8427da230a2aafbaf025a7bd8066d010eee`  
		Last Modified: Tue, 06 Dec 2022 02:16:21 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.9.4-alpine`

```console
$ docker pull chronograf@sha256:22f17928ed0e686715e2b906f6e647ccc55c1e216dff1a563b76264f87f5392d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.9.4-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:d0b7ec6f54d4499c9a81a50fd7148b478b660fc8ded25155fb3a13baa4bf6239
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.8 MB (22808795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a3777d2e14c286895c264ba3580085a048c076a33a63ce90569c4ea6d7b2f98`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:07 GMT
ADD file:b9bd10cf83356cb7281baa0fbaca5186cf27491f59eda87abe57f83a5aaf5ec1 in / 
# Tue, 09 Aug 2022 17:20:08 GMT
CMD ["/bin/sh"]
# Thu, 06 Oct 2022 20:15:36 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 06 Oct 2022 20:15:37 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Thu, 06 Oct 2022 20:15:57 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Thu, 06 Oct 2022 20:16:03 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 06 Oct 2022 20:16:03 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 06 Oct 2022 20:16:03 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 06 Oct 2022 20:16:04 GMT
EXPOSE 8888
# Thu, 06 Oct 2022 20:16:04 GMT
VOLUME [/var/lib/chronograf]
# Thu, 06 Oct 2022 20:16:04 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Thu, 06 Oct 2022 20:16:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 06 Oct 2022 20:16:04 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:c7ed990a2339ee598662849de4f56e2241399f5a32340c8c4a7bbd5378a12b5f`  
		Last Modified: Tue, 09 Aug 2022 17:21:06 GMT  
		Size: 2.8 MB (2827489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:133509570f70da73b5369d8311a4269568dbea851313f10ea1b8cb1a2c4e2fe8`  
		Last Modified: Thu, 06 Oct 2022 20:16:43 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ed07ae854e5b9e7d93d0c5eb8bbcfb2d6e5eddeb00720efe7b55766ce5bfbab`  
		Last Modified: Thu, 06 Oct 2022 20:16:41 GMT  
		Size: 284.6 KB (284583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19dfd580c937a95d72fb2af50a28c6814b4886872b951143883b0ffde4712c5f`  
		Last Modified: Thu, 06 Oct 2022 20:17:11 GMT  
		Size: 19.7 MB (19672168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9e61e6634ea5e9aa1e5e15257ac4db9252543ec14ac7bd8989d98dca8f7b54f`  
		Last Modified: Thu, 06 Oct 2022 20:17:08 GMT  
		Size: 12.3 KB (12265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f00f1a43c212b770a42e5c7bc1563a4df034c07a36e2d6f937d26b1d907303e`  
		Last Modified: Thu, 06 Oct 2022 20:17:08 GMT  
		Size: 11.9 KB (11898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4bb73bba03a148277f19627c4b0811fb06e034afa29b8939eb47b20577a3537`  
		Last Modified: Thu, 06 Oct 2022 20:17:08 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:alpine`

```console
$ docker pull chronograf@sha256:c92d2e5d3aaed3d5abd3e21e85b3dd60e8169f7bf6699f473aed28eabff1d043
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:de6c4148eeb1291ced92120697fad8332c74a726171672daf7c7b67e21d3850b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30311143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d58f859d1dc29bb2ee9f917635f6eb5621000d9d6619ec8ad4549203995550f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:07 GMT
ADD file:b9bd10cf83356cb7281baa0fbaca5186cf27491f59eda87abe57f83a5aaf5ec1 in / 
# Tue, 09 Aug 2022 17:20:08 GMT
CMD ["/bin/sh"]
# Thu, 06 Oct 2022 20:15:36 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 06 Oct 2022 20:15:37 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Thu, 06 Oct 2022 20:16:09 GMT
ENV CHRONOGRAF_VERSION=1.10.0
# Thu, 06 Oct 2022 20:16:16 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 06 Oct 2022 20:16:17 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 06 Oct 2022 20:16:17 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 06 Oct 2022 20:16:17 GMT
EXPOSE 8888
# Thu, 06 Oct 2022 20:16:17 GMT
VOLUME [/var/lib/chronograf]
# Thu, 06 Oct 2022 20:16:17 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Thu, 06 Oct 2022 20:16:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 06 Oct 2022 20:16:17 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:c7ed990a2339ee598662849de4f56e2241399f5a32340c8c4a7bbd5378a12b5f`  
		Last Modified: Tue, 09 Aug 2022 17:21:06 GMT  
		Size: 2.8 MB (2827489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:133509570f70da73b5369d8311a4269568dbea851313f10ea1b8cb1a2c4e2fe8`  
		Last Modified: Thu, 06 Oct 2022 20:16:43 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ed07ae854e5b9e7d93d0c5eb8bbcfb2d6e5eddeb00720efe7b55766ce5bfbab`  
		Last Modified: Thu, 06 Oct 2022 20:16:41 GMT  
		Size: 284.6 KB (284583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eea9d4a8a69cd5e2e5fca1b123ba2cd44364cf36b128c2fe59a5edf12221dfd`  
		Last Modified: Thu, 06 Oct 2022 20:17:26 GMT  
		Size: 27.2 MB (27174517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76a685cca594b365e8c9e5d2a452959ac02b6fde12a79d898abf1a833a483707`  
		Last Modified: Thu, 06 Oct 2022 20:17:21 GMT  
		Size: 12.3 KB (12265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80dba48a5545ef21547b2590458104e7bf680e4a5afbd1707de156d2d9420751`  
		Last Modified: Thu, 06 Oct 2022 20:17:21 GMT  
		Size: 11.9 KB (11897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ece5a9a06b7739faf864ebca0e4561819e3e331b928666a09e2c5bb2b9b2181`  
		Last Modified: Thu, 06 Oct 2022 20:17:21 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:latest`

```console
$ docker pull chronograf@sha256:5f801513652ec6ead872a616599e58f92915b0dc35890c7bc0e37633b07c71cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:latest` - linux; amd64

```console
$ docker pull chronograf@sha256:29ab1b9d91d0c5493c5a5da0a6d8d81098d48a4217cdfe1452dcefa8b5e4a720
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.3 MB (81254093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bc3e83e2be670ef62324a08070a2c4836172d7f37b0b841a50fcc5705ea594c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 06 Dec 2022 01:20:54 GMT
ADD file:1f1efd56601ebc26a041a7b994a380ef68112b91a078e225753bee7b3196d22c in / 
# Tue, 06 Dec 2022 01:20:54 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 01:46:01 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 06 Dec 2022 01:46:27 GMT
ENV CHRONOGRAF_VERSION=1.10.0
# Tue, 06 Dec 2022 01:46:34 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 06 Dec 2022 01:46:34 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 06 Dec 2022 01:46:35 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 06 Dec 2022 01:46:35 GMT
EXPOSE 8888
# Tue, 06 Dec 2022 01:46:35 GMT
VOLUME [/var/lib/chronograf]
# Tue, 06 Dec 2022 01:46:35 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 06 Dec 2022 01:46:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 06 Dec 2022 01:46:35 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:025c56f98b679f70b7a54241917e56da7b59ab9d2defecc6ebdb0bf2750484bb`  
		Last Modified: Tue, 06 Dec 2022 01:25:12 GMT  
		Size: 31.4 MB (31412852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89ff5a347561490589cdaddbb9c1d1fd79814edac3ddf8bc928b34dddfd7c5bb`  
		Last Modified: Tue, 06 Dec 2022 01:47:14 GMT  
		Size: 5.2 MB (5228712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a86e4af0a7ab80153783e9829b83a062eb28cb99ba473fdb07e876952c8354b1`  
		Last Modified: Tue, 06 Dec 2022 01:47:47 GMT  
		Size: 44.6 MB (44588133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edc2df382812100ec1f9eee6ae9216b67d9d9ae41984fab817ddf26ef056701d`  
		Last Modified: Tue, 06 Dec 2022 01:47:41 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbb68818fcfd812eb6559bb580d3b5be78474c1a0bda9b702987437c87c66309`  
		Last Modified: Tue, 06 Dec 2022 01:47:41 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c1a18d308edf2a5a71cfaffc3459b9585962a4b199e557cc2c662df81a27165`  
		Last Modified: Tue, 06 Dec 2022 01:47:41 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:latest` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:940df312875251e09bb551952c88e719e921217382ca2c0e458d679581d0206b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.6 MB (73560703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d46c8e5d166b1c72df66ec7e56027579e92b228d2e13fff21043839e020152f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 06 Dec 2022 00:58:51 GMT
ADD file:cb354f875d5631d5d4542ab57d0b9b323a261f5c631d5917127504d6eb54d85a in / 
# Tue, 06 Dec 2022 00:58:52 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 10:15:54 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 06 Dec 2022 10:16:29 GMT
ENV CHRONOGRAF_VERSION=1.10.0
# Tue, 06 Dec 2022 10:16:38 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 06 Dec 2022 10:16:38 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 06 Dec 2022 10:16:38 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 06 Dec 2022 10:16:38 GMT
EXPOSE 8888
# Tue, 06 Dec 2022 10:16:39 GMT
VOLUME [/var/lib/chronograf]
# Tue, 06 Dec 2022 10:16:39 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 06 Dec 2022 10:16:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 06 Dec 2022 10:16:39 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:4f32a98d14d26603bb8e8cf9bda992e24606d2fe00101767049a01d5176929e1`  
		Last Modified: Tue, 06 Dec 2022 01:06:05 GMT  
		Size: 26.6 MB (26576348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13331aa96eaee2e9e3ef374955946cbe0508467ec66e9c44cb3122bc85393b6e`  
		Last Modified: Tue, 06 Dec 2022 10:17:29 GMT  
		Size: 4.5 MB (4495026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72b493b2a2579f2080785c4a4e7d3db8e4d7e25e6e0afce8a048cafd3b0c0cfb`  
		Last Modified: Tue, 06 Dec 2022 10:18:08 GMT  
		Size: 42.5 MB (42464936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8875c67483f82bc20ddf506d0b3f57cac5bdc74b4ff8c31caf40a6b3b8931597`  
		Last Modified: Tue, 06 Dec 2022 10:18:00 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1458f13cd06ea42cd5ae8d1d467c93cf83f290077dad0887a29a5b3f74a87596`  
		Last Modified: Tue, 06 Dec 2022 10:18:00 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31c35ed9bc20a5bb6678297d9f268738785c2af7b2a63949d0ad2e4dd873b310`  
		Last Modified: Tue, 06 Dec 2022 10:18:00 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:latest` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:b9a923a7f9577ea18562ca96d20f9092d3564d8b7fdbab907678a2125762c73d
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.9 MB (77914187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36b562de4f793f8bfe522fb78778dadf5df254c69bff24023d08eda93fbfe602`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 06 Dec 2022 01:40:17 GMT
ADD file:379d6ac56afdb6e02d71fa0faebc13b8a2554fc6ae76c5f5bbdb5b8e475135d6 in / 
# Tue, 06 Dec 2022 01:40:17 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 02:15:19 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 06 Dec 2022 02:15:36 GMT
ENV CHRONOGRAF_VERSION=1.10.0
# Tue, 06 Dec 2022 02:15:41 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 06 Dec 2022 02:15:42 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 06 Dec 2022 02:15:42 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 06 Dec 2022 02:15:42 GMT
EXPOSE 8888
# Tue, 06 Dec 2022 02:15:42 GMT
VOLUME [/var/lib/chronograf]
# Tue, 06 Dec 2022 02:15:42 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 06 Dec 2022 02:15:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 06 Dec 2022 02:15:43 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:6064e7e5b6afa4dc711228eddfd250aebac271830dc184c400ce640020bc2cb0`  
		Last Modified: Tue, 06 Dec 2022 01:43:56 GMT  
		Size: 30.1 MB (30060320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:010bcfd47e4f0331c64dfb2af5573bf99a4b88b4d972387850c61ff6ef0d11a9`  
		Last Modified: Tue, 06 Dec 2022 02:16:10 GMT  
		Size: 5.2 MB (5211566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f63cfceb30c24c808b43865619c58241102c036bd153c354e2f2f1457954400`  
		Last Modified: Tue, 06 Dec 2022 02:16:37 GMT  
		Size: 42.6 MB (42617907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb34459112efb5b29d1c5cbe97dad350e283c8259b45e077aa3104ff0a7c432b`  
		Last Modified: Tue, 06 Dec 2022 02:16:32 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21072e41358457fcdb1399f31b7dd73322af50a96fc66fe37b8841d39bb92579`  
		Last Modified: Tue, 06 Dec 2022 02:16:32 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ca77523a925a0d9872b733837dba904a8a82c95de486d5f95f5bf8678deb165`  
		Last Modified: Tue, 06 Dec 2022 02:16:32 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
