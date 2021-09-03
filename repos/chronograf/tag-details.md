<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `chronograf`

-	[`chronograf:1.6`](#chronograf16)
-	[`chronograf:1.6-alpine`](#chronograf16-alpine)
-	[`chronograf:1.6.2`](#chronograf162)
-	[`chronograf:1.6.2-alpine`](#chronograf162-alpine)
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
-	[`chronograf:1.9.0`](#chronograf190)
-	[`chronograf:1.9.0-alpine`](#chronograf190-alpine)
-	[`chronograf:alpine`](#chronografalpine)
-	[`chronograf:latest`](#chronograflatest)

## `chronograf:1.6`

```console
$ docker pull chronograf@sha256:b56a177db7454ce6e85d075b6005b2d3d9b9eefa95afb27564a7e3179d318bee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.6` - linux; amd64

```console
$ docker pull chronograf@sha256:3b4660a26f389836597fb2b820c1575a0f927f158fafdbbd75f5cfca03cf22ff
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49357420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:310cbe311dfb78e8644fc4e01b72c743add6339c31ddad257afcbcea04839dec`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 17 Aug 2021 01:26:09 GMT
ADD file:f6c4487fa1f7a4e17f5d88fd0c91031a6efc7fa210d363a1d43d8b0f3a8d1d03 in / 
# Tue, 17 Aug 2021 01:26:09 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 09:35:17 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 17 Aug 2021 09:35:18 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Tue, 17 Aug 2021 09:35:28 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 17 Aug 2021 09:35:29 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 17 Aug 2021 09:35:29 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 17 Aug 2021 09:35:29 GMT
EXPOSE 8888
# Tue, 17 Aug 2021 09:35:30 GMT
VOLUME [/var/lib/chronograf]
# Tue, 17 Aug 2021 09:35:30 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 17 Aug 2021 09:35:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Aug 2021 09:35:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:33f99cea3b7da8c6e0143c9fd7590c6d56f7d310ddd59b11be4ad485ae4cab2a`  
		Last Modified: Tue, 17 Aug 2021 01:33:27 GMT  
		Size: 22.5 MB (22527748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6ebf00cee8edb2723f73bb596dc02dac400fcd609c6288b968066e0333dc5cd`  
		Last Modified: Tue, 17 Aug 2021 09:37:00 GMT  
		Size: 6.8 MB (6760152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccda430674c7927de7007bb50f73dece289da6d73e105bff2ef5c92500989d69`  
		Last Modified: Tue, 17 Aug 2021 09:37:02 GMT  
		Size: 20.0 MB (20045128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd5c8c3233de6e30d92f753e7ab5939410ec8ac407ff9f7a15ba73666c7caf82`  
		Last Modified: Tue, 17 Aug 2021 09:36:58 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3f441ad12b885a481ebc2e5f518f52099cbc6ca3e6b1a60a4fa43a433038734`  
		Last Modified: Tue, 17 Aug 2021 09:36:58 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:738a6d4707ebd96360080f6d9b73b271fb4ee1219cf558079a5655dd9f2f2ef2`  
		Last Modified: Tue, 17 Aug 2021 09:36:58 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.6` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:d33f2016d96c512839131152bb8eb80d2f25925cade13598fbf7eb73eba92a3b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.9 MB (43940168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d71feca0d8b5cc6f3f107b403a7cee658f8a630561937b9ea8c170f375d83dc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 03 Sep 2021 01:05:16 GMT
ADD file:425f8ae3b1354b9858904edb027190b58b65692a710cb50a4d463ac554f853a6 in / 
# Fri, 03 Sep 2021 01:05:17 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 02:45:29 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 03 Sep 2021 02:45:29 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Fri, 03 Sep 2021 02:45:49 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Fri, 03 Sep 2021 02:45:50 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 03 Sep 2021 02:45:50 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 03 Sep 2021 02:45:51 GMT
EXPOSE 8888
# Fri, 03 Sep 2021 02:45:51 GMT
VOLUME [/var/lib/chronograf]
# Fri, 03 Sep 2021 02:45:52 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Fri, 03 Sep 2021 02:45:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 03 Sep 2021 02:45:53 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:0c15a1a8c9dffe5dfe059b37d14b92f1eb4ea47f16ae7bf66bf62f34a7510dd6`  
		Last Modified: Fri, 03 Sep 2021 01:22:37 GMT  
		Size: 19.3 MB (19316099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb41f6e44cc2adc7b1da1ef11c2a061b83d79ad3aec2895b90e80a08e2eeb1be`  
		Last Modified: Fri, 03 Sep 2021 02:49:09 GMT  
		Size: 5.8 MB (5779569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e39329e39739f246799f8332fb275aeed7d3e76d7d163cb3d6e741356538bb00`  
		Last Modified: Fri, 03 Sep 2021 02:49:24 GMT  
		Size: 18.8 MB (18820116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b9a24630aba0f68d5d975a50879cc35da631f2c4077368219555053519c8975`  
		Last Modified: Fri, 03 Sep 2021 02:49:07 GMT  
		Size: 12.2 KB (12243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40e30ec87c35d229130ff0dab13773ed349331993cac16a3f49a3cf0da5c9b3e`  
		Last Modified: Fri, 03 Sep 2021 02:49:07 GMT  
		Size: 11.9 KB (11902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cca92eca14d4951fbe4ff33b1a13d7f2e8331c7b47c1e6ba95b705c10130c7f5`  
		Last Modified: Fri, 03 Sep 2021 02:49:07 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.6` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:b3993f5a0342eb8518ecb45f32402b4826530ac265ee9895a0fceff87280b1f3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45423113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0a0d2cce6e71edafe80039323e3f015795acf91d7028ea71b83f0a57c7e5c42`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 17 Aug 2021 01:48:32 GMT
ADD file:5cd26935234cc0540158a144066c0341b46a0caeb0a80db0355eeb8cfaf4fc0d in / 
# Tue, 17 Aug 2021 01:48:32 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 08:06:44 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 17 Aug 2021 08:06:44 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Tue, 17 Aug 2021 08:06:51 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 17 Aug 2021 08:06:51 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 17 Aug 2021 08:06:51 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 17 Aug 2021 08:06:51 GMT
EXPOSE 8888
# Tue, 17 Aug 2021 08:06:51 GMT
VOLUME [/var/lib/chronograf]
# Tue, 17 Aug 2021 08:06:52 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 17 Aug 2021 08:06:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Aug 2021 08:06:52 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:f862659192cd149f96ede75854bd3ebf59937831d3e4103087ae62df34ef1a29`  
		Last Modified: Tue, 17 Aug 2021 01:58:00 GMT  
		Size: 20.4 MB (20389447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09101c696c7496dfd097387796cbe96c76aa138b186200c5879c0ab29f5a13f4`  
		Last Modified: Tue, 17 Aug 2021 08:08:19 GMT  
		Size: 6.0 MB (6047480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b35a7bd7a24d14e7b972d73641567d9c535809bab448e644897b986e607352bf`  
		Last Modified: Tue, 17 Aug 2021 08:08:21 GMT  
		Size: 19.0 MB (18961797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fffa82191109e148463f249f7ab2a56bcbe64c66f80df2f4de01b0df040bfca6`  
		Last Modified: Tue, 17 Aug 2021 08:08:18 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fbe4df1b8d5a112e6eb342cca21bef851272f6f1fad782db24a6e6717463fef`  
		Last Modified: Tue, 17 Aug 2021 08:08:18 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84c8867c495c8baef876e2b57f77f5c856af2b43e06970f7ad6f6bb767a495ad`  
		Last Modified: Tue, 17 Aug 2021 08:08:18 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.6-alpine`

```console
$ docker pull chronograf@sha256:a3dea9fd70283af740db184d94417ee4c3fc1375532175d597122c325b664c27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.6-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:b14ee1822937fb01816a97288646858f187d0f02f9fd6eeeb448b30d07b2617c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14843918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c622c45336d64ee0a6e08ce97bc55bf23712e39ca3061372e2000223e9cf6a5c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 31 Aug 2021 23:18:23 GMT
ADD file:e3d2013df9d58cd9255c749dbd62e7b1b1bdf1c2ee644c17bb93e67d859f0815 in / 
# Tue, 31 Aug 2021 23:18:24 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 00:23:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 01 Sep 2021 00:23:43 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Wed, 01 Sep 2021 00:23:43 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Wed, 01 Sep 2021 00:23:52 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 01 Sep 2021 00:23:52 GMT
COPY file:aa4a9d01295c7013d89da92a943af071556aea6dbe6269affd4664fdd86969b8 in /usr/share/chronograf/LICENSE 
# Wed, 01 Sep 2021 00:23:52 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 01 Sep 2021 00:23:53 GMT
EXPOSE 8888
# Wed, 01 Sep 2021 00:23:53 GMT
VOLUME [/var/lib/chronograf]
# Wed, 01 Sep 2021 00:23:53 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Wed, 01 Sep 2021 00:23:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Sep 2021 00:23:54 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:e519532ddf75bafbbb0ad01d3fb678ef9395cd8554fa25bef4695bb6e11f39f1`  
		Last Modified: Tue, 31 Aug 2021 23:19:05 GMT  
		Size: 2.8 MB (2801707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e69cd3502d3b453e253ea48e4ff56f5af4e25895a1bfa5e84cda59eaefce23be`  
		Last Modified: Wed, 01 Sep 2021 00:25:31 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7087df4b29e442773e368f72aa50cd7765fd6e6b43879c83880b0038e62b9077`  
		Last Modified: Wed, 01 Sep 2021 00:25:29 GMT  
		Size: 280.9 KB (280879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62726903f0c0c59223b83affe0ace7300a908ba6fcea73b6c79ae3a146d2b5af`  
		Last Modified: Wed, 01 Sep 2021 00:25:31 GMT  
		Size: 11.7 MB (11736770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fff4336cfd351b47edce706376e043d71589101d40dce396d37efca10babe80d`  
		Last Modified: Wed, 01 Sep 2021 00:25:28 GMT  
		Size: 12.3 KB (12273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbbb150a469535e39e060b4b33bcad3378c611bded830e04ccb39c1942fb50de`  
		Last Modified: Wed, 01 Sep 2021 00:25:28 GMT  
		Size: 11.9 KB (11899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3550bbef48514edb6130449969746fb016808bb6c02b3e838ac98278f8869df1`  
		Last Modified: Wed, 01 Sep 2021 00:25:28 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.6.2`

```console
$ docker pull chronograf@sha256:b56a177db7454ce6e85d075b6005b2d3d9b9eefa95afb27564a7e3179d318bee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.6.2` - linux; amd64

```console
$ docker pull chronograf@sha256:3b4660a26f389836597fb2b820c1575a0f927f158fafdbbd75f5cfca03cf22ff
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49357420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:310cbe311dfb78e8644fc4e01b72c743add6339c31ddad257afcbcea04839dec`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 17 Aug 2021 01:26:09 GMT
ADD file:f6c4487fa1f7a4e17f5d88fd0c91031a6efc7fa210d363a1d43d8b0f3a8d1d03 in / 
# Tue, 17 Aug 2021 01:26:09 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 09:35:17 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 17 Aug 2021 09:35:18 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Tue, 17 Aug 2021 09:35:28 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 17 Aug 2021 09:35:29 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 17 Aug 2021 09:35:29 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 17 Aug 2021 09:35:29 GMT
EXPOSE 8888
# Tue, 17 Aug 2021 09:35:30 GMT
VOLUME [/var/lib/chronograf]
# Tue, 17 Aug 2021 09:35:30 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 17 Aug 2021 09:35:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Aug 2021 09:35:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:33f99cea3b7da8c6e0143c9fd7590c6d56f7d310ddd59b11be4ad485ae4cab2a`  
		Last Modified: Tue, 17 Aug 2021 01:33:27 GMT  
		Size: 22.5 MB (22527748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6ebf00cee8edb2723f73bb596dc02dac400fcd609c6288b968066e0333dc5cd`  
		Last Modified: Tue, 17 Aug 2021 09:37:00 GMT  
		Size: 6.8 MB (6760152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccda430674c7927de7007bb50f73dece289da6d73e105bff2ef5c92500989d69`  
		Last Modified: Tue, 17 Aug 2021 09:37:02 GMT  
		Size: 20.0 MB (20045128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd5c8c3233de6e30d92f753e7ab5939410ec8ac407ff9f7a15ba73666c7caf82`  
		Last Modified: Tue, 17 Aug 2021 09:36:58 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3f441ad12b885a481ebc2e5f518f52099cbc6ca3e6b1a60a4fa43a433038734`  
		Last Modified: Tue, 17 Aug 2021 09:36:58 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:738a6d4707ebd96360080f6d9b73b271fb4ee1219cf558079a5655dd9f2f2ef2`  
		Last Modified: Tue, 17 Aug 2021 09:36:58 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.6.2` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:d33f2016d96c512839131152bb8eb80d2f25925cade13598fbf7eb73eba92a3b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.9 MB (43940168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d71feca0d8b5cc6f3f107b403a7cee658f8a630561937b9ea8c170f375d83dc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 03 Sep 2021 01:05:16 GMT
ADD file:425f8ae3b1354b9858904edb027190b58b65692a710cb50a4d463ac554f853a6 in / 
# Fri, 03 Sep 2021 01:05:17 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 02:45:29 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 03 Sep 2021 02:45:29 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Fri, 03 Sep 2021 02:45:49 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Fri, 03 Sep 2021 02:45:50 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 03 Sep 2021 02:45:50 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 03 Sep 2021 02:45:51 GMT
EXPOSE 8888
# Fri, 03 Sep 2021 02:45:51 GMT
VOLUME [/var/lib/chronograf]
# Fri, 03 Sep 2021 02:45:52 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Fri, 03 Sep 2021 02:45:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 03 Sep 2021 02:45:53 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:0c15a1a8c9dffe5dfe059b37d14b92f1eb4ea47f16ae7bf66bf62f34a7510dd6`  
		Last Modified: Fri, 03 Sep 2021 01:22:37 GMT  
		Size: 19.3 MB (19316099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb41f6e44cc2adc7b1da1ef11c2a061b83d79ad3aec2895b90e80a08e2eeb1be`  
		Last Modified: Fri, 03 Sep 2021 02:49:09 GMT  
		Size: 5.8 MB (5779569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e39329e39739f246799f8332fb275aeed7d3e76d7d163cb3d6e741356538bb00`  
		Last Modified: Fri, 03 Sep 2021 02:49:24 GMT  
		Size: 18.8 MB (18820116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b9a24630aba0f68d5d975a50879cc35da631f2c4077368219555053519c8975`  
		Last Modified: Fri, 03 Sep 2021 02:49:07 GMT  
		Size: 12.2 KB (12243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40e30ec87c35d229130ff0dab13773ed349331993cac16a3f49a3cf0da5c9b3e`  
		Last Modified: Fri, 03 Sep 2021 02:49:07 GMT  
		Size: 11.9 KB (11902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cca92eca14d4951fbe4ff33b1a13d7f2e8331c7b47c1e6ba95b705c10130c7f5`  
		Last Modified: Fri, 03 Sep 2021 02:49:07 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.6.2` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:b3993f5a0342eb8518ecb45f32402b4826530ac265ee9895a0fceff87280b1f3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45423113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0a0d2cce6e71edafe80039323e3f015795acf91d7028ea71b83f0a57c7e5c42`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 17 Aug 2021 01:48:32 GMT
ADD file:5cd26935234cc0540158a144066c0341b46a0caeb0a80db0355eeb8cfaf4fc0d in / 
# Tue, 17 Aug 2021 01:48:32 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 08:06:44 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 17 Aug 2021 08:06:44 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Tue, 17 Aug 2021 08:06:51 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 17 Aug 2021 08:06:51 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 17 Aug 2021 08:06:51 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 17 Aug 2021 08:06:51 GMT
EXPOSE 8888
# Tue, 17 Aug 2021 08:06:51 GMT
VOLUME [/var/lib/chronograf]
# Tue, 17 Aug 2021 08:06:52 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 17 Aug 2021 08:06:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Aug 2021 08:06:52 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:f862659192cd149f96ede75854bd3ebf59937831d3e4103087ae62df34ef1a29`  
		Last Modified: Tue, 17 Aug 2021 01:58:00 GMT  
		Size: 20.4 MB (20389447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09101c696c7496dfd097387796cbe96c76aa138b186200c5879c0ab29f5a13f4`  
		Last Modified: Tue, 17 Aug 2021 08:08:19 GMT  
		Size: 6.0 MB (6047480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b35a7bd7a24d14e7b972d73641567d9c535809bab448e644897b986e607352bf`  
		Last Modified: Tue, 17 Aug 2021 08:08:21 GMT  
		Size: 19.0 MB (18961797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fffa82191109e148463f249f7ab2a56bcbe64c66f80df2f4de01b0df040bfca6`  
		Last Modified: Tue, 17 Aug 2021 08:08:18 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fbe4df1b8d5a112e6eb342cca21bef851272f6f1fad782db24a6e6717463fef`  
		Last Modified: Tue, 17 Aug 2021 08:08:18 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84c8867c495c8baef876e2b57f77f5c856af2b43e06970f7ad6f6bb767a495ad`  
		Last Modified: Tue, 17 Aug 2021 08:08:18 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.6.2-alpine`

```console
$ docker pull chronograf@sha256:a3dea9fd70283af740db184d94417ee4c3fc1375532175d597122c325b664c27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.6.2-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:b14ee1822937fb01816a97288646858f187d0f02f9fd6eeeb448b30d07b2617c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14843918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c622c45336d64ee0a6e08ce97bc55bf23712e39ca3061372e2000223e9cf6a5c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 31 Aug 2021 23:18:23 GMT
ADD file:e3d2013df9d58cd9255c749dbd62e7b1b1bdf1c2ee644c17bb93e67d859f0815 in / 
# Tue, 31 Aug 2021 23:18:24 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 00:23:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 01 Sep 2021 00:23:43 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Wed, 01 Sep 2021 00:23:43 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Wed, 01 Sep 2021 00:23:52 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 01 Sep 2021 00:23:52 GMT
COPY file:aa4a9d01295c7013d89da92a943af071556aea6dbe6269affd4664fdd86969b8 in /usr/share/chronograf/LICENSE 
# Wed, 01 Sep 2021 00:23:52 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 01 Sep 2021 00:23:53 GMT
EXPOSE 8888
# Wed, 01 Sep 2021 00:23:53 GMT
VOLUME [/var/lib/chronograf]
# Wed, 01 Sep 2021 00:23:53 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Wed, 01 Sep 2021 00:23:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Sep 2021 00:23:54 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:e519532ddf75bafbbb0ad01d3fb678ef9395cd8554fa25bef4695bb6e11f39f1`  
		Last Modified: Tue, 31 Aug 2021 23:19:05 GMT  
		Size: 2.8 MB (2801707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e69cd3502d3b453e253ea48e4ff56f5af4e25895a1bfa5e84cda59eaefce23be`  
		Last Modified: Wed, 01 Sep 2021 00:25:31 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7087df4b29e442773e368f72aa50cd7765fd6e6b43879c83880b0038e62b9077`  
		Last Modified: Wed, 01 Sep 2021 00:25:29 GMT  
		Size: 280.9 KB (280879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62726903f0c0c59223b83affe0ace7300a908ba6fcea73b6c79ae3a146d2b5af`  
		Last Modified: Wed, 01 Sep 2021 00:25:31 GMT  
		Size: 11.7 MB (11736770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fff4336cfd351b47edce706376e043d71589101d40dce396d37efca10babe80d`  
		Last Modified: Wed, 01 Sep 2021 00:25:28 GMT  
		Size: 12.3 KB (12273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbbb150a469535e39e060b4b33bcad3378c611bded830e04ccb39c1942fb50de`  
		Last Modified: Wed, 01 Sep 2021 00:25:28 GMT  
		Size: 11.9 KB (11899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3550bbef48514edb6130449969746fb016808bb6c02b3e838ac98278f8869df1`  
		Last Modified: Wed, 01 Sep 2021 00:25:28 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.7`

```console
$ docker pull chronograf@sha256:4cd571df7045704646115f9d3e75f8f4d07a72c7fd6d209dbaddafb63aeebd92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.7` - linux; amd64

```console
$ docker pull chronograf@sha256:a0bd7f9a7a6f41e1bff144f6705cbd765ad16522cd5c79f6e550d680b404c6c9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.4 MB (65385969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ec19aa91c9ffb33b4a9a9682dbb6c75d3b197f70a15fdfc2dd0a4e088425d23`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 17 Aug 2021 01:26:09 GMT
ADD file:f6c4487fa1f7a4e17f5d88fd0c91031a6efc7fa210d363a1d43d8b0f3a8d1d03 in / 
# Tue, 17 Aug 2021 01:26:09 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 09:35:45 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 17 Aug 2021 09:35:46 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 17 Aug 2021 09:35:57 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 17 Aug 2021 09:35:57 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 17 Aug 2021 09:35:58 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 17 Aug 2021 09:35:58 GMT
EXPOSE 8888
# Tue, 17 Aug 2021 09:35:58 GMT
VOLUME [/var/lib/chronograf]
# Tue, 17 Aug 2021 09:35:58 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 17 Aug 2021 09:35:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Aug 2021 09:35:59 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:33f99cea3b7da8c6e0143c9fd7590c6d56f7d310ddd59b11be4ad485ae4cab2a`  
		Last Modified: Tue, 17 Aug 2021 01:33:27 GMT  
		Size: 22.5 MB (22527748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b30e58325c4aced5f8b1db67699808a32667aa9b4c6ce8f2bdfa2483c1fca5d`  
		Last Modified: Tue, 17 Aug 2021 09:37:14 GMT  
		Size: 4.5 MB (4506000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feaf4e133d20eb12180b56077702463f8b86964c0c436a6428ba22d49937aee9`  
		Last Modified: Tue, 17 Aug 2021 09:37:19 GMT  
		Size: 38.3 MB (38327828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9423787f4c740286bf12eb3babfa4d046ac80fe5a0df99011d36bc7157b5b58`  
		Last Modified: Tue, 17 Aug 2021 09:37:13 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:327bac57cd40f7913cf4c837b08e39f503a2a96d4d741b7357a346936be0c4c6`  
		Last Modified: Tue, 17 Aug 2021 09:37:13 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dc64a52a995cae676aef575882522843ca58890ae3dac6b44c5661dffcf7173`  
		Last Modified: Tue, 17 Aug 2021 09:37:13 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.7` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:8b3b18fc16ecc98e1bf91daaa69ba32719b5c6aea8f1816553ba941399eac678
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.0 MB (59002534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bcd89da09295d29aeddbf3b845afd96a58b115fbcb4aaeb3f1e9b4126500260`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 03 Sep 2021 01:05:16 GMT
ADD file:425f8ae3b1354b9858904edb027190b58b65692a710cb50a4d463ac554f853a6 in / 
# Fri, 03 Sep 2021 01:05:17 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 02:46:19 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 03 Sep 2021 02:46:19 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Fri, 03 Sep 2021 02:46:52 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Fri, 03 Sep 2021 02:46:53 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 03 Sep 2021 02:46:53 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 03 Sep 2021 02:46:54 GMT
EXPOSE 8888
# Fri, 03 Sep 2021 02:46:54 GMT
VOLUME [/var/lib/chronograf]
# Fri, 03 Sep 2021 02:46:55 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Fri, 03 Sep 2021 02:46:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 03 Sep 2021 02:46:56 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:0c15a1a8c9dffe5dfe059b37d14b92f1eb4ea47f16ae7bf66bf62f34a7510dd6`  
		Last Modified: Fri, 03 Sep 2021 01:22:37 GMT  
		Size: 19.3 MB (19316099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72feb6c10261bcd9f265aa351af235fc6d6eb3473fad71a9579edc13f7328fa2`  
		Last Modified: Fri, 03 Sep 2021 02:49:40 GMT  
		Size: 3.9 MB (3879487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ddcfdb344e67d03f1b7a9cd328a06cbeca291255d3be23eace2601350070fa8`  
		Last Modified: Fri, 03 Sep 2021 02:49:56 GMT  
		Size: 35.8 MB (35782561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:066675693109c82818a2b7cd4bd8a8e696b01141184fe0ee98354c45b0fbc140`  
		Last Modified: Fri, 03 Sep 2021 02:49:38 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c4e25e7194766392fd80eed393de68cd1e2fb01396ecb0a421dbb046e1fc947`  
		Last Modified: Fri, 03 Sep 2021 02:49:38 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7170ad340de1bfc4912904c7dedb7f2308b8593444f2c0503a68b16faffdfa7b`  
		Last Modified: Fri, 03 Sep 2021 02:49:38 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.7` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:784ae2f5b10603b07a9469b6f024c2381eadba945c359aa00ff63815d49d2f07
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.5 MB (60482129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:addf16420eaf0c8efe1c3d1b592739421caa793126f877f4e221875ed395af62`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 17 Aug 2021 01:48:32 GMT
ADD file:5cd26935234cc0540158a144066c0341b46a0caeb0a80db0355eeb8cfaf4fc0d in / 
# Tue, 17 Aug 2021 01:48:32 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 08:07:08 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 17 Aug 2021 08:07:08 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 17 Aug 2021 08:07:17 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 17 Aug 2021 08:07:18 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 17 Aug 2021 08:07:18 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 17 Aug 2021 08:07:18 GMT
EXPOSE 8888
# Tue, 17 Aug 2021 08:07:18 GMT
VOLUME [/var/lib/chronograf]
# Tue, 17 Aug 2021 08:07:18 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 17 Aug 2021 08:07:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Aug 2021 08:07:19 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:f862659192cd149f96ede75854bd3ebf59937831d3e4103087ae62df34ef1a29`  
		Last Modified: Tue, 17 Aug 2021 01:58:00 GMT  
		Size: 20.4 MB (20389447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a633450ca1e80832c0d9d386dc78f5a7b17e96988c46adfce9f7fb9df3080cc8`  
		Last Modified: Tue, 17 Aug 2021 08:08:33 GMT  
		Size: 4.1 MB (4082143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:369d3b51668baff5b0af480d4afb8749ee0292e2bc1cda07ffb54f639a9bbf11`  
		Last Modified: Tue, 17 Aug 2021 08:08:37 GMT  
		Size: 36.0 MB (35986144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc24a9d100c2c1bddd8eb913e91e3ae5f1a7c73e8022cd1d9662b40460015b81`  
		Last Modified: Tue, 17 Aug 2021 08:08:32 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d61d15ba426300c200c2f21e8a6d770db59bda2a4345a5f1f8e6c57b2b14215c`  
		Last Modified: Tue, 17 Aug 2021 08:08:32 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eedb0a234ee76ab5785a3e9e6a79e908e8c003c24ac020d6ce8cbafd93df9774`  
		Last Modified: Tue, 17 Aug 2021 08:08:32 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.7-alpine`

```console
$ docker pull chronograf@sha256:9b177c70e25de297b100d46ba7eb922ac167a8e65f698480e2785b1886cb94a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.7-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:c3a41e489e87268456b3ac8beea5f7c2a516dc7d43af6f7066be8b9675492d70
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22662384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a94fa13b711dbb3a88df7489d3353cc6e4777a37a87a0788d36cef2fdc64c95`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 31 Aug 2021 23:18:23 GMT
ADD file:e3d2013df9d58cd9255c749dbd62e7b1b1bdf1c2ee644c17bb93e67d859f0815 in / 
# Tue, 31 Aug 2021 23:18:24 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 00:23:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 01 Sep 2021 00:23:43 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Wed, 01 Sep 2021 00:24:02 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Wed, 01 Sep 2021 00:24:13 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 01 Sep 2021 00:24:14 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 01 Sep 2021 00:24:15 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 01 Sep 2021 00:24:15 GMT
EXPOSE 8888
# Wed, 01 Sep 2021 00:24:15 GMT
VOLUME [/var/lib/chronograf]
# Wed, 01 Sep 2021 00:24:16 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Wed, 01 Sep 2021 00:24:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Sep 2021 00:24:16 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:e519532ddf75bafbbb0ad01d3fb678ef9395cd8554fa25bef4695bb6e11f39f1`  
		Last Modified: Tue, 31 Aug 2021 23:19:05 GMT  
		Size: 2.8 MB (2801707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e69cd3502d3b453e253ea48e4ff56f5af4e25895a1bfa5e84cda59eaefce23be`  
		Last Modified: Wed, 01 Sep 2021 00:25:31 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7087df4b29e442773e368f72aa50cd7765fd6e6b43879c83880b0038e62b9077`  
		Last Modified: Wed, 01 Sep 2021 00:25:29 GMT  
		Size: 280.9 KB (280879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75a1ffa92682ef14beba92c11f3c21d02b50a70f56f234ab814e604f678b2b31`  
		Last Modified: Wed, 01 Sep 2021 00:25:49 GMT  
		Size: 19.6 MB (19555249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37dbb12c4afee159bb53c97f3d0cb65034efe2713363365b1f7f5f7affb916fe`  
		Last Modified: Wed, 01 Sep 2021 00:25:43 GMT  
		Size: 12.3 KB (12265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:344ba26fb8530e7520df76f60ae8b3f9e317561d15deea2b4738f5c3e4b47e11`  
		Last Modified: Wed, 01 Sep 2021 00:25:43 GMT  
		Size: 11.9 KB (11895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da9b8b115b6329338ab5fea52358a641fbb017ecd917613643e4cbce6b3f081f`  
		Last Modified: Wed, 01 Sep 2021 00:25:43 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.7.17`

```console
$ docker pull chronograf@sha256:4cd571df7045704646115f9d3e75f8f4d07a72c7fd6d209dbaddafb63aeebd92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.7.17` - linux; amd64

```console
$ docker pull chronograf@sha256:a0bd7f9a7a6f41e1bff144f6705cbd765ad16522cd5c79f6e550d680b404c6c9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.4 MB (65385969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ec19aa91c9ffb33b4a9a9682dbb6c75d3b197f70a15fdfc2dd0a4e088425d23`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 17 Aug 2021 01:26:09 GMT
ADD file:f6c4487fa1f7a4e17f5d88fd0c91031a6efc7fa210d363a1d43d8b0f3a8d1d03 in / 
# Tue, 17 Aug 2021 01:26:09 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 09:35:45 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 17 Aug 2021 09:35:46 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 17 Aug 2021 09:35:57 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 17 Aug 2021 09:35:57 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 17 Aug 2021 09:35:58 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 17 Aug 2021 09:35:58 GMT
EXPOSE 8888
# Tue, 17 Aug 2021 09:35:58 GMT
VOLUME [/var/lib/chronograf]
# Tue, 17 Aug 2021 09:35:58 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 17 Aug 2021 09:35:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Aug 2021 09:35:59 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:33f99cea3b7da8c6e0143c9fd7590c6d56f7d310ddd59b11be4ad485ae4cab2a`  
		Last Modified: Tue, 17 Aug 2021 01:33:27 GMT  
		Size: 22.5 MB (22527748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b30e58325c4aced5f8b1db67699808a32667aa9b4c6ce8f2bdfa2483c1fca5d`  
		Last Modified: Tue, 17 Aug 2021 09:37:14 GMT  
		Size: 4.5 MB (4506000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feaf4e133d20eb12180b56077702463f8b86964c0c436a6428ba22d49937aee9`  
		Last Modified: Tue, 17 Aug 2021 09:37:19 GMT  
		Size: 38.3 MB (38327828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9423787f4c740286bf12eb3babfa4d046ac80fe5a0df99011d36bc7157b5b58`  
		Last Modified: Tue, 17 Aug 2021 09:37:13 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:327bac57cd40f7913cf4c837b08e39f503a2a96d4d741b7357a346936be0c4c6`  
		Last Modified: Tue, 17 Aug 2021 09:37:13 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dc64a52a995cae676aef575882522843ca58890ae3dac6b44c5661dffcf7173`  
		Last Modified: Tue, 17 Aug 2021 09:37:13 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.7.17` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:8b3b18fc16ecc98e1bf91daaa69ba32719b5c6aea8f1816553ba941399eac678
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.0 MB (59002534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bcd89da09295d29aeddbf3b845afd96a58b115fbcb4aaeb3f1e9b4126500260`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 03 Sep 2021 01:05:16 GMT
ADD file:425f8ae3b1354b9858904edb027190b58b65692a710cb50a4d463ac554f853a6 in / 
# Fri, 03 Sep 2021 01:05:17 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 02:46:19 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 03 Sep 2021 02:46:19 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Fri, 03 Sep 2021 02:46:52 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Fri, 03 Sep 2021 02:46:53 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 03 Sep 2021 02:46:53 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 03 Sep 2021 02:46:54 GMT
EXPOSE 8888
# Fri, 03 Sep 2021 02:46:54 GMT
VOLUME [/var/lib/chronograf]
# Fri, 03 Sep 2021 02:46:55 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Fri, 03 Sep 2021 02:46:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 03 Sep 2021 02:46:56 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:0c15a1a8c9dffe5dfe059b37d14b92f1eb4ea47f16ae7bf66bf62f34a7510dd6`  
		Last Modified: Fri, 03 Sep 2021 01:22:37 GMT  
		Size: 19.3 MB (19316099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72feb6c10261bcd9f265aa351af235fc6d6eb3473fad71a9579edc13f7328fa2`  
		Last Modified: Fri, 03 Sep 2021 02:49:40 GMT  
		Size: 3.9 MB (3879487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ddcfdb344e67d03f1b7a9cd328a06cbeca291255d3be23eace2601350070fa8`  
		Last Modified: Fri, 03 Sep 2021 02:49:56 GMT  
		Size: 35.8 MB (35782561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:066675693109c82818a2b7cd4bd8a8e696b01141184fe0ee98354c45b0fbc140`  
		Last Modified: Fri, 03 Sep 2021 02:49:38 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c4e25e7194766392fd80eed393de68cd1e2fb01396ecb0a421dbb046e1fc947`  
		Last Modified: Fri, 03 Sep 2021 02:49:38 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7170ad340de1bfc4912904c7dedb7f2308b8593444f2c0503a68b16faffdfa7b`  
		Last Modified: Fri, 03 Sep 2021 02:49:38 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.7.17` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:784ae2f5b10603b07a9469b6f024c2381eadba945c359aa00ff63815d49d2f07
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.5 MB (60482129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:addf16420eaf0c8efe1c3d1b592739421caa793126f877f4e221875ed395af62`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 17 Aug 2021 01:48:32 GMT
ADD file:5cd26935234cc0540158a144066c0341b46a0caeb0a80db0355eeb8cfaf4fc0d in / 
# Tue, 17 Aug 2021 01:48:32 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 08:07:08 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 17 Aug 2021 08:07:08 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 17 Aug 2021 08:07:17 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 17 Aug 2021 08:07:18 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 17 Aug 2021 08:07:18 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 17 Aug 2021 08:07:18 GMT
EXPOSE 8888
# Tue, 17 Aug 2021 08:07:18 GMT
VOLUME [/var/lib/chronograf]
# Tue, 17 Aug 2021 08:07:18 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 17 Aug 2021 08:07:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Aug 2021 08:07:19 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:f862659192cd149f96ede75854bd3ebf59937831d3e4103087ae62df34ef1a29`  
		Last Modified: Tue, 17 Aug 2021 01:58:00 GMT  
		Size: 20.4 MB (20389447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a633450ca1e80832c0d9d386dc78f5a7b17e96988c46adfce9f7fb9df3080cc8`  
		Last Modified: Tue, 17 Aug 2021 08:08:33 GMT  
		Size: 4.1 MB (4082143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:369d3b51668baff5b0af480d4afb8749ee0292e2bc1cda07ffb54f639a9bbf11`  
		Last Modified: Tue, 17 Aug 2021 08:08:37 GMT  
		Size: 36.0 MB (35986144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc24a9d100c2c1bddd8eb913e91e3ae5f1a7c73e8022cd1d9662b40460015b81`  
		Last Modified: Tue, 17 Aug 2021 08:08:32 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d61d15ba426300c200c2f21e8a6d770db59bda2a4345a5f1f8e6c57b2b14215c`  
		Last Modified: Tue, 17 Aug 2021 08:08:32 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eedb0a234ee76ab5785a3e9e6a79e908e8c003c24ac020d6ce8cbafd93df9774`  
		Last Modified: Tue, 17 Aug 2021 08:08:32 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.7.17-alpine`

```console
$ docker pull chronograf@sha256:9b177c70e25de297b100d46ba7eb922ac167a8e65f698480e2785b1886cb94a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.7.17-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:c3a41e489e87268456b3ac8beea5f7c2a516dc7d43af6f7066be8b9675492d70
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22662384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a94fa13b711dbb3a88df7489d3353cc6e4777a37a87a0788d36cef2fdc64c95`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 31 Aug 2021 23:18:23 GMT
ADD file:e3d2013df9d58cd9255c749dbd62e7b1b1bdf1c2ee644c17bb93e67d859f0815 in / 
# Tue, 31 Aug 2021 23:18:24 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 00:23:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 01 Sep 2021 00:23:43 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Wed, 01 Sep 2021 00:24:02 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Wed, 01 Sep 2021 00:24:13 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 01 Sep 2021 00:24:14 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 01 Sep 2021 00:24:15 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 01 Sep 2021 00:24:15 GMT
EXPOSE 8888
# Wed, 01 Sep 2021 00:24:15 GMT
VOLUME [/var/lib/chronograf]
# Wed, 01 Sep 2021 00:24:16 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Wed, 01 Sep 2021 00:24:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Sep 2021 00:24:16 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:e519532ddf75bafbbb0ad01d3fb678ef9395cd8554fa25bef4695bb6e11f39f1`  
		Last Modified: Tue, 31 Aug 2021 23:19:05 GMT  
		Size: 2.8 MB (2801707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e69cd3502d3b453e253ea48e4ff56f5af4e25895a1bfa5e84cda59eaefce23be`  
		Last Modified: Wed, 01 Sep 2021 00:25:31 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7087df4b29e442773e368f72aa50cd7765fd6e6b43879c83880b0038e62b9077`  
		Last Modified: Wed, 01 Sep 2021 00:25:29 GMT  
		Size: 280.9 KB (280879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75a1ffa92682ef14beba92c11f3c21d02b50a70f56f234ab814e604f678b2b31`  
		Last Modified: Wed, 01 Sep 2021 00:25:49 GMT  
		Size: 19.6 MB (19555249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37dbb12c4afee159bb53c97f3d0cb65034efe2713363365b1f7f5f7affb916fe`  
		Last Modified: Wed, 01 Sep 2021 00:25:43 GMT  
		Size: 12.3 KB (12265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:344ba26fb8530e7520df76f60ae8b3f9e317561d15deea2b4738f5c3e4b47e11`  
		Last Modified: Wed, 01 Sep 2021 00:25:43 GMT  
		Size: 11.9 KB (11895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da9b8b115b6329338ab5fea52358a641fbb017ecd917613643e4cbce6b3f081f`  
		Last Modified: Wed, 01 Sep 2021 00:25:43 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.8`

```console
$ docker pull chronograf@sha256:1839c6f5fbd8cd0eb465b6892cd5b91c80bf0e930e0ddd80927198fc67aef7b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.8` - linux; amd64

```console
$ docker pull chronograf@sha256:02e7e7e461fefbdc8d151d4775b08f62e9eca611e1bc888f83a4c5a8730561d5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66238411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f735df9bd93956f4544c105a5ca505c769d1ee260ad75591e8661f64394155b6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 17 Aug 2021 01:26:09 GMT
ADD file:f6c4487fa1f7a4e17f5d88fd0c91031a6efc7fa210d363a1d43d8b0f3a8d1d03 in / 
# Tue, 17 Aug 2021 01:26:09 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 09:35:17 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 17 Aug 2021 09:36:05 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Tue, 17 Aug 2021 09:36:12 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 17 Aug 2021 09:36:13 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 17 Aug 2021 09:36:13 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 17 Aug 2021 09:36:13 GMT
EXPOSE 8888
# Tue, 17 Aug 2021 09:36:13 GMT
VOLUME [/var/lib/chronograf]
# Tue, 17 Aug 2021 09:36:14 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 17 Aug 2021 09:36:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Aug 2021 09:36:14 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:33f99cea3b7da8c6e0143c9fd7590c6d56f7d310ddd59b11be4ad485ae4cab2a`  
		Last Modified: Tue, 17 Aug 2021 01:33:27 GMT  
		Size: 22.5 MB (22527748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6ebf00cee8edb2723f73bb596dc02dac400fcd609c6288b968066e0333dc5cd`  
		Last Modified: Tue, 17 Aug 2021 09:37:00 GMT  
		Size: 6.8 MB (6760152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5d733329bb98a3c70530f4e78fbc26f2e104088f96861464937e43bf83cf5bc`  
		Last Modified: Tue, 17 Aug 2021 09:37:35 GMT  
		Size: 36.9 MB (36926121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a6075bbba535a693eaae2e807d6035e58abde36009d60e74a72b3d4245bd92b`  
		Last Modified: Tue, 17 Aug 2021 09:37:30 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b744d95d8178283c366bf94fd33fbb9f2afdf33f607a43b5a44514b57b60f35d`  
		Last Modified: Tue, 17 Aug 2021 09:37:30 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e49d310da5a1e0d6daac1fdcc68637b2efd0e73f879b8b1fad67dec4eac99591`  
		Last Modified: Tue, 17 Aug 2021 09:37:30 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.8` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:68f4eea3e9539c8bb88a29f1a805b2ba18bc9e7c78d75549abc0c2ea1471f5a8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.6 MB (59630013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bde18e3cc4aea138619ed10c2da36aca91ec660823f6310027e0fdcd0e8b155`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 03 Sep 2021 01:05:16 GMT
ADD file:425f8ae3b1354b9858904edb027190b58b65692a710cb50a4d463ac554f853a6 in / 
# Fri, 03 Sep 2021 01:05:17 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 02:45:29 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 03 Sep 2021 02:47:10 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Fri, 03 Sep 2021 02:47:30 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Fri, 03 Sep 2021 02:47:31 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 03 Sep 2021 02:47:32 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 03 Sep 2021 02:47:32 GMT
EXPOSE 8888
# Fri, 03 Sep 2021 02:47:33 GMT
VOLUME [/var/lib/chronograf]
# Fri, 03 Sep 2021 02:47:34 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Fri, 03 Sep 2021 02:47:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 03 Sep 2021 02:47:35 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:0c15a1a8c9dffe5dfe059b37d14b92f1eb4ea47f16ae7bf66bf62f34a7510dd6`  
		Last Modified: Fri, 03 Sep 2021 01:22:37 GMT  
		Size: 19.3 MB (19316099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb41f6e44cc2adc7b1da1ef11c2a061b83d79ad3aec2895b90e80a08e2eeb1be`  
		Last Modified: Fri, 03 Sep 2021 02:49:09 GMT  
		Size: 5.8 MB (5779569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dad6b722e467f0d32ff6afcf74dd4ef6cdc90463d5e905ce2af68184bc1d88d4`  
		Last Modified: Fri, 03 Sep 2021 02:50:27 GMT  
		Size: 34.5 MB (34509957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e7d7c2fb7650aa3c5cd510ca927a393170e7e92b4272f51ad20a5e068655534`  
		Last Modified: Fri, 03 Sep 2021 02:50:09 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1606dfd7c0e45badcae83cbb33a057aa34259593d16c77a0547f91bd6ff1f7d`  
		Last Modified: Fri, 03 Sep 2021 02:50:09 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfece565b9d738d7e39eea024c0ee291784e9bf6cd4211dd0a6ffb1dbf3c4455`  
		Last Modified: Fri, 03 Sep 2021 02:50:09 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.8` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:50bb95ad8e75c72c6c78f2adc41fa1e4e65c9ce606149939014765140436b714
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60893485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ab2558c75bff2c996f9ab8ade4d2b02c8527c43f5217aaec182a7c2ef4bc3a4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 17 Aug 2021 01:48:32 GMT
ADD file:5cd26935234cc0540158a144066c0341b46a0caeb0a80db0355eeb8cfaf4fc0d in / 
# Tue, 17 Aug 2021 01:48:32 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 08:06:44 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 17 Aug 2021 08:07:26 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Tue, 17 Aug 2021 08:07:34 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 17 Aug 2021 08:07:34 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 17 Aug 2021 08:07:34 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 17 Aug 2021 08:07:34 GMT
EXPOSE 8888
# Tue, 17 Aug 2021 08:07:35 GMT
VOLUME [/var/lib/chronograf]
# Tue, 17 Aug 2021 08:07:35 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 17 Aug 2021 08:07:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Aug 2021 08:07:35 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:f862659192cd149f96ede75854bd3ebf59937831d3e4103087ae62df34ef1a29`  
		Last Modified: Tue, 17 Aug 2021 01:58:00 GMT  
		Size: 20.4 MB (20389447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09101c696c7496dfd097387796cbe96c76aa138b186200c5879c0ab29f5a13f4`  
		Last Modified: Tue, 17 Aug 2021 08:08:19 GMT  
		Size: 6.0 MB (6047480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dde8e33fe3c76bb15079dbf979e7a62649160f833f7b79c87e509274572b830`  
		Last Modified: Tue, 17 Aug 2021 08:08:54 GMT  
		Size: 34.4 MB (34432168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61d5bfc7c7d8d7f65b1f51b16ceaecf855e71888a5698056ab8ec5637c6840df`  
		Last Modified: Tue, 17 Aug 2021 08:08:49 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5940fd5898023978d247df91489e6acb6c1faa54e057c808855af070b0ee5eb`  
		Last Modified: Tue, 17 Aug 2021 08:08:49 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ed27ffdb1a1c2b0057c08793346e56e346582bc736e47db7707e2eb7c3c1846`  
		Last Modified: Tue, 17 Aug 2021 08:08:49 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.8-alpine`

```console
$ docker pull chronograf@sha256:30f63fa8f9214eb152af97cd85908e510c913d81f80a49b9c232ea42c281b9d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.8-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:7c4dd500f22766f0a514d9a2d1d13c944e2aaeb5be7f2be304ae8ef21ec9bead
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.3 MB (22311020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:419075de283e08462528ab9737dd9a32b8e4150dc96635bda486afb9571f2905`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 31 Aug 2021 23:18:23 GMT
ADD file:e3d2013df9d58cd9255c749dbd62e7b1b1bdf1c2ee644c17bb93e67d859f0815 in / 
# Tue, 31 Aug 2021 23:18:24 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 00:23:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 01 Sep 2021 00:23:43 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Wed, 01 Sep 2021 00:24:24 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Wed, 01 Sep 2021 00:24:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 01 Sep 2021 00:24:31 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 01 Sep 2021 00:24:32 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 01 Sep 2021 00:24:32 GMT
EXPOSE 8888
# Wed, 01 Sep 2021 00:24:33 GMT
VOLUME [/var/lib/chronograf]
# Wed, 01 Sep 2021 00:24:33 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Wed, 01 Sep 2021 00:24:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Sep 2021 00:24:34 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:e519532ddf75bafbbb0ad01d3fb678ef9395cd8554fa25bef4695bb6e11f39f1`  
		Last Modified: Tue, 31 Aug 2021 23:19:05 GMT  
		Size: 2.8 MB (2801707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e69cd3502d3b453e253ea48e4ff56f5af4e25895a1bfa5e84cda59eaefce23be`  
		Last Modified: Wed, 01 Sep 2021 00:25:31 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7087df4b29e442773e368f72aa50cd7765fd6e6b43879c83880b0038e62b9077`  
		Last Modified: Wed, 01 Sep 2021 00:25:29 GMT  
		Size: 280.9 KB (280879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9dd2619092db5ca6cb874052a71c03376efbdde1ef7f45ffd85cfa8282b9fd`  
		Last Modified: Wed, 01 Sep 2021 00:26:04 GMT  
		Size: 19.2 MB (19203889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e799830d16117d477b1f2c4fa56db3520d04b1100e2330e4e4f5458ff89e0968`  
		Last Modified: Wed, 01 Sep 2021 00:26:00 GMT  
		Size: 12.3 KB (12259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c610504f400b831a31045e828f0250e107de5ad4786642d241b0b70d2e5f744`  
		Last Modified: Wed, 01 Sep 2021 00:26:00 GMT  
		Size: 11.9 KB (11896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:996e4d82939f361d8f0003173b864e68be9fe64e83e3f4cabba3aafe8ef39f01`  
		Last Modified: Wed, 01 Sep 2021 00:26:00 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.8.10`

```console
$ docker pull chronograf@sha256:1839c6f5fbd8cd0eb465b6892cd5b91c80bf0e930e0ddd80927198fc67aef7b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.8.10` - linux; amd64

```console
$ docker pull chronograf@sha256:02e7e7e461fefbdc8d151d4775b08f62e9eca611e1bc888f83a4c5a8730561d5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66238411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f735df9bd93956f4544c105a5ca505c769d1ee260ad75591e8661f64394155b6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 17 Aug 2021 01:26:09 GMT
ADD file:f6c4487fa1f7a4e17f5d88fd0c91031a6efc7fa210d363a1d43d8b0f3a8d1d03 in / 
# Tue, 17 Aug 2021 01:26:09 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 09:35:17 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 17 Aug 2021 09:36:05 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Tue, 17 Aug 2021 09:36:12 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 17 Aug 2021 09:36:13 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 17 Aug 2021 09:36:13 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 17 Aug 2021 09:36:13 GMT
EXPOSE 8888
# Tue, 17 Aug 2021 09:36:13 GMT
VOLUME [/var/lib/chronograf]
# Tue, 17 Aug 2021 09:36:14 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 17 Aug 2021 09:36:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Aug 2021 09:36:14 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:33f99cea3b7da8c6e0143c9fd7590c6d56f7d310ddd59b11be4ad485ae4cab2a`  
		Last Modified: Tue, 17 Aug 2021 01:33:27 GMT  
		Size: 22.5 MB (22527748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6ebf00cee8edb2723f73bb596dc02dac400fcd609c6288b968066e0333dc5cd`  
		Last Modified: Tue, 17 Aug 2021 09:37:00 GMT  
		Size: 6.8 MB (6760152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5d733329bb98a3c70530f4e78fbc26f2e104088f96861464937e43bf83cf5bc`  
		Last Modified: Tue, 17 Aug 2021 09:37:35 GMT  
		Size: 36.9 MB (36926121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a6075bbba535a693eaae2e807d6035e58abde36009d60e74a72b3d4245bd92b`  
		Last Modified: Tue, 17 Aug 2021 09:37:30 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b744d95d8178283c366bf94fd33fbb9f2afdf33f607a43b5a44514b57b60f35d`  
		Last Modified: Tue, 17 Aug 2021 09:37:30 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e49d310da5a1e0d6daac1fdcc68637b2efd0e73f879b8b1fad67dec4eac99591`  
		Last Modified: Tue, 17 Aug 2021 09:37:30 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.8.10` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:68f4eea3e9539c8bb88a29f1a805b2ba18bc9e7c78d75549abc0c2ea1471f5a8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.6 MB (59630013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bde18e3cc4aea138619ed10c2da36aca91ec660823f6310027e0fdcd0e8b155`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 03 Sep 2021 01:05:16 GMT
ADD file:425f8ae3b1354b9858904edb027190b58b65692a710cb50a4d463ac554f853a6 in / 
# Fri, 03 Sep 2021 01:05:17 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 02:45:29 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 03 Sep 2021 02:47:10 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Fri, 03 Sep 2021 02:47:30 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Fri, 03 Sep 2021 02:47:31 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 03 Sep 2021 02:47:32 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 03 Sep 2021 02:47:32 GMT
EXPOSE 8888
# Fri, 03 Sep 2021 02:47:33 GMT
VOLUME [/var/lib/chronograf]
# Fri, 03 Sep 2021 02:47:34 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Fri, 03 Sep 2021 02:47:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 03 Sep 2021 02:47:35 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:0c15a1a8c9dffe5dfe059b37d14b92f1eb4ea47f16ae7bf66bf62f34a7510dd6`  
		Last Modified: Fri, 03 Sep 2021 01:22:37 GMT  
		Size: 19.3 MB (19316099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb41f6e44cc2adc7b1da1ef11c2a061b83d79ad3aec2895b90e80a08e2eeb1be`  
		Last Modified: Fri, 03 Sep 2021 02:49:09 GMT  
		Size: 5.8 MB (5779569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dad6b722e467f0d32ff6afcf74dd4ef6cdc90463d5e905ce2af68184bc1d88d4`  
		Last Modified: Fri, 03 Sep 2021 02:50:27 GMT  
		Size: 34.5 MB (34509957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e7d7c2fb7650aa3c5cd510ca927a393170e7e92b4272f51ad20a5e068655534`  
		Last Modified: Fri, 03 Sep 2021 02:50:09 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1606dfd7c0e45badcae83cbb33a057aa34259593d16c77a0547f91bd6ff1f7d`  
		Last Modified: Fri, 03 Sep 2021 02:50:09 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfece565b9d738d7e39eea024c0ee291784e9bf6cd4211dd0a6ffb1dbf3c4455`  
		Last Modified: Fri, 03 Sep 2021 02:50:09 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.8.10` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:50bb95ad8e75c72c6c78f2adc41fa1e4e65c9ce606149939014765140436b714
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60893485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ab2558c75bff2c996f9ab8ade4d2b02c8527c43f5217aaec182a7c2ef4bc3a4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 17 Aug 2021 01:48:32 GMT
ADD file:5cd26935234cc0540158a144066c0341b46a0caeb0a80db0355eeb8cfaf4fc0d in / 
# Tue, 17 Aug 2021 01:48:32 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 08:06:44 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 17 Aug 2021 08:07:26 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Tue, 17 Aug 2021 08:07:34 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 17 Aug 2021 08:07:34 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 17 Aug 2021 08:07:34 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 17 Aug 2021 08:07:34 GMT
EXPOSE 8888
# Tue, 17 Aug 2021 08:07:35 GMT
VOLUME [/var/lib/chronograf]
# Tue, 17 Aug 2021 08:07:35 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 17 Aug 2021 08:07:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Aug 2021 08:07:35 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:f862659192cd149f96ede75854bd3ebf59937831d3e4103087ae62df34ef1a29`  
		Last Modified: Tue, 17 Aug 2021 01:58:00 GMT  
		Size: 20.4 MB (20389447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09101c696c7496dfd097387796cbe96c76aa138b186200c5879c0ab29f5a13f4`  
		Last Modified: Tue, 17 Aug 2021 08:08:19 GMT  
		Size: 6.0 MB (6047480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dde8e33fe3c76bb15079dbf979e7a62649160f833f7b79c87e509274572b830`  
		Last Modified: Tue, 17 Aug 2021 08:08:54 GMT  
		Size: 34.4 MB (34432168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61d5bfc7c7d8d7f65b1f51b16ceaecf855e71888a5698056ab8ec5637c6840df`  
		Last Modified: Tue, 17 Aug 2021 08:08:49 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5940fd5898023978d247df91489e6acb6c1faa54e057c808855af070b0ee5eb`  
		Last Modified: Tue, 17 Aug 2021 08:08:49 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ed27ffdb1a1c2b0057c08793346e56e346582bc736e47db7707e2eb7c3c1846`  
		Last Modified: Tue, 17 Aug 2021 08:08:49 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.8.10-alpine`

```console
$ docker pull chronograf@sha256:30f63fa8f9214eb152af97cd85908e510c913d81f80a49b9c232ea42c281b9d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.8.10-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:7c4dd500f22766f0a514d9a2d1d13c944e2aaeb5be7f2be304ae8ef21ec9bead
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.3 MB (22311020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:419075de283e08462528ab9737dd9a32b8e4150dc96635bda486afb9571f2905`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 31 Aug 2021 23:18:23 GMT
ADD file:e3d2013df9d58cd9255c749dbd62e7b1b1bdf1c2ee644c17bb93e67d859f0815 in / 
# Tue, 31 Aug 2021 23:18:24 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 00:23:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 01 Sep 2021 00:23:43 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Wed, 01 Sep 2021 00:24:24 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Wed, 01 Sep 2021 00:24:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 01 Sep 2021 00:24:31 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 01 Sep 2021 00:24:32 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 01 Sep 2021 00:24:32 GMT
EXPOSE 8888
# Wed, 01 Sep 2021 00:24:33 GMT
VOLUME [/var/lib/chronograf]
# Wed, 01 Sep 2021 00:24:33 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Wed, 01 Sep 2021 00:24:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Sep 2021 00:24:34 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:e519532ddf75bafbbb0ad01d3fb678ef9395cd8554fa25bef4695bb6e11f39f1`  
		Last Modified: Tue, 31 Aug 2021 23:19:05 GMT  
		Size: 2.8 MB (2801707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e69cd3502d3b453e253ea48e4ff56f5af4e25895a1bfa5e84cda59eaefce23be`  
		Last Modified: Wed, 01 Sep 2021 00:25:31 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7087df4b29e442773e368f72aa50cd7765fd6e6b43879c83880b0038e62b9077`  
		Last Modified: Wed, 01 Sep 2021 00:25:29 GMT  
		Size: 280.9 KB (280879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9dd2619092db5ca6cb874052a71c03376efbdde1ef7f45ffd85cfa8282b9fd`  
		Last Modified: Wed, 01 Sep 2021 00:26:04 GMT  
		Size: 19.2 MB (19203889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e799830d16117d477b1f2c4fa56db3520d04b1100e2330e4e4f5458ff89e0968`  
		Last Modified: Wed, 01 Sep 2021 00:26:00 GMT  
		Size: 12.3 KB (12259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c610504f400b831a31045e828f0250e107de5ad4786642d241b0b70d2e5f744`  
		Last Modified: Wed, 01 Sep 2021 00:26:00 GMT  
		Size: 11.9 KB (11896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:996e4d82939f361d8f0003173b864e68be9fe64e83e3f4cabba3aafe8ef39f01`  
		Last Modified: Wed, 01 Sep 2021 00:26:00 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.9`

```console
$ docker pull chronograf@sha256:5efd920a71d94d1451451728a87976024944d9a6424de3bf6538b66fa56df107
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.9` - linux; amd64

```console
$ docker pull chronograf@sha256:d30b8a1f515a1f68ac7675f55026ef00b5c9510dde3c84e552ceafbd8da84fd5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.8 MB (66757353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:071d9a46cb06f25d04e299d93f99d10334cd8b43d697b016191c1f87004f0c27`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 17 Aug 2021 01:26:09 GMT
ADD file:f6c4487fa1f7a4e17f5d88fd0c91031a6efc7fa210d363a1d43d8b0f3a8d1d03 in / 
# Tue, 17 Aug 2021 01:26:09 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 09:35:17 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 17 Aug 2021 09:36:21 GMT
ENV CHRONOGRAF_VERSION=1.9.0
# Tue, 17 Aug 2021 09:36:30 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 17 Aug 2021 09:36:30 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 17 Aug 2021 09:36:30 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 17 Aug 2021 09:36:31 GMT
EXPOSE 8888
# Tue, 17 Aug 2021 09:36:31 GMT
VOLUME [/var/lib/chronograf]
# Tue, 17 Aug 2021 09:36:31 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 17 Aug 2021 09:36:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Aug 2021 09:36:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:33f99cea3b7da8c6e0143c9fd7590c6d56f7d310ddd59b11be4ad485ae4cab2a`  
		Last Modified: Tue, 17 Aug 2021 01:33:27 GMT  
		Size: 22.5 MB (22527748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6ebf00cee8edb2723f73bb596dc02dac400fcd609c6288b968066e0333dc5cd`  
		Last Modified: Tue, 17 Aug 2021 09:37:00 GMT  
		Size: 6.8 MB (6760152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f88d589540170378ab6422d641b642a6aa1e3fd063d84997f3d21de4c5f78981`  
		Last Modified: Tue, 17 Aug 2021 09:37:53 GMT  
		Size: 37.4 MB (37445059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e800a265cf9be534a8fe5b59b309a201c2663c6741f7c25aa4227364f32b4ba5`  
		Last Modified: Tue, 17 Aug 2021 09:37:46 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ab0427bfc914c791fecbe16f14d108518b4438951f2dd347355fabc74377f53`  
		Last Modified: Tue, 17 Aug 2021 09:37:47 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ded1c3ae33fb215a5bba57e059b94f9659e7950e44b102640e396f3bf7c72b01`  
		Last Modified: Tue, 17 Aug 2021 09:37:46 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.9` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:609775e3045917416f254d596222e113bebabf264680c6289ed7bb84e1aa0439
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60284183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b52137975532be06a48c3ceeedbf2bbd2b4f12a58bc040cdc385b36cc3204c55`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 03 Sep 2021 01:05:16 GMT
ADD file:425f8ae3b1354b9858904edb027190b58b65692a710cb50a4d463ac554f853a6 in / 
# Fri, 03 Sep 2021 01:05:17 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 02:45:29 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 03 Sep 2021 02:47:46 GMT
ENV CHRONOGRAF_VERSION=1.9.0
# Fri, 03 Sep 2021 02:48:06 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Fri, 03 Sep 2021 02:48:07 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 03 Sep 2021 02:48:07 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 03 Sep 2021 02:48:08 GMT
EXPOSE 8888
# Fri, 03 Sep 2021 02:48:08 GMT
VOLUME [/var/lib/chronograf]
# Fri, 03 Sep 2021 02:48:09 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Fri, 03 Sep 2021 02:48:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 03 Sep 2021 02:48:10 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:0c15a1a8c9dffe5dfe059b37d14b92f1eb4ea47f16ae7bf66bf62f34a7510dd6`  
		Last Modified: Fri, 03 Sep 2021 01:22:37 GMT  
		Size: 19.3 MB (19316099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb41f6e44cc2adc7b1da1ef11c2a061b83d79ad3aec2895b90e80a08e2eeb1be`  
		Last Modified: Fri, 03 Sep 2021 02:49:09 GMT  
		Size: 5.8 MB (5779569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2a8e857ff2824613b74370561a6f3ed4cf43acb1c72b8ec0604c75892f459cb`  
		Last Modified: Fri, 03 Sep 2021 02:50:58 GMT  
		Size: 35.2 MB (35164135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:736406488d5a7638a24ee9cf3f2cdefca5302b6c28f12d1ef089bd41c153f2a2`  
		Last Modified: Fri, 03 Sep 2021 02:50:40 GMT  
		Size: 12.2 KB (12241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a9b3a3fb52efb0b155e1a83b168f969aab6e53eb9a512ed6c6d16150b6d5bbc`  
		Last Modified: Fri, 03 Sep 2021 02:50:40 GMT  
		Size: 11.9 KB (11900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7af17a3f630e3db6735c25b8a73919284e41ae7925693423395adcd53097c8b7`  
		Last Modified: Fri, 03 Sep 2021 02:50:40 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.9` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:b2ebe33396b3deb42dbdc543bc92331a8a242813e8705f7d9cc0bbd5a84a048d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61522879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1378f77cfd03e8e67afd75650a3fbc1ac23364337d73d700d99a7d4693d19887`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 17 Aug 2021 01:48:32 GMT
ADD file:5cd26935234cc0540158a144066c0341b46a0caeb0a80db0355eeb8cfaf4fc0d in / 
# Tue, 17 Aug 2021 01:48:32 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 08:06:44 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 17 Aug 2021 08:07:40 GMT
ENV CHRONOGRAF_VERSION=1.9.0
# Tue, 17 Aug 2021 08:07:48 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 17 Aug 2021 08:07:49 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 17 Aug 2021 08:07:49 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 17 Aug 2021 08:07:49 GMT
EXPOSE 8888
# Tue, 17 Aug 2021 08:07:49 GMT
VOLUME [/var/lib/chronograf]
# Tue, 17 Aug 2021 08:07:49 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 17 Aug 2021 08:07:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Aug 2021 08:07:50 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:f862659192cd149f96ede75854bd3ebf59937831d3e4103087ae62df34ef1a29`  
		Last Modified: Tue, 17 Aug 2021 01:58:00 GMT  
		Size: 20.4 MB (20389447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09101c696c7496dfd097387796cbe96c76aa138b186200c5879c0ab29f5a13f4`  
		Last Modified: Tue, 17 Aug 2021 08:08:19 GMT  
		Size: 6.0 MB (6047480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:460f0536e20a65b2904cd15722337b7302f9c0dab6e10fb222940f49a6075215`  
		Last Modified: Tue, 17 Aug 2021 08:09:10 GMT  
		Size: 35.1 MB (35061557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:010e9e427ef0ba79f667341edbabc8feb479b8c29c1c343bfc81e25b644480fb`  
		Last Modified: Tue, 17 Aug 2021 08:09:05 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ee27ad129e4bae5379fe5fe8edc5931a22031014148bc4d5b24e6e6c56421a`  
		Last Modified: Tue, 17 Aug 2021 08:09:05 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fed64ace818385e3d03fa5b6dc95f4092a80eb5838be8fef6a05f07dd5162c74`  
		Last Modified: Tue, 17 Aug 2021 08:09:05 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.9-alpine`

```console
$ docker pull chronograf@sha256:bdb38dbf0d72892a4685b69391c89a1716a2465b0d52f79bd859a846f982c702
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.9-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:44ddcc13955fcee6ada98e17e24ee8f695a9823b3c3e999e5d315c9a3bb0aa8e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22689227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f86636178ef7f0961c639954f1607c343f7ed49e2749304818d81e8d9aaec58`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 31 Aug 2021 23:18:23 GMT
ADD file:e3d2013df9d58cd9255c749dbd62e7b1b1bdf1c2ee644c17bb93e67d859f0815 in / 
# Tue, 31 Aug 2021 23:18:24 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 00:23:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 01 Sep 2021 00:23:43 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Wed, 01 Sep 2021 00:24:42 GMT
ENV CHRONOGRAF_VERSION=1.9.0
# Wed, 01 Sep 2021 00:24:48 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 01 Sep 2021 00:24:49 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 01 Sep 2021 00:24:49 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 01 Sep 2021 00:24:50 GMT
EXPOSE 8888
# Wed, 01 Sep 2021 00:24:50 GMT
VOLUME [/var/lib/chronograf]
# Wed, 01 Sep 2021 00:24:51 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Wed, 01 Sep 2021 00:24:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Sep 2021 00:24:51 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:e519532ddf75bafbbb0ad01d3fb678ef9395cd8554fa25bef4695bb6e11f39f1`  
		Last Modified: Tue, 31 Aug 2021 23:19:05 GMT  
		Size: 2.8 MB (2801707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e69cd3502d3b453e253ea48e4ff56f5af4e25895a1bfa5e84cda59eaefce23be`  
		Last Modified: Wed, 01 Sep 2021 00:25:31 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7087df4b29e442773e368f72aa50cd7765fd6e6b43879c83880b0038e62b9077`  
		Last Modified: Wed, 01 Sep 2021 00:25:29 GMT  
		Size: 280.9 KB (280879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0062288c23918a5c405390da5fe197e453d3162f22d5e04c4e80c771bfb7dbb`  
		Last Modified: Wed, 01 Sep 2021 00:26:19 GMT  
		Size: 19.6 MB (19582082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a56af5fa9abf70534bf74916985c59602805aaec20e843a8fb80451dc2b4aa6b`  
		Last Modified: Wed, 01 Sep 2021 00:26:15 GMT  
		Size: 12.3 KB (12269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bad79cf9294c71cb171d84b1b435766c73b488c2eaf98668e8fb24c098ec8e0`  
		Last Modified: Wed, 01 Sep 2021 00:26:15 GMT  
		Size: 11.9 KB (11901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80584912177323f577d098fda53486bc0f440c26efb41dd2951ee13af7a0f369`  
		Last Modified: Wed, 01 Sep 2021 00:26:15 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.9.0`

```console
$ docker pull chronograf@sha256:5efd920a71d94d1451451728a87976024944d9a6424de3bf6538b66fa56df107
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.9.0` - linux; amd64

```console
$ docker pull chronograf@sha256:d30b8a1f515a1f68ac7675f55026ef00b5c9510dde3c84e552ceafbd8da84fd5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.8 MB (66757353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:071d9a46cb06f25d04e299d93f99d10334cd8b43d697b016191c1f87004f0c27`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 17 Aug 2021 01:26:09 GMT
ADD file:f6c4487fa1f7a4e17f5d88fd0c91031a6efc7fa210d363a1d43d8b0f3a8d1d03 in / 
# Tue, 17 Aug 2021 01:26:09 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 09:35:17 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 17 Aug 2021 09:36:21 GMT
ENV CHRONOGRAF_VERSION=1.9.0
# Tue, 17 Aug 2021 09:36:30 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 17 Aug 2021 09:36:30 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 17 Aug 2021 09:36:30 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 17 Aug 2021 09:36:31 GMT
EXPOSE 8888
# Tue, 17 Aug 2021 09:36:31 GMT
VOLUME [/var/lib/chronograf]
# Tue, 17 Aug 2021 09:36:31 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 17 Aug 2021 09:36:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Aug 2021 09:36:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:33f99cea3b7da8c6e0143c9fd7590c6d56f7d310ddd59b11be4ad485ae4cab2a`  
		Last Modified: Tue, 17 Aug 2021 01:33:27 GMT  
		Size: 22.5 MB (22527748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6ebf00cee8edb2723f73bb596dc02dac400fcd609c6288b968066e0333dc5cd`  
		Last Modified: Tue, 17 Aug 2021 09:37:00 GMT  
		Size: 6.8 MB (6760152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f88d589540170378ab6422d641b642a6aa1e3fd063d84997f3d21de4c5f78981`  
		Last Modified: Tue, 17 Aug 2021 09:37:53 GMT  
		Size: 37.4 MB (37445059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e800a265cf9be534a8fe5b59b309a201c2663c6741f7c25aa4227364f32b4ba5`  
		Last Modified: Tue, 17 Aug 2021 09:37:46 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ab0427bfc914c791fecbe16f14d108518b4438951f2dd347355fabc74377f53`  
		Last Modified: Tue, 17 Aug 2021 09:37:47 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ded1c3ae33fb215a5bba57e059b94f9659e7950e44b102640e396f3bf7c72b01`  
		Last Modified: Tue, 17 Aug 2021 09:37:46 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.9.0` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:609775e3045917416f254d596222e113bebabf264680c6289ed7bb84e1aa0439
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60284183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b52137975532be06a48c3ceeedbf2bbd2b4f12a58bc040cdc385b36cc3204c55`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 03 Sep 2021 01:05:16 GMT
ADD file:425f8ae3b1354b9858904edb027190b58b65692a710cb50a4d463ac554f853a6 in / 
# Fri, 03 Sep 2021 01:05:17 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 02:45:29 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 03 Sep 2021 02:47:46 GMT
ENV CHRONOGRAF_VERSION=1.9.0
# Fri, 03 Sep 2021 02:48:06 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Fri, 03 Sep 2021 02:48:07 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 03 Sep 2021 02:48:07 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 03 Sep 2021 02:48:08 GMT
EXPOSE 8888
# Fri, 03 Sep 2021 02:48:08 GMT
VOLUME [/var/lib/chronograf]
# Fri, 03 Sep 2021 02:48:09 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Fri, 03 Sep 2021 02:48:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 03 Sep 2021 02:48:10 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:0c15a1a8c9dffe5dfe059b37d14b92f1eb4ea47f16ae7bf66bf62f34a7510dd6`  
		Last Modified: Fri, 03 Sep 2021 01:22:37 GMT  
		Size: 19.3 MB (19316099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb41f6e44cc2adc7b1da1ef11c2a061b83d79ad3aec2895b90e80a08e2eeb1be`  
		Last Modified: Fri, 03 Sep 2021 02:49:09 GMT  
		Size: 5.8 MB (5779569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2a8e857ff2824613b74370561a6f3ed4cf43acb1c72b8ec0604c75892f459cb`  
		Last Modified: Fri, 03 Sep 2021 02:50:58 GMT  
		Size: 35.2 MB (35164135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:736406488d5a7638a24ee9cf3f2cdefca5302b6c28f12d1ef089bd41c153f2a2`  
		Last Modified: Fri, 03 Sep 2021 02:50:40 GMT  
		Size: 12.2 KB (12241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a9b3a3fb52efb0b155e1a83b168f969aab6e53eb9a512ed6c6d16150b6d5bbc`  
		Last Modified: Fri, 03 Sep 2021 02:50:40 GMT  
		Size: 11.9 KB (11900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7af17a3f630e3db6735c25b8a73919284e41ae7925693423395adcd53097c8b7`  
		Last Modified: Fri, 03 Sep 2021 02:50:40 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.9.0` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:b2ebe33396b3deb42dbdc543bc92331a8a242813e8705f7d9cc0bbd5a84a048d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61522879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1378f77cfd03e8e67afd75650a3fbc1ac23364337d73d700d99a7d4693d19887`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 17 Aug 2021 01:48:32 GMT
ADD file:5cd26935234cc0540158a144066c0341b46a0caeb0a80db0355eeb8cfaf4fc0d in / 
# Tue, 17 Aug 2021 01:48:32 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 08:06:44 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 17 Aug 2021 08:07:40 GMT
ENV CHRONOGRAF_VERSION=1.9.0
# Tue, 17 Aug 2021 08:07:48 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 17 Aug 2021 08:07:49 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 17 Aug 2021 08:07:49 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 17 Aug 2021 08:07:49 GMT
EXPOSE 8888
# Tue, 17 Aug 2021 08:07:49 GMT
VOLUME [/var/lib/chronograf]
# Tue, 17 Aug 2021 08:07:49 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 17 Aug 2021 08:07:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Aug 2021 08:07:50 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:f862659192cd149f96ede75854bd3ebf59937831d3e4103087ae62df34ef1a29`  
		Last Modified: Tue, 17 Aug 2021 01:58:00 GMT  
		Size: 20.4 MB (20389447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09101c696c7496dfd097387796cbe96c76aa138b186200c5879c0ab29f5a13f4`  
		Last Modified: Tue, 17 Aug 2021 08:08:19 GMT  
		Size: 6.0 MB (6047480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:460f0536e20a65b2904cd15722337b7302f9c0dab6e10fb222940f49a6075215`  
		Last Modified: Tue, 17 Aug 2021 08:09:10 GMT  
		Size: 35.1 MB (35061557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:010e9e427ef0ba79f667341edbabc8feb479b8c29c1c343bfc81e25b644480fb`  
		Last Modified: Tue, 17 Aug 2021 08:09:05 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ee27ad129e4bae5379fe5fe8edc5931a22031014148bc4d5b24e6e6c56421a`  
		Last Modified: Tue, 17 Aug 2021 08:09:05 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fed64ace818385e3d03fa5b6dc95f4092a80eb5838be8fef6a05f07dd5162c74`  
		Last Modified: Tue, 17 Aug 2021 08:09:05 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.9.0-alpine`

```console
$ docker pull chronograf@sha256:bdb38dbf0d72892a4685b69391c89a1716a2465b0d52f79bd859a846f982c702
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.9.0-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:44ddcc13955fcee6ada98e17e24ee8f695a9823b3c3e999e5d315c9a3bb0aa8e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22689227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f86636178ef7f0961c639954f1607c343f7ed49e2749304818d81e8d9aaec58`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 31 Aug 2021 23:18:23 GMT
ADD file:e3d2013df9d58cd9255c749dbd62e7b1b1bdf1c2ee644c17bb93e67d859f0815 in / 
# Tue, 31 Aug 2021 23:18:24 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 00:23:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 01 Sep 2021 00:23:43 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Wed, 01 Sep 2021 00:24:42 GMT
ENV CHRONOGRAF_VERSION=1.9.0
# Wed, 01 Sep 2021 00:24:48 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 01 Sep 2021 00:24:49 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 01 Sep 2021 00:24:49 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 01 Sep 2021 00:24:50 GMT
EXPOSE 8888
# Wed, 01 Sep 2021 00:24:50 GMT
VOLUME [/var/lib/chronograf]
# Wed, 01 Sep 2021 00:24:51 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Wed, 01 Sep 2021 00:24:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Sep 2021 00:24:51 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:e519532ddf75bafbbb0ad01d3fb678ef9395cd8554fa25bef4695bb6e11f39f1`  
		Last Modified: Tue, 31 Aug 2021 23:19:05 GMT  
		Size: 2.8 MB (2801707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e69cd3502d3b453e253ea48e4ff56f5af4e25895a1bfa5e84cda59eaefce23be`  
		Last Modified: Wed, 01 Sep 2021 00:25:31 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7087df4b29e442773e368f72aa50cd7765fd6e6b43879c83880b0038e62b9077`  
		Last Modified: Wed, 01 Sep 2021 00:25:29 GMT  
		Size: 280.9 KB (280879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0062288c23918a5c405390da5fe197e453d3162f22d5e04c4e80c771bfb7dbb`  
		Last Modified: Wed, 01 Sep 2021 00:26:19 GMT  
		Size: 19.6 MB (19582082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a56af5fa9abf70534bf74916985c59602805aaec20e843a8fb80451dc2b4aa6b`  
		Last Modified: Wed, 01 Sep 2021 00:26:15 GMT  
		Size: 12.3 KB (12269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bad79cf9294c71cb171d84b1b435766c73b488c2eaf98668e8fb24c098ec8e0`  
		Last Modified: Wed, 01 Sep 2021 00:26:15 GMT  
		Size: 11.9 KB (11901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80584912177323f577d098fda53486bc0f440c26efb41dd2951ee13af7a0f369`  
		Last Modified: Wed, 01 Sep 2021 00:26:15 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:alpine`

```console
$ docker pull chronograf@sha256:bdb38dbf0d72892a4685b69391c89a1716a2465b0d52f79bd859a846f982c702
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:44ddcc13955fcee6ada98e17e24ee8f695a9823b3c3e999e5d315c9a3bb0aa8e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22689227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f86636178ef7f0961c639954f1607c343f7ed49e2749304818d81e8d9aaec58`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 31 Aug 2021 23:18:23 GMT
ADD file:e3d2013df9d58cd9255c749dbd62e7b1b1bdf1c2ee644c17bb93e67d859f0815 in / 
# Tue, 31 Aug 2021 23:18:24 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 00:23:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 01 Sep 2021 00:23:43 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Wed, 01 Sep 2021 00:24:42 GMT
ENV CHRONOGRAF_VERSION=1.9.0
# Wed, 01 Sep 2021 00:24:48 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 01 Sep 2021 00:24:49 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 01 Sep 2021 00:24:49 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 01 Sep 2021 00:24:50 GMT
EXPOSE 8888
# Wed, 01 Sep 2021 00:24:50 GMT
VOLUME [/var/lib/chronograf]
# Wed, 01 Sep 2021 00:24:51 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Wed, 01 Sep 2021 00:24:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Sep 2021 00:24:51 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:e519532ddf75bafbbb0ad01d3fb678ef9395cd8554fa25bef4695bb6e11f39f1`  
		Last Modified: Tue, 31 Aug 2021 23:19:05 GMT  
		Size: 2.8 MB (2801707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e69cd3502d3b453e253ea48e4ff56f5af4e25895a1bfa5e84cda59eaefce23be`  
		Last Modified: Wed, 01 Sep 2021 00:25:31 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7087df4b29e442773e368f72aa50cd7765fd6e6b43879c83880b0038e62b9077`  
		Last Modified: Wed, 01 Sep 2021 00:25:29 GMT  
		Size: 280.9 KB (280879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0062288c23918a5c405390da5fe197e453d3162f22d5e04c4e80c771bfb7dbb`  
		Last Modified: Wed, 01 Sep 2021 00:26:19 GMT  
		Size: 19.6 MB (19582082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a56af5fa9abf70534bf74916985c59602805aaec20e843a8fb80451dc2b4aa6b`  
		Last Modified: Wed, 01 Sep 2021 00:26:15 GMT  
		Size: 12.3 KB (12269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bad79cf9294c71cb171d84b1b435766c73b488c2eaf98668e8fb24c098ec8e0`  
		Last Modified: Wed, 01 Sep 2021 00:26:15 GMT  
		Size: 11.9 KB (11901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80584912177323f577d098fda53486bc0f440c26efb41dd2951ee13af7a0f369`  
		Last Modified: Wed, 01 Sep 2021 00:26:15 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:latest`

```console
$ docker pull chronograf@sha256:5efd920a71d94d1451451728a87976024944d9a6424de3bf6538b66fa56df107
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:latest` - linux; amd64

```console
$ docker pull chronograf@sha256:d30b8a1f515a1f68ac7675f55026ef00b5c9510dde3c84e552ceafbd8da84fd5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.8 MB (66757353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:071d9a46cb06f25d04e299d93f99d10334cd8b43d697b016191c1f87004f0c27`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 17 Aug 2021 01:26:09 GMT
ADD file:f6c4487fa1f7a4e17f5d88fd0c91031a6efc7fa210d363a1d43d8b0f3a8d1d03 in / 
# Tue, 17 Aug 2021 01:26:09 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 09:35:17 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 17 Aug 2021 09:36:21 GMT
ENV CHRONOGRAF_VERSION=1.9.0
# Tue, 17 Aug 2021 09:36:30 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 17 Aug 2021 09:36:30 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 17 Aug 2021 09:36:30 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 17 Aug 2021 09:36:31 GMT
EXPOSE 8888
# Tue, 17 Aug 2021 09:36:31 GMT
VOLUME [/var/lib/chronograf]
# Tue, 17 Aug 2021 09:36:31 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 17 Aug 2021 09:36:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Aug 2021 09:36:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:33f99cea3b7da8c6e0143c9fd7590c6d56f7d310ddd59b11be4ad485ae4cab2a`  
		Last Modified: Tue, 17 Aug 2021 01:33:27 GMT  
		Size: 22.5 MB (22527748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6ebf00cee8edb2723f73bb596dc02dac400fcd609c6288b968066e0333dc5cd`  
		Last Modified: Tue, 17 Aug 2021 09:37:00 GMT  
		Size: 6.8 MB (6760152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f88d589540170378ab6422d641b642a6aa1e3fd063d84997f3d21de4c5f78981`  
		Last Modified: Tue, 17 Aug 2021 09:37:53 GMT  
		Size: 37.4 MB (37445059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e800a265cf9be534a8fe5b59b309a201c2663c6741f7c25aa4227364f32b4ba5`  
		Last Modified: Tue, 17 Aug 2021 09:37:46 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ab0427bfc914c791fecbe16f14d108518b4438951f2dd347355fabc74377f53`  
		Last Modified: Tue, 17 Aug 2021 09:37:47 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ded1c3ae33fb215a5bba57e059b94f9659e7950e44b102640e396f3bf7c72b01`  
		Last Modified: Tue, 17 Aug 2021 09:37:46 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:latest` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:609775e3045917416f254d596222e113bebabf264680c6289ed7bb84e1aa0439
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60284183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b52137975532be06a48c3ceeedbf2bbd2b4f12a58bc040cdc385b36cc3204c55`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 03 Sep 2021 01:05:16 GMT
ADD file:425f8ae3b1354b9858904edb027190b58b65692a710cb50a4d463ac554f853a6 in / 
# Fri, 03 Sep 2021 01:05:17 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 02:45:29 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 03 Sep 2021 02:47:46 GMT
ENV CHRONOGRAF_VERSION=1.9.0
# Fri, 03 Sep 2021 02:48:06 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Fri, 03 Sep 2021 02:48:07 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 03 Sep 2021 02:48:07 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 03 Sep 2021 02:48:08 GMT
EXPOSE 8888
# Fri, 03 Sep 2021 02:48:08 GMT
VOLUME [/var/lib/chronograf]
# Fri, 03 Sep 2021 02:48:09 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Fri, 03 Sep 2021 02:48:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 03 Sep 2021 02:48:10 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:0c15a1a8c9dffe5dfe059b37d14b92f1eb4ea47f16ae7bf66bf62f34a7510dd6`  
		Last Modified: Fri, 03 Sep 2021 01:22:37 GMT  
		Size: 19.3 MB (19316099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb41f6e44cc2adc7b1da1ef11c2a061b83d79ad3aec2895b90e80a08e2eeb1be`  
		Last Modified: Fri, 03 Sep 2021 02:49:09 GMT  
		Size: 5.8 MB (5779569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2a8e857ff2824613b74370561a6f3ed4cf43acb1c72b8ec0604c75892f459cb`  
		Last Modified: Fri, 03 Sep 2021 02:50:58 GMT  
		Size: 35.2 MB (35164135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:736406488d5a7638a24ee9cf3f2cdefca5302b6c28f12d1ef089bd41c153f2a2`  
		Last Modified: Fri, 03 Sep 2021 02:50:40 GMT  
		Size: 12.2 KB (12241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a9b3a3fb52efb0b155e1a83b168f969aab6e53eb9a512ed6c6d16150b6d5bbc`  
		Last Modified: Fri, 03 Sep 2021 02:50:40 GMT  
		Size: 11.9 KB (11900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7af17a3f630e3db6735c25b8a73919284e41ae7925693423395adcd53097c8b7`  
		Last Modified: Fri, 03 Sep 2021 02:50:40 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:latest` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:b2ebe33396b3deb42dbdc543bc92331a8a242813e8705f7d9cc0bbd5a84a048d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61522879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1378f77cfd03e8e67afd75650a3fbc1ac23364337d73d700d99a7d4693d19887`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 17 Aug 2021 01:48:32 GMT
ADD file:5cd26935234cc0540158a144066c0341b46a0caeb0a80db0355eeb8cfaf4fc0d in / 
# Tue, 17 Aug 2021 01:48:32 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 08:06:44 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 17 Aug 2021 08:07:40 GMT
ENV CHRONOGRAF_VERSION=1.9.0
# Tue, 17 Aug 2021 08:07:48 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 17 Aug 2021 08:07:49 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 17 Aug 2021 08:07:49 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 17 Aug 2021 08:07:49 GMT
EXPOSE 8888
# Tue, 17 Aug 2021 08:07:49 GMT
VOLUME [/var/lib/chronograf]
# Tue, 17 Aug 2021 08:07:49 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 17 Aug 2021 08:07:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Aug 2021 08:07:50 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:f862659192cd149f96ede75854bd3ebf59937831d3e4103087ae62df34ef1a29`  
		Last Modified: Tue, 17 Aug 2021 01:58:00 GMT  
		Size: 20.4 MB (20389447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09101c696c7496dfd097387796cbe96c76aa138b186200c5879c0ab29f5a13f4`  
		Last Modified: Tue, 17 Aug 2021 08:08:19 GMT  
		Size: 6.0 MB (6047480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:460f0536e20a65b2904cd15722337b7302f9c0dab6e10fb222940f49a6075215`  
		Last Modified: Tue, 17 Aug 2021 08:09:10 GMT  
		Size: 35.1 MB (35061557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:010e9e427ef0ba79f667341edbabc8feb479b8c29c1c343bfc81e25b644480fb`  
		Last Modified: Tue, 17 Aug 2021 08:09:05 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ee27ad129e4bae5379fe5fe8edc5931a22031014148bc4d5b24e6e6c56421a`  
		Last Modified: Tue, 17 Aug 2021 08:09:05 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fed64ace818385e3d03fa5b6dc95f4092a80eb5838be8fef6a05f07dd5162c74`  
		Last Modified: Tue, 17 Aug 2021 08:09:05 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
