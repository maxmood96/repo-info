<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `chronograf`

-	[`chronograf:1.10`](#chronograf110)
-	[`chronograf:1.10-alpine`](#chronograf110-alpine)
-	[`chronograf:1.10.7`](#chronograf1107)
-	[`chronograf:1.10.7-alpine`](#chronograf1107-alpine)
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
$ docker pull chronograf@sha256:07cba7b069e5ec7027d942b35a250358052174485c704f58aec1e2b4a7c3dcb9
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
$ docker pull chronograf@sha256:a5d5997fa575a11cbbd441528193b5078fea3221b6a6e5ea87598d4b28d1f0d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.6 MB (84581820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ecc21483ba8601581e9fde57391810fae4e11a9b6ca8f29c89c96ec401cfc0f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 17 Dec 2024 14:20:15 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
# Tue, 17 Dec 2024 14:20:15 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
ENV CHRONOGRAF_VERSION=1.10.6
# Tue, 17 Dec 2024 14:20:15 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 17 Dec 2024 14:20:15 GMT
VOLUME [/var/lib/chronograf]
# Tue, 17 Dec 2024 14:20:15 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Dec 2024 14:20:15 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:8a628cdd7ccc83e90e5a95888fcb0ec24b991141176c515ad101f12d6433eb96`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 28.2 MB (28227259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd5f7720f7246dde5561426d82d564eda3f7d36bb3a6670a3770bc88134d9db7`  
		Last Modified: Tue, 08 Apr 2025 01:24:50 GMT  
		Size: 7.9 MB (7875466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d937045b0d245509e6a15651490c28bbcf2ba34649a5e898a032e7b7b395fd30`  
		Last Modified: Tue, 08 Apr 2025 01:24:50 GMT  
		Size: 48.5 MB (48454620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea3ba974b6bb30cd12c43de5fc77a036818922515181202f95eb483d1a4d9b99`  
		Last Modified: Tue, 08 Apr 2025 01:24:49 GMT  
		Size: 12.3 KB (12251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb68d523da02175326435a308d4bda88e8185209a42f58bca62a8cb6b20fc266`  
		Last Modified: Tue, 08 Apr 2025 01:24:49 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab054931a65ce6eb03aaaea053ef5dc76ffde78efca071816c4fb4dcb34f499`  
		Last Modified: Tue, 08 Apr 2025 01:24:50 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:cd5a67855a871f08b9ea1c7c594e0ac0792e7ec64559b320cff680508cae2a7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2720301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:417c68170030f6ab0af55006508c3683fa3c6877eafa4678e99ef3c5cca621f8`

```dockerfile
```

-	Layers:
	-	`sha256:37053d94ba4f693d609b03ba15afb047eba84e57a85b148edc7b53982509d434`  
		Last Modified: Tue, 08 Apr 2025 01:24:49 GMT  
		Size: 2.7 MB (2704173 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a42a5cfa2b45c3d1c2e3a99db05f5fc6af7686c6c1a560928658d4207fdbf213`  
		Last Modified: Tue, 08 Apr 2025 01:24:49 GMT  
		Size: 16.1 KB (16128 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.10` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:079db0bd2d86f924708a5a9e6de6c2cb7d3399cf1699f557229137991509ac54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.3 MB (75344233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64a5aa6b6d812c629928d618bac6db5743606f7239a3a3a26aaad9013d7807ef`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 17 Dec 2024 14:20:15 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1743984000'
# Tue, 17 Dec 2024 14:20:15 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
ENV CHRONOGRAF_VERSION=1.10.6
# Tue, 17 Dec 2024 14:20:15 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 17 Dec 2024 14:20:15 GMT
VOLUME [/var/lib/chronograf]
# Tue, 17 Dec 2024 14:20:15 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Dec 2024 14:20:15 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:addc1be20d0979aa781d79a726ebf749adbc030186e63a44319274194e89cfa3`  
		Last Modified: Tue, 08 Apr 2025 00:23:15 GMT  
		Size: 23.9 MB (23937867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63a4cae4b4be11b615ad8d998f77262f16fb70375bec9f1790dc5e05cce9a5d4`  
		Last Modified: Tue, 08 Apr 2025 07:41:52 GMT  
		Size: 6.5 MB (6497876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ca6161fddf786d8012dd22432d04af6253ee18bf5410e706918e4de84897a3`  
		Last Modified: Tue, 08 Apr 2025 07:41:53 GMT  
		Size: 44.9 MB (44884033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb6d2e2d402730b3e47c70c7a8aabe0d0793ccf8eb0697f589f07e8d11c841be`  
		Last Modified: Tue, 08 Apr 2025 07:41:51 GMT  
		Size: 12.2 KB (12242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:791bbc1f7129cabc57b97efda40df8c58cc17296f8496c736de68e6aa6067c61`  
		Last Modified: Tue, 08 Apr 2025 07:41:52 GMT  
		Size: 11.9 KB (11900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f8db94257bbf594cc0bd3f1146569a9345620758022b6acfc42d15cd2507084`  
		Last Modified: Tue, 08 Apr 2025 07:41:52 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:9739812ff99a5b6697d386b42a97788bd24f1863f33aa2b651293d38893bb3fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2722679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80a8caa4b6b0ca8884ce0cbd8e9fa634519d744fe87bd92a071278e921b8e34a`

```dockerfile
```

-	Layers:
	-	`sha256:7d9aabb618915996af35c9036eff103c458b5b41627180a237317e736eb873da`  
		Last Modified: Tue, 08 Apr 2025 07:41:52 GMT  
		Size: 2.7 MB (2706470 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21f063817b819d3672d30970228e48a1f0fe85493751bb5fac5cd4df2f4cd441`  
		Last Modified: Tue, 08 Apr 2025 07:41:51 GMT  
		Size: 16.2 KB (16209 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.10` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:8d09faba86fbf271e53e98a9284de3d8208ce87338cf0859550d19201f57e982
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.0 MB (82026956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d1af4d2e6e170d6540fc4cf36fa34596f75e1266535d408024ebdfc38b6498d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 17 Dec 2024 14:20:15 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
# Tue, 17 Dec 2024 14:20:15 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
ENV CHRONOGRAF_VERSION=1.10.6
# Tue, 17 Dec 2024 14:20:15 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 17 Dec 2024 14:20:15 GMT
VOLUME [/var/lib/chronograf]
# Tue, 17 Dec 2024 14:20:15 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Dec 2024 14:20:15 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:16c9c4a8e9eef856231273efbb42a473740e8d50d74d35e6aedd04ff69fe161f`  
		Last Modified: Tue, 08 Apr 2025 00:23:04 GMT  
		Size: 28.1 MB (28066320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a6bdd77a3e8191d60b227c9f755f6f8f4b05034647007a07c82c1f6e4e88fd5`  
		Last Modified: Tue, 08 Apr 2025 06:06:40 GMT  
		Size: 7.7 MB (7652075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8259506abfecb0d9cefbd5da4e67b42720a246f8ee84521a7debe53fd757ba9`  
		Last Modified: Tue, 08 Apr 2025 06:06:41 GMT  
		Size: 46.3 MB (46284096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b303ae82d885113e78bb9e74c59a3e208975cc6de99b17cdda23c65c431f17cf`  
		Last Modified: Tue, 08 Apr 2025 06:06:39 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95d00ef9f739ada971c5ff08863c9ae4b2a5dd0fb640b56931da3efe57697831`  
		Last Modified: Tue, 08 Apr 2025 06:06:39 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8236a193f0c09a8aa82a0a8535f11cd23a4896d4e7607979e84f340192e25fa4`  
		Last Modified: Tue, 08 Apr 2025 06:06:40 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:89e855ac93e95ac2c414f1c7ba3731319ed22a82629cdb1a16686f71650629b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2720681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaffee6edec55303d2718b0134fe372c5e802220e816f225534996bcc0d9d0b4`

```dockerfile
```

-	Layers:
	-	`sha256:53bb146925fab3e7f4222f9293b00b8f7b9a918a381581d8818f36045f7b13b4`  
		Last Modified: Tue, 08 Apr 2025 06:06:40 GMT  
		Size: 2.7 MB (2704446 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:390ca5bb55650e1e1291992921fd0e2cad9783ef561abcb28b2d5e1c9dde57a5`  
		Last Modified: Tue, 08 Apr 2025 06:06:39 GMT  
		Size: 16.2 KB (16235 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.10-alpine`

```console
$ docker pull chronograf@sha256:357a021d3cd126c613abc52fc98c9065a2fb48f483032a725626baaa2761e3b4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.10-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:710e6bdd8c753ac12bc419bdc1cf4cedb0b554d8709fd762b307ddb4ff224659
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32156068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35ce1017cc5643e1a718b3830f3cf365a93c39b40189a9be172b575352a94374`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 17 Dec 2024 14:20:15 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
CMD ["/bin/sh"]
# Tue, 17 Dec 2024 14:20:15 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
RUN apk add --no-cache ca-certificates su-exec &&     update-ca-certificates # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
ENV CHRONOGRAF_VERSION=1.10.6
# Tue, 17 Dec 2024 14:20:15 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S chronograf &&     adduser -S chronograf -G chronograf &&     mkdir -m 0750 -p /var/lib/chronograf &&     chown chronograf:chronograf /var/lib/chronograf # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 17 Dec 2024 14:20:15 GMT
VOLUME [/var/lib/chronograf]
# Tue, 17 Dec 2024 14:20:15 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Dec 2024 14:20:15 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 12:05:36 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf00371f05d5b0928cf7ea0ada1dc3e28415f2be036fe5457e179bee6c9a23d4`  
		Last Modified: Mon, 24 Mar 2025 19:48:09 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c751720c18e7b8e894c53e3883a470d36188070073fe62c65a688cf3b065a238`  
		Last Modified: Mon, 24 Mar 2025 19:48:09 GMT  
		Size: 296.5 KB (296503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39366593367b5c31d595ef2671585706493373ae5c4cedaf022d6fa9fe81d502`  
		Last Modified: Mon, 24 Mar 2025 19:48:10 GMT  
		Size: 28.2 MB (28207965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:562bd300e80978e43bf12de6ba7c56811f6dfd92e79d94eaeaaa2224c7399f9d`  
		Last Modified: Mon, 24 Mar 2025 19:48:09 GMT  
		Size: 12.2 KB (12236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c15792c0d9c24edced73095648e9d68a08bf497c9243dce0b963b48c33814d70`  
		Last Modified: Mon, 24 Mar 2025 19:48:10 GMT  
		Size: 11.9 KB (11896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:019973f1fa061bc24fee856e1a9d0a0446bab0fa25d61bedf6c949584d5075ec`  
		Last Modified: Mon, 24 Mar 2025 19:48:10 GMT  
		Size: 292.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:90f7744b33302570f05e81ea60bd001215391027c10c0e8caf297ee94d6d1c7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.4 KB (259445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fc8eb620086f1de3306a8ded05948a19fb6a869e3f582032ce4ec8cc2758a71`

```dockerfile
```

-	Layers:
	-	`sha256:403f3626fe8060a52cb1b7dc3bf1a1d904541b71acbe11b5c100701b5a07d146`  
		Last Modified: Mon, 24 Mar 2025 19:48:09 GMT  
		Size: 241.6 KB (241591 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c8a546c4c466ea56cf10539a5a7edc0b8116bc37abc3c50063f85d03f979655`  
		Last Modified: Mon, 24 Mar 2025 19:48:09 GMT  
		Size: 17.9 KB (17854 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.10.7`

**does not exist** (yet?)

## `chronograf:1.10.7-alpine`

**does not exist** (yet?)

## `chronograf:1.7`

```console
$ docker pull chronograf@sha256:ce888f166555b7e13309a9a50df74e65871c89ddd7e9e4bf8f9afc80a2d39bc3
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
$ docker pull chronograf@sha256:4fb69119f8fc8fb688cd518a957846505f4827f1d107cfb68cfedaf28cb963d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.2 MB (69229845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad30e2bd7f538046ea540b87ea594a2f69ae4900005a702f018e788417c3ab23`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 17 Dec 2024 14:20:15 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1743984000'
# Tue, 17 Dec 2024 14:20:15 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 17 Dec 2024 14:20:15 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 17 Dec 2024 14:20:15 GMT
VOLUME [/var/lib/chronograf]
# Tue, 17 Dec 2024 14:20:15 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Dec 2024 14:20:15 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:b983e127c643116d446fa1b64216f464e1d06a8bfaeeb8a895c361c1bc3f5652`  
		Last Modified: Tue, 08 Apr 2025 00:23:09 GMT  
		Size: 30.3 MB (30257419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78d0dd2882f7ca577ef4903a60c0f5d4e4f407495874810342189540b5fe6b5c`  
		Last Modified: Tue, 08 Apr 2025 01:24:29 GMT  
		Size: 4.2 MB (4209382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a248644f16210f9906ee5dee5c21872a90bc77133e9878d20b63632cbd3a9ac5`  
		Last Modified: Tue, 08 Apr 2025 01:24:29 GMT  
		Size: 34.7 MB (34738645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24a961d4dc9d7d17319aad2301203df7cde34fa3645b1996e959bc707c70a92b`  
		Last Modified: Tue, 08 Apr 2025 01:24:29 GMT  
		Size: 12.3 KB (12251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78b810a5cd1d1a37a36835120bcc632753e228e4807d6df23f1e0e81add264fd`  
		Last Modified: Tue, 08 Apr 2025 01:24:29 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d38e8bc9f0a230083c9f83bdda48204454f48a2b7cde54ca4c4b30a23c4cdea5`  
		Last Modified: Tue, 08 Apr 2025 01:24:30 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7` - unknown; unknown

```console
$ docker pull chronograf@sha256:ed883aa7067ab7f7b187942201863b1505ea0cc351e077f74d597297ae000f28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2923080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16d061808a927641490041d9bd1bdc8d6fdf5144828b9fee9c1d87d38b1a24e3`

```dockerfile
```

-	Layers:
	-	`sha256:f16d3d5dd9174915d3dae06040319012d0102d2f2355b946c58c3effbef51cdf`  
		Last Modified: Tue, 08 Apr 2025 01:24:29 GMT  
		Size: 2.9 MB (2907303 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76c996d6de27823ef272eeabc63f7b9ecf71da65d46421d72d2a2103c12896c6`  
		Last Modified: Tue, 08 Apr 2025 01:24:29 GMT  
		Size: 15.8 KB (15777 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.7` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:55b05ecd6ac9ec307bed0721ebdc7939f8c465591096f59a8888d1de0145bce6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62172721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fea961b7c219f4311d2161bdd3fe70d741842e4e9221a93fa2c080337ea2654c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 17 Dec 2024 14:20:15 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1743984000'
# Tue, 17 Dec 2024 14:20:15 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 17 Dec 2024 14:20:15 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 17 Dec 2024 14:20:15 GMT
VOLUME [/var/lib/chronograf]
# Tue, 17 Dec 2024 14:20:15 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Dec 2024 14:20:15 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:bfc445187b87c4f640fe8b85c4ee3c251ce5e7023a5ff0acd053bde1f01e6aaf`  
		Last Modified: Tue, 08 Apr 2025 00:23:52 GMT  
		Size: 25.5 MB (25539135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1d14c78e9af4f52cf73c1b9c4b85220d72bad57e9c3f71fd942534213bb4bb0`  
		Last Modified: Tue, 08 Apr 2025 07:40:32 GMT  
		Size: 3.5 MB (3511703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6a68f8b0eff27951314444f787c5f7fb261f843fdef82c823a7ef9075e99bc2`  
		Last Modified: Tue, 08 Apr 2025 07:40:32 GMT  
		Size: 33.1 MB (33097486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67d6aeedb9e6e411b0a920b67f378446ea2c1d2f91539700339db32c921c81c4`  
		Last Modified: Tue, 08 Apr 2025 07:40:31 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5163651c84d3a13a704340c0ce489715f0faa863e48eeffde865a1154438eab`  
		Last Modified: Tue, 08 Apr 2025 07:40:31 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd268020c9ec09ff429f00b50cc325185c7dca189c543c47c0a208f149a6f8d5`  
		Last Modified: Tue, 08 Apr 2025 07:40:32 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7` - unknown; unknown

```console
$ docker pull chronograf@sha256:dc3daa045852fc37940f8a48a0745eaad3de38cfe5d21facfc4a703083a66845
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2925424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:138227f43e65edaedaae4e67dba714767663d75980f6fadfa3b12cb71a7ba03a`

```dockerfile
```

-	Layers:
	-	`sha256:d0375e574b8331d8ce78912e9c43e2ee53e35f32dfad6871059df6ac003e9506`  
		Last Modified: Tue, 08 Apr 2025 07:40:31 GMT  
		Size: 2.9 MB (2909574 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fdd26cfd1642657b1ff29199b16490e15213a678516faeef7603717c3c8a0901`  
		Last Modified: Tue, 08 Apr 2025 07:40:31 GMT  
		Size: 15.8 KB (15850 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.7` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:2ff525bc22e369edccc178ae64e3ef62bd883cec7b0c82666dd62cfb07ba05b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66222443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e4993891ccca3c03a428ea8d8f2c47da7eed477c3f0883d591c111c860600f0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 17 Dec 2024 14:20:15 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1743984000'
# Tue, 17 Dec 2024 14:20:15 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 17 Dec 2024 14:20:15 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 17 Dec 2024 14:20:15 GMT
VOLUME [/var/lib/chronograf]
# Tue, 17 Dec 2024 14:20:15 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Dec 2024 14:20:15 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:59627ca2e9712141a7d131bec6c9931f8ecea11eac34d96bd1213ccea68e18e5`  
		Last Modified: Tue, 08 Apr 2025 00:23:35 GMT  
		Size: 28.7 MB (28749498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f34c692a4ba55ec40062c62051436a12aaec0bf32d9e641edcaedec9b69f37a`  
		Last Modified: Tue, 08 Apr 2025 06:05:12 GMT  
		Size: 4.2 MB (4210644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e8443d8aaee9019ed461a4047652b1c8036146c2e07f17977d06a071febcf16`  
		Last Modified: Tue, 08 Apr 2025 06:05:12 GMT  
		Size: 33.2 MB (33237920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf081dc2c5584b0c7ff39fc577f613ecec3d71cedaa41739f750efa3bfc4012f`  
		Last Modified: Tue, 08 Apr 2025 06:05:11 GMT  
		Size: 12.2 KB (12242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a416b5388d2e8a9ade42d3402641a23922dd180928dde08ebba726f40cd6cd7`  
		Last Modified: Tue, 08 Apr 2025 06:05:11 GMT  
		Size: 11.9 KB (11900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22cfef9759938b46bdd87e3db06e225e6fa4ce4919c3e0b0b46a61b1aeaf0597`  
		Last Modified: Tue, 08 Apr 2025 06:05:12 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7` - unknown; unknown

```console
$ docker pull chronograf@sha256:e2cd81f211b2076ee9e7c4c31cde7d25cf645e9b22623c853012efbb51e6ec9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2923424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a51822590dc13c588c14875d2c3963ffac84c5e6ff2f543686ac666a66d2f2f9`

```dockerfile
```

-	Layers:
	-	`sha256:5d093599408be9ca787922bfe7cfcb0fb6541349c26f2a74c41d6d5528562ae6`  
		Last Modified: Tue, 08 Apr 2025 06:05:11 GMT  
		Size: 2.9 MB (2907552 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17aac24de39859317b140f81e79fad98ea275f45e4d5ff5802c7fa3834bfb7a1`  
		Last Modified: Tue, 08 Apr 2025 06:05:11 GMT  
		Size: 15.9 KB (15872 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.7-alpine`

```console
$ docker pull chronograf@sha256:df924b85652b1a3cf6ee401da68f4ef42a31256cd06244016ae21cec9f8952d0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.7-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:f033d37b112e959a0534de672abf91b9c3aa43535d685738ea85e838e904e8e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.5 MB (23502749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:137abfa83685c0597819295c4b3ef856c9395a461bd9bd70ff91ec3a4cd5921a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
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
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 12:05:36 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f8ae06deb09ed334ed8eba44b6e425cced470152dbdd9c0e3c6125578263f57`  
		Last Modified: Fri, 14 Feb 2025 19:24:48 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69641bcb67c77b895509abb75bf637ce2b76f0acdd981fd282b113d82c04c619`  
		Last Modified: Fri, 14 Feb 2025 19:24:48 GMT  
		Size: 294.4 KB (294383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1c71c1a03f44724b1796ddc3866d8fe5c4a5af8862448eabb7b2ebdc7a47748`  
		Last Modified: Fri, 14 Feb 2025 19:24:49 GMT  
		Size: 19.6 MB (19556823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f29450f6d74de26216b10dc587e69dd4443992a6aea3c7b424c7aaad08ceef29`  
		Last Modified: Fri, 14 Feb 2025 19:24:48 GMT  
		Size: 12.2 KB (12235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97e84d9f6956c08b6776f1b3db99e0226246d044677f2e4cf470051da809c34e`  
		Last Modified: Fri, 14 Feb 2025 19:24:49 GMT  
		Size: 11.9 KB (11893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:030349c6370852b4bfb957d5c0dc77ca8ab49cfd26485c0b053651d825d6caf9`  
		Last Modified: Fri, 14 Feb 2025 19:24:49 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:0c38d57135acbd91b733dbd02beff4e0339d76bf9f15f687bd8c4f5a2f887e91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.3 KB (189257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:471658777992e65c6b6d0f2da3225f4e41179e9be460d18106df6b906e69e00b`

```dockerfile
```

-	Layers:
	-	`sha256:6592097eed7dd5f5abfbbe36bb576489b44efd68487a9d4d946f1dc3e7aeac87`  
		Last Modified: Fri, 14 Feb 2025 19:24:48 GMT  
		Size: 172.3 KB (172345 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2af6f071245b63b559b430cac0c4aba0ef1cc49a72e9b52d3edae3f8b2d6ad95`  
		Last Modified: Fri, 14 Feb 2025 19:24:48 GMT  
		Size: 16.9 KB (16912 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.7.17`

```console
$ docker pull chronograf@sha256:ce888f166555b7e13309a9a50df74e65871c89ddd7e9e4bf8f9afc80a2d39bc3
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
$ docker pull chronograf@sha256:4fb69119f8fc8fb688cd518a957846505f4827f1d107cfb68cfedaf28cb963d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.2 MB (69229845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad30e2bd7f538046ea540b87ea594a2f69ae4900005a702f018e788417c3ab23`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 17 Dec 2024 14:20:15 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1743984000'
# Tue, 17 Dec 2024 14:20:15 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 17 Dec 2024 14:20:15 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 17 Dec 2024 14:20:15 GMT
VOLUME [/var/lib/chronograf]
# Tue, 17 Dec 2024 14:20:15 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Dec 2024 14:20:15 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:b983e127c643116d446fa1b64216f464e1d06a8bfaeeb8a895c361c1bc3f5652`  
		Last Modified: Tue, 08 Apr 2025 00:23:09 GMT  
		Size: 30.3 MB (30257419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78d0dd2882f7ca577ef4903a60c0f5d4e4f407495874810342189540b5fe6b5c`  
		Last Modified: Tue, 08 Apr 2025 01:24:29 GMT  
		Size: 4.2 MB (4209382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a248644f16210f9906ee5dee5c21872a90bc77133e9878d20b63632cbd3a9ac5`  
		Last Modified: Tue, 08 Apr 2025 01:24:29 GMT  
		Size: 34.7 MB (34738645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24a961d4dc9d7d17319aad2301203df7cde34fa3645b1996e959bc707c70a92b`  
		Last Modified: Tue, 08 Apr 2025 01:24:29 GMT  
		Size: 12.3 KB (12251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78b810a5cd1d1a37a36835120bcc632753e228e4807d6df23f1e0e81add264fd`  
		Last Modified: Tue, 08 Apr 2025 01:24:29 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d38e8bc9f0a230083c9f83bdda48204454f48a2b7cde54ca4c4b30a23c4cdea5`  
		Last Modified: Tue, 08 Apr 2025 01:24:30 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7.17` - unknown; unknown

```console
$ docker pull chronograf@sha256:ed883aa7067ab7f7b187942201863b1505ea0cc351e077f74d597297ae000f28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2923080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16d061808a927641490041d9bd1bdc8d6fdf5144828b9fee9c1d87d38b1a24e3`

```dockerfile
```

-	Layers:
	-	`sha256:f16d3d5dd9174915d3dae06040319012d0102d2f2355b946c58c3effbef51cdf`  
		Last Modified: Tue, 08 Apr 2025 01:24:29 GMT  
		Size: 2.9 MB (2907303 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76c996d6de27823ef272eeabc63f7b9ecf71da65d46421d72d2a2103c12896c6`  
		Last Modified: Tue, 08 Apr 2025 01:24:29 GMT  
		Size: 15.8 KB (15777 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.7.17` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:55b05ecd6ac9ec307bed0721ebdc7939f8c465591096f59a8888d1de0145bce6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62172721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fea961b7c219f4311d2161bdd3fe70d741842e4e9221a93fa2c080337ea2654c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 17 Dec 2024 14:20:15 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1743984000'
# Tue, 17 Dec 2024 14:20:15 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 17 Dec 2024 14:20:15 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 17 Dec 2024 14:20:15 GMT
VOLUME [/var/lib/chronograf]
# Tue, 17 Dec 2024 14:20:15 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Dec 2024 14:20:15 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:bfc445187b87c4f640fe8b85c4ee3c251ce5e7023a5ff0acd053bde1f01e6aaf`  
		Last Modified: Tue, 08 Apr 2025 00:23:52 GMT  
		Size: 25.5 MB (25539135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1d14c78e9af4f52cf73c1b9c4b85220d72bad57e9c3f71fd942534213bb4bb0`  
		Last Modified: Tue, 08 Apr 2025 07:40:32 GMT  
		Size: 3.5 MB (3511703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6a68f8b0eff27951314444f787c5f7fb261f843fdef82c823a7ef9075e99bc2`  
		Last Modified: Tue, 08 Apr 2025 07:40:32 GMT  
		Size: 33.1 MB (33097486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67d6aeedb9e6e411b0a920b67f378446ea2c1d2f91539700339db32c921c81c4`  
		Last Modified: Tue, 08 Apr 2025 07:40:31 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5163651c84d3a13a704340c0ce489715f0faa863e48eeffde865a1154438eab`  
		Last Modified: Tue, 08 Apr 2025 07:40:31 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd268020c9ec09ff429f00b50cc325185c7dca189c543c47c0a208f149a6f8d5`  
		Last Modified: Tue, 08 Apr 2025 07:40:32 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7.17` - unknown; unknown

```console
$ docker pull chronograf@sha256:dc3daa045852fc37940f8a48a0745eaad3de38cfe5d21facfc4a703083a66845
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2925424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:138227f43e65edaedaae4e67dba714767663d75980f6fadfa3b12cb71a7ba03a`

```dockerfile
```

-	Layers:
	-	`sha256:d0375e574b8331d8ce78912e9c43e2ee53e35f32dfad6871059df6ac003e9506`  
		Last Modified: Tue, 08 Apr 2025 07:40:31 GMT  
		Size: 2.9 MB (2909574 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fdd26cfd1642657b1ff29199b16490e15213a678516faeef7603717c3c8a0901`  
		Last Modified: Tue, 08 Apr 2025 07:40:31 GMT  
		Size: 15.8 KB (15850 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.7.17` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:2ff525bc22e369edccc178ae64e3ef62bd883cec7b0c82666dd62cfb07ba05b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66222443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e4993891ccca3c03a428ea8d8f2c47da7eed477c3f0883d591c111c860600f0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 17 Dec 2024 14:20:15 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1743984000'
# Tue, 17 Dec 2024 14:20:15 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 17 Dec 2024 14:20:15 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 17 Dec 2024 14:20:15 GMT
VOLUME [/var/lib/chronograf]
# Tue, 17 Dec 2024 14:20:15 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Dec 2024 14:20:15 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:59627ca2e9712141a7d131bec6c9931f8ecea11eac34d96bd1213ccea68e18e5`  
		Last Modified: Tue, 08 Apr 2025 00:23:35 GMT  
		Size: 28.7 MB (28749498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f34c692a4ba55ec40062c62051436a12aaec0bf32d9e641edcaedec9b69f37a`  
		Last Modified: Tue, 08 Apr 2025 06:05:12 GMT  
		Size: 4.2 MB (4210644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e8443d8aaee9019ed461a4047652b1c8036146c2e07f17977d06a071febcf16`  
		Last Modified: Tue, 08 Apr 2025 06:05:12 GMT  
		Size: 33.2 MB (33237920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf081dc2c5584b0c7ff39fc577f613ecec3d71cedaa41739f750efa3bfc4012f`  
		Last Modified: Tue, 08 Apr 2025 06:05:11 GMT  
		Size: 12.2 KB (12242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a416b5388d2e8a9ade42d3402641a23922dd180928dde08ebba726f40cd6cd7`  
		Last Modified: Tue, 08 Apr 2025 06:05:11 GMT  
		Size: 11.9 KB (11900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22cfef9759938b46bdd87e3db06e225e6fa4ce4919c3e0b0b46a61b1aeaf0597`  
		Last Modified: Tue, 08 Apr 2025 06:05:12 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7.17` - unknown; unknown

```console
$ docker pull chronograf@sha256:e2cd81f211b2076ee9e7c4c31cde7d25cf645e9b22623c853012efbb51e6ec9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2923424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a51822590dc13c588c14875d2c3963ffac84c5e6ff2f543686ac666a66d2f2f9`

```dockerfile
```

-	Layers:
	-	`sha256:5d093599408be9ca787922bfe7cfcb0fb6541349c26f2a74c41d6d5528562ae6`  
		Last Modified: Tue, 08 Apr 2025 06:05:11 GMT  
		Size: 2.9 MB (2907552 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17aac24de39859317b140f81e79fad98ea275f45e4d5ff5802c7fa3834bfb7a1`  
		Last Modified: Tue, 08 Apr 2025 06:05:11 GMT  
		Size: 15.9 KB (15872 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.7.17-alpine`

```console
$ docker pull chronograf@sha256:df924b85652b1a3cf6ee401da68f4ef42a31256cd06244016ae21cec9f8952d0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.7.17-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:f033d37b112e959a0534de672abf91b9c3aa43535d685738ea85e838e904e8e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.5 MB (23502749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:137abfa83685c0597819295c4b3ef856c9395a461bd9bd70ff91ec3a4cd5921a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
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
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 12:05:36 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f8ae06deb09ed334ed8eba44b6e425cced470152dbdd9c0e3c6125578263f57`  
		Last Modified: Fri, 14 Feb 2025 19:24:48 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69641bcb67c77b895509abb75bf637ce2b76f0acdd981fd282b113d82c04c619`  
		Last Modified: Fri, 14 Feb 2025 19:24:48 GMT  
		Size: 294.4 KB (294383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1c71c1a03f44724b1796ddc3866d8fe5c4a5af8862448eabb7b2ebdc7a47748`  
		Last Modified: Fri, 14 Feb 2025 19:24:49 GMT  
		Size: 19.6 MB (19556823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f29450f6d74de26216b10dc587e69dd4443992a6aea3c7b424c7aaad08ceef29`  
		Last Modified: Fri, 14 Feb 2025 19:24:48 GMT  
		Size: 12.2 KB (12235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97e84d9f6956c08b6776f1b3db99e0226246d044677f2e4cf470051da809c34e`  
		Last Modified: Fri, 14 Feb 2025 19:24:49 GMT  
		Size: 11.9 KB (11893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:030349c6370852b4bfb957d5c0dc77ca8ab49cfd26485c0b053651d825d6caf9`  
		Last Modified: Fri, 14 Feb 2025 19:24:49 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7.17-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:0c38d57135acbd91b733dbd02beff4e0339d76bf9f15f687bd8c4f5a2f887e91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.3 KB (189257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:471658777992e65c6b6d0f2da3225f4e41179e9be460d18106df6b906e69e00b`

```dockerfile
```

-	Layers:
	-	`sha256:6592097eed7dd5f5abfbbe36bb576489b44efd68487a9d4d946f1dc3e7aeac87`  
		Last Modified: Fri, 14 Feb 2025 19:24:48 GMT  
		Size: 172.3 KB (172345 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2af6f071245b63b559b430cac0c4aba0ef1cc49a72e9b52d3edae3f8b2d6ad95`  
		Last Modified: Fri, 14 Feb 2025 19:24:48 GMT  
		Size: 16.9 KB (16912 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.8`

```console
$ docker pull chronograf@sha256:561ec10755c2ca69c8e04dcaeecd5137fcd3b0e41639e0fd30d800cad7d18c6f
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
$ docker pull chronograf@sha256:13d6f9438e8d1675e5305b66f97b995806b018ec21e965cb66fe1e328b702fdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69870381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60fe9251105bfe592f1d6368c77e691986896b4131e6c9e9aa8adaefd63af6e9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 17 Dec 2024 14:20:15 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1743984000'
# Tue, 17 Dec 2024 14:20:15 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Tue, 17 Dec 2024 14:20:15 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 17 Dec 2024 14:20:15 GMT
VOLUME [/var/lib/chronograf]
# Tue, 17 Dec 2024 14:20:15 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Dec 2024 14:20:15 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:b983e127c643116d446fa1b64216f464e1d06a8bfaeeb8a895c361c1bc3f5652`  
		Last Modified: Tue, 08 Apr 2025 00:23:09 GMT  
		Size: 30.3 MB (30257419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9fb9ad9337f85af5653564f81c6afc7244bdb61a21764b6c9d42d7019f85915`  
		Last Modified: Tue, 08 Apr 2025 01:24:37 GMT  
		Size: 5.2 MB (5224274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d5309d14cad5c8b245b2c882543981a1a7533d1b881b3aa790fd1932f5aa22`  
		Last Modified: Tue, 08 Apr 2025 01:24:37 GMT  
		Size: 34.4 MB (34364289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b61aafe64d444a0a56702e77d1318b804f225c150ae2e03c17dc646f4cd87337`  
		Last Modified: Tue, 08 Apr 2025 01:24:36 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:344de50f49278e56ad01285950504292ab7bbd2c81391a34913c327a7ee80e07`  
		Last Modified: Tue, 08 Apr 2025 01:24:36 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d68a571c7cd887f42c23363ddb5c387642bf8b2efca3fab04b3c8708662a61c`  
		Last Modified: Tue, 08 Apr 2025 01:24:37 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8` - unknown; unknown

```console
$ docker pull chronograf@sha256:6d07453903853f93e8fab1afcba048c854a60b0aa8295b2656af42fe3654ae3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2978762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ca0cbb11ee44cab0f3aaebdb94e38e7115330b314676921f2063dafdcd0ff5c`

```dockerfile
```

-	Layers:
	-	`sha256:e129b7d5208c7127aa5f6d37848e010fe9057ea6c8ae243bf374450082ca1594`  
		Last Modified: Tue, 08 Apr 2025 01:24:36 GMT  
		Size: 3.0 MB (2962945 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b5c37e09175736df339f32030095550a0bdb645fe1fa038d0296b6e58e22669`  
		Last Modified: Tue, 08 Apr 2025 01:24:36 GMT  
		Size: 15.8 KB (15817 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.8` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:668eb22e47dcd4f26d001ed42d5f16a7c34a22b91a6ec148a4f18316890dfe03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.6 MB (62588621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d4759b7589587bdb9d0a41a976226cc229bde39ea6b8b52e4747c5503f7144f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 17 Dec 2024 14:20:15 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1743984000'
# Tue, 17 Dec 2024 14:20:15 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Tue, 17 Dec 2024 14:20:15 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 17 Dec 2024 14:20:15 GMT
VOLUME [/var/lib/chronograf]
# Tue, 17 Dec 2024 14:20:15 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Dec 2024 14:20:15 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:bfc445187b87c4f640fe8b85c4ee3c251ce5e7023a5ff0acd053bde1f01e6aaf`  
		Last Modified: Tue, 08 Apr 2025 00:23:52 GMT  
		Size: 25.5 MB (25539135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f0b0b39b02d12cb49936a4f5580a9ca91eeefb579f114099959b79b3128b139`  
		Last Modified: Tue, 08 Apr 2025 07:41:10 GMT  
		Size: 4.5 MB (4490190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db1f8a530e209678900b3d30c8010c8c0de4a84476f4c20b2011e2119e2fd8d8`  
		Last Modified: Tue, 08 Apr 2025 16:50:37 GMT  
		Size: 32.5 MB (32534897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d6e00bebaf901b0fb246bd96d2a602046a18c37afed6317168f2cefe4940f33`  
		Last Modified: Tue, 08 Apr 2025 16:50:35 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25a1aacac7e954dfd535bc458597639617decf5cde5c24a9dc9266bdcf381fe4`  
		Last Modified: Tue, 08 Apr 2025 16:50:36 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9ecae03690a51b2c333241bcb192b42b7403c8cc95f93b384a9315557c1dff5`  
		Last Modified: Tue, 08 Apr 2025 16:50:35 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8` - unknown; unknown

```console
$ docker pull chronograf@sha256:7ae8d6e4378a3a3855055ebc5176ea9686a9100819defd1494f97499950fe83b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2981106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f95d25b7c427321e110fd43fa364723c17638d3c7e979f86c16290097b09348`

```dockerfile
```

-	Layers:
	-	`sha256:fdd9d8d1ecc2b1938e8d4c9f031d56810a8830771d25280774986a8ebaedd004`  
		Last Modified: Tue, 08 Apr 2025 16:50:36 GMT  
		Size: 3.0 MB (2965216 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dff9ac86a43b481edb47542dfbfbda814c8c806e1984ad62eb59279cd7848162`  
		Last Modified: Tue, 08 Apr 2025 16:50:35 GMT  
		Size: 15.9 KB (15890 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.8` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:dcd1104d1b3d97203acee67a8f83252ade422ce0c1d788b391006e47cc184b46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.4 MB (66411633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a41eb25a0104d676efd079178fd3b37b18f780d9d6af898f515d57266aef70b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 17 Dec 2024 14:20:15 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1743984000'
# Tue, 17 Dec 2024 14:20:15 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Tue, 17 Dec 2024 14:20:15 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 17 Dec 2024 14:20:15 GMT
VOLUME [/var/lib/chronograf]
# Tue, 17 Dec 2024 14:20:15 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Dec 2024 14:20:15 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:59627ca2e9712141a7d131bec6c9931f8ecea11eac34d96bd1213ccea68e18e5`  
		Last Modified: Tue, 08 Apr 2025 00:23:35 GMT  
		Size: 28.7 MB (28749498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b767d408970ea6a3ea48ab8565f22be76cc47d74850030306fd979258625d7c3`  
		Last Modified: Tue, 08 Apr 2025 06:05:39 GMT  
		Size: 5.2 MB (5208207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:653e68a955cffa9d0d1d6f5bf0efc93e6808385fb2b2331fee597dcd90d86f12`  
		Last Modified: Tue, 08 Apr 2025 06:05:41 GMT  
		Size: 32.4 MB (32429527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de90a5fb19cee5ed6d5f837340270125af72ccb3d8bf9017601b4f00e3b02337`  
		Last Modified: Tue, 08 Apr 2025 06:05:39 GMT  
		Size: 12.3 KB (12251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d0a81000b8293f6af67e104708a7c7f0c70409eff53695eabc8efa4680f7189`  
		Last Modified: Tue, 08 Apr 2025 06:05:39 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66b34678ef48b9be8342db3413d4343f8e1ed90e45fd2c0bc83acc686d74c3d5`  
		Last Modified: Tue, 08 Apr 2025 06:05:40 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8` - unknown; unknown

```console
$ docker pull chronograf@sha256:34f86a7fa0aef6fbb4ad12aa78353135530a746d819c762d8d87b0c084dd719a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2979106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f5c807f5b9aec1aa1b131ac7921cb0cc681ef82f96633d64555dac737d0939c`

```dockerfile
```

-	Layers:
	-	`sha256:269c71a2962a786b9ca2ce88fb6dd019c71f0aaee4d686e48425f73d191f3993`  
		Last Modified: Tue, 08 Apr 2025 06:05:39 GMT  
		Size: 3.0 MB (2963194 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e1e737d6a45efaa4459c03f81dcb9aaf0ccfec36ec323ff40326d1c5f9532dc`  
		Last Modified: Tue, 08 Apr 2025 06:05:39 GMT  
		Size: 15.9 KB (15912 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.8-alpine`

```console
$ docker pull chronograf@sha256:830cefde62b7fa5d1e719c9cdbd90e36b6111165338d6a63589967af3b425932
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.8-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:1bc656b7ebda40ceb3556472bac3163ab7b63970a38964aba666e23cab083110
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.2 MB (23150080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a1f3cf9f33249acb43998ce431a893a6196e54c6623a39388c922e747600326`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
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
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 12:05:36 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c39259f86321f91341426ea2b7c8164eb8c8a538841604f969c31abd195acba`  
		Last Modified: Fri, 14 Feb 2025 19:24:44 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86bf003f24079392a7a29452383a6db1f26978c48f54533c79153b28b82b7257`  
		Last Modified: Fri, 14 Feb 2025 19:24:44 GMT  
		Size: 294.4 KB (294385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fb15ecadba26a5095f16beac190b0f35fa020ee3fff220c3243ebb39f58712a`  
		Last Modified: Fri, 14 Feb 2025 19:24:44 GMT  
		Size: 19.2 MB (19204154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:402cd540f74e77bd8181c883cf26fa3525fd15513ad005bc58b5bed6ddb9d248`  
		Last Modified: Fri, 14 Feb 2025 19:24:44 GMT  
		Size: 12.2 KB (12235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c299e5fdf7b7064f6b152ef78a715eefeff0a18c48c95e7a2b74b34bc318c7f5`  
		Last Modified: Fri, 14 Feb 2025 19:24:45 GMT  
		Size: 11.9 KB (11892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33ff2dde7922e46ced41d599cff59f593b600debe56130e43867bb3be500e704`  
		Last Modified: Fri, 14 Feb 2025 19:24:45 GMT  
		Size: 237.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:cdd0db3358b43541330dbf7e54517d4cbd7e2c4dfcdf798c5197cdc28507a544
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.8 KB (246816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4af8a7ead9ebe09b9d15f6a3a39569c97af7c6664e752144193917be3f3928e`

```dockerfile
```

-	Layers:
	-	`sha256:41a2c152911589c4db3aec41c07d7ba26ba8320255380bc8e9f5dad25980a11b`  
		Last Modified: Fri, 14 Feb 2025 19:24:44 GMT  
		Size: 229.9 KB (229904 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6ad8d123c697deeb31e83f6f288bbb9095d82109f9902675e157e8b88f35c2b`  
		Last Modified: Fri, 14 Feb 2025 19:24:44 GMT  
		Size: 16.9 KB (16912 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.8.10`

```console
$ docker pull chronograf@sha256:561ec10755c2ca69c8e04dcaeecd5137fcd3b0e41639e0fd30d800cad7d18c6f
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
$ docker pull chronograf@sha256:13d6f9438e8d1675e5305b66f97b995806b018ec21e965cb66fe1e328b702fdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69870381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60fe9251105bfe592f1d6368c77e691986896b4131e6c9e9aa8adaefd63af6e9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 17 Dec 2024 14:20:15 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1743984000'
# Tue, 17 Dec 2024 14:20:15 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Tue, 17 Dec 2024 14:20:15 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 17 Dec 2024 14:20:15 GMT
VOLUME [/var/lib/chronograf]
# Tue, 17 Dec 2024 14:20:15 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Dec 2024 14:20:15 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:b983e127c643116d446fa1b64216f464e1d06a8bfaeeb8a895c361c1bc3f5652`  
		Last Modified: Tue, 08 Apr 2025 00:23:09 GMT  
		Size: 30.3 MB (30257419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9fb9ad9337f85af5653564f81c6afc7244bdb61a21764b6c9d42d7019f85915`  
		Last Modified: Tue, 08 Apr 2025 01:24:37 GMT  
		Size: 5.2 MB (5224274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d5309d14cad5c8b245b2c882543981a1a7533d1b881b3aa790fd1932f5aa22`  
		Last Modified: Tue, 08 Apr 2025 01:24:37 GMT  
		Size: 34.4 MB (34364289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b61aafe64d444a0a56702e77d1318b804f225c150ae2e03c17dc646f4cd87337`  
		Last Modified: Tue, 08 Apr 2025 01:24:36 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:344de50f49278e56ad01285950504292ab7bbd2c81391a34913c327a7ee80e07`  
		Last Modified: Tue, 08 Apr 2025 01:24:36 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d68a571c7cd887f42c23363ddb5c387642bf8b2efca3fab04b3c8708662a61c`  
		Last Modified: Tue, 08 Apr 2025 01:24:37 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:6d07453903853f93e8fab1afcba048c854a60b0aa8295b2656af42fe3654ae3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2978762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ca0cbb11ee44cab0f3aaebdb94e38e7115330b314676921f2063dafdcd0ff5c`

```dockerfile
```

-	Layers:
	-	`sha256:e129b7d5208c7127aa5f6d37848e010fe9057ea6c8ae243bf374450082ca1594`  
		Last Modified: Tue, 08 Apr 2025 01:24:36 GMT  
		Size: 3.0 MB (2962945 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b5c37e09175736df339f32030095550a0bdb645fe1fa038d0296b6e58e22669`  
		Last Modified: Tue, 08 Apr 2025 01:24:36 GMT  
		Size: 15.8 KB (15817 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.8.10` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:668eb22e47dcd4f26d001ed42d5f16a7c34a22b91a6ec148a4f18316890dfe03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.6 MB (62588621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d4759b7589587bdb9d0a41a976226cc229bde39ea6b8b52e4747c5503f7144f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 17 Dec 2024 14:20:15 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1743984000'
# Tue, 17 Dec 2024 14:20:15 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Tue, 17 Dec 2024 14:20:15 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 17 Dec 2024 14:20:15 GMT
VOLUME [/var/lib/chronograf]
# Tue, 17 Dec 2024 14:20:15 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Dec 2024 14:20:15 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:bfc445187b87c4f640fe8b85c4ee3c251ce5e7023a5ff0acd053bde1f01e6aaf`  
		Last Modified: Tue, 08 Apr 2025 00:23:52 GMT  
		Size: 25.5 MB (25539135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f0b0b39b02d12cb49936a4f5580a9ca91eeefb579f114099959b79b3128b139`  
		Last Modified: Tue, 08 Apr 2025 07:41:10 GMT  
		Size: 4.5 MB (4490190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db1f8a530e209678900b3d30c8010c8c0de4a84476f4c20b2011e2119e2fd8d8`  
		Last Modified: Tue, 08 Apr 2025 16:50:37 GMT  
		Size: 32.5 MB (32534897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d6e00bebaf901b0fb246bd96d2a602046a18c37afed6317168f2cefe4940f33`  
		Last Modified: Tue, 08 Apr 2025 16:50:35 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25a1aacac7e954dfd535bc458597639617decf5cde5c24a9dc9266bdcf381fe4`  
		Last Modified: Tue, 08 Apr 2025 16:50:36 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9ecae03690a51b2c333241bcb192b42b7403c8cc95f93b384a9315557c1dff5`  
		Last Modified: Tue, 08 Apr 2025 16:50:35 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:7ae8d6e4378a3a3855055ebc5176ea9686a9100819defd1494f97499950fe83b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2981106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f95d25b7c427321e110fd43fa364723c17638d3c7e979f86c16290097b09348`

```dockerfile
```

-	Layers:
	-	`sha256:fdd9d8d1ecc2b1938e8d4c9f031d56810a8830771d25280774986a8ebaedd004`  
		Last Modified: Tue, 08 Apr 2025 16:50:36 GMT  
		Size: 3.0 MB (2965216 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dff9ac86a43b481edb47542dfbfbda814c8c806e1984ad62eb59279cd7848162`  
		Last Modified: Tue, 08 Apr 2025 16:50:35 GMT  
		Size: 15.9 KB (15890 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.8.10` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:dcd1104d1b3d97203acee67a8f83252ade422ce0c1d788b391006e47cc184b46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.4 MB (66411633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a41eb25a0104d676efd079178fd3b37b18f780d9d6af898f515d57266aef70b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 17 Dec 2024 14:20:15 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1743984000'
# Tue, 17 Dec 2024 14:20:15 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Tue, 17 Dec 2024 14:20:15 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 17 Dec 2024 14:20:15 GMT
VOLUME [/var/lib/chronograf]
# Tue, 17 Dec 2024 14:20:15 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Dec 2024 14:20:15 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:59627ca2e9712141a7d131bec6c9931f8ecea11eac34d96bd1213ccea68e18e5`  
		Last Modified: Tue, 08 Apr 2025 00:23:35 GMT  
		Size: 28.7 MB (28749498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b767d408970ea6a3ea48ab8565f22be76cc47d74850030306fd979258625d7c3`  
		Last Modified: Tue, 08 Apr 2025 06:05:39 GMT  
		Size: 5.2 MB (5208207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:653e68a955cffa9d0d1d6f5bf0efc93e6808385fb2b2331fee597dcd90d86f12`  
		Last Modified: Tue, 08 Apr 2025 06:05:41 GMT  
		Size: 32.4 MB (32429527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de90a5fb19cee5ed6d5f837340270125af72ccb3d8bf9017601b4f00e3b02337`  
		Last Modified: Tue, 08 Apr 2025 06:05:39 GMT  
		Size: 12.3 KB (12251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d0a81000b8293f6af67e104708a7c7f0c70409eff53695eabc8efa4680f7189`  
		Last Modified: Tue, 08 Apr 2025 06:05:39 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66b34678ef48b9be8342db3413d4343f8e1ed90e45fd2c0bc83acc686d74c3d5`  
		Last Modified: Tue, 08 Apr 2025 06:05:40 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:34f86a7fa0aef6fbb4ad12aa78353135530a746d819c762d8d87b0c084dd719a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2979106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f5c807f5b9aec1aa1b131ac7921cb0cc681ef82f96633d64555dac737d0939c`

```dockerfile
```

-	Layers:
	-	`sha256:269c71a2962a786b9ca2ce88fb6dd019c71f0aaee4d686e48425f73d191f3993`  
		Last Modified: Tue, 08 Apr 2025 06:05:39 GMT  
		Size: 3.0 MB (2963194 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e1e737d6a45efaa4459c03f81dcb9aaf0ccfec36ec323ff40326d1c5f9532dc`  
		Last Modified: Tue, 08 Apr 2025 06:05:39 GMT  
		Size: 15.9 KB (15912 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.8.10-alpine`

```console
$ docker pull chronograf@sha256:830cefde62b7fa5d1e719c9cdbd90e36b6111165338d6a63589967af3b425932
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.8.10-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:1bc656b7ebda40ceb3556472bac3163ab7b63970a38964aba666e23cab083110
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.2 MB (23150080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a1f3cf9f33249acb43998ce431a893a6196e54c6623a39388c922e747600326`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
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
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 12:05:36 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c39259f86321f91341426ea2b7c8164eb8c8a538841604f969c31abd195acba`  
		Last Modified: Fri, 14 Feb 2025 19:24:44 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86bf003f24079392a7a29452383a6db1f26978c48f54533c79153b28b82b7257`  
		Last Modified: Fri, 14 Feb 2025 19:24:44 GMT  
		Size: 294.4 KB (294385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fb15ecadba26a5095f16beac190b0f35fa020ee3fff220c3243ebb39f58712a`  
		Last Modified: Fri, 14 Feb 2025 19:24:44 GMT  
		Size: 19.2 MB (19204154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:402cd540f74e77bd8181c883cf26fa3525fd15513ad005bc58b5bed6ddb9d248`  
		Last Modified: Fri, 14 Feb 2025 19:24:44 GMT  
		Size: 12.2 KB (12235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c299e5fdf7b7064f6b152ef78a715eefeff0a18c48c95e7a2b74b34bc318c7f5`  
		Last Modified: Fri, 14 Feb 2025 19:24:45 GMT  
		Size: 11.9 KB (11892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33ff2dde7922e46ced41d599cff59f593b600debe56130e43867bb3be500e704`  
		Last Modified: Fri, 14 Feb 2025 19:24:45 GMT  
		Size: 237.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8.10-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:cdd0db3358b43541330dbf7e54517d4cbd7e2c4dfcdf798c5197cdc28507a544
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.8 KB (246816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4af8a7ead9ebe09b9d15f6a3a39569c97af7c6664e752144193917be3f3928e`

```dockerfile
```

-	Layers:
	-	`sha256:41a2c152911589c4db3aec41c07d7ba26ba8320255380bc8e9f5dad25980a11b`  
		Last Modified: Fri, 14 Feb 2025 19:24:44 GMT  
		Size: 229.9 KB (229904 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6ad8d123c697deeb31e83f6f288bbb9095d82109f9902675e157e8b88f35c2b`  
		Last Modified: Fri, 14 Feb 2025 19:24:44 GMT  
		Size: 16.9 KB (16912 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.9`

```console
$ docker pull chronograf@sha256:745545ba52feccf8392e4d6ae26c750e8f79a8730112d0a7a5772086575f0dad
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
$ docker pull chronograf@sha256:9d515b039fd4ab702728512219ac562f2ffbc34d782a042469095bec0f1499ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.5 MB (70517749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb4c941cd8d4a9eb92af79bfc5de352985bbe056ced04155427d627b479b4ee2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 17 Dec 2024 14:20:15 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1743984000'
# Tue, 17 Dec 2024 14:20:15 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Tue, 17 Dec 2024 14:20:15 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 17 Dec 2024 14:20:15 GMT
VOLUME [/var/lib/chronograf]
# Tue, 17 Dec 2024 14:20:15 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Dec 2024 14:20:15 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:b983e127c643116d446fa1b64216f464e1d06a8bfaeeb8a895c361c1bc3f5652`  
		Last Modified: Tue, 08 Apr 2025 00:23:09 GMT  
		Size: 30.3 MB (30257419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac3d85b0dc59db88146fe076e576531e218ae09ca17fe6ae2a97999698e7d5b4`  
		Last Modified: Tue, 08 Apr 2025 01:24:43 GMT  
		Size: 5.2 MB (5224215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b41e2e4ba6a52e6c3c34d701f967f54449bde6659e3d2085196f2271a7746b`  
		Last Modified: Tue, 08 Apr 2025 01:24:44 GMT  
		Size: 35.0 MB (35011724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b27fe2ba7adf3d5b9f0b15e15fd193c82c2f132794d601fabdb4e34bb3b76b`  
		Last Modified: Tue, 08 Apr 2025 01:24:43 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d360deadc722bd01301a6442a44d6fa236c0fae2f04f8419f2e16c47fe582d99`  
		Last Modified: Tue, 08 Apr 2025 01:24:43 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00f488f63d9ef1883f7a0b428a680f19a6718f51e86b1be8f5d4e655a11ac903`  
		Last Modified: Tue, 08 Apr 2025 01:24:44 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9` - unknown; unknown

```console
$ docker pull chronograf@sha256:66d73c20791bee150dfade1599a8c36fc627ea3e371d4033bacc8c18a6ceba80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2983964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82d8f94f24b0b50281adf43027ea07824ee5e3705ec39e7d9a71bcff1e753a28`

```dockerfile
```

-	Layers:
	-	`sha256:6c08d1263bef35dc09baf855c2fb05a01bef6252efed203932ae066cb9139cee`  
		Last Modified: Tue, 08 Apr 2025 01:24:43 GMT  
		Size: 3.0 MB (2968155 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1efac13d8e9218be244c72e631105594d6c4e9c05414b7192b4a25ff729aa1e`  
		Last Modified: Tue, 08 Apr 2025 01:24:43 GMT  
		Size: 15.8 KB (15809 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.9` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:7a804273bb9a65df3584b02e5cea98dafd2deb597174b8da4e416115adabdbad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.4 MB (63365245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f9214a2113128457a44c31fa35c58455dc38b7c8ed5d72bc551632a0056eddc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 17 Dec 2024 14:20:15 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1743984000'
# Tue, 17 Dec 2024 14:20:15 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Tue, 17 Dec 2024 14:20:15 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 17 Dec 2024 14:20:15 GMT
VOLUME [/var/lib/chronograf]
# Tue, 17 Dec 2024 14:20:15 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Dec 2024 14:20:15 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:bfc445187b87c4f640fe8b85c4ee3c251ce5e7023a5ff0acd053bde1f01e6aaf`  
		Last Modified: Tue, 08 Apr 2025 00:23:52 GMT  
		Size: 25.5 MB (25539135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f0b0b39b02d12cb49936a4f5580a9ca91eeefb579f114099959b79b3128b139`  
		Last Modified: Tue, 08 Apr 2025 07:41:10 GMT  
		Size: 4.5 MB (4490190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48430a96bef61b448970104515368d0383eb935c3c3f19d8f18ea7a8499512fd`  
		Last Modified: Tue, 08 Apr 2025 07:41:10 GMT  
		Size: 33.3 MB (33311516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4fa1b548017d769459179d1963089e5f0a5474664b18f8793de007d90259992`  
		Last Modified: Tue, 08 Apr 2025 07:41:09 GMT  
		Size: 12.3 KB (12253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c6ab35af3915d25c10b08ed987b93b161e8ce3396940c17e05e3293c09d2728`  
		Last Modified: Tue, 08 Apr 2025 07:41:09 GMT  
		Size: 11.9 KB (11911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9a2aeb3a8fca8930c64570a0675e7b1a5762acb78402582ccd3a6641009eca1`  
		Last Modified: Tue, 08 Apr 2025 07:41:10 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9` - unknown; unknown

```console
$ docker pull chronograf@sha256:5270d4452f5beb602899e0d457cb1fbed51a1bad839e7a555530487a78a82115
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2986308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e32fbd4967049b2545151cd855977da3d77437d2f886298e2b9eab2842d7132d`

```dockerfile
```

-	Layers:
	-	`sha256:2edd2e28a5e0fe57608ae68f4ae22401cae10275d339012fa2091aaca6a004f8`  
		Last Modified: Tue, 08 Apr 2025 07:41:10 GMT  
		Size: 3.0 MB (2970426 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50c573f69fbae202efdf003e20819749eb810e650591ca2aebd26ebef5863cf5`  
		Last Modified: Tue, 08 Apr 2025 07:41:09 GMT  
		Size: 15.9 KB (15882 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.9` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:175ba474b4a6a2505b2b197cb7a8158f56b232ba573156c11edbe11a52944de3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.2 MB (67163736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c17fe67c2b51ab16a5402d7c58b232db1484bd8bc1a7cb7a465812e162f1ac3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 17 Dec 2024 14:20:15 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1743984000'
# Tue, 17 Dec 2024 14:20:15 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Tue, 17 Dec 2024 14:20:15 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 17 Dec 2024 14:20:15 GMT
VOLUME [/var/lib/chronograf]
# Tue, 17 Dec 2024 14:20:15 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Dec 2024 14:20:15 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:59627ca2e9712141a7d131bec6c9931f8ecea11eac34d96bd1213ccea68e18e5`  
		Last Modified: Tue, 08 Apr 2025 00:23:35 GMT  
		Size: 28.7 MB (28749498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b767d408970ea6a3ea48ab8565f22be76cc47d74850030306fd979258625d7c3`  
		Last Modified: Tue, 08 Apr 2025 06:05:39 GMT  
		Size: 5.2 MB (5208207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6301eafc2b5438b27d99979515fb745fe3262d3c4a48270fbf44ef7c328e4370`  
		Last Modified: Tue, 08 Apr 2025 06:06:09 GMT  
		Size: 33.2 MB (33181626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6edc97b35b44335572495813fddfc8190a7b600e0608378c8ea2ed11b12c943c`  
		Last Modified: Tue, 08 Apr 2025 06:06:08 GMT  
		Size: 12.3 KB (12253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9afb2441076efb6452d39bcb44e4266c0869cc2a726d4abb25a29b21b582144f`  
		Last Modified: Tue, 08 Apr 2025 06:06:08 GMT  
		Size: 11.9 KB (11912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e51eafac08e7316eb8224da7bdb5a9416f428174da10f7596f9284a976061ed2`  
		Last Modified: Tue, 08 Apr 2025 06:06:08 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9` - unknown; unknown

```console
$ docker pull chronograf@sha256:f406af11f310d9b94595b93b37a240b2dc523efc5abb61218f8bfdf27112c98a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2984308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a023fea2ed154fc96898cc8dd181e4950fcb87098d86214b5f936cfe03f4cd3`

```dockerfile
```

-	Layers:
	-	`sha256:bb4da502e5be8b286fad8d09749f42260dcfe93c78df525b672f1f1b8a3d67dc`  
		Last Modified: Tue, 08 Apr 2025 06:06:08 GMT  
		Size: 3.0 MB (2968404 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3322cfeff9f64133f2425f37681052a8344363ade766401a8eaf8c34320ca6ab`  
		Last Modified: Tue, 08 Apr 2025 06:06:08 GMT  
		Size: 15.9 KB (15904 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.9-alpine`

```console
$ docker pull chronograf@sha256:540ce018515beb499f291d9455b2a9d1c289f8fae572d53fd54246fd7e7146d0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.9-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:a4dfb7641118d30a6585c108ec369459880e88c6faf92790e05d3593e3353a11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23617935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50c262c4b7eed1867c635b60b6ffc799536825070ed1596c83b1c42ad21c4105`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
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
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 12:05:36 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de662ab890de5cb0e03103817de459544467d4b3f0784c60d26b56b9057ad500`  
		Last Modified: Fri, 14 Feb 2025 19:24:48 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69641bcb67c77b895509abb75bf637ce2b76f0acdd981fd282b113d82c04c619`  
		Last Modified: Fri, 14 Feb 2025 19:24:48 GMT  
		Size: 294.4 KB (294383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbc476e87cc64ce09a8be67509b3baee59f88525efcf0dbb7aa18f0aeeb0823b`  
		Last Modified: Fri, 14 Feb 2025 19:24:49 GMT  
		Size: 19.7 MB (19672009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f29450f6d74de26216b10dc587e69dd4443992a6aea3c7b424c7aaad08ceef29`  
		Last Modified: Fri, 14 Feb 2025 19:24:48 GMT  
		Size: 12.2 KB (12235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97e84d9f6956c08b6776f1b3db99e0226246d044677f2e4cf470051da809c34e`  
		Last Modified: Fri, 14 Feb 2025 19:24:49 GMT  
		Size: 11.9 KB (11893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:030349c6370852b4bfb957d5c0dc77ca8ab49cfd26485c0b053651d825d6caf9`  
		Last Modified: Fri, 14 Feb 2025 19:24:49 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:50d32d3aaaf4e53754ad80987dede42204c13fb95cb686e2c2513f3385048a60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.0 KB (252025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0aafa46d648297defb395a6fbfbb62467880874da481dd27cd19da3182e2433`

```dockerfile
```

-	Layers:
	-	`sha256:4486aa18fc3114703709ddebe3fb35b7b024a9c27bc87effa33b6909ae7fe370`  
		Last Modified: Fri, 14 Feb 2025 19:24:48 GMT  
		Size: 235.1 KB (235116 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93b34d12538bfcd1dd3e2b34c8aa09be9693afe86e4462d7341bee3cf95202f0`  
		Last Modified: Fri, 14 Feb 2025 19:24:48 GMT  
		Size: 16.9 KB (16909 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.9.4`

```console
$ docker pull chronograf@sha256:745545ba52feccf8392e4d6ae26c750e8f79a8730112d0a7a5772086575f0dad
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
$ docker pull chronograf@sha256:9d515b039fd4ab702728512219ac562f2ffbc34d782a042469095bec0f1499ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.5 MB (70517749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb4c941cd8d4a9eb92af79bfc5de352985bbe056ced04155427d627b479b4ee2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 17 Dec 2024 14:20:15 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1743984000'
# Tue, 17 Dec 2024 14:20:15 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Tue, 17 Dec 2024 14:20:15 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 17 Dec 2024 14:20:15 GMT
VOLUME [/var/lib/chronograf]
# Tue, 17 Dec 2024 14:20:15 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Dec 2024 14:20:15 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:b983e127c643116d446fa1b64216f464e1d06a8bfaeeb8a895c361c1bc3f5652`  
		Last Modified: Tue, 08 Apr 2025 00:23:09 GMT  
		Size: 30.3 MB (30257419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac3d85b0dc59db88146fe076e576531e218ae09ca17fe6ae2a97999698e7d5b4`  
		Last Modified: Tue, 08 Apr 2025 01:24:43 GMT  
		Size: 5.2 MB (5224215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b41e2e4ba6a52e6c3c34d701f967f54449bde6659e3d2085196f2271a7746b`  
		Last Modified: Tue, 08 Apr 2025 01:24:44 GMT  
		Size: 35.0 MB (35011724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b27fe2ba7adf3d5b9f0b15e15fd193c82c2f132794d601fabdb4e34bb3b76b`  
		Last Modified: Tue, 08 Apr 2025 01:24:43 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d360deadc722bd01301a6442a44d6fa236c0fae2f04f8419f2e16c47fe582d99`  
		Last Modified: Tue, 08 Apr 2025 01:24:43 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00f488f63d9ef1883f7a0b428a680f19a6718f51e86b1be8f5d4e655a11ac903`  
		Last Modified: Tue, 08 Apr 2025 01:24:44 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9.4` - unknown; unknown

```console
$ docker pull chronograf@sha256:66d73c20791bee150dfade1599a8c36fc627ea3e371d4033bacc8c18a6ceba80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2983964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82d8f94f24b0b50281adf43027ea07824ee5e3705ec39e7d9a71bcff1e753a28`

```dockerfile
```

-	Layers:
	-	`sha256:6c08d1263bef35dc09baf855c2fb05a01bef6252efed203932ae066cb9139cee`  
		Last Modified: Tue, 08 Apr 2025 01:24:43 GMT  
		Size: 3.0 MB (2968155 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1efac13d8e9218be244c72e631105594d6c4e9c05414b7192b4a25ff729aa1e`  
		Last Modified: Tue, 08 Apr 2025 01:24:43 GMT  
		Size: 15.8 KB (15809 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.9.4` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:7a804273bb9a65df3584b02e5cea98dafd2deb597174b8da4e416115adabdbad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.4 MB (63365245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f9214a2113128457a44c31fa35c58455dc38b7c8ed5d72bc551632a0056eddc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 17 Dec 2024 14:20:15 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1743984000'
# Tue, 17 Dec 2024 14:20:15 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Tue, 17 Dec 2024 14:20:15 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 17 Dec 2024 14:20:15 GMT
VOLUME [/var/lib/chronograf]
# Tue, 17 Dec 2024 14:20:15 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Dec 2024 14:20:15 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:bfc445187b87c4f640fe8b85c4ee3c251ce5e7023a5ff0acd053bde1f01e6aaf`  
		Last Modified: Tue, 08 Apr 2025 00:23:52 GMT  
		Size: 25.5 MB (25539135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f0b0b39b02d12cb49936a4f5580a9ca91eeefb579f114099959b79b3128b139`  
		Last Modified: Tue, 08 Apr 2025 07:41:10 GMT  
		Size: 4.5 MB (4490190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48430a96bef61b448970104515368d0383eb935c3c3f19d8f18ea7a8499512fd`  
		Last Modified: Tue, 08 Apr 2025 07:41:10 GMT  
		Size: 33.3 MB (33311516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4fa1b548017d769459179d1963089e5f0a5474664b18f8793de007d90259992`  
		Last Modified: Tue, 08 Apr 2025 07:41:09 GMT  
		Size: 12.3 KB (12253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c6ab35af3915d25c10b08ed987b93b161e8ce3396940c17e05e3293c09d2728`  
		Last Modified: Tue, 08 Apr 2025 07:41:09 GMT  
		Size: 11.9 KB (11911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9a2aeb3a8fca8930c64570a0675e7b1a5762acb78402582ccd3a6641009eca1`  
		Last Modified: Tue, 08 Apr 2025 07:41:10 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9.4` - unknown; unknown

```console
$ docker pull chronograf@sha256:5270d4452f5beb602899e0d457cb1fbed51a1bad839e7a555530487a78a82115
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2986308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e32fbd4967049b2545151cd855977da3d77437d2f886298e2b9eab2842d7132d`

```dockerfile
```

-	Layers:
	-	`sha256:2edd2e28a5e0fe57608ae68f4ae22401cae10275d339012fa2091aaca6a004f8`  
		Last Modified: Tue, 08 Apr 2025 07:41:10 GMT  
		Size: 3.0 MB (2970426 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50c573f69fbae202efdf003e20819749eb810e650591ca2aebd26ebef5863cf5`  
		Last Modified: Tue, 08 Apr 2025 07:41:09 GMT  
		Size: 15.9 KB (15882 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.9.4` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:175ba474b4a6a2505b2b197cb7a8158f56b232ba573156c11edbe11a52944de3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.2 MB (67163736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c17fe67c2b51ab16a5402d7c58b232db1484bd8bc1a7cb7a465812e162f1ac3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 17 Dec 2024 14:20:15 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1743984000'
# Tue, 17 Dec 2024 14:20:15 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Tue, 17 Dec 2024 14:20:15 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 17 Dec 2024 14:20:15 GMT
VOLUME [/var/lib/chronograf]
# Tue, 17 Dec 2024 14:20:15 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Dec 2024 14:20:15 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:59627ca2e9712141a7d131bec6c9931f8ecea11eac34d96bd1213ccea68e18e5`  
		Last Modified: Tue, 08 Apr 2025 00:23:35 GMT  
		Size: 28.7 MB (28749498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b767d408970ea6a3ea48ab8565f22be76cc47d74850030306fd979258625d7c3`  
		Last Modified: Tue, 08 Apr 2025 06:05:39 GMT  
		Size: 5.2 MB (5208207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6301eafc2b5438b27d99979515fb745fe3262d3c4a48270fbf44ef7c328e4370`  
		Last Modified: Tue, 08 Apr 2025 06:06:09 GMT  
		Size: 33.2 MB (33181626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6edc97b35b44335572495813fddfc8190a7b600e0608378c8ea2ed11b12c943c`  
		Last Modified: Tue, 08 Apr 2025 06:06:08 GMT  
		Size: 12.3 KB (12253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9afb2441076efb6452d39bcb44e4266c0869cc2a726d4abb25a29b21b582144f`  
		Last Modified: Tue, 08 Apr 2025 06:06:08 GMT  
		Size: 11.9 KB (11912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e51eafac08e7316eb8224da7bdb5a9416f428174da10f7596f9284a976061ed2`  
		Last Modified: Tue, 08 Apr 2025 06:06:08 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9.4` - unknown; unknown

```console
$ docker pull chronograf@sha256:f406af11f310d9b94595b93b37a240b2dc523efc5abb61218f8bfdf27112c98a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2984308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a023fea2ed154fc96898cc8dd181e4950fcb87098d86214b5f936cfe03f4cd3`

```dockerfile
```

-	Layers:
	-	`sha256:bb4da502e5be8b286fad8d09749f42260dcfe93c78df525b672f1f1b8a3d67dc`  
		Last Modified: Tue, 08 Apr 2025 06:06:08 GMT  
		Size: 3.0 MB (2968404 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3322cfeff9f64133f2425f37681052a8344363ade766401a8eaf8c34320ca6ab`  
		Last Modified: Tue, 08 Apr 2025 06:06:08 GMT  
		Size: 15.9 KB (15904 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.9.4-alpine`

```console
$ docker pull chronograf@sha256:540ce018515beb499f291d9455b2a9d1c289f8fae572d53fd54246fd7e7146d0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.9.4-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:a4dfb7641118d30a6585c108ec369459880e88c6faf92790e05d3593e3353a11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23617935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50c262c4b7eed1867c635b60b6ffc799536825070ed1596c83b1c42ad21c4105`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
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
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 12:05:36 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de662ab890de5cb0e03103817de459544467d4b3f0784c60d26b56b9057ad500`  
		Last Modified: Fri, 14 Feb 2025 19:24:48 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69641bcb67c77b895509abb75bf637ce2b76f0acdd981fd282b113d82c04c619`  
		Last Modified: Fri, 14 Feb 2025 19:24:48 GMT  
		Size: 294.4 KB (294383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbc476e87cc64ce09a8be67509b3baee59f88525efcf0dbb7aa18f0aeeb0823b`  
		Last Modified: Fri, 14 Feb 2025 19:24:49 GMT  
		Size: 19.7 MB (19672009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f29450f6d74de26216b10dc587e69dd4443992a6aea3c7b424c7aaad08ceef29`  
		Last Modified: Fri, 14 Feb 2025 19:24:48 GMT  
		Size: 12.2 KB (12235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97e84d9f6956c08b6776f1b3db99e0226246d044677f2e4cf470051da809c34e`  
		Last Modified: Fri, 14 Feb 2025 19:24:49 GMT  
		Size: 11.9 KB (11893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:030349c6370852b4bfb957d5c0dc77ca8ab49cfd26485c0b053651d825d6caf9`  
		Last Modified: Fri, 14 Feb 2025 19:24:49 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9.4-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:50d32d3aaaf4e53754ad80987dede42204c13fb95cb686e2c2513f3385048a60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.0 KB (252025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0aafa46d648297defb395a6fbfbb62467880874da481dd27cd19da3182e2433`

```dockerfile
```

-	Layers:
	-	`sha256:4486aa18fc3114703709ddebe3fb35b7b024a9c27bc87effa33b6909ae7fe370`  
		Last Modified: Fri, 14 Feb 2025 19:24:48 GMT  
		Size: 235.1 KB (235116 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93b34d12538bfcd1dd3e2b34c8aa09be9693afe86e4462d7341bee3cf95202f0`  
		Last Modified: Fri, 14 Feb 2025 19:24:48 GMT  
		Size: 16.9 KB (16909 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:alpine`

```console
$ docker pull chronograf@sha256:357a021d3cd126c613abc52fc98c9065a2fb48f483032a725626baaa2761e3b4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:710e6bdd8c753ac12bc419bdc1cf4cedb0b554d8709fd762b307ddb4ff224659
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32156068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35ce1017cc5643e1a718b3830f3cf365a93c39b40189a9be172b575352a94374`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 17 Dec 2024 14:20:15 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
CMD ["/bin/sh"]
# Tue, 17 Dec 2024 14:20:15 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
RUN apk add --no-cache ca-certificates su-exec &&     update-ca-certificates # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
ENV CHRONOGRAF_VERSION=1.10.6
# Tue, 17 Dec 2024 14:20:15 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S chronograf &&     adduser -S chronograf -G chronograf &&     mkdir -m 0750 -p /var/lib/chronograf &&     chown chronograf:chronograf /var/lib/chronograf # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 17 Dec 2024 14:20:15 GMT
VOLUME [/var/lib/chronograf]
# Tue, 17 Dec 2024 14:20:15 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Dec 2024 14:20:15 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 12:05:36 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf00371f05d5b0928cf7ea0ada1dc3e28415f2be036fe5457e179bee6c9a23d4`  
		Last Modified: Mon, 24 Mar 2025 19:48:09 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c751720c18e7b8e894c53e3883a470d36188070073fe62c65a688cf3b065a238`  
		Last Modified: Mon, 24 Mar 2025 19:48:09 GMT  
		Size: 296.5 KB (296503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39366593367b5c31d595ef2671585706493373ae5c4cedaf022d6fa9fe81d502`  
		Last Modified: Mon, 24 Mar 2025 19:48:10 GMT  
		Size: 28.2 MB (28207965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:562bd300e80978e43bf12de6ba7c56811f6dfd92e79d94eaeaaa2224c7399f9d`  
		Last Modified: Mon, 24 Mar 2025 19:48:09 GMT  
		Size: 12.2 KB (12236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c15792c0d9c24edced73095648e9d68a08bf497c9243dce0b963b48c33814d70`  
		Last Modified: Mon, 24 Mar 2025 19:48:10 GMT  
		Size: 11.9 KB (11896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:019973f1fa061bc24fee856e1a9d0a0446bab0fa25d61bedf6c949584d5075ec`  
		Last Modified: Mon, 24 Mar 2025 19:48:10 GMT  
		Size: 292.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:90f7744b33302570f05e81ea60bd001215391027c10c0e8caf297ee94d6d1c7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.4 KB (259445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fc8eb620086f1de3306a8ded05948a19fb6a869e3f582032ce4ec8cc2758a71`

```dockerfile
```

-	Layers:
	-	`sha256:403f3626fe8060a52cb1b7dc3bf1a1d904541b71acbe11b5c100701b5a07d146`  
		Last Modified: Mon, 24 Mar 2025 19:48:09 GMT  
		Size: 241.6 KB (241591 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c8a546c4c466ea56cf10539a5a7edc0b8116bc37abc3c50063f85d03f979655`  
		Last Modified: Mon, 24 Mar 2025 19:48:09 GMT  
		Size: 17.9 KB (17854 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:latest`

```console
$ docker pull chronograf@sha256:07cba7b069e5ec7027d942b35a250358052174485c704f58aec1e2b4a7c3dcb9
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
$ docker pull chronograf@sha256:a5d5997fa575a11cbbd441528193b5078fea3221b6a6e5ea87598d4b28d1f0d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.6 MB (84581820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ecc21483ba8601581e9fde57391810fae4e11a9b6ca8f29c89c96ec401cfc0f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 17 Dec 2024 14:20:15 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
# Tue, 17 Dec 2024 14:20:15 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
ENV CHRONOGRAF_VERSION=1.10.6
# Tue, 17 Dec 2024 14:20:15 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 17 Dec 2024 14:20:15 GMT
VOLUME [/var/lib/chronograf]
# Tue, 17 Dec 2024 14:20:15 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Dec 2024 14:20:15 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:8a628cdd7ccc83e90e5a95888fcb0ec24b991141176c515ad101f12d6433eb96`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 28.2 MB (28227259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd5f7720f7246dde5561426d82d564eda3f7d36bb3a6670a3770bc88134d9db7`  
		Last Modified: Tue, 08 Apr 2025 01:24:50 GMT  
		Size: 7.9 MB (7875466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d937045b0d245509e6a15651490c28bbcf2ba34649a5e898a032e7b7b395fd30`  
		Last Modified: Tue, 08 Apr 2025 01:24:50 GMT  
		Size: 48.5 MB (48454620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea3ba974b6bb30cd12c43de5fc77a036818922515181202f95eb483d1a4d9b99`  
		Last Modified: Tue, 08 Apr 2025 01:24:49 GMT  
		Size: 12.3 KB (12251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb68d523da02175326435a308d4bda88e8185209a42f58bca62a8cb6b20fc266`  
		Last Modified: Tue, 08 Apr 2025 01:24:49 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab054931a65ce6eb03aaaea053ef5dc76ffde78efca071816c4fb4dcb34f499`  
		Last Modified: Tue, 08 Apr 2025 01:24:50 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:cd5a67855a871f08b9ea1c7c594e0ac0792e7ec64559b320cff680508cae2a7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2720301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:417c68170030f6ab0af55006508c3683fa3c6877eafa4678e99ef3c5cca621f8`

```dockerfile
```

-	Layers:
	-	`sha256:37053d94ba4f693d609b03ba15afb047eba84e57a85b148edc7b53982509d434`  
		Last Modified: Tue, 08 Apr 2025 01:24:49 GMT  
		Size: 2.7 MB (2704173 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a42a5cfa2b45c3d1c2e3a99db05f5fc6af7686c6c1a560928658d4207fdbf213`  
		Last Modified: Tue, 08 Apr 2025 01:24:49 GMT  
		Size: 16.1 KB (16128 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:latest` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:079db0bd2d86f924708a5a9e6de6c2cb7d3399cf1699f557229137991509ac54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.3 MB (75344233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64a5aa6b6d812c629928d618bac6db5743606f7239a3a3a26aaad9013d7807ef`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 17 Dec 2024 14:20:15 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1743984000'
# Tue, 17 Dec 2024 14:20:15 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
ENV CHRONOGRAF_VERSION=1.10.6
# Tue, 17 Dec 2024 14:20:15 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 17 Dec 2024 14:20:15 GMT
VOLUME [/var/lib/chronograf]
# Tue, 17 Dec 2024 14:20:15 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Dec 2024 14:20:15 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:addc1be20d0979aa781d79a726ebf749adbc030186e63a44319274194e89cfa3`  
		Last Modified: Tue, 08 Apr 2025 00:23:15 GMT  
		Size: 23.9 MB (23937867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63a4cae4b4be11b615ad8d998f77262f16fb70375bec9f1790dc5e05cce9a5d4`  
		Last Modified: Tue, 08 Apr 2025 07:41:52 GMT  
		Size: 6.5 MB (6497876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ca6161fddf786d8012dd22432d04af6253ee18bf5410e706918e4de84897a3`  
		Last Modified: Tue, 08 Apr 2025 07:41:53 GMT  
		Size: 44.9 MB (44884033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb6d2e2d402730b3e47c70c7a8aabe0d0793ccf8eb0697f589f07e8d11c841be`  
		Last Modified: Tue, 08 Apr 2025 07:41:51 GMT  
		Size: 12.2 KB (12242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:791bbc1f7129cabc57b97efda40df8c58cc17296f8496c736de68e6aa6067c61`  
		Last Modified: Tue, 08 Apr 2025 07:41:52 GMT  
		Size: 11.9 KB (11900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f8db94257bbf594cc0bd3f1146569a9345620758022b6acfc42d15cd2507084`  
		Last Modified: Tue, 08 Apr 2025 07:41:52 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:9739812ff99a5b6697d386b42a97788bd24f1863f33aa2b651293d38893bb3fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2722679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80a8caa4b6b0ca8884ce0cbd8e9fa634519d744fe87bd92a071278e921b8e34a`

```dockerfile
```

-	Layers:
	-	`sha256:7d9aabb618915996af35c9036eff103c458b5b41627180a237317e736eb873da`  
		Last Modified: Tue, 08 Apr 2025 07:41:52 GMT  
		Size: 2.7 MB (2706470 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21f063817b819d3672d30970228e48a1f0fe85493751bb5fac5cd4df2f4cd441`  
		Last Modified: Tue, 08 Apr 2025 07:41:51 GMT  
		Size: 16.2 KB (16209 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:latest` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:8d09faba86fbf271e53e98a9284de3d8208ce87338cf0859550d19201f57e982
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.0 MB (82026956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d1af4d2e6e170d6540fc4cf36fa34596f75e1266535d408024ebdfc38b6498d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 17 Dec 2024 14:20:15 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
# Tue, 17 Dec 2024 14:20:15 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
ENV CHRONOGRAF_VERSION=1.10.6
# Tue, 17 Dec 2024 14:20:15 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 17 Dec 2024 14:20:15 GMT
VOLUME [/var/lib/chronograf]
# Tue, 17 Dec 2024 14:20:15 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Dec 2024 14:20:15 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:16c9c4a8e9eef856231273efbb42a473740e8d50d74d35e6aedd04ff69fe161f`  
		Last Modified: Tue, 08 Apr 2025 00:23:04 GMT  
		Size: 28.1 MB (28066320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a6bdd77a3e8191d60b227c9f755f6f8f4b05034647007a07c82c1f6e4e88fd5`  
		Last Modified: Tue, 08 Apr 2025 06:06:40 GMT  
		Size: 7.7 MB (7652075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8259506abfecb0d9cefbd5da4e67b42720a246f8ee84521a7debe53fd757ba9`  
		Last Modified: Tue, 08 Apr 2025 06:06:41 GMT  
		Size: 46.3 MB (46284096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b303ae82d885113e78bb9e74c59a3e208975cc6de99b17cdda23c65c431f17cf`  
		Last Modified: Tue, 08 Apr 2025 06:06:39 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95d00ef9f739ada971c5ff08863c9ae4b2a5dd0fb640b56931da3efe57697831`  
		Last Modified: Tue, 08 Apr 2025 06:06:39 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8236a193f0c09a8aa82a0a8535f11cd23a4896d4e7607979e84f340192e25fa4`  
		Last Modified: Tue, 08 Apr 2025 06:06:40 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:89e855ac93e95ac2c414f1c7ba3731319ed22a82629cdb1a16686f71650629b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2720681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaffee6edec55303d2718b0134fe372c5e802220e816f225534996bcc0d9d0b4`

```dockerfile
```

-	Layers:
	-	`sha256:53bb146925fab3e7f4222f9293b00b8f7b9a918a381581d8818f36045f7b13b4`  
		Last Modified: Tue, 08 Apr 2025 06:06:40 GMT  
		Size: 2.7 MB (2704446 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:390ca5bb55650e1e1291992921fd0e2cad9783ef561abcb28b2d5e1c9dde57a5`  
		Last Modified: Tue, 08 Apr 2025 06:06:39 GMT  
		Size: 16.2 KB (16235 bytes)  
		MIME: application/vnd.in-toto+json
