<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `chronograf`

-	[`chronograf:1.10`](#chronograf110)
-	[`chronograf:1.10-alpine`](#chronograf110-alpine)
-	[`chronograf:1.10.9`](#chronograf1109)
-	[`chronograf:1.10.9-alpine`](#chronograf1109-alpine)
-	[`chronograf:1.11`](#chronograf111)
-	[`chronograf:1.11-alpine`](#chronograf111-alpine)
-	[`chronograf:1.11.2`](#chronograf1112)
-	[`chronograf:1.11.2-alpine`](#chronograf1112-alpine)
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
$ docker pull chronograf@sha256:3a69fbbdc2ef10b0255c333ac02979b554921cad98df1034ed30c56c0e145f44
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
$ docker pull chronograf@sha256:c992149da817a8e2de35e2d2b75e48f2702e248c1fa230fa54a4e39b727b2674
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.0 MB (85009473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f72e29ae456fb9e5e906392925b7265d5cfe3e47edde629b4ba0967661496f8b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:40:45 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 08 May 2026 19:40:51 GMT
ENV CHRONOGRAF_VERSION=1.10.9
# Fri, 08 May 2026 19:40:51 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 08 May 2026 19:40:51 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 08 May 2026 19:40:51 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 08 May 2026 19:40:51 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 08 May 2026 19:40:51 GMT
VOLUME [/var/lib/chronograf]
# Fri, 08 May 2026 19:40:51 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 08 May 2026 19:40:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 08 May 2026 19:40:51 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:9b02e9fcb40102eae20d9d1fc7594b44328f4a3eb9b8a3bdb7db283d10840a30`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 28.2 MB (28236282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c8bd6087250c0a7fb49f2a65e1b8f21cd66c46988206da393ca09373f3e705a`  
		Last Modified: Fri, 08 May 2026 19:41:03 GMT  
		Size: 7.9 MB (7880788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c794e2d6a1af2f722b49f3bbecc093f9ca5ac066f4b9916abed1d0359de4d3d9`  
		Last Modified: Fri, 08 May 2026 19:41:04 GMT  
		Size: 48.9 MB (48867928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3707a60245d5a73b30bdc0244512609468a0c373dc7474750d869962324ee22d`  
		Last Modified: Fri, 08 May 2026 19:41:03 GMT  
		Size: 12.3 KB (12252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:645d96f808d8d8f3238ec3b45cdf079b34071ec238d7457f77894eb70c78cbcf`  
		Last Modified: Fri, 08 May 2026 19:41:03 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98ab8f6fa78b01e8a6e262aadef8cf7a20bfe9f41d5180dc27261816ea668e1f`  
		Last Modified: Fri, 08 May 2026 19:41:04 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:685e6b5a94de34952de183566ba3ef37194f3106a6dc167994a9658742ffb0b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2871203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5994fb2180d244a7e90c397473d08d807b235e786f97b2f3faa2d789fc0af728`

```dockerfile
```

-	Layers:
	-	`sha256:8225388a0b559322e406e7c6aef420b6233d4c7b6fdfe3a2ef84bab2d96485a7`  
		Last Modified: Fri, 08 May 2026 19:41:03 GMT  
		Size: 2.9 MB (2855424 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4fe6d08fa3f820bfea4e1c783e4a7c2bc7b52c615cba39bcfadbd80d806cb101`  
		Last Modified: Fri, 08 May 2026 19:41:03 GMT  
		Size: 15.8 KB (15779 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.10` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:b33598875413608d0478c99f6312dd13d339ec08637245b3ca5b4240bb62ca68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76799162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9992ad53aa7a501a996585c38ab930cba9d10cebe920f0c2f2185c9a5c88837`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:45:02 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 08 May 2026 19:45:09 GMT
ENV CHRONOGRAF_VERSION=1.10.9
# Fri, 08 May 2026 19:45:09 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 08 May 2026 19:45:09 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 08 May 2026 19:45:09 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 08 May 2026 19:45:09 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 08 May 2026 19:45:09 GMT
VOLUME [/var/lib/chronograf]
# Fri, 08 May 2026 19:45:09 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 08 May 2026 19:45:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 08 May 2026 19:45:09 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:1c5a0b31b39e45b38b0c73a2e506eb60bb1de512092b4765e565207648f55da2`  
		Last Modified: Fri, 08 May 2026 18:37:03 GMT  
		Size: 23.9 MB (23941406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22fcbb5462a66e10ae555b149673e9279c8b4fa04f97791f0d52271d801feb85`  
		Last Modified: Fri, 08 May 2026 19:45:20 GMT  
		Size: 6.5 MB (6513235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80428303335f4c923793802bd4cc06173c99c0d1bbf2714ecb8ed3cea34600a1`  
		Last Modified: Fri, 08 May 2026 19:45:21 GMT  
		Size: 46.3 MB (46320043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b6a8976e5fe02f4eff7f050ed2cff1bcc9477b819e17e8a8b4c0e45c8373893`  
		Last Modified: Fri, 08 May 2026 19:45:20 GMT  
		Size: 12.3 KB (12251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebb3b88556344960cc5d503d0eff02d7e0ad6d7e8c286f15bcfc5bac05e0eacc`  
		Last Modified: Fri, 08 May 2026 19:45:20 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b67ba443a7041a914822502c3a569d8fa87c14101e30cf8aca9f2333be50399c`  
		Last Modified: Fri, 08 May 2026 19:45:21 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:fba5ca84dd4f567fd2411fe227b01ba24fe59d0fa7c565f954394a467040ddb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2873569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e37f4d652b1e1d1929dc752064280211dbf5f618d9eeea57ebfcc720c98f631c`

```dockerfile
```

-	Layers:
	-	`sha256:d24aa353c529f86124b19669daab3d883a6328ca294123a194ee377c92c997f0`  
		Last Modified: Fri, 08 May 2026 19:45:20 GMT  
		Size: 2.9 MB (2857713 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f336ed757bce5007f0ad954f554234659523f061c1aec97b6575f359d21baf2d`  
		Last Modified: Fri, 08 May 2026 19:45:20 GMT  
		Size: 15.9 KB (15856 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.10` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:23e0a595cc63dfa00773ccf4a14efd6e3d4ca899b063e8e4b93ca420af2926e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.8 MB (81847637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a563c015229c777759e74bee8ae147820469b741bfd78cde1fd23d8a43be2810`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:42:42 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 08 May 2026 19:42:48 GMT
ENV CHRONOGRAF_VERSION=1.10.9
# Fri, 08 May 2026 19:42:48 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 08 May 2026 19:42:49 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 08 May 2026 19:42:49 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 08 May 2026 19:42:49 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 08 May 2026 19:42:49 GMT
VOLUME [/var/lib/chronograf]
# Fri, 08 May 2026 19:42:49 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 08 May 2026 19:42:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 08 May 2026 19:42:49 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:6a2d07df495cc055bce0251fe801ee08db90750f52e43a555be5dfd8f5023783`  
		Last Modified: Fri, 08 May 2026 18:24:52 GMT  
		Size: 28.1 MB (28116165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eb25a44c6eacc314311a50778a03f85f40019d482b4aa85b59cfaa26895f06c`  
		Last Modified: Fri, 08 May 2026 19:43:00 GMT  
		Size: 7.7 MB (7698512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a37a62783ffbfadaafc686f7f2799d72877af30e67d2cfd0a0a3721a08e1397`  
		Last Modified: Fri, 08 May 2026 19:43:01 GMT  
		Size: 46.0 MB (46008489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60912f777650a7b57b087c957d32d9c05fd756f6ad543c4f15b20362cba8858d`  
		Last Modified: Fri, 08 May 2026 19:42:59 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee3b3a78620917721f53318cca707138b1c637708218d2302728304d6176b122`  
		Last Modified: Fri, 08 May 2026 19:42:59 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3baf5b442e8730507a21742f15187e3d4eb145a804d89398bca152e64cd3a415`  
		Last Modified: Fri, 08 May 2026 19:43:01 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:78b27e389664b8a04a1d202e12a78b36612d4084dab7960644658f92a5383cd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2871559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21e0af813bad3405290ae7a6a304ee2f9d83c1cd6023b7970c72c39ab541e5e4`

```dockerfile
```

-	Layers:
	-	`sha256:70e81fe0ccde6d44cf23c9e44d7a5bbe62099b99dfcf236fd9e116a8274f6c82`  
		Last Modified: Fri, 08 May 2026 19:43:00 GMT  
		Size: 2.9 MB (2855685 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ab1e42e671e75407b972d39fabe61cbccf4a55ff4893d76af4ef0a56861a8ea`  
		Last Modified: Fri, 08 May 2026 19:42:59 GMT  
		Size: 15.9 KB (15874 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.10-alpine`

```console
$ docker pull chronograf@sha256:d67db795c6c64bf832d051028112e619057390648fe212e9c427393769746798
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.10-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:257404077359221b264827d685e34eff5274d993cd8d02cb410638063df477d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33281872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3a15f666b3e98ed0853b3cd6db84fb4ce28ed284b973002a3e7e0745954e2d9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:23:40 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 17 Apr 2026 00:23:41 GMT
RUN apk add --no-cache ca-certificates setpriv &&     update-ca-certificates # buildkit
# Fri, 17 Apr 2026 00:23:46 GMT
ENV CHRONOGRAF_VERSION=1.10.9
# Fri, 17 Apr 2026 00:23:46 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S chronograf &&     adduser -S chronograf -G chronograf &&     mkdir -m 0750 -p /var/lib/chronograf &&     chown chronograf:chronograf /var/lib/chronograf # buildkit
# Fri, 17 Apr 2026 00:23:46 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 17 Apr 2026 00:23:46 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 17 Apr 2026 00:23:46 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 17 Apr 2026 00:23:46 GMT
VOLUME [/var/lib/chronograf]
# Fri, 17 Apr 2026 00:23:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 17 Apr 2026 00:23:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 17 Apr 2026 00:23:46 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:918c42c4c82c5088e972f05e6e4c61e835f85d39a8aa5867459dde6d6cf0dcf9`  
		Last Modified: Fri, 17 Apr 2026 00:23:54 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f386db9e6688fb72589c06bb92c9e5581bf0f12dc9e7976d1fd94aa0e0f3fb03`  
		Last Modified: Fri, 17 Apr 2026 00:23:54 GMT  
		Size: 312.2 KB (312182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c09588157059f49ad2a9622892e2ae4eea22a850019e5f096129f96ffe5ef2f`  
		Last Modified: Fri, 17 Apr 2026 00:23:55 GMT  
		Size: 29.1 MB (29136768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c29f2d6761a854698c8fc77adb5c5f5ec518db3475a4dff4dc463c7d8453e5be`  
		Last Modified: Fri, 17 Apr 2026 00:23:54 GMT  
		Size: 12.2 KB (12241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a5d89becaf0206e7f1f6029d6b6a13607ec72d9a340adcd737bec99c4e2ddbb`  
		Last Modified: Fri, 17 Apr 2026 00:23:55 GMT  
		Size: 11.9 KB (11900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b890ebfc700be8ee259bd864396302d8201bd5d269e82ead45a226bc9eb80026`  
		Last Modified: Fri, 17 Apr 2026 00:23:55 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:d2f1dd5e80f798e00c99361d4e5ae8a4c66a9cd69fa098c1a46b99dfecf9fd66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.2 KB (269153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:364dd10613f47468bd32987446ad21e97c4a4eb16fde031d198bcf3ad4eabdad`

```dockerfile
```

-	Layers:
	-	`sha256:81a1ebf9e733fa77e5931f96097a372de666e3ddcc8e8ef5d62ce11a2c9832c8`  
		Last Modified: Fri, 17 Apr 2026 00:23:54 GMT  
		Size: 251.3 KB (251342 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e576ff54c0928fe47749ca45031b2f2d5985bdeb3ea51aa3b1872c70242fdd0b`  
		Last Modified: Fri, 17 Apr 2026 00:23:54 GMT  
		Size: 17.8 KB (17811 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.10.9`

```console
$ docker pull chronograf@sha256:3a69fbbdc2ef10b0255c333ac02979b554921cad98df1034ed30c56c0e145f44
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
$ docker pull chronograf@sha256:c992149da817a8e2de35e2d2b75e48f2702e248c1fa230fa54a4e39b727b2674
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.0 MB (85009473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f72e29ae456fb9e5e906392925b7265d5cfe3e47edde629b4ba0967661496f8b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:40:45 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 08 May 2026 19:40:51 GMT
ENV CHRONOGRAF_VERSION=1.10.9
# Fri, 08 May 2026 19:40:51 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 08 May 2026 19:40:51 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 08 May 2026 19:40:51 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 08 May 2026 19:40:51 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 08 May 2026 19:40:51 GMT
VOLUME [/var/lib/chronograf]
# Fri, 08 May 2026 19:40:51 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 08 May 2026 19:40:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 08 May 2026 19:40:51 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:9b02e9fcb40102eae20d9d1fc7594b44328f4a3eb9b8a3bdb7db283d10840a30`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 28.2 MB (28236282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c8bd6087250c0a7fb49f2a65e1b8f21cd66c46988206da393ca09373f3e705a`  
		Last Modified: Fri, 08 May 2026 19:41:03 GMT  
		Size: 7.9 MB (7880788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c794e2d6a1af2f722b49f3bbecc093f9ca5ac066f4b9916abed1d0359de4d3d9`  
		Last Modified: Fri, 08 May 2026 19:41:04 GMT  
		Size: 48.9 MB (48867928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3707a60245d5a73b30bdc0244512609468a0c373dc7474750d869962324ee22d`  
		Last Modified: Fri, 08 May 2026 19:41:03 GMT  
		Size: 12.3 KB (12252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:645d96f808d8d8f3238ec3b45cdf079b34071ec238d7457f77894eb70c78cbcf`  
		Last Modified: Fri, 08 May 2026 19:41:03 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98ab8f6fa78b01e8a6e262aadef8cf7a20bfe9f41d5180dc27261816ea668e1f`  
		Last Modified: Fri, 08 May 2026 19:41:04 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10.9` - unknown; unknown

```console
$ docker pull chronograf@sha256:685e6b5a94de34952de183566ba3ef37194f3106a6dc167994a9658742ffb0b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2871203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5994fb2180d244a7e90c397473d08d807b235e786f97b2f3faa2d789fc0af728`

```dockerfile
```

-	Layers:
	-	`sha256:8225388a0b559322e406e7c6aef420b6233d4c7b6fdfe3a2ef84bab2d96485a7`  
		Last Modified: Fri, 08 May 2026 19:41:03 GMT  
		Size: 2.9 MB (2855424 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4fe6d08fa3f820bfea4e1c783e4a7c2bc7b52c615cba39bcfadbd80d806cb101`  
		Last Modified: Fri, 08 May 2026 19:41:03 GMT  
		Size: 15.8 KB (15779 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.10.9` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:b33598875413608d0478c99f6312dd13d339ec08637245b3ca5b4240bb62ca68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76799162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9992ad53aa7a501a996585c38ab930cba9d10cebe920f0c2f2185c9a5c88837`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:45:02 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 08 May 2026 19:45:09 GMT
ENV CHRONOGRAF_VERSION=1.10.9
# Fri, 08 May 2026 19:45:09 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 08 May 2026 19:45:09 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 08 May 2026 19:45:09 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 08 May 2026 19:45:09 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 08 May 2026 19:45:09 GMT
VOLUME [/var/lib/chronograf]
# Fri, 08 May 2026 19:45:09 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 08 May 2026 19:45:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 08 May 2026 19:45:09 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:1c5a0b31b39e45b38b0c73a2e506eb60bb1de512092b4765e565207648f55da2`  
		Last Modified: Fri, 08 May 2026 18:37:03 GMT  
		Size: 23.9 MB (23941406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22fcbb5462a66e10ae555b149673e9279c8b4fa04f97791f0d52271d801feb85`  
		Last Modified: Fri, 08 May 2026 19:45:20 GMT  
		Size: 6.5 MB (6513235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80428303335f4c923793802bd4cc06173c99c0d1bbf2714ecb8ed3cea34600a1`  
		Last Modified: Fri, 08 May 2026 19:45:21 GMT  
		Size: 46.3 MB (46320043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b6a8976e5fe02f4eff7f050ed2cff1bcc9477b819e17e8a8b4c0e45c8373893`  
		Last Modified: Fri, 08 May 2026 19:45:20 GMT  
		Size: 12.3 KB (12251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebb3b88556344960cc5d503d0eff02d7e0ad6d7e8c286f15bcfc5bac05e0eacc`  
		Last Modified: Fri, 08 May 2026 19:45:20 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b67ba443a7041a914822502c3a569d8fa87c14101e30cf8aca9f2333be50399c`  
		Last Modified: Fri, 08 May 2026 19:45:21 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10.9` - unknown; unknown

```console
$ docker pull chronograf@sha256:fba5ca84dd4f567fd2411fe227b01ba24fe59d0fa7c565f954394a467040ddb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2873569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e37f4d652b1e1d1929dc752064280211dbf5f618d9eeea57ebfcc720c98f631c`

```dockerfile
```

-	Layers:
	-	`sha256:d24aa353c529f86124b19669daab3d883a6328ca294123a194ee377c92c997f0`  
		Last Modified: Fri, 08 May 2026 19:45:20 GMT  
		Size: 2.9 MB (2857713 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f336ed757bce5007f0ad954f554234659523f061c1aec97b6575f359d21baf2d`  
		Last Modified: Fri, 08 May 2026 19:45:20 GMT  
		Size: 15.9 KB (15856 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.10.9` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:23e0a595cc63dfa00773ccf4a14efd6e3d4ca899b063e8e4b93ca420af2926e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.8 MB (81847637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a563c015229c777759e74bee8ae147820469b741bfd78cde1fd23d8a43be2810`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:42:42 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 08 May 2026 19:42:48 GMT
ENV CHRONOGRAF_VERSION=1.10.9
# Fri, 08 May 2026 19:42:48 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 08 May 2026 19:42:49 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 08 May 2026 19:42:49 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 08 May 2026 19:42:49 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 08 May 2026 19:42:49 GMT
VOLUME [/var/lib/chronograf]
# Fri, 08 May 2026 19:42:49 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 08 May 2026 19:42:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 08 May 2026 19:42:49 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:6a2d07df495cc055bce0251fe801ee08db90750f52e43a555be5dfd8f5023783`  
		Last Modified: Fri, 08 May 2026 18:24:52 GMT  
		Size: 28.1 MB (28116165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eb25a44c6eacc314311a50778a03f85f40019d482b4aa85b59cfaa26895f06c`  
		Last Modified: Fri, 08 May 2026 19:43:00 GMT  
		Size: 7.7 MB (7698512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a37a62783ffbfadaafc686f7f2799d72877af30e67d2cfd0a0a3721a08e1397`  
		Last Modified: Fri, 08 May 2026 19:43:01 GMT  
		Size: 46.0 MB (46008489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60912f777650a7b57b087c957d32d9c05fd756f6ad543c4f15b20362cba8858d`  
		Last Modified: Fri, 08 May 2026 19:42:59 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee3b3a78620917721f53318cca707138b1c637708218d2302728304d6176b122`  
		Last Modified: Fri, 08 May 2026 19:42:59 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3baf5b442e8730507a21742f15187e3d4eb145a804d89398bca152e64cd3a415`  
		Last Modified: Fri, 08 May 2026 19:43:01 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10.9` - unknown; unknown

```console
$ docker pull chronograf@sha256:78b27e389664b8a04a1d202e12a78b36612d4084dab7960644658f92a5383cd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2871559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21e0af813bad3405290ae7a6a304ee2f9d83c1cd6023b7970c72c39ab541e5e4`

```dockerfile
```

-	Layers:
	-	`sha256:70e81fe0ccde6d44cf23c9e44d7a5bbe62099b99dfcf236fd9e116a8274f6c82`  
		Last Modified: Fri, 08 May 2026 19:43:00 GMT  
		Size: 2.9 MB (2855685 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ab1e42e671e75407b972d39fabe61cbccf4a55ff4893d76af4ef0a56861a8ea`  
		Last Modified: Fri, 08 May 2026 19:42:59 GMT  
		Size: 15.9 KB (15874 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.10.9-alpine`

```console
$ docker pull chronograf@sha256:d67db795c6c64bf832d051028112e619057390648fe212e9c427393769746798
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.10.9-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:257404077359221b264827d685e34eff5274d993cd8d02cb410638063df477d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33281872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3a15f666b3e98ed0853b3cd6db84fb4ce28ed284b973002a3e7e0745954e2d9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:23:40 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 17 Apr 2026 00:23:41 GMT
RUN apk add --no-cache ca-certificates setpriv &&     update-ca-certificates # buildkit
# Fri, 17 Apr 2026 00:23:46 GMT
ENV CHRONOGRAF_VERSION=1.10.9
# Fri, 17 Apr 2026 00:23:46 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S chronograf &&     adduser -S chronograf -G chronograf &&     mkdir -m 0750 -p /var/lib/chronograf &&     chown chronograf:chronograf /var/lib/chronograf # buildkit
# Fri, 17 Apr 2026 00:23:46 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 17 Apr 2026 00:23:46 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 17 Apr 2026 00:23:46 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 17 Apr 2026 00:23:46 GMT
VOLUME [/var/lib/chronograf]
# Fri, 17 Apr 2026 00:23:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 17 Apr 2026 00:23:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 17 Apr 2026 00:23:46 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:918c42c4c82c5088e972f05e6e4c61e835f85d39a8aa5867459dde6d6cf0dcf9`  
		Last Modified: Fri, 17 Apr 2026 00:23:54 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f386db9e6688fb72589c06bb92c9e5581bf0f12dc9e7976d1fd94aa0e0f3fb03`  
		Last Modified: Fri, 17 Apr 2026 00:23:54 GMT  
		Size: 312.2 KB (312182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c09588157059f49ad2a9622892e2ae4eea22a850019e5f096129f96ffe5ef2f`  
		Last Modified: Fri, 17 Apr 2026 00:23:55 GMT  
		Size: 29.1 MB (29136768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c29f2d6761a854698c8fc77adb5c5f5ec518db3475a4dff4dc463c7d8453e5be`  
		Last Modified: Fri, 17 Apr 2026 00:23:54 GMT  
		Size: 12.2 KB (12241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a5d89becaf0206e7f1f6029d6b6a13607ec72d9a340adcd737bec99c4e2ddbb`  
		Last Modified: Fri, 17 Apr 2026 00:23:55 GMT  
		Size: 11.9 KB (11900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b890ebfc700be8ee259bd864396302d8201bd5d269e82ead45a226bc9eb80026`  
		Last Modified: Fri, 17 Apr 2026 00:23:55 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10.9-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:d2f1dd5e80f798e00c99361d4e5ae8a4c66a9cd69fa098c1a46b99dfecf9fd66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.2 KB (269153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:364dd10613f47468bd32987446ad21e97c4a4eb16fde031d198bcf3ad4eabdad`

```dockerfile
```

-	Layers:
	-	`sha256:81a1ebf9e733fa77e5931f96097a372de666e3ddcc8e8ef5d62ce11a2c9832c8`  
		Last Modified: Fri, 17 Apr 2026 00:23:54 GMT  
		Size: 251.3 KB (251342 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e576ff54c0928fe47749ca45031b2f2d5985bdeb3ea51aa3b1872c70242fdd0b`  
		Last Modified: Fri, 17 Apr 2026 00:23:54 GMT  
		Size: 17.8 KB (17811 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.11`

```console
$ docker pull chronograf@sha256:a6db91a1ba1d88d19b04ca4cad6db77d90ded5d9c7bec3ef5a793a967c23c04d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `chronograf:1.11` - linux; amd64

```console
$ docker pull chronograf@sha256:54e32cd3e48ac4c3def6925aa03676dc0d8a16a64eed75411011f4f527f55d45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.3 MB (96301797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad189a1b2cfe7415ac0b93a1307700b8dd6a44f716adba4f7470481115b158d5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:41:01 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 08 May 2026 19:41:08 GMT
ENV CHRONOGRAF_VERSION=1.11.2
# Fri, 08 May 2026 19:41:08 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 08 May 2026 19:41:08 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 08 May 2026 19:41:08 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 08 May 2026 19:41:08 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 08 May 2026 19:41:08 GMT
VOLUME [/var/lib/chronograf]
# Fri, 08 May 2026 19:41:08 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 08 May 2026 19:41:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 08 May 2026 19:41:08 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:9b02e9fcb40102eae20d9d1fc7594b44328f4a3eb9b8a3bdb7db283d10840a30`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 28.2 MB (28236282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1d3fd0ca26ff2a170b79fb17a608035a5b66d1ae4ae2162ba9fe03b5013b9c2`  
		Last Modified: Fri, 08 May 2026 19:41:24 GMT  
		Size: 7.9 MB (7880771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1600d57770479f768c269fcee3529bba79d87676b97fccfa0d6986e6fb35b123`  
		Last Modified: Fri, 08 May 2026 19:41:25 GMT  
		Size: 60.2 MB (60160268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf794b3a83674671e9ab42987f1abf1a9e955e6002b245a0009e665dfcab6a0f`  
		Last Modified: Fri, 08 May 2026 19:41:24 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:334c2c3c5016987b28b99b8fd10bcf0e635891be21a01e875f54aa240fc771d3`  
		Last Modified: Fri, 08 May 2026 19:41:24 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b18a35825a88afbfe2d23a81eecf482053eb67293f59ab1a712e409f73d7e4f`  
		Last Modified: Fri, 08 May 2026 19:41:25 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.11` - unknown; unknown

```console
$ docker pull chronograf@sha256:1138670f6509706eb0215dc17a4c7aace6b1ec3c94ae65e1193609f277b66a51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2889784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7312f318ce642b41773dd4ee48f6dde77882dacee25793cea5d376b990668039`

```dockerfile
```

-	Layers:
	-	`sha256:6a125d7c59f75e398266ea88913b40be232725ee1ef89a1c84c8c88fe7b46d50`  
		Last Modified: Fri, 08 May 2026 19:41:24 GMT  
		Size: 2.9 MB (2873700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2961714e758eddbdf4ad9df34423a4746d8abd41bb1cf928409032e6b2450a22`  
		Last Modified: Fri, 08 May 2026 19:41:23 GMT  
		Size: 16.1 KB (16084 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.11` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:06039e8fe6660d86b1c58ddac69bfb6992add3e7bada41f53dccfb72a6262cfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.0 MB (93017873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94183117c18e70abcb1fa65164a7ea3de8131443b142d8b3e7613026b5c1f57f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:42:44 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 08 May 2026 19:42:51 GMT
ENV CHRONOGRAF_VERSION=1.11.2
# Fri, 08 May 2026 19:42:51 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 08 May 2026 19:42:51 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 08 May 2026 19:42:51 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 08 May 2026 19:42:51 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 08 May 2026 19:42:51 GMT
VOLUME [/var/lib/chronograf]
# Fri, 08 May 2026 19:42:51 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 08 May 2026 19:42:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 08 May 2026 19:42:51 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:6a2d07df495cc055bce0251fe801ee08db90750f52e43a555be5dfd8f5023783`  
		Last Modified: Fri, 08 May 2026 18:24:52 GMT  
		Size: 28.1 MB (28116165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:014811a135ddb7b07f7c1d6306e500555c1eb6652b80c686929511fcaa4ec072`  
		Last Modified: Fri, 08 May 2026 19:43:05 GMT  
		Size: 7.7 MB (7698454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1fb404ada7af90249b507c8dd6121125a7c52b953ffd4543d339d8bf7b2db94`  
		Last Modified: Fri, 08 May 2026 19:43:08 GMT  
		Size: 57.2 MB (57178776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08b728e1b5f393e36b5537563f4ae62732cf16f2065b558fcbdf56f9022a9a7f`  
		Last Modified: Fri, 08 May 2026 19:43:05 GMT  
		Size: 12.3 KB (12252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da5ec718ae5a77034d4eed65124387bffd6fda82394f214c9d4332a91219b448`  
		Last Modified: Fri, 08 May 2026 19:43:05 GMT  
		Size: 11.9 KB (11911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b84a3b1086e4e5daebc8a431314e56550afff37660f6d6f0e45265efe2aaf59`  
		Last Modified: Fri, 08 May 2026 19:43:06 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.11` - unknown; unknown

```console
$ docker pull chronograf@sha256:0b640e32cbc0cec417e8368b9f511770bbb324545f70d758ca3d336a3bbb53d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2889106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7ac5d2b3233e3020ea6f2d5d2b46ba5e11a072406a18a391e4ddb8a3a9ddca6`

```dockerfile
```

-	Layers:
	-	`sha256:2d81cbb5f1f2ab9afe346e27664b487561e7949f8026ce308e0c0834a78b24eb`  
		Last Modified: Fri, 08 May 2026 19:43:05 GMT  
		Size: 2.9 MB (2872914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ec10703780086fed811e3f13be45453a584373a5fbd96578feffd56602b8d31`  
		Last Modified: Fri, 08 May 2026 19:43:05 GMT  
		Size: 16.2 KB (16192 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.11-alpine`

```console
$ docker pull chronograf@sha256:be0d839a52d44e71953d0b2836e8a5fbabb1fe7512aec618d48daa4fa44ed60a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.11-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:80f0eac35fdf4e62dfb101e808d23934c0c8418d946c40eef1bda748a8eb716c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62334787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1df51aab599500a1d5705e60635ce7ec1dc518251bcae39c434ef849f3a5bed`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Thu, 07 May 2026 17:43:20 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Thu, 07 May 2026 17:43:20 GMT
RUN apk add --no-cache ca-certificates setpriv &&     update-ca-certificates # buildkit
# Thu, 07 May 2026 17:43:25 GMT
ENV CHRONOGRAF_VERSION=1.11.2
# Thu, 07 May 2026 17:43:25 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S chronograf &&     adduser -S chronograf -G chronograf &&     mkdir -m 0750 -p /var/lib/chronograf &&     chown chronograf:chronograf /var/lib/chronograf # buildkit
# Thu, 07 May 2026 17:43:25 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Thu, 07 May 2026 17:43:25 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Thu, 07 May 2026 17:43:25 GMT
EXPOSE map[8888/tcp:{}]
# Thu, 07 May 2026 17:43:25 GMT
VOLUME [/var/lib/chronograf]
# Thu, 07 May 2026 17:43:25 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 07 May 2026 17:43:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 07 May 2026 17:43:25 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5f034fedb34a4c678230b662d88eead9f8327232402638bf43a349457f5af51`  
		Last Modified: Thu, 07 May 2026 17:43:38 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f387b1db623035224cf796e12a993c1c1f7a4b369bdeeb5e69b9dfa236f5be0`  
		Last Modified: Thu, 07 May 2026 17:43:39 GMT  
		Size: 312.2 KB (312193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36950b5f1bb549bd7a1db0f996523a6c41454afac370de0b8d28772164770e22`  
		Last Modified: Thu, 07 May 2026 17:43:40 GMT  
		Size: 58.2 MB (58189680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5d53388b5e8ad45e9e4d75047a3f99495f913bd091298d8cf56111072ec7482`  
		Last Modified: Thu, 07 May 2026 17:43:38 GMT  
		Size: 12.2 KB (12236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:758a472b1a9b3c3b5f474a8b06bc8c0d0f20e03bd4b65ec18316a19b0d2fb05e`  
		Last Modified: Thu, 07 May 2026 17:43:39 GMT  
		Size: 11.9 KB (11895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09eeca9b42ec7a839911d9cb1dbb30cde2510a076fd90e2a24bb8daf6967b36b`  
		Last Modified: Thu, 07 May 2026 17:43:39 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.11-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:20f564bf4977e07cdee0af68ac679d481df1edfc5b16cfe5c4f212d1287488bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.1 KB (287057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf62ab165d3d6eedbce59839293260aa5898128b6d663a167676dc41df4495dd`

```dockerfile
```

-	Layers:
	-	`sha256:379aecff8e7d7778fe0361cd9d05ebacd639bbb4bae468b1d13cfc8eaea61b87`  
		Last Modified: Thu, 07 May 2026 17:43:38 GMT  
		Size: 269.3 KB (269328 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0abeb95209c442bcfbeec66105986fcc5bba3da5e7f7017351cb3c7373dfe90e`  
		Last Modified: Thu, 07 May 2026 17:43:38 GMT  
		Size: 17.7 KB (17729 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.11.2`

```console
$ docker pull chronograf@sha256:a6db91a1ba1d88d19b04ca4cad6db77d90ded5d9c7bec3ef5a793a967c23c04d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `chronograf:1.11.2` - linux; amd64

```console
$ docker pull chronograf@sha256:54e32cd3e48ac4c3def6925aa03676dc0d8a16a64eed75411011f4f527f55d45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.3 MB (96301797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad189a1b2cfe7415ac0b93a1307700b8dd6a44f716adba4f7470481115b158d5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:41:01 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 08 May 2026 19:41:08 GMT
ENV CHRONOGRAF_VERSION=1.11.2
# Fri, 08 May 2026 19:41:08 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 08 May 2026 19:41:08 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 08 May 2026 19:41:08 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 08 May 2026 19:41:08 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 08 May 2026 19:41:08 GMT
VOLUME [/var/lib/chronograf]
# Fri, 08 May 2026 19:41:08 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 08 May 2026 19:41:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 08 May 2026 19:41:08 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:9b02e9fcb40102eae20d9d1fc7594b44328f4a3eb9b8a3bdb7db283d10840a30`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 28.2 MB (28236282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1d3fd0ca26ff2a170b79fb17a608035a5b66d1ae4ae2162ba9fe03b5013b9c2`  
		Last Modified: Fri, 08 May 2026 19:41:24 GMT  
		Size: 7.9 MB (7880771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1600d57770479f768c269fcee3529bba79d87676b97fccfa0d6986e6fb35b123`  
		Last Modified: Fri, 08 May 2026 19:41:25 GMT  
		Size: 60.2 MB (60160268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf794b3a83674671e9ab42987f1abf1a9e955e6002b245a0009e665dfcab6a0f`  
		Last Modified: Fri, 08 May 2026 19:41:24 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:334c2c3c5016987b28b99b8fd10bcf0e635891be21a01e875f54aa240fc771d3`  
		Last Modified: Fri, 08 May 2026 19:41:24 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b18a35825a88afbfe2d23a81eecf482053eb67293f59ab1a712e409f73d7e4f`  
		Last Modified: Fri, 08 May 2026 19:41:25 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.11.2` - unknown; unknown

```console
$ docker pull chronograf@sha256:1138670f6509706eb0215dc17a4c7aace6b1ec3c94ae65e1193609f277b66a51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2889784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7312f318ce642b41773dd4ee48f6dde77882dacee25793cea5d376b990668039`

```dockerfile
```

-	Layers:
	-	`sha256:6a125d7c59f75e398266ea88913b40be232725ee1ef89a1c84c8c88fe7b46d50`  
		Last Modified: Fri, 08 May 2026 19:41:24 GMT  
		Size: 2.9 MB (2873700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2961714e758eddbdf4ad9df34423a4746d8abd41bb1cf928409032e6b2450a22`  
		Last Modified: Fri, 08 May 2026 19:41:23 GMT  
		Size: 16.1 KB (16084 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.11.2` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:06039e8fe6660d86b1c58ddac69bfb6992add3e7bada41f53dccfb72a6262cfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.0 MB (93017873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94183117c18e70abcb1fa65164a7ea3de8131443b142d8b3e7613026b5c1f57f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:42:44 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 08 May 2026 19:42:51 GMT
ENV CHRONOGRAF_VERSION=1.11.2
# Fri, 08 May 2026 19:42:51 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 08 May 2026 19:42:51 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 08 May 2026 19:42:51 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 08 May 2026 19:42:51 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 08 May 2026 19:42:51 GMT
VOLUME [/var/lib/chronograf]
# Fri, 08 May 2026 19:42:51 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 08 May 2026 19:42:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 08 May 2026 19:42:51 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:6a2d07df495cc055bce0251fe801ee08db90750f52e43a555be5dfd8f5023783`  
		Last Modified: Fri, 08 May 2026 18:24:52 GMT  
		Size: 28.1 MB (28116165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:014811a135ddb7b07f7c1d6306e500555c1eb6652b80c686929511fcaa4ec072`  
		Last Modified: Fri, 08 May 2026 19:43:05 GMT  
		Size: 7.7 MB (7698454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1fb404ada7af90249b507c8dd6121125a7c52b953ffd4543d339d8bf7b2db94`  
		Last Modified: Fri, 08 May 2026 19:43:08 GMT  
		Size: 57.2 MB (57178776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08b728e1b5f393e36b5537563f4ae62732cf16f2065b558fcbdf56f9022a9a7f`  
		Last Modified: Fri, 08 May 2026 19:43:05 GMT  
		Size: 12.3 KB (12252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da5ec718ae5a77034d4eed65124387bffd6fda82394f214c9d4332a91219b448`  
		Last Modified: Fri, 08 May 2026 19:43:05 GMT  
		Size: 11.9 KB (11911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b84a3b1086e4e5daebc8a431314e56550afff37660f6d6f0e45265efe2aaf59`  
		Last Modified: Fri, 08 May 2026 19:43:06 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.11.2` - unknown; unknown

```console
$ docker pull chronograf@sha256:0b640e32cbc0cec417e8368b9f511770bbb324545f70d758ca3d336a3bbb53d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2889106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7ac5d2b3233e3020ea6f2d5d2b46ba5e11a072406a18a391e4ddb8a3a9ddca6`

```dockerfile
```

-	Layers:
	-	`sha256:2d81cbb5f1f2ab9afe346e27664b487561e7949f8026ce308e0c0834a78b24eb`  
		Last Modified: Fri, 08 May 2026 19:43:05 GMT  
		Size: 2.9 MB (2872914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ec10703780086fed811e3f13be45453a584373a5fbd96578feffd56602b8d31`  
		Last Modified: Fri, 08 May 2026 19:43:05 GMT  
		Size: 16.2 KB (16192 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.11.2-alpine`

```console
$ docker pull chronograf@sha256:be0d839a52d44e71953d0b2836e8a5fbabb1fe7512aec618d48daa4fa44ed60a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.11.2-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:80f0eac35fdf4e62dfb101e808d23934c0c8418d946c40eef1bda748a8eb716c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62334787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1df51aab599500a1d5705e60635ce7ec1dc518251bcae39c434ef849f3a5bed`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Thu, 07 May 2026 17:43:20 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Thu, 07 May 2026 17:43:20 GMT
RUN apk add --no-cache ca-certificates setpriv &&     update-ca-certificates # buildkit
# Thu, 07 May 2026 17:43:25 GMT
ENV CHRONOGRAF_VERSION=1.11.2
# Thu, 07 May 2026 17:43:25 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S chronograf &&     adduser -S chronograf -G chronograf &&     mkdir -m 0750 -p /var/lib/chronograf &&     chown chronograf:chronograf /var/lib/chronograf # buildkit
# Thu, 07 May 2026 17:43:25 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Thu, 07 May 2026 17:43:25 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Thu, 07 May 2026 17:43:25 GMT
EXPOSE map[8888/tcp:{}]
# Thu, 07 May 2026 17:43:25 GMT
VOLUME [/var/lib/chronograf]
# Thu, 07 May 2026 17:43:25 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 07 May 2026 17:43:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 07 May 2026 17:43:25 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5f034fedb34a4c678230b662d88eead9f8327232402638bf43a349457f5af51`  
		Last Modified: Thu, 07 May 2026 17:43:38 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f387b1db623035224cf796e12a993c1c1f7a4b369bdeeb5e69b9dfa236f5be0`  
		Last Modified: Thu, 07 May 2026 17:43:39 GMT  
		Size: 312.2 KB (312193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36950b5f1bb549bd7a1db0f996523a6c41454afac370de0b8d28772164770e22`  
		Last Modified: Thu, 07 May 2026 17:43:40 GMT  
		Size: 58.2 MB (58189680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5d53388b5e8ad45e9e4d75047a3f99495f913bd091298d8cf56111072ec7482`  
		Last Modified: Thu, 07 May 2026 17:43:38 GMT  
		Size: 12.2 KB (12236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:758a472b1a9b3c3b5f474a8b06bc8c0d0f20e03bd4b65ec18316a19b0d2fb05e`  
		Last Modified: Thu, 07 May 2026 17:43:39 GMT  
		Size: 11.9 KB (11895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09eeca9b42ec7a839911d9cb1dbb30cde2510a076fd90e2a24bb8daf6967b36b`  
		Last Modified: Thu, 07 May 2026 17:43:39 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.11.2-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:20f564bf4977e07cdee0af68ac679d481df1edfc5b16cfe5c4f212d1287488bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.1 KB (287057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf62ab165d3d6eedbce59839293260aa5898128b6d663a167676dc41df4495dd`

```dockerfile
```

-	Layers:
	-	`sha256:379aecff8e7d7778fe0361cd9d05ebacd639bbb4bae468b1d13cfc8eaea61b87`  
		Last Modified: Thu, 07 May 2026 17:43:38 GMT  
		Size: 269.3 KB (269328 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0abeb95209c442bcfbeec66105986fcc5bba3da5e7f7017351cb3c7373dfe90e`  
		Last Modified: Thu, 07 May 2026 17:43:38 GMT  
		Size: 17.7 KB (17729 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.8`

```console
$ docker pull chronograf@sha256:22afcae0dec0af32bab0b843aef432d9a164313b87629056be018b1f0cccf0d4
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
$ docker pull chronograf@sha256:58387425ca9901ed9679f5b56a7f4963ea1aa62a10ffab5a92b804ff1cf5b9c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69888435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b1af8c2da3c1a6456426404d4477fb5e50cddb54d12ca8c840759fbf749ad7e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1777939200'
# Fri, 08 May 2026 19:40:45 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 08 May 2026 19:40:50 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Fri, 08 May 2026 19:40:50 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 08 May 2026 19:40:50 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 08 May 2026 19:40:50 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 08 May 2026 19:40:50 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 08 May 2026 19:40:50 GMT
VOLUME [/var/lib/chronograf]
# Fri, 08 May 2026 19:40:50 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 08 May 2026 19:40:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 08 May 2026 19:40:50 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:77e30ef52aeb52d8466baf0f50b54ed2fc0b421f44c49e5bf93682b27110f4d3`  
		Last Modified: Fri, 08 May 2026 18:22:59 GMT  
		Size: 30.3 MB (30257958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2249a0da8b72ca69abe0792859ae6cb271cd0ccdc4e98fb78fca59003102dd45`  
		Last Modified: Fri, 08 May 2026 19:40:59 GMT  
		Size: 5.2 MB (5241767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afbbfb36680dd66bf9628c6dc15c78dd2dcee8f635014db2a674dcb1bf18827e`  
		Last Modified: Fri, 08 May 2026 19:41:00 GMT  
		Size: 34.4 MB (34364312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:210b1ca9a83fd0339ff990591e2cddcbe8f91b6c8e3fa540f92cc234349f8b5c`  
		Last Modified: Fri, 08 May 2026 19:40:59 GMT  
		Size: 12.3 KB (12251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aaa3dedef4a51e2f5836451743c23a5bbc8ff7bab57b71e3b2bbb4fa4b4eab2`  
		Last Modified: Fri, 08 May 2026 19:40:59 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abbb8379ed7bc4a2224df4dc77783ed5ffa0710451d3b8f384fed9ff147b34b4`  
		Last Modified: Fri, 08 May 2026 19:41:00 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8` - unknown; unknown

```console
$ docker pull chronograf@sha256:33c918182a2e305c32b8ef566b9edd2df04c3b4ed0eafc44a1d78b4fa610de30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3128705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ef18c16bf2554b5579b807174cd72768d6260a6952b2995a2b3c954b76f0fa2`

```dockerfile
```

-	Layers:
	-	`sha256:7ac5c6739d0371141529aff377e2ab13924547311c28971b3f4c032d3f48cc20`  
		Last Modified: Fri, 08 May 2026 19:40:59 GMT  
		Size: 3.1 MB (3112931 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2ce7cf0b2e2005568c0d17b005ee925fb64605db4e7ba6153615080510e7047`  
		Last Modified: Fri, 08 May 2026 19:40:59 GMT  
		Size: 15.8 KB (15774 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.8` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:33e4e680b602723e05ea53d194164dbca063a542a3fb0369296dfc5e520f0b71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.6 MB (62620570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60e2be8debca2232f009be10074e8caaea40bb6ab83923bc4149ff0af23fec79`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1777939200'
# Fri, 08 May 2026 19:44:54 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 08 May 2026 19:45:01 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Fri, 08 May 2026 19:45:01 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 08 May 2026 19:45:01 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 08 May 2026 19:45:01 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 08 May 2026 19:45:01 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 08 May 2026 19:45:01 GMT
VOLUME [/var/lib/chronograf]
# Fri, 08 May 2026 19:45:01 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 08 May 2026 19:45:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 08 May 2026 19:45:01 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:976dfa794c59ebfed71602151daddefd6dc6a747d5d0ff3934bce4d42d3677c5`  
		Last Modified: Fri, 08 May 2026 18:37:07 GMT  
		Size: 25.6 MB (25551243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4838eb30c0eea2c986ce112e434c36090cefb70c3ddccf0bd5f701a4b9a640d5`  
		Last Modified: Fri, 08 May 2026 19:45:10 GMT  
		Size: 4.5 MB (4510009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c93e915bc2ea6973f06b5cba177f074a9996b109b1536e558d60e4e33b99a21d`  
		Last Modified: Fri, 08 May 2026 19:45:11 GMT  
		Size: 32.5 MB (32534927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:295e008b32a69ae99d76be4f784b33b008221c60aa9ccb78327ea6512e9c3028`  
		Last Modified: Fri, 08 May 2026 19:45:10 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99c2287ae23031a0639fe98f0cb9fd88687f7219bc656e66fdc0ce7ff468111a`  
		Last Modified: Fri, 08 May 2026 19:45:10 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b68f199919f7b49c07f73fec7c9b4cd93da37cb8a9a52a4e3e919393d1030536`  
		Last Modified: Fri, 08 May 2026 19:45:10 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8` - unknown; unknown

```console
$ docker pull chronograf@sha256:8dd9a6d049c128da7ed2ed94f5f5b9056b7222a7c4b132c53d119fefb64b75d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3131053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a24107387d338191e9888348aeadcea4262d574c66f2606408f5ec1d2ba3c1e`

```dockerfile
```

-	Layers:
	-	`sha256:95149d75c7794bb990e2598db62a608907e83f6ad704785dd97f47f7701bc0a8`  
		Last Modified: Fri, 08 May 2026 19:45:10 GMT  
		Size: 3.1 MB (3115202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0663e60cf9c996b515f07b8fbb823e6eba609eed2fa574177daccabf6d37e72`  
		Last Modified: Fri, 08 May 2026 19:45:10 GMT  
		Size: 15.9 KB (15851 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.8` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:df9d138ef1cf463f37f33c230ad827e38b30b87ddb7818904a2a168c12921c83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.4 MB (66426256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c1736de9befd6e90c90c8395ac72054458eef3f700230fc8ccb4bdd3e653e9c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1777939200'
# Fri, 08 May 2026 19:42:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 08 May 2026 19:42:38 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Fri, 08 May 2026 19:42:38 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 08 May 2026 19:42:38 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 08 May 2026 19:42:38 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 08 May 2026 19:42:38 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 08 May 2026 19:42:38 GMT
VOLUME [/var/lib/chronograf]
# Fri, 08 May 2026 19:42:38 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 08 May 2026 19:42:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 08 May 2026 19:42:38 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:ab0f13d792ff9100407906fb422a0b62a8b437abde4c245e03f0366814be9aae`  
		Last Modified: Fri, 08 May 2026 18:25:06 GMT  
		Size: 28.7 MB (28742591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0079dfd859abfec5b017bfcfa63b0ef722c19199165856754585057337927a9`  
		Last Modified: Fri, 08 May 2026 19:42:47 GMT  
		Size: 5.2 MB (5229768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b767db34ce802f60b786bd1f76bdffc3121bd320603bc98992a1f90ad6f1c98`  
		Last Modified: Fri, 08 May 2026 19:42:48 GMT  
		Size: 32.4 MB (32429501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ef8ceaa05000b8350516b4c04084aee1ecb3b6a1944fbfebc57b6b54971e33a`  
		Last Modified: Fri, 08 May 2026 19:42:47 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b9bf95e79ae1a21a0fb7e02fdcead7bbf940765ad8cfd463d4609afec5b6f08`  
		Last Modified: Fri, 08 May 2026 19:42:47 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8e8909d97e1bb86f96e960628f50f4cfb9a129e304044193cdb8c58c45c79b1`  
		Last Modified: Fri, 08 May 2026 19:42:48 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8` - unknown; unknown

```console
$ docker pull chronograf@sha256:93ded49c8241d53be239d6ded74e900e9d1823980f9e34f72ca0e2e6605bd720
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3129049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:590bb82ccd508bd2c7b86894fac76d85bd306f871d5f5f3d31933c886802949b`

```dockerfile
```

-	Layers:
	-	`sha256:bf8a02bfb170d8ab03c998929206509270f7e300db5ac16184a11a714fcb3780`  
		Last Modified: Fri, 08 May 2026 19:42:47 GMT  
		Size: 3.1 MB (3113180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5950bd700c632e9d90f52a909e67762e3c1e005485449bd1c3cb86440eb2d6ae`  
		Last Modified: Fri, 08 May 2026 19:42:47 GMT  
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
$ docker pull chronograf@sha256:22afcae0dec0af32bab0b843aef432d9a164313b87629056be018b1f0cccf0d4
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
$ docker pull chronograf@sha256:58387425ca9901ed9679f5b56a7f4963ea1aa62a10ffab5a92b804ff1cf5b9c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69888435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b1af8c2da3c1a6456426404d4477fb5e50cddb54d12ca8c840759fbf749ad7e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1777939200'
# Fri, 08 May 2026 19:40:45 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 08 May 2026 19:40:50 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Fri, 08 May 2026 19:40:50 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 08 May 2026 19:40:50 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 08 May 2026 19:40:50 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 08 May 2026 19:40:50 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 08 May 2026 19:40:50 GMT
VOLUME [/var/lib/chronograf]
# Fri, 08 May 2026 19:40:50 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 08 May 2026 19:40:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 08 May 2026 19:40:50 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:77e30ef52aeb52d8466baf0f50b54ed2fc0b421f44c49e5bf93682b27110f4d3`  
		Last Modified: Fri, 08 May 2026 18:22:59 GMT  
		Size: 30.3 MB (30257958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2249a0da8b72ca69abe0792859ae6cb271cd0ccdc4e98fb78fca59003102dd45`  
		Last Modified: Fri, 08 May 2026 19:40:59 GMT  
		Size: 5.2 MB (5241767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afbbfb36680dd66bf9628c6dc15c78dd2dcee8f635014db2a674dcb1bf18827e`  
		Last Modified: Fri, 08 May 2026 19:41:00 GMT  
		Size: 34.4 MB (34364312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:210b1ca9a83fd0339ff990591e2cddcbe8f91b6c8e3fa540f92cc234349f8b5c`  
		Last Modified: Fri, 08 May 2026 19:40:59 GMT  
		Size: 12.3 KB (12251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aaa3dedef4a51e2f5836451743c23a5bbc8ff7bab57b71e3b2bbb4fa4b4eab2`  
		Last Modified: Fri, 08 May 2026 19:40:59 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abbb8379ed7bc4a2224df4dc77783ed5ffa0710451d3b8f384fed9ff147b34b4`  
		Last Modified: Fri, 08 May 2026 19:41:00 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:33c918182a2e305c32b8ef566b9edd2df04c3b4ed0eafc44a1d78b4fa610de30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3128705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ef18c16bf2554b5579b807174cd72768d6260a6952b2995a2b3c954b76f0fa2`

```dockerfile
```

-	Layers:
	-	`sha256:7ac5c6739d0371141529aff377e2ab13924547311c28971b3f4c032d3f48cc20`  
		Last Modified: Fri, 08 May 2026 19:40:59 GMT  
		Size: 3.1 MB (3112931 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2ce7cf0b2e2005568c0d17b005ee925fb64605db4e7ba6153615080510e7047`  
		Last Modified: Fri, 08 May 2026 19:40:59 GMT  
		Size: 15.8 KB (15774 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.8.10` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:33e4e680b602723e05ea53d194164dbca063a542a3fb0369296dfc5e520f0b71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.6 MB (62620570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60e2be8debca2232f009be10074e8caaea40bb6ab83923bc4149ff0af23fec79`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1777939200'
# Fri, 08 May 2026 19:44:54 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 08 May 2026 19:45:01 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Fri, 08 May 2026 19:45:01 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 08 May 2026 19:45:01 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 08 May 2026 19:45:01 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 08 May 2026 19:45:01 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 08 May 2026 19:45:01 GMT
VOLUME [/var/lib/chronograf]
# Fri, 08 May 2026 19:45:01 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 08 May 2026 19:45:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 08 May 2026 19:45:01 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:976dfa794c59ebfed71602151daddefd6dc6a747d5d0ff3934bce4d42d3677c5`  
		Last Modified: Fri, 08 May 2026 18:37:07 GMT  
		Size: 25.6 MB (25551243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4838eb30c0eea2c986ce112e434c36090cefb70c3ddccf0bd5f701a4b9a640d5`  
		Last Modified: Fri, 08 May 2026 19:45:10 GMT  
		Size: 4.5 MB (4510009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c93e915bc2ea6973f06b5cba177f074a9996b109b1536e558d60e4e33b99a21d`  
		Last Modified: Fri, 08 May 2026 19:45:11 GMT  
		Size: 32.5 MB (32534927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:295e008b32a69ae99d76be4f784b33b008221c60aa9ccb78327ea6512e9c3028`  
		Last Modified: Fri, 08 May 2026 19:45:10 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99c2287ae23031a0639fe98f0cb9fd88687f7219bc656e66fdc0ce7ff468111a`  
		Last Modified: Fri, 08 May 2026 19:45:10 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b68f199919f7b49c07f73fec7c9b4cd93da37cb8a9a52a4e3e919393d1030536`  
		Last Modified: Fri, 08 May 2026 19:45:10 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:8dd9a6d049c128da7ed2ed94f5f5b9056b7222a7c4b132c53d119fefb64b75d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3131053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a24107387d338191e9888348aeadcea4262d574c66f2606408f5ec1d2ba3c1e`

```dockerfile
```

-	Layers:
	-	`sha256:95149d75c7794bb990e2598db62a608907e83f6ad704785dd97f47f7701bc0a8`  
		Last Modified: Fri, 08 May 2026 19:45:10 GMT  
		Size: 3.1 MB (3115202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0663e60cf9c996b515f07b8fbb823e6eba609eed2fa574177daccabf6d37e72`  
		Last Modified: Fri, 08 May 2026 19:45:10 GMT  
		Size: 15.9 KB (15851 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.8.10` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:df9d138ef1cf463f37f33c230ad827e38b30b87ddb7818904a2a168c12921c83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.4 MB (66426256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c1736de9befd6e90c90c8395ac72054458eef3f700230fc8ccb4bdd3e653e9c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1777939200'
# Fri, 08 May 2026 19:42:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 08 May 2026 19:42:38 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Fri, 08 May 2026 19:42:38 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 08 May 2026 19:42:38 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 08 May 2026 19:42:38 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 08 May 2026 19:42:38 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 08 May 2026 19:42:38 GMT
VOLUME [/var/lib/chronograf]
# Fri, 08 May 2026 19:42:38 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 08 May 2026 19:42:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 08 May 2026 19:42:38 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:ab0f13d792ff9100407906fb422a0b62a8b437abde4c245e03f0366814be9aae`  
		Last Modified: Fri, 08 May 2026 18:25:06 GMT  
		Size: 28.7 MB (28742591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0079dfd859abfec5b017bfcfa63b0ef722c19199165856754585057337927a9`  
		Last Modified: Fri, 08 May 2026 19:42:47 GMT  
		Size: 5.2 MB (5229768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b767db34ce802f60b786bd1f76bdffc3121bd320603bc98992a1f90ad6f1c98`  
		Last Modified: Fri, 08 May 2026 19:42:48 GMT  
		Size: 32.4 MB (32429501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ef8ceaa05000b8350516b4c04084aee1ecb3b6a1944fbfebc57b6b54971e33a`  
		Last Modified: Fri, 08 May 2026 19:42:47 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b9bf95e79ae1a21a0fb7e02fdcead7bbf940765ad8cfd463d4609afec5b6f08`  
		Last Modified: Fri, 08 May 2026 19:42:47 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8e8909d97e1bb86f96e960628f50f4cfb9a129e304044193cdb8c58c45c79b1`  
		Last Modified: Fri, 08 May 2026 19:42:48 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:93ded49c8241d53be239d6ded74e900e9d1823980f9e34f72ca0e2e6605bd720
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3129049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:590bb82ccd508bd2c7b86894fac76d85bd306f871d5f5f3d31933c886802949b`

```dockerfile
```

-	Layers:
	-	`sha256:bf8a02bfb170d8ab03c998929206509270f7e300db5ac16184a11a714fcb3780`  
		Last Modified: Fri, 08 May 2026 19:42:47 GMT  
		Size: 3.1 MB (3113180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5950bd700c632e9d90f52a909e67762e3c1e005485449bd1c3cb86440eb2d6ae`  
		Last Modified: Fri, 08 May 2026 19:42:47 GMT  
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
$ docker pull chronograf@sha256:8b40f33611523df5e1047fc1a438f909da5e5125fbe7d04c407921017f0d736f
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
$ docker pull chronograf@sha256:33517945f260d32380a9856ae9a4b7eb2b059d9bdad91dafe439914342394f6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.5 MB (70535941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49dd64e4522e5e65394abc3e6b8a05c7989445e818773916c563e2e855e0fc28`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1777939200'
# Fri, 08 May 2026 19:40:44 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 08 May 2026 19:40:49 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Fri, 08 May 2026 19:40:49 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 08 May 2026 19:40:49 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 08 May 2026 19:40:49 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 08 May 2026 19:40:49 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 08 May 2026 19:40:49 GMT
VOLUME [/var/lib/chronograf]
# Fri, 08 May 2026 19:40:49 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 08 May 2026 19:40:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 08 May 2026 19:40:49 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:77e30ef52aeb52d8466baf0f50b54ed2fc0b421f44c49e5bf93682b27110f4d3`  
		Last Modified: Fri, 08 May 2026 18:22:59 GMT  
		Size: 30.3 MB (30257958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14bd79bc35505bac72815e6db9a305bc0fb469628671be936238ebf3c9963c08`  
		Last Modified: Fri, 08 May 2026 19:41:00 GMT  
		Size: 5.2 MB (5241757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5408b80a00d7f15558e232445414f414ebc409ac2c3ec5785fd28ec442e901db`  
		Last Modified: Fri, 08 May 2026 19:41:00 GMT  
		Size: 35.0 MB (35011833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787deaa881165deb2543c674eac941d693b605700c9583be127ce7ca340c81ae`  
		Last Modified: Fri, 08 May 2026 19:40:59 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0bfa9feb94a0d461aeacf42dfc916f191c2c8a59d632407a04da30075c2415c`  
		Last Modified: Fri, 08 May 2026 19:40:59 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8c0edb6fec6fe3cb9b39a240165044906995d3e48d9e1cffbc093c0ddd572ee`  
		Last Modified: Fri, 08 May 2026 19:41:00 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9` - unknown; unknown

```console
$ docker pull chronograf@sha256:20367ff39c81727e6e3025472ba5bd19f866add5bc11c14859bccc595b1cb07e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3133908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d70491e2d2e113338f8cc54d717364debc29640fb3f3711d7816e6d3c10d623`

```dockerfile
```

-	Layers:
	-	`sha256:3d3bdf8fa75e6bafef22d744c94bc02c17d3a5c58894982b22b9cd2f8ce7c225`  
		Last Modified: Fri, 08 May 2026 19:40:59 GMT  
		Size: 3.1 MB (3118141 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04cb51e287de9b43f9658f6855e92d3a5d93918f73a5fb058c07f2a78a6cd4db`  
		Last Modified: Fri, 08 May 2026 19:40:59 GMT  
		Size: 15.8 KB (15767 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.9` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:4fb8f5a88cb00a8434f6148d0eeb27ed2e113e95e558c9d685d1a2050c2c18f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.4 MB (63397280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed55a4a40684941eb2fa62c909234865cf5d717ba59f2c04b5a66d9125b20c2e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1777939200'
# Fri, 08 May 2026 19:44:54 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 08 May 2026 19:45:00 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Fri, 08 May 2026 19:45:00 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 08 May 2026 19:45:00 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 08 May 2026 19:45:00 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 08 May 2026 19:45:00 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 08 May 2026 19:45:00 GMT
VOLUME [/var/lib/chronograf]
# Fri, 08 May 2026 19:45:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 08 May 2026 19:45:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 08 May 2026 19:45:00 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:976dfa794c59ebfed71602151daddefd6dc6a747d5d0ff3934bce4d42d3677c5`  
		Last Modified: Fri, 08 May 2026 18:37:07 GMT  
		Size: 25.6 MB (25551243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c9b47b5d2e4110b7be1d4d0fe497de2b82a7b77f369d0359501a12ff84ec22d`  
		Last Modified: Fri, 08 May 2026 19:45:09 GMT  
		Size: 4.5 MB (4509996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc0891aa45032d42a327292ddcdd83e1189cf47f464b47c49fc27b8fe410514a`  
		Last Modified: Fri, 08 May 2026 19:45:10 GMT  
		Size: 33.3 MB (33311644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fd10c895343fe8c7cd2c13ab2fc137a2d41ac65b2a1017924496379adfe6d62`  
		Last Modified: Fri, 08 May 2026 19:45:09 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7a7f37cfe1435d329dc8b6929eb4c4aa5f9d63f33fe9f857bee4b0f4a67686b`  
		Last Modified: Fri, 08 May 2026 19:45:09 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b68f199919f7b49c07f73fec7c9b4cd93da37cb8a9a52a4e3e919393d1030536`  
		Last Modified: Fri, 08 May 2026 19:45:10 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9` - unknown; unknown

```console
$ docker pull chronograf@sha256:cc312c0c091cfe042206ac3c1da3623cac09277e88870ef5eff39e299e878419
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3136256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03d3606cdae0934f4cf0112d6cfbeee086227e67eaf0d67a45fdb63f86fc8eda`

```dockerfile
```

-	Layers:
	-	`sha256:5babf870bb2733009613fb6bd12358bbd747dd05ea4c85438690e4a02789a469`  
		Last Modified: Fri, 08 May 2026 19:45:09 GMT  
		Size: 3.1 MB (3120412 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9aad3be4ce124299fbd77f9ab2cab63c334c750d379a6cda5f260979f339015a`  
		Last Modified: Fri, 08 May 2026 19:45:09 GMT  
		Size: 15.8 KB (15844 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.9` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:00fd78923f67b967e85f3c874d7c046f1d68adae02e53864b4df52c88a23c0fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.2 MB (67179051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee1a67ff368f5510cf1680404a66bc5208938e9d82cef9e8b7787041bbf52787`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1777939200'
# Fri, 08 May 2026 19:42:37 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 08 May 2026 19:42:43 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Fri, 08 May 2026 19:42:43 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 08 May 2026 19:42:43 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 08 May 2026 19:42:43 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 08 May 2026 19:42:43 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 08 May 2026 19:42:43 GMT
VOLUME [/var/lib/chronograf]
# Fri, 08 May 2026 19:42:43 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 08 May 2026 19:42:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 08 May 2026 19:42:43 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:ab0f13d792ff9100407906fb422a0b62a8b437abde4c245e03f0366814be9aae`  
		Last Modified: Fri, 08 May 2026 18:25:06 GMT  
		Size: 28.7 MB (28742591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3844d08608307350b132ed1491cbc290669058e89e6ed3435786451bc6f02edf`  
		Last Modified: Fri, 08 May 2026 19:42:54 GMT  
		Size: 5.2 MB (5229780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:970b98a71369e2d33c93d0c702aa8e6d21c52bf061ebb0066029acdc978d6364`  
		Last Modified: Fri, 08 May 2026 19:42:54 GMT  
		Size: 33.2 MB (33182295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47038805eae378bd151a63ad31a251933f1138a3493469e09cb501a290392075`  
		Last Modified: Fri, 08 May 2026 19:42:53 GMT  
		Size: 12.2 KB (12243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e3b7eaecf44223189a194dc34c954043b49b957ee7c9bb5252e91c9e2f94d3f`  
		Last Modified: Fri, 08 May 2026 19:42:54 GMT  
		Size: 11.9 KB (11902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:513ef3e0324842442c3d8076c1c3ef69f90079a567e7a6e1b83b72f37453ca6c`  
		Last Modified: Fri, 08 May 2026 19:42:55 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9` - unknown; unknown

```console
$ docker pull chronograf@sha256:e14d184cc397afffea0859e8de39355e854d16e64901b7f0cc0a729968b2bc4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3134252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc15dc07337ce834770991c85e4861821a9e0a1426ea53c4b973b38069c947c4`

```dockerfile
```

-	Layers:
	-	`sha256:f0122b019b8e3dc360d131fb1cab400a846632e097f591a0f7b0cc5dc315c4f3`  
		Last Modified: Fri, 08 May 2026 19:42:54 GMT  
		Size: 3.1 MB (3118390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de510761d22ac050c13641ba54894f55fd167971183041826520f09d8e61b2ba`  
		Last Modified: Fri, 08 May 2026 19:42:53 GMT  
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
$ docker pull chronograf@sha256:8b40f33611523df5e1047fc1a438f909da5e5125fbe7d04c407921017f0d736f
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
$ docker pull chronograf@sha256:33517945f260d32380a9856ae9a4b7eb2b059d9bdad91dafe439914342394f6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.5 MB (70535941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49dd64e4522e5e65394abc3e6b8a05c7989445e818773916c563e2e855e0fc28`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1777939200'
# Fri, 08 May 2026 19:40:44 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 08 May 2026 19:40:49 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Fri, 08 May 2026 19:40:49 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 08 May 2026 19:40:49 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 08 May 2026 19:40:49 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 08 May 2026 19:40:49 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 08 May 2026 19:40:49 GMT
VOLUME [/var/lib/chronograf]
# Fri, 08 May 2026 19:40:49 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 08 May 2026 19:40:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 08 May 2026 19:40:49 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:77e30ef52aeb52d8466baf0f50b54ed2fc0b421f44c49e5bf93682b27110f4d3`  
		Last Modified: Fri, 08 May 2026 18:22:59 GMT  
		Size: 30.3 MB (30257958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14bd79bc35505bac72815e6db9a305bc0fb469628671be936238ebf3c9963c08`  
		Last Modified: Fri, 08 May 2026 19:41:00 GMT  
		Size: 5.2 MB (5241757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5408b80a00d7f15558e232445414f414ebc409ac2c3ec5785fd28ec442e901db`  
		Last Modified: Fri, 08 May 2026 19:41:00 GMT  
		Size: 35.0 MB (35011833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787deaa881165deb2543c674eac941d693b605700c9583be127ce7ca340c81ae`  
		Last Modified: Fri, 08 May 2026 19:40:59 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0bfa9feb94a0d461aeacf42dfc916f191c2c8a59d632407a04da30075c2415c`  
		Last Modified: Fri, 08 May 2026 19:40:59 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8c0edb6fec6fe3cb9b39a240165044906995d3e48d9e1cffbc093c0ddd572ee`  
		Last Modified: Fri, 08 May 2026 19:41:00 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9.4` - unknown; unknown

```console
$ docker pull chronograf@sha256:20367ff39c81727e6e3025472ba5bd19f866add5bc11c14859bccc595b1cb07e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3133908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d70491e2d2e113338f8cc54d717364debc29640fb3f3711d7816e6d3c10d623`

```dockerfile
```

-	Layers:
	-	`sha256:3d3bdf8fa75e6bafef22d744c94bc02c17d3a5c58894982b22b9cd2f8ce7c225`  
		Last Modified: Fri, 08 May 2026 19:40:59 GMT  
		Size: 3.1 MB (3118141 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04cb51e287de9b43f9658f6855e92d3a5d93918f73a5fb058c07f2a78a6cd4db`  
		Last Modified: Fri, 08 May 2026 19:40:59 GMT  
		Size: 15.8 KB (15767 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.9.4` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:4fb8f5a88cb00a8434f6148d0eeb27ed2e113e95e558c9d685d1a2050c2c18f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.4 MB (63397280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed55a4a40684941eb2fa62c909234865cf5d717ba59f2c04b5a66d9125b20c2e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1777939200'
# Fri, 08 May 2026 19:44:54 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 08 May 2026 19:45:00 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Fri, 08 May 2026 19:45:00 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 08 May 2026 19:45:00 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 08 May 2026 19:45:00 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 08 May 2026 19:45:00 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 08 May 2026 19:45:00 GMT
VOLUME [/var/lib/chronograf]
# Fri, 08 May 2026 19:45:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 08 May 2026 19:45:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 08 May 2026 19:45:00 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:976dfa794c59ebfed71602151daddefd6dc6a747d5d0ff3934bce4d42d3677c5`  
		Last Modified: Fri, 08 May 2026 18:37:07 GMT  
		Size: 25.6 MB (25551243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c9b47b5d2e4110b7be1d4d0fe497de2b82a7b77f369d0359501a12ff84ec22d`  
		Last Modified: Fri, 08 May 2026 19:45:09 GMT  
		Size: 4.5 MB (4509996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc0891aa45032d42a327292ddcdd83e1189cf47f464b47c49fc27b8fe410514a`  
		Last Modified: Fri, 08 May 2026 19:45:10 GMT  
		Size: 33.3 MB (33311644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fd10c895343fe8c7cd2c13ab2fc137a2d41ac65b2a1017924496379adfe6d62`  
		Last Modified: Fri, 08 May 2026 19:45:09 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7a7f37cfe1435d329dc8b6929eb4c4aa5f9d63f33fe9f857bee4b0f4a67686b`  
		Last Modified: Fri, 08 May 2026 19:45:09 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b68f199919f7b49c07f73fec7c9b4cd93da37cb8a9a52a4e3e919393d1030536`  
		Last Modified: Fri, 08 May 2026 19:45:10 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9.4` - unknown; unknown

```console
$ docker pull chronograf@sha256:cc312c0c091cfe042206ac3c1da3623cac09277e88870ef5eff39e299e878419
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3136256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03d3606cdae0934f4cf0112d6cfbeee086227e67eaf0d67a45fdb63f86fc8eda`

```dockerfile
```

-	Layers:
	-	`sha256:5babf870bb2733009613fb6bd12358bbd747dd05ea4c85438690e4a02789a469`  
		Last Modified: Fri, 08 May 2026 19:45:09 GMT  
		Size: 3.1 MB (3120412 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9aad3be4ce124299fbd77f9ab2cab63c334c750d379a6cda5f260979f339015a`  
		Last Modified: Fri, 08 May 2026 19:45:09 GMT  
		Size: 15.8 KB (15844 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.9.4` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:00fd78923f67b967e85f3c874d7c046f1d68adae02e53864b4df52c88a23c0fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.2 MB (67179051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee1a67ff368f5510cf1680404a66bc5208938e9d82cef9e8b7787041bbf52787`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1777939200'
# Fri, 08 May 2026 19:42:37 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 08 May 2026 19:42:43 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Fri, 08 May 2026 19:42:43 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 08 May 2026 19:42:43 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 08 May 2026 19:42:43 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 08 May 2026 19:42:43 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 08 May 2026 19:42:43 GMT
VOLUME [/var/lib/chronograf]
# Fri, 08 May 2026 19:42:43 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 08 May 2026 19:42:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 08 May 2026 19:42:43 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:ab0f13d792ff9100407906fb422a0b62a8b437abde4c245e03f0366814be9aae`  
		Last Modified: Fri, 08 May 2026 18:25:06 GMT  
		Size: 28.7 MB (28742591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3844d08608307350b132ed1491cbc290669058e89e6ed3435786451bc6f02edf`  
		Last Modified: Fri, 08 May 2026 19:42:54 GMT  
		Size: 5.2 MB (5229780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:970b98a71369e2d33c93d0c702aa8e6d21c52bf061ebb0066029acdc978d6364`  
		Last Modified: Fri, 08 May 2026 19:42:54 GMT  
		Size: 33.2 MB (33182295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47038805eae378bd151a63ad31a251933f1138a3493469e09cb501a290392075`  
		Last Modified: Fri, 08 May 2026 19:42:53 GMT  
		Size: 12.2 KB (12243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e3b7eaecf44223189a194dc34c954043b49b957ee7c9bb5252e91c9e2f94d3f`  
		Last Modified: Fri, 08 May 2026 19:42:54 GMT  
		Size: 11.9 KB (11902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:513ef3e0324842442c3d8076c1c3ef69f90079a567e7a6e1b83b72f37453ca6c`  
		Last Modified: Fri, 08 May 2026 19:42:55 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9.4` - unknown; unknown

```console
$ docker pull chronograf@sha256:e14d184cc397afffea0859e8de39355e854d16e64901b7f0cc0a729968b2bc4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3134252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc15dc07337ce834770991c85e4861821a9e0a1426ea53c4b973b38069c947c4`

```dockerfile
```

-	Layers:
	-	`sha256:f0122b019b8e3dc360d131fb1cab400a846632e097f591a0f7b0cc5dc315c4f3`  
		Last Modified: Fri, 08 May 2026 19:42:54 GMT  
		Size: 3.1 MB (3118390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de510761d22ac050c13641ba54894f55fd167971183041826520f09d8e61b2ba`  
		Last Modified: Fri, 08 May 2026 19:42:53 GMT  
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
$ docker pull chronograf@sha256:be0d839a52d44e71953d0b2836e8a5fbabb1fe7512aec618d48daa4fa44ed60a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:80f0eac35fdf4e62dfb101e808d23934c0c8418d946c40eef1bda748a8eb716c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62334787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1df51aab599500a1d5705e60635ce7ec1dc518251bcae39c434ef849f3a5bed`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Thu, 07 May 2026 17:43:20 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Thu, 07 May 2026 17:43:20 GMT
RUN apk add --no-cache ca-certificates setpriv &&     update-ca-certificates # buildkit
# Thu, 07 May 2026 17:43:25 GMT
ENV CHRONOGRAF_VERSION=1.11.2
# Thu, 07 May 2026 17:43:25 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S chronograf &&     adduser -S chronograf -G chronograf &&     mkdir -m 0750 -p /var/lib/chronograf &&     chown chronograf:chronograf /var/lib/chronograf # buildkit
# Thu, 07 May 2026 17:43:25 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Thu, 07 May 2026 17:43:25 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Thu, 07 May 2026 17:43:25 GMT
EXPOSE map[8888/tcp:{}]
# Thu, 07 May 2026 17:43:25 GMT
VOLUME [/var/lib/chronograf]
# Thu, 07 May 2026 17:43:25 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 07 May 2026 17:43:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 07 May 2026 17:43:25 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5f034fedb34a4c678230b662d88eead9f8327232402638bf43a349457f5af51`  
		Last Modified: Thu, 07 May 2026 17:43:38 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f387b1db623035224cf796e12a993c1c1f7a4b369bdeeb5e69b9dfa236f5be0`  
		Last Modified: Thu, 07 May 2026 17:43:39 GMT  
		Size: 312.2 KB (312193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36950b5f1bb549bd7a1db0f996523a6c41454afac370de0b8d28772164770e22`  
		Last Modified: Thu, 07 May 2026 17:43:40 GMT  
		Size: 58.2 MB (58189680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5d53388b5e8ad45e9e4d75047a3f99495f913bd091298d8cf56111072ec7482`  
		Last Modified: Thu, 07 May 2026 17:43:38 GMT  
		Size: 12.2 KB (12236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:758a472b1a9b3c3b5f474a8b06bc8c0d0f20e03bd4b65ec18316a19b0d2fb05e`  
		Last Modified: Thu, 07 May 2026 17:43:39 GMT  
		Size: 11.9 KB (11895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09eeca9b42ec7a839911d9cb1dbb30cde2510a076fd90e2a24bb8daf6967b36b`  
		Last Modified: Thu, 07 May 2026 17:43:39 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:20f564bf4977e07cdee0af68ac679d481df1edfc5b16cfe5c4f212d1287488bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.1 KB (287057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf62ab165d3d6eedbce59839293260aa5898128b6d663a167676dc41df4495dd`

```dockerfile
```

-	Layers:
	-	`sha256:379aecff8e7d7778fe0361cd9d05ebacd639bbb4bae468b1d13cfc8eaea61b87`  
		Last Modified: Thu, 07 May 2026 17:43:38 GMT  
		Size: 269.3 KB (269328 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0abeb95209c442bcfbeec66105986fcc5bba3da5e7f7017351cb3c7373dfe90e`  
		Last Modified: Thu, 07 May 2026 17:43:38 GMT  
		Size: 17.7 KB (17729 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:latest`

```console
$ docker pull chronograf@sha256:2eebdc6f5b0e65845ff8e9e44b54f55fd137154848ff0924dd5d79f68def9721
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
$ docker pull chronograf@sha256:54e32cd3e48ac4c3def6925aa03676dc0d8a16a64eed75411011f4f527f55d45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.3 MB (96301797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad189a1b2cfe7415ac0b93a1307700b8dd6a44f716adba4f7470481115b158d5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:41:01 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 08 May 2026 19:41:08 GMT
ENV CHRONOGRAF_VERSION=1.11.2
# Fri, 08 May 2026 19:41:08 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 08 May 2026 19:41:08 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 08 May 2026 19:41:08 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 08 May 2026 19:41:08 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 08 May 2026 19:41:08 GMT
VOLUME [/var/lib/chronograf]
# Fri, 08 May 2026 19:41:08 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 08 May 2026 19:41:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 08 May 2026 19:41:08 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:9b02e9fcb40102eae20d9d1fc7594b44328f4a3eb9b8a3bdb7db283d10840a30`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 28.2 MB (28236282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1d3fd0ca26ff2a170b79fb17a608035a5b66d1ae4ae2162ba9fe03b5013b9c2`  
		Last Modified: Fri, 08 May 2026 19:41:24 GMT  
		Size: 7.9 MB (7880771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1600d57770479f768c269fcee3529bba79d87676b97fccfa0d6986e6fb35b123`  
		Last Modified: Fri, 08 May 2026 19:41:25 GMT  
		Size: 60.2 MB (60160268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf794b3a83674671e9ab42987f1abf1a9e955e6002b245a0009e665dfcab6a0f`  
		Last Modified: Fri, 08 May 2026 19:41:24 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:334c2c3c5016987b28b99b8fd10bcf0e635891be21a01e875f54aa240fc771d3`  
		Last Modified: Fri, 08 May 2026 19:41:24 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b18a35825a88afbfe2d23a81eecf482053eb67293f59ab1a712e409f73d7e4f`  
		Last Modified: Fri, 08 May 2026 19:41:25 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:1138670f6509706eb0215dc17a4c7aace6b1ec3c94ae65e1193609f277b66a51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2889784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7312f318ce642b41773dd4ee48f6dde77882dacee25793cea5d376b990668039`

```dockerfile
```

-	Layers:
	-	`sha256:6a125d7c59f75e398266ea88913b40be232725ee1ef89a1c84c8c88fe7b46d50`  
		Last Modified: Fri, 08 May 2026 19:41:24 GMT  
		Size: 2.9 MB (2873700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2961714e758eddbdf4ad9df34423a4746d8abd41bb1cf928409032e6b2450a22`  
		Last Modified: Fri, 08 May 2026 19:41:23 GMT  
		Size: 16.1 KB (16084 bytes)  
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
$ docker pull chronograf@sha256:06039e8fe6660d86b1c58ddac69bfb6992add3e7bada41f53dccfb72a6262cfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.0 MB (93017873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94183117c18e70abcb1fa65164a7ea3de8131443b142d8b3e7613026b5c1f57f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:42:44 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 08 May 2026 19:42:51 GMT
ENV CHRONOGRAF_VERSION=1.11.2
# Fri, 08 May 2026 19:42:51 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 08 May 2026 19:42:51 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 08 May 2026 19:42:51 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 08 May 2026 19:42:51 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 08 May 2026 19:42:51 GMT
VOLUME [/var/lib/chronograf]
# Fri, 08 May 2026 19:42:51 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 08 May 2026 19:42:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 08 May 2026 19:42:51 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:6a2d07df495cc055bce0251fe801ee08db90750f52e43a555be5dfd8f5023783`  
		Last Modified: Fri, 08 May 2026 18:24:52 GMT  
		Size: 28.1 MB (28116165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:014811a135ddb7b07f7c1d6306e500555c1eb6652b80c686929511fcaa4ec072`  
		Last Modified: Fri, 08 May 2026 19:43:05 GMT  
		Size: 7.7 MB (7698454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1fb404ada7af90249b507c8dd6121125a7c52b953ffd4543d339d8bf7b2db94`  
		Last Modified: Fri, 08 May 2026 19:43:08 GMT  
		Size: 57.2 MB (57178776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08b728e1b5f393e36b5537563f4ae62732cf16f2065b558fcbdf56f9022a9a7f`  
		Last Modified: Fri, 08 May 2026 19:43:05 GMT  
		Size: 12.3 KB (12252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da5ec718ae5a77034d4eed65124387bffd6fda82394f214c9d4332a91219b448`  
		Last Modified: Fri, 08 May 2026 19:43:05 GMT  
		Size: 11.9 KB (11911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b84a3b1086e4e5daebc8a431314e56550afff37660f6d6f0e45265efe2aaf59`  
		Last Modified: Fri, 08 May 2026 19:43:06 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:0b640e32cbc0cec417e8368b9f511770bbb324545f70d758ca3d336a3bbb53d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2889106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7ac5d2b3233e3020ea6f2d5d2b46ba5e11a072406a18a391e4ddb8a3a9ddca6`

```dockerfile
```

-	Layers:
	-	`sha256:2d81cbb5f1f2ab9afe346e27664b487561e7949f8026ce308e0c0834a78b24eb`  
		Last Modified: Fri, 08 May 2026 19:43:05 GMT  
		Size: 2.9 MB (2872914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ec10703780086fed811e3f13be45453a584373a5fbd96578feffd56602b8d31`  
		Last Modified: Fri, 08 May 2026 19:43:05 GMT  
		Size: 16.2 KB (16192 bytes)  
		MIME: application/vnd.in-toto+json
