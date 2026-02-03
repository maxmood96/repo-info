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
$ docker pull chronograf@sha256:530bd973da5741a8228c32c319ba296017170c5375c5d8f5dac380e6343a8552
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
$ docker pull chronograf@sha256:45aa7da8fd07c917f0b81b9229354f097ec81dbfc40d9e25bfbef2cfc0f72228
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.0 MB (85000652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2239fbd47e9acd33f72205fa2700b29a57b528c1b7defc3ab58e3ad54fe348b3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:43:39 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 03 Feb 2026 02:43:44 GMT
ENV CHRONOGRAF_VERSION=1.10.9
# Tue, 03 Feb 2026 02:43:44 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 03 Feb 2026 02:43:44 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 03 Feb 2026 02:43:44 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 03 Feb 2026 02:43:44 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 03 Feb 2026 02:43:44 GMT
VOLUME [/var/lib/chronograf]
# Tue, 03 Feb 2026 02:43:44 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 03 Feb 2026 02:43:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 03 Feb 2026 02:43:44 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:4831516dd0cb86845f5f902cb9b9d25b5c853152c337eb57e4737a9b7e2a2eb9`  
		Last Modified: Tue, 03 Feb 2026 01:13:33 GMT  
		Size: 28.2 MB (28228487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d832a8b23bd03ee26616a22b1c1e726107955d2bb687b64d1abf55d80b9ef46`  
		Last Modified: Tue, 03 Feb 2026 02:43:56 GMT  
		Size: 7.9 MB (7879833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0866d8ff3c769213e4f45f07b683ca8fbe9d3884d9550524c69cf8a9e0a14d0c`  
		Last Modified: Tue, 03 Feb 2026 02:43:57 GMT  
		Size: 48.9 MB (48867868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab0ca67b260ec18a154423f0bb4a80104a1fa46fcd4c081f87e39ebf4d49f8cc`  
		Last Modified: Tue, 03 Feb 2026 02:43:55 GMT  
		Size: 12.2 KB (12244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:897073ceef77ec5ec1763d1ba23bf9c117ea150ac1d246acfce144bc41eb9a41`  
		Last Modified: Tue, 03 Feb 2026 02:43:55 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f884f96a9a13252fe3683d44606dc301967a92be82099a04f4284840521d5d9`  
		Last Modified: Tue, 03 Feb 2026 02:43:56 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:4186f1511d79fa944ef29f8288220efb49b030414016bffcdcc2a758cd529c77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2871815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14086ce4dff01c2ae6810168e2dc833e98be020fb77101da309f97f5a31bea15`

```dockerfile
```

-	Layers:
	-	`sha256:96c0e54a1af2614a4429deb8fd8804388343d9294fcc6fca433f614084b582fc`  
		Last Modified: Tue, 03 Feb 2026 02:43:56 GMT  
		Size: 2.9 MB (2855730 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d54c1e3b5b8d8bcc4aff8c1e3090462fe76e012c2be268e35e3a55d4bb47c86`  
		Last Modified: Tue, 03 Feb 2026 02:43:55 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:42:03 GMT  
		Size: 23.9 MB (23934118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98636f48664fa7713ca92453907c30a986eb7904d5b61e9b5600939686558872`  
		Last Modified: Tue, 13 Jan 2026 03:03:08 GMT  
		Size: 6.5 MB (6511797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afcc9f19f53b9cf27f68f3bf6ffac9e16876c44c2dccba2d42553b457f09f6a9`  
		Last Modified: Tue, 13 Jan 2026 03:03:09 GMT  
		Size: 46.3 MB (46320032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71e832636be91f6cc6b53e6818a295ee19e07ccd462ae2e3c1e21372d09db364`  
		Last Modified: Tue, 13 Jan 2026 03:03:07 GMT  
		Size: 12.2 KB (12244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45563d6b533d54cb0923504de0a85d169c2eb16dea1a2bd59a45c923343ce386`  
		Last Modified: Tue, 13 Jan 2026 03:03:08 GMT  
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
		Last Modified: Tue, 13 Jan 2026 03:03:08 GMT  
		Size: 2.9 MB (2858027 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:198292ca1a6d344ac0e12376713d0b2d6f2cc1269871cede2e0ef2769ced95ba`  
		Last Modified: Tue, 13 Jan 2026 03:03:07 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:42:00 GMT  
		Size: 28.1 MB (28107889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cc6310fab39afa190ecc5161cceaa1eb36695352620a557f88e94c3a838721b`  
		Last Modified: Tue, 13 Jan 2026 02:20:02 GMT  
		Size: 7.7 MB (7696876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:549a592ab74e868f6aef56b9688e0a142cfeaad538cf0f689c2a3394daf66571`  
		Last Modified: Tue, 13 Jan 2026 02:20:02 GMT  
		Size: 46.0 MB (46008476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a988c038996109a0a07e5713dcb205aa4ff8a19cdc93a075645d0ec04494b80e`  
		Last Modified: Tue, 13 Jan 2026 02:20:01 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c5f351ad8064c72fb1f03aa05a2c7eb8549aa94f73af89b58980523f92ef535`  
		Last Modified: Tue, 13 Jan 2026 02:20:01 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a94dcc0d0c7256c16118217f500f6aad9381085f822785282de69d1305f95c2`  
		Last Modified: Tue, 13 Jan 2026 02:20:02 GMT  
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
		Last Modified: Tue, 13 Jan 2026 02:20:01 GMT  
		Size: 2.9 MB (2856003 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46c09c314009ba98652c89fb65f2c69181b95796d7a038651b0d8b2f780f77cb`  
		Last Modified: Tue, 13 Jan 2026 02:20:01 GMT  
		Size: 16.2 KB (16192 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.10-alpine`

```console
$ docker pull chronograf@sha256:c73bbcdde515b06b9a7c553c92cc69c63197380e32554ac70bc487978d4f93e6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.10-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:f43a15493dfa286ecddb2a321f543ce0782328ace5a68abdb2f0a89fce86a0aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33281074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b149dbf0d54466603c75f2e0a21e5810e13c38a591a4994439fd92a43c9013c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:55:20 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:55:21 GMT
RUN apk add --no-cache ca-certificates setpriv &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 02:55:25 GMT
ENV CHRONOGRAF_VERSION=1.10.9
# Wed, 28 Jan 2026 02:55:25 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S chronograf &&     adduser -S chronograf -G chronograf &&     mkdir -m 0750 -p /var/lib/chronograf &&     chown chronograf:chronograf /var/lib/chronograf # buildkit
# Wed, 28 Jan 2026 02:55:25 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Wed, 28 Jan 2026 02:55:25 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Wed, 28 Jan 2026 02:55:25 GMT
EXPOSE map[8888/tcp:{}]
# Wed, 28 Jan 2026 02:55:25 GMT
VOLUME [/var/lib/chronograf]
# Wed, 28 Jan 2026 02:55:25 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 02:55:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 02:55:25 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:591c993c7d9033fa7cd78076b049ddac7d6f79bb06902c7bca758812790bc053`  
		Last Modified: Wed, 28 Jan 2026 02:55:34 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15f6ae05ff7071010198493db629f7b76646c556858fc112d3810a1ff45e7f02`  
		Last Modified: Wed, 28 Jan 2026 02:55:34 GMT  
		Size: 314.6 KB (314627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9190cc8374b20721167e978930acc3c96665f9488132a58677f6a81dad90f698`  
		Last Modified: Wed, 28 Jan 2026 02:55:35 GMT  
		Size: 29.1 MB (29136848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52b20d4daed0b72a4ba10efc2998799a5aa3a7b3da28d6057aff046b6d170da1`  
		Last Modified: Wed, 28 Jan 2026 02:55:34 GMT  
		Size: 12.2 KB (12236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7a44a4a5cb211d460d00144b50703689629cd5cd3151aa8d989477af9fdddc9`  
		Last Modified: Wed, 28 Jan 2026 02:55:35 GMT  
		Size: 11.9 KB (11894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f1870665d6b671bf68d872d353e6f3dcf8bb876176ebe068d36ebd72cc60f1a`  
		Last Modified: Wed, 28 Jan 2026 02:55:35 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:206f2990c3926bcb3257f329fb9bde8aa579b6391b11966e1c6bcf9e465730b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.8 KB (269841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f49329baac7667c2c41eaab7ec9b27b1f8b819d763c6975b1c546cc58ced7f8`

```dockerfile
```

-	Layers:
	-	`sha256:8abfdf98ab51ee4676e152235fa5a48648b67d72067e3e04c029a7c821689679`  
		Last Modified: Wed, 28 Jan 2026 02:55:34 GMT  
		Size: 252.0 KB (252029 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c804bbf74bc55745b883375aede79021007da8c962a7342173f0a71dc7ff369e`  
		Last Modified: Wed, 28 Jan 2026 02:55:34 GMT  
		Size: 17.8 KB (17812 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.10.9`

```console
$ docker pull chronograf@sha256:530bd973da5741a8228c32c319ba296017170c5375c5d8f5dac380e6343a8552
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
$ docker pull chronograf@sha256:45aa7da8fd07c917f0b81b9229354f097ec81dbfc40d9e25bfbef2cfc0f72228
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.0 MB (85000652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2239fbd47e9acd33f72205fa2700b29a57b528c1b7defc3ab58e3ad54fe348b3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:43:39 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 03 Feb 2026 02:43:44 GMT
ENV CHRONOGRAF_VERSION=1.10.9
# Tue, 03 Feb 2026 02:43:44 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 03 Feb 2026 02:43:44 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 03 Feb 2026 02:43:44 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 03 Feb 2026 02:43:44 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 03 Feb 2026 02:43:44 GMT
VOLUME [/var/lib/chronograf]
# Tue, 03 Feb 2026 02:43:44 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 03 Feb 2026 02:43:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 03 Feb 2026 02:43:44 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:4831516dd0cb86845f5f902cb9b9d25b5c853152c337eb57e4737a9b7e2a2eb9`  
		Last Modified: Tue, 03 Feb 2026 01:13:33 GMT  
		Size: 28.2 MB (28228487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d832a8b23bd03ee26616a22b1c1e726107955d2bb687b64d1abf55d80b9ef46`  
		Last Modified: Tue, 03 Feb 2026 02:43:56 GMT  
		Size: 7.9 MB (7879833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0866d8ff3c769213e4f45f07b683ca8fbe9d3884d9550524c69cf8a9e0a14d0c`  
		Last Modified: Tue, 03 Feb 2026 02:43:57 GMT  
		Size: 48.9 MB (48867868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab0ca67b260ec18a154423f0bb4a80104a1fa46fcd4c081f87e39ebf4d49f8cc`  
		Last Modified: Tue, 03 Feb 2026 02:43:55 GMT  
		Size: 12.2 KB (12244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:897073ceef77ec5ec1763d1ba23bf9c117ea150ac1d246acfce144bc41eb9a41`  
		Last Modified: Tue, 03 Feb 2026 02:43:55 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f884f96a9a13252fe3683d44606dc301967a92be82099a04f4284840521d5d9`  
		Last Modified: Tue, 03 Feb 2026 02:43:56 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10.9` - unknown; unknown

```console
$ docker pull chronograf@sha256:4186f1511d79fa944ef29f8288220efb49b030414016bffcdcc2a758cd529c77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2871815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14086ce4dff01c2ae6810168e2dc833e98be020fb77101da309f97f5a31bea15`

```dockerfile
```

-	Layers:
	-	`sha256:96c0e54a1af2614a4429deb8fd8804388343d9294fcc6fca433f614084b582fc`  
		Last Modified: Tue, 03 Feb 2026 02:43:56 GMT  
		Size: 2.9 MB (2855730 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d54c1e3b5b8d8bcc4aff8c1e3090462fe76e012c2be268e35e3a55d4bb47c86`  
		Last Modified: Tue, 03 Feb 2026 02:43:55 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:42:03 GMT  
		Size: 23.9 MB (23934118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98636f48664fa7713ca92453907c30a986eb7904d5b61e9b5600939686558872`  
		Last Modified: Tue, 13 Jan 2026 03:03:08 GMT  
		Size: 6.5 MB (6511797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afcc9f19f53b9cf27f68f3bf6ffac9e16876c44c2dccba2d42553b457f09f6a9`  
		Last Modified: Tue, 13 Jan 2026 03:03:09 GMT  
		Size: 46.3 MB (46320032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71e832636be91f6cc6b53e6818a295ee19e07ccd462ae2e3c1e21372d09db364`  
		Last Modified: Tue, 13 Jan 2026 03:03:07 GMT  
		Size: 12.2 KB (12244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45563d6b533d54cb0923504de0a85d169c2eb16dea1a2bd59a45c923343ce386`  
		Last Modified: Tue, 13 Jan 2026 03:03:08 GMT  
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
		Last Modified: Tue, 13 Jan 2026 03:03:08 GMT  
		Size: 2.9 MB (2858027 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:198292ca1a6d344ac0e12376713d0b2d6f2cc1269871cede2e0ef2769ced95ba`  
		Last Modified: Tue, 13 Jan 2026 03:03:07 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:42:00 GMT  
		Size: 28.1 MB (28107889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cc6310fab39afa190ecc5161cceaa1eb36695352620a557f88e94c3a838721b`  
		Last Modified: Tue, 13 Jan 2026 02:20:02 GMT  
		Size: 7.7 MB (7696876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:549a592ab74e868f6aef56b9688e0a142cfeaad538cf0f689c2a3394daf66571`  
		Last Modified: Tue, 13 Jan 2026 02:20:02 GMT  
		Size: 46.0 MB (46008476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a988c038996109a0a07e5713dcb205aa4ff8a19cdc93a075645d0ec04494b80e`  
		Last Modified: Tue, 13 Jan 2026 02:20:01 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c5f351ad8064c72fb1f03aa05a2c7eb8549aa94f73af89b58980523f92ef535`  
		Last Modified: Tue, 13 Jan 2026 02:20:01 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a94dcc0d0c7256c16118217f500f6aad9381085f822785282de69d1305f95c2`  
		Last Modified: Tue, 13 Jan 2026 02:20:02 GMT  
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
		Last Modified: Tue, 13 Jan 2026 02:20:01 GMT  
		Size: 2.9 MB (2856003 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46c09c314009ba98652c89fb65f2c69181b95796d7a038651b0d8b2f780f77cb`  
		Last Modified: Tue, 13 Jan 2026 02:20:01 GMT  
		Size: 16.2 KB (16192 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.10.9-alpine`

```console
$ docker pull chronograf@sha256:c73bbcdde515b06b9a7c553c92cc69c63197380e32554ac70bc487978d4f93e6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.10.9-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:f43a15493dfa286ecddb2a321f543ce0782328ace5a68abdb2f0a89fce86a0aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33281074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b149dbf0d54466603c75f2e0a21e5810e13c38a591a4994439fd92a43c9013c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:55:20 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:55:21 GMT
RUN apk add --no-cache ca-certificates setpriv &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 02:55:25 GMT
ENV CHRONOGRAF_VERSION=1.10.9
# Wed, 28 Jan 2026 02:55:25 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S chronograf &&     adduser -S chronograf -G chronograf &&     mkdir -m 0750 -p /var/lib/chronograf &&     chown chronograf:chronograf /var/lib/chronograf # buildkit
# Wed, 28 Jan 2026 02:55:25 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Wed, 28 Jan 2026 02:55:25 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Wed, 28 Jan 2026 02:55:25 GMT
EXPOSE map[8888/tcp:{}]
# Wed, 28 Jan 2026 02:55:25 GMT
VOLUME [/var/lib/chronograf]
# Wed, 28 Jan 2026 02:55:25 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 02:55:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 02:55:25 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:591c993c7d9033fa7cd78076b049ddac7d6f79bb06902c7bca758812790bc053`  
		Last Modified: Wed, 28 Jan 2026 02:55:34 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15f6ae05ff7071010198493db629f7b76646c556858fc112d3810a1ff45e7f02`  
		Last Modified: Wed, 28 Jan 2026 02:55:34 GMT  
		Size: 314.6 KB (314627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9190cc8374b20721167e978930acc3c96665f9488132a58677f6a81dad90f698`  
		Last Modified: Wed, 28 Jan 2026 02:55:35 GMT  
		Size: 29.1 MB (29136848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52b20d4daed0b72a4ba10efc2998799a5aa3a7b3da28d6057aff046b6d170da1`  
		Last Modified: Wed, 28 Jan 2026 02:55:34 GMT  
		Size: 12.2 KB (12236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7a44a4a5cb211d460d00144b50703689629cd5cd3151aa8d989477af9fdddc9`  
		Last Modified: Wed, 28 Jan 2026 02:55:35 GMT  
		Size: 11.9 KB (11894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f1870665d6b671bf68d872d353e6f3dcf8bb876176ebe068d36ebd72cc60f1a`  
		Last Modified: Wed, 28 Jan 2026 02:55:35 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10.9-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:206f2990c3926bcb3257f329fb9bde8aa579b6391b11966e1c6bcf9e465730b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.8 KB (269841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f49329baac7667c2c41eaab7ec9b27b1f8b819d763c6975b1c546cc58ced7f8`

```dockerfile
```

-	Layers:
	-	`sha256:8abfdf98ab51ee4676e152235fa5a48648b67d72067e3e04c029a7c821689679`  
		Last Modified: Wed, 28 Jan 2026 02:55:34 GMT  
		Size: 252.0 KB (252029 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c804bbf74bc55745b883375aede79021007da8c962a7342173f0a71dc7ff369e`  
		Last Modified: Wed, 28 Jan 2026 02:55:34 GMT  
		Size: 17.8 KB (17812 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.7`

```console
$ docker pull chronograf@sha256:72423d3681a1507e5e83d7aa10f834bb79eb993f8bf4f89f858d7482e57f50dc
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
$ docker pull chronograf@sha256:53867133dfe648b2c7c3b78e1022ca2f6258d69682e4d026e8b41a1470292267
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.2 MB (69230311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:503d4f964df130fd9037bbde7a8a4d8566cdf893ce3cd0f8edcd76505c388f25`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 02:43:19 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 03 Feb 2026 02:43:25 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 03 Feb 2026 02:43:25 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 03 Feb 2026 02:43:25 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 03 Feb 2026 02:43:25 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 03 Feb 2026 02:43:25 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 03 Feb 2026 02:43:25 GMT
VOLUME [/var/lib/chronograf]
# Tue, 03 Feb 2026 02:43:25 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 03 Feb 2026 02:43:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 03 Feb 2026 02:43:25 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:1c3e0f92551cc087b68faa686aead2fc80d99c54c34e9e72a0db197b668ac6be`  
		Last Modified: Tue, 03 Feb 2026 01:14:04 GMT  
		Size: 30.3 MB (30258284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7830f3c8edd68a8536376a96eca428e237aabb292d096a2452935caf7d382290`  
		Last Modified: Tue, 03 Feb 2026 02:43:35 GMT  
		Size: 4.2 MB (4209140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce66e9053c810acbb3e09870bd9d18606cc5210206194aabf768de271ca4e54d`  
		Last Modified: Tue, 03 Feb 2026 02:43:36 GMT  
		Size: 34.7 MB (34738488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1d5e6ecdb848e456edcf926ab5693567f2d8089fc14c37ec0bf4366e76737a8`  
		Last Modified: Tue, 03 Feb 2026 02:43:35 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13a9e67b4cecb96c3904448e95f7d7626086d1177ad02374c7375853df42f662`  
		Last Modified: Tue, 03 Feb 2026 02:43:35 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40044839b1b7bd6a19a179311edb247a95a27b50e66771847335ee3355d21f6f`  
		Last Modified: Tue, 03 Feb 2026 02:43:36 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7` - unknown; unknown

```console
$ docker pull chronograf@sha256:11717e304150636d10daa76841e5c0228c1c21f642922805b4d66c865d464dc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3064607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecbf9cfca557152f9d39254a2c7c141789e04c35cb1e726b3e2b0b443b6d6fd3`

```dockerfile
```

-	Layers:
	-	`sha256:65d32aaa8326f9dc0020b4adbaff20c595e511a4e087043b8f4eb14ae1b0da3e`  
		Last Modified: Tue, 03 Feb 2026 02:43:35 GMT  
		Size: 3.0 MB (3048873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f192d33621b6168ce80d19562c8b896769e4c6ef5ed347479bf3056094d95ba3`  
		Last Modified: Tue, 03 Feb 2026 02:43:35 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:42:24 GMT  
		Size: 25.5 MB (25546235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9251a13741298223fdfdc9be78334db81ff4f549edd0727a380f393b38821619`  
		Last Modified: Tue, 13 Jan 2026 02:59:29 GMT  
		Size: 3.5 MB (3511688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48701c41355a33b1cd2868933c2ed76cae2545cd6346942d912cf37ea72e476f`  
		Last Modified: Tue, 13 Jan 2026 02:59:30 GMT  
		Size: 33.1 MB (33097569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01af9d592d73eeef1d21a754c55f04464d6f50e5e310f9586072f3a741a5e0b8`  
		Last Modified: Tue, 13 Jan 2026 02:59:29 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41da3607200b9f79dfe6a0ddef1c9f298344dcb19a4f76189bf02e189becf75f`  
		Last Modified: Tue, 13 Jan 2026 02:59:29 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:41:51 GMT  
		Size: 28.7 MB (28748518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33ab95430f23401ffe30c5b7d6aeff523932df0d14da602f2e0aa5f04c8778a0`  
		Last Modified: Tue, 13 Jan 2026 02:16:32 GMT  
		Size: 4.2 MB (4210612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02f55cd2a4f1c21030ff008f48d4d8b081ba2c0785c293cff39d918b865882cb`  
		Last Modified: Tue, 13 Jan 2026 02:16:33 GMT  
		Size: 33.2 MB (33238151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25378f999a0dd8ef23b56d4d771571d8112385054b577da39a46571b760947c8`  
		Last Modified: Tue, 13 Jan 2026 02:16:31 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d635ef5c076321b1cffcb4b7f02e38a1ee40c27ef9d9a2de87e79574abb52ad1`  
		Last Modified: Tue, 13 Jan 2026 02:16:32 GMT  
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
		Last Modified: Tue, 13 Jan 2026 02:16:32 GMT  
		Size: 3.0 MB (3049122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4123bf76b137451bf5f9f0ab59ca134e2ed2e0258631dddaf852414cd58a931d`  
		Last Modified: Tue, 13 Jan 2026 02:16:31 GMT  
		Size: 15.8 KB (15829 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.7-alpine`

```console
$ docker pull chronograf@sha256:64bef3719ffd40e750e40a39da4c12abaa87dfb5feb5eda538abf94e3accb618
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.7-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:3f189f37cc38433df9fbac676c503a10acef7c7614624600135f250066886161
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.5 MB (23499863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8bec3fa8c5026e398c27b75bfa769e7655e34f7170bcdc9037dac726934f2ab`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:16 GMT
ADD alpine-minirootfs-3.20.9-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:16 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:53:36 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:53:36 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 02:53:40 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Wed, 28 Jan 2026 02:53:40 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Wed, 28 Jan 2026 02:53:40 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Wed, 28 Jan 2026 02:53:40 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Wed, 28 Jan 2026 02:53:40 GMT
EXPOSE map[8888/tcp:{}]
# Wed, 28 Jan 2026 02:53:40 GMT
VOLUME [/var/lib/chronograf]
# Wed, 28 Jan 2026 02:53:40 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 02:53:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 02:53:40 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:76eb174b37c3e263a212412822299b58d4098a7f96715f18c7eb6932c98b7efd`  
		Last Modified: Wed, 28 Jan 2026 01:18:21 GMT  
		Size: 3.6 MB (3627864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96b2964cc34286517fc6db4e61099dfdb5bb50b2c809f99bbe92d3490150811a`  
		Last Modified: Wed, 28 Jan 2026 02:53:47 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7abab41c57d391adf860ba3c6dc3cf0f0d1735950f94293661caa634ed79a539`  
		Last Modified: Wed, 28 Jan 2026 02:53:47 GMT  
		Size: 290.8 KB (290786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:340aae68687d2116364c9e894fd45843e9743365d10615f35ce86ed559892f63`  
		Last Modified: Wed, 28 Jan 2026 02:53:48 GMT  
		Size: 19.6 MB (19556564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27c53db3e00d80e1eb53e2db543c42e48bbe8cedbd46305f512e93b6a97dca45`  
		Last Modified: Wed, 28 Jan 2026 02:53:47 GMT  
		Size: 12.2 KB (12236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95dcdc4fbf054e697ef5ae3221a5d4fd5e2fdd105c6d4ff0de12003ee0b27b30`  
		Last Modified: Wed, 28 Jan 2026 02:53:48 GMT  
		Size: 11.9 KB (11895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffda149c9eaf485c096f2594f2e965917ccbc4373f09c74334e243c6b695c21c`  
		Last Modified: Wed, 28 Jan 2026 02:53:49 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:c56020b83aeb19cda9433c13248182ca3b3227bdfea0e3e87429fa828fce4e09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.7 KB (188701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f387fa3c690e841ea63c593cf9ab0ea8833159bbd96572eb1480d58af1824f1`

```dockerfile
```

-	Layers:
	-	`sha256:3952b13f0b8499685ee3fd998a70ea826c97a65c6f328d3185fff832bf3bfd8a`  
		Last Modified: Wed, 28 Jan 2026 02:53:47 GMT  
		Size: 171.8 KB (171832 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d7be3070420c927548a22fb90dc77dcced4eaf6f13c2cb97512b1fbff884e9e`  
		Last Modified: Wed, 28 Jan 2026 02:53:47 GMT  
		Size: 16.9 KB (16869 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.7.17`

```console
$ docker pull chronograf@sha256:72423d3681a1507e5e83d7aa10f834bb79eb993f8bf4f89f858d7482e57f50dc
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
$ docker pull chronograf@sha256:53867133dfe648b2c7c3b78e1022ca2f6258d69682e4d026e8b41a1470292267
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.2 MB (69230311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:503d4f964df130fd9037bbde7a8a4d8566cdf893ce3cd0f8edcd76505c388f25`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 02:43:19 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 03 Feb 2026 02:43:25 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 03 Feb 2026 02:43:25 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 03 Feb 2026 02:43:25 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 03 Feb 2026 02:43:25 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 03 Feb 2026 02:43:25 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 03 Feb 2026 02:43:25 GMT
VOLUME [/var/lib/chronograf]
# Tue, 03 Feb 2026 02:43:25 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 03 Feb 2026 02:43:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 03 Feb 2026 02:43:25 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:1c3e0f92551cc087b68faa686aead2fc80d99c54c34e9e72a0db197b668ac6be`  
		Last Modified: Tue, 03 Feb 2026 01:14:04 GMT  
		Size: 30.3 MB (30258284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7830f3c8edd68a8536376a96eca428e237aabb292d096a2452935caf7d382290`  
		Last Modified: Tue, 03 Feb 2026 02:43:35 GMT  
		Size: 4.2 MB (4209140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce66e9053c810acbb3e09870bd9d18606cc5210206194aabf768de271ca4e54d`  
		Last Modified: Tue, 03 Feb 2026 02:43:36 GMT  
		Size: 34.7 MB (34738488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1d5e6ecdb848e456edcf926ab5693567f2d8089fc14c37ec0bf4366e76737a8`  
		Last Modified: Tue, 03 Feb 2026 02:43:35 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13a9e67b4cecb96c3904448e95f7d7626086d1177ad02374c7375853df42f662`  
		Last Modified: Tue, 03 Feb 2026 02:43:35 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40044839b1b7bd6a19a179311edb247a95a27b50e66771847335ee3355d21f6f`  
		Last Modified: Tue, 03 Feb 2026 02:43:36 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7.17` - unknown; unknown

```console
$ docker pull chronograf@sha256:11717e304150636d10daa76841e5c0228c1c21f642922805b4d66c865d464dc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3064607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecbf9cfca557152f9d39254a2c7c141789e04c35cb1e726b3e2b0b443b6d6fd3`

```dockerfile
```

-	Layers:
	-	`sha256:65d32aaa8326f9dc0020b4adbaff20c595e511a4e087043b8f4eb14ae1b0da3e`  
		Last Modified: Tue, 03 Feb 2026 02:43:35 GMT  
		Size: 3.0 MB (3048873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f192d33621b6168ce80d19562c8b896769e4c6ef5ed347479bf3056094d95ba3`  
		Last Modified: Tue, 03 Feb 2026 02:43:35 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:42:24 GMT  
		Size: 25.5 MB (25546235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9251a13741298223fdfdc9be78334db81ff4f549edd0727a380f393b38821619`  
		Last Modified: Tue, 13 Jan 2026 02:59:29 GMT  
		Size: 3.5 MB (3511688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48701c41355a33b1cd2868933c2ed76cae2545cd6346942d912cf37ea72e476f`  
		Last Modified: Tue, 13 Jan 2026 02:59:30 GMT  
		Size: 33.1 MB (33097569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01af9d592d73eeef1d21a754c55f04464d6f50e5e310f9586072f3a741a5e0b8`  
		Last Modified: Tue, 13 Jan 2026 02:59:29 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41da3607200b9f79dfe6a0ddef1c9f298344dcb19a4f76189bf02e189becf75f`  
		Last Modified: Tue, 13 Jan 2026 02:59:29 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:41:51 GMT  
		Size: 28.7 MB (28748518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33ab95430f23401ffe30c5b7d6aeff523932df0d14da602f2e0aa5f04c8778a0`  
		Last Modified: Tue, 13 Jan 2026 02:16:32 GMT  
		Size: 4.2 MB (4210612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02f55cd2a4f1c21030ff008f48d4d8b081ba2c0785c293cff39d918b865882cb`  
		Last Modified: Tue, 13 Jan 2026 02:16:33 GMT  
		Size: 33.2 MB (33238151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25378f999a0dd8ef23b56d4d771571d8112385054b577da39a46571b760947c8`  
		Last Modified: Tue, 13 Jan 2026 02:16:31 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d635ef5c076321b1cffcb4b7f02e38a1ee40c27ef9d9a2de87e79574abb52ad1`  
		Last Modified: Tue, 13 Jan 2026 02:16:32 GMT  
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
		Last Modified: Tue, 13 Jan 2026 02:16:32 GMT  
		Size: 3.0 MB (3049122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4123bf76b137451bf5f9f0ab59ca134e2ed2e0258631dddaf852414cd58a931d`  
		Last Modified: Tue, 13 Jan 2026 02:16:31 GMT  
		Size: 15.8 KB (15829 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.7.17-alpine`

```console
$ docker pull chronograf@sha256:64bef3719ffd40e750e40a39da4c12abaa87dfb5feb5eda538abf94e3accb618
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.7.17-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:3f189f37cc38433df9fbac676c503a10acef7c7614624600135f250066886161
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.5 MB (23499863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8bec3fa8c5026e398c27b75bfa769e7655e34f7170bcdc9037dac726934f2ab`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:16 GMT
ADD alpine-minirootfs-3.20.9-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:16 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:53:36 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:53:36 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 02:53:40 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Wed, 28 Jan 2026 02:53:40 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Wed, 28 Jan 2026 02:53:40 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Wed, 28 Jan 2026 02:53:40 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Wed, 28 Jan 2026 02:53:40 GMT
EXPOSE map[8888/tcp:{}]
# Wed, 28 Jan 2026 02:53:40 GMT
VOLUME [/var/lib/chronograf]
# Wed, 28 Jan 2026 02:53:40 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 02:53:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 02:53:40 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:76eb174b37c3e263a212412822299b58d4098a7f96715f18c7eb6932c98b7efd`  
		Last Modified: Wed, 28 Jan 2026 01:18:21 GMT  
		Size: 3.6 MB (3627864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96b2964cc34286517fc6db4e61099dfdb5bb50b2c809f99bbe92d3490150811a`  
		Last Modified: Wed, 28 Jan 2026 02:53:47 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7abab41c57d391adf860ba3c6dc3cf0f0d1735950f94293661caa634ed79a539`  
		Last Modified: Wed, 28 Jan 2026 02:53:47 GMT  
		Size: 290.8 KB (290786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:340aae68687d2116364c9e894fd45843e9743365d10615f35ce86ed559892f63`  
		Last Modified: Wed, 28 Jan 2026 02:53:48 GMT  
		Size: 19.6 MB (19556564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27c53db3e00d80e1eb53e2db543c42e48bbe8cedbd46305f512e93b6a97dca45`  
		Last Modified: Wed, 28 Jan 2026 02:53:47 GMT  
		Size: 12.2 KB (12236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95dcdc4fbf054e697ef5ae3221a5d4fd5e2fdd105c6d4ff0de12003ee0b27b30`  
		Last Modified: Wed, 28 Jan 2026 02:53:48 GMT  
		Size: 11.9 KB (11895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffda149c9eaf485c096f2594f2e965917ccbc4373f09c74334e243c6b695c21c`  
		Last Modified: Wed, 28 Jan 2026 02:53:49 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7.17-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:c56020b83aeb19cda9433c13248182ca3b3227bdfea0e3e87429fa828fce4e09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.7 KB (188701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f387fa3c690e841ea63c593cf9ab0ea8833159bbd96572eb1480d58af1824f1`

```dockerfile
```

-	Layers:
	-	`sha256:3952b13f0b8499685ee3fd998a70ea826c97a65c6f328d3185fff832bf3bfd8a`  
		Last Modified: Wed, 28 Jan 2026 02:53:47 GMT  
		Size: 171.8 KB (171832 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d7be3070420c927548a22fb90dc77dcced4eaf6f13c2cb97512b1fbff884e9e`  
		Last Modified: Wed, 28 Jan 2026 02:53:47 GMT  
		Size: 16.9 KB (16869 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.8`

```console
$ docker pull chronograf@sha256:9ee69a8f618309d8c924090192840ea69e1a611ab1f62b9869fd23a691da6539
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
$ docker pull chronograf@sha256:82a431f61c4d69afd5180b27e1bdc57a50393935607e215f7a38af8aabed59a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69871127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a739890f78def91defebb181a3dd344b42842180933110d985a1f5853a594a43`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 02:43:22 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 03 Feb 2026 02:43:27 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Tue, 03 Feb 2026 02:43:27 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 03 Feb 2026 02:43:27 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 03 Feb 2026 02:43:27 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 03 Feb 2026 02:43:27 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 03 Feb 2026 02:43:27 GMT
VOLUME [/var/lib/chronograf]
# Tue, 03 Feb 2026 02:43:27 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 03 Feb 2026 02:43:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 03 Feb 2026 02:43:27 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:1c3e0f92551cc087b68faa686aead2fc80d99c54c34e9e72a0db197b668ac6be`  
		Last Modified: Tue, 03 Feb 2026 01:14:04 GMT  
		Size: 30.3 MB (30258284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22b9b8171691d530d3ec2f27a2155d2036234c78d2f3acbb666976a0d1a294f9`  
		Last Modified: Tue, 03 Feb 2026 02:43:37 GMT  
		Size: 5.2 MB (5224154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90df1e0931fad7a130653cd382b06b9f20689a1b6b77234e063269a0e35fde2a`  
		Last Modified: Tue, 03 Feb 2026 02:43:38 GMT  
		Size: 34.4 MB (34364287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0062c30d02512d9ff1c445a959442491ed5f80b9ceb4b07032660fa609f5f213`  
		Last Modified: Tue, 03 Feb 2026 02:43:37 GMT  
		Size: 12.3 KB (12252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:954cdfd15de94c8c186393557c201820de686e916ee1c20a9154a1ad694697a2`  
		Last Modified: Tue, 03 Feb 2026 02:43:37 GMT  
		Size: 11.9 KB (11911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16fdf76f1a2da10f860fb25fb56a712100a150a0f05dc1896b9bbda93eb2d214`  
		Last Modified: Tue, 03 Feb 2026 02:43:38 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8` - unknown; unknown

```console
$ docker pull chronograf@sha256:0b08e298e576c3f079b070532e8989143d503241bbb24614a7721689685b8f95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3120285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52cf266c526cd82086229ebfa08307d139ef95fdc5e1ecdd89c00ad11870415b`

```dockerfile
```

-	Layers:
	-	`sha256:9db2c35606289e7a65ada290859169801b1965cc1f1bbffedcd68adfbef8cdde`  
		Last Modified: Tue, 03 Feb 2026 02:43:37 GMT  
		Size: 3.1 MB (3104511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38ac23ac6af04d5746f05ee970ad5655dee9161ebccb784c3107075e32e41cbb`  
		Last Modified: Tue, 03 Feb 2026 02:43:37 GMT  
		Size: 15.8 KB (15774 bytes)  
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
		Last Modified: Tue, 13 Jan 2026 00:42:24 GMT  
		Size: 25.5 MB (25546235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c3af1e938f362bb930435d10f56ec4ea6859d1431b0a896e6f54fba60c213fe`  
		Last Modified: Tue, 13 Jan 2026 03:00:44 GMT  
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
		Last Modified: Tue, 13 Jan 2026 03:00:43 GMT  
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
		Last Modified: Tue, 13 Jan 2026 03:00:44 GMT  
		Size: 3.1 MB (3106782 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12e270ff58d0ff8bc04a4b852b1b274de7f7d41b67cbba56d7c79b178635c2b7`  
		Last Modified: Tue, 13 Jan 2026 03:00:43 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:41:51 GMT  
		Size: 28.7 MB (28748518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:587d10d83b3e1b87161492140b9ab56e0604d050f1b45f8e23cda854e1789778`  
		Last Modified: Tue, 13 Jan 2026 02:17:34 GMT  
		Size: 5.2 MB (5208128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81ef6ca9328c3547d443598e197dc110c3452aeae47a45aa9f8644c527fff6e3`  
		Last Modified: Tue, 13 Jan 2026 02:17:35 GMT  
		Size: 32.4 MB (32429482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d75295f1c5f2df3e88b0a878a9198ad08e2bb0d3ca25c43a385cdb9a7ad1541b`  
		Last Modified: Tue, 13 Jan 2026 02:17:33 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37557cabd37c79d8c8e48bf9da8c60bca3a4e8d7743ca24a1f8dcfed494d2ef4`  
		Last Modified: Tue, 13 Jan 2026 02:17:34 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:348eace459d99be8e14a85552cf6c71abdd86e064bcdf18b37573f647fede08a`  
		Last Modified: Tue, 13 Jan 2026 02:17:35 GMT  
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
		Last Modified: Tue, 13 Jan 2026 02:17:34 GMT  
		Size: 3.1 MB (3104760 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac683dd20943c6afd7861e1f08a6f85e77936b5b7fdc8759f088e11ace292a41`  
		Last Modified: Tue, 13 Jan 2026 02:17:33 GMT  
		Size: 15.9 KB (15869 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.8-alpine`

```console
$ docker pull chronograf@sha256:eaa3bb3ccb8ee814154bf133b1f66211d509c29f6dd1e1526c10230e208b863c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.8-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:c2bf30f869435c0b92e73e5d840baecf10b7556dee1180eab812a2e5c64ee8e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23147301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42f2dae78c59d8c5be31f4f138985d18bd1ba2aeb87bccc37c803d766d4dfb56`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:16 GMT
ADD alpine-minirootfs-3.20.9-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:16 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:54:14 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:54:15 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 02:54:18 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Wed, 28 Jan 2026 02:54:18 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Wed, 28 Jan 2026 02:54:18 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Wed, 28 Jan 2026 02:54:18 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Wed, 28 Jan 2026 02:54:18 GMT
EXPOSE map[8888/tcp:{}]
# Wed, 28 Jan 2026 02:54:18 GMT
VOLUME [/var/lib/chronograf]
# Wed, 28 Jan 2026 02:54:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 02:54:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 02:54:18 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:76eb174b37c3e263a212412822299b58d4098a7f96715f18c7eb6932c98b7efd`  
		Last Modified: Wed, 28 Jan 2026 01:18:21 GMT  
		Size: 3.6 MB (3627864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11511055c1a92ee4826f4450c606b4c6fe01663551c2520901ee8904c7cc029e`  
		Last Modified: Wed, 28 Jan 2026 02:54:26 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc4e7cced7996c2c54d3705c37d6189dd45203311e86f379e19dac56c87d79c1`  
		Last Modified: Wed, 28 Jan 2026 02:54:26 GMT  
		Size: 290.8 KB (290775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e85e7552262500b34023157ef8b78d59c9f8aecf673d089df4240d9c9410eaf`  
		Last Modified: Wed, 28 Jan 2026 02:54:26 GMT  
		Size: 19.2 MB (19204012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57f59d04c053bed8109181709b7b72268373c858113d4d325f91a61c9860fe15`  
		Last Modified: Wed, 28 Jan 2026 02:54:26 GMT  
		Size: 12.2 KB (12237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a39810aef4e0fd17cd3dd3a5c3df656a78821f4433c31d84d22a70687f39fc8`  
		Last Modified: Wed, 28 Jan 2026 02:54:27 GMT  
		Size: 11.9 KB (11895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39803bc8b4320a837d54074da9cd5a373b5492fbb69ba833e15e82cb22d38c2e`  
		Last Modified: Wed, 28 Jan 2026 02:54:27 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:8db07f0161f7cd63e13b7a8ec9f585002560d6c1aeb6bf3bfe117e6023c60030
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.2 KB (245210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f169dc8bb776368bcf6aeabb508e8f02347ed3c83e3ce9438f29a553783f718`

```dockerfile
```

-	Layers:
	-	`sha256:2a4f2a2d49e087fc0c9683afc43c5a8338ed6ca288ed80700190e6600854103b`  
		Last Modified: Wed, 28 Jan 2026 02:54:26 GMT  
		Size: 228.3 KB (228341 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94417dbea42e77a238ff18ac37fde210a7fb42d1a5ba372bd1e9e6e02f0e3f2d`  
		Last Modified: Wed, 28 Jan 2026 02:54:26 GMT  
		Size: 16.9 KB (16869 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.8.10`

```console
$ docker pull chronograf@sha256:9ee69a8f618309d8c924090192840ea69e1a611ab1f62b9869fd23a691da6539
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
$ docker pull chronograf@sha256:82a431f61c4d69afd5180b27e1bdc57a50393935607e215f7a38af8aabed59a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69871127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a739890f78def91defebb181a3dd344b42842180933110d985a1f5853a594a43`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 02:43:22 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 03 Feb 2026 02:43:27 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Tue, 03 Feb 2026 02:43:27 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 03 Feb 2026 02:43:27 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 03 Feb 2026 02:43:27 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 03 Feb 2026 02:43:27 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 03 Feb 2026 02:43:27 GMT
VOLUME [/var/lib/chronograf]
# Tue, 03 Feb 2026 02:43:27 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 03 Feb 2026 02:43:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 03 Feb 2026 02:43:27 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:1c3e0f92551cc087b68faa686aead2fc80d99c54c34e9e72a0db197b668ac6be`  
		Last Modified: Tue, 03 Feb 2026 01:14:04 GMT  
		Size: 30.3 MB (30258284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22b9b8171691d530d3ec2f27a2155d2036234c78d2f3acbb666976a0d1a294f9`  
		Last Modified: Tue, 03 Feb 2026 02:43:37 GMT  
		Size: 5.2 MB (5224154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90df1e0931fad7a130653cd382b06b9f20689a1b6b77234e063269a0e35fde2a`  
		Last Modified: Tue, 03 Feb 2026 02:43:38 GMT  
		Size: 34.4 MB (34364287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0062c30d02512d9ff1c445a959442491ed5f80b9ceb4b07032660fa609f5f213`  
		Last Modified: Tue, 03 Feb 2026 02:43:37 GMT  
		Size: 12.3 KB (12252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:954cdfd15de94c8c186393557c201820de686e916ee1c20a9154a1ad694697a2`  
		Last Modified: Tue, 03 Feb 2026 02:43:37 GMT  
		Size: 11.9 KB (11911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16fdf76f1a2da10f860fb25fb56a712100a150a0f05dc1896b9bbda93eb2d214`  
		Last Modified: Tue, 03 Feb 2026 02:43:38 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:0b08e298e576c3f079b070532e8989143d503241bbb24614a7721689685b8f95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3120285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52cf266c526cd82086229ebfa08307d139ef95fdc5e1ecdd89c00ad11870415b`

```dockerfile
```

-	Layers:
	-	`sha256:9db2c35606289e7a65ada290859169801b1965cc1f1bbffedcd68adfbef8cdde`  
		Last Modified: Tue, 03 Feb 2026 02:43:37 GMT  
		Size: 3.1 MB (3104511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38ac23ac6af04d5746f05ee970ad5655dee9161ebccb784c3107075e32e41cbb`  
		Last Modified: Tue, 03 Feb 2026 02:43:37 GMT  
		Size: 15.8 KB (15774 bytes)  
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
		Last Modified: Tue, 13 Jan 2026 00:42:24 GMT  
		Size: 25.5 MB (25546235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c3af1e938f362bb930435d10f56ec4ea6859d1431b0a896e6f54fba60c213fe`  
		Last Modified: Tue, 13 Jan 2026 03:00:44 GMT  
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
		Last Modified: Tue, 13 Jan 2026 03:00:43 GMT  
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
		Last Modified: Tue, 13 Jan 2026 03:00:44 GMT  
		Size: 3.1 MB (3106782 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12e270ff58d0ff8bc04a4b852b1b274de7f7d41b67cbba56d7c79b178635c2b7`  
		Last Modified: Tue, 13 Jan 2026 03:00:43 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:41:51 GMT  
		Size: 28.7 MB (28748518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:587d10d83b3e1b87161492140b9ab56e0604d050f1b45f8e23cda854e1789778`  
		Last Modified: Tue, 13 Jan 2026 02:17:34 GMT  
		Size: 5.2 MB (5208128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81ef6ca9328c3547d443598e197dc110c3452aeae47a45aa9f8644c527fff6e3`  
		Last Modified: Tue, 13 Jan 2026 02:17:35 GMT  
		Size: 32.4 MB (32429482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d75295f1c5f2df3e88b0a878a9198ad08e2bb0d3ca25c43a385cdb9a7ad1541b`  
		Last Modified: Tue, 13 Jan 2026 02:17:33 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37557cabd37c79d8c8e48bf9da8c60bca3a4e8d7743ca24a1f8dcfed494d2ef4`  
		Last Modified: Tue, 13 Jan 2026 02:17:34 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:348eace459d99be8e14a85552cf6c71abdd86e064bcdf18b37573f647fede08a`  
		Last Modified: Tue, 13 Jan 2026 02:17:35 GMT  
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
		Last Modified: Tue, 13 Jan 2026 02:17:34 GMT  
		Size: 3.1 MB (3104760 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac683dd20943c6afd7861e1f08a6f85e77936b5b7fdc8759f088e11ace292a41`  
		Last Modified: Tue, 13 Jan 2026 02:17:33 GMT  
		Size: 15.9 KB (15869 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.8.10-alpine`

```console
$ docker pull chronograf@sha256:eaa3bb3ccb8ee814154bf133b1f66211d509c29f6dd1e1526c10230e208b863c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.8.10-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:c2bf30f869435c0b92e73e5d840baecf10b7556dee1180eab812a2e5c64ee8e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23147301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42f2dae78c59d8c5be31f4f138985d18bd1ba2aeb87bccc37c803d766d4dfb56`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:16 GMT
ADD alpine-minirootfs-3.20.9-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:16 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:54:14 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:54:15 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 02:54:18 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Wed, 28 Jan 2026 02:54:18 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Wed, 28 Jan 2026 02:54:18 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Wed, 28 Jan 2026 02:54:18 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Wed, 28 Jan 2026 02:54:18 GMT
EXPOSE map[8888/tcp:{}]
# Wed, 28 Jan 2026 02:54:18 GMT
VOLUME [/var/lib/chronograf]
# Wed, 28 Jan 2026 02:54:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 02:54:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 02:54:18 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:76eb174b37c3e263a212412822299b58d4098a7f96715f18c7eb6932c98b7efd`  
		Last Modified: Wed, 28 Jan 2026 01:18:21 GMT  
		Size: 3.6 MB (3627864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11511055c1a92ee4826f4450c606b4c6fe01663551c2520901ee8904c7cc029e`  
		Last Modified: Wed, 28 Jan 2026 02:54:26 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc4e7cced7996c2c54d3705c37d6189dd45203311e86f379e19dac56c87d79c1`  
		Last Modified: Wed, 28 Jan 2026 02:54:26 GMT  
		Size: 290.8 KB (290775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e85e7552262500b34023157ef8b78d59c9f8aecf673d089df4240d9c9410eaf`  
		Last Modified: Wed, 28 Jan 2026 02:54:26 GMT  
		Size: 19.2 MB (19204012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57f59d04c053bed8109181709b7b72268373c858113d4d325f91a61c9860fe15`  
		Last Modified: Wed, 28 Jan 2026 02:54:26 GMT  
		Size: 12.2 KB (12237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a39810aef4e0fd17cd3dd3a5c3df656a78821f4433c31d84d22a70687f39fc8`  
		Last Modified: Wed, 28 Jan 2026 02:54:27 GMT  
		Size: 11.9 KB (11895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39803bc8b4320a837d54074da9cd5a373b5492fbb69ba833e15e82cb22d38c2e`  
		Last Modified: Wed, 28 Jan 2026 02:54:27 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8.10-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:8db07f0161f7cd63e13b7a8ec9f585002560d6c1aeb6bf3bfe117e6023c60030
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.2 KB (245210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f169dc8bb776368bcf6aeabb508e8f02347ed3c83e3ce9438f29a553783f718`

```dockerfile
```

-	Layers:
	-	`sha256:2a4f2a2d49e087fc0c9683afc43c5a8338ed6ca288ed80700190e6600854103b`  
		Last Modified: Wed, 28 Jan 2026 02:54:26 GMT  
		Size: 228.3 KB (228341 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94417dbea42e77a238ff18ac37fde210a7fb42d1a5ba372bd1e9e6e02f0e3f2d`  
		Last Modified: Wed, 28 Jan 2026 02:54:26 GMT  
		Size: 16.9 KB (16869 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.9`

```console
$ docker pull chronograf@sha256:b7438f948f7216ec23ba67e4a61e0eb532e0b6595005e4c09762b102a99809bf
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
$ docker pull chronograf@sha256:a45e8e64d17f42b9e9c279d0bf1889ebf89fe35e7b882a08570dd98508a15db6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.5 MB (70518609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4655efdd675a0a75671ce01aae0092e1ce6877121979aabc54172c30f42ad03`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 02:43:40 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 03 Feb 2026 02:43:44 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Tue, 03 Feb 2026 02:43:44 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 03 Feb 2026 02:43:44 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 03 Feb 2026 02:43:44 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 03 Feb 2026 02:43:44 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 03 Feb 2026 02:43:44 GMT
VOLUME [/var/lib/chronograf]
# Tue, 03 Feb 2026 02:43:44 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 03 Feb 2026 02:43:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 03 Feb 2026 02:43:44 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:1c3e0f92551cc087b68faa686aead2fc80d99c54c34e9e72a0db197b668ac6be`  
		Last Modified: Tue, 03 Feb 2026 01:14:04 GMT  
		Size: 30.3 MB (30258284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e5e4ec153d6920bdebb6be24cc5f807661e4f3adb033edef894113c413037d6`  
		Last Modified: Tue, 03 Feb 2026 02:43:54 GMT  
		Size: 5.2 MB (5224176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c284b94cdb59a4c9f31ec37144def8dca26a6907aa120f44967ce78d01125428`  
		Last Modified: Tue, 03 Feb 2026 02:43:55 GMT  
		Size: 35.0 MB (35011750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e57fc5618b979d68cdb22944bd81fff63de924b1f91e15151954cf9d8f1069e`  
		Last Modified: Tue, 03 Feb 2026 02:43:54 GMT  
		Size: 12.3 KB (12251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a9d94951f3496996faf5f42759f12fe7851be9b9b24a5f2b4e130a03650f2c1`  
		Last Modified: Tue, 03 Feb 2026 02:43:54 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b850e1d1f2d903e380c18a4a04a63c8e3b87f9b924fb8832125159099f68807d`  
		Last Modified: Tue, 03 Feb 2026 02:43:55 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9` - unknown; unknown

```console
$ docker pull chronograf@sha256:03162ca1a28f4b4bce87866220c4efe3bf401d8fa619f8a4aa9cca1ee8981749
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3125488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb6b8c3f4b49842e602eec2744868cbffb208b6e6d7efd1c46a712ff827660c1`

```dockerfile
```

-	Layers:
	-	`sha256:bd4cf9cd526f7bddb59f10de49d132869fcccdf36a27fc22df67a6750e7efeb5`  
		Last Modified: Tue, 03 Feb 2026 02:43:54 GMT  
		Size: 3.1 MB (3109721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fddcad924cd9928d89fa886b12280a937645f1ef9f1643edd90a25e00273a917`  
		Last Modified: Tue, 03 Feb 2026 02:43:54 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:42:24 GMT  
		Size: 25.5 MB (25546235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c3af1e938f362bb930435d10f56ec4ea6859d1431b0a896e6f54fba60c213fe`  
		Last Modified: Tue, 13 Jan 2026 03:00:44 GMT  
		Size: 4.5 MB (4490228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d65ff983806778d6f47f247f83d427970f7309d4aea50813b9f2bbcd4a7aba8`  
		Last Modified: Tue, 13 Jan 2026 03:01:46 GMT  
		Size: 33.3 MB (33311562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1b5ab788b7dd89d3233c3635cf42da4c696f58e3ad32aa6c4797a2c068ee159`  
		Last Modified: Tue, 13 Jan 2026 03:01:44 GMT  
		Size: 12.2 KB (12242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d25578a3ad4ec0f727aea9f33ccbbc1dc731e6b5f6f78303e3876cf3053dc73e`  
		Last Modified: Tue, 13 Jan 2026 03:01:45 GMT  
		Size: 11.9 KB (11900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bbd02315a11cae5575a0278b7b4f41912103c7936d3a3d659f2a87cf2d9993e`  
		Last Modified: Tue, 13 Jan 2026 03:01:44 GMT  
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
		Last Modified: Tue, 13 Jan 2026 03:01:44 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:41:51 GMT  
		Size: 28.7 MB (28748518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9675dbf3c11786b2e6b83e1ed02e53ebb77342287fd6825e2c892c5dc9c6002`  
		Last Modified: Tue, 13 Jan 2026 02:19:05 GMT  
		Size: 5.2 MB (5208172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36f3b66c8cafe4fbd166d9834903e13c26279e358d9739a73ac802ee2dc7e699`  
		Last Modified: Tue, 13 Jan 2026 02:19:06 GMT  
		Size: 33.2 MB (33182301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78e970438d49c8098fd527518cb476c47549a43d87d19fce3d4e41b5a4d5ee93`  
		Last Modified: Tue, 13 Jan 2026 02:19:04 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48b84714139ec00607a3895d5fa7f73a56da3c45c9b8669e4589752ddf09d6aa`  
		Last Modified: Tue, 13 Jan 2026 02:19:05 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7885b9908796aa4af090401044d65246add1a441e1e408dd6967e1ba441c99f2`  
		Last Modified: Tue, 13 Jan 2026 02:19:05 GMT  
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
		Last Modified: Tue, 13 Jan 2026 02:19:04 GMT  
		Size: 15.9 KB (15862 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.9-alpine`

```console
$ docker pull chronograf@sha256:fe4e3b3c10a641ad805b9ce0ec78cda2f470f49a830894c722953c8fb728fcb9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.9-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:67cedab187e8fc183d786cf2258d4005ec583930cc20e74da6812a9e7ff42a87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23615399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b67f6aa3073f13adbf88c9cccbd9ab0fbb58be572d0f96c9e48d3d49e2b1b015`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:16 GMT
ADD alpine-minirootfs-3.20.9-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:16 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:53:36 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:53:36 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 02:55:00 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Wed, 28 Jan 2026 02:55:00 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Wed, 28 Jan 2026 02:55:01 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Wed, 28 Jan 2026 02:55:01 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Wed, 28 Jan 2026 02:55:01 GMT
EXPOSE map[8888/tcp:{}]
# Wed, 28 Jan 2026 02:55:01 GMT
VOLUME [/var/lib/chronograf]
# Wed, 28 Jan 2026 02:55:01 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 02:55:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 02:55:01 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:76eb174b37c3e263a212412822299b58d4098a7f96715f18c7eb6932c98b7efd`  
		Last Modified: Wed, 28 Jan 2026 01:18:21 GMT  
		Size: 3.6 MB (3627864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96b2964cc34286517fc6db4e61099dfdb5bb50b2c809f99bbe92d3490150811a`  
		Last Modified: Wed, 28 Jan 2026 02:53:47 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7abab41c57d391adf860ba3c6dc3cf0f0d1735950f94293661caa634ed79a539`  
		Last Modified: Wed, 28 Jan 2026 02:53:47 GMT  
		Size: 290.8 KB (290786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49502ea6fb236afee58c16f44002da47fa15e3106a666c8b493bb26052c9274a`  
		Last Modified: Wed, 28 Jan 2026 02:55:08 GMT  
		Size: 19.7 MB (19672093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21543e57ca18bdf7a24a618747db1a314a907889b35e10bf5d53278ef3419640`  
		Last Modified: Wed, 28 Jan 2026 02:55:08 GMT  
		Size: 12.2 KB (12239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feac25ca50f9519d41319a760291be5f082cfa992b201b65d9f8ce0852c6735c`  
		Last Modified: Wed, 28 Jan 2026 02:55:08 GMT  
		Size: 11.9 KB (11899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:579664805c4fdab94b0811a476f26cd0ce412bc8c0c5a0bab5ecbdba4b190a7d`  
		Last Modified: Wed, 28 Jan 2026 02:55:08 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:4b3df4976cd08554c6148388fc472cd29690db4573063bd6d7675893a2756bb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.4 KB (250419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af162ec484f5c5e51d9958dc581b210cf6055821574b4630fdb8d5c27c93cd1f`

```dockerfile
```

-	Layers:
	-	`sha256:e1fda32b72505ea72431129c688691bca18d6a71dfc54ac36b83c1657128e64c`  
		Last Modified: Wed, 28 Jan 2026 02:55:08 GMT  
		Size: 233.6 KB (233553 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0bd8be116a02c551af1fa72b7f056c9711e39f115b000563402cba9f992d61ff`  
		Last Modified: Wed, 28 Jan 2026 02:55:08 GMT  
		Size: 16.9 KB (16866 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.9.4`

```console
$ docker pull chronograf@sha256:b7438f948f7216ec23ba67e4a61e0eb532e0b6595005e4c09762b102a99809bf
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
$ docker pull chronograf@sha256:a45e8e64d17f42b9e9c279d0bf1889ebf89fe35e7b882a08570dd98508a15db6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.5 MB (70518609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4655efdd675a0a75671ce01aae0092e1ce6877121979aabc54172c30f42ad03`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 02:43:40 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 03 Feb 2026 02:43:44 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Tue, 03 Feb 2026 02:43:44 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 03 Feb 2026 02:43:44 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 03 Feb 2026 02:43:44 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 03 Feb 2026 02:43:44 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 03 Feb 2026 02:43:44 GMT
VOLUME [/var/lib/chronograf]
# Tue, 03 Feb 2026 02:43:44 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 03 Feb 2026 02:43:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 03 Feb 2026 02:43:44 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:1c3e0f92551cc087b68faa686aead2fc80d99c54c34e9e72a0db197b668ac6be`  
		Last Modified: Tue, 03 Feb 2026 01:14:04 GMT  
		Size: 30.3 MB (30258284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e5e4ec153d6920bdebb6be24cc5f807661e4f3adb033edef894113c413037d6`  
		Last Modified: Tue, 03 Feb 2026 02:43:54 GMT  
		Size: 5.2 MB (5224176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c284b94cdb59a4c9f31ec37144def8dca26a6907aa120f44967ce78d01125428`  
		Last Modified: Tue, 03 Feb 2026 02:43:55 GMT  
		Size: 35.0 MB (35011750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e57fc5618b979d68cdb22944bd81fff63de924b1f91e15151954cf9d8f1069e`  
		Last Modified: Tue, 03 Feb 2026 02:43:54 GMT  
		Size: 12.3 KB (12251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a9d94951f3496996faf5f42759f12fe7851be9b9b24a5f2b4e130a03650f2c1`  
		Last Modified: Tue, 03 Feb 2026 02:43:54 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b850e1d1f2d903e380c18a4a04a63c8e3b87f9b924fb8832125159099f68807d`  
		Last Modified: Tue, 03 Feb 2026 02:43:55 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9.4` - unknown; unknown

```console
$ docker pull chronograf@sha256:03162ca1a28f4b4bce87866220c4efe3bf401d8fa619f8a4aa9cca1ee8981749
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3125488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb6b8c3f4b49842e602eec2744868cbffb208b6e6d7efd1c46a712ff827660c1`

```dockerfile
```

-	Layers:
	-	`sha256:bd4cf9cd526f7bddb59f10de49d132869fcccdf36a27fc22df67a6750e7efeb5`  
		Last Modified: Tue, 03 Feb 2026 02:43:54 GMT  
		Size: 3.1 MB (3109721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fddcad924cd9928d89fa886b12280a937645f1ef9f1643edd90a25e00273a917`  
		Last Modified: Tue, 03 Feb 2026 02:43:54 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:42:24 GMT  
		Size: 25.5 MB (25546235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c3af1e938f362bb930435d10f56ec4ea6859d1431b0a896e6f54fba60c213fe`  
		Last Modified: Tue, 13 Jan 2026 03:00:44 GMT  
		Size: 4.5 MB (4490228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d65ff983806778d6f47f247f83d427970f7309d4aea50813b9f2bbcd4a7aba8`  
		Last Modified: Tue, 13 Jan 2026 03:01:46 GMT  
		Size: 33.3 MB (33311562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1b5ab788b7dd89d3233c3635cf42da4c696f58e3ad32aa6c4797a2c068ee159`  
		Last Modified: Tue, 13 Jan 2026 03:01:44 GMT  
		Size: 12.2 KB (12242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d25578a3ad4ec0f727aea9f33ccbbc1dc731e6b5f6f78303e3876cf3053dc73e`  
		Last Modified: Tue, 13 Jan 2026 03:01:45 GMT  
		Size: 11.9 KB (11900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bbd02315a11cae5575a0278b7b4f41912103c7936d3a3d659f2a87cf2d9993e`  
		Last Modified: Tue, 13 Jan 2026 03:01:44 GMT  
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
		Last Modified: Tue, 13 Jan 2026 03:01:44 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:41:51 GMT  
		Size: 28.7 MB (28748518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9675dbf3c11786b2e6b83e1ed02e53ebb77342287fd6825e2c892c5dc9c6002`  
		Last Modified: Tue, 13 Jan 2026 02:19:05 GMT  
		Size: 5.2 MB (5208172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36f3b66c8cafe4fbd166d9834903e13c26279e358d9739a73ac802ee2dc7e699`  
		Last Modified: Tue, 13 Jan 2026 02:19:06 GMT  
		Size: 33.2 MB (33182301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78e970438d49c8098fd527518cb476c47549a43d87d19fce3d4e41b5a4d5ee93`  
		Last Modified: Tue, 13 Jan 2026 02:19:04 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48b84714139ec00607a3895d5fa7f73a56da3c45c9b8669e4589752ddf09d6aa`  
		Last Modified: Tue, 13 Jan 2026 02:19:05 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7885b9908796aa4af090401044d65246add1a441e1e408dd6967e1ba441c99f2`  
		Last Modified: Tue, 13 Jan 2026 02:19:05 GMT  
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
		Last Modified: Tue, 13 Jan 2026 02:19:04 GMT  
		Size: 15.9 KB (15862 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.9.4-alpine`

```console
$ docker pull chronograf@sha256:fe4e3b3c10a641ad805b9ce0ec78cda2f470f49a830894c722953c8fb728fcb9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.9.4-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:67cedab187e8fc183d786cf2258d4005ec583930cc20e74da6812a9e7ff42a87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23615399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b67f6aa3073f13adbf88c9cccbd9ab0fbb58be572d0f96c9e48d3d49e2b1b015`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:16 GMT
ADD alpine-minirootfs-3.20.9-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:16 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:53:36 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:53:36 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 02:55:00 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Wed, 28 Jan 2026 02:55:00 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Wed, 28 Jan 2026 02:55:01 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Wed, 28 Jan 2026 02:55:01 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Wed, 28 Jan 2026 02:55:01 GMT
EXPOSE map[8888/tcp:{}]
# Wed, 28 Jan 2026 02:55:01 GMT
VOLUME [/var/lib/chronograf]
# Wed, 28 Jan 2026 02:55:01 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 02:55:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 02:55:01 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:76eb174b37c3e263a212412822299b58d4098a7f96715f18c7eb6932c98b7efd`  
		Last Modified: Wed, 28 Jan 2026 01:18:21 GMT  
		Size: 3.6 MB (3627864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96b2964cc34286517fc6db4e61099dfdb5bb50b2c809f99bbe92d3490150811a`  
		Last Modified: Wed, 28 Jan 2026 02:53:47 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7abab41c57d391adf860ba3c6dc3cf0f0d1735950f94293661caa634ed79a539`  
		Last Modified: Wed, 28 Jan 2026 02:53:47 GMT  
		Size: 290.8 KB (290786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49502ea6fb236afee58c16f44002da47fa15e3106a666c8b493bb26052c9274a`  
		Last Modified: Wed, 28 Jan 2026 02:55:08 GMT  
		Size: 19.7 MB (19672093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21543e57ca18bdf7a24a618747db1a314a907889b35e10bf5d53278ef3419640`  
		Last Modified: Wed, 28 Jan 2026 02:55:08 GMT  
		Size: 12.2 KB (12239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feac25ca50f9519d41319a760291be5f082cfa992b201b65d9f8ce0852c6735c`  
		Last Modified: Wed, 28 Jan 2026 02:55:08 GMT  
		Size: 11.9 KB (11899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:579664805c4fdab94b0811a476f26cd0ce412bc8c0c5a0bab5ecbdba4b190a7d`  
		Last Modified: Wed, 28 Jan 2026 02:55:08 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9.4-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:4b3df4976cd08554c6148388fc472cd29690db4573063bd6d7675893a2756bb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.4 KB (250419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af162ec484f5c5e51d9958dc581b210cf6055821574b4630fdb8d5c27c93cd1f`

```dockerfile
```

-	Layers:
	-	`sha256:e1fda32b72505ea72431129c688691bca18d6a71dfc54ac36b83c1657128e64c`  
		Last Modified: Wed, 28 Jan 2026 02:55:08 GMT  
		Size: 233.6 KB (233553 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0bd8be116a02c551af1fa72b7f056c9711e39f115b000563402cba9f992d61ff`  
		Last Modified: Wed, 28 Jan 2026 02:55:08 GMT  
		Size: 16.9 KB (16866 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:alpine`

```console
$ docker pull chronograf@sha256:c73bbcdde515b06b9a7c553c92cc69c63197380e32554ac70bc487978d4f93e6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:f43a15493dfa286ecddb2a321f543ce0782328ace5a68abdb2f0a89fce86a0aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33281074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b149dbf0d54466603c75f2e0a21e5810e13c38a591a4994439fd92a43c9013c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:55:20 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:55:21 GMT
RUN apk add --no-cache ca-certificates setpriv &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 02:55:25 GMT
ENV CHRONOGRAF_VERSION=1.10.9
# Wed, 28 Jan 2026 02:55:25 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S chronograf &&     adduser -S chronograf -G chronograf &&     mkdir -m 0750 -p /var/lib/chronograf &&     chown chronograf:chronograf /var/lib/chronograf # buildkit
# Wed, 28 Jan 2026 02:55:25 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Wed, 28 Jan 2026 02:55:25 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Wed, 28 Jan 2026 02:55:25 GMT
EXPOSE map[8888/tcp:{}]
# Wed, 28 Jan 2026 02:55:25 GMT
VOLUME [/var/lib/chronograf]
# Wed, 28 Jan 2026 02:55:25 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 02:55:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 02:55:25 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:591c993c7d9033fa7cd78076b049ddac7d6f79bb06902c7bca758812790bc053`  
		Last Modified: Wed, 28 Jan 2026 02:55:34 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15f6ae05ff7071010198493db629f7b76646c556858fc112d3810a1ff45e7f02`  
		Last Modified: Wed, 28 Jan 2026 02:55:34 GMT  
		Size: 314.6 KB (314627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9190cc8374b20721167e978930acc3c96665f9488132a58677f6a81dad90f698`  
		Last Modified: Wed, 28 Jan 2026 02:55:35 GMT  
		Size: 29.1 MB (29136848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52b20d4daed0b72a4ba10efc2998799a5aa3a7b3da28d6057aff046b6d170da1`  
		Last Modified: Wed, 28 Jan 2026 02:55:34 GMT  
		Size: 12.2 KB (12236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7a44a4a5cb211d460d00144b50703689629cd5cd3151aa8d989477af9fdddc9`  
		Last Modified: Wed, 28 Jan 2026 02:55:35 GMT  
		Size: 11.9 KB (11894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f1870665d6b671bf68d872d353e6f3dcf8bb876176ebe068d36ebd72cc60f1a`  
		Last Modified: Wed, 28 Jan 2026 02:55:35 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:206f2990c3926bcb3257f329fb9bde8aa579b6391b11966e1c6bcf9e465730b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.8 KB (269841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f49329baac7667c2c41eaab7ec9b27b1f8b819d763c6975b1c546cc58ced7f8`

```dockerfile
```

-	Layers:
	-	`sha256:8abfdf98ab51ee4676e152235fa5a48648b67d72067e3e04c029a7c821689679`  
		Last Modified: Wed, 28 Jan 2026 02:55:34 GMT  
		Size: 252.0 KB (252029 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c804bbf74bc55745b883375aede79021007da8c962a7342173f0a71dc7ff369e`  
		Last Modified: Wed, 28 Jan 2026 02:55:34 GMT  
		Size: 17.8 KB (17812 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:latest`

```console
$ docker pull chronograf@sha256:530bd973da5741a8228c32c319ba296017170c5375c5d8f5dac380e6343a8552
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
$ docker pull chronograf@sha256:45aa7da8fd07c917f0b81b9229354f097ec81dbfc40d9e25bfbef2cfc0f72228
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.0 MB (85000652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2239fbd47e9acd33f72205fa2700b29a57b528c1b7defc3ab58e3ad54fe348b3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:43:39 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 03 Feb 2026 02:43:44 GMT
ENV CHRONOGRAF_VERSION=1.10.9
# Tue, 03 Feb 2026 02:43:44 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 03 Feb 2026 02:43:44 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 03 Feb 2026 02:43:44 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 03 Feb 2026 02:43:44 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 03 Feb 2026 02:43:44 GMT
VOLUME [/var/lib/chronograf]
# Tue, 03 Feb 2026 02:43:44 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 03 Feb 2026 02:43:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 03 Feb 2026 02:43:44 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:4831516dd0cb86845f5f902cb9b9d25b5c853152c337eb57e4737a9b7e2a2eb9`  
		Last Modified: Tue, 03 Feb 2026 01:13:33 GMT  
		Size: 28.2 MB (28228487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d832a8b23bd03ee26616a22b1c1e726107955d2bb687b64d1abf55d80b9ef46`  
		Last Modified: Tue, 03 Feb 2026 02:43:56 GMT  
		Size: 7.9 MB (7879833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0866d8ff3c769213e4f45f07b683ca8fbe9d3884d9550524c69cf8a9e0a14d0c`  
		Last Modified: Tue, 03 Feb 2026 02:43:57 GMT  
		Size: 48.9 MB (48867868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab0ca67b260ec18a154423f0bb4a80104a1fa46fcd4c081f87e39ebf4d49f8cc`  
		Last Modified: Tue, 03 Feb 2026 02:43:55 GMT  
		Size: 12.2 KB (12244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:897073ceef77ec5ec1763d1ba23bf9c117ea150ac1d246acfce144bc41eb9a41`  
		Last Modified: Tue, 03 Feb 2026 02:43:55 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f884f96a9a13252fe3683d44606dc301967a92be82099a04f4284840521d5d9`  
		Last Modified: Tue, 03 Feb 2026 02:43:56 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:4186f1511d79fa944ef29f8288220efb49b030414016bffcdcc2a758cd529c77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2871815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14086ce4dff01c2ae6810168e2dc833e98be020fb77101da309f97f5a31bea15`

```dockerfile
```

-	Layers:
	-	`sha256:96c0e54a1af2614a4429deb8fd8804388343d9294fcc6fca433f614084b582fc`  
		Last Modified: Tue, 03 Feb 2026 02:43:56 GMT  
		Size: 2.9 MB (2855730 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d54c1e3b5b8d8bcc4aff8c1e3090462fe76e012c2be268e35e3a55d4bb47c86`  
		Last Modified: Tue, 03 Feb 2026 02:43:55 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:42:03 GMT  
		Size: 23.9 MB (23934118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98636f48664fa7713ca92453907c30a986eb7904d5b61e9b5600939686558872`  
		Last Modified: Tue, 13 Jan 2026 03:03:08 GMT  
		Size: 6.5 MB (6511797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afcc9f19f53b9cf27f68f3bf6ffac9e16876c44c2dccba2d42553b457f09f6a9`  
		Last Modified: Tue, 13 Jan 2026 03:03:09 GMT  
		Size: 46.3 MB (46320032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71e832636be91f6cc6b53e6818a295ee19e07ccd462ae2e3c1e21372d09db364`  
		Last Modified: Tue, 13 Jan 2026 03:03:07 GMT  
		Size: 12.2 KB (12244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45563d6b533d54cb0923504de0a85d169c2eb16dea1a2bd59a45c923343ce386`  
		Last Modified: Tue, 13 Jan 2026 03:03:08 GMT  
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
		Last Modified: Tue, 13 Jan 2026 03:03:08 GMT  
		Size: 2.9 MB (2858027 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:198292ca1a6d344ac0e12376713d0b2d6f2cc1269871cede2e0ef2769ced95ba`  
		Last Modified: Tue, 13 Jan 2026 03:03:07 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:42:00 GMT  
		Size: 28.1 MB (28107889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cc6310fab39afa190ecc5161cceaa1eb36695352620a557f88e94c3a838721b`  
		Last Modified: Tue, 13 Jan 2026 02:20:02 GMT  
		Size: 7.7 MB (7696876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:549a592ab74e868f6aef56b9688e0a142cfeaad538cf0f689c2a3394daf66571`  
		Last Modified: Tue, 13 Jan 2026 02:20:02 GMT  
		Size: 46.0 MB (46008476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a988c038996109a0a07e5713dcb205aa4ff8a19cdc93a075645d0ec04494b80e`  
		Last Modified: Tue, 13 Jan 2026 02:20:01 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c5f351ad8064c72fb1f03aa05a2c7eb8549aa94f73af89b58980523f92ef535`  
		Last Modified: Tue, 13 Jan 2026 02:20:01 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a94dcc0d0c7256c16118217f500f6aad9381085f822785282de69d1305f95c2`  
		Last Modified: Tue, 13 Jan 2026 02:20:02 GMT  
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
		Last Modified: Tue, 13 Jan 2026 02:20:01 GMT  
		Size: 2.9 MB (2856003 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46c09c314009ba98652c89fb65f2c69181b95796d7a038651b0d8b2f780f77cb`  
		Last Modified: Tue, 13 Jan 2026 02:20:01 GMT  
		Size: 16.2 KB (16192 bytes)  
		MIME: application/vnd.in-toto+json
