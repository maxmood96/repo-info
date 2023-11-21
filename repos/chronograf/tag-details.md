<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `chronograf`

-	[`chronograf:1.10`](#chronograf110)
-	[`chronograf:1.10-alpine`](#chronograf110-alpine)
-	[`chronograf:1.10.2`](#chronograf1102)
-	[`chronograf:1.10.2-alpine`](#chronograf1102-alpine)
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
$ docker pull chronograf@sha256:1afe04050c8d702be216a813a21ef7e340e16b7fc4fb5f3a778a38db3581f0fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.10` - linux; amd64

```console
$ docker pull chronograf@sha256:380dde297f323ba57a0b07ca849a6c7582e05a7cd52577d44dce054bb502d2cf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.1 MB (84101080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1a8a073dfc63164af1a2f1bd67da6e4fbda63b5b6c1e8b8ab05060fac70496d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:37 GMT
ADD file:d261a6f6921593f1e0b3f472ab1b1822e2c6deb0b369200f0b3370556bfad017 in / 
# Tue, 21 Nov 2023 05:21:37 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 10:46:29 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 21 Nov 2023 10:46:29 GMT
ENV CHRONOGRAF_VERSION=1.10.2
# Tue, 21 Nov 2023 10:46:38 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 21 Nov 2023 10:46:38 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 21 Nov 2023 10:46:38 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 21 Nov 2023 10:46:38 GMT
EXPOSE 8888
# Tue, 21 Nov 2023 10:46:38 GMT
VOLUME [/var/lib/chronograf]
# Tue, 21 Nov 2023 10:46:38 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 21 Nov 2023 10:46:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Nov 2023 10:46:38 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:1f7ce2fa46ab3942feabee654933948821303a5a821789dddab2d8c3df59e227`  
		Last Modified: Tue, 21 Nov 2023 05:25:58 GMT  
		Size: 29.1 MB (29149908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1956287ac9cfdc19991d482f7cfe094a5236d159dca178b0e4e2888989901d13`  
		Last Modified: Tue, 21 Nov 2023 10:47:39 GMT  
		Size: 7.9 MB (7873073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fb62f985c03da59f7ba67ba98ea4eff8aac143fc92e81898567003bca5c00af`  
		Last Modified: Tue, 21 Nov 2023 10:47:43 GMT  
		Size: 47.1 MB (47053706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8b385f9ed0e852b69a364d9c189f846eb9f1df339ad58cb86610d69e86d8cb4`  
		Last Modified: Tue, 21 Nov 2023 10:47:37 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deb06199f978c7bf17a871d0668ac1245f63349368d3a416f8788268c921a171`  
		Last Modified: Tue, 21 Nov 2023 10:47:37 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c18d5e09745fe375af5895b0b1c99d8110d4704ec58d7c7df8619dc1622f8dcc`  
		Last Modified: Tue, 21 Nov 2023 10:47:37 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.10` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:3024f41d59a015cc2c86ad2aa2e0f1abb4b882b9345c6a43f7b600bf2d8af65e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75920715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2332571a6259070e1637d40b140c79fa917f32e446565a38a7a90649f0b12b57`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 21 Nov 2023 03:57:43 GMT
ADD file:b693944382a95fa47622fde77eb98f0cdeafa40261e7334bd355e00f650b6632 in / 
# Tue, 21 Nov 2023 03:57:43 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:02:00 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 21 Nov 2023 07:02:00 GMT
ENV CHRONOGRAF_VERSION=1.10.2
# Tue, 21 Nov 2023 07:02:10 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 21 Nov 2023 07:02:10 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 21 Nov 2023 07:02:10 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 21 Nov 2023 07:02:10 GMT
EXPOSE 8888
# Tue, 21 Nov 2023 07:02:11 GMT
VOLUME [/var/lib/chronograf]
# Tue, 21 Nov 2023 07:02:11 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 21 Nov 2023 07:02:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Nov 2023 07:02:11 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:b4ce590529bbcf84326048a22fce76fcfcb5c60af5519debd7935a74c1e9126e`  
		Last Modified: Tue, 21 Nov 2023 04:01:50 GMT  
		Size: 24.7 MB (24748925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a72f2ea3c3dd4c6c84869aff33141879c89aed7d1ebdee23dd5cc143fbe8c2`  
		Last Modified: Tue, 21 Nov 2023 07:03:02 GMT  
		Size: 6.5 MB (6497812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26311c9696c337908f2631c213e79d0c72849a72085fde9380f35a1c67ed28fa`  
		Last Modified: Tue, 21 Nov 2023 07:03:08 GMT  
		Size: 44.6 MB (44649586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aac8f1e393f681f858ed71dbc056c8a255df814677dc93f57014c85a6411f5bc`  
		Last Modified: Tue, 21 Nov 2023 07:03:01 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65c8c90cbbd08d52d14449a9108f380a4fd480b83a4a28fdef9ccae09f49738f`  
		Last Modified: Tue, 21 Nov 2023 07:03:01 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1527e2aad92573d1f8276fe9286d5379b57115a489a28173509391bf2c65c2a3`  
		Last Modified: Tue, 21 Nov 2023 07:03:01 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.10` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:907da70564d00845356dabad9cb329f113e7642486d3ec24208ea93466beb07c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.6 MB (81627266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9355053d09268aef0f21bada565fd0029a482328b07884f0e71fcc8b9834721d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:06 GMT
ADD file:869c7d0747a17c53715581a2e862992eb8516c7f45f167821dfa80966a4870d1 in / 
# Tue, 21 Nov 2023 06:27:06 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:56:05 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 21 Nov 2023 07:56:05 GMT
ENV CHRONOGRAF_VERSION=1.10.2
# Tue, 21 Nov 2023 07:56:12 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 21 Nov 2023 07:56:13 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 21 Nov 2023 07:56:13 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 21 Nov 2023 07:56:13 GMT
EXPOSE 8888
# Tue, 21 Nov 2023 07:56:13 GMT
VOLUME [/var/lib/chronograf]
# Tue, 21 Nov 2023 07:56:13 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 21 Nov 2023 07:56:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Nov 2023 07:56:13 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:2c6d21737d8318aa15c4cc838475029a5efc36c0429e3d8da80d97d0b96d9aaf`  
		Last Modified: Tue, 21 Nov 2023 06:30:30 GMT  
		Size: 29.2 MB (29179277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63f93356fcd55f6426d456c26d4a5e38da0bb544a18f1666780fa447b8eed55d`  
		Last Modified: Tue, 21 Nov 2023 07:57:00 GMT  
		Size: 7.6 MB (7649760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32eb3d345558481a7c6da4301adcd44374730662770cf8edb7b7c82f9c44ad26`  
		Last Modified: Tue, 21 Nov 2023 07:57:04 GMT  
		Size: 44.8 MB (44773832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1417ae54eecd2b37aef5ab9b854f4a8641033587d30e3ce30f765091c47afd4`  
		Last Modified: Tue, 21 Nov 2023 07:56:59 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:103dd685ae00f8ca4c49f165c1dc572de1b4e2510dcdbb20a96f9b963a831e69`  
		Last Modified: Tue, 21 Nov 2023 07:56:59 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ace178832cf7524abb72847cc73615fb748c94a3583f08add64d5938d2d0512`  
		Last Modified: Tue, 21 Nov 2023 07:56:59 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.10-alpine`

```console
$ docker pull chronograf@sha256:7530358bc4ca04eb208da945243c805590bf122d3261f8a97fabc0d8a89bf622
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.10-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:fb43ec35ddd6e58cc2e78ef58f797cb6de9067c3932e3db1f85a4aea80fb6751
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.6 MB (31558951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b55651823a683848ddd413718b400ba4b653ea7e671921241f5a3604a2cef16d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Tue, 17 Oct 2023 01:30:37 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 21 Oct 2023 02:34:58 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Tue, 24 Oct 2023 00:20:11 GMT
ENV CHRONOGRAF_VERSION=1.10.2
# Tue, 24 Oct 2023 00:20:16 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Tue, 24 Oct 2023 00:20:16 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 24 Oct 2023 00:20:16 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 24 Oct 2023 00:20:16 GMT
EXPOSE 8888
# Tue, 24 Oct 2023 00:20:16 GMT
VOLUME [/var/lib/chronograf]
# Tue, 24 Oct 2023 00:20:16 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Tue, 24 Oct 2023 00:20:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Oct 2023 00:20:17 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f5352bf3aec614dde8ac36d38f28f5021eff4c2ff0226eb22dfa667f2b2add1`  
		Last Modified: Tue, 17 Oct 2023 01:33:20 GMT  
		Size: 281.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4048f49511dda4f4f68ff84317685f405a4090adcf74b1c9c7116e71ae80d30a`  
		Last Modified: Sat, 21 Oct 2023 02:35:44 GMT  
		Size: 284.7 KB (284698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6545ebb960dd3a534da359758d3fec7757e7866b3655ad8432156ab58b56bf56`  
		Last Modified: Tue, 24 Oct 2023 00:21:04 GMT  
		Size: 27.8 MB (27847599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c28322186901948002f5674f518fd78626ce89862f988bcfbfe22b03a9868134`  
		Last Modified: Tue, 24 Oct 2023 00:20:58 GMT  
		Size: 12.3 KB (12268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d268d1b30ec9afb6cf8ac11fe77068afa5f6b2e2211c3e2861d51f122b8b5e07`  
		Last Modified: Tue, 24 Oct 2023 00:20:59 GMT  
		Size: 11.9 KB (11900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c48929913d0bb1a8ca03b3dfcd0cfded77493e0142ff4fd446ca1f7bfbed9bd`  
		Last Modified: Tue, 24 Oct 2023 00:20:58 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.10.2`

```console
$ docker pull chronograf@sha256:1afe04050c8d702be216a813a21ef7e340e16b7fc4fb5f3a778a38db3581f0fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.10.2` - linux; amd64

```console
$ docker pull chronograf@sha256:380dde297f323ba57a0b07ca849a6c7582e05a7cd52577d44dce054bb502d2cf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.1 MB (84101080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1a8a073dfc63164af1a2f1bd67da6e4fbda63b5b6c1e8b8ab05060fac70496d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:37 GMT
ADD file:d261a6f6921593f1e0b3f472ab1b1822e2c6deb0b369200f0b3370556bfad017 in / 
# Tue, 21 Nov 2023 05:21:37 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 10:46:29 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 21 Nov 2023 10:46:29 GMT
ENV CHRONOGRAF_VERSION=1.10.2
# Tue, 21 Nov 2023 10:46:38 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 21 Nov 2023 10:46:38 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 21 Nov 2023 10:46:38 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 21 Nov 2023 10:46:38 GMT
EXPOSE 8888
# Tue, 21 Nov 2023 10:46:38 GMT
VOLUME [/var/lib/chronograf]
# Tue, 21 Nov 2023 10:46:38 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 21 Nov 2023 10:46:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Nov 2023 10:46:38 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:1f7ce2fa46ab3942feabee654933948821303a5a821789dddab2d8c3df59e227`  
		Last Modified: Tue, 21 Nov 2023 05:25:58 GMT  
		Size: 29.1 MB (29149908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1956287ac9cfdc19991d482f7cfe094a5236d159dca178b0e4e2888989901d13`  
		Last Modified: Tue, 21 Nov 2023 10:47:39 GMT  
		Size: 7.9 MB (7873073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fb62f985c03da59f7ba67ba98ea4eff8aac143fc92e81898567003bca5c00af`  
		Last Modified: Tue, 21 Nov 2023 10:47:43 GMT  
		Size: 47.1 MB (47053706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8b385f9ed0e852b69a364d9c189f846eb9f1df339ad58cb86610d69e86d8cb4`  
		Last Modified: Tue, 21 Nov 2023 10:47:37 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deb06199f978c7bf17a871d0668ac1245f63349368d3a416f8788268c921a171`  
		Last Modified: Tue, 21 Nov 2023 10:47:37 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c18d5e09745fe375af5895b0b1c99d8110d4704ec58d7c7df8619dc1622f8dcc`  
		Last Modified: Tue, 21 Nov 2023 10:47:37 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.10.2` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:3024f41d59a015cc2c86ad2aa2e0f1abb4b882b9345c6a43f7b600bf2d8af65e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75920715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2332571a6259070e1637d40b140c79fa917f32e446565a38a7a90649f0b12b57`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 21 Nov 2023 03:57:43 GMT
ADD file:b693944382a95fa47622fde77eb98f0cdeafa40261e7334bd355e00f650b6632 in / 
# Tue, 21 Nov 2023 03:57:43 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:02:00 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 21 Nov 2023 07:02:00 GMT
ENV CHRONOGRAF_VERSION=1.10.2
# Tue, 21 Nov 2023 07:02:10 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 21 Nov 2023 07:02:10 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 21 Nov 2023 07:02:10 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 21 Nov 2023 07:02:10 GMT
EXPOSE 8888
# Tue, 21 Nov 2023 07:02:11 GMT
VOLUME [/var/lib/chronograf]
# Tue, 21 Nov 2023 07:02:11 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 21 Nov 2023 07:02:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Nov 2023 07:02:11 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:b4ce590529bbcf84326048a22fce76fcfcb5c60af5519debd7935a74c1e9126e`  
		Last Modified: Tue, 21 Nov 2023 04:01:50 GMT  
		Size: 24.7 MB (24748925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a72f2ea3c3dd4c6c84869aff33141879c89aed7d1ebdee23dd5cc143fbe8c2`  
		Last Modified: Tue, 21 Nov 2023 07:03:02 GMT  
		Size: 6.5 MB (6497812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26311c9696c337908f2631c213e79d0c72849a72085fde9380f35a1c67ed28fa`  
		Last Modified: Tue, 21 Nov 2023 07:03:08 GMT  
		Size: 44.6 MB (44649586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aac8f1e393f681f858ed71dbc056c8a255df814677dc93f57014c85a6411f5bc`  
		Last Modified: Tue, 21 Nov 2023 07:03:01 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65c8c90cbbd08d52d14449a9108f380a4fd480b83a4a28fdef9ccae09f49738f`  
		Last Modified: Tue, 21 Nov 2023 07:03:01 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1527e2aad92573d1f8276fe9286d5379b57115a489a28173509391bf2c65c2a3`  
		Last Modified: Tue, 21 Nov 2023 07:03:01 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.10.2` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:907da70564d00845356dabad9cb329f113e7642486d3ec24208ea93466beb07c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.6 MB (81627266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9355053d09268aef0f21bada565fd0029a482328b07884f0e71fcc8b9834721d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:06 GMT
ADD file:869c7d0747a17c53715581a2e862992eb8516c7f45f167821dfa80966a4870d1 in / 
# Tue, 21 Nov 2023 06:27:06 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:56:05 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 21 Nov 2023 07:56:05 GMT
ENV CHRONOGRAF_VERSION=1.10.2
# Tue, 21 Nov 2023 07:56:12 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 21 Nov 2023 07:56:13 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 21 Nov 2023 07:56:13 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 21 Nov 2023 07:56:13 GMT
EXPOSE 8888
# Tue, 21 Nov 2023 07:56:13 GMT
VOLUME [/var/lib/chronograf]
# Tue, 21 Nov 2023 07:56:13 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 21 Nov 2023 07:56:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Nov 2023 07:56:13 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:2c6d21737d8318aa15c4cc838475029a5efc36c0429e3d8da80d97d0b96d9aaf`  
		Last Modified: Tue, 21 Nov 2023 06:30:30 GMT  
		Size: 29.2 MB (29179277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63f93356fcd55f6426d456c26d4a5e38da0bb544a18f1666780fa447b8eed55d`  
		Last Modified: Tue, 21 Nov 2023 07:57:00 GMT  
		Size: 7.6 MB (7649760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32eb3d345558481a7c6da4301adcd44374730662770cf8edb7b7c82f9c44ad26`  
		Last Modified: Tue, 21 Nov 2023 07:57:04 GMT  
		Size: 44.8 MB (44773832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1417ae54eecd2b37aef5ab9b854f4a8641033587d30e3ce30f765091c47afd4`  
		Last Modified: Tue, 21 Nov 2023 07:56:59 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:103dd685ae00f8ca4c49f165c1dc572de1b4e2510dcdbb20a96f9b963a831e69`  
		Last Modified: Tue, 21 Nov 2023 07:56:59 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ace178832cf7524abb72847cc73615fb748c94a3583f08add64d5938d2d0512`  
		Last Modified: Tue, 21 Nov 2023 07:56:59 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.10.2-alpine`

```console
$ docker pull chronograf@sha256:7530358bc4ca04eb208da945243c805590bf122d3261f8a97fabc0d8a89bf622
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.10.2-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:fb43ec35ddd6e58cc2e78ef58f797cb6de9067c3932e3db1f85a4aea80fb6751
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.6 MB (31558951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b55651823a683848ddd413718b400ba4b653ea7e671921241f5a3604a2cef16d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Tue, 17 Oct 2023 01:30:37 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 21 Oct 2023 02:34:58 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Tue, 24 Oct 2023 00:20:11 GMT
ENV CHRONOGRAF_VERSION=1.10.2
# Tue, 24 Oct 2023 00:20:16 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Tue, 24 Oct 2023 00:20:16 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 24 Oct 2023 00:20:16 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 24 Oct 2023 00:20:16 GMT
EXPOSE 8888
# Tue, 24 Oct 2023 00:20:16 GMT
VOLUME [/var/lib/chronograf]
# Tue, 24 Oct 2023 00:20:16 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Tue, 24 Oct 2023 00:20:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Oct 2023 00:20:17 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f5352bf3aec614dde8ac36d38f28f5021eff4c2ff0226eb22dfa667f2b2add1`  
		Last Modified: Tue, 17 Oct 2023 01:33:20 GMT  
		Size: 281.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4048f49511dda4f4f68ff84317685f405a4090adcf74b1c9c7116e71ae80d30a`  
		Last Modified: Sat, 21 Oct 2023 02:35:44 GMT  
		Size: 284.7 KB (284698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6545ebb960dd3a534da359758d3fec7757e7866b3655ad8432156ab58b56bf56`  
		Last Modified: Tue, 24 Oct 2023 00:21:04 GMT  
		Size: 27.8 MB (27847599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c28322186901948002f5674f518fd78626ce89862f988bcfbfe22b03a9868134`  
		Last Modified: Tue, 24 Oct 2023 00:20:58 GMT  
		Size: 12.3 KB (12268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d268d1b30ec9afb6cf8ac11fe77068afa5f6b2e2211c3e2861d51f122b8b5e07`  
		Last Modified: Tue, 24 Oct 2023 00:20:59 GMT  
		Size: 11.9 KB (11900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c48929913d0bb1a8ca03b3dfcd0cfded77493e0142ff4fd446ca1f7bfbed9bd`  
		Last Modified: Tue, 24 Oct 2023 00:20:58 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.7`

```console
$ docker pull chronograf@sha256:a6f7397cde84e7340a3801d7532a6ac665dfacf009cefd6a6f03c12978e48a3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.7` - linux; amd64

```console
$ docker pull chronograf@sha256:471537ba9b54c8b3df5f71215c99853f35598b92e8a775405b8305b2d67abf60
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.6 MB (70598915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb48851de8a09203fd6db272eb6ceb889deadc7d563ce62bb57e9e64db3da506`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:58 GMT
ADD file:e9f63d1defc55282fec6525ac2886c735dc2189e34105d7fe64c2420d6673922 in / 
# Tue, 21 Nov 2023 05:21:58 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 10:45:32 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 21 Nov 2023 10:45:32 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 21 Nov 2023 10:45:41 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 21 Nov 2023 10:45:41 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 21 Nov 2023 10:45:41 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 21 Nov 2023 10:45:41 GMT
EXPOSE 8888
# Tue, 21 Nov 2023 10:45:41 GMT
VOLUME [/var/lib/chronograf]
# Tue, 21 Nov 2023 10:45:42 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 21 Nov 2023 10:45:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Nov 2023 10:45:42 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:b7f91549542cca4b35a34cdee5364339f17468971ea730bb072864d3e78c8b94`  
		Last Modified: Tue, 21 Nov 2023 05:26:39 GMT  
		Size: 31.4 MB (31417824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20c93c2a25d2d43c5990c170bc93651b61dc8519dbd390858f440c222bafaa76`  
		Last Modified: Tue, 21 Nov 2023 10:46:58 GMT  
		Size: 4.4 MB (4417343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eacf7f9eff1795c3a68b7b0ba51579906baacff04e148fa6172c4c59ccf2b410`  
		Last Modified: Tue, 21 Nov 2023 10:47:01 GMT  
		Size: 34.7 MB (34739356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7606812b08ae164036e3e6c1ffe08933b900cebf2cca4b6392aafec32d9495d1`  
		Last Modified: Tue, 21 Nov 2023 10:46:57 GMT  
		Size: 12.2 KB (12244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a6c12e0a6fa3d9d918dd5f58722b9c1b7d90f1c9445e4c02fb47144da775444`  
		Last Modified: Tue, 21 Nov 2023 10:46:57 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7fa14465a4aace867eb2740c9abf902726bf379fa5b4db3d36753285ce86a6b`  
		Last Modified: Tue, 21 Nov 2023 10:46:57 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.7` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:d0300a90632d0d54673c7f58e247b0a3ff53d0db8f0ee4973c89846a3cbb7540
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.4 MB (63422558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c4b37a1176db42fd799b1d7966125d45993f706a386395a05555e18d815433c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 21 Nov 2023 03:58:04 GMT
ADD file:c4afced274aaa80ab3018b368ed739c1c55e49b41e9637ac44d63e61344fe865 in / 
# Tue, 21 Nov 2023 03:58:04 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:01:02 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 21 Nov 2023 07:01:02 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 21 Nov 2023 07:01:11 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 21 Nov 2023 07:01:12 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 21 Nov 2023 07:01:12 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 21 Nov 2023 07:01:12 GMT
EXPOSE 8888
# Tue, 21 Nov 2023 07:01:12 GMT
VOLUME [/var/lib/chronograf]
# Tue, 21 Nov 2023 07:01:12 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 21 Nov 2023 07:01:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Nov 2023 07:01:13 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:6dc4ed5513793308b8e30b08e03f97fa54025c3d3f3172c6edccb1dbbc7ff139`  
		Last Modified: Tue, 21 Nov 2023 04:02:35 GMT  
		Size: 26.6 MB (26579014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4366746eae97bf8c56d53d420c3d99a7287f6ce1ae6d6070f415408aebd7a219`  
		Last Modified: Tue, 21 Nov 2023 07:02:23 GMT  
		Size: 3.7 MB (3719840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b14a408990c9b240c0747e8fda3c612bb4f30133aa58862bb13831bdce059b17`  
		Last Modified: Tue, 21 Nov 2023 07:02:28 GMT  
		Size: 33.1 MB (33099314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4b09abe85d1c50ccf9fee1064cdecfa50f745b2bbc10d8ec89108c71d4a2a31`  
		Last Modified: Tue, 21 Nov 2023 07:02:22 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6084651dfcfd4e3974ab6f9d8a768e0dadc201e19adcd95e7488b4ffaf13774b`  
		Last Modified: Tue, 21 Nov 2023 07:02:22 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c23f58543334945910621475981e59cd3e0b5e1ddbe002bedb410561ed91658`  
		Last Modified: Tue, 21 Nov 2023 07:02:22 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.7` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:9bce00653e56146450e22f303883cf5517d009403f353086651231a4b0b89989
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67747062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7a4ba3db8098ffa441c15eef23ce3d7fd140f78cda5812e25afb8e4f3c31c45`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:20 GMT
ADD file:7b5bbc3b85f671aaf7b38dbe3fc76aae162bbff29c525bcd127f8a26a53bc664 in / 
# Tue, 21 Nov 2023 06:27:21 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:55:21 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 21 Nov 2023 07:55:21 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 21 Nov 2023 07:55:28 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 21 Nov 2023 07:55:29 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 21 Nov 2023 07:55:29 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 21 Nov 2023 07:55:29 GMT
EXPOSE 8888
# Tue, 21 Nov 2023 07:55:29 GMT
VOLUME [/var/lib/chronograf]
# Tue, 21 Nov 2023 07:55:29 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 21 Nov 2023 07:55:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Nov 2023 07:55:29 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:ca426296fe928600d0b4b844aee43e2b70a05c6f4032de5f65dcc49f5cedfd82`  
		Last Modified: Tue, 21 Nov 2023 06:31:08 GMT  
		Size: 30.1 MB (30064123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bf26def9af2ce6036548615daf26833a54082927d7dd13c7a58bb328d1116bc`  
		Last Modified: Tue, 21 Nov 2023 07:56:24 GMT  
		Size: 4.4 MB (4418856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23a3634c35980d757a4b7d02eca3bc3c63cd59b4cbd8bfeb151116525c9ef43a`  
		Last Modified: Tue, 21 Nov 2023 07:56:27 GMT  
		Size: 33.2 MB (33239685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f1a11c4875f71b7ff3482cbbdc5431632460699f111f5b37af148d877513544`  
		Last Modified: Tue, 21 Nov 2023 07:56:24 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea39c01a141a092eb75db0c6e655c8a7fc7215b4744d7573e40c02d3e1ee72e`  
		Last Modified: Tue, 21 Nov 2023 07:56:24 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:892f7406764acfb69974a53e09c955afc966f6d695b93c39a3d9e77fc26242c1`  
		Last Modified: Tue, 21 Nov 2023 07:56:24 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.7-alpine`

```console
$ docker pull chronograf@sha256:62301ed8dd488c82101db47255be49e9986d8a25dac6fb4d2adeafe007e89efb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.7-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:24745c70055c5b34ce94a9f10ff0e038724bc65bc1299bdf1853086c5c99d150
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.2 MB (23245411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6757fd40e7a2442b1e9015bf7f4537bd61e551143b98599d0659018801dfcdb6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 07 Aug 2023 19:20:26 GMT
ADD file:6dd87346b8be240b21b4f4d9296253bf0d28b6579aa52d2118872e3936963b6b in / 
# Mon, 07 Aug 2023 19:20:26 GMT
CMD ["/bin/sh"]
# Tue, 17 Oct 2023 01:29:21 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 21 Oct 2023 00:12:27 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Sat, 21 Oct 2023 00:12:27 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Sat, 21 Oct 2023 00:12:33 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Sat, 21 Oct 2023 00:12:33 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Sat, 21 Oct 2023 00:12:33 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sat, 21 Oct 2023 00:12:33 GMT
EXPOSE 8888
# Sat, 21 Oct 2023 00:12:33 GMT
VOLUME [/var/lib/chronograf]
# Sat, 21 Oct 2023 00:12:33 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Sat, 21 Oct 2023 00:12:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 21 Oct 2023 00:12:33 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:9398808236ffac29e60c04ec906d8d409af7fa19dc57d8c65ad167e9c4967006`  
		Last Modified: Mon, 07 Aug 2023 19:21:08 GMT  
		Size: 3.4 MB (3378609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b161763ec9e11116a97547438c5541153248aba5eddc76475885813812367da`  
		Last Modified: Tue, 17 Oct 2023 01:31:50 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c036769ce42fe6069bea0e08abbf145ff40fb3519e68ec986c7aaf6b109ac7d5`  
		Last Modified: Sat, 21 Oct 2023 00:13:30 GMT  
		Size: 284.9 KB (284931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02062f55c3474493b57edcf76d3dfb180f6979574218338b17c7055e0dacdfb1`  
		Last Modified: Sat, 21 Oct 2023 00:13:33 GMT  
		Size: 19.6 MB (19557198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da33d48693c709e5812be997c1f8d1585b2038d8a3e9f07deae21538282754db`  
		Last Modified: Sat, 21 Oct 2023 00:13:30 GMT  
		Size: 12.3 KB (12262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caed337108b2c3a0c9bf35f3a66f7ed7a429550b4fbdd33ab5d231be9c2c89d9`  
		Last Modified: Sat, 21 Oct 2023 00:13:30 GMT  
		Size: 11.9 KB (11896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92a3663990537a0cc88299aff9b2651df091f1bbd4ee851fcf3787e25cacc8a0`  
		Last Modified: Sat, 21 Oct 2023 00:13:30 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.7.17`

```console
$ docker pull chronograf@sha256:a6f7397cde84e7340a3801d7532a6ac665dfacf009cefd6a6f03c12978e48a3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.7.17` - linux; amd64

```console
$ docker pull chronograf@sha256:471537ba9b54c8b3df5f71215c99853f35598b92e8a775405b8305b2d67abf60
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.6 MB (70598915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb48851de8a09203fd6db272eb6ceb889deadc7d563ce62bb57e9e64db3da506`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:58 GMT
ADD file:e9f63d1defc55282fec6525ac2886c735dc2189e34105d7fe64c2420d6673922 in / 
# Tue, 21 Nov 2023 05:21:58 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 10:45:32 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 21 Nov 2023 10:45:32 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 21 Nov 2023 10:45:41 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 21 Nov 2023 10:45:41 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 21 Nov 2023 10:45:41 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 21 Nov 2023 10:45:41 GMT
EXPOSE 8888
# Tue, 21 Nov 2023 10:45:41 GMT
VOLUME [/var/lib/chronograf]
# Tue, 21 Nov 2023 10:45:42 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 21 Nov 2023 10:45:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Nov 2023 10:45:42 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:b7f91549542cca4b35a34cdee5364339f17468971ea730bb072864d3e78c8b94`  
		Last Modified: Tue, 21 Nov 2023 05:26:39 GMT  
		Size: 31.4 MB (31417824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20c93c2a25d2d43c5990c170bc93651b61dc8519dbd390858f440c222bafaa76`  
		Last Modified: Tue, 21 Nov 2023 10:46:58 GMT  
		Size: 4.4 MB (4417343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eacf7f9eff1795c3a68b7b0ba51579906baacff04e148fa6172c4c59ccf2b410`  
		Last Modified: Tue, 21 Nov 2023 10:47:01 GMT  
		Size: 34.7 MB (34739356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7606812b08ae164036e3e6c1ffe08933b900cebf2cca4b6392aafec32d9495d1`  
		Last Modified: Tue, 21 Nov 2023 10:46:57 GMT  
		Size: 12.2 KB (12244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a6c12e0a6fa3d9d918dd5f58722b9c1b7d90f1c9445e4c02fb47144da775444`  
		Last Modified: Tue, 21 Nov 2023 10:46:57 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7fa14465a4aace867eb2740c9abf902726bf379fa5b4db3d36753285ce86a6b`  
		Last Modified: Tue, 21 Nov 2023 10:46:57 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.7.17` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:d0300a90632d0d54673c7f58e247b0a3ff53d0db8f0ee4973c89846a3cbb7540
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.4 MB (63422558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c4b37a1176db42fd799b1d7966125d45993f706a386395a05555e18d815433c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 21 Nov 2023 03:58:04 GMT
ADD file:c4afced274aaa80ab3018b368ed739c1c55e49b41e9637ac44d63e61344fe865 in / 
# Tue, 21 Nov 2023 03:58:04 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:01:02 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 21 Nov 2023 07:01:02 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 21 Nov 2023 07:01:11 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 21 Nov 2023 07:01:12 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 21 Nov 2023 07:01:12 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 21 Nov 2023 07:01:12 GMT
EXPOSE 8888
# Tue, 21 Nov 2023 07:01:12 GMT
VOLUME [/var/lib/chronograf]
# Tue, 21 Nov 2023 07:01:12 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 21 Nov 2023 07:01:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Nov 2023 07:01:13 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:6dc4ed5513793308b8e30b08e03f97fa54025c3d3f3172c6edccb1dbbc7ff139`  
		Last Modified: Tue, 21 Nov 2023 04:02:35 GMT  
		Size: 26.6 MB (26579014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4366746eae97bf8c56d53d420c3d99a7287f6ce1ae6d6070f415408aebd7a219`  
		Last Modified: Tue, 21 Nov 2023 07:02:23 GMT  
		Size: 3.7 MB (3719840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b14a408990c9b240c0747e8fda3c612bb4f30133aa58862bb13831bdce059b17`  
		Last Modified: Tue, 21 Nov 2023 07:02:28 GMT  
		Size: 33.1 MB (33099314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4b09abe85d1c50ccf9fee1064cdecfa50f745b2bbc10d8ec89108c71d4a2a31`  
		Last Modified: Tue, 21 Nov 2023 07:02:22 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6084651dfcfd4e3974ab6f9d8a768e0dadc201e19adcd95e7488b4ffaf13774b`  
		Last Modified: Tue, 21 Nov 2023 07:02:22 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c23f58543334945910621475981e59cd3e0b5e1ddbe002bedb410561ed91658`  
		Last Modified: Tue, 21 Nov 2023 07:02:22 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.7.17` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:9bce00653e56146450e22f303883cf5517d009403f353086651231a4b0b89989
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67747062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7a4ba3db8098ffa441c15eef23ce3d7fd140f78cda5812e25afb8e4f3c31c45`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:20 GMT
ADD file:7b5bbc3b85f671aaf7b38dbe3fc76aae162bbff29c525bcd127f8a26a53bc664 in / 
# Tue, 21 Nov 2023 06:27:21 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:55:21 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 21 Nov 2023 07:55:21 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 21 Nov 2023 07:55:28 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 21 Nov 2023 07:55:29 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 21 Nov 2023 07:55:29 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 21 Nov 2023 07:55:29 GMT
EXPOSE 8888
# Tue, 21 Nov 2023 07:55:29 GMT
VOLUME [/var/lib/chronograf]
# Tue, 21 Nov 2023 07:55:29 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 21 Nov 2023 07:55:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Nov 2023 07:55:29 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:ca426296fe928600d0b4b844aee43e2b70a05c6f4032de5f65dcc49f5cedfd82`  
		Last Modified: Tue, 21 Nov 2023 06:31:08 GMT  
		Size: 30.1 MB (30064123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bf26def9af2ce6036548615daf26833a54082927d7dd13c7a58bb328d1116bc`  
		Last Modified: Tue, 21 Nov 2023 07:56:24 GMT  
		Size: 4.4 MB (4418856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23a3634c35980d757a4b7d02eca3bc3c63cd59b4cbd8bfeb151116525c9ef43a`  
		Last Modified: Tue, 21 Nov 2023 07:56:27 GMT  
		Size: 33.2 MB (33239685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f1a11c4875f71b7ff3482cbbdc5431632460699f111f5b37af148d877513544`  
		Last Modified: Tue, 21 Nov 2023 07:56:24 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea39c01a141a092eb75db0c6e655c8a7fc7215b4744d7573e40c02d3e1ee72e`  
		Last Modified: Tue, 21 Nov 2023 07:56:24 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:892f7406764acfb69974a53e09c955afc966f6d695b93c39a3d9e77fc26242c1`  
		Last Modified: Tue, 21 Nov 2023 07:56:24 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.7.17-alpine`

```console
$ docker pull chronograf@sha256:62301ed8dd488c82101db47255be49e9986d8a25dac6fb4d2adeafe007e89efb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.7.17-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:24745c70055c5b34ce94a9f10ff0e038724bc65bc1299bdf1853086c5c99d150
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.2 MB (23245411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6757fd40e7a2442b1e9015bf7f4537bd61e551143b98599d0659018801dfcdb6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 07 Aug 2023 19:20:26 GMT
ADD file:6dd87346b8be240b21b4f4d9296253bf0d28b6579aa52d2118872e3936963b6b in / 
# Mon, 07 Aug 2023 19:20:26 GMT
CMD ["/bin/sh"]
# Tue, 17 Oct 2023 01:29:21 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 21 Oct 2023 00:12:27 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Sat, 21 Oct 2023 00:12:27 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Sat, 21 Oct 2023 00:12:33 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Sat, 21 Oct 2023 00:12:33 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Sat, 21 Oct 2023 00:12:33 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sat, 21 Oct 2023 00:12:33 GMT
EXPOSE 8888
# Sat, 21 Oct 2023 00:12:33 GMT
VOLUME [/var/lib/chronograf]
# Sat, 21 Oct 2023 00:12:33 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Sat, 21 Oct 2023 00:12:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 21 Oct 2023 00:12:33 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:9398808236ffac29e60c04ec906d8d409af7fa19dc57d8c65ad167e9c4967006`  
		Last Modified: Mon, 07 Aug 2023 19:21:08 GMT  
		Size: 3.4 MB (3378609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b161763ec9e11116a97547438c5541153248aba5eddc76475885813812367da`  
		Last Modified: Tue, 17 Oct 2023 01:31:50 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c036769ce42fe6069bea0e08abbf145ff40fb3519e68ec986c7aaf6b109ac7d5`  
		Last Modified: Sat, 21 Oct 2023 00:13:30 GMT  
		Size: 284.9 KB (284931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02062f55c3474493b57edcf76d3dfb180f6979574218338b17c7055e0dacdfb1`  
		Last Modified: Sat, 21 Oct 2023 00:13:33 GMT  
		Size: 19.6 MB (19557198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da33d48693c709e5812be997c1f8d1585b2038d8a3e9f07deae21538282754db`  
		Last Modified: Sat, 21 Oct 2023 00:13:30 GMT  
		Size: 12.3 KB (12262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caed337108b2c3a0c9bf35f3a66f7ed7a429550b4fbdd33ab5d231be9c2c89d9`  
		Last Modified: Sat, 21 Oct 2023 00:13:30 GMT  
		Size: 11.9 KB (11896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92a3663990537a0cc88299aff9b2651df091f1bbd4ee851fcf3787e25cacc8a0`  
		Last Modified: Sat, 21 Oct 2023 00:13:30 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.8`

```console
$ docker pull chronograf@sha256:41d50a4cdeadcd05d78e50395db31d923bfc5e9f23ecd0188e39ea18b800209e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.8` - linux; amd64

```console
$ docker pull chronograf@sha256:8eea330a0e24de366e6597bdfdfc882fe039e0cf7947311af365c8b86e9b5536
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.3 MB (71250891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc58cd3253d4386c3c51f7215680ff286791b8992f0276eefe5b5e25830cc050`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:58 GMT
ADD file:e9f63d1defc55282fec6525ac2886c735dc2189e34105d7fe64c2420d6673922 in / 
# Tue, 21 Nov 2023 05:21:58 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 10:45:57 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 21 Nov 2023 10:45:57 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Tue, 21 Nov 2023 10:46:03 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 21 Nov 2023 10:46:03 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 21 Nov 2023 10:46:04 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 21 Nov 2023 10:46:04 GMT
EXPOSE 8888
# Tue, 21 Nov 2023 10:46:04 GMT
VOLUME [/var/lib/chronograf]
# Tue, 21 Nov 2023 10:46:04 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 21 Nov 2023 10:46:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Nov 2023 10:46:04 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:b7f91549542cca4b35a34cdee5364339f17468971ea730bb072864d3e78c8b94`  
		Last Modified: Tue, 21 Nov 2023 05:26:39 GMT  
		Size: 31.4 MB (31417824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:009053c97edf11d899a1fd1a5570d1b24a7484482bfd36c78d98cb45d084be95`  
		Last Modified: Tue, 21 Nov 2023 10:47:11 GMT  
		Size: 5.2 MB (5228517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:182a2dc862586ae6873ff1e30eae7b7c98a107c44481f0f243d8e04957b3ae8d`  
		Last Modified: Tue, 21 Nov 2023 10:47:14 GMT  
		Size: 34.6 MB (34580155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64e01a98375ae02bbde81e146184dd9f6bb71c6b67f0863e905e391d3a4857c9`  
		Last Modified: Tue, 21 Nov 2023 10:47:10 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4fd77fa4e6336a410b7cd177ad863ad695af98247596ed06418c32fce282fe2`  
		Last Modified: Tue, 21 Nov 2023 10:47:10 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:848989afbf98c2a6f8fc2fbf8d4e6f23c0647755613c67da3c66e2cff42e1de4`  
		Last Modified: Tue, 21 Nov 2023 10:47:10 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.8` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:d89749ebf70ec6602a554deddcce9ab3532c9fb0952ea52904f9704a6e637a9b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.8 MB (63848452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ffa63e674a76b7d299073b09424baf058bb5ef3da0a605be8e3375768df8dd0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 21 Nov 2023 03:58:04 GMT
ADD file:c4afced274aaa80ab3018b368ed739c1c55e49b41e9637ac44d63e61344fe865 in / 
# Tue, 21 Nov 2023 03:58:04 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:01:24 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 21 Nov 2023 07:01:24 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Tue, 21 Nov 2023 07:01:33 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 21 Nov 2023 07:01:33 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 21 Nov 2023 07:01:33 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 21 Nov 2023 07:01:33 GMT
EXPOSE 8888
# Tue, 21 Nov 2023 07:01:34 GMT
VOLUME [/var/lib/chronograf]
# Tue, 21 Nov 2023 07:01:34 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 21 Nov 2023 07:01:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Nov 2023 07:01:34 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:6dc4ed5513793308b8e30b08e03f97fa54025c3d3f3172c6edccb1dbbc7ff139`  
		Last Modified: Tue, 21 Nov 2023 04:02:35 GMT  
		Size: 26.6 MB (26579014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edd55ea3fc584681fd2d6e40a3d4fb79b999745cd2cbe43ff01d200bd086a92b`  
		Last Modified: Tue, 21 Nov 2023 07:02:36 GMT  
		Size: 4.5 MB (4493545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b99d59d19081c2f945fb72760938a3db1cbaca6c9bda15474e7cbfd632b96ce`  
		Last Modified: Tue, 21 Nov 2023 07:02:40 GMT  
		Size: 32.8 MB (32751501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3b069d5d7ab647affacb48a2f6cd287993ad72143c393726984dbbafd3cf1c9`  
		Last Modified: Tue, 21 Nov 2023 07:02:36 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd51ba0f5c4845fcfc2de6aea09acad907fa226512a87dcb4f85a64d10be868e`  
		Last Modified: Tue, 21 Nov 2023 07:02:36 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11d517962e34e98fc1b21c98c500fe626aa3fc4a6d33703698eee8d92b5ebc3b`  
		Last Modified: Tue, 21 Nov 2023 07:02:35 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.8` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:2863b5ad97d34f5948205e7ec49eac585bef6970f654c56f03bb73a70eaf5adb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.9 MB (67945045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55b60da69bf60e1e55f8d4770113c73283bd163126cbe9c74892268e94c69f5d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:20 GMT
ADD file:7b5bbc3b85f671aaf7b38dbe3fc76aae162bbff29c525bcd127f8a26a53bc664 in / 
# Tue, 21 Nov 2023 06:27:21 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:55:39 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 21 Nov 2023 07:55:39 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Tue, 21 Nov 2023 07:55:44 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 21 Nov 2023 07:55:45 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 21 Nov 2023 07:55:45 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 21 Nov 2023 07:55:45 GMT
EXPOSE 8888
# Tue, 21 Nov 2023 07:55:45 GMT
VOLUME [/var/lib/chronograf]
# Tue, 21 Nov 2023 07:55:45 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 21 Nov 2023 07:55:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Nov 2023 07:55:45 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:ca426296fe928600d0b4b844aee43e2b70a05c6f4032de5f65dcc49f5cedfd82`  
		Last Modified: Tue, 21 Nov 2023 06:31:08 GMT  
		Size: 30.1 MB (30064123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb209c8b069362f70ffdcabcf039b137a94d4a1c726e84e7ef4daa1a40c46d7d`  
		Last Modified: Tue, 21 Nov 2023 07:56:35 GMT  
		Size: 5.2 MB (5210800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e151ba5193c55174eade5e99b527a017ce8d2357b471e01fa6996f4248be7b62`  
		Last Modified: Tue, 21 Nov 2023 07:56:37 GMT  
		Size: 32.6 MB (32645725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2ca33233b634341312ae87c170ab4122c2844984ac04c6aacf50e75e06deae1`  
		Last Modified: Tue, 21 Nov 2023 07:56:34 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5951cd15be002a1a8195104e1069d3899dc728f8434e2ef90f9192bb8f534504`  
		Last Modified: Tue, 21 Nov 2023 07:56:34 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5418d13c7793b3c727d966af2eeaa22fcdcabf0cc520d312fd85fec9ea63fbee`  
		Last Modified: Tue, 21 Nov 2023 07:56:34 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.8-alpine`

```console
$ docker pull chronograf@sha256:cc10fd7518969a4605d1889b1de5a95cd8979e9467f67096c73cf99fde781ca0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.8-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:1b6c05b6263c8b9cf0a11223b81084da036abaa979eef2364c5ea859b3e90285
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.9 MB (22892405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa8a9ef98bfb0bd734bcf02bc17a58a7b15f43352e7541211ffc4a0a86254a1a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 07 Aug 2023 19:20:26 GMT
ADD file:6dd87346b8be240b21b4f4d9296253bf0d28b6579aa52d2118872e3936963b6b in / 
# Mon, 07 Aug 2023 19:20:26 GMT
CMD ["/bin/sh"]
# Tue, 17 Oct 2023 01:29:21 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 21 Oct 2023 00:12:27 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Sat, 21 Oct 2023 00:12:39 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Sat, 21 Oct 2023 00:12:44 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Sat, 21 Oct 2023 00:12:45 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Sat, 21 Oct 2023 00:12:45 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sat, 21 Oct 2023 00:12:45 GMT
EXPOSE 8888
# Sat, 21 Oct 2023 00:12:45 GMT
VOLUME [/var/lib/chronograf]
# Sat, 21 Oct 2023 00:12:45 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Sat, 21 Oct 2023 00:12:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 21 Oct 2023 00:12:45 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:9398808236ffac29e60c04ec906d8d409af7fa19dc57d8c65ad167e9c4967006`  
		Last Modified: Mon, 07 Aug 2023 19:21:08 GMT  
		Size: 3.4 MB (3378609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b161763ec9e11116a97547438c5541153248aba5eddc76475885813812367da`  
		Last Modified: Tue, 17 Oct 2023 01:31:50 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c036769ce42fe6069bea0e08abbf145ff40fb3519e68ec986c7aaf6b109ac7d5`  
		Last Modified: Sat, 21 Oct 2023 00:13:30 GMT  
		Size: 284.9 KB (284931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed0b1c874c38ce8395e2b0ad4419e183732836ff93c95dbaae6750e12adf83a3`  
		Last Modified: Sat, 21 Oct 2023 00:13:46 GMT  
		Size: 19.2 MB (19204176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6504027c845086daa6704d917065b1cdabec3a571eecd15c0261123fa5430d5c`  
		Last Modified: Sat, 21 Oct 2023 00:13:43 GMT  
		Size: 12.3 KB (12268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f52fd4eb9c1c6195d51e33d2f607a12bcabe5fc16704357cdb9a04c414f18d2`  
		Last Modified: Sat, 21 Oct 2023 00:13:43 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69feeb04bb774c2c87951159d9654b586336851212e9b75a41e4256e1aabb306`  
		Last Modified: Sat, 21 Oct 2023 00:13:43 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.8.10`

```console
$ docker pull chronograf@sha256:41d50a4cdeadcd05d78e50395db31d923bfc5e9f23ecd0188e39ea18b800209e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.8.10` - linux; amd64

```console
$ docker pull chronograf@sha256:8eea330a0e24de366e6597bdfdfc882fe039e0cf7947311af365c8b86e9b5536
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.3 MB (71250891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc58cd3253d4386c3c51f7215680ff286791b8992f0276eefe5b5e25830cc050`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:58 GMT
ADD file:e9f63d1defc55282fec6525ac2886c735dc2189e34105d7fe64c2420d6673922 in / 
# Tue, 21 Nov 2023 05:21:58 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 10:45:57 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 21 Nov 2023 10:45:57 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Tue, 21 Nov 2023 10:46:03 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 21 Nov 2023 10:46:03 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 21 Nov 2023 10:46:04 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 21 Nov 2023 10:46:04 GMT
EXPOSE 8888
# Tue, 21 Nov 2023 10:46:04 GMT
VOLUME [/var/lib/chronograf]
# Tue, 21 Nov 2023 10:46:04 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 21 Nov 2023 10:46:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Nov 2023 10:46:04 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:b7f91549542cca4b35a34cdee5364339f17468971ea730bb072864d3e78c8b94`  
		Last Modified: Tue, 21 Nov 2023 05:26:39 GMT  
		Size: 31.4 MB (31417824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:009053c97edf11d899a1fd1a5570d1b24a7484482bfd36c78d98cb45d084be95`  
		Last Modified: Tue, 21 Nov 2023 10:47:11 GMT  
		Size: 5.2 MB (5228517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:182a2dc862586ae6873ff1e30eae7b7c98a107c44481f0f243d8e04957b3ae8d`  
		Last Modified: Tue, 21 Nov 2023 10:47:14 GMT  
		Size: 34.6 MB (34580155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64e01a98375ae02bbde81e146184dd9f6bb71c6b67f0863e905e391d3a4857c9`  
		Last Modified: Tue, 21 Nov 2023 10:47:10 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4fd77fa4e6336a410b7cd177ad863ad695af98247596ed06418c32fce282fe2`  
		Last Modified: Tue, 21 Nov 2023 10:47:10 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:848989afbf98c2a6f8fc2fbf8d4e6f23c0647755613c67da3c66e2cff42e1de4`  
		Last Modified: Tue, 21 Nov 2023 10:47:10 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.8.10` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:d89749ebf70ec6602a554deddcce9ab3532c9fb0952ea52904f9704a6e637a9b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.8 MB (63848452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ffa63e674a76b7d299073b09424baf058bb5ef3da0a605be8e3375768df8dd0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 21 Nov 2023 03:58:04 GMT
ADD file:c4afced274aaa80ab3018b368ed739c1c55e49b41e9637ac44d63e61344fe865 in / 
# Tue, 21 Nov 2023 03:58:04 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:01:24 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 21 Nov 2023 07:01:24 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Tue, 21 Nov 2023 07:01:33 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 21 Nov 2023 07:01:33 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 21 Nov 2023 07:01:33 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 21 Nov 2023 07:01:33 GMT
EXPOSE 8888
# Tue, 21 Nov 2023 07:01:34 GMT
VOLUME [/var/lib/chronograf]
# Tue, 21 Nov 2023 07:01:34 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 21 Nov 2023 07:01:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Nov 2023 07:01:34 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:6dc4ed5513793308b8e30b08e03f97fa54025c3d3f3172c6edccb1dbbc7ff139`  
		Last Modified: Tue, 21 Nov 2023 04:02:35 GMT  
		Size: 26.6 MB (26579014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edd55ea3fc584681fd2d6e40a3d4fb79b999745cd2cbe43ff01d200bd086a92b`  
		Last Modified: Tue, 21 Nov 2023 07:02:36 GMT  
		Size: 4.5 MB (4493545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b99d59d19081c2f945fb72760938a3db1cbaca6c9bda15474e7cbfd632b96ce`  
		Last Modified: Tue, 21 Nov 2023 07:02:40 GMT  
		Size: 32.8 MB (32751501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3b069d5d7ab647affacb48a2f6cd287993ad72143c393726984dbbafd3cf1c9`  
		Last Modified: Tue, 21 Nov 2023 07:02:36 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd51ba0f5c4845fcfc2de6aea09acad907fa226512a87dcb4f85a64d10be868e`  
		Last Modified: Tue, 21 Nov 2023 07:02:36 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11d517962e34e98fc1b21c98c500fe626aa3fc4a6d33703698eee8d92b5ebc3b`  
		Last Modified: Tue, 21 Nov 2023 07:02:35 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.8.10` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:2863b5ad97d34f5948205e7ec49eac585bef6970f654c56f03bb73a70eaf5adb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.9 MB (67945045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55b60da69bf60e1e55f8d4770113c73283bd163126cbe9c74892268e94c69f5d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:20 GMT
ADD file:7b5bbc3b85f671aaf7b38dbe3fc76aae162bbff29c525bcd127f8a26a53bc664 in / 
# Tue, 21 Nov 2023 06:27:21 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:55:39 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 21 Nov 2023 07:55:39 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Tue, 21 Nov 2023 07:55:44 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 21 Nov 2023 07:55:45 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 21 Nov 2023 07:55:45 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 21 Nov 2023 07:55:45 GMT
EXPOSE 8888
# Tue, 21 Nov 2023 07:55:45 GMT
VOLUME [/var/lib/chronograf]
# Tue, 21 Nov 2023 07:55:45 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 21 Nov 2023 07:55:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Nov 2023 07:55:45 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:ca426296fe928600d0b4b844aee43e2b70a05c6f4032de5f65dcc49f5cedfd82`  
		Last Modified: Tue, 21 Nov 2023 06:31:08 GMT  
		Size: 30.1 MB (30064123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb209c8b069362f70ffdcabcf039b137a94d4a1c726e84e7ef4daa1a40c46d7d`  
		Last Modified: Tue, 21 Nov 2023 07:56:35 GMT  
		Size: 5.2 MB (5210800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e151ba5193c55174eade5e99b527a017ce8d2357b471e01fa6996f4248be7b62`  
		Last Modified: Tue, 21 Nov 2023 07:56:37 GMT  
		Size: 32.6 MB (32645725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2ca33233b634341312ae87c170ab4122c2844984ac04c6aacf50e75e06deae1`  
		Last Modified: Tue, 21 Nov 2023 07:56:34 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5951cd15be002a1a8195104e1069d3899dc728f8434e2ef90f9192bb8f534504`  
		Last Modified: Tue, 21 Nov 2023 07:56:34 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5418d13c7793b3c727d966af2eeaa22fcdcabf0cc520d312fd85fec9ea63fbee`  
		Last Modified: Tue, 21 Nov 2023 07:56:34 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.8.10-alpine`

```console
$ docker pull chronograf@sha256:cc10fd7518969a4605d1889b1de5a95cd8979e9467f67096c73cf99fde781ca0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.8.10-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:1b6c05b6263c8b9cf0a11223b81084da036abaa979eef2364c5ea859b3e90285
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.9 MB (22892405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa8a9ef98bfb0bd734bcf02bc17a58a7b15f43352e7541211ffc4a0a86254a1a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 07 Aug 2023 19:20:26 GMT
ADD file:6dd87346b8be240b21b4f4d9296253bf0d28b6579aa52d2118872e3936963b6b in / 
# Mon, 07 Aug 2023 19:20:26 GMT
CMD ["/bin/sh"]
# Tue, 17 Oct 2023 01:29:21 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 21 Oct 2023 00:12:27 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Sat, 21 Oct 2023 00:12:39 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Sat, 21 Oct 2023 00:12:44 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Sat, 21 Oct 2023 00:12:45 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Sat, 21 Oct 2023 00:12:45 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sat, 21 Oct 2023 00:12:45 GMT
EXPOSE 8888
# Sat, 21 Oct 2023 00:12:45 GMT
VOLUME [/var/lib/chronograf]
# Sat, 21 Oct 2023 00:12:45 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Sat, 21 Oct 2023 00:12:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 21 Oct 2023 00:12:45 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:9398808236ffac29e60c04ec906d8d409af7fa19dc57d8c65ad167e9c4967006`  
		Last Modified: Mon, 07 Aug 2023 19:21:08 GMT  
		Size: 3.4 MB (3378609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b161763ec9e11116a97547438c5541153248aba5eddc76475885813812367da`  
		Last Modified: Tue, 17 Oct 2023 01:31:50 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c036769ce42fe6069bea0e08abbf145ff40fb3519e68ec986c7aaf6b109ac7d5`  
		Last Modified: Sat, 21 Oct 2023 00:13:30 GMT  
		Size: 284.9 KB (284931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed0b1c874c38ce8395e2b0ad4419e183732836ff93c95dbaae6750e12adf83a3`  
		Last Modified: Sat, 21 Oct 2023 00:13:46 GMT  
		Size: 19.2 MB (19204176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6504027c845086daa6704d917065b1cdabec3a571eecd15c0261123fa5430d5c`  
		Last Modified: Sat, 21 Oct 2023 00:13:43 GMT  
		Size: 12.3 KB (12268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f52fd4eb9c1c6195d51e33d2f607a12bcabe5fc16704357cdb9a04c414f18d2`  
		Last Modified: Sat, 21 Oct 2023 00:13:43 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69feeb04bb774c2c87951159d9654b586336851212e9b75a41e4256e1aabb306`  
		Last Modified: Sat, 21 Oct 2023 00:13:43 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.9`

```console
$ docker pull chronograf@sha256:12da73f4b7987d368474a9f4fe5e348e8bffe8b552d8826a7d7829120386f713
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.9` - linux; amd64

```console
$ docker pull chronograf@sha256:b3154023b75510ec61040c3bbb81133dbe8c78f86d1bf3f930309073cfd8bc0a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.9 MB (71898501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09c78af96a5038b55944a6d4c5bd44d4f640695e9e9e58cc65ea625d58000480`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:58 GMT
ADD file:e9f63d1defc55282fec6525ac2886c735dc2189e34105d7fe64c2420d6673922 in / 
# Tue, 21 Nov 2023 05:21:58 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 10:45:57 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 21 Nov 2023 10:46:09 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Tue, 21 Nov 2023 10:46:15 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 21 Nov 2023 10:46:15 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 21 Nov 2023 10:46:15 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 21 Nov 2023 10:46:15 GMT
EXPOSE 8888
# Tue, 21 Nov 2023 10:46:16 GMT
VOLUME [/var/lib/chronograf]
# Tue, 21 Nov 2023 10:46:16 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 21 Nov 2023 10:46:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Nov 2023 10:46:16 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:b7f91549542cca4b35a34cdee5364339f17468971ea730bb072864d3e78c8b94`  
		Last Modified: Tue, 21 Nov 2023 05:26:39 GMT  
		Size: 31.4 MB (31417824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:009053c97edf11d899a1fd1a5570d1b24a7484482bfd36c78d98cb45d084be95`  
		Last Modified: Tue, 21 Nov 2023 10:47:11 GMT  
		Size: 5.2 MB (5228517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f88fa50077db1b9dff514c32bf83acc38ea3f5dc389dac0534f43bd21abb5f2`  
		Last Modified: Tue, 21 Nov 2023 10:47:28 GMT  
		Size: 35.2 MB (35227776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9863f165b9bb8f8181d194574e2fb38dba3142004bac2969f929697d43973314`  
		Last Modified: Tue, 21 Nov 2023 10:47:23 GMT  
		Size: 12.2 KB (12240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b16aa96cae5edab6d94517fb78bc3b76d5af6f350831c218a0cc34fad67dd46`  
		Last Modified: Tue, 21 Nov 2023 10:47:23 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7596d749c82523af104114d5151add04536750992b4e3798bac6a266c39b8a2a`  
		Last Modified: Tue, 21 Nov 2023 10:47:23 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.9` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:cf66f216a5099a113e1872e62baa43cda31c368d2da1bdcee9aab4b71d6ce1ef
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.6 MB (64624657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e494c006f9ee864eb6d465e01464919b63cd1d39ee84d52fe877d4441034fe6b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 21 Nov 2023 03:58:04 GMT
ADD file:c4afced274aaa80ab3018b368ed739c1c55e49b41e9637ac44d63e61344fe865 in / 
# Tue, 21 Nov 2023 03:58:04 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:01:24 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 21 Nov 2023 07:01:37 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Tue, 21 Nov 2023 07:01:46 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 21 Nov 2023 07:01:46 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 21 Nov 2023 07:01:46 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 21 Nov 2023 07:01:46 GMT
EXPOSE 8888
# Tue, 21 Nov 2023 07:01:46 GMT
VOLUME [/var/lib/chronograf]
# Tue, 21 Nov 2023 07:01:46 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 21 Nov 2023 07:01:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Nov 2023 07:01:47 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:6dc4ed5513793308b8e30b08e03f97fa54025c3d3f3172c6edccb1dbbc7ff139`  
		Last Modified: Tue, 21 Nov 2023 04:02:35 GMT  
		Size: 26.6 MB (26579014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edd55ea3fc584681fd2d6e40a3d4fb79b999745cd2cbe43ff01d200bd086a92b`  
		Last Modified: Tue, 21 Nov 2023 07:02:36 GMT  
		Size: 4.5 MB (4493545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fc60641a1f2f9eeff47e5f3c6a278a99671b3e037057b19a77c669768d90e03`  
		Last Modified: Tue, 21 Nov 2023 07:02:53 GMT  
		Size: 33.5 MB (33527706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c57ba979c4dfdabbfc848e43722524162f73173ad7d2d38676e2769e7b3d143e`  
		Last Modified: Tue, 21 Nov 2023 07:02:48 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:879313a547c3352fcdab8316e77f24b180520731f22433f8fadb4d8b76a0c23f`  
		Last Modified: Tue, 21 Nov 2023 07:02:48 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fda4f34a967615b13a273fbca1d0cdd63fa60aec46c663ae351dbb63adbab8dc`  
		Last Modified: Tue, 21 Nov 2023 07:02:48 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.9` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:433378bb626a20dcdca7add7ace63ff38788c958fc5820698c2350a154e4f4ea
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.7 MB (68697452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f52dec4de5d0d065b15623748cf8eb3533501a2d41fb38caa59693ae855c5b2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:20 GMT
ADD file:7b5bbc3b85f671aaf7b38dbe3fc76aae162bbff29c525bcd127f8a26a53bc664 in / 
# Tue, 21 Nov 2023 06:27:21 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:55:39 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 21 Nov 2023 07:55:49 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Tue, 21 Nov 2023 07:55:54 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 21 Nov 2023 07:55:55 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 21 Nov 2023 07:55:55 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 21 Nov 2023 07:55:55 GMT
EXPOSE 8888
# Tue, 21 Nov 2023 07:55:55 GMT
VOLUME [/var/lib/chronograf]
# Tue, 21 Nov 2023 07:55:55 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 21 Nov 2023 07:55:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Nov 2023 07:55:55 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:ca426296fe928600d0b4b844aee43e2b70a05c6f4032de5f65dcc49f5cedfd82`  
		Last Modified: Tue, 21 Nov 2023 06:31:08 GMT  
		Size: 30.1 MB (30064123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb209c8b069362f70ffdcabcf039b137a94d4a1c726e84e7ef4daa1a40c46d7d`  
		Last Modified: Tue, 21 Nov 2023 07:56:35 GMT  
		Size: 5.2 MB (5210800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91cbd337036365d2a0df031c05627d333371e2de2d5e9c7abc0cc8672f3d81e9`  
		Last Modified: Tue, 21 Nov 2023 07:56:50 GMT  
		Size: 33.4 MB (33398134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94f15b89cd46b7518fb7adb8befae559ce75f3bf4515537320f03b14891d9285`  
		Last Modified: Tue, 21 Nov 2023 07:56:47 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1937ac15ba34dc4bcfcaabbcfd118c0323343328807f41b7b7dfabafa86308e8`  
		Last Modified: Tue, 21 Nov 2023 07:56:47 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22844c16747e8838a3fe28e02d67e1a719d66e4a2b3a7698b70430ff255648ef`  
		Last Modified: Tue, 21 Nov 2023 07:56:47 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.9-alpine`

```console
$ docker pull chronograf@sha256:81fd6739ec0866d54aeb57fe7f230d9fd67d1847994eb336380a5363e2c5b006
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.9-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:9c596fdc931db5549ac6d4144cbda1d6d82d666444dcce5eab5f478c02170372
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.4 MB (23360449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d248f08cbf5085807b61e50c39cc60fddb02fa315bea8cc96309bcb543b1a3a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 07 Aug 2023 19:20:26 GMT
ADD file:6dd87346b8be240b21b4f4d9296253bf0d28b6579aa52d2118872e3936963b6b in / 
# Mon, 07 Aug 2023 19:20:26 GMT
CMD ["/bin/sh"]
# Tue, 17 Oct 2023 01:29:21 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 21 Oct 2023 00:12:27 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Sat, 21 Oct 2023 00:12:51 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Sat, 21 Oct 2023 00:12:56 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Sat, 21 Oct 2023 00:12:57 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Sat, 21 Oct 2023 00:12:57 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sat, 21 Oct 2023 00:12:57 GMT
EXPOSE 8888
# Sat, 21 Oct 2023 00:12:57 GMT
VOLUME [/var/lib/chronograf]
# Sat, 21 Oct 2023 00:12:57 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Sat, 21 Oct 2023 00:12:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 21 Oct 2023 00:12:57 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:9398808236ffac29e60c04ec906d8d409af7fa19dc57d8c65ad167e9c4967006`  
		Last Modified: Mon, 07 Aug 2023 19:21:08 GMT  
		Size: 3.4 MB (3378609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b161763ec9e11116a97547438c5541153248aba5eddc76475885813812367da`  
		Last Modified: Tue, 17 Oct 2023 01:31:50 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c036769ce42fe6069bea0e08abbf145ff40fb3519e68ec986c7aaf6b109ac7d5`  
		Last Modified: Sat, 21 Oct 2023 00:13:30 GMT  
		Size: 284.9 KB (284931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01e6e2e7b6d89418bd1dbd9a733b2da1c5474358f22390f540a25006f543b033`  
		Last Modified: Sat, 21 Oct 2023 00:13:58 GMT  
		Size: 19.7 MB (19672231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9564077ee006017e729c2c63139fef09a7515d5147bfb50e5c726bdd6f34501`  
		Last Modified: Sat, 21 Oct 2023 00:13:55 GMT  
		Size: 12.3 KB (12265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e02ba258151fc19eb314b23a6d3a4d9fac29b7641e2ca5a7086b562eb82c1d1`  
		Last Modified: Sat, 21 Oct 2023 00:13:55 GMT  
		Size: 11.9 KB (11898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa94676f65ae15a93443979dc006bc3e8ffc5343e1201c834b3ef6f42d8f7427`  
		Last Modified: Sat, 21 Oct 2023 00:13:55 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.9.4`

```console
$ docker pull chronograf@sha256:12da73f4b7987d368474a9f4fe5e348e8bffe8b552d8826a7d7829120386f713
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.9.4` - linux; amd64

```console
$ docker pull chronograf@sha256:b3154023b75510ec61040c3bbb81133dbe8c78f86d1bf3f930309073cfd8bc0a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.9 MB (71898501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09c78af96a5038b55944a6d4c5bd44d4f640695e9e9e58cc65ea625d58000480`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:58 GMT
ADD file:e9f63d1defc55282fec6525ac2886c735dc2189e34105d7fe64c2420d6673922 in / 
# Tue, 21 Nov 2023 05:21:58 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 10:45:57 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 21 Nov 2023 10:46:09 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Tue, 21 Nov 2023 10:46:15 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 21 Nov 2023 10:46:15 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 21 Nov 2023 10:46:15 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 21 Nov 2023 10:46:15 GMT
EXPOSE 8888
# Tue, 21 Nov 2023 10:46:16 GMT
VOLUME [/var/lib/chronograf]
# Tue, 21 Nov 2023 10:46:16 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 21 Nov 2023 10:46:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Nov 2023 10:46:16 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:b7f91549542cca4b35a34cdee5364339f17468971ea730bb072864d3e78c8b94`  
		Last Modified: Tue, 21 Nov 2023 05:26:39 GMT  
		Size: 31.4 MB (31417824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:009053c97edf11d899a1fd1a5570d1b24a7484482bfd36c78d98cb45d084be95`  
		Last Modified: Tue, 21 Nov 2023 10:47:11 GMT  
		Size: 5.2 MB (5228517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f88fa50077db1b9dff514c32bf83acc38ea3f5dc389dac0534f43bd21abb5f2`  
		Last Modified: Tue, 21 Nov 2023 10:47:28 GMT  
		Size: 35.2 MB (35227776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9863f165b9bb8f8181d194574e2fb38dba3142004bac2969f929697d43973314`  
		Last Modified: Tue, 21 Nov 2023 10:47:23 GMT  
		Size: 12.2 KB (12240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b16aa96cae5edab6d94517fb78bc3b76d5af6f350831c218a0cc34fad67dd46`  
		Last Modified: Tue, 21 Nov 2023 10:47:23 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7596d749c82523af104114d5151add04536750992b4e3798bac6a266c39b8a2a`  
		Last Modified: Tue, 21 Nov 2023 10:47:23 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.9.4` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:cf66f216a5099a113e1872e62baa43cda31c368d2da1bdcee9aab4b71d6ce1ef
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.6 MB (64624657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e494c006f9ee864eb6d465e01464919b63cd1d39ee84d52fe877d4441034fe6b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 21 Nov 2023 03:58:04 GMT
ADD file:c4afced274aaa80ab3018b368ed739c1c55e49b41e9637ac44d63e61344fe865 in / 
# Tue, 21 Nov 2023 03:58:04 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:01:24 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 21 Nov 2023 07:01:37 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Tue, 21 Nov 2023 07:01:46 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 21 Nov 2023 07:01:46 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 21 Nov 2023 07:01:46 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 21 Nov 2023 07:01:46 GMT
EXPOSE 8888
# Tue, 21 Nov 2023 07:01:46 GMT
VOLUME [/var/lib/chronograf]
# Tue, 21 Nov 2023 07:01:46 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 21 Nov 2023 07:01:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Nov 2023 07:01:47 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:6dc4ed5513793308b8e30b08e03f97fa54025c3d3f3172c6edccb1dbbc7ff139`  
		Last Modified: Tue, 21 Nov 2023 04:02:35 GMT  
		Size: 26.6 MB (26579014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edd55ea3fc584681fd2d6e40a3d4fb79b999745cd2cbe43ff01d200bd086a92b`  
		Last Modified: Tue, 21 Nov 2023 07:02:36 GMT  
		Size: 4.5 MB (4493545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fc60641a1f2f9eeff47e5f3c6a278a99671b3e037057b19a77c669768d90e03`  
		Last Modified: Tue, 21 Nov 2023 07:02:53 GMT  
		Size: 33.5 MB (33527706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c57ba979c4dfdabbfc848e43722524162f73173ad7d2d38676e2769e7b3d143e`  
		Last Modified: Tue, 21 Nov 2023 07:02:48 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:879313a547c3352fcdab8316e77f24b180520731f22433f8fadb4d8b76a0c23f`  
		Last Modified: Tue, 21 Nov 2023 07:02:48 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fda4f34a967615b13a273fbca1d0cdd63fa60aec46c663ae351dbb63adbab8dc`  
		Last Modified: Tue, 21 Nov 2023 07:02:48 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.9.4` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:433378bb626a20dcdca7add7ace63ff38788c958fc5820698c2350a154e4f4ea
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.7 MB (68697452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f52dec4de5d0d065b15623748cf8eb3533501a2d41fb38caa59693ae855c5b2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:20 GMT
ADD file:7b5bbc3b85f671aaf7b38dbe3fc76aae162bbff29c525bcd127f8a26a53bc664 in / 
# Tue, 21 Nov 2023 06:27:21 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:55:39 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 21 Nov 2023 07:55:49 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Tue, 21 Nov 2023 07:55:54 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 21 Nov 2023 07:55:55 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 21 Nov 2023 07:55:55 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 21 Nov 2023 07:55:55 GMT
EXPOSE 8888
# Tue, 21 Nov 2023 07:55:55 GMT
VOLUME [/var/lib/chronograf]
# Tue, 21 Nov 2023 07:55:55 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 21 Nov 2023 07:55:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Nov 2023 07:55:55 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:ca426296fe928600d0b4b844aee43e2b70a05c6f4032de5f65dcc49f5cedfd82`  
		Last Modified: Tue, 21 Nov 2023 06:31:08 GMT  
		Size: 30.1 MB (30064123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb209c8b069362f70ffdcabcf039b137a94d4a1c726e84e7ef4daa1a40c46d7d`  
		Last Modified: Tue, 21 Nov 2023 07:56:35 GMT  
		Size: 5.2 MB (5210800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91cbd337036365d2a0df031c05627d333371e2de2d5e9c7abc0cc8672f3d81e9`  
		Last Modified: Tue, 21 Nov 2023 07:56:50 GMT  
		Size: 33.4 MB (33398134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94f15b89cd46b7518fb7adb8befae559ce75f3bf4515537320f03b14891d9285`  
		Last Modified: Tue, 21 Nov 2023 07:56:47 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1937ac15ba34dc4bcfcaabbcfd118c0323343328807f41b7b7dfabafa86308e8`  
		Last Modified: Tue, 21 Nov 2023 07:56:47 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22844c16747e8838a3fe28e02d67e1a719d66e4a2b3a7698b70430ff255648ef`  
		Last Modified: Tue, 21 Nov 2023 07:56:47 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.9.4-alpine`

```console
$ docker pull chronograf@sha256:81fd6739ec0866d54aeb57fe7f230d9fd67d1847994eb336380a5363e2c5b006
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.9.4-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:9c596fdc931db5549ac6d4144cbda1d6d82d666444dcce5eab5f478c02170372
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.4 MB (23360449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d248f08cbf5085807b61e50c39cc60fddb02fa315bea8cc96309bcb543b1a3a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 07 Aug 2023 19:20:26 GMT
ADD file:6dd87346b8be240b21b4f4d9296253bf0d28b6579aa52d2118872e3936963b6b in / 
# Mon, 07 Aug 2023 19:20:26 GMT
CMD ["/bin/sh"]
# Tue, 17 Oct 2023 01:29:21 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 21 Oct 2023 00:12:27 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Sat, 21 Oct 2023 00:12:51 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Sat, 21 Oct 2023 00:12:56 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Sat, 21 Oct 2023 00:12:57 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Sat, 21 Oct 2023 00:12:57 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sat, 21 Oct 2023 00:12:57 GMT
EXPOSE 8888
# Sat, 21 Oct 2023 00:12:57 GMT
VOLUME [/var/lib/chronograf]
# Sat, 21 Oct 2023 00:12:57 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Sat, 21 Oct 2023 00:12:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 21 Oct 2023 00:12:57 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:9398808236ffac29e60c04ec906d8d409af7fa19dc57d8c65ad167e9c4967006`  
		Last Modified: Mon, 07 Aug 2023 19:21:08 GMT  
		Size: 3.4 MB (3378609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b161763ec9e11116a97547438c5541153248aba5eddc76475885813812367da`  
		Last Modified: Tue, 17 Oct 2023 01:31:50 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c036769ce42fe6069bea0e08abbf145ff40fb3519e68ec986c7aaf6b109ac7d5`  
		Last Modified: Sat, 21 Oct 2023 00:13:30 GMT  
		Size: 284.9 KB (284931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01e6e2e7b6d89418bd1dbd9a733b2da1c5474358f22390f540a25006f543b033`  
		Last Modified: Sat, 21 Oct 2023 00:13:58 GMT  
		Size: 19.7 MB (19672231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9564077ee006017e729c2c63139fef09a7515d5147bfb50e5c726bdd6f34501`  
		Last Modified: Sat, 21 Oct 2023 00:13:55 GMT  
		Size: 12.3 KB (12265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e02ba258151fc19eb314b23a6d3a4d9fac29b7641e2ca5a7086b562eb82c1d1`  
		Last Modified: Sat, 21 Oct 2023 00:13:55 GMT  
		Size: 11.9 KB (11898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa94676f65ae15a93443979dc006bc3e8ffc5343e1201c834b3ef6f42d8f7427`  
		Last Modified: Sat, 21 Oct 2023 00:13:55 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:alpine`

```console
$ docker pull chronograf@sha256:7530358bc4ca04eb208da945243c805590bf122d3261f8a97fabc0d8a89bf622
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:fb43ec35ddd6e58cc2e78ef58f797cb6de9067c3932e3db1f85a4aea80fb6751
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.6 MB (31558951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b55651823a683848ddd413718b400ba4b653ea7e671921241f5a3604a2cef16d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Tue, 17 Oct 2023 01:30:37 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 21 Oct 2023 02:34:58 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Tue, 24 Oct 2023 00:20:11 GMT
ENV CHRONOGRAF_VERSION=1.10.2
# Tue, 24 Oct 2023 00:20:16 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Tue, 24 Oct 2023 00:20:16 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 24 Oct 2023 00:20:16 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 24 Oct 2023 00:20:16 GMT
EXPOSE 8888
# Tue, 24 Oct 2023 00:20:16 GMT
VOLUME [/var/lib/chronograf]
# Tue, 24 Oct 2023 00:20:16 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Tue, 24 Oct 2023 00:20:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Oct 2023 00:20:17 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f5352bf3aec614dde8ac36d38f28f5021eff4c2ff0226eb22dfa667f2b2add1`  
		Last Modified: Tue, 17 Oct 2023 01:33:20 GMT  
		Size: 281.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4048f49511dda4f4f68ff84317685f405a4090adcf74b1c9c7116e71ae80d30a`  
		Last Modified: Sat, 21 Oct 2023 02:35:44 GMT  
		Size: 284.7 KB (284698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6545ebb960dd3a534da359758d3fec7757e7866b3655ad8432156ab58b56bf56`  
		Last Modified: Tue, 24 Oct 2023 00:21:04 GMT  
		Size: 27.8 MB (27847599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c28322186901948002f5674f518fd78626ce89862f988bcfbfe22b03a9868134`  
		Last Modified: Tue, 24 Oct 2023 00:20:58 GMT  
		Size: 12.3 KB (12268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d268d1b30ec9afb6cf8ac11fe77068afa5f6b2e2211c3e2861d51f122b8b5e07`  
		Last Modified: Tue, 24 Oct 2023 00:20:59 GMT  
		Size: 11.9 KB (11900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c48929913d0bb1a8ca03b3dfcd0cfded77493e0142ff4fd446ca1f7bfbed9bd`  
		Last Modified: Tue, 24 Oct 2023 00:20:58 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:latest`

```console
$ docker pull chronograf@sha256:1afe04050c8d702be216a813a21ef7e340e16b7fc4fb5f3a778a38db3581f0fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:latest` - linux; amd64

```console
$ docker pull chronograf@sha256:380dde297f323ba57a0b07ca849a6c7582e05a7cd52577d44dce054bb502d2cf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.1 MB (84101080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1a8a073dfc63164af1a2f1bd67da6e4fbda63b5b6c1e8b8ab05060fac70496d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:37 GMT
ADD file:d261a6f6921593f1e0b3f472ab1b1822e2c6deb0b369200f0b3370556bfad017 in / 
# Tue, 21 Nov 2023 05:21:37 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 10:46:29 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 21 Nov 2023 10:46:29 GMT
ENV CHRONOGRAF_VERSION=1.10.2
# Tue, 21 Nov 2023 10:46:38 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 21 Nov 2023 10:46:38 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 21 Nov 2023 10:46:38 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 21 Nov 2023 10:46:38 GMT
EXPOSE 8888
# Tue, 21 Nov 2023 10:46:38 GMT
VOLUME [/var/lib/chronograf]
# Tue, 21 Nov 2023 10:46:38 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 21 Nov 2023 10:46:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Nov 2023 10:46:38 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:1f7ce2fa46ab3942feabee654933948821303a5a821789dddab2d8c3df59e227`  
		Last Modified: Tue, 21 Nov 2023 05:25:58 GMT  
		Size: 29.1 MB (29149908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1956287ac9cfdc19991d482f7cfe094a5236d159dca178b0e4e2888989901d13`  
		Last Modified: Tue, 21 Nov 2023 10:47:39 GMT  
		Size: 7.9 MB (7873073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fb62f985c03da59f7ba67ba98ea4eff8aac143fc92e81898567003bca5c00af`  
		Last Modified: Tue, 21 Nov 2023 10:47:43 GMT  
		Size: 47.1 MB (47053706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8b385f9ed0e852b69a364d9c189f846eb9f1df339ad58cb86610d69e86d8cb4`  
		Last Modified: Tue, 21 Nov 2023 10:47:37 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deb06199f978c7bf17a871d0668ac1245f63349368d3a416f8788268c921a171`  
		Last Modified: Tue, 21 Nov 2023 10:47:37 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c18d5e09745fe375af5895b0b1c99d8110d4704ec58d7c7df8619dc1622f8dcc`  
		Last Modified: Tue, 21 Nov 2023 10:47:37 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:latest` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:3024f41d59a015cc2c86ad2aa2e0f1abb4b882b9345c6a43f7b600bf2d8af65e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75920715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2332571a6259070e1637d40b140c79fa917f32e446565a38a7a90649f0b12b57`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 21 Nov 2023 03:57:43 GMT
ADD file:b693944382a95fa47622fde77eb98f0cdeafa40261e7334bd355e00f650b6632 in / 
# Tue, 21 Nov 2023 03:57:43 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:02:00 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 21 Nov 2023 07:02:00 GMT
ENV CHRONOGRAF_VERSION=1.10.2
# Tue, 21 Nov 2023 07:02:10 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 21 Nov 2023 07:02:10 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 21 Nov 2023 07:02:10 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 21 Nov 2023 07:02:10 GMT
EXPOSE 8888
# Tue, 21 Nov 2023 07:02:11 GMT
VOLUME [/var/lib/chronograf]
# Tue, 21 Nov 2023 07:02:11 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 21 Nov 2023 07:02:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Nov 2023 07:02:11 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:b4ce590529bbcf84326048a22fce76fcfcb5c60af5519debd7935a74c1e9126e`  
		Last Modified: Tue, 21 Nov 2023 04:01:50 GMT  
		Size: 24.7 MB (24748925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a72f2ea3c3dd4c6c84869aff33141879c89aed7d1ebdee23dd5cc143fbe8c2`  
		Last Modified: Tue, 21 Nov 2023 07:03:02 GMT  
		Size: 6.5 MB (6497812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26311c9696c337908f2631c213e79d0c72849a72085fde9380f35a1c67ed28fa`  
		Last Modified: Tue, 21 Nov 2023 07:03:08 GMT  
		Size: 44.6 MB (44649586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aac8f1e393f681f858ed71dbc056c8a255df814677dc93f57014c85a6411f5bc`  
		Last Modified: Tue, 21 Nov 2023 07:03:01 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65c8c90cbbd08d52d14449a9108f380a4fd480b83a4a28fdef9ccae09f49738f`  
		Last Modified: Tue, 21 Nov 2023 07:03:01 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1527e2aad92573d1f8276fe9286d5379b57115a489a28173509391bf2c65c2a3`  
		Last Modified: Tue, 21 Nov 2023 07:03:01 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:latest` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:907da70564d00845356dabad9cb329f113e7642486d3ec24208ea93466beb07c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.6 MB (81627266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9355053d09268aef0f21bada565fd0029a482328b07884f0e71fcc8b9834721d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:06 GMT
ADD file:869c7d0747a17c53715581a2e862992eb8516c7f45f167821dfa80966a4870d1 in / 
# Tue, 21 Nov 2023 06:27:06 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:56:05 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 21 Nov 2023 07:56:05 GMT
ENV CHRONOGRAF_VERSION=1.10.2
# Tue, 21 Nov 2023 07:56:12 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 21 Nov 2023 07:56:13 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 21 Nov 2023 07:56:13 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 21 Nov 2023 07:56:13 GMT
EXPOSE 8888
# Tue, 21 Nov 2023 07:56:13 GMT
VOLUME [/var/lib/chronograf]
# Tue, 21 Nov 2023 07:56:13 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 21 Nov 2023 07:56:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Nov 2023 07:56:13 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:2c6d21737d8318aa15c4cc838475029a5efc36c0429e3d8da80d97d0b96d9aaf`  
		Last Modified: Tue, 21 Nov 2023 06:30:30 GMT  
		Size: 29.2 MB (29179277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63f93356fcd55f6426d456c26d4a5e38da0bb544a18f1666780fa447b8eed55d`  
		Last Modified: Tue, 21 Nov 2023 07:57:00 GMT  
		Size: 7.6 MB (7649760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32eb3d345558481a7c6da4301adcd44374730662770cf8edb7b7c82f9c44ad26`  
		Last Modified: Tue, 21 Nov 2023 07:57:04 GMT  
		Size: 44.8 MB (44773832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1417ae54eecd2b37aef5ab9b854f4a8641033587d30e3ce30f765091c47afd4`  
		Last Modified: Tue, 21 Nov 2023 07:56:59 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:103dd685ae00f8ca4c49f165c1dc572de1b4e2510dcdbb20a96f9b963a831e69`  
		Last Modified: Tue, 21 Nov 2023 07:56:59 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ace178832cf7524abb72847cc73615fb748c94a3583f08add64d5938d2d0512`  
		Last Modified: Tue, 21 Nov 2023 07:56:59 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
