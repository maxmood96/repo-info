<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `chronograf`

-	[`chronograf:1.10`](#chronograf110)
-	[`chronograf:1.10-alpine`](#chronograf110-alpine)
-	[`chronograf:1.10.9`](#chronograf1109)
-	[`chronograf:1.10.9-alpine`](#chronograf1109-alpine)
-	[`chronograf:1.11`](#chronograf111)
-	[`chronograf:1.11-alpine`](#chronograf111-alpine)
-	[`chronograf:1.11.3`](#chronograf1113)
-	[`chronograf:1.11.3-alpine`](#chronograf1113-alpine)
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
$ docker pull chronograf@sha256:1e2982a21cab332a1d8ad29083c6e9799df65e497ecbc0cc4873ae3a64035d7e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `chronograf:1.10` - linux; amd64

```console
$ docker pull chronograf@sha256:8760f4d98c23b352d4d55ed05f2a2d92ce01f6f90fa8799de49e7b65617b8433
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.0 MB (85013254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:623aaab10cc07007e12c30b976d188ca4d8c4e0ea0e48994647321d8eb268651`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:42:46 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Thu, 11 Jun 2026 00:42:52 GMT
ENV CHRONOGRAF_VERSION=1.10.9
# Thu, 11 Jun 2026 00:42:52 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Thu, 11 Jun 2026 00:42:52 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Thu, 11 Jun 2026 00:42:52 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Thu, 11 Jun 2026 00:42:52 GMT
EXPOSE map[8888/tcp:{}]
# Thu, 11 Jun 2026 00:42:52 GMT
VOLUME [/var/lib/chronograf]
# Thu, 11 Jun 2026 00:42:52 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Jun 2026 00:42:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jun 2026 00:42:52 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:b9136609bef0128191aa157637b98dd7b98e52154ca60c18258d65957a01c6d0`  
		Last Modified: Wed, 10 Jun 2026 23:39:54 GMT  
		Size: 28.2 MB (28237624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:777573d12ae65c04d3140876bdc7dd031719e58dbe5e06afd0f6bc42c2a93446`  
		Last Modified: Thu, 11 Jun 2026 00:43:04 GMT  
		Size: 7.9 MB (7883331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8265ecc0dd96adcb35313ba4613cce460214db1f07a73e5e72172cd764b98b14`  
		Last Modified: Thu, 11 Jun 2026 00:43:06 GMT  
		Size: 48.9 MB (48867835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf0fa0d395cc097ddfc8f82019202e65ac2146b3d3d62599f7366baf6ba0ba28`  
		Last Modified: Thu, 11 Jun 2026 00:43:03 GMT  
		Size: 12.2 KB (12244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49f74d4683e012dac190c42635e8e1da469e82444707939395a012b8f7683984`  
		Last Modified: Thu, 11 Jun 2026 00:43:04 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75ed6d02a52d2765364e5bce636d8fdc66f7841fe6f3ecea4a7af3fd692c3822`  
		Last Modified: Thu, 11 Jun 2026 00:43:05 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:f8f562e8aedfc102c49ba86357b0fe2dfbcfae5e58e3671bc657984e4cde10ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2871238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91f10898bd9e9279e5245ee4e41146be825b58df23c9689098c49ce2c4172662`

```dockerfile
```

-	Layers:
	-	`sha256:ba7bb74c7a686129cba964213121f515ddff6a6cdf7f0bde5f4d462e229898e7`  
		Last Modified: Thu, 11 Jun 2026 00:43:04 GMT  
		Size: 2.9 MB (2855460 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:859339ed59fbee4a31097c6033f663bd90b976b1f8d123b8f675cfdd52f7e10d`  
		Last Modified: Thu, 11 Jun 2026 00:43:03 GMT  
		Size: 15.8 KB (15778 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.10` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:639c91e21b682607057aab5cfafd420d8f4472c05fc185a081319bff4fa6c24e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76803529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4666f0d926abef3a7bfeaea2a178761b4c17e46f160bec33914ebd1e3f8a2f91`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 01:30:52 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Thu, 11 Jun 2026 01:30:58 GMT
ENV CHRONOGRAF_VERSION=1.10.9
# Thu, 11 Jun 2026 01:30:58 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Thu, 11 Jun 2026 01:30:58 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Thu, 11 Jun 2026 01:30:58 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Thu, 11 Jun 2026 01:30:58 GMT
EXPOSE map[8888/tcp:{}]
# Thu, 11 Jun 2026 01:30:58 GMT
VOLUME [/var/lib/chronograf]
# Thu, 11 Jun 2026 01:30:58 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Jun 2026 01:30:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jun 2026 01:30:58 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:8ae2378435d99f39097aa4fd0d6c58c08445becca3153d53205b2cc5054b09c2`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 23.9 MB (23944473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1df41aea1f61522fb0febc178cdc134934f0cdab30cf3fd8116547c6a28ef21`  
		Last Modified: Thu, 11 Jun 2026 01:31:10 GMT  
		Size: 6.5 MB (6514534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:331d7cc0440968a01825592a1c8d60a43171834901f50e2c9a8ac4b5264e1bc9`  
		Last Modified: Thu, 11 Jun 2026 01:31:10 GMT  
		Size: 46.3 MB (46320061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:038c0fedc8f6b97547ba19c2b505783dcf0bda7cf3adaf8777c51fb292f51d92`  
		Last Modified: Thu, 11 Jun 2026 01:31:09 GMT  
		Size: 12.2 KB (12243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1ed94dee9e122944104a9020255dccb60c24e2720e3f2a4b5fea27f83f9774a`  
		Last Modified: Thu, 11 Jun 2026 01:31:09 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79eeb733bfce62026bec9dce96e10e401c7e7f58e6215b318a56a5d2611f429c`  
		Last Modified: Thu, 11 Jun 2026 01:31:10 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:e0208879ba38610ab02632ea313802f16ee1f8ca9a7ec74b45c7f060eb198314
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2873604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69883f0876ac0c1e47b4b99e3f457d761ed9a58e466c57b7b8285f9988c6abae`

```dockerfile
```

-	Layers:
	-	`sha256:ad53705953eece4ee7ac1833378cd196ef5a88915f7e7d4f7a2f3ee9c62c2732`  
		Last Modified: Thu, 11 Jun 2026 01:31:09 GMT  
		Size: 2.9 MB (2857749 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9b1a3e86baf536f21a7ad25234651c13e7a15a8b82108a1c4613774e54b3081`  
		Last Modified: Thu, 11 Jun 2026 01:31:09 GMT  
		Size: 15.9 KB (15855 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.10` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:72bf1862281573f4dcca4f4e5e9cff88f81eb7ce97c4029e89db627f083b04d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.9 MB (81855416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e73c21ceecd9ef63c5ae20524c961f624aecb406d843092b6e8f532950d50930`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:44:30 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Thu, 11 Jun 2026 00:44:36 GMT
ENV CHRONOGRAF_VERSION=1.10.9
# Thu, 11 Jun 2026 00:44:36 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Thu, 11 Jun 2026 00:44:36 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Thu, 11 Jun 2026 00:44:36 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Thu, 11 Jun 2026 00:44:36 GMT
EXPOSE map[8888/tcp:{}]
# Thu, 11 Jun 2026 00:44:36 GMT
VOLUME [/var/lib/chronograf]
# Thu, 11 Jun 2026 00:44:36 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Jun 2026 00:44:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jun 2026 00:44:36 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:402614bd39aaec1e4bdcf25aa67f88588fc8d93997a2551c4e130e6ed2b06c7a`  
		Last Modified: Wed, 10 Jun 2026 23:39:57 GMT  
		Size: 28.1 MB (28122307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:178c785dfc4e2d2645c1bc0d89fe671d8526dbbbec573f6604330067f48d5b33`  
		Last Modified: Thu, 11 Jun 2026 00:44:47 GMT  
		Size: 7.7 MB (7699782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bd903b66630bc06414d0520ccc1edd9f5b6461c98195e7b47bf0c7d17de0795`  
		Last Modified: Thu, 11 Jun 2026 00:44:48 GMT  
		Size: 46.0 MB (46008870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dc38ed08988a636521f039fed509393cd9157cc5a0ff0915ff921be433423e4`  
		Last Modified: Thu, 11 Jun 2026 00:44:46 GMT  
		Size: 12.2 KB (12242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5600d08501e1281d85bdf55615e8198a9c7c3c631f674c9eb4ee868a07477d0f`  
		Last Modified: Thu, 11 Jun 2026 00:44:46 GMT  
		Size: 11.9 KB (11901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea605ba23cf1c1bc2740f58bdd6611ff69c9aa72c7e9290df38655ccd2c84cd1`  
		Last Modified: Thu, 11 Jun 2026 00:44:47 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:950f79304babc4401b888321d6fa601af2c4d8408cd895eaa19621efce951ff5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2871595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c55ce2dd578f36a26fb90f267c9d892a5d27aa35b1f10ae87420dd537c367ae`

```dockerfile
```

-	Layers:
	-	`sha256:6dc726da581cbe1357a405d2b55c501d9c9aa548186ac9a0b1f01f758e895ff8`  
		Last Modified: Thu, 11 Jun 2026 00:44:46 GMT  
		Size: 2.9 MB (2855721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:274e20d904a3b4aa7514220ff201a73777954fc6d080ae4e7ca3a20773059822`  
		Last Modified: Thu, 11 Jun 2026 00:44:46 GMT  
		Size: 15.9 KB (15874 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.10-alpine`

```console
$ docker pull chronograf@sha256:b000618ec7e3a0bf1931ba9ed12c5b347275dff8172cdb1305dc9a9832d9cbe2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.10-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:b8e74c35e5231080b81127e0577e64d64bb246a1e1bcd5d4e650981a9673e64d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.2 MB (33214540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ca665246e4b6f85ea6db5c68c9e874fdcbcad9e207495274a3183239f9d87ee`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:21 GMT
ADD alpine-minirootfs-3.22.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:21 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:56:11 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 22 Jun 2026 19:56:11 GMT
RUN apk add --no-cache ca-certificates setpriv &&     update-ca-certificates # buildkit
# Mon, 22 Jun 2026 19:56:14 GMT
ENV CHRONOGRAF_VERSION=1.10.9
# Mon, 22 Jun 2026 19:56:14 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S chronograf &&     adduser -S chronograf -G chronograf &&     mkdir -m 0750 -p /var/lib/chronograf &&     chown chronograf:chronograf /var/lib/chronograf # buildkit
# Mon, 22 Jun 2026 19:56:14 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 22 Jun 2026 19:56:14 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 22 Jun 2026 19:56:14 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 22 Jun 2026 19:56:14 GMT
VOLUME [/var/lib/chronograf]
# Mon, 22 Jun 2026 19:56:14 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 22 Jun 2026 19:56:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Jun 2026 19:56:14 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:f7ee36c9aa34bbb665f975c76e5c0d1607f0674b94c84cfb0061f87006ea5d10`  
		Last Modified: Mon, 22 Jun 2026 09:11:44 GMT  
		Size: 3.8 MB (3787595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5117c3486ea43e29efca00448cabc535b8f239d757c2ea33ef0320285384ab97`  
		Last Modified: Mon, 22 Jun 2026 19:56:22 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73c138ad4109725f9ac144c7b23085967f20ab7006fd27272598882e140227af`  
		Last Modified: Mon, 22 Jun 2026 19:56:23 GMT  
		Size: 268.0 KB (268025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:880daa7fabb26e5620128d415d7aa48249aacd46940433d1894271ae7ef3a6b5`  
		Last Modified: Mon, 22 Jun 2026 19:56:24 GMT  
		Size: 29.1 MB (29134197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa1f3e1739343a8716664d1b82acab8681f1f3101acf6695f1cf2b791c7f83e5`  
		Last Modified: Mon, 22 Jun 2026 19:56:23 GMT  
		Size: 12.2 KB (12235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:960222739a97c24fefa7b57265a4e13a2acd84bbf3900523fd3a5ad2f9fd1cea`  
		Last Modified: Mon, 22 Jun 2026 19:56:24 GMT  
		Size: 11.9 KB (11894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eab50510b69ae15c2c3be82bc491e2c68e1139bd139081b3f29e976f73e9ae3`  
		Last Modified: Mon, 22 Jun 2026 19:56:24 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:5c9a23113a46122ee3f7481e596f13c4931878445a3dde5926f05d8f12a266aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.7 KB (251655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:002728f7c925bb71df3e5da9cc8b97957529d0941c02b0738978b7afb9f3fe71`

```dockerfile
```

-	Layers:
	-	`sha256:062994b6c398feef6a43854b00a01e7707ae30982261ff445e2126ac01e775f2`  
		Last Modified: Mon, 22 Jun 2026 19:56:22 GMT  
		Size: 234.1 KB (234149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08db123f70b5a684132c941d3d0f84fbae2815da5b5f949519b98aa5cd924c00`  
		Last Modified: Mon, 22 Jun 2026 19:56:22 GMT  
		Size: 17.5 KB (17506 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.10.9`

```console
$ docker pull chronograf@sha256:1e2982a21cab332a1d8ad29083c6e9799df65e497ecbc0cc4873ae3a64035d7e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `chronograf:1.10.9` - linux; amd64

```console
$ docker pull chronograf@sha256:8760f4d98c23b352d4d55ed05f2a2d92ce01f6f90fa8799de49e7b65617b8433
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.0 MB (85013254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:623aaab10cc07007e12c30b976d188ca4d8c4e0ea0e48994647321d8eb268651`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:42:46 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Thu, 11 Jun 2026 00:42:52 GMT
ENV CHRONOGRAF_VERSION=1.10.9
# Thu, 11 Jun 2026 00:42:52 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Thu, 11 Jun 2026 00:42:52 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Thu, 11 Jun 2026 00:42:52 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Thu, 11 Jun 2026 00:42:52 GMT
EXPOSE map[8888/tcp:{}]
# Thu, 11 Jun 2026 00:42:52 GMT
VOLUME [/var/lib/chronograf]
# Thu, 11 Jun 2026 00:42:52 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Jun 2026 00:42:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jun 2026 00:42:52 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:b9136609bef0128191aa157637b98dd7b98e52154ca60c18258d65957a01c6d0`  
		Last Modified: Wed, 10 Jun 2026 23:39:54 GMT  
		Size: 28.2 MB (28237624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:777573d12ae65c04d3140876bdc7dd031719e58dbe5e06afd0f6bc42c2a93446`  
		Last Modified: Thu, 11 Jun 2026 00:43:04 GMT  
		Size: 7.9 MB (7883331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8265ecc0dd96adcb35313ba4613cce460214db1f07a73e5e72172cd764b98b14`  
		Last Modified: Thu, 11 Jun 2026 00:43:06 GMT  
		Size: 48.9 MB (48867835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf0fa0d395cc097ddfc8f82019202e65ac2146b3d3d62599f7366baf6ba0ba28`  
		Last Modified: Thu, 11 Jun 2026 00:43:03 GMT  
		Size: 12.2 KB (12244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49f74d4683e012dac190c42635e8e1da469e82444707939395a012b8f7683984`  
		Last Modified: Thu, 11 Jun 2026 00:43:04 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75ed6d02a52d2765364e5bce636d8fdc66f7841fe6f3ecea4a7af3fd692c3822`  
		Last Modified: Thu, 11 Jun 2026 00:43:05 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10.9` - unknown; unknown

```console
$ docker pull chronograf@sha256:f8f562e8aedfc102c49ba86357b0fe2dfbcfae5e58e3671bc657984e4cde10ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2871238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91f10898bd9e9279e5245ee4e41146be825b58df23c9689098c49ce2c4172662`

```dockerfile
```

-	Layers:
	-	`sha256:ba7bb74c7a686129cba964213121f515ddff6a6cdf7f0bde5f4d462e229898e7`  
		Last Modified: Thu, 11 Jun 2026 00:43:04 GMT  
		Size: 2.9 MB (2855460 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:859339ed59fbee4a31097c6033f663bd90b976b1f8d123b8f675cfdd52f7e10d`  
		Last Modified: Thu, 11 Jun 2026 00:43:03 GMT  
		Size: 15.8 KB (15778 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.10.9` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:639c91e21b682607057aab5cfafd420d8f4472c05fc185a081319bff4fa6c24e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76803529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4666f0d926abef3a7bfeaea2a178761b4c17e46f160bec33914ebd1e3f8a2f91`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 01:30:52 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Thu, 11 Jun 2026 01:30:58 GMT
ENV CHRONOGRAF_VERSION=1.10.9
# Thu, 11 Jun 2026 01:30:58 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Thu, 11 Jun 2026 01:30:58 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Thu, 11 Jun 2026 01:30:58 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Thu, 11 Jun 2026 01:30:58 GMT
EXPOSE map[8888/tcp:{}]
# Thu, 11 Jun 2026 01:30:58 GMT
VOLUME [/var/lib/chronograf]
# Thu, 11 Jun 2026 01:30:58 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Jun 2026 01:30:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jun 2026 01:30:58 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:8ae2378435d99f39097aa4fd0d6c58c08445becca3153d53205b2cc5054b09c2`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 23.9 MB (23944473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1df41aea1f61522fb0febc178cdc134934f0cdab30cf3fd8116547c6a28ef21`  
		Last Modified: Thu, 11 Jun 2026 01:31:10 GMT  
		Size: 6.5 MB (6514534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:331d7cc0440968a01825592a1c8d60a43171834901f50e2c9a8ac4b5264e1bc9`  
		Last Modified: Thu, 11 Jun 2026 01:31:10 GMT  
		Size: 46.3 MB (46320061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:038c0fedc8f6b97547ba19c2b505783dcf0bda7cf3adaf8777c51fb292f51d92`  
		Last Modified: Thu, 11 Jun 2026 01:31:09 GMT  
		Size: 12.2 KB (12243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1ed94dee9e122944104a9020255dccb60c24e2720e3f2a4b5fea27f83f9774a`  
		Last Modified: Thu, 11 Jun 2026 01:31:09 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79eeb733bfce62026bec9dce96e10e401c7e7f58e6215b318a56a5d2611f429c`  
		Last Modified: Thu, 11 Jun 2026 01:31:10 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10.9` - unknown; unknown

```console
$ docker pull chronograf@sha256:e0208879ba38610ab02632ea313802f16ee1f8ca9a7ec74b45c7f060eb198314
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2873604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69883f0876ac0c1e47b4b99e3f457d761ed9a58e466c57b7b8285f9988c6abae`

```dockerfile
```

-	Layers:
	-	`sha256:ad53705953eece4ee7ac1833378cd196ef5a88915f7e7d4f7a2f3ee9c62c2732`  
		Last Modified: Thu, 11 Jun 2026 01:31:09 GMT  
		Size: 2.9 MB (2857749 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9b1a3e86baf536f21a7ad25234651c13e7a15a8b82108a1c4613774e54b3081`  
		Last Modified: Thu, 11 Jun 2026 01:31:09 GMT  
		Size: 15.9 KB (15855 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.10.9` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:72bf1862281573f4dcca4f4e5e9cff88f81eb7ce97c4029e89db627f083b04d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.9 MB (81855416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e73c21ceecd9ef63c5ae20524c961f624aecb406d843092b6e8f532950d50930`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:44:30 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Thu, 11 Jun 2026 00:44:36 GMT
ENV CHRONOGRAF_VERSION=1.10.9
# Thu, 11 Jun 2026 00:44:36 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Thu, 11 Jun 2026 00:44:36 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Thu, 11 Jun 2026 00:44:36 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Thu, 11 Jun 2026 00:44:36 GMT
EXPOSE map[8888/tcp:{}]
# Thu, 11 Jun 2026 00:44:36 GMT
VOLUME [/var/lib/chronograf]
# Thu, 11 Jun 2026 00:44:36 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Jun 2026 00:44:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jun 2026 00:44:36 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:402614bd39aaec1e4bdcf25aa67f88588fc8d93997a2551c4e130e6ed2b06c7a`  
		Last Modified: Wed, 10 Jun 2026 23:39:57 GMT  
		Size: 28.1 MB (28122307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:178c785dfc4e2d2645c1bc0d89fe671d8526dbbbec573f6604330067f48d5b33`  
		Last Modified: Thu, 11 Jun 2026 00:44:47 GMT  
		Size: 7.7 MB (7699782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bd903b66630bc06414d0520ccc1edd9f5b6461c98195e7b47bf0c7d17de0795`  
		Last Modified: Thu, 11 Jun 2026 00:44:48 GMT  
		Size: 46.0 MB (46008870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dc38ed08988a636521f039fed509393cd9157cc5a0ff0915ff921be433423e4`  
		Last Modified: Thu, 11 Jun 2026 00:44:46 GMT  
		Size: 12.2 KB (12242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5600d08501e1281d85bdf55615e8198a9c7c3c631f674c9eb4ee868a07477d0f`  
		Last Modified: Thu, 11 Jun 2026 00:44:46 GMT  
		Size: 11.9 KB (11901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea605ba23cf1c1bc2740f58bdd6611ff69c9aa72c7e9290df38655ccd2c84cd1`  
		Last Modified: Thu, 11 Jun 2026 00:44:47 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10.9` - unknown; unknown

```console
$ docker pull chronograf@sha256:950f79304babc4401b888321d6fa601af2c4d8408cd895eaa19621efce951ff5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2871595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c55ce2dd578f36a26fb90f267c9d892a5d27aa35b1f10ae87420dd537c367ae`

```dockerfile
```

-	Layers:
	-	`sha256:6dc726da581cbe1357a405d2b55c501d9c9aa548186ac9a0b1f01f758e895ff8`  
		Last Modified: Thu, 11 Jun 2026 00:44:46 GMT  
		Size: 2.9 MB (2855721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:274e20d904a3b4aa7514220ff201a73777954fc6d080ae4e7ca3a20773059822`  
		Last Modified: Thu, 11 Jun 2026 00:44:46 GMT  
		Size: 15.9 KB (15874 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.10.9-alpine`

```console
$ docker pull chronograf@sha256:b000618ec7e3a0bf1931ba9ed12c5b347275dff8172cdb1305dc9a9832d9cbe2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.10.9-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:b8e74c35e5231080b81127e0577e64d64bb246a1e1bcd5d4e650981a9673e64d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.2 MB (33214540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ca665246e4b6f85ea6db5c68c9e874fdcbcad9e207495274a3183239f9d87ee`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:21 GMT
ADD alpine-minirootfs-3.22.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:21 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:56:11 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 22 Jun 2026 19:56:11 GMT
RUN apk add --no-cache ca-certificates setpriv &&     update-ca-certificates # buildkit
# Mon, 22 Jun 2026 19:56:14 GMT
ENV CHRONOGRAF_VERSION=1.10.9
# Mon, 22 Jun 2026 19:56:14 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S chronograf &&     adduser -S chronograf -G chronograf &&     mkdir -m 0750 -p /var/lib/chronograf &&     chown chronograf:chronograf /var/lib/chronograf # buildkit
# Mon, 22 Jun 2026 19:56:14 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 22 Jun 2026 19:56:14 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 22 Jun 2026 19:56:14 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 22 Jun 2026 19:56:14 GMT
VOLUME [/var/lib/chronograf]
# Mon, 22 Jun 2026 19:56:14 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 22 Jun 2026 19:56:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Jun 2026 19:56:14 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:f7ee36c9aa34bbb665f975c76e5c0d1607f0674b94c84cfb0061f87006ea5d10`  
		Last Modified: Mon, 22 Jun 2026 09:11:44 GMT  
		Size: 3.8 MB (3787595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5117c3486ea43e29efca00448cabc535b8f239d757c2ea33ef0320285384ab97`  
		Last Modified: Mon, 22 Jun 2026 19:56:22 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73c138ad4109725f9ac144c7b23085967f20ab7006fd27272598882e140227af`  
		Last Modified: Mon, 22 Jun 2026 19:56:23 GMT  
		Size: 268.0 KB (268025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:880daa7fabb26e5620128d415d7aa48249aacd46940433d1894271ae7ef3a6b5`  
		Last Modified: Mon, 22 Jun 2026 19:56:24 GMT  
		Size: 29.1 MB (29134197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa1f3e1739343a8716664d1b82acab8681f1f3101acf6695f1cf2b791c7f83e5`  
		Last Modified: Mon, 22 Jun 2026 19:56:23 GMT  
		Size: 12.2 KB (12235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:960222739a97c24fefa7b57265a4e13a2acd84bbf3900523fd3a5ad2f9fd1cea`  
		Last Modified: Mon, 22 Jun 2026 19:56:24 GMT  
		Size: 11.9 KB (11894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eab50510b69ae15c2c3be82bc491e2c68e1139bd139081b3f29e976f73e9ae3`  
		Last Modified: Mon, 22 Jun 2026 19:56:24 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10.9-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:5c9a23113a46122ee3f7481e596f13c4931878445a3dde5926f05d8f12a266aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.7 KB (251655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:002728f7c925bb71df3e5da9cc8b97957529d0941c02b0738978b7afb9f3fe71`

```dockerfile
```

-	Layers:
	-	`sha256:062994b6c398feef6a43854b00a01e7707ae30982261ff445e2126ac01e775f2`  
		Last Modified: Mon, 22 Jun 2026 19:56:22 GMT  
		Size: 234.1 KB (234149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08db123f70b5a684132c941d3d0f84fbae2815da5b5f949519b98aa5cd924c00`  
		Last Modified: Mon, 22 Jun 2026 19:56:22 GMT  
		Size: 17.5 KB (17506 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.11`

```console
$ docker pull chronograf@sha256:32c87a379b2e2698e2c03c9b5baec4b150045fb67a9b5d31269ae88d1d33d8f7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `chronograf:1.11` - linux; amd64

```console
$ docker pull chronograf@sha256:73202e652dda47453c6e05e29ca9be91761dcc92f64682de2e149a3d0a622a36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.3 MB (96342670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27932b95b4e46a21c3c4b00e9535bbe9d7155a6a5128abdac0e17faac5c5c816`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:42:55 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Thu, 11 Jun 2026 00:43:02 GMT
ENV CHRONOGRAF_VERSION=1.11.3
# Thu, 11 Jun 2026 00:43:02 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Thu, 11 Jun 2026 00:43:02 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Thu, 11 Jun 2026 00:43:02 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Thu, 11 Jun 2026 00:43:02 GMT
EXPOSE map[8888/tcp:{}]
# Thu, 11 Jun 2026 00:43:02 GMT
VOLUME [/var/lib/chronograf]
# Thu, 11 Jun 2026 00:43:02 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Jun 2026 00:43:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jun 2026 00:43:02 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:b9136609bef0128191aa157637b98dd7b98e52154ca60c18258d65957a01c6d0`  
		Last Modified: Wed, 10 Jun 2026 23:39:54 GMT  
		Size: 28.2 MB (28237624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:556c9fe7644e1166887620855e94c2fba32d97d5e3ed4df537f06c1884a7f0ae`  
		Last Modified: Thu, 11 Jun 2026 00:43:15 GMT  
		Size: 7.9 MB (7883267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b55cf3f7752999b38e3d9223912ce753e63b747ba0ca49f8df5e319c088063e9`  
		Last Modified: Thu, 11 Jun 2026 00:43:16 GMT  
		Size: 60.2 MB (60197307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5769e0d1dcfbaa03829bf62a9018e38189487c8fe5cde7c33ecf939c2b143f7e`  
		Last Modified: Thu, 11 Jun 2026 00:43:15 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e438f602a3cd637900418a3cae8b6eb964b101379fb8aa88f21114895f23481`  
		Last Modified: Thu, 11 Jun 2026 00:43:14 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35b16275212f52100b6eafaf66aa0d7343a79c7ce9ce1ca94ef1ea4dd3aba17d`  
		Last Modified: Thu, 11 Jun 2026 00:43:16 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.11` - unknown; unknown

```console
$ docker pull chronograf@sha256:2c377acca3100b8eded8237f5294e94e498c9d60115575d43098702c544aab82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2889823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07de8db60e77546e14d4ee2975da7c7da016d1f475ba6cdc862591a303a9a83e`

```dockerfile
```

-	Layers:
	-	`sha256:2625568072a9dd1c4abcd0c7a987dab62a3e6c1f9f0afcb55d1ca787025eada8`  
		Last Modified: Thu, 11 Jun 2026 00:43:15 GMT  
		Size: 2.9 MB (2873738 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e92aee71ca4c730a54e0d2b4d449e648529f3c9cf1d08c370c6c63ffc0cf073`  
		Last Modified: Thu, 11 Jun 2026 00:43:15 GMT  
		Size: 16.1 KB (16085 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.11` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:366675e696db69e613db19076980c8908e9b58729a1847e6749ffe90c20dab8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.1 MB (93055462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:459b3796796fdfea3d602ce56fab1cc2c29954072f40d70adc290142e4fb3f8a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:44:38 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Thu, 11 Jun 2026 00:44:47 GMT
ENV CHRONOGRAF_VERSION=1.11.3
# Thu, 11 Jun 2026 00:44:47 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Thu, 11 Jun 2026 00:44:47 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Thu, 11 Jun 2026 00:44:47 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Thu, 11 Jun 2026 00:44:47 GMT
EXPOSE map[8888/tcp:{}]
# Thu, 11 Jun 2026 00:44:47 GMT
VOLUME [/var/lib/chronograf]
# Thu, 11 Jun 2026 00:44:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Jun 2026 00:44:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jun 2026 00:44:47 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:402614bd39aaec1e4bdcf25aa67f88588fc8d93997a2551c4e130e6ed2b06c7a`  
		Last Modified: Wed, 10 Jun 2026 23:39:57 GMT  
		Size: 28.1 MB (28122307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cbdd8fdc217506b94f451fe694a7434259077980dbfce32d678a110b1d5a084`  
		Last Modified: Thu, 11 Jun 2026 00:45:01 GMT  
		Size: 7.7 MB (7699815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8d99986976f45e221d9b9536bb7d61740629e2e34f15c8c96d9f4b700bff729`  
		Last Modified: Thu, 11 Jun 2026 00:45:02 GMT  
		Size: 57.2 MB (57208871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:694ce58a5f420870f543a6533816a87c9081c6d337adb50dc9b0fe82bec5ec9d`  
		Last Modified: Thu, 11 Jun 2026 00:45:00 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a236533c741fb74910832ada4193e1b28ee7b4538e09f17c736fc033514e8c51`  
		Last Modified: Thu, 11 Jun 2026 00:45:01 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08405dd5bfe3886ba00084d0d4013c2b5840b2fea056cdcea79f498c5bcd2084`  
		Last Modified: Thu, 11 Jun 2026 00:45:02 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.11` - unknown; unknown

```console
$ docker pull chronograf@sha256:070e47966d05c2d6ad9490421a9ea383cd4c75362b29b8a8a4dc8548fd72f921
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2889144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40398e85b3e847b5bc169b9a9120493fbe744a1c8ec58c0b8bc92cc77725a6bf`

```dockerfile
```

-	Layers:
	-	`sha256:4cc86ee46eff59029c08f7a731845be8bf30156058866c32b2ae52c16c96560b`  
		Last Modified: Thu, 11 Jun 2026 00:45:01 GMT  
		Size: 2.9 MB (2872952 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06c6deb7e17d185253c508ce914f5f9b2c1c20fb44f7b9fa7fbb5528837f1745`  
		Last Modified: Thu, 11 Jun 2026 00:45:00 GMT  
		Size: 16.2 KB (16192 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.11-alpine`

```console
$ docker pull chronograf@sha256:3a4d1bdde45637be9b012855ab2ecf9847c9bca2629e5895ceff0f08525cd1ba
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.11-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:52a00a974fa31ab104f5615656f1f1ba19124d9dae74d1e3e19095da738ba4cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62242533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3562034250a9e0cf4501b816388ce00db408d02585ac8df9a5f1c9eef9387bd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:21 GMT
ADD alpine-minirootfs-3.22.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:21 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:56:11 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 22 Jun 2026 19:56:11 GMT
RUN apk add --no-cache ca-certificates setpriv &&     update-ca-certificates # buildkit
# Mon, 22 Jun 2026 19:56:16 GMT
ENV CHRONOGRAF_VERSION=1.11.3
# Mon, 22 Jun 2026 19:56:16 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/usr/bin/* &&     cp -a /usr/src/chronograf-*/usr/bin/* /usr/bin &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S chronograf &&     adduser -S chronograf -G chronograf &&     mkdir -m 0750 -p /var/lib/chronograf &&     chown chronograf:chronograf /var/lib/chronograf # buildkit
# Mon, 22 Jun 2026 19:56:16 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 22 Jun 2026 19:56:16 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 22 Jun 2026 19:56:16 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 22 Jun 2026 19:56:16 GMT
VOLUME [/var/lib/chronograf]
# Mon, 22 Jun 2026 19:56:16 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 22 Jun 2026 19:56:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Jun 2026 19:56:16 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:f7ee36c9aa34bbb665f975c76e5c0d1607f0674b94c84cfb0061f87006ea5d10`  
		Last Modified: Mon, 22 Jun 2026 09:11:44 GMT  
		Size: 3.8 MB (3787595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5117c3486ea43e29efca00448cabc535b8f239d757c2ea33ef0320285384ab97`  
		Last Modified: Mon, 22 Jun 2026 19:56:22 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73c138ad4109725f9ac144c7b23085967f20ab7006fd27272598882e140227af`  
		Last Modified: Mon, 22 Jun 2026 19:56:23 GMT  
		Size: 268.0 KB (268025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43c7d0596ef7237fc88fb03d77af3d61b002a1e42ded225a97f9fc69ee2fe95d`  
		Last Modified: Mon, 22 Jun 2026 19:56:30 GMT  
		Size: 58.2 MB (58162177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:881dc26ef020f0cad884e72944ebec73a1f795973e8bfb6c6db1e41060f44516`  
		Last Modified: Mon, 22 Jun 2026 19:56:28 GMT  
		Size: 12.2 KB (12240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0292f8295b205f521c6f751540b266d56de9079017576ebe9221ceff52b54b42`  
		Last Modified: Mon, 22 Jun 2026 19:56:28 GMT  
		Size: 11.9 KB (11901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c48ef1b877e834580c226ecf1161f71b15017d2168d2f2546ee3982dd9be936a`  
		Last Modified: Mon, 22 Jun 2026 19:56:28 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.11-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:53d0c74f55399512e8bcbaf8564c4bdef51e154b5945714c13c0cf04a9fd1873
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.2 KB (270191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43529a8845f8039709e8625c631ae8596244bc3cb3a04816f708e98ea86e12e4`

```dockerfile
```

-	Layers:
	-	`sha256:240b9e5d786fcf925327de71a60eb8944708565e23237bec28592aba486cbeee`  
		Last Modified: Mon, 22 Jun 2026 19:56:28 GMT  
		Size: 252.4 KB (252427 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b290ab107110c261f7aeca24b0147ea4138218fee2d23ddf55b64e55f42ae82c`  
		Last Modified: Mon, 22 Jun 2026 19:56:28 GMT  
		Size: 17.8 KB (17764 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.11.3`

```console
$ docker pull chronograf@sha256:32c87a379b2e2698e2c03c9b5baec4b150045fb67a9b5d31269ae88d1d33d8f7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `chronograf:1.11.3` - linux; amd64

```console
$ docker pull chronograf@sha256:73202e652dda47453c6e05e29ca9be91761dcc92f64682de2e149a3d0a622a36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.3 MB (96342670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27932b95b4e46a21c3c4b00e9535bbe9d7155a6a5128abdac0e17faac5c5c816`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:42:55 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Thu, 11 Jun 2026 00:43:02 GMT
ENV CHRONOGRAF_VERSION=1.11.3
# Thu, 11 Jun 2026 00:43:02 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Thu, 11 Jun 2026 00:43:02 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Thu, 11 Jun 2026 00:43:02 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Thu, 11 Jun 2026 00:43:02 GMT
EXPOSE map[8888/tcp:{}]
# Thu, 11 Jun 2026 00:43:02 GMT
VOLUME [/var/lib/chronograf]
# Thu, 11 Jun 2026 00:43:02 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Jun 2026 00:43:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jun 2026 00:43:02 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:b9136609bef0128191aa157637b98dd7b98e52154ca60c18258d65957a01c6d0`  
		Last Modified: Wed, 10 Jun 2026 23:39:54 GMT  
		Size: 28.2 MB (28237624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:556c9fe7644e1166887620855e94c2fba32d97d5e3ed4df537f06c1884a7f0ae`  
		Last Modified: Thu, 11 Jun 2026 00:43:15 GMT  
		Size: 7.9 MB (7883267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b55cf3f7752999b38e3d9223912ce753e63b747ba0ca49f8df5e319c088063e9`  
		Last Modified: Thu, 11 Jun 2026 00:43:16 GMT  
		Size: 60.2 MB (60197307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5769e0d1dcfbaa03829bf62a9018e38189487c8fe5cde7c33ecf939c2b143f7e`  
		Last Modified: Thu, 11 Jun 2026 00:43:15 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e438f602a3cd637900418a3cae8b6eb964b101379fb8aa88f21114895f23481`  
		Last Modified: Thu, 11 Jun 2026 00:43:14 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35b16275212f52100b6eafaf66aa0d7343a79c7ce9ce1ca94ef1ea4dd3aba17d`  
		Last Modified: Thu, 11 Jun 2026 00:43:16 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.11.3` - unknown; unknown

```console
$ docker pull chronograf@sha256:2c377acca3100b8eded8237f5294e94e498c9d60115575d43098702c544aab82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2889823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07de8db60e77546e14d4ee2975da7c7da016d1f475ba6cdc862591a303a9a83e`

```dockerfile
```

-	Layers:
	-	`sha256:2625568072a9dd1c4abcd0c7a987dab62a3e6c1f9f0afcb55d1ca787025eada8`  
		Last Modified: Thu, 11 Jun 2026 00:43:15 GMT  
		Size: 2.9 MB (2873738 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e92aee71ca4c730a54e0d2b4d449e648529f3c9cf1d08c370c6c63ffc0cf073`  
		Last Modified: Thu, 11 Jun 2026 00:43:15 GMT  
		Size: 16.1 KB (16085 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.11.3` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:366675e696db69e613db19076980c8908e9b58729a1847e6749ffe90c20dab8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.1 MB (93055462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:459b3796796fdfea3d602ce56fab1cc2c29954072f40d70adc290142e4fb3f8a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:44:38 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Thu, 11 Jun 2026 00:44:47 GMT
ENV CHRONOGRAF_VERSION=1.11.3
# Thu, 11 Jun 2026 00:44:47 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Thu, 11 Jun 2026 00:44:47 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Thu, 11 Jun 2026 00:44:47 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Thu, 11 Jun 2026 00:44:47 GMT
EXPOSE map[8888/tcp:{}]
# Thu, 11 Jun 2026 00:44:47 GMT
VOLUME [/var/lib/chronograf]
# Thu, 11 Jun 2026 00:44:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Jun 2026 00:44:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jun 2026 00:44:47 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:402614bd39aaec1e4bdcf25aa67f88588fc8d93997a2551c4e130e6ed2b06c7a`  
		Last Modified: Wed, 10 Jun 2026 23:39:57 GMT  
		Size: 28.1 MB (28122307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cbdd8fdc217506b94f451fe694a7434259077980dbfce32d678a110b1d5a084`  
		Last Modified: Thu, 11 Jun 2026 00:45:01 GMT  
		Size: 7.7 MB (7699815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8d99986976f45e221d9b9536bb7d61740629e2e34f15c8c96d9f4b700bff729`  
		Last Modified: Thu, 11 Jun 2026 00:45:02 GMT  
		Size: 57.2 MB (57208871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:694ce58a5f420870f543a6533816a87c9081c6d337adb50dc9b0fe82bec5ec9d`  
		Last Modified: Thu, 11 Jun 2026 00:45:00 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a236533c741fb74910832ada4193e1b28ee7b4538e09f17c736fc033514e8c51`  
		Last Modified: Thu, 11 Jun 2026 00:45:01 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08405dd5bfe3886ba00084d0d4013c2b5840b2fea056cdcea79f498c5bcd2084`  
		Last Modified: Thu, 11 Jun 2026 00:45:02 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.11.3` - unknown; unknown

```console
$ docker pull chronograf@sha256:070e47966d05c2d6ad9490421a9ea383cd4c75362b29b8a8a4dc8548fd72f921
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2889144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40398e85b3e847b5bc169b9a9120493fbe744a1c8ec58c0b8bc92cc77725a6bf`

```dockerfile
```

-	Layers:
	-	`sha256:4cc86ee46eff59029c08f7a731845be8bf30156058866c32b2ae52c16c96560b`  
		Last Modified: Thu, 11 Jun 2026 00:45:01 GMT  
		Size: 2.9 MB (2872952 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06c6deb7e17d185253c508ce914f5f9b2c1c20fb44f7b9fa7fbb5528837f1745`  
		Last Modified: Thu, 11 Jun 2026 00:45:00 GMT  
		Size: 16.2 KB (16192 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.11.3-alpine`

```console
$ docker pull chronograf@sha256:3a4d1bdde45637be9b012855ab2ecf9847c9bca2629e5895ceff0f08525cd1ba
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.11.3-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:52a00a974fa31ab104f5615656f1f1ba19124d9dae74d1e3e19095da738ba4cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62242533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3562034250a9e0cf4501b816388ce00db408d02585ac8df9a5f1c9eef9387bd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:21 GMT
ADD alpine-minirootfs-3.22.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:21 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:56:11 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 22 Jun 2026 19:56:11 GMT
RUN apk add --no-cache ca-certificates setpriv &&     update-ca-certificates # buildkit
# Mon, 22 Jun 2026 19:56:16 GMT
ENV CHRONOGRAF_VERSION=1.11.3
# Mon, 22 Jun 2026 19:56:16 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/usr/bin/* &&     cp -a /usr/src/chronograf-*/usr/bin/* /usr/bin &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S chronograf &&     adduser -S chronograf -G chronograf &&     mkdir -m 0750 -p /var/lib/chronograf &&     chown chronograf:chronograf /var/lib/chronograf # buildkit
# Mon, 22 Jun 2026 19:56:16 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 22 Jun 2026 19:56:16 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 22 Jun 2026 19:56:16 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 22 Jun 2026 19:56:16 GMT
VOLUME [/var/lib/chronograf]
# Mon, 22 Jun 2026 19:56:16 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 22 Jun 2026 19:56:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Jun 2026 19:56:16 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:f7ee36c9aa34bbb665f975c76e5c0d1607f0674b94c84cfb0061f87006ea5d10`  
		Last Modified: Mon, 22 Jun 2026 09:11:44 GMT  
		Size: 3.8 MB (3787595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5117c3486ea43e29efca00448cabc535b8f239d757c2ea33ef0320285384ab97`  
		Last Modified: Mon, 22 Jun 2026 19:56:22 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73c138ad4109725f9ac144c7b23085967f20ab7006fd27272598882e140227af`  
		Last Modified: Mon, 22 Jun 2026 19:56:23 GMT  
		Size: 268.0 KB (268025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43c7d0596ef7237fc88fb03d77af3d61b002a1e42ded225a97f9fc69ee2fe95d`  
		Last Modified: Mon, 22 Jun 2026 19:56:30 GMT  
		Size: 58.2 MB (58162177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:881dc26ef020f0cad884e72944ebec73a1f795973e8bfb6c6db1e41060f44516`  
		Last Modified: Mon, 22 Jun 2026 19:56:28 GMT  
		Size: 12.2 KB (12240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0292f8295b205f521c6f751540b266d56de9079017576ebe9221ceff52b54b42`  
		Last Modified: Mon, 22 Jun 2026 19:56:28 GMT  
		Size: 11.9 KB (11901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c48ef1b877e834580c226ecf1161f71b15017d2168d2f2546ee3982dd9be936a`  
		Last Modified: Mon, 22 Jun 2026 19:56:28 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.11.3-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:53d0c74f55399512e8bcbaf8564c4bdef51e154b5945714c13c0cf04a9fd1873
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.2 KB (270191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43529a8845f8039709e8625c631ae8596244bc3cb3a04816f708e98ea86e12e4`

```dockerfile
```

-	Layers:
	-	`sha256:240b9e5d786fcf925327de71a60eb8944708565e23237bec28592aba486cbeee`  
		Last Modified: Mon, 22 Jun 2026 19:56:28 GMT  
		Size: 252.4 KB (252427 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b290ab107110c261f7aeca24b0147ea4138218fee2d23ddf55b64e55f42ae82c`  
		Last Modified: Mon, 22 Jun 2026 19:56:28 GMT  
		Size: 17.8 KB (17764 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.8`

```console
$ docker pull chronograf@sha256:8d55c6b70fb68357d195962744560226c993c1c22dd9d299f1107f607f069ef2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `chronograf:1.8` - linux; amd64

```console
$ docker pull chronograf@sha256:1e439b792d7671fd6c8ffc8a60ac1bffc2857ce1f5d4eced6ff400025627d3de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69890738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2600333790d04eb4ec725432dbae4b026c61ca84693a8f34dfc841373207b73`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1781049600'
# Thu, 11 Jun 2026 00:42:36 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Thu, 11 Jun 2026 00:42:41 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Thu, 11 Jun 2026 00:42:41 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Thu, 11 Jun 2026 00:42:41 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Thu, 11 Jun 2026 00:42:41 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Thu, 11 Jun 2026 00:42:41 GMT
EXPOSE map[8888/tcp:{}]
# Thu, 11 Jun 2026 00:42:41 GMT
VOLUME [/var/lib/chronograf]
# Thu, 11 Jun 2026 00:42:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Jun 2026 00:42:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jun 2026 00:42:41 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:55534d9909ecd18467599b415fa2553c3106849154ae8a361a75f1a24f2a4364`  
		Last Modified: Wed, 10 Jun 2026 23:40:12 GMT  
		Size: 30.3 MB (30260255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22a8f9ee435937b73a68b09b4f10c7e7dc7bae1fa64f2aed12bacfed075143ed`  
		Last Modified: Thu, 11 Jun 2026 00:42:53 GMT  
		Size: 5.2 MB (5241790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e058d65f5e3991080a4b28fd688f13360f0ae023127122e8b908cf0f80cc205`  
		Last Modified: Thu, 11 Jun 2026 00:42:54 GMT  
		Size: 34.4 MB (34364302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ef4d76f4fcc665be1c839d3f0d52ab00e63eeee8f9c37db7913501b5d3f8e4a`  
		Last Modified: Thu, 11 Jun 2026 00:42:53 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a03c1b94c7eaa89d8255c32d954aa3ba712faeaee9d7a20b16c8eb07b116895c`  
		Last Modified: Thu, 11 Jun 2026 00:42:53 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a2deb1d5fc5637721df6cf392d65173f500b6c18afa6d92a7e3bdb6301eeef4`  
		Last Modified: Thu, 11 Jun 2026 00:42:54 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8` - unknown; unknown

```console
$ docker pull chronograf@sha256:a1b6203b1e56b65937633a93bb18e8d704d8f2e66cef606aaa745c40c4f60feb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3128709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6843135e3ba85919fe308391857751596a831367ab58ddd25131f7949f79e26`

```dockerfile
```

-	Layers:
	-	`sha256:1009073240f04db00e4d9e2f219aad983d6d3a15e2b7cb17ac0f075c77e8a430`  
		Last Modified: Thu, 11 Jun 2026 00:42:53 GMT  
		Size: 3.1 MB (3112935 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d113cf753f2109946937ba86568269f470996afbd8cd1293f3db300b389fe4f3`  
		Last Modified: Thu, 11 Jun 2026 00:42:53 GMT  
		Size: 15.8 KB (15774 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.8` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:3f95c764a35f6e4501be84c1c61262c6c064895430cde7b8db4aefb8ad46c201
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.6 MB (62622172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ea339cbe386802b3303c6ebe6dc921c81062110c2bfea397e820f153450897c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1781049600'
# Thu, 11 Jun 2026 01:27:36 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Thu, 11 Jun 2026 01:27:42 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Thu, 11 Jun 2026 01:27:42 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Thu, 11 Jun 2026 01:27:42 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Thu, 11 Jun 2026 01:27:42 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Thu, 11 Jun 2026 01:27:42 GMT
EXPOSE map[8888/tcp:{}]
# Thu, 11 Jun 2026 01:27:42 GMT
VOLUME [/var/lib/chronograf]
# Thu, 11 Jun 2026 01:27:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Jun 2026 01:27:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jun 2026 01:27:42 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:7ba7c49f3099e93649e55cb3558e8587e0d0458fc435dfc054641c2347c164c3`  
		Last Modified: Wed, 10 Jun 2026 23:41:03 GMT  
		Size: 25.6 MB (25552842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e014713bc166be47a9d8f88e598297524f9d638ef5ce9ff860ae4c0d7dd67b02`  
		Last Modified: Thu, 11 Jun 2026 01:27:51 GMT  
		Size: 4.5 MB (4510004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5bcbe5a5dbdc69fb4769d18affef7f32c21bf720219d7d1ba4463c4fe7367a7`  
		Last Modified: Thu, 11 Jun 2026 01:27:52 GMT  
		Size: 32.5 MB (32534926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea153933869befe249036fd6775f02fb5600d23eac143eeb3682cc1be80c1f3f`  
		Last Modified: Thu, 11 Jun 2026 01:27:51 GMT  
		Size: 12.3 KB (12251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:331c02c2917d9a903f75f34872bf01ebe04736f5dc68c67afd140bf239f77563`  
		Last Modified: Thu, 11 Jun 2026 01:27:51 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31a2fad6e06b7ebf65823dae42950f8c359eeb306c6b5285446db94d3b817948`  
		Last Modified: Thu, 11 Jun 2026 01:27:52 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8` - unknown; unknown

```console
$ docker pull chronograf@sha256:e5b1647ce5e442ecefc2acc55d370c8fedba653d8d94de159664e1e358197fe6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3131057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a447b7b61e340a3c59ebe8de88d44df16b8ec1fbb70fd6fe11d77774214bd1ec`

```dockerfile
```

-	Layers:
	-	`sha256:761e7a5a9689b80b5b77432aad45f81ce5cd62e6aaeca392a02d78d71729f8d8`  
		Last Modified: Thu, 11 Jun 2026 01:27:51 GMT  
		Size: 3.1 MB (3115206 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d74fb231948790e3fc8a8dbafcffeee70ae105db709a86bcf79cbe39c0339c54`  
		Last Modified: Thu, 11 Jun 2026 01:27:50 GMT  
		Size: 15.9 KB (15851 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.8` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:e16bf739f132ce96d4d9d673420e4d62850ff84946dbaa16bc3998490a6c2014
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.4 MB (66429847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b38ef6547e36ccb4653f478d7db3c67432f27c7637753f773c4bc864f86c3bfd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1781049600'
# Thu, 11 Jun 2026 00:44:24 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Thu, 11 Jun 2026 00:44:29 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Thu, 11 Jun 2026 00:44:29 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Thu, 11 Jun 2026 00:44:29 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Thu, 11 Jun 2026 00:44:29 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Thu, 11 Jun 2026 00:44:29 GMT
EXPOSE map[8888/tcp:{}]
# Thu, 11 Jun 2026 00:44:29 GMT
VOLUME [/var/lib/chronograf]
# Thu, 11 Jun 2026 00:44:29 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Jun 2026 00:44:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jun 2026 00:44:29 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:ca483a18241c226a06a4a4afd22dc5496062254c671fa595136458fb8fcd0107`  
		Last Modified: Wed, 10 Jun 2026 23:39:58 GMT  
		Size: 28.7 MB (28746154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e341d0ac5bbdb331124debfb6813c85c084a06b0416c43928bdd16f7c0716733`  
		Last Modified: Thu, 11 Jun 2026 00:44:39 GMT  
		Size: 5.2 MB (5229756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad32dadbf3b8cd84900380d055bf855bee871dc3bce9254e68bfbc5f3657403a`  
		Last Modified: Thu, 11 Jun 2026 00:44:40 GMT  
		Size: 32.4 MB (32429544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe032898a3f18428d230e9de2b6cbad1a873637512ac63dc4bf0e7c4d9f16bb`  
		Last Modified: Thu, 11 Jun 2026 00:44:39 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a10c04e323776353688e398257d70b7e7b14da2f96ab8f536697ffc23c55601b`  
		Last Modified: Thu, 11 Jun 2026 00:44:39 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5c94cc7d3d38eac603465be77ec6ec969b7d9e30f07f4a311ef23b51eb93bc7`  
		Last Modified: Thu, 11 Jun 2026 00:44:41 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8` - unknown; unknown

```console
$ docker pull chronograf@sha256:3a83a759df46f98242e97204ab1d4b61623bd44dc7c7eaf8c3acb4ac69e4ff24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3129053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2ae0acb9d314921905e18b5dd10c4cf28dafe0f47f0752fa79e598603b40ac8`

```dockerfile
```

-	Layers:
	-	`sha256:469275a625ee152f0926abd75cb28346ba986e2714f3ae5a87901b0835d12dac`  
		Last Modified: Thu, 11 Jun 2026 00:44:40 GMT  
		Size: 3.1 MB (3113184 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a124d0267f99a904f0b7cc98b2b7b81d58c69be2dc9a065b27bc63d48f29932`  
		Last Modified: Thu, 11 Jun 2026 00:44:39 GMT  
		Size: 15.9 KB (15869 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.8-alpine`

```console
$ docker pull chronograf@sha256:a04ddb5aa8a08101f1c16ed3a397ee4c00dcd1ed76208f0bb50c429653294520
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.8-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:ede13c1b68d5428c626bce6c59f200e2d2f72711e9e1b8d337bf08d17699af43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23147985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1664c3e0943c41cb0fbb18db90fb8ff72cabbfa2721d8832c2b45834ec9ce934`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:26 GMT
ADD alpine-minirootfs-3.20.10-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:26 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:23:28 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 17 Apr 2026 00:23:28 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates # buildkit
# Fri, 17 Apr 2026 00:23:32 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Fri, 17 Apr 2026 00:23:32 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Fri, 17 Apr 2026 00:23:32 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 17 Apr 2026 00:23:32 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 17 Apr 2026 00:23:32 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 17 Apr 2026 00:23:32 GMT
VOLUME [/var/lib/chronograf]
# Fri, 17 Apr 2026 00:23:32 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 17 Apr 2026 00:23:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 17 Apr 2026 00:23:32 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:25f1d6b1951ac8eb3740558fe94cb83d377bdadf95fd9f98b50d2e1b96130471`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.6 MB (3630321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a16e69077797f1a90c5b8946765d6547bd0bbe62c5edf87016fc687d8691b62a`  
		Last Modified: Fri, 17 Apr 2026 00:23:39 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a582e81c7ed2cd8d0c8d79c49ea73d52bfddf13469c4d924f55b6970462df01`  
		Last Modified: Fri, 17 Apr 2026 00:23:39 GMT  
		Size: 289.1 KB (289074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaa13e0a8fa89698c9691e91370f5c5da3380b44b6ac29319a4e90a09eefbe8e`  
		Last Modified: Fri, 17 Apr 2026 00:23:40 GMT  
		Size: 19.2 MB (19203941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:782461697da8106fc90296b3ce4a6a407db932533ecd9a4da24a10753acdcf1e`  
		Last Modified: Fri, 17 Apr 2026 00:23:39 GMT  
		Size: 12.2 KB (12237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e74b1d522539dce72171cebaa3d6dd0ca9ca821e4a34e4b76dc19daa0169a5c3`  
		Last Modified: Fri, 17 Apr 2026 00:23:40 GMT  
		Size: 11.9 KB (11896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce8f5e2ebfd8736864ace9d37094fa3ee04d93d2ae268e430ca56f87eec508a5`  
		Last Modified: Fri, 17 Apr 2026 00:23:40 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:84b7bdc8d23f218c2fe980ddfdeac820e2627fc7d91f2c4202a8f26deb5e9db1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.5 KB (244523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:983e28495a7b578fd93bcd0c3b0e98c83deddb61c866fc1c2f690ba762da5922`

```dockerfile
```

-	Layers:
	-	`sha256:365c42781b673303c2c41d46ccc50ac379917ed1053135d373385311589519d1`  
		Last Modified: Fri, 17 Apr 2026 00:23:39 GMT  
		Size: 227.7 KB (227654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8bfb7d23b735a7cd84710b5948163b988bb486b65c2263456936b73344a8c85`  
		Last Modified: Fri, 17 Apr 2026 00:23:39 GMT  
		Size: 16.9 KB (16869 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.8.10`

```console
$ docker pull chronograf@sha256:8d55c6b70fb68357d195962744560226c993c1c22dd9d299f1107f607f069ef2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `chronograf:1.8.10` - linux; amd64

```console
$ docker pull chronograf@sha256:1e439b792d7671fd6c8ffc8a60ac1bffc2857ce1f5d4eced6ff400025627d3de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69890738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2600333790d04eb4ec725432dbae4b026c61ca84693a8f34dfc841373207b73`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1781049600'
# Thu, 11 Jun 2026 00:42:36 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Thu, 11 Jun 2026 00:42:41 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Thu, 11 Jun 2026 00:42:41 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Thu, 11 Jun 2026 00:42:41 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Thu, 11 Jun 2026 00:42:41 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Thu, 11 Jun 2026 00:42:41 GMT
EXPOSE map[8888/tcp:{}]
# Thu, 11 Jun 2026 00:42:41 GMT
VOLUME [/var/lib/chronograf]
# Thu, 11 Jun 2026 00:42:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Jun 2026 00:42:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jun 2026 00:42:41 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:55534d9909ecd18467599b415fa2553c3106849154ae8a361a75f1a24f2a4364`  
		Last Modified: Wed, 10 Jun 2026 23:40:12 GMT  
		Size: 30.3 MB (30260255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22a8f9ee435937b73a68b09b4f10c7e7dc7bae1fa64f2aed12bacfed075143ed`  
		Last Modified: Thu, 11 Jun 2026 00:42:53 GMT  
		Size: 5.2 MB (5241790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e058d65f5e3991080a4b28fd688f13360f0ae023127122e8b908cf0f80cc205`  
		Last Modified: Thu, 11 Jun 2026 00:42:54 GMT  
		Size: 34.4 MB (34364302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ef4d76f4fcc665be1c839d3f0d52ab00e63eeee8f9c37db7913501b5d3f8e4a`  
		Last Modified: Thu, 11 Jun 2026 00:42:53 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a03c1b94c7eaa89d8255c32d954aa3ba712faeaee9d7a20b16c8eb07b116895c`  
		Last Modified: Thu, 11 Jun 2026 00:42:53 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a2deb1d5fc5637721df6cf392d65173f500b6c18afa6d92a7e3bdb6301eeef4`  
		Last Modified: Thu, 11 Jun 2026 00:42:54 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:a1b6203b1e56b65937633a93bb18e8d704d8f2e66cef606aaa745c40c4f60feb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3128709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6843135e3ba85919fe308391857751596a831367ab58ddd25131f7949f79e26`

```dockerfile
```

-	Layers:
	-	`sha256:1009073240f04db00e4d9e2f219aad983d6d3a15e2b7cb17ac0f075c77e8a430`  
		Last Modified: Thu, 11 Jun 2026 00:42:53 GMT  
		Size: 3.1 MB (3112935 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d113cf753f2109946937ba86568269f470996afbd8cd1293f3db300b389fe4f3`  
		Last Modified: Thu, 11 Jun 2026 00:42:53 GMT  
		Size: 15.8 KB (15774 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.8.10` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:3f95c764a35f6e4501be84c1c61262c6c064895430cde7b8db4aefb8ad46c201
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.6 MB (62622172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ea339cbe386802b3303c6ebe6dc921c81062110c2bfea397e820f153450897c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1781049600'
# Thu, 11 Jun 2026 01:27:36 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Thu, 11 Jun 2026 01:27:42 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Thu, 11 Jun 2026 01:27:42 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Thu, 11 Jun 2026 01:27:42 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Thu, 11 Jun 2026 01:27:42 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Thu, 11 Jun 2026 01:27:42 GMT
EXPOSE map[8888/tcp:{}]
# Thu, 11 Jun 2026 01:27:42 GMT
VOLUME [/var/lib/chronograf]
# Thu, 11 Jun 2026 01:27:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Jun 2026 01:27:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jun 2026 01:27:42 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:7ba7c49f3099e93649e55cb3558e8587e0d0458fc435dfc054641c2347c164c3`  
		Last Modified: Wed, 10 Jun 2026 23:41:03 GMT  
		Size: 25.6 MB (25552842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e014713bc166be47a9d8f88e598297524f9d638ef5ce9ff860ae4c0d7dd67b02`  
		Last Modified: Thu, 11 Jun 2026 01:27:51 GMT  
		Size: 4.5 MB (4510004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5bcbe5a5dbdc69fb4769d18affef7f32c21bf720219d7d1ba4463c4fe7367a7`  
		Last Modified: Thu, 11 Jun 2026 01:27:52 GMT  
		Size: 32.5 MB (32534926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea153933869befe249036fd6775f02fb5600d23eac143eeb3682cc1be80c1f3f`  
		Last Modified: Thu, 11 Jun 2026 01:27:51 GMT  
		Size: 12.3 KB (12251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:331c02c2917d9a903f75f34872bf01ebe04736f5dc68c67afd140bf239f77563`  
		Last Modified: Thu, 11 Jun 2026 01:27:51 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31a2fad6e06b7ebf65823dae42950f8c359eeb306c6b5285446db94d3b817948`  
		Last Modified: Thu, 11 Jun 2026 01:27:52 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:e5b1647ce5e442ecefc2acc55d370c8fedba653d8d94de159664e1e358197fe6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3131057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a447b7b61e340a3c59ebe8de88d44df16b8ec1fbb70fd6fe11d77774214bd1ec`

```dockerfile
```

-	Layers:
	-	`sha256:761e7a5a9689b80b5b77432aad45f81ce5cd62e6aaeca392a02d78d71729f8d8`  
		Last Modified: Thu, 11 Jun 2026 01:27:51 GMT  
		Size: 3.1 MB (3115206 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d74fb231948790e3fc8a8dbafcffeee70ae105db709a86bcf79cbe39c0339c54`  
		Last Modified: Thu, 11 Jun 2026 01:27:50 GMT  
		Size: 15.9 KB (15851 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.8.10` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:e16bf739f132ce96d4d9d673420e4d62850ff84946dbaa16bc3998490a6c2014
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.4 MB (66429847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b38ef6547e36ccb4653f478d7db3c67432f27c7637753f773c4bc864f86c3bfd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1781049600'
# Thu, 11 Jun 2026 00:44:24 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Thu, 11 Jun 2026 00:44:29 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Thu, 11 Jun 2026 00:44:29 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Thu, 11 Jun 2026 00:44:29 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Thu, 11 Jun 2026 00:44:29 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Thu, 11 Jun 2026 00:44:29 GMT
EXPOSE map[8888/tcp:{}]
# Thu, 11 Jun 2026 00:44:29 GMT
VOLUME [/var/lib/chronograf]
# Thu, 11 Jun 2026 00:44:29 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Jun 2026 00:44:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jun 2026 00:44:29 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:ca483a18241c226a06a4a4afd22dc5496062254c671fa595136458fb8fcd0107`  
		Last Modified: Wed, 10 Jun 2026 23:39:58 GMT  
		Size: 28.7 MB (28746154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e341d0ac5bbdb331124debfb6813c85c084a06b0416c43928bdd16f7c0716733`  
		Last Modified: Thu, 11 Jun 2026 00:44:39 GMT  
		Size: 5.2 MB (5229756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad32dadbf3b8cd84900380d055bf855bee871dc3bce9254e68bfbc5f3657403a`  
		Last Modified: Thu, 11 Jun 2026 00:44:40 GMT  
		Size: 32.4 MB (32429544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe032898a3f18428d230e9de2b6cbad1a873637512ac63dc4bf0e7c4d9f16bb`  
		Last Modified: Thu, 11 Jun 2026 00:44:39 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a10c04e323776353688e398257d70b7e7b14da2f96ab8f536697ffc23c55601b`  
		Last Modified: Thu, 11 Jun 2026 00:44:39 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5c94cc7d3d38eac603465be77ec6ec969b7d9e30f07f4a311ef23b51eb93bc7`  
		Last Modified: Thu, 11 Jun 2026 00:44:41 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:3a83a759df46f98242e97204ab1d4b61623bd44dc7c7eaf8c3acb4ac69e4ff24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3129053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2ae0acb9d314921905e18b5dd10c4cf28dafe0f47f0752fa79e598603b40ac8`

```dockerfile
```

-	Layers:
	-	`sha256:469275a625ee152f0926abd75cb28346ba986e2714f3ae5a87901b0835d12dac`  
		Last Modified: Thu, 11 Jun 2026 00:44:40 GMT  
		Size: 3.1 MB (3113184 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a124d0267f99a904f0b7cc98b2b7b81d58c69be2dc9a065b27bc63d48f29932`  
		Last Modified: Thu, 11 Jun 2026 00:44:39 GMT  
		Size: 15.9 KB (15869 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.8.10-alpine`

```console
$ docker pull chronograf@sha256:a04ddb5aa8a08101f1c16ed3a397ee4c00dcd1ed76208f0bb50c429653294520
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.8.10-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:ede13c1b68d5428c626bce6c59f200e2d2f72711e9e1b8d337bf08d17699af43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23147985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1664c3e0943c41cb0fbb18db90fb8ff72cabbfa2721d8832c2b45834ec9ce934`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:26 GMT
ADD alpine-minirootfs-3.20.10-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:26 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:23:28 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 17 Apr 2026 00:23:28 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates # buildkit
# Fri, 17 Apr 2026 00:23:32 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Fri, 17 Apr 2026 00:23:32 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Fri, 17 Apr 2026 00:23:32 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 17 Apr 2026 00:23:32 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 17 Apr 2026 00:23:32 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 17 Apr 2026 00:23:32 GMT
VOLUME [/var/lib/chronograf]
# Fri, 17 Apr 2026 00:23:32 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 17 Apr 2026 00:23:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 17 Apr 2026 00:23:32 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:25f1d6b1951ac8eb3740558fe94cb83d377bdadf95fd9f98b50d2e1b96130471`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.6 MB (3630321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a16e69077797f1a90c5b8946765d6547bd0bbe62c5edf87016fc687d8691b62a`  
		Last Modified: Fri, 17 Apr 2026 00:23:39 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a582e81c7ed2cd8d0c8d79c49ea73d52bfddf13469c4d924f55b6970462df01`  
		Last Modified: Fri, 17 Apr 2026 00:23:39 GMT  
		Size: 289.1 KB (289074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaa13e0a8fa89698c9691e91370f5c5da3380b44b6ac29319a4e90a09eefbe8e`  
		Last Modified: Fri, 17 Apr 2026 00:23:40 GMT  
		Size: 19.2 MB (19203941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:782461697da8106fc90296b3ce4a6a407db932533ecd9a4da24a10753acdcf1e`  
		Last Modified: Fri, 17 Apr 2026 00:23:39 GMT  
		Size: 12.2 KB (12237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e74b1d522539dce72171cebaa3d6dd0ca9ca821e4a34e4b76dc19daa0169a5c3`  
		Last Modified: Fri, 17 Apr 2026 00:23:40 GMT  
		Size: 11.9 KB (11896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce8f5e2ebfd8736864ace9d37094fa3ee04d93d2ae268e430ca56f87eec508a5`  
		Last Modified: Fri, 17 Apr 2026 00:23:40 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8.10-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:84b7bdc8d23f218c2fe980ddfdeac820e2627fc7d91f2c4202a8f26deb5e9db1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.5 KB (244523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:983e28495a7b578fd93bcd0c3b0e98c83deddb61c866fc1c2f690ba762da5922`

```dockerfile
```

-	Layers:
	-	`sha256:365c42781b673303c2c41d46ccc50ac379917ed1053135d373385311589519d1`  
		Last Modified: Fri, 17 Apr 2026 00:23:39 GMT  
		Size: 227.7 KB (227654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8bfb7d23b735a7cd84710b5948163b988bb486b65c2263456936b73344a8c85`  
		Last Modified: Fri, 17 Apr 2026 00:23:39 GMT  
		Size: 16.9 KB (16869 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.9`

```console
$ docker pull chronograf@sha256:0b3c072df39f12bec0604f8e4a7c02b42085ab88ac4c28e1cc60140a70d06bc5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `chronograf:1.9` - linux; amd64

```console
$ docker pull chronograf@sha256:32542ded9c70fb95366b306747b0d6a3347e7cef6a8cb9e9b3e755f076717107
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.5 MB (70538271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:072289548e73d5fd6e32652ce90ad3f1ac4d9b33ed111d22e7f54c6c13ff9cfb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1781049600'
# Thu, 11 Jun 2026 00:42:42 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Thu, 11 Jun 2026 00:42:47 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Thu, 11 Jun 2026 00:42:47 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Thu, 11 Jun 2026 00:42:47 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Thu, 11 Jun 2026 00:42:47 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Thu, 11 Jun 2026 00:42:47 GMT
EXPOSE map[8888/tcp:{}]
# Thu, 11 Jun 2026 00:42:47 GMT
VOLUME [/var/lib/chronograf]
# Thu, 11 Jun 2026 00:42:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Jun 2026 00:42:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jun 2026 00:42:47 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:55534d9909ecd18467599b415fa2553c3106849154ae8a361a75f1a24f2a4364`  
		Last Modified: Wed, 10 Jun 2026 23:40:12 GMT  
		Size: 30.3 MB (30260255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a7bdc72d9028986df2b45952024236a0819caa65c325a9fd7bf9de39249739a`  
		Last Modified: Thu, 11 Jun 2026 00:42:57 GMT  
		Size: 5.2 MB (5241824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83b6d5f6adf14d81aae67dbcdcd6c02a70d7e356b964c04909ca7c5b79ed5c69`  
		Last Modified: Thu, 11 Jun 2026 00:42:58 GMT  
		Size: 35.0 MB (35011793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6bf247abac0bf2f179e1f2cca7d386578342bbfe29165f2a58c12bb9763e6ad`  
		Last Modified: Thu, 11 Jun 2026 00:42:57 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03fa09ba0e2903ef66131333061ca8e147d71aa0ef81d29a52e6c26dc0c9e891`  
		Last Modified: Thu, 11 Jun 2026 00:42:57 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ead191d8839dce1287ecd618fe4c0f9cb5f7e6d5948f846d1709c87bc8a8a96f`  
		Last Modified: Thu, 11 Jun 2026 00:42:58 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9` - unknown; unknown

```console
$ docker pull chronograf@sha256:b7892bbd95b79b2e9b046d9883e0831c1730eea41bfbba42017ca881232cdfc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3133911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ea80191cc26817177d9561dce8be523862932c2bf410fe773b1efdfe07829e0`

```dockerfile
```

-	Layers:
	-	`sha256:e5bc946ec96ec7515621519b871b5af30e6d5594444542e847e87a0ea3b0e4df`  
		Last Modified: Thu, 11 Jun 2026 00:42:57 GMT  
		Size: 3.1 MB (3118145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e82797b3fff0fad4e31be88bebbab91a4b094033f184d37402a6909d684dac5`  
		Last Modified: Thu, 11 Jun 2026 00:42:57 GMT  
		Size: 15.8 KB (15766 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.9` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:2dd3b604b75fc1345005187f4d027108c161dd5ec069eca28244a748ed25828e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.4 MB (63398862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d315e2a8fad8acc889f6ba99c39cbd51ef0da7b0a6e3242f316f9da213914de`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1781049600'
# Thu, 11 Jun 2026 01:30:00 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Thu, 11 Jun 2026 01:30:06 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Thu, 11 Jun 2026 01:30:06 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Thu, 11 Jun 2026 01:30:06 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Thu, 11 Jun 2026 01:30:06 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Thu, 11 Jun 2026 01:30:06 GMT
EXPOSE map[8888/tcp:{}]
# Thu, 11 Jun 2026 01:30:06 GMT
VOLUME [/var/lib/chronograf]
# Thu, 11 Jun 2026 01:30:06 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Jun 2026 01:30:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jun 2026 01:30:06 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:7ba7c49f3099e93649e55cb3558e8587e0d0458fc435dfc054641c2347c164c3`  
		Last Modified: Wed, 10 Jun 2026 23:41:03 GMT  
		Size: 25.6 MB (25552842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c20941bb3fef46667d0d5a409f5af50ede5940752aa8f393102fcf8f50ca1cfb`  
		Last Modified: Thu, 11 Jun 2026 01:30:15 GMT  
		Size: 4.5 MB (4510022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec94f538042ffbe6e7eaf08bd13fff7167d821a78e59d2e881c1f37975e4b024`  
		Last Modified: Thu, 11 Jun 2026 01:30:16 GMT  
		Size: 33.3 MB (33311608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aff2626e7077f77945ce85e013761b933b09a62c409f16a8eec49a7dc37f3cce`  
		Last Modified: Thu, 11 Jun 2026 01:30:15 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eb94ee72c6ca1d75aaf85172079d6b7ce2e7603f6858631534af0eddafa112c`  
		Last Modified: Thu, 11 Jun 2026 01:30:15 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df6fc0e520062fddde04b66698b8bdf2ef4e491eef339d04bd1434f397c363ba`  
		Last Modified: Thu, 11 Jun 2026 01:30:16 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9` - unknown; unknown

```console
$ docker pull chronograf@sha256:2d94b054096c58434be5263e6b40ccdd929f8f90c747b85096fd9f633dca6554
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3136260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18f6ab3887b23f0ff5d3000a41f2181507090fdace3367ede248e9b0c02a664c`

```dockerfile
```

-	Layers:
	-	`sha256:e48ee6c0ed75c15910d66f5baab4f2c94e4fbd91e8c60e7cbe7904debd065695`  
		Last Modified: Thu, 11 Jun 2026 01:30:15 GMT  
		Size: 3.1 MB (3120416 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f73e74106e44f894390b70e4fe2cd6d212d082d34afb53c66857920e1281f27a`  
		Last Modified: Thu, 11 Jun 2026 01:30:15 GMT  
		Size: 15.8 KB (15844 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.9` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:13a5d5516c5c08972df8e2058ad688253823a7d516fc7151c87de2cae2bc9d0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.2 MB (67182728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f42e74d6e13181f1e38f2b9ae78395bd19206349d4cbe6f6d9aabbb7959ecc4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1781049600'
# Thu, 11 Jun 2026 00:44:26 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Thu, 11 Jun 2026 00:44:31 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Thu, 11 Jun 2026 00:44:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Thu, 11 Jun 2026 00:44:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Thu, 11 Jun 2026 00:44:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Thu, 11 Jun 2026 00:44:31 GMT
EXPOSE map[8888/tcp:{}]
# Thu, 11 Jun 2026 00:44:31 GMT
VOLUME [/var/lib/chronograf]
# Thu, 11 Jun 2026 00:44:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Jun 2026 00:44:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jun 2026 00:44:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:ca483a18241c226a06a4a4afd22dc5496062254c671fa595136458fb8fcd0107`  
		Last Modified: Wed, 10 Jun 2026 23:39:58 GMT  
		Size: 28.7 MB (28746154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df19c65db679567b25fc6b51a89f0ff023c30f29903c61d91f8d09932f0a3dc1`  
		Last Modified: Thu, 11 Jun 2026 00:44:42 GMT  
		Size: 5.2 MB (5229810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f9e82af0818c57d4f43beffa14fd87f50ffa4a287a4c3ae1517efad2830a88c`  
		Last Modified: Thu, 11 Jun 2026 00:44:43 GMT  
		Size: 33.2 MB (33182372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92be84d6df7a557e61d79e4ef84158fd8d80543adef294aa6873d44207e1d0a7`  
		Last Modified: Thu, 11 Jun 2026 00:44:41 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9448ee11a9a3cdfe843f2bb8c686389731c2e97dfb8f9049256ddfa914f35700`  
		Last Modified: Thu, 11 Jun 2026 00:44:42 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0e6ab33c0bd1b32d26a88bcb4a50fb7e42c945c9403cb9f2d90674f19d08693`  
		Last Modified: Thu, 11 Jun 2026 00:44:43 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9` - unknown; unknown

```console
$ docker pull chronograf@sha256:45b67a28529bf52a66596f3b659bd1685bff505bf7025e7026bf13c5197f28f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3134256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f68ef40d1fe35c619e0deea588177adc79fbc4b01fc3b5f6afeba8c3ddb67406`

```dockerfile
```

-	Layers:
	-	`sha256:f974f608f04ecea1e41a00f32d27e537cb12d903a4d5dfe6769774712f99bc56`  
		Last Modified: Thu, 11 Jun 2026 00:44:42 GMT  
		Size: 3.1 MB (3118394 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f38eda398bda25bcb3de057dd0703272dbb3660477e629bc1049d2ca6b0ec1c4`  
		Last Modified: Thu, 11 Jun 2026 00:44:41 GMT  
		Size: 15.9 KB (15862 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.9-alpine`

```console
$ docker pull chronograf@sha256:0f80cd3823ff72714fb0be9429588b58a6cd474733e0369bc7f9181346b1d5cd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.9-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:f621eed42ec67e2c0af874c13b22cf7c5eca4a2f92496e0e777e83e0d0e54a18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23616085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d4f080ba353421341131d427d195e080f057481b2369a3ddd4db288e7a49570`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:26 GMT
ADD alpine-minirootfs-3.20.10-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:26 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:23:28 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 17 Apr 2026 00:23:28 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates # buildkit
# Fri, 17 Apr 2026 00:23:32 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Fri, 17 Apr 2026 00:23:32 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Fri, 17 Apr 2026 00:23:32 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 17 Apr 2026 00:23:32 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 17 Apr 2026 00:23:32 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 17 Apr 2026 00:23:32 GMT
VOLUME [/var/lib/chronograf]
# Fri, 17 Apr 2026 00:23:32 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 17 Apr 2026 00:23:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 17 Apr 2026 00:23:32 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:25f1d6b1951ac8eb3740558fe94cb83d377bdadf95fd9f98b50d2e1b96130471`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.6 MB (3630321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a16e69077797f1a90c5b8946765d6547bd0bbe62c5edf87016fc687d8691b62a`  
		Last Modified: Fri, 17 Apr 2026 00:23:39 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a582e81c7ed2cd8d0c8d79c49ea73d52bfddf13469c4d924f55b6970462df01`  
		Last Modified: Fri, 17 Apr 2026 00:23:39 GMT  
		Size: 289.1 KB (289074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaea6127a47f8ad745d11f7e8ea7511652ab602293817f95bee9cac7032fc393`  
		Last Modified: Fri, 17 Apr 2026 00:23:39 GMT  
		Size: 19.7 MB (19672041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:782461697da8106fc90296b3ce4a6a407db932533ecd9a4da24a10753acdcf1e`  
		Last Modified: Fri, 17 Apr 2026 00:23:39 GMT  
		Size: 12.2 KB (12237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e74b1d522539dce72171cebaa3d6dd0ca9ca821e4a34e4b76dc19daa0169a5c3`  
		Last Modified: Fri, 17 Apr 2026 00:23:40 GMT  
		Size: 11.9 KB (11896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce8f5e2ebfd8736864ace9d37094fa3ee04d93d2ae268e430ca56f87eec508a5`  
		Last Modified: Fri, 17 Apr 2026 00:23:40 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:4be611f408b68b71f2ce6e27bd942207676513556d3d2d9ec7df73b913fb49b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.7 KB (249732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8b7b7e44d247f14c51737c4557d3e8bdc7e3cc786d83a99199fb64c7df6355c`

```dockerfile
```

-	Layers:
	-	`sha256:6c6b091fcc28e6afcad2a5fe2faed4c1dcff63c11868d95adf1b2056b7bbcae1`  
		Last Modified: Fri, 17 Apr 2026 00:23:39 GMT  
		Size: 232.9 KB (232866 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d10cb23e42c41cf8502d564e4146e704991853b11b9b54a94f89af55f1264769`  
		Last Modified: Fri, 17 Apr 2026 00:23:39 GMT  
		Size: 16.9 KB (16866 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.9.4`

```console
$ docker pull chronograf@sha256:0b3c072df39f12bec0604f8e4a7c02b42085ab88ac4c28e1cc60140a70d06bc5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `chronograf:1.9.4` - linux; amd64

```console
$ docker pull chronograf@sha256:32542ded9c70fb95366b306747b0d6a3347e7cef6a8cb9e9b3e755f076717107
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.5 MB (70538271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:072289548e73d5fd6e32652ce90ad3f1ac4d9b33ed111d22e7f54c6c13ff9cfb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1781049600'
# Thu, 11 Jun 2026 00:42:42 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Thu, 11 Jun 2026 00:42:47 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Thu, 11 Jun 2026 00:42:47 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Thu, 11 Jun 2026 00:42:47 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Thu, 11 Jun 2026 00:42:47 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Thu, 11 Jun 2026 00:42:47 GMT
EXPOSE map[8888/tcp:{}]
# Thu, 11 Jun 2026 00:42:47 GMT
VOLUME [/var/lib/chronograf]
# Thu, 11 Jun 2026 00:42:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Jun 2026 00:42:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jun 2026 00:42:47 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:55534d9909ecd18467599b415fa2553c3106849154ae8a361a75f1a24f2a4364`  
		Last Modified: Wed, 10 Jun 2026 23:40:12 GMT  
		Size: 30.3 MB (30260255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a7bdc72d9028986df2b45952024236a0819caa65c325a9fd7bf9de39249739a`  
		Last Modified: Thu, 11 Jun 2026 00:42:57 GMT  
		Size: 5.2 MB (5241824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83b6d5f6adf14d81aae67dbcdcd6c02a70d7e356b964c04909ca7c5b79ed5c69`  
		Last Modified: Thu, 11 Jun 2026 00:42:58 GMT  
		Size: 35.0 MB (35011793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6bf247abac0bf2f179e1f2cca7d386578342bbfe29165f2a58c12bb9763e6ad`  
		Last Modified: Thu, 11 Jun 2026 00:42:57 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03fa09ba0e2903ef66131333061ca8e147d71aa0ef81d29a52e6c26dc0c9e891`  
		Last Modified: Thu, 11 Jun 2026 00:42:57 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ead191d8839dce1287ecd618fe4c0f9cb5f7e6d5948f846d1709c87bc8a8a96f`  
		Last Modified: Thu, 11 Jun 2026 00:42:58 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9.4` - unknown; unknown

```console
$ docker pull chronograf@sha256:b7892bbd95b79b2e9b046d9883e0831c1730eea41bfbba42017ca881232cdfc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3133911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ea80191cc26817177d9561dce8be523862932c2bf410fe773b1efdfe07829e0`

```dockerfile
```

-	Layers:
	-	`sha256:e5bc946ec96ec7515621519b871b5af30e6d5594444542e847e87a0ea3b0e4df`  
		Last Modified: Thu, 11 Jun 2026 00:42:57 GMT  
		Size: 3.1 MB (3118145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e82797b3fff0fad4e31be88bebbab91a4b094033f184d37402a6909d684dac5`  
		Last Modified: Thu, 11 Jun 2026 00:42:57 GMT  
		Size: 15.8 KB (15766 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.9.4` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:2dd3b604b75fc1345005187f4d027108c161dd5ec069eca28244a748ed25828e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.4 MB (63398862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d315e2a8fad8acc889f6ba99c39cbd51ef0da7b0a6e3242f316f9da213914de`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1781049600'
# Thu, 11 Jun 2026 01:30:00 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Thu, 11 Jun 2026 01:30:06 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Thu, 11 Jun 2026 01:30:06 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Thu, 11 Jun 2026 01:30:06 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Thu, 11 Jun 2026 01:30:06 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Thu, 11 Jun 2026 01:30:06 GMT
EXPOSE map[8888/tcp:{}]
# Thu, 11 Jun 2026 01:30:06 GMT
VOLUME [/var/lib/chronograf]
# Thu, 11 Jun 2026 01:30:06 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Jun 2026 01:30:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jun 2026 01:30:06 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:7ba7c49f3099e93649e55cb3558e8587e0d0458fc435dfc054641c2347c164c3`  
		Last Modified: Wed, 10 Jun 2026 23:41:03 GMT  
		Size: 25.6 MB (25552842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c20941bb3fef46667d0d5a409f5af50ede5940752aa8f393102fcf8f50ca1cfb`  
		Last Modified: Thu, 11 Jun 2026 01:30:15 GMT  
		Size: 4.5 MB (4510022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec94f538042ffbe6e7eaf08bd13fff7167d821a78e59d2e881c1f37975e4b024`  
		Last Modified: Thu, 11 Jun 2026 01:30:16 GMT  
		Size: 33.3 MB (33311608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aff2626e7077f77945ce85e013761b933b09a62c409f16a8eec49a7dc37f3cce`  
		Last Modified: Thu, 11 Jun 2026 01:30:15 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eb94ee72c6ca1d75aaf85172079d6b7ce2e7603f6858631534af0eddafa112c`  
		Last Modified: Thu, 11 Jun 2026 01:30:15 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df6fc0e520062fddde04b66698b8bdf2ef4e491eef339d04bd1434f397c363ba`  
		Last Modified: Thu, 11 Jun 2026 01:30:16 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9.4` - unknown; unknown

```console
$ docker pull chronograf@sha256:2d94b054096c58434be5263e6b40ccdd929f8f90c747b85096fd9f633dca6554
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3136260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18f6ab3887b23f0ff5d3000a41f2181507090fdace3367ede248e9b0c02a664c`

```dockerfile
```

-	Layers:
	-	`sha256:e48ee6c0ed75c15910d66f5baab4f2c94e4fbd91e8c60e7cbe7904debd065695`  
		Last Modified: Thu, 11 Jun 2026 01:30:15 GMT  
		Size: 3.1 MB (3120416 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f73e74106e44f894390b70e4fe2cd6d212d082d34afb53c66857920e1281f27a`  
		Last Modified: Thu, 11 Jun 2026 01:30:15 GMT  
		Size: 15.8 KB (15844 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.9.4` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:13a5d5516c5c08972df8e2058ad688253823a7d516fc7151c87de2cae2bc9d0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.2 MB (67182728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f42e74d6e13181f1e38f2b9ae78395bd19206349d4cbe6f6d9aabbb7959ecc4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1781049600'
# Thu, 11 Jun 2026 00:44:26 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Thu, 11 Jun 2026 00:44:31 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Thu, 11 Jun 2026 00:44:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Thu, 11 Jun 2026 00:44:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Thu, 11 Jun 2026 00:44:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Thu, 11 Jun 2026 00:44:31 GMT
EXPOSE map[8888/tcp:{}]
# Thu, 11 Jun 2026 00:44:31 GMT
VOLUME [/var/lib/chronograf]
# Thu, 11 Jun 2026 00:44:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Jun 2026 00:44:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jun 2026 00:44:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:ca483a18241c226a06a4a4afd22dc5496062254c671fa595136458fb8fcd0107`  
		Last Modified: Wed, 10 Jun 2026 23:39:58 GMT  
		Size: 28.7 MB (28746154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df19c65db679567b25fc6b51a89f0ff023c30f29903c61d91f8d09932f0a3dc1`  
		Last Modified: Thu, 11 Jun 2026 00:44:42 GMT  
		Size: 5.2 MB (5229810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f9e82af0818c57d4f43beffa14fd87f50ffa4a287a4c3ae1517efad2830a88c`  
		Last Modified: Thu, 11 Jun 2026 00:44:43 GMT  
		Size: 33.2 MB (33182372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92be84d6df7a557e61d79e4ef84158fd8d80543adef294aa6873d44207e1d0a7`  
		Last Modified: Thu, 11 Jun 2026 00:44:41 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9448ee11a9a3cdfe843f2bb8c686389731c2e97dfb8f9049256ddfa914f35700`  
		Last Modified: Thu, 11 Jun 2026 00:44:42 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0e6ab33c0bd1b32d26a88bcb4a50fb7e42c945c9403cb9f2d90674f19d08693`  
		Last Modified: Thu, 11 Jun 2026 00:44:43 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9.4` - unknown; unknown

```console
$ docker pull chronograf@sha256:45b67a28529bf52a66596f3b659bd1685bff505bf7025e7026bf13c5197f28f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3134256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f68ef40d1fe35c619e0deea588177adc79fbc4b01fc3b5f6afeba8c3ddb67406`

```dockerfile
```

-	Layers:
	-	`sha256:f974f608f04ecea1e41a00f32d27e537cb12d903a4d5dfe6769774712f99bc56`  
		Last Modified: Thu, 11 Jun 2026 00:44:42 GMT  
		Size: 3.1 MB (3118394 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f38eda398bda25bcb3de057dd0703272dbb3660477e629bc1049d2ca6b0ec1c4`  
		Last Modified: Thu, 11 Jun 2026 00:44:41 GMT  
		Size: 15.9 KB (15862 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.9.4-alpine`

```console
$ docker pull chronograf@sha256:0f80cd3823ff72714fb0be9429588b58a6cd474733e0369bc7f9181346b1d5cd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.9.4-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:f621eed42ec67e2c0af874c13b22cf7c5eca4a2f92496e0e777e83e0d0e54a18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23616085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d4f080ba353421341131d427d195e080f057481b2369a3ddd4db288e7a49570`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:26 GMT
ADD alpine-minirootfs-3.20.10-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:26 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:23:28 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 17 Apr 2026 00:23:28 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates # buildkit
# Fri, 17 Apr 2026 00:23:32 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Fri, 17 Apr 2026 00:23:32 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Fri, 17 Apr 2026 00:23:32 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 17 Apr 2026 00:23:32 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 17 Apr 2026 00:23:32 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 17 Apr 2026 00:23:32 GMT
VOLUME [/var/lib/chronograf]
# Fri, 17 Apr 2026 00:23:32 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 17 Apr 2026 00:23:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 17 Apr 2026 00:23:32 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:25f1d6b1951ac8eb3740558fe94cb83d377bdadf95fd9f98b50d2e1b96130471`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.6 MB (3630321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a16e69077797f1a90c5b8946765d6547bd0bbe62c5edf87016fc687d8691b62a`  
		Last Modified: Fri, 17 Apr 2026 00:23:39 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a582e81c7ed2cd8d0c8d79c49ea73d52bfddf13469c4d924f55b6970462df01`  
		Last Modified: Fri, 17 Apr 2026 00:23:39 GMT  
		Size: 289.1 KB (289074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaea6127a47f8ad745d11f7e8ea7511652ab602293817f95bee9cac7032fc393`  
		Last Modified: Fri, 17 Apr 2026 00:23:39 GMT  
		Size: 19.7 MB (19672041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:782461697da8106fc90296b3ce4a6a407db932533ecd9a4da24a10753acdcf1e`  
		Last Modified: Fri, 17 Apr 2026 00:23:39 GMT  
		Size: 12.2 KB (12237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e74b1d522539dce72171cebaa3d6dd0ca9ca821e4a34e4b76dc19daa0169a5c3`  
		Last Modified: Fri, 17 Apr 2026 00:23:40 GMT  
		Size: 11.9 KB (11896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce8f5e2ebfd8736864ace9d37094fa3ee04d93d2ae268e430ca56f87eec508a5`  
		Last Modified: Fri, 17 Apr 2026 00:23:40 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9.4-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:4be611f408b68b71f2ce6e27bd942207676513556d3d2d9ec7df73b913fb49b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.7 KB (249732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8b7b7e44d247f14c51737c4557d3e8bdc7e3cc786d83a99199fb64c7df6355c`

```dockerfile
```

-	Layers:
	-	`sha256:6c6b091fcc28e6afcad2a5fe2faed4c1dcff63c11868d95adf1b2056b7bbcae1`  
		Last Modified: Fri, 17 Apr 2026 00:23:39 GMT  
		Size: 232.9 KB (232866 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d10cb23e42c41cf8502d564e4146e704991853b11b9b54a94f89af55f1264769`  
		Last Modified: Fri, 17 Apr 2026 00:23:39 GMT  
		Size: 16.9 KB (16866 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:alpine`

```console
$ docker pull chronograf@sha256:3a4d1bdde45637be9b012855ab2ecf9847c9bca2629e5895ceff0f08525cd1ba
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:52a00a974fa31ab104f5615656f1f1ba19124d9dae74d1e3e19095da738ba4cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62242533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3562034250a9e0cf4501b816388ce00db408d02585ac8df9a5f1c9eef9387bd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:21 GMT
ADD alpine-minirootfs-3.22.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:21 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:56:11 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 22 Jun 2026 19:56:11 GMT
RUN apk add --no-cache ca-certificates setpriv &&     update-ca-certificates # buildkit
# Mon, 22 Jun 2026 19:56:16 GMT
ENV CHRONOGRAF_VERSION=1.11.3
# Mon, 22 Jun 2026 19:56:16 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/usr/bin/* &&     cp -a /usr/src/chronograf-*/usr/bin/* /usr/bin &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S chronograf &&     adduser -S chronograf -G chronograf &&     mkdir -m 0750 -p /var/lib/chronograf &&     chown chronograf:chronograf /var/lib/chronograf # buildkit
# Mon, 22 Jun 2026 19:56:16 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 22 Jun 2026 19:56:16 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 22 Jun 2026 19:56:16 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 22 Jun 2026 19:56:16 GMT
VOLUME [/var/lib/chronograf]
# Mon, 22 Jun 2026 19:56:16 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 22 Jun 2026 19:56:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Jun 2026 19:56:16 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:f7ee36c9aa34bbb665f975c76e5c0d1607f0674b94c84cfb0061f87006ea5d10`  
		Last Modified: Mon, 22 Jun 2026 09:11:44 GMT  
		Size: 3.8 MB (3787595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5117c3486ea43e29efca00448cabc535b8f239d757c2ea33ef0320285384ab97`  
		Last Modified: Mon, 22 Jun 2026 19:56:22 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73c138ad4109725f9ac144c7b23085967f20ab7006fd27272598882e140227af`  
		Last Modified: Mon, 22 Jun 2026 19:56:23 GMT  
		Size: 268.0 KB (268025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43c7d0596ef7237fc88fb03d77af3d61b002a1e42ded225a97f9fc69ee2fe95d`  
		Last Modified: Mon, 22 Jun 2026 19:56:30 GMT  
		Size: 58.2 MB (58162177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:881dc26ef020f0cad884e72944ebec73a1f795973e8bfb6c6db1e41060f44516`  
		Last Modified: Mon, 22 Jun 2026 19:56:28 GMT  
		Size: 12.2 KB (12240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0292f8295b205f521c6f751540b266d56de9079017576ebe9221ceff52b54b42`  
		Last Modified: Mon, 22 Jun 2026 19:56:28 GMT  
		Size: 11.9 KB (11901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c48ef1b877e834580c226ecf1161f71b15017d2168d2f2546ee3982dd9be936a`  
		Last Modified: Mon, 22 Jun 2026 19:56:28 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:53d0c74f55399512e8bcbaf8564c4bdef51e154b5945714c13c0cf04a9fd1873
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.2 KB (270191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43529a8845f8039709e8625c631ae8596244bc3cb3a04816f708e98ea86e12e4`

```dockerfile
```

-	Layers:
	-	`sha256:240b9e5d786fcf925327de71a60eb8944708565e23237bec28592aba486cbeee`  
		Last Modified: Mon, 22 Jun 2026 19:56:28 GMT  
		Size: 252.4 KB (252427 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b290ab107110c261f7aeca24b0147ea4138218fee2d23ddf55b64e55f42ae82c`  
		Last Modified: Mon, 22 Jun 2026 19:56:28 GMT  
		Size: 17.8 KB (17764 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:latest`

```console
$ docker pull chronograf@sha256:2aa9fb24f733b4d04e164d25f5ef96980c3b581ddab5c50857d1fdb42d222089
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `chronograf:latest` - linux; amd64

```console
$ docker pull chronograf@sha256:73202e652dda47453c6e05e29ca9be91761dcc92f64682de2e149a3d0a622a36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.3 MB (96342670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27932b95b4e46a21c3c4b00e9535bbe9d7155a6a5128abdac0e17faac5c5c816`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:42:55 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Thu, 11 Jun 2026 00:43:02 GMT
ENV CHRONOGRAF_VERSION=1.11.3
# Thu, 11 Jun 2026 00:43:02 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Thu, 11 Jun 2026 00:43:02 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Thu, 11 Jun 2026 00:43:02 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Thu, 11 Jun 2026 00:43:02 GMT
EXPOSE map[8888/tcp:{}]
# Thu, 11 Jun 2026 00:43:02 GMT
VOLUME [/var/lib/chronograf]
# Thu, 11 Jun 2026 00:43:02 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Jun 2026 00:43:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jun 2026 00:43:02 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:b9136609bef0128191aa157637b98dd7b98e52154ca60c18258d65957a01c6d0`  
		Last Modified: Wed, 10 Jun 2026 23:39:54 GMT  
		Size: 28.2 MB (28237624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:556c9fe7644e1166887620855e94c2fba32d97d5e3ed4df537f06c1884a7f0ae`  
		Last Modified: Thu, 11 Jun 2026 00:43:15 GMT  
		Size: 7.9 MB (7883267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b55cf3f7752999b38e3d9223912ce753e63b747ba0ca49f8df5e319c088063e9`  
		Last Modified: Thu, 11 Jun 2026 00:43:16 GMT  
		Size: 60.2 MB (60197307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5769e0d1dcfbaa03829bf62a9018e38189487c8fe5cde7c33ecf939c2b143f7e`  
		Last Modified: Thu, 11 Jun 2026 00:43:15 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e438f602a3cd637900418a3cae8b6eb964b101379fb8aa88f21114895f23481`  
		Last Modified: Thu, 11 Jun 2026 00:43:14 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35b16275212f52100b6eafaf66aa0d7343a79c7ce9ce1ca94ef1ea4dd3aba17d`  
		Last Modified: Thu, 11 Jun 2026 00:43:16 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:2c377acca3100b8eded8237f5294e94e498c9d60115575d43098702c544aab82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2889823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07de8db60e77546e14d4ee2975da7c7da016d1f475ba6cdc862591a303a9a83e`

```dockerfile
```

-	Layers:
	-	`sha256:2625568072a9dd1c4abcd0c7a987dab62a3e6c1f9f0afcb55d1ca787025eada8`  
		Last Modified: Thu, 11 Jun 2026 00:43:15 GMT  
		Size: 2.9 MB (2873738 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e92aee71ca4c730a54e0d2b4d449e648529f3c9cf1d08c370c6c63ffc0cf073`  
		Last Modified: Thu, 11 Jun 2026 00:43:15 GMT  
		Size: 16.1 KB (16085 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:latest` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:7f6ba8a05e8752787341b7fe2a6a74810b06aa9fa70a1a0228f775cc695b037a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76798073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:930d1c377ac04e3da986523b9e03970d9aff20f8036670f211d374ae5e6e562c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 02:04:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 07 Apr 2026 02:04:39 GMT
ENV CHRONOGRAF_VERSION=1.10.9
# Tue, 07 Apr 2026 02:04:39 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 07 Apr 2026 02:04:39 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 07 Apr 2026 02:04:39 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 07 Apr 2026 02:04:39 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 07 Apr 2026 02:04:39 GMT
VOLUME [/var/lib/chronograf]
# Tue, 07 Apr 2026 02:04:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 07 Apr 2026 02:04:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Apr 2026 02:04:39 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:dabf2c04988ff47a9777c2e6aee85c1e347525704928c5c1a366fae1fb63fea2`  
		Last Modified: Tue, 07 Apr 2026 00:58:55 GMT  
		Size: 23.9 MB (23941461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bde4224141eb326416434e57e6985960fa0299c171636ec51c978d7483ded221`  
		Last Modified: Tue, 07 Apr 2026 02:04:50 GMT  
		Size: 6.5 MB (6512130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39644797429280d1790a41b83be262964fe685b66a13098f85a2830ef136af23`  
		Last Modified: Tue, 07 Apr 2026 02:04:51 GMT  
		Size: 46.3 MB (46320009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a038716dc519bd0d53565ee9d170bb27389cee982f799ed02c5b30bb400da63b`  
		Last Modified: Tue, 07 Apr 2026 02:04:49 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2857e0024941e8431e0d2e7288ff873bb60af2b99250a6c109fb700e616232c`  
		Last Modified: Tue, 07 Apr 2026 02:04:49 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ac7ccabd4f0e669d232e23f27536a4797faec571f1d5b385e8d37e9543ad1d4`  
		Last Modified: Tue, 07 Apr 2026 02:04:50 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:d033ac4c98bc3deb3c46315bff42913e431c32321890ec7914cd6b43bf0a4454
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2874197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a769173f691e7dbe1bbac685b1b6d2cf8af5e40c11a7536386e603ca5e558e45`

```dockerfile
```

-	Layers:
	-	`sha256:dff92a3ce28b58e918bb8a1b393141f0d15f0a7436d538d1b53bafdf3cd2f3f0`  
		Last Modified: Tue, 07 Apr 2026 02:04:49 GMT  
		Size: 2.9 MB (2858027 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29723eb32c4a4046b83b01b8e97bd5b93cfc334f24c3dcc9145d178038a36230`  
		Last Modified: Tue, 07 Apr 2026 02:04:49 GMT  
		Size: 16.2 KB (16170 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:latest` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:366675e696db69e613db19076980c8908e9b58729a1847e6749ffe90c20dab8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.1 MB (93055462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:459b3796796fdfea3d602ce56fab1cc2c29954072f40d70adc290142e4fb3f8a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:44:38 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Thu, 11 Jun 2026 00:44:47 GMT
ENV CHRONOGRAF_VERSION=1.11.3
# Thu, 11 Jun 2026 00:44:47 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Thu, 11 Jun 2026 00:44:47 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Thu, 11 Jun 2026 00:44:47 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Thu, 11 Jun 2026 00:44:47 GMT
EXPOSE map[8888/tcp:{}]
# Thu, 11 Jun 2026 00:44:47 GMT
VOLUME [/var/lib/chronograf]
# Thu, 11 Jun 2026 00:44:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Jun 2026 00:44:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jun 2026 00:44:47 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:402614bd39aaec1e4bdcf25aa67f88588fc8d93997a2551c4e130e6ed2b06c7a`  
		Last Modified: Wed, 10 Jun 2026 23:39:57 GMT  
		Size: 28.1 MB (28122307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cbdd8fdc217506b94f451fe694a7434259077980dbfce32d678a110b1d5a084`  
		Last Modified: Thu, 11 Jun 2026 00:45:01 GMT  
		Size: 7.7 MB (7699815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8d99986976f45e221d9b9536bb7d61740629e2e34f15c8c96d9f4b700bff729`  
		Last Modified: Thu, 11 Jun 2026 00:45:02 GMT  
		Size: 57.2 MB (57208871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:694ce58a5f420870f543a6533816a87c9081c6d337adb50dc9b0fe82bec5ec9d`  
		Last Modified: Thu, 11 Jun 2026 00:45:00 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a236533c741fb74910832ada4193e1b28ee7b4538e09f17c736fc033514e8c51`  
		Last Modified: Thu, 11 Jun 2026 00:45:01 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08405dd5bfe3886ba00084d0d4013c2b5840b2fea056cdcea79f498c5bcd2084`  
		Last Modified: Thu, 11 Jun 2026 00:45:02 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:070e47966d05c2d6ad9490421a9ea383cd4c75362b29b8a8a4dc8548fd72f921
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2889144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40398e85b3e847b5bc169b9a9120493fbe744a1c8ec58c0b8bc92cc77725a6bf`

```dockerfile
```

-	Layers:
	-	`sha256:4cc86ee46eff59029c08f7a731845be8bf30156058866c32b2ae52c16c96560b`  
		Last Modified: Thu, 11 Jun 2026 00:45:01 GMT  
		Size: 2.9 MB (2872952 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06c6deb7e17d185253c508ce914f5f9b2c1c20fb44f7b9fa7fbb5528837f1745`  
		Last Modified: Thu, 11 Jun 2026 00:45:00 GMT  
		Size: 16.2 KB (16192 bytes)  
		MIME: application/vnd.in-toto+json
