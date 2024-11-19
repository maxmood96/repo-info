<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `telegraf`

-	[`telegraf:1.30`](#telegraf130)
-	[`telegraf:1.30-alpine`](#telegraf130-alpine)
-	[`telegraf:1.30.3`](#telegraf1303)
-	[`telegraf:1.30.3-alpine`](#telegraf1303-alpine)
-	[`telegraf:1.31`](#telegraf131)
-	[`telegraf:1.31-alpine`](#telegraf131-alpine)
-	[`telegraf:1.31.3`](#telegraf1313)
-	[`telegraf:1.31.3-alpine`](#telegraf1313-alpine)
-	[`telegraf:1.32`](#telegraf132)
-	[`telegraf:1.32-alpine`](#telegraf132-alpine)
-	[`telegraf:1.32.3`](#telegraf1323)
-	[`telegraf:1.32.3-alpine`](#telegraf1323-alpine)
-	[`telegraf:alpine`](#telegrafalpine)
-	[`telegraf:latest`](#telegraflatest)

## `telegraf:1.30`

```console
$ docker pull telegraf@sha256:9dabd1a91b2c851356c14b5a47f3fe68846c9005f2f28e5a4b8b85decf3e9175
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.30` - linux; amd64

```console
$ docker pull telegraf@sha256:26c993c5f082e6633a79fd083b0b38967de5b24cd930b2d742887d7fa03ddad7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.4 MB (155350936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70b1373ef2b8da66c0cfe9d58ae2e61d6f1280b5528300791a3c29bb4dd86d95`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
ENV TELEGRAF_VERSION=1.30.3
# Mon, 28 Oct 2024 22:11:39 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 28 Oct 2024 22:11:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Oct 2024 22:11:39 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:b2b31b28ee3c96e96195c754f8679f690db4b18e475682d716122016ef056f39`  
		Last Modified: Tue, 12 Nov 2024 00:55:23 GMT  
		Size: 49.6 MB (49575695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3cc7b6f04730c072f8b292917e0d95bb886096a2b2b1781196170965161cd27`  
		Last Modified: Tue, 12 Nov 2024 02:38:12 GMT  
		Size: 24.1 MB (24058346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad4cea0931f00f3874f45e2d5d38a115308f2056139190ff3003741afbfd9e50`  
		Last Modified: Tue, 12 Nov 2024 03:16:41 GMT  
		Size: 18.9 MB (18948068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63fa33d58f88292792c7e2d328aa6fcd59f485dd738b74ffdf7b286d1d2c15de`  
		Last Modified: Tue, 12 Nov 2024 03:16:41 GMT  
		Size: 1.8 KB (1782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c1d1a7d397fc3e016436dc9e2d9d980a917f7472111cd5bc501534cd13cd744`  
		Last Modified: Tue, 12 Nov 2024 03:16:42 GMT  
		Size: 62.8 MB (62766422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c29a82085d128f1e58771860d33ec2473b3296e7251cccdf648d8afd90e08c2d`  
		Last Modified: Tue, 12 Nov 2024 03:16:41 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.30` - unknown; unknown

```console
$ docker pull telegraf@sha256:29a6c70301633a0dc0b108028361cc82003314bac59f9ee49ccbe99011ba9a56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6424853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cbb55846b6b50d56a79b604c3365352499f06e552fc38a818858e5d962c1081`

```dockerfile
```

-	Layers:
	-	`sha256:5ed05627e8f4010ce1ab4ab418e71d38bef57c9ab660078a2e200a0e3c3153df`  
		Last Modified: Tue, 12 Nov 2024 03:16:41 GMT  
		Size: 6.4 MB (6410383 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d28aec7ff055a76b5f12bdd01c1421b47c475df6431955096b5315e2f479c00`  
		Last Modified: Tue, 12 Nov 2024 03:16:41 GMT  
		Size: 14.5 KB (14470 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.30` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:d11b10d7b351b4bd42182715e69cca4b25d230451fd8888ea26bd9caf485a5ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.1 MB (143050971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d6599186a260e8b0083de68faa2787bc6efa7b726fadb6a1ada72305ecb9ce0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
ENV TELEGRAF_VERSION=1.30.3
# Mon, 28 Oct 2024 22:11:39 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 28 Oct 2024 22:11:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Oct 2024 22:11:39 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:46618ec96098836cac7950050ba554a969ebf8e9938d85d5f0d97015d3d25076`  
		Last Modified: Tue, 12 Nov 2024 00:56:14 GMT  
		Size: 45.2 MB (45150563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df9660b2b46aa0c77f5dd078f4e57432faf3dbcda91672b9e3f8c1b7892e0ee2`  
		Last Modified: Tue, 12 Nov 2024 15:59:18 GMT  
		Size: 22.0 MB (21960017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52c1519b04115013f7821f6b8398475148c7865994c7c5de2fb71d5916d5fb2e`  
		Last Modified: Wed, 13 Nov 2024 10:41:21 GMT  
		Size: 17.7 MB (17725323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a1859599b084be651ec09e42d0c7674081d74a573bd8eb676cc088609c1a1ed`  
		Last Modified: Wed, 13 Nov 2024 10:41:21 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fee6d626f779b08de0ab57eb59fa02c95c3a7616c6e4a97dd9bdea4bc37de78b`  
		Last Modified: Wed, 13 Nov 2024 10:41:23 GMT  
		Size: 58.2 MB (58212673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39963093867bf859f3e496714bb1d55f3c91fa4b77e31e2d63e9033f4f50bc68`  
		Last Modified: Wed, 13 Nov 2024 10:41:21 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.30` - unknown; unknown

```console
$ docker pull telegraf@sha256:ac428f9081d476de7e3f7d360bcf0711162cb812da72359c5c6e9b40603787b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6419578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adb06f2040a83751ae0d83c311a5a898c4c8e9ffc624c2b6f805816ea90fdc85`

```dockerfile
```

-	Layers:
	-	`sha256:3f27beb76ecc69497466e4c9cf1043dcba85c26c48d6754df94ef9e1f864b97c`  
		Last Modified: Wed, 13 Nov 2024 10:41:21 GMT  
		Size: 6.4 MB (6405022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7320041d6292fa415dec40ea266adf7ef5447eb76ee6bb2ea292cdb310e7e235`  
		Last Modified: Wed, 13 Nov 2024 10:41:21 GMT  
		Size: 14.6 KB (14556 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.30` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:e5b204d299250f1ba02a946eddb8827d89e7d520c3b5b76382f1760a92f77839
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.2 MB (149181901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91c66cb564dfd0a984281d1fd1e260fbe265fb4e47420b92c8121c0aa2617d5e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
ENV TELEGRAF_VERSION=1.30.3
# Mon, 28 Oct 2024 22:11:39 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 28 Oct 2024 22:11:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Oct 2024 22:11:39 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:1a3f1864ec54b1398987bbe673e93d8b09842ecd51e86ab87d64857b70d188b1`  
		Last Modified: Tue, 12 Nov 2024 00:56:20 GMT  
		Size: 49.6 MB (49587201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:464f864cfaa846fbe1b8a889827404e18374f805d29d77c288a813ae8c4f6d91`  
		Last Modified: Tue, 12 Nov 2024 11:16:03 GMT  
		Size: 23.6 MB (23598253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d5aa793fe0445bc976082730ff6252895e46f7493850ef83f0509f98888fbcd`  
		Last Modified: Wed, 13 Nov 2024 06:19:22 GMT  
		Size: 18.9 MB (18870770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0541e3db3bb997348b43ecd98354da9cfea19cd50420a6ecef282eeb79d54dd`  
		Last Modified: Wed, 13 Nov 2024 06:19:21 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91d6b9dc248722f68fc641ad969574f34414d84fad8fe2db24c0064d2a46a66a`  
		Last Modified: Wed, 13 Nov 2024 06:19:23 GMT  
		Size: 57.1 MB (57123270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8245e5ccad6c53cd0aee8d098bc8b8d85c16b9d8eca036cc3ddb7ee9b2b8e3f1`  
		Last Modified: Wed, 13 Nov 2024 06:19:21 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.30` - unknown; unknown

```console
$ docker pull telegraf@sha256:879797468e7dff72072caf49e903bb32a081f9091d5541bed9491f9fe2aead4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6424886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35bbedf33304ddc9a72fd3a73f22781833d98d204b8de19f0f0a69747e112503`

```dockerfile
```

-	Layers:
	-	`sha256:ffc514b138965b4d7ac2b391a79975fae8354d7fbdc25ab23b846591843e702c`  
		Last Modified: Wed, 13 Nov 2024 06:19:22 GMT  
		Size: 6.4 MB (6410306 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9c87d3c4d6e99ed490cc36d6eb65ec3a3c7ff4a2c0f4c87308aee9f4d267dab`  
		Last Modified: Wed, 13 Nov 2024 06:19:21 GMT  
		Size: 14.6 KB (14580 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.30-alpine`

```console
$ docker pull telegraf@sha256:48b16cd7118777f0f1bfbf1646e1361f86617940bf8be0f78a8f38b38f559d38
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.30-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:d1fe88cff6f1f352b943b18a696b82f02f51b0c6cf6ef6f0f8ac06767c1aba32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.6 MB (68637840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad5e575a5e5a70553ec5d58132072558a1f2a4f93eacf2c851b9e87044e8531d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Mon, 28 Oct 2024 22:11:39 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
ENV TELEGRAF_VERSION=1.30.3
# Mon, 28 Oct 2024 22:11:39 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 28 Oct 2024 22:11:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Oct 2024 22:11:39 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f26c83f64ca1456198e770c389b38e5bf8c9e65836f4618a54a974e411188638`  
		Last Modified: Tue, 12 Nov 2024 02:21:05 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:974bbb85e144ad54cca7dc47f8bb42c769d38b56729a078fe026f811498268fb`  
		Last Modified: Tue, 12 Nov 2024 02:21:05 GMT  
		Size: 2.4 MB (2444834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d45ebb412048f7665bc09f61be06e91c3bba493788205109742894989302ec21`  
		Last Modified: Tue, 12 Nov 2024 02:21:06 GMT  
		Size: 62.6 MB (62568494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c70ab24ace3340ea55807f383962096485bd4b7d97294db29be4974593a11997`  
		Last Modified: Tue, 12 Nov 2024 02:21:05 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.30-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:4d1f2b2431200e7ea650df7ca3503ac7c776c116468c7d8b4c24cd3a1f22191e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1071366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:308834af1822db8b6728b0a622602d025641dc2c956b8ba8ccbdb6b9575572c7`

```dockerfile
```

-	Layers:
	-	`sha256:a39b74605b0de8f0c7dffc4a9341b56a5e25959232ded52dda115dd0da436a6e`  
		Last Modified: Tue, 12 Nov 2024 02:21:05 GMT  
		Size: 1.1 MB (1056405 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4fdfb4fd65fb42e643e34090b6fd02f342d53162daa4374e0ab66ebc5132de74`  
		Last Modified: Tue, 12 Nov 2024 02:21:05 GMT  
		Size: 15.0 KB (14961 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.30-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:aa8942ae1c5553ceac2e04ea1f21939261f63205249a62e2b3c04e3fb7bc14d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63540183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06a25b84a9e7b00a3db8f63063a3158b5d7fa3b6a45e1e7591e1b592c9ebfb4c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Mon, 28 Oct 2024 22:11:39 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
ENV TELEGRAF_VERSION=1.30.3
# Mon, 28 Oct 2024 22:11:39 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 28 Oct 2024 22:11:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Oct 2024 22:11:39 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9de63ce930d0f77f6402e61ee732ad4f784c59fd26df033bb1b7d6a0b87a2f4`  
		Last Modified: Tue, 12 Nov 2024 13:17:18 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:848dadffeaafa841326acf8c33573919df8ff222e2680607f7d10bb804a23d6c`  
		Last Modified: Wed, 13 Nov 2024 00:44:18 GMT  
		Size: 2.5 MB (2530663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fda24d53e12767920ea59e84b53c365e01b3b29f4988df7f2e8a669b5411862`  
		Last Modified: Wed, 13 Nov 2024 00:44:20 GMT  
		Size: 56.9 MB (56921187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8db666f85d9bf6e47b56332381281f973a63eb2e75f216da6c7de966ab6b3ccf`  
		Last Modified: Wed, 13 Nov 2024 00:44:18 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.30-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:8c63a415f442175dc0ac4d407d716e7e15c2839daedbba06a0cf1c5fbba42d70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1066346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f023ae63c182c047e5e162572d71a566b408affba4667ae76c4458764d659e63`

```dockerfile
```

-	Layers:
	-	`sha256:ca8e82b4ad234fde2144ac752875f5f4e2624ca01398237dd917456fa3876a45`  
		Last Modified: Wed, 13 Nov 2024 00:44:18 GMT  
		Size: 1.1 MB (1051275 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e884945c1eedf9b90e6c05f951a12c4509d27fa03085eababc577b6919684f86`  
		Last Modified: Wed, 13 Nov 2024 00:44:18 GMT  
		Size: 15.1 KB (15071 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.30.3`

```console
$ docker pull telegraf@sha256:9dabd1a91b2c851356c14b5a47f3fe68846c9005f2f28e5a4b8b85decf3e9175
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.30.3` - linux; amd64

```console
$ docker pull telegraf@sha256:26c993c5f082e6633a79fd083b0b38967de5b24cd930b2d742887d7fa03ddad7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.4 MB (155350936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70b1373ef2b8da66c0cfe9d58ae2e61d6f1280b5528300791a3c29bb4dd86d95`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
ENV TELEGRAF_VERSION=1.30.3
# Mon, 28 Oct 2024 22:11:39 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 28 Oct 2024 22:11:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Oct 2024 22:11:39 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:b2b31b28ee3c96e96195c754f8679f690db4b18e475682d716122016ef056f39`  
		Last Modified: Tue, 12 Nov 2024 00:55:23 GMT  
		Size: 49.6 MB (49575695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3cc7b6f04730c072f8b292917e0d95bb886096a2b2b1781196170965161cd27`  
		Last Modified: Tue, 12 Nov 2024 02:38:12 GMT  
		Size: 24.1 MB (24058346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad4cea0931f00f3874f45e2d5d38a115308f2056139190ff3003741afbfd9e50`  
		Last Modified: Tue, 12 Nov 2024 03:16:41 GMT  
		Size: 18.9 MB (18948068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63fa33d58f88292792c7e2d328aa6fcd59f485dd738b74ffdf7b286d1d2c15de`  
		Last Modified: Tue, 12 Nov 2024 03:16:41 GMT  
		Size: 1.8 KB (1782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c1d1a7d397fc3e016436dc9e2d9d980a917f7472111cd5bc501534cd13cd744`  
		Last Modified: Tue, 12 Nov 2024 03:16:42 GMT  
		Size: 62.8 MB (62766422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c29a82085d128f1e58771860d33ec2473b3296e7251cccdf648d8afd90e08c2d`  
		Last Modified: Tue, 12 Nov 2024 03:16:41 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.30.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:29a6c70301633a0dc0b108028361cc82003314bac59f9ee49ccbe99011ba9a56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6424853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cbb55846b6b50d56a79b604c3365352499f06e552fc38a818858e5d962c1081`

```dockerfile
```

-	Layers:
	-	`sha256:5ed05627e8f4010ce1ab4ab418e71d38bef57c9ab660078a2e200a0e3c3153df`  
		Last Modified: Tue, 12 Nov 2024 03:16:41 GMT  
		Size: 6.4 MB (6410383 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d28aec7ff055a76b5f12bdd01c1421b47c475df6431955096b5315e2f479c00`  
		Last Modified: Tue, 12 Nov 2024 03:16:41 GMT  
		Size: 14.5 KB (14470 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.30.3` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:d11b10d7b351b4bd42182715e69cca4b25d230451fd8888ea26bd9caf485a5ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.1 MB (143050971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d6599186a260e8b0083de68faa2787bc6efa7b726fadb6a1ada72305ecb9ce0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
ENV TELEGRAF_VERSION=1.30.3
# Mon, 28 Oct 2024 22:11:39 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 28 Oct 2024 22:11:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Oct 2024 22:11:39 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:46618ec96098836cac7950050ba554a969ebf8e9938d85d5f0d97015d3d25076`  
		Last Modified: Tue, 12 Nov 2024 00:56:14 GMT  
		Size: 45.2 MB (45150563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df9660b2b46aa0c77f5dd078f4e57432faf3dbcda91672b9e3f8c1b7892e0ee2`  
		Last Modified: Tue, 12 Nov 2024 15:59:18 GMT  
		Size: 22.0 MB (21960017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52c1519b04115013f7821f6b8398475148c7865994c7c5de2fb71d5916d5fb2e`  
		Last Modified: Wed, 13 Nov 2024 10:41:21 GMT  
		Size: 17.7 MB (17725323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a1859599b084be651ec09e42d0c7674081d74a573bd8eb676cc088609c1a1ed`  
		Last Modified: Wed, 13 Nov 2024 10:41:21 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fee6d626f779b08de0ab57eb59fa02c95c3a7616c6e4a97dd9bdea4bc37de78b`  
		Last Modified: Wed, 13 Nov 2024 10:41:23 GMT  
		Size: 58.2 MB (58212673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39963093867bf859f3e496714bb1d55f3c91fa4b77e31e2d63e9033f4f50bc68`  
		Last Modified: Wed, 13 Nov 2024 10:41:21 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.30.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:ac428f9081d476de7e3f7d360bcf0711162cb812da72359c5c6e9b40603787b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6419578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adb06f2040a83751ae0d83c311a5a898c4c8e9ffc624c2b6f805816ea90fdc85`

```dockerfile
```

-	Layers:
	-	`sha256:3f27beb76ecc69497466e4c9cf1043dcba85c26c48d6754df94ef9e1f864b97c`  
		Last Modified: Wed, 13 Nov 2024 10:41:21 GMT  
		Size: 6.4 MB (6405022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7320041d6292fa415dec40ea266adf7ef5447eb76ee6bb2ea292cdb310e7e235`  
		Last Modified: Wed, 13 Nov 2024 10:41:21 GMT  
		Size: 14.6 KB (14556 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.30.3` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:e5b204d299250f1ba02a946eddb8827d89e7d520c3b5b76382f1760a92f77839
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.2 MB (149181901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91c66cb564dfd0a984281d1fd1e260fbe265fb4e47420b92c8121c0aa2617d5e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
ENV TELEGRAF_VERSION=1.30.3
# Mon, 28 Oct 2024 22:11:39 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 28 Oct 2024 22:11:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Oct 2024 22:11:39 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:1a3f1864ec54b1398987bbe673e93d8b09842ecd51e86ab87d64857b70d188b1`  
		Last Modified: Tue, 12 Nov 2024 00:56:20 GMT  
		Size: 49.6 MB (49587201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:464f864cfaa846fbe1b8a889827404e18374f805d29d77c288a813ae8c4f6d91`  
		Last Modified: Tue, 12 Nov 2024 11:16:03 GMT  
		Size: 23.6 MB (23598253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d5aa793fe0445bc976082730ff6252895e46f7493850ef83f0509f98888fbcd`  
		Last Modified: Wed, 13 Nov 2024 06:19:22 GMT  
		Size: 18.9 MB (18870770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0541e3db3bb997348b43ecd98354da9cfea19cd50420a6ecef282eeb79d54dd`  
		Last Modified: Wed, 13 Nov 2024 06:19:21 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91d6b9dc248722f68fc641ad969574f34414d84fad8fe2db24c0064d2a46a66a`  
		Last Modified: Wed, 13 Nov 2024 06:19:23 GMT  
		Size: 57.1 MB (57123270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8245e5ccad6c53cd0aee8d098bc8b8d85c16b9d8eca036cc3ddb7ee9b2b8e3f1`  
		Last Modified: Wed, 13 Nov 2024 06:19:21 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.30.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:879797468e7dff72072caf49e903bb32a081f9091d5541bed9491f9fe2aead4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6424886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35bbedf33304ddc9a72fd3a73f22781833d98d204b8de19f0f0a69747e112503`

```dockerfile
```

-	Layers:
	-	`sha256:ffc514b138965b4d7ac2b391a79975fae8354d7fbdc25ab23b846591843e702c`  
		Last Modified: Wed, 13 Nov 2024 06:19:22 GMT  
		Size: 6.4 MB (6410306 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9c87d3c4d6e99ed490cc36d6eb65ec3a3c7ff4a2c0f4c87308aee9f4d267dab`  
		Last Modified: Wed, 13 Nov 2024 06:19:21 GMT  
		Size: 14.6 KB (14580 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.30.3-alpine`

```console
$ docker pull telegraf@sha256:48b16cd7118777f0f1bfbf1646e1361f86617940bf8be0f78a8f38b38f559d38
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.30.3-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:d1fe88cff6f1f352b943b18a696b82f02f51b0c6cf6ef6f0f8ac06767c1aba32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.6 MB (68637840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad5e575a5e5a70553ec5d58132072558a1f2a4f93eacf2c851b9e87044e8531d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Mon, 28 Oct 2024 22:11:39 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
ENV TELEGRAF_VERSION=1.30.3
# Mon, 28 Oct 2024 22:11:39 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 28 Oct 2024 22:11:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Oct 2024 22:11:39 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f26c83f64ca1456198e770c389b38e5bf8c9e65836f4618a54a974e411188638`  
		Last Modified: Tue, 12 Nov 2024 02:21:05 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:974bbb85e144ad54cca7dc47f8bb42c769d38b56729a078fe026f811498268fb`  
		Last Modified: Tue, 12 Nov 2024 02:21:05 GMT  
		Size: 2.4 MB (2444834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d45ebb412048f7665bc09f61be06e91c3bba493788205109742894989302ec21`  
		Last Modified: Tue, 12 Nov 2024 02:21:06 GMT  
		Size: 62.6 MB (62568494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c70ab24ace3340ea55807f383962096485bd4b7d97294db29be4974593a11997`  
		Last Modified: Tue, 12 Nov 2024 02:21:05 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.30.3-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:4d1f2b2431200e7ea650df7ca3503ac7c776c116468c7d8b4c24cd3a1f22191e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1071366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:308834af1822db8b6728b0a622602d025641dc2c956b8ba8ccbdb6b9575572c7`

```dockerfile
```

-	Layers:
	-	`sha256:a39b74605b0de8f0c7dffc4a9341b56a5e25959232ded52dda115dd0da436a6e`  
		Last Modified: Tue, 12 Nov 2024 02:21:05 GMT  
		Size: 1.1 MB (1056405 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4fdfb4fd65fb42e643e34090b6fd02f342d53162daa4374e0ab66ebc5132de74`  
		Last Modified: Tue, 12 Nov 2024 02:21:05 GMT  
		Size: 15.0 KB (14961 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.30.3-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:aa8942ae1c5553ceac2e04ea1f21939261f63205249a62e2b3c04e3fb7bc14d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63540183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06a25b84a9e7b00a3db8f63063a3158b5d7fa3b6a45e1e7591e1b592c9ebfb4c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Mon, 28 Oct 2024 22:11:39 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
ENV TELEGRAF_VERSION=1.30.3
# Mon, 28 Oct 2024 22:11:39 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 28 Oct 2024 22:11:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Oct 2024 22:11:39 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9de63ce930d0f77f6402e61ee732ad4f784c59fd26df033bb1b7d6a0b87a2f4`  
		Last Modified: Tue, 12 Nov 2024 13:17:18 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:848dadffeaafa841326acf8c33573919df8ff222e2680607f7d10bb804a23d6c`  
		Last Modified: Wed, 13 Nov 2024 00:44:18 GMT  
		Size: 2.5 MB (2530663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fda24d53e12767920ea59e84b53c365e01b3b29f4988df7f2e8a669b5411862`  
		Last Modified: Wed, 13 Nov 2024 00:44:20 GMT  
		Size: 56.9 MB (56921187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8db666f85d9bf6e47b56332381281f973a63eb2e75f216da6c7de966ab6b3ccf`  
		Last Modified: Wed, 13 Nov 2024 00:44:18 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.30.3-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:8c63a415f442175dc0ac4d407d716e7e15c2839daedbba06a0cf1c5fbba42d70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1066346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f023ae63c182c047e5e162572d71a566b408affba4667ae76c4458764d659e63`

```dockerfile
```

-	Layers:
	-	`sha256:ca8e82b4ad234fde2144ac752875f5f4e2624ca01398237dd917456fa3876a45`  
		Last Modified: Wed, 13 Nov 2024 00:44:18 GMT  
		Size: 1.1 MB (1051275 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e884945c1eedf9b90e6c05f951a12c4509d27fa03085eababc577b6919684f86`  
		Last Modified: Wed, 13 Nov 2024 00:44:18 GMT  
		Size: 15.1 KB (15071 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.31`

```console
$ docker pull telegraf@sha256:57ae4ed17defe4d6356011581516a09850ff2bb710e7f96ed8c37fa1d5bda901
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.31` - linux; amd64

```console
$ docker pull telegraf@sha256:3b943303efbe657cd36be0ef1c9559539ce8c2b036081b65763fbe06616f64ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.9 MB (158869814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01de6457af670794ba32f7566f26e4c61f158ce46ebba0d28835993866e128e3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
ENV TELEGRAF_VERSION=1.31.3
# Mon, 28 Oct 2024 22:11:39 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 28 Oct 2024 22:11:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Oct 2024 22:11:39 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:b2b31b28ee3c96e96195c754f8679f690db4b18e475682d716122016ef056f39`  
		Last Modified: Tue, 12 Nov 2024 00:55:23 GMT  
		Size: 49.6 MB (49575695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3cc7b6f04730c072f8b292917e0d95bb886096a2b2b1781196170965161cd27`  
		Last Modified: Tue, 12 Nov 2024 02:38:12 GMT  
		Size: 24.1 MB (24058346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e8ac371f8f6b900f6816a3f3d5cf475581282536b290f9f56a144ebdc7efa47`  
		Last Modified: Tue, 12 Nov 2024 03:16:26 GMT  
		Size: 18.9 MB (18947946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c5955811c58047faf2b5f6273d3eb53a67c23a3f88e1be68006f165beeeeaa9`  
		Last Modified: Tue, 12 Nov 2024 03:16:26 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce1d1ddb522742bcec3581546c0c3f07a01dc1f06a991e58a1698c414883ee10`  
		Last Modified: Tue, 12 Nov 2024 03:16:28 GMT  
		Size: 66.3 MB (66285433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf32759841303be4847b388926fbd63c06ade86fdd4685861d9cd5191ac3848a`  
		Last Modified: Tue, 12 Nov 2024 03:16:26 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31` - unknown; unknown

```console
$ docker pull telegraf@sha256:aebc05fc8f913627950f6f3f2da7a29a65e82df43c5de9e73e46124c593ca73c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6433061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:146110216602f9d8df59808898a14358377ac3a60025e40ad791710780261655`

```dockerfile
```

-	Layers:
	-	`sha256:ab24cdf8cd6e4da8d19551df6ba5f96fe0757192ac082c0b1ddff14a3197e96b`  
		Last Modified: Tue, 12 Nov 2024 03:16:26 GMT  
		Size: 6.4 MB (6418591 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7ef7c4c09c09360b6e64da89f2b45319a58df07350cd0caccf6b4fed8b11ddd`  
		Last Modified: Tue, 12 Nov 2024 03:16:26 GMT  
		Size: 14.5 KB (14470 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.31` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:90babf59ae355dd9ca5289657c8387483c5284a406190467f8d608934b0855e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.5 MB (146510697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bce88ea4a0c3e79d65dda7b627957b2a5b84b012a02b4e4bf50bac61256d2925`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
ENV TELEGRAF_VERSION=1.31.3
# Mon, 28 Oct 2024 22:11:39 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 28 Oct 2024 22:11:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Oct 2024 22:11:39 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:46618ec96098836cac7950050ba554a969ebf8e9938d85d5f0d97015d3d25076`  
		Last Modified: Tue, 12 Nov 2024 00:56:14 GMT  
		Size: 45.2 MB (45150563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df9660b2b46aa0c77f5dd078f4e57432faf3dbcda91672b9e3f8c1b7892e0ee2`  
		Last Modified: Tue, 12 Nov 2024 15:59:18 GMT  
		Size: 22.0 MB (21960017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52c1519b04115013f7821f6b8398475148c7865994c7c5de2fb71d5916d5fb2e`  
		Last Modified: Wed, 13 Nov 2024 10:41:21 GMT  
		Size: 17.7 MB (17725323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a1859599b084be651ec09e42d0c7674081d74a573bd8eb676cc088609c1a1ed`  
		Last Modified: Wed, 13 Nov 2024 10:41:21 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e5aa14951461d4f24e8fe98880a1cdd3e533b827a78c21ab0b29e418320a334`  
		Last Modified: Wed, 13 Nov 2024 10:42:15 GMT  
		Size: 61.7 MB (61672399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9739370ed5c207a5b6b7db43b0f9c0842fbcd23b76c95fc4621def21308c0e3e`  
		Last Modified: Wed, 13 Nov 2024 10:42:13 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31` - unknown; unknown

```console
$ docker pull telegraf@sha256:05584c0701cf4027c88e039d7fe5bd76a64dd18dd3df21edfad122d5b705a046
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6428583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf5f21606923eb8970e4464c88e6c445a5b20b02e6f592a507b872e03d5c32a2`

```dockerfile
```

-	Layers:
	-	`sha256:8fe419709d841bd11cee70d38e46053dfdcc1a9f95dc2125218f9b4e238ab477`  
		Last Modified: Wed, 13 Nov 2024 10:42:14 GMT  
		Size: 6.4 MB (6414027 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff47b9c83c808c9f089467e4bfe9feee8100d1a26f2a5ecbb7430b71c870435b`  
		Last Modified: Wed, 13 Nov 2024 10:42:13 GMT  
		Size: 14.6 KB (14556 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.31` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:ec8273f3fba004c0b3f9a5303b931e968836be763b92b2f3e8c06778822566f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.4 MB (152436458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30fc9dfdcd3bfbfc5fa2da52cebb19ce46774c2b9f4b93738f9db6c048804fb9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
ENV TELEGRAF_VERSION=1.31.3
# Mon, 28 Oct 2024 22:11:39 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 28 Oct 2024 22:11:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Oct 2024 22:11:39 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:1a3f1864ec54b1398987bbe673e93d8b09842ecd51e86ab87d64857b70d188b1`  
		Last Modified: Tue, 12 Nov 2024 00:56:20 GMT  
		Size: 49.6 MB (49587201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:464f864cfaa846fbe1b8a889827404e18374f805d29d77c288a813ae8c4f6d91`  
		Last Modified: Tue, 12 Nov 2024 11:16:03 GMT  
		Size: 23.6 MB (23598253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d5aa793fe0445bc976082730ff6252895e46f7493850ef83f0509f98888fbcd`  
		Last Modified: Wed, 13 Nov 2024 06:19:22 GMT  
		Size: 18.9 MB (18870770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0541e3db3bb997348b43ecd98354da9cfea19cd50420a6ecef282eeb79d54dd`  
		Last Modified: Wed, 13 Nov 2024 06:19:21 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04dd9acae5a45241034d074fde46fc3d0bedb96ceb14748f3001d0b27ccd1100`  
		Last Modified: Wed, 13 Nov 2024 06:20:03 GMT  
		Size: 60.4 MB (60377826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3c6483b45655d3aa4960d2aecf9447dbfda073bbc42620db650a6e21eb02d82`  
		Last Modified: Wed, 13 Nov 2024 06:20:01 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31` - unknown; unknown

```console
$ docker pull telegraf@sha256:406c7a9c7a1d5ffafbc0a2efc050be36068b22b6548ac3edcbb77cb1740bb76b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6434686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5a9c8b171a3728fcafece172dac126375d799e5c3c43c7485224a26cc7dc47a`

```dockerfile
```

-	Layers:
	-	`sha256:9c5adf7b937a032637f9aeacf562996457d94af7795d98ec1ca54416576a8396`  
		Last Modified: Wed, 13 Nov 2024 06:20:02 GMT  
		Size: 6.4 MB (6420106 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c5e31a75ec7e5ddb2347aafffae50e589091e5faa92b6f36fb14ce975f0c628`  
		Last Modified: Wed, 13 Nov 2024 06:20:01 GMT  
		Size: 14.6 KB (14580 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.31-alpine`

```console
$ docker pull telegraf@sha256:de67a108f127bbfd06b21b18fe8bba745b71b0e1e4f743a5e06ca45a705f42a8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.31-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:997da12fb34bf904334e39d911327f45ef79d2a498bc71c547e8d5d70e1e0f62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.1 MB (72149519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d731e4354684f4ef6b4d3e92a4e45008a4deb236170c5f0a349ee3416002dde`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Mon, 28 Oct 2024 22:11:39 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
ENV TELEGRAF_VERSION=1.31.3
# Mon, 28 Oct 2024 22:11:39 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 28 Oct 2024 22:11:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Oct 2024 22:11:39 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16f10048322eb86f2be1b7699a5c82453c4c117017d59212b59520756810207c`  
		Last Modified: Tue, 12 Nov 2024 02:21:18 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddf3378dfe0cc506adaa827bc20236dda2e82ec4b94cb866c503da70171e15c9`  
		Last Modified: Tue, 12 Nov 2024 02:21:18 GMT  
		Size: 2.4 MB (2444831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36d9dde8a359ac2194bdd2c1b777d7406616290d0020cc51a94a759f0ff42479`  
		Last Modified: Tue, 12 Nov 2024 02:21:18 GMT  
		Size: 66.1 MB (66080176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86878befd798f41f972e38cf31f2ad1250c4660288a9574685a05d438f0c41ec`  
		Last Modified: Tue, 12 Nov 2024 02:21:17 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:0f5d76963c8dedbac66a6c0c7490a05a1a2e628a1a60395bab2df9c350343fb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1079572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0749f1205673d1a6b749b89096eae616216f940a6b4a468d12e7e2d5c950bdd9`

```dockerfile
```

-	Layers:
	-	`sha256:f6021eb66e288afca40a3de988cb4b331eab3569a6cf828c4b2c64257f06557f`  
		Last Modified: Tue, 12 Nov 2024 02:21:18 GMT  
		Size: 1.1 MB (1064613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc8d6cf96bf0c4c71fd14e16c3f7a3b4c0a73536343040b53c476c22e16d1203`  
		Last Modified: Tue, 12 Nov 2024 02:21:17 GMT  
		Size: 15.0 KB (14959 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.31-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:c721817221b9cc330049e20dc9cf632918644881181202c11ab1ef5669e0f054
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.8 MB (66790689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52ecbb2893d24b9033fa9dbf9bf0c0fc5ead7044e742fc8801c1163854e6bc85`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Mon, 28 Oct 2024 22:11:39 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
ENV TELEGRAF_VERSION=1.31.3
# Mon, 28 Oct 2024 22:11:39 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 28 Oct 2024 22:11:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Oct 2024 22:11:39 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9de63ce930d0f77f6402e61ee732ad4f784c59fd26df033bb1b7d6a0b87a2f4`  
		Last Modified: Tue, 12 Nov 2024 13:17:18 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:848dadffeaafa841326acf8c33573919df8ff222e2680607f7d10bb804a23d6c`  
		Last Modified: Wed, 13 Nov 2024 00:44:18 GMT  
		Size: 2.5 MB (2530663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c165eccfb6fb22936f132b38db1bea94249c4f9025902071816f681d45278592`  
		Last Modified: Wed, 13 Nov 2024 00:44:58 GMT  
		Size: 60.2 MB (60171693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f25aa3692cb281849fa0eba2cb21828fd6ad1c13fa61aaec973cde6d98d95d`  
		Last Modified: Wed, 13 Nov 2024 00:44:56 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:3c1199bc5e2229bba0fa164cb749ad110ae8ccfaebe006a2f0b23f770c5e1823
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1076145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89563d9bd0aa15d8dc6e06421e37cb9040f7ff3e1cee8e2ed0852ff7977231ce`

```dockerfile
```

-	Layers:
	-	`sha256:e91298accb6ca3e23bd891af5501a0f171f772039e4cfdcea12b9c71bbac032a`  
		Last Modified: Wed, 13 Nov 2024 00:44:56 GMT  
		Size: 1.1 MB (1061075 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c48f3921a2b1ca085f8a80fe529e5b99ce2fe7915122f7539650b0150864970c`  
		Last Modified: Wed, 13 Nov 2024 00:44:56 GMT  
		Size: 15.1 KB (15070 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.31.3`

```console
$ docker pull telegraf@sha256:57ae4ed17defe4d6356011581516a09850ff2bb710e7f96ed8c37fa1d5bda901
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.31.3` - linux; amd64

```console
$ docker pull telegraf@sha256:3b943303efbe657cd36be0ef1c9559539ce8c2b036081b65763fbe06616f64ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.9 MB (158869814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01de6457af670794ba32f7566f26e4c61f158ce46ebba0d28835993866e128e3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
ENV TELEGRAF_VERSION=1.31.3
# Mon, 28 Oct 2024 22:11:39 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 28 Oct 2024 22:11:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Oct 2024 22:11:39 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:b2b31b28ee3c96e96195c754f8679f690db4b18e475682d716122016ef056f39`  
		Last Modified: Tue, 12 Nov 2024 00:55:23 GMT  
		Size: 49.6 MB (49575695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3cc7b6f04730c072f8b292917e0d95bb886096a2b2b1781196170965161cd27`  
		Last Modified: Tue, 12 Nov 2024 02:38:12 GMT  
		Size: 24.1 MB (24058346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e8ac371f8f6b900f6816a3f3d5cf475581282536b290f9f56a144ebdc7efa47`  
		Last Modified: Tue, 12 Nov 2024 03:16:26 GMT  
		Size: 18.9 MB (18947946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c5955811c58047faf2b5f6273d3eb53a67c23a3f88e1be68006f165beeeeaa9`  
		Last Modified: Tue, 12 Nov 2024 03:16:26 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce1d1ddb522742bcec3581546c0c3f07a01dc1f06a991e58a1698c414883ee10`  
		Last Modified: Tue, 12 Nov 2024 03:16:28 GMT  
		Size: 66.3 MB (66285433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf32759841303be4847b388926fbd63c06ade86fdd4685861d9cd5191ac3848a`  
		Last Modified: Tue, 12 Nov 2024 03:16:26 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:aebc05fc8f913627950f6f3f2da7a29a65e82df43c5de9e73e46124c593ca73c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6433061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:146110216602f9d8df59808898a14358377ac3a60025e40ad791710780261655`

```dockerfile
```

-	Layers:
	-	`sha256:ab24cdf8cd6e4da8d19551df6ba5f96fe0757192ac082c0b1ddff14a3197e96b`  
		Last Modified: Tue, 12 Nov 2024 03:16:26 GMT  
		Size: 6.4 MB (6418591 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7ef7c4c09c09360b6e64da89f2b45319a58df07350cd0caccf6b4fed8b11ddd`  
		Last Modified: Tue, 12 Nov 2024 03:16:26 GMT  
		Size: 14.5 KB (14470 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.31.3` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:90babf59ae355dd9ca5289657c8387483c5284a406190467f8d608934b0855e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.5 MB (146510697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bce88ea4a0c3e79d65dda7b627957b2a5b84b012a02b4e4bf50bac61256d2925`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
ENV TELEGRAF_VERSION=1.31.3
# Mon, 28 Oct 2024 22:11:39 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 28 Oct 2024 22:11:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Oct 2024 22:11:39 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:46618ec96098836cac7950050ba554a969ebf8e9938d85d5f0d97015d3d25076`  
		Last Modified: Tue, 12 Nov 2024 00:56:14 GMT  
		Size: 45.2 MB (45150563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df9660b2b46aa0c77f5dd078f4e57432faf3dbcda91672b9e3f8c1b7892e0ee2`  
		Last Modified: Tue, 12 Nov 2024 15:59:18 GMT  
		Size: 22.0 MB (21960017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52c1519b04115013f7821f6b8398475148c7865994c7c5de2fb71d5916d5fb2e`  
		Last Modified: Wed, 13 Nov 2024 10:41:21 GMT  
		Size: 17.7 MB (17725323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a1859599b084be651ec09e42d0c7674081d74a573bd8eb676cc088609c1a1ed`  
		Last Modified: Wed, 13 Nov 2024 10:41:21 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e5aa14951461d4f24e8fe98880a1cdd3e533b827a78c21ab0b29e418320a334`  
		Last Modified: Wed, 13 Nov 2024 10:42:15 GMT  
		Size: 61.7 MB (61672399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9739370ed5c207a5b6b7db43b0f9c0842fbcd23b76c95fc4621def21308c0e3e`  
		Last Modified: Wed, 13 Nov 2024 10:42:13 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:05584c0701cf4027c88e039d7fe5bd76a64dd18dd3df21edfad122d5b705a046
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6428583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf5f21606923eb8970e4464c88e6c445a5b20b02e6f592a507b872e03d5c32a2`

```dockerfile
```

-	Layers:
	-	`sha256:8fe419709d841bd11cee70d38e46053dfdcc1a9f95dc2125218f9b4e238ab477`  
		Last Modified: Wed, 13 Nov 2024 10:42:14 GMT  
		Size: 6.4 MB (6414027 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff47b9c83c808c9f089467e4bfe9feee8100d1a26f2a5ecbb7430b71c870435b`  
		Last Modified: Wed, 13 Nov 2024 10:42:13 GMT  
		Size: 14.6 KB (14556 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.31.3` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:ec8273f3fba004c0b3f9a5303b931e968836be763b92b2f3e8c06778822566f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.4 MB (152436458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30fc9dfdcd3bfbfc5fa2da52cebb19ce46774c2b9f4b93738f9db6c048804fb9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
ENV TELEGRAF_VERSION=1.31.3
# Mon, 28 Oct 2024 22:11:39 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 28 Oct 2024 22:11:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Oct 2024 22:11:39 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:1a3f1864ec54b1398987bbe673e93d8b09842ecd51e86ab87d64857b70d188b1`  
		Last Modified: Tue, 12 Nov 2024 00:56:20 GMT  
		Size: 49.6 MB (49587201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:464f864cfaa846fbe1b8a889827404e18374f805d29d77c288a813ae8c4f6d91`  
		Last Modified: Tue, 12 Nov 2024 11:16:03 GMT  
		Size: 23.6 MB (23598253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d5aa793fe0445bc976082730ff6252895e46f7493850ef83f0509f98888fbcd`  
		Last Modified: Wed, 13 Nov 2024 06:19:22 GMT  
		Size: 18.9 MB (18870770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0541e3db3bb997348b43ecd98354da9cfea19cd50420a6ecef282eeb79d54dd`  
		Last Modified: Wed, 13 Nov 2024 06:19:21 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04dd9acae5a45241034d074fde46fc3d0bedb96ceb14748f3001d0b27ccd1100`  
		Last Modified: Wed, 13 Nov 2024 06:20:03 GMT  
		Size: 60.4 MB (60377826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3c6483b45655d3aa4960d2aecf9447dbfda073bbc42620db650a6e21eb02d82`  
		Last Modified: Wed, 13 Nov 2024 06:20:01 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:406c7a9c7a1d5ffafbc0a2efc050be36068b22b6548ac3edcbb77cb1740bb76b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6434686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5a9c8b171a3728fcafece172dac126375d799e5c3c43c7485224a26cc7dc47a`

```dockerfile
```

-	Layers:
	-	`sha256:9c5adf7b937a032637f9aeacf562996457d94af7795d98ec1ca54416576a8396`  
		Last Modified: Wed, 13 Nov 2024 06:20:02 GMT  
		Size: 6.4 MB (6420106 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c5e31a75ec7e5ddb2347aafffae50e589091e5faa92b6f36fb14ce975f0c628`  
		Last Modified: Wed, 13 Nov 2024 06:20:01 GMT  
		Size: 14.6 KB (14580 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.31.3-alpine`

```console
$ docker pull telegraf@sha256:de67a108f127bbfd06b21b18fe8bba745b71b0e1e4f743a5e06ca45a705f42a8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.31.3-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:997da12fb34bf904334e39d911327f45ef79d2a498bc71c547e8d5d70e1e0f62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.1 MB (72149519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d731e4354684f4ef6b4d3e92a4e45008a4deb236170c5f0a349ee3416002dde`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Mon, 28 Oct 2024 22:11:39 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
ENV TELEGRAF_VERSION=1.31.3
# Mon, 28 Oct 2024 22:11:39 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 28 Oct 2024 22:11:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Oct 2024 22:11:39 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16f10048322eb86f2be1b7699a5c82453c4c117017d59212b59520756810207c`  
		Last Modified: Tue, 12 Nov 2024 02:21:18 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddf3378dfe0cc506adaa827bc20236dda2e82ec4b94cb866c503da70171e15c9`  
		Last Modified: Tue, 12 Nov 2024 02:21:18 GMT  
		Size: 2.4 MB (2444831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36d9dde8a359ac2194bdd2c1b777d7406616290d0020cc51a94a759f0ff42479`  
		Last Modified: Tue, 12 Nov 2024 02:21:18 GMT  
		Size: 66.1 MB (66080176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86878befd798f41f972e38cf31f2ad1250c4660288a9574685a05d438f0c41ec`  
		Last Modified: Tue, 12 Nov 2024 02:21:17 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31.3-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:0f5d76963c8dedbac66a6c0c7490a05a1a2e628a1a60395bab2df9c350343fb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1079572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0749f1205673d1a6b749b89096eae616216f940a6b4a468d12e7e2d5c950bdd9`

```dockerfile
```

-	Layers:
	-	`sha256:f6021eb66e288afca40a3de988cb4b331eab3569a6cf828c4b2c64257f06557f`  
		Last Modified: Tue, 12 Nov 2024 02:21:18 GMT  
		Size: 1.1 MB (1064613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc8d6cf96bf0c4c71fd14e16c3f7a3b4c0a73536343040b53c476c22e16d1203`  
		Last Modified: Tue, 12 Nov 2024 02:21:17 GMT  
		Size: 15.0 KB (14959 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.31.3-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:c721817221b9cc330049e20dc9cf632918644881181202c11ab1ef5669e0f054
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.8 MB (66790689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52ecbb2893d24b9033fa9dbf9bf0c0fc5ead7044e742fc8801c1163854e6bc85`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Mon, 28 Oct 2024 22:11:39 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
ENV TELEGRAF_VERSION=1.31.3
# Mon, 28 Oct 2024 22:11:39 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 28 Oct 2024 22:11:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Oct 2024 22:11:39 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9de63ce930d0f77f6402e61ee732ad4f784c59fd26df033bb1b7d6a0b87a2f4`  
		Last Modified: Tue, 12 Nov 2024 13:17:18 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:848dadffeaafa841326acf8c33573919df8ff222e2680607f7d10bb804a23d6c`  
		Last Modified: Wed, 13 Nov 2024 00:44:18 GMT  
		Size: 2.5 MB (2530663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c165eccfb6fb22936f132b38db1bea94249c4f9025902071816f681d45278592`  
		Last Modified: Wed, 13 Nov 2024 00:44:58 GMT  
		Size: 60.2 MB (60171693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f25aa3692cb281849fa0eba2cb21828fd6ad1c13fa61aaec973cde6d98d95d`  
		Last Modified: Wed, 13 Nov 2024 00:44:56 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31.3-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:3c1199bc5e2229bba0fa164cb749ad110ae8ccfaebe006a2f0b23f770c5e1823
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1076145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89563d9bd0aa15d8dc6e06421e37cb9040f7ff3e1cee8e2ed0852ff7977231ce`

```dockerfile
```

-	Layers:
	-	`sha256:e91298accb6ca3e23bd891af5501a0f171f772039e4cfdcea12b9c71bbac032a`  
		Last Modified: Wed, 13 Nov 2024 00:44:56 GMT  
		Size: 1.1 MB (1061075 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c48f3921a2b1ca085f8a80fe529e5b99ce2fe7915122f7539650b0150864970c`  
		Last Modified: Wed, 13 Nov 2024 00:44:56 GMT  
		Size: 15.1 KB (15070 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.32`

```console
$ docker pull telegraf@sha256:b1e028a8d5b2dbef4023ae0b80c0648696095a13843e9fd54ad30454d842af1d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.32` - linux; amd64

```console
$ docker pull telegraf@sha256:26ab32d6baa5d88a74f3c026969113065f921f45c429648004b1c80445308307
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.6 MB (162605552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c413022d422ab762bbbe969ae0933eaeb95575339550b95785e7c7bd9d2981b6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 Nov 2024 20:48:32 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 Nov 2024 20:48:32 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 18 Nov 2024 20:48:32 GMT
ENV TELEGRAF_VERSION=1.32.3
# Mon, 18 Nov 2024 20:48:32 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 18 Nov 2024 20:48:32 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 18 Nov 2024 20:48:32 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 18 Nov 2024 20:48:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 18 Nov 2024 20:48:32 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:b2b31b28ee3c96e96195c754f8679f690db4b18e475682d716122016ef056f39`  
		Last Modified: Tue, 12 Nov 2024 00:55:23 GMT  
		Size: 49.6 MB (49575695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3cc7b6f04730c072f8b292917e0d95bb886096a2b2b1781196170965161cd27`  
		Last Modified: Tue, 12 Nov 2024 02:38:12 GMT  
		Size: 24.1 MB (24058346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:010db0dbba3535b069ec123d815169b81b7a846befaf2f7f11071758e977afb8`  
		Last Modified: Mon, 18 Nov 2024 23:04:15 GMT  
		Size: 18.9 MB (18948023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fbe67aa00e7a7e452eef611480413f250f464b9d2d2e1cf8b61861ffb410289`  
		Last Modified: Mon, 18 Nov 2024 23:04:12 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4d7830fa54859d2cab67010b9fa1b43d31af49b0cb443b332e89757194f5a80`  
		Last Modified: Mon, 18 Nov 2024 23:04:15 GMT  
		Size: 70.0 MB (70021078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b39496eca681636463ce8350a89dd92aee8f8d2b405b7278659ea5e976890ba8`  
		Last Modified: Mon, 18 Nov 2024 23:04:13 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.32` - unknown; unknown

```console
$ docker pull telegraf@sha256:f8069a5cfc706a1f70331bb38f7088cc52071e927cf23ad2965ac31e1112cbb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6443002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dda0992c700b7338e9f6e2920a0d7e6c08b358b5084b2dbeb0f1f1904a39086a`

```dockerfile
```

-	Layers:
	-	`sha256:d9eccfe45f5f72667eaa344fe58ab1a4de11b29f18d0108696482aa1f5d12be8`  
		Last Modified: Mon, 18 Nov 2024 23:04:13 GMT  
		Size: 6.4 MB (6428231 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:984633f68829e1d69cf10b19ef022bcc5a0d0d346e20f73758fe2e9d0ff1d80f`  
		Last Modified: Mon, 18 Nov 2024 23:04:12 GMT  
		Size: 14.8 KB (14771 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.32` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:2652b91639669f475dcbafa85d5ceb407b4e5f5048ac1bae42fb5111a1574fad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.5 MB (149521208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ee0e34e51635b65425f13e5466fd55a7e9b870199cf0af36b911845e252c33c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 Nov 2024 20:48:32 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 Nov 2024 20:48:32 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 18 Nov 2024 20:48:32 GMT
ENV TELEGRAF_VERSION=1.32.3
# Mon, 18 Nov 2024 20:48:32 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 18 Nov 2024 20:48:32 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 18 Nov 2024 20:48:32 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 18 Nov 2024 20:48:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 18 Nov 2024 20:48:32 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:46618ec96098836cac7950050ba554a969ebf8e9938d85d5f0d97015d3d25076`  
		Last Modified: Tue, 12 Nov 2024 00:56:14 GMT  
		Size: 45.2 MB (45150563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df9660b2b46aa0c77f5dd078f4e57432faf3dbcda91672b9e3f8c1b7892e0ee2`  
		Last Modified: Tue, 12 Nov 2024 15:59:18 GMT  
		Size: 22.0 MB (21960017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52c1519b04115013f7821f6b8398475148c7865994c7c5de2fb71d5916d5fb2e`  
		Last Modified: Wed, 13 Nov 2024 10:41:21 GMT  
		Size: 17.7 MB (17725323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a1859599b084be651ec09e42d0c7674081d74a573bd8eb676cc088609c1a1ed`  
		Last Modified: Wed, 13 Nov 2024 10:41:21 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82bc73ed1aaf2e0fee0d7200d13d2f068a225cf6b26b40a5f955694865b8c8cc`  
		Last Modified: Mon, 18 Nov 2024 23:04:12 GMT  
		Size: 64.7 MB (64682909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96c009391f91b8895de1428a5cfbe7014c5d0674f9bc7bcf35dafc55bfa9fcfc`  
		Last Modified: Mon, 18 Nov 2024 23:04:10 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.32` - unknown; unknown

```console
$ docker pull telegraf@sha256:7c1f5dc1ef14ae1e81c1073d52d1f1c9cc0e5d2b5c8fc4859ddbd3eaad79def4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6438541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ec659d8892cbf34142ad5feb5c816f440a4c1a82e16696794ec671aaa51eb3c`

```dockerfile
```

-	Layers:
	-	`sha256:d1c124d3335a2c3aa178c49bd4dfce25b32a69478154254a7d44c040a5323ed3`  
		Last Modified: Mon, 18 Nov 2024 23:04:10 GMT  
		Size: 6.4 MB (6423675 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f10b0c590cdddd17bfac9a645ec5e1bc2dd583f281d32c22e76209aa449e28d3`  
		Last Modified: Mon, 18 Nov 2024 23:04:10 GMT  
		Size: 14.9 KB (14866 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.32` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:46eb951e12350a8349a9eab22a97e879bf9844372861a6ca57e2a54b229c7de4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.1 MB (156120112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c067c20c86a405bc577d24fb4f24730ded5b75885b386f3d028c7dc4b4d0f431`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
ENV TELEGRAF_VERSION=1.32.2
# Mon, 28 Oct 2024 22:11:39 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 28 Oct 2024 22:11:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Oct 2024 22:11:39 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:1a3f1864ec54b1398987bbe673e93d8b09842ecd51e86ab87d64857b70d188b1`  
		Last Modified: Tue, 12 Nov 2024 00:56:20 GMT  
		Size: 49.6 MB (49587201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:464f864cfaa846fbe1b8a889827404e18374f805d29d77c288a813ae8c4f6d91`  
		Last Modified: Tue, 12 Nov 2024 11:16:03 GMT  
		Size: 23.6 MB (23598253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d5aa793fe0445bc976082730ff6252895e46f7493850ef83f0509f98888fbcd`  
		Last Modified: Wed, 13 Nov 2024 06:19:22 GMT  
		Size: 18.9 MB (18870770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0541e3db3bb997348b43ecd98354da9cfea19cd50420a6ecef282eeb79d54dd`  
		Last Modified: Wed, 13 Nov 2024 06:19:21 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ecba7ebf10b2dda935eee1767535659f3aaec3e27554fd339930447ce495751`  
		Last Modified: Wed, 13 Nov 2024 06:20:49 GMT  
		Size: 64.1 MB (64061480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dceae68a9917b8fc00f1cf8405e8983aeb139626a6cde54bfc9c7c392e08d11`  
		Last Modified: Wed, 13 Nov 2024 06:20:47 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.32` - unknown; unknown

```console
$ docker pull telegraf@sha256:e98272684f7bc4e923fe35844923fe23dd6ad9c7b0617532d4d291b0c8dce201
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6444639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e2c30cdaeef6af84296cecd84e8795ecf394961e8953d4292d1862904e7c3ed`

```dockerfile
```

-	Layers:
	-	`sha256:7ff334f246f441b9760c06c58f4f71e958140a28715d02c3bc2941cd386561b2`  
		Last Modified: Wed, 13 Nov 2024 06:20:47 GMT  
		Size: 6.4 MB (6429746 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19342b085c35118dc66d01ba39202ee177c1430e22e84dbebac83d959314e441`  
		Last Modified: Wed, 13 Nov 2024 06:20:47 GMT  
		Size: 14.9 KB (14893 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.32-alpine`

```console
$ docker pull telegraf@sha256:bdbace5beb3a53e9a2caf078b4c43e71dcc33354b2d78e9cb3ad1b7fff00ca25
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.32-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:60e401f12742cafbfa564bb7f31d6e5c35daba0b50e0b5264c0cddac21e0efcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75893896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:445d094c3c199fa803bcab90c7ffcc6166fa97f07846d2d88d6b0e3bd5ad333c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Mon, 18 Nov 2024 20:48:32 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 18 Nov 2024 20:48:32 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 18 Nov 2024 20:48:32 GMT
ENV TELEGRAF_VERSION=1.32.3
# Mon, 18 Nov 2024 20:48:32 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 18 Nov 2024 20:48:32 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 18 Nov 2024 20:48:32 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 18 Nov 2024 20:48:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 18 Nov 2024 20:48:32 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caee9ab776a1c2beeb238e0643dbf6f3b7c0a83fd9aa339dc798e2b5272a39f5`  
		Last Modified: Mon, 18 Nov 2024 23:04:06 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ac69faebcdcde53563af6c2f2356011b54221d2d336fa20004d6e41cf7f676c`  
		Last Modified: Mon, 18 Nov 2024 23:04:06 GMT  
		Size: 2.4 MB (2444821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07d3519fedc4d5ee37ea7859c2cedc0f290e072022c6947c318979fd6eb71f55`  
		Last Modified: Mon, 18 Nov 2024 23:04:08 GMT  
		Size: 69.8 MB (69824563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da6fc6e4c616b483bafdc6d886f7d5a5c2d59fcbff06d37f5eec6352e6f45818`  
		Last Modified: Mon, 18 Nov 2024 23:04:06 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.32-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:281e39380036537235243436889bf410fd2908fd811d92157772d744f55dba4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1089516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3c515de8cd05e47bd266f48c2b5b5034383aebbc3b2dfc9e9eb1ba756e4d1da`

```dockerfile
```

-	Layers:
	-	`sha256:b6d2654f5db4cef75f0d0dfbaf9b3095359625a64b11278eaa23d00004cd15d9`  
		Last Modified: Mon, 18 Nov 2024 23:04:07 GMT  
		Size: 1.1 MB (1074253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34df0a4ca1bb919a775b446cf53aed82c5c950fb10f80c1950f2a1e0e6e2abdb`  
		Last Modified: Mon, 18 Nov 2024 23:04:06 GMT  
		Size: 15.3 KB (15263 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.32-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:360131f2b94e1b4e0a0a55accc6e40255089a89942b6d2d23e682dc769763f34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.5 MB (70488602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d56de21a5014770bd14dd40f920748988275ffe324b3268c2cef771f98132bf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Mon, 28 Oct 2024 22:11:39 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
ENV TELEGRAF_VERSION=1.32.2
# Mon, 28 Oct 2024 22:11:39 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 28 Oct 2024 22:11:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Oct 2024 22:11:39 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9de63ce930d0f77f6402e61ee732ad4f784c59fd26df033bb1b7d6a0b87a2f4`  
		Last Modified: Tue, 12 Nov 2024 13:17:18 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:848dadffeaafa841326acf8c33573919df8ff222e2680607f7d10bb804a23d6c`  
		Last Modified: Wed, 13 Nov 2024 00:44:18 GMT  
		Size: 2.5 MB (2530663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4383827a27cf7c8e76ae40d02da9661a942bebbe18254b9be04d527bce572de5`  
		Last Modified: Wed, 13 Nov 2024 00:45:35 GMT  
		Size: 63.9 MB (63869605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98293dc53f9f009ae42c20ca72b06e353c3ce6fbaa9fd797c46aad972fea12e7`  
		Last Modified: Wed, 13 Nov 2024 00:45:33 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.32-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:195d46a82a6c805c64e6541bef8cd6d5a323cd483df30830f7862efc8b0a850a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1086100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c86876f9c189bd84719ab02f8fa82628ea72b474c79ac492165966c68f7af49`

```dockerfile
```

-	Layers:
	-	`sha256:f52cb10165d665b2775de9498b738fbda072838abd2ba18481be987a84e09f3b`  
		Last Modified: Wed, 13 Nov 2024 00:45:33 GMT  
		Size: 1.1 MB (1070715 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:701181e3f6633764e305402b4491f468e9add860351d9ac3ebad727e1e6c9277`  
		Last Modified: Wed, 13 Nov 2024 00:45:33 GMT  
		Size: 15.4 KB (15385 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.32.3`

```console
$ docker pull telegraf@sha256:3e9e918e05b7659d74bb04bb22a7b4e5ec021834d1cfe80071211a21851fb0f6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown

### `telegraf:1.32.3` - linux; amd64

```console
$ docker pull telegraf@sha256:26ab32d6baa5d88a74f3c026969113065f921f45c429648004b1c80445308307
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.6 MB (162605552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c413022d422ab762bbbe969ae0933eaeb95575339550b95785e7c7bd9d2981b6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 Nov 2024 20:48:32 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 Nov 2024 20:48:32 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 18 Nov 2024 20:48:32 GMT
ENV TELEGRAF_VERSION=1.32.3
# Mon, 18 Nov 2024 20:48:32 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 18 Nov 2024 20:48:32 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 18 Nov 2024 20:48:32 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 18 Nov 2024 20:48:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 18 Nov 2024 20:48:32 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:b2b31b28ee3c96e96195c754f8679f690db4b18e475682d716122016ef056f39`  
		Last Modified: Tue, 12 Nov 2024 00:55:23 GMT  
		Size: 49.6 MB (49575695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3cc7b6f04730c072f8b292917e0d95bb886096a2b2b1781196170965161cd27`  
		Last Modified: Tue, 12 Nov 2024 02:38:12 GMT  
		Size: 24.1 MB (24058346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:010db0dbba3535b069ec123d815169b81b7a846befaf2f7f11071758e977afb8`  
		Last Modified: Mon, 18 Nov 2024 23:04:15 GMT  
		Size: 18.9 MB (18948023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fbe67aa00e7a7e452eef611480413f250f464b9d2d2e1cf8b61861ffb410289`  
		Last Modified: Mon, 18 Nov 2024 23:04:12 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4d7830fa54859d2cab67010b9fa1b43d31af49b0cb443b332e89757194f5a80`  
		Last Modified: Mon, 18 Nov 2024 23:04:15 GMT  
		Size: 70.0 MB (70021078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b39496eca681636463ce8350a89dd92aee8f8d2b405b7278659ea5e976890ba8`  
		Last Modified: Mon, 18 Nov 2024 23:04:13 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.32.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:f8069a5cfc706a1f70331bb38f7088cc52071e927cf23ad2965ac31e1112cbb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6443002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dda0992c700b7338e9f6e2920a0d7e6c08b358b5084b2dbeb0f1f1904a39086a`

```dockerfile
```

-	Layers:
	-	`sha256:d9eccfe45f5f72667eaa344fe58ab1a4de11b29f18d0108696482aa1f5d12be8`  
		Last Modified: Mon, 18 Nov 2024 23:04:13 GMT  
		Size: 6.4 MB (6428231 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:984633f68829e1d69cf10b19ef022bcc5a0d0d346e20f73758fe2e9d0ff1d80f`  
		Last Modified: Mon, 18 Nov 2024 23:04:12 GMT  
		Size: 14.8 KB (14771 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.32.3` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:2652b91639669f475dcbafa85d5ceb407b4e5f5048ac1bae42fb5111a1574fad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.5 MB (149521208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ee0e34e51635b65425f13e5466fd55a7e9b870199cf0af36b911845e252c33c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 Nov 2024 20:48:32 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 Nov 2024 20:48:32 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 18 Nov 2024 20:48:32 GMT
ENV TELEGRAF_VERSION=1.32.3
# Mon, 18 Nov 2024 20:48:32 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 18 Nov 2024 20:48:32 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 18 Nov 2024 20:48:32 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 18 Nov 2024 20:48:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 18 Nov 2024 20:48:32 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:46618ec96098836cac7950050ba554a969ebf8e9938d85d5f0d97015d3d25076`  
		Last Modified: Tue, 12 Nov 2024 00:56:14 GMT  
		Size: 45.2 MB (45150563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df9660b2b46aa0c77f5dd078f4e57432faf3dbcda91672b9e3f8c1b7892e0ee2`  
		Last Modified: Tue, 12 Nov 2024 15:59:18 GMT  
		Size: 22.0 MB (21960017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52c1519b04115013f7821f6b8398475148c7865994c7c5de2fb71d5916d5fb2e`  
		Last Modified: Wed, 13 Nov 2024 10:41:21 GMT  
		Size: 17.7 MB (17725323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a1859599b084be651ec09e42d0c7674081d74a573bd8eb676cc088609c1a1ed`  
		Last Modified: Wed, 13 Nov 2024 10:41:21 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82bc73ed1aaf2e0fee0d7200d13d2f068a225cf6b26b40a5f955694865b8c8cc`  
		Last Modified: Mon, 18 Nov 2024 23:04:12 GMT  
		Size: 64.7 MB (64682909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96c009391f91b8895de1428a5cfbe7014c5d0674f9bc7bcf35dafc55bfa9fcfc`  
		Last Modified: Mon, 18 Nov 2024 23:04:10 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.32.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:7c1f5dc1ef14ae1e81c1073d52d1f1c9cc0e5d2b5c8fc4859ddbd3eaad79def4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6438541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ec659d8892cbf34142ad5feb5c816f440a4c1a82e16696794ec671aaa51eb3c`

```dockerfile
```

-	Layers:
	-	`sha256:d1c124d3335a2c3aa178c49bd4dfce25b32a69478154254a7d44c040a5323ed3`  
		Last Modified: Mon, 18 Nov 2024 23:04:10 GMT  
		Size: 6.4 MB (6423675 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f10b0c590cdddd17bfac9a645ec5e1bc2dd583f281d32c22e76209aa449e28d3`  
		Last Modified: Mon, 18 Nov 2024 23:04:10 GMT  
		Size: 14.9 KB (14866 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.32.3-alpine`

```console
$ docker pull telegraf@sha256:851c5b88d8ef67a5cacf96643b91ed1d3b2ce729dade0a516cd08154d4e8c149
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `telegraf:1.32.3-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:60e401f12742cafbfa564bb7f31d6e5c35daba0b50e0b5264c0cddac21e0efcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75893896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:445d094c3c199fa803bcab90c7ffcc6166fa97f07846d2d88d6b0e3bd5ad333c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Mon, 18 Nov 2024 20:48:32 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 18 Nov 2024 20:48:32 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 18 Nov 2024 20:48:32 GMT
ENV TELEGRAF_VERSION=1.32.3
# Mon, 18 Nov 2024 20:48:32 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 18 Nov 2024 20:48:32 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 18 Nov 2024 20:48:32 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 18 Nov 2024 20:48:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 18 Nov 2024 20:48:32 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caee9ab776a1c2beeb238e0643dbf6f3b7c0a83fd9aa339dc798e2b5272a39f5`  
		Last Modified: Mon, 18 Nov 2024 23:04:06 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ac69faebcdcde53563af6c2f2356011b54221d2d336fa20004d6e41cf7f676c`  
		Last Modified: Mon, 18 Nov 2024 23:04:06 GMT  
		Size: 2.4 MB (2444821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07d3519fedc4d5ee37ea7859c2cedc0f290e072022c6947c318979fd6eb71f55`  
		Last Modified: Mon, 18 Nov 2024 23:04:08 GMT  
		Size: 69.8 MB (69824563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da6fc6e4c616b483bafdc6d886f7d5a5c2d59fcbff06d37f5eec6352e6f45818`  
		Last Modified: Mon, 18 Nov 2024 23:04:06 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.32.3-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:281e39380036537235243436889bf410fd2908fd811d92157772d744f55dba4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1089516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3c515de8cd05e47bd266f48c2b5b5034383aebbc3b2dfc9e9eb1ba756e4d1da`

```dockerfile
```

-	Layers:
	-	`sha256:b6d2654f5db4cef75f0d0dfbaf9b3095359625a64b11278eaa23d00004cd15d9`  
		Last Modified: Mon, 18 Nov 2024 23:04:07 GMT  
		Size: 1.1 MB (1074253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34df0a4ca1bb919a775b446cf53aed82c5c950fb10f80c1950f2a1e0e6e2abdb`  
		Last Modified: Mon, 18 Nov 2024 23:04:06 GMT  
		Size: 15.3 KB (15263 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:alpine`

```console
$ docker pull telegraf@sha256:bdbace5beb3a53e9a2caf078b4c43e71dcc33354b2d78e9cb3ad1b7fff00ca25
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:60e401f12742cafbfa564bb7f31d6e5c35daba0b50e0b5264c0cddac21e0efcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75893896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:445d094c3c199fa803bcab90c7ffcc6166fa97f07846d2d88d6b0e3bd5ad333c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Mon, 18 Nov 2024 20:48:32 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 18 Nov 2024 20:48:32 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 18 Nov 2024 20:48:32 GMT
ENV TELEGRAF_VERSION=1.32.3
# Mon, 18 Nov 2024 20:48:32 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 18 Nov 2024 20:48:32 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 18 Nov 2024 20:48:32 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 18 Nov 2024 20:48:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 18 Nov 2024 20:48:32 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caee9ab776a1c2beeb238e0643dbf6f3b7c0a83fd9aa339dc798e2b5272a39f5`  
		Last Modified: Mon, 18 Nov 2024 23:04:06 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ac69faebcdcde53563af6c2f2356011b54221d2d336fa20004d6e41cf7f676c`  
		Last Modified: Mon, 18 Nov 2024 23:04:06 GMT  
		Size: 2.4 MB (2444821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07d3519fedc4d5ee37ea7859c2cedc0f290e072022c6947c318979fd6eb71f55`  
		Last Modified: Mon, 18 Nov 2024 23:04:08 GMT  
		Size: 69.8 MB (69824563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da6fc6e4c616b483bafdc6d886f7d5a5c2d59fcbff06d37f5eec6352e6f45818`  
		Last Modified: Mon, 18 Nov 2024 23:04:06 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:281e39380036537235243436889bf410fd2908fd811d92157772d744f55dba4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1089516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3c515de8cd05e47bd266f48c2b5b5034383aebbc3b2dfc9e9eb1ba756e4d1da`

```dockerfile
```

-	Layers:
	-	`sha256:b6d2654f5db4cef75f0d0dfbaf9b3095359625a64b11278eaa23d00004cd15d9`  
		Last Modified: Mon, 18 Nov 2024 23:04:07 GMT  
		Size: 1.1 MB (1074253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34df0a4ca1bb919a775b446cf53aed82c5c950fb10f80c1950f2a1e0e6e2abdb`  
		Last Modified: Mon, 18 Nov 2024 23:04:06 GMT  
		Size: 15.3 KB (15263 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:360131f2b94e1b4e0a0a55accc6e40255089a89942b6d2d23e682dc769763f34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.5 MB (70488602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d56de21a5014770bd14dd40f920748988275ffe324b3268c2cef771f98132bf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Mon, 28 Oct 2024 22:11:39 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
ENV TELEGRAF_VERSION=1.32.2
# Mon, 28 Oct 2024 22:11:39 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 28 Oct 2024 22:11:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Oct 2024 22:11:39 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9de63ce930d0f77f6402e61ee732ad4f784c59fd26df033bb1b7d6a0b87a2f4`  
		Last Modified: Tue, 12 Nov 2024 13:17:18 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:848dadffeaafa841326acf8c33573919df8ff222e2680607f7d10bb804a23d6c`  
		Last Modified: Wed, 13 Nov 2024 00:44:18 GMT  
		Size: 2.5 MB (2530663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4383827a27cf7c8e76ae40d02da9661a942bebbe18254b9be04d527bce572de5`  
		Last Modified: Wed, 13 Nov 2024 00:45:35 GMT  
		Size: 63.9 MB (63869605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98293dc53f9f009ae42c20ca72b06e353c3ce6fbaa9fd797c46aad972fea12e7`  
		Last Modified: Wed, 13 Nov 2024 00:45:33 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:195d46a82a6c805c64e6541bef8cd6d5a323cd483df30830f7862efc8b0a850a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1086100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c86876f9c189bd84719ab02f8fa82628ea72b474c79ac492165966c68f7af49`

```dockerfile
```

-	Layers:
	-	`sha256:f52cb10165d665b2775de9498b738fbda072838abd2ba18481be987a84e09f3b`  
		Last Modified: Wed, 13 Nov 2024 00:45:33 GMT  
		Size: 1.1 MB (1070715 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:701181e3f6633764e305402b4491f468e9add860351d9ac3ebad727e1e6c9277`  
		Last Modified: Wed, 13 Nov 2024 00:45:33 GMT  
		Size: 15.4 KB (15385 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:latest`

```console
$ docker pull telegraf@sha256:b1e028a8d5b2dbef4023ae0b80c0648696095a13843e9fd54ad30454d842af1d
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
$ docker pull telegraf@sha256:26ab32d6baa5d88a74f3c026969113065f921f45c429648004b1c80445308307
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.6 MB (162605552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c413022d422ab762bbbe969ae0933eaeb95575339550b95785e7c7bd9d2981b6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 Nov 2024 20:48:32 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 Nov 2024 20:48:32 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 18 Nov 2024 20:48:32 GMT
ENV TELEGRAF_VERSION=1.32.3
# Mon, 18 Nov 2024 20:48:32 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 18 Nov 2024 20:48:32 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 18 Nov 2024 20:48:32 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 18 Nov 2024 20:48:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 18 Nov 2024 20:48:32 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:b2b31b28ee3c96e96195c754f8679f690db4b18e475682d716122016ef056f39`  
		Last Modified: Tue, 12 Nov 2024 00:55:23 GMT  
		Size: 49.6 MB (49575695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3cc7b6f04730c072f8b292917e0d95bb886096a2b2b1781196170965161cd27`  
		Last Modified: Tue, 12 Nov 2024 02:38:12 GMT  
		Size: 24.1 MB (24058346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:010db0dbba3535b069ec123d815169b81b7a846befaf2f7f11071758e977afb8`  
		Last Modified: Mon, 18 Nov 2024 23:04:15 GMT  
		Size: 18.9 MB (18948023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fbe67aa00e7a7e452eef611480413f250f464b9d2d2e1cf8b61861ffb410289`  
		Last Modified: Mon, 18 Nov 2024 23:04:12 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4d7830fa54859d2cab67010b9fa1b43d31af49b0cb443b332e89757194f5a80`  
		Last Modified: Mon, 18 Nov 2024 23:04:15 GMT  
		Size: 70.0 MB (70021078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b39496eca681636463ce8350a89dd92aee8f8d2b405b7278659ea5e976890ba8`  
		Last Modified: Mon, 18 Nov 2024 23:04:13 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:f8069a5cfc706a1f70331bb38f7088cc52071e927cf23ad2965ac31e1112cbb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6443002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dda0992c700b7338e9f6e2920a0d7e6c08b358b5084b2dbeb0f1f1904a39086a`

```dockerfile
```

-	Layers:
	-	`sha256:d9eccfe45f5f72667eaa344fe58ab1a4de11b29f18d0108696482aa1f5d12be8`  
		Last Modified: Mon, 18 Nov 2024 23:04:13 GMT  
		Size: 6.4 MB (6428231 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:984633f68829e1d69cf10b19ef022bcc5a0d0d346e20f73758fe2e9d0ff1d80f`  
		Last Modified: Mon, 18 Nov 2024 23:04:12 GMT  
		Size: 14.8 KB (14771 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:2652b91639669f475dcbafa85d5ceb407b4e5f5048ac1bae42fb5111a1574fad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.5 MB (149521208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ee0e34e51635b65425f13e5466fd55a7e9b870199cf0af36b911845e252c33c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 Nov 2024 20:48:32 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 Nov 2024 20:48:32 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 18 Nov 2024 20:48:32 GMT
ENV TELEGRAF_VERSION=1.32.3
# Mon, 18 Nov 2024 20:48:32 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 18 Nov 2024 20:48:32 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 18 Nov 2024 20:48:32 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 18 Nov 2024 20:48:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 18 Nov 2024 20:48:32 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:46618ec96098836cac7950050ba554a969ebf8e9938d85d5f0d97015d3d25076`  
		Last Modified: Tue, 12 Nov 2024 00:56:14 GMT  
		Size: 45.2 MB (45150563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df9660b2b46aa0c77f5dd078f4e57432faf3dbcda91672b9e3f8c1b7892e0ee2`  
		Last Modified: Tue, 12 Nov 2024 15:59:18 GMT  
		Size: 22.0 MB (21960017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52c1519b04115013f7821f6b8398475148c7865994c7c5de2fb71d5916d5fb2e`  
		Last Modified: Wed, 13 Nov 2024 10:41:21 GMT  
		Size: 17.7 MB (17725323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a1859599b084be651ec09e42d0c7674081d74a573bd8eb676cc088609c1a1ed`  
		Last Modified: Wed, 13 Nov 2024 10:41:21 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82bc73ed1aaf2e0fee0d7200d13d2f068a225cf6b26b40a5f955694865b8c8cc`  
		Last Modified: Mon, 18 Nov 2024 23:04:12 GMT  
		Size: 64.7 MB (64682909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96c009391f91b8895de1428a5cfbe7014c5d0674f9bc7bcf35dafc55bfa9fcfc`  
		Last Modified: Mon, 18 Nov 2024 23:04:10 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:7c1f5dc1ef14ae1e81c1073d52d1f1c9cc0e5d2b5c8fc4859ddbd3eaad79def4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6438541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ec659d8892cbf34142ad5feb5c816f440a4c1a82e16696794ec671aaa51eb3c`

```dockerfile
```

-	Layers:
	-	`sha256:d1c124d3335a2c3aa178c49bd4dfce25b32a69478154254a7d44c040a5323ed3`  
		Last Modified: Mon, 18 Nov 2024 23:04:10 GMT  
		Size: 6.4 MB (6423675 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f10b0c590cdddd17bfac9a645ec5e1bc2dd583f281d32c22e76209aa449e28d3`  
		Last Modified: Mon, 18 Nov 2024 23:04:10 GMT  
		Size: 14.9 KB (14866 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:46eb951e12350a8349a9eab22a97e879bf9844372861a6ca57e2a54b229c7de4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.1 MB (156120112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c067c20c86a405bc577d24fb4f24730ded5b75885b386f3d028c7dc4b4d0f431`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
ENV TELEGRAF_VERSION=1.32.2
# Mon, 28 Oct 2024 22:11:39 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 28 Oct 2024 22:11:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Oct 2024 22:11:39 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:1a3f1864ec54b1398987bbe673e93d8b09842ecd51e86ab87d64857b70d188b1`  
		Last Modified: Tue, 12 Nov 2024 00:56:20 GMT  
		Size: 49.6 MB (49587201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:464f864cfaa846fbe1b8a889827404e18374f805d29d77c288a813ae8c4f6d91`  
		Last Modified: Tue, 12 Nov 2024 11:16:03 GMT  
		Size: 23.6 MB (23598253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d5aa793fe0445bc976082730ff6252895e46f7493850ef83f0509f98888fbcd`  
		Last Modified: Wed, 13 Nov 2024 06:19:22 GMT  
		Size: 18.9 MB (18870770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0541e3db3bb997348b43ecd98354da9cfea19cd50420a6ecef282eeb79d54dd`  
		Last Modified: Wed, 13 Nov 2024 06:19:21 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ecba7ebf10b2dda935eee1767535659f3aaec3e27554fd339930447ce495751`  
		Last Modified: Wed, 13 Nov 2024 06:20:49 GMT  
		Size: 64.1 MB (64061480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dceae68a9917b8fc00f1cf8405e8983aeb139626a6cde54bfc9c7c392e08d11`  
		Last Modified: Wed, 13 Nov 2024 06:20:47 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:e98272684f7bc4e923fe35844923fe23dd6ad9c7b0617532d4d291b0c8dce201
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6444639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e2c30cdaeef6af84296cecd84e8795ecf394961e8953d4292d1862904e7c3ed`

```dockerfile
```

-	Layers:
	-	`sha256:7ff334f246f441b9760c06c58f4f71e958140a28715d02c3bc2941cd386561b2`  
		Last Modified: Wed, 13 Nov 2024 06:20:47 GMT  
		Size: 6.4 MB (6429746 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19342b085c35118dc66d01ba39202ee177c1430e22e84dbebac83d959314e441`  
		Last Modified: Wed, 13 Nov 2024 06:20:47 GMT  
		Size: 14.9 KB (14893 bytes)  
		MIME: application/vnd.in-toto+json
