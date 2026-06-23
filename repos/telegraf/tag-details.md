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
$ docker pull telegraf@sha256:2bbb518d69f0544eaca2a54322908c2b5800f5ba094a12f152676935afb5ce8d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.37-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:a611cb34739d2b4944daa6255a16a37ef417c0c3a8670c4396b6453142b039ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.9 MB (86877437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:781c36361ea2743eeb299620557502c98eebed9a491e1d1f7e8ed29eda9f78f1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:21 GMT
ADD alpine-minirootfs-3.22.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:21 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 20:08:45 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 22 Jun 2026 20:08:45 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 22 Jun 2026 20:08:52 GMT
ENV TELEGRAF_VERSION=1.37.3
# Mon, 22 Jun 2026 20:08:52 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 22 Jun 2026 20:08:52 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 22 Jun 2026 20:08:52 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 22 Jun 2026 20:08:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Jun 2026 20:08:52 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:f7ee36c9aa34bbb665f975c76e5c0d1607f0674b94c84cfb0061f87006ea5d10`  
		Last Modified: Mon, 22 Jun 2026 09:11:44 GMT  
		Size: 3.8 MB (3787595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:194bf597cb6f9f4e4ac14e4ecf923d10e5f506b6e56f7d36244ae5aa7b4137fb`  
		Last Modified: Mon, 22 Jun 2026 20:09:08 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc140e323b3c5cdd121b5bb99e0cbeb114b2117b30604c681f930de579c8dec6`  
		Last Modified: Mon, 22 Jun 2026 20:09:08 GMT  
		Size: 2.5 MB (2511659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39f3a3b505e51075e6e4ace592478ffa3d4bb1306ca571430a868d519ee70a85`  
		Last Modified: Mon, 22 Jun 2026 20:09:10 GMT  
		Size: 80.6 MB (80577284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a466e97127874af7e9e330b007efc7af4b2d5de51bdf5504bf6edf3000fc0a73`  
		Last Modified: Mon, 22 Jun 2026 20:09:08 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.37-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:4bd9ca2af5efc00299c2d45a14020605d7d285e089ef5dc25ddcf5ebc47abbb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1150507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:929ea6ff1a7b9b094747d55d3d207695de2b76a7151c71574b1de382f608299f`

```dockerfile
```

-	Layers:
	-	`sha256:4d7effe956778f7847bccdfb2116149fc770a87375a1e6ce4d5c63dd263bed69`  
		Last Modified: Mon, 22 Jun 2026 20:09:08 GMT  
		Size: 1.1 MB (1135589 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c831f4e59e5363ebfabb7f9bcbb224e7615234783f6c66486165309d8a46664d`  
		Last Modified: Mon, 22 Jun 2026 20:09:08 GMT  
		Size: 14.9 KB (14918 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.37-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:0887d7caa6a0d0793771cb0f50ee42fae77a52d44736cba379e061e303fd0319
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.7 MB (78658383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7a4baac8ce2ece31f1e506d7a476b40720f2b38575e5e2c6cab55ea423e65c4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:11 GMT
ADD alpine-minirootfs-3.22.5-aarch64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:11 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 20:11:44 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 22 Jun 2026 20:11:46 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 22 Jun 2026 20:11:53 GMT
ENV TELEGRAF_VERSION=1.37.3
# Mon, 22 Jun 2026 20:11:53 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 22 Jun 2026 20:11:53 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 22 Jun 2026 20:11:53 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 22 Jun 2026 20:11:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Jun 2026 20:11:53 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:738128faa30f570583b0e57efd831e0e6a2a9aacf1be88c8f4c1ef8a5b7033cc`  
		Last Modified: Mon, 22 Jun 2026 09:11:35 GMT  
		Size: 4.1 MB (4120486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d27a4f7541d79b95fdb40d40de6cf09fa31effe5b94d8521a343228a0bf34b18`  
		Last Modified: Mon, 22 Jun 2026 20:12:06 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5066e9f898666ad4d3312ea3082d02c8580d05a81548755066346d9a21026c34`  
		Last Modified: Mon, 22 Jun 2026 20:12:07 GMT  
		Size: 2.6 MB (2578489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ccabcf6b51d35af2690ca16078ef4ef71447698089e7915fbd37a9c40eb4d68`  
		Last Modified: Mon, 22 Jun 2026 20:12:09 GMT  
		Size: 72.0 MB (71958511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9063ba0c9c7ede43c226489650abd815b2fcfa721543a4c1163a7f8e19a4d16`  
		Last Modified: Mon, 22 Jun 2026 20:12:07 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.37-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:716edec7cf8b33075af528e6cd778d056a4ee41817e2fa9eef2c48838d691e3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1146244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6b7b9cfe54b8471c66db97423164fb2581e59ee5003becadd4a29543488a02c`

```dockerfile
```

-	Layers:
	-	`sha256:a5c5501e40490dacbc0f2959d8f3c8a4fe98477b60d967901613442adeed2730`  
		Last Modified: Mon, 22 Jun 2026 20:12:07 GMT  
		Size: 1.1 MB (1131216 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7496bbc9b77326bbe891e9993d8bf5cf35b7b7802ec20e08addad69dd65e0cfc`  
		Last Modified: Mon, 22 Jun 2026 20:12:07 GMT  
		Size: 15.0 KB (15028 bytes)  
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
$ docker pull telegraf@sha256:2bbb518d69f0544eaca2a54322908c2b5800f5ba094a12f152676935afb5ce8d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.37.3-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:a611cb34739d2b4944daa6255a16a37ef417c0c3a8670c4396b6453142b039ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.9 MB (86877437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:781c36361ea2743eeb299620557502c98eebed9a491e1d1f7e8ed29eda9f78f1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:21 GMT
ADD alpine-minirootfs-3.22.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:21 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 20:08:45 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 22 Jun 2026 20:08:45 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 22 Jun 2026 20:08:52 GMT
ENV TELEGRAF_VERSION=1.37.3
# Mon, 22 Jun 2026 20:08:52 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 22 Jun 2026 20:08:52 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 22 Jun 2026 20:08:52 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 22 Jun 2026 20:08:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Jun 2026 20:08:52 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:f7ee36c9aa34bbb665f975c76e5c0d1607f0674b94c84cfb0061f87006ea5d10`  
		Last Modified: Mon, 22 Jun 2026 09:11:44 GMT  
		Size: 3.8 MB (3787595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:194bf597cb6f9f4e4ac14e4ecf923d10e5f506b6e56f7d36244ae5aa7b4137fb`  
		Last Modified: Mon, 22 Jun 2026 20:09:08 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc140e323b3c5cdd121b5bb99e0cbeb114b2117b30604c681f930de579c8dec6`  
		Last Modified: Mon, 22 Jun 2026 20:09:08 GMT  
		Size: 2.5 MB (2511659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39f3a3b505e51075e6e4ace592478ffa3d4bb1306ca571430a868d519ee70a85`  
		Last Modified: Mon, 22 Jun 2026 20:09:10 GMT  
		Size: 80.6 MB (80577284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a466e97127874af7e9e330b007efc7af4b2d5de51bdf5504bf6edf3000fc0a73`  
		Last Modified: Mon, 22 Jun 2026 20:09:08 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.37.3-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:4bd9ca2af5efc00299c2d45a14020605d7d285e089ef5dc25ddcf5ebc47abbb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1150507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:929ea6ff1a7b9b094747d55d3d207695de2b76a7151c71574b1de382f608299f`

```dockerfile
```

-	Layers:
	-	`sha256:4d7effe956778f7847bccdfb2116149fc770a87375a1e6ce4d5c63dd263bed69`  
		Last Modified: Mon, 22 Jun 2026 20:09:08 GMT  
		Size: 1.1 MB (1135589 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c831f4e59e5363ebfabb7f9bcbb224e7615234783f6c66486165309d8a46664d`  
		Last Modified: Mon, 22 Jun 2026 20:09:08 GMT  
		Size: 14.9 KB (14918 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.37.3-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:0887d7caa6a0d0793771cb0f50ee42fae77a52d44736cba379e061e303fd0319
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.7 MB (78658383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7a4baac8ce2ece31f1e506d7a476b40720f2b38575e5e2c6cab55ea423e65c4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:11 GMT
ADD alpine-minirootfs-3.22.5-aarch64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:11 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 20:11:44 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 22 Jun 2026 20:11:46 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 22 Jun 2026 20:11:53 GMT
ENV TELEGRAF_VERSION=1.37.3
# Mon, 22 Jun 2026 20:11:53 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 22 Jun 2026 20:11:53 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 22 Jun 2026 20:11:53 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 22 Jun 2026 20:11:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Jun 2026 20:11:53 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:738128faa30f570583b0e57efd831e0e6a2a9aacf1be88c8f4c1ef8a5b7033cc`  
		Last Modified: Mon, 22 Jun 2026 09:11:35 GMT  
		Size: 4.1 MB (4120486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d27a4f7541d79b95fdb40d40de6cf09fa31effe5b94d8521a343228a0bf34b18`  
		Last Modified: Mon, 22 Jun 2026 20:12:06 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5066e9f898666ad4d3312ea3082d02c8580d05a81548755066346d9a21026c34`  
		Last Modified: Mon, 22 Jun 2026 20:12:07 GMT  
		Size: 2.6 MB (2578489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ccabcf6b51d35af2690ca16078ef4ef71447698089e7915fbd37a9c40eb4d68`  
		Last Modified: Mon, 22 Jun 2026 20:12:09 GMT  
		Size: 72.0 MB (71958511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9063ba0c9c7ede43c226489650abd815b2fcfa721543a4c1163a7f8e19a4d16`  
		Last Modified: Mon, 22 Jun 2026 20:12:07 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.37.3-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:716edec7cf8b33075af528e6cd778d056a4ee41817e2fa9eef2c48838d691e3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1146244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6b7b9cfe54b8471c66db97423164fb2581e59ee5003becadd4a29543488a02c`

```dockerfile
```

-	Layers:
	-	`sha256:a5c5501e40490dacbc0f2959d8f3c8a4fe98477b60d967901613442adeed2730`  
		Last Modified: Mon, 22 Jun 2026 20:12:07 GMT  
		Size: 1.1 MB (1131216 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7496bbc9b77326bbe891e9993d8bf5cf35b7b7802ec20e08addad69dd65e0cfc`  
		Last Modified: Mon, 22 Jun 2026 20:12:07 GMT  
		Size: 15.0 KB (15028 bytes)  
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
$ docker pull telegraf@sha256:195e52e7d20d068fb8b9c39819faeb8e21cdbad8f3c09fa63a11f56246357e6b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.38-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:e714eb35acf3e70a6c5c0395873efb12938755e4eb05083598e733b7580b868a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.7 MB (89713960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c544a94ed8d187df1edeaff3534091f47ed584f404e0c5504ee8968e04e4f63d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:09 GMT
ADD alpine-minirootfs-3.23.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:09 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 20:08:53 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 22 Jun 2026 20:08:54 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 22 Jun 2026 20:09:00 GMT
ENV TELEGRAF_VERSION=1.38.4
# Mon, 22 Jun 2026 20:09:00 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 22 Jun 2026 20:09:00 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 22 Jun 2026 20:09:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 22 Jun 2026 20:09:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Jun 2026 20:09:00 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:e6f31ffc071e5560b82a8685fba8214954e5721e3e49269d00958316edbe89fe`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.8 MB (3844421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64fc2418181e2eec37d366a16fdf647689738a6020b7a9aa004befedaebdf330`  
		Last Modified: Mon, 22 Jun 2026 20:09:16 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3001d3f012409e7632fda470c52eff60f5aa560f1ea5367f93dfc06532c1053`  
		Last Modified: Mon, 22 Jun 2026 20:09:16 GMT  
		Size: 2.6 MB (2568205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1aa8791fc292f7d715a4ec73e28141e5fdce58d6d0acc7866acae05116d1b36`  
		Last Modified: Mon, 22 Jun 2026 20:09:18 GMT  
		Size: 83.3 MB (83300435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01abc246ffe1478dcf3a2bd1812fc4e8949f57c9ff2249fecbdc8c816cdec3af`  
		Last Modified: Mon, 22 Jun 2026 20:09:16 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.38-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:673e2db49e3dd88251e19cbc6e90c71f72b432f70de8f58e326ae44345a1a123
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1157149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2d2a80d8197aeec533c3c498c604a652d379d56145d0e382ea40ba095833f9a`

```dockerfile
```

-	Layers:
	-	`sha256:b8d6c72ba4ffd10a10267f5086eb16853021305ea507556e5a8b955280d6c14e`  
		Last Modified: Mon, 22 Jun 2026 20:09:16 GMT  
		Size: 1.1 MB (1142231 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebcc7662e79e84caec4978dd6b0e238196da14464bbfa781ca7e3019280ebddc`  
		Last Modified: Mon, 22 Jun 2026 20:09:16 GMT  
		Size: 14.9 KB (14918 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.38-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:bafa9618a020524cbfbd857f1deac3c84719b4ecbd3ece82f0804282c627f96d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.1 MB (81078772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab6c25df0f302fa5a43cddb6400eb075d4d0fca9cb5b701b83b9b94279f0151c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:57 GMT
ADD alpine-minirootfs-3.23.5-aarch64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:57 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 20:11:49 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 22 Jun 2026 20:11:50 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 22 Jun 2026 20:11:56 GMT
ENV TELEGRAF_VERSION=1.38.4
# Mon, 22 Jun 2026 20:11:56 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 22 Jun 2026 20:11:56 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 22 Jun 2026 20:11:56 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 22 Jun 2026 20:11:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Jun 2026 20:11:56 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:14a4754c352fba4c6c0da8e4f01bb990463c19f7ff63e090073c385bd2bc5046`  
		Last Modified: Mon, 22 Jun 2026 12:03:31 GMT  
		Size: 4.2 MB (4181860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9e63818f95bde7c4203c7b17d236bdd8fbe58b523e900944dd984825b444178`  
		Last Modified: Mon, 22 Jun 2026 20:12:09 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61e896fb6b98964848b90f3ce6fffdd5bd5dbe42fd6b83e3808eeae74cdd9f21`  
		Last Modified: Mon, 22 Jun 2026 20:12:10 GMT  
		Size: 2.6 MB (2617155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:389345b38b3eafc6c6a9f0747acfd3a2aa0a8d9aade6c1c1dc7f2a80e29705d0`  
		Last Modified: Mon, 22 Jun 2026 20:12:13 GMT  
		Size: 74.3 MB (74278857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3878046ed96bb17cd231ce52d24084c7672b3e6656a5fffce3e1f56862a4181f`  
		Last Modified: Mon, 22 Jun 2026 20:12:09 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.38-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:398da6c1ebd5e0e6d5e78ebc1c33661011cbb95f205870e7be0148740fb67b2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1152236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c710771442252de84c28d14e92594bd71e872a6a5ee49f0c3eefd1e88f59164b`

```dockerfile
```

-	Layers:
	-	`sha256:5535a38bbb2f840db9bd10171484871e039b62f3cb936db054e65fc808b054a8`  
		Last Modified: Mon, 22 Jun 2026 20:12:09 GMT  
		Size: 1.1 MB (1137208 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b1e9b3a8d8cef361603d71fc431dd83123a292edcea9d593307e0274b79b322`  
		Last Modified: Mon, 22 Jun 2026 20:12:09 GMT  
		Size: 15.0 KB (15028 bytes)  
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
$ docker pull telegraf@sha256:195e52e7d20d068fb8b9c39819faeb8e21cdbad8f3c09fa63a11f56246357e6b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.38.4-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:e714eb35acf3e70a6c5c0395873efb12938755e4eb05083598e733b7580b868a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.7 MB (89713960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c544a94ed8d187df1edeaff3534091f47ed584f404e0c5504ee8968e04e4f63d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:09 GMT
ADD alpine-minirootfs-3.23.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:09 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 20:08:53 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 22 Jun 2026 20:08:54 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 22 Jun 2026 20:09:00 GMT
ENV TELEGRAF_VERSION=1.38.4
# Mon, 22 Jun 2026 20:09:00 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 22 Jun 2026 20:09:00 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 22 Jun 2026 20:09:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 22 Jun 2026 20:09:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Jun 2026 20:09:00 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:e6f31ffc071e5560b82a8685fba8214954e5721e3e49269d00958316edbe89fe`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.8 MB (3844421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64fc2418181e2eec37d366a16fdf647689738a6020b7a9aa004befedaebdf330`  
		Last Modified: Mon, 22 Jun 2026 20:09:16 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3001d3f012409e7632fda470c52eff60f5aa560f1ea5367f93dfc06532c1053`  
		Last Modified: Mon, 22 Jun 2026 20:09:16 GMT  
		Size: 2.6 MB (2568205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1aa8791fc292f7d715a4ec73e28141e5fdce58d6d0acc7866acae05116d1b36`  
		Last Modified: Mon, 22 Jun 2026 20:09:18 GMT  
		Size: 83.3 MB (83300435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01abc246ffe1478dcf3a2bd1812fc4e8949f57c9ff2249fecbdc8c816cdec3af`  
		Last Modified: Mon, 22 Jun 2026 20:09:16 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.38.4-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:673e2db49e3dd88251e19cbc6e90c71f72b432f70de8f58e326ae44345a1a123
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1157149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2d2a80d8197aeec533c3c498c604a652d379d56145d0e382ea40ba095833f9a`

```dockerfile
```

-	Layers:
	-	`sha256:b8d6c72ba4ffd10a10267f5086eb16853021305ea507556e5a8b955280d6c14e`  
		Last Modified: Mon, 22 Jun 2026 20:09:16 GMT  
		Size: 1.1 MB (1142231 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebcc7662e79e84caec4978dd6b0e238196da14464bbfa781ca7e3019280ebddc`  
		Last Modified: Mon, 22 Jun 2026 20:09:16 GMT  
		Size: 14.9 KB (14918 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.38.4-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:bafa9618a020524cbfbd857f1deac3c84719b4ecbd3ece82f0804282c627f96d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.1 MB (81078772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab6c25df0f302fa5a43cddb6400eb075d4d0fca9cb5b701b83b9b94279f0151c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:57 GMT
ADD alpine-minirootfs-3.23.5-aarch64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:57 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 20:11:49 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 22 Jun 2026 20:11:50 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 22 Jun 2026 20:11:56 GMT
ENV TELEGRAF_VERSION=1.38.4
# Mon, 22 Jun 2026 20:11:56 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 22 Jun 2026 20:11:56 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 22 Jun 2026 20:11:56 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 22 Jun 2026 20:11:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Jun 2026 20:11:56 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:14a4754c352fba4c6c0da8e4f01bb990463c19f7ff63e090073c385bd2bc5046`  
		Last Modified: Mon, 22 Jun 2026 12:03:31 GMT  
		Size: 4.2 MB (4181860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9e63818f95bde7c4203c7b17d236bdd8fbe58b523e900944dd984825b444178`  
		Last Modified: Mon, 22 Jun 2026 20:12:09 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61e896fb6b98964848b90f3ce6fffdd5bd5dbe42fd6b83e3808eeae74cdd9f21`  
		Last Modified: Mon, 22 Jun 2026 20:12:10 GMT  
		Size: 2.6 MB (2617155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:389345b38b3eafc6c6a9f0747acfd3a2aa0a8d9aade6c1c1dc7f2a80e29705d0`  
		Last Modified: Mon, 22 Jun 2026 20:12:13 GMT  
		Size: 74.3 MB (74278857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3878046ed96bb17cd231ce52d24084c7672b3e6656a5fffce3e1f56862a4181f`  
		Last Modified: Mon, 22 Jun 2026 20:12:09 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.38.4-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:398da6c1ebd5e0e6d5e78ebc1c33661011cbb95f205870e7be0148740fb67b2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1152236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c710771442252de84c28d14e92594bd71e872a6a5ee49f0c3eefd1e88f59164b`

```dockerfile
```

-	Layers:
	-	`sha256:5535a38bbb2f840db9bd10171484871e039b62f3cb936db054e65fc808b054a8`  
		Last Modified: Mon, 22 Jun 2026 20:12:09 GMT  
		Size: 1.1 MB (1137208 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b1e9b3a8d8cef361603d71fc431dd83123a292edcea9d593307e0274b79b322`  
		Last Modified: Mon, 22 Jun 2026 20:12:09 GMT  
		Size: 15.0 KB (15028 bytes)  
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
$ docker pull telegraf@sha256:dcad79e7e0fd1d28b058785bed296b5bf17465105ef0545f20df901003f97d59
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.39-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:2a31f3ab80358cdab9c560aa5a4bd1aa6905161caa9ef601cb648f983ff29012
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.0 MB (90023661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82cc38c7ee146bffe5a5c2533a9244ca19b9d161e5eaf93d3b5e3b55802e4721`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:09 GMT
ADD alpine-minirootfs-3.23.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:09 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 20:08:58 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 22 Jun 2026 20:08:58 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 22 Jun 2026 20:09:04 GMT
ENV TELEGRAF_VERSION=1.39.0
# Mon, 22 Jun 2026 20:09:04 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 22 Jun 2026 20:09:04 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 22 Jun 2026 20:09:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 22 Jun 2026 20:09:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Jun 2026 20:09:04 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:e6f31ffc071e5560b82a8685fba8214954e5721e3e49269d00958316edbe89fe`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.8 MB (3844421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc9191bff1bb8c25b9458adedd1f6d65ba0683b98cd126fa081cb5fa418e963a`  
		Last Modified: Mon, 22 Jun 2026 20:09:19 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc04dba755564c53fad68a69f9f1c4f28bbc17554caea9461ddbab84e381f334`  
		Last Modified: Mon, 22 Jun 2026 20:09:19 GMT  
		Size: 2.6 MB (2568188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a937e75bac10850cd72cabb1cd04c52268007a8e94e4c88c630d45c91b7e284d`  
		Last Modified: Mon, 22 Jun 2026 20:09:21 GMT  
		Size: 83.6 MB (83610155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0afc95c287107fe2631324d08dbe3b22efc9d29dcfeb19058bec982d7a4ad810`  
		Last Modified: Mon, 22 Jun 2026 20:09:19 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.39-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:02ba7fa4240b642b1846a2d2fef75600ecb340ab8f1980e899b4468d2f8f9a4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1156089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b37cbf9195ab18fade8f6f627a5e0c51b0ebf759301317929b4a1004b6864be`

```dockerfile
```

-	Layers:
	-	`sha256:9d0ed847d3a3d6f5389256bb16368d595ffc3437bdefd69e91d84e60ab5f9035`  
		Last Modified: Mon, 22 Jun 2026 20:09:19 GMT  
		Size: 1.1 MB (1140869 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b14bfa3e77cb08911b08ba335be53877f8b9e657b2b8576bce0d2208b04d1744`  
		Last Modified: Mon, 22 Jun 2026 20:09:18 GMT  
		Size: 15.2 KB (15220 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.39-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:a490f40482eebaf5cfff05247da4a60aaac0c58eebf1fd6706c041db40513189
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.3 MB (81338347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac02808a1a52561ce912df080099550326287fe66f27217871f0b9fc84d459d0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:57 GMT
ADD alpine-minirootfs-3.23.5-aarch64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:57 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 20:12:17 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 22 Jun 2026 20:12:18 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 22 Jun 2026 20:12:24 GMT
ENV TELEGRAF_VERSION=1.39.0
# Mon, 22 Jun 2026 20:12:24 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 22 Jun 2026 20:12:24 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 22 Jun 2026 20:12:24 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 22 Jun 2026 20:12:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Jun 2026 20:12:24 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:14a4754c352fba4c6c0da8e4f01bb990463c19f7ff63e090073c385bd2bc5046`  
		Last Modified: Mon, 22 Jun 2026 12:03:31 GMT  
		Size: 4.2 MB (4181860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68ea295c9c9414f5365ac233e06d57822557a1e42e235c26860245b26ace649b`  
		Last Modified: Mon, 22 Jun 2026 20:12:37 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9e9cafb73aa970d7deaca83e888b6559118bbe2ae71452a4a4eef3d116cf334`  
		Last Modified: Mon, 22 Jun 2026 20:12:38 GMT  
		Size: 2.6 MB (2617156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6d0a151684c9dabff79b5e109472ed815f24faa91b4155e65293c803d814908`  
		Last Modified: Mon, 22 Jun 2026 20:12:40 GMT  
		Size: 74.5 MB (74538432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9e76068b32b192a95aeaf60ae3c2a673fca3f4263ef1d563531b4b699a41305`  
		Last Modified: Mon, 22 Jun 2026 20:12:37 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.39-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:e33aa698fb59e981fdf3636b043318453d764759cdd0e4d102447fcdc58091c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1151199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad48249f33a230cfa1918cf57f9fcc7dcb60ad84bafa9359111362dea269ee9f`

```dockerfile
```

-	Layers:
	-	`sha256:86cc95eb261275c037858bb0cd73b13e70e9f5ee9acfc141acc709ca57b391be`  
		Last Modified: Mon, 22 Jun 2026 20:12:37 GMT  
		Size: 1.1 MB (1135858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9dde5d8df7a14d193176597fe4573083fe0d7aa197b9fe299ca51ad72870f0f`  
		Last Modified: Mon, 22 Jun 2026 20:12:38 GMT  
		Size: 15.3 KB (15341 bytes)  
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
$ docker pull telegraf@sha256:dcad79e7e0fd1d28b058785bed296b5bf17465105ef0545f20df901003f97d59
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.39.0-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:2a31f3ab80358cdab9c560aa5a4bd1aa6905161caa9ef601cb648f983ff29012
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.0 MB (90023661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82cc38c7ee146bffe5a5c2533a9244ca19b9d161e5eaf93d3b5e3b55802e4721`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:09 GMT
ADD alpine-minirootfs-3.23.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:09 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 20:08:58 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 22 Jun 2026 20:08:58 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 22 Jun 2026 20:09:04 GMT
ENV TELEGRAF_VERSION=1.39.0
# Mon, 22 Jun 2026 20:09:04 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 22 Jun 2026 20:09:04 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 22 Jun 2026 20:09:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 22 Jun 2026 20:09:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Jun 2026 20:09:04 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:e6f31ffc071e5560b82a8685fba8214954e5721e3e49269d00958316edbe89fe`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.8 MB (3844421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc9191bff1bb8c25b9458adedd1f6d65ba0683b98cd126fa081cb5fa418e963a`  
		Last Modified: Mon, 22 Jun 2026 20:09:19 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc04dba755564c53fad68a69f9f1c4f28bbc17554caea9461ddbab84e381f334`  
		Last Modified: Mon, 22 Jun 2026 20:09:19 GMT  
		Size: 2.6 MB (2568188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a937e75bac10850cd72cabb1cd04c52268007a8e94e4c88c630d45c91b7e284d`  
		Last Modified: Mon, 22 Jun 2026 20:09:21 GMT  
		Size: 83.6 MB (83610155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0afc95c287107fe2631324d08dbe3b22efc9d29dcfeb19058bec982d7a4ad810`  
		Last Modified: Mon, 22 Jun 2026 20:09:19 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.39.0-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:02ba7fa4240b642b1846a2d2fef75600ecb340ab8f1980e899b4468d2f8f9a4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1156089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b37cbf9195ab18fade8f6f627a5e0c51b0ebf759301317929b4a1004b6864be`

```dockerfile
```

-	Layers:
	-	`sha256:9d0ed847d3a3d6f5389256bb16368d595ffc3437bdefd69e91d84e60ab5f9035`  
		Last Modified: Mon, 22 Jun 2026 20:09:19 GMT  
		Size: 1.1 MB (1140869 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b14bfa3e77cb08911b08ba335be53877f8b9e657b2b8576bce0d2208b04d1744`  
		Last Modified: Mon, 22 Jun 2026 20:09:18 GMT  
		Size: 15.2 KB (15220 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.39.0-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:a490f40482eebaf5cfff05247da4a60aaac0c58eebf1fd6706c041db40513189
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.3 MB (81338347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac02808a1a52561ce912df080099550326287fe66f27217871f0b9fc84d459d0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:57 GMT
ADD alpine-minirootfs-3.23.5-aarch64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:57 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 20:12:17 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 22 Jun 2026 20:12:18 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 22 Jun 2026 20:12:24 GMT
ENV TELEGRAF_VERSION=1.39.0
# Mon, 22 Jun 2026 20:12:24 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 22 Jun 2026 20:12:24 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 22 Jun 2026 20:12:24 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 22 Jun 2026 20:12:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Jun 2026 20:12:24 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:14a4754c352fba4c6c0da8e4f01bb990463c19f7ff63e090073c385bd2bc5046`  
		Last Modified: Mon, 22 Jun 2026 12:03:31 GMT  
		Size: 4.2 MB (4181860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68ea295c9c9414f5365ac233e06d57822557a1e42e235c26860245b26ace649b`  
		Last Modified: Mon, 22 Jun 2026 20:12:37 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9e9cafb73aa970d7deaca83e888b6559118bbe2ae71452a4a4eef3d116cf334`  
		Last Modified: Mon, 22 Jun 2026 20:12:38 GMT  
		Size: 2.6 MB (2617156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6d0a151684c9dabff79b5e109472ed815f24faa91b4155e65293c803d814908`  
		Last Modified: Mon, 22 Jun 2026 20:12:40 GMT  
		Size: 74.5 MB (74538432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9e76068b32b192a95aeaf60ae3c2a673fca3f4263ef1d563531b4b699a41305`  
		Last Modified: Mon, 22 Jun 2026 20:12:37 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.39.0-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:e33aa698fb59e981fdf3636b043318453d764759cdd0e4d102447fcdc58091c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1151199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad48249f33a230cfa1918cf57f9fcc7dcb60ad84bafa9359111362dea269ee9f`

```dockerfile
```

-	Layers:
	-	`sha256:86cc95eb261275c037858bb0cd73b13e70e9f5ee9acfc141acc709ca57b391be`  
		Last Modified: Mon, 22 Jun 2026 20:12:37 GMT  
		Size: 1.1 MB (1135858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9dde5d8df7a14d193176597fe4573083fe0d7aa197b9fe299ca51ad72870f0f`  
		Last Modified: Mon, 22 Jun 2026 20:12:38 GMT  
		Size: 15.3 KB (15341 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:alpine`

```console
$ docker pull telegraf@sha256:dcad79e7e0fd1d28b058785bed296b5bf17465105ef0545f20df901003f97d59
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:2a31f3ab80358cdab9c560aa5a4bd1aa6905161caa9ef601cb648f983ff29012
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.0 MB (90023661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82cc38c7ee146bffe5a5c2533a9244ca19b9d161e5eaf93d3b5e3b55802e4721`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:09 GMT
ADD alpine-minirootfs-3.23.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:09 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 20:08:58 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 22 Jun 2026 20:08:58 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 22 Jun 2026 20:09:04 GMT
ENV TELEGRAF_VERSION=1.39.0
# Mon, 22 Jun 2026 20:09:04 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 22 Jun 2026 20:09:04 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 22 Jun 2026 20:09:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 22 Jun 2026 20:09:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Jun 2026 20:09:04 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:e6f31ffc071e5560b82a8685fba8214954e5721e3e49269d00958316edbe89fe`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.8 MB (3844421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc9191bff1bb8c25b9458adedd1f6d65ba0683b98cd126fa081cb5fa418e963a`  
		Last Modified: Mon, 22 Jun 2026 20:09:19 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc04dba755564c53fad68a69f9f1c4f28bbc17554caea9461ddbab84e381f334`  
		Last Modified: Mon, 22 Jun 2026 20:09:19 GMT  
		Size: 2.6 MB (2568188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a937e75bac10850cd72cabb1cd04c52268007a8e94e4c88c630d45c91b7e284d`  
		Last Modified: Mon, 22 Jun 2026 20:09:21 GMT  
		Size: 83.6 MB (83610155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0afc95c287107fe2631324d08dbe3b22efc9d29dcfeb19058bec982d7a4ad810`  
		Last Modified: Mon, 22 Jun 2026 20:09:19 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:02ba7fa4240b642b1846a2d2fef75600ecb340ab8f1980e899b4468d2f8f9a4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1156089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b37cbf9195ab18fade8f6f627a5e0c51b0ebf759301317929b4a1004b6864be`

```dockerfile
```

-	Layers:
	-	`sha256:9d0ed847d3a3d6f5389256bb16368d595ffc3437bdefd69e91d84e60ab5f9035`  
		Last Modified: Mon, 22 Jun 2026 20:09:19 GMT  
		Size: 1.1 MB (1140869 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b14bfa3e77cb08911b08ba335be53877f8b9e657b2b8576bce0d2208b04d1744`  
		Last Modified: Mon, 22 Jun 2026 20:09:18 GMT  
		Size: 15.2 KB (15220 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:a490f40482eebaf5cfff05247da4a60aaac0c58eebf1fd6706c041db40513189
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.3 MB (81338347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac02808a1a52561ce912df080099550326287fe66f27217871f0b9fc84d459d0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:57 GMT
ADD alpine-minirootfs-3.23.5-aarch64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:57 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 20:12:17 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 22 Jun 2026 20:12:18 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 22 Jun 2026 20:12:24 GMT
ENV TELEGRAF_VERSION=1.39.0
# Mon, 22 Jun 2026 20:12:24 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 22 Jun 2026 20:12:24 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 22 Jun 2026 20:12:24 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 22 Jun 2026 20:12:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Jun 2026 20:12:24 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:14a4754c352fba4c6c0da8e4f01bb990463c19f7ff63e090073c385bd2bc5046`  
		Last Modified: Mon, 22 Jun 2026 12:03:31 GMT  
		Size: 4.2 MB (4181860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68ea295c9c9414f5365ac233e06d57822557a1e42e235c26860245b26ace649b`  
		Last Modified: Mon, 22 Jun 2026 20:12:37 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9e9cafb73aa970d7deaca83e888b6559118bbe2ae71452a4a4eef3d116cf334`  
		Last Modified: Mon, 22 Jun 2026 20:12:38 GMT  
		Size: 2.6 MB (2617156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6d0a151684c9dabff79b5e109472ed815f24faa91b4155e65293c803d814908`  
		Last Modified: Mon, 22 Jun 2026 20:12:40 GMT  
		Size: 74.5 MB (74538432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9e76068b32b192a95aeaf60ae3c2a673fca3f4263ef1d563531b4b699a41305`  
		Last Modified: Mon, 22 Jun 2026 20:12:37 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:e33aa698fb59e981fdf3636b043318453d764759cdd0e4d102447fcdc58091c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1151199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad48249f33a230cfa1918cf57f9fcc7dcb60ad84bafa9359111362dea269ee9f`

```dockerfile
```

-	Layers:
	-	`sha256:86cc95eb261275c037858bb0cd73b13e70e9f5ee9acfc141acc709ca57b391be`  
		Last Modified: Mon, 22 Jun 2026 20:12:37 GMT  
		Size: 1.1 MB (1135858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9dde5d8df7a14d193176597fe4573083fe0d7aa197b9fe299ca51ad72870f0f`  
		Last Modified: Mon, 22 Jun 2026 20:12:38 GMT  
		Size: 15.3 KB (15341 bytes)  
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
