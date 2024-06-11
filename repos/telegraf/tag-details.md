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
-	[`telegraf:1.31.0`](#telegraf1310)
-	[`telegraf:1.31.0-alpine`](#telegraf1310-alpine)
-	[`telegraf:alpine`](#telegrafalpine)
-	[`telegraf:latest`](#telegraflatest)

## `telegraf:1.29`

```console
$ docker pull telegraf@sha256:a09248dc4950964000961fb1940cacdb79c3f034585996ace204c6fc6599e269
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
$ docker pull telegraf@sha256:fdf74958f1c7ccdf9663486165d2ea38ca107c60593e8a431c85287e60bd8620
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.2 MB (155219321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c274cffe01a623946a40f5bcf711eeaa6c1c687ce4311ee2d144cde2662e6f1a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 14 May 2024 01:27:51 GMT
ADD file:b9a9fc37b874060c713002ae1ac220f097edd7c6576116c22bb15aad8229b1b3 in / 
# Tue, 14 May 2024 01:27:51 GMT
CMD ["bash"]
# Tue, 14 May 2024 02:54:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 10 Jun 2024 21:05:04 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
ENV TELEGRAF_VERSION=1.29.5
# Mon, 10 Jun 2024 21:05:04 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
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
	-	`sha256:c6cf28de8a067787ee0d08f8b01d7f1566a508b56f6e549687b41dfd375f12c7`  
		Last Modified: Tue, 14 May 2024 01:32:07 GMT  
		Size: 49.6 MB (49576390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:891494355808bdd3db5552f0d3723fd0fa826675f774853796fafa221d850d42`  
		Last Modified: Tue, 14 May 2024 03:04:06 GMT  
		Size: 24.1 MB (24050100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:767aa67f593b02a438b4f1941e89f2302bfee1575dd9b612e632e541f5a42e89`  
		Last Modified: Mon, 10 Jun 2024 22:33:05 GMT  
		Size: 18.9 MB (18947919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99e7f8c83b0376208cc67f097e49d3743b08799e7facfe9481f04d850addf789`  
		Last Modified: Mon, 10 Jun 2024 22:33:04 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4b5778ff67eab050d02806f6a3f9ca50132d24caf144c347cb04bac8bf76bfc`  
		Last Modified: Mon, 10 Jun 2024 22:33:06 GMT  
		Size: 62.6 MB (62642518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3297c3e84d61216630b2b3e04e62d6343a796335063a9e9c864497c1f8112d9`  
		Last Modified: Mon, 10 Jun 2024 22:33:04 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.29` - unknown; unknown

```console
$ docker pull telegraf@sha256:ea381ef0670cacf0a47553b81d4ce5f6293366858241efd6499cb13a156b4b70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6313528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca98bc97991e492586ab396d2186fd2b9be2142fdfcdad4d04205a4d65c7c20a`

```dockerfile
```

-	Layers:
	-	`sha256:263204a0983af8e762143f500b6672a7f0dd42f4781332c881f7543a7842cee0`  
		Last Modified: Mon, 10 Jun 2024 22:33:05 GMT  
		Size: 6.3 MB (6299204 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:630a37db67e85565288fa457074a0093f2ba597d60c0b31b84eadd6770b41bd6`  
		Last Modified: Mon, 10 Jun 2024 22:33:04 GMT  
		Size: 14.3 KB (14324 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.29` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:50539a5172b37355b1d5e36ba7467396bf12042c4fb75b085d2779b80409d2dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.8 MB (142840876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a7a3bd64dae3fac8f6756491aede3d7602036ddf1bf3fea37d9d2c3e99367ba`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 22 Apr 2024 19:40:36 GMT
ADD file:1e106a38a0e44ca74d4d29c6d797780e7a29ffe249e473c48ee2aea553fc013b in / 
# Mon, 22 Apr 2024 19:40:36 GMT
CMD ["bash"]
# Mon, 22 Apr 2024 19:40:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 22 Apr 2024 19:40:36 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
ENV TELEGRAF_VERSION=1.29.5
# Mon, 22 Apr 2024 19:40:36 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 22 Apr 2024 19:40:36 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Apr 2024 19:40:36 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:dfc3b4ca62816a9cbf2bdfbdd78bf692a522e7f48a280492b9f87d55b2f4aa2e`  
		Last Modified: Tue, 14 May 2024 01:12:21 GMT  
		Size: 45.2 MB (45174745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:641d6443415d538c3bf0e0d6ecc0f6b7603b4caf6c79708d0670bc082e9721c5`  
		Last Modified: Tue, 14 May 2024 01:46:47 GMT  
		Size: 22.0 MB (21953893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:901b8b18d82e5b57b89385ec062d1674265344d73cca05bba989b96a6cf4f07a`  
		Last Modified: Wed, 15 May 2024 08:08:19 GMT  
		Size: 17.7 MB (17724872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6537ab1b98b6a7364bac3f994ad624855097573d29bfa741f0a5f24eaffe2bc`  
		Last Modified: Wed, 15 May 2024 08:08:18 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d34565240b6b46582dc1f7536d7c8634c9de18556ba88471f0498a22982cfc89`  
		Last Modified: Wed, 15 May 2024 08:09:16 GMT  
		Size: 58.0 MB (57984958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aca097afe6f5e7b7f0f9312c750eb3d234676c7af26891524f92625af8bd88a7`  
		Last Modified: Wed, 15 May 2024 08:09:13 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.29` - unknown; unknown

```console
$ docker pull telegraf@sha256:fb6376b03dde60320d7c9df26a7f782473293d255ca9274eab90de5e8ecfa746
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6308912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17d2a57dd94e7092a1eb03c6e303a858852a7e8f6e6744b4c59df5f063a7d061`

```dockerfile
```

-	Layers:
	-	`sha256:ff94f078643ee1854983575c9efa631670a6d369f65c91eaa26ffb6513147d13`  
		Last Modified: Wed, 15 May 2024 08:09:13 GMT  
		Size: 6.3 MB (6294557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92740553fccafd94b394d18313c167167c3c906a8cb1b2f3e3545ec140730dff`  
		Last Modified: Wed, 15 May 2024 08:09:13 GMT  
		Size: 14.4 KB (14355 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.29` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:d6d99e8b11055e02d9100541246500d269a56d09bceb879c9d4154dae3aaa853
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.1 MB (149054248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6f6f776ed66f32275284b64f32c759b86d031960beb72aaa778eb1f8a39e5eb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 22 Apr 2024 19:40:36 GMT
ADD file:b7c55dda8ded4219a7cdc9fbd91dfb5996c4886d4394b85751c2f956defe3287 in / 
# Mon, 22 Apr 2024 19:40:36 GMT
CMD ["bash"]
# Mon, 22 Apr 2024 19:40:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 22 Apr 2024 19:40:36 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
ENV TELEGRAF_VERSION=1.29.5
# Mon, 22 Apr 2024 19:40:36 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 22 Apr 2024 19:40:36 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Apr 2024 19:40:36 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:91e301773f03e9e0fabc5c177fe6bfe8daf14e992ab816f151692b814ddc462c`  
		Last Modified: Tue, 14 May 2024 00:42:35 GMT  
		Size: 49.6 MB (49613388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15856ca26414127b85cee6d10acbc4cee6eba9070f3f5a04b9cc72ce95abfa7f`  
		Last Modified: Tue, 14 May 2024 01:52:50 GMT  
		Size: 23.6 MB (23586610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787c90cc4c220f2efc01fd1f87a403a247f61d1030f562e906930332d905ebdb`  
		Last Modified: Wed, 15 May 2024 15:06:57 GMT  
		Size: 18.9 MB (18870680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a23862d11452a5b51a68997e785996fd1e75da32dd2d37041a0da1bf5f6d58f9`  
		Last Modified: Wed, 15 May 2024 15:06:56 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb0dae6f5810096e015fcb70cd4c3119441ff59d41205054c3c3eb8f94f391c5`  
		Last Modified: Wed, 15 May 2024 15:07:36 GMT  
		Size: 57.0 MB (56981163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bcb9733f8d9309b1fa960e53eaf4975cc5d12868531689e77a37a1b50d2b562`  
		Last Modified: Wed, 15 May 2024 15:07:34 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.29` - unknown; unknown

```console
$ docker pull telegraf@sha256:6f32ae9aeb4b9a57e103d236d75b4778e8ea39fc45f98927296d4cccf02a6a05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6314097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fad558760ed28c457e71f4f9d1c7a2d9423fc80dcb4ee78c5bf8b38b2c89770d`

```dockerfile
```

-	Layers:
	-	`sha256:0d084e7250c431be223550543e9f1088da83f3e71904883273aa7f4533e95789`  
		Last Modified: Wed, 15 May 2024 15:07:34 GMT  
		Size: 6.3 MB (6299816 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f63f8fe3a658e8e54453540e6c0bbb2cd09de454514c01d52b2b0379a8111d1`  
		Last Modified: Wed, 15 May 2024 15:07:34 GMT  
		Size: 14.3 KB (14281 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.29-alpine`

```console
$ docker pull telegraf@sha256:7c82e1b400f8d60ac89f563a288bce6114bc7caf96276966996f151602b796c1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.29-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:9dd41527f4aec527c54dac5489e9073f063266d5c5efd3398adeed5cbf7d98bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.5 MB (68516750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea8a87978418c4c2d8160cfc08a87984d1f5222e96516b8c01d6f2f850694542`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
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
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a31d3de31608c4eb37a8e9376bbeb0eb2468211670138269f2a723eea57f0db`  
		Last Modified: Mon, 10 Jun 2024 22:32:53 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d76b59fd6c6c8d456f928a8490e18e2c0dd6521166b794772ca68442b864fcad`  
		Last Modified: Mon, 10 Jun 2024 22:32:53 GMT  
		Size: 2.5 MB (2452611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8afec1fadba3792188f75befcedcf6745481fdd4d436734ed545401d9530ac79`  
		Last Modified: Mon, 10 Jun 2024 22:32:56 GMT  
		Size: 62.4 MB (62441437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb291c63e2c6cb0638ea6bfa58dba44ab7783743243a03e38c03e81fd2a8fe0e`  
		Last Modified: Mon, 10 Jun 2024 22:32:53 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.29-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:bc6766eaeb901deabdc98ed153853a36dc653073278b792cd7ad7938b408358b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1001194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23830580687972e6f1a70eb533c6434b84da22357e854abc46975f5de181038e`

```dockerfile
```

-	Layers:
	-	`sha256:028b70ee210d02f746331b6f94fbc32a8d83f03f295dd86ee07d52c8452f397e`  
		Last Modified: Mon, 10 Jun 2024 22:32:54 GMT  
		Size: 986.5 KB (986460 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ba463340c58a912d6b7db43f4186a311031f0cb69f8ac46b87f67abc37149fe`  
		Last Modified: Mon, 10 Jun 2024 22:32:54 GMT  
		Size: 14.7 KB (14734 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.29-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:008197f6b39fe8b7e4e013e8574523e8cda2be226f7449cdc21ae45cc96e38c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.8 MB (62849729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2bc39888daf763e890d415946b487839e389683b7796d00c03ac3ccc5748287`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Mon, 22 Apr 2024 19:40:36 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
ENV TELEGRAF_VERSION=1.29.5
# Mon, 22 Apr 2024 19:40:36 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 22 Apr 2024 19:40:36 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Apr 2024 19:40:36 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ddde0fe2ef8e41514be0d2d260ff46c7fa8adda5734b6aeb56e6ba0b174c9b1`  
		Last Modified: Wed, 01 May 2024 22:33:41 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abfb31b2d6527f81d9d04ddd4779a6ecdac4257e8769d6d10af4516be1c7b4c2`  
		Last Modified: Wed, 01 May 2024 22:33:42 GMT  
		Size: 2.7 MB (2702917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3254b71ee2dea015969e2c70ba06e521a4b4a8e66936d7d30eb4ad716ec2d81`  
		Last Modified: Wed, 01 May 2024 22:34:57 GMT  
		Size: 56.8 MB (56798489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53e47e8478949e8acbaeeb3374a1fe9cb324fe86a25bcdade81a0b694dfaee7b`  
		Last Modified: Wed, 01 May 2024 22:34:56 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.29-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:c8c312ea591a35828406adca49789bc0c872ba3256226303d289ce0c5b62160e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 MB (1375450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d06fd9a6199d3e70d2c201f8e8db94b36694f4dbb05aa873ff0e720fa9f9d01`

```dockerfile
```

-	Layers:
	-	`sha256:79da5a86dca22346c1dfc562e88f1d5dd2c719a261768ce63c0b0f8b80686c3a`  
		Last Modified: Wed, 01 May 2024 22:34:56 GMT  
		Size: 1.4 MB (1360760 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8470e678dcf0a7858cf8713ddcaf2a7e4da81c32b23a55f2aeed8b51301b287`  
		Last Modified: Wed, 01 May 2024 22:34:55 GMT  
		Size: 14.7 KB (14690 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.29.5`

```console
$ docker pull telegraf@sha256:a09248dc4950964000961fb1940cacdb79c3f034585996ace204c6fc6599e269
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
$ docker pull telegraf@sha256:fdf74958f1c7ccdf9663486165d2ea38ca107c60593e8a431c85287e60bd8620
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.2 MB (155219321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c274cffe01a623946a40f5bcf711eeaa6c1c687ce4311ee2d144cde2662e6f1a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 14 May 2024 01:27:51 GMT
ADD file:b9a9fc37b874060c713002ae1ac220f097edd7c6576116c22bb15aad8229b1b3 in / 
# Tue, 14 May 2024 01:27:51 GMT
CMD ["bash"]
# Tue, 14 May 2024 02:54:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 10 Jun 2024 21:05:04 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
ENV TELEGRAF_VERSION=1.29.5
# Mon, 10 Jun 2024 21:05:04 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
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
	-	`sha256:c6cf28de8a067787ee0d08f8b01d7f1566a508b56f6e549687b41dfd375f12c7`  
		Last Modified: Tue, 14 May 2024 01:32:07 GMT  
		Size: 49.6 MB (49576390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:891494355808bdd3db5552f0d3723fd0fa826675f774853796fafa221d850d42`  
		Last Modified: Tue, 14 May 2024 03:04:06 GMT  
		Size: 24.1 MB (24050100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:767aa67f593b02a438b4f1941e89f2302bfee1575dd9b612e632e541f5a42e89`  
		Last Modified: Mon, 10 Jun 2024 22:33:05 GMT  
		Size: 18.9 MB (18947919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99e7f8c83b0376208cc67f097e49d3743b08799e7facfe9481f04d850addf789`  
		Last Modified: Mon, 10 Jun 2024 22:33:04 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4b5778ff67eab050d02806f6a3f9ca50132d24caf144c347cb04bac8bf76bfc`  
		Last Modified: Mon, 10 Jun 2024 22:33:06 GMT  
		Size: 62.6 MB (62642518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3297c3e84d61216630b2b3e04e62d6343a796335063a9e9c864497c1f8112d9`  
		Last Modified: Mon, 10 Jun 2024 22:33:04 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.29.5` - unknown; unknown

```console
$ docker pull telegraf@sha256:ea381ef0670cacf0a47553b81d4ce5f6293366858241efd6499cb13a156b4b70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6313528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca98bc97991e492586ab396d2186fd2b9be2142fdfcdad4d04205a4d65c7c20a`

```dockerfile
```

-	Layers:
	-	`sha256:263204a0983af8e762143f500b6672a7f0dd42f4781332c881f7543a7842cee0`  
		Last Modified: Mon, 10 Jun 2024 22:33:05 GMT  
		Size: 6.3 MB (6299204 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:630a37db67e85565288fa457074a0093f2ba597d60c0b31b84eadd6770b41bd6`  
		Last Modified: Mon, 10 Jun 2024 22:33:04 GMT  
		Size: 14.3 KB (14324 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.29.5` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:50539a5172b37355b1d5e36ba7467396bf12042c4fb75b085d2779b80409d2dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.8 MB (142840876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a7a3bd64dae3fac8f6756491aede3d7602036ddf1bf3fea37d9d2c3e99367ba`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 22 Apr 2024 19:40:36 GMT
ADD file:1e106a38a0e44ca74d4d29c6d797780e7a29ffe249e473c48ee2aea553fc013b in / 
# Mon, 22 Apr 2024 19:40:36 GMT
CMD ["bash"]
# Mon, 22 Apr 2024 19:40:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 22 Apr 2024 19:40:36 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
ENV TELEGRAF_VERSION=1.29.5
# Mon, 22 Apr 2024 19:40:36 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 22 Apr 2024 19:40:36 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Apr 2024 19:40:36 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:dfc3b4ca62816a9cbf2bdfbdd78bf692a522e7f48a280492b9f87d55b2f4aa2e`  
		Last Modified: Tue, 14 May 2024 01:12:21 GMT  
		Size: 45.2 MB (45174745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:641d6443415d538c3bf0e0d6ecc0f6b7603b4caf6c79708d0670bc082e9721c5`  
		Last Modified: Tue, 14 May 2024 01:46:47 GMT  
		Size: 22.0 MB (21953893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:901b8b18d82e5b57b89385ec062d1674265344d73cca05bba989b96a6cf4f07a`  
		Last Modified: Wed, 15 May 2024 08:08:19 GMT  
		Size: 17.7 MB (17724872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6537ab1b98b6a7364bac3f994ad624855097573d29bfa741f0a5f24eaffe2bc`  
		Last Modified: Wed, 15 May 2024 08:08:18 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d34565240b6b46582dc1f7536d7c8634c9de18556ba88471f0498a22982cfc89`  
		Last Modified: Wed, 15 May 2024 08:09:16 GMT  
		Size: 58.0 MB (57984958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aca097afe6f5e7b7f0f9312c750eb3d234676c7af26891524f92625af8bd88a7`  
		Last Modified: Wed, 15 May 2024 08:09:13 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.29.5` - unknown; unknown

```console
$ docker pull telegraf@sha256:fb6376b03dde60320d7c9df26a7f782473293d255ca9274eab90de5e8ecfa746
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6308912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17d2a57dd94e7092a1eb03c6e303a858852a7e8f6e6744b4c59df5f063a7d061`

```dockerfile
```

-	Layers:
	-	`sha256:ff94f078643ee1854983575c9efa631670a6d369f65c91eaa26ffb6513147d13`  
		Last Modified: Wed, 15 May 2024 08:09:13 GMT  
		Size: 6.3 MB (6294557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92740553fccafd94b394d18313c167167c3c906a8cb1b2f3e3545ec140730dff`  
		Last Modified: Wed, 15 May 2024 08:09:13 GMT  
		Size: 14.4 KB (14355 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.29.5` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:d6d99e8b11055e02d9100541246500d269a56d09bceb879c9d4154dae3aaa853
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.1 MB (149054248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6f6f776ed66f32275284b64f32c759b86d031960beb72aaa778eb1f8a39e5eb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 22 Apr 2024 19:40:36 GMT
ADD file:b7c55dda8ded4219a7cdc9fbd91dfb5996c4886d4394b85751c2f956defe3287 in / 
# Mon, 22 Apr 2024 19:40:36 GMT
CMD ["bash"]
# Mon, 22 Apr 2024 19:40:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 22 Apr 2024 19:40:36 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
ENV TELEGRAF_VERSION=1.29.5
# Mon, 22 Apr 2024 19:40:36 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 22 Apr 2024 19:40:36 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Apr 2024 19:40:36 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:91e301773f03e9e0fabc5c177fe6bfe8daf14e992ab816f151692b814ddc462c`  
		Last Modified: Tue, 14 May 2024 00:42:35 GMT  
		Size: 49.6 MB (49613388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15856ca26414127b85cee6d10acbc4cee6eba9070f3f5a04b9cc72ce95abfa7f`  
		Last Modified: Tue, 14 May 2024 01:52:50 GMT  
		Size: 23.6 MB (23586610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787c90cc4c220f2efc01fd1f87a403a247f61d1030f562e906930332d905ebdb`  
		Last Modified: Wed, 15 May 2024 15:06:57 GMT  
		Size: 18.9 MB (18870680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a23862d11452a5b51a68997e785996fd1e75da32dd2d37041a0da1bf5f6d58f9`  
		Last Modified: Wed, 15 May 2024 15:06:56 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb0dae6f5810096e015fcb70cd4c3119441ff59d41205054c3c3eb8f94f391c5`  
		Last Modified: Wed, 15 May 2024 15:07:36 GMT  
		Size: 57.0 MB (56981163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bcb9733f8d9309b1fa960e53eaf4975cc5d12868531689e77a37a1b50d2b562`  
		Last Modified: Wed, 15 May 2024 15:07:34 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.29.5` - unknown; unknown

```console
$ docker pull telegraf@sha256:6f32ae9aeb4b9a57e103d236d75b4778e8ea39fc45f98927296d4cccf02a6a05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6314097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fad558760ed28c457e71f4f9d1c7a2d9423fc80dcb4ee78c5bf8b38b2c89770d`

```dockerfile
```

-	Layers:
	-	`sha256:0d084e7250c431be223550543e9f1088da83f3e71904883273aa7f4533e95789`  
		Last Modified: Wed, 15 May 2024 15:07:34 GMT  
		Size: 6.3 MB (6299816 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f63f8fe3a658e8e54453540e6c0bbb2cd09de454514c01d52b2b0379a8111d1`  
		Last Modified: Wed, 15 May 2024 15:07:34 GMT  
		Size: 14.3 KB (14281 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.29.5-alpine`

```console
$ docker pull telegraf@sha256:7c82e1b400f8d60ac89f563a288bce6114bc7caf96276966996f151602b796c1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.29.5-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:9dd41527f4aec527c54dac5489e9073f063266d5c5efd3398adeed5cbf7d98bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.5 MB (68516750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea8a87978418c4c2d8160cfc08a87984d1f5222e96516b8c01d6f2f850694542`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
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
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a31d3de31608c4eb37a8e9376bbeb0eb2468211670138269f2a723eea57f0db`  
		Last Modified: Mon, 10 Jun 2024 22:32:53 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d76b59fd6c6c8d456f928a8490e18e2c0dd6521166b794772ca68442b864fcad`  
		Last Modified: Mon, 10 Jun 2024 22:32:53 GMT  
		Size: 2.5 MB (2452611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8afec1fadba3792188f75befcedcf6745481fdd4d436734ed545401d9530ac79`  
		Last Modified: Mon, 10 Jun 2024 22:32:56 GMT  
		Size: 62.4 MB (62441437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb291c63e2c6cb0638ea6bfa58dba44ab7783743243a03e38c03e81fd2a8fe0e`  
		Last Modified: Mon, 10 Jun 2024 22:32:53 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.29.5-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:bc6766eaeb901deabdc98ed153853a36dc653073278b792cd7ad7938b408358b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1001194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23830580687972e6f1a70eb533c6434b84da22357e854abc46975f5de181038e`

```dockerfile
```

-	Layers:
	-	`sha256:028b70ee210d02f746331b6f94fbc32a8d83f03f295dd86ee07d52c8452f397e`  
		Last Modified: Mon, 10 Jun 2024 22:32:54 GMT  
		Size: 986.5 KB (986460 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ba463340c58a912d6b7db43f4186a311031f0cb69f8ac46b87f67abc37149fe`  
		Last Modified: Mon, 10 Jun 2024 22:32:54 GMT  
		Size: 14.7 KB (14734 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.29.5-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:008197f6b39fe8b7e4e013e8574523e8cda2be226f7449cdc21ae45cc96e38c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.8 MB (62849729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2bc39888daf763e890d415946b487839e389683b7796d00c03ac3ccc5748287`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Mon, 22 Apr 2024 19:40:36 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
ENV TELEGRAF_VERSION=1.29.5
# Mon, 22 Apr 2024 19:40:36 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 22 Apr 2024 19:40:36 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Apr 2024 19:40:36 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ddde0fe2ef8e41514be0d2d260ff46c7fa8adda5734b6aeb56e6ba0b174c9b1`  
		Last Modified: Wed, 01 May 2024 22:33:41 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abfb31b2d6527f81d9d04ddd4779a6ecdac4257e8769d6d10af4516be1c7b4c2`  
		Last Modified: Wed, 01 May 2024 22:33:42 GMT  
		Size: 2.7 MB (2702917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3254b71ee2dea015969e2c70ba06e521a4b4a8e66936d7d30eb4ad716ec2d81`  
		Last Modified: Wed, 01 May 2024 22:34:57 GMT  
		Size: 56.8 MB (56798489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53e47e8478949e8acbaeeb3374a1fe9cb324fe86a25bcdade81a0b694dfaee7b`  
		Last Modified: Wed, 01 May 2024 22:34:56 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.29.5-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:c8c312ea591a35828406adca49789bc0c872ba3256226303d289ce0c5b62160e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 MB (1375450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d06fd9a6199d3e70d2c201f8e8db94b36694f4dbb05aa873ff0e720fa9f9d01`

```dockerfile
```

-	Layers:
	-	`sha256:79da5a86dca22346c1dfc562e88f1d5dd2c719a261768ce63c0b0f8b80686c3a`  
		Last Modified: Wed, 01 May 2024 22:34:56 GMT  
		Size: 1.4 MB (1360760 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8470e678dcf0a7858cf8713ddcaf2a7e4da81c32b23a55f2aeed8b51301b287`  
		Last Modified: Wed, 01 May 2024 22:34:55 GMT  
		Size: 14.7 KB (14690 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.30`

```console
$ docker pull telegraf@sha256:f2e67caa9551063cceb419c6c237f381fc3065e3bebcd4518771de8905c84aab
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
$ docker pull telegraf@sha256:1536a0e21425afcbf83415a27903eba63c4ff33c232ff12e5ab878e048932458
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.3 MB (155343262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3eb3db616f9429922c1ad42967f050369335cba406e8363e6481680fab647ed`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 14 May 2024 01:27:51 GMT
ADD file:b9a9fc37b874060c713002ae1ac220f097edd7c6576116c22bb15aad8229b1b3 in / 
# Tue, 14 May 2024 01:27:51 GMT
CMD ["bash"]
# Tue, 14 May 2024 02:54:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 10 Jun 2024 21:05:04 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
ENV TELEGRAF_VERSION=1.30.3
# Mon, 10 Jun 2024 21:05:04 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
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
	-	`sha256:c6cf28de8a067787ee0d08f8b01d7f1566a508b56f6e549687b41dfd375f12c7`  
		Last Modified: Tue, 14 May 2024 01:32:07 GMT  
		Size: 49.6 MB (49576390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:891494355808bdd3db5552f0d3723fd0fa826675f774853796fafa221d850d42`  
		Last Modified: Tue, 14 May 2024 03:04:06 GMT  
		Size: 24.1 MB (24050100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e969ad6682604967a9717b77c98a6d0e86dbb701f9fa7ea34e83813870cbd3b`  
		Last Modified: Mon, 10 Jun 2024 22:33:05 GMT  
		Size: 18.9 MB (18947891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a63d41fe6b8ce94b5889480fa7a950106fc4c72448bea0eaca69e23a35310d2d`  
		Last Modified: Mon, 10 Jun 2024 22:33:04 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0732158ba65379866405f93434e703e89dbe155c9376d577a0f02d76acd99fee`  
		Last Modified: Mon, 10 Jun 2024 22:33:07 GMT  
		Size: 62.8 MB (62766475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3297c3e84d61216630b2b3e04e62d6343a796335063a9e9c864497c1f8112d9`  
		Last Modified: Mon, 10 Jun 2024 22:33:04 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.30` - unknown; unknown

```console
$ docker pull telegraf@sha256:bdc24167f9300b693687cbd3ff3326ab7e9fef015427a84d55c63ab50c4b0983
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6313807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46ac369e730184e4c5733be0af0391f32adfccfd72fd8277d13bb96d4bb683e3`

```dockerfile
```

-	Layers:
	-	`sha256:9272ea8c421cbf05fc7094eb44749f70d6cadbf05a83410429dd99ec0bb16f11`  
		Last Modified: Mon, 10 Jun 2024 22:33:05 GMT  
		Size: 6.3 MB (6299484 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de9fff0ee2e3d6fe2fff05993a092dd3b095bcc6cf39e44392a835c3204448da`  
		Last Modified: Mon, 10 Jun 2024 22:33:04 GMT  
		Size: 14.3 KB (14323 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.30` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:0937b1a222978be919cb00df24cdcfa62d8a100dccab0ab3776ccfba19e31a02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.1 MB (143068661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a2f8ba5cd8962f90e947f7fe1309436728ed13ef21c5fb8bf4dab976ef3b3cb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 14 May 2024 01:08:35 GMT
ADD file:1e106a38a0e44ca74d4d29c6d797780e7a29ffe249e473c48ee2aea553fc013b in / 
# Tue, 14 May 2024 01:08:36 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:35:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 May 2024 14:13:49 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 May 2024 14:13:49 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 21 May 2024 14:13:49 GMT
ENV TELEGRAF_VERSION=1.30.3
# Tue, 21 May 2024 14:13:49 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 21 May 2024 14:13:49 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 21 May 2024 14:13:49 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 21 May 2024 14:13:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 May 2024 14:13:49 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:dfc3b4ca62816a9cbf2bdfbdd78bf692a522e7f48a280492b9f87d55b2f4aa2e`  
		Last Modified: Tue, 14 May 2024 01:12:21 GMT  
		Size: 45.2 MB (45174745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:641d6443415d538c3bf0e0d6ecc0f6b7603b4caf6c79708d0670bc082e9721c5`  
		Last Modified: Tue, 14 May 2024 01:46:47 GMT  
		Size: 22.0 MB (21953893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:901b8b18d82e5b57b89385ec062d1674265344d73cca05bba989b96a6cf4f07a`  
		Last Modified: Wed, 15 May 2024 08:08:19 GMT  
		Size: 17.7 MB (17724872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6537ab1b98b6a7364bac3f994ad624855097573d29bfa741f0a5f24eaffe2bc`  
		Last Modified: Wed, 15 May 2024 08:08:18 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f4a236ed04d98e4dbbd6c88b87392bd54e369cfbb75ba5afcace4dbb33b6ef`  
		Last Modified: Tue, 21 May 2024 18:08:27 GMT  
		Size: 58.2 MB (58212744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd8eaaf18c8e5e6fb3073500e84a83e0722dc3b3231c64d24a578c283338d60c`  
		Last Modified: Tue, 21 May 2024 18:08:25 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.30` - unknown; unknown

```console
$ docker pull telegraf@sha256:ea09a00736aecf132e6b185eabe3f050148ea41c066980dd8d9cc03768abd799
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6309812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:419e20c776b8b40e3ad5056c424586ebfdd0254d17d6d87c07cc05f3bf274422`

```dockerfile
```

-	Layers:
	-	`sha256:be92ac005ea43268c72221d35410b3ffe5cda8c51a0f7fb2d095fc2a8259e1c6`  
		Last Modified: Tue, 21 May 2024 18:08:25 GMT  
		Size: 6.3 MB (6295147 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b6d8ab8fcfcde216a402b8bedfe934dd5adae59f9659864fff791d9ef974c86`  
		Last Modified: Tue, 21 May 2024 18:08:25 GMT  
		Size: 14.7 KB (14665 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.30` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:d062d9a32a4d87ea479fa7887bcb7813c9139badfdda83620cbaf1317f0d885b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.2 MB (149196386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e9e574432b44679b03199dc4767cc26b2d1f2c504cf5053af7a32a97cf038c6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 14 May 2024 00:39:32 GMT
ADD file:b7c55dda8ded4219a7cdc9fbd91dfb5996c4886d4394b85751c2f956defe3287 in / 
# Tue, 14 May 2024 00:39:33 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:44:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 May 2024 14:13:49 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 May 2024 14:13:49 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 21 May 2024 14:13:49 GMT
ENV TELEGRAF_VERSION=1.30.3
# Tue, 21 May 2024 14:13:49 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 21 May 2024 14:13:49 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 21 May 2024 14:13:49 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 21 May 2024 14:13:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 May 2024 14:13:49 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:91e301773f03e9e0fabc5c177fe6bfe8daf14e992ab816f151692b814ddc462c`  
		Last Modified: Tue, 14 May 2024 00:42:35 GMT  
		Size: 49.6 MB (49613388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15856ca26414127b85cee6d10acbc4cee6eba9070f3f5a04b9cc72ce95abfa7f`  
		Last Modified: Tue, 14 May 2024 01:52:50 GMT  
		Size: 23.6 MB (23586610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787c90cc4c220f2efc01fd1f87a403a247f61d1030f562e906930332d905ebdb`  
		Last Modified: Wed, 15 May 2024 15:06:57 GMT  
		Size: 18.9 MB (18870680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a23862d11452a5b51a68997e785996fd1e75da32dd2d37041a0da1bf5f6d58f9`  
		Last Modified: Wed, 15 May 2024 15:06:56 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d77927e413fc545578865de64349d36cc081fb9cddad7d367cbe6603e44b48cc`  
		Last Modified: Tue, 21 May 2024 19:35:30 GMT  
		Size: 57.1 MB (57123300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cbc39928b2eb309725c009a597946c56c6a462adc4a0bdd10fea3ba4a245ff7`  
		Last Modified: Tue, 21 May 2024 19:35:27 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.30` - unknown; unknown

```console
$ docker pull telegraf@sha256:fee17afc9e9dc2f01e041248c868b8a0c5f0296b9ebd44adf0759fa569c8061f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6314985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38cbf4f25a66722c5fa564a3fbe175bffaba0e2911c66085c299f720eacaf700`

```dockerfile
```

-	Layers:
	-	`sha256:4a45036b1e98c4f63e4867f33d7068bc8635061614a4648ec2e3033520a0650d`  
		Last Modified: Tue, 21 May 2024 19:35:28 GMT  
		Size: 6.3 MB (6300400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0c4cd04de694e67f0f823819d8428380c279bf3cd7fd56c726e6a8dde2f06e3`  
		Last Modified: Tue, 21 May 2024 19:35:27 GMT  
		Size: 14.6 KB (14585 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.30-alpine`

```console
$ docker pull telegraf@sha256:cfe387fe1b2fc1c51d38ee9c9244a6bffe3289c578fccedd21474914f055e488
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.30-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:ddff3de1117226b06a1cd26bbe81621aef008e22cc6cfa02305c36d790c21dca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.6 MB (68644120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72c5716fd9fffd0da2fb62d7d5bb99d436be11a4dcaa1631b988800622bdd352`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
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
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a31d3de31608c4eb37a8e9376bbeb0eb2468211670138269f2a723eea57f0db`  
		Last Modified: Mon, 10 Jun 2024 22:32:53 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d76b59fd6c6c8d456f928a8490e18e2c0dd6521166b794772ca68442b864fcad`  
		Last Modified: Mon, 10 Jun 2024 22:32:53 GMT  
		Size: 2.5 MB (2452611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5086455aeadda3a942427d1e24b500d7703e1561c447c6be407082030f7d9832`  
		Last Modified: Mon, 10 Jun 2024 22:32:55 GMT  
		Size: 62.6 MB (62568807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb291c63e2c6cb0638ea6bfa58dba44ab7783743243a03e38c03e81fd2a8fe0e`  
		Last Modified: Mon, 10 Jun 2024 22:32:53 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.30-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:43a2818e12f8c8c14f303d6871e06fe613f850498236d4d294508b95af426ef6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1001473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2f48236161ebc4d8e37b04b3466100564fe7fa8554e59b8a18bd502afb9b199`

```dockerfile
```

-	Layers:
	-	`sha256:6823e4e4b0b798e98ad738719136bd697412940fc31ae51950fc50e73733c4ea`  
		Last Modified: Mon, 10 Jun 2024 22:32:53 GMT  
		Size: 986.7 KB (986740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2c4607aa8c8545073f65c5b0a223265606e798a8cca5e58080b2271c184c288`  
		Last Modified: Mon, 10 Jun 2024 22:32:53 GMT  
		Size: 14.7 KB (14733 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.30-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:33c1a2cb6de73e279f2888dbfb9c2ab4d591ba512ed3b0c632943a3f293278d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.0 MB (62998531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f947f38465eaafcd3d85c85c55fdd97d65ff67cb124b935eabf51d4c80936d29`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Tue, 21 May 2024 14:13:49 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 21 May 2024 14:13:49 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Tue, 21 May 2024 14:13:49 GMT
ENV TELEGRAF_VERSION=1.30.3
# Tue, 21 May 2024 14:13:49 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Tue, 21 May 2024 14:13:49 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 21 May 2024 14:13:49 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 21 May 2024 14:13:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 May 2024 14:13:49 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50b0ae9590aac951e94f2baae1a59646b1132c3e10a981231c743a821f41d9ab`  
		Last Modified: Tue, 21 May 2024 20:01:35 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6dd9c7b1008b5ca36e326e19552f59e8b410f609610a513c42712f471376e67`  
		Last Modified: Tue, 21 May 2024 20:01:36 GMT  
		Size: 2.7 MB (2702921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8ab3c82d9de8f26a41d48d18ba5c0e58b1c3c15ff6908f34e89a2fd53193718`  
		Last Modified: Tue, 21 May 2024 20:01:38 GMT  
		Size: 56.9 MB (56947288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83051d2d208b78832edbd8f3b86ccb69839f624c116289700a5b26a4da435127`  
		Last Modified: Tue, 21 May 2024 20:01:35 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.30-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:4ae630baa163ce0b8744d1bb6856fbed9b79c20ce53811cbd4b2c50bbb2b1bf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 MB (1376339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d48b6b7fc3662b331b9a7dc7cc18b73fcd03fd2689df5a672b9a0421e974fb26`

```dockerfile
```

-	Layers:
	-	`sha256:fb8c35c943dd6d3722715d167caa72fb6bdb338ad405085b693be64bd3c46a40`  
		Last Modified: Tue, 21 May 2024 20:01:36 GMT  
		Size: 1.4 MB (1361344 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d79f11691deb44318e4551d0b381fbad6d42458e7f5f4ede4cb6c115cadfb81`  
		Last Modified: Tue, 21 May 2024 20:01:35 GMT  
		Size: 15.0 KB (14995 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.30.3`

```console
$ docker pull telegraf@sha256:f2e67caa9551063cceb419c6c237f381fc3065e3bebcd4518771de8905c84aab
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
$ docker pull telegraf@sha256:1536a0e21425afcbf83415a27903eba63c4ff33c232ff12e5ab878e048932458
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.3 MB (155343262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3eb3db616f9429922c1ad42967f050369335cba406e8363e6481680fab647ed`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 14 May 2024 01:27:51 GMT
ADD file:b9a9fc37b874060c713002ae1ac220f097edd7c6576116c22bb15aad8229b1b3 in / 
# Tue, 14 May 2024 01:27:51 GMT
CMD ["bash"]
# Tue, 14 May 2024 02:54:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 10 Jun 2024 21:05:04 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
ENV TELEGRAF_VERSION=1.30.3
# Mon, 10 Jun 2024 21:05:04 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
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
	-	`sha256:c6cf28de8a067787ee0d08f8b01d7f1566a508b56f6e549687b41dfd375f12c7`  
		Last Modified: Tue, 14 May 2024 01:32:07 GMT  
		Size: 49.6 MB (49576390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:891494355808bdd3db5552f0d3723fd0fa826675f774853796fafa221d850d42`  
		Last Modified: Tue, 14 May 2024 03:04:06 GMT  
		Size: 24.1 MB (24050100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e969ad6682604967a9717b77c98a6d0e86dbb701f9fa7ea34e83813870cbd3b`  
		Last Modified: Mon, 10 Jun 2024 22:33:05 GMT  
		Size: 18.9 MB (18947891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a63d41fe6b8ce94b5889480fa7a950106fc4c72448bea0eaca69e23a35310d2d`  
		Last Modified: Mon, 10 Jun 2024 22:33:04 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0732158ba65379866405f93434e703e89dbe155c9376d577a0f02d76acd99fee`  
		Last Modified: Mon, 10 Jun 2024 22:33:07 GMT  
		Size: 62.8 MB (62766475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3297c3e84d61216630b2b3e04e62d6343a796335063a9e9c864497c1f8112d9`  
		Last Modified: Mon, 10 Jun 2024 22:33:04 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.30.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:bdc24167f9300b693687cbd3ff3326ab7e9fef015427a84d55c63ab50c4b0983
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6313807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46ac369e730184e4c5733be0af0391f32adfccfd72fd8277d13bb96d4bb683e3`

```dockerfile
```

-	Layers:
	-	`sha256:9272ea8c421cbf05fc7094eb44749f70d6cadbf05a83410429dd99ec0bb16f11`  
		Last Modified: Mon, 10 Jun 2024 22:33:05 GMT  
		Size: 6.3 MB (6299484 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de9fff0ee2e3d6fe2fff05993a092dd3b095bcc6cf39e44392a835c3204448da`  
		Last Modified: Mon, 10 Jun 2024 22:33:04 GMT  
		Size: 14.3 KB (14323 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.30.3` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:0937b1a222978be919cb00df24cdcfa62d8a100dccab0ab3776ccfba19e31a02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.1 MB (143068661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a2f8ba5cd8962f90e947f7fe1309436728ed13ef21c5fb8bf4dab976ef3b3cb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 14 May 2024 01:08:35 GMT
ADD file:1e106a38a0e44ca74d4d29c6d797780e7a29ffe249e473c48ee2aea553fc013b in / 
# Tue, 14 May 2024 01:08:36 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:35:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 May 2024 14:13:49 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 May 2024 14:13:49 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 21 May 2024 14:13:49 GMT
ENV TELEGRAF_VERSION=1.30.3
# Tue, 21 May 2024 14:13:49 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 21 May 2024 14:13:49 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 21 May 2024 14:13:49 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 21 May 2024 14:13:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 May 2024 14:13:49 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:dfc3b4ca62816a9cbf2bdfbdd78bf692a522e7f48a280492b9f87d55b2f4aa2e`  
		Last Modified: Tue, 14 May 2024 01:12:21 GMT  
		Size: 45.2 MB (45174745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:641d6443415d538c3bf0e0d6ecc0f6b7603b4caf6c79708d0670bc082e9721c5`  
		Last Modified: Tue, 14 May 2024 01:46:47 GMT  
		Size: 22.0 MB (21953893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:901b8b18d82e5b57b89385ec062d1674265344d73cca05bba989b96a6cf4f07a`  
		Last Modified: Wed, 15 May 2024 08:08:19 GMT  
		Size: 17.7 MB (17724872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6537ab1b98b6a7364bac3f994ad624855097573d29bfa741f0a5f24eaffe2bc`  
		Last Modified: Wed, 15 May 2024 08:08:18 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f4a236ed04d98e4dbbd6c88b87392bd54e369cfbb75ba5afcace4dbb33b6ef`  
		Last Modified: Tue, 21 May 2024 18:08:27 GMT  
		Size: 58.2 MB (58212744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd8eaaf18c8e5e6fb3073500e84a83e0722dc3b3231c64d24a578c283338d60c`  
		Last Modified: Tue, 21 May 2024 18:08:25 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.30.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:ea09a00736aecf132e6b185eabe3f050148ea41c066980dd8d9cc03768abd799
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6309812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:419e20c776b8b40e3ad5056c424586ebfdd0254d17d6d87c07cc05f3bf274422`

```dockerfile
```

-	Layers:
	-	`sha256:be92ac005ea43268c72221d35410b3ffe5cda8c51a0f7fb2d095fc2a8259e1c6`  
		Last Modified: Tue, 21 May 2024 18:08:25 GMT  
		Size: 6.3 MB (6295147 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b6d8ab8fcfcde216a402b8bedfe934dd5adae59f9659864fff791d9ef974c86`  
		Last Modified: Tue, 21 May 2024 18:08:25 GMT  
		Size: 14.7 KB (14665 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.30.3` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:d062d9a32a4d87ea479fa7887bcb7813c9139badfdda83620cbaf1317f0d885b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.2 MB (149196386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e9e574432b44679b03199dc4767cc26b2d1f2c504cf5053af7a32a97cf038c6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 14 May 2024 00:39:32 GMT
ADD file:b7c55dda8ded4219a7cdc9fbd91dfb5996c4886d4394b85751c2f956defe3287 in / 
# Tue, 14 May 2024 00:39:33 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:44:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 May 2024 14:13:49 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 May 2024 14:13:49 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 21 May 2024 14:13:49 GMT
ENV TELEGRAF_VERSION=1.30.3
# Tue, 21 May 2024 14:13:49 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 21 May 2024 14:13:49 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 21 May 2024 14:13:49 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 21 May 2024 14:13:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 May 2024 14:13:49 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:91e301773f03e9e0fabc5c177fe6bfe8daf14e992ab816f151692b814ddc462c`  
		Last Modified: Tue, 14 May 2024 00:42:35 GMT  
		Size: 49.6 MB (49613388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15856ca26414127b85cee6d10acbc4cee6eba9070f3f5a04b9cc72ce95abfa7f`  
		Last Modified: Tue, 14 May 2024 01:52:50 GMT  
		Size: 23.6 MB (23586610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787c90cc4c220f2efc01fd1f87a403a247f61d1030f562e906930332d905ebdb`  
		Last Modified: Wed, 15 May 2024 15:06:57 GMT  
		Size: 18.9 MB (18870680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a23862d11452a5b51a68997e785996fd1e75da32dd2d37041a0da1bf5f6d58f9`  
		Last Modified: Wed, 15 May 2024 15:06:56 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d77927e413fc545578865de64349d36cc081fb9cddad7d367cbe6603e44b48cc`  
		Last Modified: Tue, 21 May 2024 19:35:30 GMT  
		Size: 57.1 MB (57123300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cbc39928b2eb309725c009a597946c56c6a462adc4a0bdd10fea3ba4a245ff7`  
		Last Modified: Tue, 21 May 2024 19:35:27 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.30.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:fee17afc9e9dc2f01e041248c868b8a0c5f0296b9ebd44adf0759fa569c8061f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6314985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38cbf4f25a66722c5fa564a3fbe175bffaba0e2911c66085c299f720eacaf700`

```dockerfile
```

-	Layers:
	-	`sha256:4a45036b1e98c4f63e4867f33d7068bc8635061614a4648ec2e3033520a0650d`  
		Last Modified: Tue, 21 May 2024 19:35:28 GMT  
		Size: 6.3 MB (6300400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0c4cd04de694e67f0f823819d8428380c279bf3cd7fd56c726e6a8dde2f06e3`  
		Last Modified: Tue, 21 May 2024 19:35:27 GMT  
		Size: 14.6 KB (14585 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.30.3-alpine`

```console
$ docker pull telegraf@sha256:cfe387fe1b2fc1c51d38ee9c9244a6bffe3289c578fccedd21474914f055e488
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.30.3-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:ddff3de1117226b06a1cd26bbe81621aef008e22cc6cfa02305c36d790c21dca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.6 MB (68644120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72c5716fd9fffd0da2fb62d7d5bb99d436be11a4dcaa1631b988800622bdd352`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
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
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a31d3de31608c4eb37a8e9376bbeb0eb2468211670138269f2a723eea57f0db`  
		Last Modified: Mon, 10 Jun 2024 22:32:53 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d76b59fd6c6c8d456f928a8490e18e2c0dd6521166b794772ca68442b864fcad`  
		Last Modified: Mon, 10 Jun 2024 22:32:53 GMT  
		Size: 2.5 MB (2452611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5086455aeadda3a942427d1e24b500d7703e1561c447c6be407082030f7d9832`  
		Last Modified: Mon, 10 Jun 2024 22:32:55 GMT  
		Size: 62.6 MB (62568807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb291c63e2c6cb0638ea6bfa58dba44ab7783743243a03e38c03e81fd2a8fe0e`  
		Last Modified: Mon, 10 Jun 2024 22:32:53 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.30.3-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:43a2818e12f8c8c14f303d6871e06fe613f850498236d4d294508b95af426ef6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1001473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2f48236161ebc4d8e37b04b3466100564fe7fa8554e59b8a18bd502afb9b199`

```dockerfile
```

-	Layers:
	-	`sha256:6823e4e4b0b798e98ad738719136bd697412940fc31ae51950fc50e73733c4ea`  
		Last Modified: Mon, 10 Jun 2024 22:32:53 GMT  
		Size: 986.7 KB (986740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2c4607aa8c8545073f65c5b0a223265606e798a8cca5e58080b2271c184c288`  
		Last Modified: Mon, 10 Jun 2024 22:32:53 GMT  
		Size: 14.7 KB (14733 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.30.3-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:33c1a2cb6de73e279f2888dbfb9c2ab4d591ba512ed3b0c632943a3f293278d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.0 MB (62998531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f947f38465eaafcd3d85c85c55fdd97d65ff67cb124b935eabf51d4c80936d29`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Tue, 21 May 2024 14:13:49 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 21 May 2024 14:13:49 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Tue, 21 May 2024 14:13:49 GMT
ENV TELEGRAF_VERSION=1.30.3
# Tue, 21 May 2024 14:13:49 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Tue, 21 May 2024 14:13:49 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 21 May 2024 14:13:49 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 21 May 2024 14:13:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 May 2024 14:13:49 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50b0ae9590aac951e94f2baae1a59646b1132c3e10a981231c743a821f41d9ab`  
		Last Modified: Tue, 21 May 2024 20:01:35 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6dd9c7b1008b5ca36e326e19552f59e8b410f609610a513c42712f471376e67`  
		Last Modified: Tue, 21 May 2024 20:01:36 GMT  
		Size: 2.7 MB (2702921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8ab3c82d9de8f26a41d48d18ba5c0e58b1c3c15ff6908f34e89a2fd53193718`  
		Last Modified: Tue, 21 May 2024 20:01:38 GMT  
		Size: 56.9 MB (56947288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83051d2d208b78832edbd8f3b86ccb69839f624c116289700a5b26a4da435127`  
		Last Modified: Tue, 21 May 2024 20:01:35 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.30.3-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:4ae630baa163ce0b8744d1bb6856fbed9b79c20ce53811cbd4b2c50bbb2b1bf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 MB (1376339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d48b6b7fc3662b331b9a7dc7cc18b73fcd03fd2689df5a672b9a0421e974fb26`

```dockerfile
```

-	Layers:
	-	`sha256:fb8c35c943dd6d3722715d167caa72fb6bdb338ad405085b693be64bd3c46a40`  
		Last Modified: Tue, 21 May 2024 20:01:36 GMT  
		Size: 1.4 MB (1361344 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d79f11691deb44318e4551d0b381fbad6d42458e7f5f4ede4cb6c115cadfb81`  
		Last Modified: Tue, 21 May 2024 20:01:35 GMT  
		Size: 15.0 KB (14995 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.31`

```console
$ docker pull telegraf@sha256:fadef7e843aa67104f271594b1ce433c278e88fdf05776ab542bf2fd8b256f4d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `telegraf:1.31` - linux; amd64

```console
$ docker pull telegraf@sha256:44dc8b1f371f400ed282951f09c77e717d4629b38d295bcf37adafb95cceb243
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.7 MB (157666082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfb33388867057e3193fe2d3768501720a7ad9f2acc4b43078eb2cc22e5147a0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 14 May 2024 01:27:51 GMT
ADD file:b9a9fc37b874060c713002ae1ac220f097edd7c6576116c22bb15aad8229b1b3 in / 
# Tue, 14 May 2024 01:27:51 GMT
CMD ["bash"]
# Tue, 14 May 2024 02:54:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 10 Jun 2024 21:05:04 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
ENV TELEGRAF_VERSION=1.31.0
# Mon, 10 Jun 2024 21:05:04 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
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
	-	`sha256:c6cf28de8a067787ee0d08f8b01d7f1566a508b56f6e549687b41dfd375f12c7`  
		Last Modified: Tue, 14 May 2024 01:32:07 GMT  
		Size: 49.6 MB (49576390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:891494355808bdd3db5552f0d3723fd0fa826675f774853796fafa221d850d42`  
		Last Modified: Tue, 14 May 2024 03:04:06 GMT  
		Size: 24.1 MB (24050100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba02c6ae7fe3311dc53f8cc7ef5044386dc1b913664583f7a6f270ba83be5853`  
		Last Modified: Mon, 10 Jun 2024 22:33:00 GMT  
		Size: 18.9 MB (18947865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bdc44775bd6481d3e78c7e2e12361e98e4227c8e9e463f1d93f83589d1b9095`  
		Last Modified: Mon, 10 Jun 2024 22:33:00 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3672b395fed0d417ceeff47f3839a16e0b978aeb7d1bc0f228f9cccd67cdd5c`  
		Last Modified: Mon, 10 Jun 2024 22:33:02 GMT  
		Size: 65.1 MB (65089317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edd204feb12d817fec8d8730699b552d5490725be1121fbb508ff0e5ebeb61ef`  
		Last Modified: Mon, 10 Jun 2024 22:33:00 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31` - unknown; unknown

```console
$ docker pull telegraf@sha256:f0b28b3a379a88b32fa46e49985d81b74033cd04affcb5b89e8cd23f311508f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6318438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4454cd70cb0be5c2706a0d29111ad45bc776dc5e19963365e0bcb97f89b80f1`

```dockerfile
```

-	Layers:
	-	`sha256:237de469e10f3b5b75580715df66063159386618e49010e34d7ca85b0071963d`  
		Last Modified: Mon, 10 Jun 2024 22:33:00 GMT  
		Size: 6.3 MB (6303812 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3d28a42ccc99d982a61ba3d837e377bc45c9762559146c164c950eb904af1ce`  
		Last Modified: Mon, 10 Jun 2024 22:32:59 GMT  
		Size: 14.6 KB (14626 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.31-alpine`

```console
$ docker pull telegraf@sha256:7e2d43be6b9923a02d5f58d7394fc928459480fac30244bb515c360e48d09ed1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `telegraf:1.31-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:cea79a5632fbe1b775eb0b5e3981cf7db25bc9facdf9ab2ec664609f8ac493ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (70967139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:179e85bca4a5ed06987cd9cc98a88e84ea7f6c9f7595074fcb0b9c65bd5860cd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
CMD ["/bin/sh"]
# Mon, 10 Jun 2024 21:05:04 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
ENV TELEGRAF_VERSION=1.31.0
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
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddc543c237aca646b092c4fdea01ab9b8bde787628b47abc72dbae1d179996a6`  
		Last Modified: Mon, 10 Jun 2024 22:32:57 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a98f63f2c15a2d76083a496a488478760a73dcf9e27005d98c677346ccb2254a`  
		Last Modified: Mon, 10 Jun 2024 22:32:57 GMT  
		Size: 2.5 MB (2452615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e226ade9494bd1902c71aa690099ca31d39ac3cdd3d988805ff9b17827e25114`  
		Last Modified: Mon, 10 Jun 2024 22:32:59 GMT  
		Size: 64.9 MB (64891822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddaea357ec378621b71776a323682e0f82ec65a54bef1706bf8994bf04dd2b35`  
		Last Modified: Mon, 10 Jun 2024 22:32:57 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:031ef6a4e0c263cc2ab30eb3d97c55cb6e5aacf456ad1a72425c73cd4303f146
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1006104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed53af325068dcf824b312cd823469fbe369e7023dff8289a05a60203b78c2d3`

```dockerfile
```

-	Layers:
	-	`sha256:2819af046f27e0e9300377570774c7c28ea5915bb7f0d6bceb87469ff75a91a6`  
		Last Modified: Mon, 10 Jun 2024 22:32:57 GMT  
		Size: 991.1 KB (991068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:940319c9ee8fdd4367be09932abf7350462a2daccbc076dff9f6f95f3479a6e1`  
		Last Modified: Mon, 10 Jun 2024 22:32:57 GMT  
		Size: 15.0 KB (15036 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.31.0`

```console
$ docker pull telegraf@sha256:fadef7e843aa67104f271594b1ce433c278e88fdf05776ab542bf2fd8b256f4d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `telegraf:1.31.0` - linux; amd64

```console
$ docker pull telegraf@sha256:44dc8b1f371f400ed282951f09c77e717d4629b38d295bcf37adafb95cceb243
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.7 MB (157666082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfb33388867057e3193fe2d3768501720a7ad9f2acc4b43078eb2cc22e5147a0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 14 May 2024 01:27:51 GMT
ADD file:b9a9fc37b874060c713002ae1ac220f097edd7c6576116c22bb15aad8229b1b3 in / 
# Tue, 14 May 2024 01:27:51 GMT
CMD ["bash"]
# Tue, 14 May 2024 02:54:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 10 Jun 2024 21:05:04 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
ENV TELEGRAF_VERSION=1.31.0
# Mon, 10 Jun 2024 21:05:04 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
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
	-	`sha256:c6cf28de8a067787ee0d08f8b01d7f1566a508b56f6e549687b41dfd375f12c7`  
		Last Modified: Tue, 14 May 2024 01:32:07 GMT  
		Size: 49.6 MB (49576390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:891494355808bdd3db5552f0d3723fd0fa826675f774853796fafa221d850d42`  
		Last Modified: Tue, 14 May 2024 03:04:06 GMT  
		Size: 24.1 MB (24050100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba02c6ae7fe3311dc53f8cc7ef5044386dc1b913664583f7a6f270ba83be5853`  
		Last Modified: Mon, 10 Jun 2024 22:33:00 GMT  
		Size: 18.9 MB (18947865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bdc44775bd6481d3e78c7e2e12361e98e4227c8e9e463f1d93f83589d1b9095`  
		Last Modified: Mon, 10 Jun 2024 22:33:00 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3672b395fed0d417ceeff47f3839a16e0b978aeb7d1bc0f228f9cccd67cdd5c`  
		Last Modified: Mon, 10 Jun 2024 22:33:02 GMT  
		Size: 65.1 MB (65089317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edd204feb12d817fec8d8730699b552d5490725be1121fbb508ff0e5ebeb61ef`  
		Last Modified: Mon, 10 Jun 2024 22:33:00 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31.0` - unknown; unknown

```console
$ docker pull telegraf@sha256:f0b28b3a379a88b32fa46e49985d81b74033cd04affcb5b89e8cd23f311508f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6318438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4454cd70cb0be5c2706a0d29111ad45bc776dc5e19963365e0bcb97f89b80f1`

```dockerfile
```

-	Layers:
	-	`sha256:237de469e10f3b5b75580715df66063159386618e49010e34d7ca85b0071963d`  
		Last Modified: Mon, 10 Jun 2024 22:33:00 GMT  
		Size: 6.3 MB (6303812 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3d28a42ccc99d982a61ba3d837e377bc45c9762559146c164c950eb904af1ce`  
		Last Modified: Mon, 10 Jun 2024 22:32:59 GMT  
		Size: 14.6 KB (14626 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.31.0-alpine`

```console
$ docker pull telegraf@sha256:7e2d43be6b9923a02d5f58d7394fc928459480fac30244bb515c360e48d09ed1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `telegraf:1.31.0-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:cea79a5632fbe1b775eb0b5e3981cf7db25bc9facdf9ab2ec664609f8ac493ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (70967139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:179e85bca4a5ed06987cd9cc98a88e84ea7f6c9f7595074fcb0b9c65bd5860cd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
CMD ["/bin/sh"]
# Mon, 10 Jun 2024 21:05:04 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
ENV TELEGRAF_VERSION=1.31.0
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
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddc543c237aca646b092c4fdea01ab9b8bde787628b47abc72dbae1d179996a6`  
		Last Modified: Mon, 10 Jun 2024 22:32:57 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a98f63f2c15a2d76083a496a488478760a73dcf9e27005d98c677346ccb2254a`  
		Last Modified: Mon, 10 Jun 2024 22:32:57 GMT  
		Size: 2.5 MB (2452615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e226ade9494bd1902c71aa690099ca31d39ac3cdd3d988805ff9b17827e25114`  
		Last Modified: Mon, 10 Jun 2024 22:32:59 GMT  
		Size: 64.9 MB (64891822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddaea357ec378621b71776a323682e0f82ec65a54bef1706bf8994bf04dd2b35`  
		Last Modified: Mon, 10 Jun 2024 22:32:57 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31.0-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:031ef6a4e0c263cc2ab30eb3d97c55cb6e5aacf456ad1a72425c73cd4303f146
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1006104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed53af325068dcf824b312cd823469fbe369e7023dff8289a05a60203b78c2d3`

```dockerfile
```

-	Layers:
	-	`sha256:2819af046f27e0e9300377570774c7c28ea5915bb7f0d6bceb87469ff75a91a6`  
		Last Modified: Mon, 10 Jun 2024 22:32:57 GMT  
		Size: 991.1 KB (991068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:940319c9ee8fdd4367be09932abf7350462a2daccbc076dff9f6f95f3479a6e1`  
		Last Modified: Mon, 10 Jun 2024 22:32:57 GMT  
		Size: 15.0 KB (15036 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:alpine`

```console
$ docker pull telegraf@sha256:bf0c681f61c39bab65c7f279752811d8be56e0a9383ceb93d14d5d71f4dab446
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:cea79a5632fbe1b775eb0b5e3981cf7db25bc9facdf9ab2ec664609f8ac493ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (70967139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:179e85bca4a5ed06987cd9cc98a88e84ea7f6c9f7595074fcb0b9c65bd5860cd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
CMD ["/bin/sh"]
# Mon, 10 Jun 2024 21:05:04 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
ENV TELEGRAF_VERSION=1.31.0
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
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddc543c237aca646b092c4fdea01ab9b8bde787628b47abc72dbae1d179996a6`  
		Last Modified: Mon, 10 Jun 2024 22:32:57 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a98f63f2c15a2d76083a496a488478760a73dcf9e27005d98c677346ccb2254a`  
		Last Modified: Mon, 10 Jun 2024 22:32:57 GMT  
		Size: 2.5 MB (2452615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e226ade9494bd1902c71aa690099ca31d39ac3cdd3d988805ff9b17827e25114`  
		Last Modified: Mon, 10 Jun 2024 22:32:59 GMT  
		Size: 64.9 MB (64891822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddaea357ec378621b71776a323682e0f82ec65a54bef1706bf8994bf04dd2b35`  
		Last Modified: Mon, 10 Jun 2024 22:32:57 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:031ef6a4e0c263cc2ab30eb3d97c55cb6e5aacf456ad1a72425c73cd4303f146
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1006104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed53af325068dcf824b312cd823469fbe369e7023dff8289a05a60203b78c2d3`

```dockerfile
```

-	Layers:
	-	`sha256:2819af046f27e0e9300377570774c7c28ea5915bb7f0d6bceb87469ff75a91a6`  
		Last Modified: Mon, 10 Jun 2024 22:32:57 GMT  
		Size: 991.1 KB (991068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:940319c9ee8fdd4367be09932abf7350462a2daccbc076dff9f6f95f3479a6e1`  
		Last Modified: Mon, 10 Jun 2024 22:32:57 GMT  
		Size: 15.0 KB (15036 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:33c1a2cb6de73e279f2888dbfb9c2ab4d591ba512ed3b0c632943a3f293278d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.0 MB (62998531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f947f38465eaafcd3d85c85c55fdd97d65ff67cb124b935eabf51d4c80936d29`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Tue, 21 May 2024 14:13:49 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 21 May 2024 14:13:49 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Tue, 21 May 2024 14:13:49 GMT
ENV TELEGRAF_VERSION=1.30.3
# Tue, 21 May 2024 14:13:49 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Tue, 21 May 2024 14:13:49 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 21 May 2024 14:13:49 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 21 May 2024 14:13:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 May 2024 14:13:49 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50b0ae9590aac951e94f2baae1a59646b1132c3e10a981231c743a821f41d9ab`  
		Last Modified: Tue, 21 May 2024 20:01:35 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6dd9c7b1008b5ca36e326e19552f59e8b410f609610a513c42712f471376e67`  
		Last Modified: Tue, 21 May 2024 20:01:36 GMT  
		Size: 2.7 MB (2702921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8ab3c82d9de8f26a41d48d18ba5c0e58b1c3c15ff6908f34e89a2fd53193718`  
		Last Modified: Tue, 21 May 2024 20:01:38 GMT  
		Size: 56.9 MB (56947288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83051d2d208b78832edbd8f3b86ccb69839f624c116289700a5b26a4da435127`  
		Last Modified: Tue, 21 May 2024 20:01:35 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:4ae630baa163ce0b8744d1bb6856fbed9b79c20ce53811cbd4b2c50bbb2b1bf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 MB (1376339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d48b6b7fc3662b331b9a7dc7cc18b73fcd03fd2689df5a672b9a0421e974fb26`

```dockerfile
```

-	Layers:
	-	`sha256:fb8c35c943dd6d3722715d167caa72fb6bdb338ad405085b693be64bd3c46a40`  
		Last Modified: Tue, 21 May 2024 20:01:36 GMT  
		Size: 1.4 MB (1361344 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d79f11691deb44318e4551d0b381fbad6d42458e7f5f4ede4cb6c115cadfb81`  
		Last Modified: Tue, 21 May 2024 20:01:35 GMT  
		Size: 15.0 KB (14995 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:latest`

```console
$ docker pull telegraf@sha256:be0e7c04e4876560322eec497d44fbec1003a793d9f6abfd389b673fce92b8e4
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
$ docker pull telegraf@sha256:44dc8b1f371f400ed282951f09c77e717d4629b38d295bcf37adafb95cceb243
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.7 MB (157666082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfb33388867057e3193fe2d3768501720a7ad9f2acc4b43078eb2cc22e5147a0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 14 May 2024 01:27:51 GMT
ADD file:b9a9fc37b874060c713002ae1ac220f097edd7c6576116c22bb15aad8229b1b3 in / 
# Tue, 14 May 2024 01:27:51 GMT
CMD ["bash"]
# Tue, 14 May 2024 02:54:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 10 Jun 2024 21:05:04 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
ENV TELEGRAF_VERSION=1.31.0
# Mon, 10 Jun 2024 21:05:04 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
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
	-	`sha256:c6cf28de8a067787ee0d08f8b01d7f1566a508b56f6e549687b41dfd375f12c7`  
		Last Modified: Tue, 14 May 2024 01:32:07 GMT  
		Size: 49.6 MB (49576390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:891494355808bdd3db5552f0d3723fd0fa826675f774853796fafa221d850d42`  
		Last Modified: Tue, 14 May 2024 03:04:06 GMT  
		Size: 24.1 MB (24050100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba02c6ae7fe3311dc53f8cc7ef5044386dc1b913664583f7a6f270ba83be5853`  
		Last Modified: Mon, 10 Jun 2024 22:33:00 GMT  
		Size: 18.9 MB (18947865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bdc44775bd6481d3e78c7e2e12361e98e4227c8e9e463f1d93f83589d1b9095`  
		Last Modified: Mon, 10 Jun 2024 22:33:00 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3672b395fed0d417ceeff47f3839a16e0b978aeb7d1bc0f228f9cccd67cdd5c`  
		Last Modified: Mon, 10 Jun 2024 22:33:02 GMT  
		Size: 65.1 MB (65089317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edd204feb12d817fec8d8730699b552d5490725be1121fbb508ff0e5ebeb61ef`  
		Last Modified: Mon, 10 Jun 2024 22:33:00 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:f0b28b3a379a88b32fa46e49985d81b74033cd04affcb5b89e8cd23f311508f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6318438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4454cd70cb0be5c2706a0d29111ad45bc776dc5e19963365e0bcb97f89b80f1`

```dockerfile
```

-	Layers:
	-	`sha256:237de469e10f3b5b75580715df66063159386618e49010e34d7ca85b0071963d`  
		Last Modified: Mon, 10 Jun 2024 22:33:00 GMT  
		Size: 6.3 MB (6303812 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3d28a42ccc99d982a61ba3d837e377bc45c9762559146c164c950eb904af1ce`  
		Last Modified: Mon, 10 Jun 2024 22:32:59 GMT  
		Size: 14.6 KB (14626 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:0937b1a222978be919cb00df24cdcfa62d8a100dccab0ab3776ccfba19e31a02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.1 MB (143068661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a2f8ba5cd8962f90e947f7fe1309436728ed13ef21c5fb8bf4dab976ef3b3cb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 14 May 2024 01:08:35 GMT
ADD file:1e106a38a0e44ca74d4d29c6d797780e7a29ffe249e473c48ee2aea553fc013b in / 
# Tue, 14 May 2024 01:08:36 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:35:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 May 2024 14:13:49 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 May 2024 14:13:49 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 21 May 2024 14:13:49 GMT
ENV TELEGRAF_VERSION=1.30.3
# Tue, 21 May 2024 14:13:49 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 21 May 2024 14:13:49 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 21 May 2024 14:13:49 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 21 May 2024 14:13:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 May 2024 14:13:49 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:dfc3b4ca62816a9cbf2bdfbdd78bf692a522e7f48a280492b9f87d55b2f4aa2e`  
		Last Modified: Tue, 14 May 2024 01:12:21 GMT  
		Size: 45.2 MB (45174745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:641d6443415d538c3bf0e0d6ecc0f6b7603b4caf6c79708d0670bc082e9721c5`  
		Last Modified: Tue, 14 May 2024 01:46:47 GMT  
		Size: 22.0 MB (21953893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:901b8b18d82e5b57b89385ec062d1674265344d73cca05bba989b96a6cf4f07a`  
		Last Modified: Wed, 15 May 2024 08:08:19 GMT  
		Size: 17.7 MB (17724872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6537ab1b98b6a7364bac3f994ad624855097573d29bfa741f0a5f24eaffe2bc`  
		Last Modified: Wed, 15 May 2024 08:08:18 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f4a236ed04d98e4dbbd6c88b87392bd54e369cfbb75ba5afcace4dbb33b6ef`  
		Last Modified: Tue, 21 May 2024 18:08:27 GMT  
		Size: 58.2 MB (58212744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd8eaaf18c8e5e6fb3073500e84a83e0722dc3b3231c64d24a578c283338d60c`  
		Last Modified: Tue, 21 May 2024 18:08:25 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:ea09a00736aecf132e6b185eabe3f050148ea41c066980dd8d9cc03768abd799
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6309812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:419e20c776b8b40e3ad5056c424586ebfdd0254d17d6d87c07cc05f3bf274422`

```dockerfile
```

-	Layers:
	-	`sha256:be92ac005ea43268c72221d35410b3ffe5cda8c51a0f7fb2d095fc2a8259e1c6`  
		Last Modified: Tue, 21 May 2024 18:08:25 GMT  
		Size: 6.3 MB (6295147 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b6d8ab8fcfcde216a402b8bedfe934dd5adae59f9659864fff791d9ef974c86`  
		Last Modified: Tue, 21 May 2024 18:08:25 GMT  
		Size: 14.7 KB (14665 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:d062d9a32a4d87ea479fa7887bcb7813c9139badfdda83620cbaf1317f0d885b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.2 MB (149196386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e9e574432b44679b03199dc4767cc26b2d1f2c504cf5053af7a32a97cf038c6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 14 May 2024 00:39:32 GMT
ADD file:b7c55dda8ded4219a7cdc9fbd91dfb5996c4886d4394b85751c2f956defe3287 in / 
# Tue, 14 May 2024 00:39:33 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:44:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 May 2024 14:13:49 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 May 2024 14:13:49 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 21 May 2024 14:13:49 GMT
ENV TELEGRAF_VERSION=1.30.3
# Tue, 21 May 2024 14:13:49 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 21 May 2024 14:13:49 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 21 May 2024 14:13:49 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 21 May 2024 14:13:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 May 2024 14:13:49 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:91e301773f03e9e0fabc5c177fe6bfe8daf14e992ab816f151692b814ddc462c`  
		Last Modified: Tue, 14 May 2024 00:42:35 GMT  
		Size: 49.6 MB (49613388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15856ca26414127b85cee6d10acbc4cee6eba9070f3f5a04b9cc72ce95abfa7f`  
		Last Modified: Tue, 14 May 2024 01:52:50 GMT  
		Size: 23.6 MB (23586610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787c90cc4c220f2efc01fd1f87a403a247f61d1030f562e906930332d905ebdb`  
		Last Modified: Wed, 15 May 2024 15:06:57 GMT  
		Size: 18.9 MB (18870680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a23862d11452a5b51a68997e785996fd1e75da32dd2d37041a0da1bf5f6d58f9`  
		Last Modified: Wed, 15 May 2024 15:06:56 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d77927e413fc545578865de64349d36cc081fb9cddad7d367cbe6603e44b48cc`  
		Last Modified: Tue, 21 May 2024 19:35:30 GMT  
		Size: 57.1 MB (57123300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cbc39928b2eb309725c009a597946c56c6a462adc4a0bdd10fea3ba4a245ff7`  
		Last Modified: Tue, 21 May 2024 19:35:27 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:fee17afc9e9dc2f01e041248c868b8a0c5f0296b9ebd44adf0759fa569c8061f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6314985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38cbf4f25a66722c5fa564a3fbe175bffaba0e2911c66085c299f720eacaf700`

```dockerfile
```

-	Layers:
	-	`sha256:4a45036b1e98c4f63e4867f33d7068bc8635061614a4648ec2e3033520a0650d`  
		Last Modified: Tue, 21 May 2024 19:35:28 GMT  
		Size: 6.3 MB (6300400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0c4cd04de694e67f0f823819d8428380c279bf3cd7fd56c726e6a8dde2f06e3`  
		Last Modified: Tue, 21 May 2024 19:35:27 GMT  
		Size: 14.6 KB (14585 bytes)  
		MIME: application/vnd.in-toto+json
