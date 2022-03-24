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
$ docker pull chronograf@sha256:8fcaa315cd224fa198a5103a167b71068715119898c99b58c21ba8835377780b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.6` - linux; amd64

```console
$ docker pull chronograf@sha256:93f47a1cbb8c6d0280a105d82da3f08c16dbd594c0f83f755ab9a6de125ac5e6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49398093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b50e92ef46146f03f27e63a296e018c488235b060c70322a76547b785ee22249`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 17 Mar 2022 04:06:48 GMT
ADD file:9fc739b295073dd1d9293d2ea8106e21156de790c82a9d19be210c0c63bfb527 in / 
# Thu, 17 Mar 2022 04:06:48 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 08:38:22 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 17 Mar 2022 08:38:22 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Thu, 17 Mar 2022 08:38:30 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Thu, 17 Mar 2022 08:38:30 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 17 Mar 2022 08:38:31 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 17 Mar 2022 08:38:31 GMT
EXPOSE 8888
# Thu, 17 Mar 2022 08:38:31 GMT
VOLUME [/var/lib/chronograf]
# Thu, 17 Mar 2022 08:38:31 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Thu, 17 Mar 2022 08:38:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 17 Mar 2022 08:38:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:5d9da879a61c05a35520eabaa04d22b4867d0cf84a91f4c7b078128e1c820ce5`  
		Last Modified: Thu, 17 Mar 2022 04:14:03 GMT  
		Size: 22.6 MB (22567740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:964f48dfa9fa2029216316deab45629f6c3afbc5021d72278ae08424dd0774b0`  
		Last Modified: Thu, 17 Mar 2022 08:40:28 GMT  
		Size: 6.8 MB (6760337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:720123d698908d3e60989ef3cfe84d0c107ec7145b33009d067b420bd45f2ee2`  
		Last Modified: Thu, 17 Mar 2022 08:40:30 GMT  
		Size: 20.0 MB (20045618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa28a36515fe8774f75f7786b2b5c40633a4c6ba62dfa2da92eeb02c0e26eec3`  
		Last Modified: Thu, 17 Mar 2022 08:40:26 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3d20de19d9d79907dedb1c3aa3c0494ff3db6e315756997f058b8824deb9735`  
		Last Modified: Thu, 17 Mar 2022 08:40:27 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bed760e0aae03c7d7dfcb33f876744360ae56125660c9b220ba0b5d1c160b70a`  
		Last Modified: Thu, 17 Mar 2022 08:40:26 GMT  
		Size: 240.0 B  
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
$ docker pull chronograf@sha256:bded7a49782e19df945fa2949eb03d1a2c6186774a3109211625f73046ffbb47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.6-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:71348f7940298a266f4a8c6aa98be0814f0b8e8f52445cdf919692ffb9448a14
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14850230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36909736792b033c5743358080825a56508649173c26849796faa7cc3f68b660`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 17 Mar 2022 15:19:26 GMT
ADD file:8ec3735d4b1b4b070607b94e3bd360117b07dc26e1baf5dd485b49b3413e8fff in / 
# Thu, 17 Mar 2022 15:19:26 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 18:05:42 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 17 Mar 2022 18:05:43 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Sat, 19 Mar 2022 00:56:17 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Sat, 19 Mar 2022 00:57:01 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Sat, 19 Mar 2022 00:57:01 GMT
COPY file:aa4a9d01295c7013d89da92a943af071556aea6dbe6269affd4664fdd86969b8 in /usr/share/chronograf/LICENSE 
# Sat, 19 Mar 2022 00:57:01 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sat, 19 Mar 2022 00:57:01 GMT
EXPOSE 8888
# Sat, 19 Mar 2022 00:57:01 GMT
VOLUME [/var/lib/chronograf]
# Sat, 19 Mar 2022 00:57:02 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Sat, 19 Mar 2022 00:57:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 19 Mar 2022 00:57:02 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:36ccefbf3d8a9a1b18baaa9cbf0f3ad50e8a7b751656c74df359900a318cbffc`  
		Last Modified: Thu, 17 Mar 2022 15:20:13 GMT  
		Size: 2.8 MB (2816169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffa1326b35d047e371043a2411e65bd818c27909ab1ecf1ce37b55741744e890`  
		Last Modified: Thu, 17 Mar 2022 18:07:13 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85eb6277290b589d592446e2f538670a432e8a6e60772ee08f89a2055bef71ec`  
		Last Modified: Thu, 17 Mar 2022 18:07:13 GMT  
		Size: 271.7 KB (271670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:435edd5df7168c6f360481b804c69d3991e9ce24c7d6933dd2bdec465b9c298b`  
		Last Modified: Sat, 19 Mar 2022 01:00:16 GMT  
		Size: 11.7 MB (11737829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa0263051770a8d669f13f3e8c3f14711eeb03c4d30fbcf312329d74c9dbaa79`  
		Last Modified: Sat, 19 Mar 2022 01:00:13 GMT  
		Size: 12.3 KB (12272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c2ac2a7fc338b67daafd0b489122ff30b9ee9b3e429ea5c349d5264e4d3c1ec`  
		Last Modified: Sat, 19 Mar 2022 01:00:13 GMT  
		Size: 11.9 KB (11899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16074735b27ff79bda7204f254f75acaed8c8bac21fc31b5ac62a650c3a2efa2`  
		Last Modified: Sat, 19 Mar 2022 01:00:13 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.6.2`

```console
$ docker pull chronograf@sha256:8fcaa315cd224fa198a5103a167b71068715119898c99b58c21ba8835377780b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.6.2` - linux; amd64

```console
$ docker pull chronograf@sha256:93f47a1cbb8c6d0280a105d82da3f08c16dbd594c0f83f755ab9a6de125ac5e6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49398093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b50e92ef46146f03f27e63a296e018c488235b060c70322a76547b785ee22249`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 17 Mar 2022 04:06:48 GMT
ADD file:9fc739b295073dd1d9293d2ea8106e21156de790c82a9d19be210c0c63bfb527 in / 
# Thu, 17 Mar 2022 04:06:48 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 08:38:22 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 17 Mar 2022 08:38:22 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Thu, 17 Mar 2022 08:38:30 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Thu, 17 Mar 2022 08:38:30 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 17 Mar 2022 08:38:31 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 17 Mar 2022 08:38:31 GMT
EXPOSE 8888
# Thu, 17 Mar 2022 08:38:31 GMT
VOLUME [/var/lib/chronograf]
# Thu, 17 Mar 2022 08:38:31 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Thu, 17 Mar 2022 08:38:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 17 Mar 2022 08:38:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:5d9da879a61c05a35520eabaa04d22b4867d0cf84a91f4c7b078128e1c820ce5`  
		Last Modified: Thu, 17 Mar 2022 04:14:03 GMT  
		Size: 22.6 MB (22567740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:964f48dfa9fa2029216316deab45629f6c3afbc5021d72278ae08424dd0774b0`  
		Last Modified: Thu, 17 Mar 2022 08:40:28 GMT  
		Size: 6.8 MB (6760337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:720123d698908d3e60989ef3cfe84d0c107ec7145b33009d067b420bd45f2ee2`  
		Last Modified: Thu, 17 Mar 2022 08:40:30 GMT  
		Size: 20.0 MB (20045618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa28a36515fe8774f75f7786b2b5c40633a4c6ba62dfa2da92eeb02c0e26eec3`  
		Last Modified: Thu, 17 Mar 2022 08:40:26 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3d20de19d9d79907dedb1c3aa3c0494ff3db6e315756997f058b8824deb9735`  
		Last Modified: Thu, 17 Mar 2022 08:40:27 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bed760e0aae03c7d7dfcb33f876744360ae56125660c9b220ba0b5d1c160b70a`  
		Last Modified: Thu, 17 Mar 2022 08:40:26 GMT  
		Size: 240.0 B  
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
$ docker pull chronograf@sha256:bded7a49782e19df945fa2949eb03d1a2c6186774a3109211625f73046ffbb47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.6.2-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:71348f7940298a266f4a8c6aa98be0814f0b8e8f52445cdf919692ffb9448a14
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14850230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36909736792b033c5743358080825a56508649173c26849796faa7cc3f68b660`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 17 Mar 2022 15:19:26 GMT
ADD file:8ec3735d4b1b4b070607b94e3bd360117b07dc26e1baf5dd485b49b3413e8fff in / 
# Thu, 17 Mar 2022 15:19:26 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 18:05:42 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 17 Mar 2022 18:05:43 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Sat, 19 Mar 2022 00:56:17 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Sat, 19 Mar 2022 00:57:01 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Sat, 19 Mar 2022 00:57:01 GMT
COPY file:aa4a9d01295c7013d89da92a943af071556aea6dbe6269affd4664fdd86969b8 in /usr/share/chronograf/LICENSE 
# Sat, 19 Mar 2022 00:57:01 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sat, 19 Mar 2022 00:57:01 GMT
EXPOSE 8888
# Sat, 19 Mar 2022 00:57:01 GMT
VOLUME [/var/lib/chronograf]
# Sat, 19 Mar 2022 00:57:02 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Sat, 19 Mar 2022 00:57:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 19 Mar 2022 00:57:02 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:36ccefbf3d8a9a1b18baaa9cbf0f3ad50e8a7b751656c74df359900a318cbffc`  
		Last Modified: Thu, 17 Mar 2022 15:20:13 GMT  
		Size: 2.8 MB (2816169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffa1326b35d047e371043a2411e65bd818c27909ab1ecf1ce37b55741744e890`  
		Last Modified: Thu, 17 Mar 2022 18:07:13 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85eb6277290b589d592446e2f538670a432e8a6e60772ee08f89a2055bef71ec`  
		Last Modified: Thu, 17 Mar 2022 18:07:13 GMT  
		Size: 271.7 KB (271670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:435edd5df7168c6f360481b804c69d3991e9ce24c7d6933dd2bdec465b9c298b`  
		Last Modified: Sat, 19 Mar 2022 01:00:16 GMT  
		Size: 11.7 MB (11737829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa0263051770a8d669f13f3e8c3f14711eeb03c4d30fbcf312329d74c9dbaa79`  
		Last Modified: Sat, 19 Mar 2022 01:00:13 GMT  
		Size: 12.3 KB (12272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c2ac2a7fc338b67daafd0b489122ff30b9ee9b3e429ea5c349d5264e4d3c1ec`  
		Last Modified: Sat, 19 Mar 2022 01:00:13 GMT  
		Size: 11.9 KB (11899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16074735b27ff79bda7204f254f75acaed8c8bac21fc31b5ac62a650c3a2efa2`  
		Last Modified: Sat, 19 Mar 2022 01:00:13 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.7`

```console
$ docker pull chronograf@sha256:63689980752a3de977b03610e5e1e933ad62b1ae05cae980b213d191f62c8a6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.7` - linux; amd64

```console
$ docker pull chronograf@sha256:ac2e6b46c9ee9427253ba61e75c7d4958aa3f2e1203674c83b62e09f5e5ab66e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.4 MB (65427515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e4e41c259365180de65f434878ea9288fc959b07737d4fc59184f084ef2f6be`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 17 Mar 2022 04:06:48 GMT
ADD file:9fc739b295073dd1d9293d2ea8106e21156de790c82a9d19be210c0c63bfb527 in / 
# Thu, 17 Mar 2022 04:06:48 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 08:39:21 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 17 Mar 2022 08:39:21 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Thu, 17 Mar 2022 08:39:32 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Thu, 17 Mar 2022 08:39:32 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 17 Mar 2022 08:39:32 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 17 Mar 2022 08:39:32 GMT
EXPOSE 8888
# Thu, 17 Mar 2022 08:39:33 GMT
VOLUME [/var/lib/chronograf]
# Thu, 17 Mar 2022 08:39:33 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Thu, 17 Mar 2022 08:39:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 17 Mar 2022 08:39:33 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:5d9da879a61c05a35520eabaa04d22b4867d0cf84a91f4c7b078128e1c820ce5`  
		Last Modified: Thu, 17 Mar 2022 04:14:03 GMT  
		Size: 22.6 MB (22567740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0be2fb68be12739fe6fae16faf55148e9959d78683503adcca5929815df1a83`  
		Last Modified: Thu, 17 Mar 2022 08:40:42 GMT  
		Size: 4.5 MB (4506805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59c3593347da1932911bccf1dc271e1cf2719319c5c1a0537b72564f0310cc7d`  
		Last Modified: Thu, 17 Mar 2022 08:40:47 GMT  
		Size: 38.3 MB (38328573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45a2d8a1f30cc86cfd9dde2f4513fa66883f64f0f7c68a4ea6c21ecb4bd3b11e`  
		Last Modified: Thu, 17 Mar 2022 08:40:41 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecdfbe73fc67ee76cc610c7e1ab4812943cdd5c9b082942d2d2154b38f1db8f7`  
		Last Modified: Thu, 17 Mar 2022 08:40:41 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a55f867bbe20ef4e91e10dc00738edae0eeaebfff2490acbcc9b10f211596fc`  
		Last Modified: Thu, 17 Mar 2022 08:40:41 GMT  
		Size: 239.0 B  
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
$ docker pull chronograf@sha256:4bd3a7e38a02cbe8a6f3d906059aa7eef301c0daa975c0276607d10c6adbba78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.7-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:0c44e7fe83c8b98aca18798ec7fc10e401aaa48552849f30cd284bb0e5e5c497
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22668629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ddd274f048917d5491568d0cc03d752e7c6977df022b06b0e165ac55f5295a5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 17 Mar 2022 15:19:26 GMT
ADD file:8ec3735d4b1b4b070607b94e3bd360117b07dc26e1baf5dd485b49b3413e8fff in / 
# Thu, 17 Mar 2022 15:19:26 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 18:05:42 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 17 Mar 2022 18:05:43 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Sat, 19 Mar 2022 00:57:07 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Sat, 19 Mar 2022 00:57:51 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Sat, 19 Mar 2022 00:57:52 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Sat, 19 Mar 2022 00:57:52 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sat, 19 Mar 2022 00:57:53 GMT
EXPOSE 8888
# Sat, 19 Mar 2022 00:57:53 GMT
VOLUME [/var/lib/chronograf]
# Sat, 19 Mar 2022 00:57:53 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Sat, 19 Mar 2022 00:57:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 19 Mar 2022 00:57:54 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:36ccefbf3d8a9a1b18baaa9cbf0f3ad50e8a7b751656c74df359900a318cbffc`  
		Last Modified: Thu, 17 Mar 2022 15:20:13 GMT  
		Size: 2.8 MB (2816169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffa1326b35d047e371043a2411e65bd818c27909ab1ecf1ce37b55741744e890`  
		Last Modified: Thu, 17 Mar 2022 18:07:13 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85eb6277290b589d592446e2f538670a432e8a6e60772ee08f89a2055bef71ec`  
		Last Modified: Thu, 17 Mar 2022 18:07:13 GMT  
		Size: 271.7 KB (271670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7543bdb548197b45794168343be8aa9ca1ccaa697e3bc04cb61aa54d56f16bee`  
		Last Modified: Sat, 19 Mar 2022 01:00:33 GMT  
		Size: 19.6 MB (19556234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4a95212b6d1425acc216b53163bddde5369cf1c701457150de5b51ec7778451`  
		Last Modified: Sat, 19 Mar 2022 01:00:27 GMT  
		Size: 12.3 KB (12265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:376c57a9b9aa1e0fa676aa3787ed7d646b608a70ab31db1c2defe2409d995db0`  
		Last Modified: Sat, 19 Mar 2022 01:00:27 GMT  
		Size: 11.9 KB (11900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0e2ad696e43ae65e2c07cc4c668b49f3ea83933f5aa3079b6ae3bb96a08c564`  
		Last Modified: Sat, 19 Mar 2022 01:00:27 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.7.17`

```console
$ docker pull chronograf@sha256:63689980752a3de977b03610e5e1e933ad62b1ae05cae980b213d191f62c8a6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.7.17` - linux; amd64

```console
$ docker pull chronograf@sha256:ac2e6b46c9ee9427253ba61e75c7d4958aa3f2e1203674c83b62e09f5e5ab66e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.4 MB (65427515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e4e41c259365180de65f434878ea9288fc959b07737d4fc59184f084ef2f6be`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 17 Mar 2022 04:06:48 GMT
ADD file:9fc739b295073dd1d9293d2ea8106e21156de790c82a9d19be210c0c63bfb527 in / 
# Thu, 17 Mar 2022 04:06:48 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 08:39:21 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 17 Mar 2022 08:39:21 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Thu, 17 Mar 2022 08:39:32 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Thu, 17 Mar 2022 08:39:32 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 17 Mar 2022 08:39:32 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 17 Mar 2022 08:39:32 GMT
EXPOSE 8888
# Thu, 17 Mar 2022 08:39:33 GMT
VOLUME [/var/lib/chronograf]
# Thu, 17 Mar 2022 08:39:33 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Thu, 17 Mar 2022 08:39:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 17 Mar 2022 08:39:33 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:5d9da879a61c05a35520eabaa04d22b4867d0cf84a91f4c7b078128e1c820ce5`  
		Last Modified: Thu, 17 Mar 2022 04:14:03 GMT  
		Size: 22.6 MB (22567740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0be2fb68be12739fe6fae16faf55148e9959d78683503adcca5929815df1a83`  
		Last Modified: Thu, 17 Mar 2022 08:40:42 GMT  
		Size: 4.5 MB (4506805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59c3593347da1932911bccf1dc271e1cf2719319c5c1a0537b72564f0310cc7d`  
		Last Modified: Thu, 17 Mar 2022 08:40:47 GMT  
		Size: 38.3 MB (38328573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45a2d8a1f30cc86cfd9dde2f4513fa66883f64f0f7c68a4ea6c21ecb4bd3b11e`  
		Last Modified: Thu, 17 Mar 2022 08:40:41 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecdfbe73fc67ee76cc610c7e1ab4812943cdd5c9b082942d2d2154b38f1db8f7`  
		Last Modified: Thu, 17 Mar 2022 08:40:41 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a55f867bbe20ef4e91e10dc00738edae0eeaebfff2490acbcc9b10f211596fc`  
		Last Modified: Thu, 17 Mar 2022 08:40:41 GMT  
		Size: 239.0 B  
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
$ docker pull chronograf@sha256:4bd3a7e38a02cbe8a6f3d906059aa7eef301c0daa975c0276607d10c6adbba78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.7.17-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:0c44e7fe83c8b98aca18798ec7fc10e401aaa48552849f30cd284bb0e5e5c497
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22668629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ddd274f048917d5491568d0cc03d752e7c6977df022b06b0e165ac55f5295a5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 17 Mar 2022 15:19:26 GMT
ADD file:8ec3735d4b1b4b070607b94e3bd360117b07dc26e1baf5dd485b49b3413e8fff in / 
# Thu, 17 Mar 2022 15:19:26 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 18:05:42 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 17 Mar 2022 18:05:43 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Sat, 19 Mar 2022 00:57:07 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Sat, 19 Mar 2022 00:57:51 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Sat, 19 Mar 2022 00:57:52 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Sat, 19 Mar 2022 00:57:52 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sat, 19 Mar 2022 00:57:53 GMT
EXPOSE 8888
# Sat, 19 Mar 2022 00:57:53 GMT
VOLUME [/var/lib/chronograf]
# Sat, 19 Mar 2022 00:57:53 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Sat, 19 Mar 2022 00:57:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 19 Mar 2022 00:57:54 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:36ccefbf3d8a9a1b18baaa9cbf0f3ad50e8a7b751656c74df359900a318cbffc`  
		Last Modified: Thu, 17 Mar 2022 15:20:13 GMT  
		Size: 2.8 MB (2816169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffa1326b35d047e371043a2411e65bd818c27909ab1ecf1ce37b55741744e890`  
		Last Modified: Thu, 17 Mar 2022 18:07:13 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85eb6277290b589d592446e2f538670a432e8a6e60772ee08f89a2055bef71ec`  
		Last Modified: Thu, 17 Mar 2022 18:07:13 GMT  
		Size: 271.7 KB (271670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7543bdb548197b45794168343be8aa9ca1ccaa697e3bc04cb61aa54d56f16bee`  
		Last Modified: Sat, 19 Mar 2022 01:00:33 GMT  
		Size: 19.6 MB (19556234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4a95212b6d1425acc216b53163bddde5369cf1c701457150de5b51ec7778451`  
		Last Modified: Sat, 19 Mar 2022 01:00:27 GMT  
		Size: 12.3 KB (12265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:376c57a9b9aa1e0fa676aa3787ed7d646b608a70ab31db1c2defe2409d995db0`  
		Last Modified: Sat, 19 Mar 2022 01:00:27 GMT  
		Size: 11.9 KB (11900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0e2ad696e43ae65e2c07cc4c668b49f3ea83933f5aa3079b6ae3bb96a08c564`  
		Last Modified: Sat, 19 Mar 2022 01:00:27 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.8`

```console
$ docker pull chronograf@sha256:d99e0ec07af2fe60bfbd86456f69cef1fbeaac82eaf3bc1d287d2703379a39a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.8` - linux; amd64

```console
$ docker pull chronograf@sha256:71720adff754f47be799c56494fd8e15eb2fda0f58fac358b2f5a8c84f035c6a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66279024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70ddb8df4a909d55e224c1f58d665520efb4de5f348d75aa9a8d80aa4610020a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 17 Mar 2022 04:06:48 GMT
ADD file:9fc739b295073dd1d9293d2ea8106e21156de790c82a9d19be210c0c63bfb527 in / 
# Thu, 17 Mar 2022 04:06:48 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 08:38:22 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 17 Mar 2022 08:39:38 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Thu, 17 Mar 2022 08:39:46 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Thu, 17 Mar 2022 08:39:46 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 17 Mar 2022 08:39:46 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 17 Mar 2022 08:39:46 GMT
EXPOSE 8888
# Thu, 17 Mar 2022 08:39:46 GMT
VOLUME [/var/lib/chronograf]
# Thu, 17 Mar 2022 08:39:46 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Thu, 17 Mar 2022 08:39:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 17 Mar 2022 08:39:46 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:5d9da879a61c05a35520eabaa04d22b4867d0cf84a91f4c7b078128e1c820ce5`  
		Last Modified: Thu, 17 Mar 2022 04:14:03 GMT  
		Size: 22.6 MB (22567740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:964f48dfa9fa2029216316deab45629f6c3afbc5021d72278ae08424dd0774b0`  
		Last Modified: Thu, 17 Mar 2022 08:40:28 GMT  
		Size: 6.8 MB (6760337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef0628cff5565c1b1d727f5fb38edc6a84c913e1937bd7f4859e77e54b35d42d`  
		Last Modified: Thu, 17 Mar 2022 08:41:03 GMT  
		Size: 36.9 MB (36926565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2342aa887107fc7ca17bfbab46a2f800ceace0f64399cd9c4fa0c005ec7f3897`  
		Last Modified: Thu, 17 Mar 2022 08:40:58 GMT  
		Size: 12.2 KB (12242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66e69d5532f76bba0cc882567ce4e49ae883248b1a3b236ce63464ee892d90d6`  
		Last Modified: Thu, 17 Mar 2022 08:40:58 GMT  
		Size: 11.9 KB (11901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62b4060dfa2d51e4e395bd3c6ac9e6aa088edd5fa71ceabd978ce37d2067f8c8`  
		Last Modified: Thu, 17 Mar 2022 08:40:58 GMT  
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
$ docker pull chronograf@sha256:0d6beb1f2713a42997d2ce44c127ccf87d438357351308125b9c4aa54324d0df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.8-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:fd32b003c95265983c7fdf485622e1a7937f36bb6249fbd1a5fc39d5d72904b2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.3 MB (22316342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbf8d9aa814b6ccb2b8192ac18b512d5cf6161dfb066d657917183e5bfacffa3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 17 Mar 2022 15:19:26 GMT
ADD file:8ec3735d4b1b4b070607b94e3bd360117b07dc26e1baf5dd485b49b3413e8fff in / 
# Thu, 17 Mar 2022 15:19:26 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 18:05:42 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 17 Mar 2022 18:05:43 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Sat, 19 Mar 2022 00:58:09 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Sat, 19 Mar 2022 00:58:50 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Sat, 19 Mar 2022 00:58:50 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Sat, 19 Mar 2022 00:58:51 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sat, 19 Mar 2022 00:58:51 GMT
EXPOSE 8888
# Sat, 19 Mar 2022 00:58:51 GMT
VOLUME [/var/lib/chronograf]
# Sat, 19 Mar 2022 00:58:51 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Sat, 19 Mar 2022 00:58:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 19 Mar 2022 00:58:51 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:36ccefbf3d8a9a1b18baaa9cbf0f3ad50e8a7b751656c74df359900a318cbffc`  
		Last Modified: Thu, 17 Mar 2022 15:20:13 GMT  
		Size: 2.8 MB (2816169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffa1326b35d047e371043a2411e65bd818c27909ab1ecf1ce37b55741744e890`  
		Last Modified: Thu, 17 Mar 2022 18:07:13 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85eb6277290b589d592446e2f538670a432e8a6e60772ee08f89a2055bef71ec`  
		Last Modified: Thu, 17 Mar 2022 18:07:13 GMT  
		Size: 271.7 KB (271670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b39ce21458bdaf243df53380280a782bfbc3099e7f36c70db0a62c12b8ebf3b9`  
		Last Modified: Sat, 19 Mar 2022 01:00:49 GMT  
		Size: 19.2 MB (19203953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cec10810f452053c3033b88ae3b35e10f6c5eecc621b99c7688ac8b1aa773dfd`  
		Last Modified: Sat, 19 Mar 2022 01:00:44 GMT  
		Size: 12.3 KB (12261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f23c5a39777071597afa83881fe6dcf2d89caf5febe1ce7c91680779968a30e7`  
		Last Modified: Sat, 19 Mar 2022 01:00:44 GMT  
		Size: 11.9 KB (11898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e946aa8c1244dccf6b09f0e8d3daff8ffbec4f144872b88bbf7c489ac9507790`  
		Last Modified: Sat, 19 Mar 2022 01:00:45 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.8.10`

```console
$ docker pull chronograf@sha256:d99e0ec07af2fe60bfbd86456f69cef1fbeaac82eaf3bc1d287d2703379a39a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.8.10` - linux; amd64

```console
$ docker pull chronograf@sha256:71720adff754f47be799c56494fd8e15eb2fda0f58fac358b2f5a8c84f035c6a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66279024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70ddb8df4a909d55e224c1f58d665520efb4de5f348d75aa9a8d80aa4610020a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 17 Mar 2022 04:06:48 GMT
ADD file:9fc739b295073dd1d9293d2ea8106e21156de790c82a9d19be210c0c63bfb527 in / 
# Thu, 17 Mar 2022 04:06:48 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 08:38:22 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 17 Mar 2022 08:39:38 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Thu, 17 Mar 2022 08:39:46 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Thu, 17 Mar 2022 08:39:46 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 17 Mar 2022 08:39:46 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 17 Mar 2022 08:39:46 GMT
EXPOSE 8888
# Thu, 17 Mar 2022 08:39:46 GMT
VOLUME [/var/lib/chronograf]
# Thu, 17 Mar 2022 08:39:46 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Thu, 17 Mar 2022 08:39:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 17 Mar 2022 08:39:46 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:5d9da879a61c05a35520eabaa04d22b4867d0cf84a91f4c7b078128e1c820ce5`  
		Last Modified: Thu, 17 Mar 2022 04:14:03 GMT  
		Size: 22.6 MB (22567740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:964f48dfa9fa2029216316deab45629f6c3afbc5021d72278ae08424dd0774b0`  
		Last Modified: Thu, 17 Mar 2022 08:40:28 GMT  
		Size: 6.8 MB (6760337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef0628cff5565c1b1d727f5fb38edc6a84c913e1937bd7f4859e77e54b35d42d`  
		Last Modified: Thu, 17 Mar 2022 08:41:03 GMT  
		Size: 36.9 MB (36926565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2342aa887107fc7ca17bfbab46a2f800ceace0f64399cd9c4fa0c005ec7f3897`  
		Last Modified: Thu, 17 Mar 2022 08:40:58 GMT  
		Size: 12.2 KB (12242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66e69d5532f76bba0cc882567ce4e49ae883248b1a3b236ce63464ee892d90d6`  
		Last Modified: Thu, 17 Mar 2022 08:40:58 GMT  
		Size: 11.9 KB (11901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62b4060dfa2d51e4e395bd3c6ac9e6aa088edd5fa71ceabd978ce37d2067f8c8`  
		Last Modified: Thu, 17 Mar 2022 08:40:58 GMT  
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
$ docker pull chronograf@sha256:0d6beb1f2713a42997d2ce44c127ccf87d438357351308125b9c4aa54324d0df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.8.10-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:fd32b003c95265983c7fdf485622e1a7937f36bb6249fbd1a5fc39d5d72904b2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.3 MB (22316342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbf8d9aa814b6ccb2b8192ac18b512d5cf6161dfb066d657917183e5bfacffa3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 17 Mar 2022 15:19:26 GMT
ADD file:8ec3735d4b1b4b070607b94e3bd360117b07dc26e1baf5dd485b49b3413e8fff in / 
# Thu, 17 Mar 2022 15:19:26 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 18:05:42 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 17 Mar 2022 18:05:43 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Sat, 19 Mar 2022 00:58:09 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Sat, 19 Mar 2022 00:58:50 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Sat, 19 Mar 2022 00:58:50 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Sat, 19 Mar 2022 00:58:51 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sat, 19 Mar 2022 00:58:51 GMT
EXPOSE 8888
# Sat, 19 Mar 2022 00:58:51 GMT
VOLUME [/var/lib/chronograf]
# Sat, 19 Mar 2022 00:58:51 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Sat, 19 Mar 2022 00:58:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 19 Mar 2022 00:58:51 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:36ccefbf3d8a9a1b18baaa9cbf0f3ad50e8a7b751656c74df359900a318cbffc`  
		Last Modified: Thu, 17 Mar 2022 15:20:13 GMT  
		Size: 2.8 MB (2816169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffa1326b35d047e371043a2411e65bd818c27909ab1ecf1ce37b55741744e890`  
		Last Modified: Thu, 17 Mar 2022 18:07:13 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85eb6277290b589d592446e2f538670a432e8a6e60772ee08f89a2055bef71ec`  
		Last Modified: Thu, 17 Mar 2022 18:07:13 GMT  
		Size: 271.7 KB (271670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b39ce21458bdaf243df53380280a782bfbc3099e7f36c70db0a62c12b8ebf3b9`  
		Last Modified: Sat, 19 Mar 2022 01:00:49 GMT  
		Size: 19.2 MB (19203953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cec10810f452053c3033b88ae3b35e10f6c5eecc621b99c7688ac8b1aa773dfd`  
		Last Modified: Sat, 19 Mar 2022 01:00:44 GMT  
		Size: 12.3 KB (12261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f23c5a39777071597afa83881fe6dcf2d89caf5febe1ce7c91680779968a30e7`  
		Last Modified: Sat, 19 Mar 2022 01:00:44 GMT  
		Size: 11.9 KB (11898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e946aa8c1244dccf6b09f0e8d3daff8ffbec4f144872b88bbf7c489ac9507790`  
		Last Modified: Sat, 19 Mar 2022 01:00:45 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.9`

```console
$ docker pull chronograf@sha256:730a25ac139d5edbef955f078c590d431d04eea198a03c28e6937e462c8003f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.9` - linux; amd64

```console
$ docker pull chronograf@sha256:985f6182121785c767b8337a4db31522d193905a01eaca6b427a6fd184c78ae5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.9 MB (66922994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81f95ec4358baed27d07bf7c3ac87f695f89b4e129cde586350ab0eae8c4e7de`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 17 Mar 2022 04:06:48 GMT
ADD file:9fc739b295073dd1d9293d2ea8106e21156de790c82a9d19be210c0c63bfb527 in / 
# Thu, 17 Mar 2022 04:06:48 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 08:38:22 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 24 Mar 2022 21:22:58 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Thu, 24 Mar 2022 21:23:06 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Thu, 24 Mar 2022 21:23:06 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 24 Mar 2022 21:23:06 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 24 Mar 2022 21:23:06 GMT
EXPOSE 8888
# Thu, 24 Mar 2022 21:23:06 GMT
VOLUME [/var/lib/chronograf]
# Thu, 24 Mar 2022 21:23:07 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Thu, 24 Mar 2022 21:23:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 24 Mar 2022 21:23:07 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:5d9da879a61c05a35520eabaa04d22b4867d0cf84a91f4c7b078128e1c820ce5`  
		Last Modified: Thu, 17 Mar 2022 04:14:03 GMT  
		Size: 22.6 MB (22567740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:964f48dfa9fa2029216316deab45629f6c3afbc5021d72278ae08424dd0774b0`  
		Last Modified: Thu, 17 Mar 2022 08:40:28 GMT  
		Size: 6.8 MB (6760337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9171e83a8c3392242027168c43b24df623272a72222ffea0a8978d1e77d61657`  
		Last Modified: Thu, 24 Mar 2022 21:23:48 GMT  
		Size: 37.6 MB (37570529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fef4b5144d43817e2d4d8760007b8159cf0b05781915691b5a683f34fc34898`  
		Last Modified: Thu, 24 Mar 2022 21:23:42 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b44fe309668140f5233bde2a2c6ca6cb8955afeded71d0b5d692b3850b2feb9`  
		Last Modified: Thu, 24 Mar 2022 21:23:42 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2b989bf63d86e693cec98709b1af248dba49de814cbfe6fa8206d3b7929a67e`  
		Last Modified: Thu, 24 Mar 2022 21:23:42 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.9` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:8c7d980c1b66920f7cd146b82853cd2991cc1d414af2af0cc3410b82d48999dd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.4 MB (60439504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:663e5f6ba5d85816707036e3d06085e8926a96ddff5998597a16216b808cd3b7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 17 Mar 2022 09:36:59 GMT
ADD file:28d5a216145f4b0aa29a7151a22e6e7dab9d430006122bbed8b13f84ae55713e in / 
# Thu, 17 Mar 2022 09:37:00 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 02:42:06 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Sat, 19 Mar 2022 02:44:38 GMT
ENV CHRONOGRAF_VERSION=1.9.3
# Sat, 19 Mar 2022 02:44:57 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Sat, 19 Mar 2022 02:44:58 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Sat, 19 Mar 2022 02:44:58 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sat, 19 Mar 2022 02:44:59 GMT
EXPOSE 8888
# Sat, 19 Mar 2022 02:44:59 GMT
VOLUME [/var/lib/chronograf]
# Sat, 19 Mar 2022 02:45:00 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Sat, 19 Mar 2022 02:45:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 19 Mar 2022 02:45:01 GMT
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
	-	`sha256:460bedd2c767d06aae75a019eb8f8477b43de8aba140942553f6da63575c6ee0`  
		Last Modified: Sat, 19 Mar 2022 02:47:37 GMT  
		Size: 35.3 MB (35274550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d9797986c81b046010c0eef4ebb3f9ed44ef0b6f5689fc3607c00fac783b2a4`  
		Last Modified: Sat, 19 Mar 2022 02:47:18 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4d9afb8b8fe48a6491aef79ab309d66a9121376c4d36626d397e3ca46efd0d2`  
		Last Modified: Sat, 19 Mar 2022 02:47:18 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3790a2d98c90ee841bc3a0afa9988011690836e08c525924195823ae4aeca290`  
		Last Modified: Sat, 19 Mar 2022 02:47:18 GMT  
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
$ docker pull chronograf@sha256:e3b8b6ccc9e4f58074b0ed4774f93ed23710f550333a7c6bded21f274d44fc4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.9-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:d30cc0213c18bdeb684fb32c6a2df32fd3696acf6eb8cac649af07f06f871412
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.8 MB (22784520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f3401e531ec61aed808da0727baa9130cf7e7df9eab77fadadf896ad494c0c8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 17 Mar 2022 15:19:26 GMT
ADD file:8ec3735d4b1b4b070607b94e3bd360117b07dc26e1baf5dd485b49b3413e8fff in / 
# Thu, 17 Mar 2022 15:19:26 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 18:05:42 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 17 Mar 2022 18:05:43 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Thu, 24 Mar 2022 21:23:10 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Thu, 24 Mar 2022 21:23:15 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 24 Mar 2022 21:23:16 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 24 Mar 2022 21:23:16 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 24 Mar 2022 21:23:16 GMT
EXPOSE 8888
# Thu, 24 Mar 2022 21:23:16 GMT
VOLUME [/var/lib/chronograf]
# Thu, 24 Mar 2022 21:23:16 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Thu, 24 Mar 2022 21:23:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 24 Mar 2022 21:23:16 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:36ccefbf3d8a9a1b18baaa9cbf0f3ad50e8a7b751656c74df359900a318cbffc`  
		Last Modified: Thu, 17 Mar 2022 15:20:13 GMT  
		Size: 2.8 MB (2816169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffa1326b35d047e371043a2411e65bd818c27909ab1ecf1ce37b55741744e890`  
		Last Modified: Thu, 17 Mar 2022 18:07:13 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85eb6277290b589d592446e2f538670a432e8a6e60772ee08f89a2055bef71ec`  
		Last Modified: Thu, 17 Mar 2022 18:07:13 GMT  
		Size: 271.7 KB (271670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af6cfdd72d402adf7db7eee583f3ac4b831b46a4e392e00c40bc5d888b7432f5`  
		Last Modified: Thu, 24 Mar 2022 21:24:04 GMT  
		Size: 19.7 MB (19672122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f23e00107588bddfd7e1c2ef130b18a04d1b2617058e2dd6a5dcff2bb8574774`  
		Last Modified: Thu, 24 Mar 2022 21:24:00 GMT  
		Size: 12.3 KB (12268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:502f2dc7f3221e0ca1249b05933e47de41591e161593e3c373bad7d5fe87512f`  
		Last Modified: Thu, 24 Mar 2022 21:24:01 GMT  
		Size: 11.9 KB (11899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d713889b3d9a4d2c25dbde2e3afec265d3914c609d03f49c812fc59e2004ddb`  
		Last Modified: Thu, 24 Mar 2022 21:24:00 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.9.4`

```console
$ docker pull chronograf@sha256:fd36c3e4abbbf6338d3d09bd928ccada2bd84a25f641c2e753939134dff9f314
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `chronograf:1.9.4` - linux; amd64

```console
$ docker pull chronograf@sha256:985f6182121785c767b8337a4db31522d193905a01eaca6b427a6fd184c78ae5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.9 MB (66922994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81f95ec4358baed27d07bf7c3ac87f695f89b4e129cde586350ab0eae8c4e7de`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 17 Mar 2022 04:06:48 GMT
ADD file:9fc739b295073dd1d9293d2ea8106e21156de790c82a9d19be210c0c63bfb527 in / 
# Thu, 17 Mar 2022 04:06:48 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 08:38:22 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 24 Mar 2022 21:22:58 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Thu, 24 Mar 2022 21:23:06 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Thu, 24 Mar 2022 21:23:06 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 24 Mar 2022 21:23:06 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 24 Mar 2022 21:23:06 GMT
EXPOSE 8888
# Thu, 24 Mar 2022 21:23:06 GMT
VOLUME [/var/lib/chronograf]
# Thu, 24 Mar 2022 21:23:07 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Thu, 24 Mar 2022 21:23:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 24 Mar 2022 21:23:07 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:5d9da879a61c05a35520eabaa04d22b4867d0cf84a91f4c7b078128e1c820ce5`  
		Last Modified: Thu, 17 Mar 2022 04:14:03 GMT  
		Size: 22.6 MB (22567740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:964f48dfa9fa2029216316deab45629f6c3afbc5021d72278ae08424dd0774b0`  
		Last Modified: Thu, 17 Mar 2022 08:40:28 GMT  
		Size: 6.8 MB (6760337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9171e83a8c3392242027168c43b24df623272a72222ffea0a8978d1e77d61657`  
		Last Modified: Thu, 24 Mar 2022 21:23:48 GMT  
		Size: 37.6 MB (37570529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fef4b5144d43817e2d4d8760007b8159cf0b05781915691b5a683f34fc34898`  
		Last Modified: Thu, 24 Mar 2022 21:23:42 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b44fe309668140f5233bde2a2c6ca6cb8955afeded71d0b5d692b3850b2feb9`  
		Last Modified: Thu, 24 Mar 2022 21:23:42 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2b989bf63d86e693cec98709b1af248dba49de814cbfe6fa8206d3b7929a67e`  
		Last Modified: Thu, 24 Mar 2022 21:23:42 GMT  
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
$ docker pull chronograf@sha256:e3b8b6ccc9e4f58074b0ed4774f93ed23710f550333a7c6bded21f274d44fc4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.9.4-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:d30cc0213c18bdeb684fb32c6a2df32fd3696acf6eb8cac649af07f06f871412
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.8 MB (22784520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f3401e531ec61aed808da0727baa9130cf7e7df9eab77fadadf896ad494c0c8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 17 Mar 2022 15:19:26 GMT
ADD file:8ec3735d4b1b4b070607b94e3bd360117b07dc26e1baf5dd485b49b3413e8fff in / 
# Thu, 17 Mar 2022 15:19:26 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 18:05:42 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 17 Mar 2022 18:05:43 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Thu, 24 Mar 2022 21:23:10 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Thu, 24 Mar 2022 21:23:15 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 24 Mar 2022 21:23:16 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 24 Mar 2022 21:23:16 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 24 Mar 2022 21:23:16 GMT
EXPOSE 8888
# Thu, 24 Mar 2022 21:23:16 GMT
VOLUME [/var/lib/chronograf]
# Thu, 24 Mar 2022 21:23:16 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Thu, 24 Mar 2022 21:23:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 24 Mar 2022 21:23:16 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:36ccefbf3d8a9a1b18baaa9cbf0f3ad50e8a7b751656c74df359900a318cbffc`  
		Last Modified: Thu, 17 Mar 2022 15:20:13 GMT  
		Size: 2.8 MB (2816169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffa1326b35d047e371043a2411e65bd818c27909ab1ecf1ce37b55741744e890`  
		Last Modified: Thu, 17 Mar 2022 18:07:13 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85eb6277290b589d592446e2f538670a432e8a6e60772ee08f89a2055bef71ec`  
		Last Modified: Thu, 17 Mar 2022 18:07:13 GMT  
		Size: 271.7 KB (271670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af6cfdd72d402adf7db7eee583f3ac4b831b46a4e392e00c40bc5d888b7432f5`  
		Last Modified: Thu, 24 Mar 2022 21:24:04 GMT  
		Size: 19.7 MB (19672122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f23e00107588bddfd7e1c2ef130b18a04d1b2617058e2dd6a5dcff2bb8574774`  
		Last Modified: Thu, 24 Mar 2022 21:24:00 GMT  
		Size: 12.3 KB (12268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:502f2dc7f3221e0ca1249b05933e47de41591e161593e3c373bad7d5fe87512f`  
		Last Modified: Thu, 24 Mar 2022 21:24:01 GMT  
		Size: 11.9 KB (11899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d713889b3d9a4d2c25dbde2e3afec265d3914c609d03f49c812fc59e2004ddb`  
		Last Modified: Thu, 24 Mar 2022 21:24:00 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:alpine`

```console
$ docker pull chronograf@sha256:e3b8b6ccc9e4f58074b0ed4774f93ed23710f550333a7c6bded21f274d44fc4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:d30cc0213c18bdeb684fb32c6a2df32fd3696acf6eb8cac649af07f06f871412
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.8 MB (22784520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f3401e531ec61aed808da0727baa9130cf7e7df9eab77fadadf896ad494c0c8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 17 Mar 2022 15:19:26 GMT
ADD file:8ec3735d4b1b4b070607b94e3bd360117b07dc26e1baf5dd485b49b3413e8fff in / 
# Thu, 17 Mar 2022 15:19:26 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 18:05:42 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 17 Mar 2022 18:05:43 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Thu, 24 Mar 2022 21:23:10 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Thu, 24 Mar 2022 21:23:15 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 24 Mar 2022 21:23:16 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 24 Mar 2022 21:23:16 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 24 Mar 2022 21:23:16 GMT
EXPOSE 8888
# Thu, 24 Mar 2022 21:23:16 GMT
VOLUME [/var/lib/chronograf]
# Thu, 24 Mar 2022 21:23:16 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Thu, 24 Mar 2022 21:23:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 24 Mar 2022 21:23:16 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:36ccefbf3d8a9a1b18baaa9cbf0f3ad50e8a7b751656c74df359900a318cbffc`  
		Last Modified: Thu, 17 Mar 2022 15:20:13 GMT  
		Size: 2.8 MB (2816169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffa1326b35d047e371043a2411e65bd818c27909ab1ecf1ce37b55741744e890`  
		Last Modified: Thu, 17 Mar 2022 18:07:13 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85eb6277290b589d592446e2f538670a432e8a6e60772ee08f89a2055bef71ec`  
		Last Modified: Thu, 17 Mar 2022 18:07:13 GMT  
		Size: 271.7 KB (271670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af6cfdd72d402adf7db7eee583f3ac4b831b46a4e392e00c40bc5d888b7432f5`  
		Last Modified: Thu, 24 Mar 2022 21:24:04 GMT  
		Size: 19.7 MB (19672122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f23e00107588bddfd7e1c2ef130b18a04d1b2617058e2dd6a5dcff2bb8574774`  
		Last Modified: Thu, 24 Mar 2022 21:24:00 GMT  
		Size: 12.3 KB (12268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:502f2dc7f3221e0ca1249b05933e47de41591e161593e3c373bad7d5fe87512f`  
		Last Modified: Thu, 24 Mar 2022 21:24:01 GMT  
		Size: 11.9 KB (11899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d713889b3d9a4d2c25dbde2e3afec265d3914c609d03f49c812fc59e2004ddb`  
		Last Modified: Thu, 24 Mar 2022 21:24:00 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:latest`

```console
$ docker pull chronograf@sha256:730a25ac139d5edbef955f078c590d431d04eea198a03c28e6937e462c8003f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:latest` - linux; amd64

```console
$ docker pull chronograf@sha256:985f6182121785c767b8337a4db31522d193905a01eaca6b427a6fd184c78ae5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.9 MB (66922994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81f95ec4358baed27d07bf7c3ac87f695f89b4e129cde586350ab0eae8c4e7de`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 17 Mar 2022 04:06:48 GMT
ADD file:9fc739b295073dd1d9293d2ea8106e21156de790c82a9d19be210c0c63bfb527 in / 
# Thu, 17 Mar 2022 04:06:48 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 08:38:22 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 24 Mar 2022 21:22:58 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Thu, 24 Mar 2022 21:23:06 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Thu, 24 Mar 2022 21:23:06 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 24 Mar 2022 21:23:06 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 24 Mar 2022 21:23:06 GMT
EXPOSE 8888
# Thu, 24 Mar 2022 21:23:06 GMT
VOLUME [/var/lib/chronograf]
# Thu, 24 Mar 2022 21:23:07 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Thu, 24 Mar 2022 21:23:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 24 Mar 2022 21:23:07 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:5d9da879a61c05a35520eabaa04d22b4867d0cf84a91f4c7b078128e1c820ce5`  
		Last Modified: Thu, 17 Mar 2022 04:14:03 GMT  
		Size: 22.6 MB (22567740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:964f48dfa9fa2029216316deab45629f6c3afbc5021d72278ae08424dd0774b0`  
		Last Modified: Thu, 17 Mar 2022 08:40:28 GMT  
		Size: 6.8 MB (6760337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9171e83a8c3392242027168c43b24df623272a72222ffea0a8978d1e77d61657`  
		Last Modified: Thu, 24 Mar 2022 21:23:48 GMT  
		Size: 37.6 MB (37570529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fef4b5144d43817e2d4d8760007b8159cf0b05781915691b5a683f34fc34898`  
		Last Modified: Thu, 24 Mar 2022 21:23:42 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b44fe309668140f5233bde2a2c6ca6cb8955afeded71d0b5d692b3850b2feb9`  
		Last Modified: Thu, 24 Mar 2022 21:23:42 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2b989bf63d86e693cec98709b1af248dba49de814cbfe6fa8206d3b7929a67e`  
		Last Modified: Thu, 24 Mar 2022 21:23:42 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:latest` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:8c7d980c1b66920f7cd146b82853cd2991cc1d414af2af0cc3410b82d48999dd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.4 MB (60439504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:663e5f6ba5d85816707036e3d06085e8926a96ddff5998597a16216b808cd3b7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 17 Mar 2022 09:36:59 GMT
ADD file:28d5a216145f4b0aa29a7151a22e6e7dab9d430006122bbed8b13f84ae55713e in / 
# Thu, 17 Mar 2022 09:37:00 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 02:42:06 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Sat, 19 Mar 2022 02:44:38 GMT
ENV CHRONOGRAF_VERSION=1.9.3
# Sat, 19 Mar 2022 02:44:57 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Sat, 19 Mar 2022 02:44:58 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Sat, 19 Mar 2022 02:44:58 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sat, 19 Mar 2022 02:44:59 GMT
EXPOSE 8888
# Sat, 19 Mar 2022 02:44:59 GMT
VOLUME [/var/lib/chronograf]
# Sat, 19 Mar 2022 02:45:00 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Sat, 19 Mar 2022 02:45:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 19 Mar 2022 02:45:01 GMT
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
	-	`sha256:460bedd2c767d06aae75a019eb8f8477b43de8aba140942553f6da63575c6ee0`  
		Last Modified: Sat, 19 Mar 2022 02:47:37 GMT  
		Size: 35.3 MB (35274550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d9797986c81b046010c0eef4ebb3f9ed44ef0b6f5689fc3607c00fac783b2a4`  
		Last Modified: Sat, 19 Mar 2022 02:47:18 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4d9afb8b8fe48a6491aef79ab309d66a9121376c4d36626d397e3ca46efd0d2`  
		Last Modified: Sat, 19 Mar 2022 02:47:18 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3790a2d98c90ee841bc3a0afa9988011690836e08c525924195823ae4aeca290`  
		Last Modified: Sat, 19 Mar 2022 02:47:18 GMT  
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
