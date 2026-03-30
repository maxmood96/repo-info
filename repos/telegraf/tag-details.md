<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `telegraf`

-	[`telegraf:1.36`](#telegraf136)
-	[`telegraf:1.36-alpine`](#telegraf136-alpine)
-	[`telegraf:1.36.4`](#telegraf1364)
-	[`telegraf:1.36.4-alpine`](#telegraf1364-alpine)
-	[`telegraf:1.37`](#telegraf137)
-	[`telegraf:1.37-alpine`](#telegraf137-alpine)
-	[`telegraf:1.37.3`](#telegraf1373)
-	[`telegraf:1.37.3-alpine`](#telegraf1373-alpine)
-	[`telegraf:1.38`](#telegraf138)
-	[`telegraf:1.38-alpine`](#telegraf138-alpine)
-	[`telegraf:1.38.2`](#telegraf1382)
-	[`telegraf:1.38.2-alpine`](#telegraf1382-alpine)
-	[`telegraf:alpine`](#telegrafalpine)
-	[`telegraf:latest`](#telegraflatest)

## `telegraf:1.36`

```console
$ docker pull telegraf@sha256:895c9ba2949612cf0d0155c80339bad9ccb71dcd6dff8fe6155d89d8b4ba3362
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.36` - linux; amd64

```console
$ docker pull telegraf@sha256:06134b709022d3916ee2b9d762723b63d876abff0e5f8f741f25a7c80f0d35d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.0 MB (171950541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:017c6aa30c9b51a2b82b9fc26a393d414efa06461f7c1f6e6b764c0326a86541`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:37:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:39:33 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:39:33 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 16 Mar 2026 23:39:37 GMT
ENV TELEGRAF_VERSION=1.36.4
# Mon, 16 Mar 2026 23:39:37 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 16 Mar 2026 23:39:37 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 16 Mar 2026 23:39:37 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 16 Mar 2026 23:39:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 16 Mar 2026 23:39:37 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:9d2f29087bcd6d99efd909a99095549425cd63e27c71b3bf37f108c6b7c370f9`  
		Last Modified: Mon, 16 Mar 2026 21:52:42 GMT  
		Size: 48.5 MB (48488584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26fa3468d221545a43d2151f3977695a31857f9342ba842627d03c9fa1b2ae02`  
		Last Modified: Mon, 16 Mar 2026 22:37:09 GMT  
		Size: 24.0 MB (24038304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:371942d4784fa8183c524aee980dfca3e6edfd0c67168eaab19e7c921b2a2778`  
		Last Modified: Mon, 16 Mar 2026 23:39:58 GMT  
		Size: 18.9 MB (18944420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c74f8c42157a6de63f9804ec1413a99ec9e6501d8d4d0a92e6deadc93698c98a`  
		Last Modified: Mon, 16 Mar 2026 23:39:57 GMT  
		Size: 5.1 KB (5055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d9063b18b02a43d1c445a40625317fa087b8d7056638349f45603c7c4b5b668`  
		Last Modified: Mon, 16 Mar 2026 23:39:59 GMT  
		Size: 80.5 MB (80473553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a57ae38fbd94f4536900cfe6384007d86784ef43c10b472f4962e084e93ecfe6`  
		Last Modified: Mon, 16 Mar 2026 23:39:57 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36` - unknown; unknown

```console
$ docker pull telegraf@sha256:ecb53e8fd3238536d852e1c6c21d8443b17191d447170444bdd8cd21de50f425
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6670530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f36e4ca34998863cfa2bbd96c7910d2b277b6a96131efeaa0a4bd12fc7baf9a`

```dockerfile
```

-	Layers:
	-	`sha256:aabc60fd79835532fea7d1a01dabcb894a916d1ca353d5162ba15d678fb1f70d`  
		Last Modified: Mon, 16 Mar 2026 23:39:57 GMT  
		Size: 6.7 MB (6656103 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7da90ee9c7b3eb1116885f705b5b7342d8cf39d63b7124ffe192cfae5964dc37`  
		Last Modified: Mon, 16 Mar 2026 23:39:56 GMT  
		Size: 14.4 KB (14427 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.36` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:f4c7d36732aa1776311252c00a6aa1f2d97fec3b1584e2280d9c6bb46a081df0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.8 MB (157818773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:593d3e222698523909b51b42b5a4cab2084e9a4fed22c97c52290e2c2143067d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 23:18:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:04:34 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:04:35 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 17 Mar 2026 01:04:41 GMT
ENV TELEGRAF_VERSION=1.36.4
# Tue, 17 Mar 2026 01:04:41 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 17 Mar 2026 01:04:41 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 17 Mar 2026 01:04:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:04:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Mar 2026 01:04:41 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:3e574dbe918dfcf76ab4fd7736cc3c62e552f2465f49a512ed26cfc623807024`  
		Last Modified: Mon, 16 Mar 2026 21:56:33 GMT  
		Size: 44.2 MB (44207568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab92577caba10dd52b0a4a93a140b02839815621e1e55d6eef1c846ec1932e81`  
		Last Modified: Mon, 16 Mar 2026 23:18:55 GMT  
		Size: 21.9 MB (21942056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c89f75eafdb2e92ab41bf14b8001db53b2a7c3362729ed7eb3bc9a72191c955`  
		Last Modified: Tue, 17 Mar 2026 01:05:02 GMT  
		Size: 17.7 MB (17699821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38e213c987f145547140d7cbd534869b26ec43bc69902432aff43896de7753ff`  
		Last Modified: Tue, 17 Mar 2026 01:05:00 GMT  
		Size: 5.1 KB (5070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dfb454401d17689aaea84be37328da0a11d3c7773e8eb0d6fb08a19c6405fb0`  
		Last Modified: Tue, 17 Mar 2026 01:05:04 GMT  
		Size: 74.0 MB (73963633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:086941cb83539f500b2d034c47b555bb6acc498e19c7dfc14dac1692d9635a5f`  
		Last Modified: Tue, 17 Mar 2026 01:05:01 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36` - unknown; unknown

```console
$ docker pull telegraf@sha256:2fa56cea76f7854f602705bb5ffb2d1c6fbb6bdf8ec4a72f3a11a265ee1930f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6665216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:132227c602ea3995200808308882d40c7028a538ac145cf07cc35b78b414b4cd`

```dockerfile
```

-	Layers:
	-	`sha256:acf44b9d2993dc78501062238a42685d92f169ca770f6d40318a79cd72f0914e`  
		Last Modified: Tue, 17 Mar 2026 01:05:01 GMT  
		Size: 6.7 MB (6650700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efb01ae79bcdb02fd663a09acd1f5e466ee29f421d7988f23c18c36ff7f16efa`  
		Last Modified: Tue, 17 Mar 2026 01:05:01 GMT  
		Size: 14.5 KB (14516 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.36` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:0493489dc7366f2e155d1341903e1980c539367f009015f8728edddb669d0de1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.7 MB (162669599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdee426af7717d4454fcddcff432aafe1766b22da74010a96951499c47d4d10a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:39:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:44:12 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:44:12 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 16 Mar 2026 23:44:16 GMT
ENV TELEGRAF_VERSION=1.36.4
# Mon, 16 Mar 2026 23:44:16 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 16 Mar 2026 23:44:16 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 16 Mar 2026 23:44:16 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 16 Mar 2026 23:44:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 16 Mar 2026 23:44:16 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:2ea98bb5eec9d02a0d7b59638c683db4e1e749f998a317bc731e9506f8480b12`  
		Last Modified: Mon, 16 Mar 2026 21:52:02 GMT  
		Size: 48.4 MB (48373032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efbce225727d69d170353500d8834770da849cbdcea48de37e492fe14ef880d0`  
		Last Modified: Mon, 16 Mar 2026 22:39:28 GMT  
		Size: 23.6 MB (23604701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:230b677ac959921d24705f779e075e8fcd18ac5a6b5e4710804e82f26406d083`  
		Last Modified: Mon, 16 Mar 2026 23:44:34 GMT  
		Size: 18.9 MB (18885843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04d71b57e0284b71ae6e007deb674d85690c061feafb943276722641030b45f7`  
		Last Modified: Mon, 16 Mar 2026 23:44:33 GMT  
		Size: 5.1 KB (5056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e109fac7ccc708f3107ff09e0780481ba89d2bd57fffa97b2abdb15ae61e3a6`  
		Last Modified: Mon, 16 Mar 2026 23:44:36 GMT  
		Size: 71.8 MB (71800342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d1ece525decb20608d94d0003ce05b90a03a4e6f8fadfa2d48a58bbcd39d032`  
		Last Modified: Mon, 16 Mar 2026 23:44:33 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36` - unknown; unknown

```console
$ docker pull telegraf@sha256:cca6336d17d44b7852d4cbda9e247188f219c21a8261c0b0f1b9d5da37416cbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6671316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9695e93ebb0a92ef436ee62d424fcce25787d50a390fb2aa49acd38b72d844b4`

```dockerfile
```

-	Layers:
	-	`sha256:8c5206b4df20ae4c98be42a232d960147d3a691327fee930c37fd20dc6679e18`  
		Last Modified: Mon, 16 Mar 2026 23:44:34 GMT  
		Size: 6.7 MB (6656779 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc67df415c7c6fc8268d4230fa298138112ec5a4bfd011c670c4a39c510caa41`  
		Last Modified: Mon, 16 Mar 2026 23:44:33 GMT  
		Size: 14.5 KB (14537 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.36-alpine`

```console
$ docker pull telegraf@sha256:74614dd18bd8c984d8d5423d6c362da8b9a0c32543f9932660f03c1e8ae22893
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.36-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:7e104d74dd7644a3f52e10b68cf4972907df0e16d541772b9da2cd987768f243
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.6 MB (86645547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:541b370deeda7910ea7253b472ecc2c000614befbc68504928d0ace6afb8ac2d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:49:38 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 03:49:39 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 03:49:47 GMT
ENV TELEGRAF_VERSION=1.36.4
# Wed, 28 Jan 2026 03:49:47 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Wed, 28 Jan 2026 03:49:47 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Wed, 28 Jan 2026 03:49:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:49:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:49:47 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b7d7273f9660e4714a4f3a80280881a133da7a4b266dd62099a308eb162f72`  
		Last Modified: Wed, 28 Jan 2026 03:50:00 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a28aadc15040b0a36abb07e3769a9f303cb26e56ef3f0d93b8d67305467d8fd`  
		Last Modified: Wed, 28 Jan 2026 03:50:03 GMT  
		Size: 2.6 MB (2563616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc81e34cf097b50b7dd067c2614b05e26095fb2414a929a91855343b1d90a521`  
		Last Modified: Wed, 28 Jan 2026 03:50:04 GMT  
		Size: 80.3 MB (80276156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b661496d98862b6bcadcc878a91c0481a10a977bd7484506964f0fa597e847e4`  
		Last Modified: Wed, 28 Jan 2026 03:50:01 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:a58b7e8c82dd5051261d6c864d491aeea150486c9e1f27c7ee855fb6a31203aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1157226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d48411f51293ab3606c49c94104046ecf052e493bbfcfe2f480129ab5409030c`

```dockerfile
```

-	Layers:
	-	`sha256:da625155b1394d0acc62042503f8abc1c81a442603c6d3593589a8d4a55f6341`  
		Last Modified: Wed, 28 Jan 2026 03:50:02 GMT  
		Size: 1.1 MB (1142308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de3d21cf0caad0d90bd450ac8df7e7d30e8f0aad489474e9e436f77f5ade2fca`  
		Last Modified: Wed, 28 Jan 2026 03:50:02 GMT  
		Size: 14.9 KB (14918 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.36-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:83bc8287ed0eb1b80b20475a90d070e187731561e718f2dd3895fe06431022eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.4 MB (78367221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54eb1f6fb6136da60a3f40864a08a135e84bee5208c5d660116eebe674366a33`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:56:03 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 03:56:05 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 03:56:13 GMT
ENV TELEGRAF_VERSION=1.36.4
# Wed, 28 Jan 2026 03:56:13 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Wed, 28 Jan 2026 03:56:13 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Wed, 28 Jan 2026 03:56:13 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:56:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:56:13 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:091ad53e26795247908fee75f1fec45378bfe7b9ed2893274f93b24025ac8c82`  
		Last Modified: Wed, 28 Jan 2026 03:56:27 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d9006dcde8e9ae246bba52f47cf327cff96c0b85caea2b7bb7c9054ff07b9d3`  
		Last Modified: Wed, 28 Jan 2026 03:56:27 GMT  
		Size: 2.6 MB (2627637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc9571296956dfa14bf2102b6281cfc90613780a517750c02daae06df9c48984`  
		Last Modified: Wed, 28 Jan 2026 03:56:29 GMT  
		Size: 71.6 MB (71599165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c402cd3a778e5774ca08af5f6640eaf81bb54e3bf015248f992dc3bedf0c94b6`  
		Last Modified: Wed, 28 Jan 2026 03:56:27 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:8ae6952c3c19ba215996ca8b6bd4634c696319744b633dceb09a71bf50bdd603
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1152962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71490915f7d134e9704e5bc89bfda33a5b8c3561ce98c890715d964fc114d237`

```dockerfile
```

-	Layers:
	-	`sha256:df6dda659050fe9d9dda0bd1f9f03b6be5573bf09cac3651532af6a2c3d3d82a`  
		Last Modified: Wed, 28 Jan 2026 03:56:27 GMT  
		Size: 1.1 MB (1137935 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56c95dceab1d5fe3c1330859a4271ff252f83fe230c9b155b95b00d6ee2a76c2`  
		Last Modified: Wed, 28 Jan 2026 03:56:27 GMT  
		Size: 15.0 KB (15027 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.36.4`

```console
$ docker pull telegraf@sha256:895c9ba2949612cf0d0155c80339bad9ccb71dcd6dff8fe6155d89d8b4ba3362
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.36.4` - linux; amd64

```console
$ docker pull telegraf@sha256:06134b709022d3916ee2b9d762723b63d876abff0e5f8f741f25a7c80f0d35d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.0 MB (171950541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:017c6aa30c9b51a2b82b9fc26a393d414efa06461f7c1f6e6b764c0326a86541`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:37:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:39:33 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:39:33 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 16 Mar 2026 23:39:37 GMT
ENV TELEGRAF_VERSION=1.36.4
# Mon, 16 Mar 2026 23:39:37 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 16 Mar 2026 23:39:37 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 16 Mar 2026 23:39:37 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 16 Mar 2026 23:39:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 16 Mar 2026 23:39:37 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:9d2f29087bcd6d99efd909a99095549425cd63e27c71b3bf37f108c6b7c370f9`  
		Last Modified: Mon, 16 Mar 2026 21:52:42 GMT  
		Size: 48.5 MB (48488584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26fa3468d221545a43d2151f3977695a31857f9342ba842627d03c9fa1b2ae02`  
		Last Modified: Mon, 16 Mar 2026 22:37:09 GMT  
		Size: 24.0 MB (24038304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:371942d4784fa8183c524aee980dfca3e6edfd0c67168eaab19e7c921b2a2778`  
		Last Modified: Mon, 16 Mar 2026 23:39:58 GMT  
		Size: 18.9 MB (18944420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c74f8c42157a6de63f9804ec1413a99ec9e6501d8d4d0a92e6deadc93698c98a`  
		Last Modified: Mon, 16 Mar 2026 23:39:57 GMT  
		Size: 5.1 KB (5055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d9063b18b02a43d1c445a40625317fa087b8d7056638349f45603c7c4b5b668`  
		Last Modified: Mon, 16 Mar 2026 23:39:59 GMT  
		Size: 80.5 MB (80473553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a57ae38fbd94f4536900cfe6384007d86784ef43c10b472f4962e084e93ecfe6`  
		Last Modified: Mon, 16 Mar 2026 23:39:57 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36.4` - unknown; unknown

```console
$ docker pull telegraf@sha256:ecb53e8fd3238536d852e1c6c21d8443b17191d447170444bdd8cd21de50f425
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6670530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f36e4ca34998863cfa2bbd96c7910d2b277b6a96131efeaa0a4bd12fc7baf9a`

```dockerfile
```

-	Layers:
	-	`sha256:aabc60fd79835532fea7d1a01dabcb894a916d1ca353d5162ba15d678fb1f70d`  
		Last Modified: Mon, 16 Mar 2026 23:39:57 GMT  
		Size: 6.7 MB (6656103 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7da90ee9c7b3eb1116885f705b5b7342d8cf39d63b7124ffe192cfae5964dc37`  
		Last Modified: Mon, 16 Mar 2026 23:39:56 GMT  
		Size: 14.4 KB (14427 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.36.4` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:f4c7d36732aa1776311252c00a6aa1f2d97fec3b1584e2280d9c6bb46a081df0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.8 MB (157818773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:593d3e222698523909b51b42b5a4cab2084e9a4fed22c97c52290e2c2143067d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 23:18:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:04:34 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:04:35 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 17 Mar 2026 01:04:41 GMT
ENV TELEGRAF_VERSION=1.36.4
# Tue, 17 Mar 2026 01:04:41 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 17 Mar 2026 01:04:41 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 17 Mar 2026 01:04:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:04:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Mar 2026 01:04:41 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:3e574dbe918dfcf76ab4fd7736cc3c62e552f2465f49a512ed26cfc623807024`  
		Last Modified: Mon, 16 Mar 2026 21:56:33 GMT  
		Size: 44.2 MB (44207568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab92577caba10dd52b0a4a93a140b02839815621e1e55d6eef1c846ec1932e81`  
		Last Modified: Mon, 16 Mar 2026 23:18:55 GMT  
		Size: 21.9 MB (21942056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c89f75eafdb2e92ab41bf14b8001db53b2a7c3362729ed7eb3bc9a72191c955`  
		Last Modified: Tue, 17 Mar 2026 01:05:02 GMT  
		Size: 17.7 MB (17699821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38e213c987f145547140d7cbd534869b26ec43bc69902432aff43896de7753ff`  
		Last Modified: Tue, 17 Mar 2026 01:05:00 GMT  
		Size: 5.1 KB (5070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dfb454401d17689aaea84be37328da0a11d3c7773e8eb0d6fb08a19c6405fb0`  
		Last Modified: Tue, 17 Mar 2026 01:05:04 GMT  
		Size: 74.0 MB (73963633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:086941cb83539f500b2d034c47b555bb6acc498e19c7dfc14dac1692d9635a5f`  
		Last Modified: Tue, 17 Mar 2026 01:05:01 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36.4` - unknown; unknown

```console
$ docker pull telegraf@sha256:2fa56cea76f7854f602705bb5ffb2d1c6fbb6bdf8ec4a72f3a11a265ee1930f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6665216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:132227c602ea3995200808308882d40c7028a538ac145cf07cc35b78b414b4cd`

```dockerfile
```

-	Layers:
	-	`sha256:acf44b9d2993dc78501062238a42685d92f169ca770f6d40318a79cd72f0914e`  
		Last Modified: Tue, 17 Mar 2026 01:05:01 GMT  
		Size: 6.7 MB (6650700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efb01ae79bcdb02fd663a09acd1f5e466ee29f421d7988f23c18c36ff7f16efa`  
		Last Modified: Tue, 17 Mar 2026 01:05:01 GMT  
		Size: 14.5 KB (14516 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.36.4` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:0493489dc7366f2e155d1341903e1980c539367f009015f8728edddb669d0de1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.7 MB (162669599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdee426af7717d4454fcddcff432aafe1766b22da74010a96951499c47d4d10a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:39:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:44:12 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:44:12 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 16 Mar 2026 23:44:16 GMT
ENV TELEGRAF_VERSION=1.36.4
# Mon, 16 Mar 2026 23:44:16 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 16 Mar 2026 23:44:16 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 16 Mar 2026 23:44:16 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 16 Mar 2026 23:44:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 16 Mar 2026 23:44:16 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:2ea98bb5eec9d02a0d7b59638c683db4e1e749f998a317bc731e9506f8480b12`  
		Last Modified: Mon, 16 Mar 2026 21:52:02 GMT  
		Size: 48.4 MB (48373032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efbce225727d69d170353500d8834770da849cbdcea48de37e492fe14ef880d0`  
		Last Modified: Mon, 16 Mar 2026 22:39:28 GMT  
		Size: 23.6 MB (23604701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:230b677ac959921d24705f779e075e8fcd18ac5a6b5e4710804e82f26406d083`  
		Last Modified: Mon, 16 Mar 2026 23:44:34 GMT  
		Size: 18.9 MB (18885843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04d71b57e0284b71ae6e007deb674d85690c061feafb943276722641030b45f7`  
		Last Modified: Mon, 16 Mar 2026 23:44:33 GMT  
		Size: 5.1 KB (5056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e109fac7ccc708f3107ff09e0780481ba89d2bd57fffa97b2abdb15ae61e3a6`  
		Last Modified: Mon, 16 Mar 2026 23:44:36 GMT  
		Size: 71.8 MB (71800342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d1ece525decb20608d94d0003ce05b90a03a4e6f8fadfa2d48a58bbcd39d032`  
		Last Modified: Mon, 16 Mar 2026 23:44:33 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36.4` - unknown; unknown

```console
$ docker pull telegraf@sha256:cca6336d17d44b7852d4cbda9e247188f219c21a8261c0b0f1b9d5da37416cbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6671316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9695e93ebb0a92ef436ee62d424fcce25787d50a390fb2aa49acd38b72d844b4`

```dockerfile
```

-	Layers:
	-	`sha256:8c5206b4df20ae4c98be42a232d960147d3a691327fee930c37fd20dc6679e18`  
		Last Modified: Mon, 16 Mar 2026 23:44:34 GMT  
		Size: 6.7 MB (6656779 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc67df415c7c6fc8268d4230fa298138112ec5a4bfd011c670c4a39c510caa41`  
		Last Modified: Mon, 16 Mar 2026 23:44:33 GMT  
		Size: 14.5 KB (14537 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.36.4-alpine`

```console
$ docker pull telegraf@sha256:74614dd18bd8c984d8d5423d6c362da8b9a0c32543f9932660f03c1e8ae22893
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.36.4-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:7e104d74dd7644a3f52e10b68cf4972907df0e16d541772b9da2cd987768f243
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.6 MB (86645547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:541b370deeda7910ea7253b472ecc2c000614befbc68504928d0ace6afb8ac2d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:49:38 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 03:49:39 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 03:49:47 GMT
ENV TELEGRAF_VERSION=1.36.4
# Wed, 28 Jan 2026 03:49:47 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Wed, 28 Jan 2026 03:49:47 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Wed, 28 Jan 2026 03:49:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:49:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:49:47 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b7d7273f9660e4714a4f3a80280881a133da7a4b266dd62099a308eb162f72`  
		Last Modified: Wed, 28 Jan 2026 03:50:00 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a28aadc15040b0a36abb07e3769a9f303cb26e56ef3f0d93b8d67305467d8fd`  
		Last Modified: Wed, 28 Jan 2026 03:50:03 GMT  
		Size: 2.6 MB (2563616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc81e34cf097b50b7dd067c2614b05e26095fb2414a929a91855343b1d90a521`  
		Last Modified: Wed, 28 Jan 2026 03:50:04 GMT  
		Size: 80.3 MB (80276156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b661496d98862b6bcadcc878a91c0481a10a977bd7484506964f0fa597e847e4`  
		Last Modified: Wed, 28 Jan 2026 03:50:01 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36.4-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:a58b7e8c82dd5051261d6c864d491aeea150486c9e1f27c7ee855fb6a31203aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1157226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d48411f51293ab3606c49c94104046ecf052e493bbfcfe2f480129ab5409030c`

```dockerfile
```

-	Layers:
	-	`sha256:da625155b1394d0acc62042503f8abc1c81a442603c6d3593589a8d4a55f6341`  
		Last Modified: Wed, 28 Jan 2026 03:50:02 GMT  
		Size: 1.1 MB (1142308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de3d21cf0caad0d90bd450ac8df7e7d30e8f0aad489474e9e436f77f5ade2fca`  
		Last Modified: Wed, 28 Jan 2026 03:50:02 GMT  
		Size: 14.9 KB (14918 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.36.4-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:83bc8287ed0eb1b80b20475a90d070e187731561e718f2dd3895fe06431022eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.4 MB (78367221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54eb1f6fb6136da60a3f40864a08a135e84bee5208c5d660116eebe674366a33`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:56:03 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 03:56:05 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 03:56:13 GMT
ENV TELEGRAF_VERSION=1.36.4
# Wed, 28 Jan 2026 03:56:13 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Wed, 28 Jan 2026 03:56:13 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Wed, 28 Jan 2026 03:56:13 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:56:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:56:13 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:091ad53e26795247908fee75f1fec45378bfe7b9ed2893274f93b24025ac8c82`  
		Last Modified: Wed, 28 Jan 2026 03:56:27 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d9006dcde8e9ae246bba52f47cf327cff96c0b85caea2b7bb7c9054ff07b9d3`  
		Last Modified: Wed, 28 Jan 2026 03:56:27 GMT  
		Size: 2.6 MB (2627637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc9571296956dfa14bf2102b6281cfc90613780a517750c02daae06df9c48984`  
		Last Modified: Wed, 28 Jan 2026 03:56:29 GMT  
		Size: 71.6 MB (71599165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c402cd3a778e5774ca08af5f6640eaf81bb54e3bf015248f992dc3bedf0c94b6`  
		Last Modified: Wed, 28 Jan 2026 03:56:27 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36.4-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:8ae6952c3c19ba215996ca8b6bd4634c696319744b633dceb09a71bf50bdd603
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1152962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71490915f7d134e9704e5bc89bfda33a5b8c3561ce98c890715d964fc114d237`

```dockerfile
```

-	Layers:
	-	`sha256:df6dda659050fe9d9dda0bd1f9f03b6be5573bf09cac3651532af6a2c3d3d82a`  
		Last Modified: Wed, 28 Jan 2026 03:56:27 GMT  
		Size: 1.1 MB (1137935 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56c95dceab1d5fe3c1330859a4271ff252f83fe230c9b155b95b00d6ee2a76c2`  
		Last Modified: Wed, 28 Jan 2026 03:56:27 GMT  
		Size: 15.0 KB (15027 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.37`

```console
$ docker pull telegraf@sha256:8bb4018fd238874ddb216857586393adfe93ee6be5995f8973cb48bcca781ba2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.37` - linux; amd64

```console
$ docker pull telegraf@sha256:dfd4c7c82108908d39df1afaf86773abc1aad3ee4651970f3df7e029a7c57307
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.3 MB (172260139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ef6655908f6972b691df41a009c09f3f74be417b0a519ac735c2782b9d895bd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:37:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:39:36 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:39:37 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 16 Mar 2026 23:39:40 GMT
ENV TELEGRAF_VERSION=1.37.3
# Mon, 16 Mar 2026 23:39:40 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 16 Mar 2026 23:39:40 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 16 Mar 2026 23:39:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 16 Mar 2026 23:39:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 16 Mar 2026 23:39:41 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:9d2f29087bcd6d99efd909a99095549425cd63e27c71b3bf37f108c6b7c370f9`  
		Last Modified: Mon, 16 Mar 2026 21:52:42 GMT  
		Size: 48.5 MB (48488584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26fa3468d221545a43d2151f3977695a31857f9342ba842627d03c9fa1b2ae02`  
		Last Modified: Mon, 16 Mar 2026 22:37:09 GMT  
		Size: 24.0 MB (24038304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7ca299949b7873bda77bfee8b697d3ae3ad84728e2e1050936aee979a1693bd`  
		Last Modified: Mon, 16 Mar 2026 23:40:04 GMT  
		Size: 18.9 MB (18944347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55b87bdc42f7f7e87bfeac9567f08d6280142f8debeae55e1bfe592badec4855`  
		Last Modified: Mon, 16 Mar 2026 23:40:03 GMT  
		Size: 5.1 KB (5070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9116717a948b97059d8a61a62f03c9ea7a5186096875384841e45f97f3a93596`  
		Last Modified: Mon, 16 Mar 2026 23:40:06 GMT  
		Size: 80.8 MB (80783210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d2bb197156c6c8b02e324d59ccb82fc8156483efe60e4bfdcc8434159a28542`  
		Last Modified: Mon, 16 Mar 2026 23:40:03 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.37` - unknown; unknown

```console
$ docker pull telegraf@sha256:b05485d416dd0d887be9da49856787441de493bb9501d493cd1b57ada5069a0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6681385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c6f86c106bed79942eaadd2222a4bf2152e94235b78bdd2715d3a58ecc2da28`

```dockerfile
```

-	Layers:
	-	`sha256:cd2b2b371aebdde7ebd816cdfb3f315f40dc26d1977eea06a856520460c51ba5`  
		Last Modified: Mon, 16 Mar 2026 23:40:04 GMT  
		Size: 6.7 MB (6666958 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eaf36f9d988856ec2516a934923e86fba5aba63b99b6cac8c1fae60aa71d22ee`  
		Last Modified: Mon, 16 Mar 2026 23:40:03 GMT  
		Size: 14.4 KB (14427 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.37` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:e83d79dd42195c49abb2ce52d3907fc9b207d9635ce382ee66bae2b1418dcbd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.5 MB (158472459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2193d35a4e8c05d5f12aace9161486f1b8311f7aa38cdd7c5413feb416e3f55`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 23:18:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:04:45 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:04:45 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 17 Mar 2026 01:04:53 GMT
ENV TELEGRAF_VERSION=1.37.3
# Tue, 17 Mar 2026 01:04:53 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 17 Mar 2026 01:04:53 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 17 Mar 2026 01:04:53 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:04:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Mar 2026 01:04:53 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:3e574dbe918dfcf76ab4fd7736cc3c62e552f2465f49a512ed26cfc623807024`  
		Last Modified: Mon, 16 Mar 2026 21:56:33 GMT  
		Size: 44.2 MB (44207568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab92577caba10dd52b0a4a93a140b02839815621e1e55d6eef1c846ec1932e81`  
		Last Modified: Mon, 16 Mar 2026 23:18:55 GMT  
		Size: 21.9 MB (21942056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5b00520d158d5f9559c7b13e7b0a4e88c9e7af14132004e9044b23ed699729b`  
		Last Modified: Tue, 17 Mar 2026 01:05:14 GMT  
		Size: 17.7 MB (17699735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f34f19e1d368e90a9ed8be2272d7e68b466bad9e0bc6d63b00d6489130074d8`  
		Last Modified: Tue, 17 Mar 2026 01:05:13 GMT  
		Size: 5.1 KB (5055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24436afcf38fd62dc9370cb940807caea711aa7561469406a8e95e6e777d9de3`  
		Last Modified: Tue, 17 Mar 2026 01:05:15 GMT  
		Size: 74.6 MB (74617420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ba0eef8fb852c9ce7209e1ee8b41651dd190f696c28dd9ac568611f7716400a`  
		Last Modified: Tue, 17 Mar 2026 01:05:13 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.37` - unknown; unknown

```console
$ docker pull telegraf@sha256:98249aa6ce2c7d05aaa94a090d0a4cf56fa4eb5f10c98cc360a89bdb6ba45885
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6676071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:735ebaa43504ccd154232936d746d5b90c812ab843f57019e065dbee98de8c95`

```dockerfile
```

-	Layers:
	-	`sha256:edae3da1af807f5a69de75e37750bd9ca1df4eebba417d79d8d3cd3a2d4fa693`  
		Last Modified: Tue, 17 Mar 2026 01:05:13 GMT  
		Size: 6.7 MB (6661555 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae69fdfcbd45f104d597e60703e42deabf25d3466f7f69469677bef6055a724f`  
		Last Modified: Tue, 17 Mar 2026 01:05:13 GMT  
		Size: 14.5 KB (14516 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.37` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:e315f9f8a1d08a7f64bc392ca283c064df167d8acb6b59ad6c6f956b1890a244
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.0 MB (163040181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04129d47b908bb1bc7e24cd6b42b4d23d699ba5d2081b39dfa022c05a654e639`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:39:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:44:15 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:44:16 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 16 Mar 2026 23:44:22 GMT
ENV TELEGRAF_VERSION=1.37.3
# Mon, 16 Mar 2026 23:44:22 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 16 Mar 2026 23:44:22 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 16 Mar 2026 23:44:22 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 16 Mar 2026 23:44:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 16 Mar 2026 23:44:22 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:2ea98bb5eec9d02a0d7b59638c683db4e1e749f998a317bc731e9506f8480b12`  
		Last Modified: Mon, 16 Mar 2026 21:52:02 GMT  
		Size: 48.4 MB (48373032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efbce225727d69d170353500d8834770da849cbdcea48de37e492fe14ef880d0`  
		Last Modified: Mon, 16 Mar 2026 22:39:28 GMT  
		Size: 23.6 MB (23604701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f775c25b6076386e8aadb02bbe54f427d15b0df69bc2c922a0622a0edd02377d`  
		Last Modified: Mon, 16 Mar 2026 23:44:40 GMT  
		Size: 18.9 MB (18885751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73037eadef315b9d4ad3acfd4bcff10755d304010d9c9a6c5829cefd40137814`  
		Last Modified: Mon, 16 Mar 2026 23:44:39 GMT  
		Size: 5.1 KB (5073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a505bf10e5a5a9424b1217ceb248f13a5a77fd37ff5fa8d9cb299a211e9fb6d`  
		Last Modified: Mon, 16 Mar 2026 23:44:42 GMT  
		Size: 72.2 MB (72171001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:715d737bb6ea059ec90b850858afb8bbd8e72c833ecde271774f79e256fdc8ad`  
		Last Modified: Mon, 16 Mar 2026 23:44:39 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.37` - unknown; unknown

```console
$ docker pull telegraf@sha256:16399fffb3ede1ac2cad6a32a23c2a22b48775eb16eae15828dc99534a0c28f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6682171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3afc75bf908e5acb4477c13bf73b13e30f397487f46da9a85f10cbf99edd942`

```dockerfile
```

-	Layers:
	-	`sha256:4816e5b8cd0fe15e89bb032c1c62236e2abae8eb58151259dd2a128481e17189`  
		Last Modified: Mon, 16 Mar 2026 23:44:40 GMT  
		Size: 6.7 MB (6667634 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b950037ac067bdae0b5dc60e3a6b20661c9c953add2fa9cc1c36a72f7e210bb`  
		Last Modified: Mon, 16 Mar 2026 23:44:39 GMT  
		Size: 14.5 KB (14537 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.37-alpine`

```console
$ docker pull telegraf@sha256:a550e63a2efbea4b49596e475f0fcd3b057ff2ab0dfc8102357de289ee342a37
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.37-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:fba66fd8b08dc6e56336289fd91c0b9c055b5431b1ac6f0cb3c5b0203b24d450
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.9 MB (86946044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38efb96d204dcce61a2419f13705ddf967966bbf6c20b8dc214d6cd4917df5cc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Mon, 23 Feb 2026 22:13:06 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 23 Feb 2026 22:13:07 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 23 Feb 2026 22:13:15 GMT
ENV TELEGRAF_VERSION=1.37.3
# Mon, 23 Feb 2026 22:13:15 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 23 Feb 2026 22:13:15 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 23 Feb 2026 22:13:15 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 23 Feb 2026 22:13:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Feb 2026 22:13:15 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce2b56c151750e24306076f9157dce93616ec037d271702f125dc64fbf3376f8`  
		Last Modified: Mon, 23 Feb 2026 22:13:30 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aff331311971b9e1b3df00d187242872c6a7167b0fa5eb1b83bf07f57f6bd227`  
		Last Modified: Mon, 23 Feb 2026 22:13:30 GMT  
		Size: 2.6 MB (2563613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:749b176fa3df8ddfa0c79b45cb78b9caf938ca77b7d56b923cdb8d9280c85548`  
		Last Modified: Mon, 23 Feb 2026 22:13:33 GMT  
		Size: 80.6 MB (80576658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3a622797146e400edbb8a20860c8044210bb4ddf360b881dd59f657a0178e56`  
		Last Modified: Mon, 23 Feb 2026 22:13:30 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.37-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:dbaf7ed8916c29f7e0e480a7ad699dbc11e6ff21f59b298ac7bc4c687f919ec4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1168683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b161c64ca482da5f21d71566f132f54ee64beb84f28a79454afce77c61e7ad74`

```dockerfile
```

-	Layers:
	-	`sha256:0ad1ed01319ca47cfb93e453ec6fce2996425a3ef91fb812891757a8a27d72c6`  
		Last Modified: Mon, 23 Feb 2026 22:13:30 GMT  
		Size: 1.2 MB (1153465 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:841e3534e20e0f7236187feb211ea64b35f00fbef79dd247d04d44865d348a5d`  
		Last Modified: Mon, 23 Feb 2026 22:13:30 GMT  
		Size: 15.2 KB (15218 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.37-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:f27c6f05cce7d68495838dcbbe51d1995f3ba235846d6753718f5b2cd8a7f603
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.7 MB (78730556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5048f1f9cdf423929349c19bb659110cd4c7e1ab38dff7597763063c5a1978b3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Mon, 23 Feb 2026 22:12:02 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 23 Feb 2026 22:12:04 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 23 Feb 2026 22:12:09 GMT
ENV TELEGRAF_VERSION=1.37.3
# Mon, 23 Feb 2026 22:12:09 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 23 Feb 2026 22:12:09 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 23 Feb 2026 22:12:09 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 23 Feb 2026 22:12:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Feb 2026 22:12:09 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f365fa2017a849f86d84f3f3776e527b8ff2fb4628dfa52b2e2726747ba9a5f`  
		Last Modified: Mon, 23 Feb 2026 22:12:22 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01dde69daba6471771a33e89fc18e2ef827eac0bbebbfa518372b5614a4c5072`  
		Last Modified: Mon, 23 Feb 2026 22:12:23 GMT  
		Size: 2.6 MB (2627610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83fb53f42b0075065a38f3acdda1775b06ee78f844307d7125a10b6688253f62`  
		Last Modified: Mon, 23 Feb 2026 22:12:24 GMT  
		Size: 72.0 MB (71962529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d896748b58358906c78fda48ddade4bd1df0e660097580f49b6f08d0bb041131`  
		Last Modified: Mon, 23 Feb 2026 22:12:22 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.37-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:f2ad750ecb35ac8a316aa4496da66885dfc42a651a503859707823f2d6f4ca2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1164446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9b3b3372362c4275569df86547f57711280021d198691725283f623157d5487`

```dockerfile
```

-	Layers:
	-	`sha256:84a7770deb78578c6e010d0e4268d870b145b32e787666e68441fd2377878852`  
		Last Modified: Mon, 23 Feb 2026 22:12:22 GMT  
		Size: 1.1 MB (1149104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b83295c00d09abd5a3a9c39ebd649a814a4169ff62cc5041580c6c7c1bfd6e5`  
		Last Modified: Mon, 23 Feb 2026 22:12:23 GMT  
		Size: 15.3 KB (15342 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.37.3`

```console
$ docker pull telegraf@sha256:8bb4018fd238874ddb216857586393adfe93ee6be5995f8973cb48bcca781ba2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.37.3` - linux; amd64

```console
$ docker pull telegraf@sha256:dfd4c7c82108908d39df1afaf86773abc1aad3ee4651970f3df7e029a7c57307
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.3 MB (172260139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ef6655908f6972b691df41a009c09f3f74be417b0a519ac735c2782b9d895bd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:37:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:39:36 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:39:37 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 16 Mar 2026 23:39:40 GMT
ENV TELEGRAF_VERSION=1.37.3
# Mon, 16 Mar 2026 23:39:40 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 16 Mar 2026 23:39:40 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 16 Mar 2026 23:39:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 16 Mar 2026 23:39:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 16 Mar 2026 23:39:41 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:9d2f29087bcd6d99efd909a99095549425cd63e27c71b3bf37f108c6b7c370f9`  
		Last Modified: Mon, 16 Mar 2026 21:52:42 GMT  
		Size: 48.5 MB (48488584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26fa3468d221545a43d2151f3977695a31857f9342ba842627d03c9fa1b2ae02`  
		Last Modified: Mon, 16 Mar 2026 22:37:09 GMT  
		Size: 24.0 MB (24038304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7ca299949b7873bda77bfee8b697d3ae3ad84728e2e1050936aee979a1693bd`  
		Last Modified: Mon, 16 Mar 2026 23:40:04 GMT  
		Size: 18.9 MB (18944347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55b87bdc42f7f7e87bfeac9567f08d6280142f8debeae55e1bfe592badec4855`  
		Last Modified: Mon, 16 Mar 2026 23:40:03 GMT  
		Size: 5.1 KB (5070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9116717a948b97059d8a61a62f03c9ea7a5186096875384841e45f97f3a93596`  
		Last Modified: Mon, 16 Mar 2026 23:40:06 GMT  
		Size: 80.8 MB (80783210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d2bb197156c6c8b02e324d59ccb82fc8156483efe60e4bfdcc8434159a28542`  
		Last Modified: Mon, 16 Mar 2026 23:40:03 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.37.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:b05485d416dd0d887be9da49856787441de493bb9501d493cd1b57ada5069a0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6681385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c6f86c106bed79942eaadd2222a4bf2152e94235b78bdd2715d3a58ecc2da28`

```dockerfile
```

-	Layers:
	-	`sha256:cd2b2b371aebdde7ebd816cdfb3f315f40dc26d1977eea06a856520460c51ba5`  
		Last Modified: Mon, 16 Mar 2026 23:40:04 GMT  
		Size: 6.7 MB (6666958 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eaf36f9d988856ec2516a934923e86fba5aba63b99b6cac8c1fae60aa71d22ee`  
		Last Modified: Mon, 16 Mar 2026 23:40:03 GMT  
		Size: 14.4 KB (14427 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.37.3` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:e83d79dd42195c49abb2ce52d3907fc9b207d9635ce382ee66bae2b1418dcbd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.5 MB (158472459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2193d35a4e8c05d5f12aace9161486f1b8311f7aa38cdd7c5413feb416e3f55`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 23:18:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:04:45 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:04:45 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 17 Mar 2026 01:04:53 GMT
ENV TELEGRAF_VERSION=1.37.3
# Tue, 17 Mar 2026 01:04:53 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 17 Mar 2026 01:04:53 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 17 Mar 2026 01:04:53 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:04:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Mar 2026 01:04:53 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:3e574dbe918dfcf76ab4fd7736cc3c62e552f2465f49a512ed26cfc623807024`  
		Last Modified: Mon, 16 Mar 2026 21:56:33 GMT  
		Size: 44.2 MB (44207568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab92577caba10dd52b0a4a93a140b02839815621e1e55d6eef1c846ec1932e81`  
		Last Modified: Mon, 16 Mar 2026 23:18:55 GMT  
		Size: 21.9 MB (21942056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5b00520d158d5f9559c7b13e7b0a4e88c9e7af14132004e9044b23ed699729b`  
		Last Modified: Tue, 17 Mar 2026 01:05:14 GMT  
		Size: 17.7 MB (17699735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f34f19e1d368e90a9ed8be2272d7e68b466bad9e0bc6d63b00d6489130074d8`  
		Last Modified: Tue, 17 Mar 2026 01:05:13 GMT  
		Size: 5.1 KB (5055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24436afcf38fd62dc9370cb940807caea711aa7561469406a8e95e6e777d9de3`  
		Last Modified: Tue, 17 Mar 2026 01:05:15 GMT  
		Size: 74.6 MB (74617420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ba0eef8fb852c9ce7209e1ee8b41651dd190f696c28dd9ac568611f7716400a`  
		Last Modified: Tue, 17 Mar 2026 01:05:13 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.37.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:98249aa6ce2c7d05aaa94a090d0a4cf56fa4eb5f10c98cc360a89bdb6ba45885
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6676071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:735ebaa43504ccd154232936d746d5b90c812ab843f57019e065dbee98de8c95`

```dockerfile
```

-	Layers:
	-	`sha256:edae3da1af807f5a69de75e37750bd9ca1df4eebba417d79d8d3cd3a2d4fa693`  
		Last Modified: Tue, 17 Mar 2026 01:05:13 GMT  
		Size: 6.7 MB (6661555 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae69fdfcbd45f104d597e60703e42deabf25d3466f7f69469677bef6055a724f`  
		Last Modified: Tue, 17 Mar 2026 01:05:13 GMT  
		Size: 14.5 KB (14516 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.37.3` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:e315f9f8a1d08a7f64bc392ca283c064df167d8acb6b59ad6c6f956b1890a244
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.0 MB (163040181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04129d47b908bb1bc7e24cd6b42b4d23d699ba5d2081b39dfa022c05a654e639`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:39:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:44:15 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:44:16 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 16 Mar 2026 23:44:22 GMT
ENV TELEGRAF_VERSION=1.37.3
# Mon, 16 Mar 2026 23:44:22 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 16 Mar 2026 23:44:22 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 16 Mar 2026 23:44:22 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 16 Mar 2026 23:44:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 16 Mar 2026 23:44:22 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:2ea98bb5eec9d02a0d7b59638c683db4e1e749f998a317bc731e9506f8480b12`  
		Last Modified: Mon, 16 Mar 2026 21:52:02 GMT  
		Size: 48.4 MB (48373032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efbce225727d69d170353500d8834770da849cbdcea48de37e492fe14ef880d0`  
		Last Modified: Mon, 16 Mar 2026 22:39:28 GMT  
		Size: 23.6 MB (23604701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f775c25b6076386e8aadb02bbe54f427d15b0df69bc2c922a0622a0edd02377d`  
		Last Modified: Mon, 16 Mar 2026 23:44:40 GMT  
		Size: 18.9 MB (18885751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73037eadef315b9d4ad3acfd4bcff10755d304010d9c9a6c5829cefd40137814`  
		Last Modified: Mon, 16 Mar 2026 23:44:39 GMT  
		Size: 5.1 KB (5073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a505bf10e5a5a9424b1217ceb248f13a5a77fd37ff5fa8d9cb299a211e9fb6d`  
		Last Modified: Mon, 16 Mar 2026 23:44:42 GMT  
		Size: 72.2 MB (72171001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:715d737bb6ea059ec90b850858afb8bbd8e72c833ecde271774f79e256fdc8ad`  
		Last Modified: Mon, 16 Mar 2026 23:44:39 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.37.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:16399fffb3ede1ac2cad6a32a23c2a22b48775eb16eae15828dc99534a0c28f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6682171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3afc75bf908e5acb4477c13bf73b13e30f397487f46da9a85f10cbf99edd942`

```dockerfile
```

-	Layers:
	-	`sha256:4816e5b8cd0fe15e89bb032c1c62236e2abae8eb58151259dd2a128481e17189`  
		Last Modified: Mon, 16 Mar 2026 23:44:40 GMT  
		Size: 6.7 MB (6667634 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b950037ac067bdae0b5dc60e3a6b20661c9c953add2fa9cc1c36a72f7e210bb`  
		Last Modified: Mon, 16 Mar 2026 23:44:39 GMT  
		Size: 14.5 KB (14537 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.37.3-alpine`

```console
$ docker pull telegraf@sha256:a550e63a2efbea4b49596e475f0fcd3b057ff2ab0dfc8102357de289ee342a37
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.37.3-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:fba66fd8b08dc6e56336289fd91c0b9c055b5431b1ac6f0cb3c5b0203b24d450
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.9 MB (86946044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38efb96d204dcce61a2419f13705ddf967966bbf6c20b8dc214d6cd4917df5cc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Mon, 23 Feb 2026 22:13:06 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 23 Feb 2026 22:13:07 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 23 Feb 2026 22:13:15 GMT
ENV TELEGRAF_VERSION=1.37.3
# Mon, 23 Feb 2026 22:13:15 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 23 Feb 2026 22:13:15 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 23 Feb 2026 22:13:15 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 23 Feb 2026 22:13:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Feb 2026 22:13:15 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce2b56c151750e24306076f9157dce93616ec037d271702f125dc64fbf3376f8`  
		Last Modified: Mon, 23 Feb 2026 22:13:30 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aff331311971b9e1b3df00d187242872c6a7167b0fa5eb1b83bf07f57f6bd227`  
		Last Modified: Mon, 23 Feb 2026 22:13:30 GMT  
		Size: 2.6 MB (2563613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:749b176fa3df8ddfa0c79b45cb78b9caf938ca77b7d56b923cdb8d9280c85548`  
		Last Modified: Mon, 23 Feb 2026 22:13:33 GMT  
		Size: 80.6 MB (80576658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3a622797146e400edbb8a20860c8044210bb4ddf360b881dd59f657a0178e56`  
		Last Modified: Mon, 23 Feb 2026 22:13:30 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.37.3-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:dbaf7ed8916c29f7e0e480a7ad699dbc11e6ff21f59b298ac7bc4c687f919ec4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1168683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b161c64ca482da5f21d71566f132f54ee64beb84f28a79454afce77c61e7ad74`

```dockerfile
```

-	Layers:
	-	`sha256:0ad1ed01319ca47cfb93e453ec6fce2996425a3ef91fb812891757a8a27d72c6`  
		Last Modified: Mon, 23 Feb 2026 22:13:30 GMT  
		Size: 1.2 MB (1153465 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:841e3534e20e0f7236187feb211ea64b35f00fbef79dd247d04d44865d348a5d`  
		Last Modified: Mon, 23 Feb 2026 22:13:30 GMT  
		Size: 15.2 KB (15218 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.37.3-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:f27c6f05cce7d68495838dcbbe51d1995f3ba235846d6753718f5b2cd8a7f603
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.7 MB (78730556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5048f1f9cdf423929349c19bb659110cd4c7e1ab38dff7597763063c5a1978b3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Mon, 23 Feb 2026 22:12:02 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 23 Feb 2026 22:12:04 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 23 Feb 2026 22:12:09 GMT
ENV TELEGRAF_VERSION=1.37.3
# Mon, 23 Feb 2026 22:12:09 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 23 Feb 2026 22:12:09 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 23 Feb 2026 22:12:09 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 23 Feb 2026 22:12:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Feb 2026 22:12:09 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f365fa2017a849f86d84f3f3776e527b8ff2fb4628dfa52b2e2726747ba9a5f`  
		Last Modified: Mon, 23 Feb 2026 22:12:22 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01dde69daba6471771a33e89fc18e2ef827eac0bbebbfa518372b5614a4c5072`  
		Last Modified: Mon, 23 Feb 2026 22:12:23 GMT  
		Size: 2.6 MB (2627610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83fb53f42b0075065a38f3acdda1775b06ee78f844307d7125a10b6688253f62`  
		Last Modified: Mon, 23 Feb 2026 22:12:24 GMT  
		Size: 72.0 MB (71962529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d896748b58358906c78fda48ddade4bd1df0e660097580f49b6f08d0bb041131`  
		Last Modified: Mon, 23 Feb 2026 22:12:22 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.37.3-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:f2ad750ecb35ac8a316aa4496da66885dfc42a651a503859707823f2d6f4ca2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1164446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9b3b3372362c4275569df86547f57711280021d198691725283f623157d5487`

```dockerfile
```

-	Layers:
	-	`sha256:84a7770deb78578c6e010d0e4268d870b145b32e787666e68441fd2377878852`  
		Last Modified: Mon, 23 Feb 2026 22:12:22 GMT  
		Size: 1.1 MB (1149104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b83295c00d09abd5a3a9c39ebd649a814a4169ff62cc5041580c6c7c1bfd6e5`  
		Last Modified: Mon, 23 Feb 2026 22:12:23 GMT  
		Size: 15.3 KB (15342 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.38`

```console
$ docker pull telegraf@sha256:4f76b2c36e9e6b555380c6fbcedb42bcda548185f8d9ceb4efbba7f1e0cdf475
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.38` - linux; amd64

```console
$ docker pull telegraf@sha256:18c293477252eb10b9d35a1ed3831634e79c609e66fd69c15751c162a30cf50d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.0 MB (172992094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53d3643190c0feb9f916016c9e7cee7ea67a625d1b28dafda4646810621dd708`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:37:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 30 Mar 2026 20:22:47 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 30 Mar 2026 20:22:48 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 30 Mar 2026 20:22:54 GMT
ENV TELEGRAF_VERSION=1.38.2
# Mon, 30 Mar 2026 20:22:54 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 30 Mar 2026 20:22:54 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 30 Mar 2026 20:22:54 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 30 Mar 2026 20:22:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 30 Mar 2026 20:22:54 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:9d2f29087bcd6d99efd909a99095549425cd63e27c71b3bf37f108c6b7c370f9`  
		Last Modified: Mon, 16 Mar 2026 21:52:42 GMT  
		Size: 48.5 MB (48488584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26fa3468d221545a43d2151f3977695a31857f9342ba842627d03c9fa1b2ae02`  
		Last Modified: Mon, 16 Mar 2026 22:37:09 GMT  
		Size: 24.0 MB (24038304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a2802c1b18862a0c00d5f61f64946870863fd4ac01ff7f395169525b46062f2`  
		Last Modified: Mon, 30 Mar 2026 20:23:14 GMT  
		Size: 18.9 MB (18944401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60ae4edaa1d0dc6938f93db74e6ccd4f10d2cf14cd026a59cf4b6649c9703123`  
		Last Modified: Mon, 30 Mar 2026 20:23:14 GMT  
		Size: 5.1 KB (5072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ade8961808d26832ee1dd01e35fac2d0282285a3ee378eb19352e5a211d1c9af`  
		Last Modified: Mon, 30 Mar 2026 20:23:16 GMT  
		Size: 81.5 MB (81515110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8dba2360cb8d06267f4391125a907449ee23717932e1523a9a7abbbe150e174`  
		Last Modified: Mon, 30 Mar 2026 20:23:14 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.38` - unknown; unknown

```console
$ docker pull telegraf@sha256:b2fb4e9ea6e75719bdbd49892a0e141fdfe7e2d0ed51c007146fad2715e76211
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6690035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e025858ff553b954359d2f13b12120ec66fcb1c222d75d001b4c4f8543189ccb`

```dockerfile
```

-	Layers:
	-	`sha256:aabab540249895ff4d542e9b58b572d37609e97a0b3cf4b564ed635b24af185c`  
		Last Modified: Mon, 30 Mar 2026 20:23:14 GMT  
		Size: 6.7 MB (6675306 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:173d4134f29c160900cdae79581079d6b6ba2b7ac63c9d4abe3aa44ab02ec1bd`  
		Last Modified: Mon, 30 Mar 2026 20:23:13 GMT  
		Size: 14.7 KB (14729 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.38` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:80a491f1d4adef2864eae4163b35525834dfc57dbaaf82d8b1ab0e018374a4a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.2 MB (159178721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f13bfde9e7b55215e0b80e6dedfbf4d9579e1b1037bad7182525efeb6510aa17`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 23:18:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 30 Mar 2026 20:19:51 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 30 Mar 2026 20:19:52 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 30 Mar 2026 20:19:59 GMT
ENV TELEGRAF_VERSION=1.38.2
# Mon, 30 Mar 2026 20:19:59 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 30 Mar 2026 20:19:59 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 30 Mar 2026 20:19:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 30 Mar 2026 20:19:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 30 Mar 2026 20:19:59 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:3e574dbe918dfcf76ab4fd7736cc3c62e552f2465f49a512ed26cfc623807024`  
		Last Modified: Mon, 16 Mar 2026 21:56:33 GMT  
		Size: 44.2 MB (44207568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab92577caba10dd52b0a4a93a140b02839815621e1e55d6eef1c846ec1932e81`  
		Last Modified: Mon, 16 Mar 2026 23:18:55 GMT  
		Size: 21.9 MB (21942056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83e8b34cc1818a00a1f7f8e2b5b38d6d7b71d2de8e1aa890c1d50ec3802a0656`  
		Last Modified: Mon, 30 Mar 2026 20:20:16 GMT  
		Size: 17.7 MB (17699834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0785fde20f5095bb7d265e70fa8fbcc58decfcab32632a6d9a4fc530a6a93a58`  
		Last Modified: Mon, 30 Mar 2026 20:20:16 GMT  
		Size: 5.1 KB (5054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfbe836590747c932d3cf9d4e242a660920c2a105435a4089aa1e2eecaa53eee`  
		Last Modified: Mon, 30 Mar 2026 20:20:18 GMT  
		Size: 75.3 MB (75323583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1271469821cf393f614409dcfa5d1687789c67e4234176866601ea788a4fd07`  
		Last Modified: Mon, 30 Mar 2026 20:20:16 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.38` - unknown; unknown

```console
$ docker pull telegraf@sha256:284319d72e82cce4028c10a69309c431e6853996656f3009a94a03a0cbd969ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6684736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8f379fe115f68207eaf2e7d9abc7461267273420d14cef78380ac501cb35009`

```dockerfile
```

-	Layers:
	-	`sha256:3ad35c9bf3b2badfb4cb0986d7460795c4757e9b2c813c6cc5ca04194454f6e3`  
		Last Modified: Mon, 30 Mar 2026 20:20:16 GMT  
		Size: 6.7 MB (6669911 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48dfc4a13e5ee43285586d2ac330d6b072a26c4e6e5f3cc8909551d8d2432ef8`  
		Last Modified: Mon, 30 Mar 2026 20:20:16 GMT  
		Size: 14.8 KB (14825 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.38` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:1cdf684c6b95ea71da37a32b4cbe8804aaaeb4f4cc7fb6f2342d2ee3118b4a6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.7 MB (163723816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebe0cd13648c1047fc5d8e35cfed87d77f8e9e467d2dc1328f1658ac27c897cf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:39:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 30 Mar 2026 20:23:03 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 30 Mar 2026 20:23:03 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 30 Mar 2026 20:23:09 GMT
ENV TELEGRAF_VERSION=1.38.2
# Mon, 30 Mar 2026 20:23:09 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 30 Mar 2026 20:23:09 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 30 Mar 2026 20:23:09 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 30 Mar 2026 20:23:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 30 Mar 2026 20:23:09 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:2ea98bb5eec9d02a0d7b59638c683db4e1e749f998a317bc731e9506f8480b12`  
		Last Modified: Mon, 16 Mar 2026 21:52:02 GMT  
		Size: 48.4 MB (48373032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efbce225727d69d170353500d8834770da849cbdcea48de37e492fe14ef880d0`  
		Last Modified: Mon, 16 Mar 2026 22:39:28 GMT  
		Size: 23.6 MB (23604701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dea57c7ce06fc0e1ab8e223ca992732c9235caa493c98081cbad02eb17ab3a0`  
		Last Modified: Mon, 30 Mar 2026 20:23:27 GMT  
		Size: 18.9 MB (18885814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4321db48e7d56bb2e430a5bfc6ef2c2bf97d35b29572de0246d82b0f5a33599f`  
		Last Modified: Mon, 30 Mar 2026 20:23:26 GMT  
		Size: 5.1 KB (5058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e5fa588be7b3ff775dd732895adccefd60773a8e2fa567b7022426ec3bab55`  
		Last Modified: Mon, 30 Mar 2026 20:23:29 GMT  
		Size: 72.9 MB (72854586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f0a3464c83b3f375a08bacfeac148c3a50f545b42f4b6f2efe09754bf674aa8`  
		Last Modified: Mon, 30 Mar 2026 20:23:26 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.38` - unknown; unknown

```console
$ docker pull telegraf@sha256:08786c217762a0eb08562be2dde68c7cfe3521c27e34b65d298fb1360ef083bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6690845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d41412b55a9486e55b68bf0bb5c2d9986ba82254eaa161cf7981de690ce2ee9`

```dockerfile
```

-	Layers:
	-	`sha256:4579fa8a646c3f412dcb970e84de25d94f1817ebc5980b985f2eff7d616f0898`  
		Last Modified: Mon, 30 Mar 2026 20:23:27 GMT  
		Size: 6.7 MB (6675994 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6ba9e3a3c5a9e23da8dc68dd2c319e8b2eb3f7d8596e64850d9a1b987f40ba4`  
		Last Modified: Mon, 30 Mar 2026 20:23:26 GMT  
		Size: 14.9 KB (14851 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.38-alpine`

```console
$ docker pull telegraf@sha256:811335001118729cd2bdbcf0aaa88fae62102ab85745bf5f4a0ed60cba56de4e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.38-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:15c787ed509753ff1c98af9c858bc4e79a8838e2f97f9da94808690f237954a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.7 MB (87671535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11d74b6eeb9d11ffd3cf0526e2dfd611c3f1a047bee5ab27f89f68f30cce3a66`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Mon, 30 Mar 2026 20:22:43 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 30 Mar 2026 20:22:44 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 30 Mar 2026 20:22:52 GMT
ENV TELEGRAF_VERSION=1.38.2
# Mon, 30 Mar 2026 20:22:52 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 30 Mar 2026 20:22:52 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 30 Mar 2026 20:22:52 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 30 Mar 2026 20:22:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 30 Mar 2026 20:22:52 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7f3ac74f06ef64597e0008d5b58e2d631cbc2a1c7c8d7827de7f6084ffd1384`  
		Last Modified: Mon, 30 Mar 2026 20:23:07 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:841b2cba4b94e9cabe8821efc5c269224dc910b9f66659d5a0118790408f9f64`  
		Last Modified: Mon, 30 Mar 2026 20:23:08 GMT  
		Size: 2.6 MB (2563409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22318848ab211de8fbcfbd33472f3c9a9f45e5bf40b3964fd587be331ef0cfff`  
		Last Modified: Mon, 30 Mar 2026 20:23:10 GMT  
		Size: 81.3 MB (81302351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1f3b3d70a34cca73560581366bf1aa5a7a571294392984eb390146e1a80a300`  
		Last Modified: Mon, 30 Mar 2026 20:23:07 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.38-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:c45de09e7ba9157e9b403a2dd99453df7bee97206572dabc5092a953691be95a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1176730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d03720b29716f6c0b29dbdaaee3000ef67a64556f9a2281d4cac081d6d996656`

```dockerfile
```

-	Layers:
	-	`sha256:98f0364ff7dd919bdcd1b7b1403d67ffa52a2b0edc4c62886b0e5011b3d3fc09`  
		Last Modified: Mon, 30 Mar 2026 20:23:07 GMT  
		Size: 1.2 MB (1161511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ee92bd2e1843be3aaa75cc44cd91b73eaba636edd0cc70546201ffdd09dd9d0`  
		Last Modified: Mon, 30 Mar 2026 20:23:07 GMT  
		Size: 15.2 KB (15219 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.38-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:fb0afd49cd58018b245cea4961f220c244fc777aa1ca0753135afd7c1f59a630
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.4 MB (79408705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcc70a72097954c4dd9b3106a74912f37b0a24e864006c9d69d2d1dcbbde7e87`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Mon, 30 Mar 2026 20:23:00 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 30 Mar 2026 20:23:01 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 30 Mar 2026 20:23:09 GMT
ENV TELEGRAF_VERSION=1.38.2
# Mon, 30 Mar 2026 20:23:09 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 30 Mar 2026 20:23:09 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 30 Mar 2026 20:23:09 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 30 Mar 2026 20:23:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 30 Mar 2026 20:23:09 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:929ce7d3c4f4050324790939845bf90248d29e90794fd46af445c1b82fa8e3ea`  
		Last Modified: Mon, 30 Mar 2026 20:23:23 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2376aa1e3858066a43b2936816204d70c2b668fa25a029d43112bb6fde89fc0e`  
		Last Modified: Mon, 30 Mar 2026 20:23:23 GMT  
		Size: 2.6 MB (2627416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:572e1b4bba075fe67f8adfc96feb476ce9866df13a73405592fb7efc167a67a3`  
		Last Modified: Mon, 30 Mar 2026 20:23:25 GMT  
		Size: 72.6 MB (72640871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03b84aaa694985c4eda65e869bf5da5464e1a8a2d08ceb445751e354912483b0`  
		Last Modified: Mon, 30 Mar 2026 20:23:23 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.38-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:936b6b08489b822579b383270e0805734d6dfceff3312eb28064c847078d400e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1172492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97cf381f8dcb2b3c9f182fa9c1b572003933f561a664db9074cf1c6ae7afb654`

```dockerfile
```

-	Layers:
	-	`sha256:4a8a6a2dc5feb376c8b91acda685d81ccc02f798d46c259afc3890bbe6e1601d`  
		Last Modified: Mon, 30 Mar 2026 20:23:23 GMT  
		Size: 1.2 MB (1157150 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:020ec74ea2d5779e6a975977b3f564113afe329c270a94159417df24fb421131`  
		Last Modified: Mon, 30 Mar 2026 20:23:23 GMT  
		Size: 15.3 KB (15342 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.38.2`

```console
$ docker pull telegraf@sha256:4f76b2c36e9e6b555380c6fbcedb42bcda548185f8d9ceb4efbba7f1e0cdf475
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.38.2` - linux; amd64

```console
$ docker pull telegraf@sha256:18c293477252eb10b9d35a1ed3831634e79c609e66fd69c15751c162a30cf50d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.0 MB (172992094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53d3643190c0feb9f916016c9e7cee7ea67a625d1b28dafda4646810621dd708`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:37:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 30 Mar 2026 20:22:47 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 30 Mar 2026 20:22:48 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 30 Mar 2026 20:22:54 GMT
ENV TELEGRAF_VERSION=1.38.2
# Mon, 30 Mar 2026 20:22:54 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 30 Mar 2026 20:22:54 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 30 Mar 2026 20:22:54 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 30 Mar 2026 20:22:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 30 Mar 2026 20:22:54 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:9d2f29087bcd6d99efd909a99095549425cd63e27c71b3bf37f108c6b7c370f9`  
		Last Modified: Mon, 16 Mar 2026 21:52:42 GMT  
		Size: 48.5 MB (48488584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26fa3468d221545a43d2151f3977695a31857f9342ba842627d03c9fa1b2ae02`  
		Last Modified: Mon, 16 Mar 2026 22:37:09 GMT  
		Size: 24.0 MB (24038304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a2802c1b18862a0c00d5f61f64946870863fd4ac01ff7f395169525b46062f2`  
		Last Modified: Mon, 30 Mar 2026 20:23:14 GMT  
		Size: 18.9 MB (18944401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60ae4edaa1d0dc6938f93db74e6ccd4f10d2cf14cd026a59cf4b6649c9703123`  
		Last Modified: Mon, 30 Mar 2026 20:23:14 GMT  
		Size: 5.1 KB (5072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ade8961808d26832ee1dd01e35fac2d0282285a3ee378eb19352e5a211d1c9af`  
		Last Modified: Mon, 30 Mar 2026 20:23:16 GMT  
		Size: 81.5 MB (81515110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8dba2360cb8d06267f4391125a907449ee23717932e1523a9a7abbbe150e174`  
		Last Modified: Mon, 30 Mar 2026 20:23:14 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.38.2` - unknown; unknown

```console
$ docker pull telegraf@sha256:b2fb4e9ea6e75719bdbd49892a0e141fdfe7e2d0ed51c007146fad2715e76211
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6690035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e025858ff553b954359d2f13b12120ec66fcb1c222d75d001b4c4f8543189ccb`

```dockerfile
```

-	Layers:
	-	`sha256:aabab540249895ff4d542e9b58b572d37609e97a0b3cf4b564ed635b24af185c`  
		Last Modified: Mon, 30 Mar 2026 20:23:14 GMT  
		Size: 6.7 MB (6675306 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:173d4134f29c160900cdae79581079d6b6ba2b7ac63c9d4abe3aa44ab02ec1bd`  
		Last Modified: Mon, 30 Mar 2026 20:23:13 GMT  
		Size: 14.7 KB (14729 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.38.2` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:80a491f1d4adef2864eae4163b35525834dfc57dbaaf82d8b1ab0e018374a4a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.2 MB (159178721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f13bfde9e7b55215e0b80e6dedfbf4d9579e1b1037bad7182525efeb6510aa17`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 23:18:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 30 Mar 2026 20:19:51 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 30 Mar 2026 20:19:52 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 30 Mar 2026 20:19:59 GMT
ENV TELEGRAF_VERSION=1.38.2
# Mon, 30 Mar 2026 20:19:59 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 30 Mar 2026 20:19:59 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 30 Mar 2026 20:19:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 30 Mar 2026 20:19:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 30 Mar 2026 20:19:59 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:3e574dbe918dfcf76ab4fd7736cc3c62e552f2465f49a512ed26cfc623807024`  
		Last Modified: Mon, 16 Mar 2026 21:56:33 GMT  
		Size: 44.2 MB (44207568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab92577caba10dd52b0a4a93a140b02839815621e1e55d6eef1c846ec1932e81`  
		Last Modified: Mon, 16 Mar 2026 23:18:55 GMT  
		Size: 21.9 MB (21942056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83e8b34cc1818a00a1f7f8e2b5b38d6d7b71d2de8e1aa890c1d50ec3802a0656`  
		Last Modified: Mon, 30 Mar 2026 20:20:16 GMT  
		Size: 17.7 MB (17699834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0785fde20f5095bb7d265e70fa8fbcc58decfcab32632a6d9a4fc530a6a93a58`  
		Last Modified: Mon, 30 Mar 2026 20:20:16 GMT  
		Size: 5.1 KB (5054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfbe836590747c932d3cf9d4e242a660920c2a105435a4089aa1e2eecaa53eee`  
		Last Modified: Mon, 30 Mar 2026 20:20:18 GMT  
		Size: 75.3 MB (75323583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1271469821cf393f614409dcfa5d1687789c67e4234176866601ea788a4fd07`  
		Last Modified: Mon, 30 Mar 2026 20:20:16 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.38.2` - unknown; unknown

```console
$ docker pull telegraf@sha256:284319d72e82cce4028c10a69309c431e6853996656f3009a94a03a0cbd969ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6684736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8f379fe115f68207eaf2e7d9abc7461267273420d14cef78380ac501cb35009`

```dockerfile
```

-	Layers:
	-	`sha256:3ad35c9bf3b2badfb4cb0986d7460795c4757e9b2c813c6cc5ca04194454f6e3`  
		Last Modified: Mon, 30 Mar 2026 20:20:16 GMT  
		Size: 6.7 MB (6669911 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48dfc4a13e5ee43285586d2ac330d6b072a26c4e6e5f3cc8909551d8d2432ef8`  
		Last Modified: Mon, 30 Mar 2026 20:20:16 GMT  
		Size: 14.8 KB (14825 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.38.2` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:1cdf684c6b95ea71da37a32b4cbe8804aaaeb4f4cc7fb6f2342d2ee3118b4a6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.7 MB (163723816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebe0cd13648c1047fc5d8e35cfed87d77f8e9e467d2dc1328f1658ac27c897cf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:39:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 30 Mar 2026 20:23:03 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 30 Mar 2026 20:23:03 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 30 Mar 2026 20:23:09 GMT
ENV TELEGRAF_VERSION=1.38.2
# Mon, 30 Mar 2026 20:23:09 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 30 Mar 2026 20:23:09 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 30 Mar 2026 20:23:09 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 30 Mar 2026 20:23:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 30 Mar 2026 20:23:09 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:2ea98bb5eec9d02a0d7b59638c683db4e1e749f998a317bc731e9506f8480b12`  
		Last Modified: Mon, 16 Mar 2026 21:52:02 GMT  
		Size: 48.4 MB (48373032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efbce225727d69d170353500d8834770da849cbdcea48de37e492fe14ef880d0`  
		Last Modified: Mon, 16 Mar 2026 22:39:28 GMT  
		Size: 23.6 MB (23604701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dea57c7ce06fc0e1ab8e223ca992732c9235caa493c98081cbad02eb17ab3a0`  
		Last Modified: Mon, 30 Mar 2026 20:23:27 GMT  
		Size: 18.9 MB (18885814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4321db48e7d56bb2e430a5bfc6ef2c2bf97d35b29572de0246d82b0f5a33599f`  
		Last Modified: Mon, 30 Mar 2026 20:23:26 GMT  
		Size: 5.1 KB (5058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e5fa588be7b3ff775dd732895adccefd60773a8e2fa567b7022426ec3bab55`  
		Last Modified: Mon, 30 Mar 2026 20:23:29 GMT  
		Size: 72.9 MB (72854586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f0a3464c83b3f375a08bacfeac148c3a50f545b42f4b6f2efe09754bf674aa8`  
		Last Modified: Mon, 30 Mar 2026 20:23:26 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.38.2` - unknown; unknown

```console
$ docker pull telegraf@sha256:08786c217762a0eb08562be2dde68c7cfe3521c27e34b65d298fb1360ef083bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6690845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d41412b55a9486e55b68bf0bb5c2d9986ba82254eaa161cf7981de690ce2ee9`

```dockerfile
```

-	Layers:
	-	`sha256:4579fa8a646c3f412dcb970e84de25d94f1817ebc5980b985f2eff7d616f0898`  
		Last Modified: Mon, 30 Mar 2026 20:23:27 GMT  
		Size: 6.7 MB (6675994 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6ba9e3a3c5a9e23da8dc68dd2c319e8b2eb3f7d8596e64850d9a1b987f40ba4`  
		Last Modified: Mon, 30 Mar 2026 20:23:26 GMT  
		Size: 14.9 KB (14851 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.38.2-alpine`

```console
$ docker pull telegraf@sha256:811335001118729cd2bdbcf0aaa88fae62102ab85745bf5f4a0ed60cba56de4e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.38.2-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:15c787ed509753ff1c98af9c858bc4e79a8838e2f97f9da94808690f237954a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.7 MB (87671535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11d74b6eeb9d11ffd3cf0526e2dfd611c3f1a047bee5ab27f89f68f30cce3a66`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Mon, 30 Mar 2026 20:22:43 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 30 Mar 2026 20:22:44 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 30 Mar 2026 20:22:52 GMT
ENV TELEGRAF_VERSION=1.38.2
# Mon, 30 Mar 2026 20:22:52 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 30 Mar 2026 20:22:52 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 30 Mar 2026 20:22:52 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 30 Mar 2026 20:22:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 30 Mar 2026 20:22:52 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7f3ac74f06ef64597e0008d5b58e2d631cbc2a1c7c8d7827de7f6084ffd1384`  
		Last Modified: Mon, 30 Mar 2026 20:23:07 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:841b2cba4b94e9cabe8821efc5c269224dc910b9f66659d5a0118790408f9f64`  
		Last Modified: Mon, 30 Mar 2026 20:23:08 GMT  
		Size: 2.6 MB (2563409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22318848ab211de8fbcfbd33472f3c9a9f45e5bf40b3964fd587be331ef0cfff`  
		Last Modified: Mon, 30 Mar 2026 20:23:10 GMT  
		Size: 81.3 MB (81302351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1f3b3d70a34cca73560581366bf1aa5a7a571294392984eb390146e1a80a300`  
		Last Modified: Mon, 30 Mar 2026 20:23:07 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.38.2-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:c45de09e7ba9157e9b403a2dd99453df7bee97206572dabc5092a953691be95a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1176730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d03720b29716f6c0b29dbdaaee3000ef67a64556f9a2281d4cac081d6d996656`

```dockerfile
```

-	Layers:
	-	`sha256:98f0364ff7dd919bdcd1b7b1403d67ffa52a2b0edc4c62886b0e5011b3d3fc09`  
		Last Modified: Mon, 30 Mar 2026 20:23:07 GMT  
		Size: 1.2 MB (1161511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ee92bd2e1843be3aaa75cc44cd91b73eaba636edd0cc70546201ffdd09dd9d0`  
		Last Modified: Mon, 30 Mar 2026 20:23:07 GMT  
		Size: 15.2 KB (15219 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.38.2-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:fb0afd49cd58018b245cea4961f220c244fc777aa1ca0753135afd7c1f59a630
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.4 MB (79408705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcc70a72097954c4dd9b3106a74912f37b0a24e864006c9d69d2d1dcbbde7e87`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Mon, 30 Mar 2026 20:23:00 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 30 Mar 2026 20:23:01 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 30 Mar 2026 20:23:09 GMT
ENV TELEGRAF_VERSION=1.38.2
# Mon, 30 Mar 2026 20:23:09 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 30 Mar 2026 20:23:09 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 30 Mar 2026 20:23:09 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 30 Mar 2026 20:23:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 30 Mar 2026 20:23:09 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:929ce7d3c4f4050324790939845bf90248d29e90794fd46af445c1b82fa8e3ea`  
		Last Modified: Mon, 30 Mar 2026 20:23:23 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2376aa1e3858066a43b2936816204d70c2b668fa25a029d43112bb6fde89fc0e`  
		Last Modified: Mon, 30 Mar 2026 20:23:23 GMT  
		Size: 2.6 MB (2627416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:572e1b4bba075fe67f8adfc96feb476ce9866df13a73405592fb7efc167a67a3`  
		Last Modified: Mon, 30 Mar 2026 20:23:25 GMT  
		Size: 72.6 MB (72640871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03b84aaa694985c4eda65e869bf5da5464e1a8a2d08ceb445751e354912483b0`  
		Last Modified: Mon, 30 Mar 2026 20:23:23 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.38.2-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:936b6b08489b822579b383270e0805734d6dfceff3312eb28064c847078d400e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1172492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97cf381f8dcb2b3c9f182fa9c1b572003933f561a664db9074cf1c6ae7afb654`

```dockerfile
```

-	Layers:
	-	`sha256:4a8a6a2dc5feb376c8b91acda685d81ccc02f798d46c259afc3890bbe6e1601d`  
		Last Modified: Mon, 30 Mar 2026 20:23:23 GMT  
		Size: 1.2 MB (1157150 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:020ec74ea2d5779e6a975977b3f564113afe329c270a94159417df24fb421131`  
		Last Modified: Mon, 30 Mar 2026 20:23:23 GMT  
		Size: 15.3 KB (15342 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:alpine`

```console
$ docker pull telegraf@sha256:811335001118729cd2bdbcf0aaa88fae62102ab85745bf5f4a0ed60cba56de4e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:15c787ed509753ff1c98af9c858bc4e79a8838e2f97f9da94808690f237954a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.7 MB (87671535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11d74b6eeb9d11ffd3cf0526e2dfd611c3f1a047bee5ab27f89f68f30cce3a66`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Mon, 30 Mar 2026 20:22:43 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 30 Mar 2026 20:22:44 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 30 Mar 2026 20:22:52 GMT
ENV TELEGRAF_VERSION=1.38.2
# Mon, 30 Mar 2026 20:22:52 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 30 Mar 2026 20:22:52 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 30 Mar 2026 20:22:52 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 30 Mar 2026 20:22:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 30 Mar 2026 20:22:52 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7f3ac74f06ef64597e0008d5b58e2d631cbc2a1c7c8d7827de7f6084ffd1384`  
		Last Modified: Mon, 30 Mar 2026 20:23:07 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:841b2cba4b94e9cabe8821efc5c269224dc910b9f66659d5a0118790408f9f64`  
		Last Modified: Mon, 30 Mar 2026 20:23:08 GMT  
		Size: 2.6 MB (2563409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22318848ab211de8fbcfbd33472f3c9a9f45e5bf40b3964fd587be331ef0cfff`  
		Last Modified: Mon, 30 Mar 2026 20:23:10 GMT  
		Size: 81.3 MB (81302351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1f3b3d70a34cca73560581366bf1aa5a7a571294392984eb390146e1a80a300`  
		Last Modified: Mon, 30 Mar 2026 20:23:07 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:c45de09e7ba9157e9b403a2dd99453df7bee97206572dabc5092a953691be95a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1176730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d03720b29716f6c0b29dbdaaee3000ef67a64556f9a2281d4cac081d6d996656`

```dockerfile
```

-	Layers:
	-	`sha256:98f0364ff7dd919bdcd1b7b1403d67ffa52a2b0edc4c62886b0e5011b3d3fc09`  
		Last Modified: Mon, 30 Mar 2026 20:23:07 GMT  
		Size: 1.2 MB (1161511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ee92bd2e1843be3aaa75cc44cd91b73eaba636edd0cc70546201ffdd09dd9d0`  
		Last Modified: Mon, 30 Mar 2026 20:23:07 GMT  
		Size: 15.2 KB (15219 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:fb0afd49cd58018b245cea4961f220c244fc777aa1ca0753135afd7c1f59a630
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.4 MB (79408705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcc70a72097954c4dd9b3106a74912f37b0a24e864006c9d69d2d1dcbbde7e87`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Mon, 30 Mar 2026 20:23:00 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 30 Mar 2026 20:23:01 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 30 Mar 2026 20:23:09 GMT
ENV TELEGRAF_VERSION=1.38.2
# Mon, 30 Mar 2026 20:23:09 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 30 Mar 2026 20:23:09 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 30 Mar 2026 20:23:09 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 30 Mar 2026 20:23:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 30 Mar 2026 20:23:09 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:929ce7d3c4f4050324790939845bf90248d29e90794fd46af445c1b82fa8e3ea`  
		Last Modified: Mon, 30 Mar 2026 20:23:23 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2376aa1e3858066a43b2936816204d70c2b668fa25a029d43112bb6fde89fc0e`  
		Last Modified: Mon, 30 Mar 2026 20:23:23 GMT  
		Size: 2.6 MB (2627416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:572e1b4bba075fe67f8adfc96feb476ce9866df13a73405592fb7efc167a67a3`  
		Last Modified: Mon, 30 Mar 2026 20:23:25 GMT  
		Size: 72.6 MB (72640871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03b84aaa694985c4eda65e869bf5da5464e1a8a2d08ceb445751e354912483b0`  
		Last Modified: Mon, 30 Mar 2026 20:23:23 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:936b6b08489b822579b383270e0805734d6dfceff3312eb28064c847078d400e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1172492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97cf381f8dcb2b3c9f182fa9c1b572003933f561a664db9074cf1c6ae7afb654`

```dockerfile
```

-	Layers:
	-	`sha256:4a8a6a2dc5feb376c8b91acda685d81ccc02f798d46c259afc3890bbe6e1601d`  
		Last Modified: Mon, 30 Mar 2026 20:23:23 GMT  
		Size: 1.2 MB (1157150 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:020ec74ea2d5779e6a975977b3f564113afe329c270a94159417df24fb421131`  
		Last Modified: Mon, 30 Mar 2026 20:23:23 GMT  
		Size: 15.3 KB (15342 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:latest`

```console
$ docker pull telegraf@sha256:4f76b2c36e9e6b555380c6fbcedb42bcda548185f8d9ceb4efbba7f1e0cdf475
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:latest` - linux; amd64

```console
$ docker pull telegraf@sha256:18c293477252eb10b9d35a1ed3831634e79c609e66fd69c15751c162a30cf50d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.0 MB (172992094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53d3643190c0feb9f916016c9e7cee7ea67a625d1b28dafda4646810621dd708`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:37:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 30 Mar 2026 20:22:47 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 30 Mar 2026 20:22:48 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 30 Mar 2026 20:22:54 GMT
ENV TELEGRAF_VERSION=1.38.2
# Mon, 30 Mar 2026 20:22:54 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 30 Mar 2026 20:22:54 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 30 Mar 2026 20:22:54 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 30 Mar 2026 20:22:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 30 Mar 2026 20:22:54 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:9d2f29087bcd6d99efd909a99095549425cd63e27c71b3bf37f108c6b7c370f9`  
		Last Modified: Mon, 16 Mar 2026 21:52:42 GMT  
		Size: 48.5 MB (48488584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26fa3468d221545a43d2151f3977695a31857f9342ba842627d03c9fa1b2ae02`  
		Last Modified: Mon, 16 Mar 2026 22:37:09 GMT  
		Size: 24.0 MB (24038304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a2802c1b18862a0c00d5f61f64946870863fd4ac01ff7f395169525b46062f2`  
		Last Modified: Mon, 30 Mar 2026 20:23:14 GMT  
		Size: 18.9 MB (18944401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60ae4edaa1d0dc6938f93db74e6ccd4f10d2cf14cd026a59cf4b6649c9703123`  
		Last Modified: Mon, 30 Mar 2026 20:23:14 GMT  
		Size: 5.1 KB (5072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ade8961808d26832ee1dd01e35fac2d0282285a3ee378eb19352e5a211d1c9af`  
		Last Modified: Mon, 30 Mar 2026 20:23:16 GMT  
		Size: 81.5 MB (81515110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8dba2360cb8d06267f4391125a907449ee23717932e1523a9a7abbbe150e174`  
		Last Modified: Mon, 30 Mar 2026 20:23:14 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:b2fb4e9ea6e75719bdbd49892a0e141fdfe7e2d0ed51c007146fad2715e76211
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6690035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e025858ff553b954359d2f13b12120ec66fcb1c222d75d001b4c4f8543189ccb`

```dockerfile
```

-	Layers:
	-	`sha256:aabab540249895ff4d542e9b58b572d37609e97a0b3cf4b564ed635b24af185c`  
		Last Modified: Mon, 30 Mar 2026 20:23:14 GMT  
		Size: 6.7 MB (6675306 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:173d4134f29c160900cdae79581079d6b6ba2b7ac63c9d4abe3aa44ab02ec1bd`  
		Last Modified: Mon, 30 Mar 2026 20:23:13 GMT  
		Size: 14.7 KB (14729 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:80a491f1d4adef2864eae4163b35525834dfc57dbaaf82d8b1ab0e018374a4a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.2 MB (159178721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f13bfde9e7b55215e0b80e6dedfbf4d9579e1b1037bad7182525efeb6510aa17`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 23:18:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 30 Mar 2026 20:19:51 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 30 Mar 2026 20:19:52 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 30 Mar 2026 20:19:59 GMT
ENV TELEGRAF_VERSION=1.38.2
# Mon, 30 Mar 2026 20:19:59 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 30 Mar 2026 20:19:59 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 30 Mar 2026 20:19:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 30 Mar 2026 20:19:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 30 Mar 2026 20:19:59 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:3e574dbe918dfcf76ab4fd7736cc3c62e552f2465f49a512ed26cfc623807024`  
		Last Modified: Mon, 16 Mar 2026 21:56:33 GMT  
		Size: 44.2 MB (44207568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab92577caba10dd52b0a4a93a140b02839815621e1e55d6eef1c846ec1932e81`  
		Last Modified: Mon, 16 Mar 2026 23:18:55 GMT  
		Size: 21.9 MB (21942056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83e8b34cc1818a00a1f7f8e2b5b38d6d7b71d2de8e1aa890c1d50ec3802a0656`  
		Last Modified: Mon, 30 Mar 2026 20:20:16 GMT  
		Size: 17.7 MB (17699834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0785fde20f5095bb7d265e70fa8fbcc58decfcab32632a6d9a4fc530a6a93a58`  
		Last Modified: Mon, 30 Mar 2026 20:20:16 GMT  
		Size: 5.1 KB (5054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfbe836590747c932d3cf9d4e242a660920c2a105435a4089aa1e2eecaa53eee`  
		Last Modified: Mon, 30 Mar 2026 20:20:18 GMT  
		Size: 75.3 MB (75323583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1271469821cf393f614409dcfa5d1687789c67e4234176866601ea788a4fd07`  
		Last Modified: Mon, 30 Mar 2026 20:20:16 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:284319d72e82cce4028c10a69309c431e6853996656f3009a94a03a0cbd969ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6684736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8f379fe115f68207eaf2e7d9abc7461267273420d14cef78380ac501cb35009`

```dockerfile
```

-	Layers:
	-	`sha256:3ad35c9bf3b2badfb4cb0986d7460795c4757e9b2c813c6cc5ca04194454f6e3`  
		Last Modified: Mon, 30 Mar 2026 20:20:16 GMT  
		Size: 6.7 MB (6669911 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48dfc4a13e5ee43285586d2ac330d6b072a26c4e6e5f3cc8909551d8d2432ef8`  
		Last Modified: Mon, 30 Mar 2026 20:20:16 GMT  
		Size: 14.8 KB (14825 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:1cdf684c6b95ea71da37a32b4cbe8804aaaeb4f4cc7fb6f2342d2ee3118b4a6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.7 MB (163723816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebe0cd13648c1047fc5d8e35cfed87d77f8e9e467d2dc1328f1658ac27c897cf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:39:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 30 Mar 2026 20:23:03 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 30 Mar 2026 20:23:03 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 30 Mar 2026 20:23:09 GMT
ENV TELEGRAF_VERSION=1.38.2
# Mon, 30 Mar 2026 20:23:09 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 30 Mar 2026 20:23:09 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 30 Mar 2026 20:23:09 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 30 Mar 2026 20:23:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 30 Mar 2026 20:23:09 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:2ea98bb5eec9d02a0d7b59638c683db4e1e749f998a317bc731e9506f8480b12`  
		Last Modified: Mon, 16 Mar 2026 21:52:02 GMT  
		Size: 48.4 MB (48373032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efbce225727d69d170353500d8834770da849cbdcea48de37e492fe14ef880d0`  
		Last Modified: Mon, 16 Mar 2026 22:39:28 GMT  
		Size: 23.6 MB (23604701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dea57c7ce06fc0e1ab8e223ca992732c9235caa493c98081cbad02eb17ab3a0`  
		Last Modified: Mon, 30 Mar 2026 20:23:27 GMT  
		Size: 18.9 MB (18885814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4321db48e7d56bb2e430a5bfc6ef2c2bf97d35b29572de0246d82b0f5a33599f`  
		Last Modified: Mon, 30 Mar 2026 20:23:26 GMT  
		Size: 5.1 KB (5058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e5fa588be7b3ff775dd732895adccefd60773a8e2fa567b7022426ec3bab55`  
		Last Modified: Mon, 30 Mar 2026 20:23:29 GMT  
		Size: 72.9 MB (72854586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f0a3464c83b3f375a08bacfeac148c3a50f545b42f4b6f2efe09754bf674aa8`  
		Last Modified: Mon, 30 Mar 2026 20:23:26 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:08786c217762a0eb08562be2dde68c7cfe3521c27e34b65d298fb1360ef083bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6690845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d41412b55a9486e55b68bf0bb5c2d9986ba82254eaa161cf7981de690ce2ee9`

```dockerfile
```

-	Layers:
	-	`sha256:4579fa8a646c3f412dcb970e84de25d94f1817ebc5980b985f2eff7d616f0898`  
		Last Modified: Mon, 30 Mar 2026 20:23:27 GMT  
		Size: 6.7 MB (6675994 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6ba9e3a3c5a9e23da8dc68dd2c319e8b2eb3f7d8596e64850d9a1b987f40ba4`  
		Last Modified: Mon, 30 Mar 2026 20:23:26 GMT  
		Size: 14.9 KB (14851 bytes)  
		MIME: application/vnd.in-toto+json
