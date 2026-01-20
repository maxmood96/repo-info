<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `chronograf`

-	[`chronograf:1.10`](#chronograf110)
-	[`chronograf:1.10-alpine`](#chronograf110-alpine)
-	[`chronograf:1.10.9`](#chronograf1109)
-	[`chronograf:1.10.9-alpine`](#chronograf1109-alpine)
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
$ docker pull chronograf@sha256:858f06c5e2ab525a8193a5f190a987b2a9b0f0dfb05f00e883a6d4215ab5a999
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
$ docker pull chronograf@sha256:0ca02df258be555db97f05cf143c919bde15c593557c0bdd247379fa01c63842
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.0 MB (85000209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:711a95539008f28a45eee16e13d093cded16283e271f0d487d78fce3279a71d2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:13:54 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 13 Jan 2026 02:13:59 GMT
ENV CHRONOGRAF_VERSION=1.10.9
# Tue, 13 Jan 2026 02:13:59 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 13 Jan 2026 02:13:59 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 13 Jan 2026 02:13:59 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 13 Jan 2026 02:13:59 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 13 Jan 2026 02:13:59 GMT
VOLUME [/var/lib/chronograf]
# Tue, 13 Jan 2026 02:13:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 13 Jan 2026 02:13:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Jan 2026 02:13:59 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:c02d17997ce3d2c82e082235ea0b5152d06ee659c4e2fabcf1e0079312f1bcde`  
		Last Modified: Tue, 13 Jan 2026 00:41:50 GMT  
		Size: 28.2 MB (28228572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f97a4c03663264daa07043a3f29f2d20b0f8166009a68253c911509bc54d620`  
		Last Modified: Tue, 13 Jan 2026 02:14:19 GMT  
		Size: 7.9 MB (7879303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1de3fdab9946b7fe91f7f64835d147fd55a0c2dd876ff89abcb4932975b563c`  
		Last Modified: Tue, 13 Jan 2026 02:14:27 GMT  
		Size: 48.9 MB (48867877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b98f709a51e0b7ad076ff093e6fbc62937fc424c617b44afb09050e162934c2`  
		Last Modified: Tue, 13 Jan 2026 02:14:11 GMT  
		Size: 12.2 KB (12240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d2105baf2c6f199637a6f8da17dd041da224c83e726af6c49c8490825887745`  
		Last Modified: Tue, 13 Jan 2026 02:14:19 GMT  
		Size: 11.9 KB (11903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc1a26f63feaf4dd4395b0829102a09d484d4da534de28a323abf3b4a7bee141`  
		Last Modified: Tue, 13 Jan 2026 02:14:19 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:d18723ded2d8ae5789aa7c7109d5a2728eb08a049cf9931fe5e85b64e0ca4c73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2871815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:859a2ca904a49afc214c3812aa4311aa8a9c03803927cf254d97df1a2e83312a`

```dockerfile
```

-	Layers:
	-	`sha256:26bf29e8df90ec3896704fc9859e3fee325b42d6795b179d2127f488258d08c5`  
		Last Modified: Tue, 13 Jan 2026 02:14:11 GMT  
		Size: 2.9 MB (2855730 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac887deeede4277c4720d5beede9b3f511ddda0275a34a8c86c9acffd9d8901f`  
		Last Modified: Tue, 13 Jan 2026 04:39:26 GMT  
		Size: 16.1 KB (16085 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.10` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:118d4a298e4756953ee1acc65f510e9b7772e025751c4451027be26d6283c73f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76790409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd0b7dd595a1be3b19803d456a8d8cdba8f542788c31f5d26747a1853d141b2c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 03:02:49 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 13 Jan 2026 03:02:57 GMT
ENV CHRONOGRAF_VERSION=1.10.9
# Tue, 13 Jan 2026 03:02:57 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 13 Jan 2026 03:02:57 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 13 Jan 2026 03:02:57 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 13 Jan 2026 03:02:57 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 13 Jan 2026 03:02:57 GMT
VOLUME [/var/lib/chronograf]
# Tue, 13 Jan 2026 03:02:57 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 13 Jan 2026 03:02:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Jan 2026 03:02:57 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:ce9b9afe4e779d4b89f92e338fcd7dde1b11be3e68cd4c559a53dc9328ce4b5e`  
		Last Modified: Tue, 13 Jan 2026 00:42:08 GMT  
		Size: 23.9 MB (23934118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98636f48664fa7713ca92453907c30a986eb7904d5b61e9b5600939686558872`  
		Last Modified: Tue, 13 Jan 2026 03:16:21 GMT  
		Size: 6.5 MB (6511797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afcc9f19f53b9cf27f68f3bf6ffac9e16876c44c2dccba2d42553b457f09f6a9`  
		Last Modified: Tue, 13 Jan 2026 03:03:09 GMT  
		Size: 46.3 MB (46320032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71e832636be91f6cc6b53e6818a295ee19e07ccd462ae2e3c1e21372d09db364`  
		Last Modified: Tue, 13 Jan 2026 03:03:15 GMT  
		Size: 12.2 KB (12244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45563d6b533d54cb0923504de0a85d169c2eb16dea1a2bd59a45c923343ce386`  
		Last Modified: Tue, 13 Jan 2026 03:03:15 GMT  
		Size: 11.9 KB (11903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c7798c5b24c073ddea2b190bd1d3ca3d1950cd905ccccb02cb48628d269cff`  
		Last Modified: Tue, 13 Jan 2026 03:03:08 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:dadc0272545bdb4d79c6821ef43eb9a925d893b1eaeb4ee2d3cf2f188d7812c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2874196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1acc4e39a06aefb56c7f9e35ebeab2574b57317d10790d0e3311c59c3a3674c8`

```dockerfile
```

-	Layers:
	-	`sha256:ab03fd2077b16e627f201c398a16843df1c165c2856cbe02e571a7462fbf3c5e`  
		Last Modified: Tue, 13 Jan 2026 04:39:31 GMT  
		Size: 2.9 MB (2858027 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:198292ca1a6d344ac0e12376713d0b2d6f2cc1269871cede2e0ef2769ced95ba`  
		Last Modified: Tue, 13 Jan 2026 04:39:31 GMT  
		Size: 16.2 KB (16169 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.10` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:8fabc493b21b1a54965004da2d26b414d67d449655ff23fd3d3bac87b00de090
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.8 MB (81837705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d86037b14ea2e39a2df4fc316eab05973e03a911596ff0a243024a8208e2f1c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:19:43 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 13 Jan 2026 02:19:50 GMT
ENV CHRONOGRAF_VERSION=1.10.9
# Tue, 13 Jan 2026 02:19:50 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 13 Jan 2026 02:19:50 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 13 Jan 2026 02:19:50 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 13 Jan 2026 02:19:50 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 13 Jan 2026 02:19:50 GMT
VOLUME [/var/lib/chronograf]
# Tue, 13 Jan 2026 02:19:50 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 13 Jan 2026 02:19:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Jan 2026 02:19:50 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:33bdc9671af8942d96d2f78f67aeec06580065dde1272decac3732689ec7c0e8`  
		Last Modified: Tue, 13 Jan 2026 00:42:09 GMT  
		Size: 28.1 MB (28107889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cc6310fab39afa190ecc5161cceaa1eb36695352620a557f88e94c3a838721b`  
		Last Modified: Tue, 13 Jan 2026 02:20:09 GMT  
		Size: 7.7 MB (7696876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:549a592ab74e868f6aef56b9688e0a142cfeaad538cf0f689c2a3394daf66571`  
		Last Modified: Tue, 13 Jan 2026 02:20:12 GMT  
		Size: 46.0 MB (46008476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a988c038996109a0a07e5713dcb205aa4ff8a19cdc93a075645d0ec04494b80e`  
		Last Modified: Tue, 13 Jan 2026 02:20:08 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c5f351ad8064c72fb1f03aa05a2c7eb8549aa94f73af89b58980523f92ef535`  
		Last Modified: Tue, 13 Jan 2026 02:20:01 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a94dcc0d0c7256c16118217f500f6aad9381085f822785282de69d1305f95c2`  
		Last Modified: Tue, 13 Jan 2026 02:20:08 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:9737f03ac4f5bddfd3ae0a95a33f3a30899b993b88c8de1e34d68411db4c708a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2872195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c4ceccea032644b03a8620d1eda2192df4e66894d011334aabf6cf48acbbbd0`

```dockerfile
```

-	Layers:
	-	`sha256:efb72d9c089b44658955c2eba33b0f9f78a9cb89c105abc89cc127f199de6e47`  
		Last Modified: Tue, 13 Jan 2026 04:39:36 GMT  
		Size: 2.9 MB (2856003 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46c09c314009ba98652c89fb65f2c69181b95796d7a038651b0d8b2f780f77cb`  
		Last Modified: Tue, 13 Jan 2026 04:39:36 GMT  
		Size: 16.2 KB (16192 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.10-alpine`

```console
$ docker pull chronograf@sha256:3180124052084e1c0db5c3ba1bfa2f415c88fc7681ef14dfc189b324b9de03c6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.10-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:ee85eacf84a2662ece23a552d71cac84b11cbc3691d0f11533c47601629436a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33278682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd20a03649aab6179a8d0fbca439a20f70197cad1151f17c7db7f2bca99a7a41`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 07 Jan 2026 17:54:23 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 07 Jan 2026 17:54:24 GMT
RUN apk add --no-cache ca-certificates setpriv &&     update-ca-certificates # buildkit
# Wed, 07 Jan 2026 17:54:28 GMT
ENV CHRONOGRAF_VERSION=1.10.9
# Wed, 07 Jan 2026 17:54:28 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S chronograf &&     adduser -S chronograf -G chronograf &&     mkdir -m 0750 -p /var/lib/chronograf &&     chown chronograf:chronograf /var/lib/chronograf # buildkit
# Wed, 07 Jan 2026 17:54:28 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Wed, 07 Jan 2026 17:54:28 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Wed, 07 Jan 2026 17:54:28 GMT
EXPOSE map[8888/tcp:{}]
# Wed, 07 Jan 2026 17:54:28 GMT
VOLUME [/var/lib/chronograf]
# Wed, 07 Jan 2026 17:54:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 07 Jan 2026 17:54:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 07 Jan 2026 17:54:28 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:21 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bb809d47327d4436ed4d3ac5b0d2b676061f267bdacedb6a6a89d360a7dae09`  
		Last Modified: Wed, 07 Jan 2026 17:54:38 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb19a309f7b798855a902544be3186a07abbb407e814358b58cd1b89a39f5d3b`  
		Last Modified: Wed, 07 Jan 2026 17:54:37 GMT  
		Size: 314.7 KB (314652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1806ce0ba099140396732948f565b7509ae183daafc58c9c0232df4fa0e46272`  
		Last Modified: Wed, 07 Jan 2026 17:54:38 GMT  
		Size: 29.1 MB (29136854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76dad571ff7e915a85ce4aba703a3ebe307f73f0a42380e0eab5d5be6f6bc208`  
		Last Modified: Wed, 07 Jan 2026 17:54:44 GMT  
		Size: 12.2 KB (12236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd67712f58a31ea13eee2648165a6e2c172ef5cbff62d5d29689482836291302`  
		Last Modified: Wed, 07 Jan 2026 17:54:38 GMT  
		Size: 11.9 KB (11895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f130002e876e593ef18015df47078dcbf1e0f19cc533e5612a81b3e99b565166`  
		Last Modified: Wed, 07 Jan 2026 17:54:44 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:28567e0f67b9b9f0f79f9b8a40d1b45120c51e8222a75fbfeff2423cc7454275
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.8 KB (269841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0da3a04ba74c76ee4048ccb25b04a06ecc361c5298007bd4a37d0e9e8371a4b2`

```dockerfile
```

-	Layers:
	-	`sha256:4b9989c9337955baf604cfdcd89af7ca51dd00300557e0cb8354a7bddd10ebe2`  
		Last Modified: Wed, 07 Jan 2026 19:38:29 GMT  
		Size: 252.0 KB (252029 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd5523918f180b39378a1fc48e9db5f725a139f89fcd1a1b8eae374b7001d78a`  
		Last Modified: Wed, 07 Jan 2026 17:54:37 GMT  
		Size: 17.8 KB (17812 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.10.9`

```console
$ docker pull chronograf@sha256:858f06c5e2ab525a8193a5f190a987b2a9b0f0dfb05f00e883a6d4215ab5a999
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
$ docker pull chronograf@sha256:0ca02df258be555db97f05cf143c919bde15c593557c0bdd247379fa01c63842
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.0 MB (85000209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:711a95539008f28a45eee16e13d093cded16283e271f0d487d78fce3279a71d2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:13:54 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 13 Jan 2026 02:13:59 GMT
ENV CHRONOGRAF_VERSION=1.10.9
# Tue, 13 Jan 2026 02:13:59 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 13 Jan 2026 02:13:59 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 13 Jan 2026 02:13:59 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 13 Jan 2026 02:13:59 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 13 Jan 2026 02:13:59 GMT
VOLUME [/var/lib/chronograf]
# Tue, 13 Jan 2026 02:13:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 13 Jan 2026 02:13:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Jan 2026 02:13:59 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:c02d17997ce3d2c82e082235ea0b5152d06ee659c4e2fabcf1e0079312f1bcde`  
		Last Modified: Tue, 13 Jan 2026 00:41:50 GMT  
		Size: 28.2 MB (28228572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f97a4c03663264daa07043a3f29f2d20b0f8166009a68253c911509bc54d620`  
		Last Modified: Tue, 13 Jan 2026 02:14:19 GMT  
		Size: 7.9 MB (7879303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1de3fdab9946b7fe91f7f64835d147fd55a0c2dd876ff89abcb4932975b563c`  
		Last Modified: Tue, 13 Jan 2026 02:14:27 GMT  
		Size: 48.9 MB (48867877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b98f709a51e0b7ad076ff093e6fbc62937fc424c617b44afb09050e162934c2`  
		Last Modified: Tue, 13 Jan 2026 02:14:11 GMT  
		Size: 12.2 KB (12240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d2105baf2c6f199637a6f8da17dd041da224c83e726af6c49c8490825887745`  
		Last Modified: Tue, 13 Jan 2026 02:14:19 GMT  
		Size: 11.9 KB (11903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc1a26f63feaf4dd4395b0829102a09d484d4da534de28a323abf3b4a7bee141`  
		Last Modified: Tue, 13 Jan 2026 02:14:19 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10.9` - unknown; unknown

```console
$ docker pull chronograf@sha256:d18723ded2d8ae5789aa7c7109d5a2728eb08a049cf9931fe5e85b64e0ca4c73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2871815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:859a2ca904a49afc214c3812aa4311aa8a9c03803927cf254d97df1a2e83312a`

```dockerfile
```

-	Layers:
	-	`sha256:26bf29e8df90ec3896704fc9859e3fee325b42d6795b179d2127f488258d08c5`  
		Last Modified: Tue, 13 Jan 2026 02:14:11 GMT  
		Size: 2.9 MB (2855730 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac887deeede4277c4720d5beede9b3f511ddda0275a34a8c86c9acffd9d8901f`  
		Last Modified: Tue, 13 Jan 2026 04:39:26 GMT  
		Size: 16.1 KB (16085 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.10.9` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:118d4a298e4756953ee1acc65f510e9b7772e025751c4451027be26d6283c73f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76790409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd0b7dd595a1be3b19803d456a8d8cdba8f542788c31f5d26747a1853d141b2c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 03:02:49 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 13 Jan 2026 03:02:57 GMT
ENV CHRONOGRAF_VERSION=1.10.9
# Tue, 13 Jan 2026 03:02:57 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 13 Jan 2026 03:02:57 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 13 Jan 2026 03:02:57 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 13 Jan 2026 03:02:57 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 13 Jan 2026 03:02:57 GMT
VOLUME [/var/lib/chronograf]
# Tue, 13 Jan 2026 03:02:57 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 13 Jan 2026 03:02:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Jan 2026 03:02:57 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:ce9b9afe4e779d4b89f92e338fcd7dde1b11be3e68cd4c559a53dc9328ce4b5e`  
		Last Modified: Tue, 13 Jan 2026 00:42:08 GMT  
		Size: 23.9 MB (23934118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98636f48664fa7713ca92453907c30a986eb7904d5b61e9b5600939686558872`  
		Last Modified: Tue, 13 Jan 2026 03:16:21 GMT  
		Size: 6.5 MB (6511797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afcc9f19f53b9cf27f68f3bf6ffac9e16876c44c2dccba2d42553b457f09f6a9`  
		Last Modified: Tue, 13 Jan 2026 03:03:09 GMT  
		Size: 46.3 MB (46320032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71e832636be91f6cc6b53e6818a295ee19e07ccd462ae2e3c1e21372d09db364`  
		Last Modified: Tue, 13 Jan 2026 03:03:15 GMT  
		Size: 12.2 KB (12244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45563d6b533d54cb0923504de0a85d169c2eb16dea1a2bd59a45c923343ce386`  
		Last Modified: Tue, 13 Jan 2026 03:03:15 GMT  
		Size: 11.9 KB (11903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c7798c5b24c073ddea2b190bd1d3ca3d1950cd905ccccb02cb48628d269cff`  
		Last Modified: Tue, 13 Jan 2026 03:03:08 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10.9` - unknown; unknown

```console
$ docker pull chronograf@sha256:dadc0272545bdb4d79c6821ef43eb9a925d893b1eaeb4ee2d3cf2f188d7812c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2874196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1acc4e39a06aefb56c7f9e35ebeab2574b57317d10790d0e3311c59c3a3674c8`

```dockerfile
```

-	Layers:
	-	`sha256:ab03fd2077b16e627f201c398a16843df1c165c2856cbe02e571a7462fbf3c5e`  
		Last Modified: Tue, 13 Jan 2026 04:39:31 GMT  
		Size: 2.9 MB (2858027 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:198292ca1a6d344ac0e12376713d0b2d6f2cc1269871cede2e0ef2769ced95ba`  
		Last Modified: Tue, 13 Jan 2026 04:39:31 GMT  
		Size: 16.2 KB (16169 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.10.9` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:8fabc493b21b1a54965004da2d26b414d67d449655ff23fd3d3bac87b00de090
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.8 MB (81837705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d86037b14ea2e39a2df4fc316eab05973e03a911596ff0a243024a8208e2f1c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:19:43 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 13 Jan 2026 02:19:50 GMT
ENV CHRONOGRAF_VERSION=1.10.9
# Tue, 13 Jan 2026 02:19:50 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 13 Jan 2026 02:19:50 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 13 Jan 2026 02:19:50 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 13 Jan 2026 02:19:50 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 13 Jan 2026 02:19:50 GMT
VOLUME [/var/lib/chronograf]
# Tue, 13 Jan 2026 02:19:50 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 13 Jan 2026 02:19:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Jan 2026 02:19:50 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:33bdc9671af8942d96d2f78f67aeec06580065dde1272decac3732689ec7c0e8`  
		Last Modified: Tue, 13 Jan 2026 00:42:09 GMT  
		Size: 28.1 MB (28107889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cc6310fab39afa190ecc5161cceaa1eb36695352620a557f88e94c3a838721b`  
		Last Modified: Tue, 13 Jan 2026 02:20:09 GMT  
		Size: 7.7 MB (7696876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:549a592ab74e868f6aef56b9688e0a142cfeaad538cf0f689c2a3394daf66571`  
		Last Modified: Tue, 13 Jan 2026 02:20:12 GMT  
		Size: 46.0 MB (46008476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a988c038996109a0a07e5713dcb205aa4ff8a19cdc93a075645d0ec04494b80e`  
		Last Modified: Tue, 13 Jan 2026 02:20:08 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c5f351ad8064c72fb1f03aa05a2c7eb8549aa94f73af89b58980523f92ef535`  
		Last Modified: Tue, 13 Jan 2026 02:20:01 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a94dcc0d0c7256c16118217f500f6aad9381085f822785282de69d1305f95c2`  
		Last Modified: Tue, 13 Jan 2026 02:20:08 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10.9` - unknown; unknown

```console
$ docker pull chronograf@sha256:9737f03ac4f5bddfd3ae0a95a33f3a30899b993b88c8de1e34d68411db4c708a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2872195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c4ceccea032644b03a8620d1eda2192df4e66894d011334aabf6cf48acbbbd0`

```dockerfile
```

-	Layers:
	-	`sha256:efb72d9c089b44658955c2eba33b0f9f78a9cb89c105abc89cc127f199de6e47`  
		Last Modified: Tue, 13 Jan 2026 04:39:36 GMT  
		Size: 2.9 MB (2856003 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46c09c314009ba98652c89fb65f2c69181b95796d7a038651b0d8b2f780f77cb`  
		Last Modified: Tue, 13 Jan 2026 04:39:36 GMT  
		Size: 16.2 KB (16192 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.10.9-alpine`

```console
$ docker pull chronograf@sha256:3180124052084e1c0db5c3ba1bfa2f415c88fc7681ef14dfc189b324b9de03c6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.10.9-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:ee85eacf84a2662ece23a552d71cac84b11cbc3691d0f11533c47601629436a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33278682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd20a03649aab6179a8d0fbca439a20f70197cad1151f17c7db7f2bca99a7a41`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 07 Jan 2026 17:54:23 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 07 Jan 2026 17:54:24 GMT
RUN apk add --no-cache ca-certificates setpriv &&     update-ca-certificates # buildkit
# Wed, 07 Jan 2026 17:54:28 GMT
ENV CHRONOGRAF_VERSION=1.10.9
# Wed, 07 Jan 2026 17:54:28 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S chronograf &&     adduser -S chronograf -G chronograf &&     mkdir -m 0750 -p /var/lib/chronograf &&     chown chronograf:chronograf /var/lib/chronograf # buildkit
# Wed, 07 Jan 2026 17:54:28 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Wed, 07 Jan 2026 17:54:28 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Wed, 07 Jan 2026 17:54:28 GMT
EXPOSE map[8888/tcp:{}]
# Wed, 07 Jan 2026 17:54:28 GMT
VOLUME [/var/lib/chronograf]
# Wed, 07 Jan 2026 17:54:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 07 Jan 2026 17:54:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 07 Jan 2026 17:54:28 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:21 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bb809d47327d4436ed4d3ac5b0d2b676061f267bdacedb6a6a89d360a7dae09`  
		Last Modified: Wed, 07 Jan 2026 17:54:38 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb19a309f7b798855a902544be3186a07abbb407e814358b58cd1b89a39f5d3b`  
		Last Modified: Wed, 07 Jan 2026 17:54:37 GMT  
		Size: 314.7 KB (314652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1806ce0ba099140396732948f565b7509ae183daafc58c9c0232df4fa0e46272`  
		Last Modified: Wed, 07 Jan 2026 17:54:38 GMT  
		Size: 29.1 MB (29136854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76dad571ff7e915a85ce4aba703a3ebe307f73f0a42380e0eab5d5be6f6bc208`  
		Last Modified: Wed, 07 Jan 2026 17:54:44 GMT  
		Size: 12.2 KB (12236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd67712f58a31ea13eee2648165a6e2c172ef5cbff62d5d29689482836291302`  
		Last Modified: Wed, 07 Jan 2026 17:54:38 GMT  
		Size: 11.9 KB (11895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f130002e876e593ef18015df47078dcbf1e0f19cc533e5612a81b3e99b565166`  
		Last Modified: Wed, 07 Jan 2026 17:54:44 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10.9-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:28567e0f67b9b9f0f79f9b8a40d1b45120c51e8222a75fbfeff2423cc7454275
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.8 KB (269841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0da3a04ba74c76ee4048ccb25b04a06ecc361c5298007bd4a37d0e9e8371a4b2`

```dockerfile
```

-	Layers:
	-	`sha256:4b9989c9337955baf604cfdcd89af7ca51dd00300557e0cb8354a7bddd10ebe2`  
		Last Modified: Wed, 07 Jan 2026 19:38:29 GMT  
		Size: 252.0 KB (252029 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd5523918f180b39378a1fc48e9db5f725a139f89fcd1a1b8eae374b7001d78a`  
		Last Modified: Wed, 07 Jan 2026 17:54:37 GMT  
		Size: 17.8 KB (17812 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.7`

```console
$ docker pull chronograf@sha256:7b84adbafd53e66ca11e93a5cc1c411b5c8f3169e5177a480869b2f3f0d691d7
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
$ docker pull chronograf@sha256:c697a1eb4df17ee93f762eee018d2ff00ee4ab0f6be961bd6fc13db3380cd51d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.2 MB (69230633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8856cb0a97df83fd642c279a766d0b7af370d3b551ebb5bfe8145acd7d9cb77b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1768176000'
# Tue, 13 Jan 2026 02:12:12 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 13 Jan 2026 02:12:18 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 13 Jan 2026 02:12:18 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 13 Jan 2026 02:12:18 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 13 Jan 2026 02:12:18 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 13 Jan 2026 02:12:18 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 13 Jan 2026 02:12:18 GMT
VOLUME [/var/lib/chronograf]
# Tue, 13 Jan 2026 02:12:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 13 Jan 2026 02:12:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Jan 2026 02:12:18 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:bd1b97a95a10ded4767bfcdbb3d042b961d107d141121fdbb255239f0ca115f4`  
		Last Modified: Tue, 13 Jan 2026 00:42:23 GMT  
		Size: 30.3 MB (30258497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb6b0e2cd7abe524ab0af4a07f8f893bde79644ca44f970a929e11ed73cbf6af`  
		Last Modified: Tue, 13 Jan 2026 02:12:36 GMT  
		Size: 4.2 MB (4209325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d365326643172de5088f73fa37865f20ab65370b3dbdc024bd1e2f4d7bc13254`  
		Last Modified: Tue, 13 Jan 2026 02:12:30 GMT  
		Size: 34.7 MB (34738426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fda7ad3a0566d72b74d48200a97f531482364b5defeb249d4d17ed8b5222ee7`  
		Last Modified: Tue, 13 Jan 2026 02:12:29 GMT  
		Size: 12.2 KB (12244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a62b23f760546f6a2724ad171d851e47d389eb5fd56c71eac6e45471e9703c8`  
		Last Modified: Tue, 13 Jan 2026 02:12:36 GMT  
		Size: 11.9 KB (11902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:761820abfe35a527b101046674ae9c6dde68bc6486afdfc58ac568caaaeae64e`  
		Last Modified: Tue, 13 Jan 2026 02:12:30 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7` - unknown; unknown

```console
$ docker pull chronograf@sha256:2593cd6b1e6f6708a55799333e20d20d88e288acd06aa55ea0102c8e530de84c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3064607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1692b1f9d2b287c95792bb8f36e2a422efb85708dbef1840c0cf87478786484c`

```dockerfile
```

-	Layers:
	-	`sha256:6360525c0f28af986c566ad83830611dcaea13dea89fa3fc11d2b7be39f937e1`  
		Last Modified: Tue, 13 Jan 2026 04:39:41 GMT  
		Size: 3.0 MB (3048873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93955f9eb57046d2f290db14525a369a94a974e13eebf59c04f6a1b0bb76e156`  
		Last Modified: Tue, 13 Jan 2026 02:12:29 GMT  
		Size: 15.7 KB (15734 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.7` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:f897d44a405c9e7421f6eccb8637fff14e24c08ada07f58248cbb9faa4e3ab18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62179885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee05d2950d2c1c05d7a9c35e48cb9256b0cdb7056031282e9d11598f1c5d34ba`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1768176000'
# Tue, 13 Jan 2026 02:59:11 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 13 Jan 2026 02:59:19 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 13 Jan 2026 02:59:19 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 13 Jan 2026 02:59:19 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 13 Jan 2026 02:59:19 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 13 Jan 2026 02:59:19 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 13 Jan 2026 02:59:19 GMT
VOLUME [/var/lib/chronograf]
# Tue, 13 Jan 2026 02:59:19 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 13 Jan 2026 02:59:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Jan 2026 02:59:19 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:ddab8730b1df461111046cd88b7848f70955e854e29bbbfa3ae304f7ec801442`  
		Last Modified: Tue, 13 Jan 2026 00:42:31 GMT  
		Size: 25.5 MB (25546235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9251a13741298223fdfdc9be78334db81ff4f549edd0727a380f393b38821619`  
		Last Modified: Tue, 13 Jan 2026 02:59:36 GMT  
		Size: 3.5 MB (3511688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48701c41355a33b1cd2868933c2ed76cae2545cd6346942d912cf37ea72e476f`  
		Last Modified: Tue, 13 Jan 2026 02:59:30 GMT  
		Size: 33.1 MB (33097569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01af9d592d73eeef1d21a754c55f04464d6f50e5e310f9586072f3a741a5e0b8`  
		Last Modified: Tue, 13 Jan 2026 02:59:36 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41da3607200b9f79dfe6a0ddef1c9f298344dcb19a4f76189bf02e189becf75f`  
		Last Modified: Tue, 13 Jan 2026 02:59:36 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d21d2b0645d2ccc2bb0c832c5a8c992c01280f7558be590020cd6730f58aa85e`  
		Last Modified: Tue, 13 Jan 2026 02:59:30 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7` - unknown; unknown

```console
$ docker pull chronograf@sha256:bf4cf2341687afe9a445c1c1373316ed806e96f42449c1cb1315a3cac2eff827
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3066955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14f9b9c41a1375390f72f6a4b1f8c4199ec8ce5decac87f6a649ce9653c7c558`

```dockerfile
```

-	Layers:
	-	`sha256:b60089c4693066549ee8939dadefac4e1711458169d15d564dcd21d80a744a42`  
		Last Modified: Tue, 13 Jan 2026 02:59:29 GMT  
		Size: 3.1 MB (3051144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a8ca59e33c7bc7b0b8a83268aeb6d250c70a58b50fcf59c7b84eaed599e6974`  
		Last Modified: Tue, 13 Jan 2026 02:59:29 GMT  
		Size: 15.8 KB (15811 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.7` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:14d3f754c77264c27a6a84f79a5fd9d7aa7953e92ddfd74bbce2f56bc474eb1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66221678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d5786af0d6d216599b81a54b31142fac727f9cd420377d3d53ba0649a4801ab`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1768176000'
# Tue, 13 Jan 2026 02:16:16 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 13 Jan 2026 02:16:22 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 13 Jan 2026 02:16:22 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 13 Jan 2026 02:16:22 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 13 Jan 2026 02:16:22 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 13 Jan 2026 02:16:22 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 13 Jan 2026 02:16:22 GMT
VOLUME [/var/lib/chronograf]
# Tue, 13 Jan 2026 02:16:22 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 13 Jan 2026 02:16:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Jan 2026 02:16:22 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:7781088accb552d6473ed64f4649a64684d928b7cfad973d13e5c50942bf7a5b`  
		Last Modified: Tue, 13 Jan 2026 00:41:59 GMT  
		Size: 28.7 MB (28748518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33ab95430f23401ffe30c5b7d6aeff523932df0d14da602f2e0aa5f04c8778a0`  
		Last Modified: Tue, 13 Jan 2026 02:16:37 GMT  
		Size: 4.2 MB (4210612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02f55cd2a4f1c21030ff008f48d4d8b081ba2c0785c293cff39d918b865882cb`  
		Last Modified: Tue, 13 Jan 2026 02:16:40 GMT  
		Size: 33.2 MB (33238151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25378f999a0dd8ef23b56d4d771571d8112385054b577da39a46571b760947c8`  
		Last Modified: Tue, 13 Jan 2026 02:16:37 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d635ef5c076321b1cffcb4b7f02e38a1ee40c27ef9d9a2de87e79574abb52ad1`  
		Last Modified: Tue, 13 Jan 2026 02:16:51 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2daa28d65d5299f4239441883ccd2249f615b383b4b4381a3b85caba2a9ff784`  
		Last Modified: Tue, 13 Jan 2026 02:16:33 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7` - unknown; unknown

```console
$ docker pull chronograf@sha256:f91e5a4570d4cf7a6e7313352af25b57e7094096d32df05952be224449240591
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3064951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dfb4510cbc9d704fde2afb68e14092f92045eb2ab01c943a7017b55c247860a`

```dockerfile
```

-	Layers:
	-	`sha256:d6fb92f3a3ad8c7d311c0279eb81d2c0a1477b29731aab3e898bfe9c0ccebc3b`  
		Last Modified: Tue, 13 Jan 2026 04:40:01 GMT  
		Size: 3.0 MB (3049122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4123bf76b137451bf5f9f0ab59ca134e2ed2e0258631dddaf852414cd58a931d`  
		Last Modified: Tue, 13 Jan 2026 02:16:31 GMT  
		Size: 15.8 KB (15829 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.7-alpine`

```console
$ docker pull chronograf@sha256:f9bf8a3a9499f5324ca9b5f428e7ecbf8a4714d366e8a7920a8d06292f7d0511
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.7-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:0e68a8f6a33cec3ad19c936e80df9706efc6f4a6651f78b3373920f503a90deb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.5 MB (23499028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5704e6698a8163ec6cf9a9f4d2fc39455f7394b4b089fd3fe4fbbfcd3c84f5fc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 15 Aug 2025 14:37:23 GMT
ADD alpine-minirootfs-3.20.8-x86_64.tar.gz / # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["/bin/sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Fri, 15 Aug 2025 14:37:23 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
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
	-	`sha256:5311e7f182d02360a7194aa2995849bcdf04795c39a0ffdcf413eae625865970`  
		Last Modified: Sun, 07 Dec 2025 13:54:16 GMT  
		Size: 3.6 MB (3627056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af74a58a446b59e39793a690435f78e585a91ea73edb6406a99a3283db12a3a2`  
		Last Modified: Tue, 09 Dec 2025 23:02:45 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:053646d1ede74b4422e0751427c045b128d56b4d9c7521a34d9a3e2fd81f2fa6`  
		Last Modified: Tue, 09 Dec 2025 23:02:46 GMT  
		Size: 290.8 KB (290771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9fddb95d664d6dacdb2318596d88bdbacf9e5bde5abe2b7e4335d05288276ea`  
		Last Modified: Wed, 08 Oct 2025 23:01:01 GMT  
		Size: 19.6 MB (19556558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56f367635d83aeb5f5f554e62a06a02ad833c17339cf302d30013629399527c0`  
		Last Modified: Tue, 09 Dec 2025 23:02:45 GMT  
		Size: 12.2 KB (12235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b07f90ee1715c3ce00ef0c8e4958732cd35aeb06708db0a00e83afbe1f17da89`  
		Last Modified: Tue, 09 Dec 2025 23:02:46 GMT  
		Size: 11.9 KB (11891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9166e539db1f38a4aa1b578555a8c92c86979cbc08b8098fba9661f87ffe6167`  
		Last Modified: Tue, 09 Dec 2025 23:02:46 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:bcbb31392ab3215af685b41ca6842da95b2e263604620ad5d7a30c80609bc543
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.7 KB (188744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:862b2564bbbfa2013c4f206e9af5027911bf83448426df87b517b51fb5f596e0`

```dockerfile
```

-	Layers:
	-	`sha256:7d486241e7d5fad65401d86ed4cecac735dc744dd18c05a5530b79d0bc9ae6ac`  
		Last Modified: Thu, 25 Dec 2025 14:19:24 GMT  
		Size: 171.8 KB (171832 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87486fae9bd6ba27ac7806fc6b1c5c571f4d3de5fc46fd1b292df95f203bc24e`  
		Last Modified: Wed, 08 Oct 2025 23:01:00 GMT  
		Size: 16.9 KB (16912 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.7.17`

```console
$ docker pull chronograf@sha256:7b84adbafd53e66ca11e93a5cc1c411b5c8f3169e5177a480869b2f3f0d691d7
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
$ docker pull chronograf@sha256:c697a1eb4df17ee93f762eee018d2ff00ee4ab0f6be961bd6fc13db3380cd51d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.2 MB (69230633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8856cb0a97df83fd642c279a766d0b7af370d3b551ebb5bfe8145acd7d9cb77b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1768176000'
# Tue, 13 Jan 2026 02:12:12 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 13 Jan 2026 02:12:18 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 13 Jan 2026 02:12:18 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 13 Jan 2026 02:12:18 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 13 Jan 2026 02:12:18 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 13 Jan 2026 02:12:18 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 13 Jan 2026 02:12:18 GMT
VOLUME [/var/lib/chronograf]
# Tue, 13 Jan 2026 02:12:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 13 Jan 2026 02:12:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Jan 2026 02:12:18 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:bd1b97a95a10ded4767bfcdbb3d042b961d107d141121fdbb255239f0ca115f4`  
		Last Modified: Tue, 13 Jan 2026 00:42:23 GMT  
		Size: 30.3 MB (30258497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb6b0e2cd7abe524ab0af4a07f8f893bde79644ca44f970a929e11ed73cbf6af`  
		Last Modified: Tue, 13 Jan 2026 02:12:36 GMT  
		Size: 4.2 MB (4209325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d365326643172de5088f73fa37865f20ab65370b3dbdc024bd1e2f4d7bc13254`  
		Last Modified: Tue, 13 Jan 2026 02:12:30 GMT  
		Size: 34.7 MB (34738426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fda7ad3a0566d72b74d48200a97f531482364b5defeb249d4d17ed8b5222ee7`  
		Last Modified: Tue, 13 Jan 2026 02:12:29 GMT  
		Size: 12.2 KB (12244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a62b23f760546f6a2724ad171d851e47d389eb5fd56c71eac6e45471e9703c8`  
		Last Modified: Tue, 13 Jan 2026 02:12:36 GMT  
		Size: 11.9 KB (11902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:761820abfe35a527b101046674ae9c6dde68bc6486afdfc58ac568caaaeae64e`  
		Last Modified: Tue, 13 Jan 2026 02:12:30 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7.17` - unknown; unknown

```console
$ docker pull chronograf@sha256:2593cd6b1e6f6708a55799333e20d20d88e288acd06aa55ea0102c8e530de84c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3064607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1692b1f9d2b287c95792bb8f36e2a422efb85708dbef1840c0cf87478786484c`

```dockerfile
```

-	Layers:
	-	`sha256:6360525c0f28af986c566ad83830611dcaea13dea89fa3fc11d2b7be39f937e1`  
		Last Modified: Tue, 13 Jan 2026 04:39:41 GMT  
		Size: 3.0 MB (3048873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93955f9eb57046d2f290db14525a369a94a974e13eebf59c04f6a1b0bb76e156`  
		Last Modified: Tue, 13 Jan 2026 02:12:29 GMT  
		Size: 15.7 KB (15734 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.7.17` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:f897d44a405c9e7421f6eccb8637fff14e24c08ada07f58248cbb9faa4e3ab18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62179885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee05d2950d2c1c05d7a9c35e48cb9256b0cdb7056031282e9d11598f1c5d34ba`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1768176000'
# Tue, 13 Jan 2026 02:59:11 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 13 Jan 2026 02:59:19 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 13 Jan 2026 02:59:19 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 13 Jan 2026 02:59:19 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 13 Jan 2026 02:59:19 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 13 Jan 2026 02:59:19 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 13 Jan 2026 02:59:19 GMT
VOLUME [/var/lib/chronograf]
# Tue, 13 Jan 2026 02:59:19 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 13 Jan 2026 02:59:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Jan 2026 02:59:19 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:ddab8730b1df461111046cd88b7848f70955e854e29bbbfa3ae304f7ec801442`  
		Last Modified: Tue, 13 Jan 2026 00:42:31 GMT  
		Size: 25.5 MB (25546235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9251a13741298223fdfdc9be78334db81ff4f549edd0727a380f393b38821619`  
		Last Modified: Tue, 13 Jan 2026 02:59:36 GMT  
		Size: 3.5 MB (3511688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48701c41355a33b1cd2868933c2ed76cae2545cd6346942d912cf37ea72e476f`  
		Last Modified: Tue, 13 Jan 2026 02:59:30 GMT  
		Size: 33.1 MB (33097569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01af9d592d73eeef1d21a754c55f04464d6f50e5e310f9586072f3a741a5e0b8`  
		Last Modified: Tue, 13 Jan 2026 02:59:36 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41da3607200b9f79dfe6a0ddef1c9f298344dcb19a4f76189bf02e189becf75f`  
		Last Modified: Tue, 13 Jan 2026 02:59:36 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d21d2b0645d2ccc2bb0c832c5a8c992c01280f7558be590020cd6730f58aa85e`  
		Last Modified: Tue, 13 Jan 2026 02:59:30 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7.17` - unknown; unknown

```console
$ docker pull chronograf@sha256:bf4cf2341687afe9a445c1c1373316ed806e96f42449c1cb1315a3cac2eff827
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3066955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14f9b9c41a1375390f72f6a4b1f8c4199ec8ce5decac87f6a649ce9653c7c558`

```dockerfile
```

-	Layers:
	-	`sha256:b60089c4693066549ee8939dadefac4e1711458169d15d564dcd21d80a744a42`  
		Last Modified: Tue, 13 Jan 2026 02:59:29 GMT  
		Size: 3.1 MB (3051144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a8ca59e33c7bc7b0b8a83268aeb6d250c70a58b50fcf59c7b84eaed599e6974`  
		Last Modified: Tue, 13 Jan 2026 02:59:29 GMT  
		Size: 15.8 KB (15811 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.7.17` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:14d3f754c77264c27a6a84f79a5fd9d7aa7953e92ddfd74bbce2f56bc474eb1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66221678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d5786af0d6d216599b81a54b31142fac727f9cd420377d3d53ba0649a4801ab`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1768176000'
# Tue, 13 Jan 2026 02:16:16 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 13 Jan 2026 02:16:22 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 13 Jan 2026 02:16:22 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 13 Jan 2026 02:16:22 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 13 Jan 2026 02:16:22 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 13 Jan 2026 02:16:22 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 13 Jan 2026 02:16:22 GMT
VOLUME [/var/lib/chronograf]
# Tue, 13 Jan 2026 02:16:22 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 13 Jan 2026 02:16:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Jan 2026 02:16:22 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:7781088accb552d6473ed64f4649a64684d928b7cfad973d13e5c50942bf7a5b`  
		Last Modified: Tue, 13 Jan 2026 00:41:59 GMT  
		Size: 28.7 MB (28748518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33ab95430f23401ffe30c5b7d6aeff523932df0d14da602f2e0aa5f04c8778a0`  
		Last Modified: Tue, 13 Jan 2026 02:16:37 GMT  
		Size: 4.2 MB (4210612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02f55cd2a4f1c21030ff008f48d4d8b081ba2c0785c293cff39d918b865882cb`  
		Last Modified: Tue, 13 Jan 2026 02:16:40 GMT  
		Size: 33.2 MB (33238151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25378f999a0dd8ef23b56d4d771571d8112385054b577da39a46571b760947c8`  
		Last Modified: Tue, 13 Jan 2026 02:16:37 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d635ef5c076321b1cffcb4b7f02e38a1ee40c27ef9d9a2de87e79574abb52ad1`  
		Last Modified: Tue, 13 Jan 2026 02:16:51 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2daa28d65d5299f4239441883ccd2249f615b383b4b4381a3b85caba2a9ff784`  
		Last Modified: Tue, 13 Jan 2026 02:16:33 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7.17` - unknown; unknown

```console
$ docker pull chronograf@sha256:f91e5a4570d4cf7a6e7313352af25b57e7094096d32df05952be224449240591
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3064951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dfb4510cbc9d704fde2afb68e14092f92045eb2ab01c943a7017b55c247860a`

```dockerfile
```

-	Layers:
	-	`sha256:d6fb92f3a3ad8c7d311c0279eb81d2c0a1477b29731aab3e898bfe9c0ccebc3b`  
		Last Modified: Tue, 13 Jan 2026 04:40:01 GMT  
		Size: 3.0 MB (3049122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4123bf76b137451bf5f9f0ab59ca134e2ed2e0258631dddaf852414cd58a931d`  
		Last Modified: Tue, 13 Jan 2026 02:16:31 GMT  
		Size: 15.8 KB (15829 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.7.17-alpine`

```console
$ docker pull chronograf@sha256:f9bf8a3a9499f5324ca9b5f428e7ecbf8a4714d366e8a7920a8d06292f7d0511
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.7.17-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:0e68a8f6a33cec3ad19c936e80df9706efc6f4a6651f78b3373920f503a90deb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.5 MB (23499028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5704e6698a8163ec6cf9a9f4d2fc39455f7394b4b089fd3fe4fbbfcd3c84f5fc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 15 Aug 2025 14:37:23 GMT
ADD alpine-minirootfs-3.20.8-x86_64.tar.gz / # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["/bin/sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Fri, 15 Aug 2025 14:37:23 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
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
	-	`sha256:5311e7f182d02360a7194aa2995849bcdf04795c39a0ffdcf413eae625865970`  
		Last Modified: Sun, 07 Dec 2025 13:54:16 GMT  
		Size: 3.6 MB (3627056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af74a58a446b59e39793a690435f78e585a91ea73edb6406a99a3283db12a3a2`  
		Last Modified: Tue, 09 Dec 2025 23:02:45 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:053646d1ede74b4422e0751427c045b128d56b4d9c7521a34d9a3e2fd81f2fa6`  
		Last Modified: Tue, 09 Dec 2025 23:02:46 GMT  
		Size: 290.8 KB (290771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9fddb95d664d6dacdb2318596d88bdbacf9e5bde5abe2b7e4335d05288276ea`  
		Last Modified: Wed, 08 Oct 2025 23:01:01 GMT  
		Size: 19.6 MB (19556558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56f367635d83aeb5f5f554e62a06a02ad833c17339cf302d30013629399527c0`  
		Last Modified: Tue, 09 Dec 2025 23:02:45 GMT  
		Size: 12.2 KB (12235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b07f90ee1715c3ce00ef0c8e4958732cd35aeb06708db0a00e83afbe1f17da89`  
		Last Modified: Tue, 09 Dec 2025 23:02:46 GMT  
		Size: 11.9 KB (11891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9166e539db1f38a4aa1b578555a8c92c86979cbc08b8098fba9661f87ffe6167`  
		Last Modified: Tue, 09 Dec 2025 23:02:46 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7.17-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:bcbb31392ab3215af685b41ca6842da95b2e263604620ad5d7a30c80609bc543
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.7 KB (188744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:862b2564bbbfa2013c4f206e9af5027911bf83448426df87b517b51fb5f596e0`

```dockerfile
```

-	Layers:
	-	`sha256:7d486241e7d5fad65401d86ed4cecac735dc744dd18c05a5530b79d0bc9ae6ac`  
		Last Modified: Thu, 25 Dec 2025 14:19:24 GMT  
		Size: 171.8 KB (171832 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87486fae9bd6ba27ac7806fc6b1c5c571f4d3de5fc46fd1b292df95f203bc24e`  
		Last Modified: Wed, 08 Oct 2025 23:01:00 GMT  
		Size: 16.9 KB (16912 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.8`

```console
$ docker pull chronograf@sha256:f510254de416ffc865aeb1e96e082e41a5c1f4c4bceba22d603b306e82527826
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
$ docker pull chronograf@sha256:b7711799e0b84d20f7382a57c971fa816e5f54e9d7ef3b2a1fb72c2989655b3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69871424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90024744a0b1c922eb77ba6060eae65fb4463ce17810df27f5e0b5750ab7f73f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1768176000'
# Tue, 13 Jan 2026 02:12:34 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 13 Jan 2026 02:12:37 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Tue, 13 Jan 2026 02:12:37 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 13 Jan 2026 02:12:37 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 13 Jan 2026 02:12:38 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 13 Jan 2026 02:12:38 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 13 Jan 2026 02:12:38 GMT
VOLUME [/var/lib/chronograf]
# Tue, 13 Jan 2026 02:12:38 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 13 Jan 2026 02:12:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Jan 2026 02:12:38 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:bd1b97a95a10ded4767bfcdbb3d042b961d107d141121fdbb255239f0ca115f4`  
		Last Modified: Tue, 13 Jan 2026 00:42:23 GMT  
		Size: 30.3 MB (30258497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf36f6ac7ca11bde95de95d57bba0050be140adfcc2dcdafab04a086d36201cd`  
		Last Modified: Tue, 13 Jan 2026 02:12:48 GMT  
		Size: 5.2 MB (5224276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7b3c737aad41b7f1ab47251c8cc5049e4969d6fab2e019994d680dca85770e5`  
		Last Modified: Tue, 13 Jan 2026 02:12:57 GMT  
		Size: 34.4 MB (34364278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d95e9936b4c407a3e0fed8d5400c10fb28014dfbc1251f6986b715fcdefd3d5`  
		Last Modified: Tue, 13 Jan 2026 02:12:48 GMT  
		Size: 12.2 KB (12236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5af5c6a0a3e259fbad14f0c548b9d35fcfa7f1575479946f0306eb82f13ab051`  
		Last Modified: Tue, 13 Jan 2026 02:12:55 GMT  
		Size: 11.9 KB (11900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7978b18d311e29ac310b86711a338c692ab22a78c200b07e8e8414ce8a5a77fc`  
		Last Modified: Tue, 13 Jan 2026 02:12:55 GMT  
		Size: 237.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8` - unknown; unknown

```console
$ docker pull chronograf@sha256:bbe2d650554f4694ca211baa665673520683771730e8be890720d4d10beac286
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3120284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33356e4796260f33488c507841f66c376c043e56c92b0f6041b97f539d52e475`

```dockerfile
```

-	Layers:
	-	`sha256:a2fa41a1ad40644da4112729eef31db04831298a5791d48006b20cffbf1987e1`  
		Last Modified: Tue, 13 Jan 2026 04:39:56 GMT  
		Size: 3.1 MB (3104511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebfe8fa1da248b0574ab5c0402890ae5beaad1fcf85793e35f93d16e75e11cd4`  
		Last Modified: Tue, 13 Jan 2026 02:12:48 GMT  
		Size: 15.8 KB (15773 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.8` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:fd0355beb08aa7d9d316bf0d449e5d6fd9aad4ff4e475c2e689f0e9dc0f04d2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.6 MB (62595800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21157d6ec242a5b1b4f147f896c66bfc90b3d44edd9a6f483e9907f699436f3e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1768176000'
# Tue, 13 Jan 2026 03:00:27 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 13 Jan 2026 03:00:34 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Tue, 13 Jan 2026 03:00:34 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 13 Jan 2026 03:00:34 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 13 Jan 2026 03:00:34 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 13 Jan 2026 03:00:34 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 13 Jan 2026 03:00:34 GMT
VOLUME [/var/lib/chronograf]
# Tue, 13 Jan 2026 03:00:34 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 13 Jan 2026 03:00:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Jan 2026 03:00:34 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:ddab8730b1df461111046cd88b7848f70955e854e29bbbfa3ae304f7ec801442`  
		Last Modified: Tue, 13 Jan 2026 00:42:31 GMT  
		Size: 25.5 MB (25546235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c3af1e938f362bb930435d10f56ec4ea6859d1431b0a896e6f54fba60c213fe`  
		Last Modified: Tue, 13 Jan 2026 03:00:50 GMT  
		Size: 4.5 MB (4490228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c8cdcb16fd65b5bab0f1b3627c66548e6149bbcad555031dd923e645c219fc8`  
		Last Modified: Tue, 13 Jan 2026 03:00:44 GMT  
		Size: 32.5 MB (32534940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5d845e4a8eb207c4949b36fac025b7ecb65113c07f5403a5df55c9e68ad6a0e`  
		Last Modified: Tue, 13 Jan 2026 03:00:43 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfc5fd20b2a7253706a72203e218fbf52dc2e3ef2f390280909b6fbcf2db8f53`  
		Last Modified: Tue, 13 Jan 2026 03:00:50 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dce7cc96b77be2ab25d296920a968873e54161214cbe882de54996928489c79`  
		Last Modified: Tue, 13 Jan 2026 03:00:45 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8` - unknown; unknown

```console
$ docker pull chronograf@sha256:dd1e532fcaca7b37fa12359bfe0c0ada14086e1fccd584bee1d84817c4cc9a8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3122633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9576f9920f59723cde7cdfe44fa882969d99421d2acfcd14e9227826708ebf6`

```dockerfile
```

-	Layers:
	-	`sha256:e89fa6bb4dcd3f4e13a4eb7e73001de2b87a6c6620bddc44a9d7d8cbf4dd512f`  
		Last Modified: Tue, 13 Jan 2026 04:40:01 GMT  
		Size: 3.1 MB (3106782 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12e270ff58d0ff8bc04a4b852b1b274de7f7d41b67cbba56d7c79b178635c2b7`  
		Last Modified: Tue, 13 Jan 2026 04:40:02 GMT  
		Size: 15.9 KB (15851 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.8` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:9564b69dfffb9a1e5a4e5d9db98003d41a4857d660c7321f5b00bfde7dc363f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.4 MB (66410521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2653fe95232b0c1bcafbff31f8fc73a6bfd444b10c8f8925c68508f833dca2f7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1768176000'
# Tue, 13 Jan 2026 02:17:20 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 13 Jan 2026 02:17:24 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Tue, 13 Jan 2026 02:17:24 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 13 Jan 2026 02:17:24 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 13 Jan 2026 02:17:24 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 13 Jan 2026 02:17:24 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 13 Jan 2026 02:17:24 GMT
VOLUME [/var/lib/chronograf]
# Tue, 13 Jan 2026 02:17:24 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 13 Jan 2026 02:17:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Jan 2026 02:17:24 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:7781088accb552d6473ed64f4649a64684d928b7cfad973d13e5c50942bf7a5b`  
		Last Modified: Tue, 13 Jan 2026 00:41:59 GMT  
		Size: 28.7 MB (28748518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:587d10d83b3e1b87161492140b9ab56e0604d050f1b45f8e23cda854e1789778`  
		Last Modified: Tue, 13 Jan 2026 02:17:34 GMT  
		Size: 5.2 MB (5208128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81ef6ca9328c3547d443598e197dc110c3452aeae47a45aa9f8644c527fff6e3`  
		Last Modified: Tue, 13 Jan 2026 02:17:48 GMT  
		Size: 32.4 MB (32429482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d75295f1c5f2df3e88b0a878a9198ad08e2bb0d3ca25c43a385cdb9a7ad1541b`  
		Last Modified: Tue, 13 Jan 2026 02:17:41 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37557cabd37c79d8c8e48bf9da8c60bca3a4e8d7743ca24a1f8dcfed494d2ef4`  
		Last Modified: Tue, 13 Jan 2026 02:17:34 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:348eace459d99be8e14a85552cf6c71abdd86e064bcdf18b37573f647fede08a`  
		Last Modified: Tue, 13 Jan 2026 02:17:42 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8` - unknown; unknown

```console
$ docker pull chronograf@sha256:77532df540c8b840c002b83897a0de3413acfe714fd77e6776bbc99ea357be48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3120629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0a6d38e1a2e5d2897d312806cd214ff9230d8a3c03cf763887a31f698bd762c`

```dockerfile
```

-	Layers:
	-	`sha256:7cd23bd9a0d9e5e726776e288e5b0fe2b2804f54ca828f9800ee4e6ce88c6c7a`  
		Last Modified: Tue, 13 Jan 2026 04:40:06 GMT  
		Size: 3.1 MB (3104760 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac683dd20943c6afd7861e1f08a6f85e77936b5b7fdc8759f088e11ace292a41`  
		Last Modified: Tue, 13 Jan 2026 02:17:33 GMT  
		Size: 15.9 KB (15869 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.8-alpine`

```console
$ docker pull chronograf@sha256:8f246b11bed20824de500e732e0e0c1a9df2e2adcf60340444da2c4d2e7d83bc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.8-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:4fae84330ab9094200744d44140ff3695efc2a2085251cd4066103541bffbe5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23146498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6035189b6fd6fc001306a038b9c5678123af0b1f907f2a31efe3e96b3b689b22`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 15 Aug 2025 14:37:23 GMT
ADD alpine-minirootfs-3.20.8-x86_64.tar.gz / # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["/bin/sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Fri, 15 Aug 2025 14:37:23 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
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
	-	`sha256:5311e7f182d02360a7194aa2995849bcdf04795c39a0ffdcf413eae625865970`  
		Last Modified: Sun, 07 Dec 2025 13:54:16 GMT  
		Size: 3.6 MB (3627056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdaabc96984af774b48937345c7cc275e3315d3a9a42aeb994f6946de24556be`  
		Last Modified: Wed, 08 Oct 2025 23:01:01 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff81f10ae11b38f809feee3b7a44d508880916016658ca83647ff9d1c294aba`  
		Last Modified: Mon, 08 Dec 2025 07:57:14 GMT  
		Size: 290.8 KB (290774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa8cf4bd3a04c4941275f4aa1db1887c01bcdadeb973d9c95d34bc905b974dce`  
		Last Modified: Mon, 08 Dec 2025 07:57:15 GMT  
		Size: 19.2 MB (19204014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4732a865d574eb12cd7075d139d6bbd7d47fea3c367baf1a1f56ff51506906fb`  
		Last Modified: Mon, 08 Dec 2025 07:57:22 GMT  
		Size: 12.2 KB (12240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0733dea6fe6d3cf04ef8c52dec6540501fbf0e79664e84fd00853fab32410e15`  
		Last Modified: Wed, 08 Oct 2025 23:01:03 GMT  
		Size: 11.9 KB (11896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe58005a9627e476ca3528af5a14e30f0d4549afa8e314dcde58ee7ec5fd6671`  
		Last Modified: Mon, 08 Dec 2025 07:57:47 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:07f09e7f03af9efcf88f89d7ad0f207d0e5ab57b9423663591e3c7aa0b3bc6a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.3 KB (245253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2779ee449137493a2aca535f4363cae748d5a6c40f2c306362a97daf2d51bf6b`

```dockerfile
```

-	Layers:
	-	`sha256:4376140096bd52be7b1473ee7e7d625fff88ab2e731a2d509ed5b7861eab79fe`  
		Last Modified: Tue, 09 Dec 2025 03:48:01 GMT  
		Size: 228.3 KB (228341 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61687d781240db246500ccffe6dc5608d9be7a5e7c809173a2694ffec485f7c3`  
		Last Modified: Tue, 09 Dec 2025 03:48:01 GMT  
		Size: 16.9 KB (16912 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.8.10`

```console
$ docker pull chronograf@sha256:f510254de416ffc865aeb1e96e082e41a5c1f4c4bceba22d603b306e82527826
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
$ docker pull chronograf@sha256:b7711799e0b84d20f7382a57c971fa816e5f54e9d7ef3b2a1fb72c2989655b3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69871424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90024744a0b1c922eb77ba6060eae65fb4463ce17810df27f5e0b5750ab7f73f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1768176000'
# Tue, 13 Jan 2026 02:12:34 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 13 Jan 2026 02:12:37 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Tue, 13 Jan 2026 02:12:37 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 13 Jan 2026 02:12:37 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 13 Jan 2026 02:12:38 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 13 Jan 2026 02:12:38 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 13 Jan 2026 02:12:38 GMT
VOLUME [/var/lib/chronograf]
# Tue, 13 Jan 2026 02:12:38 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 13 Jan 2026 02:12:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Jan 2026 02:12:38 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:bd1b97a95a10ded4767bfcdbb3d042b961d107d141121fdbb255239f0ca115f4`  
		Last Modified: Tue, 13 Jan 2026 00:42:23 GMT  
		Size: 30.3 MB (30258497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf36f6ac7ca11bde95de95d57bba0050be140adfcc2dcdafab04a086d36201cd`  
		Last Modified: Tue, 13 Jan 2026 02:12:48 GMT  
		Size: 5.2 MB (5224276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7b3c737aad41b7f1ab47251c8cc5049e4969d6fab2e019994d680dca85770e5`  
		Last Modified: Tue, 13 Jan 2026 02:12:57 GMT  
		Size: 34.4 MB (34364278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d95e9936b4c407a3e0fed8d5400c10fb28014dfbc1251f6986b715fcdefd3d5`  
		Last Modified: Tue, 13 Jan 2026 02:12:48 GMT  
		Size: 12.2 KB (12236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5af5c6a0a3e259fbad14f0c548b9d35fcfa7f1575479946f0306eb82f13ab051`  
		Last Modified: Tue, 13 Jan 2026 02:12:55 GMT  
		Size: 11.9 KB (11900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7978b18d311e29ac310b86711a338c692ab22a78c200b07e8e8414ce8a5a77fc`  
		Last Modified: Tue, 13 Jan 2026 02:12:55 GMT  
		Size: 237.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:bbe2d650554f4694ca211baa665673520683771730e8be890720d4d10beac286
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3120284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33356e4796260f33488c507841f66c376c043e56c92b0f6041b97f539d52e475`

```dockerfile
```

-	Layers:
	-	`sha256:a2fa41a1ad40644da4112729eef31db04831298a5791d48006b20cffbf1987e1`  
		Last Modified: Tue, 13 Jan 2026 04:39:56 GMT  
		Size: 3.1 MB (3104511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebfe8fa1da248b0574ab5c0402890ae5beaad1fcf85793e35f93d16e75e11cd4`  
		Last Modified: Tue, 13 Jan 2026 02:12:48 GMT  
		Size: 15.8 KB (15773 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.8.10` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:fd0355beb08aa7d9d316bf0d449e5d6fd9aad4ff4e475c2e689f0e9dc0f04d2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.6 MB (62595800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21157d6ec242a5b1b4f147f896c66bfc90b3d44edd9a6f483e9907f699436f3e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1768176000'
# Tue, 13 Jan 2026 03:00:27 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 13 Jan 2026 03:00:34 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Tue, 13 Jan 2026 03:00:34 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 13 Jan 2026 03:00:34 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 13 Jan 2026 03:00:34 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 13 Jan 2026 03:00:34 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 13 Jan 2026 03:00:34 GMT
VOLUME [/var/lib/chronograf]
# Tue, 13 Jan 2026 03:00:34 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 13 Jan 2026 03:00:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Jan 2026 03:00:34 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:ddab8730b1df461111046cd88b7848f70955e854e29bbbfa3ae304f7ec801442`  
		Last Modified: Tue, 13 Jan 2026 00:42:31 GMT  
		Size: 25.5 MB (25546235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c3af1e938f362bb930435d10f56ec4ea6859d1431b0a896e6f54fba60c213fe`  
		Last Modified: Tue, 13 Jan 2026 03:00:50 GMT  
		Size: 4.5 MB (4490228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c8cdcb16fd65b5bab0f1b3627c66548e6149bbcad555031dd923e645c219fc8`  
		Last Modified: Tue, 13 Jan 2026 03:00:44 GMT  
		Size: 32.5 MB (32534940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5d845e4a8eb207c4949b36fac025b7ecb65113c07f5403a5df55c9e68ad6a0e`  
		Last Modified: Tue, 13 Jan 2026 03:00:43 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfc5fd20b2a7253706a72203e218fbf52dc2e3ef2f390280909b6fbcf2db8f53`  
		Last Modified: Tue, 13 Jan 2026 03:00:50 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dce7cc96b77be2ab25d296920a968873e54161214cbe882de54996928489c79`  
		Last Modified: Tue, 13 Jan 2026 03:00:45 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:dd1e532fcaca7b37fa12359bfe0c0ada14086e1fccd584bee1d84817c4cc9a8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3122633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9576f9920f59723cde7cdfe44fa882969d99421d2acfcd14e9227826708ebf6`

```dockerfile
```

-	Layers:
	-	`sha256:e89fa6bb4dcd3f4e13a4eb7e73001de2b87a6c6620bddc44a9d7d8cbf4dd512f`  
		Last Modified: Tue, 13 Jan 2026 04:40:01 GMT  
		Size: 3.1 MB (3106782 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12e270ff58d0ff8bc04a4b852b1b274de7f7d41b67cbba56d7c79b178635c2b7`  
		Last Modified: Tue, 13 Jan 2026 04:40:02 GMT  
		Size: 15.9 KB (15851 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.8.10` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:9564b69dfffb9a1e5a4e5d9db98003d41a4857d660c7321f5b00bfde7dc363f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.4 MB (66410521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2653fe95232b0c1bcafbff31f8fc73a6bfd444b10c8f8925c68508f833dca2f7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1768176000'
# Tue, 13 Jan 2026 02:17:20 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 13 Jan 2026 02:17:24 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Tue, 13 Jan 2026 02:17:24 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 13 Jan 2026 02:17:24 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 13 Jan 2026 02:17:24 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 13 Jan 2026 02:17:24 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 13 Jan 2026 02:17:24 GMT
VOLUME [/var/lib/chronograf]
# Tue, 13 Jan 2026 02:17:24 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 13 Jan 2026 02:17:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Jan 2026 02:17:24 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:7781088accb552d6473ed64f4649a64684d928b7cfad973d13e5c50942bf7a5b`  
		Last Modified: Tue, 13 Jan 2026 00:41:59 GMT  
		Size: 28.7 MB (28748518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:587d10d83b3e1b87161492140b9ab56e0604d050f1b45f8e23cda854e1789778`  
		Last Modified: Tue, 13 Jan 2026 02:17:34 GMT  
		Size: 5.2 MB (5208128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81ef6ca9328c3547d443598e197dc110c3452aeae47a45aa9f8644c527fff6e3`  
		Last Modified: Tue, 13 Jan 2026 02:17:48 GMT  
		Size: 32.4 MB (32429482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d75295f1c5f2df3e88b0a878a9198ad08e2bb0d3ca25c43a385cdb9a7ad1541b`  
		Last Modified: Tue, 13 Jan 2026 02:17:41 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37557cabd37c79d8c8e48bf9da8c60bca3a4e8d7743ca24a1f8dcfed494d2ef4`  
		Last Modified: Tue, 13 Jan 2026 02:17:34 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:348eace459d99be8e14a85552cf6c71abdd86e064bcdf18b37573f647fede08a`  
		Last Modified: Tue, 13 Jan 2026 02:17:42 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:77532df540c8b840c002b83897a0de3413acfe714fd77e6776bbc99ea357be48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3120629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0a6d38e1a2e5d2897d312806cd214ff9230d8a3c03cf763887a31f698bd762c`

```dockerfile
```

-	Layers:
	-	`sha256:7cd23bd9a0d9e5e726776e288e5b0fe2b2804f54ca828f9800ee4e6ce88c6c7a`  
		Last Modified: Tue, 13 Jan 2026 04:40:06 GMT  
		Size: 3.1 MB (3104760 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac683dd20943c6afd7861e1f08a6f85e77936b5b7fdc8759f088e11ace292a41`  
		Last Modified: Tue, 13 Jan 2026 02:17:33 GMT  
		Size: 15.9 KB (15869 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.8.10-alpine`

```console
$ docker pull chronograf@sha256:8f246b11bed20824de500e732e0e0c1a9df2e2adcf60340444da2c4d2e7d83bc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.8.10-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:4fae84330ab9094200744d44140ff3695efc2a2085251cd4066103541bffbe5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23146498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6035189b6fd6fc001306a038b9c5678123af0b1f907f2a31efe3e96b3b689b22`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 15 Aug 2025 14:37:23 GMT
ADD alpine-minirootfs-3.20.8-x86_64.tar.gz / # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["/bin/sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Fri, 15 Aug 2025 14:37:23 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
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
	-	`sha256:5311e7f182d02360a7194aa2995849bcdf04795c39a0ffdcf413eae625865970`  
		Last Modified: Sun, 07 Dec 2025 13:54:16 GMT  
		Size: 3.6 MB (3627056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdaabc96984af774b48937345c7cc275e3315d3a9a42aeb994f6946de24556be`  
		Last Modified: Wed, 08 Oct 2025 23:01:01 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff81f10ae11b38f809feee3b7a44d508880916016658ca83647ff9d1c294aba`  
		Last Modified: Mon, 08 Dec 2025 07:57:14 GMT  
		Size: 290.8 KB (290774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa8cf4bd3a04c4941275f4aa1db1887c01bcdadeb973d9c95d34bc905b974dce`  
		Last Modified: Mon, 08 Dec 2025 07:57:15 GMT  
		Size: 19.2 MB (19204014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4732a865d574eb12cd7075d139d6bbd7d47fea3c367baf1a1f56ff51506906fb`  
		Last Modified: Mon, 08 Dec 2025 07:57:22 GMT  
		Size: 12.2 KB (12240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0733dea6fe6d3cf04ef8c52dec6540501fbf0e79664e84fd00853fab32410e15`  
		Last Modified: Wed, 08 Oct 2025 23:01:03 GMT  
		Size: 11.9 KB (11896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe58005a9627e476ca3528af5a14e30f0d4549afa8e314dcde58ee7ec5fd6671`  
		Last Modified: Mon, 08 Dec 2025 07:57:47 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8.10-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:07f09e7f03af9efcf88f89d7ad0f207d0e5ab57b9423663591e3c7aa0b3bc6a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.3 KB (245253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2779ee449137493a2aca535f4363cae748d5a6c40f2c306362a97daf2d51bf6b`

```dockerfile
```

-	Layers:
	-	`sha256:4376140096bd52be7b1473ee7e7d625fff88ab2e731a2d509ed5b7861eab79fe`  
		Last Modified: Tue, 09 Dec 2025 03:48:01 GMT  
		Size: 228.3 KB (228341 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61687d781240db246500ccffe6dc5608d9be7a5e7c809173a2694ffec485f7c3`  
		Last Modified: Tue, 09 Dec 2025 03:48:01 GMT  
		Size: 16.9 KB (16912 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.9`

```console
$ docker pull chronograf@sha256:fa879b6f29ef23e5d688a8965913d86832b9bfaeeef4979296d6b5136340dcc4
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
$ docker pull chronograf@sha256:14b02ff4d5359c8648f7b372be4330485036a6497e1456116184bb279acadb48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.5 MB (70518865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b94e75689d215aa492803332ff1f83afd9bda894deec2e205875a5212e30c7bc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1768176000'
# Tue, 13 Jan 2026 02:12:54 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 13 Jan 2026 02:12:59 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Tue, 13 Jan 2026 02:12:59 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 13 Jan 2026 02:12:59 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 13 Jan 2026 02:12:59 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 13 Jan 2026 02:12:59 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 13 Jan 2026 02:12:59 GMT
VOLUME [/var/lib/chronograf]
# Tue, 13 Jan 2026 02:12:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 13 Jan 2026 02:12:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Jan 2026 02:12:59 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:bd1b97a95a10ded4767bfcdbb3d042b961d107d141121fdbb255239f0ca115f4`  
		Last Modified: Tue, 13 Jan 2026 00:42:23 GMT  
		Size: 30.3 MB (30258497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7440e58dcc12885622b60791924e0060cee768b5190f0e4fa6a485400100a272`  
		Last Modified: Tue, 13 Jan 2026 02:13:16 GMT  
		Size: 5.2 MB (5224202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db2dc7daa6ef0854d9aa4deea729ed3c4f7b73c04cc1cb3147babf83987392f7`  
		Last Modified: Tue, 13 Jan 2026 02:13:19 GMT  
		Size: 35.0 MB (35011770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:351026350fad409044bd27c901a01ae3828cc183cd7057623d3f8c1d7e244bf0`  
		Last Modified: Tue, 13 Jan 2026 02:13:09 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5291325ca68690537417452422d593849e0e817ff96aef8fffa60846510b55ba`  
		Last Modified: Tue, 13 Jan 2026 02:13:16 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd90282b3a044b8f4f993e2c85c85c2777fc5090be5f7289bd728c681a0f9697`  
		Last Modified: Tue, 13 Jan 2026 02:13:16 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9` - unknown; unknown

```console
$ docker pull chronograf@sha256:daadc5bf78a457f6d9cc9e649d6cb23632fdebed4f293068d522f29da277ef6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3125488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c66439087b5ccb55032bd5bbb12b98f107367ddd2b895b105aedea3c1d88a4b6`

```dockerfile
```

-	Layers:
	-	`sha256:0d14f0ac7c08e976d54efa395d62b269c270a71b535cb1983f21e8150c7ca692`  
		Last Modified: Tue, 13 Jan 2026 04:40:13 GMT  
		Size: 3.1 MB (3109721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58de8d1d25158950fff482547fc29eb1407e7f41668c761704c5c4b2b2ea37bc`  
		Last Modified: Tue, 13 Jan 2026 04:40:14 GMT  
		Size: 15.8 KB (15767 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.9` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:907612da8f6c21459f25afcff53b40ffab86c97cd3aa1eb453f4a95006d96b81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.4 MB (63372405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0862f039098f1fb0884133c40b3c6fded071198126ca38b234c722cfbca6fd32`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1768176000'
# Tue, 13 Jan 2026 03:00:27 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 13 Jan 2026 03:01:35 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Tue, 13 Jan 2026 03:01:35 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 13 Jan 2026 03:01:35 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 13 Jan 2026 03:01:35 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 13 Jan 2026 03:01:35 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 13 Jan 2026 03:01:35 GMT
VOLUME [/var/lib/chronograf]
# Tue, 13 Jan 2026 03:01:35 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 13 Jan 2026 03:01:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Jan 2026 03:01:35 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:ddab8730b1df461111046cd88b7848f70955e854e29bbbfa3ae304f7ec801442`  
		Last Modified: Tue, 13 Jan 2026 00:42:31 GMT  
		Size: 25.5 MB (25546235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c3af1e938f362bb930435d10f56ec4ea6859d1431b0a896e6f54fba60c213fe`  
		Last Modified: Tue, 13 Jan 2026 03:00:50 GMT  
		Size: 4.5 MB (4490228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d65ff983806778d6f47f247f83d427970f7309d4aea50813b9f2bbcd4a7aba8`  
		Last Modified: Tue, 13 Jan 2026 03:01:59 GMT  
		Size: 33.3 MB (33311562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1b5ab788b7dd89d3233c3635cf42da4c696f58e3ad32aa6c4797a2c068ee159`  
		Last Modified: Tue, 13 Jan 2026 03:01:50 GMT  
		Size: 12.2 KB (12242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d25578a3ad4ec0f727aea9f33ccbbc1dc731e6b5f6f78303e3876cf3053dc73e`  
		Last Modified: Tue, 13 Jan 2026 03:01:50 GMT  
		Size: 11.9 KB (11900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bbd02315a11cae5575a0278b7b4f41912103c7936d3a3d659f2a87cf2d9993e`  
		Last Modified: Tue, 13 Jan 2026 03:01:49 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9` - unknown; unknown

```console
$ docker pull chronograf@sha256:c91921eadf671c5f0de7ddcccb1c3aac501555c4c42189bbf1a1a8abc6c3b667
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3127836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fd0e3e0181f8d72f523ec5bd6b94fe00248f62b53bd74322c5d110d82471a1f`

```dockerfile
```

-	Layers:
	-	`sha256:131ec56fecc85f0dd1469f95ddeb5f981df88e2fc47576a5f8118015b2892142`  
		Last Modified: Tue, 13 Jan 2026 03:01:45 GMT  
		Size: 3.1 MB (3111992 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a84d14d70a69fb17981bf342acb1796ea888d23a2e91d7b285501612f9c814aa`  
		Last Modified: Tue, 13 Jan 2026 04:40:20 GMT  
		Size: 15.8 KB (15844 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.9` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:8ddd1d889c8584463b5530080d96cfc136afe7eb0b570642f3fc533c536ae69d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.2 MB (67163386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e05e6c71c6c3da8012fd19478dcb8931588badc54e18cf249db772ef520358ff`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1768176000'
# Tue, 13 Jan 2026 02:18:49 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 13 Jan 2026 02:18:54 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Tue, 13 Jan 2026 02:18:54 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 13 Jan 2026 02:18:54 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 13 Jan 2026 02:18:54 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 13 Jan 2026 02:18:54 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 13 Jan 2026 02:18:54 GMT
VOLUME [/var/lib/chronograf]
# Tue, 13 Jan 2026 02:18:54 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 13 Jan 2026 02:18:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Jan 2026 02:18:54 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:7781088accb552d6473ed64f4649a64684d928b7cfad973d13e5c50942bf7a5b`  
		Last Modified: Tue, 13 Jan 2026 00:41:59 GMT  
		Size: 28.7 MB (28748518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9675dbf3c11786b2e6b83e1ed02e53ebb77342287fd6825e2c892c5dc9c6002`  
		Last Modified: Tue, 13 Jan 2026 02:19:12 GMT  
		Size: 5.2 MB (5208172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36f3b66c8cafe4fbd166d9834903e13c26279e358d9739a73ac802ee2dc7e699`  
		Last Modified: Tue, 13 Jan 2026 02:19:14 GMT  
		Size: 33.2 MB (33182301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78e970438d49c8098fd527518cb476c47549a43d87d19fce3d4e41b5a4d5ee93`  
		Last Modified: Tue, 13 Jan 2026 02:19:11 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48b84714139ec00607a3895d5fa7f73a56da3c45c9b8669e4589752ddf09d6aa`  
		Last Modified: Tue, 13 Jan 2026 02:19:11 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7885b9908796aa4af090401044d65246add1a441e1e408dd6967e1ba441c99f2`  
		Last Modified: Tue, 13 Jan 2026 02:19:11 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9` - unknown; unknown

```console
$ docker pull chronograf@sha256:00c01934403ddd64c22cf2eeccbd6178318a23e8473683627313c76a717bd1df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3125832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2ed9faa7b6943cf0742e8d3fbe83c85f356b0f627f1c2011757fb94cf0cf2f7`

```dockerfile
```

-	Layers:
	-	`sha256:9228634435fdc78d0b1eb0986d18079ebab9d651b50c96d51f3b2fb0ada57f47`  
		Last Modified: Tue, 13 Jan 2026 02:19:05 GMT  
		Size: 3.1 MB (3109970 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0dd5efde850a093b8102f291231881eb8a84af6118598438017c6618b01b61f1`  
		Last Modified: Tue, 13 Jan 2026 04:40:25 GMT  
		Size: 15.9 KB (15862 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.9-alpine`

```console
$ docker pull chronograf@sha256:b3fee5aad5c22c71cb04bbd41eea4af839aeb7d359a82d9b4233795d4cee5130
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.9-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:2d4252cb73b369cd488e239afeef5f7a6b44a46a01cfe8ab7d068d6397d5311d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23614563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9964a18d639210346c0ff7c26e65b91960ad4afbf36654d3a88e1c03026a1437`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 15 Aug 2025 14:37:23 GMT
ADD alpine-minirootfs-3.20.8-x86_64.tar.gz / # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["/bin/sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Fri, 15 Aug 2025 14:37:23 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
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
	-	`sha256:5311e7f182d02360a7194aa2995849bcdf04795c39a0ffdcf413eae625865970`  
		Last Modified: Sun, 07 Dec 2025 13:54:16 GMT  
		Size: 3.6 MB (3627056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d70c842384492021fdcd617e3e57dbc08546ebeb0a55cf5f01aa575170280c6`  
		Last Modified: Mon, 08 Dec 2025 00:01:59 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e6c508c6ab14eb797ff6524630894eea223ff1b5a3f02be3595aff5713c5112`  
		Last Modified: Wed, 08 Oct 2025 23:01:18 GMT  
		Size: 290.8 KB (290774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43383a0cdbbe70773cd822a7089d90f254cc6923262bc86a209c0c182a190472`  
		Last Modified: Thu, 11 Dec 2025 06:17:57 GMT  
		Size: 19.7 MB (19672095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11524f4d626f224d1faadbb2537a398d423351e2a0d854a4a43b4692fab631c6`  
		Last Modified: Thu, 11 Dec 2025 06:17:54 GMT  
		Size: 12.2 KB (12232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:811766d26cc20ed9c9dee509c4ef17aa945fbbf00be418890deec226cbeae620`  
		Last Modified: Thu, 11 Dec 2025 13:23:54 GMT  
		Size: 11.9 KB (11888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90296708765453bd34d3b31917ee366ec4e86d0d341504ddd046c032d6f85842`  
		Last Modified: Thu, 11 Dec 2025 13:23:54 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:c5e372192d09b31155c48fb1472089780f956a2cdeba37b4eda3358869e38aec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.5 KB (250462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad16fab4bfdaa94339daa5b35ee736124878a90af7d436293dd5657f43ac1f79`

```dockerfile
```

-	Layers:
	-	`sha256:6ed1879bf7ef8eb915186029d90ae2f6c3d14aa17bd74c3708035ff07dfcc75e`  
		Last Modified: Thu, 25 Dec 2025 14:21:32 GMT  
		Size: 233.6 KB (233553 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5586220b931721e2b29f86f48af9fa3579d18c357b0351f043fc2e76a05ebc52`  
		Last Modified: Thu, 25 Dec 2025 14:21:32 GMT  
		Size: 16.9 KB (16909 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.9.4`

```console
$ docker pull chronograf@sha256:fa879b6f29ef23e5d688a8965913d86832b9bfaeeef4979296d6b5136340dcc4
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
$ docker pull chronograf@sha256:14b02ff4d5359c8648f7b372be4330485036a6497e1456116184bb279acadb48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.5 MB (70518865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b94e75689d215aa492803332ff1f83afd9bda894deec2e205875a5212e30c7bc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1768176000'
# Tue, 13 Jan 2026 02:12:54 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 13 Jan 2026 02:12:59 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Tue, 13 Jan 2026 02:12:59 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 13 Jan 2026 02:12:59 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 13 Jan 2026 02:12:59 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 13 Jan 2026 02:12:59 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 13 Jan 2026 02:12:59 GMT
VOLUME [/var/lib/chronograf]
# Tue, 13 Jan 2026 02:12:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 13 Jan 2026 02:12:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Jan 2026 02:12:59 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:bd1b97a95a10ded4767bfcdbb3d042b961d107d141121fdbb255239f0ca115f4`  
		Last Modified: Tue, 13 Jan 2026 00:42:23 GMT  
		Size: 30.3 MB (30258497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7440e58dcc12885622b60791924e0060cee768b5190f0e4fa6a485400100a272`  
		Last Modified: Tue, 13 Jan 2026 02:13:16 GMT  
		Size: 5.2 MB (5224202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db2dc7daa6ef0854d9aa4deea729ed3c4f7b73c04cc1cb3147babf83987392f7`  
		Last Modified: Tue, 13 Jan 2026 02:13:19 GMT  
		Size: 35.0 MB (35011770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:351026350fad409044bd27c901a01ae3828cc183cd7057623d3f8c1d7e244bf0`  
		Last Modified: Tue, 13 Jan 2026 02:13:09 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5291325ca68690537417452422d593849e0e817ff96aef8fffa60846510b55ba`  
		Last Modified: Tue, 13 Jan 2026 02:13:16 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd90282b3a044b8f4f993e2c85c85c2777fc5090be5f7289bd728c681a0f9697`  
		Last Modified: Tue, 13 Jan 2026 02:13:16 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9.4` - unknown; unknown

```console
$ docker pull chronograf@sha256:daadc5bf78a457f6d9cc9e649d6cb23632fdebed4f293068d522f29da277ef6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3125488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c66439087b5ccb55032bd5bbb12b98f107367ddd2b895b105aedea3c1d88a4b6`

```dockerfile
```

-	Layers:
	-	`sha256:0d14f0ac7c08e976d54efa395d62b269c270a71b535cb1983f21e8150c7ca692`  
		Last Modified: Tue, 13 Jan 2026 04:40:13 GMT  
		Size: 3.1 MB (3109721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58de8d1d25158950fff482547fc29eb1407e7f41668c761704c5c4b2b2ea37bc`  
		Last Modified: Tue, 13 Jan 2026 04:40:14 GMT  
		Size: 15.8 KB (15767 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.9.4` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:907612da8f6c21459f25afcff53b40ffab86c97cd3aa1eb453f4a95006d96b81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.4 MB (63372405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0862f039098f1fb0884133c40b3c6fded071198126ca38b234c722cfbca6fd32`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1768176000'
# Tue, 13 Jan 2026 03:00:27 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 13 Jan 2026 03:01:35 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Tue, 13 Jan 2026 03:01:35 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 13 Jan 2026 03:01:35 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 13 Jan 2026 03:01:35 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 13 Jan 2026 03:01:35 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 13 Jan 2026 03:01:35 GMT
VOLUME [/var/lib/chronograf]
# Tue, 13 Jan 2026 03:01:35 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 13 Jan 2026 03:01:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Jan 2026 03:01:35 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:ddab8730b1df461111046cd88b7848f70955e854e29bbbfa3ae304f7ec801442`  
		Last Modified: Tue, 13 Jan 2026 00:42:31 GMT  
		Size: 25.5 MB (25546235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c3af1e938f362bb930435d10f56ec4ea6859d1431b0a896e6f54fba60c213fe`  
		Last Modified: Tue, 13 Jan 2026 03:00:50 GMT  
		Size: 4.5 MB (4490228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d65ff983806778d6f47f247f83d427970f7309d4aea50813b9f2bbcd4a7aba8`  
		Last Modified: Tue, 13 Jan 2026 03:01:59 GMT  
		Size: 33.3 MB (33311562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1b5ab788b7dd89d3233c3635cf42da4c696f58e3ad32aa6c4797a2c068ee159`  
		Last Modified: Tue, 13 Jan 2026 03:01:50 GMT  
		Size: 12.2 KB (12242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d25578a3ad4ec0f727aea9f33ccbbc1dc731e6b5f6f78303e3876cf3053dc73e`  
		Last Modified: Tue, 13 Jan 2026 03:01:50 GMT  
		Size: 11.9 KB (11900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bbd02315a11cae5575a0278b7b4f41912103c7936d3a3d659f2a87cf2d9993e`  
		Last Modified: Tue, 13 Jan 2026 03:01:49 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9.4` - unknown; unknown

```console
$ docker pull chronograf@sha256:c91921eadf671c5f0de7ddcccb1c3aac501555c4c42189bbf1a1a8abc6c3b667
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3127836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fd0e3e0181f8d72f523ec5bd6b94fe00248f62b53bd74322c5d110d82471a1f`

```dockerfile
```

-	Layers:
	-	`sha256:131ec56fecc85f0dd1469f95ddeb5f981df88e2fc47576a5f8118015b2892142`  
		Last Modified: Tue, 13 Jan 2026 03:01:45 GMT  
		Size: 3.1 MB (3111992 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a84d14d70a69fb17981bf342acb1796ea888d23a2e91d7b285501612f9c814aa`  
		Last Modified: Tue, 13 Jan 2026 04:40:20 GMT  
		Size: 15.8 KB (15844 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.9.4` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:8ddd1d889c8584463b5530080d96cfc136afe7eb0b570642f3fc533c536ae69d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.2 MB (67163386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e05e6c71c6c3da8012fd19478dcb8931588badc54e18cf249db772ef520358ff`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1768176000'
# Tue, 13 Jan 2026 02:18:49 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 13 Jan 2026 02:18:54 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Tue, 13 Jan 2026 02:18:54 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 13 Jan 2026 02:18:54 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 13 Jan 2026 02:18:54 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 13 Jan 2026 02:18:54 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 13 Jan 2026 02:18:54 GMT
VOLUME [/var/lib/chronograf]
# Tue, 13 Jan 2026 02:18:54 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 13 Jan 2026 02:18:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Jan 2026 02:18:54 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:7781088accb552d6473ed64f4649a64684d928b7cfad973d13e5c50942bf7a5b`  
		Last Modified: Tue, 13 Jan 2026 00:41:59 GMT  
		Size: 28.7 MB (28748518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9675dbf3c11786b2e6b83e1ed02e53ebb77342287fd6825e2c892c5dc9c6002`  
		Last Modified: Tue, 13 Jan 2026 02:19:12 GMT  
		Size: 5.2 MB (5208172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36f3b66c8cafe4fbd166d9834903e13c26279e358d9739a73ac802ee2dc7e699`  
		Last Modified: Tue, 13 Jan 2026 02:19:14 GMT  
		Size: 33.2 MB (33182301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78e970438d49c8098fd527518cb476c47549a43d87d19fce3d4e41b5a4d5ee93`  
		Last Modified: Tue, 13 Jan 2026 02:19:11 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48b84714139ec00607a3895d5fa7f73a56da3c45c9b8669e4589752ddf09d6aa`  
		Last Modified: Tue, 13 Jan 2026 02:19:11 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7885b9908796aa4af090401044d65246add1a441e1e408dd6967e1ba441c99f2`  
		Last Modified: Tue, 13 Jan 2026 02:19:11 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9.4` - unknown; unknown

```console
$ docker pull chronograf@sha256:00c01934403ddd64c22cf2eeccbd6178318a23e8473683627313c76a717bd1df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3125832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2ed9faa7b6943cf0742e8d3fbe83c85f356b0f627f1c2011757fb94cf0cf2f7`

```dockerfile
```

-	Layers:
	-	`sha256:9228634435fdc78d0b1eb0986d18079ebab9d651b50c96d51f3b2fb0ada57f47`  
		Last Modified: Tue, 13 Jan 2026 02:19:05 GMT  
		Size: 3.1 MB (3109970 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0dd5efde850a093b8102f291231881eb8a84af6118598438017c6618b01b61f1`  
		Last Modified: Tue, 13 Jan 2026 04:40:25 GMT  
		Size: 15.9 KB (15862 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.9.4-alpine`

```console
$ docker pull chronograf@sha256:b3fee5aad5c22c71cb04bbd41eea4af839aeb7d359a82d9b4233795d4cee5130
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.9.4-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:2d4252cb73b369cd488e239afeef5f7a6b44a46a01cfe8ab7d068d6397d5311d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23614563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9964a18d639210346c0ff7c26e65b91960ad4afbf36654d3a88e1c03026a1437`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 15 Aug 2025 14:37:23 GMT
ADD alpine-minirootfs-3.20.8-x86_64.tar.gz / # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["/bin/sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Fri, 15 Aug 2025 14:37:23 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
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
	-	`sha256:5311e7f182d02360a7194aa2995849bcdf04795c39a0ffdcf413eae625865970`  
		Last Modified: Sun, 07 Dec 2025 13:54:16 GMT  
		Size: 3.6 MB (3627056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d70c842384492021fdcd617e3e57dbc08546ebeb0a55cf5f01aa575170280c6`  
		Last Modified: Mon, 08 Dec 2025 00:01:59 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e6c508c6ab14eb797ff6524630894eea223ff1b5a3f02be3595aff5713c5112`  
		Last Modified: Wed, 08 Oct 2025 23:01:18 GMT  
		Size: 290.8 KB (290774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43383a0cdbbe70773cd822a7089d90f254cc6923262bc86a209c0c182a190472`  
		Last Modified: Thu, 11 Dec 2025 06:17:57 GMT  
		Size: 19.7 MB (19672095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11524f4d626f224d1faadbb2537a398d423351e2a0d854a4a43b4692fab631c6`  
		Last Modified: Thu, 11 Dec 2025 06:17:54 GMT  
		Size: 12.2 KB (12232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:811766d26cc20ed9c9dee509c4ef17aa945fbbf00be418890deec226cbeae620`  
		Last Modified: Thu, 11 Dec 2025 13:23:54 GMT  
		Size: 11.9 KB (11888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90296708765453bd34d3b31917ee366ec4e86d0d341504ddd046c032d6f85842`  
		Last Modified: Thu, 11 Dec 2025 13:23:54 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9.4-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:c5e372192d09b31155c48fb1472089780f956a2cdeba37b4eda3358869e38aec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.5 KB (250462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad16fab4bfdaa94339daa5b35ee736124878a90af7d436293dd5657f43ac1f79`

```dockerfile
```

-	Layers:
	-	`sha256:6ed1879bf7ef8eb915186029d90ae2f6c3d14aa17bd74c3708035ff07dfcc75e`  
		Last Modified: Thu, 25 Dec 2025 14:21:32 GMT  
		Size: 233.6 KB (233553 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5586220b931721e2b29f86f48af9fa3579d18c357b0351f043fc2e76a05ebc52`  
		Last Modified: Thu, 25 Dec 2025 14:21:32 GMT  
		Size: 16.9 KB (16909 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:alpine`

```console
$ docker pull chronograf@sha256:3180124052084e1c0db5c3ba1bfa2f415c88fc7681ef14dfc189b324b9de03c6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:ee85eacf84a2662ece23a552d71cac84b11cbc3691d0f11533c47601629436a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33278682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd20a03649aab6179a8d0fbca439a20f70197cad1151f17c7db7f2bca99a7a41`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 07 Jan 2026 17:54:23 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 07 Jan 2026 17:54:24 GMT
RUN apk add --no-cache ca-certificates setpriv &&     update-ca-certificates # buildkit
# Wed, 07 Jan 2026 17:54:28 GMT
ENV CHRONOGRAF_VERSION=1.10.9
# Wed, 07 Jan 2026 17:54:28 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S chronograf &&     adduser -S chronograf -G chronograf &&     mkdir -m 0750 -p /var/lib/chronograf &&     chown chronograf:chronograf /var/lib/chronograf # buildkit
# Wed, 07 Jan 2026 17:54:28 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Wed, 07 Jan 2026 17:54:28 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Wed, 07 Jan 2026 17:54:28 GMT
EXPOSE map[8888/tcp:{}]
# Wed, 07 Jan 2026 17:54:28 GMT
VOLUME [/var/lib/chronograf]
# Wed, 07 Jan 2026 17:54:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 07 Jan 2026 17:54:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 07 Jan 2026 17:54:28 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:21 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bb809d47327d4436ed4d3ac5b0d2b676061f267bdacedb6a6a89d360a7dae09`  
		Last Modified: Wed, 07 Jan 2026 17:54:38 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb19a309f7b798855a902544be3186a07abbb407e814358b58cd1b89a39f5d3b`  
		Last Modified: Wed, 07 Jan 2026 17:54:37 GMT  
		Size: 314.7 KB (314652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1806ce0ba099140396732948f565b7509ae183daafc58c9c0232df4fa0e46272`  
		Last Modified: Wed, 07 Jan 2026 17:54:38 GMT  
		Size: 29.1 MB (29136854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76dad571ff7e915a85ce4aba703a3ebe307f73f0a42380e0eab5d5be6f6bc208`  
		Last Modified: Wed, 07 Jan 2026 17:54:44 GMT  
		Size: 12.2 KB (12236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd67712f58a31ea13eee2648165a6e2c172ef5cbff62d5d29689482836291302`  
		Last Modified: Wed, 07 Jan 2026 17:54:38 GMT  
		Size: 11.9 KB (11895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f130002e876e593ef18015df47078dcbf1e0f19cc533e5612a81b3e99b565166`  
		Last Modified: Wed, 07 Jan 2026 17:54:44 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:28567e0f67b9b9f0f79f9b8a40d1b45120c51e8222a75fbfeff2423cc7454275
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.8 KB (269841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0da3a04ba74c76ee4048ccb25b04a06ecc361c5298007bd4a37d0e9e8371a4b2`

```dockerfile
```

-	Layers:
	-	`sha256:4b9989c9337955baf604cfdcd89af7ca51dd00300557e0cb8354a7bddd10ebe2`  
		Last Modified: Wed, 07 Jan 2026 19:38:29 GMT  
		Size: 252.0 KB (252029 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd5523918f180b39378a1fc48e9db5f725a139f89fcd1a1b8eae374b7001d78a`  
		Last Modified: Wed, 07 Jan 2026 17:54:37 GMT  
		Size: 17.8 KB (17812 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:latest`

```console
$ docker pull chronograf@sha256:858f06c5e2ab525a8193a5f190a987b2a9b0f0dfb05f00e883a6d4215ab5a999
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
$ docker pull chronograf@sha256:0ca02df258be555db97f05cf143c919bde15c593557c0bdd247379fa01c63842
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.0 MB (85000209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:711a95539008f28a45eee16e13d093cded16283e271f0d487d78fce3279a71d2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:13:54 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 13 Jan 2026 02:13:59 GMT
ENV CHRONOGRAF_VERSION=1.10.9
# Tue, 13 Jan 2026 02:13:59 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 13 Jan 2026 02:13:59 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 13 Jan 2026 02:13:59 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 13 Jan 2026 02:13:59 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 13 Jan 2026 02:13:59 GMT
VOLUME [/var/lib/chronograf]
# Tue, 13 Jan 2026 02:13:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 13 Jan 2026 02:13:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Jan 2026 02:13:59 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:c02d17997ce3d2c82e082235ea0b5152d06ee659c4e2fabcf1e0079312f1bcde`  
		Last Modified: Tue, 13 Jan 2026 00:41:50 GMT  
		Size: 28.2 MB (28228572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f97a4c03663264daa07043a3f29f2d20b0f8166009a68253c911509bc54d620`  
		Last Modified: Tue, 13 Jan 2026 02:14:19 GMT  
		Size: 7.9 MB (7879303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1de3fdab9946b7fe91f7f64835d147fd55a0c2dd876ff89abcb4932975b563c`  
		Last Modified: Tue, 13 Jan 2026 02:14:27 GMT  
		Size: 48.9 MB (48867877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b98f709a51e0b7ad076ff093e6fbc62937fc424c617b44afb09050e162934c2`  
		Last Modified: Tue, 13 Jan 2026 02:14:11 GMT  
		Size: 12.2 KB (12240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d2105baf2c6f199637a6f8da17dd041da224c83e726af6c49c8490825887745`  
		Last Modified: Tue, 13 Jan 2026 02:14:19 GMT  
		Size: 11.9 KB (11903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc1a26f63feaf4dd4395b0829102a09d484d4da534de28a323abf3b4a7bee141`  
		Last Modified: Tue, 13 Jan 2026 02:14:19 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:d18723ded2d8ae5789aa7c7109d5a2728eb08a049cf9931fe5e85b64e0ca4c73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2871815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:859a2ca904a49afc214c3812aa4311aa8a9c03803927cf254d97df1a2e83312a`

```dockerfile
```

-	Layers:
	-	`sha256:26bf29e8df90ec3896704fc9859e3fee325b42d6795b179d2127f488258d08c5`  
		Last Modified: Tue, 13 Jan 2026 02:14:11 GMT  
		Size: 2.9 MB (2855730 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac887deeede4277c4720d5beede9b3f511ddda0275a34a8c86c9acffd9d8901f`  
		Last Modified: Tue, 13 Jan 2026 04:39:26 GMT  
		Size: 16.1 KB (16085 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:latest` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:118d4a298e4756953ee1acc65f510e9b7772e025751c4451027be26d6283c73f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76790409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd0b7dd595a1be3b19803d456a8d8cdba8f542788c31f5d26747a1853d141b2c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 03:02:49 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 13 Jan 2026 03:02:57 GMT
ENV CHRONOGRAF_VERSION=1.10.9
# Tue, 13 Jan 2026 03:02:57 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 13 Jan 2026 03:02:57 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 13 Jan 2026 03:02:57 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 13 Jan 2026 03:02:57 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 13 Jan 2026 03:02:57 GMT
VOLUME [/var/lib/chronograf]
# Tue, 13 Jan 2026 03:02:57 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 13 Jan 2026 03:02:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Jan 2026 03:02:57 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:ce9b9afe4e779d4b89f92e338fcd7dde1b11be3e68cd4c559a53dc9328ce4b5e`  
		Last Modified: Tue, 13 Jan 2026 00:42:08 GMT  
		Size: 23.9 MB (23934118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98636f48664fa7713ca92453907c30a986eb7904d5b61e9b5600939686558872`  
		Last Modified: Tue, 13 Jan 2026 03:16:21 GMT  
		Size: 6.5 MB (6511797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afcc9f19f53b9cf27f68f3bf6ffac9e16876c44c2dccba2d42553b457f09f6a9`  
		Last Modified: Tue, 13 Jan 2026 03:03:09 GMT  
		Size: 46.3 MB (46320032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71e832636be91f6cc6b53e6818a295ee19e07ccd462ae2e3c1e21372d09db364`  
		Last Modified: Tue, 13 Jan 2026 03:03:15 GMT  
		Size: 12.2 KB (12244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45563d6b533d54cb0923504de0a85d169c2eb16dea1a2bd59a45c923343ce386`  
		Last Modified: Tue, 13 Jan 2026 03:03:15 GMT  
		Size: 11.9 KB (11903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c7798c5b24c073ddea2b190bd1d3ca3d1950cd905ccccb02cb48628d269cff`  
		Last Modified: Tue, 13 Jan 2026 03:03:08 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:dadc0272545bdb4d79c6821ef43eb9a925d893b1eaeb4ee2d3cf2f188d7812c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2874196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1acc4e39a06aefb56c7f9e35ebeab2574b57317d10790d0e3311c59c3a3674c8`

```dockerfile
```

-	Layers:
	-	`sha256:ab03fd2077b16e627f201c398a16843df1c165c2856cbe02e571a7462fbf3c5e`  
		Last Modified: Tue, 13 Jan 2026 04:39:31 GMT  
		Size: 2.9 MB (2858027 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:198292ca1a6d344ac0e12376713d0b2d6f2cc1269871cede2e0ef2769ced95ba`  
		Last Modified: Tue, 13 Jan 2026 04:39:31 GMT  
		Size: 16.2 KB (16169 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:latest` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:8fabc493b21b1a54965004da2d26b414d67d449655ff23fd3d3bac87b00de090
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.8 MB (81837705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d86037b14ea2e39a2df4fc316eab05973e03a911596ff0a243024a8208e2f1c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:19:43 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 13 Jan 2026 02:19:50 GMT
ENV CHRONOGRAF_VERSION=1.10.9
# Tue, 13 Jan 2026 02:19:50 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 13 Jan 2026 02:19:50 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 13 Jan 2026 02:19:50 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 13 Jan 2026 02:19:50 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 13 Jan 2026 02:19:50 GMT
VOLUME [/var/lib/chronograf]
# Tue, 13 Jan 2026 02:19:50 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 13 Jan 2026 02:19:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Jan 2026 02:19:50 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:33bdc9671af8942d96d2f78f67aeec06580065dde1272decac3732689ec7c0e8`  
		Last Modified: Tue, 13 Jan 2026 00:42:09 GMT  
		Size: 28.1 MB (28107889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cc6310fab39afa190ecc5161cceaa1eb36695352620a557f88e94c3a838721b`  
		Last Modified: Tue, 13 Jan 2026 02:20:09 GMT  
		Size: 7.7 MB (7696876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:549a592ab74e868f6aef56b9688e0a142cfeaad538cf0f689c2a3394daf66571`  
		Last Modified: Tue, 13 Jan 2026 02:20:12 GMT  
		Size: 46.0 MB (46008476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a988c038996109a0a07e5713dcb205aa4ff8a19cdc93a075645d0ec04494b80e`  
		Last Modified: Tue, 13 Jan 2026 02:20:08 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c5f351ad8064c72fb1f03aa05a2c7eb8549aa94f73af89b58980523f92ef535`  
		Last Modified: Tue, 13 Jan 2026 02:20:01 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a94dcc0d0c7256c16118217f500f6aad9381085f822785282de69d1305f95c2`  
		Last Modified: Tue, 13 Jan 2026 02:20:08 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:9737f03ac4f5bddfd3ae0a95a33f3a30899b993b88c8de1e34d68411db4c708a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2872195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c4ceccea032644b03a8620d1eda2192df4e66894d011334aabf6cf48acbbbd0`

```dockerfile
```

-	Layers:
	-	`sha256:efb72d9c089b44658955c2eba33b0f9f78a9cb89c105abc89cc127f199de6e47`  
		Last Modified: Tue, 13 Jan 2026 04:39:36 GMT  
		Size: 2.9 MB (2856003 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46c09c314009ba98652c89fb65f2c69181b95796d7a038651b0d8b2f780f77cb`  
		Last Modified: Tue, 13 Jan 2026 04:39:36 GMT  
		Size: 16.2 KB (16192 bytes)  
		MIME: application/vnd.in-toto+json
