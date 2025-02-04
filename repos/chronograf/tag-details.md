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
$ docker pull chronograf@sha256:6a7f7bd8b9459f85b2505cc6e5b991eedf7ec92bce1e984fdcb430e1cde78b09
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
$ docker pull chronograf@sha256:5c778bc81892bf7d857e84056d7f404c08d8e1a8b3a61b8be78c3456444e6c3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.3 MB (83329784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dc6296f978c36c764aeba47abfda2c2f8cfb6b6d335e6613447702b2671f9dc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
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
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea4677274335b6d13e9d85d2cb59ce3c040ab4fe297a219c71486d0a997fdf60`  
		Last Modified: Tue, 04 Feb 2025 04:38:20 GMT  
		Size: 7.9 MB (7875460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e341bdf0db524398c580141c359facb380260a87e863fd011ab4f9fd9f18700`  
		Last Modified: Tue, 04 Feb 2025 04:38:20 GMT  
		Size: 47.2 MB (47217554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5b773fd7294d9043bd106a1bd32e4ae5d935c95fa2f6c71e8402c967af36daa`  
		Last Modified: Tue, 04 Feb 2025 04:38:19 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:959c37d0b325d913afc6820bc08751b8c345ececd2e9019a6eebe37bbbef5fed`  
		Last Modified: Tue, 04 Feb 2025 04:38:20 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b22ab05d59f0f8196b08ac45a7b94f98c851c519e6c70a6c1c99113ca2fb67ed`  
		Last Modified: Tue, 04 Feb 2025 04:38:20 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:1b2e6e5404f443d80444bddcc3f103f3b8f87280e6912fae9f228d314a7877d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2719989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7461f550112f8d4354117a9c1ef0e0bc7ece095b4991a5f14e7ae843b83643c`

```dockerfile
```

-	Layers:
	-	`sha256:4d2610d19117b875074759f759521347e466a19de34b8e92d9f6758c8f854b06`  
		Last Modified: Tue, 04 Feb 2025 04:38:20 GMT  
		Size: 2.7 MB (2703861 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c59690fa3689bb8814d4273ccbf864c2d4cb427966be0444f656eb830c15c81`  
		Last Modified: Tue, 04 Feb 2025 04:38:19 GMT  
		Size: 16.1 KB (16128 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.10` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:b8eaf491a3d51ab1ad081116051d6319665ea6a159f15552fb042a8880452e0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74713234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1631585b9c6c1e93b600a77695687e7dd10bb578920dd6f3c03efc21143d4f7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1736726400'
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
	-	`sha256:f7fde15b664589586a61b714ca6b43dec045d0f187d81d4eb050918e17b0ff1e`  
		Last Modified: Tue, 14 Jan 2025 01:35:15 GMT  
		Size: 23.9 MB (23914600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31eb12efed5eb5b137542a8591ffaddcfec2ab7fbb3e4d81891c4d2ddc47283c`  
		Last Modified: Tue, 14 Jan 2025 09:02:48 GMT  
		Size: 6.5 MB (6497830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff49de7a4cba1c7f1e033fadd98d847bc9f2aed1a1b8faac5681a4d17c5590ec`  
		Last Modified: Tue, 14 Jan 2025 09:02:48 GMT  
		Size: 44.3 MB (44276343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52c409b1b91c6fc27ad30d021a65179e77d13efde84ee96abf30a124f3a86825`  
		Last Modified: Tue, 14 Jan 2025 09:02:46 GMT  
		Size: 12.2 KB (12244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9d49e53e707da3ed5d73b62a4fe374bad1d91274ce451a98133353442723fb9`  
		Last Modified: Tue, 14 Jan 2025 09:02:47 GMT  
		Size: 11.9 KB (11903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:639c7cd00071a0b62766d53b22370535830272a699de91971e54d828c113c6c2`  
		Last Modified: Tue, 14 Jan 2025 09:02:47 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:cb2388b11815c41e02b9ed158ee6d627b8e7e9ba4baae043731552a2ce9f769e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2722366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a07c2b25ff90a5be47dfbfe81063611749d333225960cec7a16874dd2006fd37`

```dockerfile
```

-	Layers:
	-	`sha256:e00d8906b7526bc8bca4dbd34a2d75af98b178ba57c9dc6badeb508556ff8f5f`  
		Last Modified: Tue, 14 Jan 2025 09:02:47 GMT  
		Size: 2.7 MB (2706158 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:309aae5baec8f6e76452e0ee1b5f805d2e41571eee241086ef065f31862b2e51`  
		Last Modified: Tue, 14 Jan 2025 09:02:46 GMT  
		Size: 16.2 KB (16208 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.10` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:e9d2adcbf05b367178d80afae5a4be65bd9d108b97ccd30e3a2e9b762fea0d4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.7 MB (80688086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04eb7b75c8d8d64b5e28916f2541f39346c1027d02cdf4fa472b6650baad04af`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
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
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe5e22ffc62c19f88c63e73d68f6271af6579883314b212065a1f3f823822404`  
		Last Modified: Tue, 14 Jan 2025 07:03:13 GMT  
		Size: 7.7 MB (7652088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9be9572b2df6cf01e21eceea0c61e00397c4baf86724385e960030ed5c53b598`  
		Last Modified: Tue, 14 Jan 2025 07:03:14 GMT  
		Size: 45.0 MB (44970507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d41d08252d2d81e968b86f218af88b55a264ed843cf51c41ee846cada501a2a`  
		Last Modified: Tue, 14 Jan 2025 07:03:12 GMT  
		Size: 12.2 KB (12243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee5d82b281a9621c48cced8f12640673ffafe06d54a29b7fd724247b1f8f95bc`  
		Last Modified: Tue, 14 Jan 2025 07:03:12 GMT  
		Size: 11.9 KB (11902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f9a4caa4163798a2515cd4a99fff2a3633d45f79045264085c0e6df6fee2b2a`  
		Last Modified: Tue, 14 Jan 2025 07:03:13 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:125aa83ae8a8ff760a9654a30dfecdaea5cd9c8c4dab202c68a7e84528a142f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2720369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:829ced801ce3aa5bbc969ab7e89d23f24cf6ebf385b222e94b27c2c48913a446`

```dockerfile
```

-	Layers:
	-	`sha256:8110c7aede011c065bc590dfb8d4c5f389270f45ffc4f9103cb3a9de4099299f`  
		Last Modified: Tue, 14 Jan 2025 07:03:13 GMT  
		Size: 2.7 MB (2704134 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2d534b8b0f8a046a6dcbd52c6eab0e8a1e013b983679b8f41cc875a2b9aa1ca`  
		Last Modified: Tue, 14 Jan 2025 07:03:12 GMT  
		Size: 16.2 KB (16235 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.10-alpine`

```console
$ docker pull chronograf@sha256:fd22e60efc394d9cf49addff75db9896bdaa59a92831d5a649f57600241b5aef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.10-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:565eafbccd78da51863ddc5af1c325bd0755703b61e5058bf3f7bb8744fbfbd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31814451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99b96aa2eecd223e38af88a65ce94b8a24ce929843e8288f199df8966577e3c8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
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
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Wed, 08 Jan 2025 15:55:45 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f10033a10c25d8a78cc5c79537d8be6f9f9570d55e41149047e0eb842ff20ff7`  
		Last Modified: Wed, 08 Jan 2025 18:14:08 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e8e1ed9e8da33db6dd03408084a900ae90824d89fc2a9b14f453422b5119fe4`  
		Last Modified: Wed, 08 Jan 2025 18:14:08 GMT  
		Size: 296.5 KB (296485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13a1a285f7323a6ea298bbeb818f3c80ab849a601de7e3c5d4f18ed1737c58ab`  
		Last Modified: Wed, 08 Jan 2025 18:14:08 GMT  
		Size: 27.9 MB (27866995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0e09ce57cfd00606804f6da64b2f6d7ed8e7ebd061da4dd39492ae664d5f448`  
		Last Modified: Wed, 08 Jan 2025 18:14:08 GMT  
		Size: 12.2 KB (12240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d437e77355a9d05d3b5d3567741989e1cdf431b8932402e004f46d65d597880`  
		Last Modified: Wed, 08 Jan 2025 18:14:09 GMT  
		Size: 11.9 KB (11898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09cab2e3ba35d3a80672462930883bcc165643bc56c7a7cb85e2274f5f883bb6`  
		Last Modified: Wed, 08 Jan 2025 18:14:09 GMT  
		Size: 293.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:4726a1af05f478eacb4e6ae7496295c8268530b94e341d465ce0254387d21986
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.4 KB (259450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4773308778b046fbf1cbd918492fb3e6940cbc43a637d34229c4a2bfddd28643`

```dockerfile
```

-	Layers:
	-	`sha256:dc9afdf2d7e83acbbcf82584839e1029a9fc056cda18c507457ad2f4c11ae85b`  
		Last Modified: Wed, 08 Jan 2025 18:14:08 GMT  
		Size: 241.6 KB (241595 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb03332e1a4f6d331e2c7201bd529d7e3b2c5caf81b355aa80d22f0c624368bc`  
		Last Modified: Wed, 08 Jan 2025 18:14:08 GMT  
		Size: 17.9 KB (17855 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.10.5`

```console
$ docker pull chronograf@sha256:6a7f7bd8b9459f85b2505cc6e5b991eedf7ec92bce1e984fdcb430e1cde78b09
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
$ docker pull chronograf@sha256:5c778bc81892bf7d857e84056d7f404c08d8e1a8b3a61b8be78c3456444e6c3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.3 MB (83329784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dc6296f978c36c764aeba47abfda2c2f8cfb6b6d335e6613447702b2671f9dc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
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
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea4677274335b6d13e9d85d2cb59ce3c040ab4fe297a219c71486d0a997fdf60`  
		Last Modified: Tue, 04 Feb 2025 04:38:20 GMT  
		Size: 7.9 MB (7875460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e341bdf0db524398c580141c359facb380260a87e863fd011ab4f9fd9f18700`  
		Last Modified: Tue, 04 Feb 2025 04:38:20 GMT  
		Size: 47.2 MB (47217554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5b773fd7294d9043bd106a1bd32e4ae5d935c95fa2f6c71e8402c967af36daa`  
		Last Modified: Tue, 04 Feb 2025 04:38:19 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:959c37d0b325d913afc6820bc08751b8c345ececd2e9019a6eebe37bbbef5fed`  
		Last Modified: Tue, 04 Feb 2025 04:38:20 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b22ab05d59f0f8196b08ac45a7b94f98c851c519e6c70a6c1c99113ca2fb67ed`  
		Last Modified: Tue, 04 Feb 2025 04:38:20 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10.5` - unknown; unknown

```console
$ docker pull chronograf@sha256:1b2e6e5404f443d80444bddcc3f103f3b8f87280e6912fae9f228d314a7877d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2719989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7461f550112f8d4354117a9c1ef0e0bc7ece095b4991a5f14e7ae843b83643c`

```dockerfile
```

-	Layers:
	-	`sha256:4d2610d19117b875074759f759521347e466a19de34b8e92d9f6758c8f854b06`  
		Last Modified: Tue, 04 Feb 2025 04:38:20 GMT  
		Size: 2.7 MB (2703861 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c59690fa3689bb8814d4273ccbf864c2d4cb427966be0444f656eb830c15c81`  
		Last Modified: Tue, 04 Feb 2025 04:38:19 GMT  
		Size: 16.1 KB (16128 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.10.5` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:b8eaf491a3d51ab1ad081116051d6319665ea6a159f15552fb042a8880452e0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74713234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1631585b9c6c1e93b600a77695687e7dd10bb578920dd6f3c03efc21143d4f7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1736726400'
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
	-	`sha256:f7fde15b664589586a61b714ca6b43dec045d0f187d81d4eb050918e17b0ff1e`  
		Last Modified: Tue, 14 Jan 2025 01:35:15 GMT  
		Size: 23.9 MB (23914600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31eb12efed5eb5b137542a8591ffaddcfec2ab7fbb3e4d81891c4d2ddc47283c`  
		Last Modified: Tue, 14 Jan 2025 09:02:48 GMT  
		Size: 6.5 MB (6497830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff49de7a4cba1c7f1e033fadd98d847bc9f2aed1a1b8faac5681a4d17c5590ec`  
		Last Modified: Tue, 14 Jan 2025 09:02:48 GMT  
		Size: 44.3 MB (44276343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52c409b1b91c6fc27ad30d021a65179e77d13efde84ee96abf30a124f3a86825`  
		Last Modified: Tue, 14 Jan 2025 09:02:46 GMT  
		Size: 12.2 KB (12244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9d49e53e707da3ed5d73b62a4fe374bad1d91274ce451a98133353442723fb9`  
		Last Modified: Tue, 14 Jan 2025 09:02:47 GMT  
		Size: 11.9 KB (11903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:639c7cd00071a0b62766d53b22370535830272a699de91971e54d828c113c6c2`  
		Last Modified: Tue, 14 Jan 2025 09:02:47 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10.5` - unknown; unknown

```console
$ docker pull chronograf@sha256:cb2388b11815c41e02b9ed158ee6d627b8e7e9ba4baae043731552a2ce9f769e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2722366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a07c2b25ff90a5be47dfbfe81063611749d333225960cec7a16874dd2006fd37`

```dockerfile
```

-	Layers:
	-	`sha256:e00d8906b7526bc8bca4dbd34a2d75af98b178ba57c9dc6badeb508556ff8f5f`  
		Last Modified: Tue, 14 Jan 2025 09:02:47 GMT  
		Size: 2.7 MB (2706158 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:309aae5baec8f6e76452e0ee1b5f805d2e41571eee241086ef065f31862b2e51`  
		Last Modified: Tue, 14 Jan 2025 09:02:46 GMT  
		Size: 16.2 KB (16208 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.10.5` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:e9d2adcbf05b367178d80afae5a4be65bd9d108b97ccd30e3a2e9b762fea0d4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.7 MB (80688086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04eb7b75c8d8d64b5e28916f2541f39346c1027d02cdf4fa472b6650baad04af`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
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
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe5e22ffc62c19f88c63e73d68f6271af6579883314b212065a1f3f823822404`  
		Last Modified: Tue, 14 Jan 2025 07:03:13 GMT  
		Size: 7.7 MB (7652088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9be9572b2df6cf01e21eceea0c61e00397c4baf86724385e960030ed5c53b598`  
		Last Modified: Tue, 14 Jan 2025 07:03:14 GMT  
		Size: 45.0 MB (44970507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d41d08252d2d81e968b86f218af88b55a264ed843cf51c41ee846cada501a2a`  
		Last Modified: Tue, 14 Jan 2025 07:03:12 GMT  
		Size: 12.2 KB (12243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee5d82b281a9621c48cced8f12640673ffafe06d54a29b7fd724247b1f8f95bc`  
		Last Modified: Tue, 14 Jan 2025 07:03:12 GMT  
		Size: 11.9 KB (11902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f9a4caa4163798a2515cd4a99fff2a3633d45f79045264085c0e6df6fee2b2a`  
		Last Modified: Tue, 14 Jan 2025 07:03:13 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10.5` - unknown; unknown

```console
$ docker pull chronograf@sha256:125aa83ae8a8ff760a9654a30dfecdaea5cd9c8c4dab202c68a7e84528a142f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2720369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:829ced801ce3aa5bbc969ab7e89d23f24cf6ebf385b222e94b27c2c48913a446`

```dockerfile
```

-	Layers:
	-	`sha256:8110c7aede011c065bc590dfb8d4c5f389270f45ffc4f9103cb3a9de4099299f`  
		Last Modified: Tue, 14 Jan 2025 07:03:13 GMT  
		Size: 2.7 MB (2704134 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2d534b8b0f8a046a6dcbd52c6eab0e8a1e013b983679b8f41cc875a2b9aa1ca`  
		Last Modified: Tue, 14 Jan 2025 07:03:12 GMT  
		Size: 16.2 KB (16235 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.10.5-alpine`

```console
$ docker pull chronograf@sha256:fd22e60efc394d9cf49addff75db9896bdaa59a92831d5a649f57600241b5aef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.10.5-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:565eafbccd78da51863ddc5af1c325bd0755703b61e5058bf3f7bb8744fbfbd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31814451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99b96aa2eecd223e38af88a65ce94b8a24ce929843e8288f199df8966577e3c8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
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
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Wed, 08 Jan 2025 15:55:45 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f10033a10c25d8a78cc5c79537d8be6f9f9570d55e41149047e0eb842ff20ff7`  
		Last Modified: Wed, 08 Jan 2025 18:14:08 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e8e1ed9e8da33db6dd03408084a900ae90824d89fc2a9b14f453422b5119fe4`  
		Last Modified: Wed, 08 Jan 2025 18:14:08 GMT  
		Size: 296.5 KB (296485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13a1a285f7323a6ea298bbeb818f3c80ab849a601de7e3c5d4f18ed1737c58ab`  
		Last Modified: Wed, 08 Jan 2025 18:14:08 GMT  
		Size: 27.9 MB (27866995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0e09ce57cfd00606804f6da64b2f6d7ed8e7ebd061da4dd39492ae664d5f448`  
		Last Modified: Wed, 08 Jan 2025 18:14:08 GMT  
		Size: 12.2 KB (12240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d437e77355a9d05d3b5d3567741989e1cdf431b8932402e004f46d65d597880`  
		Last Modified: Wed, 08 Jan 2025 18:14:09 GMT  
		Size: 11.9 KB (11898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09cab2e3ba35d3a80672462930883bcc165643bc56c7a7cb85e2274f5f883bb6`  
		Last Modified: Wed, 08 Jan 2025 18:14:09 GMT  
		Size: 293.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10.5-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:4726a1af05f478eacb4e6ae7496295c8268530b94e341d465ce0254387d21986
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.4 KB (259450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4773308778b046fbf1cbd918492fb3e6940cbc43a637d34229c4a2bfddd28643`

```dockerfile
```

-	Layers:
	-	`sha256:dc9afdf2d7e83acbbcf82584839e1029a9fc056cda18c507457ad2f4c11ae85b`  
		Last Modified: Wed, 08 Jan 2025 18:14:08 GMT  
		Size: 241.6 KB (241595 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb03332e1a4f6d331e2c7201bd529d7e3b2c5caf81b355aa80d22f0c624368bc`  
		Last Modified: Wed, 08 Jan 2025 18:14:08 GMT  
		Size: 17.9 KB (17855 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.7`

```console
$ docker pull chronograf@sha256:831ca9d1fbdb3eb3f7f0a9b5340bfce329005de552d696490b73776b40e0c592
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
$ docker pull chronograf@sha256:a3cd9c7ec095a509b5882ccb2edc4a7c31a34c5d5a86c4e44d68ea3848d877ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.0 MB (69019814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d2f57a1cda3131c62fe92301692c9814090d45e59603a71ae755bd59decf8c6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1738540800'
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
	-	`sha256:cf799a8da63a7bb7f377162d10ed737dd26b0e1174c8ac5d89a5da6c15dc7c04`  
		Last Modified: Tue, 04 Feb 2025 01:36:33 GMT  
		Size: 30.3 MB (30252588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb263ef06a2ad02d3f6ec0e64168c7dd147acc12131f58bcc612ce8ffc37a584`  
		Last Modified: Tue, 04 Feb 2025 04:38:00 GMT  
		Size: 4.2 MB (4209316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f8fa92589557a03ca8c07cb0e70a0061930753a790debe8881b09ea6ba7220b`  
		Last Modified: Tue, 04 Feb 2025 04:38:01 GMT  
		Size: 34.5 MB (34533516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92670b143efcaba740f07a60fa7602bfb277922fb26a0f837e347cd1754c5ca9`  
		Last Modified: Tue, 04 Feb 2025 04:38:00 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b4a67c6a3f895b8b052297efe1278abbd6b5893ca8e26a828b6258f18010906`  
		Last Modified: Tue, 04 Feb 2025 04:38:00 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26eb2e74f58508725b7a2d5f8c468da3347f870ca1d9edd54aff6fcc66c6a276`  
		Last Modified: Tue, 04 Feb 2025 04:38:01 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7` - unknown; unknown

```console
$ docker pull chronograf@sha256:4e15286c16584dc43adb910d20878283f1940f09cbf5fc15a928ea92a44bea9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2921166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a25ce2891b4743546e1ffc360683d8af47ca7933b1503ff12d78edd5f57bc423`

```dockerfile
```

-	Layers:
	-	`sha256:33da33ebf81df7ffb723f3e9c5d3569408c5aea8fe28a05cabf0a88a2c52010a`  
		Last Modified: Tue, 04 Feb 2025 04:38:00 GMT  
		Size: 2.9 MB (2905389 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6fae89259dc63f5968589604a26bed1df35e9ac909a175eea7bbfe351ad9db4`  
		Last Modified: Tue, 04 Feb 2025 04:38:00 GMT  
		Size: 15.8 KB (15777 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.7` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:004a2fbda54f52b1d6d0c38960b7e8dc3001ad3c5d7b1eaaac5f03a5621140e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.0 MB (61962765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ad10f16605c1d4bab272ecb820b95b143342cd87701723620b60b28a1b05f80`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1736726400'
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
	-	`sha256:61fe776d618d9b70bea09742b3fce817da0393e8911c90f01094c0a407e1f7bf`  
		Last Modified: Tue, 14 Jan 2025 01:35:53 GMT  
		Size: 25.5 MB (25533960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f365359ad90862e89e688300b84de942f065f95a9c9727de5e58438eea6de464`  
		Last Modified: Tue, 14 Jan 2025 09:00:49 GMT  
		Size: 3.5 MB (3511668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9f6edd0e5b6e1dc040737282256b261b5377bf29fce185469d4e4bfefd960d8`  
		Last Modified: Tue, 14 Jan 2025 09:00:49 GMT  
		Size: 32.9 MB (32892737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38be5f90b1b89cbdabe84245ac488b720938ed34f9c00590569f1fd00ddd4d2b`  
		Last Modified: Tue, 14 Jan 2025 09:00:48 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca9a049fe64bf19950ae4c78754cea9ee7a0bab2083a063f48c5a7dbd3c67a9`  
		Last Modified: Tue, 14 Jan 2025 09:00:48 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38fdc3dbb24fbded15b8db67dd277f2396dd617c95137c73ea42e134e38ea945`  
		Last Modified: Tue, 14 Jan 2025 09:00:49 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7` - unknown; unknown

```console
$ docker pull chronograf@sha256:c3eb56662ad353291b7facd5826d7fc5913aeb4e511e3cafff00d2125d0858d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2923509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a95486aac116a285192d27989a01106b65a854ba3f3b14edf1d63ab101a182d`

```dockerfile
```

-	Layers:
	-	`sha256:b2fba389c2ab6b17ac08cb165373a0e580026241d80553df8b48012f35287735`  
		Last Modified: Tue, 14 Jan 2025 09:00:49 GMT  
		Size: 2.9 MB (2907660 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9c16fe4485464d301600fbc44b0bc02a8b80029314c89245f0f985a352f14fb`  
		Last Modified: Tue, 14 Jan 2025 09:00:48 GMT  
		Size: 15.8 KB (15849 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.7` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:ee59fa702c5cfa2c7534ed4d216b9689248b641cd2d7684515943b2a1e03c866
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.0 MB (66012916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5c5eef796c039aab28c5725b7c7d506df3313ad5cbbd3da2bf735388edc28bc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
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
	-	`sha256:6a43d3167ec1fb9f3b40bf3e095c86abebf31d406e2de1d196433c26d262f72c`  
		Last Modified: Tue, 14 Jan 2025 01:36:26 GMT  
		Size: 28.7 MB (28744913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71910223cf94a0958dc81672d8d75228b5b9103bc95056e1293ab56b03050371`  
		Last Modified: Tue, 14 Jan 2025 07:01:49 GMT  
		Size: 4.2 MB (4210584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ab63fb1b8c7181c5a7a9f046646566da9d4d3b9cb970ec55fb6a7f0f661021`  
		Last Modified: Tue, 14 Jan 2025 07:01:50 GMT  
		Size: 33.0 MB (33033033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ead04122d0495690e4b93ea0d1d176bf4b4508fde5eeb490cadb0ec3f394783a`  
		Last Modified: Tue, 14 Jan 2025 07:01:48 GMT  
		Size: 12.2 KB (12243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7875d404ea2e215fb6cb407757479653e2c23c6aefa916e541a9960e90a73b84`  
		Last Modified: Tue, 14 Jan 2025 07:01:49 GMT  
		Size: 11.9 KB (11903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f68a1b93c7c0ba999c7267401cae8fea0929fbcafe67193636849ac3c8f8f87c`  
		Last Modified: Tue, 14 Jan 2025 07:01:49 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7` - unknown; unknown

```console
$ docker pull chronograf@sha256:660ec9d45c13dcf98eb624583d6766f9595cdcf4b988e031950aeeedb997c78d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2921509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f656dbce6fcfed650477ee6eb3638e22c2673a9b75253e48f2234c3391df4243`

```dockerfile
```

-	Layers:
	-	`sha256:4aa8b24048a0684bfdcd3c07e3a0438b4367de1f37ce1596f62965b4b743a944`  
		Last Modified: Tue, 14 Jan 2025 07:01:49 GMT  
		Size: 2.9 MB (2905638 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c302e08138ec2e598f2b7b3795cf1188f6dc3c5aab4bb0c26497867a23196d7`  
		Last Modified: Tue, 14 Jan 2025 07:01:48 GMT  
		Size: 15.9 KB (15871 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.7-alpine`

```console
$ docker pull chronograf@sha256:b75b28c87f96e1593eb275e757314f7abc1e1f86e03701d2c9332288a3924182
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.7-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:b0a2afbdf1f19910326d0a7aefd58a4fdbfa3b2df5fe41efc947cc6b6c7a1890
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.5 MB (23502138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fa86ab7692e061e9f886b0ed724e19070a6a53698bc34faf9c5340203d77974`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
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
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Wed, 08 Jan 2025 15:55:45 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c0b5a4d116740f569200dfaa6b713cb6e11f6f0ea0fa825a0f417fa5016c8c5`  
		Last Modified: Wed, 08 Jan 2025 18:14:07 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2396a1df3d0abf45ff2f3f5655ac49784a9a20b2d57b78c8fd585ec89ee44e0`  
		Last Modified: Wed, 08 Jan 2025 18:14:06 GMT  
		Size: 294.4 KB (294373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0867a6d99c311b9420effcf959a7ad8f49fb809e0577906f3d8677b729af1644`  
		Last Modified: Wed, 08 Jan 2025 18:14:07 GMT  
		Size: 19.6 MB (19556854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88d94af1c0edb0c95d03c7d0263c2703162c5e89e8dc806be972f4fc5866eb86`  
		Last Modified: Wed, 08 Jan 2025 18:14:06 GMT  
		Size: 12.2 KB (12237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba6bdebf0f9cd138902797e37e2e6d212476212b5f4224b0bd4eed1ebf274f1c`  
		Last Modified: Wed, 08 Jan 2025 18:14:07 GMT  
		Size: 11.9 KB (11896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8223d9fc0d76920756582bc3c276147cb391caf4608f3db5ecc18c889a1a428f`  
		Last Modified: Wed, 08 Jan 2025 18:14:07 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:ad86551e289621949d2d7cbbaa62892c27c7d205696b89a016fbb0c52710cdd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.3 KB (189257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ad8e43d4841be5e5286d1718809e364b0ab104e3b171e80467f746e24343171`

```dockerfile
```

-	Layers:
	-	`sha256:0986b3cb6ec75e027fc68a187b931b199e83580e0815234bea45ce58255caf5b`  
		Last Modified: Wed, 08 Jan 2025 18:14:06 GMT  
		Size: 172.3 KB (172345 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1be1e5a8b15987a899415fff72ae7c22f2206670b440d48b40906adaa960035`  
		Last Modified: Wed, 08 Jan 2025 18:14:06 GMT  
		Size: 16.9 KB (16912 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.7.17`

```console
$ docker pull chronograf@sha256:831ca9d1fbdb3eb3f7f0a9b5340bfce329005de552d696490b73776b40e0c592
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
$ docker pull chronograf@sha256:a3cd9c7ec095a509b5882ccb2edc4a7c31a34c5d5a86c4e44d68ea3848d877ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.0 MB (69019814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d2f57a1cda3131c62fe92301692c9814090d45e59603a71ae755bd59decf8c6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1738540800'
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
	-	`sha256:cf799a8da63a7bb7f377162d10ed737dd26b0e1174c8ac5d89a5da6c15dc7c04`  
		Last Modified: Tue, 04 Feb 2025 01:36:33 GMT  
		Size: 30.3 MB (30252588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb263ef06a2ad02d3f6ec0e64168c7dd147acc12131f58bcc612ce8ffc37a584`  
		Last Modified: Tue, 04 Feb 2025 04:38:00 GMT  
		Size: 4.2 MB (4209316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f8fa92589557a03ca8c07cb0e70a0061930753a790debe8881b09ea6ba7220b`  
		Last Modified: Tue, 04 Feb 2025 04:38:01 GMT  
		Size: 34.5 MB (34533516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92670b143efcaba740f07a60fa7602bfb277922fb26a0f837e347cd1754c5ca9`  
		Last Modified: Tue, 04 Feb 2025 04:38:00 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b4a67c6a3f895b8b052297efe1278abbd6b5893ca8e26a828b6258f18010906`  
		Last Modified: Tue, 04 Feb 2025 04:38:00 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26eb2e74f58508725b7a2d5f8c468da3347f870ca1d9edd54aff6fcc66c6a276`  
		Last Modified: Tue, 04 Feb 2025 04:38:01 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7.17` - unknown; unknown

```console
$ docker pull chronograf@sha256:4e15286c16584dc43adb910d20878283f1940f09cbf5fc15a928ea92a44bea9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2921166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a25ce2891b4743546e1ffc360683d8af47ca7933b1503ff12d78edd5f57bc423`

```dockerfile
```

-	Layers:
	-	`sha256:33da33ebf81df7ffb723f3e9c5d3569408c5aea8fe28a05cabf0a88a2c52010a`  
		Last Modified: Tue, 04 Feb 2025 04:38:00 GMT  
		Size: 2.9 MB (2905389 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6fae89259dc63f5968589604a26bed1df35e9ac909a175eea7bbfe351ad9db4`  
		Last Modified: Tue, 04 Feb 2025 04:38:00 GMT  
		Size: 15.8 KB (15777 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.7.17` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:004a2fbda54f52b1d6d0c38960b7e8dc3001ad3c5d7b1eaaac5f03a5621140e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.0 MB (61962765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ad10f16605c1d4bab272ecb820b95b143342cd87701723620b60b28a1b05f80`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1736726400'
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
	-	`sha256:61fe776d618d9b70bea09742b3fce817da0393e8911c90f01094c0a407e1f7bf`  
		Last Modified: Tue, 14 Jan 2025 01:35:53 GMT  
		Size: 25.5 MB (25533960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f365359ad90862e89e688300b84de942f065f95a9c9727de5e58438eea6de464`  
		Last Modified: Tue, 14 Jan 2025 09:00:49 GMT  
		Size: 3.5 MB (3511668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9f6edd0e5b6e1dc040737282256b261b5377bf29fce185469d4e4bfefd960d8`  
		Last Modified: Tue, 14 Jan 2025 09:00:49 GMT  
		Size: 32.9 MB (32892737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38be5f90b1b89cbdabe84245ac488b720938ed34f9c00590569f1fd00ddd4d2b`  
		Last Modified: Tue, 14 Jan 2025 09:00:48 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca9a049fe64bf19950ae4c78754cea9ee7a0bab2083a063f48c5a7dbd3c67a9`  
		Last Modified: Tue, 14 Jan 2025 09:00:48 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38fdc3dbb24fbded15b8db67dd277f2396dd617c95137c73ea42e134e38ea945`  
		Last Modified: Tue, 14 Jan 2025 09:00:49 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7.17` - unknown; unknown

```console
$ docker pull chronograf@sha256:c3eb56662ad353291b7facd5826d7fc5913aeb4e511e3cafff00d2125d0858d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2923509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a95486aac116a285192d27989a01106b65a854ba3f3b14edf1d63ab101a182d`

```dockerfile
```

-	Layers:
	-	`sha256:b2fba389c2ab6b17ac08cb165373a0e580026241d80553df8b48012f35287735`  
		Last Modified: Tue, 14 Jan 2025 09:00:49 GMT  
		Size: 2.9 MB (2907660 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9c16fe4485464d301600fbc44b0bc02a8b80029314c89245f0f985a352f14fb`  
		Last Modified: Tue, 14 Jan 2025 09:00:48 GMT  
		Size: 15.8 KB (15849 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.7.17` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:ee59fa702c5cfa2c7534ed4d216b9689248b641cd2d7684515943b2a1e03c866
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.0 MB (66012916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5c5eef796c039aab28c5725b7c7d506df3313ad5cbbd3da2bf735388edc28bc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
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
	-	`sha256:6a43d3167ec1fb9f3b40bf3e095c86abebf31d406e2de1d196433c26d262f72c`  
		Last Modified: Tue, 14 Jan 2025 01:36:26 GMT  
		Size: 28.7 MB (28744913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71910223cf94a0958dc81672d8d75228b5b9103bc95056e1293ab56b03050371`  
		Last Modified: Tue, 14 Jan 2025 07:01:49 GMT  
		Size: 4.2 MB (4210584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ab63fb1b8c7181c5a7a9f046646566da9d4d3b9cb970ec55fb6a7f0f661021`  
		Last Modified: Tue, 14 Jan 2025 07:01:50 GMT  
		Size: 33.0 MB (33033033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ead04122d0495690e4b93ea0d1d176bf4b4508fde5eeb490cadb0ec3f394783a`  
		Last Modified: Tue, 14 Jan 2025 07:01:48 GMT  
		Size: 12.2 KB (12243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7875d404ea2e215fb6cb407757479653e2c23c6aefa916e541a9960e90a73b84`  
		Last Modified: Tue, 14 Jan 2025 07:01:49 GMT  
		Size: 11.9 KB (11903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f68a1b93c7c0ba999c7267401cae8fea0929fbcafe67193636849ac3c8f8f87c`  
		Last Modified: Tue, 14 Jan 2025 07:01:49 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7.17` - unknown; unknown

```console
$ docker pull chronograf@sha256:660ec9d45c13dcf98eb624583d6766f9595cdcf4b988e031950aeeedb997c78d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2921509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f656dbce6fcfed650477ee6eb3638e22c2673a9b75253e48f2234c3391df4243`

```dockerfile
```

-	Layers:
	-	`sha256:4aa8b24048a0684bfdcd3c07e3a0438b4367de1f37ce1596f62965b4b743a944`  
		Last Modified: Tue, 14 Jan 2025 07:01:49 GMT  
		Size: 2.9 MB (2905638 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c302e08138ec2e598f2b7b3795cf1188f6dc3c5aab4bb0c26497867a23196d7`  
		Last Modified: Tue, 14 Jan 2025 07:01:48 GMT  
		Size: 15.9 KB (15871 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.7.17-alpine`

```console
$ docker pull chronograf@sha256:b75b28c87f96e1593eb275e757314f7abc1e1f86e03701d2c9332288a3924182
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.7.17-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:b0a2afbdf1f19910326d0a7aefd58a4fdbfa3b2df5fe41efc947cc6b6c7a1890
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.5 MB (23502138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fa86ab7692e061e9f886b0ed724e19070a6a53698bc34faf9c5340203d77974`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
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
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Wed, 08 Jan 2025 15:55:45 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c0b5a4d116740f569200dfaa6b713cb6e11f6f0ea0fa825a0f417fa5016c8c5`  
		Last Modified: Wed, 08 Jan 2025 18:14:07 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2396a1df3d0abf45ff2f3f5655ac49784a9a20b2d57b78c8fd585ec89ee44e0`  
		Last Modified: Wed, 08 Jan 2025 18:14:06 GMT  
		Size: 294.4 KB (294373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0867a6d99c311b9420effcf959a7ad8f49fb809e0577906f3d8677b729af1644`  
		Last Modified: Wed, 08 Jan 2025 18:14:07 GMT  
		Size: 19.6 MB (19556854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88d94af1c0edb0c95d03c7d0263c2703162c5e89e8dc806be972f4fc5866eb86`  
		Last Modified: Wed, 08 Jan 2025 18:14:06 GMT  
		Size: 12.2 KB (12237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba6bdebf0f9cd138902797e37e2e6d212476212b5f4224b0bd4eed1ebf274f1c`  
		Last Modified: Wed, 08 Jan 2025 18:14:07 GMT  
		Size: 11.9 KB (11896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8223d9fc0d76920756582bc3c276147cb391caf4608f3db5ecc18c889a1a428f`  
		Last Modified: Wed, 08 Jan 2025 18:14:07 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7.17-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:ad86551e289621949d2d7cbbaa62892c27c7d205696b89a016fbb0c52710cdd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.3 KB (189257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ad8e43d4841be5e5286d1718809e364b0ab104e3b171e80467f746e24343171`

```dockerfile
```

-	Layers:
	-	`sha256:0986b3cb6ec75e027fc68a187b931b199e83580e0815234bea45ce58255caf5b`  
		Last Modified: Wed, 08 Jan 2025 18:14:06 GMT  
		Size: 172.3 KB (172345 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1be1e5a8b15987a899415fff72ae7c22f2206670b440d48b40906adaa960035`  
		Last Modified: Wed, 08 Jan 2025 18:14:06 GMT  
		Size: 16.9 KB (16912 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.8`

```console
$ docker pull chronograf@sha256:71fc005851dd123e338b5d02c641762e2c11aa2ffbf0439d4e43c8b5550eb245
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
$ docker pull chronograf@sha256:bdb986e247ccc34f37b74b941ac08bd2450561634fd53a1d1427652c01836474
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.7 MB (69661552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71cb7c3b22c1252eac3bc30090b25858223c511f26c61f708d135fdd8b3e9719`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1738540800'
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
	-	`sha256:cf799a8da63a7bb7f377162d10ed737dd26b0e1174c8ac5d89a5da6c15dc7c04`  
		Last Modified: Tue, 04 Feb 2025 01:36:33 GMT  
		Size: 30.3 MB (30252588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8785ff824f6e1b7678412f031f9055ff3e4bbf7f25aa72de7594a6a33737f4fe`  
		Last Modified: Tue, 04 Feb 2025 04:38:03 GMT  
		Size: 5.0 MB (5020283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:373a42f83f554158309aac5a9a98ac1352f9ca022a3da15c9d81f66e9f2a096d`  
		Last Modified: Tue, 04 Feb 2025 04:38:04 GMT  
		Size: 34.4 MB (34364288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bdef682ebcfea8b4357dd71a924a2a310035d2bbf9a72ff368b9c7b660e7dd1`  
		Last Modified: Tue, 04 Feb 2025 04:38:03 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d50a1cbdee3599e854104fc55725621537bb008e39b8ed1ac475a3bb5397318`  
		Last Modified: Tue, 04 Feb 2025 04:38:03 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0449aacb0fb5c930d32c107a75346b442adc974f54c08925b5f90ce4fb2bd99f`  
		Last Modified: Tue, 04 Feb 2025 04:38:04 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8` - unknown; unknown

```console
$ docker pull chronograf@sha256:0062ed2a8200e397d77eb4e56fe31c361ba9b8a26e2e7d636a614102a3403790
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2977894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33c53719e06ca07cf66ea3b6871bf82d33cb1b38c249b4540faed9eb4773c214`

```dockerfile
```

-	Layers:
	-	`sha256:2f93bcb3acbe728c4ade24c71912e1184bc60cd8a724b912241422152c039c29`  
		Last Modified: Tue, 04 Feb 2025 04:38:03 GMT  
		Size: 3.0 MB (2962077 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e20530eabe6bfd8d59f5ecbc8a2e1911eb630d445bde4b77aebcc390ec8cde01`  
		Last Modified: Tue, 04 Feb 2025 04:38:03 GMT  
		Size: 15.8 KB (15817 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.8` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:de4dc20d59ef64a1eb27732c129be7e21d8b81416d91302a5115747634b3585c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62378369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9189a0e26ffa3aeb3e494a904d083aae0d882637db8510bc75d904882dfb5bc4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1736726400'
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
	-	`sha256:61fe776d618d9b70bea09742b3fce817da0393e8911c90f01094c0a407e1f7bf`  
		Last Modified: Tue, 14 Jan 2025 01:35:53 GMT  
		Size: 25.5 MB (25533960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a2ed3ddb3c1f0b1884a7cece78f6049e74ba3217ff2acd73b2add14110f846c`  
		Last Modified: Tue, 14 Jan 2025 09:01:27 GMT  
		Size: 4.3 MB (4285210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81d4ead48b02c209e8cd6a0b5cf60f06ec6d7e20db1aabe18e8900a6df6e6d65`  
		Last Modified: Tue, 14 Jan 2025 09:01:28 GMT  
		Size: 32.5 MB (32534809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6154af5df3e1b24b2fa93631ac976a57e8f77e674d0bcb33f21ea2fd4e4f862`  
		Last Modified: Tue, 14 Jan 2025 09:01:27 GMT  
		Size: 12.2 KB (12244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e75c7d960acf4ca8fa450e3475caf6f5a68ec21332ac7ad827f44f2759dbb0f`  
		Last Modified: Tue, 14 Jan 2025 09:01:27 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:118d03671505a31a39eefcca335ad7322370152a5addcd6344021cd81b16fbd8`  
		Last Modified: Tue, 14 Jan 2025 09:01:28 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8` - unknown; unknown

```console
$ docker pull chronograf@sha256:fe71ca7ef148119b902cb7fecc66b31cfc20cf327ab7f8a23d83cf8cad8b05c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2980238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89b73f50aeb55e8e77254e22220344b81af957916c3fa7ba18af04b3bccc6255`

```dockerfile
```

-	Layers:
	-	`sha256:abce3aa2f2375a79866e380116881930e72f680a6f0d4aa1a8251280de7ceda8`  
		Last Modified: Tue, 14 Jan 2025 09:01:27 GMT  
		Size: 3.0 MB (2964348 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa8311a776e980e4ad5439abee8b022dab9b4286ef3847b465224acf3550f275`  
		Last Modified: Tue, 14 Jan 2025 09:01:26 GMT  
		Size: 15.9 KB (15890 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.8` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:d30dae3a6ea010c0c663bc8e4c27b6a7f4a8947214da8d1b1ee35cb2d91c12f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66202351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c98e16205c831a42ece64c78274e4222f983148fa7409ee1caf453f12af22ff2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
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
	-	`sha256:6a43d3167ec1fb9f3b40bf3e095c86abebf31d406e2de1d196433c26d262f72c`  
		Last Modified: Tue, 14 Jan 2025 01:36:26 GMT  
		Size: 28.7 MB (28744913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98bab0c59c329bc0372b1d829f355da3eaee9c050510954a5286c1efeb1186da`  
		Last Modified: Tue, 14 Jan 2025 07:02:17 GMT  
		Size: 5.0 MB (5003559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36f0847a8d37592a58316ae4ae7184cd1f403c58afdfbc064d7d64bbb25dde3b`  
		Last Modified: Tue, 14 Jan 2025 07:02:18 GMT  
		Size: 32.4 MB (32429499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c9225f4ecf85fc2fe09c1f48fbf4c530a6936f0ff16fd742a6a615979a9f8b8`  
		Last Modified: Tue, 14 Jan 2025 07:02:17 GMT  
		Size: 12.2 KB (12241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62ba5b553216c2896378b4039fa3d5ee34a5ebc0691492ca49325ffbcc4dc9b3`  
		Last Modified: Tue, 14 Jan 2025 07:02:17 GMT  
		Size: 11.9 KB (11900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67801e65c5784c93306d0fdb35963cd146646a076795464dbbaaac78ea271bf4`  
		Last Modified: Tue, 14 Jan 2025 07:02:18 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8` - unknown; unknown

```console
$ docker pull chronograf@sha256:82a3d78d003d247b634e90474c80a8e8ee1ba8152023d79060092e5989e2f8cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2978238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dcadf548093dee411cf06f3c0d1a1a0a99a8bfb1660603da0aece27c6dbe657`

```dockerfile
```

-	Layers:
	-	`sha256:b720886352871cc2c609b83945d14e799b2db2e13096111f6ef2b2d4d33b9bef`  
		Last Modified: Tue, 14 Jan 2025 07:02:17 GMT  
		Size: 3.0 MB (2962326 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a1b9edec45357e8bb65cee9f08a1bf3a93eb2acd3f2a67852103dd1137143fd`  
		Last Modified: Tue, 14 Jan 2025 07:02:17 GMT  
		Size: 15.9 KB (15912 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.8-alpine`

```console
$ docker pull chronograf@sha256:3ec4746da3741d35b524083913c90b84d448ee55b9040b786529dcb028c6cdae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.8-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:b92b8b585c45a8775aaee079e1e28a554b91fe80988cfb648512a1e543180584
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23149454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42049fd4a422ef0b324355ed7d6127cda752784d8f978376b34a62e5333d9a13`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
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
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Wed, 08 Jan 2025 15:55:45 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0da3701f1f38fbed6411e6831a577633f241583001568dd25614d2516577b46`  
		Last Modified: Wed, 08 Jan 2025 18:13:49 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2a60f718936d296a403b15f7eb11eba63dea53c8708a4abf6e2140561b5e598`  
		Last Modified: Wed, 08 Jan 2025 18:13:49 GMT  
		Size: 294.4 KB (294381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da09e2832f81132824d91e3a9ffa966b69be05ca1701102618cd9976b00b5fff`  
		Last Modified: Wed, 08 Jan 2025 18:13:50 GMT  
		Size: 19.2 MB (19204164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e0dc3488ee2815c6e6b63eacd2d6855acb3ecf5d11b84e07165b78913c9412d`  
		Last Modified: Wed, 08 Jan 2025 18:13:49 GMT  
		Size: 12.2 KB (12236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a6d628b63cb6f9cf00d6473138c6204490e85e808c569e472aba11d073dbc94`  
		Last Modified: Wed, 08 Jan 2025 18:13:50 GMT  
		Size: 11.9 KB (11895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdd98d98774052a90e24a5df70c8a6101d9a3e80114c90468cb5d9b44ec07f93`  
		Last Modified: Wed, 08 Jan 2025 18:13:50 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:e4444e5f8b500556bfae0023e0bba6368338799319174e53d9239ce86cd62fd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.8 KB (246816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ecd9cfd9312defad16174512c5ca52a7c496b042a85b19e3451a8588b2623f5`

```dockerfile
```

-	Layers:
	-	`sha256:f7859a1c5aeec0c8a9fae906987db654fb25960e8e9f265dd215149f994e7da3`  
		Last Modified: Wed, 08 Jan 2025 18:13:49 GMT  
		Size: 229.9 KB (229904 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b31c3d0cc28e20966cf8b4acef0696aaf0993c9b01a36492c7ea8be7109d42b4`  
		Last Modified: Wed, 08 Jan 2025 18:13:49 GMT  
		Size: 16.9 KB (16912 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.8.10`

```console
$ docker pull chronograf@sha256:71fc005851dd123e338b5d02c641762e2c11aa2ffbf0439d4e43c8b5550eb245
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
$ docker pull chronograf@sha256:bdb986e247ccc34f37b74b941ac08bd2450561634fd53a1d1427652c01836474
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.7 MB (69661552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71cb7c3b22c1252eac3bc30090b25858223c511f26c61f708d135fdd8b3e9719`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1738540800'
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
	-	`sha256:cf799a8da63a7bb7f377162d10ed737dd26b0e1174c8ac5d89a5da6c15dc7c04`  
		Last Modified: Tue, 04 Feb 2025 01:36:33 GMT  
		Size: 30.3 MB (30252588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8785ff824f6e1b7678412f031f9055ff3e4bbf7f25aa72de7594a6a33737f4fe`  
		Last Modified: Tue, 04 Feb 2025 04:38:03 GMT  
		Size: 5.0 MB (5020283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:373a42f83f554158309aac5a9a98ac1352f9ca022a3da15c9d81f66e9f2a096d`  
		Last Modified: Tue, 04 Feb 2025 04:38:04 GMT  
		Size: 34.4 MB (34364288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bdef682ebcfea8b4357dd71a924a2a310035d2bbf9a72ff368b9c7b660e7dd1`  
		Last Modified: Tue, 04 Feb 2025 04:38:03 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d50a1cbdee3599e854104fc55725621537bb008e39b8ed1ac475a3bb5397318`  
		Last Modified: Tue, 04 Feb 2025 04:38:03 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0449aacb0fb5c930d32c107a75346b442adc974f54c08925b5f90ce4fb2bd99f`  
		Last Modified: Tue, 04 Feb 2025 04:38:04 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:0062ed2a8200e397d77eb4e56fe31c361ba9b8a26e2e7d636a614102a3403790
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2977894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33c53719e06ca07cf66ea3b6871bf82d33cb1b38c249b4540faed9eb4773c214`

```dockerfile
```

-	Layers:
	-	`sha256:2f93bcb3acbe728c4ade24c71912e1184bc60cd8a724b912241422152c039c29`  
		Last Modified: Tue, 04 Feb 2025 04:38:03 GMT  
		Size: 3.0 MB (2962077 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e20530eabe6bfd8d59f5ecbc8a2e1911eb630d445bde4b77aebcc390ec8cde01`  
		Last Modified: Tue, 04 Feb 2025 04:38:03 GMT  
		Size: 15.8 KB (15817 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.8.10` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:de4dc20d59ef64a1eb27732c129be7e21d8b81416d91302a5115747634b3585c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62378369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9189a0e26ffa3aeb3e494a904d083aae0d882637db8510bc75d904882dfb5bc4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1736726400'
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
	-	`sha256:61fe776d618d9b70bea09742b3fce817da0393e8911c90f01094c0a407e1f7bf`  
		Last Modified: Tue, 14 Jan 2025 01:35:53 GMT  
		Size: 25.5 MB (25533960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a2ed3ddb3c1f0b1884a7cece78f6049e74ba3217ff2acd73b2add14110f846c`  
		Last Modified: Tue, 14 Jan 2025 09:01:27 GMT  
		Size: 4.3 MB (4285210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81d4ead48b02c209e8cd6a0b5cf60f06ec6d7e20db1aabe18e8900a6df6e6d65`  
		Last Modified: Tue, 14 Jan 2025 09:01:28 GMT  
		Size: 32.5 MB (32534809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6154af5df3e1b24b2fa93631ac976a57e8f77e674d0bcb33f21ea2fd4e4f862`  
		Last Modified: Tue, 14 Jan 2025 09:01:27 GMT  
		Size: 12.2 KB (12244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e75c7d960acf4ca8fa450e3475caf6f5a68ec21332ac7ad827f44f2759dbb0f`  
		Last Modified: Tue, 14 Jan 2025 09:01:27 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:118d03671505a31a39eefcca335ad7322370152a5addcd6344021cd81b16fbd8`  
		Last Modified: Tue, 14 Jan 2025 09:01:28 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:fe71ca7ef148119b902cb7fecc66b31cfc20cf327ab7f8a23d83cf8cad8b05c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2980238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89b73f50aeb55e8e77254e22220344b81af957916c3fa7ba18af04b3bccc6255`

```dockerfile
```

-	Layers:
	-	`sha256:abce3aa2f2375a79866e380116881930e72f680a6f0d4aa1a8251280de7ceda8`  
		Last Modified: Tue, 14 Jan 2025 09:01:27 GMT  
		Size: 3.0 MB (2964348 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa8311a776e980e4ad5439abee8b022dab9b4286ef3847b465224acf3550f275`  
		Last Modified: Tue, 14 Jan 2025 09:01:26 GMT  
		Size: 15.9 KB (15890 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.8.10` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:d30dae3a6ea010c0c663bc8e4c27b6a7f4a8947214da8d1b1ee35cb2d91c12f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66202351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c98e16205c831a42ece64c78274e4222f983148fa7409ee1caf453f12af22ff2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
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
	-	`sha256:6a43d3167ec1fb9f3b40bf3e095c86abebf31d406e2de1d196433c26d262f72c`  
		Last Modified: Tue, 14 Jan 2025 01:36:26 GMT  
		Size: 28.7 MB (28744913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98bab0c59c329bc0372b1d829f355da3eaee9c050510954a5286c1efeb1186da`  
		Last Modified: Tue, 14 Jan 2025 07:02:17 GMT  
		Size: 5.0 MB (5003559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36f0847a8d37592a58316ae4ae7184cd1f403c58afdfbc064d7d64bbb25dde3b`  
		Last Modified: Tue, 14 Jan 2025 07:02:18 GMT  
		Size: 32.4 MB (32429499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c9225f4ecf85fc2fe09c1f48fbf4c530a6936f0ff16fd742a6a615979a9f8b8`  
		Last Modified: Tue, 14 Jan 2025 07:02:17 GMT  
		Size: 12.2 KB (12241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62ba5b553216c2896378b4039fa3d5ee34a5ebc0691492ca49325ffbcc4dc9b3`  
		Last Modified: Tue, 14 Jan 2025 07:02:17 GMT  
		Size: 11.9 KB (11900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67801e65c5784c93306d0fdb35963cd146646a076795464dbbaaac78ea271bf4`  
		Last Modified: Tue, 14 Jan 2025 07:02:18 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:82a3d78d003d247b634e90474c80a8e8ee1ba8152023d79060092e5989e2f8cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2978238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dcadf548093dee411cf06f3c0d1a1a0a99a8bfb1660603da0aece27c6dbe657`

```dockerfile
```

-	Layers:
	-	`sha256:b720886352871cc2c609b83945d14e799b2db2e13096111f6ef2b2d4d33b9bef`  
		Last Modified: Tue, 14 Jan 2025 07:02:17 GMT  
		Size: 3.0 MB (2962326 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a1b9edec45357e8bb65cee9f08a1bf3a93eb2acd3f2a67852103dd1137143fd`  
		Last Modified: Tue, 14 Jan 2025 07:02:17 GMT  
		Size: 15.9 KB (15912 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.8.10-alpine`

```console
$ docker pull chronograf@sha256:3ec4746da3741d35b524083913c90b84d448ee55b9040b786529dcb028c6cdae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.8.10-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:b92b8b585c45a8775aaee079e1e28a554b91fe80988cfb648512a1e543180584
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23149454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42049fd4a422ef0b324355ed7d6127cda752784d8f978376b34a62e5333d9a13`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
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
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Wed, 08 Jan 2025 15:55:45 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0da3701f1f38fbed6411e6831a577633f241583001568dd25614d2516577b46`  
		Last Modified: Wed, 08 Jan 2025 18:13:49 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2a60f718936d296a403b15f7eb11eba63dea53c8708a4abf6e2140561b5e598`  
		Last Modified: Wed, 08 Jan 2025 18:13:49 GMT  
		Size: 294.4 KB (294381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da09e2832f81132824d91e3a9ffa966b69be05ca1701102618cd9976b00b5fff`  
		Last Modified: Wed, 08 Jan 2025 18:13:50 GMT  
		Size: 19.2 MB (19204164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e0dc3488ee2815c6e6b63eacd2d6855acb3ecf5d11b84e07165b78913c9412d`  
		Last Modified: Wed, 08 Jan 2025 18:13:49 GMT  
		Size: 12.2 KB (12236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a6d628b63cb6f9cf00d6473138c6204490e85e808c569e472aba11d073dbc94`  
		Last Modified: Wed, 08 Jan 2025 18:13:50 GMT  
		Size: 11.9 KB (11895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdd98d98774052a90e24a5df70c8a6101d9a3e80114c90468cb5d9b44ec07f93`  
		Last Modified: Wed, 08 Jan 2025 18:13:50 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8.10-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:e4444e5f8b500556bfae0023e0bba6368338799319174e53d9239ce86cd62fd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.8 KB (246816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ecd9cfd9312defad16174512c5ca52a7c496b042a85b19e3451a8588b2623f5`

```dockerfile
```

-	Layers:
	-	`sha256:f7859a1c5aeec0c8a9fae906987db654fb25960e8e9f265dd215149f994e7da3`  
		Last Modified: Wed, 08 Jan 2025 18:13:49 GMT  
		Size: 229.9 KB (229904 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b31c3d0cc28e20966cf8b4acef0696aaf0993c9b01a36492c7ea8be7109d42b4`  
		Last Modified: Wed, 08 Jan 2025 18:13:49 GMT  
		Size: 16.9 KB (16912 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.9`

```console
$ docker pull chronograf@sha256:b5d9ec4df2b016b87575ebd911264afab969a2be1f605cb3360bf1d30eccb31b
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
$ docker pull chronograf@sha256:223803850cb1cfcfeffabd1c1c631c968190b8e955ce6d7ee866185fd50bff73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.3 MB (70308934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd64ee77cbb1bc144c600492445224a5cb8e29a88148f740724a51aaa763d51c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1738540800'
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
	-	`sha256:cf799a8da63a7bb7f377162d10ed737dd26b0e1174c8ac5d89a5da6c15dc7c04`  
		Last Modified: Tue, 04 Feb 2025 01:36:33 GMT  
		Size: 30.3 MB (30252588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc5eabc3fe7f89b0d4eb1cd1e4d2e7648e22783d0596e1e978cb57608097fdab`  
		Last Modified: Tue, 04 Feb 2025 04:38:15 GMT  
		Size: 5.0 MB (5020252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8de194c1335598dfa6e88894ea5c0a7b5e1b72ff3f3f3e57c0b2ee67b51bbff1`  
		Last Modified: Tue, 04 Feb 2025 04:38:17 GMT  
		Size: 35.0 MB (35011707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f87146d5ed2a2f92aa78269a9caa021f0066e7b5ce925c7089ac5a8a20b98456`  
		Last Modified: Tue, 04 Feb 2025 04:38:14 GMT  
		Size: 12.2 KB (12244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8621df80608c9e6c678eaa26ecc34c60c6e3ab3c7659c786d4f1d20dd37e5bb8`  
		Last Modified: Tue, 04 Feb 2025 04:38:14 GMT  
		Size: 11.9 KB (11903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9a5b589f142c726a2058c563cfd3c03334466ee844138e9a90892f59f9c0223`  
		Last Modified: Tue, 04 Feb 2025 04:38:15 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9` - unknown; unknown

```console
$ docker pull chronograf@sha256:fac6d1b5c520a6bfdb8a487aafdc898445f5e7e1a3761dcc80ab2eaceacee326
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2983096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e12f73720f1e21f06089cb09a011c62e27a1018f61777b527c6b7a298ae6eebc`

```dockerfile
```

-	Layers:
	-	`sha256:5312d19b10749a54349be0602e9d8c846703aad5a6b5f3f5a3178f6d577c9884`  
		Last Modified: Tue, 04 Feb 2025 04:38:14 GMT  
		Size: 3.0 MB (2967287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9fde1a3c7336984c8290284b99d507256b242601be430049b78521ae66457546`  
		Last Modified: Tue, 04 Feb 2025 04:38:14 GMT  
		Size: 15.8 KB (15809 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.9` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:a606a022ee67879c07933e8ec12d581faf88b89660d2d280e249ab1a2cd26fe6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.2 MB (63155098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ef023b85bbf539ecc7e48d24aea99f57d223e0b6de7ffd9502b6de52c17cca1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1736726400'
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
	-	`sha256:61fe776d618d9b70bea09742b3fce817da0393e8911c90f01094c0a407e1f7bf`  
		Last Modified: Tue, 14 Jan 2025 01:35:53 GMT  
		Size: 25.5 MB (25533960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a2ed3ddb3c1f0b1884a7cece78f6049e74ba3217ff2acd73b2add14110f846c`  
		Last Modified: Tue, 14 Jan 2025 09:01:27 GMT  
		Size: 4.3 MB (4285210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1f92a0944b157664d92d4f13935ea45caca74a2ff90e719ffc250181ce9d3b3`  
		Last Modified: Tue, 14 Jan 2025 09:01:59 GMT  
		Size: 33.3 MB (33311528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1233775ae68068b33e27bd86695bd9425260d17a867baa1b33ca47652f86a805`  
		Last Modified: Tue, 14 Jan 2025 09:01:57 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fe59fcac9868e1850989c4e75c954050432bc447500e0cdc55b8fa05d3fbae7`  
		Last Modified: Tue, 14 Jan 2025 09:01:57 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b30a5382637c60559dc83b0dd3f92dcbfd2da8fe8c05d8f2db091f016d96957`  
		Last Modified: Tue, 14 Jan 2025 09:01:58 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9` - unknown; unknown

```console
$ docker pull chronograf@sha256:7f8e2a1a5844e81c2bb1ab8ea9deccb335677976adea838826568fee10d04b34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2985441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecdc24386a0070af20cdad9063e88bd48b51d7fb31104ba6d63f115b97ede887`

```dockerfile
```

-	Layers:
	-	`sha256:b8c0cc9f2066f758a9065045366d300a31e65227be0723c886142978b7209c45`  
		Last Modified: Tue, 14 Jan 2025 09:01:58 GMT  
		Size: 3.0 MB (2969558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:601c03e901565cdf8cb022c4b60429c1c2aafd2ed0f4ec1b466078e0bab2ebc4`  
		Last Modified: Tue, 14 Jan 2025 09:01:57 GMT  
		Size: 15.9 KB (15883 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.9` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:276c44ece1f8db00ec8a3b8bf6499d52f2d2e4367f2334df49109f8a9a196bf6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.0 MB (66954431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:337b6d6f82a720d266a1c06f3bf320442b79f52322498d2dc49f24eeeda2f44a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
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
	-	`sha256:6a43d3167ec1fb9f3b40bf3e095c86abebf31d406e2de1d196433c26d262f72c`  
		Last Modified: Tue, 14 Jan 2025 01:36:26 GMT  
		Size: 28.7 MB (28744913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98bab0c59c329bc0372b1d829f355da3eaee9c050510954a5286c1efeb1186da`  
		Last Modified: Tue, 14 Jan 2025 07:02:17 GMT  
		Size: 5.0 MB (5003559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa83362d5761bbccb4c2e343d52ea7f888268b7c881eb988eec8420da94771c3`  
		Last Modified: Tue, 14 Jan 2025 07:02:41 GMT  
		Size: 33.2 MB (33181578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50faa8d2d1e297aecf04fa3cb862907be2c7c1fc44948018a284f9b17a8c8c63`  
		Last Modified: Tue, 14 Jan 2025 07:02:40 GMT  
		Size: 12.2 KB (12241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b8fd9d7d5d2c0ec9d3f7c6e0792d5a3bda1aa536b2416ee22961d85aec1da64`  
		Last Modified: Tue, 14 Jan 2025 07:02:40 GMT  
		Size: 11.9 KB (11901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6725fc396b26df3bd7ff1d414d1445cff57f25b8b1d26752d3669cc73e94b4c`  
		Last Modified: Tue, 14 Jan 2025 07:02:41 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9` - unknown; unknown

```console
$ docker pull chronograf@sha256:5bb2088d9da76b89e35fd6fe273aad228967a72fc8fcd77ecf926bde376d25fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2983441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbb66c8a4581c229fb9926b7d1531277172fa892bd09a835f3793ae99268834f`

```dockerfile
```

-	Layers:
	-	`sha256:0ff0ceb0982281118b2acc98525b908e189ed5ef9e98538fbed29152bf888ea9`  
		Last Modified: Tue, 14 Jan 2025 07:02:41 GMT  
		Size: 3.0 MB (2967536 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c86b291c4e0866169d05caebeee7a06ed9f6c50587c0294fe079b15d78ef35b`  
		Last Modified: Tue, 14 Jan 2025 07:02:40 GMT  
		Size: 15.9 KB (15905 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.9-alpine`

```console
$ docker pull chronograf@sha256:aa92223a25f515409f9f656182c5f7206421bf02e3d391e9c01770165ed09c9f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.9-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:6ecccec248bcce1ecf0dcfe43ab23068a93c13af96a752ebcfa602ba570ced5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23617292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b00653f032a0cd642084ec3e94f34a4a2e23b07f23f9be35986ab3647a12568d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
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
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Wed, 08 Jan 2025 15:55:45 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afe7fcb9c117622d9b76b0cebecdb2fe8ff1ff52419a133b7429370ec4bf75b0`  
		Last Modified: Wed, 08 Jan 2025 18:14:06 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:666a211b7d8fbd8876fab29f7120cf3c11a68a0f59279c107badb4e1bdb714ad`  
		Last Modified: Wed, 08 Jan 2025 18:14:06 GMT  
		Size: 294.4 KB (294367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9793be8b948ef211ee8c44e8c33b425011056710ba6a23fca9861b4ec99b4da9`  
		Last Modified: Wed, 08 Jan 2025 18:14:06 GMT  
		Size: 19.7 MB (19672018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b98c71573af081597d12ca72b1f672d9abfc0bfabc90bdb53d5b278f13b4b5e9`  
		Last Modified: Wed, 08 Jan 2025 18:14:06 GMT  
		Size: 12.2 KB (12236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4296437122a9507fc662bf7e0ce0648a735459f910dc992723c1fa572502ff9a`  
		Last Modified: Wed, 08 Jan 2025 18:14:07 GMT  
		Size: 11.9 KB (11893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7e8c86465fb666432b74fe5f04c22d9d26d182546a744afa302339288a386e1`  
		Last Modified: Wed, 08 Jan 2025 18:14:07 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:992ed9f4af10a3c98123ffe07804827ccdad6aeca3b9cbfef8b1733fdf0168c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.0 KB (252025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22cebb48a8a7336c3d4e1c7e5afdc35734f8fc776e4efd4ab80f9ea3c7122f80`

```dockerfile
```

-	Layers:
	-	`sha256:436e27fdbcf1a58d037af89205400a63468caeabdb8c0708212cc4702db0a3c2`  
		Last Modified: Wed, 08 Jan 2025 18:14:06 GMT  
		Size: 235.1 KB (235116 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b1e8475858167e931497026c48659bbb3c1085dad44cca1ae254f70b77705dd`  
		Last Modified: Wed, 08 Jan 2025 18:14:06 GMT  
		Size: 16.9 KB (16909 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.9.4`

```console
$ docker pull chronograf@sha256:b5d9ec4df2b016b87575ebd911264afab969a2be1f605cb3360bf1d30eccb31b
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
$ docker pull chronograf@sha256:223803850cb1cfcfeffabd1c1c631c968190b8e955ce6d7ee866185fd50bff73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.3 MB (70308934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd64ee77cbb1bc144c600492445224a5cb8e29a88148f740724a51aaa763d51c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1738540800'
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
	-	`sha256:cf799a8da63a7bb7f377162d10ed737dd26b0e1174c8ac5d89a5da6c15dc7c04`  
		Last Modified: Tue, 04 Feb 2025 01:36:33 GMT  
		Size: 30.3 MB (30252588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc5eabc3fe7f89b0d4eb1cd1e4d2e7648e22783d0596e1e978cb57608097fdab`  
		Last Modified: Tue, 04 Feb 2025 04:38:15 GMT  
		Size: 5.0 MB (5020252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8de194c1335598dfa6e88894ea5c0a7b5e1b72ff3f3f3e57c0b2ee67b51bbff1`  
		Last Modified: Tue, 04 Feb 2025 04:38:17 GMT  
		Size: 35.0 MB (35011707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f87146d5ed2a2f92aa78269a9caa021f0066e7b5ce925c7089ac5a8a20b98456`  
		Last Modified: Tue, 04 Feb 2025 04:38:14 GMT  
		Size: 12.2 KB (12244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8621df80608c9e6c678eaa26ecc34c60c6e3ab3c7659c786d4f1d20dd37e5bb8`  
		Last Modified: Tue, 04 Feb 2025 04:38:14 GMT  
		Size: 11.9 KB (11903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9a5b589f142c726a2058c563cfd3c03334466ee844138e9a90892f59f9c0223`  
		Last Modified: Tue, 04 Feb 2025 04:38:15 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9.4` - unknown; unknown

```console
$ docker pull chronograf@sha256:fac6d1b5c520a6bfdb8a487aafdc898445f5e7e1a3761dcc80ab2eaceacee326
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2983096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e12f73720f1e21f06089cb09a011c62e27a1018f61777b527c6b7a298ae6eebc`

```dockerfile
```

-	Layers:
	-	`sha256:5312d19b10749a54349be0602e9d8c846703aad5a6b5f3f5a3178f6d577c9884`  
		Last Modified: Tue, 04 Feb 2025 04:38:14 GMT  
		Size: 3.0 MB (2967287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9fde1a3c7336984c8290284b99d507256b242601be430049b78521ae66457546`  
		Last Modified: Tue, 04 Feb 2025 04:38:14 GMT  
		Size: 15.8 KB (15809 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.9.4` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:a606a022ee67879c07933e8ec12d581faf88b89660d2d280e249ab1a2cd26fe6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.2 MB (63155098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ef023b85bbf539ecc7e48d24aea99f57d223e0b6de7ffd9502b6de52c17cca1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1736726400'
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
	-	`sha256:61fe776d618d9b70bea09742b3fce817da0393e8911c90f01094c0a407e1f7bf`  
		Last Modified: Tue, 14 Jan 2025 01:35:53 GMT  
		Size: 25.5 MB (25533960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a2ed3ddb3c1f0b1884a7cece78f6049e74ba3217ff2acd73b2add14110f846c`  
		Last Modified: Tue, 14 Jan 2025 09:01:27 GMT  
		Size: 4.3 MB (4285210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1f92a0944b157664d92d4f13935ea45caca74a2ff90e719ffc250181ce9d3b3`  
		Last Modified: Tue, 14 Jan 2025 09:01:59 GMT  
		Size: 33.3 MB (33311528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1233775ae68068b33e27bd86695bd9425260d17a867baa1b33ca47652f86a805`  
		Last Modified: Tue, 14 Jan 2025 09:01:57 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fe59fcac9868e1850989c4e75c954050432bc447500e0cdc55b8fa05d3fbae7`  
		Last Modified: Tue, 14 Jan 2025 09:01:57 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b30a5382637c60559dc83b0dd3f92dcbfd2da8fe8c05d8f2db091f016d96957`  
		Last Modified: Tue, 14 Jan 2025 09:01:58 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9.4` - unknown; unknown

```console
$ docker pull chronograf@sha256:7f8e2a1a5844e81c2bb1ab8ea9deccb335677976adea838826568fee10d04b34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2985441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecdc24386a0070af20cdad9063e88bd48b51d7fb31104ba6d63f115b97ede887`

```dockerfile
```

-	Layers:
	-	`sha256:b8c0cc9f2066f758a9065045366d300a31e65227be0723c886142978b7209c45`  
		Last Modified: Tue, 14 Jan 2025 09:01:58 GMT  
		Size: 3.0 MB (2969558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:601c03e901565cdf8cb022c4b60429c1c2aafd2ed0f4ec1b466078e0bab2ebc4`  
		Last Modified: Tue, 14 Jan 2025 09:01:57 GMT  
		Size: 15.9 KB (15883 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.9.4` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:276c44ece1f8db00ec8a3b8bf6499d52f2d2e4367f2334df49109f8a9a196bf6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.0 MB (66954431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:337b6d6f82a720d266a1c06f3bf320442b79f52322498d2dc49f24eeeda2f44a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
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
	-	`sha256:6a43d3167ec1fb9f3b40bf3e095c86abebf31d406e2de1d196433c26d262f72c`  
		Last Modified: Tue, 14 Jan 2025 01:36:26 GMT  
		Size: 28.7 MB (28744913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98bab0c59c329bc0372b1d829f355da3eaee9c050510954a5286c1efeb1186da`  
		Last Modified: Tue, 14 Jan 2025 07:02:17 GMT  
		Size: 5.0 MB (5003559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa83362d5761bbccb4c2e343d52ea7f888268b7c881eb988eec8420da94771c3`  
		Last Modified: Tue, 14 Jan 2025 07:02:41 GMT  
		Size: 33.2 MB (33181578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50faa8d2d1e297aecf04fa3cb862907be2c7c1fc44948018a284f9b17a8c8c63`  
		Last Modified: Tue, 14 Jan 2025 07:02:40 GMT  
		Size: 12.2 KB (12241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b8fd9d7d5d2c0ec9d3f7c6e0792d5a3bda1aa536b2416ee22961d85aec1da64`  
		Last Modified: Tue, 14 Jan 2025 07:02:40 GMT  
		Size: 11.9 KB (11901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6725fc396b26df3bd7ff1d414d1445cff57f25b8b1d26752d3669cc73e94b4c`  
		Last Modified: Tue, 14 Jan 2025 07:02:41 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9.4` - unknown; unknown

```console
$ docker pull chronograf@sha256:5bb2088d9da76b89e35fd6fe273aad228967a72fc8fcd77ecf926bde376d25fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2983441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbb66c8a4581c229fb9926b7d1531277172fa892bd09a835f3793ae99268834f`

```dockerfile
```

-	Layers:
	-	`sha256:0ff0ceb0982281118b2acc98525b908e189ed5ef9e98538fbed29152bf888ea9`  
		Last Modified: Tue, 14 Jan 2025 07:02:41 GMT  
		Size: 3.0 MB (2967536 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c86b291c4e0866169d05caebeee7a06ed9f6c50587c0294fe079b15d78ef35b`  
		Last Modified: Tue, 14 Jan 2025 07:02:40 GMT  
		Size: 15.9 KB (15905 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.9.4-alpine`

```console
$ docker pull chronograf@sha256:aa92223a25f515409f9f656182c5f7206421bf02e3d391e9c01770165ed09c9f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.9.4-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:6ecccec248bcce1ecf0dcfe43ab23068a93c13af96a752ebcfa602ba570ced5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23617292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b00653f032a0cd642084ec3e94f34a4a2e23b07f23f9be35986ab3647a12568d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
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
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Wed, 08 Jan 2025 15:55:45 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afe7fcb9c117622d9b76b0cebecdb2fe8ff1ff52419a133b7429370ec4bf75b0`  
		Last Modified: Wed, 08 Jan 2025 18:14:06 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:666a211b7d8fbd8876fab29f7120cf3c11a68a0f59279c107badb4e1bdb714ad`  
		Last Modified: Wed, 08 Jan 2025 18:14:06 GMT  
		Size: 294.4 KB (294367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9793be8b948ef211ee8c44e8c33b425011056710ba6a23fca9861b4ec99b4da9`  
		Last Modified: Wed, 08 Jan 2025 18:14:06 GMT  
		Size: 19.7 MB (19672018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b98c71573af081597d12ca72b1f672d9abfc0bfabc90bdb53d5b278f13b4b5e9`  
		Last Modified: Wed, 08 Jan 2025 18:14:06 GMT  
		Size: 12.2 KB (12236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4296437122a9507fc662bf7e0ce0648a735459f910dc992723c1fa572502ff9a`  
		Last Modified: Wed, 08 Jan 2025 18:14:07 GMT  
		Size: 11.9 KB (11893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7e8c86465fb666432b74fe5f04c22d9d26d182546a744afa302339288a386e1`  
		Last Modified: Wed, 08 Jan 2025 18:14:07 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9.4-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:992ed9f4af10a3c98123ffe07804827ccdad6aeca3b9cbfef8b1733fdf0168c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.0 KB (252025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22cebb48a8a7336c3d4e1c7e5afdc35734f8fc776e4efd4ab80f9ea3c7122f80`

```dockerfile
```

-	Layers:
	-	`sha256:436e27fdbcf1a58d037af89205400a63468caeabdb8c0708212cc4702db0a3c2`  
		Last Modified: Wed, 08 Jan 2025 18:14:06 GMT  
		Size: 235.1 KB (235116 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b1e8475858167e931497026c48659bbb3c1085dad44cca1ae254f70b77705dd`  
		Last Modified: Wed, 08 Jan 2025 18:14:06 GMT  
		Size: 16.9 KB (16909 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:alpine`

```console
$ docker pull chronograf@sha256:fd22e60efc394d9cf49addff75db9896bdaa59a92831d5a649f57600241b5aef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:565eafbccd78da51863ddc5af1c325bd0755703b61e5058bf3f7bb8744fbfbd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31814451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99b96aa2eecd223e38af88a65ce94b8a24ce929843e8288f199df8966577e3c8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
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
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Wed, 08 Jan 2025 15:55:45 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f10033a10c25d8a78cc5c79537d8be6f9f9570d55e41149047e0eb842ff20ff7`  
		Last Modified: Wed, 08 Jan 2025 18:14:08 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e8e1ed9e8da33db6dd03408084a900ae90824d89fc2a9b14f453422b5119fe4`  
		Last Modified: Wed, 08 Jan 2025 18:14:08 GMT  
		Size: 296.5 KB (296485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13a1a285f7323a6ea298bbeb818f3c80ab849a601de7e3c5d4f18ed1737c58ab`  
		Last Modified: Wed, 08 Jan 2025 18:14:08 GMT  
		Size: 27.9 MB (27866995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0e09ce57cfd00606804f6da64b2f6d7ed8e7ebd061da4dd39492ae664d5f448`  
		Last Modified: Wed, 08 Jan 2025 18:14:08 GMT  
		Size: 12.2 KB (12240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d437e77355a9d05d3b5d3567741989e1cdf431b8932402e004f46d65d597880`  
		Last Modified: Wed, 08 Jan 2025 18:14:09 GMT  
		Size: 11.9 KB (11898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09cab2e3ba35d3a80672462930883bcc165643bc56c7a7cb85e2274f5f883bb6`  
		Last Modified: Wed, 08 Jan 2025 18:14:09 GMT  
		Size: 293.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:4726a1af05f478eacb4e6ae7496295c8268530b94e341d465ce0254387d21986
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.4 KB (259450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4773308778b046fbf1cbd918492fb3e6940cbc43a637d34229c4a2bfddd28643`

```dockerfile
```

-	Layers:
	-	`sha256:dc9afdf2d7e83acbbcf82584839e1029a9fc056cda18c507457ad2f4c11ae85b`  
		Last Modified: Wed, 08 Jan 2025 18:14:08 GMT  
		Size: 241.6 KB (241595 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb03332e1a4f6d331e2c7201bd529d7e3b2c5caf81b355aa80d22f0c624368bc`  
		Last Modified: Wed, 08 Jan 2025 18:14:08 GMT  
		Size: 17.9 KB (17855 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:latest`

```console
$ docker pull chronograf@sha256:6a7f7bd8b9459f85b2505cc6e5b991eedf7ec92bce1e984fdcb430e1cde78b09
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
$ docker pull chronograf@sha256:5c778bc81892bf7d857e84056d7f404c08d8e1a8b3a61b8be78c3456444e6c3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.3 MB (83329784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dc6296f978c36c764aeba47abfda2c2f8cfb6b6d335e6613447702b2671f9dc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
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
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea4677274335b6d13e9d85d2cb59ce3c040ab4fe297a219c71486d0a997fdf60`  
		Last Modified: Tue, 04 Feb 2025 04:38:20 GMT  
		Size: 7.9 MB (7875460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e341bdf0db524398c580141c359facb380260a87e863fd011ab4f9fd9f18700`  
		Last Modified: Tue, 04 Feb 2025 04:38:20 GMT  
		Size: 47.2 MB (47217554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5b773fd7294d9043bd106a1bd32e4ae5d935c95fa2f6c71e8402c967af36daa`  
		Last Modified: Tue, 04 Feb 2025 04:38:19 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:959c37d0b325d913afc6820bc08751b8c345ececd2e9019a6eebe37bbbef5fed`  
		Last Modified: Tue, 04 Feb 2025 04:38:20 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b22ab05d59f0f8196b08ac45a7b94f98c851c519e6c70a6c1c99113ca2fb67ed`  
		Last Modified: Tue, 04 Feb 2025 04:38:20 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:1b2e6e5404f443d80444bddcc3f103f3b8f87280e6912fae9f228d314a7877d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2719989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7461f550112f8d4354117a9c1ef0e0bc7ece095b4991a5f14e7ae843b83643c`

```dockerfile
```

-	Layers:
	-	`sha256:4d2610d19117b875074759f759521347e466a19de34b8e92d9f6758c8f854b06`  
		Last Modified: Tue, 04 Feb 2025 04:38:20 GMT  
		Size: 2.7 MB (2703861 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c59690fa3689bb8814d4273ccbf864c2d4cb427966be0444f656eb830c15c81`  
		Last Modified: Tue, 04 Feb 2025 04:38:19 GMT  
		Size: 16.1 KB (16128 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:latest` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:b8eaf491a3d51ab1ad081116051d6319665ea6a159f15552fb042a8880452e0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74713234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1631585b9c6c1e93b600a77695687e7dd10bb578920dd6f3c03efc21143d4f7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1736726400'
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
	-	`sha256:f7fde15b664589586a61b714ca6b43dec045d0f187d81d4eb050918e17b0ff1e`  
		Last Modified: Tue, 14 Jan 2025 01:35:15 GMT  
		Size: 23.9 MB (23914600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31eb12efed5eb5b137542a8591ffaddcfec2ab7fbb3e4d81891c4d2ddc47283c`  
		Last Modified: Tue, 14 Jan 2025 09:02:48 GMT  
		Size: 6.5 MB (6497830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff49de7a4cba1c7f1e033fadd98d847bc9f2aed1a1b8faac5681a4d17c5590ec`  
		Last Modified: Tue, 14 Jan 2025 09:02:48 GMT  
		Size: 44.3 MB (44276343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52c409b1b91c6fc27ad30d021a65179e77d13efde84ee96abf30a124f3a86825`  
		Last Modified: Tue, 14 Jan 2025 09:02:46 GMT  
		Size: 12.2 KB (12244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9d49e53e707da3ed5d73b62a4fe374bad1d91274ce451a98133353442723fb9`  
		Last Modified: Tue, 14 Jan 2025 09:02:47 GMT  
		Size: 11.9 KB (11903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:639c7cd00071a0b62766d53b22370535830272a699de91971e54d828c113c6c2`  
		Last Modified: Tue, 14 Jan 2025 09:02:47 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:cb2388b11815c41e02b9ed158ee6d627b8e7e9ba4baae043731552a2ce9f769e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2722366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a07c2b25ff90a5be47dfbfe81063611749d333225960cec7a16874dd2006fd37`

```dockerfile
```

-	Layers:
	-	`sha256:e00d8906b7526bc8bca4dbd34a2d75af98b178ba57c9dc6badeb508556ff8f5f`  
		Last Modified: Tue, 14 Jan 2025 09:02:47 GMT  
		Size: 2.7 MB (2706158 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:309aae5baec8f6e76452e0ee1b5f805d2e41571eee241086ef065f31862b2e51`  
		Last Modified: Tue, 14 Jan 2025 09:02:46 GMT  
		Size: 16.2 KB (16208 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:latest` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:e9d2adcbf05b367178d80afae5a4be65bd9d108b97ccd30e3a2e9b762fea0d4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.7 MB (80688086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04eb7b75c8d8d64b5e28916f2541f39346c1027d02cdf4fa472b6650baad04af`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
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
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe5e22ffc62c19f88c63e73d68f6271af6579883314b212065a1f3f823822404`  
		Last Modified: Tue, 14 Jan 2025 07:03:13 GMT  
		Size: 7.7 MB (7652088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9be9572b2df6cf01e21eceea0c61e00397c4baf86724385e960030ed5c53b598`  
		Last Modified: Tue, 14 Jan 2025 07:03:14 GMT  
		Size: 45.0 MB (44970507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d41d08252d2d81e968b86f218af88b55a264ed843cf51c41ee846cada501a2a`  
		Last Modified: Tue, 14 Jan 2025 07:03:12 GMT  
		Size: 12.2 KB (12243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee5d82b281a9621c48cced8f12640673ffafe06d54a29b7fd724247b1f8f95bc`  
		Last Modified: Tue, 14 Jan 2025 07:03:12 GMT  
		Size: 11.9 KB (11902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f9a4caa4163798a2515cd4a99fff2a3633d45f79045264085c0e6df6fee2b2a`  
		Last Modified: Tue, 14 Jan 2025 07:03:13 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:125aa83ae8a8ff760a9654a30dfecdaea5cd9c8c4dab202c68a7e84528a142f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2720369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:829ced801ce3aa5bbc969ab7e89d23f24cf6ebf385b222e94b27c2c48913a446`

```dockerfile
```

-	Layers:
	-	`sha256:8110c7aede011c065bc590dfb8d4c5f389270f45ffc4f9103cb3a9de4099299f`  
		Last Modified: Tue, 14 Jan 2025 07:03:13 GMT  
		Size: 2.7 MB (2704134 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2d534b8b0f8a046a6dcbd52c6eab0e8a1e013b983679b8f41cc875a2b9aa1ca`  
		Last Modified: Tue, 14 Jan 2025 07:03:12 GMT  
		Size: 16.2 KB (16235 bytes)  
		MIME: application/vnd.in-toto+json
