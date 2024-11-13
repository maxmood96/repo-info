<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `telegraf`

-	[`telegraf:1.30`](#telegraf130)
-	[`telegraf:1.30-alpine`](#telegraf130-alpine)
-	[`telegraf:1.30.3`](#telegraf1303)
-	[`telegraf:1.30.3-alpine`](#telegraf1303-alpine)
-	[`telegraf:1.31`](#telegraf131)
-	[`telegraf:1.31-alpine`](#telegraf131-alpine)
-	[`telegraf:1.31.3`](#telegraf1313)
-	[`telegraf:1.31.3-alpine`](#telegraf1313-alpine)
-	[`telegraf:1.32`](#telegraf132)
-	[`telegraf:1.32-alpine`](#telegraf132-alpine)
-	[`telegraf:1.32.2`](#telegraf1322)
-	[`telegraf:1.32.2-alpine`](#telegraf1322-alpine)
-	[`telegraf:alpine`](#telegrafalpine)
-	[`telegraf:latest`](#telegraflatest)

## `telegraf:1.30`

```console
$ docker pull telegraf@sha256:991dc94641004ef6125e685bb67a8aa4e8b9fe39af16259d97a4943331602ca1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.30` - linux; amd64

```console
$ docker pull telegraf@sha256:26c993c5f082e6633a79fd083b0b38967de5b24cd930b2d742887d7fa03ddad7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.4 MB (155350936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70b1373ef2b8da66c0cfe9d58ae2e61d6f1280b5528300791a3c29bb4dd86d95`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
ENV TELEGRAF_VERSION=1.30.3
# Mon, 28 Oct 2024 22:11:39 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 28 Oct 2024 22:11:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Oct 2024 22:11:39 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:b2b31b28ee3c96e96195c754f8679f690db4b18e475682d716122016ef056f39`  
		Last Modified: Tue, 12 Nov 2024 00:55:23 GMT  
		Size: 49.6 MB (49575695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3cc7b6f04730c072f8b292917e0d95bb886096a2b2b1781196170965161cd27`  
		Last Modified: Tue, 12 Nov 2024 02:38:12 GMT  
		Size: 24.1 MB (24058346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad4cea0931f00f3874f45e2d5d38a115308f2056139190ff3003741afbfd9e50`  
		Last Modified: Tue, 12 Nov 2024 03:16:41 GMT  
		Size: 18.9 MB (18948068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63fa33d58f88292792c7e2d328aa6fcd59f485dd738b74ffdf7b286d1d2c15de`  
		Last Modified: Tue, 12 Nov 2024 03:16:41 GMT  
		Size: 1.8 KB (1782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c1d1a7d397fc3e016436dc9e2d9d980a917f7472111cd5bc501534cd13cd744`  
		Last Modified: Tue, 12 Nov 2024 03:16:42 GMT  
		Size: 62.8 MB (62766422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c29a82085d128f1e58771860d33ec2473b3296e7251cccdf648d8afd90e08c2d`  
		Last Modified: Tue, 12 Nov 2024 03:16:41 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.30` - unknown; unknown

```console
$ docker pull telegraf@sha256:29a6c70301633a0dc0b108028361cc82003314bac59f9ee49ccbe99011ba9a56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6424853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cbb55846b6b50d56a79b604c3365352499f06e552fc38a818858e5d962c1081`

```dockerfile
```

-	Layers:
	-	`sha256:5ed05627e8f4010ce1ab4ab418e71d38bef57c9ab660078a2e200a0e3c3153df`  
		Last Modified: Tue, 12 Nov 2024 03:16:41 GMT  
		Size: 6.4 MB (6410383 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d28aec7ff055a76b5f12bdd01c1421b47c475df6431955096b5315e2f479c00`  
		Last Modified: Tue, 12 Nov 2024 03:16:41 GMT  
		Size: 14.5 KB (14470 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.30` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:1aec78acd484e3052a3b744aa4f506524919a9da02fc1433e8b4c0c4df5929c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.0 MB (143045409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9e3cf41e7ffdc46a369d820c9892c0398ad9c39b7f4f3bbb63bf1661b4676b6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:2ce9af7b514320ba230746cbff4f2f2e2b8d4a62ac035ebbe6575e17544f6416 in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
ENV TELEGRAF_VERSION=1.30.3
# Mon, 07 Oct 2024 21:02:29 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 07 Oct 2024 21:02:29 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 07 Oct 2024 21:02:29 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:b683f99b4cdeb3cb4e487b268b3949647168e16d00d07e004e03af92331dbfed`  
		Last Modified: Thu, 17 Oct 2024 03:06:32 GMT  
		Size: 45.1 MB (45147940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47b7fd5031c50fee563f16760ae6e5334672d6c9ba07d159b9e3a17a3b62011`  
		Last Modified: Sat, 19 Oct 2024 00:56:10 GMT  
		Size: 22.0 MB (21957404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2247d3273aa1d92c25210b647da389293f770c7463e0680590bba2707a00d4f`  
		Last Modified: Sat, 19 Oct 2024 07:17:52 GMT  
		Size: 17.7 MB (17724956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:431a3580592e7869e0e9a687eeb734ecbf61aa4864384cb91bf7c24aee3a5b0a`  
		Last Modified: Sat, 19 Oct 2024 07:17:51 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0d2306cc2f9dc432bdab9577e71740b948af00d4db1eb08443a0547eca2e52a`  
		Last Modified: Sat, 19 Oct 2024 07:17:54 GMT  
		Size: 58.2 MB (58212698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb81901359f5d7c38fe327abcc66538f8e4bbe770e9fdbc72048a59bd935fc94`  
		Last Modified: Sat, 19 Oct 2024 07:17:51 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.30` - unknown; unknown

```console
$ docker pull telegraf@sha256:a04be35abee58909c3d42aced2d9147ca36e1a4e096534266a96b0d2acfcf695
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6419536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ade3393bc72761ef0b9812ba99ab201b31ea335dce0f4179478937d6a830cc27`

```dockerfile
```

-	Layers:
	-	`sha256:761d0fbf418de95f0bf4b3d8831e7c0247231173b138cb38369af68e028d09aa`  
		Last Modified: Sat, 19 Oct 2024 07:17:52 GMT  
		Size: 6.4 MB (6404950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb0764e2e8db77601eaa76a040320d4088bea4d5b360d5b3af5469ddfb0053ac`  
		Last Modified: Sat, 19 Oct 2024 07:17:51 GMT  
		Size: 14.6 KB (14586 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.30` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:e15f4ecf24e9acd0d799b33dfe2655209cce1a2329ef58b7ea340d6b47526440
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.2 MB (149174941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68ee0153e92a6e7016af48b545c85b7478ac2c16331e327c3b5ffc11460a7058`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:1df819221542e236e104deb2624ffe4efd79382aed25b3ab20088becaeadad31 in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
ENV TELEGRAF_VERSION=1.30.3
# Mon, 07 Oct 2024 21:02:29 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 07 Oct 2024 21:02:29 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 07 Oct 2024 21:02:29 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:c1e0ef7b956a07c7b090256aa16cbb0550a34d0625d1d23c5b1a76e92a58d01e`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 49.6 MB (49584978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b894d63c771a6056bc65ff25192b251413259ba7d160b0076f0f5d7975dc39`  
		Last Modified: Sat, 19 Oct 2024 01:10:43 GMT  
		Size: 23.6 MB (23593834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c997025d65b9a3a17af2a5da355e59ddaef61afc5603e6e4f3d8c348d5dee2e2`  
		Last Modified: Sat, 19 Oct 2024 05:58:23 GMT  
		Size: 18.9 MB (18870445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3541e233720a537128c65519a803fff6e89bcae5e59f21c04e1e51e762996f72`  
		Last Modified: Sat, 19 Oct 2024 05:58:22 GMT  
		Size: 1.8 KB (1780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b91266b6b4b069749e7b9cfe1bb730c4ecfdcfca9f33b816b9e2f0c17f10ea15`  
		Last Modified: Sat, 19 Oct 2024 05:58:24 GMT  
		Size: 57.1 MB (57123282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d87c4bdfef8f024628957e3162ad4436c4d57fb0e5040c1e3a5970fbc4c23765`  
		Last Modified: Sat, 19 Oct 2024 05:58:22 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.30` - unknown; unknown

```console
$ docker pull telegraf@sha256:112ebaf7d621c726e72b5cb30a87e70283e1615524cf0c1ee94c1df9ba4a6b8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6424844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afc917b77a06f4ce84e84f3a352332a56c87ccbecb7fadb540e51ac5ca6f6cce`

```dockerfile
```

-	Layers:
	-	`sha256:8024b92a362069ab5c8cdbe2cdfe57d14579b8365e3e06d0e1968917732bd2a0`  
		Last Modified: Sat, 19 Oct 2024 05:58:22 GMT  
		Size: 6.4 MB (6410234 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54f4a4fa2a8c4f7d57746c6e9e061682eb70b2191cce975516f2585ac36a1024`  
		Last Modified: Sat, 19 Oct 2024 05:58:22 GMT  
		Size: 14.6 KB (14610 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.30-alpine`

```console
$ docker pull telegraf@sha256:48b16cd7118777f0f1bfbf1646e1361f86617940bf8be0f78a8f38b38f559d38
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.30-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:d1fe88cff6f1f352b943b18a696b82f02f51b0c6cf6ef6f0f8ac06767c1aba32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.6 MB (68637840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad5e575a5e5a70553ec5d58132072558a1f2a4f93eacf2c851b9e87044e8531d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Mon, 28 Oct 2024 22:11:39 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
ENV TELEGRAF_VERSION=1.30.3
# Mon, 28 Oct 2024 22:11:39 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 28 Oct 2024 22:11:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Oct 2024 22:11:39 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f26c83f64ca1456198e770c389b38e5bf8c9e65836f4618a54a974e411188638`  
		Last Modified: Tue, 12 Nov 2024 02:21:05 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:974bbb85e144ad54cca7dc47f8bb42c769d38b56729a078fe026f811498268fb`  
		Last Modified: Tue, 12 Nov 2024 02:21:05 GMT  
		Size: 2.4 MB (2444834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d45ebb412048f7665bc09f61be06e91c3bba493788205109742894989302ec21`  
		Last Modified: Tue, 12 Nov 2024 02:21:06 GMT  
		Size: 62.6 MB (62568494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c70ab24ace3340ea55807f383962096485bd4b7d97294db29be4974593a11997`  
		Last Modified: Tue, 12 Nov 2024 02:21:05 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.30-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:4d1f2b2431200e7ea650df7ca3503ac7c776c116468c7d8b4c24cd3a1f22191e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1071366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:308834af1822db8b6728b0a622602d025641dc2c956b8ba8ccbdb6b9575572c7`

```dockerfile
```

-	Layers:
	-	`sha256:a39b74605b0de8f0c7dffc4a9341b56a5e25959232ded52dda115dd0da436a6e`  
		Last Modified: Tue, 12 Nov 2024 02:21:05 GMT  
		Size: 1.1 MB (1056405 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4fdfb4fd65fb42e643e34090b6fd02f342d53162daa4374e0ab66ebc5132de74`  
		Last Modified: Tue, 12 Nov 2024 02:21:05 GMT  
		Size: 15.0 KB (14961 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.30-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:aa8942ae1c5553ceac2e04ea1f21939261f63205249a62e2b3c04e3fb7bc14d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63540183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06a25b84a9e7b00a3db8f63063a3158b5d7fa3b6a45e1e7591e1b592c9ebfb4c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Mon, 28 Oct 2024 22:11:39 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
ENV TELEGRAF_VERSION=1.30.3
# Mon, 28 Oct 2024 22:11:39 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 28 Oct 2024 22:11:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Oct 2024 22:11:39 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9de63ce930d0f77f6402e61ee732ad4f784c59fd26df033bb1b7d6a0b87a2f4`  
		Last Modified: Tue, 12 Nov 2024 13:17:18 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:848dadffeaafa841326acf8c33573919df8ff222e2680607f7d10bb804a23d6c`  
		Last Modified: Wed, 13 Nov 2024 00:44:18 GMT  
		Size: 2.5 MB (2530663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fda24d53e12767920ea59e84b53c365e01b3b29f4988df7f2e8a669b5411862`  
		Last Modified: Wed, 13 Nov 2024 00:44:20 GMT  
		Size: 56.9 MB (56921187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8db666f85d9bf6e47b56332381281f973a63eb2e75f216da6c7de966ab6b3ccf`  
		Last Modified: Wed, 13 Nov 2024 00:44:18 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.30-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:8c63a415f442175dc0ac4d407d716e7e15c2839daedbba06a0cf1c5fbba42d70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1066346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f023ae63c182c047e5e162572d71a566b408affba4667ae76c4458764d659e63`

```dockerfile
```

-	Layers:
	-	`sha256:ca8e82b4ad234fde2144ac752875f5f4e2624ca01398237dd917456fa3876a45`  
		Last Modified: Wed, 13 Nov 2024 00:44:18 GMT  
		Size: 1.1 MB (1051275 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e884945c1eedf9b90e6c05f951a12c4509d27fa03085eababc577b6919684f86`  
		Last Modified: Wed, 13 Nov 2024 00:44:18 GMT  
		Size: 15.1 KB (15071 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.30.3`

```console
$ docker pull telegraf@sha256:991dc94641004ef6125e685bb67a8aa4e8b9fe39af16259d97a4943331602ca1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.30.3` - linux; amd64

```console
$ docker pull telegraf@sha256:26c993c5f082e6633a79fd083b0b38967de5b24cd930b2d742887d7fa03ddad7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.4 MB (155350936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70b1373ef2b8da66c0cfe9d58ae2e61d6f1280b5528300791a3c29bb4dd86d95`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
ENV TELEGRAF_VERSION=1.30.3
# Mon, 28 Oct 2024 22:11:39 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 28 Oct 2024 22:11:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Oct 2024 22:11:39 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:b2b31b28ee3c96e96195c754f8679f690db4b18e475682d716122016ef056f39`  
		Last Modified: Tue, 12 Nov 2024 00:55:23 GMT  
		Size: 49.6 MB (49575695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3cc7b6f04730c072f8b292917e0d95bb886096a2b2b1781196170965161cd27`  
		Last Modified: Tue, 12 Nov 2024 02:38:12 GMT  
		Size: 24.1 MB (24058346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad4cea0931f00f3874f45e2d5d38a115308f2056139190ff3003741afbfd9e50`  
		Last Modified: Tue, 12 Nov 2024 03:16:41 GMT  
		Size: 18.9 MB (18948068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63fa33d58f88292792c7e2d328aa6fcd59f485dd738b74ffdf7b286d1d2c15de`  
		Last Modified: Tue, 12 Nov 2024 03:16:41 GMT  
		Size: 1.8 KB (1782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c1d1a7d397fc3e016436dc9e2d9d980a917f7472111cd5bc501534cd13cd744`  
		Last Modified: Tue, 12 Nov 2024 03:16:42 GMT  
		Size: 62.8 MB (62766422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c29a82085d128f1e58771860d33ec2473b3296e7251cccdf648d8afd90e08c2d`  
		Last Modified: Tue, 12 Nov 2024 03:16:41 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.30.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:29a6c70301633a0dc0b108028361cc82003314bac59f9ee49ccbe99011ba9a56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6424853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cbb55846b6b50d56a79b604c3365352499f06e552fc38a818858e5d962c1081`

```dockerfile
```

-	Layers:
	-	`sha256:5ed05627e8f4010ce1ab4ab418e71d38bef57c9ab660078a2e200a0e3c3153df`  
		Last Modified: Tue, 12 Nov 2024 03:16:41 GMT  
		Size: 6.4 MB (6410383 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d28aec7ff055a76b5f12bdd01c1421b47c475df6431955096b5315e2f479c00`  
		Last Modified: Tue, 12 Nov 2024 03:16:41 GMT  
		Size: 14.5 KB (14470 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.30.3` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:1aec78acd484e3052a3b744aa4f506524919a9da02fc1433e8b4c0c4df5929c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.0 MB (143045409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9e3cf41e7ffdc46a369d820c9892c0398ad9c39b7f4f3bbb63bf1661b4676b6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:2ce9af7b514320ba230746cbff4f2f2e2b8d4a62ac035ebbe6575e17544f6416 in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
ENV TELEGRAF_VERSION=1.30.3
# Mon, 07 Oct 2024 21:02:29 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 07 Oct 2024 21:02:29 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 07 Oct 2024 21:02:29 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:b683f99b4cdeb3cb4e487b268b3949647168e16d00d07e004e03af92331dbfed`  
		Last Modified: Thu, 17 Oct 2024 03:06:32 GMT  
		Size: 45.1 MB (45147940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47b7fd5031c50fee563f16760ae6e5334672d6c9ba07d159b9e3a17a3b62011`  
		Last Modified: Sat, 19 Oct 2024 00:56:10 GMT  
		Size: 22.0 MB (21957404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2247d3273aa1d92c25210b647da389293f770c7463e0680590bba2707a00d4f`  
		Last Modified: Sat, 19 Oct 2024 07:17:52 GMT  
		Size: 17.7 MB (17724956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:431a3580592e7869e0e9a687eeb734ecbf61aa4864384cb91bf7c24aee3a5b0a`  
		Last Modified: Sat, 19 Oct 2024 07:17:51 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0d2306cc2f9dc432bdab9577e71740b948af00d4db1eb08443a0547eca2e52a`  
		Last Modified: Sat, 19 Oct 2024 07:17:54 GMT  
		Size: 58.2 MB (58212698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb81901359f5d7c38fe327abcc66538f8e4bbe770e9fdbc72048a59bd935fc94`  
		Last Modified: Sat, 19 Oct 2024 07:17:51 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.30.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:a04be35abee58909c3d42aced2d9147ca36e1a4e096534266a96b0d2acfcf695
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6419536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ade3393bc72761ef0b9812ba99ab201b31ea335dce0f4179478937d6a830cc27`

```dockerfile
```

-	Layers:
	-	`sha256:761d0fbf418de95f0bf4b3d8831e7c0247231173b138cb38369af68e028d09aa`  
		Last Modified: Sat, 19 Oct 2024 07:17:52 GMT  
		Size: 6.4 MB (6404950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb0764e2e8db77601eaa76a040320d4088bea4d5b360d5b3af5469ddfb0053ac`  
		Last Modified: Sat, 19 Oct 2024 07:17:51 GMT  
		Size: 14.6 KB (14586 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.30.3` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:e15f4ecf24e9acd0d799b33dfe2655209cce1a2329ef58b7ea340d6b47526440
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.2 MB (149174941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68ee0153e92a6e7016af48b545c85b7478ac2c16331e327c3b5ffc11460a7058`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:1df819221542e236e104deb2624ffe4efd79382aed25b3ab20088becaeadad31 in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
ENV TELEGRAF_VERSION=1.30.3
# Mon, 07 Oct 2024 21:02:29 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 07 Oct 2024 21:02:29 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 07 Oct 2024 21:02:29 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:c1e0ef7b956a07c7b090256aa16cbb0550a34d0625d1d23c5b1a76e92a58d01e`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 49.6 MB (49584978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b894d63c771a6056bc65ff25192b251413259ba7d160b0076f0f5d7975dc39`  
		Last Modified: Sat, 19 Oct 2024 01:10:43 GMT  
		Size: 23.6 MB (23593834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c997025d65b9a3a17af2a5da355e59ddaef61afc5603e6e4f3d8c348d5dee2e2`  
		Last Modified: Sat, 19 Oct 2024 05:58:23 GMT  
		Size: 18.9 MB (18870445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3541e233720a537128c65519a803fff6e89bcae5e59f21c04e1e51e762996f72`  
		Last Modified: Sat, 19 Oct 2024 05:58:22 GMT  
		Size: 1.8 KB (1780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b91266b6b4b069749e7b9cfe1bb730c4ecfdcfca9f33b816b9e2f0c17f10ea15`  
		Last Modified: Sat, 19 Oct 2024 05:58:24 GMT  
		Size: 57.1 MB (57123282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d87c4bdfef8f024628957e3162ad4436c4d57fb0e5040c1e3a5970fbc4c23765`  
		Last Modified: Sat, 19 Oct 2024 05:58:22 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.30.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:112ebaf7d621c726e72b5cb30a87e70283e1615524cf0c1ee94c1df9ba4a6b8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6424844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afc917b77a06f4ce84e84f3a352332a56c87ccbecb7fadb540e51ac5ca6f6cce`

```dockerfile
```

-	Layers:
	-	`sha256:8024b92a362069ab5c8cdbe2cdfe57d14579b8365e3e06d0e1968917732bd2a0`  
		Last Modified: Sat, 19 Oct 2024 05:58:22 GMT  
		Size: 6.4 MB (6410234 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54f4a4fa2a8c4f7d57746c6e9e061682eb70b2191cce975516f2585ac36a1024`  
		Last Modified: Sat, 19 Oct 2024 05:58:22 GMT  
		Size: 14.6 KB (14610 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.30.3-alpine`

```console
$ docker pull telegraf@sha256:48b16cd7118777f0f1bfbf1646e1361f86617940bf8be0f78a8f38b38f559d38
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.30.3-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:d1fe88cff6f1f352b943b18a696b82f02f51b0c6cf6ef6f0f8ac06767c1aba32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.6 MB (68637840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad5e575a5e5a70553ec5d58132072558a1f2a4f93eacf2c851b9e87044e8531d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Mon, 28 Oct 2024 22:11:39 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
ENV TELEGRAF_VERSION=1.30.3
# Mon, 28 Oct 2024 22:11:39 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 28 Oct 2024 22:11:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Oct 2024 22:11:39 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f26c83f64ca1456198e770c389b38e5bf8c9e65836f4618a54a974e411188638`  
		Last Modified: Tue, 12 Nov 2024 02:21:05 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:974bbb85e144ad54cca7dc47f8bb42c769d38b56729a078fe026f811498268fb`  
		Last Modified: Tue, 12 Nov 2024 02:21:05 GMT  
		Size: 2.4 MB (2444834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d45ebb412048f7665bc09f61be06e91c3bba493788205109742894989302ec21`  
		Last Modified: Tue, 12 Nov 2024 02:21:06 GMT  
		Size: 62.6 MB (62568494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c70ab24ace3340ea55807f383962096485bd4b7d97294db29be4974593a11997`  
		Last Modified: Tue, 12 Nov 2024 02:21:05 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.30.3-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:4d1f2b2431200e7ea650df7ca3503ac7c776c116468c7d8b4c24cd3a1f22191e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1071366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:308834af1822db8b6728b0a622602d025641dc2c956b8ba8ccbdb6b9575572c7`

```dockerfile
```

-	Layers:
	-	`sha256:a39b74605b0de8f0c7dffc4a9341b56a5e25959232ded52dda115dd0da436a6e`  
		Last Modified: Tue, 12 Nov 2024 02:21:05 GMT  
		Size: 1.1 MB (1056405 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4fdfb4fd65fb42e643e34090b6fd02f342d53162daa4374e0ab66ebc5132de74`  
		Last Modified: Tue, 12 Nov 2024 02:21:05 GMT  
		Size: 15.0 KB (14961 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.30.3-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:aa8942ae1c5553ceac2e04ea1f21939261f63205249a62e2b3c04e3fb7bc14d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63540183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06a25b84a9e7b00a3db8f63063a3158b5d7fa3b6a45e1e7591e1b592c9ebfb4c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Mon, 28 Oct 2024 22:11:39 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
ENV TELEGRAF_VERSION=1.30.3
# Mon, 28 Oct 2024 22:11:39 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 28 Oct 2024 22:11:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Oct 2024 22:11:39 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9de63ce930d0f77f6402e61ee732ad4f784c59fd26df033bb1b7d6a0b87a2f4`  
		Last Modified: Tue, 12 Nov 2024 13:17:18 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:848dadffeaafa841326acf8c33573919df8ff222e2680607f7d10bb804a23d6c`  
		Last Modified: Wed, 13 Nov 2024 00:44:18 GMT  
		Size: 2.5 MB (2530663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fda24d53e12767920ea59e84b53c365e01b3b29f4988df7f2e8a669b5411862`  
		Last Modified: Wed, 13 Nov 2024 00:44:20 GMT  
		Size: 56.9 MB (56921187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8db666f85d9bf6e47b56332381281f973a63eb2e75f216da6c7de966ab6b3ccf`  
		Last Modified: Wed, 13 Nov 2024 00:44:18 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.30.3-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:8c63a415f442175dc0ac4d407d716e7e15c2839daedbba06a0cf1c5fbba42d70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1066346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f023ae63c182c047e5e162572d71a566b408affba4667ae76c4458764d659e63`

```dockerfile
```

-	Layers:
	-	`sha256:ca8e82b4ad234fde2144ac752875f5f4e2624ca01398237dd917456fa3876a45`  
		Last Modified: Wed, 13 Nov 2024 00:44:18 GMT  
		Size: 1.1 MB (1051275 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e884945c1eedf9b90e6c05f951a12c4509d27fa03085eababc577b6919684f86`  
		Last Modified: Wed, 13 Nov 2024 00:44:18 GMT  
		Size: 15.1 KB (15071 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.31`

```console
$ docker pull telegraf@sha256:045aafd4dd9b9af284b8556848c42f078f227cc38e963a4287fb36154838d7f6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.31` - linux; amd64

```console
$ docker pull telegraf@sha256:3b943303efbe657cd36be0ef1c9559539ce8c2b036081b65763fbe06616f64ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.9 MB (158869814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01de6457af670794ba32f7566f26e4c61f158ce46ebba0d28835993866e128e3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
ENV TELEGRAF_VERSION=1.31.3
# Mon, 28 Oct 2024 22:11:39 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 28 Oct 2024 22:11:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Oct 2024 22:11:39 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:b2b31b28ee3c96e96195c754f8679f690db4b18e475682d716122016ef056f39`  
		Last Modified: Tue, 12 Nov 2024 00:55:23 GMT  
		Size: 49.6 MB (49575695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3cc7b6f04730c072f8b292917e0d95bb886096a2b2b1781196170965161cd27`  
		Last Modified: Tue, 12 Nov 2024 02:38:12 GMT  
		Size: 24.1 MB (24058346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e8ac371f8f6b900f6816a3f3d5cf475581282536b290f9f56a144ebdc7efa47`  
		Last Modified: Tue, 12 Nov 2024 03:16:26 GMT  
		Size: 18.9 MB (18947946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c5955811c58047faf2b5f6273d3eb53a67c23a3f88e1be68006f165beeeeaa9`  
		Last Modified: Tue, 12 Nov 2024 03:16:26 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce1d1ddb522742bcec3581546c0c3f07a01dc1f06a991e58a1698c414883ee10`  
		Last Modified: Tue, 12 Nov 2024 03:16:28 GMT  
		Size: 66.3 MB (66285433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf32759841303be4847b388926fbd63c06ade86fdd4685861d9cd5191ac3848a`  
		Last Modified: Tue, 12 Nov 2024 03:16:26 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31` - unknown; unknown

```console
$ docker pull telegraf@sha256:aebc05fc8f913627950f6f3f2da7a29a65e82df43c5de9e73e46124c593ca73c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6433061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:146110216602f9d8df59808898a14358377ac3a60025e40ad791710780261655`

```dockerfile
```

-	Layers:
	-	`sha256:ab24cdf8cd6e4da8d19551df6ba5f96fe0757192ac082c0b1ddff14a3197e96b`  
		Last Modified: Tue, 12 Nov 2024 03:16:26 GMT  
		Size: 6.4 MB (6418591 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7ef7c4c09c09360b6e64da89f2b45319a58df07350cd0caccf6b4fed8b11ddd`  
		Last Modified: Tue, 12 Nov 2024 03:16:26 GMT  
		Size: 14.5 KB (14470 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.31` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:a1f078b55f9f610ad5846395121f8d60f6c31fb7a8092e765f6d4db750c743a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.5 MB (146505020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dc155a80eba3d2e0e66066a2ea4ba35e3f0bdebd523c802855c2681d88f4222`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:2ce9af7b514320ba230746cbff4f2f2e2b8d4a62ac035ebbe6575e17544f6416 in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
ENV TELEGRAF_VERSION=1.31.3
# Mon, 07 Oct 2024 21:02:29 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 07 Oct 2024 21:02:29 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 07 Oct 2024 21:02:29 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:b683f99b4cdeb3cb4e487b268b3949647168e16d00d07e004e03af92331dbfed`  
		Last Modified: Thu, 17 Oct 2024 03:06:32 GMT  
		Size: 45.1 MB (45147940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47b7fd5031c50fee563f16760ae6e5334672d6c9ba07d159b9e3a17a3b62011`  
		Last Modified: Sat, 19 Oct 2024 00:56:10 GMT  
		Size: 22.0 MB (21957404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2247d3273aa1d92c25210b647da389293f770c7463e0680590bba2707a00d4f`  
		Last Modified: Sat, 19 Oct 2024 07:17:52 GMT  
		Size: 17.7 MB (17724956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:431a3580592e7869e0e9a687eeb734ecbf61aa4864384cb91bf7c24aee3a5b0a`  
		Last Modified: Sat, 19 Oct 2024 07:17:51 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eacb03abf0c7c48a71fac48e96e9fb38faf180c40f09354e23071882ad24bb7`  
		Last Modified: Sat, 19 Oct 2024 07:18:47 GMT  
		Size: 61.7 MB (61672311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a07573c18686fe6f8cdb08b70ad829f06e91f077d95acb7a82cadadcfd3e5ce9`  
		Last Modified: Sat, 19 Oct 2024 07:18:45 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31` - unknown; unknown

```console
$ docker pull telegraf@sha256:5d74cb512d2619f69c3f63bfe9e759d3081100e6e4c546343cc4ebaba8e757fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6428539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6beecdecb74e8d6019ebb06c9e34c2e00d6b4f356b6e908614a52c2ff5c2e86`

```dockerfile
```

-	Layers:
	-	`sha256:8e2bc141fe377ba66db0533d0c54136a71ec022c574f6540f4cf334d06ecec14`  
		Last Modified: Sat, 19 Oct 2024 07:18:46 GMT  
		Size: 6.4 MB (6413955 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01b2b73c2f10326706992aae9c3de960b27cfb07a2f91ced75197a04ebbb769d`  
		Last Modified: Sat, 19 Oct 2024 07:18:45 GMT  
		Size: 14.6 KB (14584 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.31` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:7243bd28d2fc52162e63d17c1a3da13033a0581c9346803c5434c2c9b55b1a31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.4 MB (152429478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37ee2e306a81782ddda358f26d15807b7b9c15c9fe6b26691ad431801db79687`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:1df819221542e236e104deb2624ffe4efd79382aed25b3ab20088becaeadad31 in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
ENV TELEGRAF_VERSION=1.31.3
# Mon, 07 Oct 2024 21:02:29 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 07 Oct 2024 21:02:29 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 07 Oct 2024 21:02:29 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:c1e0ef7b956a07c7b090256aa16cbb0550a34d0625d1d23c5b1a76e92a58d01e`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 49.6 MB (49584978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b894d63c771a6056bc65ff25192b251413259ba7d160b0076f0f5d7975dc39`  
		Last Modified: Sat, 19 Oct 2024 01:10:43 GMT  
		Size: 23.6 MB (23593834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c997025d65b9a3a17af2a5da355e59ddaef61afc5603e6e4f3d8c348d5dee2e2`  
		Last Modified: Sat, 19 Oct 2024 05:58:23 GMT  
		Size: 18.9 MB (18870445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3541e233720a537128c65519a803fff6e89bcae5e59f21c04e1e51e762996f72`  
		Last Modified: Sat, 19 Oct 2024 05:58:22 GMT  
		Size: 1.8 KB (1780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe15e9c7710d70a178beb6ed98ba9e666ffd3580ad8e46febf1b90bb762a4803`  
		Last Modified: Sat, 19 Oct 2024 05:59:10 GMT  
		Size: 60.4 MB (60377818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e2322d8dc04ab6e646d0172e015614584248b876c90fa93dc2c397cc6a41405`  
		Last Modified: Sat, 19 Oct 2024 05:59:08 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31` - unknown; unknown

```console
$ docker pull telegraf@sha256:1f27329d7ea64281bf1adc2d1fc4f1aaef16af5304fc5d3fab12adbf0e651812
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6434643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8451d90d88989cbf130586d38cf79ea9ecdac03bbf610b50dd9ae3fd99c3a7bf`

```dockerfile
```

-	Layers:
	-	`sha256:c0ce5698d7c8fa7a6dd546ca94f7a72c2388bf409df4b8e23aaa2a5631b78de6`  
		Last Modified: Sat, 19 Oct 2024 05:59:09 GMT  
		Size: 6.4 MB (6420034 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:574153a67c23c0bfa30b4e1fd1c808e0a4921c304ced1ff0cddc66db662ef3ff`  
		Last Modified: Sat, 19 Oct 2024 05:59:08 GMT  
		Size: 14.6 KB (14609 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.31-alpine`

```console
$ docker pull telegraf@sha256:de67a108f127bbfd06b21b18fe8bba745b71b0e1e4f743a5e06ca45a705f42a8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.31-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:997da12fb34bf904334e39d911327f45ef79d2a498bc71c547e8d5d70e1e0f62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.1 MB (72149519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d731e4354684f4ef6b4d3e92a4e45008a4deb236170c5f0a349ee3416002dde`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Mon, 28 Oct 2024 22:11:39 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
ENV TELEGRAF_VERSION=1.31.3
# Mon, 28 Oct 2024 22:11:39 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 28 Oct 2024 22:11:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Oct 2024 22:11:39 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16f10048322eb86f2be1b7699a5c82453c4c117017d59212b59520756810207c`  
		Last Modified: Tue, 12 Nov 2024 02:21:18 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddf3378dfe0cc506adaa827bc20236dda2e82ec4b94cb866c503da70171e15c9`  
		Last Modified: Tue, 12 Nov 2024 02:21:18 GMT  
		Size: 2.4 MB (2444831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36d9dde8a359ac2194bdd2c1b777d7406616290d0020cc51a94a759f0ff42479`  
		Last Modified: Tue, 12 Nov 2024 02:21:18 GMT  
		Size: 66.1 MB (66080176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86878befd798f41f972e38cf31f2ad1250c4660288a9574685a05d438f0c41ec`  
		Last Modified: Tue, 12 Nov 2024 02:21:17 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:0f5d76963c8dedbac66a6c0c7490a05a1a2e628a1a60395bab2df9c350343fb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1079572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0749f1205673d1a6b749b89096eae616216f940a6b4a468d12e7e2d5c950bdd9`

```dockerfile
```

-	Layers:
	-	`sha256:f6021eb66e288afca40a3de988cb4b331eab3569a6cf828c4b2c64257f06557f`  
		Last Modified: Tue, 12 Nov 2024 02:21:18 GMT  
		Size: 1.1 MB (1064613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc8d6cf96bf0c4c71fd14e16c3f7a3b4c0a73536343040b53c476c22e16d1203`  
		Last Modified: Tue, 12 Nov 2024 02:21:17 GMT  
		Size: 15.0 KB (14959 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.31-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:c721817221b9cc330049e20dc9cf632918644881181202c11ab1ef5669e0f054
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.8 MB (66790689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52ecbb2893d24b9033fa9dbf9bf0c0fc5ead7044e742fc8801c1163854e6bc85`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Mon, 28 Oct 2024 22:11:39 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
ENV TELEGRAF_VERSION=1.31.3
# Mon, 28 Oct 2024 22:11:39 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 28 Oct 2024 22:11:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Oct 2024 22:11:39 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9de63ce930d0f77f6402e61ee732ad4f784c59fd26df033bb1b7d6a0b87a2f4`  
		Last Modified: Tue, 12 Nov 2024 13:17:18 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:848dadffeaafa841326acf8c33573919df8ff222e2680607f7d10bb804a23d6c`  
		Last Modified: Wed, 13 Nov 2024 00:44:18 GMT  
		Size: 2.5 MB (2530663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c165eccfb6fb22936f132b38db1bea94249c4f9025902071816f681d45278592`  
		Last Modified: Wed, 13 Nov 2024 00:44:58 GMT  
		Size: 60.2 MB (60171693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f25aa3692cb281849fa0eba2cb21828fd6ad1c13fa61aaec973cde6d98d95d`  
		Last Modified: Wed, 13 Nov 2024 00:44:56 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:3c1199bc5e2229bba0fa164cb749ad110ae8ccfaebe006a2f0b23f770c5e1823
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1076145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89563d9bd0aa15d8dc6e06421e37cb9040f7ff3e1cee8e2ed0852ff7977231ce`

```dockerfile
```

-	Layers:
	-	`sha256:e91298accb6ca3e23bd891af5501a0f171f772039e4cfdcea12b9c71bbac032a`  
		Last Modified: Wed, 13 Nov 2024 00:44:56 GMT  
		Size: 1.1 MB (1061075 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c48f3921a2b1ca085f8a80fe529e5b99ce2fe7915122f7539650b0150864970c`  
		Last Modified: Wed, 13 Nov 2024 00:44:56 GMT  
		Size: 15.1 KB (15070 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.31.3`

```console
$ docker pull telegraf@sha256:045aafd4dd9b9af284b8556848c42f078f227cc38e963a4287fb36154838d7f6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.31.3` - linux; amd64

```console
$ docker pull telegraf@sha256:3b943303efbe657cd36be0ef1c9559539ce8c2b036081b65763fbe06616f64ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.9 MB (158869814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01de6457af670794ba32f7566f26e4c61f158ce46ebba0d28835993866e128e3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
ENV TELEGRAF_VERSION=1.31.3
# Mon, 28 Oct 2024 22:11:39 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 28 Oct 2024 22:11:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Oct 2024 22:11:39 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:b2b31b28ee3c96e96195c754f8679f690db4b18e475682d716122016ef056f39`  
		Last Modified: Tue, 12 Nov 2024 00:55:23 GMT  
		Size: 49.6 MB (49575695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3cc7b6f04730c072f8b292917e0d95bb886096a2b2b1781196170965161cd27`  
		Last Modified: Tue, 12 Nov 2024 02:38:12 GMT  
		Size: 24.1 MB (24058346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e8ac371f8f6b900f6816a3f3d5cf475581282536b290f9f56a144ebdc7efa47`  
		Last Modified: Tue, 12 Nov 2024 03:16:26 GMT  
		Size: 18.9 MB (18947946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c5955811c58047faf2b5f6273d3eb53a67c23a3f88e1be68006f165beeeeaa9`  
		Last Modified: Tue, 12 Nov 2024 03:16:26 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce1d1ddb522742bcec3581546c0c3f07a01dc1f06a991e58a1698c414883ee10`  
		Last Modified: Tue, 12 Nov 2024 03:16:28 GMT  
		Size: 66.3 MB (66285433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf32759841303be4847b388926fbd63c06ade86fdd4685861d9cd5191ac3848a`  
		Last Modified: Tue, 12 Nov 2024 03:16:26 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:aebc05fc8f913627950f6f3f2da7a29a65e82df43c5de9e73e46124c593ca73c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6433061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:146110216602f9d8df59808898a14358377ac3a60025e40ad791710780261655`

```dockerfile
```

-	Layers:
	-	`sha256:ab24cdf8cd6e4da8d19551df6ba5f96fe0757192ac082c0b1ddff14a3197e96b`  
		Last Modified: Tue, 12 Nov 2024 03:16:26 GMT  
		Size: 6.4 MB (6418591 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7ef7c4c09c09360b6e64da89f2b45319a58df07350cd0caccf6b4fed8b11ddd`  
		Last Modified: Tue, 12 Nov 2024 03:16:26 GMT  
		Size: 14.5 KB (14470 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.31.3` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:a1f078b55f9f610ad5846395121f8d60f6c31fb7a8092e765f6d4db750c743a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.5 MB (146505020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dc155a80eba3d2e0e66066a2ea4ba35e3f0bdebd523c802855c2681d88f4222`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:2ce9af7b514320ba230746cbff4f2f2e2b8d4a62ac035ebbe6575e17544f6416 in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
ENV TELEGRAF_VERSION=1.31.3
# Mon, 07 Oct 2024 21:02:29 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 07 Oct 2024 21:02:29 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 07 Oct 2024 21:02:29 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:b683f99b4cdeb3cb4e487b268b3949647168e16d00d07e004e03af92331dbfed`  
		Last Modified: Thu, 17 Oct 2024 03:06:32 GMT  
		Size: 45.1 MB (45147940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47b7fd5031c50fee563f16760ae6e5334672d6c9ba07d159b9e3a17a3b62011`  
		Last Modified: Sat, 19 Oct 2024 00:56:10 GMT  
		Size: 22.0 MB (21957404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2247d3273aa1d92c25210b647da389293f770c7463e0680590bba2707a00d4f`  
		Last Modified: Sat, 19 Oct 2024 07:17:52 GMT  
		Size: 17.7 MB (17724956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:431a3580592e7869e0e9a687eeb734ecbf61aa4864384cb91bf7c24aee3a5b0a`  
		Last Modified: Sat, 19 Oct 2024 07:17:51 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eacb03abf0c7c48a71fac48e96e9fb38faf180c40f09354e23071882ad24bb7`  
		Last Modified: Sat, 19 Oct 2024 07:18:47 GMT  
		Size: 61.7 MB (61672311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a07573c18686fe6f8cdb08b70ad829f06e91f077d95acb7a82cadadcfd3e5ce9`  
		Last Modified: Sat, 19 Oct 2024 07:18:45 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:5d74cb512d2619f69c3f63bfe9e759d3081100e6e4c546343cc4ebaba8e757fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6428539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6beecdecb74e8d6019ebb06c9e34c2e00d6b4f356b6e908614a52c2ff5c2e86`

```dockerfile
```

-	Layers:
	-	`sha256:8e2bc141fe377ba66db0533d0c54136a71ec022c574f6540f4cf334d06ecec14`  
		Last Modified: Sat, 19 Oct 2024 07:18:46 GMT  
		Size: 6.4 MB (6413955 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01b2b73c2f10326706992aae9c3de960b27cfb07a2f91ced75197a04ebbb769d`  
		Last Modified: Sat, 19 Oct 2024 07:18:45 GMT  
		Size: 14.6 KB (14584 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.31.3` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:7243bd28d2fc52162e63d17c1a3da13033a0581c9346803c5434c2c9b55b1a31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.4 MB (152429478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37ee2e306a81782ddda358f26d15807b7b9c15c9fe6b26691ad431801db79687`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:1df819221542e236e104deb2624ffe4efd79382aed25b3ab20088becaeadad31 in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
ENV TELEGRAF_VERSION=1.31.3
# Mon, 07 Oct 2024 21:02:29 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 07 Oct 2024 21:02:29 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 07 Oct 2024 21:02:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 07 Oct 2024 21:02:29 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:c1e0ef7b956a07c7b090256aa16cbb0550a34d0625d1d23c5b1a76e92a58d01e`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 49.6 MB (49584978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b894d63c771a6056bc65ff25192b251413259ba7d160b0076f0f5d7975dc39`  
		Last Modified: Sat, 19 Oct 2024 01:10:43 GMT  
		Size: 23.6 MB (23593834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c997025d65b9a3a17af2a5da355e59ddaef61afc5603e6e4f3d8c348d5dee2e2`  
		Last Modified: Sat, 19 Oct 2024 05:58:23 GMT  
		Size: 18.9 MB (18870445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3541e233720a537128c65519a803fff6e89bcae5e59f21c04e1e51e762996f72`  
		Last Modified: Sat, 19 Oct 2024 05:58:22 GMT  
		Size: 1.8 KB (1780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe15e9c7710d70a178beb6ed98ba9e666ffd3580ad8e46febf1b90bb762a4803`  
		Last Modified: Sat, 19 Oct 2024 05:59:10 GMT  
		Size: 60.4 MB (60377818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e2322d8dc04ab6e646d0172e015614584248b876c90fa93dc2c397cc6a41405`  
		Last Modified: Sat, 19 Oct 2024 05:59:08 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:1f27329d7ea64281bf1adc2d1fc4f1aaef16af5304fc5d3fab12adbf0e651812
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6434643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8451d90d88989cbf130586d38cf79ea9ecdac03bbf610b50dd9ae3fd99c3a7bf`

```dockerfile
```

-	Layers:
	-	`sha256:c0ce5698d7c8fa7a6dd546ca94f7a72c2388bf409df4b8e23aaa2a5631b78de6`  
		Last Modified: Sat, 19 Oct 2024 05:59:09 GMT  
		Size: 6.4 MB (6420034 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:574153a67c23c0bfa30b4e1fd1c808e0a4921c304ced1ff0cddc66db662ef3ff`  
		Last Modified: Sat, 19 Oct 2024 05:59:08 GMT  
		Size: 14.6 KB (14609 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.31.3-alpine`

```console
$ docker pull telegraf@sha256:de67a108f127bbfd06b21b18fe8bba745b71b0e1e4f743a5e06ca45a705f42a8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.31.3-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:997da12fb34bf904334e39d911327f45ef79d2a498bc71c547e8d5d70e1e0f62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.1 MB (72149519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d731e4354684f4ef6b4d3e92a4e45008a4deb236170c5f0a349ee3416002dde`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Mon, 28 Oct 2024 22:11:39 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
ENV TELEGRAF_VERSION=1.31.3
# Mon, 28 Oct 2024 22:11:39 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 28 Oct 2024 22:11:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Oct 2024 22:11:39 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16f10048322eb86f2be1b7699a5c82453c4c117017d59212b59520756810207c`  
		Last Modified: Tue, 12 Nov 2024 02:21:18 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddf3378dfe0cc506adaa827bc20236dda2e82ec4b94cb866c503da70171e15c9`  
		Last Modified: Tue, 12 Nov 2024 02:21:18 GMT  
		Size: 2.4 MB (2444831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36d9dde8a359ac2194bdd2c1b777d7406616290d0020cc51a94a759f0ff42479`  
		Last Modified: Tue, 12 Nov 2024 02:21:18 GMT  
		Size: 66.1 MB (66080176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86878befd798f41f972e38cf31f2ad1250c4660288a9574685a05d438f0c41ec`  
		Last Modified: Tue, 12 Nov 2024 02:21:17 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31.3-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:0f5d76963c8dedbac66a6c0c7490a05a1a2e628a1a60395bab2df9c350343fb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1079572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0749f1205673d1a6b749b89096eae616216f940a6b4a468d12e7e2d5c950bdd9`

```dockerfile
```

-	Layers:
	-	`sha256:f6021eb66e288afca40a3de988cb4b331eab3569a6cf828c4b2c64257f06557f`  
		Last Modified: Tue, 12 Nov 2024 02:21:18 GMT  
		Size: 1.1 MB (1064613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc8d6cf96bf0c4c71fd14e16c3f7a3b4c0a73536343040b53c476c22e16d1203`  
		Last Modified: Tue, 12 Nov 2024 02:21:17 GMT  
		Size: 15.0 KB (14959 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.31.3-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:c721817221b9cc330049e20dc9cf632918644881181202c11ab1ef5669e0f054
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.8 MB (66790689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52ecbb2893d24b9033fa9dbf9bf0c0fc5ead7044e742fc8801c1163854e6bc85`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Mon, 28 Oct 2024 22:11:39 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
ENV TELEGRAF_VERSION=1.31.3
# Mon, 28 Oct 2024 22:11:39 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 28 Oct 2024 22:11:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Oct 2024 22:11:39 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9de63ce930d0f77f6402e61ee732ad4f784c59fd26df033bb1b7d6a0b87a2f4`  
		Last Modified: Tue, 12 Nov 2024 13:17:18 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:848dadffeaafa841326acf8c33573919df8ff222e2680607f7d10bb804a23d6c`  
		Last Modified: Wed, 13 Nov 2024 00:44:18 GMT  
		Size: 2.5 MB (2530663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c165eccfb6fb22936f132b38db1bea94249c4f9025902071816f681d45278592`  
		Last Modified: Wed, 13 Nov 2024 00:44:58 GMT  
		Size: 60.2 MB (60171693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f25aa3692cb281849fa0eba2cb21828fd6ad1c13fa61aaec973cde6d98d95d`  
		Last Modified: Wed, 13 Nov 2024 00:44:56 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31.3-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:3c1199bc5e2229bba0fa164cb749ad110ae8ccfaebe006a2f0b23f770c5e1823
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1076145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89563d9bd0aa15d8dc6e06421e37cb9040f7ff3e1cee8e2ed0852ff7977231ce`

```dockerfile
```

-	Layers:
	-	`sha256:e91298accb6ca3e23bd891af5501a0f171f772039e4cfdcea12b9c71bbac032a`  
		Last Modified: Wed, 13 Nov 2024 00:44:56 GMT  
		Size: 1.1 MB (1061075 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c48f3921a2b1ca085f8a80fe529e5b99ce2fe7915122f7539650b0150864970c`  
		Last Modified: Wed, 13 Nov 2024 00:44:56 GMT  
		Size: 15.1 KB (15070 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.32`

```console
$ docker pull telegraf@sha256:959da5a531eebce5db7b453234cefcb310aad55501e74ec292cb903369e3642e
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
$ docker pull telegraf@sha256:97bb1a17ef1af44642e0bc228ee635906825bf1c475a56ab0d41f20101c45380
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.6 MB (163620064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd9a1144d868b83b432312c8dad1574e02b2f5badf6cd487dd213a88737c3879`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
ENV TELEGRAF_VERSION=1.32.2
# Mon, 28 Oct 2024 22:11:39 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 28 Oct 2024 22:11:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Oct 2024 22:11:39 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:b2b31b28ee3c96e96195c754f8679f690db4b18e475682d716122016ef056f39`  
		Last Modified: Tue, 12 Nov 2024 00:55:23 GMT  
		Size: 49.6 MB (49575695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3cc7b6f04730c072f8b292917e0d95bb886096a2b2b1781196170965161cd27`  
		Last Modified: Tue, 12 Nov 2024 02:38:12 GMT  
		Size: 24.1 MB (24058346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23f2e2047df7e2f387bee7214610d85f418a2b0f212c6f1f6eaee882d6d32444`  
		Last Modified: Tue, 12 Nov 2024 03:16:25 GMT  
		Size: 18.9 MB (18948097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cec5ef2e84f55cf715952487f4871c5d31ee84c2564cc9e2ef203d3d8394caa`  
		Last Modified: Tue, 12 Nov 2024 03:16:24 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1cef6be5300fa2e27485dbc48470b500f4e54ab0bced4d651f48910c6b0732f`  
		Last Modified: Tue, 12 Nov 2024 03:16:25 GMT  
		Size: 71.0 MB (71035533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa9983172de0f034e6469bf8ec055749ecc65f496220eea36240920970de48a9`  
		Last Modified: Tue, 12 Nov 2024 03:16:24 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.32` - unknown; unknown

```console
$ docker pull telegraf@sha256:1135d2fd4d14bc36c0b43849bb61bc274df73c028d08348169e8d0c6ee6317eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6443788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ec90c2c2a09b2af14ecf643d7405caca9b8f6c7e2adc3643b090379918f496d`

```dockerfile
```

-	Layers:
	-	`sha256:2c37a1d77bf2e7d901d08bcb8dab360d7a3fe3aecfd9643d77a90e9c5ee302f5`  
		Last Modified: Tue, 12 Nov 2024 03:16:24 GMT  
		Size: 6.4 MB (6429016 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a288cd6b4b2ff7290c1a682d600723d4d9898a08f33c874a2adbb72674df2359`  
		Last Modified: Tue, 12 Nov 2024 03:16:24 GMT  
		Size: 14.8 KB (14772 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.32` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:04b6577c812070f274ce15ce928a53864314c754c9ed92f58128e7e438b906a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.6 MB (150625344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0712361ac2b8ae51dd895af739707480e7eda069cdfa26d9a868d700e6b7ae6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:2ce9af7b514320ba230746cbff4f2f2e2b8d4a62ac035ebbe6575e17544f6416 in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
ENV TELEGRAF_VERSION=1.32.2
# Mon, 28 Oct 2024 22:11:39 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 28 Oct 2024 22:11:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Oct 2024 22:11:39 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:b683f99b4cdeb3cb4e487b268b3949647168e16d00d07e004e03af92331dbfed`  
		Last Modified: Thu, 17 Oct 2024 03:06:32 GMT  
		Size: 45.1 MB (45147940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47b7fd5031c50fee563f16760ae6e5334672d6c9ba07d159b9e3a17a3b62011`  
		Last Modified: Sat, 19 Oct 2024 00:56:10 GMT  
		Size: 22.0 MB (21957404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2247d3273aa1d92c25210b647da389293f770c7463e0680590bba2707a00d4f`  
		Last Modified: Sat, 19 Oct 2024 07:17:52 GMT  
		Size: 17.7 MB (17724956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ce5b94c2bbc729b36f1960f93b7ec6c2a95a43a18ba0a45cc454eac7d35b439`  
		Last Modified: Tue, 29 Oct 2024 05:01:00 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a07021e02e5050b2cdc3717c87d8a478091d0570662e1b477e1f6117fe1dfd0`  
		Last Modified: Tue, 29 Oct 2024 05:01:03 GMT  
		Size: 65.8 MB (65792648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff0b1faddfd563f9859d102060f228af24bd0a80066b379e72421db22ed20258`  
		Last Modified: Tue, 29 Oct 2024 05:01:00 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.32` - unknown; unknown

```console
$ docker pull telegraf@sha256:8eeeb1ec87c39c5ec04315af8a61c4db05243ee1faa3bfb16ecd810c3c284dfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6439284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:925659d92f5e3ca5238d6a7bd1eebed8b16ab3ed1dac0a6552951aaaf5d4e4b9`

```dockerfile
```

-	Layers:
	-	`sha256:ea15cbd0b35cc1347a7691a7cf9cc463da340ef92fd806c3c6fcc27e46e61885`  
		Last Modified: Tue, 29 Oct 2024 05:01:01 GMT  
		Size: 6.4 MB (6424388 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83c72bd917ccd64d25ab9c7dafe3f57ffa5ae1005e77e0eeaba7533ca75d3748`  
		Last Modified: Tue, 29 Oct 2024 05:01:00 GMT  
		Size: 14.9 KB (14896 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.32` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:480e15d49e83ae340cd3bf32ff384a188f0c347d4bcf7058d2e17c3cb49b2692
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.1 MB (156113237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d8f4fe1c67ef36f0cc2f771060e1bd779cceabc69de6aac9058a88175ed5a5a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:1df819221542e236e104deb2624ffe4efd79382aed25b3ab20088becaeadad31 in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
ENV TELEGRAF_VERSION=1.32.2
# Mon, 28 Oct 2024 22:11:39 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 28 Oct 2024 22:11:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Oct 2024 22:11:39 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:c1e0ef7b956a07c7b090256aa16cbb0550a34d0625d1d23c5b1a76e92a58d01e`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 49.6 MB (49584978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b894d63c771a6056bc65ff25192b251413259ba7d160b0076f0f5d7975dc39`  
		Last Modified: Sat, 19 Oct 2024 01:10:43 GMT  
		Size: 23.6 MB (23593834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e66595c705129c5730b8646de79531481b8cb13763baf90c3b96d036ddf98362`  
		Last Modified: Tue, 29 Oct 2024 05:55:08 GMT  
		Size: 18.9 MB (18870583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13287a0c9f8805355ea97d1603870eabf63879cd2d1faaf951aca6e332365969`  
		Last Modified: Tue, 29 Oct 2024 05:55:07 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61625606c80a4ee75db903204c47c7871d8755e675080487598be4f3b6a5a293`  
		Last Modified: Tue, 29 Oct 2024 05:55:09 GMT  
		Size: 64.1 MB (64061436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e6d238d30b7987263da699d795a6c3a0b1b9e7bedd8fb538bce44ee8b666857`  
		Last Modified: Tue, 29 Oct 2024 05:55:07 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.32` - unknown; unknown

```console
$ docker pull telegraf@sha256:b0f7b05ff6169d6bfd68d03a708053f6e97f41c98e6121216c361df682825557
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6444598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc2b89afaf727aea7fad41e4f5f378a8b19e81f25e568c41e08cb3e8599c358c`

```dockerfile
```

-	Layers:
	-	`sha256:4b22cfd3bd756cac3a3294cb210cdbc94e3f36713d2810bba113c0b8a0d29e51`  
		Last Modified: Tue, 29 Oct 2024 05:55:08 GMT  
		Size: 6.4 MB (6429674 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa44f138429976d5f635ff83285f36ed44e3baee6edfb8701c9708c582e8b788`  
		Last Modified: Tue, 29 Oct 2024 05:55:07 GMT  
		Size: 14.9 KB (14924 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.32-alpine`

```console
$ docker pull telegraf@sha256:efbcdf0e7ab69d3435ea0f461fd6eafbcc78218a56967c5a4a716243fcd5b8f1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.32-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:01b02df93201a0900559932f66c19656f5bc006856431ec8a3c55a97203cf39c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.9 MB (76897588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:416722b7aa0ae6ee5acfb146710777244cac4f620f6725e4177e492e47a9d7fb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Mon, 28 Oct 2024 22:11:39 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
ENV TELEGRAF_VERSION=1.32.2
# Mon, 28 Oct 2024 22:11:39 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 28 Oct 2024 22:11:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Oct 2024 22:11:39 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b08342fb4a15566c984bd8b550d2c6c3ca140282923a7ca9052a39c3a95e2ff3`  
		Last Modified: Tue, 12 Nov 2024 02:21:26 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23fdb6caa57be3237ed9057d1c14b85ebb2c4ae7b86aaa4bc5779092c1fa0482`  
		Last Modified: Tue, 12 Nov 2024 02:21:26 GMT  
		Size: 2.4 MB (2444825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a201f0922fd7c1147588a702ba1299395744f0b8364e7a71a66b90f262d0910`  
		Last Modified: Tue, 12 Nov 2024 02:21:27 GMT  
		Size: 70.8 MB (70828250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f67f2b39b4cc830dd11c65acded3c52414fe51480f00f26734a56024513ea44b`  
		Last Modified: Tue, 12 Nov 2024 02:21:26 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.32-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:7221f00e7b8f98ce1a8efdd3d93036ad4cfc281ec78ca1ef1f3ddad30b016a25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1090301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a10b1e50777dd205f11ea45c03655998121a7cad6b392a60c9b807039a5a9f8b`

```dockerfile
```

-	Layers:
	-	`sha256:9cba6aaeefe511469c1f79c58f11721e14288103a96c03e82f457c78cdfd6400`  
		Last Modified: Tue, 12 Nov 2024 02:21:26 GMT  
		Size: 1.1 MB (1075038 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2a279eb77a8cdc7ad361069df5c5f19840f210c2a284fe28734993bfff3d32c`  
		Last Modified: Tue, 12 Nov 2024 02:21:26 GMT  
		Size: 15.3 KB (15263 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.32-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:360131f2b94e1b4e0a0a55accc6e40255089a89942b6d2d23e682dc769763f34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.5 MB (70488602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d56de21a5014770bd14dd40f920748988275ffe324b3268c2cef771f98132bf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Mon, 28 Oct 2024 22:11:39 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
ENV TELEGRAF_VERSION=1.32.2
# Mon, 28 Oct 2024 22:11:39 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 28 Oct 2024 22:11:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Oct 2024 22:11:39 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9de63ce930d0f77f6402e61ee732ad4f784c59fd26df033bb1b7d6a0b87a2f4`  
		Last Modified: Tue, 12 Nov 2024 13:17:18 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:848dadffeaafa841326acf8c33573919df8ff222e2680607f7d10bb804a23d6c`  
		Last Modified: Wed, 13 Nov 2024 00:44:18 GMT  
		Size: 2.5 MB (2530663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4383827a27cf7c8e76ae40d02da9661a942bebbe18254b9be04d527bce572de5`  
		Last Modified: Wed, 13 Nov 2024 00:45:35 GMT  
		Size: 63.9 MB (63869605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98293dc53f9f009ae42c20ca72b06e353c3ce6fbaa9fd797c46aad972fea12e7`  
		Last Modified: Wed, 13 Nov 2024 00:45:33 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.32-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:195d46a82a6c805c64e6541bef8cd6d5a323cd483df30830f7862efc8b0a850a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1086100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c86876f9c189bd84719ab02f8fa82628ea72b474c79ac492165966c68f7af49`

```dockerfile
```

-	Layers:
	-	`sha256:f52cb10165d665b2775de9498b738fbda072838abd2ba18481be987a84e09f3b`  
		Last Modified: Wed, 13 Nov 2024 00:45:33 GMT  
		Size: 1.1 MB (1070715 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:701181e3f6633764e305402b4491f468e9add860351d9ac3ebad727e1e6c9277`  
		Last Modified: Wed, 13 Nov 2024 00:45:33 GMT  
		Size: 15.4 KB (15385 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.32.2`

```console
$ docker pull telegraf@sha256:959da5a531eebce5db7b453234cefcb310aad55501e74ec292cb903369e3642e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.32.2` - linux; amd64

```console
$ docker pull telegraf@sha256:97bb1a17ef1af44642e0bc228ee635906825bf1c475a56ab0d41f20101c45380
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.6 MB (163620064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd9a1144d868b83b432312c8dad1574e02b2f5badf6cd487dd213a88737c3879`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
ENV TELEGRAF_VERSION=1.32.2
# Mon, 28 Oct 2024 22:11:39 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 28 Oct 2024 22:11:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Oct 2024 22:11:39 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:b2b31b28ee3c96e96195c754f8679f690db4b18e475682d716122016ef056f39`  
		Last Modified: Tue, 12 Nov 2024 00:55:23 GMT  
		Size: 49.6 MB (49575695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3cc7b6f04730c072f8b292917e0d95bb886096a2b2b1781196170965161cd27`  
		Last Modified: Tue, 12 Nov 2024 02:38:12 GMT  
		Size: 24.1 MB (24058346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23f2e2047df7e2f387bee7214610d85f418a2b0f212c6f1f6eaee882d6d32444`  
		Last Modified: Tue, 12 Nov 2024 03:16:25 GMT  
		Size: 18.9 MB (18948097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cec5ef2e84f55cf715952487f4871c5d31ee84c2564cc9e2ef203d3d8394caa`  
		Last Modified: Tue, 12 Nov 2024 03:16:24 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1cef6be5300fa2e27485dbc48470b500f4e54ab0bced4d651f48910c6b0732f`  
		Last Modified: Tue, 12 Nov 2024 03:16:25 GMT  
		Size: 71.0 MB (71035533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa9983172de0f034e6469bf8ec055749ecc65f496220eea36240920970de48a9`  
		Last Modified: Tue, 12 Nov 2024 03:16:24 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.32.2` - unknown; unknown

```console
$ docker pull telegraf@sha256:1135d2fd4d14bc36c0b43849bb61bc274df73c028d08348169e8d0c6ee6317eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6443788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ec90c2c2a09b2af14ecf643d7405caca9b8f6c7e2adc3643b090379918f496d`

```dockerfile
```

-	Layers:
	-	`sha256:2c37a1d77bf2e7d901d08bcb8dab360d7a3fe3aecfd9643d77a90e9c5ee302f5`  
		Last Modified: Tue, 12 Nov 2024 03:16:24 GMT  
		Size: 6.4 MB (6429016 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a288cd6b4b2ff7290c1a682d600723d4d9898a08f33c874a2adbb72674df2359`  
		Last Modified: Tue, 12 Nov 2024 03:16:24 GMT  
		Size: 14.8 KB (14772 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.32.2` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:04b6577c812070f274ce15ce928a53864314c754c9ed92f58128e7e438b906a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.6 MB (150625344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0712361ac2b8ae51dd895af739707480e7eda069cdfa26d9a868d700e6b7ae6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:2ce9af7b514320ba230746cbff4f2f2e2b8d4a62ac035ebbe6575e17544f6416 in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
ENV TELEGRAF_VERSION=1.32.2
# Mon, 28 Oct 2024 22:11:39 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 28 Oct 2024 22:11:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Oct 2024 22:11:39 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:b683f99b4cdeb3cb4e487b268b3949647168e16d00d07e004e03af92331dbfed`  
		Last Modified: Thu, 17 Oct 2024 03:06:32 GMT  
		Size: 45.1 MB (45147940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47b7fd5031c50fee563f16760ae6e5334672d6c9ba07d159b9e3a17a3b62011`  
		Last Modified: Sat, 19 Oct 2024 00:56:10 GMT  
		Size: 22.0 MB (21957404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2247d3273aa1d92c25210b647da389293f770c7463e0680590bba2707a00d4f`  
		Last Modified: Sat, 19 Oct 2024 07:17:52 GMT  
		Size: 17.7 MB (17724956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ce5b94c2bbc729b36f1960f93b7ec6c2a95a43a18ba0a45cc454eac7d35b439`  
		Last Modified: Tue, 29 Oct 2024 05:01:00 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a07021e02e5050b2cdc3717c87d8a478091d0570662e1b477e1f6117fe1dfd0`  
		Last Modified: Tue, 29 Oct 2024 05:01:03 GMT  
		Size: 65.8 MB (65792648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff0b1faddfd563f9859d102060f228af24bd0a80066b379e72421db22ed20258`  
		Last Modified: Tue, 29 Oct 2024 05:01:00 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.32.2` - unknown; unknown

```console
$ docker pull telegraf@sha256:8eeeb1ec87c39c5ec04315af8a61c4db05243ee1faa3bfb16ecd810c3c284dfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6439284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:925659d92f5e3ca5238d6a7bd1eebed8b16ab3ed1dac0a6552951aaaf5d4e4b9`

```dockerfile
```

-	Layers:
	-	`sha256:ea15cbd0b35cc1347a7691a7cf9cc463da340ef92fd806c3c6fcc27e46e61885`  
		Last Modified: Tue, 29 Oct 2024 05:01:01 GMT  
		Size: 6.4 MB (6424388 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83c72bd917ccd64d25ab9c7dafe3f57ffa5ae1005e77e0eeaba7533ca75d3748`  
		Last Modified: Tue, 29 Oct 2024 05:01:00 GMT  
		Size: 14.9 KB (14896 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.32.2` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:480e15d49e83ae340cd3bf32ff384a188f0c347d4bcf7058d2e17c3cb49b2692
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.1 MB (156113237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d8f4fe1c67ef36f0cc2f771060e1bd779cceabc69de6aac9058a88175ed5a5a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:1df819221542e236e104deb2624ffe4efd79382aed25b3ab20088becaeadad31 in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
ENV TELEGRAF_VERSION=1.32.2
# Mon, 28 Oct 2024 22:11:39 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 28 Oct 2024 22:11:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Oct 2024 22:11:39 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:c1e0ef7b956a07c7b090256aa16cbb0550a34d0625d1d23c5b1a76e92a58d01e`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 49.6 MB (49584978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b894d63c771a6056bc65ff25192b251413259ba7d160b0076f0f5d7975dc39`  
		Last Modified: Sat, 19 Oct 2024 01:10:43 GMT  
		Size: 23.6 MB (23593834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e66595c705129c5730b8646de79531481b8cb13763baf90c3b96d036ddf98362`  
		Last Modified: Tue, 29 Oct 2024 05:55:08 GMT  
		Size: 18.9 MB (18870583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13287a0c9f8805355ea97d1603870eabf63879cd2d1faaf951aca6e332365969`  
		Last Modified: Tue, 29 Oct 2024 05:55:07 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61625606c80a4ee75db903204c47c7871d8755e675080487598be4f3b6a5a293`  
		Last Modified: Tue, 29 Oct 2024 05:55:09 GMT  
		Size: 64.1 MB (64061436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e6d238d30b7987263da699d795a6c3a0b1b9e7bedd8fb538bce44ee8b666857`  
		Last Modified: Tue, 29 Oct 2024 05:55:07 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.32.2` - unknown; unknown

```console
$ docker pull telegraf@sha256:b0f7b05ff6169d6bfd68d03a708053f6e97f41c98e6121216c361df682825557
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6444598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc2b89afaf727aea7fad41e4f5f378a8b19e81f25e568c41e08cb3e8599c358c`

```dockerfile
```

-	Layers:
	-	`sha256:4b22cfd3bd756cac3a3294cb210cdbc94e3f36713d2810bba113c0b8a0d29e51`  
		Last Modified: Tue, 29 Oct 2024 05:55:08 GMT  
		Size: 6.4 MB (6429674 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa44f138429976d5f635ff83285f36ed44e3baee6edfb8701c9708c582e8b788`  
		Last Modified: Tue, 29 Oct 2024 05:55:07 GMT  
		Size: 14.9 KB (14924 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.32.2-alpine`

```console
$ docker pull telegraf@sha256:efbcdf0e7ab69d3435ea0f461fd6eafbcc78218a56967c5a4a716243fcd5b8f1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.32.2-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:01b02df93201a0900559932f66c19656f5bc006856431ec8a3c55a97203cf39c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.9 MB (76897588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:416722b7aa0ae6ee5acfb146710777244cac4f620f6725e4177e492e47a9d7fb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Mon, 28 Oct 2024 22:11:39 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
ENV TELEGRAF_VERSION=1.32.2
# Mon, 28 Oct 2024 22:11:39 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 28 Oct 2024 22:11:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Oct 2024 22:11:39 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b08342fb4a15566c984bd8b550d2c6c3ca140282923a7ca9052a39c3a95e2ff3`  
		Last Modified: Tue, 12 Nov 2024 02:21:26 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23fdb6caa57be3237ed9057d1c14b85ebb2c4ae7b86aaa4bc5779092c1fa0482`  
		Last Modified: Tue, 12 Nov 2024 02:21:26 GMT  
		Size: 2.4 MB (2444825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a201f0922fd7c1147588a702ba1299395744f0b8364e7a71a66b90f262d0910`  
		Last Modified: Tue, 12 Nov 2024 02:21:27 GMT  
		Size: 70.8 MB (70828250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f67f2b39b4cc830dd11c65acded3c52414fe51480f00f26734a56024513ea44b`  
		Last Modified: Tue, 12 Nov 2024 02:21:26 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.32.2-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:7221f00e7b8f98ce1a8efdd3d93036ad4cfc281ec78ca1ef1f3ddad30b016a25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1090301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a10b1e50777dd205f11ea45c03655998121a7cad6b392a60c9b807039a5a9f8b`

```dockerfile
```

-	Layers:
	-	`sha256:9cba6aaeefe511469c1f79c58f11721e14288103a96c03e82f457c78cdfd6400`  
		Last Modified: Tue, 12 Nov 2024 02:21:26 GMT  
		Size: 1.1 MB (1075038 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2a279eb77a8cdc7ad361069df5c5f19840f210c2a284fe28734993bfff3d32c`  
		Last Modified: Tue, 12 Nov 2024 02:21:26 GMT  
		Size: 15.3 KB (15263 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.32.2-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:360131f2b94e1b4e0a0a55accc6e40255089a89942b6d2d23e682dc769763f34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.5 MB (70488602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d56de21a5014770bd14dd40f920748988275ffe324b3268c2cef771f98132bf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Mon, 28 Oct 2024 22:11:39 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
ENV TELEGRAF_VERSION=1.32.2
# Mon, 28 Oct 2024 22:11:39 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 28 Oct 2024 22:11:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Oct 2024 22:11:39 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9de63ce930d0f77f6402e61ee732ad4f784c59fd26df033bb1b7d6a0b87a2f4`  
		Last Modified: Tue, 12 Nov 2024 13:17:18 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:848dadffeaafa841326acf8c33573919df8ff222e2680607f7d10bb804a23d6c`  
		Last Modified: Wed, 13 Nov 2024 00:44:18 GMT  
		Size: 2.5 MB (2530663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4383827a27cf7c8e76ae40d02da9661a942bebbe18254b9be04d527bce572de5`  
		Last Modified: Wed, 13 Nov 2024 00:45:35 GMT  
		Size: 63.9 MB (63869605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98293dc53f9f009ae42c20ca72b06e353c3ce6fbaa9fd797c46aad972fea12e7`  
		Last Modified: Wed, 13 Nov 2024 00:45:33 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.32.2-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:195d46a82a6c805c64e6541bef8cd6d5a323cd483df30830f7862efc8b0a850a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1086100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c86876f9c189bd84719ab02f8fa82628ea72b474c79ac492165966c68f7af49`

```dockerfile
```

-	Layers:
	-	`sha256:f52cb10165d665b2775de9498b738fbda072838abd2ba18481be987a84e09f3b`  
		Last Modified: Wed, 13 Nov 2024 00:45:33 GMT  
		Size: 1.1 MB (1070715 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:701181e3f6633764e305402b4491f468e9add860351d9ac3ebad727e1e6c9277`  
		Last Modified: Wed, 13 Nov 2024 00:45:33 GMT  
		Size: 15.4 KB (15385 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:alpine`

```console
$ docker pull telegraf@sha256:efbcdf0e7ab69d3435ea0f461fd6eafbcc78218a56967c5a4a716243fcd5b8f1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:01b02df93201a0900559932f66c19656f5bc006856431ec8a3c55a97203cf39c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.9 MB (76897588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:416722b7aa0ae6ee5acfb146710777244cac4f620f6725e4177e492e47a9d7fb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Mon, 28 Oct 2024 22:11:39 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
ENV TELEGRAF_VERSION=1.32.2
# Mon, 28 Oct 2024 22:11:39 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 28 Oct 2024 22:11:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Oct 2024 22:11:39 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b08342fb4a15566c984bd8b550d2c6c3ca140282923a7ca9052a39c3a95e2ff3`  
		Last Modified: Tue, 12 Nov 2024 02:21:26 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23fdb6caa57be3237ed9057d1c14b85ebb2c4ae7b86aaa4bc5779092c1fa0482`  
		Last Modified: Tue, 12 Nov 2024 02:21:26 GMT  
		Size: 2.4 MB (2444825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a201f0922fd7c1147588a702ba1299395744f0b8364e7a71a66b90f262d0910`  
		Last Modified: Tue, 12 Nov 2024 02:21:27 GMT  
		Size: 70.8 MB (70828250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f67f2b39b4cc830dd11c65acded3c52414fe51480f00f26734a56024513ea44b`  
		Last Modified: Tue, 12 Nov 2024 02:21:26 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:7221f00e7b8f98ce1a8efdd3d93036ad4cfc281ec78ca1ef1f3ddad30b016a25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1090301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a10b1e50777dd205f11ea45c03655998121a7cad6b392a60c9b807039a5a9f8b`

```dockerfile
```

-	Layers:
	-	`sha256:9cba6aaeefe511469c1f79c58f11721e14288103a96c03e82f457c78cdfd6400`  
		Last Modified: Tue, 12 Nov 2024 02:21:26 GMT  
		Size: 1.1 MB (1075038 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2a279eb77a8cdc7ad361069df5c5f19840f210c2a284fe28734993bfff3d32c`  
		Last Modified: Tue, 12 Nov 2024 02:21:26 GMT  
		Size: 15.3 KB (15263 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:360131f2b94e1b4e0a0a55accc6e40255089a89942b6d2d23e682dc769763f34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.5 MB (70488602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d56de21a5014770bd14dd40f920748988275ffe324b3268c2cef771f98132bf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Mon, 28 Oct 2024 22:11:39 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
ENV TELEGRAF_VERSION=1.32.2
# Mon, 28 Oct 2024 22:11:39 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 28 Oct 2024 22:11:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Oct 2024 22:11:39 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9de63ce930d0f77f6402e61ee732ad4f784c59fd26df033bb1b7d6a0b87a2f4`  
		Last Modified: Tue, 12 Nov 2024 13:17:18 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:848dadffeaafa841326acf8c33573919df8ff222e2680607f7d10bb804a23d6c`  
		Last Modified: Wed, 13 Nov 2024 00:44:18 GMT  
		Size: 2.5 MB (2530663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4383827a27cf7c8e76ae40d02da9661a942bebbe18254b9be04d527bce572de5`  
		Last Modified: Wed, 13 Nov 2024 00:45:35 GMT  
		Size: 63.9 MB (63869605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98293dc53f9f009ae42c20ca72b06e353c3ce6fbaa9fd797c46aad972fea12e7`  
		Last Modified: Wed, 13 Nov 2024 00:45:33 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:195d46a82a6c805c64e6541bef8cd6d5a323cd483df30830f7862efc8b0a850a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1086100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c86876f9c189bd84719ab02f8fa82628ea72b474c79ac492165966c68f7af49`

```dockerfile
```

-	Layers:
	-	`sha256:f52cb10165d665b2775de9498b738fbda072838abd2ba18481be987a84e09f3b`  
		Last Modified: Wed, 13 Nov 2024 00:45:33 GMT  
		Size: 1.1 MB (1070715 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:701181e3f6633764e305402b4491f468e9add860351d9ac3ebad727e1e6c9277`  
		Last Modified: Wed, 13 Nov 2024 00:45:33 GMT  
		Size: 15.4 KB (15385 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:latest`

```console
$ docker pull telegraf@sha256:959da5a531eebce5db7b453234cefcb310aad55501e74ec292cb903369e3642e
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
$ docker pull telegraf@sha256:97bb1a17ef1af44642e0bc228ee635906825bf1c475a56ab0d41f20101c45380
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.6 MB (163620064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd9a1144d868b83b432312c8dad1574e02b2f5badf6cd487dd213a88737c3879`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
ENV TELEGRAF_VERSION=1.32.2
# Mon, 28 Oct 2024 22:11:39 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 28 Oct 2024 22:11:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Oct 2024 22:11:39 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:b2b31b28ee3c96e96195c754f8679f690db4b18e475682d716122016ef056f39`  
		Last Modified: Tue, 12 Nov 2024 00:55:23 GMT  
		Size: 49.6 MB (49575695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3cc7b6f04730c072f8b292917e0d95bb886096a2b2b1781196170965161cd27`  
		Last Modified: Tue, 12 Nov 2024 02:38:12 GMT  
		Size: 24.1 MB (24058346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23f2e2047df7e2f387bee7214610d85f418a2b0f212c6f1f6eaee882d6d32444`  
		Last Modified: Tue, 12 Nov 2024 03:16:25 GMT  
		Size: 18.9 MB (18948097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cec5ef2e84f55cf715952487f4871c5d31ee84c2564cc9e2ef203d3d8394caa`  
		Last Modified: Tue, 12 Nov 2024 03:16:24 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1cef6be5300fa2e27485dbc48470b500f4e54ab0bced4d651f48910c6b0732f`  
		Last Modified: Tue, 12 Nov 2024 03:16:25 GMT  
		Size: 71.0 MB (71035533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa9983172de0f034e6469bf8ec055749ecc65f496220eea36240920970de48a9`  
		Last Modified: Tue, 12 Nov 2024 03:16:24 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:1135d2fd4d14bc36c0b43849bb61bc274df73c028d08348169e8d0c6ee6317eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6443788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ec90c2c2a09b2af14ecf643d7405caca9b8f6c7e2adc3643b090379918f496d`

```dockerfile
```

-	Layers:
	-	`sha256:2c37a1d77bf2e7d901d08bcb8dab360d7a3fe3aecfd9643d77a90e9c5ee302f5`  
		Last Modified: Tue, 12 Nov 2024 03:16:24 GMT  
		Size: 6.4 MB (6429016 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a288cd6b4b2ff7290c1a682d600723d4d9898a08f33c874a2adbb72674df2359`  
		Last Modified: Tue, 12 Nov 2024 03:16:24 GMT  
		Size: 14.8 KB (14772 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:04b6577c812070f274ce15ce928a53864314c754c9ed92f58128e7e438b906a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.6 MB (150625344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0712361ac2b8ae51dd895af739707480e7eda069cdfa26d9a868d700e6b7ae6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:2ce9af7b514320ba230746cbff4f2f2e2b8d4a62ac035ebbe6575e17544f6416 in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
ENV TELEGRAF_VERSION=1.32.2
# Mon, 28 Oct 2024 22:11:39 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 28 Oct 2024 22:11:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Oct 2024 22:11:39 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:b683f99b4cdeb3cb4e487b268b3949647168e16d00d07e004e03af92331dbfed`  
		Last Modified: Thu, 17 Oct 2024 03:06:32 GMT  
		Size: 45.1 MB (45147940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47b7fd5031c50fee563f16760ae6e5334672d6c9ba07d159b9e3a17a3b62011`  
		Last Modified: Sat, 19 Oct 2024 00:56:10 GMT  
		Size: 22.0 MB (21957404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2247d3273aa1d92c25210b647da389293f770c7463e0680590bba2707a00d4f`  
		Last Modified: Sat, 19 Oct 2024 07:17:52 GMT  
		Size: 17.7 MB (17724956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ce5b94c2bbc729b36f1960f93b7ec6c2a95a43a18ba0a45cc454eac7d35b439`  
		Last Modified: Tue, 29 Oct 2024 05:01:00 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a07021e02e5050b2cdc3717c87d8a478091d0570662e1b477e1f6117fe1dfd0`  
		Last Modified: Tue, 29 Oct 2024 05:01:03 GMT  
		Size: 65.8 MB (65792648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff0b1faddfd563f9859d102060f228af24bd0a80066b379e72421db22ed20258`  
		Last Modified: Tue, 29 Oct 2024 05:01:00 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:8eeeb1ec87c39c5ec04315af8a61c4db05243ee1faa3bfb16ecd810c3c284dfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6439284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:925659d92f5e3ca5238d6a7bd1eebed8b16ab3ed1dac0a6552951aaaf5d4e4b9`

```dockerfile
```

-	Layers:
	-	`sha256:ea15cbd0b35cc1347a7691a7cf9cc463da340ef92fd806c3c6fcc27e46e61885`  
		Last Modified: Tue, 29 Oct 2024 05:01:01 GMT  
		Size: 6.4 MB (6424388 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83c72bd917ccd64d25ab9c7dafe3f57ffa5ae1005e77e0eeaba7533ca75d3748`  
		Last Modified: Tue, 29 Oct 2024 05:01:00 GMT  
		Size: 14.9 KB (14896 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:480e15d49e83ae340cd3bf32ff384a188f0c347d4bcf7058d2e17c3cb49b2692
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.1 MB (156113237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d8f4fe1c67ef36f0cc2f771060e1bd779cceabc69de6aac9058a88175ed5a5a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:1df819221542e236e104deb2624ffe4efd79382aed25b3ab20088becaeadad31 in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
ENV TELEGRAF_VERSION=1.32.2
# Mon, 28 Oct 2024 22:11:39 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 28 Oct 2024 22:11:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Oct 2024 22:11:39 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:c1e0ef7b956a07c7b090256aa16cbb0550a34d0625d1d23c5b1a76e92a58d01e`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 49.6 MB (49584978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b894d63c771a6056bc65ff25192b251413259ba7d160b0076f0f5d7975dc39`  
		Last Modified: Sat, 19 Oct 2024 01:10:43 GMT  
		Size: 23.6 MB (23593834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e66595c705129c5730b8646de79531481b8cb13763baf90c3b96d036ddf98362`  
		Last Modified: Tue, 29 Oct 2024 05:55:08 GMT  
		Size: 18.9 MB (18870583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13287a0c9f8805355ea97d1603870eabf63879cd2d1faaf951aca6e332365969`  
		Last Modified: Tue, 29 Oct 2024 05:55:07 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61625606c80a4ee75db903204c47c7871d8755e675080487598be4f3b6a5a293`  
		Last Modified: Tue, 29 Oct 2024 05:55:09 GMT  
		Size: 64.1 MB (64061436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e6d238d30b7987263da699d795a6c3a0b1b9e7bedd8fb538bce44ee8b666857`  
		Last Modified: Tue, 29 Oct 2024 05:55:07 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:b0f7b05ff6169d6bfd68d03a708053f6e97f41c98e6121216c361df682825557
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6444598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc2b89afaf727aea7fad41e4f5f378a8b19e81f25e568c41e08cb3e8599c358c`

```dockerfile
```

-	Layers:
	-	`sha256:4b22cfd3bd756cac3a3294cb210cdbc94e3f36713d2810bba113c0b8a0d29e51`  
		Last Modified: Tue, 29 Oct 2024 05:55:08 GMT  
		Size: 6.4 MB (6429674 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa44f138429976d5f635ff83285f36ed44e3baee6edfb8701c9708c582e8b788`  
		Last Modified: Tue, 29 Oct 2024 05:55:07 GMT  
		Size: 14.9 KB (14924 bytes)  
		MIME: application/vnd.in-toto+json
