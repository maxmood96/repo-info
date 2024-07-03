<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `telegraf`

-	[`telegraf:1.29`](#telegraf129)
-	[`telegraf:1.29-alpine`](#telegraf129-alpine)
-	[`telegraf:1.29.5`](#telegraf1295)
-	[`telegraf:1.29.5-alpine`](#telegraf1295-alpine)
-	[`telegraf:1.30`](#telegraf130)
-	[`telegraf:1.30-alpine`](#telegraf130-alpine)
-	[`telegraf:1.30.3`](#telegraf1303)
-	[`telegraf:1.30.3-alpine`](#telegraf1303-alpine)
-	[`telegraf:1.31`](#telegraf131)
-	[`telegraf:1.31-alpine`](#telegraf131-alpine)
-	[`telegraf:1.31.1`](#telegraf1311)
-	[`telegraf:1.31.1-alpine`](#telegraf1311-alpine)
-	[`telegraf:alpine`](#telegrafalpine)
-	[`telegraf:latest`](#telegraflatest)

## `telegraf:1.29`

```console
$ docker pull telegraf@sha256:aa2549a0ff1a7447fe3bcccd57aa4639ebe73c66f7f96e62cafe6b7968ea1246
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.29` - linux; amd64

```console
$ docker pull telegraf@sha256:897c17a2c34f54cb6a022ec173880f7f02405b5ec5d5d2a85ccb0a5b80af2d47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.2 MB (155196644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14fccd60b3993e5d5946dd1524e8b5b06628685161eb45be3324a99a95b78659`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 01 Jul 2024 19:20:29 GMT
ADD file:e8aac9b1598114ead96b4038c19d915b87f662ef342291d69c7e5255c5d731fc in / 
# Mon, 01 Jul 2024 19:20:29 GMT
CMD ["bash"]
# Mon, 01 Jul 2024 19:20:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 01 Jul 2024 19:20:29 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 01 Jul 2024 19:20:29 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 01 Jul 2024 19:20:29 GMT
ENV TELEGRAF_VERSION=1.29.5
# Mon, 01 Jul 2024 19:20:29 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 01 Jul 2024 19:20:29 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 01 Jul 2024 19:20:29 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 01 Jul 2024 19:20:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 01 Jul 2024 19:20:29 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:e9aef93137af6e967e7242f3b3c8ecd8e6f571d1e6fdd9e72db0befeeae3cf13`  
		Last Modified: Tue, 02 Jul 2024 01:28:26 GMT  
		Size: 49.6 MB (49554064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58b365fa3e8dc16e70d89fab0e91f5242feb38ae3cfeb6655e654209ea109333`  
		Last Modified: Tue, 02 Jul 2024 02:00:17 GMT  
		Size: 24.0 MB (24049794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b01edb9ec64b0b954bbea8260b13e3cff24ab2266e8154e7da7e6fd89d55139`  
		Last Modified: Tue, 02 Jul 2024 03:15:10 GMT  
		Size: 18.9 MB (18947914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69dd3e5cc7c577a448ae9dea947b7de855835839ef25adcd6fa614a44eacf6e9`  
		Last Modified: Tue, 02 Jul 2024 03:15:09 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec642ba15ef8b93e8dde95fa0ec91f46b174e375c88f70cd4dfcc599a39cc31a`  
		Last Modified: Tue, 02 Jul 2024 03:15:10 GMT  
		Size: 62.6 MB (62642479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c97eb0fc449238a8646274b98f0a269733cae8a9eb903ac344793d2cafdea24d`  
		Last Modified: Tue, 02 Jul 2024 03:15:09 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.29` - unknown; unknown

```console
$ docker pull telegraf@sha256:ea711398623dec31a7370facf2b3fa413e91a0f85367031edafe91caaa11efde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6312751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:057efb115f5c692ba6bec7409df9d905681bddf78892d95565880ddecb838586`

```dockerfile
```

-	Layers:
	-	`sha256:63f7a3eafbb9e5bddaaf5b0b503e5babbd9c7adbc2fc902a1ae854c937499273`  
		Last Modified: Tue, 02 Jul 2024 03:15:09 GMT  
		Size: 6.3 MB (6298427 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa0ea84312aeda58e533afa9e47437be32018b610557d8c2810680c32ade322d`  
		Last Modified: Tue, 02 Jul 2024 03:15:09 GMT  
		Size: 14.3 KB (14324 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.29` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:5093cadb9c5cc125d4486626a00b625d6e4343e763022b114a61cb9e26ee238b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.8 MB (142814327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:900f50b62a0eb2c505edb703bdaeb1dc3bb288f9fa1f06ecced9caff95fc1656`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 01 Jul 2024 19:20:29 GMT
ADD file:526dbb34ac449ae8f3c9025d71b3ffeb0e24fa5dc1a01da707f0a8b834eb4e33 in / 
# Mon, 01 Jul 2024 19:20:29 GMT
CMD ["bash"]
# Mon, 01 Jul 2024 19:20:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 01 Jul 2024 19:20:29 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 01 Jul 2024 19:20:29 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 01 Jul 2024 19:20:29 GMT
ENV TELEGRAF_VERSION=1.29.5
# Mon, 01 Jul 2024 19:20:29 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 01 Jul 2024 19:20:29 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 01 Jul 2024 19:20:29 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 01 Jul 2024 19:20:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 01 Jul 2024 19:20:29 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:335f2c484898b910fac13d5650ed3c78e5e673fe8dab1b06a071c71478a153d0`  
		Last Modified: Tue, 02 Jul 2024 01:02:57 GMT  
		Size: 45.1 MB (45148097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aa30b2bcbde45c2fc67abf425197af3af3e67d55296f168143343ef1b0e2d3e`  
		Last Modified: Tue, 02 Jul 2024 01:39:04 GMT  
		Size: 22.0 MB (21954038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac7a987fd3254b4eb8a2e6cc7206b9d5eac3e938a9d3c13d8fa167031b4fbcce`  
		Last Modified: Wed, 03 Jul 2024 01:34:48 GMT  
		Size: 17.7 MB (17724841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e17cfe5d83da74d5e8c4d81b008e6599fc7cca1105639345e4bf236669c7f0c5`  
		Last Modified: Wed, 03 Jul 2024 01:34:47 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddcf1df454007f974a71e14b2e46859f99ac31d508c0550f70d6dfb977ee686b`  
		Last Modified: Wed, 03 Jul 2024 01:34:49 GMT  
		Size: 58.0 MB (57984941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f18150f999cff9629dd9df7a2f3a2b273acf2e5127190881d8a596262449c0b1`  
		Last Modified: Wed, 03 Jul 2024 01:34:47 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.29` - unknown; unknown

```console
$ docker pull telegraf@sha256:0c8e2c3e12ddf19a2e480758c04b64b9f502cbe4402734bd2f620a3025c3f096
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6308185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8fb621815ac46dad4c61f36a4c6cb010d1e695a30c0430c6add4022b39a4a64`

```dockerfile
```

-	Layers:
	-	`sha256:0be07c235c3580ff48c89677e518be535d7e40449f458152a875fe0c8efb3681`  
		Last Modified: Wed, 03 Jul 2024 01:34:48 GMT  
		Size: 6.3 MB (6293781 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf46b4aa8154890d2f12c4eb1b6898b44c282080716711c654226ec1fb203b8f`  
		Last Modified: Wed, 03 Jul 2024 01:34:47 GMT  
		Size: 14.4 KB (14404 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.29` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:981cc25bec023e8b3aa562a85b8ec346a314d7fc3f1b09c9dc35f11081826a57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.0 MB (149033424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5d61046af06c7c8dce28363b8025db4864be5c917909984b7ff7350029fdea0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 01 Jul 2024 19:20:29 GMT
ADD file:696648070a57689a69a184fda234045f7be4a8a9f3b2fff9031ff0a2d9914113 in / 
# Mon, 01 Jul 2024 19:20:29 GMT
CMD ["bash"]
# Mon, 01 Jul 2024 19:20:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 01 Jul 2024 19:20:29 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 01 Jul 2024 19:20:29 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 01 Jul 2024 19:20:29 GMT
ENV TELEGRAF_VERSION=1.29.5
# Mon, 01 Jul 2024 19:20:29 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 01 Jul 2024 19:20:29 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 01 Jul 2024 19:20:29 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 01 Jul 2024 19:20:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 01 Jul 2024 19:20:29 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:0bd1f8180c504ba389021ce74895ed487ccd8c70e2d9af3707934bc801ba28d8`  
		Last Modified: Tue, 02 Jul 2024 00:42:03 GMT  
		Size: 49.6 MB (49588448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b16610496e73ba3d120d519598b53fa8a2db4c80ccc097a5016ad44aedd0654b`  
		Last Modified: Tue, 02 Jul 2024 04:01:41 GMT  
		Size: 23.6 MB (23591145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49fa4258ace16a879b6bae48191a62329ef9150aaf9ac97497e6d6c0f3d622aa`  
		Last Modified: Wed, 03 Jul 2024 00:51:44 GMT  
		Size: 18.9 MB (18870342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c86c902d4b3d360929e7f2bfb7aebbb19eb7c0bd8f515cf202c7fe68e2315b58`  
		Last Modified: Wed, 03 Jul 2024 00:51:43 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f305e73468286824509c01bc579f72e5f63bba704827d093567fd35a68bd676`  
		Last Modified: Wed, 03 Jul 2024 00:51:45 GMT  
		Size: 57.0 MB (56981083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7ccb4116e54c87f79eeb0f706c4a196800349d0c77cfc59c6933a6434dcce9e`  
		Last Modified: Wed, 03 Jul 2024 00:51:43 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.29` - unknown; unknown

```console
$ docker pull telegraf@sha256:9d714879819aa68e15b2fb64d87e48601c21246461cfadfe97b7b6fc086b2aec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6313682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fbc747216f89b25cd16e1a988c5cc389fd7b40330971dd6db7f3bc363d9da89`

```dockerfile
```

-	Layers:
	-	`sha256:d7a7d0f68f6a8fde3691bea88c7b4a63a3386e664df60760fe4e7d3a9e72850a`  
		Last Modified: Wed, 03 Jul 2024 00:51:43 GMT  
		Size: 6.3 MB (6299065 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99486cb13e22018b282649e324ae7be1590fc88138f9990993daf02ac88b39c9`  
		Last Modified: Wed, 03 Jul 2024 00:51:43 GMT  
		Size: 14.6 KB (14617 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.29-alpine`

```console
$ docker pull telegraf@sha256:a45a418654e7d83c676a6eaf8f4210a32b629b6a2da4257b89db761aee5e3183
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.29-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:b4d98fbfaf3f1d7ff40ed85c70540146aa0fa4fbbf687468b22f6d1be26ee7a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.5 MB (68518614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1564c81134cb93813370f8f75f08a8ff72d6fe556a6477f8f471a0656ba84285`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 10 Jun 2024 21:05:04 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
# Mon, 10 Jun 2024 21:05:04 GMT
CMD ["/bin/sh"]
# Mon, 10 Jun 2024 21:05:04 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
ENV TELEGRAF_VERSION=1.29.5
# Mon, 10 Jun 2024 21:05:04 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 10 Jun 2024 21:05:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Jun 2024 21:05:04 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75ec0c8543450ee946ac4c2c2f9aae3874329b9df256dec7a2a2a6d7f82239c0`  
		Last Modified: Thu, 20 Jun 2024 20:56:35 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8534341557b73ef6ba41ed2d84c14b991298e80406cf30c829ba55fe6dd531f`  
		Last Modified: Thu, 20 Jun 2024 20:56:36 GMT  
		Size: 2.5 MB (2452641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4f5c878a1912d5951bb711c8ca6e5701e3a41e6303e969b9d649d6eb6cc5e46`  
		Last Modified: Thu, 20 Jun 2024 20:56:37 GMT  
		Size: 62.4 MB (62441523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e19a98d885f59b7a00fd273e5d42a3adbcf0e25041776976d419d67ed1af9dca`  
		Last Modified: Thu, 20 Jun 2024 20:56:36 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.29-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:4038f9156f61acbb53b9b11ee502dfe0b780778414853776fb72b398a3e2292f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1001195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39f1c3562eeafe030c5c11fd3b202e29dcc941762f0295b8cf5d16e2dc380849`

```dockerfile
```

-	Layers:
	-	`sha256:f0cae03b640a9f603aae38824edacff44ff1270375fe427c4616ae3a52e9a999`  
		Last Modified: Thu, 20 Jun 2024 20:56:36 GMT  
		Size: 986.5 KB (986461 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7d6dfd596bbf816398bc597d3fbf1e07a5b42d4be22a9ac110ab19f5dde9e84`  
		Last Modified: Thu, 20 Jun 2024 20:56:36 GMT  
		Size: 14.7 KB (14734 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.29-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:b7489cc89bfbb3afc64cc0793f8fbab9518ec171300f43ebc2a54910a1fe3230
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.4 MB (63409663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b08dcf16d2d6c13b7f338d440e32ce6090f8dcb04751cfe89b432933d216749`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 10 Jun 2024 21:05:04 GMT
ADD file:033626ac44156f3d5800a602c46870486b1492b9ba26096eaa66cceb6fcead77 in / 
# Mon, 10 Jun 2024 21:05:04 GMT
CMD ["/bin/sh"]
# Mon, 10 Jun 2024 21:05:04 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
ENV TELEGRAF_VERSION=1.29.5
# Mon, 10 Jun 2024 21:05:04 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 10 Jun 2024 21:05:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Jun 2024 21:05:04 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:a258b2a6b59a7aa244d8ceab095c7f8df726f27075a69fca7ad8490f3f63148a`  
		Last Modified: Thu, 20 Jun 2024 17:40:58 GMT  
		Size: 4.1 MB (4088800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe4d02fd6d451824a88c3da056c35af5ef536e8a634a98239ab90c650e0518e3`  
		Last Modified: Fri, 21 Jun 2024 05:12:50 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c75d4393617a41a89527ad46200950f81c7c7993bd950a78413ef7d03b012113`  
		Last Modified: Fri, 21 Jun 2024 07:01:17 GMT  
		Size: 2.5 MB (2539706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c47c4e323f89c2384b089a00b5839fef87d6d056002482c0b5a22f16c82591b0`  
		Last Modified: Fri, 21 Jun 2024 07:01:18 GMT  
		Size: 56.8 MB (56780548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cc69c6a8c13d94f9a7918c8e2e35a98316ac001c4dd518830eabf4be200e719`  
		Last Modified: Fri, 21 Jun 2024 07:01:17 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.29-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:acd007149b6c53fcc9954bf1954aa3e170d017d3cc5262c637fb99e5c9c3ac49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **997.1 KB (997056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3d60c41b16981197be52d5b58d9375d085534cfcd7d9011770d3c335620024f`

```dockerfile
```

-	Layers:
	-	`sha256:a420d692f20432c4fa2c0cc78f826bc1c840c30e2d680d3460871ae0ed0e9577`  
		Last Modified: Fri, 21 Jun 2024 07:01:17 GMT  
		Size: 982.0 KB (982046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b72022ed01d76aa33626ce3346bb33bb260b2175e125d2f891ee54b12100c65c`  
		Last Modified: Fri, 21 Jun 2024 07:01:17 GMT  
		Size: 15.0 KB (15010 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.29.5`

```console
$ docker pull telegraf@sha256:aa2549a0ff1a7447fe3bcccd57aa4639ebe73c66f7f96e62cafe6b7968ea1246
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.29.5` - linux; amd64

```console
$ docker pull telegraf@sha256:897c17a2c34f54cb6a022ec173880f7f02405b5ec5d5d2a85ccb0a5b80af2d47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.2 MB (155196644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14fccd60b3993e5d5946dd1524e8b5b06628685161eb45be3324a99a95b78659`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 01 Jul 2024 19:20:29 GMT
ADD file:e8aac9b1598114ead96b4038c19d915b87f662ef342291d69c7e5255c5d731fc in / 
# Mon, 01 Jul 2024 19:20:29 GMT
CMD ["bash"]
# Mon, 01 Jul 2024 19:20:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 01 Jul 2024 19:20:29 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 01 Jul 2024 19:20:29 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 01 Jul 2024 19:20:29 GMT
ENV TELEGRAF_VERSION=1.29.5
# Mon, 01 Jul 2024 19:20:29 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 01 Jul 2024 19:20:29 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 01 Jul 2024 19:20:29 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 01 Jul 2024 19:20:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 01 Jul 2024 19:20:29 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:e9aef93137af6e967e7242f3b3c8ecd8e6f571d1e6fdd9e72db0befeeae3cf13`  
		Last Modified: Tue, 02 Jul 2024 01:28:26 GMT  
		Size: 49.6 MB (49554064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58b365fa3e8dc16e70d89fab0e91f5242feb38ae3cfeb6655e654209ea109333`  
		Last Modified: Tue, 02 Jul 2024 02:00:17 GMT  
		Size: 24.0 MB (24049794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b01edb9ec64b0b954bbea8260b13e3cff24ab2266e8154e7da7e6fd89d55139`  
		Last Modified: Tue, 02 Jul 2024 03:15:10 GMT  
		Size: 18.9 MB (18947914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69dd3e5cc7c577a448ae9dea947b7de855835839ef25adcd6fa614a44eacf6e9`  
		Last Modified: Tue, 02 Jul 2024 03:15:09 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec642ba15ef8b93e8dde95fa0ec91f46b174e375c88f70cd4dfcc599a39cc31a`  
		Last Modified: Tue, 02 Jul 2024 03:15:10 GMT  
		Size: 62.6 MB (62642479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c97eb0fc449238a8646274b98f0a269733cae8a9eb903ac344793d2cafdea24d`  
		Last Modified: Tue, 02 Jul 2024 03:15:09 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.29.5` - unknown; unknown

```console
$ docker pull telegraf@sha256:ea711398623dec31a7370facf2b3fa413e91a0f85367031edafe91caaa11efde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6312751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:057efb115f5c692ba6bec7409df9d905681bddf78892d95565880ddecb838586`

```dockerfile
```

-	Layers:
	-	`sha256:63f7a3eafbb9e5bddaaf5b0b503e5babbd9c7adbc2fc902a1ae854c937499273`  
		Last Modified: Tue, 02 Jul 2024 03:15:09 GMT  
		Size: 6.3 MB (6298427 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa0ea84312aeda58e533afa9e47437be32018b610557d8c2810680c32ade322d`  
		Last Modified: Tue, 02 Jul 2024 03:15:09 GMT  
		Size: 14.3 KB (14324 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.29.5` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:5093cadb9c5cc125d4486626a00b625d6e4343e763022b114a61cb9e26ee238b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.8 MB (142814327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:900f50b62a0eb2c505edb703bdaeb1dc3bb288f9fa1f06ecced9caff95fc1656`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 01 Jul 2024 19:20:29 GMT
ADD file:526dbb34ac449ae8f3c9025d71b3ffeb0e24fa5dc1a01da707f0a8b834eb4e33 in / 
# Mon, 01 Jul 2024 19:20:29 GMT
CMD ["bash"]
# Mon, 01 Jul 2024 19:20:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 01 Jul 2024 19:20:29 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 01 Jul 2024 19:20:29 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 01 Jul 2024 19:20:29 GMT
ENV TELEGRAF_VERSION=1.29.5
# Mon, 01 Jul 2024 19:20:29 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 01 Jul 2024 19:20:29 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 01 Jul 2024 19:20:29 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 01 Jul 2024 19:20:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 01 Jul 2024 19:20:29 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:335f2c484898b910fac13d5650ed3c78e5e673fe8dab1b06a071c71478a153d0`  
		Last Modified: Tue, 02 Jul 2024 01:02:57 GMT  
		Size: 45.1 MB (45148097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aa30b2bcbde45c2fc67abf425197af3af3e67d55296f168143343ef1b0e2d3e`  
		Last Modified: Tue, 02 Jul 2024 01:39:04 GMT  
		Size: 22.0 MB (21954038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac7a987fd3254b4eb8a2e6cc7206b9d5eac3e938a9d3c13d8fa167031b4fbcce`  
		Last Modified: Wed, 03 Jul 2024 01:34:48 GMT  
		Size: 17.7 MB (17724841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e17cfe5d83da74d5e8c4d81b008e6599fc7cca1105639345e4bf236669c7f0c5`  
		Last Modified: Wed, 03 Jul 2024 01:34:47 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddcf1df454007f974a71e14b2e46859f99ac31d508c0550f70d6dfb977ee686b`  
		Last Modified: Wed, 03 Jul 2024 01:34:49 GMT  
		Size: 58.0 MB (57984941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f18150f999cff9629dd9df7a2f3a2b273acf2e5127190881d8a596262449c0b1`  
		Last Modified: Wed, 03 Jul 2024 01:34:47 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.29.5` - unknown; unknown

```console
$ docker pull telegraf@sha256:0c8e2c3e12ddf19a2e480758c04b64b9f502cbe4402734bd2f620a3025c3f096
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6308185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8fb621815ac46dad4c61f36a4c6cb010d1e695a30c0430c6add4022b39a4a64`

```dockerfile
```

-	Layers:
	-	`sha256:0be07c235c3580ff48c89677e518be535d7e40449f458152a875fe0c8efb3681`  
		Last Modified: Wed, 03 Jul 2024 01:34:48 GMT  
		Size: 6.3 MB (6293781 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf46b4aa8154890d2f12c4eb1b6898b44c282080716711c654226ec1fb203b8f`  
		Last Modified: Wed, 03 Jul 2024 01:34:47 GMT  
		Size: 14.4 KB (14404 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.29.5` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:981cc25bec023e8b3aa562a85b8ec346a314d7fc3f1b09c9dc35f11081826a57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.0 MB (149033424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5d61046af06c7c8dce28363b8025db4864be5c917909984b7ff7350029fdea0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 01 Jul 2024 19:20:29 GMT
ADD file:696648070a57689a69a184fda234045f7be4a8a9f3b2fff9031ff0a2d9914113 in / 
# Mon, 01 Jul 2024 19:20:29 GMT
CMD ["bash"]
# Mon, 01 Jul 2024 19:20:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 01 Jul 2024 19:20:29 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 01 Jul 2024 19:20:29 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 01 Jul 2024 19:20:29 GMT
ENV TELEGRAF_VERSION=1.29.5
# Mon, 01 Jul 2024 19:20:29 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 01 Jul 2024 19:20:29 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 01 Jul 2024 19:20:29 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 01 Jul 2024 19:20:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 01 Jul 2024 19:20:29 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:0bd1f8180c504ba389021ce74895ed487ccd8c70e2d9af3707934bc801ba28d8`  
		Last Modified: Tue, 02 Jul 2024 00:42:03 GMT  
		Size: 49.6 MB (49588448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b16610496e73ba3d120d519598b53fa8a2db4c80ccc097a5016ad44aedd0654b`  
		Last Modified: Tue, 02 Jul 2024 04:01:41 GMT  
		Size: 23.6 MB (23591145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49fa4258ace16a879b6bae48191a62329ef9150aaf9ac97497e6d6c0f3d622aa`  
		Last Modified: Wed, 03 Jul 2024 00:51:44 GMT  
		Size: 18.9 MB (18870342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c86c902d4b3d360929e7f2bfb7aebbb19eb7c0bd8f515cf202c7fe68e2315b58`  
		Last Modified: Wed, 03 Jul 2024 00:51:43 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f305e73468286824509c01bc579f72e5f63bba704827d093567fd35a68bd676`  
		Last Modified: Wed, 03 Jul 2024 00:51:45 GMT  
		Size: 57.0 MB (56981083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7ccb4116e54c87f79eeb0f706c4a196800349d0c77cfc59c6933a6434dcce9e`  
		Last Modified: Wed, 03 Jul 2024 00:51:43 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.29.5` - unknown; unknown

```console
$ docker pull telegraf@sha256:9d714879819aa68e15b2fb64d87e48601c21246461cfadfe97b7b6fc086b2aec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6313682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fbc747216f89b25cd16e1a988c5cc389fd7b40330971dd6db7f3bc363d9da89`

```dockerfile
```

-	Layers:
	-	`sha256:d7a7d0f68f6a8fde3691bea88c7b4a63a3386e664df60760fe4e7d3a9e72850a`  
		Last Modified: Wed, 03 Jul 2024 00:51:43 GMT  
		Size: 6.3 MB (6299065 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99486cb13e22018b282649e324ae7be1590fc88138f9990993daf02ac88b39c9`  
		Last Modified: Wed, 03 Jul 2024 00:51:43 GMT  
		Size: 14.6 KB (14617 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.29.5-alpine`

```console
$ docker pull telegraf@sha256:a45a418654e7d83c676a6eaf8f4210a32b629b6a2da4257b89db761aee5e3183
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.29.5-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:b4d98fbfaf3f1d7ff40ed85c70540146aa0fa4fbbf687468b22f6d1be26ee7a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.5 MB (68518614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1564c81134cb93813370f8f75f08a8ff72d6fe556a6477f8f471a0656ba84285`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 10 Jun 2024 21:05:04 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
# Mon, 10 Jun 2024 21:05:04 GMT
CMD ["/bin/sh"]
# Mon, 10 Jun 2024 21:05:04 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
ENV TELEGRAF_VERSION=1.29.5
# Mon, 10 Jun 2024 21:05:04 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 10 Jun 2024 21:05:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Jun 2024 21:05:04 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75ec0c8543450ee946ac4c2c2f9aae3874329b9df256dec7a2a2a6d7f82239c0`  
		Last Modified: Thu, 20 Jun 2024 20:56:35 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8534341557b73ef6ba41ed2d84c14b991298e80406cf30c829ba55fe6dd531f`  
		Last Modified: Thu, 20 Jun 2024 20:56:36 GMT  
		Size: 2.5 MB (2452641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4f5c878a1912d5951bb711c8ca6e5701e3a41e6303e969b9d649d6eb6cc5e46`  
		Last Modified: Thu, 20 Jun 2024 20:56:37 GMT  
		Size: 62.4 MB (62441523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e19a98d885f59b7a00fd273e5d42a3adbcf0e25041776976d419d67ed1af9dca`  
		Last Modified: Thu, 20 Jun 2024 20:56:36 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.29.5-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:4038f9156f61acbb53b9b11ee502dfe0b780778414853776fb72b398a3e2292f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1001195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39f1c3562eeafe030c5c11fd3b202e29dcc941762f0295b8cf5d16e2dc380849`

```dockerfile
```

-	Layers:
	-	`sha256:f0cae03b640a9f603aae38824edacff44ff1270375fe427c4616ae3a52e9a999`  
		Last Modified: Thu, 20 Jun 2024 20:56:36 GMT  
		Size: 986.5 KB (986461 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7d6dfd596bbf816398bc597d3fbf1e07a5b42d4be22a9ac110ab19f5dde9e84`  
		Last Modified: Thu, 20 Jun 2024 20:56:36 GMT  
		Size: 14.7 KB (14734 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.29.5-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:b7489cc89bfbb3afc64cc0793f8fbab9518ec171300f43ebc2a54910a1fe3230
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.4 MB (63409663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b08dcf16d2d6c13b7f338d440e32ce6090f8dcb04751cfe89b432933d216749`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 10 Jun 2024 21:05:04 GMT
ADD file:033626ac44156f3d5800a602c46870486b1492b9ba26096eaa66cceb6fcead77 in / 
# Mon, 10 Jun 2024 21:05:04 GMT
CMD ["/bin/sh"]
# Mon, 10 Jun 2024 21:05:04 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
ENV TELEGRAF_VERSION=1.29.5
# Mon, 10 Jun 2024 21:05:04 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 10 Jun 2024 21:05:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Jun 2024 21:05:04 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:a258b2a6b59a7aa244d8ceab095c7f8df726f27075a69fca7ad8490f3f63148a`  
		Last Modified: Thu, 20 Jun 2024 17:40:58 GMT  
		Size: 4.1 MB (4088800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe4d02fd6d451824a88c3da056c35af5ef536e8a634a98239ab90c650e0518e3`  
		Last Modified: Fri, 21 Jun 2024 05:12:50 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c75d4393617a41a89527ad46200950f81c7c7993bd950a78413ef7d03b012113`  
		Last Modified: Fri, 21 Jun 2024 07:01:17 GMT  
		Size: 2.5 MB (2539706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c47c4e323f89c2384b089a00b5839fef87d6d056002482c0b5a22f16c82591b0`  
		Last Modified: Fri, 21 Jun 2024 07:01:18 GMT  
		Size: 56.8 MB (56780548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cc69c6a8c13d94f9a7918c8e2e35a98316ac001c4dd518830eabf4be200e719`  
		Last Modified: Fri, 21 Jun 2024 07:01:17 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.29.5-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:acd007149b6c53fcc9954bf1954aa3e170d017d3cc5262c637fb99e5c9c3ac49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **997.1 KB (997056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3d60c41b16981197be52d5b58d9375d085534cfcd7d9011770d3c335620024f`

```dockerfile
```

-	Layers:
	-	`sha256:a420d692f20432c4fa2c0cc78f826bc1c840c30e2d680d3460871ae0ed0e9577`  
		Last Modified: Fri, 21 Jun 2024 07:01:17 GMT  
		Size: 982.0 KB (982046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b72022ed01d76aa33626ce3346bb33bb260b2175e125d2f891ee54b12100c65c`  
		Last Modified: Fri, 21 Jun 2024 07:01:17 GMT  
		Size: 15.0 KB (15010 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.30`

```console
$ docker pull telegraf@sha256:2abea02b6e577938131b83fecc83964539477d621acfe7134306b7542eb540b5
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
$ docker pull telegraf@sha256:f73ff0e0b13f014ccabcde4195e44a975e6cbd92813606cdcb71522c57e2ba5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.3 MB (155320684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c8deb06ed042a928956d9ce5e5a2470daae87404cf02dccbfd37ca6f5fb177c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 01 Jul 2024 19:20:29 GMT
ADD file:e8aac9b1598114ead96b4038c19d915b87f662ef342291d69c7e5255c5d731fc in / 
# Mon, 01 Jul 2024 19:20:29 GMT
CMD ["bash"]
# Mon, 01 Jul 2024 19:20:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 01 Jul 2024 19:20:29 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 01 Jul 2024 19:20:29 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 01 Jul 2024 19:20:29 GMT
ENV TELEGRAF_VERSION=1.30.3
# Mon, 01 Jul 2024 19:20:29 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 01 Jul 2024 19:20:29 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 01 Jul 2024 19:20:29 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 01 Jul 2024 19:20:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 01 Jul 2024 19:20:29 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:e9aef93137af6e967e7242f3b3c8ecd8e6f571d1e6fdd9e72db0befeeae3cf13`  
		Last Modified: Tue, 02 Jul 2024 01:28:26 GMT  
		Size: 49.6 MB (49554064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58b365fa3e8dc16e70d89fab0e91f5242feb38ae3cfeb6655e654209ea109333`  
		Last Modified: Tue, 02 Jul 2024 02:00:17 GMT  
		Size: 24.0 MB (24049794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5da89946764fe6bc921e753ff7761fdb24625e8d8a07165504de7111f8274324`  
		Last Modified: Tue, 02 Jul 2024 03:15:27 GMT  
		Size: 18.9 MB (18947987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d0ed75ef4d83b1fc9916de999fffb31b9d202dd97e63299228bc50a745abb4d`  
		Last Modified: Tue, 02 Jul 2024 03:15:27 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26b0d0ebc88ae7933e7aa23a67dc168c230dd1dcc529768c1295e92049a48d46`  
		Last Modified: Tue, 02 Jul 2024 03:15:28 GMT  
		Size: 62.8 MB (62766444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e5489c87b9807b63efbdda8579e0d344e48000e436195a6e16797b2cd68b07c`  
		Last Modified: Tue, 02 Jul 2024 03:15:27 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.30` - unknown; unknown

```console
$ docker pull telegraf@sha256:1089c75e9f7745b1ed28464fe06d3723fef1524114df41345d7537306ed4901e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6313031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28bf0f3519c0bbf553c4bb7cdecded651ab2d5e38747485c75e33e92506dc2c9`

```dockerfile
```

-	Layers:
	-	`sha256:d572c57273bcfe0c2d47035ab9cc309404ff7a3b1c450e0937846f7203a136b7`  
		Last Modified: Tue, 02 Jul 2024 03:15:27 GMT  
		Size: 6.3 MB (6298707 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6d5c8d609a2f18588d8963f7c5b49e56d882946f44e02adffcfa76067c84d4d`  
		Last Modified: Tue, 02 Jul 2024 03:15:27 GMT  
		Size: 14.3 KB (14324 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.30` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:e6b6a03a34cffc85ca6bcf4c71f4351a57d3224891ba0aa9220429632ab865f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.0 MB (143042022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:842d5bbe61154b5ce2ff8ed5e3b51057ad021f9c044c13e0a69690f32b96de35`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 01 Jul 2024 19:20:29 GMT
ADD file:526dbb34ac449ae8f3c9025d71b3ffeb0e24fa5dc1a01da707f0a8b834eb4e33 in / 
# Mon, 01 Jul 2024 19:20:29 GMT
CMD ["bash"]
# Mon, 01 Jul 2024 19:20:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 01 Jul 2024 19:20:29 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 01 Jul 2024 19:20:29 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 01 Jul 2024 19:20:29 GMT
ENV TELEGRAF_VERSION=1.30.3
# Mon, 01 Jul 2024 19:20:29 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 01 Jul 2024 19:20:29 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 01 Jul 2024 19:20:29 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 01 Jul 2024 19:20:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 01 Jul 2024 19:20:29 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:335f2c484898b910fac13d5650ed3c78e5e673fe8dab1b06a071c71478a153d0`  
		Last Modified: Tue, 02 Jul 2024 01:02:57 GMT  
		Size: 45.1 MB (45148097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aa30b2bcbde45c2fc67abf425197af3af3e67d55296f168143343ef1b0e2d3e`  
		Last Modified: Tue, 02 Jul 2024 01:39:04 GMT  
		Size: 22.0 MB (21954038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac7a987fd3254b4eb8a2e6cc7206b9d5eac3e938a9d3c13d8fa167031b4fbcce`  
		Last Modified: Wed, 03 Jul 2024 01:34:48 GMT  
		Size: 17.7 MB (17724841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e17cfe5d83da74d5e8c4d81b008e6599fc7cca1105639345e4bf236669c7f0c5`  
		Last Modified: Wed, 03 Jul 2024 01:34:47 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31604fe832b771fdfc0f57206b12dc1e97a61e92e19904e3eeadac79dcfe3606`  
		Last Modified: Wed, 03 Jul 2024 01:35:46 GMT  
		Size: 58.2 MB (58212636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10093f2352b79e66ceb029afc2305de76684b93675bd445148a5cc9dcff9618f`  
		Last Modified: Wed, 03 Jul 2024 01:35:44 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.30` - unknown; unknown

```console
$ docker pull telegraf@sha256:bea64ec9cc31676dd3fee1dd7b6eb0aa254afad308d6c8e943d0b5c884f70c17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6308465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c0f15de22e1d60de199faf973a835e9571c4c91ccd75f5f6a4ff5326968d985`

```dockerfile
```

-	Layers:
	-	`sha256:7899a503f349afc059a73a696098fa8dc056bdecfa2cb6e59c78476735d27310`  
		Last Modified: Wed, 03 Jul 2024 01:35:44 GMT  
		Size: 6.3 MB (6294061 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07452d604d36664587ed6a5966b02fe03f53d59715a8bb21fc5c65c503664243`  
		Last Modified: Wed, 03 Jul 2024 01:35:44 GMT  
		Size: 14.4 KB (14404 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.30` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:461d5e652edda6eee02ee4b136447d4838a9e7a56b331659bd3e2e9b236e12a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.2 MB (149175580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb7430674a24c6da24b76c10cdedff842a2209505b3c307ab14c4bbe4e60f57c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 01 Jul 2024 19:20:29 GMT
ADD file:696648070a57689a69a184fda234045f7be4a8a9f3b2fff9031ff0a2d9914113 in / 
# Mon, 01 Jul 2024 19:20:29 GMT
CMD ["bash"]
# Mon, 01 Jul 2024 19:20:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 01 Jul 2024 19:20:29 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 01 Jul 2024 19:20:29 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 01 Jul 2024 19:20:29 GMT
ENV TELEGRAF_VERSION=1.30.3
# Mon, 01 Jul 2024 19:20:29 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 01 Jul 2024 19:20:29 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 01 Jul 2024 19:20:29 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 01 Jul 2024 19:20:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 01 Jul 2024 19:20:29 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:0bd1f8180c504ba389021ce74895ed487ccd8c70e2d9af3707934bc801ba28d8`  
		Last Modified: Tue, 02 Jul 2024 00:42:03 GMT  
		Size: 49.6 MB (49588448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b16610496e73ba3d120d519598b53fa8a2db4c80ccc097a5016ad44aedd0654b`  
		Last Modified: Tue, 02 Jul 2024 04:01:41 GMT  
		Size: 23.6 MB (23591145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49fa4258ace16a879b6bae48191a62329ef9150aaf9ac97497e6d6c0f3d622aa`  
		Last Modified: Wed, 03 Jul 2024 00:51:44 GMT  
		Size: 18.9 MB (18870342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c86c902d4b3d360929e7f2bfb7aebbb19eb7c0bd8f515cf202c7fe68e2315b58`  
		Last Modified: Wed, 03 Jul 2024 00:51:43 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ac8c25bdfdab25b547db505539bd2fd37ce75df8f18e7c0ab0f54bbdc2ccaf9`  
		Last Modified: Wed, 03 Jul 2024 00:52:23 GMT  
		Size: 57.1 MB (57123239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:579a549f635d458174ccd9012b15f0520e9d6f7968c8a41b85bcd6c655163306`  
		Last Modified: Wed, 03 Jul 2024 00:52:21 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.30` - unknown; unknown

```console
$ docker pull telegraf@sha256:04e4e275a7b3a7b9af5825abaf2eedf4f98dae987a0db48a7500f16d0cfcb5f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6313962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88e87f495c8d1975910a9b54b973571a8a5a0d2d4319dc27b8df8c7f7a6eb455`

```dockerfile
```

-	Layers:
	-	`sha256:be545d25107ef0652b891b232e09d106529d96b4f8b31f8d53e21ffcd358e2d0`  
		Last Modified: Wed, 03 Jul 2024 00:52:21 GMT  
		Size: 6.3 MB (6299345 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49f4c3aab6ccdf973e4787db7c17b8db477dd8d7930b95f3b521f971756d2828`  
		Last Modified: Wed, 03 Jul 2024 00:52:20 GMT  
		Size: 14.6 KB (14617 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.30-alpine`

```console
$ docker pull telegraf@sha256:a2ed1c626f31e48a36261fb87b45435d08df5c8da8f8deef0aa567dd54e0fa8c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.30-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:7d9dd9a8d17927b5ab64f2b5ab5d753392bb6f602fa6926d9081256ad66894f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.6 MB (68645907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c78422aae7eb12bd23f41bce4cb35583613d09d7f9f20a343bd2110d44d1408`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 10 Jun 2024 21:05:04 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
# Mon, 10 Jun 2024 21:05:04 GMT
CMD ["/bin/sh"]
# Mon, 10 Jun 2024 21:05:04 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
ENV TELEGRAF_VERSION=1.30.3
# Mon, 10 Jun 2024 21:05:04 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 10 Jun 2024 21:05:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Jun 2024 21:05:04 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:854692264f8809cf92629e7525eb2598493eae4136d97f12ba8db44a2957cb6a`  
		Last Modified: Thu, 20 Jun 2024 20:56:40 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f81fa91f596181920960e72a6871a7fbfd31377b83e4d7ecdd55850dba219e7`  
		Last Modified: Thu, 20 Jun 2024 20:56:40 GMT  
		Size: 2.5 MB (2452628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5989c1129b25207a17de9c1e2b3b4d9bb5e4fa649a47321695b750cacd317a6b`  
		Last Modified: Thu, 20 Jun 2024 20:56:41 GMT  
		Size: 62.6 MB (62568829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8194eec5904ba428ad67b75aabc1dcc4ec6535ed0da6072bf4cbc796f12edf2f`  
		Last Modified: Thu, 20 Jun 2024 20:56:40 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.30-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:ec438523f550864f5f8cde1a61b9cb8dcafd1ce5b8e7039c9ca4358ff1d5688c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1001473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a99b04efa643dcbf93abeb20c32c100ab442b5c97962b86919ffda7368edf4f1`

```dockerfile
```

-	Layers:
	-	`sha256:ed43db3ec20a6ba58ead7a069a1bf3aa51caa9afdd7e617641224fdd0c9864f6`  
		Last Modified: Thu, 20 Jun 2024 20:56:40 GMT  
		Size: 986.7 KB (986741 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e2212a71037664885b4644cfe397c388c4704a4a706dcee39402e20ef0035c3`  
		Last Modified: Thu, 20 Jun 2024 20:56:40 GMT  
		Size: 14.7 KB (14732 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.30-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:669deff433f02f6cacdd048db7d127be4525d4dbe2db1a46f64ff6871a2341be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.6 MB (63550043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b3dfe6b665f35c9e2fa07a7dba07cabfb44eec39975e2e76fb054559813bbea`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 10 Jun 2024 21:05:04 GMT
ADD file:033626ac44156f3d5800a602c46870486b1492b9ba26096eaa66cceb6fcead77 in / 
# Mon, 10 Jun 2024 21:05:04 GMT
CMD ["/bin/sh"]
# Mon, 10 Jun 2024 21:05:04 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
ENV TELEGRAF_VERSION=1.30.3
# Mon, 10 Jun 2024 21:05:04 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 10 Jun 2024 21:05:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Jun 2024 21:05:04 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:a258b2a6b59a7aa244d8ceab095c7f8df726f27075a69fca7ad8490f3f63148a`  
		Last Modified: Thu, 20 Jun 2024 17:40:58 GMT  
		Size: 4.1 MB (4088800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe4d02fd6d451824a88c3da056c35af5ef536e8a634a98239ab90c650e0518e3`  
		Last Modified: Fri, 21 Jun 2024 05:12:50 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c75d4393617a41a89527ad46200950f81c7c7993bd950a78413ef7d03b012113`  
		Last Modified: Fri, 21 Jun 2024 07:01:17 GMT  
		Size: 2.5 MB (2539706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30ee2de43b13169732d1745220365bd29615aa3000ad87986f795e3646215063`  
		Last Modified: Fri, 21 Jun 2024 07:01:54 GMT  
		Size: 56.9 MB (56920929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d390d8961f619b0803315f7c8b9d30e7635c6a23d4217bb5eff1f2c1bb2dabe`  
		Last Modified: Fri, 21 Jun 2024 07:01:52 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.30-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:9a79b9bfee239c98abdfc6ec6c30c40e6a5e4a9db8fbbec7cf5c9f54d5673969
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **997.3 KB (997336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e324cc8737b4f71db9beb447e8c7883604b95a87d1ab87f69850af44f2d0522`

```dockerfile
```

-	Layers:
	-	`sha256:e76a842a5de56bcea91c867461438062efcf970ccadae5ef1f9762f0e04de620`  
		Last Modified: Fri, 21 Jun 2024 07:01:52 GMT  
		Size: 982.3 KB (982326 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f43f107321e13e25da1cbba39d7755e169259c65de055b3c2bdc12aa9b2cc261`  
		Last Modified: Fri, 21 Jun 2024 07:01:51 GMT  
		Size: 15.0 KB (15010 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.30.3`

```console
$ docker pull telegraf@sha256:2abea02b6e577938131b83fecc83964539477d621acfe7134306b7542eb540b5
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
$ docker pull telegraf@sha256:f73ff0e0b13f014ccabcde4195e44a975e6cbd92813606cdcb71522c57e2ba5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.3 MB (155320684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c8deb06ed042a928956d9ce5e5a2470daae87404cf02dccbfd37ca6f5fb177c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 01 Jul 2024 19:20:29 GMT
ADD file:e8aac9b1598114ead96b4038c19d915b87f662ef342291d69c7e5255c5d731fc in / 
# Mon, 01 Jul 2024 19:20:29 GMT
CMD ["bash"]
# Mon, 01 Jul 2024 19:20:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 01 Jul 2024 19:20:29 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 01 Jul 2024 19:20:29 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 01 Jul 2024 19:20:29 GMT
ENV TELEGRAF_VERSION=1.30.3
# Mon, 01 Jul 2024 19:20:29 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 01 Jul 2024 19:20:29 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 01 Jul 2024 19:20:29 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 01 Jul 2024 19:20:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 01 Jul 2024 19:20:29 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:e9aef93137af6e967e7242f3b3c8ecd8e6f571d1e6fdd9e72db0befeeae3cf13`  
		Last Modified: Tue, 02 Jul 2024 01:28:26 GMT  
		Size: 49.6 MB (49554064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58b365fa3e8dc16e70d89fab0e91f5242feb38ae3cfeb6655e654209ea109333`  
		Last Modified: Tue, 02 Jul 2024 02:00:17 GMT  
		Size: 24.0 MB (24049794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5da89946764fe6bc921e753ff7761fdb24625e8d8a07165504de7111f8274324`  
		Last Modified: Tue, 02 Jul 2024 03:15:27 GMT  
		Size: 18.9 MB (18947987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d0ed75ef4d83b1fc9916de999fffb31b9d202dd97e63299228bc50a745abb4d`  
		Last Modified: Tue, 02 Jul 2024 03:15:27 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26b0d0ebc88ae7933e7aa23a67dc168c230dd1dcc529768c1295e92049a48d46`  
		Last Modified: Tue, 02 Jul 2024 03:15:28 GMT  
		Size: 62.8 MB (62766444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e5489c87b9807b63efbdda8579e0d344e48000e436195a6e16797b2cd68b07c`  
		Last Modified: Tue, 02 Jul 2024 03:15:27 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.30.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:1089c75e9f7745b1ed28464fe06d3723fef1524114df41345d7537306ed4901e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6313031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28bf0f3519c0bbf553c4bb7cdecded651ab2d5e38747485c75e33e92506dc2c9`

```dockerfile
```

-	Layers:
	-	`sha256:d572c57273bcfe0c2d47035ab9cc309404ff7a3b1c450e0937846f7203a136b7`  
		Last Modified: Tue, 02 Jul 2024 03:15:27 GMT  
		Size: 6.3 MB (6298707 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6d5c8d609a2f18588d8963f7c5b49e56d882946f44e02adffcfa76067c84d4d`  
		Last Modified: Tue, 02 Jul 2024 03:15:27 GMT  
		Size: 14.3 KB (14324 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.30.3` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:e6b6a03a34cffc85ca6bcf4c71f4351a57d3224891ba0aa9220429632ab865f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.0 MB (143042022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:842d5bbe61154b5ce2ff8ed5e3b51057ad021f9c044c13e0a69690f32b96de35`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 01 Jul 2024 19:20:29 GMT
ADD file:526dbb34ac449ae8f3c9025d71b3ffeb0e24fa5dc1a01da707f0a8b834eb4e33 in / 
# Mon, 01 Jul 2024 19:20:29 GMT
CMD ["bash"]
# Mon, 01 Jul 2024 19:20:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 01 Jul 2024 19:20:29 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 01 Jul 2024 19:20:29 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 01 Jul 2024 19:20:29 GMT
ENV TELEGRAF_VERSION=1.30.3
# Mon, 01 Jul 2024 19:20:29 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 01 Jul 2024 19:20:29 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 01 Jul 2024 19:20:29 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 01 Jul 2024 19:20:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 01 Jul 2024 19:20:29 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:335f2c484898b910fac13d5650ed3c78e5e673fe8dab1b06a071c71478a153d0`  
		Last Modified: Tue, 02 Jul 2024 01:02:57 GMT  
		Size: 45.1 MB (45148097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aa30b2bcbde45c2fc67abf425197af3af3e67d55296f168143343ef1b0e2d3e`  
		Last Modified: Tue, 02 Jul 2024 01:39:04 GMT  
		Size: 22.0 MB (21954038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac7a987fd3254b4eb8a2e6cc7206b9d5eac3e938a9d3c13d8fa167031b4fbcce`  
		Last Modified: Wed, 03 Jul 2024 01:34:48 GMT  
		Size: 17.7 MB (17724841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e17cfe5d83da74d5e8c4d81b008e6599fc7cca1105639345e4bf236669c7f0c5`  
		Last Modified: Wed, 03 Jul 2024 01:34:47 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31604fe832b771fdfc0f57206b12dc1e97a61e92e19904e3eeadac79dcfe3606`  
		Last Modified: Wed, 03 Jul 2024 01:35:46 GMT  
		Size: 58.2 MB (58212636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10093f2352b79e66ceb029afc2305de76684b93675bd445148a5cc9dcff9618f`  
		Last Modified: Wed, 03 Jul 2024 01:35:44 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.30.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:bea64ec9cc31676dd3fee1dd7b6eb0aa254afad308d6c8e943d0b5c884f70c17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6308465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c0f15de22e1d60de199faf973a835e9571c4c91ccd75f5f6a4ff5326968d985`

```dockerfile
```

-	Layers:
	-	`sha256:7899a503f349afc059a73a696098fa8dc056bdecfa2cb6e59c78476735d27310`  
		Last Modified: Wed, 03 Jul 2024 01:35:44 GMT  
		Size: 6.3 MB (6294061 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07452d604d36664587ed6a5966b02fe03f53d59715a8bb21fc5c65c503664243`  
		Last Modified: Wed, 03 Jul 2024 01:35:44 GMT  
		Size: 14.4 KB (14404 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.30.3` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:461d5e652edda6eee02ee4b136447d4838a9e7a56b331659bd3e2e9b236e12a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.2 MB (149175580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb7430674a24c6da24b76c10cdedff842a2209505b3c307ab14c4bbe4e60f57c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 01 Jul 2024 19:20:29 GMT
ADD file:696648070a57689a69a184fda234045f7be4a8a9f3b2fff9031ff0a2d9914113 in / 
# Mon, 01 Jul 2024 19:20:29 GMT
CMD ["bash"]
# Mon, 01 Jul 2024 19:20:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 01 Jul 2024 19:20:29 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 01 Jul 2024 19:20:29 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 01 Jul 2024 19:20:29 GMT
ENV TELEGRAF_VERSION=1.30.3
# Mon, 01 Jul 2024 19:20:29 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 01 Jul 2024 19:20:29 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 01 Jul 2024 19:20:29 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 01 Jul 2024 19:20:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 01 Jul 2024 19:20:29 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:0bd1f8180c504ba389021ce74895ed487ccd8c70e2d9af3707934bc801ba28d8`  
		Last Modified: Tue, 02 Jul 2024 00:42:03 GMT  
		Size: 49.6 MB (49588448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b16610496e73ba3d120d519598b53fa8a2db4c80ccc097a5016ad44aedd0654b`  
		Last Modified: Tue, 02 Jul 2024 04:01:41 GMT  
		Size: 23.6 MB (23591145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49fa4258ace16a879b6bae48191a62329ef9150aaf9ac97497e6d6c0f3d622aa`  
		Last Modified: Wed, 03 Jul 2024 00:51:44 GMT  
		Size: 18.9 MB (18870342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c86c902d4b3d360929e7f2bfb7aebbb19eb7c0bd8f515cf202c7fe68e2315b58`  
		Last Modified: Wed, 03 Jul 2024 00:51:43 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ac8c25bdfdab25b547db505539bd2fd37ce75df8f18e7c0ab0f54bbdc2ccaf9`  
		Last Modified: Wed, 03 Jul 2024 00:52:23 GMT  
		Size: 57.1 MB (57123239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:579a549f635d458174ccd9012b15f0520e9d6f7968c8a41b85bcd6c655163306`  
		Last Modified: Wed, 03 Jul 2024 00:52:21 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.30.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:04e4e275a7b3a7b9af5825abaf2eedf4f98dae987a0db48a7500f16d0cfcb5f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6313962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88e87f495c8d1975910a9b54b973571a8a5a0d2d4319dc27b8df8c7f7a6eb455`

```dockerfile
```

-	Layers:
	-	`sha256:be545d25107ef0652b891b232e09d106529d96b4f8b31f8d53e21ffcd358e2d0`  
		Last Modified: Wed, 03 Jul 2024 00:52:21 GMT  
		Size: 6.3 MB (6299345 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49f4c3aab6ccdf973e4787db7c17b8db477dd8d7930b95f3b521f971756d2828`  
		Last Modified: Wed, 03 Jul 2024 00:52:20 GMT  
		Size: 14.6 KB (14617 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.30.3-alpine`

```console
$ docker pull telegraf@sha256:a2ed1c626f31e48a36261fb87b45435d08df5c8da8f8deef0aa567dd54e0fa8c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.30.3-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:7d9dd9a8d17927b5ab64f2b5ab5d753392bb6f602fa6926d9081256ad66894f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.6 MB (68645907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c78422aae7eb12bd23f41bce4cb35583613d09d7f9f20a343bd2110d44d1408`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 10 Jun 2024 21:05:04 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
# Mon, 10 Jun 2024 21:05:04 GMT
CMD ["/bin/sh"]
# Mon, 10 Jun 2024 21:05:04 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
ENV TELEGRAF_VERSION=1.30.3
# Mon, 10 Jun 2024 21:05:04 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 10 Jun 2024 21:05:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Jun 2024 21:05:04 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:854692264f8809cf92629e7525eb2598493eae4136d97f12ba8db44a2957cb6a`  
		Last Modified: Thu, 20 Jun 2024 20:56:40 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f81fa91f596181920960e72a6871a7fbfd31377b83e4d7ecdd55850dba219e7`  
		Last Modified: Thu, 20 Jun 2024 20:56:40 GMT  
		Size: 2.5 MB (2452628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5989c1129b25207a17de9c1e2b3b4d9bb5e4fa649a47321695b750cacd317a6b`  
		Last Modified: Thu, 20 Jun 2024 20:56:41 GMT  
		Size: 62.6 MB (62568829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8194eec5904ba428ad67b75aabc1dcc4ec6535ed0da6072bf4cbc796f12edf2f`  
		Last Modified: Thu, 20 Jun 2024 20:56:40 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.30.3-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:ec438523f550864f5f8cde1a61b9cb8dcafd1ce5b8e7039c9ca4358ff1d5688c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1001473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a99b04efa643dcbf93abeb20c32c100ab442b5c97962b86919ffda7368edf4f1`

```dockerfile
```

-	Layers:
	-	`sha256:ed43db3ec20a6ba58ead7a069a1bf3aa51caa9afdd7e617641224fdd0c9864f6`  
		Last Modified: Thu, 20 Jun 2024 20:56:40 GMT  
		Size: 986.7 KB (986741 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e2212a71037664885b4644cfe397c388c4704a4a706dcee39402e20ef0035c3`  
		Last Modified: Thu, 20 Jun 2024 20:56:40 GMT  
		Size: 14.7 KB (14732 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.30.3-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:669deff433f02f6cacdd048db7d127be4525d4dbe2db1a46f64ff6871a2341be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.6 MB (63550043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b3dfe6b665f35c9e2fa07a7dba07cabfb44eec39975e2e76fb054559813bbea`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 10 Jun 2024 21:05:04 GMT
ADD file:033626ac44156f3d5800a602c46870486b1492b9ba26096eaa66cceb6fcead77 in / 
# Mon, 10 Jun 2024 21:05:04 GMT
CMD ["/bin/sh"]
# Mon, 10 Jun 2024 21:05:04 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
ENV TELEGRAF_VERSION=1.30.3
# Mon, 10 Jun 2024 21:05:04 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 10 Jun 2024 21:05:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Jun 2024 21:05:04 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:a258b2a6b59a7aa244d8ceab095c7f8df726f27075a69fca7ad8490f3f63148a`  
		Last Modified: Thu, 20 Jun 2024 17:40:58 GMT  
		Size: 4.1 MB (4088800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe4d02fd6d451824a88c3da056c35af5ef536e8a634a98239ab90c650e0518e3`  
		Last Modified: Fri, 21 Jun 2024 05:12:50 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c75d4393617a41a89527ad46200950f81c7c7993bd950a78413ef7d03b012113`  
		Last Modified: Fri, 21 Jun 2024 07:01:17 GMT  
		Size: 2.5 MB (2539706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30ee2de43b13169732d1745220365bd29615aa3000ad87986f795e3646215063`  
		Last Modified: Fri, 21 Jun 2024 07:01:54 GMT  
		Size: 56.9 MB (56920929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d390d8961f619b0803315f7c8b9d30e7635c6a23d4217bb5eff1f2c1bb2dabe`  
		Last Modified: Fri, 21 Jun 2024 07:01:52 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.30.3-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:9a79b9bfee239c98abdfc6ec6c30c40e6a5e4a9db8fbbec7cf5c9f54d5673969
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **997.3 KB (997336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e324cc8737b4f71db9beb447e8c7883604b95a87d1ab87f69850af44f2d0522`

```dockerfile
```

-	Layers:
	-	`sha256:e76a842a5de56bcea91c867461438062efcf970ccadae5ef1f9762f0e04de620`  
		Last Modified: Fri, 21 Jun 2024 07:01:52 GMT  
		Size: 982.3 KB (982326 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f43f107321e13e25da1cbba39d7755e169259c65de055b3c2bdc12aa9b2cc261`  
		Last Modified: Fri, 21 Jun 2024 07:01:51 GMT  
		Size: 15.0 KB (15010 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.31`

```console
$ docker pull telegraf@sha256:a6d46429979581953b7b81f5b245ee3d6ab45d110d3b9086380f27167f7e33f4
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
$ docker pull telegraf@sha256:0bf8d0b836337c94ec66c11f36bf35b653348fc4d274f242c7c49df70a7b6ce3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.8 MB (158781425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e5ef5932dbb288c90648457ca93ec01caded5034ec8bd2cca94d4e8b8667869`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 01 Jul 2024 19:20:29 GMT
ADD file:e8aac9b1598114ead96b4038c19d915b87f662ef342291d69c7e5255c5d731fc in / 
# Mon, 01 Jul 2024 19:20:29 GMT
CMD ["bash"]
# Mon, 01 Jul 2024 19:20:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 01 Jul 2024 19:20:29 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 01 Jul 2024 19:20:29 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 01 Jul 2024 19:20:29 GMT
ENV TELEGRAF_VERSION=1.31.1
# Mon, 01 Jul 2024 19:20:29 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 01 Jul 2024 19:20:29 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 01 Jul 2024 19:20:29 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 01 Jul 2024 19:20:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 01 Jul 2024 19:20:29 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:e9aef93137af6e967e7242f3b3c8ecd8e6f571d1e6fdd9e72db0befeeae3cf13`  
		Last Modified: Tue, 02 Jul 2024 01:28:26 GMT  
		Size: 49.6 MB (49554064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58b365fa3e8dc16e70d89fab0e91f5242feb38ae3cfeb6655e654209ea109333`  
		Last Modified: Tue, 02 Jul 2024 02:00:17 GMT  
		Size: 24.0 MB (24049794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73640a629d5c024f9dfe1e45997e798ee73d8a1610b0f3b8323574909a371251`  
		Last Modified: Tue, 02 Jul 2024 03:32:15 GMT  
		Size: 18.9 MB (18947959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b734f825ca42c8b2531d5b7bff4a2fd773b28e939e01ba10cd88aba8b1d5923`  
		Last Modified: Tue, 02 Jul 2024 03:32:14 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5592f5a587d7f8eedb6976959e4f68eced16e31fd88eadca308608811f4f2ee5`  
		Last Modified: Tue, 02 Jul 2024 03:32:15 GMT  
		Size: 66.2 MB (66227197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1345e4c69b07d7c081836490c21d7fdcf540c9048e4dd30fc6cbb845c5c9e0a`  
		Last Modified: Tue, 02 Jul 2024 03:32:14 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31` - unknown; unknown

```console
$ docker pull telegraf@sha256:acb0bd848143d98105741c38a6e2c59d0374115be8f9da3c9133fd7d86110f84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6318988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16d34bd18c3254b1f26fe2d3a73e22e781ba64cde20b65d21cbddcb43fac5ff1`

```dockerfile
```

-	Layers:
	-	`sha256:64ff97c343edd9924cbb0d64971baecadd617383c57598cc79313feb2f8abd2e`  
		Last Modified: Tue, 02 Jul 2024 03:32:14 GMT  
		Size: 6.3 MB (6304363 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e60e4cc25bb1bf81857c3e626e050e6bbef9703b8b409cb67cc933378595b25`  
		Last Modified: Tue, 02 Jul 2024 03:32:14 GMT  
		Size: 14.6 KB (14625 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.31` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:bd326c1e04da02a6334b2adc11a33126fb5f4bca543e27fb7f6e835937dd7529
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.4 MB (146430538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c6c497ad4bd877235dc727f34b836a9683c7066e9b23174518c7505c40f0810`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 01 Jul 2024 19:20:29 GMT
ADD file:526dbb34ac449ae8f3c9025d71b3ffeb0e24fa5dc1a01da707f0a8b834eb4e33 in / 
# Mon, 01 Jul 2024 19:20:29 GMT
CMD ["bash"]
# Mon, 01 Jul 2024 19:20:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 01 Jul 2024 19:20:29 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 01 Jul 2024 19:20:29 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 01 Jul 2024 19:20:29 GMT
ENV TELEGRAF_VERSION=1.31.1
# Mon, 01 Jul 2024 19:20:29 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 01 Jul 2024 19:20:29 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 01 Jul 2024 19:20:29 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 01 Jul 2024 19:20:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 01 Jul 2024 19:20:29 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:335f2c484898b910fac13d5650ed3c78e5e673fe8dab1b06a071c71478a153d0`  
		Last Modified: Tue, 02 Jul 2024 01:02:57 GMT  
		Size: 45.1 MB (45148097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aa30b2bcbde45c2fc67abf425197af3af3e67d55296f168143343ef1b0e2d3e`  
		Last Modified: Tue, 02 Jul 2024 01:39:04 GMT  
		Size: 22.0 MB (21954038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac7a987fd3254b4eb8a2e6cc7206b9d5eac3e938a9d3c13d8fa167031b4fbcce`  
		Last Modified: Wed, 03 Jul 2024 01:34:48 GMT  
		Size: 17.7 MB (17724841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e17cfe5d83da74d5e8c4d81b008e6599fc7cca1105639345e4bf236669c7f0c5`  
		Last Modified: Wed, 03 Jul 2024 01:34:47 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffb5b65e557f72b22f833c43955f3c8d36093fd4040e5d8d436bc2f39dd8362a`  
		Last Modified: Wed, 03 Jul 2024 01:36:38 GMT  
		Size: 61.6 MB (61601152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20f5ed5bd1d96e3bf9e9b6f47eaf1e1aa50042560ddc6f546da60292553a2f16`  
		Last Modified: Wed, 03 Jul 2024 01:36:35 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31` - unknown; unknown

```console
$ docker pull telegraf@sha256:e031f34a1bc0b974683b355de0553a9bc75a572a724cdc37cb87839c016959a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6315093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05d317ad92eb5361752a0696f2725b1f92deff7bdddfb49f36188c03b20af44d`

```dockerfile
```

-	Layers:
	-	`sha256:1aab98ed50ba77997063ac8e4d303152b55a27f70a4465de6fdbf5fa1404f018`  
		Last Modified: Wed, 03 Jul 2024 01:36:36 GMT  
		Size: 6.3 MB (6300379 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e1b16159e9459b5b279a5f297fc73228d4d21f3d2996504fdb2f28a9eeb1c55`  
		Last Modified: Wed, 03 Jul 2024 01:36:35 GMT  
		Size: 14.7 KB (14714 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.31` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:9df7de5c3c95b0f72771ffa58f2b9a5a5dcf22b41b63a6b9fb244244a06e3249
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.3 MB (152336093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08fce67cb8fa54d34a54c6266529978c8db1a3d91fb2a8f72cc4ad46e963d103`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 01 Jul 2024 19:20:29 GMT
ADD file:696648070a57689a69a184fda234045f7be4a8a9f3b2fff9031ff0a2d9914113 in / 
# Mon, 01 Jul 2024 19:20:29 GMT
CMD ["bash"]
# Mon, 01 Jul 2024 19:20:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 01 Jul 2024 19:20:29 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 01 Jul 2024 19:20:29 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 01 Jul 2024 19:20:29 GMT
ENV TELEGRAF_VERSION=1.31.1
# Mon, 01 Jul 2024 19:20:29 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 01 Jul 2024 19:20:29 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 01 Jul 2024 19:20:29 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 01 Jul 2024 19:20:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 01 Jul 2024 19:20:29 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:0bd1f8180c504ba389021ce74895ed487ccd8c70e2d9af3707934bc801ba28d8`  
		Last Modified: Tue, 02 Jul 2024 00:42:03 GMT  
		Size: 49.6 MB (49588448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b16610496e73ba3d120d519598b53fa8a2db4c80ccc097a5016ad44aedd0654b`  
		Last Modified: Tue, 02 Jul 2024 04:01:41 GMT  
		Size: 23.6 MB (23591145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49fa4258ace16a879b6bae48191a62329ef9150aaf9ac97497e6d6c0f3d622aa`  
		Last Modified: Wed, 03 Jul 2024 00:51:44 GMT  
		Size: 18.9 MB (18870342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c86c902d4b3d360929e7f2bfb7aebbb19eb7c0bd8f515cf202c7fe68e2315b58`  
		Last Modified: Wed, 03 Jul 2024 00:51:43 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53711602d3ab9a60d8d35c9202bbe4620c8c8fd1888fb16601d4bf36e311690b`  
		Last Modified: Wed, 03 Jul 2024 00:52:55 GMT  
		Size: 60.3 MB (60283753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78887db2826f45f52baafab97c61e63c1124243fd6cae85e2f8c3a06853036b3`  
		Last Modified: Wed, 03 Jul 2024 00:52:53 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31` - unknown; unknown

```console
$ docker pull telegraf@sha256:0e7d3e64ffa05e5ff13896af64e5aaf547d82c4b22de2a8b5630b0e6470f196f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6321250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f69bceb31f7804c7610329c5a403aba38aa8a6e6b8c4aeb879381d81b7bbeba`

```dockerfile
```

-	Layers:
	-	`sha256:152e5903a51b12964d1ec93c4d2aa0b4929a87744964442b58e3d753aa892a59`  
		Last Modified: Wed, 03 Jul 2024 00:52:54 GMT  
		Size: 6.3 MB (6306319 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d3e466a2111dd26c94480a8dc228e399e4ddfd66f64147958a1783efa147799`  
		Last Modified: Wed, 03 Jul 2024 00:52:53 GMT  
		Size: 14.9 KB (14931 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.31-alpine`

```console
$ docker pull telegraf@sha256:66b95b2dfb5846da212397c4594f8cfd38f3047d1d72955a420fd9bf088068ab
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.31-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:e6110654779dffe3af93674173ab6ee65d98de67ba562583827498c83cd53fe8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.1 MB (72102360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:690e3afff75e2915f456af71b4ef75228606e25dc91159fb154d1736d41e037c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Thu, 20 Jun 2024 20:16:57 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
# Thu, 20 Jun 2024 20:16:58 GMT
CMD ["/bin/sh"]
# Mon, 01 Jul 2024 19:20:29 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 01 Jul 2024 19:20:29 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 01 Jul 2024 19:20:29 GMT
ENV TELEGRAF_VERSION=1.31.1
# Mon, 01 Jul 2024 19:20:29 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 01 Jul 2024 19:20:29 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 01 Jul 2024 19:20:29 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 01 Jul 2024 19:20:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 01 Jul 2024 19:20:29 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f026d2909cd521d5e52efb7fd369a9ad0fde515ce36e3e67ee6a5c4866a5b719`  
		Last Modified: Mon, 01 Jul 2024 23:55:03 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e686998f6bff2309f7498d422d6eba5a6c2e01c8f6aee776455d33d3f205a195`  
		Last Modified: Mon, 01 Jul 2024 23:55:03 GMT  
		Size: 2.5 MB (2452606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:243a6d3006b5e4f58627b5b7abd8215164fde6b7f4956e8eb2bc358f1674cb28`  
		Last Modified: Mon, 01 Jul 2024 23:55:04 GMT  
		Size: 66.0 MB (66025305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad210721abc8e4b05979e6a3bb37039633ec7ed12e427c27306169fccd73973d`  
		Last Modified: Mon, 01 Jul 2024 23:55:03 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:38bdf9eec17433a6514491e416d9f1a5486fb6316d156e5e7ebbdb2f04a38a8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1007433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c85c73a22037ce20ce906665b70aa5e6fc880bb17cbbc40efbb1324eddda506`

```dockerfile
```

-	Layers:
	-	`sha256:53a3e95a49ad1a494a788bded03675776caadb3dec72aa6ac64e1b2c8308f33e`  
		Last Modified: Mon, 01 Jul 2024 23:55:03 GMT  
		Size: 992.4 KB (992397 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7bb7667d37c570b271319f05d4318ba936c80c6a958ae6d51a2eb199e61b2e59`  
		Last Modified: Mon, 01 Jul 2024 23:55:03 GMT  
		Size: 15.0 KB (15036 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.31-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:82db004093bbbaea8c9deef8f4fc92752c2720d217391af0479c9032cf4e53bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66715791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0dfde127891469f8009177857aa32bb0adf9ae21ba4fb05a7c3442b57d7f712`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:35 GMT
ADD file:033626ac44156f3d5800a602c46870486b1492b9ba26096eaa66cceb6fcead77 in / 
# Thu, 20 Jun 2024 17:40:35 GMT
CMD ["/bin/sh"]
# Mon, 01 Jul 2024 19:20:29 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 01 Jul 2024 19:20:29 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 01 Jul 2024 19:20:29 GMT
ENV TELEGRAF_VERSION=1.31.1
# Mon, 01 Jul 2024 19:20:29 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 01 Jul 2024 19:20:29 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 01 Jul 2024 19:20:29 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 01 Jul 2024 19:20:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 01 Jul 2024 19:20:29 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:a258b2a6b59a7aa244d8ceab095c7f8df726f27075a69fca7ad8490f3f63148a`  
		Last Modified: Thu, 20 Jun 2024 17:40:58 GMT  
		Size: 4.1 MB (4088800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11eba8dd2e5fd29bab729423d14db817b55f44940b10b1e32f92827462e6e423`  
		Last Modified: Mon, 01 Jul 2024 23:59:24 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59ceccb2cc5da64d07330ea2171242f64cd0bd8c1a58c50cf78d5afec75bdb08`  
		Last Modified: Mon, 01 Jul 2024 23:59:24 GMT  
		Size: 2.5 MB (2539679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3da2f3607c9ebd8d31adfea01b8869e3ecc164fe7711dc33994a8253da973947`  
		Last Modified: Mon, 01 Jul 2024 23:59:26 GMT  
		Size: 60.1 MB (60086705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f16e1577aef80fc7823214e09bebb6fe8556f86173907f1d23e6b46d84c923b`  
		Last Modified: Mon, 01 Jul 2024 23:59:24 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:e3148bdad776e71b356d54317b7473aed6523aa96cc09e440d876e25e51656c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1004624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cf6a5a2db81e49f9aba624d891858033ec37e2233f9c55234f71aa8c28437b0`

```dockerfile
```

-	Layers:
	-	`sha256:d24c61ecd55103603c7f91fdf5c6f18b9938562ce87de478877e3ae358d5ab6c`  
		Last Modified: Mon, 01 Jul 2024 23:59:25 GMT  
		Size: 989.3 KB (989300 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5777d418d3d75900d18eba587c27585dcb2eb0b7e90c248e8890f74558e32fa2`  
		Last Modified: Mon, 01 Jul 2024 23:59:24 GMT  
		Size: 15.3 KB (15324 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.31.1`

```console
$ docker pull telegraf@sha256:a6d46429979581953b7b81f5b245ee3d6ab45d110d3b9086380f27167f7e33f4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.31.1` - linux; amd64

```console
$ docker pull telegraf@sha256:0bf8d0b836337c94ec66c11f36bf35b653348fc4d274f242c7c49df70a7b6ce3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.8 MB (158781425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e5ef5932dbb288c90648457ca93ec01caded5034ec8bd2cca94d4e8b8667869`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 01 Jul 2024 19:20:29 GMT
ADD file:e8aac9b1598114ead96b4038c19d915b87f662ef342291d69c7e5255c5d731fc in / 
# Mon, 01 Jul 2024 19:20:29 GMT
CMD ["bash"]
# Mon, 01 Jul 2024 19:20:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 01 Jul 2024 19:20:29 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 01 Jul 2024 19:20:29 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 01 Jul 2024 19:20:29 GMT
ENV TELEGRAF_VERSION=1.31.1
# Mon, 01 Jul 2024 19:20:29 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 01 Jul 2024 19:20:29 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 01 Jul 2024 19:20:29 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 01 Jul 2024 19:20:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 01 Jul 2024 19:20:29 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:e9aef93137af6e967e7242f3b3c8ecd8e6f571d1e6fdd9e72db0befeeae3cf13`  
		Last Modified: Tue, 02 Jul 2024 01:28:26 GMT  
		Size: 49.6 MB (49554064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58b365fa3e8dc16e70d89fab0e91f5242feb38ae3cfeb6655e654209ea109333`  
		Last Modified: Tue, 02 Jul 2024 02:00:17 GMT  
		Size: 24.0 MB (24049794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73640a629d5c024f9dfe1e45997e798ee73d8a1610b0f3b8323574909a371251`  
		Last Modified: Tue, 02 Jul 2024 03:32:15 GMT  
		Size: 18.9 MB (18947959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b734f825ca42c8b2531d5b7bff4a2fd773b28e939e01ba10cd88aba8b1d5923`  
		Last Modified: Tue, 02 Jul 2024 03:32:14 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5592f5a587d7f8eedb6976959e4f68eced16e31fd88eadca308608811f4f2ee5`  
		Last Modified: Tue, 02 Jul 2024 03:32:15 GMT  
		Size: 66.2 MB (66227197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1345e4c69b07d7c081836490c21d7fdcf540c9048e4dd30fc6cbb845c5c9e0a`  
		Last Modified: Tue, 02 Jul 2024 03:32:14 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31.1` - unknown; unknown

```console
$ docker pull telegraf@sha256:acb0bd848143d98105741c38a6e2c59d0374115be8f9da3c9133fd7d86110f84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6318988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16d34bd18c3254b1f26fe2d3a73e22e781ba64cde20b65d21cbddcb43fac5ff1`

```dockerfile
```

-	Layers:
	-	`sha256:64ff97c343edd9924cbb0d64971baecadd617383c57598cc79313feb2f8abd2e`  
		Last Modified: Tue, 02 Jul 2024 03:32:14 GMT  
		Size: 6.3 MB (6304363 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e60e4cc25bb1bf81857c3e626e050e6bbef9703b8b409cb67cc933378595b25`  
		Last Modified: Tue, 02 Jul 2024 03:32:14 GMT  
		Size: 14.6 KB (14625 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.31.1` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:bd326c1e04da02a6334b2adc11a33126fb5f4bca543e27fb7f6e835937dd7529
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.4 MB (146430538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c6c497ad4bd877235dc727f34b836a9683c7066e9b23174518c7505c40f0810`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 01 Jul 2024 19:20:29 GMT
ADD file:526dbb34ac449ae8f3c9025d71b3ffeb0e24fa5dc1a01da707f0a8b834eb4e33 in / 
# Mon, 01 Jul 2024 19:20:29 GMT
CMD ["bash"]
# Mon, 01 Jul 2024 19:20:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 01 Jul 2024 19:20:29 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 01 Jul 2024 19:20:29 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 01 Jul 2024 19:20:29 GMT
ENV TELEGRAF_VERSION=1.31.1
# Mon, 01 Jul 2024 19:20:29 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 01 Jul 2024 19:20:29 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 01 Jul 2024 19:20:29 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 01 Jul 2024 19:20:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 01 Jul 2024 19:20:29 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:335f2c484898b910fac13d5650ed3c78e5e673fe8dab1b06a071c71478a153d0`  
		Last Modified: Tue, 02 Jul 2024 01:02:57 GMT  
		Size: 45.1 MB (45148097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aa30b2bcbde45c2fc67abf425197af3af3e67d55296f168143343ef1b0e2d3e`  
		Last Modified: Tue, 02 Jul 2024 01:39:04 GMT  
		Size: 22.0 MB (21954038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac7a987fd3254b4eb8a2e6cc7206b9d5eac3e938a9d3c13d8fa167031b4fbcce`  
		Last Modified: Wed, 03 Jul 2024 01:34:48 GMT  
		Size: 17.7 MB (17724841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e17cfe5d83da74d5e8c4d81b008e6599fc7cca1105639345e4bf236669c7f0c5`  
		Last Modified: Wed, 03 Jul 2024 01:34:47 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffb5b65e557f72b22f833c43955f3c8d36093fd4040e5d8d436bc2f39dd8362a`  
		Last Modified: Wed, 03 Jul 2024 01:36:38 GMT  
		Size: 61.6 MB (61601152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20f5ed5bd1d96e3bf9e9b6f47eaf1e1aa50042560ddc6f546da60292553a2f16`  
		Last Modified: Wed, 03 Jul 2024 01:36:35 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31.1` - unknown; unknown

```console
$ docker pull telegraf@sha256:e031f34a1bc0b974683b355de0553a9bc75a572a724cdc37cb87839c016959a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6315093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05d317ad92eb5361752a0696f2725b1f92deff7bdddfb49f36188c03b20af44d`

```dockerfile
```

-	Layers:
	-	`sha256:1aab98ed50ba77997063ac8e4d303152b55a27f70a4465de6fdbf5fa1404f018`  
		Last Modified: Wed, 03 Jul 2024 01:36:36 GMT  
		Size: 6.3 MB (6300379 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e1b16159e9459b5b279a5f297fc73228d4d21f3d2996504fdb2f28a9eeb1c55`  
		Last Modified: Wed, 03 Jul 2024 01:36:35 GMT  
		Size: 14.7 KB (14714 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.31.1` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:9df7de5c3c95b0f72771ffa58f2b9a5a5dcf22b41b63a6b9fb244244a06e3249
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.3 MB (152336093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08fce67cb8fa54d34a54c6266529978c8db1a3d91fb2a8f72cc4ad46e963d103`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 01 Jul 2024 19:20:29 GMT
ADD file:696648070a57689a69a184fda234045f7be4a8a9f3b2fff9031ff0a2d9914113 in / 
# Mon, 01 Jul 2024 19:20:29 GMT
CMD ["bash"]
# Mon, 01 Jul 2024 19:20:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 01 Jul 2024 19:20:29 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 01 Jul 2024 19:20:29 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 01 Jul 2024 19:20:29 GMT
ENV TELEGRAF_VERSION=1.31.1
# Mon, 01 Jul 2024 19:20:29 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 01 Jul 2024 19:20:29 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 01 Jul 2024 19:20:29 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 01 Jul 2024 19:20:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 01 Jul 2024 19:20:29 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:0bd1f8180c504ba389021ce74895ed487ccd8c70e2d9af3707934bc801ba28d8`  
		Last Modified: Tue, 02 Jul 2024 00:42:03 GMT  
		Size: 49.6 MB (49588448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b16610496e73ba3d120d519598b53fa8a2db4c80ccc097a5016ad44aedd0654b`  
		Last Modified: Tue, 02 Jul 2024 04:01:41 GMT  
		Size: 23.6 MB (23591145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49fa4258ace16a879b6bae48191a62329ef9150aaf9ac97497e6d6c0f3d622aa`  
		Last Modified: Wed, 03 Jul 2024 00:51:44 GMT  
		Size: 18.9 MB (18870342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c86c902d4b3d360929e7f2bfb7aebbb19eb7c0bd8f515cf202c7fe68e2315b58`  
		Last Modified: Wed, 03 Jul 2024 00:51:43 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53711602d3ab9a60d8d35c9202bbe4620c8c8fd1888fb16601d4bf36e311690b`  
		Last Modified: Wed, 03 Jul 2024 00:52:55 GMT  
		Size: 60.3 MB (60283753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78887db2826f45f52baafab97c61e63c1124243fd6cae85e2f8c3a06853036b3`  
		Last Modified: Wed, 03 Jul 2024 00:52:53 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31.1` - unknown; unknown

```console
$ docker pull telegraf@sha256:0e7d3e64ffa05e5ff13896af64e5aaf547d82c4b22de2a8b5630b0e6470f196f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6321250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f69bceb31f7804c7610329c5a403aba38aa8a6e6b8c4aeb879381d81b7bbeba`

```dockerfile
```

-	Layers:
	-	`sha256:152e5903a51b12964d1ec93c4d2aa0b4929a87744964442b58e3d753aa892a59`  
		Last Modified: Wed, 03 Jul 2024 00:52:54 GMT  
		Size: 6.3 MB (6306319 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d3e466a2111dd26c94480a8dc228e399e4ddfd66f64147958a1783efa147799`  
		Last Modified: Wed, 03 Jul 2024 00:52:53 GMT  
		Size: 14.9 KB (14931 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.31.1-alpine`

```console
$ docker pull telegraf@sha256:66b95b2dfb5846da212397c4594f8cfd38f3047d1d72955a420fd9bf088068ab
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.31.1-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:e6110654779dffe3af93674173ab6ee65d98de67ba562583827498c83cd53fe8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.1 MB (72102360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:690e3afff75e2915f456af71b4ef75228606e25dc91159fb154d1736d41e037c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Thu, 20 Jun 2024 20:16:57 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
# Thu, 20 Jun 2024 20:16:58 GMT
CMD ["/bin/sh"]
# Mon, 01 Jul 2024 19:20:29 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 01 Jul 2024 19:20:29 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 01 Jul 2024 19:20:29 GMT
ENV TELEGRAF_VERSION=1.31.1
# Mon, 01 Jul 2024 19:20:29 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 01 Jul 2024 19:20:29 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 01 Jul 2024 19:20:29 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 01 Jul 2024 19:20:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 01 Jul 2024 19:20:29 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f026d2909cd521d5e52efb7fd369a9ad0fde515ce36e3e67ee6a5c4866a5b719`  
		Last Modified: Mon, 01 Jul 2024 23:55:03 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e686998f6bff2309f7498d422d6eba5a6c2e01c8f6aee776455d33d3f205a195`  
		Last Modified: Mon, 01 Jul 2024 23:55:03 GMT  
		Size: 2.5 MB (2452606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:243a6d3006b5e4f58627b5b7abd8215164fde6b7f4956e8eb2bc358f1674cb28`  
		Last Modified: Mon, 01 Jul 2024 23:55:04 GMT  
		Size: 66.0 MB (66025305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad210721abc8e4b05979e6a3bb37039633ec7ed12e427c27306169fccd73973d`  
		Last Modified: Mon, 01 Jul 2024 23:55:03 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31.1-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:38bdf9eec17433a6514491e416d9f1a5486fb6316d156e5e7ebbdb2f04a38a8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1007433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c85c73a22037ce20ce906665b70aa5e6fc880bb17cbbc40efbb1324eddda506`

```dockerfile
```

-	Layers:
	-	`sha256:53a3e95a49ad1a494a788bded03675776caadb3dec72aa6ac64e1b2c8308f33e`  
		Last Modified: Mon, 01 Jul 2024 23:55:03 GMT  
		Size: 992.4 KB (992397 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7bb7667d37c570b271319f05d4318ba936c80c6a958ae6d51a2eb199e61b2e59`  
		Last Modified: Mon, 01 Jul 2024 23:55:03 GMT  
		Size: 15.0 KB (15036 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.31.1-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:82db004093bbbaea8c9deef8f4fc92752c2720d217391af0479c9032cf4e53bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66715791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0dfde127891469f8009177857aa32bb0adf9ae21ba4fb05a7c3442b57d7f712`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:35 GMT
ADD file:033626ac44156f3d5800a602c46870486b1492b9ba26096eaa66cceb6fcead77 in / 
# Thu, 20 Jun 2024 17:40:35 GMT
CMD ["/bin/sh"]
# Mon, 01 Jul 2024 19:20:29 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 01 Jul 2024 19:20:29 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 01 Jul 2024 19:20:29 GMT
ENV TELEGRAF_VERSION=1.31.1
# Mon, 01 Jul 2024 19:20:29 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 01 Jul 2024 19:20:29 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 01 Jul 2024 19:20:29 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 01 Jul 2024 19:20:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 01 Jul 2024 19:20:29 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:a258b2a6b59a7aa244d8ceab095c7f8df726f27075a69fca7ad8490f3f63148a`  
		Last Modified: Thu, 20 Jun 2024 17:40:58 GMT  
		Size: 4.1 MB (4088800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11eba8dd2e5fd29bab729423d14db817b55f44940b10b1e32f92827462e6e423`  
		Last Modified: Mon, 01 Jul 2024 23:59:24 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59ceccb2cc5da64d07330ea2171242f64cd0bd8c1a58c50cf78d5afec75bdb08`  
		Last Modified: Mon, 01 Jul 2024 23:59:24 GMT  
		Size: 2.5 MB (2539679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3da2f3607c9ebd8d31adfea01b8869e3ecc164fe7711dc33994a8253da973947`  
		Last Modified: Mon, 01 Jul 2024 23:59:26 GMT  
		Size: 60.1 MB (60086705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f16e1577aef80fc7823214e09bebb6fe8556f86173907f1d23e6b46d84c923b`  
		Last Modified: Mon, 01 Jul 2024 23:59:24 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31.1-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:e3148bdad776e71b356d54317b7473aed6523aa96cc09e440d876e25e51656c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1004624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cf6a5a2db81e49f9aba624d891858033ec37e2233f9c55234f71aa8c28437b0`

```dockerfile
```

-	Layers:
	-	`sha256:d24c61ecd55103603c7f91fdf5c6f18b9938562ce87de478877e3ae358d5ab6c`  
		Last Modified: Mon, 01 Jul 2024 23:59:25 GMT  
		Size: 989.3 KB (989300 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5777d418d3d75900d18eba587c27585dcb2eb0b7e90c248e8890f74558e32fa2`  
		Last Modified: Mon, 01 Jul 2024 23:59:24 GMT  
		Size: 15.3 KB (15324 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:alpine`

```console
$ docker pull telegraf@sha256:66b95b2dfb5846da212397c4594f8cfd38f3047d1d72955a420fd9bf088068ab
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:e6110654779dffe3af93674173ab6ee65d98de67ba562583827498c83cd53fe8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.1 MB (72102360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:690e3afff75e2915f456af71b4ef75228606e25dc91159fb154d1736d41e037c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Thu, 20 Jun 2024 20:16:57 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
# Thu, 20 Jun 2024 20:16:58 GMT
CMD ["/bin/sh"]
# Mon, 01 Jul 2024 19:20:29 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 01 Jul 2024 19:20:29 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 01 Jul 2024 19:20:29 GMT
ENV TELEGRAF_VERSION=1.31.1
# Mon, 01 Jul 2024 19:20:29 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 01 Jul 2024 19:20:29 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 01 Jul 2024 19:20:29 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 01 Jul 2024 19:20:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 01 Jul 2024 19:20:29 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f026d2909cd521d5e52efb7fd369a9ad0fde515ce36e3e67ee6a5c4866a5b719`  
		Last Modified: Mon, 01 Jul 2024 23:55:03 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e686998f6bff2309f7498d422d6eba5a6c2e01c8f6aee776455d33d3f205a195`  
		Last Modified: Mon, 01 Jul 2024 23:55:03 GMT  
		Size: 2.5 MB (2452606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:243a6d3006b5e4f58627b5b7abd8215164fde6b7f4956e8eb2bc358f1674cb28`  
		Last Modified: Mon, 01 Jul 2024 23:55:04 GMT  
		Size: 66.0 MB (66025305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad210721abc8e4b05979e6a3bb37039633ec7ed12e427c27306169fccd73973d`  
		Last Modified: Mon, 01 Jul 2024 23:55:03 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:38bdf9eec17433a6514491e416d9f1a5486fb6316d156e5e7ebbdb2f04a38a8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1007433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c85c73a22037ce20ce906665b70aa5e6fc880bb17cbbc40efbb1324eddda506`

```dockerfile
```

-	Layers:
	-	`sha256:53a3e95a49ad1a494a788bded03675776caadb3dec72aa6ac64e1b2c8308f33e`  
		Last Modified: Mon, 01 Jul 2024 23:55:03 GMT  
		Size: 992.4 KB (992397 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7bb7667d37c570b271319f05d4318ba936c80c6a958ae6d51a2eb199e61b2e59`  
		Last Modified: Mon, 01 Jul 2024 23:55:03 GMT  
		Size: 15.0 KB (15036 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:82db004093bbbaea8c9deef8f4fc92752c2720d217391af0479c9032cf4e53bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66715791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0dfde127891469f8009177857aa32bb0adf9ae21ba4fb05a7c3442b57d7f712`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:35 GMT
ADD file:033626ac44156f3d5800a602c46870486b1492b9ba26096eaa66cceb6fcead77 in / 
# Thu, 20 Jun 2024 17:40:35 GMT
CMD ["/bin/sh"]
# Mon, 01 Jul 2024 19:20:29 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 01 Jul 2024 19:20:29 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 01 Jul 2024 19:20:29 GMT
ENV TELEGRAF_VERSION=1.31.1
# Mon, 01 Jul 2024 19:20:29 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 01 Jul 2024 19:20:29 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 01 Jul 2024 19:20:29 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 01 Jul 2024 19:20:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 01 Jul 2024 19:20:29 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:a258b2a6b59a7aa244d8ceab095c7f8df726f27075a69fca7ad8490f3f63148a`  
		Last Modified: Thu, 20 Jun 2024 17:40:58 GMT  
		Size: 4.1 MB (4088800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11eba8dd2e5fd29bab729423d14db817b55f44940b10b1e32f92827462e6e423`  
		Last Modified: Mon, 01 Jul 2024 23:59:24 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59ceccb2cc5da64d07330ea2171242f64cd0bd8c1a58c50cf78d5afec75bdb08`  
		Last Modified: Mon, 01 Jul 2024 23:59:24 GMT  
		Size: 2.5 MB (2539679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3da2f3607c9ebd8d31adfea01b8869e3ecc164fe7711dc33994a8253da973947`  
		Last Modified: Mon, 01 Jul 2024 23:59:26 GMT  
		Size: 60.1 MB (60086705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f16e1577aef80fc7823214e09bebb6fe8556f86173907f1d23e6b46d84c923b`  
		Last Modified: Mon, 01 Jul 2024 23:59:24 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:e3148bdad776e71b356d54317b7473aed6523aa96cc09e440d876e25e51656c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1004624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cf6a5a2db81e49f9aba624d891858033ec37e2233f9c55234f71aa8c28437b0`

```dockerfile
```

-	Layers:
	-	`sha256:d24c61ecd55103603c7f91fdf5c6f18b9938562ce87de478877e3ae358d5ab6c`  
		Last Modified: Mon, 01 Jul 2024 23:59:25 GMT  
		Size: 989.3 KB (989300 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5777d418d3d75900d18eba587c27585dcb2eb0b7e90c248e8890f74558e32fa2`  
		Last Modified: Mon, 01 Jul 2024 23:59:24 GMT  
		Size: 15.3 KB (15324 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:latest`

```console
$ docker pull telegraf@sha256:a6d46429979581953b7b81f5b245ee3d6ab45d110d3b9086380f27167f7e33f4
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
$ docker pull telegraf@sha256:0bf8d0b836337c94ec66c11f36bf35b653348fc4d274f242c7c49df70a7b6ce3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.8 MB (158781425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e5ef5932dbb288c90648457ca93ec01caded5034ec8bd2cca94d4e8b8667869`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 01 Jul 2024 19:20:29 GMT
ADD file:e8aac9b1598114ead96b4038c19d915b87f662ef342291d69c7e5255c5d731fc in / 
# Mon, 01 Jul 2024 19:20:29 GMT
CMD ["bash"]
# Mon, 01 Jul 2024 19:20:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 01 Jul 2024 19:20:29 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 01 Jul 2024 19:20:29 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 01 Jul 2024 19:20:29 GMT
ENV TELEGRAF_VERSION=1.31.1
# Mon, 01 Jul 2024 19:20:29 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 01 Jul 2024 19:20:29 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 01 Jul 2024 19:20:29 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 01 Jul 2024 19:20:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 01 Jul 2024 19:20:29 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:e9aef93137af6e967e7242f3b3c8ecd8e6f571d1e6fdd9e72db0befeeae3cf13`  
		Last Modified: Tue, 02 Jul 2024 01:28:26 GMT  
		Size: 49.6 MB (49554064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58b365fa3e8dc16e70d89fab0e91f5242feb38ae3cfeb6655e654209ea109333`  
		Last Modified: Tue, 02 Jul 2024 02:00:17 GMT  
		Size: 24.0 MB (24049794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73640a629d5c024f9dfe1e45997e798ee73d8a1610b0f3b8323574909a371251`  
		Last Modified: Tue, 02 Jul 2024 03:32:15 GMT  
		Size: 18.9 MB (18947959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b734f825ca42c8b2531d5b7bff4a2fd773b28e939e01ba10cd88aba8b1d5923`  
		Last Modified: Tue, 02 Jul 2024 03:32:14 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5592f5a587d7f8eedb6976959e4f68eced16e31fd88eadca308608811f4f2ee5`  
		Last Modified: Tue, 02 Jul 2024 03:32:15 GMT  
		Size: 66.2 MB (66227197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1345e4c69b07d7c081836490c21d7fdcf540c9048e4dd30fc6cbb845c5c9e0a`  
		Last Modified: Tue, 02 Jul 2024 03:32:14 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:acb0bd848143d98105741c38a6e2c59d0374115be8f9da3c9133fd7d86110f84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6318988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16d34bd18c3254b1f26fe2d3a73e22e781ba64cde20b65d21cbddcb43fac5ff1`

```dockerfile
```

-	Layers:
	-	`sha256:64ff97c343edd9924cbb0d64971baecadd617383c57598cc79313feb2f8abd2e`  
		Last Modified: Tue, 02 Jul 2024 03:32:14 GMT  
		Size: 6.3 MB (6304363 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e60e4cc25bb1bf81857c3e626e050e6bbef9703b8b409cb67cc933378595b25`  
		Last Modified: Tue, 02 Jul 2024 03:32:14 GMT  
		Size: 14.6 KB (14625 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:bd326c1e04da02a6334b2adc11a33126fb5f4bca543e27fb7f6e835937dd7529
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.4 MB (146430538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c6c497ad4bd877235dc727f34b836a9683c7066e9b23174518c7505c40f0810`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 01 Jul 2024 19:20:29 GMT
ADD file:526dbb34ac449ae8f3c9025d71b3ffeb0e24fa5dc1a01da707f0a8b834eb4e33 in / 
# Mon, 01 Jul 2024 19:20:29 GMT
CMD ["bash"]
# Mon, 01 Jul 2024 19:20:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 01 Jul 2024 19:20:29 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 01 Jul 2024 19:20:29 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 01 Jul 2024 19:20:29 GMT
ENV TELEGRAF_VERSION=1.31.1
# Mon, 01 Jul 2024 19:20:29 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 01 Jul 2024 19:20:29 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 01 Jul 2024 19:20:29 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 01 Jul 2024 19:20:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 01 Jul 2024 19:20:29 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:335f2c484898b910fac13d5650ed3c78e5e673fe8dab1b06a071c71478a153d0`  
		Last Modified: Tue, 02 Jul 2024 01:02:57 GMT  
		Size: 45.1 MB (45148097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aa30b2bcbde45c2fc67abf425197af3af3e67d55296f168143343ef1b0e2d3e`  
		Last Modified: Tue, 02 Jul 2024 01:39:04 GMT  
		Size: 22.0 MB (21954038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac7a987fd3254b4eb8a2e6cc7206b9d5eac3e938a9d3c13d8fa167031b4fbcce`  
		Last Modified: Wed, 03 Jul 2024 01:34:48 GMT  
		Size: 17.7 MB (17724841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e17cfe5d83da74d5e8c4d81b008e6599fc7cca1105639345e4bf236669c7f0c5`  
		Last Modified: Wed, 03 Jul 2024 01:34:47 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffb5b65e557f72b22f833c43955f3c8d36093fd4040e5d8d436bc2f39dd8362a`  
		Last Modified: Wed, 03 Jul 2024 01:36:38 GMT  
		Size: 61.6 MB (61601152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20f5ed5bd1d96e3bf9e9b6f47eaf1e1aa50042560ddc6f546da60292553a2f16`  
		Last Modified: Wed, 03 Jul 2024 01:36:35 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:e031f34a1bc0b974683b355de0553a9bc75a572a724cdc37cb87839c016959a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6315093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05d317ad92eb5361752a0696f2725b1f92deff7bdddfb49f36188c03b20af44d`

```dockerfile
```

-	Layers:
	-	`sha256:1aab98ed50ba77997063ac8e4d303152b55a27f70a4465de6fdbf5fa1404f018`  
		Last Modified: Wed, 03 Jul 2024 01:36:36 GMT  
		Size: 6.3 MB (6300379 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e1b16159e9459b5b279a5f297fc73228d4d21f3d2996504fdb2f28a9eeb1c55`  
		Last Modified: Wed, 03 Jul 2024 01:36:35 GMT  
		Size: 14.7 KB (14714 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:9df7de5c3c95b0f72771ffa58f2b9a5a5dcf22b41b63a6b9fb244244a06e3249
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.3 MB (152336093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08fce67cb8fa54d34a54c6266529978c8db1a3d91fb2a8f72cc4ad46e963d103`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 01 Jul 2024 19:20:29 GMT
ADD file:696648070a57689a69a184fda234045f7be4a8a9f3b2fff9031ff0a2d9914113 in / 
# Mon, 01 Jul 2024 19:20:29 GMT
CMD ["bash"]
# Mon, 01 Jul 2024 19:20:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 01 Jul 2024 19:20:29 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 01 Jul 2024 19:20:29 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 01 Jul 2024 19:20:29 GMT
ENV TELEGRAF_VERSION=1.31.1
# Mon, 01 Jul 2024 19:20:29 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 01 Jul 2024 19:20:29 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 01 Jul 2024 19:20:29 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 01 Jul 2024 19:20:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 01 Jul 2024 19:20:29 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:0bd1f8180c504ba389021ce74895ed487ccd8c70e2d9af3707934bc801ba28d8`  
		Last Modified: Tue, 02 Jul 2024 00:42:03 GMT  
		Size: 49.6 MB (49588448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b16610496e73ba3d120d519598b53fa8a2db4c80ccc097a5016ad44aedd0654b`  
		Last Modified: Tue, 02 Jul 2024 04:01:41 GMT  
		Size: 23.6 MB (23591145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49fa4258ace16a879b6bae48191a62329ef9150aaf9ac97497e6d6c0f3d622aa`  
		Last Modified: Wed, 03 Jul 2024 00:51:44 GMT  
		Size: 18.9 MB (18870342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c86c902d4b3d360929e7f2bfb7aebbb19eb7c0bd8f515cf202c7fe68e2315b58`  
		Last Modified: Wed, 03 Jul 2024 00:51:43 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53711602d3ab9a60d8d35c9202bbe4620c8c8fd1888fb16601d4bf36e311690b`  
		Last Modified: Wed, 03 Jul 2024 00:52:55 GMT  
		Size: 60.3 MB (60283753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78887db2826f45f52baafab97c61e63c1124243fd6cae85e2f8c3a06853036b3`  
		Last Modified: Wed, 03 Jul 2024 00:52:53 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:0e7d3e64ffa05e5ff13896af64e5aaf547d82c4b22de2a8b5630b0e6470f196f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6321250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f69bceb31f7804c7610329c5a403aba38aa8a6e6b8c4aeb879381d81b7bbeba`

```dockerfile
```

-	Layers:
	-	`sha256:152e5903a51b12964d1ec93c4d2aa0b4929a87744964442b58e3d753aa892a59`  
		Last Modified: Wed, 03 Jul 2024 00:52:54 GMT  
		Size: 6.3 MB (6306319 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d3e466a2111dd26c94480a8dc228e399e4ddfd66f64147958a1783efa147799`  
		Last Modified: Wed, 03 Jul 2024 00:52:53 GMT  
		Size: 14.9 KB (14931 bytes)  
		MIME: application/vnd.in-toto+json
