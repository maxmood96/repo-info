<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `chronograf`

-	[`chronograf:1.10`](#chronograf110)
-	[`chronograf:1.10-alpine`](#chronograf110-alpine)
-	[`chronograf:1.10.5`](#chronograf1105)
-	[`chronograf:1.10.5-alpine`](#chronograf1105-alpine)
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
$ docker pull chronograf@sha256:f6877613a1f76be6870685199e8080872c7256691affd70b0464cd2cf5bdc886
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
$ docker pull chronograf@sha256:55179cf3247aed84a08e6880b420d6b0d7d6c6e1f681cea25cd72ba48bdc0ae6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.2 MB (83154481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72b958df0fda7d82ce567ce17ab6ee07dcc5dbefe414410ce84ed2fd2c5fac70`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.10.5
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:bc0965b23a04fe7f2d9fb20f597008fcf89891de1c705ffc1c80483a1f098e4f`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 28.2 MB (28231580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16d1b25159cefd879024a50ac2a21f071888ee20994d1d560b1ed646bad30676`  
		Last Modified: Tue, 03 Dec 2024 02:29:26 GMT  
		Size: 7.7 MB (7680870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:504c8e1c66df44af38ba4711698f5fd119bd1d3c0a5d3cbbad222b6de6be76db`  
		Last Modified: Tue, 03 Dec 2024 02:29:26 GMT  
		Size: 47.2 MB (47217567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:838382be2ab64d8e09274691b82074f7619d8f270200fdeb820adb86bb0b2526`  
		Last Modified: Tue, 03 Dec 2024 02:29:26 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8597baf10c7f4991bb67c12ecd1064563d82773d44fa11fcb39fd1b11619e744`  
		Last Modified: Tue, 03 Dec 2024 02:29:26 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4e643f9b16da6d1d3b681b9d7db20df09ec9518cb56018c8f4b79af604725a3`  
		Last Modified: Tue, 03 Dec 2024 02:29:26 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:5720a12825375d7b7a0c1e253129b817d15fc760b5d1a434e73580621afbb3f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2721657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f55bf58b616a89619e2ca47656f498e76f513ab42fa925ea7ce02a488613b86`

```dockerfile
```

-	Layers:
	-	`sha256:f86610197bd4dd56307695e593f78f560f42c259a4481365558d72ef23ac213c`  
		Last Modified: Tue, 03 Dec 2024 02:29:26 GMT  
		Size: 2.7 MB (2705529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90853a1cf3a79efb76a02ecac0aabab26757acfc1ce2e9dea710f795ea378fe7`  
		Last Modified: Tue, 03 Dec 2024 02:29:26 GMT  
		Size: 16.1 KB (16128 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.10` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:45f678c553711d2db70d58535b9794b3ad28d4d84f59d79a55f54f272827789b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75517507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:902c66527b2d96a1b1c3a0c88cbe54876f2dbd2a511a4c5fcb504a5a7838819d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["bash"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.10.5
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:ddd3c6488ea8b62db6811ba136fe14cba70219532910e67a91ed3388ec9f5757`  
		Last Modified: Tue, 12 Nov 2024 00:56:42 GMT  
		Size: 24.7 MB (24718909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6550685acd063dc6cce640c6f10c1dfac73cc458f5b8b19ec449579a08ab1401`  
		Last Modified: Tue, 12 Nov 2024 16:06:26 GMT  
		Size: 6.5 MB (6497842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb4d9638c811aa475e3ef3dd738ebb9839a72c09623ca60283c170c2babda7f6`  
		Last Modified: Tue, 12 Nov 2024 16:06:27 GMT  
		Size: 44.3 MB (44276286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:009a1e4b1ee7537b61421076ee24fd717c335f249c42420356c0539a1f6899b9`  
		Last Modified: Tue, 12 Nov 2024 16:06:25 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f869afcceefe33812d97f686e429f4d846795d1cd930495accf77f409f2506`  
		Last Modified: Tue, 12 Nov 2024 16:06:26 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf3c728782b2eeb8dd6001ebe7610861c011ebe762fcafbd576160449ed7bcb0`  
		Last Modified: Tue, 12 Nov 2024 16:06:26 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:b310981b0390adbddba27b5ffa275d03002a50389474dc02ab36dd4e8c5b9ebf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2725282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:621bb400573b68da87ad02e9d81f7ae8827c3ae22bd31fdb1d8e42dd93d4bd88`

```dockerfile
```

-	Layers:
	-	`sha256:a7b6c982a3a1c70e9c895470939fb5317eb615837e1c7b10cdac4960efaf1f79`  
		Last Modified: Tue, 12 Nov 2024 16:06:26 GMT  
		Size: 2.7 MB (2709073 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6bda2b8c1e48a2737a6f3b881aea6e27ed53014051c50ff50e1613800ad657f8`  
		Last Modified: Tue, 12 Nov 2024 16:06:25 GMT  
		Size: 16.2 KB (16209 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.10` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:e7e6e8bcd037e4e3ef78dacf184dfd0607468688afcf34385ecf6fd6a43c688d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.5 MB (80513339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65251b89dd6b695070376aecd12bca6d93d4e0c50c538c14ead4ef1b8ad206e6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1733097600'
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.10.5
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:bb3f2b52e6af242cee1bc6c19ce79e05544f8a1d13f5a6c1e828d98d2dbdc94e`  
		Last Modified: Tue, 03 Dec 2024 01:30:11 GMT  
		Size: 28.1 MB (28058810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4b37923b73842e71b50c0097b23bdbf8c1fd5737de2267f0155b551b4a35e04`  
		Last Modified: Tue, 03 Dec 2024 05:43:25 GMT  
		Size: 7.5 MB (7459550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46cca2e9b8da36020418d166d65e08204386ea6f0f9c8322e4bd8326297bf576`  
		Last Modified: Tue, 03 Dec 2024 05:43:26 GMT  
		Size: 45.0 MB (44970512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af126f9679492862794ec3faa0aa3a04dc474c3487ed61d6e3362db8da417d84`  
		Last Modified: Tue, 03 Dec 2024 05:43:24 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e77b78079d47e9a8f9ddfb5a8c846820b91f9661f995c92a8e852ba1d225538`  
		Last Modified: Tue, 03 Dec 2024 05:43:24 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:811ed1b8177864765392b433bcdaadb9a7d967c62836d60595ad00bec37e4ba6`  
		Last Modified: Tue, 03 Dec 2024 05:43:25 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:38606c6e184fd9a185d7dc62063caf17e7fb05f859ff7cd6d02af14ab3413586
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2722036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:376b2d0b0fea4af460bac0228148298741be2212268e3bddd98b7980c0b1c4b1`

```dockerfile
```

-	Layers:
	-	`sha256:fa9dec0ce88733aebf94edfe9b94a5a4a2658b69f26d434dcfd834896edd7588`  
		Last Modified: Tue, 03 Dec 2024 05:43:25 GMT  
		Size: 2.7 MB (2705801 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:940877f4eedacf098fda84d4925a189fb1243588d36c9d11468460a06aeb4e1e`  
		Last Modified: Tue, 03 Dec 2024 05:43:24 GMT  
		Size: 16.2 KB (16235 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.10-alpine`

```console
$ docker pull chronograf@sha256:e917c05d49569ffc91363b69db1139b3aec3ea352d7e4ab116ac73b5276c1e63
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.10-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:9177fbf8d1abc0941d457afc9b0e50767dab53c0fa38968d0935948927429e18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31808028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09dbf6891fc635a202a911272984b230346ed88f7ed61e7c5b4e6699d84faef9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["/bin/sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
RUN apk add --no-cache ca-certificates su-exec &&     update-ca-certificates # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.10.5
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S chronograf &&     adduser -S chronograf -G chronograf &&     mkdir -m 0750 -p /var/lib/chronograf &&     chown chronograf:chronograf /var/lib/chronograf # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2d999415b039365cadf590cb0dee4382b11889c724dd0eab32e010a66c2dda7`  
		Last Modified: Tue, 12 Nov 2024 02:38:06 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd85d2cc53952cb93e416bed6638ae8631ac933e78edf15edc8f453889c78a4b`  
		Last Modified: Tue, 12 Nov 2024 02:38:09 GMT  
		Size: 292.6 KB (292626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09c8ac47ff12105d7e2e63bdfecfe44bad8e9ed2abbb6bf69e824e6185e38c30`  
		Last Modified: Tue, 12 Nov 2024 02:38:09 GMT  
		Size: 27.9 MB (27866799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11e56c6035356fa99cb81386116d4e7f9647b9d607a8d8bf3c7bad00f71e5ae4`  
		Last Modified: Tue, 12 Nov 2024 02:38:09 GMT  
		Size: 12.2 KB (12234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:404105c04126e648e925115b31e8503e9be79bff0ac07d22b960fce01cc68627`  
		Last Modified: Tue, 12 Nov 2024 02:38:09 GMT  
		Size: 11.9 KB (11892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a2d0f282dc22ee43b73a0bfff8802169fb0b6a1285ee756c538a46c2ffc4303`  
		Last Modified: Tue, 12 Nov 2024 02:38:09 GMT  
		Size: 293.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:fcf8a567d3540090f865ac052c59bda542cc0aebd2c1ad4413eadd03d956c0d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.8 KB (257758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe6ab8b16a87c767b2f89aa09b99f84a49a0f574642aff41a53d43e44085627d`

```dockerfile
```

-	Layers:
	-	`sha256:608de47fe583d55de96c34e4f648a275957c4723931f32f5bf45243c183b05fb`  
		Last Modified: Tue, 12 Nov 2024 02:38:09 GMT  
		Size: 239.9 KB (239903 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6cf620aebcdf5b9e70ca057c32bcd31da203ea2fc4f7048080488c8522073c0c`  
		Last Modified: Tue, 12 Nov 2024 02:38:09 GMT  
		Size: 17.9 KB (17855 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.10.5`

```console
$ docker pull chronograf@sha256:f6877613a1f76be6870685199e8080872c7256691affd70b0464cd2cf5bdc886
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `chronograf:1.10.5` - linux; amd64

```console
$ docker pull chronograf@sha256:55179cf3247aed84a08e6880b420d6b0d7d6c6e1f681cea25cd72ba48bdc0ae6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.2 MB (83154481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72b958df0fda7d82ce567ce17ab6ee07dcc5dbefe414410ce84ed2fd2c5fac70`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.10.5
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:bc0965b23a04fe7f2d9fb20f597008fcf89891de1c705ffc1c80483a1f098e4f`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 28.2 MB (28231580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16d1b25159cefd879024a50ac2a21f071888ee20994d1d560b1ed646bad30676`  
		Last Modified: Tue, 03 Dec 2024 02:29:26 GMT  
		Size: 7.7 MB (7680870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:504c8e1c66df44af38ba4711698f5fd119bd1d3c0a5d3cbbad222b6de6be76db`  
		Last Modified: Tue, 03 Dec 2024 02:29:26 GMT  
		Size: 47.2 MB (47217567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:838382be2ab64d8e09274691b82074f7619d8f270200fdeb820adb86bb0b2526`  
		Last Modified: Tue, 03 Dec 2024 02:29:26 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8597baf10c7f4991bb67c12ecd1064563d82773d44fa11fcb39fd1b11619e744`  
		Last Modified: Tue, 03 Dec 2024 02:29:26 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4e643f9b16da6d1d3b681b9d7db20df09ec9518cb56018c8f4b79af604725a3`  
		Last Modified: Tue, 03 Dec 2024 02:29:26 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10.5` - unknown; unknown

```console
$ docker pull chronograf@sha256:5720a12825375d7b7a0c1e253129b817d15fc760b5d1a434e73580621afbb3f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2721657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f55bf58b616a89619e2ca47656f498e76f513ab42fa925ea7ce02a488613b86`

```dockerfile
```

-	Layers:
	-	`sha256:f86610197bd4dd56307695e593f78f560f42c259a4481365558d72ef23ac213c`  
		Last Modified: Tue, 03 Dec 2024 02:29:26 GMT  
		Size: 2.7 MB (2705529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90853a1cf3a79efb76a02ecac0aabab26757acfc1ce2e9dea710f795ea378fe7`  
		Last Modified: Tue, 03 Dec 2024 02:29:26 GMT  
		Size: 16.1 KB (16128 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.10.5` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:45f678c553711d2db70d58535b9794b3ad28d4d84f59d79a55f54f272827789b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75517507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:902c66527b2d96a1b1c3a0c88cbe54876f2dbd2a511a4c5fcb504a5a7838819d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["bash"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.10.5
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:ddd3c6488ea8b62db6811ba136fe14cba70219532910e67a91ed3388ec9f5757`  
		Last Modified: Tue, 12 Nov 2024 00:56:42 GMT  
		Size: 24.7 MB (24718909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6550685acd063dc6cce640c6f10c1dfac73cc458f5b8b19ec449579a08ab1401`  
		Last Modified: Tue, 12 Nov 2024 16:06:26 GMT  
		Size: 6.5 MB (6497842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb4d9638c811aa475e3ef3dd738ebb9839a72c09623ca60283c170c2babda7f6`  
		Last Modified: Tue, 12 Nov 2024 16:06:27 GMT  
		Size: 44.3 MB (44276286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:009a1e4b1ee7537b61421076ee24fd717c335f249c42420356c0539a1f6899b9`  
		Last Modified: Tue, 12 Nov 2024 16:06:25 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f869afcceefe33812d97f686e429f4d846795d1cd930495accf77f409f2506`  
		Last Modified: Tue, 12 Nov 2024 16:06:26 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf3c728782b2eeb8dd6001ebe7610861c011ebe762fcafbd576160449ed7bcb0`  
		Last Modified: Tue, 12 Nov 2024 16:06:26 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10.5` - unknown; unknown

```console
$ docker pull chronograf@sha256:b310981b0390adbddba27b5ffa275d03002a50389474dc02ab36dd4e8c5b9ebf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2725282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:621bb400573b68da87ad02e9d81f7ae8827c3ae22bd31fdb1d8e42dd93d4bd88`

```dockerfile
```

-	Layers:
	-	`sha256:a7b6c982a3a1c70e9c895470939fb5317eb615837e1c7b10cdac4960efaf1f79`  
		Last Modified: Tue, 12 Nov 2024 16:06:26 GMT  
		Size: 2.7 MB (2709073 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6bda2b8c1e48a2737a6f3b881aea6e27ed53014051c50ff50e1613800ad657f8`  
		Last Modified: Tue, 12 Nov 2024 16:06:25 GMT  
		Size: 16.2 KB (16209 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.10.5` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:e7e6e8bcd037e4e3ef78dacf184dfd0607468688afcf34385ecf6fd6a43c688d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.5 MB (80513339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65251b89dd6b695070376aecd12bca6d93d4e0c50c538c14ead4ef1b8ad206e6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1733097600'
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.10.5
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:bb3f2b52e6af242cee1bc6c19ce79e05544f8a1d13f5a6c1e828d98d2dbdc94e`  
		Last Modified: Tue, 03 Dec 2024 01:30:11 GMT  
		Size: 28.1 MB (28058810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4b37923b73842e71b50c0097b23bdbf8c1fd5737de2267f0155b551b4a35e04`  
		Last Modified: Tue, 03 Dec 2024 05:43:25 GMT  
		Size: 7.5 MB (7459550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46cca2e9b8da36020418d166d65e08204386ea6f0f9c8322e4bd8326297bf576`  
		Last Modified: Tue, 03 Dec 2024 05:43:26 GMT  
		Size: 45.0 MB (44970512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af126f9679492862794ec3faa0aa3a04dc474c3487ed61d6e3362db8da417d84`  
		Last Modified: Tue, 03 Dec 2024 05:43:24 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e77b78079d47e9a8f9ddfb5a8c846820b91f9661f995c92a8e852ba1d225538`  
		Last Modified: Tue, 03 Dec 2024 05:43:24 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:811ed1b8177864765392b433bcdaadb9a7d967c62836d60595ad00bec37e4ba6`  
		Last Modified: Tue, 03 Dec 2024 05:43:25 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10.5` - unknown; unknown

```console
$ docker pull chronograf@sha256:38606c6e184fd9a185d7dc62063caf17e7fb05f859ff7cd6d02af14ab3413586
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2722036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:376b2d0b0fea4af460bac0228148298741be2212268e3bddd98b7980c0b1c4b1`

```dockerfile
```

-	Layers:
	-	`sha256:fa9dec0ce88733aebf94edfe9b94a5a4a2658b69f26d434dcfd834896edd7588`  
		Last Modified: Tue, 03 Dec 2024 05:43:25 GMT  
		Size: 2.7 MB (2705801 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:940877f4eedacf098fda84d4925a189fb1243588d36c9d11468460a06aeb4e1e`  
		Last Modified: Tue, 03 Dec 2024 05:43:24 GMT  
		Size: 16.2 KB (16235 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.10.5-alpine`

```console
$ docker pull chronograf@sha256:e917c05d49569ffc91363b69db1139b3aec3ea352d7e4ab116ac73b5276c1e63
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.10.5-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:9177fbf8d1abc0941d457afc9b0e50767dab53c0fa38968d0935948927429e18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31808028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09dbf6891fc635a202a911272984b230346ed88f7ed61e7c5b4e6699d84faef9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["/bin/sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
RUN apk add --no-cache ca-certificates su-exec &&     update-ca-certificates # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.10.5
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S chronograf &&     adduser -S chronograf -G chronograf &&     mkdir -m 0750 -p /var/lib/chronograf &&     chown chronograf:chronograf /var/lib/chronograf # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2d999415b039365cadf590cb0dee4382b11889c724dd0eab32e010a66c2dda7`  
		Last Modified: Tue, 12 Nov 2024 02:38:06 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd85d2cc53952cb93e416bed6638ae8631ac933e78edf15edc8f453889c78a4b`  
		Last Modified: Tue, 12 Nov 2024 02:38:09 GMT  
		Size: 292.6 KB (292626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09c8ac47ff12105d7e2e63bdfecfe44bad8e9ed2abbb6bf69e824e6185e38c30`  
		Last Modified: Tue, 12 Nov 2024 02:38:09 GMT  
		Size: 27.9 MB (27866799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11e56c6035356fa99cb81386116d4e7f9647b9d607a8d8bf3c7bad00f71e5ae4`  
		Last Modified: Tue, 12 Nov 2024 02:38:09 GMT  
		Size: 12.2 KB (12234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:404105c04126e648e925115b31e8503e9be79bff0ac07d22b960fce01cc68627`  
		Last Modified: Tue, 12 Nov 2024 02:38:09 GMT  
		Size: 11.9 KB (11892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a2d0f282dc22ee43b73a0bfff8802169fb0b6a1285ee756c538a46c2ffc4303`  
		Last Modified: Tue, 12 Nov 2024 02:38:09 GMT  
		Size: 293.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10.5-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:fcf8a567d3540090f865ac052c59bda542cc0aebd2c1ad4413eadd03d956c0d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.8 KB (257758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe6ab8b16a87c767b2f89aa09b99f84a49a0f574642aff41a53d43e44085627d`

```dockerfile
```

-	Layers:
	-	`sha256:608de47fe583d55de96c34e4f648a275957c4723931f32f5bf45243c183b05fb`  
		Last Modified: Tue, 12 Nov 2024 02:38:09 GMT  
		Size: 239.9 KB (239903 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6cf620aebcdf5b9e70ca057c32bcd31da203ea2fc4f7048080488c8522073c0c`  
		Last Modified: Tue, 12 Nov 2024 02:38:09 GMT  
		Size: 17.9 KB (17855 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.7`

```console
$ docker pull chronograf@sha256:6ea6e7156e35ae2edc2af86ce3f0840677029af457a4db8bb53805968ac5872c
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
$ docker pull chronograf@sha256:6d458cf3bc762184448ca6f9588554f68d7afbf767f09f122de5c806f6455f95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.0 MB (69019829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc5066df4326900df149a2ec999030938c404d9fc72f4a4edf50921cc6a4f63b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1733097600'
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:69fb10dc82f9580a647bd4638e741b2338cb8e2575d2be6f0bacfcada936a617`  
		Last Modified: Tue, 03 Dec 2024 01:27:21 GMT  
		Size: 30.3 MB (30252644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:735fe4fb3c88d3efedae80da47eb75f1945c3062f44b30c2474918bed32c4136`  
		Last Modified: Tue, 03 Dec 2024 02:29:19 GMT  
		Size: 4.2 MB (4209313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba224bcb5d59f303a2fe505109775eca98ef296d64b10994cb2858be32ab0e4b`  
		Last Modified: Tue, 03 Dec 2024 02:29:19 GMT  
		Size: 34.5 MB (34533478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87ee091d29f8b49cb8fb5604c33db0077b5aa3f53559b5bf60b37a2002167c65`  
		Last Modified: Tue, 03 Dec 2024 02:29:19 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:390be8b662a23fadc9cf8964ef13f32e79d43a13aabc7e866c0eaa7cb01d261c`  
		Last Modified: Tue, 03 Dec 2024 02:29:19 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d1e1695c77b377f003b2f8a0c298b1187214272668da4cdffde8e562da706c1`  
		Last Modified: Tue, 03 Dec 2024 02:29:20 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7` - unknown; unknown

```console
$ docker pull chronograf@sha256:aef9e724dd181b181b386c31dfa384d09bb5478f004a564f48986a7a12d35392
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2923612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7db84b8a4329645724323cad25da57ea925b484df30dee2c677083865b28af26`

```dockerfile
```

-	Layers:
	-	`sha256:2ec246bf9917edabf37d835d68c85cfd46cb0311b3256482dd373ead2d36a804`  
		Last Modified: Tue, 03 Dec 2024 02:29:19 GMT  
		Size: 2.9 MB (2907835 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b195ac5a47b65d5c9d3647b3b5817966fd6c1db2aebffdf105d55470da39995`  
		Last Modified: Tue, 03 Dec 2024 02:29:19 GMT  
		Size: 15.8 KB (15777 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.7` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:c1c5f694705fce3fbe449e7ed1b7bb044b5c15604880f4b148295401932e1fdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.0 MB (63038303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3544fa788e4eb9d2fa9e298d55283f7e96616ccbba747ad15d0bcd9821b8bc49`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["bash"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:bbaa022ef9e0b119beb47d4a40af03cbd55afe3bf050a7353d06e43694cf5c25`  
		Last Modified: Tue, 12 Nov 2024 00:57:51 GMT  
		Size: 26.6 MB (26609257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89e86de284799b39b69899ac399f34a7e299d0ca33cebde1afa32aa2fce74e7c`  
		Last Modified: Tue, 12 Nov 2024 16:03:41 GMT  
		Size: 3.5 MB (3511727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f595c92af9e20b5ce1f7f0d0b17c42f7b8d5fe65ee105cc8d6653f82c00d65f`  
		Last Modified: Tue, 12 Nov 2024 16:03:42 GMT  
		Size: 32.9 MB (32892923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08d3d977cf89ece02f427f7939d8234b22f1aa42137ee568d635f0b0d153e3e1`  
		Last Modified: Tue, 12 Nov 2024 16:03:41 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bd85221d37ddf5147c2ab226fdfa2606e9efa138e5efaded81d945fda08fe98`  
		Last Modified: Tue, 12 Nov 2024 16:03:41 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c9cdb5db7614542db1972a5e5227c5b5ae80fc3431a52f8a2e5ba9a264960b6`  
		Last Modified: Tue, 12 Nov 2024 16:03:42 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7` - unknown; unknown

```console
$ docker pull chronograf@sha256:ec43459aa0a16c69bf7f8625ae42ed8708bb247c9bcf3a06d91765694723aa6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2927829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61c0716827457303b9a452dd07c6643bc521dd374f0036bc41b11efe82ba15b2`

```dockerfile
```

-	Layers:
	-	`sha256:5b7dd43acae4dd22ac445e34bc88f5a97b86c965136335b517dade9815bddb18`  
		Last Modified: Tue, 12 Nov 2024 16:03:41 GMT  
		Size: 2.9 MB (2911980 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:764ac41752faa72e6c79507c775d81dd2f15bee47ab151c89e50f10188a04218`  
		Last Modified: Tue, 12 Nov 2024 16:03:41 GMT  
		Size: 15.8 KB (15849 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.7` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:2c0233b4350f10ffa8d8e3ccf53d3759adc164d243a11774542a2ba54621e34a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.0 MB (66012996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f89c2584d6d862a99aa34df1b82252ef3fa368beaa16a10a935c515860b4f81`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1733097600'
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:8861e715dd4ae7d0bd8da39ea24d5c695bc09f0f4e43ca5221686621a10cd31b`  
		Last Modified: Tue, 03 Dec 2024 01:30:38 GMT  
		Size: 28.7 MB (28744923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab8b977e081093f71ca462c72649a5c9ebc9295bc304fcf501f99b6870c57499`  
		Last Modified: Tue, 03 Dec 2024 05:42:08 GMT  
		Size: 4.2 MB (4210609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbf81119147351a202cfa531386599924ff88467f61b7551e7ff9cf1535c2fe3`  
		Last Modified: Tue, 03 Dec 2024 05:42:09 GMT  
		Size: 33.0 MB (33033070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd1b84a3e05881c647d1128e6a4fc6dd04a3d9b0d8a2942711fff57e4ec1f536`  
		Last Modified: Tue, 03 Dec 2024 05:42:07 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5817f0d49b2f7e3d8b0edd7fa40610bd014f181dceffad2bef15a0887f39f9f`  
		Last Modified: Tue, 03 Dec 2024 05:42:08 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c10cda3b44145c239bd4ff943432c72d8f00314330ab2e073d5fda056c92d83`  
		Last Modified: Tue, 03 Dec 2024 05:42:08 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7` - unknown; unknown

```console
$ docker pull chronograf@sha256:b40915adf7e660b021c014698cebbc9e3f4f3d694e8bd49f5dac1b3bff1fd619
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2923955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae8bbb534b070237fc2a595b5e55e3b064959754c54c5d9ae353dfc872ff43f7`

```dockerfile
```

-	Layers:
	-	`sha256:d8d1b6c6aa259d0ebf55d57fe633faa384cf95855c72f78be0ebc0c7586f23b8`  
		Last Modified: Tue, 03 Dec 2024 05:42:08 GMT  
		Size: 2.9 MB (2908083 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67c2c2600fb7c64b3c38aa18f2816a2218987c31cda1e745713ca4dc2213cd71`  
		Last Modified: Tue, 03 Dec 2024 05:42:07 GMT  
		Size: 15.9 KB (15872 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.7-alpine`

```console
$ docker pull chronograf@sha256:287ff0fe62f1d938c9f5a4276ffdac4b96b80a9fe3f1c5cd2a5fe136a8b60b07
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.7-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:e590b22cd07479b45e4b1e21199857d7b8dad3afdadf9fbf74affe9e22fbaeaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.5 MB (23496129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54ee9cbce84cddf5af1b3cec11a1bec04e7c131c56c4e0ab88301e36b1c61f66`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["/bin/sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2d999415b039365cadf590cb0dee4382b11889c724dd0eab32e010a66c2dda7`  
		Last Modified: Tue, 12 Nov 2024 02:38:06 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44bb0c63a516b7d1c4b6f1b8b33078458f7cbd1898070843f549e6d43cd5324d`  
		Last Modified: Tue, 12 Nov 2024 02:38:06 GMT  
		Size: 290.9 KB (290886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc9ab55224078be68f4a7871e8058733688c9eb20b9ac31ef4ecad44b26714f0`  
		Last Modified: Tue, 12 Nov 2024 02:38:07 GMT  
		Size: 19.6 MB (19556696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:782f73fe87195977b450fc5374cb4eb5706d48954c1f955f9a381f81c91a51b8`  
		Last Modified: Tue, 12 Nov 2024 02:38:07 GMT  
		Size: 12.2 KB (12233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e14c1d264bde5e62a8767474eb0bbec13ddf17d34ee732fe1b1fcfed60e89672`  
		Last Modified: Tue, 12 Nov 2024 02:38:07 GMT  
		Size: 11.9 KB (11892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e310fd68fe32a67bc64c8924a620d071699d04bea0e7015d71946c0ab8d28c43`  
		Last Modified: Tue, 12 Nov 2024 02:38:07 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:43cb3142ea3dde7754a8511a1bf59b24c421ce486acc40e35e5d2ca247019c12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.3 KB (188251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f960e3661dbab4d85d385021946762c4fe6b9774a09368fcf9fb0ef400426ed`

```dockerfile
```

-	Layers:
	-	`sha256:247771501dba854ae3371fbeb61ba23468ea08d067b3a7b9ce93ea0def7bd516`  
		Last Modified: Tue, 12 Nov 2024 02:38:06 GMT  
		Size: 171.3 KB (171339 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae95d3380a26f742724416d959bc64a1d708327eda838c26bff991cbbcd839e3`  
		Last Modified: Tue, 12 Nov 2024 02:38:06 GMT  
		Size: 16.9 KB (16912 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.7.17`

```console
$ docker pull chronograf@sha256:6ea6e7156e35ae2edc2af86ce3f0840677029af457a4db8bb53805968ac5872c
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
$ docker pull chronograf@sha256:6d458cf3bc762184448ca6f9588554f68d7afbf767f09f122de5c806f6455f95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.0 MB (69019829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc5066df4326900df149a2ec999030938c404d9fc72f4a4edf50921cc6a4f63b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1733097600'
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:69fb10dc82f9580a647bd4638e741b2338cb8e2575d2be6f0bacfcada936a617`  
		Last Modified: Tue, 03 Dec 2024 01:27:21 GMT  
		Size: 30.3 MB (30252644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:735fe4fb3c88d3efedae80da47eb75f1945c3062f44b30c2474918bed32c4136`  
		Last Modified: Tue, 03 Dec 2024 02:29:19 GMT  
		Size: 4.2 MB (4209313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba224bcb5d59f303a2fe505109775eca98ef296d64b10994cb2858be32ab0e4b`  
		Last Modified: Tue, 03 Dec 2024 02:29:19 GMT  
		Size: 34.5 MB (34533478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87ee091d29f8b49cb8fb5604c33db0077b5aa3f53559b5bf60b37a2002167c65`  
		Last Modified: Tue, 03 Dec 2024 02:29:19 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:390be8b662a23fadc9cf8964ef13f32e79d43a13aabc7e866c0eaa7cb01d261c`  
		Last Modified: Tue, 03 Dec 2024 02:29:19 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d1e1695c77b377f003b2f8a0c298b1187214272668da4cdffde8e562da706c1`  
		Last Modified: Tue, 03 Dec 2024 02:29:20 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7.17` - unknown; unknown

```console
$ docker pull chronograf@sha256:aef9e724dd181b181b386c31dfa384d09bb5478f004a564f48986a7a12d35392
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2923612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7db84b8a4329645724323cad25da57ea925b484df30dee2c677083865b28af26`

```dockerfile
```

-	Layers:
	-	`sha256:2ec246bf9917edabf37d835d68c85cfd46cb0311b3256482dd373ead2d36a804`  
		Last Modified: Tue, 03 Dec 2024 02:29:19 GMT  
		Size: 2.9 MB (2907835 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b195ac5a47b65d5c9d3647b3b5817966fd6c1db2aebffdf105d55470da39995`  
		Last Modified: Tue, 03 Dec 2024 02:29:19 GMT  
		Size: 15.8 KB (15777 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.7.17` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:c1c5f694705fce3fbe449e7ed1b7bb044b5c15604880f4b148295401932e1fdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.0 MB (63038303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3544fa788e4eb9d2fa9e298d55283f7e96616ccbba747ad15d0bcd9821b8bc49`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["bash"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:bbaa022ef9e0b119beb47d4a40af03cbd55afe3bf050a7353d06e43694cf5c25`  
		Last Modified: Tue, 12 Nov 2024 00:57:51 GMT  
		Size: 26.6 MB (26609257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89e86de284799b39b69899ac399f34a7e299d0ca33cebde1afa32aa2fce74e7c`  
		Last Modified: Tue, 12 Nov 2024 16:03:41 GMT  
		Size: 3.5 MB (3511727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f595c92af9e20b5ce1f7f0d0b17c42f7b8d5fe65ee105cc8d6653f82c00d65f`  
		Last Modified: Tue, 12 Nov 2024 16:03:42 GMT  
		Size: 32.9 MB (32892923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08d3d977cf89ece02f427f7939d8234b22f1aa42137ee568d635f0b0d153e3e1`  
		Last Modified: Tue, 12 Nov 2024 16:03:41 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bd85221d37ddf5147c2ab226fdfa2606e9efa138e5efaded81d945fda08fe98`  
		Last Modified: Tue, 12 Nov 2024 16:03:41 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c9cdb5db7614542db1972a5e5227c5b5ae80fc3431a52f8a2e5ba9a264960b6`  
		Last Modified: Tue, 12 Nov 2024 16:03:42 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7.17` - unknown; unknown

```console
$ docker pull chronograf@sha256:ec43459aa0a16c69bf7f8625ae42ed8708bb247c9bcf3a06d91765694723aa6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2927829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61c0716827457303b9a452dd07c6643bc521dd374f0036bc41b11efe82ba15b2`

```dockerfile
```

-	Layers:
	-	`sha256:5b7dd43acae4dd22ac445e34bc88f5a97b86c965136335b517dade9815bddb18`  
		Last Modified: Tue, 12 Nov 2024 16:03:41 GMT  
		Size: 2.9 MB (2911980 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:764ac41752faa72e6c79507c775d81dd2f15bee47ab151c89e50f10188a04218`  
		Last Modified: Tue, 12 Nov 2024 16:03:41 GMT  
		Size: 15.8 KB (15849 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.7.17` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:2c0233b4350f10ffa8d8e3ccf53d3759adc164d243a11774542a2ba54621e34a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.0 MB (66012996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f89c2584d6d862a99aa34df1b82252ef3fa368beaa16a10a935c515860b4f81`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1733097600'
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:8861e715dd4ae7d0bd8da39ea24d5c695bc09f0f4e43ca5221686621a10cd31b`  
		Last Modified: Tue, 03 Dec 2024 01:30:38 GMT  
		Size: 28.7 MB (28744923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab8b977e081093f71ca462c72649a5c9ebc9295bc304fcf501f99b6870c57499`  
		Last Modified: Tue, 03 Dec 2024 05:42:08 GMT  
		Size: 4.2 MB (4210609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbf81119147351a202cfa531386599924ff88467f61b7551e7ff9cf1535c2fe3`  
		Last Modified: Tue, 03 Dec 2024 05:42:09 GMT  
		Size: 33.0 MB (33033070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd1b84a3e05881c647d1128e6a4fc6dd04a3d9b0d8a2942711fff57e4ec1f536`  
		Last Modified: Tue, 03 Dec 2024 05:42:07 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5817f0d49b2f7e3d8b0edd7fa40610bd014f181dceffad2bef15a0887f39f9f`  
		Last Modified: Tue, 03 Dec 2024 05:42:08 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c10cda3b44145c239bd4ff943432c72d8f00314330ab2e073d5fda056c92d83`  
		Last Modified: Tue, 03 Dec 2024 05:42:08 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7.17` - unknown; unknown

```console
$ docker pull chronograf@sha256:b40915adf7e660b021c014698cebbc9e3f4f3d694e8bd49f5dac1b3bff1fd619
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2923955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae8bbb534b070237fc2a595b5e55e3b064959754c54c5d9ae353dfc872ff43f7`

```dockerfile
```

-	Layers:
	-	`sha256:d8d1b6c6aa259d0ebf55d57fe633faa384cf95855c72f78be0ebc0c7586f23b8`  
		Last Modified: Tue, 03 Dec 2024 05:42:08 GMT  
		Size: 2.9 MB (2908083 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67c2c2600fb7c64b3c38aa18f2816a2218987c31cda1e745713ca4dc2213cd71`  
		Last Modified: Tue, 03 Dec 2024 05:42:07 GMT  
		Size: 15.9 KB (15872 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.7.17-alpine`

```console
$ docker pull chronograf@sha256:287ff0fe62f1d938c9f5a4276ffdac4b96b80a9fe3f1c5cd2a5fe136a8b60b07
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.7.17-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:e590b22cd07479b45e4b1e21199857d7b8dad3afdadf9fbf74affe9e22fbaeaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.5 MB (23496129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54ee9cbce84cddf5af1b3cec11a1bec04e7c131c56c4e0ab88301e36b1c61f66`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["/bin/sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2d999415b039365cadf590cb0dee4382b11889c724dd0eab32e010a66c2dda7`  
		Last Modified: Tue, 12 Nov 2024 02:38:06 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44bb0c63a516b7d1c4b6f1b8b33078458f7cbd1898070843f549e6d43cd5324d`  
		Last Modified: Tue, 12 Nov 2024 02:38:06 GMT  
		Size: 290.9 KB (290886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc9ab55224078be68f4a7871e8058733688c9eb20b9ac31ef4ecad44b26714f0`  
		Last Modified: Tue, 12 Nov 2024 02:38:07 GMT  
		Size: 19.6 MB (19556696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:782f73fe87195977b450fc5374cb4eb5706d48954c1f955f9a381f81c91a51b8`  
		Last Modified: Tue, 12 Nov 2024 02:38:07 GMT  
		Size: 12.2 KB (12233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e14c1d264bde5e62a8767474eb0bbec13ddf17d34ee732fe1b1fcfed60e89672`  
		Last Modified: Tue, 12 Nov 2024 02:38:07 GMT  
		Size: 11.9 KB (11892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e310fd68fe32a67bc64c8924a620d071699d04bea0e7015d71946c0ab8d28c43`  
		Last Modified: Tue, 12 Nov 2024 02:38:07 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7.17-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:43cb3142ea3dde7754a8511a1bf59b24c421ce486acc40e35e5d2ca247019c12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.3 KB (188251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f960e3661dbab4d85d385021946762c4fe6b9774a09368fcf9fb0ef400426ed`

```dockerfile
```

-	Layers:
	-	`sha256:247771501dba854ae3371fbeb61ba23468ea08d067b3a7b9ce93ea0def7bd516`  
		Last Modified: Tue, 12 Nov 2024 02:38:06 GMT  
		Size: 171.3 KB (171339 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae95d3380a26f742724416d959bc64a1d708327eda838c26bff991cbbcd839e3`  
		Last Modified: Tue, 12 Nov 2024 02:38:06 GMT  
		Size: 16.9 KB (16912 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.8`

```console
$ docker pull chronograf@sha256:ea8a52e618c5770e7715951c58b8ac3eac4b8a926ade59d3bf64edce162b53b8
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
$ docker pull chronograf@sha256:ec5b235dbeef282ee1e1ac601b3b98e6a96c4b99b39c7603a925fdca0e5b2109
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.7 MB (69661611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3b403f3a8ff4d21f5d69a67c90f5dbf37d66ba57e5bf548c7eea2342b97560d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1733097600'
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:69fb10dc82f9580a647bd4638e741b2338cb8e2575d2be6f0bacfcada936a617`  
		Last Modified: Tue, 03 Dec 2024 01:27:21 GMT  
		Size: 30.3 MB (30252644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d37303ce9c86894db8bf447fd4078e6db29f48047eada71eca47f3542f7a0f5`  
		Last Modified: Tue, 03 Dec 2024 02:29:29 GMT  
		Size: 5.0 MB (5020301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:202e553d7140549791d579deab154b9569aaefe47274e7051cd9fb0d2c58328a`  
		Last Modified: Tue, 03 Dec 2024 02:29:30 GMT  
		Size: 34.4 MB (34364272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9492cc92464a2cc59e9311b34ff89436edd7f1130f938a91308780a58c6b062`  
		Last Modified: Tue, 03 Dec 2024 02:29:29 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e91f687157c235e3d140fb7b3700457e716df4599a2e62b45ecd7e69e5609b3`  
		Last Modified: Tue, 03 Dec 2024 02:29:29 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebea28d68d613ab1f03be199b0c801431765c42ca1a9814a8b8a9276fabb97ce`  
		Last Modified: Tue, 03 Dec 2024 02:29:30 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8` - unknown; unknown

```console
$ docker pull chronograf@sha256:985fd78b7bce95dab1359dd9f8a3c3eaeaf2c5e2e83fecc91322f24b3830396b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2979749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b630e108ece3ea8026d6883de1319cf332727e8166d4cae288fdd259da98789`

```dockerfile
```

-	Layers:
	-	`sha256:2ed1a3de410b3a7ef1c2873770e2ee04a13aa96edc115e5a0ae270108d174a65`  
		Last Modified: Tue, 03 Dec 2024 02:29:29 GMT  
		Size: 3.0 MB (2963933 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7005eee0dbc8f922c24afce3ebe8b58794b2c81d7a6a8cc8331de89f82d45549`  
		Last Modified: Tue, 03 Dec 2024 02:29:28 GMT  
		Size: 15.8 KB (15816 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.8` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:d7d6954d7fd4aab60890b8d7624bda675bcd549a9e54c8b1744a80ca07a85260
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63453986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99eb1856242f898da63b992fdd037edaa885004b3032c9ba497d8d6e201d97e2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["bash"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:bbaa022ef9e0b119beb47d4a40af03cbd55afe3bf050a7353d06e43694cf5c25`  
		Last Modified: Tue, 12 Nov 2024 00:57:51 GMT  
		Size: 26.6 MB (26609257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f76d0fca1db4a044faf08522a97847fc66e7e267da5542f8bc65fe610e106f08`  
		Last Modified: Tue, 12 Nov 2024 16:04:50 GMT  
		Size: 4.3 MB (4285456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25fcfa7230636b263ff76ac4fe23a9870068288825083d14e0f44f8aa58120d6`  
		Last Modified: Tue, 12 Nov 2024 16:04:51 GMT  
		Size: 32.5 MB (32534875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c77488472c2eb5f2d59dee7492b3e11d348378c2766df3a7bd3eb1d7529a8430`  
		Last Modified: Tue, 12 Nov 2024 16:04:50 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01ecc94ed5fa6cc46954c64eccdfeffce3f3a39fb6ec27cad3e9d782fc4e18df`  
		Last Modified: Tue, 12 Nov 2024 16:04:50 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed11325cad19cc333b89724dfc65d6f9fb0a427e7d283cecfb3d4c957486c1d1`  
		Last Modified: Tue, 12 Nov 2024 16:04:51 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8` - unknown; unknown

```console
$ docker pull chronograf@sha256:345fd6d64437794416af8b10c449de17a799b508c606e9370c4d0914a878985e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2983968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:958f2d498caf8465e94d71fa69743fb005c5cbd421727c7c546f1644374003dc`

```dockerfile
```

-	Layers:
	-	`sha256:ccacc90fc91acc02bd6fe5c06e4af6a45b91cd022df7f360fc21e0bacbbfd397`  
		Last Modified: Tue, 12 Nov 2024 16:04:50 GMT  
		Size: 3.0 MB (2968078 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22e52bbdfb233b28907f03d1027ca9b3da799269f95c42f01363cb4a5a227743`  
		Last Modified: Tue, 12 Nov 2024 16:04:49 GMT  
		Size: 15.9 KB (15890 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.8` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:0409fc98c6d1a79c0f15de438570d2864cdbb5d2c34fd050ade20a28225b0e10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66202304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfbed170ce86ee34a3fe9241ddc4e7e284a32eccd74bad1bc4785ad8a8c64892`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1733097600'
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:8861e715dd4ae7d0bd8da39ea24d5c695bc09f0f4e43ca5221686621a10cd31b`  
		Last Modified: Tue, 03 Dec 2024 01:30:38 GMT  
		Size: 28.7 MB (28744923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da8b91290b61b9dbf0c1ca830cb74b33b50374f57fb454328be3492d32d016d`  
		Last Modified: Tue, 03 Dec 2024 05:42:34 GMT  
		Size: 5.0 MB (5003514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a231c3d51e77e3e6ad0a600c2e89b7ce1227e89114a523bdb6251384e3a37f6`  
		Last Modified: Tue, 03 Dec 2024 05:42:35 GMT  
		Size: 32.4 MB (32429481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff4eaf89fa812754d2627ae8731287a1d485f44c1b6cacea42e343407c536e2f`  
		Last Modified: Tue, 03 Dec 2024 05:42:34 GMT  
		Size: 12.2 KB (12244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f707a49c193bc69ac5a48ae30baf2c4782b4ca58db1e8503ef9604932646614f`  
		Last Modified: Tue, 03 Dec 2024 05:42:34 GMT  
		Size: 11.9 KB (11903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a547c7181e83392b410136fdabcbd98df6eadc03fa1bf3c0d5b43f03fd60bbe`  
		Last Modified: Tue, 03 Dec 2024 05:42:35 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8` - unknown; unknown

```console
$ docker pull chronograf@sha256:657ae2a2a987986345d66993762aec52bcc0e1dc072768e424242914176ca3c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2980093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98d71e52ad03a24f7c2533b0cbf9635303d211dda56983de697a4ba198a754f6`

```dockerfile
```

-	Layers:
	-	`sha256:0fc59879149129906d53a1c6f790e26a9a24eecb8e5da76ccf729d98a2d1bd36`  
		Last Modified: Tue, 03 Dec 2024 05:42:34 GMT  
		Size: 3.0 MB (2964181 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d0bdb35ae8193134e24ce78f4e00ecd66214c04195e1ba27a0c127527b0a9ed`  
		Last Modified: Tue, 03 Dec 2024 05:42:34 GMT  
		Size: 15.9 KB (15912 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.8-alpine`

```console
$ docker pull chronograf@sha256:92dc915f49a171a9bff9c19efc9a24e8c79d4b27b352785d02e8b337da5c9289
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.8-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:bcb0d37b5c18fb36680f7eb5ce3e0453be8e8385449c26644be8e3f92518aa62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23143481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3be622339b1663b25fee8bc1addea46f9fe079dbde554e6cea10b9988b928b57`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["/bin/sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f837f0e9fa34b0ee2116e7f1db559192bed2b3210feab89b723dd970f6fdb28b`  
		Last Modified: Tue, 12 Nov 2024 02:38:08 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3982c112ae596e0cf07497f1016dc504b80fd0ad68cc723f7f2066e1aa7c0a55`  
		Last Modified: Tue, 12 Nov 2024 02:38:08 GMT  
		Size: 290.9 KB (290887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e7272e467da9f0a75a0f807ca4b262a06aee61541f7014b554868ade8fc95b`  
		Last Modified: Tue, 12 Nov 2024 02:38:08 GMT  
		Size: 19.2 MB (19204040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29657181aa450b81b61910eeb70b371a8216c40ae4a395a7a79a49f5956181f7`  
		Last Modified: Tue, 12 Nov 2024 02:38:08 GMT  
		Size: 12.2 KB (12237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2062c76035454d3284bbc7ca4f0c61310bbb4d60df320b9c9c456b4fdd023e8`  
		Last Modified: Tue, 12 Nov 2024 02:38:09 GMT  
		Size: 11.9 KB (11895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b05a1c7abb5eb31b653dd382a993cea9700df0838f570c317de0e5d211af6fc`  
		Last Modified: Tue, 12 Nov 2024 02:38:09 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:f8bddac8d03188aa5158f46ab76e02927dc923117f8eac59fa9ab0750bf56ade
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.2 KB (245222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3beca0b115f7a7d4f457168aa29385f5b3134e4b669263817d46a2a82e0370a4`

```dockerfile
```

-	Layers:
	-	`sha256:35214902caaa7ed50f2443bb8424883e23a2fe8f20c545e1260430164b8c05d9`  
		Last Modified: Tue, 12 Nov 2024 02:38:08 GMT  
		Size: 228.3 KB (228310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b14c355a1a64de3b8bb5d6a1704de421d53d0023b84d87ae4e790f4724694481`  
		Last Modified: Tue, 12 Nov 2024 02:38:08 GMT  
		Size: 16.9 KB (16912 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.8.10`

```console
$ docker pull chronograf@sha256:ea8a52e618c5770e7715951c58b8ac3eac4b8a926ade59d3bf64edce162b53b8
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
$ docker pull chronograf@sha256:ec5b235dbeef282ee1e1ac601b3b98e6a96c4b99b39c7603a925fdca0e5b2109
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.7 MB (69661611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3b403f3a8ff4d21f5d69a67c90f5dbf37d66ba57e5bf548c7eea2342b97560d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1733097600'
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:69fb10dc82f9580a647bd4638e741b2338cb8e2575d2be6f0bacfcada936a617`  
		Last Modified: Tue, 03 Dec 2024 01:27:21 GMT  
		Size: 30.3 MB (30252644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d37303ce9c86894db8bf447fd4078e6db29f48047eada71eca47f3542f7a0f5`  
		Last Modified: Tue, 03 Dec 2024 02:29:29 GMT  
		Size: 5.0 MB (5020301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:202e553d7140549791d579deab154b9569aaefe47274e7051cd9fb0d2c58328a`  
		Last Modified: Tue, 03 Dec 2024 02:29:30 GMT  
		Size: 34.4 MB (34364272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9492cc92464a2cc59e9311b34ff89436edd7f1130f938a91308780a58c6b062`  
		Last Modified: Tue, 03 Dec 2024 02:29:29 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e91f687157c235e3d140fb7b3700457e716df4599a2e62b45ecd7e69e5609b3`  
		Last Modified: Tue, 03 Dec 2024 02:29:29 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebea28d68d613ab1f03be199b0c801431765c42ca1a9814a8b8a9276fabb97ce`  
		Last Modified: Tue, 03 Dec 2024 02:29:30 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:985fd78b7bce95dab1359dd9f8a3c3eaeaf2c5e2e83fecc91322f24b3830396b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2979749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b630e108ece3ea8026d6883de1319cf332727e8166d4cae288fdd259da98789`

```dockerfile
```

-	Layers:
	-	`sha256:2ed1a3de410b3a7ef1c2873770e2ee04a13aa96edc115e5a0ae270108d174a65`  
		Last Modified: Tue, 03 Dec 2024 02:29:29 GMT  
		Size: 3.0 MB (2963933 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7005eee0dbc8f922c24afce3ebe8b58794b2c81d7a6a8cc8331de89f82d45549`  
		Last Modified: Tue, 03 Dec 2024 02:29:28 GMT  
		Size: 15.8 KB (15816 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.8.10` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:d7d6954d7fd4aab60890b8d7624bda675bcd549a9e54c8b1744a80ca07a85260
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63453986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99eb1856242f898da63b992fdd037edaa885004b3032c9ba497d8d6e201d97e2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["bash"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:bbaa022ef9e0b119beb47d4a40af03cbd55afe3bf050a7353d06e43694cf5c25`  
		Last Modified: Tue, 12 Nov 2024 00:57:51 GMT  
		Size: 26.6 MB (26609257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f76d0fca1db4a044faf08522a97847fc66e7e267da5542f8bc65fe610e106f08`  
		Last Modified: Tue, 12 Nov 2024 16:04:50 GMT  
		Size: 4.3 MB (4285456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25fcfa7230636b263ff76ac4fe23a9870068288825083d14e0f44f8aa58120d6`  
		Last Modified: Tue, 12 Nov 2024 16:04:51 GMT  
		Size: 32.5 MB (32534875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c77488472c2eb5f2d59dee7492b3e11d348378c2766df3a7bd3eb1d7529a8430`  
		Last Modified: Tue, 12 Nov 2024 16:04:50 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01ecc94ed5fa6cc46954c64eccdfeffce3f3a39fb6ec27cad3e9d782fc4e18df`  
		Last Modified: Tue, 12 Nov 2024 16:04:50 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed11325cad19cc333b89724dfc65d6f9fb0a427e7d283cecfb3d4c957486c1d1`  
		Last Modified: Tue, 12 Nov 2024 16:04:51 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:345fd6d64437794416af8b10c449de17a799b508c606e9370c4d0914a878985e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2983968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:958f2d498caf8465e94d71fa69743fb005c5cbd421727c7c546f1644374003dc`

```dockerfile
```

-	Layers:
	-	`sha256:ccacc90fc91acc02bd6fe5c06e4af6a45b91cd022df7f360fc21e0bacbbfd397`  
		Last Modified: Tue, 12 Nov 2024 16:04:50 GMT  
		Size: 3.0 MB (2968078 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22e52bbdfb233b28907f03d1027ca9b3da799269f95c42f01363cb4a5a227743`  
		Last Modified: Tue, 12 Nov 2024 16:04:49 GMT  
		Size: 15.9 KB (15890 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.8.10` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:0409fc98c6d1a79c0f15de438570d2864cdbb5d2c34fd050ade20a28225b0e10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66202304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfbed170ce86ee34a3fe9241ddc4e7e284a32eccd74bad1bc4785ad8a8c64892`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1733097600'
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:8861e715dd4ae7d0bd8da39ea24d5c695bc09f0f4e43ca5221686621a10cd31b`  
		Last Modified: Tue, 03 Dec 2024 01:30:38 GMT  
		Size: 28.7 MB (28744923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da8b91290b61b9dbf0c1ca830cb74b33b50374f57fb454328be3492d32d016d`  
		Last Modified: Tue, 03 Dec 2024 05:42:34 GMT  
		Size: 5.0 MB (5003514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a231c3d51e77e3e6ad0a600c2e89b7ce1227e89114a523bdb6251384e3a37f6`  
		Last Modified: Tue, 03 Dec 2024 05:42:35 GMT  
		Size: 32.4 MB (32429481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff4eaf89fa812754d2627ae8731287a1d485f44c1b6cacea42e343407c536e2f`  
		Last Modified: Tue, 03 Dec 2024 05:42:34 GMT  
		Size: 12.2 KB (12244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f707a49c193bc69ac5a48ae30baf2c4782b4ca58db1e8503ef9604932646614f`  
		Last Modified: Tue, 03 Dec 2024 05:42:34 GMT  
		Size: 11.9 KB (11903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a547c7181e83392b410136fdabcbd98df6eadc03fa1bf3c0d5b43f03fd60bbe`  
		Last Modified: Tue, 03 Dec 2024 05:42:35 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:657ae2a2a987986345d66993762aec52bcc0e1dc072768e424242914176ca3c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2980093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98d71e52ad03a24f7c2533b0cbf9635303d211dda56983de697a4ba198a754f6`

```dockerfile
```

-	Layers:
	-	`sha256:0fc59879149129906d53a1c6f790e26a9a24eecb8e5da76ccf729d98a2d1bd36`  
		Last Modified: Tue, 03 Dec 2024 05:42:34 GMT  
		Size: 3.0 MB (2964181 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d0bdb35ae8193134e24ce78f4e00ecd66214c04195e1ba27a0c127527b0a9ed`  
		Last Modified: Tue, 03 Dec 2024 05:42:34 GMT  
		Size: 15.9 KB (15912 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.8.10-alpine`

```console
$ docker pull chronograf@sha256:92dc915f49a171a9bff9c19efc9a24e8c79d4b27b352785d02e8b337da5c9289
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.8.10-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:bcb0d37b5c18fb36680f7eb5ce3e0453be8e8385449c26644be8e3f92518aa62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23143481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3be622339b1663b25fee8bc1addea46f9fe079dbde554e6cea10b9988b928b57`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["/bin/sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f837f0e9fa34b0ee2116e7f1db559192bed2b3210feab89b723dd970f6fdb28b`  
		Last Modified: Tue, 12 Nov 2024 02:38:08 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3982c112ae596e0cf07497f1016dc504b80fd0ad68cc723f7f2066e1aa7c0a55`  
		Last Modified: Tue, 12 Nov 2024 02:38:08 GMT  
		Size: 290.9 KB (290887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e7272e467da9f0a75a0f807ca4b262a06aee61541f7014b554868ade8fc95b`  
		Last Modified: Tue, 12 Nov 2024 02:38:08 GMT  
		Size: 19.2 MB (19204040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29657181aa450b81b61910eeb70b371a8216c40ae4a395a7a79a49f5956181f7`  
		Last Modified: Tue, 12 Nov 2024 02:38:08 GMT  
		Size: 12.2 KB (12237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2062c76035454d3284bbc7ca4f0c61310bbb4d60df320b9c9c456b4fdd023e8`  
		Last Modified: Tue, 12 Nov 2024 02:38:09 GMT  
		Size: 11.9 KB (11895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b05a1c7abb5eb31b653dd382a993cea9700df0838f570c317de0e5d211af6fc`  
		Last Modified: Tue, 12 Nov 2024 02:38:09 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8.10-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:f8bddac8d03188aa5158f46ab76e02927dc923117f8eac59fa9ab0750bf56ade
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.2 KB (245222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3beca0b115f7a7d4f457168aa29385f5b3134e4b669263817d46a2a82e0370a4`

```dockerfile
```

-	Layers:
	-	`sha256:35214902caaa7ed50f2443bb8424883e23a2fe8f20c545e1260430164b8c05d9`  
		Last Modified: Tue, 12 Nov 2024 02:38:08 GMT  
		Size: 228.3 KB (228310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b14c355a1a64de3b8bb5d6a1704de421d53d0023b84d87ae4e790f4724694481`  
		Last Modified: Tue, 12 Nov 2024 02:38:08 GMT  
		Size: 16.9 KB (16912 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.9`

```console
$ docker pull chronograf@sha256:55a845451fd2c05ad43ed8ca30f986fd7efd871f9aefd7d04a656d1fa9530771
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
$ docker pull chronograf@sha256:47f6c566add0004a22c2245312a85ca7f91fd352c7b2b98556441bc0867f885a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.3 MB (70309129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:066b1cc3ea43f007990d458aec44b2ac938ab5df57e3a91daf0fa94d2ddc62fc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1733097600'
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:69fb10dc82f9580a647bd4638e741b2338cb8e2575d2be6f0bacfcada936a617`  
		Last Modified: Tue, 03 Dec 2024 01:27:21 GMT  
		Size: 30.3 MB (30252644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f71a1dbdfca2fcce5326b66841f5bb133ec975d82431c1fb3ec49ace2d4e0797`  
		Last Modified: Tue, 03 Dec 2024 02:29:23 GMT  
		Size: 5.0 MB (5020286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfcae033d795a31a50fd0fbbd9de1ccd097487215aaa6eb1213515552d476628`  
		Last Modified: Tue, 03 Dec 2024 02:29:24 GMT  
		Size: 35.0 MB (35011806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0918b6ee26aac502c1af068d3743ae970643640eaf0bcccab6639cf2f38e409c`  
		Last Modified: Tue, 03 Dec 2024 02:29:23 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eca3867e27debd77d1bd9a99c78819089ab895e59067e79f881e72066cb7641`  
		Last Modified: Tue, 03 Dec 2024 02:29:23 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa2e9fc737d2d37b93e3026c178859ab5bc0886861ebaf7df9076dc56804645a`  
		Last Modified: Tue, 03 Dec 2024 02:29:23 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9` - unknown; unknown

```console
$ docker pull chronograf@sha256:48d565524b3e3be8f08dd93d996a6a1b9cc9b31c34fed96b1631b0f8654f9449
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2984893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd68df59ecae1998f3f05afd2977b2ecb437a97457eb4f3ec85c25ca7447d363`

```dockerfile
```

-	Layers:
	-	`sha256:774770a7d4dab7e3fd9060ada79e634335cc41ed2bd4a5819ed1df0569ab399c`  
		Last Modified: Tue, 03 Dec 2024 02:29:23 GMT  
		Size: 3.0 MB (2969083 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e67b60a5138edd519bb345d285715cd6bf41c86b2c22f99b58905b3677fb0aae`  
		Last Modified: Tue, 03 Dec 2024 02:29:23 GMT  
		Size: 15.8 KB (15810 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.9` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:be1bc44ad7a448f8b76ed626885dd87bf8a64a4439948161d1b84dfb9da24c62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.2 MB (64230635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de60101b590c14bee87d0954707bf670bf8ee4fedb77b9da37d4c60708a1b5ca`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["bash"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:bbaa022ef9e0b119beb47d4a40af03cbd55afe3bf050a7353d06e43694cf5c25`  
		Last Modified: Tue, 12 Nov 2024 00:57:51 GMT  
		Size: 26.6 MB (26609257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f76d0fca1db4a044faf08522a97847fc66e7e267da5542f8bc65fe610e106f08`  
		Last Modified: Tue, 12 Nov 2024 16:04:50 GMT  
		Size: 4.3 MB (4285456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b925fe4b840e6b2aa003870d0a452f0c22fb0f736d62b6158e8d47cf0917a56f`  
		Last Modified: Tue, 12 Nov 2024 16:05:32 GMT  
		Size: 33.3 MB (33311523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a93dc802863f365b023bbdfa88ec35de4d4093e176cb5b89e698c26c9ab5d0b`  
		Last Modified: Tue, 12 Nov 2024 16:05:31 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddde9edf2a28beda7cc59a41fa8cbdf4d7054ff2e6d736760ea37deb61ec0e94`  
		Last Modified: Tue, 12 Nov 2024 16:05:31 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a53b6ad43a1916d84c5640b4c9c8046ce758fafc39f1dac7887492f182fcb03b`  
		Last Modified: Tue, 12 Nov 2024 16:05:31 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9` - unknown; unknown

```console
$ docker pull chronograf@sha256:a7a1ceb05758d05082c0a423533b7248fdf7d291aab10d2745f599b7169178ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2989111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8a9810a211ebfde38c90dee4d98d754313fe38f54e661363ac0fe34d4831dda`

```dockerfile
```

-	Layers:
	-	`sha256:bef13d45e3ddfd22f3337a796ae159b53a972132c5b63be4a7fe23b36d83f8e2`  
		Last Modified: Tue, 12 Nov 2024 16:05:31 GMT  
		Size: 3.0 MB (2973228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:177f0c391e14922c9b7ef31b6218c5499bcda996876d5a7e4215fd535aceae20`  
		Last Modified: Tue, 12 Nov 2024 16:05:31 GMT  
		Size: 15.9 KB (15883 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.9` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:e623da3d1a29b06636f1206d6d42169e36eb5c6cad1ec0f391675bfd782b383e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.0 MB (66954349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb1173e891b9fd8aa6ce77f3128ad2931d48d8a3a79746513cd9a5d11ecc735b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1733097600'
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:8861e715dd4ae7d0bd8da39ea24d5c695bc09f0f4e43ca5221686621a10cd31b`  
		Last Modified: Tue, 03 Dec 2024 01:30:38 GMT  
		Size: 28.7 MB (28744923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da8b91290b61b9dbf0c1ca830cb74b33b50374f57fb454328be3492d32d016d`  
		Last Modified: Tue, 03 Dec 2024 05:42:34 GMT  
		Size: 5.0 MB (5003514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:452c81186300372e9f2eca9be97efad26e64cf0d660842c0e36d1f5d342ce131`  
		Last Modified: Tue, 03 Dec 2024 05:42:56 GMT  
		Size: 33.2 MB (33181523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74ac105c95db5553f4df553fd1f74d9455713a67d3bd804f72eeb604e024427a`  
		Last Modified: Tue, 03 Dec 2024 05:42:54 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f76ba8cb1f6cfe8a94c4ebc35705dec02b7cdcf3eaaa2b90b3a2de447a3cd6d7`  
		Last Modified: Tue, 03 Dec 2024 05:42:55 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a5ae52db475159d47e19db5a9dd5f39b6dff1c89c8931e57d417bdf36ad93bd`  
		Last Modified: Tue, 03 Dec 2024 05:42:55 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9` - unknown; unknown

```console
$ docker pull chronograf@sha256:ae8f1a9ceca72594c276c95dc291db9a3f626da22bd8c1dd88097bde470f2178
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2985236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d4bba172b224aa4f78f5213c14503b5c439aeaaf8365589314cfe047c1a7073`

```dockerfile
```

-	Layers:
	-	`sha256:9075258b6e710aa70c635aa3cf7504574feaf59b990e52ed1ae7934c8d143357`  
		Last Modified: Tue, 03 Dec 2024 05:42:55 GMT  
		Size: 3.0 MB (2969331 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0387a095cbc0862b0ab4c85e0eaca43c284dc4086b27983c2bfca290f73ecd8`  
		Last Modified: Tue, 03 Dec 2024 05:42:54 GMT  
		Size: 15.9 KB (15905 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.9-alpine`

```console
$ docker pull chronograf@sha256:b52ddf6c80429a91e462840afcb013b449c5fa7b4b356c92a83490e61debe3c6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.9-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:e0b078ddef48edabb3edd67587d73dce0886f1676d777da47062ab1eed88b0da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23611520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23c5bb53ba7aca946cba46980d5ab416af7a303ae1e8c442f2ddfdd0486a3297`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["/bin/sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a938a04d3b903456f3b0c899a1ee719f0fbe0c20572ce8f8a333cbd7204c9424`  
		Last Modified: Tue, 12 Nov 2024 02:38:03 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e403debb40518414e6b358a892a18b3e5f0f7e54081cfeb9b07c2b3101c971a6`  
		Last Modified: Tue, 12 Nov 2024 02:38:03 GMT  
		Size: 290.9 KB (290888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fac7ca426c5927695eb459153d6e03440a125f298ee6e62fc6919e2107e3567b`  
		Last Modified: Tue, 12 Nov 2024 02:38:03 GMT  
		Size: 19.7 MB (19672077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81b5a34d409580ae00a43acde566afb4380ddaf799697c813b6950eb6182c8e3`  
		Last Modified: Tue, 12 Nov 2024 02:38:03 GMT  
		Size: 12.2 KB (12238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eed6f91e2c5f917da15268635d210a1b9b6578179b3c6e3ca8ddf34bfe965eb`  
		Last Modified: Tue, 12 Nov 2024 02:38:04 GMT  
		Size: 11.9 KB (11897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8e9b4f4321537230681e57bb52a6ee546109b0a5ce852c867370658982bab4a`  
		Last Modified: Tue, 12 Nov 2024 02:38:04 GMT  
		Size: 237.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:e401a0ae1338217c8774af1a7e7659865b503b32642d6b625261d45b377ad8b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.4 KB (250371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf3f1efc9c7e0a00983a84864956c0978fe19267c7224a63934dad2143b6116b`

```dockerfile
```

-	Layers:
	-	`sha256:b6b58d80490c4f66b398d6fe9770891de0d7a7dc51a5f8f529ef457e3b7c94f6`  
		Last Modified: Tue, 12 Nov 2024 02:38:03 GMT  
		Size: 233.5 KB (233462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9fe607b78ca533bf4dab527c8ab91e259f9b0e65f7abef6ead17fae5eb09ef2`  
		Last Modified: Tue, 12 Nov 2024 02:38:03 GMT  
		Size: 16.9 KB (16909 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.9.4`

```console
$ docker pull chronograf@sha256:55a845451fd2c05ad43ed8ca30f986fd7efd871f9aefd7d04a656d1fa9530771
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
$ docker pull chronograf@sha256:47f6c566add0004a22c2245312a85ca7f91fd352c7b2b98556441bc0867f885a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.3 MB (70309129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:066b1cc3ea43f007990d458aec44b2ac938ab5df57e3a91daf0fa94d2ddc62fc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1733097600'
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:69fb10dc82f9580a647bd4638e741b2338cb8e2575d2be6f0bacfcada936a617`  
		Last Modified: Tue, 03 Dec 2024 01:27:21 GMT  
		Size: 30.3 MB (30252644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f71a1dbdfca2fcce5326b66841f5bb133ec975d82431c1fb3ec49ace2d4e0797`  
		Last Modified: Tue, 03 Dec 2024 02:29:23 GMT  
		Size: 5.0 MB (5020286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfcae033d795a31a50fd0fbbd9de1ccd097487215aaa6eb1213515552d476628`  
		Last Modified: Tue, 03 Dec 2024 02:29:24 GMT  
		Size: 35.0 MB (35011806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0918b6ee26aac502c1af068d3743ae970643640eaf0bcccab6639cf2f38e409c`  
		Last Modified: Tue, 03 Dec 2024 02:29:23 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eca3867e27debd77d1bd9a99c78819089ab895e59067e79f881e72066cb7641`  
		Last Modified: Tue, 03 Dec 2024 02:29:23 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa2e9fc737d2d37b93e3026c178859ab5bc0886861ebaf7df9076dc56804645a`  
		Last Modified: Tue, 03 Dec 2024 02:29:23 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9.4` - unknown; unknown

```console
$ docker pull chronograf@sha256:48d565524b3e3be8f08dd93d996a6a1b9cc9b31c34fed96b1631b0f8654f9449
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2984893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd68df59ecae1998f3f05afd2977b2ecb437a97457eb4f3ec85c25ca7447d363`

```dockerfile
```

-	Layers:
	-	`sha256:774770a7d4dab7e3fd9060ada79e634335cc41ed2bd4a5819ed1df0569ab399c`  
		Last Modified: Tue, 03 Dec 2024 02:29:23 GMT  
		Size: 3.0 MB (2969083 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e67b60a5138edd519bb345d285715cd6bf41c86b2c22f99b58905b3677fb0aae`  
		Last Modified: Tue, 03 Dec 2024 02:29:23 GMT  
		Size: 15.8 KB (15810 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.9.4` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:be1bc44ad7a448f8b76ed626885dd87bf8a64a4439948161d1b84dfb9da24c62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.2 MB (64230635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de60101b590c14bee87d0954707bf670bf8ee4fedb77b9da37d4c60708a1b5ca`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["bash"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:bbaa022ef9e0b119beb47d4a40af03cbd55afe3bf050a7353d06e43694cf5c25`  
		Last Modified: Tue, 12 Nov 2024 00:57:51 GMT  
		Size: 26.6 MB (26609257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f76d0fca1db4a044faf08522a97847fc66e7e267da5542f8bc65fe610e106f08`  
		Last Modified: Tue, 12 Nov 2024 16:04:50 GMT  
		Size: 4.3 MB (4285456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b925fe4b840e6b2aa003870d0a452f0c22fb0f736d62b6158e8d47cf0917a56f`  
		Last Modified: Tue, 12 Nov 2024 16:05:32 GMT  
		Size: 33.3 MB (33311523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a93dc802863f365b023bbdfa88ec35de4d4093e176cb5b89e698c26c9ab5d0b`  
		Last Modified: Tue, 12 Nov 2024 16:05:31 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddde9edf2a28beda7cc59a41fa8cbdf4d7054ff2e6d736760ea37deb61ec0e94`  
		Last Modified: Tue, 12 Nov 2024 16:05:31 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a53b6ad43a1916d84c5640b4c9c8046ce758fafc39f1dac7887492f182fcb03b`  
		Last Modified: Tue, 12 Nov 2024 16:05:31 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9.4` - unknown; unknown

```console
$ docker pull chronograf@sha256:a7a1ceb05758d05082c0a423533b7248fdf7d291aab10d2745f599b7169178ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2989111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8a9810a211ebfde38c90dee4d98d754313fe38f54e661363ac0fe34d4831dda`

```dockerfile
```

-	Layers:
	-	`sha256:bef13d45e3ddfd22f3337a796ae159b53a972132c5b63be4a7fe23b36d83f8e2`  
		Last Modified: Tue, 12 Nov 2024 16:05:31 GMT  
		Size: 3.0 MB (2973228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:177f0c391e14922c9b7ef31b6218c5499bcda996876d5a7e4215fd535aceae20`  
		Last Modified: Tue, 12 Nov 2024 16:05:31 GMT  
		Size: 15.9 KB (15883 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.9.4` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:e623da3d1a29b06636f1206d6d42169e36eb5c6cad1ec0f391675bfd782b383e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.0 MB (66954349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb1173e891b9fd8aa6ce77f3128ad2931d48d8a3a79746513cd9a5d11ecc735b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1733097600'
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:8861e715dd4ae7d0bd8da39ea24d5c695bc09f0f4e43ca5221686621a10cd31b`  
		Last Modified: Tue, 03 Dec 2024 01:30:38 GMT  
		Size: 28.7 MB (28744923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da8b91290b61b9dbf0c1ca830cb74b33b50374f57fb454328be3492d32d016d`  
		Last Modified: Tue, 03 Dec 2024 05:42:34 GMT  
		Size: 5.0 MB (5003514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:452c81186300372e9f2eca9be97efad26e64cf0d660842c0e36d1f5d342ce131`  
		Last Modified: Tue, 03 Dec 2024 05:42:56 GMT  
		Size: 33.2 MB (33181523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74ac105c95db5553f4df553fd1f74d9455713a67d3bd804f72eeb604e024427a`  
		Last Modified: Tue, 03 Dec 2024 05:42:54 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f76ba8cb1f6cfe8a94c4ebc35705dec02b7cdcf3eaaa2b90b3a2de447a3cd6d7`  
		Last Modified: Tue, 03 Dec 2024 05:42:55 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a5ae52db475159d47e19db5a9dd5f39b6dff1c89c8931e57d417bdf36ad93bd`  
		Last Modified: Tue, 03 Dec 2024 05:42:55 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9.4` - unknown; unknown

```console
$ docker pull chronograf@sha256:ae8f1a9ceca72594c276c95dc291db9a3f626da22bd8c1dd88097bde470f2178
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2985236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d4bba172b224aa4f78f5213c14503b5c439aeaaf8365589314cfe047c1a7073`

```dockerfile
```

-	Layers:
	-	`sha256:9075258b6e710aa70c635aa3cf7504574feaf59b990e52ed1ae7934c8d143357`  
		Last Modified: Tue, 03 Dec 2024 05:42:55 GMT  
		Size: 3.0 MB (2969331 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0387a095cbc0862b0ab4c85e0eaca43c284dc4086b27983c2bfca290f73ecd8`  
		Last Modified: Tue, 03 Dec 2024 05:42:54 GMT  
		Size: 15.9 KB (15905 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.9.4-alpine`

```console
$ docker pull chronograf@sha256:b52ddf6c80429a91e462840afcb013b449c5fa7b4b356c92a83490e61debe3c6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.9.4-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:e0b078ddef48edabb3edd67587d73dce0886f1676d777da47062ab1eed88b0da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23611520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23c5bb53ba7aca946cba46980d5ab416af7a303ae1e8c442f2ddfdd0486a3297`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["/bin/sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a938a04d3b903456f3b0c899a1ee719f0fbe0c20572ce8f8a333cbd7204c9424`  
		Last Modified: Tue, 12 Nov 2024 02:38:03 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e403debb40518414e6b358a892a18b3e5f0f7e54081cfeb9b07c2b3101c971a6`  
		Last Modified: Tue, 12 Nov 2024 02:38:03 GMT  
		Size: 290.9 KB (290888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fac7ca426c5927695eb459153d6e03440a125f298ee6e62fc6919e2107e3567b`  
		Last Modified: Tue, 12 Nov 2024 02:38:03 GMT  
		Size: 19.7 MB (19672077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81b5a34d409580ae00a43acde566afb4380ddaf799697c813b6950eb6182c8e3`  
		Last Modified: Tue, 12 Nov 2024 02:38:03 GMT  
		Size: 12.2 KB (12238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eed6f91e2c5f917da15268635d210a1b9b6578179b3c6e3ca8ddf34bfe965eb`  
		Last Modified: Tue, 12 Nov 2024 02:38:04 GMT  
		Size: 11.9 KB (11897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8e9b4f4321537230681e57bb52a6ee546109b0a5ce852c867370658982bab4a`  
		Last Modified: Tue, 12 Nov 2024 02:38:04 GMT  
		Size: 237.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9.4-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:e401a0ae1338217c8774af1a7e7659865b503b32642d6b625261d45b377ad8b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.4 KB (250371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf3f1efc9c7e0a00983a84864956c0978fe19267c7224a63934dad2143b6116b`

```dockerfile
```

-	Layers:
	-	`sha256:b6b58d80490c4f66b398d6fe9770891de0d7a7dc51a5f8f529ef457e3b7c94f6`  
		Last Modified: Tue, 12 Nov 2024 02:38:03 GMT  
		Size: 233.5 KB (233462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9fe607b78ca533bf4dab527c8ab91e259f9b0e65f7abef6ead17fae5eb09ef2`  
		Last Modified: Tue, 12 Nov 2024 02:38:03 GMT  
		Size: 16.9 KB (16909 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:alpine`

```console
$ docker pull chronograf@sha256:e917c05d49569ffc91363b69db1139b3aec3ea352d7e4ab116ac73b5276c1e63
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:9177fbf8d1abc0941d457afc9b0e50767dab53c0fa38968d0935948927429e18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31808028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09dbf6891fc635a202a911272984b230346ed88f7ed61e7c5b4e6699d84faef9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["/bin/sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
RUN apk add --no-cache ca-certificates su-exec &&     update-ca-certificates # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.10.5
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S chronograf &&     adduser -S chronograf -G chronograf &&     mkdir -m 0750 -p /var/lib/chronograf &&     chown chronograf:chronograf /var/lib/chronograf # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2d999415b039365cadf590cb0dee4382b11889c724dd0eab32e010a66c2dda7`  
		Last Modified: Tue, 12 Nov 2024 02:38:06 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd85d2cc53952cb93e416bed6638ae8631ac933e78edf15edc8f453889c78a4b`  
		Last Modified: Tue, 12 Nov 2024 02:38:09 GMT  
		Size: 292.6 KB (292626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09c8ac47ff12105d7e2e63bdfecfe44bad8e9ed2abbb6bf69e824e6185e38c30`  
		Last Modified: Tue, 12 Nov 2024 02:38:09 GMT  
		Size: 27.9 MB (27866799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11e56c6035356fa99cb81386116d4e7f9647b9d607a8d8bf3c7bad00f71e5ae4`  
		Last Modified: Tue, 12 Nov 2024 02:38:09 GMT  
		Size: 12.2 KB (12234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:404105c04126e648e925115b31e8503e9be79bff0ac07d22b960fce01cc68627`  
		Last Modified: Tue, 12 Nov 2024 02:38:09 GMT  
		Size: 11.9 KB (11892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a2d0f282dc22ee43b73a0bfff8802169fb0b6a1285ee756c538a46c2ffc4303`  
		Last Modified: Tue, 12 Nov 2024 02:38:09 GMT  
		Size: 293.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:fcf8a567d3540090f865ac052c59bda542cc0aebd2c1ad4413eadd03d956c0d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.8 KB (257758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe6ab8b16a87c767b2f89aa09b99f84a49a0f574642aff41a53d43e44085627d`

```dockerfile
```

-	Layers:
	-	`sha256:608de47fe583d55de96c34e4f648a275957c4723931f32f5bf45243c183b05fb`  
		Last Modified: Tue, 12 Nov 2024 02:38:09 GMT  
		Size: 239.9 KB (239903 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6cf620aebcdf5b9e70ca057c32bcd31da203ea2fc4f7048080488c8522073c0c`  
		Last Modified: Tue, 12 Nov 2024 02:38:09 GMT  
		Size: 17.9 KB (17855 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:latest`

```console
$ docker pull chronograf@sha256:f6877613a1f76be6870685199e8080872c7256691affd70b0464cd2cf5bdc886
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
$ docker pull chronograf@sha256:55179cf3247aed84a08e6880b420d6b0d7d6c6e1f681cea25cd72ba48bdc0ae6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.2 MB (83154481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72b958df0fda7d82ce567ce17ab6ee07dcc5dbefe414410ce84ed2fd2c5fac70`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.10.5
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:bc0965b23a04fe7f2d9fb20f597008fcf89891de1c705ffc1c80483a1f098e4f`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 28.2 MB (28231580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16d1b25159cefd879024a50ac2a21f071888ee20994d1d560b1ed646bad30676`  
		Last Modified: Tue, 03 Dec 2024 02:29:26 GMT  
		Size: 7.7 MB (7680870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:504c8e1c66df44af38ba4711698f5fd119bd1d3c0a5d3cbbad222b6de6be76db`  
		Last Modified: Tue, 03 Dec 2024 02:29:26 GMT  
		Size: 47.2 MB (47217567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:838382be2ab64d8e09274691b82074f7619d8f270200fdeb820adb86bb0b2526`  
		Last Modified: Tue, 03 Dec 2024 02:29:26 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8597baf10c7f4991bb67c12ecd1064563d82773d44fa11fcb39fd1b11619e744`  
		Last Modified: Tue, 03 Dec 2024 02:29:26 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4e643f9b16da6d1d3b681b9d7db20df09ec9518cb56018c8f4b79af604725a3`  
		Last Modified: Tue, 03 Dec 2024 02:29:26 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:5720a12825375d7b7a0c1e253129b817d15fc760b5d1a434e73580621afbb3f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2721657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f55bf58b616a89619e2ca47656f498e76f513ab42fa925ea7ce02a488613b86`

```dockerfile
```

-	Layers:
	-	`sha256:f86610197bd4dd56307695e593f78f560f42c259a4481365558d72ef23ac213c`  
		Last Modified: Tue, 03 Dec 2024 02:29:26 GMT  
		Size: 2.7 MB (2705529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90853a1cf3a79efb76a02ecac0aabab26757acfc1ce2e9dea710f795ea378fe7`  
		Last Modified: Tue, 03 Dec 2024 02:29:26 GMT  
		Size: 16.1 KB (16128 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:latest` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:45f678c553711d2db70d58535b9794b3ad28d4d84f59d79a55f54f272827789b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75517507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:902c66527b2d96a1b1c3a0c88cbe54876f2dbd2a511a4c5fcb504a5a7838819d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["bash"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.10.5
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:ddd3c6488ea8b62db6811ba136fe14cba70219532910e67a91ed3388ec9f5757`  
		Last Modified: Tue, 12 Nov 2024 00:56:42 GMT  
		Size: 24.7 MB (24718909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6550685acd063dc6cce640c6f10c1dfac73cc458f5b8b19ec449579a08ab1401`  
		Last Modified: Tue, 12 Nov 2024 16:06:26 GMT  
		Size: 6.5 MB (6497842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb4d9638c811aa475e3ef3dd738ebb9839a72c09623ca60283c170c2babda7f6`  
		Last Modified: Tue, 12 Nov 2024 16:06:27 GMT  
		Size: 44.3 MB (44276286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:009a1e4b1ee7537b61421076ee24fd717c335f249c42420356c0539a1f6899b9`  
		Last Modified: Tue, 12 Nov 2024 16:06:25 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f869afcceefe33812d97f686e429f4d846795d1cd930495accf77f409f2506`  
		Last Modified: Tue, 12 Nov 2024 16:06:26 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf3c728782b2eeb8dd6001ebe7610861c011ebe762fcafbd576160449ed7bcb0`  
		Last Modified: Tue, 12 Nov 2024 16:06:26 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:b310981b0390adbddba27b5ffa275d03002a50389474dc02ab36dd4e8c5b9ebf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2725282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:621bb400573b68da87ad02e9d81f7ae8827c3ae22bd31fdb1d8e42dd93d4bd88`

```dockerfile
```

-	Layers:
	-	`sha256:a7b6c982a3a1c70e9c895470939fb5317eb615837e1c7b10cdac4960efaf1f79`  
		Last Modified: Tue, 12 Nov 2024 16:06:26 GMT  
		Size: 2.7 MB (2709073 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6bda2b8c1e48a2737a6f3b881aea6e27ed53014051c50ff50e1613800ad657f8`  
		Last Modified: Tue, 12 Nov 2024 16:06:25 GMT  
		Size: 16.2 KB (16209 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:latest` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:e7e6e8bcd037e4e3ef78dacf184dfd0607468688afcf34385ecf6fd6a43c688d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.5 MB (80513339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65251b89dd6b695070376aecd12bca6d93d4e0c50c538c14ead4ef1b8ad206e6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1733097600'
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.10.5
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:bb3f2b52e6af242cee1bc6c19ce79e05544f8a1d13f5a6c1e828d98d2dbdc94e`  
		Last Modified: Tue, 03 Dec 2024 01:30:11 GMT  
		Size: 28.1 MB (28058810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4b37923b73842e71b50c0097b23bdbf8c1fd5737de2267f0155b551b4a35e04`  
		Last Modified: Tue, 03 Dec 2024 05:43:25 GMT  
		Size: 7.5 MB (7459550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46cca2e9b8da36020418d166d65e08204386ea6f0f9c8322e4bd8326297bf576`  
		Last Modified: Tue, 03 Dec 2024 05:43:26 GMT  
		Size: 45.0 MB (44970512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af126f9679492862794ec3faa0aa3a04dc474c3487ed61d6e3362db8da417d84`  
		Last Modified: Tue, 03 Dec 2024 05:43:24 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e77b78079d47e9a8f9ddfb5a8c846820b91f9661f995c92a8e852ba1d225538`  
		Last Modified: Tue, 03 Dec 2024 05:43:24 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:811ed1b8177864765392b433bcdaadb9a7d967c62836d60595ad00bec37e4ba6`  
		Last Modified: Tue, 03 Dec 2024 05:43:25 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:38606c6e184fd9a185d7dc62063caf17e7fb05f859ff7cd6d02af14ab3413586
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2722036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:376b2d0b0fea4af460bac0228148298741be2212268e3bddd98b7980c0b1c4b1`

```dockerfile
```

-	Layers:
	-	`sha256:fa9dec0ce88733aebf94edfe9b94a5a4a2658b69f26d434dcfd834896edd7588`  
		Last Modified: Tue, 03 Dec 2024 05:43:25 GMT  
		Size: 2.7 MB (2705801 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:940877f4eedacf098fda84d4925a189fb1243588d36c9d11468460a06aeb4e1e`  
		Last Modified: Tue, 03 Dec 2024 05:43:24 GMT  
		Size: 16.2 KB (16235 bytes)  
		MIME: application/vnd.in-toto+json
