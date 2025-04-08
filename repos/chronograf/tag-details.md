<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `chronograf`

-	[`chronograf:1.10`](#chronograf110)
-	[`chronograf:1.10-alpine`](#chronograf110-alpine)
-	[`chronograf:1.10.6`](#chronograf1106)
-	[`chronograf:1.10.6-alpine`](#chronograf1106-alpine)
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
$ docker pull chronograf@sha256:0c22a6c5ae0b643ad35105193413dfeb51fa6e1173097671029b816fbeb23f45
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
$ docker pull chronograf@sha256:b260a3123644b9ce63ee8aa47d7961ec53b07a7338f3b99487f2bd1a19ed8988
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.3 MB (75321453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bcb6293557107c7c70317795de5eb47dfd4729a8b296356277d8bbd1dfea931`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 17 Dec 2024 14:20:15 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1742169600'
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
	-	`sha256:676cf117f557880ff2e894692781cbce1b2a04502aff2e34b58c230b14731b8f`  
		Last Modified: Mon, 17 Mar 2025 22:18:43 GMT  
		Size: 23.9 MB (23915088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:836bf62ab11d8c3347e2b9c9875e4f5244b7c812f26387df20a42923dd493475`  
		Last Modified: Tue, 18 Mar 2025 05:01:49 GMT  
		Size: 6.5 MB (6497861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cd5e397f077f36bab298a73a6baa9cfddf9ba2855844b398cb4152dd3b2138a`  
		Last Modified: Mon, 24 Mar 2025 19:48:00 GMT  
		Size: 44.9 MB (44884055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:292e2a30424af1b957bc373b40acf6bd3dff9e9f3961a2b341e27df8199b6720`  
		Last Modified: Mon, 24 Mar 2025 19:47:58 GMT  
		Size: 12.2 KB (12236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e41885583796b497a975495b43a1ea0ca07b699187f80d457f8d8ee2941cfc63`  
		Last Modified: Mon, 24 Mar 2025 19:47:59 GMT  
		Size: 11.9 KB (11899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f6b04419aa9d9bf716af5126f25373776bf8d05bee4879eb9953e13d9150dab`  
		Last Modified: Mon, 24 Mar 2025 19:47:59 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:0230f8d433f579076e612b985a5a116266f15bf31980c92e9344405feae3892d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2722393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23f8e441d09f74baf3d0c194c1aecd74a2bfc787bcc240b4b366ce92f7aba681`

```dockerfile
```

-	Layers:
	-	`sha256:601fb24d96032b97dc376d29c2acf5270170cf4abb952dd24c4787dc8c03cdef`  
		Last Modified: Mon, 24 Mar 2025 19:47:59 GMT  
		Size: 2.7 MB (2706184 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3aeb60dc26a9921906054bc7ee7a15a5d30b6f4f7172ed892065ab8887ceff60`  
		Last Modified: Mon, 24 Mar 2025 19:47:58 GMT  
		Size: 16.2 KB (16209 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.10` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:f578c708604ef073d5a20ffe5192c6784c8a37a720800b85ffdde6345daa0037
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.0 MB (82004624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e67a035ac1f247740fc08c011f111cabc5482f3186f0f6bca30b7a5ff650d08`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 17 Dec 2024 14:20:15 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
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
	-	`sha256:d9b6365477446a79987b20560ae52637be6f54d6d2f801e16aaa0ca25dd0964b`  
		Last Modified: Mon, 17 Mar 2025 22:17:34 GMT  
		Size: 28.0 MB (28044037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2c079ee7f0b0bf943a7f05825d499d2bcdb7c98a14336bc3f01d66c7fdbbd87`  
		Last Modified: Mon, 24 Mar 2025 20:32:00 GMT  
		Size: 7.7 MB (7652096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d19111a9ad9101d6f43ea3f764707d90bf7e11e1d90f2bd605cc906985562fee`  
		Last Modified: Mon, 24 Mar 2025 20:32:00 GMT  
		Size: 46.3 MB (46284026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef0e9ebc6948e3ee716039b9299f2e9572c5865047f4b9cfb4478f9ed51fcef0`  
		Last Modified: Mon, 24 Mar 2025 20:31:58 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:474d17c66d54ed1fb6c1f0c4027f5fadc71b2fa678039b7958dff80c58c04091`  
		Last Modified: Mon, 24 Mar 2025 20:31:58 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9200ba2416a7362a2168bbbbbbec91dc8175f0be27f65f425b6f925232e29052`  
		Last Modified: Mon, 24 Mar 2025 20:31:59 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:96d3aad0a2a4b5e709891e0247a6c6561a63fba4fe9e3983ebd5a8d6420fed22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2720395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe483a2e90f446b0d86a7111dace701b3330ac57a955bad03275e5b780693ce6`

```dockerfile
```

-	Layers:
	-	`sha256:f05d4574473ddde09267e5153052c58f938fd1da1bb8a09bf089c34224ea2f0a`  
		Last Modified: Mon, 24 Mar 2025 20:31:59 GMT  
		Size: 2.7 MB (2704160 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b861aad354ed84431b47ba6777c2e776c884ff7c500d3da714fbbf8ecda66e7a`  
		Last Modified: Mon, 24 Mar 2025 20:31:58 GMT  
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

## `chronograf:1.10.6`

```console
$ docker pull chronograf@sha256:0c22a6c5ae0b643ad35105193413dfeb51fa6e1173097671029b816fbeb23f45
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `chronograf:1.10.6` - linux; amd64

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

### `chronograf:1.10.6` - unknown; unknown

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

### `chronograf:1.10.6` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:b260a3123644b9ce63ee8aa47d7961ec53b07a7338f3b99487f2bd1a19ed8988
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.3 MB (75321453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bcb6293557107c7c70317795de5eb47dfd4729a8b296356277d8bbd1dfea931`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 17 Dec 2024 14:20:15 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1742169600'
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
	-	`sha256:676cf117f557880ff2e894692781cbce1b2a04502aff2e34b58c230b14731b8f`  
		Last Modified: Mon, 17 Mar 2025 22:18:43 GMT  
		Size: 23.9 MB (23915088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:836bf62ab11d8c3347e2b9c9875e4f5244b7c812f26387df20a42923dd493475`  
		Last Modified: Tue, 18 Mar 2025 05:01:49 GMT  
		Size: 6.5 MB (6497861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cd5e397f077f36bab298a73a6baa9cfddf9ba2855844b398cb4152dd3b2138a`  
		Last Modified: Mon, 24 Mar 2025 19:48:00 GMT  
		Size: 44.9 MB (44884055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:292e2a30424af1b957bc373b40acf6bd3dff9e9f3961a2b341e27df8199b6720`  
		Last Modified: Mon, 24 Mar 2025 19:47:58 GMT  
		Size: 12.2 KB (12236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e41885583796b497a975495b43a1ea0ca07b699187f80d457f8d8ee2941cfc63`  
		Last Modified: Mon, 24 Mar 2025 19:47:59 GMT  
		Size: 11.9 KB (11899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f6b04419aa9d9bf716af5126f25373776bf8d05bee4879eb9953e13d9150dab`  
		Last Modified: Mon, 24 Mar 2025 19:47:59 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10.6` - unknown; unknown

```console
$ docker pull chronograf@sha256:0230f8d433f579076e612b985a5a116266f15bf31980c92e9344405feae3892d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2722393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23f8e441d09f74baf3d0c194c1aecd74a2bfc787bcc240b4b366ce92f7aba681`

```dockerfile
```

-	Layers:
	-	`sha256:601fb24d96032b97dc376d29c2acf5270170cf4abb952dd24c4787dc8c03cdef`  
		Last Modified: Mon, 24 Mar 2025 19:47:59 GMT  
		Size: 2.7 MB (2706184 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3aeb60dc26a9921906054bc7ee7a15a5d30b6f4f7172ed892065ab8887ceff60`  
		Last Modified: Mon, 24 Mar 2025 19:47:58 GMT  
		Size: 16.2 KB (16209 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.10.6` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:f578c708604ef073d5a20ffe5192c6784c8a37a720800b85ffdde6345daa0037
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.0 MB (82004624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e67a035ac1f247740fc08c011f111cabc5482f3186f0f6bca30b7a5ff650d08`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 17 Dec 2024 14:20:15 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
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
	-	`sha256:d9b6365477446a79987b20560ae52637be6f54d6d2f801e16aaa0ca25dd0964b`  
		Last Modified: Mon, 17 Mar 2025 22:17:34 GMT  
		Size: 28.0 MB (28044037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2c079ee7f0b0bf943a7f05825d499d2bcdb7c98a14336bc3f01d66c7fdbbd87`  
		Last Modified: Mon, 24 Mar 2025 20:32:00 GMT  
		Size: 7.7 MB (7652096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d19111a9ad9101d6f43ea3f764707d90bf7e11e1d90f2bd605cc906985562fee`  
		Last Modified: Mon, 24 Mar 2025 20:32:00 GMT  
		Size: 46.3 MB (46284026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef0e9ebc6948e3ee716039b9299f2e9572c5865047f4b9cfb4478f9ed51fcef0`  
		Last Modified: Mon, 24 Mar 2025 20:31:58 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:474d17c66d54ed1fb6c1f0c4027f5fadc71b2fa678039b7958dff80c58c04091`  
		Last Modified: Mon, 24 Mar 2025 20:31:58 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9200ba2416a7362a2168bbbbbbec91dc8175f0be27f65f425b6f925232e29052`  
		Last Modified: Mon, 24 Mar 2025 20:31:59 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10.6` - unknown; unknown

```console
$ docker pull chronograf@sha256:96d3aad0a2a4b5e709891e0247a6c6561a63fba4fe9e3983ebd5a8d6420fed22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2720395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe483a2e90f446b0d86a7111dace701b3330ac57a955bad03275e5b780693ce6`

```dockerfile
```

-	Layers:
	-	`sha256:f05d4574473ddde09267e5153052c58f938fd1da1bb8a09bf089c34224ea2f0a`  
		Last Modified: Mon, 24 Mar 2025 20:31:59 GMT  
		Size: 2.7 MB (2704160 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b861aad354ed84431b47ba6777c2e776c884ff7c500d3da714fbbf8ecda66e7a`  
		Last Modified: Mon, 24 Mar 2025 20:31:58 GMT  
		Size: 16.2 KB (16235 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.10.6-alpine`

```console
$ docker pull chronograf@sha256:357a021d3cd126c613abc52fc98c9065a2fb48f483032a725626baaa2761e3b4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.10.6-alpine` - linux; amd64

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

### `chronograf:1.10.6-alpine` - unknown; unknown

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

## `chronograf:1.7`

```console
$ docker pull chronograf@sha256:1a571f513a1408a036427c5f730fa738b9c46781bb2b8783c1fdae96c20fe97f
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
$ docker pull chronograf@sha256:4634b8da3fa1cdd66ec7f7d3509c85ca01a37a4851a7a10cd471f6ac754918a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.0 MB (61964138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3978b1dc792e87ccae956b6f30405363851af304ff78fb81c2913171353140c3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1742169600'
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
	-	`sha256:3687c9079028ac9bf763326f4be55b4e440b37b5baf0c4529715d811c7ec1718`  
		Last Modified: Mon, 17 Mar 2025 22:19:22 GMT  
		Size: 25.5 MB (25535344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8d1ca93cdfa24b7d2a8781a280eced4fbbeca2f855cecfd0310f92c72b1f3a8`  
		Last Modified: Tue, 18 Mar 2025 07:19:32 GMT  
		Size: 3.5 MB (3511650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7582cd8d20319ea4872c71629e7a13ef9452cdcc58456a40d65e173360ab7d89`  
		Last Modified: Tue, 18 Mar 2025 07:19:33 GMT  
		Size: 32.9 MB (32892750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3991c885a6914614fc424555dc507da8a3bf18dca25733ff447421518a0751cb`  
		Last Modified: Tue, 18 Mar 2025 07:19:32 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:701be1acddd8faed4b5129073ff55b58b8f51e2309c743a9ddcf697ddd7a2ba3`  
		Last Modified: Tue, 18 Mar 2025 07:19:32 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b80675c7573c809ac84505cf312c86de64172356526fe46b201d69091eb826a`  
		Last Modified: Tue, 18 Mar 2025 07:19:33 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7` - unknown; unknown

```console
$ docker pull chronograf@sha256:d5f4cb030fe66e2f7034f94ef4c963033fe8034c9c3cdcd1741450f31c524049
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2923510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aeccedb7eabc98e6550534f972936ca1116fe1a8a1cf75e7b9780e6166e0cc08`

```dockerfile
```

-	Layers:
	-	`sha256:6e4914e46ad96093846deef0c428dce476f729f8c8e7254d5f15595fe1177e12`  
		Last Modified: Tue, 18 Mar 2025 07:19:32 GMT  
		Size: 2.9 MB (2907660 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11a62e29b12984918cdb8891c62fcab6cd2d5f8388c30f866bbcdad9303249b5`  
		Last Modified: Tue, 18 Mar 2025 07:19:32 GMT  
		Size: 15.8 KB (15850 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.7` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:7837b1f9e13e0d07440705ebb31354d3ea707ffaab75385ef236786f87736bcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.0 MB (66013968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:581fc0983c4a8c824349890d283f23a4e50cdbe70a2405180a5eb141a0c35f5a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1742169600'
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
	-	`sha256:6eba8885c82049d690776150810f32585aca6c3eba49f692753434bdaee447ec`  
		Last Modified: Mon, 17 Mar 2025 22:18:52 GMT  
		Size: 28.7 MB (28745923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c79e09b72ead71f0c8003269a685ee7f33519ae49476478cf88a68c6c2bd558c`  
		Last Modified: Tue, 18 Mar 2025 04:58:33 GMT  
		Size: 4.2 MB (4210595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b00c5cc54c47e50a08d3b73a1a82f72053cf43411653ca93576c161f4cda5c7`  
		Last Modified: Tue, 18 Mar 2025 04:58:34 GMT  
		Size: 33.0 MB (33033062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2437adf3cc2dc8888af87d361cf33c5ba444dfe56b2360a85297b8a7990dda2c`  
		Last Modified: Tue, 18 Mar 2025 04:58:33 GMT  
		Size: 12.2 KB (12242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0c8ba7dab83d9c9e309de48384f8eb49145a902431902237614671bbcdc74f0`  
		Last Modified: Tue, 18 Mar 2025 04:58:33 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3f5bc823e9fd5ef8be9a32b2813f9f46a0921550ecc1b720ca4457585562c8`  
		Last Modified: Tue, 18 Mar 2025 04:58:34 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7` - unknown; unknown

```console
$ docker pull chronograf@sha256:9d70100adf9fbb7da5071f07572ac5e7407b12cddf1076326b818f7a066cfa90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2921510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f18c1595ca21a2b0e4b3a1187c48b0929d2c58fe070eb090361b1909c1a9873c`

```dockerfile
```

-	Layers:
	-	`sha256:2a56ca3ce69c827183c13f5444cc758c0cd7902c3d6f3c92a7b6c8aa4f8568ed`  
		Last Modified: Tue, 18 Mar 2025 04:58:33 GMT  
		Size: 2.9 MB (2905638 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:470bd79e965b7c8d173ec83f3db695e2bb7d4fa1d0f4937ff774a466ef691f4c`  
		Last Modified: Tue, 18 Mar 2025 04:58:33 GMT  
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
$ docker pull chronograf@sha256:1a571f513a1408a036427c5f730fa738b9c46781bb2b8783c1fdae96c20fe97f
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
$ docker pull chronograf@sha256:4634b8da3fa1cdd66ec7f7d3509c85ca01a37a4851a7a10cd471f6ac754918a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.0 MB (61964138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3978b1dc792e87ccae956b6f30405363851af304ff78fb81c2913171353140c3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1742169600'
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
	-	`sha256:3687c9079028ac9bf763326f4be55b4e440b37b5baf0c4529715d811c7ec1718`  
		Last Modified: Mon, 17 Mar 2025 22:19:22 GMT  
		Size: 25.5 MB (25535344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8d1ca93cdfa24b7d2a8781a280eced4fbbeca2f855cecfd0310f92c72b1f3a8`  
		Last Modified: Tue, 18 Mar 2025 07:19:32 GMT  
		Size: 3.5 MB (3511650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7582cd8d20319ea4872c71629e7a13ef9452cdcc58456a40d65e173360ab7d89`  
		Last Modified: Tue, 18 Mar 2025 07:19:33 GMT  
		Size: 32.9 MB (32892750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3991c885a6914614fc424555dc507da8a3bf18dca25733ff447421518a0751cb`  
		Last Modified: Tue, 18 Mar 2025 07:19:32 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:701be1acddd8faed4b5129073ff55b58b8f51e2309c743a9ddcf697ddd7a2ba3`  
		Last Modified: Tue, 18 Mar 2025 07:19:32 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b80675c7573c809ac84505cf312c86de64172356526fe46b201d69091eb826a`  
		Last Modified: Tue, 18 Mar 2025 07:19:33 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7.17` - unknown; unknown

```console
$ docker pull chronograf@sha256:d5f4cb030fe66e2f7034f94ef4c963033fe8034c9c3cdcd1741450f31c524049
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2923510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aeccedb7eabc98e6550534f972936ca1116fe1a8a1cf75e7b9780e6166e0cc08`

```dockerfile
```

-	Layers:
	-	`sha256:6e4914e46ad96093846deef0c428dce476f729f8c8e7254d5f15595fe1177e12`  
		Last Modified: Tue, 18 Mar 2025 07:19:32 GMT  
		Size: 2.9 MB (2907660 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11a62e29b12984918cdb8891c62fcab6cd2d5f8388c30f866bbcdad9303249b5`  
		Last Modified: Tue, 18 Mar 2025 07:19:32 GMT  
		Size: 15.8 KB (15850 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.7.17` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:7837b1f9e13e0d07440705ebb31354d3ea707ffaab75385ef236786f87736bcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.0 MB (66013968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:581fc0983c4a8c824349890d283f23a4e50cdbe70a2405180a5eb141a0c35f5a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1742169600'
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
	-	`sha256:6eba8885c82049d690776150810f32585aca6c3eba49f692753434bdaee447ec`  
		Last Modified: Mon, 17 Mar 2025 22:18:52 GMT  
		Size: 28.7 MB (28745923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c79e09b72ead71f0c8003269a685ee7f33519ae49476478cf88a68c6c2bd558c`  
		Last Modified: Tue, 18 Mar 2025 04:58:33 GMT  
		Size: 4.2 MB (4210595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b00c5cc54c47e50a08d3b73a1a82f72053cf43411653ca93576c161f4cda5c7`  
		Last Modified: Tue, 18 Mar 2025 04:58:34 GMT  
		Size: 33.0 MB (33033062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2437adf3cc2dc8888af87d361cf33c5ba444dfe56b2360a85297b8a7990dda2c`  
		Last Modified: Tue, 18 Mar 2025 04:58:33 GMT  
		Size: 12.2 KB (12242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0c8ba7dab83d9c9e309de48384f8eb49145a902431902237614671bbcdc74f0`  
		Last Modified: Tue, 18 Mar 2025 04:58:33 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3f5bc823e9fd5ef8be9a32b2813f9f46a0921550ecc1b720ca4457585562c8`  
		Last Modified: Tue, 18 Mar 2025 04:58:34 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7.17` - unknown; unknown

```console
$ docker pull chronograf@sha256:9d70100adf9fbb7da5071f07572ac5e7407b12cddf1076326b818f7a066cfa90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2921510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f18c1595ca21a2b0e4b3a1187c48b0929d2c58fe070eb090361b1909c1a9873c`

```dockerfile
```

-	Layers:
	-	`sha256:2a56ca3ce69c827183c13f5444cc758c0cd7902c3d6f3c92a7b6c8aa4f8568ed`  
		Last Modified: Tue, 18 Mar 2025 04:58:33 GMT  
		Size: 2.9 MB (2905638 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:470bd79e965b7c8d173ec83f3db695e2bb7d4fa1d0f4937ff774a466ef691f4c`  
		Last Modified: Tue, 18 Mar 2025 04:58:33 GMT  
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
$ docker pull chronograf@sha256:03996f38244bab17b5b2819f721759a5b6497993eb2538a62d0d24ace4ad4802
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
$ docker pull chronograf@sha256:2d35d237b936d5f81224ef44d78208c9e163f6e1a988506b93e5bbaaba03b653
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62379885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5cb83736f0e87ccfa8237274cf8b8d41ae4794e0bbd5d0f4b85fbc562c97601`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1742169600'
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
	-	`sha256:3687c9079028ac9bf763326f4be55b4e440b37b5baf0c4529715d811c7ec1718`  
		Last Modified: Mon, 17 Mar 2025 22:19:22 GMT  
		Size: 25.5 MB (25535344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:605c5d344c0fcbfd3ec727246cb26c24e86356819630333c90a0ca2ce6f53c49`  
		Last Modified: Mon, 17 Mar 2025 23:27:05 GMT  
		Size: 4.3 MB (4285211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3b9cc7cf220e8d536073a4d46103bdb0d89e64803465eba981e5e5caa373f40`  
		Last Modified: Tue, 18 Mar 2025 07:18:19 GMT  
		Size: 32.5 MB (32534938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787d44903937a4a34f31747aa0560ab17ef8bed2064f9aeae0e32e891a0953f9`  
		Last Modified: Tue, 18 Mar 2025 07:18:18 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efb5221b579581df41c5704a6810e3865fe7631d1693d79031ab7ddf9cfbc9dd`  
		Last Modified: Tue, 18 Mar 2025 07:18:18 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6803ad9a7b6eaee7b3867a16aa772180447d3723932d0f0af1ccb0385af7b1dd`  
		Last Modified: Tue, 18 Mar 2025 07:18:18 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8` - unknown; unknown

```console
$ docker pull chronograf@sha256:2df3a2c4d99813e11ab0d0c43e2f442fa618d75d61b5e90f1eee8f5c1ae93c81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2980238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a75acdd3f6903436fafa2910009b5a31765f2f03ea4fac1ceca55673b0a7e7e`

```dockerfile
```

-	Layers:
	-	`sha256:8d37ea437455345a50789ff57e0094ac5beb97c295f7064e93c2a32325fd6520`  
		Last Modified: Tue, 18 Mar 2025 07:18:18 GMT  
		Size: 3.0 MB (2964348 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4fb6b3e3d3462fb82d29cb0c41daa0d0cac8df7a6208d04da973717cd8fbeaf`  
		Last Modified: Tue, 18 Mar 2025 07:18:18 GMT  
		Size: 15.9 KB (15890 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.8` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:0049863b9b8e7cd67c5e1a312b89560ab92219d69a534147a2e2411fe5a7480d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66203412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:008774c5a8878a2141bf474b6a77f981dff9659f66c38b25ec5375dc436f1932`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1742169600'
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
	-	`sha256:6eba8885c82049d690776150810f32585aca6c3eba49f692753434bdaee447ec`  
		Last Modified: Mon, 17 Mar 2025 22:18:52 GMT  
		Size: 28.7 MB (28745923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:009b00c806d29b7dae38f39212f3427da1010214541c15b5ef1dc30e6b6836c5`  
		Last Modified: Tue, 18 Mar 2025 04:57:35 GMT  
		Size: 5.0 MB (5003593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2cd89b82febb031b41d22193b96517b231dd947a30675beea1428a8df02b8d1`  
		Last Modified: Tue, 18 Mar 2025 04:57:58 GMT  
		Size: 32.4 MB (32429510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a911023f21724f4c30678b4f12469a64071840f3df4e043c47729dd96561e6ba`  
		Last Modified: Tue, 18 Mar 2025 04:57:57 GMT  
		Size: 12.2 KB (12244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42d70f38e63c3d6b3a408ca489504a18aa86f9f1a69300a4bef99d5c237dde83`  
		Last Modified: Tue, 18 Mar 2025 04:57:57 GMT  
		Size: 11.9 KB (11903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d24ba58a182108bb82de43658a21fd69b77a342c9294edce39f2270a77db0b89`  
		Last Modified: Tue, 18 Mar 2025 04:57:57 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8` - unknown; unknown

```console
$ docker pull chronograf@sha256:182c468baf68977268e2e542eebb1c8f43ee32759789fccb5b8a91bfe47ebdd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2978238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:076b8087bf548393f63e6baa75abe68cde5a564186dda5dbb31111d924fe6ecc`

```dockerfile
```

-	Layers:
	-	`sha256:d5d095729605b9adfd4e9810f22275d270b0ea8cdb601b04afcfffcb4d172bca`  
		Last Modified: Tue, 18 Mar 2025 04:57:57 GMT  
		Size: 3.0 MB (2962326 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b05e3dd2266e63bde7ee4020c9cee68df87fd3c690a0de8aef6b3ce3d20004b4`  
		Last Modified: Tue, 18 Mar 2025 04:57:57 GMT  
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
$ docker pull chronograf@sha256:03996f38244bab17b5b2819f721759a5b6497993eb2538a62d0d24ace4ad4802
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
$ docker pull chronograf@sha256:2d35d237b936d5f81224ef44d78208c9e163f6e1a988506b93e5bbaaba03b653
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62379885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5cb83736f0e87ccfa8237274cf8b8d41ae4794e0bbd5d0f4b85fbc562c97601`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1742169600'
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
	-	`sha256:3687c9079028ac9bf763326f4be55b4e440b37b5baf0c4529715d811c7ec1718`  
		Last Modified: Mon, 17 Mar 2025 22:19:22 GMT  
		Size: 25.5 MB (25535344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:605c5d344c0fcbfd3ec727246cb26c24e86356819630333c90a0ca2ce6f53c49`  
		Last Modified: Mon, 17 Mar 2025 23:27:05 GMT  
		Size: 4.3 MB (4285211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3b9cc7cf220e8d536073a4d46103bdb0d89e64803465eba981e5e5caa373f40`  
		Last Modified: Tue, 18 Mar 2025 07:18:19 GMT  
		Size: 32.5 MB (32534938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787d44903937a4a34f31747aa0560ab17ef8bed2064f9aeae0e32e891a0953f9`  
		Last Modified: Tue, 18 Mar 2025 07:18:18 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efb5221b579581df41c5704a6810e3865fe7631d1693d79031ab7ddf9cfbc9dd`  
		Last Modified: Tue, 18 Mar 2025 07:18:18 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6803ad9a7b6eaee7b3867a16aa772180447d3723932d0f0af1ccb0385af7b1dd`  
		Last Modified: Tue, 18 Mar 2025 07:18:18 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:2df3a2c4d99813e11ab0d0c43e2f442fa618d75d61b5e90f1eee8f5c1ae93c81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2980238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a75acdd3f6903436fafa2910009b5a31765f2f03ea4fac1ceca55673b0a7e7e`

```dockerfile
```

-	Layers:
	-	`sha256:8d37ea437455345a50789ff57e0094ac5beb97c295f7064e93c2a32325fd6520`  
		Last Modified: Tue, 18 Mar 2025 07:18:18 GMT  
		Size: 3.0 MB (2964348 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4fb6b3e3d3462fb82d29cb0c41daa0d0cac8df7a6208d04da973717cd8fbeaf`  
		Last Modified: Tue, 18 Mar 2025 07:18:18 GMT  
		Size: 15.9 KB (15890 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.8.10` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:0049863b9b8e7cd67c5e1a312b89560ab92219d69a534147a2e2411fe5a7480d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66203412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:008774c5a8878a2141bf474b6a77f981dff9659f66c38b25ec5375dc436f1932`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1742169600'
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
	-	`sha256:6eba8885c82049d690776150810f32585aca6c3eba49f692753434bdaee447ec`  
		Last Modified: Mon, 17 Mar 2025 22:18:52 GMT  
		Size: 28.7 MB (28745923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:009b00c806d29b7dae38f39212f3427da1010214541c15b5ef1dc30e6b6836c5`  
		Last Modified: Tue, 18 Mar 2025 04:57:35 GMT  
		Size: 5.0 MB (5003593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2cd89b82febb031b41d22193b96517b231dd947a30675beea1428a8df02b8d1`  
		Last Modified: Tue, 18 Mar 2025 04:57:58 GMT  
		Size: 32.4 MB (32429510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a911023f21724f4c30678b4f12469a64071840f3df4e043c47729dd96561e6ba`  
		Last Modified: Tue, 18 Mar 2025 04:57:57 GMT  
		Size: 12.2 KB (12244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42d70f38e63c3d6b3a408ca489504a18aa86f9f1a69300a4bef99d5c237dde83`  
		Last Modified: Tue, 18 Mar 2025 04:57:57 GMT  
		Size: 11.9 KB (11903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d24ba58a182108bb82de43658a21fd69b77a342c9294edce39f2270a77db0b89`  
		Last Modified: Tue, 18 Mar 2025 04:57:57 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:182c468baf68977268e2e542eebb1c8f43ee32759789fccb5b8a91bfe47ebdd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2978238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:076b8087bf548393f63e6baa75abe68cde5a564186dda5dbb31111d924fe6ecc`

```dockerfile
```

-	Layers:
	-	`sha256:d5d095729605b9adfd4e9810f22275d270b0ea8cdb601b04afcfffcb4d172bca`  
		Last Modified: Tue, 18 Mar 2025 04:57:57 GMT  
		Size: 3.0 MB (2962326 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b05e3dd2266e63bde7ee4020c9cee68df87fd3c690a0de8aef6b3ce3d20004b4`  
		Last Modified: Tue, 18 Mar 2025 04:57:57 GMT  
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
$ docker pull chronograf@sha256:aa8657afc7f0c7f3958f70aeebdab50a5b820757e2bddc871a8bab51071873c9
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
$ docker pull chronograf@sha256:c8703e6642fa1be183cf41ae890e964a3d1412e2d79689afd037c98d34c8fd1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.2 MB (63156410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:041f5b21713351624328e33186eedb6588bb0a370f86e98ac68a3a997a4a0fe0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1742169600'
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
	-	`sha256:3687c9079028ac9bf763326f4be55b4e440b37b5baf0c4529715d811c7ec1718`  
		Last Modified: Mon, 17 Mar 2025 22:19:22 GMT  
		Size: 25.5 MB (25535344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:605c5d344c0fcbfd3ec727246cb26c24e86356819630333c90a0ca2ce6f53c49`  
		Last Modified: Mon, 17 Mar 2025 23:27:05 GMT  
		Size: 4.3 MB (4285211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f901a908badd355fc1beaa92e4bbe3b9974c56ff7edfd3b43a6ec24a7af57fa`  
		Last Modified: Mon, 17 Mar 2025 23:27:06 GMT  
		Size: 33.3 MB (33311472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:099ad31178dc58c371aed0b5283dfc65dd4fd6977d4b9e5413a72a73108cb3d6`  
		Last Modified: Mon, 17 Mar 2025 23:27:05 GMT  
		Size: 12.2 KB (12242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:801863779a4fc55c2ed1a0f9a2d17424e193b7d7a210af43afb7b9b21889c3d3`  
		Last Modified: Mon, 17 Mar 2025 23:27:05 GMT  
		Size: 11.9 KB (11901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8b839129c0a0e91bc2fb90c551ba8869727f672c548cd5f2cb6d898642122c9`  
		Last Modified: Mon, 17 Mar 2025 23:27:06 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9` - unknown; unknown

```console
$ docker pull chronograf@sha256:86d2daf70ee359a31f3ceec233c009339e2c5cbbac18124eca433dcc5c7093e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2985441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d50d229f8a62fcd9a0977f7ab3cb247c1d04831960110e4230d90090ae0c80a`

```dockerfile
```

-	Layers:
	-	`sha256:439d1ff9b7a5c9f7d91a03b52210bf36aa5116c43b1ba9efad0fae4475b8daf0`  
		Last Modified: Mon, 17 Mar 2025 23:27:05 GMT  
		Size: 3.0 MB (2969558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:741a3f4d84913d2f2519a6561a0eba4016d298070039bc8b25451faa6f85fa4d`  
		Last Modified: Mon, 17 Mar 2025 23:27:05 GMT  
		Size: 15.9 KB (15883 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.9` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:c2955440eddbe2f797f904243d094813687cfccb8bb6a152d36840024d7340ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.0 MB (66955512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6db383263ed052c8cde8a8cbf4194678290b7d98194f437814b5a231fda68128`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1742169600'
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
	-	`sha256:6eba8885c82049d690776150810f32585aca6c3eba49f692753434bdaee447ec`  
		Last Modified: Mon, 17 Mar 2025 22:18:52 GMT  
		Size: 28.7 MB (28745923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:009b00c806d29b7dae38f39212f3427da1010214541c15b5ef1dc30e6b6836c5`  
		Last Modified: Tue, 18 Mar 2025 04:57:35 GMT  
		Size: 5.0 MB (5003593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d80b24ee2385306e5afad723b37d06995df906dffdb482420700cc55f550c56`  
		Last Modified: Tue, 18 Mar 2025 04:57:36 GMT  
		Size: 33.2 MB (33181607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42bc4073be23696b46a5d8d2c4dea0fb313213008dc24198a4da7d3468b50db3`  
		Last Modified: Tue, 18 Mar 2025 04:57:35 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd362e9401f017c4f2ddd3bfa77a77ab0fcb4dfc11b6d36e770a0c9fa2c8e670`  
		Last Modified: Tue, 18 Mar 2025 04:57:35 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:424fcb19c6d1d3832f2bb723b0885e903dccaee937ed7147953da8bed1f3fb22`  
		Last Modified: Tue, 18 Mar 2025 04:57:36 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9` - unknown; unknown

```console
$ docker pull chronograf@sha256:b8fd00cfc4e84b2c7832e55c4d3c36aa2db6f0d71ccbf165034340d11571fbfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2983441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aa4831bf7992b19c710c41de9c980ed3f1ef91168f152fa62a613522d5c1c6f`

```dockerfile
```

-	Layers:
	-	`sha256:89a4bbca52f30694eae8700eff8c5bab6fbd29b0c3fb16f4a80e499e8cf67f02`  
		Last Modified: Tue, 18 Mar 2025 04:57:35 GMT  
		Size: 3.0 MB (2967536 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b4c212bc6ba65beee8f440ee750fcd5df7936096cbdc9ed593de3b743fdda51`  
		Last Modified: Tue, 18 Mar 2025 04:57:35 GMT  
		Size: 15.9 KB (15905 bytes)  
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
$ docker pull chronograf@sha256:aa8657afc7f0c7f3958f70aeebdab50a5b820757e2bddc871a8bab51071873c9
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
$ docker pull chronograf@sha256:c8703e6642fa1be183cf41ae890e964a3d1412e2d79689afd037c98d34c8fd1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.2 MB (63156410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:041f5b21713351624328e33186eedb6588bb0a370f86e98ac68a3a997a4a0fe0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1742169600'
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
	-	`sha256:3687c9079028ac9bf763326f4be55b4e440b37b5baf0c4529715d811c7ec1718`  
		Last Modified: Mon, 17 Mar 2025 22:19:22 GMT  
		Size: 25.5 MB (25535344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:605c5d344c0fcbfd3ec727246cb26c24e86356819630333c90a0ca2ce6f53c49`  
		Last Modified: Mon, 17 Mar 2025 23:27:05 GMT  
		Size: 4.3 MB (4285211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f901a908badd355fc1beaa92e4bbe3b9974c56ff7edfd3b43a6ec24a7af57fa`  
		Last Modified: Mon, 17 Mar 2025 23:27:06 GMT  
		Size: 33.3 MB (33311472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:099ad31178dc58c371aed0b5283dfc65dd4fd6977d4b9e5413a72a73108cb3d6`  
		Last Modified: Mon, 17 Mar 2025 23:27:05 GMT  
		Size: 12.2 KB (12242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:801863779a4fc55c2ed1a0f9a2d17424e193b7d7a210af43afb7b9b21889c3d3`  
		Last Modified: Mon, 17 Mar 2025 23:27:05 GMT  
		Size: 11.9 KB (11901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8b839129c0a0e91bc2fb90c551ba8869727f672c548cd5f2cb6d898642122c9`  
		Last Modified: Mon, 17 Mar 2025 23:27:06 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9.4` - unknown; unknown

```console
$ docker pull chronograf@sha256:86d2daf70ee359a31f3ceec233c009339e2c5cbbac18124eca433dcc5c7093e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2985441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d50d229f8a62fcd9a0977f7ab3cb247c1d04831960110e4230d90090ae0c80a`

```dockerfile
```

-	Layers:
	-	`sha256:439d1ff9b7a5c9f7d91a03b52210bf36aa5116c43b1ba9efad0fae4475b8daf0`  
		Last Modified: Mon, 17 Mar 2025 23:27:05 GMT  
		Size: 3.0 MB (2969558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:741a3f4d84913d2f2519a6561a0eba4016d298070039bc8b25451faa6f85fa4d`  
		Last Modified: Mon, 17 Mar 2025 23:27:05 GMT  
		Size: 15.9 KB (15883 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.9.4` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:c2955440eddbe2f797f904243d094813687cfccb8bb6a152d36840024d7340ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.0 MB (66955512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6db383263ed052c8cde8a8cbf4194678290b7d98194f437814b5a231fda68128`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1742169600'
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
	-	`sha256:6eba8885c82049d690776150810f32585aca6c3eba49f692753434bdaee447ec`  
		Last Modified: Mon, 17 Mar 2025 22:18:52 GMT  
		Size: 28.7 MB (28745923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:009b00c806d29b7dae38f39212f3427da1010214541c15b5ef1dc30e6b6836c5`  
		Last Modified: Tue, 18 Mar 2025 04:57:35 GMT  
		Size: 5.0 MB (5003593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d80b24ee2385306e5afad723b37d06995df906dffdb482420700cc55f550c56`  
		Last Modified: Tue, 18 Mar 2025 04:57:36 GMT  
		Size: 33.2 MB (33181607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42bc4073be23696b46a5d8d2c4dea0fb313213008dc24198a4da7d3468b50db3`  
		Last Modified: Tue, 18 Mar 2025 04:57:35 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd362e9401f017c4f2ddd3bfa77a77ab0fcb4dfc11b6d36e770a0c9fa2c8e670`  
		Last Modified: Tue, 18 Mar 2025 04:57:35 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:424fcb19c6d1d3832f2bb723b0885e903dccaee937ed7147953da8bed1f3fb22`  
		Last Modified: Tue, 18 Mar 2025 04:57:36 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9.4` - unknown; unknown

```console
$ docker pull chronograf@sha256:b8fd00cfc4e84b2c7832e55c4d3c36aa2db6f0d71ccbf165034340d11571fbfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2983441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aa4831bf7992b19c710c41de9c980ed3f1ef91168f152fa62a613522d5c1c6f`

```dockerfile
```

-	Layers:
	-	`sha256:89a4bbca52f30694eae8700eff8c5bab6fbd29b0c3fb16f4a80e499e8cf67f02`  
		Last Modified: Tue, 18 Mar 2025 04:57:35 GMT  
		Size: 3.0 MB (2967536 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b4c212bc6ba65beee8f440ee750fcd5df7936096cbdc9ed593de3b743fdda51`  
		Last Modified: Tue, 18 Mar 2025 04:57:35 GMT  
		Size: 15.9 KB (15905 bytes)  
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
$ docker pull chronograf@sha256:0c22a6c5ae0b643ad35105193413dfeb51fa6e1173097671029b816fbeb23f45
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
$ docker pull chronograf@sha256:b260a3123644b9ce63ee8aa47d7961ec53b07a7338f3b99487f2bd1a19ed8988
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.3 MB (75321453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bcb6293557107c7c70317795de5eb47dfd4729a8b296356277d8bbd1dfea931`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 17 Dec 2024 14:20:15 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1742169600'
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
	-	`sha256:676cf117f557880ff2e894692781cbce1b2a04502aff2e34b58c230b14731b8f`  
		Last Modified: Mon, 17 Mar 2025 22:18:43 GMT  
		Size: 23.9 MB (23915088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:836bf62ab11d8c3347e2b9c9875e4f5244b7c812f26387df20a42923dd493475`  
		Last Modified: Tue, 18 Mar 2025 05:01:49 GMT  
		Size: 6.5 MB (6497861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cd5e397f077f36bab298a73a6baa9cfddf9ba2855844b398cb4152dd3b2138a`  
		Last Modified: Mon, 24 Mar 2025 19:48:00 GMT  
		Size: 44.9 MB (44884055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:292e2a30424af1b957bc373b40acf6bd3dff9e9f3961a2b341e27df8199b6720`  
		Last Modified: Mon, 24 Mar 2025 19:47:58 GMT  
		Size: 12.2 KB (12236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e41885583796b497a975495b43a1ea0ca07b699187f80d457f8d8ee2941cfc63`  
		Last Modified: Mon, 24 Mar 2025 19:47:59 GMT  
		Size: 11.9 KB (11899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f6b04419aa9d9bf716af5126f25373776bf8d05bee4879eb9953e13d9150dab`  
		Last Modified: Mon, 24 Mar 2025 19:47:59 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:0230f8d433f579076e612b985a5a116266f15bf31980c92e9344405feae3892d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2722393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23f8e441d09f74baf3d0c194c1aecd74a2bfc787bcc240b4b366ce92f7aba681`

```dockerfile
```

-	Layers:
	-	`sha256:601fb24d96032b97dc376d29c2acf5270170cf4abb952dd24c4787dc8c03cdef`  
		Last Modified: Mon, 24 Mar 2025 19:47:59 GMT  
		Size: 2.7 MB (2706184 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3aeb60dc26a9921906054bc7ee7a15a5d30b6f4f7172ed892065ab8887ceff60`  
		Last Modified: Mon, 24 Mar 2025 19:47:58 GMT  
		Size: 16.2 KB (16209 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:latest` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:f578c708604ef073d5a20ffe5192c6784c8a37a720800b85ffdde6345daa0037
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.0 MB (82004624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e67a035ac1f247740fc08c011f111cabc5482f3186f0f6bca30b7a5ff650d08`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 17 Dec 2024 14:20:15 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
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
	-	`sha256:d9b6365477446a79987b20560ae52637be6f54d6d2f801e16aaa0ca25dd0964b`  
		Last Modified: Mon, 17 Mar 2025 22:17:34 GMT  
		Size: 28.0 MB (28044037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2c079ee7f0b0bf943a7f05825d499d2bcdb7c98a14336bc3f01d66c7fdbbd87`  
		Last Modified: Mon, 24 Mar 2025 20:32:00 GMT  
		Size: 7.7 MB (7652096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d19111a9ad9101d6f43ea3f764707d90bf7e11e1d90f2bd605cc906985562fee`  
		Last Modified: Mon, 24 Mar 2025 20:32:00 GMT  
		Size: 46.3 MB (46284026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef0e9ebc6948e3ee716039b9299f2e9572c5865047f4b9cfb4478f9ed51fcef0`  
		Last Modified: Mon, 24 Mar 2025 20:31:58 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:474d17c66d54ed1fb6c1f0c4027f5fadc71b2fa678039b7958dff80c58c04091`  
		Last Modified: Mon, 24 Mar 2025 20:31:58 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9200ba2416a7362a2168bbbbbbec91dc8175f0be27f65f425b6f925232e29052`  
		Last Modified: Mon, 24 Mar 2025 20:31:59 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:96d3aad0a2a4b5e709891e0247a6c6561a63fba4fe9e3983ebd5a8d6420fed22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2720395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe483a2e90f446b0d86a7111dace701b3330ac57a955bad03275e5b780693ce6`

```dockerfile
```

-	Layers:
	-	`sha256:f05d4574473ddde09267e5153052c58f938fd1da1bb8a09bf089c34224ea2f0a`  
		Last Modified: Mon, 24 Mar 2025 20:31:59 GMT  
		Size: 2.7 MB (2704160 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b861aad354ed84431b47ba6777c2e776c884ff7c500d3da714fbbf8ecda66e7a`  
		Last Modified: Mon, 24 Mar 2025 20:31:58 GMT  
		Size: 16.2 KB (16235 bytes)  
		MIME: application/vnd.in-toto+json
