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
-	[`telegraf:1.38.3`](#telegraf1383)
-	[`telegraf:1.38.3-alpine`](#telegraf1383-alpine)
-	[`telegraf:alpine`](#telegrafalpine)
-	[`telegraf:latest`](#telegraflatest)

## `telegraf:1.36`

```console
$ docker pull telegraf@sha256:bf8d917a92016c39fe329539d4049c5d782c0b94525493ad47019612d15c037e
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
$ docker pull telegraf@sha256:0e6e85918f0db0ff2d534aab5025ea4b2620a3bb059bd7d77c0d826de9dc2253
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.0 MB (171954451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bdad7f9144e6aa11c7581d57a64f947ef9cc65c894f35a83fafc4fa17ba5679`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 05:00:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 05:15:19 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 05:15:20 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 22 Apr 2026 05:15:23 GMT
ENV TELEGRAF_VERSION=1.36.4
# Wed, 22 Apr 2026 05:15:23 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Wed, 22 Apr 2026 05:15:23 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Wed, 22 Apr 2026 05:15:23 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 22 Apr 2026 05:15:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 05:15:23 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:db53381ee51f9e43304e236099ba097ae1b33ae41a8007e0b6319992eb55fd00`  
		Last Modified: Wed, 22 Apr 2026 00:15:45 GMT  
		Size: 48.5 MB (48488628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5203b2bfeff92b72e816dc6cbb1f16856f0cd592e521e3c0cfa195a78fe180e`  
		Last Modified: Wed, 22 Apr 2026 05:01:15 GMT  
		Size: 24.0 MB (24042234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cefe34ac9813cf91fc35c08779b2efbf4e1de3cc646bcec4585b9c657abbca9`  
		Last Modified: Wed, 22 Apr 2026 05:15:41 GMT  
		Size: 18.9 MB (18944333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:252b6f41b470257a2a7e779f74a8acd079e87276927a78f5a1739f7ac42c2b8d`  
		Last Modified: Wed, 22 Apr 2026 05:15:40 GMT  
		Size: 5.1 KB (5073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9723e7afdf81097815b4d30d8dec28911b84157f378d41e3bad86d0b27849251`  
		Last Modified: Wed, 22 Apr 2026 05:15:42 GMT  
		Size: 80.5 MB (80473560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58a2a35f4e27972849403d23b8edc6345efeff3ba32add52a66e0402d820b222`  
		Last Modified: Wed, 22 Apr 2026 05:15:40 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36` - unknown; unknown

```console
$ docker pull telegraf@sha256:aaaf8df1837f03220d570aa4f09631b00f428b36c5eb69f98a9020af947d1038
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6670530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:197edcd75fa4640610ccc26bbb3c4d8856cac06c2aa7f092f77c1ac300e11078`

```dockerfile
```

-	Layers:
	-	`sha256:38d886380b63c5b88eed0c38c9f78b5efbc21fa39a229bb91bd939a90efe8881`  
		Last Modified: Wed, 22 Apr 2026 05:15:40 GMT  
		Size: 6.7 MB (6656103 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3cbf04768886ec7c24514209f32bd7b310c2af2120e3264907ff3b1233c7aa03`  
		Last Modified: Wed, 22 Apr 2026 05:15:40 GMT  
		Size: 14.4 KB (14427 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.36` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:5fee6ca1cae731516f93d087945c41bccca47aba80445b8379f7720d42a70ba9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.8 MB (157823044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d87e84cbbb60660af53b33713d205391a4944b6ac98905c2de792a66ad8e1dee`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 02:18:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 04:04:03 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 04:04:04 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 22 Apr 2026 04:04:10 GMT
ENV TELEGRAF_VERSION=1.36.4
# Wed, 22 Apr 2026 04:04:10 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Wed, 22 Apr 2026 04:04:10 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Wed, 22 Apr 2026 04:04:11 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 22 Apr 2026 04:04:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 04:04:11 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:a78e7b2123c5c35e65ee1cc17df0d11c1db8ab3c4fe80b457270c2d9ae5003b1`  
		Last Modified: Wed, 22 Apr 2026 00:16:29 GMT  
		Size: 44.2 MB (44207655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:218160481dc948cfbf943718a4363de6a3663997f19a965c7b86136ac3e28f30`  
		Last Modified: Wed, 22 Apr 2026 02:18:15 GMT  
		Size: 21.9 MB (21946340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e50f3fe9427265a744330430310e8f573afb11464ba8b1f918bde4073acd49e2`  
		Last Modified: Wed, 22 Apr 2026 04:04:28 GMT  
		Size: 17.7 MB (17699708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed529d42cb9bafeb0f5406594de356c1bb6cec52ea62a8ff7d9b849a63bb0e04`  
		Last Modified: Wed, 22 Apr 2026 04:04:27 GMT  
		Size: 5.1 KB (5071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59146bc0dc3f1c8716791326349ee546a4956c98633165bba543ec841cb67afd`  
		Last Modified: Wed, 22 Apr 2026 04:04:29 GMT  
		Size: 74.0 MB (73963646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ec49bf1c7df8e4cdc502a78e1a14f7db33f1fd9194a32302e8d2e6bf5081eac`  
		Last Modified: Wed, 22 Apr 2026 04:04:27 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36` - unknown; unknown

```console
$ docker pull telegraf@sha256:5ce66a1389036f0ba486edd81bbed8a5736104e8fc300b6e556e6ef5b0d7b522
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6665217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f8f26f4690076a142597add3bfdcb27dc5babd21c9f297da25ac659fdcbd51e`

```dockerfile
```

-	Layers:
	-	`sha256:b3af3feb30ae1b2548a7749dd48fef724e72fff9338b2c1ce8b3d1ca273136a4`  
		Last Modified: Wed, 22 Apr 2026 04:04:27 GMT  
		Size: 6.7 MB (6650700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6d8d9f757c686cd74be216ae7945de65d398721ca1a34bead95d275739c0d8d`  
		Last Modified: Wed, 22 Apr 2026 04:04:27 GMT  
		Size: 14.5 KB (14517 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.36` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:f940bb839b4e778849bb295528fac00dace70b10148ba7a044368a4b293a4431
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.7 MB (162674411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fd1db3de0e9885ad6419d40eaafbdb9efdea273b2e9f74a5312c3ee3a3c8a9a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:42:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:45:00 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:45:01 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 22 Apr 2026 02:45:07 GMT
ENV TELEGRAF_VERSION=1.36.4
# Wed, 22 Apr 2026 02:45:07 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Wed, 22 Apr 2026 02:45:07 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Wed, 22 Apr 2026 02:45:07 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 22 Apr 2026 02:45:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 02:45:07 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:30de66f8fdafab67e88d876087f571a693a1a6c4cf0abc29efbf88ea878e0d29`  
		Last Modified: Wed, 22 Apr 2026 00:15:43 GMT  
		Size: 48.4 MB (48373071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bb7bd28fbdfe678a7f45878b7b1c07dbbc0fa7753b0312aa8fd049667a9e137`  
		Last Modified: Wed, 22 Apr 2026 01:43:06 GMT  
		Size: 23.6 MB (23609423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5ced485666dc02eeaf6a1d3c0ba3301d4157979b102ac809b01db0e00fe0665`  
		Last Modified: Wed, 22 Apr 2026 02:45:26 GMT  
		Size: 18.9 MB (18885865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0259d1308abc26a318f8c1e85bf3a6b21299489dccafd5d335a5851de1fb4fe5`  
		Last Modified: Wed, 22 Apr 2026 02:45:25 GMT  
		Size: 5.1 KB (5072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85d1d25f3029279cb9ea7f06c205860b2c42090a2ae44718e4d2ecde8a914102`  
		Last Modified: Wed, 22 Apr 2026 02:45:29 GMT  
		Size: 71.8 MB (71800355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cc6b44f2c40299caae7c53f039ee77c09278f8470246bed15f7d6dd7ad2af60`  
		Last Modified: Wed, 22 Apr 2026 02:45:25 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36` - unknown; unknown

```console
$ docker pull telegraf@sha256:45631e31a2e5dcc443b6b23082644eb3c35b155e31b9cb3154a171dd459317ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6671316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdb953e08a3564a108dbac4f385cdb96e34e4073ce1ff6ec87df772891fb2425`

```dockerfile
```

-	Layers:
	-	`sha256:e9c55b284afe83754eacdd0adbe9ff25856b2123750115f1895976c44b17efc1`  
		Last Modified: Wed, 22 Apr 2026 02:45:25 GMT  
		Size: 6.7 MB (6656779 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d01fd8b860f2cc3a70552d3be6881aa005230da2194a9fce7fc5977875868bf9`  
		Last Modified: Wed, 22 Apr 2026 02:45:25 GMT  
		Size: 14.5 KB (14537 bytes)  
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
$ docker pull telegraf@sha256:bf8d917a92016c39fe329539d4049c5d782c0b94525493ad47019612d15c037e
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
$ docker pull telegraf@sha256:0e6e85918f0db0ff2d534aab5025ea4b2620a3bb059bd7d77c0d826de9dc2253
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.0 MB (171954451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bdad7f9144e6aa11c7581d57a64f947ef9cc65c894f35a83fafc4fa17ba5679`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 05:00:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 05:15:19 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 05:15:20 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 22 Apr 2026 05:15:23 GMT
ENV TELEGRAF_VERSION=1.36.4
# Wed, 22 Apr 2026 05:15:23 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Wed, 22 Apr 2026 05:15:23 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Wed, 22 Apr 2026 05:15:23 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 22 Apr 2026 05:15:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 05:15:23 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:db53381ee51f9e43304e236099ba097ae1b33ae41a8007e0b6319992eb55fd00`  
		Last Modified: Wed, 22 Apr 2026 00:15:45 GMT  
		Size: 48.5 MB (48488628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5203b2bfeff92b72e816dc6cbb1f16856f0cd592e521e3c0cfa195a78fe180e`  
		Last Modified: Wed, 22 Apr 2026 05:01:15 GMT  
		Size: 24.0 MB (24042234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cefe34ac9813cf91fc35c08779b2efbf4e1de3cc646bcec4585b9c657abbca9`  
		Last Modified: Wed, 22 Apr 2026 05:15:41 GMT  
		Size: 18.9 MB (18944333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:252b6f41b470257a2a7e779f74a8acd079e87276927a78f5a1739f7ac42c2b8d`  
		Last Modified: Wed, 22 Apr 2026 05:15:40 GMT  
		Size: 5.1 KB (5073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9723e7afdf81097815b4d30d8dec28911b84157f378d41e3bad86d0b27849251`  
		Last Modified: Wed, 22 Apr 2026 05:15:42 GMT  
		Size: 80.5 MB (80473560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58a2a35f4e27972849403d23b8edc6345efeff3ba32add52a66e0402d820b222`  
		Last Modified: Wed, 22 Apr 2026 05:15:40 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36.4` - unknown; unknown

```console
$ docker pull telegraf@sha256:aaaf8df1837f03220d570aa4f09631b00f428b36c5eb69f98a9020af947d1038
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6670530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:197edcd75fa4640610ccc26bbb3c4d8856cac06c2aa7f092f77c1ac300e11078`

```dockerfile
```

-	Layers:
	-	`sha256:38d886380b63c5b88eed0c38c9f78b5efbc21fa39a229bb91bd939a90efe8881`  
		Last Modified: Wed, 22 Apr 2026 05:15:40 GMT  
		Size: 6.7 MB (6656103 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3cbf04768886ec7c24514209f32bd7b310c2af2120e3264907ff3b1233c7aa03`  
		Last Modified: Wed, 22 Apr 2026 05:15:40 GMT  
		Size: 14.4 KB (14427 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.36.4` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:5fee6ca1cae731516f93d087945c41bccca47aba80445b8379f7720d42a70ba9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.8 MB (157823044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d87e84cbbb60660af53b33713d205391a4944b6ac98905c2de792a66ad8e1dee`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 02:18:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 04:04:03 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 04:04:04 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 22 Apr 2026 04:04:10 GMT
ENV TELEGRAF_VERSION=1.36.4
# Wed, 22 Apr 2026 04:04:10 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Wed, 22 Apr 2026 04:04:10 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Wed, 22 Apr 2026 04:04:11 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 22 Apr 2026 04:04:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 04:04:11 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:a78e7b2123c5c35e65ee1cc17df0d11c1db8ab3c4fe80b457270c2d9ae5003b1`  
		Last Modified: Wed, 22 Apr 2026 00:16:29 GMT  
		Size: 44.2 MB (44207655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:218160481dc948cfbf943718a4363de6a3663997f19a965c7b86136ac3e28f30`  
		Last Modified: Wed, 22 Apr 2026 02:18:15 GMT  
		Size: 21.9 MB (21946340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e50f3fe9427265a744330430310e8f573afb11464ba8b1f918bde4073acd49e2`  
		Last Modified: Wed, 22 Apr 2026 04:04:28 GMT  
		Size: 17.7 MB (17699708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed529d42cb9bafeb0f5406594de356c1bb6cec52ea62a8ff7d9b849a63bb0e04`  
		Last Modified: Wed, 22 Apr 2026 04:04:27 GMT  
		Size: 5.1 KB (5071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59146bc0dc3f1c8716791326349ee546a4956c98633165bba543ec841cb67afd`  
		Last Modified: Wed, 22 Apr 2026 04:04:29 GMT  
		Size: 74.0 MB (73963646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ec49bf1c7df8e4cdc502a78e1a14f7db33f1fd9194a32302e8d2e6bf5081eac`  
		Last Modified: Wed, 22 Apr 2026 04:04:27 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36.4` - unknown; unknown

```console
$ docker pull telegraf@sha256:5ce66a1389036f0ba486edd81bbed8a5736104e8fc300b6e556e6ef5b0d7b522
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6665217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f8f26f4690076a142597add3bfdcb27dc5babd21c9f297da25ac659fdcbd51e`

```dockerfile
```

-	Layers:
	-	`sha256:b3af3feb30ae1b2548a7749dd48fef724e72fff9338b2c1ce8b3d1ca273136a4`  
		Last Modified: Wed, 22 Apr 2026 04:04:27 GMT  
		Size: 6.7 MB (6650700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6d8d9f757c686cd74be216ae7945de65d398721ca1a34bead95d275739c0d8d`  
		Last Modified: Wed, 22 Apr 2026 04:04:27 GMT  
		Size: 14.5 KB (14517 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.36.4` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:f940bb839b4e778849bb295528fac00dace70b10148ba7a044368a4b293a4431
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.7 MB (162674411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fd1db3de0e9885ad6419d40eaafbdb9efdea273b2e9f74a5312c3ee3a3c8a9a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:42:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:45:00 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:45:01 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 22 Apr 2026 02:45:07 GMT
ENV TELEGRAF_VERSION=1.36.4
# Wed, 22 Apr 2026 02:45:07 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Wed, 22 Apr 2026 02:45:07 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Wed, 22 Apr 2026 02:45:07 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 22 Apr 2026 02:45:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 02:45:07 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:30de66f8fdafab67e88d876087f571a693a1a6c4cf0abc29efbf88ea878e0d29`  
		Last Modified: Wed, 22 Apr 2026 00:15:43 GMT  
		Size: 48.4 MB (48373071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bb7bd28fbdfe678a7f45878b7b1c07dbbc0fa7753b0312aa8fd049667a9e137`  
		Last Modified: Wed, 22 Apr 2026 01:43:06 GMT  
		Size: 23.6 MB (23609423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5ced485666dc02eeaf6a1d3c0ba3301d4157979b102ac809b01db0e00fe0665`  
		Last Modified: Wed, 22 Apr 2026 02:45:26 GMT  
		Size: 18.9 MB (18885865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0259d1308abc26a318f8c1e85bf3a6b21299489dccafd5d335a5851de1fb4fe5`  
		Last Modified: Wed, 22 Apr 2026 02:45:25 GMT  
		Size: 5.1 KB (5072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85d1d25f3029279cb9ea7f06c205860b2c42090a2ae44718e4d2ecde8a914102`  
		Last Modified: Wed, 22 Apr 2026 02:45:29 GMT  
		Size: 71.8 MB (71800355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cc6b44f2c40299caae7c53f039ee77c09278f8470246bed15f7d6dd7ad2af60`  
		Last Modified: Wed, 22 Apr 2026 02:45:25 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36.4` - unknown; unknown

```console
$ docker pull telegraf@sha256:45631e31a2e5dcc443b6b23082644eb3c35b155e31b9cb3154a171dd459317ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6671316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdb953e08a3564a108dbac4f385cdb96e34e4073ce1ff6ec87df772891fb2425`

```dockerfile
```

-	Layers:
	-	`sha256:e9c55b284afe83754eacdd0adbe9ff25856b2123750115f1895976c44b17efc1`  
		Last Modified: Wed, 22 Apr 2026 02:45:25 GMT  
		Size: 6.7 MB (6656779 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d01fd8b860f2cc3a70552d3be6881aa005230da2194a9fce7fc5977875868bf9`  
		Last Modified: Wed, 22 Apr 2026 02:45:25 GMT  
		Size: 14.5 KB (14537 bytes)  
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
$ docker pull telegraf@sha256:0e8acc517d492600ca7af650199563c26aa4ec0ffe4bafce41b75964f6fe448f
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
$ docker pull telegraf@sha256:60db0772b246ce34a5c785f018bbb8ead1a31ea26f030bd46413601d1f2953ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.3 MB (172264105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:491e9217641a06fd90d46291bcdeec308493a259cc5887556ff58fdd119a9df6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 05:00:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 05:15:19 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 05:15:20 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 22 Apr 2026 05:15:51 GMT
ENV TELEGRAF_VERSION=1.37.3
# Wed, 22 Apr 2026 05:15:51 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Wed, 22 Apr 2026 05:15:51 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Wed, 22 Apr 2026 05:15:51 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 22 Apr 2026 05:15:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 05:15:51 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:db53381ee51f9e43304e236099ba097ae1b33ae41a8007e0b6319992eb55fd00`  
		Last Modified: Wed, 22 Apr 2026 00:15:45 GMT  
		Size: 48.5 MB (48488628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5203b2bfeff92b72e816dc6cbb1f16856f0cd592e521e3c0cfa195a78fe180e`  
		Last Modified: Wed, 22 Apr 2026 05:01:15 GMT  
		Size: 24.0 MB (24042234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cefe34ac9813cf91fc35c08779b2efbf4e1de3cc646bcec4585b9c657abbca9`  
		Last Modified: Wed, 22 Apr 2026 05:15:41 GMT  
		Size: 18.9 MB (18944333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:252b6f41b470257a2a7e779f74a8acd079e87276927a78f5a1739f7ac42c2b8d`  
		Last Modified: Wed, 22 Apr 2026 05:15:40 GMT  
		Size: 5.1 KB (5073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54de11fe6c2337fc8063bd80900fdccfa5dcd783c32be80d750108d780ab1fca`  
		Last Modified: Wed, 22 Apr 2026 05:16:10 GMT  
		Size: 80.8 MB (80783214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d006494f26e2495076dfdf7614aa283386181170ed9ef1d7624ee53d56240b1`  
		Last Modified: Wed, 22 Apr 2026 05:16:08 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.37` - unknown; unknown

```console
$ docker pull telegraf@sha256:6e0123137e378edd9730802877cd0be6134b78767780f82ae053c4d07463b19e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6681385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1ddb249fa537ed98fdfeb3cf9d749591d1233f2c57a52454a6375e31341b014`

```dockerfile
```

-	Layers:
	-	`sha256:4e3f7d3575bfd375445ed2bf77f374a997abc2e18118bf11affa02a4e17cf5b3`  
		Last Modified: Wed, 22 Apr 2026 05:16:08 GMT  
		Size: 6.7 MB (6666958 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84b353d3b3d8a8d8c6e877f94794990dc65c908dd326dc5433a3856e2a14cb60`  
		Last Modified: Wed, 22 Apr 2026 05:16:08 GMT  
		Size: 14.4 KB (14427 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.37` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:85687743be9a30b7d2c0212ad4367263559d98a88803838d69f50e3075177e76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.5 MB (158476942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7720427eb3a8521191b9064c2c96c85385b922de9ec5d661c26c89159e8ff064`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 02:18:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 04:04:33 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 04:04:34 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 22 Apr 2026 04:04:41 GMT
ENV TELEGRAF_VERSION=1.37.3
# Wed, 22 Apr 2026 04:04:41 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Wed, 22 Apr 2026 04:04:41 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Wed, 22 Apr 2026 04:04:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 22 Apr 2026 04:04:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 04:04:41 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:a78e7b2123c5c35e65ee1cc17df0d11c1db8ab3c4fe80b457270c2d9ae5003b1`  
		Last Modified: Wed, 22 Apr 2026 00:16:29 GMT  
		Size: 44.2 MB (44207655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:218160481dc948cfbf943718a4363de6a3663997f19a965c7b86136ac3e28f30`  
		Last Modified: Wed, 22 Apr 2026 02:18:15 GMT  
		Size: 21.9 MB (21946340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f7856e52010a1e73ab5b014b98af258ab8dc423feb38088fa470a5e6a91e4bc`  
		Last Modified: Wed, 22 Apr 2026 04:05:02 GMT  
		Size: 17.7 MB (17699825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0454abd4fea266919a3e5afeea7421151dfdafbfb6e894107cc557d35a61460`  
		Last Modified: Wed, 22 Apr 2026 04:05:01 GMT  
		Size: 5.1 KB (5070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:067de9cc77b71037bbde9609176369180cfbb29d134b51d838d4e950a9664ffd`  
		Last Modified: Wed, 22 Apr 2026 04:05:04 GMT  
		Size: 74.6 MB (74617428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3f576290e1af8cf828d77e14667af0104dcac413cc23c8ab3bd85610535bd25`  
		Last Modified: Wed, 22 Apr 2026 04:05:01 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.37` - unknown; unknown

```console
$ docker pull telegraf@sha256:4cb823f6b9fc5986439cca743b405bcfc765fdef0d4481f41fb83dfd0f0d0c11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6676072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0e4959dc1c41e85b3c59695a9b9146a15f84b0a5328e4c0ddb56e8e6ecae70d`

```dockerfile
```

-	Layers:
	-	`sha256:9a5947290847f131f1158e43398626bca62d56ecbab9cb410083e521799dd20f`  
		Last Modified: Wed, 22 Apr 2026 04:05:01 GMT  
		Size: 6.7 MB (6661555 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be2f551ae2ee0c545106dd023ebe918c2471b83996c2b1cc382c4f7048d283aa`  
		Last Modified: Wed, 22 Apr 2026 04:05:01 GMT  
		Size: 14.5 KB (14517 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.37` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:dece3919d373f039700c2cbf86e6d356003a503934ad42730833dbdc148e2843
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.0 MB (163045032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c507b757424ce43ebc2c34597d596f5722389018562f49add7d899362872213`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:42:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:45:26 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:45:27 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 22 Apr 2026 02:45:30 GMT
ENV TELEGRAF_VERSION=1.37.3
# Wed, 22 Apr 2026 02:45:30 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Wed, 22 Apr 2026 02:45:30 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Wed, 22 Apr 2026 02:45:30 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 22 Apr 2026 02:45:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 02:45:30 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:30de66f8fdafab67e88d876087f571a693a1a6c4cf0abc29efbf88ea878e0d29`  
		Last Modified: Wed, 22 Apr 2026 00:15:43 GMT  
		Size: 48.4 MB (48373071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bb7bd28fbdfe678a7f45878b7b1c07dbbc0fa7753b0312aa8fd049667a9e137`  
		Last Modified: Wed, 22 Apr 2026 01:43:06 GMT  
		Size: 23.6 MB (23609423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae6b123277b7c8ca78ad159a1676310edb5bcffbc21fbda2b0368d0654e9955d`  
		Last Modified: Wed, 22 Apr 2026 02:45:51 GMT  
		Size: 18.9 MB (18885862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2cc22c655a0edd71d8d9ec069a51c8b62f4a9f304a5a46503d56d15169758cb`  
		Last Modified: Wed, 22 Apr 2026 02:45:50 GMT  
		Size: 5.1 KB (5069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f269e0af6748ec01e5c0360e1d44b72f5bfbf6f57f518c3e19080c8167885929`  
		Last Modified: Wed, 22 Apr 2026 02:45:53 GMT  
		Size: 72.2 MB (72170984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bef9e2f2bb83c02fd35982cce3e47cd67b8e7ebff1b4b8f858483c025c969f3`  
		Last Modified: Wed, 22 Apr 2026 02:45:50 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.37` - unknown; unknown

```console
$ docker pull telegraf@sha256:a634aa612787a90bf756ec084a22339d7a17d139595ccb73e35413f5c618970d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6682170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a85a51b1c27ccaf7789a2f085a9f670c72b6a99c7f049679c29fdb1a59c257d5`

```dockerfile
```

-	Layers:
	-	`sha256:85fd8b41f76cfb3972241481296f2d221545a7b7537a675bcf48e039cf9cef40`  
		Last Modified: Wed, 22 Apr 2026 02:45:50 GMT  
		Size: 6.7 MB (6667634 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dcc52d98b13a142a3ce6f415f129c7acf3ae0ca7080eb937829b3cef5188a5de`  
		Last Modified: Wed, 22 Apr 2026 02:45:50 GMT  
		Size: 14.5 KB (14536 bytes)  
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
$ docker pull telegraf@sha256:0e8acc517d492600ca7af650199563c26aa4ec0ffe4bafce41b75964f6fe448f
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
$ docker pull telegraf@sha256:60db0772b246ce34a5c785f018bbb8ead1a31ea26f030bd46413601d1f2953ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.3 MB (172264105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:491e9217641a06fd90d46291bcdeec308493a259cc5887556ff58fdd119a9df6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 05:00:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 05:15:19 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 05:15:20 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 22 Apr 2026 05:15:51 GMT
ENV TELEGRAF_VERSION=1.37.3
# Wed, 22 Apr 2026 05:15:51 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Wed, 22 Apr 2026 05:15:51 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Wed, 22 Apr 2026 05:15:51 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 22 Apr 2026 05:15:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 05:15:51 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:db53381ee51f9e43304e236099ba097ae1b33ae41a8007e0b6319992eb55fd00`  
		Last Modified: Wed, 22 Apr 2026 00:15:45 GMT  
		Size: 48.5 MB (48488628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5203b2bfeff92b72e816dc6cbb1f16856f0cd592e521e3c0cfa195a78fe180e`  
		Last Modified: Wed, 22 Apr 2026 05:01:15 GMT  
		Size: 24.0 MB (24042234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cefe34ac9813cf91fc35c08779b2efbf4e1de3cc646bcec4585b9c657abbca9`  
		Last Modified: Wed, 22 Apr 2026 05:15:41 GMT  
		Size: 18.9 MB (18944333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:252b6f41b470257a2a7e779f74a8acd079e87276927a78f5a1739f7ac42c2b8d`  
		Last Modified: Wed, 22 Apr 2026 05:15:40 GMT  
		Size: 5.1 KB (5073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54de11fe6c2337fc8063bd80900fdccfa5dcd783c32be80d750108d780ab1fca`  
		Last Modified: Wed, 22 Apr 2026 05:16:10 GMT  
		Size: 80.8 MB (80783214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d006494f26e2495076dfdf7614aa283386181170ed9ef1d7624ee53d56240b1`  
		Last Modified: Wed, 22 Apr 2026 05:16:08 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.37.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:6e0123137e378edd9730802877cd0be6134b78767780f82ae053c4d07463b19e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6681385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1ddb249fa537ed98fdfeb3cf9d749591d1233f2c57a52454a6375e31341b014`

```dockerfile
```

-	Layers:
	-	`sha256:4e3f7d3575bfd375445ed2bf77f374a997abc2e18118bf11affa02a4e17cf5b3`  
		Last Modified: Wed, 22 Apr 2026 05:16:08 GMT  
		Size: 6.7 MB (6666958 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84b353d3b3d8a8d8c6e877f94794990dc65c908dd326dc5433a3856e2a14cb60`  
		Last Modified: Wed, 22 Apr 2026 05:16:08 GMT  
		Size: 14.4 KB (14427 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.37.3` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:85687743be9a30b7d2c0212ad4367263559d98a88803838d69f50e3075177e76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.5 MB (158476942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7720427eb3a8521191b9064c2c96c85385b922de9ec5d661c26c89159e8ff064`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 02:18:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 04:04:33 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 04:04:34 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 22 Apr 2026 04:04:41 GMT
ENV TELEGRAF_VERSION=1.37.3
# Wed, 22 Apr 2026 04:04:41 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Wed, 22 Apr 2026 04:04:41 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Wed, 22 Apr 2026 04:04:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 22 Apr 2026 04:04:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 04:04:41 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:a78e7b2123c5c35e65ee1cc17df0d11c1db8ab3c4fe80b457270c2d9ae5003b1`  
		Last Modified: Wed, 22 Apr 2026 00:16:29 GMT  
		Size: 44.2 MB (44207655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:218160481dc948cfbf943718a4363de6a3663997f19a965c7b86136ac3e28f30`  
		Last Modified: Wed, 22 Apr 2026 02:18:15 GMT  
		Size: 21.9 MB (21946340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f7856e52010a1e73ab5b014b98af258ab8dc423feb38088fa470a5e6a91e4bc`  
		Last Modified: Wed, 22 Apr 2026 04:05:02 GMT  
		Size: 17.7 MB (17699825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0454abd4fea266919a3e5afeea7421151dfdafbfb6e894107cc557d35a61460`  
		Last Modified: Wed, 22 Apr 2026 04:05:01 GMT  
		Size: 5.1 KB (5070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:067de9cc77b71037bbde9609176369180cfbb29d134b51d838d4e950a9664ffd`  
		Last Modified: Wed, 22 Apr 2026 04:05:04 GMT  
		Size: 74.6 MB (74617428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3f576290e1af8cf828d77e14667af0104dcac413cc23c8ab3bd85610535bd25`  
		Last Modified: Wed, 22 Apr 2026 04:05:01 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.37.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:4cb823f6b9fc5986439cca743b405bcfc765fdef0d4481f41fb83dfd0f0d0c11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6676072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0e4959dc1c41e85b3c59695a9b9146a15f84b0a5328e4c0ddb56e8e6ecae70d`

```dockerfile
```

-	Layers:
	-	`sha256:9a5947290847f131f1158e43398626bca62d56ecbab9cb410083e521799dd20f`  
		Last Modified: Wed, 22 Apr 2026 04:05:01 GMT  
		Size: 6.7 MB (6661555 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be2f551ae2ee0c545106dd023ebe918c2471b83996c2b1cc382c4f7048d283aa`  
		Last Modified: Wed, 22 Apr 2026 04:05:01 GMT  
		Size: 14.5 KB (14517 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.37.3` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:dece3919d373f039700c2cbf86e6d356003a503934ad42730833dbdc148e2843
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.0 MB (163045032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c507b757424ce43ebc2c34597d596f5722389018562f49add7d899362872213`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:42:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:45:26 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:45:27 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 22 Apr 2026 02:45:30 GMT
ENV TELEGRAF_VERSION=1.37.3
# Wed, 22 Apr 2026 02:45:30 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Wed, 22 Apr 2026 02:45:30 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Wed, 22 Apr 2026 02:45:30 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 22 Apr 2026 02:45:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 02:45:30 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:30de66f8fdafab67e88d876087f571a693a1a6c4cf0abc29efbf88ea878e0d29`  
		Last Modified: Wed, 22 Apr 2026 00:15:43 GMT  
		Size: 48.4 MB (48373071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bb7bd28fbdfe678a7f45878b7b1c07dbbc0fa7753b0312aa8fd049667a9e137`  
		Last Modified: Wed, 22 Apr 2026 01:43:06 GMT  
		Size: 23.6 MB (23609423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae6b123277b7c8ca78ad159a1676310edb5bcffbc21fbda2b0368d0654e9955d`  
		Last Modified: Wed, 22 Apr 2026 02:45:51 GMT  
		Size: 18.9 MB (18885862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2cc22c655a0edd71d8d9ec069a51c8b62f4a9f304a5a46503d56d15169758cb`  
		Last Modified: Wed, 22 Apr 2026 02:45:50 GMT  
		Size: 5.1 KB (5069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f269e0af6748ec01e5c0360e1d44b72f5bfbf6f57f518c3e19080c8167885929`  
		Last Modified: Wed, 22 Apr 2026 02:45:53 GMT  
		Size: 72.2 MB (72170984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bef9e2f2bb83c02fd35982cce3e47cd67b8e7ebff1b4b8f858483c025c969f3`  
		Last Modified: Wed, 22 Apr 2026 02:45:50 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.37.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:a634aa612787a90bf756ec084a22339d7a17d139595ccb73e35413f5c618970d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6682170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a85a51b1c27ccaf7789a2f085a9f670c72b6a99c7f049679c29fdb1a59c257d5`

```dockerfile
```

-	Layers:
	-	`sha256:85fd8b41f76cfb3972241481296f2d221545a7b7537a675bcf48e039cf9cef40`  
		Last Modified: Wed, 22 Apr 2026 02:45:50 GMT  
		Size: 6.7 MB (6667634 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dcc52d98b13a142a3ce6f415f129c7acf3ae0ca7080eb937829b3cef5188a5de`  
		Last Modified: Wed, 22 Apr 2026 02:45:50 GMT  
		Size: 14.5 KB (14536 bytes)  
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
$ docker pull telegraf@sha256:88eb354ac9926d70791b70558d69644b527b3c7e6f02c2af9165038a3e306a6d
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
$ docker pull telegraf@sha256:3278cab4b3ba80a90e2de385a9855dd4e3500c891025a982e1c5dc51f57f1c56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.5 MB (174547969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2e6dfa7b8ce8f5cc1bd36dafe5ee923713b0fc0ddf123ecd310ce4102ee7aaf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 05:00:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 05:16:10 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 05:16:11 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 22 Apr 2026 05:16:15 GMT
ENV TELEGRAF_VERSION=1.38.3
# Wed, 22 Apr 2026 05:16:15 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Wed, 22 Apr 2026 05:16:15 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Wed, 22 Apr 2026 05:16:15 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 22 Apr 2026 05:16:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 05:16:15 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:db53381ee51f9e43304e236099ba097ae1b33ae41a8007e0b6319992eb55fd00`  
		Last Modified: Wed, 22 Apr 2026 00:15:45 GMT  
		Size: 48.5 MB (48488628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5203b2bfeff92b72e816dc6cbb1f16856f0cd592e521e3c0cfa195a78fe180e`  
		Last Modified: Wed, 22 Apr 2026 05:01:15 GMT  
		Size: 24.0 MB (24042234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8acdaa6f91c9ba4895ddb392aae95bc41fff1e0597f39b3d6a96b67500de023c`  
		Last Modified: Wed, 22 Apr 2026 05:16:34 GMT  
		Size: 18.9 MB (18944330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb77e8a73df98439739f415dd132afbece308e0c5d694a0d38a765e4904aa86e`  
		Last Modified: Wed, 22 Apr 2026 05:16:33 GMT  
		Size: 5.1 KB (5070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f40d61eeb10ad19b0c1deeee0bcba32c309264ff42136064ada8798f128faa09`  
		Last Modified: Wed, 22 Apr 2026 05:16:36 GMT  
		Size: 83.1 MB (83067082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59a33f3a5d60285ac12d5a9eeeab3f92064752300d3b3a75fcd16b90c8b3e322`  
		Last Modified: Wed, 22 Apr 2026 05:16:33 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.38` - unknown; unknown

```console
$ docker pull telegraf@sha256:6293af4bad25705a78b1dc84924547003b1863bcc59474e92bbb515d97ae81da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6690845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:930334ea18d85ba05593bd839e27a887835513365d5cc0f56b5d8a88e95e131a`

```dockerfile
```

-	Layers:
	-	`sha256:e81c19a14633e8727bea8c55b5630657691a6ea57998e353bd2edd623e295b91`  
		Last Modified: Wed, 22 Apr 2026 05:16:33 GMT  
		Size: 6.7 MB (6676117 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:193bd5147cc76d0e7667bc71ddaeafcd0990ea9a4498d2c42eb4e96b0f015b2c`  
		Last Modified: Wed, 22 Apr 2026 05:16:33 GMT  
		Size: 14.7 KB (14728 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.38` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:9c34d13f45a6fe087e8b762d8fefb174b7aedfe46c8b0f066e2fd3a26a4671ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.8 MB (160829606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb782f542da35921cd1cd23f40605441990d7123ba00a1df765769174ca50bef`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 02:18:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 04:04:35 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 04:04:35 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 22 Apr 2026 04:04:40 GMT
ENV TELEGRAF_VERSION=1.38.3
# Wed, 22 Apr 2026 04:04:40 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Wed, 22 Apr 2026 04:04:40 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Wed, 22 Apr 2026 04:04:40 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 22 Apr 2026 04:04:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 04:04:40 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:a78e7b2123c5c35e65ee1cc17df0d11c1db8ab3c4fe80b457270c2d9ae5003b1`  
		Last Modified: Wed, 22 Apr 2026 00:16:29 GMT  
		Size: 44.2 MB (44207655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:218160481dc948cfbf943718a4363de6a3663997f19a965c7b86136ac3e28f30`  
		Last Modified: Wed, 22 Apr 2026 02:18:15 GMT  
		Size: 21.9 MB (21946340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9742f40fc9d5bb902bd77ee1549e0c0815816441cf37052058bb32ebee0e18ec`  
		Last Modified: Wed, 22 Apr 2026 04:04:59 GMT  
		Size: 17.7 MB (17699933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8726f263804a6205f42456a2db18b58eac1f997dee87aa0a54c367d66366f8b8`  
		Last Modified: Wed, 22 Apr 2026 04:04:58 GMT  
		Size: 5.1 KB (5055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef5c472b4f00d8e1d0623d3c9cdb5bbb924e15ca10c0492d280a152d76a43b60`  
		Last Modified: Wed, 22 Apr 2026 04:05:01 GMT  
		Size: 77.0 MB (76969998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e12d49f366146ec8630190da0ccf729e6d970e44bce60ea1f65670cdf0544b9`  
		Last Modified: Wed, 22 Apr 2026 04:04:58 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.38` - unknown; unknown

```console
$ docker pull telegraf@sha256:6f5b5648c87d352bde9bd712fed1e666268fa06c582a8dae4f4f75df99b9d89d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6685549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ccf4b491558cbb21acf76bd1a280a051f07701fbc5bc25832ba635179b1b8f2`

```dockerfile
```

-	Layers:
	-	`sha256:20aafae970bae744f4f1f865dbe6e13bc42e74c41734b18e4a4966153deb05da`  
		Last Modified: Wed, 22 Apr 2026 04:04:59 GMT  
		Size: 6.7 MB (6670722 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25e54bf1037c1b5f317d6bf5f0f522625bd3bed553c47c6add94800551e6a8ff`  
		Last Modified: Wed, 22 Apr 2026 04:04:58 GMT  
		Size: 14.8 KB (14827 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.38` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:94cec1265657b661cf97bed460c428b3760f4156637de5aa38a65ba122c58e38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.0 MB (164951045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d6a01e1373825d7bc9d85167c7cf3756f6a7a8663b4b179cd56060e46bcd1be`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:42:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:45:32 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:45:33 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 22 Apr 2026 02:45:37 GMT
ENV TELEGRAF_VERSION=1.38.3
# Wed, 22 Apr 2026 02:45:37 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Wed, 22 Apr 2026 02:45:37 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Wed, 22 Apr 2026 02:45:37 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 22 Apr 2026 02:45:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 02:45:37 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:30de66f8fdafab67e88d876087f571a693a1a6c4cf0abc29efbf88ea878e0d29`  
		Last Modified: Wed, 22 Apr 2026 00:15:43 GMT  
		Size: 48.4 MB (48373071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bb7bd28fbdfe678a7f45878b7b1c07dbbc0fa7753b0312aa8fd049667a9e137`  
		Last Modified: Wed, 22 Apr 2026 01:43:06 GMT  
		Size: 23.6 MB (23609423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:264e018336b4afedc4c6c2eae7bf9c8a47abd9fcd044978c11423a06a0060e9c`  
		Last Modified: Wed, 22 Apr 2026 02:45:57 GMT  
		Size: 18.9 MB (18885932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a6dd0995bf7067d49c403e08c32d6c48e03e0bd82e49dfe6a56c4aea107d1f3`  
		Last Modified: Wed, 22 Apr 2026 02:45:56 GMT  
		Size: 5.1 KB (5054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3480a92102a815f6264a05a3fb0fe8a7527dbf5cad4c772d9b545419c269efc`  
		Last Modified: Wed, 22 Apr 2026 02:45:58 GMT  
		Size: 74.1 MB (74076940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45af3e5712b7dc9b1067f4eaf53e0f4f025fd2d8539da812449e82435813fdfe`  
		Last Modified: Wed, 22 Apr 2026 02:45:56 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.38` - unknown; unknown

```console
$ docker pull telegraf@sha256:70c949d885543e44567741db3a8d9a0f516fb74bb6bc6cf05f9ecf44b5d8442f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6691656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c2373511b792dfa6a7ab716e4c6bb0327dd901936bc09ad1ec0386112fbc11b`

```dockerfile
```

-	Layers:
	-	`sha256:66a9f60f79c0bf2a3b62657d4b02928990c0488b1be62a2f37ed52d90174b1f5`  
		Last Modified: Wed, 22 Apr 2026 02:45:57 GMT  
		Size: 6.7 MB (6676805 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72499d4039655c2e504c2149df5089645e647802f887758d92f2e86aa81ae813`  
		Last Modified: Wed, 22 Apr 2026 02:45:56 GMT  
		Size: 14.9 KB (14851 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.38-alpine`

```console
$ docker pull telegraf@sha256:d96a87891f25955c267ff09c866c749ba6e5a3f00b922af7d327553c8eaaec59
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.38-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:9329f79e4f61821fe34e6675a45e3bc5ba490a10c29b78fa1b07fb96d7413f28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.3 MB (89341570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e446ecec12ac9e43036b90aaf265da167e1f9a7bcd791a4f54b88a61bc77c6b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Mon, 20 Apr 2026 23:01:10 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 20 Apr 2026 23:01:10 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 20 Apr 2026 23:01:19 GMT
ENV TELEGRAF_VERSION=1.38.3
# Mon, 20 Apr 2026 23:01:19 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 20 Apr 2026 23:01:19 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 20 Apr 2026 23:01:19 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 20 Apr 2026 23:01:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 20 Apr 2026 23:01:19 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55ba1ca119c95dcc4002e43d75c16e92ca9ed5da328c91b893b12b7255d7808e`  
		Last Modified: Mon, 20 Apr 2026 23:01:34 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af90712c1065542090e47fc7cae5ac33079ab2ac78f365778f253d4470f006a9`  
		Last Modified: Mon, 20 Apr 2026 23:01:34 GMT  
		Size: 2.6 MB (2615621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95c6c96fc8127cf13a62e341546d0e33ffc6487a2d73623bba1d94c06326f1c3`  
		Last Modified: Mon, 20 Apr 2026 23:01:36 GMT  
		Size: 82.9 MB (82860856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33475f37e3f83a07cd01d957666e351be2340dc48eb31201ef97999c3a1aefaa`  
		Last Modified: Mon, 20 Apr 2026 23:01:34 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.38-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:72f9b141756df474c234b4b675ad4d948bed8a7faa78fc15d82c70ee21202b68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1176197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4beb1e608277e4c322525e16b08bb3c33d5459cc20f7a9d63040d627b0bdd27`

```dockerfile
```

-	Layers:
	-	`sha256:28f27aa5782d9baf2fa31f0b92fa98b22a918aa1bad41ab129608fdc4e651f0d`  
		Last Modified: Mon, 20 Apr 2026 23:01:34 GMT  
		Size: 1.2 MB (1160977 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0cd23b43aaf5b8f30b1880dc9a34d19226c9e036aab4086c52d67bf2e97f045d`  
		Last Modified: Mon, 20 Apr 2026 23:01:34 GMT  
		Size: 15.2 KB (15220 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.38-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:8b04ef3b191824da04c0b5874838b5821ada4a6d7b48afd86e3df6270a36db11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.7 MB (80731816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52511b9f42dc7b99e2458d4d1bbdafc8a021247811ad1d4c46941f8efe498987`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Mon, 20 Apr 2026 23:00:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 20 Apr 2026 23:00:47 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 20 Apr 2026 23:00:53 GMT
ENV TELEGRAF_VERSION=1.38.3
# Mon, 20 Apr 2026 23:00:53 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 20 Apr 2026 23:00:53 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 20 Apr 2026 23:00:53 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 20 Apr 2026 23:00:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 20 Apr 2026 23:00:53 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c9b733d983622224ecddbe820bed2cb7e904ed583c6326d1fcbda67959fbc01`  
		Last Modified: Mon, 20 Apr 2026 23:01:08 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11f7df98aba8c78e2e29b3b228c032880b5e8acf2e6e1cf0bed0f6363b715335`  
		Last Modified: Mon, 20 Apr 2026 23:01:07 GMT  
		Size: 2.7 MB (2663564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9b5d3fbd32d64ada75fc47549619be9adf0a668037fe436c3d7c3de355d6493`  
		Last Modified: Mon, 20 Apr 2026 23:01:08 GMT  
		Size: 73.9 MB (73867483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9409057d942df5ffc8f8e16a5abcc46365c47c48f909fe2ae426cdbac197930a`  
		Last Modified: Mon, 20 Apr 2026 23:01:06 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.38-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:ec76870da5c01f53a2e038528dbebb056788db16195c62c9ae5103e3b9c0510a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1171308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c287ee0afb47dc691b031e966daab08c1affe814f449dda4ed648a6b4612f6e5`

```dockerfile
```

-	Layers:
	-	`sha256:4ff1462719c9ec6f85248c19a687f2a0602683d711a5dddc76daf068ff84395e`  
		Last Modified: Mon, 20 Apr 2026 23:01:07 GMT  
		Size: 1.2 MB (1155966 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9dfcaf9bb18b8737ae93288d4b086fec056bf86622b17b184faf48cf3120545f`  
		Last Modified: Mon, 20 Apr 2026 23:01:07 GMT  
		Size: 15.3 KB (15342 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.38.3`

```console
$ docker pull telegraf@sha256:88eb354ac9926d70791b70558d69644b527b3c7e6f02c2af9165038a3e306a6d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.38.3` - linux; amd64

```console
$ docker pull telegraf@sha256:3278cab4b3ba80a90e2de385a9855dd4e3500c891025a982e1c5dc51f57f1c56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.5 MB (174547969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2e6dfa7b8ce8f5cc1bd36dafe5ee923713b0fc0ddf123ecd310ce4102ee7aaf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 05:00:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 05:16:10 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 05:16:11 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 22 Apr 2026 05:16:15 GMT
ENV TELEGRAF_VERSION=1.38.3
# Wed, 22 Apr 2026 05:16:15 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Wed, 22 Apr 2026 05:16:15 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Wed, 22 Apr 2026 05:16:15 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 22 Apr 2026 05:16:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 05:16:15 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:db53381ee51f9e43304e236099ba097ae1b33ae41a8007e0b6319992eb55fd00`  
		Last Modified: Wed, 22 Apr 2026 00:15:45 GMT  
		Size: 48.5 MB (48488628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5203b2bfeff92b72e816dc6cbb1f16856f0cd592e521e3c0cfa195a78fe180e`  
		Last Modified: Wed, 22 Apr 2026 05:01:15 GMT  
		Size: 24.0 MB (24042234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8acdaa6f91c9ba4895ddb392aae95bc41fff1e0597f39b3d6a96b67500de023c`  
		Last Modified: Wed, 22 Apr 2026 05:16:34 GMT  
		Size: 18.9 MB (18944330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb77e8a73df98439739f415dd132afbece308e0c5d694a0d38a765e4904aa86e`  
		Last Modified: Wed, 22 Apr 2026 05:16:33 GMT  
		Size: 5.1 KB (5070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f40d61eeb10ad19b0c1deeee0bcba32c309264ff42136064ada8798f128faa09`  
		Last Modified: Wed, 22 Apr 2026 05:16:36 GMT  
		Size: 83.1 MB (83067082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59a33f3a5d60285ac12d5a9eeeab3f92064752300d3b3a75fcd16b90c8b3e322`  
		Last Modified: Wed, 22 Apr 2026 05:16:33 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.38.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:6293af4bad25705a78b1dc84924547003b1863bcc59474e92bbb515d97ae81da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6690845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:930334ea18d85ba05593bd839e27a887835513365d5cc0f56b5d8a88e95e131a`

```dockerfile
```

-	Layers:
	-	`sha256:e81c19a14633e8727bea8c55b5630657691a6ea57998e353bd2edd623e295b91`  
		Last Modified: Wed, 22 Apr 2026 05:16:33 GMT  
		Size: 6.7 MB (6676117 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:193bd5147cc76d0e7667bc71ddaeafcd0990ea9a4498d2c42eb4e96b0f015b2c`  
		Last Modified: Wed, 22 Apr 2026 05:16:33 GMT  
		Size: 14.7 KB (14728 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.38.3` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:9c34d13f45a6fe087e8b762d8fefb174b7aedfe46c8b0f066e2fd3a26a4671ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.8 MB (160829606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb782f542da35921cd1cd23f40605441990d7123ba00a1df765769174ca50bef`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 02:18:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 04:04:35 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 04:04:35 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 22 Apr 2026 04:04:40 GMT
ENV TELEGRAF_VERSION=1.38.3
# Wed, 22 Apr 2026 04:04:40 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Wed, 22 Apr 2026 04:04:40 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Wed, 22 Apr 2026 04:04:40 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 22 Apr 2026 04:04:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 04:04:40 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:a78e7b2123c5c35e65ee1cc17df0d11c1db8ab3c4fe80b457270c2d9ae5003b1`  
		Last Modified: Wed, 22 Apr 2026 00:16:29 GMT  
		Size: 44.2 MB (44207655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:218160481dc948cfbf943718a4363de6a3663997f19a965c7b86136ac3e28f30`  
		Last Modified: Wed, 22 Apr 2026 02:18:15 GMT  
		Size: 21.9 MB (21946340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9742f40fc9d5bb902bd77ee1549e0c0815816441cf37052058bb32ebee0e18ec`  
		Last Modified: Wed, 22 Apr 2026 04:04:59 GMT  
		Size: 17.7 MB (17699933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8726f263804a6205f42456a2db18b58eac1f997dee87aa0a54c367d66366f8b8`  
		Last Modified: Wed, 22 Apr 2026 04:04:58 GMT  
		Size: 5.1 KB (5055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef5c472b4f00d8e1d0623d3c9cdb5bbb924e15ca10c0492d280a152d76a43b60`  
		Last Modified: Wed, 22 Apr 2026 04:05:01 GMT  
		Size: 77.0 MB (76969998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e12d49f366146ec8630190da0ccf729e6d970e44bce60ea1f65670cdf0544b9`  
		Last Modified: Wed, 22 Apr 2026 04:04:58 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.38.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:6f5b5648c87d352bde9bd712fed1e666268fa06c582a8dae4f4f75df99b9d89d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6685549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ccf4b491558cbb21acf76bd1a280a051f07701fbc5bc25832ba635179b1b8f2`

```dockerfile
```

-	Layers:
	-	`sha256:20aafae970bae744f4f1f865dbe6e13bc42e74c41734b18e4a4966153deb05da`  
		Last Modified: Wed, 22 Apr 2026 04:04:59 GMT  
		Size: 6.7 MB (6670722 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25e54bf1037c1b5f317d6bf5f0f522625bd3bed553c47c6add94800551e6a8ff`  
		Last Modified: Wed, 22 Apr 2026 04:04:58 GMT  
		Size: 14.8 KB (14827 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.38.3` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:94cec1265657b661cf97bed460c428b3760f4156637de5aa38a65ba122c58e38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.0 MB (164951045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d6a01e1373825d7bc9d85167c7cf3756f6a7a8663b4b179cd56060e46bcd1be`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:42:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:45:32 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:45:33 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 22 Apr 2026 02:45:37 GMT
ENV TELEGRAF_VERSION=1.38.3
# Wed, 22 Apr 2026 02:45:37 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Wed, 22 Apr 2026 02:45:37 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Wed, 22 Apr 2026 02:45:37 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 22 Apr 2026 02:45:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 02:45:37 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:30de66f8fdafab67e88d876087f571a693a1a6c4cf0abc29efbf88ea878e0d29`  
		Last Modified: Wed, 22 Apr 2026 00:15:43 GMT  
		Size: 48.4 MB (48373071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bb7bd28fbdfe678a7f45878b7b1c07dbbc0fa7753b0312aa8fd049667a9e137`  
		Last Modified: Wed, 22 Apr 2026 01:43:06 GMT  
		Size: 23.6 MB (23609423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:264e018336b4afedc4c6c2eae7bf9c8a47abd9fcd044978c11423a06a0060e9c`  
		Last Modified: Wed, 22 Apr 2026 02:45:57 GMT  
		Size: 18.9 MB (18885932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a6dd0995bf7067d49c403e08c32d6c48e03e0bd82e49dfe6a56c4aea107d1f3`  
		Last Modified: Wed, 22 Apr 2026 02:45:56 GMT  
		Size: 5.1 KB (5054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3480a92102a815f6264a05a3fb0fe8a7527dbf5cad4c772d9b545419c269efc`  
		Last Modified: Wed, 22 Apr 2026 02:45:58 GMT  
		Size: 74.1 MB (74076940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45af3e5712b7dc9b1067f4eaf53e0f4f025fd2d8539da812449e82435813fdfe`  
		Last Modified: Wed, 22 Apr 2026 02:45:56 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.38.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:70c949d885543e44567741db3a8d9a0f516fb74bb6bc6cf05f9ecf44b5d8442f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6691656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c2373511b792dfa6a7ab716e4c6bb0327dd901936bc09ad1ec0386112fbc11b`

```dockerfile
```

-	Layers:
	-	`sha256:66a9f60f79c0bf2a3b62657d4b02928990c0488b1be62a2f37ed52d90174b1f5`  
		Last Modified: Wed, 22 Apr 2026 02:45:57 GMT  
		Size: 6.7 MB (6676805 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72499d4039655c2e504c2149df5089645e647802f887758d92f2e86aa81ae813`  
		Last Modified: Wed, 22 Apr 2026 02:45:56 GMT  
		Size: 14.9 KB (14851 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.38.3-alpine`

```console
$ docker pull telegraf@sha256:d96a87891f25955c267ff09c866c749ba6e5a3f00b922af7d327553c8eaaec59
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.38.3-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:9329f79e4f61821fe34e6675a45e3bc5ba490a10c29b78fa1b07fb96d7413f28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.3 MB (89341570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e446ecec12ac9e43036b90aaf265da167e1f9a7bcd791a4f54b88a61bc77c6b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Mon, 20 Apr 2026 23:01:10 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 20 Apr 2026 23:01:10 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 20 Apr 2026 23:01:19 GMT
ENV TELEGRAF_VERSION=1.38.3
# Mon, 20 Apr 2026 23:01:19 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 20 Apr 2026 23:01:19 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 20 Apr 2026 23:01:19 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 20 Apr 2026 23:01:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 20 Apr 2026 23:01:19 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55ba1ca119c95dcc4002e43d75c16e92ca9ed5da328c91b893b12b7255d7808e`  
		Last Modified: Mon, 20 Apr 2026 23:01:34 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af90712c1065542090e47fc7cae5ac33079ab2ac78f365778f253d4470f006a9`  
		Last Modified: Mon, 20 Apr 2026 23:01:34 GMT  
		Size: 2.6 MB (2615621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95c6c96fc8127cf13a62e341546d0e33ffc6487a2d73623bba1d94c06326f1c3`  
		Last Modified: Mon, 20 Apr 2026 23:01:36 GMT  
		Size: 82.9 MB (82860856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33475f37e3f83a07cd01d957666e351be2340dc48eb31201ef97999c3a1aefaa`  
		Last Modified: Mon, 20 Apr 2026 23:01:34 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.38.3-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:72f9b141756df474c234b4b675ad4d948bed8a7faa78fc15d82c70ee21202b68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1176197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4beb1e608277e4c322525e16b08bb3c33d5459cc20f7a9d63040d627b0bdd27`

```dockerfile
```

-	Layers:
	-	`sha256:28f27aa5782d9baf2fa31f0b92fa98b22a918aa1bad41ab129608fdc4e651f0d`  
		Last Modified: Mon, 20 Apr 2026 23:01:34 GMT  
		Size: 1.2 MB (1160977 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0cd23b43aaf5b8f30b1880dc9a34d19226c9e036aab4086c52d67bf2e97f045d`  
		Last Modified: Mon, 20 Apr 2026 23:01:34 GMT  
		Size: 15.2 KB (15220 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.38.3-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:8b04ef3b191824da04c0b5874838b5821ada4a6d7b48afd86e3df6270a36db11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.7 MB (80731816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52511b9f42dc7b99e2458d4d1bbdafc8a021247811ad1d4c46941f8efe498987`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Mon, 20 Apr 2026 23:00:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 20 Apr 2026 23:00:47 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 20 Apr 2026 23:00:53 GMT
ENV TELEGRAF_VERSION=1.38.3
# Mon, 20 Apr 2026 23:00:53 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 20 Apr 2026 23:00:53 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 20 Apr 2026 23:00:53 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 20 Apr 2026 23:00:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 20 Apr 2026 23:00:53 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c9b733d983622224ecddbe820bed2cb7e904ed583c6326d1fcbda67959fbc01`  
		Last Modified: Mon, 20 Apr 2026 23:01:08 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11f7df98aba8c78e2e29b3b228c032880b5e8acf2e6e1cf0bed0f6363b715335`  
		Last Modified: Mon, 20 Apr 2026 23:01:07 GMT  
		Size: 2.7 MB (2663564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9b5d3fbd32d64ada75fc47549619be9adf0a668037fe436c3d7c3de355d6493`  
		Last Modified: Mon, 20 Apr 2026 23:01:08 GMT  
		Size: 73.9 MB (73867483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9409057d942df5ffc8f8e16a5abcc46365c47c48f909fe2ae426cdbac197930a`  
		Last Modified: Mon, 20 Apr 2026 23:01:06 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.38.3-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:ec76870da5c01f53a2e038528dbebb056788db16195c62c9ae5103e3b9c0510a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1171308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c287ee0afb47dc691b031e966daab08c1affe814f449dda4ed648a6b4612f6e5`

```dockerfile
```

-	Layers:
	-	`sha256:4ff1462719c9ec6f85248c19a687f2a0602683d711a5dddc76daf068ff84395e`  
		Last Modified: Mon, 20 Apr 2026 23:01:07 GMT  
		Size: 1.2 MB (1155966 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9dfcaf9bb18b8737ae93288d4b086fec056bf86622b17b184faf48cf3120545f`  
		Last Modified: Mon, 20 Apr 2026 23:01:07 GMT  
		Size: 15.3 KB (15342 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:alpine`

```console
$ docker pull telegraf@sha256:d96a87891f25955c267ff09c866c749ba6e5a3f00b922af7d327553c8eaaec59
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:9329f79e4f61821fe34e6675a45e3bc5ba490a10c29b78fa1b07fb96d7413f28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.3 MB (89341570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e446ecec12ac9e43036b90aaf265da167e1f9a7bcd791a4f54b88a61bc77c6b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Mon, 20 Apr 2026 23:01:10 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 20 Apr 2026 23:01:10 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 20 Apr 2026 23:01:19 GMT
ENV TELEGRAF_VERSION=1.38.3
# Mon, 20 Apr 2026 23:01:19 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 20 Apr 2026 23:01:19 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 20 Apr 2026 23:01:19 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 20 Apr 2026 23:01:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 20 Apr 2026 23:01:19 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55ba1ca119c95dcc4002e43d75c16e92ca9ed5da328c91b893b12b7255d7808e`  
		Last Modified: Mon, 20 Apr 2026 23:01:34 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af90712c1065542090e47fc7cae5ac33079ab2ac78f365778f253d4470f006a9`  
		Last Modified: Mon, 20 Apr 2026 23:01:34 GMT  
		Size: 2.6 MB (2615621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95c6c96fc8127cf13a62e341546d0e33ffc6487a2d73623bba1d94c06326f1c3`  
		Last Modified: Mon, 20 Apr 2026 23:01:36 GMT  
		Size: 82.9 MB (82860856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33475f37e3f83a07cd01d957666e351be2340dc48eb31201ef97999c3a1aefaa`  
		Last Modified: Mon, 20 Apr 2026 23:01:34 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:72f9b141756df474c234b4b675ad4d948bed8a7faa78fc15d82c70ee21202b68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1176197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4beb1e608277e4c322525e16b08bb3c33d5459cc20f7a9d63040d627b0bdd27`

```dockerfile
```

-	Layers:
	-	`sha256:28f27aa5782d9baf2fa31f0b92fa98b22a918aa1bad41ab129608fdc4e651f0d`  
		Last Modified: Mon, 20 Apr 2026 23:01:34 GMT  
		Size: 1.2 MB (1160977 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0cd23b43aaf5b8f30b1880dc9a34d19226c9e036aab4086c52d67bf2e97f045d`  
		Last Modified: Mon, 20 Apr 2026 23:01:34 GMT  
		Size: 15.2 KB (15220 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:8b04ef3b191824da04c0b5874838b5821ada4a6d7b48afd86e3df6270a36db11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.7 MB (80731816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52511b9f42dc7b99e2458d4d1bbdafc8a021247811ad1d4c46941f8efe498987`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Mon, 20 Apr 2026 23:00:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 20 Apr 2026 23:00:47 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 20 Apr 2026 23:00:53 GMT
ENV TELEGRAF_VERSION=1.38.3
# Mon, 20 Apr 2026 23:00:53 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 20 Apr 2026 23:00:53 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 20 Apr 2026 23:00:53 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 20 Apr 2026 23:00:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 20 Apr 2026 23:00:53 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c9b733d983622224ecddbe820bed2cb7e904ed583c6326d1fcbda67959fbc01`  
		Last Modified: Mon, 20 Apr 2026 23:01:08 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11f7df98aba8c78e2e29b3b228c032880b5e8acf2e6e1cf0bed0f6363b715335`  
		Last Modified: Mon, 20 Apr 2026 23:01:07 GMT  
		Size: 2.7 MB (2663564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9b5d3fbd32d64ada75fc47549619be9adf0a668037fe436c3d7c3de355d6493`  
		Last Modified: Mon, 20 Apr 2026 23:01:08 GMT  
		Size: 73.9 MB (73867483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9409057d942df5ffc8f8e16a5abcc46365c47c48f909fe2ae426cdbac197930a`  
		Last Modified: Mon, 20 Apr 2026 23:01:06 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:ec76870da5c01f53a2e038528dbebb056788db16195c62c9ae5103e3b9c0510a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1171308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c287ee0afb47dc691b031e966daab08c1affe814f449dda4ed648a6b4612f6e5`

```dockerfile
```

-	Layers:
	-	`sha256:4ff1462719c9ec6f85248c19a687f2a0602683d711a5dddc76daf068ff84395e`  
		Last Modified: Mon, 20 Apr 2026 23:01:07 GMT  
		Size: 1.2 MB (1155966 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9dfcaf9bb18b8737ae93288d4b086fec056bf86622b17b184faf48cf3120545f`  
		Last Modified: Mon, 20 Apr 2026 23:01:07 GMT  
		Size: 15.3 KB (15342 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:latest`

```console
$ docker pull telegraf@sha256:88eb354ac9926d70791b70558d69644b527b3c7e6f02c2af9165038a3e306a6d
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
$ docker pull telegraf@sha256:3278cab4b3ba80a90e2de385a9855dd4e3500c891025a982e1c5dc51f57f1c56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.5 MB (174547969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2e6dfa7b8ce8f5cc1bd36dafe5ee923713b0fc0ddf123ecd310ce4102ee7aaf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 05:00:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 05:16:10 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 05:16:11 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 22 Apr 2026 05:16:15 GMT
ENV TELEGRAF_VERSION=1.38.3
# Wed, 22 Apr 2026 05:16:15 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Wed, 22 Apr 2026 05:16:15 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Wed, 22 Apr 2026 05:16:15 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 22 Apr 2026 05:16:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 05:16:15 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:db53381ee51f9e43304e236099ba097ae1b33ae41a8007e0b6319992eb55fd00`  
		Last Modified: Wed, 22 Apr 2026 00:15:45 GMT  
		Size: 48.5 MB (48488628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5203b2bfeff92b72e816dc6cbb1f16856f0cd592e521e3c0cfa195a78fe180e`  
		Last Modified: Wed, 22 Apr 2026 05:01:15 GMT  
		Size: 24.0 MB (24042234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8acdaa6f91c9ba4895ddb392aae95bc41fff1e0597f39b3d6a96b67500de023c`  
		Last Modified: Wed, 22 Apr 2026 05:16:34 GMT  
		Size: 18.9 MB (18944330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb77e8a73df98439739f415dd132afbece308e0c5d694a0d38a765e4904aa86e`  
		Last Modified: Wed, 22 Apr 2026 05:16:33 GMT  
		Size: 5.1 KB (5070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f40d61eeb10ad19b0c1deeee0bcba32c309264ff42136064ada8798f128faa09`  
		Last Modified: Wed, 22 Apr 2026 05:16:36 GMT  
		Size: 83.1 MB (83067082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59a33f3a5d60285ac12d5a9eeeab3f92064752300d3b3a75fcd16b90c8b3e322`  
		Last Modified: Wed, 22 Apr 2026 05:16:33 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:6293af4bad25705a78b1dc84924547003b1863bcc59474e92bbb515d97ae81da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6690845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:930334ea18d85ba05593bd839e27a887835513365d5cc0f56b5d8a88e95e131a`

```dockerfile
```

-	Layers:
	-	`sha256:e81c19a14633e8727bea8c55b5630657691a6ea57998e353bd2edd623e295b91`  
		Last Modified: Wed, 22 Apr 2026 05:16:33 GMT  
		Size: 6.7 MB (6676117 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:193bd5147cc76d0e7667bc71ddaeafcd0990ea9a4498d2c42eb4e96b0f015b2c`  
		Last Modified: Wed, 22 Apr 2026 05:16:33 GMT  
		Size: 14.7 KB (14728 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:9c34d13f45a6fe087e8b762d8fefb174b7aedfe46c8b0f066e2fd3a26a4671ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.8 MB (160829606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb782f542da35921cd1cd23f40605441990d7123ba00a1df765769174ca50bef`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 02:18:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 04:04:35 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 04:04:35 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 22 Apr 2026 04:04:40 GMT
ENV TELEGRAF_VERSION=1.38.3
# Wed, 22 Apr 2026 04:04:40 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Wed, 22 Apr 2026 04:04:40 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Wed, 22 Apr 2026 04:04:40 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 22 Apr 2026 04:04:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 04:04:40 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:a78e7b2123c5c35e65ee1cc17df0d11c1db8ab3c4fe80b457270c2d9ae5003b1`  
		Last Modified: Wed, 22 Apr 2026 00:16:29 GMT  
		Size: 44.2 MB (44207655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:218160481dc948cfbf943718a4363de6a3663997f19a965c7b86136ac3e28f30`  
		Last Modified: Wed, 22 Apr 2026 02:18:15 GMT  
		Size: 21.9 MB (21946340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9742f40fc9d5bb902bd77ee1549e0c0815816441cf37052058bb32ebee0e18ec`  
		Last Modified: Wed, 22 Apr 2026 04:04:59 GMT  
		Size: 17.7 MB (17699933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8726f263804a6205f42456a2db18b58eac1f997dee87aa0a54c367d66366f8b8`  
		Last Modified: Wed, 22 Apr 2026 04:04:58 GMT  
		Size: 5.1 KB (5055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef5c472b4f00d8e1d0623d3c9cdb5bbb924e15ca10c0492d280a152d76a43b60`  
		Last Modified: Wed, 22 Apr 2026 04:05:01 GMT  
		Size: 77.0 MB (76969998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e12d49f366146ec8630190da0ccf729e6d970e44bce60ea1f65670cdf0544b9`  
		Last Modified: Wed, 22 Apr 2026 04:04:58 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:6f5b5648c87d352bde9bd712fed1e666268fa06c582a8dae4f4f75df99b9d89d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6685549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ccf4b491558cbb21acf76bd1a280a051f07701fbc5bc25832ba635179b1b8f2`

```dockerfile
```

-	Layers:
	-	`sha256:20aafae970bae744f4f1f865dbe6e13bc42e74c41734b18e4a4966153deb05da`  
		Last Modified: Wed, 22 Apr 2026 04:04:59 GMT  
		Size: 6.7 MB (6670722 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25e54bf1037c1b5f317d6bf5f0f522625bd3bed553c47c6add94800551e6a8ff`  
		Last Modified: Wed, 22 Apr 2026 04:04:58 GMT  
		Size: 14.8 KB (14827 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:94cec1265657b661cf97bed460c428b3760f4156637de5aa38a65ba122c58e38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.0 MB (164951045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d6a01e1373825d7bc9d85167c7cf3756f6a7a8663b4b179cd56060e46bcd1be`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:42:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:45:32 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:45:33 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 22 Apr 2026 02:45:37 GMT
ENV TELEGRAF_VERSION=1.38.3
# Wed, 22 Apr 2026 02:45:37 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Wed, 22 Apr 2026 02:45:37 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Wed, 22 Apr 2026 02:45:37 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 22 Apr 2026 02:45:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 02:45:37 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:30de66f8fdafab67e88d876087f571a693a1a6c4cf0abc29efbf88ea878e0d29`  
		Last Modified: Wed, 22 Apr 2026 00:15:43 GMT  
		Size: 48.4 MB (48373071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bb7bd28fbdfe678a7f45878b7b1c07dbbc0fa7753b0312aa8fd049667a9e137`  
		Last Modified: Wed, 22 Apr 2026 01:43:06 GMT  
		Size: 23.6 MB (23609423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:264e018336b4afedc4c6c2eae7bf9c8a47abd9fcd044978c11423a06a0060e9c`  
		Last Modified: Wed, 22 Apr 2026 02:45:57 GMT  
		Size: 18.9 MB (18885932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a6dd0995bf7067d49c403e08c32d6c48e03e0bd82e49dfe6a56c4aea107d1f3`  
		Last Modified: Wed, 22 Apr 2026 02:45:56 GMT  
		Size: 5.1 KB (5054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3480a92102a815f6264a05a3fb0fe8a7527dbf5cad4c772d9b545419c269efc`  
		Last Modified: Wed, 22 Apr 2026 02:45:58 GMT  
		Size: 74.1 MB (74076940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45af3e5712b7dc9b1067f4eaf53e0f4f025fd2d8539da812449e82435813fdfe`  
		Last Modified: Wed, 22 Apr 2026 02:45:56 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:70c949d885543e44567741db3a8d9a0f516fb74bb6bc6cf05f9ecf44b5d8442f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6691656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c2373511b792dfa6a7ab716e4c6bb0327dd901936bc09ad1ec0386112fbc11b`

```dockerfile
```

-	Layers:
	-	`sha256:66a9f60f79c0bf2a3b62657d4b02928990c0488b1be62a2f37ed52d90174b1f5`  
		Last Modified: Wed, 22 Apr 2026 02:45:57 GMT  
		Size: 6.7 MB (6676805 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72499d4039655c2e504c2149df5089645e647802f887758d92f2e86aa81ae813`  
		Last Modified: Wed, 22 Apr 2026 02:45:56 GMT  
		Size: 14.9 KB (14851 bytes)  
		MIME: application/vnd.in-toto+json
