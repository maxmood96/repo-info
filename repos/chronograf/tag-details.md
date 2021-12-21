<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `chronograf`

-	[`chronograf:1.6`](#chronograf16)
-	[`chronograf:1.6-alpine`](#chronograf16-alpine)
-	[`chronograf:1.6.2`](#chronograf162)
-	[`chronograf:1.6.2-alpine`](#chronograf162-alpine)
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
-	[`chronograf:1.9.1`](#chronograf191)
-	[`chronograf:1.9.1-alpine`](#chronograf191-alpine)
-	[`chronograf:alpine`](#chronografalpine)
-	[`chronograf:latest`](#chronograflatest)

## `chronograf:1.6`

```console
$ docker pull chronograf@sha256:d6e31e78c07b47acc1a45a0d9308a02c7b5c285439281dc2480f9b3e996f9214
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.6` - linux; amd64

```console
$ docker pull chronograf@sha256:93e93e04ec5f120f4be847e1e21c2792e0f53c8f063c923fe9be2539d996ae2a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49359006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e50a3e228f3934e7fe226c9871de8fe05178a60c0538d65cd867ddb3330d83d2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 21 Dec 2021 01:24:41 GMT
ADD file:b1650c19c1dd1f4cff71553f2bb0bc949944d0bc24b54c318b2880c14538648a in / 
# Tue, 21 Dec 2021 01:24:42 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 02:06:33 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 21 Dec 2021 02:06:33 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Tue, 21 Dec 2021 02:06:40 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 21 Dec 2021 02:06:41 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 21 Dec 2021 02:06:41 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 21 Dec 2021 02:06:41 GMT
EXPOSE 8888
# Tue, 21 Dec 2021 02:06:41 GMT
VOLUME [/var/lib/chronograf]
# Tue, 21 Dec 2021 02:06:41 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 21 Dec 2021 02:06:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Dec 2021 02:06:42 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:35b2232c987ef3e6249ed229afcca51cd83320e08f6700022f4a3644a11f00f2`  
		Last Modified: Tue, 21 Dec 2021 01:31:36 GMT  
		Size: 22.5 MB (22529141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f793a6dcc9ba1d2eaa75faeeeb59be02b0ff06ca902fac32486ebe1c2c81b387`  
		Last Modified: Tue, 21 Dec 2021 02:08:07 GMT  
		Size: 6.8 MB (6760216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73c295d35e6c0ab03a07772baf7084a53d62645c7d5c5c86d03673565c237cc4`  
		Last Modified: Tue, 21 Dec 2021 02:08:10 GMT  
		Size: 20.0 MB (20045252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f3232c0faeb1c6624dcc4cc6cecd73030fb511a47f3f093eb4a86b9c99912a8`  
		Last Modified: Tue, 21 Dec 2021 02:08:06 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57e4efaac704674f22592cef55d4b6bc2b2d615653e49364a9df19f9180aef16`  
		Last Modified: Tue, 21 Dec 2021 02:08:06 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a9621900e2afa0500276e4ffb208e25701a534d18b0f1ccd59a6ff8820e8e53`  
		Last Modified: Tue, 21 Dec 2021 02:08:06 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.6` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:284bf251afa2030b26410f5db673808d3293549fec3489c0841f6abbc680b58f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.9 MB (43944354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c34d96833bc7acbf020626a8ac862f0dacc02c6e070e679c250554338dac7df`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 21 Dec 2021 02:05:40 GMT
ADD file:924a2e95e52f87fd6e79e8b0865e63f19432a71f823114b8b4d729ecd420d7fb in / 
# Tue, 21 Dec 2021 02:05:41 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 03:25:11 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 21 Dec 2021 03:25:12 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Tue, 21 Dec 2021 03:25:30 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 21 Dec 2021 03:25:30 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 21 Dec 2021 03:25:31 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 21 Dec 2021 03:25:31 GMT
EXPOSE 8888
# Tue, 21 Dec 2021 03:25:32 GMT
VOLUME [/var/lib/chronograf]
# Tue, 21 Dec 2021 03:25:32 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 21 Dec 2021 03:25:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Dec 2021 03:25:33 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:12790d92cf90440e36a3292fe34a336c54030e049074eb36386502daa81decea`  
		Last Modified: Tue, 21 Dec 2021 02:22:43 GMT  
		Size: 19.3 MB (19318715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8d896bc18835bd9e95e55d9744358d7ff742c715935b1ccc5f0793ac8c739b6`  
		Last Modified: Tue, 21 Dec 2021 03:28:51 GMT  
		Size: 5.8 MB (5780617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f43bbbddc116d62de0d41c6523bc8267a4192be3edcf677a36c0c2320c659721`  
		Last Modified: Tue, 21 Dec 2021 03:29:00 GMT  
		Size: 18.8 MB (18820624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51d40c53a7635035cabeac6b490d8bbb87cc011b93681f37bd8f363fab813a41`  
		Last Modified: Tue, 21 Dec 2021 03:28:48 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8981c61c6ce2d6c6dee5e004ba87892182c76a9320918316953b07d5f92faed`  
		Last Modified: Tue, 21 Dec 2021 03:28:48 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c657e98f6cc58d8d8866982daafcf86d59170245540293cf6c072d62e944a9c2`  
		Last Modified: Tue, 21 Dec 2021 03:28:48 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.6` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:f1456ca71c9922506f6cd3c4d314f0c293451b68d999319e9296772ca5b9bef3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45421915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83ea8b0f13f77d052e74a5265c69c1a4fc337de36062808f6afbd9b8c34df35a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 21 Dec 2021 01:44:39 GMT
ADD file:3bd088d09a71e361b1691e6fc4002843c7c0c3a591ac718d31a05b7eed3f1509 in / 
# Tue, 21 Dec 2021 01:44:40 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 10:38:10 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 21 Dec 2021 10:38:11 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Tue, 21 Dec 2021 10:38:19 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 21 Dec 2021 10:38:20 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 21 Dec 2021 10:38:21 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 21 Dec 2021 10:38:21 GMT
EXPOSE 8888
# Tue, 21 Dec 2021 10:38:22 GMT
VOLUME [/var/lib/chronograf]
# Tue, 21 Dec 2021 10:38:24 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 21 Dec 2021 10:38:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Dec 2021 10:38:25 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:0c10218d14f066bac4a45577b86a8b86e637c81535d33e71c03493e8ce5f0a30`  
		Last Modified: Tue, 21 Dec 2021 01:53:04 GMT  
		Size: 20.4 MB (20389374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:157c02822419c95c32eccbdc1c7e69e43f3c034ba9961d974480f4431e6062be`  
		Last Modified: Tue, 21 Dec 2021 10:40:17 GMT  
		Size: 6.0 MB (6046874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b28f2a34391aabaa38ddea6c1317cd82f602886b9a84438ec6a1d3e7a8fc2a43`  
		Last Modified: Tue, 21 Dec 2021 10:40:19 GMT  
		Size: 19.0 MB (18961264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9435b054722159b2dc2f67400bc53625440eb6cfeb0199d0230868238fa68b78`  
		Last Modified: Tue, 21 Dec 2021 10:40:16 GMT  
		Size: 12.3 KB (12252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a55e24fd201e1c83f0c4b5ba4b3a3a1d3473160bbb5818281d6f7ab1ed05d683`  
		Last Modified: Tue, 21 Dec 2021 10:40:16 GMT  
		Size: 11.9 KB (11912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caff1b3acfe9dd31b75bc6c8c00936c507c21ae4d190b6e47bd38f762a18beba`  
		Last Modified: Tue, 21 Dec 2021 10:40:16 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.6-alpine`

```console
$ docker pull chronograf@sha256:d83014d2850383073830fe3cc8b1dd10280ccadb3dc727fc46c18f0133876e24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.6-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:42be608ccf5cf8a282705866e53559a2f683cee86f301d5335d2b0a8a722d1a7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14867541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72592bc7b5181925382f61d3755716a15c0a3222db4caad2f764f58f7c77f70b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 21:55:17 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 12 Nov 2021 21:55:18 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Fri, 12 Nov 2021 21:55:18 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Fri, 12 Nov 2021 21:55:32 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 12 Nov 2021 21:55:32 GMT
COPY file:aa4a9d01295c7013d89da92a943af071556aea6dbe6269affd4664fdd86969b8 in /usr/share/chronograf/LICENSE 
# Fri, 12 Nov 2021 21:55:32 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 12 Nov 2021 21:55:32 GMT
EXPOSE 8888
# Fri, 12 Nov 2021 21:55:32 GMT
VOLUME [/var/lib/chronograf]
# Fri, 12 Nov 2021 21:55:33 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Fri, 12 Nov 2021 21:55:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 12 Nov 2021 21:55:33 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc79f199b43e46c5dfea12dfa8b92b7811e74b4d3812ff99c8368e4d2af803e7`  
		Last Modified: Fri, 12 Nov 2021 21:56:45 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aac166cdd02de2f1baf9250ebe4e1a5bec54cc49a59dbb3716570ed37d5bf63`  
		Last Modified: Fri, 12 Nov 2021 21:56:43 GMT  
		Size: 282.0 KB (281961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:168157deaab4ba90e7cb5d2b6d5e649804bbf43d504044d8e9f3b7d8572f1935`  
		Last Modified: Fri, 12 Nov 2021 21:56:45 GMT  
		Size: 11.7 MB (11738046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a7b8146058f9a9b104394531bbfffada3698450341aa41fa890a7a4aae65320`  
		Last Modified: Fri, 12 Nov 2021 21:56:43 GMT  
		Size: 12.3 KB (12267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f36021c872f9879231ff8873fe042d102c69ef4a5a63c1b5a3fdf00ac44b9467`  
		Last Modified: Fri, 12 Nov 2021 21:56:43 GMT  
		Size: 11.9 KB (11895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b09ac85e2c2a25870fabd125b2933114782d6d8dc3b752bc9c5ebfd77bb0764`  
		Last Modified: Fri, 12 Nov 2021 21:56:43 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.6.2`

```console
$ docker pull chronograf@sha256:d6e31e78c07b47acc1a45a0d9308a02c7b5c285439281dc2480f9b3e996f9214
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.6.2` - linux; amd64

```console
$ docker pull chronograf@sha256:93e93e04ec5f120f4be847e1e21c2792e0f53c8f063c923fe9be2539d996ae2a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49359006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e50a3e228f3934e7fe226c9871de8fe05178a60c0538d65cd867ddb3330d83d2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 21 Dec 2021 01:24:41 GMT
ADD file:b1650c19c1dd1f4cff71553f2bb0bc949944d0bc24b54c318b2880c14538648a in / 
# Tue, 21 Dec 2021 01:24:42 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 02:06:33 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 21 Dec 2021 02:06:33 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Tue, 21 Dec 2021 02:06:40 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 21 Dec 2021 02:06:41 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 21 Dec 2021 02:06:41 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 21 Dec 2021 02:06:41 GMT
EXPOSE 8888
# Tue, 21 Dec 2021 02:06:41 GMT
VOLUME [/var/lib/chronograf]
# Tue, 21 Dec 2021 02:06:41 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 21 Dec 2021 02:06:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Dec 2021 02:06:42 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:35b2232c987ef3e6249ed229afcca51cd83320e08f6700022f4a3644a11f00f2`  
		Last Modified: Tue, 21 Dec 2021 01:31:36 GMT  
		Size: 22.5 MB (22529141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f793a6dcc9ba1d2eaa75faeeeb59be02b0ff06ca902fac32486ebe1c2c81b387`  
		Last Modified: Tue, 21 Dec 2021 02:08:07 GMT  
		Size: 6.8 MB (6760216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73c295d35e6c0ab03a07772baf7084a53d62645c7d5c5c86d03673565c237cc4`  
		Last Modified: Tue, 21 Dec 2021 02:08:10 GMT  
		Size: 20.0 MB (20045252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f3232c0faeb1c6624dcc4cc6cecd73030fb511a47f3f093eb4a86b9c99912a8`  
		Last Modified: Tue, 21 Dec 2021 02:08:06 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57e4efaac704674f22592cef55d4b6bc2b2d615653e49364a9df19f9180aef16`  
		Last Modified: Tue, 21 Dec 2021 02:08:06 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a9621900e2afa0500276e4ffb208e25701a534d18b0f1ccd59a6ff8820e8e53`  
		Last Modified: Tue, 21 Dec 2021 02:08:06 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.6.2` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:284bf251afa2030b26410f5db673808d3293549fec3489c0841f6abbc680b58f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.9 MB (43944354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c34d96833bc7acbf020626a8ac862f0dacc02c6e070e679c250554338dac7df`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 21 Dec 2021 02:05:40 GMT
ADD file:924a2e95e52f87fd6e79e8b0865e63f19432a71f823114b8b4d729ecd420d7fb in / 
# Tue, 21 Dec 2021 02:05:41 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 03:25:11 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 21 Dec 2021 03:25:12 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Tue, 21 Dec 2021 03:25:30 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 21 Dec 2021 03:25:30 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 21 Dec 2021 03:25:31 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 21 Dec 2021 03:25:31 GMT
EXPOSE 8888
# Tue, 21 Dec 2021 03:25:32 GMT
VOLUME [/var/lib/chronograf]
# Tue, 21 Dec 2021 03:25:32 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 21 Dec 2021 03:25:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Dec 2021 03:25:33 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:12790d92cf90440e36a3292fe34a336c54030e049074eb36386502daa81decea`  
		Last Modified: Tue, 21 Dec 2021 02:22:43 GMT  
		Size: 19.3 MB (19318715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8d896bc18835bd9e95e55d9744358d7ff742c715935b1ccc5f0793ac8c739b6`  
		Last Modified: Tue, 21 Dec 2021 03:28:51 GMT  
		Size: 5.8 MB (5780617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f43bbbddc116d62de0d41c6523bc8267a4192be3edcf677a36c0c2320c659721`  
		Last Modified: Tue, 21 Dec 2021 03:29:00 GMT  
		Size: 18.8 MB (18820624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51d40c53a7635035cabeac6b490d8bbb87cc011b93681f37bd8f363fab813a41`  
		Last Modified: Tue, 21 Dec 2021 03:28:48 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8981c61c6ce2d6c6dee5e004ba87892182c76a9320918316953b07d5f92faed`  
		Last Modified: Tue, 21 Dec 2021 03:28:48 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c657e98f6cc58d8d8866982daafcf86d59170245540293cf6c072d62e944a9c2`  
		Last Modified: Tue, 21 Dec 2021 03:28:48 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.6.2` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:f1456ca71c9922506f6cd3c4d314f0c293451b68d999319e9296772ca5b9bef3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45421915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83ea8b0f13f77d052e74a5265c69c1a4fc337de36062808f6afbd9b8c34df35a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 21 Dec 2021 01:44:39 GMT
ADD file:3bd088d09a71e361b1691e6fc4002843c7c0c3a591ac718d31a05b7eed3f1509 in / 
# Tue, 21 Dec 2021 01:44:40 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 10:38:10 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 21 Dec 2021 10:38:11 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Tue, 21 Dec 2021 10:38:19 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 21 Dec 2021 10:38:20 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 21 Dec 2021 10:38:21 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 21 Dec 2021 10:38:21 GMT
EXPOSE 8888
# Tue, 21 Dec 2021 10:38:22 GMT
VOLUME [/var/lib/chronograf]
# Tue, 21 Dec 2021 10:38:24 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 21 Dec 2021 10:38:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Dec 2021 10:38:25 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:0c10218d14f066bac4a45577b86a8b86e637c81535d33e71c03493e8ce5f0a30`  
		Last Modified: Tue, 21 Dec 2021 01:53:04 GMT  
		Size: 20.4 MB (20389374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:157c02822419c95c32eccbdc1c7e69e43f3c034ba9961d974480f4431e6062be`  
		Last Modified: Tue, 21 Dec 2021 10:40:17 GMT  
		Size: 6.0 MB (6046874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b28f2a34391aabaa38ddea6c1317cd82f602886b9a84438ec6a1d3e7a8fc2a43`  
		Last Modified: Tue, 21 Dec 2021 10:40:19 GMT  
		Size: 19.0 MB (18961264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9435b054722159b2dc2f67400bc53625440eb6cfeb0199d0230868238fa68b78`  
		Last Modified: Tue, 21 Dec 2021 10:40:16 GMT  
		Size: 12.3 KB (12252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a55e24fd201e1c83f0c4b5ba4b3a3a1d3473160bbb5818281d6f7ab1ed05d683`  
		Last Modified: Tue, 21 Dec 2021 10:40:16 GMT  
		Size: 11.9 KB (11912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caff1b3acfe9dd31b75bc6c8c00936c507c21ae4d190b6e47bd38f762a18beba`  
		Last Modified: Tue, 21 Dec 2021 10:40:16 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.6.2-alpine`

```console
$ docker pull chronograf@sha256:d83014d2850383073830fe3cc8b1dd10280ccadb3dc727fc46c18f0133876e24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.6.2-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:42be608ccf5cf8a282705866e53559a2f683cee86f301d5335d2b0a8a722d1a7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14867541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72592bc7b5181925382f61d3755716a15c0a3222db4caad2f764f58f7c77f70b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 21:55:17 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 12 Nov 2021 21:55:18 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Fri, 12 Nov 2021 21:55:18 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Fri, 12 Nov 2021 21:55:32 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 12 Nov 2021 21:55:32 GMT
COPY file:aa4a9d01295c7013d89da92a943af071556aea6dbe6269affd4664fdd86969b8 in /usr/share/chronograf/LICENSE 
# Fri, 12 Nov 2021 21:55:32 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 12 Nov 2021 21:55:32 GMT
EXPOSE 8888
# Fri, 12 Nov 2021 21:55:32 GMT
VOLUME [/var/lib/chronograf]
# Fri, 12 Nov 2021 21:55:33 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Fri, 12 Nov 2021 21:55:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 12 Nov 2021 21:55:33 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc79f199b43e46c5dfea12dfa8b92b7811e74b4d3812ff99c8368e4d2af803e7`  
		Last Modified: Fri, 12 Nov 2021 21:56:45 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aac166cdd02de2f1baf9250ebe4e1a5bec54cc49a59dbb3716570ed37d5bf63`  
		Last Modified: Fri, 12 Nov 2021 21:56:43 GMT  
		Size: 282.0 KB (281961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:168157deaab4ba90e7cb5d2b6d5e649804bbf43d504044d8e9f3b7d8572f1935`  
		Last Modified: Fri, 12 Nov 2021 21:56:45 GMT  
		Size: 11.7 MB (11738046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a7b8146058f9a9b104394531bbfffada3698450341aa41fa890a7a4aae65320`  
		Last Modified: Fri, 12 Nov 2021 21:56:43 GMT  
		Size: 12.3 KB (12267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f36021c872f9879231ff8873fe042d102c69ef4a5a63c1b5a3fdf00ac44b9467`  
		Last Modified: Fri, 12 Nov 2021 21:56:43 GMT  
		Size: 11.9 KB (11895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b09ac85e2c2a25870fabd125b2933114782d6d8dc3b752bc9c5ebfd77bb0764`  
		Last Modified: Fri, 12 Nov 2021 21:56:43 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.7`

```console
$ docker pull chronograf@sha256:1532ea515c7a8aaf253bcac680ee9053bff0aaa8a8cda2a0deed97bf638a2cd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.7` - linux; amd64

```console
$ docker pull chronograf@sha256:7467f1396741813ee8a22e5debdf8acef05bb403aa2ed6061f841ae520377a49
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.4 MB (65388230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09f4c660b623d287995e8edf2ecf21ee49d70ad90f7816ea50d97474cf461726`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 21 Dec 2021 01:24:41 GMT
ADD file:b1650c19c1dd1f4cff71553f2bb0bc949944d0bc24b54c318b2880c14538648a in / 
# Tue, 21 Dec 2021 01:24:42 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 02:07:00 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 21 Dec 2021 02:07:00 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 21 Dec 2021 02:07:10 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 21 Dec 2021 02:07:11 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 21 Dec 2021 02:07:11 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 21 Dec 2021 02:07:11 GMT
EXPOSE 8888
# Tue, 21 Dec 2021 02:07:11 GMT
VOLUME [/var/lib/chronograf]
# Tue, 21 Dec 2021 02:07:12 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 21 Dec 2021 02:07:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Dec 2021 02:07:12 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:35b2232c987ef3e6249ed229afcca51cd83320e08f6700022f4a3644a11f00f2`  
		Last Modified: Tue, 21 Dec 2021 01:31:36 GMT  
		Size: 22.5 MB (22529141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cac527340873130e9b032cf6cade457760a835592e71ea2ddbebcb38980129ec`  
		Last Modified: Tue, 21 Dec 2021 02:08:21 GMT  
		Size: 4.5 MB (4506577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f51a7663f3aaadcb78e6304ea5cedbb005f1fc65b67e99fd54db61d71666403e`  
		Last Modified: Tue, 21 Dec 2021 02:08:26 GMT  
		Size: 38.3 MB (38328115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7de830434c8f9c5c145e08070ff8b660955db3308702d01c0faf5012fdfaa99d`  
		Last Modified: Tue, 21 Dec 2021 02:08:20 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d80acb32947eca17479949ab9314d2b864db8b9cd1b61a572489bd4e5084015`  
		Last Modified: Tue, 21 Dec 2021 02:08:20 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42ac6a2bafa3fdfe0ad18405fc6c4e38815df3815e76af8c635d78c8c62701d9`  
		Last Modified: Tue, 21 Dec 2021 02:08:20 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.7` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:aa1f885d9ef18a45ac8fbb10c18842be5821c97e8a14bdc627fc7b277a622955
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.0 MB (59006472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1ce354293bfc541a57cb8cd5dd05020bcca53b440247dfc01822a12bba5b382`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 21 Dec 2021 02:05:40 GMT
ADD file:924a2e95e52f87fd6e79e8b0865e63f19432a71f823114b8b4d729ecd420d7fb in / 
# Tue, 21 Dec 2021 02:05:41 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 03:26:02 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 21 Dec 2021 03:26:02 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 21 Dec 2021 03:26:34 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 21 Dec 2021 03:26:35 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 21 Dec 2021 03:26:36 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 21 Dec 2021 03:26:36 GMT
EXPOSE 8888
# Tue, 21 Dec 2021 03:26:37 GMT
VOLUME [/var/lib/chronograf]
# Tue, 21 Dec 2021 03:26:37 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 21 Dec 2021 03:26:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Dec 2021 03:26:38 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:12790d92cf90440e36a3292fe34a336c54030e049074eb36386502daa81decea`  
		Last Modified: Tue, 21 Dec 2021 02:22:43 GMT  
		Size: 19.3 MB (19318715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8bac0e9fd12113ed9a3b2a9d4d2e22927558625db75127da07d5a2e87347e7c`  
		Last Modified: Tue, 21 Dec 2021 03:29:14 GMT  
		Size: 3.9 MB (3879873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6a20156b3e468b456ee7ddc1886c1e2833731ea3d8cf5a7097bfa15ffa925a3`  
		Last Modified: Tue, 21 Dec 2021 03:29:32 GMT  
		Size: 35.8 MB (35783485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ee6921fe050cf767f1f7a8d94a61e572a629077daa1a911c065a1f2fcfbab44`  
		Last Modified: Tue, 21 Dec 2021 03:29:12 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5be49d7791d277af8b7e2fc60d924e5d084402cb14994b86ba0178e48b34a32`  
		Last Modified: Tue, 21 Dec 2021 03:29:12 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3528401c5df5689945845d8936ecca75b3fa1417b57604e32aa8b7dc728709a9`  
		Last Modified: Tue, 21 Dec 2021 03:29:12 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.7` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:9b471e023ab02e87fa401e9c0a14cea090fa831e7f5d22c649b34b75e743cf3c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60294433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcb7cdeeedb35e81c054657932256640c2e49fcc0154f574e1e310ed8d882c4b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 21 Dec 2021 01:44:39 GMT
ADD file:3bd088d09a71e361b1691e6fc4002843c7c0c3a591ac718d31a05b7eed3f1509 in / 
# Tue, 21 Dec 2021 01:44:40 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 10:38:48 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 21 Dec 2021 10:38:49 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 21 Dec 2021 10:39:00 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 21 Dec 2021 10:39:01 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 21 Dec 2021 10:39:02 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 21 Dec 2021 10:39:02 GMT
EXPOSE 8888
# Tue, 21 Dec 2021 10:39:03 GMT
VOLUME [/var/lib/chronograf]
# Tue, 21 Dec 2021 10:39:05 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 21 Dec 2021 10:39:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Dec 2021 10:39:06 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:0c10218d14f066bac4a45577b86a8b86e637c81535d33e71c03493e8ce5f0a30`  
		Last Modified: Tue, 21 Dec 2021 01:53:04 GMT  
		Size: 20.4 MB (20389374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fa0e98337b01760f6d5b757d71165199e16fd1526d796c828174c23ed0a3771`  
		Last Modified: Tue, 21 Dec 2021 10:40:30 GMT  
		Size: 3.9 MB (3893809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a7f6a994c25c1ddfa1201a312539865cd0d2db2656a33fa3bfb15ad1cb8da32`  
		Last Modified: Tue, 21 Dec 2021 10:40:35 GMT  
		Size: 36.0 MB (35986855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30838c9b5339133a99abf371bb8d8ea942de4c81161e30e434a9e041d5817c77`  
		Last Modified: Tue, 21 Dec 2021 10:40:29 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbff305548f3a5461b73b2027e2b7682a3a1f969b397673cc62fceae4ec79474`  
		Last Modified: Tue, 21 Dec 2021 10:40:29 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18b5a7430e18c396b42895cf3d5d63d6f1c66fc8551c3f77c7604735c4f8f481`  
		Last Modified: Tue, 21 Dec 2021 10:40:29 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.7-alpine`

```console
$ docker pull chronograf@sha256:997ecebb69bae99483291c00663c3d1d2ec0628a1c0abb4aae057cc7b004570c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.7-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:77cf883ffa62d74117fd7c6e4a998199f6fbb063e654a42b8046a6cfe3ce69b1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22686062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c027745c7d556a42156b262cea5fa7ff78b10d534ae6c2a4decd69caaeedaa26`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 21:55:17 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 12 Nov 2021 21:55:18 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Fri, 12 Nov 2021 21:55:38 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Fri, 12 Nov 2021 21:55:44 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 12 Nov 2021 21:55:45 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 12 Nov 2021 21:55:45 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 12 Nov 2021 21:55:45 GMT
EXPOSE 8888
# Fri, 12 Nov 2021 21:55:46 GMT
VOLUME [/var/lib/chronograf]
# Fri, 12 Nov 2021 21:55:46 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Fri, 12 Nov 2021 21:55:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 12 Nov 2021 21:55:46 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc79f199b43e46c5dfea12dfa8b92b7811e74b4d3812ff99c8368e4d2af803e7`  
		Last Modified: Fri, 12 Nov 2021 21:56:45 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aac166cdd02de2f1baf9250ebe4e1a5bec54cc49a59dbb3716570ed37d5bf63`  
		Last Modified: Fri, 12 Nov 2021 21:56:43 GMT  
		Size: 282.0 KB (281961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8283a3b7cad208670302a759a3e65783b946b1fb9221a8ab882fef07277d38d3`  
		Last Modified: Fri, 12 Nov 2021 21:56:59 GMT  
		Size: 19.6 MB (19556570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01b447bd4534f47d32c04a9937b72b986d155e25c02cb3add58d4a1c700940c3`  
		Last Modified: Fri, 12 Nov 2021 21:56:55 GMT  
		Size: 12.3 KB (12263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deac552aa1d37ccee70bddc7022a3ce80dad98b87b9fd130543f7fa787be0caa`  
		Last Modified: Fri, 12 Nov 2021 21:56:55 GMT  
		Size: 11.9 KB (11895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1656207cac83a586c1a7cf9aec72e8f8cc2ee68c672d3cf8403ff18631c28cf2`  
		Last Modified: Fri, 12 Nov 2021 21:56:55 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.7.17`

```console
$ docker pull chronograf@sha256:1532ea515c7a8aaf253bcac680ee9053bff0aaa8a8cda2a0deed97bf638a2cd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.7.17` - linux; amd64

```console
$ docker pull chronograf@sha256:7467f1396741813ee8a22e5debdf8acef05bb403aa2ed6061f841ae520377a49
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.4 MB (65388230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09f4c660b623d287995e8edf2ecf21ee49d70ad90f7816ea50d97474cf461726`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 21 Dec 2021 01:24:41 GMT
ADD file:b1650c19c1dd1f4cff71553f2bb0bc949944d0bc24b54c318b2880c14538648a in / 
# Tue, 21 Dec 2021 01:24:42 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 02:07:00 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 21 Dec 2021 02:07:00 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 21 Dec 2021 02:07:10 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 21 Dec 2021 02:07:11 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 21 Dec 2021 02:07:11 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 21 Dec 2021 02:07:11 GMT
EXPOSE 8888
# Tue, 21 Dec 2021 02:07:11 GMT
VOLUME [/var/lib/chronograf]
# Tue, 21 Dec 2021 02:07:12 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 21 Dec 2021 02:07:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Dec 2021 02:07:12 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:35b2232c987ef3e6249ed229afcca51cd83320e08f6700022f4a3644a11f00f2`  
		Last Modified: Tue, 21 Dec 2021 01:31:36 GMT  
		Size: 22.5 MB (22529141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cac527340873130e9b032cf6cade457760a835592e71ea2ddbebcb38980129ec`  
		Last Modified: Tue, 21 Dec 2021 02:08:21 GMT  
		Size: 4.5 MB (4506577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f51a7663f3aaadcb78e6304ea5cedbb005f1fc65b67e99fd54db61d71666403e`  
		Last Modified: Tue, 21 Dec 2021 02:08:26 GMT  
		Size: 38.3 MB (38328115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7de830434c8f9c5c145e08070ff8b660955db3308702d01c0faf5012fdfaa99d`  
		Last Modified: Tue, 21 Dec 2021 02:08:20 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d80acb32947eca17479949ab9314d2b864db8b9cd1b61a572489bd4e5084015`  
		Last Modified: Tue, 21 Dec 2021 02:08:20 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42ac6a2bafa3fdfe0ad18405fc6c4e38815df3815e76af8c635d78c8c62701d9`  
		Last Modified: Tue, 21 Dec 2021 02:08:20 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.7.17` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:aa1f885d9ef18a45ac8fbb10c18842be5821c97e8a14bdc627fc7b277a622955
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.0 MB (59006472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1ce354293bfc541a57cb8cd5dd05020bcca53b440247dfc01822a12bba5b382`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 21 Dec 2021 02:05:40 GMT
ADD file:924a2e95e52f87fd6e79e8b0865e63f19432a71f823114b8b4d729ecd420d7fb in / 
# Tue, 21 Dec 2021 02:05:41 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 03:26:02 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 21 Dec 2021 03:26:02 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 21 Dec 2021 03:26:34 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 21 Dec 2021 03:26:35 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 21 Dec 2021 03:26:36 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 21 Dec 2021 03:26:36 GMT
EXPOSE 8888
# Tue, 21 Dec 2021 03:26:37 GMT
VOLUME [/var/lib/chronograf]
# Tue, 21 Dec 2021 03:26:37 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 21 Dec 2021 03:26:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Dec 2021 03:26:38 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:12790d92cf90440e36a3292fe34a336c54030e049074eb36386502daa81decea`  
		Last Modified: Tue, 21 Dec 2021 02:22:43 GMT  
		Size: 19.3 MB (19318715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8bac0e9fd12113ed9a3b2a9d4d2e22927558625db75127da07d5a2e87347e7c`  
		Last Modified: Tue, 21 Dec 2021 03:29:14 GMT  
		Size: 3.9 MB (3879873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6a20156b3e468b456ee7ddc1886c1e2833731ea3d8cf5a7097bfa15ffa925a3`  
		Last Modified: Tue, 21 Dec 2021 03:29:32 GMT  
		Size: 35.8 MB (35783485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ee6921fe050cf767f1f7a8d94a61e572a629077daa1a911c065a1f2fcfbab44`  
		Last Modified: Tue, 21 Dec 2021 03:29:12 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5be49d7791d277af8b7e2fc60d924e5d084402cb14994b86ba0178e48b34a32`  
		Last Modified: Tue, 21 Dec 2021 03:29:12 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3528401c5df5689945845d8936ecca75b3fa1417b57604e32aa8b7dc728709a9`  
		Last Modified: Tue, 21 Dec 2021 03:29:12 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.7.17` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:9b471e023ab02e87fa401e9c0a14cea090fa831e7f5d22c649b34b75e743cf3c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60294433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcb7cdeeedb35e81c054657932256640c2e49fcc0154f574e1e310ed8d882c4b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 21 Dec 2021 01:44:39 GMT
ADD file:3bd088d09a71e361b1691e6fc4002843c7c0c3a591ac718d31a05b7eed3f1509 in / 
# Tue, 21 Dec 2021 01:44:40 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 10:38:48 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 21 Dec 2021 10:38:49 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 21 Dec 2021 10:39:00 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 21 Dec 2021 10:39:01 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 21 Dec 2021 10:39:02 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 21 Dec 2021 10:39:02 GMT
EXPOSE 8888
# Tue, 21 Dec 2021 10:39:03 GMT
VOLUME [/var/lib/chronograf]
# Tue, 21 Dec 2021 10:39:05 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 21 Dec 2021 10:39:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Dec 2021 10:39:06 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:0c10218d14f066bac4a45577b86a8b86e637c81535d33e71c03493e8ce5f0a30`  
		Last Modified: Tue, 21 Dec 2021 01:53:04 GMT  
		Size: 20.4 MB (20389374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fa0e98337b01760f6d5b757d71165199e16fd1526d796c828174c23ed0a3771`  
		Last Modified: Tue, 21 Dec 2021 10:40:30 GMT  
		Size: 3.9 MB (3893809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a7f6a994c25c1ddfa1201a312539865cd0d2db2656a33fa3bfb15ad1cb8da32`  
		Last Modified: Tue, 21 Dec 2021 10:40:35 GMT  
		Size: 36.0 MB (35986855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30838c9b5339133a99abf371bb8d8ea942de4c81161e30e434a9e041d5817c77`  
		Last Modified: Tue, 21 Dec 2021 10:40:29 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbff305548f3a5461b73b2027e2b7682a3a1f969b397673cc62fceae4ec79474`  
		Last Modified: Tue, 21 Dec 2021 10:40:29 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18b5a7430e18c396b42895cf3d5d63d6f1c66fc8551c3f77c7604735c4f8f481`  
		Last Modified: Tue, 21 Dec 2021 10:40:29 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.7.17-alpine`

```console
$ docker pull chronograf@sha256:997ecebb69bae99483291c00663c3d1d2ec0628a1c0abb4aae057cc7b004570c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.7.17-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:77cf883ffa62d74117fd7c6e4a998199f6fbb063e654a42b8046a6cfe3ce69b1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22686062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c027745c7d556a42156b262cea5fa7ff78b10d534ae6c2a4decd69caaeedaa26`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 21:55:17 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 12 Nov 2021 21:55:18 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Fri, 12 Nov 2021 21:55:38 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Fri, 12 Nov 2021 21:55:44 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 12 Nov 2021 21:55:45 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 12 Nov 2021 21:55:45 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 12 Nov 2021 21:55:45 GMT
EXPOSE 8888
# Fri, 12 Nov 2021 21:55:46 GMT
VOLUME [/var/lib/chronograf]
# Fri, 12 Nov 2021 21:55:46 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Fri, 12 Nov 2021 21:55:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 12 Nov 2021 21:55:46 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc79f199b43e46c5dfea12dfa8b92b7811e74b4d3812ff99c8368e4d2af803e7`  
		Last Modified: Fri, 12 Nov 2021 21:56:45 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aac166cdd02de2f1baf9250ebe4e1a5bec54cc49a59dbb3716570ed37d5bf63`  
		Last Modified: Fri, 12 Nov 2021 21:56:43 GMT  
		Size: 282.0 KB (281961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8283a3b7cad208670302a759a3e65783b946b1fb9221a8ab882fef07277d38d3`  
		Last Modified: Fri, 12 Nov 2021 21:56:59 GMT  
		Size: 19.6 MB (19556570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01b447bd4534f47d32c04a9937b72b986d155e25c02cb3add58d4a1c700940c3`  
		Last Modified: Fri, 12 Nov 2021 21:56:55 GMT  
		Size: 12.3 KB (12263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deac552aa1d37ccee70bddc7022a3ce80dad98b87b9fd130543f7fa787be0caa`  
		Last Modified: Fri, 12 Nov 2021 21:56:55 GMT  
		Size: 11.9 KB (11895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1656207cac83a586c1a7cf9aec72e8f8cc2ee68c672d3cf8403ff18631c28cf2`  
		Last Modified: Fri, 12 Nov 2021 21:56:55 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.8`

```console
$ docker pull chronograf@sha256:32bdc1f3c1aa14e1a3d75be5db9a8350b6008dc76eb887e76379011c658ec7fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.8` - linux; amd64

```console
$ docker pull chronograf@sha256:24c1489232c4bf49187cdc0e38ead9e9855d3508726a6319a36d62158cb0b55b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66239980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fe54eb7381d6db36efb4c18efc35948053c8f1bfcec2a74d833f72b09569d69`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 21 Dec 2021 01:24:41 GMT
ADD file:b1650c19c1dd1f4cff71553f2bb0bc949944d0bc24b54c318b2880c14538648a in / 
# Tue, 21 Dec 2021 01:24:42 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 02:06:33 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 21 Dec 2021 02:07:17 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Tue, 21 Dec 2021 02:07:25 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 21 Dec 2021 02:07:26 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 21 Dec 2021 02:07:26 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 21 Dec 2021 02:07:26 GMT
EXPOSE 8888
# Tue, 21 Dec 2021 02:07:26 GMT
VOLUME [/var/lib/chronograf]
# Tue, 21 Dec 2021 02:07:27 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 21 Dec 2021 02:07:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Dec 2021 02:07:27 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:35b2232c987ef3e6249ed229afcca51cd83320e08f6700022f4a3644a11f00f2`  
		Last Modified: Tue, 21 Dec 2021 01:31:36 GMT  
		Size: 22.5 MB (22529141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f793a6dcc9ba1d2eaa75faeeeb59be02b0ff06ca902fac32486ebe1c2c81b387`  
		Last Modified: Tue, 21 Dec 2021 02:08:07 GMT  
		Size: 6.8 MB (6760216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:103d8450209050e71541957f1076d1ddc8272aaeb330d6744938b6aab410adf4`  
		Last Modified: Tue, 21 Dec 2021 02:08:41 GMT  
		Size: 36.9 MB (36926228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1204ba88f6eba01d3ed46beb9cc3e66f1844dfc19e2f45966690c4ed284f7152`  
		Last Modified: Tue, 21 Dec 2021 02:08:36 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71c1c8490e0b569bfd1d22f0bdabfd1e96babfa3243297c7e1737c356c70d961`  
		Last Modified: Tue, 21 Dec 2021 02:08:36 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc3d4bd0cdcfb6d463feab4866595c849350110da76523dc6a646904d42841f6`  
		Last Modified: Tue, 21 Dec 2021 02:08:36 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.8` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:358ea5930855cd06c65f5b559cb52bf20c4096b977d8b0579b9c84210fedcfe2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.6 MB (59635407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2db9a87a58e7c5501eb1567faf81ca6ceeed2d38444f4b8bc783b0fb4ffe55e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 21 Dec 2021 02:05:40 GMT
ADD file:924a2e95e52f87fd6e79e8b0865e63f19432a71f823114b8b4d729ecd420d7fb in / 
# Tue, 21 Dec 2021 02:05:41 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 03:25:11 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 21 Dec 2021 03:26:55 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Tue, 21 Dec 2021 03:27:13 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 21 Dec 2021 03:27:14 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 21 Dec 2021 03:27:14 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 21 Dec 2021 03:27:15 GMT
EXPOSE 8888
# Tue, 21 Dec 2021 03:27:15 GMT
VOLUME [/var/lib/chronograf]
# Tue, 21 Dec 2021 03:27:16 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 21 Dec 2021 03:27:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Dec 2021 03:27:17 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:12790d92cf90440e36a3292fe34a336c54030e049074eb36386502daa81decea`  
		Last Modified: Tue, 21 Dec 2021 02:22:43 GMT  
		Size: 19.3 MB (19318715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8d896bc18835bd9e95e55d9744358d7ff742c715935b1ccc5f0793ac8c739b6`  
		Last Modified: Tue, 21 Dec 2021 03:28:51 GMT  
		Size: 5.8 MB (5780617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e01b32ee3c54737d2dce8e3c0748451e77f36873e3343e7b598b405baeb6774`  
		Last Modified: Tue, 21 Dec 2021 03:30:03 GMT  
		Size: 34.5 MB (34511673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67a67722c63c300f4e67b6dda73ed124ca8606d523e207ee23a8349cdb0c9b8d`  
		Last Modified: Tue, 21 Dec 2021 03:29:43 GMT  
		Size: 12.3 KB (12252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca34a4ce076ccca1d920c30455b9f9a4bdc4401afdf09fb51630627064808721`  
		Last Modified: Tue, 21 Dec 2021 03:29:43 GMT  
		Size: 11.9 KB (11911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:584b2f6f8f0a5cec313b639ad898ebee07a8e4d351bd99049ea453aad1fe0da4`  
		Last Modified: Tue, 21 Dec 2021 03:29:43 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.8` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:5a807c08d58c17825ca04e3eed8295863aa44a3bc81c17618f88920c0244d5ea
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60892065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b796b7ee829676b97c9ea63411e8352b4336d034b20e694bd4160fd06edb7ba`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 21 Dec 2021 01:44:39 GMT
ADD file:3bd088d09a71e361b1691e6fc4002843c7c0c3a591ac718d31a05b7eed3f1509 in / 
# Tue, 21 Dec 2021 01:44:40 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 10:38:10 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 21 Dec 2021 10:39:16 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Tue, 21 Dec 2021 10:39:25 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 21 Dec 2021 10:39:26 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 21 Dec 2021 10:39:27 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 21 Dec 2021 10:39:27 GMT
EXPOSE 8888
# Tue, 21 Dec 2021 10:39:28 GMT
VOLUME [/var/lib/chronograf]
# Tue, 21 Dec 2021 10:39:30 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 21 Dec 2021 10:39:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Dec 2021 10:39:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:0c10218d14f066bac4a45577b86a8b86e637c81535d33e71c03493e8ce5f0a30`  
		Last Modified: Tue, 21 Dec 2021 01:53:04 GMT  
		Size: 20.4 MB (20389374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:157c02822419c95c32eccbdc1c7e69e43f3c034ba9961d974480f4431e6062be`  
		Last Modified: Tue, 21 Dec 2021 10:40:17 GMT  
		Size: 6.0 MB (6046874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1908ddeebd145333485d198328a10060b747ba6123ac0944a07ea5fda6939c78`  
		Last Modified: Tue, 21 Dec 2021 10:40:50 GMT  
		Size: 34.4 MB (34431415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a9cebf28c960283b9ffc60c02fc7d0d39e88b02a42ea3e64e4d1b3a251da354`  
		Last Modified: Tue, 21 Dec 2021 10:40:45 GMT  
		Size: 12.3 KB (12252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c82d51247f4b623305ad4a8d00269592f65cf83a3ae06f48e0fbeff68a7b7c60`  
		Last Modified: Tue, 21 Dec 2021 10:40:45 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:732636b907c3c8b9a5ce0e81ce1863709f529804335f866a59383ab69e817eed`  
		Last Modified: Tue, 21 Dec 2021 10:40:45 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.8-alpine`

```console
$ docker pull chronograf@sha256:37af8f9a75619ff9a41d61b2395fad185b1daaf94aea63c81ca013ddcc112510
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.8-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:4f2fdffd0f89e9d26b360b63d1a7794d2511e88417b624fa63e82aceb3ecdea5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.3 MB (22333670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01ac33f8cebe8e52e9d28a37599d6205b0aa51c9ba34cd1e2bbf18b32324fe96`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 21:55:17 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 12 Nov 2021 21:55:18 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Fri, 12 Nov 2021 21:55:51 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Fri, 12 Nov 2021 21:56:00 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 12 Nov 2021 21:56:00 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 12 Nov 2021 21:56:00 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 12 Nov 2021 21:56:01 GMT
EXPOSE 8888
# Fri, 12 Nov 2021 21:56:01 GMT
VOLUME [/var/lib/chronograf]
# Fri, 12 Nov 2021 21:56:01 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Fri, 12 Nov 2021 21:56:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 12 Nov 2021 21:56:01 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc79f199b43e46c5dfea12dfa8b92b7811e74b4d3812ff99c8368e4d2af803e7`  
		Last Modified: Fri, 12 Nov 2021 21:56:45 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aac166cdd02de2f1baf9250ebe4e1a5bec54cc49a59dbb3716570ed37d5bf63`  
		Last Modified: Fri, 12 Nov 2021 21:56:43 GMT  
		Size: 282.0 KB (281961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:799e7fd8ed3ec32e09323ac48e268943b7d77fc4ed3a618a2a93ae2bef5d99d4`  
		Last Modified: Fri, 12 Nov 2021 21:57:13 GMT  
		Size: 19.2 MB (19204166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:126bd6c969f1bb9e4ad0a7f6f576cf330325d804279329adc1cc66549dc44358`  
		Last Modified: Fri, 12 Nov 2021 21:57:10 GMT  
		Size: 12.3 KB (12268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0a5f10b7fe32ea10409e5fabd241935dfd702349e179ae54173d56679568d9c`  
		Last Modified: Fri, 12 Nov 2021 21:57:09 GMT  
		Size: 11.9 KB (11901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:860006ae37408c8d020a52a83bc91fdb91f8aea8a67a319597dfcccb0268666f`  
		Last Modified: Fri, 12 Nov 2021 21:57:09 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.8.10`

```console
$ docker pull chronograf@sha256:32bdc1f3c1aa14e1a3d75be5db9a8350b6008dc76eb887e76379011c658ec7fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.8.10` - linux; amd64

```console
$ docker pull chronograf@sha256:24c1489232c4bf49187cdc0e38ead9e9855d3508726a6319a36d62158cb0b55b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66239980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fe54eb7381d6db36efb4c18efc35948053c8f1bfcec2a74d833f72b09569d69`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 21 Dec 2021 01:24:41 GMT
ADD file:b1650c19c1dd1f4cff71553f2bb0bc949944d0bc24b54c318b2880c14538648a in / 
# Tue, 21 Dec 2021 01:24:42 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 02:06:33 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 21 Dec 2021 02:07:17 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Tue, 21 Dec 2021 02:07:25 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 21 Dec 2021 02:07:26 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 21 Dec 2021 02:07:26 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 21 Dec 2021 02:07:26 GMT
EXPOSE 8888
# Tue, 21 Dec 2021 02:07:26 GMT
VOLUME [/var/lib/chronograf]
# Tue, 21 Dec 2021 02:07:27 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 21 Dec 2021 02:07:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Dec 2021 02:07:27 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:35b2232c987ef3e6249ed229afcca51cd83320e08f6700022f4a3644a11f00f2`  
		Last Modified: Tue, 21 Dec 2021 01:31:36 GMT  
		Size: 22.5 MB (22529141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f793a6dcc9ba1d2eaa75faeeeb59be02b0ff06ca902fac32486ebe1c2c81b387`  
		Last Modified: Tue, 21 Dec 2021 02:08:07 GMT  
		Size: 6.8 MB (6760216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:103d8450209050e71541957f1076d1ddc8272aaeb330d6744938b6aab410adf4`  
		Last Modified: Tue, 21 Dec 2021 02:08:41 GMT  
		Size: 36.9 MB (36926228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1204ba88f6eba01d3ed46beb9cc3e66f1844dfc19e2f45966690c4ed284f7152`  
		Last Modified: Tue, 21 Dec 2021 02:08:36 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71c1c8490e0b569bfd1d22f0bdabfd1e96babfa3243297c7e1737c356c70d961`  
		Last Modified: Tue, 21 Dec 2021 02:08:36 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc3d4bd0cdcfb6d463feab4866595c849350110da76523dc6a646904d42841f6`  
		Last Modified: Tue, 21 Dec 2021 02:08:36 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.8.10` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:358ea5930855cd06c65f5b559cb52bf20c4096b977d8b0579b9c84210fedcfe2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.6 MB (59635407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2db9a87a58e7c5501eb1567faf81ca6ceeed2d38444f4b8bc783b0fb4ffe55e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 21 Dec 2021 02:05:40 GMT
ADD file:924a2e95e52f87fd6e79e8b0865e63f19432a71f823114b8b4d729ecd420d7fb in / 
# Tue, 21 Dec 2021 02:05:41 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 03:25:11 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 21 Dec 2021 03:26:55 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Tue, 21 Dec 2021 03:27:13 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 21 Dec 2021 03:27:14 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 21 Dec 2021 03:27:14 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 21 Dec 2021 03:27:15 GMT
EXPOSE 8888
# Tue, 21 Dec 2021 03:27:15 GMT
VOLUME [/var/lib/chronograf]
# Tue, 21 Dec 2021 03:27:16 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 21 Dec 2021 03:27:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Dec 2021 03:27:17 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:12790d92cf90440e36a3292fe34a336c54030e049074eb36386502daa81decea`  
		Last Modified: Tue, 21 Dec 2021 02:22:43 GMT  
		Size: 19.3 MB (19318715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8d896bc18835bd9e95e55d9744358d7ff742c715935b1ccc5f0793ac8c739b6`  
		Last Modified: Tue, 21 Dec 2021 03:28:51 GMT  
		Size: 5.8 MB (5780617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e01b32ee3c54737d2dce8e3c0748451e77f36873e3343e7b598b405baeb6774`  
		Last Modified: Tue, 21 Dec 2021 03:30:03 GMT  
		Size: 34.5 MB (34511673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67a67722c63c300f4e67b6dda73ed124ca8606d523e207ee23a8349cdb0c9b8d`  
		Last Modified: Tue, 21 Dec 2021 03:29:43 GMT  
		Size: 12.3 KB (12252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca34a4ce076ccca1d920c30455b9f9a4bdc4401afdf09fb51630627064808721`  
		Last Modified: Tue, 21 Dec 2021 03:29:43 GMT  
		Size: 11.9 KB (11911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:584b2f6f8f0a5cec313b639ad898ebee07a8e4d351bd99049ea453aad1fe0da4`  
		Last Modified: Tue, 21 Dec 2021 03:29:43 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.8.10` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:5a807c08d58c17825ca04e3eed8295863aa44a3bc81c17618f88920c0244d5ea
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60892065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b796b7ee829676b97c9ea63411e8352b4336d034b20e694bd4160fd06edb7ba`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 21 Dec 2021 01:44:39 GMT
ADD file:3bd088d09a71e361b1691e6fc4002843c7c0c3a591ac718d31a05b7eed3f1509 in / 
# Tue, 21 Dec 2021 01:44:40 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 10:38:10 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 21 Dec 2021 10:39:16 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Tue, 21 Dec 2021 10:39:25 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 21 Dec 2021 10:39:26 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 21 Dec 2021 10:39:27 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 21 Dec 2021 10:39:27 GMT
EXPOSE 8888
# Tue, 21 Dec 2021 10:39:28 GMT
VOLUME [/var/lib/chronograf]
# Tue, 21 Dec 2021 10:39:30 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 21 Dec 2021 10:39:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Dec 2021 10:39:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:0c10218d14f066bac4a45577b86a8b86e637c81535d33e71c03493e8ce5f0a30`  
		Last Modified: Tue, 21 Dec 2021 01:53:04 GMT  
		Size: 20.4 MB (20389374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:157c02822419c95c32eccbdc1c7e69e43f3c034ba9961d974480f4431e6062be`  
		Last Modified: Tue, 21 Dec 2021 10:40:17 GMT  
		Size: 6.0 MB (6046874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1908ddeebd145333485d198328a10060b747ba6123ac0944a07ea5fda6939c78`  
		Last Modified: Tue, 21 Dec 2021 10:40:50 GMT  
		Size: 34.4 MB (34431415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a9cebf28c960283b9ffc60c02fc7d0d39e88b02a42ea3e64e4d1b3a251da354`  
		Last Modified: Tue, 21 Dec 2021 10:40:45 GMT  
		Size: 12.3 KB (12252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c82d51247f4b623305ad4a8d00269592f65cf83a3ae06f48e0fbeff68a7b7c60`  
		Last Modified: Tue, 21 Dec 2021 10:40:45 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:732636b907c3c8b9a5ce0e81ce1863709f529804335f866a59383ab69e817eed`  
		Last Modified: Tue, 21 Dec 2021 10:40:45 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.8.10-alpine`

```console
$ docker pull chronograf@sha256:37af8f9a75619ff9a41d61b2395fad185b1daaf94aea63c81ca013ddcc112510
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.8.10-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:4f2fdffd0f89e9d26b360b63d1a7794d2511e88417b624fa63e82aceb3ecdea5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.3 MB (22333670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01ac33f8cebe8e52e9d28a37599d6205b0aa51c9ba34cd1e2bbf18b32324fe96`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 21:55:17 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 12 Nov 2021 21:55:18 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Fri, 12 Nov 2021 21:55:51 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Fri, 12 Nov 2021 21:56:00 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 12 Nov 2021 21:56:00 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 12 Nov 2021 21:56:00 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 12 Nov 2021 21:56:01 GMT
EXPOSE 8888
# Fri, 12 Nov 2021 21:56:01 GMT
VOLUME [/var/lib/chronograf]
# Fri, 12 Nov 2021 21:56:01 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Fri, 12 Nov 2021 21:56:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 12 Nov 2021 21:56:01 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc79f199b43e46c5dfea12dfa8b92b7811e74b4d3812ff99c8368e4d2af803e7`  
		Last Modified: Fri, 12 Nov 2021 21:56:45 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aac166cdd02de2f1baf9250ebe4e1a5bec54cc49a59dbb3716570ed37d5bf63`  
		Last Modified: Fri, 12 Nov 2021 21:56:43 GMT  
		Size: 282.0 KB (281961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:799e7fd8ed3ec32e09323ac48e268943b7d77fc4ed3a618a2a93ae2bef5d99d4`  
		Last Modified: Fri, 12 Nov 2021 21:57:13 GMT  
		Size: 19.2 MB (19204166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:126bd6c969f1bb9e4ad0a7f6f576cf330325d804279329adc1cc66549dc44358`  
		Last Modified: Fri, 12 Nov 2021 21:57:10 GMT  
		Size: 12.3 KB (12268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0a5f10b7fe32ea10409e5fabd241935dfd702349e179ae54173d56679568d9c`  
		Last Modified: Fri, 12 Nov 2021 21:57:09 GMT  
		Size: 11.9 KB (11901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:860006ae37408c8d020a52a83bc91fdb91f8aea8a67a319597dfcccb0268666f`  
		Last Modified: Fri, 12 Nov 2021 21:57:09 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.9`

```console
$ docker pull chronograf@sha256:1ee54fdd64f63d3bdd897302e6199e676e266d8580585939ce945f345c1b7474
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.9` - linux; amd64

```console
$ docker pull chronograf@sha256:36b0885d46b59bd550a156d4cba30dade430afea834259bd51d494e999640286
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.9 MB (66882346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0e8fe8c1e538fd1cab12df4561c611663b13605d66c9feffb6360bb4950a8dd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 21 Dec 2021 01:24:41 GMT
ADD file:b1650c19c1dd1f4cff71553f2bb0bc949944d0bc24b54c318b2880c14538648a in / 
# Tue, 21 Dec 2021 01:24:42 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 02:06:33 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 21 Dec 2021 02:07:32 GMT
ENV CHRONOGRAF_VERSION=1.9.1
# Tue, 21 Dec 2021 02:07:40 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 21 Dec 2021 02:07:40 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 21 Dec 2021 02:07:40 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 21 Dec 2021 02:07:41 GMT
EXPOSE 8888
# Tue, 21 Dec 2021 02:07:41 GMT
VOLUME [/var/lib/chronograf]
# Tue, 21 Dec 2021 02:07:41 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 21 Dec 2021 02:07:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Dec 2021 02:07:41 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:35b2232c987ef3e6249ed229afcca51cd83320e08f6700022f4a3644a11f00f2`  
		Last Modified: Tue, 21 Dec 2021 01:31:36 GMT  
		Size: 22.5 MB (22529141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f793a6dcc9ba1d2eaa75faeeeb59be02b0ff06ca902fac32486ebe1c2c81b387`  
		Last Modified: Tue, 21 Dec 2021 02:08:07 GMT  
		Size: 6.8 MB (6760216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:803983a2507d1dd48ad71e86cbc337d38fcf63aedcfc57864213a6a61835d5d3`  
		Last Modified: Tue, 21 Dec 2021 02:08:56 GMT  
		Size: 37.6 MB (37568588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e2e39ba929e285f992fedc7c8745575d2829518617332d8f7098227d0dd2284`  
		Last Modified: Tue, 21 Dec 2021 02:08:51 GMT  
		Size: 12.3 KB (12251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40c2e226a2017fe45ca19eba7592b9602236a3ff815eba38aeba4c4c35f5e20d`  
		Last Modified: Tue, 21 Dec 2021 02:08:51 GMT  
		Size: 11.9 KB (11911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb5d1ec264a392fa5850c20a32ffe965aa0c925051411861ccd180b2fac08839`  
		Last Modified: Tue, 21 Dec 2021 02:08:51 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.9` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:3789bc1dd421aed199b169fd6d150c493e4e8c7f77091dc6f0a7b2cf895d6ae1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.4 MB (60402989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e404133019b5ea58a0a426cb7a67f491f58338b2cb2b3bce01aac2c004c54476`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 21 Dec 2021 02:05:40 GMT
ADD file:924a2e95e52f87fd6e79e8b0865e63f19432a71f823114b8b4d729ecd420d7fb in / 
# Tue, 21 Dec 2021 02:05:41 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 03:25:11 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 21 Dec 2021 03:27:28 GMT
ENV CHRONOGRAF_VERSION=1.9.1
# Tue, 21 Dec 2021 03:27:50 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 21 Dec 2021 03:27:50 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 21 Dec 2021 03:27:51 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 21 Dec 2021 03:27:51 GMT
EXPOSE 8888
# Tue, 21 Dec 2021 03:27:52 GMT
VOLUME [/var/lib/chronograf]
# Tue, 21 Dec 2021 03:27:52 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 21 Dec 2021 03:27:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Dec 2021 03:27:53 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:12790d92cf90440e36a3292fe34a336c54030e049074eb36386502daa81decea`  
		Last Modified: Tue, 21 Dec 2021 02:22:43 GMT  
		Size: 19.3 MB (19318715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8d896bc18835bd9e95e55d9744358d7ff742c715935b1ccc5f0793ac8c739b6`  
		Last Modified: Tue, 21 Dec 2021 03:28:51 GMT  
		Size: 5.8 MB (5780617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14aaafced9d5f74e8c450525883a6cfdc6ea827509c355c74a4cdccdf6d39347`  
		Last Modified: Tue, 21 Dec 2021 03:30:34 GMT  
		Size: 35.3 MB (35279257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4e6a7edd1e5846f1b7d7c958e6dc9da2bc8e16d0b3c5f68e27ef140b96e7481`  
		Last Modified: Tue, 21 Dec 2021 03:30:15 GMT  
		Size: 12.3 KB (12251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee3ccd9d48657d5d6b4286411e1cdf6165c4bf2fac47816a96cf4c52c86c22d3`  
		Last Modified: Tue, 21 Dec 2021 03:30:15 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34990d2306fc460b4a73ac46ef64b68c97528a5e4a8260e38b1cb74326209681`  
		Last Modified: Tue, 21 Dec 2021 03:30:15 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.9` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:37b7fb3e02d00d85c882b00f1a37f299be8e2e26c2a490f583058f9a6c250f50
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.6 MB (61623648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b31f957f9e32e99ad2bc5db34e5f327bb60cc1059af10e3ae516b663bae3ecc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 21 Dec 2021 01:44:39 GMT
ADD file:3bd088d09a71e361b1691e6fc4002843c7c0c3a591ac718d31a05b7eed3f1509 in / 
# Tue, 21 Dec 2021 01:44:40 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 10:38:10 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 21 Dec 2021 10:39:36 GMT
ENV CHRONOGRAF_VERSION=1.9.1
# Tue, 21 Dec 2021 10:39:45 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 21 Dec 2021 10:39:46 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 21 Dec 2021 10:39:47 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 21 Dec 2021 10:39:47 GMT
EXPOSE 8888
# Tue, 21 Dec 2021 10:39:48 GMT
VOLUME [/var/lib/chronograf]
# Tue, 21 Dec 2021 10:39:50 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 21 Dec 2021 10:39:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Dec 2021 10:39:51 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:0c10218d14f066bac4a45577b86a8b86e637c81535d33e71c03493e8ce5f0a30`  
		Last Modified: Tue, 21 Dec 2021 01:53:04 GMT  
		Size: 20.4 MB (20389374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:157c02822419c95c32eccbdc1c7e69e43f3c034ba9961d974480f4431e6062be`  
		Last Modified: Tue, 21 Dec 2021 10:40:17 GMT  
		Size: 6.0 MB (6046874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c43a2a97e28a6ee40e342b49c8993e7fe9fe5eea75e7c60c280209181184d54`  
		Last Modified: Tue, 21 Dec 2021 10:41:12 GMT  
		Size: 35.2 MB (35163004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:912647a7755913c1d564241a1e9642fed45713b69ac07e6fc98a118b3bbc7aaf`  
		Last Modified: Tue, 21 Dec 2021 10:41:07 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53e3ebb08119280f0ef5bc0e4f221913fcf5d6cdc5798bd769f55f90a2d88401`  
		Last Modified: Tue, 21 Dec 2021 10:41:07 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f389bf4822495952ea79159d2a486bba41cab58608888fceb26a38f822f6fd2c`  
		Last Modified: Tue, 21 Dec 2021 10:41:07 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.9-alpine`

```console
$ docker pull chronograf@sha256:61f1153f5cbb64d78ef85eeefcdece467687ac9f285bf2c82aa23e77298521cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.9-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:f058416548a083cd4eed1795030fe2a3f175baeb3975d0d6f39b3fa35c7a12ec
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.8 MB (22790730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2038b29989b30a347cc92f835d8bdbb8cf9b046a2d0e79bc93d5a6c33b044288`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 21:55:17 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 12 Nov 2021 21:55:18 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Fri, 12 Nov 2021 21:56:07 GMT
ENV CHRONOGRAF_VERSION=1.9.1
# Fri, 12 Nov 2021 21:56:16 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 12 Nov 2021 21:56:16 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 12 Nov 2021 21:56:16 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 12 Nov 2021 21:56:16 GMT
EXPOSE 8888
# Fri, 12 Nov 2021 21:56:17 GMT
VOLUME [/var/lib/chronograf]
# Fri, 12 Nov 2021 21:56:17 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Fri, 12 Nov 2021 21:56:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 12 Nov 2021 21:56:17 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc79f199b43e46c5dfea12dfa8b92b7811e74b4d3812ff99c8368e4d2af803e7`  
		Last Modified: Fri, 12 Nov 2021 21:56:45 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aac166cdd02de2f1baf9250ebe4e1a5bec54cc49a59dbb3716570ed37d5bf63`  
		Last Modified: Fri, 12 Nov 2021 21:56:43 GMT  
		Size: 282.0 KB (281961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99072c44d340c8a9fe28c4fc543e6c42b35b5d7346feeb7cbd368a2efea17527`  
		Last Modified: Fri, 12 Nov 2021 21:57:27 GMT  
		Size: 19.7 MB (19661235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d423a9c662479af0c48dc95fbc8c9990e352dcf3c918dde087acdc8447421a1e`  
		Last Modified: Fri, 12 Nov 2021 21:57:24 GMT  
		Size: 12.3 KB (12264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be23b2ea4c0096063257f0b44a67f6f18296d22e5a78dc135bbf2cfa43f07e72`  
		Last Modified: Fri, 12 Nov 2021 21:57:24 GMT  
		Size: 11.9 KB (11896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75249649e859aeb1cdabcd6daf012c9ad8b86ea19843eb9c30100a835327d4be`  
		Last Modified: Fri, 12 Nov 2021 21:57:24 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.9.1`

```console
$ docker pull chronograf@sha256:1ee54fdd64f63d3bdd897302e6199e676e266d8580585939ce945f345c1b7474
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.9.1` - linux; amd64

```console
$ docker pull chronograf@sha256:36b0885d46b59bd550a156d4cba30dade430afea834259bd51d494e999640286
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.9 MB (66882346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0e8fe8c1e538fd1cab12df4561c611663b13605d66c9feffb6360bb4950a8dd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 21 Dec 2021 01:24:41 GMT
ADD file:b1650c19c1dd1f4cff71553f2bb0bc949944d0bc24b54c318b2880c14538648a in / 
# Tue, 21 Dec 2021 01:24:42 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 02:06:33 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 21 Dec 2021 02:07:32 GMT
ENV CHRONOGRAF_VERSION=1.9.1
# Tue, 21 Dec 2021 02:07:40 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 21 Dec 2021 02:07:40 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 21 Dec 2021 02:07:40 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 21 Dec 2021 02:07:41 GMT
EXPOSE 8888
# Tue, 21 Dec 2021 02:07:41 GMT
VOLUME [/var/lib/chronograf]
# Tue, 21 Dec 2021 02:07:41 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 21 Dec 2021 02:07:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Dec 2021 02:07:41 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:35b2232c987ef3e6249ed229afcca51cd83320e08f6700022f4a3644a11f00f2`  
		Last Modified: Tue, 21 Dec 2021 01:31:36 GMT  
		Size: 22.5 MB (22529141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f793a6dcc9ba1d2eaa75faeeeb59be02b0ff06ca902fac32486ebe1c2c81b387`  
		Last Modified: Tue, 21 Dec 2021 02:08:07 GMT  
		Size: 6.8 MB (6760216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:803983a2507d1dd48ad71e86cbc337d38fcf63aedcfc57864213a6a61835d5d3`  
		Last Modified: Tue, 21 Dec 2021 02:08:56 GMT  
		Size: 37.6 MB (37568588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e2e39ba929e285f992fedc7c8745575d2829518617332d8f7098227d0dd2284`  
		Last Modified: Tue, 21 Dec 2021 02:08:51 GMT  
		Size: 12.3 KB (12251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40c2e226a2017fe45ca19eba7592b9602236a3ff815eba38aeba4c4c35f5e20d`  
		Last Modified: Tue, 21 Dec 2021 02:08:51 GMT  
		Size: 11.9 KB (11911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb5d1ec264a392fa5850c20a32ffe965aa0c925051411861ccd180b2fac08839`  
		Last Modified: Tue, 21 Dec 2021 02:08:51 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.9.1` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:3789bc1dd421aed199b169fd6d150c493e4e8c7f77091dc6f0a7b2cf895d6ae1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.4 MB (60402989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e404133019b5ea58a0a426cb7a67f491f58338b2cb2b3bce01aac2c004c54476`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 21 Dec 2021 02:05:40 GMT
ADD file:924a2e95e52f87fd6e79e8b0865e63f19432a71f823114b8b4d729ecd420d7fb in / 
# Tue, 21 Dec 2021 02:05:41 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 03:25:11 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 21 Dec 2021 03:27:28 GMT
ENV CHRONOGRAF_VERSION=1.9.1
# Tue, 21 Dec 2021 03:27:50 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 21 Dec 2021 03:27:50 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 21 Dec 2021 03:27:51 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 21 Dec 2021 03:27:51 GMT
EXPOSE 8888
# Tue, 21 Dec 2021 03:27:52 GMT
VOLUME [/var/lib/chronograf]
# Tue, 21 Dec 2021 03:27:52 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 21 Dec 2021 03:27:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Dec 2021 03:27:53 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:12790d92cf90440e36a3292fe34a336c54030e049074eb36386502daa81decea`  
		Last Modified: Tue, 21 Dec 2021 02:22:43 GMT  
		Size: 19.3 MB (19318715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8d896bc18835bd9e95e55d9744358d7ff742c715935b1ccc5f0793ac8c739b6`  
		Last Modified: Tue, 21 Dec 2021 03:28:51 GMT  
		Size: 5.8 MB (5780617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14aaafced9d5f74e8c450525883a6cfdc6ea827509c355c74a4cdccdf6d39347`  
		Last Modified: Tue, 21 Dec 2021 03:30:34 GMT  
		Size: 35.3 MB (35279257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4e6a7edd1e5846f1b7d7c958e6dc9da2bc8e16d0b3c5f68e27ef140b96e7481`  
		Last Modified: Tue, 21 Dec 2021 03:30:15 GMT  
		Size: 12.3 KB (12251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee3ccd9d48657d5d6b4286411e1cdf6165c4bf2fac47816a96cf4c52c86c22d3`  
		Last Modified: Tue, 21 Dec 2021 03:30:15 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34990d2306fc460b4a73ac46ef64b68c97528a5e4a8260e38b1cb74326209681`  
		Last Modified: Tue, 21 Dec 2021 03:30:15 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.9.1` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:37b7fb3e02d00d85c882b00f1a37f299be8e2e26c2a490f583058f9a6c250f50
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.6 MB (61623648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b31f957f9e32e99ad2bc5db34e5f327bb60cc1059af10e3ae516b663bae3ecc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 21 Dec 2021 01:44:39 GMT
ADD file:3bd088d09a71e361b1691e6fc4002843c7c0c3a591ac718d31a05b7eed3f1509 in / 
# Tue, 21 Dec 2021 01:44:40 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 10:38:10 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 21 Dec 2021 10:39:36 GMT
ENV CHRONOGRAF_VERSION=1.9.1
# Tue, 21 Dec 2021 10:39:45 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 21 Dec 2021 10:39:46 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 21 Dec 2021 10:39:47 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 21 Dec 2021 10:39:47 GMT
EXPOSE 8888
# Tue, 21 Dec 2021 10:39:48 GMT
VOLUME [/var/lib/chronograf]
# Tue, 21 Dec 2021 10:39:50 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 21 Dec 2021 10:39:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Dec 2021 10:39:51 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:0c10218d14f066bac4a45577b86a8b86e637c81535d33e71c03493e8ce5f0a30`  
		Last Modified: Tue, 21 Dec 2021 01:53:04 GMT  
		Size: 20.4 MB (20389374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:157c02822419c95c32eccbdc1c7e69e43f3c034ba9961d974480f4431e6062be`  
		Last Modified: Tue, 21 Dec 2021 10:40:17 GMT  
		Size: 6.0 MB (6046874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c43a2a97e28a6ee40e342b49c8993e7fe9fe5eea75e7c60c280209181184d54`  
		Last Modified: Tue, 21 Dec 2021 10:41:12 GMT  
		Size: 35.2 MB (35163004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:912647a7755913c1d564241a1e9642fed45713b69ac07e6fc98a118b3bbc7aaf`  
		Last Modified: Tue, 21 Dec 2021 10:41:07 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53e3ebb08119280f0ef5bc0e4f221913fcf5d6cdc5798bd769f55f90a2d88401`  
		Last Modified: Tue, 21 Dec 2021 10:41:07 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f389bf4822495952ea79159d2a486bba41cab58608888fceb26a38f822f6fd2c`  
		Last Modified: Tue, 21 Dec 2021 10:41:07 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.9.1-alpine`

```console
$ docker pull chronograf@sha256:61f1153f5cbb64d78ef85eeefcdece467687ac9f285bf2c82aa23e77298521cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.9.1-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:f058416548a083cd4eed1795030fe2a3f175baeb3975d0d6f39b3fa35c7a12ec
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.8 MB (22790730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2038b29989b30a347cc92f835d8bdbb8cf9b046a2d0e79bc93d5a6c33b044288`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 21:55:17 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 12 Nov 2021 21:55:18 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Fri, 12 Nov 2021 21:56:07 GMT
ENV CHRONOGRAF_VERSION=1.9.1
# Fri, 12 Nov 2021 21:56:16 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 12 Nov 2021 21:56:16 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 12 Nov 2021 21:56:16 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 12 Nov 2021 21:56:16 GMT
EXPOSE 8888
# Fri, 12 Nov 2021 21:56:17 GMT
VOLUME [/var/lib/chronograf]
# Fri, 12 Nov 2021 21:56:17 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Fri, 12 Nov 2021 21:56:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 12 Nov 2021 21:56:17 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc79f199b43e46c5dfea12dfa8b92b7811e74b4d3812ff99c8368e4d2af803e7`  
		Last Modified: Fri, 12 Nov 2021 21:56:45 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aac166cdd02de2f1baf9250ebe4e1a5bec54cc49a59dbb3716570ed37d5bf63`  
		Last Modified: Fri, 12 Nov 2021 21:56:43 GMT  
		Size: 282.0 KB (281961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99072c44d340c8a9fe28c4fc543e6c42b35b5d7346feeb7cbd368a2efea17527`  
		Last Modified: Fri, 12 Nov 2021 21:57:27 GMT  
		Size: 19.7 MB (19661235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d423a9c662479af0c48dc95fbc8c9990e352dcf3c918dde087acdc8447421a1e`  
		Last Modified: Fri, 12 Nov 2021 21:57:24 GMT  
		Size: 12.3 KB (12264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be23b2ea4c0096063257f0b44a67f6f18296d22e5a78dc135bbf2cfa43f07e72`  
		Last Modified: Fri, 12 Nov 2021 21:57:24 GMT  
		Size: 11.9 KB (11896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75249649e859aeb1cdabcd6daf012c9ad8b86ea19843eb9c30100a835327d4be`  
		Last Modified: Fri, 12 Nov 2021 21:57:24 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:alpine`

```console
$ docker pull chronograf@sha256:61f1153f5cbb64d78ef85eeefcdece467687ac9f285bf2c82aa23e77298521cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:f058416548a083cd4eed1795030fe2a3f175baeb3975d0d6f39b3fa35c7a12ec
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.8 MB (22790730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2038b29989b30a347cc92f835d8bdbb8cf9b046a2d0e79bc93d5a6c33b044288`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 21:55:17 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 12 Nov 2021 21:55:18 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Fri, 12 Nov 2021 21:56:07 GMT
ENV CHRONOGRAF_VERSION=1.9.1
# Fri, 12 Nov 2021 21:56:16 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 12 Nov 2021 21:56:16 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 12 Nov 2021 21:56:16 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 12 Nov 2021 21:56:16 GMT
EXPOSE 8888
# Fri, 12 Nov 2021 21:56:17 GMT
VOLUME [/var/lib/chronograf]
# Fri, 12 Nov 2021 21:56:17 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Fri, 12 Nov 2021 21:56:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 12 Nov 2021 21:56:17 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc79f199b43e46c5dfea12dfa8b92b7811e74b4d3812ff99c8368e4d2af803e7`  
		Last Modified: Fri, 12 Nov 2021 21:56:45 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aac166cdd02de2f1baf9250ebe4e1a5bec54cc49a59dbb3716570ed37d5bf63`  
		Last Modified: Fri, 12 Nov 2021 21:56:43 GMT  
		Size: 282.0 KB (281961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99072c44d340c8a9fe28c4fc543e6c42b35b5d7346feeb7cbd368a2efea17527`  
		Last Modified: Fri, 12 Nov 2021 21:57:27 GMT  
		Size: 19.7 MB (19661235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d423a9c662479af0c48dc95fbc8c9990e352dcf3c918dde087acdc8447421a1e`  
		Last Modified: Fri, 12 Nov 2021 21:57:24 GMT  
		Size: 12.3 KB (12264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be23b2ea4c0096063257f0b44a67f6f18296d22e5a78dc135bbf2cfa43f07e72`  
		Last Modified: Fri, 12 Nov 2021 21:57:24 GMT  
		Size: 11.9 KB (11896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75249649e859aeb1cdabcd6daf012c9ad8b86ea19843eb9c30100a835327d4be`  
		Last Modified: Fri, 12 Nov 2021 21:57:24 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:latest`

```console
$ docker pull chronograf@sha256:1ee54fdd64f63d3bdd897302e6199e676e266d8580585939ce945f345c1b7474
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:latest` - linux; amd64

```console
$ docker pull chronograf@sha256:36b0885d46b59bd550a156d4cba30dade430afea834259bd51d494e999640286
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.9 MB (66882346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0e8fe8c1e538fd1cab12df4561c611663b13605d66c9feffb6360bb4950a8dd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 21 Dec 2021 01:24:41 GMT
ADD file:b1650c19c1dd1f4cff71553f2bb0bc949944d0bc24b54c318b2880c14538648a in / 
# Tue, 21 Dec 2021 01:24:42 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 02:06:33 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 21 Dec 2021 02:07:32 GMT
ENV CHRONOGRAF_VERSION=1.9.1
# Tue, 21 Dec 2021 02:07:40 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 21 Dec 2021 02:07:40 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 21 Dec 2021 02:07:40 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 21 Dec 2021 02:07:41 GMT
EXPOSE 8888
# Tue, 21 Dec 2021 02:07:41 GMT
VOLUME [/var/lib/chronograf]
# Tue, 21 Dec 2021 02:07:41 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 21 Dec 2021 02:07:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Dec 2021 02:07:41 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:35b2232c987ef3e6249ed229afcca51cd83320e08f6700022f4a3644a11f00f2`  
		Last Modified: Tue, 21 Dec 2021 01:31:36 GMT  
		Size: 22.5 MB (22529141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f793a6dcc9ba1d2eaa75faeeeb59be02b0ff06ca902fac32486ebe1c2c81b387`  
		Last Modified: Tue, 21 Dec 2021 02:08:07 GMT  
		Size: 6.8 MB (6760216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:803983a2507d1dd48ad71e86cbc337d38fcf63aedcfc57864213a6a61835d5d3`  
		Last Modified: Tue, 21 Dec 2021 02:08:56 GMT  
		Size: 37.6 MB (37568588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e2e39ba929e285f992fedc7c8745575d2829518617332d8f7098227d0dd2284`  
		Last Modified: Tue, 21 Dec 2021 02:08:51 GMT  
		Size: 12.3 KB (12251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40c2e226a2017fe45ca19eba7592b9602236a3ff815eba38aeba4c4c35f5e20d`  
		Last Modified: Tue, 21 Dec 2021 02:08:51 GMT  
		Size: 11.9 KB (11911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb5d1ec264a392fa5850c20a32ffe965aa0c925051411861ccd180b2fac08839`  
		Last Modified: Tue, 21 Dec 2021 02:08:51 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:latest` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:3789bc1dd421aed199b169fd6d150c493e4e8c7f77091dc6f0a7b2cf895d6ae1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.4 MB (60402989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e404133019b5ea58a0a426cb7a67f491f58338b2cb2b3bce01aac2c004c54476`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 21 Dec 2021 02:05:40 GMT
ADD file:924a2e95e52f87fd6e79e8b0865e63f19432a71f823114b8b4d729ecd420d7fb in / 
# Tue, 21 Dec 2021 02:05:41 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 03:25:11 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 21 Dec 2021 03:27:28 GMT
ENV CHRONOGRAF_VERSION=1.9.1
# Tue, 21 Dec 2021 03:27:50 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 21 Dec 2021 03:27:50 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 21 Dec 2021 03:27:51 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 21 Dec 2021 03:27:51 GMT
EXPOSE 8888
# Tue, 21 Dec 2021 03:27:52 GMT
VOLUME [/var/lib/chronograf]
# Tue, 21 Dec 2021 03:27:52 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 21 Dec 2021 03:27:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Dec 2021 03:27:53 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:12790d92cf90440e36a3292fe34a336c54030e049074eb36386502daa81decea`  
		Last Modified: Tue, 21 Dec 2021 02:22:43 GMT  
		Size: 19.3 MB (19318715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8d896bc18835bd9e95e55d9744358d7ff742c715935b1ccc5f0793ac8c739b6`  
		Last Modified: Tue, 21 Dec 2021 03:28:51 GMT  
		Size: 5.8 MB (5780617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14aaafced9d5f74e8c450525883a6cfdc6ea827509c355c74a4cdccdf6d39347`  
		Last Modified: Tue, 21 Dec 2021 03:30:34 GMT  
		Size: 35.3 MB (35279257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4e6a7edd1e5846f1b7d7c958e6dc9da2bc8e16d0b3c5f68e27ef140b96e7481`  
		Last Modified: Tue, 21 Dec 2021 03:30:15 GMT  
		Size: 12.3 KB (12251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee3ccd9d48657d5d6b4286411e1cdf6165c4bf2fac47816a96cf4c52c86c22d3`  
		Last Modified: Tue, 21 Dec 2021 03:30:15 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34990d2306fc460b4a73ac46ef64b68c97528a5e4a8260e38b1cb74326209681`  
		Last Modified: Tue, 21 Dec 2021 03:30:15 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:latest` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:37b7fb3e02d00d85c882b00f1a37f299be8e2e26c2a490f583058f9a6c250f50
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.6 MB (61623648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b31f957f9e32e99ad2bc5db34e5f327bb60cc1059af10e3ae516b663bae3ecc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 21 Dec 2021 01:44:39 GMT
ADD file:3bd088d09a71e361b1691e6fc4002843c7c0c3a591ac718d31a05b7eed3f1509 in / 
# Tue, 21 Dec 2021 01:44:40 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 10:38:10 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 21 Dec 2021 10:39:36 GMT
ENV CHRONOGRAF_VERSION=1.9.1
# Tue, 21 Dec 2021 10:39:45 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 21 Dec 2021 10:39:46 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 21 Dec 2021 10:39:47 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 21 Dec 2021 10:39:47 GMT
EXPOSE 8888
# Tue, 21 Dec 2021 10:39:48 GMT
VOLUME [/var/lib/chronograf]
# Tue, 21 Dec 2021 10:39:50 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 21 Dec 2021 10:39:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Dec 2021 10:39:51 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:0c10218d14f066bac4a45577b86a8b86e637c81535d33e71c03493e8ce5f0a30`  
		Last Modified: Tue, 21 Dec 2021 01:53:04 GMT  
		Size: 20.4 MB (20389374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:157c02822419c95c32eccbdc1c7e69e43f3c034ba9961d974480f4431e6062be`  
		Last Modified: Tue, 21 Dec 2021 10:40:17 GMT  
		Size: 6.0 MB (6046874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c43a2a97e28a6ee40e342b49c8993e7fe9fe5eea75e7c60c280209181184d54`  
		Last Modified: Tue, 21 Dec 2021 10:41:12 GMT  
		Size: 35.2 MB (35163004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:912647a7755913c1d564241a1e9642fed45713b69ac07e6fc98a118b3bbc7aaf`  
		Last Modified: Tue, 21 Dec 2021 10:41:07 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53e3ebb08119280f0ef5bc0e4f221913fcf5d6cdc5798bd769f55f90a2d88401`  
		Last Modified: Tue, 21 Dec 2021 10:41:07 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f389bf4822495952ea79159d2a486bba41cab58608888fceb26a38f822f6fd2c`  
		Last Modified: Tue, 21 Dec 2021 10:41:07 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
