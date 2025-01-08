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
$ docker pull chronograf@sha256:b494e3f3eb6e647b352a93e639623cc6e854181c9d46a93e9b31e717f5074b8c
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
$ docker pull chronograf@sha256:6d6e2d67ef9cf89d6996942538989783fc8b3f91167f50841f9d8506369c72a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.2 MB (83154509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a0670664e2e0faf522c9087986ad3de12c4aba0585d409de31408553f0dd012`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
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
	-	`sha256:fd674058ff8f8cfa7fb8a20c006fc0128541cbbad7f7f7f28df570d08f9e4d92`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 28.2 MB (28231581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07687c0360bda289fea7f2a79d82292cbe6df4c80c8424a9073cc8381ee26269`  
		Last Modified: Tue, 24 Dec 2024 22:25:56 GMT  
		Size: 7.7 MB (7680873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:767cb31ef8d1819a81d3ff15fbee3ea57bf51c34324ff78484f03319e16c14bc`  
		Last Modified: Tue, 24 Dec 2024 22:25:57 GMT  
		Size: 47.2 MB (47217584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ae16e897c30f0ef8e2220d5cf12238b47c7dd479da1a541ce5e1dc2e124a1a6`  
		Last Modified: Tue, 24 Dec 2024 22:25:55 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f03b87843e34ecc6c966cde512b43bc5fe6cb9b03f5b3893d5119675caf1772`  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:967238f4eab21ca6c33f2dc208e381ad7d895d66fa0d1e9bc3cf2211f00d894f`  
		Last Modified: Tue, 24 Dec 2024 22:25:56 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:d8b32bee1973167d2abd19fc3e19747eaf5345d478f5ffd9cb07867b6b2de9e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2719989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7441887b68abb2a2cc80a500e90a8567e98e0b8529f2cf3155641245c93a0fd3`

```dockerfile
```

-	Layers:
	-	`sha256:5bea8c2a06958727ce0210bd47562fd31721974f71638aa7116f9db1c6acbf96`  
		Last Modified: Tue, 24 Dec 2024 22:25:55 GMT  
		Size: 2.7 MB (2703861 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:258ce8fe84e595d08f1bad1f0e307596f49dc98ce1e13ceb085385d56fe01c7e`  
		Last Modified: Tue, 24 Dec 2024 22:25:55 GMT  
		Size: 16.1 KB (16128 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.10` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:902f9e124ef8eec6c6d6aaf937dbb351f8fbacba944250f4c20d1c548562ad11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.5 MB (74538543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09a47e055aad54318e8f2ff6dc0e255fab7e01a069a3554e2a719da9610348b0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1734912000'
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
	-	`sha256:24f0da30a772db626789cda3e7b0911098d07574c40b30be943d43dec3ed685f`  
		Last Modified: Tue, 24 Dec 2024 21:33:51 GMT  
		Size: 23.9 MB (23933522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a587153466beafd4a360abbe5227775fc6eb4f96163ff031f27ae280fbd146fb`  
		Last Modified: Wed, 25 Dec 2024 03:48:06 GMT  
		Size: 6.3 MB (6304249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:624273166d9b9dacbd343713c47d88140ca26bea1b6658b142897d4b2df9ebf1`  
		Last Modified: Wed, 25 Dec 2024 03:48:07 GMT  
		Size: 44.3 MB (44276315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb7936cd4fd8f299aa0fbf53ae0359605709f585ef631e09a1c56f056e388052`  
		Last Modified: Wed, 25 Dec 2024 03:48:06 GMT  
		Size: 12.2 KB (12241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4fb71a77718411db1d6fba7cd6cf5285481c6aa627fb6445de8c4127f06157f`  
		Last Modified: Wed, 25 Dec 2024 03:48:06 GMT  
		Size: 11.9 KB (11901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bd9b5d9635a02e3542dcd753d350662856b78a90805becda9f0f6df2b5499eb`  
		Last Modified: Wed, 25 Dec 2024 03:48:07 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:ccc99f48f31a9a61144299934ece16f81e3ead8caaf292e36e3c0d06edf456dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2722365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f34eac170ebb6e4736416f3d82546f9b45a22f5725f473e8ceac4b711e57017`

```dockerfile
```

-	Layers:
	-	`sha256:328f2d718a94e63d68a0992dd9b2063e42e664c8d2fb65f0cba9d7357f6d6578`  
		Last Modified: Wed, 25 Dec 2024 03:48:06 GMT  
		Size: 2.7 MB (2706158 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da1f387e2e6bf4b4a2bc73da901c5c3040bc3de0e55e0a86dbd36920bead94fd`  
		Last Modified: Wed, 25 Dec 2024 03:48:06 GMT  
		Size: 16.2 KB (16207 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.10` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:9636dae65e9631cf82030227df43ce5a21a7f0684ef566279545187d8bc6cabf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.5 MB (80513234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c459246fb31ffeff8ee987e4e19750f98ac33a42fcc74c2a8b145dfa2c48f67d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
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
	-	`sha256:f5c6876bb3d7d368455916fa98c705330bd8a8d9c080ccea8fe4c4b35a2ecb1f`  
		Last Modified: Tue, 24 Dec 2024 21:34:20 GMT  
		Size: 28.1 MB (28058723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:232f29504ec153209d0d6933a57ff49bae77c7a6234e88fcaf11cad8a7723bee`  
		Last Modified: Wed, 25 Dec 2024 01:52:46 GMT  
		Size: 7.5 MB (7459496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b2d2416f3e06d017c146f7a008f7e832c79d4d743507977252bfad16ccc0f51`  
		Last Modified: Wed, 25 Dec 2024 01:52:47 GMT  
		Size: 45.0 MB (44970555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9c2199ac63999a5d396dd76b0f697485319d69a8bfd129d09eecd6edb26fd79`  
		Last Modified: Wed, 25 Dec 2024 01:52:46 GMT  
		Size: 12.2 KB (12243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0245154bee61145c1748e294d72f49b69d7eb92fe78d4630b386771a731479bc`  
		Last Modified: Wed, 25 Dec 2024 01:52:46 GMT  
		Size: 11.9 KB (11902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:016d64276c8a4c1da71ef108932f169f0ee0fce7f101fccf20bd38daec3d4e07`  
		Last Modified: Wed, 25 Dec 2024 01:52:46 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:f28bf7b20289699eb40567193016ae5cdaba2b5d26aeb72ef42cce03fc7d22e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2720369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5202c10d949b0915ae82ce7488826f450a9e0f4a360275b8c35f2fa907184ccc`

```dockerfile
```

-	Layers:
	-	`sha256:b4af31a11ba8ca753ae64b866a74ffb5d0db1c18f70d5da361e6a4b0c5aa9cfd`  
		Last Modified: Wed, 25 Dec 2024 01:52:46 GMT  
		Size: 2.7 MB (2704134 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fbd98a0ed9b4d372cc9ea8ab71090909acd3f2734850cf0288363ec174da8b31`  
		Last Modified: Wed, 25 Dec 2024 01:52:45 GMT  
		Size: 16.2 KB (16235 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.10-alpine`

```console
$ docker pull chronograf@sha256:dde838ae1b743eb4d98d4b29b992fb7444b632ecbe2bf1b14e5bf78a96bcffa4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.10-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:ef35193e7e590e0a03c8550d74db0bec87be56cd5a15b1f020e966c6e6f78fb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31785614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c272e549048210a3ab50069f88ac438ed4a1707214e0b3289f84f0f491b34345`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD alpine-minirootfs-3.20.4-x86_64.tar.gz / # buildkit
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
	-	`sha256:63b69af3dc5582ce6b63be03623e334ccd4e5cb4bde42702bbfc7a986a1bf432`  
		Last Modified: Tue, 07 Jan 2025 02:28:35 GMT  
		Size: 3.6 MB (3613999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c46d8447fa31dea56913880abdd6f87f37a1a1f14aa39842807294d35b1db0d`  
		Last Modified: Tue, 07 Jan 2025 03:31:06 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fd617a6972020255d51696c8d3bfb0786fd896142684197413244eee22bc80a`  
		Last Modified: Tue, 07 Jan 2025 03:31:07 GMT  
		Size: 280.8 KB (280840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0487a8767300fb6ef70b3919b2fb90c086f446b646300015dcc0b044d9e5c8d`  
		Last Modified: Tue, 07 Jan 2025 03:31:08 GMT  
		Size: 27.9 MB (27866061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a04b3562cd1e0d44c469b817017c1201637c902bf3bd66a827b7a58eff33672`  
		Last Modified: Tue, 07 Jan 2025 03:31:07 GMT  
		Size: 12.2 KB (12241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01cb613e5324cd9d0a318d9f6ae96447ee7a0e708df412749fa68d9742015fe6`  
		Size: 11.9 KB (11901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a7bd88632473de5cac4c883ec9470a631e2fe300d21c49f850ae0649e48e02`  
		Last Modified: Tue, 07 Jan 2025 03:31:08 GMT  
		Size: 292.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:c7c0fc8d91df4e8247bf270f41096b92d1e798292131a24a526aa32cefe376a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.6 KB (253572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ddbcc06bbcdf739077f575ab496a6239c9ad10d086d07c0861161d270644d2d`

```dockerfile
```

-	Layers:
	-	`sha256:bfd112895266bbd1c01511dd3dcdd6257f837bab85bcfc0b208e594614f00913`  
		Last Modified: Tue, 07 Jan 2025 03:31:07 GMT  
		Size: 235.7 KB (235717 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f078ec94cbf82ebe831b16a9d2b06edf070b1ab167af5e09aadd4cedad2d42f`  
		Last Modified: Tue, 07 Jan 2025 03:31:07 GMT  
		Size: 17.9 KB (17855 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.10.5`

```console
$ docker pull chronograf@sha256:b494e3f3eb6e647b352a93e639623cc6e854181c9d46a93e9b31e717f5074b8c
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
$ docker pull chronograf@sha256:6d6e2d67ef9cf89d6996942538989783fc8b3f91167f50841f9d8506369c72a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.2 MB (83154509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a0670664e2e0faf522c9087986ad3de12c4aba0585d409de31408553f0dd012`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
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
	-	`sha256:fd674058ff8f8cfa7fb8a20c006fc0128541cbbad7f7f7f28df570d08f9e4d92`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 28.2 MB (28231581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07687c0360bda289fea7f2a79d82292cbe6df4c80c8424a9073cc8381ee26269`  
		Last Modified: Tue, 24 Dec 2024 22:25:56 GMT  
		Size: 7.7 MB (7680873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:767cb31ef8d1819a81d3ff15fbee3ea57bf51c34324ff78484f03319e16c14bc`  
		Last Modified: Tue, 24 Dec 2024 22:25:57 GMT  
		Size: 47.2 MB (47217584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ae16e897c30f0ef8e2220d5cf12238b47c7dd479da1a541ce5e1dc2e124a1a6`  
		Last Modified: Tue, 24 Dec 2024 22:25:55 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f03b87843e34ecc6c966cde512b43bc5fe6cb9b03f5b3893d5119675caf1772`  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:967238f4eab21ca6c33f2dc208e381ad7d895d66fa0d1e9bc3cf2211f00d894f`  
		Last Modified: Tue, 24 Dec 2024 22:25:56 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10.5` - unknown; unknown

```console
$ docker pull chronograf@sha256:d8b32bee1973167d2abd19fc3e19747eaf5345d478f5ffd9cb07867b6b2de9e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2719989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7441887b68abb2a2cc80a500e90a8567e98e0b8529f2cf3155641245c93a0fd3`

```dockerfile
```

-	Layers:
	-	`sha256:5bea8c2a06958727ce0210bd47562fd31721974f71638aa7116f9db1c6acbf96`  
		Last Modified: Tue, 24 Dec 2024 22:25:55 GMT  
		Size: 2.7 MB (2703861 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:258ce8fe84e595d08f1bad1f0e307596f49dc98ce1e13ceb085385d56fe01c7e`  
		Last Modified: Tue, 24 Dec 2024 22:25:55 GMT  
		Size: 16.1 KB (16128 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.10.5` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:902f9e124ef8eec6c6d6aaf937dbb351f8fbacba944250f4c20d1c548562ad11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.5 MB (74538543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09a47e055aad54318e8f2ff6dc0e255fab7e01a069a3554e2a719da9610348b0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1734912000'
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
	-	`sha256:24f0da30a772db626789cda3e7b0911098d07574c40b30be943d43dec3ed685f`  
		Last Modified: Tue, 24 Dec 2024 21:33:51 GMT  
		Size: 23.9 MB (23933522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a587153466beafd4a360abbe5227775fc6eb4f96163ff031f27ae280fbd146fb`  
		Last Modified: Wed, 25 Dec 2024 03:48:06 GMT  
		Size: 6.3 MB (6304249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:624273166d9b9dacbd343713c47d88140ca26bea1b6658b142897d4b2df9ebf1`  
		Last Modified: Wed, 25 Dec 2024 03:48:07 GMT  
		Size: 44.3 MB (44276315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb7936cd4fd8f299aa0fbf53ae0359605709f585ef631e09a1c56f056e388052`  
		Last Modified: Wed, 25 Dec 2024 03:48:06 GMT  
		Size: 12.2 KB (12241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4fb71a77718411db1d6fba7cd6cf5285481c6aa627fb6445de8c4127f06157f`  
		Last Modified: Wed, 25 Dec 2024 03:48:06 GMT  
		Size: 11.9 KB (11901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bd9b5d9635a02e3542dcd753d350662856b78a90805becda9f0f6df2b5499eb`  
		Last Modified: Wed, 25 Dec 2024 03:48:07 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10.5` - unknown; unknown

```console
$ docker pull chronograf@sha256:ccc99f48f31a9a61144299934ece16f81e3ead8caaf292e36e3c0d06edf456dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2722365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f34eac170ebb6e4736416f3d82546f9b45a22f5725f473e8ceac4b711e57017`

```dockerfile
```

-	Layers:
	-	`sha256:328f2d718a94e63d68a0992dd9b2063e42e664c8d2fb65f0cba9d7357f6d6578`  
		Last Modified: Wed, 25 Dec 2024 03:48:06 GMT  
		Size: 2.7 MB (2706158 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da1f387e2e6bf4b4a2bc73da901c5c3040bc3de0e55e0a86dbd36920bead94fd`  
		Last Modified: Wed, 25 Dec 2024 03:48:06 GMT  
		Size: 16.2 KB (16207 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.10.5` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:9636dae65e9631cf82030227df43ce5a21a7f0684ef566279545187d8bc6cabf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.5 MB (80513234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c459246fb31ffeff8ee987e4e19750f98ac33a42fcc74c2a8b145dfa2c48f67d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
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
	-	`sha256:f5c6876bb3d7d368455916fa98c705330bd8a8d9c080ccea8fe4c4b35a2ecb1f`  
		Last Modified: Tue, 24 Dec 2024 21:34:20 GMT  
		Size: 28.1 MB (28058723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:232f29504ec153209d0d6933a57ff49bae77c7a6234e88fcaf11cad8a7723bee`  
		Last Modified: Wed, 25 Dec 2024 01:52:46 GMT  
		Size: 7.5 MB (7459496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b2d2416f3e06d017c146f7a008f7e832c79d4d743507977252bfad16ccc0f51`  
		Last Modified: Wed, 25 Dec 2024 01:52:47 GMT  
		Size: 45.0 MB (44970555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9c2199ac63999a5d396dd76b0f697485319d69a8bfd129d09eecd6edb26fd79`  
		Last Modified: Wed, 25 Dec 2024 01:52:46 GMT  
		Size: 12.2 KB (12243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0245154bee61145c1748e294d72f49b69d7eb92fe78d4630b386771a731479bc`  
		Last Modified: Wed, 25 Dec 2024 01:52:46 GMT  
		Size: 11.9 KB (11902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:016d64276c8a4c1da71ef108932f169f0ee0fce7f101fccf20bd38daec3d4e07`  
		Last Modified: Wed, 25 Dec 2024 01:52:46 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10.5` - unknown; unknown

```console
$ docker pull chronograf@sha256:f28bf7b20289699eb40567193016ae5cdaba2b5d26aeb72ef42cce03fc7d22e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2720369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5202c10d949b0915ae82ce7488826f450a9e0f4a360275b8c35f2fa907184ccc`

```dockerfile
```

-	Layers:
	-	`sha256:b4af31a11ba8ca753ae64b866a74ffb5d0db1c18f70d5da361e6a4b0c5aa9cfd`  
		Last Modified: Wed, 25 Dec 2024 01:52:46 GMT  
		Size: 2.7 MB (2704134 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fbd98a0ed9b4d372cc9ea8ab71090909acd3f2734850cf0288363ec174da8b31`  
		Last Modified: Wed, 25 Dec 2024 01:52:45 GMT  
		Size: 16.2 KB (16235 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.10.5-alpine`

```console
$ docker pull chronograf@sha256:dde838ae1b743eb4d98d4b29b992fb7444b632ecbe2bf1b14e5bf78a96bcffa4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.10.5-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:ef35193e7e590e0a03c8550d74db0bec87be56cd5a15b1f020e966c6e6f78fb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31785614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c272e549048210a3ab50069f88ac438ed4a1707214e0b3289f84f0f491b34345`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD alpine-minirootfs-3.20.4-x86_64.tar.gz / # buildkit
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
	-	`sha256:63b69af3dc5582ce6b63be03623e334ccd4e5cb4bde42702bbfc7a986a1bf432`  
		Last Modified: Tue, 07 Jan 2025 02:28:35 GMT  
		Size: 3.6 MB (3613999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c46d8447fa31dea56913880abdd6f87f37a1a1f14aa39842807294d35b1db0d`  
		Last Modified: Tue, 07 Jan 2025 03:31:06 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fd617a6972020255d51696c8d3bfb0786fd896142684197413244eee22bc80a`  
		Last Modified: Tue, 07 Jan 2025 03:31:07 GMT  
		Size: 280.8 KB (280840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0487a8767300fb6ef70b3919b2fb90c086f446b646300015dcc0b044d9e5c8d`  
		Last Modified: Tue, 07 Jan 2025 03:31:08 GMT  
		Size: 27.9 MB (27866061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a04b3562cd1e0d44c469b817017c1201637c902bf3bd66a827b7a58eff33672`  
		Last Modified: Tue, 07 Jan 2025 03:31:07 GMT  
		Size: 12.2 KB (12241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01cb613e5324cd9d0a318d9f6ae96447ee7a0e708df412749fa68d9742015fe6`  
		Size: 11.9 KB (11901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a7bd88632473de5cac4c883ec9470a631e2fe300d21c49f850ae0649e48e02`  
		Last Modified: Tue, 07 Jan 2025 03:31:08 GMT  
		Size: 292.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10.5-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:c7c0fc8d91df4e8247bf270f41096b92d1e798292131a24a526aa32cefe376a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.6 KB (253572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ddbcc06bbcdf739077f575ab496a6239c9ad10d086d07c0861161d270644d2d`

```dockerfile
```

-	Layers:
	-	`sha256:bfd112895266bbd1c01511dd3dcdd6257f837bab85bcfc0b208e594614f00913`  
		Last Modified: Tue, 07 Jan 2025 03:31:07 GMT  
		Size: 235.7 KB (235717 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f078ec94cbf82ebe831b16a9d2b06edf070b1ab167af5e09aadd4cedad2d42f`  
		Last Modified: Tue, 07 Jan 2025 03:31:07 GMT  
		Size: 17.9 KB (17855 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.7`

```console
$ docker pull chronograf@sha256:835a163a111f025a504a7b19ae40d320d07f835fd4a9c32d4705d8f56f1294f9
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
$ docker pull chronograf@sha256:f4485c255b2991c4cdc1c2abd385db98d13d2a1ba55ce1d059224a66ee45f362
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.0 MB (69019873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86dc84c69587461ca8f21959216797cf055064a9a30dc90b526e4d54c0c26a15`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1734912000'
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
	-	`sha256:6c87eefc1f428634061bcdc9ec95ccceecd7c7475d35a777479af83f64ee6915`  
		Last Modified: Tue, 24 Dec 2024 21:32:32 GMT  
		Size: 30.3 MB (30252643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:632b6c0c593af0cd1fb186a7c28fbf1b292898bdba793c92e8006c7dbe2fba30`  
		Last Modified: Tue, 24 Dec 2024 22:25:42 GMT  
		Size: 4.2 MB (4209359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b13f01a5d82415e28b904f33e04dc4fff59a87286d9ff17670214ea68ffa83f9`  
		Last Modified: Tue, 24 Dec 2024 22:25:43 GMT  
		Size: 34.5 MB (34533482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b0867dbf12e8cc4ac720cc9793dbedec776e1bb6e6c3d1e8d71513a6b0e858`  
		Last Modified: Tue, 24 Dec 2024 22:25:42 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf5d67957dc87502f7b7605404763bf559373dc67e591eadaa8d9eda4934dd82`  
		Last Modified: Tue, 24 Dec 2024 22:25:42 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcdcd775fae1fb86bcade01fb28d8ddae33742fc08dab5bd6e2754e91f1e49a3`  
		Last Modified: Tue, 24 Dec 2024 22:25:42 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7` - unknown; unknown

```console
$ docker pull chronograf@sha256:a3a99c74d7f6604dc40bb101cd4ef6c3994d69e9fedeaf470855907a61e4a745
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2921165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4716a4d7bf5f81093181080ecfad28e1b5afdd0b281f2db85ec75f3fe3d38047`

```dockerfile
```

-	Layers:
	-	`sha256:49a0b52d3bc92c681bce979b9b3af54fedef791485647ff29d8fcf8e3c4b9ce3`  
		Last Modified: Tue, 24 Dec 2024 22:25:42 GMT  
		Size: 2.9 MB (2905389 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da3473275745403a47320b1b7ec6936268c456538508774a5831c543360318fb`  
		Last Modified: Tue, 24 Dec 2024 22:25:42 GMT  
		Size: 15.8 KB (15776 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.7` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:8973cbc90a0fa445378ca8d70558815329d6d2546678d2570eaa010062b5d025
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.0 MB (61962696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f0289a7329aedc72ade80323c0417dd47a3182d8fa09e4926ccf93a19851522`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1734912000'
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
	-	`sha256:0d436ac8a1fac914a00940d8604851d3414adc2ed370af15a8a5e6b319671b5b`  
		Last Modified: Tue, 24 Dec 2024 21:34:33 GMT  
		Size: 25.5 MB (25533937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:732c23e4d1841ba07e2f67ff4f09b6495d53955d93196232dcc7da6c27a7cf00`  
		Last Modified: Wed, 25 Dec 2024 03:46:16 GMT  
		Size: 3.5 MB (3511692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:120ff0975eded0a67db2b0e0ea018029ad2641b18642acb1179df296aec90b7d`  
		Last Modified: Wed, 25 Dec 2024 03:46:17 GMT  
		Size: 32.9 MB (32892674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ef709e1bf7930bd661ced6418d90f4733cd07f6165eb446708c5bd96f5d33d2`  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2db42a12ac0b5adf9e56967706110e85339720cac4455357af8a8cfa3e55efd`  
		Last Modified: Wed, 25 Dec 2024 03:46:16 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3580464a35a2c0e4223df1cc1ad2d25238a41848919a41313009e8bd11e35a3e`  
		Last Modified: Wed, 25 Dec 2024 03:46:17 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7` - unknown; unknown

```console
$ docker pull chronograf@sha256:238f08b0531c98f9cce66b57c12371d85ccee507473b6a5dced2e826fd98cec1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2923510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ffae8c3f1a034a4ec971847ba4c1a25e050967ff63adc93cfd7dc6ba2fb9255`

```dockerfile
```

-	Layers:
	-	`sha256:006e4151f1dcc4e6d070ac02a14d6fb4c8a23b3461c51f7c0ac17edfec943f6e`  
		Size: 2.9 MB (2907660 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa4b6a6ee876f1d8c4bbd90b6fd69dddae6842056302510b62dbf7691df7b291`  
		Last Modified: Wed, 25 Dec 2024 03:46:16 GMT  
		Size: 15.8 KB (15850 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.7` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:c4add2bf61da32c0d169c4e020bb49a180053f1ef7200f909000fafe6d8e3665
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.0 MB (66012958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d90da266ca064a719454043fc2767d344c87a8f846d4aaf02009531a07612bdd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1734912000'
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
	-	`sha256:879a6187682fc52c69294a2f450abdb54e257a50e8133ec6e89cb140345be6ce`  
		Last Modified: Tue, 24 Dec 2024 21:34:50 GMT  
		Size: 28.7 MB (28744853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd521a2bc39f9e75a6ea7e0423749fa0bb90408ff00bcd0fd01760f8c7a2b49`  
		Last Modified: Wed, 25 Dec 2024 01:51:18 GMT  
		Size: 4.2 MB (4210607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cef110f1544d38e0f9c8b691e45dc4d9fd8e1cb4d224d40425ce6f41e1e18304`  
		Last Modified: Wed, 25 Dec 2024 01:51:19 GMT  
		Size: 33.0 MB (33033100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e9fea5e495563f458ece1050c5bdb6402a550e36e245bd3d954108646c19e9a`  
		Last Modified: Wed, 25 Dec 2024 01:51:18 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:320c29ab92a04a7950f2f1a495ef146f04d28329bf419737cc00228f1247a672`  
		Last Modified: Wed, 25 Dec 2024 01:51:18 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87226c7efd6ea442607e8d9ecedc3598a734ef100682466a06bee6ef5c35a7c3`  
		Last Modified: Wed, 25 Dec 2024 01:51:19 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7` - unknown; unknown

```console
$ docker pull chronograf@sha256:398a0d75f3c0c6a6199a9ded024313097b5c4c12582ffe1f7a9221b4223a71dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2921510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6111a908aedccbe885436b30879b815b38be703195b4abc9a80d294911e6d1b7`

```dockerfile
```

-	Layers:
	-	`sha256:d63b43f3a7bf475c6db3ab0a7c381f2f970d1aca51269e46d308230702cd213b`  
		Last Modified: Wed, 25 Dec 2024 01:51:18 GMT  
		Size: 2.9 MB (2905638 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a10d28aa9860b4c2278ea7a0fc4067b990e60643f6d32831fe779332cbbd5014`  
		Last Modified: Wed, 25 Dec 2024 01:51:18 GMT  
		Size: 15.9 KB (15872 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.7-alpine`

```console
$ docker pull chronograf@sha256:2e679353e65e3047b762667bb92e77dc2b398c0d0939d836293bfbd7dd36c4c7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.7-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:5e8cf8facda66c3ce05798b6e957e99539f31005dd40772171530b1393805cdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.5 MB (23473983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b1363470a0fa3d3286193516805fcea1fb103647c9006ac51fc6c59f56df398`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD alpine-minirootfs-3.20.4-x86_64.tar.gz / # buildkit
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
	-	`sha256:63b69af3dc5582ce6b63be03623e334ccd4e5cb4bde42702bbfc7a986a1bf432`  
		Last Modified: Tue, 07 Jan 2025 02:28:35 GMT  
		Size: 3.6 MB (3613999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:387bb09c06c9f965134babeb333c6e4c87bd6948365748c30ab8620d975107ea`  
		Last Modified: Tue, 07 Jan 2025 03:30:56 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc8247c4823ca48d6aa14ffb4d28918fa7d6a99c64b80a0006abb4874d9cccec`  
		Last Modified: Tue, 07 Jan 2025 03:30:57 GMT  
		Size: 279.1 KB (279143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a26456c187e4fec9be2d4a22b1a8e0a4a698426013612aabf16d473201e51e3b`  
		Last Modified: Tue, 07 Jan 2025 03:30:57 GMT  
		Size: 19.6 MB (19556189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8a93263e99d65d12a652f56c96e7a0d94f31ffe852d3edaabe2fc07ab2343f9`  
		Last Modified: Tue, 07 Jan 2025 03:30:57 GMT  
		Size: 12.2 KB (12237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5555df4480890a9d250303fadb19f1303ef9fb6d18ea6a7af31871d2009f6fd`  
		Last Modified: Tue, 07 Jan 2025 03:30:57 GMT  
		Size: 11.9 KB (11896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e1a7418929be922c7a14eb64eac78e3bd228a2320ff11f8117bff2149b40ee5`  
		Last Modified: Tue, 07 Jan 2025 03:30:57 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:169f06622798b10f06b93cf0d878257eefcffcb32a300362f181c90265dfb4ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 KB (183379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8572ce8e7041fdf352106073cf5293cd6ffa22dd172dfbffbc461727ba4ef39e`

```dockerfile
```

-	Layers:
	-	`sha256:f08a12ae7e85d581ddacfb3afe1a73a17ccff95133e12c9bca08864ffb6faaed`  
		Last Modified: Tue, 07 Jan 2025 03:30:56 GMT  
		Size: 166.5 KB (166467 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:506d07f0c1bb3fec4e2cdc4ccff05e465fc697baebb781e082af904ac5b99552`  
		Last Modified: Tue, 07 Jan 2025 03:30:56 GMT  
		Size: 16.9 KB (16912 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.7.17`

```console
$ docker pull chronograf@sha256:835a163a111f025a504a7b19ae40d320d07f835fd4a9c32d4705d8f56f1294f9
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
$ docker pull chronograf@sha256:f4485c255b2991c4cdc1c2abd385db98d13d2a1ba55ce1d059224a66ee45f362
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.0 MB (69019873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86dc84c69587461ca8f21959216797cf055064a9a30dc90b526e4d54c0c26a15`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1734912000'
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
	-	`sha256:6c87eefc1f428634061bcdc9ec95ccceecd7c7475d35a777479af83f64ee6915`  
		Last Modified: Tue, 24 Dec 2024 21:32:32 GMT  
		Size: 30.3 MB (30252643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:632b6c0c593af0cd1fb186a7c28fbf1b292898bdba793c92e8006c7dbe2fba30`  
		Last Modified: Tue, 24 Dec 2024 22:25:42 GMT  
		Size: 4.2 MB (4209359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b13f01a5d82415e28b904f33e04dc4fff59a87286d9ff17670214ea68ffa83f9`  
		Last Modified: Tue, 24 Dec 2024 22:25:43 GMT  
		Size: 34.5 MB (34533482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b0867dbf12e8cc4ac720cc9793dbedec776e1bb6e6c3d1e8d71513a6b0e858`  
		Last Modified: Tue, 24 Dec 2024 22:25:42 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf5d67957dc87502f7b7605404763bf559373dc67e591eadaa8d9eda4934dd82`  
		Last Modified: Tue, 24 Dec 2024 22:25:42 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcdcd775fae1fb86bcade01fb28d8ddae33742fc08dab5bd6e2754e91f1e49a3`  
		Last Modified: Tue, 24 Dec 2024 22:25:42 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7.17` - unknown; unknown

```console
$ docker pull chronograf@sha256:a3a99c74d7f6604dc40bb101cd4ef6c3994d69e9fedeaf470855907a61e4a745
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2921165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4716a4d7bf5f81093181080ecfad28e1b5afdd0b281f2db85ec75f3fe3d38047`

```dockerfile
```

-	Layers:
	-	`sha256:49a0b52d3bc92c681bce979b9b3af54fedef791485647ff29d8fcf8e3c4b9ce3`  
		Last Modified: Tue, 24 Dec 2024 22:25:42 GMT  
		Size: 2.9 MB (2905389 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da3473275745403a47320b1b7ec6936268c456538508774a5831c543360318fb`  
		Last Modified: Tue, 24 Dec 2024 22:25:42 GMT  
		Size: 15.8 KB (15776 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.7.17` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:8973cbc90a0fa445378ca8d70558815329d6d2546678d2570eaa010062b5d025
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.0 MB (61962696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f0289a7329aedc72ade80323c0417dd47a3182d8fa09e4926ccf93a19851522`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1734912000'
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
	-	`sha256:0d436ac8a1fac914a00940d8604851d3414adc2ed370af15a8a5e6b319671b5b`  
		Last Modified: Tue, 24 Dec 2024 21:34:33 GMT  
		Size: 25.5 MB (25533937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:732c23e4d1841ba07e2f67ff4f09b6495d53955d93196232dcc7da6c27a7cf00`  
		Last Modified: Wed, 25 Dec 2024 03:46:16 GMT  
		Size: 3.5 MB (3511692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:120ff0975eded0a67db2b0e0ea018029ad2641b18642acb1179df296aec90b7d`  
		Last Modified: Wed, 25 Dec 2024 03:46:17 GMT  
		Size: 32.9 MB (32892674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ef709e1bf7930bd661ced6418d90f4733cd07f6165eb446708c5bd96f5d33d2`  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2db42a12ac0b5adf9e56967706110e85339720cac4455357af8a8cfa3e55efd`  
		Last Modified: Wed, 25 Dec 2024 03:46:16 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3580464a35a2c0e4223df1cc1ad2d25238a41848919a41313009e8bd11e35a3e`  
		Last Modified: Wed, 25 Dec 2024 03:46:17 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7.17` - unknown; unknown

```console
$ docker pull chronograf@sha256:238f08b0531c98f9cce66b57c12371d85ccee507473b6a5dced2e826fd98cec1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2923510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ffae8c3f1a034a4ec971847ba4c1a25e050967ff63adc93cfd7dc6ba2fb9255`

```dockerfile
```

-	Layers:
	-	`sha256:006e4151f1dcc4e6d070ac02a14d6fb4c8a23b3461c51f7c0ac17edfec943f6e`  
		Size: 2.9 MB (2907660 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa4b6a6ee876f1d8c4bbd90b6fd69dddae6842056302510b62dbf7691df7b291`  
		Last Modified: Wed, 25 Dec 2024 03:46:16 GMT  
		Size: 15.8 KB (15850 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.7.17` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:c4add2bf61da32c0d169c4e020bb49a180053f1ef7200f909000fafe6d8e3665
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.0 MB (66012958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d90da266ca064a719454043fc2767d344c87a8f846d4aaf02009531a07612bdd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1734912000'
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
	-	`sha256:879a6187682fc52c69294a2f450abdb54e257a50e8133ec6e89cb140345be6ce`  
		Last Modified: Tue, 24 Dec 2024 21:34:50 GMT  
		Size: 28.7 MB (28744853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd521a2bc39f9e75a6ea7e0423749fa0bb90408ff00bcd0fd01760f8c7a2b49`  
		Last Modified: Wed, 25 Dec 2024 01:51:18 GMT  
		Size: 4.2 MB (4210607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cef110f1544d38e0f9c8b691e45dc4d9fd8e1cb4d224d40425ce6f41e1e18304`  
		Last Modified: Wed, 25 Dec 2024 01:51:19 GMT  
		Size: 33.0 MB (33033100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e9fea5e495563f458ece1050c5bdb6402a550e36e245bd3d954108646c19e9a`  
		Last Modified: Wed, 25 Dec 2024 01:51:18 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:320c29ab92a04a7950f2f1a495ef146f04d28329bf419737cc00228f1247a672`  
		Last Modified: Wed, 25 Dec 2024 01:51:18 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87226c7efd6ea442607e8d9ecedc3598a734ef100682466a06bee6ef5c35a7c3`  
		Last Modified: Wed, 25 Dec 2024 01:51:19 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7.17` - unknown; unknown

```console
$ docker pull chronograf@sha256:398a0d75f3c0c6a6199a9ded024313097b5c4c12582ffe1f7a9221b4223a71dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2921510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6111a908aedccbe885436b30879b815b38be703195b4abc9a80d294911e6d1b7`

```dockerfile
```

-	Layers:
	-	`sha256:d63b43f3a7bf475c6db3ab0a7c381f2f970d1aca51269e46d308230702cd213b`  
		Last Modified: Wed, 25 Dec 2024 01:51:18 GMT  
		Size: 2.9 MB (2905638 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a10d28aa9860b4c2278ea7a0fc4067b990e60643f6d32831fe779332cbbd5014`  
		Last Modified: Wed, 25 Dec 2024 01:51:18 GMT  
		Size: 15.9 KB (15872 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.7.17-alpine`

```console
$ docker pull chronograf@sha256:2e679353e65e3047b762667bb92e77dc2b398c0d0939d836293bfbd7dd36c4c7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.7.17-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:5e8cf8facda66c3ce05798b6e957e99539f31005dd40772171530b1393805cdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.5 MB (23473983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b1363470a0fa3d3286193516805fcea1fb103647c9006ac51fc6c59f56df398`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD alpine-minirootfs-3.20.4-x86_64.tar.gz / # buildkit
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
	-	`sha256:63b69af3dc5582ce6b63be03623e334ccd4e5cb4bde42702bbfc7a986a1bf432`  
		Last Modified: Tue, 07 Jan 2025 02:28:35 GMT  
		Size: 3.6 MB (3613999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:387bb09c06c9f965134babeb333c6e4c87bd6948365748c30ab8620d975107ea`  
		Last Modified: Tue, 07 Jan 2025 03:30:56 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc8247c4823ca48d6aa14ffb4d28918fa7d6a99c64b80a0006abb4874d9cccec`  
		Last Modified: Tue, 07 Jan 2025 03:30:57 GMT  
		Size: 279.1 KB (279143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a26456c187e4fec9be2d4a22b1a8e0a4a698426013612aabf16d473201e51e3b`  
		Last Modified: Tue, 07 Jan 2025 03:30:57 GMT  
		Size: 19.6 MB (19556189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8a93263e99d65d12a652f56c96e7a0d94f31ffe852d3edaabe2fc07ab2343f9`  
		Last Modified: Tue, 07 Jan 2025 03:30:57 GMT  
		Size: 12.2 KB (12237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5555df4480890a9d250303fadb19f1303ef9fb6d18ea6a7af31871d2009f6fd`  
		Last Modified: Tue, 07 Jan 2025 03:30:57 GMT  
		Size: 11.9 KB (11896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e1a7418929be922c7a14eb64eac78e3bd228a2320ff11f8117bff2149b40ee5`  
		Last Modified: Tue, 07 Jan 2025 03:30:57 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7.17-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:169f06622798b10f06b93cf0d878257eefcffcb32a300362f181c90265dfb4ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 KB (183379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8572ce8e7041fdf352106073cf5293cd6ffa22dd172dfbffbc461727ba4ef39e`

```dockerfile
```

-	Layers:
	-	`sha256:f08a12ae7e85d581ddacfb3afe1a73a17ccff95133e12c9bca08864ffb6faaed`  
		Last Modified: Tue, 07 Jan 2025 03:30:56 GMT  
		Size: 166.5 KB (166467 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:506d07f0c1bb3fec4e2cdc4ccff05e465fc697baebb781e082af904ac5b99552`  
		Last Modified: Tue, 07 Jan 2025 03:30:56 GMT  
		Size: 16.9 KB (16912 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.8`

```console
$ docker pull chronograf@sha256:2958749fdf1979964c24dd88afcc6e6dad08ec61d1f41c470c3ec8822635e66b
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
$ docker pull chronograf@sha256:111c47f2b18bc6fe3b3b31ac9678ad84057298a636208f2186254fb57f8dab16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.7 MB (69661618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e95fde6ab988342d7af8c4f416be394ddb64854d93e14400fcc275d45c81e27`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1734912000'
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
	-	`sha256:6c87eefc1f428634061bcdc9ec95ccceecd7c7475d35a777479af83f64ee6915`  
		Last Modified: Tue, 24 Dec 2024 21:32:32 GMT  
		Size: 30.3 MB (30252643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89f8c5a66bbe16d8d32801377db46908d212b183a3d384f5ef319c4e1de09b5b`  
		Last Modified: Tue, 24 Dec 2024 22:25:42 GMT  
		Size: 5.0 MB (5020316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0c0ca2189c6b76d2e52a7884408ec468e92de29bf1c89850e4f3fd31c1cd1c5`  
		Last Modified: Tue, 24 Dec 2024 22:25:42 GMT  
		Size: 34.4 MB (34364282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a8fc1f7b5cc913b10a60270db32969ab74ac9e5037639a66b0f5c88219f7acc`  
		Last Modified: Tue, 24 Dec 2024 22:25:42 GMT  
		Size: 12.2 KB (12239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a727c48c9956764b78dcf8f00a79dd1a8f56f13bb30b52848c4b4a54717a84d4`  
		Last Modified: Tue, 24 Dec 2024 22:25:42 GMT  
		Size: 11.9 KB (11898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcdcd775fae1fb86bcade01fb28d8ddae33742fc08dab5bd6e2754e91f1e49a3`  
		Last Modified: Tue, 24 Dec 2024 22:25:42 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8` - unknown; unknown

```console
$ docker pull chronograf@sha256:a817e8482a0774630d7624fe62db287f68176322a7c57c6f4c7588e0f646ec43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2977894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac32c41be03bb65a79d2db0370a2d8f437338d50109e891fa53b0a332469d756`

```dockerfile
```

-	Layers:
	-	`sha256:81eb5bf3faf27fcec655455112a13cce0a1604d73977ebdae4b53bb17a8c0146`  
		Last Modified: Tue, 24 Dec 2024 22:25:42 GMT  
		Size: 3.0 MB (2962077 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c2fdb41c0761faf801de697c36f7c5634a7bb41b86d4ed491366f1eb26998a5`  
		Last Modified: Tue, 24 Dec 2024 22:25:42 GMT  
		Size: 15.8 KB (15817 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.8` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:dfb4ff9ceda4445597093dfee0b9b41c2cff16f8d731bfeb0962baeedc114c4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62378300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c744f04c58344bbb1f8b3de6b9b5c90f7a0fefebb0d83ba8d2dc09226be2e873`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1734912000'
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
	-	`sha256:0d436ac8a1fac914a00940d8604851d3414adc2ed370af15a8a5e6b319671b5b`  
		Last Modified: Tue, 24 Dec 2024 21:34:33 GMT  
		Size: 25.5 MB (25533937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c5aea0517ff11e65f4f79db7ff0a1993688e3a1615a5cdd3e6d7b2963c326c`  
		Last Modified: Wed, 25 Dec 2024 03:46:53 GMT  
		Size: 4.3 MB (4285127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5535b34e37cf4c2bd9f473a370a6464c1b9dc64e41f5578a23d56b48f3c001fc`  
		Last Modified: Wed, 25 Dec 2024 03:46:54 GMT  
		Size: 32.5 MB (32534842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7b694f83b3c2cbc20caf04697b521900ef49464144c36a3085866292dedb1dc`  
		Last Modified: Wed, 25 Dec 2024 03:46:53 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa5e526fa1d4a4154eed7197659c5695eae0e5ac95d6602aa0e274c3bc3eaddc`  
		Last Modified: Wed, 25 Dec 2024 03:46:53 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a31d1cbaec8ae49482633a2d83c9495246724d1a8e0a4f3c3873b87a1710aa8`  
		Last Modified: Wed, 25 Dec 2024 03:46:54 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8` - unknown; unknown

```console
$ docker pull chronograf@sha256:cdb2ffb291f5c1ee780e3c88a882fa66f322528bd37205b9314c35961f0ebaad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2980238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92d6cecfddcaae7a9c9926bf29359d593ea0ee796e9d134381f7d5ae7fe5e8f0`

```dockerfile
```

-	Layers:
	-	`sha256:eb0ef123091ddf4067926aa66fda1813c8c856382fa5e239989f5f97fc7d85f3`  
		Last Modified: Wed, 25 Dec 2024 03:46:53 GMT  
		Size: 3.0 MB (2964348 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17fa179eda58ddc570ac9cbba467d1c3dd288594b3785bee1127285ccf3a465a`  
		Last Modified: Wed, 25 Dec 2024 03:46:53 GMT  
		Size: 15.9 KB (15890 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.8` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:7af91e2663289c9f05cc64717260bebdcd0964900f4bdee8163601e3d2e80ea4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66202354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1dd666424cab68e20ba165a3bc2b02387b797564af1887d7d340d76e33a049f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1734912000'
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
	-	`sha256:879a6187682fc52c69294a2f450abdb54e257a50e8133ec6e89cb140345be6ce`  
		Last Modified: Tue, 24 Dec 2024 21:34:50 GMT  
		Size: 28.7 MB (28744853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be2b72c46a4097f386a148f9e3c2d9bc8366dcf98677d42addcf30df8433028a`  
		Last Modified: Wed, 25 Dec 2024 01:51:46 GMT  
		Size: 5.0 MB (5003577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebbb562ca7b005f52b2e7ed2ceb36bf5a215639f7ebe2979add65868089af0c1`  
		Last Modified: Wed, 25 Dec 2024 01:51:47 GMT  
		Size: 32.4 MB (32429533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec0d7a739e6a417cd3c421271ff3498c3bebd4f473511182eaf9d7e06fd208dc`  
		Last Modified: Wed, 25 Dec 2024 01:51:46 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd654193d820ecd638c5c2a98af96c5bc3300c39bb6b8e1f36027df35e581da5`  
		Last Modified: Wed, 25 Dec 2024 01:51:46 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:148d342beb5fc4e456fc4a1aa9844e51e5cfb19d0a8ce774b853aab9a53c2451`  
		Last Modified: Wed, 25 Dec 2024 01:51:47 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8` - unknown; unknown

```console
$ docker pull chronograf@sha256:51a4e21835090950476d7a7b5256e32348955ca8ed44ef49ef2baa6ff8589135
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2978237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90c6b83ba2386754805aac9d8aaf64b6fce32422bab783a30a98315da6ebd34b`

```dockerfile
```

-	Layers:
	-	`sha256:ac417df418a8c41b014c30954c11bdcb3a28ce4e7a70f0e13d510c3ad85f555c`  
		Last Modified: Wed, 25 Dec 2024 01:51:46 GMT  
		Size: 3.0 MB (2962326 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:362c0406a038fde00e69cf51f51b75560360bd714922cafb5b535830999358ed`  
		Last Modified: Wed, 25 Dec 2024 01:51:46 GMT  
		Size: 15.9 KB (15911 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.8-alpine`

```console
$ docker pull chronograf@sha256:cd69b804e02f8bdb596b0413a6a69ac66eb01f6ecb6bb1c8baac1fc9bbe849e2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.8-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:c305a6139eb6395790031b2b8d0a438303bdd8f26ffedae25276183e49abc30d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23121683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f288500319fe8e9ec3b7542415419ed087700bb0373e2712a88d20db093d590`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD alpine-minirootfs-3.20.4-x86_64.tar.gz / # buildkit
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
	-	`sha256:63b69af3dc5582ce6b63be03623e334ccd4e5cb4bde42702bbfc7a986a1bf432`  
		Last Modified: Tue, 07 Jan 2025 02:28:35 GMT  
		Size: 3.6 MB (3613999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bfbff95abbb53da6e174b003718b9702584d06532ba4018686ff2f03f3b4dfd`  
		Last Modified: Tue, 07 Jan 2025 03:30:54 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2f9252db0b8fa0810b74416ae0b63531f01ec99bdf29191a821c7d71485b28d`  
		Last Modified: Tue, 07 Jan 2025 03:30:55 GMT  
		Size: 279.1 KB (279133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d29a9bc7edce36d720ea0855f77acf5429b947a0d538423bbe65332de9f745a5`  
		Last Modified: Tue, 07 Jan 2025 03:30:56 GMT  
		Size: 19.2 MB (19203900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:045eca8e141b2bdd0eb2b8f910d982b6a53b427db4e3c02f1959a8141bc6de6e`  
		Last Modified: Tue, 07 Jan 2025 03:30:55 GMT  
		Size: 12.2 KB (12237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77bc9d4d66f42fb97b01c70f1cf4492b9b7b8dd3925fd94d7cb90a1a0e2dcfdf`  
		Last Modified: Tue, 07 Jan 2025 03:30:56 GMT  
		Size: 11.9 KB (11896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f6d4bdced72a5e0156ad0b46236ea3f3882be890a6d5e78d3983930e549fa71`  
		Last Modified: Tue, 07 Jan 2025 03:30:55 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:23ffc733fa58247fda90d366a00cc8d49c09868fef5f073a9c76b2670ef4cb42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.9 KB (240938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65c82cdee2dcd23b72a15b73704a45d795e8d6b5c331cc3b30f27a0df0f3dd8e`

```dockerfile
```

-	Layers:
	-	`sha256:99908a9ed9f04e8c27c9ca9e427b407ffdc414ff98dbb8b2c9ec484aaa80e3b5`  
		Last Modified: Tue, 07 Jan 2025 03:30:55 GMT  
		Size: 224.0 KB (224026 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d66c7ff640426a4b49e4bf70bddc0b944a67676274265b6dbe6caad83fad8592`  
		Size: 16.9 KB (16912 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.8.10`

```console
$ docker pull chronograf@sha256:2958749fdf1979964c24dd88afcc6e6dad08ec61d1f41c470c3ec8822635e66b
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
$ docker pull chronograf@sha256:111c47f2b18bc6fe3b3b31ac9678ad84057298a636208f2186254fb57f8dab16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.7 MB (69661618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e95fde6ab988342d7af8c4f416be394ddb64854d93e14400fcc275d45c81e27`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1734912000'
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
	-	`sha256:6c87eefc1f428634061bcdc9ec95ccceecd7c7475d35a777479af83f64ee6915`  
		Last Modified: Tue, 24 Dec 2024 21:32:32 GMT  
		Size: 30.3 MB (30252643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89f8c5a66bbe16d8d32801377db46908d212b183a3d384f5ef319c4e1de09b5b`  
		Last Modified: Tue, 24 Dec 2024 22:25:42 GMT  
		Size: 5.0 MB (5020316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0c0ca2189c6b76d2e52a7884408ec468e92de29bf1c89850e4f3fd31c1cd1c5`  
		Last Modified: Tue, 24 Dec 2024 22:25:42 GMT  
		Size: 34.4 MB (34364282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a8fc1f7b5cc913b10a60270db32969ab74ac9e5037639a66b0f5c88219f7acc`  
		Last Modified: Tue, 24 Dec 2024 22:25:42 GMT  
		Size: 12.2 KB (12239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a727c48c9956764b78dcf8f00a79dd1a8f56f13bb30b52848c4b4a54717a84d4`  
		Last Modified: Tue, 24 Dec 2024 22:25:42 GMT  
		Size: 11.9 KB (11898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcdcd775fae1fb86bcade01fb28d8ddae33742fc08dab5bd6e2754e91f1e49a3`  
		Last Modified: Tue, 24 Dec 2024 22:25:42 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:a817e8482a0774630d7624fe62db287f68176322a7c57c6f4c7588e0f646ec43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2977894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac32c41be03bb65a79d2db0370a2d8f437338d50109e891fa53b0a332469d756`

```dockerfile
```

-	Layers:
	-	`sha256:81eb5bf3faf27fcec655455112a13cce0a1604d73977ebdae4b53bb17a8c0146`  
		Last Modified: Tue, 24 Dec 2024 22:25:42 GMT  
		Size: 3.0 MB (2962077 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c2fdb41c0761faf801de697c36f7c5634a7bb41b86d4ed491366f1eb26998a5`  
		Last Modified: Tue, 24 Dec 2024 22:25:42 GMT  
		Size: 15.8 KB (15817 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.8.10` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:dfb4ff9ceda4445597093dfee0b9b41c2cff16f8d731bfeb0962baeedc114c4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62378300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c744f04c58344bbb1f8b3de6b9b5c90f7a0fefebb0d83ba8d2dc09226be2e873`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1734912000'
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
	-	`sha256:0d436ac8a1fac914a00940d8604851d3414adc2ed370af15a8a5e6b319671b5b`  
		Last Modified: Tue, 24 Dec 2024 21:34:33 GMT  
		Size: 25.5 MB (25533937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c5aea0517ff11e65f4f79db7ff0a1993688e3a1615a5cdd3e6d7b2963c326c`  
		Last Modified: Wed, 25 Dec 2024 03:46:53 GMT  
		Size: 4.3 MB (4285127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5535b34e37cf4c2bd9f473a370a6464c1b9dc64e41f5578a23d56b48f3c001fc`  
		Last Modified: Wed, 25 Dec 2024 03:46:54 GMT  
		Size: 32.5 MB (32534842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7b694f83b3c2cbc20caf04697b521900ef49464144c36a3085866292dedb1dc`  
		Last Modified: Wed, 25 Dec 2024 03:46:53 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa5e526fa1d4a4154eed7197659c5695eae0e5ac95d6602aa0e274c3bc3eaddc`  
		Last Modified: Wed, 25 Dec 2024 03:46:53 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a31d1cbaec8ae49482633a2d83c9495246724d1a8e0a4f3c3873b87a1710aa8`  
		Last Modified: Wed, 25 Dec 2024 03:46:54 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:cdb2ffb291f5c1ee780e3c88a882fa66f322528bd37205b9314c35961f0ebaad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2980238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92d6cecfddcaae7a9c9926bf29359d593ea0ee796e9d134381f7d5ae7fe5e8f0`

```dockerfile
```

-	Layers:
	-	`sha256:eb0ef123091ddf4067926aa66fda1813c8c856382fa5e239989f5f97fc7d85f3`  
		Last Modified: Wed, 25 Dec 2024 03:46:53 GMT  
		Size: 3.0 MB (2964348 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17fa179eda58ddc570ac9cbba467d1c3dd288594b3785bee1127285ccf3a465a`  
		Last Modified: Wed, 25 Dec 2024 03:46:53 GMT  
		Size: 15.9 KB (15890 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.8.10` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:7af91e2663289c9f05cc64717260bebdcd0964900f4bdee8163601e3d2e80ea4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66202354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1dd666424cab68e20ba165a3bc2b02387b797564af1887d7d340d76e33a049f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1734912000'
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
	-	`sha256:879a6187682fc52c69294a2f450abdb54e257a50e8133ec6e89cb140345be6ce`  
		Last Modified: Tue, 24 Dec 2024 21:34:50 GMT  
		Size: 28.7 MB (28744853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be2b72c46a4097f386a148f9e3c2d9bc8366dcf98677d42addcf30df8433028a`  
		Last Modified: Wed, 25 Dec 2024 01:51:46 GMT  
		Size: 5.0 MB (5003577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebbb562ca7b005f52b2e7ed2ceb36bf5a215639f7ebe2979add65868089af0c1`  
		Last Modified: Wed, 25 Dec 2024 01:51:47 GMT  
		Size: 32.4 MB (32429533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec0d7a739e6a417cd3c421271ff3498c3bebd4f473511182eaf9d7e06fd208dc`  
		Last Modified: Wed, 25 Dec 2024 01:51:46 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd654193d820ecd638c5c2a98af96c5bc3300c39bb6b8e1f36027df35e581da5`  
		Last Modified: Wed, 25 Dec 2024 01:51:46 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:148d342beb5fc4e456fc4a1aa9844e51e5cfb19d0a8ce774b853aab9a53c2451`  
		Last Modified: Wed, 25 Dec 2024 01:51:47 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:51a4e21835090950476d7a7b5256e32348955ca8ed44ef49ef2baa6ff8589135
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2978237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90c6b83ba2386754805aac9d8aaf64b6fce32422bab783a30a98315da6ebd34b`

```dockerfile
```

-	Layers:
	-	`sha256:ac417df418a8c41b014c30954c11bdcb3a28ce4e7a70f0e13d510c3ad85f555c`  
		Last Modified: Wed, 25 Dec 2024 01:51:46 GMT  
		Size: 3.0 MB (2962326 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:362c0406a038fde00e69cf51f51b75560360bd714922cafb5b535830999358ed`  
		Last Modified: Wed, 25 Dec 2024 01:51:46 GMT  
		Size: 15.9 KB (15911 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.8.10-alpine`

```console
$ docker pull chronograf@sha256:cd69b804e02f8bdb596b0413a6a69ac66eb01f6ecb6bb1c8baac1fc9bbe849e2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.8.10-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:c305a6139eb6395790031b2b8d0a438303bdd8f26ffedae25276183e49abc30d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23121683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f288500319fe8e9ec3b7542415419ed087700bb0373e2712a88d20db093d590`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD alpine-minirootfs-3.20.4-x86_64.tar.gz / # buildkit
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
	-	`sha256:63b69af3dc5582ce6b63be03623e334ccd4e5cb4bde42702bbfc7a986a1bf432`  
		Last Modified: Tue, 07 Jan 2025 02:28:35 GMT  
		Size: 3.6 MB (3613999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bfbff95abbb53da6e174b003718b9702584d06532ba4018686ff2f03f3b4dfd`  
		Last Modified: Tue, 07 Jan 2025 03:30:54 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2f9252db0b8fa0810b74416ae0b63531f01ec99bdf29191a821c7d71485b28d`  
		Last Modified: Tue, 07 Jan 2025 03:30:55 GMT  
		Size: 279.1 KB (279133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d29a9bc7edce36d720ea0855f77acf5429b947a0d538423bbe65332de9f745a5`  
		Last Modified: Tue, 07 Jan 2025 03:30:56 GMT  
		Size: 19.2 MB (19203900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:045eca8e141b2bdd0eb2b8f910d982b6a53b427db4e3c02f1959a8141bc6de6e`  
		Last Modified: Tue, 07 Jan 2025 03:30:55 GMT  
		Size: 12.2 KB (12237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77bc9d4d66f42fb97b01c70f1cf4492b9b7b8dd3925fd94d7cb90a1a0e2dcfdf`  
		Last Modified: Tue, 07 Jan 2025 03:30:56 GMT  
		Size: 11.9 KB (11896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f6d4bdced72a5e0156ad0b46236ea3f3882be890a6d5e78d3983930e549fa71`  
		Last Modified: Tue, 07 Jan 2025 03:30:55 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8.10-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:23ffc733fa58247fda90d366a00cc8d49c09868fef5f073a9c76b2670ef4cb42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.9 KB (240938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65c82cdee2dcd23b72a15b73704a45d795e8d6b5c331cc3b30f27a0df0f3dd8e`

```dockerfile
```

-	Layers:
	-	`sha256:99908a9ed9f04e8c27c9ca9e427b407ffdc414ff98dbb8b2c9ec484aaa80e3b5`  
		Last Modified: Tue, 07 Jan 2025 03:30:55 GMT  
		Size: 224.0 KB (224026 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d66c7ff640426a4b49e4bf70bddc0b944a67676274265b6dbe6caad83fad8592`  
		Size: 16.9 KB (16912 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.9`

```console
$ docker pull chronograf@sha256:29f888e5e99d9c672a7864383741d42372cb06db0a0f10c8a53a70127829eebe
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
$ docker pull chronograf@sha256:4d854805a9aebd9fb259951dd4e2ab142eedc6e5c52aa804af53106b5826d03a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.3 MB (70309168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb9b14880b799ffec73a815e70def17b0e60716b8c5865ead5e77e19aad0048e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1734912000'
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
	-	`sha256:6c87eefc1f428634061bcdc9ec95ccceecd7c7475d35a777479af83f64ee6915`  
		Last Modified: Tue, 24 Dec 2024 21:32:32 GMT  
		Size: 30.3 MB (30252643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93c917fbf0b5e6b7b00e8506b08cdc5db0455b7a9fb286072e71934b28aef708`  
		Last Modified: Tue, 24 Dec 2024 22:26:11 GMT  
		Size: 5.0 MB (5020342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9418529954f6bc4549e9eaf27be7d5a3a19ff9f7511c5b13d751483ce226b241`  
		Size: 35.0 MB (35011790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d66cb115d5217ad16ead81e2dc6eb90f49924a32c69f40992c4050138a7ebf3b`  
		Last Modified: Tue, 24 Dec 2024 22:26:11 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5c615f987b753ef7315d6e3b48114c01dd6fe076c58a7000be3a27fcd2553fa`  
		Last Modified: Tue, 24 Dec 2024 22:26:11 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c4f1f85a1dee947ce37ba5e46302a70bb1b7d2033405804234c6208574d51d8`  
		Last Modified: Tue, 24 Dec 2024 22:26:12 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9` - unknown; unknown

```console
$ docker pull chronograf@sha256:da08d045c8c7b64561b6d9ec8186eeac9f4b056de637389e2e958da3a43bba74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2983097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1332b7e60e445dbbfbbd6f8c4434ca8155377c66271447d8336d44aab3d019d`

```dockerfile
```

-	Layers:
	-	`sha256:7bfec5fe8d460cfd9964f4e9611fa3690a2918aa8340583162a300792513c64e`  
		Last Modified: Tue, 24 Dec 2024 22:26:11 GMT  
		Size: 3.0 MB (2967287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c84780b0d2ca24cfadc6d577807314bf29d3e06fa074b48f5ac98d1ecb2a09ae`  
		Size: 15.8 KB (15810 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.9` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:d35183cfe36adcc131bcd947ed9f0fe5d3f19d54be29bf75689ba428f320a931
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.2 MB (63154941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91db14f135b1061778dc0da431bf981a9a4ba0459fd8a793801e67ce8e221afa`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1734912000'
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
	-	`sha256:0d436ac8a1fac914a00940d8604851d3414adc2ed370af15a8a5e6b319671b5b`  
		Last Modified: Tue, 24 Dec 2024 21:34:33 GMT  
		Size: 25.5 MB (25533937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c5aea0517ff11e65f4f79db7ff0a1993688e3a1615a5cdd3e6d7b2963c326c`  
		Last Modified: Wed, 25 Dec 2024 03:46:53 GMT  
		Size: 4.3 MB (4285127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f9a8ec131bd92e17068cc9a29c589f0108327206f9824fd1bbe9293ef6b93bc`  
		Last Modified: Wed, 25 Dec 2024 03:47:24 GMT  
		Size: 33.3 MB (33311488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b21866b007fddf02307e6844c2950d068e5ffef24291e925fa8eff1d65f0551`  
		Last Modified: Wed, 25 Dec 2024 03:47:23 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5efabfbc75f8766cb5f81cf8b80b122a60c323d06b929c873787b623630538b9`  
		Last Modified: Wed, 25 Dec 2024 03:47:23 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fff84b7ead15784b365ea2701b57479a767fbd67d8cbd40fa63a840690b353e`  
		Last Modified: Wed, 25 Dec 2024 03:47:23 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9` - unknown; unknown

```console
$ docker pull chronograf@sha256:1f4bf1b4361ccdf00d36c58fc9da54bbd1bf962dd388e52f07d45b7d5d59e750
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2985441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2f2ef8943d15f8183f6a701ebcaa02c52894a6376624d5c38f1b46d2b7f57ba`

```dockerfile
```

-	Layers:
	-	`sha256:e88a1ee0f921fad87e3678abde23f3ed50a457bca005ffffadcc59b8979934ea`  
		Last Modified: Wed, 25 Dec 2024 03:47:23 GMT  
		Size: 3.0 MB (2969558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:735a16c5042966b08ba2229dc43ff427dabe2a2cb332b8618422304d69b22fad`  
		Last Modified: Wed, 25 Dec 2024 03:47:23 GMT  
		Size: 15.9 KB (15883 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.9` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:54757144c6add57997f4810bf337989aef78b078d4821da9f3e53826815c9d07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.0 MB (66954447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f81cdac0c854f99895102c5c2e02febbd3abb48ff20a4b33b078805578047629`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1734912000'
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
	-	`sha256:879a6187682fc52c69294a2f450abdb54e257a50e8133ec6e89cb140345be6ce`  
		Last Modified: Tue, 24 Dec 2024 21:34:50 GMT  
		Size: 28.7 MB (28744853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be2b72c46a4097f386a148f9e3c2d9bc8366dcf98677d42addcf30df8433028a`  
		Last Modified: Wed, 25 Dec 2024 01:51:46 GMT  
		Size: 5.0 MB (5003577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80be9671cb9e929f9912e3751f1b9ad7c16ff3b6922d32982cd9e4bf46405482`  
		Last Modified: Wed, 25 Dec 2024 01:52:16 GMT  
		Size: 33.2 MB (33181630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cbe51ee6c59886fbfe06ee3bcf5a1f09b7ecc7d529b60e6ef1c431b4b130698`  
		Last Modified: Wed, 25 Dec 2024 01:52:15 GMT  
		Size: 12.2 KB (12244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:176640989e428d64137819f8fe2a8bfe2403256d00c31eadae42e55a1cab9a91`  
		Last Modified: Wed, 25 Dec 2024 01:52:15 GMT  
		Size: 11.9 KB (11903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95c917c7c1a2989a8e11a1aad523f0b96d75439b7d71b7c7554467cee49c6b87`  
		Last Modified: Wed, 25 Dec 2024 01:52:15 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9` - unknown; unknown

```console
$ docker pull chronograf@sha256:5741357b33ba8149db41ba4c2a3946bf56ed7898248b6cd03a167f8c31a51add
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2983441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:392ea0ece110bed1f5e54e027b44a3e91731773e5349bdf8631f27d8dc934a6e`

```dockerfile
```

-	Layers:
	-	`sha256:58d0927019a624f522e2d53b5e3add76e40ac0914b629d39da3e3f2f67a84bc2`  
		Last Modified: Wed, 25 Dec 2024 01:52:15 GMT  
		Size: 3.0 MB (2967536 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f740566634c83eeb29449799c1b2c3e34e390525099b18cbab78783adbef656`  
		Last Modified: Wed, 25 Dec 2024 01:52:15 GMT  
		Size: 15.9 KB (15905 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.9-alpine`

```console
$ docker pull chronograf@sha256:f929772f78639a674ebbc2e53e8a4ced0538836305b0e06466b4ba5e357e201c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.9-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:d88cfa90947735219bdb8d2f4b95507933de8b79d693e195271984103063c95a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23589801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ed5f81e66408f10c7f74167483c578d2885d23b86485222ae5002ad0d5ddae8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD alpine-minirootfs-3.20.4-x86_64.tar.gz / # buildkit
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
	-	`sha256:63b69af3dc5582ce6b63be03623e334ccd4e5cb4bde42702bbfc7a986a1bf432`  
		Last Modified: Tue, 07 Jan 2025 02:28:35 GMT  
		Size: 3.6 MB (3613999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bfbff95abbb53da6e174b003718b9702584d06532ba4018686ff2f03f3b4dfd`  
		Last Modified: Tue, 07 Jan 2025 03:30:54 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:835d456474e07ef91a0c109823461f5a1a05e2d84efd3d981f084fbe63627986`  
		Last Modified: Tue, 07 Jan 2025 03:30:54 GMT  
		Size: 279.1 KB (279134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fbf6fde88328234fcd4e691130955d09bfe23096d63780b58140acc48ddfae5`  
		Last Modified: Tue, 07 Jan 2025 03:30:55 GMT  
		Size: 19.7 MB (19672018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80edb5438907d16c4b509396aecc873ec01300a1bdfadcab97fcb994b1b2d3c9`  
		Last Modified: Tue, 07 Jan 2025 03:30:54 GMT  
		Size: 12.2 KB (12236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b88661ef4c63e9d4725d7519a7890d6776f1d8c0baf6ed47fc50829428ede7d0`  
		Last Modified: Tue, 07 Jan 2025 03:30:55 GMT  
		Size: 11.9 KB (11896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f6d4bdced72a5e0156ad0b46236ea3f3882be890a6d5e78d3983930e549fa71`  
		Last Modified: Tue, 07 Jan 2025 03:30:55 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:67a6fc65a166055453a55fce4d944ed707e0147e964845e26459f46a7d1bfe03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.1 KB (246147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71a202451865885bcc8e3752c0b7a6a57be9ee98f872c66d117596c46e757db9`

```dockerfile
```

-	Layers:
	-	`sha256:be2322b4591902abe89c5084d777103dc55b26b7376edf330e17fa7acefbe9a6`  
		Last Modified: Tue, 07 Jan 2025 03:30:54 GMT  
		Size: 229.2 KB (229238 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ece7b302d5ade3bd7ddfa27720432db093ab401ddde671e3907cfd8b4bcc843`  
		Last Modified: Tue, 07 Jan 2025 03:30:54 GMT  
		Size: 16.9 KB (16909 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.9.4`

```console
$ docker pull chronograf@sha256:29f888e5e99d9c672a7864383741d42372cb06db0a0f10c8a53a70127829eebe
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
$ docker pull chronograf@sha256:4d854805a9aebd9fb259951dd4e2ab142eedc6e5c52aa804af53106b5826d03a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.3 MB (70309168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb9b14880b799ffec73a815e70def17b0e60716b8c5865ead5e77e19aad0048e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1734912000'
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
	-	`sha256:6c87eefc1f428634061bcdc9ec95ccceecd7c7475d35a777479af83f64ee6915`  
		Last Modified: Tue, 24 Dec 2024 21:32:32 GMT  
		Size: 30.3 MB (30252643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93c917fbf0b5e6b7b00e8506b08cdc5db0455b7a9fb286072e71934b28aef708`  
		Last Modified: Tue, 24 Dec 2024 22:26:11 GMT  
		Size: 5.0 MB (5020342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9418529954f6bc4549e9eaf27be7d5a3a19ff9f7511c5b13d751483ce226b241`  
		Size: 35.0 MB (35011790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d66cb115d5217ad16ead81e2dc6eb90f49924a32c69f40992c4050138a7ebf3b`  
		Last Modified: Tue, 24 Dec 2024 22:26:11 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5c615f987b753ef7315d6e3b48114c01dd6fe076c58a7000be3a27fcd2553fa`  
		Last Modified: Tue, 24 Dec 2024 22:26:11 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c4f1f85a1dee947ce37ba5e46302a70bb1b7d2033405804234c6208574d51d8`  
		Last Modified: Tue, 24 Dec 2024 22:26:12 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9.4` - unknown; unknown

```console
$ docker pull chronograf@sha256:da08d045c8c7b64561b6d9ec8186eeac9f4b056de637389e2e958da3a43bba74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2983097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1332b7e60e445dbbfbbd6f8c4434ca8155377c66271447d8336d44aab3d019d`

```dockerfile
```

-	Layers:
	-	`sha256:7bfec5fe8d460cfd9964f4e9611fa3690a2918aa8340583162a300792513c64e`  
		Last Modified: Tue, 24 Dec 2024 22:26:11 GMT  
		Size: 3.0 MB (2967287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c84780b0d2ca24cfadc6d577807314bf29d3e06fa074b48f5ac98d1ecb2a09ae`  
		Size: 15.8 KB (15810 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.9.4` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:d35183cfe36adcc131bcd947ed9f0fe5d3f19d54be29bf75689ba428f320a931
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.2 MB (63154941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91db14f135b1061778dc0da431bf981a9a4ba0459fd8a793801e67ce8e221afa`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1734912000'
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
	-	`sha256:0d436ac8a1fac914a00940d8604851d3414adc2ed370af15a8a5e6b319671b5b`  
		Last Modified: Tue, 24 Dec 2024 21:34:33 GMT  
		Size: 25.5 MB (25533937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c5aea0517ff11e65f4f79db7ff0a1993688e3a1615a5cdd3e6d7b2963c326c`  
		Last Modified: Wed, 25 Dec 2024 03:46:53 GMT  
		Size: 4.3 MB (4285127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f9a8ec131bd92e17068cc9a29c589f0108327206f9824fd1bbe9293ef6b93bc`  
		Last Modified: Wed, 25 Dec 2024 03:47:24 GMT  
		Size: 33.3 MB (33311488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b21866b007fddf02307e6844c2950d068e5ffef24291e925fa8eff1d65f0551`  
		Last Modified: Wed, 25 Dec 2024 03:47:23 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5efabfbc75f8766cb5f81cf8b80b122a60c323d06b929c873787b623630538b9`  
		Last Modified: Wed, 25 Dec 2024 03:47:23 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fff84b7ead15784b365ea2701b57479a767fbd67d8cbd40fa63a840690b353e`  
		Last Modified: Wed, 25 Dec 2024 03:47:23 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9.4` - unknown; unknown

```console
$ docker pull chronograf@sha256:1f4bf1b4361ccdf00d36c58fc9da54bbd1bf962dd388e52f07d45b7d5d59e750
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2985441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2f2ef8943d15f8183f6a701ebcaa02c52894a6376624d5c38f1b46d2b7f57ba`

```dockerfile
```

-	Layers:
	-	`sha256:e88a1ee0f921fad87e3678abde23f3ed50a457bca005ffffadcc59b8979934ea`  
		Last Modified: Wed, 25 Dec 2024 03:47:23 GMT  
		Size: 3.0 MB (2969558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:735a16c5042966b08ba2229dc43ff427dabe2a2cb332b8618422304d69b22fad`  
		Last Modified: Wed, 25 Dec 2024 03:47:23 GMT  
		Size: 15.9 KB (15883 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.9.4` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:54757144c6add57997f4810bf337989aef78b078d4821da9f3e53826815c9d07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.0 MB (66954447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f81cdac0c854f99895102c5c2e02febbd3abb48ff20a4b33b078805578047629`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1734912000'
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
	-	`sha256:879a6187682fc52c69294a2f450abdb54e257a50e8133ec6e89cb140345be6ce`  
		Last Modified: Tue, 24 Dec 2024 21:34:50 GMT  
		Size: 28.7 MB (28744853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be2b72c46a4097f386a148f9e3c2d9bc8366dcf98677d42addcf30df8433028a`  
		Last Modified: Wed, 25 Dec 2024 01:51:46 GMT  
		Size: 5.0 MB (5003577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80be9671cb9e929f9912e3751f1b9ad7c16ff3b6922d32982cd9e4bf46405482`  
		Last Modified: Wed, 25 Dec 2024 01:52:16 GMT  
		Size: 33.2 MB (33181630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cbe51ee6c59886fbfe06ee3bcf5a1f09b7ecc7d529b60e6ef1c431b4b130698`  
		Last Modified: Wed, 25 Dec 2024 01:52:15 GMT  
		Size: 12.2 KB (12244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:176640989e428d64137819f8fe2a8bfe2403256d00c31eadae42e55a1cab9a91`  
		Last Modified: Wed, 25 Dec 2024 01:52:15 GMT  
		Size: 11.9 KB (11903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95c917c7c1a2989a8e11a1aad523f0b96d75439b7d71b7c7554467cee49c6b87`  
		Last Modified: Wed, 25 Dec 2024 01:52:15 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9.4` - unknown; unknown

```console
$ docker pull chronograf@sha256:5741357b33ba8149db41ba4c2a3946bf56ed7898248b6cd03a167f8c31a51add
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2983441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:392ea0ece110bed1f5e54e027b44a3e91731773e5349bdf8631f27d8dc934a6e`

```dockerfile
```

-	Layers:
	-	`sha256:58d0927019a624f522e2d53b5e3add76e40ac0914b629d39da3e3f2f67a84bc2`  
		Last Modified: Wed, 25 Dec 2024 01:52:15 GMT  
		Size: 3.0 MB (2967536 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f740566634c83eeb29449799c1b2c3e34e390525099b18cbab78783adbef656`  
		Last Modified: Wed, 25 Dec 2024 01:52:15 GMT  
		Size: 15.9 KB (15905 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.9.4-alpine`

```console
$ docker pull chronograf@sha256:f929772f78639a674ebbc2e53e8a4ced0538836305b0e06466b4ba5e357e201c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.9.4-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:d88cfa90947735219bdb8d2f4b95507933de8b79d693e195271984103063c95a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23589801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ed5f81e66408f10c7f74167483c578d2885d23b86485222ae5002ad0d5ddae8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD alpine-minirootfs-3.20.4-x86_64.tar.gz / # buildkit
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
	-	`sha256:63b69af3dc5582ce6b63be03623e334ccd4e5cb4bde42702bbfc7a986a1bf432`  
		Last Modified: Tue, 07 Jan 2025 02:28:35 GMT  
		Size: 3.6 MB (3613999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bfbff95abbb53da6e174b003718b9702584d06532ba4018686ff2f03f3b4dfd`  
		Last Modified: Tue, 07 Jan 2025 03:30:54 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:835d456474e07ef91a0c109823461f5a1a05e2d84efd3d981f084fbe63627986`  
		Last Modified: Tue, 07 Jan 2025 03:30:54 GMT  
		Size: 279.1 KB (279134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fbf6fde88328234fcd4e691130955d09bfe23096d63780b58140acc48ddfae5`  
		Last Modified: Tue, 07 Jan 2025 03:30:55 GMT  
		Size: 19.7 MB (19672018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80edb5438907d16c4b509396aecc873ec01300a1bdfadcab97fcb994b1b2d3c9`  
		Last Modified: Tue, 07 Jan 2025 03:30:54 GMT  
		Size: 12.2 KB (12236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b88661ef4c63e9d4725d7519a7890d6776f1d8c0baf6ed47fc50829428ede7d0`  
		Last Modified: Tue, 07 Jan 2025 03:30:55 GMT  
		Size: 11.9 KB (11896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f6d4bdced72a5e0156ad0b46236ea3f3882be890a6d5e78d3983930e549fa71`  
		Last Modified: Tue, 07 Jan 2025 03:30:55 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9.4-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:67a6fc65a166055453a55fce4d944ed707e0147e964845e26459f46a7d1bfe03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.1 KB (246147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71a202451865885bcc8e3752c0b7a6a57be9ee98f872c66d117596c46e757db9`

```dockerfile
```

-	Layers:
	-	`sha256:be2322b4591902abe89c5084d777103dc55b26b7376edf330e17fa7acefbe9a6`  
		Last Modified: Tue, 07 Jan 2025 03:30:54 GMT  
		Size: 229.2 KB (229238 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ece7b302d5ade3bd7ddfa27720432db093ab401ddde671e3907cfd8b4bcc843`  
		Last Modified: Tue, 07 Jan 2025 03:30:54 GMT  
		Size: 16.9 KB (16909 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:alpine`

```console
$ docker pull chronograf@sha256:dde838ae1b743eb4d98d4b29b992fb7444b632ecbe2bf1b14e5bf78a96bcffa4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:ef35193e7e590e0a03c8550d74db0bec87be56cd5a15b1f020e966c6e6f78fb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31785614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c272e549048210a3ab50069f88ac438ed4a1707214e0b3289f84f0f491b34345`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD alpine-minirootfs-3.20.4-x86_64.tar.gz / # buildkit
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
	-	`sha256:63b69af3dc5582ce6b63be03623e334ccd4e5cb4bde42702bbfc7a986a1bf432`  
		Last Modified: Tue, 07 Jan 2025 02:28:35 GMT  
		Size: 3.6 MB (3613999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c46d8447fa31dea56913880abdd6f87f37a1a1f14aa39842807294d35b1db0d`  
		Last Modified: Tue, 07 Jan 2025 03:31:06 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fd617a6972020255d51696c8d3bfb0786fd896142684197413244eee22bc80a`  
		Last Modified: Tue, 07 Jan 2025 03:31:07 GMT  
		Size: 280.8 KB (280840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0487a8767300fb6ef70b3919b2fb90c086f446b646300015dcc0b044d9e5c8d`  
		Last Modified: Tue, 07 Jan 2025 03:31:08 GMT  
		Size: 27.9 MB (27866061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a04b3562cd1e0d44c469b817017c1201637c902bf3bd66a827b7a58eff33672`  
		Last Modified: Tue, 07 Jan 2025 03:31:07 GMT  
		Size: 12.2 KB (12241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01cb613e5324cd9d0a318d9f6ae96447ee7a0e708df412749fa68d9742015fe6`  
		Size: 11.9 KB (11901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a7bd88632473de5cac4c883ec9470a631e2fe300d21c49f850ae0649e48e02`  
		Last Modified: Tue, 07 Jan 2025 03:31:08 GMT  
		Size: 292.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:c7c0fc8d91df4e8247bf270f41096b92d1e798292131a24a526aa32cefe376a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.6 KB (253572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ddbcc06bbcdf739077f575ab496a6239c9ad10d086d07c0861161d270644d2d`

```dockerfile
```

-	Layers:
	-	`sha256:bfd112895266bbd1c01511dd3dcdd6257f837bab85bcfc0b208e594614f00913`  
		Last Modified: Tue, 07 Jan 2025 03:31:07 GMT  
		Size: 235.7 KB (235717 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f078ec94cbf82ebe831b16a9d2b06edf070b1ab167af5e09aadd4cedad2d42f`  
		Last Modified: Tue, 07 Jan 2025 03:31:07 GMT  
		Size: 17.9 KB (17855 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:latest`

```console
$ docker pull chronograf@sha256:b494e3f3eb6e647b352a93e639623cc6e854181c9d46a93e9b31e717f5074b8c
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
$ docker pull chronograf@sha256:6d6e2d67ef9cf89d6996942538989783fc8b3f91167f50841f9d8506369c72a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.2 MB (83154509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a0670664e2e0faf522c9087986ad3de12c4aba0585d409de31408553f0dd012`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
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
	-	`sha256:fd674058ff8f8cfa7fb8a20c006fc0128541cbbad7f7f7f28df570d08f9e4d92`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 28.2 MB (28231581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07687c0360bda289fea7f2a79d82292cbe6df4c80c8424a9073cc8381ee26269`  
		Last Modified: Tue, 24 Dec 2024 22:25:56 GMT  
		Size: 7.7 MB (7680873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:767cb31ef8d1819a81d3ff15fbee3ea57bf51c34324ff78484f03319e16c14bc`  
		Last Modified: Tue, 24 Dec 2024 22:25:57 GMT  
		Size: 47.2 MB (47217584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ae16e897c30f0ef8e2220d5cf12238b47c7dd479da1a541ce5e1dc2e124a1a6`  
		Last Modified: Tue, 24 Dec 2024 22:25:55 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f03b87843e34ecc6c966cde512b43bc5fe6cb9b03f5b3893d5119675caf1772`  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:967238f4eab21ca6c33f2dc208e381ad7d895d66fa0d1e9bc3cf2211f00d894f`  
		Last Modified: Tue, 24 Dec 2024 22:25:56 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:d8b32bee1973167d2abd19fc3e19747eaf5345d478f5ffd9cb07867b6b2de9e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2719989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7441887b68abb2a2cc80a500e90a8567e98e0b8529f2cf3155641245c93a0fd3`

```dockerfile
```

-	Layers:
	-	`sha256:5bea8c2a06958727ce0210bd47562fd31721974f71638aa7116f9db1c6acbf96`  
		Last Modified: Tue, 24 Dec 2024 22:25:55 GMT  
		Size: 2.7 MB (2703861 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:258ce8fe84e595d08f1bad1f0e307596f49dc98ce1e13ceb085385d56fe01c7e`  
		Last Modified: Tue, 24 Dec 2024 22:25:55 GMT  
		Size: 16.1 KB (16128 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:latest` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:902f9e124ef8eec6c6d6aaf937dbb351f8fbacba944250f4c20d1c548562ad11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.5 MB (74538543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09a47e055aad54318e8f2ff6dc0e255fab7e01a069a3554e2a719da9610348b0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1734912000'
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
	-	`sha256:24f0da30a772db626789cda3e7b0911098d07574c40b30be943d43dec3ed685f`  
		Last Modified: Tue, 24 Dec 2024 21:33:51 GMT  
		Size: 23.9 MB (23933522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a587153466beafd4a360abbe5227775fc6eb4f96163ff031f27ae280fbd146fb`  
		Last Modified: Wed, 25 Dec 2024 03:48:06 GMT  
		Size: 6.3 MB (6304249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:624273166d9b9dacbd343713c47d88140ca26bea1b6658b142897d4b2df9ebf1`  
		Last Modified: Wed, 25 Dec 2024 03:48:07 GMT  
		Size: 44.3 MB (44276315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb7936cd4fd8f299aa0fbf53ae0359605709f585ef631e09a1c56f056e388052`  
		Last Modified: Wed, 25 Dec 2024 03:48:06 GMT  
		Size: 12.2 KB (12241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4fb71a77718411db1d6fba7cd6cf5285481c6aa627fb6445de8c4127f06157f`  
		Last Modified: Wed, 25 Dec 2024 03:48:06 GMT  
		Size: 11.9 KB (11901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bd9b5d9635a02e3542dcd753d350662856b78a90805becda9f0f6df2b5499eb`  
		Last Modified: Wed, 25 Dec 2024 03:48:07 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:ccc99f48f31a9a61144299934ece16f81e3ead8caaf292e36e3c0d06edf456dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2722365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f34eac170ebb6e4736416f3d82546f9b45a22f5725f473e8ceac4b711e57017`

```dockerfile
```

-	Layers:
	-	`sha256:328f2d718a94e63d68a0992dd9b2063e42e664c8d2fb65f0cba9d7357f6d6578`  
		Last Modified: Wed, 25 Dec 2024 03:48:06 GMT  
		Size: 2.7 MB (2706158 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da1f387e2e6bf4b4a2bc73da901c5c3040bc3de0e55e0a86dbd36920bead94fd`  
		Last Modified: Wed, 25 Dec 2024 03:48:06 GMT  
		Size: 16.2 KB (16207 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:latest` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:9636dae65e9631cf82030227df43ce5a21a7f0684ef566279545187d8bc6cabf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.5 MB (80513234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c459246fb31ffeff8ee987e4e19750f98ac33a42fcc74c2a8b145dfa2c48f67d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
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
	-	`sha256:f5c6876bb3d7d368455916fa98c705330bd8a8d9c080ccea8fe4c4b35a2ecb1f`  
		Last Modified: Tue, 24 Dec 2024 21:34:20 GMT  
		Size: 28.1 MB (28058723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:232f29504ec153209d0d6933a57ff49bae77c7a6234e88fcaf11cad8a7723bee`  
		Last Modified: Wed, 25 Dec 2024 01:52:46 GMT  
		Size: 7.5 MB (7459496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b2d2416f3e06d017c146f7a008f7e832c79d4d743507977252bfad16ccc0f51`  
		Last Modified: Wed, 25 Dec 2024 01:52:47 GMT  
		Size: 45.0 MB (44970555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9c2199ac63999a5d396dd76b0f697485319d69a8bfd129d09eecd6edb26fd79`  
		Last Modified: Wed, 25 Dec 2024 01:52:46 GMT  
		Size: 12.2 KB (12243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0245154bee61145c1748e294d72f49b69d7eb92fe78d4630b386771a731479bc`  
		Last Modified: Wed, 25 Dec 2024 01:52:46 GMT  
		Size: 11.9 KB (11902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:016d64276c8a4c1da71ef108932f169f0ee0fce7f101fccf20bd38daec3d4e07`  
		Last Modified: Wed, 25 Dec 2024 01:52:46 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:f28bf7b20289699eb40567193016ae5cdaba2b5d26aeb72ef42cce03fc7d22e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2720369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5202c10d949b0915ae82ce7488826f450a9e0f4a360275b8c35f2fa907184ccc`

```dockerfile
```

-	Layers:
	-	`sha256:b4af31a11ba8ca753ae64b866a74ffb5d0db1c18f70d5da361e6a4b0c5aa9cfd`  
		Last Modified: Wed, 25 Dec 2024 01:52:46 GMT  
		Size: 2.7 MB (2704134 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fbd98a0ed9b4d372cc9ea8ab71090909acd3f2734850cf0288363ec174da8b31`  
		Last Modified: Wed, 25 Dec 2024 01:52:45 GMT  
		Size: 16.2 KB (16235 bytes)  
		MIME: application/vnd.in-toto+json
