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
		Last Modified: Tue, 13 Jan 2026 00:41:44 GMT  
		Size: 28.2 MB (28228572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f97a4c03663264daa07043a3f29f2d20b0f8166009a68253c911509bc54d620`  
		Last Modified: Tue, 13 Jan 2026 02:14:12 GMT  
		Size: 7.9 MB (7879303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1de3fdab9946b7fe91f7f64835d147fd55a0c2dd876ff89abcb4932975b563c`  
		Last Modified: Tue, 13 Jan 2026 02:14:27 GMT  
		Size: 48.9 MB (48867877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b98f709a51e0b7ad076ff093e6fbc62937fc424c617b44afb09050e162934c2`  
		Last Modified: Tue, 13 Jan 2026 02:14:19 GMT  
		Size: 12.2 KB (12240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d2105baf2c6f199637a6f8da17dd041da224c83e726af6c49c8490825887745`  
		Last Modified: Tue, 13 Jan 2026 02:14:11 GMT  
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
		Last Modified: Tue, 13 Jan 2026 04:39:26 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:42:03 GMT  
		Size: 23.9 MB (23934118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98636f48664fa7713ca92453907c30a986eb7904d5b61e9b5600939686558872`  
		Last Modified: Tue, 13 Jan 2026 03:03:08 GMT  
		Size: 6.5 MB (6511797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afcc9f19f53b9cf27f68f3bf6ffac9e16876c44c2dccba2d42553b457f09f6a9`  
		Last Modified: Tue, 13 Jan 2026 03:03:20 GMT  
		Size: 46.3 MB (46320032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71e832636be91f6cc6b53e6818a295ee19e07ccd462ae2e3c1e21372d09db364`  
		Last Modified: Tue, 13 Jan 2026 03:03:07 GMT  
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
		Last Modified: Tue, 13 Jan 2026 02:20:12 GMT  
		Size: 46.0 MB (46008476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a988c038996109a0a07e5713dcb205aa4ff8a19cdc93a075645d0ec04494b80e`  
		Last Modified: Tue, 13 Jan 2026 02:20:08 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c5f351ad8064c72fb1f03aa05a2c7eb8549aa94f73af89b58980523f92ef535`  
		Last Modified: Tue, 13 Jan 2026 02:20:08 GMT  
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
