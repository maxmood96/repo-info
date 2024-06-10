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
$ docker pull telegraf@sha256:56eeb18a04795f8623419b4add3f123557477d3577106f31cff614222cd5d607
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
$ docker pull telegraf@sha256:03ff03f20ffeb13bd15052fea8393357d316c12f0d3d8dfd5cfd767817811fe4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.2 MB (155219398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34950cc48e4249d1efe53ad593d81506f149cfbc2db1f831a9b127a172c83f94`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 22 Apr 2024 19:40:36 GMT
ADD file:b9a9fc37b874060c713002ae1ac220f097edd7c6576116c22bb15aad8229b1b3 in / 
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
	-	`sha256:c6cf28de8a067787ee0d08f8b01d7f1566a508b56f6e549687b41dfd375f12c7`  
		Last Modified: Tue, 14 May 2024 01:32:07 GMT  
		Size: 49.6 MB (49576390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:891494355808bdd3db5552f0d3723fd0fa826675f774853796fafa221d850d42`  
		Last Modified: Tue, 14 May 2024 03:04:06 GMT  
		Size: 24.1 MB (24050100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbb18af3a724e3cf224127a83533de2686c1a4f5f9842e943bd7a288c2e11631`  
		Last Modified: Tue, 14 May 2024 03:58:10 GMT  
		Size: 18.9 MB (18947990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:307ca8195c9db3477da4e9d4424c85f1f0f590a7b800e61035c7539f809135e7`  
		Last Modified: Tue, 14 May 2024 03:58:10 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a3d4602b080c2f585af7f5b3788a3cadc620a559332fdbdaa4904fa65849d9a`  
		Last Modified: Tue, 14 May 2024 03:58:11 GMT  
		Size: 62.6 MB (62642512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f11091066be848f94bc4eeeabc2e81d0838e8efd324e1b578bd06b671d975f71`  
		Last Modified: Tue, 14 May 2024 03:58:10 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.29` - unknown; unknown

```console
$ docker pull telegraf@sha256:88010e4986fa4a60576e0697c79e5d6891cd9566683f5687b85b4a4e54b6ad8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6313810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:595ada0f0c20a6d0f1b443672f95ac5a275cce2c9b987ba2560e1d448e760549`

```dockerfile
```

-	Layers:
	-	`sha256:18201db310e1d93bdab1da759dfe4e5d115c99221fc41df4e8b9ae643dbec959`  
		Last Modified: Tue, 14 May 2024 03:58:10 GMT  
		Size: 6.3 MB (6299203 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:018ac014087ac4ae92459a75eca9fdbdf103dc0d7425f1eb3b8035bde38d8a28`  
		Last Modified: Tue, 14 May 2024 03:58:10 GMT  
		Size: 14.6 KB (14607 bytes)  
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
$ docker pull telegraf@sha256:0e4bd174d340f3058ff29f2197d89bd3c9eed5fb07e69da9c33046270d2c3adb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.29-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:29830a51d9174ec4932b0f32a44c2a5696271e572402a2b9308dbc0d876a3062
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.5 MB (68485548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ae49ea2b894a59d0baa970122b87381c7f5c647bd92a0d30eff9eda1bdc3c0a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
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
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66916d60fd220360ccf9f8ce7c7629a0f7b9c16e56dc879ed453c020a7ff8c8`  
		Last Modified: Wed, 01 May 2024 21:52:33 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d681b89e78ca35ddd5dac78bea950a4dc933fb18f3662365cddc94efe62c17d`  
		Last Modified: Wed, 01 May 2024 21:52:38 GMT  
		Size: 2.6 MB (2618968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35e43ef88a1d8ac6699e940f1bb502a106c9c69dd61ec39064283029b3990893`  
		Last Modified: Wed, 01 May 2024 21:52:38 GMT  
		Size: 62.5 MB (62457243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fe64437110d2f0ec023235c3c2dbfa922dd2bc68f5b44c199bac1f117dbd382`  
		Last Modified: Wed, 01 May 2024 21:52:38 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.29-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:31bd3022d8ca6189b92fdf28380fa9874d03bbd4ae130bfd243d7d94dabb0fca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 MB (1380050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db7b478da9edb82e9bba1762e22889f93d651c3b5c92bead224c6c8f9606f580`

```dockerfile
```

-	Layers:
	-	`sha256:808603a313dac867ddc4e10685e3da7916e6c936ac48e56a978a915db7b2e4a1`  
		Last Modified: Wed, 01 May 2024 21:52:38 GMT  
		Size: 1.4 MB (1365200 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1c54cd2d4e7c728b5246c616629df51baac071e16bef995e8ee8a0cc4e6b02d`  
		Last Modified: Wed, 01 May 2024 21:52:38 GMT  
		Size: 14.8 KB (14850 bytes)  
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
$ docker pull telegraf@sha256:56eeb18a04795f8623419b4add3f123557477d3577106f31cff614222cd5d607
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
$ docker pull telegraf@sha256:03ff03f20ffeb13bd15052fea8393357d316c12f0d3d8dfd5cfd767817811fe4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.2 MB (155219398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34950cc48e4249d1efe53ad593d81506f149cfbc2db1f831a9b127a172c83f94`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 22 Apr 2024 19:40:36 GMT
ADD file:b9a9fc37b874060c713002ae1ac220f097edd7c6576116c22bb15aad8229b1b3 in / 
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
	-	`sha256:c6cf28de8a067787ee0d08f8b01d7f1566a508b56f6e549687b41dfd375f12c7`  
		Last Modified: Tue, 14 May 2024 01:32:07 GMT  
		Size: 49.6 MB (49576390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:891494355808bdd3db5552f0d3723fd0fa826675f774853796fafa221d850d42`  
		Last Modified: Tue, 14 May 2024 03:04:06 GMT  
		Size: 24.1 MB (24050100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbb18af3a724e3cf224127a83533de2686c1a4f5f9842e943bd7a288c2e11631`  
		Last Modified: Tue, 14 May 2024 03:58:10 GMT  
		Size: 18.9 MB (18947990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:307ca8195c9db3477da4e9d4424c85f1f0f590a7b800e61035c7539f809135e7`  
		Last Modified: Tue, 14 May 2024 03:58:10 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a3d4602b080c2f585af7f5b3788a3cadc620a559332fdbdaa4904fa65849d9a`  
		Last Modified: Tue, 14 May 2024 03:58:11 GMT  
		Size: 62.6 MB (62642512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f11091066be848f94bc4eeeabc2e81d0838e8efd324e1b578bd06b671d975f71`  
		Last Modified: Tue, 14 May 2024 03:58:10 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.29.5` - unknown; unknown

```console
$ docker pull telegraf@sha256:88010e4986fa4a60576e0697c79e5d6891cd9566683f5687b85b4a4e54b6ad8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6313810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:595ada0f0c20a6d0f1b443672f95ac5a275cce2c9b987ba2560e1d448e760549`

```dockerfile
```

-	Layers:
	-	`sha256:18201db310e1d93bdab1da759dfe4e5d115c99221fc41df4e8b9ae643dbec959`  
		Last Modified: Tue, 14 May 2024 03:58:10 GMT  
		Size: 6.3 MB (6299203 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:018ac014087ac4ae92459a75eca9fdbdf103dc0d7425f1eb3b8035bde38d8a28`  
		Last Modified: Tue, 14 May 2024 03:58:10 GMT  
		Size: 14.6 KB (14607 bytes)  
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
$ docker pull telegraf@sha256:0e4bd174d340f3058ff29f2197d89bd3c9eed5fb07e69da9c33046270d2c3adb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.29.5-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:29830a51d9174ec4932b0f32a44c2a5696271e572402a2b9308dbc0d876a3062
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.5 MB (68485548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ae49ea2b894a59d0baa970122b87381c7f5c647bd92a0d30eff9eda1bdc3c0a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
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
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66916d60fd220360ccf9f8ce7c7629a0f7b9c16e56dc879ed453c020a7ff8c8`  
		Last Modified: Wed, 01 May 2024 21:52:33 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d681b89e78ca35ddd5dac78bea950a4dc933fb18f3662365cddc94efe62c17d`  
		Last Modified: Wed, 01 May 2024 21:52:38 GMT  
		Size: 2.6 MB (2618968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35e43ef88a1d8ac6699e940f1bb502a106c9c69dd61ec39064283029b3990893`  
		Last Modified: Wed, 01 May 2024 21:52:38 GMT  
		Size: 62.5 MB (62457243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fe64437110d2f0ec023235c3c2dbfa922dd2bc68f5b44c199bac1f117dbd382`  
		Last Modified: Wed, 01 May 2024 21:52:38 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.29.5-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:31bd3022d8ca6189b92fdf28380fa9874d03bbd4ae130bfd243d7d94dabb0fca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 MB (1380050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db7b478da9edb82e9bba1762e22889f93d651c3b5c92bead224c6c8f9606f580`

```dockerfile
```

-	Layers:
	-	`sha256:808603a313dac867ddc4e10685e3da7916e6c936ac48e56a978a915db7b2e4a1`  
		Last Modified: Wed, 01 May 2024 21:52:38 GMT  
		Size: 1.4 MB (1365200 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1c54cd2d4e7c728b5246c616629df51baac071e16bef995e8ee8a0cc4e6b02d`  
		Last Modified: Wed, 01 May 2024 21:52:38 GMT  
		Size: 14.8 KB (14850 bytes)  
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
$ docker pull telegraf@sha256:6a2e3704806806f9396c74a72cc5e7ab894204dcb6309879fa3d482c42513589
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
$ docker pull telegraf@sha256:07cd42b8f3f49d178bb00357b4f74448fe16585ad5d2871adc218e948187214f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.3 MB (155343333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ba979829ba8f4987039f70174d92e2c5a9776347ff03174d9f30bcd15cd795d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 14 May 2024 01:27:51 GMT
ADD file:b9a9fc37b874060c713002ae1ac220f097edd7c6576116c22bb15aad8229b1b3 in / 
# Tue, 14 May 2024 01:27:51 GMT
CMD ["bash"]
# Tue, 14 May 2024 02:54:40 GMT
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
	-	`sha256:c6cf28de8a067787ee0d08f8b01d7f1566a508b56f6e549687b41dfd375f12c7`  
		Last Modified: Tue, 14 May 2024 01:32:07 GMT  
		Size: 49.6 MB (49576390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:891494355808bdd3db5552f0d3723fd0fa826675f774853796fafa221d850d42`  
		Last Modified: Tue, 14 May 2024 03:04:06 GMT  
		Size: 24.1 MB (24050100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:173b929c6efddf7cfa03cb32b85af7e5eef76ccf7e09e872e6bad098c7d05bbf`  
		Last Modified: Tue, 21 May 2024 17:53:26 GMT  
		Size: 18.9 MB (18947956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28179bb3e96427e3db5bf787bac8ed46f53a18770f800e301bd086c78f07bbb5`  
		Last Modified: Tue, 21 May 2024 17:53:25 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55c34ae1f11ee1ee421df788bdf8cc0d5674c3bbe93c2b8e021f5c50fd7fce0b`  
		Last Modified: Tue, 21 May 2024 17:53:27 GMT  
		Size: 62.8 MB (62766480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41ba26e33833383f7308749d7abb7443405b6d79c97ceb9d3d46739a538aa050`  
		Last Modified: Tue, 21 May 2024 17:53:25 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.30` - unknown; unknown

```console
$ docker pull telegraf@sha256:89e0e688daeae1a822c9b860498c54efa36eb06d53638dc37ef88f556e1c65b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6314694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:feb310b9d39fc607646bf7530e7bc0ae9cb923aa3cb6943b08ede34dcc4efc39`

```dockerfile
```

-	Layers:
	-	`sha256:ddb3f48199f4c19bc0435fdf32b9f7b1c1cbb619802b6405a8993cf60917d751`  
		Last Modified: Tue, 21 May 2024 17:53:25 GMT  
		Size: 6.3 MB (6299785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cacab7abf66ef13ec06b34f0e25c4b754ac9abac74dbf074e6fe13f263a18d38`  
		Last Modified: Tue, 21 May 2024 17:53:25 GMT  
		Size: 14.9 KB (14909 bytes)  
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
$ docker pull telegraf@sha256:3f9361dbade7fa110267d348f1aececfd28d55e9305f08289af5da388294eb63
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.30-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:f80ac3a7e04b757fc00e8a7d6b26ce2728d28e898ae3252338a309de2a7e6f3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.6 MB (68608895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd66701dcc20b0646e947b9cb8860354d4a9ebecf958bf27d6dbf31bd9edcdc9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
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
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf9d56880179c0173282d206f8905f45fa9d36acc0bb3fd17168ef4ea8fed246`  
		Last Modified: Tue, 21 May 2024 17:53:27 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cccb57210f04899dea68eac0db2bfe1e7462c254532b30bccd598eb8db0d3a65`  
		Last Modified: Tue, 21 May 2024 17:53:27 GMT  
		Size: 2.6 MB (2618977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbcde6f107a71c5ce886bf1f798b0fe237f729959d2f2ffc695ed2acb37dbde9`  
		Last Modified: Tue, 21 May 2024 17:53:28 GMT  
		Size: 62.6 MB (62580582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6725ee7028bc5f73be376c1879645751daececa916b333638122ae8ead461943`  
		Last Modified: Tue, 21 May 2024 17:53:27 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.30-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:baf1983df6f26904976174963303f8cd47ec991aa70a1c328170a032032f91c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 MB (1380934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46d513343256a4bf1a6fb223bb127b915f5a8572df2df409ea8d9a2a2ad1eb3a`

```dockerfile
```

-	Layers:
	-	`sha256:c3ab684a0d57fb67f3896e010202d8f63a500d282fff70f2feab93135d7ab493`  
		Last Modified: Tue, 21 May 2024 17:53:27 GMT  
		Size: 1.4 MB (1365782 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0dfc7badb303d89ccd18de8de652b66c25f05f90e39c4337c8b00d9e94248691`  
		Last Modified: Tue, 21 May 2024 17:53:27 GMT  
		Size: 15.2 KB (15152 bytes)  
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
$ docker pull telegraf@sha256:6a2e3704806806f9396c74a72cc5e7ab894204dcb6309879fa3d482c42513589
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
$ docker pull telegraf@sha256:07cd42b8f3f49d178bb00357b4f74448fe16585ad5d2871adc218e948187214f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.3 MB (155343333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ba979829ba8f4987039f70174d92e2c5a9776347ff03174d9f30bcd15cd795d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 14 May 2024 01:27:51 GMT
ADD file:b9a9fc37b874060c713002ae1ac220f097edd7c6576116c22bb15aad8229b1b3 in / 
# Tue, 14 May 2024 01:27:51 GMT
CMD ["bash"]
# Tue, 14 May 2024 02:54:40 GMT
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
	-	`sha256:c6cf28de8a067787ee0d08f8b01d7f1566a508b56f6e549687b41dfd375f12c7`  
		Last Modified: Tue, 14 May 2024 01:32:07 GMT  
		Size: 49.6 MB (49576390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:891494355808bdd3db5552f0d3723fd0fa826675f774853796fafa221d850d42`  
		Last Modified: Tue, 14 May 2024 03:04:06 GMT  
		Size: 24.1 MB (24050100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:173b929c6efddf7cfa03cb32b85af7e5eef76ccf7e09e872e6bad098c7d05bbf`  
		Last Modified: Tue, 21 May 2024 17:53:26 GMT  
		Size: 18.9 MB (18947956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28179bb3e96427e3db5bf787bac8ed46f53a18770f800e301bd086c78f07bbb5`  
		Last Modified: Tue, 21 May 2024 17:53:25 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55c34ae1f11ee1ee421df788bdf8cc0d5674c3bbe93c2b8e021f5c50fd7fce0b`  
		Last Modified: Tue, 21 May 2024 17:53:27 GMT  
		Size: 62.8 MB (62766480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41ba26e33833383f7308749d7abb7443405b6d79c97ceb9d3d46739a538aa050`  
		Last Modified: Tue, 21 May 2024 17:53:25 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.30.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:89e0e688daeae1a822c9b860498c54efa36eb06d53638dc37ef88f556e1c65b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6314694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:feb310b9d39fc607646bf7530e7bc0ae9cb923aa3cb6943b08ede34dcc4efc39`

```dockerfile
```

-	Layers:
	-	`sha256:ddb3f48199f4c19bc0435fdf32b9f7b1c1cbb619802b6405a8993cf60917d751`  
		Last Modified: Tue, 21 May 2024 17:53:25 GMT  
		Size: 6.3 MB (6299785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cacab7abf66ef13ec06b34f0e25c4b754ac9abac74dbf074e6fe13f263a18d38`  
		Last Modified: Tue, 21 May 2024 17:53:25 GMT  
		Size: 14.9 KB (14909 bytes)  
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
$ docker pull telegraf@sha256:3f9361dbade7fa110267d348f1aececfd28d55e9305f08289af5da388294eb63
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.30.3-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:f80ac3a7e04b757fc00e8a7d6b26ce2728d28e898ae3252338a309de2a7e6f3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.6 MB (68608895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd66701dcc20b0646e947b9cb8860354d4a9ebecf958bf27d6dbf31bd9edcdc9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
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
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf9d56880179c0173282d206f8905f45fa9d36acc0bb3fd17168ef4ea8fed246`  
		Last Modified: Tue, 21 May 2024 17:53:27 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cccb57210f04899dea68eac0db2bfe1e7462c254532b30bccd598eb8db0d3a65`  
		Last Modified: Tue, 21 May 2024 17:53:27 GMT  
		Size: 2.6 MB (2618977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbcde6f107a71c5ce886bf1f798b0fe237f729959d2f2ffc695ed2acb37dbde9`  
		Last Modified: Tue, 21 May 2024 17:53:28 GMT  
		Size: 62.6 MB (62580582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6725ee7028bc5f73be376c1879645751daececa916b333638122ae8ead461943`  
		Last Modified: Tue, 21 May 2024 17:53:27 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.30.3-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:baf1983df6f26904976174963303f8cd47ec991aa70a1c328170a032032f91c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 MB (1380934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46d513343256a4bf1a6fb223bb127b915f5a8572df2df409ea8d9a2a2ad1eb3a`

```dockerfile
```

-	Layers:
	-	`sha256:c3ab684a0d57fb67f3896e010202d8f63a500d282fff70f2feab93135d7ab493`  
		Last Modified: Tue, 21 May 2024 17:53:27 GMT  
		Size: 1.4 MB (1365782 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0dfc7badb303d89ccd18de8de652b66c25f05f90e39c4337c8b00d9e94248691`  
		Last Modified: Tue, 21 May 2024 17:53:27 GMT  
		Size: 15.2 KB (15152 bytes)  
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
$ docker pull telegraf@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `telegraf:1.31-alpine`

```console
$ docker pull telegraf@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `telegraf:1.31.0`

```console
$ docker pull telegraf@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `telegraf:1.31.0-alpine`

```console
$ docker pull telegraf@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `telegraf:alpine`

```console
$ docker pull telegraf@sha256:3f9361dbade7fa110267d348f1aececfd28d55e9305f08289af5da388294eb63
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:f80ac3a7e04b757fc00e8a7d6b26ce2728d28e898ae3252338a309de2a7e6f3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.6 MB (68608895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd66701dcc20b0646e947b9cb8860354d4a9ebecf958bf27d6dbf31bd9edcdc9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
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
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf9d56880179c0173282d206f8905f45fa9d36acc0bb3fd17168ef4ea8fed246`  
		Last Modified: Tue, 21 May 2024 17:53:27 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cccb57210f04899dea68eac0db2bfe1e7462c254532b30bccd598eb8db0d3a65`  
		Last Modified: Tue, 21 May 2024 17:53:27 GMT  
		Size: 2.6 MB (2618977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbcde6f107a71c5ce886bf1f798b0fe237f729959d2f2ffc695ed2acb37dbde9`  
		Last Modified: Tue, 21 May 2024 17:53:28 GMT  
		Size: 62.6 MB (62580582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6725ee7028bc5f73be376c1879645751daececa916b333638122ae8ead461943`  
		Last Modified: Tue, 21 May 2024 17:53:27 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:baf1983df6f26904976174963303f8cd47ec991aa70a1c328170a032032f91c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 MB (1380934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46d513343256a4bf1a6fb223bb127b915f5a8572df2df409ea8d9a2a2ad1eb3a`

```dockerfile
```

-	Layers:
	-	`sha256:c3ab684a0d57fb67f3896e010202d8f63a500d282fff70f2feab93135d7ab493`  
		Last Modified: Tue, 21 May 2024 17:53:27 GMT  
		Size: 1.4 MB (1365782 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0dfc7badb303d89ccd18de8de652b66c25f05f90e39c4337c8b00d9e94248691`  
		Last Modified: Tue, 21 May 2024 17:53:27 GMT  
		Size: 15.2 KB (15152 bytes)  
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
$ docker pull telegraf@sha256:6a2e3704806806f9396c74a72cc5e7ab894204dcb6309879fa3d482c42513589
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
$ docker pull telegraf@sha256:07cd42b8f3f49d178bb00357b4f74448fe16585ad5d2871adc218e948187214f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.3 MB (155343333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ba979829ba8f4987039f70174d92e2c5a9776347ff03174d9f30bcd15cd795d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 14 May 2024 01:27:51 GMT
ADD file:b9a9fc37b874060c713002ae1ac220f097edd7c6576116c22bb15aad8229b1b3 in / 
# Tue, 14 May 2024 01:27:51 GMT
CMD ["bash"]
# Tue, 14 May 2024 02:54:40 GMT
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
	-	`sha256:c6cf28de8a067787ee0d08f8b01d7f1566a508b56f6e549687b41dfd375f12c7`  
		Last Modified: Tue, 14 May 2024 01:32:07 GMT  
		Size: 49.6 MB (49576390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:891494355808bdd3db5552f0d3723fd0fa826675f774853796fafa221d850d42`  
		Last Modified: Tue, 14 May 2024 03:04:06 GMT  
		Size: 24.1 MB (24050100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:173b929c6efddf7cfa03cb32b85af7e5eef76ccf7e09e872e6bad098c7d05bbf`  
		Last Modified: Tue, 21 May 2024 17:53:26 GMT  
		Size: 18.9 MB (18947956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28179bb3e96427e3db5bf787bac8ed46f53a18770f800e301bd086c78f07bbb5`  
		Last Modified: Tue, 21 May 2024 17:53:25 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55c34ae1f11ee1ee421df788bdf8cc0d5674c3bbe93c2b8e021f5c50fd7fce0b`  
		Last Modified: Tue, 21 May 2024 17:53:27 GMT  
		Size: 62.8 MB (62766480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41ba26e33833383f7308749d7abb7443405b6d79c97ceb9d3d46739a538aa050`  
		Last Modified: Tue, 21 May 2024 17:53:25 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:89e0e688daeae1a822c9b860498c54efa36eb06d53638dc37ef88f556e1c65b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6314694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:feb310b9d39fc607646bf7530e7bc0ae9cb923aa3cb6943b08ede34dcc4efc39`

```dockerfile
```

-	Layers:
	-	`sha256:ddb3f48199f4c19bc0435fdf32b9f7b1c1cbb619802b6405a8993cf60917d751`  
		Last Modified: Tue, 21 May 2024 17:53:25 GMT  
		Size: 6.3 MB (6299785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cacab7abf66ef13ec06b34f0e25c4b754ac9abac74dbf074e6fe13f263a18d38`  
		Last Modified: Tue, 21 May 2024 17:53:25 GMT  
		Size: 14.9 KB (14909 bytes)  
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
