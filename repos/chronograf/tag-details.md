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
$ docker pull chronograf@sha256:d892b3beb2e87e15a7bf775fa81b3e3898f59593127f1298f7ffcc1c6ef7c84c
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
$ docker pull chronograf@sha256:5f5537b449b3f8035637e4ce9eb6d4720ced46f8db9d4e2c13c95be6f1ac7be9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.1 MB (84069434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45996034df2c6fe446e5e2fd0aa29d585534c107ab461bba710b9e9e2a59446d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 14 May 2024 01:28:03 GMT
ADD file:5aaace706aa00ff97d243daa2c29f5de88f124e1b97c570634f16eef90783286 in / 
# Tue, 14 May 2024 01:28:04 GMT
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
	-	`sha256:09f376ebb190216b0459f470e71bec7b5dfa611d66bf008492b40dcc5f1d8eae`  
		Last Modified: Tue, 14 May 2024 01:32:30 GMT  
		Size: 29.2 MB (29150411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8f47b768815e9c2366c46a8534a57f09e4f6f0ff4b0b52b64ba601dc9a9c174`  
		Last Modified: Mon, 03 Jun 2024 19:00:29 GMT  
		Size: 7.7 MB (7676940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9489fbf683135fcfa140c8d0a17e9d550c173fc3a052bc84f9f267f99252cf48`  
		Last Modified: Mon, 03 Jun 2024 19:00:31 GMT  
		Size: 47.2 MB (47217627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ed019f6b0534dfea3bfb7a969d8574f9df636506f6f19524b92326e37d2ada2`  
		Last Modified: Mon, 03 Jun 2024 19:00:28 GMT  
		Size: 12.2 KB (12241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb7ab6f5f28a95f1a3f7d8c842fdfc39c48d986d7d2fc301067f3717612a58d4`  
		Last Modified: Mon, 03 Jun 2024 19:00:28 GMT  
		Size: 11.9 KB (11900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af934b4bf874818dedfe49e86bee37a24e98cfb0e261bef354508666419f1249`  
		Last Modified: Mon, 03 Jun 2024 19:00:30 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:c109af0e26df5eea8f474e65c0139dbb1f2441db69a8534d6e4d0c20f1eebaa6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2671399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d7cf432a9a5718d9f6b2250ab83415c141962d8a0deb4e8a169e459aff78d57`

```dockerfile
```

-	Layers:
	-	`sha256:c3d8929c831b697a62dc9682fd7ae7044d6cd8342004667d41fd27a573432ef3`  
		Last Modified: Mon, 03 Jun 2024 19:00:29 GMT  
		Size: 2.7 MB (2655514 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3661947447bdb2d0b40fbad7fa348a99abb8e7e835a3351efddc4c57262a0019`  
		Last Modified: Mon, 03 Jun 2024 19:00:28 GMT  
		Size: 15.9 KB (15885 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.10` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:44faf726089000b60356258f9f7d98942577a8dc5aeb81222e3e19f45544bc44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.3 MB (75343499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:607c12abf0a6340e115ce9868d3b8c08e9e126e903c3b7255375c8e63b924d45`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:4c737c0a5e5b59fcbe2bc42dca815263159a1e1d16789ebeee086933aac4649a in / 
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
	-	`sha256:12af5edb53b85c10582c3e3d437561cc626437f48928a30456a99941d87706e3`  
		Last Modified: Thu, 13 Jun 2024 01:01:38 GMT  
		Size: 24.7 MB (24740215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75438d5f55c1596d5b71b0ff2de7f744bb89ef0e34e17f35b68bc5407fcdd25c`  
		Last Modified: Thu, 13 Jun 2024 11:32:08 GMT  
		Size: 6.3 MB (6301071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8abb520682775aaf2f92e765c274afa25f92e29c9b06447406bc30196ecc7bbc`  
		Last Modified: Thu, 13 Jun 2024 11:32:09 GMT  
		Size: 44.3 MB (44277740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b096b401a3f1861dc090a8ec1e2b4feaf49ccedac38fa2b1a64433c4f3420ab0`  
		Last Modified: Thu, 13 Jun 2024 11:32:07 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ab4535f77e97c81c5f28b6bb30afc0a83ffa2f442f4eaa7013e620809b7f93a`  
		Last Modified: Thu, 13 Jun 2024 11:32:08 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77a22d996d479e1f6829449de4179c0e10096d4d6385851e085b36a83c96838`  
		Last Modified: Thu, 13 Jun 2024 11:32:09 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:1443e3a29bba6c1446a91cf9601149e6ed12d20dc103f10ba2a56e6c0eba5437
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2673817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e7f4b8109398f8f54b12e17810dd5d145dfbef6df08bf2c38321d54cd3ce0bc`

```dockerfile
```

-	Layers:
	-	`sha256:925658867c31cec76fa2298b3c9e4098bfe049889801846102570d8fa6afdb1b`  
		Last Modified: Thu, 13 Jun 2024 11:32:08 GMT  
		Size: 2.7 MB (2657810 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44c0ad4f959c95f849adfcf72f39c5078b2f5c6d3ddb009f2536969bdc22f677`  
		Last Modified: Thu, 13 Jun 2024 11:32:07 GMT  
		Size: 16.0 KB (16007 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.10` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:2509b79f21f8d2f01cc6fb1787c60e192cedbaa1c3a0df512f250cef530831b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.6 MB (81628369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa0abb98411db0e43a2472ca9a04e405f3988fda0221fc73309073c33d3f1e22`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:5f17f77072bcd27aa8c4d09ef5117423b789c42445b6e6c13af711dfb2abd544 in / 
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
	-	`sha256:559a764445207341cf1207d83ceb89f1e59e2b57e860b7a80a6df6447641832b`  
		Last Modified: Thu, 13 Jun 2024 00:43:13 GMT  
		Size: 29.2 MB (29179666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:190c44ee98f21bfee7c5d1f4a14f776fde4841c39b3768dd1ef9237f050a1c7e`  
		Last Modified: Thu, 13 Jun 2024 11:07:25 GMT  
		Size: 7.5 MB (7453190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1353d59f878028d1e53f5b9ba7ff5ffc15eba37b01f82eb05dd966d56edd38d`  
		Last Modified: Thu, 13 Jun 2024 11:07:27 GMT  
		Size: 45.0 MB (44971054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2acf276b9e8fbbd0dcc962675f697db83c1ae8c2bddaca1cb5c11c46971d74c7`  
		Last Modified: Thu, 13 Jun 2024 11:07:25 GMT  
		Size: 12.2 KB (12242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56e6dd95139e23cb8a4d10dad60fa476b92f5a9145a7dd7065456fe757ca3a31`  
		Last Modified: Thu, 13 Jun 2024 11:07:26 GMT  
		Size: 11.9 KB (11901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91708736b0c8e603f3424312a2afcaa5a538aa78627f508d8c4987f3ed15b722`  
		Last Modified: Thu, 13 Jun 2024 11:07:27 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:cd716da942a514ab19d44c83fa585a1630ed5119a82b7e3f88ebe30d0925a055
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2672016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1778fda725b4d6774f106bdc18c6d9b53fc21bdb277af9413e686b3ad5f1441`

```dockerfile
```

-	Layers:
	-	`sha256:f3e3f8f7212f21dc6670ffb3733e2c1980e6bc43ea569b9fd42cf0084277c5c9`  
		Last Modified: Thu, 13 Jun 2024 11:07:26 GMT  
		Size: 2.7 MB (2655786 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ecd3e10071bb448a595fd2dac1ecd5a65e785f3fad6449fd2bc71fbcbbe02612`  
		Last Modified: Thu, 13 Jun 2024 11:07:25 GMT  
		Size: 16.2 KB (16230 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.10-alpine`

```console
$ docker pull chronograf@sha256:0a4afb73e2d3a91a06e36601c0b8c9c18e5aeb825e8edcceb9d18e338a0e0203
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.10-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:b55598a8b3ee7feb689bcb380dc0f234d328f2eb47c881346dc30b481bb81f1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31807875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b40200ab7f22ab99c0b92e31ce0a9ef862bfd80a2efa3813ebad5e2bdf598f9b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
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
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a541091e90e8b5010bc3e6964324ac4919c24be8f5fb5653082302eec5fc1ec4`  
		Last Modified: Mon, 03 Jun 2024 19:00:15 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d70bae9f6b1c0feca8cb0ba973e7e28953ffa5a9d62cfbfcd897abd2d016af8`  
		Last Modified: Mon, 03 Jun 2024 19:00:16 GMT  
		Size: 294.3 KB (294348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27b085bda50e0c5e25c7a4ebec7e1ccd7ae22a5c76ef00439f8b7c4d022b38fb`  
		Last Modified: Mon, 03 Jun 2024 19:00:16 GMT  
		Size: 27.9 MB (27866729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1990a674718757fef7810e42e4c5340c248ad43f1d9abdec7439e5b9cd01723`  
		Last Modified: Mon, 03 Jun 2024 19:00:15 GMT  
		Size: 12.2 KB (12237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14e68549b54b63067c056976b55d6c93ac1866dcad3a2e1dde832662e2da39f8`  
		Last Modified: Mon, 03 Jun 2024 19:00:16 GMT  
		Size: 11.9 KB (11896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9edb80f2e5c4143929355c91c8f989dafdbea5bce4a5e2c628198ab81d0e456e`  
		Last Modified: Mon, 03 Jun 2024 19:00:16 GMT  
		Size: 292.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:27b4cb11ebf88b4475e41a68de08386fcb61342e61fff5f48ad3b929f482634f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.5 KB (244494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65197df914a82b3f2f03ba701ae27857bf44eff66c30c4cf0b573d7eda631965`

```dockerfile
```

-	Layers:
	-	`sha256:ca5768a37193228f1c8c19dcb7236caefe2d82d164db3e45a19eea54e191d717`  
		Last Modified: Mon, 03 Jun 2024 19:00:15 GMT  
		Size: 226.9 KB (226903 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe809aec848a51e9dedbd725ce359b20a0efb4f28696cc4188181514e5202eac`  
		Last Modified: Mon, 03 Jun 2024 19:00:15 GMT  
		Size: 17.6 KB (17591 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.10.5`

```console
$ docker pull chronograf@sha256:d892b3beb2e87e15a7bf775fa81b3e3898f59593127f1298f7ffcc1c6ef7c84c
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
$ docker pull chronograf@sha256:5f5537b449b3f8035637e4ce9eb6d4720ced46f8db9d4e2c13c95be6f1ac7be9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.1 MB (84069434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45996034df2c6fe446e5e2fd0aa29d585534c107ab461bba710b9e9e2a59446d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 14 May 2024 01:28:03 GMT
ADD file:5aaace706aa00ff97d243daa2c29f5de88f124e1b97c570634f16eef90783286 in / 
# Tue, 14 May 2024 01:28:04 GMT
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
	-	`sha256:09f376ebb190216b0459f470e71bec7b5dfa611d66bf008492b40dcc5f1d8eae`  
		Last Modified: Tue, 14 May 2024 01:32:30 GMT  
		Size: 29.2 MB (29150411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8f47b768815e9c2366c46a8534a57f09e4f6f0ff4b0b52b64ba601dc9a9c174`  
		Last Modified: Mon, 03 Jun 2024 19:00:29 GMT  
		Size: 7.7 MB (7676940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9489fbf683135fcfa140c8d0a17e9d550c173fc3a052bc84f9f267f99252cf48`  
		Last Modified: Mon, 03 Jun 2024 19:00:31 GMT  
		Size: 47.2 MB (47217627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ed019f6b0534dfea3bfb7a969d8574f9df636506f6f19524b92326e37d2ada2`  
		Last Modified: Mon, 03 Jun 2024 19:00:28 GMT  
		Size: 12.2 KB (12241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb7ab6f5f28a95f1a3f7d8c842fdfc39c48d986d7d2fc301067f3717612a58d4`  
		Last Modified: Mon, 03 Jun 2024 19:00:28 GMT  
		Size: 11.9 KB (11900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af934b4bf874818dedfe49e86bee37a24e98cfb0e261bef354508666419f1249`  
		Last Modified: Mon, 03 Jun 2024 19:00:30 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10.5` - unknown; unknown

```console
$ docker pull chronograf@sha256:c109af0e26df5eea8f474e65c0139dbb1f2441db69a8534d6e4d0c20f1eebaa6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2671399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d7cf432a9a5718d9f6b2250ab83415c141962d8a0deb4e8a169e459aff78d57`

```dockerfile
```

-	Layers:
	-	`sha256:c3d8929c831b697a62dc9682fd7ae7044d6cd8342004667d41fd27a573432ef3`  
		Last Modified: Mon, 03 Jun 2024 19:00:29 GMT  
		Size: 2.7 MB (2655514 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3661947447bdb2d0b40fbad7fa348a99abb8e7e835a3351efddc4c57262a0019`  
		Last Modified: Mon, 03 Jun 2024 19:00:28 GMT  
		Size: 15.9 KB (15885 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.10.5` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:44faf726089000b60356258f9f7d98942577a8dc5aeb81222e3e19f45544bc44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.3 MB (75343499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:607c12abf0a6340e115ce9868d3b8c08e9e126e903c3b7255375c8e63b924d45`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:4c737c0a5e5b59fcbe2bc42dca815263159a1e1d16789ebeee086933aac4649a in / 
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
	-	`sha256:12af5edb53b85c10582c3e3d437561cc626437f48928a30456a99941d87706e3`  
		Last Modified: Thu, 13 Jun 2024 01:01:38 GMT  
		Size: 24.7 MB (24740215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75438d5f55c1596d5b71b0ff2de7f744bb89ef0e34e17f35b68bc5407fcdd25c`  
		Last Modified: Thu, 13 Jun 2024 11:32:08 GMT  
		Size: 6.3 MB (6301071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8abb520682775aaf2f92e765c274afa25f92e29c9b06447406bc30196ecc7bbc`  
		Last Modified: Thu, 13 Jun 2024 11:32:09 GMT  
		Size: 44.3 MB (44277740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b096b401a3f1861dc090a8ec1e2b4feaf49ccedac38fa2b1a64433c4f3420ab0`  
		Last Modified: Thu, 13 Jun 2024 11:32:07 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ab4535f77e97c81c5f28b6bb30afc0a83ffa2f442f4eaa7013e620809b7f93a`  
		Last Modified: Thu, 13 Jun 2024 11:32:08 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77a22d996d479e1f6829449de4179c0e10096d4d6385851e085b36a83c96838`  
		Last Modified: Thu, 13 Jun 2024 11:32:09 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10.5` - unknown; unknown

```console
$ docker pull chronograf@sha256:1443e3a29bba6c1446a91cf9601149e6ed12d20dc103f10ba2a56e6c0eba5437
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2673817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e7f4b8109398f8f54b12e17810dd5d145dfbef6df08bf2c38321d54cd3ce0bc`

```dockerfile
```

-	Layers:
	-	`sha256:925658867c31cec76fa2298b3c9e4098bfe049889801846102570d8fa6afdb1b`  
		Last Modified: Thu, 13 Jun 2024 11:32:08 GMT  
		Size: 2.7 MB (2657810 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44c0ad4f959c95f849adfcf72f39c5078b2f5c6d3ddb009f2536969bdc22f677`  
		Last Modified: Thu, 13 Jun 2024 11:32:07 GMT  
		Size: 16.0 KB (16007 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.10.5` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:2509b79f21f8d2f01cc6fb1787c60e192cedbaa1c3a0df512f250cef530831b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.6 MB (81628369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa0abb98411db0e43a2472ca9a04e405f3988fda0221fc73309073c33d3f1e22`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:5f17f77072bcd27aa8c4d09ef5117423b789c42445b6e6c13af711dfb2abd544 in / 
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
	-	`sha256:559a764445207341cf1207d83ceb89f1e59e2b57e860b7a80a6df6447641832b`  
		Last Modified: Thu, 13 Jun 2024 00:43:13 GMT  
		Size: 29.2 MB (29179666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:190c44ee98f21bfee7c5d1f4a14f776fde4841c39b3768dd1ef9237f050a1c7e`  
		Last Modified: Thu, 13 Jun 2024 11:07:25 GMT  
		Size: 7.5 MB (7453190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1353d59f878028d1e53f5b9ba7ff5ffc15eba37b01f82eb05dd966d56edd38d`  
		Last Modified: Thu, 13 Jun 2024 11:07:27 GMT  
		Size: 45.0 MB (44971054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2acf276b9e8fbbd0dcc962675f697db83c1ae8c2bddaca1cb5c11c46971d74c7`  
		Last Modified: Thu, 13 Jun 2024 11:07:25 GMT  
		Size: 12.2 KB (12242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56e6dd95139e23cb8a4d10dad60fa476b92f5a9145a7dd7065456fe757ca3a31`  
		Last Modified: Thu, 13 Jun 2024 11:07:26 GMT  
		Size: 11.9 KB (11901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91708736b0c8e603f3424312a2afcaa5a538aa78627f508d8c4987f3ed15b722`  
		Last Modified: Thu, 13 Jun 2024 11:07:27 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10.5` - unknown; unknown

```console
$ docker pull chronograf@sha256:cd716da942a514ab19d44c83fa585a1630ed5119a82b7e3f88ebe30d0925a055
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2672016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1778fda725b4d6774f106bdc18c6d9b53fc21bdb277af9413e686b3ad5f1441`

```dockerfile
```

-	Layers:
	-	`sha256:f3e3f8f7212f21dc6670ffb3733e2c1980e6bc43ea569b9fd42cf0084277c5c9`  
		Last Modified: Thu, 13 Jun 2024 11:07:26 GMT  
		Size: 2.7 MB (2655786 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ecd3e10071bb448a595fd2dac1ecd5a65e785f3fad6449fd2bc71fbcbbe02612`  
		Last Modified: Thu, 13 Jun 2024 11:07:25 GMT  
		Size: 16.2 KB (16230 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.10.5-alpine`

```console
$ docker pull chronograf@sha256:0a4afb73e2d3a91a06e36601c0b8c9c18e5aeb825e8edcceb9d18e338a0e0203
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.10.5-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:b55598a8b3ee7feb689bcb380dc0f234d328f2eb47c881346dc30b481bb81f1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31807875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b40200ab7f22ab99c0b92e31ce0a9ef862bfd80a2efa3813ebad5e2bdf598f9b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
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
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a541091e90e8b5010bc3e6964324ac4919c24be8f5fb5653082302eec5fc1ec4`  
		Last Modified: Mon, 03 Jun 2024 19:00:15 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d70bae9f6b1c0feca8cb0ba973e7e28953ffa5a9d62cfbfcd897abd2d016af8`  
		Last Modified: Mon, 03 Jun 2024 19:00:16 GMT  
		Size: 294.3 KB (294348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27b085bda50e0c5e25c7a4ebec7e1ccd7ae22a5c76ef00439f8b7c4d022b38fb`  
		Last Modified: Mon, 03 Jun 2024 19:00:16 GMT  
		Size: 27.9 MB (27866729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1990a674718757fef7810e42e4c5340c248ad43f1d9abdec7439e5b9cd01723`  
		Last Modified: Mon, 03 Jun 2024 19:00:15 GMT  
		Size: 12.2 KB (12237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14e68549b54b63067c056976b55d6c93ac1866dcad3a2e1dde832662e2da39f8`  
		Last Modified: Mon, 03 Jun 2024 19:00:16 GMT  
		Size: 11.9 KB (11896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9edb80f2e5c4143929355c91c8f989dafdbea5bce4a5e2c628198ab81d0e456e`  
		Last Modified: Mon, 03 Jun 2024 19:00:16 GMT  
		Size: 292.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10.5-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:27b4cb11ebf88b4475e41a68de08386fcb61342e61fff5f48ad3b929f482634f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.5 KB (244494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65197df914a82b3f2f03ba701ae27857bf44eff66c30c4cf0b573d7eda631965`

```dockerfile
```

-	Layers:
	-	`sha256:ca5768a37193228f1c8c19dcb7236caefe2d82d164db3e45a19eea54e191d717`  
		Last Modified: Mon, 03 Jun 2024 19:00:15 GMT  
		Size: 226.9 KB (226903 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe809aec848a51e9dedbd725ce359b20a0efb4f28696cc4188181514e5202eac`  
		Last Modified: Mon, 03 Jun 2024 19:00:15 GMT  
		Size: 17.6 KB (17591 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.7`

```console
$ docker pull chronograf@sha256:429c6f0726522ec7ca8ea5b77d0c8a370713ea1952bbd405d17971bc3a756616
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
$ docker pull chronograf@sha256:e771eb1dd91558b1a234191d5b194723beb1f3acc6e887e1256051809977b2a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.2 MB (70201689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:605b64690951dfc164c533fad52c3743ffded563d05b84cc7e57c039205d2bd8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 14 May 2024 01:28:26 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
# Tue, 14 May 2024 01:28:27 GMT
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
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e7df2ee68a080fc3deb51ba4dc43a775497c517aff0c008f3250e06a2213587`  
		Last Modified: Mon, 03 Jun 2024 19:00:25 GMT  
		Size: 4.2 MB (4209290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17bf786ae42424dee79b994f9cd126bac3d075fccb72431933919c3c68f73081`  
		Last Modified: Mon, 03 Jun 2024 19:00:26 GMT  
		Size: 34.5 MB (34534081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83a0e61a65cd4085f394773e0a72b2bad7b72aa7b019abf7c461f523c2f4882d`  
		Last Modified: Mon, 03 Jun 2024 19:00:25 GMT  
		Size: 12.2 KB (12244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5300f7eb373467760bca394f741820823cdff2c6283a0b53f99b0df10a409b87`  
		Last Modified: Mon, 03 Jun 2024 19:00:24 GMT  
		Size: 11.9 KB (11903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d808014185b840155ec50f288b516fb94796c0651de48d9c110092fc34d4c540`  
		Last Modified: Mon, 03 Jun 2024 19:00:26 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7` - unknown; unknown

```console
$ docker pull chronograf@sha256:f397e6f11dd2f45e8dfca8151e06aadf76e5ae70bcd8defdc24bea152505427d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2882783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b81349ac4d5da0b18ef4d787d573f58ca14ede92048d9375cafdd998ad87538c`

```dockerfile
```

-	Layers:
	-	`sha256:4329e3e09074a6b3f14c33a784981c038f7eeac0768fd30776809a37b101221f`  
		Last Modified: Mon, 03 Jun 2024 19:00:24 GMT  
		Size: 2.9 MB (2867249 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:818df8a93fce3900326584636d20d90a00c8a677eef7decf16aca065754112ec`  
		Last Modified: Mon, 03 Jun 2024 19:00:24 GMT  
		Size: 15.5 KB (15534 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.7` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:e8c1dbdc58cd867a546082d749f4c4298d9f577ee3ea1cdaa7632942e3613056
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.0 MB (63024178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80dae7d4d704f3d4c2e548cadc3850abcf2e811a4beb4f4a5bf71ecea42f2c88`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:b23992f77c1f22e7bf9048641d6da1d6ef922d78b4118f6d513e183ae6de7e34 in / 
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
	-	`sha256:4873d96591a32d2d686ff6c86338fc9a63b9d60639482601b5402eb76e56a566`  
		Last Modified: Thu, 13 Jun 2024 01:02:22 GMT  
		Size: 26.6 MB (26594507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfc857b368b8d710984e0be6746147b47360c2eec872da8f74f84a7acc2420dd`  
		Last Modified: Thu, 13 Jun 2024 09:19:48 GMT  
		Size: 3.5 MB (3511581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5108114b9315a3767e2447a201e68bd82a9f349f22a7ea2ccd0b248f4a968d9`  
		Last Modified: Thu, 13 Jun 2024 09:19:49 GMT  
		Size: 32.9 MB (32893691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64b644705e9420f4863aac931a7a860af1d8364c25854856db631ef5b25c5348`  
		Last Modified: Thu, 13 Jun 2024 09:19:48 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c72f17ae86f0e003d7648dd33392156625d7fe55790ffa8469c68ffdd3bfa3a3`  
		Last Modified: Thu, 13 Jun 2024 09:19:49 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d418424a0ed31ec5f14612187a10bec0499bc90cd08fa251c74a8c953c3303c`  
		Last Modified: Thu, 13 Jun 2024 09:19:49 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7` - unknown; unknown

```console
$ docker pull chronograf@sha256:c453ddd11dad5c1768b003cd64385720200341b9382ee0a4abaca7477bce6b53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2885167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b75968b473964d93f5fc0adad8690facb44b1ae12f148fafbd11dd1ef745c56`

```dockerfile
```

-	Layers:
	-	`sha256:7c3b2d30cddcd65e0006cd88358bd792915ed9cdb020a574e2e4bcf174d64fb5`  
		Last Modified: Thu, 13 Jun 2024 09:19:48 GMT  
		Size: 2.9 MB (2869519 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6451a2dd77920643ca8b0150757c6732c25e5fb619e2a527f42d5509d6eb522b`  
		Last Modified: Thu, 13 Jun 2024 09:19:48 GMT  
		Size: 15.6 KB (15648 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.7` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:5a189457a4964185a65a2a1d6d6c3c1d2db507466c49135b1f74424a4cdaf828
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.4 MB (67355818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb9c267055303d21cdaca86881e279f2d208b80964f55576da91fdb916363886`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:55edb70d595bba9782144ef15994a2ae5c40adeb65f6c3acd6570a0c148ffa96 in / 
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
	-	`sha256:ca4da1869379178993d4f7abc946f75e7515789ff7e15c7ccfedfc8e2bfeaf6d`  
		Last Modified: Thu, 13 Jun 2024 00:43:54 GMT  
		Size: 30.1 MB (30086973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2c8db4492f9f092c550f5ffb33afd2d670d2b138f83d90b8b8a69d7e9b1fec2`  
		Last Modified: Thu, 13 Jun 2024 08:44:32 GMT  
		Size: 4.2 MB (4210560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca33934a7cbc211a45559871136f7c60f01f796fb536d63dc036173814faf236`  
		Last Modified: Thu, 13 Jun 2024 08:44:33 GMT  
		Size: 33.0 MB (33033891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96932bde717aa7cebd87911175141b352c136580456aa23dcb72516623588ed1`  
		Last Modified: Thu, 13 Jun 2024 08:44:31 GMT  
		Size: 12.2 KB (12244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01523c2ad47ed495e4192d57a1f4f25cf64b250f9b173a87a4e8d378c62f22a1`  
		Last Modified: Thu, 13 Jun 2024 08:44:32 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4792d4db8a65302c0b0963b8e8559d7e6ef32bad62d4610f037aac8e0edd38b2`  
		Last Modified: Thu, 13 Jun 2024 08:44:33 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7` - unknown; unknown

```console
$ docker pull chronograf@sha256:d6b789e80c41b570391981557b35d3c0ee8b386b24274358088320b71ccaf6f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2883365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39b75d0f914bf542c53e473755fa81ae9ce94b8ffd80eedfd68549562c9dd16b`

```dockerfile
```

-	Layers:
	-	`sha256:6564687ae3dc3ab0d1ae7e9828d8f6a9e8c1fb7cd2462b5d3b3b6388e95d075f`  
		Last Modified: Thu, 13 Jun 2024 08:44:32 GMT  
		Size: 2.9 MB (2867497 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7dcbcad728ed505b86f2a4428c05f3c6531b9b9a0afd66eca17a99300ee8f19e`  
		Last Modified: Thu, 13 Jun 2024 08:44:31 GMT  
		Size: 15.9 KB (15868 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.7-alpine`

```console
$ docker pull chronograf@sha256:97e608fbc9d5ece2e10d6a4fdeb5400ab2b90bc51fa11a1bc0e329b22085ddae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.7-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:1d63485ec327e512c21c99df65684bcd2a16298a4db56ce0a85d74a728119938
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.5 MB (23495805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:def726efefa52ab291a85a9ff7797ab7af190886858938f7279f3bb6606a5341`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
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
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75e2c1a9f5d7c296d9d1f78c0c01e7df684fbdaa939eb66a82be32faea4e39ae`  
		Last Modified: Mon, 03 Jun 2024 18:59:59 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aa917d7092520fd13899ba8333f1456d1f26988be1ae52b911a160ddd5b2809`  
		Last Modified: Mon, 03 Jun 2024 18:59:59 GMT  
		Size: 292.4 KB (292424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aedecea2ae51e24c52152130aca5bb48b609f7bbbdd3239bf354d7180a56dc47`  
		Last Modified: Mon, 03 Jun 2024 19:00:00 GMT  
		Size: 19.6 MB (19556638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c35c4f6bb929f1d4a3a4e51fd8978406eb1d2c52a4446eaef7c8a9e65dd3d58`  
		Last Modified: Mon, 03 Jun 2024 18:59:59 GMT  
		Size: 12.2 KB (12236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d44cf4b9c32bc43bfa342f40a682936838b43be837fda1cbe80bb5406d2e77a6`  
		Last Modified: Mon, 03 Jun 2024 19:00:00 GMT  
		Size: 11.9 KB (11895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ba311571e9924d052a4fd7db0373dbf85cfc7c1a99913ffc875962b0301edbd`  
		Last Modified: Mon, 03 Jun 2024 19:00:00 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:684f4abf7dc03aafcafa10c64f606dcd67321ed31a6a18fa0a649e5afb6cdf9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.2 KB (185205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f58c1b8e25e159332e920cd7b703247a56de8758e250f5754e17d928cd5fbe5`

```dockerfile
```

-	Layers:
	-	`sha256:777bc9907af9c3bab9a2d0bbdbd7fe95706c24123c611cc88a32ac9879ad3b34`  
		Last Modified: Mon, 03 Jun 2024 18:59:59 GMT  
		Size: 168.6 KB (168559 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10b5c042e918ee2f9be2275c2fa0c83af682a39434975a5196910b675f04ee6f`  
		Last Modified: Mon, 03 Jun 2024 18:59:59 GMT  
		Size: 16.6 KB (16646 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.7.17`

```console
$ docker pull chronograf@sha256:429c6f0726522ec7ca8ea5b77d0c8a370713ea1952bbd405d17971bc3a756616
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
$ docker pull chronograf@sha256:e771eb1dd91558b1a234191d5b194723beb1f3acc6e887e1256051809977b2a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.2 MB (70201689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:605b64690951dfc164c533fad52c3743ffded563d05b84cc7e57c039205d2bd8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 14 May 2024 01:28:26 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
# Tue, 14 May 2024 01:28:27 GMT
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
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e7df2ee68a080fc3deb51ba4dc43a775497c517aff0c008f3250e06a2213587`  
		Last Modified: Mon, 03 Jun 2024 19:00:25 GMT  
		Size: 4.2 MB (4209290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17bf786ae42424dee79b994f9cd126bac3d075fccb72431933919c3c68f73081`  
		Last Modified: Mon, 03 Jun 2024 19:00:26 GMT  
		Size: 34.5 MB (34534081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83a0e61a65cd4085f394773e0a72b2bad7b72aa7b019abf7c461f523c2f4882d`  
		Last Modified: Mon, 03 Jun 2024 19:00:25 GMT  
		Size: 12.2 KB (12244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5300f7eb373467760bca394f741820823cdff2c6283a0b53f99b0df10a409b87`  
		Last Modified: Mon, 03 Jun 2024 19:00:24 GMT  
		Size: 11.9 KB (11903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d808014185b840155ec50f288b516fb94796c0651de48d9c110092fc34d4c540`  
		Last Modified: Mon, 03 Jun 2024 19:00:26 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7.17` - unknown; unknown

```console
$ docker pull chronograf@sha256:f397e6f11dd2f45e8dfca8151e06aadf76e5ae70bcd8defdc24bea152505427d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2882783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b81349ac4d5da0b18ef4d787d573f58ca14ede92048d9375cafdd998ad87538c`

```dockerfile
```

-	Layers:
	-	`sha256:4329e3e09074a6b3f14c33a784981c038f7eeac0768fd30776809a37b101221f`  
		Last Modified: Mon, 03 Jun 2024 19:00:24 GMT  
		Size: 2.9 MB (2867249 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:818df8a93fce3900326584636d20d90a00c8a677eef7decf16aca065754112ec`  
		Last Modified: Mon, 03 Jun 2024 19:00:24 GMT  
		Size: 15.5 KB (15534 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.7.17` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:e8c1dbdc58cd867a546082d749f4c4298d9f577ee3ea1cdaa7632942e3613056
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.0 MB (63024178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80dae7d4d704f3d4c2e548cadc3850abcf2e811a4beb4f4a5bf71ecea42f2c88`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:b23992f77c1f22e7bf9048641d6da1d6ef922d78b4118f6d513e183ae6de7e34 in / 
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
	-	`sha256:4873d96591a32d2d686ff6c86338fc9a63b9d60639482601b5402eb76e56a566`  
		Last Modified: Thu, 13 Jun 2024 01:02:22 GMT  
		Size: 26.6 MB (26594507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfc857b368b8d710984e0be6746147b47360c2eec872da8f74f84a7acc2420dd`  
		Last Modified: Thu, 13 Jun 2024 09:19:48 GMT  
		Size: 3.5 MB (3511581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5108114b9315a3767e2447a201e68bd82a9f349f22a7ea2ccd0b248f4a968d9`  
		Last Modified: Thu, 13 Jun 2024 09:19:49 GMT  
		Size: 32.9 MB (32893691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64b644705e9420f4863aac931a7a860af1d8364c25854856db631ef5b25c5348`  
		Last Modified: Thu, 13 Jun 2024 09:19:48 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c72f17ae86f0e003d7648dd33392156625d7fe55790ffa8469c68ffdd3bfa3a3`  
		Last Modified: Thu, 13 Jun 2024 09:19:49 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d418424a0ed31ec5f14612187a10bec0499bc90cd08fa251c74a8c953c3303c`  
		Last Modified: Thu, 13 Jun 2024 09:19:49 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7.17` - unknown; unknown

```console
$ docker pull chronograf@sha256:c453ddd11dad5c1768b003cd64385720200341b9382ee0a4abaca7477bce6b53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2885167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b75968b473964d93f5fc0adad8690facb44b1ae12f148fafbd11dd1ef745c56`

```dockerfile
```

-	Layers:
	-	`sha256:7c3b2d30cddcd65e0006cd88358bd792915ed9cdb020a574e2e4bcf174d64fb5`  
		Last Modified: Thu, 13 Jun 2024 09:19:48 GMT  
		Size: 2.9 MB (2869519 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6451a2dd77920643ca8b0150757c6732c25e5fb619e2a527f42d5509d6eb522b`  
		Last Modified: Thu, 13 Jun 2024 09:19:48 GMT  
		Size: 15.6 KB (15648 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.7.17` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:5a189457a4964185a65a2a1d6d6c3c1d2db507466c49135b1f74424a4cdaf828
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.4 MB (67355818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb9c267055303d21cdaca86881e279f2d208b80964f55576da91fdb916363886`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:55edb70d595bba9782144ef15994a2ae5c40adeb65f6c3acd6570a0c148ffa96 in / 
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
	-	`sha256:ca4da1869379178993d4f7abc946f75e7515789ff7e15c7ccfedfc8e2bfeaf6d`  
		Last Modified: Thu, 13 Jun 2024 00:43:54 GMT  
		Size: 30.1 MB (30086973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2c8db4492f9f092c550f5ffb33afd2d670d2b138f83d90b8b8a69d7e9b1fec2`  
		Last Modified: Thu, 13 Jun 2024 08:44:32 GMT  
		Size: 4.2 MB (4210560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca33934a7cbc211a45559871136f7c60f01f796fb536d63dc036173814faf236`  
		Last Modified: Thu, 13 Jun 2024 08:44:33 GMT  
		Size: 33.0 MB (33033891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96932bde717aa7cebd87911175141b352c136580456aa23dcb72516623588ed1`  
		Last Modified: Thu, 13 Jun 2024 08:44:31 GMT  
		Size: 12.2 KB (12244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01523c2ad47ed495e4192d57a1f4f25cf64b250f9b173a87a4e8d378c62f22a1`  
		Last Modified: Thu, 13 Jun 2024 08:44:32 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4792d4db8a65302c0b0963b8e8559d7e6ef32bad62d4610f037aac8e0edd38b2`  
		Last Modified: Thu, 13 Jun 2024 08:44:33 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7.17` - unknown; unknown

```console
$ docker pull chronograf@sha256:d6b789e80c41b570391981557b35d3c0ee8b386b24274358088320b71ccaf6f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2883365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39b75d0f914bf542c53e473755fa81ae9ce94b8ffd80eedfd68549562c9dd16b`

```dockerfile
```

-	Layers:
	-	`sha256:6564687ae3dc3ab0d1ae7e9828d8f6a9e8c1fb7cd2462b5d3b3b6388e95d075f`  
		Last Modified: Thu, 13 Jun 2024 08:44:32 GMT  
		Size: 2.9 MB (2867497 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7dcbcad728ed505b86f2a4428c05f3c6531b9b9a0afd66eca17a99300ee8f19e`  
		Last Modified: Thu, 13 Jun 2024 08:44:31 GMT  
		Size: 15.9 KB (15868 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.7.17-alpine`

```console
$ docker pull chronograf@sha256:97e608fbc9d5ece2e10d6a4fdeb5400ab2b90bc51fa11a1bc0e329b22085ddae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.7.17-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:1d63485ec327e512c21c99df65684bcd2a16298a4db56ce0a85d74a728119938
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.5 MB (23495805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:def726efefa52ab291a85a9ff7797ab7af190886858938f7279f3bb6606a5341`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
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
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75e2c1a9f5d7c296d9d1f78c0c01e7df684fbdaa939eb66a82be32faea4e39ae`  
		Last Modified: Mon, 03 Jun 2024 18:59:59 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aa917d7092520fd13899ba8333f1456d1f26988be1ae52b911a160ddd5b2809`  
		Last Modified: Mon, 03 Jun 2024 18:59:59 GMT  
		Size: 292.4 KB (292424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aedecea2ae51e24c52152130aca5bb48b609f7bbbdd3239bf354d7180a56dc47`  
		Last Modified: Mon, 03 Jun 2024 19:00:00 GMT  
		Size: 19.6 MB (19556638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c35c4f6bb929f1d4a3a4e51fd8978406eb1d2c52a4446eaef7c8a9e65dd3d58`  
		Last Modified: Mon, 03 Jun 2024 18:59:59 GMT  
		Size: 12.2 KB (12236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d44cf4b9c32bc43bfa342f40a682936838b43be837fda1cbe80bb5406d2e77a6`  
		Last Modified: Mon, 03 Jun 2024 19:00:00 GMT  
		Size: 11.9 KB (11895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ba311571e9924d052a4fd7db0373dbf85cfc7c1a99913ffc875962b0301edbd`  
		Last Modified: Mon, 03 Jun 2024 19:00:00 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7.17-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:684f4abf7dc03aafcafa10c64f606dcd67321ed31a6a18fa0a649e5afb6cdf9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.2 KB (185205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f58c1b8e25e159332e920cd7b703247a56de8758e250f5754e17d928cd5fbe5`

```dockerfile
```

-	Layers:
	-	`sha256:777bc9907af9c3bab9a2d0bbdbd7fe95706c24123c611cc88a32ac9879ad3b34`  
		Last Modified: Mon, 03 Jun 2024 18:59:59 GMT  
		Size: 168.6 KB (168559 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10b5c042e918ee2f9be2275c2fa0c83af682a39434975a5196910b675f04ee6f`  
		Last Modified: Mon, 03 Jun 2024 18:59:59 GMT  
		Size: 16.6 KB (16646 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.8`

```console
$ docker pull chronograf@sha256:fa8458016108f89d7a41e199b5a2328f4fd99fbbd6ece7cf481744bf7f0d9cba
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
$ docker pull chronograf@sha256:5557231e8b7359e64fe893db4c44ec6a88c6941ab9c0255f63e4a5b525be776d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.8 MB (70843298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:343f144f88c351cb4154a088c734f465dd8f0948cd8739479a75af84e756370e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 14 May 2024 01:28:26 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
# Tue, 14 May 2024 01:28:27 GMT
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
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2f2f9f4c33d963aab8040475e05d4ef5a3f7ae046cc091ed9bda0c18b756da5`  
		Last Modified: Mon, 03 Jun 2024 19:00:11 GMT  
		Size: 5.0 MB (5020970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c035d2957988e1173e9f6f9599aa16e8270ac0d9edf22d7e06e9d2768bf95e03`  
		Last Modified: Mon, 03 Jun 2024 19:00:12 GMT  
		Size: 34.4 MB (34364003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7ff06671a7bd3dc445e3a0b76cf4980c954f465684e3aade2573d09e8ae5dbb`  
		Last Modified: Mon, 03 Jun 2024 19:00:11 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8886242ffbb981aeeb9fb18ca92fafe3551251f1113894a8ee302d4bd4065d10`  
		Last Modified: Mon, 03 Jun 2024 19:00:11 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1477d5e19f7a88eec147ff9d1087ddf91119230a6cad1df2639442af1ba928f`  
		Last Modified: Mon, 03 Jun 2024 19:00:12 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8` - unknown; unknown

```console
$ docker pull chronograf@sha256:67f8177d088cf68030d2928785378620f67d557018c26651ced27c2adfec3b69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2930484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e58e4ab8ef6e0f7c2502f1a91712fac46383806ad0b9ec2ed29fe6cf3034cc25`

```dockerfile
```

-	Layers:
	-	`sha256:58e9f2be0be0429d43da092caf76494013dc3a94b38c76351ec82141bbe4824c`  
		Last Modified: Mon, 03 Jun 2024 19:00:10 GMT  
		Size: 2.9 MB (2914910 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2392821973aa9fda09092705d6fa46b96ac55ac41c9e025d2addeeb034282a9`  
		Last Modified: Mon, 03 Jun 2024 19:00:10 GMT  
		Size: 15.6 KB (15574 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.8` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:bb3e66d6c9832cd664e9021e3f6405ba83f5ecb4870941aa5cf11c6bf09ece41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.4 MB (63439778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c017f219aa60be9c7ea5f843fac93fd944419c42b5cfc23e11ea0c8d11200372`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:b23992f77c1f22e7bf9048641d6da1d6ef922d78b4118f6d513e183ae6de7e34 in / 
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
	-	`sha256:4873d96591a32d2d686ff6c86338fc9a63b9d60639482601b5402eb76e56a566`  
		Last Modified: Thu, 13 Jun 2024 01:02:22 GMT  
		Size: 26.6 MB (26594507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38b44c51ee1047daf831e46ae5c5d51ab0bb42e09a720bc2494af40a62b0e8a5`  
		Last Modified: Thu, 13 Jun 2024 11:25:33 GMT  
		Size: 4.3 MB (4286106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1a074d54bfff3b561913083eb215bd5f65bbb794a9f95250734413da02fae4c`  
		Last Modified: Thu, 13 Jun 2024 11:25:34 GMT  
		Size: 32.5 MB (32534764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08e0c3ada9a445e5493eadc340a0097258667b6c249b9ec950dd9545687d671c`  
		Last Modified: Thu, 13 Jun 2024 11:25:33 GMT  
		Size: 12.3 KB (12251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:661f5843759261a7047ba154588dd336e3d6561415a5860a5e24297b4af03c30`  
		Last Modified: Thu, 13 Jun 2024 11:25:33 GMT  
		Size: 11.9 KB (11911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1e34f4ae112ea0100db29d1348d379ae29dd6a9c8e50d13c3ed2a26c3c5175f`  
		Last Modified: Thu, 13 Jun 2024 11:25:34 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8` - unknown; unknown

```console
$ docker pull chronograf@sha256:7cce967027f5ef040a5bfd642ee75418d62ce37a267f3134ba86212318358701
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2932870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:710f6a30bdc8189d94d8503246650ab0383af609099a64b653ba125b30aed718`

```dockerfile
```

-	Layers:
	-	`sha256:2838fb4151efe572aff1b000c48fb89f6b70eeed955a8bda2dfb3bb3506238bf`  
		Last Modified: Thu, 13 Jun 2024 11:25:33 GMT  
		Size: 2.9 MB (2917180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b742368182d39ce403a01c97059fcebd519d6bbd3d64139595e651fd7a516f94`  
		Last Modified: Thu, 13 Jun 2024 11:25:32 GMT  
		Size: 15.7 KB (15690 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.8` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:91aae5d8912885c88287b065515265162286007c187c648361ed8b47cc99f3f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.5 MB (67544910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6d7a5d74734ac0e44525de668af66d1c8a820511af4d2e35028e5d5de72473b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:55edb70d595bba9782144ef15994a2ae5c40adeb65f6c3acd6570a0c148ffa96 in / 
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
	-	`sha256:ca4da1869379178993d4f7abc946f75e7515789ff7e15c7ccfedfc8e2bfeaf6d`  
		Last Modified: Thu, 13 Jun 2024 00:43:54 GMT  
		Size: 30.1 MB (30086973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e198db4c78d05a7fae6481f1f23e9abd0f4bd589e25e5b4afa53b8cb416bbfc7`  
		Last Modified: Thu, 13 Jun 2024 10:39:04 GMT  
		Size: 5.0 MB (5004108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0299cfd86fa3f79a7004d1cce8b56dde224addfbd665488e4ca70acc75d20470`  
		Last Modified: Thu, 13 Jun 2024 10:39:05 GMT  
		Size: 32.4 MB (32429432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:352c9608ddcf2ce9b44f0b0aaf9a71dbf0a7d9d83dd4c946e20c4bb07a21ce7c`  
		Last Modified: Thu, 13 Jun 2024 10:39:04 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ebdc4ba22b8ea39106433506e2f36daae588229d50644f58ff2347feaa7bdc3`  
		Last Modified: Thu, 13 Jun 2024 10:39:04 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f74e98413252a072b47934a947e3ff659675761a772b2098a242888f8876feaf`  
		Last Modified: Thu, 13 Jun 2024 10:39:05 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8` - unknown; unknown

```console
$ docker pull chronograf@sha256:f84cd02a12ebfbf384a8f5228f5a9bb7e90f0d010b65917008dc506c8d61e53a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2931066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d6c2de8e3269574d9287fcc9e73e6428b5b977210e3fa490bbc7b86f5c033be`

```dockerfile
```

-	Layers:
	-	`sha256:6d9f8b4d656f1021b4fc951ad5021fd727a0f2d9868dc178776008ea2e8d2588`  
		Last Modified: Thu, 13 Jun 2024 10:39:04 GMT  
		Size: 2.9 MB (2915158 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:669b39bb1e5a6a4645a76705f6123148de76ad978dc395af0a5542509ae8f98f`  
		Last Modified: Thu, 13 Jun 2024 10:39:04 GMT  
		Size: 15.9 KB (15908 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.8-alpine`

```console
$ docker pull chronograf@sha256:aeff6b0f33ad0c7163d0f15359676e3783b2c4f051277623bb87d3d8f525245b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.8-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:6901af16d25884590ef18c7cf6bc51e247e34e8db598d51aeac3a32686b96281
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23143191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fabb3a35dd209be242515d9abdb28872c03b6087716da9e68d7144ced10310b9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
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
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7135375e7e2b93794abc3a6fae771e0e810f1c985d87d5e2b116928c4a5811bb`  
		Last Modified: Mon, 03 Jun 2024 19:00:15 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7604efdcdfb5e914425082e913fa11feebc46f84efbd0eab4d63c026755d79f1`  
		Last Modified: Mon, 03 Jun 2024 19:00:14 GMT  
		Size: 292.4 KB (292422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed08262353aa43a044b72561106caeca51305919dbb951ad7fe4acfc2ad372f0`  
		Last Modified: Mon, 03 Jun 2024 19:00:15 GMT  
		Size: 19.2 MB (19204026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c69cc0629a8f4b4b5775f08d6212e7252bb99bc8b01e1d779a5306d8ce594551`  
		Last Modified: Mon, 03 Jun 2024 19:00:14 GMT  
		Size: 12.2 KB (12236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36c2b2e66b9548a4f932659927715ec1cabc2c5dd4425dd03f2b7185209ba8b9`  
		Last Modified: Mon, 03 Jun 2024 19:00:16 GMT  
		Size: 11.9 KB (11896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0910d626bd5a2723486bd6566ee32668ae861e7a1e18975ac98825605fefe14`  
		Last Modified: Mon, 03 Jun 2024 19:00:16 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:e509b26098019dd58f191c86c4a74dae8e741425f72ae6bf2db1768e4eb80d54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.5 KB (233529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2a1345abbc1eb7303aad85d664a52c2b91b5a286113333875fd693f733f01db`

```dockerfile
```

-	Layers:
	-	`sha256:15f8d2f11400eec69f6ea0110c8ae1da088d7809dc0222f8354511b1bcef6a8a`  
		Last Modified: Mon, 03 Jun 2024 19:00:14 GMT  
		Size: 216.9 KB (216881 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f7394674c01a304ac4ca09c635793f21386d3fff6e6fe7b304eea2650beae68`  
		Last Modified: Mon, 03 Jun 2024 19:00:14 GMT  
		Size: 16.6 KB (16648 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.8.10`

```console
$ docker pull chronograf@sha256:fa8458016108f89d7a41e199b5a2328f4fd99fbbd6ece7cf481744bf7f0d9cba
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
$ docker pull chronograf@sha256:5557231e8b7359e64fe893db4c44ec6a88c6941ab9c0255f63e4a5b525be776d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.8 MB (70843298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:343f144f88c351cb4154a088c734f465dd8f0948cd8739479a75af84e756370e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 14 May 2024 01:28:26 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
# Tue, 14 May 2024 01:28:27 GMT
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
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2f2f9f4c33d963aab8040475e05d4ef5a3f7ae046cc091ed9bda0c18b756da5`  
		Last Modified: Mon, 03 Jun 2024 19:00:11 GMT  
		Size: 5.0 MB (5020970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c035d2957988e1173e9f6f9599aa16e8270ac0d9edf22d7e06e9d2768bf95e03`  
		Last Modified: Mon, 03 Jun 2024 19:00:12 GMT  
		Size: 34.4 MB (34364003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7ff06671a7bd3dc445e3a0b76cf4980c954f465684e3aade2573d09e8ae5dbb`  
		Last Modified: Mon, 03 Jun 2024 19:00:11 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8886242ffbb981aeeb9fb18ca92fafe3551251f1113894a8ee302d4bd4065d10`  
		Last Modified: Mon, 03 Jun 2024 19:00:11 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1477d5e19f7a88eec147ff9d1087ddf91119230a6cad1df2639442af1ba928f`  
		Last Modified: Mon, 03 Jun 2024 19:00:12 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:67f8177d088cf68030d2928785378620f67d557018c26651ced27c2adfec3b69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2930484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e58e4ab8ef6e0f7c2502f1a91712fac46383806ad0b9ec2ed29fe6cf3034cc25`

```dockerfile
```

-	Layers:
	-	`sha256:58e9f2be0be0429d43da092caf76494013dc3a94b38c76351ec82141bbe4824c`  
		Last Modified: Mon, 03 Jun 2024 19:00:10 GMT  
		Size: 2.9 MB (2914910 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2392821973aa9fda09092705d6fa46b96ac55ac41c9e025d2addeeb034282a9`  
		Last Modified: Mon, 03 Jun 2024 19:00:10 GMT  
		Size: 15.6 KB (15574 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.8.10` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:bb3e66d6c9832cd664e9021e3f6405ba83f5ecb4870941aa5cf11c6bf09ece41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.4 MB (63439778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c017f219aa60be9c7ea5f843fac93fd944419c42b5cfc23e11ea0c8d11200372`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:b23992f77c1f22e7bf9048641d6da1d6ef922d78b4118f6d513e183ae6de7e34 in / 
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
	-	`sha256:4873d96591a32d2d686ff6c86338fc9a63b9d60639482601b5402eb76e56a566`  
		Last Modified: Thu, 13 Jun 2024 01:02:22 GMT  
		Size: 26.6 MB (26594507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38b44c51ee1047daf831e46ae5c5d51ab0bb42e09a720bc2494af40a62b0e8a5`  
		Last Modified: Thu, 13 Jun 2024 11:25:33 GMT  
		Size: 4.3 MB (4286106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1a074d54bfff3b561913083eb215bd5f65bbb794a9f95250734413da02fae4c`  
		Last Modified: Thu, 13 Jun 2024 11:25:34 GMT  
		Size: 32.5 MB (32534764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08e0c3ada9a445e5493eadc340a0097258667b6c249b9ec950dd9545687d671c`  
		Last Modified: Thu, 13 Jun 2024 11:25:33 GMT  
		Size: 12.3 KB (12251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:661f5843759261a7047ba154588dd336e3d6561415a5860a5e24297b4af03c30`  
		Last Modified: Thu, 13 Jun 2024 11:25:33 GMT  
		Size: 11.9 KB (11911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1e34f4ae112ea0100db29d1348d379ae29dd6a9c8e50d13c3ed2a26c3c5175f`  
		Last Modified: Thu, 13 Jun 2024 11:25:34 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:7cce967027f5ef040a5bfd642ee75418d62ce37a267f3134ba86212318358701
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2932870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:710f6a30bdc8189d94d8503246650ab0383af609099a64b653ba125b30aed718`

```dockerfile
```

-	Layers:
	-	`sha256:2838fb4151efe572aff1b000c48fb89f6b70eeed955a8bda2dfb3bb3506238bf`  
		Last Modified: Thu, 13 Jun 2024 11:25:33 GMT  
		Size: 2.9 MB (2917180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b742368182d39ce403a01c97059fcebd519d6bbd3d64139595e651fd7a516f94`  
		Last Modified: Thu, 13 Jun 2024 11:25:32 GMT  
		Size: 15.7 KB (15690 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.8.10` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:91aae5d8912885c88287b065515265162286007c187c648361ed8b47cc99f3f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.5 MB (67544910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6d7a5d74734ac0e44525de668af66d1c8a820511af4d2e35028e5d5de72473b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:55edb70d595bba9782144ef15994a2ae5c40adeb65f6c3acd6570a0c148ffa96 in / 
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
	-	`sha256:ca4da1869379178993d4f7abc946f75e7515789ff7e15c7ccfedfc8e2bfeaf6d`  
		Last Modified: Thu, 13 Jun 2024 00:43:54 GMT  
		Size: 30.1 MB (30086973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e198db4c78d05a7fae6481f1f23e9abd0f4bd589e25e5b4afa53b8cb416bbfc7`  
		Last Modified: Thu, 13 Jun 2024 10:39:04 GMT  
		Size: 5.0 MB (5004108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0299cfd86fa3f79a7004d1cce8b56dde224addfbd665488e4ca70acc75d20470`  
		Last Modified: Thu, 13 Jun 2024 10:39:05 GMT  
		Size: 32.4 MB (32429432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:352c9608ddcf2ce9b44f0b0aaf9a71dbf0a7d9d83dd4c946e20c4bb07a21ce7c`  
		Last Modified: Thu, 13 Jun 2024 10:39:04 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ebdc4ba22b8ea39106433506e2f36daae588229d50644f58ff2347feaa7bdc3`  
		Last Modified: Thu, 13 Jun 2024 10:39:04 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f74e98413252a072b47934a947e3ff659675761a772b2098a242888f8876feaf`  
		Last Modified: Thu, 13 Jun 2024 10:39:05 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:f84cd02a12ebfbf384a8f5228f5a9bb7e90f0d010b65917008dc506c8d61e53a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2931066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d6c2de8e3269574d9287fcc9e73e6428b5b977210e3fa490bbc7b86f5c033be`

```dockerfile
```

-	Layers:
	-	`sha256:6d9f8b4d656f1021b4fc951ad5021fd727a0f2d9868dc178776008ea2e8d2588`  
		Last Modified: Thu, 13 Jun 2024 10:39:04 GMT  
		Size: 2.9 MB (2915158 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:669b39bb1e5a6a4645a76705f6123148de76ad978dc395af0a5542509ae8f98f`  
		Last Modified: Thu, 13 Jun 2024 10:39:04 GMT  
		Size: 15.9 KB (15908 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.8.10-alpine`

```console
$ docker pull chronograf@sha256:aeff6b0f33ad0c7163d0f15359676e3783b2c4f051277623bb87d3d8f525245b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.8.10-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:6901af16d25884590ef18c7cf6bc51e247e34e8db598d51aeac3a32686b96281
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23143191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fabb3a35dd209be242515d9abdb28872c03b6087716da9e68d7144ced10310b9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
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
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7135375e7e2b93794abc3a6fae771e0e810f1c985d87d5e2b116928c4a5811bb`  
		Last Modified: Mon, 03 Jun 2024 19:00:15 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7604efdcdfb5e914425082e913fa11feebc46f84efbd0eab4d63c026755d79f1`  
		Last Modified: Mon, 03 Jun 2024 19:00:14 GMT  
		Size: 292.4 KB (292422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed08262353aa43a044b72561106caeca51305919dbb951ad7fe4acfc2ad372f0`  
		Last Modified: Mon, 03 Jun 2024 19:00:15 GMT  
		Size: 19.2 MB (19204026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c69cc0629a8f4b4b5775f08d6212e7252bb99bc8b01e1d779a5306d8ce594551`  
		Last Modified: Mon, 03 Jun 2024 19:00:14 GMT  
		Size: 12.2 KB (12236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36c2b2e66b9548a4f932659927715ec1cabc2c5dd4425dd03f2b7185209ba8b9`  
		Last Modified: Mon, 03 Jun 2024 19:00:16 GMT  
		Size: 11.9 KB (11896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0910d626bd5a2723486bd6566ee32668ae861e7a1e18975ac98825605fefe14`  
		Last Modified: Mon, 03 Jun 2024 19:00:16 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8.10-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:e509b26098019dd58f191c86c4a74dae8e741425f72ae6bf2db1768e4eb80d54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.5 KB (233529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2a1345abbc1eb7303aad85d664a52c2b91b5a286113333875fd693f733f01db`

```dockerfile
```

-	Layers:
	-	`sha256:15f8d2f11400eec69f6ea0110c8ae1da088d7809dc0222f8354511b1bcef6a8a`  
		Last Modified: Mon, 03 Jun 2024 19:00:14 GMT  
		Size: 216.9 KB (216881 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f7394674c01a304ac4ca09c635793f21386d3fff6e6fe7b304eea2650beae68`  
		Last Modified: Mon, 03 Jun 2024 19:00:14 GMT  
		Size: 16.6 KB (16648 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.9`

```console
$ docker pull chronograf@sha256:22a13862c8577dcc95d400c9709bac87bd49b0fa977e0ec60f6e0f876a1f9f9f
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
$ docker pull chronograf@sha256:d48dd5bb50d4ac61a8b59ebecf668ea1e2feeaacf7343244281da6ea1bc7335c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.5 MB (71490896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a39c95a93e60665df72ede9e81e772774df1f15ffb4eb658180d3b55d7979c32`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 14 May 2024 01:28:26 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
# Tue, 14 May 2024 01:28:27 GMT
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
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eebde8aef47f19c2494521f6728f1d46879b6d43cc65c98827665512e07d7180`  
		Last Modified: Mon, 03 Jun 2024 19:00:13 GMT  
		Size: 5.0 MB (5020989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e00d912bf834c33d1afc737541a1cf76b9081506517f1774f458d466e9ffc41`  
		Last Modified: Mon, 03 Jun 2024 19:00:14 GMT  
		Size: 35.0 MB (35011583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3eeecadf719e9963e96d74f691ceb64b4c1418f9fa747e119400c95abbe54fd`  
		Last Modified: Mon, 03 Jun 2024 19:00:13 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bb454410615e0774b4d45e276e61b6a3649df6671e61f1100e9e0f88b65090f`  
		Last Modified: Mon, 03 Jun 2024 19:00:13 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0dac812eb9441ab765eebaf54b6f990739097b38a7a8db888fee7eca4fea90c`  
		Last Modified: Mon, 03 Jun 2024 19:00:14 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9` - unknown; unknown

```console
$ docker pull chronograf@sha256:1a9f8f1cf63e156075b712b5fe0373693141e173dab5583b67edf0fd2e4610fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2934769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39d13481ad5f3aab793a30c5d6246a30614b6001ce2d98dbb2dbc149cabe306c`

```dockerfile
```

-	Layers:
	-	`sha256:902412b236e167bec25d36685579a7b81c96b4212b9ffe387674035c30fad596`  
		Last Modified: Mon, 03 Jun 2024 19:00:14 GMT  
		Size: 2.9 MB (2919202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61b704bbc2e583a9902028f29d0d69c9847f70e6a0150bc24a5415afb378d31b`  
		Last Modified: Mon, 03 Jun 2024 19:00:13 GMT  
		Size: 15.6 KB (15567 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.9` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:1504146f699f7ccd0824416b630cf0f59802b6e14ebfcd213960e886925c3ed4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.2 MB (64216442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:823b761c00e0cbef419678a52e7d8a968c2c00406bda12b6a4225eca2ede81b8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:b23992f77c1f22e7bf9048641d6da1d6ef922d78b4118f6d513e183ae6de7e34 in / 
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
	-	`sha256:4873d96591a32d2d686ff6c86338fc9a63b9d60639482601b5402eb76e56a566`  
		Last Modified: Thu, 13 Jun 2024 01:02:22 GMT  
		Size: 26.6 MB (26594507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38b44c51ee1047daf831e46ae5c5d51ab0bb42e09a720bc2494af40a62b0e8a5`  
		Last Modified: Thu, 13 Jun 2024 11:25:33 GMT  
		Size: 4.3 MB (4286106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d76d528dd9ea9ae7a620d86301591b180f45985711ebbb9e3ee3b78e7d0b25ed`  
		Last Modified: Thu, 13 Jun 2024 11:30:53 GMT  
		Size: 33.3 MB (33311433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40c8eda98b3ca216d5126aaca47eb20d57e973be7b811129a229ee0bd7f817ef`  
		Last Modified: Thu, 13 Jun 2024 11:30:52 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4af81bf7f69722b29c06bdd1b598d5d7fbc3a1c484f36a5a7f3253edd5d97be9`  
		Last Modified: Thu, 13 Jun 2024 11:30:52 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2173aefa897643b83859935c7e50e6354e3ffc4105d92d93bb54ad48df932ad1`  
		Last Modified: Thu, 13 Jun 2024 11:30:52 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9` - unknown; unknown

```console
$ docker pull chronograf@sha256:8c96562b8cfa0aee6fdf64c25d9992cf732dd60531fafc46a6a02383660e499e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2937155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55e10ad9156cd1bd3db8ef076020687763951101eaf19e8fad3b2d4f14429630`

```dockerfile
```

-	Layers:
	-	`sha256:4274baf8e7b9ee106f19305bb7504a8209c43b644428e12e53b60d7b0ee009de`  
		Last Modified: Thu, 13 Jun 2024 11:30:52 GMT  
		Size: 2.9 MB (2921472 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bbb3caf41164fa9c291fe5d6406c94093292633469168685a7a8dcfe82908b3f`  
		Last Modified: Thu, 13 Jun 2024 11:30:52 GMT  
		Size: 15.7 KB (15683 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.9` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:6e8c68703b2c32c0caa49fca9a178c1b1570fc83f02d4983afda43ef05187cf6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.3 MB (68296970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2383c1504df2d6569fca6055e53ec08b06e23f454c5b375c7ebed93ac65d7c6b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:55edb70d595bba9782144ef15994a2ae5c40adeb65f6c3acd6570a0c148ffa96 in / 
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
	-	`sha256:ca4da1869379178993d4f7abc946f75e7515789ff7e15c7ccfedfc8e2bfeaf6d`  
		Last Modified: Thu, 13 Jun 2024 00:43:54 GMT  
		Size: 30.1 MB (30086973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e198db4c78d05a7fae6481f1f23e9abd0f4bd589e25e5b4afa53b8cb416bbfc7`  
		Last Modified: Thu, 13 Jun 2024 10:39:04 GMT  
		Size: 5.0 MB (5004108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5ad92281f32fe70c0311ce7ed3f7acd1741c8032fde27cbc16f94a5c38d565f`  
		Last Modified: Thu, 13 Jun 2024 10:55:38 GMT  
		Size: 33.2 MB (33181496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da50fde1cce334f6a1ad1711bb3d87397a8080057f40cf3f96350391baf652ca`  
		Last Modified: Thu, 13 Jun 2024 10:55:36 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3509692559eedcda3f2b71b87c4c102ab3f01cb0cace7bf32e1a47a4eef43a2`  
		Last Modified: Thu, 13 Jun 2024 10:55:37 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ac4d965d75fd56f4d880446b398e9a6070d38f4b50bbd1e7407d4967eeb618`  
		Last Modified: Thu, 13 Jun 2024 10:55:37 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9` - unknown; unknown

```console
$ docker pull chronograf@sha256:f51c3c268b6054fba5a9c1d7b5f3b873174ec5faae2d43bc933de2f8139a39ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2935351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e5af6a49938dd2a8df3b0af59b7ce70e798dd386349119c683868194949f96c`

```dockerfile
```

-	Layers:
	-	`sha256:f2d7394ca425fefa0fc2285f002417e4488e41a44e6be35d3d56e63eede1491d`  
		Last Modified: Thu, 13 Jun 2024 10:55:37 GMT  
		Size: 2.9 MB (2919450 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:417534c734d87b40b3a2af7e2151653dad429ec2863595e87e5230bdb8e55eea`  
		Last Modified: Thu, 13 Jun 2024 10:55:36 GMT  
		Size: 15.9 KB (15901 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.9-alpine`

```console
$ docker pull chronograf@sha256:4b387cd5abb5c4edf5ff7f449886c0b639d79aea15126cd2803af5273be66311
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.9-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:b024857b0a53699ca0cad01569dea1afa1611459ac1b391db87f766880e3f118
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23611241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7614fb2d6f19684100cbd8399c97243cfc34d1726acb7d1a377821d9db961936`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
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
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec4b899bd7765ff7f024156013a60645642a8d8410290dd6b529e9f936235eb5`  
		Last Modified: Mon, 03 Jun 2024 19:00:01 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6c47b68fae599b34128310d83189330caf17d6e6fdfcc1cacbdd32267e0ae42`  
		Last Modified: Mon, 03 Jun 2024 19:00:01 GMT  
		Size: 292.4 KB (292430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41685855cc4143b0f365fc5044bdf6223bff2af6dc57c216fcef4a95b50b01ef`  
		Last Modified: Mon, 03 Jun 2024 19:00:01 GMT  
		Size: 19.7 MB (19672068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73e45b2a86e01d139c7d17f449fa1384f1e526e2edde32d57bd93c0a1f4eccff`  
		Last Modified: Mon, 03 Jun 2024 19:00:01 GMT  
		Size: 12.2 KB (12237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2ecf24fc9eb6f8609cefdd0b3052ce939f62a8fdb02ba99938d5c002b59c9cf`  
		Last Modified: Mon, 03 Jun 2024 19:00:02 GMT  
		Size: 11.9 KB (11895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450b96b549cc85c4e767722042711a38adf3c74af9d3ce9e9e979c7a3d272dca`  
		Last Modified: Mon, 03 Jun 2024 19:00:02 GMT  
		Size: 237.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:9a13b6067af2556aa442e647412bccffdff3b8cea9a45074dea4db6ee1bc064d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.8 KB (237820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b1a49d5661190b467bd3d435f136d258f21a63140cb24416d434a0d47db09f4`

```dockerfile
```

-	Layers:
	-	`sha256:e1ecf37f9c69a9603213851b2aa836e8ab0c2b20d7598093c6e0090e83c8c1e3`  
		Last Modified: Mon, 03 Jun 2024 19:00:01 GMT  
		Size: 221.2 KB (221175 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:336e29c57bb46d2b50c1ddbae6313a58fa48f48b52d575c8731648e2925c181a`  
		Last Modified: Mon, 03 Jun 2024 19:00:01 GMT  
		Size: 16.6 KB (16645 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.9.4`

```console
$ docker pull chronograf@sha256:22a13862c8577dcc95d400c9709bac87bd49b0fa977e0ec60f6e0f876a1f9f9f
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
$ docker pull chronograf@sha256:d48dd5bb50d4ac61a8b59ebecf668ea1e2feeaacf7343244281da6ea1bc7335c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.5 MB (71490896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a39c95a93e60665df72ede9e81e772774df1f15ffb4eb658180d3b55d7979c32`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 14 May 2024 01:28:26 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
# Tue, 14 May 2024 01:28:27 GMT
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
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eebde8aef47f19c2494521f6728f1d46879b6d43cc65c98827665512e07d7180`  
		Last Modified: Mon, 03 Jun 2024 19:00:13 GMT  
		Size: 5.0 MB (5020989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e00d912bf834c33d1afc737541a1cf76b9081506517f1774f458d466e9ffc41`  
		Last Modified: Mon, 03 Jun 2024 19:00:14 GMT  
		Size: 35.0 MB (35011583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3eeecadf719e9963e96d74f691ceb64b4c1418f9fa747e119400c95abbe54fd`  
		Last Modified: Mon, 03 Jun 2024 19:00:13 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bb454410615e0774b4d45e276e61b6a3649df6671e61f1100e9e0f88b65090f`  
		Last Modified: Mon, 03 Jun 2024 19:00:13 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0dac812eb9441ab765eebaf54b6f990739097b38a7a8db888fee7eca4fea90c`  
		Last Modified: Mon, 03 Jun 2024 19:00:14 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9.4` - unknown; unknown

```console
$ docker pull chronograf@sha256:1a9f8f1cf63e156075b712b5fe0373693141e173dab5583b67edf0fd2e4610fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2934769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39d13481ad5f3aab793a30c5d6246a30614b6001ce2d98dbb2dbc149cabe306c`

```dockerfile
```

-	Layers:
	-	`sha256:902412b236e167bec25d36685579a7b81c96b4212b9ffe387674035c30fad596`  
		Last Modified: Mon, 03 Jun 2024 19:00:14 GMT  
		Size: 2.9 MB (2919202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61b704bbc2e583a9902028f29d0d69c9847f70e6a0150bc24a5415afb378d31b`  
		Last Modified: Mon, 03 Jun 2024 19:00:13 GMT  
		Size: 15.6 KB (15567 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.9.4` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:1504146f699f7ccd0824416b630cf0f59802b6e14ebfcd213960e886925c3ed4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.2 MB (64216442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:823b761c00e0cbef419678a52e7d8a968c2c00406bda12b6a4225eca2ede81b8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:b23992f77c1f22e7bf9048641d6da1d6ef922d78b4118f6d513e183ae6de7e34 in / 
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
	-	`sha256:4873d96591a32d2d686ff6c86338fc9a63b9d60639482601b5402eb76e56a566`  
		Last Modified: Thu, 13 Jun 2024 01:02:22 GMT  
		Size: 26.6 MB (26594507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38b44c51ee1047daf831e46ae5c5d51ab0bb42e09a720bc2494af40a62b0e8a5`  
		Last Modified: Thu, 13 Jun 2024 11:25:33 GMT  
		Size: 4.3 MB (4286106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d76d528dd9ea9ae7a620d86301591b180f45985711ebbb9e3ee3b78e7d0b25ed`  
		Last Modified: Thu, 13 Jun 2024 11:30:53 GMT  
		Size: 33.3 MB (33311433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40c8eda98b3ca216d5126aaca47eb20d57e973be7b811129a229ee0bd7f817ef`  
		Last Modified: Thu, 13 Jun 2024 11:30:52 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4af81bf7f69722b29c06bdd1b598d5d7fbc3a1c484f36a5a7f3253edd5d97be9`  
		Last Modified: Thu, 13 Jun 2024 11:30:52 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2173aefa897643b83859935c7e50e6354e3ffc4105d92d93bb54ad48df932ad1`  
		Last Modified: Thu, 13 Jun 2024 11:30:52 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9.4` - unknown; unknown

```console
$ docker pull chronograf@sha256:8c96562b8cfa0aee6fdf64c25d9992cf732dd60531fafc46a6a02383660e499e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2937155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55e10ad9156cd1bd3db8ef076020687763951101eaf19e8fad3b2d4f14429630`

```dockerfile
```

-	Layers:
	-	`sha256:4274baf8e7b9ee106f19305bb7504a8209c43b644428e12e53b60d7b0ee009de`  
		Last Modified: Thu, 13 Jun 2024 11:30:52 GMT  
		Size: 2.9 MB (2921472 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bbb3caf41164fa9c291fe5d6406c94093292633469168685a7a8dcfe82908b3f`  
		Last Modified: Thu, 13 Jun 2024 11:30:52 GMT  
		Size: 15.7 KB (15683 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.9.4` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:6e8c68703b2c32c0caa49fca9a178c1b1570fc83f02d4983afda43ef05187cf6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.3 MB (68296970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2383c1504df2d6569fca6055e53ec08b06e23f454c5b375c7ebed93ac65d7c6b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:55edb70d595bba9782144ef15994a2ae5c40adeb65f6c3acd6570a0c148ffa96 in / 
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
	-	`sha256:ca4da1869379178993d4f7abc946f75e7515789ff7e15c7ccfedfc8e2bfeaf6d`  
		Last Modified: Thu, 13 Jun 2024 00:43:54 GMT  
		Size: 30.1 MB (30086973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e198db4c78d05a7fae6481f1f23e9abd0f4bd589e25e5b4afa53b8cb416bbfc7`  
		Last Modified: Thu, 13 Jun 2024 10:39:04 GMT  
		Size: 5.0 MB (5004108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5ad92281f32fe70c0311ce7ed3f7acd1741c8032fde27cbc16f94a5c38d565f`  
		Last Modified: Thu, 13 Jun 2024 10:55:38 GMT  
		Size: 33.2 MB (33181496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da50fde1cce334f6a1ad1711bb3d87397a8080057f40cf3f96350391baf652ca`  
		Last Modified: Thu, 13 Jun 2024 10:55:36 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3509692559eedcda3f2b71b87c4c102ab3f01cb0cace7bf32e1a47a4eef43a2`  
		Last Modified: Thu, 13 Jun 2024 10:55:37 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ac4d965d75fd56f4d880446b398e9a6070d38f4b50bbd1e7407d4967eeb618`  
		Last Modified: Thu, 13 Jun 2024 10:55:37 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9.4` - unknown; unknown

```console
$ docker pull chronograf@sha256:f51c3c268b6054fba5a9c1d7b5f3b873174ec5faae2d43bc933de2f8139a39ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2935351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e5af6a49938dd2a8df3b0af59b7ce70e798dd386349119c683868194949f96c`

```dockerfile
```

-	Layers:
	-	`sha256:f2d7394ca425fefa0fc2285f002417e4488e41a44e6be35d3d56e63eede1491d`  
		Last Modified: Thu, 13 Jun 2024 10:55:37 GMT  
		Size: 2.9 MB (2919450 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:417534c734d87b40b3a2af7e2151653dad429ec2863595e87e5230bdb8e55eea`  
		Last Modified: Thu, 13 Jun 2024 10:55:36 GMT  
		Size: 15.9 KB (15901 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.9.4-alpine`

```console
$ docker pull chronograf@sha256:4b387cd5abb5c4edf5ff7f449886c0b639d79aea15126cd2803af5273be66311
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.9.4-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:b024857b0a53699ca0cad01569dea1afa1611459ac1b391db87f766880e3f118
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23611241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7614fb2d6f19684100cbd8399c97243cfc34d1726acb7d1a377821d9db961936`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
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
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec4b899bd7765ff7f024156013a60645642a8d8410290dd6b529e9f936235eb5`  
		Last Modified: Mon, 03 Jun 2024 19:00:01 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6c47b68fae599b34128310d83189330caf17d6e6fdfcc1cacbdd32267e0ae42`  
		Last Modified: Mon, 03 Jun 2024 19:00:01 GMT  
		Size: 292.4 KB (292430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41685855cc4143b0f365fc5044bdf6223bff2af6dc57c216fcef4a95b50b01ef`  
		Last Modified: Mon, 03 Jun 2024 19:00:01 GMT  
		Size: 19.7 MB (19672068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73e45b2a86e01d139c7d17f449fa1384f1e526e2edde32d57bd93c0a1f4eccff`  
		Last Modified: Mon, 03 Jun 2024 19:00:01 GMT  
		Size: 12.2 KB (12237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2ecf24fc9eb6f8609cefdd0b3052ce939f62a8fdb02ba99938d5c002b59c9cf`  
		Last Modified: Mon, 03 Jun 2024 19:00:02 GMT  
		Size: 11.9 KB (11895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450b96b549cc85c4e767722042711a38adf3c74af9d3ce9e9e979c7a3d272dca`  
		Last Modified: Mon, 03 Jun 2024 19:00:02 GMT  
		Size: 237.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9.4-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:9a13b6067af2556aa442e647412bccffdff3b8cea9a45074dea4db6ee1bc064d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.8 KB (237820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b1a49d5661190b467bd3d435f136d258f21a63140cb24416d434a0d47db09f4`

```dockerfile
```

-	Layers:
	-	`sha256:e1ecf37f9c69a9603213851b2aa836e8ab0c2b20d7598093c6e0090e83c8c1e3`  
		Last Modified: Mon, 03 Jun 2024 19:00:01 GMT  
		Size: 221.2 KB (221175 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:336e29c57bb46d2b50c1ddbae6313a58fa48f48b52d575c8731648e2925c181a`  
		Last Modified: Mon, 03 Jun 2024 19:00:01 GMT  
		Size: 16.6 KB (16645 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:alpine`

```console
$ docker pull chronograf@sha256:0a4afb73e2d3a91a06e36601c0b8c9c18e5aeb825e8edcceb9d18e338a0e0203
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:b55598a8b3ee7feb689bcb380dc0f234d328f2eb47c881346dc30b481bb81f1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31807875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b40200ab7f22ab99c0b92e31ce0a9ef862bfd80a2efa3813ebad5e2bdf598f9b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
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
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a541091e90e8b5010bc3e6964324ac4919c24be8f5fb5653082302eec5fc1ec4`  
		Last Modified: Mon, 03 Jun 2024 19:00:15 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d70bae9f6b1c0feca8cb0ba973e7e28953ffa5a9d62cfbfcd897abd2d016af8`  
		Last Modified: Mon, 03 Jun 2024 19:00:16 GMT  
		Size: 294.3 KB (294348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27b085bda50e0c5e25c7a4ebec7e1ccd7ae22a5c76ef00439f8b7c4d022b38fb`  
		Last Modified: Mon, 03 Jun 2024 19:00:16 GMT  
		Size: 27.9 MB (27866729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1990a674718757fef7810e42e4c5340c248ad43f1d9abdec7439e5b9cd01723`  
		Last Modified: Mon, 03 Jun 2024 19:00:15 GMT  
		Size: 12.2 KB (12237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14e68549b54b63067c056976b55d6c93ac1866dcad3a2e1dde832662e2da39f8`  
		Last Modified: Mon, 03 Jun 2024 19:00:16 GMT  
		Size: 11.9 KB (11896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9edb80f2e5c4143929355c91c8f989dafdbea5bce4a5e2c628198ab81d0e456e`  
		Last Modified: Mon, 03 Jun 2024 19:00:16 GMT  
		Size: 292.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:27b4cb11ebf88b4475e41a68de08386fcb61342e61fff5f48ad3b929f482634f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.5 KB (244494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65197df914a82b3f2f03ba701ae27857bf44eff66c30c4cf0b573d7eda631965`

```dockerfile
```

-	Layers:
	-	`sha256:ca5768a37193228f1c8c19dcb7236caefe2d82d164db3e45a19eea54e191d717`  
		Last Modified: Mon, 03 Jun 2024 19:00:15 GMT  
		Size: 226.9 KB (226903 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe809aec848a51e9dedbd725ce359b20a0efb4f28696cc4188181514e5202eac`  
		Last Modified: Mon, 03 Jun 2024 19:00:15 GMT  
		Size: 17.6 KB (17591 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:latest`

```console
$ docker pull chronograf@sha256:d892b3beb2e87e15a7bf775fa81b3e3898f59593127f1298f7ffcc1c6ef7c84c
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
$ docker pull chronograf@sha256:5f5537b449b3f8035637e4ce9eb6d4720ced46f8db9d4e2c13c95be6f1ac7be9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.1 MB (84069434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45996034df2c6fe446e5e2fd0aa29d585534c107ab461bba710b9e9e2a59446d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 14 May 2024 01:28:03 GMT
ADD file:5aaace706aa00ff97d243daa2c29f5de88f124e1b97c570634f16eef90783286 in / 
# Tue, 14 May 2024 01:28:04 GMT
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
	-	`sha256:09f376ebb190216b0459f470e71bec7b5dfa611d66bf008492b40dcc5f1d8eae`  
		Last Modified: Tue, 14 May 2024 01:32:30 GMT  
		Size: 29.2 MB (29150411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8f47b768815e9c2366c46a8534a57f09e4f6f0ff4b0b52b64ba601dc9a9c174`  
		Last Modified: Mon, 03 Jun 2024 19:00:29 GMT  
		Size: 7.7 MB (7676940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9489fbf683135fcfa140c8d0a17e9d550c173fc3a052bc84f9f267f99252cf48`  
		Last Modified: Mon, 03 Jun 2024 19:00:31 GMT  
		Size: 47.2 MB (47217627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ed019f6b0534dfea3bfb7a969d8574f9df636506f6f19524b92326e37d2ada2`  
		Last Modified: Mon, 03 Jun 2024 19:00:28 GMT  
		Size: 12.2 KB (12241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb7ab6f5f28a95f1a3f7d8c842fdfc39c48d986d7d2fc301067f3717612a58d4`  
		Last Modified: Mon, 03 Jun 2024 19:00:28 GMT  
		Size: 11.9 KB (11900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af934b4bf874818dedfe49e86bee37a24e98cfb0e261bef354508666419f1249`  
		Last Modified: Mon, 03 Jun 2024 19:00:30 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:c109af0e26df5eea8f474e65c0139dbb1f2441db69a8534d6e4d0c20f1eebaa6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2671399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d7cf432a9a5718d9f6b2250ab83415c141962d8a0deb4e8a169e459aff78d57`

```dockerfile
```

-	Layers:
	-	`sha256:c3d8929c831b697a62dc9682fd7ae7044d6cd8342004667d41fd27a573432ef3`  
		Last Modified: Mon, 03 Jun 2024 19:00:29 GMT  
		Size: 2.7 MB (2655514 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3661947447bdb2d0b40fbad7fa348a99abb8e7e835a3351efddc4c57262a0019`  
		Last Modified: Mon, 03 Jun 2024 19:00:28 GMT  
		Size: 15.9 KB (15885 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:latest` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:44faf726089000b60356258f9f7d98942577a8dc5aeb81222e3e19f45544bc44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.3 MB (75343499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:607c12abf0a6340e115ce9868d3b8c08e9e126e903c3b7255375c8e63b924d45`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:4c737c0a5e5b59fcbe2bc42dca815263159a1e1d16789ebeee086933aac4649a in / 
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
	-	`sha256:12af5edb53b85c10582c3e3d437561cc626437f48928a30456a99941d87706e3`  
		Last Modified: Thu, 13 Jun 2024 01:01:38 GMT  
		Size: 24.7 MB (24740215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75438d5f55c1596d5b71b0ff2de7f744bb89ef0e34e17f35b68bc5407fcdd25c`  
		Last Modified: Thu, 13 Jun 2024 11:32:08 GMT  
		Size: 6.3 MB (6301071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8abb520682775aaf2f92e765c274afa25f92e29c9b06447406bc30196ecc7bbc`  
		Last Modified: Thu, 13 Jun 2024 11:32:09 GMT  
		Size: 44.3 MB (44277740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b096b401a3f1861dc090a8ec1e2b4feaf49ccedac38fa2b1a64433c4f3420ab0`  
		Last Modified: Thu, 13 Jun 2024 11:32:07 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ab4535f77e97c81c5f28b6bb30afc0a83ffa2f442f4eaa7013e620809b7f93a`  
		Last Modified: Thu, 13 Jun 2024 11:32:08 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77a22d996d479e1f6829449de4179c0e10096d4d6385851e085b36a83c96838`  
		Last Modified: Thu, 13 Jun 2024 11:32:09 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:1443e3a29bba6c1446a91cf9601149e6ed12d20dc103f10ba2a56e6c0eba5437
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2673817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e7f4b8109398f8f54b12e17810dd5d145dfbef6df08bf2c38321d54cd3ce0bc`

```dockerfile
```

-	Layers:
	-	`sha256:925658867c31cec76fa2298b3c9e4098bfe049889801846102570d8fa6afdb1b`  
		Last Modified: Thu, 13 Jun 2024 11:32:08 GMT  
		Size: 2.7 MB (2657810 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44c0ad4f959c95f849adfcf72f39c5078b2f5c6d3ddb009f2536969bdc22f677`  
		Last Modified: Thu, 13 Jun 2024 11:32:07 GMT  
		Size: 16.0 KB (16007 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:latest` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:2509b79f21f8d2f01cc6fb1787c60e192cedbaa1c3a0df512f250cef530831b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.6 MB (81628369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa0abb98411db0e43a2472ca9a04e405f3988fda0221fc73309073c33d3f1e22`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:5f17f77072bcd27aa8c4d09ef5117423b789c42445b6e6c13af711dfb2abd544 in / 
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
	-	`sha256:559a764445207341cf1207d83ceb89f1e59e2b57e860b7a80a6df6447641832b`  
		Last Modified: Thu, 13 Jun 2024 00:43:13 GMT  
		Size: 29.2 MB (29179666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:190c44ee98f21bfee7c5d1f4a14f776fde4841c39b3768dd1ef9237f050a1c7e`  
		Last Modified: Thu, 13 Jun 2024 11:07:25 GMT  
		Size: 7.5 MB (7453190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1353d59f878028d1e53f5b9ba7ff5ffc15eba37b01f82eb05dd966d56edd38d`  
		Last Modified: Thu, 13 Jun 2024 11:07:27 GMT  
		Size: 45.0 MB (44971054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2acf276b9e8fbbd0dcc962675f697db83c1ae8c2bddaca1cb5c11c46971d74c7`  
		Last Modified: Thu, 13 Jun 2024 11:07:25 GMT  
		Size: 12.2 KB (12242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56e6dd95139e23cb8a4d10dad60fa476b92f5a9145a7dd7065456fe757ca3a31`  
		Last Modified: Thu, 13 Jun 2024 11:07:26 GMT  
		Size: 11.9 KB (11901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91708736b0c8e603f3424312a2afcaa5a538aa78627f508d8c4987f3ed15b722`  
		Last Modified: Thu, 13 Jun 2024 11:07:27 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:cd716da942a514ab19d44c83fa585a1630ed5119a82b7e3f88ebe30d0925a055
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2672016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1778fda725b4d6774f106bdc18c6d9b53fc21bdb277af9413e686b3ad5f1441`

```dockerfile
```

-	Layers:
	-	`sha256:f3e3f8f7212f21dc6670ffb3733e2c1980e6bc43ea569b9fd42cf0084277c5c9`  
		Last Modified: Thu, 13 Jun 2024 11:07:26 GMT  
		Size: 2.7 MB (2655786 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ecd3e10071bb448a595fd2dac1ecd5a65e785f3fad6449fd2bc71fbcbbe02612`  
		Last Modified: Thu, 13 Jun 2024 11:07:25 GMT  
		Size: 16.2 KB (16230 bytes)  
		MIME: application/vnd.in-toto+json
