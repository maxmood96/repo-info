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
-	[`chronograf:1.9.4`](#chronograf194)
-	[`chronograf:1.9.4-alpine`](#chronograf194-alpine)
-	[`chronograf:alpine`](#chronografalpine)
-	[`chronograf:latest`](#chronograflatest)

## `chronograf:1.6`

```console
$ docker pull chronograf@sha256:363048988b1f8863ad98f406fa6190c8aeae287b7016519705281cc0b8eb4736
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.6` - linux; amd64

```console
$ docker pull chronograf@sha256:4ca8554e029e62750a25f7636a4824eab4fa77d538c6afb339ec7039ab3d46b6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49398078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:197b2cfb555f805fd66f12d47f521c4288b3dbe3516dcf214fc3f4973e71e22d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 29 Mar 2022 00:24:14 GMT
ADD file:67d83164f6e419d116be47b3e915cea9beb88948f1656f3f0924f249ac2894f3 in / 
# Tue, 29 Mar 2022 00:24:14 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 05:59:28 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 29 Mar 2022 05:59:28 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Tue, 29 Mar 2022 05:59:36 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 29 Mar 2022 05:59:36 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 29 Mar 2022 05:59:36 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 29 Mar 2022 05:59:36 GMT
EXPOSE 8888
# Tue, 29 Mar 2022 05:59:36 GMT
VOLUME [/var/lib/chronograf]
# Tue, 29 Mar 2022 05:59:37 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 29 Mar 2022 05:59:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 29 Mar 2022 05:59:37 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:21fb02cbac852f4be42877e7b52e5eab70cd1991c41fad18656f46c684fe4868`  
		Last Modified: Tue, 29 Mar 2022 00:31:08 GMT  
		Size: 22.6 MB (22567695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56b9c16e1754e07f3324fc31da705ef8a61540f0c8d8cdb08f2d86425ca373af`  
		Last Modified: Tue, 29 Mar 2022 06:01:23 GMT  
		Size: 6.8 MB (6760319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d919762f821e0b7f015dd51300adea896d552c9efdbc75e507b6fe3e1f16c4c6`  
		Last Modified: Tue, 29 Mar 2022 06:01:26 GMT  
		Size: 20.0 MB (20045671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22ee92ed87e48cca4188fc1fc7d3ff89f52a0d3df5eb4d055648664b8da0e1c3`  
		Last Modified: Tue, 29 Mar 2022 06:01:23 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60198571e227711068bf87cfce62fae31e51d3e0dadd1353991a1802ff26ac2a`  
		Last Modified: Tue, 29 Mar 2022 06:01:22 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20cd460a38732c66e47a74981e9631506328f87bee6046865a8e1b452db14041`  
		Last Modified: Tue, 29 Mar 2022 06:01:22 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.6` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:249973bd69f1d1d31680b558be22e7a8985af29da9f7dc44282ec59275681042
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.0 MB (43986001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c6122fd1295b2db71b1309529c0cb8ef3f1f0cb0273cf30f0f0eb7669cab816`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 17 Mar 2022 09:36:59 GMT
ADD file:28d5a216145f4b0aa29a7151a22e6e7dab9d430006122bbed8b13f84ae55713e in / 
# Thu, 17 Mar 2022 09:37:00 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 02:42:06 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Sat, 19 Mar 2022 02:42:06 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Sat, 19 Mar 2022 02:42:24 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Sat, 19 Mar 2022 02:42:24 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Sat, 19 Mar 2022 02:42:25 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sat, 19 Mar 2022 02:42:25 GMT
EXPOSE 8888
# Sat, 19 Mar 2022 02:42:26 GMT
VOLUME [/var/lib/chronograf]
# Sat, 19 Mar 2022 02:42:26 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Sat, 19 Mar 2022 02:42:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 19 Mar 2022 02:42:27 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:db6b474f79893f85b457aa5924e44453557a4b8963f5dbf6f78a60f93f73d19d`  
		Last Modified: Thu, 17 Mar 2022 09:53:37 GMT  
		Size: 19.4 MB (19359700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff6bf2997b6e0bfcc0741907bb7f1b0dcd194f8096745c677b23000d0147b16c`  
		Last Modified: Sat, 19 Mar 2022 02:45:56 GMT  
		Size: 5.8 MB (5780855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4695f55bcdcbf9e0bdb9109ffc2014d6fae5c4288151a807f774fe320f70da04`  
		Last Modified: Sat, 19 Mar 2022 02:46:06 GMT  
		Size: 18.8 MB (18821048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c48a57bd87a3f6c3a10131245b9499067938027cab9ab521f42efb4a932e828b`  
		Last Modified: Sat, 19 Mar 2022 02:45:53 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad042a44472a24eb21fbc4a2462a1aeb044803278f5bd02f64e3b3588fdee0c0`  
		Last Modified: Sat, 19 Mar 2022 02:45:53 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32303aea412cd1b9322be85d2ef4381418ccd186e9821df673b0da9345c6b88b`  
		Last Modified: Sat, 19 Mar 2022 02:45:53 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.6` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:3efcd27fad0b1d1c691abf60c5db33e54a2851e556839c5ffdddad6454520d53
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45456978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a792c808ec8ba2d16916eec975edf492ce240e66b18509a5c7a3333c2eba4dd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 17 Mar 2022 03:24:16 GMT
ADD file:9d9c04bf28d7e6075270ca8a75c01a6d4015bc3eccc4812a82681a7fabf27027 in / 
# Thu, 17 Mar 2022 03:24:17 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 22:26:56 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 17 Mar 2022 22:26:57 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Thu, 17 Mar 2022 22:27:04 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Thu, 17 Mar 2022 22:27:06 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 17 Mar 2022 22:27:07 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 17 Mar 2022 22:27:07 GMT
EXPOSE 8888
# Thu, 17 Mar 2022 22:27:08 GMT
VOLUME [/var/lib/chronograf]
# Thu, 17 Mar 2022 22:27:10 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Thu, 17 Mar 2022 22:27:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 17 Mar 2022 22:27:11 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:ecb1e7e01fa06e43b3018b38895366ba643cbac6d46bce566be2aa1cf10abf48`  
		Last Modified: Thu, 17 Mar 2022 03:32:58 GMT  
		Size: 20.4 MB (20423817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdcc9ed8b864108c2f441d508e2349d88968c42f8446c04f18fb121e256bd9bb`  
		Last Modified: Thu, 17 Mar 2022 22:29:15 GMT  
		Size: 6.0 MB (6047145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b49eb31bf8b92102afa0e9611d2127d24ba5d02a40d548d28d1fe63a56123c15`  
		Last Modified: Thu, 17 Mar 2022 22:29:17 GMT  
		Size: 19.0 MB (18961619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9f0f56891e4dd9e5e2e04eefbfd4ab2db58b05a943764ea37b56c31b26d145e`  
		Last Modified: Thu, 17 Mar 2022 22:29:14 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08e96f6a5814fd550c73b8f71ce07cff189d58c91084604bd5489b31cbcbd15a`  
		Last Modified: Thu, 17 Mar 2022 22:29:14 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1e990ea0aab83a77e2dc2e2b7d9b9340424377aff0f41590a752dfab868ea17`  
		Last Modified: Thu, 17 Mar 2022 22:29:14 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.6-alpine`

```console
$ docker pull chronograf@sha256:149094b38475e66a1765a73c97222000b0f56775a73a7943189a1fd002eefe42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.6-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:47951475ac48c790b9be5ac0140aad01c1c3567d0ffed3750e5818c55597b1a7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14852399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9539c7bb25466660437dd1598f3247aaffcd0800a2d2ef730ba231c6fa9f103f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 29 Mar 2022 00:19:41 GMT
ADD file:900b3c9d6bd18f94bde19b8eb177a55f956f4030deea9171e6c3da797a213636 in / 
# Tue, 29 Mar 2022 00:19:41 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 05:59:42 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 29 Mar 2022 05:59:43 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Tue, 29 Mar 2022 05:59:43 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Tue, 29 Mar 2022 05:59:47 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Tue, 29 Mar 2022 05:59:47 GMT
COPY file:aa4a9d01295c7013d89da92a943af071556aea6dbe6269affd4664fdd86969b8 in /usr/share/chronograf/LICENSE 
# Tue, 29 Mar 2022 05:59:47 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 29 Mar 2022 05:59:48 GMT
EXPOSE 8888
# Tue, 29 Mar 2022 05:59:48 GMT
VOLUME [/var/lib/chronograf]
# Tue, 29 Mar 2022 05:59:48 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Tue, 29 Mar 2022 05:59:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 29 Mar 2022 05:59:48 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:cfab2db722092277479ddd659049695fa8081d2a03c31b01d388cc21802de8b4`  
		Last Modified: Tue, 29 Mar 2022 00:20:33 GMT  
		Size: 2.8 MB (2818354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b8e4488850ad3e08f0aba8d339de3abde1e79494ff7d9a00067fa8b08eed46`  
		Last Modified: Tue, 29 Mar 2022 06:01:38 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f25991090eec670a7642f167cf12c22992033088ab88cc13dd27f5d7b50aada`  
		Last Modified: Tue, 29 Mar 2022 06:01:36 GMT  
		Size: 271.7 KB (271672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:190da19f5b9543d6dc11493484c017a3eee2d26c7fc9077c87e00b3ede667cd9`  
		Last Modified: Tue, 29 Mar 2022 06:01:40 GMT  
		Size: 11.7 MB (11737818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ff8558a8645d5e7c3aa21a4fb27e76a7f7af846a40496b2ca1ecf43aa012831`  
		Last Modified: Tue, 29 Mar 2022 06:01:36 GMT  
		Size: 12.3 KB (12270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4555f20c5e3a04c67fc6c5bb7950e9aca67e3458800da8a50557eb8ec1305d35`  
		Last Modified: Tue, 29 Mar 2022 06:01:36 GMT  
		Size: 11.9 KB (11894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f86da85397360345208ca762afd8341de76c77f25ba06fd037cc1c4083000c2`  
		Last Modified: Tue, 29 Mar 2022 06:01:37 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.6.2`

```console
$ docker pull chronograf@sha256:363048988b1f8863ad98f406fa6190c8aeae287b7016519705281cc0b8eb4736
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.6.2` - linux; amd64

```console
$ docker pull chronograf@sha256:4ca8554e029e62750a25f7636a4824eab4fa77d538c6afb339ec7039ab3d46b6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49398078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:197b2cfb555f805fd66f12d47f521c4288b3dbe3516dcf214fc3f4973e71e22d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 29 Mar 2022 00:24:14 GMT
ADD file:67d83164f6e419d116be47b3e915cea9beb88948f1656f3f0924f249ac2894f3 in / 
# Tue, 29 Mar 2022 00:24:14 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 05:59:28 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 29 Mar 2022 05:59:28 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Tue, 29 Mar 2022 05:59:36 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 29 Mar 2022 05:59:36 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 29 Mar 2022 05:59:36 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 29 Mar 2022 05:59:36 GMT
EXPOSE 8888
# Tue, 29 Mar 2022 05:59:36 GMT
VOLUME [/var/lib/chronograf]
# Tue, 29 Mar 2022 05:59:37 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 29 Mar 2022 05:59:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 29 Mar 2022 05:59:37 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:21fb02cbac852f4be42877e7b52e5eab70cd1991c41fad18656f46c684fe4868`  
		Last Modified: Tue, 29 Mar 2022 00:31:08 GMT  
		Size: 22.6 MB (22567695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56b9c16e1754e07f3324fc31da705ef8a61540f0c8d8cdb08f2d86425ca373af`  
		Last Modified: Tue, 29 Mar 2022 06:01:23 GMT  
		Size: 6.8 MB (6760319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d919762f821e0b7f015dd51300adea896d552c9efdbc75e507b6fe3e1f16c4c6`  
		Last Modified: Tue, 29 Mar 2022 06:01:26 GMT  
		Size: 20.0 MB (20045671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22ee92ed87e48cca4188fc1fc7d3ff89f52a0d3df5eb4d055648664b8da0e1c3`  
		Last Modified: Tue, 29 Mar 2022 06:01:23 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60198571e227711068bf87cfce62fae31e51d3e0dadd1353991a1802ff26ac2a`  
		Last Modified: Tue, 29 Mar 2022 06:01:22 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20cd460a38732c66e47a74981e9631506328f87bee6046865a8e1b452db14041`  
		Last Modified: Tue, 29 Mar 2022 06:01:22 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.6.2` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:249973bd69f1d1d31680b558be22e7a8985af29da9f7dc44282ec59275681042
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.0 MB (43986001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c6122fd1295b2db71b1309529c0cb8ef3f1f0cb0273cf30f0f0eb7669cab816`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 17 Mar 2022 09:36:59 GMT
ADD file:28d5a216145f4b0aa29a7151a22e6e7dab9d430006122bbed8b13f84ae55713e in / 
# Thu, 17 Mar 2022 09:37:00 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 02:42:06 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Sat, 19 Mar 2022 02:42:06 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Sat, 19 Mar 2022 02:42:24 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Sat, 19 Mar 2022 02:42:24 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Sat, 19 Mar 2022 02:42:25 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sat, 19 Mar 2022 02:42:25 GMT
EXPOSE 8888
# Sat, 19 Mar 2022 02:42:26 GMT
VOLUME [/var/lib/chronograf]
# Sat, 19 Mar 2022 02:42:26 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Sat, 19 Mar 2022 02:42:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 19 Mar 2022 02:42:27 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:db6b474f79893f85b457aa5924e44453557a4b8963f5dbf6f78a60f93f73d19d`  
		Last Modified: Thu, 17 Mar 2022 09:53:37 GMT  
		Size: 19.4 MB (19359700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff6bf2997b6e0bfcc0741907bb7f1b0dcd194f8096745c677b23000d0147b16c`  
		Last Modified: Sat, 19 Mar 2022 02:45:56 GMT  
		Size: 5.8 MB (5780855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4695f55bcdcbf9e0bdb9109ffc2014d6fae5c4288151a807f774fe320f70da04`  
		Last Modified: Sat, 19 Mar 2022 02:46:06 GMT  
		Size: 18.8 MB (18821048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c48a57bd87a3f6c3a10131245b9499067938027cab9ab521f42efb4a932e828b`  
		Last Modified: Sat, 19 Mar 2022 02:45:53 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad042a44472a24eb21fbc4a2462a1aeb044803278f5bd02f64e3b3588fdee0c0`  
		Last Modified: Sat, 19 Mar 2022 02:45:53 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32303aea412cd1b9322be85d2ef4381418ccd186e9821df673b0da9345c6b88b`  
		Last Modified: Sat, 19 Mar 2022 02:45:53 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.6.2` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:3efcd27fad0b1d1c691abf60c5db33e54a2851e556839c5ffdddad6454520d53
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45456978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a792c808ec8ba2d16916eec975edf492ce240e66b18509a5c7a3333c2eba4dd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 17 Mar 2022 03:24:16 GMT
ADD file:9d9c04bf28d7e6075270ca8a75c01a6d4015bc3eccc4812a82681a7fabf27027 in / 
# Thu, 17 Mar 2022 03:24:17 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 22:26:56 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 17 Mar 2022 22:26:57 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Thu, 17 Mar 2022 22:27:04 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Thu, 17 Mar 2022 22:27:06 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 17 Mar 2022 22:27:07 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 17 Mar 2022 22:27:07 GMT
EXPOSE 8888
# Thu, 17 Mar 2022 22:27:08 GMT
VOLUME [/var/lib/chronograf]
# Thu, 17 Mar 2022 22:27:10 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Thu, 17 Mar 2022 22:27:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 17 Mar 2022 22:27:11 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:ecb1e7e01fa06e43b3018b38895366ba643cbac6d46bce566be2aa1cf10abf48`  
		Last Modified: Thu, 17 Mar 2022 03:32:58 GMT  
		Size: 20.4 MB (20423817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdcc9ed8b864108c2f441d508e2349d88968c42f8446c04f18fb121e256bd9bb`  
		Last Modified: Thu, 17 Mar 2022 22:29:15 GMT  
		Size: 6.0 MB (6047145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b49eb31bf8b92102afa0e9611d2127d24ba5d02a40d548d28d1fe63a56123c15`  
		Last Modified: Thu, 17 Mar 2022 22:29:17 GMT  
		Size: 19.0 MB (18961619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9f0f56891e4dd9e5e2e04eefbfd4ab2db58b05a943764ea37b56c31b26d145e`  
		Last Modified: Thu, 17 Mar 2022 22:29:14 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08e96f6a5814fd550c73b8f71ce07cff189d58c91084604bd5489b31cbcbd15a`  
		Last Modified: Thu, 17 Mar 2022 22:29:14 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1e990ea0aab83a77e2dc2e2b7d9b9340424377aff0f41590a752dfab868ea17`  
		Last Modified: Thu, 17 Mar 2022 22:29:14 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.6.2-alpine`

```console
$ docker pull chronograf@sha256:149094b38475e66a1765a73c97222000b0f56775a73a7943189a1fd002eefe42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.6.2-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:47951475ac48c790b9be5ac0140aad01c1c3567d0ffed3750e5818c55597b1a7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14852399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9539c7bb25466660437dd1598f3247aaffcd0800a2d2ef730ba231c6fa9f103f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 29 Mar 2022 00:19:41 GMT
ADD file:900b3c9d6bd18f94bde19b8eb177a55f956f4030deea9171e6c3da797a213636 in / 
# Tue, 29 Mar 2022 00:19:41 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 05:59:42 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 29 Mar 2022 05:59:43 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Tue, 29 Mar 2022 05:59:43 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Tue, 29 Mar 2022 05:59:47 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Tue, 29 Mar 2022 05:59:47 GMT
COPY file:aa4a9d01295c7013d89da92a943af071556aea6dbe6269affd4664fdd86969b8 in /usr/share/chronograf/LICENSE 
# Tue, 29 Mar 2022 05:59:47 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 29 Mar 2022 05:59:48 GMT
EXPOSE 8888
# Tue, 29 Mar 2022 05:59:48 GMT
VOLUME [/var/lib/chronograf]
# Tue, 29 Mar 2022 05:59:48 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Tue, 29 Mar 2022 05:59:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 29 Mar 2022 05:59:48 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:cfab2db722092277479ddd659049695fa8081d2a03c31b01d388cc21802de8b4`  
		Last Modified: Tue, 29 Mar 2022 00:20:33 GMT  
		Size: 2.8 MB (2818354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b8e4488850ad3e08f0aba8d339de3abde1e79494ff7d9a00067fa8b08eed46`  
		Last Modified: Tue, 29 Mar 2022 06:01:38 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f25991090eec670a7642f167cf12c22992033088ab88cc13dd27f5d7b50aada`  
		Last Modified: Tue, 29 Mar 2022 06:01:36 GMT  
		Size: 271.7 KB (271672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:190da19f5b9543d6dc11493484c017a3eee2d26c7fc9077c87e00b3ede667cd9`  
		Last Modified: Tue, 29 Mar 2022 06:01:40 GMT  
		Size: 11.7 MB (11737818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ff8558a8645d5e7c3aa21a4fb27e76a7f7af846a40496b2ca1ecf43aa012831`  
		Last Modified: Tue, 29 Mar 2022 06:01:36 GMT  
		Size: 12.3 KB (12270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4555f20c5e3a04c67fc6c5bb7950e9aca67e3458800da8a50557eb8ec1305d35`  
		Last Modified: Tue, 29 Mar 2022 06:01:36 GMT  
		Size: 11.9 KB (11894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f86da85397360345208ca762afd8341de76c77f25ba06fd037cc1c4083000c2`  
		Last Modified: Tue, 29 Mar 2022 06:01:37 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.7`

```console
$ docker pull chronograf@sha256:916f2c9a2ebaee5b09287caad261ff3d51ca57246c8900a26d14e6cb3f6976a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.7` - linux; amd64

```console
$ docker pull chronograf@sha256:82a9ae69c50c3c55c4e16ec8689ba90901b8e2e9bf7e184e92cb32b9212e0be2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.4 MB (65427491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b88fcf8d4c8e2eb4455f196504af7e25e189641adb694dcc1c201cb9f809f9d9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 29 Mar 2022 00:24:14 GMT
ADD file:67d83164f6e419d116be47b3e915cea9beb88948f1656f3f0924f249ac2894f3 in / 
# Tue, 29 Mar 2022 00:24:14 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 05:59:58 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 29 Mar 2022 05:59:58 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 29 Mar 2022 06:00:09 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 29 Mar 2022 06:00:09 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 29 Mar 2022 06:00:09 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 29 Mar 2022 06:00:09 GMT
EXPOSE 8888
# Tue, 29 Mar 2022 06:00:09 GMT
VOLUME [/var/lib/chronograf]
# Tue, 29 Mar 2022 06:00:09 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 29 Mar 2022 06:00:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 29 Mar 2022 06:00:10 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:21fb02cbac852f4be42877e7b52e5eab70cd1991c41fad18656f46c684fe4868`  
		Last Modified: Tue, 29 Mar 2022 00:31:08 GMT  
		Size: 22.6 MB (22567695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc90ab2ee211a99d3732d06a98c04999d5882869742e5344236a3ee28856bba8`  
		Last Modified: Tue, 29 Mar 2022 06:01:49 GMT  
		Size: 4.5 MB (4506810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e3b1487b4246a38d7f72da0e808be469961e3326e8c320e4d0ee1e47360279f`  
		Last Modified: Tue, 29 Mar 2022 06:01:54 GMT  
		Size: 38.3 MB (38328592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ac292e41ce63f5189adcf715e178555707be1439a5eadbe563ba15c09393aed`  
		Last Modified: Tue, 29 Mar 2022 06:01:48 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d75aa23a466f649dc462f5343da1686868b9ed7363c5af1cf9c6ad19e55d998b`  
		Last Modified: Tue, 29 Mar 2022 06:01:49 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd5305b713625f1c0bd82f5c6606db8198f6c4c5cf5d007a5f33e8660df10ce9`  
		Last Modified: Tue, 29 Mar 2022 06:01:49 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.7` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:28c484e544019f8604fb64ba82edc840772a62a83f85fd728d4ffdbc39bf562e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.0 MB (59047982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9ae0844c27ebe65afbb8cecf1bfcfa4d9492baf97919d4cf00b867979d6908e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 17 Mar 2022 09:36:59 GMT
ADD file:28d5a216145f4b0aa29a7151a22e6e7dab9d430006122bbed8b13f84ae55713e in / 
# Thu, 17 Mar 2022 09:37:00 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 02:43:13 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Sat, 19 Mar 2022 02:43:13 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Sat, 19 Mar 2022 02:43:43 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Sat, 19 Mar 2022 02:43:44 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Sat, 19 Mar 2022 02:43:44 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sat, 19 Mar 2022 02:43:44 GMT
EXPOSE 8888
# Sat, 19 Mar 2022 02:43:45 GMT
VOLUME [/var/lib/chronograf]
# Sat, 19 Mar 2022 02:43:45 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Sat, 19 Mar 2022 02:43:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 19 Mar 2022 02:43:46 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:db6b474f79893f85b457aa5924e44453557a4b8963f5dbf6f78a60f93f73d19d`  
		Last Modified: Thu, 17 Mar 2022 09:53:37 GMT  
		Size: 19.4 MB (19359700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7e46ef5c29b4e0ef2dc186134f1993bb7fd2ee323e3768c50aee09466540e61`  
		Last Modified: Sat, 19 Mar 2022 02:46:19 GMT  
		Size: 3.9 MB (3880104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35490d8b8d8f838da5e1814750e0aebc6ce544038311bc0161cdea169e4abd22`  
		Last Modified: Sat, 19 Mar 2022 02:46:37 GMT  
		Size: 35.8 MB (35783786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b98e3601fa709163f85c69a22e9a1671d83c10a856db82f0162342167c1927a`  
		Last Modified: Sat, 19 Mar 2022 02:46:17 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ce4a91876a79a26ecada84785a9a3f882e69459227d0c339c73debb630df750`  
		Last Modified: Sat, 19 Mar 2022 02:46:17 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3ed16bc4a660ef4d840c6175d757f8e23fac64a252780abeba4ec79e8d428b2`  
		Last Modified: Sat, 19 Mar 2022 02:46:17 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.7` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:09e246219d0264d911a92ad0be54203fafc940702d62047c675f9f7dc290e9e4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60329425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b05e26649361353c66ad71e26220aa0497937d3c2a8d29943cba4d8485c8dba`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 17 Mar 2022 03:24:16 GMT
ADD file:9d9c04bf28d7e6075270ca8a75c01a6d4015bc3eccc4812a82681a7fabf27027 in / 
# Thu, 17 Mar 2022 03:24:17 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 22:27:43 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 17 Mar 2022 22:27:44 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Thu, 17 Mar 2022 22:27:56 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Thu, 17 Mar 2022 22:27:57 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 17 Mar 2022 22:27:58 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 17 Mar 2022 22:27:58 GMT
EXPOSE 8888
# Thu, 17 Mar 2022 22:27:59 GMT
VOLUME [/var/lib/chronograf]
# Thu, 17 Mar 2022 22:28:01 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Thu, 17 Mar 2022 22:28:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 17 Mar 2022 22:28:02 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:ecb1e7e01fa06e43b3018b38895366ba643cbac6d46bce566be2aa1cf10abf48`  
		Last Modified: Thu, 17 Mar 2022 03:32:58 GMT  
		Size: 20.4 MB (20423817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1c7e6a48dd13c5836b8b218a8372a493902f5c1fd57da5fd955912922b08908`  
		Last Modified: Thu, 17 Mar 2022 22:29:29 GMT  
		Size: 3.9 MB (3893978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ee03b87db2ef7df6d347aa7fece6d1b742b3f04cc4326f790b492a35aba5ff3`  
		Last Modified: Thu, 17 Mar 2022 22:29:33 GMT  
		Size: 36.0 MB (35987238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26efabf26d8cda661366200eba61be6c70512fcb3a4b7075d8c246ae611cdb10`  
		Last Modified: Thu, 17 Mar 2022 22:29:28 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6b4caa4fa7d35196b80ace1472f74b19ae694593e76f96317a47d711e50e227`  
		Last Modified: Thu, 17 Mar 2022 22:29:28 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24cb8978df300b2aaeecac468d0fc67f633057f78f17560b1cb51b90eab15205`  
		Last Modified: Thu, 17 Mar 2022 22:29:28 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.7-alpine`

```console
$ docker pull chronograf@sha256:b5b01d44c5d9035aef770c18b9d327a0968b802a8be1d006a00cb29cba80572f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.7-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:eebeee3efa2d087e65b7a372b0910361df1499481ae8276c0c9141932859a387
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22670796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:717726f6e8ebe674b82be439bf841971133c6e4340c8c0ce895c6ac5c2f64c94`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 29 Mar 2022 00:19:41 GMT
ADD file:900b3c9d6bd18f94bde19b8eb177a55f956f4030deea9171e6c3da797a213636 in / 
# Tue, 29 Mar 2022 00:19:41 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 05:59:42 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 29 Mar 2022 05:59:43 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Tue, 29 Mar 2022 06:00:14 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 29 Mar 2022 06:00:19 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Tue, 29 Mar 2022 06:00:19 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 29 Mar 2022 06:00:19 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 29 Mar 2022 06:00:19 GMT
EXPOSE 8888
# Tue, 29 Mar 2022 06:00:19 GMT
VOLUME [/var/lib/chronograf]
# Tue, 29 Mar 2022 06:00:19 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Tue, 29 Mar 2022 06:00:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 29 Mar 2022 06:00:20 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:cfab2db722092277479ddd659049695fa8081d2a03c31b01d388cc21802de8b4`  
		Last Modified: Tue, 29 Mar 2022 00:20:33 GMT  
		Size: 2.8 MB (2818354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b8e4488850ad3e08f0aba8d339de3abde1e79494ff7d9a00067fa8b08eed46`  
		Last Modified: Tue, 29 Mar 2022 06:01:38 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f25991090eec670a7642f167cf12c22992033088ab88cc13dd27f5d7b50aada`  
		Last Modified: Tue, 29 Mar 2022 06:01:36 GMT  
		Size: 271.7 KB (271672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aff4146b3517b8df8f33451c732a5e27f4b0a4779364c6c35e08344b124049c`  
		Last Modified: Tue, 29 Mar 2022 06:02:06 GMT  
		Size: 19.6 MB (19556218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05ec36459a9d9eb16d9a00cd7f1cd9cac171987d3aa941600af873314f4307e9`  
		Last Modified: Tue, 29 Mar 2022 06:02:03 GMT  
		Size: 12.3 KB (12265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c405900c5d3492fed542255cbec266bd3c407c83ccba7cca19592add7023403b`  
		Last Modified: Tue, 29 Mar 2022 06:02:03 GMT  
		Size: 11.9 KB (11896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbe9bfee9598e337978b28817031ecf1a8a826d9322b3d863f22de866787cce1`  
		Last Modified: Tue, 29 Mar 2022 06:02:03 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.7.17`

```console
$ docker pull chronograf@sha256:916f2c9a2ebaee5b09287caad261ff3d51ca57246c8900a26d14e6cb3f6976a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.7.17` - linux; amd64

```console
$ docker pull chronograf@sha256:82a9ae69c50c3c55c4e16ec8689ba90901b8e2e9bf7e184e92cb32b9212e0be2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.4 MB (65427491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b88fcf8d4c8e2eb4455f196504af7e25e189641adb694dcc1c201cb9f809f9d9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 29 Mar 2022 00:24:14 GMT
ADD file:67d83164f6e419d116be47b3e915cea9beb88948f1656f3f0924f249ac2894f3 in / 
# Tue, 29 Mar 2022 00:24:14 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 05:59:58 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 29 Mar 2022 05:59:58 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 29 Mar 2022 06:00:09 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 29 Mar 2022 06:00:09 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 29 Mar 2022 06:00:09 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 29 Mar 2022 06:00:09 GMT
EXPOSE 8888
# Tue, 29 Mar 2022 06:00:09 GMT
VOLUME [/var/lib/chronograf]
# Tue, 29 Mar 2022 06:00:09 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 29 Mar 2022 06:00:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 29 Mar 2022 06:00:10 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:21fb02cbac852f4be42877e7b52e5eab70cd1991c41fad18656f46c684fe4868`  
		Last Modified: Tue, 29 Mar 2022 00:31:08 GMT  
		Size: 22.6 MB (22567695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc90ab2ee211a99d3732d06a98c04999d5882869742e5344236a3ee28856bba8`  
		Last Modified: Tue, 29 Mar 2022 06:01:49 GMT  
		Size: 4.5 MB (4506810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e3b1487b4246a38d7f72da0e808be469961e3326e8c320e4d0ee1e47360279f`  
		Last Modified: Tue, 29 Mar 2022 06:01:54 GMT  
		Size: 38.3 MB (38328592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ac292e41ce63f5189adcf715e178555707be1439a5eadbe563ba15c09393aed`  
		Last Modified: Tue, 29 Mar 2022 06:01:48 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d75aa23a466f649dc462f5343da1686868b9ed7363c5af1cf9c6ad19e55d998b`  
		Last Modified: Tue, 29 Mar 2022 06:01:49 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd5305b713625f1c0bd82f5c6606db8198f6c4c5cf5d007a5f33e8660df10ce9`  
		Last Modified: Tue, 29 Mar 2022 06:01:49 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.7.17` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:28c484e544019f8604fb64ba82edc840772a62a83f85fd728d4ffdbc39bf562e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.0 MB (59047982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9ae0844c27ebe65afbb8cecf1bfcfa4d9492baf97919d4cf00b867979d6908e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 17 Mar 2022 09:36:59 GMT
ADD file:28d5a216145f4b0aa29a7151a22e6e7dab9d430006122bbed8b13f84ae55713e in / 
# Thu, 17 Mar 2022 09:37:00 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 02:43:13 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Sat, 19 Mar 2022 02:43:13 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Sat, 19 Mar 2022 02:43:43 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Sat, 19 Mar 2022 02:43:44 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Sat, 19 Mar 2022 02:43:44 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sat, 19 Mar 2022 02:43:44 GMT
EXPOSE 8888
# Sat, 19 Mar 2022 02:43:45 GMT
VOLUME [/var/lib/chronograf]
# Sat, 19 Mar 2022 02:43:45 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Sat, 19 Mar 2022 02:43:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 19 Mar 2022 02:43:46 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:db6b474f79893f85b457aa5924e44453557a4b8963f5dbf6f78a60f93f73d19d`  
		Last Modified: Thu, 17 Mar 2022 09:53:37 GMT  
		Size: 19.4 MB (19359700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7e46ef5c29b4e0ef2dc186134f1993bb7fd2ee323e3768c50aee09466540e61`  
		Last Modified: Sat, 19 Mar 2022 02:46:19 GMT  
		Size: 3.9 MB (3880104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35490d8b8d8f838da5e1814750e0aebc6ce544038311bc0161cdea169e4abd22`  
		Last Modified: Sat, 19 Mar 2022 02:46:37 GMT  
		Size: 35.8 MB (35783786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b98e3601fa709163f85c69a22e9a1671d83c10a856db82f0162342167c1927a`  
		Last Modified: Sat, 19 Mar 2022 02:46:17 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ce4a91876a79a26ecada84785a9a3f882e69459227d0c339c73debb630df750`  
		Last Modified: Sat, 19 Mar 2022 02:46:17 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3ed16bc4a660ef4d840c6175d757f8e23fac64a252780abeba4ec79e8d428b2`  
		Last Modified: Sat, 19 Mar 2022 02:46:17 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.7.17` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:09e246219d0264d911a92ad0be54203fafc940702d62047c675f9f7dc290e9e4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60329425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b05e26649361353c66ad71e26220aa0497937d3c2a8d29943cba4d8485c8dba`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 17 Mar 2022 03:24:16 GMT
ADD file:9d9c04bf28d7e6075270ca8a75c01a6d4015bc3eccc4812a82681a7fabf27027 in / 
# Thu, 17 Mar 2022 03:24:17 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 22:27:43 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 17 Mar 2022 22:27:44 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Thu, 17 Mar 2022 22:27:56 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Thu, 17 Mar 2022 22:27:57 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 17 Mar 2022 22:27:58 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 17 Mar 2022 22:27:58 GMT
EXPOSE 8888
# Thu, 17 Mar 2022 22:27:59 GMT
VOLUME [/var/lib/chronograf]
# Thu, 17 Mar 2022 22:28:01 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Thu, 17 Mar 2022 22:28:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 17 Mar 2022 22:28:02 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:ecb1e7e01fa06e43b3018b38895366ba643cbac6d46bce566be2aa1cf10abf48`  
		Last Modified: Thu, 17 Mar 2022 03:32:58 GMT  
		Size: 20.4 MB (20423817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1c7e6a48dd13c5836b8b218a8372a493902f5c1fd57da5fd955912922b08908`  
		Last Modified: Thu, 17 Mar 2022 22:29:29 GMT  
		Size: 3.9 MB (3893978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ee03b87db2ef7df6d347aa7fece6d1b742b3f04cc4326f790b492a35aba5ff3`  
		Last Modified: Thu, 17 Mar 2022 22:29:33 GMT  
		Size: 36.0 MB (35987238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26efabf26d8cda661366200eba61be6c70512fcb3a4b7075d8c246ae611cdb10`  
		Last Modified: Thu, 17 Mar 2022 22:29:28 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6b4caa4fa7d35196b80ace1472f74b19ae694593e76f96317a47d711e50e227`  
		Last Modified: Thu, 17 Mar 2022 22:29:28 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24cb8978df300b2aaeecac468d0fc67f633057f78f17560b1cb51b90eab15205`  
		Last Modified: Thu, 17 Mar 2022 22:29:28 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.7.17-alpine`

```console
$ docker pull chronograf@sha256:b5b01d44c5d9035aef770c18b9d327a0968b802a8be1d006a00cb29cba80572f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.7.17-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:eebeee3efa2d087e65b7a372b0910361df1499481ae8276c0c9141932859a387
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22670796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:717726f6e8ebe674b82be439bf841971133c6e4340c8c0ce895c6ac5c2f64c94`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 29 Mar 2022 00:19:41 GMT
ADD file:900b3c9d6bd18f94bde19b8eb177a55f956f4030deea9171e6c3da797a213636 in / 
# Tue, 29 Mar 2022 00:19:41 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 05:59:42 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 29 Mar 2022 05:59:43 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Tue, 29 Mar 2022 06:00:14 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 29 Mar 2022 06:00:19 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Tue, 29 Mar 2022 06:00:19 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 29 Mar 2022 06:00:19 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 29 Mar 2022 06:00:19 GMT
EXPOSE 8888
# Tue, 29 Mar 2022 06:00:19 GMT
VOLUME [/var/lib/chronograf]
# Tue, 29 Mar 2022 06:00:19 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Tue, 29 Mar 2022 06:00:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 29 Mar 2022 06:00:20 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:cfab2db722092277479ddd659049695fa8081d2a03c31b01d388cc21802de8b4`  
		Last Modified: Tue, 29 Mar 2022 00:20:33 GMT  
		Size: 2.8 MB (2818354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b8e4488850ad3e08f0aba8d339de3abde1e79494ff7d9a00067fa8b08eed46`  
		Last Modified: Tue, 29 Mar 2022 06:01:38 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f25991090eec670a7642f167cf12c22992033088ab88cc13dd27f5d7b50aada`  
		Last Modified: Tue, 29 Mar 2022 06:01:36 GMT  
		Size: 271.7 KB (271672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aff4146b3517b8df8f33451c732a5e27f4b0a4779364c6c35e08344b124049c`  
		Last Modified: Tue, 29 Mar 2022 06:02:06 GMT  
		Size: 19.6 MB (19556218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05ec36459a9d9eb16d9a00cd7f1cd9cac171987d3aa941600af873314f4307e9`  
		Last Modified: Tue, 29 Mar 2022 06:02:03 GMT  
		Size: 12.3 KB (12265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c405900c5d3492fed542255cbec266bd3c407c83ccba7cca19592add7023403b`  
		Last Modified: Tue, 29 Mar 2022 06:02:03 GMT  
		Size: 11.9 KB (11896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbe9bfee9598e337978b28817031ecf1a8a826d9322b3d863f22de866787cce1`  
		Last Modified: Tue, 29 Mar 2022 06:02:03 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.8`

```console
$ docker pull chronograf@sha256:42aa430f9dfe0dc26166040f98b5bb61c2f4aaada32e86112bfa9dcb93a4c3f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.8` - linux; amd64

```console
$ docker pull chronograf@sha256:31b2fc8169a25236774c93e707100bd30ead45e9b638e5cf26a0c0a07301477e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66279048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2575d5adf2a8064cbb53dda61fb9da258efbd2739a5cd38b10978813d777ae86`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 29 Mar 2022 00:24:14 GMT
ADD file:67d83164f6e419d116be47b3e915cea9beb88948f1656f3f0924f249ac2894f3 in / 
# Tue, 29 Mar 2022 00:24:14 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 05:59:28 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 29 Mar 2022 06:00:22 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Tue, 29 Mar 2022 06:00:30 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 29 Mar 2022 06:00:30 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 29 Mar 2022 06:00:31 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 29 Mar 2022 06:00:31 GMT
EXPOSE 8888
# Tue, 29 Mar 2022 06:00:31 GMT
VOLUME [/var/lib/chronograf]
# Tue, 29 Mar 2022 06:00:31 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 29 Mar 2022 06:00:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 29 Mar 2022 06:00:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:21fb02cbac852f4be42877e7b52e5eab70cd1991c41fad18656f46c684fe4868`  
		Last Modified: Tue, 29 Mar 2022 00:31:08 GMT  
		Size: 22.6 MB (22567695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56b9c16e1754e07f3324fc31da705ef8a61540f0c8d8cdb08f2d86425ca373af`  
		Last Modified: Tue, 29 Mar 2022 06:01:23 GMT  
		Size: 6.8 MB (6760319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:560721966902f64cbc88ea4993558380641375bf0a2aa60ad7e5634e75923cfc`  
		Last Modified: Tue, 29 Mar 2022 06:02:20 GMT  
		Size: 36.9 MB (36926648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3c87b8e0cb0748cdf0a89aed64124ef471316f31ddc62ac4acca3e51f702437`  
		Last Modified: Tue, 29 Mar 2022 06:02:16 GMT  
		Size: 12.2 KB (12242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e47d864d19ed24cfe33805b0f6a4b79ddef18f4f47c5de7053de376e7cf8ea0`  
		Last Modified: Tue, 29 Mar 2022 06:02:16 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d79949ae8c42bca83b746ba9e1747e0724e30a20883d9210909346c93325007`  
		Last Modified: Tue, 29 Mar 2022 06:02:16 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.8` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:1525b88b8b42f3c0b721c82641b30a90734abddb9a8a3eb65b5fad0439ce9eb5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59676946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dc232ab5a714446b4595257c02e1b938cbd3259744762066d8b770de23e6171`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 17 Mar 2022 09:36:59 GMT
ADD file:28d5a216145f4b0aa29a7151a22e6e7dab9d430006122bbed8b13f84ae55713e in / 
# Thu, 17 Mar 2022 09:37:00 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 02:42:06 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Sat, 19 Mar 2022 02:44:04 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Sat, 19 Mar 2022 02:44:23 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Sat, 19 Mar 2022 02:44:24 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Sat, 19 Mar 2022 02:44:24 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sat, 19 Mar 2022 02:44:25 GMT
EXPOSE 8888
# Sat, 19 Mar 2022 02:44:25 GMT
VOLUME [/var/lib/chronograf]
# Sat, 19 Mar 2022 02:44:26 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Sat, 19 Mar 2022 02:44:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 19 Mar 2022 02:44:26 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:db6b474f79893f85b457aa5924e44453557a4b8963f5dbf6f78a60f93f73d19d`  
		Last Modified: Thu, 17 Mar 2022 09:53:37 GMT  
		Size: 19.4 MB (19359700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff6bf2997b6e0bfcc0741907bb7f1b0dcd194f8096745c677b23000d0147b16c`  
		Last Modified: Sat, 19 Mar 2022 02:45:56 GMT  
		Size: 5.8 MB (5780855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dabec4b9ec5f4af9fa45bd73cae34b7f48ac7683442cbbf3c0fdfad795e0f1e2`  
		Last Modified: Sat, 19 Mar 2022 02:47:07 GMT  
		Size: 34.5 MB (34511995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df234141d3473a6c753871ac5692bf1a7f936877c2fd82224e02e2e7635565cf`  
		Last Modified: Sat, 19 Mar 2022 02:46:49 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd657a9a51ce033c48157d720402eaeef59a726e65d2e48a936caf82837240f4`  
		Last Modified: Sat, 19 Mar 2022 02:46:48 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cc56ad5df3c1b361bec71cbe8609a945f7a52379dbb816dcdf1fe18fe4cf308`  
		Last Modified: Sat, 19 Mar 2022 02:46:48 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.8` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:f4419f7c07ad710f862ede3620c211660b54f7a853b8ba1e49111ffffec60522
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60926992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e198a1d504a269c573cbb65153cf66b357f2bbb8819c47ac787875f47f4205c7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 17 Mar 2022 03:24:16 GMT
ADD file:9d9c04bf28d7e6075270ca8a75c01a6d4015bc3eccc4812a82681a7fabf27027 in / 
# Thu, 17 Mar 2022 03:24:17 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 22:26:56 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 17 Mar 2022 22:28:12 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Thu, 17 Mar 2022 22:28:20 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Thu, 17 Mar 2022 22:28:22 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 17 Mar 2022 22:28:23 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 17 Mar 2022 22:28:23 GMT
EXPOSE 8888
# Thu, 17 Mar 2022 22:28:24 GMT
VOLUME [/var/lib/chronograf]
# Thu, 17 Mar 2022 22:28:26 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Thu, 17 Mar 2022 22:28:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 17 Mar 2022 22:28:27 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:ecb1e7e01fa06e43b3018b38895366ba643cbac6d46bce566be2aa1cf10abf48`  
		Last Modified: Thu, 17 Mar 2022 03:32:58 GMT  
		Size: 20.4 MB (20423817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdcc9ed8b864108c2f441d508e2349d88968c42f8446c04f18fb121e256bd9bb`  
		Last Modified: Thu, 17 Mar 2022 22:29:15 GMT  
		Size: 6.0 MB (6047145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feff8b25ef2859d6d5baa4cb27318419efe784820857970e2fcefc8ecceb4c92`  
		Last Modified: Thu, 17 Mar 2022 22:29:49 GMT  
		Size: 34.4 MB (34431638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d273285d82262d4299a0d4651c5e0afc50c7b84b6a692198d79215a6d7b5dbd8`  
		Last Modified: Thu, 17 Mar 2022 22:29:44 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9871739638ffdb446fc0ffec3c5269a1872cc3255467e1be724299bbef9813e1`  
		Last Modified: Thu, 17 Mar 2022 22:29:44 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2450f64c0a194bb55a966b877ba08cbbdbf5b1421237c417b0e87bd41c32acc9`  
		Last Modified: Thu, 17 Mar 2022 22:29:44 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.8-alpine`

```console
$ docker pull chronograf@sha256:683ec635da540c60d440a716b470d4c3eb215b8c19c81ca319d78b6bef9e4823
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.8-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:4dad309eabab3e5fd63df66e2fbe6b73a6300af3fb96d46c878f3af706965f96
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.3 MB (22318519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f035563c7dc22996dd78b387ec7b03f742f125426ef72d8887aa3ea190850e5c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 29 Mar 2022 00:19:41 GMT
ADD file:900b3c9d6bd18f94bde19b8eb177a55f956f4030deea9171e6c3da797a213636 in / 
# Tue, 29 Mar 2022 00:19:41 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 05:59:42 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 29 Mar 2022 05:59:43 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Tue, 29 Mar 2022 06:00:33 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Tue, 29 Mar 2022 06:00:38 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Tue, 29 Mar 2022 06:00:38 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 29 Mar 2022 06:00:39 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 29 Mar 2022 06:00:39 GMT
EXPOSE 8888
# Tue, 29 Mar 2022 06:00:39 GMT
VOLUME [/var/lib/chronograf]
# Tue, 29 Mar 2022 06:00:39 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Tue, 29 Mar 2022 06:00:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 29 Mar 2022 06:00:39 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:cfab2db722092277479ddd659049695fa8081d2a03c31b01d388cc21802de8b4`  
		Last Modified: Tue, 29 Mar 2022 00:20:33 GMT  
		Size: 2.8 MB (2818354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b8e4488850ad3e08f0aba8d339de3abde1e79494ff7d9a00067fa8b08eed46`  
		Last Modified: Tue, 29 Mar 2022 06:01:38 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f25991090eec670a7642f167cf12c22992033088ab88cc13dd27f5d7b50aada`  
		Last Modified: Tue, 29 Mar 2022 06:01:36 GMT  
		Size: 271.7 KB (271672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:110fba8622ed8de7f3805d03104130dc6f1ff6be7548830f9dc90bb7c51e8eeb`  
		Last Modified: Tue, 29 Mar 2022 06:02:33 GMT  
		Size: 19.2 MB (19203942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb79040e735ea81a7c47a719dbc0d96c6853c2ac870a868eb1be5d21d7fbca20`  
		Last Modified: Tue, 29 Mar 2022 06:02:30 GMT  
		Size: 12.3 KB (12266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aa242e8ce0a14c30a0ddbbd91835d9c608756e349d42854e69340e120b9b572`  
		Last Modified: Tue, 29 Mar 2022 06:02:30 GMT  
		Size: 11.9 KB (11895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e65fc00914b7c9fea3d787e61fd8344b330a9183881e12f11636825d90a9dac`  
		Last Modified: Tue, 29 Mar 2022 06:02:30 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.8.10`

```console
$ docker pull chronograf@sha256:42aa430f9dfe0dc26166040f98b5bb61c2f4aaada32e86112bfa9dcb93a4c3f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.8.10` - linux; amd64

```console
$ docker pull chronograf@sha256:31b2fc8169a25236774c93e707100bd30ead45e9b638e5cf26a0c0a07301477e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66279048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2575d5adf2a8064cbb53dda61fb9da258efbd2739a5cd38b10978813d777ae86`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 29 Mar 2022 00:24:14 GMT
ADD file:67d83164f6e419d116be47b3e915cea9beb88948f1656f3f0924f249ac2894f3 in / 
# Tue, 29 Mar 2022 00:24:14 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 05:59:28 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 29 Mar 2022 06:00:22 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Tue, 29 Mar 2022 06:00:30 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 29 Mar 2022 06:00:30 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 29 Mar 2022 06:00:31 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 29 Mar 2022 06:00:31 GMT
EXPOSE 8888
# Tue, 29 Mar 2022 06:00:31 GMT
VOLUME [/var/lib/chronograf]
# Tue, 29 Mar 2022 06:00:31 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 29 Mar 2022 06:00:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 29 Mar 2022 06:00:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:21fb02cbac852f4be42877e7b52e5eab70cd1991c41fad18656f46c684fe4868`  
		Last Modified: Tue, 29 Mar 2022 00:31:08 GMT  
		Size: 22.6 MB (22567695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56b9c16e1754e07f3324fc31da705ef8a61540f0c8d8cdb08f2d86425ca373af`  
		Last Modified: Tue, 29 Mar 2022 06:01:23 GMT  
		Size: 6.8 MB (6760319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:560721966902f64cbc88ea4993558380641375bf0a2aa60ad7e5634e75923cfc`  
		Last Modified: Tue, 29 Mar 2022 06:02:20 GMT  
		Size: 36.9 MB (36926648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3c87b8e0cb0748cdf0a89aed64124ef471316f31ddc62ac4acca3e51f702437`  
		Last Modified: Tue, 29 Mar 2022 06:02:16 GMT  
		Size: 12.2 KB (12242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e47d864d19ed24cfe33805b0f6a4b79ddef18f4f47c5de7053de376e7cf8ea0`  
		Last Modified: Tue, 29 Mar 2022 06:02:16 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d79949ae8c42bca83b746ba9e1747e0724e30a20883d9210909346c93325007`  
		Last Modified: Tue, 29 Mar 2022 06:02:16 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.8.10` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:1525b88b8b42f3c0b721c82641b30a90734abddb9a8a3eb65b5fad0439ce9eb5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59676946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dc232ab5a714446b4595257c02e1b938cbd3259744762066d8b770de23e6171`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 17 Mar 2022 09:36:59 GMT
ADD file:28d5a216145f4b0aa29a7151a22e6e7dab9d430006122bbed8b13f84ae55713e in / 
# Thu, 17 Mar 2022 09:37:00 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 02:42:06 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Sat, 19 Mar 2022 02:44:04 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Sat, 19 Mar 2022 02:44:23 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Sat, 19 Mar 2022 02:44:24 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Sat, 19 Mar 2022 02:44:24 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sat, 19 Mar 2022 02:44:25 GMT
EXPOSE 8888
# Sat, 19 Mar 2022 02:44:25 GMT
VOLUME [/var/lib/chronograf]
# Sat, 19 Mar 2022 02:44:26 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Sat, 19 Mar 2022 02:44:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 19 Mar 2022 02:44:26 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:db6b474f79893f85b457aa5924e44453557a4b8963f5dbf6f78a60f93f73d19d`  
		Last Modified: Thu, 17 Mar 2022 09:53:37 GMT  
		Size: 19.4 MB (19359700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff6bf2997b6e0bfcc0741907bb7f1b0dcd194f8096745c677b23000d0147b16c`  
		Last Modified: Sat, 19 Mar 2022 02:45:56 GMT  
		Size: 5.8 MB (5780855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dabec4b9ec5f4af9fa45bd73cae34b7f48ac7683442cbbf3c0fdfad795e0f1e2`  
		Last Modified: Sat, 19 Mar 2022 02:47:07 GMT  
		Size: 34.5 MB (34511995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df234141d3473a6c753871ac5692bf1a7f936877c2fd82224e02e2e7635565cf`  
		Last Modified: Sat, 19 Mar 2022 02:46:49 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd657a9a51ce033c48157d720402eaeef59a726e65d2e48a936caf82837240f4`  
		Last Modified: Sat, 19 Mar 2022 02:46:48 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cc56ad5df3c1b361bec71cbe8609a945f7a52379dbb816dcdf1fe18fe4cf308`  
		Last Modified: Sat, 19 Mar 2022 02:46:48 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.8.10` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:f4419f7c07ad710f862ede3620c211660b54f7a853b8ba1e49111ffffec60522
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60926992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e198a1d504a269c573cbb65153cf66b357f2bbb8819c47ac787875f47f4205c7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 17 Mar 2022 03:24:16 GMT
ADD file:9d9c04bf28d7e6075270ca8a75c01a6d4015bc3eccc4812a82681a7fabf27027 in / 
# Thu, 17 Mar 2022 03:24:17 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 22:26:56 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 17 Mar 2022 22:28:12 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Thu, 17 Mar 2022 22:28:20 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Thu, 17 Mar 2022 22:28:22 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 17 Mar 2022 22:28:23 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 17 Mar 2022 22:28:23 GMT
EXPOSE 8888
# Thu, 17 Mar 2022 22:28:24 GMT
VOLUME [/var/lib/chronograf]
# Thu, 17 Mar 2022 22:28:26 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Thu, 17 Mar 2022 22:28:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 17 Mar 2022 22:28:27 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:ecb1e7e01fa06e43b3018b38895366ba643cbac6d46bce566be2aa1cf10abf48`  
		Last Modified: Thu, 17 Mar 2022 03:32:58 GMT  
		Size: 20.4 MB (20423817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdcc9ed8b864108c2f441d508e2349d88968c42f8446c04f18fb121e256bd9bb`  
		Last Modified: Thu, 17 Mar 2022 22:29:15 GMT  
		Size: 6.0 MB (6047145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feff8b25ef2859d6d5baa4cb27318419efe784820857970e2fcefc8ecceb4c92`  
		Last Modified: Thu, 17 Mar 2022 22:29:49 GMT  
		Size: 34.4 MB (34431638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d273285d82262d4299a0d4651c5e0afc50c7b84b6a692198d79215a6d7b5dbd8`  
		Last Modified: Thu, 17 Mar 2022 22:29:44 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9871739638ffdb446fc0ffec3c5269a1872cc3255467e1be724299bbef9813e1`  
		Last Modified: Thu, 17 Mar 2022 22:29:44 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2450f64c0a194bb55a966b877ba08cbbdbf5b1421237c417b0e87bd41c32acc9`  
		Last Modified: Thu, 17 Mar 2022 22:29:44 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.8.10-alpine`

```console
$ docker pull chronograf@sha256:683ec635da540c60d440a716b470d4c3eb215b8c19c81ca319d78b6bef9e4823
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.8.10-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:4dad309eabab3e5fd63df66e2fbe6b73a6300af3fb96d46c878f3af706965f96
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.3 MB (22318519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f035563c7dc22996dd78b387ec7b03f742f125426ef72d8887aa3ea190850e5c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 29 Mar 2022 00:19:41 GMT
ADD file:900b3c9d6bd18f94bde19b8eb177a55f956f4030deea9171e6c3da797a213636 in / 
# Tue, 29 Mar 2022 00:19:41 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 05:59:42 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 29 Mar 2022 05:59:43 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Tue, 29 Mar 2022 06:00:33 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Tue, 29 Mar 2022 06:00:38 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Tue, 29 Mar 2022 06:00:38 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 29 Mar 2022 06:00:39 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 29 Mar 2022 06:00:39 GMT
EXPOSE 8888
# Tue, 29 Mar 2022 06:00:39 GMT
VOLUME [/var/lib/chronograf]
# Tue, 29 Mar 2022 06:00:39 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Tue, 29 Mar 2022 06:00:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 29 Mar 2022 06:00:39 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:cfab2db722092277479ddd659049695fa8081d2a03c31b01d388cc21802de8b4`  
		Last Modified: Tue, 29 Mar 2022 00:20:33 GMT  
		Size: 2.8 MB (2818354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b8e4488850ad3e08f0aba8d339de3abde1e79494ff7d9a00067fa8b08eed46`  
		Last Modified: Tue, 29 Mar 2022 06:01:38 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f25991090eec670a7642f167cf12c22992033088ab88cc13dd27f5d7b50aada`  
		Last Modified: Tue, 29 Mar 2022 06:01:36 GMT  
		Size: 271.7 KB (271672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:110fba8622ed8de7f3805d03104130dc6f1ff6be7548830f9dc90bb7c51e8eeb`  
		Last Modified: Tue, 29 Mar 2022 06:02:33 GMT  
		Size: 19.2 MB (19203942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb79040e735ea81a7c47a719dbc0d96c6853c2ac870a868eb1be5d21d7fbca20`  
		Last Modified: Tue, 29 Mar 2022 06:02:30 GMT  
		Size: 12.3 KB (12266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aa242e8ce0a14c30a0ddbbd91835d9c608756e349d42854e69340e120b9b572`  
		Last Modified: Tue, 29 Mar 2022 06:02:30 GMT  
		Size: 11.9 KB (11895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e65fc00914b7c9fea3d787e61fd8344b330a9183881e12f11636825d90a9dac`  
		Last Modified: Tue, 29 Mar 2022 06:02:30 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.9`

```console
$ docker pull chronograf@sha256:704f75c4a7355448058209d9ced2b71536e092ed744aa6727a3b1c27020026a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.9` - linux; amd64

```console
$ docker pull chronograf@sha256:15a99f7a300d2e041300009a3c364b1f724119fc299f8a40dd3b2882a282d4c5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.9 MB (66922847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53ba73fe4ae163f4ad5c16f29664af403847e437f25c9b8b050fcaa82533485a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 29 Mar 2022 00:24:14 GMT
ADD file:67d83164f6e419d116be47b3e915cea9beb88948f1656f3f0924f249ac2894f3 in / 
# Tue, 29 Mar 2022 00:24:14 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 05:59:28 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 29 Mar 2022 06:00:41 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Tue, 29 Mar 2022 06:00:50 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 29 Mar 2022 06:00:50 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 29 Mar 2022 06:00:50 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 29 Mar 2022 06:00:50 GMT
EXPOSE 8888
# Tue, 29 Mar 2022 06:00:50 GMT
VOLUME [/var/lib/chronograf]
# Tue, 29 Mar 2022 06:00:50 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 29 Mar 2022 06:00:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 29 Mar 2022 06:00:51 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:21fb02cbac852f4be42877e7b52e5eab70cd1991c41fad18656f46c684fe4868`  
		Last Modified: Tue, 29 Mar 2022 00:31:08 GMT  
		Size: 22.6 MB (22567695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56b9c16e1754e07f3324fc31da705ef8a61540f0c8d8cdb08f2d86425ca373af`  
		Last Modified: Tue, 29 Mar 2022 06:01:23 GMT  
		Size: 6.8 MB (6760319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0bda37b43acd0c440794a23a5765a56372231df70c41b2f64fa0a6c79871b02`  
		Last Modified: Tue, 29 Mar 2022 06:02:47 GMT  
		Size: 37.6 MB (37570449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e091fb54b38ba68b0e7fefb8249b3be64a9d3b07e389234811a38fcfca3add5c`  
		Last Modified: Tue, 29 Mar 2022 06:02:42 GMT  
		Size: 12.2 KB (12242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d3ce8d41d7dff561e4f28e9aefb93d548cc683ca81b47663e270c52105d08fe`  
		Last Modified: Tue, 29 Mar 2022 06:02:42 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1032cdb5990ddcf856cc28132155100914d3642debc19b29c32a217fece104e7`  
		Last Modified: Tue, 29 Mar 2022 06:02:42 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.9` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:bfeb7966a4c5fb1bf24eb18ba92d922624888cd3be110355b2c674d252a6389b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.5 MB (60456428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a33945351a002efc5f47a74cf82a21f244afa0dde4efc3637f0796513a7c9254`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 17 Mar 2022 09:36:59 GMT
ADD file:28d5a216145f4b0aa29a7151a22e6e7dab9d430006122bbed8b13f84ae55713e in / 
# Thu, 17 Mar 2022 09:37:00 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 02:42:06 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 24 Mar 2022 22:21:01 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Thu, 24 Mar 2022 22:21:20 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Thu, 24 Mar 2022 22:21:21 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 24 Mar 2022 22:21:21 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 24 Mar 2022 22:21:21 GMT
EXPOSE 8888
# Thu, 24 Mar 2022 22:21:22 GMT
VOLUME [/var/lib/chronograf]
# Thu, 24 Mar 2022 22:21:22 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Thu, 24 Mar 2022 22:21:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 24 Mar 2022 22:21:23 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:db6b474f79893f85b457aa5924e44453557a4b8963f5dbf6f78a60f93f73d19d`  
		Last Modified: Thu, 17 Mar 2022 09:53:37 GMT  
		Size: 19.4 MB (19359700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff6bf2997b6e0bfcc0741907bb7f1b0dcd194f8096745c677b23000d0147b16c`  
		Last Modified: Sat, 19 Mar 2022 02:45:56 GMT  
		Size: 5.8 MB (5780855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddb9109c6da475cc963f12be9c4a328783af849e0bd2ee79d85430d2a0614382`  
		Last Modified: Thu, 24 Mar 2022 22:22:43 GMT  
		Size: 35.3 MB (35291482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:119d602e1079d24260c1760a150c4d6bda21b42c978eb1e07e2e29f41a823e8b`  
		Last Modified: Thu, 24 Mar 2022 22:22:24 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93e4ee91a2464457151ba353133acb38787214c628cf5f0c767f814ea6e040af`  
		Last Modified: Thu, 24 Mar 2022 22:22:24 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7ce674455f2d68cfe0af6f9360d133c707a42f55e2e901082f06404aff9ced4`  
		Last Modified: Thu, 24 Mar 2022 22:22:24 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.9` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:6ad923beb75f1f8da1cd14a3e86204c8f4aa144608359dfa5cc54f9e6159ddee
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61669535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72bd3711653ee186a5445233af133b67624cbca85683492be81f37dfcaee3e43`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 17 Mar 2022 03:24:16 GMT
ADD file:9d9c04bf28d7e6075270ca8a75c01a6d4015bc3eccc4812a82681a7fabf27027 in / 
# Thu, 17 Mar 2022 03:24:17 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 22:26:56 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 24 Mar 2022 21:39:46 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Thu, 24 Mar 2022 21:39:55 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Thu, 24 Mar 2022 21:39:56 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 24 Mar 2022 21:39:57 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 24 Mar 2022 21:39:57 GMT
EXPOSE 8888
# Thu, 24 Mar 2022 21:39:58 GMT
VOLUME [/var/lib/chronograf]
# Thu, 24 Mar 2022 21:40:00 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Thu, 24 Mar 2022 21:40:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 24 Mar 2022 21:40:01 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:ecb1e7e01fa06e43b3018b38895366ba643cbac6d46bce566be2aa1cf10abf48`  
		Last Modified: Thu, 17 Mar 2022 03:32:58 GMT  
		Size: 20.4 MB (20423817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdcc9ed8b864108c2f441d508e2349d88968c42f8446c04f18fb121e256bd9bb`  
		Last Modified: Thu, 17 Mar 2022 22:29:15 GMT  
		Size: 6.0 MB (6047145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8693526e8c2799b835c31d42a7cdd67b1b354b5707b2ccc44c885949036ebad9`  
		Last Modified: Thu, 24 Mar 2022 21:40:35 GMT  
		Size: 35.2 MB (35174174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58ce15bdaf8393f730650bdb74d7a2963b7503ea366f9de4be5b68c633d81275`  
		Last Modified: Thu, 24 Mar 2022 21:40:30 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b493f64efcabc5b7a1db60efe7e93a551ab1e074b3d9498f452976380cea43a9`  
		Last Modified: Thu, 24 Mar 2022 21:40:30 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baab4ad36cd20abcb753ab39c8cf427f3140da83c4691e198ad6512c50a002ce`  
		Last Modified: Thu, 24 Mar 2022 21:40:31 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.9-alpine`

```console
$ docker pull chronograf@sha256:f4f6fa974920811818dfb6c270d59bbe5d5bade68b0be74684cd994e79af8c10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.9-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:ef4cd3408c73d477551dfb72aaae2abdeed0b9b9a08d851bfa122561f91bdbe2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.8 MB (22786692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7596cd4f4cf4a22ac894e20298bb8b808de42e832647b9f14d53b8f9f23eccf2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 29 Mar 2022 00:19:41 GMT
ADD file:900b3c9d6bd18f94bde19b8eb177a55f956f4030deea9171e6c3da797a213636 in / 
# Tue, 29 Mar 2022 00:19:41 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 05:59:42 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 29 Mar 2022 05:59:43 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Tue, 29 Mar 2022 06:00:53 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Tue, 29 Mar 2022 06:00:58 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Tue, 29 Mar 2022 06:00:59 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 29 Mar 2022 06:00:59 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 29 Mar 2022 06:00:59 GMT
EXPOSE 8888
# Tue, 29 Mar 2022 06:00:59 GMT
VOLUME [/var/lib/chronograf]
# Tue, 29 Mar 2022 06:00:59 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Tue, 29 Mar 2022 06:00:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 29 Mar 2022 06:00:59 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:cfab2db722092277479ddd659049695fa8081d2a03c31b01d388cc21802de8b4`  
		Last Modified: Tue, 29 Mar 2022 00:20:33 GMT  
		Size: 2.8 MB (2818354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b8e4488850ad3e08f0aba8d339de3abde1e79494ff7d9a00067fa8b08eed46`  
		Last Modified: Tue, 29 Mar 2022 06:01:38 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f25991090eec670a7642f167cf12c22992033088ab88cc13dd27f5d7b50aada`  
		Last Modified: Tue, 29 Mar 2022 06:01:36 GMT  
		Size: 271.7 KB (271672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfaaa6fcac2260ec607ed995de50d7d5ae598edbea49cf4b31303459a61b14a9`  
		Last Modified: Tue, 29 Mar 2022 06:03:02 GMT  
		Size: 19.7 MB (19672108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1248964caea31424a9c33d7e3295221dddf0cfa49827d784f1042f9ef3b88fe2`  
		Last Modified: Tue, 29 Mar 2022 06:02:59 GMT  
		Size: 12.3 KB (12267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98c4c042f5251a173f8cc6bcef3590725b41eea4cdc97212885e03f5494638db`  
		Last Modified: Tue, 29 Mar 2022 06:03:00 GMT  
		Size: 11.9 KB (11900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4692a723f66a42998f49e22f718968845f26d3ed54349b437f08602d75640477`  
		Last Modified: Tue, 29 Mar 2022 06:02:59 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.9.4`

```console
$ docker pull chronograf@sha256:704f75c4a7355448058209d9ced2b71536e092ed744aa6727a3b1c27020026a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.9.4` - linux; amd64

```console
$ docker pull chronograf@sha256:15a99f7a300d2e041300009a3c364b1f724119fc299f8a40dd3b2882a282d4c5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.9 MB (66922847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53ba73fe4ae163f4ad5c16f29664af403847e437f25c9b8b050fcaa82533485a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 29 Mar 2022 00:24:14 GMT
ADD file:67d83164f6e419d116be47b3e915cea9beb88948f1656f3f0924f249ac2894f3 in / 
# Tue, 29 Mar 2022 00:24:14 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 05:59:28 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 29 Mar 2022 06:00:41 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Tue, 29 Mar 2022 06:00:50 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 29 Mar 2022 06:00:50 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 29 Mar 2022 06:00:50 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 29 Mar 2022 06:00:50 GMT
EXPOSE 8888
# Tue, 29 Mar 2022 06:00:50 GMT
VOLUME [/var/lib/chronograf]
# Tue, 29 Mar 2022 06:00:50 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 29 Mar 2022 06:00:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 29 Mar 2022 06:00:51 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:21fb02cbac852f4be42877e7b52e5eab70cd1991c41fad18656f46c684fe4868`  
		Last Modified: Tue, 29 Mar 2022 00:31:08 GMT  
		Size: 22.6 MB (22567695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56b9c16e1754e07f3324fc31da705ef8a61540f0c8d8cdb08f2d86425ca373af`  
		Last Modified: Tue, 29 Mar 2022 06:01:23 GMT  
		Size: 6.8 MB (6760319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0bda37b43acd0c440794a23a5765a56372231df70c41b2f64fa0a6c79871b02`  
		Last Modified: Tue, 29 Mar 2022 06:02:47 GMT  
		Size: 37.6 MB (37570449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e091fb54b38ba68b0e7fefb8249b3be64a9d3b07e389234811a38fcfca3add5c`  
		Last Modified: Tue, 29 Mar 2022 06:02:42 GMT  
		Size: 12.2 KB (12242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d3ce8d41d7dff561e4f28e9aefb93d548cc683ca81b47663e270c52105d08fe`  
		Last Modified: Tue, 29 Mar 2022 06:02:42 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1032cdb5990ddcf856cc28132155100914d3642debc19b29c32a217fece104e7`  
		Last Modified: Tue, 29 Mar 2022 06:02:42 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.9.4` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:bfeb7966a4c5fb1bf24eb18ba92d922624888cd3be110355b2c674d252a6389b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.5 MB (60456428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a33945351a002efc5f47a74cf82a21f244afa0dde4efc3637f0796513a7c9254`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 17 Mar 2022 09:36:59 GMT
ADD file:28d5a216145f4b0aa29a7151a22e6e7dab9d430006122bbed8b13f84ae55713e in / 
# Thu, 17 Mar 2022 09:37:00 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 02:42:06 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 24 Mar 2022 22:21:01 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Thu, 24 Mar 2022 22:21:20 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Thu, 24 Mar 2022 22:21:21 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 24 Mar 2022 22:21:21 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 24 Mar 2022 22:21:21 GMT
EXPOSE 8888
# Thu, 24 Mar 2022 22:21:22 GMT
VOLUME [/var/lib/chronograf]
# Thu, 24 Mar 2022 22:21:22 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Thu, 24 Mar 2022 22:21:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 24 Mar 2022 22:21:23 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:db6b474f79893f85b457aa5924e44453557a4b8963f5dbf6f78a60f93f73d19d`  
		Last Modified: Thu, 17 Mar 2022 09:53:37 GMT  
		Size: 19.4 MB (19359700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff6bf2997b6e0bfcc0741907bb7f1b0dcd194f8096745c677b23000d0147b16c`  
		Last Modified: Sat, 19 Mar 2022 02:45:56 GMT  
		Size: 5.8 MB (5780855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddb9109c6da475cc963f12be9c4a328783af849e0bd2ee79d85430d2a0614382`  
		Last Modified: Thu, 24 Mar 2022 22:22:43 GMT  
		Size: 35.3 MB (35291482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:119d602e1079d24260c1760a150c4d6bda21b42c978eb1e07e2e29f41a823e8b`  
		Last Modified: Thu, 24 Mar 2022 22:22:24 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93e4ee91a2464457151ba353133acb38787214c628cf5f0c767f814ea6e040af`  
		Last Modified: Thu, 24 Mar 2022 22:22:24 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7ce674455f2d68cfe0af6f9360d133c707a42f55e2e901082f06404aff9ced4`  
		Last Modified: Thu, 24 Mar 2022 22:22:24 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.9.4` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:6ad923beb75f1f8da1cd14a3e86204c8f4aa144608359dfa5cc54f9e6159ddee
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61669535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72bd3711653ee186a5445233af133b67624cbca85683492be81f37dfcaee3e43`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 17 Mar 2022 03:24:16 GMT
ADD file:9d9c04bf28d7e6075270ca8a75c01a6d4015bc3eccc4812a82681a7fabf27027 in / 
# Thu, 17 Mar 2022 03:24:17 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 22:26:56 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 24 Mar 2022 21:39:46 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Thu, 24 Mar 2022 21:39:55 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Thu, 24 Mar 2022 21:39:56 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 24 Mar 2022 21:39:57 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 24 Mar 2022 21:39:57 GMT
EXPOSE 8888
# Thu, 24 Mar 2022 21:39:58 GMT
VOLUME [/var/lib/chronograf]
# Thu, 24 Mar 2022 21:40:00 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Thu, 24 Mar 2022 21:40:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 24 Mar 2022 21:40:01 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:ecb1e7e01fa06e43b3018b38895366ba643cbac6d46bce566be2aa1cf10abf48`  
		Last Modified: Thu, 17 Mar 2022 03:32:58 GMT  
		Size: 20.4 MB (20423817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdcc9ed8b864108c2f441d508e2349d88968c42f8446c04f18fb121e256bd9bb`  
		Last Modified: Thu, 17 Mar 2022 22:29:15 GMT  
		Size: 6.0 MB (6047145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8693526e8c2799b835c31d42a7cdd67b1b354b5707b2ccc44c885949036ebad9`  
		Last Modified: Thu, 24 Mar 2022 21:40:35 GMT  
		Size: 35.2 MB (35174174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58ce15bdaf8393f730650bdb74d7a2963b7503ea366f9de4be5b68c633d81275`  
		Last Modified: Thu, 24 Mar 2022 21:40:30 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b493f64efcabc5b7a1db60efe7e93a551ab1e074b3d9498f452976380cea43a9`  
		Last Modified: Thu, 24 Mar 2022 21:40:30 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baab4ad36cd20abcb753ab39c8cf427f3140da83c4691e198ad6512c50a002ce`  
		Last Modified: Thu, 24 Mar 2022 21:40:31 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.9.4-alpine`

```console
$ docker pull chronograf@sha256:f4f6fa974920811818dfb6c270d59bbe5d5bade68b0be74684cd994e79af8c10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.9.4-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:ef4cd3408c73d477551dfb72aaae2abdeed0b9b9a08d851bfa122561f91bdbe2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.8 MB (22786692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7596cd4f4cf4a22ac894e20298bb8b808de42e832647b9f14d53b8f9f23eccf2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 29 Mar 2022 00:19:41 GMT
ADD file:900b3c9d6bd18f94bde19b8eb177a55f956f4030deea9171e6c3da797a213636 in / 
# Tue, 29 Mar 2022 00:19:41 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 05:59:42 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 29 Mar 2022 05:59:43 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Tue, 29 Mar 2022 06:00:53 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Tue, 29 Mar 2022 06:00:58 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Tue, 29 Mar 2022 06:00:59 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 29 Mar 2022 06:00:59 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 29 Mar 2022 06:00:59 GMT
EXPOSE 8888
# Tue, 29 Mar 2022 06:00:59 GMT
VOLUME [/var/lib/chronograf]
# Tue, 29 Mar 2022 06:00:59 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Tue, 29 Mar 2022 06:00:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 29 Mar 2022 06:00:59 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:cfab2db722092277479ddd659049695fa8081d2a03c31b01d388cc21802de8b4`  
		Last Modified: Tue, 29 Mar 2022 00:20:33 GMT  
		Size: 2.8 MB (2818354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b8e4488850ad3e08f0aba8d339de3abde1e79494ff7d9a00067fa8b08eed46`  
		Last Modified: Tue, 29 Mar 2022 06:01:38 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f25991090eec670a7642f167cf12c22992033088ab88cc13dd27f5d7b50aada`  
		Last Modified: Tue, 29 Mar 2022 06:01:36 GMT  
		Size: 271.7 KB (271672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfaaa6fcac2260ec607ed995de50d7d5ae598edbea49cf4b31303459a61b14a9`  
		Last Modified: Tue, 29 Mar 2022 06:03:02 GMT  
		Size: 19.7 MB (19672108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1248964caea31424a9c33d7e3295221dddf0cfa49827d784f1042f9ef3b88fe2`  
		Last Modified: Tue, 29 Mar 2022 06:02:59 GMT  
		Size: 12.3 KB (12267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98c4c042f5251a173f8cc6bcef3590725b41eea4cdc97212885e03f5494638db`  
		Last Modified: Tue, 29 Mar 2022 06:03:00 GMT  
		Size: 11.9 KB (11900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4692a723f66a42998f49e22f718968845f26d3ed54349b437f08602d75640477`  
		Last Modified: Tue, 29 Mar 2022 06:02:59 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:alpine`

```console
$ docker pull chronograf@sha256:f4f6fa974920811818dfb6c270d59bbe5d5bade68b0be74684cd994e79af8c10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:ef4cd3408c73d477551dfb72aaae2abdeed0b9b9a08d851bfa122561f91bdbe2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.8 MB (22786692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7596cd4f4cf4a22ac894e20298bb8b808de42e832647b9f14d53b8f9f23eccf2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 29 Mar 2022 00:19:41 GMT
ADD file:900b3c9d6bd18f94bde19b8eb177a55f956f4030deea9171e6c3da797a213636 in / 
# Tue, 29 Mar 2022 00:19:41 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 05:59:42 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 29 Mar 2022 05:59:43 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Tue, 29 Mar 2022 06:00:53 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Tue, 29 Mar 2022 06:00:58 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Tue, 29 Mar 2022 06:00:59 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 29 Mar 2022 06:00:59 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 29 Mar 2022 06:00:59 GMT
EXPOSE 8888
# Tue, 29 Mar 2022 06:00:59 GMT
VOLUME [/var/lib/chronograf]
# Tue, 29 Mar 2022 06:00:59 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Tue, 29 Mar 2022 06:00:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 29 Mar 2022 06:00:59 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:cfab2db722092277479ddd659049695fa8081d2a03c31b01d388cc21802de8b4`  
		Last Modified: Tue, 29 Mar 2022 00:20:33 GMT  
		Size: 2.8 MB (2818354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b8e4488850ad3e08f0aba8d339de3abde1e79494ff7d9a00067fa8b08eed46`  
		Last Modified: Tue, 29 Mar 2022 06:01:38 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f25991090eec670a7642f167cf12c22992033088ab88cc13dd27f5d7b50aada`  
		Last Modified: Tue, 29 Mar 2022 06:01:36 GMT  
		Size: 271.7 KB (271672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfaaa6fcac2260ec607ed995de50d7d5ae598edbea49cf4b31303459a61b14a9`  
		Last Modified: Tue, 29 Mar 2022 06:03:02 GMT  
		Size: 19.7 MB (19672108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1248964caea31424a9c33d7e3295221dddf0cfa49827d784f1042f9ef3b88fe2`  
		Last Modified: Tue, 29 Mar 2022 06:02:59 GMT  
		Size: 12.3 KB (12267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98c4c042f5251a173f8cc6bcef3590725b41eea4cdc97212885e03f5494638db`  
		Last Modified: Tue, 29 Mar 2022 06:03:00 GMT  
		Size: 11.9 KB (11900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4692a723f66a42998f49e22f718968845f26d3ed54349b437f08602d75640477`  
		Last Modified: Tue, 29 Mar 2022 06:02:59 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:latest`

```console
$ docker pull chronograf@sha256:704f75c4a7355448058209d9ced2b71536e092ed744aa6727a3b1c27020026a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:latest` - linux; amd64

```console
$ docker pull chronograf@sha256:15a99f7a300d2e041300009a3c364b1f724119fc299f8a40dd3b2882a282d4c5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.9 MB (66922847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53ba73fe4ae163f4ad5c16f29664af403847e437f25c9b8b050fcaa82533485a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 29 Mar 2022 00:24:14 GMT
ADD file:67d83164f6e419d116be47b3e915cea9beb88948f1656f3f0924f249ac2894f3 in / 
# Tue, 29 Mar 2022 00:24:14 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 05:59:28 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 29 Mar 2022 06:00:41 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Tue, 29 Mar 2022 06:00:50 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 29 Mar 2022 06:00:50 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 29 Mar 2022 06:00:50 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 29 Mar 2022 06:00:50 GMT
EXPOSE 8888
# Tue, 29 Mar 2022 06:00:50 GMT
VOLUME [/var/lib/chronograf]
# Tue, 29 Mar 2022 06:00:50 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 29 Mar 2022 06:00:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 29 Mar 2022 06:00:51 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:21fb02cbac852f4be42877e7b52e5eab70cd1991c41fad18656f46c684fe4868`  
		Last Modified: Tue, 29 Mar 2022 00:31:08 GMT  
		Size: 22.6 MB (22567695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56b9c16e1754e07f3324fc31da705ef8a61540f0c8d8cdb08f2d86425ca373af`  
		Last Modified: Tue, 29 Mar 2022 06:01:23 GMT  
		Size: 6.8 MB (6760319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0bda37b43acd0c440794a23a5765a56372231df70c41b2f64fa0a6c79871b02`  
		Last Modified: Tue, 29 Mar 2022 06:02:47 GMT  
		Size: 37.6 MB (37570449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e091fb54b38ba68b0e7fefb8249b3be64a9d3b07e389234811a38fcfca3add5c`  
		Last Modified: Tue, 29 Mar 2022 06:02:42 GMT  
		Size: 12.2 KB (12242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d3ce8d41d7dff561e4f28e9aefb93d548cc683ca81b47663e270c52105d08fe`  
		Last Modified: Tue, 29 Mar 2022 06:02:42 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1032cdb5990ddcf856cc28132155100914d3642debc19b29c32a217fece104e7`  
		Last Modified: Tue, 29 Mar 2022 06:02:42 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:latest` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:bfeb7966a4c5fb1bf24eb18ba92d922624888cd3be110355b2c674d252a6389b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.5 MB (60456428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a33945351a002efc5f47a74cf82a21f244afa0dde4efc3637f0796513a7c9254`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 17 Mar 2022 09:36:59 GMT
ADD file:28d5a216145f4b0aa29a7151a22e6e7dab9d430006122bbed8b13f84ae55713e in / 
# Thu, 17 Mar 2022 09:37:00 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 02:42:06 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 24 Mar 2022 22:21:01 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Thu, 24 Mar 2022 22:21:20 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Thu, 24 Mar 2022 22:21:21 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 24 Mar 2022 22:21:21 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 24 Mar 2022 22:21:21 GMT
EXPOSE 8888
# Thu, 24 Mar 2022 22:21:22 GMT
VOLUME [/var/lib/chronograf]
# Thu, 24 Mar 2022 22:21:22 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Thu, 24 Mar 2022 22:21:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 24 Mar 2022 22:21:23 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:db6b474f79893f85b457aa5924e44453557a4b8963f5dbf6f78a60f93f73d19d`  
		Last Modified: Thu, 17 Mar 2022 09:53:37 GMT  
		Size: 19.4 MB (19359700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff6bf2997b6e0bfcc0741907bb7f1b0dcd194f8096745c677b23000d0147b16c`  
		Last Modified: Sat, 19 Mar 2022 02:45:56 GMT  
		Size: 5.8 MB (5780855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddb9109c6da475cc963f12be9c4a328783af849e0bd2ee79d85430d2a0614382`  
		Last Modified: Thu, 24 Mar 2022 22:22:43 GMT  
		Size: 35.3 MB (35291482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:119d602e1079d24260c1760a150c4d6bda21b42c978eb1e07e2e29f41a823e8b`  
		Last Modified: Thu, 24 Mar 2022 22:22:24 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93e4ee91a2464457151ba353133acb38787214c628cf5f0c767f814ea6e040af`  
		Last Modified: Thu, 24 Mar 2022 22:22:24 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7ce674455f2d68cfe0af6f9360d133c707a42f55e2e901082f06404aff9ced4`  
		Last Modified: Thu, 24 Mar 2022 22:22:24 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:latest` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:6ad923beb75f1f8da1cd14a3e86204c8f4aa144608359dfa5cc54f9e6159ddee
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61669535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72bd3711653ee186a5445233af133b67624cbca85683492be81f37dfcaee3e43`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 17 Mar 2022 03:24:16 GMT
ADD file:9d9c04bf28d7e6075270ca8a75c01a6d4015bc3eccc4812a82681a7fabf27027 in / 
# Thu, 17 Mar 2022 03:24:17 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 22:26:56 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 24 Mar 2022 21:39:46 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Thu, 24 Mar 2022 21:39:55 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Thu, 24 Mar 2022 21:39:56 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 24 Mar 2022 21:39:57 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 24 Mar 2022 21:39:57 GMT
EXPOSE 8888
# Thu, 24 Mar 2022 21:39:58 GMT
VOLUME [/var/lib/chronograf]
# Thu, 24 Mar 2022 21:40:00 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Thu, 24 Mar 2022 21:40:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 24 Mar 2022 21:40:01 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:ecb1e7e01fa06e43b3018b38895366ba643cbac6d46bce566be2aa1cf10abf48`  
		Last Modified: Thu, 17 Mar 2022 03:32:58 GMT  
		Size: 20.4 MB (20423817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdcc9ed8b864108c2f441d508e2349d88968c42f8446c04f18fb121e256bd9bb`  
		Last Modified: Thu, 17 Mar 2022 22:29:15 GMT  
		Size: 6.0 MB (6047145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8693526e8c2799b835c31d42a7cdd67b1b354b5707b2ccc44c885949036ebad9`  
		Last Modified: Thu, 24 Mar 2022 21:40:35 GMT  
		Size: 35.2 MB (35174174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58ce15bdaf8393f730650bdb74d7a2963b7503ea366f9de4be5b68c633d81275`  
		Last Modified: Thu, 24 Mar 2022 21:40:30 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b493f64efcabc5b7a1db60efe7e93a551ab1e074b3d9498f452976380cea43a9`  
		Last Modified: Thu, 24 Mar 2022 21:40:30 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baab4ad36cd20abcb753ab39c8cf427f3140da83c4691e198ad6512c50a002ce`  
		Last Modified: Thu, 24 Mar 2022 21:40:31 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
