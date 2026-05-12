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
-	[`telegraf:1.38.4`](#telegraf1384)
-	[`telegraf:1.38.4-alpine`](#telegraf1384-alpine)
-	[`telegraf:alpine`](#telegrafalpine)
-	[`telegraf:latest`](#telegraflatest)

## `telegraf:1.36`

```console
$ docker pull telegraf@sha256:a8aa55493d7c2733bc38e32e67cbffc714747fff3f79a3c675960dc6d6470e22
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
$ docker pull telegraf@sha256:ed3cf13470ae3ef2c12b14d78646856557365b7d1e7752454af1f684c5a680d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.0 MB (171954575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54c5ac0f9bb269a82f6dc2b5857d9c02ef0cfb9a345820a400e3a3c6fca4023f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:40:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:40:24 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:40:25 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 08 May 2026 20:40:29 GMT
ENV TELEGRAF_VERSION=1.36.4
# Fri, 08 May 2026 20:40:29 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Fri, 08 May 2026 20:40:29 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Fri, 08 May 2026 20:40:29 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 08 May 2026 20:40:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 08 May 2026 20:40:29 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:9104793a826a01456b0ba567a92064e85a029816661fbb4524da7913f0123ab5`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 48.5 MB (48488676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d055cea50c88c57fc27fcd44845ebabfe5b830ea8a0a621b89d38a2b650b7ff3`  
		Last Modified: Fri, 08 May 2026 19:40:29 GMT  
		Size: 24.0 MB (24042180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a4154482c2eb44c183af49bf72c7aade026ba03f675b7956894c73917e4aeb`  
		Last Modified: Fri, 08 May 2026 20:40:49 GMT  
		Size: 18.9 MB (18944433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d89cea0c2d13f431cd03079dc8778aedad84e9961c3396ec4db39503ecddf1a`  
		Last Modified: Fri, 08 May 2026 20:40:48 GMT  
		Size: 5.1 KB (5071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23aa70749964761b5e0c0d61e55832cb1804b29ba5dfbe139b19d2e1ba6e57d5`  
		Last Modified: Fri, 08 May 2026 20:40:50 GMT  
		Size: 80.5 MB (80473590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5fa5cc78a5df08df1dce4d8f7f25b53a4c64859f9da8ef36d19103371b0f690`  
		Last Modified: Fri, 08 May 2026 20:40:48 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36` - unknown; unknown

```console
$ docker pull telegraf@sha256:64c4e5cb0dac9a65442494c0b0507e2bcb7b23042b15f970b0d78c36f19f3f6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6670530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:633c5743edfa0a08353249ff063b114102abdaf33858d291c74efad350bb4e40`

```dockerfile
```

-	Layers:
	-	`sha256:8ee2630cf664d7e5bbcb46d99bd3be74646ee9015d426a35f380660e65d1f652`  
		Last Modified: Fri, 08 May 2026 20:40:48 GMT  
		Size: 6.7 MB (6656103 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f537f6254b79fe1ff68887a92103907c6872c6153f6d8e5cf13ed9fdb50d82e8`  
		Last Modified: Fri, 08 May 2026 20:40:48 GMT  
		Size: 14.4 KB (14427 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.36` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:34c0671c4d8c1940e2543f9175b2cf11f48f36840fe0c184ade15f3c8f8370ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.8 MB (157823252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bcc7cf8844489079b979fb613faf7fd2dfae5387f668918f3fd5204613cbae4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:44:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 21:47:53 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 21:47:54 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 08 May 2026 21:47:59 GMT
ENV TELEGRAF_VERSION=1.36.4
# Fri, 08 May 2026 21:47:59 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Fri, 08 May 2026 21:47:59 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Fri, 08 May 2026 21:47:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 08 May 2026 21:47:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 08 May 2026 21:47:59 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:752ba895535a5b96e621b623e0a11ff696fe28fb2110ab16de49e150423d0a89`  
		Last Modified: Fri, 08 May 2026 18:36:54 GMT  
		Size: 44.2 MB (44207696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b0504388ca2bf72a5fec3556b58015e5dce736337a948976b22cd4cce283cb0`  
		Last Modified: Fri, 08 May 2026 19:44:39 GMT  
		Size: 21.9 MB (21946392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5a6ba2cc1567fd653f51e96d4ac12f7ca6b7b4aed30577e0c4e17b5d252c459`  
		Last Modified: Fri, 08 May 2026 21:48:17 GMT  
		Size: 17.7 MB (17699847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f595515517c5f1e3b043bd33128b620206d79f7f8d445d31885c2035300171f`  
		Last Modified: Fri, 08 May 2026 21:48:16 GMT  
		Size: 5.1 KB (5054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db06c86962c37657991405a7566ca3aaaa20cfae71d6bbc9aaa4625d998a0f5b`  
		Last Modified: Fri, 08 May 2026 21:48:19 GMT  
		Size: 74.0 MB (73963638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff99cf870fa6e3b09f8a7af079ab03e97538752436308543f499382d35201c37`  
		Last Modified: Fri, 08 May 2026 21:48:15 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36` - unknown; unknown

```console
$ docker pull telegraf@sha256:df6f7057da4f0c191da72e0255cdab577490836d3ca3e938c810092ec1d12ce7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6665217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfdeb95e713a082d9a4e436fb2a382c2a562287f38d94ca392af0659235421e9`

```dockerfile
```

-	Layers:
	-	`sha256:c2e22544e95b3cf25f1c3d8bb2b77d6f0190681387ab7c9c40bf4f7d0c3e297b`  
		Last Modified: Fri, 08 May 2026 21:48:16 GMT  
		Size: 6.7 MB (6650700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc864105f0e9e40932a5abb7480ea0ee04d904c3ccb28e7e66a16f16f7a33152`  
		Last Modified: Fri, 08 May 2026 21:48:16 GMT  
		Size: 14.5 KB (14517 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.36` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:e3c6383352b9eff01aef5ce42bc7a75a7dc3eb39cb93433d788ad224a1aeba21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.7 MB (162674309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b30d4ea88a7c369a56e845aa4fbbae03ced50ea8f6e650e65634301b5142490e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:42:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:45:29 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:45:30 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 08 May 2026 20:45:34 GMT
ENV TELEGRAF_VERSION=1.36.4
# Fri, 08 May 2026 20:45:34 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Fri, 08 May 2026 20:45:34 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Fri, 08 May 2026 20:45:34 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 08 May 2026 20:45:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 08 May 2026 20:45:34 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:8eda28c6ece628fdff982fd6c7c1cd1f5eeccc51cfd0a3ee9155b2ccbdcc68a3`  
		Last Modified: Fri, 08 May 2026 18:24:51 GMT  
		Size: 48.4 MB (48373150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19f56578c9577bd69a05b2319baacd770a986ae61a8568047ddd91db1a1893b4`  
		Last Modified: Fri, 08 May 2026 19:42:30 GMT  
		Size: 23.6 MB (23609357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7caea1cfc8e4f5cfda68032987e00be0f353a17dbe6ff2971a9512a9c750266d`  
		Last Modified: Fri, 08 May 2026 20:45:53 GMT  
		Size: 18.9 MB (18885802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e8debbb6c9b7777b0f748abdee1061b0ec3a8f9dcc95cd14696b4cbe8b39637`  
		Last Modified: Fri, 08 May 2026 20:45:52 GMT  
		Size: 5.1 KB (5058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b7137f098a0ecf2d12f5964d2084c1e0517316750c0408ef293073a06c5ede2`  
		Last Modified: Fri, 08 May 2026 20:45:54 GMT  
		Size: 71.8 MB (71800318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cbf371040d2851c8a9ac6d9957009d8250386ba6db397061643db722dd67637`  
		Last Modified: Fri, 08 May 2026 20:45:52 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36` - unknown; unknown

```console
$ docker pull telegraf@sha256:6a73b9e8bbe8c4b1157aa53bca20fcc150da562a81e700357177403faefe4044
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6671315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1279ff4f8fc251200ee06891b2342d3e249bf6c8148d61428c1ffcd7ef44039`

```dockerfile
```

-	Layers:
	-	`sha256:ee0041620fabf31680c2d497d4b774fecd02bba1f9fbf731a9855b19fec39af4`  
		Last Modified: Fri, 08 May 2026 20:45:52 GMT  
		Size: 6.7 MB (6656779 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1802f83be627dea6546d588b5683637af6956111542424c9fc73dbf6fef3ecc`  
		Last Modified: Fri, 08 May 2026 20:45:52 GMT  
		Size: 14.5 KB (14536 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.36-alpine`

```console
$ docker pull telegraf@sha256:03418f3e6c7395c6e5b14f9e057abe26024e4f6fa5b88fa6e6ab57ce6f8c7a5c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.36-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:e42e15e551b65fd997636e15e96974d57b54b60aacb82f56d596c5f7b42f84cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.6 MB (86647081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d9572dba87617bf4a6b1616002ce3bd493b7bf4f41c1ae10e9cd95c2188f117`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:35:14 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 17 Apr 2026 00:35:15 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Fri, 17 Apr 2026 00:35:24 GMT
ENV TELEGRAF_VERSION=1.36.4
# Fri, 17 Apr 2026 00:35:24 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Fri, 17 Apr 2026 00:35:24 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Fri, 17 Apr 2026 00:35:24 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 17 Apr 2026 00:35:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 17 Apr 2026 00:35:24 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad4d35ed9ce2a9043f49d4a2af780155068be3d64d1e73c46b02e5f5508ebd7d`  
		Last Modified: Fri, 17 Apr 2026 00:35:38 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5abe5b9b65035ba0c23da9d6a13f11d34e00c0c90f2f61fbfce2cdd6eb06ace`  
		Last Modified: Fri, 17 Apr 2026 00:35:39 GMT  
		Size: 2.6 MB (2562112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f12d2461c6856cb4b9e38f1e10f58b3c691f6150f59f066733d397ee75b5105f`  
		Last Modified: Fri, 17 Apr 2026 00:35:41 GMT  
		Size: 80.3 MB (80275884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54ea22269492c2f542153a408f8ae664ab7c758b69e9678eae1ef999484ee076`  
		Last Modified: Fri, 17 Apr 2026 00:35:39 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:21bb405795d823acf425cc9da14d62bb4f4922f6fe43b1185b8d9632fc6c3a33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1156537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb030500a879c45e1fe1f170d34cf57968eacbea225e06b231ff6496506ab4af`

```dockerfile
```

-	Layers:
	-	`sha256:298e83ba9d24ad873c1be021ca7abe369c9edcdec684ce4a2091b640460c1895`  
		Last Modified: Fri, 17 Apr 2026 00:35:39 GMT  
		Size: 1.1 MB (1141621 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01cec6da3589f3f1d3c57de3fef1bc321becb78658112ec75680dbf322a3e50e`  
		Last Modified: Fri, 17 Apr 2026 00:35:38 GMT  
		Size: 14.9 KB (14916 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.36-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:31b06ea04b6386db9b3807547a5d5b8f92214e9cdcfca8f6aa50cfbedae42e6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.4 MB (78368694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3317ab3c639d75d8d58870fc6c8e58519689b42f64d7ddb5b11ee84d97bed89`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:38:59 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 17 Apr 2026 00:39:01 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Fri, 17 Apr 2026 00:39:10 GMT
ENV TELEGRAF_VERSION=1.36.4
# Fri, 17 Apr 2026 00:39:10 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Fri, 17 Apr 2026 00:39:10 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Fri, 17 Apr 2026 00:39:10 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 17 Apr 2026 00:39:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 17 Apr 2026 00:39:10 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ee1ba827ed87872710c3d5ce693b64b6db6f73987e88856fae02234e76bf1ab`  
		Last Modified: Fri, 17 Apr 2026 00:39:23 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbfa8d3e4a64bfc784e7eec9e6e0a8081bfa3ef68532086a1dcfd3bc066fe855`  
		Last Modified: Fri, 17 Apr 2026 00:39:24 GMT  
		Size: 2.6 MB (2626909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aca4eb97653f28b13b386581736c4df20af7dde6ad0fd43f072849e46b0c5e9d`  
		Last Modified: Fri, 17 Apr 2026 00:39:26 GMT  
		Size: 71.6 MB (71598995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:443be9e4bf62e1c1c2370c5d9834c9e04d4118fba678e64c920fb1f1aadec3ee`  
		Last Modified: Fri, 17 Apr 2026 00:39:24 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:edbbfe80ef8a9f3d16ed8c15c3b61de8e347ac670df94942cb4a476de2a40afd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1152276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b5266cff90a3bfc13af0e5e3d94c4a3c17e34062d06b81df9296364bd088457`

```dockerfile
```

-	Layers:
	-	`sha256:b17280399b757ca659be23a08bf2456927703fd56930c4a53a6ef6843ff0f6a1`  
		Last Modified: Fri, 17 Apr 2026 00:39:24 GMT  
		Size: 1.1 MB (1137248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eaf6c769b365fba66a6167b1b28709dc12b612f0f322433a7ce7e721981d8935`  
		Last Modified: Fri, 17 Apr 2026 00:39:24 GMT  
		Size: 15.0 KB (15028 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.36.4`

```console
$ docker pull telegraf@sha256:a8aa55493d7c2733bc38e32e67cbffc714747fff3f79a3c675960dc6d6470e22
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
$ docker pull telegraf@sha256:ed3cf13470ae3ef2c12b14d78646856557365b7d1e7752454af1f684c5a680d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.0 MB (171954575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54c5ac0f9bb269a82f6dc2b5857d9c02ef0cfb9a345820a400e3a3c6fca4023f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:40:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:40:24 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:40:25 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 08 May 2026 20:40:29 GMT
ENV TELEGRAF_VERSION=1.36.4
# Fri, 08 May 2026 20:40:29 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Fri, 08 May 2026 20:40:29 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Fri, 08 May 2026 20:40:29 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 08 May 2026 20:40:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 08 May 2026 20:40:29 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:9104793a826a01456b0ba567a92064e85a029816661fbb4524da7913f0123ab5`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 48.5 MB (48488676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d055cea50c88c57fc27fcd44845ebabfe5b830ea8a0a621b89d38a2b650b7ff3`  
		Last Modified: Fri, 08 May 2026 19:40:29 GMT  
		Size: 24.0 MB (24042180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a4154482c2eb44c183af49bf72c7aade026ba03f675b7956894c73917e4aeb`  
		Last Modified: Fri, 08 May 2026 20:40:49 GMT  
		Size: 18.9 MB (18944433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d89cea0c2d13f431cd03079dc8778aedad84e9961c3396ec4db39503ecddf1a`  
		Last Modified: Fri, 08 May 2026 20:40:48 GMT  
		Size: 5.1 KB (5071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23aa70749964761b5e0c0d61e55832cb1804b29ba5dfbe139b19d2e1ba6e57d5`  
		Last Modified: Fri, 08 May 2026 20:40:50 GMT  
		Size: 80.5 MB (80473590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5fa5cc78a5df08df1dce4d8f7f25b53a4c64859f9da8ef36d19103371b0f690`  
		Last Modified: Fri, 08 May 2026 20:40:48 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36.4` - unknown; unknown

```console
$ docker pull telegraf@sha256:64c4e5cb0dac9a65442494c0b0507e2bcb7b23042b15f970b0d78c36f19f3f6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6670530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:633c5743edfa0a08353249ff063b114102abdaf33858d291c74efad350bb4e40`

```dockerfile
```

-	Layers:
	-	`sha256:8ee2630cf664d7e5bbcb46d99bd3be74646ee9015d426a35f380660e65d1f652`  
		Last Modified: Fri, 08 May 2026 20:40:48 GMT  
		Size: 6.7 MB (6656103 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f537f6254b79fe1ff68887a92103907c6872c6153f6d8e5cf13ed9fdb50d82e8`  
		Last Modified: Fri, 08 May 2026 20:40:48 GMT  
		Size: 14.4 KB (14427 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.36.4` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:34c0671c4d8c1940e2543f9175b2cf11f48f36840fe0c184ade15f3c8f8370ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.8 MB (157823252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bcc7cf8844489079b979fb613faf7fd2dfae5387f668918f3fd5204613cbae4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:44:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 21:47:53 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 21:47:54 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 08 May 2026 21:47:59 GMT
ENV TELEGRAF_VERSION=1.36.4
# Fri, 08 May 2026 21:47:59 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Fri, 08 May 2026 21:47:59 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Fri, 08 May 2026 21:47:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 08 May 2026 21:47:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 08 May 2026 21:47:59 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:752ba895535a5b96e621b623e0a11ff696fe28fb2110ab16de49e150423d0a89`  
		Last Modified: Fri, 08 May 2026 18:36:54 GMT  
		Size: 44.2 MB (44207696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b0504388ca2bf72a5fec3556b58015e5dce736337a948976b22cd4cce283cb0`  
		Last Modified: Fri, 08 May 2026 19:44:39 GMT  
		Size: 21.9 MB (21946392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5a6ba2cc1567fd653f51e96d4ac12f7ca6b7b4aed30577e0c4e17b5d252c459`  
		Last Modified: Fri, 08 May 2026 21:48:17 GMT  
		Size: 17.7 MB (17699847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f595515517c5f1e3b043bd33128b620206d79f7f8d445d31885c2035300171f`  
		Last Modified: Fri, 08 May 2026 21:48:16 GMT  
		Size: 5.1 KB (5054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db06c86962c37657991405a7566ca3aaaa20cfae71d6bbc9aaa4625d998a0f5b`  
		Last Modified: Fri, 08 May 2026 21:48:19 GMT  
		Size: 74.0 MB (73963638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff99cf870fa6e3b09f8a7af079ab03e97538752436308543f499382d35201c37`  
		Last Modified: Fri, 08 May 2026 21:48:15 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36.4` - unknown; unknown

```console
$ docker pull telegraf@sha256:df6f7057da4f0c191da72e0255cdab577490836d3ca3e938c810092ec1d12ce7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6665217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfdeb95e713a082d9a4e436fb2a382c2a562287f38d94ca392af0659235421e9`

```dockerfile
```

-	Layers:
	-	`sha256:c2e22544e95b3cf25f1c3d8bb2b77d6f0190681387ab7c9c40bf4f7d0c3e297b`  
		Last Modified: Fri, 08 May 2026 21:48:16 GMT  
		Size: 6.7 MB (6650700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc864105f0e9e40932a5abb7480ea0ee04d904c3ccb28e7e66a16f16f7a33152`  
		Last Modified: Fri, 08 May 2026 21:48:16 GMT  
		Size: 14.5 KB (14517 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.36.4` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:e3c6383352b9eff01aef5ce42bc7a75a7dc3eb39cb93433d788ad224a1aeba21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.7 MB (162674309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b30d4ea88a7c369a56e845aa4fbbae03ced50ea8f6e650e65634301b5142490e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:42:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:45:29 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:45:30 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 08 May 2026 20:45:34 GMT
ENV TELEGRAF_VERSION=1.36.4
# Fri, 08 May 2026 20:45:34 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Fri, 08 May 2026 20:45:34 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Fri, 08 May 2026 20:45:34 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 08 May 2026 20:45:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 08 May 2026 20:45:34 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:8eda28c6ece628fdff982fd6c7c1cd1f5eeccc51cfd0a3ee9155b2ccbdcc68a3`  
		Last Modified: Fri, 08 May 2026 18:24:51 GMT  
		Size: 48.4 MB (48373150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19f56578c9577bd69a05b2319baacd770a986ae61a8568047ddd91db1a1893b4`  
		Last Modified: Fri, 08 May 2026 19:42:30 GMT  
		Size: 23.6 MB (23609357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7caea1cfc8e4f5cfda68032987e00be0f353a17dbe6ff2971a9512a9c750266d`  
		Last Modified: Fri, 08 May 2026 20:45:53 GMT  
		Size: 18.9 MB (18885802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e8debbb6c9b7777b0f748abdee1061b0ec3a8f9dcc95cd14696b4cbe8b39637`  
		Last Modified: Fri, 08 May 2026 20:45:52 GMT  
		Size: 5.1 KB (5058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b7137f098a0ecf2d12f5964d2084c1e0517316750c0408ef293073a06c5ede2`  
		Last Modified: Fri, 08 May 2026 20:45:54 GMT  
		Size: 71.8 MB (71800318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cbf371040d2851c8a9ac6d9957009d8250386ba6db397061643db722dd67637`  
		Last Modified: Fri, 08 May 2026 20:45:52 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36.4` - unknown; unknown

```console
$ docker pull telegraf@sha256:6a73b9e8bbe8c4b1157aa53bca20fcc150da562a81e700357177403faefe4044
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6671315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1279ff4f8fc251200ee06891b2342d3e249bf6c8148d61428c1ffcd7ef44039`

```dockerfile
```

-	Layers:
	-	`sha256:ee0041620fabf31680c2d497d4b774fecd02bba1f9fbf731a9855b19fec39af4`  
		Last Modified: Fri, 08 May 2026 20:45:52 GMT  
		Size: 6.7 MB (6656779 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1802f83be627dea6546d588b5683637af6956111542424c9fc73dbf6fef3ecc`  
		Last Modified: Fri, 08 May 2026 20:45:52 GMT  
		Size: 14.5 KB (14536 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.36.4-alpine`

```console
$ docker pull telegraf@sha256:03418f3e6c7395c6e5b14f9e057abe26024e4f6fa5b88fa6e6ab57ce6f8c7a5c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.36.4-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:e42e15e551b65fd997636e15e96974d57b54b60aacb82f56d596c5f7b42f84cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.6 MB (86647081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d9572dba87617bf4a6b1616002ce3bd493b7bf4f41c1ae10e9cd95c2188f117`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:35:14 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 17 Apr 2026 00:35:15 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Fri, 17 Apr 2026 00:35:24 GMT
ENV TELEGRAF_VERSION=1.36.4
# Fri, 17 Apr 2026 00:35:24 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Fri, 17 Apr 2026 00:35:24 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Fri, 17 Apr 2026 00:35:24 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 17 Apr 2026 00:35:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 17 Apr 2026 00:35:24 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad4d35ed9ce2a9043f49d4a2af780155068be3d64d1e73c46b02e5f5508ebd7d`  
		Last Modified: Fri, 17 Apr 2026 00:35:38 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5abe5b9b65035ba0c23da9d6a13f11d34e00c0c90f2f61fbfce2cdd6eb06ace`  
		Last Modified: Fri, 17 Apr 2026 00:35:39 GMT  
		Size: 2.6 MB (2562112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f12d2461c6856cb4b9e38f1e10f58b3c691f6150f59f066733d397ee75b5105f`  
		Last Modified: Fri, 17 Apr 2026 00:35:41 GMT  
		Size: 80.3 MB (80275884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54ea22269492c2f542153a408f8ae664ab7c758b69e9678eae1ef999484ee076`  
		Last Modified: Fri, 17 Apr 2026 00:35:39 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36.4-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:21bb405795d823acf425cc9da14d62bb4f4922f6fe43b1185b8d9632fc6c3a33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1156537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb030500a879c45e1fe1f170d34cf57968eacbea225e06b231ff6496506ab4af`

```dockerfile
```

-	Layers:
	-	`sha256:298e83ba9d24ad873c1be021ca7abe369c9edcdec684ce4a2091b640460c1895`  
		Last Modified: Fri, 17 Apr 2026 00:35:39 GMT  
		Size: 1.1 MB (1141621 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01cec6da3589f3f1d3c57de3fef1bc321becb78658112ec75680dbf322a3e50e`  
		Last Modified: Fri, 17 Apr 2026 00:35:38 GMT  
		Size: 14.9 KB (14916 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.36.4-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:31b06ea04b6386db9b3807547a5d5b8f92214e9cdcfca8f6aa50cfbedae42e6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.4 MB (78368694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3317ab3c639d75d8d58870fc6c8e58519689b42f64d7ddb5b11ee84d97bed89`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:38:59 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 17 Apr 2026 00:39:01 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Fri, 17 Apr 2026 00:39:10 GMT
ENV TELEGRAF_VERSION=1.36.4
# Fri, 17 Apr 2026 00:39:10 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Fri, 17 Apr 2026 00:39:10 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Fri, 17 Apr 2026 00:39:10 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 17 Apr 2026 00:39:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 17 Apr 2026 00:39:10 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ee1ba827ed87872710c3d5ce693b64b6db6f73987e88856fae02234e76bf1ab`  
		Last Modified: Fri, 17 Apr 2026 00:39:23 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbfa8d3e4a64bfc784e7eec9e6e0a8081bfa3ef68532086a1dcfd3bc066fe855`  
		Last Modified: Fri, 17 Apr 2026 00:39:24 GMT  
		Size: 2.6 MB (2626909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aca4eb97653f28b13b386581736c4df20af7dde6ad0fd43f072849e46b0c5e9d`  
		Last Modified: Fri, 17 Apr 2026 00:39:26 GMT  
		Size: 71.6 MB (71598995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:443be9e4bf62e1c1c2370c5d9834c9e04d4118fba678e64c920fb1f1aadec3ee`  
		Last Modified: Fri, 17 Apr 2026 00:39:24 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36.4-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:edbbfe80ef8a9f3d16ed8c15c3b61de8e347ac670df94942cb4a476de2a40afd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1152276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b5266cff90a3bfc13af0e5e3d94c4a3c17e34062d06b81df9296364bd088457`

```dockerfile
```

-	Layers:
	-	`sha256:b17280399b757ca659be23a08bf2456927703fd56930c4a53a6ef6843ff0f6a1`  
		Last Modified: Fri, 17 Apr 2026 00:39:24 GMT  
		Size: 1.1 MB (1137248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eaf6c769b365fba66a6167b1b28709dc12b612f0f322433a7ce7e721981d8935`  
		Last Modified: Fri, 17 Apr 2026 00:39:24 GMT  
		Size: 15.0 KB (15028 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.37`

```console
$ docker pull telegraf@sha256:9d950b2096ff608d75451dc3d925cf2781e7202cf4cd7022ce6f4d56c75ddd95
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
$ docker pull telegraf@sha256:1e42d5443a3ec3a8e3cd4ddf0f651b941eed254c00bf8e9aeb5ea7d0bd40a1aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.3 MB (172264160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce34859927ddbeed936b411222496ab0fda866c46a003c40b2dbc28a414147e7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:40:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:40:25 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:40:26 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 08 May 2026 20:40:30 GMT
ENV TELEGRAF_VERSION=1.37.3
# Fri, 08 May 2026 20:40:30 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Fri, 08 May 2026 20:40:30 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Fri, 08 May 2026 20:40:30 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 08 May 2026 20:40:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 08 May 2026 20:40:30 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:9104793a826a01456b0ba567a92064e85a029816661fbb4524da7913f0123ab5`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 48.5 MB (48488676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d055cea50c88c57fc27fcd44845ebabfe5b830ea8a0a621b89d38a2b650b7ff3`  
		Last Modified: Fri, 08 May 2026 19:40:29 GMT  
		Size: 24.0 MB (24042180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d437cb911601568e742d3a0ca458eb982c87ae00adacc692eee8c6377457dae`  
		Last Modified: Fri, 08 May 2026 20:40:51 GMT  
		Size: 18.9 MB (18944410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f962bf2e511abcaf5b122fadd3b00c79eafa85e96e74033613126d122c0cd1d5`  
		Last Modified: Fri, 08 May 2026 20:40:50 GMT  
		Size: 5.1 KB (5070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d7625cbdd0c53d4ec2952140fae7494f8b3a5e3b7d859042b040b112b071d0c`  
		Last Modified: Fri, 08 May 2026 20:40:53 GMT  
		Size: 80.8 MB (80783201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4959127cd671d79bed80f6e3c9d038ec7cacd92a016bd091471d3e46464e7329`  
		Last Modified: Fri, 08 May 2026 20:40:50 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.37` - unknown; unknown

```console
$ docker pull telegraf@sha256:26fb62146df49d5ac91cf64f216e1cca7acd202fa63ff83066c5d0ab656733b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6681384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac4f44dcfdf075f897a53aa85da2da50e7dce6f5e13f3dc78a292393572ae53d`

```dockerfile
```

-	Layers:
	-	`sha256:5b7929418c33152c8cba13d794b9e69628ea44e3d32b152e28f9ab863a9c4b21`  
		Last Modified: Fri, 08 May 2026 20:40:50 GMT  
		Size: 6.7 MB (6666958 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef11e882917acc2e2eeb766e06dab6e72fb8c840e1d30e9fda5a02926587b6d7`  
		Last Modified: Fri, 08 May 2026 20:40:50 GMT  
		Size: 14.4 KB (14426 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.37` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:c835b7f782b802284661d378ce532e3f6c1da29598374894377bb112646751a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.5 MB (158476964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90dc29025e1332a0ae901f992fd14b14f3e8029a682a2aae7dec9cbd613e4d89`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:44:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 21:47:53 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 21:47:53 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 08 May 2026 21:47:58 GMT
ENV TELEGRAF_VERSION=1.37.3
# Fri, 08 May 2026 21:47:58 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Fri, 08 May 2026 21:47:58 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Fri, 08 May 2026 21:47:58 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 08 May 2026 21:47:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 08 May 2026 21:47:58 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:752ba895535a5b96e621b623e0a11ff696fe28fb2110ab16de49e150423d0a89`  
		Last Modified: Fri, 08 May 2026 18:36:54 GMT  
		Size: 44.2 MB (44207696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b0504388ca2bf72a5fec3556b58015e5dce736337a948976b22cd4cce283cb0`  
		Last Modified: Fri, 08 May 2026 19:44:39 GMT  
		Size: 21.9 MB (21946392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4de4a66492a0fee7fb483eeef88fe8e8078344b18c20ddcf5f5e4a6ba8a0b975`  
		Last Modified: Fri, 08 May 2026 21:48:16 GMT  
		Size: 17.7 MB (17699694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b718887c4a9dacbf242d7b341a38c412e7702a286ec1a960acb1565a095e180`  
		Last Modified: Fri, 08 May 2026 21:48:15 GMT  
		Size: 5.1 KB (5055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:941aa2295988ea5808fdeefe258497ddc6fb27472f6e6a8fd51a0bc9f6ee3691`  
		Last Modified: Fri, 08 May 2026 21:48:18 GMT  
		Size: 74.6 MB (74617502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff99cf870fa6e3b09f8a7af079ab03e97538752436308543f499382d35201c37`  
		Last Modified: Fri, 08 May 2026 21:48:15 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.37` - unknown; unknown

```console
$ docker pull telegraf@sha256:9cd4dd8e6ca32d371459420f87d2a42c09326dcc38da3a06f82ad06c26d658cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6676072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cff6a94a8821c57907c6f1aa504e6cd1dc7085e3677857d9c91fa73b70f8a41e`

```dockerfile
```

-	Layers:
	-	`sha256:d14c8f3f5f490f73b336a2658f18b772367fc5f8b7c29ec40901f78ffb105d8f`  
		Last Modified: Fri, 08 May 2026 21:48:15 GMT  
		Size: 6.7 MB (6661555 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43600b67dadc8c4fdfbabdfbb5afecf8256cae039c620c1b7a7f584a1ed29ba8`  
		Last Modified: Fri, 08 May 2026 21:48:15 GMT  
		Size: 14.5 KB (14517 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.37` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:a139c5c629b9ac5313b9df5eef6044d7391eec370eb6201e3d0f77cf2e7d35ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.0 MB (163044928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5eb2e5323323a0cbaee7e0f65593c222baaee851bf7af4246e37a840fc03b390`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:42:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:45:34 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:45:35 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 08 May 2026 20:45:39 GMT
ENV TELEGRAF_VERSION=1.37.3
# Fri, 08 May 2026 20:45:39 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Fri, 08 May 2026 20:45:39 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Fri, 08 May 2026 20:45:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 08 May 2026 20:45:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 08 May 2026 20:45:39 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:8eda28c6ece628fdff982fd6c7c1cd1f5eeccc51cfd0a3ee9155b2ccbdcc68a3`  
		Last Modified: Fri, 08 May 2026 18:24:51 GMT  
		Size: 48.4 MB (48373150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19f56578c9577bd69a05b2319baacd770a986ae61a8568047ddd91db1a1893b4`  
		Last Modified: Fri, 08 May 2026 19:42:30 GMT  
		Size: 23.6 MB (23609357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:669c3f7991064defd37cc1f81aa89d917442ada26ec0edfd67dc104622914568`  
		Last Modified: Fri, 08 May 2026 20:45:57 GMT  
		Size: 18.9 MB (18885750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e6612517e51c9a0cd6e380e2c8c51d60eaaf4fdeb2fcc6c9343ffe283168303`  
		Last Modified: Fri, 08 May 2026 20:45:55 GMT  
		Size: 5.1 KB (5058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7091eab61e6dca8cb214340ea72e33defa2efff757cd6b33cecc3ce7a59158c`  
		Last Modified: Fri, 08 May 2026 20:45:58 GMT  
		Size: 72.2 MB (72170989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:549b189507f46375d9a05fa4d74bdedb262561128b9457dd4cbee205f829191c`  
		Last Modified: Fri, 08 May 2026 20:45:56 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.37` - unknown; unknown

```console
$ docker pull telegraf@sha256:3c44c1c625b30c8a3a8659f17e6b808d9d09c1d4ec64d74943629a3c36ee19c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6682171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23c7aac860fca774ab71d17dcabdf6268e0fb947f573cc4183357c950934df53`

```dockerfile
```

-	Layers:
	-	`sha256:59138b81e4e8e13ae5322cf19e48342bda8547b9de2e4aadc7e7083cb789e928`  
		Last Modified: Fri, 08 May 2026 20:45:56 GMT  
		Size: 6.7 MB (6667634 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b9c496897ce8f75370cecd4020f1f0a2ed6ef56af32f2739482a0648f49afe0`  
		Last Modified: Fri, 08 May 2026 20:45:56 GMT  
		Size: 14.5 KB (14537 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.37-alpine`

```console
$ docker pull telegraf@sha256:7ce48bd5c31b4445f9374372e878e4eaaa0fe9a1a09038e48fbe2ffdcf3688c6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.37-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:8dc34975014acbe34d8f1c9840a68e3c22a91a756badd81dbcef76581390d9ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.9 MB (86947908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3d5b66113f71a03ab0425b955c1deb5ba3f0c77b95c2b51ae1b4671c7b79d86`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:30:04 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 17 Apr 2026 00:35:17 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Fri, 17 Apr 2026 00:35:26 GMT
ENV TELEGRAF_VERSION=1.37.3
# Fri, 17 Apr 2026 00:35:26 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Fri, 17 Apr 2026 00:35:26 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Fri, 17 Apr 2026 00:35:26 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 17 Apr 2026 00:35:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 17 Apr 2026 00:35:26 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d7600c85c12c2ddea00a9ffd598e19d68011c93d7ff61b76b12d615b618d996`  
		Last Modified: Fri, 17 Apr 2026 00:30:27 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2a51d3715d3b0601ef9268636e1023122bea6ae3bb0fafbfe706893c084c2b8`  
		Last Modified: Fri, 17 Apr 2026 00:35:40 GMT  
		Size: 2.6 MB (2562092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71083104bc01e56e9de463fdb3005eaa1893af5c4a695e3d2162ad2bd3ef1db6`  
		Last Modified: Fri, 17 Apr 2026 00:35:42 GMT  
		Size: 80.6 MB (80576729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72681e60733a7583a520d23d4d887a797429e5fa0224a8f37563965788a2b361`  
		Last Modified: Fri, 17 Apr 2026 00:35:40 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.37-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:72fda82e1ce6efbf9c5daf84534c21fa25028de4f94bae3085f53abb68bd61bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1167394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f681817e17e1c087aee4b058ddef6e464bef59279a5c91f9df01e38830bd3d45`

```dockerfile
```

-	Layers:
	-	`sha256:3fe66e1a1733c82f9e247d838f0a2bef9f271cc994740be8089bc39bab296490`  
		Last Modified: Fri, 17 Apr 2026 00:35:40 GMT  
		Size: 1.2 MB (1152476 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e4d2627591f9d25cc99ea260d322b98694609da032c6ae21d328f1d37a2e656`  
		Last Modified: Fri, 17 Apr 2026 00:35:40 GMT  
		Size: 14.9 KB (14918 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.37-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:18045c4777e9e64159571af8098a783ea888a90d8b92b970580907f2d973855a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.7 MB (78732054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7589f8514fb411ea5b8fb73b4536c12c8c79043b1302c67562edc3fb1a2bc9cb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:39:16 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 17 Apr 2026 00:39:17 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Fri, 17 Apr 2026 00:39:26 GMT
ENV TELEGRAF_VERSION=1.37.3
# Fri, 17 Apr 2026 00:39:26 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Fri, 17 Apr 2026 00:39:26 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Fri, 17 Apr 2026 00:39:26 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 17 Apr 2026 00:39:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 17 Apr 2026 00:39:26 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f96f22d1f5699a3326a5b940499fa9fe7b7357964fae6531d8af1885eb09358a`  
		Last Modified: Fri, 17 Apr 2026 00:39:39 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b37cbdd61b2cd6abaa0b31912f17c681f202f7cc6c15bc6e0c37ab9268b785ba`  
		Last Modified: Fri, 17 Apr 2026 00:39:39 GMT  
		Size: 2.6 MB (2626894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63e0cbb4f736f59179413e8cafe912549e9a33cde6e1f56eb9193f499f86d7bc`  
		Last Modified: Fri, 17 Apr 2026 00:39:41 GMT  
		Size: 72.0 MB (71962368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e1cfc5c288d01b4e69a072c6f493dcc7bd2ca7bcec8978c66386e943337ca9d`  
		Last Modified: Fri, 17 Apr 2026 00:39:39 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.37-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:d9cb24d71eaa220f09fbec2e28f039f46ee85a7fd3cfd837e6f639a848af49b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1163130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a6051285162d488c6150940d19ff88ddb0bca537ac70a6451d6a0c355722fc5`

```dockerfile
```

-	Layers:
	-	`sha256:eefa7a071bcab8d81979b369b4a1d7d163c82d6da0847b977a1bc31c1474ac09`  
		Last Modified: Fri, 17 Apr 2026 00:39:39 GMT  
		Size: 1.1 MB (1148103 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32fcbca9fdcfe9317c201f860fd3e6f9318a9055e2bac9e7aed6297bd5ba98d4`  
		Last Modified: Fri, 17 Apr 2026 00:39:39 GMT  
		Size: 15.0 KB (15027 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.37.3`

```console
$ docker pull telegraf@sha256:9d950b2096ff608d75451dc3d925cf2781e7202cf4cd7022ce6f4d56c75ddd95
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
$ docker pull telegraf@sha256:1e42d5443a3ec3a8e3cd4ddf0f651b941eed254c00bf8e9aeb5ea7d0bd40a1aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.3 MB (172264160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce34859927ddbeed936b411222496ab0fda866c46a003c40b2dbc28a414147e7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:40:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:40:25 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:40:26 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 08 May 2026 20:40:30 GMT
ENV TELEGRAF_VERSION=1.37.3
# Fri, 08 May 2026 20:40:30 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Fri, 08 May 2026 20:40:30 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Fri, 08 May 2026 20:40:30 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 08 May 2026 20:40:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 08 May 2026 20:40:30 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:9104793a826a01456b0ba567a92064e85a029816661fbb4524da7913f0123ab5`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 48.5 MB (48488676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d055cea50c88c57fc27fcd44845ebabfe5b830ea8a0a621b89d38a2b650b7ff3`  
		Last Modified: Fri, 08 May 2026 19:40:29 GMT  
		Size: 24.0 MB (24042180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d437cb911601568e742d3a0ca458eb982c87ae00adacc692eee8c6377457dae`  
		Last Modified: Fri, 08 May 2026 20:40:51 GMT  
		Size: 18.9 MB (18944410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f962bf2e511abcaf5b122fadd3b00c79eafa85e96e74033613126d122c0cd1d5`  
		Last Modified: Fri, 08 May 2026 20:40:50 GMT  
		Size: 5.1 KB (5070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d7625cbdd0c53d4ec2952140fae7494f8b3a5e3b7d859042b040b112b071d0c`  
		Last Modified: Fri, 08 May 2026 20:40:53 GMT  
		Size: 80.8 MB (80783201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4959127cd671d79bed80f6e3c9d038ec7cacd92a016bd091471d3e46464e7329`  
		Last Modified: Fri, 08 May 2026 20:40:50 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.37.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:26fb62146df49d5ac91cf64f216e1cca7acd202fa63ff83066c5d0ab656733b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6681384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac4f44dcfdf075f897a53aa85da2da50e7dce6f5e13f3dc78a292393572ae53d`

```dockerfile
```

-	Layers:
	-	`sha256:5b7929418c33152c8cba13d794b9e69628ea44e3d32b152e28f9ab863a9c4b21`  
		Last Modified: Fri, 08 May 2026 20:40:50 GMT  
		Size: 6.7 MB (6666958 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef11e882917acc2e2eeb766e06dab6e72fb8c840e1d30e9fda5a02926587b6d7`  
		Last Modified: Fri, 08 May 2026 20:40:50 GMT  
		Size: 14.4 KB (14426 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.37.3` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:c835b7f782b802284661d378ce532e3f6c1da29598374894377bb112646751a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.5 MB (158476964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90dc29025e1332a0ae901f992fd14b14f3e8029a682a2aae7dec9cbd613e4d89`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:44:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 21:47:53 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 21:47:53 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 08 May 2026 21:47:58 GMT
ENV TELEGRAF_VERSION=1.37.3
# Fri, 08 May 2026 21:47:58 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Fri, 08 May 2026 21:47:58 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Fri, 08 May 2026 21:47:58 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 08 May 2026 21:47:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 08 May 2026 21:47:58 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:752ba895535a5b96e621b623e0a11ff696fe28fb2110ab16de49e150423d0a89`  
		Last Modified: Fri, 08 May 2026 18:36:54 GMT  
		Size: 44.2 MB (44207696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b0504388ca2bf72a5fec3556b58015e5dce736337a948976b22cd4cce283cb0`  
		Last Modified: Fri, 08 May 2026 19:44:39 GMT  
		Size: 21.9 MB (21946392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4de4a66492a0fee7fb483eeef88fe8e8078344b18c20ddcf5f5e4a6ba8a0b975`  
		Last Modified: Fri, 08 May 2026 21:48:16 GMT  
		Size: 17.7 MB (17699694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b718887c4a9dacbf242d7b341a38c412e7702a286ec1a960acb1565a095e180`  
		Last Modified: Fri, 08 May 2026 21:48:15 GMT  
		Size: 5.1 KB (5055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:941aa2295988ea5808fdeefe258497ddc6fb27472f6e6a8fd51a0bc9f6ee3691`  
		Last Modified: Fri, 08 May 2026 21:48:18 GMT  
		Size: 74.6 MB (74617502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff99cf870fa6e3b09f8a7af079ab03e97538752436308543f499382d35201c37`  
		Last Modified: Fri, 08 May 2026 21:48:15 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.37.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:9cd4dd8e6ca32d371459420f87d2a42c09326dcc38da3a06f82ad06c26d658cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6676072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cff6a94a8821c57907c6f1aa504e6cd1dc7085e3677857d9c91fa73b70f8a41e`

```dockerfile
```

-	Layers:
	-	`sha256:d14c8f3f5f490f73b336a2658f18b772367fc5f8b7c29ec40901f78ffb105d8f`  
		Last Modified: Fri, 08 May 2026 21:48:15 GMT  
		Size: 6.7 MB (6661555 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43600b67dadc8c4fdfbabdfbb5afecf8256cae039c620c1b7a7f584a1ed29ba8`  
		Last Modified: Fri, 08 May 2026 21:48:15 GMT  
		Size: 14.5 KB (14517 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.37.3` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:a139c5c629b9ac5313b9df5eef6044d7391eec370eb6201e3d0f77cf2e7d35ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.0 MB (163044928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5eb2e5323323a0cbaee7e0f65593c222baaee851bf7af4246e37a840fc03b390`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:42:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:45:34 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:45:35 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 08 May 2026 20:45:39 GMT
ENV TELEGRAF_VERSION=1.37.3
# Fri, 08 May 2026 20:45:39 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Fri, 08 May 2026 20:45:39 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Fri, 08 May 2026 20:45:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 08 May 2026 20:45:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 08 May 2026 20:45:39 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:8eda28c6ece628fdff982fd6c7c1cd1f5eeccc51cfd0a3ee9155b2ccbdcc68a3`  
		Last Modified: Fri, 08 May 2026 18:24:51 GMT  
		Size: 48.4 MB (48373150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19f56578c9577bd69a05b2319baacd770a986ae61a8568047ddd91db1a1893b4`  
		Last Modified: Fri, 08 May 2026 19:42:30 GMT  
		Size: 23.6 MB (23609357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:669c3f7991064defd37cc1f81aa89d917442ada26ec0edfd67dc104622914568`  
		Last Modified: Fri, 08 May 2026 20:45:57 GMT  
		Size: 18.9 MB (18885750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e6612517e51c9a0cd6e380e2c8c51d60eaaf4fdeb2fcc6c9343ffe283168303`  
		Last Modified: Fri, 08 May 2026 20:45:55 GMT  
		Size: 5.1 KB (5058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7091eab61e6dca8cb214340ea72e33defa2efff757cd6b33cecc3ce7a59158c`  
		Last Modified: Fri, 08 May 2026 20:45:58 GMT  
		Size: 72.2 MB (72170989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:549b189507f46375d9a05fa4d74bdedb262561128b9457dd4cbee205f829191c`  
		Last Modified: Fri, 08 May 2026 20:45:56 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.37.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:3c44c1c625b30c8a3a8659f17e6b808d9d09c1d4ec64d74943629a3c36ee19c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6682171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23c7aac860fca774ab71d17dcabdf6268e0fb947f573cc4183357c950934df53`

```dockerfile
```

-	Layers:
	-	`sha256:59138b81e4e8e13ae5322cf19e48342bda8547b9de2e4aadc7e7083cb789e928`  
		Last Modified: Fri, 08 May 2026 20:45:56 GMT  
		Size: 6.7 MB (6667634 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b9c496897ce8f75370cecd4020f1f0a2ed6ef56af32f2739482a0648f49afe0`  
		Last Modified: Fri, 08 May 2026 20:45:56 GMT  
		Size: 14.5 KB (14537 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.37.3-alpine`

```console
$ docker pull telegraf@sha256:7ce48bd5c31b4445f9374372e878e4eaaa0fe9a1a09038e48fbe2ffdcf3688c6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.37.3-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:8dc34975014acbe34d8f1c9840a68e3c22a91a756badd81dbcef76581390d9ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.9 MB (86947908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3d5b66113f71a03ab0425b955c1deb5ba3f0c77b95c2b51ae1b4671c7b79d86`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:30:04 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 17 Apr 2026 00:35:17 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Fri, 17 Apr 2026 00:35:26 GMT
ENV TELEGRAF_VERSION=1.37.3
# Fri, 17 Apr 2026 00:35:26 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Fri, 17 Apr 2026 00:35:26 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Fri, 17 Apr 2026 00:35:26 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 17 Apr 2026 00:35:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 17 Apr 2026 00:35:26 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d7600c85c12c2ddea00a9ffd598e19d68011c93d7ff61b76b12d615b618d996`  
		Last Modified: Fri, 17 Apr 2026 00:30:27 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2a51d3715d3b0601ef9268636e1023122bea6ae3bb0fafbfe706893c084c2b8`  
		Last Modified: Fri, 17 Apr 2026 00:35:40 GMT  
		Size: 2.6 MB (2562092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71083104bc01e56e9de463fdb3005eaa1893af5c4a695e3d2162ad2bd3ef1db6`  
		Last Modified: Fri, 17 Apr 2026 00:35:42 GMT  
		Size: 80.6 MB (80576729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72681e60733a7583a520d23d4d887a797429e5fa0224a8f37563965788a2b361`  
		Last Modified: Fri, 17 Apr 2026 00:35:40 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.37.3-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:72fda82e1ce6efbf9c5daf84534c21fa25028de4f94bae3085f53abb68bd61bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1167394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f681817e17e1c087aee4b058ddef6e464bef59279a5c91f9df01e38830bd3d45`

```dockerfile
```

-	Layers:
	-	`sha256:3fe66e1a1733c82f9e247d838f0a2bef9f271cc994740be8089bc39bab296490`  
		Last Modified: Fri, 17 Apr 2026 00:35:40 GMT  
		Size: 1.2 MB (1152476 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e4d2627591f9d25cc99ea260d322b98694609da032c6ae21d328f1d37a2e656`  
		Last Modified: Fri, 17 Apr 2026 00:35:40 GMT  
		Size: 14.9 KB (14918 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.37.3-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:18045c4777e9e64159571af8098a783ea888a90d8b92b970580907f2d973855a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.7 MB (78732054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7589f8514fb411ea5b8fb73b4536c12c8c79043b1302c67562edc3fb1a2bc9cb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:39:16 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 17 Apr 2026 00:39:17 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Fri, 17 Apr 2026 00:39:26 GMT
ENV TELEGRAF_VERSION=1.37.3
# Fri, 17 Apr 2026 00:39:26 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Fri, 17 Apr 2026 00:39:26 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Fri, 17 Apr 2026 00:39:26 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 17 Apr 2026 00:39:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 17 Apr 2026 00:39:26 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f96f22d1f5699a3326a5b940499fa9fe7b7357964fae6531d8af1885eb09358a`  
		Last Modified: Fri, 17 Apr 2026 00:39:39 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b37cbdd61b2cd6abaa0b31912f17c681f202f7cc6c15bc6e0c37ab9268b785ba`  
		Last Modified: Fri, 17 Apr 2026 00:39:39 GMT  
		Size: 2.6 MB (2626894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63e0cbb4f736f59179413e8cafe912549e9a33cde6e1f56eb9193f499f86d7bc`  
		Last Modified: Fri, 17 Apr 2026 00:39:41 GMT  
		Size: 72.0 MB (71962368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e1cfc5c288d01b4e69a072c6f493dcc7bd2ca7bcec8978c66386e943337ca9d`  
		Last Modified: Fri, 17 Apr 2026 00:39:39 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.37.3-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:d9cb24d71eaa220f09fbec2e28f039f46ee85a7fd3cfd837e6f639a848af49b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1163130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a6051285162d488c6150940d19ff88ddb0bca537ac70a6451d6a0c355722fc5`

```dockerfile
```

-	Layers:
	-	`sha256:eefa7a071bcab8d81979b369b4a1d7d163c82d6da0847b977a1bc31c1474ac09`  
		Last Modified: Fri, 17 Apr 2026 00:39:39 GMT  
		Size: 1.1 MB (1148103 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32fcbca9fdcfe9317c201f860fd3e6f9318a9055e2bac9e7aed6297bd5ba98d4`  
		Last Modified: Fri, 17 Apr 2026 00:39:39 GMT  
		Size: 15.0 KB (15027 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.38`

```console
$ docker pull telegraf@sha256:cf7f3e5c0cd7b1ee5ab69b707fe7b30e3b969c2b940f087cc84debe92ce0aae8
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
$ docker pull telegraf@sha256:80f0262f1764d7220207e02d4f39e2e4746a57836865f95339121c2f5d4b9319
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.0 MB (174991948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3c60b6e1594923a92cb94407321531d19377b3f65ff3d0f2b9a13618f5234b0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:40:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 23:53:40 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 23:53:41 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 11 May 2026 23:53:45 GMT
ENV TELEGRAF_VERSION=1.38.4
# Mon, 11 May 2026 23:53:45 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 11 May 2026 23:53:45 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 11 May 2026 23:53:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 11 May 2026 23:53:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 11 May 2026 23:53:45 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:9104793a826a01456b0ba567a92064e85a029816661fbb4524da7913f0123ab5`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 48.5 MB (48488676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d055cea50c88c57fc27fcd44845ebabfe5b830ea8a0a621b89d38a2b650b7ff3`  
		Last Modified: Fri, 08 May 2026 19:40:29 GMT  
		Size: 24.0 MB (24042180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc401cab11768d2b73aa0f36b0d76831b9aa4c7a568fdf9be0fa309112ef4fd4`  
		Last Modified: Mon, 11 May 2026 23:54:06 GMT  
		Size: 18.9 MB (18944282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60bf251f55455c38e3f15bed7a3f75b426f1815c5d0dce73125a3617fc770a62`  
		Last Modified: Mon, 11 May 2026 23:54:04 GMT  
		Size: 5.1 KB (5069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a720032e9b8bdb47e8f616671f2022496c72cf16644ad344541cf9d2b135a92`  
		Last Modified: Mon, 11 May 2026 23:54:07 GMT  
		Size: 83.5 MB (83511119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c19c791a0de19bd603e238311b3d1fa63543a036ff1f69d222c7e7b1dce41fd`  
		Last Modified: Mon, 11 May 2026 23:54:05 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.38` - unknown; unknown

```console
$ docker pull telegraf@sha256:55cbed9339d919070e63e8ec47800577b2df280770b0f6afc723190d297a3a27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6689294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4934a5127878b8d5da77a4ceb933d0c592f8332e1119e4d02ebd3205ad434146`

```dockerfile
```

-	Layers:
	-	`sha256:febb6e9adddc67a1c7ad1bc75bfbf4884cc6b32992f68ebd4f2cb60a9ed0a7e5`  
		Last Modified: Mon, 11 May 2026 23:54:05 GMT  
		Size: 6.7 MB (6674565 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ab5e4877b539a3bedcb6961e259913239cd77f99ba352bf3cb774d5fb4da89c`  
		Last Modified: Mon, 11 May 2026 23:54:04 GMT  
		Size: 14.7 KB (14729 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.38` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:a04f5de1f41fdc580bf27c29e7cf392a389198156eb0988abd4c83e25e675fe8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.3 MB (161287558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb1bdce67fbf4f45c1907d2d9a913aa2da7bdcaf53273d0ed34099497664685f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:44:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 23:53:44 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 23:53:45 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 11 May 2026 23:53:50 GMT
ENV TELEGRAF_VERSION=1.38.4
# Mon, 11 May 2026 23:53:50 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 11 May 2026 23:53:50 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 11 May 2026 23:53:50 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 11 May 2026 23:53:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 11 May 2026 23:53:50 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:752ba895535a5b96e621b623e0a11ff696fe28fb2110ab16de49e150423d0a89`  
		Last Modified: Fri, 08 May 2026 18:36:54 GMT  
		Size: 44.2 MB (44207696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b0504388ca2bf72a5fec3556b58015e5dce736337a948976b22cd4cce283cb0`  
		Last Modified: Fri, 08 May 2026 19:44:39 GMT  
		Size: 21.9 MB (21946392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb6eba3c782b7cc747ee4a809321eebf18d8982c91ea59720226b56cac299608`  
		Last Modified: Mon, 11 May 2026 23:54:08 GMT  
		Size: 17.7 MB (17699869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1618dd9f2c5aa795ad17b5c76403cd1d2f28c2a8a4be35ef9a3c963e71104631`  
		Last Modified: Mon, 11 May 2026 23:54:07 GMT  
		Size: 5.1 KB (5070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b47fa8118f4e1b53b666dfc2d985df74424cff2482f6f7ce3268ec8b3ef5da`  
		Last Modified: Mon, 11 May 2026 23:54:09 GMT  
		Size: 77.4 MB (77427909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac6fe4d37f249d0b62a594b3eb04746408285e8763e0b846fd7031d7e3c0a71c`  
		Last Modified: Mon, 11 May 2026 23:54:07 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.38` - unknown; unknown

```console
$ docker pull telegraf@sha256:7fd0f946cee5b67fc708d89eb1fbc208bdca91e28630d0f28b10bb390255286b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6683997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a209fb2471636227dac7b3f894e7f4b4d265e322ed71c06322fdff32ba436ce6`

```dockerfile
```

-	Layers:
	-	`sha256:67b856fdec15003642b567bbde1db8736a5c99300c58a08bcb65be0cc7b37850`  
		Last Modified: Mon, 11 May 2026 23:54:07 GMT  
		Size: 6.7 MB (6669170 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0572bfd71e1532ea0d65afa82546864d446b3780babb902b2406fdbd37b18a56`  
		Last Modified: Mon, 11 May 2026 23:54:07 GMT  
		Size: 14.8 KB (14827 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.38` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:9d5ad52e5e2b07a326e5cd0f0f064566b413335ca5704768cc173da61ffe0a2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.4 MB (165350749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba33f42f3b75c6f86298a199f6f46fa4d3c7ef629cbd4350ee11c43dd66f849b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:42:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 23:53:44 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 23:53:45 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 11 May 2026 23:53:49 GMT
ENV TELEGRAF_VERSION=1.38.4
# Mon, 11 May 2026 23:53:49 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 11 May 2026 23:53:49 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 11 May 2026 23:53:49 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 11 May 2026 23:53:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 11 May 2026 23:53:49 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:8eda28c6ece628fdff982fd6c7c1cd1f5eeccc51cfd0a3ee9155b2ccbdcc68a3`  
		Last Modified: Fri, 08 May 2026 18:24:51 GMT  
		Size: 48.4 MB (48373150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19f56578c9577bd69a05b2319baacd770a986ae61a8568047ddd91db1a1893b4`  
		Last Modified: Fri, 08 May 2026 19:42:30 GMT  
		Size: 23.6 MB (23609357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:814a8bda2fbfc42c158410ad33c204312964d366ad654eccf35597219b49b9ad`  
		Last Modified: Mon, 11 May 2026 23:54:09 GMT  
		Size: 18.9 MB (18885813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1618dd9f2c5aa795ad17b5c76403cd1d2f28c2a8a4be35ef9a3c963e71104631`  
		Last Modified: Mon, 11 May 2026 23:54:07 GMT  
		Size: 5.1 KB (5070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:472f805f5e0ffc4e1ed052f46b773ec7e7c39887926a10953189f7aafdd2b9a3`  
		Last Modified: Mon, 11 May 2026 23:54:10 GMT  
		Size: 74.5 MB (74476737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac6fe4d37f249d0b62a594b3eb04746408285e8763e0b846fd7031d7e3c0a71c`  
		Last Modified: Mon, 11 May 2026 23:54:07 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.38` - unknown; unknown

```console
$ docker pull telegraf@sha256:ec75681b0736c5a8ba960e031f6573f031b7a4f5a97da4eccc6905c7b57ff184
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6690104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f9a392223a61f98d69639a2ee694a7221d184761b44ccf470ed0f28654f58ec`

```dockerfile
```

-	Layers:
	-	`sha256:3128e488344cda446d4255fc7a4a85691d278f03fc0fdf963b0312b35d3b4153`  
		Last Modified: Mon, 11 May 2026 23:54:08 GMT  
		Size: 6.7 MB (6675253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74a9a55247bffe2184c7f32a22162b27d6839dc2affe61be40888960239dde1e`  
		Last Modified: Mon, 11 May 2026 23:54:08 GMT  
		Size: 14.9 KB (14851 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.38-alpine`

```console
$ docker pull telegraf@sha256:49fc4b3e60115966979d653e76874bd960acdd27cd484a4a57813132e474d882
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.38-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:c7bba96a83d3784fa69230bfa127df503fc8fb40ed96579d1577695a4ebc4049
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.8 MB (89781668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bde7e8a9f0886477eb58d149d3fdb897576a1ff2880814cec5bb3e33a87fe23`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Mon, 11 May 2026 23:53:34 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 11 May 2026 23:53:35 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 11 May 2026 23:53:41 GMT
ENV TELEGRAF_VERSION=1.38.4
# Mon, 11 May 2026 23:53:41 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 11 May 2026 23:53:41 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 11 May 2026 23:53:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 11 May 2026 23:53:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 11 May 2026 23:53:41 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:632464fc81a2417f86866f355eb404dd6fbaf95f23753e20e4aa1e267529287c`  
		Last Modified: Mon, 11 May 2026 23:53:57 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2019e1df3daf5a5b4b76e4c51b0f6852dfe81b1860b80f3453f1e6834f8b07e7`  
		Last Modified: Mon, 11 May 2026 23:53:57 GMT  
		Size: 2.6 MB (2615506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55706eb6bc48155a245fd2f96c71cb107f44fcccdd2aaa7c8a9010f4d9f3531e`  
		Last Modified: Mon, 11 May 2026 23:53:59 GMT  
		Size: 83.3 MB (83301076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e18d0f774411b978b4a6dcff56ac3efb4fe752d82ff76811fa2d292168e096ee`  
		Last Modified: Mon, 11 May 2026 23:53:57 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.38-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:6cfc1222edb07a0523e4a8b7d809b2cba473b87420ca92dfc9494a8e05a0249b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1174645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43e4e891c501b04fc88f432dee4f0cbe8b1a2f9fbef27a8b59b5e1c8c857b410`

```dockerfile
```

-	Layers:
	-	`sha256:87172905ac106dc4e375b2ee186d37f6d4ae3e2e57f8397ed23b9df4a4af5ef3`  
		Last Modified: Mon, 11 May 2026 23:53:57 GMT  
		Size: 1.2 MB (1159425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95634f1fdd7e204e3763697b4cc7367156ab43224e38e2c5541d394a304ed5f2`  
		Last Modified: Mon, 11 May 2026 23:53:57 GMT  
		Size: 15.2 KB (15220 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.38-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:19af6c4fafd30c79942ce50f05f02e295c12e5b03235cdae3524693152d2297d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.1 MB (81139701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bb01df9de16a90f3948b5ece3e32033cdede92445b135f94ab92f92ba653a91`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Mon, 11 May 2026 23:53:37 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 11 May 2026 23:53:38 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 11 May 2026 23:53:44 GMT
ENV TELEGRAF_VERSION=1.38.4
# Mon, 11 May 2026 23:53:44 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 11 May 2026 23:53:44 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 11 May 2026 23:53:44 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 11 May 2026 23:53:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 11 May 2026 23:53:44 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:516037cb512d171e8192c72d6cce6bcc6520c5c810cd1897a55fad977b22648e`  
		Last Modified: Mon, 11 May 2026 23:53:58 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee16394386df16ff764f3efa01797c33a2433da101aef041fd08fc6005c2cdc6`  
		Last Modified: Mon, 11 May 2026 23:53:58 GMT  
		Size: 2.7 MB (2663399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a626a22da7deea10123bbb5b91da01956fbd43220b4895c44a51c0f606eeb453`  
		Last Modified: Mon, 11 May 2026 23:54:00 GMT  
		Size: 74.3 MB (74275535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee8a4a41e5ca652cb64623bdbe2d62a7093dc0f2b34d0959c77727c15e396aea`  
		Last Modified: Mon, 11 May 2026 23:53:58 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.38-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:2e7bcc746fce8c8515152b4009e46d0ccb46de3da94f69c8801fcc984c8309b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1169756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c6a3537a13a07028d6032f354fb67501d10d8219ccc35d65313195b862e73d3`

```dockerfile
```

-	Layers:
	-	`sha256:dac57cdea5ed6e2c983aac5dd06719625adb227c4b87bc662d57a13712de8dc0`  
		Last Modified: Mon, 11 May 2026 23:53:58 GMT  
		Size: 1.2 MB (1154414 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51e77d863cf01a81facd30cb97595935291e5ad1ceb3762e95f7082ff1fd5252`  
		Last Modified: Mon, 11 May 2026 23:53:58 GMT  
		Size: 15.3 KB (15342 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.38.4`

```console
$ docker pull telegraf@sha256:cf7f3e5c0cd7b1ee5ab69b707fe7b30e3b969c2b940f087cc84debe92ce0aae8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.38.4` - linux; amd64

```console
$ docker pull telegraf@sha256:80f0262f1764d7220207e02d4f39e2e4746a57836865f95339121c2f5d4b9319
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.0 MB (174991948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3c60b6e1594923a92cb94407321531d19377b3f65ff3d0f2b9a13618f5234b0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:40:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 23:53:40 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 23:53:41 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 11 May 2026 23:53:45 GMT
ENV TELEGRAF_VERSION=1.38.4
# Mon, 11 May 2026 23:53:45 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 11 May 2026 23:53:45 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 11 May 2026 23:53:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 11 May 2026 23:53:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 11 May 2026 23:53:45 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:9104793a826a01456b0ba567a92064e85a029816661fbb4524da7913f0123ab5`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 48.5 MB (48488676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d055cea50c88c57fc27fcd44845ebabfe5b830ea8a0a621b89d38a2b650b7ff3`  
		Last Modified: Fri, 08 May 2026 19:40:29 GMT  
		Size: 24.0 MB (24042180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc401cab11768d2b73aa0f36b0d76831b9aa4c7a568fdf9be0fa309112ef4fd4`  
		Last Modified: Mon, 11 May 2026 23:54:06 GMT  
		Size: 18.9 MB (18944282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60bf251f55455c38e3f15bed7a3f75b426f1815c5d0dce73125a3617fc770a62`  
		Last Modified: Mon, 11 May 2026 23:54:04 GMT  
		Size: 5.1 KB (5069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a720032e9b8bdb47e8f616671f2022496c72cf16644ad344541cf9d2b135a92`  
		Last Modified: Mon, 11 May 2026 23:54:07 GMT  
		Size: 83.5 MB (83511119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c19c791a0de19bd603e238311b3d1fa63543a036ff1f69d222c7e7b1dce41fd`  
		Last Modified: Mon, 11 May 2026 23:54:05 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.38.4` - unknown; unknown

```console
$ docker pull telegraf@sha256:55cbed9339d919070e63e8ec47800577b2df280770b0f6afc723190d297a3a27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6689294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4934a5127878b8d5da77a4ceb933d0c592f8332e1119e4d02ebd3205ad434146`

```dockerfile
```

-	Layers:
	-	`sha256:febb6e9adddc67a1c7ad1bc75bfbf4884cc6b32992f68ebd4f2cb60a9ed0a7e5`  
		Last Modified: Mon, 11 May 2026 23:54:05 GMT  
		Size: 6.7 MB (6674565 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ab5e4877b539a3bedcb6961e259913239cd77f99ba352bf3cb774d5fb4da89c`  
		Last Modified: Mon, 11 May 2026 23:54:04 GMT  
		Size: 14.7 KB (14729 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.38.4` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:a04f5de1f41fdc580bf27c29e7cf392a389198156eb0988abd4c83e25e675fe8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.3 MB (161287558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb1bdce67fbf4f45c1907d2d9a913aa2da7bdcaf53273d0ed34099497664685f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:44:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 23:53:44 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 23:53:45 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 11 May 2026 23:53:50 GMT
ENV TELEGRAF_VERSION=1.38.4
# Mon, 11 May 2026 23:53:50 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 11 May 2026 23:53:50 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 11 May 2026 23:53:50 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 11 May 2026 23:53:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 11 May 2026 23:53:50 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:752ba895535a5b96e621b623e0a11ff696fe28fb2110ab16de49e150423d0a89`  
		Last Modified: Fri, 08 May 2026 18:36:54 GMT  
		Size: 44.2 MB (44207696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b0504388ca2bf72a5fec3556b58015e5dce736337a948976b22cd4cce283cb0`  
		Last Modified: Fri, 08 May 2026 19:44:39 GMT  
		Size: 21.9 MB (21946392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb6eba3c782b7cc747ee4a809321eebf18d8982c91ea59720226b56cac299608`  
		Last Modified: Mon, 11 May 2026 23:54:08 GMT  
		Size: 17.7 MB (17699869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1618dd9f2c5aa795ad17b5c76403cd1d2f28c2a8a4be35ef9a3c963e71104631`  
		Last Modified: Mon, 11 May 2026 23:54:07 GMT  
		Size: 5.1 KB (5070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b47fa8118f4e1b53b666dfc2d985df74424cff2482f6f7ce3268ec8b3ef5da`  
		Last Modified: Mon, 11 May 2026 23:54:09 GMT  
		Size: 77.4 MB (77427909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac6fe4d37f249d0b62a594b3eb04746408285e8763e0b846fd7031d7e3c0a71c`  
		Last Modified: Mon, 11 May 2026 23:54:07 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.38.4` - unknown; unknown

```console
$ docker pull telegraf@sha256:7fd0f946cee5b67fc708d89eb1fbc208bdca91e28630d0f28b10bb390255286b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6683997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a209fb2471636227dac7b3f894e7f4b4d265e322ed71c06322fdff32ba436ce6`

```dockerfile
```

-	Layers:
	-	`sha256:67b856fdec15003642b567bbde1db8736a5c99300c58a08bcb65be0cc7b37850`  
		Last Modified: Mon, 11 May 2026 23:54:07 GMT  
		Size: 6.7 MB (6669170 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0572bfd71e1532ea0d65afa82546864d446b3780babb902b2406fdbd37b18a56`  
		Last Modified: Mon, 11 May 2026 23:54:07 GMT  
		Size: 14.8 KB (14827 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.38.4` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:9d5ad52e5e2b07a326e5cd0f0f064566b413335ca5704768cc173da61ffe0a2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.4 MB (165350749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba33f42f3b75c6f86298a199f6f46fa4d3c7ef629cbd4350ee11c43dd66f849b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:42:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 23:53:44 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 23:53:45 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 11 May 2026 23:53:49 GMT
ENV TELEGRAF_VERSION=1.38.4
# Mon, 11 May 2026 23:53:49 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 11 May 2026 23:53:49 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 11 May 2026 23:53:49 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 11 May 2026 23:53:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 11 May 2026 23:53:49 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:8eda28c6ece628fdff982fd6c7c1cd1f5eeccc51cfd0a3ee9155b2ccbdcc68a3`  
		Last Modified: Fri, 08 May 2026 18:24:51 GMT  
		Size: 48.4 MB (48373150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19f56578c9577bd69a05b2319baacd770a986ae61a8568047ddd91db1a1893b4`  
		Last Modified: Fri, 08 May 2026 19:42:30 GMT  
		Size: 23.6 MB (23609357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:814a8bda2fbfc42c158410ad33c204312964d366ad654eccf35597219b49b9ad`  
		Last Modified: Mon, 11 May 2026 23:54:09 GMT  
		Size: 18.9 MB (18885813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1618dd9f2c5aa795ad17b5c76403cd1d2f28c2a8a4be35ef9a3c963e71104631`  
		Last Modified: Mon, 11 May 2026 23:54:07 GMT  
		Size: 5.1 KB (5070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:472f805f5e0ffc4e1ed052f46b773ec7e7c39887926a10953189f7aafdd2b9a3`  
		Last Modified: Mon, 11 May 2026 23:54:10 GMT  
		Size: 74.5 MB (74476737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac6fe4d37f249d0b62a594b3eb04746408285e8763e0b846fd7031d7e3c0a71c`  
		Last Modified: Mon, 11 May 2026 23:54:07 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.38.4` - unknown; unknown

```console
$ docker pull telegraf@sha256:ec75681b0736c5a8ba960e031f6573f031b7a4f5a97da4eccc6905c7b57ff184
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6690104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f9a392223a61f98d69639a2ee694a7221d184761b44ccf470ed0f28654f58ec`

```dockerfile
```

-	Layers:
	-	`sha256:3128e488344cda446d4255fc7a4a85691d278f03fc0fdf963b0312b35d3b4153`  
		Last Modified: Mon, 11 May 2026 23:54:08 GMT  
		Size: 6.7 MB (6675253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74a9a55247bffe2184c7f32a22162b27d6839dc2affe61be40888960239dde1e`  
		Last Modified: Mon, 11 May 2026 23:54:08 GMT  
		Size: 14.9 KB (14851 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.38.4-alpine`

```console
$ docker pull telegraf@sha256:49fc4b3e60115966979d653e76874bd960acdd27cd484a4a57813132e474d882
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.38.4-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:c7bba96a83d3784fa69230bfa127df503fc8fb40ed96579d1577695a4ebc4049
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.8 MB (89781668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bde7e8a9f0886477eb58d149d3fdb897576a1ff2880814cec5bb3e33a87fe23`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Mon, 11 May 2026 23:53:34 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 11 May 2026 23:53:35 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 11 May 2026 23:53:41 GMT
ENV TELEGRAF_VERSION=1.38.4
# Mon, 11 May 2026 23:53:41 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 11 May 2026 23:53:41 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 11 May 2026 23:53:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 11 May 2026 23:53:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 11 May 2026 23:53:41 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:632464fc81a2417f86866f355eb404dd6fbaf95f23753e20e4aa1e267529287c`  
		Last Modified: Mon, 11 May 2026 23:53:57 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2019e1df3daf5a5b4b76e4c51b0f6852dfe81b1860b80f3453f1e6834f8b07e7`  
		Last Modified: Mon, 11 May 2026 23:53:57 GMT  
		Size: 2.6 MB (2615506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55706eb6bc48155a245fd2f96c71cb107f44fcccdd2aaa7c8a9010f4d9f3531e`  
		Last Modified: Mon, 11 May 2026 23:53:59 GMT  
		Size: 83.3 MB (83301076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e18d0f774411b978b4a6dcff56ac3efb4fe752d82ff76811fa2d292168e096ee`  
		Last Modified: Mon, 11 May 2026 23:53:57 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.38.4-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:6cfc1222edb07a0523e4a8b7d809b2cba473b87420ca92dfc9494a8e05a0249b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1174645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43e4e891c501b04fc88f432dee4f0cbe8b1a2f9fbef27a8b59b5e1c8c857b410`

```dockerfile
```

-	Layers:
	-	`sha256:87172905ac106dc4e375b2ee186d37f6d4ae3e2e57f8397ed23b9df4a4af5ef3`  
		Last Modified: Mon, 11 May 2026 23:53:57 GMT  
		Size: 1.2 MB (1159425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95634f1fdd7e204e3763697b4cc7367156ab43224e38e2c5541d394a304ed5f2`  
		Last Modified: Mon, 11 May 2026 23:53:57 GMT  
		Size: 15.2 KB (15220 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.38.4-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:19af6c4fafd30c79942ce50f05f02e295c12e5b03235cdae3524693152d2297d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.1 MB (81139701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bb01df9de16a90f3948b5ece3e32033cdede92445b135f94ab92f92ba653a91`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Mon, 11 May 2026 23:53:37 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 11 May 2026 23:53:38 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 11 May 2026 23:53:44 GMT
ENV TELEGRAF_VERSION=1.38.4
# Mon, 11 May 2026 23:53:44 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 11 May 2026 23:53:44 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 11 May 2026 23:53:44 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 11 May 2026 23:53:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 11 May 2026 23:53:44 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:516037cb512d171e8192c72d6cce6bcc6520c5c810cd1897a55fad977b22648e`  
		Last Modified: Mon, 11 May 2026 23:53:58 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee16394386df16ff764f3efa01797c33a2433da101aef041fd08fc6005c2cdc6`  
		Last Modified: Mon, 11 May 2026 23:53:58 GMT  
		Size: 2.7 MB (2663399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a626a22da7deea10123bbb5b91da01956fbd43220b4895c44a51c0f606eeb453`  
		Last Modified: Mon, 11 May 2026 23:54:00 GMT  
		Size: 74.3 MB (74275535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee8a4a41e5ca652cb64623bdbe2d62a7093dc0f2b34d0959c77727c15e396aea`  
		Last Modified: Mon, 11 May 2026 23:53:58 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.38.4-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:2e7bcc746fce8c8515152b4009e46d0ccb46de3da94f69c8801fcc984c8309b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1169756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c6a3537a13a07028d6032f354fb67501d10d8219ccc35d65313195b862e73d3`

```dockerfile
```

-	Layers:
	-	`sha256:dac57cdea5ed6e2c983aac5dd06719625adb227c4b87bc662d57a13712de8dc0`  
		Last Modified: Mon, 11 May 2026 23:53:58 GMT  
		Size: 1.2 MB (1154414 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51e77d863cf01a81facd30cb97595935291e5ad1ceb3762e95f7082ff1fd5252`  
		Last Modified: Mon, 11 May 2026 23:53:58 GMT  
		Size: 15.3 KB (15342 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:alpine`

```console
$ docker pull telegraf@sha256:49fc4b3e60115966979d653e76874bd960acdd27cd484a4a57813132e474d882
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:c7bba96a83d3784fa69230bfa127df503fc8fb40ed96579d1577695a4ebc4049
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.8 MB (89781668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bde7e8a9f0886477eb58d149d3fdb897576a1ff2880814cec5bb3e33a87fe23`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Mon, 11 May 2026 23:53:34 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 11 May 2026 23:53:35 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 11 May 2026 23:53:41 GMT
ENV TELEGRAF_VERSION=1.38.4
# Mon, 11 May 2026 23:53:41 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 11 May 2026 23:53:41 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 11 May 2026 23:53:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 11 May 2026 23:53:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 11 May 2026 23:53:41 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:632464fc81a2417f86866f355eb404dd6fbaf95f23753e20e4aa1e267529287c`  
		Last Modified: Mon, 11 May 2026 23:53:57 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2019e1df3daf5a5b4b76e4c51b0f6852dfe81b1860b80f3453f1e6834f8b07e7`  
		Last Modified: Mon, 11 May 2026 23:53:57 GMT  
		Size: 2.6 MB (2615506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55706eb6bc48155a245fd2f96c71cb107f44fcccdd2aaa7c8a9010f4d9f3531e`  
		Last Modified: Mon, 11 May 2026 23:53:59 GMT  
		Size: 83.3 MB (83301076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e18d0f774411b978b4a6dcff56ac3efb4fe752d82ff76811fa2d292168e096ee`  
		Last Modified: Mon, 11 May 2026 23:53:57 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:6cfc1222edb07a0523e4a8b7d809b2cba473b87420ca92dfc9494a8e05a0249b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1174645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43e4e891c501b04fc88f432dee4f0cbe8b1a2f9fbef27a8b59b5e1c8c857b410`

```dockerfile
```

-	Layers:
	-	`sha256:87172905ac106dc4e375b2ee186d37f6d4ae3e2e57f8397ed23b9df4a4af5ef3`  
		Last Modified: Mon, 11 May 2026 23:53:57 GMT  
		Size: 1.2 MB (1159425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95634f1fdd7e204e3763697b4cc7367156ab43224e38e2c5541d394a304ed5f2`  
		Last Modified: Mon, 11 May 2026 23:53:57 GMT  
		Size: 15.2 KB (15220 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:19af6c4fafd30c79942ce50f05f02e295c12e5b03235cdae3524693152d2297d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.1 MB (81139701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bb01df9de16a90f3948b5ece3e32033cdede92445b135f94ab92f92ba653a91`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Mon, 11 May 2026 23:53:37 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 11 May 2026 23:53:38 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 11 May 2026 23:53:44 GMT
ENV TELEGRAF_VERSION=1.38.4
# Mon, 11 May 2026 23:53:44 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 11 May 2026 23:53:44 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 11 May 2026 23:53:44 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 11 May 2026 23:53:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 11 May 2026 23:53:44 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:516037cb512d171e8192c72d6cce6bcc6520c5c810cd1897a55fad977b22648e`  
		Last Modified: Mon, 11 May 2026 23:53:58 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee16394386df16ff764f3efa01797c33a2433da101aef041fd08fc6005c2cdc6`  
		Last Modified: Mon, 11 May 2026 23:53:58 GMT  
		Size: 2.7 MB (2663399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a626a22da7deea10123bbb5b91da01956fbd43220b4895c44a51c0f606eeb453`  
		Last Modified: Mon, 11 May 2026 23:54:00 GMT  
		Size: 74.3 MB (74275535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee8a4a41e5ca652cb64623bdbe2d62a7093dc0f2b34d0959c77727c15e396aea`  
		Last Modified: Mon, 11 May 2026 23:53:58 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:2e7bcc746fce8c8515152b4009e46d0ccb46de3da94f69c8801fcc984c8309b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1169756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c6a3537a13a07028d6032f354fb67501d10d8219ccc35d65313195b862e73d3`

```dockerfile
```

-	Layers:
	-	`sha256:dac57cdea5ed6e2c983aac5dd06719625adb227c4b87bc662d57a13712de8dc0`  
		Last Modified: Mon, 11 May 2026 23:53:58 GMT  
		Size: 1.2 MB (1154414 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51e77d863cf01a81facd30cb97595935291e5ad1ceb3762e95f7082ff1fd5252`  
		Last Modified: Mon, 11 May 2026 23:53:58 GMT  
		Size: 15.3 KB (15342 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:latest`

```console
$ docker pull telegraf@sha256:cf7f3e5c0cd7b1ee5ab69b707fe7b30e3b969c2b940f087cc84debe92ce0aae8
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
$ docker pull telegraf@sha256:80f0262f1764d7220207e02d4f39e2e4746a57836865f95339121c2f5d4b9319
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.0 MB (174991948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3c60b6e1594923a92cb94407321531d19377b3f65ff3d0f2b9a13618f5234b0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:40:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 23:53:40 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 23:53:41 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 11 May 2026 23:53:45 GMT
ENV TELEGRAF_VERSION=1.38.4
# Mon, 11 May 2026 23:53:45 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 11 May 2026 23:53:45 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 11 May 2026 23:53:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 11 May 2026 23:53:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 11 May 2026 23:53:45 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:9104793a826a01456b0ba567a92064e85a029816661fbb4524da7913f0123ab5`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 48.5 MB (48488676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d055cea50c88c57fc27fcd44845ebabfe5b830ea8a0a621b89d38a2b650b7ff3`  
		Last Modified: Fri, 08 May 2026 19:40:29 GMT  
		Size: 24.0 MB (24042180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc401cab11768d2b73aa0f36b0d76831b9aa4c7a568fdf9be0fa309112ef4fd4`  
		Last Modified: Mon, 11 May 2026 23:54:06 GMT  
		Size: 18.9 MB (18944282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60bf251f55455c38e3f15bed7a3f75b426f1815c5d0dce73125a3617fc770a62`  
		Last Modified: Mon, 11 May 2026 23:54:04 GMT  
		Size: 5.1 KB (5069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a720032e9b8bdb47e8f616671f2022496c72cf16644ad344541cf9d2b135a92`  
		Last Modified: Mon, 11 May 2026 23:54:07 GMT  
		Size: 83.5 MB (83511119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c19c791a0de19bd603e238311b3d1fa63543a036ff1f69d222c7e7b1dce41fd`  
		Last Modified: Mon, 11 May 2026 23:54:05 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:55cbed9339d919070e63e8ec47800577b2df280770b0f6afc723190d297a3a27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6689294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4934a5127878b8d5da77a4ceb933d0c592f8332e1119e4d02ebd3205ad434146`

```dockerfile
```

-	Layers:
	-	`sha256:febb6e9adddc67a1c7ad1bc75bfbf4884cc6b32992f68ebd4f2cb60a9ed0a7e5`  
		Last Modified: Mon, 11 May 2026 23:54:05 GMT  
		Size: 6.7 MB (6674565 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ab5e4877b539a3bedcb6961e259913239cd77f99ba352bf3cb774d5fb4da89c`  
		Last Modified: Mon, 11 May 2026 23:54:04 GMT  
		Size: 14.7 KB (14729 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:a04f5de1f41fdc580bf27c29e7cf392a389198156eb0988abd4c83e25e675fe8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.3 MB (161287558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb1bdce67fbf4f45c1907d2d9a913aa2da7bdcaf53273d0ed34099497664685f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:44:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 23:53:44 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 23:53:45 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 11 May 2026 23:53:50 GMT
ENV TELEGRAF_VERSION=1.38.4
# Mon, 11 May 2026 23:53:50 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 11 May 2026 23:53:50 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 11 May 2026 23:53:50 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 11 May 2026 23:53:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 11 May 2026 23:53:50 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:752ba895535a5b96e621b623e0a11ff696fe28fb2110ab16de49e150423d0a89`  
		Last Modified: Fri, 08 May 2026 18:36:54 GMT  
		Size: 44.2 MB (44207696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b0504388ca2bf72a5fec3556b58015e5dce736337a948976b22cd4cce283cb0`  
		Last Modified: Fri, 08 May 2026 19:44:39 GMT  
		Size: 21.9 MB (21946392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb6eba3c782b7cc747ee4a809321eebf18d8982c91ea59720226b56cac299608`  
		Last Modified: Mon, 11 May 2026 23:54:08 GMT  
		Size: 17.7 MB (17699869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1618dd9f2c5aa795ad17b5c76403cd1d2f28c2a8a4be35ef9a3c963e71104631`  
		Last Modified: Mon, 11 May 2026 23:54:07 GMT  
		Size: 5.1 KB (5070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b47fa8118f4e1b53b666dfc2d985df74424cff2482f6f7ce3268ec8b3ef5da`  
		Last Modified: Mon, 11 May 2026 23:54:09 GMT  
		Size: 77.4 MB (77427909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac6fe4d37f249d0b62a594b3eb04746408285e8763e0b846fd7031d7e3c0a71c`  
		Last Modified: Mon, 11 May 2026 23:54:07 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:7fd0f946cee5b67fc708d89eb1fbc208bdca91e28630d0f28b10bb390255286b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6683997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a209fb2471636227dac7b3f894e7f4b4d265e322ed71c06322fdff32ba436ce6`

```dockerfile
```

-	Layers:
	-	`sha256:67b856fdec15003642b567bbde1db8736a5c99300c58a08bcb65be0cc7b37850`  
		Last Modified: Mon, 11 May 2026 23:54:07 GMT  
		Size: 6.7 MB (6669170 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0572bfd71e1532ea0d65afa82546864d446b3780babb902b2406fdbd37b18a56`  
		Last Modified: Mon, 11 May 2026 23:54:07 GMT  
		Size: 14.8 KB (14827 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:9d5ad52e5e2b07a326e5cd0f0f064566b413335ca5704768cc173da61ffe0a2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.4 MB (165350749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba33f42f3b75c6f86298a199f6f46fa4d3c7ef629cbd4350ee11c43dd66f849b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:42:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 23:53:44 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 23:53:45 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 11 May 2026 23:53:49 GMT
ENV TELEGRAF_VERSION=1.38.4
# Mon, 11 May 2026 23:53:49 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 11 May 2026 23:53:49 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 11 May 2026 23:53:49 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 11 May 2026 23:53:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 11 May 2026 23:53:49 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:8eda28c6ece628fdff982fd6c7c1cd1f5eeccc51cfd0a3ee9155b2ccbdcc68a3`  
		Last Modified: Fri, 08 May 2026 18:24:51 GMT  
		Size: 48.4 MB (48373150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19f56578c9577bd69a05b2319baacd770a986ae61a8568047ddd91db1a1893b4`  
		Last Modified: Fri, 08 May 2026 19:42:30 GMT  
		Size: 23.6 MB (23609357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:814a8bda2fbfc42c158410ad33c204312964d366ad654eccf35597219b49b9ad`  
		Last Modified: Mon, 11 May 2026 23:54:09 GMT  
		Size: 18.9 MB (18885813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1618dd9f2c5aa795ad17b5c76403cd1d2f28c2a8a4be35ef9a3c963e71104631`  
		Last Modified: Mon, 11 May 2026 23:54:07 GMT  
		Size: 5.1 KB (5070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:472f805f5e0ffc4e1ed052f46b773ec7e7c39887926a10953189f7aafdd2b9a3`  
		Last Modified: Mon, 11 May 2026 23:54:10 GMT  
		Size: 74.5 MB (74476737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac6fe4d37f249d0b62a594b3eb04746408285e8763e0b846fd7031d7e3c0a71c`  
		Last Modified: Mon, 11 May 2026 23:54:07 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:ec75681b0736c5a8ba960e031f6573f031b7a4f5a97da4eccc6905c7b57ff184
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6690104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f9a392223a61f98d69639a2ee694a7221d184761b44ccf470ed0f28654f58ec`

```dockerfile
```

-	Layers:
	-	`sha256:3128e488344cda446d4255fc7a4a85691d278f03fc0fdf963b0312b35d3b4153`  
		Last Modified: Mon, 11 May 2026 23:54:08 GMT  
		Size: 6.7 MB (6675253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74a9a55247bffe2184c7f32a22162b27d6839dc2affe61be40888960239dde1e`  
		Last Modified: Mon, 11 May 2026 23:54:08 GMT  
		Size: 14.9 KB (14851 bytes)  
		MIME: application/vnd.in-toto+json
