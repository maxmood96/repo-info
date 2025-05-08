<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `telegraf`

-	[`telegraf:1.32`](#telegraf132)
-	[`telegraf:1.32-alpine`](#telegraf132-alpine)
-	[`telegraf:1.32.3`](#telegraf1323)
-	[`telegraf:1.32.3-alpine`](#telegraf1323-alpine)
-	[`telegraf:1.33`](#telegraf133)
-	[`telegraf:1.33-alpine`](#telegraf133-alpine)
-	[`telegraf:1.33.3`](#telegraf1333)
-	[`telegraf:1.33.3-alpine`](#telegraf1333-alpine)
-	[`telegraf:1.34`](#telegraf134)
-	[`telegraf:1.34-alpine`](#telegraf134-alpine)
-	[`telegraf:1.34.3`](#telegraf1343)
-	[`telegraf:1.34.3-alpine`](#telegraf1343-alpine)
-	[`telegraf:alpine`](#telegrafalpine)
-	[`telegraf:latest`](#telegraflatest)

## `telegraf:1.32`

```console
$ docker pull telegraf@sha256:3467ba322b199721c0583e684524aedb46d3389b284602c4031bd24b83cfa30d
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
$ docker pull telegraf@sha256:133a1f6fad5bdf91291538d0c99b7092cb0227c99a2a63c55d7fe556178fe8aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.5 MB (161472346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:495572a3faa0524733483264fde59a6043400c181d666d4c21592025aa349c95`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 17:23:46 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 17:23:46 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 14 Apr 2025 17:23:46 GMT
ENV TELEGRAF_VERSION=1.32.3
# Mon, 14 Apr 2025 17:23:46 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 14 Apr 2025 17:23:46 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 14 Apr 2025 17:23:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 14 Apr 2025 17:23:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 14 Apr 2025 17:23:46 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:cf05a52c02353f0b2b6f9be0549ac916c3fb1dc8d4bacd405eac7f28562ec9f2`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 48.5 MB (48491199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63964a8518f54dc31f8df89d7f06714c7a793aa1aa08a64ae3d7f4f4f30b4ac8`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 24.0 MB (24011181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c933b6be6e4b5fa149324199e7b0a1c9ccb7cf0ac29ed8b5b9b44fd4408d57f`  
		Last Modified: Thu, 08 May 2025 17:38:15 GMT  
		Size: 18.9 MB (18946492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2b2f6c561c97261c4b0f61c5db60a43d784c78dca5ffd46b06e72090acb250f`  
		Last Modified: Thu, 08 May 2025 17:38:14 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38da449724bdaeb9151e330aa111ac8a64b07fd6504603ca0550fd0ebfebcec9`  
		Last Modified: Thu, 08 May 2025 17:38:20 GMT  
		Size: 70.0 MB (70021066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39ab13a890f276867bb402308d18f401d354b5ea78288c440f5fbaf9d06638c2`  
		Last Modified: Thu, 08 May 2025 17:38:14 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.32` - unknown; unknown

```console
$ docker pull telegraf@sha256:9e2f40dd9d9cfb83d681771aa13ce7edc00c799a06c7e66e43660c899244f34c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6438476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86f5e2f11776c992b4e619645c5282d1de67d83d81d6f6913f7ce99728f0d834`

```dockerfile
```

-	Layers:
	-	`sha256:91178148c42fa39443216872b394bb291ff7165babad0a68ec0daef0742a9b66`  
		Last Modified: Mon, 28 Apr 2025 22:21:44 GMT  
		Size: 6.4 MB (6424006 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b2ca0d300a3dcbdfaf1773af9a3ecfed0eacb8c6a204171bd964b13854c8f23`  
		Last Modified: Mon, 28 Apr 2025 22:21:44 GMT  
		Size: 14.5 KB (14470 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.32` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:5e0316150e5e96e705c5c10e9bd574da3a1bf96d415875960d5003943fde1f52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.5 MB (148525488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c3a3d3ab0b8e0e43511135d7510bd621f472b0817d860382bfc1731679b779f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 17:23:46 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 17:23:46 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 14 Apr 2025 17:23:46 GMT
ENV TELEGRAF_VERSION=1.32.3
# Mon, 14 Apr 2025 17:23:46 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 14 Apr 2025 17:23:46 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 14 Apr 2025 17:23:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 14 Apr 2025 17:23:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 14 Apr 2025 17:23:46 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:a735d4b4a53e8e11448d15bc50ce4670d54dff52e426cf0510c9b713d3a7ad09`  
		Last Modified: Thu, 08 May 2025 17:04:48 GMT  
		Size: 44.2 MB (44197079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b01e6436acd06b177253a4ba25e5179715088c2f493e89c91bbf6fdc41a2034`  
		Last Modified: Thu, 08 May 2025 17:05:35 GMT  
		Size: 21.9 MB (21918380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eabe566c6af2691f3105823447ac937c1f11b004965e6abc01575a064a841148`  
		Last Modified: Thu, 08 May 2025 19:54:16 GMT  
		Size: 17.7 MB (17724705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2d5c5bcea6d97d32d23b37764468583109ef0810d01e6d83a881b0023fe34ef`  
		Last Modified: Thu, 08 May 2025 19:54:19 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a9c4a9ba46b05c9fc1043c16a2d77b4cd85e76b9604f9d490862d12ff932cf6`  
		Last Modified: Tue, 29 Apr 2025 15:23:41 GMT  
		Size: 64.7 MB (64682927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9250a0aa5455fbe2090dac00f5beda1b9dc530c54587a3d92e23f7622e18113`  
		Last Modified: Tue, 29 Apr 2025 15:23:39 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.32` - unknown; unknown

```console
$ docker pull telegraf@sha256:034c3bdc3cf115313c5b638a066e26de7365996d2676afb265e23ddb19a01da8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6433966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b3b5dd92dfdb3de595b994a99c985a3fce8156dd0b81912f7d67dd8fcf1cadd`

```dockerfile
```

-	Layers:
	-	`sha256:4dbcd1380dac15d9db4b21afd6cefc918a92ed82583a3956df06f4e1ea313fd2`  
		Last Modified: Tue, 29 Apr 2025 15:23:39 GMT  
		Size: 6.4 MB (6419410 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3801861fc02d9f777aada0ad295bfca4d677645e8d9c7c2ae063cb8909e5986`  
		Last Modified: Tue, 29 Apr 2025 15:23:38 GMT  
		Size: 14.6 KB (14556 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.32` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:ae34603da2c6d4d6f0bb614c276c2fd6b9945aacc49405ab2fdf5acd3e3411b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.9 MB (153897671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:801fd23dffa15d66e19b59a801fc1fcbb041368189b60c2750e60a3e6c0facb1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 17:23:46 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 17:23:46 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 14 Apr 2025 17:23:46 GMT
ENV TELEGRAF_VERSION=1.32.3
# Mon, 14 Apr 2025 17:23:46 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 14 Apr 2025 17:23:46 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 14 Apr 2025 17:23:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 14 Apr 2025 17:23:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 14 Apr 2025 17:23:46 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:de07ba6f486e0ce29760ab32d4381edabbc660a04c493e95eb9a8056925d8955`  
		Last Modified: Thu, 08 May 2025 17:04:44 GMT  
		Size: 48.3 MB (48327644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84649bff67ea459549b6f371f7045d9968d6ebf370b815c922a625f3ab065724`  
		Last Modified: Thu, 08 May 2025 17:04:42 GMT  
		Size: 23.5 MB (23544262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7446c58993d11b00fcf70a65c363df298c8fd24914c3657943f2362852a75e88`  
		Last Modified: Thu, 08 May 2025 17:07:55 GMT  
		Size: 18.9 MB (18871759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38670875debfb321519f19305350d13646a48ebaac8d2b798ab7aa84cefe61b0`  
		Last Modified: Thu, 08 May 2025 17:07:53 GMT  
		Size: 1.8 KB (1782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df5079117dbac2057f98deaff5edbb025897cdcefeaa944b9523223f24fad7c5`  
		Last Modified: Tue, 29 Apr 2025 19:27:35 GMT  
		Size: 63.2 MB (63151600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c6076ec624b8284c1e646b98e2c38bccc71e847a3e241dd13b70b13dfa440eb`  
		Last Modified: Tue, 29 Apr 2025 19:27:33 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.32` - unknown; unknown

```console
$ docker pull telegraf@sha256:bc308f54bf5dde871d7ce887ae35355c130fb75bfdf42460544a0d2f15032c59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6439262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae430ca89a2034170876208e34e7d8303ec3efa23f6c75f178f0edfc594d7619`

```dockerfile
```

-	Layers:
	-	`sha256:fe97e3d0ffbbff78b920dcfe801839987317812b123de1de562d8960f800679c`  
		Last Modified: Tue, 29 Apr 2025 19:27:33 GMT  
		Size: 6.4 MB (6424682 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1cca97bd02c75aae00cfeafb6bb4a2d316744bb9accd7d75b970a782882afa73`  
		Last Modified: Tue, 29 Apr 2025 19:27:32 GMT  
		Size: 14.6 KB (14580 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.32-alpine`

```console
$ docker pull telegraf@sha256:9613ea0126325721f7087013726dadd23bf0aff8caed38d9337c449cdb66f05b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.32-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:3ad9fa3557eec07393d93ba99a10a803a1d358c08aee5b31f11927ed45248331
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75899910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87127c7ae451c11d56da2e3bbdb0133e4fc5465199f4a064700dc7bc1b95f94d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 10 Feb 2025 22:49:00 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
CMD ["/bin/sh"]
# Mon, 10 Feb 2025 22:49:00 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
ENV TELEGRAF_VERSION=1.32.3
# Mon, 10 Feb 2025 22:49:00 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 10 Feb 2025 22:49:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Feb 2025 22:49:00 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 14:35:06 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eb2f8452f18fa5ca6d6eab55873b03df9cb04ec2a5cbef0b0347252dd1f1b98`  
		Last Modified: Fri, 14 Feb 2025 22:10:30 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b1849576e5bfb8707e5b6da1ed76fc1b4642590a5cd627cc954d4458c972b87`  
		Last Modified: Fri, 14 Feb 2025 22:10:31 GMT  
		Size: 2.4 MB (2447977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8976f17c93a72e5f006514ed0e2d593d5fa816d872152c28e428bea70d7a275`  
		Last Modified: Fri, 14 Feb 2025 22:13:09 GMT  
		Size: 69.8 MB (69824429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a0c5ba34859540677e65faaa6f81da813c58e83b5870ad2c8611227ad0b1a0`  
		Last Modified: Fri, 14 Feb 2025 22:10:32 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.32-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:6a788cf31b15ae6004a2eb7b8e1abe4b99d5f46318fabad2c75620283de0f097
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1093716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a9834368eb385832d1124281f968481309de1c0912c4bea4bad334e1ee56503`

```dockerfile
```

-	Layers:
	-	`sha256:36d17874c7c519d61791ce6538dcf5b70d8d316102b689fadc4fcbf715597e97`  
		Last Modified: Fri, 14 Feb 2025 22:10:24 GMT  
		Size: 1.1 MB (1078755 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a53875bd2d4d184394b04b7247846ef535add592138dcbbc0131261f51dd4b97`  
		Last Modified: Fri, 14 Feb 2025 22:10:24 GMT  
		Size: 15.0 KB (14961 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.32-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:5c131e9d3dfd41b67fbe1efc79eade66effd3013805af278d26b9581ac0535eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.6 MB (69569876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7adaf8892bce40df4e537a256a91cdc51bfcdaf585b04cdc584cdded2e35ab2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 10 Feb 2025 22:49:00 GMT
ADD alpine-minirootfs-3.20.6-aarch64.tar.gz / # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
CMD ["/bin/sh"]
# Mon, 10 Feb 2025 22:49:00 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
ENV TELEGRAF_VERSION=1.32.3
# Mon, 10 Feb 2025 22:49:00 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 10 Feb 2025 22:49:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Feb 2025 22:49:00 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:94e9d8af22013aabf0edcaf42950c88b0a1350c3a9ce076d61b98a535a673dd9`  
		Last Modified: Fri, 14 Feb 2025 14:35:45 GMT  
		Size: 4.1 MB (4091165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a61a5f488a07a5f9b377e1e8af47680d864b0a298fd6acfe930441fecb3ecf84`  
		Last Modified: Sat, 15 Feb 2025 03:20:35 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:976a777ce7d187cf232aae59fd07445827d4a146c69dd2ff0adb80ede2329896`  
		Last Modified: Sat, 15 Feb 2025 10:11:16 GMT  
		Size: 2.5 MB (2533889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cd034834e7dc25546d11a5edde9078270a777c1002a13613255b26db02298a6`  
		Last Modified: Sat, 15 Feb 2025 11:18:03 GMT  
		Size: 62.9 MB (62944215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:570d8419ba9fcec72ee59593f2912c265a2f2650c283c863e9e30235da563b5f`  
		Last Modified: Sat, 15 Feb 2025 11:18:00 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.32-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:e951a2565274dbce09494aac2324db6c6f4fe6b0940ca7528fc4c98c8023c85d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1089453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a33f51f8d0f3468d4c73164109a47998bc26ee6bb0739487e7e5c768a16499b1`

```dockerfile
```

-	Layers:
	-	`sha256:bb8efb89840ee2ef6a38b956f3d6cbdbf3e368f97c83314121ef06c9cc5b3a98`  
		Last Modified: Sat, 15 Feb 2025 10:10:24 GMT  
		Size: 1.1 MB (1074382 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c6663ca7744f97d48d6c22ad8f29c6a45701e956bceefa937ea8e5eeab84f7b`  
		Last Modified: Sat, 15 Feb 2025 10:10:24 GMT  
		Size: 15.1 KB (15071 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.32.3`

```console
$ docker pull telegraf@sha256:3467ba322b199721c0583e684524aedb46d3389b284602c4031bd24b83cfa30d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.32.3` - linux; amd64

```console
$ docker pull telegraf@sha256:133a1f6fad5bdf91291538d0c99b7092cb0227c99a2a63c55d7fe556178fe8aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.5 MB (161472346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:495572a3faa0524733483264fde59a6043400c181d666d4c21592025aa349c95`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 17:23:46 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 17:23:46 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 14 Apr 2025 17:23:46 GMT
ENV TELEGRAF_VERSION=1.32.3
# Mon, 14 Apr 2025 17:23:46 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 14 Apr 2025 17:23:46 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 14 Apr 2025 17:23:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 14 Apr 2025 17:23:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 14 Apr 2025 17:23:46 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:cf05a52c02353f0b2b6f9be0549ac916c3fb1dc8d4bacd405eac7f28562ec9f2`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 48.5 MB (48491199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63964a8518f54dc31f8df89d7f06714c7a793aa1aa08a64ae3d7f4f4f30b4ac8`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 24.0 MB (24011181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c933b6be6e4b5fa149324199e7b0a1c9ccb7cf0ac29ed8b5b9b44fd4408d57f`  
		Last Modified: Thu, 08 May 2025 17:38:15 GMT  
		Size: 18.9 MB (18946492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2b2f6c561c97261c4b0f61c5db60a43d784c78dca5ffd46b06e72090acb250f`  
		Last Modified: Thu, 08 May 2025 17:38:14 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38da449724bdaeb9151e330aa111ac8a64b07fd6504603ca0550fd0ebfebcec9`  
		Last Modified: Thu, 08 May 2025 17:38:20 GMT  
		Size: 70.0 MB (70021066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39ab13a890f276867bb402308d18f401d354b5ea78288c440f5fbaf9d06638c2`  
		Last Modified: Thu, 08 May 2025 17:38:14 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.32.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:9e2f40dd9d9cfb83d681771aa13ce7edc00c799a06c7e66e43660c899244f34c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6438476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86f5e2f11776c992b4e619645c5282d1de67d83d81d6f6913f7ce99728f0d834`

```dockerfile
```

-	Layers:
	-	`sha256:91178148c42fa39443216872b394bb291ff7165babad0a68ec0daef0742a9b66`  
		Last Modified: Mon, 28 Apr 2025 22:21:44 GMT  
		Size: 6.4 MB (6424006 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b2ca0d300a3dcbdfaf1773af9a3ecfed0eacb8c6a204171bd964b13854c8f23`  
		Last Modified: Mon, 28 Apr 2025 22:21:44 GMT  
		Size: 14.5 KB (14470 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.32.3` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:5e0316150e5e96e705c5c10e9bd574da3a1bf96d415875960d5003943fde1f52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.5 MB (148525488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c3a3d3ab0b8e0e43511135d7510bd621f472b0817d860382bfc1731679b779f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 17:23:46 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 17:23:46 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 14 Apr 2025 17:23:46 GMT
ENV TELEGRAF_VERSION=1.32.3
# Mon, 14 Apr 2025 17:23:46 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 14 Apr 2025 17:23:46 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 14 Apr 2025 17:23:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 14 Apr 2025 17:23:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 14 Apr 2025 17:23:46 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:a735d4b4a53e8e11448d15bc50ce4670d54dff52e426cf0510c9b713d3a7ad09`  
		Last Modified: Thu, 08 May 2025 17:04:48 GMT  
		Size: 44.2 MB (44197079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b01e6436acd06b177253a4ba25e5179715088c2f493e89c91bbf6fdc41a2034`  
		Last Modified: Thu, 08 May 2025 17:05:35 GMT  
		Size: 21.9 MB (21918380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eabe566c6af2691f3105823447ac937c1f11b004965e6abc01575a064a841148`  
		Last Modified: Thu, 08 May 2025 19:54:16 GMT  
		Size: 17.7 MB (17724705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2d5c5bcea6d97d32d23b37764468583109ef0810d01e6d83a881b0023fe34ef`  
		Last Modified: Thu, 08 May 2025 19:54:19 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a9c4a9ba46b05c9fc1043c16a2d77b4cd85e76b9604f9d490862d12ff932cf6`  
		Last Modified: Tue, 29 Apr 2025 15:23:41 GMT  
		Size: 64.7 MB (64682927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9250a0aa5455fbe2090dac00f5beda1b9dc530c54587a3d92e23f7622e18113`  
		Last Modified: Tue, 29 Apr 2025 15:23:39 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.32.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:034c3bdc3cf115313c5b638a066e26de7365996d2676afb265e23ddb19a01da8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6433966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b3b5dd92dfdb3de595b994a99c985a3fce8156dd0b81912f7d67dd8fcf1cadd`

```dockerfile
```

-	Layers:
	-	`sha256:4dbcd1380dac15d9db4b21afd6cefc918a92ed82583a3956df06f4e1ea313fd2`  
		Last Modified: Tue, 29 Apr 2025 15:23:39 GMT  
		Size: 6.4 MB (6419410 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3801861fc02d9f777aada0ad295bfca4d677645e8d9c7c2ae063cb8909e5986`  
		Last Modified: Tue, 29 Apr 2025 15:23:38 GMT  
		Size: 14.6 KB (14556 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.32.3` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:ae34603da2c6d4d6f0bb614c276c2fd6b9945aacc49405ab2fdf5acd3e3411b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.9 MB (153897671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:801fd23dffa15d66e19b59a801fc1fcbb041368189b60c2750e60a3e6c0facb1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 17:23:46 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 17:23:46 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 14 Apr 2025 17:23:46 GMT
ENV TELEGRAF_VERSION=1.32.3
# Mon, 14 Apr 2025 17:23:46 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 14 Apr 2025 17:23:46 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 14 Apr 2025 17:23:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 14 Apr 2025 17:23:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 14 Apr 2025 17:23:46 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:de07ba6f486e0ce29760ab32d4381edabbc660a04c493e95eb9a8056925d8955`  
		Last Modified: Thu, 08 May 2025 17:04:44 GMT  
		Size: 48.3 MB (48327644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84649bff67ea459549b6f371f7045d9968d6ebf370b815c922a625f3ab065724`  
		Last Modified: Thu, 08 May 2025 17:04:42 GMT  
		Size: 23.5 MB (23544262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7446c58993d11b00fcf70a65c363df298c8fd24914c3657943f2362852a75e88`  
		Last Modified: Thu, 08 May 2025 17:07:55 GMT  
		Size: 18.9 MB (18871759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38670875debfb321519f19305350d13646a48ebaac8d2b798ab7aa84cefe61b0`  
		Last Modified: Thu, 08 May 2025 17:07:53 GMT  
		Size: 1.8 KB (1782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df5079117dbac2057f98deaff5edbb025897cdcefeaa944b9523223f24fad7c5`  
		Last Modified: Tue, 29 Apr 2025 19:27:35 GMT  
		Size: 63.2 MB (63151600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c6076ec624b8284c1e646b98e2c38bccc71e847a3e241dd13b70b13dfa440eb`  
		Last Modified: Tue, 29 Apr 2025 19:27:33 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.32.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:bc308f54bf5dde871d7ce887ae35355c130fb75bfdf42460544a0d2f15032c59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6439262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae430ca89a2034170876208e34e7d8303ec3efa23f6c75f178f0edfc594d7619`

```dockerfile
```

-	Layers:
	-	`sha256:fe97e3d0ffbbff78b920dcfe801839987317812b123de1de562d8960f800679c`  
		Last Modified: Tue, 29 Apr 2025 19:27:33 GMT  
		Size: 6.4 MB (6424682 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1cca97bd02c75aae00cfeafb6bb4a2d316744bb9accd7d75b970a782882afa73`  
		Last Modified: Tue, 29 Apr 2025 19:27:32 GMT  
		Size: 14.6 KB (14580 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.32.3-alpine`

```console
$ docker pull telegraf@sha256:9613ea0126325721f7087013726dadd23bf0aff8caed38d9337c449cdb66f05b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.32.3-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:3ad9fa3557eec07393d93ba99a10a803a1d358c08aee5b31f11927ed45248331
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75899910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87127c7ae451c11d56da2e3bbdb0133e4fc5465199f4a064700dc7bc1b95f94d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 10 Feb 2025 22:49:00 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
CMD ["/bin/sh"]
# Mon, 10 Feb 2025 22:49:00 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
ENV TELEGRAF_VERSION=1.32.3
# Mon, 10 Feb 2025 22:49:00 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 10 Feb 2025 22:49:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Feb 2025 22:49:00 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 14:35:06 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eb2f8452f18fa5ca6d6eab55873b03df9cb04ec2a5cbef0b0347252dd1f1b98`  
		Last Modified: Fri, 14 Feb 2025 22:10:30 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b1849576e5bfb8707e5b6da1ed76fc1b4642590a5cd627cc954d4458c972b87`  
		Last Modified: Fri, 14 Feb 2025 22:10:31 GMT  
		Size: 2.4 MB (2447977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8976f17c93a72e5f006514ed0e2d593d5fa816d872152c28e428bea70d7a275`  
		Last Modified: Fri, 14 Feb 2025 22:13:09 GMT  
		Size: 69.8 MB (69824429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a0c5ba34859540677e65faaa6f81da813c58e83b5870ad2c8611227ad0b1a0`  
		Last Modified: Fri, 14 Feb 2025 22:10:32 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.32.3-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:6a788cf31b15ae6004a2eb7b8e1abe4b99d5f46318fabad2c75620283de0f097
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1093716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a9834368eb385832d1124281f968481309de1c0912c4bea4bad334e1ee56503`

```dockerfile
```

-	Layers:
	-	`sha256:36d17874c7c519d61791ce6538dcf5b70d8d316102b689fadc4fcbf715597e97`  
		Last Modified: Fri, 14 Feb 2025 22:10:24 GMT  
		Size: 1.1 MB (1078755 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a53875bd2d4d184394b04b7247846ef535add592138dcbbc0131261f51dd4b97`  
		Last Modified: Fri, 14 Feb 2025 22:10:24 GMT  
		Size: 15.0 KB (14961 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.32.3-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:5c131e9d3dfd41b67fbe1efc79eade66effd3013805af278d26b9581ac0535eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.6 MB (69569876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7adaf8892bce40df4e537a256a91cdc51bfcdaf585b04cdc584cdded2e35ab2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 10 Feb 2025 22:49:00 GMT
ADD alpine-minirootfs-3.20.6-aarch64.tar.gz / # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
CMD ["/bin/sh"]
# Mon, 10 Feb 2025 22:49:00 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
ENV TELEGRAF_VERSION=1.32.3
# Mon, 10 Feb 2025 22:49:00 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 10 Feb 2025 22:49:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Feb 2025 22:49:00 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:94e9d8af22013aabf0edcaf42950c88b0a1350c3a9ce076d61b98a535a673dd9`  
		Last Modified: Fri, 14 Feb 2025 14:35:45 GMT  
		Size: 4.1 MB (4091165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a61a5f488a07a5f9b377e1e8af47680d864b0a298fd6acfe930441fecb3ecf84`  
		Last Modified: Sat, 15 Feb 2025 03:20:35 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:976a777ce7d187cf232aae59fd07445827d4a146c69dd2ff0adb80ede2329896`  
		Last Modified: Sat, 15 Feb 2025 10:11:16 GMT  
		Size: 2.5 MB (2533889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cd034834e7dc25546d11a5edde9078270a777c1002a13613255b26db02298a6`  
		Last Modified: Sat, 15 Feb 2025 11:18:03 GMT  
		Size: 62.9 MB (62944215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:570d8419ba9fcec72ee59593f2912c265a2f2650c283c863e9e30235da563b5f`  
		Last Modified: Sat, 15 Feb 2025 11:18:00 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.32.3-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:e951a2565274dbce09494aac2324db6c6f4fe6b0940ca7528fc4c98c8023c85d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1089453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a33f51f8d0f3468d4c73164109a47998bc26ee6bb0739487e7e5c768a16499b1`

```dockerfile
```

-	Layers:
	-	`sha256:bb8efb89840ee2ef6a38b956f3d6cbdbf3e368f97c83314121ef06c9cc5b3a98`  
		Last Modified: Sat, 15 Feb 2025 10:10:24 GMT  
		Size: 1.1 MB (1074382 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c6663ca7744f97d48d6c22ad8f29c6a45701e956bceefa937ea8e5eeab84f7b`  
		Last Modified: Sat, 15 Feb 2025 10:10:24 GMT  
		Size: 15.1 KB (15071 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.33`

```console
$ docker pull telegraf@sha256:f4ee345b1e155464c4959953c84a6caafb66a98ff737d7f22166b2dea341e352
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.33` - linux; amd64

```console
$ docker pull telegraf@sha256:6764fb2994841d7e9ae55b7ef9696f1dbbe11f99f4d4d1f47849abbb4a8fc9e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.8 MB (168761199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcfeac060adc25600860012ae27337864368400144472d21432550661db79d7f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 17:23:46 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 17:23:46 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 14 Apr 2025 17:23:46 GMT
ENV TELEGRAF_VERSION=1.33.3
# Mon, 14 Apr 2025 17:23:46 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 14 Apr 2025 17:23:46 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 14 Apr 2025 17:23:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 14 Apr 2025 17:23:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 14 Apr 2025 17:23:46 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:cf05a52c02353f0b2b6f9be0549ac916c3fb1dc8d4bacd405eac7f28562ec9f2`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 48.5 MB (48491199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63964a8518f54dc31f8df89d7f06714c7a793aa1aa08a64ae3d7f4f4f30b4ac8`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 24.0 MB (24011181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e700090997c55781c95a4c615dd47fc820ab013adec1e07401224614e19f007`  
		Last Modified: Thu, 08 May 2025 17:42:43 GMT  
		Size: 18.9 MB (18946472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06a1a2052ed46625d7c055c38f77b898d54598db5c819c8f5978a140cd680015`  
		Last Modified: Thu, 08 May 2025 17:42:42 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:584d69bd42a00f6cd52d953595e81d6dae5674aa04c58460a05d29e97d028185`  
		Last Modified: Thu, 08 May 2025 17:42:48 GMT  
		Size: 77.3 MB (77309942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb346f0143c8baf0babdb2dcf00e717d9d6c27352039bd21138f533a27526495`  
		Last Modified: Thu, 08 May 2025 17:42:43 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.33` - unknown; unknown

```console
$ docker pull telegraf@sha256:a9336642489a729f518c73d3e8584d2b93e7b15c410faeee300d346b23a447ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6454195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db792edffe8afe73b382876b76841e3381ae132a7273c3b775b4510dad1494d4`

```dockerfile
```

-	Layers:
	-	`sha256:20b2a226d82319ea5b1d6c7683dbcd9b838fb15013454f14c6dacbc60e00b869`  
		Last Modified: Mon, 28 Apr 2025 22:21:40 GMT  
		Size: 6.4 MB (6439725 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00b212f89a69306ae92a430b3fc56f24813333f75ec1bcd4f8078bafafa5b4e5`  
		Last Modified: Mon, 28 Apr 2025 22:21:39 GMT  
		Size: 14.5 KB (14470 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.33` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:20c2d5239f5d5bbc365c9fa7d370f2b55662390aa7d63052d956ff77de98e781
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.9 MB (154918434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97813da38ee654e5f742136eebd752f2f39c040e5b603478ca60730f6cb4ca43`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 17:23:46 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 17:23:46 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 14 Apr 2025 17:23:46 GMT
ENV TELEGRAF_VERSION=1.33.3
# Mon, 14 Apr 2025 17:23:46 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 14 Apr 2025 17:23:46 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 14 Apr 2025 17:23:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 14 Apr 2025 17:23:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 14 Apr 2025 17:23:46 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:a735d4b4a53e8e11448d15bc50ce4670d54dff52e426cf0510c9b713d3a7ad09`  
		Last Modified: Thu, 08 May 2025 17:04:48 GMT  
		Size: 44.2 MB (44197079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b01e6436acd06b177253a4ba25e5179715088c2f493e89c91bbf6fdc41a2034`  
		Last Modified: Thu, 08 May 2025 17:05:35 GMT  
		Size: 21.9 MB (21918380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eabe566c6af2691f3105823447ac937c1f11b004965e6abc01575a064a841148`  
		Last Modified: Thu, 08 May 2025 19:54:16 GMT  
		Size: 17.7 MB (17724705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2d5c5bcea6d97d32d23b37764468583109ef0810d01e6d83a881b0023fe34ef`  
		Last Modified: Thu, 08 May 2025 19:54:19 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85205d5c822eeed530cfce4c53626bb65b4ce190e0677d94e98cccadb9d1e5c2`  
		Last Modified: Tue, 29 Apr 2025 15:24:29 GMT  
		Size: 71.1 MB (71075874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71b5ccdf942f1f4ccb8101c23f9d215b4c023db12590239317da9dd52536bae4`  
		Last Modified: Tue, 29 Apr 2025 15:24:26 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.33` - unknown; unknown

```console
$ docker pull telegraf@sha256:2ba8d1ba743f6005be4731579456a87fca85effa04f2efa46a13c89c9b289e32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6449685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2bfa00018d1226893165072129196f27208d13ed5db91968a7524903d8384da`

```dockerfile
```

-	Layers:
	-	`sha256:70bf6c4520ebabd92211ff5b14b04a15a86d45a0e58c581fa3bb5269b5155110`  
		Last Modified: Tue, 29 Apr 2025 15:24:27 GMT  
		Size: 6.4 MB (6435129 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4fc3a1b9157d76a07038d3a2c0e8446ed7a695f4ae466611402f0645971a3a3a`  
		Last Modified: Tue, 29 Apr 2025 15:24:26 GMT  
		Size: 14.6 KB (14556 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.33` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:494d4fb1f48caefbc565e639b3f414d92afab9bbffdfacd9a49376fbba35c671
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.3 MB (160345762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0433653b0846523890c06435a9eca66c45395f3b5bf33379c819344bd64418e8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 17:23:46 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 17:23:46 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 14 Apr 2025 17:23:46 GMT
ENV TELEGRAF_VERSION=1.33.3
# Mon, 14 Apr 2025 17:23:46 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 14 Apr 2025 17:23:46 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 14 Apr 2025 17:23:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 14 Apr 2025 17:23:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 14 Apr 2025 17:23:46 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:de07ba6f486e0ce29760ab32d4381edabbc660a04c493e95eb9a8056925d8955`  
		Last Modified: Thu, 08 May 2025 17:04:44 GMT  
		Size: 48.3 MB (48327644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84649bff67ea459549b6f371f7045d9968d6ebf370b815c922a625f3ab065724`  
		Last Modified: Thu, 08 May 2025 17:04:42 GMT  
		Size: 23.5 MB (23544262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7446c58993d11b00fcf70a65c363df298c8fd24914c3657943f2362852a75e88`  
		Last Modified: Thu, 08 May 2025 17:07:55 GMT  
		Size: 18.9 MB (18871759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38670875debfb321519f19305350d13646a48ebaac8d2b798ab7aa84cefe61b0`  
		Last Modified: Thu, 08 May 2025 17:07:53 GMT  
		Size: 1.8 KB (1782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04b77e063c80399c1896bacd0968ac87d88a1f34ee69301b4a6b496f792cd326`  
		Last Modified: Tue, 29 Apr 2025 19:28:05 GMT  
		Size: 69.6 MB (69599692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5496791050ee6580b8149e9d08867a94c80fe032b35e0c8fc8f1f21a9d1e75d7`  
		Last Modified: Tue, 29 Apr 2025 19:28:02 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.33` - unknown; unknown

```console
$ docker pull telegraf@sha256:e9a929e70db0a281e9ee159ee24eaacd5c189ecc704c04f6da219d27aad315e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6454981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baab5839aca0a7b135f729df362c0bdbc996dba97f1b6bcb52cdf368ba971201`

```dockerfile
```

-	Layers:
	-	`sha256:3b6c121e1cfef761345154a829497595662ab81bf0e61f329f11870bbf3ba387`  
		Last Modified: Tue, 29 Apr 2025 19:28:02 GMT  
		Size: 6.4 MB (6440401 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e72509c2d6d5fe8b70315c73a6c923c07f1a5e5a9d0ce8d63586644c74a224e0`  
		Last Modified: Tue, 29 Apr 2025 19:28:02 GMT  
		Size: 14.6 KB (14580 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.33-alpine`

```console
$ docker pull telegraf@sha256:bc804829ecc8a436fe7852c14d8e8189f7cbe84a9971410504ad0298ac395c25
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.33-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:307dff9d25edf62e990b02f7427799852b411acf9defbe0a746da41334fc2280
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.2 MB (83181342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00a2f2610a65d4727686a80d149dec5e8eabc84964f8672c121ae59bf5129b0f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Tue, 25 Feb 2025 19:20:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 25 Feb 2025 19:20:46 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Tue, 25 Feb 2025 19:20:46 GMT
ENV TELEGRAF_VERSION=1.33.3
# Tue, 25 Feb 2025 19:20:46 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Tue, 25 Feb 2025 19:20:46 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 25 Feb 2025 19:20:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 25 Feb 2025 19:20:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 25 Feb 2025 19:20:46 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 14:35:06 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38049afbf35aebc48750aa922431b39f2fc798c04bdbe76bd6ae3b281fed2ba5`  
		Last Modified: Thu, 08 May 2025 19:55:06 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:073bd82841c579643840dc44375728fdc6290a0b75a5c7c7a9f475e2fd33df5c`  
		Last Modified: Thu, 08 May 2025 19:55:07 GMT  
		Size: 2.4 MB (2448010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:804d0c3c2f1304b11b15aa3615c2ae951b7aa267345cd8caebf2534c09f432c4`  
		Last Modified: Thu, 08 May 2025 19:55:11 GMT  
		Size: 77.1 MB (77105828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fecb0ae4356bd231d8a07dbc4b04fad1e156e8bcf1f303290303cee493817e28`  
		Last Modified: Thu, 08 May 2025 19:55:07 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.33-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:c7da2eb2660beb59ed82ea1425fe6e4bb730c61f69a7197c2ed08ebc3cdc021d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1110039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:028284213fd46027a1ced219a906753338d9c763850718d8f063be618ea2b50f`

```dockerfile
```

-	Layers:
	-	`sha256:f43b03bb1a8042cca6df1e56fbc4d2705ce1afa316953c6a42fa05d0dd301ff3`  
		Last Modified: Tue, 25 Feb 2025 23:27:37 GMT  
		Size: 1.1 MB (1094776 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b15e5bf904084afce0335a323cb7a49eb0e277254fb8c1ce8618e0518df0650`  
		Last Modified: Tue, 25 Feb 2025 23:27:36 GMT  
		Size: 15.3 KB (15263 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.33-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:a43e4a027c5584945633041b846be6f9fcf9a440ba9dc357ce3b5ce86c7dd4f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.0 MB (76021133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8591b770895f10d03fe40dc2f2b0cd25b81c7f2ead94a86a0521e60712ee2ed6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Tue, 25 Feb 2025 19:20:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 25 Feb 2025 19:20:46 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Tue, 25 Feb 2025 19:20:46 GMT
ENV TELEGRAF_VERSION=1.33.3
# Tue, 25 Feb 2025 19:20:46 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Tue, 25 Feb 2025 19:20:46 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 25 Feb 2025 19:20:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 25 Feb 2025 19:20:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 25 Feb 2025 19:20:46 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:94e9d8af22013aabf0edcaf42950c88b0a1350c3a9ce076d61b98a535a673dd9`  
		Last Modified: Fri, 14 Feb 2025 14:35:45 GMT  
		Size: 4.1 MB (4091165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a61a5f488a07a5f9b377e1e8af47680d864b0a298fd6acfe930441fecb3ecf84`  
		Last Modified: Sat, 15 Feb 2025 03:20:35 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:976a777ce7d187cf232aae59fd07445827d4a146c69dd2ff0adb80ede2329896`  
		Last Modified: Sat, 15 Feb 2025 10:11:16 GMT  
		Size: 2.5 MB (2533889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb755c12ce2b641e186784c9d65629a9e336edd2adbfc1769a50ca60cc9d39c7`  
		Last Modified: Wed, 26 Feb 2025 00:01:21 GMT  
		Size: 69.4 MB (69395470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0cb2567b59e86792e2fb28a415d81a683488ae3254f26baf29d93ab79827052`  
		Last Modified: Wed, 26 Feb 2025 00:01:19 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.33-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:8859417a657434c92362fd7628b01aa683b21e0131e15a12d1b8db1e6adc949b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1105800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2279b435bd3fccc85c118d273f224fa5d354af37b7f133bebe2b97de2e263235`

```dockerfile
```

-	Layers:
	-	`sha256:75cfdceac3bea7f46c668c49082e6a34da449c79fac4278cdb6a9095936d12b0`  
		Last Modified: Wed, 26 Feb 2025 00:01:19 GMT  
		Size: 1.1 MB (1090415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5040171f06da0c2a54629d1c7e68fd289af078d85e7686d7a27924345d07e654`  
		Last Modified: Wed, 26 Feb 2025 00:01:19 GMT  
		Size: 15.4 KB (15385 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.33.3`

```console
$ docker pull telegraf@sha256:f4ee345b1e155464c4959953c84a6caafb66a98ff737d7f22166b2dea341e352
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.33.3` - linux; amd64

```console
$ docker pull telegraf@sha256:6764fb2994841d7e9ae55b7ef9696f1dbbe11f99f4d4d1f47849abbb4a8fc9e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.8 MB (168761199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcfeac060adc25600860012ae27337864368400144472d21432550661db79d7f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 17:23:46 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 17:23:46 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 14 Apr 2025 17:23:46 GMT
ENV TELEGRAF_VERSION=1.33.3
# Mon, 14 Apr 2025 17:23:46 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 14 Apr 2025 17:23:46 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 14 Apr 2025 17:23:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 14 Apr 2025 17:23:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 14 Apr 2025 17:23:46 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:cf05a52c02353f0b2b6f9be0549ac916c3fb1dc8d4bacd405eac7f28562ec9f2`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 48.5 MB (48491199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63964a8518f54dc31f8df89d7f06714c7a793aa1aa08a64ae3d7f4f4f30b4ac8`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 24.0 MB (24011181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e700090997c55781c95a4c615dd47fc820ab013adec1e07401224614e19f007`  
		Last Modified: Thu, 08 May 2025 17:42:43 GMT  
		Size: 18.9 MB (18946472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06a1a2052ed46625d7c055c38f77b898d54598db5c819c8f5978a140cd680015`  
		Last Modified: Thu, 08 May 2025 17:42:42 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:584d69bd42a00f6cd52d953595e81d6dae5674aa04c58460a05d29e97d028185`  
		Last Modified: Thu, 08 May 2025 17:42:48 GMT  
		Size: 77.3 MB (77309942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb346f0143c8baf0babdb2dcf00e717d9d6c27352039bd21138f533a27526495`  
		Last Modified: Thu, 08 May 2025 17:42:43 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.33.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:a9336642489a729f518c73d3e8584d2b93e7b15c410faeee300d346b23a447ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6454195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db792edffe8afe73b382876b76841e3381ae132a7273c3b775b4510dad1494d4`

```dockerfile
```

-	Layers:
	-	`sha256:20b2a226d82319ea5b1d6c7683dbcd9b838fb15013454f14c6dacbc60e00b869`  
		Last Modified: Mon, 28 Apr 2025 22:21:40 GMT  
		Size: 6.4 MB (6439725 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00b212f89a69306ae92a430b3fc56f24813333f75ec1bcd4f8078bafafa5b4e5`  
		Last Modified: Mon, 28 Apr 2025 22:21:39 GMT  
		Size: 14.5 KB (14470 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.33.3` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:20c2d5239f5d5bbc365c9fa7d370f2b55662390aa7d63052d956ff77de98e781
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.9 MB (154918434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97813da38ee654e5f742136eebd752f2f39c040e5b603478ca60730f6cb4ca43`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 17:23:46 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 17:23:46 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 14 Apr 2025 17:23:46 GMT
ENV TELEGRAF_VERSION=1.33.3
# Mon, 14 Apr 2025 17:23:46 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 14 Apr 2025 17:23:46 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 14 Apr 2025 17:23:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 14 Apr 2025 17:23:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 14 Apr 2025 17:23:46 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:a735d4b4a53e8e11448d15bc50ce4670d54dff52e426cf0510c9b713d3a7ad09`  
		Last Modified: Thu, 08 May 2025 17:04:48 GMT  
		Size: 44.2 MB (44197079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b01e6436acd06b177253a4ba25e5179715088c2f493e89c91bbf6fdc41a2034`  
		Last Modified: Thu, 08 May 2025 17:05:35 GMT  
		Size: 21.9 MB (21918380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eabe566c6af2691f3105823447ac937c1f11b004965e6abc01575a064a841148`  
		Last Modified: Thu, 08 May 2025 19:54:16 GMT  
		Size: 17.7 MB (17724705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2d5c5bcea6d97d32d23b37764468583109ef0810d01e6d83a881b0023fe34ef`  
		Last Modified: Thu, 08 May 2025 19:54:19 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85205d5c822eeed530cfce4c53626bb65b4ce190e0677d94e98cccadb9d1e5c2`  
		Last Modified: Tue, 29 Apr 2025 15:24:29 GMT  
		Size: 71.1 MB (71075874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71b5ccdf942f1f4ccb8101c23f9d215b4c023db12590239317da9dd52536bae4`  
		Last Modified: Tue, 29 Apr 2025 15:24:26 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.33.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:2ba8d1ba743f6005be4731579456a87fca85effa04f2efa46a13c89c9b289e32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6449685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2bfa00018d1226893165072129196f27208d13ed5db91968a7524903d8384da`

```dockerfile
```

-	Layers:
	-	`sha256:70bf6c4520ebabd92211ff5b14b04a15a86d45a0e58c581fa3bb5269b5155110`  
		Last Modified: Tue, 29 Apr 2025 15:24:27 GMT  
		Size: 6.4 MB (6435129 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4fc3a1b9157d76a07038d3a2c0e8446ed7a695f4ae466611402f0645971a3a3a`  
		Last Modified: Tue, 29 Apr 2025 15:24:26 GMT  
		Size: 14.6 KB (14556 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.33.3` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:494d4fb1f48caefbc565e639b3f414d92afab9bbffdfacd9a49376fbba35c671
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.3 MB (160345762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0433653b0846523890c06435a9eca66c45395f3b5bf33379c819344bd64418e8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 17:23:46 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 17:23:46 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 14 Apr 2025 17:23:46 GMT
ENV TELEGRAF_VERSION=1.33.3
# Mon, 14 Apr 2025 17:23:46 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 14 Apr 2025 17:23:46 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 14 Apr 2025 17:23:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 14 Apr 2025 17:23:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 14 Apr 2025 17:23:46 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:de07ba6f486e0ce29760ab32d4381edabbc660a04c493e95eb9a8056925d8955`  
		Last Modified: Thu, 08 May 2025 17:04:44 GMT  
		Size: 48.3 MB (48327644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84649bff67ea459549b6f371f7045d9968d6ebf370b815c922a625f3ab065724`  
		Last Modified: Thu, 08 May 2025 17:04:42 GMT  
		Size: 23.5 MB (23544262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7446c58993d11b00fcf70a65c363df298c8fd24914c3657943f2362852a75e88`  
		Last Modified: Thu, 08 May 2025 17:07:55 GMT  
		Size: 18.9 MB (18871759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38670875debfb321519f19305350d13646a48ebaac8d2b798ab7aa84cefe61b0`  
		Last Modified: Thu, 08 May 2025 17:07:53 GMT  
		Size: 1.8 KB (1782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04b77e063c80399c1896bacd0968ac87d88a1f34ee69301b4a6b496f792cd326`  
		Last Modified: Tue, 29 Apr 2025 19:28:05 GMT  
		Size: 69.6 MB (69599692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5496791050ee6580b8149e9d08867a94c80fe032b35e0c8fc8f1f21a9d1e75d7`  
		Last Modified: Tue, 29 Apr 2025 19:28:02 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.33.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:e9a929e70db0a281e9ee159ee24eaacd5c189ecc704c04f6da219d27aad315e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6454981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baab5839aca0a7b135f729df362c0bdbc996dba97f1b6bcb52cdf368ba971201`

```dockerfile
```

-	Layers:
	-	`sha256:3b6c121e1cfef761345154a829497595662ab81bf0e61f329f11870bbf3ba387`  
		Last Modified: Tue, 29 Apr 2025 19:28:02 GMT  
		Size: 6.4 MB (6440401 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e72509c2d6d5fe8b70315c73a6c923c07f1a5e5a9d0ce8d63586644c74a224e0`  
		Last Modified: Tue, 29 Apr 2025 19:28:02 GMT  
		Size: 14.6 KB (14580 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.33.3-alpine`

```console
$ docker pull telegraf@sha256:bc804829ecc8a436fe7852c14d8e8189f7cbe84a9971410504ad0298ac395c25
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.33.3-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:307dff9d25edf62e990b02f7427799852b411acf9defbe0a746da41334fc2280
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.2 MB (83181342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00a2f2610a65d4727686a80d149dec5e8eabc84964f8672c121ae59bf5129b0f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Tue, 25 Feb 2025 19:20:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 25 Feb 2025 19:20:46 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Tue, 25 Feb 2025 19:20:46 GMT
ENV TELEGRAF_VERSION=1.33.3
# Tue, 25 Feb 2025 19:20:46 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Tue, 25 Feb 2025 19:20:46 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 25 Feb 2025 19:20:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 25 Feb 2025 19:20:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 25 Feb 2025 19:20:46 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 14:35:06 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38049afbf35aebc48750aa922431b39f2fc798c04bdbe76bd6ae3b281fed2ba5`  
		Last Modified: Thu, 08 May 2025 19:55:06 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:073bd82841c579643840dc44375728fdc6290a0b75a5c7c7a9f475e2fd33df5c`  
		Last Modified: Thu, 08 May 2025 19:55:07 GMT  
		Size: 2.4 MB (2448010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:804d0c3c2f1304b11b15aa3615c2ae951b7aa267345cd8caebf2534c09f432c4`  
		Last Modified: Thu, 08 May 2025 19:55:11 GMT  
		Size: 77.1 MB (77105828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fecb0ae4356bd231d8a07dbc4b04fad1e156e8bcf1f303290303cee493817e28`  
		Last Modified: Thu, 08 May 2025 19:55:07 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.33.3-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:c7da2eb2660beb59ed82ea1425fe6e4bb730c61f69a7197c2ed08ebc3cdc021d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1110039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:028284213fd46027a1ced219a906753338d9c763850718d8f063be618ea2b50f`

```dockerfile
```

-	Layers:
	-	`sha256:f43b03bb1a8042cca6df1e56fbc4d2705ce1afa316953c6a42fa05d0dd301ff3`  
		Last Modified: Tue, 25 Feb 2025 23:27:37 GMT  
		Size: 1.1 MB (1094776 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b15e5bf904084afce0335a323cb7a49eb0e277254fb8c1ce8618e0518df0650`  
		Last Modified: Tue, 25 Feb 2025 23:27:36 GMT  
		Size: 15.3 KB (15263 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.33.3-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:a43e4a027c5584945633041b846be6f9fcf9a440ba9dc357ce3b5ce86c7dd4f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.0 MB (76021133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8591b770895f10d03fe40dc2f2b0cd25b81c7f2ead94a86a0521e60712ee2ed6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Tue, 25 Feb 2025 19:20:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 25 Feb 2025 19:20:46 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Tue, 25 Feb 2025 19:20:46 GMT
ENV TELEGRAF_VERSION=1.33.3
# Tue, 25 Feb 2025 19:20:46 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Tue, 25 Feb 2025 19:20:46 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 25 Feb 2025 19:20:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 25 Feb 2025 19:20:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 25 Feb 2025 19:20:46 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:94e9d8af22013aabf0edcaf42950c88b0a1350c3a9ce076d61b98a535a673dd9`  
		Last Modified: Fri, 14 Feb 2025 14:35:45 GMT  
		Size: 4.1 MB (4091165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a61a5f488a07a5f9b377e1e8af47680d864b0a298fd6acfe930441fecb3ecf84`  
		Last Modified: Sat, 15 Feb 2025 03:20:35 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:976a777ce7d187cf232aae59fd07445827d4a146c69dd2ff0adb80ede2329896`  
		Last Modified: Sat, 15 Feb 2025 10:11:16 GMT  
		Size: 2.5 MB (2533889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb755c12ce2b641e186784c9d65629a9e336edd2adbfc1769a50ca60cc9d39c7`  
		Last Modified: Wed, 26 Feb 2025 00:01:21 GMT  
		Size: 69.4 MB (69395470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0cb2567b59e86792e2fb28a415d81a683488ae3254f26baf29d93ab79827052`  
		Last Modified: Wed, 26 Feb 2025 00:01:19 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.33.3-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:8859417a657434c92362fd7628b01aa683b21e0131e15a12d1b8db1e6adc949b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1105800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2279b435bd3fccc85c118d273f224fa5d354af37b7f133bebe2b97de2e263235`

```dockerfile
```

-	Layers:
	-	`sha256:75cfdceac3bea7f46c668c49082e6a34da449c79fac4278cdb6a9095936d12b0`  
		Last Modified: Wed, 26 Feb 2025 00:01:19 GMT  
		Size: 1.1 MB (1090415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5040171f06da0c2a54629d1c7e68fd289af078d85e7686d7a27924345d07e654`  
		Last Modified: Wed, 26 Feb 2025 00:01:19 GMT  
		Size: 15.4 KB (15385 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.34`

```console
$ docker pull telegraf@sha256:80c2d6e3e421382ace42eb38c125b9b482dc20996693f4ab1967b2e8e76590d2
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
$ docker pull telegraf@sha256:49b40dd64751da9cfd0d9b030e128c216d6c393412a129991b4c1f7f3fd85f18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.6 MB (168648209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:519e6e29ffe0a7e938ab4f90499d0c11d5c0b4f42bdaf123e25d804909e91365`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 05 May 2025 20:28:05 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 05 May 2025 20:28:05 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 05 May 2025 20:28:05 GMT
ENV TELEGRAF_VERSION=1.34.3
# Mon, 05 May 2025 20:28:05 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 05 May 2025 20:28:05 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 05 May 2025 20:28:05 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 05 May 2025 20:28:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 05 May 2025 20:28:05 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:cf05a52c02353f0b2b6f9be0549ac916c3fb1dc8d4bacd405eac7f28562ec9f2`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 48.5 MB (48491199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63964a8518f54dc31f8df89d7f06714c7a793aa1aa08a64ae3d7f4f4f30b4ac8`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 24.0 MB (24011181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dacc14b4e0bdc5194a2c8473cb1b6c87502ade9e518dd4fc860d6e2b92fabc2`  
		Last Modified: Thu, 08 May 2025 17:05:09 GMT  
		Size: 18.9 MB (18946555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60feec1ed28bf204a6705b299fb6150e3fdc5b79525f640a479f05fee0ecdb59`  
		Last Modified: Thu, 08 May 2025 17:05:28 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acbdec894ca78c4fe47dd8ac0c9f441acfa4578ed79e781c0279e94ff19c9119`  
		Last Modified: Thu, 08 May 2025 17:05:14 GMT  
		Size: 77.2 MB (77196866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01b51d74a199fd95947ea33f9ec3514fffab3a8ef9246bded84a400656d77c13`  
		Last Modified: Thu, 08 May 2025 17:04:49 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.34` - unknown; unknown

```console
$ docker pull telegraf@sha256:e53a298f46a8e7d1885bd3a2dc4d41d6b1c6c364de7dc6bcc3d402aece988750
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6461031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7b59d75249146d4adb68eeb664ac0c1b8e17da560f7cc77c91bc4a415a40c96`

```dockerfile
```

-	Layers:
	-	`sha256:6addf961b16060916a345fcbd3b60d5df5d9ed1bf254dc43270a16f915aadded`  
		Last Modified: Mon, 05 May 2025 21:43:54 GMT  
		Size: 6.4 MB (6446259 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d627eade19e5b07c1115be617fce2ade5b596bfc798f27899b1661106aa11d28`  
		Last Modified: Mon, 05 May 2025 21:43:54 GMT  
		Size: 14.8 KB (14772 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.34` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:acacb2a9994c771837719bde79a0b3cf3bd213810fcaa937e2e7e41f76911ab0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.2 MB (155159090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:396350dfa8d3a9e70655ebd921574d6889182c536c05c1a62e5b641257271105`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 05 May 2025 20:28:05 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 05 May 2025 20:28:05 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 05 May 2025 20:28:05 GMT
ENV TELEGRAF_VERSION=1.34.3
# Mon, 05 May 2025 20:28:05 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 05 May 2025 20:28:05 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 05 May 2025 20:28:05 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 05 May 2025 20:28:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 05 May 2025 20:28:05 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:a735d4b4a53e8e11448d15bc50ce4670d54dff52e426cf0510c9b713d3a7ad09`  
		Last Modified: Thu, 08 May 2025 17:04:48 GMT  
		Size: 44.2 MB (44197079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b01e6436acd06b177253a4ba25e5179715088c2f493e89c91bbf6fdc41a2034`  
		Last Modified: Thu, 08 May 2025 17:05:35 GMT  
		Size: 21.9 MB (21918380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eabe566c6af2691f3105823447ac937c1f11b004965e6abc01575a064a841148`  
		Last Modified: Thu, 08 May 2025 19:54:16 GMT  
		Size: 17.7 MB (17724705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2d5c5bcea6d97d32d23b37764468583109ef0810d01e6d83a881b0023fe34ef`  
		Last Modified: Thu, 08 May 2025 19:54:19 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04ee6f04b91006925ceab7576921c368aa0075806393b4fdd1c8b77f9ff99287`  
		Last Modified: Mon, 05 May 2025 21:43:55 GMT  
		Size: 71.3 MB (71316530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bbffd0f20d8462cede56db1171d487ce44cc115861b1bca0b1ae366dc13aae2`  
		Last Modified: Thu, 08 May 2025 19:54:21 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.34` - unknown; unknown

```console
$ docker pull telegraf@sha256:43aef8fa73b7066f2c6c1fb05ca46bd0e50db98f3c72b05ddd927037cd4482b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6455728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6545d34a2fcec0c4881d7fa165c598c9ca3714d3d120fdf1e468f4b6173cb87c`

```dockerfile
```

-	Layers:
	-	`sha256:dcb63a79fb52b2c69a956ef3e1703d26d3b33188a387457170ad1b189bb81726`  
		Last Modified: Mon, 05 May 2025 21:43:53 GMT  
		Size: 6.4 MB (6440862 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76b89b32d4be35cd37dabeca683f8fd271c5f757168e9a1cd18eb5739a8a8e16`  
		Last Modified: Mon, 05 May 2025 21:43:53 GMT  
		Size: 14.9 KB (14866 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.34` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:7236866cd0c185414043e05d17134a659c925307be4df7b08c0c1be8b964b02f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.7 MB (160741620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:543f8780e6330b59dfb5ffb9c60d1a98c5c1132b8e861bfe92539aaca3f620ac`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 05 May 2025 20:28:05 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 05 May 2025 20:28:05 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 05 May 2025 20:28:05 GMT
ENV TELEGRAF_VERSION=1.34.3
# Mon, 05 May 2025 20:28:05 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 05 May 2025 20:28:05 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 05 May 2025 20:28:05 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 05 May 2025 20:28:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 05 May 2025 20:28:05 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:de07ba6f486e0ce29760ab32d4381edabbc660a04c493e95eb9a8056925d8955`  
		Last Modified: Thu, 08 May 2025 17:04:44 GMT  
		Size: 48.3 MB (48327644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84649bff67ea459549b6f371f7045d9968d6ebf370b815c922a625f3ab065724`  
		Last Modified: Thu, 08 May 2025 17:04:42 GMT  
		Size: 23.5 MB (23544262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7446c58993d11b00fcf70a65c363df298c8fd24914c3657943f2362852a75e88`  
		Last Modified: Thu, 08 May 2025 17:07:55 GMT  
		Size: 18.9 MB (18871759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38670875debfb321519f19305350d13646a48ebaac8d2b798ab7aa84cefe61b0`  
		Last Modified: Thu, 08 May 2025 17:07:53 GMT  
		Size: 1.8 KB (1782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f36787a5ee1c46394cceb50e0a896ee120448916cbad47fc0217040703e6e7a`  
		Last Modified: Thu, 08 May 2025 17:08:01 GMT  
		Size: 70.0 MB (69995550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3536c1dd589a2ac2c4c00c4cd04745d4d4e332fdae5ec2ff5d532014e0c07f6`  
		Last Modified: Thu, 08 May 2025 17:07:53 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.34` - unknown; unknown

```console
$ docker pull telegraf@sha256:9cef8234a18e2bced21cf4ae272a9d369c7877266b3cc91a30dc0730b781eb41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6461841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07fb57fe16b24773c7424ca1c0442e97df1436abfe3618ac00589a1de84457fc`

```dockerfile
```

-	Layers:
	-	`sha256:353f0e0d864a7a3999c226d18d1ab5b5cb6807ec88724876ccba00c3d8dcf486`  
		Last Modified: Tue, 06 May 2025 02:06:29 GMT  
		Size: 6.4 MB (6446947 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1220a2a4a2dc3d9f0273f3ef0a58d42b992b9f7be92783d32b58495669cafb3`  
		Last Modified: Tue, 06 May 2025 02:06:28 GMT  
		Size: 14.9 KB (14894 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.34-alpine`

```console
$ docker pull telegraf@sha256:2e19df3142f74083fa1ec0ee98901a277971e144fae9a49bca21aeecddadb6be
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.34-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:645c9bfb6439247ce432fa016aa288a7c063b546dcccc1a1efbd2047ade7a000
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.1 MB (83066472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fd00bc80283e5dee38fcda1db589eb3f70d4ad664d029b857f5a315a414d7bb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Mon, 05 May 2025 20:28:05 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 05 May 2025 20:28:05 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 05 May 2025 20:28:05 GMT
ENV TELEGRAF_VERSION=1.34.3
# Mon, 05 May 2025 20:28:05 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 05 May 2025 20:28:05 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 05 May 2025 20:28:05 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 05 May 2025 20:28:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 05 May 2025 20:28:05 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 14:35:06 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e036f026e2ca6ce0fb410d4555de5d0b0d3e8228adc8d209c04e482abbd86453`  
		Last Modified: Thu, 08 May 2025 17:05:41 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb0861b20c0225a79f2e78e27dc922e52c78082d6a774646a4d2d8f7548508a7`  
		Last Modified: Thu, 08 May 2025 17:05:41 GMT  
		Size: 2.4 MB (2449575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55d80681ba2be41917f5f0ee9aa4583465fe80682feff10dce7ac9d8787ca085`  
		Last Modified: Thu, 08 May 2025 17:05:48 GMT  
		Size: 77.0 MB (76989395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6f559c698c5228b31a27032040a2e50b37d397a2bc72fe8c569fe8ae8b4d28c`  
		Last Modified: Thu, 08 May 2025 17:05:43 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.34-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:b776a430c712f166e58d64205f9395ff4831bd55f8bf69786e3f0ed8ac68bc43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1116095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:000dd7750d7df88059611520d73ca93811803be83a179ce099a8a6c0ad12539a`

```dockerfile
```

-	Layers:
	-	`sha256:f7220dd330064a19390f85ae82c72a2dacdb31e562fc20818899cc094e0bd61d`  
		Last Modified: Thu, 08 May 2025 17:18:24 GMT  
		Size: 1.1 MB (1100832 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0433ef5061b69291b9e8aafea4752870b788cb583117e263f986c7c56363ceae`  
		Last Modified: Thu, 08 May 2025 17:18:23 GMT  
		Size: 15.3 KB (15263 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.34-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:68cd1d14ab575884f986f51fce537a3bddf30ce7549ba3988937cd2f1b0949bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.4 MB (76418004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24e6f62920d3e2d73423452627351881ed3c5a054c44883ea45eec858dc5575a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Mon, 05 May 2025 20:28:05 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 05 May 2025 20:28:05 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 05 May 2025 20:28:05 GMT
ENV TELEGRAF_VERSION=1.34.3
# Mon, 05 May 2025 20:28:05 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 05 May 2025 20:28:05 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 05 May 2025 20:28:05 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 05 May 2025 20:28:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 05 May 2025 20:28:05 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:94e9d8af22013aabf0edcaf42950c88b0a1350c3a9ce076d61b98a535a673dd9`  
		Last Modified: Fri, 14 Feb 2025 14:35:45 GMT  
		Size: 4.1 MB (4091165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:434c8ed1b411bf87e31d51dcd5e11ad29b842c6ac23d29867f58c9b6657217f9`  
		Last Modified: Thu, 08 May 2025 17:16:04 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d509229eaab440944eafb92883af0415ca875e0db2665add61e48bfe43f6b4dd`  
		Last Modified: Thu, 08 May 2025 17:16:06 GMT  
		Size: 2.5 MB (2535687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23c7c4b61f32dbb4ada9f4d0a285db0eecb9e3184c28b45c375020c4b7cb3a59`  
		Last Modified: Thu, 08 May 2025 17:16:14 GMT  
		Size: 69.8 MB (69790548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b4c2e91ab15daceb80fd337395a9c5ab3793298495749ff949b046e665a1938`  
		Last Modified: Thu, 08 May 2025 17:16:05 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.34-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:3676f10d7f2e1cffd8a87077aa981add2eda7f67129c7500bfa8616e73bd5ca8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1111856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f9ce31efac00e0ee13c4a6b2494564a069c7e7262edfc5d4507253ae576b4ea`

```dockerfile
```

-	Layers:
	-	`sha256:99177517ca325a8d873c732ad1ce28e40f9dcf9a28bb766712177cbcf9f16775`  
		Last Modified: Thu, 08 May 2025 17:18:25 GMT  
		Size: 1.1 MB (1096471 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf602a6b5044f56bc88a87ee5516d257fc98641926b1d1ea0f918d509c2fa83b`  
		Last Modified: Thu, 08 May 2025 17:18:23 GMT  
		Size: 15.4 KB (15385 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.34.3`

```console
$ docker pull telegraf@sha256:80c2d6e3e421382ace42eb38c125b9b482dc20996693f4ab1967b2e8e76590d2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.34.3` - linux; amd64

```console
$ docker pull telegraf@sha256:49b40dd64751da9cfd0d9b030e128c216d6c393412a129991b4c1f7f3fd85f18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.6 MB (168648209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:519e6e29ffe0a7e938ab4f90499d0c11d5c0b4f42bdaf123e25d804909e91365`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 05 May 2025 20:28:05 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 05 May 2025 20:28:05 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 05 May 2025 20:28:05 GMT
ENV TELEGRAF_VERSION=1.34.3
# Mon, 05 May 2025 20:28:05 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 05 May 2025 20:28:05 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 05 May 2025 20:28:05 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 05 May 2025 20:28:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 05 May 2025 20:28:05 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:cf05a52c02353f0b2b6f9be0549ac916c3fb1dc8d4bacd405eac7f28562ec9f2`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 48.5 MB (48491199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63964a8518f54dc31f8df89d7f06714c7a793aa1aa08a64ae3d7f4f4f30b4ac8`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 24.0 MB (24011181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dacc14b4e0bdc5194a2c8473cb1b6c87502ade9e518dd4fc860d6e2b92fabc2`  
		Last Modified: Thu, 08 May 2025 17:05:09 GMT  
		Size: 18.9 MB (18946555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60feec1ed28bf204a6705b299fb6150e3fdc5b79525f640a479f05fee0ecdb59`  
		Last Modified: Thu, 08 May 2025 17:05:28 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acbdec894ca78c4fe47dd8ac0c9f441acfa4578ed79e781c0279e94ff19c9119`  
		Last Modified: Thu, 08 May 2025 17:05:14 GMT  
		Size: 77.2 MB (77196866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01b51d74a199fd95947ea33f9ec3514fffab3a8ef9246bded84a400656d77c13`  
		Last Modified: Thu, 08 May 2025 17:04:49 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.34.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:e53a298f46a8e7d1885bd3a2dc4d41d6b1c6c364de7dc6bcc3d402aece988750
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6461031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7b59d75249146d4adb68eeb664ac0c1b8e17da560f7cc77c91bc4a415a40c96`

```dockerfile
```

-	Layers:
	-	`sha256:6addf961b16060916a345fcbd3b60d5df5d9ed1bf254dc43270a16f915aadded`  
		Last Modified: Mon, 05 May 2025 21:43:54 GMT  
		Size: 6.4 MB (6446259 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d627eade19e5b07c1115be617fce2ade5b596bfc798f27899b1661106aa11d28`  
		Last Modified: Mon, 05 May 2025 21:43:54 GMT  
		Size: 14.8 KB (14772 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.34.3` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:acacb2a9994c771837719bde79a0b3cf3bd213810fcaa937e2e7e41f76911ab0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.2 MB (155159090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:396350dfa8d3a9e70655ebd921574d6889182c536c05c1a62e5b641257271105`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 05 May 2025 20:28:05 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 05 May 2025 20:28:05 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 05 May 2025 20:28:05 GMT
ENV TELEGRAF_VERSION=1.34.3
# Mon, 05 May 2025 20:28:05 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 05 May 2025 20:28:05 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 05 May 2025 20:28:05 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 05 May 2025 20:28:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 05 May 2025 20:28:05 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:a735d4b4a53e8e11448d15bc50ce4670d54dff52e426cf0510c9b713d3a7ad09`  
		Last Modified: Thu, 08 May 2025 17:04:48 GMT  
		Size: 44.2 MB (44197079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b01e6436acd06b177253a4ba25e5179715088c2f493e89c91bbf6fdc41a2034`  
		Last Modified: Thu, 08 May 2025 17:05:35 GMT  
		Size: 21.9 MB (21918380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eabe566c6af2691f3105823447ac937c1f11b004965e6abc01575a064a841148`  
		Last Modified: Thu, 08 May 2025 19:54:16 GMT  
		Size: 17.7 MB (17724705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2d5c5bcea6d97d32d23b37764468583109ef0810d01e6d83a881b0023fe34ef`  
		Last Modified: Thu, 08 May 2025 19:54:19 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04ee6f04b91006925ceab7576921c368aa0075806393b4fdd1c8b77f9ff99287`  
		Last Modified: Mon, 05 May 2025 21:43:55 GMT  
		Size: 71.3 MB (71316530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bbffd0f20d8462cede56db1171d487ce44cc115861b1bca0b1ae366dc13aae2`  
		Last Modified: Thu, 08 May 2025 19:54:21 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.34.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:43aef8fa73b7066f2c6c1fb05ca46bd0e50db98f3c72b05ddd927037cd4482b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6455728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6545d34a2fcec0c4881d7fa165c598c9ca3714d3d120fdf1e468f4b6173cb87c`

```dockerfile
```

-	Layers:
	-	`sha256:dcb63a79fb52b2c69a956ef3e1703d26d3b33188a387457170ad1b189bb81726`  
		Last Modified: Mon, 05 May 2025 21:43:53 GMT  
		Size: 6.4 MB (6440862 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76b89b32d4be35cd37dabeca683f8fd271c5f757168e9a1cd18eb5739a8a8e16`  
		Last Modified: Mon, 05 May 2025 21:43:53 GMT  
		Size: 14.9 KB (14866 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.34.3` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:7236866cd0c185414043e05d17134a659c925307be4df7b08c0c1be8b964b02f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.7 MB (160741620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:543f8780e6330b59dfb5ffb9c60d1a98c5c1132b8e861bfe92539aaca3f620ac`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 05 May 2025 20:28:05 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 05 May 2025 20:28:05 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 05 May 2025 20:28:05 GMT
ENV TELEGRAF_VERSION=1.34.3
# Mon, 05 May 2025 20:28:05 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 05 May 2025 20:28:05 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 05 May 2025 20:28:05 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 05 May 2025 20:28:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 05 May 2025 20:28:05 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:de07ba6f486e0ce29760ab32d4381edabbc660a04c493e95eb9a8056925d8955`  
		Last Modified: Thu, 08 May 2025 17:04:44 GMT  
		Size: 48.3 MB (48327644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84649bff67ea459549b6f371f7045d9968d6ebf370b815c922a625f3ab065724`  
		Last Modified: Thu, 08 May 2025 17:04:42 GMT  
		Size: 23.5 MB (23544262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7446c58993d11b00fcf70a65c363df298c8fd24914c3657943f2362852a75e88`  
		Last Modified: Thu, 08 May 2025 17:07:55 GMT  
		Size: 18.9 MB (18871759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38670875debfb321519f19305350d13646a48ebaac8d2b798ab7aa84cefe61b0`  
		Last Modified: Thu, 08 May 2025 17:07:53 GMT  
		Size: 1.8 KB (1782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f36787a5ee1c46394cceb50e0a896ee120448916cbad47fc0217040703e6e7a`  
		Last Modified: Thu, 08 May 2025 17:08:01 GMT  
		Size: 70.0 MB (69995550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3536c1dd589a2ac2c4c00c4cd04745d4d4e332fdae5ec2ff5d532014e0c07f6`  
		Last Modified: Thu, 08 May 2025 17:07:53 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.34.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:9cef8234a18e2bced21cf4ae272a9d369c7877266b3cc91a30dc0730b781eb41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6461841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07fb57fe16b24773c7424ca1c0442e97df1436abfe3618ac00589a1de84457fc`

```dockerfile
```

-	Layers:
	-	`sha256:353f0e0d864a7a3999c226d18d1ab5b5cb6807ec88724876ccba00c3d8dcf486`  
		Last Modified: Tue, 06 May 2025 02:06:29 GMT  
		Size: 6.4 MB (6446947 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1220a2a4a2dc3d9f0273f3ef0a58d42b992b9f7be92783d32b58495669cafb3`  
		Last Modified: Tue, 06 May 2025 02:06:28 GMT  
		Size: 14.9 KB (14894 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.34.3-alpine`

```console
$ docker pull telegraf@sha256:2e19df3142f74083fa1ec0ee98901a277971e144fae9a49bca21aeecddadb6be
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.34.3-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:645c9bfb6439247ce432fa016aa288a7c063b546dcccc1a1efbd2047ade7a000
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.1 MB (83066472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fd00bc80283e5dee38fcda1db589eb3f70d4ad664d029b857f5a315a414d7bb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Mon, 05 May 2025 20:28:05 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 05 May 2025 20:28:05 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 05 May 2025 20:28:05 GMT
ENV TELEGRAF_VERSION=1.34.3
# Mon, 05 May 2025 20:28:05 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 05 May 2025 20:28:05 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 05 May 2025 20:28:05 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 05 May 2025 20:28:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 05 May 2025 20:28:05 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 14:35:06 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e036f026e2ca6ce0fb410d4555de5d0b0d3e8228adc8d209c04e482abbd86453`  
		Last Modified: Thu, 08 May 2025 17:05:41 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb0861b20c0225a79f2e78e27dc922e52c78082d6a774646a4d2d8f7548508a7`  
		Last Modified: Thu, 08 May 2025 17:05:41 GMT  
		Size: 2.4 MB (2449575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55d80681ba2be41917f5f0ee9aa4583465fe80682feff10dce7ac9d8787ca085`  
		Last Modified: Thu, 08 May 2025 17:05:48 GMT  
		Size: 77.0 MB (76989395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6f559c698c5228b31a27032040a2e50b37d397a2bc72fe8c569fe8ae8b4d28c`  
		Last Modified: Thu, 08 May 2025 17:05:43 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.34.3-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:b776a430c712f166e58d64205f9395ff4831bd55f8bf69786e3f0ed8ac68bc43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1116095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:000dd7750d7df88059611520d73ca93811803be83a179ce099a8a6c0ad12539a`

```dockerfile
```

-	Layers:
	-	`sha256:f7220dd330064a19390f85ae82c72a2dacdb31e562fc20818899cc094e0bd61d`  
		Last Modified: Thu, 08 May 2025 17:18:24 GMT  
		Size: 1.1 MB (1100832 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0433ef5061b69291b9e8aafea4752870b788cb583117e263f986c7c56363ceae`  
		Last Modified: Thu, 08 May 2025 17:18:23 GMT  
		Size: 15.3 KB (15263 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.34.3-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:68cd1d14ab575884f986f51fce537a3bddf30ce7549ba3988937cd2f1b0949bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.4 MB (76418004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24e6f62920d3e2d73423452627351881ed3c5a054c44883ea45eec858dc5575a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Mon, 05 May 2025 20:28:05 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 05 May 2025 20:28:05 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 05 May 2025 20:28:05 GMT
ENV TELEGRAF_VERSION=1.34.3
# Mon, 05 May 2025 20:28:05 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 05 May 2025 20:28:05 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 05 May 2025 20:28:05 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 05 May 2025 20:28:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 05 May 2025 20:28:05 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:94e9d8af22013aabf0edcaf42950c88b0a1350c3a9ce076d61b98a535a673dd9`  
		Last Modified: Fri, 14 Feb 2025 14:35:45 GMT  
		Size: 4.1 MB (4091165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:434c8ed1b411bf87e31d51dcd5e11ad29b842c6ac23d29867f58c9b6657217f9`  
		Last Modified: Thu, 08 May 2025 17:16:04 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d509229eaab440944eafb92883af0415ca875e0db2665add61e48bfe43f6b4dd`  
		Last Modified: Thu, 08 May 2025 17:16:06 GMT  
		Size: 2.5 MB (2535687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23c7c4b61f32dbb4ada9f4d0a285db0eecb9e3184c28b45c375020c4b7cb3a59`  
		Last Modified: Thu, 08 May 2025 17:16:14 GMT  
		Size: 69.8 MB (69790548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b4c2e91ab15daceb80fd337395a9c5ab3793298495749ff949b046e665a1938`  
		Last Modified: Thu, 08 May 2025 17:16:05 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.34.3-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:3676f10d7f2e1cffd8a87077aa981add2eda7f67129c7500bfa8616e73bd5ca8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1111856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f9ce31efac00e0ee13c4a6b2494564a069c7e7262edfc5d4507253ae576b4ea`

```dockerfile
```

-	Layers:
	-	`sha256:99177517ca325a8d873c732ad1ce28e40f9dcf9a28bb766712177cbcf9f16775`  
		Last Modified: Thu, 08 May 2025 17:18:25 GMT  
		Size: 1.1 MB (1096471 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf602a6b5044f56bc88a87ee5516d257fc98641926b1d1ea0f918d509c2fa83b`  
		Last Modified: Thu, 08 May 2025 17:18:23 GMT  
		Size: 15.4 KB (15385 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:alpine`

```console
$ docker pull telegraf@sha256:2e19df3142f74083fa1ec0ee98901a277971e144fae9a49bca21aeecddadb6be
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:645c9bfb6439247ce432fa016aa288a7c063b546dcccc1a1efbd2047ade7a000
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.1 MB (83066472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fd00bc80283e5dee38fcda1db589eb3f70d4ad664d029b857f5a315a414d7bb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Mon, 05 May 2025 20:28:05 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 05 May 2025 20:28:05 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 05 May 2025 20:28:05 GMT
ENV TELEGRAF_VERSION=1.34.3
# Mon, 05 May 2025 20:28:05 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 05 May 2025 20:28:05 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 05 May 2025 20:28:05 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 05 May 2025 20:28:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 05 May 2025 20:28:05 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 14:35:06 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e036f026e2ca6ce0fb410d4555de5d0b0d3e8228adc8d209c04e482abbd86453`  
		Last Modified: Thu, 08 May 2025 17:05:41 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb0861b20c0225a79f2e78e27dc922e52c78082d6a774646a4d2d8f7548508a7`  
		Last Modified: Thu, 08 May 2025 17:05:41 GMT  
		Size: 2.4 MB (2449575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55d80681ba2be41917f5f0ee9aa4583465fe80682feff10dce7ac9d8787ca085`  
		Last Modified: Thu, 08 May 2025 17:05:48 GMT  
		Size: 77.0 MB (76989395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6f559c698c5228b31a27032040a2e50b37d397a2bc72fe8c569fe8ae8b4d28c`  
		Last Modified: Thu, 08 May 2025 17:05:43 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:b776a430c712f166e58d64205f9395ff4831bd55f8bf69786e3f0ed8ac68bc43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1116095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:000dd7750d7df88059611520d73ca93811803be83a179ce099a8a6c0ad12539a`

```dockerfile
```

-	Layers:
	-	`sha256:f7220dd330064a19390f85ae82c72a2dacdb31e562fc20818899cc094e0bd61d`  
		Last Modified: Thu, 08 May 2025 17:18:24 GMT  
		Size: 1.1 MB (1100832 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0433ef5061b69291b9e8aafea4752870b788cb583117e263f986c7c56363ceae`  
		Last Modified: Thu, 08 May 2025 17:18:23 GMT  
		Size: 15.3 KB (15263 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:68cd1d14ab575884f986f51fce537a3bddf30ce7549ba3988937cd2f1b0949bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.4 MB (76418004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24e6f62920d3e2d73423452627351881ed3c5a054c44883ea45eec858dc5575a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Mon, 05 May 2025 20:28:05 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 05 May 2025 20:28:05 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 05 May 2025 20:28:05 GMT
ENV TELEGRAF_VERSION=1.34.3
# Mon, 05 May 2025 20:28:05 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 05 May 2025 20:28:05 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 05 May 2025 20:28:05 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 05 May 2025 20:28:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 05 May 2025 20:28:05 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:94e9d8af22013aabf0edcaf42950c88b0a1350c3a9ce076d61b98a535a673dd9`  
		Last Modified: Fri, 14 Feb 2025 14:35:45 GMT  
		Size: 4.1 MB (4091165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:434c8ed1b411bf87e31d51dcd5e11ad29b842c6ac23d29867f58c9b6657217f9`  
		Last Modified: Thu, 08 May 2025 17:16:04 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d509229eaab440944eafb92883af0415ca875e0db2665add61e48bfe43f6b4dd`  
		Last Modified: Thu, 08 May 2025 17:16:06 GMT  
		Size: 2.5 MB (2535687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23c7c4b61f32dbb4ada9f4d0a285db0eecb9e3184c28b45c375020c4b7cb3a59`  
		Last Modified: Thu, 08 May 2025 17:16:14 GMT  
		Size: 69.8 MB (69790548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b4c2e91ab15daceb80fd337395a9c5ab3793298495749ff949b046e665a1938`  
		Last Modified: Thu, 08 May 2025 17:16:05 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:3676f10d7f2e1cffd8a87077aa981add2eda7f67129c7500bfa8616e73bd5ca8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1111856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f9ce31efac00e0ee13c4a6b2494564a069c7e7262edfc5d4507253ae576b4ea`

```dockerfile
```

-	Layers:
	-	`sha256:99177517ca325a8d873c732ad1ce28e40f9dcf9a28bb766712177cbcf9f16775`  
		Last Modified: Thu, 08 May 2025 17:18:25 GMT  
		Size: 1.1 MB (1096471 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf602a6b5044f56bc88a87ee5516d257fc98641926b1d1ea0f918d509c2fa83b`  
		Last Modified: Thu, 08 May 2025 17:18:23 GMT  
		Size: 15.4 KB (15385 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:latest`

```console
$ docker pull telegraf@sha256:80c2d6e3e421382ace42eb38c125b9b482dc20996693f4ab1967b2e8e76590d2
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
$ docker pull telegraf@sha256:49b40dd64751da9cfd0d9b030e128c216d6c393412a129991b4c1f7f3fd85f18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.6 MB (168648209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:519e6e29ffe0a7e938ab4f90499d0c11d5c0b4f42bdaf123e25d804909e91365`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 05 May 2025 20:28:05 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 05 May 2025 20:28:05 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 05 May 2025 20:28:05 GMT
ENV TELEGRAF_VERSION=1.34.3
# Mon, 05 May 2025 20:28:05 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 05 May 2025 20:28:05 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 05 May 2025 20:28:05 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 05 May 2025 20:28:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 05 May 2025 20:28:05 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:cf05a52c02353f0b2b6f9be0549ac916c3fb1dc8d4bacd405eac7f28562ec9f2`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 48.5 MB (48491199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63964a8518f54dc31f8df89d7f06714c7a793aa1aa08a64ae3d7f4f4f30b4ac8`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 24.0 MB (24011181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dacc14b4e0bdc5194a2c8473cb1b6c87502ade9e518dd4fc860d6e2b92fabc2`  
		Last Modified: Thu, 08 May 2025 17:05:09 GMT  
		Size: 18.9 MB (18946555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60feec1ed28bf204a6705b299fb6150e3fdc5b79525f640a479f05fee0ecdb59`  
		Last Modified: Thu, 08 May 2025 17:05:28 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acbdec894ca78c4fe47dd8ac0c9f441acfa4578ed79e781c0279e94ff19c9119`  
		Last Modified: Thu, 08 May 2025 17:05:14 GMT  
		Size: 77.2 MB (77196866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01b51d74a199fd95947ea33f9ec3514fffab3a8ef9246bded84a400656d77c13`  
		Last Modified: Thu, 08 May 2025 17:04:49 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:e53a298f46a8e7d1885bd3a2dc4d41d6b1c6c364de7dc6bcc3d402aece988750
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6461031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7b59d75249146d4adb68eeb664ac0c1b8e17da560f7cc77c91bc4a415a40c96`

```dockerfile
```

-	Layers:
	-	`sha256:6addf961b16060916a345fcbd3b60d5df5d9ed1bf254dc43270a16f915aadded`  
		Last Modified: Mon, 05 May 2025 21:43:54 GMT  
		Size: 6.4 MB (6446259 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d627eade19e5b07c1115be617fce2ade5b596bfc798f27899b1661106aa11d28`  
		Last Modified: Mon, 05 May 2025 21:43:54 GMT  
		Size: 14.8 KB (14772 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:acacb2a9994c771837719bde79a0b3cf3bd213810fcaa937e2e7e41f76911ab0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.2 MB (155159090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:396350dfa8d3a9e70655ebd921574d6889182c536c05c1a62e5b641257271105`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 05 May 2025 20:28:05 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 05 May 2025 20:28:05 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 05 May 2025 20:28:05 GMT
ENV TELEGRAF_VERSION=1.34.3
# Mon, 05 May 2025 20:28:05 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 05 May 2025 20:28:05 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 05 May 2025 20:28:05 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 05 May 2025 20:28:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 05 May 2025 20:28:05 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:a735d4b4a53e8e11448d15bc50ce4670d54dff52e426cf0510c9b713d3a7ad09`  
		Last Modified: Thu, 08 May 2025 17:04:48 GMT  
		Size: 44.2 MB (44197079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b01e6436acd06b177253a4ba25e5179715088c2f493e89c91bbf6fdc41a2034`  
		Last Modified: Thu, 08 May 2025 17:05:35 GMT  
		Size: 21.9 MB (21918380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eabe566c6af2691f3105823447ac937c1f11b004965e6abc01575a064a841148`  
		Last Modified: Thu, 08 May 2025 19:54:16 GMT  
		Size: 17.7 MB (17724705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2d5c5bcea6d97d32d23b37764468583109ef0810d01e6d83a881b0023fe34ef`  
		Last Modified: Thu, 08 May 2025 19:54:19 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04ee6f04b91006925ceab7576921c368aa0075806393b4fdd1c8b77f9ff99287`  
		Last Modified: Mon, 05 May 2025 21:43:55 GMT  
		Size: 71.3 MB (71316530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bbffd0f20d8462cede56db1171d487ce44cc115861b1bca0b1ae366dc13aae2`  
		Last Modified: Thu, 08 May 2025 19:54:21 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:43aef8fa73b7066f2c6c1fb05ca46bd0e50db98f3c72b05ddd927037cd4482b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6455728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6545d34a2fcec0c4881d7fa165c598c9ca3714d3d120fdf1e468f4b6173cb87c`

```dockerfile
```

-	Layers:
	-	`sha256:dcb63a79fb52b2c69a956ef3e1703d26d3b33188a387457170ad1b189bb81726`  
		Last Modified: Mon, 05 May 2025 21:43:53 GMT  
		Size: 6.4 MB (6440862 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76b89b32d4be35cd37dabeca683f8fd271c5f757168e9a1cd18eb5739a8a8e16`  
		Last Modified: Mon, 05 May 2025 21:43:53 GMT  
		Size: 14.9 KB (14866 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:7236866cd0c185414043e05d17134a659c925307be4df7b08c0c1be8b964b02f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.7 MB (160741620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:543f8780e6330b59dfb5ffb9c60d1a98c5c1132b8e861bfe92539aaca3f620ac`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 05 May 2025 20:28:05 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 05 May 2025 20:28:05 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 05 May 2025 20:28:05 GMT
ENV TELEGRAF_VERSION=1.34.3
# Mon, 05 May 2025 20:28:05 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 05 May 2025 20:28:05 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 05 May 2025 20:28:05 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 05 May 2025 20:28:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 05 May 2025 20:28:05 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:de07ba6f486e0ce29760ab32d4381edabbc660a04c493e95eb9a8056925d8955`  
		Last Modified: Thu, 08 May 2025 17:04:44 GMT  
		Size: 48.3 MB (48327644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84649bff67ea459549b6f371f7045d9968d6ebf370b815c922a625f3ab065724`  
		Last Modified: Thu, 08 May 2025 17:04:42 GMT  
		Size: 23.5 MB (23544262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7446c58993d11b00fcf70a65c363df298c8fd24914c3657943f2362852a75e88`  
		Last Modified: Thu, 08 May 2025 17:07:55 GMT  
		Size: 18.9 MB (18871759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38670875debfb321519f19305350d13646a48ebaac8d2b798ab7aa84cefe61b0`  
		Last Modified: Thu, 08 May 2025 17:07:53 GMT  
		Size: 1.8 KB (1782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f36787a5ee1c46394cceb50e0a896ee120448916cbad47fc0217040703e6e7a`  
		Last Modified: Thu, 08 May 2025 17:08:01 GMT  
		Size: 70.0 MB (69995550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3536c1dd589a2ac2c4c00c4cd04745d4d4e332fdae5ec2ff5d532014e0c07f6`  
		Last Modified: Thu, 08 May 2025 17:07:53 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:9cef8234a18e2bced21cf4ae272a9d369c7877266b3cc91a30dc0730b781eb41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6461841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07fb57fe16b24773c7424ca1c0442e97df1436abfe3618ac00589a1de84457fc`

```dockerfile
```

-	Layers:
	-	`sha256:353f0e0d864a7a3999c226d18d1ab5b5cb6807ec88724876ccba00c3d8dcf486`  
		Last Modified: Tue, 06 May 2025 02:06:29 GMT  
		Size: 6.4 MB (6446947 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1220a2a4a2dc3d9f0273f3ef0a58d42b992b9f7be92783d32b58495669cafb3`  
		Last Modified: Tue, 06 May 2025 02:06:28 GMT  
		Size: 14.9 KB (14894 bytes)  
		MIME: application/vnd.in-toto+json
