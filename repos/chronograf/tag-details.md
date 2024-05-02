<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `chronograf`

-	[`chronograf:1.10`](#chronograf110)
-	[`chronograf:1.10-alpine`](#chronograf110-alpine)
-	[`chronograf:1.10.4`](#chronograf1104)
-	[`chronograf:1.10.4-alpine`](#chronograf1104-alpine)
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
$ docker pull chronograf@sha256:f8576295bb2633b50b8f2b3c8cc683708e74282cf1a768da80f45b1124de5ee8
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
$ docker pull chronograf@sha256:2cb0b8b1da8690af36b9f7b4959bae0f25ba0a187424cac651b20650603445f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.1 MB (84060126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:277f0977dde354462ebac171186c995a845df807d021a0ac3ccdc47f42617d31`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:09 GMT
ADD file:4b1be1de1a1e5aa608c688cad2824587262081866180d7368feb79d33ca05953 in / 
# Wed, 24 Apr 2024 03:28:09 GMT
CMD ["bash"]
# Fri, 26 Apr 2024 13:23:50 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
ENV CHRONOGRAF_VERSION=1.10.4
# Fri, 26 Apr 2024 13:23:50 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 26 Apr 2024 13:23:50 GMT
VOLUME [/var/lib/chronograf]
# Fri, 26 Apr 2024 13:23:50 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Apr 2024 13:23:50 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:b0a0cf830b12453b7e15359a804215a7bcccd3788e2bcecff2a03af64bbd4df7`  
		Last Modified: Wed, 24 Apr 2024 03:32:41 GMT  
		Size: 29.2 MB (29150479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9bca853186d9fa4f3d07e24de79741fa25427f0b2d0eab8996be63473fd1c48`  
		Last Modified: Wed, 01 May 2024 21:52:27 GMT  
		Size: 7.7 MB (7676917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73cc39eb1df3ab70aa7dacba37e772033cd108cd90bdaa74e45011d6198634e2`  
		Last Modified: Wed, 01 May 2024 21:52:27 GMT  
		Size: 47.2 MB (47208254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2157983f1cb0f03e7a121bed8ff6e98027c8c6a3be7d161e4fe2b062522ec970`  
		Last Modified: Wed, 01 May 2024 21:52:26 GMT  
		Size: 12.3 KB (12251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f63d3959c98d650bf99c6413a0b9e85714a8cbcc9e7e258b319a70c5dbc23c3`  
		Last Modified: Wed, 01 May 2024 21:52:27 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4a815190e4fba0bf1463fe2293f2924dfdb71cff35211a1797c45aa66f62fb2`  
		Last Modified: Wed, 01 May 2024 21:52:27 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:1478d940f96dbaafe093d86241a298969ab344d11b536c0664e66d4e82608497
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2671561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f85b25a662f4291186189dd5d3dc33534aa1725e52dcc65c37f9b2766cd1d97`

```dockerfile
```

-	Layers:
	-	`sha256:f54b34b309e82a1681005dc1777c2b0f8604c1d314cb797cfbd1505b30897ba4`  
		Last Modified: Wed, 01 May 2024 21:52:26 GMT  
		Size: 2.7 MB (2655509 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2f8299d252d4df87db8af04601374b4348d6985c3594eb49c1877cdc524b51a`  
		Last Modified: Wed, 01 May 2024 21:52:26 GMT  
		Size: 16.1 KB (16052 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.10` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:e7b87511934d274d44fdf7a810d210f8b2bebfedbca8c0de6128a5bda5f26532
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.3 MB (75340418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44445870df96cde21c7fd5b24ea74b673c0850e9e01577c1b168553f9cef8453`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 24 Apr 2024 04:07:05 GMT
ADD file:719e14b0eb733543ace336c71543b593f88e2b452e40fb315f5f6e49ebe6af58 in / 
# Wed, 24 Apr 2024 04:07:06 GMT
CMD ["bash"]
# Fri, 26 Apr 2024 13:23:50 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
ENV CHRONOGRAF_VERSION=1.10.4
# Fri, 26 Apr 2024 13:23:50 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 26 Apr 2024 13:23:50 GMT
VOLUME [/var/lib/chronograf]
# Fri, 26 Apr 2024 13:23:50 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Apr 2024 13:23:50 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:77e415c4e7c678efbc2cc774d4bc05f6f2de2a2e04959d7e324ce092026c650e`  
		Last Modified: Wed, 24 Apr 2024 04:11:13 GMT  
		Size: 24.7 MB (24740442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50316fbdc37f48b441d6a5300c3b2f5011fe5ff93920de46d8e37f26b19c1d0c`  
		Last Modified: Wed, 01 May 2024 22:09:40 GMT  
		Size: 6.3 MB (6301004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26e807757725f3d1ccaff9e57a0166983a73816ed082c8ef4173e057c9c61e87`  
		Last Modified: Wed, 01 May 2024 22:09:41 GMT  
		Size: 44.3 MB (44274487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42dfb47a244cadf0ec10ec3b5b8d475fb580dac07af32b9a27dbcde94f0c3cd4`  
		Last Modified: Wed, 01 May 2024 22:09:40 GMT  
		Size: 12.3 KB (12255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dff168616ff7f4d51eeab0e490b470d7be9bc49f74a5c75dd0769f58e6dd700d`  
		Last Modified: Wed, 01 May 2024 22:09:40 GMT  
		Size: 11.9 KB (11915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4e9b69be2b29851b3a218eeb456c72de15f9662b211438a21f396067cd6a4a9`  
		Last Modified: Wed, 01 May 2024 22:09:41 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:25dc80c7fe7448e89953320590af015f568304748c3b4855343d6e9792d63195
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2673765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc039a1ec77e176937bbd6406e7d5c07bd658a7893298e2a025947d0d09faef0`

```dockerfile
```

-	Layers:
	-	`sha256:b513cb3404b83faf32634e4946d2c0c5160a5001c8695d86ccfbb890a34cba61`  
		Last Modified: Wed, 01 May 2024 22:09:40 GMT  
		Size: 2.7 MB (2657805 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b6e8b8f908a14cafee41c6387f290c5241c3caf12fa4e5a54d1a9694dcf7efb`  
		Last Modified: Wed, 01 May 2024 22:09:40 GMT  
		Size: 16.0 KB (15960 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.10` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:60a815700707f1df08df1029b83847eaa235f0e912a34fa6c253f12499024cf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.6 MB (81636840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5eaf05222cf53da43f8ef2282da0792a02048e92364dbcd68d586504103b4409`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:39 GMT
ADD file:ea7004fb788ab5cf1604d6e71153c48d99b75fbd1810e78a8c79faff11fe6771 in / 
# Wed, 24 Apr 2024 04:10:39 GMT
CMD ["bash"]
# Fri, 26 Apr 2024 13:23:50 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
ENV CHRONOGRAF_VERSION=1.10.4
# Fri, 26 Apr 2024 13:23:50 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 26 Apr 2024 13:23:50 GMT
VOLUME [/var/lib/chronograf]
# Fri, 26 Apr 2024 13:23:50 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Apr 2024 13:23:50 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:22d97f6a5d13532e867231d23d92620a81874d51a456196be50154eeb32edc08`  
		Last Modified: Wed, 24 Apr 2024 04:14:07 GMT  
		Size: 29.2 MB (29179935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afb2e161aae97649675931a79d1973b601f753dd3f37c4532530c72c07636d3d`  
		Last Modified: Wed, 01 May 2024 22:27:06 GMT  
		Size: 7.5 MB (7453129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1130d13b51f5f0ed17ab174e642adb1112bb78775d279ad3c199e0b61bd90b9b`  
		Last Modified: Wed, 01 May 2024 22:27:06 GMT  
		Size: 45.0 MB (44979293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac52f1d1a62121ca7fcfe7cc928aade001f7b7874c8bd7b40e7256c5e3ea6e1a`  
		Last Modified: Wed, 01 May 2024 22:27:04 GMT  
		Size: 12.3 KB (12254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:957a06817cfb183d334232ce4a1711d8735a39d983d25146bf657bf1f530254a`  
		Last Modified: Wed, 01 May 2024 22:27:05 GMT  
		Size: 11.9 KB (11914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b9bf80ee0ddb49a63ed6b1ca461f772f3c550d4d7c5615143ca62e3e21887ad`  
		Last Modified: Wed, 01 May 2024 22:27:05 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:f0e5abe681ea42d2efc7c7b8030e027274a57edf6ad0df5d93534ce2946ebdd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2671639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f479d33da2a64ac7a34333ed6adc29193bb65bee2a716d94a348e2858f84a85`

```dockerfile
```

-	Layers:
	-	`sha256:7c4fdc79c78dae83df78d9db456f5b419479096350f7ddb60685cc893a76a462`  
		Last Modified: Wed, 01 May 2024 22:27:04 GMT  
		Size: 2.7 MB (2655746 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:032a014ac7dc76467dddff4fd025e78a13e66d45993577bb48911db0c688e710`  
		Last Modified: Wed, 01 May 2024 22:27:04 GMT  
		Size: 15.9 KB (15893 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.10-alpine`

```console
$ docker pull chronograf@sha256:d11a629d4cfa1e0b9ca605f0719d5a9dc17add74c6fa2ed5f1901d2cb5c88be8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.10-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:bfdc2916cdf18901c104cbb5f9c37af0dcc9670c7da181038e306ff77d6cd169
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.6 MB (31589712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac8161dc609b83d7c07ff98e4828ced9b2e7f2ca0ff7144adade754fc64e7b28`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Fri, 26 Apr 2024 13:23:50 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
RUN apk add --no-cache ca-certificates su-exec &&     update-ca-certificates # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
ENV CHRONOGRAF_VERSION=1.10.4
# Fri, 26 Apr 2024 13:23:50 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S chronograf &&     adduser -S chronograf -G chronograf &&     mkdir -m 0750 -p /var/lib/chronograf &&     chown chronograf:chronograf /var/lib/chronograf # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 26 Apr 2024 13:23:50 GMT
VOLUME [/var/lib/chronograf]
# Fri, 26 Apr 2024 13:23:50 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Apr 2024 13:23:50 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d68e27f81705183aede5ec8d16b05af8c07d462f75e94160d798299e372f7a69`  
		Last Modified: Wed, 01 May 2024 21:52:22 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:310f07ece82e275ea4dc66a9a9033fdcdaf998fe6c7997781d299f934b8c039f`  
		Last Modified: Wed, 01 May 2024 21:52:22 GMT  
		Size: 295.8 KB (295755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df60bc3d01a0c01b095244792c5eb913e78e49a27aed12d0298bfeb99e8a5ae0`  
		Last Modified: Wed, 01 May 2024 21:52:23 GMT  
		Size: 27.9 MB (27866708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:809a3d10431465aa989b32320fcfa614917e4dd78b0ef3b4ba628af38b03e71c`  
		Last Modified: Wed, 01 May 2024 21:52:22 GMT  
		Size: 12.2 KB (12238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f26c5e66ed649fcbf21fdb6804855736c49214b33b70c57c236a56a02a0571a`  
		Last Modified: Wed, 01 May 2024 21:52:23 GMT  
		Size: 11.9 KB (11897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7cb52b403bfe177c53c218fda5245ba026945a8f393b97742e454946cf636a0`  
		Last Modified: Wed, 01 May 2024 21:52:23 GMT  
		Size: 292.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:d9169b4cb482ee5951ad4ecd2517a3d1409300a9dbb434cf060738a8755d0638
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.9 KB (248883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1186269e1898e56e2c477e1d1b6f8cdc68fa2be6a7ec7f5d9d857d8ac776419e`

```dockerfile
```

-	Layers:
	-	`sha256:f971f5ac4f8155c9092387ba6239303ff77b238f4abcfaaf23311628c0c78175`  
		Last Modified: Wed, 01 May 2024 21:52:22 GMT  
		Size: 231.1 KB (231128 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9504ad10dc79d5f0656c0ac6e2b5636b26abca0889311e5b247b31f93728d9cc`  
		Last Modified: Wed, 01 May 2024 21:52:22 GMT  
		Size: 17.8 KB (17755 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.10.4`

```console
$ docker pull chronograf@sha256:f8576295bb2633b50b8f2b3c8cc683708e74282cf1a768da80f45b1124de5ee8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `chronograf:1.10.4` - linux; amd64

```console
$ docker pull chronograf@sha256:2cb0b8b1da8690af36b9f7b4959bae0f25ba0a187424cac651b20650603445f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.1 MB (84060126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:277f0977dde354462ebac171186c995a845df807d021a0ac3ccdc47f42617d31`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:09 GMT
ADD file:4b1be1de1a1e5aa608c688cad2824587262081866180d7368feb79d33ca05953 in / 
# Wed, 24 Apr 2024 03:28:09 GMT
CMD ["bash"]
# Fri, 26 Apr 2024 13:23:50 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
ENV CHRONOGRAF_VERSION=1.10.4
# Fri, 26 Apr 2024 13:23:50 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 26 Apr 2024 13:23:50 GMT
VOLUME [/var/lib/chronograf]
# Fri, 26 Apr 2024 13:23:50 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Apr 2024 13:23:50 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:b0a0cf830b12453b7e15359a804215a7bcccd3788e2bcecff2a03af64bbd4df7`  
		Last Modified: Wed, 24 Apr 2024 03:32:41 GMT  
		Size: 29.2 MB (29150479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9bca853186d9fa4f3d07e24de79741fa25427f0b2d0eab8996be63473fd1c48`  
		Last Modified: Wed, 01 May 2024 21:52:27 GMT  
		Size: 7.7 MB (7676917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73cc39eb1df3ab70aa7dacba37e772033cd108cd90bdaa74e45011d6198634e2`  
		Last Modified: Wed, 01 May 2024 21:52:27 GMT  
		Size: 47.2 MB (47208254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2157983f1cb0f03e7a121bed8ff6e98027c8c6a3be7d161e4fe2b062522ec970`  
		Last Modified: Wed, 01 May 2024 21:52:26 GMT  
		Size: 12.3 KB (12251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f63d3959c98d650bf99c6413a0b9e85714a8cbcc9e7e258b319a70c5dbc23c3`  
		Last Modified: Wed, 01 May 2024 21:52:27 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4a815190e4fba0bf1463fe2293f2924dfdb71cff35211a1797c45aa66f62fb2`  
		Last Modified: Wed, 01 May 2024 21:52:27 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10.4` - unknown; unknown

```console
$ docker pull chronograf@sha256:1478d940f96dbaafe093d86241a298969ab344d11b536c0664e66d4e82608497
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2671561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f85b25a662f4291186189dd5d3dc33534aa1725e52dcc65c37f9b2766cd1d97`

```dockerfile
```

-	Layers:
	-	`sha256:f54b34b309e82a1681005dc1777c2b0f8604c1d314cb797cfbd1505b30897ba4`  
		Last Modified: Wed, 01 May 2024 21:52:26 GMT  
		Size: 2.7 MB (2655509 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2f8299d252d4df87db8af04601374b4348d6985c3594eb49c1877cdc524b51a`  
		Last Modified: Wed, 01 May 2024 21:52:26 GMT  
		Size: 16.1 KB (16052 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.10.4` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:e7b87511934d274d44fdf7a810d210f8b2bebfedbca8c0de6128a5bda5f26532
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.3 MB (75340418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44445870df96cde21c7fd5b24ea74b673c0850e9e01577c1b168553f9cef8453`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 24 Apr 2024 04:07:05 GMT
ADD file:719e14b0eb733543ace336c71543b593f88e2b452e40fb315f5f6e49ebe6af58 in / 
# Wed, 24 Apr 2024 04:07:06 GMT
CMD ["bash"]
# Fri, 26 Apr 2024 13:23:50 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
ENV CHRONOGRAF_VERSION=1.10.4
# Fri, 26 Apr 2024 13:23:50 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 26 Apr 2024 13:23:50 GMT
VOLUME [/var/lib/chronograf]
# Fri, 26 Apr 2024 13:23:50 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Apr 2024 13:23:50 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:77e415c4e7c678efbc2cc774d4bc05f6f2de2a2e04959d7e324ce092026c650e`  
		Last Modified: Wed, 24 Apr 2024 04:11:13 GMT  
		Size: 24.7 MB (24740442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50316fbdc37f48b441d6a5300c3b2f5011fe5ff93920de46d8e37f26b19c1d0c`  
		Last Modified: Wed, 01 May 2024 22:09:40 GMT  
		Size: 6.3 MB (6301004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26e807757725f3d1ccaff9e57a0166983a73816ed082c8ef4173e057c9c61e87`  
		Last Modified: Wed, 01 May 2024 22:09:41 GMT  
		Size: 44.3 MB (44274487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42dfb47a244cadf0ec10ec3b5b8d475fb580dac07af32b9a27dbcde94f0c3cd4`  
		Last Modified: Wed, 01 May 2024 22:09:40 GMT  
		Size: 12.3 KB (12255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dff168616ff7f4d51eeab0e490b470d7be9bc49f74a5c75dd0769f58e6dd700d`  
		Last Modified: Wed, 01 May 2024 22:09:40 GMT  
		Size: 11.9 KB (11915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4e9b69be2b29851b3a218eeb456c72de15f9662b211438a21f396067cd6a4a9`  
		Last Modified: Wed, 01 May 2024 22:09:41 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10.4` - unknown; unknown

```console
$ docker pull chronograf@sha256:25dc80c7fe7448e89953320590af015f568304748c3b4855343d6e9792d63195
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2673765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc039a1ec77e176937bbd6406e7d5c07bd658a7893298e2a025947d0d09faef0`

```dockerfile
```

-	Layers:
	-	`sha256:b513cb3404b83faf32634e4946d2c0c5160a5001c8695d86ccfbb890a34cba61`  
		Last Modified: Wed, 01 May 2024 22:09:40 GMT  
		Size: 2.7 MB (2657805 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b6e8b8f908a14cafee41c6387f290c5241c3caf12fa4e5a54d1a9694dcf7efb`  
		Last Modified: Wed, 01 May 2024 22:09:40 GMT  
		Size: 16.0 KB (15960 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.10.4` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:60a815700707f1df08df1029b83847eaa235f0e912a34fa6c253f12499024cf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.6 MB (81636840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5eaf05222cf53da43f8ef2282da0792a02048e92364dbcd68d586504103b4409`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:39 GMT
ADD file:ea7004fb788ab5cf1604d6e71153c48d99b75fbd1810e78a8c79faff11fe6771 in / 
# Wed, 24 Apr 2024 04:10:39 GMT
CMD ["bash"]
# Fri, 26 Apr 2024 13:23:50 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
ENV CHRONOGRAF_VERSION=1.10.4
# Fri, 26 Apr 2024 13:23:50 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 26 Apr 2024 13:23:50 GMT
VOLUME [/var/lib/chronograf]
# Fri, 26 Apr 2024 13:23:50 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Apr 2024 13:23:50 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:22d97f6a5d13532e867231d23d92620a81874d51a456196be50154eeb32edc08`  
		Last Modified: Wed, 24 Apr 2024 04:14:07 GMT  
		Size: 29.2 MB (29179935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afb2e161aae97649675931a79d1973b601f753dd3f37c4532530c72c07636d3d`  
		Last Modified: Wed, 01 May 2024 22:27:06 GMT  
		Size: 7.5 MB (7453129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1130d13b51f5f0ed17ab174e642adb1112bb78775d279ad3c199e0b61bd90b9b`  
		Last Modified: Wed, 01 May 2024 22:27:06 GMT  
		Size: 45.0 MB (44979293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac52f1d1a62121ca7fcfe7cc928aade001f7b7874c8bd7b40e7256c5e3ea6e1a`  
		Last Modified: Wed, 01 May 2024 22:27:04 GMT  
		Size: 12.3 KB (12254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:957a06817cfb183d334232ce4a1711d8735a39d983d25146bf657bf1f530254a`  
		Last Modified: Wed, 01 May 2024 22:27:05 GMT  
		Size: 11.9 KB (11914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b9bf80ee0ddb49a63ed6b1ca461f772f3c550d4d7c5615143ca62e3e21887ad`  
		Last Modified: Wed, 01 May 2024 22:27:05 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10.4` - unknown; unknown

```console
$ docker pull chronograf@sha256:f0e5abe681ea42d2efc7c7b8030e027274a57edf6ad0df5d93534ce2946ebdd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2671639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f479d33da2a64ac7a34333ed6adc29193bb65bee2a716d94a348e2858f84a85`

```dockerfile
```

-	Layers:
	-	`sha256:7c4fdc79c78dae83df78d9db456f5b419479096350f7ddb60685cc893a76a462`  
		Last Modified: Wed, 01 May 2024 22:27:04 GMT  
		Size: 2.7 MB (2655746 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:032a014ac7dc76467dddff4fd025e78a13e66d45993577bb48911db0c688e710`  
		Last Modified: Wed, 01 May 2024 22:27:04 GMT  
		Size: 15.9 KB (15893 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.10.4-alpine`

```console
$ docker pull chronograf@sha256:d11a629d4cfa1e0b9ca605f0719d5a9dc17add74c6fa2ed5f1901d2cb5c88be8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.10.4-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:bfdc2916cdf18901c104cbb5f9c37af0dcc9670c7da181038e306ff77d6cd169
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.6 MB (31589712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac8161dc609b83d7c07ff98e4828ced9b2e7f2ca0ff7144adade754fc64e7b28`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Fri, 26 Apr 2024 13:23:50 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
RUN apk add --no-cache ca-certificates su-exec &&     update-ca-certificates # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
ENV CHRONOGRAF_VERSION=1.10.4
# Fri, 26 Apr 2024 13:23:50 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S chronograf &&     adduser -S chronograf -G chronograf &&     mkdir -m 0750 -p /var/lib/chronograf &&     chown chronograf:chronograf /var/lib/chronograf # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 26 Apr 2024 13:23:50 GMT
VOLUME [/var/lib/chronograf]
# Fri, 26 Apr 2024 13:23:50 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Apr 2024 13:23:50 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d68e27f81705183aede5ec8d16b05af8c07d462f75e94160d798299e372f7a69`  
		Last Modified: Wed, 01 May 2024 21:52:22 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:310f07ece82e275ea4dc66a9a9033fdcdaf998fe6c7997781d299f934b8c039f`  
		Last Modified: Wed, 01 May 2024 21:52:22 GMT  
		Size: 295.8 KB (295755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df60bc3d01a0c01b095244792c5eb913e78e49a27aed12d0298bfeb99e8a5ae0`  
		Last Modified: Wed, 01 May 2024 21:52:23 GMT  
		Size: 27.9 MB (27866708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:809a3d10431465aa989b32320fcfa614917e4dd78b0ef3b4ba628af38b03e71c`  
		Last Modified: Wed, 01 May 2024 21:52:22 GMT  
		Size: 12.2 KB (12238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f26c5e66ed649fcbf21fdb6804855736c49214b33b70c57c236a56a02a0571a`  
		Last Modified: Wed, 01 May 2024 21:52:23 GMT  
		Size: 11.9 KB (11897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7cb52b403bfe177c53c218fda5245ba026945a8f393b97742e454946cf636a0`  
		Last Modified: Wed, 01 May 2024 21:52:23 GMT  
		Size: 292.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10.4-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:d9169b4cb482ee5951ad4ecd2517a3d1409300a9dbb434cf060738a8755d0638
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.9 KB (248883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1186269e1898e56e2c477e1d1b6f8cdc68fa2be6a7ec7f5d9d857d8ac776419e`

```dockerfile
```

-	Layers:
	-	`sha256:f971f5ac4f8155c9092387ba6239303ff77b238f4abcfaaf23311628c0c78175`  
		Last Modified: Wed, 01 May 2024 21:52:22 GMT  
		Size: 231.1 KB (231128 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9504ad10dc79d5f0656c0ac6e2b5636b26abca0889311e5b247b31f93728d9cc`  
		Last Modified: Wed, 01 May 2024 21:52:22 GMT  
		Size: 17.8 KB (17755 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.7`

```console
$ docker pull chronograf@sha256:98c34d939c741f333c88dbd1593623fa8a8603c0091f90b660abda20237ec25c
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
$ docker pull chronograf@sha256:89a96def46065d2dcaacaab163bd1c93f309143671d67cd0a8070e098cedc817
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.2 MB (70202097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:938071c8c78ee600dd82f910aa6e8d65c8cea6d6b0374830dbbec5bea08532bb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:31 GMT
ADD file:0e5a7771d5c0c58072db41fa02f288def8a40f2116b48e6127f1034f848bc2cd in / 
# Wed, 24 Apr 2024 03:28:32 GMT
CMD ["bash"]
# Fri, 26 Apr 2024 13:23:50 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Fri, 26 Apr 2024 13:23:50 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 26 Apr 2024 13:23:50 GMT
VOLUME [/var/lib/chronograf]
# Fri, 26 Apr 2024 13:23:50 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Apr 2024 13:23:50 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:6177a7f9989f56e11ac23856a0c014002800d83111aaa3e41fb2591161a166c2`  
		Last Modified: Wed, 24 Apr 2024 03:33:23 GMT  
		Size: 31.4 MB (31434263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:313f97c5604eed34838cd6e00c6c922e8a64cca26a54768ed9663262caa38d1b`  
		Last Modified: Wed, 01 May 2024 21:52:32 GMT  
		Size: 4.2 MB (4209330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b883403ea76600d868fa4f69c7d65c488a3e41ab462b13e776208f698b91dda`  
		Last Modified: Wed, 01 May 2024 21:52:34 GMT  
		Size: 34.5 MB (34534104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a139a11bc66eddbc2377f085c23513dd149fb872bc93ffb0dc0c480e69955597`  
		Last Modified: Wed, 01 May 2024 21:52:32 GMT  
		Size: 12.3 KB (12251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb726c0b2d364007c5acd665353019f15dbeed595eaa91ba41859b9f871a572f`  
		Last Modified: Wed, 01 May 2024 21:52:32 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a80080663e0e4f10cfc631e3cb8a74731a1bb923a9b85ded841f73a48aa7f96c`  
		Last Modified: Wed, 01 May 2024 21:52:33 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7` - unknown; unknown

```console
$ docker pull chronograf@sha256:ccd749f2e80b03240d23dd7d01cba46d6377a38c91f89c3332295b814ecf4229
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2882945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caa16723e47453655eabd13d7f9fe4b915eaaf8b48544cdf29c420129ee19f7e`

```dockerfile
```

-	Layers:
	-	`sha256:b47fe70389eb5b41635f5edb4372668630957a5e568516b2db4f2744703d70c6`  
		Last Modified: Wed, 01 May 2024 21:52:32 GMT  
		Size: 2.9 MB (2867244 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b18ab52fb4b8a6481aafc8e7862f7d318d3722bd66a3736bbf39bf0b9cd914c2`  
		Last Modified: Wed, 01 May 2024 21:52:32 GMT  
		Size: 15.7 KB (15701 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.7` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:24bc87defac4c83616b004eddc63b57c2f431c7a5b093208da5551112ba26908
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.0 MB (63024462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc59f27a3fd37b6856dd726731f2cdf9ccab8da93af97d69a724c9abcb17e783`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 24 Apr 2024 04:07:25 GMT
ADD file:83a77ac4b262a896dbca1f6974e4401639b3e4d4ca432d88a933c7983e8ccf10 in / 
# Wed, 24 Apr 2024 04:07:25 GMT
CMD ["bash"]
# Fri, 26 Apr 2024 13:23:50 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Fri, 26 Apr 2024 13:23:50 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 26 Apr 2024 13:23:50 GMT
VOLUME [/var/lib/chronograf]
# Fri, 26 Apr 2024 13:23:50 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Apr 2024 13:23:50 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:913a7319952754f0a4a369ee846fb9ecf15cbbead6a1be0f4bdf4a7cbeb1d33c`  
		Last Modified: Wed, 24 Apr 2024 04:11:56 GMT  
		Size: 26.6 MB (26594742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a02d4e2dcc0c18f1edb50078447fc9db19b875a366eefa52d2f7924faa93dc8`  
		Last Modified: Wed, 01 May 2024 22:07:22 GMT  
		Size: 3.5 MB (3511608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c399cb825747bd01b7b446a7c516df7e0736286e5a13254cf67f7327f3cf398`  
		Last Modified: Wed, 01 May 2024 22:07:23 GMT  
		Size: 32.9 MB (32893710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e03e02c499fea8e567f6c934658b1c0419f48cb3b73333cc6a5c43138ecd694b`  
		Last Modified: Wed, 01 May 2024 22:07:22 GMT  
		Size: 12.3 KB (12251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f9cf20464d7eea3168bb9a79cb631569c3c91b624cc469d86d673045beaa9bd`  
		Last Modified: Wed, 01 May 2024 22:07:22 GMT  
		Size: 11.9 KB (11911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a98822bfb3ab70f0c5c12b68241180145dfed495a8fc2710f92afdb2580b2b5b`  
		Last Modified: Wed, 01 May 2024 22:07:23 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7` - unknown; unknown

```console
$ docker pull chronograf@sha256:14c0258a045dd6cbf8ec922a69b575374599923cd09fb9a55d0d912400da6cbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2885115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c319a7f9210a01ab89791d1b8e3608bdb4bbeb9c1199931a4027064167349458`

```dockerfile
```

-	Layers:
	-	`sha256:198e11891e568f2a76a22cb55d06776ae6149b21c9248d3ebe30370ae5fd9ed8`  
		Last Modified: Wed, 01 May 2024 22:07:22 GMT  
		Size: 2.9 MB (2869514 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2980ce3ea639ef05061227f89a728e920aaf5491f6a3d368655e626bbf9ad88`  
		Last Modified: Wed, 01 May 2024 22:07:22 GMT  
		Size: 15.6 KB (15601 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.7` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:feaa26d7c7395560df9df720d143b82f638a6c1f0702cd778cfb4c5f46ed6def
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.4 MB (67356179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:844bbe76861fef142dc0cc704424d2005bf3d8250bb01bf44cf757cd1ea2e509`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:54 GMT
ADD file:e8990741de71fcc1884f30fcd1b6c5ea411bfa752419a82e9748fcd378ca100a in / 
# Wed, 24 Apr 2024 04:10:54 GMT
CMD ["bash"]
# Fri, 26 Apr 2024 13:23:50 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Fri, 26 Apr 2024 13:23:50 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 26 Apr 2024 13:23:50 GMT
VOLUME [/var/lib/chronograf]
# Fri, 26 Apr 2024 13:23:50 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Apr 2024 13:23:50 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:40a322c395ab3df43e27d8be65cc48139c091588ac868643a02567ca247d0c73`  
		Last Modified: Wed, 24 Apr 2024 04:14:48 GMT  
		Size: 30.1 MB (30087336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:241dc733a2765d1ed6b5df2ad5a04edd25d816d790ee85807e647a3703919ea0`  
		Last Modified: Wed, 01 May 2024 22:24:18 GMT  
		Size: 4.2 MB (4210545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:268e94289fff21f738f3871b0fcbfba9b98c5f703ed616181a59df8c19a66a02`  
		Last Modified: Wed, 01 May 2024 22:24:19 GMT  
		Size: 33.0 MB (33033899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:889ea780f967eeaf1a35da1a75e281ffa6cc71e38d06e2895227685a703aea34`  
		Last Modified: Wed, 01 May 2024 22:24:18 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edaf118e59ce4b51ecadbcc627b491fda58e175ad8499ef61709b9e94d8733f4`  
		Last Modified: Wed, 01 May 2024 22:24:18 GMT  
		Size: 11.9 KB (11912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f61b2bc02d9d1365b9369462541909296760a8dcf3b9c65ba494fff9c3a53f41`  
		Last Modified: Wed, 01 May 2024 22:24:19 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7` - unknown; unknown

```console
$ docker pull chronograf@sha256:fa70d9133049bae88f878027769410ece28589e1a2981b61857e08e065204e67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2883006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bc46ab248d0b03f6a2a754a6b204fc431aa76764921b11fdcc76e1bbde3b482`

```dockerfile
```

-	Layers:
	-	`sha256:a8307e0a8364066aafba104ad26d1e97f945019e407934613ed1f9b98763a607`  
		Last Modified: Wed, 01 May 2024 22:24:18 GMT  
		Size: 2.9 MB (2867467 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dfae096072032baf73a1ac486e9c5f6f3d82facbe9028c876ce649470d0dd770`  
		Last Modified: Wed, 01 May 2024 22:24:18 GMT  
		Size: 15.5 KB (15539 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.7-alpine`

```console
$ docker pull chronograf@sha256:928b0a355d0fbeec6b13e9526b9625c464ac595eb3395f795029e9050e697b6a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.7-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:b9c6ca19fbcf0459c66980dfbedf1468bfe1aa2f7e8f23bdc2808c6f5725680b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.3 MB (23255145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:545aecf6038870239dfd16bcd783a9aa43a8e7395d0fd0911c217cb2d1b280a4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:02 GMT
ADD file:c44c9bd36ba35cc78fb9396304ea008def9f42a3beef76aa33b2cf1fde1c10b3 in / 
# Sat, 27 Jan 2024 00:31:02 GMT
CMD ["/bin/sh"]
# Fri, 26 Apr 2024 13:23:50 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Fri, 26 Apr 2024 13:23:50 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 26 Apr 2024 13:23:50 GMT
VOLUME [/var/lib/chronograf]
# Fri, 26 Apr 2024 13:23:50 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Apr 2024 13:23:50 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:3c854c8cbf469fda815b8f6183300c07cfa2fbb5703859ca79aff93ae934961b`  
		Last Modified: Sat, 27 Jan 2024 00:31:44 GMT  
		Size: 3.4 MB (3379404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f856bcbf54737edf390824db1bece56b8c5fc05a6f2357cf56aff5cc454b7815`  
		Last Modified: Wed, 01 May 2024 21:52:13 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f682ae190076e739abc29ac7268f8311bf0f89cd06898bdbf626d365256991f`  
		Last Modified: Wed, 01 May 2024 21:52:13 GMT  
		Size: 293.8 KB (293819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78b77340b0623e50c661f5c33aa9a52eda57aaee21bcae42f4bca10376bca837`  
		Last Modified: Wed, 01 May 2024 21:52:13 GMT  
		Size: 19.6 MB (19557279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9800825cd1091a4a5a9ea6780c03cbb785566d2a46a67c67adddee5d1257631f`  
		Last Modified: Wed, 01 May 2024 21:52:13 GMT  
		Size: 12.2 KB (12231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62a6068243de8a38e51180eb703f4a7074577730f5d5c7396684e2e01c761cfc`  
		Last Modified: Wed, 01 May 2024 21:52:14 GMT  
		Size: 11.9 KB (11894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff9637de3f7407a724769b527d8ce12f0599ebe99c39e30fc48f76897d885a23`  
		Last Modified: Wed, 01 May 2024 21:52:14 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:ef74a07b8e210fe8679e422c5f3baa0c69a6f6a225504e61fca49dbb9c3844a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.0 KB (189001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9666d76fae59dccd086b0c79b67c9d87c71ef8822f7df72f3beb5b3ce74c3d5f`

```dockerfile
```

-	Layers:
	-	`sha256:752685232661d306de8c69d57fb0f651e4724b416adf5d76ce6e05fce95f1f72`  
		Last Modified: Wed, 01 May 2024 21:52:13 GMT  
		Size: 172.2 KB (172188 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1ed049f07a9377f3e36162dfcd54ca83c3ae9304da37fa9f0c479366fe98c29`  
		Last Modified: Wed, 01 May 2024 21:52:13 GMT  
		Size: 16.8 KB (16813 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.7.17`

```console
$ docker pull chronograf@sha256:98c34d939c741f333c88dbd1593623fa8a8603c0091f90b660abda20237ec25c
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
$ docker pull chronograf@sha256:89a96def46065d2dcaacaab163bd1c93f309143671d67cd0a8070e098cedc817
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.2 MB (70202097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:938071c8c78ee600dd82f910aa6e8d65c8cea6d6b0374830dbbec5bea08532bb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:31 GMT
ADD file:0e5a7771d5c0c58072db41fa02f288def8a40f2116b48e6127f1034f848bc2cd in / 
# Wed, 24 Apr 2024 03:28:32 GMT
CMD ["bash"]
# Fri, 26 Apr 2024 13:23:50 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Fri, 26 Apr 2024 13:23:50 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 26 Apr 2024 13:23:50 GMT
VOLUME [/var/lib/chronograf]
# Fri, 26 Apr 2024 13:23:50 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Apr 2024 13:23:50 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:6177a7f9989f56e11ac23856a0c014002800d83111aaa3e41fb2591161a166c2`  
		Last Modified: Wed, 24 Apr 2024 03:33:23 GMT  
		Size: 31.4 MB (31434263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:313f97c5604eed34838cd6e00c6c922e8a64cca26a54768ed9663262caa38d1b`  
		Last Modified: Wed, 01 May 2024 21:52:32 GMT  
		Size: 4.2 MB (4209330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b883403ea76600d868fa4f69c7d65c488a3e41ab462b13e776208f698b91dda`  
		Last Modified: Wed, 01 May 2024 21:52:34 GMT  
		Size: 34.5 MB (34534104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a139a11bc66eddbc2377f085c23513dd149fb872bc93ffb0dc0c480e69955597`  
		Last Modified: Wed, 01 May 2024 21:52:32 GMT  
		Size: 12.3 KB (12251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb726c0b2d364007c5acd665353019f15dbeed595eaa91ba41859b9f871a572f`  
		Last Modified: Wed, 01 May 2024 21:52:32 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a80080663e0e4f10cfc631e3cb8a74731a1bb923a9b85ded841f73a48aa7f96c`  
		Last Modified: Wed, 01 May 2024 21:52:33 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7.17` - unknown; unknown

```console
$ docker pull chronograf@sha256:ccd749f2e80b03240d23dd7d01cba46d6377a38c91f89c3332295b814ecf4229
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2882945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caa16723e47453655eabd13d7f9fe4b915eaaf8b48544cdf29c420129ee19f7e`

```dockerfile
```

-	Layers:
	-	`sha256:b47fe70389eb5b41635f5edb4372668630957a5e568516b2db4f2744703d70c6`  
		Last Modified: Wed, 01 May 2024 21:52:32 GMT  
		Size: 2.9 MB (2867244 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b18ab52fb4b8a6481aafc8e7862f7d318d3722bd66a3736bbf39bf0b9cd914c2`  
		Last Modified: Wed, 01 May 2024 21:52:32 GMT  
		Size: 15.7 KB (15701 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.7.17` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:24bc87defac4c83616b004eddc63b57c2f431c7a5b093208da5551112ba26908
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.0 MB (63024462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc59f27a3fd37b6856dd726731f2cdf9ccab8da93af97d69a724c9abcb17e783`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 24 Apr 2024 04:07:25 GMT
ADD file:83a77ac4b262a896dbca1f6974e4401639b3e4d4ca432d88a933c7983e8ccf10 in / 
# Wed, 24 Apr 2024 04:07:25 GMT
CMD ["bash"]
# Fri, 26 Apr 2024 13:23:50 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Fri, 26 Apr 2024 13:23:50 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 26 Apr 2024 13:23:50 GMT
VOLUME [/var/lib/chronograf]
# Fri, 26 Apr 2024 13:23:50 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Apr 2024 13:23:50 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:913a7319952754f0a4a369ee846fb9ecf15cbbead6a1be0f4bdf4a7cbeb1d33c`  
		Last Modified: Wed, 24 Apr 2024 04:11:56 GMT  
		Size: 26.6 MB (26594742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a02d4e2dcc0c18f1edb50078447fc9db19b875a366eefa52d2f7924faa93dc8`  
		Last Modified: Wed, 01 May 2024 22:07:22 GMT  
		Size: 3.5 MB (3511608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c399cb825747bd01b7b446a7c516df7e0736286e5a13254cf67f7327f3cf398`  
		Last Modified: Wed, 01 May 2024 22:07:23 GMT  
		Size: 32.9 MB (32893710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e03e02c499fea8e567f6c934658b1c0419f48cb3b73333cc6a5c43138ecd694b`  
		Last Modified: Wed, 01 May 2024 22:07:22 GMT  
		Size: 12.3 KB (12251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f9cf20464d7eea3168bb9a79cb631569c3c91b624cc469d86d673045beaa9bd`  
		Last Modified: Wed, 01 May 2024 22:07:22 GMT  
		Size: 11.9 KB (11911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a98822bfb3ab70f0c5c12b68241180145dfed495a8fc2710f92afdb2580b2b5b`  
		Last Modified: Wed, 01 May 2024 22:07:23 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7.17` - unknown; unknown

```console
$ docker pull chronograf@sha256:14c0258a045dd6cbf8ec922a69b575374599923cd09fb9a55d0d912400da6cbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2885115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c319a7f9210a01ab89791d1b8e3608bdb4bbeb9c1199931a4027064167349458`

```dockerfile
```

-	Layers:
	-	`sha256:198e11891e568f2a76a22cb55d06776ae6149b21c9248d3ebe30370ae5fd9ed8`  
		Last Modified: Wed, 01 May 2024 22:07:22 GMT  
		Size: 2.9 MB (2869514 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2980ce3ea639ef05061227f89a728e920aaf5491f6a3d368655e626bbf9ad88`  
		Last Modified: Wed, 01 May 2024 22:07:22 GMT  
		Size: 15.6 KB (15601 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.7.17` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:feaa26d7c7395560df9df720d143b82f638a6c1f0702cd778cfb4c5f46ed6def
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.4 MB (67356179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:844bbe76861fef142dc0cc704424d2005bf3d8250bb01bf44cf757cd1ea2e509`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:54 GMT
ADD file:e8990741de71fcc1884f30fcd1b6c5ea411bfa752419a82e9748fcd378ca100a in / 
# Wed, 24 Apr 2024 04:10:54 GMT
CMD ["bash"]
# Fri, 26 Apr 2024 13:23:50 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Fri, 26 Apr 2024 13:23:50 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 26 Apr 2024 13:23:50 GMT
VOLUME [/var/lib/chronograf]
# Fri, 26 Apr 2024 13:23:50 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Apr 2024 13:23:50 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:40a322c395ab3df43e27d8be65cc48139c091588ac868643a02567ca247d0c73`  
		Last Modified: Wed, 24 Apr 2024 04:14:48 GMT  
		Size: 30.1 MB (30087336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:241dc733a2765d1ed6b5df2ad5a04edd25d816d790ee85807e647a3703919ea0`  
		Last Modified: Wed, 01 May 2024 22:24:18 GMT  
		Size: 4.2 MB (4210545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:268e94289fff21f738f3871b0fcbfba9b98c5f703ed616181a59df8c19a66a02`  
		Last Modified: Wed, 01 May 2024 22:24:19 GMT  
		Size: 33.0 MB (33033899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:889ea780f967eeaf1a35da1a75e281ffa6cc71e38d06e2895227685a703aea34`  
		Last Modified: Wed, 01 May 2024 22:24:18 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edaf118e59ce4b51ecadbcc627b491fda58e175ad8499ef61709b9e94d8733f4`  
		Last Modified: Wed, 01 May 2024 22:24:18 GMT  
		Size: 11.9 KB (11912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f61b2bc02d9d1365b9369462541909296760a8dcf3b9c65ba494fff9c3a53f41`  
		Last Modified: Wed, 01 May 2024 22:24:19 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7.17` - unknown; unknown

```console
$ docker pull chronograf@sha256:fa70d9133049bae88f878027769410ece28589e1a2981b61857e08e065204e67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2883006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bc46ab248d0b03f6a2a754a6b204fc431aa76764921b11fdcc76e1bbde3b482`

```dockerfile
```

-	Layers:
	-	`sha256:a8307e0a8364066aafba104ad26d1e97f945019e407934613ed1f9b98763a607`  
		Last Modified: Wed, 01 May 2024 22:24:18 GMT  
		Size: 2.9 MB (2867467 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dfae096072032baf73a1ac486e9c5f6f3d82facbe9028c876ce649470d0dd770`  
		Last Modified: Wed, 01 May 2024 22:24:18 GMT  
		Size: 15.5 KB (15539 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.7.17-alpine`

```console
$ docker pull chronograf@sha256:928b0a355d0fbeec6b13e9526b9625c464ac595eb3395f795029e9050e697b6a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.7.17-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:b9c6ca19fbcf0459c66980dfbedf1468bfe1aa2f7e8f23bdc2808c6f5725680b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.3 MB (23255145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:545aecf6038870239dfd16bcd783a9aa43a8e7395d0fd0911c217cb2d1b280a4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:02 GMT
ADD file:c44c9bd36ba35cc78fb9396304ea008def9f42a3beef76aa33b2cf1fde1c10b3 in / 
# Sat, 27 Jan 2024 00:31:02 GMT
CMD ["/bin/sh"]
# Fri, 26 Apr 2024 13:23:50 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Fri, 26 Apr 2024 13:23:50 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 26 Apr 2024 13:23:50 GMT
VOLUME [/var/lib/chronograf]
# Fri, 26 Apr 2024 13:23:50 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Apr 2024 13:23:50 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:3c854c8cbf469fda815b8f6183300c07cfa2fbb5703859ca79aff93ae934961b`  
		Last Modified: Sat, 27 Jan 2024 00:31:44 GMT  
		Size: 3.4 MB (3379404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f856bcbf54737edf390824db1bece56b8c5fc05a6f2357cf56aff5cc454b7815`  
		Last Modified: Wed, 01 May 2024 21:52:13 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f682ae190076e739abc29ac7268f8311bf0f89cd06898bdbf626d365256991f`  
		Last Modified: Wed, 01 May 2024 21:52:13 GMT  
		Size: 293.8 KB (293819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78b77340b0623e50c661f5c33aa9a52eda57aaee21bcae42f4bca10376bca837`  
		Last Modified: Wed, 01 May 2024 21:52:13 GMT  
		Size: 19.6 MB (19557279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9800825cd1091a4a5a9ea6780c03cbb785566d2a46a67c67adddee5d1257631f`  
		Last Modified: Wed, 01 May 2024 21:52:13 GMT  
		Size: 12.2 KB (12231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62a6068243de8a38e51180eb703f4a7074577730f5d5c7396684e2e01c761cfc`  
		Last Modified: Wed, 01 May 2024 21:52:14 GMT  
		Size: 11.9 KB (11894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff9637de3f7407a724769b527d8ce12f0599ebe99c39e30fc48f76897d885a23`  
		Last Modified: Wed, 01 May 2024 21:52:14 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7.17-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:ef74a07b8e210fe8679e422c5f3baa0c69a6f6a225504e61fca49dbb9c3844a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.0 KB (189001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9666d76fae59dccd086b0c79b67c9d87c71ef8822f7df72f3beb5b3ce74c3d5f`

```dockerfile
```

-	Layers:
	-	`sha256:752685232661d306de8c69d57fb0f651e4724b416adf5d76ce6e05fce95f1f72`  
		Last Modified: Wed, 01 May 2024 21:52:13 GMT  
		Size: 172.2 KB (172188 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1ed049f07a9377f3e36162dfcd54ca83c3ae9304da37fa9f0c479366fe98c29`  
		Last Modified: Wed, 01 May 2024 21:52:13 GMT  
		Size: 16.8 KB (16813 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.8`

```console
$ docker pull chronograf@sha256:29736a44e864ef5d80157ff969bebc0f1a0c071c1e15a585c3fd348c79090625
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
$ docker pull chronograf@sha256:dc8db5815b9d119e2605cc84a2fd44a61a313d31e6d0b5cb72dc71cace20b051
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.8 MB (70843750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a377c5c8e8259b19d73e5dc616d29d203e4fd06f817d6abc1be7cfb9481aa52d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:31 GMT
ADD file:0e5a7771d5c0c58072db41fa02f288def8a40f2116b48e6127f1034f848bc2cd in / 
# Wed, 24 Apr 2024 03:28:32 GMT
CMD ["bash"]
# Fri, 26 Apr 2024 13:23:50 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Fri, 26 Apr 2024 13:23:50 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 26 Apr 2024 13:23:50 GMT
VOLUME [/var/lib/chronograf]
# Fri, 26 Apr 2024 13:23:50 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Apr 2024 13:23:50 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:6177a7f9989f56e11ac23856a0c014002800d83111aaa3e41fb2591161a166c2`  
		Last Modified: Wed, 24 Apr 2024 03:33:23 GMT  
		Size: 31.4 MB (31434263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:657898ef93dd5fef6983c8dc73cf426aa65ac37585779fff62ded83f4d5c1155`  
		Last Modified: Wed, 01 May 2024 21:52:23 GMT  
		Size: 5.0 MB (5020999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff62cb8cc9bb2e4dde852457b7ccff737fa910dbc9d4736b06cf64769c2ff45a`  
		Last Modified: Wed, 01 May 2024 21:52:23 GMT  
		Size: 34.4 MB (34364084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aabbd8db9262c6c83e581256f52fb92c2ff481756cfc50ad970184bdc5ccf406`  
		Last Modified: Wed, 01 May 2024 21:52:23 GMT  
		Size: 12.3 KB (12252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a916d2f8b63f3d60c2d45adedff83fc2f75426c674f9b4dce4a98850ca50507`  
		Last Modified: Wed, 01 May 2024 21:52:23 GMT  
		Size: 11.9 KB (11912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2557c02f17a258f3539eb8bb650c4c19a012c925e0a0adb90b7b89e152f5df7e`  
		Last Modified: Wed, 01 May 2024 21:52:23 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8` - unknown; unknown

```console
$ docker pull chronograf@sha256:ed95ebfd68e36bf7411569ca5ddeeab3c899b6a0d4b5b3986c1209062d299b61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2931054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a5aa18b64b23309d6f36d0c2773db71456c360a602459e1f8956930ce57dd80`

```dockerfile
```

-	Layers:
	-	`sha256:21b4c4ce2c390289235b77c4bb3043b3f408c7f0f1baafb38508596bed8023aa`  
		Last Modified: Wed, 01 May 2024 21:52:23 GMT  
		Size: 2.9 MB (2915313 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6d8761eb0c3742403371bf8c57281e46fc5e6bc8110c3520fc401cc2605472f`  
		Last Modified: Wed, 01 May 2024 21:52:23 GMT  
		Size: 15.7 KB (15741 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.8` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:ed7bce4bdf71f3892aecd3f4930162da8949091b9c8045477e19cc0a2a196a1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.4 MB (63439846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dbb4c8936316accfd0547f15087206bb68cba2894fa8eb993041c7add639328`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 24 Apr 2024 04:07:25 GMT
ADD file:83a77ac4b262a896dbca1f6974e4401639b3e4d4ca432d88a933c7983e8ccf10 in / 
# Wed, 24 Apr 2024 04:07:25 GMT
CMD ["bash"]
# Fri, 26 Apr 2024 13:23:50 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Fri, 26 Apr 2024 13:23:50 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 26 Apr 2024 13:23:50 GMT
VOLUME [/var/lib/chronograf]
# Fri, 26 Apr 2024 13:23:50 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Apr 2024 13:23:50 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:913a7319952754f0a4a369ee846fb9ecf15cbbead6a1be0f4bdf4a7cbeb1d33c`  
		Last Modified: Wed, 24 Apr 2024 04:11:56 GMT  
		Size: 26.6 MB (26594742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a302c781c4408e94b4c3e6674ccf180302198aa3f60c91c5758c490f01e64ee`  
		Last Modified: Wed, 01 May 2024 22:08:10 GMT  
		Size: 4.3 MB (4285961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d4a854bc3075530223c718eb1a3f11362b02e787db9041abcc2e3e1c2d44c0d`  
		Last Modified: Wed, 01 May 2024 22:08:10 GMT  
		Size: 32.5 MB (32534742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aaef33f5603fef1b3ef4569f9f1f4ccf1cae3f668c654cfa1b981b7ec03f0df`  
		Last Modified: Wed, 01 May 2024 22:08:09 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c5840ec825f85841482024dc1956a8c8759960b4ea95337b27a0c8a37da5a89`  
		Last Modified: Wed, 01 May 2024 22:08:09 GMT  
		Size: 11.9 KB (11911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ce14e7932d1a8b7272ccd4b7219f9ea13cc0866c25763299521d9a65a56237a`  
		Last Modified: Wed, 01 May 2024 22:08:10 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8` - unknown; unknown

```console
$ docker pull chronograf@sha256:1f084c163056d93967d6a6dcfb700d9e9240292f53712449e54be80b538be8af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2933224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d82fd92cf67661e7eeb574a8e40155f767facf2dbf01246ae8cd14a60b7c09d8`

```dockerfile
```

-	Layers:
	-	`sha256:e2ca788bd8f00e0fadeaa07c895a64a8db98a6a10116eef39c1ff78f1a4c2bfc`  
		Last Modified: Wed, 01 May 2024 22:08:10 GMT  
		Size: 2.9 MB (2917583 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ea8b8820ef2ed0ed73daf45529b5dd7261443626e667ec987dca2f0fb115245`  
		Last Modified: Wed, 01 May 2024 22:08:09 GMT  
		Size: 15.6 KB (15641 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.8` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:1fdab5644c6923c0008548d3a794afd6c16daffc4a7a9666ffdaba87b53970a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.5 MB (67545197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8bf21a1a9476746feeecf1a077b6ccd7cc52c8b50831e9cee1aa145d820c900`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:54 GMT
ADD file:e8990741de71fcc1884f30fcd1b6c5ea411bfa752419a82e9748fcd378ca100a in / 
# Wed, 24 Apr 2024 04:10:54 GMT
CMD ["bash"]
# Fri, 26 Apr 2024 13:23:50 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Fri, 26 Apr 2024 13:23:50 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 26 Apr 2024 13:23:50 GMT
VOLUME [/var/lib/chronograf]
# Fri, 26 Apr 2024 13:23:50 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Apr 2024 13:23:50 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:40a322c395ab3df43e27d8be65cc48139c091588ac868643a02567ca247d0c73`  
		Last Modified: Wed, 24 Apr 2024 04:14:48 GMT  
		Size: 30.1 MB (30087336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4a6e23c8c428db58c77f34fd8c6769eb773c6862e5f9137c4cbcd2b171bd80f`  
		Last Modified: Wed, 01 May 2024 22:25:51 GMT  
		Size: 5.0 MB (5004084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6137daa81d6407d77d85919ba8d1ba4d92fed2b3242ba22349278fe32ac3d610`  
		Last Modified: Wed, 01 May 2024 22:25:52 GMT  
		Size: 32.4 MB (32429373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a197d582fdc8a30285eda7d2cd5811e5fc214dc2898d8950229f05c61e30abf`  
		Last Modified: Wed, 01 May 2024 22:25:51 GMT  
		Size: 12.3 KB (12253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:424764863809c7c2a698e53f675dfa8d597de2c2319b18f0071b25735d68f831`  
		Last Modified: Wed, 01 May 2024 22:25:51 GMT  
		Size: 11.9 KB (11912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da55de4fa23002012b06ec2d9861b2e673c46efdb95559f91e4576d5f7f25c78`  
		Last Modified: Wed, 01 May 2024 22:25:52 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8` - unknown; unknown

```console
$ docker pull chronograf@sha256:24d08e162ee287a2da2daa8a07263eb3cbf191fa41d432e1d428f88466004367
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2931116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23783b0c7573625f24845b856382305f9a91a48cfe13fbbc896c2d38cb6b182f`

```dockerfile
```

-	Layers:
	-	`sha256:a39132a2a5742f8af2469a4c4259071cec5c319bc2d052568f53794171ede80f`  
		Last Modified: Wed, 01 May 2024 22:25:51 GMT  
		Size: 2.9 MB (2915536 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1147352d808cb4858205f73c4d4da6326838ad937ce386120fba53b3b7dc49f4`  
		Last Modified: Wed, 01 May 2024 22:25:51 GMT  
		Size: 15.6 KB (15580 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.8-alpine`

```console
$ docker pull chronograf@sha256:783f7f57144b3cb1223f79c8ed7fc2acbf57f228b7cb198886a7c4a1bbb92a31
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.8-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:988ca69d0a21c9c8449ff282652240a633d82a4224e283237eb077baf70d04c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.9 MB (22901673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:826da14f207d3d9875fb4098bf34b2433742088b63e563d4a335190e8fb8fdc2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:02 GMT
ADD file:c44c9bd36ba35cc78fb9396304ea008def9f42a3beef76aa33b2cf1fde1c10b3 in / 
# Sat, 27 Jan 2024 00:31:02 GMT
CMD ["/bin/sh"]
# Fri, 26 Apr 2024 13:23:50 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Fri, 26 Apr 2024 13:23:50 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 26 Apr 2024 13:23:50 GMT
VOLUME [/var/lib/chronograf]
# Fri, 26 Apr 2024 13:23:50 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Apr 2024 13:23:50 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:3c854c8cbf469fda815b8f6183300c07cfa2fbb5703859ca79aff93ae934961b`  
		Last Modified: Sat, 27 Jan 2024 00:31:44 GMT  
		Size: 3.4 MB (3379404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f856bcbf54737edf390824db1bece56b8c5fc05a6f2357cf56aff5cc454b7815`  
		Last Modified: Wed, 01 May 2024 21:52:13 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f682ae190076e739abc29ac7268f8311bf0f89cd06898bdbf626d365256991f`  
		Last Modified: Wed, 01 May 2024 21:52:13 GMT  
		Size: 293.8 KB (293819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e085ab93f5a719335e00baffda9fda197f6dabf01519266f034246d788a0e8a1`  
		Last Modified: Wed, 01 May 2024 21:52:15 GMT  
		Size: 19.2 MB (19203807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9800825cd1091a4a5a9ea6780c03cbb785566d2a46a67c67adddee5d1257631f`  
		Last Modified: Wed, 01 May 2024 21:52:13 GMT  
		Size: 12.2 KB (12231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62a6068243de8a38e51180eb703f4a7074577730f5d5c7396684e2e01c761cfc`  
		Last Modified: Wed, 01 May 2024 21:52:14 GMT  
		Size: 11.9 KB (11894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff9637de3f7407a724769b527d8ce12f0599ebe99c39e30fc48f76897d885a23`  
		Last Modified: Wed, 01 May 2024 21:52:14 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:5494979ee29716f641192f16fd8399bc8b3dc3b778589c93813bafbc1252b0ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.7 KB (237732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:654dfdae68d2e33518e4acf5e67e933041433c6d0683740274a6063ef7177de7`

```dockerfile
```

-	Layers:
	-	`sha256:b3bd066b3ae87fb97f88345084ed238a0ea3134aadb3750d5d27b949f70fb82f`  
		Last Modified: Wed, 01 May 2024 21:52:15 GMT  
		Size: 220.9 KB (220918 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1137d4428bed044fa1f9beedd0862da2b91a6a2c291bdfcee0a98519653b69d`  
		Last Modified: Wed, 01 May 2024 21:52:15 GMT  
		Size: 16.8 KB (16814 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.8.10`

```console
$ docker pull chronograf@sha256:29736a44e864ef5d80157ff969bebc0f1a0c071c1e15a585c3fd348c79090625
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
$ docker pull chronograf@sha256:dc8db5815b9d119e2605cc84a2fd44a61a313d31e6d0b5cb72dc71cace20b051
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.8 MB (70843750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a377c5c8e8259b19d73e5dc616d29d203e4fd06f817d6abc1be7cfb9481aa52d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:31 GMT
ADD file:0e5a7771d5c0c58072db41fa02f288def8a40f2116b48e6127f1034f848bc2cd in / 
# Wed, 24 Apr 2024 03:28:32 GMT
CMD ["bash"]
# Fri, 26 Apr 2024 13:23:50 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Fri, 26 Apr 2024 13:23:50 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 26 Apr 2024 13:23:50 GMT
VOLUME [/var/lib/chronograf]
# Fri, 26 Apr 2024 13:23:50 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Apr 2024 13:23:50 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:6177a7f9989f56e11ac23856a0c014002800d83111aaa3e41fb2591161a166c2`  
		Last Modified: Wed, 24 Apr 2024 03:33:23 GMT  
		Size: 31.4 MB (31434263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:657898ef93dd5fef6983c8dc73cf426aa65ac37585779fff62ded83f4d5c1155`  
		Last Modified: Wed, 01 May 2024 21:52:23 GMT  
		Size: 5.0 MB (5020999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff62cb8cc9bb2e4dde852457b7ccff737fa910dbc9d4736b06cf64769c2ff45a`  
		Last Modified: Wed, 01 May 2024 21:52:23 GMT  
		Size: 34.4 MB (34364084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aabbd8db9262c6c83e581256f52fb92c2ff481756cfc50ad970184bdc5ccf406`  
		Last Modified: Wed, 01 May 2024 21:52:23 GMT  
		Size: 12.3 KB (12252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a916d2f8b63f3d60c2d45adedff83fc2f75426c674f9b4dce4a98850ca50507`  
		Last Modified: Wed, 01 May 2024 21:52:23 GMT  
		Size: 11.9 KB (11912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2557c02f17a258f3539eb8bb650c4c19a012c925e0a0adb90b7b89e152f5df7e`  
		Last Modified: Wed, 01 May 2024 21:52:23 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:ed95ebfd68e36bf7411569ca5ddeeab3c899b6a0d4b5b3986c1209062d299b61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2931054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a5aa18b64b23309d6f36d0c2773db71456c360a602459e1f8956930ce57dd80`

```dockerfile
```

-	Layers:
	-	`sha256:21b4c4ce2c390289235b77c4bb3043b3f408c7f0f1baafb38508596bed8023aa`  
		Last Modified: Wed, 01 May 2024 21:52:23 GMT  
		Size: 2.9 MB (2915313 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6d8761eb0c3742403371bf8c57281e46fc5e6bc8110c3520fc401cc2605472f`  
		Last Modified: Wed, 01 May 2024 21:52:23 GMT  
		Size: 15.7 KB (15741 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.8.10` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:ed7bce4bdf71f3892aecd3f4930162da8949091b9c8045477e19cc0a2a196a1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.4 MB (63439846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dbb4c8936316accfd0547f15087206bb68cba2894fa8eb993041c7add639328`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 24 Apr 2024 04:07:25 GMT
ADD file:83a77ac4b262a896dbca1f6974e4401639b3e4d4ca432d88a933c7983e8ccf10 in / 
# Wed, 24 Apr 2024 04:07:25 GMT
CMD ["bash"]
# Fri, 26 Apr 2024 13:23:50 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Fri, 26 Apr 2024 13:23:50 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 26 Apr 2024 13:23:50 GMT
VOLUME [/var/lib/chronograf]
# Fri, 26 Apr 2024 13:23:50 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Apr 2024 13:23:50 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:913a7319952754f0a4a369ee846fb9ecf15cbbead6a1be0f4bdf4a7cbeb1d33c`  
		Last Modified: Wed, 24 Apr 2024 04:11:56 GMT  
		Size: 26.6 MB (26594742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a302c781c4408e94b4c3e6674ccf180302198aa3f60c91c5758c490f01e64ee`  
		Last Modified: Wed, 01 May 2024 22:08:10 GMT  
		Size: 4.3 MB (4285961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d4a854bc3075530223c718eb1a3f11362b02e787db9041abcc2e3e1c2d44c0d`  
		Last Modified: Wed, 01 May 2024 22:08:10 GMT  
		Size: 32.5 MB (32534742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aaef33f5603fef1b3ef4569f9f1f4ccf1cae3f668c654cfa1b981b7ec03f0df`  
		Last Modified: Wed, 01 May 2024 22:08:09 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c5840ec825f85841482024dc1956a8c8759960b4ea95337b27a0c8a37da5a89`  
		Last Modified: Wed, 01 May 2024 22:08:09 GMT  
		Size: 11.9 KB (11911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ce14e7932d1a8b7272ccd4b7219f9ea13cc0866c25763299521d9a65a56237a`  
		Last Modified: Wed, 01 May 2024 22:08:10 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:1f084c163056d93967d6a6dcfb700d9e9240292f53712449e54be80b538be8af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2933224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d82fd92cf67661e7eeb574a8e40155f767facf2dbf01246ae8cd14a60b7c09d8`

```dockerfile
```

-	Layers:
	-	`sha256:e2ca788bd8f00e0fadeaa07c895a64a8db98a6a10116eef39c1ff78f1a4c2bfc`  
		Last Modified: Wed, 01 May 2024 22:08:10 GMT  
		Size: 2.9 MB (2917583 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ea8b8820ef2ed0ed73daf45529b5dd7261443626e667ec987dca2f0fb115245`  
		Last Modified: Wed, 01 May 2024 22:08:09 GMT  
		Size: 15.6 KB (15641 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.8.10` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:1fdab5644c6923c0008548d3a794afd6c16daffc4a7a9666ffdaba87b53970a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.5 MB (67545197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8bf21a1a9476746feeecf1a077b6ccd7cc52c8b50831e9cee1aa145d820c900`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:54 GMT
ADD file:e8990741de71fcc1884f30fcd1b6c5ea411bfa752419a82e9748fcd378ca100a in / 
# Wed, 24 Apr 2024 04:10:54 GMT
CMD ["bash"]
# Fri, 26 Apr 2024 13:23:50 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Fri, 26 Apr 2024 13:23:50 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 26 Apr 2024 13:23:50 GMT
VOLUME [/var/lib/chronograf]
# Fri, 26 Apr 2024 13:23:50 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Apr 2024 13:23:50 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:40a322c395ab3df43e27d8be65cc48139c091588ac868643a02567ca247d0c73`  
		Last Modified: Wed, 24 Apr 2024 04:14:48 GMT  
		Size: 30.1 MB (30087336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4a6e23c8c428db58c77f34fd8c6769eb773c6862e5f9137c4cbcd2b171bd80f`  
		Last Modified: Wed, 01 May 2024 22:25:51 GMT  
		Size: 5.0 MB (5004084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6137daa81d6407d77d85919ba8d1ba4d92fed2b3242ba22349278fe32ac3d610`  
		Last Modified: Wed, 01 May 2024 22:25:52 GMT  
		Size: 32.4 MB (32429373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a197d582fdc8a30285eda7d2cd5811e5fc214dc2898d8950229f05c61e30abf`  
		Last Modified: Wed, 01 May 2024 22:25:51 GMT  
		Size: 12.3 KB (12253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:424764863809c7c2a698e53f675dfa8d597de2c2319b18f0071b25735d68f831`  
		Last Modified: Wed, 01 May 2024 22:25:51 GMT  
		Size: 11.9 KB (11912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da55de4fa23002012b06ec2d9861b2e673c46efdb95559f91e4576d5f7f25c78`  
		Last Modified: Wed, 01 May 2024 22:25:52 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:24d08e162ee287a2da2daa8a07263eb3cbf191fa41d432e1d428f88466004367
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2931116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23783b0c7573625f24845b856382305f9a91a48cfe13fbbc896c2d38cb6b182f`

```dockerfile
```

-	Layers:
	-	`sha256:a39132a2a5742f8af2469a4c4259071cec5c319bc2d052568f53794171ede80f`  
		Last Modified: Wed, 01 May 2024 22:25:51 GMT  
		Size: 2.9 MB (2915536 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1147352d808cb4858205f73c4d4da6326838ad937ce386120fba53b3b7dc49f4`  
		Last Modified: Wed, 01 May 2024 22:25:51 GMT  
		Size: 15.6 KB (15580 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.8.10-alpine`

```console
$ docker pull chronograf@sha256:783f7f57144b3cb1223f79c8ed7fc2acbf57f228b7cb198886a7c4a1bbb92a31
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.8.10-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:988ca69d0a21c9c8449ff282652240a633d82a4224e283237eb077baf70d04c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.9 MB (22901673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:826da14f207d3d9875fb4098bf34b2433742088b63e563d4a335190e8fb8fdc2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:02 GMT
ADD file:c44c9bd36ba35cc78fb9396304ea008def9f42a3beef76aa33b2cf1fde1c10b3 in / 
# Sat, 27 Jan 2024 00:31:02 GMT
CMD ["/bin/sh"]
# Fri, 26 Apr 2024 13:23:50 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Fri, 26 Apr 2024 13:23:50 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 26 Apr 2024 13:23:50 GMT
VOLUME [/var/lib/chronograf]
# Fri, 26 Apr 2024 13:23:50 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Apr 2024 13:23:50 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:3c854c8cbf469fda815b8f6183300c07cfa2fbb5703859ca79aff93ae934961b`  
		Last Modified: Sat, 27 Jan 2024 00:31:44 GMT  
		Size: 3.4 MB (3379404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f856bcbf54737edf390824db1bece56b8c5fc05a6f2357cf56aff5cc454b7815`  
		Last Modified: Wed, 01 May 2024 21:52:13 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f682ae190076e739abc29ac7268f8311bf0f89cd06898bdbf626d365256991f`  
		Last Modified: Wed, 01 May 2024 21:52:13 GMT  
		Size: 293.8 KB (293819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e085ab93f5a719335e00baffda9fda197f6dabf01519266f034246d788a0e8a1`  
		Last Modified: Wed, 01 May 2024 21:52:15 GMT  
		Size: 19.2 MB (19203807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9800825cd1091a4a5a9ea6780c03cbb785566d2a46a67c67adddee5d1257631f`  
		Last Modified: Wed, 01 May 2024 21:52:13 GMT  
		Size: 12.2 KB (12231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62a6068243de8a38e51180eb703f4a7074577730f5d5c7396684e2e01c761cfc`  
		Last Modified: Wed, 01 May 2024 21:52:14 GMT  
		Size: 11.9 KB (11894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff9637de3f7407a724769b527d8ce12f0599ebe99c39e30fc48f76897d885a23`  
		Last Modified: Wed, 01 May 2024 21:52:14 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8.10-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:5494979ee29716f641192f16fd8399bc8b3dc3b778589c93813bafbc1252b0ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.7 KB (237732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:654dfdae68d2e33518e4acf5e67e933041433c6d0683740274a6063ef7177de7`

```dockerfile
```

-	Layers:
	-	`sha256:b3bd066b3ae87fb97f88345084ed238a0ea3134aadb3750d5d27b949f70fb82f`  
		Last Modified: Wed, 01 May 2024 21:52:15 GMT  
		Size: 220.9 KB (220918 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1137d4428bed044fa1f9beedd0862da2b91a6a2c291bdfcee0a98519653b69d`  
		Last Modified: Wed, 01 May 2024 21:52:15 GMT  
		Size: 16.8 KB (16814 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.9`

```console
$ docker pull chronograf@sha256:8fa8138a6785a86e24ad7514c3cb463405ac1eebf862a6404eefd06409fd6116
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
$ docker pull chronograf@sha256:b48026dcc5ce8f15ac67e4e1fa822101490c1a71f35b3aef31fd6a5323e8b339
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.5 MB (71491273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc034e7758d41efcb9a1a435c34534097d986d9d78f901fcba93c7912140e029`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:31 GMT
ADD file:0e5a7771d5c0c58072db41fa02f288def8a40f2116b48e6127f1034f848bc2cd in / 
# Wed, 24 Apr 2024 03:28:32 GMT
CMD ["bash"]
# Fri, 26 Apr 2024 13:23:50 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Fri, 26 Apr 2024 13:23:50 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 26 Apr 2024 13:23:50 GMT
VOLUME [/var/lib/chronograf]
# Fri, 26 Apr 2024 13:23:50 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Apr 2024 13:23:50 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:6177a7f9989f56e11ac23856a0c014002800d83111aaa3e41fb2591161a166c2`  
		Last Modified: Wed, 24 Apr 2024 03:33:23 GMT  
		Size: 31.4 MB (31434263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f612a532a64ce0d6b3a0f0da48d5794186cbc39ca9c04f17cb191c9111fe094`  
		Last Modified: Wed, 01 May 2024 21:52:25 GMT  
		Size: 5.0 MB (5021019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d954f26c303744af0c33cb582f0a2997cd5b6e28ac458cfdf1851b0613ed8b04`  
		Last Modified: Wed, 01 May 2024 21:52:26 GMT  
		Size: 35.0 MB (35011581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5132d968aa0bcc795d6aa3ec8ead2a1d38d2dfb1e8d558fb759807a31b1a4f63`  
		Last Modified: Wed, 01 May 2024 21:52:25 GMT  
		Size: 12.3 KB (12255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b91e6fd6b9ab0dbbffb9973750cd530c9e997455313b18e7a8ba2445c7175cfc`  
		Last Modified: Wed, 01 May 2024 21:52:25 GMT  
		Size: 11.9 KB (11915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:749e1e49fbbd69bde4e963cb7bb03a54b2a26b86549945237b41aa31bfb07a85`  
		Last Modified: Wed, 01 May 2024 21:52:26 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9` - unknown; unknown

```console
$ docker pull chronograf@sha256:530075da02dd7c5403c4410d238d1334a6275747cb0e3541343db722802d1487
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2935337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:831de0f45374e06c3f592239c1aca9b5a6a0cb1f5b7a9c3d18ef62e9541302e5`

```dockerfile
```

-	Layers:
	-	`sha256:92bf8bcc5816090daf10d22ab687ee3c541fd1b914b00da82e530a0ba781ecae`  
		Last Modified: Wed, 01 May 2024 21:52:25 GMT  
		Size: 2.9 MB (2919603 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6538b3aa945aa94c737e925ab098a6e9fd2adbe96f1e87bdf56adb2425dbb504`  
		Last Modified: Wed, 01 May 2024 21:52:25 GMT  
		Size: 15.7 KB (15734 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.9` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:f597a6b6919d22adde89ea006072b5ddb6c201f191aca711989916f65e4a3dd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.2 MB (64216498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d20e2cf8ed9cc07e66ae04f82b42625d2aecb30551e266834e3bddd17946e04`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 24 Apr 2024 04:07:25 GMT
ADD file:83a77ac4b262a896dbca1f6974e4401639b3e4d4ca432d88a933c7983e8ccf10 in / 
# Wed, 24 Apr 2024 04:07:25 GMT
CMD ["bash"]
# Fri, 26 Apr 2024 13:23:50 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Fri, 26 Apr 2024 13:23:50 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 26 Apr 2024 13:23:50 GMT
VOLUME [/var/lib/chronograf]
# Fri, 26 Apr 2024 13:23:50 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Apr 2024 13:23:50 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:913a7319952754f0a4a369ee846fb9ecf15cbbead6a1be0f4bdf4a7cbeb1d33c`  
		Last Modified: Wed, 24 Apr 2024 04:11:56 GMT  
		Size: 26.6 MB (26594742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a302c781c4408e94b4c3e6674ccf180302198aa3f60c91c5758c490f01e64ee`  
		Last Modified: Wed, 01 May 2024 22:08:10 GMT  
		Size: 4.3 MB (4285961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9643bbb65f87c523500671f827897abf0d14dfa83bb3d8f549c78e9efa2438d3`  
		Last Modified: Wed, 01 May 2024 22:08:49 GMT  
		Size: 33.3 MB (33311386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1402527242400cf2b213c5739ca593fb25afcca5b5ba2edf737c281665f6aec2`  
		Last Modified: Wed, 01 May 2024 22:08:47 GMT  
		Size: 12.3 KB (12255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6096ddd41567ceba4273266fd86f1843231f2851a798773fec659d29e3897fb7`  
		Last Modified: Wed, 01 May 2024 22:08:47 GMT  
		Size: 11.9 KB (11914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed9ea445163b72fa4566be7388ea2f24810d1f0768f71d2cecb968196aa4bdf`  
		Last Modified: Wed, 01 May 2024 22:08:48 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9` - unknown; unknown

```console
$ docker pull chronograf@sha256:17e44db873457384420cbfefe411938db3fd7ff8cde4e8c4c22ea999d9eda1db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2937507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d1b43f3a271d26a10b78d63fa08ac7320a3cfde5fcbc549746ec361e1d62fc9`

```dockerfile
```

-	Layers:
	-	`sha256:45133544e4c49bfbaead688f4e7bc8e9040e928a4aecc0a8f3f4c13b1fff4155`  
		Last Modified: Wed, 01 May 2024 22:08:47 GMT  
		Size: 2.9 MB (2921873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c593615a6ccac02bb20b6a97eed5c8f682d0e6942d141a1d6853d4615ccd1ed5`  
		Last Modified: Wed, 01 May 2024 22:08:47 GMT  
		Size: 15.6 KB (15634 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.9` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:1033b73e755be0640a3e70dda0e2606c3189eb468defc12d0d914f4b64041b42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.3 MB (68297241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04186bb844058bad01509429b797f672386aa30c4c8ca144c95015cdb26a97cd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:54 GMT
ADD file:e8990741de71fcc1884f30fcd1b6c5ea411bfa752419a82e9748fcd378ca100a in / 
# Wed, 24 Apr 2024 04:10:54 GMT
CMD ["bash"]
# Fri, 26 Apr 2024 13:23:50 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Fri, 26 Apr 2024 13:23:50 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 26 Apr 2024 13:23:50 GMT
VOLUME [/var/lib/chronograf]
# Fri, 26 Apr 2024 13:23:50 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Apr 2024 13:23:50 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:40a322c395ab3df43e27d8be65cc48139c091588ac868643a02567ca247d0c73`  
		Last Modified: Wed, 24 Apr 2024 04:14:48 GMT  
		Size: 30.1 MB (30087336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4a6e23c8c428db58c77f34fd8c6769eb773c6862e5f9137c4cbcd2b171bd80f`  
		Last Modified: Wed, 01 May 2024 22:25:51 GMT  
		Size: 5.0 MB (5004084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaa435322d856cdc42ba0d5f370257f1d63eee4ca561534691ab3f58f7c602d2`  
		Last Modified: Wed, 01 May 2024 22:26:23 GMT  
		Size: 33.2 MB (33181415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad432f24ac33dbb82432ab1705c96ddcbdede59cf4b72d552fd8d677bda70b13`  
		Last Modified: Wed, 01 May 2024 22:26:22 GMT  
		Size: 12.3 KB (12254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96f5b8e1cbc0dfd4aceb6545084eb5dfba000d16fbb61a75e53aef8dadc0313c`  
		Last Modified: Wed, 01 May 2024 22:26:22 GMT  
		Size: 11.9 KB (11913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ece554b0e16579f6eca042ac77fda8301b91377fe355fec7e38644069671ed37`  
		Last Modified: Wed, 01 May 2024 22:26:22 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9` - unknown; unknown

```console
$ docker pull chronograf@sha256:32e36bc7d0320878274fd9055c9b49d3ad02e9295ae3d017378f10ceeed72176
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2935399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2efbb8d23e0c30e4a544c0cf050ac9a5859c8e2c1f212dd396a26a4ae79f1bc`

```dockerfile
```

-	Layers:
	-	`sha256:54c21553d4ee45a43b90b1a55c4708c72324deaab32cee2b36b6be9a36df9e09`  
		Last Modified: Wed, 01 May 2024 22:26:23 GMT  
		Size: 2.9 MB (2919826 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a616a16ba79649176f0c1d76cdc4d7df56186bac9419a6a88c5c59c304e39f16`  
		Last Modified: Wed, 01 May 2024 22:26:22 GMT  
		Size: 15.6 KB (15573 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.9-alpine`

```console
$ docker pull chronograf@sha256:3607a1412330759a0309175f05feed5e182de153010072cf2fa35d77e7792d90
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.9-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:0270ede33d6ea81a1f77b1ca82b31b33bc77179ac3eea07062c2143f432e614a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.4 MB (23370321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b993bea2bcbf6e82f08d1419015dbd9142364e724ca1529fe1f2a35e0c293415`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:02 GMT
ADD file:c44c9bd36ba35cc78fb9396304ea008def9f42a3beef76aa33b2cf1fde1c10b3 in / 
# Sat, 27 Jan 2024 00:31:02 GMT
CMD ["/bin/sh"]
# Fri, 26 Apr 2024 13:23:50 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Fri, 26 Apr 2024 13:23:50 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 26 Apr 2024 13:23:50 GMT
VOLUME [/var/lib/chronograf]
# Fri, 26 Apr 2024 13:23:50 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Apr 2024 13:23:50 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:3c854c8cbf469fda815b8f6183300c07cfa2fbb5703859ca79aff93ae934961b`  
		Last Modified: Sat, 27 Jan 2024 00:31:44 GMT  
		Size: 3.4 MB (3379404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55d66e26ed51acf4d96c08bb777b841268e106a7712b3862519b5d7507d4f189`  
		Last Modified: Wed, 01 May 2024 21:52:30 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dfea2aafe084a180e61447e9634f8af46995faa9268477431f491e0992900b5`  
		Last Modified: Wed, 01 May 2024 21:52:30 GMT  
		Size: 293.8 KB (293822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8383b05439ec46b7769b3ef7dc46662e55bf3fb0a8eb297417b0adfa699bad0`  
		Last Modified: Wed, 01 May 2024 21:52:30 GMT  
		Size: 19.7 MB (19672445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1871e53f5f6a8dadc8ec00cdacdf391d6813188f7d1e7c48d8e04eabe2c8bf8`  
		Last Modified: Wed, 01 May 2024 21:52:30 GMT  
		Size: 12.2 KB (12237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57f6b0b2f314a14cdb1ff1d1017020a998e85536ae3036f7ea871eb13a855e56`  
		Last Modified: Wed, 01 May 2024 21:52:31 GMT  
		Size: 11.9 KB (11895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:211a27c77f3168981e3a035b6825b27928c14b6276e07bf6b4f02f809507684c`  
		Last Modified: Wed, 01 May 2024 21:52:31 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:b946e43e28460ea7768378ffe6e8d682fed9033cfb1d326d36bb9daa843b59d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.0 KB (242020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74a6b4c0646fbf108e01db4f2ddeb6fa3e8e9c22d88902a6e75414c299a2c5d5`

```dockerfile
```

-	Layers:
	-	`sha256:ed8c4f682bfeb98432a8a8322036506db17c4b108b1fd3c1a3a2c4b411f24dc1`  
		Last Modified: Wed, 01 May 2024 21:52:30 GMT  
		Size: 225.2 KB (225210 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f2ff59fae389024bf949358e002424f80c60f2a4b5ee8c312f3c020d6fccaed`  
		Last Modified: Wed, 01 May 2024 21:52:29 GMT  
		Size: 16.8 KB (16810 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.9.4`

```console
$ docker pull chronograf@sha256:8fa8138a6785a86e24ad7514c3cb463405ac1eebf862a6404eefd06409fd6116
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
$ docker pull chronograf@sha256:b48026dcc5ce8f15ac67e4e1fa822101490c1a71f35b3aef31fd6a5323e8b339
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.5 MB (71491273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc034e7758d41efcb9a1a435c34534097d986d9d78f901fcba93c7912140e029`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:31 GMT
ADD file:0e5a7771d5c0c58072db41fa02f288def8a40f2116b48e6127f1034f848bc2cd in / 
# Wed, 24 Apr 2024 03:28:32 GMT
CMD ["bash"]
# Fri, 26 Apr 2024 13:23:50 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Fri, 26 Apr 2024 13:23:50 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 26 Apr 2024 13:23:50 GMT
VOLUME [/var/lib/chronograf]
# Fri, 26 Apr 2024 13:23:50 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Apr 2024 13:23:50 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:6177a7f9989f56e11ac23856a0c014002800d83111aaa3e41fb2591161a166c2`  
		Last Modified: Wed, 24 Apr 2024 03:33:23 GMT  
		Size: 31.4 MB (31434263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f612a532a64ce0d6b3a0f0da48d5794186cbc39ca9c04f17cb191c9111fe094`  
		Last Modified: Wed, 01 May 2024 21:52:25 GMT  
		Size: 5.0 MB (5021019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d954f26c303744af0c33cb582f0a2997cd5b6e28ac458cfdf1851b0613ed8b04`  
		Last Modified: Wed, 01 May 2024 21:52:26 GMT  
		Size: 35.0 MB (35011581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5132d968aa0bcc795d6aa3ec8ead2a1d38d2dfb1e8d558fb759807a31b1a4f63`  
		Last Modified: Wed, 01 May 2024 21:52:25 GMT  
		Size: 12.3 KB (12255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b91e6fd6b9ab0dbbffb9973750cd530c9e997455313b18e7a8ba2445c7175cfc`  
		Last Modified: Wed, 01 May 2024 21:52:25 GMT  
		Size: 11.9 KB (11915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:749e1e49fbbd69bde4e963cb7bb03a54b2a26b86549945237b41aa31bfb07a85`  
		Last Modified: Wed, 01 May 2024 21:52:26 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9.4` - unknown; unknown

```console
$ docker pull chronograf@sha256:530075da02dd7c5403c4410d238d1334a6275747cb0e3541343db722802d1487
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2935337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:831de0f45374e06c3f592239c1aca9b5a6a0cb1f5b7a9c3d18ef62e9541302e5`

```dockerfile
```

-	Layers:
	-	`sha256:92bf8bcc5816090daf10d22ab687ee3c541fd1b914b00da82e530a0ba781ecae`  
		Last Modified: Wed, 01 May 2024 21:52:25 GMT  
		Size: 2.9 MB (2919603 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6538b3aa945aa94c737e925ab098a6e9fd2adbe96f1e87bdf56adb2425dbb504`  
		Last Modified: Wed, 01 May 2024 21:52:25 GMT  
		Size: 15.7 KB (15734 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.9.4` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:f597a6b6919d22adde89ea006072b5ddb6c201f191aca711989916f65e4a3dd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.2 MB (64216498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d20e2cf8ed9cc07e66ae04f82b42625d2aecb30551e266834e3bddd17946e04`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 24 Apr 2024 04:07:25 GMT
ADD file:83a77ac4b262a896dbca1f6974e4401639b3e4d4ca432d88a933c7983e8ccf10 in / 
# Wed, 24 Apr 2024 04:07:25 GMT
CMD ["bash"]
# Fri, 26 Apr 2024 13:23:50 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Fri, 26 Apr 2024 13:23:50 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 26 Apr 2024 13:23:50 GMT
VOLUME [/var/lib/chronograf]
# Fri, 26 Apr 2024 13:23:50 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Apr 2024 13:23:50 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:913a7319952754f0a4a369ee846fb9ecf15cbbead6a1be0f4bdf4a7cbeb1d33c`  
		Last Modified: Wed, 24 Apr 2024 04:11:56 GMT  
		Size: 26.6 MB (26594742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a302c781c4408e94b4c3e6674ccf180302198aa3f60c91c5758c490f01e64ee`  
		Last Modified: Wed, 01 May 2024 22:08:10 GMT  
		Size: 4.3 MB (4285961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9643bbb65f87c523500671f827897abf0d14dfa83bb3d8f549c78e9efa2438d3`  
		Last Modified: Wed, 01 May 2024 22:08:49 GMT  
		Size: 33.3 MB (33311386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1402527242400cf2b213c5739ca593fb25afcca5b5ba2edf737c281665f6aec2`  
		Last Modified: Wed, 01 May 2024 22:08:47 GMT  
		Size: 12.3 KB (12255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6096ddd41567ceba4273266fd86f1843231f2851a798773fec659d29e3897fb7`  
		Last Modified: Wed, 01 May 2024 22:08:47 GMT  
		Size: 11.9 KB (11914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed9ea445163b72fa4566be7388ea2f24810d1f0768f71d2cecb968196aa4bdf`  
		Last Modified: Wed, 01 May 2024 22:08:48 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9.4` - unknown; unknown

```console
$ docker pull chronograf@sha256:17e44db873457384420cbfefe411938db3fd7ff8cde4e8c4c22ea999d9eda1db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2937507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d1b43f3a271d26a10b78d63fa08ac7320a3cfde5fcbc549746ec361e1d62fc9`

```dockerfile
```

-	Layers:
	-	`sha256:45133544e4c49bfbaead688f4e7bc8e9040e928a4aecc0a8f3f4c13b1fff4155`  
		Last Modified: Wed, 01 May 2024 22:08:47 GMT  
		Size: 2.9 MB (2921873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c593615a6ccac02bb20b6a97eed5c8f682d0e6942d141a1d6853d4615ccd1ed5`  
		Last Modified: Wed, 01 May 2024 22:08:47 GMT  
		Size: 15.6 KB (15634 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.9.4` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:1033b73e755be0640a3e70dda0e2606c3189eb468defc12d0d914f4b64041b42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.3 MB (68297241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04186bb844058bad01509429b797f672386aa30c4c8ca144c95015cdb26a97cd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:54 GMT
ADD file:e8990741de71fcc1884f30fcd1b6c5ea411bfa752419a82e9748fcd378ca100a in / 
# Wed, 24 Apr 2024 04:10:54 GMT
CMD ["bash"]
# Fri, 26 Apr 2024 13:23:50 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Fri, 26 Apr 2024 13:23:50 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 26 Apr 2024 13:23:50 GMT
VOLUME [/var/lib/chronograf]
# Fri, 26 Apr 2024 13:23:50 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Apr 2024 13:23:50 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:40a322c395ab3df43e27d8be65cc48139c091588ac868643a02567ca247d0c73`  
		Last Modified: Wed, 24 Apr 2024 04:14:48 GMT  
		Size: 30.1 MB (30087336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4a6e23c8c428db58c77f34fd8c6769eb773c6862e5f9137c4cbcd2b171bd80f`  
		Last Modified: Wed, 01 May 2024 22:25:51 GMT  
		Size: 5.0 MB (5004084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaa435322d856cdc42ba0d5f370257f1d63eee4ca561534691ab3f58f7c602d2`  
		Last Modified: Wed, 01 May 2024 22:26:23 GMT  
		Size: 33.2 MB (33181415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad432f24ac33dbb82432ab1705c96ddcbdede59cf4b72d552fd8d677bda70b13`  
		Last Modified: Wed, 01 May 2024 22:26:22 GMT  
		Size: 12.3 KB (12254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96f5b8e1cbc0dfd4aceb6545084eb5dfba000d16fbb61a75e53aef8dadc0313c`  
		Last Modified: Wed, 01 May 2024 22:26:22 GMT  
		Size: 11.9 KB (11913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ece554b0e16579f6eca042ac77fda8301b91377fe355fec7e38644069671ed37`  
		Last Modified: Wed, 01 May 2024 22:26:22 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9.4` - unknown; unknown

```console
$ docker pull chronograf@sha256:32e36bc7d0320878274fd9055c9b49d3ad02e9295ae3d017378f10ceeed72176
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2935399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2efbb8d23e0c30e4a544c0cf050ac9a5859c8e2c1f212dd396a26a4ae79f1bc`

```dockerfile
```

-	Layers:
	-	`sha256:54c21553d4ee45a43b90b1a55c4708c72324deaab32cee2b36b6be9a36df9e09`  
		Last Modified: Wed, 01 May 2024 22:26:23 GMT  
		Size: 2.9 MB (2919826 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a616a16ba79649176f0c1d76cdc4d7df56186bac9419a6a88c5c59c304e39f16`  
		Last Modified: Wed, 01 May 2024 22:26:22 GMT  
		Size: 15.6 KB (15573 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.9.4-alpine`

```console
$ docker pull chronograf@sha256:3607a1412330759a0309175f05feed5e182de153010072cf2fa35d77e7792d90
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.9.4-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:0270ede33d6ea81a1f77b1ca82b31b33bc77179ac3eea07062c2143f432e614a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.4 MB (23370321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b993bea2bcbf6e82f08d1419015dbd9142364e724ca1529fe1f2a35e0c293415`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:02 GMT
ADD file:c44c9bd36ba35cc78fb9396304ea008def9f42a3beef76aa33b2cf1fde1c10b3 in / 
# Sat, 27 Jan 2024 00:31:02 GMT
CMD ["/bin/sh"]
# Fri, 26 Apr 2024 13:23:50 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Fri, 26 Apr 2024 13:23:50 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 26 Apr 2024 13:23:50 GMT
VOLUME [/var/lib/chronograf]
# Fri, 26 Apr 2024 13:23:50 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Apr 2024 13:23:50 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:3c854c8cbf469fda815b8f6183300c07cfa2fbb5703859ca79aff93ae934961b`  
		Last Modified: Sat, 27 Jan 2024 00:31:44 GMT  
		Size: 3.4 MB (3379404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55d66e26ed51acf4d96c08bb777b841268e106a7712b3862519b5d7507d4f189`  
		Last Modified: Wed, 01 May 2024 21:52:30 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dfea2aafe084a180e61447e9634f8af46995faa9268477431f491e0992900b5`  
		Last Modified: Wed, 01 May 2024 21:52:30 GMT  
		Size: 293.8 KB (293822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8383b05439ec46b7769b3ef7dc46662e55bf3fb0a8eb297417b0adfa699bad0`  
		Last Modified: Wed, 01 May 2024 21:52:30 GMT  
		Size: 19.7 MB (19672445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1871e53f5f6a8dadc8ec00cdacdf391d6813188f7d1e7c48d8e04eabe2c8bf8`  
		Last Modified: Wed, 01 May 2024 21:52:30 GMT  
		Size: 12.2 KB (12237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57f6b0b2f314a14cdb1ff1d1017020a998e85536ae3036f7ea871eb13a855e56`  
		Last Modified: Wed, 01 May 2024 21:52:31 GMT  
		Size: 11.9 KB (11895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:211a27c77f3168981e3a035b6825b27928c14b6276e07bf6b4f02f809507684c`  
		Last Modified: Wed, 01 May 2024 21:52:31 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9.4-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:b946e43e28460ea7768378ffe6e8d682fed9033cfb1d326d36bb9daa843b59d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.0 KB (242020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74a6b4c0646fbf108e01db4f2ddeb6fa3e8e9c22d88902a6e75414c299a2c5d5`

```dockerfile
```

-	Layers:
	-	`sha256:ed8c4f682bfeb98432a8a8322036506db17c4b108b1fd3c1a3a2c4b411f24dc1`  
		Last Modified: Wed, 01 May 2024 21:52:30 GMT  
		Size: 225.2 KB (225210 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f2ff59fae389024bf949358e002424f80c60f2a4b5ee8c312f3c020d6fccaed`  
		Last Modified: Wed, 01 May 2024 21:52:29 GMT  
		Size: 16.8 KB (16810 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:alpine`

```console
$ docker pull chronograf@sha256:d11a629d4cfa1e0b9ca605f0719d5a9dc17add74c6fa2ed5f1901d2cb5c88be8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:bfdc2916cdf18901c104cbb5f9c37af0dcc9670c7da181038e306ff77d6cd169
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.6 MB (31589712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac8161dc609b83d7c07ff98e4828ced9b2e7f2ca0ff7144adade754fc64e7b28`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Fri, 26 Apr 2024 13:23:50 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
RUN apk add --no-cache ca-certificates su-exec &&     update-ca-certificates # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
ENV CHRONOGRAF_VERSION=1.10.4
# Fri, 26 Apr 2024 13:23:50 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S chronograf &&     adduser -S chronograf -G chronograf &&     mkdir -m 0750 -p /var/lib/chronograf &&     chown chronograf:chronograf /var/lib/chronograf # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 26 Apr 2024 13:23:50 GMT
VOLUME [/var/lib/chronograf]
# Fri, 26 Apr 2024 13:23:50 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Apr 2024 13:23:50 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d68e27f81705183aede5ec8d16b05af8c07d462f75e94160d798299e372f7a69`  
		Last Modified: Wed, 01 May 2024 21:52:22 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:310f07ece82e275ea4dc66a9a9033fdcdaf998fe6c7997781d299f934b8c039f`  
		Last Modified: Wed, 01 May 2024 21:52:22 GMT  
		Size: 295.8 KB (295755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df60bc3d01a0c01b095244792c5eb913e78e49a27aed12d0298bfeb99e8a5ae0`  
		Last Modified: Wed, 01 May 2024 21:52:23 GMT  
		Size: 27.9 MB (27866708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:809a3d10431465aa989b32320fcfa614917e4dd78b0ef3b4ba628af38b03e71c`  
		Last Modified: Wed, 01 May 2024 21:52:22 GMT  
		Size: 12.2 KB (12238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f26c5e66ed649fcbf21fdb6804855736c49214b33b70c57c236a56a02a0571a`  
		Last Modified: Wed, 01 May 2024 21:52:23 GMT  
		Size: 11.9 KB (11897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7cb52b403bfe177c53c218fda5245ba026945a8f393b97742e454946cf636a0`  
		Last Modified: Wed, 01 May 2024 21:52:23 GMT  
		Size: 292.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:d9169b4cb482ee5951ad4ecd2517a3d1409300a9dbb434cf060738a8755d0638
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.9 KB (248883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1186269e1898e56e2c477e1d1b6f8cdc68fa2be6a7ec7f5d9d857d8ac776419e`

```dockerfile
```

-	Layers:
	-	`sha256:f971f5ac4f8155c9092387ba6239303ff77b238f4abcfaaf23311628c0c78175`  
		Last Modified: Wed, 01 May 2024 21:52:22 GMT  
		Size: 231.1 KB (231128 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9504ad10dc79d5f0656c0ac6e2b5636b26abca0889311e5b247b31f93728d9cc`  
		Last Modified: Wed, 01 May 2024 21:52:22 GMT  
		Size: 17.8 KB (17755 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:latest`

```console
$ docker pull chronograf@sha256:f8576295bb2633b50b8f2b3c8cc683708e74282cf1a768da80f45b1124de5ee8
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
$ docker pull chronograf@sha256:2cb0b8b1da8690af36b9f7b4959bae0f25ba0a187424cac651b20650603445f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.1 MB (84060126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:277f0977dde354462ebac171186c995a845df807d021a0ac3ccdc47f42617d31`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:09 GMT
ADD file:4b1be1de1a1e5aa608c688cad2824587262081866180d7368feb79d33ca05953 in / 
# Wed, 24 Apr 2024 03:28:09 GMT
CMD ["bash"]
# Fri, 26 Apr 2024 13:23:50 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
ENV CHRONOGRAF_VERSION=1.10.4
# Fri, 26 Apr 2024 13:23:50 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 26 Apr 2024 13:23:50 GMT
VOLUME [/var/lib/chronograf]
# Fri, 26 Apr 2024 13:23:50 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Apr 2024 13:23:50 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:b0a0cf830b12453b7e15359a804215a7bcccd3788e2bcecff2a03af64bbd4df7`  
		Last Modified: Wed, 24 Apr 2024 03:32:41 GMT  
		Size: 29.2 MB (29150479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9bca853186d9fa4f3d07e24de79741fa25427f0b2d0eab8996be63473fd1c48`  
		Last Modified: Wed, 01 May 2024 21:52:27 GMT  
		Size: 7.7 MB (7676917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73cc39eb1df3ab70aa7dacba37e772033cd108cd90bdaa74e45011d6198634e2`  
		Last Modified: Wed, 01 May 2024 21:52:27 GMT  
		Size: 47.2 MB (47208254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2157983f1cb0f03e7a121bed8ff6e98027c8c6a3be7d161e4fe2b062522ec970`  
		Last Modified: Wed, 01 May 2024 21:52:26 GMT  
		Size: 12.3 KB (12251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f63d3959c98d650bf99c6413a0b9e85714a8cbcc9e7e258b319a70c5dbc23c3`  
		Last Modified: Wed, 01 May 2024 21:52:27 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4a815190e4fba0bf1463fe2293f2924dfdb71cff35211a1797c45aa66f62fb2`  
		Last Modified: Wed, 01 May 2024 21:52:27 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:1478d940f96dbaafe093d86241a298969ab344d11b536c0664e66d4e82608497
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2671561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f85b25a662f4291186189dd5d3dc33534aa1725e52dcc65c37f9b2766cd1d97`

```dockerfile
```

-	Layers:
	-	`sha256:f54b34b309e82a1681005dc1777c2b0f8604c1d314cb797cfbd1505b30897ba4`  
		Last Modified: Wed, 01 May 2024 21:52:26 GMT  
		Size: 2.7 MB (2655509 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2f8299d252d4df87db8af04601374b4348d6985c3594eb49c1877cdc524b51a`  
		Last Modified: Wed, 01 May 2024 21:52:26 GMT  
		Size: 16.1 KB (16052 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:latest` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:e7b87511934d274d44fdf7a810d210f8b2bebfedbca8c0de6128a5bda5f26532
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.3 MB (75340418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44445870df96cde21c7fd5b24ea74b673c0850e9e01577c1b168553f9cef8453`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 24 Apr 2024 04:07:05 GMT
ADD file:719e14b0eb733543ace336c71543b593f88e2b452e40fb315f5f6e49ebe6af58 in / 
# Wed, 24 Apr 2024 04:07:06 GMT
CMD ["bash"]
# Fri, 26 Apr 2024 13:23:50 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
ENV CHRONOGRAF_VERSION=1.10.4
# Fri, 26 Apr 2024 13:23:50 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 26 Apr 2024 13:23:50 GMT
VOLUME [/var/lib/chronograf]
# Fri, 26 Apr 2024 13:23:50 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Apr 2024 13:23:50 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:77e415c4e7c678efbc2cc774d4bc05f6f2de2a2e04959d7e324ce092026c650e`  
		Last Modified: Wed, 24 Apr 2024 04:11:13 GMT  
		Size: 24.7 MB (24740442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50316fbdc37f48b441d6a5300c3b2f5011fe5ff93920de46d8e37f26b19c1d0c`  
		Last Modified: Wed, 01 May 2024 22:09:40 GMT  
		Size: 6.3 MB (6301004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26e807757725f3d1ccaff9e57a0166983a73816ed082c8ef4173e057c9c61e87`  
		Last Modified: Wed, 01 May 2024 22:09:41 GMT  
		Size: 44.3 MB (44274487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42dfb47a244cadf0ec10ec3b5b8d475fb580dac07af32b9a27dbcde94f0c3cd4`  
		Last Modified: Wed, 01 May 2024 22:09:40 GMT  
		Size: 12.3 KB (12255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dff168616ff7f4d51eeab0e490b470d7be9bc49f74a5c75dd0769f58e6dd700d`  
		Last Modified: Wed, 01 May 2024 22:09:40 GMT  
		Size: 11.9 KB (11915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4e9b69be2b29851b3a218eeb456c72de15f9662b211438a21f396067cd6a4a9`  
		Last Modified: Wed, 01 May 2024 22:09:41 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:25dc80c7fe7448e89953320590af015f568304748c3b4855343d6e9792d63195
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2673765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc039a1ec77e176937bbd6406e7d5c07bd658a7893298e2a025947d0d09faef0`

```dockerfile
```

-	Layers:
	-	`sha256:b513cb3404b83faf32634e4946d2c0c5160a5001c8695d86ccfbb890a34cba61`  
		Last Modified: Wed, 01 May 2024 22:09:40 GMT  
		Size: 2.7 MB (2657805 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b6e8b8f908a14cafee41c6387f290c5241c3caf12fa4e5a54d1a9694dcf7efb`  
		Last Modified: Wed, 01 May 2024 22:09:40 GMT  
		Size: 16.0 KB (15960 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:latest` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:60a815700707f1df08df1029b83847eaa235f0e912a34fa6c253f12499024cf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.6 MB (81636840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5eaf05222cf53da43f8ef2282da0792a02048e92364dbcd68d586504103b4409`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:39 GMT
ADD file:ea7004fb788ab5cf1604d6e71153c48d99b75fbd1810e78a8c79faff11fe6771 in / 
# Wed, 24 Apr 2024 04:10:39 GMT
CMD ["bash"]
# Fri, 26 Apr 2024 13:23:50 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
ENV CHRONOGRAF_VERSION=1.10.4
# Fri, 26 Apr 2024 13:23:50 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 26 Apr 2024 13:23:50 GMT
VOLUME [/var/lib/chronograf]
# Fri, 26 Apr 2024 13:23:50 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Apr 2024 13:23:50 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:22d97f6a5d13532e867231d23d92620a81874d51a456196be50154eeb32edc08`  
		Last Modified: Wed, 24 Apr 2024 04:14:07 GMT  
		Size: 29.2 MB (29179935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afb2e161aae97649675931a79d1973b601f753dd3f37c4532530c72c07636d3d`  
		Last Modified: Wed, 01 May 2024 22:27:06 GMT  
		Size: 7.5 MB (7453129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1130d13b51f5f0ed17ab174e642adb1112bb78775d279ad3c199e0b61bd90b9b`  
		Last Modified: Wed, 01 May 2024 22:27:06 GMT  
		Size: 45.0 MB (44979293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac52f1d1a62121ca7fcfe7cc928aade001f7b7874c8bd7b40e7256c5e3ea6e1a`  
		Last Modified: Wed, 01 May 2024 22:27:04 GMT  
		Size: 12.3 KB (12254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:957a06817cfb183d334232ce4a1711d8735a39d983d25146bf657bf1f530254a`  
		Last Modified: Wed, 01 May 2024 22:27:05 GMT  
		Size: 11.9 KB (11914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b9bf80ee0ddb49a63ed6b1ca461f772f3c550d4d7c5615143ca62e3e21887ad`  
		Last Modified: Wed, 01 May 2024 22:27:05 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:f0e5abe681ea42d2efc7c7b8030e027274a57edf6ad0df5d93534ce2946ebdd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2671639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f479d33da2a64ac7a34333ed6adc29193bb65bee2a716d94a348e2858f84a85`

```dockerfile
```

-	Layers:
	-	`sha256:7c4fdc79c78dae83df78d9db456f5b419479096350f7ddb60685cc893a76a462`  
		Last Modified: Wed, 01 May 2024 22:27:04 GMT  
		Size: 2.7 MB (2655746 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:032a014ac7dc76467dddff4fd025e78a13e66d45993577bb48911db0c688e710`  
		Last Modified: Wed, 01 May 2024 22:27:04 GMT  
		Size: 15.9 KB (15893 bytes)  
		MIME: application/vnd.in-toto+json
