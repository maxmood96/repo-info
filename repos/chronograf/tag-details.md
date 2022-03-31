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
$ docker pull chronograf@sha256:0fac8a1aad0035035b56d430aa25dc47f4f0d949736e57948657f03566dd6039
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
$ docker pull chronograf@sha256:b3689a088abcce62fb781f8d50e99afa352c940bd1d4fc8158d785b166302124
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.0 MB (43986145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8215f0dd26cc899bdf0baf3d8c71ad00142125d1020b348c85ef1e1aba3ed20c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 29 Mar 2022 02:24:30 GMT
ADD file:a9cc850c256adf321d6c477c8875da7208938384cb764d33a90a78b2c0740a28 in / 
# Tue, 29 Mar 2022 02:24:31 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 21:43:18 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 30 Mar 2022 21:43:18 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Wed, 30 Mar 2022 21:43:35 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 30 Mar 2022 21:43:36 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 30 Mar 2022 21:43:36 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 30 Mar 2022 21:43:37 GMT
EXPOSE 8888
# Wed, 30 Mar 2022 21:43:37 GMT
VOLUME [/var/lib/chronograf]
# Wed, 30 Mar 2022 21:43:38 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 30 Mar 2022 21:43:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 30 Mar 2022 21:43:39 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:072a4a410a8ca19c3bba361b4ad2205c16658c8130309a0ddc1b92d3d9fb8e7b`  
		Last Modified: Tue, 29 Mar 2022 02:41:11 GMT  
		Size: 19.4 MB (19359808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0df16a38b9594b1f24af35716b84b3eff3b553f13abf4eccc7c2d6c29815fd5e`  
		Last Modified: Wed, 30 Mar 2022 21:46:52 GMT  
		Size: 5.8 MB (5780857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e5fa116bfe7ed24b2709ee2fe22060deef5c46560c1fa7ccb5a038306d9ccc2`  
		Last Modified: Wed, 30 Mar 2022 21:47:02 GMT  
		Size: 18.8 MB (18821084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda857333a40f0092282f153de83ec5300e1245989ea1f5b16181a8ad1cbe4d7`  
		Last Modified: Wed, 30 Mar 2022 21:46:49 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b420efc17c0a962b4b720eaa71294c12b7ddacebb433bb90c2a9199533469791`  
		Last Modified: Wed, 30 Mar 2022 21:46:49 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65d3260a795f4cb87b7dc0aa3ac6d7beec15a1ede10f38a5eee42512da858178`  
		Last Modified: Wed, 30 Mar 2022 21:46:49 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.6` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:d030cb8f4dc80a264deedaa2d9fc77de6d718ed708d602bb2b3ed7119eb38cef
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45457215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:950b7c5e7891bcff9809ee3d7e116b72b6bd2cbc541f40ce92b705f04092e693`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 29 Mar 2022 00:45:36 GMT
ADD file:e754ad83155f3f9d7419711eba00fb58e2d7be1ac24ec386b4ace6f1582bae31 in / 
# Tue, 29 Mar 2022 00:45:37 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 02:29:45 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 30 Mar 2022 02:29:45 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Wed, 30 Mar 2022 02:29:54 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 30 Mar 2022 02:29:55 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 30 Mar 2022 02:29:56 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 30 Mar 2022 02:29:56 GMT
EXPOSE 8888
# Wed, 30 Mar 2022 02:29:57 GMT
VOLUME [/var/lib/chronograf]
# Wed, 30 Mar 2022 02:29:59 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 30 Mar 2022 02:29:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 30 Mar 2022 02:30:00 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:fdcfc792a1f8b9e7f758eaa734b92858ca636af5571eac11c5da87ce721db2d5`  
		Last Modified: Tue, 29 Mar 2022 00:54:21 GMT  
		Size: 20.4 MB (20423743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81e150d438592de367bca726042ec26ad6c7f34b79930a4d66ae91da4fa5d2ad`  
		Last Modified: Wed, 30 Mar 2022 02:31:50 GMT  
		Size: 6.0 MB (6047427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77f7e35f9aa1a13dad5e0215a8afb9293b19d04738d736a4de7006460d9fa5dc`  
		Last Modified: Wed, 30 Mar 2022 02:31:52 GMT  
		Size: 19.0 MB (18961659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f87e7e606f6c3efd0832f76a118eacb4d635ccc0603304e0a5022463c362cc47`  
		Last Modified: Wed, 30 Mar 2022 02:31:49 GMT  
		Size: 12.2 KB (12243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee03675e6cfe9b0a28eddfe77a52dab6e72467b38117d01603002eaf62ed2a86`  
		Last Modified: Wed, 30 Mar 2022 02:31:50 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a34fb20758788b4f602f5ce9a293179503705f486f1f9c76700787125fa1dda`  
		Last Modified: Wed, 30 Mar 2022 02:31:49 GMT  
		Size: 238.0 B  
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
$ docker pull chronograf@sha256:0fac8a1aad0035035b56d430aa25dc47f4f0d949736e57948657f03566dd6039
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
$ docker pull chronograf@sha256:b3689a088abcce62fb781f8d50e99afa352c940bd1d4fc8158d785b166302124
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.0 MB (43986145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8215f0dd26cc899bdf0baf3d8c71ad00142125d1020b348c85ef1e1aba3ed20c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 29 Mar 2022 02:24:30 GMT
ADD file:a9cc850c256adf321d6c477c8875da7208938384cb764d33a90a78b2c0740a28 in / 
# Tue, 29 Mar 2022 02:24:31 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 21:43:18 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 30 Mar 2022 21:43:18 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Wed, 30 Mar 2022 21:43:35 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 30 Mar 2022 21:43:36 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 30 Mar 2022 21:43:36 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 30 Mar 2022 21:43:37 GMT
EXPOSE 8888
# Wed, 30 Mar 2022 21:43:37 GMT
VOLUME [/var/lib/chronograf]
# Wed, 30 Mar 2022 21:43:38 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 30 Mar 2022 21:43:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 30 Mar 2022 21:43:39 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:072a4a410a8ca19c3bba361b4ad2205c16658c8130309a0ddc1b92d3d9fb8e7b`  
		Last Modified: Tue, 29 Mar 2022 02:41:11 GMT  
		Size: 19.4 MB (19359808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0df16a38b9594b1f24af35716b84b3eff3b553f13abf4eccc7c2d6c29815fd5e`  
		Last Modified: Wed, 30 Mar 2022 21:46:52 GMT  
		Size: 5.8 MB (5780857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e5fa116bfe7ed24b2709ee2fe22060deef5c46560c1fa7ccb5a038306d9ccc2`  
		Last Modified: Wed, 30 Mar 2022 21:47:02 GMT  
		Size: 18.8 MB (18821084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda857333a40f0092282f153de83ec5300e1245989ea1f5b16181a8ad1cbe4d7`  
		Last Modified: Wed, 30 Mar 2022 21:46:49 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b420efc17c0a962b4b720eaa71294c12b7ddacebb433bb90c2a9199533469791`  
		Last Modified: Wed, 30 Mar 2022 21:46:49 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65d3260a795f4cb87b7dc0aa3ac6d7beec15a1ede10f38a5eee42512da858178`  
		Last Modified: Wed, 30 Mar 2022 21:46:49 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.6.2` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:d030cb8f4dc80a264deedaa2d9fc77de6d718ed708d602bb2b3ed7119eb38cef
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45457215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:950b7c5e7891bcff9809ee3d7e116b72b6bd2cbc541f40ce92b705f04092e693`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 29 Mar 2022 00:45:36 GMT
ADD file:e754ad83155f3f9d7419711eba00fb58e2d7be1ac24ec386b4ace6f1582bae31 in / 
# Tue, 29 Mar 2022 00:45:37 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 02:29:45 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 30 Mar 2022 02:29:45 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Wed, 30 Mar 2022 02:29:54 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 30 Mar 2022 02:29:55 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 30 Mar 2022 02:29:56 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 30 Mar 2022 02:29:56 GMT
EXPOSE 8888
# Wed, 30 Mar 2022 02:29:57 GMT
VOLUME [/var/lib/chronograf]
# Wed, 30 Mar 2022 02:29:59 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 30 Mar 2022 02:29:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 30 Mar 2022 02:30:00 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:fdcfc792a1f8b9e7f758eaa734b92858ca636af5571eac11c5da87ce721db2d5`  
		Last Modified: Tue, 29 Mar 2022 00:54:21 GMT  
		Size: 20.4 MB (20423743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81e150d438592de367bca726042ec26ad6c7f34b79930a4d66ae91da4fa5d2ad`  
		Last Modified: Wed, 30 Mar 2022 02:31:50 GMT  
		Size: 6.0 MB (6047427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77f7e35f9aa1a13dad5e0215a8afb9293b19d04738d736a4de7006460d9fa5dc`  
		Last Modified: Wed, 30 Mar 2022 02:31:52 GMT  
		Size: 19.0 MB (18961659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f87e7e606f6c3efd0832f76a118eacb4d635ccc0603304e0a5022463c362cc47`  
		Last Modified: Wed, 30 Mar 2022 02:31:49 GMT  
		Size: 12.2 KB (12243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee03675e6cfe9b0a28eddfe77a52dab6e72467b38117d01603002eaf62ed2a86`  
		Last Modified: Wed, 30 Mar 2022 02:31:50 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a34fb20758788b4f602f5ce9a293179503705f486f1f9c76700787125fa1dda`  
		Last Modified: Wed, 30 Mar 2022 02:31:49 GMT  
		Size: 238.0 B  
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
$ docker pull chronograf@sha256:ce80d87be3faa71e1e254bf92d4be2320d1faba3de23ce790d24e34dd84988d6
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
$ docker pull chronograf@sha256:cf09ff01267042e3586cdaf4d2b7af26805f1d96b5e95896a5d1d519b072e1af
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.0 MB (59048349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b8a3c07e9687f083df6e3b8a1fb967fbd5e5b8abdbd70724d3f221c8695e4a7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 29 Mar 2022 02:24:30 GMT
ADD file:a9cc850c256adf321d6c477c8875da7208938384cb764d33a90a78b2c0740a28 in / 
# Tue, 29 Mar 2022 02:24:31 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 21:44:05 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 30 Mar 2022 21:44:05 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Wed, 30 Mar 2022 21:44:39 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 30 Mar 2022 21:44:40 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 30 Mar 2022 21:44:40 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 30 Mar 2022 21:44:41 GMT
EXPOSE 8888
# Wed, 30 Mar 2022 21:44:41 GMT
VOLUME [/var/lib/chronograf]
# Wed, 30 Mar 2022 21:44:42 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 30 Mar 2022 21:44:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 30 Mar 2022 21:44:42 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:072a4a410a8ca19c3bba361b4ad2205c16658c8130309a0ddc1b92d3d9fb8e7b`  
		Last Modified: Tue, 29 Mar 2022 02:41:11 GMT  
		Size: 19.4 MB (19359808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39844bbafdefabfb551a1b4ff17d8a5edc293968193149449875ebfdac27937a`  
		Last Modified: Wed, 30 Mar 2022 21:47:15 GMT  
		Size: 3.9 MB (3880277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a07b5a70b6f42c82c926fc7d2728a30a5626a13cb87fcb7c9287908a1fe7cc91`  
		Last Modified: Wed, 30 Mar 2022 21:47:33 GMT  
		Size: 35.8 MB (35783876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff6f5cbff3264c6b1435d226b049bed1ede02329fdbfd578d941c56f5eaff3a7`  
		Last Modified: Wed, 30 Mar 2022 21:47:13 GMT  
		Size: 12.2 KB (12244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aede3a0129c0ab157d7cb83f4ef7b833693fb7762b68fafaabafdb9dd69bff8`  
		Last Modified: Wed, 30 Mar 2022 21:47:13 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130d64973b14c354b674c0acaddd34cd4b209914fbde340a2d28adbcdda970a3`  
		Last Modified: Wed, 30 Mar 2022 21:47:13 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.7` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:da785f87397ffb30b1e9bc9d9424302ffcb839b46c22e2ac3904c8fc7840d6c3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60329478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30a14eaf7a6dded423824d24729dd141f875d50a82e9adfcd08bf972ca6f6240`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 29 Mar 2022 00:45:36 GMT
ADD file:e754ad83155f3f9d7419711eba00fb58e2d7be1ac24ec386b4ace6f1582bae31 in / 
# Tue, 29 Mar 2022 00:45:37 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 02:30:14 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 30 Mar 2022 02:30:15 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Wed, 30 Mar 2022 02:30:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 30 Mar 2022 02:30:32 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 30 Mar 2022 02:30:33 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 30 Mar 2022 02:30:33 GMT
EXPOSE 8888
# Wed, 30 Mar 2022 02:30:34 GMT
VOLUME [/var/lib/chronograf]
# Wed, 30 Mar 2022 02:30:36 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 30 Mar 2022 02:30:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 30 Mar 2022 02:30:37 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:fdcfc792a1f8b9e7f758eaa734b92858ca636af5571eac11c5da87ce721db2d5`  
		Last Modified: Tue, 29 Mar 2022 00:54:21 GMT  
		Size: 20.4 MB (20423743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd46d0499f095f9fa0c29a157cf9d6ff0fff80da52412f53f406e6c0f0d7412a`  
		Last Modified: Wed, 30 Mar 2022 02:32:04 GMT  
		Size: 3.9 MB (3894002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78bb4d065844d6e2e1d0264f3b006179b254a688ed544cd2ec99ec85c18f2cf7`  
		Last Modified: Wed, 30 Mar 2022 02:32:07 GMT  
		Size: 36.0 MB (35987346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4554f3c58f35cbbe81ea4ddff472cb7e4fa445cf20e2d029a90eb051ae2e25ba`  
		Last Modified: Wed, 30 Mar 2022 02:32:03 GMT  
		Size: 12.2 KB (12243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca2f5c18f5743263fe7c5badea4d67555d96b9a18928190a3f48d42aed313660`  
		Last Modified: Wed, 30 Mar 2022 02:32:03 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:593bc2bde7a2037d0118b77cb725930d7854fadd0acf022f781c885f46f07b3c`  
		Last Modified: Wed, 30 Mar 2022 02:32:03 GMT  
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
$ docker pull chronograf@sha256:ce80d87be3faa71e1e254bf92d4be2320d1faba3de23ce790d24e34dd84988d6
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
$ docker pull chronograf@sha256:cf09ff01267042e3586cdaf4d2b7af26805f1d96b5e95896a5d1d519b072e1af
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.0 MB (59048349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b8a3c07e9687f083df6e3b8a1fb967fbd5e5b8abdbd70724d3f221c8695e4a7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 29 Mar 2022 02:24:30 GMT
ADD file:a9cc850c256adf321d6c477c8875da7208938384cb764d33a90a78b2c0740a28 in / 
# Tue, 29 Mar 2022 02:24:31 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 21:44:05 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 30 Mar 2022 21:44:05 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Wed, 30 Mar 2022 21:44:39 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 30 Mar 2022 21:44:40 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 30 Mar 2022 21:44:40 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 30 Mar 2022 21:44:41 GMT
EXPOSE 8888
# Wed, 30 Mar 2022 21:44:41 GMT
VOLUME [/var/lib/chronograf]
# Wed, 30 Mar 2022 21:44:42 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 30 Mar 2022 21:44:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 30 Mar 2022 21:44:42 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:072a4a410a8ca19c3bba361b4ad2205c16658c8130309a0ddc1b92d3d9fb8e7b`  
		Last Modified: Tue, 29 Mar 2022 02:41:11 GMT  
		Size: 19.4 MB (19359808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39844bbafdefabfb551a1b4ff17d8a5edc293968193149449875ebfdac27937a`  
		Last Modified: Wed, 30 Mar 2022 21:47:15 GMT  
		Size: 3.9 MB (3880277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a07b5a70b6f42c82c926fc7d2728a30a5626a13cb87fcb7c9287908a1fe7cc91`  
		Last Modified: Wed, 30 Mar 2022 21:47:33 GMT  
		Size: 35.8 MB (35783876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff6f5cbff3264c6b1435d226b049bed1ede02329fdbfd578d941c56f5eaff3a7`  
		Last Modified: Wed, 30 Mar 2022 21:47:13 GMT  
		Size: 12.2 KB (12244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aede3a0129c0ab157d7cb83f4ef7b833693fb7762b68fafaabafdb9dd69bff8`  
		Last Modified: Wed, 30 Mar 2022 21:47:13 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130d64973b14c354b674c0acaddd34cd4b209914fbde340a2d28adbcdda970a3`  
		Last Modified: Wed, 30 Mar 2022 21:47:13 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.7.17` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:da785f87397ffb30b1e9bc9d9424302ffcb839b46c22e2ac3904c8fc7840d6c3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60329478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30a14eaf7a6dded423824d24729dd141f875d50a82e9adfcd08bf972ca6f6240`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 29 Mar 2022 00:45:36 GMT
ADD file:e754ad83155f3f9d7419711eba00fb58e2d7be1ac24ec386b4ace6f1582bae31 in / 
# Tue, 29 Mar 2022 00:45:37 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 02:30:14 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 30 Mar 2022 02:30:15 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Wed, 30 Mar 2022 02:30:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 30 Mar 2022 02:30:32 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 30 Mar 2022 02:30:33 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 30 Mar 2022 02:30:33 GMT
EXPOSE 8888
# Wed, 30 Mar 2022 02:30:34 GMT
VOLUME [/var/lib/chronograf]
# Wed, 30 Mar 2022 02:30:36 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 30 Mar 2022 02:30:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 30 Mar 2022 02:30:37 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:fdcfc792a1f8b9e7f758eaa734b92858ca636af5571eac11c5da87ce721db2d5`  
		Last Modified: Tue, 29 Mar 2022 00:54:21 GMT  
		Size: 20.4 MB (20423743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd46d0499f095f9fa0c29a157cf9d6ff0fff80da52412f53f406e6c0f0d7412a`  
		Last Modified: Wed, 30 Mar 2022 02:32:04 GMT  
		Size: 3.9 MB (3894002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78bb4d065844d6e2e1d0264f3b006179b254a688ed544cd2ec99ec85c18f2cf7`  
		Last Modified: Wed, 30 Mar 2022 02:32:07 GMT  
		Size: 36.0 MB (35987346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4554f3c58f35cbbe81ea4ddff472cb7e4fa445cf20e2d029a90eb051ae2e25ba`  
		Last Modified: Wed, 30 Mar 2022 02:32:03 GMT  
		Size: 12.2 KB (12243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca2f5c18f5743263fe7c5badea4d67555d96b9a18928190a3f48d42aed313660`  
		Last Modified: Wed, 30 Mar 2022 02:32:03 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:593bc2bde7a2037d0118b77cb725930d7854fadd0acf022f781c885f46f07b3c`  
		Last Modified: Wed, 30 Mar 2022 02:32:03 GMT  
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
$ docker pull chronograf@sha256:30fd46bec3e203ba5c37dcdfaca36da308544613b553665f6a946892fdbcd66c
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
$ docker pull chronograf@sha256:a52a7d6ab60d74b8be6cd547183d4acf82e11627094ce0841408f23989d055ed
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59677109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29c7277b7b1c93920de116215606ce31fd6f4fb236b3dd4d1996724ccb7fb5a8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 29 Mar 2022 02:24:30 GMT
ADD file:a9cc850c256adf321d6c477c8875da7208938384cb764d33a90a78b2c0740a28 in / 
# Tue, 29 Mar 2022 02:24:31 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 21:43:18 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 30 Mar 2022 21:44:58 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Wed, 30 Mar 2022 21:45:18 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 30 Mar 2022 21:45:19 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 30 Mar 2022 21:45:19 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 30 Mar 2022 21:45:20 GMT
EXPOSE 8888
# Wed, 30 Mar 2022 21:45:20 GMT
VOLUME [/var/lib/chronograf]
# Wed, 30 Mar 2022 21:45:21 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 30 Mar 2022 21:45:21 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 30 Mar 2022 21:45:21 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:072a4a410a8ca19c3bba361b4ad2205c16658c8130309a0ddc1b92d3d9fb8e7b`  
		Last Modified: Tue, 29 Mar 2022 02:41:11 GMT  
		Size: 19.4 MB (19359808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0df16a38b9594b1f24af35716b84b3eff3b553f13abf4eccc7c2d6c29815fd5e`  
		Last Modified: Wed, 30 Mar 2022 21:46:52 GMT  
		Size: 5.8 MB (5780857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d92a7869c22b86738c3396e81eb96f2ea4e0360dfa916ec00c9c50ab2d4e0645`  
		Last Modified: Wed, 30 Mar 2022 21:48:04 GMT  
		Size: 34.5 MB (34512057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:317f97f67ababa24ad1c5525c1dd0cc56fb20434be42dd7168ca48c2cdbc0056`  
		Last Modified: Wed, 30 Mar 2022 21:47:45 GMT  
		Size: 12.2 KB (12243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1053d38d138f36a739b5705bfa54d7b56308409fd2e82f80d12e7d841b98ac99`  
		Last Modified: Wed, 30 Mar 2022 21:47:45 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:743746d3235b1e82e6209a6eff07680ec002baae2c266aa597964dbedadd95d4`  
		Last Modified: Wed, 30 Mar 2022 21:47:45 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.8` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:73d9b36a24cfec568fca776462243a01f70b8b8948e6e4e8f3b0e1f01e931d9b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60927239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52411caf09b3ee307c340b231a684168fcdef2532b7a03494c3981455cb413e5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 29 Mar 2022 00:45:36 GMT
ADD file:e754ad83155f3f9d7419711eba00fb58e2d7be1ac24ec386b4ace6f1582bae31 in / 
# Tue, 29 Mar 2022 00:45:37 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 02:29:45 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 30 Mar 2022 02:30:43 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Wed, 30 Mar 2022 02:30:52 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 30 Mar 2022 02:30:53 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 30 Mar 2022 02:30:54 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 30 Mar 2022 02:30:54 GMT
EXPOSE 8888
# Wed, 30 Mar 2022 02:30:55 GMT
VOLUME [/var/lib/chronograf]
# Wed, 30 Mar 2022 02:30:57 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 30 Mar 2022 02:30:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 30 Mar 2022 02:30:58 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:fdcfc792a1f8b9e7f758eaa734b92858ca636af5571eac11c5da87ce721db2d5`  
		Last Modified: Tue, 29 Mar 2022 00:54:21 GMT  
		Size: 20.4 MB (20423743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81e150d438592de367bca726042ec26ad6c7f34b79930a4d66ae91da4fa5d2ad`  
		Last Modified: Wed, 30 Mar 2022 02:31:50 GMT  
		Size: 6.0 MB (6047427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:214a36244dd76b12df3d682f78b165fd07ea379c1ce7b0d66f620d92ce72c945`  
		Last Modified: Wed, 30 Mar 2022 02:32:23 GMT  
		Size: 34.4 MB (34431682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30509c659f854ead8d1067ce3f0b38026a21863cf1501d544518467b5db241ed`  
		Last Modified: Wed, 30 Mar 2022 02:32:18 GMT  
		Size: 12.2 KB (12243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0d4784d17e0e94a4bbbc15664b97e9d0dda0a879c16bc554db9802ced39c41a`  
		Last Modified: Wed, 30 Mar 2022 02:32:19 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5bc4a33970f597831f438d79ca6ab1930b30294e7e36b85fe38a2fa34d10d51`  
		Last Modified: Wed, 30 Mar 2022 02:32:18 GMT  
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
$ docker pull chronograf@sha256:30fd46bec3e203ba5c37dcdfaca36da308544613b553665f6a946892fdbcd66c
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
$ docker pull chronograf@sha256:a52a7d6ab60d74b8be6cd547183d4acf82e11627094ce0841408f23989d055ed
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59677109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29c7277b7b1c93920de116215606ce31fd6f4fb236b3dd4d1996724ccb7fb5a8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 29 Mar 2022 02:24:30 GMT
ADD file:a9cc850c256adf321d6c477c8875da7208938384cb764d33a90a78b2c0740a28 in / 
# Tue, 29 Mar 2022 02:24:31 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 21:43:18 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 30 Mar 2022 21:44:58 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Wed, 30 Mar 2022 21:45:18 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 30 Mar 2022 21:45:19 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 30 Mar 2022 21:45:19 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 30 Mar 2022 21:45:20 GMT
EXPOSE 8888
# Wed, 30 Mar 2022 21:45:20 GMT
VOLUME [/var/lib/chronograf]
# Wed, 30 Mar 2022 21:45:21 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 30 Mar 2022 21:45:21 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 30 Mar 2022 21:45:21 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:072a4a410a8ca19c3bba361b4ad2205c16658c8130309a0ddc1b92d3d9fb8e7b`  
		Last Modified: Tue, 29 Mar 2022 02:41:11 GMT  
		Size: 19.4 MB (19359808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0df16a38b9594b1f24af35716b84b3eff3b553f13abf4eccc7c2d6c29815fd5e`  
		Last Modified: Wed, 30 Mar 2022 21:46:52 GMT  
		Size: 5.8 MB (5780857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d92a7869c22b86738c3396e81eb96f2ea4e0360dfa916ec00c9c50ab2d4e0645`  
		Last Modified: Wed, 30 Mar 2022 21:48:04 GMT  
		Size: 34.5 MB (34512057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:317f97f67ababa24ad1c5525c1dd0cc56fb20434be42dd7168ca48c2cdbc0056`  
		Last Modified: Wed, 30 Mar 2022 21:47:45 GMT  
		Size: 12.2 KB (12243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1053d38d138f36a739b5705bfa54d7b56308409fd2e82f80d12e7d841b98ac99`  
		Last Modified: Wed, 30 Mar 2022 21:47:45 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:743746d3235b1e82e6209a6eff07680ec002baae2c266aa597964dbedadd95d4`  
		Last Modified: Wed, 30 Mar 2022 21:47:45 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.8.10` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:73d9b36a24cfec568fca776462243a01f70b8b8948e6e4e8f3b0e1f01e931d9b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60927239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52411caf09b3ee307c340b231a684168fcdef2532b7a03494c3981455cb413e5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 29 Mar 2022 00:45:36 GMT
ADD file:e754ad83155f3f9d7419711eba00fb58e2d7be1ac24ec386b4ace6f1582bae31 in / 
# Tue, 29 Mar 2022 00:45:37 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 02:29:45 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 30 Mar 2022 02:30:43 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Wed, 30 Mar 2022 02:30:52 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 30 Mar 2022 02:30:53 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 30 Mar 2022 02:30:54 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 30 Mar 2022 02:30:54 GMT
EXPOSE 8888
# Wed, 30 Mar 2022 02:30:55 GMT
VOLUME [/var/lib/chronograf]
# Wed, 30 Mar 2022 02:30:57 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 30 Mar 2022 02:30:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 30 Mar 2022 02:30:58 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:fdcfc792a1f8b9e7f758eaa734b92858ca636af5571eac11c5da87ce721db2d5`  
		Last Modified: Tue, 29 Mar 2022 00:54:21 GMT  
		Size: 20.4 MB (20423743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81e150d438592de367bca726042ec26ad6c7f34b79930a4d66ae91da4fa5d2ad`  
		Last Modified: Wed, 30 Mar 2022 02:31:50 GMT  
		Size: 6.0 MB (6047427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:214a36244dd76b12df3d682f78b165fd07ea379c1ce7b0d66f620d92ce72c945`  
		Last Modified: Wed, 30 Mar 2022 02:32:23 GMT  
		Size: 34.4 MB (34431682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30509c659f854ead8d1067ce3f0b38026a21863cf1501d544518467b5db241ed`  
		Last Modified: Wed, 30 Mar 2022 02:32:18 GMT  
		Size: 12.2 KB (12243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0d4784d17e0e94a4bbbc15664b97e9d0dda0a879c16bc554db9802ced39c41a`  
		Last Modified: Wed, 30 Mar 2022 02:32:19 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5bc4a33970f597831f438d79ca6ab1930b30294e7e36b85fe38a2fa34d10d51`  
		Last Modified: Wed, 30 Mar 2022 02:32:18 GMT  
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
$ docker pull chronograf@sha256:390710b78ab8172b84fd3902efb9768e3b78428fe9796a23af8945250a114ebc
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
$ docker pull chronograf@sha256:28c1b7c71cabf829b4b37b93039c14a6cc7332a7aa272849eaa2c7ab61f82c44
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.5 MB (60456614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43c36f88414ba3d88ce2b8cddf66d30c4f9aa5bb63dd79ee282f1bd095115b77`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 29 Mar 2022 02:24:30 GMT
ADD file:a9cc850c256adf321d6c477c8875da7208938384cb764d33a90a78b2c0740a28 in / 
# Tue, 29 Mar 2022 02:24:31 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 21:43:18 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 30 Mar 2022 21:45:32 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Wed, 30 Mar 2022 21:45:52 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 30 Mar 2022 21:45:53 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 30 Mar 2022 21:45:53 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 30 Mar 2022 21:45:54 GMT
EXPOSE 8888
# Wed, 30 Mar 2022 21:45:54 GMT
VOLUME [/var/lib/chronograf]
# Wed, 30 Mar 2022 21:45:54 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 30 Mar 2022 21:45:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 30 Mar 2022 21:45:55 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:072a4a410a8ca19c3bba361b4ad2205c16658c8130309a0ddc1b92d3d9fb8e7b`  
		Last Modified: Tue, 29 Mar 2022 02:41:11 GMT  
		Size: 19.4 MB (19359808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0df16a38b9594b1f24af35716b84b3eff3b553f13abf4eccc7c2d6c29815fd5e`  
		Last Modified: Wed, 30 Mar 2022 21:46:52 GMT  
		Size: 5.8 MB (5780857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b689b28ec0f5fd9867512745dc95fcf50974220dcf21696a0e8329b3e2dac77`  
		Last Modified: Wed, 30 Mar 2022 21:48:35 GMT  
		Size: 35.3 MB (35291555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e476ad8f658d4588b03fbdbd118bc712e22585375ba53ea48fea4d048f29ebc`  
		Last Modified: Wed, 30 Mar 2022 21:48:16 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4f12729090779afe0bec275f3ef8a4e06c6e35e57eb722a40d99ad29ad16635`  
		Last Modified: Wed, 30 Mar 2022 21:48:16 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e002a22ed7522b00cef8b18b76c52df13429e78ba0db0e873e198dc02a1514e6`  
		Last Modified: Wed, 30 Mar 2022 21:48:15 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.9` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:a5e31eeae87dc2cf51d401b4c1adb942d8748b7f0e795acda9ef1c803095ec4b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61669666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:251f8e464f4cc70cf31bbd3319ea4344ffd48756fee5399a80679d13b1f99915`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 29 Mar 2022 00:45:36 GMT
ADD file:e754ad83155f3f9d7419711eba00fb58e2d7be1ac24ec386b4ace6f1582bae31 in / 
# Tue, 29 Mar 2022 00:45:37 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 02:29:45 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 30 Mar 2022 02:31:05 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Wed, 30 Mar 2022 02:31:14 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 30 Mar 2022 02:31:16 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 30 Mar 2022 02:31:17 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 30 Mar 2022 02:31:17 GMT
EXPOSE 8888
# Wed, 30 Mar 2022 02:31:18 GMT
VOLUME [/var/lib/chronograf]
# Wed, 30 Mar 2022 02:31:20 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 30 Mar 2022 02:31:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 30 Mar 2022 02:31:21 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:fdcfc792a1f8b9e7f758eaa734b92858ca636af5571eac11c5da87ce721db2d5`  
		Last Modified: Tue, 29 Mar 2022 00:54:21 GMT  
		Size: 20.4 MB (20423743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81e150d438592de367bca726042ec26ad6c7f34b79930a4d66ae91da4fa5d2ad`  
		Last Modified: Wed, 30 Mar 2022 02:31:50 GMT  
		Size: 6.0 MB (6047427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30f6ef2f73b73fa91f89e265c36c697702f9f513a740cf2859f5ef2ae32ccaaa`  
		Last Modified: Wed, 30 Mar 2022 02:32:39 GMT  
		Size: 35.2 MB (35174111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bba3963407622d3e2a358b0e2d859011d8174246b7b5cadfaf3a03318a6c96a`  
		Last Modified: Wed, 30 Mar 2022 02:32:35 GMT  
		Size: 12.2 KB (12242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a82e13dc8eba72a06ef8ab6cfc6ae95b3d87f6549e7c8ce313e5cf5fc8a066b9`  
		Last Modified: Wed, 30 Mar 2022 02:32:35 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c5bed435e30f4673d5ce94c92c7cdc0dfb187e6aac6fe6cb8c68fe9aee16e44`  
		Last Modified: Wed, 30 Mar 2022 02:32:35 GMT  
		Size: 239.0 B  
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
$ docker pull chronograf@sha256:390710b78ab8172b84fd3902efb9768e3b78428fe9796a23af8945250a114ebc
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
$ docker pull chronograf@sha256:28c1b7c71cabf829b4b37b93039c14a6cc7332a7aa272849eaa2c7ab61f82c44
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.5 MB (60456614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43c36f88414ba3d88ce2b8cddf66d30c4f9aa5bb63dd79ee282f1bd095115b77`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 29 Mar 2022 02:24:30 GMT
ADD file:a9cc850c256adf321d6c477c8875da7208938384cb764d33a90a78b2c0740a28 in / 
# Tue, 29 Mar 2022 02:24:31 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 21:43:18 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 30 Mar 2022 21:45:32 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Wed, 30 Mar 2022 21:45:52 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 30 Mar 2022 21:45:53 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 30 Mar 2022 21:45:53 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 30 Mar 2022 21:45:54 GMT
EXPOSE 8888
# Wed, 30 Mar 2022 21:45:54 GMT
VOLUME [/var/lib/chronograf]
# Wed, 30 Mar 2022 21:45:54 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 30 Mar 2022 21:45:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 30 Mar 2022 21:45:55 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:072a4a410a8ca19c3bba361b4ad2205c16658c8130309a0ddc1b92d3d9fb8e7b`  
		Last Modified: Tue, 29 Mar 2022 02:41:11 GMT  
		Size: 19.4 MB (19359808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0df16a38b9594b1f24af35716b84b3eff3b553f13abf4eccc7c2d6c29815fd5e`  
		Last Modified: Wed, 30 Mar 2022 21:46:52 GMT  
		Size: 5.8 MB (5780857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b689b28ec0f5fd9867512745dc95fcf50974220dcf21696a0e8329b3e2dac77`  
		Last Modified: Wed, 30 Mar 2022 21:48:35 GMT  
		Size: 35.3 MB (35291555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e476ad8f658d4588b03fbdbd118bc712e22585375ba53ea48fea4d048f29ebc`  
		Last Modified: Wed, 30 Mar 2022 21:48:16 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4f12729090779afe0bec275f3ef8a4e06c6e35e57eb722a40d99ad29ad16635`  
		Last Modified: Wed, 30 Mar 2022 21:48:16 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e002a22ed7522b00cef8b18b76c52df13429e78ba0db0e873e198dc02a1514e6`  
		Last Modified: Wed, 30 Mar 2022 21:48:15 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.9.4` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:a5e31eeae87dc2cf51d401b4c1adb942d8748b7f0e795acda9ef1c803095ec4b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61669666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:251f8e464f4cc70cf31bbd3319ea4344ffd48756fee5399a80679d13b1f99915`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 29 Mar 2022 00:45:36 GMT
ADD file:e754ad83155f3f9d7419711eba00fb58e2d7be1ac24ec386b4ace6f1582bae31 in / 
# Tue, 29 Mar 2022 00:45:37 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 02:29:45 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 30 Mar 2022 02:31:05 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Wed, 30 Mar 2022 02:31:14 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 30 Mar 2022 02:31:16 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 30 Mar 2022 02:31:17 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 30 Mar 2022 02:31:17 GMT
EXPOSE 8888
# Wed, 30 Mar 2022 02:31:18 GMT
VOLUME [/var/lib/chronograf]
# Wed, 30 Mar 2022 02:31:20 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 30 Mar 2022 02:31:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 30 Mar 2022 02:31:21 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:fdcfc792a1f8b9e7f758eaa734b92858ca636af5571eac11c5da87ce721db2d5`  
		Last Modified: Tue, 29 Mar 2022 00:54:21 GMT  
		Size: 20.4 MB (20423743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81e150d438592de367bca726042ec26ad6c7f34b79930a4d66ae91da4fa5d2ad`  
		Last Modified: Wed, 30 Mar 2022 02:31:50 GMT  
		Size: 6.0 MB (6047427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30f6ef2f73b73fa91f89e265c36c697702f9f513a740cf2859f5ef2ae32ccaaa`  
		Last Modified: Wed, 30 Mar 2022 02:32:39 GMT  
		Size: 35.2 MB (35174111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bba3963407622d3e2a358b0e2d859011d8174246b7b5cadfaf3a03318a6c96a`  
		Last Modified: Wed, 30 Mar 2022 02:32:35 GMT  
		Size: 12.2 KB (12242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a82e13dc8eba72a06ef8ab6cfc6ae95b3d87f6549e7c8ce313e5cf5fc8a066b9`  
		Last Modified: Wed, 30 Mar 2022 02:32:35 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c5bed435e30f4673d5ce94c92c7cdc0dfb187e6aac6fe6cb8c68fe9aee16e44`  
		Last Modified: Wed, 30 Mar 2022 02:32:35 GMT  
		Size: 239.0 B  
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
$ docker pull chronograf@sha256:390710b78ab8172b84fd3902efb9768e3b78428fe9796a23af8945250a114ebc
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
$ docker pull chronograf@sha256:28c1b7c71cabf829b4b37b93039c14a6cc7332a7aa272849eaa2c7ab61f82c44
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.5 MB (60456614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43c36f88414ba3d88ce2b8cddf66d30c4f9aa5bb63dd79ee282f1bd095115b77`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 29 Mar 2022 02:24:30 GMT
ADD file:a9cc850c256adf321d6c477c8875da7208938384cb764d33a90a78b2c0740a28 in / 
# Tue, 29 Mar 2022 02:24:31 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 21:43:18 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 30 Mar 2022 21:45:32 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Wed, 30 Mar 2022 21:45:52 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 30 Mar 2022 21:45:53 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 30 Mar 2022 21:45:53 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 30 Mar 2022 21:45:54 GMT
EXPOSE 8888
# Wed, 30 Mar 2022 21:45:54 GMT
VOLUME [/var/lib/chronograf]
# Wed, 30 Mar 2022 21:45:54 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 30 Mar 2022 21:45:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 30 Mar 2022 21:45:55 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:072a4a410a8ca19c3bba361b4ad2205c16658c8130309a0ddc1b92d3d9fb8e7b`  
		Last Modified: Tue, 29 Mar 2022 02:41:11 GMT  
		Size: 19.4 MB (19359808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0df16a38b9594b1f24af35716b84b3eff3b553f13abf4eccc7c2d6c29815fd5e`  
		Last Modified: Wed, 30 Mar 2022 21:46:52 GMT  
		Size: 5.8 MB (5780857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b689b28ec0f5fd9867512745dc95fcf50974220dcf21696a0e8329b3e2dac77`  
		Last Modified: Wed, 30 Mar 2022 21:48:35 GMT  
		Size: 35.3 MB (35291555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e476ad8f658d4588b03fbdbd118bc712e22585375ba53ea48fea4d048f29ebc`  
		Last Modified: Wed, 30 Mar 2022 21:48:16 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4f12729090779afe0bec275f3ef8a4e06c6e35e57eb722a40d99ad29ad16635`  
		Last Modified: Wed, 30 Mar 2022 21:48:16 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e002a22ed7522b00cef8b18b76c52df13429e78ba0db0e873e198dc02a1514e6`  
		Last Modified: Wed, 30 Mar 2022 21:48:15 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:latest` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:a5e31eeae87dc2cf51d401b4c1adb942d8748b7f0e795acda9ef1c803095ec4b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61669666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:251f8e464f4cc70cf31bbd3319ea4344ffd48756fee5399a80679d13b1f99915`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 29 Mar 2022 00:45:36 GMT
ADD file:e754ad83155f3f9d7419711eba00fb58e2d7be1ac24ec386b4ace6f1582bae31 in / 
# Tue, 29 Mar 2022 00:45:37 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 02:29:45 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 30 Mar 2022 02:31:05 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Wed, 30 Mar 2022 02:31:14 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 30 Mar 2022 02:31:16 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 30 Mar 2022 02:31:17 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 30 Mar 2022 02:31:17 GMT
EXPOSE 8888
# Wed, 30 Mar 2022 02:31:18 GMT
VOLUME [/var/lib/chronograf]
# Wed, 30 Mar 2022 02:31:20 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 30 Mar 2022 02:31:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 30 Mar 2022 02:31:21 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:fdcfc792a1f8b9e7f758eaa734b92858ca636af5571eac11c5da87ce721db2d5`  
		Last Modified: Tue, 29 Mar 2022 00:54:21 GMT  
		Size: 20.4 MB (20423743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81e150d438592de367bca726042ec26ad6c7f34b79930a4d66ae91da4fa5d2ad`  
		Last Modified: Wed, 30 Mar 2022 02:31:50 GMT  
		Size: 6.0 MB (6047427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30f6ef2f73b73fa91f89e265c36c697702f9f513a740cf2859f5ef2ae32ccaaa`  
		Last Modified: Wed, 30 Mar 2022 02:32:39 GMT  
		Size: 35.2 MB (35174111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bba3963407622d3e2a358b0e2d859011d8174246b7b5cadfaf3a03318a6c96a`  
		Last Modified: Wed, 30 Mar 2022 02:32:35 GMT  
		Size: 12.2 KB (12242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a82e13dc8eba72a06ef8ab6cfc6ae95b3d87f6549e7c8ce313e5cf5fc8a066b9`  
		Last Modified: Wed, 30 Mar 2022 02:32:35 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c5bed435e30f4673d5ce94c92c7cdc0dfb187e6aac6fe6cb8c68fe9aee16e44`  
		Last Modified: Wed, 30 Mar 2022 02:32:35 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
