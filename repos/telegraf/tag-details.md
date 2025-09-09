<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `telegraf`

-	[`telegraf:1.34`](#telegraf134)
-	[`telegraf:1.34-alpine`](#telegraf134-alpine)
-	[`telegraf:1.34.4`](#telegraf1344)
-	[`telegraf:1.34.4-alpine`](#telegraf1344-alpine)
-	[`telegraf:1.35`](#telegraf135)
-	[`telegraf:1.35-alpine`](#telegraf135-alpine)
-	[`telegraf:1.35.4`](#telegraf1354)
-	[`telegraf:1.35.4-alpine`](#telegraf1354-alpine)
-	[`telegraf:1.36`](#telegraf136)
-	[`telegraf:1.36-alpine`](#telegraf136-alpine)
-	[`telegraf:1.36.1`](#telegraf1361)
-	[`telegraf:1.36.1-alpine`](#telegraf1361-alpine)
-	[`telegraf:alpine`](#telegrafalpine)
-	[`telegraf:latest`](#telegraflatest)

## `telegraf:1.34`

```console
$ docker pull telegraf@sha256:b8a75db2ce3959925019a14b632a258677aae7a1f10bcfb1b6c600d473721121
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.34` - linux; amd64

```console
$ docker pull telegraf@sha256:634b237ed27cfc0ea2dd24470648c529b7e06665f5a67d23a8d0c1a8767d5920
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.9 MB (168898019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc441610f3d1f8dd48ce1aaf251f9b85ed88ad267c3dfd60efc6f7402b41d508`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
ENV TELEGRAF_VERSION=1.34.4
# Tue, 19 Aug 2025 08:40:07 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 19 Aug 2025 08:40:07 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Aug 2025 08:40:07 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:8fb375ec14f3df8b31b70d0216508565ab7264a7e16cac4f8cc07f8eca22445f`  
		Last Modified: Mon, 08 Sep 2025 21:12:37 GMT  
		Size: 48.5 MB (48480610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccbbb2080a06a2888e44131965340c1eccd23f4d49efe72176246649abfbf9d9`  
		Last Modified: Mon, 08 Sep 2025 21:54:14 GMT  
		Size: 24.0 MB (24025996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:713c0828c39ab022dbf13ba47edb1968e8b2e5c9c0479f3035c18c3e3f69f08f`  
		Last Modified: Tue, 09 Sep 2025 00:10:19 GMT  
		Size: 18.9 MB (18942765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adbd87b60718d74054de983d4a9266a059766adfe7c598cc2a2cee738db0bc1d`  
		Last Modified: Mon, 08 Sep 2025 22:38:30 GMT  
		Size: 1.8 KB (1784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b08dbc3b287c8de62508162e19edf850157fe47256d1503e33a8969d4667dae8`  
		Last Modified: Tue, 09 Sep 2025 00:10:24 GMT  
		Size: 77.4 MB (77446240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:967cfee02b473da3c46b4b284d322cd048f4cccb968bb8f6c355518fb48806e5`  
		Last Modified: Mon, 08 Sep 2025 22:38:33 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.34` - unknown; unknown

```console
$ docker pull telegraf@sha256:f8670880cdbc5dcc824a09b211a2d4471d052052a628023793f56e94ce61f2ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6644690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7441e4e50d74d617cdbe8008ad27242adbc44da8d6016e29960d83f3033159de`

```dockerfile
```

-	Layers:
	-	`sha256:6ea4aab32c3dbd6ef0d220d3fb13bcec687b8dc7ac2fb7d33a5fded4862a5f32`  
		Last Modified: Tue, 09 Sep 2025 00:10:18 GMT  
		Size: 6.6 MB (6630220 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5bfa398a00445bf8f2faa865d20821cdc8f16fd531314e5df0fb31f967dc03f`  
		Last Modified: Tue, 09 Sep 2025 00:10:19 GMT  
		Size: 14.5 KB (14470 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.34` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:b43f0038614a559504ba11a976eccb5923e7ad082435ae9daf76fcb24387852d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.4 MB (155379360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e023a33a8eb30de1e69021a6ba747ddd10e9148c972a8a2ff585fdabe401535`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1757289600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Sep 2025 21:35:06 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Sep 2025 21:35:06 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 08 Sep 2025 21:35:06 GMT
ENV TELEGRAF_VERSION=1.34.4
# Mon, 08 Sep 2025 21:35:06 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 08 Sep 2025 21:35:06 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 08 Sep 2025 21:35:06 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 08 Sep 2025 21:35:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Sep 2025 21:35:06 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:66de9a3b6b96c15de3235377e1618295643161d16058e17bde51f54951c6ec21`  
		Last Modified: Mon, 08 Sep 2025 21:14:33 GMT  
		Size: 44.2 MB (44195998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0efd1e8889a5c39ed7ad3628cf08e3daff474f9ff5b33972b323c79f306440f8`  
		Last Modified: Mon, 08 Sep 2025 23:37:54 GMT  
		Size: 21.9 MB (21931079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cf37909f7ac4e3f15c2c7ecacc16fa58ef82d28624bff9276a057663fd0976d`  
		Last Modified: Tue, 09 Sep 2025 04:48:49 GMT  
		Size: 17.7 MB (17722690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:357da611076f9bea097256a99992d403698e61db6ab4457d659bac12e58128f0`  
		Last Modified: Tue, 09 Sep 2025 04:17:08 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b7e4549d65810a4409c13b03032262e90355f619efd0ca8ca95eae9961f013c`  
		Last Modified: Tue, 09 Sep 2025 06:16:00 GMT  
		Size: 71.5 MB (71527197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:855fa5a11739d4afae0f7dad1c02389e01218fa53110c34656833e407ce88167`  
		Last Modified: Tue, 09 Sep 2025 04:19:58 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.34` - unknown; unknown

```console
$ docker pull telegraf@sha256:16ea68656455d5a131196e9039ca5c81d566fcf18601622657bacaea1fbab2c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6639375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11f6eb56d7d96fe6e2026889dc00440f86652b27dfac7a7a3c99349949cd94bb`

```dockerfile
```

-	Layers:
	-	`sha256:4a79d4ed9712f1bed8e6d4ccdf32293f33ccb60fc6c24a1c56bdd6e6b14bc345`  
		Last Modified: Tue, 09 Sep 2025 06:10:25 GMT  
		Size: 6.6 MB (6624815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:537cc0f5152c02aefc5bac7d4ba8a0bdc7fc9d86160c55571c6e82157129fb5b`  
		Last Modified: Tue, 09 Sep 2025 06:10:26 GMT  
		Size: 14.6 KB (14560 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.34` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:ee4eaf636b601633f4cf2fcdd3891bb9a0d9da760d6448633b1f836756851f40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.0 MB (161041352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a85c6cf84655561b309d817a55916d1c0e12bcd751ca91407b0f19fc0642cfe`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1757289600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Sep 2025 21:35:06 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Sep 2025 21:35:06 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 08 Sep 2025 21:35:06 GMT
ENV TELEGRAF_VERSION=1.34.4
# Mon, 08 Sep 2025 21:35:06 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 08 Sep 2025 21:35:06 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 08 Sep 2025 21:35:06 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 08 Sep 2025 21:35:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Sep 2025 21:35:06 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:a9331b686701a987bcd276cc69a0f676d471ccda1aa353d2f7fad017f2894cd0`  
		Last Modified: Mon, 08 Sep 2025 21:14:32 GMT  
		Size: 48.4 MB (48359019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e108925666d6d84c8fa32751877e66a295ad55c9fbd10142325b99d60e786e17`  
		Last Modified: Mon, 08 Sep 2025 22:21:46 GMT  
		Size: 23.6 MB (23594789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9932a094b7d24e4069b55fbe3bb8fa068f21ab38e3e8f1879f0dd9fd28cb078a`  
		Last Modified: Tue, 09 Sep 2025 03:12:38 GMT  
		Size: 18.9 MB (18883952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fed7d73b45d897627e75245933352c9b6b80085fe055330355ff7e1c1e58468`  
		Last Modified: Tue, 09 Sep 2025 02:21:38 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:053fede7b0d036e1805b9180f40554e65dfdaac8590743b383257c2b3e475aba`  
		Last Modified: Tue, 09 Sep 2025 03:15:57 GMT  
		Size: 70.2 MB (70201196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17c3816148bf2042c34720fa1b52bb588219d77bcff549af664ec2111cf8b06a`  
		Last Modified: Tue, 09 Sep 2025 02:21:38 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.34` - unknown; unknown

```console
$ docker pull telegraf@sha256:9220a38d09eb96583272511d477d8bb41a876d27934aaa2360b039255035fddd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6645475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b4c1e1bbf24c84440392bbb381eb5345f37bfeeb4e686a905442c161e102cc2`

```dockerfile
```

-	Layers:
	-	`sha256:e887f05ef9732c63d77ce457008b6153862190fe1882237256be29146c76dc3a`  
		Last Modified: Tue, 09 Sep 2025 03:10:25 GMT  
		Size: 6.6 MB (6630896 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d48e5ce916ccba829b9a7355e900d158201796d179e5ee10c791f654ce6a41f8`  
		Last Modified: Tue, 09 Sep 2025 03:10:26 GMT  
		Size: 14.6 KB (14579 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.34-alpine`

```console
$ docker pull telegraf@sha256:9be449277b6e16b04c256e629f93828212eb22ab7078d8cfc31eabb8f235958e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.34-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:e362bcc7d4ae010b3a0c3e4d8b1f9bf282889ad6f7ea994b2b3880e48c475013
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.3 MB (83297830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a95af6019e0f47aab1b15987c237287a5ef2e1b0b0ba2212a018af58df10444b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 08 Jul 2025 13:49:16 GMT
ADD alpine-minirootfs-3.20.7-x86_64.tar.gz / # buildkit
# Tue, 08 Jul 2025 13:49:16 GMT
CMD ["/bin/sh"]
# Tue, 08 Jul 2025 13:49:16 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 08 Jul 2025 13:49:16 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Tue, 08 Jul 2025 13:49:16 GMT
ENV TELEGRAF_VERSION=1.34.4
# Tue, 08 Jul 2025 13:49:16 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Tue, 08 Jul 2025 13:49:16 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 08 Jul 2025 13:49:16 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 08 Jul 2025 13:49:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 08 Jul 2025 13:49:16 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:01d036902a3ca86e8793073c8094cba44d83a38953a489ac0641f3de017fe2d2`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3620477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0189be59b6d310438ecb57749d0b53be563f40ffe1756830daa09c83bef8415`  
		Last Modified: Tue, 15 Jul 2025 19:29:47 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:849892cdebd263b6f41ddad1e9e9871a82acbc1ec12f6f6b59662c23a53ecbf1`  
		Last Modified: Tue, 15 Jul 2025 19:29:47 GMT  
		Size: 2.4 MB (2439839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:316eafe4c20455456d584383463ddea70937a57b18aec6228e29596ee9de83a7`  
		Last Modified: Tue, 15 Jul 2025 19:30:07 GMT  
		Size: 77.2 MB (77236907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f076fa9b0654a47181d7442facaee6b922f57fa5852d7fc10dd0be83c120b346`  
		Last Modified: Tue, 15 Jul 2025 19:29:47 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.34-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:e15eb7de3d16b848ef39912698dda6c995896e073b4008ad9600961cdb860db9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1115137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f198cead148de598872801d73980fdb724789579180ff32cfe6f04947dad89a`

```dockerfile
```

-	Layers:
	-	`sha256:d3ea611838b71a81e7a7367547df6df24cef1c638e19546e4dc7e33cc7a068de`  
		Last Modified: Tue, 15 Jul 2025 21:10:26 GMT  
		Size: 1.1 MB (1100176 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:625f67f8eb83f5062222a4600b78ea3fe502964fed0a9a5926fb7bc39e252874`  
		Last Modified: Tue, 15 Jul 2025 21:10:27 GMT  
		Size: 15.0 KB (14961 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.34-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:5b64250fc700aeebd3f26215ece94e7341b6e7d58d45d99523b55053d6f91eef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.6 MB (76607035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdc67083c4f61db20b3105fe2cd30bcf445b17a5158845f1d0d70dce9347dbc6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 08 Jul 2025 13:49:16 GMT
ADD alpine-minirootfs-3.20.7-aarch64.tar.gz / # buildkit
# Tue, 08 Jul 2025 13:49:16 GMT
CMD ["/bin/sh"]
# Tue, 08 Jul 2025 13:49:16 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 08 Jul 2025 13:49:16 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Tue, 08 Jul 2025 13:49:16 GMT
ENV TELEGRAF_VERSION=1.34.4
# Tue, 08 Jul 2025 13:49:16 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Tue, 08 Jul 2025 13:49:16 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 08 Jul 2025 13:49:16 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 08 Jul 2025 13:49:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 08 Jul 2025 13:49:16 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:13e713f825654e9e4f57146ec84918d478434f708d4d3d9d18d0e7ba2be56801`  
		Last Modified: Tue, 15 Jul 2025 19:00:10 GMT  
		Size: 4.1 MB (4088368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fa97d491d631a48e4505bc7c819c75f4b17b81cb0aa363976f80703a1234abb`  
		Last Modified: Wed, 16 Jul 2025 05:48:09 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60e3d554c3bbc91882bf606a734d925d5ed86684e95c17dc1c4086533c11d92d`  
		Last Modified: Wed, 16 Jul 2025 05:48:12 GMT  
		Size: 2.5 MB (2521335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86d0fd404ed95c46e6aea3a067faf07519cbf026660c39be7025cd50716ea7f2`  
		Last Modified: Wed, 16 Jul 2025 05:53:22 GMT  
		Size: 70.0 MB (69996726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b8c75c3500cb4a7e076b1b9b4f29b7e03521b0ece8f93dd40ebd6daf77abb00`  
		Last Modified: Wed, 16 Jul 2025 05:53:21 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.34-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:e3e029dcd13960995bf695390d4a2863fbd47f5a8130d6e768e12b90244327da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1110874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7223847de5ba827672f9a137203b3140516fd02c91cd068c3052bca535e9171`

```dockerfile
```

-	Layers:
	-	`sha256:011b777430464b8e65f955ffc476335083996826eff86889230201ccf2006966`  
		Last Modified: Wed, 16 Jul 2025 09:10:27 GMT  
		Size: 1.1 MB (1095803 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de9bd2eeda1dc84918e31e2ed46ae9d5f948064f10caa04e320d93e42d3e633e`  
		Last Modified: Wed, 16 Jul 2025 09:10:28 GMT  
		Size: 15.1 KB (15071 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.34.4`

```console
$ docker pull telegraf@sha256:b8a75db2ce3959925019a14b632a258677aae7a1f10bcfb1b6c600d473721121
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.34.4` - linux; amd64

```console
$ docker pull telegraf@sha256:634b237ed27cfc0ea2dd24470648c529b7e06665f5a67d23a8d0c1a8767d5920
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.9 MB (168898019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc441610f3d1f8dd48ce1aaf251f9b85ed88ad267c3dfd60efc6f7402b41d508`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
ENV TELEGRAF_VERSION=1.34.4
# Tue, 19 Aug 2025 08:40:07 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 19 Aug 2025 08:40:07 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Aug 2025 08:40:07 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:8fb375ec14f3df8b31b70d0216508565ab7264a7e16cac4f8cc07f8eca22445f`  
		Last Modified: Mon, 08 Sep 2025 21:12:37 GMT  
		Size: 48.5 MB (48480610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccbbb2080a06a2888e44131965340c1eccd23f4d49efe72176246649abfbf9d9`  
		Last Modified: Mon, 08 Sep 2025 21:54:14 GMT  
		Size: 24.0 MB (24025996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:713c0828c39ab022dbf13ba47edb1968e8b2e5c9c0479f3035c18c3e3f69f08f`  
		Last Modified: Tue, 09 Sep 2025 00:10:19 GMT  
		Size: 18.9 MB (18942765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adbd87b60718d74054de983d4a9266a059766adfe7c598cc2a2cee738db0bc1d`  
		Last Modified: Mon, 08 Sep 2025 22:38:30 GMT  
		Size: 1.8 KB (1784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b08dbc3b287c8de62508162e19edf850157fe47256d1503e33a8969d4667dae8`  
		Last Modified: Tue, 09 Sep 2025 00:10:24 GMT  
		Size: 77.4 MB (77446240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:967cfee02b473da3c46b4b284d322cd048f4cccb968bb8f6c355518fb48806e5`  
		Last Modified: Mon, 08 Sep 2025 22:38:33 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.34.4` - unknown; unknown

```console
$ docker pull telegraf@sha256:f8670880cdbc5dcc824a09b211a2d4471d052052a628023793f56e94ce61f2ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6644690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7441e4e50d74d617cdbe8008ad27242adbc44da8d6016e29960d83f3033159de`

```dockerfile
```

-	Layers:
	-	`sha256:6ea4aab32c3dbd6ef0d220d3fb13bcec687b8dc7ac2fb7d33a5fded4862a5f32`  
		Last Modified: Tue, 09 Sep 2025 00:10:18 GMT  
		Size: 6.6 MB (6630220 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5bfa398a00445bf8f2faa865d20821cdc8f16fd531314e5df0fb31f967dc03f`  
		Last Modified: Tue, 09 Sep 2025 00:10:19 GMT  
		Size: 14.5 KB (14470 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.34.4` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:b43f0038614a559504ba11a976eccb5923e7ad082435ae9daf76fcb24387852d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.4 MB (155379360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e023a33a8eb30de1e69021a6ba747ddd10e9148c972a8a2ff585fdabe401535`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1757289600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Sep 2025 21:35:06 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Sep 2025 21:35:06 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 08 Sep 2025 21:35:06 GMT
ENV TELEGRAF_VERSION=1.34.4
# Mon, 08 Sep 2025 21:35:06 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 08 Sep 2025 21:35:06 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 08 Sep 2025 21:35:06 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 08 Sep 2025 21:35:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Sep 2025 21:35:06 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:66de9a3b6b96c15de3235377e1618295643161d16058e17bde51f54951c6ec21`  
		Last Modified: Mon, 08 Sep 2025 21:14:33 GMT  
		Size: 44.2 MB (44195998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0efd1e8889a5c39ed7ad3628cf08e3daff474f9ff5b33972b323c79f306440f8`  
		Last Modified: Mon, 08 Sep 2025 23:37:54 GMT  
		Size: 21.9 MB (21931079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cf37909f7ac4e3f15c2c7ecacc16fa58ef82d28624bff9276a057663fd0976d`  
		Last Modified: Tue, 09 Sep 2025 04:48:49 GMT  
		Size: 17.7 MB (17722690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:357da611076f9bea097256a99992d403698e61db6ab4457d659bac12e58128f0`  
		Last Modified: Tue, 09 Sep 2025 04:17:08 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b7e4549d65810a4409c13b03032262e90355f619efd0ca8ca95eae9961f013c`  
		Last Modified: Tue, 09 Sep 2025 06:16:00 GMT  
		Size: 71.5 MB (71527197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:855fa5a11739d4afae0f7dad1c02389e01218fa53110c34656833e407ce88167`  
		Last Modified: Tue, 09 Sep 2025 04:19:58 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.34.4` - unknown; unknown

```console
$ docker pull telegraf@sha256:16ea68656455d5a131196e9039ca5c81d566fcf18601622657bacaea1fbab2c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6639375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11f6eb56d7d96fe6e2026889dc00440f86652b27dfac7a7a3c99349949cd94bb`

```dockerfile
```

-	Layers:
	-	`sha256:4a79d4ed9712f1bed8e6d4ccdf32293f33ccb60fc6c24a1c56bdd6e6b14bc345`  
		Last Modified: Tue, 09 Sep 2025 06:10:25 GMT  
		Size: 6.6 MB (6624815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:537cc0f5152c02aefc5bac7d4ba8a0bdc7fc9d86160c55571c6e82157129fb5b`  
		Last Modified: Tue, 09 Sep 2025 06:10:26 GMT  
		Size: 14.6 KB (14560 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.34.4` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:ee4eaf636b601633f4cf2fcdd3891bb9a0d9da760d6448633b1f836756851f40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.0 MB (161041352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a85c6cf84655561b309d817a55916d1c0e12bcd751ca91407b0f19fc0642cfe`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1757289600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Sep 2025 21:35:06 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Sep 2025 21:35:06 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 08 Sep 2025 21:35:06 GMT
ENV TELEGRAF_VERSION=1.34.4
# Mon, 08 Sep 2025 21:35:06 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 08 Sep 2025 21:35:06 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 08 Sep 2025 21:35:06 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 08 Sep 2025 21:35:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Sep 2025 21:35:06 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:a9331b686701a987bcd276cc69a0f676d471ccda1aa353d2f7fad017f2894cd0`  
		Last Modified: Mon, 08 Sep 2025 21:14:32 GMT  
		Size: 48.4 MB (48359019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e108925666d6d84c8fa32751877e66a295ad55c9fbd10142325b99d60e786e17`  
		Last Modified: Mon, 08 Sep 2025 22:21:46 GMT  
		Size: 23.6 MB (23594789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9932a094b7d24e4069b55fbe3bb8fa068f21ab38e3e8f1879f0dd9fd28cb078a`  
		Last Modified: Tue, 09 Sep 2025 03:12:38 GMT  
		Size: 18.9 MB (18883952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fed7d73b45d897627e75245933352c9b6b80085fe055330355ff7e1c1e58468`  
		Last Modified: Tue, 09 Sep 2025 02:21:38 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:053fede7b0d036e1805b9180f40554e65dfdaac8590743b383257c2b3e475aba`  
		Last Modified: Tue, 09 Sep 2025 03:15:57 GMT  
		Size: 70.2 MB (70201196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17c3816148bf2042c34720fa1b52bb588219d77bcff549af664ec2111cf8b06a`  
		Last Modified: Tue, 09 Sep 2025 02:21:38 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.34.4` - unknown; unknown

```console
$ docker pull telegraf@sha256:9220a38d09eb96583272511d477d8bb41a876d27934aaa2360b039255035fddd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6645475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b4c1e1bbf24c84440392bbb381eb5345f37bfeeb4e686a905442c161e102cc2`

```dockerfile
```

-	Layers:
	-	`sha256:e887f05ef9732c63d77ce457008b6153862190fe1882237256be29146c76dc3a`  
		Last Modified: Tue, 09 Sep 2025 03:10:25 GMT  
		Size: 6.6 MB (6630896 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d48e5ce916ccba829b9a7355e900d158201796d179e5ee10c791f654ce6a41f8`  
		Last Modified: Tue, 09 Sep 2025 03:10:26 GMT  
		Size: 14.6 KB (14579 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.34.4-alpine`

```console
$ docker pull telegraf@sha256:9be449277b6e16b04c256e629f93828212eb22ab7078d8cfc31eabb8f235958e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.34.4-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:e362bcc7d4ae010b3a0c3e4d8b1f9bf282889ad6f7ea994b2b3880e48c475013
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.3 MB (83297830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a95af6019e0f47aab1b15987c237287a5ef2e1b0b0ba2212a018af58df10444b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 08 Jul 2025 13:49:16 GMT
ADD alpine-minirootfs-3.20.7-x86_64.tar.gz / # buildkit
# Tue, 08 Jul 2025 13:49:16 GMT
CMD ["/bin/sh"]
# Tue, 08 Jul 2025 13:49:16 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 08 Jul 2025 13:49:16 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Tue, 08 Jul 2025 13:49:16 GMT
ENV TELEGRAF_VERSION=1.34.4
# Tue, 08 Jul 2025 13:49:16 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Tue, 08 Jul 2025 13:49:16 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 08 Jul 2025 13:49:16 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 08 Jul 2025 13:49:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 08 Jul 2025 13:49:16 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:01d036902a3ca86e8793073c8094cba44d83a38953a489ac0641f3de017fe2d2`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3620477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0189be59b6d310438ecb57749d0b53be563f40ffe1756830daa09c83bef8415`  
		Last Modified: Tue, 15 Jul 2025 19:29:47 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:849892cdebd263b6f41ddad1e9e9871a82acbc1ec12f6f6b59662c23a53ecbf1`  
		Last Modified: Tue, 15 Jul 2025 19:29:47 GMT  
		Size: 2.4 MB (2439839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:316eafe4c20455456d584383463ddea70937a57b18aec6228e29596ee9de83a7`  
		Last Modified: Tue, 15 Jul 2025 19:30:07 GMT  
		Size: 77.2 MB (77236907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f076fa9b0654a47181d7442facaee6b922f57fa5852d7fc10dd0be83c120b346`  
		Last Modified: Tue, 15 Jul 2025 19:29:47 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.34.4-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:e15eb7de3d16b848ef39912698dda6c995896e073b4008ad9600961cdb860db9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1115137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f198cead148de598872801d73980fdb724789579180ff32cfe6f04947dad89a`

```dockerfile
```

-	Layers:
	-	`sha256:d3ea611838b71a81e7a7367547df6df24cef1c638e19546e4dc7e33cc7a068de`  
		Last Modified: Tue, 15 Jul 2025 21:10:26 GMT  
		Size: 1.1 MB (1100176 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:625f67f8eb83f5062222a4600b78ea3fe502964fed0a9a5926fb7bc39e252874`  
		Last Modified: Tue, 15 Jul 2025 21:10:27 GMT  
		Size: 15.0 KB (14961 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.34.4-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:5b64250fc700aeebd3f26215ece94e7341b6e7d58d45d99523b55053d6f91eef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.6 MB (76607035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdc67083c4f61db20b3105fe2cd30bcf445b17a5158845f1d0d70dce9347dbc6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 08 Jul 2025 13:49:16 GMT
ADD alpine-minirootfs-3.20.7-aarch64.tar.gz / # buildkit
# Tue, 08 Jul 2025 13:49:16 GMT
CMD ["/bin/sh"]
# Tue, 08 Jul 2025 13:49:16 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 08 Jul 2025 13:49:16 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Tue, 08 Jul 2025 13:49:16 GMT
ENV TELEGRAF_VERSION=1.34.4
# Tue, 08 Jul 2025 13:49:16 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Tue, 08 Jul 2025 13:49:16 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 08 Jul 2025 13:49:16 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 08 Jul 2025 13:49:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 08 Jul 2025 13:49:16 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:13e713f825654e9e4f57146ec84918d478434f708d4d3d9d18d0e7ba2be56801`  
		Last Modified: Tue, 15 Jul 2025 19:00:10 GMT  
		Size: 4.1 MB (4088368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fa97d491d631a48e4505bc7c819c75f4b17b81cb0aa363976f80703a1234abb`  
		Last Modified: Wed, 16 Jul 2025 05:48:09 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60e3d554c3bbc91882bf606a734d925d5ed86684e95c17dc1c4086533c11d92d`  
		Last Modified: Wed, 16 Jul 2025 05:48:12 GMT  
		Size: 2.5 MB (2521335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86d0fd404ed95c46e6aea3a067faf07519cbf026660c39be7025cd50716ea7f2`  
		Last Modified: Wed, 16 Jul 2025 05:53:22 GMT  
		Size: 70.0 MB (69996726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b8c75c3500cb4a7e076b1b9b4f29b7e03521b0ece8f93dd40ebd6daf77abb00`  
		Last Modified: Wed, 16 Jul 2025 05:53:21 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.34.4-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:e3e029dcd13960995bf695390d4a2863fbd47f5a8130d6e768e12b90244327da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1110874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7223847de5ba827672f9a137203b3140516fd02c91cd068c3052bca535e9171`

```dockerfile
```

-	Layers:
	-	`sha256:011b777430464b8e65f955ffc476335083996826eff86889230201ccf2006966`  
		Last Modified: Wed, 16 Jul 2025 09:10:27 GMT  
		Size: 1.1 MB (1095803 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de9bd2eeda1dc84918e31e2ed46ae9d5f948064f10caa04e320d93e42d3e633e`  
		Last Modified: Wed, 16 Jul 2025 09:10:28 GMT  
		Size: 15.1 KB (15071 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.35`

```console
$ docker pull telegraf@sha256:6a052a237e217637f0f2a17c82af8c08f254a5f753d4b16db05261530bb17a18
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.35` - linux; amd64

```console
$ docker pull telegraf@sha256:36d255dd9ae95d3e27b946eb1fe0b49fc2af2345008072da50014e4bcda242ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.0 MB (171022468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf0dc6c618d32f6cde59aec8a49d929007d42b66db90f523a03c87efb89da0ac`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
ENV TELEGRAF_VERSION=1.35.4
# Tue, 19 Aug 2025 08:40:07 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 19 Aug 2025 08:40:07 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Aug 2025 08:40:07 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:8fb375ec14f3df8b31b70d0216508565ab7264a7e16cac4f8cc07f8eca22445f`  
		Last Modified: Mon, 08 Sep 2025 21:12:37 GMT  
		Size: 48.5 MB (48480610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccbbb2080a06a2888e44131965340c1eccd23f4d49efe72176246649abfbf9d9`  
		Last Modified: Mon, 08 Sep 2025 21:54:14 GMT  
		Size: 24.0 MB (24025996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93f0e44eea62b373168e2637ef3acd7d9c0cdc1f54e46dbba237c53ffe1a6677`  
		Last Modified: Mon, 08 Sep 2025 23:07:11 GMT  
		Size: 18.9 MB (18942775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0b8e00afe64f97c33175f8fd3049909003fc239302631480338eada1d36e866`  
		Last Modified: Mon, 08 Sep 2025 22:38:28 GMT  
		Size: 1.8 KB (1772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28e040dee2cd7e3fe769dbf2c2d7354e6001775cbf76d3ecaba320d245a47391`  
		Last Modified: Mon, 08 Sep 2025 23:07:23 GMT  
		Size: 79.6 MB (79570693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44d38927b48db8048f0c4e35f6b04babcf2270a93ac7b3123fa1e51a3049676e`  
		Last Modified: Mon, 08 Sep 2025 22:38:32 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35` - unknown; unknown

```console
$ docker pull telegraf@sha256:9b16d545ae6013b56868cd457f45e3f0307b650a64427869a8ce59884cd01193
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6660020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bfa191c748905e60046920fe24441aacd2d46d7291b6276e72faa1e69a835fe`

```dockerfile
```

-	Layers:
	-	`sha256:986b097123cd85a28ac5c30b5895d3005769d9941e963c1b1ee283e5d579f842`  
		Last Modified: Tue, 09 Sep 2025 00:10:26 GMT  
		Size: 6.6 MB (6645248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3460e2249de1c5dc714828e70f912f1132d32b07cab2fd1c11853efa3ace949b`  
		Last Modified: Tue, 09 Sep 2025 00:10:27 GMT  
		Size: 14.8 KB (14772 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.35` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:73251f8e80ba2a176904f1014f141848212f993a3181dbfbfa702a3f58561068
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.1 MB (157142865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80ed48bde4daddea121bad996029829e89fd7c46d345ec36a42ac3d83b2c6204`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1757289600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Sep 2025 21:35:06 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Sep 2025 21:35:06 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 08 Sep 2025 21:35:06 GMT
ENV TELEGRAF_VERSION=1.35.4
# Mon, 08 Sep 2025 21:35:06 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 08 Sep 2025 21:35:06 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 08 Sep 2025 21:35:06 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 08 Sep 2025 21:35:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Sep 2025 21:35:06 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:66de9a3b6b96c15de3235377e1618295643161d16058e17bde51f54951c6ec21`  
		Last Modified: Mon, 08 Sep 2025 21:14:33 GMT  
		Size: 44.2 MB (44195998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0efd1e8889a5c39ed7ad3628cf08e3daff474f9ff5b33972b323c79f306440f8`  
		Last Modified: Mon, 08 Sep 2025 23:37:54 GMT  
		Size: 21.9 MB (21931079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f80a54b7f01bb44d60641a76d77f5c6f5ffef4675de6dd1e1907d53a015a701`  
		Last Modified: Tue, 09 Sep 2025 06:16:09 GMT  
		Size: 17.7 MB (17722675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf9748a0def3f6fc0246ff5eb830a45c4fd8b6f151645e505888c42dc00e025c`  
		Last Modified: Tue, 09 Sep 2025 04:16:57 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9911e37b7fced99e41e1cb55198ed88a3c2de39ad5bdf8ac99c153f634b9eea2`  
		Last Modified: Tue, 09 Sep 2025 06:16:14 GMT  
		Size: 73.3 MB (73290717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1179e6bedb78b31947328fd7aa31e009cfa13536a9f7643581e9406787eb503a`  
		Last Modified: Tue, 09 Sep 2025 04:16:52 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35` - unknown; unknown

```console
$ docker pull telegraf@sha256:e3c70aff846f07811a97e1cec87441063c5d9c8a0f8814000260fb77d28e129d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6654103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b7afb311271f05ea122c1692b882428ad874947d2efb60c37d48ecfefef0e91`

```dockerfile
```

-	Layers:
	-	`sha256:b56d101f4fb860a115d90967f223dd19049d51333ea7e6762171ae57b5a3e406`  
		Last Modified: Tue, 09 Sep 2025 06:10:33 GMT  
		Size: 6.6 MB (6639543 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40244ab12e75c0f773558aaa32db9b48ec4cd5cd5e88c4cd06268cafb8aadadb`  
		Last Modified: Tue, 09 Sep 2025 06:10:34 GMT  
		Size: 14.6 KB (14560 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.35` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:beda89f31055dacaa4aab8af2f661e7101c079fb49011c51a01b8ce2ccd26cf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.9 MB (162919482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a23c1ed157cc6c6c2c8d54f7a3273716665e6ee465f9df914d2b42cc998a3e99`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1757289600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Sep 2025 21:35:06 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Sep 2025 21:35:06 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 08 Sep 2025 21:35:06 GMT
ENV TELEGRAF_VERSION=1.35.4
# Mon, 08 Sep 2025 21:35:06 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 08 Sep 2025 21:35:06 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 08 Sep 2025 21:35:06 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 08 Sep 2025 21:35:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Sep 2025 21:35:06 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:a9331b686701a987bcd276cc69a0f676d471ccda1aa353d2f7fad017f2894cd0`  
		Last Modified: Mon, 08 Sep 2025 21:14:32 GMT  
		Size: 48.4 MB (48359019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e108925666d6d84c8fa32751877e66a295ad55c9fbd10142325b99d60e786e17`  
		Last Modified: Mon, 08 Sep 2025 22:21:46 GMT  
		Size: 23.6 MB (23594789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a26e220328f978177fc338e1213ed5da76b98168101ff01a34a0ee25977092a`  
		Last Modified: Tue, 09 Sep 2025 03:16:07 GMT  
		Size: 18.9 MB (18883991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a48fcfc61f533fef671c379efbc2af295fd7f0cfcca748a87b2359f17726f618`  
		Last Modified: Tue, 09 Sep 2025 02:21:43 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6f4f905731802674abda750b5c62c670905e230428f8e5982dc9c3d845517a2`  
		Last Modified: Tue, 09 Sep 2025 03:16:12 GMT  
		Size: 72.1 MB (72079289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbe1d30585ad2b6e481fa11dd96b53146aea79dcfc04bf012bc2b4496e85199c`  
		Last Modified: Tue, 09 Sep 2025 02:21:44 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35` - unknown; unknown

```console
$ docker pull telegraf@sha256:6f8dd0fa2aa72d4a4e6d9ad6c37da014271a40561e17f35eb639eba75e9a4c99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6660201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f986f48b37a0733a178ab12258ce2ef091d2aa0640647387f1bb32a0c139fb77`

```dockerfile
```

-	Layers:
	-	`sha256:dcecae63d898843bb4ecccab3750c6292fe0139bda17df6f9802a3f0dd351787`  
		Last Modified: Tue, 09 Sep 2025 03:10:35 GMT  
		Size: 6.6 MB (6645622 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe13d7882936c8c492bb0d8e1c3b2d0de424aba262b478f8632f03180db4c51f`  
		Last Modified: Tue, 09 Sep 2025 03:10:36 GMT  
		Size: 14.6 KB (14579 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.35-alpine`

```console
$ docker pull telegraf@sha256:c2f97b178be0d6da47934693aab5f12968d4c357067466b00750d7c883c7ca5d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.35-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:b9f1dad8bfc6e2e0a071ec3708f69b608314a1638df1a27dbee6c8d9c201157d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.7 MB (85721229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1898bfc2837a825d9ca57c11162f841378cca6e17895db8ff8007425b40ae030`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 19 Aug 2025 08:40:07 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
ENV TELEGRAF_VERSION=1.35.4
# Tue, 19 Aug 2025 08:40:07 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 19 Aug 2025 08:40:07 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Aug 2025 08:40:07 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:111a65e71ad846fe6bc5cf5d9981577f402356a07fa8643556a52a493832248d`  
		Last Modified: Tue, 19 Aug 2025 16:43:11 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30cbaff1778259b3073527b025ae9ab08156e23a8b7f42fbbc0fafca178fc2a4`  
		Last Modified: Tue, 19 Aug 2025 16:43:11 GMT  
		Size: 2.6 MB (2552105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e527cfac45a96a64d7cc6821810e5660eec3f9f105ee9595ff5d0ef9ce3889e5`  
		Last Modified: Tue, 19 Aug 2025 16:43:18 GMT  
		Size: 79.4 MB (79368534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:701fb22e4edb908e9c9db1946c3275c80eb50f1b6a4a0a263e2bcc780d2db6cb`  
		Last Modified: Tue, 19 Aug 2025 16:43:13 GMT  
		Size: 621.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:d62ff060ab03e0e18dd18b68bef85d0e6253116947fe2889d8b0627c72be5d6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1146960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00067d3ac59b152349cce2ee62d1d1fc80d424366cca0741b5130316ec1f36f0`

```dockerfile
```

-	Layers:
	-	`sha256:ae9d5119dea6d9d8dc370f0197b7815e7ea4eab7a50e3962df4ff7507b5ec15b`  
		Last Modified: Tue, 19 Aug 2025 18:10:39 GMT  
		Size: 1.1 MB (1131697 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2678129d408de246508eace01dabc93d4762f22a4bce5468f32eb78e3c0d9cf4`  
		Last Modified: Tue, 19 Aug 2025 18:10:40 GMT  
		Size: 15.3 KB (15263 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.35-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:236e9d66b8103bd93e3872764468db2ac263c373b260498613a72d79b42e7f58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.6 MB (78624875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f602f26ba2bca549d1b9b7ae0a9904b7bb21d6746ba5781c2e0a9a6e6aea23ae`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 19 Aug 2025 08:40:07 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
ENV TELEGRAF_VERSION=1.35.4
# Tue, 19 Aug 2025 08:40:07 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 19 Aug 2025 08:40:07 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Aug 2025 08:40:07 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb9ba851c3cc6f6a60e1f54d90b4a3e0088e3e71c1361234db72c0e681312948`  
		Last Modified: Tue, 19 Aug 2025 17:00:42 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c4ac1b57267caa5ade49b9cf526c34877421ccf3ab657266741789a47db05a4`  
		Last Modified: Tue, 19 Aug 2025 17:00:42 GMT  
		Size: 2.6 MB (2616107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6254a8553d06cd74dd83678e67660d16a33aafe7a727405a4a8950db4c073a8`  
		Last Modified: Tue, 19 Aug 2025 17:00:55 GMT  
		Size: 71.9 MB (71877119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dcbf034e9f0cedd31ed4f69e865f928e913e9e964d333ea83a0e38eab973e42`  
		Last Modified: Tue, 19 Aug 2025 17:00:42 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:c7e18faf8edc102ce2aed72cca6a6ede5f0e92daa3e47336568447b0b82b2a78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1142721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96f034d01f06a7ef20999ff7fac16427ff60c143a68c0c7cd7ce2d43a9eeeffd`

```dockerfile
```

-	Layers:
	-	`sha256:b879ba997169df517ba2e5569a8fcd1783cfdde33a4b2a993479bdf25aeac651`  
		Last Modified: Tue, 19 Aug 2025 18:10:44 GMT  
		Size: 1.1 MB (1127336 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2c8fbc4be53f9d0b83f8a5baee19ef6ea265b37202aba06848c4f081543b0b3`  
		Last Modified: Tue, 19 Aug 2025 18:10:45 GMT  
		Size: 15.4 KB (15385 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.35.4`

```console
$ docker pull telegraf@sha256:6a052a237e217637f0f2a17c82af8c08f254a5f753d4b16db05261530bb17a18
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.35.4` - linux; amd64

```console
$ docker pull telegraf@sha256:36d255dd9ae95d3e27b946eb1fe0b49fc2af2345008072da50014e4bcda242ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.0 MB (171022468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf0dc6c618d32f6cde59aec8a49d929007d42b66db90f523a03c87efb89da0ac`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
ENV TELEGRAF_VERSION=1.35.4
# Tue, 19 Aug 2025 08:40:07 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 19 Aug 2025 08:40:07 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Aug 2025 08:40:07 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:8fb375ec14f3df8b31b70d0216508565ab7264a7e16cac4f8cc07f8eca22445f`  
		Last Modified: Mon, 08 Sep 2025 21:12:37 GMT  
		Size: 48.5 MB (48480610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccbbb2080a06a2888e44131965340c1eccd23f4d49efe72176246649abfbf9d9`  
		Last Modified: Mon, 08 Sep 2025 21:54:14 GMT  
		Size: 24.0 MB (24025996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93f0e44eea62b373168e2637ef3acd7d9c0cdc1f54e46dbba237c53ffe1a6677`  
		Last Modified: Mon, 08 Sep 2025 23:07:11 GMT  
		Size: 18.9 MB (18942775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0b8e00afe64f97c33175f8fd3049909003fc239302631480338eada1d36e866`  
		Last Modified: Mon, 08 Sep 2025 22:38:28 GMT  
		Size: 1.8 KB (1772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28e040dee2cd7e3fe769dbf2c2d7354e6001775cbf76d3ecaba320d245a47391`  
		Last Modified: Mon, 08 Sep 2025 23:07:23 GMT  
		Size: 79.6 MB (79570693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44d38927b48db8048f0c4e35f6b04babcf2270a93ac7b3123fa1e51a3049676e`  
		Last Modified: Mon, 08 Sep 2025 22:38:32 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35.4` - unknown; unknown

```console
$ docker pull telegraf@sha256:9b16d545ae6013b56868cd457f45e3f0307b650a64427869a8ce59884cd01193
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6660020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bfa191c748905e60046920fe24441aacd2d46d7291b6276e72faa1e69a835fe`

```dockerfile
```

-	Layers:
	-	`sha256:986b097123cd85a28ac5c30b5895d3005769d9941e963c1b1ee283e5d579f842`  
		Last Modified: Tue, 09 Sep 2025 00:10:26 GMT  
		Size: 6.6 MB (6645248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3460e2249de1c5dc714828e70f912f1132d32b07cab2fd1c11853efa3ace949b`  
		Last Modified: Tue, 09 Sep 2025 00:10:27 GMT  
		Size: 14.8 KB (14772 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.35.4` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:73251f8e80ba2a176904f1014f141848212f993a3181dbfbfa702a3f58561068
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.1 MB (157142865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80ed48bde4daddea121bad996029829e89fd7c46d345ec36a42ac3d83b2c6204`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1757289600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Sep 2025 21:35:06 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Sep 2025 21:35:06 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 08 Sep 2025 21:35:06 GMT
ENV TELEGRAF_VERSION=1.35.4
# Mon, 08 Sep 2025 21:35:06 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 08 Sep 2025 21:35:06 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 08 Sep 2025 21:35:06 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 08 Sep 2025 21:35:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Sep 2025 21:35:06 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:66de9a3b6b96c15de3235377e1618295643161d16058e17bde51f54951c6ec21`  
		Last Modified: Mon, 08 Sep 2025 21:14:33 GMT  
		Size: 44.2 MB (44195998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0efd1e8889a5c39ed7ad3628cf08e3daff474f9ff5b33972b323c79f306440f8`  
		Last Modified: Mon, 08 Sep 2025 23:37:54 GMT  
		Size: 21.9 MB (21931079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f80a54b7f01bb44d60641a76d77f5c6f5ffef4675de6dd1e1907d53a015a701`  
		Last Modified: Tue, 09 Sep 2025 06:16:09 GMT  
		Size: 17.7 MB (17722675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf9748a0def3f6fc0246ff5eb830a45c4fd8b6f151645e505888c42dc00e025c`  
		Last Modified: Tue, 09 Sep 2025 04:16:57 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9911e37b7fced99e41e1cb55198ed88a3c2de39ad5bdf8ac99c153f634b9eea2`  
		Last Modified: Tue, 09 Sep 2025 06:16:14 GMT  
		Size: 73.3 MB (73290717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1179e6bedb78b31947328fd7aa31e009cfa13536a9f7643581e9406787eb503a`  
		Last Modified: Tue, 09 Sep 2025 04:16:52 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35.4` - unknown; unknown

```console
$ docker pull telegraf@sha256:e3c70aff846f07811a97e1cec87441063c5d9c8a0f8814000260fb77d28e129d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6654103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b7afb311271f05ea122c1692b882428ad874947d2efb60c37d48ecfefef0e91`

```dockerfile
```

-	Layers:
	-	`sha256:b56d101f4fb860a115d90967f223dd19049d51333ea7e6762171ae57b5a3e406`  
		Last Modified: Tue, 09 Sep 2025 06:10:33 GMT  
		Size: 6.6 MB (6639543 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40244ab12e75c0f773558aaa32db9b48ec4cd5cd5e88c4cd06268cafb8aadadb`  
		Last Modified: Tue, 09 Sep 2025 06:10:34 GMT  
		Size: 14.6 KB (14560 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.35.4` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:beda89f31055dacaa4aab8af2f661e7101c079fb49011c51a01b8ce2ccd26cf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.9 MB (162919482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a23c1ed157cc6c6c2c8d54f7a3273716665e6ee465f9df914d2b42cc998a3e99`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1757289600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Sep 2025 21:35:06 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Sep 2025 21:35:06 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 08 Sep 2025 21:35:06 GMT
ENV TELEGRAF_VERSION=1.35.4
# Mon, 08 Sep 2025 21:35:06 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 08 Sep 2025 21:35:06 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 08 Sep 2025 21:35:06 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 08 Sep 2025 21:35:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Sep 2025 21:35:06 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:a9331b686701a987bcd276cc69a0f676d471ccda1aa353d2f7fad017f2894cd0`  
		Last Modified: Mon, 08 Sep 2025 21:14:32 GMT  
		Size: 48.4 MB (48359019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e108925666d6d84c8fa32751877e66a295ad55c9fbd10142325b99d60e786e17`  
		Last Modified: Mon, 08 Sep 2025 22:21:46 GMT  
		Size: 23.6 MB (23594789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a26e220328f978177fc338e1213ed5da76b98168101ff01a34a0ee25977092a`  
		Last Modified: Tue, 09 Sep 2025 03:16:07 GMT  
		Size: 18.9 MB (18883991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a48fcfc61f533fef671c379efbc2af295fd7f0cfcca748a87b2359f17726f618`  
		Last Modified: Tue, 09 Sep 2025 02:21:43 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6f4f905731802674abda750b5c62c670905e230428f8e5982dc9c3d845517a2`  
		Last Modified: Tue, 09 Sep 2025 03:16:12 GMT  
		Size: 72.1 MB (72079289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbe1d30585ad2b6e481fa11dd96b53146aea79dcfc04bf012bc2b4496e85199c`  
		Last Modified: Tue, 09 Sep 2025 02:21:44 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35.4` - unknown; unknown

```console
$ docker pull telegraf@sha256:6f8dd0fa2aa72d4a4e6d9ad6c37da014271a40561e17f35eb639eba75e9a4c99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6660201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f986f48b37a0733a178ab12258ce2ef091d2aa0640647387f1bb32a0c139fb77`

```dockerfile
```

-	Layers:
	-	`sha256:dcecae63d898843bb4ecccab3750c6292fe0139bda17df6f9802a3f0dd351787`  
		Last Modified: Tue, 09 Sep 2025 03:10:35 GMT  
		Size: 6.6 MB (6645622 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe13d7882936c8c492bb0d8e1c3b2d0de424aba262b478f8632f03180db4c51f`  
		Last Modified: Tue, 09 Sep 2025 03:10:36 GMT  
		Size: 14.6 KB (14579 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.35.4-alpine`

```console
$ docker pull telegraf@sha256:c2f97b178be0d6da47934693aab5f12968d4c357067466b00750d7c883c7ca5d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.35.4-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:b9f1dad8bfc6e2e0a071ec3708f69b608314a1638df1a27dbee6c8d9c201157d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.7 MB (85721229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1898bfc2837a825d9ca57c11162f841378cca6e17895db8ff8007425b40ae030`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 19 Aug 2025 08:40:07 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
ENV TELEGRAF_VERSION=1.35.4
# Tue, 19 Aug 2025 08:40:07 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 19 Aug 2025 08:40:07 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Aug 2025 08:40:07 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:111a65e71ad846fe6bc5cf5d9981577f402356a07fa8643556a52a493832248d`  
		Last Modified: Tue, 19 Aug 2025 16:43:11 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30cbaff1778259b3073527b025ae9ab08156e23a8b7f42fbbc0fafca178fc2a4`  
		Last Modified: Tue, 19 Aug 2025 16:43:11 GMT  
		Size: 2.6 MB (2552105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e527cfac45a96a64d7cc6821810e5660eec3f9f105ee9595ff5d0ef9ce3889e5`  
		Last Modified: Tue, 19 Aug 2025 16:43:18 GMT  
		Size: 79.4 MB (79368534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:701fb22e4edb908e9c9db1946c3275c80eb50f1b6a4a0a263e2bcc780d2db6cb`  
		Last Modified: Tue, 19 Aug 2025 16:43:13 GMT  
		Size: 621.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35.4-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:d62ff060ab03e0e18dd18b68bef85d0e6253116947fe2889d8b0627c72be5d6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1146960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00067d3ac59b152349cce2ee62d1d1fc80d424366cca0741b5130316ec1f36f0`

```dockerfile
```

-	Layers:
	-	`sha256:ae9d5119dea6d9d8dc370f0197b7815e7ea4eab7a50e3962df4ff7507b5ec15b`  
		Last Modified: Tue, 19 Aug 2025 18:10:39 GMT  
		Size: 1.1 MB (1131697 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2678129d408de246508eace01dabc93d4762f22a4bce5468f32eb78e3c0d9cf4`  
		Last Modified: Tue, 19 Aug 2025 18:10:40 GMT  
		Size: 15.3 KB (15263 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.35.4-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:236e9d66b8103bd93e3872764468db2ac263c373b260498613a72d79b42e7f58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.6 MB (78624875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f602f26ba2bca549d1b9b7ae0a9904b7bb21d6746ba5781c2e0a9a6e6aea23ae`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 19 Aug 2025 08:40:07 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
ENV TELEGRAF_VERSION=1.35.4
# Tue, 19 Aug 2025 08:40:07 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 19 Aug 2025 08:40:07 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Aug 2025 08:40:07 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb9ba851c3cc6f6a60e1f54d90b4a3e0088e3e71c1361234db72c0e681312948`  
		Last Modified: Tue, 19 Aug 2025 17:00:42 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c4ac1b57267caa5ade49b9cf526c34877421ccf3ab657266741789a47db05a4`  
		Last Modified: Tue, 19 Aug 2025 17:00:42 GMT  
		Size: 2.6 MB (2616107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6254a8553d06cd74dd83678e67660d16a33aafe7a727405a4a8950db4c073a8`  
		Last Modified: Tue, 19 Aug 2025 17:00:55 GMT  
		Size: 71.9 MB (71877119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dcbf034e9f0cedd31ed4f69e865f928e913e9e964d333ea83a0e38eab973e42`  
		Last Modified: Tue, 19 Aug 2025 17:00:42 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35.4-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:c7e18faf8edc102ce2aed72cca6a6ede5f0e92daa3e47336568447b0b82b2a78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1142721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96f034d01f06a7ef20999ff7fac16427ff60c143a68c0c7cd7ce2d43a9eeeffd`

```dockerfile
```

-	Layers:
	-	`sha256:b879ba997169df517ba2e5569a8fcd1783cfdde33a4b2a993479bdf25aeac651`  
		Last Modified: Tue, 19 Aug 2025 18:10:44 GMT  
		Size: 1.1 MB (1127336 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2c8fbc4be53f9d0b83f8a5baee19ef6ea265b37202aba06848c4f081543b0b3`  
		Last Modified: Tue, 19 Aug 2025 18:10:45 GMT  
		Size: 15.4 KB (15385 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.36`

```console
$ docker pull telegraf@sha256:bfe0a116f05de4257c071e2b912b8835f4f894e5009324a8e881dbc1c257af10
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
$ docker pull telegraf@sha256:fd45e1d1713e1f4a189f58adb0e3bb990388054a8c05b8b7bd40265a3ba8b0d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.2 MB (171242086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5391e161b50cabc3a294af8f066a133637ba3c5952a29044e00ab536f737ddcc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Sep 2025 21:35:06 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Sep 2025 21:35:06 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 08 Sep 2025 21:35:06 GMT
ENV TELEGRAF_VERSION=1.36.0
# Mon, 08 Sep 2025 21:35:06 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 08 Sep 2025 21:35:06 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 08 Sep 2025 21:35:06 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 08 Sep 2025 21:35:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Sep 2025 21:35:06 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:8fb375ec14f3df8b31b70d0216508565ab7264a7e16cac4f8cc07f8eca22445f`  
		Last Modified: Mon, 08 Sep 2025 21:12:37 GMT  
		Size: 48.5 MB (48480610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccbbb2080a06a2888e44131965340c1eccd23f4d49efe72176246649abfbf9d9`  
		Last Modified: Mon, 08 Sep 2025 21:54:14 GMT  
		Size: 24.0 MB (24025996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57c2ee446e0b5bbdfe651f8e8a947c6da99475770aacba32d83156a92dc224bd`  
		Last Modified: Tue, 09 Sep 2025 00:10:46 GMT  
		Size: 18.9 MB (18942743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6485ea33a36258d7f06e4548b5e7c0dc7cb4517f659c372057cafb5977ce27c6`  
		Last Modified: Mon, 08 Sep 2025 23:21:28 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78d02dfb1e8e097b292ae6245bd5355535dc759bf8e6915d003bf63ae4bc3514`  
		Last Modified: Tue, 09 Sep 2025 00:10:50 GMT  
		Size: 79.8 MB (79790329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ef7eff07ccf38016fce817cbf6236870952ff975e62a5ea2a252b52aa6246b5`  
		Last Modified: Mon, 08 Sep 2025 23:21:32 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36` - unknown; unknown

```console
$ docker pull telegraf@sha256:480803422cc9df0d8ae0b64688b0cd583a2ca70c5149cd11ffb7391cfdf4dbfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6661776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f989ee600ffa69e8527cfc3b08477f5df6877e6fa6ada1ba85cfc676a34fc97`

```dockerfile
```

-	Layers:
	-	`sha256:38f8df255fc19c30a1b2c093d0871e3e8d49ba059cbb35f851f699685ca9de65`  
		Last Modified: Tue, 09 Sep 2025 00:10:35 GMT  
		Size: 6.6 MB (6647004 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2f24b7f6bdd42b8290ccd785bda01ec46b8535fcefa59c9347cdf7e030a1fa5`  
		Last Modified: Tue, 09 Sep 2025 00:10:36 GMT  
		Size: 14.8 KB (14772 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.36` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:6f1e156f9ba35b0c4fbfc560e1d1a970018ad55136b70fca3b93a1f22cb00901
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.2 MB (157245348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e523b7d1d3f47e63da901c640e5a2a21e815c8ca0a3ba25e019066150c1ef664`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1757289600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Sep 2025 21:35:06 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Sep 2025 21:35:06 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 08 Sep 2025 21:35:06 GMT
ENV TELEGRAF_VERSION=1.36.0
# Mon, 08 Sep 2025 21:35:06 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 08 Sep 2025 21:35:06 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 08 Sep 2025 21:35:06 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 08 Sep 2025 21:35:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Sep 2025 21:35:06 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:66de9a3b6b96c15de3235377e1618295643161d16058e17bde51f54951c6ec21`  
		Last Modified: Mon, 08 Sep 2025 21:14:33 GMT  
		Size: 44.2 MB (44195998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0efd1e8889a5c39ed7ad3628cf08e3daff474f9ff5b33972b323c79f306440f8`  
		Last Modified: Mon, 08 Sep 2025 23:37:54 GMT  
		Size: 21.9 MB (21931079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cf37909f7ac4e3f15c2c7ecacc16fa58ef82d28624bff9276a057663fd0976d`  
		Last Modified: Tue, 09 Sep 2025 04:48:49 GMT  
		Size: 17.7 MB (17722690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:357da611076f9bea097256a99992d403698e61db6ab4457d659bac12e58128f0`  
		Last Modified: Tue, 09 Sep 2025 04:17:08 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bb0d2a9d377a19d06964706a4d17bfdbe89817368efd35ab26f960e67f074b5`  
		Last Modified: Tue, 09 Sep 2025 06:16:26 GMT  
		Size: 73.4 MB (73393187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:925b60c2429fcfe053fa357672b92a9ef0312eadb39ee79a57fc1501dcb0c40f`  
		Last Modified: Tue, 09 Sep 2025 04:17:08 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36` - unknown; unknown

```console
$ docker pull telegraf@sha256:a89b5bb15ca9c81b168f04f65af123d104dc9de7f03cc75cbe8c4ff7f2b899aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6656478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cebf7d439bea332dc983877d0abdf722422cc2df7f14341b438b18e2b10a0d4e`

```dockerfile
```

-	Layers:
	-	`sha256:3a12b16a293fe0fb5be1024302575a94f36f668b77c1418e7578245d7182a783`  
		Last Modified: Tue, 09 Sep 2025 06:10:40 GMT  
		Size: 6.6 MB (6641609 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0287306c6a36fa7761e95df155193fee70867cdd779051d5c3be3d47c8341727`  
		Last Modified: Tue, 09 Sep 2025 06:10:41 GMT  
		Size: 14.9 KB (14869 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.36` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:0523d06ce0843d29e2d8f224e3d38267b5ccda09e195d42c9890701908059e0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.1 MB (162052135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b3827a84def9d7d257577bbada5dcee1dd5664e11852964e902245fe27f1296`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1757289600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Sep 2025 21:35:06 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Sep 2025 21:35:06 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 08 Sep 2025 21:35:06 GMT
ENV TELEGRAF_VERSION=1.36.0
# Mon, 08 Sep 2025 21:35:06 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 08 Sep 2025 21:35:06 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 08 Sep 2025 21:35:06 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 08 Sep 2025 21:35:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Sep 2025 21:35:06 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:a9331b686701a987bcd276cc69a0f676d471ccda1aa353d2f7fad017f2894cd0`  
		Last Modified: Mon, 08 Sep 2025 21:14:32 GMT  
		Size: 48.4 MB (48359019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e108925666d6d84c8fa32751877e66a295ad55c9fbd10142325b99d60e786e17`  
		Last Modified: Mon, 08 Sep 2025 22:21:46 GMT  
		Size: 23.6 MB (23594789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6164fcfed84e1c4e85e432856b2a87eb600a74e1a3593495b5cbf37306be6b68`  
		Last Modified: Tue, 09 Sep 2025 02:30:08 GMT  
		Size: 18.9 MB (18884019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad5c0bc84f09aa9905cb1e2686725a41008b57dcb1f04d9981c6f9cdbc303b0c`  
		Last Modified: Tue, 09 Sep 2025 02:23:20 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5c9ec34b7c0601f78e378ca8a39adc94ebe24a8e60614e5dd4f97a6bda21dea`  
		Last Modified: Tue, 09 Sep 2025 02:30:11 GMT  
		Size: 71.2 MB (71211897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7fea26294569d3d04727fc0f8cd7c42b978e0825eb40ef965d5857a8ea2a95c`  
		Last Modified: Tue, 09 Sep 2025 02:23:19 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36` - unknown; unknown

```console
$ docker pull telegraf@sha256:7a45a99cf5874d166b9ffc8252efde13f233b125256b1babc5021cb71ce17e4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6662586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f291bc4a2338b84d5cf160df7fd0506ceee989b28d30b8a98915440f84082f0`

```dockerfile
```

-	Layers:
	-	`sha256:517b563a6a20b522f8a3d37cebf314584cbdaca4610189cea638097a7a77c536`  
		Last Modified: Tue, 09 Sep 2025 03:10:38 GMT  
		Size: 6.6 MB (6647692 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56ccb47971f161945c59e8d2260543720693ce1e3e401d200dfdc78ebde51e7b`  
		Last Modified: Tue, 09 Sep 2025 03:10:39 GMT  
		Size: 14.9 KB (14894 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.36-alpine`

```console
$ docker pull telegraf@sha256:309a6af7fbee5c03de8ab69d05940286508761840013b742f0adc0f6d7159298
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.36-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:8e1002f94b5bf2486eb0c2e12b20c486ad97242d0c9efdab031078f50873caf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.9 MB (85939575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0308cea28713e4d54bcac49e9c35389c5c595b84e7d28071ac8e959398cbeb42`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Mon, 08 Sep 2025 21:35:06 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 08 Sep 2025 21:35:06 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 08 Sep 2025 21:35:06 GMT
ENV TELEGRAF_VERSION=1.36.0
# Mon, 08 Sep 2025 21:35:06 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 08 Sep 2025 21:35:06 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 08 Sep 2025 21:35:06 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 08 Sep 2025 21:35:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Sep 2025 21:35:06 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f57f7bea3083dc00c76d66d744c2500e9fdf264ca4e1a1d29c6c7f178e411a2e`  
		Last Modified: Mon, 08 Sep 2025 23:21:33 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a3bd815d0677ace72391844908df3b201322b73d9694ba91e4610e608bc52f`  
		Last Modified: Mon, 08 Sep 2025 23:21:37 GMT  
		Size: 2.6 MB (2552123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92e1b056e56e5538f0d791dd5a49cbf726fd923ac5f48ee7c6f8509f52dd73c9`  
		Last Modified: Tue, 09 Sep 2025 00:10:47 GMT  
		Size: 79.6 MB (79586863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f74e8bcadda67067b6ecfb128a06abe5e7de1b76679d4bfceb4b7e2e7fccd747`  
		Last Modified: Mon, 08 Sep 2025 23:21:49 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:6399707b3929497ea018417bf956e57cb35a8d72248dd5d93ddc24e7cd19e619
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1148716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd53a2646b2e7925055335cef6a55679ceb685b2104c4ebfce8810a9471af8f2`

```dockerfile
```

-	Layers:
	-	`sha256:b5ea504d9dfbee3c00456cf096612397252ba9def59f6242ace0b1e792367c1c`  
		Last Modified: Tue, 09 Sep 2025 00:10:40 GMT  
		Size: 1.1 MB (1133453 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e805f3d9087c9590961bf99f832797e344abf05a8297cccef1e4c60f59ac8181`  
		Last Modified: Tue, 09 Sep 2025 00:10:41 GMT  
		Size: 15.3 KB (15263 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.36-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:f10e3fe8ad1ce17160f453a703ae0d3eb296220785a657d5cff2d1a2e0a1d140
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.8 MB (77757782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59e3e3ad5b1945cd00029702277041b9c1c551f2f3c40e7857130c47c284a70b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Mon, 08 Sep 2025 21:35:06 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 08 Sep 2025 21:35:06 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 08 Sep 2025 21:35:06 GMT
ENV TELEGRAF_VERSION=1.36.0
# Mon, 08 Sep 2025 21:35:06 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 08 Sep 2025 21:35:06 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 08 Sep 2025 21:35:06 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 08 Sep 2025 21:35:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Sep 2025 21:35:06 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbc5c960edda77fbca70b29eb5bbc0fceabcc14588573a30b8be258805108389`  
		Last Modified: Tue, 09 Sep 2025 02:21:40 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21710032ff03b3b3a23a0ed25ea0ad22a86f51072fcce5fe7c7a5a9b933fccbe`  
		Last Modified: Tue, 09 Sep 2025 02:21:41 GMT  
		Size: 2.6 MB (2616143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb441015907d0eee5dab2f305a8e36d1ce9cbd5f68a74af796feca4daf289b76`  
		Last Modified: Tue, 09 Sep 2025 02:26:39 GMT  
		Size: 71.0 MB (71009992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92272ac37f13f80377406c538edb16c6614adac9c464532143d667f9b12c5b4a`  
		Last Modified: Tue, 09 Sep 2025 02:21:40 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:e0bfec97eca1cc2c601c9ce04bd507b46e2b71163a2a87434d95798d3ebca4fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1144475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4162b0ea20e6692a56536c1906e3e60393ef1788128e542779c870b7bf3b60f7`

```dockerfile
```

-	Layers:
	-	`sha256:00bd71b5bfaa5b0795ee551bbca330dfa36157112f91dacc6864e0437a200aeb`  
		Last Modified: Tue, 09 Sep 2025 03:10:41 GMT  
		Size: 1.1 MB (1129092 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:553a060fdf37c5d8c8760a06af1becba12d2745e03cb22cdcfade81a4f7c9271`  
		Last Modified: Tue, 09 Sep 2025 03:10:42 GMT  
		Size: 15.4 KB (15383 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.36.1`

**does not exist** (yet?)

## `telegraf:1.36.1-alpine`

**does not exist** (yet?)

## `telegraf:alpine`

```console
$ docker pull telegraf@sha256:309a6af7fbee5c03de8ab69d05940286508761840013b742f0adc0f6d7159298
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:8e1002f94b5bf2486eb0c2e12b20c486ad97242d0c9efdab031078f50873caf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.9 MB (85939575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0308cea28713e4d54bcac49e9c35389c5c595b84e7d28071ac8e959398cbeb42`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Mon, 08 Sep 2025 21:35:06 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 08 Sep 2025 21:35:06 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 08 Sep 2025 21:35:06 GMT
ENV TELEGRAF_VERSION=1.36.0
# Mon, 08 Sep 2025 21:35:06 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 08 Sep 2025 21:35:06 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 08 Sep 2025 21:35:06 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 08 Sep 2025 21:35:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Sep 2025 21:35:06 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f57f7bea3083dc00c76d66d744c2500e9fdf264ca4e1a1d29c6c7f178e411a2e`  
		Last Modified: Mon, 08 Sep 2025 23:21:33 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a3bd815d0677ace72391844908df3b201322b73d9694ba91e4610e608bc52f`  
		Last Modified: Mon, 08 Sep 2025 23:21:37 GMT  
		Size: 2.6 MB (2552123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92e1b056e56e5538f0d791dd5a49cbf726fd923ac5f48ee7c6f8509f52dd73c9`  
		Last Modified: Tue, 09 Sep 2025 00:10:47 GMT  
		Size: 79.6 MB (79586863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f74e8bcadda67067b6ecfb128a06abe5e7de1b76679d4bfceb4b7e2e7fccd747`  
		Last Modified: Mon, 08 Sep 2025 23:21:49 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:6399707b3929497ea018417bf956e57cb35a8d72248dd5d93ddc24e7cd19e619
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1148716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd53a2646b2e7925055335cef6a55679ceb685b2104c4ebfce8810a9471af8f2`

```dockerfile
```

-	Layers:
	-	`sha256:b5ea504d9dfbee3c00456cf096612397252ba9def59f6242ace0b1e792367c1c`  
		Last Modified: Tue, 09 Sep 2025 00:10:40 GMT  
		Size: 1.1 MB (1133453 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e805f3d9087c9590961bf99f832797e344abf05a8297cccef1e4c60f59ac8181`  
		Last Modified: Tue, 09 Sep 2025 00:10:41 GMT  
		Size: 15.3 KB (15263 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:f10e3fe8ad1ce17160f453a703ae0d3eb296220785a657d5cff2d1a2e0a1d140
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.8 MB (77757782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59e3e3ad5b1945cd00029702277041b9c1c551f2f3c40e7857130c47c284a70b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Mon, 08 Sep 2025 21:35:06 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 08 Sep 2025 21:35:06 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 08 Sep 2025 21:35:06 GMT
ENV TELEGRAF_VERSION=1.36.0
# Mon, 08 Sep 2025 21:35:06 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 08 Sep 2025 21:35:06 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 08 Sep 2025 21:35:06 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 08 Sep 2025 21:35:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Sep 2025 21:35:06 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbc5c960edda77fbca70b29eb5bbc0fceabcc14588573a30b8be258805108389`  
		Last Modified: Tue, 09 Sep 2025 02:21:40 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21710032ff03b3b3a23a0ed25ea0ad22a86f51072fcce5fe7c7a5a9b933fccbe`  
		Last Modified: Tue, 09 Sep 2025 02:21:41 GMT  
		Size: 2.6 MB (2616143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb441015907d0eee5dab2f305a8e36d1ce9cbd5f68a74af796feca4daf289b76`  
		Last Modified: Tue, 09 Sep 2025 02:26:39 GMT  
		Size: 71.0 MB (71009992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92272ac37f13f80377406c538edb16c6614adac9c464532143d667f9b12c5b4a`  
		Last Modified: Tue, 09 Sep 2025 02:21:40 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:e0bfec97eca1cc2c601c9ce04bd507b46e2b71163a2a87434d95798d3ebca4fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1144475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4162b0ea20e6692a56536c1906e3e60393ef1788128e542779c870b7bf3b60f7`

```dockerfile
```

-	Layers:
	-	`sha256:00bd71b5bfaa5b0795ee551bbca330dfa36157112f91dacc6864e0437a200aeb`  
		Last Modified: Tue, 09 Sep 2025 03:10:41 GMT  
		Size: 1.1 MB (1129092 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:553a060fdf37c5d8c8760a06af1becba12d2745e03cb22cdcfade81a4f7c9271`  
		Last Modified: Tue, 09 Sep 2025 03:10:42 GMT  
		Size: 15.4 KB (15383 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:latest`

```console
$ docker pull telegraf@sha256:bfe0a116f05de4257c071e2b912b8835f4f894e5009324a8e881dbc1c257af10
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
$ docker pull telegraf@sha256:fd45e1d1713e1f4a189f58adb0e3bb990388054a8c05b8b7bd40265a3ba8b0d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.2 MB (171242086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5391e161b50cabc3a294af8f066a133637ba3c5952a29044e00ab536f737ddcc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Sep 2025 21:35:06 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Sep 2025 21:35:06 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 08 Sep 2025 21:35:06 GMT
ENV TELEGRAF_VERSION=1.36.0
# Mon, 08 Sep 2025 21:35:06 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 08 Sep 2025 21:35:06 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 08 Sep 2025 21:35:06 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 08 Sep 2025 21:35:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Sep 2025 21:35:06 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:8fb375ec14f3df8b31b70d0216508565ab7264a7e16cac4f8cc07f8eca22445f`  
		Last Modified: Mon, 08 Sep 2025 21:12:37 GMT  
		Size: 48.5 MB (48480610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccbbb2080a06a2888e44131965340c1eccd23f4d49efe72176246649abfbf9d9`  
		Last Modified: Mon, 08 Sep 2025 21:54:14 GMT  
		Size: 24.0 MB (24025996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57c2ee446e0b5bbdfe651f8e8a947c6da99475770aacba32d83156a92dc224bd`  
		Last Modified: Tue, 09 Sep 2025 00:10:46 GMT  
		Size: 18.9 MB (18942743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6485ea33a36258d7f06e4548b5e7c0dc7cb4517f659c372057cafb5977ce27c6`  
		Last Modified: Mon, 08 Sep 2025 23:21:28 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78d02dfb1e8e097b292ae6245bd5355535dc759bf8e6915d003bf63ae4bc3514`  
		Last Modified: Tue, 09 Sep 2025 00:10:50 GMT  
		Size: 79.8 MB (79790329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ef7eff07ccf38016fce817cbf6236870952ff975e62a5ea2a252b52aa6246b5`  
		Last Modified: Mon, 08 Sep 2025 23:21:32 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:480803422cc9df0d8ae0b64688b0cd583a2ca70c5149cd11ffb7391cfdf4dbfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6661776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f989ee600ffa69e8527cfc3b08477f5df6877e6fa6ada1ba85cfc676a34fc97`

```dockerfile
```

-	Layers:
	-	`sha256:38f8df255fc19c30a1b2c093d0871e3e8d49ba059cbb35f851f699685ca9de65`  
		Last Modified: Tue, 09 Sep 2025 00:10:35 GMT  
		Size: 6.6 MB (6647004 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2f24b7f6bdd42b8290ccd785bda01ec46b8535fcefa59c9347cdf7e030a1fa5`  
		Last Modified: Tue, 09 Sep 2025 00:10:36 GMT  
		Size: 14.8 KB (14772 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:6f1e156f9ba35b0c4fbfc560e1d1a970018ad55136b70fca3b93a1f22cb00901
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.2 MB (157245348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e523b7d1d3f47e63da901c640e5a2a21e815c8ca0a3ba25e019066150c1ef664`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1757289600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Sep 2025 21:35:06 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Sep 2025 21:35:06 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 08 Sep 2025 21:35:06 GMT
ENV TELEGRAF_VERSION=1.36.0
# Mon, 08 Sep 2025 21:35:06 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 08 Sep 2025 21:35:06 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 08 Sep 2025 21:35:06 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 08 Sep 2025 21:35:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Sep 2025 21:35:06 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:66de9a3b6b96c15de3235377e1618295643161d16058e17bde51f54951c6ec21`  
		Last Modified: Mon, 08 Sep 2025 21:14:33 GMT  
		Size: 44.2 MB (44195998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0efd1e8889a5c39ed7ad3628cf08e3daff474f9ff5b33972b323c79f306440f8`  
		Last Modified: Mon, 08 Sep 2025 23:37:54 GMT  
		Size: 21.9 MB (21931079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cf37909f7ac4e3f15c2c7ecacc16fa58ef82d28624bff9276a057663fd0976d`  
		Last Modified: Tue, 09 Sep 2025 04:48:49 GMT  
		Size: 17.7 MB (17722690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:357da611076f9bea097256a99992d403698e61db6ab4457d659bac12e58128f0`  
		Last Modified: Tue, 09 Sep 2025 04:17:08 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bb0d2a9d377a19d06964706a4d17bfdbe89817368efd35ab26f960e67f074b5`  
		Last Modified: Tue, 09 Sep 2025 06:16:26 GMT  
		Size: 73.4 MB (73393187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:925b60c2429fcfe053fa357672b92a9ef0312eadb39ee79a57fc1501dcb0c40f`  
		Last Modified: Tue, 09 Sep 2025 04:17:08 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:a89b5bb15ca9c81b168f04f65af123d104dc9de7f03cc75cbe8c4ff7f2b899aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6656478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cebf7d439bea332dc983877d0abdf722422cc2df7f14341b438b18e2b10a0d4e`

```dockerfile
```

-	Layers:
	-	`sha256:3a12b16a293fe0fb5be1024302575a94f36f668b77c1418e7578245d7182a783`  
		Last Modified: Tue, 09 Sep 2025 06:10:40 GMT  
		Size: 6.6 MB (6641609 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0287306c6a36fa7761e95df155193fee70867cdd779051d5c3be3d47c8341727`  
		Last Modified: Tue, 09 Sep 2025 06:10:41 GMT  
		Size: 14.9 KB (14869 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:0523d06ce0843d29e2d8f224e3d38267b5ccda09e195d42c9890701908059e0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.1 MB (162052135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b3827a84def9d7d257577bbada5dcee1dd5664e11852964e902245fe27f1296`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1757289600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Sep 2025 21:35:06 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Sep 2025 21:35:06 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 08 Sep 2025 21:35:06 GMT
ENV TELEGRAF_VERSION=1.36.0
# Mon, 08 Sep 2025 21:35:06 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 08 Sep 2025 21:35:06 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 08 Sep 2025 21:35:06 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 08 Sep 2025 21:35:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Sep 2025 21:35:06 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:a9331b686701a987bcd276cc69a0f676d471ccda1aa353d2f7fad017f2894cd0`  
		Last Modified: Mon, 08 Sep 2025 21:14:32 GMT  
		Size: 48.4 MB (48359019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e108925666d6d84c8fa32751877e66a295ad55c9fbd10142325b99d60e786e17`  
		Last Modified: Mon, 08 Sep 2025 22:21:46 GMT  
		Size: 23.6 MB (23594789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6164fcfed84e1c4e85e432856b2a87eb600a74e1a3593495b5cbf37306be6b68`  
		Last Modified: Tue, 09 Sep 2025 02:30:08 GMT  
		Size: 18.9 MB (18884019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad5c0bc84f09aa9905cb1e2686725a41008b57dcb1f04d9981c6f9cdbc303b0c`  
		Last Modified: Tue, 09 Sep 2025 02:23:20 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5c9ec34b7c0601f78e378ca8a39adc94ebe24a8e60614e5dd4f97a6bda21dea`  
		Last Modified: Tue, 09 Sep 2025 02:30:11 GMT  
		Size: 71.2 MB (71211897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7fea26294569d3d04727fc0f8cd7c42b978e0825eb40ef965d5857a8ea2a95c`  
		Last Modified: Tue, 09 Sep 2025 02:23:19 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:7a45a99cf5874d166b9ffc8252efde13f233b125256b1babc5021cb71ce17e4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6662586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f291bc4a2338b84d5cf160df7fd0506ceee989b28d30b8a98915440f84082f0`

```dockerfile
```

-	Layers:
	-	`sha256:517b563a6a20b522f8a3d37cebf314584cbdaca4610189cea638097a7a77c536`  
		Last Modified: Tue, 09 Sep 2025 03:10:38 GMT  
		Size: 6.6 MB (6647692 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56ccb47971f161945c59e8d2260543720693ce1e3e401d200dfdc78ebde51e7b`  
		Last Modified: Tue, 09 Sep 2025 03:10:39 GMT  
		Size: 14.9 KB (14894 bytes)  
		MIME: application/vnd.in-toto+json
