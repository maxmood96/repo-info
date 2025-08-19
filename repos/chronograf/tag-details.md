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
$ docker pull chronograf@sha256:b496312dcbd5ed38a3f1b8019f4692d2286df3255f77c22a0749139f8c1b9f4a
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
$ docker pull chronograf@sha256:78f194a5d8af0c73ca58362cca0592948111066a607dc37e0efed338037c00c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.4 MB (85409598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7227e098d6fdf17602053f1bd639e4f7b287a3243db15ed6cc2d99c44c487f9b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
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
	-	`sha256:b1badc6e50664185acfaa0ca255d8076061c2a9d881cecaaad281ae11af000ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:36 GMT  
		Size: 28.2 MB (28230255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57aec7ed967710aa3b3c38f8e7c98bff4173fe4269ed328bf52c69764048e03a`  
		Last Modified: Tue, 19 Aug 2025 16:46:07 GMT  
		Size: 7.9 MB (7878510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:062fc0487b5a20bcce7da16873ef46d5817c66d9d26faaa0a97e2aeb8d8ab2fd`  
		Last Modified: Tue, 19 Aug 2025 16:46:15 GMT  
		Size: 49.3 MB (49276370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dae64cb64cda55f522eaf1fe4ce88abdc53ae785d49a1e4fa1b93060396f096`  
		Last Modified: Tue, 19 Aug 2025 16:46:07 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c31654218009837dc4e26a1c34054dc87208494176e02ec6d7fbe1c1c6a5c5b0`  
		Last Modified: Tue, 19 Aug 2025 16:46:08 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43e3d95a8276abff48229102090caae2a128c08eee17ac353c3ae20759d94382`  
		Last Modified: Tue, 19 Aug 2025 16:46:08 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:8f7ee4f6c203fd1cc6832be3f4960f8092f1b71a11dc4def5c56d5c7388c44cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2867907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:736d3ee42dbd8a5e31d825443acee05181a59de41097627f3742c0b3fa22d1fa`

```dockerfile
```

-	Layers:
	-	`sha256:738f58d2b5b9f06f6b9dcce1872dc43b347364a0ed829903ace6caef278cfe1b`  
		Last Modified: Tue, 19 Aug 2025 18:38:26 GMT  
		Size: 2.9 MB (2851779 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d113181e5d099d77cd193bd01905dab2ea210354d0c9ed81b8acd51f4d6e858`  
		Last Modified: Tue, 19 Aug 2025 18:38:27 GMT  
		Size: 16.1 KB (16128 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.10` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:5d4706b5ea3431b7a6d88f9a0e2c53c3c9de00e4867de1b85664f636675ba834
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76092724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1144f67aa0da33184a38ff78812da721e4318df5b0e6aef06a607a747cd273e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1754870400'
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
	-	`sha256:a8db185805c54c045d888f7030794ebee970355b2336287cac0a0e22638ffc98`  
		Last Modified: Tue, 12 Aug 2025 20:46:38 GMT  
		Size: 23.9 MB (23938929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6467ca1c42d384f418a149d76dc5dffecb06ee7bfd528370c217304ba45aa285`  
		Last Modified: Wed, 13 Aug 2025 00:19:33 GMT  
		Size: 6.5 MB (6507882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcde1791bf4a512698b9677a862e632cd904c5fe7d3cee3d3b2aa646ef39ff87`  
		Last Modified: Tue, 19 Aug 2025 16:45:16 GMT  
		Size: 45.6 MB (45621441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bb91915267956814c74aebb7affae5121addaa975b893c424f2789482bc6e9c`  
		Last Modified: Tue, 19 Aug 2025 16:45:12 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0eec03b6d74dd34f2b5434d4c06da89877670b1764b17758045801edf4d0029`  
		Last Modified: Tue, 19 Aug 2025 16:45:12 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44416c5e6e1125817c2bf8094b06422a46969077532be262773ff3d352309225`  
		Last Modified: Tue, 19 Aug 2025 16:45:12 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:a241ff49c55dc2ffca9c96b8b7165d4d16a6c875ad63c7d7b5167510d6d7ed05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2870283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1a2e6f8150a59143322702f7593648f341f96ddfa322b614ba13e9f2f3d4cf2`

```dockerfile
```

-	Layers:
	-	`sha256:1ccd882973abac33915102be65e694c85f036ad99ec8f02bbc09e9abe57fb889`  
		Last Modified: Tue, 19 Aug 2025 18:38:31 GMT  
		Size: 2.9 MB (2854076 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74931f1e4ddb721dd5d0a5fa1659791d0bbdb3f118eeb325615bfe5365a44233`  
		Last Modified: Tue, 19 Aug 2025 18:38:32 GMT  
		Size: 16.2 KB (16207 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.10` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:7ab5bc34d8381df765d9e5225aa7245b40146f2b9032fcb59d2eab658cb387b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.8 MB (82841556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f963ed5432e0f380dc79450a4d42adf2caf8946e145434d7dfe9b81ab0fd452`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
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
	-	`sha256:9a80f9a055240e1d5ffd4b99717e18b5b3e924369b9155fb0a951a7a94b2c61f`  
		Last Modified: Tue, 12 Aug 2025 22:08:02 GMT  
		Size: 28.1 MB (28082001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93c08badcdfd21351f06fb3f6f3100986ebded72d529323ebb60dcb10b0854d8`  
		Last Modified: Tue, 19 Aug 2025 17:04:15 GMT  
		Size: 7.7 MB (7671576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e74f295773a20c5d5f5c63be7643f2dca67e8ac9ec4312b3b1a5a8b0f8aa8ce9`  
		Last Modified: Tue, 19 Aug 2025 17:04:18 GMT  
		Size: 47.1 MB (47063502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c0c286a7a2c93b238d8df6da9007c81af02dfde9d802ef02c8e7cd50d0e8c1e`  
		Last Modified: Tue, 19 Aug 2025 17:04:14 GMT  
		Size: 12.3 KB (12251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09a89652c558e398d8ff709538a0fae99179a0d8ab2fff955b6a35ff22903528`  
		Last Modified: Tue, 19 Aug 2025 17:04:14 GMT  
		Size: 11.9 KB (11912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:852aa334798995fd535d739a7c0c01cd0164ccc76062286a3af068e924569d30`  
		Last Modified: Tue, 19 Aug 2025 17:04:14 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:fbb8df3edfa7da1d3cf1ae84e530fe2ec2f5c2025d6c517978f3cb8be329d726
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2868287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1601707b645f7ec55a77c78262c0e519000abb798cc1a9179aad3b5035d207a`

```dockerfile
```

-	Layers:
	-	`sha256:b0f155cca9bdbc8e9c71242f7915ab57b5e588d6675befc5af3328123ea7653c`  
		Last Modified: Tue, 19 Aug 2025 18:38:36 GMT  
		Size: 2.9 MB (2852052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e07ce71181601270438c4e693d6bff3eeb54d11919dd1f334a08ea813a82e56a`  
		Last Modified: Tue, 19 Aug 2025 18:38:37 GMT  
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
$ docker pull chronograf@sha256:b496312dcbd5ed38a3f1b8019f4692d2286df3255f77c22a0749139f8c1b9f4a
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
$ docker pull chronograf@sha256:78f194a5d8af0c73ca58362cca0592948111066a607dc37e0efed338037c00c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.4 MB (85409598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7227e098d6fdf17602053f1bd639e4f7b287a3243db15ed6cc2d99c44c487f9b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
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
	-	`sha256:b1badc6e50664185acfaa0ca255d8076061c2a9d881cecaaad281ae11af000ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:36 GMT  
		Size: 28.2 MB (28230255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57aec7ed967710aa3b3c38f8e7c98bff4173fe4269ed328bf52c69764048e03a`  
		Last Modified: Tue, 19 Aug 2025 16:46:07 GMT  
		Size: 7.9 MB (7878510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:062fc0487b5a20bcce7da16873ef46d5817c66d9d26faaa0a97e2aeb8d8ab2fd`  
		Last Modified: Tue, 19 Aug 2025 16:46:15 GMT  
		Size: 49.3 MB (49276370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dae64cb64cda55f522eaf1fe4ce88abdc53ae785d49a1e4fa1b93060396f096`  
		Last Modified: Tue, 19 Aug 2025 16:46:07 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c31654218009837dc4e26a1c34054dc87208494176e02ec6d7fbe1c1c6a5c5b0`  
		Last Modified: Tue, 19 Aug 2025 16:46:08 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43e3d95a8276abff48229102090caae2a128c08eee17ac353c3ae20759d94382`  
		Last Modified: Tue, 19 Aug 2025 16:46:08 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10.8` - unknown; unknown

```console
$ docker pull chronograf@sha256:8f7ee4f6c203fd1cc6832be3f4960f8092f1b71a11dc4def5c56d5c7388c44cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2867907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:736d3ee42dbd8a5e31d825443acee05181a59de41097627f3742c0b3fa22d1fa`

```dockerfile
```

-	Layers:
	-	`sha256:738f58d2b5b9f06f6b9dcce1872dc43b347364a0ed829903ace6caef278cfe1b`  
		Last Modified: Tue, 19 Aug 2025 18:38:26 GMT  
		Size: 2.9 MB (2851779 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d113181e5d099d77cd193bd01905dab2ea210354d0c9ed81b8acd51f4d6e858`  
		Last Modified: Tue, 19 Aug 2025 18:38:27 GMT  
		Size: 16.1 KB (16128 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.10.8` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:5d4706b5ea3431b7a6d88f9a0e2c53c3c9de00e4867de1b85664f636675ba834
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76092724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1144f67aa0da33184a38ff78812da721e4318df5b0e6aef06a607a747cd273e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1754870400'
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
	-	`sha256:a8db185805c54c045d888f7030794ebee970355b2336287cac0a0e22638ffc98`  
		Last Modified: Tue, 12 Aug 2025 20:46:38 GMT  
		Size: 23.9 MB (23938929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6467ca1c42d384f418a149d76dc5dffecb06ee7bfd528370c217304ba45aa285`  
		Last Modified: Wed, 13 Aug 2025 00:19:33 GMT  
		Size: 6.5 MB (6507882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcde1791bf4a512698b9677a862e632cd904c5fe7d3cee3d3b2aa646ef39ff87`  
		Last Modified: Tue, 19 Aug 2025 16:45:16 GMT  
		Size: 45.6 MB (45621441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bb91915267956814c74aebb7affae5121addaa975b893c424f2789482bc6e9c`  
		Last Modified: Tue, 19 Aug 2025 16:45:12 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0eec03b6d74dd34f2b5434d4c06da89877670b1764b17758045801edf4d0029`  
		Last Modified: Tue, 19 Aug 2025 16:45:12 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44416c5e6e1125817c2bf8094b06422a46969077532be262773ff3d352309225`  
		Last Modified: Tue, 19 Aug 2025 16:45:12 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10.8` - unknown; unknown

```console
$ docker pull chronograf@sha256:a241ff49c55dc2ffca9c96b8b7165d4d16a6c875ad63c7d7b5167510d6d7ed05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2870283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1a2e6f8150a59143322702f7593648f341f96ddfa322b614ba13e9f2f3d4cf2`

```dockerfile
```

-	Layers:
	-	`sha256:1ccd882973abac33915102be65e694c85f036ad99ec8f02bbc09e9abe57fb889`  
		Last Modified: Tue, 19 Aug 2025 18:38:31 GMT  
		Size: 2.9 MB (2854076 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74931f1e4ddb721dd5d0a5fa1659791d0bbdb3f118eeb325615bfe5365a44233`  
		Last Modified: Tue, 19 Aug 2025 18:38:32 GMT  
		Size: 16.2 KB (16207 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.10.8` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:7ab5bc34d8381df765d9e5225aa7245b40146f2b9032fcb59d2eab658cb387b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.8 MB (82841556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f963ed5432e0f380dc79450a4d42adf2caf8946e145434d7dfe9b81ab0fd452`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
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
	-	`sha256:9a80f9a055240e1d5ffd4b99717e18b5b3e924369b9155fb0a951a7a94b2c61f`  
		Last Modified: Tue, 12 Aug 2025 22:08:02 GMT  
		Size: 28.1 MB (28082001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93c08badcdfd21351f06fb3f6f3100986ebded72d529323ebb60dcb10b0854d8`  
		Last Modified: Tue, 19 Aug 2025 17:04:15 GMT  
		Size: 7.7 MB (7671576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e74f295773a20c5d5f5c63be7643f2dca67e8ac9ec4312b3b1a5a8b0f8aa8ce9`  
		Last Modified: Tue, 19 Aug 2025 17:04:18 GMT  
		Size: 47.1 MB (47063502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c0c286a7a2c93b238d8df6da9007c81af02dfde9d802ef02c8e7cd50d0e8c1e`  
		Last Modified: Tue, 19 Aug 2025 17:04:14 GMT  
		Size: 12.3 KB (12251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09a89652c558e398d8ff709538a0fae99179a0d8ab2fff955b6a35ff22903528`  
		Last Modified: Tue, 19 Aug 2025 17:04:14 GMT  
		Size: 11.9 KB (11912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:852aa334798995fd535d739a7c0c01cd0164ccc76062286a3af068e924569d30`  
		Last Modified: Tue, 19 Aug 2025 17:04:14 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10.8` - unknown; unknown

```console
$ docker pull chronograf@sha256:fbb8df3edfa7da1d3cf1ae84e530fe2ec2f5c2025d6c517978f3cb8be329d726
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2868287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1601707b645f7ec55a77c78262c0e519000abb798cc1a9179aad3b5035d207a`

```dockerfile
```

-	Layers:
	-	`sha256:b0f155cca9bdbc8e9c71242f7915ab57b5e588d6675befc5af3328123ea7653c`  
		Last Modified: Tue, 19 Aug 2025 18:38:36 GMT  
		Size: 2.9 MB (2852052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e07ce71181601270438c4e693d6bff3eeb54d11919dd1f334a08ea813a82e56a`  
		Last Modified: Tue, 19 Aug 2025 18:38:37 GMT  
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
$ docker pull chronograf@sha256:1b0a5d63b1e163bb5ae5b42bd9f5e73f84fe7f7e81ca45674ee5aeff70b36ddc
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
$ docker pull chronograf@sha256:6bc202b581d2dd8ccbbd8844e51c29029611229a817626b114cfc6a7e162af34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.2 MB (69229574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e3797158d25229129a49f0d176af6f6c9bc4e93dbcdc69b21350e01e8f19414`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 16 Apr 2025 11:55:02 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1754870400'
# Wed, 16 Apr 2025 11:55:02 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Wed, 16 Apr 2025 11:55:02 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
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
	-	`sha256:3e41ca17193bcd7630e4dd210602930b1f94464bdd59680bbf6654206f7707b8`  
		Last Modified: Tue, 12 Aug 2025 20:44:40 GMT  
		Size: 30.3 MB (30256118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d503d9fc7da0af5e9a2de10b4703d45a22c325cf9f0f5eba384608d5e6b69971`  
		Last Modified: Tue, 12 Aug 2025 21:18:36 GMT  
		Size: 4.2 MB (4209293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30cb867dad2e80c5da59b19d6096af3fce7ccf5e4efa76ab29478fc17329cb02`  
		Last Modified: Tue, 12 Aug 2025 21:18:38 GMT  
		Size: 34.7 MB (34739781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8231b5464fa2d2842c0645b5ae3008702e597b51f09087de37fb0bbac12b6b95`  
		Last Modified: Tue, 12 Aug 2025 21:18:34 GMT  
		Size: 12.2 KB (12242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e3fadc12b6d6ed9fe86862bd4a6f581fb20ae9bd793ffb6dce23e328658d30c`  
		Last Modified: Tue, 12 Aug 2025 21:18:35 GMT  
		Size: 11.9 KB (11900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a78b4b84fd0b337439f8e4477127e97e9d5b2e491e42063d55661c1dbcb4021c`  
		Last Modified: Tue, 12 Aug 2025 21:18:34 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7` - unknown; unknown

```console
$ docker pull chronograf@sha256:a89b18a2e8a91881bc31ee85ea88a0f922d458333875ef4cd11f9097efd7a6e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3064650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c6cea727a9bfc42157897eff03487feda647e46162639a377a641bbd2557854`

```dockerfile
```

-	Layers:
	-	`sha256:764e18f8d85f05eb1bdf2a745d21c15065d6f400c55bc2504c9a9fe39edbced4`  
		Last Modified: Wed, 13 Aug 2025 00:38:25 GMT  
		Size: 3.0 MB (3048873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abd285ffed3d150d28f12cf24fc33483e36582fff666709a18a8d03f207516ef`  
		Last Modified: Wed, 13 Aug 2025 00:38:27 GMT  
		Size: 15.8 KB (15777 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.7` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:1d65af4c37d292c904a5ca458a7f8b9a45c3f1f408712aefc062df11360c05bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62179008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01e0d9b28e526376cd0d045a2f6a18518318d2be8f3002044d185f1a77a77f43`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 16 Apr 2025 11:55:02 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1754870400'
# Wed, 16 Apr 2025 11:55:02 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Wed, 16 Apr 2025 11:55:02 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
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
	-	`sha256:42c6883fd732cb484051b4fff6157db32a689c12264945da05c930608a6fe450`  
		Last Modified: Tue, 12 Aug 2025 20:47:00 GMT  
		Size: 25.5 MB (25544117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f490915f2a82a168f807a7af3c1bbff01bf2dd8215918790c7a76f3d3c505d04`  
		Last Modified: Wed, 13 Aug 2025 00:17:45 GMT  
		Size: 3.5 MB (3511662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:825c2c9827986da3ac1871b417ad365daabae6550167000b0d4f401398be8b6b`  
		Last Modified: Wed, 13 Aug 2025 00:17:49 GMT  
		Size: 33.1 MB (33098829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e787c899ede0f4eb4eae876c5a2816ab1a83611f0c89d23bb0a1c6a80f0c866`  
		Last Modified: Wed, 13 Aug 2025 00:17:43 GMT  
		Size: 12.3 KB (12251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:990d3949ef50aaf925412fbf694ef7f2d788b332a87537ccfe5cb82e18471ec7`  
		Last Modified: Wed, 13 Aug 2025 00:17:43 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fa16de71880aa18a7df1720ce15323ce27d10d935b3ad8bf127f950b6e2cce8`  
		Last Modified: Wed, 13 Aug 2025 00:17:43 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7` - unknown; unknown

```console
$ docker pull chronograf@sha256:5beee2201345a635886c74aec6a0bb4f5ab40ea671022a457f288d40d3bca205
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3066994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01001787bbeeceb701238af0fe80e927a543b6240205034917ff7cdb49536e68`

```dockerfile
```

-	Layers:
	-	`sha256:481baa36e9957e7c810c9352f530281d196308e48fe568a679643121617a466c`  
		Last Modified: Wed, 13 Aug 2025 03:38:28 GMT  
		Size: 3.1 MB (3051144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c89892ef138768ea693b0ca128040a318cae2b6ca5fbe355999f8446bf540575`  
		Last Modified: Wed, 13 Aug 2025 03:38:29 GMT  
		Size: 15.8 KB (15850 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.7` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:d09cf68c6a2adfae71fc3dce3e9cb8beab84700de7c1c7609eba438134fd6689
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66224883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51b58515e3bcd7621793f092c2b007853daa7ddc22e2602ef3cf37805e1c6cf7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 16 Apr 2025 11:55:02 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1754870400'
# Wed, 16 Apr 2025 11:55:02 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Wed, 16 Apr 2025 11:55:02 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
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
	-	`sha256:b99ef417bc3eb3946e7b3162f6c19dbca1039f3b4124deb116c3a0ab763e65ad`  
		Last Modified: Tue, 12 Aug 2025 22:33:30 GMT  
		Size: 28.8 MB (28750491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:353c4c80bc5a2a5890c2b20ab9c5c5ca2fae704eeec7a06c307ef1e16ec44dde`  
		Last Modified: Wed, 13 Aug 2025 06:58:53 GMT  
		Size: 4.2 MB (4210636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3af284caca940f5e6883d16d52b1f1980327a492c1479cf4cb4d5c54ca0156f`  
		Last Modified: Wed, 13 Aug 2025 06:58:55 GMT  
		Size: 33.2 MB (33239365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e32babd3106df8511c09b311f314cc73dda6e38c4b4b5effda39b0b7a2b53d9`  
		Last Modified: Wed, 13 Aug 2025 06:58:53 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:547fdcd8e52fda8c5de2e4ec6c0249ab1c12d776cdd69b6c6a953f8232ecafb7`  
		Last Modified: Wed, 13 Aug 2025 06:58:54 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d49affcc0c2408e55cabe335cfa4fad773b4a1f543c2e18d1eae79f6b234c153`  
		Last Modified: Wed, 13 Aug 2025 06:58:55 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7` - unknown; unknown

```console
$ docker pull chronograf@sha256:b3291287f70c59f49752a9e009852fb20d66faea2e65ec37cd8872b986141513
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3064992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:363cffbb9dd7e44cea9c64e2a7223d15616e59033addc7ae3381e58769a7df91`

```dockerfile
```

-	Layers:
	-	`sha256:a1a64bf0acc7466c28a15dc66e9913283eaeea461fdfdd8dca2743f5f6902e8e`  
		Last Modified: Wed, 13 Aug 2025 09:38:29 GMT  
		Size: 3.0 MB (3049122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfc781f3e2353c44b1675831baf79c1ae7e0233036be73724d2e9c13a9f04a94`  
		Last Modified: Wed, 13 Aug 2025 09:38:30 GMT  
		Size: 15.9 KB (15870 bytes)  
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
$ docker pull chronograf@sha256:1b0a5d63b1e163bb5ae5b42bd9f5e73f84fe7f7e81ca45674ee5aeff70b36ddc
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
$ docker pull chronograf@sha256:6bc202b581d2dd8ccbbd8844e51c29029611229a817626b114cfc6a7e162af34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.2 MB (69229574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e3797158d25229129a49f0d176af6f6c9bc4e93dbcdc69b21350e01e8f19414`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 16 Apr 2025 11:55:02 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1754870400'
# Wed, 16 Apr 2025 11:55:02 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Wed, 16 Apr 2025 11:55:02 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
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
	-	`sha256:3e41ca17193bcd7630e4dd210602930b1f94464bdd59680bbf6654206f7707b8`  
		Last Modified: Tue, 12 Aug 2025 20:44:40 GMT  
		Size: 30.3 MB (30256118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d503d9fc7da0af5e9a2de10b4703d45a22c325cf9f0f5eba384608d5e6b69971`  
		Last Modified: Tue, 12 Aug 2025 21:18:36 GMT  
		Size: 4.2 MB (4209293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30cb867dad2e80c5da59b19d6096af3fce7ccf5e4efa76ab29478fc17329cb02`  
		Last Modified: Tue, 12 Aug 2025 21:18:38 GMT  
		Size: 34.7 MB (34739781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8231b5464fa2d2842c0645b5ae3008702e597b51f09087de37fb0bbac12b6b95`  
		Last Modified: Tue, 12 Aug 2025 21:18:34 GMT  
		Size: 12.2 KB (12242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e3fadc12b6d6ed9fe86862bd4a6f581fb20ae9bd793ffb6dce23e328658d30c`  
		Last Modified: Tue, 12 Aug 2025 21:18:35 GMT  
		Size: 11.9 KB (11900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a78b4b84fd0b337439f8e4477127e97e9d5b2e491e42063d55661c1dbcb4021c`  
		Last Modified: Tue, 12 Aug 2025 21:18:34 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7.17` - unknown; unknown

```console
$ docker pull chronograf@sha256:a89b18a2e8a91881bc31ee85ea88a0f922d458333875ef4cd11f9097efd7a6e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3064650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c6cea727a9bfc42157897eff03487feda647e46162639a377a641bbd2557854`

```dockerfile
```

-	Layers:
	-	`sha256:764e18f8d85f05eb1bdf2a745d21c15065d6f400c55bc2504c9a9fe39edbced4`  
		Last Modified: Wed, 13 Aug 2025 00:38:25 GMT  
		Size: 3.0 MB (3048873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abd285ffed3d150d28f12cf24fc33483e36582fff666709a18a8d03f207516ef`  
		Last Modified: Wed, 13 Aug 2025 00:38:27 GMT  
		Size: 15.8 KB (15777 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.7.17` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:1d65af4c37d292c904a5ca458a7f8b9a45c3f1f408712aefc062df11360c05bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62179008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01e0d9b28e526376cd0d045a2f6a18518318d2be8f3002044d185f1a77a77f43`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 16 Apr 2025 11:55:02 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1754870400'
# Wed, 16 Apr 2025 11:55:02 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Wed, 16 Apr 2025 11:55:02 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
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
	-	`sha256:42c6883fd732cb484051b4fff6157db32a689c12264945da05c930608a6fe450`  
		Last Modified: Tue, 12 Aug 2025 20:47:00 GMT  
		Size: 25.5 MB (25544117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f490915f2a82a168f807a7af3c1bbff01bf2dd8215918790c7a76f3d3c505d04`  
		Last Modified: Wed, 13 Aug 2025 00:17:45 GMT  
		Size: 3.5 MB (3511662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:825c2c9827986da3ac1871b417ad365daabae6550167000b0d4f401398be8b6b`  
		Last Modified: Wed, 13 Aug 2025 00:17:49 GMT  
		Size: 33.1 MB (33098829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e787c899ede0f4eb4eae876c5a2816ab1a83611f0c89d23bb0a1c6a80f0c866`  
		Last Modified: Wed, 13 Aug 2025 00:17:43 GMT  
		Size: 12.3 KB (12251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:990d3949ef50aaf925412fbf694ef7f2d788b332a87537ccfe5cb82e18471ec7`  
		Last Modified: Wed, 13 Aug 2025 00:17:43 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fa16de71880aa18a7df1720ce15323ce27d10d935b3ad8bf127f950b6e2cce8`  
		Last Modified: Wed, 13 Aug 2025 00:17:43 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7.17` - unknown; unknown

```console
$ docker pull chronograf@sha256:5beee2201345a635886c74aec6a0bb4f5ab40ea671022a457f288d40d3bca205
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3066994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01001787bbeeceb701238af0fe80e927a543b6240205034917ff7cdb49536e68`

```dockerfile
```

-	Layers:
	-	`sha256:481baa36e9957e7c810c9352f530281d196308e48fe568a679643121617a466c`  
		Last Modified: Wed, 13 Aug 2025 03:38:28 GMT  
		Size: 3.1 MB (3051144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c89892ef138768ea693b0ca128040a318cae2b6ca5fbe355999f8446bf540575`  
		Last Modified: Wed, 13 Aug 2025 03:38:29 GMT  
		Size: 15.8 KB (15850 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.7.17` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:d09cf68c6a2adfae71fc3dce3e9cb8beab84700de7c1c7609eba438134fd6689
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66224883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51b58515e3bcd7621793f092c2b007853daa7ddc22e2602ef3cf37805e1c6cf7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 16 Apr 2025 11:55:02 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1754870400'
# Wed, 16 Apr 2025 11:55:02 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Wed, 16 Apr 2025 11:55:02 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
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
	-	`sha256:b99ef417bc3eb3946e7b3162f6c19dbca1039f3b4124deb116c3a0ab763e65ad`  
		Last Modified: Tue, 12 Aug 2025 22:33:30 GMT  
		Size: 28.8 MB (28750491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:353c4c80bc5a2a5890c2b20ab9c5c5ca2fae704eeec7a06c307ef1e16ec44dde`  
		Last Modified: Wed, 13 Aug 2025 06:58:53 GMT  
		Size: 4.2 MB (4210636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3af284caca940f5e6883d16d52b1f1980327a492c1479cf4cb4d5c54ca0156f`  
		Last Modified: Wed, 13 Aug 2025 06:58:55 GMT  
		Size: 33.2 MB (33239365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e32babd3106df8511c09b311f314cc73dda6e38c4b4b5effda39b0b7a2b53d9`  
		Last Modified: Wed, 13 Aug 2025 06:58:53 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:547fdcd8e52fda8c5de2e4ec6c0249ab1c12d776cdd69b6c6a953f8232ecafb7`  
		Last Modified: Wed, 13 Aug 2025 06:58:54 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d49affcc0c2408e55cabe335cfa4fad773b4a1f543c2e18d1eae79f6b234c153`  
		Last Modified: Wed, 13 Aug 2025 06:58:55 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7.17` - unknown; unknown

```console
$ docker pull chronograf@sha256:b3291287f70c59f49752a9e009852fb20d66faea2e65ec37cd8872b986141513
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3064992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:363cffbb9dd7e44cea9c64e2a7223d15616e59033addc7ae3381e58769a7df91`

```dockerfile
```

-	Layers:
	-	`sha256:a1a64bf0acc7466c28a15dc66e9913283eaeea461fdfdd8dca2743f5f6902e8e`  
		Last Modified: Wed, 13 Aug 2025 09:38:29 GMT  
		Size: 3.0 MB (3049122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfc781f3e2353c44b1675831baf79c1ae7e0233036be73724d2e9c13a9f04a94`  
		Last Modified: Wed, 13 Aug 2025 09:38:30 GMT  
		Size: 15.9 KB (15870 bytes)  
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
$ docker pull chronograf@sha256:5e543d8daf9e71f4a380bcec7e334ee7b956956fd509e291215add105482a7a4
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
$ docker pull chronograf@sha256:e595032ca7a7e72ce587a5c3afaff653b2aab0a595c84c6c4f5c8305881e2f22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69870660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b19a1f05025bd11ab6eb7e1b70d2131f2fd99f03338e4971b09e414d13f18beb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 16 Apr 2025 11:55:02 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1754870400'
# Wed, 16 Apr 2025 11:55:02 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Wed, 16 Apr 2025 11:55:02 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
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
	-	`sha256:3e41ca17193bcd7630e4dd210602930b1f94464bdd59680bbf6654206f7707b8`  
		Last Modified: Tue, 12 Aug 2025 20:44:40 GMT  
		Size: 30.3 MB (30256118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:013e3bf3ae9031d2b9d5fcf1768338af208f6c2ed28ca318cb6a9ba68182e4b9`  
		Last Modified: Wed, 13 Aug 2025 00:23:17 GMT  
		Size: 5.2 MB (5225946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e042d5fb3411c211cb2fd8b4c71c7996f4b9ad63583a78b10c15ff6e226737f`  
		Last Modified: Wed, 13 Aug 2025 00:23:22 GMT  
		Size: 34.4 MB (34364214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dff2eec9c97be4e9fe0994de789b6a92e265be94c5f79ab9ab2f14358e07488`  
		Last Modified: Tue, 12 Aug 2025 22:06:18 GMT  
		Size: 12.2 KB (12241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e98a3e09d411b1718bc82c054e831e84752521e53791ab70b7b9dee42da01e5`  
		Last Modified: Tue, 12 Aug 2025 22:06:18 GMT  
		Size: 11.9 KB (11901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2ff85da906dae290ffaba8a5a50cafae0c86c3e0dd001a882d2cad87920595d`  
		Last Modified: Tue, 12 Aug 2025 22:06:16 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8` - unknown; unknown

```console
$ docker pull chronograf@sha256:b0121e5a14098ee87f1575f640653db77026279aea8d2990840be21ab873547c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3120328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c18bc27bd52af28bfdf836c585fb05e68178d1787d040ba11ace421f6cc9c3e`

```dockerfile
```

-	Layers:
	-	`sha256:d58aee012475b5fc47c4cfa0a9ac091470432a55239a9a5b7d51e30763bec1b1`  
		Last Modified: Wed, 13 Aug 2025 00:38:32 GMT  
		Size: 3.1 MB (3104511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2bccac58b32f7a51e1286ee10e3f8fa58b7784f211122e5c11985cec723fb0b1`  
		Last Modified: Wed, 13 Aug 2025 00:38:33 GMT  
		Size: 15.8 KB (15817 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.8` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:e26ef285f76a5819db9a853f98a91dff88d8adb9ded2d7cc6f3c7b983857450e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.6 MB (62595228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:515f6011e3cf4f256426584179578c62ed3682e856d0e7b0f3d781427de18dab`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 16 Apr 2025 11:55:02 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1754870400'
# Wed, 16 Apr 2025 11:55:02 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Wed, 16 Apr 2025 11:55:02 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
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
	-	`sha256:42c6883fd732cb484051b4fff6157db32a689c12264945da05c930608a6fe450`  
		Last Modified: Tue, 12 Aug 2025 20:47:00 GMT  
		Size: 25.5 MB (25544117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04f99498d847e9f3cd5269623df3574a733aa9ef5a52b928a12d356921ac1224`  
		Last Modified: Wed, 13 Aug 2025 00:18:28 GMT  
		Size: 4.5 MB (4491819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a04a48877bfee825800028e207a3f98024d8c5e7653d4b9e05454787e0a989e`  
		Last Modified: Wed, 13 Aug 2025 00:18:29 GMT  
		Size: 32.5 MB (32534893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2994bbd9f6eb41c5cffd83f1a1b02284e60dac1b43c692a990c7b7d0842dbc4a`  
		Last Modified: Wed, 13 Aug 2025 00:18:27 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bfdcd4322c33a2afca3073a13a8eeca590a06ec1444f7c4f9cde8624f23c6aa`  
		Last Modified: Wed, 13 Aug 2025 00:18:29 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec25587a0d46c0ece0966d6aacc6c815d0248d089302eec495daf595cfa29c3c`  
		Last Modified: Wed, 13 Aug 2025 00:18:29 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8` - unknown; unknown

```console
$ docker pull chronograf@sha256:a7a542bf50b8ae46fdd0c98371f164c2b468cd4f9acdd32712d3c56e68fbeaaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3122672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78de9d14adac0f91de0bb9c53e5347932ebd68589935fbc2846f356ce538ac3e`

```dockerfile
```

-	Layers:
	-	`sha256:8948fcda8f8323bdb573069f109bf53383b00d888a68bbc02a702d69ce309ab5`  
		Last Modified: Wed, 13 Aug 2025 03:38:35 GMT  
		Size: 3.1 MB (3106782 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d586c1b17363e73e822248cf1abc54c56801b95e6b0da9c570ba780529bb8ccf`  
		Last Modified: Wed, 13 Aug 2025 03:38:36 GMT  
		Size: 15.9 KB (15890 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.8` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:bd95136c140d325e6cdeeded68737b8c24e480f45cf6e7157bb8a3e5d0c6c6f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.4 MB (66413756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44b3cdf2f8e2a21dc350d5fa39e2149ee29622e86c28b1ed8d50b7defb0fe406`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 16 Apr 2025 11:55:02 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1754870400'
# Wed, 16 Apr 2025 11:55:02 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Wed, 16 Apr 2025 11:55:02 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
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
	-	`sha256:b99ef417bc3eb3946e7b3162f6c19dbca1039f3b4124deb116c3a0ab763e65ad`  
		Last Modified: Tue, 12 Aug 2025 22:33:30 GMT  
		Size: 28.8 MB (28750491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb2bf7bf292427b2ba72209f2594d098eecd42f7f9360bfb670e1b31c92b8330`  
		Last Modified: Wed, 13 Aug 2025 06:59:29 GMT  
		Size: 5.2 MB (5209361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:186f0168bb19c9aa00a7d52b33c1cf56be03609f157248538c540d9d395f5e04`  
		Last Modified: Wed, 13 Aug 2025 06:59:40 GMT  
		Size: 32.4 MB (32429502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16a3db29f7ad659b158bdb01ec35ea41d48036ad079c8b64e10d796cc2896b61`  
		Last Modified: Wed, 13 Aug 2025 06:59:29 GMT  
		Size: 12.3 KB (12251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd2b6fcf996bbf24e1bbeec62c2afd5e033b4d0f1944e60b4f959c5373ed9a82`  
		Last Modified: Wed, 13 Aug 2025 06:59:29 GMT  
		Size: 11.9 KB (11911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede42836bdc6e2a23cbb645b9862b9c1a99c8f1d52e628afa8284f6915f17beb`  
		Last Modified: Wed, 13 Aug 2025 06:59:29 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8` - unknown; unknown

```console
$ docker pull chronograf@sha256:df7ea41594c2a9a4221b3d1a18a747a911c8ad37dbb2906461af15c1a345a02d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3120672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccd7832e68e558035672ae4348621d02ec4bdc93bea7ff6d294674e79a44479a`

```dockerfile
```

-	Layers:
	-	`sha256:3d09df83d05cbae0468ac8f7e190ffbf90c97c3f24e99d7088aafef1c0a1323a`  
		Last Modified: Wed, 13 Aug 2025 09:38:36 GMT  
		Size: 3.1 MB (3104760 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:edeaf361d02d2b1298efa2d7b8d132d00e4128e62aaced2481956987cf45df72`  
		Last Modified: Wed, 13 Aug 2025 09:38:36 GMT  
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
$ docker pull chronograf@sha256:5e543d8daf9e71f4a380bcec7e334ee7b956956fd509e291215add105482a7a4
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
$ docker pull chronograf@sha256:e595032ca7a7e72ce587a5c3afaff653b2aab0a595c84c6c4f5c8305881e2f22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69870660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b19a1f05025bd11ab6eb7e1b70d2131f2fd99f03338e4971b09e414d13f18beb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 16 Apr 2025 11:55:02 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1754870400'
# Wed, 16 Apr 2025 11:55:02 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Wed, 16 Apr 2025 11:55:02 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
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
	-	`sha256:3e41ca17193bcd7630e4dd210602930b1f94464bdd59680bbf6654206f7707b8`  
		Last Modified: Tue, 12 Aug 2025 20:44:40 GMT  
		Size: 30.3 MB (30256118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:013e3bf3ae9031d2b9d5fcf1768338af208f6c2ed28ca318cb6a9ba68182e4b9`  
		Last Modified: Wed, 13 Aug 2025 00:23:17 GMT  
		Size: 5.2 MB (5225946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e042d5fb3411c211cb2fd8b4c71c7996f4b9ad63583a78b10c15ff6e226737f`  
		Last Modified: Wed, 13 Aug 2025 00:23:22 GMT  
		Size: 34.4 MB (34364214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dff2eec9c97be4e9fe0994de789b6a92e265be94c5f79ab9ab2f14358e07488`  
		Last Modified: Tue, 12 Aug 2025 22:06:18 GMT  
		Size: 12.2 KB (12241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e98a3e09d411b1718bc82c054e831e84752521e53791ab70b7b9dee42da01e5`  
		Last Modified: Tue, 12 Aug 2025 22:06:18 GMT  
		Size: 11.9 KB (11901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2ff85da906dae290ffaba8a5a50cafae0c86c3e0dd001a882d2cad87920595d`  
		Last Modified: Tue, 12 Aug 2025 22:06:16 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:b0121e5a14098ee87f1575f640653db77026279aea8d2990840be21ab873547c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3120328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c18bc27bd52af28bfdf836c585fb05e68178d1787d040ba11ace421f6cc9c3e`

```dockerfile
```

-	Layers:
	-	`sha256:d58aee012475b5fc47c4cfa0a9ac091470432a55239a9a5b7d51e30763bec1b1`  
		Last Modified: Wed, 13 Aug 2025 00:38:32 GMT  
		Size: 3.1 MB (3104511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2bccac58b32f7a51e1286ee10e3f8fa58b7784f211122e5c11985cec723fb0b1`  
		Last Modified: Wed, 13 Aug 2025 00:38:33 GMT  
		Size: 15.8 KB (15817 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.8.10` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:e26ef285f76a5819db9a853f98a91dff88d8adb9ded2d7cc6f3c7b983857450e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.6 MB (62595228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:515f6011e3cf4f256426584179578c62ed3682e856d0e7b0f3d781427de18dab`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 16 Apr 2025 11:55:02 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1754870400'
# Wed, 16 Apr 2025 11:55:02 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Wed, 16 Apr 2025 11:55:02 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
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
	-	`sha256:42c6883fd732cb484051b4fff6157db32a689c12264945da05c930608a6fe450`  
		Last Modified: Tue, 12 Aug 2025 20:47:00 GMT  
		Size: 25.5 MB (25544117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04f99498d847e9f3cd5269623df3574a733aa9ef5a52b928a12d356921ac1224`  
		Last Modified: Wed, 13 Aug 2025 00:18:28 GMT  
		Size: 4.5 MB (4491819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a04a48877bfee825800028e207a3f98024d8c5e7653d4b9e05454787e0a989e`  
		Last Modified: Wed, 13 Aug 2025 00:18:29 GMT  
		Size: 32.5 MB (32534893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2994bbd9f6eb41c5cffd83f1a1b02284e60dac1b43c692a990c7b7d0842dbc4a`  
		Last Modified: Wed, 13 Aug 2025 00:18:27 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bfdcd4322c33a2afca3073a13a8eeca590a06ec1444f7c4f9cde8624f23c6aa`  
		Last Modified: Wed, 13 Aug 2025 00:18:29 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec25587a0d46c0ece0966d6aacc6c815d0248d089302eec495daf595cfa29c3c`  
		Last Modified: Wed, 13 Aug 2025 00:18:29 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:a7a542bf50b8ae46fdd0c98371f164c2b468cd4f9acdd32712d3c56e68fbeaaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3122672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78de9d14adac0f91de0bb9c53e5347932ebd68589935fbc2846f356ce538ac3e`

```dockerfile
```

-	Layers:
	-	`sha256:8948fcda8f8323bdb573069f109bf53383b00d888a68bbc02a702d69ce309ab5`  
		Last Modified: Wed, 13 Aug 2025 03:38:35 GMT  
		Size: 3.1 MB (3106782 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d586c1b17363e73e822248cf1abc54c56801b95e6b0da9c570ba780529bb8ccf`  
		Last Modified: Wed, 13 Aug 2025 03:38:36 GMT  
		Size: 15.9 KB (15890 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.8.10` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:bd95136c140d325e6cdeeded68737b8c24e480f45cf6e7157bb8a3e5d0c6c6f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.4 MB (66413756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44b3cdf2f8e2a21dc350d5fa39e2149ee29622e86c28b1ed8d50b7defb0fe406`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 16 Apr 2025 11:55:02 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1754870400'
# Wed, 16 Apr 2025 11:55:02 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Wed, 16 Apr 2025 11:55:02 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
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
	-	`sha256:b99ef417bc3eb3946e7b3162f6c19dbca1039f3b4124deb116c3a0ab763e65ad`  
		Last Modified: Tue, 12 Aug 2025 22:33:30 GMT  
		Size: 28.8 MB (28750491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb2bf7bf292427b2ba72209f2594d098eecd42f7f9360bfb670e1b31c92b8330`  
		Last Modified: Wed, 13 Aug 2025 06:59:29 GMT  
		Size: 5.2 MB (5209361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:186f0168bb19c9aa00a7d52b33c1cf56be03609f157248538c540d9d395f5e04`  
		Last Modified: Wed, 13 Aug 2025 06:59:40 GMT  
		Size: 32.4 MB (32429502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16a3db29f7ad659b158bdb01ec35ea41d48036ad079c8b64e10d796cc2896b61`  
		Last Modified: Wed, 13 Aug 2025 06:59:29 GMT  
		Size: 12.3 KB (12251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd2b6fcf996bbf24e1bbeec62c2afd5e033b4d0f1944e60b4f959c5373ed9a82`  
		Last Modified: Wed, 13 Aug 2025 06:59:29 GMT  
		Size: 11.9 KB (11911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede42836bdc6e2a23cbb645b9862b9c1a99c8f1d52e628afa8284f6915f17beb`  
		Last Modified: Wed, 13 Aug 2025 06:59:29 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:df7ea41594c2a9a4221b3d1a18a747a911c8ad37dbb2906461af15c1a345a02d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3120672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccd7832e68e558035672ae4348621d02ec4bdc93bea7ff6d294674e79a44479a`

```dockerfile
```

-	Layers:
	-	`sha256:3d09df83d05cbae0468ac8f7e190ffbf90c97c3f24e99d7088aafef1c0a1323a`  
		Last Modified: Wed, 13 Aug 2025 09:38:36 GMT  
		Size: 3.1 MB (3104760 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:edeaf361d02d2b1298efa2d7b8d132d00e4128e62aaced2481956987cf45df72`  
		Last Modified: Wed, 13 Aug 2025 09:38:36 GMT  
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
$ docker pull chronograf@sha256:4f07612ac9189032160213db3d09dca438664adf0d7901f296ade037c24e7df4
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
$ docker pull chronograf@sha256:af3c63195f586442a8b214c6753d3cabcaa41badda9cc231b62db75275b98126
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.5 MB (70518240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ccfa4d2309ca03cce796f5549726c9d3dd8b1b7398977f882b277624e915019`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 16 Apr 2025 11:55:02 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1754870400'
# Wed, 16 Apr 2025 11:55:02 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Wed, 16 Apr 2025 11:55:02 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
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
	-	`sha256:3e41ca17193bcd7630e4dd210602930b1f94464bdd59680bbf6654206f7707b8`  
		Last Modified: Tue, 12 Aug 2025 20:44:40 GMT  
		Size: 30.3 MB (30256118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00de6d2c80c33c22628fce0ffc1cc6bd2ad0473189669537b4ae8cfbc2d02a80`  
		Last Modified: Tue, 12 Aug 2025 21:22:57 GMT  
		Size: 5.2 MB (5226005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22daa18bd4e741fe41f098bee490776da7a37a0701fc514170952b21673583c2`  
		Last Modified: Tue, 12 Aug 2025 21:22:59 GMT  
		Size: 35.0 MB (35011741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:226fe7d00a2614a02d80239454ff6f80363ea1b591dc7cb8a9aa6adc1fd1170e`  
		Last Modified: Tue, 12 Aug 2025 21:22:57 GMT  
		Size: 12.2 KB (12237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ac2636356f53cc0d7be6c0fb54d340386ee674d4c4726a3635921aeb084dc11`  
		Last Modified: Tue, 12 Aug 2025 21:22:57 GMT  
		Size: 11.9 KB (11900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77fb31bd2ff670c5348032166a1d06dcf6eb1d3572d38e8eb1245aa369b381e3`  
		Last Modified: Tue, 12 Aug 2025 21:22:57 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9` - unknown; unknown

```console
$ docker pull chronograf@sha256:19f83cd415657cf3d21e186f986654a7a4082ff32e0e2fce909c25cf60bbb8f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3125530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22ff884e7ef9e6c391c4ec87bde2c5a59ff643ee15d6f6d91e087455cca8dd20`

```dockerfile
```

-	Layers:
	-	`sha256:4ca934156d28d47bb0b393b355fa132a5595152ceb1d89e154ae19e16ffdaa5c`  
		Last Modified: Wed, 13 Aug 2025 00:38:40 GMT  
		Size: 3.1 MB (3109721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c103e6d0957244309f9fbc9e82070a49e3a6e3bdd872f36d552aa6e51c991604`  
		Last Modified: Wed, 13 Aug 2025 00:38:40 GMT  
		Size: 15.8 KB (15809 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.9` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:acd8fd00fa697674f035e1a3a208246964278b7e99fdaed114a2028a13eac5d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.4 MB (63371938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dbf6afa277997294b6f9e3bd7f8014662d29b3033a85b3ee5d4dc7bdebb89d4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 16 Apr 2025 11:55:02 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1754870400'
# Wed, 16 Apr 2025 11:55:02 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Wed, 16 Apr 2025 11:55:02 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
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
	-	`sha256:42c6883fd732cb484051b4fff6157db32a689c12264945da05c930608a6fe450`  
		Last Modified: Tue, 12 Aug 2025 20:47:00 GMT  
		Size: 25.5 MB (25544117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04f99498d847e9f3cd5269623df3574a733aa9ef5a52b928a12d356921ac1224`  
		Last Modified: Wed, 13 Aug 2025 00:18:28 GMT  
		Size: 4.5 MB (4491819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b4fa885c91e8780fb0d8a72e2a4378b07aee4f992a55e4635280694898b37f5`  
		Last Modified: Wed, 13 Aug 2025 00:18:53 GMT  
		Size: 33.3 MB (33311601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7c79f4d0f6c9999373dab61ea00c25df8717e3123d3fabf034145d804798480`  
		Last Modified: Wed, 13 Aug 2025 00:18:49 GMT  
		Size: 12.3 KB (12251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17b55877b4bdb93d35b49f27a89d5f36cbee1aef6385ce423e7525aae7a5aeb1`  
		Last Modified: Wed, 13 Aug 2025 00:18:49 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6797f08ba9e910ef062f6f63e61e00919bfeea1d9b7a85626f64892f50978cb5`  
		Last Modified: Wed, 13 Aug 2025 00:18:49 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9` - unknown; unknown

```console
$ docker pull chronograf@sha256:1dbdfa3a47641050da20e32061e446e46a97544552d324690efcb480c3684540
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3127875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78747f45cd7790c94bd33c2be34a21e3d79877c7271a4cd3dbac57c26bbf6d14`

```dockerfile
```

-	Layers:
	-	`sha256:87a7c8f01f56d30206382c338a31984664216e5681a6e061a53935b8ad67fcf9`  
		Last Modified: Wed, 13 Aug 2025 03:38:42 GMT  
		Size: 3.1 MB (3111992 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63b3041c3e3a93905c9116d64bb3642d3ecb14898fae8deae5f5a97942a3bdf5`  
		Last Modified: Wed, 13 Aug 2025 03:38:42 GMT  
		Size: 15.9 KB (15883 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.9` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:0acdda34c87960bdaf5198d4a7c2bbfe82bbadb86606667882d5d50588d7317c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.2 MB (67166472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69b18571ff87f3f4c8c52c3cb2d4116529904af794ad4025996a48f8f65604b1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 16 Apr 2025 11:55:02 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1754870400'
# Wed, 16 Apr 2025 11:55:02 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Wed, 16 Apr 2025 11:55:02 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
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
	-	`sha256:b99ef417bc3eb3946e7b3162f6c19dbca1039f3b4124deb116c3a0ab763e65ad`  
		Last Modified: Tue, 12 Aug 2025 22:33:30 GMT  
		Size: 28.8 MB (28750491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb2bf7bf292427b2ba72209f2594d098eecd42f7f9360bfb670e1b31c92b8330`  
		Last Modified: Wed, 13 Aug 2025 06:59:29 GMT  
		Size: 5.2 MB (5209361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8800c81a8fbc693f41522d128629da0cf014ff079f088d09bb3947f1726e59f`  
		Last Modified: Wed, 13 Aug 2025 07:00:09 GMT  
		Size: 33.2 MB (33182235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b91f58e92e3d6b605c4c28fa21dbdc326fefa1111ff36087f49965c1a8f920d`  
		Last Modified: Wed, 13 Aug 2025 06:59:54 GMT  
		Size: 12.2 KB (12243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eef94ee9ebb2a844e52f83b0c9edb9a834ead3648ba01c3403a9b84b23fbae90`  
		Last Modified: Wed, 13 Aug 2025 06:59:55 GMT  
		Size: 11.9 KB (11903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8005db9e7308570df42f9e44b0df6fffe9fe07d22464c5929a1b0c7fa5a8654d`  
		Last Modified: Wed, 13 Aug 2025 06:59:55 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9` - unknown; unknown

```console
$ docker pull chronograf@sha256:9a9ed7e8f89b58f06e4afb3acac4e72fae387eab5f80daf33d3294b23032ab77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3125874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:deb3214af4ca7f9f5ee13684454cb0ad92e68f61c08f1125b01c4b539d1aacaa`

```dockerfile
```

-	Layers:
	-	`sha256:f9d5c7aa84d82a763c736b133e533f1ef4ce46f824254c9b5a525729c65b8d62`  
		Last Modified: Wed, 13 Aug 2025 09:38:41 GMT  
		Size: 3.1 MB (3109970 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54401664136d934217ccd90ea8677a1be5999a8b32b6a83333d95d679e4b96b1`  
		Last Modified: Wed, 13 Aug 2025 09:38:42 GMT  
		Size: 15.9 KB (15904 bytes)  
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
$ docker pull chronograf@sha256:4f07612ac9189032160213db3d09dca438664adf0d7901f296ade037c24e7df4
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
$ docker pull chronograf@sha256:af3c63195f586442a8b214c6753d3cabcaa41badda9cc231b62db75275b98126
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.5 MB (70518240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ccfa4d2309ca03cce796f5549726c9d3dd8b1b7398977f882b277624e915019`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 16 Apr 2025 11:55:02 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1754870400'
# Wed, 16 Apr 2025 11:55:02 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Wed, 16 Apr 2025 11:55:02 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
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
	-	`sha256:3e41ca17193bcd7630e4dd210602930b1f94464bdd59680bbf6654206f7707b8`  
		Last Modified: Tue, 12 Aug 2025 20:44:40 GMT  
		Size: 30.3 MB (30256118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00de6d2c80c33c22628fce0ffc1cc6bd2ad0473189669537b4ae8cfbc2d02a80`  
		Last Modified: Tue, 12 Aug 2025 21:22:57 GMT  
		Size: 5.2 MB (5226005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22daa18bd4e741fe41f098bee490776da7a37a0701fc514170952b21673583c2`  
		Last Modified: Tue, 12 Aug 2025 21:22:59 GMT  
		Size: 35.0 MB (35011741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:226fe7d00a2614a02d80239454ff6f80363ea1b591dc7cb8a9aa6adc1fd1170e`  
		Last Modified: Tue, 12 Aug 2025 21:22:57 GMT  
		Size: 12.2 KB (12237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ac2636356f53cc0d7be6c0fb54d340386ee674d4c4726a3635921aeb084dc11`  
		Last Modified: Tue, 12 Aug 2025 21:22:57 GMT  
		Size: 11.9 KB (11900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77fb31bd2ff670c5348032166a1d06dcf6eb1d3572d38e8eb1245aa369b381e3`  
		Last Modified: Tue, 12 Aug 2025 21:22:57 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9.4` - unknown; unknown

```console
$ docker pull chronograf@sha256:19f83cd415657cf3d21e186f986654a7a4082ff32e0e2fce909c25cf60bbb8f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3125530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22ff884e7ef9e6c391c4ec87bde2c5a59ff643ee15d6f6d91e087455cca8dd20`

```dockerfile
```

-	Layers:
	-	`sha256:4ca934156d28d47bb0b393b355fa132a5595152ceb1d89e154ae19e16ffdaa5c`  
		Last Modified: Wed, 13 Aug 2025 00:38:40 GMT  
		Size: 3.1 MB (3109721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c103e6d0957244309f9fbc9e82070a49e3a6e3bdd872f36d552aa6e51c991604`  
		Last Modified: Wed, 13 Aug 2025 00:38:40 GMT  
		Size: 15.8 KB (15809 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.9.4` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:acd8fd00fa697674f035e1a3a208246964278b7e99fdaed114a2028a13eac5d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.4 MB (63371938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dbf6afa277997294b6f9e3bd7f8014662d29b3033a85b3ee5d4dc7bdebb89d4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 16 Apr 2025 11:55:02 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1754870400'
# Wed, 16 Apr 2025 11:55:02 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Wed, 16 Apr 2025 11:55:02 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
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
	-	`sha256:42c6883fd732cb484051b4fff6157db32a689c12264945da05c930608a6fe450`  
		Last Modified: Tue, 12 Aug 2025 20:47:00 GMT  
		Size: 25.5 MB (25544117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04f99498d847e9f3cd5269623df3574a733aa9ef5a52b928a12d356921ac1224`  
		Last Modified: Wed, 13 Aug 2025 00:18:28 GMT  
		Size: 4.5 MB (4491819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b4fa885c91e8780fb0d8a72e2a4378b07aee4f992a55e4635280694898b37f5`  
		Last Modified: Wed, 13 Aug 2025 00:18:53 GMT  
		Size: 33.3 MB (33311601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7c79f4d0f6c9999373dab61ea00c25df8717e3123d3fabf034145d804798480`  
		Last Modified: Wed, 13 Aug 2025 00:18:49 GMT  
		Size: 12.3 KB (12251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17b55877b4bdb93d35b49f27a89d5f36cbee1aef6385ce423e7525aae7a5aeb1`  
		Last Modified: Wed, 13 Aug 2025 00:18:49 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6797f08ba9e910ef062f6f63e61e00919bfeea1d9b7a85626f64892f50978cb5`  
		Last Modified: Wed, 13 Aug 2025 00:18:49 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9.4` - unknown; unknown

```console
$ docker pull chronograf@sha256:1dbdfa3a47641050da20e32061e446e46a97544552d324690efcb480c3684540
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3127875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78747f45cd7790c94bd33c2be34a21e3d79877c7271a4cd3dbac57c26bbf6d14`

```dockerfile
```

-	Layers:
	-	`sha256:87a7c8f01f56d30206382c338a31984664216e5681a6e061a53935b8ad67fcf9`  
		Last Modified: Wed, 13 Aug 2025 03:38:42 GMT  
		Size: 3.1 MB (3111992 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63b3041c3e3a93905c9116d64bb3642d3ecb14898fae8deae5f5a97942a3bdf5`  
		Last Modified: Wed, 13 Aug 2025 03:38:42 GMT  
		Size: 15.9 KB (15883 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.9.4` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:0acdda34c87960bdaf5198d4a7c2bbfe82bbadb86606667882d5d50588d7317c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.2 MB (67166472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69b18571ff87f3f4c8c52c3cb2d4116529904af794ad4025996a48f8f65604b1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 16 Apr 2025 11:55:02 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1754870400'
# Wed, 16 Apr 2025 11:55:02 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Wed, 16 Apr 2025 11:55:02 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
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
	-	`sha256:b99ef417bc3eb3946e7b3162f6c19dbca1039f3b4124deb116c3a0ab763e65ad`  
		Last Modified: Tue, 12 Aug 2025 22:33:30 GMT  
		Size: 28.8 MB (28750491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb2bf7bf292427b2ba72209f2594d098eecd42f7f9360bfb670e1b31c92b8330`  
		Last Modified: Wed, 13 Aug 2025 06:59:29 GMT  
		Size: 5.2 MB (5209361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8800c81a8fbc693f41522d128629da0cf014ff079f088d09bb3947f1726e59f`  
		Last Modified: Wed, 13 Aug 2025 07:00:09 GMT  
		Size: 33.2 MB (33182235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b91f58e92e3d6b605c4c28fa21dbdc326fefa1111ff36087f49965c1a8f920d`  
		Last Modified: Wed, 13 Aug 2025 06:59:54 GMT  
		Size: 12.2 KB (12243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eef94ee9ebb2a844e52f83b0c9edb9a834ead3648ba01c3403a9b84b23fbae90`  
		Last Modified: Wed, 13 Aug 2025 06:59:55 GMT  
		Size: 11.9 KB (11903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8005db9e7308570df42f9e44b0df6fffe9fe07d22464c5929a1b0c7fa5a8654d`  
		Last Modified: Wed, 13 Aug 2025 06:59:55 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9.4` - unknown; unknown

```console
$ docker pull chronograf@sha256:9a9ed7e8f89b58f06e4afb3acac4e72fae387eab5f80daf33d3294b23032ab77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3125874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:deb3214af4ca7f9f5ee13684454cb0ad92e68f61c08f1125b01c4b539d1aacaa`

```dockerfile
```

-	Layers:
	-	`sha256:f9d5c7aa84d82a763c736b133e533f1ef4ce46f824254c9b5a525729c65b8d62`  
		Last Modified: Wed, 13 Aug 2025 09:38:41 GMT  
		Size: 3.1 MB (3109970 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54401664136d934217ccd90ea8677a1be5999a8b32b6a83333d95d679e4b96b1`  
		Last Modified: Wed, 13 Aug 2025 09:38:42 GMT  
		Size: 15.9 KB (15904 bytes)  
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
$ docker pull chronograf@sha256:b496312dcbd5ed38a3f1b8019f4692d2286df3255f77c22a0749139f8c1b9f4a
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
$ docker pull chronograf@sha256:78f194a5d8af0c73ca58362cca0592948111066a607dc37e0efed338037c00c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.4 MB (85409598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7227e098d6fdf17602053f1bd639e4f7b287a3243db15ed6cc2d99c44c487f9b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
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
	-	`sha256:b1badc6e50664185acfaa0ca255d8076061c2a9d881cecaaad281ae11af000ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:36 GMT  
		Size: 28.2 MB (28230255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57aec7ed967710aa3b3c38f8e7c98bff4173fe4269ed328bf52c69764048e03a`  
		Last Modified: Tue, 19 Aug 2025 16:46:07 GMT  
		Size: 7.9 MB (7878510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:062fc0487b5a20bcce7da16873ef46d5817c66d9d26faaa0a97e2aeb8d8ab2fd`  
		Last Modified: Tue, 19 Aug 2025 16:46:15 GMT  
		Size: 49.3 MB (49276370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dae64cb64cda55f522eaf1fe4ce88abdc53ae785d49a1e4fa1b93060396f096`  
		Last Modified: Tue, 19 Aug 2025 16:46:07 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c31654218009837dc4e26a1c34054dc87208494176e02ec6d7fbe1c1c6a5c5b0`  
		Last Modified: Tue, 19 Aug 2025 16:46:08 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43e3d95a8276abff48229102090caae2a128c08eee17ac353c3ae20759d94382`  
		Last Modified: Tue, 19 Aug 2025 16:46:08 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:8f7ee4f6c203fd1cc6832be3f4960f8092f1b71a11dc4def5c56d5c7388c44cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2867907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:736d3ee42dbd8a5e31d825443acee05181a59de41097627f3742c0b3fa22d1fa`

```dockerfile
```

-	Layers:
	-	`sha256:738f58d2b5b9f06f6b9dcce1872dc43b347364a0ed829903ace6caef278cfe1b`  
		Last Modified: Tue, 19 Aug 2025 18:38:26 GMT  
		Size: 2.9 MB (2851779 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d113181e5d099d77cd193bd01905dab2ea210354d0c9ed81b8acd51f4d6e858`  
		Last Modified: Tue, 19 Aug 2025 18:38:27 GMT  
		Size: 16.1 KB (16128 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:latest` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:5d4706b5ea3431b7a6d88f9a0e2c53c3c9de00e4867de1b85664f636675ba834
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76092724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1144f67aa0da33184a38ff78812da721e4318df5b0e6aef06a607a747cd273e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1754870400'
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
	-	`sha256:a8db185805c54c045d888f7030794ebee970355b2336287cac0a0e22638ffc98`  
		Last Modified: Tue, 12 Aug 2025 20:46:38 GMT  
		Size: 23.9 MB (23938929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6467ca1c42d384f418a149d76dc5dffecb06ee7bfd528370c217304ba45aa285`  
		Last Modified: Wed, 13 Aug 2025 00:19:33 GMT  
		Size: 6.5 MB (6507882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcde1791bf4a512698b9677a862e632cd904c5fe7d3cee3d3b2aa646ef39ff87`  
		Last Modified: Tue, 19 Aug 2025 16:45:16 GMT  
		Size: 45.6 MB (45621441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bb91915267956814c74aebb7affae5121addaa975b893c424f2789482bc6e9c`  
		Last Modified: Tue, 19 Aug 2025 16:45:12 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0eec03b6d74dd34f2b5434d4c06da89877670b1764b17758045801edf4d0029`  
		Last Modified: Tue, 19 Aug 2025 16:45:12 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44416c5e6e1125817c2bf8094b06422a46969077532be262773ff3d352309225`  
		Last Modified: Tue, 19 Aug 2025 16:45:12 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:a241ff49c55dc2ffca9c96b8b7165d4d16a6c875ad63c7d7b5167510d6d7ed05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2870283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1a2e6f8150a59143322702f7593648f341f96ddfa322b614ba13e9f2f3d4cf2`

```dockerfile
```

-	Layers:
	-	`sha256:1ccd882973abac33915102be65e694c85f036ad99ec8f02bbc09e9abe57fb889`  
		Last Modified: Tue, 19 Aug 2025 18:38:31 GMT  
		Size: 2.9 MB (2854076 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74931f1e4ddb721dd5d0a5fa1659791d0bbdb3f118eeb325615bfe5365a44233`  
		Last Modified: Tue, 19 Aug 2025 18:38:32 GMT  
		Size: 16.2 KB (16207 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:latest` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:7ab5bc34d8381df765d9e5225aa7245b40146f2b9032fcb59d2eab658cb387b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.8 MB (82841556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f963ed5432e0f380dc79450a4d42adf2caf8946e145434d7dfe9b81ab0fd452`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
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
	-	`sha256:9a80f9a055240e1d5ffd4b99717e18b5b3e924369b9155fb0a951a7a94b2c61f`  
		Last Modified: Tue, 12 Aug 2025 22:08:02 GMT  
		Size: 28.1 MB (28082001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93c08badcdfd21351f06fb3f6f3100986ebded72d529323ebb60dcb10b0854d8`  
		Last Modified: Tue, 19 Aug 2025 17:04:15 GMT  
		Size: 7.7 MB (7671576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e74f295773a20c5d5f5c63be7643f2dca67e8ac9ec4312b3b1a5a8b0f8aa8ce9`  
		Last Modified: Tue, 19 Aug 2025 17:04:18 GMT  
		Size: 47.1 MB (47063502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c0c286a7a2c93b238d8df6da9007c81af02dfde9d802ef02c8e7cd50d0e8c1e`  
		Last Modified: Tue, 19 Aug 2025 17:04:14 GMT  
		Size: 12.3 KB (12251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09a89652c558e398d8ff709538a0fae99179a0d8ab2fff955b6a35ff22903528`  
		Last Modified: Tue, 19 Aug 2025 17:04:14 GMT  
		Size: 11.9 KB (11912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:852aa334798995fd535d739a7c0c01cd0164ccc76062286a3af068e924569d30`  
		Last Modified: Tue, 19 Aug 2025 17:04:14 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:fbb8df3edfa7da1d3cf1ae84e530fe2ec2f5c2025d6c517978f3cb8be329d726
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2868287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1601707b645f7ec55a77c78262c0e519000abb798cc1a9179aad3b5035d207a`

```dockerfile
```

-	Layers:
	-	`sha256:b0f155cca9bdbc8e9c71242f7915ab57b5e588d6675befc5af3328123ea7653c`  
		Last Modified: Tue, 19 Aug 2025 18:38:36 GMT  
		Size: 2.9 MB (2852052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e07ce71181601270438c4e693d6bff3eeb54d11919dd1f334a08ea813a82e56a`  
		Last Modified: Tue, 19 Aug 2025 18:38:37 GMT  
		Size: 16.2 KB (16235 bytes)  
		MIME: application/vnd.in-toto+json
