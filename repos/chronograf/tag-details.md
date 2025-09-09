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
$ docker pull chronograf@sha256:6158ba6535c6e5304450d2875f24a246794f365638e3c3ad9c13e5ea24c2b35f
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
$ docker pull chronograf@sha256:ed2de1f89c27c85485c48689033a698b0605588cb5f71eccde4db80a149399f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.4 MB (85408147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d8671e516fd5ceb578dcb8b71097cf5249b6b5f21af2445d928a0ad8226c9d9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 15 Aug 2025 14:37:23 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
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
	-	`sha256:d107e437f7299a0db6425d4e37f44fa779f7917ecc8daf1e87128ee91b9ed3d3`  
		Last Modified: Mon, 08 Sep 2025 21:12:45 GMT  
		Size: 28.2 MB (28228346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8ec1264b746b5ed836d125ad5b3fcd9c90a8323d3d8cefe59b01e7cc3a15ed4`  
		Last Modified: Mon, 08 Sep 2025 21:38:57 GMT  
		Size: 7.9 MB (7878747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8aace19f075d228f9fc42f2c96ff91ef59d9b339fcfdf5b6fcc9e377b646dc9`  
		Last Modified: Mon, 08 Sep 2025 21:38:59 GMT  
		Size: 49.3 MB (49276591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94a65b76654b92ef3489059af6a84dc57c0f015cb6b5ee975d5fb23a3ca3a109`  
		Last Modified: Mon, 08 Sep 2025 21:38:57 GMT  
		Size: 12.2 KB (12244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6128e21eb224cbfb37847c80019417e069fb5cb48829689fdfc170fcc6d4c76`  
		Last Modified: Mon, 08 Sep 2025 21:38:59 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb5e3c90c0b42db2c538517099569edea486783085d095a0dbbe4b7c712e17c3`  
		Last Modified: Mon, 08 Sep 2025 21:38:58 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:5ca3c3d6e06f2a8c499d66a38ca2ed28076f30d81fe198b2627605823d284b77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2870202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c9674b2e72e1acc7e97fa4b55b594f89639168359987cea79a22935bdcba22f`

```dockerfile
```

-	Layers:
	-	`sha256:be51c01c98535ab6baa072f2fd65a79f7f2ad2e752a3cb788ae3e957de621830`  
		Last Modified: Mon, 08 Sep 2025 21:38:40 GMT  
		Size: 2.9 MB (2854074 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e66f417756fb1ecacbcb0a30b675c468cf91fe90cb86662dd4fe226aa5f4ceb0`  
		Last Modified: Mon, 08 Sep 2025 21:38:41 GMT  
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
$ docker pull chronograf@sha256:d50127f59f3fa0a96ed4bb4e64416110f05b18512a02629097b751a1ba725573
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.9 MB (82885055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81c6863f0df00eea2daeba084da0b6c7cb82a54b053cde50495f85311ef632b6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 15 Aug 2025 14:37:23 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1757289600'
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
	-	`sha256:0878ecc8b0afd0d835641c015541aacd4780ec19e5565a3e1a5af3f77d208d42`  
		Last Modified: Mon, 08 Sep 2025 21:13:25 GMT  
		Size: 28.1 MB (28102099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d78cfe50a3e7a025a01a1ca761aefd05be3111851fbad03f6482905c3357c59`  
		Last Modified: Tue, 09 Sep 2025 00:43:18 GMT  
		Size: 7.7 MB (7691791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a031f751001fec7ce32cfc1d9e63bafec921a9c9687276ccebc0742de646939c`  
		Last Modified: Tue, 09 Sep 2025 00:43:20 GMT  
		Size: 47.1 MB (47066700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c535dfa97dea8fa10cd9684a5c6f9f2361179e71718eb56e8357e14cbf92ef52`  
		Last Modified: Mon, 08 Sep 2025 22:08:06 GMT  
		Size: 12.2 KB (12242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b583dc93ca578194a6dca62139a2b7a050a0225b82cd5b4417931be4fce6efd1`  
		Last Modified: Mon, 08 Sep 2025 22:08:10 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d030b49489a2aee46f57778cbc8146c2a7fb66a06525360748c5fa9d58ff8a5`  
		Last Modified: Mon, 08 Sep 2025 22:08:13 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:3ea2aa364bb8adaffb28ab961ba651e5740d658b4b7faa9d33b65c97b7dd8722
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2870582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbf7e8000136a9588f534a0da00e67ee0e98dc788013b149aff1a50ecfebec8b`

```dockerfile
```

-	Layers:
	-	`sha256:566395eef78e722d7dca8fa6fbfeb4244ac6740ce8e2daed5173a2005e54294f`  
		Last Modified: Tue, 09 Sep 2025 00:38:32 GMT  
		Size: 2.9 MB (2854347 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed96c7718f7e1a8efd5c46ec88f5c59bc9703641dd4747eb6c3cf6683e09488d`  
		Last Modified: Tue, 09 Sep 2025 00:38:33 GMT  
		Size: 16.2 KB (16235 bytes)  
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
$ docker pull chronograf@sha256:6158ba6535c6e5304450d2875f24a246794f365638e3c3ad9c13e5ea24c2b35f
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
$ docker pull chronograf@sha256:ed2de1f89c27c85485c48689033a698b0605588cb5f71eccde4db80a149399f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.4 MB (85408147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d8671e516fd5ceb578dcb8b71097cf5249b6b5f21af2445d928a0ad8226c9d9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 15 Aug 2025 14:37:23 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
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
	-	`sha256:d107e437f7299a0db6425d4e37f44fa779f7917ecc8daf1e87128ee91b9ed3d3`  
		Last Modified: Mon, 08 Sep 2025 21:12:45 GMT  
		Size: 28.2 MB (28228346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8ec1264b746b5ed836d125ad5b3fcd9c90a8323d3d8cefe59b01e7cc3a15ed4`  
		Last Modified: Mon, 08 Sep 2025 21:38:57 GMT  
		Size: 7.9 MB (7878747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8aace19f075d228f9fc42f2c96ff91ef59d9b339fcfdf5b6fcc9e377b646dc9`  
		Last Modified: Mon, 08 Sep 2025 21:38:59 GMT  
		Size: 49.3 MB (49276591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94a65b76654b92ef3489059af6a84dc57c0f015cb6b5ee975d5fb23a3ca3a109`  
		Last Modified: Mon, 08 Sep 2025 21:38:57 GMT  
		Size: 12.2 KB (12244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6128e21eb224cbfb37847c80019417e069fb5cb48829689fdfc170fcc6d4c76`  
		Last Modified: Mon, 08 Sep 2025 21:38:59 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb5e3c90c0b42db2c538517099569edea486783085d095a0dbbe4b7c712e17c3`  
		Last Modified: Mon, 08 Sep 2025 21:38:58 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10.8` - unknown; unknown

```console
$ docker pull chronograf@sha256:5ca3c3d6e06f2a8c499d66a38ca2ed28076f30d81fe198b2627605823d284b77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2870202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c9674b2e72e1acc7e97fa4b55b594f89639168359987cea79a22935bdcba22f`

```dockerfile
```

-	Layers:
	-	`sha256:be51c01c98535ab6baa072f2fd65a79f7f2ad2e752a3cb788ae3e957de621830`  
		Last Modified: Mon, 08 Sep 2025 21:38:40 GMT  
		Size: 2.9 MB (2854074 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e66f417756fb1ecacbcb0a30b675c468cf91fe90cb86662dd4fe226aa5f4ceb0`  
		Last Modified: Mon, 08 Sep 2025 21:38:41 GMT  
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
$ docker pull chronograf@sha256:d50127f59f3fa0a96ed4bb4e64416110f05b18512a02629097b751a1ba725573
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.9 MB (82885055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81c6863f0df00eea2daeba084da0b6c7cb82a54b053cde50495f85311ef632b6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 15 Aug 2025 14:37:23 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1757289600'
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
	-	`sha256:0878ecc8b0afd0d835641c015541aacd4780ec19e5565a3e1a5af3f77d208d42`  
		Last Modified: Mon, 08 Sep 2025 21:13:25 GMT  
		Size: 28.1 MB (28102099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d78cfe50a3e7a025a01a1ca761aefd05be3111851fbad03f6482905c3357c59`  
		Last Modified: Tue, 09 Sep 2025 00:43:18 GMT  
		Size: 7.7 MB (7691791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a031f751001fec7ce32cfc1d9e63bafec921a9c9687276ccebc0742de646939c`  
		Last Modified: Tue, 09 Sep 2025 00:43:20 GMT  
		Size: 47.1 MB (47066700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c535dfa97dea8fa10cd9684a5c6f9f2361179e71718eb56e8357e14cbf92ef52`  
		Last Modified: Mon, 08 Sep 2025 22:08:06 GMT  
		Size: 12.2 KB (12242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b583dc93ca578194a6dca62139a2b7a050a0225b82cd5b4417931be4fce6efd1`  
		Last Modified: Mon, 08 Sep 2025 22:08:10 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d030b49489a2aee46f57778cbc8146c2a7fb66a06525360748c5fa9d58ff8a5`  
		Last Modified: Mon, 08 Sep 2025 22:08:13 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10.8` - unknown; unknown

```console
$ docker pull chronograf@sha256:3ea2aa364bb8adaffb28ab961ba651e5740d658b4b7faa9d33b65c97b7dd8722
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2870582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbf7e8000136a9588f534a0da00e67ee0e98dc788013b149aff1a50ecfebec8b`

```dockerfile
```

-	Layers:
	-	`sha256:566395eef78e722d7dca8fa6fbfeb4244ac6740ce8e2daed5173a2005e54294f`  
		Last Modified: Tue, 09 Sep 2025 00:38:32 GMT  
		Size: 2.9 MB (2854347 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed96c7718f7e1a8efd5c46ec88f5c59bc9703641dd4747eb6c3cf6683e09488d`  
		Last Modified: Tue, 09 Sep 2025 00:38:33 GMT  
		Size: 16.2 KB (16235 bytes)  
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
$ docker pull chronograf@sha256:1f3fd5d6816860f644ad629e0ce7cb96170e33e66440e5744293660adb6baae6
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
$ docker pull chronograf@sha256:157391a0370d02ee0ddc8936f00821c37a7e5422d2c8de2321bf604a8ca47a7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.2 MB (69229590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27a41e47a40cc755e317628edd793c6c4e0fab07623728374c234299999123b1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 15 Aug 2025 14:37:23 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1757289600'
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
	-	`sha256:456a3213e1b1f193dc759cd05f6f8422428b8c4bd45ef40fbf41ba43bdce8570`  
		Last Modified: Mon, 08 Sep 2025 21:12:48 GMT  
		Size: 30.3 MB (30256068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d14ea3166335c41d0effc8a3d1323dfec852f2ec2e1a88b526eed7282abc684`  
		Last Modified: Mon, 08 Sep 2025 21:41:04 GMT  
		Size: 4.2 MB (4209357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60c29360a3f4e2bc51ac10ba89baa8d9b1b5cd4e440f0d4105ec4014585cb699`  
		Last Modified: Mon, 08 Sep 2025 21:41:06 GMT  
		Size: 34.7 MB (34739766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0b19eb8817cbb306e899db1e9605f0ce65878915e237ad348cb52246a549060`  
		Last Modified: Mon, 08 Sep 2025 21:41:05 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2915a1f721440b82e55fd0a6d712602aa3f30d5b171c90f290f4457238c1cc1`  
		Last Modified: Mon, 08 Sep 2025 21:41:05 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:131a60a4d86cf7d3a563a680947862d710863d2418e80c8a1d260420e8581800`  
		Last Modified: Mon, 08 Sep 2025 21:41:06 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7` - unknown; unknown

```console
$ docker pull chronograf@sha256:8bd2cd9434279c360fcd74e53c139c1233bb2f9cbab67c04f95103321cbaed1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3064650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32f129f2d9cdde902f14cce40505b72398cdaf26511a0145ad0cf6385528b05c`

```dockerfile
```

-	Layers:
	-	`sha256:6f6a32eb47f28daff166cb87d1095b70f8a5151066774acc0b1546f818912bc5`  
		Last Modified: Mon, 08 Sep 2025 21:38:48 GMT  
		Size: 3.0 MB (3048873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0bd4299da8ade70dcc37c2650b8eadce52917eafc3e5dec550f1e68aacf383ef`  
		Last Modified: Mon, 08 Sep 2025 21:38:49 GMT  
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
		Last Modified: Mon, 08 Sep 2025 22:29:14 GMT  
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
$ docker pull chronograf@sha256:8a3431ba1360b04767642ef5a79d70ae786714d9a893e80edf2463967c884768
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66224739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cd319dce31638941b0d4e583abdd073a674b5b8a29eb5dc05ebb5979f6474a7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 15 Aug 2025 14:37:23 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1757289600'
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
	-	`sha256:8568e9af3ab25a29d98aac9a07896467a19253e72e5be0cf09cd3982ac4444d0`  
		Last Modified: Mon, 08 Sep 2025 21:15:52 GMT  
		Size: 28.8 MB (28750457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41f4c66095dd4e1f308034dc9f36a7a84d0271fd1c49428f4dd199b83c1d1afc`  
		Last Modified: Tue, 09 Sep 2025 01:57:23 GMT  
		Size: 4.2 MB (4210585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b1c4f575c529a9f38433229187d5fe34f0f03e6de1eb41e82d3478cf7f67707`  
		Last Modified: Mon, 08 Sep 2025 21:40:27 GMT  
		Size: 33.2 MB (33239316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ab7ba06cb4e168960fe0a5521be35c6191d44920239fb70e6c9adf4c4c8a52`  
		Last Modified: Mon, 08 Sep 2025 22:08:06 GMT  
		Size: 12.2 KB (12242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c53241f82d2442db1bba12c81af619573fb5feeaa57b8d63effd478a3e6dca3`  
		Last Modified: Mon, 08 Sep 2025 22:08:09 GMT  
		Size: 11.9 KB (11901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:764a5841e0d748f1f0ad769200cdf761b9fac7b96d23fd9a7ef680bfceb2bb2d`  
		Last Modified: Mon, 08 Sep 2025 22:08:13 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7` - unknown; unknown

```console
$ docker pull chronograf@sha256:67c3afb4fd838647628944b9885556d99386d89a48c1301de857af9ca97b64c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3064994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6231401d48b6bb72cc06d52d365ad21295bab88c2ad6b0140b884f7d8c8e4720`

```dockerfile
```

-	Layers:
	-	`sha256:5428fe63a58b92e1f2cec6cb2535afc180ed327602a2add7036c984b0e7a97e9`  
		Last Modified: Tue, 09 Sep 2025 00:38:43 GMT  
		Size: 3.0 MB (3049122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27526e17ed608ff61380d020afdb9c262e9c3fbe3760230838343c9bff29a6fa`  
		Last Modified: Tue, 09 Sep 2025 00:38:44 GMT  
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
$ docker pull chronograf@sha256:1f3fd5d6816860f644ad629e0ce7cb96170e33e66440e5744293660adb6baae6
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
$ docker pull chronograf@sha256:157391a0370d02ee0ddc8936f00821c37a7e5422d2c8de2321bf604a8ca47a7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.2 MB (69229590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27a41e47a40cc755e317628edd793c6c4e0fab07623728374c234299999123b1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 15 Aug 2025 14:37:23 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1757289600'
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
	-	`sha256:456a3213e1b1f193dc759cd05f6f8422428b8c4bd45ef40fbf41ba43bdce8570`  
		Last Modified: Mon, 08 Sep 2025 21:12:48 GMT  
		Size: 30.3 MB (30256068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d14ea3166335c41d0effc8a3d1323dfec852f2ec2e1a88b526eed7282abc684`  
		Last Modified: Mon, 08 Sep 2025 21:41:04 GMT  
		Size: 4.2 MB (4209357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60c29360a3f4e2bc51ac10ba89baa8d9b1b5cd4e440f0d4105ec4014585cb699`  
		Last Modified: Mon, 08 Sep 2025 21:41:06 GMT  
		Size: 34.7 MB (34739766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0b19eb8817cbb306e899db1e9605f0ce65878915e237ad348cb52246a549060`  
		Last Modified: Mon, 08 Sep 2025 21:41:05 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2915a1f721440b82e55fd0a6d712602aa3f30d5b171c90f290f4457238c1cc1`  
		Last Modified: Mon, 08 Sep 2025 21:41:05 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:131a60a4d86cf7d3a563a680947862d710863d2418e80c8a1d260420e8581800`  
		Last Modified: Mon, 08 Sep 2025 21:41:06 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7.17` - unknown; unknown

```console
$ docker pull chronograf@sha256:8bd2cd9434279c360fcd74e53c139c1233bb2f9cbab67c04f95103321cbaed1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3064650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32f129f2d9cdde902f14cce40505b72398cdaf26511a0145ad0cf6385528b05c`

```dockerfile
```

-	Layers:
	-	`sha256:6f6a32eb47f28daff166cb87d1095b70f8a5151066774acc0b1546f818912bc5`  
		Last Modified: Mon, 08 Sep 2025 21:38:48 GMT  
		Size: 3.0 MB (3048873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0bd4299da8ade70dcc37c2650b8eadce52917eafc3e5dec550f1e68aacf383ef`  
		Last Modified: Mon, 08 Sep 2025 21:38:49 GMT  
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
		Last Modified: Mon, 08 Sep 2025 22:29:14 GMT  
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
$ docker pull chronograf@sha256:8a3431ba1360b04767642ef5a79d70ae786714d9a893e80edf2463967c884768
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66224739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cd319dce31638941b0d4e583abdd073a674b5b8a29eb5dc05ebb5979f6474a7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 15 Aug 2025 14:37:23 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1757289600'
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
	-	`sha256:8568e9af3ab25a29d98aac9a07896467a19253e72e5be0cf09cd3982ac4444d0`  
		Last Modified: Mon, 08 Sep 2025 21:15:52 GMT  
		Size: 28.8 MB (28750457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41f4c66095dd4e1f308034dc9f36a7a84d0271fd1c49428f4dd199b83c1d1afc`  
		Last Modified: Tue, 09 Sep 2025 01:57:23 GMT  
		Size: 4.2 MB (4210585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b1c4f575c529a9f38433229187d5fe34f0f03e6de1eb41e82d3478cf7f67707`  
		Last Modified: Mon, 08 Sep 2025 21:40:27 GMT  
		Size: 33.2 MB (33239316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ab7ba06cb4e168960fe0a5521be35c6191d44920239fb70e6c9adf4c4c8a52`  
		Last Modified: Mon, 08 Sep 2025 22:08:06 GMT  
		Size: 12.2 KB (12242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c53241f82d2442db1bba12c81af619573fb5feeaa57b8d63effd478a3e6dca3`  
		Last Modified: Mon, 08 Sep 2025 22:08:09 GMT  
		Size: 11.9 KB (11901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:764a5841e0d748f1f0ad769200cdf761b9fac7b96d23fd9a7ef680bfceb2bb2d`  
		Last Modified: Mon, 08 Sep 2025 22:08:13 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7.17` - unknown; unknown

```console
$ docker pull chronograf@sha256:67c3afb4fd838647628944b9885556d99386d89a48c1301de857af9ca97b64c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3064994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6231401d48b6bb72cc06d52d365ad21295bab88c2ad6b0140b884f7d8c8e4720`

```dockerfile
```

-	Layers:
	-	`sha256:5428fe63a58b92e1f2cec6cb2535afc180ed327602a2add7036c984b0e7a97e9`  
		Last Modified: Tue, 09 Sep 2025 00:38:43 GMT  
		Size: 3.0 MB (3049122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27526e17ed608ff61380d020afdb9c262e9c3fbe3760230838343c9bff29a6fa`  
		Last Modified: Tue, 09 Sep 2025 00:38:44 GMT  
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
$ docker pull chronograf@sha256:4854f703f8e6747d4a3a2a42e0f3c67ef1535e46c85657cb18c8d0989b6a4312
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
$ docker pull chronograf@sha256:bfdba387c16a5f25c76e957ff834d4d58c4ba134d9613bad2a69d88de647e2e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69870718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72b55d6ed12845d00b02870fb2bcae52024807204c7a05f8d4fe1c32fc02cb28`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 15 Aug 2025 14:37:23 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1757289600'
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
	-	`sha256:456a3213e1b1f193dc759cd05f6f8422428b8c4bd45ef40fbf41ba43bdce8570`  
		Last Modified: Mon, 08 Sep 2025 21:12:48 GMT  
		Size: 30.3 MB (30256068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b8977671e2d0d8dde43fed5eac039e292ccd764b24ff7f1683c008749815940`  
		Last Modified: Mon, 08 Sep 2025 21:39:04 GMT  
		Size: 5.2 MB (5225966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46de114f415d32c495ace51be894d6e89b63ac25a4eaab8d813f17da707d14a0`  
		Last Modified: Mon, 08 Sep 2025 21:39:07 GMT  
		Size: 34.4 MB (34364303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0eb964f1e38fc499d29619a463db05538bfcfb021649c44f2712f5459397dc8`  
		Last Modified: Mon, 08 Sep 2025 21:39:04 GMT  
		Size: 12.2 KB (12242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c57c3abdf5ffeefd3cd49873b7b806d2a30f3b6c72f81a260ca17ac3fb15b4c`  
		Last Modified: Mon, 08 Sep 2025 21:39:06 GMT  
		Size: 11.9 KB (11900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0c813ce3fdedd8ef47b10c81d2078908765c868d5c3c51ebb175597664b0652`  
		Last Modified: Mon, 08 Sep 2025 21:39:06 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8` - unknown; unknown

```console
$ docker pull chronograf@sha256:67e2932dabcad8004fa801fcefcaa279fd7f2f2ff1f8531dab7e38fbf307a4ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3120328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38b0289672ea7bd8d260450355e33b7c66cc366c1a3acce58109b540f81646e6`

```dockerfile
```

-	Layers:
	-	`sha256:3b3ac202fb4816ec528a4868048c4adf10a8729365f3a844f9010c512dea03a2`  
		Last Modified: Mon, 08 Sep 2025 21:39:02 GMT  
		Size: 3.1 MB (3104511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6dc22f9883b102397c3a6ce8feadad489a92f662befb4b3bb00f823471ab6384`  
		Last Modified: Mon, 08 Sep 2025 21:39:04 GMT  
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
		Last Modified: Mon, 08 Sep 2025 22:29:53 GMT  
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
$ docker pull chronograf@sha256:d63edd50cfd3a0f1f8c52bcad3d66705d174ecddcfc653379871eaa676b34637
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.4 MB (66413752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4f2ccaaf5a21be9c86034a94f9bc07deadcd8259ae4afbae76a749bc06ac448`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 15 Aug 2025 14:37:23 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1757289600'
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
	-	`sha256:8568e9af3ab25a29d98aac9a07896467a19253e72e5be0cf09cd3982ac4444d0`  
		Last Modified: Mon, 08 Sep 2025 21:15:52 GMT  
		Size: 28.8 MB (28750457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47296e0cce69e590c4d9b4cf6a667622c969c32dc79b705b737202b1bf36b945`  
		Last Modified: Tue, 09 Sep 2025 01:54:38 GMT  
		Size: 5.2 MB (5209376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f7c900935bcedfd12b6ce82ee7ac24951e6040ea7c4c54e54729943d99918c5`  
		Last Modified: Mon, 08 Sep 2025 21:40:33 GMT  
		Size: 32.4 MB (32429531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9ac9f8c252cadfb7213594f6af04bb5f75f250cf1d6d5a557c7264caa5e6c71`  
		Last Modified: Mon, 08 Sep 2025 22:08:10 GMT  
		Size: 12.2 KB (12244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef853661cb122a0e63325d090ddbb752d431ba40ff1b2f33e1c2271ed2f62802`  
		Last Modified: Mon, 08 Sep 2025 22:08:14 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64fc71ae27e55d74871de52c712ed04ede7163a3597a49264ad4979098e4dc3b`  
		Last Modified: Mon, 08 Sep 2025 22:08:17 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8` - unknown; unknown

```console
$ docker pull chronograf@sha256:d2807b125285828f41e2863dcc065c3b04c0ded47272f57e2764f145dcb48d40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3120672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4aa51d303e4b7c3e15637f01b4e2aaf8d30f0f67c6db27fb66390fa8c9b1dfc`

```dockerfile
```

-	Layers:
	-	`sha256:ad95d673d9640943bdf71939c60ae68a3089ec20fa3453ca43b5c1fe7ca17e54`  
		Last Modified: Tue, 09 Sep 2025 00:38:53 GMT  
		Size: 3.1 MB (3104760 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5d22fcc079c34928c9e4e85dab03e7e04ebc6750f7664e568588cb55fca74a7`  
		Last Modified: Tue, 09 Sep 2025 00:38:54 GMT  
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
$ docker pull chronograf@sha256:4854f703f8e6747d4a3a2a42e0f3c67ef1535e46c85657cb18c8d0989b6a4312
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
$ docker pull chronograf@sha256:bfdba387c16a5f25c76e957ff834d4d58c4ba134d9613bad2a69d88de647e2e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69870718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72b55d6ed12845d00b02870fb2bcae52024807204c7a05f8d4fe1c32fc02cb28`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 15 Aug 2025 14:37:23 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1757289600'
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
	-	`sha256:456a3213e1b1f193dc759cd05f6f8422428b8c4bd45ef40fbf41ba43bdce8570`  
		Last Modified: Mon, 08 Sep 2025 21:12:48 GMT  
		Size: 30.3 MB (30256068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b8977671e2d0d8dde43fed5eac039e292ccd764b24ff7f1683c008749815940`  
		Last Modified: Mon, 08 Sep 2025 21:39:04 GMT  
		Size: 5.2 MB (5225966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46de114f415d32c495ace51be894d6e89b63ac25a4eaab8d813f17da707d14a0`  
		Last Modified: Mon, 08 Sep 2025 21:39:07 GMT  
		Size: 34.4 MB (34364303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0eb964f1e38fc499d29619a463db05538bfcfb021649c44f2712f5459397dc8`  
		Last Modified: Mon, 08 Sep 2025 21:39:04 GMT  
		Size: 12.2 KB (12242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c57c3abdf5ffeefd3cd49873b7b806d2a30f3b6c72f81a260ca17ac3fb15b4c`  
		Last Modified: Mon, 08 Sep 2025 21:39:06 GMT  
		Size: 11.9 KB (11900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0c813ce3fdedd8ef47b10c81d2078908765c868d5c3c51ebb175597664b0652`  
		Last Modified: Mon, 08 Sep 2025 21:39:06 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:67e2932dabcad8004fa801fcefcaa279fd7f2f2ff1f8531dab7e38fbf307a4ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3120328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38b0289672ea7bd8d260450355e33b7c66cc366c1a3acce58109b540f81646e6`

```dockerfile
```

-	Layers:
	-	`sha256:3b3ac202fb4816ec528a4868048c4adf10a8729365f3a844f9010c512dea03a2`  
		Last Modified: Mon, 08 Sep 2025 21:39:02 GMT  
		Size: 3.1 MB (3104511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6dc22f9883b102397c3a6ce8feadad489a92f662befb4b3bb00f823471ab6384`  
		Last Modified: Mon, 08 Sep 2025 21:39:04 GMT  
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
		Last Modified: Mon, 08 Sep 2025 22:29:53 GMT  
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
$ docker pull chronograf@sha256:d63edd50cfd3a0f1f8c52bcad3d66705d174ecddcfc653379871eaa676b34637
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.4 MB (66413752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4f2ccaaf5a21be9c86034a94f9bc07deadcd8259ae4afbae76a749bc06ac448`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 15 Aug 2025 14:37:23 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1757289600'
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
	-	`sha256:8568e9af3ab25a29d98aac9a07896467a19253e72e5be0cf09cd3982ac4444d0`  
		Last Modified: Mon, 08 Sep 2025 21:15:52 GMT  
		Size: 28.8 MB (28750457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47296e0cce69e590c4d9b4cf6a667622c969c32dc79b705b737202b1bf36b945`  
		Last Modified: Tue, 09 Sep 2025 01:54:38 GMT  
		Size: 5.2 MB (5209376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f7c900935bcedfd12b6ce82ee7ac24951e6040ea7c4c54e54729943d99918c5`  
		Last Modified: Mon, 08 Sep 2025 21:40:33 GMT  
		Size: 32.4 MB (32429531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9ac9f8c252cadfb7213594f6af04bb5f75f250cf1d6d5a557c7264caa5e6c71`  
		Last Modified: Mon, 08 Sep 2025 22:08:10 GMT  
		Size: 12.2 KB (12244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef853661cb122a0e63325d090ddbb752d431ba40ff1b2f33e1c2271ed2f62802`  
		Last Modified: Mon, 08 Sep 2025 22:08:14 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64fc71ae27e55d74871de52c712ed04ede7163a3597a49264ad4979098e4dc3b`  
		Last Modified: Mon, 08 Sep 2025 22:08:17 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:d2807b125285828f41e2863dcc065c3b04c0ded47272f57e2764f145dcb48d40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3120672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4aa51d303e4b7c3e15637f01b4e2aaf8d30f0f67c6db27fb66390fa8c9b1dfc`

```dockerfile
```

-	Layers:
	-	`sha256:ad95d673d9640943bdf71939c60ae68a3089ec20fa3453ca43b5c1fe7ca17e54`  
		Last Modified: Tue, 09 Sep 2025 00:38:53 GMT  
		Size: 3.1 MB (3104760 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5d22fcc079c34928c9e4e85dab03e7e04ebc6750f7664e568588cb55fca74a7`  
		Last Modified: Tue, 09 Sep 2025 00:38:54 GMT  
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
$ docker pull chronograf@sha256:101c727cd8d24853627732771d1b8b5e6cab07c9e91c6341834c722a5bc2e152
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
$ docker pull chronograf@sha256:0f57c7f9299927eb005794c54bca2aebf9027786708fbcdb29099e1416e3a587
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.5 MB (70518095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5545487d126d5798e44c45da05733f68667b22f146f3cc7a20e1aa9fb347ebc6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 15 Aug 2025 14:37:23 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1757289600'
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
	-	`sha256:456a3213e1b1f193dc759cd05f6f8422428b8c4bd45ef40fbf41ba43bdce8570`  
		Last Modified: Mon, 08 Sep 2025 21:12:48 GMT  
		Size: 30.3 MB (30256068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5d0bdbc2db0f7a54fcbfcd8acdc63e1a6c35127b233965cdd5c4cc087a0c459`  
		Last Modified: Mon, 08 Sep 2025 22:06:54 GMT  
		Size: 5.2 MB (5225927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a81ea78af25ff906fa2373e31b87c34b70b489971730d1bbdc88025d1adc4a2`  
		Last Modified: Mon, 08 Sep 2025 22:06:57 GMT  
		Size: 35.0 MB (35011714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad382df32fef5f7ed2fab2984797c85bae5ffadc0976e22402f8ca8e88388ed9`  
		Last Modified: Mon, 08 Sep 2025 21:47:09 GMT  
		Size: 12.2 KB (12244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f28d46b4526469d52560eaa8aadf03dd0d6ccaeec24574d8fa6a8957994d831`  
		Last Modified: Mon, 08 Sep 2025 21:47:13 GMT  
		Size: 11.9 KB (11902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fae4843896d535a9baf2a30b52a5867f4637f7ca1391057ea2d5d64c2e860dd6`  
		Last Modified: Mon, 08 Sep 2025 21:47:19 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9` - unknown; unknown

```console
$ docker pull chronograf@sha256:c223d3eb3757ccbcfa1cd6239e6f9274aec925cddc2efca7567d094797ed7e40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3125531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4930cc6cf8b6f4984b5f5a5eb0e400b104d9d180e75e5f141d4febf52d4b2b5`

```dockerfile
```

-	Layers:
	-	`sha256:ebe7fad8133f88e8ccde72a4ba3b019395c577c6b177b5d09dd454efa75adcca`  
		Last Modified: Mon, 08 Sep 2025 21:39:09 GMT  
		Size: 3.1 MB (3109721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6cd3d1453da38a58be846537844bf7c11d64e294a775dc54407fd27978148df`  
		Last Modified: Mon, 08 Sep 2025 21:39:10 GMT  
		Size: 15.8 KB (15810 bytes)  
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
		Last Modified: Mon, 08 Sep 2025 22:30:42 GMT  
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
$ docker pull chronograf@sha256:01143b2ce10abbde57b481020c145038a86bbcb0b0396ac6db22736855de6933
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.2 MB (67166375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6fec2925f552db01ebcc18d933f6c45dd77532de684b8ed6c2fab46c77af5be`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 15 Aug 2025 14:37:23 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1757289600'
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
	-	`sha256:8568e9af3ab25a29d98aac9a07896467a19253e72e5be0cf09cd3982ac4444d0`  
		Last Modified: Mon, 08 Sep 2025 21:15:52 GMT  
		Size: 28.8 MB (28750457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a45336fc4edbd9b0be4e819c200cf72ed8056dd673f45edd1464001eb9de84c`  
		Last Modified: Mon, 08 Sep 2025 22:31:49 GMT  
		Size: 5.2 MB (5209377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:942cbfb347f28b3295be6676c8fe8368e094fbb4ebd922da0490cc9443440fdc`  
		Last Modified: Mon, 08 Sep 2025 22:31:39 GMT  
		Size: 33.2 MB (33182141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17751d7e2d5166230421fa00123922950ec6e6f4741c3a39a4a7883f9bb13938`  
		Last Modified: Mon, 08 Sep 2025 22:08:08 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0764c1188073e3b47122505f4a89a7051efd765b3c1e7c0c17eab85139e56400`  
		Last Modified: Mon, 08 Sep 2025 22:08:12 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d75031e34552adb5a87179bf86a57e39eace1b07c1955b56e56503ae1cb44f3`  
		Last Modified: Mon, 08 Sep 2025 22:08:16 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9` - unknown; unknown

```console
$ docker pull chronograf@sha256:1583b2e87578a34be48db80f4eef7bc1c96b9213b8f145cd80e17137e3221e81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3125875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c736dcdf6c59daec6031029e3071d04ec21a4a319a4afbd5b42d8f8ade62e5ab`

```dockerfile
```

-	Layers:
	-	`sha256:df3887d01e81d62a0dce719e4be00eba5dff66abf57f660a03fe558718d5b4cf`  
		Last Modified: Tue, 09 Sep 2025 00:39:10 GMT  
		Size: 3.1 MB (3109970 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b3ce2230f367843c66736469ddcc9052f2f98ebfd1b3ba68f588a59416acbc4`  
		Last Modified: Tue, 09 Sep 2025 00:39:10 GMT  
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
$ docker pull chronograf@sha256:101c727cd8d24853627732771d1b8b5e6cab07c9e91c6341834c722a5bc2e152
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
$ docker pull chronograf@sha256:0f57c7f9299927eb005794c54bca2aebf9027786708fbcdb29099e1416e3a587
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.5 MB (70518095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5545487d126d5798e44c45da05733f68667b22f146f3cc7a20e1aa9fb347ebc6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 15 Aug 2025 14:37:23 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1757289600'
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
	-	`sha256:456a3213e1b1f193dc759cd05f6f8422428b8c4bd45ef40fbf41ba43bdce8570`  
		Last Modified: Mon, 08 Sep 2025 21:12:48 GMT  
		Size: 30.3 MB (30256068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5d0bdbc2db0f7a54fcbfcd8acdc63e1a6c35127b233965cdd5c4cc087a0c459`  
		Last Modified: Mon, 08 Sep 2025 22:06:54 GMT  
		Size: 5.2 MB (5225927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a81ea78af25ff906fa2373e31b87c34b70b489971730d1bbdc88025d1adc4a2`  
		Last Modified: Mon, 08 Sep 2025 22:06:57 GMT  
		Size: 35.0 MB (35011714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad382df32fef5f7ed2fab2984797c85bae5ffadc0976e22402f8ca8e88388ed9`  
		Last Modified: Mon, 08 Sep 2025 21:47:09 GMT  
		Size: 12.2 KB (12244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f28d46b4526469d52560eaa8aadf03dd0d6ccaeec24574d8fa6a8957994d831`  
		Last Modified: Mon, 08 Sep 2025 21:47:13 GMT  
		Size: 11.9 KB (11902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fae4843896d535a9baf2a30b52a5867f4637f7ca1391057ea2d5d64c2e860dd6`  
		Last Modified: Mon, 08 Sep 2025 21:47:19 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9.4` - unknown; unknown

```console
$ docker pull chronograf@sha256:c223d3eb3757ccbcfa1cd6239e6f9274aec925cddc2efca7567d094797ed7e40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3125531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4930cc6cf8b6f4984b5f5a5eb0e400b104d9d180e75e5f141d4febf52d4b2b5`

```dockerfile
```

-	Layers:
	-	`sha256:ebe7fad8133f88e8ccde72a4ba3b019395c577c6b177b5d09dd454efa75adcca`  
		Last Modified: Mon, 08 Sep 2025 21:39:09 GMT  
		Size: 3.1 MB (3109721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6cd3d1453da38a58be846537844bf7c11d64e294a775dc54407fd27978148df`  
		Last Modified: Mon, 08 Sep 2025 21:39:10 GMT  
		Size: 15.8 KB (15810 bytes)  
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
		Last Modified: Mon, 08 Sep 2025 22:30:42 GMT  
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
$ docker pull chronograf@sha256:01143b2ce10abbde57b481020c145038a86bbcb0b0396ac6db22736855de6933
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.2 MB (67166375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6fec2925f552db01ebcc18d933f6c45dd77532de684b8ed6c2fab46c77af5be`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 15 Aug 2025 14:37:23 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1757289600'
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
	-	`sha256:8568e9af3ab25a29d98aac9a07896467a19253e72e5be0cf09cd3982ac4444d0`  
		Last Modified: Mon, 08 Sep 2025 21:15:52 GMT  
		Size: 28.8 MB (28750457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a45336fc4edbd9b0be4e819c200cf72ed8056dd673f45edd1464001eb9de84c`  
		Last Modified: Mon, 08 Sep 2025 22:31:49 GMT  
		Size: 5.2 MB (5209377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:942cbfb347f28b3295be6676c8fe8368e094fbb4ebd922da0490cc9443440fdc`  
		Last Modified: Mon, 08 Sep 2025 22:31:39 GMT  
		Size: 33.2 MB (33182141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17751d7e2d5166230421fa00123922950ec6e6f4741c3a39a4a7883f9bb13938`  
		Last Modified: Mon, 08 Sep 2025 22:08:08 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0764c1188073e3b47122505f4a89a7051efd765b3c1e7c0c17eab85139e56400`  
		Last Modified: Mon, 08 Sep 2025 22:08:12 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d75031e34552adb5a87179bf86a57e39eace1b07c1955b56e56503ae1cb44f3`  
		Last Modified: Mon, 08 Sep 2025 22:08:16 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9.4` - unknown; unknown

```console
$ docker pull chronograf@sha256:1583b2e87578a34be48db80f4eef7bc1c96b9213b8f145cd80e17137e3221e81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3125875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c736dcdf6c59daec6031029e3071d04ec21a4a319a4afbd5b42d8f8ade62e5ab`

```dockerfile
```

-	Layers:
	-	`sha256:df3887d01e81d62a0dce719e4be00eba5dff66abf57f660a03fe558718d5b4cf`  
		Last Modified: Tue, 09 Sep 2025 00:39:10 GMT  
		Size: 3.1 MB (3109970 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b3ce2230f367843c66736469ddcc9052f2f98ebfd1b3ba68f588a59416acbc4`  
		Last Modified: Tue, 09 Sep 2025 00:39:10 GMT  
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
$ docker pull chronograf@sha256:6158ba6535c6e5304450d2875f24a246794f365638e3c3ad9c13e5ea24c2b35f
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
$ docker pull chronograf@sha256:ed2de1f89c27c85485c48689033a698b0605588cb5f71eccde4db80a149399f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.4 MB (85408147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d8671e516fd5ceb578dcb8b71097cf5249b6b5f21af2445d928a0ad8226c9d9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 15 Aug 2025 14:37:23 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
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
	-	`sha256:d107e437f7299a0db6425d4e37f44fa779f7917ecc8daf1e87128ee91b9ed3d3`  
		Last Modified: Mon, 08 Sep 2025 21:12:45 GMT  
		Size: 28.2 MB (28228346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8ec1264b746b5ed836d125ad5b3fcd9c90a8323d3d8cefe59b01e7cc3a15ed4`  
		Last Modified: Mon, 08 Sep 2025 21:38:57 GMT  
		Size: 7.9 MB (7878747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8aace19f075d228f9fc42f2c96ff91ef59d9b339fcfdf5b6fcc9e377b646dc9`  
		Last Modified: Mon, 08 Sep 2025 21:38:59 GMT  
		Size: 49.3 MB (49276591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94a65b76654b92ef3489059af6a84dc57c0f015cb6b5ee975d5fb23a3ca3a109`  
		Last Modified: Mon, 08 Sep 2025 21:38:57 GMT  
		Size: 12.2 KB (12244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6128e21eb224cbfb37847c80019417e069fb5cb48829689fdfc170fcc6d4c76`  
		Last Modified: Mon, 08 Sep 2025 21:38:59 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb5e3c90c0b42db2c538517099569edea486783085d095a0dbbe4b7c712e17c3`  
		Last Modified: Mon, 08 Sep 2025 21:38:58 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:5ca3c3d6e06f2a8c499d66a38ca2ed28076f30d81fe198b2627605823d284b77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2870202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c9674b2e72e1acc7e97fa4b55b594f89639168359987cea79a22935bdcba22f`

```dockerfile
```

-	Layers:
	-	`sha256:be51c01c98535ab6baa072f2fd65a79f7f2ad2e752a3cb788ae3e957de621830`  
		Last Modified: Mon, 08 Sep 2025 21:38:40 GMT  
		Size: 2.9 MB (2854074 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e66f417756fb1ecacbcb0a30b675c468cf91fe90cb86662dd4fe226aa5f4ceb0`  
		Last Modified: Mon, 08 Sep 2025 21:38:41 GMT  
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
$ docker pull chronograf@sha256:d50127f59f3fa0a96ed4bb4e64416110f05b18512a02629097b751a1ba725573
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.9 MB (82885055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81c6863f0df00eea2daeba084da0b6c7cb82a54b053cde50495f85311ef632b6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 15 Aug 2025 14:37:23 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1757289600'
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
	-	`sha256:0878ecc8b0afd0d835641c015541aacd4780ec19e5565a3e1a5af3f77d208d42`  
		Last Modified: Mon, 08 Sep 2025 21:13:25 GMT  
		Size: 28.1 MB (28102099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d78cfe50a3e7a025a01a1ca761aefd05be3111851fbad03f6482905c3357c59`  
		Last Modified: Tue, 09 Sep 2025 00:43:18 GMT  
		Size: 7.7 MB (7691791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a031f751001fec7ce32cfc1d9e63bafec921a9c9687276ccebc0742de646939c`  
		Last Modified: Tue, 09 Sep 2025 00:43:20 GMT  
		Size: 47.1 MB (47066700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c535dfa97dea8fa10cd9684a5c6f9f2361179e71718eb56e8357e14cbf92ef52`  
		Last Modified: Mon, 08 Sep 2025 22:08:06 GMT  
		Size: 12.2 KB (12242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b583dc93ca578194a6dca62139a2b7a050a0225b82cd5b4417931be4fce6efd1`  
		Last Modified: Mon, 08 Sep 2025 22:08:10 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d030b49489a2aee46f57778cbc8146c2a7fb66a06525360748c5fa9d58ff8a5`  
		Last Modified: Mon, 08 Sep 2025 22:08:13 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:3ea2aa364bb8adaffb28ab961ba651e5740d658b4b7faa9d33b65c97b7dd8722
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2870582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbf7e8000136a9588f534a0da00e67ee0e98dc788013b149aff1a50ecfebec8b`

```dockerfile
```

-	Layers:
	-	`sha256:566395eef78e722d7dca8fa6fbfeb4244ac6740ce8e2daed5173a2005e54294f`  
		Last Modified: Tue, 09 Sep 2025 00:38:32 GMT  
		Size: 2.9 MB (2854347 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed96c7718f7e1a8efd5c46ec88f5c59bc9703641dd4747eb6c3cf6683e09488d`  
		Last Modified: Tue, 09 Sep 2025 00:38:33 GMT  
		Size: 16.2 KB (16235 bytes)  
		MIME: application/vnd.in-toto+json
