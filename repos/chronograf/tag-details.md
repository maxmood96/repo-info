<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `chronograf`

-	[`chronograf:1.10`](#chronograf110)
-	[`chronograf:1.10-alpine`](#chronograf110-alpine)
-	[`chronograf:1.10.8`](#chronograf1108)
-	[`chronograf:1.10.8-alpine`](#chronograf1108-alpine)
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
$ docker pull chronograf@sha256:9f0069d5e74770b48d357f8007df8068ccb20353ae1cd9b1d3c68712d34c37b7
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
$ docker pull chronograf@sha256:8e22ca42eca51af0770099dfd8d36924a51de213c107c50286aedb5a9fecb1e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.4 MB (85408161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3285e8978ea95e807515b6f3f620464e98d8386928a0973148decdf52c0ef5f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 15 Aug 2025 14:37:23 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1760918400'
# Fri, 15 Aug 2025 14:37:23 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENV CHRONOGRAF_VERSION=1.10.8
# Fri, 15 Aug 2025 14:37:23 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 15 Aug 2025 14:37:23 GMT
VOLUME [/var/lib/chronograf]
# Fri, 15 Aug 2025 14:37:23 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:abe1fea375429ba91b23776f15f53da4ed790fa2b779b40d20f21e69bd66de5a`  
		Last Modified: Tue, 21 Oct 2025 00:19:19 GMT  
		Size: 28.2 MB (28228321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d678f7ea98bc9cde3cdc6f3822daf66c286a55145d5059c1ab6c170401471c4`  
		Last Modified: Tue, 21 Oct 2025 01:43:32 GMT  
		Size: 7.9 MB (7878755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1823d4badf365aba7b0fd3f98cff8b0abaff5803f47b8d57fbaeeb656471aaba`  
		Last Modified: Tue, 21 Oct 2025 01:43:41 GMT  
		Size: 49.3 MB (49276618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7715f277f40ad8ce01cbe83aa480fed068eb208132e1f1fd18dfec1ad82db60`  
		Last Modified: Tue, 21 Oct 2025 01:43:32 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:612be43be9a1667d3407539a10d5ac2ee077fa118ee89b45931f0c208c3807bf`  
		Last Modified: Tue, 21 Oct 2025 01:43:32 GMT  
		Size: 11.9 KB (11903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d40e348cd71352ccc887adef3c8508b00e9365e7eb81c4a82f557bfca578293`  
		Last Modified: Tue, 21 Oct 2025 01:43:32 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:ad8cbe492cda8ed466b5bfceee4c067234a11ad5d563254ca2ef0464fcdca1f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2870202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8ab40ab435551a74d356b54da4e19abedd945d17b41755c881256ead253ab52`

```dockerfile
```

-	Layers:
	-	`sha256:0b5d752ece03c44d95a557c603adf74579763ef225bb2cbfe38468b0e2b15134`  
		Last Modified: Tue, 21 Oct 2025 09:38:25 GMT  
		Size: 2.9 MB (2854074 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ceda444489ed6780403e9c2aadba05d5c2b42a2cc6307f16d07c466c2d98ec52`  
		Last Modified: Tue, 21 Oct 2025 09:38:25 GMT  
		Size: 16.1 KB (16128 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.10` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:1eb13a30653187377adf857362ebf6ad28bb1be8b6dce31f702e7a85f76ab352
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76088345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f743908bb2d47bfb245efff0d344b461c09d68649b31deaf8e14796c39b60af6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 15 Aug 2025 14:37:23 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1760918400'
# Fri, 15 Aug 2025 14:37:23 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENV CHRONOGRAF_VERSION=1.10.8
# Fri, 15 Aug 2025 14:37:23 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 15 Aug 2025 14:37:23 GMT
VOLUME [/var/lib/chronograf]
# Fri, 15 Aug 2025 14:37:23 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:4f520125372ffa3e5f64f19eebfdfce1c8314446e9e3ab2629f5c13cacbd8345`  
		Last Modified: Tue, 21 Oct 2025 00:20:18 GMT  
		Size: 23.9 MB (23934023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9b9cbeab7d89257c02df3df623dbb0db0b03ff0dacad804425d03c0c6bc538f`  
		Last Modified: Tue, 21 Oct 2025 02:48:15 GMT  
		Size: 6.5 MB (6508047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:483e264e639c89e02d166ec79b2c1a646f8a597f6b7f64e075012186ba1f257e`  
		Last Modified: Tue, 21 Oct 2025 02:48:18 GMT  
		Size: 45.6 MB (45621809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e30658b9289a25d89d66fd38b677bf33aab69f2b04e80a707c57437215f1ef49`  
		Last Modified: Tue, 21 Oct 2025 02:48:14 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47956f4970e0f490a78bc21edeef2c2c72c756000f50b21c9644801538fef1e1`  
		Last Modified: Tue, 21 Oct 2025 02:48:14 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13da7c92b57d7e1af6e5c05141a0cccdae906f9f905eac3ba3a2c2d11cc0ea83`  
		Last Modified: Tue, 21 Oct 2025 02:48:14 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:eb3600838cbf523178cf02ba62cddb9aeb6954442b16f7b3199129ebc555a75e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2872584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68df4bb273f5e075b878118d7f75b73f44394c9cbdcf0168a86f5d0bbc5cee15`

```dockerfile
```

-	Layers:
	-	`sha256:76f5f9bb4a19323ff3e5bbf4ebe978240554408deb1602b69c9585473d403666`  
		Last Modified: Tue, 21 Oct 2025 09:38:29 GMT  
		Size: 2.9 MB (2856371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f68f79b94989765e47276910de76c69663b987742ad04584fe7b0dd6009a761b`  
		Last Modified: Tue, 21 Oct 2025 09:38:30 GMT  
		Size: 16.2 KB (16213 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.10` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:113b7e3cac741fa1e3247a9cae8b958bd60881497da3522ca371fe48300a5b74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.9 MB (82885222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78be669f8c5ec34a56c042c2f6039c64076f1fcc76c54bf1fa5d924777de9fec`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 15 Aug 2025 14:37:23 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1760918400'
# Fri, 15 Aug 2025 14:37:23 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENV CHRONOGRAF_VERSION=1.10.8
# Fri, 15 Aug 2025 14:37:23 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 15 Aug 2025 14:37:23 GMT
VOLUME [/var/lib/chronograf]
# Fri, 15 Aug 2025 14:37:23 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:21b7accdc53fc02b56a5c1cccd412be04189e5a5e674fd092ffbedc72596be91`  
		Last Modified: Tue, 21 Oct 2025 00:18:57 GMT  
		Size: 28.1 MB (28102190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57847360efefbe97c6032227969a42bcd11fb0de5f8a7c988562801256856d9c`  
		Last Modified: Tue, 21 Oct 2025 01:47:59 GMT  
		Size: 7.7 MB (7691784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24a918b13d7ee929fee3564b1f4a8fa48e9589b846d399d39bd00bd3706efc80`  
		Last Modified: Tue, 21 Oct 2025 01:48:04 GMT  
		Size: 47.1 MB (47066776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:374fd9f33dcbadd2f16dfbc41a0a6ff13c7d47122d503c0c2d2fbd5c0ee89402`  
		Last Modified: Tue, 21 Oct 2025 01:47:59 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb2ed856870944b103a5a36bde6d94fadae3f7c49b1b938759b5c11771bfce7d`  
		Last Modified: Tue, 21 Oct 2025 01:47:59 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b769d03b89d7173d3468a7148bdaeaabb6283887b02bc55d9cee4c147439578`  
		Last Modified: Tue, 21 Oct 2025 01:48:00 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:6b186910c1614e00ad47ee34f42fc5e5f377e0a3cd954e6db6f6297b3d5f7517
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2870582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3d006836f764de414f23cfb6ab70e4c70e43facebc9d32443ba15b850a72b37`

```dockerfile
```

-	Layers:
	-	`sha256:f966f9b47cbb4657cec2c202c92f1d51d230717ec1a948e8f76fa115c46f1c8b`  
		Last Modified: Tue, 21 Oct 2025 09:38:34 GMT  
		Size: 2.9 MB (2854347 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e91722f76a858459622d6a244a19d8ed86fe848ae9085cb9902257a44a8387fd`  
		Last Modified: Tue, 21 Oct 2025 09:38:35 GMT  
		Size: 16.2 KB (16235 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.10-alpine`

```console
$ docker pull chronograf@sha256:efc72c285cae492b0fb820a7794f2da69a70ef77caa8d28282e0df6f79856029
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.10-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:08463b31a0a2617a51e230161f997b525214640155e291a423ae53004330c719
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.7 MB (32700225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8af178eb7af41f52d85b69957fc583d381f6a24a9e604b40818766ecf3004a1a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 15 Aug 2025 14:37:23 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["/bin/sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
RUN apk add --no-cache ca-certificates setpriv &&     update-ca-certificates # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENV CHRONOGRAF_VERSION=1.10.8
# Fri, 15 Aug 2025 14:37:23 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S chronograf &&     adduser -S chronograf -G chronograf &&     mkdir -m 0750 -p /var/lib/chronograf &&     chown chronograf:chronograf /var/lib/chronograf # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 15 Aug 2025 14:37:23 GMT
VOLUME [/var/lib/chronograf]
# Fri, 15 Aug 2025 14:37:23 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f08cd1461c07b6d2b803ff1e365582cea280da85884cb0fe20c1b539046e9c0f`  
		Last Modified: Wed, 08 Oct 2025 23:01:28 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:642952c8832a913bc8124d8c1f9800b4c40ed32aa2d21f4bbd9c85e32729fdf2`  
		Last Modified: Wed, 08 Oct 2025 23:01:28 GMT  
		Size: 314.6 KB (314639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff188fbd44ef51d6c15c61b590915a7d108294cea3cebd1224f569cf88dbfbd2`  
		Last Modified: Wed, 08 Oct 2025 23:01:31 GMT  
		Size: 28.6 MB (28558408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ada6ea712a91804f080e3ac3a6fec72f1bf330d8affb0a76902b1f0b78a5046`  
		Last Modified: Wed, 08 Oct 2025 23:01:28 GMT  
		Size: 12.2 KB (12237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:322d214c5daa6878e468360de897da9cd0cad1be05283f5529b5e2ce07c9e72f`  
		Last Modified: Wed, 08 Oct 2025 23:01:28 GMT  
		Size: 11.9 KB (11895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:175f9d62a6d73ab836332ca97429aec6104967dc35d5ab6aaa103f374c1539bd`  
		Last Modified: Wed, 08 Oct 2025 23:01:28 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:dd3236bd7a2263357f0c7258a9a36c7fef283fd9f58f17f5fc2cbfa8330df313
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.2 KB (268238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:808a56c94ce865ff68fe325760f90b15b31758031ea028455935f57e4d2afe56`

```dockerfile
```

-	Layers:
	-	`sha256:d62aac69b78bc656cc8510a0566537353a4cda897cdaf124ca24ad68c0fa7fb1`  
		Last Modified: Thu, 09 Oct 2025 00:38:17 GMT  
		Size: 250.4 KB (250383 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c7ffc31e817e3fff1eade663dcae6dc3da5bb4370e43abaf921eebc9dd7f0a1`  
		Last Modified: Thu, 09 Oct 2025 00:38:18 GMT  
		Size: 17.9 KB (17855 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.10.8`

```console
$ docker pull chronograf@sha256:9f0069d5e74770b48d357f8007df8068ccb20353ae1cd9b1d3c68712d34c37b7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `chronograf:1.10.8` - linux; amd64

```console
$ docker pull chronograf@sha256:8e22ca42eca51af0770099dfd8d36924a51de213c107c50286aedb5a9fecb1e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.4 MB (85408161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3285e8978ea95e807515b6f3f620464e98d8386928a0973148decdf52c0ef5f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 15 Aug 2025 14:37:23 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1760918400'
# Fri, 15 Aug 2025 14:37:23 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENV CHRONOGRAF_VERSION=1.10.8
# Fri, 15 Aug 2025 14:37:23 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 15 Aug 2025 14:37:23 GMT
VOLUME [/var/lib/chronograf]
# Fri, 15 Aug 2025 14:37:23 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:abe1fea375429ba91b23776f15f53da4ed790fa2b779b40d20f21e69bd66de5a`  
		Last Modified: Tue, 21 Oct 2025 00:19:19 GMT  
		Size: 28.2 MB (28228321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d678f7ea98bc9cde3cdc6f3822daf66c286a55145d5059c1ab6c170401471c4`  
		Last Modified: Tue, 21 Oct 2025 01:43:32 GMT  
		Size: 7.9 MB (7878755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1823d4badf365aba7b0fd3f98cff8b0abaff5803f47b8d57fbaeeb656471aaba`  
		Last Modified: Tue, 21 Oct 2025 01:43:41 GMT  
		Size: 49.3 MB (49276618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7715f277f40ad8ce01cbe83aa480fed068eb208132e1f1fd18dfec1ad82db60`  
		Last Modified: Tue, 21 Oct 2025 01:43:32 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:612be43be9a1667d3407539a10d5ac2ee077fa118ee89b45931f0c208c3807bf`  
		Last Modified: Tue, 21 Oct 2025 01:43:32 GMT  
		Size: 11.9 KB (11903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d40e348cd71352ccc887adef3c8508b00e9365e7eb81c4a82f557bfca578293`  
		Last Modified: Tue, 21 Oct 2025 01:43:32 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10.8` - unknown; unknown

```console
$ docker pull chronograf@sha256:ad8cbe492cda8ed466b5bfceee4c067234a11ad5d563254ca2ef0464fcdca1f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2870202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8ab40ab435551a74d356b54da4e19abedd945d17b41755c881256ead253ab52`

```dockerfile
```

-	Layers:
	-	`sha256:0b5d752ece03c44d95a557c603adf74579763ef225bb2cbfe38468b0e2b15134`  
		Last Modified: Tue, 21 Oct 2025 09:38:25 GMT  
		Size: 2.9 MB (2854074 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ceda444489ed6780403e9c2aadba05d5c2b42a2cc6307f16d07c466c2d98ec52`  
		Last Modified: Tue, 21 Oct 2025 09:38:25 GMT  
		Size: 16.1 KB (16128 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.10.8` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:1eb13a30653187377adf857362ebf6ad28bb1be8b6dce31f702e7a85f76ab352
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76088345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f743908bb2d47bfb245efff0d344b461c09d68649b31deaf8e14796c39b60af6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 15 Aug 2025 14:37:23 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1760918400'
# Fri, 15 Aug 2025 14:37:23 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENV CHRONOGRAF_VERSION=1.10.8
# Fri, 15 Aug 2025 14:37:23 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 15 Aug 2025 14:37:23 GMT
VOLUME [/var/lib/chronograf]
# Fri, 15 Aug 2025 14:37:23 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:4f520125372ffa3e5f64f19eebfdfce1c8314446e9e3ab2629f5c13cacbd8345`  
		Last Modified: Tue, 21 Oct 2025 00:20:18 GMT  
		Size: 23.9 MB (23934023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9b9cbeab7d89257c02df3df623dbb0db0b03ff0dacad804425d03c0c6bc538f`  
		Last Modified: Tue, 21 Oct 2025 02:48:15 GMT  
		Size: 6.5 MB (6508047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:483e264e639c89e02d166ec79b2c1a646f8a597f6b7f64e075012186ba1f257e`  
		Last Modified: Tue, 21 Oct 2025 02:48:18 GMT  
		Size: 45.6 MB (45621809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e30658b9289a25d89d66fd38b677bf33aab69f2b04e80a707c57437215f1ef49`  
		Last Modified: Tue, 21 Oct 2025 02:48:14 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47956f4970e0f490a78bc21edeef2c2c72c756000f50b21c9644801538fef1e1`  
		Last Modified: Tue, 21 Oct 2025 02:48:14 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13da7c92b57d7e1af6e5c05141a0cccdae906f9f905eac3ba3a2c2d11cc0ea83`  
		Last Modified: Tue, 21 Oct 2025 02:48:14 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10.8` - unknown; unknown

```console
$ docker pull chronograf@sha256:eb3600838cbf523178cf02ba62cddb9aeb6954442b16f7b3199129ebc555a75e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2872584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68df4bb273f5e075b878118d7f75b73f44394c9cbdcf0168a86f5d0bbc5cee15`

```dockerfile
```

-	Layers:
	-	`sha256:76f5f9bb4a19323ff3e5bbf4ebe978240554408deb1602b69c9585473d403666`  
		Last Modified: Tue, 21 Oct 2025 09:38:29 GMT  
		Size: 2.9 MB (2856371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f68f79b94989765e47276910de76c69663b987742ad04584fe7b0dd6009a761b`  
		Last Modified: Tue, 21 Oct 2025 09:38:30 GMT  
		Size: 16.2 KB (16213 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.10.8` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:113b7e3cac741fa1e3247a9cae8b958bd60881497da3522ca371fe48300a5b74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.9 MB (82885222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78be669f8c5ec34a56c042c2f6039c64076f1fcc76c54bf1fa5d924777de9fec`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 15 Aug 2025 14:37:23 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1760918400'
# Fri, 15 Aug 2025 14:37:23 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENV CHRONOGRAF_VERSION=1.10.8
# Fri, 15 Aug 2025 14:37:23 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 15 Aug 2025 14:37:23 GMT
VOLUME [/var/lib/chronograf]
# Fri, 15 Aug 2025 14:37:23 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:21b7accdc53fc02b56a5c1cccd412be04189e5a5e674fd092ffbedc72596be91`  
		Last Modified: Tue, 21 Oct 2025 00:18:57 GMT  
		Size: 28.1 MB (28102190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57847360efefbe97c6032227969a42bcd11fb0de5f8a7c988562801256856d9c`  
		Last Modified: Tue, 21 Oct 2025 01:47:59 GMT  
		Size: 7.7 MB (7691784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24a918b13d7ee929fee3564b1f4a8fa48e9589b846d399d39bd00bd3706efc80`  
		Last Modified: Tue, 21 Oct 2025 01:48:04 GMT  
		Size: 47.1 MB (47066776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:374fd9f33dcbadd2f16dfbc41a0a6ff13c7d47122d503c0c2d2fbd5c0ee89402`  
		Last Modified: Tue, 21 Oct 2025 01:47:59 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb2ed856870944b103a5a36bde6d94fadae3f7c49b1b938759b5c11771bfce7d`  
		Last Modified: Tue, 21 Oct 2025 01:47:59 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b769d03b89d7173d3468a7148bdaeaabb6283887b02bc55d9cee4c147439578`  
		Last Modified: Tue, 21 Oct 2025 01:48:00 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10.8` - unknown; unknown

```console
$ docker pull chronograf@sha256:6b186910c1614e00ad47ee34f42fc5e5f377e0a3cd954e6db6f6297b3d5f7517
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2870582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3d006836f764de414f23cfb6ab70e4c70e43facebc9d32443ba15b850a72b37`

```dockerfile
```

-	Layers:
	-	`sha256:f966f9b47cbb4657cec2c202c92f1d51d230717ec1a948e8f76fa115c46f1c8b`  
		Last Modified: Tue, 21 Oct 2025 09:38:34 GMT  
		Size: 2.9 MB (2854347 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e91722f76a858459622d6a244a19d8ed86fe848ae9085cb9902257a44a8387fd`  
		Last Modified: Tue, 21 Oct 2025 09:38:35 GMT  
		Size: 16.2 KB (16235 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.10.8-alpine`

```console
$ docker pull chronograf@sha256:efc72c285cae492b0fb820a7794f2da69a70ef77caa8d28282e0df6f79856029
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.10.8-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:08463b31a0a2617a51e230161f997b525214640155e291a423ae53004330c719
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.7 MB (32700225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8af178eb7af41f52d85b69957fc583d381f6a24a9e604b40818766ecf3004a1a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 15 Aug 2025 14:37:23 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["/bin/sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
RUN apk add --no-cache ca-certificates setpriv &&     update-ca-certificates # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENV CHRONOGRAF_VERSION=1.10.8
# Fri, 15 Aug 2025 14:37:23 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S chronograf &&     adduser -S chronograf -G chronograf &&     mkdir -m 0750 -p /var/lib/chronograf &&     chown chronograf:chronograf /var/lib/chronograf # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 15 Aug 2025 14:37:23 GMT
VOLUME [/var/lib/chronograf]
# Fri, 15 Aug 2025 14:37:23 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f08cd1461c07b6d2b803ff1e365582cea280da85884cb0fe20c1b539046e9c0f`  
		Last Modified: Wed, 08 Oct 2025 23:01:28 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:642952c8832a913bc8124d8c1f9800b4c40ed32aa2d21f4bbd9c85e32729fdf2`  
		Last Modified: Wed, 08 Oct 2025 23:01:28 GMT  
		Size: 314.6 KB (314639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff188fbd44ef51d6c15c61b590915a7d108294cea3cebd1224f569cf88dbfbd2`  
		Last Modified: Wed, 08 Oct 2025 23:01:31 GMT  
		Size: 28.6 MB (28558408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ada6ea712a91804f080e3ac3a6fec72f1bf330d8affb0a76902b1f0b78a5046`  
		Last Modified: Wed, 08 Oct 2025 23:01:28 GMT  
		Size: 12.2 KB (12237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:322d214c5daa6878e468360de897da9cd0cad1be05283f5529b5e2ce07c9e72f`  
		Last Modified: Wed, 08 Oct 2025 23:01:28 GMT  
		Size: 11.9 KB (11895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:175f9d62a6d73ab836332ca97429aec6104967dc35d5ab6aaa103f374c1539bd`  
		Last Modified: Wed, 08 Oct 2025 23:01:28 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10.8-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:dd3236bd7a2263357f0c7258a9a36c7fef283fd9f58f17f5fc2cbfa8330df313
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.2 KB (268238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:808a56c94ce865ff68fe325760f90b15b31758031ea028455935f57e4d2afe56`

```dockerfile
```

-	Layers:
	-	`sha256:d62aac69b78bc656cc8510a0566537353a4cda897cdaf124ca24ad68c0fa7fb1`  
		Last Modified: Thu, 09 Oct 2025 00:38:17 GMT  
		Size: 250.4 KB (250383 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c7ffc31e817e3fff1eade663dcae6dc3da5bb4370e43abaf921eebc9dd7f0a1`  
		Last Modified: Thu, 09 Oct 2025 00:38:18 GMT  
		Size: 17.9 KB (17855 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.7`

```console
$ docker pull chronograf@sha256:3587dda70b9b3d28551390e4b3e33bcd88712fd86248a38cf86fb3c5d5311210
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
$ docker pull chronograf@sha256:b1a0d645f833bfade77047b1ceaebecfd01536ab53cbb78f55d6cf87fc82a604
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.2 MB (69230689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c425ce494f2bde3ab5436aef779e230766d1ce6b5e9a3eb03e55f2a0175411ee`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 15 Aug 2025 14:37:23 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1760918400'
# Fri, 15 Aug 2025 14:37:23 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Fri, 15 Aug 2025 14:37:23 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 15 Aug 2025 14:37:23 GMT
VOLUME [/var/lib/chronograf]
# Fri, 15 Aug 2025 14:37:23 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:d207cc66da44f4d060efb9a20dc200ca0e6b10c76276d0c1db9c735eaee1d506`  
		Last Modified: Tue, 21 Oct 2025 00:19:22 GMT  
		Size: 30.3 MB (30258365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b63942e2f77b1f2aab97b4edb3525fcb896fbd7ba61f319225c6a2d5ad319e56`  
		Last Modified: Tue, 21 Oct 2025 01:42:49 GMT  
		Size: 4.2 MB (4209357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6319dddfcb5bcbe7e36d91ba947859cf0c3d6dd5022c7f334d8126d26f8ddc59`  
		Last Modified: Tue, 21 Oct 2025 01:42:52 GMT  
		Size: 34.7 MB (34738578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a483ae6a6e0c102e040a6cc11a24681ff5012ad4129ecaed308c4732f6e25b1d`  
		Last Modified: Tue, 21 Oct 2025 01:42:49 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0435378ef6a28ba6c5540e3116fbc7985a9e9a4d33336c0dd9f4288e816aa67b`  
		Last Modified: Tue, 21 Oct 2025 01:42:49 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27cbe019f09af36267ead906db76240e91e6a8765bd03195d4f237d291bade5f`  
		Last Modified: Tue, 21 Oct 2025 01:42:49 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7` - unknown; unknown

```console
$ docker pull chronograf@sha256:1deed6d8e13b667160045bcd3d88fb05529e87d4d7b4f9057508ef0d498e4079
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3064650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2ccde256ae52250ad527685f3400769dd017ac58a946fc7e20e437e24f53fed`

```dockerfile
```

-	Layers:
	-	`sha256:18d9a58ae38ed177346adecaa91f2b64e6fbe665a4f0acdec121a3bc3bd3cb92`  
		Last Modified: Tue, 21 Oct 2025 09:38:41 GMT  
		Size: 3.0 MB (3048873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22b9ab5b35b190bf469081b6d28c990ea0eca6158d1b31b21ac21786ca9a3278`  
		Last Modified: Tue, 21 Oct 2025 09:38:41 GMT  
		Size: 15.8 KB (15777 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.7` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:d7c651cc9386112b6048e54ed6301649a64c0f803ca430e816d5bf3c329b976d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62179759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfc63c581c215a5d61d1e313f7c2aaabe9d8183d6713be8008f83403f8c92380`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 15 Aug 2025 14:37:23 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1760918400'
# Fri, 15 Aug 2025 14:37:23 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Fri, 15 Aug 2025 14:37:23 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 15 Aug 2025 14:37:23 GMT
VOLUME [/var/lib/chronograf]
# Fri, 15 Aug 2025 14:37:23 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:4b897c04dec26603bcc1b01b4283220cd1ffb208f0ec4c0db9e08dab58fcfb5d`  
		Last Modified: Tue, 21 Oct 2025 00:20:34 GMT  
		Size: 25.5 MB (25546187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cf1b635d9f4c8daa9833aa0873308b127fafd575822651a6fc74b0cda823c64`  
		Last Modified: Tue, 21 Oct 2025 02:45:42 GMT  
		Size: 3.5 MB (3511692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42fbd9e61d38fd8c5d8fccb35ba56b7db4a51a296298dc9222a5bfa4daa54976`  
		Last Modified: Tue, 21 Oct 2025 02:45:45 GMT  
		Size: 33.1 MB (33097496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f05dab141846b3bb132bec5fcb671d76ce8b14934d299bb2eee9af3a69f9994b`  
		Last Modified: Tue, 21 Oct 2025 02:45:41 GMT  
		Size: 12.2 KB (12243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05443bc9beb2f17b98b75a3e535da6488ae48c3004c06e6fc6b2e5e35e8b6a8a`  
		Last Modified: Tue, 21 Oct 2025 02:45:42 GMT  
		Size: 11.9 KB (11903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5a96aa7142df9f9757a5a1df18ac04ab1fe8f622c5e43b8689a2aabd9df3f7d`  
		Last Modified: Tue, 21 Oct 2025 02:45:41 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7` - unknown; unknown

```console
$ docker pull chronograf@sha256:be6376d0f2b862864e3a7b835814ec0da24590ee4e51bd1301abf0c8ac03424f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3066998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80e32e6a570582836717e62d81ee9abba85d153323b323360f8236f356a3775b`

```dockerfile
```

-	Layers:
	-	`sha256:4c57d37a83b534519533d97ade9ec00a1bcf704761b774f993082cd91ba482f5`  
		Last Modified: Tue, 21 Oct 2025 09:38:45 GMT  
		Size: 3.1 MB (3051144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dbab0aee08e446f276e2ecea7c37f879375cdf141679d9efbd81299d15057a98`  
		Last Modified: Tue, 21 Oct 2025 09:38:46 GMT  
		Size: 15.9 KB (15854 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.7` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:a59adef3cde2445dc02a0014a05388aa4b17016ead01f0bb88395c73047fa620
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66221576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a131b1c27ef01db4b934f1074563bb4d5f9b68999e130aa4debb907566a01c55`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 15 Aug 2025 14:37:23 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1760918400'
# Fri, 15 Aug 2025 14:37:23 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Fri, 15 Aug 2025 14:37:23 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 15 Aug 2025 14:37:23 GMT
VOLUME [/var/lib/chronograf]
# Fri, 15 Aug 2025 14:37:23 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:40bdde71139ce202a6b0b5346000bda907331b21efec94960489d60568d26752`  
		Last Modified: Tue, 21 Oct 2025 00:19:19 GMT  
		Size: 28.7 MB (28748401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2678153ed072f6422255b9b54f32c84814da857bc01d4c72a4b52fb8b690b4b`  
		Last Modified: Tue, 21 Oct 2025 01:47:19 GMT  
		Size: 4.2 MB (4210657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2af1e2c2da268a9bc2bc42bf56938674e0cbb6baf2eb8960b7d48580b9e22862`  
		Last Modified: Tue, 21 Oct 2025 01:47:21 GMT  
		Size: 33.2 MB (33238136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4fe9c90ceb55e350bbfcb2d7b90f1c9a91e12553de2b9d6c4c8612ddaef9874`  
		Last Modified: Tue, 21 Oct 2025 01:47:19 GMT  
		Size: 12.2 KB (12244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:243ceaac1741e7e77815c149c3ac7c20176b11fa64e9d8bd84c0644b067c6715`  
		Last Modified: Tue, 21 Oct 2025 01:47:20 GMT  
		Size: 11.9 KB (11900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0fdc839a2d95ea8d1bdc5082b71a7a18ae4be93124c8b9470ed292c57b9482b`  
		Last Modified: Tue, 21 Oct 2025 01:47:20 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7` - unknown; unknown

```console
$ docker pull chronograf@sha256:32754981cc2e1036573b80cfa8b700d175e2a0ff2b1defdf5444627bff37c656
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3064994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7d99a47a7381e71b02256687a25c81fd2c53c47c8b3d87e887a0686e4d4b6a2`

```dockerfile
```

-	Layers:
	-	`sha256:4e2a050fb6b761d1d91ab288963abc79f0e411e7bfc082e0f3e5756ec642ec98`  
		Last Modified: Tue, 21 Oct 2025 09:38:49 GMT  
		Size: 3.0 MB (3049122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e0b8f99cb973884f8320f24d6bcb9f8b89607c81c7e3f9b58ddfca44ebae10b`  
		Last Modified: Tue, 21 Oct 2025 09:38:50 GMT  
		Size: 15.9 KB (15872 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.7-alpine`

```console
$ docker pull chronograf@sha256:f9bf8a3a9499f5324ca9b5f428e7ecbf8a4714d366e8a7920a8d06292f7d0511
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.7-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:0e68a8f6a33cec3ad19c936e80df9706efc6f4a6651f78b3373920f503a90deb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.5 MB (23499028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5704e6698a8163ec6cf9a9f4d2fc39455f7394b4b089fd3fe4fbbfcd3c84f5fc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 15 Aug 2025 14:37:23 GMT
ADD alpine-minirootfs-3.20.8-x86_64.tar.gz / # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["/bin/sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Fri, 15 Aug 2025 14:37:23 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 15 Aug 2025 14:37:23 GMT
VOLUME [/var/lib/chronograf]
# Fri, 15 Aug 2025 14:37:23 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:5311e7f182d02360a7194aa2995849bcdf04795c39a0ffdcf413eae625865970`  
		Last Modified: Wed, 08 Oct 2025 12:03:10 GMT  
		Size: 3.6 MB (3627056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af74a58a446b59e39793a690435f78e585a91ea73edb6406a99a3283db12a3a2`  
		Last Modified: Wed, 08 Oct 2025 23:01:06 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:053646d1ede74b4422e0751427c045b128d56b4d9c7521a34d9a3e2fd81f2fa6`  
		Last Modified: Wed, 08 Oct 2025 23:01:06 GMT  
		Size: 290.8 KB (290771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9fddb95d664d6dacdb2318596d88bdbacf9e5bde5abe2b7e4335d05288276ea`  
		Last Modified: Wed, 08 Oct 2025 23:01:21 GMT  
		Size: 19.6 MB (19556558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56f367635d83aeb5f5f554e62a06a02ad833c17339cf302d30013629399527c0`  
		Last Modified: Wed, 08 Oct 2025 23:01:06 GMT  
		Size: 12.2 KB (12235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b07f90ee1715c3ce00ef0c8e4958732cd35aeb06708db0a00e83afbe1f17da89`  
		Last Modified: Wed, 08 Oct 2025 23:01:06 GMT  
		Size: 11.9 KB (11891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9166e539db1f38a4aa1b578555a8c92c86979cbc08b8098fba9661f87ffe6167`  
		Last Modified: Wed, 08 Oct 2025 23:01:06 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:bcbb31392ab3215af685b41ca6842da95b2e263604620ad5d7a30c80609bc543
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.7 KB (188744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:862b2564bbbfa2013c4f206e9af5027911bf83448426df87b517b51fb5f596e0`

```dockerfile
```

-	Layers:
	-	`sha256:7d486241e7d5fad65401d86ed4cecac735dc744dd18c05a5530b79d0bc9ae6ac`  
		Last Modified: Thu, 09 Oct 2025 00:38:28 GMT  
		Size: 171.8 KB (171832 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87486fae9bd6ba27ac7806fc6b1c5c571f4d3de5fc46fd1b292df95f203bc24e`  
		Last Modified: Thu, 09 Oct 2025 00:38:28 GMT  
		Size: 16.9 KB (16912 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.7.17`

```console
$ docker pull chronograf@sha256:3587dda70b9b3d28551390e4b3e33bcd88712fd86248a38cf86fb3c5d5311210
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
$ docker pull chronograf@sha256:b1a0d645f833bfade77047b1ceaebecfd01536ab53cbb78f55d6cf87fc82a604
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.2 MB (69230689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c425ce494f2bde3ab5436aef779e230766d1ce6b5e9a3eb03e55f2a0175411ee`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 15 Aug 2025 14:37:23 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1760918400'
# Fri, 15 Aug 2025 14:37:23 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Fri, 15 Aug 2025 14:37:23 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 15 Aug 2025 14:37:23 GMT
VOLUME [/var/lib/chronograf]
# Fri, 15 Aug 2025 14:37:23 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:d207cc66da44f4d060efb9a20dc200ca0e6b10c76276d0c1db9c735eaee1d506`  
		Last Modified: Tue, 21 Oct 2025 00:19:22 GMT  
		Size: 30.3 MB (30258365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b63942e2f77b1f2aab97b4edb3525fcb896fbd7ba61f319225c6a2d5ad319e56`  
		Last Modified: Tue, 21 Oct 2025 01:42:49 GMT  
		Size: 4.2 MB (4209357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6319dddfcb5bcbe7e36d91ba947859cf0c3d6dd5022c7f334d8126d26f8ddc59`  
		Last Modified: Tue, 21 Oct 2025 01:42:52 GMT  
		Size: 34.7 MB (34738578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a483ae6a6e0c102e040a6cc11a24681ff5012ad4129ecaed308c4732f6e25b1d`  
		Last Modified: Tue, 21 Oct 2025 01:42:49 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0435378ef6a28ba6c5540e3116fbc7985a9e9a4d33336c0dd9f4288e816aa67b`  
		Last Modified: Tue, 21 Oct 2025 01:42:49 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27cbe019f09af36267ead906db76240e91e6a8765bd03195d4f237d291bade5f`  
		Last Modified: Tue, 21 Oct 2025 01:42:49 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7.17` - unknown; unknown

```console
$ docker pull chronograf@sha256:1deed6d8e13b667160045bcd3d88fb05529e87d4d7b4f9057508ef0d498e4079
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3064650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2ccde256ae52250ad527685f3400769dd017ac58a946fc7e20e437e24f53fed`

```dockerfile
```

-	Layers:
	-	`sha256:18d9a58ae38ed177346adecaa91f2b64e6fbe665a4f0acdec121a3bc3bd3cb92`  
		Last Modified: Tue, 21 Oct 2025 09:38:41 GMT  
		Size: 3.0 MB (3048873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22b9ab5b35b190bf469081b6d28c990ea0eca6158d1b31b21ac21786ca9a3278`  
		Last Modified: Tue, 21 Oct 2025 09:38:41 GMT  
		Size: 15.8 KB (15777 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.7.17` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:d7c651cc9386112b6048e54ed6301649a64c0f803ca430e816d5bf3c329b976d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62179759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfc63c581c215a5d61d1e313f7c2aaabe9d8183d6713be8008f83403f8c92380`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 15 Aug 2025 14:37:23 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1760918400'
# Fri, 15 Aug 2025 14:37:23 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Fri, 15 Aug 2025 14:37:23 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 15 Aug 2025 14:37:23 GMT
VOLUME [/var/lib/chronograf]
# Fri, 15 Aug 2025 14:37:23 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:4b897c04dec26603bcc1b01b4283220cd1ffb208f0ec4c0db9e08dab58fcfb5d`  
		Last Modified: Tue, 21 Oct 2025 00:20:34 GMT  
		Size: 25.5 MB (25546187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cf1b635d9f4c8daa9833aa0873308b127fafd575822651a6fc74b0cda823c64`  
		Last Modified: Tue, 21 Oct 2025 02:45:42 GMT  
		Size: 3.5 MB (3511692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42fbd9e61d38fd8c5d8fccb35ba56b7db4a51a296298dc9222a5bfa4daa54976`  
		Last Modified: Tue, 21 Oct 2025 02:45:45 GMT  
		Size: 33.1 MB (33097496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f05dab141846b3bb132bec5fcb671d76ce8b14934d299bb2eee9af3a69f9994b`  
		Last Modified: Tue, 21 Oct 2025 02:45:41 GMT  
		Size: 12.2 KB (12243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05443bc9beb2f17b98b75a3e535da6488ae48c3004c06e6fc6b2e5e35e8b6a8a`  
		Last Modified: Tue, 21 Oct 2025 02:45:42 GMT  
		Size: 11.9 KB (11903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5a96aa7142df9f9757a5a1df18ac04ab1fe8f622c5e43b8689a2aabd9df3f7d`  
		Last Modified: Tue, 21 Oct 2025 02:45:41 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7.17` - unknown; unknown

```console
$ docker pull chronograf@sha256:be6376d0f2b862864e3a7b835814ec0da24590ee4e51bd1301abf0c8ac03424f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3066998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80e32e6a570582836717e62d81ee9abba85d153323b323360f8236f356a3775b`

```dockerfile
```

-	Layers:
	-	`sha256:4c57d37a83b534519533d97ade9ec00a1bcf704761b774f993082cd91ba482f5`  
		Last Modified: Tue, 21 Oct 2025 09:38:45 GMT  
		Size: 3.1 MB (3051144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dbab0aee08e446f276e2ecea7c37f879375cdf141679d9efbd81299d15057a98`  
		Last Modified: Tue, 21 Oct 2025 09:38:46 GMT  
		Size: 15.9 KB (15854 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.7.17` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:a59adef3cde2445dc02a0014a05388aa4b17016ead01f0bb88395c73047fa620
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66221576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a131b1c27ef01db4b934f1074563bb4d5f9b68999e130aa4debb907566a01c55`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 15 Aug 2025 14:37:23 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1760918400'
# Fri, 15 Aug 2025 14:37:23 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Fri, 15 Aug 2025 14:37:23 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 15 Aug 2025 14:37:23 GMT
VOLUME [/var/lib/chronograf]
# Fri, 15 Aug 2025 14:37:23 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:40bdde71139ce202a6b0b5346000bda907331b21efec94960489d60568d26752`  
		Last Modified: Tue, 21 Oct 2025 00:19:19 GMT  
		Size: 28.7 MB (28748401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2678153ed072f6422255b9b54f32c84814da857bc01d4c72a4b52fb8b690b4b`  
		Last Modified: Tue, 21 Oct 2025 01:47:19 GMT  
		Size: 4.2 MB (4210657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2af1e2c2da268a9bc2bc42bf56938674e0cbb6baf2eb8960b7d48580b9e22862`  
		Last Modified: Tue, 21 Oct 2025 01:47:21 GMT  
		Size: 33.2 MB (33238136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4fe9c90ceb55e350bbfcb2d7b90f1c9a91e12553de2b9d6c4c8612ddaef9874`  
		Last Modified: Tue, 21 Oct 2025 01:47:19 GMT  
		Size: 12.2 KB (12244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:243ceaac1741e7e77815c149c3ac7c20176b11fa64e9d8bd84c0644b067c6715`  
		Last Modified: Tue, 21 Oct 2025 01:47:20 GMT  
		Size: 11.9 KB (11900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0fdc839a2d95ea8d1bdc5082b71a7a18ae4be93124c8b9470ed292c57b9482b`  
		Last Modified: Tue, 21 Oct 2025 01:47:20 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7.17` - unknown; unknown

```console
$ docker pull chronograf@sha256:32754981cc2e1036573b80cfa8b700d175e2a0ff2b1defdf5444627bff37c656
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3064994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7d99a47a7381e71b02256687a25c81fd2c53c47c8b3d87e887a0686e4d4b6a2`

```dockerfile
```

-	Layers:
	-	`sha256:4e2a050fb6b761d1d91ab288963abc79f0e411e7bfc082e0f3e5756ec642ec98`  
		Last Modified: Tue, 21 Oct 2025 09:38:49 GMT  
		Size: 3.0 MB (3049122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e0b8f99cb973884f8320f24d6bcb9f8b89607c81c7e3f9b58ddfca44ebae10b`  
		Last Modified: Tue, 21 Oct 2025 09:38:50 GMT  
		Size: 15.9 KB (15872 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.7.17-alpine`

```console
$ docker pull chronograf@sha256:f9bf8a3a9499f5324ca9b5f428e7ecbf8a4714d366e8a7920a8d06292f7d0511
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.7.17-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:0e68a8f6a33cec3ad19c936e80df9706efc6f4a6651f78b3373920f503a90deb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.5 MB (23499028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5704e6698a8163ec6cf9a9f4d2fc39455f7394b4b089fd3fe4fbbfcd3c84f5fc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 15 Aug 2025 14:37:23 GMT
ADD alpine-minirootfs-3.20.8-x86_64.tar.gz / # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["/bin/sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Fri, 15 Aug 2025 14:37:23 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 15 Aug 2025 14:37:23 GMT
VOLUME [/var/lib/chronograf]
# Fri, 15 Aug 2025 14:37:23 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:5311e7f182d02360a7194aa2995849bcdf04795c39a0ffdcf413eae625865970`  
		Last Modified: Wed, 08 Oct 2025 12:03:10 GMT  
		Size: 3.6 MB (3627056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af74a58a446b59e39793a690435f78e585a91ea73edb6406a99a3283db12a3a2`  
		Last Modified: Wed, 08 Oct 2025 23:01:06 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:053646d1ede74b4422e0751427c045b128d56b4d9c7521a34d9a3e2fd81f2fa6`  
		Last Modified: Wed, 08 Oct 2025 23:01:06 GMT  
		Size: 290.8 KB (290771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9fddb95d664d6dacdb2318596d88bdbacf9e5bde5abe2b7e4335d05288276ea`  
		Last Modified: Wed, 08 Oct 2025 23:01:21 GMT  
		Size: 19.6 MB (19556558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56f367635d83aeb5f5f554e62a06a02ad833c17339cf302d30013629399527c0`  
		Last Modified: Wed, 08 Oct 2025 23:01:06 GMT  
		Size: 12.2 KB (12235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b07f90ee1715c3ce00ef0c8e4958732cd35aeb06708db0a00e83afbe1f17da89`  
		Last Modified: Wed, 08 Oct 2025 23:01:06 GMT  
		Size: 11.9 KB (11891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9166e539db1f38a4aa1b578555a8c92c86979cbc08b8098fba9661f87ffe6167`  
		Last Modified: Wed, 08 Oct 2025 23:01:06 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7.17-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:bcbb31392ab3215af685b41ca6842da95b2e263604620ad5d7a30c80609bc543
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.7 KB (188744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:862b2564bbbfa2013c4f206e9af5027911bf83448426df87b517b51fb5f596e0`

```dockerfile
```

-	Layers:
	-	`sha256:7d486241e7d5fad65401d86ed4cecac735dc744dd18c05a5530b79d0bc9ae6ac`  
		Last Modified: Thu, 09 Oct 2025 00:38:28 GMT  
		Size: 171.8 KB (171832 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87486fae9bd6ba27ac7806fc6b1c5c571f4d3de5fc46fd1b292df95f203bc24e`  
		Last Modified: Thu, 09 Oct 2025 00:38:28 GMT  
		Size: 16.9 KB (16912 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.8`

```console
$ docker pull chronograf@sha256:63f91b3aa51dfeea525163611519f1ea648564f4098911ee7c2cdf1897d44a0e
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
$ docker pull chronograf@sha256:62129252f850c7722caa2a2d66787560fb28df4f215b8b4e9ad9bc9e59b07b2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69871367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb7787d9e759f01fbacc85a00ab3a1f73d7296d3ece93d422afae761b7da2a57`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 15 Aug 2025 14:37:23 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1760918400'
# Fri, 15 Aug 2025 14:37:23 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Fri, 15 Aug 2025 14:37:23 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 15 Aug 2025 14:37:23 GMT
VOLUME [/var/lib/chronograf]
# Fri, 15 Aug 2025 14:37:23 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:d207cc66da44f4d060efb9a20dc200ca0e6b10c76276d0c1db9c735eaee1d506`  
		Last Modified: Tue, 21 Oct 2025 00:19:22 GMT  
		Size: 30.3 MB (30258365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22e93e6a212aa2a56c525bf376c7c36fc44259cef0ed10a57ee5a350ee1ce17d`  
		Last Modified: Tue, 21 Oct 2025 01:43:21 GMT  
		Size: 5.2 MB (5224288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d0fdfb26b0e539cd1407c5ede33ba80a5fffa720850e003f0926d0463a5dae1`  
		Last Modified: Tue, 21 Oct 2025 01:43:25 GMT  
		Size: 34.4 MB (34364332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87334660c2a8116680fe46d0ad6c35f2c96891180b02aaad1c412bfcf0b7892d`  
		Last Modified: Tue, 21 Oct 2025 01:43:21 GMT  
		Size: 12.2 KB (12244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7838131886f15d61ae9c1453a5ef88a00a0d685e2d8336c3b4a940b2cf0a64e9`  
		Last Modified: Tue, 21 Oct 2025 01:43:21 GMT  
		Size: 11.9 KB (11900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:512d759d2265761b9f5409a96de938371e25fa62d542b0bc3abedc8cb9df957c`  
		Last Modified: Tue, 21 Oct 2025 01:43:21 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8` - unknown; unknown

```console
$ docker pull chronograf@sha256:7e3e195660f2a5cd1eb90c9429cf9e2c6e96fffbdd901fbcb4b89fbe2f3cd9ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3120328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bb0886c5baebdea2087f989ac7a58e56481dbb480614e2fa3dd67cd6727c832`

```dockerfile
```

-	Layers:
	-	`sha256:6d8a1b9a2dc4254fb93913beba9bdcbe9d42d4225c02a0bdc9ba2a79fe1ea031`  
		Last Modified: Tue, 21 Oct 2025 09:38:55 GMT  
		Size: 3.1 MB (3104511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7ec6612f8f053f9d7456a39bae22967a3f0a6c3b54ba7338da5fd4b778571e9`  
		Last Modified: Tue, 21 Oct 2025 09:38:55 GMT  
		Size: 15.8 KB (15817 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.8` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:20ea7e394a13f5aa03c66b8985f654c0c5e6e910dc041f8bddc020ccc4152375
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.6 MB (62595669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cbaac80b922b71edcc34c1ce87c4c2bfe3b904c7d6f1655995d66ef7fa68f5e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 15 Aug 2025 14:37:23 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1760918400'
# Fri, 15 Aug 2025 14:37:23 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Fri, 15 Aug 2025 14:37:23 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 15 Aug 2025 14:37:23 GMT
VOLUME [/var/lib/chronograf]
# Fri, 15 Aug 2025 14:37:23 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:4b897c04dec26603bcc1b01b4283220cd1ffb208f0ec4c0db9e08dab58fcfb5d`  
		Last Modified: Tue, 21 Oct 2025 00:20:34 GMT  
		Size: 25.5 MB (25546187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3849e75ed501b132052b559f3f67a2944412858b9f6b7349368093f88990de31`  
		Last Modified: Tue, 21 Oct 2025 02:45:42 GMT  
		Size: 4.5 MB (4490214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9092b62c139984eb5f6625a6f89d57bc5c91352a2b33bf43e01855e22b8df8b9`  
		Last Modified: Tue, 21 Oct 2025 02:45:43 GMT  
		Size: 32.5 MB (32534883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:791922ef09608e55f5a128d3ad18b2c4a944358125dbfcfffd2b8748c3a7d2cb`  
		Last Modified: Tue, 21 Oct 2025 02:45:41 GMT  
		Size: 12.2 KB (12244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38b0520df62e24f1910e7d7c7507cd6d9c08d0f5fab5c18406dd05696e3a04b4`  
		Last Modified: Tue, 21 Oct 2025 02:45:42 GMT  
		Size: 11.9 KB (11903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:669d441744bd526577687f648c7d7b1f76bdc52113c188bf409a6689b5ba4628`  
		Last Modified: Tue, 21 Oct 2025 02:45:41 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8` - unknown; unknown

```console
$ docker pull chronograf@sha256:25c4c2f113370187e655f31e6172566146957dad3f1923f4aa1599acbd53ab0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3122676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d52d7184b2614c832072bc68f4fb11f9aa337519dd084709207628c95b9c6636`

```dockerfile
```

-	Layers:
	-	`sha256:3d1ecc9054cc1c00f16ddd55408261c0402f576c0342d77204eb1103d1eb3cd1`  
		Last Modified: Tue, 21 Oct 2025 09:39:00 GMT  
		Size: 3.1 MB (3106782 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a13caebd4f87286f8bc025e062b4f6352bc239740bb9a71ad0b80556eadcbf62`  
		Last Modified: Tue, 21 Oct 2025 09:39:01 GMT  
		Size: 15.9 KB (15894 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.8` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:cfce7b6c98621901ea91a8204c0d91c26bf6acc1efb4a6fdd3b1a6832f0d5cec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.4 MB (66410435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8a1687f4264511edccf0bbc4202c422f0f3466bd465ce5245c4064020a41074`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 15 Aug 2025 14:37:23 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1760918400'
# Fri, 15 Aug 2025 14:37:23 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Fri, 15 Aug 2025 14:37:23 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 15 Aug 2025 14:37:23 GMT
VOLUME [/var/lib/chronograf]
# Fri, 15 Aug 2025 14:37:23 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:40bdde71139ce202a6b0b5346000bda907331b21efec94960489d60568d26752`  
		Last Modified: Tue, 21 Oct 2025 00:19:19 GMT  
		Size: 28.7 MB (28748401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9955db2cbcbd0d0c75c26c739017ba7cd68154a7636de607ebb6e5ccc68f88bb`  
		Last Modified: Tue, 21 Oct 2025 01:47:36 GMT  
		Size: 5.2 MB (5208129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a4ff276a1114cb0b116f6ed294e0cd28c624a5ea98327452bfc612e43273bcb`  
		Last Modified: Tue, 21 Oct 2025 01:47:40 GMT  
		Size: 32.4 MB (32429510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5da5f7263e91a2a6a546fce38a732535db6f77052392448e25bb726c5cd28d8f`  
		Last Modified: Tue, 21 Oct 2025 01:47:36 GMT  
		Size: 12.3 KB (12251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f0e42a145221643d7ad56c18c73ebca813b5751c66ae983049e91abeff873d1`  
		Last Modified: Tue, 21 Oct 2025 01:47:36 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:735c02c97e69b6fdabcf10844f0c8d34c406781e71fdce3f49a73b6b540ddeb6`  
		Last Modified: Tue, 21 Oct 2025 01:47:36 GMT  
		Size: 237.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8` - unknown; unknown

```console
$ docker pull chronograf@sha256:9c2101cb96bb1743c3358b62b4596c1bbaab3ddde9a466f7869fcda446d12865
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3120672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c721231580e00b5f38783314ff0b49bdbde9c2500ad554c5571082ed553510d0`

```dockerfile
```

-	Layers:
	-	`sha256:3447cafe3d2ab80a2bfdae9aae8bc1758fa5246308ffc3b54e2e9cd2158d239e`  
		Last Modified: Tue, 21 Oct 2025 09:39:05 GMT  
		Size: 3.1 MB (3104760 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b2ff33fb8f08fb9006b62642c6c2966ba05688b795b1579109b99331bd12aea`  
		Last Modified: Tue, 21 Oct 2025 09:39:05 GMT  
		Size: 15.9 KB (15912 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.8-alpine`

```console
$ docker pull chronograf@sha256:8f246b11bed20824de500e732e0e0c1a9df2e2adcf60340444da2c4d2e7d83bc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.8-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:4fae84330ab9094200744d44140ff3695efc2a2085251cd4066103541bffbe5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23146498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6035189b6fd6fc001306a038b9c5678123af0b1f907f2a31efe3e96b3b689b22`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 15 Aug 2025 14:37:23 GMT
ADD alpine-minirootfs-3.20.8-x86_64.tar.gz / # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["/bin/sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Fri, 15 Aug 2025 14:37:23 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 15 Aug 2025 14:37:23 GMT
VOLUME [/var/lib/chronograf]
# Fri, 15 Aug 2025 14:37:23 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:5311e7f182d02360a7194aa2995849bcdf04795c39a0ffdcf413eae625865970`  
		Last Modified: Wed, 08 Oct 2025 12:03:10 GMT  
		Size: 3.6 MB (3627056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdaabc96984af774b48937345c7cc275e3315d3a9a42aeb994f6946de24556be`  
		Last Modified: Wed, 08 Oct 2025 23:01:09 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff81f10ae11b38f809feee3b7a44d508880916016658ca83647ff9d1c294aba`  
		Last Modified: Wed, 08 Oct 2025 23:01:09 GMT  
		Size: 290.8 KB (290774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa8cf4bd3a04c4941275f4aa1db1887c01bcdadeb973d9c95d34bc905b974dce`  
		Last Modified: Wed, 08 Oct 2025 23:01:11 GMT  
		Size: 19.2 MB (19204014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4732a865d574eb12cd7075d139d6bbd7d47fea3c367baf1a1f56ff51506906fb`  
		Last Modified: Wed, 08 Oct 2025 23:01:08 GMT  
		Size: 12.2 KB (12240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0733dea6fe6d3cf04ef8c52dec6540501fbf0e79664e84fd00853fab32410e15`  
		Last Modified: Wed, 08 Oct 2025 23:01:09 GMT  
		Size: 11.9 KB (11896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe58005a9627e476ca3528af5a14e30f0d4549afa8e314dcde58ee7ec5fd6671`  
		Last Modified: Wed, 08 Oct 2025 23:01:09 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:07f09e7f03af9efcf88f89d7ad0f207d0e5ab57b9423663591e3c7aa0b3bc6a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.3 KB (245253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2779ee449137493a2aca535f4363cae748d5a6c40f2c306362a97daf2d51bf6b`

```dockerfile
```

-	Layers:
	-	`sha256:4376140096bd52be7b1473ee7e7d625fff88ab2e731a2d509ed5b7861eab79fe`  
		Last Modified: Thu, 09 Oct 2025 00:38:34 GMT  
		Size: 228.3 KB (228341 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61687d781240db246500ccffe6dc5608d9be7a5e7c809173a2694ffec485f7c3`  
		Last Modified: Thu, 09 Oct 2025 00:38:35 GMT  
		Size: 16.9 KB (16912 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.8.10`

```console
$ docker pull chronograf@sha256:63f91b3aa51dfeea525163611519f1ea648564f4098911ee7c2cdf1897d44a0e
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
$ docker pull chronograf@sha256:62129252f850c7722caa2a2d66787560fb28df4f215b8b4e9ad9bc9e59b07b2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69871367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb7787d9e759f01fbacc85a00ab3a1f73d7296d3ece93d422afae761b7da2a57`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 15 Aug 2025 14:37:23 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1760918400'
# Fri, 15 Aug 2025 14:37:23 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Fri, 15 Aug 2025 14:37:23 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 15 Aug 2025 14:37:23 GMT
VOLUME [/var/lib/chronograf]
# Fri, 15 Aug 2025 14:37:23 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:d207cc66da44f4d060efb9a20dc200ca0e6b10c76276d0c1db9c735eaee1d506`  
		Last Modified: Tue, 21 Oct 2025 00:19:22 GMT  
		Size: 30.3 MB (30258365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22e93e6a212aa2a56c525bf376c7c36fc44259cef0ed10a57ee5a350ee1ce17d`  
		Last Modified: Tue, 21 Oct 2025 01:43:21 GMT  
		Size: 5.2 MB (5224288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d0fdfb26b0e539cd1407c5ede33ba80a5fffa720850e003f0926d0463a5dae1`  
		Last Modified: Tue, 21 Oct 2025 01:43:25 GMT  
		Size: 34.4 MB (34364332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87334660c2a8116680fe46d0ad6c35f2c96891180b02aaad1c412bfcf0b7892d`  
		Last Modified: Tue, 21 Oct 2025 01:43:21 GMT  
		Size: 12.2 KB (12244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7838131886f15d61ae9c1453a5ef88a00a0d685e2d8336c3b4a940b2cf0a64e9`  
		Last Modified: Tue, 21 Oct 2025 01:43:21 GMT  
		Size: 11.9 KB (11900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:512d759d2265761b9f5409a96de938371e25fa62d542b0bc3abedc8cb9df957c`  
		Last Modified: Tue, 21 Oct 2025 01:43:21 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:7e3e195660f2a5cd1eb90c9429cf9e2c6e96fffbdd901fbcb4b89fbe2f3cd9ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3120328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bb0886c5baebdea2087f989ac7a58e56481dbb480614e2fa3dd67cd6727c832`

```dockerfile
```

-	Layers:
	-	`sha256:6d8a1b9a2dc4254fb93913beba9bdcbe9d42d4225c02a0bdc9ba2a79fe1ea031`  
		Last Modified: Tue, 21 Oct 2025 09:38:55 GMT  
		Size: 3.1 MB (3104511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7ec6612f8f053f9d7456a39bae22967a3f0a6c3b54ba7338da5fd4b778571e9`  
		Last Modified: Tue, 21 Oct 2025 09:38:55 GMT  
		Size: 15.8 KB (15817 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.8.10` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:20ea7e394a13f5aa03c66b8985f654c0c5e6e910dc041f8bddc020ccc4152375
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.6 MB (62595669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cbaac80b922b71edcc34c1ce87c4c2bfe3b904c7d6f1655995d66ef7fa68f5e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 15 Aug 2025 14:37:23 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1760918400'
# Fri, 15 Aug 2025 14:37:23 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Fri, 15 Aug 2025 14:37:23 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 15 Aug 2025 14:37:23 GMT
VOLUME [/var/lib/chronograf]
# Fri, 15 Aug 2025 14:37:23 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:4b897c04dec26603bcc1b01b4283220cd1ffb208f0ec4c0db9e08dab58fcfb5d`  
		Last Modified: Tue, 21 Oct 2025 00:20:34 GMT  
		Size: 25.5 MB (25546187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3849e75ed501b132052b559f3f67a2944412858b9f6b7349368093f88990de31`  
		Last Modified: Tue, 21 Oct 2025 02:45:42 GMT  
		Size: 4.5 MB (4490214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9092b62c139984eb5f6625a6f89d57bc5c91352a2b33bf43e01855e22b8df8b9`  
		Last Modified: Tue, 21 Oct 2025 02:45:43 GMT  
		Size: 32.5 MB (32534883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:791922ef09608e55f5a128d3ad18b2c4a944358125dbfcfffd2b8748c3a7d2cb`  
		Last Modified: Tue, 21 Oct 2025 02:45:41 GMT  
		Size: 12.2 KB (12244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38b0520df62e24f1910e7d7c7507cd6d9c08d0f5fab5c18406dd05696e3a04b4`  
		Last Modified: Tue, 21 Oct 2025 02:45:42 GMT  
		Size: 11.9 KB (11903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:669d441744bd526577687f648c7d7b1f76bdc52113c188bf409a6689b5ba4628`  
		Last Modified: Tue, 21 Oct 2025 02:45:41 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:25c4c2f113370187e655f31e6172566146957dad3f1923f4aa1599acbd53ab0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3122676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d52d7184b2614c832072bc68f4fb11f9aa337519dd084709207628c95b9c6636`

```dockerfile
```

-	Layers:
	-	`sha256:3d1ecc9054cc1c00f16ddd55408261c0402f576c0342d77204eb1103d1eb3cd1`  
		Last Modified: Tue, 21 Oct 2025 09:39:00 GMT  
		Size: 3.1 MB (3106782 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a13caebd4f87286f8bc025e062b4f6352bc239740bb9a71ad0b80556eadcbf62`  
		Last Modified: Tue, 21 Oct 2025 09:39:01 GMT  
		Size: 15.9 KB (15894 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.8.10` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:cfce7b6c98621901ea91a8204c0d91c26bf6acc1efb4a6fdd3b1a6832f0d5cec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.4 MB (66410435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8a1687f4264511edccf0bbc4202c422f0f3466bd465ce5245c4064020a41074`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 15 Aug 2025 14:37:23 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1760918400'
# Fri, 15 Aug 2025 14:37:23 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Fri, 15 Aug 2025 14:37:23 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 15 Aug 2025 14:37:23 GMT
VOLUME [/var/lib/chronograf]
# Fri, 15 Aug 2025 14:37:23 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:40bdde71139ce202a6b0b5346000bda907331b21efec94960489d60568d26752`  
		Last Modified: Tue, 21 Oct 2025 00:19:19 GMT  
		Size: 28.7 MB (28748401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9955db2cbcbd0d0c75c26c739017ba7cd68154a7636de607ebb6e5ccc68f88bb`  
		Last Modified: Tue, 21 Oct 2025 01:47:36 GMT  
		Size: 5.2 MB (5208129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a4ff276a1114cb0b116f6ed294e0cd28c624a5ea98327452bfc612e43273bcb`  
		Last Modified: Tue, 21 Oct 2025 01:47:40 GMT  
		Size: 32.4 MB (32429510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5da5f7263e91a2a6a546fce38a732535db6f77052392448e25bb726c5cd28d8f`  
		Last Modified: Tue, 21 Oct 2025 01:47:36 GMT  
		Size: 12.3 KB (12251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f0e42a145221643d7ad56c18c73ebca813b5751c66ae983049e91abeff873d1`  
		Last Modified: Tue, 21 Oct 2025 01:47:36 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:735c02c97e69b6fdabcf10844f0c8d34c406781e71fdce3f49a73b6b540ddeb6`  
		Last Modified: Tue, 21 Oct 2025 01:47:36 GMT  
		Size: 237.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:9c2101cb96bb1743c3358b62b4596c1bbaab3ddde9a466f7869fcda446d12865
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3120672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c721231580e00b5f38783314ff0b49bdbde9c2500ad554c5571082ed553510d0`

```dockerfile
```

-	Layers:
	-	`sha256:3447cafe3d2ab80a2bfdae9aae8bc1758fa5246308ffc3b54e2e9cd2158d239e`  
		Last Modified: Tue, 21 Oct 2025 09:39:05 GMT  
		Size: 3.1 MB (3104760 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b2ff33fb8f08fb9006b62642c6c2966ba05688b795b1579109b99331bd12aea`  
		Last Modified: Tue, 21 Oct 2025 09:39:05 GMT  
		Size: 15.9 KB (15912 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.8.10-alpine`

```console
$ docker pull chronograf@sha256:8f246b11bed20824de500e732e0e0c1a9df2e2adcf60340444da2c4d2e7d83bc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.8.10-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:4fae84330ab9094200744d44140ff3695efc2a2085251cd4066103541bffbe5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23146498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6035189b6fd6fc001306a038b9c5678123af0b1f907f2a31efe3e96b3b689b22`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 15 Aug 2025 14:37:23 GMT
ADD alpine-minirootfs-3.20.8-x86_64.tar.gz / # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["/bin/sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Fri, 15 Aug 2025 14:37:23 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 15 Aug 2025 14:37:23 GMT
VOLUME [/var/lib/chronograf]
# Fri, 15 Aug 2025 14:37:23 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:5311e7f182d02360a7194aa2995849bcdf04795c39a0ffdcf413eae625865970`  
		Last Modified: Wed, 08 Oct 2025 12:03:10 GMT  
		Size: 3.6 MB (3627056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdaabc96984af774b48937345c7cc275e3315d3a9a42aeb994f6946de24556be`  
		Last Modified: Wed, 08 Oct 2025 23:01:09 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff81f10ae11b38f809feee3b7a44d508880916016658ca83647ff9d1c294aba`  
		Last Modified: Wed, 08 Oct 2025 23:01:09 GMT  
		Size: 290.8 KB (290774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa8cf4bd3a04c4941275f4aa1db1887c01bcdadeb973d9c95d34bc905b974dce`  
		Last Modified: Wed, 08 Oct 2025 23:01:11 GMT  
		Size: 19.2 MB (19204014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4732a865d574eb12cd7075d139d6bbd7d47fea3c367baf1a1f56ff51506906fb`  
		Last Modified: Wed, 08 Oct 2025 23:01:08 GMT  
		Size: 12.2 KB (12240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0733dea6fe6d3cf04ef8c52dec6540501fbf0e79664e84fd00853fab32410e15`  
		Last Modified: Wed, 08 Oct 2025 23:01:09 GMT  
		Size: 11.9 KB (11896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe58005a9627e476ca3528af5a14e30f0d4549afa8e314dcde58ee7ec5fd6671`  
		Last Modified: Wed, 08 Oct 2025 23:01:09 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8.10-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:07f09e7f03af9efcf88f89d7ad0f207d0e5ab57b9423663591e3c7aa0b3bc6a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.3 KB (245253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2779ee449137493a2aca535f4363cae748d5a6c40f2c306362a97daf2d51bf6b`

```dockerfile
```

-	Layers:
	-	`sha256:4376140096bd52be7b1473ee7e7d625fff88ab2e731a2d509ed5b7861eab79fe`  
		Last Modified: Thu, 09 Oct 2025 00:38:34 GMT  
		Size: 228.3 KB (228341 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61687d781240db246500ccffe6dc5608d9be7a5e7c809173a2694ffec485f7c3`  
		Last Modified: Thu, 09 Oct 2025 00:38:35 GMT  
		Size: 16.9 KB (16912 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.9`

```console
$ docker pull chronograf@sha256:5a97bdd06430abb6b6541bb66a965396334126f9b6f6e66d945af1c3b3ea798f
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
$ docker pull chronograf@sha256:dbf638ede671617f87ef9e4fa556bbcc791c9a1a3fedc2f8bc7c2776c3daad17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.5 MB (70518809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41d7cfc1fe10a12a9535417379672d1359adbb1c3a7e6265e4f9cbe73dca8bdb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 15 Aug 2025 14:37:23 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1760918400'
# Fri, 15 Aug 2025 14:37:23 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Fri, 15 Aug 2025 14:37:23 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 15 Aug 2025 14:37:23 GMT
VOLUME [/var/lib/chronograf]
# Fri, 15 Aug 2025 14:37:23 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:d207cc66da44f4d060efb9a20dc200ca0e6b10c76276d0c1db9c735eaee1d506`  
		Last Modified: Tue, 21 Oct 2025 00:19:22 GMT  
		Size: 30.3 MB (30258365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65382ca1b15e9ba1efdf10fd01865db9594ef8af9c86896b3634b200068f380f`  
		Last Modified: Tue, 21 Oct 2025 01:43:33 GMT  
		Size: 5.2 MB (5224230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a789dd399271790f89b866ca519f073df004d1a69bae5e615b4227c7092c9e6`  
		Last Modified: Tue, 21 Oct 2025 01:43:36 GMT  
		Size: 35.0 MB (35011818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39fb0d61f010117ac3f7d213ba5548040a6313bcdd4406e653363f37d6f4fefc`  
		Last Modified: Tue, 21 Oct 2025 01:43:34 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17d2b2d4dde93dad32d23e6a5370bb492a49f77b4cdd0b98cfaa2d8d4e41c153`  
		Last Modified: Tue, 21 Oct 2025 01:43:34 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99472c167064d1fb2369a32873afdb224a927536f434d475856b72aec5c68501`  
		Last Modified: Tue, 21 Oct 2025 01:43:34 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9` - unknown; unknown

```console
$ docker pull chronograf@sha256:5063c01a4c67bf7b5ef724d7ce6ed39307941eb35dc0caf96933a63c650f38f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3125531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5cf9ec6f267b3ee4a7489240f7a05cc67fb436d936d8b4a33e652b39b205d18`

```dockerfile
```

-	Layers:
	-	`sha256:17961d5e6969acbce04a30f9e0bfa0a1c3f845eb3315518cef05cdb2cd2f8e07`  
		Last Modified: Tue, 21 Oct 2025 09:39:11 GMT  
		Size: 3.1 MB (3109721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0142f0569d0b0606c878bcf1634527a0f1543bce0be479307fe2df1270f5e4ce`  
		Last Modified: Tue, 21 Oct 2025 09:39:12 GMT  
		Size: 15.8 KB (15810 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.9` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:1ce07b0bea76bacb07b68dd747a9c7b8d1b1a2e7a631ced8fc9ca2d6543c3f47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.4 MB (63372315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c811e2dd38938b50031c399ad6c31f5f79399aa50171ba962371062aa5ff405`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 15 Aug 2025 14:37:23 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1760918400'
# Fri, 15 Aug 2025 14:37:23 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Fri, 15 Aug 2025 14:37:23 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 15 Aug 2025 14:37:23 GMT
VOLUME [/var/lib/chronograf]
# Fri, 15 Aug 2025 14:37:23 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:4b897c04dec26603bcc1b01b4283220cd1ffb208f0ec4c0db9e08dab58fcfb5d`  
		Last Modified: Tue, 21 Oct 2025 00:20:34 GMT  
		Size: 25.5 MB (25546187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf1235dcfeaabfd105342da22688b5e418379ac3b5ea9f0a4f423f986ffbdf9d`  
		Last Modified: Tue, 21 Oct 2025 02:46:24 GMT  
		Size: 4.5 MB (4490179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75fa9f41c4841b26c4ed7fc9b2351a9c5a450e82a556f876b879ac1f5bd71a44`  
		Last Modified: Tue, 21 Oct 2025 02:46:29 GMT  
		Size: 33.3 MB (33311563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:080567a325ba028cc9ab32fe60887d39a20d46736fb000b59918c94fa8737675`  
		Last Modified: Tue, 21 Oct 2025 02:46:24 GMT  
		Size: 12.2 KB (12244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dba856093b84f24dce1efe0cc4d61433c65893e479c70cb1719f022d242e0e28`  
		Last Modified: Tue, 21 Oct 2025 02:46:24 GMT  
		Size: 11.9 KB (11903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fe2df3a708651ca683798d5e8bc0590acfbf6ae45756d61adfa3b0bdcd9e475`  
		Last Modified: Tue, 21 Oct 2025 02:46:24 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9` - unknown; unknown

```console
$ docker pull chronograf@sha256:229399c1da1dcb14932ca3b586cf8bca677373b43dfe8a4ccd33fa3100c789ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3127879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3d88ac8b16d5d6a6de48cfff922616e9caae4b9773a184015100151c8908700`

```dockerfile
```

-	Layers:
	-	`sha256:05b003ce93fc9cbbe0e06fd809336e89af1859a454f9401c008583f524e843fd`  
		Last Modified: Tue, 21 Oct 2025 09:39:16 GMT  
		Size: 3.1 MB (3111992 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81fed343f9d07112c37286c1810a0a009bfb935f0e81a2f627ab2b14548eb71c`  
		Last Modified: Tue, 21 Oct 2025 09:39:17 GMT  
		Size: 15.9 KB (15887 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.9` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:07409011bfbd1ef1642e7ced3a8a6972e7b82db30e73a32d6cab0219c285967c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.2 MB (67163104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35a188dbc1adf6f59ed5c50b12f0663945fab857bb2871870ad02c7978f8dd83`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 15 Aug 2025 14:37:23 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1760918400'
# Fri, 15 Aug 2025 14:37:23 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Fri, 15 Aug 2025 14:37:23 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 15 Aug 2025 14:37:23 GMT
VOLUME [/var/lib/chronograf]
# Fri, 15 Aug 2025 14:37:23 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:40bdde71139ce202a6b0b5346000bda907331b21efec94960489d60568d26752`  
		Last Modified: Tue, 21 Oct 2025 00:19:19 GMT  
		Size: 28.7 MB (28748401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ee4bb34415c567092d70ec2dd9665a2af4bec19cbbceaf253da019ea294062f`  
		Last Modified: Tue, 21 Oct 2025 01:47:37 GMT  
		Size: 5.2 MB (5208160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a292b384e98bba87e55a84127d7f039b6d0108b0c3c623264a117f06f4c77370`  
		Last Modified: Tue, 21 Oct 2025 01:47:39 GMT  
		Size: 33.2 MB (33182159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad6e2ca61287ae0f05c41085ca44539657f565ea6b1326cfe90a07052da03471`  
		Last Modified: Tue, 21 Oct 2025 01:47:36 GMT  
		Size: 12.2 KB (12242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04dcb1624f763f979714862784b6d51816a7eeeded2a95a9c1450809b31e38e0`  
		Last Modified: Tue, 21 Oct 2025 01:47:36 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:615e76c45a3796236089eec1a08f6f316deeed2797ba07be10b6f66732b49d0f`  
		Last Modified: Tue, 21 Oct 2025 01:47:36 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9` - unknown; unknown

```console
$ docker pull chronograf@sha256:5467c7e925e8c2586f9dfce498ce025e3f3b46743eeb1106ad36ae1170e1aba8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3125875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14ae427f7cd6fdbfe27300cf51be047deffded9401d011036025d515c218779f`

```dockerfile
```

-	Layers:
	-	`sha256:8b56dfbebe66a54637b774031e3fb46f66085c85895ddccba26704baed6413dc`  
		Last Modified: Tue, 21 Oct 2025 09:39:21 GMT  
		Size: 3.1 MB (3109970 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76aa0b8038d00c56e6488b8fe5f2b5eb433c756dffc6fb3fa66b33191d2f2791`  
		Last Modified: Tue, 21 Oct 2025 09:39:22 GMT  
		Size: 15.9 KB (15905 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.9-alpine`

```console
$ docker pull chronograf@sha256:b3fee5aad5c22c71cb04bbd41eea4af839aeb7d359a82d9b4233795d4cee5130
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.9-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:2d4252cb73b369cd488e239afeef5f7a6b44a46a01cfe8ab7d068d6397d5311d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23614563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9964a18d639210346c0ff7c26e65b91960ad4afbf36654d3a88e1c03026a1437`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 15 Aug 2025 14:37:23 GMT
ADD alpine-minirootfs-3.20.8-x86_64.tar.gz / # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["/bin/sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Fri, 15 Aug 2025 14:37:23 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 15 Aug 2025 14:37:23 GMT
VOLUME [/var/lib/chronograf]
# Fri, 15 Aug 2025 14:37:23 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:5311e7f182d02360a7194aa2995849bcdf04795c39a0ffdcf413eae625865970`  
		Last Modified: Wed, 08 Oct 2025 12:03:10 GMT  
		Size: 3.6 MB (3627056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d70c842384492021fdcd617e3e57dbc08546ebeb0a55cf5f01aa575170280c6`  
		Last Modified: Wed, 08 Oct 2025 23:01:25 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e6c508c6ab14eb797ff6524630894eea223ff1b5a3f02be3595aff5713c5112`  
		Last Modified: Wed, 08 Oct 2025 23:01:25 GMT  
		Size: 290.8 KB (290774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43383a0cdbbe70773cd822a7089d90f254cc6923262bc86a209c0c182a190472`  
		Last Modified: Wed, 08 Oct 2025 23:01:26 GMT  
		Size: 19.7 MB (19672095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11524f4d626f224d1faadbb2537a398d423351e2a0d854a4a43b4692fab631c6`  
		Last Modified: Wed, 08 Oct 2025 23:01:25 GMT  
		Size: 12.2 KB (12232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:811766d26cc20ed9c9dee509c4ef17aa945fbbf00be418890deec226cbeae620`  
		Last Modified: Wed, 08 Oct 2025 23:01:25 GMT  
		Size: 11.9 KB (11888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90296708765453bd34d3b31917ee366ec4e86d0d341504ddd046c032d6f85842`  
		Last Modified: Wed, 08 Oct 2025 23:01:25 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:c5e372192d09b31155c48fb1472089780f956a2cdeba37b4eda3358869e38aec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.5 KB (250462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad16fab4bfdaa94339daa5b35ee736124878a90af7d436293dd5657f43ac1f79`

```dockerfile
```

-	Layers:
	-	`sha256:6ed1879bf7ef8eb915186029d90ae2f6c3d14aa17bd74c3708035ff07dfcc75e`  
		Last Modified: Thu, 09 Oct 2025 00:38:42 GMT  
		Size: 233.6 KB (233553 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5586220b931721e2b29f86f48af9fa3579d18c357b0351f043fc2e76a05ebc52`  
		Last Modified: Thu, 09 Oct 2025 00:38:42 GMT  
		Size: 16.9 KB (16909 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.9.4`

```console
$ docker pull chronograf@sha256:5a97bdd06430abb6b6541bb66a965396334126f9b6f6e66d945af1c3b3ea798f
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
$ docker pull chronograf@sha256:dbf638ede671617f87ef9e4fa556bbcc791c9a1a3fedc2f8bc7c2776c3daad17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.5 MB (70518809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41d7cfc1fe10a12a9535417379672d1359adbb1c3a7e6265e4f9cbe73dca8bdb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 15 Aug 2025 14:37:23 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1760918400'
# Fri, 15 Aug 2025 14:37:23 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Fri, 15 Aug 2025 14:37:23 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 15 Aug 2025 14:37:23 GMT
VOLUME [/var/lib/chronograf]
# Fri, 15 Aug 2025 14:37:23 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:d207cc66da44f4d060efb9a20dc200ca0e6b10c76276d0c1db9c735eaee1d506`  
		Last Modified: Tue, 21 Oct 2025 00:19:22 GMT  
		Size: 30.3 MB (30258365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65382ca1b15e9ba1efdf10fd01865db9594ef8af9c86896b3634b200068f380f`  
		Last Modified: Tue, 21 Oct 2025 01:43:33 GMT  
		Size: 5.2 MB (5224230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a789dd399271790f89b866ca519f073df004d1a69bae5e615b4227c7092c9e6`  
		Last Modified: Tue, 21 Oct 2025 01:43:36 GMT  
		Size: 35.0 MB (35011818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39fb0d61f010117ac3f7d213ba5548040a6313bcdd4406e653363f37d6f4fefc`  
		Last Modified: Tue, 21 Oct 2025 01:43:34 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17d2b2d4dde93dad32d23e6a5370bb492a49f77b4cdd0b98cfaa2d8d4e41c153`  
		Last Modified: Tue, 21 Oct 2025 01:43:34 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99472c167064d1fb2369a32873afdb224a927536f434d475856b72aec5c68501`  
		Last Modified: Tue, 21 Oct 2025 01:43:34 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9.4` - unknown; unknown

```console
$ docker pull chronograf@sha256:5063c01a4c67bf7b5ef724d7ce6ed39307941eb35dc0caf96933a63c650f38f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3125531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5cf9ec6f267b3ee4a7489240f7a05cc67fb436d936d8b4a33e652b39b205d18`

```dockerfile
```

-	Layers:
	-	`sha256:17961d5e6969acbce04a30f9e0bfa0a1c3f845eb3315518cef05cdb2cd2f8e07`  
		Last Modified: Tue, 21 Oct 2025 09:39:11 GMT  
		Size: 3.1 MB (3109721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0142f0569d0b0606c878bcf1634527a0f1543bce0be479307fe2df1270f5e4ce`  
		Last Modified: Tue, 21 Oct 2025 09:39:12 GMT  
		Size: 15.8 KB (15810 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.9.4` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:1ce07b0bea76bacb07b68dd747a9c7b8d1b1a2e7a631ced8fc9ca2d6543c3f47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.4 MB (63372315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c811e2dd38938b50031c399ad6c31f5f79399aa50171ba962371062aa5ff405`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 15 Aug 2025 14:37:23 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1760918400'
# Fri, 15 Aug 2025 14:37:23 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Fri, 15 Aug 2025 14:37:23 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 15 Aug 2025 14:37:23 GMT
VOLUME [/var/lib/chronograf]
# Fri, 15 Aug 2025 14:37:23 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:4b897c04dec26603bcc1b01b4283220cd1ffb208f0ec4c0db9e08dab58fcfb5d`  
		Last Modified: Tue, 21 Oct 2025 00:20:34 GMT  
		Size: 25.5 MB (25546187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf1235dcfeaabfd105342da22688b5e418379ac3b5ea9f0a4f423f986ffbdf9d`  
		Last Modified: Tue, 21 Oct 2025 02:46:24 GMT  
		Size: 4.5 MB (4490179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75fa9f41c4841b26c4ed7fc9b2351a9c5a450e82a556f876b879ac1f5bd71a44`  
		Last Modified: Tue, 21 Oct 2025 02:46:29 GMT  
		Size: 33.3 MB (33311563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:080567a325ba028cc9ab32fe60887d39a20d46736fb000b59918c94fa8737675`  
		Last Modified: Tue, 21 Oct 2025 02:46:24 GMT  
		Size: 12.2 KB (12244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dba856093b84f24dce1efe0cc4d61433c65893e479c70cb1719f022d242e0e28`  
		Last Modified: Tue, 21 Oct 2025 02:46:24 GMT  
		Size: 11.9 KB (11903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fe2df3a708651ca683798d5e8bc0590acfbf6ae45756d61adfa3b0bdcd9e475`  
		Last Modified: Tue, 21 Oct 2025 02:46:24 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9.4` - unknown; unknown

```console
$ docker pull chronograf@sha256:229399c1da1dcb14932ca3b586cf8bca677373b43dfe8a4ccd33fa3100c789ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3127879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3d88ac8b16d5d6a6de48cfff922616e9caae4b9773a184015100151c8908700`

```dockerfile
```

-	Layers:
	-	`sha256:05b003ce93fc9cbbe0e06fd809336e89af1859a454f9401c008583f524e843fd`  
		Last Modified: Tue, 21 Oct 2025 09:39:16 GMT  
		Size: 3.1 MB (3111992 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81fed343f9d07112c37286c1810a0a009bfb935f0e81a2f627ab2b14548eb71c`  
		Last Modified: Tue, 21 Oct 2025 09:39:17 GMT  
		Size: 15.9 KB (15887 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.9.4` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:07409011bfbd1ef1642e7ced3a8a6972e7b82db30e73a32d6cab0219c285967c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.2 MB (67163104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35a188dbc1adf6f59ed5c50b12f0663945fab857bb2871870ad02c7978f8dd83`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 15 Aug 2025 14:37:23 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1760918400'
# Fri, 15 Aug 2025 14:37:23 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Fri, 15 Aug 2025 14:37:23 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 15 Aug 2025 14:37:23 GMT
VOLUME [/var/lib/chronograf]
# Fri, 15 Aug 2025 14:37:23 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:40bdde71139ce202a6b0b5346000bda907331b21efec94960489d60568d26752`  
		Last Modified: Tue, 21 Oct 2025 00:19:19 GMT  
		Size: 28.7 MB (28748401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ee4bb34415c567092d70ec2dd9665a2af4bec19cbbceaf253da019ea294062f`  
		Last Modified: Tue, 21 Oct 2025 01:47:37 GMT  
		Size: 5.2 MB (5208160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a292b384e98bba87e55a84127d7f039b6d0108b0c3c623264a117f06f4c77370`  
		Last Modified: Tue, 21 Oct 2025 01:47:39 GMT  
		Size: 33.2 MB (33182159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad6e2ca61287ae0f05c41085ca44539657f565ea6b1326cfe90a07052da03471`  
		Last Modified: Tue, 21 Oct 2025 01:47:36 GMT  
		Size: 12.2 KB (12242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04dcb1624f763f979714862784b6d51816a7eeeded2a95a9c1450809b31e38e0`  
		Last Modified: Tue, 21 Oct 2025 01:47:36 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:615e76c45a3796236089eec1a08f6f316deeed2797ba07be10b6f66732b49d0f`  
		Last Modified: Tue, 21 Oct 2025 01:47:36 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9.4` - unknown; unknown

```console
$ docker pull chronograf@sha256:5467c7e925e8c2586f9dfce498ce025e3f3b46743eeb1106ad36ae1170e1aba8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3125875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14ae427f7cd6fdbfe27300cf51be047deffded9401d011036025d515c218779f`

```dockerfile
```

-	Layers:
	-	`sha256:8b56dfbebe66a54637b774031e3fb46f66085c85895ddccba26704baed6413dc`  
		Last Modified: Tue, 21 Oct 2025 09:39:21 GMT  
		Size: 3.1 MB (3109970 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76aa0b8038d00c56e6488b8fe5f2b5eb433c756dffc6fb3fa66b33191d2f2791`  
		Last Modified: Tue, 21 Oct 2025 09:39:22 GMT  
		Size: 15.9 KB (15905 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.9.4-alpine`

```console
$ docker pull chronograf@sha256:b3fee5aad5c22c71cb04bbd41eea4af839aeb7d359a82d9b4233795d4cee5130
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.9.4-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:2d4252cb73b369cd488e239afeef5f7a6b44a46a01cfe8ab7d068d6397d5311d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23614563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9964a18d639210346c0ff7c26e65b91960ad4afbf36654d3a88e1c03026a1437`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 15 Aug 2025 14:37:23 GMT
ADD alpine-minirootfs-3.20.8-x86_64.tar.gz / # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["/bin/sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Fri, 15 Aug 2025 14:37:23 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 15 Aug 2025 14:37:23 GMT
VOLUME [/var/lib/chronograf]
# Fri, 15 Aug 2025 14:37:23 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:5311e7f182d02360a7194aa2995849bcdf04795c39a0ffdcf413eae625865970`  
		Last Modified: Wed, 08 Oct 2025 12:03:10 GMT  
		Size: 3.6 MB (3627056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d70c842384492021fdcd617e3e57dbc08546ebeb0a55cf5f01aa575170280c6`  
		Last Modified: Wed, 08 Oct 2025 23:01:25 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e6c508c6ab14eb797ff6524630894eea223ff1b5a3f02be3595aff5713c5112`  
		Last Modified: Wed, 08 Oct 2025 23:01:25 GMT  
		Size: 290.8 KB (290774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43383a0cdbbe70773cd822a7089d90f254cc6923262bc86a209c0c182a190472`  
		Last Modified: Wed, 08 Oct 2025 23:01:26 GMT  
		Size: 19.7 MB (19672095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11524f4d626f224d1faadbb2537a398d423351e2a0d854a4a43b4692fab631c6`  
		Last Modified: Wed, 08 Oct 2025 23:01:25 GMT  
		Size: 12.2 KB (12232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:811766d26cc20ed9c9dee509c4ef17aa945fbbf00be418890deec226cbeae620`  
		Last Modified: Wed, 08 Oct 2025 23:01:25 GMT  
		Size: 11.9 KB (11888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90296708765453bd34d3b31917ee366ec4e86d0d341504ddd046c032d6f85842`  
		Last Modified: Wed, 08 Oct 2025 23:01:25 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9.4-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:c5e372192d09b31155c48fb1472089780f956a2cdeba37b4eda3358869e38aec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.5 KB (250462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad16fab4bfdaa94339daa5b35ee736124878a90af7d436293dd5657f43ac1f79`

```dockerfile
```

-	Layers:
	-	`sha256:6ed1879bf7ef8eb915186029d90ae2f6c3d14aa17bd74c3708035ff07dfcc75e`  
		Last Modified: Thu, 09 Oct 2025 00:38:42 GMT  
		Size: 233.6 KB (233553 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5586220b931721e2b29f86f48af9fa3579d18c357b0351f043fc2e76a05ebc52`  
		Last Modified: Thu, 09 Oct 2025 00:38:42 GMT  
		Size: 16.9 KB (16909 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:alpine`

```console
$ docker pull chronograf@sha256:efc72c285cae492b0fb820a7794f2da69a70ef77caa8d28282e0df6f79856029
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:08463b31a0a2617a51e230161f997b525214640155e291a423ae53004330c719
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.7 MB (32700225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8af178eb7af41f52d85b69957fc583d381f6a24a9e604b40818766ecf3004a1a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 15 Aug 2025 14:37:23 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["/bin/sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
RUN apk add --no-cache ca-certificates setpriv &&     update-ca-certificates # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENV CHRONOGRAF_VERSION=1.10.8
# Fri, 15 Aug 2025 14:37:23 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S chronograf &&     adduser -S chronograf -G chronograf &&     mkdir -m 0750 -p /var/lib/chronograf &&     chown chronograf:chronograf /var/lib/chronograf # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 15 Aug 2025 14:37:23 GMT
VOLUME [/var/lib/chronograf]
# Fri, 15 Aug 2025 14:37:23 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f08cd1461c07b6d2b803ff1e365582cea280da85884cb0fe20c1b539046e9c0f`  
		Last Modified: Wed, 08 Oct 2025 23:01:28 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:642952c8832a913bc8124d8c1f9800b4c40ed32aa2d21f4bbd9c85e32729fdf2`  
		Last Modified: Wed, 08 Oct 2025 23:01:28 GMT  
		Size: 314.6 KB (314639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff188fbd44ef51d6c15c61b590915a7d108294cea3cebd1224f569cf88dbfbd2`  
		Last Modified: Wed, 08 Oct 2025 23:01:31 GMT  
		Size: 28.6 MB (28558408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ada6ea712a91804f080e3ac3a6fec72f1bf330d8affb0a76902b1f0b78a5046`  
		Last Modified: Wed, 08 Oct 2025 23:01:28 GMT  
		Size: 12.2 KB (12237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:322d214c5daa6878e468360de897da9cd0cad1be05283f5529b5e2ce07c9e72f`  
		Last Modified: Wed, 08 Oct 2025 23:01:28 GMT  
		Size: 11.9 KB (11895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:175f9d62a6d73ab836332ca97429aec6104967dc35d5ab6aaa103f374c1539bd`  
		Last Modified: Wed, 08 Oct 2025 23:01:28 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:dd3236bd7a2263357f0c7258a9a36c7fef283fd9f58f17f5fc2cbfa8330df313
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.2 KB (268238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:808a56c94ce865ff68fe325760f90b15b31758031ea028455935f57e4d2afe56`

```dockerfile
```

-	Layers:
	-	`sha256:d62aac69b78bc656cc8510a0566537353a4cda897cdaf124ca24ad68c0fa7fb1`  
		Last Modified: Thu, 09 Oct 2025 00:38:17 GMT  
		Size: 250.4 KB (250383 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c7ffc31e817e3fff1eade663dcae6dc3da5bb4370e43abaf921eebc9dd7f0a1`  
		Last Modified: Thu, 09 Oct 2025 00:38:18 GMT  
		Size: 17.9 KB (17855 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:latest`

```console
$ docker pull chronograf@sha256:9f0069d5e74770b48d357f8007df8068ccb20353ae1cd9b1d3c68712d34c37b7
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
$ docker pull chronograf@sha256:8e22ca42eca51af0770099dfd8d36924a51de213c107c50286aedb5a9fecb1e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.4 MB (85408161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3285e8978ea95e807515b6f3f620464e98d8386928a0973148decdf52c0ef5f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 15 Aug 2025 14:37:23 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1760918400'
# Fri, 15 Aug 2025 14:37:23 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENV CHRONOGRAF_VERSION=1.10.8
# Fri, 15 Aug 2025 14:37:23 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 15 Aug 2025 14:37:23 GMT
VOLUME [/var/lib/chronograf]
# Fri, 15 Aug 2025 14:37:23 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:abe1fea375429ba91b23776f15f53da4ed790fa2b779b40d20f21e69bd66de5a`  
		Last Modified: Tue, 21 Oct 2025 00:19:19 GMT  
		Size: 28.2 MB (28228321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d678f7ea98bc9cde3cdc6f3822daf66c286a55145d5059c1ab6c170401471c4`  
		Last Modified: Tue, 21 Oct 2025 01:43:32 GMT  
		Size: 7.9 MB (7878755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1823d4badf365aba7b0fd3f98cff8b0abaff5803f47b8d57fbaeeb656471aaba`  
		Last Modified: Tue, 21 Oct 2025 01:43:41 GMT  
		Size: 49.3 MB (49276618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7715f277f40ad8ce01cbe83aa480fed068eb208132e1f1fd18dfec1ad82db60`  
		Last Modified: Tue, 21 Oct 2025 01:43:32 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:612be43be9a1667d3407539a10d5ac2ee077fa118ee89b45931f0c208c3807bf`  
		Last Modified: Tue, 21 Oct 2025 01:43:32 GMT  
		Size: 11.9 KB (11903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d40e348cd71352ccc887adef3c8508b00e9365e7eb81c4a82f557bfca578293`  
		Last Modified: Tue, 21 Oct 2025 01:43:32 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:ad8cbe492cda8ed466b5bfceee4c067234a11ad5d563254ca2ef0464fcdca1f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2870202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8ab40ab435551a74d356b54da4e19abedd945d17b41755c881256ead253ab52`

```dockerfile
```

-	Layers:
	-	`sha256:0b5d752ece03c44d95a557c603adf74579763ef225bb2cbfe38468b0e2b15134`  
		Last Modified: Tue, 21 Oct 2025 09:38:25 GMT  
		Size: 2.9 MB (2854074 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ceda444489ed6780403e9c2aadba05d5c2b42a2cc6307f16d07c466c2d98ec52`  
		Last Modified: Tue, 21 Oct 2025 09:38:25 GMT  
		Size: 16.1 KB (16128 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:latest` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:1eb13a30653187377adf857362ebf6ad28bb1be8b6dce31f702e7a85f76ab352
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76088345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f743908bb2d47bfb245efff0d344b461c09d68649b31deaf8e14796c39b60af6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 15 Aug 2025 14:37:23 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1760918400'
# Fri, 15 Aug 2025 14:37:23 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENV CHRONOGRAF_VERSION=1.10.8
# Fri, 15 Aug 2025 14:37:23 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 15 Aug 2025 14:37:23 GMT
VOLUME [/var/lib/chronograf]
# Fri, 15 Aug 2025 14:37:23 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:4f520125372ffa3e5f64f19eebfdfce1c8314446e9e3ab2629f5c13cacbd8345`  
		Last Modified: Tue, 21 Oct 2025 00:20:18 GMT  
		Size: 23.9 MB (23934023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9b9cbeab7d89257c02df3df623dbb0db0b03ff0dacad804425d03c0c6bc538f`  
		Last Modified: Tue, 21 Oct 2025 02:48:15 GMT  
		Size: 6.5 MB (6508047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:483e264e639c89e02d166ec79b2c1a646f8a597f6b7f64e075012186ba1f257e`  
		Last Modified: Tue, 21 Oct 2025 02:48:18 GMT  
		Size: 45.6 MB (45621809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e30658b9289a25d89d66fd38b677bf33aab69f2b04e80a707c57437215f1ef49`  
		Last Modified: Tue, 21 Oct 2025 02:48:14 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47956f4970e0f490a78bc21edeef2c2c72c756000f50b21c9644801538fef1e1`  
		Last Modified: Tue, 21 Oct 2025 02:48:14 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13da7c92b57d7e1af6e5c05141a0cccdae906f9f905eac3ba3a2c2d11cc0ea83`  
		Last Modified: Tue, 21 Oct 2025 02:48:14 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:eb3600838cbf523178cf02ba62cddb9aeb6954442b16f7b3199129ebc555a75e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2872584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68df4bb273f5e075b878118d7f75b73f44394c9cbdcf0168a86f5d0bbc5cee15`

```dockerfile
```

-	Layers:
	-	`sha256:76f5f9bb4a19323ff3e5bbf4ebe978240554408deb1602b69c9585473d403666`  
		Last Modified: Tue, 21 Oct 2025 09:38:29 GMT  
		Size: 2.9 MB (2856371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f68f79b94989765e47276910de76c69663b987742ad04584fe7b0dd6009a761b`  
		Last Modified: Tue, 21 Oct 2025 09:38:30 GMT  
		Size: 16.2 KB (16213 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:latest` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:113b7e3cac741fa1e3247a9cae8b958bd60881497da3522ca371fe48300a5b74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.9 MB (82885222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78be669f8c5ec34a56c042c2f6039c64076f1fcc76c54bf1fa5d924777de9fec`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 15 Aug 2025 14:37:23 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1760918400'
# Fri, 15 Aug 2025 14:37:23 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENV CHRONOGRAF_VERSION=1.10.8
# Fri, 15 Aug 2025 14:37:23 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 15 Aug 2025 14:37:23 GMT
VOLUME [/var/lib/chronograf]
# Fri, 15 Aug 2025 14:37:23 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:21b7accdc53fc02b56a5c1cccd412be04189e5a5e674fd092ffbedc72596be91`  
		Last Modified: Tue, 21 Oct 2025 00:18:57 GMT  
		Size: 28.1 MB (28102190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57847360efefbe97c6032227969a42bcd11fb0de5f8a7c988562801256856d9c`  
		Last Modified: Tue, 21 Oct 2025 01:47:59 GMT  
		Size: 7.7 MB (7691784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24a918b13d7ee929fee3564b1f4a8fa48e9589b846d399d39bd00bd3706efc80`  
		Last Modified: Tue, 21 Oct 2025 01:48:04 GMT  
		Size: 47.1 MB (47066776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:374fd9f33dcbadd2f16dfbc41a0a6ff13c7d47122d503c0c2d2fbd5c0ee89402`  
		Last Modified: Tue, 21 Oct 2025 01:47:59 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb2ed856870944b103a5a36bde6d94fadae3f7c49b1b938759b5c11771bfce7d`  
		Last Modified: Tue, 21 Oct 2025 01:47:59 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b769d03b89d7173d3468a7148bdaeaabb6283887b02bc55d9cee4c147439578`  
		Last Modified: Tue, 21 Oct 2025 01:48:00 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:6b186910c1614e00ad47ee34f42fc5e5f377e0a3cd954e6db6f6297b3d5f7517
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2870582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3d006836f764de414f23cfb6ab70e4c70e43facebc9d32443ba15b850a72b37`

```dockerfile
```

-	Layers:
	-	`sha256:f966f9b47cbb4657cec2c202c92f1d51d230717ec1a948e8f76fa115c46f1c8b`  
		Last Modified: Tue, 21 Oct 2025 09:38:34 GMT  
		Size: 2.9 MB (2854347 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e91722f76a858459622d6a244a19d8ed86fe848ae9085cb9902257a44a8387fd`  
		Last Modified: Tue, 21 Oct 2025 09:38:35 GMT  
		Size: 16.2 KB (16235 bytes)  
		MIME: application/vnd.in-toto+json
