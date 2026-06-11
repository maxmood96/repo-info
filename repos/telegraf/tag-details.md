<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `telegraf`

-	[`telegraf:1.37`](#telegraf137)
-	[`telegraf:1.37-alpine`](#telegraf137-alpine)
-	[`telegraf:1.37.3`](#telegraf1373)
-	[`telegraf:1.37.3-alpine`](#telegraf1373-alpine)
-	[`telegraf:1.38`](#telegraf138)
-	[`telegraf:1.38-alpine`](#telegraf138-alpine)
-	[`telegraf:1.38.4`](#telegraf1384)
-	[`telegraf:1.38.4-alpine`](#telegraf1384-alpine)
-	[`telegraf:1.39`](#telegraf139)
-	[`telegraf:1.39-alpine`](#telegraf139-alpine)
-	[`telegraf:1.39.0`](#telegraf1390)
-	[`telegraf:1.39.0-alpine`](#telegraf1390-alpine)
-	[`telegraf:alpine`](#telegrafalpine)
-	[`telegraf:latest`](#telegraflatest)

## `telegraf:1.37`

```console
$ docker pull telegraf@sha256:6200cc9ab56baf61feabdfeca95956d5bdb880402aab6704cc82f202a863c239
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
$ docker pull telegraf@sha256:540821e7c1d936939d72a90ea543e13db1c97da16ca5ad281c5e5f106b58b791
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.3 MB (172278963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cab70ae82e0b25a61b979b073a283d6158e2ea8f40dc1de9151019f8a16be560`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:42:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 02:37:54 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 02:37:55 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Thu, 11 Jun 2026 02:37:59 GMT
ENV TELEGRAF_VERSION=1.37.3
# Thu, 11 Jun 2026 02:37:59 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Thu, 11 Jun 2026 02:37:59 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Thu, 11 Jun 2026 02:37:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Jun 2026 02:37:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jun 2026 02:37:59 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:01cedcff86f879d042805360ecba268802bec3d8201484ff3ec54f4250a2d3b7`  
		Last Modified: Wed, 10 Jun 2026 23:39:39 GMT  
		Size: 48.5 MB (48502042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4da31edd9efdb812e66d13819903973ea6b188d2e7358547676d33d1e3f706f2`  
		Last Modified: Thu, 11 Jun 2026 00:42:23 GMT  
		Size: 24.0 MB (24044000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5c5d25e682b8511b89540a207437e1049c9eb10d917b8743db54f0c6210d077`  
		Last Modified: Thu, 11 Jun 2026 02:38:18 GMT  
		Size: 18.9 MB (18944025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:060021b7513e0ef9bff29adb2ac7344f71998104571e3823f3b6c62d72a7a45b`  
		Last Modified: Thu, 11 Jun 2026 02:38:17 GMT  
		Size: 5.1 KB (5070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eb615e19c1c0d6f400e99ede44aaa294c7a3c02937095bda6f5b7315658eb0b`  
		Last Modified: Thu, 11 Jun 2026 02:38:20 GMT  
		Size: 80.8 MB (80783202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43619133a45988816667ea2d066f1f2ccdde65dcfe0cffae04446297151f0d0b`  
		Last Modified: Thu, 11 Jun 2026 02:38:17 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.37` - unknown; unknown

```console
$ docker pull telegraf@sha256:3966b0ec30726bfa83f9d6d30601822b3d2b0c0b4d5ddee9bd620aef1e11b95b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6681421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67cc40a8319c59d9bfbd1d6e711665799883a98805de8d834bf78edf1d392ed4`

```dockerfile
```

-	Layers:
	-	`sha256:41b6962d39b6b060c9da10ccfebbb37b73d17a35ae5451fdea96b9c0682f5e29`  
		Last Modified: Thu, 11 Jun 2026 02:38:17 GMT  
		Size: 6.7 MB (6666994 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e562a59e43711092f98f964ec0f5e6f828ec120efce383a25979cabdc7a8886e`  
		Last Modified: Thu, 11 Jun 2026 02:38:17 GMT  
		Size: 14.4 KB (14427 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.37` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:cf88df4b5c0ebe7a1d22574560be19f579e0b9bc6702d61f10a2f02e50eceaa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.5 MB (158480931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c6a6e9341680389bd52579c638566d8e9666872e2c89a772356b7324dd9b77a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 01:23:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 03:12:10 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 03:12:11 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Thu, 11 Jun 2026 03:12:16 GMT
ENV TELEGRAF_VERSION=1.37.3
# Thu, 11 Jun 2026 03:12:16 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Thu, 11 Jun 2026 03:12:16 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Thu, 11 Jun 2026 03:12:16 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Jun 2026 03:12:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jun 2026 03:12:16 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:c0213091aa87e4be7caed06dd364889c231dab5ba50fa1e54365eb7a94390261`  
		Last Modified: Wed, 10 Jun 2026 23:39:46 GMT  
		Size: 44.2 MB (44208065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d14356188705148a948907491c78974967557826c6ca92209148b3bc14f0f659`  
		Last Modified: Thu, 11 Jun 2026 01:23:38 GMT  
		Size: 21.9 MB (21949873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7f4f71b7aa7967cac2e7fe74af896b10f8575011077f212b22b07da3142ecaf`  
		Last Modified: Thu, 11 Jun 2026 03:12:33 GMT  
		Size: 17.7 MB (17699840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd6124c403094611ad92756a567cdf29c0faf7343e692f5bd0809739cbe6b18`  
		Last Modified: Thu, 11 Jun 2026 03:12:32 GMT  
		Size: 5.1 KB (5069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3adc3c832937a8d506708861673cd47425e07c67972cacb2b9b43174b0143f0`  
		Last Modified: Thu, 11 Jun 2026 03:12:36 GMT  
		Size: 74.6 MB (74617462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5dadfde0f93516ab2250aa2b81967f2ef6a5bd9b526bed6e71edd68786efab8`  
		Last Modified: Thu, 11 Jun 2026 03:12:32 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.37` - unknown; unknown

```console
$ docker pull telegraf@sha256:867ce862e4ace0c4d30828ed72bfe01609c4cf8f6468c574e7ce5382c52ff9d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6676107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:943997f5c3119cbb8501ade9f65e68068e6967b3032cdb6f63d7e622a33b5bfd`

```dockerfile
```

-	Layers:
	-	`sha256:c1380b8fcb81267a08fec40ab605084d3d5cf4f3b266979c3518f769c6d71090`  
		Last Modified: Thu, 11 Jun 2026 03:12:33 GMT  
		Size: 6.7 MB (6661591 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b4c2e687a09adb925e74a272414a7b15fd2d6bc9d72886c46decaa866fdcc99`  
		Last Modified: Thu, 11 Jun 2026 03:12:32 GMT  
		Size: 14.5 KB (14516 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.37` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:fcfe8a58ad0b7f727aab1736b0a531be5f8623d18bca9db4ed8519a99389c13f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.1 MB (163064890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28b93cc8686bd901a080e2f92039c20617f94a3cd07b134a4e3aab5194b448b0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:43:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 02:37:33 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 02:37:34 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Thu, 11 Jun 2026 02:37:38 GMT
ENV TELEGRAF_VERSION=1.37.3
# Thu, 11 Jun 2026 02:37:38 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Thu, 11 Jun 2026 02:37:38 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Thu, 11 Jun 2026 02:37:38 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Jun 2026 02:37:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jun 2026 02:37:38 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:c847f328095fb083f4a22895b90fe4226efa6458ac57362b64b6e5d99da9e4a3`  
		Last Modified: Wed, 10 Jun 2026 23:39:28 GMT  
		Size: 48.4 MB (48389016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f511b4c80a6e453785fbcd573c1bf1cb986c4e8d43ed4500ad1ac9a4719762b`  
		Last Modified: Thu, 11 Jun 2026 00:43:56 GMT  
		Size: 23.6 MB (23613296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c190ef3f5f7acc6d44552bd3c4080c3a0fe6a2b8c594caff252a7a6d1b89a523`  
		Last Modified: Thu, 11 Jun 2026 02:37:55 GMT  
		Size: 18.9 MB (18885883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f24b9de6d86f6333b5aa1983c1dd0a8f6873a5a2904c22c512d14cbd25b77c`  
		Last Modified: Thu, 11 Jun 2026 02:37:55 GMT  
		Size: 5.1 KB (5071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79da11f6c6e9ed536df5b256e4538d36f21857459ad039bde72c6636e5f5445e`  
		Last Modified: Thu, 11 Jun 2026 02:37:57 GMT  
		Size: 72.2 MB (72170999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e208dc574291067cffff2f423a7abf48abfa9a91d02347b04e4858f79dc95dbc`  
		Last Modified: Thu, 11 Jun 2026 02:37:55 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.37` - unknown; unknown

```console
$ docker pull telegraf@sha256:b17522f9538ef3b69a0284a1e8db8b4cf4b2f54778cb0f434b23cfb91de8777f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6682207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aff99d567a5fde6df4f3ed1ff473ab938a3cb8c3e9e2ac5996a956bd60208d55`

```dockerfile
```

-	Layers:
	-	`sha256:06e13e957888e12d836a12c0eda088e429308f7d167661b31d422e2f56a7ba60`  
		Last Modified: Thu, 11 Jun 2026 02:37:55 GMT  
		Size: 6.7 MB (6667670 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b68793260588f2f9de0df9b8bd28bd6430a6e471b159e7ef751f116a2cf6b0ff`  
		Last Modified: Thu, 11 Jun 2026 02:37:55 GMT  
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
$ docker pull telegraf@sha256:6200cc9ab56baf61feabdfeca95956d5bdb880402aab6704cc82f202a863c239
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
$ docker pull telegraf@sha256:540821e7c1d936939d72a90ea543e13db1c97da16ca5ad281c5e5f106b58b791
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.3 MB (172278963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cab70ae82e0b25a61b979b073a283d6158e2ea8f40dc1de9151019f8a16be560`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:42:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 02:37:54 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 02:37:55 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Thu, 11 Jun 2026 02:37:59 GMT
ENV TELEGRAF_VERSION=1.37.3
# Thu, 11 Jun 2026 02:37:59 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Thu, 11 Jun 2026 02:37:59 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Thu, 11 Jun 2026 02:37:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Jun 2026 02:37:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jun 2026 02:37:59 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:01cedcff86f879d042805360ecba268802bec3d8201484ff3ec54f4250a2d3b7`  
		Last Modified: Wed, 10 Jun 2026 23:39:39 GMT  
		Size: 48.5 MB (48502042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4da31edd9efdb812e66d13819903973ea6b188d2e7358547676d33d1e3f706f2`  
		Last Modified: Thu, 11 Jun 2026 00:42:23 GMT  
		Size: 24.0 MB (24044000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5c5d25e682b8511b89540a207437e1049c9eb10d917b8743db54f0c6210d077`  
		Last Modified: Thu, 11 Jun 2026 02:38:18 GMT  
		Size: 18.9 MB (18944025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:060021b7513e0ef9bff29adb2ac7344f71998104571e3823f3b6c62d72a7a45b`  
		Last Modified: Thu, 11 Jun 2026 02:38:17 GMT  
		Size: 5.1 KB (5070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eb615e19c1c0d6f400e99ede44aaa294c7a3c02937095bda6f5b7315658eb0b`  
		Last Modified: Thu, 11 Jun 2026 02:38:20 GMT  
		Size: 80.8 MB (80783202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43619133a45988816667ea2d066f1f2ccdde65dcfe0cffae04446297151f0d0b`  
		Last Modified: Thu, 11 Jun 2026 02:38:17 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.37.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:3966b0ec30726bfa83f9d6d30601822b3d2b0c0b4d5ddee9bd620aef1e11b95b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6681421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67cc40a8319c59d9bfbd1d6e711665799883a98805de8d834bf78edf1d392ed4`

```dockerfile
```

-	Layers:
	-	`sha256:41b6962d39b6b060c9da10ccfebbb37b73d17a35ae5451fdea96b9c0682f5e29`  
		Last Modified: Thu, 11 Jun 2026 02:38:17 GMT  
		Size: 6.7 MB (6666994 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e562a59e43711092f98f964ec0f5e6f828ec120efce383a25979cabdc7a8886e`  
		Last Modified: Thu, 11 Jun 2026 02:38:17 GMT  
		Size: 14.4 KB (14427 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.37.3` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:cf88df4b5c0ebe7a1d22574560be19f579e0b9bc6702d61f10a2f02e50eceaa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.5 MB (158480931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c6a6e9341680389bd52579c638566d8e9666872e2c89a772356b7324dd9b77a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 01:23:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 03:12:10 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 03:12:11 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Thu, 11 Jun 2026 03:12:16 GMT
ENV TELEGRAF_VERSION=1.37.3
# Thu, 11 Jun 2026 03:12:16 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Thu, 11 Jun 2026 03:12:16 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Thu, 11 Jun 2026 03:12:16 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Jun 2026 03:12:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jun 2026 03:12:16 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:c0213091aa87e4be7caed06dd364889c231dab5ba50fa1e54365eb7a94390261`  
		Last Modified: Wed, 10 Jun 2026 23:39:46 GMT  
		Size: 44.2 MB (44208065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d14356188705148a948907491c78974967557826c6ca92209148b3bc14f0f659`  
		Last Modified: Thu, 11 Jun 2026 01:23:38 GMT  
		Size: 21.9 MB (21949873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7f4f71b7aa7967cac2e7fe74af896b10f8575011077f212b22b07da3142ecaf`  
		Last Modified: Thu, 11 Jun 2026 03:12:33 GMT  
		Size: 17.7 MB (17699840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd6124c403094611ad92756a567cdf29c0faf7343e692f5bd0809739cbe6b18`  
		Last Modified: Thu, 11 Jun 2026 03:12:32 GMT  
		Size: 5.1 KB (5069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3adc3c832937a8d506708861673cd47425e07c67972cacb2b9b43174b0143f0`  
		Last Modified: Thu, 11 Jun 2026 03:12:36 GMT  
		Size: 74.6 MB (74617462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5dadfde0f93516ab2250aa2b81967f2ef6a5bd9b526bed6e71edd68786efab8`  
		Last Modified: Thu, 11 Jun 2026 03:12:32 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.37.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:867ce862e4ace0c4d30828ed72bfe01609c4cf8f6468c574e7ce5382c52ff9d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6676107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:943997f5c3119cbb8501ade9f65e68068e6967b3032cdb6f63d7e622a33b5bfd`

```dockerfile
```

-	Layers:
	-	`sha256:c1380b8fcb81267a08fec40ab605084d3d5cf4f3b266979c3518f769c6d71090`  
		Last Modified: Thu, 11 Jun 2026 03:12:33 GMT  
		Size: 6.7 MB (6661591 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b4c2e687a09adb925e74a272414a7b15fd2d6bc9d72886c46decaa866fdcc99`  
		Last Modified: Thu, 11 Jun 2026 03:12:32 GMT  
		Size: 14.5 KB (14516 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.37.3` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:fcfe8a58ad0b7f727aab1736b0a531be5f8623d18bca9db4ed8519a99389c13f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.1 MB (163064890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28b93cc8686bd901a080e2f92039c20617f94a3cd07b134a4e3aab5194b448b0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:43:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 02:37:33 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 02:37:34 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Thu, 11 Jun 2026 02:37:38 GMT
ENV TELEGRAF_VERSION=1.37.3
# Thu, 11 Jun 2026 02:37:38 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Thu, 11 Jun 2026 02:37:38 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Thu, 11 Jun 2026 02:37:38 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Jun 2026 02:37:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jun 2026 02:37:38 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:c847f328095fb083f4a22895b90fe4226efa6458ac57362b64b6e5d99da9e4a3`  
		Last Modified: Wed, 10 Jun 2026 23:39:28 GMT  
		Size: 48.4 MB (48389016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f511b4c80a6e453785fbcd573c1bf1cb986c4e8d43ed4500ad1ac9a4719762b`  
		Last Modified: Thu, 11 Jun 2026 00:43:56 GMT  
		Size: 23.6 MB (23613296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c190ef3f5f7acc6d44552bd3c4080c3a0fe6a2b8c594caff252a7a6d1b89a523`  
		Last Modified: Thu, 11 Jun 2026 02:37:55 GMT  
		Size: 18.9 MB (18885883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f24b9de6d86f6333b5aa1983c1dd0a8f6873a5a2904c22c512d14cbd25b77c`  
		Last Modified: Thu, 11 Jun 2026 02:37:55 GMT  
		Size: 5.1 KB (5071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79da11f6c6e9ed536df5b256e4538d36f21857459ad039bde72c6636e5f5445e`  
		Last Modified: Thu, 11 Jun 2026 02:37:57 GMT  
		Size: 72.2 MB (72170999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e208dc574291067cffff2f423a7abf48abfa9a91d02347b04e4858f79dc95dbc`  
		Last Modified: Thu, 11 Jun 2026 02:37:55 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.37.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:b17522f9538ef3b69a0284a1e8db8b4cf4b2f54778cb0f434b23cfb91de8777f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6682207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aff99d567a5fde6df4f3ed1ff473ab938a3cb8c3e9e2ac5996a956bd60208d55`

```dockerfile
```

-	Layers:
	-	`sha256:06e13e957888e12d836a12c0eda088e429308f7d167661b31d422e2f56a7ba60`  
		Last Modified: Thu, 11 Jun 2026 02:37:55 GMT  
		Size: 6.7 MB (6667670 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b68793260588f2f9de0df9b8bd28bd6430a6e471b159e7ef751f116a2cf6b0ff`  
		Last Modified: Thu, 11 Jun 2026 02:37:55 GMT  
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
$ docker pull telegraf@sha256:5fcea414e39f49ffda05b4dd359586752803d5060a7713fdb17fd77528c355e0
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
$ docker pull telegraf@sha256:ee4366160d6315969aa45fc26cf95c30160edaf1eebc905381535126933a9a7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.0 MB (175007161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a2e4686810792bbe410718383b8dfe7e590607ae7004d2350bbae370477fd19`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:42:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 02:38:00 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 02:38:00 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Thu, 11 Jun 2026 02:38:04 GMT
ENV TELEGRAF_VERSION=1.38.4
# Thu, 11 Jun 2026 02:38:04 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Thu, 11 Jun 2026 02:38:04 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Thu, 11 Jun 2026 02:38:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Jun 2026 02:38:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jun 2026 02:38:04 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:01cedcff86f879d042805360ecba268802bec3d8201484ff3ec54f4250a2d3b7`  
		Last Modified: Wed, 10 Jun 2026 23:39:39 GMT  
		Size: 48.5 MB (48502042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4da31edd9efdb812e66d13819903973ea6b188d2e7358547676d33d1e3f706f2`  
		Last Modified: Thu, 11 Jun 2026 00:42:23 GMT  
		Size: 24.0 MB (24044000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49e4325e58c2f6af137d87e461e374cb51f5303f310ccf5bd3ee4f6621942721`  
		Last Modified: Thu, 11 Jun 2026 02:38:23 GMT  
		Size: 18.9 MB (18944350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bba15729782f0b2801f8329537629b930ea7a2eb434172d0475792d3e81b54b`  
		Last Modified: Thu, 11 Jun 2026 02:38:22 GMT  
		Size: 5.1 KB (5055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f9f846d29ea4f40a10d459e24e56d47edbe49829532ab4d253d2c4ae920ae03`  
		Last Modified: Thu, 11 Jun 2026 02:38:25 GMT  
		Size: 83.5 MB (83511091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b0d336a7afeb32aa18b00151cd3388b2adbe3af11c7c8118cb754301934690d`  
		Last Modified: Thu, 11 Jun 2026 02:38:23 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.38` - unknown; unknown

```console
$ docker pull telegraf@sha256:9da46f1a14cc111e8184f632bbdf3aada74c22fbae8fba214bc881ca32de9282
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6688726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b85584a82824500243669f169bad9e9af7f724c8041e80ce17353dc03074430`

```dockerfile
```

-	Layers:
	-	`sha256:d87ae5763db3e837c311b283207a99c0e18f65f04bb7a6b178f1697c74088a7f`  
		Last Modified: Thu, 11 Jun 2026 02:38:23 GMT  
		Size: 6.7 MB (6674299 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51f68ab484104df6c43f16475eccd46a5fab3eb9fe91790e548c7e89ad77bff8`  
		Last Modified: Thu, 11 Jun 2026 02:38:22 GMT  
		Size: 14.4 KB (14427 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.38` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:4d391c769205e5b9f96ea1e766c1fed9e376856e95a63b8bdcb29d8b60f1efa9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.3 MB (161291163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59c519830d33ee00374aed3a8bc76e87ab71b58a7a6cd309b2618c6d50d91918`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 01:23:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 03:12:28 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 03:12:28 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Thu, 11 Jun 2026 03:12:34 GMT
ENV TELEGRAF_VERSION=1.38.4
# Thu, 11 Jun 2026 03:12:34 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Thu, 11 Jun 2026 03:12:34 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Thu, 11 Jun 2026 03:12:34 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Jun 2026 03:12:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jun 2026 03:12:34 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:c0213091aa87e4be7caed06dd364889c231dab5ba50fa1e54365eb7a94390261`  
		Last Modified: Wed, 10 Jun 2026 23:39:46 GMT  
		Size: 44.2 MB (44208065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d14356188705148a948907491c78974967557826c6ca92209148b3bc14f0f659`  
		Last Modified: Thu, 11 Jun 2026 01:23:38 GMT  
		Size: 21.9 MB (21949873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44af63200c8763646e024454fa5e03a3c2b62c5dac697147c3b446e04c173d9a`  
		Last Modified: Thu, 11 Jun 2026 03:12:54 GMT  
		Size: 17.7 MB (17699616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6785b770b93531cf6824747880e75ce709b34aafdffa0a59344dd566d5414baa`  
		Last Modified: Thu, 11 Jun 2026 03:12:53 GMT  
		Size: 5.1 KB (5056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f1d7202d3c0241b13428b12027d5756896eb1dc409d7ab02258aaa50d3a3e8e`  
		Last Modified: Thu, 11 Jun 2026 03:12:56 GMT  
		Size: 77.4 MB (77427931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08c6c4631d6cf8f6e3e68d99d26284e543110e8e98fd7257c18c9b8f4bf87950`  
		Last Modified: Thu, 11 Jun 2026 03:12:53 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.38` - unknown; unknown

```console
$ docker pull telegraf@sha256:35cc8deccbaaafa1ded92919d067350f12cc73c344b5b39ced0fb125bbcc4d59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6683413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6918a51755842276d754e3dc914aaab97639e0f69da00f63e1cf177d4e670f47`

```dockerfile
```

-	Layers:
	-	`sha256:228b1eef15c6a7c7dbe2b7f9ec9d389cffb9a626ade752ea0bb37b5bf74c14a6`  
		Last Modified: Thu, 11 Jun 2026 03:12:54 GMT  
		Size: 6.7 MB (6668896 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef3232a2ea3c0f02f8962844cd9ba7a214836f65ac1f695cc110c8b1028cac2f`  
		Last Modified: Thu, 11 Jun 2026 03:12:53 GMT  
		Size: 14.5 KB (14517 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.38` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:dc19e304233d3e7826b66540919384f11c4dd8d373b67900870bcfa097996b15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.4 MB (165370549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:306b724d73159fed98c387b9e8e893dbfb39a385af5785a2993ce9b0376b8186`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:43:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 02:38:02 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 02:38:03 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Thu, 11 Jun 2026 02:38:07 GMT
ENV TELEGRAF_VERSION=1.38.4
# Thu, 11 Jun 2026 02:38:07 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Thu, 11 Jun 2026 02:38:07 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Thu, 11 Jun 2026 02:38:07 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Jun 2026 02:38:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jun 2026 02:38:07 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:c847f328095fb083f4a22895b90fe4226efa6458ac57362b64b6e5d99da9e4a3`  
		Last Modified: Wed, 10 Jun 2026 23:39:28 GMT  
		Size: 48.4 MB (48389016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f511b4c80a6e453785fbcd573c1bf1cb986c4e8d43ed4500ad1ac9a4719762b`  
		Last Modified: Thu, 11 Jun 2026 00:43:56 GMT  
		Size: 23.6 MB (23613296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:626a0843d1e475e7995383906770115761545199c6fc7f909e2a4f54e72abb2e`  
		Last Modified: Thu, 11 Jun 2026 02:38:25 GMT  
		Size: 18.9 MB (18885765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faba5a110e88bbe89235aee61fa6243ce139bfe94fbb60171dfb8a727259c4e5`  
		Last Modified: Thu, 11 Jun 2026 02:38:24 GMT  
		Size: 5.1 KB (5069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b323b177bf29334b8a45dcbb48b067ea8e49a135d49202e14d71a6d36a9b62aa`  
		Last Modified: Thu, 11 Jun 2026 02:38:26 GMT  
		Size: 74.5 MB (74476780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b0d336a7afeb32aa18b00151cd3388b2adbe3af11c7c8118cb754301934690d`  
		Last Modified: Thu, 11 Jun 2026 02:38:23 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.38` - unknown; unknown

```console
$ docker pull telegraf@sha256:aa21293244a6a0237dc53c8db2c715625b2e2979d57ac806913af342622ea778
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6689512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcb4b1f9007724aa4c9633effe6f52a0a58d2d131083a7f46168406f45dd2596`

```dockerfile
```

-	Layers:
	-	`sha256:78d4f833c2cf1b0c86bbab218f72d895d263baf4171e07a8cace9102acc2e602`  
		Last Modified: Thu, 11 Jun 2026 02:38:24 GMT  
		Size: 6.7 MB (6674975 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be60d940b566988b121930e240c5d5d8f1ae454ff3f232191022d6f7a4447dda`  
		Last Modified: Thu, 11 Jun 2026 02:38:24 GMT  
		Size: 14.5 KB (14537 bytes)  
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
$ docker pull telegraf@sha256:5fcea414e39f49ffda05b4dd359586752803d5060a7713fdb17fd77528c355e0
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
$ docker pull telegraf@sha256:ee4366160d6315969aa45fc26cf95c30160edaf1eebc905381535126933a9a7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.0 MB (175007161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a2e4686810792bbe410718383b8dfe7e590607ae7004d2350bbae370477fd19`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:42:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 02:38:00 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 02:38:00 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Thu, 11 Jun 2026 02:38:04 GMT
ENV TELEGRAF_VERSION=1.38.4
# Thu, 11 Jun 2026 02:38:04 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Thu, 11 Jun 2026 02:38:04 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Thu, 11 Jun 2026 02:38:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Jun 2026 02:38:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jun 2026 02:38:04 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:01cedcff86f879d042805360ecba268802bec3d8201484ff3ec54f4250a2d3b7`  
		Last Modified: Wed, 10 Jun 2026 23:39:39 GMT  
		Size: 48.5 MB (48502042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4da31edd9efdb812e66d13819903973ea6b188d2e7358547676d33d1e3f706f2`  
		Last Modified: Thu, 11 Jun 2026 00:42:23 GMT  
		Size: 24.0 MB (24044000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49e4325e58c2f6af137d87e461e374cb51f5303f310ccf5bd3ee4f6621942721`  
		Last Modified: Thu, 11 Jun 2026 02:38:23 GMT  
		Size: 18.9 MB (18944350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bba15729782f0b2801f8329537629b930ea7a2eb434172d0475792d3e81b54b`  
		Last Modified: Thu, 11 Jun 2026 02:38:22 GMT  
		Size: 5.1 KB (5055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f9f846d29ea4f40a10d459e24e56d47edbe49829532ab4d253d2c4ae920ae03`  
		Last Modified: Thu, 11 Jun 2026 02:38:25 GMT  
		Size: 83.5 MB (83511091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b0d336a7afeb32aa18b00151cd3388b2adbe3af11c7c8118cb754301934690d`  
		Last Modified: Thu, 11 Jun 2026 02:38:23 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.38.4` - unknown; unknown

```console
$ docker pull telegraf@sha256:9da46f1a14cc111e8184f632bbdf3aada74c22fbae8fba214bc881ca32de9282
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6688726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b85584a82824500243669f169bad9e9af7f724c8041e80ce17353dc03074430`

```dockerfile
```

-	Layers:
	-	`sha256:d87ae5763db3e837c311b283207a99c0e18f65f04bb7a6b178f1697c74088a7f`  
		Last Modified: Thu, 11 Jun 2026 02:38:23 GMT  
		Size: 6.7 MB (6674299 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51f68ab484104df6c43f16475eccd46a5fab3eb9fe91790e548c7e89ad77bff8`  
		Last Modified: Thu, 11 Jun 2026 02:38:22 GMT  
		Size: 14.4 KB (14427 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.38.4` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:4d391c769205e5b9f96ea1e766c1fed9e376856e95a63b8bdcb29d8b60f1efa9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.3 MB (161291163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59c519830d33ee00374aed3a8bc76e87ab71b58a7a6cd309b2618c6d50d91918`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 01:23:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 03:12:28 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 03:12:28 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Thu, 11 Jun 2026 03:12:34 GMT
ENV TELEGRAF_VERSION=1.38.4
# Thu, 11 Jun 2026 03:12:34 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Thu, 11 Jun 2026 03:12:34 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Thu, 11 Jun 2026 03:12:34 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Jun 2026 03:12:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jun 2026 03:12:34 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:c0213091aa87e4be7caed06dd364889c231dab5ba50fa1e54365eb7a94390261`  
		Last Modified: Wed, 10 Jun 2026 23:39:46 GMT  
		Size: 44.2 MB (44208065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d14356188705148a948907491c78974967557826c6ca92209148b3bc14f0f659`  
		Last Modified: Thu, 11 Jun 2026 01:23:38 GMT  
		Size: 21.9 MB (21949873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44af63200c8763646e024454fa5e03a3c2b62c5dac697147c3b446e04c173d9a`  
		Last Modified: Thu, 11 Jun 2026 03:12:54 GMT  
		Size: 17.7 MB (17699616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6785b770b93531cf6824747880e75ce709b34aafdffa0a59344dd566d5414baa`  
		Last Modified: Thu, 11 Jun 2026 03:12:53 GMT  
		Size: 5.1 KB (5056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f1d7202d3c0241b13428b12027d5756896eb1dc409d7ab02258aaa50d3a3e8e`  
		Last Modified: Thu, 11 Jun 2026 03:12:56 GMT  
		Size: 77.4 MB (77427931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08c6c4631d6cf8f6e3e68d99d26284e543110e8e98fd7257c18c9b8f4bf87950`  
		Last Modified: Thu, 11 Jun 2026 03:12:53 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.38.4` - unknown; unknown

```console
$ docker pull telegraf@sha256:35cc8deccbaaafa1ded92919d067350f12cc73c344b5b39ced0fb125bbcc4d59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6683413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6918a51755842276d754e3dc914aaab97639e0f69da00f63e1cf177d4e670f47`

```dockerfile
```

-	Layers:
	-	`sha256:228b1eef15c6a7c7dbe2b7f9ec9d389cffb9a626ade752ea0bb37b5bf74c14a6`  
		Last Modified: Thu, 11 Jun 2026 03:12:54 GMT  
		Size: 6.7 MB (6668896 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef3232a2ea3c0f02f8962844cd9ba7a214836f65ac1f695cc110c8b1028cac2f`  
		Last Modified: Thu, 11 Jun 2026 03:12:53 GMT  
		Size: 14.5 KB (14517 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.38.4` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:dc19e304233d3e7826b66540919384f11c4dd8d373b67900870bcfa097996b15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.4 MB (165370549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:306b724d73159fed98c387b9e8e893dbfb39a385af5785a2993ce9b0376b8186`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:43:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 02:38:02 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 02:38:03 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Thu, 11 Jun 2026 02:38:07 GMT
ENV TELEGRAF_VERSION=1.38.4
# Thu, 11 Jun 2026 02:38:07 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Thu, 11 Jun 2026 02:38:07 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Thu, 11 Jun 2026 02:38:07 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Jun 2026 02:38:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jun 2026 02:38:07 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:c847f328095fb083f4a22895b90fe4226efa6458ac57362b64b6e5d99da9e4a3`  
		Last Modified: Wed, 10 Jun 2026 23:39:28 GMT  
		Size: 48.4 MB (48389016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f511b4c80a6e453785fbcd573c1bf1cb986c4e8d43ed4500ad1ac9a4719762b`  
		Last Modified: Thu, 11 Jun 2026 00:43:56 GMT  
		Size: 23.6 MB (23613296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:626a0843d1e475e7995383906770115761545199c6fc7f909e2a4f54e72abb2e`  
		Last Modified: Thu, 11 Jun 2026 02:38:25 GMT  
		Size: 18.9 MB (18885765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faba5a110e88bbe89235aee61fa6243ce139bfe94fbb60171dfb8a727259c4e5`  
		Last Modified: Thu, 11 Jun 2026 02:38:24 GMT  
		Size: 5.1 KB (5069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b323b177bf29334b8a45dcbb48b067ea8e49a135d49202e14d71a6d36a9b62aa`  
		Last Modified: Thu, 11 Jun 2026 02:38:26 GMT  
		Size: 74.5 MB (74476780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b0d336a7afeb32aa18b00151cd3388b2adbe3af11c7c8118cb754301934690d`  
		Last Modified: Thu, 11 Jun 2026 02:38:23 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.38.4` - unknown; unknown

```console
$ docker pull telegraf@sha256:aa21293244a6a0237dc53c8db2c715625b2e2979d57ac806913af342622ea778
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6689512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcb4b1f9007724aa4c9633effe6f52a0a58d2d131083a7f46168406f45dd2596`

```dockerfile
```

-	Layers:
	-	`sha256:78d4f833c2cf1b0c86bbab218f72d895d263baf4171e07a8cace9102acc2e602`  
		Last Modified: Thu, 11 Jun 2026 02:38:24 GMT  
		Size: 6.7 MB (6674975 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be60d940b566988b121930e240c5d5d8f1ae454ff3f232191022d6f7a4447dda`  
		Last Modified: Thu, 11 Jun 2026 02:38:24 GMT  
		Size: 14.5 KB (14537 bytes)  
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

## `telegraf:1.39`

```console
$ docker pull telegraf@sha256:9768f82ebf8bde6da0d61ba220c00161750740c3e322b507a5982b89bbfca99a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.39` - linux; amd64

```console
$ docker pull telegraf@sha256:3fc4238e808b2f478fc4b75ca20ad1591d7d8e4d00cd24c1849e06b0d7bb476d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.3 MB (175318286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cba2b198a419da73a31ba9e67d57290f8dcb68596fd0e81b78a75f63fddcc33f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:42:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 02:38:05 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 02:38:06 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Thu, 11 Jun 2026 02:38:10 GMT
ENV TELEGRAF_VERSION=1.39.0
# Thu, 11 Jun 2026 02:38:10 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Thu, 11 Jun 2026 02:38:10 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Thu, 11 Jun 2026 02:38:10 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Jun 2026 02:38:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jun 2026 02:38:10 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:01cedcff86f879d042805360ecba268802bec3d8201484ff3ec54f4250a2d3b7`  
		Last Modified: Wed, 10 Jun 2026 23:39:39 GMT  
		Size: 48.5 MB (48502042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4da31edd9efdb812e66d13819903973ea6b188d2e7358547676d33d1e3f706f2`  
		Last Modified: Thu, 11 Jun 2026 00:42:23 GMT  
		Size: 24.0 MB (24044000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7e155aa599b08cfc50d0f771f6c9e59a26cc3db1ee8f23d96c752045946ebcb`  
		Last Modified: Thu, 11 Jun 2026 02:38:29 GMT  
		Size: 18.9 MB (18944395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7f40305f2528a0074d7b3653af61e0dabf428fc001c4f0ef4f673d8d00dcbf8`  
		Last Modified: Thu, 11 Jun 2026 02:38:28 GMT  
		Size: 5.1 KB (5070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10fe74ec8be4e76e3eeeaa5ce9e622028481c0ed8d57aa6be447a3bde9539cf2`  
		Last Modified: Thu, 11 Jun 2026 02:38:31 GMT  
		Size: 83.8 MB (83822154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b36e074ab3ae61fe91559fea6042fff3bf206c18d93dd5a8b48c3a2388b2217`  
		Last Modified: Thu, 11 Jun 2026 02:38:28 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.39` - unknown; unknown

```console
$ docker pull telegraf@sha256:cd95848d5b140458c457b030ae76b9f962124f03bd360f55355f8ceccf38ab4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6687666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97ab420b7b4f8d15cba4ec1c2fb5a15733b264a6bcff0b85758504baf20d4c9d`

```dockerfile
```

-	Layers:
	-	`sha256:beef73a3089eafad7c4e32aed5edcf8380afa58610e43ecdf90a802ad49c1ba3`  
		Last Modified: Thu, 11 Jun 2026 02:38:29 GMT  
		Size: 6.7 MB (6672937 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b4cf003c03def45113a2bed2a8208f28f824177d46f372be4ded5526487f05a`  
		Last Modified: Thu, 11 Jun 2026 02:38:28 GMT  
		Size: 14.7 KB (14729 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.39` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:a946077d5018834e7983558f2a0a57f000252e11c0900f6bbade39b5a9326138
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.6 MB (161564792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0331c7b809a0c64ebcdcd52942423b4c1a6a408fc06433191d4e7b01807fcbd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 01:23:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 03:12:51 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 03:12:51 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Thu, 11 Jun 2026 03:12:57 GMT
ENV TELEGRAF_VERSION=1.39.0
# Thu, 11 Jun 2026 03:12:57 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Thu, 11 Jun 2026 03:12:57 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Thu, 11 Jun 2026 03:12:57 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Jun 2026 03:12:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jun 2026 03:12:57 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:c0213091aa87e4be7caed06dd364889c231dab5ba50fa1e54365eb7a94390261`  
		Last Modified: Wed, 10 Jun 2026 23:39:46 GMT  
		Size: 44.2 MB (44208065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d14356188705148a948907491c78974967557826c6ca92209148b3bc14f0f659`  
		Last Modified: Thu, 11 Jun 2026 01:23:38 GMT  
		Size: 21.9 MB (21949873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80941b0bdd88cb14fce09cd860981822c6590d738dd60fa2b425ad1a2429293d`  
		Last Modified: Thu, 11 Jun 2026 03:13:15 GMT  
		Size: 17.7 MB (17699817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f9b6c1fafb4b14de088e98dca0de3494f44b322e5b325eafc52eec89ddc5148`  
		Last Modified: Thu, 11 Jun 2026 03:13:14 GMT  
		Size: 5.1 KB (5056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9141dff73825ba6ee195b24a91285533c2cad6d58c0626cfcbd901eafd72b97`  
		Last Modified: Thu, 11 Jun 2026 03:13:17 GMT  
		Size: 77.7 MB (77701357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4875f91dfac36b7631c83f84ec7dff018503073edc88c769230e2fa1c6e5467`  
		Last Modified: Thu, 11 Jun 2026 03:13:13 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.39` - unknown; unknown

```console
$ docker pull telegraf@sha256:0487b9099eff11da70a8440c42beb10e2ba249c22ad6fb3a433944557e112fb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6682368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff9095f5ab3dc9b58e92061b8b9f1af712195195681919d0b8dd34df8ce73f59`

```dockerfile
```

-	Layers:
	-	`sha256:883ba0a7487f08ce93931197cc951f75d91ed7302d25f321b397295cb37fa629`  
		Last Modified: Thu, 11 Jun 2026 03:13:14 GMT  
		Size: 6.7 MB (6667542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6087deec867efbcf573afe33841bba228436e08b33510f1eda0178b058b8dc24`  
		Last Modified: Thu, 11 Jun 2026 03:13:14 GMT  
		Size: 14.8 KB (14826 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.39` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:ef03e3f7e60c80c324d644e62848925dabd58fde52b7bede56a9df33c4138150
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.6 MB (165642228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e803603c69c0fec78a586496a6ecc0819c8e3280219e4cfa6a92181c5958afae`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:43:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 02:37:33 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 02:37:34 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Thu, 11 Jun 2026 02:38:09 GMT
ENV TELEGRAF_VERSION=1.39.0
# Thu, 11 Jun 2026 02:38:09 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Thu, 11 Jun 2026 02:38:09 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Thu, 11 Jun 2026 02:38:09 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Jun 2026 02:38:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jun 2026 02:38:09 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:c847f328095fb083f4a22895b90fe4226efa6458ac57362b64b6e5d99da9e4a3`  
		Last Modified: Wed, 10 Jun 2026 23:39:28 GMT  
		Size: 48.4 MB (48389016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f511b4c80a6e453785fbcd573c1bf1cb986c4e8d43ed4500ad1ac9a4719762b`  
		Last Modified: Thu, 11 Jun 2026 00:43:56 GMT  
		Size: 23.6 MB (23613296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c190ef3f5f7acc6d44552bd3c4080c3a0fe6a2b8c594caff252a7a6d1b89a523`  
		Last Modified: Thu, 11 Jun 2026 02:37:55 GMT  
		Size: 18.9 MB (18885883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f24b9de6d86f6333b5aa1983c1dd0a8f6873a5a2904c22c512d14cbd25b77c`  
		Last Modified: Thu, 11 Jun 2026 02:37:55 GMT  
		Size: 5.1 KB (5071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91ae3a233fa6f07584fe61e4bb99d85f21204734e79571844baae03bfab53654`  
		Last Modified: Thu, 11 Jun 2026 02:38:28 GMT  
		Size: 74.7 MB (74748337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a94bad00e15d9a51745fd11cdda66763215b62892a220dd25d0c9c2daee0120c`  
		Last Modified: Thu, 11 Jun 2026 02:38:25 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.39` - unknown; unknown

```console
$ docker pull telegraf@sha256:d3da96f26730a480bde408c681552dc264b705778d2808b7f4cac2b0012caaf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6688475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd605b571f78407a533a0a4ce989a44613ce9da57de9dbe252d1d75730603ec6`

```dockerfile
```

-	Layers:
	-	`sha256:325a4ab33a42d976c41276df893b8a6fac1ffb11c32e74d323a73300ffcab816`  
		Last Modified: Thu, 11 Jun 2026 02:38:25 GMT  
		Size: 6.7 MB (6673625 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:edc92bac93d6fe676f799a5b64caa5c8dd2703a51b4e1427264c7e693404085e`  
		Last Modified: Thu, 11 Jun 2026 02:38:25 GMT  
		Size: 14.8 KB (14850 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.39-alpine`

```console
$ docker pull telegraf@sha256:e5226af100b22b26b628c2f25268985541b8e04367ca1392bd704b0d488f6b91
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.39-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:24dfd35ff04cbaf51ee6ae2cb4adbcd0685fab04ed871d8068efefaa18b69667
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.1 MB (90091126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52c3d009e134e78926811768785b2379d2553300e8a2c76c1b880293bd3c0077`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Mon, 08 Jun 2026 19:33:28 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 08 Jun 2026 19:33:29 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 08 Jun 2026 19:33:35 GMT
ENV TELEGRAF_VERSION=1.39.0
# Mon, 08 Jun 2026 19:33:35 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 08 Jun 2026 19:33:35 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 08 Jun 2026 19:33:35 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 08 Jun 2026 19:33:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Jun 2026 19:33:35 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b78cbe9dd99262d6d456db1e27c3aa45b6b06c9845c5b98cccf065f4dbd0485f`  
		Last Modified: Mon, 08 Jun 2026 19:33:51 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4e98f55428d3403b7d4915048651510e60b3841891394ea326d6f5238d9cdad`  
		Last Modified: Mon, 08 Jun 2026 19:33:51 GMT  
		Size: 2.6 MB (2615476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1eed0b000d88926bf46c7eb3555919d1b39dbab8bf2f6aa03472f49b71f917a`  
		Last Modified: Mon, 08 Jun 2026 19:33:54 GMT  
		Size: 83.6 MB (83610562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e5730870d1e61bd804af545e88b2253b12266e7cb5265ef8fe4981945566b78`  
		Last Modified: Mon, 08 Jun 2026 19:33:51 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.39-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:4fcb5ccf45efe63c761bbd304ac29be7c49c47e184e2fcba71dfe83bb0d4e9e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1172981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1c0ef1b3412075ab8b75e101db7e907aee9894470f0964ac4d36214b42e7fbe`

```dockerfile
```

-	Layers:
	-	`sha256:dd82967f130f0f1255f3c9786b6d5607463a7133177fddd02d2d03f11f37ed0f`  
		Last Modified: Mon, 08 Jun 2026 19:33:51 GMT  
		Size: 1.2 MB (1157761 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d572b7be776dbddbbb1c26badb01d9680a53ced76feb8abf272df390138831d7`  
		Last Modified: Mon, 08 Jun 2026 19:33:51 GMT  
		Size: 15.2 KB (15220 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.39-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:6b66eb0080cbbf00b42b11818a220c506a9850b0c298a0fbbd50d7384a5df896
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.4 MB (81405285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e90f2baaf68b2eba385baeab8785b6ad48c02dfa2dba818b9a6c81a9416dfa1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Mon, 08 Jun 2026 19:33:35 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 08 Jun 2026 19:33:35 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 08 Jun 2026 19:33:41 GMT
ENV TELEGRAF_VERSION=1.39.0
# Mon, 08 Jun 2026 19:33:41 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 08 Jun 2026 19:33:41 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 08 Jun 2026 19:33:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 08 Jun 2026 19:33:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Jun 2026 19:33:42 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6ca5dabf7783a6f9f9ce035e047cef313b5969395dd331a6ae02b4888644baf`  
		Last Modified: Mon, 08 Jun 2026 19:33:56 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f722e30210b3ae00ddc7f9a8e1903197f494d3197297bc2fbf0201008bc826`  
		Last Modified: Mon, 08 Jun 2026 19:33:56 GMT  
		Size: 2.7 MB (2663404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75fa91218e8453a0f48f968d4e79ec2915ff4e94f9ddd205c806928bcf6401fd`  
		Last Modified: Mon, 08 Jun 2026 19:33:58 GMT  
		Size: 74.5 MB (74541112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca7bb573a3266c7638c7802e066265f0c51f4d1c3b1a8273fc32812d65618ab`  
		Last Modified: Mon, 08 Jun 2026 19:33:55 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.39-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:95293b4a78213f540b3e48a94125ce0c51a8f02593c5b9344631a30200610346
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1168092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a654bf0957227d01a365840e084285d2e1ff416172a723b453027d8bd6cc77b6`

```dockerfile
```

-	Layers:
	-	`sha256:8ad6e19bd77984338905bc7bb0cff26357a4f37f952d6edf88e00b900cc3c4e0`  
		Last Modified: Mon, 08 Jun 2026 19:33:56 GMT  
		Size: 1.2 MB (1152750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dfff3047d82a9d84c31708e992a7106776945fa93bda13ba3af793b751c0a4f2`  
		Last Modified: Mon, 08 Jun 2026 19:33:55 GMT  
		Size: 15.3 KB (15342 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.39.0`

```console
$ docker pull telegraf@sha256:9768f82ebf8bde6da0d61ba220c00161750740c3e322b507a5982b89bbfca99a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.39.0` - linux; amd64

```console
$ docker pull telegraf@sha256:3fc4238e808b2f478fc4b75ca20ad1591d7d8e4d00cd24c1849e06b0d7bb476d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.3 MB (175318286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cba2b198a419da73a31ba9e67d57290f8dcb68596fd0e81b78a75f63fddcc33f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:42:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 02:38:05 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 02:38:06 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Thu, 11 Jun 2026 02:38:10 GMT
ENV TELEGRAF_VERSION=1.39.0
# Thu, 11 Jun 2026 02:38:10 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Thu, 11 Jun 2026 02:38:10 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Thu, 11 Jun 2026 02:38:10 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Jun 2026 02:38:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jun 2026 02:38:10 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:01cedcff86f879d042805360ecba268802bec3d8201484ff3ec54f4250a2d3b7`  
		Last Modified: Wed, 10 Jun 2026 23:39:39 GMT  
		Size: 48.5 MB (48502042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4da31edd9efdb812e66d13819903973ea6b188d2e7358547676d33d1e3f706f2`  
		Last Modified: Thu, 11 Jun 2026 00:42:23 GMT  
		Size: 24.0 MB (24044000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7e155aa599b08cfc50d0f771f6c9e59a26cc3db1ee8f23d96c752045946ebcb`  
		Last Modified: Thu, 11 Jun 2026 02:38:29 GMT  
		Size: 18.9 MB (18944395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7f40305f2528a0074d7b3653af61e0dabf428fc001c4f0ef4f673d8d00dcbf8`  
		Last Modified: Thu, 11 Jun 2026 02:38:28 GMT  
		Size: 5.1 KB (5070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10fe74ec8be4e76e3eeeaa5ce9e622028481c0ed8d57aa6be447a3bde9539cf2`  
		Last Modified: Thu, 11 Jun 2026 02:38:31 GMT  
		Size: 83.8 MB (83822154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b36e074ab3ae61fe91559fea6042fff3bf206c18d93dd5a8b48c3a2388b2217`  
		Last Modified: Thu, 11 Jun 2026 02:38:28 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.39.0` - unknown; unknown

```console
$ docker pull telegraf@sha256:cd95848d5b140458c457b030ae76b9f962124f03bd360f55355f8ceccf38ab4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6687666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97ab420b7b4f8d15cba4ec1c2fb5a15733b264a6bcff0b85758504baf20d4c9d`

```dockerfile
```

-	Layers:
	-	`sha256:beef73a3089eafad7c4e32aed5edcf8380afa58610e43ecdf90a802ad49c1ba3`  
		Last Modified: Thu, 11 Jun 2026 02:38:29 GMT  
		Size: 6.7 MB (6672937 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b4cf003c03def45113a2bed2a8208f28f824177d46f372be4ded5526487f05a`  
		Last Modified: Thu, 11 Jun 2026 02:38:28 GMT  
		Size: 14.7 KB (14729 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.39.0` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:a946077d5018834e7983558f2a0a57f000252e11c0900f6bbade39b5a9326138
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.6 MB (161564792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0331c7b809a0c64ebcdcd52942423b4c1a6a408fc06433191d4e7b01807fcbd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 01:23:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 03:12:51 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 03:12:51 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Thu, 11 Jun 2026 03:12:57 GMT
ENV TELEGRAF_VERSION=1.39.0
# Thu, 11 Jun 2026 03:12:57 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Thu, 11 Jun 2026 03:12:57 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Thu, 11 Jun 2026 03:12:57 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Jun 2026 03:12:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jun 2026 03:12:57 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:c0213091aa87e4be7caed06dd364889c231dab5ba50fa1e54365eb7a94390261`  
		Last Modified: Wed, 10 Jun 2026 23:39:46 GMT  
		Size: 44.2 MB (44208065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d14356188705148a948907491c78974967557826c6ca92209148b3bc14f0f659`  
		Last Modified: Thu, 11 Jun 2026 01:23:38 GMT  
		Size: 21.9 MB (21949873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80941b0bdd88cb14fce09cd860981822c6590d738dd60fa2b425ad1a2429293d`  
		Last Modified: Thu, 11 Jun 2026 03:13:15 GMT  
		Size: 17.7 MB (17699817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f9b6c1fafb4b14de088e98dca0de3494f44b322e5b325eafc52eec89ddc5148`  
		Last Modified: Thu, 11 Jun 2026 03:13:14 GMT  
		Size: 5.1 KB (5056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9141dff73825ba6ee195b24a91285533c2cad6d58c0626cfcbd901eafd72b97`  
		Last Modified: Thu, 11 Jun 2026 03:13:17 GMT  
		Size: 77.7 MB (77701357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4875f91dfac36b7631c83f84ec7dff018503073edc88c769230e2fa1c6e5467`  
		Last Modified: Thu, 11 Jun 2026 03:13:13 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.39.0` - unknown; unknown

```console
$ docker pull telegraf@sha256:0487b9099eff11da70a8440c42beb10e2ba249c22ad6fb3a433944557e112fb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6682368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff9095f5ab3dc9b58e92061b8b9f1af712195195681919d0b8dd34df8ce73f59`

```dockerfile
```

-	Layers:
	-	`sha256:883ba0a7487f08ce93931197cc951f75d91ed7302d25f321b397295cb37fa629`  
		Last Modified: Thu, 11 Jun 2026 03:13:14 GMT  
		Size: 6.7 MB (6667542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6087deec867efbcf573afe33841bba228436e08b33510f1eda0178b058b8dc24`  
		Last Modified: Thu, 11 Jun 2026 03:13:14 GMT  
		Size: 14.8 KB (14826 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.39.0` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:ef03e3f7e60c80c324d644e62848925dabd58fde52b7bede56a9df33c4138150
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.6 MB (165642228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e803603c69c0fec78a586496a6ecc0819c8e3280219e4cfa6a92181c5958afae`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:43:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 02:37:33 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 02:37:34 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Thu, 11 Jun 2026 02:38:09 GMT
ENV TELEGRAF_VERSION=1.39.0
# Thu, 11 Jun 2026 02:38:09 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Thu, 11 Jun 2026 02:38:09 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Thu, 11 Jun 2026 02:38:09 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Jun 2026 02:38:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jun 2026 02:38:09 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:c847f328095fb083f4a22895b90fe4226efa6458ac57362b64b6e5d99da9e4a3`  
		Last Modified: Wed, 10 Jun 2026 23:39:28 GMT  
		Size: 48.4 MB (48389016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f511b4c80a6e453785fbcd573c1bf1cb986c4e8d43ed4500ad1ac9a4719762b`  
		Last Modified: Thu, 11 Jun 2026 00:43:56 GMT  
		Size: 23.6 MB (23613296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c190ef3f5f7acc6d44552bd3c4080c3a0fe6a2b8c594caff252a7a6d1b89a523`  
		Last Modified: Thu, 11 Jun 2026 02:37:55 GMT  
		Size: 18.9 MB (18885883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f24b9de6d86f6333b5aa1983c1dd0a8f6873a5a2904c22c512d14cbd25b77c`  
		Last Modified: Thu, 11 Jun 2026 02:37:55 GMT  
		Size: 5.1 KB (5071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91ae3a233fa6f07584fe61e4bb99d85f21204734e79571844baae03bfab53654`  
		Last Modified: Thu, 11 Jun 2026 02:38:28 GMT  
		Size: 74.7 MB (74748337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a94bad00e15d9a51745fd11cdda66763215b62892a220dd25d0c9c2daee0120c`  
		Last Modified: Thu, 11 Jun 2026 02:38:25 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.39.0` - unknown; unknown

```console
$ docker pull telegraf@sha256:d3da96f26730a480bde408c681552dc264b705778d2808b7f4cac2b0012caaf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6688475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd605b571f78407a533a0a4ce989a44613ce9da57de9dbe252d1d75730603ec6`

```dockerfile
```

-	Layers:
	-	`sha256:325a4ab33a42d976c41276df893b8a6fac1ffb11c32e74d323a73300ffcab816`  
		Last Modified: Thu, 11 Jun 2026 02:38:25 GMT  
		Size: 6.7 MB (6673625 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:edc92bac93d6fe676f799a5b64caa5c8dd2703a51b4e1427264c7e693404085e`  
		Last Modified: Thu, 11 Jun 2026 02:38:25 GMT  
		Size: 14.8 KB (14850 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.39.0-alpine`

```console
$ docker pull telegraf@sha256:e5226af100b22b26b628c2f25268985541b8e04367ca1392bd704b0d488f6b91
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.39.0-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:24dfd35ff04cbaf51ee6ae2cb4adbcd0685fab04ed871d8068efefaa18b69667
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.1 MB (90091126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52c3d009e134e78926811768785b2379d2553300e8a2c76c1b880293bd3c0077`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Mon, 08 Jun 2026 19:33:28 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 08 Jun 2026 19:33:29 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 08 Jun 2026 19:33:35 GMT
ENV TELEGRAF_VERSION=1.39.0
# Mon, 08 Jun 2026 19:33:35 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 08 Jun 2026 19:33:35 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 08 Jun 2026 19:33:35 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 08 Jun 2026 19:33:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Jun 2026 19:33:35 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b78cbe9dd99262d6d456db1e27c3aa45b6b06c9845c5b98cccf065f4dbd0485f`  
		Last Modified: Mon, 08 Jun 2026 19:33:51 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4e98f55428d3403b7d4915048651510e60b3841891394ea326d6f5238d9cdad`  
		Last Modified: Mon, 08 Jun 2026 19:33:51 GMT  
		Size: 2.6 MB (2615476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1eed0b000d88926bf46c7eb3555919d1b39dbab8bf2f6aa03472f49b71f917a`  
		Last Modified: Mon, 08 Jun 2026 19:33:54 GMT  
		Size: 83.6 MB (83610562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e5730870d1e61bd804af545e88b2253b12266e7cb5265ef8fe4981945566b78`  
		Last Modified: Mon, 08 Jun 2026 19:33:51 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.39.0-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:4fcb5ccf45efe63c761bbd304ac29be7c49c47e184e2fcba71dfe83bb0d4e9e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1172981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1c0ef1b3412075ab8b75e101db7e907aee9894470f0964ac4d36214b42e7fbe`

```dockerfile
```

-	Layers:
	-	`sha256:dd82967f130f0f1255f3c9786b6d5607463a7133177fddd02d2d03f11f37ed0f`  
		Last Modified: Mon, 08 Jun 2026 19:33:51 GMT  
		Size: 1.2 MB (1157761 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d572b7be776dbddbbb1c26badb01d9680a53ced76feb8abf272df390138831d7`  
		Last Modified: Mon, 08 Jun 2026 19:33:51 GMT  
		Size: 15.2 KB (15220 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.39.0-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:6b66eb0080cbbf00b42b11818a220c506a9850b0c298a0fbbd50d7384a5df896
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.4 MB (81405285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e90f2baaf68b2eba385baeab8785b6ad48c02dfa2dba818b9a6c81a9416dfa1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Mon, 08 Jun 2026 19:33:35 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 08 Jun 2026 19:33:35 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 08 Jun 2026 19:33:41 GMT
ENV TELEGRAF_VERSION=1.39.0
# Mon, 08 Jun 2026 19:33:41 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 08 Jun 2026 19:33:41 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 08 Jun 2026 19:33:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 08 Jun 2026 19:33:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Jun 2026 19:33:42 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6ca5dabf7783a6f9f9ce035e047cef313b5969395dd331a6ae02b4888644baf`  
		Last Modified: Mon, 08 Jun 2026 19:33:56 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f722e30210b3ae00ddc7f9a8e1903197f494d3197297bc2fbf0201008bc826`  
		Last Modified: Mon, 08 Jun 2026 19:33:56 GMT  
		Size: 2.7 MB (2663404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75fa91218e8453a0f48f968d4e79ec2915ff4e94f9ddd205c806928bcf6401fd`  
		Last Modified: Mon, 08 Jun 2026 19:33:58 GMT  
		Size: 74.5 MB (74541112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca7bb573a3266c7638c7802e066265f0c51f4d1c3b1a8273fc32812d65618ab`  
		Last Modified: Mon, 08 Jun 2026 19:33:55 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.39.0-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:95293b4a78213f540b3e48a94125ce0c51a8f02593c5b9344631a30200610346
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1168092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a654bf0957227d01a365840e084285d2e1ff416172a723b453027d8bd6cc77b6`

```dockerfile
```

-	Layers:
	-	`sha256:8ad6e19bd77984338905bc7bb0cff26357a4f37f952d6edf88e00b900cc3c4e0`  
		Last Modified: Mon, 08 Jun 2026 19:33:56 GMT  
		Size: 1.2 MB (1152750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dfff3047d82a9d84c31708e992a7106776945fa93bda13ba3af793b751c0a4f2`  
		Last Modified: Mon, 08 Jun 2026 19:33:55 GMT  
		Size: 15.3 KB (15342 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:alpine`

```console
$ docker pull telegraf@sha256:e5226af100b22b26b628c2f25268985541b8e04367ca1392bd704b0d488f6b91
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:24dfd35ff04cbaf51ee6ae2cb4adbcd0685fab04ed871d8068efefaa18b69667
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.1 MB (90091126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52c3d009e134e78926811768785b2379d2553300e8a2c76c1b880293bd3c0077`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Mon, 08 Jun 2026 19:33:28 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 08 Jun 2026 19:33:29 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 08 Jun 2026 19:33:35 GMT
ENV TELEGRAF_VERSION=1.39.0
# Mon, 08 Jun 2026 19:33:35 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 08 Jun 2026 19:33:35 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 08 Jun 2026 19:33:35 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 08 Jun 2026 19:33:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Jun 2026 19:33:35 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b78cbe9dd99262d6d456db1e27c3aa45b6b06c9845c5b98cccf065f4dbd0485f`  
		Last Modified: Mon, 08 Jun 2026 19:33:51 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4e98f55428d3403b7d4915048651510e60b3841891394ea326d6f5238d9cdad`  
		Last Modified: Mon, 08 Jun 2026 19:33:51 GMT  
		Size: 2.6 MB (2615476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1eed0b000d88926bf46c7eb3555919d1b39dbab8bf2f6aa03472f49b71f917a`  
		Last Modified: Mon, 08 Jun 2026 19:33:54 GMT  
		Size: 83.6 MB (83610562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e5730870d1e61bd804af545e88b2253b12266e7cb5265ef8fe4981945566b78`  
		Last Modified: Mon, 08 Jun 2026 19:33:51 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:4fcb5ccf45efe63c761bbd304ac29be7c49c47e184e2fcba71dfe83bb0d4e9e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1172981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1c0ef1b3412075ab8b75e101db7e907aee9894470f0964ac4d36214b42e7fbe`

```dockerfile
```

-	Layers:
	-	`sha256:dd82967f130f0f1255f3c9786b6d5607463a7133177fddd02d2d03f11f37ed0f`  
		Last Modified: Mon, 08 Jun 2026 19:33:51 GMT  
		Size: 1.2 MB (1157761 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d572b7be776dbddbbb1c26badb01d9680a53ced76feb8abf272df390138831d7`  
		Last Modified: Mon, 08 Jun 2026 19:33:51 GMT  
		Size: 15.2 KB (15220 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:6b66eb0080cbbf00b42b11818a220c506a9850b0c298a0fbbd50d7384a5df896
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.4 MB (81405285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e90f2baaf68b2eba385baeab8785b6ad48c02dfa2dba818b9a6c81a9416dfa1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Mon, 08 Jun 2026 19:33:35 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 08 Jun 2026 19:33:35 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 08 Jun 2026 19:33:41 GMT
ENV TELEGRAF_VERSION=1.39.0
# Mon, 08 Jun 2026 19:33:41 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 08 Jun 2026 19:33:41 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 08 Jun 2026 19:33:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 08 Jun 2026 19:33:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Jun 2026 19:33:42 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6ca5dabf7783a6f9f9ce035e047cef313b5969395dd331a6ae02b4888644baf`  
		Last Modified: Mon, 08 Jun 2026 19:33:56 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f722e30210b3ae00ddc7f9a8e1903197f494d3197297bc2fbf0201008bc826`  
		Last Modified: Mon, 08 Jun 2026 19:33:56 GMT  
		Size: 2.7 MB (2663404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75fa91218e8453a0f48f968d4e79ec2915ff4e94f9ddd205c806928bcf6401fd`  
		Last Modified: Mon, 08 Jun 2026 19:33:58 GMT  
		Size: 74.5 MB (74541112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca7bb573a3266c7638c7802e066265f0c51f4d1c3b1a8273fc32812d65618ab`  
		Last Modified: Mon, 08 Jun 2026 19:33:55 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:95293b4a78213f540b3e48a94125ce0c51a8f02593c5b9344631a30200610346
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1168092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a654bf0957227d01a365840e084285d2e1ff416172a723b453027d8bd6cc77b6`

```dockerfile
```

-	Layers:
	-	`sha256:8ad6e19bd77984338905bc7bb0cff26357a4f37f952d6edf88e00b900cc3c4e0`  
		Last Modified: Mon, 08 Jun 2026 19:33:56 GMT  
		Size: 1.2 MB (1152750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dfff3047d82a9d84c31708e992a7106776945fa93bda13ba3af793b751c0a4f2`  
		Last Modified: Mon, 08 Jun 2026 19:33:55 GMT  
		Size: 15.3 KB (15342 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:latest`

```console
$ docker pull telegraf@sha256:9768f82ebf8bde6da0d61ba220c00161750740c3e322b507a5982b89bbfca99a
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
$ docker pull telegraf@sha256:3fc4238e808b2f478fc4b75ca20ad1591d7d8e4d00cd24c1849e06b0d7bb476d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.3 MB (175318286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cba2b198a419da73a31ba9e67d57290f8dcb68596fd0e81b78a75f63fddcc33f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:42:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 02:38:05 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 02:38:06 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Thu, 11 Jun 2026 02:38:10 GMT
ENV TELEGRAF_VERSION=1.39.0
# Thu, 11 Jun 2026 02:38:10 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Thu, 11 Jun 2026 02:38:10 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Thu, 11 Jun 2026 02:38:10 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Jun 2026 02:38:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jun 2026 02:38:10 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:01cedcff86f879d042805360ecba268802bec3d8201484ff3ec54f4250a2d3b7`  
		Last Modified: Wed, 10 Jun 2026 23:39:39 GMT  
		Size: 48.5 MB (48502042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4da31edd9efdb812e66d13819903973ea6b188d2e7358547676d33d1e3f706f2`  
		Last Modified: Thu, 11 Jun 2026 00:42:23 GMT  
		Size: 24.0 MB (24044000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7e155aa599b08cfc50d0f771f6c9e59a26cc3db1ee8f23d96c752045946ebcb`  
		Last Modified: Thu, 11 Jun 2026 02:38:29 GMT  
		Size: 18.9 MB (18944395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7f40305f2528a0074d7b3653af61e0dabf428fc001c4f0ef4f673d8d00dcbf8`  
		Last Modified: Thu, 11 Jun 2026 02:38:28 GMT  
		Size: 5.1 KB (5070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10fe74ec8be4e76e3eeeaa5ce9e622028481c0ed8d57aa6be447a3bde9539cf2`  
		Last Modified: Thu, 11 Jun 2026 02:38:31 GMT  
		Size: 83.8 MB (83822154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b36e074ab3ae61fe91559fea6042fff3bf206c18d93dd5a8b48c3a2388b2217`  
		Last Modified: Thu, 11 Jun 2026 02:38:28 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:cd95848d5b140458c457b030ae76b9f962124f03bd360f55355f8ceccf38ab4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6687666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97ab420b7b4f8d15cba4ec1c2fb5a15733b264a6bcff0b85758504baf20d4c9d`

```dockerfile
```

-	Layers:
	-	`sha256:beef73a3089eafad7c4e32aed5edcf8380afa58610e43ecdf90a802ad49c1ba3`  
		Last Modified: Thu, 11 Jun 2026 02:38:29 GMT  
		Size: 6.7 MB (6672937 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b4cf003c03def45113a2bed2a8208f28f824177d46f372be4ded5526487f05a`  
		Last Modified: Thu, 11 Jun 2026 02:38:28 GMT  
		Size: 14.7 KB (14729 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:a946077d5018834e7983558f2a0a57f000252e11c0900f6bbade39b5a9326138
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.6 MB (161564792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0331c7b809a0c64ebcdcd52942423b4c1a6a408fc06433191d4e7b01807fcbd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 01:23:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 03:12:51 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 03:12:51 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Thu, 11 Jun 2026 03:12:57 GMT
ENV TELEGRAF_VERSION=1.39.0
# Thu, 11 Jun 2026 03:12:57 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Thu, 11 Jun 2026 03:12:57 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Thu, 11 Jun 2026 03:12:57 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Jun 2026 03:12:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jun 2026 03:12:57 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:c0213091aa87e4be7caed06dd364889c231dab5ba50fa1e54365eb7a94390261`  
		Last Modified: Wed, 10 Jun 2026 23:39:46 GMT  
		Size: 44.2 MB (44208065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d14356188705148a948907491c78974967557826c6ca92209148b3bc14f0f659`  
		Last Modified: Thu, 11 Jun 2026 01:23:38 GMT  
		Size: 21.9 MB (21949873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80941b0bdd88cb14fce09cd860981822c6590d738dd60fa2b425ad1a2429293d`  
		Last Modified: Thu, 11 Jun 2026 03:13:15 GMT  
		Size: 17.7 MB (17699817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f9b6c1fafb4b14de088e98dca0de3494f44b322e5b325eafc52eec89ddc5148`  
		Last Modified: Thu, 11 Jun 2026 03:13:14 GMT  
		Size: 5.1 KB (5056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9141dff73825ba6ee195b24a91285533c2cad6d58c0626cfcbd901eafd72b97`  
		Last Modified: Thu, 11 Jun 2026 03:13:17 GMT  
		Size: 77.7 MB (77701357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4875f91dfac36b7631c83f84ec7dff018503073edc88c769230e2fa1c6e5467`  
		Last Modified: Thu, 11 Jun 2026 03:13:13 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:0487b9099eff11da70a8440c42beb10e2ba249c22ad6fb3a433944557e112fb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6682368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff9095f5ab3dc9b58e92061b8b9f1af712195195681919d0b8dd34df8ce73f59`

```dockerfile
```

-	Layers:
	-	`sha256:883ba0a7487f08ce93931197cc951f75d91ed7302d25f321b397295cb37fa629`  
		Last Modified: Thu, 11 Jun 2026 03:13:14 GMT  
		Size: 6.7 MB (6667542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6087deec867efbcf573afe33841bba228436e08b33510f1eda0178b058b8dc24`  
		Last Modified: Thu, 11 Jun 2026 03:13:14 GMT  
		Size: 14.8 KB (14826 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:ef03e3f7e60c80c324d644e62848925dabd58fde52b7bede56a9df33c4138150
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.6 MB (165642228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e803603c69c0fec78a586496a6ecc0819c8e3280219e4cfa6a92181c5958afae`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:43:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 02:37:33 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 02:37:34 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Thu, 11 Jun 2026 02:38:09 GMT
ENV TELEGRAF_VERSION=1.39.0
# Thu, 11 Jun 2026 02:38:09 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Thu, 11 Jun 2026 02:38:09 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Thu, 11 Jun 2026 02:38:09 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Jun 2026 02:38:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jun 2026 02:38:09 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:c847f328095fb083f4a22895b90fe4226efa6458ac57362b64b6e5d99da9e4a3`  
		Last Modified: Wed, 10 Jun 2026 23:39:28 GMT  
		Size: 48.4 MB (48389016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f511b4c80a6e453785fbcd573c1bf1cb986c4e8d43ed4500ad1ac9a4719762b`  
		Last Modified: Thu, 11 Jun 2026 00:43:56 GMT  
		Size: 23.6 MB (23613296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c190ef3f5f7acc6d44552bd3c4080c3a0fe6a2b8c594caff252a7a6d1b89a523`  
		Last Modified: Thu, 11 Jun 2026 02:37:55 GMT  
		Size: 18.9 MB (18885883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f24b9de6d86f6333b5aa1983c1dd0a8f6873a5a2904c22c512d14cbd25b77c`  
		Last Modified: Thu, 11 Jun 2026 02:37:55 GMT  
		Size: 5.1 KB (5071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91ae3a233fa6f07584fe61e4bb99d85f21204734e79571844baae03bfab53654`  
		Last Modified: Thu, 11 Jun 2026 02:38:28 GMT  
		Size: 74.7 MB (74748337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a94bad00e15d9a51745fd11cdda66763215b62892a220dd25d0c9c2daee0120c`  
		Last Modified: Thu, 11 Jun 2026 02:38:25 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:d3da96f26730a480bde408c681552dc264b705778d2808b7f4cac2b0012caaf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6688475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd605b571f78407a533a0a4ce989a44613ce9da57de9dbe252d1d75730603ec6`

```dockerfile
```

-	Layers:
	-	`sha256:325a4ab33a42d976c41276df893b8a6fac1ffb11c32e74d323a73300ffcab816`  
		Last Modified: Thu, 11 Jun 2026 02:38:25 GMT  
		Size: 6.7 MB (6673625 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:edc92bac93d6fe676f799a5b64caa5c8dd2703a51b4e1427264c7e693404085e`  
		Last Modified: Thu, 11 Jun 2026 02:38:25 GMT  
		Size: 14.8 KB (14850 bytes)  
		MIME: application/vnd.in-toto+json
