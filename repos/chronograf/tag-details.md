<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `chronograf`

-	[`chronograf:1.10`](#chronograf110)
-	[`chronograf:1.10-alpine`](#chronograf110-alpine)
-	[`chronograf:1.10.8`](#chronograf1108)
-	[`chronograf:1.10.8-alpine`](#chronograf1108-alpine)
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
$ docker pull chronograf@sha256:4f4e40fdf0e855d127591f1e9900ff2d0ceecc52925e9d8b6af100491356bbc2
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
$ docker pull chronograf@sha256:d0b735de0338681ab1deeb206f4367d66ad016b4f0aa8aa641a7f4bf9550201d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.4 MB (85408171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfe6e45e8672fa4255607fcb8f990c8d49a27b82d764ed7dc22124d1622ff068`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 15 Aug 2025 14:37:23 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1759104000'
# Fri, 15 Aug 2025 14:37:23 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENV CHRONOGRAF_VERSION=1.10.8
# Fri, 15 Aug 2025 14:37:23 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 15 Aug 2025 14:37:23 GMT
VOLUME [/var/lib/chronograf]
# Fri, 15 Aug 2025 14:37:23 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:5c32499ab806884c5725c705c2bf528662d034ed99de13d3205309e0d9ef0375`  
		Last Modified: Mon, 29 Sep 2025 23:34:35 GMT  
		Size: 28.2 MB (28228336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c565502243bfc584c19aa42478e3b6ffd360f0aa9511965b5a8c85e62976b99`  
		Last Modified: Tue, 30 Sep 2025 21:38:30 GMT  
		Size: 7.9 MB (7878758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d99c8246fc7c45a2eda09b31831a752340b5f7f2306f83c8b885569de570b154`  
		Last Modified: Tue, 30 Sep 2025 21:38:32 GMT  
		Size: 49.3 MB (49276613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12575b13123c97743e1601aea6b620470cd8c3e25b4cde80494b99d736ede41b`  
		Last Modified: Tue, 30 Sep 2025 01:02:59 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17cb7667e402714079cf20570799096a3d51e8e68e4c74ef2451a835fa43e42a`  
		Last Modified: Tue, 30 Sep 2025 01:02:59 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4a89b8ff038b82766c18e9de2d8873fdc5ee1100b5e99b593dad8e5cfa57911`  
		Last Modified: Tue, 30 Sep 2025 01:02:59 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:fd59189507488845ebea82e9b86c5c6a308f9c8ced9bd6b24c63561578ab0d0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2870202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3314e1696b23a57f0915083301ff00dbe939b8a9e64db79ed29f6aceb67c888`

```dockerfile
```

-	Layers:
	-	`sha256:bb040956c6bd766a36591d90eb254901d9d8f838f977e2a2644e3b12755a2b21`  
		Last Modified: Tue, 30 Sep 2025 21:38:20 GMT  
		Size: 2.9 MB (2854074 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00d495b61186223ff2af947e470fe001315b7ff26a16ace52dc8299d313350f0`  
		Last Modified: Tue, 30 Sep 2025 21:38:21 GMT  
		Size: 16.1 KB (16128 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.10` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:f189a29427f97eecc7768bca139276270349aa7d98b57e98772bf56fc190d34a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76088312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36a94564436fe34f1c742b4b3a1aa79316130308430cd2d43d4ad6e47b3b2895`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 15 Aug 2025 14:37:23 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1757289600'
# Fri, 15 Aug 2025 14:37:23 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENV CHRONOGRAF_VERSION=1.10.8
# Fri, 15 Aug 2025 14:37:23 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 15 Aug 2025 14:37:23 GMT
VOLUME [/var/lib/chronograf]
# Fri, 15 Aug 2025 14:37:23 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:e747f8ef7f1d9a41c99bfb53889f7b8de3504300740a326627fc7522904708cc`  
		Last Modified: Mon, 08 Sep 2025 21:14:21 GMT  
		Size: 23.9 MB (23933904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dec635ab1c380e6e730c672c038827bb3e867453884ab704fea74982ba82e1d`  
		Last Modified: Mon, 08 Sep 2025 22:53:38 GMT  
		Size: 6.5 MB (6508082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:441abcfc8919aa192be1da5f5617adbba057a764b0e352a29f1f1d512effca70`  
		Last Modified: Mon, 08 Sep 2025 22:53:38 GMT  
		Size: 45.6 MB (45621861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb5085ff402d82b73039a7434cc3d4e91a50deb09fff90fd4bd998229319fc26`  
		Last Modified: Mon, 08 Sep 2025 22:38:28 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e95b01abe85ff5bbb5cc08ff120db75e8d1c3b7b81d8e159da1586a37018f818`  
		Last Modified: Mon, 08 Sep 2025 22:38:32 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf87c54eae35aecca65e9361087715fab6d3c24bba6083f6f7089cec3f040573`  
		Last Modified: Mon, 08 Sep 2025 22:38:35 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:14687783dfad06fbcc1f3a5c0b4341f5808e9c0a24124f5050b183891b850211
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2872584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c54263a6d7bf00388a84cc3a87e88753a50cb7fa75d458174d929780824bc309`

```dockerfile
```

-	Layers:
	-	`sha256:bdb5efca6a366afce6d4aff087f1ad2c73d98d6d29f750e3e1df5aff87a5b9a4`  
		Last Modified: Tue, 09 Sep 2025 00:38:27 GMT  
		Size: 2.9 MB (2856371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4eea43490b007b5564ee72dd410bc48fa888d26c7382c13b9819305dae04d1af`  
		Last Modified: Tue, 09 Sep 2025 00:38:28 GMT  
		Size: 16.2 KB (16213 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.10` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:66d488bf0021b438816e299b886fbe5b07fb07cafda79e587129fb90b99fe1cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.9 MB (82885221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a9aabbff50fd92c964ac8504015912d94aff0605cae5e0d0ad9ed3efa04183f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 15 Aug 2025 14:37:23 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1759104000'
# Fri, 15 Aug 2025 14:37:23 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENV CHRONOGRAF_VERSION=1.10.8
# Fri, 15 Aug 2025 14:37:23 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 15 Aug 2025 14:37:23 GMT
VOLUME [/var/lib/chronograf]
# Fri, 15 Aug 2025 14:37:23 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:f4e51325a7cb57cd9ae67bd9540483838b96bf7c9b0bf18205d9d30819e9ca38`  
		Last Modified: Mon, 29 Sep 2025 23:34:17 GMT  
		Size: 28.1 MB (28102145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddb9beba0102cb8a016357eaaaab7036f79df6eb1af669946d5ccb3bb523757a`  
		Last Modified: Tue, 30 Sep 2025 00:15:10 GMT  
		Size: 7.7 MB (7691801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b79c2d997f11ab4e545898b7661ab47c8605c718eb81019294ffb2306a52e72`  
		Last Modified: Tue, 30 Sep 2025 00:15:29 GMT  
		Size: 47.1 MB (47066804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d8bdc8362426bc7a0b2c8c96df4436b4eeffcbadc60d6eddfb62d3b3daa3105`  
		Last Modified: Tue, 30 Sep 2025 00:15:11 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33806231fa81aa323170575a5229bf1cba922a82f2a5c1ff40e2cd64948a3d16`  
		Last Modified: Tue, 30 Sep 2025 00:15:11 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3497d1bd60a46456aec7c35fb956f57b6b433ba81f8249c3467882b40eea9664`  
		Last Modified: Tue, 30 Sep 2025 00:15:14 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:e386baa1528d15451d2e6312153a556a7eb1283fd44e7e25c61422eebf89ba2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2870581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ef63d0ec60521a6cc1e8c174d6de979d19937a2fe2777b143e1eb630b090b94`

```dockerfile
```

-	Layers:
	-	`sha256:e8d775b5048f14c0c446e01d800fa9b9e087615e5f69f74fc49e22c5645fcf1a`  
		Last Modified: Wed, 01 Oct 2025 12:38:24 GMT  
		Size: 2.9 MB (2854347 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b365ac64465a8ae692b8dce815e49856ade9437224141f848a34efb94c20330c`  
		Last Modified: Wed, 01 Oct 2025 12:38:25 GMT  
		Size: 16.2 KB (16234 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.10-alpine`

```console
$ docker pull chronograf@sha256:1ddf470cfa125f9de7db291932845b6b1c839a17470a5edc9937520e555021fd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.10-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:313949b2dd32c7b925d8f1df1814ea49db2dfaa617a995372f7c633ddbe37571
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.7 MB (32688182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed55e91957e952193ac6c0b4c3d2348e04403644844c0eea861726392a1fe789`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
RUN apk add --no-cache ca-certificates setpriv &&     update-ca-certificates # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENV CHRONOGRAF_VERSION=1.10.8
# Fri, 15 Aug 2025 14:37:23 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S chronograf &&     adduser -S chronograf -G chronograf &&     mkdir -m 0750 -p /var/lib/chronograf &&     chown chronograf:chronograf /var/lib/chronograf # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 15 Aug 2025 14:37:23 GMT
VOLUME [/var/lib/chronograf]
# Fri, 15 Aug 2025 14:37:23 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fac5852aab88158a636f5c62b8372eeb08344812accaa647d93267bb5aabbe90`  
		Last Modified: Tue, 19 Aug 2025 16:45:51 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f629721feb48667f4ade9b4f3439178d5683262876745a0dbe2a1a200cf55024`  
		Last Modified: Tue, 19 Aug 2025 16:45:52 GMT  
		Size: 305.9 KB (305880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbe170c0d482899a4f59077af1eb298089e38f7895c3a04eb0896631e83d8247`  
		Last Modified: Tue, 19 Aug 2025 16:45:56 GMT  
		Size: 28.6 MB (28557892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c8a90fb1888f50f9757485fd13c0739accd286933df741c386b75b66c8dcdbe`  
		Last Modified: Tue, 19 Aug 2025 16:45:52 GMT  
		Size: 12.2 KB (12236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faa33ce60529ed7913cfa394491c65481d4d49d33259e1e59fc23f92cee6e032`  
		Last Modified: Tue, 19 Aug 2025 16:45:52 GMT  
		Size: 11.9 KB (11892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:706de7adfac6567def5ce908056a9dc4c7d01529aaff53726d8f2feeceed04ef`  
		Last Modified: Tue, 19 Aug 2025 16:45:52 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:7aee1aa708c95df18c4c5fccc05eb80166744df023669f9774715fa5386cf8d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.6 KB (265625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a231bfc9063c7a6fbb1fae07d3082eb216852349d0654aeb6a0c122482cb3a92`

```dockerfile
```

-	Layers:
	-	`sha256:f269451dd549f671f7ea78b61bd711e09bfc0f478b96d30dcd4ccf7ac0eea26c`  
		Last Modified: Tue, 19 Aug 2025 18:38:30 GMT  
		Size: 247.8 KB (247770 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a6b2fd6d2f7b798e331a71fe469e5c57487bacdc8e5532bc2af0acb4733f74a`  
		Last Modified: Tue, 19 Aug 2025 18:38:30 GMT  
		Size: 17.9 KB (17855 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.10.8`

```console
$ docker pull chronograf@sha256:4f4e40fdf0e855d127591f1e9900ff2d0ceecc52925e9d8b6af100491356bbc2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `chronograf:1.10.8` - linux; amd64

```console
$ docker pull chronograf@sha256:d0b735de0338681ab1deeb206f4367d66ad016b4f0aa8aa641a7f4bf9550201d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.4 MB (85408171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfe6e45e8672fa4255607fcb8f990c8d49a27b82d764ed7dc22124d1622ff068`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 15 Aug 2025 14:37:23 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1759104000'
# Fri, 15 Aug 2025 14:37:23 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENV CHRONOGRAF_VERSION=1.10.8
# Fri, 15 Aug 2025 14:37:23 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 15 Aug 2025 14:37:23 GMT
VOLUME [/var/lib/chronograf]
# Fri, 15 Aug 2025 14:37:23 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:5c32499ab806884c5725c705c2bf528662d034ed99de13d3205309e0d9ef0375`  
		Last Modified: Mon, 29 Sep 2025 23:34:35 GMT  
		Size: 28.2 MB (28228336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c565502243bfc584c19aa42478e3b6ffd360f0aa9511965b5a8c85e62976b99`  
		Last Modified: Tue, 30 Sep 2025 21:38:30 GMT  
		Size: 7.9 MB (7878758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d99c8246fc7c45a2eda09b31831a752340b5f7f2306f83c8b885569de570b154`  
		Last Modified: Tue, 30 Sep 2025 21:38:32 GMT  
		Size: 49.3 MB (49276613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12575b13123c97743e1601aea6b620470cd8c3e25b4cde80494b99d736ede41b`  
		Last Modified: Tue, 30 Sep 2025 01:02:59 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17cb7667e402714079cf20570799096a3d51e8e68e4c74ef2451a835fa43e42a`  
		Last Modified: Tue, 30 Sep 2025 01:02:59 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4a89b8ff038b82766c18e9de2d8873fdc5ee1100b5e99b593dad8e5cfa57911`  
		Last Modified: Tue, 30 Sep 2025 01:02:59 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10.8` - unknown; unknown

```console
$ docker pull chronograf@sha256:fd59189507488845ebea82e9b86c5c6a308f9c8ced9bd6b24c63561578ab0d0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2870202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3314e1696b23a57f0915083301ff00dbe939b8a9e64db79ed29f6aceb67c888`

```dockerfile
```

-	Layers:
	-	`sha256:bb040956c6bd766a36591d90eb254901d9d8f838f977e2a2644e3b12755a2b21`  
		Last Modified: Tue, 30 Sep 2025 21:38:20 GMT  
		Size: 2.9 MB (2854074 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00d495b61186223ff2af947e470fe001315b7ff26a16ace52dc8299d313350f0`  
		Last Modified: Tue, 30 Sep 2025 21:38:21 GMT  
		Size: 16.1 KB (16128 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.10.8` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:f189a29427f97eecc7768bca139276270349aa7d98b57e98772bf56fc190d34a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76088312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36a94564436fe34f1c742b4b3a1aa79316130308430cd2d43d4ad6e47b3b2895`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 15 Aug 2025 14:37:23 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1757289600'
# Fri, 15 Aug 2025 14:37:23 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENV CHRONOGRAF_VERSION=1.10.8
# Fri, 15 Aug 2025 14:37:23 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 15 Aug 2025 14:37:23 GMT
VOLUME [/var/lib/chronograf]
# Fri, 15 Aug 2025 14:37:23 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:e747f8ef7f1d9a41c99bfb53889f7b8de3504300740a326627fc7522904708cc`  
		Last Modified: Mon, 08 Sep 2025 21:14:21 GMT  
		Size: 23.9 MB (23933904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dec635ab1c380e6e730c672c038827bb3e867453884ab704fea74982ba82e1d`  
		Last Modified: Mon, 08 Sep 2025 22:53:38 GMT  
		Size: 6.5 MB (6508082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:441abcfc8919aa192be1da5f5617adbba057a764b0e352a29f1f1d512effca70`  
		Last Modified: Mon, 08 Sep 2025 22:53:38 GMT  
		Size: 45.6 MB (45621861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb5085ff402d82b73039a7434cc3d4e91a50deb09fff90fd4bd998229319fc26`  
		Last Modified: Mon, 08 Sep 2025 22:38:28 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e95b01abe85ff5bbb5cc08ff120db75e8d1c3b7b81d8e159da1586a37018f818`  
		Last Modified: Mon, 08 Sep 2025 22:38:32 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf87c54eae35aecca65e9361087715fab6d3c24bba6083f6f7089cec3f040573`  
		Last Modified: Mon, 08 Sep 2025 22:38:35 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10.8` - unknown; unknown

```console
$ docker pull chronograf@sha256:14687783dfad06fbcc1f3a5c0b4341f5808e9c0a24124f5050b183891b850211
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2872584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c54263a6d7bf00388a84cc3a87e88753a50cb7fa75d458174d929780824bc309`

```dockerfile
```

-	Layers:
	-	`sha256:bdb5efca6a366afce6d4aff087f1ad2c73d98d6d29f750e3e1df5aff87a5b9a4`  
		Last Modified: Tue, 09 Sep 2025 00:38:27 GMT  
		Size: 2.9 MB (2856371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4eea43490b007b5564ee72dd410bc48fa888d26c7382c13b9819305dae04d1af`  
		Last Modified: Tue, 09 Sep 2025 00:38:28 GMT  
		Size: 16.2 KB (16213 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.10.8` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:66d488bf0021b438816e299b886fbe5b07fb07cafda79e587129fb90b99fe1cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.9 MB (82885221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a9aabbff50fd92c964ac8504015912d94aff0605cae5e0d0ad9ed3efa04183f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 15 Aug 2025 14:37:23 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1759104000'
# Fri, 15 Aug 2025 14:37:23 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENV CHRONOGRAF_VERSION=1.10.8
# Fri, 15 Aug 2025 14:37:23 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 15 Aug 2025 14:37:23 GMT
VOLUME [/var/lib/chronograf]
# Fri, 15 Aug 2025 14:37:23 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:f4e51325a7cb57cd9ae67bd9540483838b96bf7c9b0bf18205d9d30819e9ca38`  
		Last Modified: Mon, 29 Sep 2025 23:34:17 GMT  
		Size: 28.1 MB (28102145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddb9beba0102cb8a016357eaaaab7036f79df6eb1af669946d5ccb3bb523757a`  
		Last Modified: Tue, 30 Sep 2025 00:15:10 GMT  
		Size: 7.7 MB (7691801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b79c2d997f11ab4e545898b7661ab47c8605c718eb81019294ffb2306a52e72`  
		Last Modified: Tue, 30 Sep 2025 00:15:29 GMT  
		Size: 47.1 MB (47066804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d8bdc8362426bc7a0b2c8c96df4436b4eeffcbadc60d6eddfb62d3b3daa3105`  
		Last Modified: Tue, 30 Sep 2025 00:15:11 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33806231fa81aa323170575a5229bf1cba922a82f2a5c1ff40e2cd64948a3d16`  
		Last Modified: Tue, 30 Sep 2025 00:15:11 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3497d1bd60a46456aec7c35fb956f57b6b433ba81f8249c3467882b40eea9664`  
		Last Modified: Tue, 30 Sep 2025 00:15:14 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10.8` - unknown; unknown

```console
$ docker pull chronograf@sha256:e386baa1528d15451d2e6312153a556a7eb1283fd44e7e25c61422eebf89ba2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2870581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ef63d0ec60521a6cc1e8c174d6de979d19937a2fe2777b143e1eb630b090b94`

```dockerfile
```

-	Layers:
	-	`sha256:e8d775b5048f14c0c446e01d800fa9b9e087615e5f69f74fc49e22c5645fcf1a`  
		Last Modified: Wed, 01 Oct 2025 12:38:24 GMT  
		Size: 2.9 MB (2854347 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b365ac64465a8ae692b8dce815e49856ade9437224141f848a34efb94c20330c`  
		Last Modified: Wed, 01 Oct 2025 12:38:25 GMT  
		Size: 16.2 KB (16234 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.10.8-alpine`

```console
$ docker pull chronograf@sha256:1ddf470cfa125f9de7db291932845b6b1c839a17470a5edc9937520e555021fd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.10.8-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:313949b2dd32c7b925d8f1df1814ea49db2dfaa617a995372f7c633ddbe37571
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.7 MB (32688182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed55e91957e952193ac6c0b4c3d2348e04403644844c0eea861726392a1fe789`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
RUN apk add --no-cache ca-certificates setpriv &&     update-ca-certificates # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENV CHRONOGRAF_VERSION=1.10.8
# Fri, 15 Aug 2025 14:37:23 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S chronograf &&     adduser -S chronograf -G chronograf &&     mkdir -m 0750 -p /var/lib/chronograf &&     chown chronograf:chronograf /var/lib/chronograf # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 15 Aug 2025 14:37:23 GMT
VOLUME [/var/lib/chronograf]
# Fri, 15 Aug 2025 14:37:23 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fac5852aab88158a636f5c62b8372eeb08344812accaa647d93267bb5aabbe90`  
		Last Modified: Tue, 19 Aug 2025 16:45:51 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f629721feb48667f4ade9b4f3439178d5683262876745a0dbe2a1a200cf55024`  
		Last Modified: Tue, 19 Aug 2025 16:45:52 GMT  
		Size: 305.9 KB (305880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbe170c0d482899a4f59077af1eb298089e38f7895c3a04eb0896631e83d8247`  
		Last Modified: Tue, 19 Aug 2025 16:45:56 GMT  
		Size: 28.6 MB (28557892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c8a90fb1888f50f9757485fd13c0739accd286933df741c386b75b66c8dcdbe`  
		Last Modified: Tue, 19 Aug 2025 16:45:52 GMT  
		Size: 12.2 KB (12236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faa33ce60529ed7913cfa394491c65481d4d49d33259e1e59fc23f92cee6e032`  
		Last Modified: Tue, 19 Aug 2025 16:45:52 GMT  
		Size: 11.9 KB (11892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:706de7adfac6567def5ce908056a9dc4c7d01529aaff53726d8f2feeceed04ef`  
		Last Modified: Tue, 19 Aug 2025 16:45:52 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10.8-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:7aee1aa708c95df18c4c5fccc05eb80166744df023669f9774715fa5386cf8d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.6 KB (265625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a231bfc9063c7a6fbb1fae07d3082eb216852349d0654aeb6a0c122482cb3a92`

```dockerfile
```

-	Layers:
	-	`sha256:f269451dd549f671f7ea78b61bd711e09bfc0f478b96d30dcd4ccf7ac0eea26c`  
		Last Modified: Tue, 19 Aug 2025 18:38:30 GMT  
		Size: 247.8 KB (247770 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a6b2fd6d2f7b798e331a71fe469e5c57487bacdc8e5532bc2af0acb4733f74a`  
		Last Modified: Tue, 19 Aug 2025 18:38:30 GMT  
		Size: 17.9 KB (17855 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.7`

```console
$ docker pull chronograf@sha256:ec0aa61e8d1bc21434d20552e7cd479cca1cb236d1b4e9b8181ecdb93957c2b5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `chronograf:1.7` - linux; amd64

```console
$ docker pull chronograf@sha256:82a5b4495583317f926d8545d057074bab8cba391305b840e667dadcf72bac4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.2 MB (69230566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:589590643f73694123b539a00f20898fa7bc6afa9f70d80e30c8a209663075ca`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 15 Aug 2025 14:37:23 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1759104000'
# Fri, 15 Aug 2025 14:37:23 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Fri, 15 Aug 2025 14:37:23 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 15 Aug 2025 14:37:23 GMT
VOLUME [/var/lib/chronograf]
# Fri, 15 Aug 2025 14:37:23 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:4eb1dd59a73886acc6a3cc9d4c8f8e66d1fd6ba6d6195b05ce21c22b0658aab8`  
		Last Modified: Mon, 29 Sep 2025 23:35:18 GMT  
		Size: 30.3 MB (30258363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d8194d35dc8befc2bbf3fa6c0903b995aa718141f758a64a42df73a172ab8e1`  
		Last Modified: Tue, 30 Sep 2025 21:41:08 GMT  
		Size: 4.2 MB (4209313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44216c910304cc7077c5d167150708eac2d2c3b30c2b2904454966ba53b0247b`  
		Last Modified: Tue, 30 Sep 2025 21:41:09 GMT  
		Size: 34.7 MB (34738489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14d497b8cb66195fab3942ada5319619c608849e9b391b1e7f12a73ff853609a`  
		Last Modified: Tue, 30 Sep 2025 01:02:31 GMT  
		Size: 12.3 KB (12252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d383b3fd2521d55cf369ac995e8cdb630fd5afc6451ccf6240820ce3d50ef0a2`  
		Last Modified: Tue, 30 Sep 2025 01:02:31 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:657940c1d52d56ad3f4c54d66fc3bde9793cf1ca316063f7a01376115d9d44ee`  
		Last Modified: Tue, 30 Sep 2025 01:02:31 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7` - unknown; unknown

```console
$ docker pull chronograf@sha256:36e8f7aa2fcdbff9580ef4da33765ba1d23a8f36efebf95b8b7f843d68554bbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3064650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e0cf961572bd030e3984f6400d149315ce9bb3705001f6c2c5b3588a441aaa7`

```dockerfile
```

-	Layers:
	-	`sha256:32ea254241084fac55ec0860d362d757236d86c472bbbe0641aa574ca9779813`  
		Last Modified: Tue, 30 Sep 2025 21:38:26 GMT  
		Size: 3.0 MB (3048873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae0539ff63668b67108199b58336893000c23db2c07f7bada62a58f0468b8b84`  
		Last Modified: Tue, 30 Sep 2025 21:38:27 GMT  
		Size: 15.8 KB (15777 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.7` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:c8de0ca4be67c6d96e98258db039b6b87d13c4dd6ceec0b4d34c32102d8e2adb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62178795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca32626d9f7b33510ca6c0d0b4775c4db619fc63dd91057f87f1b461a1b46ab7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 15 Aug 2025 14:37:23 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1757289600'
# Fri, 15 Aug 2025 14:37:23 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Fri, 15 Aug 2025 14:37:23 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 15 Aug 2025 14:37:23 GMT
VOLUME [/var/lib/chronograf]
# Fri, 15 Aug 2025 14:37:23 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:6060ada35559867e583ae59d61cbfce25e84350e0631f50a795fd6d2b2c5651b`  
		Last Modified: Mon, 08 Sep 2025 21:24:07 GMT  
		Size: 25.5 MB (25544079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1beeb819e46f0fbbb48345f84bc87e88f452d2356dbde363acd9b9a5d0faddff`  
		Last Modified: Mon, 08 Sep 2025 23:20:35 GMT  
		Size: 3.5 MB (3511576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b07b514ce995e655c9d44b7d78e3d0bc46e6e566fcbd8f59c7ba88a0efbb8db7`  
		Last Modified: Thu, 11 Sep 2025 07:02:21 GMT  
		Size: 33.1 MB (33098757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:749ee37b330fa9dd2cd69649caafbfc613e73851cbfcc869e287f35a9d4e15b8`  
		Last Modified: Mon, 08 Sep 2025 23:20:08 GMT  
		Size: 12.2 KB (12243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ace6162bf2f3707a2703ee05300487c3cbcdef541805e6b779b0fd549bb777d2`  
		Last Modified: Mon, 08 Sep 2025 23:20:07 GMT  
		Size: 11.9 KB (11901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2a526f9c2c9a24554ec58e22312ae557596ff99243c4974ac439f74c2677260`  
		Last Modified: Mon, 08 Sep 2025 23:20:10 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7` - unknown; unknown

```console
$ docker pull chronograf@sha256:6c18743b9abc61616dea63fa13b3ff04f470a7475785ae4b8f01feed214763e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3066998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:430ce237b329d0e84a4f1822083bc25a33090c8d83d336b6ed33580ea8158e30`

```dockerfile
```

-	Layers:
	-	`sha256:7152f537b106593f1b8f0e84cc9e33c82e1fa7b319427222bcf1696fa2f9496b`  
		Last Modified: Tue, 09 Sep 2025 00:38:38 GMT  
		Size: 3.1 MB (3051144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00663a5b0c70ef8e1e9aa81c9813cf6cfdcab8fb41aa9b5a9efc790cbdb8f838`  
		Last Modified: Tue, 09 Sep 2025 00:38:39 GMT  
		Size: 15.9 KB (15854 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.7` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:e1e2bec5870b0563403e54e85e5eddcfe63fb83a7069d50a528adc445461c9f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66221533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7267a606e21b88aeeecfdf37140cd229b2ae51c76e005ef0b7f6f4f7c701020b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 15 Aug 2025 14:37:23 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1759104000'
# Fri, 15 Aug 2025 14:37:23 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Fri, 15 Aug 2025 14:37:23 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 15 Aug 2025 14:37:23 GMT
VOLUME [/var/lib/chronograf]
# Fri, 15 Aug 2025 14:37:23 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:93b0b88e50eb7468103e583a7be2e8ee3fe5f86e6c74df4baca40a3685b5eee1`  
		Last Modified: Mon, 29 Sep 2025 23:34:34 GMT  
		Size: 28.7 MB (28748427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96b9a6ea06149c95a8cea79b4bfb8b6c3c1a224f9892f61b03d39a64b72954bc`  
		Last Modified: Tue, 30 Sep 2025 00:14:26 GMT  
		Size: 4.2 MB (4210625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16b3a34ee1250709ecda0b702e5b1bb6630d67c44a79a856f97f4528388eb991`  
		Last Modified: Tue, 30 Sep 2025 00:14:28 GMT  
		Size: 33.2 MB (33238101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ad3e6398ba302e2a73375169f95196ef41e78cb273241b7f7bc589b42df83f`  
		Last Modified: Tue, 30 Sep 2025 00:14:25 GMT  
		Size: 12.2 KB (12243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07eef01bd7ed05794b0af4148ee344e0b1e205b09baf1180ace4347c67745b4c`  
		Last Modified: Tue, 30 Sep 2025 00:14:25 GMT  
		Size: 11.9 KB (11898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a36a3d5a0a77d5e6b24ded673c2f0fdee528add59b23533390db92859ca00d86`  
		Last Modified: Tue, 30 Sep 2025 00:14:25 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7` - unknown; unknown

```console
$ docker pull chronograf@sha256:fcf42dd60779b32e2ccc2ec9c7cffea46b551b9581f1604e8a6b1596ea513dce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3064994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f28b6dc7700ba1d3e35ecf2e5cbc17e4b69c5af81cb8860ad310f9b87b7b1ad6`

```dockerfile
```

-	Layers:
	-	`sha256:5e5c29d2aba79d310d333ff102ca7b2207de7016aab76a36a6d55c3e23ba0a72`  
		Last Modified: Wed, 01 Oct 2025 12:38:32 GMT  
		Size: 3.0 MB (3049122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c119e56197eb4f26acb20122004c9a70615536baddcc512b92ceb973caa74cc`  
		Last Modified: Wed, 01 Oct 2025 12:38:33 GMT  
		Size: 15.9 KB (15872 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.7-alpine`

```console
$ docker pull chronograf@sha256:b90bcafe5219412d35868276c85f4d80c7e18d54618cbfab57ec675efd405157
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.7-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:1d548db4842ce84a24b34df3e0196892ebe88d9caa15ece3769606d555b164f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.5 MB (23483441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76bbd529f93384e04f37ec3d00e1cc8a9aaf79c52c00a4473e3cb2f63f70f6da`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 16 Apr 2025 11:55:02 GMT
ADD alpine-minirootfs-3.20.7-x86_64.tar.gz / # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
CMD ["/bin/sh"]
# Wed, 16 Apr 2025 11:55:02 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Wed, 16 Apr 2025 11:55:02 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
EXPOSE map[8888/tcp:{}]
# Wed, 16 Apr 2025 11:55:02 GMT
VOLUME [/var/lib/chronograf]
# Wed, 16 Apr 2025 11:55:02 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 16 Apr 2025 11:55:02 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:01d036902a3ca86e8793073c8094cba44d83a38953a489ac0641f3de017fe2d2`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3620477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22a2fc7c1c74da72a42afda946fafe7f5ce9fc167d848adac804aba9aaa35f71`  
		Last Modified: Tue, 15 Jul 2025 19:25:42 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:425d0be71ea0a5643b2bb6127de22d2e9db43c78894f143836b1b4b1e6a2590f`  
		Last Modified: Tue, 15 Jul 2025 19:25:42 GMT  
		Size: 282.1 KB (282050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:629ea2a89dc40367c50e991e4d35e516f7346f328300d769802b5fcdcf90f141`  
		Last Modified: Tue, 15 Jul 2025 19:25:46 GMT  
		Size: 19.6 MB (19556267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b523f6cc68d030e209e9a82ce3b3451828dc30ea36835538683ce58effd0364e`  
		Last Modified: Tue, 15 Jul 2025 19:25:44 GMT  
		Size: 12.2 KB (12236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b0ebca30eb1be4ea618c47b7df8edfe29ea98ee9a50e9f5ac737d4def9d43eb`  
		Last Modified: Tue, 15 Jul 2025 19:25:44 GMT  
		Size: 11.9 KB (11895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4a0c26e12214ed30329c891e237537b5f1300d0cbb3fb3373f735d7a88ad7c5`  
		Last Modified: Tue, 15 Jul 2025 19:25:43 GMT  
		Size: 237.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:657fe6fbe370582f5c02e3060e50aa260ef4337a04819df606e1f6ddef06f178
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.1 KB (186131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef1a38a41afefa7d15b684d86787bd13668e232e2bae0606c4d13c2928bb10fb`

```dockerfile
```

-	Layers:
	-	`sha256:b666ed462b0b587e4074f667fa9c57ca9514692758ebe77f7fdb7d0e2f9cf571`  
		Last Modified: Tue, 15 Jul 2025 21:38:24 GMT  
		Size: 169.2 KB (169219 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:210c85b79477d42432c1e662ca4140caf59b700dc7b0f6b9870e337bbd012561`  
		Last Modified: Tue, 15 Jul 2025 21:38:25 GMT  
		Size: 16.9 KB (16912 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.7.17`

```console
$ docker pull chronograf@sha256:ec0aa61e8d1bc21434d20552e7cd479cca1cb236d1b4e9b8181ecdb93957c2b5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `chronograf:1.7.17` - linux; amd64

```console
$ docker pull chronograf@sha256:82a5b4495583317f926d8545d057074bab8cba391305b840e667dadcf72bac4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.2 MB (69230566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:589590643f73694123b539a00f20898fa7bc6afa9f70d80e30c8a209663075ca`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 15 Aug 2025 14:37:23 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1759104000'
# Fri, 15 Aug 2025 14:37:23 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Fri, 15 Aug 2025 14:37:23 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 15 Aug 2025 14:37:23 GMT
VOLUME [/var/lib/chronograf]
# Fri, 15 Aug 2025 14:37:23 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:4eb1dd59a73886acc6a3cc9d4c8f8e66d1fd6ba6d6195b05ce21c22b0658aab8`  
		Last Modified: Mon, 29 Sep 2025 23:35:18 GMT  
		Size: 30.3 MB (30258363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d8194d35dc8befc2bbf3fa6c0903b995aa718141f758a64a42df73a172ab8e1`  
		Last Modified: Tue, 30 Sep 2025 21:41:08 GMT  
		Size: 4.2 MB (4209313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44216c910304cc7077c5d167150708eac2d2c3b30c2b2904454966ba53b0247b`  
		Last Modified: Tue, 30 Sep 2025 21:41:09 GMT  
		Size: 34.7 MB (34738489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14d497b8cb66195fab3942ada5319619c608849e9b391b1e7f12a73ff853609a`  
		Last Modified: Tue, 30 Sep 2025 01:02:31 GMT  
		Size: 12.3 KB (12252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d383b3fd2521d55cf369ac995e8cdb630fd5afc6451ccf6240820ce3d50ef0a2`  
		Last Modified: Tue, 30 Sep 2025 01:02:31 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:657940c1d52d56ad3f4c54d66fc3bde9793cf1ca316063f7a01376115d9d44ee`  
		Last Modified: Tue, 30 Sep 2025 01:02:31 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7.17` - unknown; unknown

```console
$ docker pull chronograf@sha256:36e8f7aa2fcdbff9580ef4da33765ba1d23a8f36efebf95b8b7f843d68554bbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3064650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e0cf961572bd030e3984f6400d149315ce9bb3705001f6c2c5b3588a441aaa7`

```dockerfile
```

-	Layers:
	-	`sha256:32ea254241084fac55ec0860d362d757236d86c472bbbe0641aa574ca9779813`  
		Last Modified: Tue, 30 Sep 2025 21:38:26 GMT  
		Size: 3.0 MB (3048873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae0539ff63668b67108199b58336893000c23db2c07f7bada62a58f0468b8b84`  
		Last Modified: Tue, 30 Sep 2025 21:38:27 GMT  
		Size: 15.8 KB (15777 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.7.17` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:c8de0ca4be67c6d96e98258db039b6b87d13c4dd6ceec0b4d34c32102d8e2adb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62178795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca32626d9f7b33510ca6c0d0b4775c4db619fc63dd91057f87f1b461a1b46ab7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 15 Aug 2025 14:37:23 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1757289600'
# Fri, 15 Aug 2025 14:37:23 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Fri, 15 Aug 2025 14:37:23 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 15 Aug 2025 14:37:23 GMT
VOLUME [/var/lib/chronograf]
# Fri, 15 Aug 2025 14:37:23 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:6060ada35559867e583ae59d61cbfce25e84350e0631f50a795fd6d2b2c5651b`  
		Last Modified: Mon, 08 Sep 2025 21:24:07 GMT  
		Size: 25.5 MB (25544079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1beeb819e46f0fbbb48345f84bc87e88f452d2356dbde363acd9b9a5d0faddff`  
		Last Modified: Mon, 08 Sep 2025 23:20:35 GMT  
		Size: 3.5 MB (3511576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b07b514ce995e655c9d44b7d78e3d0bc46e6e566fcbd8f59c7ba88a0efbb8db7`  
		Last Modified: Thu, 11 Sep 2025 07:02:21 GMT  
		Size: 33.1 MB (33098757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:749ee37b330fa9dd2cd69649caafbfc613e73851cbfcc869e287f35a9d4e15b8`  
		Last Modified: Mon, 08 Sep 2025 23:20:08 GMT  
		Size: 12.2 KB (12243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ace6162bf2f3707a2703ee05300487c3cbcdef541805e6b779b0fd549bb777d2`  
		Last Modified: Mon, 08 Sep 2025 23:20:07 GMT  
		Size: 11.9 KB (11901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2a526f9c2c9a24554ec58e22312ae557596ff99243c4974ac439f74c2677260`  
		Last Modified: Mon, 08 Sep 2025 23:20:10 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7.17` - unknown; unknown

```console
$ docker pull chronograf@sha256:6c18743b9abc61616dea63fa13b3ff04f470a7475785ae4b8f01feed214763e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3066998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:430ce237b329d0e84a4f1822083bc25a33090c8d83d336b6ed33580ea8158e30`

```dockerfile
```

-	Layers:
	-	`sha256:7152f537b106593f1b8f0e84cc9e33c82e1fa7b319427222bcf1696fa2f9496b`  
		Last Modified: Tue, 09 Sep 2025 00:38:38 GMT  
		Size: 3.1 MB (3051144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00663a5b0c70ef8e1e9aa81c9813cf6cfdcab8fb41aa9b5a9efc790cbdb8f838`  
		Last Modified: Tue, 09 Sep 2025 00:38:39 GMT  
		Size: 15.9 KB (15854 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.7.17` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:e1e2bec5870b0563403e54e85e5eddcfe63fb83a7069d50a528adc445461c9f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66221533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7267a606e21b88aeeecfdf37140cd229b2ae51c76e005ef0b7f6f4f7c701020b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 15 Aug 2025 14:37:23 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1759104000'
# Fri, 15 Aug 2025 14:37:23 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Fri, 15 Aug 2025 14:37:23 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 15 Aug 2025 14:37:23 GMT
VOLUME [/var/lib/chronograf]
# Fri, 15 Aug 2025 14:37:23 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:93b0b88e50eb7468103e583a7be2e8ee3fe5f86e6c74df4baca40a3685b5eee1`  
		Last Modified: Mon, 29 Sep 2025 23:34:34 GMT  
		Size: 28.7 MB (28748427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96b9a6ea06149c95a8cea79b4bfb8b6c3c1a224f9892f61b03d39a64b72954bc`  
		Last Modified: Tue, 30 Sep 2025 00:14:26 GMT  
		Size: 4.2 MB (4210625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16b3a34ee1250709ecda0b702e5b1bb6630d67c44a79a856f97f4528388eb991`  
		Last Modified: Tue, 30 Sep 2025 00:14:28 GMT  
		Size: 33.2 MB (33238101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ad3e6398ba302e2a73375169f95196ef41e78cb273241b7f7bc589b42df83f`  
		Last Modified: Tue, 30 Sep 2025 00:14:25 GMT  
		Size: 12.2 KB (12243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07eef01bd7ed05794b0af4148ee344e0b1e205b09baf1180ace4347c67745b4c`  
		Last Modified: Tue, 30 Sep 2025 00:14:25 GMT  
		Size: 11.9 KB (11898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a36a3d5a0a77d5e6b24ded673c2f0fdee528add59b23533390db92859ca00d86`  
		Last Modified: Tue, 30 Sep 2025 00:14:25 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7.17` - unknown; unknown

```console
$ docker pull chronograf@sha256:fcf42dd60779b32e2ccc2ec9c7cffea46b551b9581f1604e8a6b1596ea513dce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3064994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f28b6dc7700ba1d3e35ecf2e5cbc17e4b69c5af81cb8860ad310f9b87b7b1ad6`

```dockerfile
```

-	Layers:
	-	`sha256:5e5c29d2aba79d310d333ff102ca7b2207de7016aab76a36a6d55c3e23ba0a72`  
		Last Modified: Wed, 01 Oct 2025 12:38:32 GMT  
		Size: 3.0 MB (3049122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c119e56197eb4f26acb20122004c9a70615536baddcc512b92ceb973caa74cc`  
		Last Modified: Wed, 01 Oct 2025 12:38:33 GMT  
		Size: 15.9 KB (15872 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.7.17-alpine`

```console
$ docker pull chronograf@sha256:b90bcafe5219412d35868276c85f4d80c7e18d54618cbfab57ec675efd405157
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.7.17-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:1d548db4842ce84a24b34df3e0196892ebe88d9caa15ece3769606d555b164f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.5 MB (23483441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76bbd529f93384e04f37ec3d00e1cc8a9aaf79c52c00a4473e3cb2f63f70f6da`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 16 Apr 2025 11:55:02 GMT
ADD alpine-minirootfs-3.20.7-x86_64.tar.gz / # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
CMD ["/bin/sh"]
# Wed, 16 Apr 2025 11:55:02 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Wed, 16 Apr 2025 11:55:02 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
EXPOSE map[8888/tcp:{}]
# Wed, 16 Apr 2025 11:55:02 GMT
VOLUME [/var/lib/chronograf]
# Wed, 16 Apr 2025 11:55:02 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 16 Apr 2025 11:55:02 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:01d036902a3ca86e8793073c8094cba44d83a38953a489ac0641f3de017fe2d2`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3620477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22a2fc7c1c74da72a42afda946fafe7f5ce9fc167d848adac804aba9aaa35f71`  
		Last Modified: Tue, 15 Jul 2025 19:25:42 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:425d0be71ea0a5643b2bb6127de22d2e9db43c78894f143836b1b4b1e6a2590f`  
		Last Modified: Tue, 15 Jul 2025 19:25:42 GMT  
		Size: 282.1 KB (282050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:629ea2a89dc40367c50e991e4d35e516f7346f328300d769802b5fcdcf90f141`  
		Last Modified: Tue, 15 Jul 2025 19:25:46 GMT  
		Size: 19.6 MB (19556267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b523f6cc68d030e209e9a82ce3b3451828dc30ea36835538683ce58effd0364e`  
		Last Modified: Tue, 15 Jul 2025 19:25:44 GMT  
		Size: 12.2 KB (12236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b0ebca30eb1be4ea618c47b7df8edfe29ea98ee9a50e9f5ac737d4def9d43eb`  
		Last Modified: Tue, 15 Jul 2025 19:25:44 GMT  
		Size: 11.9 KB (11895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4a0c26e12214ed30329c891e237537b5f1300d0cbb3fb3373f735d7a88ad7c5`  
		Last Modified: Tue, 15 Jul 2025 19:25:43 GMT  
		Size: 237.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7.17-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:657fe6fbe370582f5c02e3060e50aa260ef4337a04819df606e1f6ddef06f178
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.1 KB (186131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef1a38a41afefa7d15b684d86787bd13668e232e2bae0606c4d13c2928bb10fb`

```dockerfile
```

-	Layers:
	-	`sha256:b666ed462b0b587e4074f667fa9c57ca9514692758ebe77f7fdb7d0e2f9cf571`  
		Last Modified: Tue, 15 Jul 2025 21:38:24 GMT  
		Size: 169.2 KB (169219 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:210c85b79477d42432c1e662ca4140caf59b700dc7b0f6b9870e337bbd012561`  
		Last Modified: Tue, 15 Jul 2025 21:38:25 GMT  
		Size: 16.9 KB (16912 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.8`

```console
$ docker pull chronograf@sha256:7965a031fecdaf6c92fedba9e0ded9c5594c9c936513c0fa4b919effd7202aa9
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
$ docker pull chronograf@sha256:2a17b87bcf1e58be6f9198133d9b572779dc469e39a7bda8e32e4bd6e97fb4d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69871306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1df26b781beaebba13efe14f226161bd9255cb4422ef9dc315086ee24ebebf10`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 15 Aug 2025 14:37:23 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1759104000'
# Fri, 15 Aug 2025 14:37:23 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Fri, 15 Aug 2025 14:37:23 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 15 Aug 2025 14:37:23 GMT
VOLUME [/var/lib/chronograf]
# Fri, 15 Aug 2025 14:37:23 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:4eb1dd59a73886acc6a3cc9d4c8f8e66d1fd6ba6d6195b05ce21c22b0658aab8`  
		Last Modified: Mon, 29 Sep 2025 23:35:18 GMT  
		Size: 30.3 MB (30258363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3cbfb4c21aa5ab132349ea17be4aad352a653407e5249308347fd6bae2c64d0`  
		Last Modified: Tue, 30 Sep 2025 21:38:48 GMT  
		Size: 5.2 MB (5224250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d94ee829238400a2683d1d4aa6d1545a0f8ab6c0bdb15a786db204cb88c323f9`  
		Last Modified: Tue, 30 Sep 2025 21:38:52 GMT  
		Size: 34.4 MB (34364297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db872bca7a829ff52ab451098c15bc0f5bf9c025fe6cfe8feed42834f57b2f31`  
		Last Modified: Tue, 30 Sep 2025 01:02:32 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48e43915ded8b51295db97feca4ad4450dc6fee8fa5f3a8c7526a56bd7c6c579`  
		Last Modified: Tue, 30 Sep 2025 01:02:32 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1932504812845279ef6141926c617b576be723c7146141a456aa63d1edde6b01`  
		Last Modified: Tue, 30 Sep 2025 01:02:32 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8` - unknown; unknown

```console
$ docker pull chronograf@sha256:5425208ecfc71833d5cc9cf4e28991ae47233cfca4a511f0e839d264daf8c89a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3120328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf63047efabf091f84b41b33bd3f54016c8b2d6aa637d2e0aefa7e7626a3a58a`

```dockerfile
```

-	Layers:
	-	`sha256:d51d68a7a47decc4e6cbcf3470ae114fc095d18143eb40631dd25d07be173ddd`  
		Last Modified: Tue, 30 Sep 2025 21:38:34 GMT  
		Size: 3.1 MB (3104511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:343874cf8e1ec14ce48dedc0e3ae1826a4a151a14f0988dddc095655fcc2ea30`  
		Last Modified: Tue, 30 Sep 2025 21:38:34 GMT  
		Size: 15.8 KB (15817 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.8` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:8b19e8a899898297fbd1febb35941377e253a69f5434cb2e856fad5336d67ebc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.6 MB (62595105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a63556518067a4c716312395422f97da42ced04d697598c28d58d6c0e6eb993`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 15 Aug 2025 14:37:23 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1757289600'
# Fri, 15 Aug 2025 14:37:23 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Fri, 15 Aug 2025 14:37:23 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 15 Aug 2025 14:37:23 GMT
VOLUME [/var/lib/chronograf]
# Fri, 15 Aug 2025 14:37:23 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:6060ada35559867e583ae59d61cbfce25e84350e0631f50a795fd6d2b2c5651b`  
		Last Modified: Mon, 08 Sep 2025 21:24:07 GMT  
		Size: 25.5 MB (25544079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9487f5eff15efd1793bb98df8c7907cd332d3e7ed6ef63baa5e2e5175bbf9dfd`  
		Last Modified: Tue, 09 Sep 2025 01:15:13 GMT  
		Size: 4.5 MB (4491764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9314f05eb9e48d01dd3350670971a6f58b2c2ff59f379ec3762e12121b8ff4a2`  
		Last Modified: Wed, 10 Sep 2025 17:01:49 GMT  
		Size: 32.5 MB (32534875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a720c565e2a7ee717215a9fd3dd36292c5e6a785515c69db5ff79a61e29ee17`  
		Last Modified: Mon, 08 Sep 2025 23:17:35 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7581e833bfc719ebd396f2287df4f67d9ff20f5fb2a4079ba16f558a5cbde543`  
		Last Modified: Mon, 08 Sep 2025 23:17:34 GMT  
		Size: 11.9 KB (11903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f354753690a7f3b247cab4e6c811c3e09d0e962098c4a7d333bde2a962dd7b93`  
		Last Modified: Mon, 08 Sep 2025 23:17:34 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8` - unknown; unknown

```console
$ docker pull chronograf@sha256:eda5482e5f9c59bef85bb35342d87615a4db08fc281f530301a0e99f440c2cd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3122676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47b73b70615be0b355b866bd3a27add7fa6f3df9640408f1e3b84172874f0f5f`

```dockerfile
```

-	Layers:
	-	`sha256:e400c775846936d96ff96034d6175aaa8ea29b4bd115a27bc711b6f9d6882d8b`  
		Last Modified: Tue, 09 Sep 2025 00:38:48 GMT  
		Size: 3.1 MB (3106782 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80b78fe380f3a67ec991d19f19cdf94f6c2d4bb29ae3514842cfc2a0a21c55d9`  
		Last Modified: Tue, 09 Sep 2025 00:38:49 GMT  
		Size: 15.9 KB (15894 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.8` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:454ceb130dbd6a031f08bc4379bf2fe5fefe3918eec17fca2ec54b1d407f6fa2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.4 MB (66410499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a8281c6a310fff9f5c49dd6d8cc47b5134f814cd43ed272d56679f182e53cf4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 15 Aug 2025 14:37:23 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1759104000'
# Fri, 15 Aug 2025 14:37:23 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Fri, 15 Aug 2025 14:37:23 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 15 Aug 2025 14:37:23 GMT
VOLUME [/var/lib/chronograf]
# Fri, 15 Aug 2025 14:37:23 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:93b0b88e50eb7468103e583a7be2e8ee3fe5f86e6c74df4baca40a3685b5eee1`  
		Last Modified: Mon, 29 Sep 2025 23:34:34 GMT  
		Size: 28.7 MB (28748427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f27f261d0bdd63d3dc58e25e695b881fb1a3d4a921967c201f54ae645d2c7d5`  
		Last Modified: Tue, 30 Sep 2025 00:14:30 GMT  
		Size: 5.2 MB (5208161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:331f0b9dea60ba5320a50b40db1013740effbaed49f9e6639778d83795a8288d`  
		Last Modified: Tue, 30 Sep 2025 00:14:41 GMT  
		Size: 32.4 MB (32429531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c2aa3bfc8e88dee2ab425d399a55009a6804b26b02cb755aa311fe337ffc2d7`  
		Last Modified: Tue, 30 Sep 2025 00:14:29 GMT  
		Size: 12.2 KB (12243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e05b1be0d3fcf884c5df6c65a7313c68cf2c6af8296a90826872fec450552730`  
		Last Modified: Tue, 30 Sep 2025 00:14:29 GMT  
		Size: 11.9 KB (11901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6df912228c6dd76b259d6bbf7ecefd201d60f88496ed4f6c1974798f8e7dff75`  
		Last Modified: Tue, 30 Sep 2025 00:14:30 GMT  
		Size: 236.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8` - unknown; unknown

```console
$ docker pull chronograf@sha256:45e070be126f0b5e02e07b762f2eb3c98b75e0112569aa8f55f33143471037c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3120672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b39e2cab67745cc98e188d0c37225853bc4961705dad74e86bddeb385753f5e1`

```dockerfile
```

-	Layers:
	-	`sha256:fec311de03d295c18725b0c8d17178b9c56769972e6bc1647fc5c7169a5fe817`  
		Last Modified: Wed, 01 Oct 2025 12:38:41 GMT  
		Size: 3.1 MB (3104760 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f85cef9289133bc4b1c5a80dff20976118c7731841d2feff7a86717e06278395`  
		Last Modified: Wed, 01 Oct 2025 12:38:42 GMT  
		Size: 15.9 KB (15912 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.8-alpine`

```console
$ docker pull chronograf@sha256:54a1981ae71b04211489fad87cc788179b1969d8713156b3cea07cbaf7090d04
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.8-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:2af44b54e74243ca5754ad26788de059677be70c697237fc01ecf00800e287e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23131116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8944de4cb3390268f4182e207d58142bad8cf86cc8d4ba4bb2d6a76f93a5f61a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 16 Apr 2025 11:55:02 GMT
ADD alpine-minirootfs-3.20.7-x86_64.tar.gz / # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
CMD ["/bin/sh"]
# Wed, 16 Apr 2025 11:55:02 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Wed, 16 Apr 2025 11:55:02 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
EXPOSE map[8888/tcp:{}]
# Wed, 16 Apr 2025 11:55:02 GMT
VOLUME [/var/lib/chronograf]
# Wed, 16 Apr 2025 11:55:02 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 16 Apr 2025 11:55:02 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:01d036902a3ca86e8793073c8094cba44d83a38953a489ac0641f3de017fe2d2`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3620477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61dfbe3fe473721826ba2315011c32e845a31e60c224eb6db771b2ed4f7fac6f`  
		Last Modified: Tue, 15 Jul 2025 19:25:56 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:224fc53fdd5a40c66ad01df25f767e91507c88115f6e077d847c380989e5c13c`  
		Last Modified: Tue, 15 Jul 2025 19:25:57 GMT  
		Size: 282.1 KB (282055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d4481f0d10edfe8a5260527212182f4c665615fdf2ab512a239a1004a362d68`  
		Last Modified: Tue, 15 Jul 2025 19:25:59 GMT  
		Size: 19.2 MB (19203940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3c9448ffa42575a52ca79751becfd8ff88d467aacad765a524819586b4113cd`  
		Last Modified: Tue, 15 Jul 2025 19:25:57 GMT  
		Size: 12.2 KB (12235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9a9091371bf981662395acfb27b8136708502c44a7061cf0419d445c6a9b652`  
		Last Modified: Tue, 15 Jul 2025 19:25:57 GMT  
		Size: 11.9 KB (11893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:524a2b95bb4eb6fa43ed81f190663e10ca8e5e70cb4c7c4df1651453f882a256`  
		Last Modified: Tue, 15 Jul 2025 19:25:57 GMT  
		Size: 237.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:335a303ffe4bde200d8e9aee490ab147b361e306c03dd59631af3f3fcdca15c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.6 KB (242640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41cde0c6a7d495f23d0ed36df6ed7f4e783b5775c26ab7760d11049ecb6a84b7`

```dockerfile
```

-	Layers:
	-	`sha256:aeb56b5710b5ead79604361cfe592b8496dfc6c06f1e29ccff68a50376ceb346`  
		Last Modified: Tue, 15 Jul 2025 21:38:31 GMT  
		Size: 225.7 KB (225728 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64c6f94d66b56f30a1a9e5630f1bb8ecae792d1c11b3a95f444d99f31ed7e54e`  
		Last Modified: Tue, 15 Jul 2025 21:38:32 GMT  
		Size: 16.9 KB (16912 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.8.10`

```console
$ docker pull chronograf@sha256:7965a031fecdaf6c92fedba9e0ded9c5594c9c936513c0fa4b919effd7202aa9
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
$ docker pull chronograf@sha256:2a17b87bcf1e58be6f9198133d9b572779dc469e39a7bda8e32e4bd6e97fb4d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69871306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1df26b781beaebba13efe14f226161bd9255cb4422ef9dc315086ee24ebebf10`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 15 Aug 2025 14:37:23 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1759104000'
# Fri, 15 Aug 2025 14:37:23 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Fri, 15 Aug 2025 14:37:23 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 15 Aug 2025 14:37:23 GMT
VOLUME [/var/lib/chronograf]
# Fri, 15 Aug 2025 14:37:23 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:4eb1dd59a73886acc6a3cc9d4c8f8e66d1fd6ba6d6195b05ce21c22b0658aab8`  
		Last Modified: Mon, 29 Sep 2025 23:35:18 GMT  
		Size: 30.3 MB (30258363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3cbfb4c21aa5ab132349ea17be4aad352a653407e5249308347fd6bae2c64d0`  
		Last Modified: Tue, 30 Sep 2025 21:38:48 GMT  
		Size: 5.2 MB (5224250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d94ee829238400a2683d1d4aa6d1545a0f8ab6c0bdb15a786db204cb88c323f9`  
		Last Modified: Tue, 30 Sep 2025 21:38:52 GMT  
		Size: 34.4 MB (34364297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db872bca7a829ff52ab451098c15bc0f5bf9c025fe6cfe8feed42834f57b2f31`  
		Last Modified: Tue, 30 Sep 2025 01:02:32 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48e43915ded8b51295db97feca4ad4450dc6fee8fa5f3a8c7526a56bd7c6c579`  
		Last Modified: Tue, 30 Sep 2025 01:02:32 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1932504812845279ef6141926c617b576be723c7146141a456aa63d1edde6b01`  
		Last Modified: Tue, 30 Sep 2025 01:02:32 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:5425208ecfc71833d5cc9cf4e28991ae47233cfca4a511f0e839d264daf8c89a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3120328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf63047efabf091f84b41b33bd3f54016c8b2d6aa637d2e0aefa7e7626a3a58a`

```dockerfile
```

-	Layers:
	-	`sha256:d51d68a7a47decc4e6cbcf3470ae114fc095d18143eb40631dd25d07be173ddd`  
		Last Modified: Tue, 30 Sep 2025 21:38:34 GMT  
		Size: 3.1 MB (3104511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:343874cf8e1ec14ce48dedc0e3ae1826a4a151a14f0988dddc095655fcc2ea30`  
		Last Modified: Tue, 30 Sep 2025 21:38:34 GMT  
		Size: 15.8 KB (15817 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.8.10` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:8b19e8a899898297fbd1febb35941377e253a69f5434cb2e856fad5336d67ebc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.6 MB (62595105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a63556518067a4c716312395422f97da42ced04d697598c28d58d6c0e6eb993`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 15 Aug 2025 14:37:23 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1757289600'
# Fri, 15 Aug 2025 14:37:23 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Fri, 15 Aug 2025 14:37:23 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 15 Aug 2025 14:37:23 GMT
VOLUME [/var/lib/chronograf]
# Fri, 15 Aug 2025 14:37:23 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:6060ada35559867e583ae59d61cbfce25e84350e0631f50a795fd6d2b2c5651b`  
		Last Modified: Mon, 08 Sep 2025 21:24:07 GMT  
		Size: 25.5 MB (25544079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9487f5eff15efd1793bb98df8c7907cd332d3e7ed6ef63baa5e2e5175bbf9dfd`  
		Last Modified: Tue, 09 Sep 2025 01:15:13 GMT  
		Size: 4.5 MB (4491764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9314f05eb9e48d01dd3350670971a6f58b2c2ff59f379ec3762e12121b8ff4a2`  
		Last Modified: Wed, 10 Sep 2025 17:01:49 GMT  
		Size: 32.5 MB (32534875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a720c565e2a7ee717215a9fd3dd36292c5e6a785515c69db5ff79a61e29ee17`  
		Last Modified: Mon, 08 Sep 2025 23:17:35 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7581e833bfc719ebd396f2287df4f67d9ff20f5fb2a4079ba16f558a5cbde543`  
		Last Modified: Mon, 08 Sep 2025 23:17:34 GMT  
		Size: 11.9 KB (11903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f354753690a7f3b247cab4e6c811c3e09d0e962098c4a7d333bde2a962dd7b93`  
		Last Modified: Mon, 08 Sep 2025 23:17:34 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:eda5482e5f9c59bef85bb35342d87615a4db08fc281f530301a0e99f440c2cd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3122676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47b73b70615be0b355b866bd3a27add7fa6f3df9640408f1e3b84172874f0f5f`

```dockerfile
```

-	Layers:
	-	`sha256:e400c775846936d96ff96034d6175aaa8ea29b4bd115a27bc711b6f9d6882d8b`  
		Last Modified: Tue, 09 Sep 2025 00:38:48 GMT  
		Size: 3.1 MB (3106782 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80b78fe380f3a67ec991d19f19cdf94f6c2d4bb29ae3514842cfc2a0a21c55d9`  
		Last Modified: Tue, 09 Sep 2025 00:38:49 GMT  
		Size: 15.9 KB (15894 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.8.10` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:454ceb130dbd6a031f08bc4379bf2fe5fefe3918eec17fca2ec54b1d407f6fa2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.4 MB (66410499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a8281c6a310fff9f5c49dd6d8cc47b5134f814cd43ed272d56679f182e53cf4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 15 Aug 2025 14:37:23 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1759104000'
# Fri, 15 Aug 2025 14:37:23 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Fri, 15 Aug 2025 14:37:23 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 15 Aug 2025 14:37:23 GMT
VOLUME [/var/lib/chronograf]
# Fri, 15 Aug 2025 14:37:23 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:93b0b88e50eb7468103e583a7be2e8ee3fe5f86e6c74df4baca40a3685b5eee1`  
		Last Modified: Mon, 29 Sep 2025 23:34:34 GMT  
		Size: 28.7 MB (28748427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f27f261d0bdd63d3dc58e25e695b881fb1a3d4a921967c201f54ae645d2c7d5`  
		Last Modified: Tue, 30 Sep 2025 00:14:30 GMT  
		Size: 5.2 MB (5208161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:331f0b9dea60ba5320a50b40db1013740effbaed49f9e6639778d83795a8288d`  
		Last Modified: Tue, 30 Sep 2025 00:14:41 GMT  
		Size: 32.4 MB (32429531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c2aa3bfc8e88dee2ab425d399a55009a6804b26b02cb755aa311fe337ffc2d7`  
		Last Modified: Tue, 30 Sep 2025 00:14:29 GMT  
		Size: 12.2 KB (12243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e05b1be0d3fcf884c5df6c65a7313c68cf2c6af8296a90826872fec450552730`  
		Last Modified: Tue, 30 Sep 2025 00:14:29 GMT  
		Size: 11.9 KB (11901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6df912228c6dd76b259d6bbf7ecefd201d60f88496ed4f6c1974798f8e7dff75`  
		Last Modified: Tue, 30 Sep 2025 00:14:30 GMT  
		Size: 236.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:45e070be126f0b5e02e07b762f2eb3c98b75e0112569aa8f55f33143471037c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3120672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b39e2cab67745cc98e188d0c37225853bc4961705dad74e86bddeb385753f5e1`

```dockerfile
```

-	Layers:
	-	`sha256:fec311de03d295c18725b0c8d17178b9c56769972e6bc1647fc5c7169a5fe817`  
		Last Modified: Wed, 01 Oct 2025 12:38:41 GMT  
		Size: 3.1 MB (3104760 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f85cef9289133bc4b1c5a80dff20976118c7731841d2feff7a86717e06278395`  
		Last Modified: Wed, 01 Oct 2025 12:38:42 GMT  
		Size: 15.9 KB (15912 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.8.10-alpine`

```console
$ docker pull chronograf@sha256:54a1981ae71b04211489fad87cc788179b1969d8713156b3cea07cbaf7090d04
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.8.10-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:2af44b54e74243ca5754ad26788de059677be70c697237fc01ecf00800e287e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23131116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8944de4cb3390268f4182e207d58142bad8cf86cc8d4ba4bb2d6a76f93a5f61a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 16 Apr 2025 11:55:02 GMT
ADD alpine-minirootfs-3.20.7-x86_64.tar.gz / # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
CMD ["/bin/sh"]
# Wed, 16 Apr 2025 11:55:02 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Wed, 16 Apr 2025 11:55:02 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
EXPOSE map[8888/tcp:{}]
# Wed, 16 Apr 2025 11:55:02 GMT
VOLUME [/var/lib/chronograf]
# Wed, 16 Apr 2025 11:55:02 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 16 Apr 2025 11:55:02 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:01d036902a3ca86e8793073c8094cba44d83a38953a489ac0641f3de017fe2d2`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3620477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61dfbe3fe473721826ba2315011c32e845a31e60c224eb6db771b2ed4f7fac6f`  
		Last Modified: Tue, 15 Jul 2025 19:25:56 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:224fc53fdd5a40c66ad01df25f767e91507c88115f6e077d847c380989e5c13c`  
		Last Modified: Tue, 15 Jul 2025 19:25:57 GMT  
		Size: 282.1 KB (282055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d4481f0d10edfe8a5260527212182f4c665615fdf2ab512a239a1004a362d68`  
		Last Modified: Tue, 15 Jul 2025 19:25:59 GMT  
		Size: 19.2 MB (19203940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3c9448ffa42575a52ca79751becfd8ff88d467aacad765a524819586b4113cd`  
		Last Modified: Tue, 15 Jul 2025 19:25:57 GMT  
		Size: 12.2 KB (12235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9a9091371bf981662395acfb27b8136708502c44a7061cf0419d445c6a9b652`  
		Last Modified: Tue, 15 Jul 2025 19:25:57 GMT  
		Size: 11.9 KB (11893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:524a2b95bb4eb6fa43ed81f190663e10ca8e5e70cb4c7c4df1651453f882a256`  
		Last Modified: Tue, 15 Jul 2025 19:25:57 GMT  
		Size: 237.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8.10-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:335a303ffe4bde200d8e9aee490ab147b361e306c03dd59631af3f3fcdca15c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.6 KB (242640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41cde0c6a7d495f23d0ed36df6ed7f4e783b5775c26ab7760d11049ecb6a84b7`

```dockerfile
```

-	Layers:
	-	`sha256:aeb56b5710b5ead79604361cfe592b8496dfc6c06f1e29ccff68a50376ceb346`  
		Last Modified: Tue, 15 Jul 2025 21:38:31 GMT  
		Size: 225.7 KB (225728 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64c6f94d66b56f30a1a9e5630f1bb8ecae792d1c11b3a95f444d99f31ed7e54e`  
		Last Modified: Tue, 15 Jul 2025 21:38:32 GMT  
		Size: 16.9 KB (16912 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.9`

```console
$ docker pull chronograf@sha256:90f392f443e4e6a465b72972172bfdf630270b3ac9c6298377d01389b516ea33
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
$ docker pull chronograf@sha256:efe2ab804e18ecb6d9a13664a061260518869ee8952b42d3b311f9d2c69f18fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.5 MB (70518754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b869ae75ea8a26aba44e5dc85ea92e8b7c53e773727acb769e56d4f7998ee51`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 15 Aug 2025 14:37:23 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1759104000'
# Fri, 15 Aug 2025 14:37:23 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Fri, 15 Aug 2025 14:37:23 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 15 Aug 2025 14:37:23 GMT
VOLUME [/var/lib/chronograf]
# Fri, 15 Aug 2025 14:37:23 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:4eb1dd59a73886acc6a3cc9d4c8f8e66d1fd6ba6d6195b05ce21c22b0658aab8`  
		Last Modified: Mon, 29 Sep 2025 23:35:18 GMT  
		Size: 30.3 MB (30258363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edbea7086b920180de745b57f78d07e3d29bc8ea40db5adae7728c1a28c365bb`  
		Last Modified: Wed, 01 Oct 2025 04:00:24 GMT  
		Size: 5.2 MB (5224242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4de18b2071aa68f29d1480ccd2762148cb67f3d8588d374fc9b5f8120b6b275`  
		Last Modified: Wed, 01 Oct 2025 04:00:26 GMT  
		Size: 35.0 MB (35011767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:107230c064f53f23788f94eedc0e11276d51534d1969689876a89de0f72aa5ce`  
		Last Modified: Tue, 30 Sep 2025 20:47:50 GMT  
		Size: 12.2 KB (12243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8336d32c06bd611a7215e14dc313b07dd540f06e9ba6dbe04a4ec16f85a37535`  
		Last Modified: Tue, 30 Sep 2025 20:47:51 GMT  
		Size: 11.9 KB (11900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c267d532bd03c36a6317a8e5088eb3a687f7f814c09ff5a6196da970032eae70`  
		Last Modified: Tue, 30 Sep 2025 20:47:50 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9` - unknown; unknown

```console
$ docker pull chronograf@sha256:1d40443b5abcefeca56cd1cf55e8b2f1619d2276e563aa22a014e646c5dcbd52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3125530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1e0e371fa58e41eb498feaa658b576b18dad21fcdb9da575d25f2824e79a142`

```dockerfile
```

-	Layers:
	-	`sha256:9b56c9caedb07aec7019390496f8adff84f2588f5d3b50e41a4da4de8e884614`  
		Last Modified: Tue, 30 Sep 2025 21:38:40 GMT  
		Size: 3.1 MB (3109721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1670ca5e66236fc2945f05e3b574d647d432a6ad3e26dd4e38097f320b80f892`  
		Last Modified: Tue, 30 Sep 2025 21:38:41 GMT  
		Size: 15.8 KB (15809 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.9` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:b4f3a31cea9d6e92ac29ee9ac16ed3d79158f5ecfccb499045f7121bf5b9e85d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.4 MB (63371891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dd9b82576c808e971d5a8987f10d7fc2c1cbc90ee9963d866dee8e90609cdc4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 15 Aug 2025 14:37:23 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1757289600'
# Fri, 15 Aug 2025 14:37:23 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Fri, 15 Aug 2025 14:37:23 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 15 Aug 2025 14:37:23 GMT
VOLUME [/var/lib/chronograf]
# Fri, 15 Aug 2025 14:37:23 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:6060ada35559867e583ae59d61cbfce25e84350e0631f50a795fd6d2b2c5651b`  
		Last Modified: Mon, 08 Sep 2025 21:24:07 GMT  
		Size: 25.5 MB (25544079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdddcaecebf4f0973baa371565eb33995d428ae7fcda18dd4e8a8cd413e07fa5`  
		Last Modified: Tue, 09 Sep 2025 01:16:55 GMT  
		Size: 4.5 MB (4491837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:467a5ecd58b41b80ad949de62a6b6fba37e8deb11ea2845bd270404234897325`  
		Last Modified: Tue, 09 Sep 2025 19:04:14 GMT  
		Size: 33.3 MB (33311586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d09cafc7b1ab6e2ff3cabac054c05b11036384584a483791b8f87e4c8f4f9f2`  
		Last Modified: Mon, 08 Sep 2025 23:18:36 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8fdcdf633f0f72ea7785b15dd45c53b6d50e7e68d6d9df56da14aa41ed8570e`  
		Last Modified: Mon, 08 Sep 2025 23:18:35 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb26294d42550b6211c2beb2b1f05caed0597fd232c2bbe8c88bd61c2650ef9`  
		Last Modified: Mon, 08 Sep 2025 23:18:35 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9` - unknown; unknown

```console
$ docker pull chronograf@sha256:94084e14d1d36ff640e92621433e2be884aaf5c1d3be382bad9224ddc5aee02f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3127879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5a48b4f9c17aacc24839175a593d546ea78b6161fcf9ec5f1b2066037b87487`

```dockerfile
```

-	Layers:
	-	`sha256:6ee6c1a2ef29f1e703266608156e0e1f21a4e5845b73914c73e7b753f07beaf9`  
		Last Modified: Tue, 09 Sep 2025 00:39:01 GMT  
		Size: 3.1 MB (3111992 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1684a2ed2354662dafbd12d947d6a6fbc7c04030b1614802691117210e570deb`  
		Last Modified: Tue, 09 Sep 2025 00:39:03 GMT  
		Size: 15.9 KB (15887 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.9` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:b7c0624e4ef443577c5225970823d099b3cb66aa31411ea8952dd2b24fa4817c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.2 MB (67163245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91e96cc0801f4755322ad891341fe5e30cbf4ea2b077105952f158031abb48cb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 15 Aug 2025 14:37:23 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1759104000'
# Fri, 15 Aug 2025 14:37:23 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Fri, 15 Aug 2025 14:37:23 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 15 Aug 2025 14:37:23 GMT
VOLUME [/var/lib/chronograf]
# Fri, 15 Aug 2025 14:37:23 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:93b0b88e50eb7468103e583a7be2e8ee3fe5f86e6c74df4baca40a3685b5eee1`  
		Last Modified: Mon, 29 Sep 2025 23:34:34 GMT  
		Size: 28.7 MB (28748427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63f1246c1f32025bcd5eb0006a5af07c7d527ec945ae8952a05924b77653fe3c`  
		Last Modified: Tue, 30 Sep 2025 00:15:16 GMT  
		Size: 5.2 MB (5208205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8e94aae0e8a8d09703a56a58b79fcc695c032b0c2af6ba3e830a0a5123dcccd`  
		Last Modified: Tue, 30 Sep 2025 00:15:21 GMT  
		Size: 33.2 MB (33182224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e8735956a828fd8a9594e7e2612483de3e3b6fd91c25c77796f5164c88a5e78`  
		Last Modified: Tue, 30 Sep 2025 00:15:15 GMT  
		Size: 12.2 KB (12243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:506aac38cee1b1bb75d73fae22384036de21a851dab8922e96c65ab822fda1fc`  
		Last Modified: Tue, 30 Sep 2025 00:15:15 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cc64dea0dea3ff4c659038af20186c2dabb8eba9b42195d77b5ed20217d002d`  
		Last Modified: Tue, 30 Sep 2025 00:15:17 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9` - unknown; unknown

```console
$ docker pull chronograf@sha256:6072ada9f6b3510775f5f75ab88549449db04ce7543e79924454eb25d6e7c2c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3125875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d4480ce93844679c10d684c9cd64a2b109c99df52f8ce20bd50ab070d0c793f`

```dockerfile
```

-	Layers:
	-	`sha256:302c2ad3c248f682c92b97e80bced95fc6ca92ba5828f70a62c3862bba74b54e`  
		Last Modified: Wed, 01 Oct 2025 12:38:51 GMT  
		Size: 3.1 MB (3109970 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66c6e190e39a15242effa5877cdadb534679e846e9dd579fac195174c8d207ff`  
		Last Modified: Wed, 01 Oct 2025 12:38:52 GMT  
		Size: 15.9 KB (15905 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.9-alpine`

```console
$ docker pull chronograf@sha256:e82268bc63214aefb7795c76800f58a49a77298fdf914d0aaa852225b5b2d6c6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.9-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:0cc8a5ee6056da671779bbc53828ea65e1f309e51a74e27865cb051828059ca5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23599205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7f8220dd98febecb9f6e0c358bb6ebaf7eb7d89f028ed05aacb6cd04b6ad50d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 16 Apr 2025 11:55:02 GMT
ADD alpine-minirootfs-3.20.7-x86_64.tar.gz / # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
CMD ["/bin/sh"]
# Wed, 16 Apr 2025 11:55:02 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Wed, 16 Apr 2025 11:55:02 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
EXPOSE map[8888/tcp:{}]
# Wed, 16 Apr 2025 11:55:02 GMT
VOLUME [/var/lib/chronograf]
# Wed, 16 Apr 2025 11:55:02 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 16 Apr 2025 11:55:02 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:01d036902a3ca86e8793073c8094cba44d83a38953a489ac0641f3de017fe2d2`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3620477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61dfbe3fe473721826ba2315011c32e845a31e60c224eb6db771b2ed4f7fac6f`  
		Last Modified: Tue, 15 Jul 2025 19:25:56 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d060473c62053335105b184ca2e2227dd2cc77e588a502f6a81a0ed10b85527`  
		Last Modified: Tue, 15 Jul 2025 19:26:01 GMT  
		Size: 282.1 KB (282051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93fe87eb48ed778a345d6348cc0c25a6f24351995c78dc99903bef7e95a00fb2`  
		Last Modified: Tue, 15 Jul 2025 19:26:04 GMT  
		Size: 19.7 MB (19672029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00a0420546acb914cbfdd3a2c0572c061f01b15eab8a5a297ef553b30b87b935`  
		Last Modified: Tue, 15 Jul 2025 19:26:02 GMT  
		Size: 12.2 KB (12237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1735c34287fbc0a2623ad4d4af0815e429fcede15029790e23b6782f23fa9df`  
		Last Modified: Tue, 15 Jul 2025 19:26:02 GMT  
		Size: 11.9 KB (11895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dad38d49a745fab260e4e8f63afcab82c1339b91b8546c645f8d67f4153ce717`  
		Last Modified: Tue, 15 Jul 2025 19:26:02 GMT  
		Size: 237.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:8c475c61b1d16550e4609c1c1a314791065bec6f38da628a08a5db2516a8d791
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.8 KB (247849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5da7a725769919c0c6a29671a279fe0f2589d8fe32414c6f321e623d908e2bc7`

```dockerfile
```

-	Layers:
	-	`sha256:9477ca0f980bf7c4a32ff5ebde9e96019a08792d16c74bab24fdc7524a75e316`  
		Last Modified: Tue, 15 Jul 2025 21:38:36 GMT  
		Size: 230.9 KB (230940 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57495c4652bfee0d305b99c69695067ed1bebda167b19c7925c0a918774382e2`  
		Last Modified: Tue, 15 Jul 2025 21:38:36 GMT  
		Size: 16.9 KB (16909 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.9.4`

```console
$ docker pull chronograf@sha256:90f392f443e4e6a465b72972172bfdf630270b3ac9c6298377d01389b516ea33
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
$ docker pull chronograf@sha256:efe2ab804e18ecb6d9a13664a061260518869ee8952b42d3b311f9d2c69f18fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.5 MB (70518754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b869ae75ea8a26aba44e5dc85ea92e8b7c53e773727acb769e56d4f7998ee51`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 15 Aug 2025 14:37:23 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1759104000'
# Fri, 15 Aug 2025 14:37:23 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Fri, 15 Aug 2025 14:37:23 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 15 Aug 2025 14:37:23 GMT
VOLUME [/var/lib/chronograf]
# Fri, 15 Aug 2025 14:37:23 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:4eb1dd59a73886acc6a3cc9d4c8f8e66d1fd6ba6d6195b05ce21c22b0658aab8`  
		Last Modified: Mon, 29 Sep 2025 23:35:18 GMT  
		Size: 30.3 MB (30258363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edbea7086b920180de745b57f78d07e3d29bc8ea40db5adae7728c1a28c365bb`  
		Last Modified: Wed, 01 Oct 2025 04:00:24 GMT  
		Size: 5.2 MB (5224242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4de18b2071aa68f29d1480ccd2762148cb67f3d8588d374fc9b5f8120b6b275`  
		Last Modified: Wed, 01 Oct 2025 04:00:26 GMT  
		Size: 35.0 MB (35011767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:107230c064f53f23788f94eedc0e11276d51534d1969689876a89de0f72aa5ce`  
		Last Modified: Tue, 30 Sep 2025 20:47:50 GMT  
		Size: 12.2 KB (12243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8336d32c06bd611a7215e14dc313b07dd540f06e9ba6dbe04a4ec16f85a37535`  
		Last Modified: Tue, 30 Sep 2025 20:47:51 GMT  
		Size: 11.9 KB (11900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c267d532bd03c36a6317a8e5088eb3a687f7f814c09ff5a6196da970032eae70`  
		Last Modified: Tue, 30 Sep 2025 20:47:50 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9.4` - unknown; unknown

```console
$ docker pull chronograf@sha256:1d40443b5abcefeca56cd1cf55e8b2f1619d2276e563aa22a014e646c5dcbd52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3125530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1e0e371fa58e41eb498feaa658b576b18dad21fcdb9da575d25f2824e79a142`

```dockerfile
```

-	Layers:
	-	`sha256:9b56c9caedb07aec7019390496f8adff84f2588f5d3b50e41a4da4de8e884614`  
		Last Modified: Tue, 30 Sep 2025 21:38:40 GMT  
		Size: 3.1 MB (3109721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1670ca5e66236fc2945f05e3b574d647d432a6ad3e26dd4e38097f320b80f892`  
		Last Modified: Tue, 30 Sep 2025 21:38:41 GMT  
		Size: 15.8 KB (15809 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.9.4` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:b4f3a31cea9d6e92ac29ee9ac16ed3d79158f5ecfccb499045f7121bf5b9e85d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.4 MB (63371891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dd9b82576c808e971d5a8987f10d7fc2c1cbc90ee9963d866dee8e90609cdc4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 15 Aug 2025 14:37:23 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1757289600'
# Fri, 15 Aug 2025 14:37:23 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Fri, 15 Aug 2025 14:37:23 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 15 Aug 2025 14:37:23 GMT
VOLUME [/var/lib/chronograf]
# Fri, 15 Aug 2025 14:37:23 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:6060ada35559867e583ae59d61cbfce25e84350e0631f50a795fd6d2b2c5651b`  
		Last Modified: Mon, 08 Sep 2025 21:24:07 GMT  
		Size: 25.5 MB (25544079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdddcaecebf4f0973baa371565eb33995d428ae7fcda18dd4e8a8cd413e07fa5`  
		Last Modified: Tue, 09 Sep 2025 01:16:55 GMT  
		Size: 4.5 MB (4491837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:467a5ecd58b41b80ad949de62a6b6fba37e8deb11ea2845bd270404234897325`  
		Last Modified: Tue, 09 Sep 2025 19:04:14 GMT  
		Size: 33.3 MB (33311586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d09cafc7b1ab6e2ff3cabac054c05b11036384584a483791b8f87e4c8f4f9f2`  
		Last Modified: Mon, 08 Sep 2025 23:18:36 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8fdcdf633f0f72ea7785b15dd45c53b6d50e7e68d6d9df56da14aa41ed8570e`  
		Last Modified: Mon, 08 Sep 2025 23:18:35 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb26294d42550b6211c2beb2b1f05caed0597fd232c2bbe8c88bd61c2650ef9`  
		Last Modified: Mon, 08 Sep 2025 23:18:35 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9.4` - unknown; unknown

```console
$ docker pull chronograf@sha256:94084e14d1d36ff640e92621433e2be884aaf5c1d3be382bad9224ddc5aee02f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3127879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5a48b4f9c17aacc24839175a593d546ea78b6161fcf9ec5f1b2066037b87487`

```dockerfile
```

-	Layers:
	-	`sha256:6ee6c1a2ef29f1e703266608156e0e1f21a4e5845b73914c73e7b753f07beaf9`  
		Last Modified: Tue, 09 Sep 2025 00:39:01 GMT  
		Size: 3.1 MB (3111992 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1684a2ed2354662dafbd12d947d6a6fbc7c04030b1614802691117210e570deb`  
		Last Modified: Tue, 09 Sep 2025 00:39:03 GMT  
		Size: 15.9 KB (15887 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.9.4` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:b7c0624e4ef443577c5225970823d099b3cb66aa31411ea8952dd2b24fa4817c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.2 MB (67163245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91e96cc0801f4755322ad891341fe5e30cbf4ea2b077105952f158031abb48cb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 15 Aug 2025 14:37:23 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1759104000'
# Fri, 15 Aug 2025 14:37:23 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Fri, 15 Aug 2025 14:37:23 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 15 Aug 2025 14:37:23 GMT
VOLUME [/var/lib/chronograf]
# Fri, 15 Aug 2025 14:37:23 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:93b0b88e50eb7468103e583a7be2e8ee3fe5f86e6c74df4baca40a3685b5eee1`  
		Last Modified: Mon, 29 Sep 2025 23:34:34 GMT  
		Size: 28.7 MB (28748427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63f1246c1f32025bcd5eb0006a5af07c7d527ec945ae8952a05924b77653fe3c`  
		Last Modified: Tue, 30 Sep 2025 00:15:16 GMT  
		Size: 5.2 MB (5208205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8e94aae0e8a8d09703a56a58b79fcc695c032b0c2af6ba3e830a0a5123dcccd`  
		Last Modified: Tue, 30 Sep 2025 00:15:21 GMT  
		Size: 33.2 MB (33182224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e8735956a828fd8a9594e7e2612483de3e3b6fd91c25c77796f5164c88a5e78`  
		Last Modified: Tue, 30 Sep 2025 00:15:15 GMT  
		Size: 12.2 KB (12243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:506aac38cee1b1bb75d73fae22384036de21a851dab8922e96c65ab822fda1fc`  
		Last Modified: Tue, 30 Sep 2025 00:15:15 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cc64dea0dea3ff4c659038af20186c2dabb8eba9b42195d77b5ed20217d002d`  
		Last Modified: Tue, 30 Sep 2025 00:15:17 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9.4` - unknown; unknown

```console
$ docker pull chronograf@sha256:6072ada9f6b3510775f5f75ab88549449db04ce7543e79924454eb25d6e7c2c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3125875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d4480ce93844679c10d684c9cd64a2b109c99df52f8ce20bd50ab070d0c793f`

```dockerfile
```

-	Layers:
	-	`sha256:302c2ad3c248f682c92b97e80bced95fc6ca92ba5828f70a62c3862bba74b54e`  
		Last Modified: Wed, 01 Oct 2025 12:38:51 GMT  
		Size: 3.1 MB (3109970 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66c6e190e39a15242effa5877cdadb534679e846e9dd579fac195174c8d207ff`  
		Last Modified: Wed, 01 Oct 2025 12:38:52 GMT  
		Size: 15.9 KB (15905 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.9.4-alpine`

```console
$ docker pull chronograf@sha256:e82268bc63214aefb7795c76800f58a49a77298fdf914d0aaa852225b5b2d6c6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.9.4-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:0cc8a5ee6056da671779bbc53828ea65e1f309e51a74e27865cb051828059ca5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23599205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7f8220dd98febecb9f6e0c358bb6ebaf7eb7d89f028ed05aacb6cd04b6ad50d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 16 Apr 2025 11:55:02 GMT
ADD alpine-minirootfs-3.20.7-x86_64.tar.gz / # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
CMD ["/bin/sh"]
# Wed, 16 Apr 2025 11:55:02 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Wed, 16 Apr 2025 11:55:02 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
EXPOSE map[8888/tcp:{}]
# Wed, 16 Apr 2025 11:55:02 GMT
VOLUME [/var/lib/chronograf]
# Wed, 16 Apr 2025 11:55:02 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 16 Apr 2025 11:55:02 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:01d036902a3ca86e8793073c8094cba44d83a38953a489ac0641f3de017fe2d2`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3620477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61dfbe3fe473721826ba2315011c32e845a31e60c224eb6db771b2ed4f7fac6f`  
		Last Modified: Tue, 15 Jul 2025 19:25:56 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d060473c62053335105b184ca2e2227dd2cc77e588a502f6a81a0ed10b85527`  
		Last Modified: Tue, 15 Jul 2025 19:26:01 GMT  
		Size: 282.1 KB (282051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93fe87eb48ed778a345d6348cc0c25a6f24351995c78dc99903bef7e95a00fb2`  
		Last Modified: Tue, 15 Jul 2025 19:26:04 GMT  
		Size: 19.7 MB (19672029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00a0420546acb914cbfdd3a2c0572c061f01b15eab8a5a297ef553b30b87b935`  
		Last Modified: Tue, 15 Jul 2025 19:26:02 GMT  
		Size: 12.2 KB (12237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1735c34287fbc0a2623ad4d4af0815e429fcede15029790e23b6782f23fa9df`  
		Last Modified: Tue, 15 Jul 2025 19:26:02 GMT  
		Size: 11.9 KB (11895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dad38d49a745fab260e4e8f63afcab82c1339b91b8546c645f8d67f4153ce717`  
		Last Modified: Tue, 15 Jul 2025 19:26:02 GMT  
		Size: 237.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9.4-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:8c475c61b1d16550e4609c1c1a314791065bec6f38da628a08a5db2516a8d791
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.8 KB (247849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5da7a725769919c0c6a29671a279fe0f2589d8fe32414c6f321e623d908e2bc7`

```dockerfile
```

-	Layers:
	-	`sha256:9477ca0f980bf7c4a32ff5ebde9e96019a08792d16c74bab24fdc7524a75e316`  
		Last Modified: Tue, 15 Jul 2025 21:38:36 GMT  
		Size: 230.9 KB (230940 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57495c4652bfee0d305b99c69695067ed1bebda167b19c7925c0a918774382e2`  
		Last Modified: Tue, 15 Jul 2025 21:38:36 GMT  
		Size: 16.9 KB (16909 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:alpine`

```console
$ docker pull chronograf@sha256:1ddf470cfa125f9de7db291932845b6b1c839a17470a5edc9937520e555021fd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:313949b2dd32c7b925d8f1df1814ea49db2dfaa617a995372f7c633ddbe37571
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.7 MB (32688182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed55e91957e952193ac6c0b4c3d2348e04403644844c0eea861726392a1fe789`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
RUN apk add --no-cache ca-certificates setpriv &&     update-ca-certificates # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENV CHRONOGRAF_VERSION=1.10.8
# Fri, 15 Aug 2025 14:37:23 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S chronograf &&     adduser -S chronograf -G chronograf &&     mkdir -m 0750 -p /var/lib/chronograf &&     chown chronograf:chronograf /var/lib/chronograf # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 15 Aug 2025 14:37:23 GMT
VOLUME [/var/lib/chronograf]
# Fri, 15 Aug 2025 14:37:23 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fac5852aab88158a636f5c62b8372eeb08344812accaa647d93267bb5aabbe90`  
		Last Modified: Tue, 19 Aug 2025 16:45:51 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f629721feb48667f4ade9b4f3439178d5683262876745a0dbe2a1a200cf55024`  
		Last Modified: Tue, 19 Aug 2025 16:45:52 GMT  
		Size: 305.9 KB (305880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbe170c0d482899a4f59077af1eb298089e38f7895c3a04eb0896631e83d8247`  
		Last Modified: Tue, 19 Aug 2025 16:45:56 GMT  
		Size: 28.6 MB (28557892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c8a90fb1888f50f9757485fd13c0739accd286933df741c386b75b66c8dcdbe`  
		Last Modified: Tue, 19 Aug 2025 16:45:52 GMT  
		Size: 12.2 KB (12236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faa33ce60529ed7913cfa394491c65481d4d49d33259e1e59fc23f92cee6e032`  
		Last Modified: Tue, 19 Aug 2025 16:45:52 GMT  
		Size: 11.9 KB (11892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:706de7adfac6567def5ce908056a9dc4c7d01529aaff53726d8f2feeceed04ef`  
		Last Modified: Tue, 19 Aug 2025 16:45:52 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:7aee1aa708c95df18c4c5fccc05eb80166744df023669f9774715fa5386cf8d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.6 KB (265625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a231bfc9063c7a6fbb1fae07d3082eb216852349d0654aeb6a0c122482cb3a92`

```dockerfile
```

-	Layers:
	-	`sha256:f269451dd549f671f7ea78b61bd711e09bfc0f478b96d30dcd4ccf7ac0eea26c`  
		Last Modified: Tue, 19 Aug 2025 18:38:30 GMT  
		Size: 247.8 KB (247770 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a6b2fd6d2f7b798e331a71fe469e5c57487bacdc8e5532bc2af0acb4733f74a`  
		Last Modified: Tue, 19 Aug 2025 18:38:30 GMT  
		Size: 17.9 KB (17855 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:latest`

```console
$ docker pull chronograf@sha256:4f4e40fdf0e855d127591f1e9900ff2d0ceecc52925e9d8b6af100491356bbc2
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
$ docker pull chronograf@sha256:d0b735de0338681ab1deeb206f4367d66ad016b4f0aa8aa641a7f4bf9550201d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.4 MB (85408171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfe6e45e8672fa4255607fcb8f990c8d49a27b82d764ed7dc22124d1622ff068`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 15 Aug 2025 14:37:23 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1759104000'
# Fri, 15 Aug 2025 14:37:23 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENV CHRONOGRAF_VERSION=1.10.8
# Fri, 15 Aug 2025 14:37:23 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 15 Aug 2025 14:37:23 GMT
VOLUME [/var/lib/chronograf]
# Fri, 15 Aug 2025 14:37:23 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:5c32499ab806884c5725c705c2bf528662d034ed99de13d3205309e0d9ef0375`  
		Last Modified: Mon, 29 Sep 2025 23:34:35 GMT  
		Size: 28.2 MB (28228336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c565502243bfc584c19aa42478e3b6ffd360f0aa9511965b5a8c85e62976b99`  
		Last Modified: Tue, 30 Sep 2025 21:38:30 GMT  
		Size: 7.9 MB (7878758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d99c8246fc7c45a2eda09b31831a752340b5f7f2306f83c8b885569de570b154`  
		Last Modified: Tue, 30 Sep 2025 21:38:32 GMT  
		Size: 49.3 MB (49276613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12575b13123c97743e1601aea6b620470cd8c3e25b4cde80494b99d736ede41b`  
		Last Modified: Tue, 30 Sep 2025 01:02:59 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17cb7667e402714079cf20570799096a3d51e8e68e4c74ef2451a835fa43e42a`  
		Last Modified: Tue, 30 Sep 2025 01:02:59 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4a89b8ff038b82766c18e9de2d8873fdc5ee1100b5e99b593dad8e5cfa57911`  
		Last Modified: Tue, 30 Sep 2025 01:02:59 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:fd59189507488845ebea82e9b86c5c6a308f9c8ced9bd6b24c63561578ab0d0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2870202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3314e1696b23a57f0915083301ff00dbe939b8a9e64db79ed29f6aceb67c888`

```dockerfile
```

-	Layers:
	-	`sha256:bb040956c6bd766a36591d90eb254901d9d8f838f977e2a2644e3b12755a2b21`  
		Last Modified: Tue, 30 Sep 2025 21:38:20 GMT  
		Size: 2.9 MB (2854074 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00d495b61186223ff2af947e470fe001315b7ff26a16ace52dc8299d313350f0`  
		Last Modified: Tue, 30 Sep 2025 21:38:21 GMT  
		Size: 16.1 KB (16128 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:latest` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:f189a29427f97eecc7768bca139276270349aa7d98b57e98772bf56fc190d34a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76088312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36a94564436fe34f1c742b4b3a1aa79316130308430cd2d43d4ad6e47b3b2895`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 15 Aug 2025 14:37:23 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1757289600'
# Fri, 15 Aug 2025 14:37:23 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENV CHRONOGRAF_VERSION=1.10.8
# Fri, 15 Aug 2025 14:37:23 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 15 Aug 2025 14:37:23 GMT
VOLUME [/var/lib/chronograf]
# Fri, 15 Aug 2025 14:37:23 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:e747f8ef7f1d9a41c99bfb53889f7b8de3504300740a326627fc7522904708cc`  
		Last Modified: Mon, 08 Sep 2025 21:14:21 GMT  
		Size: 23.9 MB (23933904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dec635ab1c380e6e730c672c038827bb3e867453884ab704fea74982ba82e1d`  
		Last Modified: Mon, 08 Sep 2025 22:53:38 GMT  
		Size: 6.5 MB (6508082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:441abcfc8919aa192be1da5f5617adbba057a764b0e352a29f1f1d512effca70`  
		Last Modified: Mon, 08 Sep 2025 22:53:38 GMT  
		Size: 45.6 MB (45621861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb5085ff402d82b73039a7434cc3d4e91a50deb09fff90fd4bd998229319fc26`  
		Last Modified: Mon, 08 Sep 2025 22:38:28 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e95b01abe85ff5bbb5cc08ff120db75e8d1c3b7b81d8e159da1586a37018f818`  
		Last Modified: Mon, 08 Sep 2025 22:38:32 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf87c54eae35aecca65e9361087715fab6d3c24bba6083f6f7089cec3f040573`  
		Last Modified: Mon, 08 Sep 2025 22:38:35 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:14687783dfad06fbcc1f3a5c0b4341f5808e9c0a24124f5050b183891b850211
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2872584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c54263a6d7bf00388a84cc3a87e88753a50cb7fa75d458174d929780824bc309`

```dockerfile
```

-	Layers:
	-	`sha256:bdb5efca6a366afce6d4aff087f1ad2c73d98d6d29f750e3e1df5aff87a5b9a4`  
		Last Modified: Tue, 09 Sep 2025 00:38:27 GMT  
		Size: 2.9 MB (2856371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4eea43490b007b5564ee72dd410bc48fa888d26c7382c13b9819305dae04d1af`  
		Last Modified: Tue, 09 Sep 2025 00:38:28 GMT  
		Size: 16.2 KB (16213 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:latest` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:66d488bf0021b438816e299b886fbe5b07fb07cafda79e587129fb90b99fe1cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.9 MB (82885221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a9aabbff50fd92c964ac8504015912d94aff0605cae5e0d0ad9ed3efa04183f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 15 Aug 2025 14:37:23 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1759104000'
# Fri, 15 Aug 2025 14:37:23 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENV CHRONOGRAF_VERSION=1.10.8
# Fri, 15 Aug 2025 14:37:23 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 15 Aug 2025 14:37:23 GMT
VOLUME [/var/lib/chronograf]
# Fri, 15 Aug 2025 14:37:23 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:f4e51325a7cb57cd9ae67bd9540483838b96bf7c9b0bf18205d9d30819e9ca38`  
		Last Modified: Mon, 29 Sep 2025 23:34:17 GMT  
		Size: 28.1 MB (28102145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddb9beba0102cb8a016357eaaaab7036f79df6eb1af669946d5ccb3bb523757a`  
		Last Modified: Tue, 30 Sep 2025 00:15:10 GMT  
		Size: 7.7 MB (7691801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b79c2d997f11ab4e545898b7661ab47c8605c718eb81019294ffb2306a52e72`  
		Last Modified: Tue, 30 Sep 2025 00:15:29 GMT  
		Size: 47.1 MB (47066804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d8bdc8362426bc7a0b2c8c96df4436b4eeffcbadc60d6eddfb62d3b3daa3105`  
		Last Modified: Tue, 30 Sep 2025 00:15:11 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33806231fa81aa323170575a5229bf1cba922a82f2a5c1ff40e2cd64948a3d16`  
		Last Modified: Tue, 30 Sep 2025 00:15:11 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3497d1bd60a46456aec7c35fb956f57b6b433ba81f8249c3467882b40eea9664`  
		Last Modified: Tue, 30 Sep 2025 00:15:14 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:e386baa1528d15451d2e6312153a556a7eb1283fd44e7e25c61422eebf89ba2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2870581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ef63d0ec60521a6cc1e8c174d6de979d19937a2fe2777b143e1eb630b090b94`

```dockerfile
```

-	Layers:
	-	`sha256:e8d775b5048f14c0c446e01d800fa9b9e087615e5f69f74fc49e22c5645fcf1a`  
		Last Modified: Wed, 01 Oct 2025 12:38:24 GMT  
		Size: 2.9 MB (2854347 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b365ac64465a8ae692b8dce815e49856ade9437224141f848a34efb94c20330c`  
		Last Modified: Wed, 01 Oct 2025 12:38:25 GMT  
		Size: 16.2 KB (16234 bytes)  
		MIME: application/vnd.in-toto+json
