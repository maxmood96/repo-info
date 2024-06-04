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
$ docker pull chronograf@sha256:cf6bab04e7f150c1ecae89c8e94de6873be3b146e71803d992ac46ad73cf0c5a
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
$ docker pull chronograf@sha256:5f5537b449b3f8035637e4ce9eb6d4720ced46f8db9d4e2c13c95be6f1ac7be9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.1 MB (84069434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45996034df2c6fe446e5e2fd0aa29d585534c107ab461bba710b9e9e2a59446d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 14 May 2024 01:28:03 GMT
ADD file:5aaace706aa00ff97d243daa2c29f5de88f124e1b97c570634f16eef90783286 in / 
# Tue, 14 May 2024 01:28:04 GMT
CMD ["bash"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.10.5
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:09f376ebb190216b0459f470e71bec7b5dfa611d66bf008492b40dcc5f1d8eae`  
		Last Modified: Tue, 14 May 2024 01:32:30 GMT  
		Size: 29.2 MB (29150411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8f47b768815e9c2366c46a8534a57f09e4f6f0ff4b0b52b64ba601dc9a9c174`  
		Last Modified: Mon, 03 Jun 2024 19:00:29 GMT  
		Size: 7.7 MB (7676940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9489fbf683135fcfa140c8d0a17e9d550c173fc3a052bc84f9f267f99252cf48`  
		Last Modified: Mon, 03 Jun 2024 19:00:31 GMT  
		Size: 47.2 MB (47217627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ed019f6b0534dfea3bfb7a969d8574f9df636506f6f19524b92326e37d2ada2`  
		Last Modified: Mon, 03 Jun 2024 19:00:28 GMT  
		Size: 12.2 KB (12241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb7ab6f5f28a95f1a3f7d8c842fdfc39c48d986d7d2fc301067f3717612a58d4`  
		Last Modified: Mon, 03 Jun 2024 19:00:28 GMT  
		Size: 11.9 KB (11900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af934b4bf874818dedfe49e86bee37a24e98cfb0e261bef354508666419f1249`  
		Last Modified: Mon, 03 Jun 2024 19:00:30 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:c109af0e26df5eea8f474e65c0139dbb1f2441db69a8534d6e4d0c20f1eebaa6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2671399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d7cf432a9a5718d9f6b2250ab83415c141962d8a0deb4e8a169e459aff78d57`

```dockerfile
```

-	Layers:
	-	`sha256:c3d8929c831b697a62dc9682fd7ae7044d6cd8342004667d41fd27a573432ef3`  
		Last Modified: Mon, 03 Jun 2024 19:00:29 GMT  
		Size: 2.7 MB (2655514 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3661947447bdb2d0b40fbad7fa348a99abb8e7e835a3351efddc4c57262a0019`  
		Last Modified: Mon, 03 Jun 2024 19:00:28 GMT  
		Size: 15.9 KB (15885 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.10` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:1a460b0bc194e24766aea7533b5cb8d0b916e7f6a09f4ef955743cbbb2a3d430
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.3 MB (75343302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fd2dc826fb7082fc62609abbeac1458117fce816a079a2e66b02f714e7625b3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 14 May 2024 01:08:45 GMT
ADD file:e170e8e24c36eb1a1a24d68a97cd2a7784d689387d804630dc7b596551d91090 in / 
# Tue, 14 May 2024 01:08:45 GMT
CMD ["bash"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.10.5
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:3b9aff019fd47145a0f08828c4c912b901596e71f6dbe2367a7a098e8882ef55`  
		Last Modified: Tue, 14 May 2024 01:12:45 GMT  
		Size: 24.7 MB (24740205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8351e2a7bec99074c9b2552b2d42aabba4fff0d39db3d0ba9b68a404136d1453`  
		Last Modified: Mon, 03 Jun 2024 19:21:37 GMT  
		Size: 6.3 MB (6301009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ecd35a42c7fd3bb3846a30c6d03f105a7b0004871c712048da35ad37776b89a`  
		Last Modified: Mon, 03 Jun 2024 19:21:38 GMT  
		Size: 44.3 MB (44277619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c6834d5d76602cbf35137f057e581f58279ed2341c8d70ea3c43059d1e869aa`  
		Last Modified: Mon, 03 Jun 2024 19:21:37 GMT  
		Size: 12.2 KB (12244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a1ff0b1eeee3067ebbfb12a9699f51e68c235bba7025e052f468ff25d8a0a8e`  
		Last Modified: Mon, 03 Jun 2024 19:21:37 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c88710b32ff5bef236a642c6ffa7546c65aafb1a9703ec9aa5584b140c831f8e`  
		Last Modified: Mon, 03 Jun 2024 19:21:38 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:80c599174d5b9b187f9c7428801ab128e6596094361cbaf40235d64ed9cb9168
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2673769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9a7de8a8b42ee3697139c5dc16ce57f52de462a641be9a93075c7416c83c588`

```dockerfile
```

-	Layers:
	-	`sha256:912fd66c49cdd7f7ba8e22dc0f03fa2098c87be72f0f8e38c2d13d2dea925230`  
		Last Modified: Mon, 03 Jun 2024 19:21:37 GMT  
		Size: 2.7 MB (2657810 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de523748666f12dea6e03853effe8f169d72dbd26d1ddcb7bb613ac802d32c6b`  
		Last Modified: Mon, 03 Jun 2024 19:21:37 GMT  
		Size: 16.0 KB (15959 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.10` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:56fc9a7d7b5e4129e88ff15e6e3f443c62536180fba87c675a42fce7c1e2a205
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.6 MB (81628060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06be28a02b74fac1638579f669127787c0ed3809f3587e6af1cf9b7761558b79`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 14 May 2024 00:39:40 GMT
ADD file:e23ba17afc7850bcca9e73ba5022db9f0a80c6a0250585fd3f50a1960226474b in / 
# Tue, 14 May 2024 00:39:41 GMT
CMD ["bash"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.10.5
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:24c63b8dcb66721062f32b893ef1027404afddd62aade87f3f39a3a6e70a74d0`  
		Last Modified: Tue, 14 May 2024 00:42:56 GMT  
		Size: 29.2 MB (29179503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d41ef92593599be99b703585f08f0f9d449d437aa1a40c01770b9496e36d09aa`  
		Last Modified: Tue, 04 Jun 2024 00:30:46 GMT  
		Size: 7.5 MB (7453158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:242a93b9d52597004cac704e713b2296dc4c9e12747f37ef26bfc754a8185575`  
		Last Modified: Tue, 04 Jun 2024 00:30:47 GMT  
		Size: 45.0 MB (44970929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:587e2528d7bd8b04b6611e9bf599ba3bd5f715852109189a0e3083d0cd3ab8ac`  
		Last Modified: Tue, 04 Jun 2024 00:30:45 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b63360a3869dd2324b9afc69220fdd9ab679f048bf48e30222b3a33d9f2131c`  
		Last Modified: Tue, 04 Jun 2024 00:30:46 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f61f348ae95890e7ffe175821d70d36dff6cbf8a1090acb513be2054d1fdd14e`  
		Last Modified: Tue, 04 Jun 2024 00:30:46 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:83948834d4691d46e4700a9818e255dd94a223e116a82e35c3c507e2e1c660e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2671968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:719c7373785b7461f4782337be23d22796be7338f526f53a70360d9da6da9c55`

```dockerfile
```

-	Layers:
	-	`sha256:cac0bb0a71f4dcd5eb86f11e418d44546f1e35f9eeaad8c1e730b1a5e36e20a1`  
		Last Modified: Tue, 04 Jun 2024 00:30:46 GMT  
		Size: 2.7 MB (2655786 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d43bed1639b69a3e0de48c7b22f9418945ed030c68b8f871ed9ab7743ea403f`  
		Last Modified: Tue, 04 Jun 2024 00:30:46 GMT  
		Size: 16.2 KB (16182 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.10-alpine`

```console
$ docker pull chronograf@sha256:0a4afb73e2d3a91a06e36601c0b8c9c18e5aeb825e8edcceb9d18e338a0e0203
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.10-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:b55598a8b3ee7feb689bcb380dc0f234d328f2eb47c881346dc30b481bb81f1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31807875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b40200ab7f22ab99c0b92e31ce0a9ef862bfd80a2efa3813ebad5e2bdf598f9b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
CMD ["/bin/sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
RUN apk add --no-cache ca-certificates su-exec &&     update-ca-certificates # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.10.5
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S chronograf &&     adduser -S chronograf -G chronograf &&     mkdir -m 0750 -p /var/lib/chronograf &&     chown chronograf:chronograf /var/lib/chronograf # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a541091e90e8b5010bc3e6964324ac4919c24be8f5fb5653082302eec5fc1ec4`  
		Last Modified: Mon, 03 Jun 2024 19:00:15 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d70bae9f6b1c0feca8cb0ba973e7e28953ffa5a9d62cfbfcd897abd2d016af8`  
		Last Modified: Mon, 03 Jun 2024 19:00:16 GMT  
		Size: 294.3 KB (294348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27b085bda50e0c5e25c7a4ebec7e1ccd7ae22a5c76ef00439f8b7c4d022b38fb`  
		Last Modified: Mon, 03 Jun 2024 19:00:16 GMT  
		Size: 27.9 MB (27866729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1990a674718757fef7810e42e4c5340c248ad43f1d9abdec7439e5b9cd01723`  
		Last Modified: Mon, 03 Jun 2024 19:00:15 GMT  
		Size: 12.2 KB (12237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14e68549b54b63067c056976b55d6c93ac1866dcad3a2e1dde832662e2da39f8`  
		Last Modified: Mon, 03 Jun 2024 19:00:16 GMT  
		Size: 11.9 KB (11896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9edb80f2e5c4143929355c91c8f989dafdbea5bce4a5e2c628198ab81d0e456e`  
		Last Modified: Mon, 03 Jun 2024 19:00:16 GMT  
		Size: 292.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:27b4cb11ebf88b4475e41a68de08386fcb61342e61fff5f48ad3b929f482634f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.5 KB (244494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65197df914a82b3f2f03ba701ae27857bf44eff66c30c4cf0b573d7eda631965`

```dockerfile
```

-	Layers:
	-	`sha256:ca5768a37193228f1c8c19dcb7236caefe2d82d164db3e45a19eea54e191d717`  
		Last Modified: Mon, 03 Jun 2024 19:00:15 GMT  
		Size: 226.9 KB (226903 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe809aec848a51e9dedbd725ce359b20a0efb4f28696cc4188181514e5202eac`  
		Last Modified: Mon, 03 Jun 2024 19:00:15 GMT  
		Size: 17.6 KB (17591 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.10.5`

```console
$ docker pull chronograf@sha256:cf6bab04e7f150c1ecae89c8e94de6873be3b146e71803d992ac46ad73cf0c5a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `chronograf:1.10.5` - linux; amd64

```console
$ docker pull chronograf@sha256:5f5537b449b3f8035637e4ce9eb6d4720ced46f8db9d4e2c13c95be6f1ac7be9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.1 MB (84069434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45996034df2c6fe446e5e2fd0aa29d585534c107ab461bba710b9e9e2a59446d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 14 May 2024 01:28:03 GMT
ADD file:5aaace706aa00ff97d243daa2c29f5de88f124e1b97c570634f16eef90783286 in / 
# Tue, 14 May 2024 01:28:04 GMT
CMD ["bash"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.10.5
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:09f376ebb190216b0459f470e71bec7b5dfa611d66bf008492b40dcc5f1d8eae`  
		Last Modified: Tue, 14 May 2024 01:32:30 GMT  
		Size: 29.2 MB (29150411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8f47b768815e9c2366c46a8534a57f09e4f6f0ff4b0b52b64ba601dc9a9c174`  
		Last Modified: Mon, 03 Jun 2024 19:00:29 GMT  
		Size: 7.7 MB (7676940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9489fbf683135fcfa140c8d0a17e9d550c173fc3a052bc84f9f267f99252cf48`  
		Last Modified: Mon, 03 Jun 2024 19:00:31 GMT  
		Size: 47.2 MB (47217627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ed019f6b0534dfea3bfb7a969d8574f9df636506f6f19524b92326e37d2ada2`  
		Last Modified: Mon, 03 Jun 2024 19:00:28 GMT  
		Size: 12.2 KB (12241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb7ab6f5f28a95f1a3f7d8c842fdfc39c48d986d7d2fc301067f3717612a58d4`  
		Last Modified: Mon, 03 Jun 2024 19:00:28 GMT  
		Size: 11.9 KB (11900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af934b4bf874818dedfe49e86bee37a24e98cfb0e261bef354508666419f1249`  
		Last Modified: Mon, 03 Jun 2024 19:00:30 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10.5` - unknown; unknown

```console
$ docker pull chronograf@sha256:c109af0e26df5eea8f474e65c0139dbb1f2441db69a8534d6e4d0c20f1eebaa6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2671399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d7cf432a9a5718d9f6b2250ab83415c141962d8a0deb4e8a169e459aff78d57`

```dockerfile
```

-	Layers:
	-	`sha256:c3d8929c831b697a62dc9682fd7ae7044d6cd8342004667d41fd27a573432ef3`  
		Last Modified: Mon, 03 Jun 2024 19:00:29 GMT  
		Size: 2.7 MB (2655514 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3661947447bdb2d0b40fbad7fa348a99abb8e7e835a3351efddc4c57262a0019`  
		Last Modified: Mon, 03 Jun 2024 19:00:28 GMT  
		Size: 15.9 KB (15885 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.10.5` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:1a460b0bc194e24766aea7533b5cb8d0b916e7f6a09f4ef955743cbbb2a3d430
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.3 MB (75343302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fd2dc826fb7082fc62609abbeac1458117fce816a079a2e66b02f714e7625b3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 14 May 2024 01:08:45 GMT
ADD file:e170e8e24c36eb1a1a24d68a97cd2a7784d689387d804630dc7b596551d91090 in / 
# Tue, 14 May 2024 01:08:45 GMT
CMD ["bash"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.10.5
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:3b9aff019fd47145a0f08828c4c912b901596e71f6dbe2367a7a098e8882ef55`  
		Last Modified: Tue, 14 May 2024 01:12:45 GMT  
		Size: 24.7 MB (24740205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8351e2a7bec99074c9b2552b2d42aabba4fff0d39db3d0ba9b68a404136d1453`  
		Last Modified: Mon, 03 Jun 2024 19:21:37 GMT  
		Size: 6.3 MB (6301009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ecd35a42c7fd3bb3846a30c6d03f105a7b0004871c712048da35ad37776b89a`  
		Last Modified: Mon, 03 Jun 2024 19:21:38 GMT  
		Size: 44.3 MB (44277619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c6834d5d76602cbf35137f057e581f58279ed2341c8d70ea3c43059d1e869aa`  
		Last Modified: Mon, 03 Jun 2024 19:21:37 GMT  
		Size: 12.2 KB (12244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a1ff0b1eeee3067ebbfb12a9699f51e68c235bba7025e052f468ff25d8a0a8e`  
		Last Modified: Mon, 03 Jun 2024 19:21:37 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c88710b32ff5bef236a642c6ffa7546c65aafb1a9703ec9aa5584b140c831f8e`  
		Last Modified: Mon, 03 Jun 2024 19:21:38 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10.5` - unknown; unknown

```console
$ docker pull chronograf@sha256:80c599174d5b9b187f9c7428801ab128e6596094361cbaf40235d64ed9cb9168
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2673769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9a7de8a8b42ee3697139c5dc16ce57f52de462a641be9a93075c7416c83c588`

```dockerfile
```

-	Layers:
	-	`sha256:912fd66c49cdd7f7ba8e22dc0f03fa2098c87be72f0f8e38c2d13d2dea925230`  
		Last Modified: Mon, 03 Jun 2024 19:21:37 GMT  
		Size: 2.7 MB (2657810 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de523748666f12dea6e03853effe8f169d72dbd26d1ddcb7bb613ac802d32c6b`  
		Last Modified: Mon, 03 Jun 2024 19:21:37 GMT  
		Size: 16.0 KB (15959 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.10.5` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:56fc9a7d7b5e4129e88ff15e6e3f443c62536180fba87c675a42fce7c1e2a205
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.6 MB (81628060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06be28a02b74fac1638579f669127787c0ed3809f3587e6af1cf9b7761558b79`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 14 May 2024 00:39:40 GMT
ADD file:e23ba17afc7850bcca9e73ba5022db9f0a80c6a0250585fd3f50a1960226474b in / 
# Tue, 14 May 2024 00:39:41 GMT
CMD ["bash"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.10.5
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:24c63b8dcb66721062f32b893ef1027404afddd62aade87f3f39a3a6e70a74d0`  
		Last Modified: Tue, 14 May 2024 00:42:56 GMT  
		Size: 29.2 MB (29179503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d41ef92593599be99b703585f08f0f9d449d437aa1a40c01770b9496e36d09aa`  
		Last Modified: Tue, 04 Jun 2024 00:30:46 GMT  
		Size: 7.5 MB (7453158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:242a93b9d52597004cac704e713b2296dc4c9e12747f37ef26bfc754a8185575`  
		Last Modified: Tue, 04 Jun 2024 00:30:47 GMT  
		Size: 45.0 MB (44970929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:587e2528d7bd8b04b6611e9bf599ba3bd5f715852109189a0e3083d0cd3ab8ac`  
		Last Modified: Tue, 04 Jun 2024 00:30:45 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b63360a3869dd2324b9afc69220fdd9ab679f048bf48e30222b3a33d9f2131c`  
		Last Modified: Tue, 04 Jun 2024 00:30:46 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f61f348ae95890e7ffe175821d70d36dff6cbf8a1090acb513be2054d1fdd14e`  
		Last Modified: Tue, 04 Jun 2024 00:30:46 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10.5` - unknown; unknown

```console
$ docker pull chronograf@sha256:83948834d4691d46e4700a9818e255dd94a223e116a82e35c3c507e2e1c660e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2671968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:719c7373785b7461f4782337be23d22796be7338f526f53a70360d9da6da9c55`

```dockerfile
```

-	Layers:
	-	`sha256:cac0bb0a71f4dcd5eb86f11e418d44546f1e35f9eeaad8c1e730b1a5e36e20a1`  
		Last Modified: Tue, 04 Jun 2024 00:30:46 GMT  
		Size: 2.7 MB (2655786 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d43bed1639b69a3e0de48c7b22f9418945ed030c68b8f871ed9ab7743ea403f`  
		Last Modified: Tue, 04 Jun 2024 00:30:46 GMT  
		Size: 16.2 KB (16182 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.10.5-alpine`

```console
$ docker pull chronograf@sha256:0a4afb73e2d3a91a06e36601c0b8c9c18e5aeb825e8edcceb9d18e338a0e0203
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.10.5-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:b55598a8b3ee7feb689bcb380dc0f234d328f2eb47c881346dc30b481bb81f1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31807875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b40200ab7f22ab99c0b92e31ce0a9ef862bfd80a2efa3813ebad5e2bdf598f9b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
CMD ["/bin/sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
RUN apk add --no-cache ca-certificates su-exec &&     update-ca-certificates # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.10.5
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S chronograf &&     adduser -S chronograf -G chronograf &&     mkdir -m 0750 -p /var/lib/chronograf &&     chown chronograf:chronograf /var/lib/chronograf # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a541091e90e8b5010bc3e6964324ac4919c24be8f5fb5653082302eec5fc1ec4`  
		Last Modified: Mon, 03 Jun 2024 19:00:15 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d70bae9f6b1c0feca8cb0ba973e7e28953ffa5a9d62cfbfcd897abd2d016af8`  
		Last Modified: Mon, 03 Jun 2024 19:00:16 GMT  
		Size: 294.3 KB (294348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27b085bda50e0c5e25c7a4ebec7e1ccd7ae22a5c76ef00439f8b7c4d022b38fb`  
		Last Modified: Mon, 03 Jun 2024 19:00:16 GMT  
		Size: 27.9 MB (27866729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1990a674718757fef7810e42e4c5340c248ad43f1d9abdec7439e5b9cd01723`  
		Last Modified: Mon, 03 Jun 2024 19:00:15 GMT  
		Size: 12.2 KB (12237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14e68549b54b63067c056976b55d6c93ac1866dcad3a2e1dde832662e2da39f8`  
		Last Modified: Mon, 03 Jun 2024 19:00:16 GMT  
		Size: 11.9 KB (11896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9edb80f2e5c4143929355c91c8f989dafdbea5bce4a5e2c628198ab81d0e456e`  
		Last Modified: Mon, 03 Jun 2024 19:00:16 GMT  
		Size: 292.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10.5-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:27b4cb11ebf88b4475e41a68de08386fcb61342e61fff5f48ad3b929f482634f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.5 KB (244494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65197df914a82b3f2f03ba701ae27857bf44eff66c30c4cf0b573d7eda631965`

```dockerfile
```

-	Layers:
	-	`sha256:ca5768a37193228f1c8c19dcb7236caefe2d82d164db3e45a19eea54e191d717`  
		Last Modified: Mon, 03 Jun 2024 19:00:15 GMT  
		Size: 226.9 KB (226903 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe809aec848a51e9dedbd725ce359b20a0efb4f28696cc4188181514e5202eac`  
		Last Modified: Mon, 03 Jun 2024 19:00:15 GMT  
		Size: 17.6 KB (17591 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.7`

```console
$ docker pull chronograf@sha256:aad01cfb598572242859deb86844490944779e5fddef6274a7a748aa2ca1b411
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
$ docker pull chronograf@sha256:e771eb1dd91558b1a234191d5b194723beb1f3acc6e887e1256051809977b2a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.2 MB (70201689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:605b64690951dfc164c533fad52c3743ffded563d05b84cc7e57c039205d2bd8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 14 May 2024 01:28:26 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
# Tue, 14 May 2024 01:28:27 GMT
CMD ["bash"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e7df2ee68a080fc3deb51ba4dc43a775497c517aff0c008f3250e06a2213587`  
		Last Modified: Mon, 03 Jun 2024 19:00:25 GMT  
		Size: 4.2 MB (4209290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17bf786ae42424dee79b994f9cd126bac3d075fccb72431933919c3c68f73081`  
		Last Modified: Mon, 03 Jun 2024 19:00:26 GMT  
		Size: 34.5 MB (34534081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83a0e61a65cd4085f394773e0a72b2bad7b72aa7b019abf7c461f523c2f4882d`  
		Last Modified: Mon, 03 Jun 2024 19:00:25 GMT  
		Size: 12.2 KB (12244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5300f7eb373467760bca394f741820823cdff2c6283a0b53f99b0df10a409b87`  
		Last Modified: Mon, 03 Jun 2024 19:00:24 GMT  
		Size: 11.9 KB (11903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d808014185b840155ec50f288b516fb94796c0651de48d9c110092fc34d4c540`  
		Last Modified: Mon, 03 Jun 2024 19:00:26 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7` - unknown; unknown

```console
$ docker pull chronograf@sha256:f397e6f11dd2f45e8dfca8151e06aadf76e5ae70bcd8defdc24bea152505427d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2882783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b81349ac4d5da0b18ef4d787d573f58ca14ede92048d9375cafdd998ad87538c`

```dockerfile
```

-	Layers:
	-	`sha256:4329e3e09074a6b3f14c33a784981c038f7eeac0768fd30776809a37b101221f`  
		Last Modified: Mon, 03 Jun 2024 19:00:24 GMT  
		Size: 2.9 MB (2867249 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:818df8a93fce3900326584636d20d90a00c8a677eef7decf16aca065754112ec`  
		Last Modified: Mon, 03 Jun 2024 19:00:24 GMT  
		Size: 15.5 KB (15534 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.7` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:74ec5d55658d378d1c56252dcacdc0a321abc52b53823fc1d467c373a5133bb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.0 MB (63024051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:163630a4c42551f1a07caa331cc624451014f8b945a5ff46e3022ff3ab190a05`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 14 May 2024 01:09:04 GMT
ADD file:b58f353e9d2a24c2c16ae0913b28705d3ecc439d60d82b5b4982780c59aae249 in / 
# Tue, 14 May 2024 01:09:04 GMT
CMD ["bash"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:a5c0b9604ae49509a7875b258d98493d63bdb4c1c27a70f2befa5fa4fcea1888`  
		Last Modified: Tue, 14 May 2024 01:13:30 GMT  
		Size: 26.6 MB (26594493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c14fec17bc28ba0f6c10d4eac337f8c3195922f47d5f10c14fcacb48178d7a4`  
		Last Modified: Mon, 03 Jun 2024 19:18:59 GMT  
		Size: 3.5 MB (3511538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a106d63f143ac2f8a90e7c3fad17cf470ef852d06ee33ef32e0e6bf1b544e72`  
		Last Modified: Mon, 03 Jun 2024 19:19:00 GMT  
		Size: 32.9 MB (32893636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bc2f1818e8b8ca568704279b496b9bf47cabcf1bac38945a3c35fd4b7ac0674`  
		Last Modified: Mon, 03 Jun 2024 19:18:58 GMT  
		Size: 12.2 KB (12243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f925e859b18f1469bc996a37a79461c8c2a6e4909926cd5416974f542b86bf43`  
		Last Modified: Mon, 03 Jun 2024 19:18:58 GMT  
		Size: 11.9 KB (11902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1331f68246f938f2b09d35aa9c04ffa0f1cc3beca4ebdaaa774a7f901d33d473`  
		Last Modified: Mon, 03 Jun 2024 19:18:59 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7` - unknown; unknown

```console
$ docker pull chronograf@sha256:a075e23b5da3d43f002532bcb50b07182954a495c400124bbe08a9936df1e621
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2885119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2341a626caf71b70a908dd11443c5ad0ab2ae372c7b5a8f7c675d9594a8fee8a`

```dockerfile
```

-	Layers:
	-	`sha256:cb193408eef6c065e9b904cb4a28b1975a10cd56e175538ebfb6022b24bc6774`  
		Last Modified: Mon, 03 Jun 2024 19:18:58 GMT  
		Size: 2.9 MB (2869519 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b4ba62523961f2ad83a20b67b15faa1fe65e4c825b1d217dd93d7d17dc04abf`  
		Last Modified: Mon, 03 Jun 2024 19:18:58 GMT  
		Size: 15.6 KB (15600 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.7` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:f5f138a405eca97131766d972a9b64b4b063e8fc672fa704505b166c46aa4b82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.4 MB (67355720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1d8c5109318b3590705255bc640e47a1e35ed4c716a6c1d564349d47daf999c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 14 May 2024 00:39:55 GMT
ADD file:0465ea1f0e8a2ee3e0f770c3b7f8e4a2b8719c624b440cabe7d7ecbe87200e7b in / 
# Tue, 14 May 2024 00:39:56 GMT
CMD ["bash"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:3a0037c67e2f4632684ea787f751ddb0b6af2b86113ab3b6859744b6eaf77e2f`  
		Last Modified: Tue, 14 May 2024 00:43:33 GMT  
		Size: 30.1 MB (30086908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f325e83bfe43f42c021f8efbd1a8530851b2a40f81f04ba8f0f9c539519a29b9`  
		Last Modified: Mon, 03 Jun 2024 22:31:50 GMT  
		Size: 4.2 MB (4210542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f9b4c4123152a83eb7f142ebd9a87075d4735160ca439984308b30e437de37`  
		Last Modified: Mon, 03 Jun 2024 22:31:51 GMT  
		Size: 33.0 MB (33033870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53db58f56ec04bed395fd3616f000f2d5f03937512ca7cf3571e4694b3906ade`  
		Last Modified: Mon, 03 Jun 2024 22:31:50 GMT  
		Size: 12.3 KB (12251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28ccbd9aba90aeeb526a950cfb3726e257e7fabd6beea975a0199d1a64d00ea3`  
		Last Modified: Mon, 03 Jun 2024 22:31:50 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8578f9bde0057d8b4dfd74188ccab1b78d25ecd19af3a926b843396ddb372b3e`  
		Last Modified: Mon, 03 Jun 2024 22:31:51 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7` - unknown; unknown

```console
$ docker pull chronograf@sha256:0c5e11652dd76b8a396d6bfc2a49fe1979119d82673feaa3f8fa9266563de7d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2883314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3857c6d6b6f83d56188742e0c2ad0e6eb44f1ab4c893685c5d07e11fbe7444a9`

```dockerfile
```

-	Layers:
	-	`sha256:24a28d8dee5a53d1b1e6486e6fe7e0c177888fddf76245e4cc56f8caf99129f6`  
		Last Modified: Mon, 03 Jun 2024 22:31:50 GMT  
		Size: 2.9 MB (2867497 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ae6e62ad7576689d2f38f5c225227a21b38c2d82328a75efe6a7746ffa56614`  
		Last Modified: Mon, 03 Jun 2024 22:31:50 GMT  
		Size: 15.8 KB (15817 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.7-alpine`

```console
$ docker pull chronograf@sha256:97e608fbc9d5ece2e10d6a4fdeb5400ab2b90bc51fa11a1bc0e329b22085ddae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.7-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:1d63485ec327e512c21c99df65684bcd2a16298a4db56ce0a85d74a728119938
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.5 MB (23495805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:def726efefa52ab291a85a9ff7797ab7af190886858938f7279f3bb6606a5341`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
CMD ["/bin/sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75e2c1a9f5d7c296d9d1f78c0c01e7df684fbdaa939eb66a82be32faea4e39ae`  
		Last Modified: Mon, 03 Jun 2024 18:59:59 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aa917d7092520fd13899ba8333f1456d1f26988be1ae52b911a160ddd5b2809`  
		Last Modified: Mon, 03 Jun 2024 18:59:59 GMT  
		Size: 292.4 KB (292424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aedecea2ae51e24c52152130aca5bb48b609f7bbbdd3239bf354d7180a56dc47`  
		Last Modified: Mon, 03 Jun 2024 19:00:00 GMT  
		Size: 19.6 MB (19556638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c35c4f6bb929f1d4a3a4e51fd8978406eb1d2c52a4446eaef7c8a9e65dd3d58`  
		Last Modified: Mon, 03 Jun 2024 18:59:59 GMT  
		Size: 12.2 KB (12236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d44cf4b9c32bc43bfa342f40a682936838b43be837fda1cbe80bb5406d2e77a6`  
		Last Modified: Mon, 03 Jun 2024 19:00:00 GMT  
		Size: 11.9 KB (11895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ba311571e9924d052a4fd7db0373dbf85cfc7c1a99913ffc875962b0301edbd`  
		Last Modified: Mon, 03 Jun 2024 19:00:00 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:684f4abf7dc03aafcafa10c64f606dcd67321ed31a6a18fa0a649e5afb6cdf9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.2 KB (185205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f58c1b8e25e159332e920cd7b703247a56de8758e250f5754e17d928cd5fbe5`

```dockerfile
```

-	Layers:
	-	`sha256:777bc9907af9c3bab9a2d0bbdbd7fe95706c24123c611cc88a32ac9879ad3b34`  
		Last Modified: Mon, 03 Jun 2024 18:59:59 GMT  
		Size: 168.6 KB (168559 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10b5c042e918ee2f9be2275c2fa0c83af682a39434975a5196910b675f04ee6f`  
		Last Modified: Mon, 03 Jun 2024 18:59:59 GMT  
		Size: 16.6 KB (16646 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.7.17`

```console
$ docker pull chronograf@sha256:aad01cfb598572242859deb86844490944779e5fddef6274a7a748aa2ca1b411
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
$ docker pull chronograf@sha256:e771eb1dd91558b1a234191d5b194723beb1f3acc6e887e1256051809977b2a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.2 MB (70201689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:605b64690951dfc164c533fad52c3743ffded563d05b84cc7e57c039205d2bd8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 14 May 2024 01:28:26 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
# Tue, 14 May 2024 01:28:27 GMT
CMD ["bash"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e7df2ee68a080fc3deb51ba4dc43a775497c517aff0c008f3250e06a2213587`  
		Last Modified: Mon, 03 Jun 2024 19:00:25 GMT  
		Size: 4.2 MB (4209290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17bf786ae42424dee79b994f9cd126bac3d075fccb72431933919c3c68f73081`  
		Last Modified: Mon, 03 Jun 2024 19:00:26 GMT  
		Size: 34.5 MB (34534081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83a0e61a65cd4085f394773e0a72b2bad7b72aa7b019abf7c461f523c2f4882d`  
		Last Modified: Mon, 03 Jun 2024 19:00:25 GMT  
		Size: 12.2 KB (12244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5300f7eb373467760bca394f741820823cdff2c6283a0b53f99b0df10a409b87`  
		Last Modified: Mon, 03 Jun 2024 19:00:24 GMT  
		Size: 11.9 KB (11903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d808014185b840155ec50f288b516fb94796c0651de48d9c110092fc34d4c540`  
		Last Modified: Mon, 03 Jun 2024 19:00:26 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7.17` - unknown; unknown

```console
$ docker pull chronograf@sha256:f397e6f11dd2f45e8dfca8151e06aadf76e5ae70bcd8defdc24bea152505427d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2882783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b81349ac4d5da0b18ef4d787d573f58ca14ede92048d9375cafdd998ad87538c`

```dockerfile
```

-	Layers:
	-	`sha256:4329e3e09074a6b3f14c33a784981c038f7eeac0768fd30776809a37b101221f`  
		Last Modified: Mon, 03 Jun 2024 19:00:24 GMT  
		Size: 2.9 MB (2867249 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:818df8a93fce3900326584636d20d90a00c8a677eef7decf16aca065754112ec`  
		Last Modified: Mon, 03 Jun 2024 19:00:24 GMT  
		Size: 15.5 KB (15534 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.7.17` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:74ec5d55658d378d1c56252dcacdc0a321abc52b53823fc1d467c373a5133bb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.0 MB (63024051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:163630a4c42551f1a07caa331cc624451014f8b945a5ff46e3022ff3ab190a05`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 14 May 2024 01:09:04 GMT
ADD file:b58f353e9d2a24c2c16ae0913b28705d3ecc439d60d82b5b4982780c59aae249 in / 
# Tue, 14 May 2024 01:09:04 GMT
CMD ["bash"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:a5c0b9604ae49509a7875b258d98493d63bdb4c1c27a70f2befa5fa4fcea1888`  
		Last Modified: Tue, 14 May 2024 01:13:30 GMT  
		Size: 26.6 MB (26594493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c14fec17bc28ba0f6c10d4eac337f8c3195922f47d5f10c14fcacb48178d7a4`  
		Last Modified: Mon, 03 Jun 2024 19:18:59 GMT  
		Size: 3.5 MB (3511538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a106d63f143ac2f8a90e7c3fad17cf470ef852d06ee33ef32e0e6bf1b544e72`  
		Last Modified: Mon, 03 Jun 2024 19:19:00 GMT  
		Size: 32.9 MB (32893636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bc2f1818e8b8ca568704279b496b9bf47cabcf1bac38945a3c35fd4b7ac0674`  
		Last Modified: Mon, 03 Jun 2024 19:18:58 GMT  
		Size: 12.2 KB (12243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f925e859b18f1469bc996a37a79461c8c2a6e4909926cd5416974f542b86bf43`  
		Last Modified: Mon, 03 Jun 2024 19:18:58 GMT  
		Size: 11.9 KB (11902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1331f68246f938f2b09d35aa9c04ffa0f1cc3beca4ebdaaa774a7f901d33d473`  
		Last Modified: Mon, 03 Jun 2024 19:18:59 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7.17` - unknown; unknown

```console
$ docker pull chronograf@sha256:a075e23b5da3d43f002532bcb50b07182954a495c400124bbe08a9936df1e621
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2885119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2341a626caf71b70a908dd11443c5ad0ab2ae372c7b5a8f7c675d9594a8fee8a`

```dockerfile
```

-	Layers:
	-	`sha256:cb193408eef6c065e9b904cb4a28b1975a10cd56e175538ebfb6022b24bc6774`  
		Last Modified: Mon, 03 Jun 2024 19:18:58 GMT  
		Size: 2.9 MB (2869519 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b4ba62523961f2ad83a20b67b15faa1fe65e4c825b1d217dd93d7d17dc04abf`  
		Last Modified: Mon, 03 Jun 2024 19:18:58 GMT  
		Size: 15.6 KB (15600 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.7.17` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:f5f138a405eca97131766d972a9b64b4b063e8fc672fa704505b166c46aa4b82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.4 MB (67355720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1d8c5109318b3590705255bc640e47a1e35ed4c716a6c1d564349d47daf999c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 14 May 2024 00:39:55 GMT
ADD file:0465ea1f0e8a2ee3e0f770c3b7f8e4a2b8719c624b440cabe7d7ecbe87200e7b in / 
# Tue, 14 May 2024 00:39:56 GMT
CMD ["bash"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:3a0037c67e2f4632684ea787f751ddb0b6af2b86113ab3b6859744b6eaf77e2f`  
		Last Modified: Tue, 14 May 2024 00:43:33 GMT  
		Size: 30.1 MB (30086908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f325e83bfe43f42c021f8efbd1a8530851b2a40f81f04ba8f0f9c539519a29b9`  
		Last Modified: Mon, 03 Jun 2024 22:31:50 GMT  
		Size: 4.2 MB (4210542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f9b4c4123152a83eb7f142ebd9a87075d4735160ca439984308b30e437de37`  
		Last Modified: Mon, 03 Jun 2024 22:31:51 GMT  
		Size: 33.0 MB (33033870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53db58f56ec04bed395fd3616f000f2d5f03937512ca7cf3571e4694b3906ade`  
		Last Modified: Mon, 03 Jun 2024 22:31:50 GMT  
		Size: 12.3 KB (12251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28ccbd9aba90aeeb526a950cfb3726e257e7fabd6beea975a0199d1a64d00ea3`  
		Last Modified: Mon, 03 Jun 2024 22:31:50 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8578f9bde0057d8b4dfd74188ccab1b78d25ecd19af3a926b843396ddb372b3e`  
		Last Modified: Mon, 03 Jun 2024 22:31:51 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7.17` - unknown; unknown

```console
$ docker pull chronograf@sha256:0c5e11652dd76b8a396d6bfc2a49fe1979119d82673feaa3f8fa9266563de7d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2883314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3857c6d6b6f83d56188742e0c2ad0e6eb44f1ab4c893685c5d07e11fbe7444a9`

```dockerfile
```

-	Layers:
	-	`sha256:24a28d8dee5a53d1b1e6486e6fe7e0c177888fddf76245e4cc56f8caf99129f6`  
		Last Modified: Mon, 03 Jun 2024 22:31:50 GMT  
		Size: 2.9 MB (2867497 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ae6e62ad7576689d2f38f5c225227a21b38c2d82328a75efe6a7746ffa56614`  
		Last Modified: Mon, 03 Jun 2024 22:31:50 GMT  
		Size: 15.8 KB (15817 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.7.17-alpine`

```console
$ docker pull chronograf@sha256:97e608fbc9d5ece2e10d6a4fdeb5400ab2b90bc51fa11a1bc0e329b22085ddae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.7.17-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:1d63485ec327e512c21c99df65684bcd2a16298a4db56ce0a85d74a728119938
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.5 MB (23495805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:def726efefa52ab291a85a9ff7797ab7af190886858938f7279f3bb6606a5341`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
CMD ["/bin/sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75e2c1a9f5d7c296d9d1f78c0c01e7df684fbdaa939eb66a82be32faea4e39ae`  
		Last Modified: Mon, 03 Jun 2024 18:59:59 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aa917d7092520fd13899ba8333f1456d1f26988be1ae52b911a160ddd5b2809`  
		Last Modified: Mon, 03 Jun 2024 18:59:59 GMT  
		Size: 292.4 KB (292424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aedecea2ae51e24c52152130aca5bb48b609f7bbbdd3239bf354d7180a56dc47`  
		Last Modified: Mon, 03 Jun 2024 19:00:00 GMT  
		Size: 19.6 MB (19556638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c35c4f6bb929f1d4a3a4e51fd8978406eb1d2c52a4446eaef7c8a9e65dd3d58`  
		Last Modified: Mon, 03 Jun 2024 18:59:59 GMT  
		Size: 12.2 KB (12236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d44cf4b9c32bc43bfa342f40a682936838b43be837fda1cbe80bb5406d2e77a6`  
		Last Modified: Mon, 03 Jun 2024 19:00:00 GMT  
		Size: 11.9 KB (11895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ba311571e9924d052a4fd7db0373dbf85cfc7c1a99913ffc875962b0301edbd`  
		Last Modified: Mon, 03 Jun 2024 19:00:00 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7.17-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:684f4abf7dc03aafcafa10c64f606dcd67321ed31a6a18fa0a649e5afb6cdf9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.2 KB (185205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f58c1b8e25e159332e920cd7b703247a56de8758e250f5754e17d928cd5fbe5`

```dockerfile
```

-	Layers:
	-	`sha256:777bc9907af9c3bab9a2d0bbdbd7fe95706c24123c611cc88a32ac9879ad3b34`  
		Last Modified: Mon, 03 Jun 2024 18:59:59 GMT  
		Size: 168.6 KB (168559 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10b5c042e918ee2f9be2275c2fa0c83af682a39434975a5196910b675f04ee6f`  
		Last Modified: Mon, 03 Jun 2024 18:59:59 GMT  
		Size: 16.6 KB (16646 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.8`

```console
$ docker pull chronograf@sha256:bc6359007b7dead8bb3276440c9442514268d44d12951795c4ad58784cff204b
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
$ docker pull chronograf@sha256:5557231e8b7359e64fe893db4c44ec6a88c6941ab9c0255f63e4a5b525be776d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.8 MB (70843298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:343f144f88c351cb4154a088c734f465dd8f0948cd8739479a75af84e756370e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 14 May 2024 01:28:26 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
# Tue, 14 May 2024 01:28:27 GMT
CMD ["bash"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2f2f9f4c33d963aab8040475e05d4ef5a3f7ae046cc091ed9bda0c18b756da5`  
		Last Modified: Mon, 03 Jun 2024 19:00:11 GMT  
		Size: 5.0 MB (5020970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c035d2957988e1173e9f6f9599aa16e8270ac0d9edf22d7e06e9d2768bf95e03`  
		Last Modified: Mon, 03 Jun 2024 19:00:12 GMT  
		Size: 34.4 MB (34364003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7ff06671a7bd3dc445e3a0b76cf4980c954f465684e3aade2573d09e8ae5dbb`  
		Last Modified: Mon, 03 Jun 2024 19:00:11 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8886242ffbb981aeeb9fb18ca92fafe3551251f1113894a8ee302d4bd4065d10`  
		Last Modified: Mon, 03 Jun 2024 19:00:11 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1477d5e19f7a88eec147ff9d1087ddf91119230a6cad1df2639442af1ba928f`  
		Last Modified: Mon, 03 Jun 2024 19:00:12 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8` - unknown; unknown

```console
$ docker pull chronograf@sha256:67f8177d088cf68030d2928785378620f67d557018c26651ced27c2adfec3b69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2930484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e58e4ab8ef6e0f7c2502f1a91712fac46383806ad0b9ec2ed29fe6cf3034cc25`

```dockerfile
```

-	Layers:
	-	`sha256:58e9f2be0be0429d43da092caf76494013dc3a94b38c76351ec82141bbe4824c`  
		Last Modified: Mon, 03 Jun 2024 19:00:10 GMT  
		Size: 2.9 MB (2914910 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2392821973aa9fda09092705d6fa46b96ac55ac41c9e025d2addeeb034282a9`  
		Last Modified: Mon, 03 Jun 2024 19:00:10 GMT  
		Size: 15.6 KB (15574 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.8` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:f13aec18f54cf4c0d2ee722f72a895c7cc0668b33db82b7a09b524e598a51149
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.4 MB (63439861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f83158b65b6cbfac8ad1586876ef981757411371ebd4ae60e431a503e5f22d1f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 14 May 2024 01:09:04 GMT
ADD file:b58f353e9d2a24c2c16ae0913b28705d3ecc439d60d82b5b4982780c59aae249 in / 
# Tue, 14 May 2024 01:09:04 GMT
CMD ["bash"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:a5c0b9604ae49509a7875b258d98493d63bdb4c1c27a70f2befa5fa4fcea1888`  
		Last Modified: Tue, 14 May 2024 01:13:30 GMT  
		Size: 26.6 MB (26594493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0b0acb5a1b927da712d58a924d52531d1a48efeb89cda46a49ebf7ac59c41b6`  
		Last Modified: Mon, 03 Jun 2024 19:19:59 GMT  
		Size: 4.3 MB (4286192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450a08c630325441489f21cd800611e9feb2492b8eb31f83a6594b2e40214cd8`  
		Last Modified: Mon, 03 Jun 2024 19:20:00 GMT  
		Size: 32.5 MB (32534782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bc626dd10091954b5146ae202f47df0ef7c9190b2af49d014e7c37442d81c04`  
		Last Modified: Mon, 03 Jun 2024 19:19:59 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb73719554076c9154225b52ae4b1ac65633f938a7b950a58de1e76b2214af0`  
		Last Modified: Mon, 03 Jun 2024 19:19:59 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed0c4b1398c8124d3e9ad0a3c189014d60c8b6bb3d1bfbb9bbc82648d90ee15d`  
		Last Modified: Mon, 03 Jun 2024 19:20:00 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8` - unknown; unknown

```console
$ docker pull chronograf@sha256:832b7439347fd01f72ea20bea12d776d2d231fd2f0cd9dd6cca60d666a42786d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2932821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e5f07bbbd77d6baf590d6679346f363e8f59f88c0674e3117ed9b93013e2565`

```dockerfile
```

-	Layers:
	-	`sha256:4b632f8757379f48ce7f62375be58317607752c05ca50bf0467970bc7732b8be`  
		Last Modified: Mon, 03 Jun 2024 19:19:59 GMT  
		Size: 2.9 MB (2917180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:445eff67ac2cb7aaefb9d6dacdc1618bc755d7897a207812ddec4de6bda2f483`  
		Last Modified: Mon, 03 Jun 2024 19:19:59 GMT  
		Size: 15.6 KB (15641 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.8` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:4fc1edca1f790b8ac9d5b2173aada3b9286d9682b37f283e782a7ec70bc7a7ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.5 MB (67544788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecb60de9eeaab7c013187a0bec5f7b0bba61e6e24218866965d49eda48c4cfb0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 14 May 2024 00:39:55 GMT
ADD file:0465ea1f0e8a2ee3e0f770c3b7f8e4a2b8719c624b440cabe7d7ecbe87200e7b in / 
# Tue, 14 May 2024 00:39:56 GMT
CMD ["bash"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:3a0037c67e2f4632684ea787f751ddb0b6af2b86113ab3b6859744b6eaf77e2f`  
		Last Modified: Tue, 14 May 2024 00:43:33 GMT  
		Size: 30.1 MB (30086908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a30d1c4ea046e3d2ec261eed89b6a11b07f27477f9db9937ea3d7f1bdf96770`  
		Last Modified: Mon, 03 Jun 2024 23:21:36 GMT  
		Size: 5.0 MB (5004067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1348b8e55237ade45f01834586e51a0102e0b2e5470aa9241f3c9d43d91d8184`  
		Last Modified: Mon, 03 Jun 2024 23:21:37 GMT  
		Size: 32.4 MB (32429418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53c860bd2e343ea246524ecfcdcddab5bc3be9ca2ca76cd5520f473af7ed08b6`  
		Last Modified: Mon, 03 Jun 2024 23:21:35 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6affc35b1b8deb8c68b2ed39088b6cb464a8c715cfeb13b98b7a46a71f363927`  
		Last Modified: Mon, 03 Jun 2024 23:21:35 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c827d71aec063d0b0ef29780a8713a8ba0922e75b119c6556079adf5b5f50db0`  
		Last Modified: Mon, 03 Jun 2024 23:21:36 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8` - unknown; unknown

```console
$ docker pull chronograf@sha256:88bd147fc6fc78aef40ad23875d03d99ea387bc6017d5da123c1af47f5330558
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2931017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a260c5f7ccad1cf371ec733de6364012ea0537067f6e5e706362301433f77928`

```dockerfile
```

-	Layers:
	-	`sha256:68619ec59da40fc071fc5498fd43d7726287e94a8b402bf77d0e477f09aa84cd`  
		Last Modified: Mon, 03 Jun 2024 23:21:36 GMT  
		Size: 2.9 MB (2915158 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6548bb1998e4b025532a832bdd2103900b776501e3c4d122ee707d7b0036c48`  
		Last Modified: Mon, 03 Jun 2024 23:21:35 GMT  
		Size: 15.9 KB (15859 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.8-alpine`

```console
$ docker pull chronograf@sha256:aeff6b0f33ad0c7163d0f15359676e3783b2c4f051277623bb87d3d8f525245b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.8-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:6901af16d25884590ef18c7cf6bc51e247e34e8db598d51aeac3a32686b96281
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23143191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fabb3a35dd209be242515d9abdb28872c03b6087716da9e68d7144ced10310b9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
CMD ["/bin/sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7135375e7e2b93794abc3a6fae771e0e810f1c985d87d5e2b116928c4a5811bb`  
		Last Modified: Mon, 03 Jun 2024 19:00:15 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7604efdcdfb5e914425082e913fa11feebc46f84efbd0eab4d63c026755d79f1`  
		Last Modified: Mon, 03 Jun 2024 19:00:14 GMT  
		Size: 292.4 KB (292422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed08262353aa43a044b72561106caeca51305919dbb951ad7fe4acfc2ad372f0`  
		Last Modified: Mon, 03 Jun 2024 19:00:15 GMT  
		Size: 19.2 MB (19204026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c69cc0629a8f4b4b5775f08d6212e7252bb99bc8b01e1d779a5306d8ce594551`  
		Last Modified: Mon, 03 Jun 2024 19:00:14 GMT  
		Size: 12.2 KB (12236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36c2b2e66b9548a4f932659927715ec1cabc2c5dd4425dd03f2b7185209ba8b9`  
		Last Modified: Mon, 03 Jun 2024 19:00:16 GMT  
		Size: 11.9 KB (11896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0910d626bd5a2723486bd6566ee32668ae861e7a1e18975ac98825605fefe14`  
		Last Modified: Mon, 03 Jun 2024 19:00:16 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:e509b26098019dd58f191c86c4a74dae8e741425f72ae6bf2db1768e4eb80d54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.5 KB (233529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2a1345abbc1eb7303aad85d664a52c2b91b5a286113333875fd693f733f01db`

```dockerfile
```

-	Layers:
	-	`sha256:15f8d2f11400eec69f6ea0110c8ae1da088d7809dc0222f8354511b1bcef6a8a`  
		Last Modified: Mon, 03 Jun 2024 19:00:14 GMT  
		Size: 216.9 KB (216881 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f7394674c01a304ac4ca09c635793f21386d3fff6e6fe7b304eea2650beae68`  
		Last Modified: Mon, 03 Jun 2024 19:00:14 GMT  
		Size: 16.6 KB (16648 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.8.10`

```console
$ docker pull chronograf@sha256:bc6359007b7dead8bb3276440c9442514268d44d12951795c4ad58784cff204b
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
$ docker pull chronograf@sha256:5557231e8b7359e64fe893db4c44ec6a88c6941ab9c0255f63e4a5b525be776d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.8 MB (70843298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:343f144f88c351cb4154a088c734f465dd8f0948cd8739479a75af84e756370e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 14 May 2024 01:28:26 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
# Tue, 14 May 2024 01:28:27 GMT
CMD ["bash"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2f2f9f4c33d963aab8040475e05d4ef5a3f7ae046cc091ed9bda0c18b756da5`  
		Last Modified: Mon, 03 Jun 2024 19:00:11 GMT  
		Size: 5.0 MB (5020970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c035d2957988e1173e9f6f9599aa16e8270ac0d9edf22d7e06e9d2768bf95e03`  
		Last Modified: Mon, 03 Jun 2024 19:00:12 GMT  
		Size: 34.4 MB (34364003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7ff06671a7bd3dc445e3a0b76cf4980c954f465684e3aade2573d09e8ae5dbb`  
		Last Modified: Mon, 03 Jun 2024 19:00:11 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8886242ffbb981aeeb9fb18ca92fafe3551251f1113894a8ee302d4bd4065d10`  
		Last Modified: Mon, 03 Jun 2024 19:00:11 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1477d5e19f7a88eec147ff9d1087ddf91119230a6cad1df2639442af1ba928f`  
		Last Modified: Mon, 03 Jun 2024 19:00:12 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:67f8177d088cf68030d2928785378620f67d557018c26651ced27c2adfec3b69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2930484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e58e4ab8ef6e0f7c2502f1a91712fac46383806ad0b9ec2ed29fe6cf3034cc25`

```dockerfile
```

-	Layers:
	-	`sha256:58e9f2be0be0429d43da092caf76494013dc3a94b38c76351ec82141bbe4824c`  
		Last Modified: Mon, 03 Jun 2024 19:00:10 GMT  
		Size: 2.9 MB (2914910 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2392821973aa9fda09092705d6fa46b96ac55ac41c9e025d2addeeb034282a9`  
		Last Modified: Mon, 03 Jun 2024 19:00:10 GMT  
		Size: 15.6 KB (15574 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.8.10` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:f13aec18f54cf4c0d2ee722f72a895c7cc0668b33db82b7a09b524e598a51149
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.4 MB (63439861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f83158b65b6cbfac8ad1586876ef981757411371ebd4ae60e431a503e5f22d1f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 14 May 2024 01:09:04 GMT
ADD file:b58f353e9d2a24c2c16ae0913b28705d3ecc439d60d82b5b4982780c59aae249 in / 
# Tue, 14 May 2024 01:09:04 GMT
CMD ["bash"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:a5c0b9604ae49509a7875b258d98493d63bdb4c1c27a70f2befa5fa4fcea1888`  
		Last Modified: Tue, 14 May 2024 01:13:30 GMT  
		Size: 26.6 MB (26594493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0b0acb5a1b927da712d58a924d52531d1a48efeb89cda46a49ebf7ac59c41b6`  
		Last Modified: Mon, 03 Jun 2024 19:19:59 GMT  
		Size: 4.3 MB (4286192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450a08c630325441489f21cd800611e9feb2492b8eb31f83a6594b2e40214cd8`  
		Last Modified: Mon, 03 Jun 2024 19:20:00 GMT  
		Size: 32.5 MB (32534782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bc626dd10091954b5146ae202f47df0ef7c9190b2af49d014e7c37442d81c04`  
		Last Modified: Mon, 03 Jun 2024 19:19:59 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb73719554076c9154225b52ae4b1ac65633f938a7b950a58de1e76b2214af0`  
		Last Modified: Mon, 03 Jun 2024 19:19:59 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed0c4b1398c8124d3e9ad0a3c189014d60c8b6bb3d1bfbb9bbc82648d90ee15d`  
		Last Modified: Mon, 03 Jun 2024 19:20:00 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:832b7439347fd01f72ea20bea12d776d2d231fd2f0cd9dd6cca60d666a42786d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2932821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e5f07bbbd77d6baf590d6679346f363e8f59f88c0674e3117ed9b93013e2565`

```dockerfile
```

-	Layers:
	-	`sha256:4b632f8757379f48ce7f62375be58317607752c05ca50bf0467970bc7732b8be`  
		Last Modified: Mon, 03 Jun 2024 19:19:59 GMT  
		Size: 2.9 MB (2917180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:445eff67ac2cb7aaefb9d6dacdc1618bc755d7897a207812ddec4de6bda2f483`  
		Last Modified: Mon, 03 Jun 2024 19:19:59 GMT  
		Size: 15.6 KB (15641 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.8.10` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:4fc1edca1f790b8ac9d5b2173aada3b9286d9682b37f283e782a7ec70bc7a7ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.5 MB (67544788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecb60de9eeaab7c013187a0bec5f7b0bba61e6e24218866965d49eda48c4cfb0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 14 May 2024 00:39:55 GMT
ADD file:0465ea1f0e8a2ee3e0f770c3b7f8e4a2b8719c624b440cabe7d7ecbe87200e7b in / 
# Tue, 14 May 2024 00:39:56 GMT
CMD ["bash"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:3a0037c67e2f4632684ea787f751ddb0b6af2b86113ab3b6859744b6eaf77e2f`  
		Last Modified: Tue, 14 May 2024 00:43:33 GMT  
		Size: 30.1 MB (30086908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a30d1c4ea046e3d2ec261eed89b6a11b07f27477f9db9937ea3d7f1bdf96770`  
		Last Modified: Mon, 03 Jun 2024 23:21:36 GMT  
		Size: 5.0 MB (5004067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1348b8e55237ade45f01834586e51a0102e0b2e5470aa9241f3c9d43d91d8184`  
		Last Modified: Mon, 03 Jun 2024 23:21:37 GMT  
		Size: 32.4 MB (32429418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53c860bd2e343ea246524ecfcdcddab5bc3be9ca2ca76cd5520f473af7ed08b6`  
		Last Modified: Mon, 03 Jun 2024 23:21:35 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6affc35b1b8deb8c68b2ed39088b6cb464a8c715cfeb13b98b7a46a71f363927`  
		Last Modified: Mon, 03 Jun 2024 23:21:35 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c827d71aec063d0b0ef29780a8713a8ba0922e75b119c6556079adf5b5f50db0`  
		Last Modified: Mon, 03 Jun 2024 23:21:36 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:88bd147fc6fc78aef40ad23875d03d99ea387bc6017d5da123c1af47f5330558
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2931017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a260c5f7ccad1cf371ec733de6364012ea0537067f6e5e706362301433f77928`

```dockerfile
```

-	Layers:
	-	`sha256:68619ec59da40fc071fc5498fd43d7726287e94a8b402bf77d0e477f09aa84cd`  
		Last Modified: Mon, 03 Jun 2024 23:21:36 GMT  
		Size: 2.9 MB (2915158 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6548bb1998e4b025532a832bdd2103900b776501e3c4d122ee707d7b0036c48`  
		Last Modified: Mon, 03 Jun 2024 23:21:35 GMT  
		Size: 15.9 KB (15859 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.8.10-alpine`

```console
$ docker pull chronograf@sha256:aeff6b0f33ad0c7163d0f15359676e3783b2c4f051277623bb87d3d8f525245b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.8.10-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:6901af16d25884590ef18c7cf6bc51e247e34e8db598d51aeac3a32686b96281
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23143191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fabb3a35dd209be242515d9abdb28872c03b6087716da9e68d7144ced10310b9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
CMD ["/bin/sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7135375e7e2b93794abc3a6fae771e0e810f1c985d87d5e2b116928c4a5811bb`  
		Last Modified: Mon, 03 Jun 2024 19:00:15 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7604efdcdfb5e914425082e913fa11feebc46f84efbd0eab4d63c026755d79f1`  
		Last Modified: Mon, 03 Jun 2024 19:00:14 GMT  
		Size: 292.4 KB (292422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed08262353aa43a044b72561106caeca51305919dbb951ad7fe4acfc2ad372f0`  
		Last Modified: Mon, 03 Jun 2024 19:00:15 GMT  
		Size: 19.2 MB (19204026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c69cc0629a8f4b4b5775f08d6212e7252bb99bc8b01e1d779a5306d8ce594551`  
		Last Modified: Mon, 03 Jun 2024 19:00:14 GMT  
		Size: 12.2 KB (12236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36c2b2e66b9548a4f932659927715ec1cabc2c5dd4425dd03f2b7185209ba8b9`  
		Last Modified: Mon, 03 Jun 2024 19:00:16 GMT  
		Size: 11.9 KB (11896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0910d626bd5a2723486bd6566ee32668ae861e7a1e18975ac98825605fefe14`  
		Last Modified: Mon, 03 Jun 2024 19:00:16 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8.10-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:e509b26098019dd58f191c86c4a74dae8e741425f72ae6bf2db1768e4eb80d54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.5 KB (233529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2a1345abbc1eb7303aad85d664a52c2b91b5a286113333875fd693f733f01db`

```dockerfile
```

-	Layers:
	-	`sha256:15f8d2f11400eec69f6ea0110c8ae1da088d7809dc0222f8354511b1bcef6a8a`  
		Last Modified: Mon, 03 Jun 2024 19:00:14 GMT  
		Size: 216.9 KB (216881 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f7394674c01a304ac4ca09c635793f21386d3fff6e6fe7b304eea2650beae68`  
		Last Modified: Mon, 03 Jun 2024 19:00:14 GMT  
		Size: 16.6 KB (16648 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.9`

```console
$ docker pull chronograf@sha256:26ed229b33ba93dd08529d1cb2fa1f0e3a9779dbc46c4f9eb26d2a516395dd7f
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
$ docker pull chronograf@sha256:d48dd5bb50d4ac61a8b59ebecf668ea1e2feeaacf7343244281da6ea1bc7335c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.5 MB (71490896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a39c95a93e60665df72ede9e81e772774df1f15ffb4eb658180d3b55d7979c32`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 14 May 2024 01:28:26 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
# Tue, 14 May 2024 01:28:27 GMT
CMD ["bash"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eebde8aef47f19c2494521f6728f1d46879b6d43cc65c98827665512e07d7180`  
		Last Modified: Mon, 03 Jun 2024 19:00:13 GMT  
		Size: 5.0 MB (5020989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e00d912bf834c33d1afc737541a1cf76b9081506517f1774f458d466e9ffc41`  
		Last Modified: Mon, 03 Jun 2024 19:00:14 GMT  
		Size: 35.0 MB (35011583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3eeecadf719e9963e96d74f691ceb64b4c1418f9fa747e119400c95abbe54fd`  
		Last Modified: Mon, 03 Jun 2024 19:00:13 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bb454410615e0774b4d45e276e61b6a3649df6671e61f1100e9e0f88b65090f`  
		Last Modified: Mon, 03 Jun 2024 19:00:13 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0dac812eb9441ab765eebaf54b6f990739097b38a7a8db888fee7eca4fea90c`  
		Last Modified: Mon, 03 Jun 2024 19:00:14 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9` - unknown; unknown

```console
$ docker pull chronograf@sha256:1a9f8f1cf63e156075b712b5fe0373693141e173dab5583b67edf0fd2e4610fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2934769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39d13481ad5f3aab793a30c5d6246a30614b6001ce2d98dbb2dbc149cabe306c`

```dockerfile
```

-	Layers:
	-	`sha256:902412b236e167bec25d36685579a7b81c96b4212b9ffe387674035c30fad596`  
		Last Modified: Mon, 03 Jun 2024 19:00:14 GMT  
		Size: 2.9 MB (2919202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61b704bbc2e583a9902028f29d0d69c9847f70e6a0150bc24a5415afb378d31b`  
		Last Modified: Mon, 03 Jun 2024 19:00:13 GMT  
		Size: 15.6 KB (15567 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.9` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:9c6b86dda96de22e604832a5ddd2f58e506ada7942e70d1d353ade7a2158e8c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.2 MB (64216478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ce22cf62b1c39c65c7c227d805a5a01f38971630f3d591d39d5d79900d94fc8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 14 May 2024 01:09:04 GMT
ADD file:b58f353e9d2a24c2c16ae0913b28705d3ecc439d60d82b5b4982780c59aae249 in / 
# Tue, 14 May 2024 01:09:04 GMT
CMD ["bash"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:a5c0b9604ae49509a7875b258d98493d63bdb4c1c27a70f2befa5fa4fcea1888`  
		Last Modified: Tue, 14 May 2024 01:13:30 GMT  
		Size: 26.6 MB (26594493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0b0acb5a1b927da712d58a924d52531d1a48efeb89cda46a49ebf7ac59c41b6`  
		Last Modified: Mon, 03 Jun 2024 19:19:59 GMT  
		Size: 4.3 MB (4286192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c973b433a6d09a2b89a3d96e521d53f98b101682b82ab0c6996d5ce529420678`  
		Last Modified: Mon, 03 Jun 2024 19:20:38 GMT  
		Size: 33.3 MB (33311392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:931ed93e0574e5724da44720f62eceeb0e477cd74e9526845e9a4301daa8fca8`  
		Last Modified: Mon, 03 Jun 2024 19:20:37 GMT  
		Size: 12.3 KB (12251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dcacd736a276704224b470cf71f1d0d35390a498255c5d9b15f12aca09aa201`  
		Last Modified: Mon, 03 Jun 2024 19:20:37 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f7a0e6863080b47c4f881da36d34c74790e1f71fab43a3a8de31d41d243a6b6`  
		Last Modified: Mon, 03 Jun 2024 19:20:38 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9` - unknown; unknown

```console
$ docker pull chronograf@sha256:29e131f4180a9c90f0b2c88d781f7ba5c54c113391e65981ce390e25271766f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2937106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7a3fe4bcf96203ed481cc6ba8be0c85dd78fafd39f9cd7f72c5d8547cb910b6`

```dockerfile
```

-	Layers:
	-	`sha256:93fa1ccd40bf860f3b8714ca6536871e601405643f3ea1ba326c9f09fe8422ef`  
		Last Modified: Mon, 03 Jun 2024 19:20:37 GMT  
		Size: 2.9 MB (2921472 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e0dd759ae5dade5ebbd26e335c5c5179d03f90dab24e1c159e85825708881f2`  
		Last Modified: Mon, 03 Jun 2024 19:20:37 GMT  
		Size: 15.6 KB (15634 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.9` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:e79d8149aa77e9e372d25e3fb89f02141683c0603e17d796746fec1a5b224277
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.3 MB (68296839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95fdf77837ea2772cec9dead38ab95ab8b9f59900036fce135644ac813fdc1e3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 14 May 2024 00:39:55 GMT
ADD file:0465ea1f0e8a2ee3e0f770c3b7f8e4a2b8719c624b440cabe7d7ecbe87200e7b in / 
# Tue, 14 May 2024 00:39:56 GMT
CMD ["bash"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:3a0037c67e2f4632684ea787f751ddb0b6af2b86113ab3b6859744b6eaf77e2f`  
		Last Modified: Tue, 14 May 2024 00:43:33 GMT  
		Size: 30.1 MB (30086908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a30d1c4ea046e3d2ec261eed89b6a11b07f27477f9db9937ea3d7f1bdf96770`  
		Last Modified: Mon, 03 Jun 2024 23:21:36 GMT  
		Size: 5.0 MB (5004067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34f0525e0f164cc7950b023dca0f0104fff90fb497193be6a351efa4283f079b`  
		Last Modified: Mon, 03 Jun 2024 23:52:24 GMT  
		Size: 33.2 MB (33181466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f483fb720b7db44ab6c6e8b9e8d6e6bdfab0590927004dc1dd9565b00c483298`  
		Last Modified: Mon, 03 Jun 2024 23:52:22 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05c0477d2bb66027767dc6d418161a42d0b99fd4a99f8069e209d344d5692c5b`  
		Last Modified: Mon, 03 Jun 2024 23:52:23 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2d9e3bc45164d83c58abf43d2b72c97277fc3d8b0e2ede6fc61750abec97ecb`  
		Last Modified: Mon, 03 Jun 2024 23:52:23 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9` - unknown; unknown

```console
$ docker pull chronograf@sha256:991dc39a57e51fc0b11883586cba827d44972f6e06a31807b666fba4a2bc684f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2935299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbe6aa92ef98f335791098e66a4998e48a990116b9f40bcef6e465fbc95c9896`

```dockerfile
```

-	Layers:
	-	`sha256:1bff86fc31dda38c9962e53608c57200f3fd27c32f540f63e91f629459b67614`  
		Last Modified: Mon, 03 Jun 2024 23:52:23 GMT  
		Size: 2.9 MB (2919450 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:271fd9dcd762b186ff6e233308cd11a994ef55651f42a4328d37edc3bd997a00`  
		Last Modified: Mon, 03 Jun 2024 23:52:23 GMT  
		Size: 15.8 KB (15849 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.9-alpine`

```console
$ docker pull chronograf@sha256:4b387cd5abb5c4edf5ff7f449886c0b639d79aea15126cd2803af5273be66311
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.9-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:b024857b0a53699ca0cad01569dea1afa1611459ac1b391db87f766880e3f118
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23611241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7614fb2d6f19684100cbd8399c97243cfc34d1726acb7d1a377821d9db961936`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
CMD ["/bin/sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec4b899bd7765ff7f024156013a60645642a8d8410290dd6b529e9f936235eb5`  
		Last Modified: Mon, 03 Jun 2024 19:00:01 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6c47b68fae599b34128310d83189330caf17d6e6fdfcc1cacbdd32267e0ae42`  
		Last Modified: Mon, 03 Jun 2024 19:00:01 GMT  
		Size: 292.4 KB (292430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41685855cc4143b0f365fc5044bdf6223bff2af6dc57c216fcef4a95b50b01ef`  
		Last Modified: Mon, 03 Jun 2024 19:00:01 GMT  
		Size: 19.7 MB (19672068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73e45b2a86e01d139c7d17f449fa1384f1e526e2edde32d57bd93c0a1f4eccff`  
		Last Modified: Mon, 03 Jun 2024 19:00:01 GMT  
		Size: 12.2 KB (12237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2ecf24fc9eb6f8609cefdd0b3052ce939f62a8fdb02ba99938d5c002b59c9cf`  
		Last Modified: Mon, 03 Jun 2024 19:00:02 GMT  
		Size: 11.9 KB (11895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450b96b549cc85c4e767722042711a38adf3c74af9d3ce9e9e979c7a3d272dca`  
		Last Modified: Mon, 03 Jun 2024 19:00:02 GMT  
		Size: 237.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:9a13b6067af2556aa442e647412bccffdff3b8cea9a45074dea4db6ee1bc064d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.8 KB (237820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b1a49d5661190b467bd3d435f136d258f21a63140cb24416d434a0d47db09f4`

```dockerfile
```

-	Layers:
	-	`sha256:e1ecf37f9c69a9603213851b2aa836e8ab0c2b20d7598093c6e0090e83c8c1e3`  
		Last Modified: Mon, 03 Jun 2024 19:00:01 GMT  
		Size: 221.2 KB (221175 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:336e29c57bb46d2b50c1ddbae6313a58fa48f48b52d575c8731648e2925c181a`  
		Last Modified: Mon, 03 Jun 2024 19:00:01 GMT  
		Size: 16.6 KB (16645 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.9.4`

```console
$ docker pull chronograf@sha256:26ed229b33ba93dd08529d1cb2fa1f0e3a9779dbc46c4f9eb26d2a516395dd7f
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
$ docker pull chronograf@sha256:d48dd5bb50d4ac61a8b59ebecf668ea1e2feeaacf7343244281da6ea1bc7335c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.5 MB (71490896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a39c95a93e60665df72ede9e81e772774df1f15ffb4eb658180d3b55d7979c32`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 14 May 2024 01:28:26 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
# Tue, 14 May 2024 01:28:27 GMT
CMD ["bash"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eebde8aef47f19c2494521f6728f1d46879b6d43cc65c98827665512e07d7180`  
		Last Modified: Mon, 03 Jun 2024 19:00:13 GMT  
		Size: 5.0 MB (5020989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e00d912bf834c33d1afc737541a1cf76b9081506517f1774f458d466e9ffc41`  
		Last Modified: Mon, 03 Jun 2024 19:00:14 GMT  
		Size: 35.0 MB (35011583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3eeecadf719e9963e96d74f691ceb64b4c1418f9fa747e119400c95abbe54fd`  
		Last Modified: Mon, 03 Jun 2024 19:00:13 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bb454410615e0774b4d45e276e61b6a3649df6671e61f1100e9e0f88b65090f`  
		Last Modified: Mon, 03 Jun 2024 19:00:13 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0dac812eb9441ab765eebaf54b6f990739097b38a7a8db888fee7eca4fea90c`  
		Last Modified: Mon, 03 Jun 2024 19:00:14 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9.4` - unknown; unknown

```console
$ docker pull chronograf@sha256:1a9f8f1cf63e156075b712b5fe0373693141e173dab5583b67edf0fd2e4610fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2934769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39d13481ad5f3aab793a30c5d6246a30614b6001ce2d98dbb2dbc149cabe306c`

```dockerfile
```

-	Layers:
	-	`sha256:902412b236e167bec25d36685579a7b81c96b4212b9ffe387674035c30fad596`  
		Last Modified: Mon, 03 Jun 2024 19:00:14 GMT  
		Size: 2.9 MB (2919202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61b704bbc2e583a9902028f29d0d69c9847f70e6a0150bc24a5415afb378d31b`  
		Last Modified: Mon, 03 Jun 2024 19:00:13 GMT  
		Size: 15.6 KB (15567 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.9.4` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:9c6b86dda96de22e604832a5ddd2f58e506ada7942e70d1d353ade7a2158e8c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.2 MB (64216478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ce22cf62b1c39c65c7c227d805a5a01f38971630f3d591d39d5d79900d94fc8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 14 May 2024 01:09:04 GMT
ADD file:b58f353e9d2a24c2c16ae0913b28705d3ecc439d60d82b5b4982780c59aae249 in / 
# Tue, 14 May 2024 01:09:04 GMT
CMD ["bash"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:a5c0b9604ae49509a7875b258d98493d63bdb4c1c27a70f2befa5fa4fcea1888`  
		Last Modified: Tue, 14 May 2024 01:13:30 GMT  
		Size: 26.6 MB (26594493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0b0acb5a1b927da712d58a924d52531d1a48efeb89cda46a49ebf7ac59c41b6`  
		Last Modified: Mon, 03 Jun 2024 19:19:59 GMT  
		Size: 4.3 MB (4286192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c973b433a6d09a2b89a3d96e521d53f98b101682b82ab0c6996d5ce529420678`  
		Last Modified: Mon, 03 Jun 2024 19:20:38 GMT  
		Size: 33.3 MB (33311392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:931ed93e0574e5724da44720f62eceeb0e477cd74e9526845e9a4301daa8fca8`  
		Last Modified: Mon, 03 Jun 2024 19:20:37 GMT  
		Size: 12.3 KB (12251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dcacd736a276704224b470cf71f1d0d35390a498255c5d9b15f12aca09aa201`  
		Last Modified: Mon, 03 Jun 2024 19:20:37 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f7a0e6863080b47c4f881da36d34c74790e1f71fab43a3a8de31d41d243a6b6`  
		Last Modified: Mon, 03 Jun 2024 19:20:38 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9.4` - unknown; unknown

```console
$ docker pull chronograf@sha256:29e131f4180a9c90f0b2c88d781f7ba5c54c113391e65981ce390e25271766f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2937106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7a3fe4bcf96203ed481cc6ba8be0c85dd78fafd39f9cd7f72c5d8547cb910b6`

```dockerfile
```

-	Layers:
	-	`sha256:93fa1ccd40bf860f3b8714ca6536871e601405643f3ea1ba326c9f09fe8422ef`  
		Last Modified: Mon, 03 Jun 2024 19:20:37 GMT  
		Size: 2.9 MB (2921472 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e0dd759ae5dade5ebbd26e335c5c5179d03f90dab24e1c159e85825708881f2`  
		Last Modified: Mon, 03 Jun 2024 19:20:37 GMT  
		Size: 15.6 KB (15634 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.9.4` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:e79d8149aa77e9e372d25e3fb89f02141683c0603e17d796746fec1a5b224277
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.3 MB (68296839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95fdf77837ea2772cec9dead38ab95ab8b9f59900036fce135644ac813fdc1e3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 14 May 2024 00:39:55 GMT
ADD file:0465ea1f0e8a2ee3e0f770c3b7f8e4a2b8719c624b440cabe7d7ecbe87200e7b in / 
# Tue, 14 May 2024 00:39:56 GMT
CMD ["bash"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:3a0037c67e2f4632684ea787f751ddb0b6af2b86113ab3b6859744b6eaf77e2f`  
		Last Modified: Tue, 14 May 2024 00:43:33 GMT  
		Size: 30.1 MB (30086908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a30d1c4ea046e3d2ec261eed89b6a11b07f27477f9db9937ea3d7f1bdf96770`  
		Last Modified: Mon, 03 Jun 2024 23:21:36 GMT  
		Size: 5.0 MB (5004067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34f0525e0f164cc7950b023dca0f0104fff90fb497193be6a351efa4283f079b`  
		Last Modified: Mon, 03 Jun 2024 23:52:24 GMT  
		Size: 33.2 MB (33181466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f483fb720b7db44ab6c6e8b9e8d6e6bdfab0590927004dc1dd9565b00c483298`  
		Last Modified: Mon, 03 Jun 2024 23:52:22 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05c0477d2bb66027767dc6d418161a42d0b99fd4a99f8069e209d344d5692c5b`  
		Last Modified: Mon, 03 Jun 2024 23:52:23 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2d9e3bc45164d83c58abf43d2b72c97277fc3d8b0e2ede6fc61750abec97ecb`  
		Last Modified: Mon, 03 Jun 2024 23:52:23 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9.4` - unknown; unknown

```console
$ docker pull chronograf@sha256:991dc39a57e51fc0b11883586cba827d44972f6e06a31807b666fba4a2bc684f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2935299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbe6aa92ef98f335791098e66a4998e48a990116b9f40bcef6e465fbc95c9896`

```dockerfile
```

-	Layers:
	-	`sha256:1bff86fc31dda38c9962e53608c57200f3fd27c32f540f63e91f629459b67614`  
		Last Modified: Mon, 03 Jun 2024 23:52:23 GMT  
		Size: 2.9 MB (2919450 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:271fd9dcd762b186ff6e233308cd11a994ef55651f42a4328d37edc3bd997a00`  
		Last Modified: Mon, 03 Jun 2024 23:52:23 GMT  
		Size: 15.8 KB (15849 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.9.4-alpine`

```console
$ docker pull chronograf@sha256:4b387cd5abb5c4edf5ff7f449886c0b639d79aea15126cd2803af5273be66311
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.9.4-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:b024857b0a53699ca0cad01569dea1afa1611459ac1b391db87f766880e3f118
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23611241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7614fb2d6f19684100cbd8399c97243cfc34d1726acb7d1a377821d9db961936`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
CMD ["/bin/sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec4b899bd7765ff7f024156013a60645642a8d8410290dd6b529e9f936235eb5`  
		Last Modified: Mon, 03 Jun 2024 19:00:01 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6c47b68fae599b34128310d83189330caf17d6e6fdfcc1cacbdd32267e0ae42`  
		Last Modified: Mon, 03 Jun 2024 19:00:01 GMT  
		Size: 292.4 KB (292430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41685855cc4143b0f365fc5044bdf6223bff2af6dc57c216fcef4a95b50b01ef`  
		Last Modified: Mon, 03 Jun 2024 19:00:01 GMT  
		Size: 19.7 MB (19672068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73e45b2a86e01d139c7d17f449fa1384f1e526e2edde32d57bd93c0a1f4eccff`  
		Last Modified: Mon, 03 Jun 2024 19:00:01 GMT  
		Size: 12.2 KB (12237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2ecf24fc9eb6f8609cefdd0b3052ce939f62a8fdb02ba99938d5c002b59c9cf`  
		Last Modified: Mon, 03 Jun 2024 19:00:02 GMT  
		Size: 11.9 KB (11895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450b96b549cc85c4e767722042711a38adf3c74af9d3ce9e9e979c7a3d272dca`  
		Last Modified: Mon, 03 Jun 2024 19:00:02 GMT  
		Size: 237.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9.4-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:9a13b6067af2556aa442e647412bccffdff3b8cea9a45074dea4db6ee1bc064d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.8 KB (237820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b1a49d5661190b467bd3d435f136d258f21a63140cb24416d434a0d47db09f4`

```dockerfile
```

-	Layers:
	-	`sha256:e1ecf37f9c69a9603213851b2aa836e8ab0c2b20d7598093c6e0090e83c8c1e3`  
		Last Modified: Mon, 03 Jun 2024 19:00:01 GMT  
		Size: 221.2 KB (221175 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:336e29c57bb46d2b50c1ddbae6313a58fa48f48b52d575c8731648e2925c181a`  
		Last Modified: Mon, 03 Jun 2024 19:00:01 GMT  
		Size: 16.6 KB (16645 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:alpine`

```console
$ docker pull chronograf@sha256:0a4afb73e2d3a91a06e36601c0b8c9c18e5aeb825e8edcceb9d18e338a0e0203
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:b55598a8b3ee7feb689bcb380dc0f234d328f2eb47c881346dc30b481bb81f1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31807875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b40200ab7f22ab99c0b92e31ce0a9ef862bfd80a2efa3813ebad5e2bdf598f9b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
CMD ["/bin/sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
RUN apk add --no-cache ca-certificates su-exec &&     update-ca-certificates # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.10.5
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S chronograf &&     adduser -S chronograf -G chronograf &&     mkdir -m 0750 -p /var/lib/chronograf &&     chown chronograf:chronograf /var/lib/chronograf # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a541091e90e8b5010bc3e6964324ac4919c24be8f5fb5653082302eec5fc1ec4`  
		Last Modified: Mon, 03 Jun 2024 19:00:15 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d70bae9f6b1c0feca8cb0ba973e7e28953ffa5a9d62cfbfcd897abd2d016af8`  
		Last Modified: Mon, 03 Jun 2024 19:00:16 GMT  
		Size: 294.3 KB (294348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27b085bda50e0c5e25c7a4ebec7e1ccd7ae22a5c76ef00439f8b7c4d022b38fb`  
		Last Modified: Mon, 03 Jun 2024 19:00:16 GMT  
		Size: 27.9 MB (27866729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1990a674718757fef7810e42e4c5340c248ad43f1d9abdec7439e5b9cd01723`  
		Last Modified: Mon, 03 Jun 2024 19:00:15 GMT  
		Size: 12.2 KB (12237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14e68549b54b63067c056976b55d6c93ac1866dcad3a2e1dde832662e2da39f8`  
		Last Modified: Mon, 03 Jun 2024 19:00:16 GMT  
		Size: 11.9 KB (11896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9edb80f2e5c4143929355c91c8f989dafdbea5bce4a5e2c628198ab81d0e456e`  
		Last Modified: Mon, 03 Jun 2024 19:00:16 GMT  
		Size: 292.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:27b4cb11ebf88b4475e41a68de08386fcb61342e61fff5f48ad3b929f482634f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.5 KB (244494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65197df914a82b3f2f03ba701ae27857bf44eff66c30c4cf0b573d7eda631965`

```dockerfile
```

-	Layers:
	-	`sha256:ca5768a37193228f1c8c19dcb7236caefe2d82d164db3e45a19eea54e191d717`  
		Last Modified: Mon, 03 Jun 2024 19:00:15 GMT  
		Size: 226.9 KB (226903 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe809aec848a51e9dedbd725ce359b20a0efb4f28696cc4188181514e5202eac`  
		Last Modified: Mon, 03 Jun 2024 19:00:15 GMT  
		Size: 17.6 KB (17591 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:latest`

```console
$ docker pull chronograf@sha256:cf6bab04e7f150c1ecae89c8e94de6873be3b146e71803d992ac46ad73cf0c5a
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
$ docker pull chronograf@sha256:5f5537b449b3f8035637e4ce9eb6d4720ced46f8db9d4e2c13c95be6f1ac7be9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.1 MB (84069434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45996034df2c6fe446e5e2fd0aa29d585534c107ab461bba710b9e9e2a59446d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 14 May 2024 01:28:03 GMT
ADD file:5aaace706aa00ff97d243daa2c29f5de88f124e1b97c570634f16eef90783286 in / 
# Tue, 14 May 2024 01:28:04 GMT
CMD ["bash"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.10.5
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:09f376ebb190216b0459f470e71bec7b5dfa611d66bf008492b40dcc5f1d8eae`  
		Last Modified: Tue, 14 May 2024 01:32:30 GMT  
		Size: 29.2 MB (29150411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8f47b768815e9c2366c46a8534a57f09e4f6f0ff4b0b52b64ba601dc9a9c174`  
		Last Modified: Mon, 03 Jun 2024 19:00:29 GMT  
		Size: 7.7 MB (7676940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9489fbf683135fcfa140c8d0a17e9d550c173fc3a052bc84f9f267f99252cf48`  
		Last Modified: Mon, 03 Jun 2024 19:00:31 GMT  
		Size: 47.2 MB (47217627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ed019f6b0534dfea3bfb7a969d8574f9df636506f6f19524b92326e37d2ada2`  
		Last Modified: Mon, 03 Jun 2024 19:00:28 GMT  
		Size: 12.2 KB (12241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb7ab6f5f28a95f1a3f7d8c842fdfc39c48d986d7d2fc301067f3717612a58d4`  
		Last Modified: Mon, 03 Jun 2024 19:00:28 GMT  
		Size: 11.9 KB (11900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af934b4bf874818dedfe49e86bee37a24e98cfb0e261bef354508666419f1249`  
		Last Modified: Mon, 03 Jun 2024 19:00:30 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:c109af0e26df5eea8f474e65c0139dbb1f2441db69a8534d6e4d0c20f1eebaa6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2671399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d7cf432a9a5718d9f6b2250ab83415c141962d8a0deb4e8a169e459aff78d57`

```dockerfile
```

-	Layers:
	-	`sha256:c3d8929c831b697a62dc9682fd7ae7044d6cd8342004667d41fd27a573432ef3`  
		Last Modified: Mon, 03 Jun 2024 19:00:29 GMT  
		Size: 2.7 MB (2655514 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3661947447bdb2d0b40fbad7fa348a99abb8e7e835a3351efddc4c57262a0019`  
		Last Modified: Mon, 03 Jun 2024 19:00:28 GMT  
		Size: 15.9 KB (15885 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:latest` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:1a460b0bc194e24766aea7533b5cb8d0b916e7f6a09f4ef955743cbbb2a3d430
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.3 MB (75343302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fd2dc826fb7082fc62609abbeac1458117fce816a079a2e66b02f714e7625b3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 14 May 2024 01:08:45 GMT
ADD file:e170e8e24c36eb1a1a24d68a97cd2a7784d689387d804630dc7b596551d91090 in / 
# Tue, 14 May 2024 01:08:45 GMT
CMD ["bash"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.10.5
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:3b9aff019fd47145a0f08828c4c912b901596e71f6dbe2367a7a098e8882ef55`  
		Last Modified: Tue, 14 May 2024 01:12:45 GMT  
		Size: 24.7 MB (24740205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8351e2a7bec99074c9b2552b2d42aabba4fff0d39db3d0ba9b68a404136d1453`  
		Last Modified: Mon, 03 Jun 2024 19:21:37 GMT  
		Size: 6.3 MB (6301009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ecd35a42c7fd3bb3846a30c6d03f105a7b0004871c712048da35ad37776b89a`  
		Last Modified: Mon, 03 Jun 2024 19:21:38 GMT  
		Size: 44.3 MB (44277619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c6834d5d76602cbf35137f057e581f58279ed2341c8d70ea3c43059d1e869aa`  
		Last Modified: Mon, 03 Jun 2024 19:21:37 GMT  
		Size: 12.2 KB (12244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a1ff0b1eeee3067ebbfb12a9699f51e68c235bba7025e052f468ff25d8a0a8e`  
		Last Modified: Mon, 03 Jun 2024 19:21:37 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c88710b32ff5bef236a642c6ffa7546c65aafb1a9703ec9aa5584b140c831f8e`  
		Last Modified: Mon, 03 Jun 2024 19:21:38 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:80c599174d5b9b187f9c7428801ab128e6596094361cbaf40235d64ed9cb9168
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2673769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9a7de8a8b42ee3697139c5dc16ce57f52de462a641be9a93075c7416c83c588`

```dockerfile
```

-	Layers:
	-	`sha256:912fd66c49cdd7f7ba8e22dc0f03fa2098c87be72f0f8e38c2d13d2dea925230`  
		Last Modified: Mon, 03 Jun 2024 19:21:37 GMT  
		Size: 2.7 MB (2657810 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de523748666f12dea6e03853effe8f169d72dbd26d1ddcb7bb613ac802d32c6b`  
		Last Modified: Mon, 03 Jun 2024 19:21:37 GMT  
		Size: 16.0 KB (15959 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:latest` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:56fc9a7d7b5e4129e88ff15e6e3f443c62536180fba87c675a42fce7c1e2a205
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.6 MB (81628060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06be28a02b74fac1638579f669127787c0ed3809f3587e6af1cf9b7761558b79`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 14 May 2024 00:39:40 GMT
ADD file:e23ba17afc7850bcca9e73ba5022db9f0a80c6a0250585fd3f50a1960226474b in / 
# Tue, 14 May 2024 00:39:41 GMT
CMD ["bash"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.10.5
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:24c63b8dcb66721062f32b893ef1027404afddd62aade87f3f39a3a6e70a74d0`  
		Last Modified: Tue, 14 May 2024 00:42:56 GMT  
		Size: 29.2 MB (29179503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d41ef92593599be99b703585f08f0f9d449d437aa1a40c01770b9496e36d09aa`  
		Last Modified: Tue, 04 Jun 2024 00:30:46 GMT  
		Size: 7.5 MB (7453158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:242a93b9d52597004cac704e713b2296dc4c9e12747f37ef26bfc754a8185575`  
		Last Modified: Tue, 04 Jun 2024 00:30:47 GMT  
		Size: 45.0 MB (44970929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:587e2528d7bd8b04b6611e9bf599ba3bd5f715852109189a0e3083d0cd3ab8ac`  
		Last Modified: Tue, 04 Jun 2024 00:30:45 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b63360a3869dd2324b9afc69220fdd9ab679f048bf48e30222b3a33d9f2131c`  
		Last Modified: Tue, 04 Jun 2024 00:30:46 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f61f348ae95890e7ffe175821d70d36dff6cbf8a1090acb513be2054d1fdd14e`  
		Last Modified: Tue, 04 Jun 2024 00:30:46 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:83948834d4691d46e4700a9818e255dd94a223e116a82e35c3c507e2e1c660e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2671968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:719c7373785b7461f4782337be23d22796be7338f526f53a70360d9da6da9c55`

```dockerfile
```

-	Layers:
	-	`sha256:cac0bb0a71f4dcd5eb86f11e418d44546f1e35f9eeaad8c1e730b1a5e36e20a1`  
		Last Modified: Tue, 04 Jun 2024 00:30:46 GMT  
		Size: 2.7 MB (2655786 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d43bed1639b69a3e0de48c7b22f9418945ed030c68b8f871ed9ab7743ea403f`  
		Last Modified: Tue, 04 Jun 2024 00:30:46 GMT  
		Size: 16.2 KB (16182 bytes)  
		MIME: application/vnd.in-toto+json
