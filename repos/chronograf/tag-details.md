<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `chronograf`

-	[`chronograf:1.10`](#chronograf110)
-	[`chronograf:1.10-alpine`](#chronograf110-alpine)
-	[`chronograf:1.10.5`](#chronograf1105)
-	[`chronograf:1.10.5-alpine`](#chronograf1105-alpine)
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
$ docker pull chronograf@sha256:08114d9fb1640d6d8c011b7b08e1e12a78159495bc4e0c392bfaaedf0971f500
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
$ docker pull chronograf@sha256:370f05ad3d8c6b50fb3a4fdd7cbf9b1836210ad1881b2bb63062fb39b4575df8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.1 MB (84059979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78c17d60244565546a461f59d627296012f9949935d265eb2cd88bb8b8c88586`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 26 Apr 2024 13:23:50 GMT
ADD file:5aaace706aa00ff97d243daa2c29f5de88f124e1b97c570634f16eef90783286 in / 
# Fri, 26 Apr 2024 13:23:50 GMT
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
	-	`sha256:09f376ebb190216b0459f470e71bec7b5dfa611d66bf008492b40dcc5f1d8eae`  
		Last Modified: Tue, 14 May 2024 01:32:30 GMT  
		Size: 29.2 MB (29150411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dbd162c551db1cedcc5685816502236791c589c7a634dd5f4a867de19ba7f38`  
		Last Modified: Tue, 14 May 2024 02:55:56 GMT  
		Size: 7.7 MB (7676849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:218aa6196b269ed0201bb83377bf508d123413baac8c9f9b20e22560a398d2ed`  
		Last Modified: Tue, 14 May 2024 02:55:56 GMT  
		Size: 47.2 MB (47208256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85486ce5ee6e3bab219ecee2356577cc653be020cda927d247b35120485014af`  
		Last Modified: Tue, 14 May 2024 02:55:55 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9391b3eeeb7b2c88bdb336f2c8618e1db7b4c6502f2d731c0e1aac199022edeb`  
		Last Modified: Tue, 14 May 2024 02:55:56 GMT  
		Size: 11.9 KB (11903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16e5ab8b984ad49c5e7d53df9b3d1418832463f922b367e619cf6ba7470943f7`  
		Last Modified: Tue, 14 May 2024 02:55:56 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:c68b48e82ddc714d2e319db43d7d0af9c903d502fe305c99c0c4c4865d6c429e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2671560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0af4be7101b87554b824e4f7d0bcfc68fde9ac2d7e9bcb4d05c70240661b1aa0`

```dockerfile
```

-	Layers:
	-	`sha256:44f14bc5a63ccbd6ba7032dd6cf38f2675f82192e107423942403febb43c58de`  
		Last Modified: Tue, 14 May 2024 02:55:55 GMT  
		Size: 2.7 MB (2655509 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f27ff5c15c540e98d0f5c00ad5551d464faf790df6a47e177597215f7b044c21`  
		Last Modified: Tue, 14 May 2024 02:55:55 GMT  
		Size: 16.1 KB (16051 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.10` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:4454450565a10f9c0f92ad91a57f89bd2629b2d09a2c8bc623fcf54d8a041c65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.3 MB (75340138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfa6c3f0e7d9919e63d53c2f3a4f72859d9a728b1678a732c6ac061b0cde216c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 26 Apr 2024 13:23:50 GMT
ADD file:e170e8e24c36eb1a1a24d68a97cd2a7784d689387d804630dc7b596551d91090 in / 
# Fri, 26 Apr 2024 13:23:50 GMT
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
	-	`sha256:3b9aff019fd47145a0f08828c4c912b901596e71f6dbe2367a7a098e8882ef55`  
		Last Modified: Tue, 14 May 2024 01:12:45 GMT  
		Size: 24.7 MB (24740205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae78fd4d89254613f98aee5c6d8592017b8888f1320a37d7c18f7cdc0a5c8f73`  
		Last Modified: Tue, 14 May 2024 13:38:03 GMT  
		Size: 6.3 MB (6300974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d15bb3eff33edb829c42eea9980bfe1dd0c3c96d0cd372d42fb53ce2755a88c`  
		Last Modified: Tue, 14 May 2024 13:38:04 GMT  
		Size: 44.3 MB (44274487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdb37d02d8616fa2ccadead03979f62b9514cb22f7caaf6008a45ac2556fae54`  
		Last Modified: Tue, 14 May 2024 13:38:02 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b5009690c2b4e4806000a314b524ccf49938c4032adb91d11d9eb0ad5ea0c17`  
		Last Modified: Tue, 14 May 2024 13:38:03 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44e925b6e3859567a2a423d41903c0fafe4a3cfaab572aea1e37b859e51b0b91`  
		Last Modified: Tue, 14 May 2024 13:38:04 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:3fc203da88c6fbae57694bdafd0c0a222183011440b4ea2e66da46420711a8d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2673932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5549dd6aa6ffcf61935098be5152ecb588242641d0fbec8b22c8541087a6af48`

```dockerfile
```

-	Layers:
	-	`sha256:3a65d6278f8a0207f2b660bea4a844c1bb2d762d183450099f130ca81aa6eee1`  
		Last Modified: Tue, 14 May 2024 13:38:02 GMT  
		Size: 2.7 MB (2657805 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18adbf636c8b5f147322be8d3030a032e7856f58ece4113dbbd1dd589b5391d1`  
		Last Modified: Tue, 14 May 2024 13:38:02 GMT  
		Size: 16.1 KB (16127 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.10` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:90fe147a4a79fd98e190cda381c62a6d10dbd7ae1cf1ad03af24d4f99e95a2ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.6 MB (81636498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b041bd0bd9a505336c6ace981317292c30ce478d08e7c07438755f4cccb6183e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 26 Apr 2024 13:23:50 GMT
ADD file:e23ba17afc7850bcca9e73ba5022db9f0a80c6a0250585fd3f50a1960226474b in / 
# Fri, 26 Apr 2024 13:23:50 GMT
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
	-	`sha256:24c63b8dcb66721062f32b893ef1027404afddd62aade87f3f39a3a6e70a74d0`  
		Last Modified: Tue, 14 May 2024 00:42:56 GMT  
		Size: 29.2 MB (29179503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd20443421cd93c019fcbb19e74f1450e18b447aa335c1d318a95ea8018e4ed6`  
		Last Modified: Tue, 14 May 2024 16:44:06 GMT  
		Size: 7.5 MB (7453155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b11949ec29396c960299ec121197cfbe1d911787c6a85ba4ae70dc6e5c200dc9`  
		Last Modified: Tue, 14 May 2024 16:44:07 GMT  
		Size: 45.0 MB (44979366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfd3477973ab7deea1fbfe89506ee4a3ceb778b2eae3ed0bf9d4d65f9d7decce`  
		Last Modified: Tue, 14 May 2024 16:44:06 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2850d0e5e2a5f3e6e3a1a429148b603571d1bd284f3818f62cd75d64b4ddab7`  
		Last Modified: Tue, 14 May 2024 16:44:07 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af27fa30c08e0d5c7b3fb5e3e42a0720079744a5157ed7c9898d76a6627753ed`  
		Last Modified: Tue, 14 May 2024 16:44:07 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:f93b06732d31e7c269bc7aee726c6725c33892110ef0f4dae9b55fc745e9f8bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2671804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f82436f7353878d334e85eb452905f969a2251ecc6eba00f1fd6a406fb97a3b`

```dockerfile
```

-	Layers:
	-	`sha256:ab2112e396d32f67e01a848c132042a6b6ef97a122dee98f740d3da5492f7fc8`  
		Last Modified: Tue, 14 May 2024 16:44:06 GMT  
		Size: 2.7 MB (2655746 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71d84312bfff6cc1b324888756dc21ce74ef9ff8acd6d7069ea3ab255a7b8db6`  
		Last Modified: Tue, 14 May 2024 16:44:05 GMT  
		Size: 16.1 KB (16058 bytes)  
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

## `chronograf:1.10.5`

**does not exist** (yet?)

## `chronograf:1.10.5-alpine`

**does not exist** (yet?)

## `chronograf:1.7`

```console
$ docker pull chronograf@sha256:b5aa1a68a347627f2e3c9753dbc4bc043594cff78950f0c902f1c7165e27063a
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
$ docker pull chronograf@sha256:6c0323e3c4f48d061985c56b1e2e550615b009b2b09596e35d98e7cef090366c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.2 MB (70201769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdb26e21b8825a85f9292ac306255eb145ece54719cf03168d588779b712309c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 26 Apr 2024 13:23:50 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
# Fri, 26 Apr 2024 13:23:50 GMT
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
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86e68b080734523a87557ef9506077c627f030d9b5b10e4b257f7e62549174a8`  
		Last Modified: Tue, 14 May 2024 02:56:01 GMT  
		Size: 4.2 MB (4209340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f815e888a11a08990c3b8510d37641cbf1e9742d1c5bf2dc1ffe01df3e4459b`  
		Last Modified: Tue, 14 May 2024 02:56:02 GMT  
		Size: 34.5 MB (34534107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a5c4defb5bfb3c48cb8a155b97e40ea9fef0077a941db42af6f68e6e3d9649c`  
		Last Modified: Tue, 14 May 2024 02:56:00 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85a3324c53522596a82df3cab31581c4747b150409b34e50f5e23d90bb5f9b96`  
		Last Modified: Tue, 14 May 2024 02:56:00 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ff6b7d35e4a035c5d1b4f09748ca9dc79638b7e166bf69c40b3ee635685795`  
		Last Modified: Tue, 14 May 2024 02:56:01 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7` - unknown; unknown

```console
$ docker pull chronograf@sha256:610f87662aa307af100eab019d0214f62dee5e9cb70b361813b82ab0c69b82db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2882950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b0f6d30d9f1abfc81932cc35217d15f4103a61106a8e841239e71564c95beac`

```dockerfile
```

-	Layers:
	-	`sha256:8a1757da958952becf37aa001fb0ba137a551534377eb38dd37ea41d5e124a22`  
		Last Modified: Tue, 14 May 2024 02:56:00 GMT  
		Size: 2.9 MB (2867250 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec44cb4cf4caa41383b6cd6a7702adac08516ff960c776cf0e401e0fbeb915d5`  
		Last Modified: Tue, 14 May 2024 02:56:00 GMT  
		Size: 15.7 KB (15700 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.7` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:c8fec65e50f3b4a0923b8e6145669e38d6ce0e089c491c546ce7e4bbe6404caa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.0 MB (63024021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:192996997062ee6a4dd051043feda22b6337bfee059ce32807e7d624c96d4204`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 26 Apr 2024 13:23:50 GMT
ADD file:b58f353e9d2a24c2c16ae0913b28705d3ecc439d60d82b5b4982780c59aae249 in / 
# Fri, 26 Apr 2024 13:23:50 GMT
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
	-	`sha256:a5c0b9604ae49509a7875b258d98493d63bdb4c1c27a70f2befa5fa4fcea1888`  
		Last Modified: Tue, 14 May 2024 01:13:30 GMT  
		Size: 26.6 MB (26594493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38c4ecee3b185e32c5719e8fc7562b549a8a7febf9faaf3b9330740ceb42f5bd`  
		Last Modified: Tue, 14 May 2024 10:25:18 GMT  
		Size: 3.5 MB (3511533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb22c940a2b808e082d924a80531c9a375cfe5ac7258219a7e33180bc679db99`  
		Last Modified: Tue, 14 May 2024 10:25:19 GMT  
		Size: 32.9 MB (32893603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d8c10b93cf2c9ee2fcb4cbd6fbad7844616951a4dbde8d66e0c7a06efb5df86`  
		Last Modified: Tue, 14 May 2024 10:25:18 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4357851416710baeb871ae44aa8d78271e57df1a350acea5137861ff76a4ba25`  
		Last Modified: Tue, 14 May 2024 10:25:19 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a1327c103f3cd66fe95c52321d4c4e68ae91702ba9744bd579280c2f41e4127`  
		Last Modified: Tue, 14 May 2024 10:25:19 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7` - unknown; unknown

```console
$ docker pull chronograf@sha256:4cb02df38dbab5b9de1c767dfdea9e28232132c23511eab6ab09b8e2b71e707d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2885288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05f351c0a582eb3d3cb7d175a3774e0e5a22aafab6322296ffb09b0401d77cd2`

```dockerfile
```

-	Layers:
	-	`sha256:0a523a9b302e726d59a8070387260c694d1f00a060c40c94cfbb8bf3e76e2bc2`  
		Last Modified: Tue, 14 May 2024 10:25:18 GMT  
		Size: 2.9 MB (2869520 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c741903b151af6b170607d6b2f5c075f19ae3130536bfe1a4f0de3c327343165`  
		Last Modified: Tue, 14 May 2024 10:25:18 GMT  
		Size: 15.8 KB (15768 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.7` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:0043a6af89f339579793b4e5f30599f158e70d4325fb62cc8d0b578cca2903a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.4 MB (67355700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:389645b4093f4d1276c678678650062ed1817fb9859881491993d5477699b02e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 26 Apr 2024 13:23:50 GMT
ADD file:0465ea1f0e8a2ee3e0f770c3b7f8e4a2b8719c624b440cabe7d7ecbe87200e7b in / 
# Fri, 26 Apr 2024 13:23:50 GMT
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
	-	`sha256:3a0037c67e2f4632684ea787f751ddb0b6af2b86113ab3b6859744b6eaf77e2f`  
		Last Modified: Tue, 14 May 2024 00:43:33 GMT  
		Size: 30.1 MB (30086908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1360c3a858539593adda3e5aee79c57f0ec7de3d1102c1043ab0069e8b164fb9`  
		Last Modified: Tue, 14 May 2024 09:24:28 GMT  
		Size: 4.2 MB (4210530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8c9c171f9864d4054a0548bed42c4b0e8fa60a32691d7e84c47cf3d68d390ff`  
		Last Modified: Tue, 14 May 2024 09:24:29 GMT  
		Size: 33.0 MB (33033871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85290ede46b40988c030ebb5c4f66dc1d99cf130a894b62aa7c461ec3ee3e868`  
		Last Modified: Tue, 14 May 2024 09:24:27 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8b46f7625082ed186a4a99584606969eecce35b3fc9ed516807f8de73d532ba`  
		Last Modified: Tue, 14 May 2024 09:24:29 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e45d306c77b4970fc48dfb11be3a8ee382e7e525ad36b67b2d32586588657fd`  
		Last Modified: Tue, 14 May 2024 09:24:29 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7` - unknown; unknown

```console
$ docker pull chronograf@sha256:1516551c164a022d48ef857a68f580f2a92ead3e588448f0aff362417774f54b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2883180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24c9316dee3a5aad6f9a7add6037539ea202d085d60d00d99b706ab9da81ba6c`

```dockerfile
```

-	Layers:
	-	`sha256:218e217d48b749daaf5e6bd26e2406d4aa457fc8ae9456e31a301e445ebb0504`  
		Last Modified: Tue, 14 May 2024 09:24:28 GMT  
		Size: 2.9 MB (2867473 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b18a2071172d764aa2afad2cb716f453c8309be0e49d913b274f021a2176b17`  
		Last Modified: Tue, 14 May 2024 09:24:28 GMT  
		Size: 15.7 KB (15707 bytes)  
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
$ docker pull chronograf@sha256:b5aa1a68a347627f2e3c9753dbc4bc043594cff78950f0c902f1c7165e27063a
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
$ docker pull chronograf@sha256:6c0323e3c4f48d061985c56b1e2e550615b009b2b09596e35d98e7cef090366c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.2 MB (70201769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdb26e21b8825a85f9292ac306255eb145ece54719cf03168d588779b712309c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 26 Apr 2024 13:23:50 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
# Fri, 26 Apr 2024 13:23:50 GMT
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
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86e68b080734523a87557ef9506077c627f030d9b5b10e4b257f7e62549174a8`  
		Last Modified: Tue, 14 May 2024 02:56:01 GMT  
		Size: 4.2 MB (4209340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f815e888a11a08990c3b8510d37641cbf1e9742d1c5bf2dc1ffe01df3e4459b`  
		Last Modified: Tue, 14 May 2024 02:56:02 GMT  
		Size: 34.5 MB (34534107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a5c4defb5bfb3c48cb8a155b97e40ea9fef0077a941db42af6f68e6e3d9649c`  
		Last Modified: Tue, 14 May 2024 02:56:00 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85a3324c53522596a82df3cab31581c4747b150409b34e50f5e23d90bb5f9b96`  
		Last Modified: Tue, 14 May 2024 02:56:00 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ff6b7d35e4a035c5d1b4f09748ca9dc79638b7e166bf69c40b3ee635685795`  
		Last Modified: Tue, 14 May 2024 02:56:01 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7.17` - unknown; unknown

```console
$ docker pull chronograf@sha256:610f87662aa307af100eab019d0214f62dee5e9cb70b361813b82ab0c69b82db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2882950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b0f6d30d9f1abfc81932cc35217d15f4103a61106a8e841239e71564c95beac`

```dockerfile
```

-	Layers:
	-	`sha256:8a1757da958952becf37aa001fb0ba137a551534377eb38dd37ea41d5e124a22`  
		Last Modified: Tue, 14 May 2024 02:56:00 GMT  
		Size: 2.9 MB (2867250 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec44cb4cf4caa41383b6cd6a7702adac08516ff960c776cf0e401e0fbeb915d5`  
		Last Modified: Tue, 14 May 2024 02:56:00 GMT  
		Size: 15.7 KB (15700 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.7.17` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:c8fec65e50f3b4a0923b8e6145669e38d6ce0e089c491c546ce7e4bbe6404caa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.0 MB (63024021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:192996997062ee6a4dd051043feda22b6337bfee059ce32807e7d624c96d4204`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 26 Apr 2024 13:23:50 GMT
ADD file:b58f353e9d2a24c2c16ae0913b28705d3ecc439d60d82b5b4982780c59aae249 in / 
# Fri, 26 Apr 2024 13:23:50 GMT
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
	-	`sha256:a5c0b9604ae49509a7875b258d98493d63bdb4c1c27a70f2befa5fa4fcea1888`  
		Last Modified: Tue, 14 May 2024 01:13:30 GMT  
		Size: 26.6 MB (26594493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38c4ecee3b185e32c5719e8fc7562b549a8a7febf9faaf3b9330740ceb42f5bd`  
		Last Modified: Tue, 14 May 2024 10:25:18 GMT  
		Size: 3.5 MB (3511533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb22c940a2b808e082d924a80531c9a375cfe5ac7258219a7e33180bc679db99`  
		Last Modified: Tue, 14 May 2024 10:25:19 GMT  
		Size: 32.9 MB (32893603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d8c10b93cf2c9ee2fcb4cbd6fbad7844616951a4dbde8d66e0c7a06efb5df86`  
		Last Modified: Tue, 14 May 2024 10:25:18 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4357851416710baeb871ae44aa8d78271e57df1a350acea5137861ff76a4ba25`  
		Last Modified: Tue, 14 May 2024 10:25:19 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a1327c103f3cd66fe95c52321d4c4e68ae91702ba9744bd579280c2f41e4127`  
		Last Modified: Tue, 14 May 2024 10:25:19 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7.17` - unknown; unknown

```console
$ docker pull chronograf@sha256:4cb02df38dbab5b9de1c767dfdea9e28232132c23511eab6ab09b8e2b71e707d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2885288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05f351c0a582eb3d3cb7d175a3774e0e5a22aafab6322296ffb09b0401d77cd2`

```dockerfile
```

-	Layers:
	-	`sha256:0a523a9b302e726d59a8070387260c694d1f00a060c40c94cfbb8bf3e76e2bc2`  
		Last Modified: Tue, 14 May 2024 10:25:18 GMT  
		Size: 2.9 MB (2869520 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c741903b151af6b170607d6b2f5c075f19ae3130536bfe1a4f0de3c327343165`  
		Last Modified: Tue, 14 May 2024 10:25:18 GMT  
		Size: 15.8 KB (15768 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.7.17` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:0043a6af89f339579793b4e5f30599f158e70d4325fb62cc8d0b578cca2903a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.4 MB (67355700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:389645b4093f4d1276c678678650062ed1817fb9859881491993d5477699b02e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 26 Apr 2024 13:23:50 GMT
ADD file:0465ea1f0e8a2ee3e0f770c3b7f8e4a2b8719c624b440cabe7d7ecbe87200e7b in / 
# Fri, 26 Apr 2024 13:23:50 GMT
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
	-	`sha256:3a0037c67e2f4632684ea787f751ddb0b6af2b86113ab3b6859744b6eaf77e2f`  
		Last Modified: Tue, 14 May 2024 00:43:33 GMT  
		Size: 30.1 MB (30086908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1360c3a858539593adda3e5aee79c57f0ec7de3d1102c1043ab0069e8b164fb9`  
		Last Modified: Tue, 14 May 2024 09:24:28 GMT  
		Size: 4.2 MB (4210530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8c9c171f9864d4054a0548bed42c4b0e8fa60a32691d7e84c47cf3d68d390ff`  
		Last Modified: Tue, 14 May 2024 09:24:29 GMT  
		Size: 33.0 MB (33033871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85290ede46b40988c030ebb5c4f66dc1d99cf130a894b62aa7c461ec3ee3e868`  
		Last Modified: Tue, 14 May 2024 09:24:27 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8b46f7625082ed186a4a99584606969eecce35b3fc9ed516807f8de73d532ba`  
		Last Modified: Tue, 14 May 2024 09:24:29 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e45d306c77b4970fc48dfb11be3a8ee382e7e525ad36b67b2d32586588657fd`  
		Last Modified: Tue, 14 May 2024 09:24:29 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7.17` - unknown; unknown

```console
$ docker pull chronograf@sha256:1516551c164a022d48ef857a68f580f2a92ead3e588448f0aff362417774f54b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2883180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24c9316dee3a5aad6f9a7add6037539ea202d085d60d00d99b706ab9da81ba6c`

```dockerfile
```

-	Layers:
	-	`sha256:218e217d48b749daaf5e6bd26e2406d4aa457fc8ae9456e31a301e445ebb0504`  
		Last Modified: Tue, 14 May 2024 09:24:28 GMT  
		Size: 2.9 MB (2867473 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b18a2071172d764aa2afad2cb716f453c8309be0e49d913b274f021a2176b17`  
		Last Modified: Tue, 14 May 2024 09:24:28 GMT  
		Size: 15.7 KB (15707 bytes)  
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
$ docker pull chronograf@sha256:edee98fb23c5e9027f8022994fbceb1a4bad6d05098928733bc1ae6681d1ffe9
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
$ docker pull chronograf@sha256:329a93c02ac3c5ed0d9fcb0967ae3b43672168443734ca7f91b0af98497a1eea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.8 MB (70843253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53643e2719d577994865e97dc7c7d7e17e7bc205b2b803a8e18126985eb59575`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 26 Apr 2024 13:23:50 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
# Fri, 26 Apr 2024 13:23:50 GMT
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
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:328f1347dcd1e905807c6d5f21851b06c36198459d531852689a9d417f852562`  
		Last Modified: Tue, 14 May 2024 02:55:55 GMT  
		Size: 5.0 MB (5020956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d82e645923bb00aac44ddbf2722ebc1d72d808321dd860e7e877f15e2d0aefde`  
		Last Modified: Tue, 14 May 2024 02:55:56 GMT  
		Size: 34.4 MB (34363988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46b4c602c7c3c7eb2545198056893e61c4376c4d4e1817f66df145eb6339e5c4`  
		Last Modified: Tue, 14 May 2024 02:55:55 GMT  
		Size: 12.2 KB (12238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f50e4234545dbbc993c07944175e92f9ce0c3de15e666a1eb3d594df82f6b128`  
		Last Modified: Tue, 14 May 2024 02:55:56 GMT  
		Size: 11.9 KB (11901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6def16dddac4b9a7784599d3b30a8d89dc17d5c65327249c4b0920fe06941a4`  
		Last Modified: Tue, 14 May 2024 02:55:56 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8` - unknown; unknown

```console
$ docker pull chronograf@sha256:ce78d8cdfd28f61d43b6342d05b605f9d7a21ca6970e1136d9cf840c09762fd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2931059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b85cf43ef0a5a42f2f84f06a6b6717fdcb5daa4d00f05d9de740d2ef00e092db`

```dockerfile
```

-	Layers:
	-	`sha256:45fc8441532fc4dd9bf3545ffb508ddc018578b4d67e4dc485e76cd8d71540e5`  
		Last Modified: Tue, 14 May 2024 02:55:55 GMT  
		Size: 2.9 MB (2915319 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03f0bf4a4fa6094a9448a2316a90b4ae5af3a6424e5deca551dd69213211b707`  
		Last Modified: Tue, 14 May 2024 02:55:55 GMT  
		Size: 15.7 KB (15740 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.8` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:504914b8f530e583de7a012cb5982ad4d05764e9864b0d1fa202f38d84a882ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.4 MB (63439559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33e1ff672d9dbedcc3d03ff3b006495cb695d051f73595232a4985c049061cb1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 26 Apr 2024 13:23:50 GMT
ADD file:b58f353e9d2a24c2c16ae0913b28705d3ecc439d60d82b5b4982780c59aae249 in / 
# Fri, 26 Apr 2024 13:23:50 GMT
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
	-	`sha256:a5c0b9604ae49509a7875b258d98493d63bdb4c1c27a70f2befa5fa4fcea1888`  
		Last Modified: Tue, 14 May 2024 01:13:30 GMT  
		Size: 26.6 MB (26594493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38430fbb49bdb0ef13904d8f0d6cf6d5311baeb625f7f250e2056121896cd918`  
		Last Modified: Tue, 14 May 2024 13:29:45 GMT  
		Size: 4.3 MB (4285960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a61063faea5f788fe56400e8561a84c054e191d9cdcfb501a9ca77e975a247cf`  
		Last Modified: Tue, 14 May 2024 13:29:46 GMT  
		Size: 32.5 MB (32534709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bc073534bcc2f2b529b924ef2bcae5eed56b6d5a4053986f9d550e6a98b0b5c`  
		Last Modified: Tue, 14 May 2024 13:29:45 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12f0c191a2ab8622ae3647754937ee5bf9b48c6e9439062fe9a47a475ca5a27b`  
		Last Modified: Tue, 14 May 2024 13:29:45 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45e0d9f5aaa951ff81dc2d71a3ca23e3e770647f4b8dd11e5ada50aef58a1b55`  
		Last Modified: Tue, 14 May 2024 13:29:46 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8` - unknown; unknown

```console
$ docker pull chronograf@sha256:6595d8961a006fba048a5b50917aab85cc08811d11aa74a571ce1b7386e9bb70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2933230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5246e936c56bb219b7b00627c74a9feac02dbea40c44bc90a2d139674d54c5b`

```dockerfile
```

-	Layers:
	-	`sha256:b699fc6dfa92325dcfcc7e975c4d6e63a5bf26958d5cf85a605446e18ab834b4`  
		Last Modified: Tue, 14 May 2024 13:29:45 GMT  
		Size: 2.9 MB (2917589 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8017181ef9b0bc269dc7bb3e57afc4b3c77d5c49df9980394c9c80f43faf3685`  
		Last Modified: Tue, 14 May 2024 13:29:45 GMT  
		Size: 15.6 KB (15641 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.8` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:5c419fbb8cc8699bc0d8836fe19630f92f915a24eb7b482975d3733b057437e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.5 MB (67544791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ef29e03db4b03cff883a3da11d3b9fb16ec5b34cfeaf5595d044d38d5b30112`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 26 Apr 2024 13:23:50 GMT
ADD file:0465ea1f0e8a2ee3e0f770c3b7f8e4a2b8719c624b440cabe7d7ecbe87200e7b in / 
# Fri, 26 Apr 2024 13:23:50 GMT
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
	-	`sha256:3a0037c67e2f4632684ea787f751ddb0b6af2b86113ab3b6859744b6eaf77e2f`  
		Last Modified: Tue, 14 May 2024 00:43:33 GMT  
		Size: 30.1 MB (30086908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d90cfd1e8c7a3f7846a76ac12ac26faec1ea636632ce1a0ffb6ab8e2df399799`  
		Last Modified: Tue, 14 May 2024 15:54:56 GMT  
		Size: 5.0 MB (5004091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:326696275a5e02d62e526c6ac26fff417a724aef5694370992f1e3a5b9d8b1ff`  
		Last Modified: Tue, 14 May 2024 15:54:56 GMT  
		Size: 32.4 MB (32429407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35a69e4ed051ad39e7de4022ed4fe61496b49ab3fc3ad0934f32a6cc39d0ef7d`  
		Last Modified: Tue, 14 May 2024 15:54:55 GMT  
		Size: 12.2 KB (12241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71f52af9aef58aac835bfd39ee7286bcf7fe6dd7d976d9ea3dc9f6ab360e0f97`  
		Last Modified: Tue, 14 May 2024 15:54:55 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a65e68bcdf74990bb0f82f6bcf844b5303975e49a01f2e9e4c42a60d8056488a`  
		Last Modified: Tue, 14 May 2024 15:54:56 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8` - unknown; unknown

```console
$ docker pull chronograf@sha256:0965093c5ead1a052b1df4319ddf4ab3ca060198d8cefd410c854160719cb6d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2931122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b3206528adacbbcecfa67fa8c48273dc8f3acbd9148e9154232b5ec50c37555`

```dockerfile
```

-	Layers:
	-	`sha256:effe0462051c62119b7c3d280970bee765637fdb65fbc8b88b1e3d6a18c5c439`  
		Last Modified: Tue, 14 May 2024 15:54:56 GMT  
		Size: 2.9 MB (2915542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51effe8b869a5fbe2071237383e69fe53c802549257d50a1b108e008c8f9166a`  
		Last Modified: Tue, 14 May 2024 15:54:56 GMT  
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
$ docker pull chronograf@sha256:edee98fb23c5e9027f8022994fbceb1a4bad6d05098928733bc1ae6681d1ffe9
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
$ docker pull chronograf@sha256:329a93c02ac3c5ed0d9fcb0967ae3b43672168443734ca7f91b0af98497a1eea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.8 MB (70843253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53643e2719d577994865e97dc7c7d7e17e7bc205b2b803a8e18126985eb59575`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 26 Apr 2024 13:23:50 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
# Fri, 26 Apr 2024 13:23:50 GMT
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
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:328f1347dcd1e905807c6d5f21851b06c36198459d531852689a9d417f852562`  
		Last Modified: Tue, 14 May 2024 02:55:55 GMT  
		Size: 5.0 MB (5020956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d82e645923bb00aac44ddbf2722ebc1d72d808321dd860e7e877f15e2d0aefde`  
		Last Modified: Tue, 14 May 2024 02:55:56 GMT  
		Size: 34.4 MB (34363988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46b4c602c7c3c7eb2545198056893e61c4376c4d4e1817f66df145eb6339e5c4`  
		Last Modified: Tue, 14 May 2024 02:55:55 GMT  
		Size: 12.2 KB (12238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f50e4234545dbbc993c07944175e92f9ce0c3de15e666a1eb3d594df82f6b128`  
		Last Modified: Tue, 14 May 2024 02:55:56 GMT  
		Size: 11.9 KB (11901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6def16dddac4b9a7784599d3b30a8d89dc17d5c65327249c4b0920fe06941a4`  
		Last Modified: Tue, 14 May 2024 02:55:56 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:ce78d8cdfd28f61d43b6342d05b605f9d7a21ca6970e1136d9cf840c09762fd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2931059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b85cf43ef0a5a42f2f84f06a6b6717fdcb5daa4d00f05d9de740d2ef00e092db`

```dockerfile
```

-	Layers:
	-	`sha256:45fc8441532fc4dd9bf3545ffb508ddc018578b4d67e4dc485e76cd8d71540e5`  
		Last Modified: Tue, 14 May 2024 02:55:55 GMT  
		Size: 2.9 MB (2915319 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03f0bf4a4fa6094a9448a2316a90b4ae5af3a6424e5deca551dd69213211b707`  
		Last Modified: Tue, 14 May 2024 02:55:55 GMT  
		Size: 15.7 KB (15740 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.8.10` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:504914b8f530e583de7a012cb5982ad4d05764e9864b0d1fa202f38d84a882ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.4 MB (63439559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33e1ff672d9dbedcc3d03ff3b006495cb695d051f73595232a4985c049061cb1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 26 Apr 2024 13:23:50 GMT
ADD file:b58f353e9d2a24c2c16ae0913b28705d3ecc439d60d82b5b4982780c59aae249 in / 
# Fri, 26 Apr 2024 13:23:50 GMT
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
	-	`sha256:a5c0b9604ae49509a7875b258d98493d63bdb4c1c27a70f2befa5fa4fcea1888`  
		Last Modified: Tue, 14 May 2024 01:13:30 GMT  
		Size: 26.6 MB (26594493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38430fbb49bdb0ef13904d8f0d6cf6d5311baeb625f7f250e2056121896cd918`  
		Last Modified: Tue, 14 May 2024 13:29:45 GMT  
		Size: 4.3 MB (4285960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a61063faea5f788fe56400e8561a84c054e191d9cdcfb501a9ca77e975a247cf`  
		Last Modified: Tue, 14 May 2024 13:29:46 GMT  
		Size: 32.5 MB (32534709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bc073534bcc2f2b529b924ef2bcae5eed56b6d5a4053986f9d550e6a98b0b5c`  
		Last Modified: Tue, 14 May 2024 13:29:45 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12f0c191a2ab8622ae3647754937ee5bf9b48c6e9439062fe9a47a475ca5a27b`  
		Last Modified: Tue, 14 May 2024 13:29:45 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45e0d9f5aaa951ff81dc2d71a3ca23e3e770647f4b8dd11e5ada50aef58a1b55`  
		Last Modified: Tue, 14 May 2024 13:29:46 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:6595d8961a006fba048a5b50917aab85cc08811d11aa74a571ce1b7386e9bb70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2933230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5246e936c56bb219b7b00627c74a9feac02dbea40c44bc90a2d139674d54c5b`

```dockerfile
```

-	Layers:
	-	`sha256:b699fc6dfa92325dcfcc7e975c4d6e63a5bf26958d5cf85a605446e18ab834b4`  
		Last Modified: Tue, 14 May 2024 13:29:45 GMT  
		Size: 2.9 MB (2917589 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8017181ef9b0bc269dc7bb3e57afc4b3c77d5c49df9980394c9c80f43faf3685`  
		Last Modified: Tue, 14 May 2024 13:29:45 GMT  
		Size: 15.6 KB (15641 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.8.10` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:5c419fbb8cc8699bc0d8836fe19630f92f915a24eb7b482975d3733b057437e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.5 MB (67544791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ef29e03db4b03cff883a3da11d3b9fb16ec5b34cfeaf5595d044d38d5b30112`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 26 Apr 2024 13:23:50 GMT
ADD file:0465ea1f0e8a2ee3e0f770c3b7f8e4a2b8719c624b440cabe7d7ecbe87200e7b in / 
# Fri, 26 Apr 2024 13:23:50 GMT
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
	-	`sha256:3a0037c67e2f4632684ea787f751ddb0b6af2b86113ab3b6859744b6eaf77e2f`  
		Last Modified: Tue, 14 May 2024 00:43:33 GMT  
		Size: 30.1 MB (30086908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d90cfd1e8c7a3f7846a76ac12ac26faec1ea636632ce1a0ffb6ab8e2df399799`  
		Last Modified: Tue, 14 May 2024 15:54:56 GMT  
		Size: 5.0 MB (5004091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:326696275a5e02d62e526c6ac26fff417a724aef5694370992f1e3a5b9d8b1ff`  
		Last Modified: Tue, 14 May 2024 15:54:56 GMT  
		Size: 32.4 MB (32429407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35a69e4ed051ad39e7de4022ed4fe61496b49ab3fc3ad0934f32a6cc39d0ef7d`  
		Last Modified: Tue, 14 May 2024 15:54:55 GMT  
		Size: 12.2 KB (12241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71f52af9aef58aac835bfd39ee7286bcf7fe6dd7d976d9ea3dc9f6ab360e0f97`  
		Last Modified: Tue, 14 May 2024 15:54:55 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a65e68bcdf74990bb0f82f6bcf844b5303975e49a01f2e9e4c42a60d8056488a`  
		Last Modified: Tue, 14 May 2024 15:54:56 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:0965093c5ead1a052b1df4319ddf4ab3ca060198d8cefd410c854160719cb6d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2931122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b3206528adacbbcecfa67fa8c48273dc8f3acbd9148e9154232b5ec50c37555`

```dockerfile
```

-	Layers:
	-	`sha256:effe0462051c62119b7c3d280970bee765637fdb65fbc8b88b1e3d6a18c5c439`  
		Last Modified: Tue, 14 May 2024 15:54:56 GMT  
		Size: 2.9 MB (2915542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51effe8b869a5fbe2071237383e69fe53c802549257d50a1b108e008c8f9166a`  
		Last Modified: Tue, 14 May 2024 15:54:56 GMT  
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
$ docker pull chronograf@sha256:cd43ce91ecf53a49a90484c4aee2a152bd2f15b29ee192d31985c3d5b7505561
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
$ docker pull chronograf@sha256:f0372da93a7f11ad42e07c324e32e59b6283539787113ec538028f4fbe0c9e2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.5 MB (71490854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2313d52ef9798d9eac3c6e088f57b23e8fcad2f3efff2581b4f450cb4164ce98`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 26 Apr 2024 13:23:50 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
# Fri, 26 Apr 2024 13:23:50 GMT
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
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14560fc7f5782a98cb97c871c33bf22378c59f278de9251692820377258ed0c2`  
		Last Modified: Tue, 14 May 2024 02:55:59 GMT  
		Size: 5.0 MB (5020969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b329ffb9c332ed3749c7f19b261690ebfcfd46dacf6e77da6d4973a623a4a978`  
		Last Modified: Tue, 14 May 2024 02:56:00 GMT  
		Size: 35.0 MB (35011565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51049a47d01297bc29139fb0b0902aef200cff156cc3738234b02f94ebd9882d`  
		Last Modified: Tue, 14 May 2024 02:55:59 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67430ea6ab6ac578276b2c7db0ccaa05b0cc90da2ad8d63a92fd941a36cd94d5`  
		Last Modified: Tue, 14 May 2024 02:55:58 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac59ab093bea1f8921bc54d6eb8c5c75b7a9ea7fecde286793f79604d42ac31a`  
		Last Modified: Tue, 14 May 2024 02:56:00 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9` - unknown; unknown

```console
$ docker pull chronograf@sha256:af30aa0de42a55023f1cf5cc511eed94a725262078d079eebae7f26aa4be54da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2935341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e657d7939bbaf81bfbf4ab0bd732136e69d32c0aef188ebddb30c8b529fd813f`

```dockerfile
```

-	Layers:
	-	`sha256:819544a8bd1a9ec8f816fbb437d8e6b75f078957a3872c5bcc8ac12b79d76a4a`  
		Last Modified: Tue, 14 May 2024 02:55:59 GMT  
		Size: 2.9 MB (2919609 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f87d5d83972f432ba89572aa01b0b87c55342749b75ae567c4a9e1ab504367bb`  
		Last Modified: Tue, 14 May 2024 02:55:58 GMT  
		Size: 15.7 KB (15732 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.9` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:4fc81486074881f6e48bed1fe2865b12f56bb0c26cdd3c977a618acc6ee45316
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.2 MB (64216216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89b10a5429230b23763296559f1cb575d9dacff6339e9f6cf1d7cd37c6a0d2fc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 26 Apr 2024 13:23:50 GMT
ADD file:b58f353e9d2a24c2c16ae0913b28705d3ecc439d60d82b5b4982780c59aae249 in / 
# Fri, 26 Apr 2024 13:23:50 GMT
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
	-	`sha256:a5c0b9604ae49509a7875b258d98493d63bdb4c1c27a70f2befa5fa4fcea1888`  
		Last Modified: Tue, 14 May 2024 01:13:30 GMT  
		Size: 26.6 MB (26594493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38430fbb49bdb0ef13904d8f0d6cf6d5311baeb625f7f250e2056121896cd918`  
		Last Modified: Tue, 14 May 2024 13:29:45 GMT  
		Size: 4.3 MB (4285960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80e0f273e1c86795f6a5dca34f487b51793f59600f8c1dfb9e3420ef4cf52c7e`  
		Last Modified: Tue, 14 May 2024 13:37:04 GMT  
		Size: 33.3 MB (33311372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba54ede2cbfac8974265a98f9fc817373cdfae0337733c3f796d650562966694`  
		Last Modified: Tue, 14 May 2024 13:37:02 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d559e1274f7d7fb6efaf5aef9f4e273ea32f1f979130dfd514f3967af6164be`  
		Last Modified: Tue, 14 May 2024 13:37:02 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63aa0b01541ece3cfd8c95ce4c859b646da85cab56fd93787707db178cffdc4c`  
		Last Modified: Tue, 14 May 2024 13:37:03 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9` - unknown; unknown

```console
$ docker pull chronograf@sha256:dcb239ee1ac48b6ac47b5289c1a6f93b04f8c5c6cd55d991cac4a73688089466
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2937513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f0cc7a2bb703daf7503c3487769d4c5df1511f44b6a47c51812c3ac2e5a8bbd`

```dockerfile
```

-	Layers:
	-	`sha256:377a5ed75977b81f376bb8c113f2de50ecbb5277ffcf97680c8b221303264c45`  
		Last Modified: Tue, 14 May 2024 13:37:02 GMT  
		Size: 2.9 MB (2921879 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4fcb07ac15c20b00f498807eee8a233cedb202cee1ed760f45090fce72536db`  
		Last Modified: Tue, 14 May 2024 13:37:02 GMT  
		Size: 15.6 KB (15634 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.9` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:dfb95177ea0e1ce9d2f078f0fb49facc66a48d7eb83e73cb44e702dfd3a93d5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.3 MB (68296887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5968e71a858767ca10f5bd1fead506500155e6ad42998c127589c2dd1a8eab2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 26 Apr 2024 13:23:50 GMT
ADD file:0465ea1f0e8a2ee3e0f770c3b7f8e4a2b8719c624b440cabe7d7ecbe87200e7b in / 
# Fri, 26 Apr 2024 13:23:50 GMT
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
	-	`sha256:3a0037c67e2f4632684ea787f751ddb0b6af2b86113ab3b6859744b6eaf77e2f`  
		Last Modified: Tue, 14 May 2024 00:43:33 GMT  
		Size: 30.1 MB (30086908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d90cfd1e8c7a3f7846a76ac12ac26faec1ea636632ce1a0ffb6ab8e2df399799`  
		Last Modified: Tue, 14 May 2024 15:54:56 GMT  
		Size: 5.0 MB (5004091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dee2d8ccada3c8d10ec741e8193b9f329681040c36075ad0444bfce0cc902219`  
		Last Modified: Tue, 14 May 2024 16:22:42 GMT  
		Size: 33.2 MB (33181498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4464afbaf628ecf3c39bb28810d455ace830d6ec809e82bffe99becd150e3da3`  
		Last Modified: Tue, 14 May 2024 16:22:41 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c46bd61a1b08bb81e3f6343552d518609e613484667726cc254778b755e3ce73`  
		Last Modified: Tue, 14 May 2024 16:22:42 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:557cfb250db6cc3f125c48bf17386b83e3d1b7022c0bdb6b877f68e553674b5c`  
		Last Modified: Tue, 14 May 2024 16:22:42 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9` - unknown; unknown

```console
$ docker pull chronograf@sha256:363a1414daa451be02f87e51e11572d0cb3cf0f0e3f3c32caaa8f5abd0b15ac5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2935405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27abf893d9d37c3518416c99e74f21383d93fc5ba14281918205024ee70cfe8f`

```dockerfile
```

-	Layers:
	-	`sha256:331ec1eac6491a95eb7f8a6cc268418149e175e8813d2c968598d4ddb8eea6a7`  
		Last Modified: Tue, 14 May 2024 16:22:41 GMT  
		Size: 2.9 MB (2919832 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba50cb56cb5838154cad3b8703f3283f5603d0abc97e67ba7b5e1cf43bfd93a2`  
		Last Modified: Tue, 14 May 2024 16:22:41 GMT  
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
$ docker pull chronograf@sha256:cd43ce91ecf53a49a90484c4aee2a152bd2f15b29ee192d31985c3d5b7505561
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
$ docker pull chronograf@sha256:f0372da93a7f11ad42e07c324e32e59b6283539787113ec538028f4fbe0c9e2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.5 MB (71490854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2313d52ef9798d9eac3c6e088f57b23e8fcad2f3efff2581b4f450cb4164ce98`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 26 Apr 2024 13:23:50 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
# Fri, 26 Apr 2024 13:23:50 GMT
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
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14560fc7f5782a98cb97c871c33bf22378c59f278de9251692820377258ed0c2`  
		Last Modified: Tue, 14 May 2024 02:55:59 GMT  
		Size: 5.0 MB (5020969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b329ffb9c332ed3749c7f19b261690ebfcfd46dacf6e77da6d4973a623a4a978`  
		Last Modified: Tue, 14 May 2024 02:56:00 GMT  
		Size: 35.0 MB (35011565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51049a47d01297bc29139fb0b0902aef200cff156cc3738234b02f94ebd9882d`  
		Last Modified: Tue, 14 May 2024 02:55:59 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67430ea6ab6ac578276b2c7db0ccaa05b0cc90da2ad8d63a92fd941a36cd94d5`  
		Last Modified: Tue, 14 May 2024 02:55:58 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac59ab093bea1f8921bc54d6eb8c5c75b7a9ea7fecde286793f79604d42ac31a`  
		Last Modified: Tue, 14 May 2024 02:56:00 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9.4` - unknown; unknown

```console
$ docker pull chronograf@sha256:af30aa0de42a55023f1cf5cc511eed94a725262078d079eebae7f26aa4be54da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2935341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e657d7939bbaf81bfbf4ab0bd732136e69d32c0aef188ebddb30c8b529fd813f`

```dockerfile
```

-	Layers:
	-	`sha256:819544a8bd1a9ec8f816fbb437d8e6b75f078957a3872c5bcc8ac12b79d76a4a`  
		Last Modified: Tue, 14 May 2024 02:55:59 GMT  
		Size: 2.9 MB (2919609 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f87d5d83972f432ba89572aa01b0b87c55342749b75ae567c4a9e1ab504367bb`  
		Last Modified: Tue, 14 May 2024 02:55:58 GMT  
		Size: 15.7 KB (15732 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.9.4` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:4fc81486074881f6e48bed1fe2865b12f56bb0c26cdd3c977a618acc6ee45316
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.2 MB (64216216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89b10a5429230b23763296559f1cb575d9dacff6339e9f6cf1d7cd37c6a0d2fc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 26 Apr 2024 13:23:50 GMT
ADD file:b58f353e9d2a24c2c16ae0913b28705d3ecc439d60d82b5b4982780c59aae249 in / 
# Fri, 26 Apr 2024 13:23:50 GMT
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
	-	`sha256:a5c0b9604ae49509a7875b258d98493d63bdb4c1c27a70f2befa5fa4fcea1888`  
		Last Modified: Tue, 14 May 2024 01:13:30 GMT  
		Size: 26.6 MB (26594493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38430fbb49bdb0ef13904d8f0d6cf6d5311baeb625f7f250e2056121896cd918`  
		Last Modified: Tue, 14 May 2024 13:29:45 GMT  
		Size: 4.3 MB (4285960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80e0f273e1c86795f6a5dca34f487b51793f59600f8c1dfb9e3420ef4cf52c7e`  
		Last Modified: Tue, 14 May 2024 13:37:04 GMT  
		Size: 33.3 MB (33311372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba54ede2cbfac8974265a98f9fc817373cdfae0337733c3f796d650562966694`  
		Last Modified: Tue, 14 May 2024 13:37:02 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d559e1274f7d7fb6efaf5aef9f4e273ea32f1f979130dfd514f3967af6164be`  
		Last Modified: Tue, 14 May 2024 13:37:02 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63aa0b01541ece3cfd8c95ce4c859b646da85cab56fd93787707db178cffdc4c`  
		Last Modified: Tue, 14 May 2024 13:37:03 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9.4` - unknown; unknown

```console
$ docker pull chronograf@sha256:dcb239ee1ac48b6ac47b5289c1a6f93b04f8c5c6cd55d991cac4a73688089466
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2937513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f0cc7a2bb703daf7503c3487769d4c5df1511f44b6a47c51812c3ac2e5a8bbd`

```dockerfile
```

-	Layers:
	-	`sha256:377a5ed75977b81f376bb8c113f2de50ecbb5277ffcf97680c8b221303264c45`  
		Last Modified: Tue, 14 May 2024 13:37:02 GMT  
		Size: 2.9 MB (2921879 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4fcb07ac15c20b00f498807eee8a233cedb202cee1ed760f45090fce72536db`  
		Last Modified: Tue, 14 May 2024 13:37:02 GMT  
		Size: 15.6 KB (15634 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.9.4` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:dfb95177ea0e1ce9d2f078f0fb49facc66a48d7eb83e73cb44e702dfd3a93d5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.3 MB (68296887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5968e71a858767ca10f5bd1fead506500155e6ad42998c127589c2dd1a8eab2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 26 Apr 2024 13:23:50 GMT
ADD file:0465ea1f0e8a2ee3e0f770c3b7f8e4a2b8719c624b440cabe7d7ecbe87200e7b in / 
# Fri, 26 Apr 2024 13:23:50 GMT
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
	-	`sha256:3a0037c67e2f4632684ea787f751ddb0b6af2b86113ab3b6859744b6eaf77e2f`  
		Last Modified: Tue, 14 May 2024 00:43:33 GMT  
		Size: 30.1 MB (30086908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d90cfd1e8c7a3f7846a76ac12ac26faec1ea636632ce1a0ffb6ab8e2df399799`  
		Last Modified: Tue, 14 May 2024 15:54:56 GMT  
		Size: 5.0 MB (5004091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dee2d8ccada3c8d10ec741e8193b9f329681040c36075ad0444bfce0cc902219`  
		Last Modified: Tue, 14 May 2024 16:22:42 GMT  
		Size: 33.2 MB (33181498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4464afbaf628ecf3c39bb28810d455ace830d6ec809e82bffe99becd150e3da3`  
		Last Modified: Tue, 14 May 2024 16:22:41 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c46bd61a1b08bb81e3f6343552d518609e613484667726cc254778b755e3ce73`  
		Last Modified: Tue, 14 May 2024 16:22:42 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:557cfb250db6cc3f125c48bf17386b83e3d1b7022c0bdb6b877f68e553674b5c`  
		Last Modified: Tue, 14 May 2024 16:22:42 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9.4` - unknown; unknown

```console
$ docker pull chronograf@sha256:363a1414daa451be02f87e51e11572d0cb3cf0f0e3f3c32caaa8f5abd0b15ac5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2935405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27abf893d9d37c3518416c99e74f21383d93fc5ba14281918205024ee70cfe8f`

```dockerfile
```

-	Layers:
	-	`sha256:331ec1eac6491a95eb7f8a6cc268418149e175e8813d2c968598d4ddb8eea6a7`  
		Last Modified: Tue, 14 May 2024 16:22:41 GMT  
		Size: 2.9 MB (2919832 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba50cb56cb5838154cad3b8703f3283f5603d0abc97e67ba7b5e1cf43bfd93a2`  
		Last Modified: Tue, 14 May 2024 16:22:41 GMT  
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
$ docker pull chronograf@sha256:08114d9fb1640d6d8c011b7b08e1e12a78159495bc4e0c392bfaaedf0971f500
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
$ docker pull chronograf@sha256:370f05ad3d8c6b50fb3a4fdd7cbf9b1836210ad1881b2bb63062fb39b4575df8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.1 MB (84059979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78c17d60244565546a461f59d627296012f9949935d265eb2cd88bb8b8c88586`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 26 Apr 2024 13:23:50 GMT
ADD file:5aaace706aa00ff97d243daa2c29f5de88f124e1b97c570634f16eef90783286 in / 
# Fri, 26 Apr 2024 13:23:50 GMT
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
	-	`sha256:09f376ebb190216b0459f470e71bec7b5dfa611d66bf008492b40dcc5f1d8eae`  
		Last Modified: Tue, 14 May 2024 01:32:30 GMT  
		Size: 29.2 MB (29150411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dbd162c551db1cedcc5685816502236791c589c7a634dd5f4a867de19ba7f38`  
		Last Modified: Tue, 14 May 2024 02:55:56 GMT  
		Size: 7.7 MB (7676849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:218aa6196b269ed0201bb83377bf508d123413baac8c9f9b20e22560a398d2ed`  
		Last Modified: Tue, 14 May 2024 02:55:56 GMT  
		Size: 47.2 MB (47208256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85486ce5ee6e3bab219ecee2356577cc653be020cda927d247b35120485014af`  
		Last Modified: Tue, 14 May 2024 02:55:55 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9391b3eeeb7b2c88bdb336f2c8618e1db7b4c6502f2d731c0e1aac199022edeb`  
		Last Modified: Tue, 14 May 2024 02:55:56 GMT  
		Size: 11.9 KB (11903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16e5ab8b984ad49c5e7d53df9b3d1418832463f922b367e619cf6ba7470943f7`  
		Last Modified: Tue, 14 May 2024 02:55:56 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:c68b48e82ddc714d2e319db43d7d0af9c903d502fe305c99c0c4c4865d6c429e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2671560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0af4be7101b87554b824e4f7d0bcfc68fde9ac2d7e9bcb4d05c70240661b1aa0`

```dockerfile
```

-	Layers:
	-	`sha256:44f14bc5a63ccbd6ba7032dd6cf38f2675f82192e107423942403febb43c58de`  
		Last Modified: Tue, 14 May 2024 02:55:55 GMT  
		Size: 2.7 MB (2655509 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f27ff5c15c540e98d0f5c00ad5551d464faf790df6a47e177597215f7b044c21`  
		Last Modified: Tue, 14 May 2024 02:55:55 GMT  
		Size: 16.1 KB (16051 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:latest` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:4454450565a10f9c0f92ad91a57f89bd2629b2d09a2c8bc623fcf54d8a041c65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.3 MB (75340138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfa6c3f0e7d9919e63d53c2f3a4f72859d9a728b1678a732c6ac061b0cde216c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 26 Apr 2024 13:23:50 GMT
ADD file:e170e8e24c36eb1a1a24d68a97cd2a7784d689387d804630dc7b596551d91090 in / 
# Fri, 26 Apr 2024 13:23:50 GMT
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
	-	`sha256:3b9aff019fd47145a0f08828c4c912b901596e71f6dbe2367a7a098e8882ef55`  
		Last Modified: Tue, 14 May 2024 01:12:45 GMT  
		Size: 24.7 MB (24740205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae78fd4d89254613f98aee5c6d8592017b8888f1320a37d7c18f7cdc0a5c8f73`  
		Last Modified: Tue, 14 May 2024 13:38:03 GMT  
		Size: 6.3 MB (6300974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d15bb3eff33edb829c42eea9980bfe1dd0c3c96d0cd372d42fb53ce2755a88c`  
		Last Modified: Tue, 14 May 2024 13:38:04 GMT  
		Size: 44.3 MB (44274487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdb37d02d8616fa2ccadead03979f62b9514cb22f7caaf6008a45ac2556fae54`  
		Last Modified: Tue, 14 May 2024 13:38:02 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b5009690c2b4e4806000a314b524ccf49938c4032adb91d11d9eb0ad5ea0c17`  
		Last Modified: Tue, 14 May 2024 13:38:03 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44e925b6e3859567a2a423d41903c0fafe4a3cfaab572aea1e37b859e51b0b91`  
		Last Modified: Tue, 14 May 2024 13:38:04 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:3fc203da88c6fbae57694bdafd0c0a222183011440b4ea2e66da46420711a8d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2673932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5549dd6aa6ffcf61935098be5152ecb588242641d0fbec8b22c8541087a6af48`

```dockerfile
```

-	Layers:
	-	`sha256:3a65d6278f8a0207f2b660bea4a844c1bb2d762d183450099f130ca81aa6eee1`  
		Last Modified: Tue, 14 May 2024 13:38:02 GMT  
		Size: 2.7 MB (2657805 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18adbf636c8b5f147322be8d3030a032e7856f58ece4113dbbd1dd589b5391d1`  
		Last Modified: Tue, 14 May 2024 13:38:02 GMT  
		Size: 16.1 KB (16127 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:latest` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:90fe147a4a79fd98e190cda381c62a6d10dbd7ae1cf1ad03af24d4f99e95a2ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.6 MB (81636498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b041bd0bd9a505336c6ace981317292c30ce478d08e7c07438755f4cccb6183e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 26 Apr 2024 13:23:50 GMT
ADD file:e23ba17afc7850bcca9e73ba5022db9f0a80c6a0250585fd3f50a1960226474b in / 
# Fri, 26 Apr 2024 13:23:50 GMT
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
	-	`sha256:24c63b8dcb66721062f32b893ef1027404afddd62aade87f3f39a3a6e70a74d0`  
		Last Modified: Tue, 14 May 2024 00:42:56 GMT  
		Size: 29.2 MB (29179503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd20443421cd93c019fcbb19e74f1450e18b447aa335c1d318a95ea8018e4ed6`  
		Last Modified: Tue, 14 May 2024 16:44:06 GMT  
		Size: 7.5 MB (7453155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b11949ec29396c960299ec121197cfbe1d911787c6a85ba4ae70dc6e5c200dc9`  
		Last Modified: Tue, 14 May 2024 16:44:07 GMT  
		Size: 45.0 MB (44979366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfd3477973ab7deea1fbfe89506ee4a3ceb778b2eae3ed0bf9d4d65f9d7decce`  
		Last Modified: Tue, 14 May 2024 16:44:06 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2850d0e5e2a5f3e6e3a1a429148b603571d1bd284f3818f62cd75d64b4ddab7`  
		Last Modified: Tue, 14 May 2024 16:44:07 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af27fa30c08e0d5c7b3fb5e3e42a0720079744a5157ed7c9898d76a6627753ed`  
		Last Modified: Tue, 14 May 2024 16:44:07 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:f93b06732d31e7c269bc7aee726c6725c33892110ef0f4dae9b55fc745e9f8bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2671804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f82436f7353878d334e85eb452905f969a2251ecc6eba00f1fd6a406fb97a3b`

```dockerfile
```

-	Layers:
	-	`sha256:ab2112e396d32f67e01a848c132042a6b6ef97a122dee98f740d3da5492f7fc8`  
		Last Modified: Tue, 14 May 2024 16:44:06 GMT  
		Size: 2.7 MB (2655746 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71d84312bfff6cc1b324888756dc21ce74ef9ff8acd6d7069ea3ab255a7b8db6`  
		Last Modified: Tue, 14 May 2024 16:44:05 GMT  
		Size: 16.1 KB (16058 bytes)  
		MIME: application/vnd.in-toto+json
